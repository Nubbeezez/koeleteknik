# Danfoss Optyma Control AK-RC 101 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## OPTYMA TM Control Single-phase AK-RC 101 – Table of contents Page

*Kilde: Danfoss-dokument BC164886433666en-000501.pdf*

### **OPTYMA**<sup>**TM**</sup> **Control Single-phase** AK-RC 101

|**Table of contents**|**Page**|
|---|---|
|**General**......................................................................................................................................................|...............................................3|
|Description ..........................................................................................................................................|...............................................3|
|Applications ........................................................................................................................................|...............................................3|
|Main characteristics .........................................................................................................................|...............................................3|
|**Overall dimensions**.............................................................................................................................|...............................................3|
|**Identification data**...............................................................................................................................|...............................................4|
|**Installation**..............................................................................................................................................|...............................................4|
|Important information for the installer ....................................................................................|...............................................4|
|Standard assembly kit .....................................................................................................................|...............................................4|
|Installing the unit ..............................................................................................................................|...............................................5|
|**Functions**.................................................................................................................................................|...............................................7|
|**Technical characteristics of OPTYMA**<sup>**TM**</sup>**Control, single-phase**.......................................|...............................................7|
|**Control panel**.........................................................................................................................................|...............................................8|
|Front keypad .......................................................................................................................................|...............................................8|
|LED Display..........................................................................................................................................|...............................................9|
|General .................................................................................................................................................|...............................................9|
|Symbols used .....................................................................................................................................|...............................................9|
|Setting and displaying the set points ........................................................................................|...............................................9|
|Level 1 - Programming (User Level)............................................................................................|............................................ 10|
|List of Level 1 variables (User Level) ...........................................................................................|............................................ 10|
|Level 2 - Programming (Installer Level).....................................................................................|............................................ 11|
|List of Level 2 variables (Installer Level) ....................................................................................|............................................ 11|
|Switching on the OPTYMA<sup>TM</sup>Control single-phase ..............................................................|............................................ 12|
|Compressor activation/deactivation conditions ...................................................................|............................................ 12|
|Manual defrosting ............................................................................................................................|............................................ 12|
|Hot-gas defrosting ...........................................................................................................................|............................................ 13|
|Pump-down function ......................................................................................................................|............................................ 13|
|Password function ............................................................................................................................|............................................ 13|
|**Alarm relay**..............................................................................................................................................|............................................ 14|
|**Trouble shooting / Alarm list**..........................................................................................................|............................................ 15|
|**Connection diagrams**.........................................................................................................................|............................................ 16|
|**Parts list**....................................................................................................................................................|............................................ 18|
|**Ordering**...................................................................................................................................................|............................................ 19|

2

##### **General**

##### **Description**

The OPTYMA<sup>TM</sup> Control single-phase is a new control panel for cold rooms with a single-phase compressor up to 2 HP, specially designed for safety, protection, control and ease of installation.

It allows the user to control all the components on a refrigeration system: compressor, evaporator fans, defrosting elements, room light and thermostatholder.

##### **Main characteristics**

- Direct control of defrosting elements, evaporator fans, room light with outputs directly connectable to the various units.

- Automatic fuse protect the refrigeration unit.

- Stylish ABS housing with transparent cover for access to the automatic fuse, all with an IP65 protection rating so that panel can be used outside the room.

##### **Applications**

- Complete management of single-phase static or ventilated refrigeration systems up to 2 HP, with off-cycle or electrical defrosting and with direct or pump-down compressor stop.

- Control of single-phase evaporator unit only with solenoid valve or remote condensing unit.

- LED indicators and large display show system status.

- User-friendly keypad.

- Display resolution to 0.1 °C.

- Modbus data communication that can be connected to an ADAP-KOOL® system unit.

##### **Overall dimensions**

Dimensions in mm.

3

##### **Identification data**

The unit described in this manual has an ID label on the side showing all the relevant identification data:

- Name of Manufacturer

- Type and code number

- Product name

- Power supply

- Serial number (10 digits)

- Date (Day/Month/Year)

##### **Installation**

##### **Important information for the installer. Installation to be done by authorised person only!**

1. Install the device in places where the protection rating is observed and try not to damage the housing when drilling holes for wire penetrations

