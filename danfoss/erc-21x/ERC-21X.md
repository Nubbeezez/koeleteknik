# Danfoss ERC 21X – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Electronic refrigeration control Type ERC 21X series

*Kilde: Danfoss-dokument BC194286421698en-001002.pdf*

**User Guide**

Electronic refrigeration control Type **ERC 21X** series

Smart multipurpose refrigeration controller

### **Contents**

|**Introduction**|**5**|
|---|---|
|Application|5|
|General description|5|
|ERC 21X series|5|
|ERC 211|5|
|ERC 213|6|
|ERC 214|6|
|**Functions**|**8**|
|Voltage protection|8|
|Compressor protection|8|
|Compressor protection against high condensing temperature|8|
|Reference displacement|9|
|Night mode|9|
|Fan cycling during compressor OFF cycle|10|
|Defrost on Demand|10|
|**Applications**|**11**|
|Pre-defined applications|11|
|ERC 211 controller|11|
|ERC 213 controller|11|
|ERC 214 controller|12|
|Electrical connection diagram|12|
|**Configuration**|**14**|
|Menu navigation and overview|14|
|Quick configuration at power up|14|
|Quick configuration via cFg menu|15|
|Factory resetting|17|
|Display codes|17|
|**Parameters**|**18**|
|Parameter description|18|
|Configuration|18|
|Thermostat|18|
|Alarm settings|19|
|Defrost|19|

|Fan|20|
|---|---|
|Compressor|20|
|Miscellaneous|21|
|Service|22|
|Parameters: ERC 211|22|
|Configuration|22|
|Reference|23|
|Alarm|23|
|Defrost|23|
|Compressor|24|
|Others|24|
|Polarity|24|
|Parameters: ERC 213|24|
|Configuration|24|
|Reference|25|
|Alarm|25|
|Defrost|25|
|Fan control|26|
|Compressor|26|
|Others|26|
|Polarity|27|
|Parameters: ERC 214|27|
|Configuration|27|
|Reference|27|
|Alarm|28|
|Defrost|28|
|Fan control|28|
|Compressor|29|
|Others|29|
|Polarity|29|
|Alarm code|30|
|**Product specification**|**31**|
|Technical specification|31|
|Mounting|31|
|Installation steps|32|
|Dimensions|32|
|Accessories|32|

|KoolKey (EKA200)|32|
|---|---|
|Mass Programming Key (EKA 201)|32|
|Bluetooth Adapter (EKA 202 & EKA 203)|33|
|**Ordering**|**34**|
|**Certificates, declarations, and approvals**|**35**|
|Certificates, declarations, and approvals|35|
|**Online support**|**36**|

### **Introduction**

### **Application**

ERC 21X is a smart multipurpose refrigeration controller designed to fulfill today’s requirement of commercial refrigeration applications. This controller is suitable for high, medium and low temperature applications with natural, electrical and hot gas defrost compatibilities.

Typical applications include Glass door merchandisers, commercial fridges and freezers, cold rooms and various other commercial refrigeration applications.

### **General description**

ERC 21X controller comes with four push buttons, a big display, easy and intuitive menu structure and pre-defined applications ensure ease of use. Controller is loaded with energy efficiency features like smart evaporator fan management, night mode and defrosts on demand features.

High capacity 16 A relay enable direct connection of heavy loads without use of intermediate relay: up to 2 hp compressors depending on its power factor and motor efficiency (power factor greater than 0.65 for 230 V and greater than 0.85 for 115 V).

Safe operation of the unit is ensured through voltage protection, zero cross switching and high condenser temperature protection features.

### **ERC 21X series**

Three version of ERC 21X is available in both 230 V AC, 50/60HZ and 115 V AC, 60Hz.

- ERC 211: single relay output for refrigeration and heating applications.

- ERC 213: three relays outputs for ventilated refrigeration and heating applications.

- ERC 214: four relays outputs for ventilated refrigeration and heating applications.

### ERC 211

ERC 211 has one relay output and two inputs (1 analogue, 1 analogue/digital). This controller can be used for either cooling or heating applications.

##### **Fi** **g ure 1: ERC 211**

*[Figurtekst: DI1 · Sair · DO1 · Sc]*

#### **Outputs:**

- Relay 1: compressor/solenoid valve control or simple heater in case of heating application.

#### **Inputs:**

- Input 1: control sensor (Sair).

- Input 2: condenser sensor or digital inputs that can be configured for various functions as mentioned under menu code o02.

### ERC 213

ERC 213 has three relays outputs and four inputs (2 analogues, 1 analogue/digital, 1 digital) for cooling and heating applications.

##### **Fi** **g ure 2: ERC 213**

*[Figurtekst: DI1 · DI2 · Sair · DO1 · S5 · DO2 · DO3 · Sc]*

#### **Outputs:**

- Relay 1: compressor/solenoid valve control or heater in case of heating applications

- Relay 2: can be configured defrost control or external alarm or cabinet light

- Relay 3: fan control

#### **Inputs:**

- Input 1: control sensor (Sair)

- Input 2: defrost sensor (S5)

- Input 3: condenser sensor (Sc) or digital input that can be configured for various functions as mentioned under menu code o02

- Input 4: digital input that can be configured for various functions as mentioned under menu code o37

### ERC 214

ERC 214 has four relays outputs and four inputs (2 analogue, 1 analogue/digital, 1 digital) for cooling applications.

*[Figurtekst: Fi g ure 3: ERC 214 · DI1 · DI2 · DO4 · Sair · DO1 · S5 · DO2 · DO3 Sc]*

#### **Outputs:**

- Relay 1: compressor/solenoid valve control

- Relay 2: defrost control, external alarm or cabinet light

- Relay 3: fan control

- Relay 4: this can be configured for either cabinet light or external alarm

#### **Inputs:**

- Input 1: control sensor (Sair)

- Input 2: defrost sensor (S5)

- Input 3: condenser sensor (Sc) or digital input that can be configured for various functions as metioned under menu code o02

- Input4: digital input that can be configured for various functions as mentioned under menu code o37

### **Functions**

### **Voltage protection**

The voltage protection ensures that the compressor motor is operating within safe voltage ranges. If the power supply voltage gets outside the specified high/low voltage cut-out ranges, the compressor is cut-out or restricted from starting. Normal compressor operation is resumed when the power supply voltage is back in the area between the high voltage cut-out limit and the low voltage cut-in limit.

##### **Fi** **g ure 4: Volta** **g e** **p rotection**

*[Figurtekst: H igh voltage limit · Lo w voltage cut-in · limit (compressor start) · Low voltage cut-out · li mit (alarm and · compressor stop)]*

### **Compressor protection**

Compressor protection feature protects compressor from short ON and OFF cycles by securing minimum run and stop time. This would allow the refrigeration system to stabilize before starting the compressor again and also avoid the chances of too many compressor cycles.

##### **Fi** **g ure 5: Com** **p ressor** **p rotection**

*[Figurtekst: min run time · ON · OFF · min stop time · time · CUT-IN · CUT-OFF · time · Power to com p ressor · Temerature p]*

### **Compressor protection against high condensing temperature**

If the condenser is blocking up with dirt and thereby reaches a too high condensing temperature, the controller will give the user early warning through condenser alarm and if temperature rises further, it will switch the compressor OFF. If the temperature measured by the condenser sensor (Sc) is reaching the set “pre-alarm limit” an alarm is raised, but no further action is taken. This is used to indicate to the user that something is wrong with the condenser. Often the reason is that that the air flow to the condenser is restricted (dirt) or because the condenser fan is broken.

The alarm will reset if the condenser temperature drops back by 5 °C. If the measured condenser temperature continues to increase and reaches the set “Block limit” the compressor is stopped, and it is restricted from starting again until the alarm is reset manually. The alarm can be reset manually by setting the parameter r12 Main switch to OFF position and back to ON position or by powering the controller down.

**Figure 6: Compressor protection against high condensing tem** **p erature**

*[Figurtekst: Sc temperature °C · Block limit · Pre alarm limit · Pre alarm OK · Manual reset · Sc temperature °C · Compressor · Pre alarm · Block alarm · T1    T2 T3    T4]*

### **Reference displacement**

This feature enable user to toggle between two different set-points quickly by activating a switch on digital input. This provides facility to switch between two storage temperatures without getting in to the menu. For example meat requires different set points than vegetables. The reference displacement signal changes the normal thermostat set-point and the alarm limits by a predefined reference displacement offset value (r40).

##### **Fi** **g ure 7: Reference dis** **p lacement**

*[Figurtekst: Thermostat ref. disp. · High alarm limit · Thermostat ref. disp. · Cut out · Low temp. alarm limit · Ref. displacement activated · Ref. displacement deactivated Ref. displacement deactivated · Time · Cabinet temp.]*

### **Night mode**

Night mode helps to reduce cooling load and thereby power consumption during non-business hours i.e., Night time. The thermostat set point will be offset by a fixed value during night mode keeping alarm limits same.

##### **Fi** **g ure 8: Ni** **g ht mode**

### **Fan cycling during compressor OFF cycle**

During compressor OFF cycle controller will run the fan with defined duty cycle to maintain uniform temperature and delay the need of compressor switching ON.

##### **Fi** **g ure 9: Fan c** **y cle**

*[Figurtekst: Thermostat cut in · Cabinet air temp. · Thermostat cut out · Fan · Fan ON Fan OFF · cycle cycle · Compressor]*

### **Defrost on Demand**

This feature records the evaporator temperature when it is clean and constantly monitors the compares that at every compressor cut outs. If the evaporator temperature goes below the recorded temperature by the value set in parameter d30 before the configured defrost interval, it will trigger defrost immediately.

- This function can only be used in 1:1 systems.

- This function is disabled when the parameter “d30” is set to 20.

- Defrost on demand is triggered only if the time since the last defrost session has ended is greater than ¼ of the defrost interval or 2 hours whichever is lesser.

- Defrost doesn’t start by this method during the following scenarios.

- Pull down mode

- Night mode

- Main switch in DI or main switch in Menu is in OFF position

- Manual control mode

- Evaporator temperature greater than 0 °C.

### **Applications**

### **Pre -** **def i** **ned applications**

The purpose of the pre-defined applications is to give the user an easy and fast way to configure the controller to a specific application based on storage temperature (LT, MT, HT), defrost type (none, natural, electrical) and defrost method (terminated on time or temperature).

When user select specific application based on their requirements, the controller will load a specific set of parameter values and will hide parameters that are not relevant for the selected application. Adjustment of the set of parameters value will be still possible at any time.

In addition to pre-defined applications, all controller versions have two standard applications, one with full list of parameters and another with simplified list of parameters, that allows the user to make their own customized parameter settings (AP0 and AP5 in case of ERC 211 and AP0 and AP6 in case of ERC 213 / ERC 214).

