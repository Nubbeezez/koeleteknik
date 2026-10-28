# Danfoss AK-CC 450 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## RI8LM802 10-2013 – The controller is provided with signs from the factory indicating application 1. If you employ another use, signs are provided so t

*Kilde: Danfoss-dokument AN098686427594en-000801.pdf*

*[Figurtekst: Instructions · AK-CC 450 · Identification Dimensions · 084B8022 · Principle · Expansion valve Brine valve]*

RI8LM802  10-2013

The controller is provided with signs from the factory indicating application 1. If you employ another use, signs are provided so that you can mount the relevant one.

2

*[Figurtekst: 5 · 6 · 6 + 8 · 7 · 7 · 8 · As 6 · 9 · As 1-5]*

*[Figurtekst: 5 · 6 · 6 + 8 · 7 · 7 · 8 · As 6 · 9]*

3

#### **Data communication**

**Important** All connections to the data communication MODBUS, RS 485 and DANBUSS must comply with the requirements for data communication cables. See literature: RC8AC.

AKA 245 version 6.20<sup>+</sup> / OEM AK-SM...

**System manager** AK-SM.... **/ Gateway**

#### **Display EKA 163 / 164**

**L < 15 m**

#### **L > 15 m**

4

**English**

### **Connections**

*[Figurtekst: Overview of outputs and · Application DO1 DO2 DO3 DO4 DO5 DO6 DI1 DI2 DI3 AI1 AI2 AI3 AI4 AI5 AI6 · applications. · 1 / • • • S3 S4 S5 S6 · See also electrical diagrams earlier in the instruction. 2 / Blinds • • • S3 S4 S5 S6 · 3 • • • S3 S4 S5 S6 · 4 suction hotgas • • • S3 S4 S5 S6 · 5 / heat • • • S3 S4 S5 S6 · 6 / B A • • • S3B S5B S3A S4 S5 S6 · 7 / • • • S3B S6B S3A S4 S5 S6A · 8 / B A • • • S3B S5B S3A S4 S5 S6 · 9 • • • S3 S4 S5 S6]*

#### **DI1**

Digital input signal.

The defined function is active when the input is short-circuited/ opened. The function is defined in o02.

#### **RJ45**

For data communication, but only if a TCP/IP module is inserted in the controller. (OEM)

#### **DI2**

Digital input signal.

The defined function is active when the input is short-circuited/ opened. The function is defined in o37.

#### **S3, S4, S5, S3B, S5B**

Pt 1000 ohm sensor or PTC 1000 ohm sensor. All have to be of the same type.

#### **S6, S6B**

#### **MODBUS**

For data communication. Terminal 56 = screen Terminal 57 = A+ Terminal 58 = B- (Alternatively the terminals can be connected to an external display type EKA 163A or 164A, but then they cannot be used for data communication. Any data communication must then be carried out by one of the other methods.)

Pt 1000 ohm

S3, air sensor, placed in the warm air before the evaporator S4, air sensor, placed in the cold air after the evaporator (the need for either S3 or S4 can be deselected in the configuration)

S5, defrost sensor, placed on the evaporator S6, product sensor

#### **Supply voltage**

230 V a.c., 50/60 Hz

#### **DO1**

Connection of solenoid valve or relay for compressor. The coil must be a 230 V a.c. coil.

#### **EKA Display**

If there is be external reading/operation of the controller, display type EKA 163B or EKA 164B can be connected.

#### **RS485 (terminal 51, 52, 53)**

For data communication, but only if a data communication module is inserted in the controller. The module can be a LON RS485, DANBUSS or a MODBUS. Terminal 51 = screen Terminal 52 = A (A+) Terminal 53 = B (B-) (For LON RS485 and gateway type AKA 245 the gateway must be version 6.20 or hi g her.)

#### **DO2**

Alarm

There is a connection between terminal 7 and 8 in alarm situations and when the controller is without power. Night blind There is connection between terminal 7 and 9 when the night blind is up/down.

Suction line valve There is connection between terminal 7 and 9 when the suction line must be open.

Rail heat

There is connection between terminal 7 and 8 when the function must be active.

5

#### **DO3**

Refrigeration, Rail heat, Heat function, Defrost 2

There is connection between terminal 10 and 11 when the function must be active.

#### **Data communication**

If data communication is used, it is important that the installation of the data communication cable is performed correctly. See separate literature No. RC8AC…

#### Heating element in drip tray

There is connection between terminal 10 and 11 when heating takes place.

#### **DO4**

#### Defrost