2.  Do not use multi-polar cables which have wires connected to inductive/power loads and signalling wires (e.g. sensors and digital inputs).

3.  Do not fit power supply wiring and signal wiring (sensors and digital inputs) in the same raceways or ducts.

4.  Minimise the length of connector wires so that wiring does not twist into a spiral shape as this could have a detrimental effect on the electronics.

5.  Fit a general protection fuse before the electronic controller.

6.  All wiring must be of a diameter suitable for relevant power levels.

7.  If a sensor extension is required, the wires must have a diameter of at least 1 mm<sup>2</sup> .

8.  If data communication is used, it is important that the data communication cable is correctly installed. See separate literature, no. RC8AC...

9. If data communication is used, the alarm relay cannot be used.

##### **Standard assembly kit**

For the purposes of assembly and use, the electronic OPTYMA<sup>TM</sup> Control single-phase unit comes with:

- Three rubber washers, to be fitted between the fixing screws and the housing back panel

- One user’s manual.

- Two temperature sensors

4

##### **Installing the unit**

##### **1.**

Lift the transparent cover.

Remove the screw cover on the right-hand side of the housing.

##### **2.**

Undo the 4 fixing screws at the front of the housing.

##### **3.**

Open the front of the housing, lift it and slide the two hinges out as far as they will go.

##### **4.**

Press on the sides of the hinges to remove them from their seats and then remove the front panel completely.

5

##### **5.**

Use the three existing holes to fix the housing back panel to the wall: use three screws of a suitable length for the thickness of the wall on which the panel will be mounted. Fit a rubber washer (supplied) between each screw and the housing back panel.

##### **6.**

Hook the front panel back up to the lower part of the housing by inserting the two hinges in their seats and, bending them, rotate downwards 180° to gain access to the electronic board.

If Modbus data communication is connected, see the JUMPER setting on page 14, preferably before all the wiring is connected.

##### **NOTE !**

**Make all the electrical connections as illustrated in the diagram for the corresponding model (see drawing on page 16).**

**To effect correct electrical connection and maintain the protection rating, use appropriate wire/ raceway grips to ensure a good seal.**

**Route the wiring inside the unit in as tidy a fashion as possible: be especially careful to keep power wires away from signal wires. Use clips to hold wires in place.**

##### **7.**

Close the front panel, making sure that all the wires are inside the housing  and that the housing  seal sits in its seat properly.

Tighten the front panel using the 4 screws, making sure the O-rings on the head of each screw are used. Power up the panel and carry out thorough reading/programming of all the parameters.

##### **NOTE !**

**Be careful not to over-tighten the closure screws as this could warp the housing  and compromise proper operation of the membrane-type keypad.**

**Install short-circuit overload safety devices on all the power cables connected to the OPTYMA**<sup>**TM**</sup> **Control so as to prevent damage to the device. Work and/or maintenance must be carried out on the unit ONLY after disconnecting the panel from the power supply and from any inductive/power loads: doing so allows the worker to do his job safely.**

6

##### **Functions**

##### **OPTYMA**<sup>**TM**</sup> **Control single-phase:**

- Display and adjustment of cold room temperature setting to 0.1 °C

- Display of evaporator temperature from parameter

- System control activation/deactivation

- System warnings (probe/sensor errors, minimum and maximum temperature warnings, compressor shutdown)

- Evaporator fans control

- Automatic and manual defrost (static, heating element, cycle inversion)

- Direct control of compressor unit up to 2 HP

- Room light, via panel key or door switch

- Alarms/auxiliary relay

- Defrosting, lights and alarms can be operated via data communication.

##### **Technical characteristics of OPTYMA**<sup>**TM**</sup> **Control single-phase**