### ERC 211 controller

**Table 1: Pre-defined a** **pp lication table of ERC 211 controller**

|**APP**|**Description**<br>**Temp. range**|**Defrost end**|**DO1**|**AI1**|**DI1**<sup>**(1)**</sup>|
|---|---|---|---|---|---|
|AP0|Fully Configurable Standard Application (Cooling / Heating)|||||
|AP1|MT, No defrost<br>4 – 20 °C|NA||Sair|DI1|
|AP2|MT, Natural defrost<br>2 – 6 °C|Time||Sair|DI1|
|AP3|MT, Natural defrost, defrost stop by Sair<br>2 – 6 °C|Sair temp||Sair|DI1|
|AP4|Heating Thermostat<br>30 – 70 °C|NA||Sair|DI1|
|AP5|Fully configurable simplified application (Cooling / Heating)|||||

> **(1) The digital inputs DI1 can be conf** i **gured for multiple functions (refer parameter “o02”).**

### ERC 213 controller

**Table 2: Pre-defined a** **pp lication table of ERC 213 controller**

|**APP**|**Description**|**Temp.**<br>**range**|**Defrost**<br>**end**|**DO1**|**DO2**|**DO3**|**AI1**|**AI2**|**DI1**<sup>**(1)**</sup>|**DI2**<sup>**(1)**</sup>|
|---|---|---|---|---|---|---|---|---|---|---|
|AP0|Fully Configurable Standard Applic|i  ation (Cooling /|i     Heating)||||||||
|AP1|MT, Natural defrost, Alarm, fan|2 – 6 °C|By time||||Sair|NC|DI1/Sc|DI2|
|AP2|MT, Electrical defrost, Fan|0 – 4 °C|By time||||Sair|NC|DI1/Sc|DI2|
|AP3|LT, Electrical defrost, fan|-24 – -18 °C|By time||||Sair|NC|DI1/Sc|DI2|
|AP4|MT, Electrical defrost, Fan|0 – 4 °C|By<br>temp(S5)||||Sair|S5|DI1/Sc|DI2|
|AP5|LT, Electrical defrost, Fan|-26 – -20 °C|By<br>temp(S5)||||Sair|S5|DI1/Sc|DI2|
|AP6|Fully configurable simplified applic|i i ation (Cooling /|i i    Heating)||||||||
|AP7|Heating Thermostat|30 – 70 °C|NA||||Sair|NC|DI1|DI2|

> **(1) The digital inputs DI1 and DI2 can be conf** i **gured for multiple functions (refer Parameters “o02” and “o37”).**

NC = Not configured

### ERC 214 controller

**Table 3: Pre-defined a** **pp lication table of ERC 214 controller**

|**APP**|**Description**|**Temp.**<br>**range**|**Defrost**<br>**end**|**DO1**|**DO2**|**DO3**|**DO4**|**AI1**|**AI2**|**DI1**<sup>**(1)**</sup>|**DI2**<sup>**(1)**</sup>|
|---|---|---|---|---|---|---|---|---|---|---|---|
|AP0|Fully Configurable Standard Appli|i  cation (Coolin|i   g / Heating)|||||||||
|AP1|MT, Natural defrost, Alarm, fan|2 – 6 °C|By time|||||Sair|NC|DI1/Sc|DI2|
|AP2|MT, Electrical defrost, Fan|0 – 4 °C|By time|||||Sair|NC|DI1/Sc|DI2|
|AP3|LT, Electrical defrost, fan|-24 – -18<br>°C|By time|||||Sair|NC|DI1/Sc|DI2|
|AP4|MT, Electrical defrost, Fan|0 – 4 °C|By<br>temp(S5)|||||Sair|S5|DI1/Sc|DI2|
|AP5|LT, Electrical defrost, Fan|-26 – -20<br>°C|By<br>temp(S5)|||||Sair|S5|DI1/Sc|DI2|
|AP6|Fully configurable simplified appli|i i cation (Coolin|i i  g / Heating)|||||||||
|AP7|Heating Thermostat|30 – 70 °C|NA|||||Sair|NC|DI1|DI2|

> **(1) The digital inputs DI1 and DI2 can be conf** i **gured for multiple functions (refer Parameters “o02” and “o37”)**

#### NC = Not configured

### **Electrical connection diagram**

**Table 4: Electrical connection dia** **g ram**

*[Figurtekst: Type Connection diagrams · GND TX RX +5V · 15 16 17 18 · DO1 · GND GND · ERC 211 · 1 2L 3L 4N 5 6 7 8 9 10 11 12 13 14 · N ot use d · 115/ 115/ Sair DI/Sc · 230V 230V · GND TX RX +5V · 15 16 17 18 · DO1 DO2 DO3 · GND GND · ERC 213 · 1 2L 3L 4N 5 6 7 8 9 10 11 12 13 14 · N ot use d · 115/ 115/ Sair S5 Sc/DI1 DI2 · 230V 230V · GND TX RX +5V · 15 16 17 18 · DO1 DO2 DO3 DO4 · GND GND · ERC 214 · 1 2L 3L 4N 5 6 7 8 9 10 11 12 13 14 · Not used · 115/ 115/ Sair S5 Sc/DI1 DI2 · 230V 230V]*

|3L, 4N|Power supply 115 V AC or 230 V AC (refer to the controller label).|
|---|---|
|Sair|Control Sensor|
|S5|Defrost (evaporator) sensor|
|Sc|Condenser sensor|
|DI1|Digital input - configurable to the functions listed under menu code o02.|
|DI2|Digital input - configurable to the functions listed under menu code o37.|

- **NOTE:**

- 1. Cables for sensors, DI inputs and data communication must be kept separate from other high voltage cables to avoid electric noises.

- Use separate cable trays

- Keep a distance between cables of at least 10 cm

- Long cables at the DI input should be avoided

2. Do not use excessive force while securing wires in to the connectors, allowed tightening torque and wire sizes are:

- Power connectors: wire size = 0.5 – 1.5 mm<sup>2</sup> , max. tightening torque = 0.4 Nm

- Low voltage signal connectors: wire size = 0.15 – 1.5 mm<sup>2</sup> , max. tightening torque = 0.2 Nm

- 2L and 3L must be connected to the same phase

### **Menu navigation and overview**

**Table 5: Ke** **y functions**

*[Figurtekst: Scroll up: Short press (less than 1 second) · Scroll down: Short press (Less than 1 sec.) · Main switch ON/OFF : Press and hold (~ 3 seconds) · Defrost Start/Stop : Press and hold (~3 secs.) · Factory reset: Press and hold at Power up · Back function : Short press (less than 1 sec.) Set point change or OK : Short press (Less than 1 sec.) · Pull down start / stop : Press and hold (~3 secs.) Enter Menu : Press and hold (~ 3 secs.)]*

##### **Table 6: Dis** **p la** **y icons**

*[Figurtekst: Night mode (Energy saving) Fan running · Compressor running (Flashes in pull-down mode) Active alarm · Defrost Unit (°C or °F)]*

### **Quick conf i** **guration at power up**

- **STEP 1: power on**

- **STEP 2: select the quick configuration menu**

Within 30 seconds of power on, press “<” BACK for 3 seconds. The main switch “r12” is automatically set to OFF.

- **STEP 3: select pre-installed application o61**

The display automatically shows the application selection parameter “o61”.

Press SET to select the pre-installed application.

The display shows the default value (eg. “AP0” flashing).

Choose the application type by pressing UP/DOWN and press SET to confirm.

The controller presets parameter values according to the selected application and does not hide relevant parameters.

Tip: you can easily move from AP0 to AP6, and thus select the simplified list of parameters, by pressing the UP key (circular list).

- **STEP 4: select sensor type “o06**

The display automatically shows sensor selection parameter “o06”.

Press SET to select the sensor type.

The display shows the default value (eg. “n10” flashing).

Choose sensor type by pressing UP/DOWN (n5=NTC 5 K, n10=NTC 10 K, Ptc=PTC, Pt1=Pt1000) and press SET to confirm.

 **NOTE:**

All sensors must be the same type.

#### • **STEP 5: configure DO4 output “o36”**

The display automatically shows the o36 parameter to configure “DO4” output. (Available only in 4 relays model). Select light “Lig” or alarm “ALA” as per the application and press SET to confirm.

The display returns to normal display mode and the control is started.

 **NOTE:**

Refer Pre-defined applications for a complete description of the available applications.

##### **Fi** **g ure 10: Confi** **g uration**

*[Figurtekst: SET: press for 3 seconds to access · status, setup and service · 1. Parameter groups · Password (if enabled) · 3. Value · Status input · 2. Parameter name · SET Application · 1-2-3-4-5-6 · Configuration Main switch · SET · Application Application 0 · Sensor type Application · 1-2-3-4-5-6 · Scroll through the · parameter names · DO4 configuration · (only for 4 relays model) · Scroll through the · parameter groups]*

### **Quick conf i** **guration via cFg menu**

1. Press "SET" button for 3 seconds to access the parameter menu (display will show "cFg").

