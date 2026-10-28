# Danfoss AK-CC55 Compact – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Case/room controller (EEV) Type AK-CC55 Compact

*Kilde: Danfoss-dokument BC365212986197en-000201.pdf*

#### **User Guide**

Case/room controller (EEV) Type **AK-CC55 Compact**

**SW Ver. 2.1x** For refrigeration appliances and cold storage rooms.

|**Contents**||
|---|---|
|**Introduction**|**5**|
|**Portfolio overview**|**6**|
|Function overview|6|
|Connectivity|7|
|Data communication|7|
|AK-CC55 Compact|7|
|External display|7|
|**Controller functionality**|**9**|
|Functions|9|
|Injection control|9|
|Adaptive superheat control|9|
|Adaptive liquid control|9|
|Thermostatic expansion valve control|10|
|Temperature control|11|
|Temperature monitoring|11|
|Thermostat bands|11|
|Night setback of thermostat value|12|
|Temperature sensor types|12|
|Appliance cleaning|13|
|Appliance shutdown|13|
|Defrost|14|
|Electrical defrosting|14|
|Simple hot gas defrosting|14|
|Natural defrost|14|
|Start of defrost|14|
|Stop of defrost|15|
|Defrost sequence|15|
|Real-time clock|16|
|Coordinated defrost|16|
|Melt function|17|
|Control of two compressors (only with custom set-up)|17|
|Rail heat|18|
|Fan|19|
|Light function|20|

|Night blind|20|
|---|---|
|Heating function (only with custom set-up)|21|
|Digital inputs|21|
|Forced closing|21|
|Door contact|22|
|Display|22|
|Override|22|
|**Applications**|**24**|
|AK-CC55 Compact connections and application options|24|
|Application set-ups and IO connections|25|
|Product identification|28|
|AK-CC55 Compact connections|29|
|Data communication|29|
|AKV info|29|
|External solid state relay for rail heat|30|
|AKS 32R info|30|
|Coordinated defrost via cable connections|30|
|External display AK-UI55|31|
|Connections|31|
|**Operation**|**33**|
|Operation via data communication|33|
|Direct operation|33|
|Operation via AK-UI55 Set|33|
|Parameter groups when operating via display|35|
|Get a good start|35|
|**AK-UI55 display menu (SW ver. 2.1x)**|**37**|
|Thermostat|37|
|Alarm settings|37|
|Compressor|38|
|Defrost|38|
|Injection control|38|
|Fan control|39|
|Defrost schedule|39|
|Miscellaneous|39|
|Control|41|
|DO config and manual|41|

|Service|42|
|---|---|
|**Operation via AK-UI55 Bluetooth**|**44**|
|**AK-CC55 Connect menu (SW ver. 2.1x)**|**45**|
|Start / Stop|45|
|Configuration|45|
|Thermostat control|46|
|Alarm limits and delays|48|
|Injection control|49|
|Defrost control|49|
|Defrost schedules|51|
|Compressor|51|
|Fan control|52|
|Railheat control|52|
|Light/Blinds/Cleaning control|53|
|Display control|54|
|Alarm relay priorities|54|
|Miscellaneous|55|
|Advanced|55|
|Fault message|57|
|**Operating status**|**58**|
|**Product specification**|**59**|
|Technical data|59|
|Electrical specifications|59|
|Sensor and measuring data|59|
|Input and output relay specifications|59|
|Function data|60|
|Environmental conditions|60|
|Dimensions|60|
|**Ordering**|**61**|
|**Certificates, declarations, and approvals**|**62**|
|Statements for the AK-UI55 Bluetooth display|63|
|**Online support**|**64**|

### **Introduction**

##### **Application**

Refrigeration appliance control with great flexibility to adapt to refrigeration appliances and cold storage rooms.

##### **Advantages:**

- Control of Thermostatic Expansion Valve (TEV) and Electronic Expansion valve(EEV) applications

- Quick set-up with predefined settings

- Easy configuration and service using a mobile app with Bluetooth

- Adaptive Minimum Stable Superheat (MSS) control is performed with lowest possible superheat

- Allows the suction pressure to be raised several degrees

- Adaptive Liquid Control (ALC) can be performed with superheat down to 0 degrees on transcritical CO2 systems with liquid ejectors

##### **Principle**

The temperature in the appliance is registered by one or two temperature sensors which are located in the air flow before the evaporator (S3) or after the evaporator (S4) respectively. A setting for thermostat, alarm thermostat and display reading determines the influence the two sensor values should have for each individual function.

The temperature of the evaporator is registered with the S5 sensor which can be used as a defrosting sensor.

In addition to the output of the electronic AKV injection valve, the controller has relay outputs which are defined by the application setting

###### **Fi** **g ure 1: AK-CC55 with eva** **p orator, AKV valve and sensor positions**

*[Figurtekst: S4 · S2 P · S5 · AKV · S3]*

### **Portfolio overview**

The AK-CC55 portfolio contains four controllers with different functionalities and application settings, as outlined in the table.

**Table 1: AK-CC55 Portfolio**

||**AK-CC55 Compact**|**AK-CC55 Single Coil**|**AK-CC55 Single Coil UI**|**AK-CC55 Multi Coil**|
|---|---|---|---|---|
|Product image|||||
|Valve|1 x TXV or AKV|1 x AKV|1 x AKV|3 x AKV|
|Digital Output|3|5|5|4|
|Digital input|1 (2)|3 (2)|3 (2)|3 (2)|
|Analogue Output|1|1|1|1|
|Analogue Input|5 (4)|6 (7)|6 (7)|6 (7)|
|Display|1 remote|2 remote|1 remote + 1 Integrated|2 remote|
|Comm. module|Modbus|Modbus|Modbus|Modbus|
|Optional comm. module||LON module|LON module|LON module|

### **Function overview**

**Table 2: AK-CC55 function overview b** **y t** **yp e**

|**Application**|**AK-CC55 Compact**|**AK-CC55 Single Coil**<br>**AK-CC55 Single Coil UI**|**AK-CC55 Multi Coil**|
|---|---|---|---|
|AKV - application (electrically operated expansion valve)|x|x|x|
|0 – 10 V to control external stepper driver||x||
|TXV - application (thermostatic expansion valve + solenoid valve or compressor)|x|||
|Remote hot gas - application||x||
|One valve, one evaporator, one refrigeration section|x|x|x|
|One valve, one evaporator, two refrigeration sections||x||
|One valve and two evaporators, two refrigeration sections||x||
|Two valves and two evaporators (same refrigeration section)|||x|
|Three valves and three evaporators (same refrigeration section)|||x|
|Custom configuration of relay outputs|x|x||
|Two compressors|x|x||
|Heating function|x|x||
|Control of air humidity||x|x|
|Adaptive superheat|x|x|x|
|Adaptive liquid control<br>(zero superheat control for transcritical CO2systems with liquid ejectors)|x|x|x|
|Adaptive defrosting||x||
|Product sensor||x||
|Oil recovery||x||
|RS485 Lon, option (AK-OB55)||x|x|

### **Connectivity**

The diagram outlines the connectivity options presented by AK-CC55 for the design of system functionality.

###### **Fi** **g ure 2: Connectivit** **y**

*[Figurtekst: AKA 245: LON units · only and max 250 · controller parameters · System Manager · Bluetooth AK-CC55 Connect · AK-CC55 Compact AK-UI55 Bluetooth · AK-UI55 Set · AK-CC55 Multi Coil · Smart Device · KoolProg (iOS or Android) · AK-UI55 Info · AK-CC55 Single Coil UI · Case Controller Remote Display Service App · Modbus · Modbus LON/ TCP/IP (SNMP) · Modbus LON/ TCP/IP (SNMP) · Display Bus]*

### **Data communication**

The AK-CC55 Compact controller has built-in MODBUS data communication only.

### **AK -** **CC55 Compact**

Compact version for controlling one evaporator.

An application mode setting will configure inputs and outputs for the desired use. There are nine applications to choose from.

Regulation is performed using a TXV in combination with a liquid line solenoid valve, controlling a compressor or an AKV expansion valve.

AK-CC55 Compact is without display, and can be extended with one external display (see Figure 3 and Figure 4):

###### **Fi** **g ure 3: AK-CC55 Compact Fi** **g ure 4: AK-CC55 Com** **p act with external display.**

### **External display**

There are three versions available with different functions:

- AK-UI55 Info: Temperature display.

- AK-UI55 Set: Temperature display with control buttons on the front.

- AK-UI55 Bluetooth: Temperature display with Bluetooth communication, for use with AK-CC55 Connect Mobile app.

**Figure 5: AK-UI55 Info**

**Figure 6: AK-UI55 Set**

**Figure 7: AK-UI55 Bluetooth**

### **Controller functionality**

### **Functions**

- Day/night thermostat with ON/OFF or modulating principle

- Switch between thermostat settings via digital input

- Adaptive superheat control

- Adaptive liquid control

- Modulating PWM control of brine valve

- Start of defrost via schedule, digital input, network or setting display

- Natural, electric, simple hot gas, or warm brine defrost.

- Stop of defrost on time and/or temperature

- Coordination of defrosting among several controllers in a line-up

- Pulsing or ECO control of fans when thermostat is satisfied

- Appliance cleaning function for documentation of HACCP procedure

- Rail heat control via day/night load or dew point

- Door function

- Control of two compressors

- Control of night blinds

- Light control

- Heat thermostat

- High accuracy inputs:

- to guarantee a better measuring accuracy than stated in the standard EN ISO 23953-2 without subsequent calibration (Pt1000 ohm sensor).

- Support of user defined temp. sensor type

- Integrated MODBUS communication

### **Injection control**

### Adaptive superheat control

Liquid injection in the evaporator is controlled by an electronic injection valve of the type AKV. The valve operates as both expansion valve and solenoid valve. The controller opens and closes the valve based on sensor readings.

###### **Fi** **g ure 8: Ada** **p tive su** **p erheat control with AKV valve**

*[Figurtekst: pe · S2 · AKV Danfoss 84B2732]*

The superheat is measured via a pressure sensor Pe and temperature sensor S2. By using a pressure sensor, and temperature sensor a correct measurement of superheat is achieved under all conditions which ensures a very robust and precise control. The signal from one pressure transmitter can be shared by max. 10 controllers, but only if there is no significant pressure difference between the evaporators in question.

The function contains an adaptive algorithm which independently adjusts the valve’s opening so that the evaporator constantly supplies optimum amount of refrigerant.

### Adaptive liquid control

Adaptive liquid control is used in trans-critical CO2 ejector systems, which allow liquid flow. When adaptive liquid control is initiated, the superheat of the evaporator will be minimized so that a controlled amount of liquid is present at the outlet of the evaporator.

This type of control requires that the controller receives an on/off signal from (for example) a suction accumulator in the suction line.

###### **Fi** **g ure 9: Ada** **p tive li** **q uid control with AKV valve**

A level switch in the tank will register when the liquid level exceeds the max. level. When this happens, the controller will switch to dry expansion, and then back to liquid control when the liquid level has dropped. The function is defined in setting o02, o37 or o84.

The function can also be activated via data communication from a system unit. If the adaptive liquid control signal is lost, the controller will automatically switch back to dry expansion.

######  **WARNING:**

Accidental actuation may allow liquid throughput to the compressor. It is the installer’s responsibility to ensure that signal loss to the controller will not result in liquid throughput to the compressor. Danfoss accepts no responsibility for damage resulting from inadequate installation.

### **Thermostatic expansion valve control**

In the compact version the refrigeration (injection) can be controlled either by starting/stopping a compressor or by opening/closing a solenoid valve in the liquid line.

**Figure 10: AK-CC55 Compact with evaporator, solenoid valve, ex** **p ansion valve and sensor** **p ositions**

##### **Brine control**

When changing from ON/OFF control to modulating control in TXV applications, a solenoid valve can be PWM controlled with a set period time from 30 – 900 sec. A number of additional brine control parameters are available in the injection control menu. When brine control is enabled, a dedicated brine defrost can also be set up in order to force open the brine valve while defrosting.

### **Temperature control**

The temperature in the appliance is registered by one or two temperature sensors which are located in the return air before the evaporator (S3) or after the evaporator (S4) respectively. A setting for the thermostat, night thermostat, alarm thermostat and display reading determines how much the two sensor values should influence each individual function, e.g. 50% of S4 will produce an equal value from both sensors.

The actual temperature control can take place in two ways:

1. As an ordinary ON/OFF regulation with a differential, or 2. As a modulating control where the temperature variation will not be nearly as high as in ON/OFF control.

There is, however, a limit to the use of a modulating control as it can only be used in remote cabinets. It is not recommended to use modulating thermostat control in low temperature applications. In applications with one evaporator and one compressor, the thermostat function with ON/OFF control should be selected. In remote cabinets, the thermostat function may either be selected for ON/OFF control or modulating control.

**Table 3: Control methods**

*[Figurtekst: ON/OFF control Modulating control]*

### **Temperature monitoring**

Just as is possible for the thermostat, the alarm monitoring can be set with a weighting between S3 and S4 so that you can decide how much the two sensor values should influence the alarm monitoring. Minimum and maximum limits can be set for alarm temperature and time delays. A longer time delay can be set for high temperature alarm. This time delay is active for pull-down, after defrosting, appliance cleaning and start-up.

### **Thermostat bands**

Thermostat bands can be used beneficially for appliances where different product types are stored, which requires different temperature conditions. It is possible to change between the two different thermostat bands via a contact signal on a digital input. Separate thermostat and alarm limits can be set for each thermostat band.

For the defrost control, separate defrost stop temperature and max. defrost time can be set for each thermostat band. For the compressor control it is possible to disable the second compressor in thermostat band 2 if required.

**Fi** **g ure 11: Thermostat band function with two different band settings**

### **Night setback of thermostat value**

In refrigeration appliances there may be big load differences between the shop’s opening and closing hours, especially if night lids/blinds are used. The thermostat reference may be raised here without it having any effect on the product temperature.

Change-over between day and night operation can take place as follows:

- via an external switch connected to a digital input

- via a signal from the data communication system

###### **Fi** **g ure 12: Thermostat band function with Ni** **g ht setback**

### Temperature sensor types

The S2 and S6 sensors always have to be Pt1000 sensors due to the high measuring accuracy.

For the S3, S4 and S5 sensors, the user can select between the following sensor types:

0 = Pt1000 (Danfoss AKS 11)

1 = PTC1000 (Danfoss EKS 111)

- 2 = NTC 5k (Danfoss EKS 211)

- 3 = NTC 10k (Danfoss EKS 221)

4 = User-defined

If “User-defined” is selected, three sensor measuring points must be provided and based on these three sensor points, a sensor characteristic is generated.

A sensor point is defined by setting a temperature value and the corresponding resistance value at this temperature. The resistance value is set via two values for kohm and ohm respectively. These values can be found in the data sheet for the sensor.

The three sensor points must be:

1. Lowest temperature in wanted measuring range 2. Highest temperature value in wanted temperature range

3. Temp. value in the middle where a high measuring accuracy is required

A sensor error is detected at temperature values below/above the min./max. temperature values typed in for the sensor points.

*[Figurtekst: Fi g ure 13: Exam p le of sensor  p oints from a NTC sensor · y x Temp [°C] · 350 y R [kohm] · A Sensor point (-30 °C, 180 kΩ) · 300 · 250 · 200 · A · 150 · 100 · 50 · 0 x · -40 -20 0 20 40 60 80]*

##### **Limitations:**

A user defined temperature sensor can only be be defined within the temperature range from -40 – +60 °C and within the resistance range from 400 – 179.999 ohm.

When applying a new user defined sensor type, please contact Danfoss for validation of compliance and measuring accuracy.

### **Appliance cleaning**

This function makes it easy for the shop’s staff to carry out a cleaning of the appliance according to a standard procedure. Appliance cleaning is activated via a pulse signal – as a rule via a key switch placed on the appliance or via the AK-CC55 Connect mobile app.

Appliance cleaning is carried out via three phases:

1. At the first activation, the refrigeration is stopped, but the fans keep on operating in order to defrost the evaporators. ”Fan” is shown on the display.

2. At the second activation, the fans are also stopped and the appliance can now be cleaned. ”OFF” is shown on the display.

3. At the third activation, refrigeration is recommenced. The display will show the actual appliance temperature, o97 setting.

When appliance cleaning is activated, a cleaning alarm is transmitted to the normal alarm recipient. A later processing of these alarms will document that the appliance has been cleaned as often as planned.

There are no temperature alarms during appliance cleaning.

**Table 4: A** **pp liance cleanin** **g function**

|-|+|+<br>°C|
|---|---|---|
|1|÷|+<br>Fan|
|2|÷|÷<br>Off|
|3|+|+<br>°C|

### **Appliance shutdown**

The function closes the AKV valve and all outputs are switched off. The cooling appliance is stopped like the “Main switch”, but this happens without an “A45 standby alarm”. The function can be enabled by a switch on the DI input or via a setting through data communication.

### **Defrost**

Depending on the application, you may choose between the following defrost methods:

- Natural: Here the fans are kept operating during the defrost

- Electric: The heating element is activated

- Hot gas: Simple hot gas defrost can be selected in application modes where a compressor is controlled. The compressor unit will operate during defrosting

- Brine defrost: The brine valve is forced open while defrosting (only possible when selecting modulating control in TXV applications)

### Electrical defrosting

At electrical defrost, an electrical heater is placed in front of the evaporator and the fan will “pull” the hot air through the evaporator during defrosting.

###### **Fi** **g ure 14: Electrical defrostin** **g**

*[Figurtekst: S3 · S5 · M M · S4]*

### Simple hot gas defrosting

If hot gas defrost is selected in application 1-5, the compressor will be running during defrost and a hot gas valve (HGV) is bypassing the compressor discharge gas to the evaporator inlet and thereby the evaporator is defrosted.

### Natural defrost

At natural defrost, the ice is melted by running the fans and thereby circulating warm air through the evaporator.

###### **Fi** **g ure 15: Natural defrost**

*[Figurtekst: S3 · S5 · M M · S4]*

### **Start of defrost**

A defrost can be started in different ways:

##### **Interval:**

Defrost is started at fixed time intervals like e.g. every eighth hour. An interval must ALWAYS be set to a "higher" value than the period set between two defrostings when a schedule or network signal is used.

##### **Week schedule:**

Here defrost can be started at fixed times of the day and night. However, max. 6 defrosts per day.

##### **Contact:**

Defrost is started with a contact signal on a digital input.

###### **Fi** **g ure 16: Defrost start**

##### **Network:**

The defrost start signal is received from a system manager via data communication.

##### **Max. thermostat runtime:**

When the aggregate time has passed a preset value, a defrost will be initiated.

##### **Manual:**

An extra defrost can be activated from the defrost button on the AK-UI55 Set display via the app, or via the parameter setting. All the mentioned methods can be used in parallel – if just one of them is activated, a defrost will be started.

### **Stop of defrost**

Defrosting can be stopped by either:

- Time

- S4A temperature (with time as safety)

- S5A temperature (with time as safety)

When the selected defrost stop sensor reaches the set defrost stop limit, the defrost is terminated. If the defrost stop sensor does not reach the set defrost stop limit within the set max. defrost time, the defrost will be terminated on time.

##### **Minimum defrost time**

When using hot gas for defrosting, the heat is coming from within the evaporator, and this means that the S5 sensor is rising fast when the inner layer of ice is melted. This will sometimes cause parts of the evaporator not to be defrosted when defrost is terminated on S5 evaporator temperature.

To prevent this, the user is given the option of setting a minimum defrost time. When a defrost is initiated, it will have to run for the set minimum time even if the set defrost stop limit has been reached by the selected defrost stop sensor.

### **Defrost sequence**

When a defrost is initiated, the controller will run through the following sequence:

1. **Pump down:** where the evaporator is emptied of refrigerant

2. **Defrost:** where the ice on the evaporator is melted

3. **Hold after defrosting:** where multiple controllers wait for each other (coordinated defrost)

4. **Drip off:** where remaining water is dripping off evaporator

5. **Drain delay (Hot gas only):** where the drain valve is opened to drain the liquid refrigerant

6. **Fan delay:** where the fans are restarted when the remaining water on the evaporator has turned into ice

*[Figurtekst: Fi g ure 17: Electrical defrost se q uence · x Time · A Pump down · AKV B Defrost · C Hold · D Drip · E Fan delay · X · A B C D E]*

During an electrical defrost sequence where the defrost heater is ON during defrost, AKV valve is closed and fans are running during defrost but stopped during drip.

##### **Fan control during defrost**

During the defrost sequence, the evaporator fans can be controlled in one of the following ways:

1. The fan is OFF in the entire defrost sequence

2. The fan is ON during the entire defrost sequence except during fan delay state

3. The fan is ON during defrost state and is OFF in the rest of the defrost sequence

4. Like option 2, however the fans can be stopped if the selected defrost stop sensor exceeds a set fan stop limit

### **Real -** **time clock**

The controller has a built-in real-time clock which can be used to start defrosts. This clock has a power reserve of four days.

If the controller is equipped with data communication, the clock will automatically be updated from a Danfoss system manager.

### **Coordinated defrost**

There are two ways in which coordinated defrost can be arranged.

###### **Fi** **g ure 18: Coordinated defrost o** **p tions**

*[Figurtekst: Max 10. · System manager]*

Either with wire connections between the controllers or via data communication:

##### **Wire connections**

The digital input DI2 must be configured for coordinated defrost and wiring must be connected between the relevant controllers. When one controller starts a defrost, all the other controllers will follow suit and likewise start a defrost. After the defrost, the individual controllers will move into waiting position. When all are in waiting position there will be a change-over to refrigeration.

##### **Coordination via data communication**

Here the system manager handles the coordination. The controllers are gathered in defrosting groups and the system manager ensures that defrosting is started in the group according to a weekly schedule.

When a controller has completed defrosting, it sends a message to the system manager and then goes into a waiting position. When every controller in the group is in a waiting position, refrigeration is again permitted in all the individual controllers.

### **Melt function**

This function will prevent the air flow in the evaporator from being reduced by frost created by uninterrupted operation for a long time.

The function is activated if the thermostat temperature has remained in the range between -5 °C and +10 °C for a longer period than the set melting interval. The refrigeration will then be stopped during the set melting period. The frost will be melted so that the air flow and hence the evaporator’s capacity will be greatly improved.

### **Control of two compressors (only with custom set -** **up)**

Two compressor steps can be controlled cyclic or sequentially. At cyclic control, two compressors must be of the same size, while in sequential control compressor step 1 can be larger than step 2.

###### **Fi** **g ure 19: Control of two com** **p ressors.**

##### **Cyclic control**

When the controller demands refrigeration, it will first cut in the compressor with the shortest operating time. After the time delay, the second compressor will be cut in.

When the temperature has dropped to ”the middle of the differential”, the compressor with the longest operation time will be cut out.

The running compressor will continue until the temperature has reached the cut-out value. Then it will cut out. When the temperature again reaches the middle of the differential, a compressor will again be started.

If one compressor cannot maintain the temperature within the differential, the second compressor will also be started.

If one of the compressors has run on its own for two hours, the compressors will be changed over so that operational time is balanced.

The two compressors must be of a type that can start up against a high pressure.

The compressor's settings for ”Min. On time” and ”Min. Off time” will always have top priority during normal regulation. But if one of the override functions is activated, like e.g. defrost, door open function, case shutdown, forced closing, the ”Min. On time” will be disregarded.

##### **Sequential control**

Compressor steps are controlled in the same manner as described for cyclic control, but compressor step 1 will always be started first and cut out as the last one. No time equalization is available in sequential control mode.

##### **Thermostat band**

In thermostat band 2, it is possible to disable the operation of the second compressor.

### **Rail heat**

It is possible to pulse-control the power to the rail heat in order to save energy. Pulse control can either be controlled according to day/night load or dewpoint.

##### **Relay or analogue output**

A relay output can be used when long cycle times are permitted. If fast pulsing is required, the AO1/PWM output can be used. The output must be connected to an external power solid state relay. The cycle time must be configured for the relay output in o43 or for analogue output in P82.

##### **Pulse control according to day and night**

Various ON periods can be set for day and night operation. A cycle time is set as well as the percentage part of the period in which the rail heat is ON.

###### **Fi** **g ure 20: Rail heat control, da** **y /ni** **g ht load.**

##### **Pulse control according to dewpoint**

In order to use this function, a system manager of the type AK-SM is required which can measure ambient temperature and humidity to calculate dewpoint and distribute to the appliance controllers. For this the rail heat’s ON period is controlled according to the distributed dewpoint.

Two dewpoint values are set in the appliance control:

- One where the effect must be max. i.e. 100%. (o87)

- One where the effect must be min. (o86)

At a dewpoint which is equal to or lower than the value in 086, the effect will be the value indicated in o88. In the area between the two dewpoint values, the controller will manage the power to be supplied to the rail heat.

###### **Fi** **g ure 21: Rail heat control, dew** **p oint**

*[Figurtekst: 100% · o88 · o86 o87]*

##### **During defrosting**

During defrosting rail heat will be active, as selected in setting d27.

### **Fan**

##### **Pulse control**

To obtain energy savings, it is possible to pulse control the power supply to the evaporator fans. Pulse control can be accomplished in one of the following ways:

- during the thermostat’s cut-out period (cold room)

- during night operation and during the thermostat’s cut-out period (appliance with night blinds) (The function is not actual when r14=2, i.e. modulating regulation).

A period of time is set as well as the percentage of this period of time where the fans have to be operating.

###### **Fi** **g ure 22: Fan c** **y cle time**

##### **Cut-out of fans during plant breakdowns**

If the refrigeration in a breakdown situation stops, the temperature in the cold room may rise quickly as a result of the emission of heat from large fans. In order to prevent this situation, the controller can stop the fans if the temperature at S5 exceeds a set limit value. The fans will start running again when the S5 temperature has dropped 2K below the set limit. (The function can also be used as a type of MOP function. Here the load on the compressors is limited until the S5 temperature has fallen below the configured value).

##### **Fan ECO operation (only custom set-up)**

Fan ECO operation is used to reduce fan speed during night operation – typically on cabinets with night blinds.

The function is enabled when a relay has been configured for Fan ECO function in one of the applications with custom set-up of relay functions.

The fan economy control (fan speed) is controlled via the two fan outputs:

- Fan output

- Fan Eco output

If the Fan output is activated, then the fan is running with 100% speed. If the Fan ECO output is also activated, then the fan is running with reduced speed (typically 50%). If both fan outputs are de-activated, then the fans are stopped.

###### **Fi** **g ure 23: Fan ECO control – Fan s** **p eed reduced to 50% durin** **g night operation**

*[Figurtekst: Y X Time · Y Fan speed · 100% A Fan · B Fan ECO · 50% · X · 0% · A · B]*

The fans will always run with full speed during day operation, first stage of case cleaning, defrost, forced cooling and when air heating is active.

### **Light function**

The function can be used for controlling the light in a refrigeration appliance or in a cold room. It can also be used for controlling a motorised night blind.

The light function can be defined in several ways:

1. The light is controlled via the day/night function. A digital input setup for light control can switch light ON, if the light is switched off during night

2. The light is controlled by a system manager via the parameter o39. A digital input setup for light control can switch light ON, if the light is switched off by the system manager.

3. Light is controlled via the door switch. Light is switched ON when door is opened and switched OFF 2 minutes after the door has been closed.

4. Like option 2, but here the light is switched ON automatically if the communication to the system manager has been lost for 15 minutes

5. Light is only controlled via a digital input setup for light control

The light load must be connected to the NC terminals on the relay.

This ensures that the light remains ON in the appliance if power to the controller should fail.

A setting defines how light is controlled when regulation is stopped via r12 Main switch = OFF (see o98). The light is switched off when the appliance cleaning function is activated.

### **Night blind**

Motorised night blinds can be controlled automatically from the controller. The night blinds will follow the status of the light function. When the light is switched on, the night blinds open, and when the light is switched off, the night blinds close again. When the night blinds are closed, it is possible to open them using a switch signal on the digital input. If this pulse signal is activated, the night blinds will open and the refrigeration appliance can be filled with new products. If the pulse signal is activated again, the blinds close.

When the night blind function is used, the thermostat function can control with different weighting between the S3 and S4 sensors. A weighting during day operation and another when the blind is closed.

A night blind is opened when the appliance cleaning function is activated.

A setting can define that the night blind is opened when "r12" (Main switch) is set to off (see o98).

When the night blind rolls down, the fan will be stopped for the set time. The night blind can thereby roll down to the correct position.

### **Heating function (only with custom set -** **up)**

The heating function is used to prevent the temperature from becoming too low, e.g. in a cold room, etc. The limit for when the heating function cuts off is set as an offset value below the current cut-out limit for the refrigeration thermostat. This ensures that refrigeration and heating do not occur simultaneously. The difference for the heating thermostat has the same value as for the refrigeration thermostat. To prevent that the heating thermostat cuts in during short-term drops in air temperature, a time delay can be set for when to change from refrigeration to heating.

###### **Fi** **g ure 24: Heatin** **g function**

*[Figurtekst: º C A Refrigeration · t · B Neutral zone · C Heat · A r01 · B r62 · C r01]*

### **Digital inputs**

There are two digital inputs, DI1 and DI2, with dry contact function. They can be used for the following functions:

**Table 5: Function table and DI settin** **g s**

||**Input / Set**|**tings menu**||
|---|---|---|---|
|**Function**|**DI1**|**DI2**|**Setting**|
||**o02**|**o37**||
|None|+|+|0|
|DI Status|+|+|1|
|Door function|+|+|2|
|Door alarm|+|+|3|
|Defrost start|+|+|4|
|Main switch|+|+|5|
|Night setback|+|+|6|
|Thermostat band|+|+|7|
|Alarm at closed|+|+|8|
|Alarm at open|+|+|9|
|Case cleaning|+|+|10|
|Forced cooling|+|+|11|
|Open blinds|+|+|12|
|Coordinated defrost||+|13|
|Forced closing|+|+|14|
|Shutdown|+|+|15|
|Light control|+|+|16|
|Leak detection|+|+|20|
|Adaptive liquid control|+|+|21|
|Door fan stop|+|+|29|

Example: If DI1 is to be used to start a defrost, o02 must be set to 4.

### **Forced closing**

The AKV valves can be closed with an external signal ("Forced closing").

The function must be used in connection with the compressor’s safety circuit, so that there will be no injection of liquid into the evaporator when the compressor is stopped by the safety controls and cannot start again (however not at low pressure – LP).

Via a setting (see o90 Fan at forced closing) it is possible to define whether the fan should be ON or OFF during forced closing and whether an ongoing defrost is suppressed (i.e. put in standby position for a period of upto 10 minutes before it is cancelled) - this feature can be used in CO2 systems to eliminate excessive heating while compressors cannot run.

The signal can be received from the DI-input or via the data communication.

### **Door contact**

The door contact function can via the digital inputs be defined for two different applications:

##### **Alarm monitoring:**

The controller monitors the door contact and delivers an alarm message if the door has been opened for a longer period than the set alarm delay.

##### **Alarm monitoring and stop of refrigeration:**

When the door is opened, the refrigeration is stopped, i.e. the injection, the compressor and the fan are stopped and light switches on. If the door remains open for a longer time than the set restart time, refrigeration will be resumed. This will ensure that refrigeration is maintained even if the door is left open or if the door contact should be defective. If the door remains open for a longer period than the set alarm delay, an alarm will also be triggered.

##### **Alarm monitoring and stop of fans:**

When the door is opened, only the fans are stopped. If the door remains open for a longer time than the set alarm delay, an alarm is triggered and the fans will start running again.

### **Display**

The controller has one plug for an external display. One of the following display types can be connected:

- AK-UI55 Info (temperature display).

- AK-UI55 Set (temperature display and operation).

- AK-UI55 Bluetooth (temperature display and app interface).

The connection between the display and the controller must be made using an AK-UI55 cable.

The distance between the controller and the display must not exceed 100 m.

###### **Fi** **g ure 25: Controller with one dis** **p la** **y**

### **Override**

The controller contains a number of override functions which can be used together with Master Control functions in the Danfoss gateway/system manager:

**Table 6: Override functionalit** **y**

|**Master control function**|**Description**|
|---|---|
|MC Ther. toggle|Master control signal used for switching case load ON/OFF depending on the load condition|
|MC Load request|Master control signal used to control the load balance between multiple case controllers on the same suction line|
|MC Max. Te offset|Requested offset to actual evaporating temperature in order to keep the air temperature at the actual setpoint|
|MC Liquid control|Master control signal allowing switch to adaptive liquid control|

|**Master control function**|**Description**|
|---|---|
|MC Night setback|Master control signal for changing between day and night time operation|
|MC Case shutdown|Master control signal used to shut down a case for a time period. During shutdown there will be no alarm monitoring|
|MC Forced closing|Master control signal that will close the injection valve|
|MC Forced cooling|Master control signal that will provide forced cooling|
|MC Defrost start|Master control signal for starting a defrost. At adaptive defrost the defrost might be skipped if the defrost is not needed|
|MC Defrost state|Read out the actual state of the defrost|
|MC Hold after defrost|Master control signal used for co-ordinated defrost control to hold cabinets from returning to normal refrigeration after a defrost<br>until all cabinets have terminated defrost|
|MC Stop defrost|Master control signal used to prevent a defrost start in a controller.|
|MC Light signal|Master control signal for control of light via a data communication signal from the system manager|
|MC Actual dewpoint|Master control signal sending the actual measured dewpoint from the system manager to the controller over the network.|
|MC Po load factor|Calculated load factor for the refrigerated appliance. Used for suction pressure optimization.|
|MC Key/Bluetooth lock|Master control signal that will lock down all Bluetooth data communication|
|MC Min. delta T|Required minimum delta temperature across evaporator (S3 - Te) in order to keep the air temperature at the actual setpoint|

### **Applications**

The chapter outlines application examples:

- Standard display case

- Cold rooms

An application setting will configure inputs and outputs so that the controller’s operation interface is reflecting the selected application.

In application 4 and 9, users can custom define the functions of relay 2, 3 and 4, e.g.:

- Controlling two compressors

- Controlling the night blind

- Controlling the heat function

- ECO operations of fans

**Fi** **g ure 26: Standard dis** **p la** **y case, u** **p ri** **g ht or normal, with one evaporator**

*[Figurtekst: S₄ · S₃ S₄ · S₅ · S₂ · S₅ · S₃]*

**Fi** **g ure 27: Cold room confi** **g uration with door, li** **g ht and heat control function**

### **AK -** **CC55 Compact connections and application options**

**Fi** **g ure 28: Electrical connections AK-CC55 Com** **p act**

*[Figurtekst: 40 41 42 43 44 4 5 4 6 47 4 8 4 9 50 60 61 70 71 83 84 85 · 5V s AI2 AI3 AI4 AI5 DI2 AO1 B A · A1 DI1 PWM MODBUS · 115 - 230V AC DO1 DO2 DO3 DO4 · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17]*

- Max. 0.5 A - No overload protection!

AK-CC55 Compact is optimised for control of one evaporator plus different combinations of light, rail heat and alarm relays.

It has 4 Digital Outputs (DO), known as DO1 – DO4, one Analogue Output (AO), known as AO1, 4 Analogue Inputs (AI), known as AI1 – AI4, an input that can be used as either an AI5 or as a DI (Digital Input) DI1, and one Digital Input (DI2).

It has 9 different application options (Application 1 – Application 9) to control the functions of the input and output relays.

**Table 7: A** **pp lication with di** **g ital and analo** **g ue in/out** **p ut s** **p ecification**

