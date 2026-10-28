# Danfoss AK-CC 550A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.

---

## AK-CC 550 – Brugervejledning (dansk)

*Kilde: Danfoss-dokument BC187486426386da-000701. Regulator til kølemøbelstyring. Virkemåde, menuoversigt, parametre, alarm- og fejlkoder.*

**User Guide**

**Regulator til kølemøbelstyring** AK-CC 550

ADAP-KOOL® Refrigeration control systems

### **Indhold**

|---|

|---|

### **Introduktion**

##### **Anvendelse**

Komplet kølemøbelstyring med stor fleksibilitet for tilpasning til alle typer kølemøbler og kølerum.

##### **Fordele**

- Energioptimering af hele kølemøblet

- Én regulator til flere forskellige kølemøbler

- Integreret display i front af regulator

- Hurtig opsætning via prædefinerede opsætninger

- Indbygget datakommunikation

- Indbygget urfunktion med gangreserve

##### **Princip**

Temperaturen i møblet registreres af én eller to temperaturfølere som hhv. placeres i luftstrømmen før fordamperen S3 og efter fordamperen S4. En indstilling for såvel termostat, alarmtermostat og displayudlæsning bestemmer hvor stor indflydelse de to følerværdier skal have for hver enkelt funktion.

*[Figurtekst: dier skal have for hver enkelt funktion. · Derudover kan der anvendes en produktføler S6, som kan placeres · valgfrit i møblet og som kan anvendes til at registrere temperatu- · ren ved den ønskede vare et sted i møblet. · Temperaturen på fordamperen registreres med S5 føleren, som · kan anvendes som afrimningsstopføler. · Foruden udgang til den elektroniske indsprøjtningsventil af typen · AKV, har regulatoren 5 relæudgange, som defineres via valg af · anvendelse – på side 12 er de enkelte anvendelsesmuligheder · beskrevet i detaljer. · Funktioner · • Dag/nat termostat iht. ON/OFF eller modulerende princip · • Produktføler S6 med separate alarmgrænser · • Skift imellem termostatindstillinger via digital indgang · • Adaptiv regulering af overhedning · • Adaptiv afrimning baseret på fordamperydelse · • Start af afrimning via skema, digital indgang eller netværk · • Naturlig, elektrisk eller varmgas afrimning · • Stop af afrimning på tid og/eller temperatur · • Koordinering af afrimning imellem flere regulatorer · • Pulsering af blæsere når termostaten er udkoblet · • Møbelrengøringsfunktion til dokumentation af HACCP proce- · dure · • Kantvarme styring via dag/nat belastning eller dugpunkt · • Dørfunktion · • Styring af to kompressorer · • Styring af natgardin · • Styring af lys · • Varmetermostat · • Fabrikskalibrering der garanterer en bedre målenøjagtighed end · angivet i standarden EN 441-13 uden efterfølgende kalibrering · (Pt1000 ohms føler) · • Integreret MODBUS kommunikation med mulighed for efter · montering af LonWorks eller DANBUSS kommunikationskort. · Møbeleksempler]*

2

##### **Anvendelser**

Her er en oversigt over regulatorens anvendelsesmuligheder. En indstilling vil konfigurere ind- og udgange, så regulatorens betjeningsflade bliver målrettet til den valgte anvendelse. På side 28 kan du se de aktuelle indstillinger for de respektive anvendelser.

##### Anvendelse 1-8

Disse anvendelser anvendes til standard møbel eller kølerum med én ventil, én fordamper og én kølesektion. Følerne bliver anvendt efter standardprincip. Funktionen af udgangene ændrer sig alt efter valgt anvendelse.

##### Anvendelse 9

Denne anvendelse er til kølemøbler med én ventil, to fordampere og to kølesektioner.

Her reguleres temperaturen og alarmovervågningen altid efter S4 føleren.

S3 føleren anvendes til displayudlæsning. Produktføleren er erstattet af en ekstra afrimningsføler S5B til den anden fordamper.

##### Anvendelse 10

Denne anvendelse er til kølemøbler med én ventil, én fordamper og to kølesektioner.

Her reguleres temperaturen altid efter S4 temperaturen. S6 føleren placeres på S3B positionen. S3B føleren anvender alarmgrænser m.m. der normalt anvendes for S6 føleren. De to S3 temperaturer anvendes til alarmovervågning og display udlæsning for hver kølesektion. Der er separate alarmgrænser for hver kølesektion.

3

### **Virkemåde**

##### **Væskeindsprøjtning**

Væskeindsprøjtningen i fordamperen styres af en elektronisk indsprøjtningsventil af typen AKV. Ventilen fungerer både som ekspansionsventil og magnetventil. Ventilen åbner og lukker efter signaler fra regulatoren.

Funktionen indeholder en adaptiv algoritme, der selvstændigt justerer ventilens åbningsgrad, så fordamperen hele tiden leverer den optimale køling.

Overhedningen kan måles via et af følgende to principper:

- Trykføler Po og temperaturføler S2

Ved denne anvendelse opnås en korrekt måling af overhedningen under alle forhold, hvilket sikrer en meget robust og præcis regulering.

Signalet fra én tryktransmitter kan anvendes af flere regulatorer, men kun hvis der ikke er nævneværdig trykforskel imellem de pågældende fordampere.

- To temperaturfølere S1 og S2

- Ved anvendelse af S1 føler er placeringen særdeles vigtig. Føleren skal placeres, hvor der altid vil være kølemiddel under indsprøjtning, uden der er for meget trykfald. Danfoss anbefaler at S1 føleren placeres på den første rørbøjning på fordamperen.

##### **Temperaturregulering**

Temperaturen i møblet registreres af én eller to temperaturfølere som hhv. placeres i luftstrømmen før fordamperen S3 og efter fordamperen S4. En indstilling for såvel termostat, alarm termostat og displayudlæsning bestemmer hvor stor indflydelse de to følerværdier skal have for hver enkelt funktion, fx vil 50 % give en lige stor værdi fra begge følere.

Selve temperaturreguleringen kan ske på to måder:

Som en almindelig on/off-regulering med en tilhørende differens, eller som en modulerende regulering hvor temperaturvariationen ikke bliver nær så stor som ved on/off-regulering. Der er dog en begrænsning i anvendelsen, da en modulerende regulering kun kan anvendes på centralanlæg.

På et decentralt anlæg skal termostatfunktionen vælges til on/off regulering.

På et centralt anlæg kan termostatfunktionen vælges til enten on/off regulering eller til modulerende regulering.

##### **Temperaturovervågning**

Ligesom for termostaten kan man for alarmovervågningen indstille en vægtning imellem S3 og S4 således at man kan bestemme hvor stor indflydelse de to følerværdier skal have i alarmovervågningen. Man kan indstille min. og maks. grænser for alarmtemperaturen samt tidsforsinkelser. Der kan indstilles en længere tidsforsinkelse på høj temperatur alarm. Denne tidsforsinkelse er gældende under afrimning, møbelrengøring og opstart.

Placering af S1 føleren er altafgørende for et sikkert signal og hermed for en tilfredsstillende regulering.

4

##### **Termostatbånd**

Termostatbånd kan med fordel benyttes til impulsmøbler, hvor der opbevares forskellige varetyper, der kræver forskellige temperatur forhold. Via et kontaktsignal på en digital indgang kan der skiftes imellem to forskellige termostatbånd.

For hvert termostatbånd kan der indstilles separate termostat- og alarmgrænser – også for produktføleren.

##### **Nathævning af termostatværdi**

På kølemøbler kan der være store belastningsforskelle imellem butikkens åbnings- og lukketid, især hvis der anvendes natlåg/gardiner.

Her kan termostatreferencen hæves uden, at det går ud over varernes temperatur.

Skift imellem dag- og natdrift kan ske på følgende måde:

- Via et eksternt kontaktsignal

- Via et signal over datakommunikationen.

##### **Produktføler**

Der kan anvendes en separat produktføler S6, som kan placeres valgfrit i møblet og som kan anvendes til registrering og overvågning af temperaturen på det varmeste sted i møblet. Der er tilknyttet separate alarmgrænser og tidsforsinkelser for produktføleren.

##### **Møbelrengøring**

Denne funktion gør det let for butikspersonale at udføre en møbelrengøring efter en standardprocedure. Møbelrengøringen aktiveres via et pulskontaktsignal  – som regel via en nøgleomskifter placeret på møblet. Møbelrengøringen gennemføres via 3 faser:

- 1 - Ved første aktivering stoppes kølingen, men ventilatorerne kører fortsat for at afrime fordamperne. På displayet vises ”Fan”.

- 2 - Ved den anden aktivering stoppes blæserne også, og møblet kan nu rengøres. På displayet vises ”OFF”.

- 3 - Ved den tredje aktivering genstartes kølingen. På displayet vises den aktuelle møbeltemperatur (o97 indstilling).

|-|+|+|°C|
|---|---|---|---|
|1|÷|+|Fan|
|2|÷|÷|Off|
|3|+|+|°C|

##### Dokumentation

Når møbelrengøringen aktiveres sendes en rengøringsalarm til den normale alarmmodtager. En senere behandling af disse alarmer vil dokumentere, at møblet er rengjort så ofte som planlagt.

##### Alarmovervågning

Der er ingen temperaturalarmer under møbelrengøring.

5

##### **Afrimning**

Alt efter anvendelsen kan der vælges imellem følgende afrimningsmetoder:

- Naturlig: Her holdes ventilatorerne igang under afrimningen

- El: Varmelegemet aktiveres

- Varmgas: Her styres magnetventilerne, så varmgassen kan strømme igennem fordamperen.

##### Afrimningssekvens

- 1) Pump down

- 2) Afrimning

- 3) Venteposition efter afrimning

- 4) Tømning (drain forsinkelse. Kun ved varmgas)

- 5) Afdrypning

- 6) Forsinkelse af ventilator

##### Varmgasafrimning (kun anvendelse 6)

Denne tilslutningsmåde kan anvendes på anlæg med varmgasafrimning, men kun til mindre anlæg i fx supermarkeder – funktionsindholdet er ikke tilpasset anlæg med store fyldninger. Relæ 2 anvendes til sugeventilen

Relæ 4's skiftefunktionen benyttes henholdsvis af bypass-ventilen og af varmgas-ventilen.

Må ikke anvendes sammen med ventilerne PMLX og GPLX medmindre der installeres et forsinkelsesrelæ som sikrer at PMLX / GPLX ventilen er helt lukket før der åbnes for varmgasventilen.

*[Figurtekst: Varmgasapplication]*

##### Drypbakke varmelegeme

I forbindelse med varmgasafrimning er det muligt at styre et varmelegeme i drypbakken. Når afrimningen indledes, aktiveres varmelegemet. Varmelegemet forbliver aktiveret indtil en indstillet tid efter at afrimningen er stoppet på tid eller temperatur.

##### Start af afrimning

En afrimning kan startes på forskellige måder:

Interval: Afrimningen starter med faste tidsintervaller fx hver

ottende time. En intervaltid skal ALTID indstilles til en "højere" værdi end den periodetid, der indstilles imellem to afrimninger, når der anvendes skema eller netværkssignal.

Køletid: Afrimningen starter med faste køletidsintervaller dvs. at et lavt kølebehov vil "udskyde" den kommende afrimning. Skema: Her kan afrimningen startes på faste tider i døgnet. Dog max. 6 stk.

Kontakt: Her startes afrimningen med et kontaktsignal på en digital indgang.

Netværk: Her modtages signalet om afrimningsstart fra en systemenhed via datakommunikationen.

Adaptiv afrimning: Her startes afrimning baseret på intelligent registrering af fordamperydelse.

Manuel: En extra afrimning kan aktiveres fra nederste knap på displayet eller via en parameterindstilling.

Alle de nævnte metoder kan anvendes i flæng — blot én går aktiv vil det starte afrimningen.

##### Stop af afrimning

En afrimning kan stoppes på enten:

- Tid

- Temperatur (med tid som sikkerhed).

6

##### Koordineret afrimning

Der er to måder, hvorpå der kan laves koordineret afrimning. Enten med ledningsforbindelser imellem regulatorerne, eller via datakommunikation.

##### Ledningsforbindelser

Den digitale indgang DI2 forbindes imellem de aktuelle regulatorer.

Når en regulator starter en afrimning vil alle de øvrige regulatorer følge efter, og ligeledes starte en afrimning. Efter afrimningen vil de enkelte regulatorer gå i en venteposition. Når alle er i venteposition, bliver køling igen tilladt.

##### Koordinering via datakommunikation

Her klarer systemenheden koordineringen. Regulatorerne samles i afrimningsgrupper, og systemenheden sørger for at starte afrimningen i gruppen ud fra et ugeskema. Når en regulator har afsluttet afrimningen, sender den besked til systemenheden og går derefter i en venteposition. Når alle i gruppen er i venteposition, bliver kølingen igen tilladt i de enkelte regulatorer.

*[Figurtekst: Max. 10 stk. · Systemmanager]*

##### Behovstyret afrimning

##### 1 Køletidsbestemt

- Når den opsummerede køletid har passeret en fastlagt tid bliver der startet en afrimning.

- 2 Adaptiv afrimning baseret på overvågning af fordamperydelse Denne funktion bygger på en registrering af luftflowet igennem fordamperen. Ved at benytte AKV ventilen som masseflowmåler for kølemiddelflowet er det muligt at sammenligne energioptagelsen på kølemiddelsiden med energiafgivelsen på luftsiden. Via denne sammenligning kan luftflowet igennem fordamperen bestemmes og dermed også størrelsen af is/rim opbygningen på fordamperoverfladen. Såfremt rim/is opbygningen reducerer fordamperens effektivitet, vil funktionen gennemføre en ekstra afrimning.

I det ugentlige afrimningsskema indlægges det antal afrimninger, som svarer til grundbelastningen. Såfremt belastningen på fordamperen øges udover dette, vil behovsafrimningen indlægge de nødvendige ekstra afrimninger. Funktionen kræver følgende tilslutninger:

- Ekspansionsventil type AKV

- Temperatursignal fra både S3 og S4

- Temperatursignal fra kondenseringstrykket Tc som skal distribueres via netværket fra en system manager. Hvis regulatoren ikke kan hente Tc signalet, bliver målingen erstattet af en konstant.

- NB. S3 og S4 følerne skal placeres i luftstrømmen/kanalen umiddelbart før/efter fordamperen.

##### **Smeltefunktion**

Denne funktion forhindrer, at luftgennemstrømningen i fordamperen nedsættes af rim, der bygges op ved længere tids uafbrudt drift.

Funktionen træder i kraft, hvis termostattemperaturen har ligget i området fra –5°C til 10°C i mere end det indstillede smelteinterval. Kølingen stoppes herefter i den indstillede smeltetid. Rimen smeltes, så luftgennemstrømningen og dermed fordamperens ydelse forbedres væsentligt.

##### Min. tid imellem afrimninger

Der er en 2  timers minimumstid imellem afrimninger.

Herved kan det undgås, at planlagte afrimninger i hht. ugeskemaet udføres lige efter, at en behovsstyret afrimning er blevet gennemført. Tiden gælder, fra en behovsstyret afrimning er afsluttet, til der igen tillades en planlagt afrimning. Behovsafrimningen vil heller ikke starte afrimninger med kortere interval end de 2 timer.

##### Reset

Hvis den adaptive afrimningsfunktion registrerer problemer med afrimningen, vil den vise en fejltilstand, og funktionen vil ikke længere gennemføre ekstra afrimninger. I dette tilfælde bør der gennemføres en manuel reset af funktionen via d22. Når reset funktionen aktiveres, vil det starte en afrimning, så den efterfølgende tuning vil ske på en fordamper uden rim/is opbygning.

##### NB

Funktionen "Adaptiv afrimning" bør først aktiveres, når fordamperen kører under normale driftsbetingelser.

##### **Realtidsur**