2. Enter “CFg” menu by pressing "SET" button (diaplay will show first parameter "r12” main switch.

3. Select "r12" by pressing "SET" button again and set the main switch to "oFF" (r12=0).

4. Press back button (<) to come back to 'CFg" menu.

5. Press DOWN button to scroll through the "cFg" menu parameter list.

6. Open the “o61 application mode" and select needed application mode (Press SET).

7. Open the “o06 Sensor type” and select the temperature sensor type used (n5=NTC 5 K, n10=NTC 10 K, Ptc=PTC, Pt1=Pt1000)- (Press “SET”).

8. Open the “o02 DI1 Configuration” and select the function associated to digital input 1 (Press “SET”).

9. Open the “o37 DI2 Configuration” and select the function associated to digital input 2 (Press “SET”). 10. Navigate back to parameter “r12 Main switch” and set it in “ON” position to start control.

11. Go through other parameters default settings and change wherever needed

##### **Fi** **g ure 11: Ad** **j ust Set** **p oint**

*[Figurtekst: A Short press "SET" button (Setpoint flashes) · B Press UP/DOWN button to change setpoint · A · C Press "SET" button to save the changed setpoint · B · C]*

**Fi** **g ure 12: Initiate a manual defrost**

*[Figurtekst: A Press "DEFROST" button for 3 seconds to initiate a defrost (Display · shows "-d-" during defrost) · A · B Press "DEFROST" button again for 3 seconds to stop defrost. · B · Fi g ure 13: Initiate a  p ull down · A Press "PULL DOWN" button for 3 seconds to initiate pull down · A · (controller displays "Pud" during pull down) · B Press "PULL DOWN" button again for 3 seconds to stop the pull down · B · Fi g ure 14: View active alarm · A Temperature and alarm codes alternate flashes until the alarm is · resolved. The alarm bell is shown. · A]*

##### **Fi** **g ure 15: Unloack ke** **y board**

- After 5 minutes of no activity, the keypad is locked (if P76=yes).

- When the keypad is locked any button press shows “LoC” in the display.

- Press UP and DOWN buttons simultaneously for 3 seconds to unlock the keyboard. “unl” is displayed for 3 seconds.

### Factory resetting

The controller can be set back to factory settings by using the following procedure:

1. Power OFF controller.

2. Keep up "∧" and down "∨" arrow buttons pressed while reconnecting the supply voltage.

3. When the code “Fac” is shown in the display, select "yes".

 **NOTE:**

The OEM factory setting will either be the Danfoss factory settings or a user defined factory setting if one has been made. The user can save his setting as OEM factory setting via parameter o67.

### **Display codes**

**Table 7: Dis** **p la** **y codes**

|**Code**|**Description**|
|---|---|
|-d-|Defrost cycle is in progress|
|Pud|A temperature pulldown cycle has been initiated|
|Err|The temperature cannot be displayed due to a sensor error|
|---|Shown in top of display: The parameter value has reached max. Limit|
|---|Shown in bottom of display: The parameter value has reached min. Limit|
|Loc|The display keyboard is locked|
|UnL|The display keyboard has been unlocked|
|PS|The access code is required to enter the parameter menu|
|Axx/Exx|Alarm or error code flashing with normal temp. readout|
|OFF|Control is stopped as r12 Main switch is set OFF|
|On|Control is started as r12 Main switch is set ON (code shown in 3 seconds)|
|Fac|The controller is reset to factory setting|

### **Parameters**

### **Parameter description**

**Table 8: Confi** **g uration**

|**Code**|**Parameter description**|**Min.**|**Max.**<br>**Unit**|
|---|---|---|---|
|**cFg**|**Configuration**|||
|r12|**Main Switch**<br>With this setting refrigeration can be started, stopped or a manual override of the outputs can be allowed.<br>Service (manual control of outputs allowed)(-1 in Controller Display)<br>OFF (0 in Controller Display)<br>ON (1 in Controller Display)|Service|ON|
|o61|**Predefined applications**<br>Predefined applications is to give the user an easy and fast way to configure the controller. Users can set appropriate applica-<br>tion that meets their requirements under this menu (please refer predefined applications table under section 2.4 for more<br>details). Predefined application is protected by main switch.|AP0|AP7|
|o07|Select main application type for which controller is used<br>rE= Cooling<br>Ht= Heating|rE|Ht|
|o06|**Sensor type**<br>This parameter defines the type of temperature sensors connected to the controller. Below sensor types can be used in<br>ERC21x<br>n5=NTC 5K (5000 Ohm at 25 °C, Beta value=3980 @25/100 °C)<br>n10= NTC 10 (10000 Ohm at 25 °C, Beta value = 3435 @ 25/100 °C)<br>pt1= PT1000<br>ptc= PTC<br>All the mounted sensors (Sair, S5 and Sc)must be of same type.|n10|pt1|
|o71|This parameter defines the desired configuration for Relay 2 (DO2)<br>dEF=Defrost<br>ALA=alarm<br>Lig=Light|dEF|Lig|
|o36|This parameter defines the desired configuration for Relay 4 (DO4). Applicable only for ERC214.<br>Lig=Light<br>ALA=alarm|Lig|ALA|

### Thermostat

**Table 9: Thermostat**

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|**r--**|**Thermostat**||||
|r00|**SetPoint**<br>This parameter defines the desired cabinet temperature at which compressor cuts out. The set point can be locked to a range<br>within r02 and r03 settings.|-100.0|200.0|°C|
|r01|**Differential**<br>This defines the difference between the cut-out and the cut-in of compressor relay. Compressor relay will cut-in when the<br>cabinet temperature reaches the set point+ differetial. In case of heating application, heater will cut-in when the temperature<br>reaches the set point-differential.|0.1|20.0|K|
|r02|**Maximum Set Point limitation**<br>The maximum allowable setpoint value can be configured here that would avoid setting too high values by mistake.|-100.0|200.0|°C|
|r03|**Minimum Set Point limitation**<br>The minimum allowable setpoint value can be configured here that would avoid setting too low values by accident/mistake.|-100.0|200.0|°C|
|r04|**Display offset**<br>Correction value in display temperature. If the temperature of the products / cabinet and the temperature received by the<br>controller are not identical, an offset adjustment of the display temperature can be carried out using this parameter.|-10.0|10.0|K|
|r05|**Display Unit**<br>Set here if the controller is to show temperature values in °C or in °F. Switching from one to the other will cause all tempera-<br>ture settings to be automatically updated to respective unit.|-C|-F||
|r09|**Calibration of Sair**<br>This parameter is a relative value and allows adjustment of the Sair sensor temperature. For instance, at a measured tempera-<br>ture of 7 °C and r09 set to 2K, the input from the Sair sensor will be 9 °C instead.|-20.0|20.0|K|
|r12|**Main Switch**<br>With this setting refrigeration can be started, stopped or a manual override of the outputs can be allowed. Stopped refrigera-<br>tion will give a “OFF” signal on the display.<br>-1=service (manual control of outputs allowed)<br>0=OFF<br>1=ON|-1|1||
|r13|**Night setback value**<br>The thermostat’s reference can be offset by this value during night or when there is no usage. Offset can be set both possitive<br>and negative sides (Select a negative value if there is to be cold accumulation). Activation can take place via digital input.|-50.0|50.0|K|

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|r40|**Reference displacement offset temperature**<br>The thermostat setpoint and the alarm values get shifted by this value when the reference displacement is activated. Activa-<br>tion can take place via digital input.|-50.0|20.0|°C|
|r96|**Pull-down duration**<br>Maximum duration of the pull-down mode. When set as “0” Pull down mode disabled.|0|960|min|
|r97|**Pull-down limit temperature**<br>A safety feature; the lowest temperature allowed during pull-down.|-100.0|200.0|°C|

### Alarm settings

##### **Table 10: Alarm settin** **g s**

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|**A--**|**Alarm settings**||||
|A03|**Delay for temperature alarm during normal conditions**<br>High and low temperature alarm will be delayed by this value after crossing the set alarm limits. The alarm will not become<br>active until the set time delay has been passed.|0|240|min|
|A12|**Delay for temperature alarm during pull-down/start-up/defrost**<br>Controller uses this time delay to trigger low and high temperature alarms during start-up, defrost and pull-down modes|0|240|min|
|A13|**High temperature alarm limit**<br>If the cabinet temperature stays above this limit for the time mentioned by the alarm delay parameters, high temperature<br>alarm is raised.|-100.0|200.0|°C|
|A14|**Low temperature alarm limit**<br>If the cabinet temperature stays below this limit for the time mentioned by the alarm delay parameters, low temperature<br>alarm is raised.|-100.0|200.0|°C|
|A27|**DI1 delay**<br>If Di1 is configured as a door open alarm or as an external alarm, this delay is used to raise the respective alarm.|0|240|min|
|A28|**DI2 delay**<br>If Di2 is configured as a door open alarm or as an external alarm, this delay is used to raise the respective alarm.|0|240|min|
|A37|**Condenser high alarm limit**<br>If the condenser temperature reaches above this limit, condenser alarm is raised immediately and no action is taken. The<br>alarm is reset if temperature falls 5 K below the set temperature.|0|200|°C|
|A54|**Condenser High block limit**<br>If the condenser temperature continues to increase above the A37 limit and reaches this temperature limit, condenser block<br>alarm is raised and compressor is stopped. It is restricted to starting again until alarm is reset manually. Manual reset of con-<br>denser block alarm can be performed by power cycling the controller either by main switch button or input supply.|0|200|°C|
|A72|**Voltage protection**<br>This parameter is to enable and disable the voltage protection feature, which protects compressor from adverse line voltage<br>conditions.|no|YES||
|A73|**Minimum cut-in voltage**<br>When the compressor is due to start, the voltage of the power supply will be checked and the compressor is allowed to start<br>if the supply voltage is greater than this value.|0|270|V|
|A74|**Minimum cut-out voltage**<br>When the compressor is running, it will be switched OFF if the supply voltage goes below this value.|0|270|V|
|A75|**Maximum voltage**<br>When the compressor is running, it will be switched OFF if the supply voltage exceeds this value.|0|270|V|

### Defrost

**Table 11: Defrost**

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|**d--**|**Defrost**||||
|d01|**Defrost type**<br>Selection of desired defrost type<br>no= No defrost (defrost function diabled)<br>nAt = Natural defrost (Off cycle defrost)<br>EL = Electrical defrost<br>gAS = Hot gas defrost|no|gAS||
|d02|**Defrost stop temperature**<br>This parameter defines at what temperature the defrost cycle will stop. Defrost can be stoped based on either evaporator<br>sensor or by the cabinet temperature sensor as defined in menu code d10.|0.0|50.0|°C|
|d03|**Defrost interval**<br>Defines the maximum time period between the start of two defrost cycles. In case of power failure elapsed time is stored in<br>the memory and next defrost will happen considering the stored time interval.|0|240|hour|
|d04|**Maximum defrost time**<br>This parameter defines the maximum time defrost will be performed. In case of temperature based defrost this is treated as<br>safety time to stop the defrost if it is not terminated based on the temperature.|0|480|min|
|d05|**Defrost delay at power up or DI signal**<br>This parameter decides the time offset when the defrost is triggered by digital inputs or during power up. This function is<br>only relevant if you have several refrigeration appliances or groups where you want the defrost to be staggered in relation to<br>one another.|0|240|min|

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|d06|**Drip-off time**<br>This parameter defines the time delay to start the compressor after defrost heater being switched OFF. This delay is generally<br>provided to ensure all water droplets on the evaporator drips off before starting the refrigeration cycle.|0|60|min|
|d07|**Fan delay after defrost**<br>Defines how long the delay is between the start of the compressor and the fan after defrost cycle. This would help to avoid<br>hot air circulation in the cabinet imedietely after defrost.|0|60|min|
|d08|**Fan start temperature after defrost**<br>This only applies if an evaporator temperature sensor is fitted. This parameter determines at what evaporator temperature<br>the fan will start after a defrost cycle is complete. If the time set in d07 occurs before the temperature set in d08, the fan will<br>start in line with d07. If the temperature set in d08 occurs first, then the fan will start in line with d08.|-50.0|50.0|°C|
|d09|**Fan during defrost**<br>This parameter is to define whether fan is to operate during defrost or not.|OFF|on||
|d10|**Defrost Stop Sensor**<br>This parameter is to define which sensor has to be used to exit / terminate the defrost<br>non = none, defrost is based on time<br>Air = Sair sensor<br>dEF = S5 defrost sensor|non|dEF||
|d18|**Compressor accumulated runtime to start defrost**<br>When the accumulated compressor runtime is equal to the value set in this Parameter, defrost will be triggered. If the accu-<br>mulated compressor runtime is less than the set value during the defined defrost interval (d03), defrost will be triggered<br>based on the defrost interval (d03). This feature is disabled when this parameter is set to zero.|0|96|hour|
|d19|**Defrost on demand**<br>The controller will record S5 temperature during each defrost interval when the evaporator is clean and continue to monitor<br>S5 temperature. Controller triggers defrost if the S5 temperature becomes less than recorded temperature by this value it will<br>initiate the defrost on demand. This feature is disabled when this parameter is set to 20. This function can only be used in 1:1<br>systems.|0.0|20.0|K|
|d30|**Defrost delay after pull down**<br>This parameter defines the time delay to start the defrost after pull down cycle. This has to ensure defrost doesnot happen<br>immedietely after pull down cycle.|0|960|min|

### Fan

##### **Table 12: Fan**

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|**F--**|**Fan**||||
|F01|**Fan control during compressor off cycle**<br>This parameter define the fan operation during compressor off cycle.<br>FAo=Fan always ON<br>FFC=Fan follow compressor (Fan is switched off during compressor off cycle)<br>FPL= Fan Cycling|FAo|FPL||
|F04|**Fan stop evaporating temperature**<br>This parameter defines the maximum evaporator temperature at which the Fan must switch OFF. If the defrost sensor regis-<br>ters a higher temperature than the one set here, the fans will be stopped to avoid the warm air circulation in the cabinet.|-50.0|50.0|°C|
|F07|**Fan On cycle**<br>This parameter is applicable only when the Fan at Compressor cut out (F01) is set to Fan cycling mode. The Fan ON time will<br>be as per the time set in this parameter.|0|180|min|
|F08|**Fan OFF cycle**<br>This parameter is applicable only when the Fan at Compressor cut out (F01) is set to Fan cycling mode. The Fan OFF time will<br>be as per the time set in this parameter.|0|180|min|

### Compressor

##### **Table 13: Com** **p ressor**

|**Code**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|**c--**|**Compressor**||||
|C01|**Compressor minimum ON time**<br>This parameter determines the minimum number of minutes the compressor must run before a cut-out can take effect based<br>on temperature. This is to avoid sudden switching ON and OFF of the compressor. When used for Heating application, sug-<br>gest to set this value 0 to avoid any overheating.|0|30|min|
|C02|**Compressor minimum OFF time**<br>This parameter determines the minimum number of minutes the compressor must switched OFF before a cut-in can take<br>effect based on temperature. This is to avoid sudden switching OFF and ON of the compressor.|0|30|min|
|C04|**Compressor OFF delay at door open**<br>This parameter sets the delay to stop the compressor when the door is opened. If set to 900, the function is disabled.|0|900|sec|
|C70|**Zero crossing selection**<br>This feature will increase the relay life time, reduce the contact welding and switching noise by switching ON at Zero crossing.<br>Disable zero crossing when external relay is used.|no|YES||

### Miscellaneous

**Table 14: Miscellaneous**

|**Code**<br>**o--**|**Parameter description**|**Min.**|**Max.**|**Unit**|
|---|---|---|---|---|
|o01|**Delay of outputs at startup**<br>After start-up the controller functions can be delayed by the time delay defined here so that overloading of the electricity<br>supply network is avoided.|0|600|sec|
|o02|**Desired configuration for digital input 1 (DI1)**<br>nC= Not configured<br>Sdc = Status display output<br>doo = Door alarm with resumption<br>doA = Door alarm without resumption<br>SCH = Main switch<br>nig = Day/Night mode<br>rFd = Reference displasement<br>EAL = External alarm<br>dEF = Defrost<br>Pud = Pull down<br>Sc = Condensor Sensor|nC|Sc||
|o03|**Serial Address**<br>Data communication is possible by using external TTL to RS485 converter|0|247|No|
|o05|**Password**<br>If the settings in the controller are to be protected with an access code you can set a numerical value between 0 and 999. You<br>can cancel the function by setting to 0.|0|999|No|
|o15|**Display Resolution**<br>This parameter defines the steps in which the temperature must be displayed by 0.1 or 0.5 or 1|0.1|1.0||
|o37|**Desired configuration for digital input 2 (DI2)**<br>nC= Not configured<br>Sdc = Status display output<br>doo = Door alarm with resumption<br>doA = Door alarm without resumption<br>SCH = Main switch, nig = Day/ Night mode<br>rFd = Reference displasement<br>EAL = External alarm<br>dEF = Defrost<br>Pud = Pull down|nC|Pud||
|o38|This defines the method to control cabinet light<br>on= Always on<br>dAn = Day/Night<br>doo=Based on door action|on|doo||
|o67|**Save settings as factory**<br>This parameter when set to YES , The current controller Parameter settings are stored as Factory default.<br>**WARNING:**<br>Original factory settings are overwritten|no|YES||
|o91|**Display during defrost**<br>You can set what is to be displayed during defrost here.<br>Air = actual air temperature<br>FrE = freezed temperature (display the temperature just before starting defrost)<br>-d- = -d- is displayed|Air|-d-||
|**P--**|||||
|P73|**DI1 input polarity**<br>no (normally open) = associated functionality is activated when DI1 port is short circuit and deactivated when DI1 port is<br>open circuit.<br>nc (normally closed) = associated functionality is activated when DI1 port is open circuit and deactivated when DI1 port is<br>short circuit.|no|nc||
|P74|**DI2 input polarity**<br>no (normally open) = associated functionality is activated when DI2 port is short circuit and deactivated when DI2 port is<br>open circuit.<br>nc (normally closed) = associated functionality is activated when DI2 port is open circuit and deactivated when DI2 port is<br>short circuit.|no|nc||
|P75|**Invert alarm relay**<br>Alarm relay operation can be inverted here<br>0=normal, 1= invert relay action|0|1||
|P76|**Key board lock enable**<br>Setting this parameter as "YES" enables controller keypad lock functionality after 5 minutes of no activity on the keypad.<br>When the keypad is locked any button press shows “LoC” in the display. Press UP and DOWN buttons simultaneously for 3<br>seconds to unlock the keyboard. “unl” is displayed for 3 seconds.|no|YES||

### Service

**Table 15: Service**

|**Code**|**Parameter description**<br>**Min.**<br>**Max.**<br>**Unit**|
|---|---|
|**u--**|**Service**|
|u00|**Controller Status**<br>S0=Cooling ON/Heating ON<br>S2=wait for compressor ON time to elapse<br>S3=wait for compressor OFF time to elapse<br>S4=drip OFF delay after defrost<br>S10=cooling stopped by MainSwitch OFF<br>S11=cooling stopped by thermostat/heating OFF<br>S14=defrosting state<br>S15=fan delay state after defrost<br>S17=door open (DI input)<br>S20=emergency cooling<br>S25=manual control of outputs<br>S30=Pull-down<br>S32=delay of outputs at power up|
|u01|Temperature measured by Sair sensor|
|u02|Reference set point used for the control|
|u09|Temperature measured byevaporator sensor|
|u10|Status of connected Digital input configured to DI1<br>Open<br>Close|
|u13|Shows status of night mode<br>ON or OFF|
|u37|Status of connected Digital input configured to DI2<br>Open<br>Close|
|u29|Temperature measured by condenser Sensor|
|u58|Status of compressor relay<br>ON/OFF|
|u59|Status of Fan relay<br>ON/OFF|
|u60|Status of Defrost relay<br>ON/OFF|
|u63|Status of Light relay<br>ON/OFF|
|o23|**Relay 1 counter**<br>The number of cycles for the DO1 relay can be read in this menu. The read value is multiplied by 100 to obtain the number of<br>cycles. On reaching 999x100 cycles the counts stops and is reset to 0.<br>0<br>999|
|o24|**Relay 2 counter**<br>The number of cycles for the DO2 relay can be read in this menu. The read value is multiplied by 100 to obtain the number of<br>cycles. On reaching 999x100 cycles the counts stops and is reset to 0.<br>0<br>999|
|o25|**Relay 3 counter**<br>The number of cycles for the DO3 relay can be read in this menu. The read value is multiplied by 100 to obtain the number of<br>cycles. On reaching 999x100 cycles the counts stops and is reset to 0.<br>0<br>999|
|o26|**Relay 4 counter**<br>The number of cycles for the DO4 relay can be read in this menu. The read value is multiplied by 100 to obtain the number of<br>cycles. On reaching 999x100 cycles the counts stops and is reset to 0."<br>0<br>999|
|u80<br>u82|Firmware version readout<br>Controller code number|

### **Parameters: ERC 211**

**Table 16: Confi** **g uration**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Configuration**|**cFg**||||||||||
|Main switch -1=Service, 0=OFF, 1=ON)|r12|-1|1||1|1|1|1|1|1|
|Predefined applications|o61<sup>**(2)**</sup>|AP0|AP5||AP0|AP1|AP2|AP3|AP4|AP5|
|Cooling/Heating (rE=Cooling, Ht= Heating)|o07<sup>**(2)**</sup>|rE|Ht||rE|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|Ht<sup>**(1)**</sup>|rE|
|Sensor type selection (n5=NTC 5K, n10=NTC10K, ptc=PTC,<br>pt1=PT1000)|o06<sup>**(2)**</sup>|n5|ptc||n10|n10|n10|n10|n10|n10|