|**No. **|**Application description**|**DO1**|**DO2**|**DO3**|**DO4**|**AO1**|**AI1**|**AI2**|**AI3**|**AI4**|**AI5/ DI1**|**DI2**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|TXV appl.|||||||S3|S4|S5|||
|2|TXV appl.|||||||S3|S4|S5|||
|3|TXV appl.|||||||S3|S4|S5|||
|4|TXV appl./ User def. config.||User def.|User def.|User def.|||S3|S4|S5|||
|5|EEV appl.||||||Pe|S2|S3|S4|S5||
|6|EEV appl.||||||Pe|S2|S3|S4|S5||
|7|EEV appl.||||||Pe|S2|S3|S4|S5||
|8|EEV appl.||||||Pe|S2|S3|S4|S5||
|9|EEV appl./ User def. config.||User def.|User def.|User def.||Pe|S2|S3|S4|S5||

= Optional use

**Table 8: Sensor descri** **p tion**

|Pe|Evaporating pressure|
|---|---|
|S2|Gas outlet of evaporator|
|S3|Return air temperature|
|S4|Discharge air temperature|
|S5|Evaporator temperature|

### **Application set -** **ups and IO connections**

AK-CC55 Compact is designed for control of one evaporator + different combinations of light, rail heat and alarm relays.

The most important variations are:

##### **Applications 1-4: TEV applications**

Control of compressor or solenoid valve, alarm relay, lights, rail heat Application 4: Configurable outputs, e.g.: Dual compressor operation, heat function, night blind, ECO fan

##### **Applications 5-9: EEV applications**

Control of AKV valve, compressor, alarm relay, light, rail heat. 9: Configurable outputs, e.g.: Dual compressor operation, heat function, night blind, ECO fan

###### **Fi** **g ure 29: Connections for a** **pp lication 1**

*[Figurtekst: 1 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · AI5 DI2 AO1 B - A + · S3 S4 S5 DI1 MODBUS · 115 – 230 V AC Comp. Alarm Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Fi g ure 30: Connections for a pp lication 2 · 2 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · AI5 DI2 AO1 B - A + · S3 S4 S5 DI1 MODBUS · 115 – 230 V AC Comp. Light Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Fi g ure 31: Connections for a pp lication 3 · 3 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · AI5 DI2 AO1 B - A + · S3 S4 S5 DI1 MODBUS · 115 – 230 V AC Comp. Railheat Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · 0 – 10 V/ PWM · 0 – 10 V/ PWM · 0 – 10 V/ PWM]*

###### **Fi** **g ure 32: Connections for a** **pp lication 4**

*[Figurtekst: 4 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · AI5 DI2 AO1 B - A + · S3 S4 S5 DI1 MODBUS · 115 – 230 V AC Comp. DO2 DO3 DO4 · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Custom set-up · Fi g ure 33: Connections for a pp lication 5 · P · 1 3 2 · 5 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · 5V s AI5 DI2 AO1 B - A + · Pe S2 S3 S4 S5 MODBUS · 115 – 230 V AC AKV Comp. Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Fi g ure 34: Connections for a pp lication 6 · P · 1 3 2 · 6 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · 5V s AI5 DI2 AO1 B - A + · Pe S2 S3 S4 S5 MODBUS · 115 – 230 V AC AKV Alarm Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · 0 – 10 V/ PWM · 0 – 10 V/ PWM · 0 – 10 V/ PWM]*

###### **Fi** **g ure 35: Connections for a** **pp lication 7**

*[Figurtekst: P · 1 3 2 · 7 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · 5V s AI5 DI2 AO1 B - A + · Pe S2 S3 S4 S5 MODBUS · 115 – 230 V AC AKV Light Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Fi g ure 36: Connections for a pp lication 8 · P · 1 3 2 · 8 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · 5V s AI5 DI2 AO1 B - A + · Pe S2 S3 S4 S5 MODBUS · 115 – 230 V AC AKV Railheat Fan Defrost · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Fi g ure 37: Connections for a pp lication 9 · P · 1 3 2 · 9 · 40 41 42 43 44 45 46 47 48 49 50 60 61 70 71 83 84 85 · 5V s AI5 DI2 AO1 B - A + · Pe S2 S3 S4 S5 MODBUS · 115 – 230 V AC AKV DO2 DO3 DO4 · L N · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 · Custom set-up · 0 – 10 V/ PWM · 0 – 10 V/ PWM · 0 – 10 V/ PWM]*

### **Product identif i** **cation**

The controller is provided with labels from the factory, indicating a generic application. When selecting the required application, specific labels are provided so that you can mount the relevant one.

The application number is indicated on the left-hand side of the labels. Use the label fitting the selected application.

Some of the labels are applicable to multiple application options.

###### **Fi** **g ure 38: Labels used to indicate application number**

### **AK -** **CC55 Compact connections**

Data communication

###### **Fi** **g ure 39: Data communication**

 **IMPORTANT:**

It is important that the installation of the data communication cable is performed correctly with sufficient distance to high voltage cables.

### AKV info

**Fi** **g ure 40: AKV info**

*[Figurtekst: 230 V AC (115 AC)]*

230 V or 115 V AC coil Max. 0.5 A

Not overload protected

External solid state relay for rail heat

**Fi** **g ure 41: External solid state rela** **y for rail heat**

*[Figurtekst: SSR · 60 61 70 71 · AO1/ · PWM]*

0 / 10 V Pulse Width Modulated (PWM) Max. 15 mA.

AKS 32R info

###### **Fi** **g ure 42: AKS 32R info**

*[Figurtekst: AKS 32R A Black · out · B Brown · C Blue · A B C]*

 **NOTE:**

A ratiometric pressure transmitter with a 5 V, 10 – 90% voltage output signal must be used.

The signal from one pressure transmitter can be received by up to 10 controllers. There must not be a significant pressure drop from the pressure transmitter's position in the suction line to the individual evaporators.

Coordinated defrost via cable connections

**Fi** **g ure 43: Coordinated defrost via cable connections**

Max. 10

The following controllers can be connected in this way: EKC 204A, AK-CC 210, AK-CC 250, AK-CC 450, AK-CC 550 and AK-CC55.

Refrigeration is resumed at the same time when all controllers have terminated defrost.

External display AK-UI55

**Fi** **g ure 44: External dis** **p la** **y AK-UI55**

(Total length: max. 100 m)

### Connections

**Table 9: Connection details**

|**AI1**|**Pressure transmitter**<br>AKS 32R<br>Connect to terminal 40, 41 and 42.<br>(Use cable 060G1034: Black=40, Brown=41, Blue=42)|
|---|---|
||The signal from one pressure transmitter can be received by up to 10 controllers. But only if there are no significant pressure drops be-<br>tween the evaporators to be controlled. SeeFigure 42: AKS 32R info.|
|**AI2 - AI5**|**Primarily for temperature inputs**<br>• S2<br>Pt 1000 ohm sensor AKS11, placed at the evaporator outlet<br>• S3, S4, S5<br>Pt 1000 AKS11, PTC 1000 EKS111, NTC5K EKS211 or NTC10K EKS221 sensor or a user-defined sensor type. All have to be of the same<br>type.<br>• S3, air sensor, placed in the warm air before the evaporator<br>• S4, discharge air sensor, placed in the cold air after the evaporator<br>(the need for either S3 or S4 can be selected in the configuration)<br>• S5, defrost sensor, placed in the evaporator|
||(If the DI1 input is used for a temperature measurement, it will appear as AI5.))|
|**DI1**|**Digital input signal**<br>The defined function is active when the input is short-circuited or opened, depending on the function defined in o02.|
|**DI2**|**Digital input signal**<br>The defined function is active when the input is short-circuited or opened, depending on the function defined in o37.|
|**AO1**|**Analogue output signal**<br>• Analogue 0 – 10 V (currently not used)<br>• Pulse width modulated signal<br>Can be used for fast pulse control of rail heat via an external power solid state relay.|
|**MODBUS**|For data communication:<br>• Terminal 83 = B-<br>• Terminal 84 = A+<br>• Terminal 85 = screen|
|**Supply voltage**|230 V AC or 115 V AC|
|**DO1**|• AKV valve:<br>Connection of expansion valve type AKV, AKVA, AKVH or AKVP.<br>The coil must be a**230 V**or**115 V AC coil**<br>• Compressor:<br>Connection of a relay. The coil must be a**230 V**or**115 V AC coil. Max. 0.5 A.**<br>• Solenoid valve:<br>The coil must be a**230 V**or**115 V AC coil. Max. 0.5 A.**|
|**DO2**|• Alarm:<br>There is a connection between terminal 10 and 12 in alarm situations and when the controller is without power.<br>DO2 has reinforced insulation that can be used with 24 V.<br>• Light, Rail heat, Compressor/Liquid line valve:<br>There is connection between terminal 10 and 11 (10 and 12 at light) when the function is ON.|
|**DO3**|• Fan:<br>There is connection between terminal 13 and 14 when the fan is ON.|
|**DO4**|• Defrost:<br>There is connection between terminal 15 and 16 when defrosting takes place.|
|**DO2-DO4 + AO1 and**<br>**Application 4 / 9**|Here, the different outputs can be custom defined in q02-q09|

##### **Display (RJ12 plug)**

If readings/operation of the controller is required, an external display can be connected. The max. cable length is 100 m.

##### **Electric noise**

Cables for sensors, low voltage DI inputs and data communication **must** be kept separate from other electric cables:

- Use separate cable trays

- Keep a distance between cables of at least 10 cm

- Long cables at the low voltage DI input should be avoided

##### **Installation considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown.

Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss will not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer's responsibility to check the installation thoroughly, and to fit the necessary safety devices.

Special reference is made to the necessity of signals to the controller when the compressor is stopped and to the need of liquid receivers before the compressors.

Your local Danfoss agent will be pleased to assist with further advice, etc.

### **Operation**

The controller can be operated in different ways depending on the user interface.

The following options are available:

- Via data commmunication

- Via AK-UI55 Setting display

- Via AK-UI55 Bluetooth display

### **Operation via data communication**

##### **Via system manager's display**

All AK-CC55 controllers can be operated from a central location, e.g. AK-SM 800. Data communication is to take place via MODBUS.

##### **Via system manager and service tool**

Operation can also be performed from a central location with PC software "Service Tool" connected to a system manager AK-SM 720 via MODBUS.

##### **Programming via KoolProg**

Programming by use of PC software type KoolProg® via interface MMIMYK connected to RJ12 display connector.

### **Direct operation**

Operation via AK-UI55 setting display

The display can be located at a distance of up to 100 meters from the controller.

##### **Smart phone and app via AK-UI55 Bluetooth display**

The "AK-CC55 connect" app is used for smart phone operation. **AK-CC55 connect** can be downloaded freely to a compatible iOS/Android smartphone device. Menu operation is established by activating Bluetooth communication to the app.

### **Operation via AK -** **UI55 Set**

##### **Display AK-UI55 Set**

The values will be shown with three digits, and with a setting you can determine whether the temperature is to be shown in °C or in °F.

To prevent any passing-by user from making unauthorized changes, the access to the display menu is restricted by access codes.

Besides this, the parameter P89 provides the following options for handling of the display keyboard:

- 0 The display keys are always operative

- 1 The display keys will be locked automatically when not used for some time and the keyboard must be unlocked by pressing the arrow-up and arrow-down keys at the same time.

- 2 The display keys will be locked and unlocked by means of a master control signal from the System Manager.

###### **Fi** **g ure 45: O** **p eratin** **g via AK-UI55 Set**

*[Figurtekst: B C · D · A · E · Danfoss 84B8325 F]*

- A Lights up in event of: Energy optimization, Cooling, Defrosting, Fan operation

- B Lights in event of alarm

- C Long press (3 seconds) on alarm button alarm — relay is reset — alarm code displayed — e.g. “A1”

- D Long press (3 seconds) gives access to the information menu “InF” Up arrow / Down arrow / Arrow to left: Navigation in the menu and setting of values.

- E Long press (3 seconds) will start a defrost, “-d-” is shown in the display. Ongoing defrosting can be stopped by a long press.

- F SET: Long press (3 seconds) gives access to the “SEt” menu. If the operation is locked with a password, “PS” is shown. Enter the code. Shows the setting for a chosen parameter / saves a changed setting. Short press gives access to entering of the thermostat’s cut-out limit.

**Table 10: Messa** **g es** **p rovided b** **y the dis** **p la** **y**

|**Display readout**|**Denomination**|
|---|---|
|-d-|Defrost is in progress|
|Err|The temperature cannot be displayed due to a sensor error|
|Er1|The display cannot load data from the controller. Disconnect and then reconnect the display|
|Er2|Lost display communication|
|ALA|The alarm button is activated. The first alarm code is then shown|
|- - -|At top position of the menu or when max. value has been reached, the three dashes are shown in the top of the display|
|- - -|At bottom position of menu or when min. value has been reached, the three dashes are shown in the bottom of the display|
|Loc|The menu operation is locked. Unlock by pressing (for 3 seconds) on the ‘up arrow’ and ‘down arrow’ simultaneously|
|UnL|The menu operation is unlocked|
|- - -|The parameter has reached min. or max. limit|
|PS|A password is required for access to the menu|
|Fan|Appliance cleaning has been initiated. The fans are running|
|OFF|Appliance cleaning is activated and the appliance can now be cleaned|
|OFF|The main switch is set to Off|
|SEr|The main switch is set to service / manual operation|
|CO2|Flashes: Will display in event of a refrigerant leakage alarm, but only if the refrigerant is set up for CO2|

##### **Factory setting**

If you need to return to the factory-set values, do the following:

- Cut off the supply voltage to the controller

- Keep up "∧" and down "∨" arrow buttons depressed at the same time as you reconnect the supply voltage

- When FAc is shown in the display, select "yes"

######  **NOTE:**

The OEM factory setting will either be the Danfoss factory settings or a user defined factory setting if one has been made.

The user can save his setting as OEM factory setting via parameter o67.

### Parameter groups when operating via display

###### **Fi** **g ure 46: SET button** **p arameter list**

*[Figurtekst: SET SET button, · 3 s: Configuration settings · Set · PS: Password (if any) · (PS) · cFg SET r12 Main switch · o61 Application · r-- o03 MODBUS address · A-- r89 Food type · c-- r00 Cut-out temperature · d-- r15 Ther. sensor S4 % · n-- r61 Ther. sensor S4% night · F-- A36 Alarm sensor S4% · t-- o17 Display air S4% · h-- o30 Refrigerant type · o-- o20 Min. transmitter range · p-- o21 Max. transmitter range · q-- d01 Defrost method · u-- d03 Defrost interval · < d10 Defrost sensor · (Return) d04 Max. defrost time · d02 Defrost stop temperature · < · (Return) · Fi g ure 47: Info button  p arameter list · Info button, · 3 s: Information for service use · Inf · StA SET See control state message · App SET See selected application · in SET AI1 (PE) · out SET do1 * AI2 ** · buS SET MODBUS quality do2 AI3 ** · SoF SET See SW version do3 AI4 ** · < do4 AI5 ** · (Return) Ao1 ** di1 ** · < di2 ** · (Return) < · Output status · When you want info on a relay (Return) · output, the dot will show whether · the relay is activated (energized) · for e.g.: · do4 = not activated · do.4 = activated · < · < · Menu groups · See also the following pages. · < · * · * · * · Read output status Read input status]*

The output's function (determined at configuration). DOs and AOs can also be forced controlled from this menu, when r12 Main switch has been set to position "service". Forced control of a function can also be performed in codes q11 to q27.

- ** The input's function (determined at configuration)

StA See control state message in Table 43

### Get a good start

With the following procedure you can start regulation very quickly:

1. Open parameter r12 and stop the regulation (in a new and not previously set unit, r12 will already be set to 0 which means stopped regulation.)

2. Select application based on the wiring diagrams (see Application set-ups and IO connections)

3. Open parameter o61 and set the application number

4. For network. Set the address in o03

5. Then select a set of presets from the "Food type" help table

6. Open parameter r89 and set the number for the array of presettings. The few selected settings will now be transferred to the menu

7. Set the desired cut-out temperature r00 8. Set the weighted thermostat air temperature between S4 and S3 sensor r15

9. Set the weighted thermostat air temperature between S4 and S3 during night operation r61 10. Set the weighted alarm air temperature between S4 and S3 A36

11. Set the weighted display readout between S4 and S3 o17 12. Select refrigerant via parameter o30 (only application 5-9) 13. Set the pressure transmitter min. and max. range via parameter o20 and o21 (only application 5-9) 14. Set the desired defrost method in d01 15. Set the interval time between defrost starts in d03 16. Set the desired defrost sensor in d10 17. Set the maximum defrost time in d04 18. Set the defrost stop temperature in d02 19. Open parameter r12 and start the regulation 20. Go through the parameter list and change the factory values where needed 21. Get the controller up and running on network:

- MODBUS: Activate scan function in system unit

**Table 11: Food t** **yp e settin** **g s**

|**Setting of presettings (r89).**<br>**After setting 1-5, setting is returned to 0.**|**1**|**2**|**3**|**4**|**5**|
|---|---|---|---|---|---|
|**Food type**|**Vegetables**|**Milk**|**Meat/fish**|**Frozen food**|**Ice cream**|
|Temperature (r00)|8 °C|0 °C|-2 °C|-20 °C|-24 °C|
|Max. temp. setting (r02)|10 °C|4 °C|2 °C|-16 °C|-20 °C|
|Min. temp. setting (r03)|4 °C|-4 °C|-6 °C|-24 °C|-28 °C|
|Upper alarm limit (A13)|14 °C|8 °C|8 °C|-15 °C|-15 °C|
|Lower alarm limit (A14)|0 °C|-5 °C|-5 °C|-30 °C|-30 °C|
|Upper alarm limit for S6 (A22)|14 °C|8 °C|8 °C|-15 °C|-15 °C|
|Lower alarm limit for S6 (A23)|0 °C|-5 °C|-5 °C|-30 °C|-30 °C|

### **AK-UI55 display menu (SW ver. 2.1x)**

- R-W If the operation is protected by one or more passwords, reading and setting the parameter will be limited to: R or W

- R This setting can be seen with password no. _ or higher (3 is the highest level).

- W This setting can be performed with password no. _ or higher (3 is the highest level).

- The asterisk indicates in which application from 1-9 the parameter is applicable

### **Thermostat**