Regulatoren har indbygget et realtidsur, der kan benyttes til start af afrimninger. Dette ur har en gangreserve på 4 timer. Hvis regulatoren udstyres med datakommunikation, bliver uret automatisk opdateret fra systemenheden.

7

##### **Styring af to kompressorer**

De to kompressorer skal være af samme størrelse.

Når regulatoren kalder på køling, vil den først indkoble kompressoren med den mindste driftstid. Efter forsinkelsestiden vil den anden kompressor blive koblet ind.

Når temperaturen er nået ned til "midt i differencen", vil kompressoren med den længste drifttid blive koblet ud.

Den igangværende kompressor vil fortsætte indtil temperaturen er nået ned til udkoblingsværdien. Herefter kobler den ud.  Når temperaturen igen når op til midten af differencen, bliver der igen indkoblet en kompressor.

Hvis én kompressor ikke kan holde temperaturen indenfor differencen, bliver den anden kompressor også koblet ind. Hvis en af kompressorerne har kørt alene i to timer, vil der ske en omkobling imellem kompressorerne, så drifttiden kan udlignes.

De to kompessorerer skal være af en type, der kan starte op mod et højt tryk.

Kompressorernes indstillinger for "Min On tid" og "Min Off tid" vil altid have højeste prioritet under normal regulering. Men hvis en af overstyringsfunktionerne bliver aktiveret, ses der bort fra "Min On tiden"

##### **Kantvarme**

For at spare energi er det muligt at pulsstyre effekttilførslen til kantvarmen. Pulsstyringen kan enten styres ud fra dag/nat belastning eller via dugpunkt.

##### Pulsstyring i hht dag og nat

Der kan indstilles forskellige On-perioder for dagdrift og natdrift. Der indstilles en periodetid samt den procentdel af periodetiden, hvori kantvarmen er On.

##### Pulsstyring i hht. dugpunkt

For at kunne benytte denne funktion kræves det, at der anvendes en Systemmanager af typen AK-SM, der kan måle dugpunktet og distribuere det aktuelle dugpunkt til møbelregulatorerne. I dette tilfælde styres kantvarmens ON periode ud fra det aktuelle dugpunkt.

I møbelstyringen indstilles to dugpunktsværdier:

- En hvor effekten skal være max. dvs.100%. (o87)

- En hvor effekten skal være min. (o86).

Ved et dugpunkt der er lig med eller lavere end værdien i 086, vil effekten være den værdi, der angives i o88.

I området imellem de to dugpunktsværdier vil regulatoren regulere effekten, der skal tilføres kantvarmen.

##### Under afrimning

Under afrimning vil kantvarmen altid være 100% On.

*[Figurtekst: Kantvarme · Dugpunkt]*

8

##### **Ventilator**

##### Pulsstyring

For at opnå energibesparelse er det muligt at pulsstyre effekttilførslen til ventilatorerne ved fordamperne. Der kan pulsstyres på en af følgende måder:

- I termostatens udkoblingsperiode (kølerum)

- Under natdrift og i termostatens udkoblingsperiode (møbel med natlåg)

- (Funktionen er ikke aktuel, når r14=2, dvs. modulerende regulering.)

Der indstilles en periodetid samt den procentdel af periodetiden, hvori ventilatorerne skal være i drift.

##### Udkobling af ventilatorer ved anlægsfejl

Såfremt kølingen i en fejlsituation bortfalder kan temperaturen i kølerummet stige hurtigt som følge af effekttilførelsen fra store ventilatorer. For at forhindre denne situation kan regulatoren stoppe ventilatorerne, hvis temperaturen ved S5 overskrider en indstillet grænseværdi.

##### **Lysfunktion**

Funktionen kan anvendes til styring af lyset i et kølemøbel eller i et kølerum. Den kan også anvendes til styring af et motoriseret natgardin.

Lysfunktionen kan defineres på tre måder:

- Lyset styres via et signal fra en dørkontakt. Sammen med denne funktion kan der indstilles en forsinkelsestid, så lyset holdes tændt i en periode efter, at døren er lukket.

- Lyset styres via dag/nat funktionen

- Lyset styres via datakommunikationen fra en systemenhed. Her er der to muligheder for drift, hvis datakommunikationen skulle svigte:

- Lyset kan gå On

- Lyset kan forblive i den aktuelle tilstand.

Lysbelastningen skal forbindes til NC-kontakten på relæet. Herved sikres det, at lyset forbliver tændt i møblet, hvis spændingen til regulatoren skulle svigte.

Lyset kan slukkes når "r12" (Main switch) indstilles til off (se o98). Lyset slukkes, når møbelrengøringsfunktionen aktiveres.

##### **Natgardin**

Motoriserede natgardiner kan styres automatisk fra regulatoren. Natgardinerne vil følge status på lys funktionen. Når lyset tændes åbner natgardinerne og når lyset slukkes lukker natgardinerne igen. Når natgardinerne er lukkede er det muligt at åbne dem via et kontakt signal på en digitale indgang. Hvis dette pulstryk aktiveres, åbner natgardinerne og man kan fylde nye vare i kølemøblet. Såfremt man igen aktivere pulstryk signalet lukker gardinerne igen.

Når natgardinfunktionen anvendes, kan termostatfunktionen regulere med forskellige vægtninger  imellem S3 og S4 føleren. En vægtning under dagdrift og en anden, når gardinet er for. Et natgardin er åbent, når møbelrengøringsfunktionen aktiveres. En indstilling kan definere, at natgardinet er åbent, når "r12" (main switch) indstilles til off. (se o98).

9

##### **Digitale indgange**

Der er to digitale indgange DI1 og DI2 med kontaktfunktion og én digital indgang DI3 med højspændingssignal. De digitale indgange kan anvendes til følgende funktioner:

- Videresende en kontakts position over datakommunikation

- Dørkontaktfunktion med alarm

- Starte en afrimning

- Hovedafbryder - start/stop af køling

- Nathævning

- Thermostatbåndsskift

- Generel alarm overvågning

- Møbelrengøring

- Tvangskøling

- Overstyring af natgardin

- Koordineret afrimning (kun DI2)

- Tvangslukning af ventil (kun DI 3)

##### **Tvangslukning**

AKV-ventilerne kan lukkes med et eksternt signal ( "Forced closing").

Funktionen skal anvendes i forbindelse med kompressorens sikkerhedskreds, så der ikke sprøjtes væske ind i fordamperen, når kompressoren er stoppet på sikkerhedsautomatikken (dog ikke på lavtryk - LP).

Er der en afrimning i gang, vil tvangslukningstilstanden først indtræde, når afrimningen er afsluttet. Signalet kan modtages på DI3-indgangen eller det kan modtages via datakommunikationen. Under en tvangslukning kan ventilatorerne defineres til at være stoppet eller være i drift.

##### **Dørkontakt**

Dørkontaktfunktionen kan via de digitale indgange defineres til to forskellige anvendelser:

- Alarmovervågning Regulatoren overvåger dørkontakten og afgiver en alarmmeddelelse, hvis døren har været åben i længere tid end den indstillede alarmforsinkelse.

• Alarmovervågning og stop af køling Når døren åbnes, stoppes kølingen, dvs. indsprøjtningen, kompressoren og ventilatoren stoppes og lyset tændes. Hvis døren forbliver åben i længere tid end den indstillede genstartstid, genoptages kølingen. Dette vil sikre, at køling opretholdes, selvom døren bliver efterladt åben eller dørkontakten skulle være defekt.

Hvis døren forbliver åben i længere tid end den indstillede alarmforsinkelse, afgives tillige en alarm.

##### **Varmefunktion**

Varmefunktionen anvendes for at hindre at temperaturen bliver for lav f.eks. i opskæringsrum eller lignende. Grænsen for hvornår varmefunktionen bliver udkoblet indstilles som en offset værdi under den aktuelle udkoblingsgrænse for køletermostaten. Derved sikres det at der ikke køles og varmes samtidigt. Differensen for varmetermostaten har samme værdi som for køletermostaten. For at hindre at varmetermostaten indkobles ved kortvarige undersving i lufttemperaturen kan der indstilles en tidsforsinkelse for hvornår der skiftes fra køling til opvarmning.

*[Figurtekst: Køling · Neutralzone · Varme]*

10

##### **Datakommunikation**

Regulatoren har fast indbygget MODBUS datakommunikation.

Hvis der er ønske om anden form for datakommunikation kan der indsættes ét Lon RS 485 eller DANBUSS modul i regulatoren. Tilslutningen skal så ske på klemme RS 485.

(Ved anvendelsen af et Lon RS 485 modul og gateway type AKA 245, skal modulet være version 6.20 eller nyere.)

##### **Display**

Regulatoren har ét stik til et display. Her kan der tilsluttes et display type EKA 163B eller EKA 164B (max. længde 15m). EKA 163B er et display til udlæsning. EKA 164B er både til udlæsning og til betjening. Forbindelsen imellen display og regulator kan ske med et kabel, der har stik i begge ender.

Hvis afstanden imellem display og regulator er større end 15 m, skal tilslutningen foretages anderledes.

Og der skal også monteres et ekstra modul i regulatoren, hvis der anvendes datakommunikation.

Den indbyggede MODBUS datakommunikation anvendes så til displayforbindelsen, og datakommunikationen til de øvrige regulatorer skal så ske via et modul. Modulet kan være: Lon RS 485, DANBUSS eller  MODBUS.

Når der skal tilsluttes et display på den indbyggede MODBUS, kan displayet med fordel ændres til et af samme type men med indeks A (version med skrueklemmer).

Regulatorens adresse skal indstilles højere end 0 for at displayet kan kommunikere med regulatoren. Hvis der ønskes tilslutning af to displays, skal det ene tilsluttes stikket (max. 15 m.), og det andet skal så tilsluttes den fastmonterede datakommunikation.

##### **Vigtigt**

Alle tilslutninger til datakommunikationen MODBUS, DANBUSS  og RS 485, skal overholde de krav, der stilles til datakommunikationskabler. Se litteratur: RC8AC

*[Figurtekst: Adressen o03 > 0]*

##### **Overstyring**

Regulatoren indeholder en række funktioner, som kan benyttes sammen med overstyringsfunktionen i mastergatewayen / System

Mana g er.

|**Funktion via datakommunikation**|**Funktion i gateway/system manager**|**Benyttet parameter i AK-CC 550**|
|---|---|---|
|Start af afrimning|Afrimningskontrol / Tidsskema / Afrimningsgruppe|--- Def start|
|Koordineret afrimning|Afrimningskontrol / Afrimningsgruppe|--- HoldAfterDef / - - - DefrostState|
|Forhindre afrimningsstart||--- Disable Def|
|Dag/Nat skema|Dag/Nat styring / Tidsskema / Lyszone|--- Night setback|
|Lysstyring|Dag/Nat styring / Tidsskema|O39 light Remote|
|Tvangslukning|Forced Close / Injection ON / AKC ON|--- Forced cl.|
|Tvangskøling||--- Forced cool|
|Kantvarme i henhold til dugpunkt|/ Enhanced railheat|--- Dew point|
|P0 optimering|P0 Optimering|Regulatoren understøtter P0 optimering|
|Adaptiv afrimning|/ Adaptive defrost.  kun system manager|- - - Tc TempMean|

11

### **Anvendelser**

Her er en oversigt over regulatorens anvendelsesmuligheder.

En indstilling vil konfigurere relæudgangene, så regulatorens betjeningsflade bliver målrettet til den valgte anvendelse.

På side 28 kan du se de aktuelle indstillinger for de respektive el-diagrammer.

S3 og S4 er temperaturfølere. Anvendelsen bestemmer om enten den ene eller den anden eller begge følere skal anvendes. S3 placeres i luftstrømmen før fordamperen. S4 efter fordamperen.

En %- indstilling bestemmer, hvad der er reguleres efter.

S5 er afrimningsføler og placeres på fordamperen.

S6 er produktføler, men i application 9 og 10 har den anden anvendelse. DI1, DI2 og DI3 er on/off-indgange, der fx kan benyttes til en af følgende funktioner: Dørfunktion, alarmfunktion, afrimningsstart, ekstern hovedafbryder, natdrift, skift af termostatreference, møbelrengøring, tvangskøling eller koordineret afrimning. DI3 er en 230 V indgang. Se funktionerne i indstillingerne o02, o37 og o84.

*[Figurtekst: 1 · Generelt : · De ti anvendelser er alle tilpasset kommercielle · køleanlæg i form af enten kølemøbler eller kølerum. · Gennemgående har alle anvendelser udgange til: · • AKV ventil · • Fan · • Afrimning · Derudover har de forskellige anvendelser · forskellige funktioner og dermed ind- og udgange. · Anvendelse 1-4 · Standard anvendelser. 2 · Dette er til standard anvendelser, hvor den · afgørende forskel kun er forskellige kombinationer · af følgende funktioner/udgange: · • Alarm · • Kantvarme · • Kompressor · • Lys · 3 · 4]*

12

**5**

De efterfølgende anvendelser har alle nogle specielle funktioner, som kort er:

##### **Anvendelse 5**

”To-kompressor” drift.

De to kompressorer skal være af samme størrelse. Ved opstart (efter afrimning, driftstop etc.) indkobles begge kompressorer med en indstillet tidsforskydning. Den ene kompressor kobler med den halve differens, således at der sker en optimal tilpasning af kompressorkapaciteten til den aktuelle belastning i møblet/rummet. Der er automatisk drifttime udligning imellem kompressorerne.

**6**

For en mere detaljeret beskrivelse se tidligere i manualen

##### **Anvendelse 6**

Varmgas afrimning.

Varmgas afrimningen er tilpasset kommercielle møbler/rum med begrænset anlægsfyldning. Det ene relæ styrer hovedventilen i sugeledningen.

#### **7**

Et skifterelæ styrer såvel varmgasventil og drænventil.

Det vil sige, at der ikke er en tidsforsinkelse imellem stop af varmgas og påbegyndelse af tømning.

##### **Anvendelse 7**

##### Styring af natgardiner

Natgardinerne vil følge status på lysfunktionen – når lyset er tændt, er natgardiner oppe, og når lys er slukket, er natgardiner nede. Derudover giver en digital indgang mulighed for tvangsåbning af gardiner, så varer kan fyldes i møblet.

**8**

##### **Anvendelse 8**

##### Varmetermostat

Varmetermostat anvendes typisk, hvis temperaturen skal reguleres indenfor mere snævre grænser f.eks. til opskæringsrum etc. Varmetermostaten kan indstilles som en differens i forhold til udkoblingsgrænsen for køletermostaten, så samtidig køle og varme undgås.

#### **9**

##### **Anvendelse 9**

To kølesektioner - to afrimningsudgange Denne anvendelse er til kølemøbler med én ventil, to fordampere og to kølesektioner. Temperaturen reguleres og alarmovervåges altid efter S4 temperaturen. Produktføleren er i denne anvendelse benyttet som afrimningsstopføler til fordamper nummer to.

##### **Anvendelse 10**

To kølesektioner – individuel alarm/display via S3 Denne anvendelse er til kølemøbler med én ventil, én fordamper og to kølesektioner. Temperaturen reguleres altid efter S4 temperaturen. Produktføleren er benyttet som ekstra S3 føler til sektion nummer to. Alarmovervågning og displayudlæsning foregår så individuelt via "S3" følere i hver kølesektion.

**10**

13

##### **Tilslutningsskilte**

Fra fabrikken er regulatoren leveret med skilte, der angiver anvendelse 1.

Hvis du benytter en anden anvendelse, er der medleveret skilte, så du kan montere det aktuelle. Det er kun det nederste skilt, der skal monteres.

Til venstre på skiltene, er nummeret angivet. Benyt skiltet med det aktuelle nummer. Et af skiltene er gældende for både anvendelse 4 og 10.

14

### **Funktionsoversigt**

