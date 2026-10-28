# Danfoss EKC 315A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## Instructions – RI8GT652 12-2009

*Kilde: Danfoss-dokument AN12368642832001-000601.pdf*

### **Instructions**

*[Figurtekst: Identifikation Mål · Identification Dimensions · Maße · Dimensions · 084B7086 · Princip · Principle · Montageprinzip · Principe]*

RI8GT652  12-2009

*[Figurtekst: ICAD skal forsynes fra ek- · stern kilde med 24 V d.c. · ICAD must be supplied · Data kommunikation with 24 V DC from an · Data communication external source. · Datenkommunikation · Communication des données Das ICAD muss von einer · externen Quelle mit 24 · V Gleichstrom versorgt · werden. · ICAD doit être alimenté · par une source externe de · 24 V c.c.]*

*[Figurtekst: !! U77-78: 24 V +/-10% !! · Kabel fx, Cable ex., Kabel z.B., câble fx · L < 25 m   :  0.75 mm 2 · 25 m < L < 75 m   :  1.5 mm 2 · 75 m < L   :  2.5 mm 2]*

##### **Tilslutninger**

###### **DANSK**

##### **Connections**

###### **ENGLISH**

- **Nødvendige tilslutninger** Klemme: 25-26 Forsyningsspænding 24 V a.c.

- 17-18 Kun ved TQ aktuator: Signal fra aktuator

- 20-21 Pt 1000 føler ved fordamperafgang (S2)

- 14-15 Tryktransmitter type AKS 33

- 9-10 Relækontakt til start/stop af magnetventil

- 1-2 Kontaktfunktion til start/stop af reguleringen. Hvis der ikke tilsluttes en kontakt, skal klemme 1 og 2 kortsluttes.

- **Applicationbestemte tilslutninger** Klemme: 21-22 Pt 1000 føler til måling af lufttemperatur (S3) 12-13  Alarmrelæet Der er forbindelse imellem 12 og 13 i alarmsituationer, og når regulatoren er spændingsløs

- 18-19 Strømsignal fra anden regulering (Ext.Ref.)

- 23-24 Spænding til aktuator AKV/TQ

- 2-5 Strømudgang til visning af overhedning eller lufttemperatur. Eller til signal til et slavemodul. Eller styring af ICM ventil.

- 3-4 Datakommunikation

   - Monteres kun, hvis der også er monteret et datakommunikationsmodul.

Det e r vigtigt, a t installationen af datakommunikationskablet udføres korrekt. Se separat litteratur nr. RC8AC...

**Necessary connections** Terminals:

- 25-26 Supply voltage 24 V a.c.

- 17-18 Only at TQ actuator: Signal from actuator

- 20-21 Pt 1000 sensor at evaporator outlet (S2)

- 14-15 Pressure transmitter type AKS 33

- 9-10 Relay switch for start/stop of solenoid valve

- 1-2 Switch function for start/stop of regulation. If a switch is not connected, terminals 1 and 2 must be shortcircuited.

**Application dependent connections** Terminal:

21-22 Pt 1000 sensor for measuring air temperature (S3) 12-13  Alarm relay There is connection between 12 and 13 in alarm

   - situa tions and when the controller is dead

- 18-19 Current signal from other regulation (Ext.Ref.) 23-24 Supply to actuator AKV/TQ

- 2-5 Current output for showing superheat or air temperature. Or for signal to a slave module. Or control of ICM valve.

- 3-4 Data communication Mount only, if a data communication module has been mounted.

   - It i s important t hat the installation of the data communication cable be done correctly. Cf. separate literature No. RC8AC...

2

###### **DEUTSCH**

##### **Anschlüsse**

###### **Benötigte Anschlüsse**

###### Klemme

- 25-26 Versorgungsspannung 24 V a.c.

- 17-18 Nur am TQ Stellantrieb: Signal vom Stellantrieb

- 20-21 Pt 1000 Fühler am Verdampferausgang (S2)

- 14-15 Druckmessumformer Typ AKS 33

- 9-10 Relaiskontakt für start/stop der Magnetventile

- 1-2 Kontaktfunktion für start/stop der Regelung. Wenn kein Kontakt angeschlossen wird, muss Klemme 1 und 2 kurzgeschlossen werden.

###### **Anwendungsbestimmte Anschlüsse** Klemme:

- 21-22 Pt 1000 Fühler für messung der Lufttemperatur (S3) 12-13  Alarmrelais

   - Es besteht Verbindung zwischen 12 und 13 in Alarm

   - situationen, und wenn der Regler Span nungslos ist.

- 18-19 Spannungssignal von einer anderen Regelung (Ext.Ref.)

- 23-24 Spannung an das Stellantrieb AKV/TQ

- 2-5 Spannungsausgang zur anzeige der Überhitzung oder die Lufttemperatur. Oder an Signal zu einem Slavenmodul. Oder regelung von ICM Ventil.

- 3-4 Datenkommunikation Nur bei montiertem Datenkommunikationsmodul anzuschließen.

Bitt e beachten, dass die Installation des Datenkommunikationskabels korrekt vorgenommen wird. Siehe separate Literatur Nr. RC8AC...

###### **FRANCAIS**

##### **Raccordements**

###### **Raccordements nécessaires**

###### Bornes :

25-26 Tension d’alimentation 24 V c.a.

- 17-18 Actuateur TQ seulement : Signal provenant de l’actuateur

- 20-21 Sonde Pt 1000 à la sortie de l’évaporateur (S2)

- 14-15 Transmetteur de pression type AKS 33

- 9-10 Relais de marche/arrêt des électrovannes

- 1-2 Contact pour marche/arrêt de la régulation.  Si aucun contact n’est raccordé, il faut court-circuiter les bornes 1 et 2.

###### **Raccordements selon les applications**

###### Bornes :

- 21-22 Capteur Pt 1000 pour relever la température de l’air (S3)

- 12-13  Relais d’alarme

   - Il y a liaison entre 12 et 13 en cas d’alarme et si le régulateur est hors tension.

- 18-19 Signal de courant d’une autre régulation (Ext.Ref.)

- 23-24 Tension vers l’actuateur AKV/TQ

- 2-5 Sortie de courant pour affichage de surchauffe ou de température d’air. Ou pour signal vers un module esclave. Ou commande du robinet ICM.

3-4 Transmission de données Ne faire ce raccordement qu’après installation du module de transmission de données. Il est très important que l’installation du câble de transmission soit effectuée correctement. Se reporter au document spécifique RC8AC.

3

**DANSK**

##### **Betjening**

###### **Display**

Værdierne bliver vist med tre cifre, og med en indstilling kan du bestemme, om temperaturen skal vises i °C eller i °F.

###### **Lysdioder på fronten**

Der er lysdioder på fronten, som vil lyse, når den tilhørende funktion er aktiveret.

Den øverste lysdiode vil angive ventilens åbningsgrad. Kort puls angiver et lille væskeflow og lang puls et stort væskeflow. Den næste lysdiode vil angive, når regulatoren kalder på køling. De tre nederste lysdioder vil blinke, hvis der er en fejl i reguleringen.

I denne situation kan du kalde fejlkoden frem på displayet og udkoble alarmen ved at trykke kortvarigt på den øverste knap.

###### **Knapperne**