- **(1) This option is a default setting in the controller and cannot be changed.**

> **(2) This parameter can only be set when regulation is stopped, i.e. “r12” is set to 0.**

### Reference

**Table 17: Reference**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Reference**|**r--**||||||||||
|Setpoint|r00|-100.0|200.0|°C|2.0|8.0|4.0|4.0|50.0|2.0|
|Differential|r01|0.1|20.0|K|2.0|2.0|2.0|2.0|2.0|2.0|
|Maximum set point limitation|r02|-100.0|200.0|°C|50.0|20.0|6.0|6.0|70.0|50.0|
|Minimum set point limitation|r03|-100.0|200.0|°C|-35.0|4.0|2.0|2.0|30.0|-35.0|
|Display offset|r04|-10.0|10.0|K|0.0|0.0|0.0|0.0|0.0|0.0|
|Display Unit (°C/ °F)|r05|-C|-F||-C|-C|-C|-C|-C|-C|
|Calibration of Sair|r09|-20.0|20.0|K|0.0|0.0|0.0|0.0|0.0|-|
|Main switch ( -1=Service, 0=OFF, 1=ON)|r12|-1|1||1|1|1|1|1|1|
|Night Set back|r13|-50.0|50.0|K|0.0|0.0|0.0|0.0|0.0|0.0|
|Reference displacement offset temperature|r40|-50.0|20.0|°C|0.0|0.0|0.0|0.0|0.0|-|
|Pull down duration|r96|0|960|min|0|-|0|0|-|-|
|Pull down limit temperature|r97|-100.0|200.0|°C|0.0|-|0.0|0.0|-|-|