**Table 12: Thermostat**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min. value **|**Max. value **|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Cutout 1||0-0|r00|*|*|*|*|*|*|*|*|*|r03|r02|2.0 °C|
|Differential||1-2|r01|*|*|*|*|*|*|*|*|*|0.1 °C|20.0 °C|2.0 °C|
|Max cutout limit||0-2|r02|*|*|*|*|*|*|*|*|*|r03|50.0 °C|50.0 °C|
|Min cutout limit||0-2|r03|*|*|*|*|*|*|*|*|*|-60.0 °C|r02|-60.0 °C|
|Temperature unit|0=Celsius, 1=Fahrenheit|1-2|r05|*|*|*|*|*|*|*|*|*|0|1|0|
|S4 Air OFF evap. A - Ad-<br>justment||1-2|r09|*|*|*|*|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|S3 Air ON evap. A - Adjust-<br>ment||1-2|r10|*|*|*|*|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|S5 Evaporator A - Adjust-<br>ment||1-2|r11|*|*|*|*|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|Main switch|-1=Manual, 0=Stop,<br>1=Start|0-2|r12|*|*|*|*|*|*|*|*|*|-1|1|0|
|Night offset||1-2|r13|*|*|*|*|*|*|*|*|*|-50.0 °C|50.0 °C|0.0 °C|
|Thermostat mode|2=Modulating, 1=ON/OFF|1-2|r14|*|*|*|*|*|*|*|*|*|1|2|1|
|Thermostat sensor S4 %||1-2|r15|*|*|*|*|*|*|*|*|*|0 %|100 %|100%|
|Melt interval||1-2|r16|*|*|*|*|*|*|*|*|*|0 h|10 h|1 h|
|Melt period||1-2|r17|*|*|*|*|*|*|*|*|*|0 min|30 min|5 min|
|S2 Gas outlet A - Adjust-<br>ment||1-2|r19|*|*|*|*|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|Cutout 2||0-2|r21|*|*|*|*|*|*|*|*|*|-60.0 °C|50.0 °C|2.0 °C|
|Thermostat sensor S4 %<br>night||1-2|r61|*|*|*|*|*|*|*|*|*|0 %|100 %|100%|
|Air heater neutral zone||1-2|r62||||*|||||*|0.0 °C|50.0 °C|5.0 °C|
|Air heater start delay||1-2|r63||||*|||||*|0 min|240 min|240 min|
||0=None, 1=Vegetables,|||||||||||||||
|Food type|2=Dairy, 3=Meat and fish,<br>4=Frozen food, 5=Ice<br>cream|1-2<sup>**(1)**</sup>|r89|*|*|*|*|*|*|*|*|*|0|5|0|
|Differential 2||1-2|r93|*|*|*|*|*|*|*|*|*|0.1 °C|20.0 °C|2.0 °C|
|S4 frost protection||1-2|r98|*|*|*|*|*|*|*|*|*|-60.0 °C|50.0 °C|-60.0 °C|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Alarm settings**

**Table 13: Alarm settin** **g s**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**<br>**4**|**5**|**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Alarm delay A||1-2|A03|*<br>*|*<br>*|*|*|*|*|*|0 min|240 min|30 min|
|Door open alarm delay||1-2|A04|*<br>*|*<br>*|*|*|*|*|*|0 min|240 min|60 min|
|Alarm delay pulldown A||1-2|A12|*<br>*|*<br>*|*|*|*|*|*|0 min|240 min|90 min|
|High alarm limit 1||1-2|A13|*<br>*|*<br>*|*|*|*|*|*|-60.0 °C|50.0 °C|8.0 °C|
|Low alarm limit 1||1-2|A14|*<br>*|*<br>*|*|*|*|*|*|-60.0 °C|50.0 °C|-30.0 °C|
|High alarm limit 2||1-2|A20|*<br>*|*<br>*|*|*|*|*|*|-60.0 °C|50.0 °C|8.0 °C|
|Low alarm limit 2||1-2|A21|*<br>*|*<br>*|*|*|*|*|*|-60.0 °C|50.0 °C|-30.0 °C|

|**Function**<br>**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Alarm delay DI 1|1-2|A27|*|*|*|*||||||0 min|240 min|30 min|
|Alarm delay DI 2|1-2|A28|*|*|*|*|*|*|*|*|*|0 min|240 min|30 min|
|Alarm sensor S4% A|1-2|A36|*|*|*|*|*|*|*|*|*|0 %|100 %|100%|

### **Compressor**

**Table 14: Com** **p ressor**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**<br>**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Min ON time||1-2|c01|*<br>*|*|*|*|||*|0 min|30 min|0 min|
|Min OFF time||1-2|c02|*<br>*|*|*|*|||*|0 min|30 min|0 min|
|Delay between comp.||1-2|c05|||*||||*|0 s|999 s|5s|
|Step control mode|1=Sequential, 2=Cyclic|1-2|c08|||*||||*|1|2|2|
|Comp. 2 ctrl. Th. band 2|0=OFF, 1=ON|1-2|c85|||*||||*|0|1|1|

### **Defrost**

**Table 15: Defrost**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
||0=None, 1=Electrical,|||||||||||||||
|Defrost method|2=Hot gas, 3=Brine, 4=Air/<br>Offcycle|1-3|d01|*|*|*|*|*|*|*|*|*|0|4|1|
|Defrost stop limit A||1-2|d02|*|*|*|*|*|*|*|*|*|0.0 °C|50.0 °C|6.0 °C|
|Defrost start interval||1-2|d03|*|*|*|*|*|*|*|*|*|0 h|240 h|8h|
|Max defrost time||1-2|d04|*|*|*|*|*|*|*|*|*|0 min|360 min|45 min|
|Time staggering power up||1-2|d05|*|*|*|*|*|*|*|*|*|0 min|240 min|0 min|
|Drip off time||1-2|d06|*|*|*|*|*|*|*|*|*|0 min|60 min|0 min|
|Fan start delay||1-2|d07|*|*|*|*|*|*|*|*|*|0 min|60 min|0 min|
|Fan start temperature||1-2|d08|*|*|*|*|*|*|*|*|*|-60.0 °C|10.0 °C|-5.0 °C|
|Fan control during defrost|<sup>0=OFF, 1=ON, 2=OFF at</sup><br>drip, 3=OFF at high temp|1-2|d09|*|*|*|*|*|*|*|*|*|0|3|1|
|Defrost stop method|0=Time, 1=S5 sensor,<br>2=S4 sensor|1-2|d10|*|*|*|*|*|*|*|*|*|0|2|0|
|Pump down delay||1-2|d16|*|*|*|*|*|*|*|*|*|0 min|60 min|0 min|
|Max thermostat runtime||1-2|d18|*|*|*|*|*|*|*|*|*|0 h|240 h|0h|
|Min. defrost time||1-2|d24|*|*|*|*|*|*|*|*|*|0 min|d04|0 min|
|Rail heat during defrost|0=OFF, 1=ON, 2=Normal<br>control|1-2|d27|*|*|*|*|*|*|*|*|*|0|2|1|
|Defrost stop limit 2||1-2|d28|*|*|*|*|*|*|*|*|*|0.0 °C|50.0 °C|6.0 °C|
|Max. defrost time 2||1-2|d29|*|*|*|*|*|*|*|*|*|0 min|360 min|45 min|
|Display delay after defrost||1-2|d40|*|*|*|*|*|*|*|*|*|5 min|240 min|30 min|
|Fan stop temperature||1-2|d41|*|*|*|*|*|*|*|*|*|-20.0 °C|20.0 °C|0.0 °C|

### **Injection control**

**Table 16: In** **j ection control**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Max superheat limit||1-2|n09||||*|*|*|*|*|n10|20.0 °C|12.0 °C|
|Min superheat limit||1-2|n10||||*|*|*|*|*|2.0 °C|n09|3.0 °C|
|MOP temperature||1-2|n11||||*|*|*|*|*|-60.0 °C|15.0 °C|15.0 °C|
|AKV Period time||1-2<sup>**(1)**</sup>|n13||||*|*|*|*|*|3 s|6 s|6 s|
|Brine valve - Period time||1-2|n63|*<br>*|*|*||||||30 s|900 s|300 s|
|Brine valve max OD||1-2|n64|*<br>*|*|*||||||n65|100 %|100%|
|Brine valve min OD||1-2|n65|*<br>*|*|*||||||0 %|n64|0%|
|Brine valve windup||1-2|n66|*<br>*|*|*||||||0.2|1.0|1.0|
|Brine valve Kp||1-2|n67|*<br>*|*|*||||||0.5|10.0|4.0|
|Brine valve Tn||1-2|n68|*<br>*|*|*||||||60 s|1800 s|300 s|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Fan control**

**Table 17: Fan control**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Fan stop high S5 temp.||1-2|F04|*<br>*|*|*|*|*|*|*|*|-60.0 °C|50.0 °C|50.0 °C|
|Fan pulsing mode|0=No pulsing, 1=Pulsing<br>cutout, 2=Pulsing cutout<br>night|1-2|F05|*<br>*|*|*|*|*|*|*|*|0|2|0|
|Fan period time||1-2|F06|*<br>*|*|*|*|*|*|*|*|1 min|30 min|5 min|
|Fan ON cycle||1-2|F07|*<br>*|*|*|*|*|*|*|*|0 %|100 %|100%|

### **Defrost schedule**

**Table 18: Defrost schedule**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Defrost schedule|0=No, 1=Yes|1-2|t00|*|*|*|*|*|*|*|*|*|0|1|0|
|Def. start 1 - Hours||1-2|t01|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Def. start 1 - Minutes||1-2|t11|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 2 - Hours||1-2|t02|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Def. start 2 - Minutes||1-2|t12|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 3 - Hours||1-2|t03|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Def. start 3 - Minutes||1-2|t13|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 4 - Hours||1-2|t04|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Def. start 4 - Minutes||1-2|t14|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 5 - Hours||1-2|t05|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Def. start 5 - Minutes||1-2|t15|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 6 - Hours||1-2|t06|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Def. start 6 - Minutes||1-2|t16|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Time hours||0-1|t07|*|*|*|*|*|*|*|*|*|0 h|23 h|0 h|
|Time minutes||0-1|t08|*|*|*|*|*|*|*|*|*|0 min|59 min|0 min|
|Time date||0-1|t45|*|*|*|*|*|*|*|*|*|1|31|1|
|Time month||0-1|t46|*|*|*|*|*|*|*|*|*|1|12|1|
|Time year||0-1|t47|*|*|*|*|*|*|*|*|*|0|100|0|
|Monday - Follow schedule|0=No, 1=Yes|1-2|t51|*|*|*|*|*|*|*|*|*|0|1|1|
|Tuesday - Follow schedule|0=No, 1=Yes|1-2|t52|*|*|*|*|*|*|*|*|*|0|1|1|
|Wednesday - Follow<br>schedule|0=No, 1=Yes|1-2|t53|*|*|*|*|*|*|*|*|*|0|1|1|
|Thursday - Follow sched-<br>ule|0=No, 1=Yes|1-2|t54|*|*|*|*|*|*|*|*|*|0|1|1|
|Friday - Follow schedule|0=No, 1=Yes|1-2|t55|*|*|*|*|*|*|*|*|*|0|1|1|
|Saturday - Follow sched-<br>ule|0=No, 1=Yes|1-2|t56|*|*|*|*|*|*|*|*|*|0|1|1|
|Sunday - Follow schedule|0=No, 1=Yes|1-2|t57|*|*|*|*|*|*|*|*|*|0|1|1|

### **Miscellaneous**

**Table 19: Miscellaneous**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min. value **|**Max. value **|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Delay of outputs at power<br>up||1-2|o01|*<br>*|*|*|*|*|*|*|*|0 s|600 s|5s|
|DI1 Configuration|0=None, 1=DI status,<br>2=Door function, 3=Door<br>alarm, 4=Defrost start,<br>5=Main switch, 6=Night<br>setback, 7=Thermostat<br>band, 8=Alarm at closed,<br>9=Alarm at open, 10=Case<br>cleaning, 11=Forced cool-<br>ing, 12=Open blinds,<br>14=Forced closing,<br>15=Shutdown, 16=Light<br>control, 20=Leak detec-<br>tion, 21=Adaptive liquid<br>control, 29=Door fan stop|1-2<sup>**(1)**</sup>|o02|*<br>*|*|*||||||0|29|0|
|Network address||1-3<sup>**(1)**</sup>|o03|*<br>*|*|*|*|*|*|*|*|0|240|0|

|**Function**<br>Access code 3|**Values**|**R-W**<br>3-3|**Code**<br>o05|**1**<br>**2**<br>*<br>*|**3**<br>*|**4**<br>*|**5**<br>*|**6**<br>*|**7**<br>*|**8**<br>*|**9**<br>*|**Min. value **<br>0|**Max. value **<br>999|**Fact. value**<br>0|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|<br>Temperature sensor type|0=Pt 1000, 1=PTC 1000,<br>2=NTC 5k, 3=NTC 10k,<br>4=User-defined|1-3<sup>**(1)**</sup>|o06|*<br>*|*|*|*|*|*|*|*|0|4|0|
|Max hold time||1-2|o16|*<br>*|*|*|*|*|*|*|*|0 min|360 min|20 min|
|Display air S4%||1-2|o17|*<br>*|*|*|*|*|*|*|*|0 %|100 %|100%|
|Pe Min range||1-3<sup>**(1)**</sup>|o20||||*|*|*|*|*|-1.0 Bar|5.0 Bar|-1.0Bar|
|Pe Max range||1-3<sup>**(1)**</sup>|o21||||*|*|*|*|*|6.0 Bar|200.0 Bar|12.0Bar|
|Refrigerant|0=Not seleted, 6=R13,<br>7=R13b1, 2=R22, 8=R23,<br>14=R32, 11=R114,<br>3=R134a, 12=R142b,<br>24=R170, 15=R227,<br>25=R290, 16=R401A,<br>18=R402A, 19=R404A,<br>21=R407A, 22=R407B,<br>20=R407C, 37=R407F,<br>49=R407H, 23=R410A,<br>32=R413A, 30=R417A,<br>31=R422A, 33=R422D,<br>34=R427A, 35=R438A,<br>40=R448A, 41=R449A,<br>48=R449B, 43=R450A,<br>44=R452B, 45=R454B,<br>9=R500, 4=R502,<br>10=R503, 17=R507,<br>36=R513A, 26=R600,<br>27=R600a, 5=R717,<br>28=R744, 46=R1233zdE,<br>38=R1234ze, 39=R1234yf,<br>47=R1234zeZ, 29=R1270,<br>42=R452A, 1=User de-<br>fined display, 13=User de-<br>fined|1-3<sup>**(1)**</sup>|o30||||*|*|*|*|*|0|49|0|
|DI2 Configuration|0=None, 1=DI status,<br>2=Door function, 3=Door<br>alarm, 4=Defrost start,<br>5=Main switch, 6=Night<br>setback, 7=Thermostat<br>band, 8=Alarm at closed,<br>9=Alarm at open, 10=Case<br>cleaning, 11=Forced cool-<br>ing, 12=Open blinds,<br>13=Coordinated defrost,<br>14=Forced closing,<br>15=Shutdown, 16=Light<br>control, 20=Leak detec-<br>tion, 21=Adaptive liquid<br>control, 29=Door fan stop|1-2<sup>**(1)**</sup>|o37|*<br>*|*|*|*|*|*|*|*|0|29|0|
|Light control mode|1=Day and night, 2=Net-<br>work, 3=Door switch,<br>4=Network (Fallback),<br>5=Digital input|1-2|o38|*||*|||*||*|1|5|1|
|MC Light signal|<br>0=OFF, 1=ON|1-2|o39|*||*|||*||*|0|1|0|
|Rail heat ON cycle day||1-2|o41|*<br>*|*|*|*|*|*|*|*|0 %|100 %|100%|
|<br>Rail heat ON cycle night||1-2|o42|*<br>*|*|*|*|*|*|*|*|0 %|100 %|100%|
|Rail heat period time||1-2|o43||*|*||||*|*|6 min|60 min|6min|
|Case cleaning mode|0=OFF, 1=Fans run,<br>2=Cleaning|0-1|o46|*<br>*|*|*|*|*|*|*|*|0|2|0|
|Application mode|1=1. Comp/Alarm/Fan/<br>Defrost, 2=2. Comp/<br>Light/Fan/Defrost, 3=3.<br>Comp/Railheat/Fan/<br>Defrost, 4=4. Comp/<br>Custom, 5=5. EEV/<br>Comp/Fan/Defrost, 6=6.<br>EEV/Alarm/Fan/Defrost,<br>7=7. EEV/Light/Fan/<br>Defrost, 8=8. EEV/<br>Rail/Fan/Defrost, 9=9.<br>EEV/Custom|1-3<sup>**(1)**</sup>|o61|*<br>*|*|*|*|*|*|*|*|1|9|5|
|Access code 2||2-2|o64|*<br>*|*|*|*|*|*|*|*|0|999|0|
|Make new factory|0=OFF, 1=ON|3-3<sup>**(1)**</sup>|o67|*<br>*|*|*|*|*|*|*|*|0|1|0|
|Rail heat control mode|0=ON, 1=Day/Night timer,<br>2=Dew point ctrl.|1-2|o85|*<br>*|*|*|*|*|*|*|*|0|2|0|

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**<br>**4**|**5**|**6**|**7**|**8**|**9**|**Min. value **|**Max. value **|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Dewpoint min limit||1-2|o86|*<br>*|*<br>*|*|*|*|*|*|-10.0 °C|o87|8.0 °C|
|Dewpoint max limit||1-2|o87|*<br>*|*<br>*|*|*|*|*|*|o86|50.0 °C|17.0 °C|
|Rail heat min ON cycle||1-2|o88|*<br>*|*<br>*|*|*|*|*|*|0 %|100 %|30%|
|Door restart inj. delay||1-2|o89|*<br>*|*<br>*|*|*|*|*|*|0 min|240 min|30 min|
|Fan at forced closing|0=OFF, 1=ON, 2=OFF and<br>suppress defrost, 3=ON<br>and suppress defrost|1-2|o90|*<br>*|*<br>*|*|*|*|*|*|0|3|1|
|Light at Main switch OFF|0=OFF, 1=Normal ctrl.|1-2|o98|*|*|||*||*|0|1|0|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Control**