Når du vil ændre en indstilling, vil de to knapper give en højere eller en lavere værdi alt efter hvilken knap, du trykker på. Men før du kan ændre værdien, skal du have adgang ind i menuen. Det får du ved at trykke på den øverste knap i et par sekunder – så kommer du ind i rækken med parameterkoder. Find den parameterkode du vil ændre, og tryk så på begge knapper samtidig. Når du har ændret værdien, gemmer du den nye værdi ved igen at trykke på begge knapper samtidig. Eller kort:

Giver adgang til menuen (eller udkoble en alarm)

Giver adgang til at ændre

- Gemmer en ændring.

###### **Eksempler på betjening**

###### Indstille setpunkt

1. Tryk på begge knapper samtidig

2. Tryk på en af knapperne og vælg den nye værdi

3. Tryk igen på begge knapper for at afslutte indstillingen.

###### Indstille en af de øvrige menuer

1. Tryk på den øverste knap til der vises en parameter

2. Tryk på en af knapperne og find hen til den parameter, du vil indstille

3. Tryk på begge knapper samtidig indtil værdien for parameteren vises

4. Tryk på en af knapperne og vælg den nye værdi

5. Tryk igen på begge knapper for at afslutte indstillingen.

Fabriksindstilling

##### **Menuoversigt**

||**Para-**||SW =1|.3x<br>**Fabind-**|
|---|---|---|---|---|
|**Funktion**|**meter **|<sup>**Min.**</sup>|**Max.**|**.**<br>**stilling**|
|**Normalbillede**|||||
|Viser den aktuelle overhedning / åbningsgrad<br>|||||
|/ temp.<br>Visningen defineres i o17<br>|-||K||
|Temperatur, overhedning eller temp. referencen<br>|||||
|vises ved kortvarigt tryk på den nederste knap.<br>Visningen defineres i o17|-||%||
|i <br>**Reference**|||||
|Indstil det ønskede setpunkt|-|-60°C|50°C|10|
|Differens|r01|0,1 K|20,0 K|2.0|
|Enheder (0=°C+bar /1=°F+psig)|r05|0|1|0|
|Eksternt bidrag til referencen|r06|-50 K|50 K|0|
|Korrektion af signalet fra S2|r09|-10.0 K|10.0 K|0.0|
|Korrektion af signalet fra S3|r10|-10.0 K|10.0 K|0.0|
|Start / stop af kølingen<br>i|r12|OFF|On|1|
|Termostatfunktionen defineres<br>(0= ingen termostatfunktion, 1=On/off-termo-<br>|r14|0|1|0|
|stat)<br>**Alarm**|||||
|Øvre afvigelse (over temperaturindstillingen)|A01|3.0 K|20 K|5.0|
|Nedre afvigelse (under temperaturindstillingen)|A02|1 K|10 K|3.0|
|Alarmforsinkelse|A03|0 min.|90 min.|30|
|**Reguleringsparametre**|||||
|P: Forstærkningsfaktor Kp|n04|0.5|20|3.0|
|I: Integrationstid Tn|n05|30 s|600 s|120|
|D: Differentiationstid Td (0 = off)|n06|0 s|90 s|0|
|Max. værdi for overhedningsreferencen|n09|2 K|50 K|6|
|Min. værdi for overhedningsreferencen|n10|1 K|12 K|4|
|MOP (max. = off)|n11|0.0 bar|60 bar|60|
|Periodetid (kun hvis der anvendes AKV/A-ventil)|n13|3 s|10 s|6|
|Stabilitetsfaktor for regulering af overhednin-|||||
|gen.<br>Bør kun ændres af instrueret personale|n18|0|10|5|
|Dæmpning af forstærkningen omkring refer-<br>encen.<br>Bør kun ændres af instrueret personale|n19|0.2|1.0|0.3|
|Forstærkningsfaktor for overhedningen.<br>Bør kun ændres af instrueret personale|n20|0.0|10.0|0.4|
|Definition af overhedningsreguleringen.<br>1=MSS, 2=LOADAP|n21|1|2|1|
|Værdi for min. overhedningsreference ved<br>belastninger under 10%|n22|1|15|2|
|<br>Standbytemperatur ved lukket ventil (kun ved<br>TQ-ventil).<br>Bør kun ændres af instrueret personale|n26|0 K|20 K|0|
|<br>Standbytemperatur ved åben ventil (kun ved<br>TQ-ventil).<br>Bør kun ændres af instrueret personale|n27|-15 K|70 K|20|
|Max. åbningsgrad.<br>Bør kun ændres af instrueret personale|n32|0|100|100|
|<br>Min. åbningsgrad<br>Bør kun ændres af instrueret personale|n33|0|100|0|
|<br>**Diverse**|||||
|Regulatorens adresse|o03*|0|119|-|
|On/off omskifter (service-pin meddelelse)|o04*|-|-|-|
|Definér ventil og udgangssignal:<br>f|||||
|0: Off<br>1: TQ. AO: 0-20 mA<br>2: TQ. AO: 4-20 mA<br>3: AKV, AO: 0-20 m|o09|0|7|0|
|4: AKV, AO: 4-20 mA<br>5: AKV, AO: EKC 347-SLAVE<br>|||||
|6: ICM, AO: 0-20 mA/ICM OD%<br>7: ICM AO: 4-20 mA/ICM OD%|||||

Hvis du får behov for at vende tilbage til de fabriksindstillede værdier, kan det ske således:

> - Afbryd forsyningsspændingen til regulatoren

> - Hold begge knapper inde samtidig med at du igen tilslutter forsyningsspændingen.

4

