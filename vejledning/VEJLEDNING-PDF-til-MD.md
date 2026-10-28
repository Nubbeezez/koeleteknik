# Vejledning til Claude: PDF-manualer → Markdown til fejlfindingsprojekt

Denne fil beskriver, hvordan PDF-manualer til køleregulatorer (Danfoss, Dixell, Carel m.fl.) laves om til Markdown-filer, der kan uploades som "Project knowledge" i et Claude-projekt på claude.ai. Følg vejledningen, når brugeren beder om "MD-filer af manualerne" eller lignende.

## Resultatet brugeren forventer

- Manualerne ligger i en mappe pr. mærke: `Danfoss/`, `Dixell/`, `Carel/` osv.
- **Danfoss og Carel:** én undermappe pr. regulator. Der laves **én MD-fil pr. undermappe**, gemt i undermappen og navngivet efter den, fx `Danfoss/AK-PC 782A/AK-PC 782A.md`. Ligger der flere PDF'er i samme undermappe, **samles de i den ene fil** med en indholdsfortegnelse øverst. Den største PDF (typisk hovedmanualen) kommer først.
- **Dixell:** PDF'erne ligger direkte i `Dixell/`. Der laves **én MD-fil pr. model**, navngivet efter modellen, fx `Dixell/XR70CX.md`.
- Teksten beholdes på **originalsproget** (oftest engelsk). Den skal ikke oversættes. Claude i projektet svarer alligevel på dansk. Er en PDF tosproget, tages kun den engelske (eller danske) del med.
- Lav **ikke** én samlet fil for alle mapper.
- Øverst i hver fil står en kort vejledning til projektets Claude. Scriptet indsætter den automatisk.

Eksempel på mappestruktur:

```
manualer til claude/
├── Danfoss/
│   ├── AK-CC 55 Single Coil/
│   │   ├── BC364229688105en-000201.pdf
│   │   └── AK-CC 55 Single Coil.md      ← genereret
│   └── AK-PC 782A/
│       ├── BC245386497365en-001201.pdf
│       ├── AU479234099123en-000101.pdf
│       └── AK-PC 782A.md                ← genereret (2+ manualer samlet)
├── Dixell/
│   ├── XR70CX-GB.pdf
│   └── XR70CX.md                        ← genereret
├── Carel/
│   └── easy/
│       ├── User-Manual-CAREL-PJEZ-Controllers.pdf
│       └── easy.md                      ← genereret
└── Noget om Køleteknik/                 ← lærebog, se særskilt afsnit
```

## Fremgangsmåde

1. **Installér værktøjet** (kun første gang):
   ```
   python -m pip install pymupdf4llm
   ```
   Brug PyMuPDF (`pymupdf4llm`) og **ikke** `pdftotext`. `pdftotext` mister ligaturerne fi, fl og ff i Danfoss-PDF'erne ("configuration" bliver til "con guration"), og tabellerne bliver ulæselige. `pymupdf4llm` laver rigtige Markdown-tabeller, og det er vigtigt for alarm- og parametertabeller.

2. **Gem scriptet** nedenfor som `pdf_til_md.py`. Læg det uden for manualmappen, fx i en midlertidig mappe.

3. **Kør det på mærkemappen** (Danfoss, Carel …):
   - Alle undermapper: `python pdf_til_md.py "C:\sti\til\manualer til claude\Danfoss"`
   - Kun én ny undermappe: `python pdf_til_md.py "C:\sti\til\manualer til claude\Danfoss" "AK-PC 782A"`

   Mærkemappens navn bruges i filens overskrift. Advarslen "RapidOCR is missing" kan ignoreres. Store manualer (300+ sider) tager et par minutter.

4. **Dixell-manualer (og andre tospaltede manualer):** Dixell sætter teksten i to spalter, og så kommer afsnittene ud i forkert rækkefølge (fx 3.3 før 1). Del først hver side i venstre og højre halvdel med funktionen `split_columns` nedenfor, og konvertér derefter den opdelte PDF. Tjek bagefter, at overskrifterne står i rækkefølge (1, 1.1, 2, 3 …). Folderark med 3–4 spalter eller blandet kinesisk/engelsk giver ofte stadig rod. Så er det bedre at springe dem over og sige det til brugeren end at levere en rodet fil.