### Alarm

**Table 18: Alarm**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Alarm**|**A--**||||||||||
|Delay for temp alarm during normal conditions|A03|0|240|min|30|45|45|45|10|30|
|Delay for temp alarm during pull-down/start up/ defrost|A12|0|240|min|60|60|90|90|NA|60|
|High temp. alarm limit|A13|-100.0|200.0|°C|8.0|16.0|10.0|10.0|80.0|8.0|
|Low temp. alarm limit|A14|-100.0|200.0|°C|-30.0|0.0|0.0|0.0|10.0|-30.0|
|DI1 delay (Time delay for selected DI1 function)|A27|0|240|min|30|30|30|30|30|30|
|Condenser High alarm limit|A37|0|200|°C|80|80|80|80|-|-|
|Condenser High block limit|A54|0|200|°C|85|85|85|85|-|-|
|Voltage protection enable|A72|no|YES||no|no|no|no|no|no|
|Minimum cut-in voltage|A73|0|270|V|0|0|0|0|0|0|
|Minimum cut-out voltage|A74|0|270|V|0|0|0|0|0|0|
|Maximum voltage|A75|0|270|V|270|270|270|270|270|270|

### Defrost

**Table 19: Defrost**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Defrost**|**d--**||||||||||
|Defrost Method (no=no defrost, nAt=Natural)|d01|no|nAt||nAt|no|nAt|nAt|no|no|
|Defrost stop temperature.|d02|0.0|50.0|°C|6.0|-|-|8.0|-|6.0|
|Defrost Interval|d03|0|240|hour|8.0|-|6.0|6.0|-|8.0|
|Max defrost Time|d04|0|480|min|30|-|45|60|-|30|
|Defrost delay at power up (or DI signal)|d05|0|240|min|0|-|0|0|-|-|
|Drip delay|d06|0|60|min|0|-|0|0|-|-|
|Defrost stop sensor non=None (Time), Air = Sair temp. Sensor|d10|non|Air||non|-|non<sup>**(1)**</sup>|Air<sup>**(1)**</sup>|-|non|
|Accumulated Compressor runtime to start defrost (0=OFF)|d18|0|96|hour|0|-|0|0|-|-|
|Defrost delay after pull down cycle|d30|0|960|min|0|-|0|0|-|-|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Compressor

**Table 20: Com** **p ressor**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Compressor**|**c--**||||||||||
|Compressor minimum ON time|C01|0|30|min|0.0|0.0|0.0|0.0|0.0|0.0|
|Compressor minimum OFF time|C02|0|30|min|2.0|2.0|2.0|2.0|2.0|2.0|
|Compressor OFF delay at open door|C04|0|900|sec|900.0|900.0|900.0|900.0|900.0|60.0|
|Zero crossing selection (YES / no)|C70|no|YES||YES|YES|YES|YES|YES|YES<sup>**(1)**</sup>|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Others

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Others**|**o--**||||||||||
|Delay of outputs at startup|o01|0|600|sec|10|10|10|10|10|10<sup>**(1)**</sup>|
|DI1 configuration<br>nC= Not configured; Sdc = Status display output, doo = Door<br>alarm with resumption, doA = Door alarm without resumption,<br>SCH = Main switch, nig = Day/ Night mode, rFd = Reference dis-<br>plasement, EAL = External alarm, dEF = Defrost, Pud = Pull<br>down; Sc = Condensor Sensor|o02|oFF|Sc||oFF|oFF|oFF|oFF|oFF|oFF|
|Serial address|o03|0|247|No|0|0|0|0|0|-|
|Password|o05|0|999|No|0|0|0|0|0|0|
|Sensor type selection (n5=NTC 5K, n10=NTC10K, ptc=PTC,<br>pt1=PT1000)|o06<sup>**(2)**</sup>|n5|ptc||n10|n10|n10|n10|n10|n10|
|Cooling/Heating (rE=Cooling, Ht= Heating)|o07<sup>**(2)**</sup>|rE|Ht||rE|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|Ht<sup>**(1)**</sup>|rE|
|Display Resolution|o15|0.1|1.0||0.1|0.1|0.1|0.1|0.1|0.1<sup>**(1)**</sup>|
|Predefined applications|o61<sup>**(2)**</sup>|AP0|AP5||AP0|AP1|AP2|AP3|AP4|AP5|
|Save settings as factory<br>**WARNING:**<br>The earlier factory settings are overwritten|o67|no|YES||no|no|no|no|no|-|
|Display during defrost<br>Air=actual air temperature, FrE=freezed temperature, -d-="-d-"<br>is displayed|o91|-d-|Air||-d-|-|-d-|-d-|-|-d-<sup>**(1)**</sup>|

> **(1) This option is a default setting in the controller and cannot be changed.**

> **(2) This parameter can only be set when regulation is stopped, i.e. “r12” is set to 0**

### Polarity

**Table 21: Polarit** **y**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|
|---|---|---|---|---|---|---|---|---|---|---|
|**Polarity**|**P--**||||||||||
|DI1 input polarity (nc/no)|P73|no|nc||no|no|no|no|no|no|
|no = normally open|||||||||||
|nc = normally closed|||||||||||
|Key board lock (no / yes)(0=no, 1=yes)|P76|no|YES||no|no|no|no|no|-|

### **Parameters: ERC 213**

**Table 22: Confi** **g uration**

|**Function**|**Code**|**Min.**|**Max.**<br>**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|**Configuration**|**cFg**|||||||||||
|Main switch (-1=Service, 0=OFF, 1=ON)|r12|-1|1|1|1|1|1|1|1|1|1|
|Predefined applications|o61<sup>**(2)**</sup>|AP0|AP7|AP0|AP1|AP2|AP3|AP4|AP5|AP6|AP7|

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Cooling/Heating (rE=Cooling, Ht= Heating)|o07<sup>**(2)**</sup>|rE|Ht||rE|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE|Ht<sup>**(1)**</sup>|
|Sensor type (n5=NTC 5K, n10=NTC10K, ptc=PTC,<br>pt1=PT1000)|o06<sup>**(2)**</sup>|n5|ptc||n10|n10|n10|n10|n10|n10|n10|n10|
|DO2 config (dEF=Defrost; ALA=alarm; Lig=Light)|o71<sup>**(2)**</sup>|dEF|Lig||dEF|ALA<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF|ALA|

> **(1) This option is a default setting in the controller and cannot be changed.**

> **(2) This parameter can only be set when regulation is stopped, i.e. “r12” is set to 0.**

### Reference

**Table 23: Reference**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Reference**|**r--**||||||||||||
|Setpoint|r00|-100.0|200.0|°C|2.0|4.0|2.0|-20.0|2.0|-24.0|2.0|50.0|
|Differential|r01|0.1|20.0|K|2.0|2.0|2.0|2.0|2.0|2.0|2.0|4.0|
|Maximum set point limitation|r02|-100.0|200.0|°C|50.0|6.0|4.0|-18.0|4.0|-20.0|50.0|70.0|
|Minimum set point limitation|r03|-100.0|200.0|°C|-35.0|2.0|0.0|-24.0|0.0|-26.0|-35.0|30.0|
|Display offset|r04|-10.0|10.0|K|0.0|0.0|0.0|0.0|0.0|0.0|0.0|0.0|
|Display Unit (°C/ °F)|r05|-C|-F||-C|-C|-C|-C|-C|-C|-C|-C|
|Calibration of Sair|r09|-20.0|20.0|K|0.0|0.0|0.0|0.0|0.0|0.0|0.0|0.0|
|Main switch ( -1=Service, 0=OFF, 1=ON,)|r12|-1|1||1|1|1|1|1|1|1|1|
|Night Set back|r13|-50.0|50.0|K|0.0|0.0|0.0|0.0|0.0|0.0|0.0|0.0|
|Reference displacement offset temperature|r40|-50.0|20.0|°C|0.0|0.0|0.0|0.0|0.0|0.0|-|0.0|
|Pull down duration|r96|0|960|min|0|0|0|0|0|0|-|-|
|Pull down limit temperature|r97|-100.0|200.0|°C|0.0|0.0|0.0|0.0|0.0|0.0|-|-|

### Alarm

**Table 24: Alarm**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Alarm**|**A--**||||||||||||
|Delay for temp alarm during normal conditions|A03|0|240|min|30|45|30|30|30|30|30|10|
|Delay for temp alarm during pull-down/start up/<br>defrost|A12|0|240|min|60|90|60|60|60|60|60|-|
|High temp. alarm limit|A13|-100.0|200.0|°C|8.0|10.0|8.0|-15.0|8.0|-15.0|8.0|80.0|
|Low temp. alarm limit|A14|-100.0|200.0|°C|-30.0|0.0|-2.0|-30|-2.0|-30.0|-30.0|20.0|
|DI1 delay (Time delay for selected DI1 function)|A27|0|240|min|30|30|30|30|30|30|30|30|
|DI2 delay (Time delay for selected DI2 function)|A28|0|240|min|30|30|30|30|30|30|30|30|
|Condenser High alarm limit|A37|0|200|°C|80|80|80|80|80|80|-|-|
|Condenser High block limit|A54|0|200|°C|85|85|85|85|85|85|-|-|
|Voltage protection enable|A72|no|YES||no|no|no|no|no|no|no|no|
|Minimum cut-in voltage|A73|0|270|V|0|0|0|0|0|0|0|0|
|Minimum cut-out voltage|A74|0|270|V|0|0|0|0|0|0|0|0|
|Maximum voltage|A75|0|270|V|270|270|270|270|270|270|270|270|

### Defrost