There is connection between terminal 12 and 14 when defrosting takes place.

#### **Hot gas / drain valve**

There is connection between terminal 13 and 14 during normal operation.

There is connection between terminal 12 and 14 when the hot gas valves must open.

#### **DO5**

#### Fan

There is connection between terminal 15 and 16 when the fan is on.

#### **DO6**

#### Light relay

There is connection between terminal 17 and 18 when the light must be on.

#### **DI3**

#### **Electric noise**

Cables for sensors, DI inputs and data communication **must** be kept separate from other electric cables:

- Use separate cable trays

- Keep a distance between cables of at least 10 cm

- Long cables at the DI input should be avoided

#### **Installation considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown.

Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation, for example, could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss wil not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer's responsibility to check the installation thoroughly, and to fit the necessary safety devices.

Special reference is made to the necessity of signals to the controller when the compressor is stopped and to the need of liquid receivers before the compressors.

Your local Danfoss agent will be pleased to assist with further advice, etc.

Digital input signal.

The signal must have a voltage of 0 / 230 V AC. The function is defined in o84.

*[Figurtekst: Coordinated defrost via  max. 10 · cable connections]*

The following controllers can be connected up in this way: EKC 204A, AK-CC 210, AK-CC 250, AK-CC 450, AK-CC 550,

Refrigeration is resumed when all controllers have “released” the signal for defrost.

Coordinated defrost via data communication

The setting of controllers to coordinate their defrosting takes place in the gateway/system manager.

Refrigeration is resumed when all controllers have “released” the signal for defrost.

6

### **Operation**

#### **Controller/Display**

The values will be shown with three digits, and with a setting you can determine whether the temperature is to be shown in °C or in °F.

#### **Light-emitting diodes (LED) on front panel**

The LED’s on the front panel will light up when the relevant relay is activated.

- = Refrigeration

- = Defrost

- = Fan running

The light-emitting diodes will flash when there is an alarm. In this situation you can download the error code to the display and cancel/accept for the alarm by giving the top button a brief push.

#### **The buttons**

When you want to change a setting, the upper and the lower buttons will give you a higher or lower value depending on the button you are pushing. But before you change the value, you must have access to the menu. You obtain this by pushing the upper button for a couple of seconds - you will then enter the column with parameter codes. Find the parameter code you want to change and push the middle button until value for the parameter is shown. When you have changed the value, save the new value by once more pushing the middle button.

#### Examples

#### Set menu

1. Push the upper button until a parameter r01 is shown

2. Push the upper or the lower button and find that parameter you want to change

3. Push the middle button until the parameter value is shown

4. Push the upper or the lower button and select the new value

5. Push the middle button again to set the value.

#### Cutout alarm relay / receipt alarm/see alarm code

- A short press of the upper button

If there are several alarm codes they are found in a rolling stack. Push the uppermost or lowermost button to scan the rolling stack.

#### Set temperature

1. Push the middle button until the temperature value is shown

#### **Get a good start**

With the following procedure you can start regulation very quickly:

- **1** Open parameter r12 and stop the regulation (in a new and not previously set unit, r12 will already be set to 0 which means stopped regulation.)

- **2** Select electrical connection based on the drawings on page 2 and 3

- **3** Open parameter o61 and set the electric connection number in it

|**4**Now select one of the<br>|preset|setting<br>|s from|the tabl|e<br>||
|---|---|---|---|---|---|---|
|Auxillary schedule for<br>k||**Case**|||**Room**||
|settings quic-setup|||||||
||Defrost<br>stop on<br>time|Defros<br>on|t stop<br>S5|Defrost<br>stop on<br>time|Defro<br>on|st stop<br>S5|
|**Preset settings**(o62)|**1**|**2**|**3**|**4**|**5**|**6**|
|Temperature (SP)|2°C|-2°C|-28°C|4°C|0°C|-22°C|
|Max. temp. setting (r02)|6°C|4°C|-22°C|8°C|5°C|-20°C|
|Min. temp. setting (r03)|0°C|-4°C|-30°C|0°C|-2°C|-24°C|
|Sensor signal for thermo-<br>stat. S4% (r15)<br>||100%|||0%||
|Alarm limit high (A13)|8°C|6°C|-15°C|10°C|8°C|-15°C|
|Alarm limit low (A14)|-5°C|-5°C|-30°C|0°C|0°C|-30°C|
|Sensor signal for alarm<br>funct.S4% (A36)<br>|0%||100%||0%||
|Interval between defrost<br>(d03)|6 h|6h|12h|8h|8h|6h|
|Defrost sensor: 0=time,<br>1=S5, 2=S4 (d10)|0|1|1|0|1|1|
|DI1 config. (o02)|Case c|leaning|(=10)|Door|function|(=2)|
|Sensor signal for display<br>view S4% (017)<br>Note: For applications 6 and 7 t<br>thermostat, alarm thermostat a|he sensor w<br>nd display r|eighting f<br>eadings a|0<br>or the S3/<br>s the sens|%<br>S4 sensors is<br>or uses are p|not used<br>redefined|for the<br>.|

   - **5** Open parameter o62 and set the number for the array of presettings. The few selected settings will now be transferred to the menu.

   - **6** Open parameter r12 and start the regulation

   - **7** Go through the survey of factory settings. The values in the grey cells are changed according to your choice of settings. Make any necessary changes in the respective parameters.

   - **8** For network. Set the address in o03

   - **9** Send address to system unit:

      - MODBUS: Activate scan function in system unit

      - If another data communication card is used in the controller:

      - LON RS485: Activate the function o04