|**Funktion**|**Para-**<br>**meter**|**Parameter ved betjening via**<br>**datakommunikation**|
|---|---|---|
|**Normalbilledet**|||
|Normalt vises temperaturværdien fra en af de to termostatfølere S3 eller S4 eller et<br>mix af de to målinger.<br>I o17 bestemmes forholdet.||Display air (u56)|
|**Termostat**||**Thermostat control**|
|**Setpunkt**<br>Der reguleres efter den her indstillede værdi + en evt. forskydning. Værdien indstilles<br>via tryk på den midterste knap.<br>Den indstillede værdi kan fastlåses eller begrænses til et område med indstillingerne<br>i 02  03||Cutout °C|
|r og r.<br>Den øjeblikkelige reference kan ses i"u91 Cutout temp".|||
|<br>**Differens**<br>Når temperaturen er højere end referencen + den indstillede differens, vil kompres-<br>sorrelæet være trukket. Det vil bryde igen, når temperaturen når ned på den indstil-<br>lede reference.|r01|Differential|
|Ref.<br>Dif.|||
|**Setpunktsbegrænsning**<br>Regulatorens indstillingsområde for setpunktet kan indsnævres, så der ikke ved et<br>uheld bliver indstillet en alt for stor eller en alt for lille værdi - med skader til følge.|||
|For at undgå en for høj indstilling af setpunktet, angives et max. tilladeligt setpunkt.|r02|Max cutout °C|
|For at undgå en for lav indstilling af setpunkt, angives et min. tilladeligt setpunkt.|r03|Min cutout °C|
|**Korrektion af displayets temperaturvisning**<br>Hvis temperaturen ved varerne og temperaturen, der modtages af regulatoren, ikke<br>er ens, kan der ske en offset justering af den viste displaytemperatur.|r04|Disp. Adj. K|
|f <br>**Temperaturenhed**<br>Her kan du vælge, om regulatoren skal vise temperaturværdierne i °C eller i °F.|r05|Temp. unit<br>°C=0. / °F=1<br>I Systemsoftware AKM vil der kun blive<br>vist °C - uanset indstillingen.|
|**Korrektion af signalet fra S4**<br>Kompensationsmulighed ved en lang følerledning.|r09|Adjust S4|
|**Korrektion af signalet fra S3**<br>Kompensationsmulighed ved en lang følerledning.|r10|Adjust S3|
|**Start / stop af kølingen**<br>Med denne indstilling kan kølingen startes, stoppes eller der kan tillades en manuel<br>overstyring af udgangene. (Ved manuel styring indstilles værdien til -1. Herefter kan<br>AKV-udgang og relæudgange tvangsstyres via den respektive udlæsningsparameter<br>(u23, u58 osv.). Her skal den udlæste værdi overskrives.)<br>Start / stop af kølingen kan eventuelt også foretages med en ekstern kontaktfunktion,<br>der tilsluttes en DI indgang.<br> " "|r12|Main Switch<br>1: Start<br>0: Stop<br>-1: Manuel styring af udgange tillades|
|Stoppet køling vil give enStandby alarm.|||
|**Nathævningsværdi**<br>Termostatens reference bliver setpunktet + denne værdi, når regulatoren skifter over|r13|Night offset|
|<br>til natdrift. (Vælg en negativ værdi, hvis der skal ske kuldeakkumulering.)|||
|**Termostatfunktionen**<br>Her defineres hvordan termostaten skal fungere. Enten som en almindelig ON/OFF<br>termostat eller som en modulerende termostat.<br>**1=**ON/OFF termostat<br>**2=**Modulerende|r14|Therm. mode|
|Ved "modulerende" vil AKV ventilen begrænse gennemstrømningen af kølemiddel, så<br>temperaturvariation bliver mindre end ved ON/OFF termostaten.<br>Ved "modulerende" må differensen (r01) ikke stilles lavere end 2 K.|||
|På et decentralt anlæg**skal**indstillingen vælges til ON/OFF termostat.|||
|<br>**Valg af termostatføler S4%**<br>Her skal du definere den føler, som termostaten skal anvende i reguleringen.<br>S3, S4  eller en kombination af dem begge.<br>Med indstillingen 0% anvendes kun S3. Med 100% anvendes kun S4.|r15|Ther. S4 %|

15

|**Smeltefunktion**<br>Kun ved regulering på køl (-5 - +10°C).<br>Funktionen sikrer at fordamperen ikke lukkes af rim.<br>Her indstilles hvor tit funktionen skal stoppe kølingen og derved omdanne rimen til<br>vand (eller is hvis der er meget rim).|r16|MeltInterval|
|---|---|---|
|**Smeltetid**<br>Her indstilles i hvor langtid, en igangsat smeltefunktion skal vare.|r17|Melt period|
|**Setpunkt 2**<br>Termostatens udkoblingsværdi når termostatbånd 2 er aktiveret via en digital ind-<br>gang.|r21|Cutout2 temp|
|**Korrektion af signalet fra S6**<br>Kompensationsmulighed ved en langfølerledning.|r59|Adjust S6|
|**Valg af termostatføler S4% under natdrift med natgardin**<br>Her skal du definere den føler, som termostaten skal anvende i reguleringen.<br>S3, S4  eller en kombination af dem begge.|r61|Ther.S4% Ngt|
|<br>Med indstillingen 0% anvendes kun S3. Med 100% anvendes kun S4.<br>|||
|**Varmefunktion**<br>Her indstilles størrelsenpå neutralzonen ved overgangfra kølingtil varme|r62|Heat NZ|
|Tidsforsinkelse ved overgangen fra kølefase til varmefase.<br>(der er ingen tidsforsinkelse ved overgangen fra varmefasen til kølefasen).|r63|HeatStartDel|
|||Night setbck<br>(start af natsignal.  0=Dag,1=Nat)<br>Forced cool.<br>(start af tvangskøling)<br>|
|||Forced close<br>(tvangsstopaf køling)|
|**Alarm**||**Alarm settings**|
|Regulatoren kan give alarm i forskellige situationer.<br>Ved alarm blinker alle lysdioderne på fronten af regulatoren, og alarmrelæet bliver<br>aktiveret.||Ved datakommunikation kan vigtig-<br>heden for de enkelte alarmer define-<br>res. Indstillingen foretages i menuen<br>"Alarm destinationer".|
|**Alarmforsinkelse**(kort alarmforsinkelse på lufttemperatur)<br>Hvis den øvre eller nedre alarmgrænse overskrides, starter en timerfunktion. Alarmen<br>bliver først aktiv, når den indstillede forsinkelsestid er passeret.<br>Forsinkelsestiden indstilles i minutter.|A03|Alarm delay|
|**Alarmforsinkelse for døralarm**<br>Fikltid idtill i itt|A04|DoorOpen del|
|orsnesesen nses  mnuer.<br>Funktionen defineres i o02, o37 eller i o84.|||
|**Forsinkelsestid ved nedkøling**(lang alarmforsinkelse)<br>Denne forsinkelsestid bliver anvendt under opstart, under afrimning, og efter møbel-<br>|A12|Pulldown del|
|rengøring.<br>Der skiftes over til den normale forsinkelsestid (A03), når temperaturen er nået ned<br>under den indstillede øvre alarmgrænse.<br>Forsinkelsestiden indstilles i minutter.|||
|**Øvre alarmgrænse**<br>Her skal du indstille, hvornår alarmen ved højtemperatur skal træde i kraft. Grænse-<br>værdien indstilles i °C (absolut værdi).<br>Grænseværdien bliver hævet under natdrift. Værdien er den samme, som er indstillet|A13|HighLim Air|
|som nathævningsværdi, men den hæves kun, hvis værdien er positiv.<br>|||
|**Nedre alarmgrænse**<br>Her skal du indstille, hvornår alarmen ved lavtemperatur skal træde i kraft. Grænse-<br>værdien indstilles i°C (absolut værdi).|A14|LowLim Air|
|<br>**Øvre alarmgrænse for termostat 2 (termostatbånd 2)**<br>(Samme funktion som for termostat 1)|A20|HighLim2 Air|
|**Nedre alarmgrænse for termostat 2 (termostatbånd 2)**<br>(Samme funktion som for termostat 1)|A21|LowLim2 Air|
|**Øvre alarmgrænse for S6-temperaturen ved termostat 1**|A22|HighLim1 S6|
|**Nedre alarmgrænse for S6-temperaturen ved termostat 1**|A23|LowLim1 S6|
|**Øvre alarmgrænse for S6-temperaturen ved termostat 2 (termostatbånd 2)**|A24|HighLim2 S6|
|**Nedre alarmgrænse for S6-temperaturen ved termostat 2 (termostatbånd 2)**|A25|LowLim2 S6|
|**Forsinkelse på S6-temperaturalarm**|A26|Al. Delay S6|
|<br>Alarmen træder i kraft hvis en af de respektive grænseværdier i A22, A23, A24 eller<br>A25 overskrides.<br>|||
|Forsinkelsestiden indstilles i minutter.|||
|(Alarmer vil ikke optræde, når indstillingen vælges til max-værdi.)<br>|||
|**Forsinkelse på en DI1 alarm**<br>|A27|AI.Delay DI1|
|En brudt/sluttet indgang vil give alarm, når forsinkelsestiden er passeret. Funktionen<br>defineres i o02.|||
|i<br>**Forsinkelse på en DI2 alarm**<br>|A28|AI.Delay DI2|
|En brudt/sluttet indgang vil give alarm, når forsinkelsestiden er passeret. Funktionen<br>defineres i o37.|||

*[Figurtekst: Signal til alarmtermostaten A36 Alarm S4% · Her skal du definere det forhold imellem følerne, som alarmtermostaten skal anvende. · S3, S4  eller en kombination af dem begge. · Med indstillingen 0% anvendes kun S3. Med 100% anvendes kun S4. · Forsinkelsestid på S6 (produktføler) ved nedkøling  (lang alarmforsinkelse) A52 PullD del.S6 · Denne forsinkelsestid bliver anvendt under opstart, under afrimning, lige efter en · afrimning og efter en møbelrengøring. · Der skiftes over til den normale forsinkelsestid (A26), når temperaturen er nået ned · under den indstillede øvre alarmgrænse. · Forsinkelsestiden indstilles i minutter. · Reset alarm · Ctrl. Error (EKC error) · Kompressor Compressor control · Kompressorrelæet arbejder sammen med termostaten. Når termostaten kalder på · kulde vil kompressorrelæet være trukket. · Gangtider · For at forhindre pjatkørsel, kan der indstilles værdier for, i hvor lang tid kompresso- · ren skal køre, når den først er i gang. Og hvor lang tid den mindst skal være stoppet. · Gan g tiderne overholdes ikke ved afrimnin g sstarter. · Min. ON-tid  ( i minutter ) c01 Min. On time · Min. OFF-tid  (  i minutter ) c02 Min. Off time · Forsinkelsestid ved kobling af to kompressorer c05 Step delay · Indstillingen angiver den tid, der skal gå fra det første relæ trækker til det næste relæ · må trække. · Lysdioden på regulatorens front vil vise om kølingen er igang. Comp Relay · Her kan du aflæse kompressorrelæets · status. · Afrimning Defrost control · Regulatoren indeholder en timerfunktion, som nulstilles efter  hver  afrimningsstart. · Timerfunktionen vil starte en afrimning, når/hvis intervaltiden passeres. · Timerfunktionen starter, når der tilsluttes spænding til regulatoren, men den forsky- · des første gang med indstillingen i d05. · Hvis der sker en strømafbrydelse, vil timerværdien blive gemt, og fortsætte herfra, når · strømmen igen kommer tilbage. · Denne timerfunktion kan benyttes som en simpel måde at starte afrimninger på, men · den vil altid virke som en sikkerhedsafrimning, hvis en af de følgende afrimningsstar- · ter ikke modtages. · Regulatoren indeholder også et realtidsur. Ved indstilling af dette ur og tidspunkter · for afrimningstidspunkter, kan afrimningen startes på bestemte tider af dagen. · Afrimningsstart kan også foretages via datakommunikation, via kontaktsignal, ma- · nuel start eller behovsafrimningsmetoder. · Alle startmetoder vil fungere i regulatoren. De forskellige funktioner skal indstilles, så · afrimningerne ikke "falder over hinanden". · Afrimningen kan foretages med el eller varmgas. · Selve afrimningen stoppes på tid eller på temperatur med et signal fra en tempera- · turføler. · Afrimningsmetode d01 Def. method · Her skal du indstille om afrimningen skal foretages med el, varmgas eller "ingen".  0 = Off · Under en afrimning vil afrimningsrelæet være trukket. 1 = El · 2 = Gas · Afrimnings-stoptemperatur d02 Def. Stop Temp · Afrimningen stoppes ved en given temperatur, der måles med en føler (føleren defi- · neres i d10). · Tem p eraturværdien indstilles. · Intervaltid mellem afrimningsstarter d03 Def Interval · Funktionen nulstiller og starter timerfunktionen ved  hver  afrimningsstart. Når tiden  (0=off) · er udløbet vil funktionen starte en afrimning. · Funktionen benyttes som en simpel afrimningsstart eller den benyttes som en sik- · kerhed, hvis det normale signal udebliver. · Hvis der anvendes master/slaveafrimning uden urfunktion eller uden datakommuni- · kation, vil det være denne intervaltid, der starter afrimningerne. · Udebliver en afrimningsstart via datakommunikation, vil intervaltiden blive anvendt · som max. tid imellem afrimningerne. · Ved afrimning med urfunktion eller med datakommunikation skal intervaltiden · indstilles til en lidt længere tid end den planlagte, ellers vil intervaltiden starte en · afrimning, og lidt senere kommer så den planlagte. · Ved strømudfald vil intervaltiden blive fastholdt, og når strømmen vender tilbage, vil · intervaltiden fortsætte fra den fastholdte værdi. · Intervaltiden er ikke aktiv ,  når indstillin g en sættes til 0.]*

17