5. **Kontrollér resultatet** før du melder tilbage:
   - Søg efter `© Danfoss` og `<mark>`. Der bør være 0 forekomster. Er der rester, så udvid `FOOTER_RES` i scriptet og kør igen.
   - Find alarmtabellerne (søg fx på `A01`, `E25`, `HA` eller `Alarm`), og tjek at de står som tabeller med kode, tekst og beskrivelse.
   - Kig efter ord med manglende bogstaver. Der var ét kendt tilfælde i den danske AK-CC 550-manual: "Aarmreæet vi ive ativeret …" skulle være "Alarmrelæet vil blive aktiveret …". Ret den slags i hånden direkte i MD-filen.
   - Se indholdsfortegnelsen i filer med flere manualer. Er en titel misvisende, så ret den i hånden.

6. **Meld tilbage til brugeren** med stien til hver fil, filstørrelsen og antallet af manualer i hver fil, og nævn ting du har rettet i hånden eller sprunget over.

## Når brugeren beder dig hente nye manualer

- **Spørg først.** Vis en liste over de regulatorer, du vil hente manualer til, og lad brugeren vælge, før du downloader noget.
- Hent kun fra producenten eller en kendt forhandler, der har lagt producentens egen PDF op:
  - **Danfoss:** `assets.danfoss.com/documents/<id>/<dokumentnr>.pdf`. Vælg filer med `en` i navnet (fx `BC…en-000201.pdf`). Bemærk: serveren ser kun på `<id>`. Skifter du sprogkoden i filnavnet, får du stadig samme (fx russiske) fil, så tjek altid forsiden.
  - **Dixell:** Copeland har de engelske manualer på `webapps.copeland.com/Dixell/Content/Pages/Manuals/<serie>/<MODEL>/<MODEL>-GB.pdf`, fx serien `XR-CX` (XR20CX, XR30CX, XR60CX, XR70CX, XR75CX) og `WING` (XW60K, XW264K, XW-L-modeller).
  - **Carel:** Carels egne PDF'er ligger ofte hos forhandlere (fx Reece). Mange Carel-manualer er tosprogede.
- Brug ikke ManualsLib, Scribd eller lignende sider, og prøv ikke at komme uden om sider, der blokerer download (403).
- Tjek forsiden på hver PDF efter download (`pdftotext -l 1 fil.pdf -`): er det den rigtige model, og er det på engelsk eller dansk?
- Udgåede modeller (fx EKC 315A/316A, som er erstattet af EKE 1) har ofte kun korte instruktionsark. Sig det til brugeren.

## Lærebøger og andre ikke-manualer

En lærebog som "Noget om køleteknik" skal **ikke** gennem reglen om gentagne linjer, for så forsvinder overskrifter som "Fejlfinding", der står på hver side. Konvertér med `pymupdf4llm`, fjern kun sidetal (linjer med kun et tal) og `<mark>`-tags, og skriv en overskrift og vejledning, der passer til en lærebog (udgivelsesår, at lovgivning kan være ændret siden, at regulatormanualer går forud).

## Hvad scriptet gør

- Konverterer hver PDF til Markdown med tabeller (billeder udelades).
- Fjerner sidefødder (© Danfoss, dokumentnummer | sidetal, ældre "RS8…/RI8… © Danfoss"-fødder) og gentagne sidehoveder (linjer der går igen 5 gange eller mere).
- Laver tekst fra diagrammer om til en kort linje: `*[Figurtekst: … · … ]*`.
- Skubber manualernes overskrifter 2 niveauer ned, så `#` er filens titel og `##` er hver manual.
- Finder hver manuals titel ud fra de første linjer, fx "User Guide – System Manager AK-SM 800A series".

## Scriptet: `pdf_til_md.py`