2. Push the upper or the lower button and select the new value

3. Push the middle button again to conclude the setting.

Reading the temperature at defrost sensor (Or product sensor, if selected in o92.)

- A short press of the lower button

#### Manual start or stop of a defrost

- Push the lower button for four seconds.

7

### **Menu survey**

|<br>|||||||||||||||SW = 1.8x|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Parameter**<br>**Function**|Code|1<br>|2|**EL-dia**<br>3<br>|**g**<br>4|**ram p**<br>5|**age**<br>6|**or 3**<br>7|<br>8||9|**Min.-**<br>**value**|**Max.-value**|<sup>**Factory**</sup><br>**setting**|**Actual**<br>**setting**|
|**Normal operation**||||||||||||||||
|Temperature (setpoint)|- - -|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|2||
|**Thermostat**<br>f||||||||||||||||
|Differential|r01|1<br>|1|1<br>|1|1|1|1||1|1|0.1 K|20 K|2||
|Max. limitation of setpoint setting|r02|1<br>|1|1<br>|1|1|1|1||1|1|-49°C|50°C|50||
|Min. limitation of setpoint setting|r03|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|49°C|-50||
|Adjustment of temperature indication|r04|1<br>|1|1<br>|1|1|1|1||1|1|-10|10|0||
|Temperature unit (°C/°F)|r05|1<br>|1|1<br>|1|1|1|1||1|1|0/°C|1/F|0/°C||
|Correction of the signal from S4|r09|1<br>|1|1<br>|1|1|1|1||1|1|-10 K|10 K|0||
|Correction of the signal from S3|r10|1<br>|1|1<br>|1|1|1|1||1|1|-10 K|10 K|0||
|Manual service, stop regulation, start regulation (-1, 0, 1)|r12|1<br>|1|1<br>|1|1|1|1||1|1|-1|1|0||
|Displacement of reference during night operation|r13|1<br>|1|1<br>|1|1|1|1||1|1|-50 K|50 K|0||
|Define thermostat function<br>1=ON/OFF, 2=Pulse width modulating(PWM)|r14|1<br>|1|1<br>|1|1|1|1||1|1|1|2|1||
|Definition and weighting, if applicable, of thermostat sensors -<br>S4% (100%=S4,  0%=S3)|r15|1<br>|1|1<br>|1|1|||||1|0 %|100 %|100||
|Time between melt periods|r16|1<br>|1|1<br>|1|1|1|1||1|1|0 hrs|10 hrs|1||
|Duration of melt periods|r17|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|30 min.|5||
|Temperature setting for thermostat band 2. As differential use<br>|r21|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|2||
|r01 for application 1-8. R93 for application 9||||||||||||||||
|Correction of the signal fromS3B|r53||||||1|1||1||-10 K|10 K|0||
|Correction of the signal fromS6|r59|1<br>|1|1<br>|1|1|1|1||1|1|-10 K|10 K|0||
|<br>Correction of the signal fromS6B|r60|||||||1||||-10 K|10 K|0||
|Definition and weighting, if applicable, of thermostat sensors<br>when night cover is on.  (100%=S4,  0%=S3)|r61|1<br>|1|1<br>|1|1|||||1|0 %|100 %|100||
|Heat function<br>Neutral zone between refrigeration and heat function|r62|||||1||||||0 K|50 K|2||
|Time delay at switch between refrigeration and heat<br>function|r63|||||1||||||0 min.|240 min.|0||
|<br>Differential for thermostat band 2|r93||||||||||1|0.1|20 K|2 K||
|**Alarms**||||||||||||||||
|Delay for temperature alarm|A03|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|30||
|Delay for door alarm|A04|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|60||
|Delay for temperature alarm after defrost|A12|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|90||
|High alarm limit for thermostat 1|A13|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|8||
|Low alarm limit for thermostat 1|A14|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|-30||
|High alarm limit for thermostat 2|A20|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|8||
|L l liit f thtt 2||||||||||||°|°|||
|ow aarm m or ermosa|A21|1<br>||1<br>|1|1|1|1|||1|-50C|50C|-30||
|High alarm limit for sensor S6 at thermostat 1|A22|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|8||
|Low alarm limit for sensor S6 at thermostat 1|A23|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|-30||
|High alarm limit for sensor S6 at thermostat 2|A24|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|8||
|Low alarm limit for sensor S6 at thermostat 2|A25|1<br>|1|1<br>|1|1|1|1||1|1|-50°C|50°C|-30||
|S6 alarm time delay|A26|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|240||
|<br>With setting= 240 the S6 alarm will be omitted||||||||||||||||
|<br>Alarm time delay or signal on the DI1 input|A27|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|30||
|Alarm time delay or signal on the DI2 input|A28|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|30||
|Signal for alarm thermostat. S4% (100%=S4, 0%=S3)|A36|1<br>|1|1<br>|1|1|||||1|0 %|100 %|100||
|Delay for S6 (product sensor alarm) after defrost|A52|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|240 min.|90||
|<br>Delayfor S3B alarm during normal regulation|A53|||||||1||1||0 min.|240 min.|90||
|**Compressor**||||||||||||||||
|Min. ON-time|c01|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|30 min.|0||
|Min. OFF-time|c02|1<br>|1|1<br>|1|1|1|1||1|1|0 min.|30 min.|0||
|Time delay for cutin of comp.2|c05|||1|||||||1|0 sec|999 sec|5||
|Step Mode 1= Sequential, 2=Cyclic|c08|||1||||||||1|2|2||
|Comp.2 run in thermostat band 2<br>0: no<br>1|c85||||||||||1|0|1|0||
|:yes<br>Comp. on time when sensor fault|c86||||||||||1|0 min|240 min|15||

