# Danfoss AK-CC 250A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## INSTRUCTIONS – Coordinated defrost

*Kilde: Danfoss-dokument AN112486427656en-000301.pdf*

### **INSTRUCTIONS**

*[Figurtekst: tamb = 0 - +55°C · 230 V a.c.  50/60 Hz · 2.5 VA · 10 V < U < 256 V · CE (250 V a.c.) UL *** (240 V a.c.) Pt /PTC sensors · 10 A Resistive · DO1. Refrigeration * 8 (6) A · 5FLA, 30LRA See page 6. · 10 A Resistive · DO2. Defrost * 8 (6) A · 5FLA, 30LRA · 6 A Resistive · DO3. Fan or · 6 (3) A 3FLA, 18LRA · refrigeration 2 * · 131 VA Pilot duty · DO4. Alarm, light, rail heat     4 (1) A 4 A Resistive · or hotgas defrost * Min. 100 mA** 131 VA Pilot duty · * DO1 and DO2 are 16 A relays. DO3 and DO4 are 8 A relays. Max. load must  be keept. · ** Gold plating ensures make function with small contact loads · *** UL-approval based on 30000  couplings]*

###### Coordinated defrost

*[Figurtekst: Data communication MOD-BUS:]*

06-2015 RI8PG302

*[Figurtekst: o61 — Electrical connections · 1  *) 2 *) · *) *) · 3  4 · *) *) · 5  6 · *) *) · 7  8 · *) *) · 9  10 · ! ! ! *) DI1, DI2:   AU: Guld, Gold, Or, Oro   l = max. 15 m · 2  Instructions      RI8PG302   © Danfoss 06/2015    AK-CC 250A · Danfoss 84B2428.12 Danfoss 84B2429.13 · Danfoss 84B2430.13]*

2

En g lish

##### **Setting:**

|**1 Open parameter r12 and stop the regulation**|Auxiliary table for settings<br>||**Case**|||**Room**||
|---|---|---|---|---|---|---|---|
|**2 Open parameter o06 and set the used sensor**<br>**type**|(quick-setup)|Defrost<br>stop on<br>time|Defro<br>on|st stop<br>S5|Defrost<br>stop on<br>time|Defro<br>on|st stop<br>S5|
|**3 Select electric connection based on the draw-**|**Preset settings**(o62)|**1**|**2**|**3**|**4**|**5**|**6**|
|<br>**ings on page 2**|Temperature (SP)|4°C|2°C|-24°C|6°C|3°C|-22°C|
|**4 Oen arameter o61 and set the electric con-**|Max. temp. setting (r02)|6°C|4°C|-22°C|8°C|5°C|-20°C|
|**p p**<br>**nection number in it**|Min. temp. setting (r03)|2°C|0°C|-26°C|4°C|1°C|-24°C|
||Sensor signal for thermostat. S4% (r15)||100%|||0%||
|**5 Now select one of the preset settings from the**<br>**tbl  th ihthd id**|Alarm limit high (A13)|10°C|8°C|-15°C|10°C|8°C|-15°C|
|**ae on e rg-an se**|Alarm limit low (A14)|-5°C|-5°C|-30°C|0°C|0°C|-30°C|
|**6 Open parameter o62 and set the number for**<br>|Sensor signal for alarm funct.S4% (A36)||100%|||0%||
|**the array of presettings**|Interval between defrost (d03)|6 h|6h|12h|8h|8h|12h|
|**7 Open parameter r12 and start the regulation**|Defrost sensor: 0=time, 1=S5, 2=S4 (d10)|0|1|1|0|1|1|
|**8 G thh th  f ft tti**|DI1 config. (o02)|Case|cleaning|=10|Doo|r function|=3|
|**o roug e survey o acory sengs.**<br>**Make any necessary changes in the respective**|Sensor signal for display view S4% (017)||100%|||0%||
|**parameters.**|||A        i|16  Th     i|tti i th  i|fild i|i l b h|