|Definér indgangssignalet på den analoge<br>indgang AIA:|||||**Start af regulatoren**|
|---|---|---|---|---|---|
|<br>0: Ikke noget signal||||||
|,<br>1: Temperatursetpunkt. 0-20 mA<br>2: Temperatursetpunkt. 4-20 mA<br>|<br>o10|0|4|0|Når el-tilslutningen til regulatoren er foretaget, skal de følgende<br>kt ft id li  i|
|3: Forskydning af overhedningsreferencen. 0-20<br>mA|||||puner oreages, nen reguerngen er  gang:<br>1. Afbryd den eksterne kontakt, der starter og stopper|
|4: Forskydning af overhedningsreferencen. 4-20<br>A|||||<br>reguleringen.<br>|
|m<br>Indstil forsyningsspændingens frekvens|o12|50 Hz|60 Hz|0|2. Følg menuoversigten og indstil de forskellige parametre til de<br>ønskede værdier|
|Vælg displayvisningen til "normalbilledet"<br>(Vd ktit tk å d dt k i|||||.<br>3. Slut den eksterne kontakt, og reguleringen bliver startet.|
|e orvarg ry p en neerse nap vses<br>det, der er angivet i parentesen)<br>1: Overhedning (Temperatur)<br>2: Ventilens åbningsgrad (Overhedning)|o17|1|3|1|4. Følg den aktuelle rumtemperatur eller overhedning på displayet<br>(På klemme 2 og 5 kan der afgives et strømsignal,<br>der repræsenterer displayvisningen. Tilslut evt. et|
|3: Lufttemperaturen (Temperatur reference)<br>Manuel styring af udgange:|||||<br>dataopsamlingsudstyr så temperaturforløbet kan følges.)|
|<br>OFF: Ingen manuel styring<br>||f||f||
|1: Relæet til magnetventilen vælges ON<br>2: AKV/A udgangen vælges ON|o18|off|3|Off|**Hvis overhedningen pendler**|
|3: Alarmrelæet aktiveres (brydes)||||||
|Arbejdsområdet for tryktransmitteren - min.<br>værdi|o20|-1 bar|60 bar|-1.0|Når køleanlægget er bragt til at arbejde stabilt, skulle regulatorens|
|Arbejdsområdet for trktransmitteren - max|||||<br>fbikidilld li i d fl ilfld i|
|y  .<br>|o21|-1 bar|60 bar|12|arsnstee reguerngsparametre  e leste tæe gve et<br>|
|værdi<br>(Indstilling til o09 funktionen, kun AKV og TQ)|||||stabilt og relativt hurtigt reguleringssystem.|
|Vælg den temperaturværdi eller åbningsgrad,|27|70°C|160°C|35||
|hvor udgangssignalet skal være minimum (0|o|-||-|Hvis systemet derimod pendler, kan det skyldes at|
|eller 4 mA)<br>(Indstillin til o09 funktionen kun AKV o TQ)|||||overhedningsparametrene er valgt for lave:|
|g   ,   g<br>Vælg den temperaturværdi eller åbningsgrad,<br>hvor udgangssignalet skal være maksimum (20|o28|-70°C|160°C|15|Hvis der er valgt adaptiv overhedning:<br>|
|mA)|||||Juster: n09, n10 og n18.|
|Kølemiddelindstilling<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.|||||Hvis der er valt belastninsdefineret overhednin:|
|6=R13.  7=R13b1.  8=R23.  9=R500.  10=R503.<br>11=R114.  12=R142b. 13=Brugerdefineret.<br>|o30|0|29|0|g gi g<br>Juster: n09, n10 og n22.|
|14=R32. 15=R227.  16=R401A.  17=R507.<br>18=R402A.  19=R404A. 20=R407C.  21=R407A.|||||Alternativt kan det skyldes, at de indstillede reguleringsparametre|
|22=R407B.  23=R410A.  24=R170.  25=R290.<br>26=R600  27=R600a  28=R744  29=R1270|||||ikke er optimale:|
|....<br>**Service**|||||Hvis periodetiden er større end integrationtiden:|
|TQ-ventilens aktuatortemperatur|u04|||°C|<br>(Tp> Tn, (Tner fx 240 sekunder))<br>|
|Referencen for TQ-ventilens aktuatortemperatur|u05|||°C|1. Forøg  Tntil 1,2 x T|
|<br>Analog indgang AIA (18-19)|u06|||mA|p<br>2. Vent til anlægget igen er i balance<br>|
|l|||||3. Hvis der stadig er pendling, reduceres Kpmed fx 20%.|
|Anaog udgang AO (2-5)|u08|||mA|4 Vent til anlægget er i balance|
|Aflæse status på indgangen DI|u10|||on/off|.<br>|
|l<br>Termostatens indkoblingstid|u18|||f<br>min.|5. Ved fortsat pendling gentages 3 og 4.|
|Temperaturen ved S2 føleren|u20|||°C|Hvis periodetiden er mindre end integrationstiden:|
|Overhedningen|u21|||K|(Tp< Tn, (Tner fx 240 sekunder))<br>1 Reducér Kmed fx 20% af skalaværdien|
|Overhedningsreferencen|u22|||K|.p <br>|
|Aflæse ventilens åbningsgrad|u24|||%|2. Vent til anlægget er i balance<br>3 Ved fortsat pendling gentages 1 og 2|
|Aflæse fordampningstrykket|u25|||bar|.       .|
|Aflæse fordampningstemperaturen|u26|||°C||
|Temperaturen ved S3 føleren|u27|||°C|**Hvis overhedningen har for stort undersving**|
|Temperaturreferencen|u28|||°C|<br>**ved opstart**|
|Aflæse signalet på tryktransmitterindgangen|u29|||mA||
|l<br>*) Denne indstilling vil kun være mulig, hvis der<br>|er monte|ret et d|atakommu|nika-|Hvis der reguleres med ventil type AKV:|
|tionsmodul i regulatoren.|||||Juster n22 lidt op og/eller n04 lidt ned|
|**Regulatoren kangive følgende meddelelser:**|||||,    .|
|E1<br>Fejl i regulato|ren||||Hvis der reguleres med ventil type TQ:|
|E11<br>Ventilens akt<br>åd|uatortem|peratu|r er udenfo|r|<br>Juster n26 lidt ned.|
|omret<br>E15<br>Afbrudt S2 fø|ler|||||
|E16<br>Kortsluttet S2|føler|||||
|**Fejlmeddelelse**<br>E17<br>Afbrudt S3 fø|ler|||||
|E18<br>Kortsluttet S3|føler|||||
|E19<br>Indgangssign<br>området|alet på k|lemme|18-19 er u|denfor||
|Indgangssig|alet på k|lemme|14-15 er u|denfor||
|E20<br> <br>området (P0|<br>signalet)|||||
|A1<br><br>Højtemperat<br><br>|uralarm<br>|||||
|**Alarmmeddelelse**<br>A2<br>Lavtemperat<br>A11<br>Der er ikke va|uralarm<br>lgt køle|middel||||

5

**ENGLISH**

##### **Operation**

###### **Display**

The values will be shown with three digits, and with a setting you can determine whether the temperature are to be shown in °C or in °F.

###### **Light-emitting diodes (LED) on front panel**

There are LED’s on the front panel which will light up when the belonging relay is activated.

The upper LED will indicate the valve’s opening degree. A short pulse indicates a small liquid flow and a long pulse a heavy liquid flow. The other LED will indicate when the controller calls for refrigeration.

The three lowermost LED’s will flash, if there is an error in the regulation.

In this situation you can upload the error code on the display and cancel the alarm by giving the uppermost button a brief push.

###### **The buttons**

When you want to change a setting, the two buttons will give you a higher or lower value depending on the button you are pushing. But before you change the value, you must have access to the menu. You obtain this by pushing the upper button for a couple of seconds - you will then enter the column with parameter codes. Find the parameter code you want to change and push the two buttons simultaneously. When you have changed the value, save the new value by once more pushing the two buttons simultaneously.

- Gives access to the menu (or cutout an alarm)

- Gives access to changes

- Saves a change

###### **Examples of operations**

Set set-point

1. Push the two buttons simultaneously

2. Push one of the buttons and select the new value

3. Push both buttons again to conclude the setting

###### Set one of the other menus

1. Push the upper button until a parameter is shown

2. Push one of the buttons and find the parameter you want to change

3. Push both buttons simultaneously until the parameter value is shown

4. Push one of the buttons and select the new value

5. Push both buttons again to conclude the setting

##### **Menu survey**