8

|**Continued**|**code**|**1**|**2**|**3**<br>**4**|**5**|<br>**6**|**7**|**8**|**9**|**Min.**|**Max.**|**Fac.**|**Actual**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Comp. off time when sensor fault|c87||||||||1|0 min|240 min|30||
|f<br>**Defrost**||||||||||||||
|Defrost method: 0=none, 1= EL,  2= Gas, 3 = Brine|d01|1|1|1<br>1|1|1|1|1|1|0/No|3/bri|1/EL||
|Defrost stop temperature|d02|1|1|1<br>1|1|1|1|1|1|0°C|50°C|6||
|Interval between defrost starts<br>|d03<br>|1|1|1<br>1|1|1|1|1|1|0 hrs/Off|f<br>240 hrs|8||
|Max. defrost duration|d04|1|1|1<br>1|1|1|1|1|1|0 min.|360 min.|45||
|Displacement of time on cutin of defrost at start-up|d05|1|1|1<br>1|1|1|1|1|1|0 min.|240 min.|0||
|Drip off time|d06|1|1|1<br>1|1|1|1|1|1|0 min.|60 min.|0||
|Delay for fan start after defrost|d07|1|1|1<br>1|1|1|1|1|1|0 min.|60 min.|0||
|Fan start temperature|d08|1|1|1<br>1|1|1|1|1|1|-50 °C|0 °C|-5||
|Fan cutin during defrost<br>0: stopped<br>1 Ri|d09|1|1|1<br>1|1|1|1|1|1|0|2|1||
|: unnng<br>2: Runningduring pumpdown and defrost||||||||||||||
|Defrost sensor:0 =Stop on time, 1=S5, 2=S4, 3=<br>(Alication 1-5 and 7: Both S5A and S6A|d10|1|1|1<br>1|1|1|1|1|1|0|3|0||
|pp       .<br>Application 6 and 8: individual S5A and S5B)||||||||||||||
|Pump down delay|d16|1|1|1<br>1|1|1|1|1|1|0 min.|60 min.|0||
|Drain delay  (used at hot gas defrost only)|d17|||1||||||0 min.|60 min.|0||
|Max. aggregate refrigeration time between two defrosts|d18|1|1|1<br>1|1|1|1|1|1|0 hrs|48 hrs|0/OFF||
|Heat in drip tray. Time from defrosting stops to heating in<br>the driptrayis switched off|d20|||1||||||0 min.|240 min.|30||
|f<br>Delay time before opening hot gas valve|d23|||1||||||0 min|60 min|0||
|Rail heat during defrost<br>f|d27|1|1||||1|1||0|2|2||
|0: off||||||||||||||
|1: on<br>2: Pulsing||||||||||||||
|Defrost stop temp. thermostat band 2|d28||||||||1|0°C|50°C|6||
|Max. defrost duration thermostat band 2|d29||||||||1|0 min|360 min|45||
|**Regulation parameter for refrigeration**||||||||||||||
|Period time at PWM|n63|1|1|1<br>1|1|1|1|1|1|30 sec.|900 sec.|300||
|Max. openingdegree at PWM|n64|1|1|1<br>1|1|1|1|1|1|0%|100%|100||
|Min. openingdegree at PWM|n65|1|1|1<br>1|1|1|1|1|1|0%|90%|0||
|Expert setting.  Windup at PWM|n66|1|1|1<br>1|1|1|1|1|1|0.2|1.0|1.0||
|<br>Expert setting. Kp at PWM|n67|1|1|1<br>1|1|1|1|1|1|0.5|10.0|4.0||
|Expert setting. Tn at PWM|n68|1|1|1<br>1|1|1|1|1|1|60 sec|1800 sec|300||
|**Fan**||||||||||||||
|Fan stop temperature (S5)|F04|1|1|1<br>1|1|1|1|1|1|-50°C|50°C|50||
|Pulse operation on fans:  0=No pulse operation,  1=At<br>thermostat cuts out only,  2= Only at thermostat cut outs<br>duringnight operation|F05|1|1|1<br>1|1|1|1|1|1|0|2|0||
|Period time for fan pulsation (on-time + off-time)|F06|1|1|1<br>1|1|1|1|1|1|1 min.|30 min.|5||
|On-time in % of period time|F07|1|1|1<br>1|1|1|1|1|1|0 %|100 %|100||
|**Real time clock**||||||||||||||
|Six start times for defrost.<br>Setting of hours.<br>0=OFF|t01 -<br>t06|1|1|1<br>1|1|1|1|1|1|0 hrs|23 hrs|0||
|Six start times for defrost.<br>Setting of minutes.<br>0=OFF|t11 -<br>t16|1|1|1<br>1|1|1|1|1|1|0 min.|59 min.|0||
|Clock - Setting of hours|t07|1|1|1<br>1|1|1|1|1|1|0 hrs|23 hrs|0||
|Clock - Setting of minute|t08|1|1|1<br>1|1|1|1|1|1|0 min.|59 min.|0||
|Clock - Setting of date|t45|1|1|1<br>1|1|1|1|1|1|1 day|31 day|1||
|<br>Clock - Setting of month|t46|1|1|1<br>1|1|1|1|1|1|1 mon.|12 mon.|1||
|Clock - Setting of year|t47|1|1|1<br>1|1|1|1|1|1|0year|99year|0||
|**Miscellaneous**||||||||||||||
|Delay of output signals after start-up|o01|1|1|1<br>1|1|1|1|1|1|0 sec|600 sec|5||
|<br>Input signal on DI1. Function:|o02|1|1|1<br>1|1|1|1|1|1|0|15|0||
|0=not used. 1=status on DI1. 2=door function with alarm<br>when open. 3=door alarm when open. 4=defrost start (pulse-<br>signal).  5=ext.main switch. 6=night operation 7=Thermostat<br>band changeover(activate r21). 8=alarm function when<br>closed. 9=alarm function when open. 10=case cleaning (pulse||||||||||||||
|signal). 11=forced cooling at hot gas defrost,12=night cover.<br>15=application shutdown||||||||||||||