**Table 20: Control**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min. value **|**Max. value **|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Alarm relay priority|0=Not used, 1=High Prior-<br>ity, 2=Medium priority,<br>3=All|1-2|P41|*||*||*|||*|0|3|2|
|Blinds max open time||1-2|P60|||*|||||*|0 min|60 min|5 min|
|Fan stop at blinds closing||1-2|P65|*||*|||*||*|0 s|300 s|0 s|
|Rail heat PWM - Period<br>time||1-2|P82|*<br>*|*|*|*|*|*|*|*|4 s|60 s|10 s|
|Refrigerant factor K1||1-3<sup>**(1)**</sup>|P83||||*|*|*|*|*|-999|999|300|
|Refrigerant factor K2||1-3<sup>**(1)**</sup>|P84||||*|*|*|*|*|-999|999|300|
|Refrigerant factor K3||1-3<sup>**(1)**</sup>|P85||||*|*|*|*|*|-999|999|300|
|Max superheat liquid ctrl.||1-2|P86||||*|*|*|*|*|P87|20.0 °C|3.0 °C|
|Min superheat liquid ctrl||1-2|P87||||*|*|*|*|*|0.0 °C|P86|1.0 °C|
|Access code 1||1-1|P88|*<br>*|*|*|*|*|*|*|*|0|999|0|
|Display keyboard lock|0=None, 1=Local, 2=Net-<br>work|1-2|P89|*<br>*|*|*|*|*|*|*|*|0|2|0|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **DO conf i** **g and manual**

**Table 21: DO confi** **g and manual**

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min. value **|**Max. value **|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|DO2 Configuration|0=None, 1=Fans, 2=Fan<br>ECO, 3=Defrost, 4=Rail<br>heat, 5=Alarm, 6=Light,<br>7=Blinds, 8=Compressor/<br>LLSV, 9=Compressor 2,<br>10=Air heater|1-3<sup>**(1)**</sup>|q02|||*|||||*|0|10|6|
|DO3 Configuration|0=None, 1=Fans, 2=Fan<br>ECO, 3=Defrost, 4=Rail<br>heat, 5=Alarm, 6=Light,<br>7=Blinds, 8=Compressor/<br>LLSV, 9=Compressor 2,<br>10=Air heater|1-3<sup>**(1)**</sup>|q03|||*|||||*|0|10|8|
|DO4 Configuration|0=None, 1=Fans, 2=Fan<br>ECO, 3=Defrost, 4=Rail<br>heat, 5=Alarm, 6=Light,<br>7=Blinds, 8=Compressor/<br>LLSV, 9=Compressor 2,<br>10=Air heater|1-3<sup>**(1)**</sup>|q04|||*|||||*|0|10|9|
|AO1 Configuration|0=None, 1=Rail heat PWM|1-3<sup>**(1)**</sup>|q09|*<br>*|*|*|*|*|*|*|*|0|1|0|
|EEV override A||1-2<sup>**(2)**</sup>|q11||||*|*|*|*|*|0 %|100 %|0%|
|Compressor 1 - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q12|*<br>*|*|*|*||||*|0|1|0|
|Fan - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q13|*<br>*|*|*|*|*|*|*|*|0|1|0|
|Defrost A - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q14|*<br>*|*|*|*|*|*|*|*|0|1|0|
|Rail heat - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q15||*|*||||*|*|0|1|0|
|Alarm relay - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q16|*||*||*|||*|0|1|0|
|Light - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q17|*||*|||*||*|0|1|0|
|Compressor 2 - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q19|||*|||||*|0|1|0|

|**Function**|**Values**|**R-W**|**Code**|**1**<br>**2**|**3**|**4**|**5**|**6**|**7**|**8**|**9**|**Min. value **|**Max. value **|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Blinds - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q21|||*|||||*|0|1|0|
|Air heater - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q23|||*|||||*|0|1|0|
|Fan ECO - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q24|||*|||||*|0|1|0|
|Rail heat PWM - override||1-2<sup>**(2)**</sup>|q27|*<br>*|*|*|*|*|*|*|*|0 %|100 %|0%|
|High temperature - Priori-<br>ty|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q28|*<br>*|*|*|*|*|*|*|*|0|3|1|
|Low temperature - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q29|*<br>*|*|*|*|*|*|*|*|0|3|1|
|Sensor errors - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q30|*<br>*|*|*|*|*|*|*|*|0|3|1|
|DI alarms - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q31|*<br>*|*|*|*|*|*|*|*|0|3|2|
|Defrost - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q32|*<br>*|*|*|*|*|*|*|*|0|3|3|
|Miscellaneous - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q33|*<br>*|*|*|*|*|*|*|*|0|3|2|
|Injection - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q34|*<br>*|*|*|*|*|*|*|*|0|3|2|
|Control stopped - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q35|*<br>*|*|*|*|*|*|*|*|0|3|3|
|Leak detection - Priority|0=Disabled, 3=Low,<br>2=Medium, 1=High|1-2|q36|*<br>*|*|*|*|*|*|*|*|0|3|2|
|Food temp. sensor|1=Thermostat air,<br>2=Alarm air, 3=S3 Air ON<br>evap.|1-2<sup>**(1)**</sup>|q39|*<br>*|*|*|*|*|*|*|*|1|3|2|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

> **(2) In order to change this parameter the parameter r12 Main switch must be set in position "SEr" allowing manual control of outputs.**

### **Service**

**Table 22: Service**

|**Function**<br>Control state A|**Values**<br>0=Normal ctrl., 1=Hold af-<br>ter defrost, 2=Min ON tim-<br>er, 3=Min OFF timer,<br>4=Drip off, 10=Main<br>switch OFF, 11=Thermo-<br>stat cut-out, 12=Frost pro-<br>tection S4, 14=Defrost,<br>15=Fan delay, 16=Forced<br>closing, 17=Door open,<br>18=Melt period, 19=Mod-<br>ulating temp. control,<br>20=Emergency control,<br>23=Adaptive superheat<br>control, 24=Start injec-<br>tion, 25=Manual control,<br>26=No refrigerant selec-<br>ted, 29=Case cleaning,<br>30=Forced cooling,<br>31=Door open, 32=Pow-<br>er-up delay, 33=Air heat-<br>ing, 45=Shut down con-<br>troller, 48=Adaptive liquid<br>control|**R-W**<br>0-X|**Code**<br>u00|**1**<br>**2**<br>*<br>*|**3**<br>*|**4**<br>*|**5**<br>*|**6**<br>*|**7**<br>*|**8**<br>*|**9**<br>*|**Min. value **<br>0|**Max. value **<br>48|**Fact. value**<br>0|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|S5 Evaporator A||0-X|u09|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|DI1 Status|0=OFF, 1=ON|0-X|u10|*<br>*|*|*||||||0|1|0|
|Defrost time A||0-X|u11|*<br>*|*|*|*|*|*|*|*|0 min|900 min|0 min|
|S3 Air ON evap. A||0-X|u12|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Night condition|0=OFF, 1=ON|0-X|u13|*<br>*|*|*|*|*|*|*|*|0|1|0|
|S4 Air OFF evap. A||0-X|u16|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Thermostat air temp. A||0-X|u17|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Thermostat runtime A||0-X|u18|*<br>*|*|*|*|*|*|*|*|0 min|999 min|0 min|
|S2 Gas outlet A||0-X|u20||||*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Superheat A||0-X|u21||||*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Superheat reference A||0-X|u22||||*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|EEV opening A||0-X|u23||||*|*|*|*|*|0 %|100 %|0%|

|**Function**<br>Pe Evap. pressure|**Values**|**R-W**<br>0-X|**Code**<br>u25|**1**<br>**2**|**3**|**4**|**5**<br>*|**6**<br>*|**7**<br>*|**8**<br>*|**9**<br>*|**Min. value **<br>-1.0 Bar|**Max. value **<br>200.0 Bar|**Fact. value**<br>0.0Bar|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Te Evap. temp.||0-X|u26||||*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|DI2 Status|0=OFF, 1=ON|0-X|u37|*<br>*|*|*|*|*|*|*|*|0|1|0|
|Display readout 1||0-X|u56|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Alarm air temp. A||0-X|u57|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Compressor 1|0=OFF, 1=ON|0-X|u58|*<br>*|*|*|*||||*|0|1|0|
|Fan|0=OFF, 1=ON|0-X|u59|*<br>*|*|*|*|*|*|*|*|0|1|0|
|Defrost A|0=OFF, 1=ON|0-X|u60|*<br>*|*|*|*|*|*|*|*|0|1|0|
|Rail heat|0=OFF, 1=ON|0-X|u61||*|*||||*|*|0|1|0|
|Alarm relay|0=OFF, 1=ON|0-X|u62|*||*||*|||*|0|1|0|
|Light|0=OFF, 1=ON|0-X|u63|*||*|||*||*|0|1|0|
|Compressor 2|0=OFF, 1=ON|0-X|u67|||*|||||*|0|1|0|
|Blinds|0=OFF, 1=ON|0-X|u82|||*|||||*|0|1|0|
|Air heater|0=OFF, 1=ON|0-X|u84|||*|||||*|0|1|0|
|Railheat power||0-X|u85|*<br>*|*|*|*|*|*|*|*|0 %|100 %|0%|
|Thermostat band|1=Band 1, 2=Band 2|0-X|u86|*<br>*|*|*|*|*|*|*|*|1|2|1|
|Thermostat cutin temp.||0-X|u90|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|4.0 °C|
|Thermostat cutout temp.||0-X|u91|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|2.0 °C|
|Brine valve opening||0-X|U02|*<br>*|*|*||||||0 %|100 %|0%|
|Fan ECO|0=OFF, 1=ON|0-X|U37|||*|||||*|0|1|0|
|Network status||0-X|U45|*<br>*|*|*|*|*|*|*|*|0 %|100 %|0%|
|Rail heat PWM||0-X|U59|*<br>*|*|*|*|*|*|*|*|0 %|100 %|0%|
|Food temperature A||0-X|U72|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Defrost sensor tempera-<br>ture A||0-X|U73|*<br>*|*|*|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|

### **Operation via AK-UI55 Bluetooth**

##### **Access to parameters via Bluetooth and app**

1. App can be downloaded from App Store and Google Play.

- Name = AK-CC55 Connect

- Start the app.

2. Click on the display’s Bluetooth button for 3 seconds.

- The Bluetooth light will then flash while display is showing the controller’s address.

3. Connect to the controller from the app.

###### **Figure 48: AK-UI55 Bluetooth**

##### **Display info:**

- Loc

- The operation is locked and cannot be operated via Bluetooth.

- Unlock from the system manager.

*[Figurtekst: Fi g ure 49: Connect to controller Fi g ure 50: Controller dashboard]*

*[Figurtekst: Fi g ure 51: Set-u p  menu]*

The functions are described on Page 45 – Page 57.

### **AK-CC55 Connect menu (SW ver. 2.1x)**

### **Start / Stop**