|**Menu survey**<br>|**Para-**<br>||SW|= 1.3x<br>**Factory**|
|---|---|---|---|---|
|**Function**|**meter **|<sup>**Min.**</sup>|**Max.**|<br>**setting**|
|**Normal display**|||||
|Shows the actual superheat/ valve's opening<br>degree/ temperature|-||K||
|<br>Dfii i 17|||||
|eine vew n o<br>Temperature, superheating, or the temp. reference|||||
|<br>is displayed if the bottom button is pressed briefly.|<br>-||%||
|Define view in o17|||||
|**Reference**|||||
|Set the requirede set point|-|-60°C|50°C|10|
|Differential|r01|0.1 K|20 K|2.0|
|Units (0=°C+bar /1=°F+psig)|r05|0|1|0|
|External contribution to the reference|r06|-50 K|50 K|0|
|Correction of signal from S2|r09|-10.0 K|10.0 K|0.0|
|Correction of signal from S3|r10|-10.0 K|10.0 K|0.0|
|Start / stop of refrigeration<br>i|r12|OFF|On|1|
|Define thermostat function<br>(0=no thermostat function, 1=On/offthermostat)|<sup>r14</sup>|0|1|0|
|**Alarm**|||||
|Upper deviation (above the temperature setting)|A01|3.0 K|20 K|5.0|
|Lower deviation (below the temperature setting)|A02|1 K|10 K|3.0|
|Alarm’s time delay|A03|0 min.|90 min.|30|
|**Regulating parameters**|||||
|P: Amplification factor Kp|n04|0.5|20|3.0|
|I:  Integration time T|n05|30 s|600 s|120|
|D: Differentiation time Td (0 = off)|n06|0 s|90 s|0|
|Max. value of superheat reference|n09|2 K|50 K|6|
|Min. value of superheat reference|n10|1 K|12 K|4|
|MOP (max = off)|n11|0.0 bar|60 bar|60|
|Period time (only when AKV/A valve is used)|n13|3 s|10 s|6|
|Stability factor for superheat control.<br>Changes should only be made by trained staf|n18|0|10|5|
|<br>Damping of amplification around reference value|||||
|i<br>Changes should only be made by trained staf|n19|0.2|1.0|0.3|
|<br>Amplification factor for superheat|n20|00|100|04|
|Changes should only be made by trained staf||.|.|.|
|Definition of superheat control<br>1=MSS, 2=LOADAP|n21|1|2|1|
|Value of min. superheat reference for loads under<br>10%|n22|1|15|2|
|Standby temperature when valve closed (TQ valve<br>only)<br>Chanes should onl be made b trained staf|n26|0 K|20 K|0|
|g  y   y<br>Standby temperature when valve open (TQ valve<br>only)|n27|-15 K|70 K|20|
|Changes should only be made by trained staf<br>|||||
|Max. opening degree|n32|0|100|100|
|Changes should only be made by trained staf|||||
|<br>Min. opening degree<br>Changes should only be made by trained staf|n33|0|100|0|
|<br>**Miscellaneous**|||||
|Controller’s address|o03*|0|119|-|
|ON/OFF switch (service-pin message)|o04*|-|-|-|
|<br>Define valve and output signal:|||||
|0: Off<br>1 T AO 020 A|||||
|: Q. : - m<br>2: TQ. AO: 4-20 mA<br>3: AKV, AO: 0-20 m<br>4: AKV, AO: 4-20 mA|o09|0|7|0|
|5: AKV, AO: EKC 347-SLAVE<br>|||||
|6: ICM, AO: 0-20 mA / ICM OD%<br>7: ICM, AO: 4-20 mA / ICM OD%|||||

> If you need to return to the factory-set values, it can be done in this way:

> - Cut out the supply voltage to the controller

> - Keep both buttons depressed at the same time as you recon nect the supply voltage

Factory setting

6

|Define input signal on the analoge input AIA:<br>0: no signal,||||||
|---|---|---|---|---|---|
|1: Temperature setpoint. 0-20 mA<br>2: Temperature setpoint. 4-20 mA<br>|o10|0|4|0|**Start of controller**|
|3:  Displacement of superheat reference. 0-20 mA<br>4:  Displacement of superheat reference. 4-20 mA|||||When the electric wires have been connected to the controller,<br>|
|Set supply voltage frequency|o12|50 Hz|60 Hz|0|the following points have to be attended to before the regulation<br>|
|Select display for ”normal picture”|||||starts:<br>f|
|<br>(Display the item indicated in parenthesis by<br>briefly pressing the bottom button)|o17|1|3|1|1. Switch off the external ON/OFF switch that starts and stops the<br>regulation.|
|1:  Superheat (Temperature)<br>’|||||2. Follow the menu survey and set the various parameters to the<br>|
|2:  Valves opening degree (Superheat)|||||required values.|
|3:  Air temperature (Temperature reference)<br>|||||3. Switch on the external switch, and regulation will start.|
|Manual control of outputs:<br>OFF: no manual control|||||4. Follow the actual room temperature or superheat on the<br>|
|1:  Relay for solenoid valve: select ON|o18|off|3|Off|display.|
|<br>2:  AKV/A output: select ON||f||f|(On terminals 2 and 5 a current signal can be transmitted|
|3:  Alarm relay activated (cut out)<br>|||||which represents the display view. Connect a data collection|
|Working range for pressure transmitter – min.<br>value<br>|o20|-1 bar|60 bar|-1.0|unit, if applicable, so that the temperature performance can be<br>followed)|
|Working range for pressure transmitter – max.<br>value|o21|-1 bar|60 bar|12|.|
|(Setting for the function o09, only AKV and TQ)<br>Set the temperature value or opening degree<br>where the output signal must be minimum (0 or|o27|-70°C|160°C|-35|**If the superheating fluctuates**|
|4 mA)<br>|||||When the refrigerating system has been made to work steadily,|
|(Setting for the function o09, only AKV and TQ)|||||the controller’s factory-set control parameters should in most|
|Set the temperature value or opening degree<br>where the output signal must be maximum (20<br>mA)|o28|-70°C|160°C|15|<br>cases provide a stable and relatively fast regulating system.<br>If the system however fluctuates this may be due to the fact that<br>|
|Refrigerant setting|||||too low superheat parameters have been selected:|
|<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.||||||
|6=R13.  7=R13b1.  8=R23.  9=R500.  10=R503.<br>i|||||If adaptive superheat has been selected:|
|11=R114.  12=R142b. 13=User defined. 14=R32.<br>15=R227.  16=R401A.  17=R507. 18=R402A.|o30|0|29|0|Adjust: n09, n10 and n18.|
|19=R404A. 20=R407C.  21=R407A.  22=R407B.<br>23=R410A.  24=R170.  25=R290.  26=R600.|||||If load-defined superheat has been selected:<br>|
||||||Adjust: n09 n10 and n22.|
|27=R600a.  28=R744.  29=R1270.|||||,|
|**Service**||||||
|TQ valve's actuator temperature|u04|||°C|Alternatively it may be due to the fact that the set regulation<br>|
|Reference of the valve's actuator temperature|u05|||°C|parameters are not optimal.|
|Analog input AIA (18-19)|u06|||mA|If the time of oscillation is longer than the integration time:|
|Analog output AO (2-5)|u08|||mA|<br>(Tp> Tn, (Tnis, say, 240 seconds))|
|Read status of input DI|u10|||on/off|1. Increase Tnto 1.2 times Tp|
|Thermostat cut-in time|u18|||min.|2. Wait until the system is in balance again|
|Temperature at S2 sensor|u20|||°C|3. If there is still oscillation, reduce Kpby, say, 20%|
|<br>Superheat|u21|||K|4. Wait until the system is in balance<br>5 If it continues to oscillate repeat 3 and 4|
|Superheat reference|u22|||K|.     ,|
|Read AKV valve’s opening degree|u24|||%|If the time of oscillation is shorter than the integration time:|
|Read evaporating pressure|u25|||bar|(Tp< Tn, (Tnis, say, 240 seconds))<br>|
|Read evaporating temperature|u26|||°C|1. Reduce Kpby, say, 20% of the scale reading<br>|
|Tt t S3|27|||°C|2. Wait until the system is in balance|
|emperaure a  sensor|u||||3 If it ti t illt t 1 d 2|
|Temperature reference|u28|||°C|.   connues o oscae, repea  an .|
|Read signal at pressure transmitter input|u29|||mA||
|*) This setting will only be possible if a data comm|unicatio|n modul|e has be|en||