**Table 25: Defrost**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Defrost**|**d--**||||||||||||
|Defrost Method (no=None, nAt=Natural, EL = Elec-<br>tric; gAS=Hot gas)|d01|no|gAS||EL|nAt|EL|EL|EL|EL|EL|-|
|Defrost stop temperature.|d02|0.0|50.0|°C|6.0|-|-|-|6.0|6.0|6.0|-|
|Defrost Interval|d03|0|240|hour|8|6|8|12|8|12|8|-|
|Max defrost Time|d04|0|480|min|30|45|15|15|30|30|30|-|
|Defrost delay at power up|d05|0|240|min|0|0|0|0|0|0|NA|-|
|Drip delay|d06|0|60|min|0|0|0|0|0|0|2<sup>**(1)**</sup>|-|
|Fan delay after defrost|d07|0|60|min|0|0|0|0|0|0|5<sup>**(1)**</sup>|-|
|Fan start temperature after defrost|d08|-50.0|50.0|°C|-5.0|50.0<sup>**(1)**</sup>|50.0<sup>**(1)**</sup>|50.0<sup>**(1)**</sup>|-5.0|-5.0|-|-|

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Fan during defrost|d09|OFF|on||on|on|OFF|OFF|OFF|OFF|OFF|-|
|Defrost stop sensor non=None (Time), Air = Sair<br>temp. sensor, dEF= S5 Defrost sensor|d10|non|dEF||non|non<sup>**(1)**</sup>|non<sup>**(1)**</sup>|non<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|non|-|
|Accumulated Compressor runtime to start defrost<br>(0=OFF)|d18|0|96|hour|0|0|0|0|0|0|-|-|
|Defrost on demand (20=OFF)|d19|0.0|20.0|K|20.0|20.0<sup>**(1)**</sup>|20.0<sup>**(1)**</sup>|20.0<sup>**(1)**</sup>|20.0|20.0|-|-|
|Defrost delay after pull down cycle|d30|0|960|min|0|0|0|0|0|0|-|-|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Fan control

**Table 26: Fan control**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Fan control**|**F--**||||||||||||
|Fan at compressor cutout (FAo=Fan always ON;<br>FFC=Fan follow compressor; FPL= Fan Pulsating)|F01|Fao|FPL||FAo|FAo|FAo|FAo|FAo|FAo|FAo|FAo|
|Fan stop evap. Temperature|F04|-50.0|50.0|°C|50.0|-|-|-|50.0|50.0|50.0|-|
|Fan ON Cycle|F07|0|180|min|2|2|2|2|2|2<sup>**(1)**</sup>|2|2|
|Fan OFF cycle|F08|0|180|min|2|2|2|2|2|2<sup>**(1)**</sup>|2|2|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Compressor

**Table 27: Com** **p ressor**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Compressor**|**c--**||||||||||||
|Compressor / Heater minimum ON time|C01|0|30|min|0|0|0|0|0|0|0|0|
|Compressor /Heater minimum OFF time|C02|0|30|min|2|2|2|2|2|2|2|2|
|Compressor OFF delay at open door|C04|0|900|Sec|900|900|900|900|900|900|60<sup>**(1)**</sup>|900|
|Zero crossing selection (YES / no)|C70|no|YES||YES|YES|YES|YES|YES|YES|YES<sup>**(1)**</sup>|YES|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Others

**Table 28: Others**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Others**|**o--**||||||||||||
|Delay of outputs at startup|o01|0|600|sec|10|10|10|10|10|10|10<sup>**(1)**</sup>|10|
|DI1 configuration<br>nC= Not configured; Sdc = Status display output,<br>doo = Door alarm with resumption, doA = Door<br>alarm without resumption, SCH = Main switch, nig<br>= Day/ Night mode, rFd = Reference displasement,<br>EAL = External alarm, dEF = Defrost, Pud = Pull<br>down; Sc = Condensor Sensor|o02|nC|Sc||nC|nC|nC|nC|nC|nC|nC|nC|
|Serial address|o03|0|247|No|0|0|0|0|0|0|-|0|
|Password|o05|0|999|No|0|0|0|0|0|0|0|0|
|Sensor type (n5=NTC 5K, n10=NTC10K, ptc=PTC,<br>pt1=PT1000)|o06<sup>**(2)**</sup>|n5|ptc||n10|n10|n10|n10|n10|n10|n10|n10|
|Cooling/Heating (rE=Cooling, Ht= Heating)|o07<sup>**(2)**</sup>|rE|Ht||rE|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE|Ht<sup>**(1)**</sup>|
|Display Resolution|o15|0.1|1.0||0.1|0.1|0.1|0.1|0.1|0.1|0.1<sup>**(1)**</sup>|0.1|
|DI2 configuration<br>nC= Not configured; Sdc = Status display output,<br>doo = Door alarm with resumption, doA = Door<br>alarm without resumption, SCH = Main switch, nig<br>= Day/Night mode, rFd = Reference displasement,<br>EAL = External alarm, dEF = Defrost, Pud = Pull<br>down|o37|nC|Pud||nC|nC|nC|nC|nC|nC|nC|nC|

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Light Control<br>on= Always on, dAn = Day/Night, doo=Based on<br>door action|o38|on|doo||on|on|on|on|on|on|on|on|
|Predefined applications|o61<sup>**(2)**</sup>|AP0|AP7||AP0|AP1|AP2|AP3|AP4|AP5|AP6|AP7|
|Save settings as factory<br>**NOTE:**<br>The earlier factory settings are overwritten|o67|no|YES||no|no|no|no|no|no|-|no|
|DO2 config<br>dEF=Defrost; ALA=alarm; Lig=Light|o71<sup>**(2)**</sup>|dEF|Lig||dEF|ALA<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF|ALA|
|Display during defrost<br>Air=actual air temperature, FrE=freezed tempera-<br>ture, -d-="-d-" is displayed|o91|Air|-d-||-d-|-d-|-d-|-d-|-d-|-d-|-d-<sup>**(1)**</sup>|-|

> **(1) This option is a default setting in the controller and cannot be changed.**

> **(2) This parameter can only be set when regulation is stopped, i.e. “r12” is set to 0.**

### Polarity

**Table 29: Polarit** **y**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Polarity**|**P--**||||||||||||
|DI1 input polarity (nc/no)<br>no = normally open<br>nc = normally closed|P73|no|nc||no|no|no|no|no|no|no|no|
|DI2 input polarity (nc/no)<br>no = normally open<br>nc = normally closed|P74|no|nc||no|no|no|no|no|no|no|no|
|Invert alarm relay (0= normal, 1= invert relay ac-<br>tion)|P75|0|1||0|0|0|0|0|0|-|0|
|Key board lock (no / yes)(0=no, 1=yes)|P76|no|YES||no|no|no|no|no|no|-|no|

### **Parameters: ERC 214**

**Table 30: Confi** **g uration**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Configuration**|**cFg**||||||||||||
|Main switch (-1=Service, 0=OFF, 1=ON)|r12|-1|1||1|1|1|1|1|1|1|1|
|Predefined applications|o61<sup>**(2)**</sup>|AP0|AP7||AP0|AP1|AP2|AP3|AP4|AP4|AP6|AP7|
|Cooling/Heating (rE=Cooling, Ht= Heating)|o07<sup>**(2)**</sup>|rE|Ht||rE|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE|Ht<sup>**(1)**</sup>|
|Sensor type selection (n5=NTC 5K, n10=NTC10K,<br>ptc=PTC, pt1=PT1000)|o06<sup>**(2)**</sup>|n10|pt1||n10|n10|n10|n10|n10|n10|n10|n10|
|DO2 config (dEF=Defrost; ALA=alarm; Lig=Light)|o71<sup>**(2)**</sup>|dEF|Lig||dEF|ALA<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF|ALA<sup>**(1)**</sup>|
|DO4 config (Lig=Light, ALA=Alarm)|o36<sup>**(2)**</sup>|Lig|ALA||Lig|Lig|Lig|Lig|Lig|Lig|Lig|Lig|

> **(1) This option is a default setting in the controller and cannot be changed.**

> **(2) This parameter can only be set when regulation is stopped, i.e. “r12” is set to 0.**

### Reference

**Table 31: Reference**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Reference**|**r--**||||||||||||
|Setpoint|r00|-100.0|200.0|°C|2.0|4.0|2.0|-20.0|2.0|-24.0|2.0|50.0|
|Differential|r01|0.1|20.0|K|2.0|2.0|2.0|2.0|2.0|2.0|2.0|4.0|
|Maximum set point limitation|r02|-100.0|200.0|°C|50.0|6.0|4.0|-18.0|4.0|-20.0|50.0|70.0|
|Minimum set point limitation|r03|-100.0|200.0|°C|-35.0|2.0|0.0|-24.0|0.0|-26.0|-35.0|30.0|
|Display offset|r04|-10.0|10.0|K|0.0|0.0|0.0|0.0|0.0|0.0|0.0|0.0|
|Display Unit (°C/ °F)|r05|-C|-F||-C|-C|-C|-C|-C|-C|-C|-C|
|Calibration of Sair|r09|-20.0|20.0|K|0.0|0.0|0.0|0.0|0.0|0.0|0.0|0.0|

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Main switch ( -1=Service, 0=OFF, 1=ON,)|r12|-1|1||1|1|1|1|1|1|1|1|
|Night Set back|r13|-50.0|50.0|K|0.0|0.0|0.0|0.0|0.0|0.0|0.0|0.0|
|Reference displacement offset temperature|r40|-50.0|20.0|°C|0.0|0.0|0.0|0.0|0.0|0.0|-|0.0|
|Pull down duration|r96|0|960|min|0|0|0|0|0|0|-|-|
|Pull down limit temperature|r97|-100.0|200.0|°C|0.0|0.0|0.0|0.0|0.0|0.0|-|-|

### Alarm

**Table 32: Alarm**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Alarm**|**A--**||||||||||||
|Delay for temp alarm during normal conditions|A03|0|240|min|30|45|30|30|30|30|30|10|
|Delay for temp alarm during pull-down/start up/<br>defrost|A12|0|240|min|60|90|60|60|60|60|60|-|
|High temp. alarm limit|A13|-100.0|200.0|°C|8.0|10.0|8.0|-15.0|8.0|-15.0|8.0|80.0|
|Low temp. alarm limit|A14|-100.0|200.0|°C|-30.0|0.0|-2.0|-30.0|-2.0|-30.0|-30.0|20.0|
|DI1 delay (Time delay for selected DI1 function)|A27|0|240|min|30|30|30|30|30|30|30|30|
|DI2 delay (Time delay for selected DI2 function)|A28|0|240|min|30|30|30|30|30|30|30|30|
|Condenser High alarm limit|A37|0|200|°C|80|80|80|80|80|80|-|-|
|Condenser High block limit|A54|0|200|°C|85|85|85|85|85|85|-|-|
|Voltage protection|A72|no|YES||no|no|no|no|no|no|no|no|
|Minimum cut-in voltage|A73|0|270|V|0|0|0|0|0|0|0|0|
|Minimum cut-out voltage|A74|0|270|V|0|0|0|0|0|0|0|0|
|Maximum voltage|A75|0|270|V|270|270|270|270|270|270|270|270|