Array 1-6:  The settings in the grey fields will be changed

**9 For network.**

- **a. Set the address in o03**

- **b. Start scan function in the system unit.**

|**Parameters**|||**EL-diagram**|**n**|**umbe**|**r (pag**|**e 2)**||**Min.-**|**Max.-**|**Factory**|**Actual**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Function**|**Codes**|**1**<br>**2**|**3**<br>**4**|**5**|**6**|**7**|**8**|**9**<br>**10**|**value**|**value**|**setting**|**setting**|
|**Normal operation**|||||||||||||
|Temperature(setpoint)|---||||||||-50.0°C|50.0°C|2.0°C||
|**Thermostat**<br>f|||||||||||||
|Differential|***<br>r01||||||||0.0 K|20.0K|2.0 K||
|Max. limitation of stepson setting|***<br>r02||||||||-49.0°C|50°C|50.0°C||
|Min. limitation of setpoint setting|***<br>r03||||||||-50.0°C|49.0°C|-50.0°C||
|Adjustment of temperature indication<br>|r04<br>||||||||-20.0 K<br>|20.0 K<br>|0.0 K<br>||
|Temperature unit(°C/°F)<br>|r05<br>||||||||°C<br>|°F<br>|°C<br>||
|Correction of the signal from S4|r09||||||||-10.0 K|+10.0 K|0.0 K||
|Correction of the signal from S3<br>|r10||||||||-10.0 K|+10.0 K|0.0 K||
|Manual service,stopregulation,start regulation(-1,0,1)|r12||||||||-1|1|0||
|Displacement of reference duringnight operation<br>i|r13||||||||-10.0 K<br>|10.0 K<br>|0.0 K<br>||
|Definition and weighting, if applicable, of thermostat sensors<br>-S4% (100%=S4,  0%=S3)|r15||||||||0%|100%|100%||
|The heating function is started a number of degrees below the|r36||||||||-15.0 K|-3.0 K|-15.0 K||
|thermostats cutout temperature|||||||||||||
|Activation of reference displacement  r40|r39||||||||OFF|ON|OFF||
|Value of reference displacement(activate via r39 or DI)|r40||||||||-50.0 K|50.0 K|0.0 K||
|**Alarm**|||||||||||||
|Delayfor temperature alarm|A03||||||||0 min|240 min|30 min||
|Delayfor door alarm<br>|***<br>A04<br>||||||||0 min<br>|240 min<br>|60 min<br>||
|Delayfor temperature alarm after defrost|A12||||||||0 min|240 min|90 min||
|High alarm limit|***<br>A13||||||||-50.0°C|50.0°C|8.0°C||
|Low alarm limit|***<br>A14||||||||-50.0°C|50.0°C|-30.0°C||
|Alarm delayDI1|A27||||||||0 min|240 min|30 min||
|Alarm delayDI2|A28||||||||0 min|240 min|30 min||
|Signal for alarm thermostat. S4%(100%=S4,0%=S3)<br>|A36||||||||0%|100%|100%||
|**Compressor**<br>|||||||||||||
|Min. ON-time|c01||||||||0 min|30 min|0 min||
|Min. OFF-time|c02||||||||0 min|30 min|0 min||
|Time delayfor cutin of comp.2|c05||||||||0 sec|999 sec|0 sec||
|Compressor relay 1 must cutin and out inversely|c30||||||||0|1|0||
|<br>(NC-function)|||||||||OFF|ON|OFF||
|**Defrost**|||||||||||||
|Defrost method(none/EL/GAS/BRINE)|d01||||||||no|bri|EL||
|Defrost stoptemperature|d02||||||||0.0°C|25.0°C|6.0°C||
|Interval between defrost starts<br>|d03||||||||0 hours|48 hours|8 hours||
|Max. defrost duration|d04||||||||0 min|180 min|45 min||
|Displacement of time on cutin of defrost at start-up|d05||||||||0 min|240 min|0 min||
|Dripoff time<br>|d06<br>||||||||0 min|60 min|0 min||
|Delayfor fan start after defrost|d07||||||||0 min|60 min|0 min||
|Fan start temperature|d08||||||||-15.0°C|0.0°C|-5.0°C||
|Fan cutin during defrost<br>0: Stopped<br>1: Running|d09||||||||0|2|1||
|<br>2: Running during  pump down and defrost|||||||||||||
|<br>Defrost sensor(0=time,1=S5,2=S4)|d10||||||||0|2|0||
|Pumpdown delay|d16||||||||0 min|60 min|0 min||
|Drain delay|d17||||||||0 min|60 min|0 min||
|Max. aggregate refrigeration time between two defrosts|d18||||||||0 hours|48 hours|0 hours||
|Defrost on demand - S5 temperature’s permitted variation dur-<br>  f|d19||||||||0.0 K|20.0 k|20.0 K||
|ing frost build-up. On central plant choose 20 K (=off)|||||||||||||
|f<br>Delayof hotgas injection|d23||||||||0 min|60 min|0 min||