9

|**Continued**|||**Code**|**1**|**2**|<br>**3**||**4**|**5**|**6**|**7**|**8**|**9**|**Min.**|**Max.**|**Fac.**|**Actual**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Network address (0= off)|||o03|1|1||1|1|1|1|1|1|1|0|240|0||
|On/Off switch (Service Pin message)<br>IMPORTANT! o61**must**be set prior to o04<br>(used at LON 485 only)|||o04|1|1||1|1|1|1|1|1|1|0/Off|1/On|0/Off||
|Access code 1 (all settings)|||o05|1|1||1|1|1|1|1|1|1|0|100|0||
|Used sensor type: 0=Pt1000,  1=Ptc1000,|||o06|1|1||1|1|1|1|1|1|1|0/Pt|1/Ptc|0/Pt||
|Software Version|||o08|1|1||1|1|1|1|1|1|1|100|999|||
|Max hold time after coordinated defrost|||o16|1|1||1|1|1|1|1|1|1|0 min.|360 min.|20||
|Select signal for display view.  S4% (100%=S4, 0%=S3)|||o17|1|1||1|1|1|||||0 %|100 %|100||
|Input signal on DI2. Function:<br>(0=not used. 1=status on DI2. 2=door function with alarm<br>when open. 3=door alarm when open. 4=defrost start (pulse-<br>signal).  5=ext. main switch 6=night operation 7=Thermostat<br>band changeover(activate r21). 8=alarm function when<br>closed. 9=alarm function when open. 10=case cleaning (pulse<br>signal). 11=forced cooling at hot gas defrost.). 12=night cover,<br>13=coordinated defrost). 15=application shutdown|||o37|1|1||1|1|1|1|1|1|1|0|15|0||
|Configuration of light function: 1=Light follows day /night<br>operation,  2=Light control via data communication via<br>‘o39’,  3=Light control with a DI-input,  4=As "2", but light<br>switch on and night cover will open if the network cut out|||o38|1|1||1|1|1|1|1|1|1|1|4|1||
|<br>for more than 15 minutes.||||||||||||||||||
|Activation of light relay (only if o38=2)On=light|||o39|1|1||1|1|1|1|1|1|1|0/Off|1/On|0/Off||
|Rail heat On time during day operations|||o41|1|1||||||1|1||0 %|100 %|100||
|Rail heat On time during night operations|||o42|1|1||||||1|1||0 %|100 %|100||
|Rail heat period time (On time + Off time)|||o43|1|1||||||1|1||6 min.|60 min.|10||
|Case cleaning. 0=no case cleaning. 1=Fans only. 2=All output<br>Off.|*|**|o46|1|1||1|1|1|1|1|1|1|0|2|0||
|f<br>Selection of  EL diagram. See overview page 2 and 3|*||o61|1|1||1|1|1|1|1|1|1|1|8|1||
|Download a  set of predetermined settings. See overview page<br>15|*||o62|1|1||1|1|1|1|1|1|1|0|6|0||
|Access code 2 (partial access)|*|**|o64|1|1||1|1|1|1|1|1|1|0|100|0||
|Replace the controllers factory settings with the present set-<br>tings|||o67|1|1||1|1|1|1|1|1|1|0/Off|1/On|0/Off||
|Input signal on DI3. Function:<br>(0=not used. 1=status on DI2. 2=door function with alarm<br>when open. 3=door alarm when open. 4=defrost start (pulse-<br>signal).  5=ext. main switch 6=night operation,7=Thermostat<br>band changeover(activater21). 8=Not used. 9=Not used.<br>10=case cleaning (pulse signal). 11=forced cooling at hot gas<br>defrost,12=night cover. 13=Not used. 14=Refrigeration|||o84|1|1||1|1|1|1|1|1|1|0|15|0||
|<br>stopped (forced closing)). 15= application shutdown||||||||||||||||||
|Rail heat control|||o85|1|1||||||1|1||0|2|0||
|0=not used, 1=pulse control with timer function (o41 and<br>o42), 2=pulse control with dewpoint function||||||||||||||||||
|Dew point value where the rail heat is minimum|||o86|1|1||||||1|1||-10°C|50°C|8||
|Dew point value where the rail heat is 100% on|||o87|1|1||||||1|1||-9°C|50°C|17||
|Lowest permitted rail heat effect in %|||o88|1|1||||||1|1||0 %|100 %|30||
|Time delay from "open door” refrigeration is started|||o89|1|1||1|1|1|1|1|1|1|0 min.|240 min.|30||
|Fan operation on stopped refrigeration (forced closing):<br>0 = Stopped (defrosting permitted)<br>1= Running (defrosting permitted)<br>2=Stopped (defrosting not permitted)|||o90|1|1||1|1|1|1|1|1|1|0|3|1||
|<br>3= Running(defrostingnotpermitted)||||||||||||||||||
|Definition of readings on lower button:<br>1=defrost stop temperature,  2=S6 temperature,    3=S5_B<br>temperature. 4= Readout of S3B temperature|||o92|1|1||1|1|1|1|1|1|1|1|4|1||
|Display of temperature<br>1= 56 Air temeratre|||o97|1|1||1|1|1|1|1|1|1|1|2|1||
|u  pu<br>2= u36 product temperature||||||||||||||||||
|Light and night blinds defined<br>0: Light is switch off and night blind is open when the<br>main switch is off<br>1: Light and night blind is independent of main switch|||o98|1|1||1|1|1|1|1|1|1|0|1|0||