installed in the controller.

###### **If the superheat has excessive underswing during start-up**

|**The controller cangive the following messages:**|
|---|

|E1|Fault in controller|**during start-up**|
|---|---|---|
|E11|Valve’s actuator temperature outside its range|If you regulate with valve type AKV:|
|E15|Cut-out S2 sensor|Adjust n22 a little bit up and/or n04 a little bit down.|
|E16|Shortcircuited S2 sensor||
|**Error message**<br>E17|Cut-out  S3 sensor|If you regulate with valve type TQ:|
|E18|Shortcircuited S3 sensor|Adjust n26 a littlle bit down|
|E19|The input signal on terminals 18-19 is outside<br>the range.||
|E20|The input signal on terminals 14-15 is outside<br>the range(P0 signal)||
|A1|High-temperature alarm||
|**Alarm message**<br>A2|Low-temperature alarm||
|A11|No refrigerant has been selected||

7

**DEUTSCH**

##### **Bedienung**

###### **Display**

Die Wertdarstellung erfolgt dreistellig. Es besteht die Wahl zwischen Anzeige in °C oder in °F.

###### **Frontplatzierte Leuchtdioden**

Auf der Front sind Leuchtdioden angebracht, die aufleuchten, falls das zugehörige Relais aktiviert ist.

Die oberste Leuchtdiode zeigt den Öffnungsgrad des Ventils an. Kurze Impulse bedeuten geringen Flüssigkeitsstrom, und lange Impulse einen großen Flüssigkeitsstrom.

Die nächste Leuchtdiode zeigt an, ob der Regler Kältebedarf meldet.

Die drei untersten Leuchtdioden blinken, falls in der Regelung ein Fehler aufgetreten ist.

In diesem Fall lässt sich durch kurzzeitiges Betätigen der obersten Taste der Fehlercode am Display anzeigen und der Alarm abschalten.

###### **Tasten**

Mit den beiden Tasten lassen sich die Einstellungen ändern. Je nachdem, welche Taste Sie betätigen, ergibt sich ein höherer oder niedrigerer Wert. Bevor Werte geändert werden können, muss Zugang zum Menü hergestellt werden. Durch einige Sekunden langes Betätigen der obersten Taste erhält man Zugang zu einer Reihe von Parametercodes. Wählen Sie den zu ändernden Parametercode aus, und betätigen Sie anschließend beide Tasten gleichzeitig. Nach Änderung des Werts lässt sich der neue Wert speichern, indem erneut beide Tasten gleichzeitig betätigt werden.

Kurz zusammengefasst:

- Zugang zum Menü (oder schaltet einen Alarm aus)

- Zugang zu Änderungen

- Speichert eine Änderung

###### **Beispiele zur Bedienung**

Einstellen des Setpunkts

1. Beide Tasten gleichzeitig betätigen.

2. Eine der Tasten betätigen, und den neuen Wert auswählen.

3. Erneut beide Tasten gleichzeitig betätigen, um die Einstellung abzuschließen.

Einstellung eines der übrigen Menüs

1. Die oberste Taste betätigen, bis ein Parameter zur Anzeige gelangt.

2. Eine der Tasten betätigen, um zum gewünschten Para meter zu gelangen.

3. Beide Tasten gleichzeitig betätigen, bis der Wert des Parameters zur Anzeige kommt.

4. Eine der Tasten betätigen, und einen neuen Wert festlegen.

5. Erneut beide Tasten betätigen, um den Einstellvorgang abzuschließen.

###### Werkseinstellung

Die Rückkehr zu den ab Fabrik eingestellten Werten lässt sich wie folgt vornehmen: - Die Spannungszufuhr zum Regler unterbrechen.

- Beide Tasten betätigt halten und gleichzeitig die Spannungszufuhr wieder einschalten.

##### **Menüübersicht**

|**Menüübersicht**|||SW =|1.3x<br>**Werks-**|
|---|---|---|---|---|
|**Funktion**|**Para-**<br>**meter **|<sup>**Min.**</sup>|**Max.**|**einstel-**<br>**lun**|
|**Normalbild**<br>||||**g**|
|Zeigt den aktuellen Wert für Überhitzung /<br>Öffnungsgrad / Temp. Die Anzeige wird in o17<br>definiert|-||K||
|Temperatur, Überhitzung oder Temperatursollwert<br>kann durch kurzzeitige betätigung der untersten<br>T i d|<br>-||%||
|aste angezegt weren.<br>Anzeige wird in o17 definiert|||||
|**Temperaturregelung**|||||
|Einstellung der gewünschten Sollwert|-|-60°C|50°C|10|
|Differenz|r01|0,1 K|20,0 K|2.0|
|Einheiten (0=°C+bar /1=°F+psig)|r05|0|1|0|
|Externer Beitrag zur Referenz|r06|-50 K|50 K|0|
|Korrektur des Signals vom S2|r09|-10.0 K|10.0 K|0.0|
|Korrektur des Signals vom S3|r10|-10.0 K|10.0 K|0.0|
|Start / stopder Kühlung<br>i|r12|OFF|On|1|
|Thermostatfunktion definieren<br>(0= keine Thermostatfunktion, 1=On/off-Ther-<br>mostat)|r14|0|1|0|
|**Alarmmitteilungen**|||||
|Obere Abweichung (über Temperatureinstellung)|A01|3.0 K|20 K|5.0|
|Untere Abweichung (unter Temperatureinstellung)|A02|1 K|10 K|3.0|
|Verzögerungszeit des Alarms|A03|0 min.|90<br>min.|30|
|**Q-Aktuator Parameter**|||||
|P: Verstärkungsfaktor Kp|n04|0.5|20|3.0|
|I: Integrationszeit Tn|n05|30 s|600 s|120|
|D: Differentiationszeit Td (0 = off)|n06|0 s|90 s|0|
|Max. Wert des Überhitzungsreferenz|n09|2 K|50 K|6|
|Min. Wert des Überhitzungsreferenz|n10|1 K|12 K|4|
|MOP (max. = off)|n11|0.0 bar|60 bar|60|
|Periodenzeit (nur bei Anwendung von AKV/A-<br>Ventile)|n13|3 s|10 s|6|
|Stabilitätsfaktor zur Regelung der Überhitzung.<br>Änderungen sollten nur von geschultem Personal<br>vorgenommen werden.|n18|0|10|5|
|Dämpfung der Verstärkung im Sollwertbereich.<br>Änderungen sollten nur von geschultem Personal<br>vorgenommen werden.|n19|0.2|1.0|0.3|
|<br>Verstärkungsfaktor für die Überhitzung.<br>Änderungen sollten nur von geschultem Personal<br>|n20|0.0|10.0|0.4|
|vorgenommen werden.<br>Definition der Überhitzungsregelung.<br>1=MSS, 2=LOADAP|n21|1|2|1|
|<br>Wert für den min. Überhitzungssollwert bei Belas-<br>tungen unter 10%|n22|1|15|2|
|<br>Standby-Temperatur bei geschlossenem Ventil.<br>|||||
|(nur bei TQ-Ventil).<br>Änderungen sollten nur von geschultem Personal<br>|n26|0 K|20 K|0|
|vorgenommen werden.<br>Standby-Temperatur bei offenem Ventil (nur bei|||||
|f<br>TQ-Ventil).<br>Änderungen sollten nur von geschultem Personal<br>vorgenommen werden.<br>f|n27|-15 K|70 K|20|
|Max. Öffnungsgrad.<br>Änderungen sollten nur von geschultem Personal|n32|0|100|100|
|vorgenommen werden.<br>f|||||
|Min. Öffnungsgrad.<br>Änderungen sollten nur von geschultem Personal<br>|n33|0|100|0|
|vorgenommen werden.<br>**Diverses**|||||
|Regleradresse|o03*|0|119|-|
|AUS/EIN-Wechselschalter (Service-PIN-Mitteilung)|o04*|-|-|-|
|Ventil und Ausgangssignal definieren:<br>0: Off|||||
|f<br>1: TQ. AO: 0-20 mA<br>2: TQ. AO: 4-20 mA|||||
|3: AKV, AO: 0-20 m<br>4: AKV, AO: 4-20 mA|o09|0|7|0|