|**Max. afrimningsvarighed**<br>Denne indstilling er en sikkerhedstid, så afrimningen vil blive stoppet, hvis der ikke er<br>sket et stop på temperatur.<br>(Indstillingen er afrimningstiden,hvis d10 vælges til 0.)|d04|Max Def. time|
|---|---|---|
|**Tidsforskydning på afrimningsindkoblinger ved opstart**<br>Funktionen er kun aktuel, hvis du har flere kølemøbler eller grupper, hvor du ønsker,<br>at afrimningen skal forskydes i forhold til hinanden. Funktionen er kun aktuel, hvis du<br>har valgt afrimning med intervalstart (d03).<br>Funktionen forsinker intervaltiden d03 med det indstillede antal minutter, men den<br>gør det kun én gang, og det sker ved den allerførste afrimning, der kommer, når der<br>sættes spænding til regulatoren.<br>Funktionen er aktiv efter hvert strømudfald.|d05|Time Stagg.|
|**Afdrypningstid**<br>Her skal du indstille den tid, der skal gå fra en afrimning er afsluttet, til kompressoren<br>igen må starte. (Tiden, hvor vandet drypper af fordamperen.)|d06|DripOff time|
|**Forsinkelse på ventilatorstart efter afrimning**<br>Her skal du indstille den tid, der skal gå fra kompressoren startes efter en afrimning,<br>til ventilatoren igen må starte. (Tiden, hvor vandet skal “bindes” til fordamperen.)|d07|FanStartDel|
|**Ventilator-starttemperatur**<br>Ventilatoren kan også startes lidt tidligere end nævnt under “Forsinkelse på ventila-<br>torstart efter afrimning”, hvis S5-afrimningsføleren registrerer en lavere værdi end den<br>her indstillede.|d08|FanStartTemp|
|**Ventilator indkoblet under afrimning**<br>Her skal du indstille, om ventilatoren skal køre under en afrimning.<br>0: Stoppet (kører under pump down)<br>1: kører (stoppet under "ventilatorforsinkelse")|d09|FanDuringDef|
|<br>2: kører under pump down og afrimning. Derefter stoppet.|||
|**Afrimningsføler**<br>Her skal du definere afrimningsføleren.<br>0: Ingen, der afrimes på tid<br>1: S5<br>|d10|DefStopSens.|
|2: S4<br>3: Sx.  I anvendelse 1 til 8 og 10 stoppes afrimningen, når både S5 og S6 har nået den<br>indstillede temperatur (begge følere skal placeres på fordamperen). I anven-<br>delse 9 stoppes afrimningerne individuelt på de to sektioner af S5 / S5B|||
|**Pump down forsinkelse**<br>Indstil tiden hvor fordamperen tømmes for kølemiddel  før afrimningen|d16|Pump dwn del.|
|**Drain forsinkelse**(kun i forbindelse med varmgas)<br>Indstil tiden hvor fordamperen tømmes for kondenseret kølemiddel efter afrimnin-<br>gen|d17|Drain del|
|**Behovstyret afrimning - opsummeret køletid**<br>Her indstilles den køletid, der kan tillades uden afrimninger. Passeres tiden, bliver der<br>startet en afrimning.<br>Med indstilling=0 er funktionen afbrudt.|d18|MaxTherRunT|
|<br>**Forsinkelse på stop af varmen i afdrypningsbakken**<br>Tiden gælder fra afrimningen stopper på tid eller temperatur, til varmelegemet i<br>afdrypningsbakken skal afbrydes.|d20|Drip Tray del|
|**Adaptiv afrimning**<br>En adaptiv afrimning er en ekstra afrimning ud over de planlagte afrimninger. Her<br>indstilles hvornår den adaptive afrimning må starte en afrimning, hvis behovet<br>optræder:<br>0: Aldrig<br>1 K l d tilii|d21|AD mode|
|: un aarm ve -snng<br>2: Den må kun starte under dagdrift|||
|3: Den må starte både under dagdrift og under natdrift<br>4: Den må kun starte under natdrift|||
|<br>**Genstart af den adaptive afrimning**<br>Funktionen starter en afrimning, og når den er afsluttet, genstarter tuningsfunktio-<br>å fd dt k it|d22|AD reset|
|nen, s oramperens aa an regsreres.<br>SKAL FØRST AKTIVERES UNDER NORMALDRIFT.|||
|Hvis du vil se temperaturen ved afrimningsføleren, skal du trykke på regulatorens<br>nederste knap. (Kan være ændret til anden funktion i o92.)||Defrost temp.|
|Hvis du vil starte en ekstra afrimning, skal du trykke på regulatorens nederste knap i 4<br>sekunder.<br>En igangværende afrimning kan du stoppe på lignende måde.||Def Start<br>Her kan du starte en manuel afrim-<br>ning.<br>Hold After Def<br>Viser ON, hvis regulatoren er igang<br>med en koordineret afrimning.|
|||Disable def.<br>En igangværende afrimning kan stop-<br>pes|

18

|||Defrost State<br>Status på afrimningen|
|---|---|---|
|||<br>1=pumpdown / afrimer|
|**Parametre for kølefunktionen**|||
|**Integrationstid**<br>Ektidtilli f idtifkti|n05|Tn sec|
|spernsng or nsprøjnngsunonen.<br>Værdien bør**kun**ændres af særligt instrueretpersonale.|||
|**Max. værdi for overhedningsreferencen**|n09|Max SH|
|**Min. værdi for overhedningsreferencen**|n10|Min SH|
|**MOP-temperatur**<br>Hvis der ikke ønskes MOP-funktion, skal indstillingen vælges til OFF.|n11|MOP temp<br>(En værdi på 15 vil svare til OFF)|
|**Temperaturglid (kun ved anvendelse af S1-temperaturføler)**|n12|Glide|
|<br>Er der anvendt et zeotropkølemiddel, skal der indstilles en værdi for temperaturglid.|||
|**AKV-ventilens periodetid i sekunder**|n13|AKV Period|
|<br>(Bør kun indstilles til en lavere værdi, hvis det er et decentralt anlæg, og sugetrykket<br>varierer meget ogi takt med åbningen af AKV-ventilen.|||
|**Opstartstid for signalsikkerhed**<br>Hvis regulatoren ikke opnår et sikkert S1 signal indenfor denne periode, prøver<br>regulatoren på anden måde at skabe et stabilt signal. (En for høj værdi kan resultere<br>i en oversvømmet fordamper)|n15|StartUp time|
|.<br>Værdien bør**kun**ændres af særligt instrueret personale.<br>|||
|**Gennemsnitlig åbningsgrad**<br>Regulatoren registrerer løbende ventilens åbningsgrad og anvender værdien i<br>reguleringen.<br>|n16|AKV Dim.|
|Værdien bør**kun**ændres af særligt instrueret personale.|||
|<br>**Signalsikkerhed ved opstart**<br>|n17|Start OD %|
|Reguleringen anvender værdien som startværdi for ventilens åbningsgrad ved hver<br>termostatindkobling. Ved adaptiv regulering beregner regulatoren løbende en ny<br>værdi|||
|.<br>Værdien bør**kun**ændres af særligt instrueret personale.|||
|**Stabilitetsfaktor for regulering af overhedningen  (**Stability)|n18|-|
|<br>Med en højere værdi vil reguleringen tillade et større udsving af overhedningen,<br>|||
|inden referencen bliver ændret.<br>Værdien bør**kun**ændres af særligt instrueret personale. (Fabriksindstilling=4.0)|||
|<br>**Forstærkningsfaktor**<br>|n23|MTR Kp factor|
|Ekspertindstilling for indsprøjtningsfunktionen.<br>Værdien bør**kun**ændres af særligt instrueretpersonale.|||
|**Integrationstid**<br>Ekspertindstilling for indsprøjtningsfunktionen.|n24|MTR Tn sec|
|<br>Værdien bør**kun**ændres af særligt instrueretpersonale.|||
|**Valg af føler til overhedningsfunktionen**(kan kun indstilles når "r12" = 0)<br>k|n57|Pe/S1 select|
|1: Trytransmitter type AKS 32R<br>2: Temperaturføler S1 (Pt1000 Ohm ved 0°C)|||
|<br>**Ventilator**||**Fan control**|
|**Ventilatorstop temperatur**<br>Fki  il i  flii å d ikk ilf ffk il kl|F04|FanStopTemp.|
|untonen stopper ventatorerne  en ejstuaton, s e e tører efet t øe-<br>|||
|stedet.<br>Hvis afrimningsføleren registrerer en højere temperatur end den her indstillede,<br>bliver ventilatorerne stoppet. Der startes igen 2 K under indstillingen.<br>|||
|Funktionen er ikke aktiv under en afrimning eller ved opstart efter en afrimning. Med<br>indstillingen +50°C er funktionen afbrudt.|||
|<br>**Pulsdrift af ventilator**<br>|F05|FanPulseMode|
|0: Ingen pulsdrift<br>1: Pulsdrift når termostaten ikke kalder på køling|||
|<br>2: Pulsdrift når termostaten ikke kalder på køling, men kun under natdrift|||
|**Pulsdriftperiode for ventilator**<br>Her indstilles den samledepulstid. Summen af on-til ogoff-tid.|F06|Fan cycle|
|On-tid for ventilator<br>Her indstilles den %-del afperioden, som ventilatorerne skal være i drift.|F07|Fan ON %|
|Lysdioden på regulatorens front vil vise om ventilatoren er i gang.||Fan Relay<br>Her kan du aflæse ventilatorrelæets<br>status eller du kan tvangsstyre relæet i<br>"Manual control" mode.|
|**Internt afrimningsskema / urfunktion**|||
|(Benyttes ikke, hvis der anvendes et eksternt afrimningsskema via datakommunika-<br>|||
|tion.)<br>Der kan indstilles op til 6 individuelle klokkeslet for afrimningsstarter i døgnet.|||
|Afrimningsstart, timeindstilling|t01-t06||

19

|Afrimningstart, minutindstilling (1 og 11 hører sammen. osv.)<br>Med alle t01 til t16=0 starter uret ikke afrimniner|t11-t16||
|---|---|---|
|g.<br>Realtidsur:|||
|Indstilling af uret er kun relevant, når der ikke er datakommunikation.<br>Ved strømudfald under 4 timer, vil urfunktionen blive bevaret.|||
|Ur: Timeindstilling|t07||
|Ur: Minutindstilling|t08||
|Ur: Datoindstilling|t45||
|Ur: Månedsindstilling|t46||
|Ur: Årsindstilling|t47||
|**Diverse**||Miscellaneous|
|**Forsinkelse af udgangssignaler ved opstart**<br>Ved opstart eller efter strømudfald kan regulatorens funktioner forsinkes, så en evt.<br>overbelastning af el-nettet undgås.<br>Her kan du indstille forsinkelsestiden.|o01|DelayOfOutp.|
|**Digitalt indgangssignal - DI1**<br>Regulatoren har en digital indgang 1, der kan anvendes til en af de følgende funktio-<br>ner:|o02|DI 1 Config.<br>Definitionen sker med talværdien, der<br>er vist til venstre.|
|Off: Indgangen anvendes ikke.||(0 = off)|
|f<br>1) Statusvisning af en kontaktfunktion<br>||f|
|2) Dørfunktion. Når indgangen er åben, er det signal om, at døren er åben. Kølingen<br>og ventilatorerne stoppes og lyset tændes. Når tidsindstillingen i "A04" passeres,<br>gives alarm og kølingen genstartes (o89).|||
|<br>3) Døralarm. Når indgangen er åben, er det signal om, at døren er åben og lyset er||DI state|
|<br>tændt. Når tidsindstillingen i "A04" passeres, gives alarm.||(Måling)|
|<br>4) Afrimning. Funktionen startes med pulstryk. Regulatoren vil registrere, når indgan-<br>gen bliver sluttet. Herefter starter regulatoren en afrimning.<br>5) Main switch. Der reguleres, når indgangen er kortsluttet, og reguleringen stoppes,<br>når indgangen brydes.||Her vises Di-indgangens aktuelle<br>status. On eller off.|
|<br>6) Natdrift. Når indgangen kortsluttes, reguleres med natdrift.<br>7) Termostat bånd skift. Der skiftes over til termostat 2 (r21).|||
|8) Searat alarmfunktion Der ives alarm når indanen kortsluttes|||
|p .  g ,  gg .<br>9) Separat alarmfunktion. Der gives alarm, når indgangen åbnes. (For 8 og 9 indstilles<br>forsinkelsestiden i A27.)|||
|<br>10) Møbelrengøring. Funktionen startes med pulstryk. Se også beskrivelsen side 5.<br>11) Tvangskøling ved varmgasafrimning når indgangen kortsluttes.|||
|<br>12) Natafdækning|||
|<br>Hvis regulatoren kobles op i et net med datakommunikation, skal den have en<br>adresse, og systemenheden på datakommunikationen skal så kende denne adresse.|||
|Adressen indstilles  imellem 0 og 240, afhængig af systemenhed og valgt datakom-<br>munikation. Er systemenheden en gateway type AKA 245 skal versionen være 6.20<br>eller nyere.|o03||
|Adressen sendes til systemenheden, når menuen indstilles til ON<br>VIGTIGT: Inden du indstiller o04 SKAL du indstille o61. Ellers får du det forkerte data-<br>sæt sendt afsted.|o04||
|<br>(Funktionen benyttes ikke når datakommunikationen er MODBUS)|||
|**Adgangskode 1 (Adgang til alle indstillinger)**<br>Hvis indstillingerne i regulatoren skal beskyttes med en adgangkode, kan du indstille<br>en talværdi imellem 0 og 100. Hvis ikke, kan du annullere funktionen med indstillin-<br>gen=0. (99 vil altid give adgang.)|o05|Acc. code<br>i|
|**Følertype for S3 S4 S5 S6**|o06|SensorConfig|
|**, , ,**<br>Normalt anvendes en Pt 1000 føler med stor signalnøjagtighed. Men der kan også<br>anvendes en PTC-1000 Ω føler med en anden signalnøjagtighed.<br>**Alle**de monterede S3-S6 følere skal være af samme type.||i<br>Pt = 0<br>PTC = 1|
|<br>**Max. standby-tid efter koordineret afrimning**|o16|Max HoldTime|
|<br>Når en regulator er færdig med en afrimning, vil den afvente et signal, der fortæller<br>om kølingen må genoptages. Hvis dette signal udebliver af en eller anden grund, vil<br>|||
|regulatoren selv påbegynde kølingen, når denne standby-tid er gået.|||
|<br>**Vælg signal til displayvisningen S4%**<br>i|o17|Disp. S4%|
|Her skal du definere det signal, som displayet skal vise.<br>S3 S4  ll  kbiti f d b|||
|,   eer en omnaon a em egge.<br>Med indstillingen 0% anvendes kun S3. Med 100% anvendes kun S4.|||
|Pe. Arbejdsområdet for tryktransmitteren - min. værdi|o20|MinTransPres|
|Pe. Arbejdsområdet for tryktransmitteren - max. værdi|o21|MaxTransPres|

20

|**Kølemiddelindstilling**(kun hvis "r12" = 0)<br>Inden kølingen kan startes, skal kølemidlet defineres. Der kan vælges imellem føl-<br>gende kølemidler:<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.  6=R13.  7=R13b1.  8=R23.  9=R500.<br>10=R503.  11=R114.  12=R142b. 13=Brugerdefineret. 14=R32. 15=R227.  16=R401A.<br>17=R507. 18=R402A.  19=R404A. 20=R407C.  21=R407A.  22=R407B.  23=R410A.<br>24=R170.  25=R290.  26=R600.  27=R600a.  28=R744.  29=R1270. 30=R417A.<br>31=R422A<br>Advarsel: Forkert valg af kølemiddel kan medføre skade på kompressoren.<br>Andre kølemidler: Her vælges indstilling 13 og derefter skal der indstilles tre faktorer<br>-Ref.Fac a1, a2 og a3-via AKM.|o30|Refrigerant|
|---|---|---|
|**Digitalt indgangssignal - DI2**<br>Regulatoren har en digital indgang 2, der kan anvendes til en af de følgende funktio-<br>ner:|o37|DI2 config.|
|Off: Indgangen anvendes ikke.<br>1) Statusvisning af en kontaktfunktion<br>2) Dørfunktion. Når indgangen er åben, er det signal om, at døren er åben. Kølingen<br>og ventilatorerne stoppes. Når tidsindstillingen i "A04" passeres, gives alarm og<br>kølingen genstartes (o89).<br>3) Døralarm. Når indgangen er åben, er det signal om, at døren er åben. Når tids-<br>indstillingen i "A04" passeres, gives alarm.<br>4) Afrimning. Funktionen startes med pulstryk. Regulatoren vil registrere, når ind-<br>gangen bliver sluttet. Herefter starter regulatoren en afrimning. Hvis signalet skal<br>modtages af flere regulatorer, er det vigtigt at ALLE tilslutninger monteres ens (DI<br>til DI og GND til GND).|||
|5) Main switch. Der reguleres, når indgangen er kortsluttet, og reguleringen stoppes,<br>når indgangen brydes.<br>6) Natdrift. Når indgangen kortsluttes, reguleres med natdrift.<br>7) Termostat bånd skift. Der skiftes over til termostat 2 (r21).<br>8) Separat alarmfunktion. Der gives alarm, når indgangen kortsluttes.<br>9) Separat alarmfunktion. Der gives alarm, når indgangen åbnes.<br>10) Møbelrengøring. Funktionen startes med pulstryk. Se også beskrivelsen side 5.<br>11) Tvangskøling ved varmgasafrimning når indgangen kortsluttes.<br>12) Natgardin. Når indgangen kortsluttes, aktiveres natgardinet.<br>13) Indgangen anvendes til koordineret afrimning sammen med andre regulatorer af<br>t|||
|samme ype.<br>**Konfiguration af lysfunktion**<br>1) Lys styres via dag/nat<br>2) Lys styres via datakommunikationen og "Light remote o39"<br>3) Lys styres af dørkontakt, der er defineret i enten o02, o37 eller o84, hvor indstillin-<br>gen er valgt til enten 2 eller 3. Når døren åbnes vil relæet trække. Når døren ingen<br>lukkes, vil der være et efterløb på 2 minutter inden lyset slukkes.<br>4) Som"2"men ved evt 15 min netværksfejl vil lyset tænde og natgardinet åbne|o38|Light config|
|.  . ,      .<br>**Aktivering af lysrelæ**<br>Her kan lysrelæet aktiveres, men kun hvis det er defineret i o38 med indstilling 2.|o39|Light remote|
|**Kantvarme under dagdrift**<br>On-perioden indstilles i % af tiden|o41|Railh.ON day%|
|**Kantvarme under natdrift**<br>On-perioden indstilles i % af tiden|o42|Railh.ON ngt%|
|**Kantvarmecyklus**<br>Periodetiden for den samlede On-tid + Off-tid indstilles i minutter|o43|Railh. cycle|
|**Møbelrengøring**<br>Her kan status på funktionen følges eller funktionen kan startes manuelt.<br>**0=**Normaldrift (ingen rengøring)<br>**1=**Rengøring med ventilatorer i drift. Alle andre udgange er Off.<br>**2=**Rengøring med stoppede ventilatorer. Alle udgange er Off.<br>Hvis funktionen styres med et signal på DI1, DI2 eller DI3-indgangen, kan den aktu-<br>elle status ses her i menuen.|o46|Case clean|
|**Valg af application**<br>Regulatoren kan konfigureres på forskellig vis. Her indstilles hvilken af de 10 anven-<br>delser, der ønskes. På side 12 kan du se oversigten over anvendelser.<br>Denne menu kan kun indstilles, når reguleringen er stoppet dvs. "r12" er indstillet til 0.|o61|Appl. Mode|
|**Overfør et sæt af forudindstillinger til regulatoren**<br>Der er mulighed for at vælge en hurtig indstilling af en række parametre. Der tages<br>udgangspunkt i, om der skal reguleres et møbel eller et rum, og om afrimningen skal<br>stoppes på tid eller på temperatur. Oversigten kan ses på side 27.<br>Denne menu kan kun indstilles, når reguleringen er stoppet dvs. "r12" er indstillet til 0.|o62|-|
|Efter indstillingen vil værdien falde tilbage til 0.  En efterfølgende justering/indstilling<br>afparametre kan foretages efter ønske.|||