3

|**Fan**||**1**<br>**2**<br>**3**<br>**4**<br>**5**<br>**6**<br>**7**<br>**8**<br>**9**<br>**10**||||
|---|---|---|---|---|---|
|Fan stopat cutout compressor<br>Dlf f||F01<br>F|no<br>i|yes<br>i|no<br>i|
|eayo an stop<br>||02<br>|0 mn<br>°|30 mn<br>°|0 mn<br>°|
|Fan stoptemperature(S5)<br>||F04|-50.0C|50.0C|50.0C|
|**HACCP**<br>Actual temperature measurement for the HACCP function<br>Last registered peak temperature||h01<br>h10||||
|<br>Selection of function and sensor for the HACCP function 0 = no||h11|0|2|0|
|.<br>HACCP fi 1S4 d b l S3 2S d||||||
|uncton.=use (maye aso ).=5 use<br>Alarm limit for the HACCP function<br>||h12<br>|-50.0°C<br>|50.0°C<br>|8.0°C<br>|
|Time delay for the HACCP alarm||h13|0 min.|240 min.|30 min.|
|Select signal for the HACCP function. S4% (100% = S4, 0% = S3)<br>**Real time clock**||h14|0%|100%|100%|
|Six start times for defrost.<br>||t01-t06|0 hours|23 hours|0 hours|
|Setting of hours.<br>0=OFF||||||
|Six start times for defrost.<br>Setting of minutes.<br>0=OFF||t11-t16|0 min|59 min|0 min|
|Clock - Settinof hours|***|t07|0 hours|23 hours|0 hours|
|g <br>Clk  Sif i|***||<br>i|<br>i|<br>i|
|oc - ettngo mnute<br>Clock - Settingof date|***|t08<br>t45|0 mn<br>1|59 mn<br>31|0 mn<br>1|
|Clock - Settingof month|***|t46|1|12|1|
|Clock - Settingofyear<br>**Miscellaneous**|***|t47|0|99|0|
|Delayof output signals after start-up<br>||o01<br>|0 s<br>|600 s<br>|5 s<br>|
|Input signal on DI1. Function:<br>0=not used. 1=status on DI1. 2=door function with alarm when||o02|1|11|0|
|open. 3=door alarm when open. 4=defrost start (pulse-pres-<br>sure).  5=ext.main switch. 6=night operation 7=change refer-<br>ence (activate r40). 8=alarm function when closed. 9=alarm<br>||||||
|function when open. 10=case cleaning (pulse pressure).<br>11=forced cooling at hot gas defrost.||||||
|Network address(0=off)||o03|0|240|0|
|f<br>Access code 1(all settings)||o05|0|100|0|
|<br>Used sensor type. See page 6.<br>°||o06|Pt|P02|Pt|
|Pt: Pt 1000 Ω @ 0C<br>||||||
|P01: PTC 1000 Ω (nominal 990 Ω) = EKS 111||||||
|P02: PTC 1000 Ω @ 25°C (nominal 1000 Ω)<br>Displaystep= 0.5(normal 0.1 at Pt sensor)||o15|no|yes|no|
|Max hold time after coordinated defrost<br>||o16<br>|0 min<br>|60 min<br>|20<br>|
|Select signal for displayview.  S4%(100%=S4,0%=S3)<br>||o17<br>|0%<br>|100%<br>|100%<br>|
|Input signal on DI2. Function:<br>(0=not used. 1=status on DI2. 2=door function with alarm when<br>open. 3=door alarm when open. 4=defrost start (pulse-pres-<br>sure).  5=ext. main switch 6=night operation 7=change refer-<br>ence (activate r40). 8=alarm function when closed. 9=alarm<br>||o37|0|12|0|
|function when open. 10=case cleaning (pulse pressure).<br>11=forced cooling at hot gas defrost.). 12=coordinated defrost)||||||
|Configuration of light function (relay 4)||o38|1|3|1|
|1=ON during day operation. 2=ON / OFF via data communica-||||||
|<br>tion. 3=ON follows the DI-function, when DI is selected to door<br>fi   d l||||||
|uncton or to oor aarm<br>Activation of light relay (onlyif o38=2)<br>||o39|OFF|ON|OFF|
|Rail heat On time duringdayoperations||o41|0%|100%|0|
|Rail heat On time duringnight operations||o42|0%|100%|0|
|Rail heat period time (On time + Offtime)||o43|6 min|60 min|10 min|
|f <br>Case cleaning. 0=no case cleaning. 1=Fans only. 2=All output<br>Off|***|o46|<br>0|<br>2|<br>0|
|f.<br>Selection of  EL diagram. See overviewpage 2<br>|*<br>|o61*<br>|1|10|1|
|Download a  set of predetermined settings. See overview<br>previous page.|*|o62*|0|6|0|
|<br>Access code 2(partlyaccess)|***|o64|0|100|0|
|Save the controllers present settings to the programming key.<br>l||o65|0|25|0|
|Seect your own number.<br>Load a set of settings from the programming key (previously<br>||o66*|0|25|0|
|saved via o65 function)<br>Replace the controllers factory settings with the present set-||o67|OFF|On|OFF|
|tings<br>**Service**||||||
|Status codes are shown onpage 5||S0-S33||||
|Temperature measured with S5 sensor<br>Status on DI1 input. on/1=closed|***|u09<br>u10||||
|Temperature measured with S3 sensor|***|u12||||
|<br>Stt  ihtti(ff)1ld|***|13||||
|aus on ngoperaonon or of=cose<br>Temperature measured with S4 sensor|***|u<br>u16||||
|Thermostat temperature<br>Read thepresent regulation reference||u17<br>u28||||
|Status on DI2 output. on/1=closed<br>Temerature shown on disla||u37<br>u56||||
|p py<br>Measured temperature for alarm thermostat<br>||u57<br>||||
|Status on relayfor cooling<br>Status on relayfor fan|**<br>**|u58<br>u59||||