**Table 23: Start / Sto** **p**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Main switch|Start / stop of refrigeration. With this setting refrigera-<br>tion can be started, stopped or a manual override of<br>the outputs can be allowed. (For manual control the<br>value is set at -1. Then the outputs can be force con-<br>trolled. Start / stop of refrigeration can also be accom-<br>plished with the external switch function connected<br>to a DI input.Stopped control will give a ”Main switch<br>OFF" alarm.|-1=Manual, 0=Stop, 1=Start|r12|r12 Main switch|
|Delay of outputs at<br>power up|Delay of output signal after start-up After start-up or a<br>power failure the controller’s functions can be de-<br>layed so that overloading of the electricity supply net-<br>work is avoided. Here you can set the time delay.||o01|o01 DelayOfOutp.|

### **Conf i** **guration**

**Table 24: Confi** **g uration**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Main switch|Start / stop of refrigeration. With this setting refrigera-<br>tion can be started, stopped or a manual override of<br>the outputs can be allowed. (For manual control the<br>value is set at -1. Then the outputs can be force con-<br>trolled. Start / stop of refrigeration can also be accom-<br>plished with the external switch function connected<br>to a DI input.Stopped control will give a ”Main switch<br>OFF" alarm.|-1=Manual, 0=Stop, 1=Start|r12|r12 Main switch|
|Application mode|Selection of application The controller covers several<br>applications for control of a refrigerated case. Here<br>you set which of the possible applications is re-<br>quired.This menu can only be set when regulation is<br>stopped, i.e. “r12 Main Switch” is set to 0.|1=1. Comp/Alarm/Fan/Defrost, 2=2. Comp/Light/Fan/<br>Defrost, 3=3. Comp/Railheat/Fan/Defrost, 4=4. Comp/<br>Custom, 5=5. EEV/Comp/Fan/Defrost, 6=6. EEV/<br>Alarm/Fan/Defrost, 7=7. EEV/Light/Fan/Defrost, 8=8.<br>EEV/Rail/Fan/Defrost, 9=9. EEV/Custom|o61|o61 Appl. mode|
|DO2 Configuration|Select the function of the digital output|0=None, 1=Fans, 2=Fan ECO, 3=Defrost, 4=Rail heat,<br>5=Alarm, 6=Light, 7=Blinds, 8=Compressor/LLSV,<br>9=Compressor 2, 10=Air heater|q02|q02 DO2 Config.|
|DO3 Configuration|Select the function of the digital output|0=None, 1=Fans, 2=Fan ECO, 3=Defrost, 4=Rail heat,<br>5=Alarm, 6=Light, 7=Blinds, 8=Compressor/LLSV,<br>9=Compressor 2, 10=Air heater|q03|q03 DO3 Config.|
|DO4 Configuration|Select the function of the digital output|0=None, 1=Fans, 2=Fan ECO, 3=Defrost, 4=Rail heat,<br>5=Alarm, 6=Light, 7=Blinds, 8=Compressor/LLSV,<br>9=Compressor 2, 10=Air heater|q04|q04 DO4 Config.|
|AO1 Configuration|Select the function of the analogue output|0=None, 1=Rail heat PWM|q09|q09 AO1 Config.|
|DI1 Configuration|Select the function of the digital input|0=None, 1=DI status, 2=Door function, 3=Door alarm,<br>4=Defrost start, 5=Main switch, 6=Night setback,<br>7=Thermostat band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced cooling,<br>12=Open blinds, 13=Coordinated defrost, 14=Forced<br>closing, 15=Shutdown, 16=Light control, 20=Leak de-<br>tection, 21=Adaptive liquid control, 29=Door fan stop|o02|o02 DI1 Config.|
|DI2 Configuration|Select the function of the digital input|0=None, 1=DI status, 2=Door function, 3=Door alarm,<br>4=Defrost start, 5=Main switch, 6=Night setback,<br>7=Thermostat band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced cooling,<br>12=Open blinds, 13=Coordinated defrost, 14=Forced<br>closing, 15=Shutdown, 16=Light control, 20=Leak de-<br>tection, 21=Adaptive liquid control, 29=Door fan stop|o37|o37 DI2 Config.|
|Refrigerant|Select the type of refrigerant. If the required refriger-<br>ant is not part of the list, the user defined option can<br>be used. Please contact Danfoss for detailed informa-<br>tionWarning: Wrong selection of refrigerant may<br>cause damage to the system.|0=Not seleted, 6=R13, 7=R13b1, 2=R22, 8=R23,<br>14=R32, 11=R114, 3=R134a, 12=R142b, 24=R170,<br>15=R227, 25=R290, 16=R401A, 18=R402A, 19=R404A,<br>21=R407A, 22=R407B, 20=R407C, 37=R407F,<br>49=R407H, 23=R410A, 32=R413A, 30=R417A,<br>31=R422A, 33=R422D, 34=R427A, 35=R438A,<br>40=R448A, 41=R449A, 48=R449B, 43=R450A,<br>44=R452B, 45=R454B, 9=R500, 4=R502, 10=R503,<br>17=R507, 36=R513A, 26=R600, 27=R600a, 5=R717,<br>28=R744, 46=R1233zdE, 38=R1234ze, 39=R1234yf,<br>47=R1234zeZ, 29=R1270, 42=R452A, 1=User defined,<br>13=User defined display|o30|o30 Refrigerant|
|Refrigerant factor K1|Refrigerant factor for a custom refrigerant - please<br>contact Danfoss for detailed information||P83|P83 RfgFac.K1|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Refrigerant factor K2|Refrigerant factor for a custom refrigerant - please<br>contact Danfoss for detailed information||P84|P84 RfgFac.K2|
|Refrigerant factor K3|Refrigerant factor for a custom refrigerant - please<br>contact Danfoss for detailed information||P85|P85 RfgFac.K3|
|Refrigerant factor<br>A1|Refrigerant factor for a custom refrigerant - please<br>contact Danfoss for detailed information||x65|--- Rfg.Fac.A1|
|Refrigerant factor<br>A2|Refrigerant factor for a custom refrigerant - please<br>contact Danfoss for detailed information||x66|--- Rfg.Fac.A2|
|Refrigerant factor<br>A3|Refrigerant factor for a custom refrigerant - please<br>contact Danfoss for detailed information||x67|--- Rfg.Fac.A3|
|Pe Min range|Minimum measuring range for sensor||o20|o20 MinTransPres|
|Pe Max range|Maximum measuring range for sensor||o21|o21 MaxTransPres|
|Temperature sensor<br>type|Sensor type for S3, S4 and S5. Normally a Pt 1000 sen-<br>sor with great signal accuracy is used. But you can al-<br>so use a sensor with another signal accuracy. That<br>could e.g. be a PTC sensor (1000 ohm at 25 °C). All the<br>mounted sensors S3-S5 must be of the same type.|0=Pt 1000, 1=PTC 1000, 2=NTC 5k, 3=NTC 10k,<br>4=User-defined|o06|o06 SensorConfig|
|Sensor point 1 -<br>Temp.|The temperature value for the user-defined tempera-<br>ture sensor in the reference point.||X20|--- SP1 Temp|
|Sensor point 1 -<br>kohm|The resistance value in kohm for the user-defined<br>temperature sensor in the reference point.||X21|--- SP1 kohm|
|Sensor point 1 -<br>ohm|The resistance value in ohm for the user-defined tem-<br>perature sensor in the reference point.||X22|--- SP1 ohm|
|Sensor point 2 -<br>Temp.|The temperature value for the user-defined tempera-<br>ture sensor in the reference point.||X23|--- SP2 Temp|
|Sensor point 2 -<br>kohm|The resistance value in kohm for the user-defined<br>temperature sensor in the reference point.||X24|--- SP2 kohm|
|Sensor point 2 -<br>ohm|The resistance value in ohm for the user-defined tem-<br>perature sensor in the reference point.||X25|--- SP2 ohm|
|Sensor point 3 -<br>Temp.|The temperature value for the user-defined tempera-<br>ture sensor in the reference point.||X26|--- SP3 Temp|
|Sensor point 3 -<br>kohm|The resistance value in kohm for the user-defined<br>temperature sensor in the reference point.||X27|--- SP3 kohm|
|Sensor point 3 -<br>ohm|The resistance value in ohm for the user-defined tem-<br>perature sensor in the reference point.||X28|--- SP3 ohm|
|Defrost method|Select method of defrost|0=None, 1=Electrical, 2=Hot gas, 3=Brine, 4=Air/<br>Offcycle|d01|d01 Def. method|
|Defrost stop meth-<br>od|Here you define whether a defrost cycle is to be stop-<br>ped by time or by a temperature sensor|0=Time, 1=S5 sensor, 2=S4 sensor|d10|d10 DefStopSens.|
|Defrost stop limit A|When the selected defrost stop sensor reaches the set<br>limit, the defrost cycle is terminated||d02|d02 Def.StopTemp|
|Food type|When changing the food type the controller will auto-<br>matically adapt temperature setpoints and alarm lim-<br>its according to the selected food type. Please be<br>aware that the setting will revert to "None" after hav-<br>ing been changed.|0=None, 1=Vegetables, 2=Dairy, 3=Meat and fish,<br>4=Frozen food, 5=Ice cream|r89|r89 Food type|
|Food temp. sensor<br>Network address|Select the temperature to be used for the food tem-<br>perature representation<br>Network address of the controller|1=Thermostat air, 2=Alarm air, 3=S3 Air ON evap.|q39<br>o03|q39 Food sensor<br>o03 Unit addr.|

### **Thermostat control**

###### **Table 25: Thermostat control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Thermostat air<br>temp. A|Thermostat temperature||u17|u17 Ther. air|
|Food temperature A|Read out of food temperature||U72|U72 Food temp.|
|S3 Air ON evap. A|Actual sensor value||u12|u12 S3 air temp.|

|**Function**<br>|**Description**<br>|**Values**|**Code**<br>|**Short name**<br>|
|---|---|---|---|---|
|S4 Air OFF evap. A|Actual sensor value||u16|u16 S4 air temp.|
|Night condition|Status at the day-/night operation (night operation:<br>on/off)|0=OFF, 1=ON|u13|u13 Night Cond.|
|Thermostat cutin<br>temp.|Readout of the actual cutin value for the thermostat||u90|u90 Cutin temp.|
|Thermostat cutout<br>temp.|Readout of the actual cut out value for the thermostat||u91|u91 Cutout temp.|
|Thermostat runtime<br>A|Read the ongoing cutin time for the thermostat or the<br>duration of the last completed cutin||u18|u18 Ther runtime|
|Thermostat band|Readout of which thermostat used for regulation: 1=<br>Thermostat band 12= Thermostat band 2|1=Band 1, 2=Band 2|u86|u86 Ther. band|
|Air heater|Actual status of output function|0=OFF, 1=ON|u84|u84 Heat relay|
|Thermostat mode|Here it is defined how the thermostat is to operate. Ei-<br>ther as an ordinary ON/OFF thermostat or as a modu-<br>lating thermostat.When operation is ”modulating” the<br>valve will limit the flow of refrigerant so that the tem-<br>perature variation will be less than for the ON/OFF<br>thermostat.The thermostat differential (r01) must not<br>be set lower than 2K for ""modulating"".In a decentral-<br>ised plant you must select the ON/OFF thermostat<br>setting."|2=Modulating, 1=ON/OFF|r14|r14 Therm. mode|
|Cutout 1|Set point. The thermostat’s cutout value when the<br>given thermostat band is in use||r00|r00 Cutout|
|Differential 1|When the temperature is higher than the set cutout +<br>the set differential, the compressor relay will be cut in.<br>It will cut out again when the temperature comes<br>down to the set cutout limit||r01|r01 Differential|
|Cutout 2|Set point. The thermostat’s cutout value when the<br>given thermostat band is in use||r21|r21 Cutout 2|
|Differential 2|When the temperature is higher than the set cutout +<br>the set differential, the compressor relay will be cutin.<br>It will cutout again when the temperature comes<br>down to the set cut-out limit||r93|r93 Diff Th2|
|Max cutout limit|Setpoint limitation - The controller’s setting range for<br>the thermostat setpoint may be narrowed down, so<br>that much too high or much too low values are not<br>set accidentally - with resulting damages.To avoid a<br>too high setting of the setpoint, the max. allowable<br>reference value may be lowered||r02|r02 Max cutout|
|Min cutout limit|Setpoint limitation - The controller’s setting range for<br>the thermostat setpoint may be narrowed down, so<br>that much too high or much too low values are not<br>set accidentally - with resulting damages.To avoid a<br>too low setting of the setpoint, the min. allowable ref-<br>erence value may be increased||r03|r03 Min cutout|
|Thermostat sensor<br>S4 %|Selection of thermostat sensor. Here you define the<br>sensor the thermostat is to use for its control function.<br>S3, S4, or a combination of them. With the setting 0%,<br>only S3 is used. With 100%, only S4.||r15|r15 Ther. S4 %|
|Thermostat sensor<br>S4 % night|Selection of thermostat sensor S4% during night op-<br>eration with night blinds. Here you define the sensor<br>the thermostat is to use for its control function. S3, S4,<br>or a combination of them. With the setting 0%, only<br>S3 is used. With 100%, only S4.||r61|r61 Ther.S4% Ngt|
|Night offset|Night setback value.The thermostat’s reference will be<br>the setpoint plus this value when the controller<br>changes over to night operation.||r13|r13 Night offset|
|S4 frost protection|Frost protection on S4 air temperature. If the S4 tem-<br>perature sensors measures a temperature lower than<br>the set limit, refrigeration will be stopped in order to<br>protect produce from ice formation. Refrigeration will<br>start again when the S4 temperature has risen 2K<br>above the set limit||r98|r98 S4 Min Lim|
|Air heater neutral<br>zone|Heat function. Set the width of the Neutral Zone for<br>changeover from cooling to heating "||r62|r62 Heat NZ|

|**Function**|**Description**<br>**Values**|**Code**|**Short name**|
|---|---|---|---|
|Air heater start de-<br>lay|Time delay on transition from refrigeration phase to<br>heating phase (there is not time delay on transition<br>from heating phase to refrigeration phase)|r63|r63 HeatStartDel|
|Melt interval|Melt function. Only for control of MT cases/rooms (-5<br>to +10°C). The function ensures that the evaporator<br>will not be blocked by ice crystals. Here you set how<br>often the function is to stop the refrigeration and<br>hence transform the ice crystals to water.|r16|r16 MeltInterval|
|Melt period|Melt period. Here you set how long an on-going melt<br>function is to last|r17|r17 Melt period|

### **Alarm limits and delays**

**Table 26: Alarm limits and dela** **y s**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Alarm status|Actual alarm status|0=OFF, 1=ON|x16|--- Sum alarm|
|Alarm air temp. A|Measured temperature for alarm thermostat||u57|u57 Alarm air|
|High alarm limit|Readout of actual high alarm limit for the tempera-<br>ture monitoring||y10|--- High al. lim|
|Low alarm limit|Readout of actual low alarm limit for the temperature<br>monitoring||y11|--- Low al. lim|
|S3 Air ON evap. A|Actual sensor value||u12|u12 S3 air temp.|
|S4 Air OFF evap. A|Actual sensor value||u16|u16 S4 air temp.|
|Reset alarms|Command for resetting all alarms, unless they are still<br>active|0=OFF, 1=ON|x15|--- Reset alarm|
|Alarm sensor S4% A|Signal to the alarm thermostat Here you have to de-<br>fine the ratio between the sensors which the alarm<br>thermostat has to use. S3, S4 or a combination of the<br>two. With setting 0% only S3 is used. With 100% only<br>S4 is used||A36|A36 Alarm S4 %|
|High alarm limit 1|Upper alarm limit. The limit value is set in absolute<br>value. The limit value will be raised with the night off-<br>set during night operation.||A13|A13 HighLim Air|
|Low alarm limit 1|Lower alarm limit. The limit value is set in absolute<br>value||A14|A14 LowLim Air|
|High alarm limit 2|Upper alarm limit. The limit value is set in absolute<br>value. The limit value will be raised with the night off-<br>set during night operation.||A20|A20 HighLim2 Air|
|Low alarm limit 2|Lower alarm limit. The limit value is set in absolute<br>value||A21|A21 LowLim2 Air|
|Alarm delay A|Alarm delay (short alarm delay on air temperature). If<br>the upper or the lower alarm limit values are excee-<br>ded, a timer function will commence. The alarm will<br>not become active until the set time delay has been<br>passed. The time delay is set in minutes||A03|A03 Alarm delay|
|Alarm delay pull-<br>down A|Alarm delay at tempeature pulldown conditions (long<br>alarm delay). This time delay is used during start-up,<br>during defrost, immediately after a defrost. There will<br>be change-over to the normal time delay when the<br>temperature has dropped below the set upper alarm<br>limit.||A12|A12 Pulldown del|
|Door open alarm<br>delay|Time delay for door alarm||A04|A04 DoorOpen del|
|Door restart inj. de-<br>lay|Start of refrigeration when door is open. If the door<br>has been left open, refrigeration will be started after<br>the set time.||o89|o89 DoorInjStart|
|Alarm delay DI 1|Time delay for digital input alarm||A27|A27 Al.Delay DI1|
|Alarm delay DI 2|Time delay for digital input alarm||A28|A28 Al.Delay DI2|

### **Injection control**

**Table 27: In** **j ection control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Thermostat air<br>temp. A|Thermostat temperature||u17|u17 Ther. air|
|S3 Air ON evap. A|Actual sensor value||u12|u12 S3 air temp.|
|S4 Air OFF evap. A|Actual sensor value||u16|u16 S4 air temp.|
|EEV opening A|Actual status of output function||u23|u23 EEV OD %|
|Pe Evap. pressure|Actual sensor signal||u25|u25 EvapPress Pe|
|Te Evap. temp.|Temperature converted from pressure||u26|u26 EvapTemp Te|
|S2 Gas outlet A|Actual sensor value||u20|u20 S2 temp.|
|Superheat A|Readout of actual superheat at the outlet of the evap-<br>orator||u21|u21 Superheat|
|Superheat reference<br>A|Read out of the actual superheat reference||u22|u22 SuperheatRef|
|Brine valve opening|Actual status of output function||U02|U02 PWM OD %|
|Min superheat limit|Min. value for the superheat reference||n10|n10 Min SH|
|Max superheat limit|Max. value for the superheat reference||n09|n09 Max SH|
|MOP temperature|MOP temperature. The valve opening degree is re-<br>duced until the evaporating temperature reaches the<br>set MOP limit. If no MOP function is required, select<br>highest value, which corresponds to OFF||n11|n11 MOP temp.|
|AKV Period time|Period time for the pulse width modulation||n13|n13 AKV Period|
|Min superheat liq-<br>uid ctrl|Min. value for the superheat reference during adap-<br>tive liquid control||P87|P87 SH Min Liq.|
|Max superheat liq-<br>uid ctrl.|Max. value for the superheat reference during adap-<br>tive liquid control||P86|P86 SH Max Liq.|
|Brine valve - Period<br>time|Period time for the pulse width modulation||n63|n63 Pwm Period|
|Brine valve max OD|Expert setting - please contact Danfoss for further in-<br>fo||n64|n64 Pwm Max. OD|
|Brine valve min OD|Expert setting - please contact Danfoss for further in-<br>fo||n65|n65 Pwm Min. OD|
|Brine valve windup|Expert setting - please contact Danfoss for further in-<br>fo||n66|n66 PwmWindUp-<br>Fac|
|Brine valve Kp|Expert setting - please contact Danfoss for further in-<br>fo||n67|n67 Pwm Kp fact.|
|Brine valve Tn|Expert setting - please contact Danfoss for further in-<br>fo||n68|n68 Pwm Tn sec|

### **Defrost control**

**Table 28: Defrost control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Defrost sensor tem-<br>perature A|Actual temperature of selected defrost stop sensor||U73|U73 Def.StopTemp|
|S5 Evaporator A|Actual sensor value||u09|u09 S5 temp.|

|**Function**<br>Defrost A|**Description**<br>Actual status of output function|**Values**<br>0=OFF, 1=ON|**Code**<br>u60|**Short name**<br>u60 Def. relay|
|---|---|---|---|---|
|Defrost time A|<br>Read the duration of the ongoing defrost or the dura-<br>tion of the last completed defrost.||u11|<br>u11 Defrost time|
|Start defrost|Command for starting a defrost|0=OFF, 1=ON|x09|--- Def. Start|
|Stop defrost|Command for stopping an ongoing defrost cycle|0=OFF, 1=ON|x10|--- Def. Stop|
|Defrost method|Select method of defrost|0=None, 1=Electrical, 2=Hot gas, 3=Brine, 4=Air/<br>Offcycle|d01|d01 Def. method|
|Defrost stop meth-<br>od|Here you define whether a defrost cycle is to be stop-<br>ped by time or by a temperature sensor|0=Time, 1=S5 sensor, 2=S4 sensor|d10|d10 DefStopSens.|
|Defrost stop limit 1|When the selected defrost stop sensor reaches the set<br>limit, the defrost cycle is terminated||d02|d02 Def.StopTemp|
|Defrost stop limit 2|Defrost stop temperature limit when thermostat band<br>2 is in operation.When the selected defrost stop sen-<br>sor reaches the set limit, the defrost cycle is termina-<br>ted||d28|d28 DefStopTemp2|
|Min. defrost time|Minimum duration of a defrost cycle. The defrost cy-<br>cle will as a minimum run for the set minimum defrost<br>time once it is started||d24|d24 Min Def Time|
|Max. defrost time 1|Max. duration of a defrost cycle. The setting is also<br>used as a safety time if the defrost is stopped on tem-<br>perature. If the selected defrost stop sensor does not<br>reach the set defrost stop temperature limit within<br>the set time, the defrost will be stopped anyway.||d04|d04 Max Def.time|
|Max. defrost time 2|Max. duration of a defrost cycle when thermostat<br>band 2 is in operation. The setting is also used as a<br>safety time if the defrost is stopped on temperature. If<br>the selected defrost stop sensor does not reach the<br>set defrost stop temperature limit within the set time,<br>the defrost will be stopped anyway.||d29|d29 MaxDefTime2|
|Defrost start interval|The function is zeroset and will start the timer func-<br>tion at each defrost start. When the time has expired<br>the function will start a defrost. The function is used<br>as a simple defrost start, or it may be used as a safe-<br>guard if the normal signal fails to appear. If master/<br>slave defrost without clock function or without data<br>communication is used, the interval time will be used<br>as max. time between defrosts. If a defrost start via<br>data communcation does not take place, the interval<br>time will be used as max. time between de-<br>frosts.When there is defrost with clock function or da-<br>ta communication, the interval time must be set for a<br>somewhat longer period of time than the planned<br>one. In connection with power failure the interval<br>time will be maintained, and when the power returns<br>the interval time will continue from the maintained<br>value. he interval time is not active when set to 0||d03|d03 Def.Interval|
|Time staggering<br>power up|Time staggering for defrost cutins during start-up The<br>function is only relevant if you have several refrigera-<br>tion appliances or groups where you want the defrost<br>to be staggered in relation to one another. The func-<br>tion is furthermore only relevant if you have chosen<br>defrost with interval start. The function delays the in-<br>terval time by the set number of minutes, but it only<br>does it once, and this at the very first defrost taking<br>place when voltage is connected to the controller.<br>The function will be active after each and every pow-<br>er failure.||d05|d05 Time stagg.|
|Max thermostat run-<br>time|Defrost on demand – aggregate refrigeration time Set<br>here is the refrigeration time allowed without de-<br>frosts. If the time is passed, a defrost will be started.<br>With setting = 0 the function is not in use.||d18|d18 MaxTherRunT.|
|Pump down delay|Set the time where the evaporator is emptied of re-<br>frigerant prior to the actual defrost cycle||d16|d16 Pump dwn del|
|Drip off time|Here you set the time that is to elapse from a defrost<br>and until the compressor is to start again. (The time<br>when water drips off the evaporator).||d06|d06 DripOff time|
|Max hold time|Max. standby time after coordinated defrost. When a<br>controller has completed a defrost it will wait for a<br>signal which tells that the refrigeration may be re-<br>sumed. If this signal fails to appear for one reason or<br>another, the controller will itself start the refrigeration<br>when this standby time has elapsed.||o16|o16 MaxHoldTime|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Fan control during<br>defrost|Fan operation during defrost Here you can set how<br>the fan is to operate during defrost.0: Stopped (Runs<br>during pump down)1: Running (stopped during "fan<br>delay")2: Running during pump down and defrost. Af-<br>ter that stopped3: Running during pump down and<br>defrost until defrost stop sensor reaches fan stop tem-<br>perature limit|0=OFF, 1=ON, 2=OFF at drip, 3=OFF at high temp|d09|d09 FanDuringDef|
|Fan start delay|Delay of fan start after defrost. Here you set the time<br>that is to elapse from compressor start after a defrost<br>and until the fan may start again. (The time when re-<br>maining water is transformed into ice on the evapora-<br>tor).||d07|d07 FanStartDel|
|Fan start tempera-<br>ture|Temperature limit for starting the fans after a defrost.<br>When the measured S5 evaporator temperature is<br>getting below the set limit, the fans are started||d08|d08 FanStartTemp|
|Fan stop tempera-<br>ture|If the fan control during defrost has been set up for it,<br>the fans can be stopped during the defrost if the de-<br>frost sensor exceeds the set temperature limit||d41|d41 Def Fan Stop|
|Rail heat during de-<br>frost|Define how railheat is controlled during defrost0: Rail-<br>heat is OFF all the time1: Railheat is ON all the time2:<br>Normal railheat control|0=OFF, 1=ON, 2=Normal control|d27|d27 Railh.at def|
|Display delay after<br>defrost|Set the maximum time the display should show the<br>defrost code "-d-" after a defrost. The normal temper-<br>ature readout is normally started when the tempera-<br>ture in the case is OK again or if a high temperature<br>alarm is raised.||d40|d40 Disp. d del.|

### **Defrost schedules**

**Table 29: Defrost schedules**

|**Function**<br>**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|
|Defrost schedule|0=No, 1=Yes|t00|t00 Def.Schedule|
|Def. start 1 - Hours||t01|t01 Def. 1 hr.|
|Def. start 1 - Minutes||t11|t11 Def. 1 min.|
|Def. start 2 - Hours||t02|t02 Def. 2 hr.|
|Def. start 2 - Minutes||t12|t12 Def. 2 min.|
|Def. start 3 - Hours||t03|t03 Def. 3 hr.|
|Def. start 3 - Minutes||t13|t13 Def. 3 min.|
|Def. start 4 - Hours||t04|t04 Def. 4 hr.|
|Def. start 4 - Minutes||t14|t14 Def. 4 min.|
|Def. start 5 - Hours||t05|t05 Def. 5 hr.|
|Def. start 5 - Minutes||t15|t15 Def. 5 min.|
|Def. start 6 - Hours||t06|t06 Def. 6 hr.|
|Def. start 6 - Minutes||t16|t16 Def. 6 min.|
|Monday - Follow<br>schedule|0=No, 1=Yes|t51|t51 Mon.Schedule|
|Tuesday - Follow<br>schedule|0=No, 1=Yes|t52|t52 Tue.Schedule|
|Wednesday - Follow<br>schedule|0=No, 1=Yes|t53|t53 Wed.Schedule|
|Thursday - Follow<br>schedule|0=No, 1=Yes|t54|t54 Thu.Schedule|
|Friday - Follow<br>schedule|0=No, 1=Yes|t55|t55 Fri.Schedule|
|Saturday - Follow<br>schedule|0=No, 1=Yes|t56|t56 Sat.Schedule|
|Sunday - Follow<br>schedule|0=No, 1=Yes|t57|t57 Sun.Schedule|

### **Compressor**

**Table 30: Com** **p ressor**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Compressor 1|Actual status of output function|0=OFF, 1=ON|u58|u58 Comp1/LLSV|
|Compressor 2|Actual status of output function|0=OFF, 1=ON|u67|u67 Comp2 relay|
|Min ON time|Minimum time the compressor is to run once it has<br>been started.||c01|c01 Min. On time|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Min OFF time|Minimum time the compressor has to be stopped||c02|c02 Min.Off time|
|Delay between<br>comp.|Time delay for couplings of two compressors. The<br>step delay is the time that has to elapse from the first<br>compressor cuts in and until the next compressor can<br>cut in.||c05|c05 Step delay|
|Step control mode|Selection of step control mode for compressors. At se-<br>quential mode compressor 1 will always be the first to<br>start and the last to stop. In cyclic mode the run time<br>between the compressor will be equalized.|1=Sequential, 2=Cyclic|c08|c08 Step mode|
|Comp. 2 ctrl. Th.<br>band 2|Select whether compressor 2 is to be in operation in<br>thermostat band 2|0=OFF, 1=ON|c85|c85 Cmp2 In Th2|

### **Fan control**

**Table 31: Fan control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Fan|Actual status of output function|0=OFF, 1=ON|u59|u59 Fan relay|
|Fan ECO|Actual status of output function|0=OFF, 1=ON|U37|U37 Fan Eco|
|Fan pulsing mode|Pulse operation of fan 0: No pulse operation 1: Pulse<br>operation when the thermostat is cut out2: Pulse op-<br>eration when the thermostat is cut out, but only dur-<br>ing night operation|0=No pulsing, 1=Pulsing cutout, 2=Pulsing cutout<br>night|F05|F05 FanPulseMode|
|Fan period time|Periodtime for pulsing of fan||F06|F06 Fan cycle|
|Fan ON cycle|ON time for fan. The ON period is set as a percentage<br>of the period time||F07|F07 Fan ON %|
|Fan stop high S5<br>temp.|Fan stop temperature The function stops the fans in<br>an error situation, so that they will not provide power<br>to the appliance. If the defrost sensor registers a high-<br>er temperature than the one set here, the fans will be<br>stopped. There will be re-start at 2 K below the set-<br>ting. The function is not active during a defrost or<br>start-up after a defrost.||F04|F04 FanStop temp|
|Fan at forced closing|You can set whether fans should be operational or<br>stopped if the function "Forced closing" is activated<br>here. 0: Fans are OFF1: Fans are ON2: Fans are OFF and<br>defrost is not permitted3: Fans are ON and defrost is<br>not permitted|0=OFF, 1=ON, 2=OFF and suppress defrost, 3=ON and<br>suppress defrost|o90|o90 Fan ForcedCl|
|Fan stop at blinds<br>closing|When blinds are closing the fans are stopped in the<br>defined time delay in order to ensure that the blinds<br>are closed correctly||P65|P65 BlindFanStop|

### **Railheat control**

**Table 32: Railheat control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Dewpoint|Actual dewpoint received from system manager via<br>network||x18|--- Dew point|
|Rail heat|Actual status of output function|0=OFF, 1=ON|u61|u61 Railh. relay|
|Railheat power|Readout of the actual rail power in %||u85|u85 Rail DutyC %|
|Rail heat PWM|Actual status of output function||U59|U59 Railheat PWM|

|**Function**|**Description**<br>**Values**|**Code**|**Short name**|
|---|---|---|---|
|Rail heat control<br>mode|The rail heat can be controlled in several ways: 0: Rail-<br>heat is running all the time 1: Pulse control is used<br>with a timer function following the day/night opera-<br>tion 2: Pulse control is used with a dew point function.<br>This function requires that a signal is received about<br>the dew point value. The value is measured by a sys-<br>tem manager and sent to the controller via the data<br>communication.<br>0=ON, 1=Day/Night timer, 2=Dew point ctrl.|o85|o85 Railh. mode|
|Rail heat ON cycle<br>day|Railheat power during day time. The ON period is set<br>as a percentage of the period|o41|o41 Railh.ONday%|
|Rail heat ON cycle<br>night|Railheat power during night time. The ON period is<br>set as a percentage of the period time|o42|o42 Railh.ONngt%|
|Rail heat period<br>time|Periodtime for pulsing of railheat|o43|o43 Railh.cycle|
|Rail heat PWM - Peri-<br>od time|Period time for the pulse width modulation|P82|P82 RailCyclePWM|
|Rail heat min ON cy-<br>cle|Lowest permitted rail heat power. When the meas-<br>ured dew point is below the defined minimum limit<br>the rail heat will run with the set minimum power|o88|o88 Rail Min ON%|
|Dewpoint min limit|If the measuered dew point is below the set value the<br>rail heat is running at minimum heat|o86|o86 DewP Min lim|
|Dewpoint max limit|If the measured dew point is above the set value the<br>rail heat is maximum|o87|o87 DewP Max lim|

### **Light/Blinds/Cleaning control**

**Table 33: Li** **g ht/Blinds/Cleanin** **g control**

|**Function**<br>Control state A|**Description**<br>Readout of the actual control state of the controller|**Values**<br>0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>14=Defrost, 15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period, 19=Modulating<br>temp. control, 20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection, 25=Manual<br>control, 26=No refrigerant selected, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|**Code**<br>u00|**Short name**<br>u00 Ctrl. state|
|---|---|---|---|---|
|Night condition|Status at the day-/night operation (night operation:<br>on/off)|0=OFF, 1=ON|u13|u13 Night Cond.|
|Light|Actual status of output function|0=OFF, 1=ON|u63|u63 Light relay|
|Blinds|Actual status of output function|0=OFF, 1=ON|u82|u82 Blinds relay|
|Light control mode|Configuration of light function1: Light is controlled<br>via day/night status 2: Light is controlled via data<br>communication and master control parameter "MC<br>Light signal" 3: Light is controlled by door contact on<br>DI input. When the door is opened the relay will cut<br>in. When the door is closed again there will be a time<br>delay of two minutes before the light is switched off.<br>4: As "2" but if there are any 15-minute network errors,<br>the light will switch on and the night blind will open.<br>5: Light is controlled via DI input signal|1=Day and night, 2=Network, 3=Door switch, 4=Net-<br>work (Fallback), 5=Digital input|o38|o38 Light config|
|Light at Main switch<br>OFF|Define how light and blinds are to be controlled at<br>Main switch OFF 0: Light is switched off and night<br>blinds are open when the main switch is off 1: Light<br>and night blinds are independent of main switch.|0=OFF, 1=Normal ctrl.|o98|o98 Light MS=Off|
|Blinds max open<br>time|Time delay from when blinds have been opened<br>manually until they close again||P60|P60 BlindOpenTim|
|Case cleaning mode|The status of the function can be followed here or the<br>function can be started manually.0 = Normal opera-<br>tion (no cleaning) 1 = Only fans are running to defrost<br>the evaporator. All other outputs are Off. 2 = Cleaning<br>with stopped fans. All outputs are Off. If the function<br>is controlled by a digital input signal, the relevant sta-<br>tus can be seen here in the menu.|0=OFF, 1=Fans run, 2=Cleaning|o46|o46 Case clean|

### **Display control**

**Table 34: Dis** **p la** **y control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 2=Min ON timer,<br>3=Min OFF timer, 4=Drip off, 10=Main switch OFF,<br>11=Thermostat cut-out, 12=Frost protection S4,<br>13=Not_used, 14=Defrost, 15=Fan delay, 17=Door<br>open, 18=Melt period, 19=Modulating temp. control,<br>20=Emergency control, 23=Adaptive superheat con-<br>trol, 24=Start injection, 25=Manual control, 26=No re-<br>frigerant selected, 16=Forced closing, 29=Case clean-<br>ing, 30=Forced cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down controller,<br>48=Adaptive liquid control|u00|u00 Ctrl. state|
|Display readout 1|Read out of the temperature shown on the display||u56|u56 Display air|
|Display air S4%|Signal to the display sensor. Here you have to define<br>the ratio between the sensors which the display has<br>to use. S3, S4 or a combination of the two. With set-<br>ting 0% only S3 is used. With 100% only S4 is used||o17|o17 Disp. S4 %|
|Display readout ad-<br>justment|Correction of the display´s temperature.If the temper-<br>ature at the products and the temperature received<br>by the controller are not identical, an offset adjust-<br>ment of the display temperature can be carried out."||r04|r04 Disp. Adj. K|
|Temperature unit|Select whether temperatures are to be shown as °C or<br>as °F.|0=Celsius, 1=Fahrenheit|r05|r05 Temp.unit|
|Display keyboard<br>lock|With this setting it is possible to lock the keyboard<br>operation of the local display.<br>None: Display keyboard operation will never be<br>locked.<br>Local: When not used for some time, the local display<br>will lock the keyboard operations and a special key<br>combination is required in order to enable the key-<br>board operations.<br>Network: When the controller receives a master con-<br>trol signal (--- Key/BT lock) via the network, the dis-<br>play keyboard operations will be locked. The key-<br>board operations can only be activated again by set-<br>ting the master control signal OFF via the System<br>Manager.|0=None, 1=Local, 2=Network|P89|P89 LockDispKey|

### **Alarm relay priorities**

**Table 35: Alarm rela** **y p riorities**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Alarm relay|Actual status of output function|0=OFF, 1=ON|u62|u62 Alarm relay|
|Alarm relay priority|Set which alarm priorities that are to activate the<br>alarm relay: 0=Not used, alarm relay is not used1:<br>High, alarm with high priority will activate relay2: Me-<br>dium, alarms with high or medium priority will acti-<br>vate the alarm relay3: All, all alarms will activate alarm<br>relay|0=Not used, 1=High Priority, 2=Medium priority,<br>3=All|P41|P41 Al.Rel.Prio|
|Mute alarm|When muting alarms, the alarm relay will stop signal-<br>ling the alarm until a new alarm arises|0=OFF, 1=ON|q38|q38 Mute Alarm|
|High temperature -<br>Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q28|q28 Hi Temp Prio|
|Low temperature -<br>Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q29|q29 Lo Temp Prio|
|Sensor errors - Prior-<br>ity|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q30|q30 Sensor Prio|
|DI alarms - Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q31|q31 DIAlarm Prio|
|Defrost - Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q32|q32 Defrost Prio|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Miscellaneous - Pri-<br>ority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q33|q33 Misc Prio|
|Injection - Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q34|q34 Inject Prio|
|Control stopped -<br>Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q35|q35 CtrlOFF Prio|
|Leak detection - Pri-<br>ority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q36|q36 Leak Prio|

### **Miscellaneous**

**Table 36: Miscellaneous** → **Access codes**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Access code 3|Access code for local display||o05|o05 Acc. code 3|
|Access code 2|Access code for local display||o64|o64 Acc. code 2|
|Access code 1|Access code for local display||P88|P88 Acc. code 1|
|**Table 37: Miscel**<br>**Function**|**laneous**→**Network**<br>**Description**|**Values**|**Code**|**Short name**|
|Network status|Quality of the network communication||U45|U45 Comm. status|
|Network address|Network address of the controller||o03|o03 Unit addr.|
|Baudrate|Communication speed of network|1=Auto, 2=9600 Baud, 3=19200 Baud, 4=38400 Baud|x96|--- Bus baudrate|
|Parity and stop bit|Select parity and stop bit of Modbus messages|0=None, 1=Even, 2=Odd|x97|--- Parity bit|

###### **Table 37: Miscellaneous** → **Network**

**Table 38: Miscellaneous** → **Sensor ad** **j ustment**

|**Function**|**Description**<br>**Values**|**Code**|**Short name**|
|---|---|---|---|
|S2 Gas outlet A - Ad-<br>justment|Correction of sensor signal e.g. due to long sensor ca-<br>ble|r19|r19 Adjust S2|
|S3 Air ON evap. A -<br>Adjustment|Correction of sensor signal e.g. due to long sensor ca-<br>ble|r10|r10 Adjust S3|
|S4 Air OFF evap. A -|Correction of sensor signal e.g. due to long sensor ca-|r09|r09 Adjust S4|
|Adjustment|ble|||
|S5 Evaporator A -<br>Adjustment|Correction of sensor signal e.g. due to long sensor ca-<br>ble|r11|r11 Adjust S5|

###### **Table 39: Miscellaneous** → **Factor** **y reset**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Make new factory|With this command you save the controller’s actual<br>settings as a new basic setting (the earlier factory set-<br>tings are overwritten).|0=OFF, 1=ON|o67|o67 Make factory|
|Reset to factory set-<br>tings|Command which will revert all controller settings to<br>factory values.|0=OFF, 1=ON|z06|--- Reset factory|

### **Advanced**

**Table 40: Advanced** → **Advanced in** **j ection control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Superheat ctrl.<br>mode A|Select how to control the superheat of the evapora-<br>tor. At adaptive control the superheat reference is<br>adapted automatically to give the best utilization of<br>the evaporator surface. At load based control the su-<br>perheat reference is increased at high loads|1=Adaptive, 2=Load based|n21|n21 SH mode|
|Superheat close A|Minimum superheat limit where the valve is closing||x68|--- SH close|
|AFidentForce A|Expert setting - contact Danfoss for further informa-<br>tion||x69|--- AFidentForce|
|Superheat Kp min A|Min limit for amplification factor of PI controller ad-<br>justing the valve opening degree (expert setting)||x70|--- SH Kp min|
|Superheat Kp max A|Max limit for amplification factor of PI controller ad-<br>justing the valve opening degree (expert setting)||x71|--- SH Kp max|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Superheat Tn A|Integration time of PI controller adjusting the valve<br>opening degree (expert setting)||x72|--- SH Tn|
|S2 stabillity A|Setting of required stability of S2 gas outlet tempera-<br>ture before the superheat reference is reduced (Ex-<br>pert setting)A higher value will allow more instabillity<br>in S2 signalA lower value will allow less instabillity in<br>S2 signal||Y33|--- S2 Stability|
|S2 Std deviation|Expert injection setting - contact Danfoss for further<br>information||Y34|--- S2 Std Dev|
|Te feedback gain A|Gain factor for feedback of evaporating temperature<br>signal Te to PI controller controlling the superheat<br>(expert setting)||x73|--- Te-gain|
|Kp MTR control A|Amplification factor for modulating temperature con-<br>trol (Expert setting)||x77|--- MTR Kpfactor|
|Tn MTR control A|Integration time for modulating temperature control<br>(Expert setting)||x78|--- MTR Tn sec|
|AFident A|Expert readout - contact Danfoss for further informa-<br>tion||x79|--- AFident|
|Calculated Max OD<br>A|Calculated maximum opening degree of injection<br>valve (expert readout)||x80|--- Max OD %|
|Superheat close liq-<br>uid ctrl. A|Minimum limit of superheat where the valve is clos-<br>ing duting adaptive liquid control||x87|--- SH close Liq|
|Emergency OD day|Average opening degree of liquid line solenoid valve<br>during day operation||z01|--- EmerC OD day|
|Emergency OD<br>night|Average opening degree of liquid line solenoid valve<br>during night operation||z02|--- EmerC OD ngt|
|SH Band|Expert injection setting - contact Danfoss for further<br>information||Y28|--- SH Band|
|Injection duty cycle<br>SP|Expert setting - contact Danfoss for further informa-<br>tion||Y29|--- ThDutyCycle|
|Injection duty cycle|Expert injection setting - contact Danfoss for further<br>information||Y30|--- ActDutyCycle|
|P-gain|Expert injection setting - contact Danfoss for further<br>information||Y31|--- P - Gain|
|OD Ctrl. status|Readout showing which part of the injection function<br>that is in control of the valve opening degree|Values must be changed as per below:<br>0=Adaptive SH control<br>1=MOP<br>2=Superheat close<br>3=MTR|Y32|--- OD Status|

**Table 41: Advanced** → **Master control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Regulation condi-<br>tion A|Readout of the actual control state of the controller|0=Main switch OFF, 1=Injection start, 2=Superheat<br>ctrl., 3=Fill evap., 4=Defrost, 5=Post defrost, 6=Forced<br>closing, 7=Injection fault, 8=Emergency control,<br>9=Modulating ctrl., 10=Melt period, 11=Door open,<br>12=Case cleaning, 13=Cutout, 14=Forced cooling,<br>15=Shut down|x62|--- Reg. Cond.|
|MC Actual cutin<br>temp.|||x63|--- Cutin temp.|
|MC Actual cutout<br>temp.|||x64|--- Cutout temp.|
|MC Ther. toggle|Master control signal used for switching case load<br>ON/OFF depending on load condition|0=No action, 1=Toggle ON, 2=Toggle OFF|x81|--- TherToggle|
|MC Load request|Master control signal used to control load balance be-<br>tween multiple case controllers on the same suction<br>line||x82|--- LoadReq|
|MC Max Te offset|Requested offset to actual evporating temperature in<br>order to keep the air temperature at the actual set<br>point||x84|--- MaxTeOffset|
|MC Liquid control|Master control signal allowing switch to adaptive liq-<br>uid control|0=OFF, 1=ON|x85|--- MC Liq. Ctrl|
|MC Night setback|Master control signal for changing between day and<br>night time operation|0=OFF, 1=ON|x06|--- Night setbck|
|MC Case shutdown|Master control signal used to shut down a case for a<br>time period. During shut down there will be no alarm<br>monitoring|0=OFF, 1=ON|x17|--- Case shutdwn|
|MC Forced closing|Master control signal that will close the injection<br>valve|0=OFF, 1=ON|x07|--- Forced close|
|MC Forced cooling|Master control signal that will provide forced cooling|0=OFF, 1=ON|x08|--- Forced cool.|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|MC Defrost start|Master control signal for starting a defrost. At adap-<br>tive defrost the defrost might be skipped if the de-<br>frost is not needed|0=OFF, 1=ON|x13|--- MC def.start|
|MC Defrost state|Read out the actual state of the defrost|0=OFF, 1=ON|x14|--- DefrostState|
|MC Hold after de-<br>frost|Master control signal used for co-ordinated defrost<br>control to hold cabinets from returning to normal re-<br>frigeration after a defrost until all cabinets have termi-<br>nated defrost|0=OFF, 1=ON|x11|--- HoldAfterDef|
|MC Stop defrost|Master control signal used to prevent a defrost start in<br>a controller.|0=OFF, 1=ON|x12|--- Disable def.|
|MC Light signal|Master control signal for control of light via data com-<br>munication signal from system manager|0=OFF, 1=ON|o39|o39 Light remote|
|MC Actual dewpoint|Master control signal sending the actual measured<br>dew point from system manager to controller over<br>the network.||x03|--- Act.DewPoint|
|MC Po load factor|||x83|--- Load factor|
|MC Key/Bluetooth<br>lock|Master control signal that will lock down all Bluetooth<br>data communication and optionally also the opera-<br>tion of the display keys (depend upon selection in<br>P89 Display keyboard lock).|0=OFF, 1=ON|X33|--- BT lock|
|MC Min delta T|Required minimum delta temperature across evapo-<br>rator (S3 - Te) in order to keep the air temperature at<br>the actual set point||y04|--- Min Delta T|

### **Fault message**

In an error situation the alarm LED on the front will be on and the alarm relay will be activated (depending on priority). If you push the alarm button for 3 seconds you can see the alarm report in the display. (Alarm priorities can be changed. See the Table 35: Alarm relay priorities.) Here are the messages that may appear:

**Table 42: Fault messa** **g e**

|**Code**|**Alarm text**|**Description**|
|---|---|---|
|E01|Hardware failure|The controller has a hardware failure|
|E06|Clock lost time|Clock has lost valid time|
|E20|Pe Evap. pressure A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E24|S2 Gas outlet A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E25|S3 Air ON evap. A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E26|S4 Air OFF evap. A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E27|S5 Evaporator A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|A01|High temperature alarm A|The alarm temperature has been above the max alarm limit for a longer time period than the set alarm de-<br>lay.|
|A02|Low temperature alarm A|The alarm temperature has been below the min alarm limit for a longer time period than the set alarm de-<br>lay.|
|A04|Door open alarm|The door has been open for a too long time|
|A05|Max defrost hold time exceeded|The controller has been waiting longer time than permitted after a co-ordinated defrost.|
|A11|Refrigerant not selected|The refrigerant has not been selected hence control can not be initiated|
|A15|DI alarm 1|Alarm signal from digital input signal|
|A16|DI alarm 2|Alarm signal from digital input signal|
|A45|Main switch set OFF|The controller manin switch has been set to either Stop or Manaual control. Alternatively a digital input set<br>up for "main switch" function, has stopped control|
|A59|Case in cleaning mode|A case cleaning operation has been started on a case|
|AA2|CO2leak detected|CO2is leaking from the refrigerantion system|
|AA3|Refrigerant leak detected|Refrigerant is leaking from the refrigeration system|
|a04|Wrong IO configuration|Inputs and outputs have not been configured correctly|

 **NOTE:**

##### **Data communication**

The importance of individual alarms can be defined with a setting. The setting must be carried out in the group "Alarm destinations"

### **Operating status**

**Table 43: O** **p eratin** **g status**

|**Ctrl. State/**<br>**Code**|**Operating status**|**Description**|
|---|---|---|
||Push the info button for 3 seco<br>following meanings:|nds to see status. If there is a status code, it will be shown on the display. The individual status codes have the|
|S0|Normal ctrl.|The controller is running normal control. There is no other control taking priority|
|S1|Hold after defrost|The controller is waiting for other controllers to terminate coordinated defrost|
|S2|Min ON timer|The compressor is restricted from stopping until the minimum ON timer expires|
|S3|Min OFF timer|The compressor is restricted from starting until the minimum OFF timer expires|
|S4|Drip off|The defrost has terminated and the controller is waiting for drip delay to expire, while the water is dripping off the<br>evaporator|
|S10|Main switch OFF|The controller has been stopped because the parameter r12 Main switch has been set in OFF or Service position or<br>the controller has been stopped via Main switch function on DI input|
|S11|Thermostat cut-out|The air temperature has reached the thermostat cut-out value|
|S12|Frost protection S4|The air off temperature is below the minimum S4 frost limit (r98, S4 frost protection)|
|S14|Defrost|The controller is running a defrost cycle|
|S15|Fan delay|The evaporator fans are waiting to start after a defrost cycle (d07, Fan start delay and d08, Fan start temperature)|
|S16|Forced closing|The injection valve has been forced closed via a signal on a digital input or from the system manager (compressor<br>pack is restricted from starting)|
|S17|Door open|DI signal indicates that the cold room door is open|
|S18|Melt period|The controller has stopped refrigeration for a short while to turn ice crystals into water and thereby improve air<br>flow through the evaporator|
|S19|Modulating temp. control|The air temperature is controlled close to the set point via a modulating temperature control|
|S20|Emergency control<sup>**(1)**</sup>|The air temperature is controlled according to an emergency procedure due to sensor error (Pe, S2, S3 or S4)|
|S23|Adaptive superheat control|The superheat of the evaporator is optimized|
|S24|Start injection|The liquid injection into the evaporator has started|
|S25|Manual control|Main switch has been set in Service position for manual control of outputs|
|S26|No refrigerant selected|The refrigerant type has not been selected (parameter o30 Refrigerant)|
|S29|Case cleaning|A case cleaning operation has been initiated via parameter o46 Case cleaning mode or via a signal on a digital<br>input or via the AK-CC55 Connect app|
|S30|Forced cooling|The thermostat has been overruled to run forced cooling via a signal on a digital input|
|S32|Power-up delay|The controller has just been powered up and the output control is waiting for the power-up delay to expire (pa-<br>rameter o01, Delay of outputs at power-up)|
|S33|Air heating|The air heater is energized in order to raise the air temperature (parameters r62, Air heater neutral zone and r63, Air<br>heater start delay)|
|S45|Shut down controller|The control has been stopped due to a digital input signal or from the system manager|
|S48|Adaptive liquid control|The superheat control is running adaptive liquid control with reduced superheat for transcritical CO2 systems with<br>ejectors. Signal is provided via digital input or from the system manager|

> **(1) Emergency control:**

- **If Pe or S2 sensor fails, the controller will operate with a safe opening degree based on normally registered opening degree during day and night operation.**

- **If S3 or S4 sensor fails, the thermostat will operate with a registered ON/OFF duty cycle during day and night operation.**

### **Product specification**

### **Technical data**

### Electrical specifications

**Table 44: Electrical s** **p ecifications**

|**Electrical data**|**Value**|
|---|---|
|Supply voltage AC [V]|115 V / 230 V, 50/60 Hz|
|Power consumption [VA]|5 VA|
|Power ON indicator|Green LED|
|Electrical cable dimensioning [mm<sup>2</sup>]|Max. 1.5 mm<sup>2</sup>multi-core cable|

### Sensor and measuring data

**Table 45: Sensor and measurin** **g data**

|**Sensor and measuring data**|**Value**|
|---|---|
|Sensor S2|Pt 1000 AKS11|
|Sensor S3, S4, S5|Pt 1000 AKS11<br>PTC 1000 EKS111<br>NTC5K EKS211<br>NTC10K EKS221 sensor|
||(All 3 must be of the same type)|
|Temperature measuring accuracy|Pt1000: -60 – 120 °C. ±0.5 K<br>PTC1000: -60 – 80 °C. ±0.5 K<br>NTC5K: -40 – 80 °C. ±1.0 K<br>NTC10K: -40 – 120 °C. ±1.0 K|
|Pt1000 sensor specification|±0.3 K at 0 °C<br>±0.005 K per degree|
|Pe measuring|AKS 32R Ratiometric pressure transmitter: 10-90%|

### Input and output relay specifications

**Table 46: In** **p ut and out** **p ut rela** **y s** **p ecifications**

|**Input and output relay specifications**|**Input/output**|**Description**|
|---|---|---|
|Digital input|DI1<br>DI2|Signal from dry contact functions<br>Requirements to contacts: Gold plating<br>Cable length must be max. 15 m<br>Use auxiliary relays when the cable is longer<br>Open loop: 12 V (SELV)<br>Contact 3.5 mA|
|Solid state output|DO1 (for AKV coil)|115V / 230 V AC<br>Max. 0.5 A (No overload protection!)<br>Max. 1 x 20 W AKV for 115 V AC<br>2 x 20 W AKV for 230 V AC<br>**Note:**2 EC coils are not supported.|
|Relays|DO2<br>DO3|115 V / 230 V AC<br>Load max.: CE. 8 (6)A|
||DO4|UL. 8A res. 3FLA 18LRA<br>Load min.: 1VA<br>Inrush: DO2 DO3 TV-5 80A|
|Analogue output/ PWM|AO1|0 / 10 V Pulse Width Modulated<br>(PWM) max. 15 mA.<br>0 – 10 V variable, max. 2 mA|

- **NOTE:**

- DO2 to DO4 are 16 A relays.

- Max. load must be observed.

- DO2 / DO3 is recommended for load with high inrush current e.g. EC Fan and LED light.

- All relays are sealed for use with flammable refrigerant like Propane R290.

- Compliance with EN 60 335-2-89: 2010 Annex BB.

### Function data

**Table 47: Function data**

|**Function data**|**Value**|
|---|---|
|Display|LED 3 digit|
|External display, AK-CC55 Compact|1 external display|
|External display connection|RJ12|
|Max. display cable length [m]|100 m|
|Data communication built-in|MODBUS|
|Clock battery backup power reserve|4 days|
|Mounting|DIN rail|

### Environmental conditions

**Table 48: Environmental conditions**

|**Environmental conditions**|**Value**|
|---|---|
|Ambient temperature range, operation|0 – 55 °C|
|Ambient temperature range, transport|-40 – 70 °C|
|Enclosure rating IP|IP20|
|Relative humidity range [%]|20 – 80%, non-condensing|
|Shocks/Vibrations|No shocks and vibrations allowed|

### Dimensions

Measurements are in mm.

*[Figurtekst: Fi g ure 52: AK-CC55 Com p act Fi g ure 53: AK-CC55 Set]*

### **Ordering**

The list contains the components that make up an AK-CC55 Compact setup. For other Danfoss products mentioned in the document, such as sensors and valves, refer to relevant product documentation.

**Table 49: Orderin** **g**

|**Type**|**Symbol**|**Function**|**Code no.**|
|---|---|---|---|
|AK-CC55 Compact||Case controller for one AKV or solenoid valve|**084B4081**|
|AK-UI55 Info||External display|**084B4077**|
|AK-UI55 Bluetooth||External display with Bluetooth operation|**084B4075**|
|AK-UI55 Set||External display with control buttons|**084B4076**|
|AK-UI55 Mounting Base|Danfoss<br>80G8236|Mounting kit for display types: AK-UI55 Set, AK-UI55 Bluetooth, AK-UI55 Info|**084B4099**|
|AK-UI cable||External display cable with RJ12 connector. 3 m|**084B4078**|
|AK-UI cable||External display cable with RJ12 connector. 6 m|**084B4079**|
|MMIMYK|Danfoss<br>80G8284|Gateway between AK-CC55 and PC installed with KoolProg software|**080G0073**|

### **Certificates, declarations, and approvals**

The list contains all certificates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

Some approvals may change over time. You can check the most current status at danfoss.com or contact your local Danfoss representative if you have any questions.

**Table 50: Controller**

|**Control**|**Certification**|**Mark**|**Country**|
|---|---|---|---|
|Compact|EMC/LVD/RoHS|CE|EU|
|Compact|UL recognized|cURus|NAM (US and Canada)|
|Compact|ACMA (EMC)|RCM|Australia/New Zealand|
|Compact|LVE/EMC/RoHS|EAC|Russia, Kazakhstan, Belarus|
|Compact|LVD/EMC/RoHS|UA|Ukraine|

###### **Table 51: Dis** **p la** **y module**

|**Display module**|**Certification**|**Mark**|**Country**|
|---|---|---|---|
|AK-UI55 Bluetooth|RED|CE|EU|
|AK-UI55 Bluetooth|FCC|FCC ID|USA|
|AK-UI55 Bluetooth|IC (ISED)|IC ID|Canada|
|AK-UI55 Bluetooth|CMIIT|CMITT ID|China|
|AK-UI55 Bluetooth|ACMA (EMC/Wireless)|RCM|Australia|
|AK-UI55 Bluetooth|RSM (EMC/Wireless)|RCM|New Zealand|
|AK-UI55 Bluetooth|EMC/LVD/Wireless|UA|Ukraine|
|AK-UI55 Info|EMC/LVD|UA|Ukraine|
|AK-UI55 Info|ACMA (EMC)|RCM|Australia|
|AK-UI55 Info|RSM (EMC)|RCM|New Zealand|
|AK-UI55 Info|RoHS|EAC|Russia, Kazakhstan, Belarus|
|AK-UI55 Set|EMC/LVD|UA|Ukraine|
|AK-UI55 Set|ACMA (EMC)|RCM|Australia|
|AK-UI55 Set|RSM (EMC)|RCM|New Zealand|
|AK-UI55 Set|RoHS|EAC|Russia, Kazakhstan, Belarus|

##### **Controllers/displays/option module:**

CB certificate including all deviation according to IEC 60730-1 and 2-9

##### **Relays:**

Tested according to IEC 60079-15

### **Statements for the AK -** **UI55 Bluetooth display**

##### **FCC COMPLIANCE STATEMENT**

######  **CAUTION:**

Changes or modifications not expressly approved could void your authority to use this equipment This device complies with Part 15 of the FCC Rules. Operation to the following two conditions: (1) This device may not cause harmful interference, and (2) this device must accept any interference received, including interference that may cause undesired operation.

##### **INDUSTRY CANADA STATEMENT**

This device complies with Industry Canada license-exempt RSS standard(s). Operation is subject to the following two conditions: (1) this device may not cause interference, and (2) this device must accept any interference, including interference that may cause undesired operation of the device.

Le présent appareil est conforme aux CNR d'Industrie Canada applicables aux appareils radio exempts de licence. L'exploitation est autorisée aux deux conditions suivantes : (1) l'appareil ne doit pas produire de brouillage, et (2) l'utilisateur de l'appareil doit accepter tout brouillage radioélectrique subi, même si le brouillage est susceptible d'en compromettre le fonctionnement.

### **Online support**

Danfoss offers a wide range of support along with our products, including digital product information, software, mobile apps, and expert guidance. See the possibilities below.

##### **The Danfoss Product Store**

The Danfoss Product Store is your one-stop shop for everything product related—no matter where you are in the world or what area of the cooling industry you work in. Get quick access to essential information like product specs, code numbers, technical documentation, certifications, accessories, and more.

Start browsing at store.danfoss.com.

##### **Find technical documentation**

Find the technical documentation you need to get your project up and running. Get direct access to our official collection of data sheets, certificates and declarations, manuals and guides, 3D models and drawings, case stories, brochures, and much more.

Start searching now at www.danfoss.com/en/service-and-support/documentation.

##### **Get local information and support**

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest regional news, or connect with a nearby expert—all in your own language.

Find your local Danfoss website here: www.danfoss.com/en/choose-region.

##### **AK-CC55 Connect**

Make service easy with the free AK-CC55 Connect app. Via a Danfoss Bluetooth display you can connect to an AK-CC55 case controller and get a visual overview of the display functions. The app ensures smooth interaction with a Danfoss AK-CC55 case controller in a user-friendly design.

Download the a pp here:

Play Store

App Store