21

|**Adgangskode 2 (Adgang til justeringer)**<br>D  d til ti f di  ikk til kfitiidtilli|o64|Acc. code 2|
|---|---|---|
|er er agang  juserng a værer, men e  oniguraonsnsnger.<br>Hvis indstillingerne i regulatoren skal beskyttes med en adgangkode, kan du indstille<br>en talværdi imellem 0 og 100. Hvis ikke, kan du annullere funktionen med indstillin-<br>gen = 0. Hvis funktionen anvendes**skal**adgangskode 1 (o05)**også**anvendes.|||
|**Gem som fabriksindstilling**<br>Med denne funktion gemmes regulatorens aktuelle indstillinger som en ny grundind-<br>stilling (de tidligere fabriksindstillinger overskrives).|o67|-|
|**Digitalt indgangssignal - DI3 (High voltage input)**<br>Regulatoren har en digital indgang 3, der kan anvendes til en af de følgende funktio-<br>ner:|o84|DI3 config.|
|Off: Indgangen anvendes ikke.<br>1) Statusvisning af 230 V signal|||
|<br>2) Dørfunktion. Når indgangen er 0 V, er det signal om, at døren er åben. Kølingen<br>og ventilatorerne stoppes. Når tidsindstillingen i "A04" passeres, gives alarm og<br>kølingen genstartes (o89).|||
|<br>3) Døralarm. Når indgangen er 0 V, er det signal om, at døren er åben. Når tidsindstil-<br>lingen i "A04" passeres, gives alarm.<br>4) Afrimning. Funktionen startes med pulstryk. (puls på 230 V)<br>5) Main switch. Der reguleres, når indgangen er 230 V, og reguleringen stoppes, når<br>indgangen er 0 V|||
|.<br>6) Natdrift. Når indgangen 230 V, reguleres med natdrift.<br>7) Termostat bånd skift. Der skiftes over til termostat 2 (r21).<br>8) Benyttes ikke.<br>|||
|9) Benyttes ikke.<br>10) Møbelrengøring. Funktionen startes med pulstryk (puls på 230 V). Se også beskri-<br>velsen side 5.<br>11) Tvangskøling ved varmgasafrimning når indgangen 230 V.<br>12) Natafdækning<br>13) Benyttes ikke|||
|<br>14) Kølingen stoppes med funktionen"Forced closing"|||
|**Kantvarmestyring**<br>Kantvarmen kan styres på flere måder:<br>|o85|Railh. mode|
|0: Funktionen anvendes ikke<br>1: Der pulsstyres med en timerfunktion efter dag/natdrift (o41 og o42)<br>2: Der pulsstyres med en dugpunktsfunktion. Denne funktion kræver, at der modta-<br>ges et signal om dugpunktsværdien. Værdien måles af en System manager og sendes<br>til regulatoren via datakommunikationen.|||
|**Dugpunktsværdi hvor kantvarmen er minimum**<br>Funktionen er omtalt tidligere i manualen.|o86|DewP Min lim|
|**Dugpunktsværdi hvor kantvarmen er maximun**<br>Funktionen er omtalt tidligere i manualen.|o87|DewP Max lim|
|**Lavest tilladelige kantvarmeeffekt**<br>Her indstilles den %-del af effekten, som skal afgives, når dugpunktsværdien er mini-<br>mum.|o88|Rail Min ON%|
|**Start af kølingen ved åben dør**<br>Hvis døren er efterladt åben, skal kølingen startes efter en given tid. Her indstilles<br>tiden.|o89|DoorInjStart|
|**Ventilator ved "Forced Closing"**<br>Her indstilles om ventilatorerne skal være i drift eller være stoppet, hvis funktionen<br>"Forced closing" bliver aktiveret.<br>Ved "No eller 0" bliver ventilatorerne stoppet|o90|Fan ForcedCl|
|<br>Ved"Yes eller 1"vil de være i drift|||
|.<br>**Alternativ visning**<br>Ved tryk på regulatorens nederste knap, kan der vises en udlæsning. Fra fabrikken er<br>denne udlæsning indstillet, så afrimningsstoptemperaturen bliver vist.<br>En anden indstilling vil give følgende udlæsning:<br>1: (Afrimningsstoptemperatur = fabriksindstilling)<br>|o92|Displ menu 2|
|2: S6 temperatur<br>3: S5B temperatur (kun anvendelse 9)|||
|<br>**Temperaturvisning under normaldrift**<br>1: Lufttemperatur. Vægtet S3 + S4<br>2: Produkttemperatur S6|o97|Disp. Ctrl.|
|**Lys og natgardin definition**<br>0 L  lkkt  tdi  åb å hdfbd  ff|o98|Light MS = Off|
|: ys er sue og nagarn er en, nr ovearyer er of<br>1: Lys og natgardin er uafhængig af hovedafbryder.|||

|**Konfiguration af alarmrelæet**|P41|Al.Rel.Conf.|
|---|---|---|
|Alarmrelæet vil blive aktiveret ved en alarm i en af de følgende grupper:<br>1 - Højtemperaturalarmer<br>2 - Lavtemperaturalarmer<br>4 - Følerfejl|||
|8 - Digital indgang aktiveres til alarm<br>16 - Afrimningsalarmer<br>32 - Diverse<br>64 - Indsprøjtningsalarmer|||
|<br>Hvilke grupper, der skal aktivere alarmrelæet, skal indstilles med en talværdi, der er<br>summen af de grupper, der skal aktiveres.<br>|||
|(Fx: en værdi på 5 vil aktivere alle højtemperaturalarmer og alle følerfejl. En værdi på 0<br>l|||
|vil aflyse relæfunktionen.)|||
|**Service**||**Service**|
|Temperaturen målt med S5 føleren|u09|S5 temp.|
|Statuspå DI1 indgangen. On/1=sluttet|u10|DI1 status|
|Aflæse varigheden af den igangværende afrimning eller varigheden af den sidst<br>afsluttede afrimning|u11|Defrost time|
|Temperaturen målt med S3 føleren|u12|S3 air temp|
|Statuspå natdrift(on eller off)on =natdrift|u13|Night Cond.|
|Temperaturen målt med S4 føleren|u16|S4 air temp|
|Termostattemperaturen<br>l|u17|Ther. air|
|Aflæse den igangværende indkoblingstid for termostaten eller varigheden af den|u18|Ther runtime|
|sidst afsluttede indkobling<br>l|||
|Aflæse temperaturen ved S1 føleren|u19|S1 temp.|
|Aflæse temperaturen ved S2 føleren<br>l|u20|S2 temp.|
|Aflæse overhedningen|u21|Superheat|
|Aflæse reguleringens aktuelle overhedningsreference|u22|SH ref.|
|Aflæse ventilens aktuelle åbningsgrad<br>l|u23|AKV OD %|
|Aflæse fordampningstrykket|u25|Evap.press Pe|
|l<br>Aflæse fordampningstemperaturen|u26|Evap.tempTe|
|Aflæse temperaturen ved S6 føleren|u36|S6 temp|
|Statuspå DI2 udgangen. On/1=sluttet|u37|DI2 status|
|Lufttemperatur. Vægtet S3 + S4 temp.|u56|Displayair|
|Målt temperatur til alarmtermostaten|u57|Alarm air|
|* Statuspå relæet til køling|u58|Comp1/LLSV|
|* Statuspå relæet til ventilator|u59|Fan relay|
|* Statuspå relæet til afrimning|u60|Def. relay|
|* Statuspå relæet til kantvarme|u61|Railh. relay|
|* Statuspå relæet til alarm|u62|Alarm relay|
|* Statuspå relæet til lys|u63|Light relay|
|* Statuspå relæet til ventil i sugeledningen|u64|SuctionValve|
|* Statuspå relæet til kompressor 2|u67|Comp2 relay|
|* Temperaturen målt med S5B føleren|u75|S5 temp. B|
|* Statuspå relæet til varmgas|u80|Hotgas valve|
|* Statuspå relæet til varmelegemet i drypbakken|u81|Driptray|
|* Statuspå relæet til natgardin|u82|Blinds relay|
|* Statuspå relæet til afrimningB|u83|Def. relayB|
|* Statuspå relæet til varmefunktionen|u84|Heat relay|
|* Udlæsningaf den aktuelle kantvarmeeffekt i %|u85|Rail DutyC %|
|Udlæsning af hvilken termostat, der reguleres efter: 1= Thermostat 1,|u86|Ther. band|
|<br>2= Thermostat 2|||
|Statuspå indgangen DI3 (on/1 = 230 V)|u87|DI3 status|
|Udlæsningaf den aktuelle indkoblingsværdi for termostaten|u90|Cutin temp.|
|Udlæsningaf den aktuelle udkoblingsværdi for termostaten|u91|Cutout temp.|

23

|Status på funktionen "Adaptiv afrimning"<br>f|U01|AD state|
|---|---|---|
|0: Off. Funktionen er ikke aktiveret|||
|1: Fejl. Der skal gennemføres en reset med d22|||
|2: Reset er aktiveret. Ny tuning er igang|||
|3: Normal|||
|4: Let is-opbygning|||
|5: Medium is-opbygning|||
|6: Kraftigis-opbygning|||

*) Ikke alle vil blive vist. Der vises kun den funktion, der hører til den valgte application.

|**Driftstatus**||**(Measurement)**|
|---|---|---|
|Regulatoren gennemgår nogle reguleringssituationer, hvor den bare venter på  næste<br>punkt i reguleringen. For at synliggøre disse "hvorfor sker der ikke noget", kan du<br>se en driftsstatus i displayet. Tryk kortvarig (1s) på den øverste knap. Hvis der er en<br>statuskode, vil den blive vist i displayet.<br>De enkelte statuskoder betyder følgende:||Ctrl. state:<br>(Vises i alle menubilleder.)|
|Normal regulering|S0|0|
|Venterpå at den koordinerede afrimningafsluttes|S1|1|
|Når kompressoren er i drift,skal den mindst køre i x minutter.|S2|2|
|Når kompressoren er stoppet,skal den mindst være stoppet i x minutter.|S3|3|
|Fordamperen drypper af ogafventer,at tiden udløber.|S4|4|
|Kølingen er stoppet med en hovedafbryder. Enten med r12 eller en DI-indgang|S10|10|
|Kølingen er stoppet af termostaten|S11|11|
|Afrimningssekvens. Der afrimes|S14|14|
|Afrimningssekvens. Ventilatorforsinkelse — vand bindes til fordamperen|S15|15|
|Kølingen er stoppetpga. stoppet indsprøjtningsfunktion eller stoppet regulering|S16|16|
|Døren er åben(åben DI indgang)|S17|17|
|Smeltefunktionen er igang. Kølingen er afbrudt|S18|18|
|Modulerende termostatregulering|S19|19|
|Nødkøling*)|S20|20|
|Reguleringsproblem i indsprøjtningsfunktionen|S21|21|
|Opstartsfase 2. Fordamperen fyldes|S22|22|
|Adaptiv regulering|S23|23|
|Opstartsfase 1. Signalsikkerheden fra følerne kontrolleres|S24|24|
|Manuel styringaf udgange|S25|25|
|Kølemiddeltypen er ikke indstillet|S26|26|
|Møbelrengøring|S29|29|
|Tvangskøling|S30|30|
|Forsinkelse af udgange ved opstart|S32|32|
|Varmefunktionen r36 er aktiv|S33|33|
|Andre visninger:|||
|Afrimningstemperaturen kan ikke vises. Der stoppespå tid|non||
|Afrimningen er igang. / Første nedkøling efter afrimningen hvor temperaturen fortsat<br>er over termostatbåndet|-d-||
|Password erpåkrævet.  Indstilpassword|PS||
|Reguleringen er stoppet via hovedafbryderen|OFF||

*) Nødkøling vil træde i kraft ved manglende signal fra en defineret S3 eller S4 føler. Reguleringen vil fortsætte med en registreret gennnemsnitlig indkoblingsfrekvens. Der er to registrerede værdier — én for dagdrift og én for natdrift.

24

###### **Fejlmeddelelser**

I en fejlsituation vil lysdioderne på fronten blinke, og alarmrelæet bliver aktiveret.

Hvis du trykker på den øverste knap i denne situation, kan du se alarmmeddelelsen i displayet. Er der flere, kan du trykke videre og se dem. Der er to former for fejlmeddelelser - enten er det en alarm, der optræder under den daglige drift, eller det er en fejl i installationen. A-alarmer vil først blive synlige, når den indstillede tidsforsinkelse er udløbet. E-alarmer vil derimod straks blive synlige, når fejlen indtræder. Her er de meddelelser, der kan komme:

|**Kode / Alarmtekst via**<br>**datakommunikation**|**Betydning**|||**Alarmrelæ grupper**<br>**(P41)**|
|---|---|---|---|---|
|A1/---  High t.alarm|Højtemperaturalarm|||1|
|A2/---  Low t. alarm|Lavtemperaturalarm|||2|
|A4/--- Door alarm|Døralarm|||8|
|A5/--- Max hold time|Funktionen "o16" er aktiveret under en koordineret afrimning|||16|
|A10/--- Inject prob.|Reguleringsproblem|||64|
|A11/--- No Rfg. sel.|Der er ikke valgt kølemiddel|||64|
|A13/--- High temp S6|Temperaturalarm. Høj S6|||1|
|A14/--- Low temp S6|Temperaturalarm. Lav S6|||2|
|A15/--- DI1 alarm|DI1 alarm|||8|
|A16/--- DI2 alarm|DI2 alarm|||8|
|A45/--- Standby mode|Standby tilstand (stoppet køling via r12 eller DI-indgang)|||-|
|A59/--- Case clean|Møbelrengøring. Signal fra DI-indgang|||-|
|A74/--- AD fault|Fejl i den adaptive afrimningsfunktion|||16|
|A75/--- AD Iced|Fordamperen er tiliset. Der er reduceret luftgennemgang|||16|
|A76/--- AD not defr.|Fordamperen er ikke afrimet tilfredsstillende|||16|
|E1/---  Ctrl. error|Fejl i regulatoren|||32|
|E6/--- RTC error|Kontrollér ur|||32|
|E20/--- Pe error|Fejl på tryktransmitter Pe|||64|
|E23/--- S1 error|Fejl på S1 føleren|||4|
|E24/--- S2 error|Fejl på S2 føleren|||4|
|E25/--- S3 error|Fejl på S3 føleren|||4|
|E26/--- S4 error|Fejl på S4 føleren|||4|
|E27/--- S5 error|Fejl på S5 føleren|||4|
|E28/--- S6 error|Fejl på S6 føleren|||4|
|E37/--- S5 error B|Fejl på S5B føleren|||4|
|---/--- Max Def.Time|Afrimningen er stoppet på tid i stedet for temperatur|||16|
|**Datakommunikation**<br>Vigtigheden af de enkelte   i|alarmer kan defineres med en indstilling. Indstillingen skal foretages i gru|i        ppen "Alarm|i          destinations"||
|Indstilling fra|Indstilling fra<br>Log<br>Alarmrelævalg||Sendes over||
|Systemmanager|AKM (AKM destination)<br>Ingen<br>Høj|Lav-Høj|Netværk||
|Høj|<br><br><br>1<br>X<br>X|X|X||
|Middel|2<br>X|X|X||
|Lav|3<br>X|X|X||
|Kun log<br>Afbrudt|X||||

25

### **Betjening**

##### **Display**

Værdierne bliver vist med tre cifre, og med en indstilling kan du bestemme, om temperaturen skal vises i °C eller i °F.

##### **Lysdioder på fronten**

Lysdioderne vil lyse, når det tilhørende relæ er aktiveret:

- = køling

- = afrimning

- = ventilator i gang

Lysdioderne vil blinke, når der er en alarm.

I denne situation kan du kalde fejlkoden frem på displayet og udkoble / kvittere alarmen ved at trykke kortvarigt på den øverste knap.

##### **Knapperne**

Når du vil ændre en indstilling, vil den øverste og nederste knap give en højere eller en lavere værdi alt efter hvilken knap, du trykker på. Men før du kan ændre værdien, skal du have adgang ind i menuen. Det får du ved at trykke på den øverste knap i et par sekunder – så kommer du ind i rækken med parameterkoder. Find den parameterkode du vil ændre, og tryk så på den midterste knap så værdien for parameteren vises. Når du har ændret værdien, gemmer du den nye værdi ved igen at trykke på den midterste knap

##### **Kom godt igang**

Med følgende procedure vil du få reguleringen startet hurtigst mulig:

- **1** Åbn parameter r12 og stop reguleringen (i et nyt og ikke tidligere indstillet apparat, vil r12 allerede være indstillet til 0, som betyder stoppet regulering)

- **2** Vælg elforbindelse ud fra tegningerne side 12 eller13

- **3** Åbn parameter o61 og indstil elforbindelsesnummeret heri

- **4** Vælg derefter et sæt af forudindstillinger fra hjælpeskemaet side 27

- **5** Åbn parameter o62 og indstil nummeret for sættet af forudindstillinger. Herefter overføres de få udvalgte indstillinger til menuen

- **6** Åben parameteren n57 og vælg metode for måling af fordampningstryk Pe eller S1 (fabriksindstilling er Pe tryktransmitter)

- **7** Hvis der anvendes tryktransmitter Pe skal du også vælge kølemiddel via parameter o30

- **8** Åbn parameter r12 og start reguleringen

- **9** Se oversigten over fabriksindstillinger igennem. Værdierne i de grå felter er ændret iht. dit valg af forudindstillinger. — Foretag de nødvendige ændringer i de respektive parametre

- **10** Ved netværk. Indstil adressen i o03

- **11** Send adressen til systemenheden:

##### Eksempler

##### Indstille en menu

1. Tryk på den øverste knap til parameteren r01 vises

2. Tryk på øverste eller nederste knap og find hen til den parameter, du vil indstille

   - Ved MODBUS: Aktivér skanfunktionen i systemenheden

   - Hvis der er indsat et andet datakommunikationskort i regulatoren:

   - LON RS485: Aktiver funktionen o04

   - DANBUSS: Aktiver funktionen o04

   - Ethernet: Anvend MAC-adressen

3. Tryk på den midterste knap hvorefter værdien vises

4. Tryk på den øverste eller den nederste knap og indstil den nye værdi

5. Tryk igen på den midterste knap for at gemme værdien.

##### Udkoble alarmrelæ / kvittere alarm /se alarmkode

- Kort tryk på den øverste knap.

Hvis der er flere alarmkoder ligger de i en rullestak. Tryk på den øverste eller nederste knap for at se rullestakken igennem.

##### Indstille temperaturen

1. Tryk på den midterste knap hvorefter temperaturindstillingen vises

2. Tryk på den øverste eller den nederste knap og indstil den nye værdi

3. Tryk på den midterste knap for at gemme indstillingen.

Aflæse temperaturen ved afrimningsføleren (Eller produktføleren, hvis det er valgt i o92.)

- Kort tryk på den nederste knap

##### Manuel start eller stop af en afrimning

- Tryk på den nederste knap i 4 sekunder.

26

##### **Hjælpeskema til indstillinger (quick-setup)**

|||**Møbler**|||**Rum**||
|---|---|---|---|---|---|---|
||Afr. stop på tid|Afr. stop|på S5|Afr. stop på tid|Afr. stop|på S5|
|**Sæt af forudindstillinger**(o62)|**1**|**2**|**3**|**4**|**5**|**6**|
|Temperatur (SP)|2°C|-2°C|-28°C|4°C|0°C|-22°C|
|Max. temp. indstilling(r02)|6°C|4°C|-22°C|8°C|5°C|-20°C|
|Min. temp. indstilling(r03)|0°C|-4°C|-30°C|0°C|-2°C|-24°C|
|Følersignal til termostaten. S4% (r15)||100%|||0%||
|Alarmgrænse høj(A13)|8°C|6°C|-15°C|10°C|8°C|-15°C|
|Alarmgrænse lav (A14)|-5°C|-5°C|-30°C|0°C|0°C|-30°C|
|Følersignal til alarmfunk. S4% (A36)|0%||100%||0%||
|Interval imellem afrimn. (d03)|6 h|6h|12h|8h|8h|6h|
|Afrimningsføler: 0=time,1=S5, 2=S4 (d10)|0|1|1|0|1|1|
|DI1 config. (o02)|Mø|belrengøring(=10|)||Dørfunktion (=2)||
|Følersignal til displayvisning. S4% (017)||||0%|||

Bemærk: For anvendelse 9 og 10 benyttes følervægtningen for S3/S4 følerne for termostat, alarmtermostat og displayudlæsning ikke, idet føleranvendelserne er prædefineret .

27

### **Menuoversigt**

||||||||||<br>|SW = 1.5x<br>|
|---|---|---|---|---|---|---|---|---|---|---|
|**Parametre**<br>**Funktion**|Kode|**El**<br>1<br>2<br>|**-di**<br>3|**agram s**<br>4<br>5|**ide 12 eller 13**<br>6<br>7<br>8|<br>9<br>10|**Min.**<br>**værdi**|**Max.**<br>**værdi**|**Fabriks-**<br>**indstil-**<br>**li**|**Aktuel**<br>**indstil-**<br>**li**|
|**Normaldrift**|||||||||**ng**|**ng**|
|Temperatur(setpoint)<br>|- - -|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-50°C|50°C|2||
|**Termostat**<br>f|||||||||||
|Differens|r01|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|0.1 K|20 K|2||
|f<br>Max. begrænsningaf setpunktsindstilling<br>Min. begrænsningaf setpunktsindstilling|r02<br>r03|1<br>1<br><br>1<br>1<br>|1<br>1|1<br>1<br>1<br>1|1<br>1<br>1<br>1<br>1<br>1|1<br>1<br>1<br>1|-49°C<br>-50°C|50°C<br>49°C|50<br>-50||
|Justering af temperaturvisning|r04|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-10|10|0||
|Temperaturenhed(°C/°F)|r05|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|0/°C|1/F|0/°C||
|Korrektion af signalet fra S4<br>k fl f|r09<br>|1<br>1<br><br><br><br>|1<br>|1<br>1<br><br>|1<br>1<br>1<br><br><br>|1<br>1<br><br>|-10 K<br>|10 K<br>|0<br>||
|Korretion a signaet ra S3<br>Manuel service, Stop regulering, Start regulering<br>(-1,0,1)|r10<br>r12|1<br>1<br><br>1<br>1<br>|1|1<br>1<br>1<br>1|1<br>1<br>1<br>1<br>1<br>1|1<br>1<br>1<br>1|-10 K<br>-1|10 K<br>1|0<br>0||
|Referenceforskydningunder natdrift<br>i|r13|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-50 K|50 K|0||
|Termostatfunktionen defineres<br>1 = ON/OFF,2 = Modulerende|r14|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|1|2|1||
|Definition o evt vætnin af termostatfølere - S4%|r15|1<br>1<br>|1|1<br>1|1<br>1<br>1||0 %|100 %|100||
|i g . gg<br>(100%=S4,0%=S3)|||||||||||
|Tid imellem smelteperioder|r16|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|0 hrs|10 hrs|1||
|Smelteperiodens varighed|r17|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|0 min.|30 min.|5||
|Temperaturindstilling for termostatbånd 2. Som dif-<br>feres benyttes r01|r21|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-50°C|50°C|2||
|Korrektion af signalet fra S6<br>i|r59<br>|1<br>1<br>|1|1<br>1|1<br>1<br>1<br>|1|-10 K<br>|10 K<br>|0<br>||
|Definition og evt. vægtning af termostatfølere, når<br>natafdækningen erpå.(100%=S4,0%=S3)|r61||||1||0 %|100 %|100||
|Varmefunktion<br>Neutralzone imellem køle- og varmefunktion|r62||||1||0 K|50 K|2||
|Tidsforsinkelse ved skift fra køle- til varmefunktion<br>|r63||||1||0 min.|240 min.|0||
|**Alarmer**<br>Forsinkelsepå temperaturalarm<br>Forsinkelseå døralarm|A03<br>A04|1<br>1<br><br>1<br>1<br>|1<br>1|1<br>1<br>1<br>1|1<br>1<br>1<br>1<br>1<br>1|1<br>1<br>1<br>1|0 min.<br>0 min|240 min.<br>240 min|30<br>60||
|p <br>Forsinkelsepå temperaturalarm efter afrimning|A12|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|.<br>0 min.|.<br>240 min.|90||
|Højalarmgrænse for termostat 1|A13|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-50°C|50°C|8||
|Lav alarmgrænse for termostat 1<br>|A14<br>|1<br>1<br><br><br><br>|1<br>|1<br>1<br><br>|1<br>1<br>1<br><br><br>|1<br>1<br><br>|-50°C<br>|50°C<br>|-30<br>||
|Højalarmgrænse for termostat 2|A20|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-50°C|50°C|8||
|Lav alarmgrænse for termostat 2|A21|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|-50°C|50°C|-30||
|Højalarmrænse for S6-føleren ved termostat 1|A22|1<br>1<br>|1|1<br>1|1<br>1<br>1|1|-50°C|50°C|8||
|g  <br>Lav alarmgrænse for S6-føleren ved termostat 1|A23|1<br>1<br>|1|1<br>1|1<br>1<br>1|1|-50°C|50°C|-30||
|Højalarmgrænse for S6-føleren ved termostat 2|A24|1<br>1<br>|1|1<br>1|1<br>1<br>1|1|-50°C|50°C|8||
|Lav alarmrænse for S6-føleren ved termostat 2|A25|1<br>1<br>|1|1<br>1|1<br>1<br>1|1|-50°C|50°C|-30||
|g  <br>S6 alarmens forsinkelsestid|A26|1<br>1<br>|1|1<br>1|1<br>1<br>1|1|0 min.|240 min.|240||
|Med indstilling= 240,vil S6-alarmen blive udeladt|||||||||||
|Alarmforsinkelsestid efter signalpå DI1 indgangen<br>|A27<br>|1<br>1<br><br><br><br>|1<br>|1<br>1<br><br>|1<br>1<br>1<br><br><br>|1<br>1<br><br>|0 min.<br>|240 min.<br>|30<br>||
|Alarmforsinkelsestid efter signalpå DI2 indgangen|A28|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|0 min.|240 min.|30||
|Signal til alarmtermostaten.(100%=S4,0%=S3)|A36|1<br>1<br>|1|1<br>1|1<br>1<br>1||0 %|100 %|100||
|Forsinkelsepå S6(produktføleralarm)efter afrimning<br>|A52|1<br>1<br>|1|1<br>1|1<br>1<br>1|1|0 min.|240 min.|90||
|**Kompressor**<br>Min. ON-tid|c01|1<br>1<br>|1|1|||0 min.|30 min.|0||
|Min. OFF-tid<br>|c02<br>|1<br>1<br>|1|1<br>|||0 min.<br>|30 min.<br>|0<br>||
|Forsinkelsestid for indkoblingaf compr. 2<br>**Afrimning**|c05|||1|||0 sec|999 sec|5||
|Afrimningsmetode: 0=Ingen,1= EL,2= Gas<br>|d01<br>|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|0/Off|2/gAs|1/EL||
|Afrimnings-stoptemperatur<br>Interval mellem afrimningsstarter|d02<br>d03|1<br>1<br><br>1<br>1<br>|1<br>1|1<br>1<br>1<br>1|1<br>1<br>1<br>1<br>1<br>1|1<br>1<br>1<br>1|0°C<br>0 hrs/Off|50°C<br>240 hrs|6<br>8||
|<br>Max. afrimningsvarighed|d04|1<br>1<br>|1|1<br>1|1<br>1<br>1|1<br>1|f<br>0 min.|360 min.|45||
|Tidsforskydning på afrimningsindkoblingen ved opstart|d05|1<br>1<br>1||1<br>1|1<br>1<br>1|1<br>1|0 min.|240 min.|0||
|Afdrypningstid|d06|1<br>1<br>1||1<br>1|1<br>1<br>1|1<br>1|0 min.|60 min.|0||
|Forsinkelsepå ventilatorstart efter afrimning|d07|1<br>1<br>1||1<br>1|1<br>1<br>1|1<br>1|<br>0 min.|<br>60 min.|0||
|Ventilator-starttemperatur|d08|1<br>1<br>1||1<br>1|1<br>1<br>1|1<br>1|-50 °C|0 °C|-5||
|Ventilator indkoblet under afrimning|d09|1<br>1<br>||1<br>1|1<br>1<br>1|1<br>1|0|2|1||
|<br>0: stoppet<br>|||||||||||
|1: Kører<br>2: Kører underpumpdown ogafrimning|||||||||||
|Afiifl 0 =St å tid 1=S5 2=S4 3=S|d10|1<br>1<br>||1<br>1|1<br>1<br>1|1<br>1|0|3|0||
|rmnngøer:  op p , , , x<br>|||||||||||
|(Anvendelse 1-8 og 10: både S5 og S6.<br>Anvendelse 9: S5 ogS5B)|||||||||||
|Pumpdown forsinkelse<br>|d16<br>|1<br>1<br>1||1<br>1|1<br>1<br>1<br>|1<br>1|0 min.<br>|60 min.<br>|0<br>||
|Drain forsinkelse(benyttes kun ved varmgasafr.)<br>Max. opsummeret køletid imellem to afrimninger|d17<br>d18|1<br>1<br>1||1<br>1|1<br>1<br>1<br>1|1<br>1|0 min.<br>0 hrs|60 min.<br>48 hrs|0<br>0/OFF||