10

|**Continued**||**Code**|**1**<br>**2**|**3**<br>**4**|**5**<br>**6**|**7**|**8**<br>**9**|**Min.**|**Max.**|**Fac.**|**Actual**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Configuration of alarm relay<br>The alarm relay will be activated upon an alarm signal<br>from the following groups:<br>1 - High temperature alarms<br>2 - Low temperature alarms<br>4 - Sensor error<br>8 - Digital input is activated for alarm<br>16 - Defrost alarms<br>32 - Miscellaneous<br>The groups that are to activate the alarm relay must be set<br>by using a numerical value which is the sum of the groups<br>that must be activated.<br>(E.g. a value of 5 will activate all high temperature alarms<br>and all sensor errors)||P41|1|1|1<br>1|1|1|0|63|47||
|.<br>0 = Cancel relayfunction||||||||||||
|**Service**||||||||||||
|Temperature measured with S5 sensor||u09|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on DI1 input. on/1=closed||u10|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Actual defrost time (minutes)||u11|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Temperature measured with S3 sensor||u12|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on night operation (on or off) 1=on||u13|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Temperature measured with S4 sensor||u16|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Thermostat temperature||u17|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Run time of thermostat (cooling time) in minutes||u18|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Temperature measured with S6 sensor<br>(product temperature)||u36|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on DI2 output. on/1=closed||u37|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Air temperature. Weighted  S3 + S4||u56|1<br>1|1<br>1|1||1|||||
|Measured temperature for alarm thermostat||u57|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on relay for cooling|**|u58|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on relay for fan|**|u59|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on relay for defrost|**|u60|1<br>1|1|1<br>1|1|1<br>1|||||
|Status on relay for rail heat|**|u61|1<br>1|||1|1|||||
|Status on relay for alarm|**|u62|1|1|1<br>1|1|1|||||
|Status on relay for light|**|u63|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on relay for valve in suction line|**|u64||1||||||||
|Status on relay for compressor 2|**|u67||1|||1|||||
|Temperature measured with S5B sensor||u75|||1||1|||||
|Temperature measured with S3B sensor||u76|||1|1|1|||||
|Temperature measured with S6B sensor||u79||||1||||||
|Status on relay for hotgas- / drain valve|**|u80||1||||||||
|Status on relay for heating element in drip tray|**|u81||1||||||||
|Status on relay fornight blinds|**|u82|1|||||||||
|Status on relay for defrostB|**|u83|||1||1|||||
|Status on relay for heat function|**|u84|||1|||||||
|Readout of the actual rail heat effect||u85|1<br>1|||1|1|||||
|1: Thermostat 1 operating,   2: Thermostat 2 operating||u86|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Status on high voltage input DI3||u87|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Readout of thermostats actual cut in value||u90|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Readout of thermostats actual cut out value||u91|1<br>1|1<br>1|1<br>1|1|1<br>1|||||
|Readout the brine PWM OD%||U02|1<br>1|1<br>1|1<br>1|1|1<br>1|||||

