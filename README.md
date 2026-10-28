# Køleteknik – manualer til CO2-fejlfindingsassistenten

Manualer til køleregulatorer (Danfoss, Dixell, Carel) konverteret til Markdown til brug i Claude-projektet "Køleteknikker".

## Danfoss

| Mappe | Controller | Bemærkning |
|---|---|---|
| `danfoss/ak-pc-782a/` | AK-PC 782A (pack-controller, transkritisk CO2) | User Guide SW 4.3x + heat recovery-strategi + deling af tryktransmitter |
| `danfoss/ak-pc-772a/` | AK-PC 772A (pack-controller, transkritisk CO2, mindre anlæg) | User Guide |
| `danfoss/ak-pc-781/` | AK-PC 781 (pack-controller med varmegenvinding) | User Guide 2013. Ikke specifikt 781A |
| `danfoss/ak-pc-651a/` | AK-PC 651A (pack-controller, én sugegruppe) | User Guide |
| `danfoss/ak-pc-551/` | AK-PC 551 (pack-controller, to sugegrupper) | User Guide SW 1.7 |
| `danfoss/ak-pc-530/` | AK-PC 530 (pack-controller) | Kun instruktionsark (2010) |
| `danfoss/ak-pc-351/` | AK-PC 351 (pack-controller, op til 4 kompressorer) | Kun engelsk instruktionsark + datablad. Fuld user guide findes kun på RU/FR |
| `danfoss/ak-sm-800a/` | AK-SM 820A/850A/880A (system manager) | User Guide, Data sheet, Installation Guide |
| `danfoss/ak-sm-800/` | AK-SM 800 (gammel model) | Quick Setup Guide – ikke det samme som 800A |
| `danfoss/ak-cc55/` | AK-CC55 Single Coil / Single Coil UI | SW 1.7x |
| `danfoss/ak-cc55-compact/` | AK-CC55 Compact | User Guide SW 2.1x |
| `danfoss/ak-cc55-multi-coil/` | AK-CC55 Multi Coil | User Guide SW 1.9x |
| `danfoss/ak-cc-750a/` | AK-CC 750A (fordamperregulator) | User Guide |
| `danfoss/ak-cc-550/` | AK-CC 550 (ældre møbelcontroller) | Dansk. Andre alarmkoder end AK-CC55 |
| `danfoss/ak-cc-450/` | AK-CC 450 | Kun instruktionsark (2013) |
| `danfoss/ak-cc-250a/` | AK-CC 250A | Kun instruktionsark (2015) |
| `danfoss/ak-cc-210/` | AK-CC 210 | User Guide (2018) |
| `danfoss/ekc-202/` | EKC 202A/B/C | Kun instruktionsark |
| `danfoss/erc-21x/` | ERC 211 / 213 / 214 (plug-in møbler) | User Guide |
| `danfoss/eke-1/` | EKE 1A/1B/1C/1D (overhedningsregulator) | User Guide + datablad. Afløser for EKC 315A/316A |
| `danfoss/ekc-315a/` | EKC 315A (overhedningsregulator, udgået) | Kun instruktionsark |
| `danfoss/optyma-plus/` | Optyma Plus (styring i kondenseringsaggregat) | User Guide SW 3.7x |
| `danfoss/optyma-control-ak-rc-101/` | Optyma Control AK-RC 101 (kølerumsstyring, 1-faset) | User Guide |

## Dixell

| Mappe | Controller | Bemærkning |
|---|---|---|
| `dixell/xr20cx/` | XR20CX (off-cycle afrimning) | |
| `dixell/xr30cx/` | XR30CX (off-cycle afrimning + AUX-relæ) | |
| `dixell/xr60cx/` | XR60CX (møbel/rum-controller) | r1.1, 2015 |
| `dixell/xr70cx/` | XR70CX (afrimning, ventilator, alarmrelæ) | r1.3, 2015 |
| `dixell/xr75cx/` | XR75CX (4 relæer) | r1.0, 2015 |
| `dixell/xw60k/` | XW60K (kølerum, separat tastatur T620/V620) | |
| `dixell/xw264k/` | XW264K (kølerum, 6 relæer) | |

## Carel

| Mappe | Controller | Bemærkning |
|---|---|---|
| `carel/easy/` | easy / easy compact / easy split | User manual rel. 3.4 (2021) |
| `carel/ir33/` | ir33-platformen (ir33, power, DIN, powercompact, mastercella) | Kun tilslutningsmanual (el-diagrammer), ikke parameterliste |

## Andet

- `vejledning/VEJLEDNING-PDF-til-MD.md` – vejledning til Claude i at lave nye MD-filer af PDF-manualer. Den er ikke en manual og skal ikke uploades til projektet.

Mangler: UltraCella, Dixell XR02CX/XR06CX, Carel ir33 parameterliste, fuld EKC 202-manual.