4

|Status on relayfor defrost|**|u60|
|---|---|---|
|Status on relayfor rail heat|**|u61|
|Status on relayfor alarm|**|u62|
|Status on relayfor light|**|u63|
|Status on relayfor valve in suction line|**|u64|
|Status on relayfor compressor 2|**|u67|

*) Can only be set when regulation is stopped (r12=0)

SW = 2.3x

**) Can be controlled manually, but only when r12=-1

***) With access code 2 the access to these menus will be limited

Factory settings are indicated for standard units. Other code numbers have customized settings.

*[Figurtekst: Fault code display Alarm code display Status code display · E 1 Fault in controller A 1 Hi g h tem p erature alarm S0 Re g ulatin g · E 6 Chan g e batter y  + check clock A 2 Low  tem p erature alarm S 1 Waitin g  for end of the coordinated defrost · E 25 S3 sensor error A 4 Door alarm S 2 ON-time Com p ressor · E 26 S4 sensor error A 5 Max. Hold time S 3 OFF-time Com p ressor · E 27 S5 sensor error A 15 DI 1 alarm S 4 Dri p -off time · A 16 DI 2 alarm S 10 Refri g eration sto pp ed b y  main switch · A 45 Standb y  mode S 11 Refri g eration sto pp ed b y  thermostat · A 59 Case cleanin g S 14 Defrost se q uence. Defrostin g · A 60 HACCP alarm S 15 Defrost se q uence. Fan dela y · S 17 Door o p en  ( o p en DI in p ut ) · S 20 Emer g enc y  coolin g · S 25 Manual control of out p uts · S 29 Case cleanin g · S 30 Forced coolin g · S 32 Dela y  of out p ut at start-u p · S33 Heat function r36 is active · non The defrost temperature cannot be dis- · played. There is stop based on time · -d- Defrost in  p ro g ress · PS Password re q uired]*