*) Can only be set when regulation is stopped (r12=0)

**) Can be controlled manually, but only when r12=-1

***) With access code 2 the access to these menus will be limited

##### **Forced control**

If you need to force-control an output, you should set r12 to -1 (manual mode). You should then select the relevant relay function, e.g. u58. Go to the function by pressing the middle button. Select On.

##### **Factory setting**

If you need to return to the factory-set values, it can be done in this way:

- Cut out the supply voltage to the controller

- Keep upper and lower button depressed at the same time as you reconnect the supply voltage

Factory settings are indicated for standard units. Other code numbers have customized settings.

11

#### **Fault messa** **g e**

|In an error situation the L     l<br>will be activated. If you p<br>the alarm report in the di<br>There are two kinds of err<br>during the daily operatio<br>A-alarms will not become<br>E-alarms, on the other ha<br>occurs.<br>(An A alarm will not be vi<br>Here are the messages th|ED’s on the front will flash and the a<br>ush the top button in this situation<br>splay.<br>or reports - it can either be an alarm<br>n, or there may be a defect in the in<br>visible until the set time delay has<br>nd, will become visible the moment<br>sible as long as there is an active E a<br>at may appear:|l   larm relay<br>you can see<br>occurring<br>stallation.<br>expired.<br>the error<br>larm).|
|---|---|---|
|**Code / Alarm text via**<br>**data communication**|**Description**|**Alarm**<br>**relay**<br>**groups**<br>**(P41)**|
|A1/---  High t.alarm|High temperature alarm|1|
|A2/---  Low t. alarm|Low temperature alarm|2|
|A4/--- Door alarm|Door alarm|8|
|A5/--- Max hold time|The ”o16” function is activated<br>duringa coordinated defrost|16|
|A13/--- High temp S6|Temperature alarm. High S6|1|
|A14/--- Low temp S6|Temperature alarm. Low S6|2|
|A15/--- DI1 alarm|DI1 alarm|8|
|A16/--- DI2 alarm|DI2 alarm|8|
|A45/--- Standby mode|Standby position (stopped<br>refrigeration via r12 or DI input)|-|
|A59/--- Case clean|Case cleaning. Signal from DI<br>input|-|
|A70/--- HighTemp.S3B|Temperature alarm. High S3B|1|
|A71/--- Low Temp.S3B|Temperature alarm. Low S3B|2|
|A72/--- HighTemp.S6B|Temperature alarm. High S6B|1|
|A73/--- Low Temp.S6B|Temperature alarm. Low S6B|2|
|E1/---  Ctrl. error|Faults in the controller|32|
|E6/--- RTC error|Check clock|32|
|E25/--- S3 error|Error on S3 sensor|4|
|E26/--- S4 error|Error on S4 sensor|4|
|E27/--- S5 error|Error on S5 sensor|4|
|E28/--- S6 error|Error on S6 sensor|4|
|E34/--- S3 error B|Error on S3B sensor|4|
|E37/--- S5 error B|Error on S5B sensor|4|
|E38/--- S6 error B|Error on S6B sensor|4|
|---/--- Max Def.Time|Defrost stopped based on<br>time instead of, as wanted, on|16|
|**Data communication**<br>The importance of individ    i<br>settingmust be carried o|temperature<br>ual alarms can be defined with a se<br>ut in thegroup"Alarm destinations"|i   tting. The<br>|
|Settings from<br>System manager AK-SM|Settings from<br>AKM (AKM destination)<br>S<br>N|end via<br>etwork|
|<br>High<br>|<br>1<br>|X<br>|
|Middle|2|X|
|Low<br>|3|X|
|Log only<br>Disabled|||