|**Power supply**||
|---|---|
|Voltage|230 V~ ± 10% 50Hz/60Hz|
|Power consumption(electronics only)|~ 7 VA|
|**Cold room conditions**||
|Operatingtemperature|-5 to 50°C|
|Storage temperature|-10 to 70°C|
|Relative humidity|Less than 90% -<br>Not condensed. No shock influence/vibration.|
|**General characteristics**||
|Type of sensors|EKS 221,code no.: 084N3210|
|Resolution|0.1 °K|
|Sensor readprecision|± 0.5 °K|
|Read range|-45…+45 °C|
|**Digital inputs**||
|Requirements to contact|Goldplating|
|**OPTYMA**<sup>**TM**</sup>**Control single-phase - Output chara**<br>|**cteristics - max. applicable load(230 V AC)**<br>|
|Compressor|1500W(AC3)|
|Defrost|3000W(AC1)|
|Fans|500W(AC3)|
|Room light|800W(AC1)|
|Alarm contact(non-powered contact)|100W|
|General electrical protection|Automatic fuse 16A<br>Id=300 mA|
||Disconnecting power 4.5 kA|
|**Dimensions**||
|Dimensions|168 mm x 97 mm x 262 mm(HxPxL)|
|**Insulation/ mechanical characteristics**||
|Housing protection rating|IP65|
|Housingmaterial|Self-extinguishingABS|
|Type of insulation|Class II|

###### **Capacitive load**

The relays cannot be used for the direct connection of capacitive loads such as LEDs and on/off control of EC motors. All loads with a switch mode power supply must be connected with a suitable contactor or similar.

7

##### **Control Panel**

##### **Front keypad**

##### **AUXILIARY RELAY CONTROL**

(on the version with alarm relay controls the relay manual if parameter AU=1)

**UP / MUTE WARNING BUZZER**

**STAND BY**

(The LED flashes if the system shuts down)

**Room temperature SETTING / SET key**

**DOWN / MANUAL DEFROST**

**ROOM LIGHT**

8

##### **LED Display**

1. Cold room temperature / parameters

2. Stand-by (flashes on stand-by). Outputs are deactivated

3. Room light (flashes if door switch activated)

4. Cold (indicates activation of compressor)

5. Fans

6. Defrosting

7. Auxiliary

8. Alarm/warning

##### **General**

To enhance safety and simplify the operator’s work, the OPTYMA<sup>TM</sup> Control has two programming levels; the first level (Level 1) is used to configure the frequently-modified SETPOINT parameters. The second programming level (Level 2) is for general parameter programming of the various controller work modes.

It is not possible to access the Level 2 programming directly from Level 1: you must exit the programming mode first.

##### **Symbols used**

For practical purposes the following symbols are used:

- (▲) the UP key is used to increase values and mute the alarm.

- (▼) the DOWN key is used to decrease values and force defrosting.

##### **Setting and displaying the setpoints**

1. Press the SET key to display the current SETPOINT (temperature)

2. Hold down the SET key and press the (▲) or (▼) keys to modify the SETPOINT.

Release the SET key to return to cold room temperature display: the new setting will be saved automatically.

9

##### **Level 1 - Programming (User Level)**

To gain access to the Level 1 configuration menu proceed as follows:

1. Press the (▲) and (▼) keys simultaneously and keep them pressed for a few seconds until the first programming variable appears on the display.

When configuration values have been set, you can exit the menu by pressing the (▲) and (▼) keys simultaneously for a few seconds until the cold room temperature reappears.

   5.  The new settings are saved automatically when you exit the configuration menu.

2. Release the (▲) and (▼) keys.

3. Select the variable to be modified using the (▲) and (▼) key.

4.  When the variable has been selected it is

- possible to:

- display the setting by pressing the SET key

- modify the setting by pressing the SET key

- together with the (▲) and (▼) key.

##### **List of Level 1 variables (User Level)**