### Defrost

**Table 33: Defrost**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Defrost**|**d--**||||||||||||
|Defrost Method (no=None, nAt=Natural, EL = Elec-<br>tric; gAS=Hot gas)|d01|no|gAS||EL|nAt|EL|EL|EL|EL|EL|-|
|Defrost stop temperature.|d02|0.0|50.0|°C|6.0|-|-|-|6.0|6.0|6.0|-|
|Defrost Interval|d03|0|240|hour|8|6|8|12|8|12|8|-|
|Max defrost Time|d04|0|480|min|30|45|15|15|30|30|30|-|
|Defrost delay at power up (or DI signal)|d05|0|240|min|0|0|0|0|0|0|-|-|
|Drip delay|d06|0|60|min|0|0|0|0|0|0|2<sup>**(1)**</sup>|-|
|Fan delay after defrost|d07|0|60|min|0|0|0|0|0|0|5<sup>**(1)**</sup>|-|
|Fan start temperature after defrost|d08|-50.0|50.0|°C|-5.0|50.0<sup>**(1)**</sup>|50.0<sup>**(1)**</sup>|50.0<sup>**(1)**</sup>|-5.0|-5.0|NA|-|
|Fan during defrost|d09|OFF|on||on|on|OFF|OFF|OFF|OFF|OFF|-|
|Defrost stop sensor|d10|non|dEF||non|non<sup>**(1)**</sup>|non<sup>**(1)**</sup>|non<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|non|-|
|Accumulated Compressor runtime to start defrost<br>(0=OFF)|d18|0|96|hour|0|0|0|0|0|0|-|-|
|Defrost on demand (20=OFF)|d19|0.0|20.0|K|20.0|-|-|-|20.0|20.0|-|-|
|Defrost delay after pull down cycle|d30|0|960|min|0|0|0|0|0|0|-|-|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Fan control

**Table 34: Fan control**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Fan control**|**F--**||||||||||||
|Fan at compressor cutout|F01|FAo|FPL||FAo|FAo|FAo|FAo|FAo|FAo|FAo|FAo|
|Fan stop evap. Temperature|F04|-50.0|50.0|°C|50.0|-|-|-|50.0|50.0|50.0<sup>**(1)**</sup>|-|
|Fan ON Cycle|F07|0|180|min|2|2|2|2|2|2|2<sup>**(1)**</sup>|2|
|Fan OFF cycle|F08|0|180|min|2|2|2|2|2|2|2<sup>**(1)**</sup>|2|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Compressor

**Table 35: Com** **p ressor**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Compressor**|**c--**||||||||||||
|Compressor minimum ON time|C01|0|30|min|0|0|0|0|0|0|0|0|
|Compressor minimum OFF time|C02|0|30|min|2|2|2|2|2|2|2|2|
|Compressor /Heater OFF delay at open door|C04|0|900|Secs|900|900|900|900|900|900|60<sup>**(1)**</sup>|900|
|Zero crossing selection (YES / NO)|C70|no|YES||YES|YES|YES|YES|YES|YES|YES<sup>**(1)**</sup>|YES|

> **(1) This option is a default setting in the controller and cannot be changed.**

### Others

**Table 36: Others**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Others**|**o--**||||||||||||
|Delay of outputs at startup|o01|0|600|sec|10|10|10|10|10|10|10<sup>**(1)**</sup>|10|
|DI1 configuration<br>nC= Not configured; Sdc = Status display output,<br>doo = Door alarm with resumption, doA = Door<br>alarm without resumption, SCH = Main switch, nig<br>= Day/ Night mode, rFd = Reference displasement ,<br>EAL = External alarm, dEF = Defrost, Pud = Pull<br>down; Sc = Condensor Sensor|o02|nC|Sc||nC|nC|nC|nC|nC|nC|nC|nC|
|Serial address|o03|0|247|No|0|0|0|0|0|0|-|0.0|
|Password|o05|0|999|No|0|0|0|0|0|0|0|0|
|Sensor type selection (n5=NTC 5K, n10=NTC10K,<br>ptc=PTC, pt1=PT1000)|o06<sup>**(2)**</sup>|n10|ptc||n10|n10|n10|n10|n10|n10|n10|n10|
|Cooling/Heating (rE=Cooling, Ht= Heating)|o07<sup>**(2)**</sup>|rE|Ht||rE|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE<sup>**(1)**</sup>|rE|Ht<sup>**(1)**</sup>|
|Display Resolution|o15|0.1|1.0||0.1|0.1|0.1|0.1|0.1|0.1|0.1<sup>**(1)**</sup>|0.1|
|DO4 config (Lig=Light, ALA=Alarm)|o36<sup>**(2)**</sup>|Lig|ALA||Lig|Lig|Lig|Lig|Lig|Lig|Lig|Lig|
|DI2 configuration<br>nC= Not configured; Sdc = Status display output,<br>doo = Door alarm with resumption, doA = Door<br>alarm without resumption, SCH = Main switch, nig<br>= Day/ Night mode, rFd = Reference displasement ,<br>EAL = External alarm, dEF = Defrost, Pud = Pull<br>down|o37|nC|Pud||nC|nC|nC|nC|nC|nC|nC|nC|
|Light Control<br>on= Always on, dAn = Day/Night, doo=Based on<br>door action|o38|on|doo||on|on|on|on|on|on|on|on|
|Predefined applications|o61<sup>**(2)**</sup>|AP0|AP7||AP0|AP1|AP2|AP3|AP4|AP4|AP6|AP7|
|Save settings as factory|o67|no|YES||no|no|no|no|no|no|-|no|
|DO2 config (dEF=Defrost; ALA=alarm; Lig=Light)|o71<sup>**(2)**</sup>|dEF|Lig||dEF|ALA<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF<sup>**(1)**</sup>|dEF|ALA<sup>**(1)**</sup>|
|Display during defrost|o91|Air|-d-||-d-|-d-|-d-|-d-|-d-|-d-|-d-<sup>**(1)**</sup>|-|

> **(1) This option is a default setting in the controller and cannot be changed.**

> **(2) This parameter can only be set when regulation is stopped, i.e. “r12” is set to 0**

### Polarity

**Table 37: Polarit** **y**

|**Function**|**Code**|**Min.**|**Max.**|**Unit**|**AP0**|**AP1**|**AP2**|**AP3**|**AP4**|**AP5**|**AP6**|**AP7**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Polarity**|**P--**||||||||||||
|DI1 input polarity (nc/no)<br>no = normally open<br>nc = normally closed|P73|no|nc||no|no|no|no|no|no|no|no|
|DI2 input polarity (nc/no)<br>no = normally open<br>nc = normally closed|P74|no|nc||no|no|no|no|no|no|no|no|
|Invert alarm relay (0= normal, 1= invert relay ac-<br>tion)|P75|0|1||0|0|0|0|0|0|-|0.0|
|Key board lock (no / yes)(0=no, 1=yes)|P76|no|YES||no|no|no|no|no|no|-|no|

### **Alarm code**

In an alarm situation the display will alternate between readout of the actual air temperature and readout of the alarm codes of active alarms. Various alarm codes and their descriptions are as below.

**Table 38: Alarm codes**

|**Code**|**Alarms**|**Description**|
|---|---|---|
|E29|Sair sensor error|Air temperature sensor is defect or electrical connection is lost|
|E27|Def sensor error|S5 Evaporator sensor is defect or electrical connection is lost|
|E30|Sc sensor error|Sc Condenser sensor is defect or electrical connection is lost|
|A01|High temp alarm|Air temperature in cabinet is too high|
|A02|Low temp alarm|Air temperature in cabinet is too low|
|A99|High Volt alarm|Supply voltage is too high (compressor protection)|
|AA1|Low Volt alarm|Supply voltage is too low (compressor protection)|
|A61|Condenser alarm|Condenser temp. too high - check air flow|
|A80|Cond. block alarm|Condenser temp. too high - manual reset of alarm required<sup>**(1)**</sup>|
|A04|Door alarm|Door has been open for too long|
|A15|DI Alarm|External alarm from DI input|
|A45|Standby Alarm|Control has been stopped by "r12 Main switch"|

> **(1) The condenser block alarm can be reset by setting r12 Main switch OFF and ON again or by powering down the controller.**

### **Product specification**

### **Technical specif i** **cation**

**Table 39: Technical s** **p ecification**

|**Features**<br>Purpose of control|**Description**<br>Operating temperature sensing control suitable for incorporation into commercial air-conditioning and refrigeration appli-<br>cations|
|---|---|
|Construction of control|Incorporated control|
|Power supply|115 V AC / 230 V AC 50/60 Hz, galvanic isolated low voltage regulated power supply|
|Rated power|Less than 0.7 W|
|Inputs|Sensor inputs, Digital inputs, Programming key<br>Connected to SELV limited energy <15 W|
|Allowed sensor types|NTC 5000 Ohm at 25 °C, (Beta value=3980 at 25/100 °C - EKS 211)<br>NTC 10000 Ohm at 25 °C, (Beta value=3435 at 25/85 °C - EKS 221)<br>PTC 990 Ohm at 25 °C, (EKS 111)<br>Pt1000, (AKS 11, AKS 12, AKS 21)|
|Sensors included in kit Solution|NTC 10000 Ohm at 25 °C, cable length: 1.5 m|
|Accuracy|Measuring range:<br>-40 – 105 °C (-40 – 221 °F)|
||Controller accuracy:<br>±1 K below -35 °C, ±0.5 K between -35 – 25 °C<br>±1 K above 25 °C|
|Type of action|1B (relay)|
|Output|DO1 - Relay 1:<br>16 A, 16 (16) A, EN 60730-1<br>10 FLA / 60 LRA at 230 V, UL60730-1<br>16 FLA / 72 LRA at 115 V, UL60730-1|
||DO2 - Relay 2:<br>8 A, 2 FLA / 12 LRA, UL60730-1<br>8 A, 2 (2 A), EN60730-1|
||DO3 - Relay 3:<br>3 A, 2 FLA / 12 LRA, UL60730-1<br>3 A, 2 (2 A), EN60730-1|
||DO4 - Relay 4:<br>2 A|
|Display|LED display, 3 digits, decimal point and multi-function icons, °C + °F scale|
|Operating conditions|-10 – +55 °C (14 – 131 °F), 90% Rh|
|Storage conditions|-40 – +70 °C (-40 – +158 °F), 90% Rh|
|Protection|Front: IP65 (Gasket integrated)<br>Rear: IP00|
|Environmental|Pollution degree II, non-condensing|
|Overvoltage category|II - 230 V supply version - (ENEC, UL recognized)<br>III - 115 V supply version - (UL recognized)|
|Resistance to heat and fire|UL94-V0<br>Temperature for ball pressure test statement According to Annex G (EN 60730-1)|
|EMC category|Emission: IEC/EN 61000 6-3, Immunity: IEC/EN 61000 6-2|