|**Operating status**||**(Measure-**<br>**ment)**|
|---|---|---|
|The controller goes through some regulating situ-<br>ations where it is just waiting for the next point<br>of the regulation. To make these “why is nothing<br>happening” situations visible, you can see an op-<br>erating status on the display. Push briefly (1s) the<br>upper button. If there is a status code, it will be<br>shown on the display. The individual status codes<br>have the followingmeanings:||Ctrl. state:<br>(Shown in<br>all menu<br>displays)|
|Normal regulation|S0|0|
|Waitingfor end of the coordinated defrost|S1|1|
|When the compressor is operating it must run for<br>at least x minutes.|S2|2|
|When the compressor is stopped, it must remain<br>stopped for at least x minutes.|S3|3|
|The evaporator drips off and waits for the time to<br>run out|S4|4|
|Refrigeration stopped by main switch. Either with<br>r12 or a DI-input|S10|10|
|Refrigeration stopped bythermostat|S11|11|
|Defrost sequence. Defrost inprogress|S14|14|
|Defrost sequence. Fan delay — water attaches to<br>the evaporator|S15|15|
|Refrigeration stopped due to open ON input or<br>stopped regulation|S16|16|
|Door is open. DI input is open|S17|17|
|Melt function in progress. Refrigeration is inter-<br>rupted|S18|18|
|Modulatingthermostat control|S19|19|
|Emergencycoolingdue to sensor error *)|S20|20|
|Manual control of outputs|S25|25|
|Case cleaning|S29|29|
|Forced cooling|S30|30|
|Delayon outputs duringstart-up|S32|32|
|Heat function r36 is active|S33|33|
|Case shut down|S45|45|
|Other displays:|||
|The defrost temperature cannot be displayed.<br>There is stopbased on time|non||
|Defrost in progress / First coolingafter defrost|-d-||
|Password required.  Set password|PS||
|Regulation is stopped via main switch|OFF||

*) Emergency cooling will take effect when there is lack of signal from a defined S3 or S4 sensor. The regulation will continue with a registered average cutin frequency. There are two registered values – one for day operation and one for night operation.

**Additional information: Manual RS8EU**

12