|**Variables**|**Explanation**|**Value**|**Default**|
|---|---|---|---|
|**r0**|**Differential**above main SETPOINT*<br>* SETPOINT seepage 9|0.2 - 10 K|2K|
|**d0**|**Defrost interval (hours)**|0 - 24 hours|4 hours|
|**d2**|**End-of-defrost setpoint.**<br>Defrosting will not take place if the temperature detected by the defrost<br>sensor isgreater than d2 (If the sensor is faultydefrostingis timed)|-35 - 45 °C|15°C|
|**d3**|**Max defrost duration**(minutes)|1 - 240 min|25 min|
|**d7**|**Drip duration**(minutes)<br>At the end of defrost, the compressor and fans remain at standstill for time<br>d7 and the defrost LED on the frontpanel flashes.|0 - 10 min|0 min|
|**F5**|**Fan pause**after defrost (minutes)<br>Allows fans to be kept at standstill for time F5 after dripping. This time<br>begins at the end of dripping. If no dripping has been set, the fan pause<br>starts directlyat the end of defrost.|0 - 10 min|0 min|
|**A1**|**Minimum temperature alarm**<br>Allows user to define a minimum temperature for the room being<br>refrigerated. Below value A1 an alarm trips: the alarm LED flashes, the<br>displayed temperature flashes and the buzzer sounds to indicate the<br>problem.|-|-45°C|
|**A2**|**Maximum temperature alarm**<br>Allows user to define a maximum temperature for the room being<br>refrigerated. Above value A2 an alarm trips: the alarm LED flashes, the<br>displayed temperature flashes and the buzzer sounds to indicate the<br>problem.|-|+45°C|
|**tEu**|**Evaporator sensor temperature display**|Displays<br>evaporator<br>temperature<br>(displays<br>nothing if<br>dE =1)|read<br>only|

10

##### **Level 2 - Programming (Installer Level)**

To access the second programming level press the UP (▲) and DOWN (▼) keys and the LIGHT key simultaneously for a few seconds.

When the first programming variable appears the system automatically goes to stand-by.

1.  Select the variable to be modified by pressing the UP (▲) and DOWN (▼) keys. When the parameter has been selected it is

   2.  View the setting by pressing the SET key.

   3.  Modify the setting by holding the SET key down and pressing the (▲) or (▼) key.

   4.  When configuration settings have been completed you can exit the menu by pressing the (▲) and (▼) keys simultaneously and keep them pressed until the room temperature reappears.

   5.  Changes are saved automatically when you exit the configuration menu.

   6.  Press the STAND-BY key to enable electronic control.

- possible to:

**List of Level 2 variables (Installer Level)**

|**Variables**|**Explanation**|**Value**|**Default**|
|---|---|---|---|
|**AC**|**Door switch status**|0  =  normally open<br>1  =  normallyclosed|0|
|**F3**|**Fan status with compressor off**|0  =  fans run continuously<br>1  =  fans only run when<br>compressor is working|1|
|**F4**|**Fan pause during defrost**|0  =  fans run during defrost<br>1  =  fans do not run duringdefrost|1|
|**dE**|**Sensor presence**<br>If the evaporator sensor is disabled defrosts are<br>carried out cyclically with period d0: defrosting<br>ends when an external device trips and closes the<br>remote defrost contact or when time d3 expires.|0  =  evaporator sensor present<br>1  =  no evaporator sensor|0|
|**d1**|**Defrost type**, cycle inversion (hot gas) or with<br>heater elements|1 =  hot gas<br>0 =  electric|0|
|**bdr**|Modbus baudrate<br>(Danfoss System unit =19200 baud)|0=300. 1=600. 2=1200. 3=2400.<br>4=4800. 5=9600. 6=14400.<br>**7=19200**. 8=38400 baud.|7|
|**Ad**|Modbus address|1 ... 247<br>(+ setting: AU must be set to 7)<br>(+ movejumper: seepage 14)|0|
|**Ald**|**Minimum and maximum temperature**<br>Signallingand alarm displaydelay|1…240 min|120 min|
|**C1**|Minimum time between shutdown and<br>**subsequent switching on of the compressor**.|0…15 min|0 min|
|**CAL**|**Correction of sensor signal**|-10…+10|0|
|**Pc**|**Compressor protection contact status**|0 = NO<br>1 = NC|0 = NO|
|**doC**|**Compressor safety time for door switch**: when<br>the door is opened the evaporator fans shut down<br>and the compressor will continue working for time<br>doC, after which it will shut down.|0…5 minutes|0|
|**tdo**|**Restart time, if the door remains open**|0... 240 min. (0=no function)|0|
|**Fst**|**FAN shutdown TEMPERATURE**<br>The fans will stop if the temperature value read by<br>the evaporator sensor exceeds  this value.|-45…+45°C|+45°C|

11