28

|**Fortsat**|**Kode**|**1**|**2**|**3**|**4**|**5**|<br>|**6**||**7**|**8**|**9**<br>|**1**|**0**<br>**Min.**|**Max.**|**Fab.**|**Aktuel**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Varme i afdrypningsbakke. Tid fra afrimningen stopper|d20||||||1|||||||0 min.|240 min.|30||
|til varmen i afdrypningsbakken slukkes<br>||||||||||||||||||
|Ekstra afrimning med adaptiv funktion tillades:<br>0=Ikke,  1=Kun overvågning,  2=Kun om dagen, 3=Både<br>dagognat,4=Kun om natten<br>Reset af den "Adaptive afrimningsfunktion" (starter en<br>afrimninostarter efterfølende en ntunin)|d21<br>d22|1<br>1|1<br>1|1<br>1|1<br>1|1<br>1|1||1||1<br>1|1<br><br>1<br>|1|0<br>0/OFF|4<br>1/ON|0<br>0/OFF||
|g g g y g<br>**Indsprøjtningsfunktionen**||||||||||||||||||
|Indsprøjtningsalgoritme<br>Bør kun ændres af instrueretpersonale|n05|1|1|1|1|1|1||1||1|1<br>|1|30 sec|600 sec|150||
|.<br>Max. begrænsningaf overhedningsreferencen<br>|n09<br>|1<br>|1<br>|1<br>|1<br>|1<br>|1<br>||1<br>||1<br>|1<br><br><br>|1<br>|3°C<br>|20°C<br>|12<br>||
|Min. begrænsningaf overhedningsreferencen<br>MOP temperatur. Off hvis MOP temp. = 15.0 °C|n10<br>n11|1<br>1|1<br>1|1<br>1|1<br>1|1<br>1|1<br>1||1<br>1||1<br>1|1<br><br>1<br>|1<br>1|3°C<br>-50°C|20°C<br>15°C|3<br>15||
|f<br>Glid ved Azeotropkølemiddel(kun ved S1-måling)<br>|n12<br>|1<br>|1<br>|1<br>|1<br>|1<br>|1<br>||1<br>||1<br>|1<br><br><br>|1<br>|0 K<br>|10 K<br>|0<br>||
|Periodetid of AKV pulsering<br>Bør kun ændres af instrueretpersonale.|n13|1|1|1|1|1|||1||1|1<br>|1|3 sec|6 sec|6||
|Indsprøjtningsalgoritme|n15|1|1|1|1|1|1||1||1|1<br>|1|30 sec|600 sec|180||
|Bør kun ændres af instrueretpersonale.||||||||||||||||||
|Indsprøjtningsalgoritme<br>Bør kun ændres af instrueret personale.|n16|1|1|1|1|1|1||1||1|1<br>|1|10 %|75 %|30||
|Indsprøjtningsalgoritme<br>Bør kun ændres af instrueretersonale|n17|1|1|1|1|1|1||1||1|1<br>|1|5 %|70 %|30||
|p.<br>Indsprøjtningsalgoritme<br>Bør kun ændres af instrueretpersonale|n18|1|1|1|1|1|1||1||1|1<br>|1|0|10|4||
|.<br>Indsprøjtningsalgoritme<br>Bør kun ændres af instrueretpersonale.|n23|1|1|1|1|1|1||1||1|1<br>|1|1|50|6||
|Indsprøjtningsalgoritme<br>Bør kun ændres af instrueretpersonale.|n24|1|1|1|1|1|1||1||1|1<br>|1|100 sec|1800 sec|900||
|Valg af signal til overhedningsmåling: 1= Tryk-<br>|n57|1|1|1|1|1|1||1||1|1<br>|1|1|2|1||
|transmitter AKS32R,2= Temperaturføler S1<br>||||||||||||||||||
|**Fan**<br>Ventilatorstoptemperatur S5<br>Pldift å tilt  0=N i ldift|F04<br>F05|1<br>1|1<br>1|1<br>1|1<br>1|1<br>1|1<br>||1<br>||1<br>1|1<br><br>1<br>|1<br>|-50°C<br>0|50°C<br>2|50<br>0||
|usr p venaorer:  ej ngen pusr,<br>1=Kun ved termostatudkoblinger,  2= Kun ved<br>termostatudkoblinger under natdrift||||||||||||||||||
|Periodetid for ventilatorpulsering (on-tid + off-tid)|F06|1|1|1|1|1|1||1||1|1<br>|1|1 min.|30 min.|5||
|f<br>On-tid i % afperiodetiden<br>|F07|1|1|1|1|1|1||1||1|1<br>|1|0 %|100 %|100||
|**Realtidsur**<br>Seks starttidspunkter for afrimning.<br>Indstillingaf timer. 0=OFF|t01 -<br>t06|1|1|1|1|1|1||1||1|1<br>|1|0 hrs|23 hrs|0||
|<br>Seks starttidspunkter for afrimning.<br>|t11 -<br>|1|1|1|1|1|1||1||1|1<br>|1|0 min.|59 min.|0||
|Indstillingaf minutter 0=OFF<br>Ur - Timeindstilling|t16<br>t07|1|1|1|1|1|1||1||1|1<br>|1|0 hrs|23 hrs|0||
|Ur - Minutindstilling|t08|1|1|1|1|1|1||1||1|1<br>|1|0 min.|59 min.|0||
|Ur - Indstillingaf dato|t45|1|1|1|1|1|1||1||1|1<br>|1|1 day|31 day|1||
|Ur - Indstillingaf måned<br>|t46<br>|1<br>|1<br>|1<br>|1<br>|1<br>|1<br>||1<br>||1<br>|1<br><br><br>|1<br>|1 mon.<br>|12 mon.<br>|1<br>||
|Ur - Indstillingaf år<br>|t47|1|1|1|1|1|||1||1|1<br>|1|0year|99year|0||
|**Diverse**<br>Forsinkelse af udgangssignaler efter opstart<br>Idil  å DI1 Fkti|o01<br>02|1<br>1|1<br>1|1<br>|1<br><br>1|1<br>1||1<br>|1<br>||1<br>1|1<br>1|1<br>1|0 sec<br>0|600 sec<br>12|5<br>0||
|ngangssgna  p . unon:<br>(0=ikke anvendt, 1=status på DI1. 2=dørfunktion<br>med alarm ved åben. 3=døralarm ved åben.<br>4=afrimningsstart (pulstryk).  5=ekstern<br>hovedafbryder. 6=natdrift. 7=termostat bånd<br>skift (r21 aktiveres). 8=alarmfunktion ved sluttet.<br>9=alarmfunktion ved åben. 10=møbelrengøring<br>|o|||||||||||||||||
|(pulstryk). 11=Tvangskøling ved varmgas-afrimning.),<br>12=natafdækning||||||||||||||||||
|Adresseå netværk(0=off)|o03|1|1|1|1|1|||||1|1|1|0|240|0||
|p f<br>On/Off omskifter (Service Pin meddelelse)<br>VIGTIGT! o61**skal**indstilles før o04<br>(anvendes kun ved LON 485 ogDANBUSS)|o04|1|1|1|1|1||1|1||1|1|1|0/Off|1/On|0/Off||
|Adgangskode 1(samtlige indstillinger)|o05|1|1|1|1|1||1|||1|1|1|0|100|0||
|<br>Anvendt følertype: 0=Pt1000,1=Ptc1000,|o06|1|1|1|1|1||1|1||1|1|1|0/Pt|1/Ptc|0/Pt||
|Max holdetid efter koordineret afrimning|o16|1|1|1|1|1||1|1||1|1|1|0 min.|360 min.|20||
|Vælg signal til displayvisningen.  S4%<br>(100%=S40%=S3)|o17|1|1|1|1|1||1|1||1|||0 %|100 %|100||
|, <br>Arbejdsområdet for tryktransmitteren - min. værdi|o20|1|1|1|1|1||1|1||1|1|1|-1 bar|5 bar|-1||
|Arbejdsområdet for tryktransmitteren - max. værdi|o21|1|1|1|1|1||1|1||1|1|1|6 bar|200 bar|12||
|Kølemiddelindstilling<br>1R12  2R22  3R134  4R502  5R717  6R13|o30|1|1|1|1|1||1|1||1|1|1|0|31|0||
|=.  =.  =a.  =.  =.  =.<br>7=R13b1.  8=R23.  9=R500.  10=R503.  11=R114.<br>12=R142b. 13=Brugerdefineret. 14=R32. 15=R227.<br>16=R401A.  17=R507. 18=R402A.  19=R404A.<br>20=R407C.  21=R407A.  22=R407B.  23=R410A.||||||||||||||||||
|24=R170.  25=R290.  26=R600.  27=R600a.  28=R744.<br>29=R1270. 30=R417A. 31=R422A.||||||||||||||||||

29

|**Fortsat**|**Kode**|**1**|<br>**2**|**3**<br>**4**<br>|**5**||**6**|**7**|**8**|**9**|**10**|**Min.**|**Max.**|**Fab.**|**Aktuel**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Indgangssignal på DI2. Funktion:<br>(0=ikke anvendt, 1=status på DI2. 2=dørfunktion<br>med alarm ved åben. 3=døralarm ved åben.<br>4=afrimningsstart (pulstryk).  5=ekstern<br>hovedafbryder. 6=natdrift. 7=termostat bånd<br>skift (r21 aktiveres). 8=alarmfunktion ved sluttet.<br>9=alarmfunktion ved åben. 10=møbelrengøring<br>(pulstryk). 11=Tvangskøling ved varmgasafrimning.|o37|1|1|1<br>1<br>|1|1||1|1|1|1|0|13|0||
|12=natafdækning. 13=koordineret afrimning)||||||||||||||||
|Konfiguration af lysfunktionen: 1=Lyset følger dag/<br>nat driften,  2=Lyset styres via datakommunikation via<br>‘o39’,  3=Lyset styres med en DI-indgang,  4=Som "2",<br>lt td  tfdki il åb hi|o38|1|1|1||1||1|1|1|1|1|4|1||
|men yse ænes og naaænngen v ne, vs<br>netværket falder ud i mere end 15 minutter.||||||||||||||||
|Aktiveringaf lysrelæ(kun hvis o38=2)On=lys<br>Kantvarme On-tid under dagdrift|o39<br>o41|1|1<br>1|1<br>1<br>1<br>|1|1||1<br>1|1|1<br>1|1<br>1|0/Off<br>0 %|1/On<br>100 %|0/Off<br>100||
|Kantvarme On-tid under natdrift|o42||1|1<br>1<br>|1|||1||1|1|0 %|100 %|100||
|Kantvarmeperiodetid(On tid + Off tid)|o43||1|1<br>1<br>|1|||1||1|1|6 min.|60 min.|10||
|Møbelrengøring: 0= ingen møbelrengørring 1= kun<br>ventilatorer. 2 Alle udgange er OFF<br>*|**<br>o46|1|1|1<br>1<br>|1|1||1|1|1|1|0|2|0||
|<br>Valgaf EL-diagram. Se oversigten side 12 og13<br>*|o61|1|1|1<br>1<br>|1|1||1|1|1|1|1|10|1||
|Overfør et sæt af forudindstillinger. Se oversigten på<br>side 27<br>*|o62|1|1|1<br>1<br>|1|1||1|1|1|1|0|6|0||
|<br>Adgangskode 2(delvis adgang)<br>*|**<br>o64|1|1|1<br>1<br>|1|1||1|1|1|1|0|100|0||
|Overskriv regulatorens fabriksindstillinger med de<br>nuværende indstilliner|o67|1|1|1<br>1<br>|1|1||1|1|1|1|0/Off|1/On|0/Off||
|g <br>Indgangssignal på DI3. Funktion:  (high voltage input)<br>(0=ikke anvendt, 1=status på DI3. 2=dørfunktion<br>med alarm ved åben. 3=døralarm ved åben.<br>4=afrimningsstart (pulstryk).  5=ekstern<br>hovedafbryder. 6=natdrift. 7=termostat bånd skift<br>(r21 aktiveres). 8=Benyttes ikke. 9=Benyttes ikke.<br>10=møbelrengøring (pulstryk). 11=Tvangskøling ved<br>varmasafrimnin 12=natafdæknin 13=Benttes|o84|1|1|1<br>1<br>|1|1||1|1|1|1|0|14|0||
|gg. g. y<br>ikke. 14=Kølingen stoppes(forced closing))||||||||||||||||
|Kantvarmestyring<br>|o85||1|1<br>1<br>|1|||1||1|1|0|2|0||
|0=anvendes ikke, 1=pulsstyring med timerfunktion<br>(o41 ogo42),2=pulsstyringmed dugpunktsfunktion||||||||||||||||
|Dugpunktsværdi hvor kantvarmen er minimum|o86||1|1<br>1<br>|1|||1||1|1|-10°C|50°C|8||
|Dugpunktsværdi hvor kantvarmen er 100% on|o87||1|1<br>1<br>|1|||1||1|1|-9°C|50°C|17||
|Lavest tilladelige kantvarmeeffekt i %<br>|o88<br>||1<br>|1<br>1<br><br><br><br>|1<br>|||1<br>||1<br>|1<br>|0 %<br>|100 %<br>|30<br>||
|Tidsforsinkelse fra "åben dør" til kølingen startes|o89|1|1|1<br>1<br>|1|||1|1|1|1|0 min.|240 min.|30||
|Ventilatordrift ved stoppet køling (forced closing):<br>no/0=Fan Offyes/1=Fan On|o90|1|1|1<br>1<br>|1|1||1|1|1|1|0/no|1/yes|1/yes||
|f,  <br>Definition af udlæsning på nederste knap:|o92|1|1|1<br>1<br>|1|1||1|1|1|1|1|3|1||
|1=afrimningsstoptemperatur,  2=S6 temperatur,<br>3S5B tt||||||||||||||||
|=_emperaur<br>Temperaturvisning i display<br>1= u56 lufttemeratur|o97|1|1|1<br>1<br>|1|1||1|1|1|1|1|2|1||
|p<br>2= u36produkttemperatur||||||||||||||||
|Lys og natgardin definition<br>0: Lys er slukket og natgardin er åben, når<br>hovedafbryder er off|o98|1|1|1<br>1<br>|1|1||1|1|1|1|0|1|0||
|f<br>1: Lys ognatgardin er uafhængigaf hovedafbryder||||||||||||||||
|<br>Konfiguration af alarmrelæet|P41|1||1<br>1|||||1||1|0|127|111||
|Alarmrelæet vil blive aktiveret ved en alarm i en af de<br>følgende grupper:<br>1 - Højtemperaturalarmer<br>2 - Lavtemperaturalarmer<br>4 - Følerfejl<br>8 - Digital indgang aktiveres til alarm<br>16 - Afrimningsalarmer<br>32 - Diverse<br>64 - Indsprøjtningsalarmer<br>Hvilke grupper, der skal aktivere alarmrelæet, skal<br>indstilles med en talværdi, der er summen af de<br>grupper, der skal aktiveres.<br>(Fx: en værdi på 5 vil aktivere alle<br>højtemperaturalarmer og alle følerfejl. 0 vil aflyse<br>relæfunktionen)||||||||||||||||

30