### **Mounting**

*[Figurtekst: Fi g ure 16: Mountin g Fi g ure 17: Dismountin g · Danfoss 80G8391 Danfoss 80G8392]*

### Installation steps

- Place the wired controller in the slot and ensure rubber sealing is resting properly on the mounting surface.

- Slide the mounting clips along the rails of the rear plastic from the rear side of the panel.

- Slide the clips towards mounting surface until controller is firmly fixed.

- To remove the controller, one needs to skillfully unlatch the snapping tab and pull the clips backwards.

### **Dimensions**

##### **Fi** **g ure 18: Dimensions (mm)**

*[Figurtekst: 71 · 29 · 61.2 Drilling template · 83 66 · Rear mounting (lock with clips) · 36 28]*

### **Accessories**

### KoolKey (EKA200)

KoolKey acts as a gateway to connect PC tool KoolProg and also a programming key.

##### **Fi** **g ure 19: KoolKe** **y (EKA 200) as** **g atewa** **y**

*[Figurtekst: A Standard Micro-USB cable · B KoolKey · C Interface cable · D Controller · D · C · A B C · Fi g ure 20: KoolKe y  (EKA 200) as  p ro g rammin g  ke y · A Koolkey · B Interface cable · A B · C Controller · C]*

Refer to the KoolKey installation guide for detailed instructions.

### Mass Programming Key (EKA 201)

Mass Programming Key is a simple programming key for programming the controller in production assembly line.

*[Figurtekst: Fi g ure 21: Mass Pro g rammin g  Ke y  (EKA 201) · A EKA 201 · B Interface cable · A · B C Controller · C · Danfoss 0G8276 8]*

Refer to the EKA 201 installation guide for detailed instructions.

### Bluetooth Adapter (EKA 202 & EKA 203)

Bluetooth Adapter: external plug-in type module that provides wireless connectivity with Danfoss mobile application "KoolConnect".

**Fi** **g ure 22: Bluetooth Ada** **p ter (EKA 202 & EKA 203)**

*[Figurtekst: A Bluetooth adapter · B Interface cable · C Controller]*

Refer to the EKA 202/203 installation guide for detailed instructions.

### **Ordering**

**Table 40: ERC 21X controllers**

|**Type**|**Description**|**Relay**|**Qty.**|**Code no.**|
|---|---|---|---|---|
|ERC 211|ERC 211, Red LED, 115 V - Kit|1|1|080G3451|
||ERC 211, Red LED, 230 V - Kit|1|1|080G3453|
||ERC 211, Controller, Red LED, 230 V|1|1|080G3454|
||ERC 211, Controller, Red LED, 230 V, I-Pack|1|30|080G3459|
|ERC 213|ERC 213, Red LED, 230 V - Kit|3|1|080G3457|
||ERC 213, Controller, Red LED, 230 V|3|1|080G3458|
||ERC 213, Controller, Red LED, 230 V, I-Pack|3|30|080G3460|
||ERC 213 Red, 115 V USA - Kit|3|1|080G3467|
||ERC 213 Red, 230 V USA - Kit|3|1|080G3469|
|ERC 214|ERC 214, Controller, Red LED, 115 V - Kit|4|1|080G3466|
||ERC 214, Controller, Red LED, 230 V - Kit|4|1|080G3463|

**Table 41: Pro** **g rammin** **g tools and other accessories**

|**Type**|**Description**|**Qty.**|**Code no.**|
|---|---|---|---|
|EKA 200|KoolKey - Gateway cum Programming key|1|080N0020|
|EKA 201|Mass Programming Key|1|080N0021|
|BLE Adapter|Without RTC power back up|Single pack|080N0022|
|||54|080N0026|
||With RTC power back up|Single pack|080N0023|
|||54|080N0027|
|Interface cable|Interface cable for ERC 21x, 1 m|1|080N0326|
||Interface cable for ERC 21x, 0.5 m|1|080N0327|

**Table 42: Sensors**

|**Type**|**Sensor element**|**Sensor housing**|**Cable**|**Qty.**|**Code no.**|
|---|---|---|---|---|---|
|EKS 211|NTC 5000 ohm / 25 °C (Beta =3980 at 25/100 °C)|Thermo plastic polyester 8x30|1.5 m|150|084B4403|
|||Thermo plastic polyester 8x30|3.5 m|75|084B4404|
|||Thermo plastic polyester 8x30|1.5 m|1|084N1220|
|||Thermo plastic polyester 8x30|3.5 m|1|084N1221|
|EKS 221|NTC 10000 ohm / 25 °C (Beta =3435 at 25/85 °C)|Thermo plastic rubber 6x5x15|3.5 m|150|084N3206|
|||Thermo plastic rubber 6x5x15|3.5 m|1|084N3210|
|||Thermo plastic rubber 6x5x15|8.5 m|50|084N3208|
|||Thermo plastic rubber 6x5x15|8.5 m|1|084N3209|
|||Stainless steel 6x20|1.5 m|150|084N3200|
|EKS 111|PTC 990 ohm / 25 °C|Stainless steel 6x30|1.5 m|1|084N1178|
|||Stainless steel 6x30|1.5 m|150|084N1161|
|||Stainless steel 6x30|3.5 m|1|084N1179|
|||Stainless steel 6x30|3.5 m|150|084N1163|
|||Stainless steel 6x30|6 m|1|084N1180|
|||Stainless steel 6x30|6 m|80|084N1173|
|||Stainless steel 6x30|8.5 m|60|084N1168|
|AKS 11|PT1000|Top part: PPO (Noryl)|3.5 m|1|084N0003|
|||Bottom: stainless steel||||
|||Top part: PPO (Noryl)|5.5 m|1|084N0005|
|||Bottom: stainless steel||||
|||Top part: PPO (Noryl)|8.5 m|1|084N0008|
|||Bottom: stainless steel||||
|AKS 12|PT1000|Stainless steel 6x40|1.5 m|1|084N0036|
|||Stainless steel 6x40|1.5 m|30|084N0035|
|||Stainless steel 6x40|3.5 m|30|084N0039|
|||Stainless steel 6x40|5.5 m|30|084N0038|

 **NOTE:**

All the mounted sensors must be of same type.

### **Certificates, declarations, and approvals**

The list contains all certificates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

Some approvals may change over time. You can check the most current status at danfoss.com or contact your local Danfoss representative if you have any questions.

### **Certif i** **cates, declarations, and approvals**

**Table 43: Certificates, declarations, and a** **pp rovals**

|**Regulatory and Compliance**|**Directive / Document topic**|**Standards**|**Country - Marking**|
|---|---|---|---|
|Electrical Safety (Incorporated Control<br>for use in Class I or Class II equipment)|Low Voltage Directive: 2014/35/EU|EN IEC 60730-2-9:2019, EN IEC<br>60730-2-9:2019/A1:2019, EN IEC<br>60730-2-9:2019/A2:2020, EN<br>60730-1:2016,<br>EN 60730-1:2016/A1:2019, EN<br>60730-1:2016/A2:2022|Europe - CE|
|Electrical Safety (control is validated to<br>use as Incorporated)|Recoganized Component|UL 60730-1 - 2009 - Revision 2014,<br>UL 60730-2-9 : 2010, Revision : 2013|United States -CURUS|
|Electrical Safety (control is validated to<br>use as Incorporated)|Recoganized Component|CSA E60730-1 :2013, CSA E60730-2-9 :<br>2001, Revision : 2008, AMD 1|Canada -CURUS|
|Electrical Safety (Incorporated Control<br>for use in Class I or Class II equipment)|-|GB 14536.1:2008, GB 14536.10:2008|China - CQC|
|Electrical Safety & Electromagnetic<br>Compatibility|Supplier Declaration of Conformity<br>(SDoC)|EN 60730-1:2016, EN 60730 2-9:2019,<br>EN 610006-2:2005 & EN<br>61000-6-3:2007+A1:2011|Ukraine - UA|
|Elelctrical Safety|Certification of Conformity (CoC)|CU TR 004/2011|Eurasia - EAC|
|Electromagnetic Compatibility|EMC Directive: 2014/30/EU|EN 610006-2:2005 & EN<br>61000-6-3:2007+A1:2011|Europe - CE|
|RoHS|RoHS Directive: 2011/65/EU &<br>2015/863/EU|EN IEC 63000:2018|Europe - CE|
|Food Safety|Food Equipment|NSF/ANSI standard 2|United States|
|Approved for use in Flammable Refrig-<br>erants|Enclosed Break Device / sealed device<br>nC (Relays)|Sealed Device "nC" IEC 600079-15:2017,<br>Enclosed-Break device "dC" IEC<br>60079-1:2014, clause 15.5.3|Europe|
|Approved for use in Flammable Refrig-<br>erants|Enclosed Break Device (Relays)|Sealed device "nC" UL 60079-15 and<br>CAN/CSA C22.2 No. 60079-15, Enclosed-<br>Break device "dC" IEC 60079-1:2014,<br>clause 15.5.3|US and Canada|
|Enclosure Material Flammable Class|-|UL 94, V-0|US|
|HACCP, Temperature Measuring probe<br>in compliance with EN13485 Class I,<br>when used with AKS 12 sensor|-|EN 13485:2001|Europe|
|Certification and Manufacturer Declara-<br>tions on Conformity|CE,CURUS, CQC, UA, EAC, NSF, RoHS|||

### **Online support**

Danfoss offers a wide range of support along with our products, including digital product information, software, mobile apps, and expert guidance. See the possibilities below.

#### **The Danfoss Product Store**

The Danfoss Product Store is your one-stop shop for everything product related—no matter where you are in the world or what area of the cooling industry you work in. Get quick access to essential information like product specs, code numbers, technical documentation, certifications, accessories, and more.

Start browsing at store.danfoss.com.

#### **Find technical documentation**

Find the technical documentation you need to get your project up and running. Get direct access to our official collection of data sheets, certificates and declarations, manuals and guides, 3D models and drawings, case stories, brochures, and much more.

Start searching now at www.danfoss.com/en/service-and-support/documentation.

Danfoss Learning is a free online learning platform. It features courses and materials specifically designed to help engineers, installers, service technicians, and wholesalers better understand the products, applications, industry topics, and trends that will help you do your job better.

Create your Danfoss Learning account for free at www.danfoss.com/en/service-and-support/learning.

#### **Get local information and support**

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest regional news, or connect with a nearby expert—all in your own language.

Find your local Danfoss website here: www.danfoss.com/en/choose-region.