|Continued...||||
|---|---|---|---|
|**Variables**|**Explanation**|**Value**|**Default**|
|**Fd**|**Fan differential below Fst**|0…+10K|2K|
|**LSE**|**Min. limit of setpoint setting**|-45...HSE|-45°C|
|**HSE**|**Max. limit of setpoint setting**|45... LSE|45°C|
|**tA**|**NO – NC**alarm relay switching|0 = activates when alarm is on<br>1 = deactivates when alarm is on|1|
|**AU**|**Auxiliary/alarm relay control**|0 = alarm relay<br>1 = manual auxiliary relay<br>controlled via AUX key<br>2 = automatic auxiliary relay<br>managed by StA temp. setting<br>with 2°C differential<br>3 = not used<br>4 =  pump-down function (see 5.15)<br>5 =  free voltage contact for<br>condensing unit (AUX relay and<br>compressor relay in parallel)<br>6 =  Relay used to control a heating<br>element in the crankcase.<br>The relay is on when the<br>compressor is stopped.<br>7 = The relay function is cancelled<br>and data communication is<br>permitted|0|
|**StA**|**Temp. setting for aux. relay**|-45…+45°C|0|
|**In1**|**Man in cold room alarm**<br>Select input INP1 on the board as compressor<br>protection alarm or as man-in-room alarm<br>(contact NC).|0  =  compressor protection<br>1  =  man-in-room alarm|0|
|**P1**|**Password type of protection**<br>( active when PA does not equal 0)|0  =  display set point only<br>1 =  display set point, AUX, light<br>access<br>2 =  access to programming not<br>permitted<br>3 =  access to second level<br> programmingnotpermitted|3|
|**PA**|**Password**<br>(see P1 for the type ofprotection)|0...999<br>0  =  not active|0|
|**reL**|**Software release**|The version can be read|-|

##### **Switching on the OPTYMA**<sup>**TM**</sup> **Control single-phase**

After wiring the electronic controller correctly, connect 230 V a.c.; the display panel will

immediately emit a beep and all the LEDs will come on simultaneously for a few seconds.

##### **Compressor activation/deactivation conditions**

The OPTYMA<sup>TM</sup> Control single-phase activates the compressor when cold room temperature exceeds

setting+differential (r0); it deactivates the compressor when the cold room temperature is lower than the setting.

##### **Manual defrosting**

To defrost just press the dedicated key (see page 8) to activate the elements relay. Defrosting will not take place if the end-of-defrost temperature setting (d2) is lower than the temperature detected by the

evaporator sensor. Defrosting ends when the endof-defrost temperature (d2) or maximum defrost time (d3) is reached.

When using data communication, the defrost cycle can be started from the system unit.

12

##### **Hot-gas defrosting**

Set parameter d1 =1 to defrost in cycle inversion mode.

The compressor relay and defrost relay are activated throughout the defrost phase. To ensure proper control of the system the installer must use the defrost output: this must allow

opening of the cycle inversion solenoid valve and closure of the liquid solenoid valve.

For capillary systems (without thermostat valve) the cycle inversion solenoid valve can be controlled via the defrost relay control.

##### **Pump-down function**

Pump-down function is activated when parameter AU=4 (for version with AUX/Alarm relay only). Connect pump-down pressostat on the digital input INP-1.

The compressor is directly controlled by pressostat. Connect evaporator solenoid valve on the AUX relay. The solenoid is controlled directly by the thermostat.

##### **Password function**

The protection function is activated when parameter PA is set to a value other than 0. See parameter P1 for the different protection types. When PA is set, protection starts after two

minutes of inactivity. 000 appears on the display. Use the up/down keys to change the number, and the set key to confirm it. If you have forgotten your password, use the universal number 100.

13

##### **Alarm relay  / Modbus**

Factory setting = The relay functions as an alarm relay.

When using data communication, a JUMPER must be moved.

See the following:

1. Open the front of the housing as described on page 5: rotate it downwards 180° to gain access to the electronic board.

2. Undo the 6 CPU board fixing screws: remove the board from the front part of the housing in ABS.

3. Remove the jumper from JUMPER JP2.

4. Insert the jumper in JUMPER JP2 in position: 3-2: to select data communication Modbus (2-1: is the alarm relay position).

14

##### **Trouble shooting / Alarm list**

In the event of any anomalies the OPTYMA<sup>TM</sup> Control warns the operator by displaying alarm codes and sounding the warning buzzer inside the control

panel. If an alarm is tripped the display will show one of the following messages.