- 5: AKV, AO: EKC 347-SLAVE

- 6: ICM, AO:0-20 mA/ICM OD%

- 7: ICM, AO:4 - 20 mA /ICM OD%

8

|Festlegung des Eingangssignals am analogein-<br>gang AIA:|||||
|---|---|---|---|---|
|<br>0: kein Signal,<br>1: Temperatursollwert. 0-20 mA<br>2: Temperatursollwert. 4-20 mA<br>3: Verschiebung des Überhitzungssollwerts 0-20<br>mA|o10|0|4|0|
|4: Verschiebung des Überhitzungssollwerts. 4-20<br>mA|||||
|Einstellungs der Spannungsversorgungsfrequenz|o12|50 Hz|60 Hz|0|
|Displayanzeige für “Normalbild” wählen<br>(Bei kurzer Betätigung der unteren Taste wird<br>das in der Klammer angegebene Kriterium<br>angezeigt.)<br>1: Überhitzung  (Temperatur)<br>2: Öffnungsgrad des Ventils (Überhitzung)<br>3: Lufttemperatur  (Temperatursollwert)|o17|1|3|1|
|Handsteuerung der Ausgänge:<br>OFF: Keine Zwangssteuerung<br>1: Relais des Magnetventils ist ON<br>2: AKV/A-Ausgang ist ON<br>3: Alarmrelais wird aktiviert (öffnet)|o18|off|3|Off|
|Arbeitsbereich für Druckmessumformer – Mind-<br>estwert|o20|-1 bar|60 bar|-1.0|
|Arbeitsbereich für Druckmessumformer – Maxi-<br>malwert|o21|-1 bar|60 bar|12|
|(Einstellung für o09-Funktion, nur AKV und TQ)<br>Den Temperaturwert oder Öffnungsgrad festle-<br>gen, bei dem das Ausgangssignal das Minimum<br>betragen soll (0 oder 4 mA)|o27|-70°C|160°C|-35|
|(Einstellung für o09-Funktion, nur AKV und TQ)<br>Den Temperaturwert oder Öffnungsgrad festle-<br>gen, bei dem das Ausgangssignal das Maximum<br>betragen soll (20 mA)|o28|-70°C|160°C|15|
|Kältemitteleinstellung<br>|||||
|1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.<br>6=R13.  7=R13b1.  8=R23.  9=R500.  10=R503.<br>11=R114.  12=R142b. 13=Benutzerdefinert.<br>14=R32. 15=R227.  16=R401A.  17=R507.<br>18=R402A.  19=R404A. 20=R407C.  21=R407A.<br>|o30|0|29|0|
|22=R407B.  23=R410A.  24=R170.  25=R290.|||||
|26=R600.  27=R600a.  28=R744.  29=R1270.|||||
|**Service**|||||
|Anzeige der Stellantriebstemperatur des Ventils|u04|||°C|
|Anzeige der Referenz der Stellantriebstemperatur<br>des Ventils|u05|||°C|
|naloger EingangAIA (18-19)|u06|||mA|
|Analoger AusgangAO (2-5)|u08|||mA|
|Anzeige des Status am DI Eingang (start/stop<br>Eingang)|u10|||on/off|
|Einschaltzeit des Thermostats|u18|||min.|
|Anzeige der Temperatur am S2-Fühler|u20|||°C|
|Anzeige der Überhitzung|u21|||K|
|Anzeige der aktuellen Überhitzungssollwert der<br>Regelung|u22|||K|
|Anzeige des Öffnungsgrad des Ventils|u24|||%|
|Anzeige des Verdampfungsdrucks|u25|||bar|
|Anzeige der Vedampfungstemperatur|u26|||°C|
|Anzeige der Temperatur am S3-Fühler|u27|||°C|
|Temperaturreferenz|u28|||°C|
|Signal am Druckmessumformereingang ablesen|u29|||mA|

*) Diese Einstellung is nur möglich, wenn ein Datenkommunikationsmodul im Regler montiert ist.

###### **Start des Reglers**

- Nach Anschluss des Reglers an die Stromversorgung sind vor Inbetriebnahme des Reglers folgende Schritte vorzunehmen: 1. Den externen Schalter zum Starten und Stoppen der Regelung ausschalten.

2. Gemäß Menüübersicht die gewünschten Werte für die verschiedenen Parameter einstellen.

3. Den externen Schalter einschalten - die Regelung wird gestartet.

4. Verfolgen Sie die aktuelle Raum-temperatur oder Überhitzung am Display.

- (Über die Klemmen 2 und 5 kann ein der Displayanzeige entsprechendes Stromsignal abgegeben werden. Ggf. Datenerfassungs ausrüstung zur Verfolgung des Temperaturverlaufs anschliessen.)

###### **Pendeln der Überhitzung**

Erreicht die Kälteanlage einen stabilen Arbeitszustand, ist mit den werkseits eingestellten Regelparametern in den meisten Fällen ein stabiles und relativ schnelles Regelsystem gegeben. Sollte das System dennoch pendeln, kann die Ursache zu niedrig gewählte Überhitzungsparameter sein:

Falls adaptive Überhitzung gewählt wurde: n09, n10 und n18 justieren.

Falls belastungsabhängige Überhitzung gewählt wurde: n09, n10 und n22 justieren.

Eine andere Ursache können nicht optimal eingestellte Regelungsparameter sein:

Bei einer Periodendauer größer als die Integrationszeit:

(Tp > Tn , (Tn ist z.B. 240 Sekunden))

1. Tn auf 1.2 x Tp erhöhen

2. Abwarten, bis sich die Anlage wieder stabilisiert.

3. Pendelt sie nach wie vor, Kp mit z.B. 20% reduzieren. 4. Abwarten, bis sich die Anlage wieder stabilisiert.

5. Bei fortgesetztem Pendeln Punkt 3 und 4 wiederholen.

Bei einer Periodendauer kleiner als die Integrationszeit:

(Tp < Tn , (Tn ist z.B. 240 Sekunden))

1. Kp mit z.B. 20% des Skalenwerts reduzieren.

2. Abwarten, bis sich die Anlage wieder stabilisiert.

3. Bei fortgesetztem Pendeln Punkt 1 und 2 wiederholen.

###### **Der Re** **g ler kann fol** **g ende Meldun** **g en anzei** **g en:**

|E1||Fehler im Regler|
|---|---|---|
|E11||Stellantriebstemperatur des Ventils außerhalb<br>des Bereichs|
|E15||S2 Unterbrochen|
|E16||S2 kurzgeschlossen|
|E17|**Fehlermitteilung**|S3 Unterbrochen|
|E18||S3 kurzgeschlossen|
|E19||Das Eingangssignal auf Klemme 18-19 liegt<br>außerhalb des Bereichs.|
|E20||Das Eingangssignal auf Klemme 14-15 liegt<br>außerhalb des Bereichs (P0-Signal).|
|A1||Hoch Temperaturalarm|
|A2|**Alarmmitteilung**|Tief Temperaturalarm|
|A11||Kein Kältemittelgewählt|

###### **Bei zu starkem Unterschwingen der Überhitzung beim Anlauf**

Falls mit Ventil Typ AKV geregelt wird: n22 etwas höher, und/oder n04 etwas tiefer justieren.

Falls mit Ventil Typ TQ geregelt wird: n26 etwas tiefer justieren.

9

**FRANCAIS**

##### **Utilisation**

###### **Afficheur**

Les valeurs sont affichées avec trois chiffres, un réglage permettant de choisir entre °C et °F.

###### **Diodes luminescentes en façade**

Les diodes s’allument lorsque leurs relais respectifs sont alimentés. La diode supérieure indique l’ouverture de la vanne. Impulsions courtes : faible débit de liquide ; impulsions prolongées : fort débit de liquide.

La diode suivante indique l’appel de froid émis par le régulateur. Les trois diodes inférieures clignotent en cas d’erreur de régulation.

Dans ce cas, on peut appeler le code d’erreur à l’afficheur et annuler l’alarme en appuyant brièvement sur le bouton supérieur.

###### **Les boutons**

Les deux boutons permettent de modifier un réglage, l’augmentant ou la réduisant selon le cas. Mais il faut d’abord avoir accès au menu: appuyer quelques secondes sur le bouton supérieur. Apparaissent alors la série de codes de paramétrage. Chercher le code à modifier et appuyer sur les deux boutons en même temps. Après la modification, mémoriser la nouvelle valeur en appuyant à nouveau sur les deux boutons en même temps. Ou bref :

- Accès au menu (ou suppression d’une alarme)

- Accès à la modification

- Mémorisation de la modification

###### **Exemples d’utilisation**

###### Réglage du point de consigne

1. Appuyer sur les deux boutons en même temps.

2. Appuyer sur l’un des boutons pour choisir la nouvelle valeur.

3. Appuyer à nouveau sur les deux boutons en même temps pour terminer le réglage.

###### Réglage des autres menus

1. Appuyer sur le bouton supérieur jusqu’à apparition d’un paramètre.

2. Appuyer sur l’un des boutons pour trouver le paramètre à régler.

3. Appuyer sur les deux boutons en même temps jusqu’à apparition de la valeur du paramètre.

4. Appuyer sur l’un des boutons pour choisir la nouvelle valeur.

5. Appuyer à nouveau sur les deux boutons en même temps pour terminer le réglage.

###### Réglage départ usine

Pour retrouver éventuellement les valeurs réglées en usine, procéder ainsi :

- Couper la tension d’alimentation du régulateur.

- Maintenir les deux boutons enfoncés en remettant le régulateur sous tension.

|**Sommaire des menus**|||S|W =1.3x<br>|
|---|---|---|---|---|
|**Fonction**|**Para-**<br>**mètre **|<sup>**Min.**</sup>|**Max.**|**Regl.**<br>**usine**|
|**Image normale**<br>Indique la surchauffe/l'ouverture actuelle/la tem-|-||||
|pérature Cet affichage est défini en o17|||||
|.fi i.<br>La température, la surchauffe ou la référence de<br>temp. s’affiche en tapant brièvement sur le bouton|-||%||
|inférieur. Cet  affichage est défini en o17.|||||
|fi i<br>**Référence**|||||
|Régler le point de consigne voulu.|-|-60°C|50°C|10|
|Différentiel|r01|0,1 K|20,0 K|2.0|
|Unités (0=°C+bar /1=°F+psig)|r05|0|1|0|
|modification externe de la référence|r06|-50 K|50 K|0|
|Correction du signal en provenance de S2|r09|-10.0 K|10.0 K|0.0|
|Correction du signal en provenance de S3|r10|-10.0 K|10.0 K|0.0|
|Arrêt/marche du refroidissement|r12|OFF|On|1|
|Définition de la fonction thermostatique<br>(0=aucune fonction ; 1=thermostat tout/rien)|r14|0|1|0|
|**Alarme**|||||
|Déviation supérieure (au-dessus du réglage de<br>temp.)|A01|3.0 K|20 K|5.0|
|Déviation inférieure (au-dessous du réglage de<br>temp.)|A02|1 K|10 K|3.0|
|Temporisation de l'alarme|A03|0 min.|90 min.|30|
|**Paramètres de régulation**|||||
|P: Facteur d'amplification Kp|n04|0.5|20|3.0|
|I: Temps d'intégration Tn|n05|30 s|600 s|120|
|D: Temps de différentiation Td (0 = off)|n06|0 s|90 s|0|
|Valeur maximum de la référence de surchauffe|n09|2 K|50 K|6|
|Valeur minimum de la référence de surchauffe|n10|1 K|12 K|4|
|MOP (max. = Off)|n11|0.0 bar|60 bar|60|
|Période (AKV/A seulement)|n13|3 s|10 s|6|
|Facteur stabilité de la régulation de surchauffe<br>Modification uniquement par du personnel spé-<br>|n18|0|10|5|
|cialement formé.<br>Amortissement de l’amplification dans la zone près|i||||
|de la référence<br>Modification uniquement par du personnel spé-<br>cialement formé.|n19|0.2|1.0|0.3|
|Facteur d’amplification de surchauffe.<br>Modification uniquement par du personnel spé-<br>cialement formé.|n20|0.0|10.0|0.4|
|Définition de la réulation de surchauffe|||||
|i   g  f.<br>1=MSS, 2=LOADAP|n21|1|2|1|
|Valeur de la référence de surchauffe minimum pour<br>charges inférieures à 10%|f<br>n22|1|15|2|
|<br>Température minimum à vanne fermée (TQ seule-<br>ment). Modification uniquement par du personnel<br>|n26|0 K|20 K|0|
|spécialement formé.<br>Température minimum à vanne ouverte (TQ seule-|||||
|<br>ment). Modification uniquement par du personnel<br>|n27|-15 K|70 K|20|
|spécialement formé.<br>Ouverture maximum.|||||
|Modification uniquement par du personnel spé-<br>cialement formé.|n32|0|100|100|
|Ouverture minimum.|||||
|Modification uniquement par du personnel spé-<br>|n32|0|100|0|
|cialement formé.|||||
|**Divers**|||||
|Adresse du régulateur|o03*|0|119|-|
|Commutateur ON/OFF (message broche service)|o04*|-|-|-|
|Définition de vanne et de signal de sortie :<br>0: Off<br>1: TQ. AO: 0-20 mA<br>2: TQ. AO: 4-20 mA<br>|||||
|3: AKV, AO: 0-20 m<br>4: AKV, AO: 4-20 mA|o09|0|7|0|