###### **The buttons**

###### **LED**

###### Set menu

1. Push the upper button until a parameter r01 is shown

2. Push the upper or the lower button and find that parameter you want to change

3. Push the middle button until the parameter value is shown

4. Push the upper or the lower button and select the new value

5. Push the middle button again to enter the value.

###### Set temperature

1. Push the middle button until the temperature value is shown

2. Push the upper or the lower button and select the new value

3. Push the middle button to select the setting.

Reading the temperature at defrost sensor

- Push briefly the lower button

- Light emitting diode

   - = refrigeration

   - = defrost

   - = fan running

Flashes fast at alarm

###### **HACCP**

HACCP function is active

Manuel start or stop of a defrost

Cutout alarm relay / receipt alarm/see alarm code

   - Push the lower button for four seconds. (Though not for application 4).

- Push short the upper button

See HACCP registration

1. Give the middle button a long push until h01 appears

2. Select required h01-h10

3. See value by giving the middle button a short push

5

###### **Sensor overview**

###### **o06**

Pt: Pt 1000 Ω @ 0°C (AKS 11, AKS 12, AKS 21) P01: PTC 1000 Ω (nominal 990 Ω) = EKS 111 P02: PTC 1000 Ω @ 25°C (nominal 1000 Ω)

*[Figurtekst: Pt 1000  PTC 1000 Ω  PTC 1000 Ω · @ 0°C @ 25°C · AKS 11,  KTY81-121 KTY81-110 · AKS 12,  EKS 111 · AKS 21 · °C  Ω Ω Ω · 30 1167.7    1029 1040 · 25 1097.3    990 1000 · 20 1077.9 951 961 · 15 1058.5    914 923 · 10 1039.0   877 886 · 5 1019.5   841 850 · 0 1000.0  807 815 · −5  980.4  773 781 · −10     960.9  740 747 · −15      941.2  708 715 · −20      921.6  677 684 · −25      901.9  647 653 · −30      882.2  617 624 · −35      862.5  589 595 · −40     842.7  562 567 · Carel: Carel: Frigo: · TSH/TST/TSM/ 03/06/015 VX6 · TSQ/PT1 Dixell: · Dixell: S6 · PMG/PMP/PMT Elliwell: · SN6/SN7 · Lae: · ST1K.CP · o06 Pt P01 P02]*

|Additional information:|English Manual|||
|---|---|---|---|
|Weitere Information:|Deutsches Manual|||
|Renseignements supplémentaires:|Manuel en français|||
|Yderligere information:|Dansk Manual|RS8GC...|www.danfoss.com|
|Información adicional:|Manual español|||
|Ytterligare information:|Svenska Handbok|||
|Aanvullende informatie:|Dutch Handleiding|||

The Product contains electrical components A nd may not be disposed together with domestic waste. Equipment must be separate collected with Electrical and Electronic waste. According to Local and currently valid legislation.

6