|**Fortsat**|**Kode**|**1**<br>**2**|**3**<br>**4**<br>|**5**<br>**6**|**7**<br>**8**|**9**<br>**10**|**Min.**|**Max.**|**Fab.**|**Aktuel**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Service**|||||||||||
|Temperaturen målt med S5 føleren|u09|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Statuspå DI1 indgangen. 1=sluttet|u10|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Aktuel afrimningstid(minutter)|u11|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Temperaturen målt med S3 føleren|u12|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Statuspå natdrift(on eller off)1=sluttet|u13|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Temperaturen målt med S4 føleren|u16|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Termostattemperaturen|u17|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Termostatens igangværende køretid (cooling time) i|u18|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|minutter|||||||||||
|Temperatur ved fordamper indgang|u19|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Temperatur ved fordamper udgang|u20|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Overhedningover fordamperen|u21|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Reference for overhedning|u22|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|AKV ventilens åbningsgrad|**<br>u23|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Fordampningstryk Po(relative)|u25|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Fordamper temperatur To(beregnet)|u26|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Temperaturen målt med S6 føleren|u36|1<br>1|1<br>1<br>|1<br>1|1<br>1|1|||||
|(produkttemperatur)|||||||||||
|Statuspå DI2 udgangen. 1=sluttet|u37|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Lufttemperatur. Vægtet S3 ogS4|u56|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Målt temperatur til alarmtermostaten|u57|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Statuspå relæet til køling|**<br>u58|1<br>1|1<br>|1|||||||
|Statuspå relæet tll ventilator|**<br>u59|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Statuspå relæet til afrimning|**<br>u60|1<br>1|1<br>1<br>|1|1<br>1|1<br>1|||||
|Statuspå relæet til kantvarme|**<br>u61|1|1<br>1<br>|1|1|1<br>1|||||
|Statuspå relæet til alarm|**<br>u62|1|1<br>1||1|1|||||
|Statuspå relæet til lys|**<br>u63|1<br>1|1|1|1<br>1|1<br>1|||||
|Statuspå relæet til ventil i sugeledningen|**<br>u64|||1|||||||
|Status på relæet til kompressor 2|**<br>u67|||1|||||||
|Temperaturen målt med S5B føleren|u75|||||1|||||
|Statuspå relæet til varmgas-/drænventil|**<br>u80|||1|||||||
|Statuspå relæet til varmelegeme i drypbakke|**<br>u81|||1|||||||
|Statuspå relæet til natgardin|**<br>u82||||1||||||
|Statuspå relæet til afrimningB|**<br>u83|||||1|||||
|Statuspå relæet til varmefunktionen|**<br>u84||||1||||||
|Udlæsningaf den aktuelle kantvarmeeffekt|u85|1|1<br>1<br>|1|1|1<br>1|||||
|1: Termostat 1 i drift,2: Termostat 2 i drift|u86|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Statuspå højvoltsindgangen DI3|u87|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Udlæsningaf termostatens aktuelle indkoblingsværdi|u90|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Udlæsningaf termostatens aktuelle udkoblingsværdi|u91|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|Udlæsning af status på den adaptive afrimning|U01|1<br>1|1<br>1<br>|1<br>1|1<br>1|1<br>1|||||
|<br>0: Off. Funktionen er ikke aktiveret<br>1: Fejl. Der skal gennemføres en reset med d22<br>2: Reset er aktiveret. Ny tuning er igang<br>3: Normal<br>4: Let is-opbygning<br>5: Medium is-opbygning|||||||||||
|<br>6: Kraftigis-opbygning|||||||||||

*) Kan kun indstilles, når reguleringen er stoppet (r12=0)

**)  Kan styres manuelt, men kun når r12 = -1

***) Med adgangskode 2 begrænses adgangen til disse menuer

Fabriksindstilling

Hvis du får behov for at vende tilbage til de fabriksindstillde værdier, kan det ske således:

- Afbryd forsyningsspændingen til regulatoren

- Hold den øverste og nederste knap inde samtidig med at du igen tilslutter forsyningsspændingen.

31

### **Tilslutninger**

*[Figurtekst: Oversigt over udgange og  Application DO1 DO2 DO3 DO4 DO5 DO6 DI1 DI2 DI3 AI1 AI2 AI3 AI4 AI5 AI6 · anvendelser. · 1 • • • P0/S1 S2 S3 S4 S5 S6 · Se også el-diagrammerne tidligere  2 • • • P0/S1 S2 S3 S4 S5 S6 · i manualen · 3 • • • P0/S1 S2 S3 S4 S5 S6 · 4 • • • P0/S1 S2 S3 S4 S5 S6 · 5 • • • P0/S1 S2 S3 S4 S5 S6 · 6 suction hotgas • • • P0/S1 S2 S3 S4 S5 S6 · 7 Blinds • • • P0/S1 S2 S3 S4 S5 S6 · 8 heat • • • P0/S1 S2 S3 S4 S5 S6 · 9 2 1 • • • P0/S1 S2 S3 S4 S5 S5B · 10 • • • P0/S1 S2 S3 S4 S5 S3B]*

##### **DI1**

Digitalt indgangssignal. Den definerede funktion er aktiv, når indgangen kortsluttes / åbnes. Funktionen defineres i o02.

##### **EKA Display**

Hvis der skal være ekstern aflæsning / betjening af regulatoren, kan der tilsluttes et display type EKA 163B eller EKA 164B.

##### **DI2**

Digitalt indgangssignal.

Den definerede funktion er aktiv, når indgangen kortsluttes / åbnes. Funktionen defineres i o37.

##### **Tryktransmitter eller temperaturføler S1**

Pe / AKS 32R (trykmåling anbefales)

   - Forbindes til terminal 30, 31 og 32. (Anvendes kabel 060G1034: Sort=30, Blå=31, Brun=32) Signalet fra èn tryktransmitter kan modtages af op til 10 regulatorer. Men kun hvis der ikke er nævneværdige trykfald imellem de fordampere, der skal styres. Se tegning side 34.

- S1 (korrekt placering er vigtig for en korrekt måling) Pt 1000 ohm føler

Forbindes til terminal 31 og 32.

##### **S2**

Pt 1000 ohm føler

##### **S3, S4, S5, S6**

Pt 1000 ohm føler eller PTC 1000 ohm føler. Alle skal være af samme type.

S3, luftføler, placeres i den varme luft før fordamperen

S4, luftføler, placeres i den kolde luft efter fordamperen (behovet for enten S3 eller S4 kan være fravalgt i konfigurationen)

##### **RS485 (terminal 51, 52,53)**

Til datakommunikation, men kun hvis der indsættes et datakommunikationsmodul i regulatoren. Modulet kan være et LON RS485, DANBUSS eller et MODBUS. Terminal 51 = skærm Terminal 52 = A (A+) Terminal 53 = B (B-) (Ved LON RS485 og gateway type AKA 245, skal gatewayen være version 6.20 eller nyere.)

##### **RJ45**

Til datakommunikation, men kun hvis der indsættes et TCP/IPmodul i regulatoren. (OEM specificeret).

##### **MODBUS**

Til datakommunikation. Terminal 56 = skærm Terminal 57 = A+ Terminal 58 = B- (Alternativt kan klemmerne tilsluttes et eksternt display type EKA 163A eller 164A, men så kan de ikke benyttes til datakommunikation. En evt. datakommunikationen skal så foretages på en af de andre måder.)

##### **Forsyningsspænding**

230 V a.c.

- S5, afrimingsføler, placeres på fordamperen

- S6, produktføler eller afrimningsføler B eller luftføler B. Konfigurationen bestemmer hvilken.

32

##### **DO1**

Tilslutning af ekspansionsventil type AKV eller AKVA. Spolen skal være en **230 V a.c. spole** .

##### **DO2**

##### Alarm

Der er forbindelse imellem terminal 7 og 8 i alarmsituationer, og når regulatoren er spændingsløs.

Kantvarme

Der er forbindelse imellem terminal 7 og 9, når der varmes. Natgardin

Der er forbindelse imellem terminal 7 og 9, når natgardinet skal være for.

Sugeledningsventil

Der er forbindelse imellem terminal 7 og 9, når ventilen i sugeledningen skal være åben.

##### **DO6**

Lysrelæ

Der er forbindelse imellem terminal 17 og 18, når lyset skal være tændt.

Kantvarme, Kompressor 2

Der er forbindelse imellem terminal 17 og 19, når funktionen skal være aktiv.

##### **DI3**

Digitalt indgangssignal. Signalet skal være en spænding på 0 /  230 V a.c. Funktionen defineres i o84.

##### **Datakommunikation**

Hvis der anvendes datakommunikation, er det vigtigt, a t installationen af datakommunikationskablet udføres korrekt. Se separat litteratur nr. RC8AC...

##### **DO3**

Køling, Kantvarme, Varmefunktion, Afrimning 2

Der er forbindelse imellem terminal 10 og 11, når funktionen skal være aktiv.

Varmelegeme i drypbakke

Der er forbindelse imellem terminal 10 og 11, når der varmes.

##### **Elektrisk støj**

Kabler til følere, DI indgange og datakommunikation **skal** holdes adskilt fra andre elkabler:

- Benyt separate kabelbakker

- Hold afstand imellem kabler på mindst 10 cm

- Lange kabler på DI-indgangen skal undgås.

##### **DO4**

##### Afrimning

Der er forbindelse imellem terminal 12 og 14, når der afrimes. Varmgas / drænventil

Der er forbindelse imellem terminal 13 og 14 under normaldrift. Der er forbindelse imellem terminal 12 og 14, når varmgasventilen skal åbne.

##### **DO5**

##### Ventilator

Der er forbindelse imellem terminal 15 og 16, når ventilatoren er igang.

##### **Installationshensyn**

Utilsigtet påvirkning kan medføre funktionssvigt af føler, regulator, ventil eller datakommunikation med deraf følgende driftsfejl på køleanlægget. Fx temperaturstigning eller væskegennemløb i fordamperen.

Danfoss påtager sig ikke ansvar for varer og dele i installationer, der beskadiges som følge af ovenstående fejl. Ved installation påhviler det installatøren at foretage de nødvendige sikringer mod ovenstående fejl. Specielt henvises til nødvendigheden af signal til regulatoren, når kompressorer bliver stoppet, og til nødvendigheden af væskeopsamlere før kompressorerne.

Koordineret afrimning via ledningsforbindelser

Følgende regulatorer kan kobles sammen på denne måde: EKC 204A, AK-CC 210, AK-CC 250, AK-CC 450, AK-CC 550

Kølingen genoptages, når alle regulatorer har "frigivet" signalet om afrimning.

Koordineret afrimning via datakommunikation

Opsætningen af hvilke regulatorer der skal koordinere deres afrimning foretages i gatewayen/system manageren.

Kølingen genoptages, når alle regulatorer har "frigivet" signalet om afrimning.

33

### **Data**

*[Figurtekst: Fors y nin g 230 V a.c. +10/-15 %. 5 VA ,  50/60 Hz · Føler S2, (S1) Pt 1000 · Pt 1000 eller · Føler S3, S4, · PTC 1000 ohm · S5, S6 · ( Alle 4 skal være af samme t yp e ) · Måleområde -60 til +120°C · ±1 K under -35°C · Regulator  ± 0,5 K imellem -35 til +25°C; · Nøjagtighed · ±1 K over +25°C · ±0,3 K ved 0°C · Pt 1000 føler · ±0 , 005 K  p er  g rad · Målin g  af Pe Tr y ktransmitter AKS 32R · Dis p la y LED, 3 cifre · Eksternt dis p la y EKA 163B eller 164B. (Evt. EKA 163A eller 164A) · Signal fra kontaktfunktioner. · Digitale ind- Krav til kontakter: Guldbelægning. · gange DI1, DI2 Kabellængden må max. være 15 m. · Ben y t h j æl p erelæer ,  når afstanden er læn g ere. · Digital indgang · 230 V a.c. · DI3 · El-tilslutnings- · Max.1,5 mm 2  flerlederkabel · kabel · Max. 240 V a.c. , Min. 28 V a.c. · DO1 Max. 0,5 A · Solid state · (Til AKV spole) Læk < 1 mA · udgang · Max. 1 stk. AKV (2 stk. hvis der · anvendes EEC s p oler ) · CE · (250 V a.c.) · Relæer* DO3, DO4 4 (3) A · DO2, DO5, DO6 4 (3) A · 0 - 55°C, under drift · -40 - 70°C, under trans p ort · Omgivelser · 20 - 80% Rh ,  ikke kondenserende · Ikke chok p åvirknin g er / vibrationer · Tætheds g rad IP 20 · Monta g e På DIN-skinne eller  p å væ g · Væ g t 0,4 K g · Fast  MODBUS · LON RS485 · DANBUSS · Datakommuni- Udvidelsesmulighed · TCP/IP · kation · MODBUS · Regulatoren kan ikke kobles op sammen med en · overvå g nin g senhed t yp e m2. · Gangreserve til · 4 timer · uret · EU lavspændingsdirektiv og EMC krav til CE-mærk- · Godkendelser · ning er opfyldt. · LVD-testet iht. EN 60730-1 og EN 60730-2-9, A1, A2 · EMC-testet iht. EN50082-1 o g  EN 60730-2-9, A2]*

*  DO3 og DO4 er 16 A relæer. DO2, DO5 og DO6 er 8 A relæer. Max. belastning skal overholdes.

*[Figurtekst: AKV info !! · 230 V a.c. spole]*

###### **Kapacitiv belastning**

Relæerne er ikke anvendelige til direkte kobling af kapacitive belastninger så som LED og on/off styring af EC motorer.

Alle belastninger med en switch mode strømforsyning skal kobles med en dertil egnet kontaktor eller lignende.

*[Figurtekst: Signalet fra èn tryktransmitter kan modtages af op til · 10 regulatorer.]*

34

### **Bestilling**

|**Type**|**Funktion**|**Bestilling**|
|---|---|---|
|AK-CC 550|Kølemøbelstyring med MODBUS datakommunikation<br>Følertilslutninger er med skrueklemmer|**084B8020**|
|EKA 175|Datakommunikationsmodul LON RS 485|**084B8579**|
|EKA 178B|Datakommunikationsmodul MODBUS|**084B8571**|
|EKA 176|Datakommunikationsmodul DANBUSS + gateway|**084B8583**|
|EKA 176A|Datakommunikationsmodul DANBUSS + AK-PI 200|**084B8591**|
|EKA 163B|Eksternt display med stik til direkte tilslutning|**084B8574**|
|EKA 164B|Eksternt display med betjeningsknapper og stik  til direkte<br>tilslutning|**084B8575**|
|EKA 163A|Eksternt display med skrueklemmer|**084B8562**|
|EKA 164A|Eksternt display med betjeningsknapper og skrueklemmer|**084B8563**|

##### **Eksempler på bestilling**

|**Installation**|**Datakommunikation**|**Tilslutning**|**Bestilling**|
|---|---|---|---|
||MODBUS<br>LON||084B8020 (AK-CC 550)<br>084B8020<br>084B8579|
||DANBUSS||084B8020<br>084B8583|
||MODBUS||084B8020<br>084B8574 (display)<br>084B7299 (kabel, 6 m)|
|L|LON / DANBUSS||084B8020<br>084B8574 (display)<br>084B7299 (kabel, 6 m)<br>084Bxxxx (data-modul)|
|L < 15 m||||
|L > 15 m<br>L|MODBUS / LON / DANBUSS||084B8020<br>084B8562 (display)<br>084Bxxxx (data-modul)|

35

Danfoss påtager sig intet ansvar for mulige fejl i kataloger, brochurer og andet trykt materiale. Danfoss forbeholder sig ret til uden forudgående varsel at foretage ændringer i sine produkter, herunder i produkter, som allerede er i ordre, såfremt dette kan ske uden at ændre allerede aftalte specifikationer.

Alle varemærker i dette materiale tilhører de respektive virksomheder. Danfoss og Danfoss-logoet er varemærker tilhørende Danfoss A/S. Alle rettigheder forbeholdes.

36