- 5: AKV, AO: EKC 347-SLAVE

- 6: ICM, AO:0-20 mA/ICMID% 7: ICM, AO:4-20 mA/ICMID%

10

|Définir le signal de l'entrée analogique AIA:<br>0  il|||||
|---|---|---|---|---|
|: aucun sgna<br>1: Point de consigne température, 0-20 mA<br>2: Point de consigne température, 4-20 mA<br>3: Décalage de la référence de surchauffe de 0-20<br>mA|o10|0|4|0|
|4: Décalage de la référence de surchauffe, 4-20 mA|||||
|Choisir la fréquence d’alimentation|o12|50 Hz|60 Hz|0|
|Choisir l’affichage pour « Image normale »<br>(En tapant brièvement sur le bouton inférieur<br>on peut faire apparaître ce qui est indiqué entre<br>parenthèses)<br>f|o17|1|3|1|
|1 : Surchauffe (température)<br>2 : Ouverture de la vanne (surchauffe)|||||
|3 : Température de l’air (réference de température)|||||
|Commande manuelle des sorties<br>Off : Aucune commande manuelle|||||
|1: Le relais vers l’électrovanne est ON<br>2: La sortie AKV/A est ON<br>|o18|off|3|Off|
|3: Le relais d’alarmes est alimenté (ouverture)|||||
|Gamme de travail du transmetteur de pression<br>–valeur minimum|o20|-1 bar|60 bar|-1.0|
|Gamme de travail du transmetteur de pression<br>–valeur maximum|o21|-1 bar|60 bar|12|
|<br>(Réglage relatif à la fonction o09, uniquement pour|||||
|AKV et TQ)<br>Choisir la température liée au signal de sortie<br>minimum (0 ou 4 mA).|o27|-70°C|160°C|-35|
|(Réglage relatif à la fonction o09,uniquement pour<br>AKV et TQ). Choisir la température liée au signal de<br>sortie maximum (20 mA).|o28|-70°C|160°C|15|
|Définition du réfrigérant<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.<br>6=R13.  7=R13b1.  8=R23.  9=R500.  10=R503.|||||
|11=R114.  12=R142b. 13=Définition client. 14=R32.<br>15=R227.  16=R401A.  17=R507. 18=R402A.<br>19=R404A. 20=R407C.  21=R407A.  22=R407B.|o30|0|29|0|
|23=R410A.  24=R170.  25=R290.  26=R600.|||||
|27=R600a.  28=R744.  29=R1270.|||||
|**Entretien**|||||
|Température de l'actuateur de la vanne  TQ|u04|||°C|
|Référence de la température de l'actuateur de la|05|||°C|
|vanne|u||||
|Entrée analogique AIA (18-19)|u06|||mA|
|Sortie analogique AO(2-5)|u08|||mA|
|L'état de l'entrée DI|u10|||on/off|
|Temps d’enclenchement du thermostat|u18|||min.|
|Température du capteur S2|u20|||°C|
|Surchauffe|u21|||K|
|Référence de surchauffe|u22|||K|
|L’ouverture de la vanne|u24|||%|
|Pression d’évaporation|u25|||bar|
|Température d’évaporation|u26|||°C|
|Température du capteur S3|u27|||°C|
|Référence de température|u28|||°C|
|Signal de l’entrée du transmetteur de pression|u29|||mA|

*)  Ce réglage n’est possible que si un module de transmission de données est installé dans le régulateur.

|**Le rég**|**ulateurpeut émettre le**|**s messages suivants :**|
|---|---|---|
|E1||Erreur dans le régulateur|
|E11||Température de l’actuateur de la vanne hors<br>limite|
|E15||S2 coupée|
|E16|**Message d’erreur**|S2 court-circuitée|
|E17||S3 coupée|
|E18||S3 court-circuitée|
|E19||Signal d’entrée bornes 18-19 horsgamme|
|E20||Signal d’entrée bornes 14-15 hors gamme<br>(signal P0)|
|A1|**’**|Alarmepour température tropélevée|
|A2|**Message dalarme**|Alarmepour température tropbasse|
|A11||Omission choix de réfrigérant|

###### **Mise en route du régulateur**

Après le raccordement électrique du régulateur, il faut effectuer les actions suivantes pour démarrer la régulation :

1. Ouvrir le contact externe qui démarre et arrête la régulation.

2. Suivre le sommaire des menus et régler les différents paramètres sur les valeurs désirées.

3. Fermer le contact externe pour mettre la régulation en route.

4. Suivez la température ambiante actuelle ou la surchauffe à l’afficheur. (Un signal de courant émis aux bornes 2 et 5 peut transmettre l’affichage. Raccordez éventuellement un matériel de recueil de données pour pouvoir suivre le comportement de la température.)

###### **S’il y a pompage de la surchauffe**

Lorsque l’installation frigorifique a obtenu un fonctionnement stable, les paramètres de régulation départ usine assurent normalement un système de régulation stable et relativement rapide.

Si par contre, il y a pompage dans le système, c’est peut-être que les paramètres de surchauffe choisis sont trop bas :

En cas de surchauffe adaptative : Ajuster : n09, n10 et. N18

En cas de surchauffe en fonction de la charge : Ajuster : n09, n10 et n22 Une autre cause peut être que les paramètres de régulation choisis ne sont pas optimaux :

Si les périodes sont supérieures au temps d’intégration :

(Tp > Tn , (Tn = 240 secondes, par exemple))

1. Augmenter Tn à 1,2 x Tp

2. Attendre que l’installation soit stable.

3. S’il y a encore des oscillations, réduire Kp de 20%, par exemple.

4. Attendre que l’installation soit stable.

5. Si les oscillations persistent, répéter les points 3 et 4.

Si les périodes sont inférieures au temps d’intégration :

(Tp < Tn , (Tn  240 secondes, par exemple))

1. Réduire Kp de 20% de la valeur d’échelle, par exemple

2. Attendre que l’installation soit stable.

3. Si les oscillations persistent, répéter les points 1 et 2.

###### **Si la surchauffe accuse un dépassement de réglage (négatif) trop important**

Installations AKV : Ajuster n22 légèrement vers le haut et/ou n04 légèrement vers le bas.

Installations TQ : Ajuster n26 légèrement vers le bas.

11

12