|**Alarm code**|**Possible cause**|**Solution**|
|---|---|---|
|**E0**|Cold room temperature sensor not working<br>properly|• Check that cold room temperature sensor is<br>working properly<br>• If theproblempersists replace the sensor|
|**E1**|Defrost sensor not working properly<br>(In this case defrosts will last time d3)|• Check that defrost sensor is working<br>properly<br>• If theproblemspersists replace the sensor|
|**E2**|Eeprom alarm<br>An EEPROM memory alarm has been detected<br>(All outputs except the alarm one are<br>deactivated)|• Switch unit off and then back on again|
|**E8**|Man-in-room alarm|• Reset the alarm input inside the cold room|
|**Ec**|Compressor protection tripped (e.g. thermal<br>protection or max pressure switch)<br>(All outputs except the alarm one – where<br>applicable – are deactivated)|• Check that compressor is working properly<br>• Check compressor absorption<br>• If the problem persists contact the technical<br>assistance|
|**Ed**|Open door - alarm (Open door and tdo-time<br>has expired)|Check door / door contact|
|**Temperature**<br>**shown on**<br>**display is**<br>**flashing**|Minimum or maximum temperature alarm.<br>The temperature inside the cold room has<br>exceeded the min. or max. temperature<br>alarm setting (see variables**A1**and**A2**, user<br>programminglevel)|• Check that the compressor is working<br>properly.<br>• Sensor not reading temperature properly or<br>compressor start/stop control not working.|

15

##### **Connection diagram**

*[Figurtekst: Common · B B · Modbus A A · Defrost probe · Ambient probe · Common probe · Common dig. input · Door Limit Switch · Comp. Protection · Danfoss 80Z679.10 · 1816 1719 · 1415 · 11 1213 · Power  Supply 230Vac 910 · 62315748]*

16

##### **How to connect the OPTYMA**<sup>**TM**</sup> **Control single-phase to OPTYMA**<sup>**TM**</sup> **condensing unit**

*[Figurtekst: Danfoss80Z681.10 · Power · Supply · 230Vac · 9 10 11 12 13 14 15 16 17 18 19 · 1 2 3 4 5 6 7 8 · OPTYMA TM  Condensing unit · 1 2 N L · HP · P Condenser Compressor · fan · How to connect the OPTYMA TM  Control single-phase to OPTYMA PLUS TM  and SlimPack condensing unit · Danfoss80Z682.11 · Power · Supply · 230Vac · 9 10 11 12 13 14 15 16 17 18 19 · 1 2 3 4 5 6 7 8 · Connect Compr. Relay output to room thermostat input terminals of · OptymaPlus / SlimPack  (remove bridge before): · Term. 3-4  Optyma SlimPack · Term. 4-5  OptymaPlus Evo.2 H1 - H3 · Term. 5-6  OptymaPlus Evo.2 H4 · Term. 6-7  OptymaPlus Evo.2 230V-3Phase · Term. 24-25  OptymaPlus new Generation (DI1 of OptymaPlus Controller) · Modbus · Comp. Protection Door Limit Switch Common dig. input Common probe Ambient probe Defrost probe · A B · A B · Modbus · Comp. Protection Door Limit Switch Common dig. input Common probe Ambient probe Defrost probe A B · A B]*

##### **How to connect the OPTYMA**<sup>**TM**</sup> **Control single-phase to OPTYMA PLUS**<sup>**TM**</sup> **and SlimPack condensing unit**

17

##### **Parts list**

|**1**|Housingbackpanel in ABS|
|---|---|
|**2**|Housingfrontpanel in ABS|
|**3**|Front cover in transparentpolycabonate|
|**4**|Frontpanel openinghinge|
|**5**|Frontpanel closure screws|
|**6**|Board fixingscrews|
|**7**|Automatic fuse/ Cut out switch|
|**8**|CPU board|
|**9**|Polycarbonate screw cover|
|**10**|Terminal for earth connections|

18

##### **Ordering**

|**Type**|**Code no.**|
|---|---|
|**OPTYMA**<sup>**TM**</sup>**Control single-phase (2 HP)**|**Z2**|
|**including two sensors**|**080300**|
|**Sensor EKS 221 (spare part)**|**084N3210**|

19

#### **Notes**

20