```python
"""Konverterer PDF-manualer (Danfoss, Carel m.fl.) til én Markdown-fil pr. mappe.

Brug:  python pdf_til_md.py "<mærkemappe, fx .../manualer til claude/Danfoss>" ["<undermappe>"]
Uden undermappe behandles alle undermapper med PDF'er i mærkemappen.
Mærkemappens navn (Danfoss, Carel ...) bruges i filens overskrift.
"""
import re, sys, pathlib, collections
import pymupdf4llm


FOOTER_RES = [
    re.compile(r"^(\d+\s*\|\s*)?©\s*Danfoss"),                    # copyright-fod
    re.compile(r"^[A-Z]{2}\d{12}[a-z]{2}-\d{6}\s*(\|\s*\d+)?$"),  # dokumentnr. | sidetal
    re.compile(r"^[\w -]{0,12}(Manual |User Guide |Instructions )?R[SI]8\w+ © Danfoss [\d./-]+( AK-\w+ \w+)?$"),  # ældre manualers fod
    re.compile(r"^(User Guide|Quick Setup Guide|Application Guide|Operating Guide|Programming Guide|Installation Guide|Data sheet)\s*\|"),
    re.compile(r"^Danfoss\s+\w+$"),                                # tegningsnumre
]
PIC_RE = re.compile(r"<!-- Start of picture text -->(.*?)<!-- End of picture text -->", re.S)

def norm(line):
    return re.sub(r"[#*\s]+", " ", line).strip()

def clean(text):
    text = text.replace("<mark>", "").replace("</mark>", "")

    def pic(m):
        parts = [p.strip() for p in m.group(1).split("<br>") if p.strip()]
        parts = [p for p in parts if not re.fullmatch(r"Danfoss\s+\w+", p)]
        body = " · ".join(parts)
        return f"*[Figurtekst: {body}]*" if len(body) >= 15 else ""
    text = PIC_RE.sub(pic, text)

    lines = [l.rstrip() for l in text.splitlines()]
    skip = ("|", ">", "-", "*[")
    counts = collections.Counter(norm(l) for l in lines if l.strip() and not l.lstrip().startswith(skip))
    out = []
    for l in lines:
        s = norm(l)
        if any(r.search(s) for r in FOOTER_RES):
            continue
        # linjer der går igen 5+ gange er sidehoveder (tabeller/lister/noter undtaget)
        if s and counts[s] >= 5 and not l.lstrip().startswith(("|", ">", "-")) and "NOTE" not in s.upper():
            continue
        m = re.match(r"^(#{1,6})\s+(.*)$", l)
        if m:  # skub overskrifter 2 niveauer ned under fil- og manualoverskrift
            if not norm(m.group(2)):
                continue
            l = "#" * min(len(m.group(1)) + 2, 6) + " " + m.group(2).strip()
        out.append(l)
    return re.sub(r"\n{3,}", "\n\n", "\n".join(out)).strip()

def guess_title(md):
    """Første par meningsfulde overskrifter/linjer, fx 'User Guide – AK-PC 782A'."""
    found = []
    for l in md.splitlines():
        t = re.sub(r"<[^>]+>|[#*|]", " ", l)
        t = re.sub(r"\s+", " ", t).strip()
        if len(t) < 3 or t.startswith("[Figurtekst") or t.lower().startswith("www."):
            continue
        found.append(t)
        if len(found) == 2:
            break
    return " – ".join(found)[:150] or "Manual"

HEADER = """# {brand} {folder} – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.
"""

def main():
  ROOT = pathlib.Path(sys.argv[1])
  ONLY = sys.argv[2] if len(sys.argv) > 2 else None
  folders = [ROOT / ONLY] if ONLY else sorted(p for p in ROOT.iterdir() if p.is_dir())
  for folder in folders:
      pdfs = sorted(folder.glob("*.pdf"), key=lambda p: p.stat().st_size, reverse=True)  # største (hovedmanual) først
      if not pdfs:
          continue
      docs = []
      for pdf in pdfs:
          raw = pymupdf4llm.to_markdown(str(pdf), ignore_images=True, show_progress=False)
          body = clean(raw)
          docs.append((pdf.stem, guess_title(body), body))
      parts = [HEADER.format(brand=ROOT.name, folder=folder.name)]
      if len(docs) > 1:
          parts.append("## Indhold\n")
          parts += [f"{i}. {t}" for i, (_, t, _) in enumerate(docs, 1)]
          parts.append("")
      for i, (stem, title, body) in enumerate(docs, 1):
          parts.append("\n---\n")
          parts.append(f"## {i}. {title}\n" if len(docs) > 1 else f"## {title}\n")
          parts.append(f"*Kilde: Danfoss-dokument {stem}.pdf*\n")
          parts.append(body)
      out = folder / f"{folder.name}.md"
      out.write_text("\n".join(parts) + "\n", encoding="utf-8")
      print(f"{out}  ({out.stat().st_size // 1024} KB, {len(docs)} manual(er))")


if __name__ == "__main__":
    main()
```

## Spalteopdeling til Dixell: `split_columns`

Kør `split_columns("XR70CX-GB.pdf", "XR70CX_split.pdf")`, og konvertér derefter `XR70CX_split.pdf` med `pymupdf4llm.to_markdown` og `clean()` fra scriptet ovenfor. Gem resultatet som `Dixell/XR70CX.md` med en tilsvarende overskrift og vejledning øverst.

```python
import pymupdf

def split_columns(src, out):
    doc, new = pymupdf.open(src), pymupdf.open()
    for page in doc:
        r = page.rect
        mid = r.x0 + r.width / 2
        for clip in (pymupdf.Rect(r.x0, r.y0, mid, r.y1), pymupdf.Rect(mid, r.y0, r.x1, r.y1)):
            p = new.new_page(width=clip.width, height=clip.height)
            p.show_pdf_page(p.rect, doc, page.number, clip=clip)
    new.save(out)
```
