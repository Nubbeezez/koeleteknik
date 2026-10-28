# Danfoss AK-CC55 Multi Coil – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Case/room controller (EEV) Type AK-CC55 Multi Coil

*Kilde: Danfoss-dokument BC365022028193en-000201.pdf*

#### **User Guide**

Case/room controller (EEV) Type **AK-CC55 Multi Coil**

**SW Ver. 1.9x** For refrigeration appliances and cold storage rooms.

|**Contents**||
|---|---|
|**Introduction**|**5**|
|**Portfolio overview**|**6**|
|Function overview|6|
|Connectivity|7|
|Data communication|7|
|AK-CC55 Multi Coil|8|
|External display|8|
|**Controller functionality**|**9**|
|Functions|9|
|Injection control|9|
|Adaptive superheat control|9|
|Adaptive liquid control|9|
|Temperature control|10|
|Temperature monitoring|10|
|Thermostat bands|11|
|Night setback of thermostat value|11|
|Temperature sensor types|11|
|Appliance cleaning|12|
|Appliance shutdown|13|
|Defrost|13|
|Electrical defrosting|13|
|Natural defrost|13|
|Start of defrost|13|
|Stop of defrost|14|
|Defrost sequence|14|
|Real-time clock|15|
|Coordinated defrost|15|
|Melt function|15|
|Rail heat|15|
|Fan pulse control|16|
|Light function|17|
|Night blind|17|
|Humidity control|17|
|Heating function (application 4 only)|19|

|Digital inputs|19|
|---|---|
|Forced closing|20|
|Door contact|20|
|Display|20|
|Override|21|
|**Applications**|**22**|
|AK-CC55 connections and application options|22|
|Application set-ups and IO connections|23|
|Product identification|25|
|AK-CC55 Multi Coil connections|25|
|Data communication|25|
|AKV info|26|
|External solid state relay for rail heat|26|
|AKS 32R info|26|
|Coordinated defrost via cable connections|27|
|External display AK-UI55|27|
|Connections|27|
|**Operation**|**29**|
|Operation via data communication|29|
|Direct operation|29|
|Operation via AK-UI55 Set|29|
|Parameter groups when operating via display|31|
|Get a good start|31|
|**AK-UI55 display menu (SW ver. 1.9x)**|**33**|
|Thermostat|33|
|Alarm settings|33|
|Defrost|34|
|Injection control|34|
|Fan control|34|
|Defrost schedule|34|
|Humidity control|35|
|Miscellaneous|35|
|Control|37|
|DO config and manual|37|
|Service|38|
|**Operation via AK-UI55 Bluetooth**|**40**|

|**AK-CC55 connect menu (SW ver. 1.9x)**|**41**|
|---|---|
|Start / Stop|41|
|Configuration|41|
|Thermostat control|43|
|Alarm limits and delays|44|
|Humidity control|46|
|Injection control|47|
|Defrost control|48|
|Defrost schedules|50|
|Fan control|51|
|Railheat control|52|
|Light/Cleaning control|53|
|Display control|53|
|Alarm relay priorities|54|
|Miscellaneous|55|
|Advanced|55|
|Fault message|58|
|**Operating status**|**60**|
|**Product specification**|**61**|
|Technical data|61|
|Electrical specifications|61|
|Sensor and measuring data|61|
|Input and output relay specifications|61|
|Function data|62|
|Environmental conditions|62|
|Dimensions|62|
|**Ordering**|**63**|
|**Certificates, declarations, and approvals**|**64**|
|Statements for the AK-UI55 Bluetooth display|65|
|**Online support**|**66**|

### **Introduction**

##### **Application**

Complete refrigeration appliance control with great flexibility to adapt to refrigeration appliances and cold storage rooms.

##### **Advantages:**

- Universal controller for control of up to 3 AKV valves in same refrigeration section

- Quick set-up with predefined settings

- Easy configuration and service using a mobile app with Bluetooth

- Energy optimization of the whole refrigeration appliance

- Adaptive Minimum Stable Superheat (MSS) control is performed with lowest possible superheat

- Allows the suction pressure to be raised several degrees

- Adaptive Liquid Control (ALC) can be performed with superheat down to 0 degrees on transcritical CO2 systems with liquid ejectors

##### **Principle**

The temperature in the appliance is registered by one to three S4 air temperature sensors which can be located in the air flow of the evaporator. A setting for display read-out determines, if thermostat A temperature, the average S4 temperature or the highest S4 temperature is read out in the display.

If two displays are connected, it can be selected to read-out thermostat A temperature in display 1 and thermostat B temperature in display 2.

The temperature of the evaporator is registered with one or two S5 sensors which can be used as a defrosting sensor.

In addition to the outputs of the electronic AKV injection valves, the controller has relay outputs which are defined by the application setting.

###### **Fi** **g ure 1: AK-CC55 with eva** **p orator, AKV valve and sensor** **p ositions**

*[Figurtekst: S4/S4B/S4C · S2/S2B/S2C P · S5/S5 B · AKV]*

**Hint:** On cold rooms the S4 sensor can be placed at the air inlet of the evaporator.

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

The controller has built-in MODBUS data communication. If there is a requirement for a different form of data communication, a Lon RS 485 module can be inserted in the controller.

The connection must then be to the module.

###### **Fi** **g ure 3: Mountin** **g of communication module**

### **AK -** **CC55 Multi Coil**

**AK-CC55 Multi Coil** – Controlling up to 3 AKV valves.

An application mode setting will configure inputs and outputs for the desired use. There are five applications to choose from.

Standard enclosure. Typically used for display cases where the controller is mounted in a tray. The standard enclosure can be expanded with one or two external displays.

### **External display**

There are three versions available with different functions:

- AK-UI55 Info: Temperature display.

- AK-UI55 Set: Temperature display with control buttons on the front.

- AK-UI55 Bluetooth: Temperature display with Bluetooth communication, for use with AK-CC55 Connect Mobile app.

**Figure 4: AK-UI55 Info**

**Figure 5: AK-UI55 Set**

**Figure 6: AK-UI55 Bluetooth**

### **Controller functionality**

### **Functions**

- Day/night thermostat with ON/OFF or modulating principle

- Switch between thermostat settings via digital input

- Adaptive control of superheat

- Adaptive liquid control

- Start of defrost via schedule, digital input, network or setting display

- Natural or electric defrost

- Stop of defrost on time and/or temperature

- Coordination of defrosting among several controllers in a line-up

- Pulsing of fans when thermostat is satisfied

- Appliance cleaning function for documentation of HACCP procedure

- Rail heat control via day/night load or dewpoint

- Humidity control in cold storage rooms

- Door function

- Control of night blinds

- Light control

- Heat thermostat

- High accuracy inputs will guarantee a better measuring accuracy than stated in the standard EN ISO 23953-2 without subsequent calibration (Pt 1000 ohm sensor)

- Support of user defined temp. sensor type

- Integrated MODBUS communication with the option of mounting a LonWorks communication card

### **Injection control**

### Adaptive superheat control

Liquid injection in the evaporator is controlled by an electronic injection valve of the type AKV. The valve operates as both expansion valve and solenoid valve. The controller opens and closes the valve based on sensor readings.

###### **Fi** **g ure 7: Ada** **p tive su** **p erheat control with AKV valve**

*[Figurtekst: pe · S2 · AKV Danfoss 84B2732]*

The superheat is measured via a pressure sensor Pe and temperature sensor S2. By using a pressure sensor, and temperature sensor a correct measurement of superheat is achieved under all conditions which ensures a very robust and precise control. The signal from one pressure transmitter can be shared by max. 10 controllers, but only if there is no significant pressure difference between the evaporators in question.

The function contains an adaptive algorithm which independently adjusts the valve’s opening so that the evaporator constantly supplies optimum amount of refrigerant.

### Adaptive liquid control

Adaptive liquid control is used in trans-critical CO2 ejector systems, which allow liquid flow. When adaptive liquid control is initiated, the superheat of the evaporator will be minimized so that a controlled amount of liquid is present at the outlet of the evaporator.

This type of control requires that the controller receives an on/off signal from (for example) a suction accumulator in the suction line.

###### **Fi** **g ure 8: Ada** **p tive li** **q uid control with AKV valve**

A level switch in the tank will register when the liquid level exceeds the max. level. When this happens, the controller will switch to dry expansion, and then back to liquid control when the liquid level has dropped. The function is defined in setting o02, o37 or o84.

The function can also be activated via data communication from a system unit. If the adaptive liquid control signal is lost, the controller will automatically switch back to dry expansion.

######  **WARNING:**

Accidental actuation may allow liquid throughput to the compressor. It is the installer’s responsibility to ensure that signal loss to the controller will not result in liquid throughput to the compressor. Danfoss accepts no responsibility for damage resulting from inadequate installation.

### **Temperature control**

The temperature in the appliance is registered by one up to three S4 air temperature sensors.

The actual temperature control can take place in three ways (same thermostat set point used for all evaporators):

1. As an ON/OFF regulation with a differential using the individual S4 sensor per evaporator. 2. As a modulating control, using the individual S4 sensor per evaporator.

3. As one ON/OFF thermostat common for all evaporators. It can be selected to use:

- the S4A air temperature sensor,

- the average of all S4 air temperature sensors,

- the highest value of all S4 air temperature sensors for the common thermostat.

There is, however, a limit to the use of a modulating control as it can only be used in remote cabinets. It is not recommended to use modulating thermostat control in low temperature applications. In applications with one evaporator and one compressor the thermostat function with ON/OFF control should be selected. In remote cabinets, the thermostat function may either be selected for ON/OFF control or modulating control.

**Table 3: Control methods**

*[Figurtekst: ON/OFF control Modulating control]*

### **Temperature monitoring**

The individual S4A, S4B and S4C air sensors are always used for temperature alarm monitoring independent of which sensor is defined as thermostat sensor. Common settings for High temperature limit, Low temperature limit and alarm delays are used for all 3 sensors, and alarms are generated for each individual evaporator section. A longer time delay can be set for high temperature alarm. This time delay is active for pull-down after defrosting, appliance cleaning and start-up.

### **Thermostat bands**

Thermostat bands can be used beneficially for appliances where different product types are stored, which requires different temperature conditions. It is possible to change between the two different thermostat bands via a contact signal on a digital input. Separate thermostat and alarm limits can be set for each thermostat band.

For the defrost control, separate defrost stop temperature and max. defrost time can be set for each thermostat band.

**Fi** **g ure 9: Thermostat band function with two different band settings**

### **Night setback of thermostat value**

In refrigeration appliances there may be big load differences between the shop’s opening and closing hours, especially if night lids/blinds are used. The thermostat reference may be raised here without it having any effect on the product temperature.

Change-over between day and night operation can take place as follows:

- via an external switch connected to a digital input

- via a signal from the data communication system

###### **Fi** **g ure 10: Thermostat band function with Ni** **g ht setback**

### Temperature sensor types

The S2 sensors always have to be Pt1000 sensors due to the high measuring accuracy.

For the S4 and S5 sensors, the user can select between the following sensor types: 0=Pt1000 (Danfoss AKS 11) 1=PTC1000 (Danfoss EKS 111) 2=NTC 5k (Danfoss EKS 211) 3=NTC 10k (Danfoss EKS 221)

4 = User-defined

If “User-defined” is selected, three sensor measuring points must be provided and based on these three sensor points, a sensor characteristic is generated.

A sensor point is defined by setting a temperature value and the corresponding resistance value at this temperature. The resistance value is set via two values for kohm and ohm respectively. These values can be found in the data sheet for the sensor.

The three sensor points must be:

1. Lowest temperature in wanted measuring range 2. Highest temperature value in wanted temperature range

3. Temp. value in the middle where a high measuring accuracy is required

A sensor error is detected at temperature values below/above the min./max. temperature values typed in for the sensor points.

###### **Fi** **g ure 11: Exam** **p le of sensor** **p oints from a NTC sensor**

*[Figurtekst: y x Temp [°C] · 350 y R [kohm] · A Sensor point (-30 °C, 180 kΩ) · 300 · 250 · 200 · A · 150 · 100 · 50 · 0 x · -40 -20 0 20 40 60 80]*

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

|-<br>+|+<br>°C|
|---|---|
|1<br>÷|+<br>Fan|
|2<br>÷|÷<br>Off|
|3<br>+|+<br>°C|

### **Appliance shutdown**

The function closes the AKV valve and all outputs are switched off. The cooling appliance is stopped like the “Main switch”, but this happens without an “A45 standby alarm”. The function can be enabled by a switch on the DI input or via a setting through data communication.

### **Defrost**

Depending on the application, you may choose between the following defrost methods: Natural: Here the fans are kept operating during the defrost Electric: The heating element is activated

### Electrical defrosting

At electrical defrost, an electrical heater is placed in front of the evaporator and the fan will “pull” the hot air through the evaporator during defrosting.

**Fi** **g ure 12: Electrical defrostin** **g**

### Natural defrost

At natural defrost, the ice is melted by running the fans and thereby circulating warm air through the evaporator.

###### **Fi** **g ure 13: Natural defrost**

### **Start of defrost**

A defrost can be started in different ways:

##### **Interval:**

Defrost is started at fixed time intervals like e.g. every eighth hour. An interval must ALWAYS be set to a "higher" value than the period set between two defrostings when a schedule or network signal is used.

##### **Week schedule:**

Here defrost can be started at fixed times of the day and night. However, max. 6 defrosts per day.

##### **Contact:**

Defrost is started with a contact signal on a digital input.

###### **Fi** **g ure 14: Defrost start**

##### **Network:**

The defrost start signal is received from a system manager via data communication.

##### **Max. thermostat runtime:**

When the aggregate time has passed a preset value, a defrost will be initiated.

##### **Manual:**

An extra defrost can be activated from the defrost button on the AK-UI55 Set display or via a parameter setting. All the mentioned methods can be used in parallel – if just one of them is activated, a defrost will be started.

### **Stop of defrost**

Defrosting can be stopped by either:

- Time

- S4 temperature (with time as safety)

- S5 temperature (with time as safety)

When the selected defrost stop sensor reaches the set defrost stop limit, the defrost is terminated. If the defrost stop sensor does not reach the set defrost stop limit within the set max. defrost time, the defrost will be terminated on time.

### **Defrost sequence**

When a defrost is initiated, the controller will run through the following sequence:

1. **Pump down:** where the evaporator is emptied of refrigerant 2. **Defrost:** where the ice on the evaporator is melted

3. **Hold after defrosting:** where multiple controllers wait for each other (coordinated defrost)

4. **Drip off:** where remaining water is dripping off evaporator

5. **Fan delay:** where the fans are restarted when the remaining water on the evaporator has turned into ice

###### **Fi** **g ure 15: Electrical defrost se** **q uence**

*[Figurtekst: x Time · A Pump down · AKV B Defrost · C Hold · D Drip · E Fan delay · X · A B C D E]*

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

###### **Fi** **g ure 16: Coordinated defrost o** **p tions**

*[Figurtekst: Max 10. · System manager]*

Either with wire connections between the controllers or via data communication:

##### **Wire connections**

The digital input DI2 must be configured for coordinated defrost and wiring must be connected between the relevant controllers. When one controller starts a defrost, all the other controllers will follow suit and likewise start a defrost. After the defrost, the individual controllers will move into waiting position. When all are in waiting position there will be a change-over to refrigeration.

##### **Coordination via data communication**

Here the system manager handles the coordination.

The controllers are gathered in defrosting groups and the system manager ensures that defrosting is started in the group according to a weekly schedule.

When a controller has completed defrosting, it sends a message to the system manager and then goes into a waiting position. When every controller in the group is in a waiting position, refrigeration is again permitted in all the individual controllers.

### **Melt function**

This function will prevent the air flow in the evaporator from being reduced by frost created by uninterrupted operation for a long time.

The function is activated if the thermostat temperature has remained in the range between -5 °C and +10 °C for a longer period than the set melting interval. The refrigeration will then be stopped during the set melting period. The frost will be melted so that the air flow and hence the evaporator’s capacity will be greatly improved.

### **Rail heat**

It is possible to pulse-control the power to the rail heat in order to save energy. Pulse control can either be controlled according to day/night load or dew point.

##### **Relay or analogue output**

A relay output can be used when long cycle times are permitted. If fast pulsing is required, the AO1/PWM output can be used. The output must be connected to an external power solid state relay. The cycle time must be configured for the relay output in o43 or for analogue output in P82.

##### **Pulse control according to day and night**

Various ON periods can be set for day and night operation. A cycle time is set as well as the percentage part of the period in which the rail heat is ON.

###### **Fi** **g ure 17: Rail heat control, da** **y /ni** **g ht load**

##### **Pulse control according to dewpoint**

In order to use this function, a system manager of the type AK-SM is required which can measure ambient temperature and humidity to calculate dew point and distribute to the appliance controllers. For this the rail heat’s ON period is controlled according to the distributed dewpoint.

Two dew point values are set in the appliance control:

- One where the effect must be max. i.e. 100%. (o87)

- One where the effect must be min. (o86)

At a dewpoint which is equal to or lower than the value in 086, the effect will be the value indicated in o88. In the area between the two dew point values, the controller will manage the power to be supplied to the rail heat.

###### **Fi** **g ure 18: Rail heat control, dew** **p oint**

*[Figurtekst: 100% · o88 · o86 o87]*

##### **During defrosting**

During defrosting rail heat can be selected to be OFF, ON or run normal control as selected in setting d27.

### **Fan pulse control**

To obtain energy savings, it is possible to pulse control the power supply to the evaporator fans. Pulse control can be accomplished in one of the following ways:

- during the thermostat’s cut-out period (cold room)

- during night operation and during the thermostat’s cut-out period (appliance with night blinds)

(The function is not actual when r14=2, i.e. modulating regulation).

A period of time is set as well as the percentage of this period of time where the fans have to be operating.

###### **Fi** **g ure 19: Fan c** **y cle time**

##### **Cut-out of fans during plant breakdowns**

If the refrigeration in a breakdown situation stops, the temperature in the cold room may rise quickly as a result of the emission of heat from large fans. In order to prevent this situation, the controller can stop the fans if the temperature at S5 exceeds a set limit value. The fans will start running again when the S5 temperature has dropped 2K below the set limit. (The function can also be used as a type of MOP function. Here the load on the compressors is limited until the S5 temperature has fallen below the configured value).

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

Motorised night blinds can be controlled automatically from the controller via the NO connector on the light relay. The night blinds will follow the status of the light function. When the light is switched on, the night blinds open, and when the light is switched off, the night blinds close again. When the night blinds are closed, it is possible to open them using a switch signal on the digital input. If this pulse signal is activated, the night blinds will open and the refrigeration appliance can be filled with new products. If the pulse signal is activated again, the blinds close.

A night blind is opened when the appliance cleaning function is activated.

A setting can define that the night blind is opened when "r12" (Main switch) is set to off (see o98).

When the night blind rolls down, the fan will be stopped for the set time. The night blind can thereby roll down to the correct position.

### **Humidity control**

In application 4 when setup for room control it is possible to define if humidity control should be done via a humidifier or a dehumidifier.

When humidity control is enabled, the second display will read out the actual humidity.

The controller measures the humidity via a 0 – 10 V signal from a humidity sensor and by means of a DO relay it can activate a humidifier or a de-humidifier.

High and low humidity alarm limits can be set to generate a humidity alarm.

Humidity control is disabled when main switch is OFF, at manual control, at case shutdown, at forced closing mode, at door open, if cooling is stopped, at humidity sensor error and at case cleaning.

It is possible to define whether humidity control is enabled during defrost or not.

###### **Fi** **g ure 20: Humidit** **y control**

*[Figurtekst: y x Time · y Temperature · A A Humidity max temp. difference · B Humidity min temp. difference · B C Humidity control enabled · x · C]*

A Max and Min temperature range can be defined wherein the humidity control is enabled. Upper and lower differential is fixed at 1K.

**Fi** **g ure 21: Humidifier control**

*[Figurtekst: y x Time · 100% y Humidity · A Humidity difference · SP Setpoint · A · B Humidifier · SP · x · B]*

If the humidity gets below the SP, then humidification is started via a DO signal to a humidifier.

If the humidity increases to SP + humidity differential, then humidification is stopped.

*[Figurtekst: Fi g ure 22: Dehumidifier control · y x Time · 100% · y Humidity · SP Setpoint · SP · A Humidity difference · A · B Dehumidifier · x · B]*

If the humidity rises above the SP, then dehumidification is started via a DO signal to a dehumidifier.

If the humidity drops below the SP – Humidity differential, then dehumidification is stopped.

### **Heating function (application 4 only)**

The heating function is used to prevent the temperature from becoming too low, e.g. in a cold room, etc. The limit for when the heating function cuts off is set as an offset value below the current cut-out limit for the refrigeration thermostat. This ensures that refrigeration and heating do not occur simultaneously. The difference for the heating thermostat has the same value as for the refrigeration thermostat. To prevent that the heating thermostat cuts in during short-term drops in air temperature, a time delay can be set for when to change from refrigeration to heating.

**Fi** **g ure 23: Heatin** **g function**

*[Figurtekst: º C A Refrigeration · t · B Neutral zone · C Heat · A r01 · B r62 · C r01]*

### **Digital inputs**

There are two digital inputs, DI1 and DI2, with dry contact function, and one digital input DI3 with high voltage signal.

They can be used for the following functions:

**Table 5: Function table and DI settin** **g s**

||**I**|**nput / Settings men**|**u**||
|---|---|---|---|---|
|**Function**|**DI1**|**DI2**|**DI3**|**Setting**|
||**o02**|**o37**|**o84**||
|None|+|+|+|0|
|DI Status|+|+|+|1|
|Door function|+|+|+|2|
|Door alarm|+|+|+|3|

||**I**|**nput / Settings men**|**u**||
|---|---|---|---|---|
|**Function**|**DI1**|**DI2**|**DI3**|**Setting**|
||**o02**|**o37**|**o84**||
|Defrost start|+|+|+|4|
|Main switch|+|+|+|5|
|Night setback|+|+|+|6|
|Thermostat band|+|+|+|7|
|Alarm at closed|+|+||8|
|Alarm at open|+|+||9|
|Case cleaning|+|+|+|10|
|Forced cooling|+|+|+|11|
|Open blinds|+|+|+|12|
|Coordinated defrost||+||13|
|Forced closing|+|+|+|14|
|Shutdown|+|+|+|15|
|Light control|+|+|+|16|
|Leak detection|+|+|+|20|
|Adaptive liquid control|+|+|+|21|
|Door fan stop|+|+|+|29|

Example: If DI1 is to be used to start a defrost, o02 must be set to 4.

### **Forced closing**

The AKV valves can be closed with an external signal ("Forced closing").

The function must be used in connection with the compressor’s safety circuit, so that there will be no injection of liquid into the evaporator when the compressor is stopped by the safety controls and cannot start again (however not at low pressure – LP).

Via a setting (see o90 Fan at forced closing) it is possible to define whether the fan should be ON or OFF during forced closing and whether an ongoing defrost is suppressed (i.e. put in standby position for a period of up 10 minutes before it is cancelled) - this feature can be used in CO2 systems to eliminate excessive heating while compressors cannot run.

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

The controller has one or two plugs for an external display. One of the following display types can be connected to a plug:

- AK-UI55 Info (temperature display)

- AK-UI55 Set (temperature display and operation)

- AK-UI55 Bluetooth (temperature display and app interface)

The connection between the display and the controller must be made using an AK-UI55 cable. The distance between the controller and the display must not exceed 100 m.

If there are two external displays, it will be the sum of the two distances that cannot exceed 100 m.

###### **Fi** **g ure 24: Controller with two dis** **p la** **y s**

### **Override**

The controller contains a number of override functions which can be used together with Master Control functions in the Danfoss gateway/system manager:

**Table 6: Override functionalit** **y**

|**Master control function**|**Description**|
|---|---|
|MC Ther. toggle|Master control signal used for switching case load ON/OFF depending on the load condition|
|MC Load request|Master control signal used to control the load balance between multiple case controllers on the same suction line|
|MC Max. Te offset|Requested offset to actual evaporating temperature in order to keep the air temperature at the actual setpoint|
|MC Liquid control|Master control signal allowing switch to adaptive liquid control|
|MC Night setback|Master control signal for changing between day and night time operation|
|MC Case shutdown|Master control signal used to shut down a case for a time period. During shutdown there will be no alarm monitoring|
|MC Forced closing|Master control signal that will close the injection valve|
|MC Forced cooling|Master control signal that will provide forced cooling|
|MC Defrost start|Master control signal for starting a defrost. At adaptive defrost the defrost might be skipped if the defrost is not needed|
|MC Defrost state|Read out the actual state of the defrost|
|MC Hold after defrost|Master control signal used for co-ordinated defrost control to hold cabinets from returning to normal refrigeration after a defrost<br>until all cabinets have terminated defrost.|
|MC Stop defrost|Master control signal used to prevent a defrost start in a controller.|
|MC Light signal|Master control signal for control of light via a data communication signal from the system manager.|
|MC Actual dewpoint|Master control signal sending the actual measured dewpoint from the system manager to the controller over the network.|
|MC Key/Bluetooth lock|Master control signal that will lock down all Bluetooth data communication and optionally also lock the display keyboard (parame-<br>ter P89)|

### **Applications**

The chapter outlines application examples:

- 1-3: Control of one, two and three evaporators

- 4: Control of high temperature cold rooms with two evaporators

- 5: Control of low temperature cold rooms with two evaporators

An application setting will configure inputs and outputs so that the controller’s operation interface is reflecting the selected application.

*[Figurtekst: Figure 25: Standard display case, upright or normal, with Figure 26: Cold room configuration with door, light and · one eva p orator heat control function · S₄ · S₄ (S4) S5 S4 · S₅ · S₂ · S₅ · (S4) Hint: On cold rooms the S4 sensor can be placed · at the air inlet of the evaporator.]*

### **AK -** **CC55 connections and application options**

Upper and lower connection labels are laid out as shown in figure:

**Fi** **g ure 27: Electrical connections AK-CC55 Multi Coil**

*[Figurtekst: 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 60 61 70 71 83 84 85 · 5V s AI2 AI3 AI4 AI5 AI6 (1) DI1/ DI2 AO1 B - A + · AI1 AI7 (1) PWM MODBUS · 115 – 230 V AC AKV DO2 DO3 DO4 DO5 DO6 DO7 DI3 · L N 115 – 230 V AC · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 30 31]*

- (1) See Table 8

- Max. 0.5 A - No overload protection!

AK-CC55 Multi Coil is optimised for control of one to three expansion valve + different combinations of light, rail heat and alarm relays. It has 7 Digital Outputs (DO), known as DO1 – DO7, one Analogue Output (AO), known as AO1, 6 Analogue Inputs (AI), known as AI1 – AI6, an input that can be used as either DI1 (Digital Input) or AI7 (Sensor Input), and 2 Digital Inputs, known as DI2 - DI3.

**Table 7: The controller covers the followin** **g five a** **pp lications:**

**Application 1-3** Control of one, two and three evaporators. **Application 4** Control of high temperature cold rooms with two evaporators. **Application 5** Control of low temperature cold rooms with two evaporators.

**Table 8: AK-CC55 Multi Coil A** **pp lication with Di** **g ital and Analo** **g ue out** **p ut s** **p ecification**

|**No.**|**Application description**|**DO1**|**DO2**|**DO3**|**DO4**|**DO5**|**DO6**|**DO7**|**AO1**|
|---|---|---|---|---|---|---|---|---|---|
|1|1 evaporator|A|||A|||||
|2|2 evaporators|A||B|A|||B||
|3|3 evaporators|A||B||||C||
|4|Cold room|A||B||||||
|5|Cold room|A||B|A|||B||

**Table 9: Sensor descri** **p tion**

|Pe|Evaporating pressure|
|---|---|
|S2 A, B or C|Gas outlet of evaporator A, B or C|
|S4<sup>**(1)**</sup>A, B or C|Discharge air temperature A, B or C|
|S5 A or B|Evaporator temperature A or B|
|RH%|Relative humidity sensor|

> **(1) On cold room applications the S4 sensor can be placed at return air.**

**Table 10: AK-CC55 Multi Coil A** **pp lication with Di** **g ital and Analo** **g ue in** **p ut s** **p ecification**

|**No.**|**Application description**|**AI1**|**AI2**|**AI3**|**AI4**|**AI5**|**AI6**|**AI7/DI1**|**DI2**|**DI3**|
|---|---|---|---|---|---|---|---|---|---|---|
|1|1 evaporator|Pe|S2A|S4A|S5A||||||
|2|2 evaporators|Pe|S2A|S4A|S5A|S2B|S4B|S5B|||
|3|3 evaporators|Pe|S2A|S4A|S5B|S4B|S2C|S4C|||
|4|Cold room|Pe|S2A|S4A|S5B|S4B|RH%||||
|5|Cold room|Pe|S2A|S4A|S5B|S2B|S4B|S5B|||

= Optional use

### **Application set -** **ups and IO connections**

###### **Fi** **g ure 28: Connections for a** **pp lication 1**

*[Figurtekst: P · 1 3 2 · 1 · 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 60 61 70 71 83 84 85 · 5V s S2A S4A S5A DI1 DI2 AO1 B - A + · Pe PWM MODBUS · 115 – 230 V AC AKV  A Alarm Railheat Defrost Light Fan DI3 · L N 115 – 230 V AC · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 30 31 · 0 – 10 V/ PWM]*

###### **Fi** **g ure 29: Connections for a** **pp lication 2**

*[Figurtekst: P · 1 3 2 · 2 · 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 60 61 70 71 83 84 85 · 5V s S2A S4A S5A S2B S4B S5B DI2 AO1 B - A + · Pe PWM MODBUS · 115 – 230 V AC AKV  A Railheat AKV  B Defrost A Light Fan Defrost B DI3 · L N 115 – 230 V AC · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 30 31 · A B A B · Fi g ure 30: Connections for a pp lication 3 · P · 1 3 2 · 3 · 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 60 61 70 71 83 84 85 · 5V s S2A S4A S2B S4B S2C S4C DI2 AO1 B - A + · Pe PWM MODBUS · 115 – 230 V AC AKV  A Alarm AKV  B Railheat Light Fan AKV  C DI3 · L N 115 – 230 V AC · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 30 31 · A B C · Fi g ure 31: Connections for a pp lication 4 · P U · 1 3 2 RH · 0-10 · 4 · 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 60 61 70 71 83 84 85 · 5V s S2A S4A S2B S4B RH% DI1 DI2 AO1 B - A + · Pe PWM MODBUS · 115 – 230 V AC AKV  A Alarm AKV  B Humidity Light Fan Heat DI3 · L N 115 – 230 V AC · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 30 31 · A B · 0 – 10 V/ PWM · 0 – 10 V/ PWM · 0 – 10 V/ PWM]*

###### **Fi** **g ure 32: Connections for a** **pp lication 5**

*[Figurtekst: P · 1 3 2 · 5 · 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 60 61 70 71 83 84 85 · 5V s S2A S4A S5A S2B S4B S5B DI2 AO1 B - A + · Pe PWM MODBUS · 115 – 230 V AC AKV  A Alarm AKV  B Defrost A Light Fan Defrost B DI3 · L N 115 – 230 V AC · 1 2 3 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 30 31 · A B A B · 0 – 10 V/ PWM]*

### **Product identif i** **cation**

The controller is provided with labels from the factory, indicating a generic application. When selecting the required application, specific labels are provided so that you can mount the relevant one.

The application number is indicated on the left-hand side of the labels. Use the label fitting the selected application.

Some of the labels can be applicable to multiple application options.

###### **Fi** **g ure 33: Product identification**

*[Figurtekst: Danfoss 84B3232.11A]*

**AK -** **CC55 Multi Coil connections**

### Data communication

###### **Fi** **g ure 34: Data communication**

 **IMPORTANT:**

It is important that the installation of the data communication cable is performed correctly with sufficient distance to high voltage cables.

### AKV info

*[Figurtekst: Fi g ure 35: AKV A info Fi g ure 36: AKV B info · AKV DO3 · 8 9 13 14 · 230 V AC (115 AC) 230 V AC (115 AC) · 230 V or 115 V · 230 V or 115 V AC coil · AC coil Max. 0.5 A · Max. 0.5 A Not overload protected · Danfoss 84B8285 Danfoss 84B8286]*

*[Figurtekst: Fi g ure 37: AKV C info · DO7 · 23 24 · 230 V AC (115 AC) · 230 V or 115 V · AC coil · Max. 0.5 A · Not overload protected]*

### External solid state relay for rail heat

**Fi** **g ure 38: External solid state rela** **y for rail heat**

*[Figurtekst: SSR · 60 61 70 71 · AO1/ · PWM]*

0 / 10 V Pulse Width Modulated (PWM) Max. 15 mA.

AKS 32R info

*[Figurtekst: Fi g ure 39: AKS 32R info · AKS 32R · out · A B C]*

*[Figurtekst: AKS 32R A Black · out · B Brown · C Blue · A B C]*

 **NOTE:**

A ratiometric pressure transmitter with a 5 V, 10 – 90% voltage output signal must be used.

The signal from one pressure transmitter can be received by up to 10 controllers. There must not be a significant pressure drop from the pressure transmitter's position in the suction line to the individual evaporators.

### Coordinated defrost via cable connections

**Fi** **g ure 40: Coordinated defrost via cable connections**

Max. 10

The following controllers can be connected in this way: EKC 204A, AK-CC 210, AK-CC 250, AK-CC 450, AK-CC 550 and AK-CC55.

Refrigeration is resumed at the same time when all controllers have terminated defrost.

### External display AK-UI55

**Fi** **g ure 41: External dis** **p la** **y AK-UI55**

(Total length: max. 100 m)

### Connections

**Table 11: Connection details**

|**AI1**|**Pressure transmitter**<br>AKS 32R<br>Connect to terminal 40, 41 and 42.<br>(Use cable 060G1034: Black=40, Brown=41, Blue=42)|
|---|---|
||The signal from one pressure transmitter can be received by up to 10 controllers. But only if there are no significant pressure drops be-<br>tween the evaporators to be controlled. SeeFigure 39: AKS 32R info.|
|**AI2 - AI7**|**Primarily for temperature inputs**<br>• S2<br>Pt 1000 ohm sensor AKS11, placed at the evaporator outlet<br>• S4, S5<br>Pt 1000 AKS11, PTC 1000 EKS111, NTC5K EKS211 or NTC10K EKS221 sensor or a user-defined sensor type. All have to be of the same<br>type.<br>• S4, discharge air sensor, placed in the cold air of the evaporator<br>• S5, defrost sensor, placed in the evaporator.<br>• RH%, 0 – 10 V signal input from Humidity sensor<br>(If the DI1 input is used for a temperature measurement, it will appear as AI7.)|
|**DI1**|**Digital input signal (dry contact)**<br>The defined function is active when the input is short-circuited or opened, depending on the function defined in o02.|
|**DI2**|**Digital input signal (dry contact)**<br>The defined function is active when the input is short-circuited or opened, depending on the function defined in o37.|
|**AO1**|**Analogue output signal**<br>• Analogue 0 – 10 V (currently not used)<br>• Pulse width modulated signal<br>Can be used for fast pulse control of rail heat via an external power solid state relay.|

|**MODBUS**|For data communication:<br>• Terminal 83 = B-<br>• Terminal 84 = A+<br>• Terminal 85 = screen|
|---|---|
|**Supply voltage**|230 V AC or 115 V AC|
|**DO1**|• AKV valve section A:<br>Connection of expansion valve type AKV, AKVA, AKVH or AKVP.<br>The coil must be a**230 V**or**115 V AC coil**|
|**DO2**|• Alarm:<br>There is a connection between terminal 10 and 12 in alarm situations and when the controller is without power.<br>DO2 has reinforced insulation that can be used with 24 V.<br>• Rail heat:<br>There is connection between terminal 10 and 11 when the function is on.|
|**DO3**(Solid State Relay)|• Rail heat, AKV valve section B:<br>There is connection between terminal 13 and 14 when the function must be active.<br>The coil must be a**230 V**or**115 V AC coil. Max. 0.5 A**|
|**DO4**|• Defrost section A, Rail heat, Humidity:<br>There is connection between terminal 15 and 16 when the function is on.|
|**DO5**|• Light:<br>There is connection between terminal 18 and 20 when the function must be active.|
|**DO6**|• Fan:<br>There is connection between terminal 21 and 22 when the fan is on.|
|**DO7**(Solid State Relay)|• Defrost section B, AKV valve section C, Heat function:<br>There is connection between terminal 23 and 24 when the function is on.<br>The coil must be a**230 V**or**115 V AC coil. Max. 0.5 A**|
|**DI3**|**Digital input signal**<br>The signal must have a voltage of 0 / 230 V AC (115 V AC). The function is defined in o84.|

##### **Display (RJ12 plug)**

If external readings/operation of the controller is required, a display can be connected. For one display the max. cable length is 100 m. For two displays the sum of the two cable lengths must not exceed 100 m.

##### **Electric noise**

Cables for sensors, low voltage DI inputs and data communication **must** be kept separate from other high voltage cables:

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

The controller can be operated in different ways depending on the user interface. The following options are available:

- Via data commmunication

- Via AK-UI55 Setting Display

- Via AK-UI55 Bluetooth display

### **Operation via data communication**

##### **Via system manager's display**

All AK-CC55 controllers can be operated from a central location, e.g. AK-SM 800. Data communication is to take place via MODBUS or Lon.

##### **Via system manager and service tool**

Operation can also be performed from a central location with PC software "Service Tool" connected to a system manager AK-SM 720 via MODBUS or Lon.

##### **Programming via KoolProg**

Programming by use of PC software type KoolProg® via interface MMIMYK connected to RJ12 display connector.

### **Direct operation**

Operation via AK-UI55 setting display

The display can be placed at a distance of up to 100 metres from the controller.

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

###### **Fi** **g ure 42: O** **p eratin** **g via AK-UI55 Set**

*[Figurtekst: B C · D · A · E · Danfoss 84B8325 F]*

- A Lights up in event of: Energy optimization, Cooling, Defrosting, Fan operation

- B Lights in event of alarm

- C Long press (3 seconds) on alarm button alarm — relay is reset — alarm code displayed — e.g. “A1”

- D Long press (3 seconds) gives access to the information menu “InF” Up arrow / Down arrow / Arrow to left: Navigation in the menu and setting of values.

- E Long press (3 seconds) will start a defrost, “-d-” is shown in the display. Ongoing defrosting can be stopped by a long press.

- F SET: Long press (3 seconds) gives access to the “SEt” menu. If the operation is locked with a password, “PS” is shown. Enter the code. Shows the setting for a chosen parameter / saves a changed setting. Short press gives access to entering of the thermostat’s cut-out limit.

**Table 12: Messa** **g es** **p rovided b** **y the dis** **p la** **y**

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

###### **Fi** **g ure 43: SET button** **p arameter list**

*[Figurtekst: SET SET button, 3 s: Configuration settings · Set · PS: Password (if any) · (PS) · cFg SET r12 Main switch · o61 Application · r-- o03 MODBUS address · A-- r89 Food type · d-- r00 Cut-out temperature · n-- o30 Refrigerant type · F-- o20 Min. transmitter range · t-- o21 Max. transmitter range · h-- d01 Defrost method · o-- d03 Defrost interval · p-- d10 Defrost sensor · q-- d04 Max. defrost time · u-- d02 Defrost stop temperature · < < · (Return) (Return) · Fi g ure 44: Info button  p arameter list · Info button, · 3 s: Information for service use · Inf · StA SET See control state message · App SET See selected application · in SET di1/ ** · AI7 · out SET do1 Akv di2 ** · buS SET MODBUS quality do2 di3 ** · SoF SET See SW version do3 AI1 PE · < do4 AI2 S2 · (Return) do5 AI3 S4 · do6 AI4 S5 · do7 AI5 ** · Output status Ao1 AI6 ** · When you want info on a relay · output, the dot will show < < · whether the relay is activated (Return) (Return) · (energized) for, e.g.: · do4 = not activated · do.4 = activated · < · < · Menu groups · See also the following pages. · < · * · * · * · * · * Read output status Read input status · * · *]*

The output's function (determined at configuration). The DOs and AOs can also be forced controlled from this menu, when r12 Main switch has been set in position "service". Forced control of a function can also be performed in codes q11 to q27.

** The input's function (determined at configuration).

StA See control state message in Table 46

### Get a good start

With the following procedure you can start regulation very quickly:

1. Open parameter r12 and stop the regulation (in a new and not previously set unit, r12 will already be set to 0 which means stopped regulation)

2. Select application based on the wiring diagrams (see Application set-ups and IO connections)

3. Open parameter o61 and set the application number

4. For network. Set the address in o03

5. Then select a set of presets from the "Food type" help table

6. Open parameter r89 and set the number for the array of presettings. The few selected settings will now be transferred to the menu

7. Set the desired cut-out temperature r00

8. Select refrigerant via parameter o30

9. Set the pressure transmitter min. and max. range via parameter o20 and o21

10. Set the desired defrost method in d01 11. Set the interval time between defrost starts in d03

12. Set the desired defrost sensor in d10 13. Set the maximum defrost time in d04 14. Set the defrost stop temperature in d02 15. Open parameter r12 and start the regulation 16. Go through the parameter list and change the factory values where needed 17. Get the controller up and running on network:

- MODBUS: Activate scan function in system unit

- If another data communication card is used in the controller:

- Lon RS485: Activate the function o04

- Ethernet: Use the MAC address

**Table 13: Food t** **yp e settin** **g s**

|**Setting of presettings (r89).**<br>**After setting 1-5, setting is returned to 0.**|**1**|**2**|**3**|**4**|**5**|
|---|---|---|---|---|---|
|**Food type**|**Vegetables**|**Milk**|**Meat/fish**|**Frozen food**|**Ice cream**|
|Temperature (r00)|8 °C|0 °C|-2 °C|-20 °C|-24 °C|
|Max. temp. setting (r02)|10 °C|4 °C|2 °C|-16 °C|-20 °C|
|Min. temp. setting (r03)|4 °C|-4 °C|-6 °C|-24 °C|-28 °C|
|Upper alarm limit (A13)|14 °C|8 °C|8 °C|-15 °C|-15 °C|
|Lower alarm limit (A14)|0 °C|-5 °C|-5 °C|-30 °C|-30 °C|

Can only be set when r12=0.

### **AK-UI55 display menu (SW ver. 1.9x)**

- R-W If the operation is protected by one or more passwords, reading and setting the parameter will be limited to: R or W

- R This setting can be seen with password no. _ or higher (3 is the highest level).

- W This setting can be performed with password no. _ or higher (3 is the highest level).

- The asterisk indicates in which application from 1-5 the parameter is applicable.

### **Thermostat**

**Table 14: Thermostat**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Cut-out 1||0-0|r00|*|*|*|*|*|r03|r02|2.0 °C|
|Differential 1||1-2|r01|*|*|*|*|*|0.1 °C|20.0 °C|2.0 °C|
|Max. cut-out limit||0-2|r02|*|*|*|*|*|r03|50.0 °C|50.0 °C|
|Min. cut-out limit||0-2|r03|*|*|*|*|*|-60.0 °C|r02|-60.0 °C|
|Temperature unit|0=Celsius, 1=Fahrenheit|1-2|r05|*|*|*|*|*|0|1|0|
|S4 Air OFF evap. A - Adjustment||1-2|r09|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|S5 Evaporator A - Adjustment||1-2|r11|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|Main switch|-1=Manual, 0=Stop, 1=Start|0-2|r12|*|*|*|*|*|-1|1|0|
|Night offset||1-2|r13|*|*|*|*|*|-50.0 °C|50.0 °C|0.0 °C|
|Thermostat mode|1=ON/OFF, 2=Modulating,<br>3=ON/OFF Common|1-2|r14|*|*|*|*|*|1|3|1|
|Melt interval||1-2|r16|*|*|*|*|*|0 hours|10 hours|1 hour|
|Melt period||1-2|r17|*|*|*|*|*|0 min|30 min|5 min|
|S2 Gas outlet A - Adjustment||1-2|r19|*|*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|Cut-out 2||0-2|r21|*|*|*|*|*|-60.0 °C|50.0 °C|2.0 °C|
|Air heater neutral zone||1-2|r62||||*||0.0 °C|50.0 °C|5.0 °C|
|Air heater start delay||1-2|r63||||*||0 min|240 min|240 min|
|Food type|0=None, 1=Vegetables, 2=Dairy,<br>3=Meat and fish, 4=Frozen food,<br>5=Ice cream|1-2<sup>**(1)**</sup>|r89|*|*|*|*|*|0|5|0|
|Differential 2||1-2|r93|*|*|*|*|*|0.1 °C|20.0 °C|2.0 °C|
|Thermostat sensor|1=Ther. air A, 2=Average all,<br>3=Maximum all|1-2|r99||*|*|*|*|1|3|1|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Alarm settings**

**Table 15: Alarm settin** **g s**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Alarm delay A||1-2|A03|*|*|*|*|*|0 min|240 min|30 min|
|Door open alarm delay||1-2|A04|*|*|*|*|*|0 min|240 min|60 min|
|Alarm delay pulldown A||1-2|A12|*|*|*|*|*|0 min|240 min|90 min|
|High alarm limit 1||1-2|A13|*|*|*|*|*|-60.0 °C|50.0 °C|8.0 °C|
|Low alarm limit 1||1-2|A14|*|*|*|*|*|-60.0 °C|50.0 °C|-30.0 °C|
|High alarm limit 2||1-2|A20|*|*|*|*|*|-60.0 °C|50.0 °C|8.0 °C|
|Low alarm limit 2||1-2|A21|*|*|*|*|*|-60.0 °C|50.0 °C|-30.0 °C|
|Alarm delay DI 1||1-2|A27|*|||*||0 min|240 min|30 min|
|Alarm delay DI 2||1-2|A28|*|*|*|*|*|0 min|240 min|30 min|

### **Defrost**

**Table 16: Defrost**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min.value**|**Max.value**|**Fact.value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Defrost method|0=None, 1=Electrical, 4=Air/<br>Offcycle|1-3|d01|*|*|*|*|*|0|4|1|
|Defrost stop limit A||1-2|d02|*|*|*|*|*|0.0 °C|50.0 °C|6.0 °C|
|Defrost start interval||1-2|d03|*|*|*|*|*|0 hours|240 hours|8 hours|
|Max. defrost time||1-2|d04|*|*|*|*|*|0 min|360 min|45 min|
|Time staggering power-up||1-2|d05|*|*|*|*|*|0 min|240 min|0 min|
|Drip off time||1-2|d06|*|*|*|*|*|0 min|60 min|0 min|
|Fan start delay||1-2|d07|*|*|*|*|*|0 min|60 min|0 min|
|Fan start temperature||1-2|d08|*|*|||*|-60.0 °C|10.0 °C|5.0 °C|
|Fan control during defrost|0=OFF, 1=ON, 2=OFF at drip,<br>3=OFF at high temp|1-2|d09|*|*|*|*|*|0|3|1|
|Defrost stop method|0=Time, 1=S5 sensor, 2=S4 sen-<br>sor|1-2|d10|*|*|*|*|*|0|2|0|
|Pump down delay||1-2|d16|*|*|*|*|*|0 min|60 min|0 min|
|Max. thermostat run time||1-2|d18|*|*|*|*|*|0 hours|240 hours|0 hours|
|Min. defrost time||1-2|d24|*|*|*|*|*|0 min|d04|0 min|
|Rail heat during defrost|0=OFF, 1=ON, 2=Normal control|1-2|d27|*|*|*|*|*|0|2|1|
|Defrost stop limit 2||1-2|d28|*|*|*|*|*|0.0 °C|50.0 °C|6.0 °C|
|Max. defrost time 2||1-2|d29|*|*|*|*|*|0 min|360 min|45 min|
|Display delay after defrost||1-2|d40|*|*|*|*|*|5 min|240 min|30 min|
|Fan stop temperature||1-2|d41|*|*|*|*|*|-20.0 °C|20.0 °C|0.0 °C|

### **Injection control**

**Table 17: In** **j ection control**

|**Function**<br>**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|
|Max. superheat limit|1-2|n09|*|*|*|*|*|n10|20.0 °C|12.0 °C|
|Min. superheat limit|1-2|n10|*|*|*|*|*|2.0 °C|n09|3.0 °C|
|MOP temperature|1-2|n11|*|*|*|*|*|-60.0 °C|15.0 °C|15.0 °C|
|AKV Period time|1-2<sup>**(1)**</sup>|n13|*|*|*|*|*|3 s|6 s|6 s|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Fan control**

**Table 18: Fan control**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Fan stop high S5 temp.||1-2|F04|*|*|||*|-60.0 °C|50.0 °C|50.0 °C|
|Fan pulsing mode|0=No pulsing, 1=Pulsing cut-<br>out, 2=Pulsing cut-out night|1-2|F05|*|*|*|*|*|0|2|0|
|Fan period time||1-2|F06|*|*|*|*|*|1 min|30 min|5 min|
|Fan ON cycle||1-2|F07|*|*|*|*|*|0 %|100 %|100%|

### **Defrost schedule**

**Table 19: Defrost schedule**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Defrost schedule|0=No, 1=Yes|1-2|t00|*|*|*|*|*|0|1|0|
|Def. start 1 - Hours||1-2|t01|*|*|*|*|*|0 hours|23 hours|0 hour|
|Def. start 1 - min||1-2|t11|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 2 - Hours||1-2|t02|*|*|*|*|*|0 hours|23 hours|0 hour|
|Def. start 2 - min||1-2|t12|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 3 - Hours||1-2|t03|*|*|*|*|*|0 hours|23 hours|0 hour|
|Def. start 3 - min||1-2|t13|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 4 - Hours||1-2|t04|*|*|*|*|*|0 hours|23 hours|0 hour|
|Def. start 4 - min||1-2|t14|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 5 - Hours||1-2|t05|*|*|*|*|*|0 hours|23 hours|0 hour|

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Def. start 5 - min||1-2|t15|*|*|*|*|*|0 min|59 min|0 min|
|Def. start 6 - Hours||1-2|t06|*|*|*|*|*|0 hours|23 hours|0 hour|
|Def. start 6 - min||1-2|t16|*|*|*|*|*|0 min|59 min|0 min|
|Time hours||0-1|t07|*|*|*|*|*|0 hours|23 hours|0 hour|
|Time min||0-1|t08|*|*|*|*|*|0 min|59 min|0 min|
|Time date||0-1|t45|*|*|*|*|*|1|31|1|
|Time month||0-1|t46|*|*|*|*|*|1|12|1|
|Time year||0-1|t47|*|*|*|*|*|0|100|0|
|Monday - Follow schedule|0=No, 1=Yes|1-2|t51|*|*|*|*|*|0|1|1|
|Tuesday - Follow schedule|0=No, 1=Yes|1-2|t52|*|*|*|*|*|0|1|1|
|Wednesday - Follow schedule|0=No, 1=Yes|1-2|t53|*|*|*|*|*|0|1|1|
|Thursday - Follow schedule|0=No, 1=Yes|1-2|t54|*|*|*|*|*|0|1|1|
|Friday - Follow schedule|0=No, 1=Yes|1-2|t55|*|*|*|*|*|0|1|1|
|Saturday - Follow schedule|0=No, 1=Yes|1-2|t56|*|*|*|*|*|0|1|1|
|Sunday - Follow schedule|0=No, 1=Yes|1-2|t57|*|*|*|*|*|0|1|1|

### **Humidity control**

**Table 20: Humidit** **y control**

|**Function**|**Values**|**R-W**|**Code**<br>**1**<br>**2**|**3**|**4**<br>**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|
|Humidity cut-in||0-2|h23||*|0 %|100 %|70%|
|Humidity differential||1-2|h24||*|1 %|30 %|5%|
|Humidity high alarm limit||1-2|h25||*|0 %|100 %|100%|
|Humidity low alarm limit||1-2|h26||*|0 %|100 %|0%|
|Humidity alarm delay||1-2|h27||*|0 min|240 min|60 min|
|Humidity ctrl. at defrost|0=No, 1=Yes|1-2|h28||*|0|1|0|
|Humidity sensor - Min signal||1-2<sup>**(1)**</sup>|h29||*|0 %|h30|0%|
|Humidity sensor - Max signal||1-2<sup>**(1)**</sup>|h30||*|h29|100 %|100%|
|Humidity control|0=None, 1=Humidifier, 2=Dehu-<br>midifier|1-2<sup>**(1)**</sup>|h31||*|0|2|0|
|Humidity max. temp.||1-2|h32||*|h33|70.0 °C|70.0 °C|
|Humidity min. temp.||1-2|h33||*|-5.0 °C|h32|2.0 °C|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Miscellaneous**

**Table 21: Miscellaneous**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Delay of outputs at pow-<br>er-up||1-2|o01|*|*|*|*|*|0 s|600 s|5s|
|DI1 Configuration|0=None, 1=DI status, 2=Door function,<br>3=Door alarm, 4=Defrost start, 5=Main<br>switch, 6=Night setback, 7=Thermostat<br>band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced<br>cooling, 14=Forced closing, 15=Shut-<br>down, 16=Light control, 20=Leak detec-<br>tion, 21=Adaptive liquid control,<br>29=Door fan stop|1-2<sup>**(1)**</sup>|o02|*|||*||0|29|0|
|Network address||1-3<sup>**(1)**</sup>|o03|*|*|*|*|*|0|240|0|
|Service pin|0=OFF, 1=ON|1-2|o04|*|*|*|*|*|0|1|0|
|Access code 3||3-3|o05|*|*|*|*|*|0|999|0|
|Temperature sensor type|0=Pt 1000, 1=PTC 1000, 2=NTC 5k,<br>3=NTC 10k, 4=User-defined|1-3<sup>**(1)**</sup>|o06|*|*|*|*|*|0|4|0|
|Max. hold time||1-2|o16|*|*|*|*|*|0 min|360 min|20 min|
|Pe Min range||1-3<sup>**(1)**</sup>|o20|*|*|*|*|*|-1.0 Bar|5.0 Bar|-1.0Bar|
|Pe Max range||1-3<sup>**(1)**</sup>|o21|*|*|*|*|*|6.0 Bar|200.0 Bar|12.0Bar|

|**Function**<br>|**Values**<br>|**R-W**<br>|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Refrigerant|0=Not seleted, 6=R13, 7=R13b1, 2=R22,<br>8=R23, 14=R32, 11=R114, 3=R134a,<br>12=R142b, 24=R170, 15=R227,<br>25=R290, 16=R401A, 18=R402A,<br>19=R404A, 21=R407A, 22=R407B,<br>20=R407C, 37=R407F, 49=R407H,<br>23=R410A, 32=R413A, 30=R417A,<br>31=R422A, 33=R422D, 34=R427A,<br>35=R438A, 40=R448A, 41=R449A,<br>48=R449B, 43=R450A, 44=R452B,<br>45=R454B, 9=R500, 4=R502, 10=R503,<br>17=R507, 36=R513A, 26=R600,<br>27=R600a, 5=R717, 28=R744,<br>46=R1233zdE, 38=R1234ze,<br>39=R1234yf, 47=R1234zeZ, 29=R1270,<br>42=R452A, 1=User defined display,<br>13=User defined|1-3<sup>**(1)**</sup>|o30|*|*|*|*|*|0|49|0|
|DI2 Configuration|0=None, 1=DI status, 2=Door function,<br>3=Door alarm, 4=Defrost start, 5=Main<br>switch, 6=Night setback, 7=Thermostat<br>band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced<br>cooling, 13=Coordinated defrost,<br>14=Forced closing, 15=Shutdown,<br>16=Light control, 20=Leak detection,<br>21=Adaptive liquid control, 29=Door<br>fan stop|1-2<sup>**(1)**</sup>|o37|*|*|*|*|*|0|29|0|
|Light control mode|1=Day and night, 2=Network, 3=Door<br>switch, 4=Network (Fallback), 5=Digital<br>input|1-2|o38|*|*|*|*|*|1|5|1|
|MC Light signal|0=OFF, 1=ON|1-2|o39|*|*|*|*|*|0|1|0|
|Rail heat ON cycle day||1-2|o41|*|*|*|*|*|0 %|100 %|100%|
|Rail heat ON cycle night||1-2|o42|*|*|*|*|*|0 %|100 %|100%|
|Rail heat period time||1-2|o43|*|*|*|||6 min|60 min|6min|
|<br>Case cleaning mode|0=OFF, 1=Fans run, 2=Cleaning|0-1|o46|*|*|*|*|*|0|2|0|
|Application mode|1=1. One evaporator MT/LT, 2=2. Two<br>evaporators MT/LT, 3=3. Three evapora-<br>tors MT, 4=4. Coldroom 2 MT/HT, 5=5.<br>Coldroom 2 MT/LT|1-3<sup>**(1)**</sup>|o61|*|*|*|*|*|1|5|1|
|Access code 2||2-2|o64|*|*|*|*|*|0|999|0|
|Make new factory|0=OFF, 1=ON|3-3<sup>**(1)**</sup>|o67|*|*|*|*|*|0|1|0|
|DI3 Configuration|0=None, 1=DI status, 2=Door function,<br>3=Door alarm, 4=Defrost start, 5=Main<br>switch, 6=Night setback, 7=Thermostat<br>band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced<br>cooling, 13=Coordinated defrost,<br>14=Forced closing, 15=Shutdown,<br>16=Light control, 20=Leak detection,<br>21=Adaptive liquid control, 29=Door<br>fan stop|1-2<sup>**(1)**</sup>|o84|*|*|*|*|*|0|29|0|
|Rail heat control mode|0=ON, 1=Day/Night timer, 2=Dewpoint<br>ctrl.|1-2|o85|*|*|*|*|*|0|2|0|
|Dewpoint min. limit||1-2|o86|*|*|*|*|*|-10.0 °C|o87|8.0 °C|
|Dewpoint max. limit||1-2|o87|*|*|*|*|*|o86|50.0 °C|17.0 °C|
|<br>Rail heat min. ON cycle||1-2|o88|*|*|*|*|*|0 %|100 %|30%|
|Door restart inj. delay||1-2|o89|*|*|*|*|*|0 min|240 min|30 min|
|Fan at forced closing|0=OFF, 1=ON, 2=OFF and suppress de-<br>frost, 3=ON and suppress defrost|1-2|o90|*|*|*|*|*|0|3|1|
|Display readout|1=Ther. air A, 2=Average all, 3=Maxi-<br>mum all, 4=S4A and S4B|1-2|o97|*|*|*|*|*|1|4|1|
|Light at Main switch OFF|<br> 0=OFF, 1=Normal ctrl.|1-2|o98|*|*|*|*|*|0|1|0|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **Control**

**Table 22: Control**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Alarm relay priority|0=Not used, 1=High Priority,<br>2=Medium priority, 3=All|1-2|P41|*||*|*|*|0|3|1|
|Fan stop at blinds closing||1-2|P65|*|*|*|*|*|0 s|300 s|0 s|
|Rail heat PWM - Period time||1-2|P82|*|*|*|*|*|4 s|60 s|10 s|
|Refrigerant factor K1||1-3<sup>**(1)**</sup>|P83|*|*|*|*|*|-999|999|300|
|Refrigerant factor K2||1-3<sup>**(1)**</sup>|P84|*|*|*|*|*|-999|999|300|
|Refrigerant factor K3||1-3<sup>**(1)**</sup>|P85|*|*|*|*|*|-999|999|300|
|Max superheat liquid ctrl.||1-2|P86|*|*|*|*|*|P87|20.0 °C|3.0 °C|
|Min superheat liquid ctrl||1-2|P87|*|*|*|*|*|0.0 °C|P86|1.0 °C|
|Access code 1||1-1|P88|*|*|*|*|*|0|999|0|
|Display keyboard lock|0=None, 1=Local, 2=Network|1-2|P89|*|*|*|*|*|0|2|0|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

### **DO conf i** **g and manual**

**Table 23: DO confi** **g and manual**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|AO1 Configuration|0=None, 1=Rail heat PWM|1-3<sup>**(1)**</sup>|q09|*|*|*|*|*|0|1|0|
|EEV override A||1-2<sup>**(2)**</sup>|q11|*|*|*|*|*|0 %|100 %|0%|
|Fan - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q13|*|*|*|*|*|0|1|0|
|Defrost A - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q14|*|*|||*|0|1|0|
|Rail heat - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q15|*|*|*|||0|1|0|
|Alarm relay - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q16|*||*|*|*|0|1|0|
|Light - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q17|*|*|*|*|*|0|1|0|
|Defrost B - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q22||*|||*|0|1|0|
|Air heater - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q23||||*||0|1|0|
|Humidifier - override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q26||||*||0|1|0|
|Rail heat PWM - override||1-2<sup>**(2)**</sup>|q27|*|*|*|*|*|0 %|100 %|0%|
|High temperature - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|0-2|q28|*|*|*|*|*|0|3|1|
|Low temperature - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q29|*|*|*|*|*|0|3|1|
|Sensor errors - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q30|*|*|*|*|*|0|3|1|
|DI alarms - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q31|*|*|*|*|*|0|3|2|
|Defrost - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q32|*|*|*|*|*|0|3|3|
|Miscellaneous - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q33|*|*|*|*|*|0|3|2|
|Injection - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q34|*|*|*|*|*|0|3|2|
|Control stopped - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q35|*|*|*|*|*|0|3|3|
|Leak detection - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q36|*|*|*|*|*|0|3|2|
|Humidity ctrl. - Priority|0=Disabled, 3=Low, 2=Medium,<br>1=High|1-2|q37||||*||0|3|2|
|Food temp. sensor|1=Ther. air A, 2=Average all,<br>3=Maximum all|1-2<sup>**(1)**</sup>|q39|*|*|*|*|*|1|3|1|
|EEV override B||1-2<sup>**(2)**</sup>|q41||*|*|*|*|0 %|100 %|0%|
|EEV override C||1-2<sup>**(2)**</sup>|q42|||*|||0 %|100 %|0%|
|S4 Air OFF evap. B - Adjustment||1-2|q43||*|*|*|*|-10.0 °C|10.0 °C|0.0 °C|
|S4 Air OFF evap. C - Adjustment||1-2|q44|||*|||-10.0 °C|10.0 °C|0.0 °C|
|Dehumidifier -override|0=MAN OFF, 1=MAN ON|1-2<sup>**(2)**</sup>|q46||||*||0|1|0|

> **(1) In order to change this parameter the regulation must be stopped via the parameter r12 Main switch = OFF.**

> **(2) In order to change this parameter the parameter r12 Main switch must be set in position "SEr" allowing manual control of outputs.**

### **Service**

**Table 24: Service**

|**Function**|**Values**|**R-W**|**Code**|**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Control state A|0=Normal ctrl., 1=Hold after defrost,<br>4=Drip off, 10=Main switch OFF,<br>11=Thermostat cutout, 12=Frost pro-<br>tection S4, 14=Defrost, 15=Fan delay,<br>16=Forced closing, 17=Door open,<br>18=Melt period, 19=Modulating temp.<br>control, 20=Emergency control,<br>23=Adaptive superheat control,<br>24=Start injection, 25=Manual control,<br>26=No refrigerant selected, 29=Case<br>cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heat-<br>ing, 45=Shut down controller, 48=Adap-<br>tive liquid control|0-X|u00|*|*|*|*|*|0|48|0|
|S5 Evaporator A||0-X|u09|*|*|||*|-200.0 °C|200.0 °C|0.0 °C|
|DI1 Status|0=OFF, 1=ON|0-X|u10|*|||*||0|1|0|
|Defrost time A||0-X|u11|*|*|*|*|*|0 min|900 min|0 min|
|Night condition|0=OFF, 1=ON|0-X|u13|*|*|*|*|*|0|1|0|
|S4 Air OFF evap. A||0-X|u16|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Thermostat air temp. A||0-X|u17|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Thermostat run time A||0-X|u18|*|*|*|*|*|0 min|999 min|0 min|
|S2 Gas outlet A||0-X|u20|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Superheat A||0-X|u21|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Superheat reference A||0-X|u22|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|EEV opening A||0-X|u23|*|*|*|*|*|0 %|100 %|0%|
|Pe Evap. pressure||0-X|u25|*|*|*|*|*|-1.0 Bar|200.0 Bar|0.0Bar|
|Te Evap. temp.||0-X|u26|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|DI2 Status|0=OFF, 1=ON|0-X|u37|*|*|*|*|*|0|1|0|
|Display readout 1||0-X|u56|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Alarm air temp. A||0-X|u57|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Fan|0=OFF, 1=ON|0-X|u59|*|*|*|*|*|0|1|0|
|Defrost A|0=OFF, 1=ON|0-X|u60|*|*|||*|0|1|0|
|Rail heat|0=OFF, 1=ON|0-X|u61|*|*|*|||0|1|0|
|Alarm relay|0=OFF, 1=ON|0-X|u62|*||*|*|*|0|1|0|
|Light|0=OFF, 1=ON|0-X|u63|*|*|*|*|*|0|1|0|
|S5 Evaporator B||0-X|u75||*|||*|-200.0 °C|200.0 °C|0.0 °C|
|Defrost B|0=OFF, 1=ON|0-X|u83||*|||*|0|1|0|
|Air heater|0=OFF, 1=ON|0-X|u84||||*||0|1|0|
|Rail heat power||0-X|u85|*|*|*|*|*|0 %|100 %|0%|
|Thermostat band|1=Band 1, 2=Band 2|0-X|u86|*|*|*|*|*|1|2|1|
|DI3 Status|0=OFF, 1=ON|0-X|u87|*|*|*|*|*|0|1|0|
|Thermostat cut-in temp.||0-X|u90|*|*|*|*|*|-200.0 °C|200.0 °C|4.0 °C|
|Thermostat cut-out||0-X|u91|*|*|*|*|*|-200.0 °C|200.0 °C|2.0 °C|
|temp.||||||||||||
|Alarm air temp. B||0-X|U34||*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Display readout 2||0-X|U35|*|*|*||*|-200.0 °C|200.0 °C|0.0 °C|
|Network status||0-X|U45|*|*|*|*|*|0 %|100 %|0%|
|Humidity sensor||0-X|U57||||*||0 %|100 %|0%|
|Humidifier|0=OFF, 1=ON|0-X|U58||||*||0|1|0|
|Rail heat PWM||0-X|U59|*|*|*|*|*|0 %|100 %|0%|
|Food temperature A||0-X|U72|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Defrost sensor tempera-<br>ture A||0-X|U73|*|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|

|**Function**|**Values**|**R-W**|**Code**<br>**1**|**2**|**3**|**4**|**5**|**Min. value**|**Max. value**|**Fact. value**|
|---|---|---|---|---|---|---|---|---|---|---|
|Control state B|0=Normal ctrl., 1=Hold after defrost,<br>4=Drip off, 10=Main switch OFF,<br>11=Thermostat cutout, 12=Frost pro-<br>tection S4, 13=Not_used, 14=Defrost,<br>15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period,<br>19=Modulating temp. control,<br>20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection,<br>25=Manual control, 26=No refrigerant<br>selected, 29=Case cleaning, 30=Forced<br>cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down<br>controller, 48=Adaptive liquid control|0-X|U74|*|*|*|*|0|48|0|
|Defrost time B||0-X|U75|*|*|*|*|0 min|900 min|0 min|
|S4 Air OFF evap. B||0-X|U76|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Thermostat air temp. B||0-X|U77|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Thermostat run time B||0-X|U78|*|*|*|*|0 min|999 min|0 min|
|S2 Gas outlet B||0-X|U79|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Superheat B||0-X|U80|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Superheat reference B||0-X|U81|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|EEV opening B||0-X|U82|*|*|*|*|0 %|100 %|0%|
|Control state C|0=Normal ctrl., 1=Hold after defrost,<br>4=Drip off, 10=Main switch OFF,<br>11=Thermostat cutout, 12=Frost pro-<br>tection S4, 13=Not_used, 14=Defrost,<br>15=Fan delay, 16=Forced closing,<br>17=Door open, 18=Melt period,<br>19=Modulating temp. control,<br>20=Emergency control, 23=Adaptive<br>superheat control, 24=Start injection,<br>25=Manual control, 26=No refrigerant<br>selected, 29=Case cleaning, 30=Forced<br>cooling, 31=Door open, 32=Power-up<br>delay, 33=Air heating, 45=Shut down<br>controller, 48=Adaptive liquid control|0-X|U83||*|||0|48|0|
|Defrost time C||0-X|U84||*|||0 min|900 min|0 min|
|S4 Air OFF evap. C||0-X|U85||*|||-200.0 °C|200.0 °C|0.0 °C|
|Thermostat air temp. C||0-X|U86||*|||-200.0 °C|200.0 °C|0.0 °C|
|Thermostat run time C||0-X|U87||*|||0 min|999 min|0 min|
|S2 Gas outlet C||0-X|U88||*|||-200.0 °C|200.0 °C|0.0 °C|
|Superheat C||0-X|U89||*|||-200.0 °C|200.0 °C|0.0 °C|
|Superheat reference C||0-X|U90||*|||-200.0 °C|200.0 °C|0.0 °C|
|EEV opening C||0-X|U91||*|||0 %|100 %|0%|
|<br>Alarm air temp. C||0-X|U92||*|||-200.0 °C|200.0 °C|0.0 °C|
|Defrost sensor tempera-<br>ture B||0-X|U93|*|*|*|*|-200.0 °C|200.0 °C|0.0 °C|
|Defrost sensor tempera-<br>||0-X|U94||*|||-200.0 °C|200.0 °C|0.0 °C|
|ture C|||||||||||
|Dehumidifier|0=OFF, 1=ON|0-X|U96|||*||0|1|0|

### **Operation via AK-UI55 Bluetooth**

##### **Access to parameters via Bluetooth and app**

1. App can be downloaded from App Store and Google Play.

- Name = AK-CC55 Connect

- Start the app.

2. Click on the display’s Bluetooth button for 3 seconds.

- The Bluetooth light will then flash while display is showing the controller’s address.

3. Connect to the controller from the app.

###### **Figure 45: AK-UI55 Bluetooth**

##### **Display info:**

- Loc

- The operation is locked and cannot be operated via Bluetooth.

- Unlock from the system manager.

*[Figurtekst: Fi g ure 46: Connect to controller Fi g ure 47: Controller dashboard]*

*[Figurtekst: Fi g ure 48: Set-u p  menu]*

The functions are described on Page 41 – Page 58.

### **AK-CC55 connect menu (SW ver. 1.9x)**

### **Start / Stop**

**Table 25: Start / Sto** **p**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Main switch|Start / stop of refrigeration.<br>With this setting refrigeration can be started, stopped<br>or a manual override of the outputs can be allowed.<br>(For manual control the value is set at -1). Then the<br>outputs can be force controlled. Start / stop of refrig-<br>eration can also be accomplished with the external<br>switch function connected to a DI input.Stopped con-<br>trol will give a ”Main switch OFF" alarm.|-1=Manual, 0=Stop, 1=Start|r12|r12 Main switch|
|Delay of outputs at<br>power-up|Delay of output signal after start-up.<br>After start-up or a power failure the controller’s func-<br>tions can be delayed so that overloading of the elec-<br>tricity supply network is avoided. Here you can set the<br>time delay.||o01|o01 DelayOfOutp.|

### **Conf i** **guration**

**Table 26: Confi** **g uration**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Main switch|Start / stop of refrigeration.<br>With this setting refrigeration can be started, stopped<br>or a manual override of the outputs can be allowed.<br>(For manual control the value is set at -1). Then the<br>outputs can be force controlled. Start / stop of refrig-<br>eration can also be accomplished with the external<br>switch function connected to a DI input. Stopped<br>control will give a ”Main switch OFF" alarm.|-1=Manual, 0=Stop, 1=Start|r12|r12 Main switch|
|Application mode|Selection of application.<br>The controller covers several applications for control<br>of a refrigerated case. Here you set which of the possi-<br>ble applications is required.This menu can only be set<br>when regulation is stopped, i.e. “r12 Main Switch” is<br>set to 0.|1=1. One evaporator MT/LT<br>2=2. Two evaporators MT/LT<br>3=3. Three evaporators MT<br>4=4. Coldroom 2 MT/HT<br>5=5. Coldroom 2 MT/LT|o61|o61 Appl. mode|
|AO1 Configuration|Select the function of the analogue output|0=None, 1=Rail heat PWM|q09|q09 AO1 Config.|
|DI1 Configuration|Select the function of the digital input|0=None, 1=DI status, 2=Door function, 3=Door alarm,<br>4=Defrost start, 5=Main switch, 6=Night setback,<br>7=Thermostat band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced cooling,<br>14=Forced closing, 15=Shutdown, 16=Light control,<br>20=Leak detection, 21=Adaptive liquid control,<br>29=Door fan stop|o02|o02 DI1 Config.|
|DI2 Configuration|Select the function of the digital input|0=None, 1=DI status, 2=Door function, 3=Door alarm,<br>4=Defrost start, 5=Main switch, 6=Night setback,<br>7=Thermostat band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced cooling, 13=Co-<br>ordinated defrost, 14=Forced closing, 15=Shutdown,<br>16=Light control, 20=Leak detection, 21=Adaptive<br>liquid control, 29=Door fan stop|o37|o37 DI2 Config.|
|DI3 Configuration|Select the function of the digital input|0=None, 1=DI status, 2=Door function, 3=Door alarm,<br>4=Defrost start, 5=Main switch, 6=Night setback,<br>7=Thermostat band, 8=Alarm at closed, 9=Alarm at<br>open, 10=Case cleaning, 11=Forced cooling,<br>14=Forced closing, 15=Shutdown, 16=Light control,<br>20=Leak detection, 21=Adaptive liquid control,<br>29=Door fan stop|o84|o84 DI3 Config|
|Refrigerant|Select the type of refrigerant.<br>If the required refrigerant is not part of the list, the<br>user defined option can be used. Please contact Dan-<br>foss for detailed information<br>**WARNING:**<br>Wrong selection of refrigerant may cause damage to<br>the system.|0=Not seleted, 6=R13, 7=R13b1, 2=R22, 8=R23,<br>14=R32, 11=R114, 3=R134a, 12=R142b, 24=R170,<br>15=R227, 25=R290, 16=R401A, 18=R402A, 19=R404A,<br>21=R407A, 22=R407B, 20=R407C, 37=R407F,<br>49=R407H, 23=R410A, 32=R413A, 30=R417A,<br>31=R422A, 33=R422D, 34=R427A, 35=R438A,<br>40=R448A, 41=R449A, 48=R449B, 43=R450A,<br>44=R452B, 45=R454B, 9=R500, 4=R502, 10=R503,<br>17=R507, 36=R513A, 26=R600, 27=R600a, 5=R717,<br>28=R744, 46=R1233zdE, 38=R1234ze, 39=R1234yf,<br>47=R1234zeZ, 29=R1270, 42=R452A, 1=User defined<br>display, 13=User defined|o30|o30 Refrigerant|
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
|Sensor point 1 -<br>Temp.|The temperature value for the user-defined tempera-<br>ture sensor in the reference point||X20|--- SP1 Temp|
|Sensor point 1 -<br>kohm|The resistance value in kohm for the user-defined<br>temperature sensor in the reference point||X21|--- SP1 kohm|
|Sensor point 1 -<br>ohm|The resistance value in ohm for the user-defined tem-<br>perature sensor in the reference point||X22|--- SP1 ohm|
|Sensor point 2 -<br>Temp.|The temperature value for the user-defined tempera-<br>ture sensor in the reference point||X23|--- SP2 Temp|
|Sensor point 2 -<br>kohm|The resistance value in kohm for the user-defined<br>temperature sensor in the reference point||X24|--- SP2 kohm|
|Sensor point 2 -<br>ohm|The resistance value in ohm for the user-defined tem-<br>perature sensor in the reference point||X25|--- SP2 ohm|
|Sensor point 3 -<br>Temp.|The temperature value for the user-defined tempera-<br>ture sensor in the reference point||X26|--- SP3 Temp|
|Sensor point 3 -<br>kohm|The resistance value in kohm for the user-defined<br>temperature sensor in the reference point||X27|--- SP3 kohm|
|Sensor point 3 -<br>ohm|The resistance value in ohm for the user-defined tem-<br>perature sensor in the reference point||X28|--- SP3 ohm|
|Defrost method|Select method of defrost|0=None, 1=Electrical, 4=Air/Offcycle|d01|d01 Def. method|
|Defrost stop meth-<br>od|Here you define whether a defrost cycle is to be stop-<br>ped by time or by a temperature sensor|0=Time, 1=S5 sensor, 2=S4 sensor|d10|d10 DefStopSens.|
|Defrost stop limit A|When the selected defrost stop sensor reaches the set<br>limit, the defrost cycle is terminated||d02|d02 Def.StopTemp|
|Food type|When changing the food type the controller will auto-<br>matically adapt temperature setpoints and alarm lim-<br>its according to the selected food type. Please be<br>aware that the setting will revert to "None" after hav-<br>ing been changed.|0=None, 1=Vegetables, 2=Dairy, 3=Meat and fish,<br>4=Frozen food, 5=Ice cream|r89|r89 Food type|
|Food temp. sensor|Select the temperature to be used for the food tem-<br>perature representation|1=Ther. air A, 2=Average all, 3=Maximum all|q39|q39 Food sensor|
|Network address|Network address of the controller||o03|o03 Unit addr.|
|Service pin|If the controller is built into a LonWorks network with<br>data communication, it must have an address, and<br>the system manager must know this address.The ad-<br>dress is sent to the system manager when the menu is<br>set in pos. ON.|0=OFF, 1=ON|o04|o04 Service pin|
||**IMPORTANT:**<br>Before you set o04, you MUST set the application<br>mode of the controller (The function is not used<br>when the data communication is MODBUS)||||

### **Thermostat control**

**Table 27: Thermostat control**

|**Function**<br>|**Description**<br>|**Values**<br>f|**Code**<br>|**Short name**<br>|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Thermostat air<br>temp. A|Thermostat temperature||u17|u17 Ther. air|
|Thermostat air<br>temp. B|Thermostat temperature||U77|U77 Ther. Air B|
|Thermostat air<br>temp. C|Thermostat temperature||U86|U86 Ther. Air C|
|Food temperature A|Readout of food temperature||U72|U72 Food temp.|
|S4 Air OFF evap. A|Actual sensor value||u16|u16 S4 air temp.|
|S4 Air OFF evap. B|Actual sensor value||U76|U76 S4 temp B|
|S4 Air OFF evap. C|Actual sensor value||U85|U85 S4 temp C|
|Night condition|Status of the day/night operation (night operation:<br>on/off)|0=OFF, 1=ON|u13|u13 Night Cond.|
|Thermostat cut-in<br>temp.|f<br>Readout of the actual cut-in value for the thermostat||u90|u90 Cutin temp.|
|Thermostat cut-out<br>temp.|Readout of the actual cut-out value for the thermo-<br>stat||u91|u91 Cutout temp.|
|Thermostat run time<br>A|Read the ongoing cut-in time for the thermostat or<br>the duration of the last completed cut-in||u18|u18 Ther runtime|
|Thermostat run time<br>B|Read the ongoing cut-in time for the thermostat or<br>the duration of the last completed cut-in||U78|U78 TherRuntimeB|
|Thermostat run time<br>|Read the ongoing cut-in time for the thermostat or<br>||U87|U87 TherRuntimeC|
|C|the duration of the last completed cut-in||||
|Thermostat band|Readout of which thermostat is used for regulation:<br>1= Thermostat band 1<br>2= Thermostat band 2|1=Band 1, 2=Band 2|u86|u86 Ther. band|
|Air heater|Actual status of output function|0=OFF, 1=ON|u84|u84 Heat relay|
|Thermostat mode|Here it is defined how the thermostat is to be operat-<br>ed. Either as an ordinary ON/OFF thermostat or as a<br>modulating thermostat.When operation is ”modulat-<br>ing” the valve will limit the flow of refrigerant so that<br>the temperature variation will be less than for the<br>ON/OFF thermostat.The thermostat differential (r01)<br>must not be set lower than 2K for ”modulating”. In a<br>decentralised plant you must select the ON/OFF ther-<br>mostat setting.|1=ON/OFF, 2=Modulating, 3=ON/OFF Common|r14|r14 Therm. mode|
|Thermostat sensor|Select which sensor to be used for the thermostat<br>control|1=Ther. air A, 2=Average all, 3=Maximum all|r99|r99 Ther. sensor|
|Cut-out 1|Setpoint. The thermostat’s cut-out value when the<br>given thermostat band is in use||r00|r00 Cutout|

|**Function**|**Description**<br>**Values**|**Code**|**Short name**|
|---|---|---|---|
|Differential 1|When the temperature is higher than the set cut-out<br>+ the set differential, the compressor relay will be cut-<br>in. It will cut-out again when the temperature comes<br>down to the set cut-out limit.|r01|r01 Differential|
|Cut-out 2|Setpoint. The thermostat’s cut-out value when the<br>given thermostat band is in use|r21|r21 Cutout 2|
|Differential 2|When the temperature is higher than the set cut-out<br>+ the set differential, the compressor relay will be cut-<br>in. It will cut-out again when the temperature comes<br>down to the set cut-out limit|r93|r93 Diff Th2|
|Max cut-out limit|Setpoint limitation - The controller’s setting range for<br>the thermostat setpoint may be narrowed down, so<br>that too high or too low values are not set accidental-<br>ly - with resulting damages.To avoid a too high set-<br>ting of the setpoint, the max. allowable reference val-<br>ue may be lowered|r02|r02 Max cutout|
|Min cut-out limit|Setpoint limitation - The controller’s setting range for<br>the thermostat setpoint may be narrowed down, so<br>that too high or too low values are not set accidental-<br>ly - with resulting damages.To avoid a too low setting<br>of the setpoint, the min. allowable reference value<br>may be increased|r03|r03 Min cutout|
|Night offset|Night setback value.The thermostat’s reference will be<br>the setpoint plus this value when the controller<br>changes over to night operation.|r13|r13 Night offset|
|Air heater neutral<br>zone|Heat function. Set the width of the Neutral Zone for<br>changeover from cooling to heating|r62|r62 Heat NZ|
|Air heater start de-<br>lay|Time delay on transition from refrigeration phase to<br>heating phase (there is no time delay on transition<br>from heating phase to refrigeration)|r63|r63 HeatStartDel|
|Melt interval|Melt function. Only for control of MT cases/rooms (-5<br>to +10°C). The function ensures that the evaporator<br>will not be blocked by ice crystals. Here you set how<br>often the function is to stop the refrigeration and<br>hence transform the ice crystals to water.|r16|r16 MeltInterval|
|Melt period|Melt period. Here you set how long an ongoing melt<br>function is to last|r17|r17 Melt period|

### **Alarm limits and delays**

###### **Table 28: Alarm limits and dela** **y s**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Alarm status|Actual alarm status|0=OFF, 1=ON|x16|--- Sum alarm|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Alarm air temp. A|Measured temperature for alarm thermostat||u57|u57 Alarm air|

|**Function**|**Description**<br>**Values**|**Code**|**Short name**|
|---|---|---|---|
|Alarm air temp. B|Measured temperature for alarm thermostat|U34|U34 Alarm air B|
|Alarm air temp. C|Measured temperature for alarm thermostat|U92|U92 Alarm air C|
|High alarm limit|Readout of actual high alarm limit for the tempera-<br>ture monitoring|y10|--- High al. lim|
|Low alarm limit|Readout of actual low alarm limit for the temperature<br>monitoring|y11|--- Low al. lim|
|S4 Air OFF evap. A|Actual sensor value|u16|u16 S4 air temp.|
|S4 Air OFF evap. B|Actual sensor value|U76|U76 S4 temp B|
|S4 Air OFF evap. C|Actual sensor value|U85|U85 S4 temp C|
|Reset alarms|Command for resetting all alarms, unless they are still<br>active<br>0=OFF, 1=ON|x15|--- Reset alarm|
|High alarm limit 1|Upper alarm limit. The limit value is set in absolute<br>value. The limit value will be raised with the night off-<br>set during night operation.|A13|A13 HighLim Air|
|Low alarm limit 1|Lower alarm limit. The limit value is set in absolute<br>value|A14|A14 LowLim Air|
|High alarm limit 2|Upper alarm limit. The limit value is set in absolute<br>value. The limit value will be raised with the night off-<br>set during night operation.|A20|A20 HighLim2 Air|
|Low alarm limit 2|Lower alarm limit. The limit value is set in absolute<br>value|A21|A21 LowLim2 Air|
|Alarm delay A|Alarm delay (short alarm delay on air temperature). If<br>the upper or the lower alarm limit values are excee-<br>ded, a timer function will commence. The alarm will<br>not become active until the set time delay has been<br>passed. The time delay is set in minutes|A03|A03 Alarm delay|
|Alarm delay pull-<br>down A|Alarm delay at tempeature pull down conditions<br>(long alarm delay). This time delay is used during<br>start-up, during defrost and immediately after a de-<br>frost. There will be a change-over to the normal time<br>delay when the temperature has dropped below the<br>set upper alarm limit.|A12|A12 Pulldown del|
|Door open alarm<br>delay|Time delay for door alarm|A04|A04 DoorOpen del|
|Door restart inj. de-<br>lay|Start of refrigeration when the door is open. If the<br>door has been left open, refrigeration will be started<br>after the set time.|o89|o89 DoorInjStart|
|Alarm delay DI 1|Time delay for digital input alarm|A27|A27 Al.Delay DI1|
|Alarm delay DI 2|Time delay for digital input alarm|A28|A28 Al.Delay DI2|

### **Humidity control**

**Table 29: Humidit** **y control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Humidity sensor|||U57|U57 RH level %|
|Humidifier|Actual status of output function|0=OFF, 1=ON|U58|U58 Humidifier|
|Dehumidifier|Actual status of output function|0=OFF, 1=ON|U96|U96 Dehumidifier|
|Humidity control|Select the type of humidity control|0=None, 1=Humidifier, 2=Dehumidifier|h31|h31 RH function|
|Humidity cut-in|Set-point for the humidity control.<br>At humidifier control, the humidifier is started when<br>the humidity has dropped to the set-point.<br>At dehumidifier control, the dehumidifier is stopped,<br>when the humidity has dropped to the set-point||h23|h23 RH Cutin SP|
|Humidity differen-<br>tial|Differential for humidity control.<br>At humidifier control, the humidifier is stopped when<br>the humidity has increased with the set differential<br>above the set-point.<br>At dehumidifier control, the dehumidifier is started,<br>when the humidity has increased with the set differ-<br>ential above the set-point||h24|h24 RH Diff.|
|Humidity high alarm<br>limit|High alarm limit for relative humidity||h25|h25 RH HighLimAl|
|Humidity low alarm<br>limit|Low alarm limit for relative humidity||h26|h26 RH LowLimAl|
|Humidity alarm de-<br>lay|Delay of high and low humidity alarms||h27|h27 RH Al. delay|
|Humidity sensor -<br>Min signal|||h29|h29 RH Min Value|
|Humidity sensor -<br>Max signal|||h30|h30 RH Max Value|
|Humidity ctrl. at de-<br>frost|Select how to control humidity during defrost:<br>No: Humidity control is stopped during defrost<br>Yes: Normal humidity control is running during de-<br>frost|0=No, 1=Yes|h28|h28 RH CtrlAtDef|
|Humidity max.<br>temp.|Maximum limit for thermostat air temperature in or-<br>der for humidity control to run (frost limit)||h32|h32 RH Max temp.|
|Humidity min. temp.|Minimum limit for thermostat air temperature in or-<br>der for humidity control to run (frost limit)||h33|h33 RH Min temp.|

### **Injection control**

**Table 30: In** **j ection control** → **In** **j ection control A**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Thermostat air<br>temp. A|Thermostat temperature||u17|u17 Ther. air|
|S4 Air OFF evap. A|Actual sensor value||u16|u16 S4 air temp.|
|EEV opening A|Actual status of output function||u23|u23 EEV OD %|
|Pe Evap. pressure|Actual sensor signal||u25|u25 EvapPress Pe|
|Te Evap. temp.|Temperature converted from pressure||u26|u26 EvapTemp Te|
|S2 Gas outlet A|Actual sensor value||u20|u20 S2 temp.|
|Superheat A|Readout of actual superheat at the outlet of the evap-<br>orator||u21|u21 Superheat|
|Superheat reference<br>A|Readout of the actual superheat reference||u22|u22 SuperheatRef|
|Min. superheat limit|Min. value for the superheat reference||n10|n10 Min SH|
|Max. superheat limit|Max. value for the superheat reference||n09|n09 Max SH|
|MOP temperature|MOP temperature. The valve opening degree is re-<br>duced until the evaporating temperature reaches the<br>set MOP limit. If no MOP function is required, select<br>the highest value that corresponds to OFF||n11|n11 MOP temp.|
|AKV Period time|Period time for the pulse width modulation||n13|n13 AKV Period|
|Min superheat liq-<br>uid ctrl|Min. value for the superheat reference during adap-<br>tive liquid control||P87|P87 SH Min Liq.|
|Max superheat liq-<br>uid ctrl.|Max. value for the superheat reference during adap-<br>tive liquid control||P86|P86 SH Max Liq.|

**Table 31: In** **j ection control** → **In** **j ection control B**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Thermostat air<br>temp. B|Thermostat temperature||U77|U77 Ther. Air B|
|S4 Air OFF evap. B|Actual sensor value||U76|U76 S4 temp B|
|EEV opening B|Actual status of output function||U82|U82 EEV OD % B|
|Pe Evap. pressure|Actual sensor signal||u25|u25 EvapPress Pe|
|Te Evap. temp.|Temperature converted from pressure||u26|u26 EvapTemp Te|
|S2 Gas outlet B|Actual sensor value||U79|U79 S2 temp. B|
|Superheat B|Readout of actual superheat at the outlet of the evap-<br>orator||U80|U80 Superheat B|
|Superheat reference<br>B|Readout of the actual superheat reference||U81|U81 SH Ref B|

**Table 32: In** **j ection control** → **In** **j ection control C**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Thermostat air<br>temp. C|Thermostat temperature||U86|U86 Ther. Air C|
|S4 Air OFF evap. C|Actual sensor value||U85|U85 S4 temp C|
|EEV opening C|Actual status of output function||U91|U91 EEV OD % C|
|Pe Evap. pressure|Actual sensor signal||u25|u25 EvapPress Pe|
|Te Evap. temp.|Temperature converted from pressure||u26|u26 EvapTemp Te|
|S2 Gas outlet C|Actual sensor value||U88|U88 S2 temp. C|
|Superheat C|Readout of actual superheat at the outlet of the evap-<br>orator||U89|U89 Superheat C|
|Superheat reference<br>C|Readout of the actual superheat reference||U90|U90 SH Ref C|

### **Defrost control**

**Table 33: Defrost control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Defrost sensor tem-<br>perature A|Actual temperature of selected defrost stop sensor||U73|U73 Def.StopTemp|
|Defrost sensor tem-<br>perature B|Actual temperature of selected defrost stop sensor||U93|U93 Def.StopTemB|
|Defrost sensor tem-<br>perature C|Actual temperature of selected defrost stop sensor||U94|U94 Def.StopTemC|
|S5 Evaporator A|Actual sensor value||u09|u09 S5 temp.|
|S5 Evaporator B|Actual sensor value||u75|u75 S5 temp. B|
|Defrost A|Actual status of output function|0=OFF, 1=ON|u60|u60 Def. relay|
|Defrost B|Actual status of output function|0=OFF, 1=ON|u83|u83 Def. relay B|
|Defrost time A|Read the duration of the ongoing defrost or the dura-<br>tion of the last completed defrost.||u11|u11 Defrost time|
|Defrost time B|Read the duration of the ongoing defrost or the dura-<br>tion of the last completed defrost.||U75|U75 Def. Time B|

|**Function**<br>Defrost time C|**Description**<br>Read the duration of the ongoing defrost or the dura-<br>tion of the last completed defrost.|**Values**|**Code**<br>U84|**Short name**<br>U84 Def. Time C|
|---|---|---|---|---|
|Start defrost|Command for starting a defrost|0=OFF, 1=ON|x09|--- Def. Start|
|Stop defrost|Command for stopping an ongoing defrost cycle|0=OFF, 1=ON|x10|--- Def. Stop|
|Defrost method|Select method of defrost|0=None, 1=Electrical, 4=Air/Offcycle|d01|d01 Def. method|
|Defrost stop meth-<br>od|Here you define whether a defrost cycle is to be stop-<br>ped by time or by a temperature sensor|0=Time, 1=S5 sensor, 2=S4 sensor|d10|d10 DefStopSens.|
|Defrost stop limit 1|When the selected defrost stop sensor reaches the set<br>limit, the defrost cycle is terminated||d02|d02 Def.StopTemp|
|Defrost stop limit 2|Defrost stop temperature limit when thermostat band<br>2 is in operation.When the selected defrost stop sen-<br>sor reaches the set limit, the defrost cycle is termina-<br>ted||d28|d28 DefStopTemp2|
|Min. defrost time|Minimum duration of a defrost cycle. The defrost cy-<br>cle will as a minimum run for the set minimum defrost<br>time once it is started||d24|d24 Min Def Time|
|Max. defrost time 1|Max duration of a defrost cycle. The setting is also<br>used as a safety time if the defrost is stopped on tem-<br>perature. If the selected defrost stop sensor does not<br>reach the set defrost stop temperature limit within<br>the set time, the defrost will be stopped anyway.||d04|d04 Max Def.time|
|Max. defrost time 2|Max duration of a defrost cycle when thermostat<br>band 2 is in operation. The setting is also used as a<br>safety time if the defrost is stopped on temperature. If<br>the selected defrost stop sensor does not reach the<br>set defrost stop temperature limit within the set time,<br>the defrost will be stopped anyway.||d29|d29 MaxDefTime2|
|Defrost start interval|The function is zeroset and will start the timer func-<br>tion at each defrost start. When the time has expired<br>the function will start a defrost. The function is used<br>as a simple defrost start, or it may be used as a safe-<br>guard if the normal signal fails to appear. If master/<br>slave defrost without clock function or without data<br>communication is used, the interval time will be used<br>as max. time between defrosts. If a defrost start via<br>data communcation does not take place, the interval<br>time will be used as max. time between de-<br>frosts.When there is defrost with clock function or da-<br>ta communication, the interval time must be set for a<br>somewhat longer period of time than the planned<br>one. In connection with power failure the interval<br>time will be maintained, and when the power returns<br>the interval time will continue from the maintained<br>value. he interval time is not active when set to 0||d03|d03 Def.Interval|
|Time staggering<br>power-up|Time staggering for defrost cut-ins during start-up<br>The function is only relevant if you have several refrig-<br>eration appliances or groups where you want the de-<br>frost to be staggered in relation to one another. The<br>function is furthermore only relevant if you have<br>chosen defrost with interval start. The function delays<br>the interval time by the set number of minutes, but it<br>only does it once, and this at the very first defrost tak-<br>ing place when voltage is connected to the controller.<br>The function will be active after each and every pow-<br>er failure.||d05|d05 Time stagg.|
|Max. thermostat run<br>time|Defrost on demand. Aggregate refrigeration time set<br>here is the refrigeration time allowed without de-<br>frosts. If the time is passed, a defrost will be started.<br>With setting = 0 the function is not in use.||d18|d18 MaxTherRunT.|
|Pump down delay|Set the time where the evaporator is emptied of re-<br>frigerant prior to the actual defrost cycle||d16|d16 Pump dwn del|
|Drip off time|Here you set the time that is to elapse from a defrost<br>and until the compressor is to start again. (The time<br>when water drips off the evaporator).||d06|d06 DripOff time|
|Max. hold time|Max. standby time after coordinated defrost. When a<br>controller has completed a defrost it will wait for a<br>signal tellingthat the refrigeration may be resumed. If<br>this signal fails to appear for one reason or another,<br>the controller itself will start the refrigeration when<br>the standby time has elapsed.||o16|o16 MaxHoldTime|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Fan control during<br>defrost|Fan operation during defrost Here you can set how<br>the fan is to operate during defrost.<br>0: Stopped (runs during pump down)<br>1: Running (stopped during "fan delay)<br>2: Running during pump down and defrost. After that<br>stopped<br>3: Running during pump down and defrost until de-<br>frost stop sensor reaches fan stop temperature limit|0=OFF, 1=ON, 2=OFF at drip, 3=OFF at high temp|d09|d09 FanDuringDef|
|Fan start delay|Delay of fan start after defrost. Here you set the time<br>that is to elapse from compressor start after a defrost<br>and until the fan may start again. (The time when re-<br>maining water is transformed into ice on the evapora-<br>tor).||d07|d07 FanStartDel|
|Fan start tempera-<br>ture|Temperature limit for starting the fans after a defrost.<br>When the measured S5 evaporator temperature is<br>getting below the set limit, the fans are started||d08|d08 FanStartTemp|
|Fan stop tempera-<br>ture|If the fan control during defrost has been set up for it,<br>the fans can be stopped during the defrost if the de-<br>frost sensor exceeds the set temperature limit||d41|d41 Def Fan Stop|
|Rail heat during de-<br>frost|Define how rail heat is controlled during defrost<br>0: Rail heat is OFF all the time<br>1: Rail heat is ON all the time<br>2: Normal rail heat control|0=OFF, 1=ON, 2=Normal control|d27|d27 Railh.at def|
|Display delay after<br>defrost|Set the maximum time the display should show the<br>defrost code "-d-" after a defrost. The normal temper-<br>ature readout is normally started when the tempera-<br>ture in the case is OK again or if a high temperature<br>alarm is raised.||d40|d40 Disp. d del.|

### **Defrost schedules**

**Table 34: Defrost schedules**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Defrost schedule||0=No, 1=Yes|t00|t00 Def.Schedule|
|Def. start 1 - Hours|Time in hours for start of defrost||t01|t01 Def. 1 hr.|
|Def. start 1 - Minutes|Time in minutes for when defrost cycle is to be star-<br>ted||t11|t11 Def. 1 min.|
|Def. start 2 - Hours|Time in hours for start of defrost||t02|t02 Def. 2 hr.|
|Def. start 2 - Minutes|Time in minutes for when defrost cycle is to be star-<br>ted||t12|t12 Def. 2 min.|
|Def. start 3 - Hours|Time in hours for start of defrost||t03|t03 Def. 3 hr.|
|Def. start 3 - Minutes|Time in minutes for when defrost cycle is to be star-<br>ted||t13|t13 Def. 3 min.|
|Def. start 4 - Hours|Time in hours for start of defrost||t04|t04 Def. 4 hr.|
|Def. start 4 - Minutes|Time in minutes for when defrost cycle is to be star-<br>ted||t14|t14 Def. 4 min.|
|Def. start 5 - Hours|Time in hours for start of defrost||t05|t05 Def. 5 hr.|
|Def. start 5 - Minutes|Time in minutes for when defrost cycle is to be star-<br>ted||t15|t15 Def. 5 min.|
|Def. start 6 - Hours|Time in hours for start of defrost||t06|t06 Def. 6 hr.|
|Def. start 6 - Minutes|Time in minutes for when defrost cycle is to be star-<br>ted||t16|t16 Def. 6 min.|
|Monday - Follow<br>schedule||0=No, 1=Yes|t51|t51 Mon.Schedule|
|Tuesday - Follow<br>schedule||0=No, 1=Yes|t52|t52 Tue.Schedule|
|Wednesday - Follow<br>schedule||0=No, 1=Yes|t53|t53 Wed.Schedule|
|Thursday - Follow<br>schedule||0=No, 1=Yes|t54|t54 Thu.Schedule|
|Friday - Follow<br>schedule||0=No, 1=Yes|t55|t55 Fri.Schedule|
|Saturday - Follow<br>schedule||0=No, 1=Yes|t56|t56 Sat.Schedule|
|Sunday - Follow<br>schedule||0=No, 1=Yes|t57|t57 Sun.Schedule|

### **Fan control**

**Table 35: Fan control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Fan|Actual status of output function|0=OFF, 1=ON|u59|u59 Fan relay|
|Fan pulsing mode|Pulse operation of fan<br>0: No pulse operation<br>1: Pulse operation when the thermostat is cut out<br>2: Pulse operation when the thermostat is cut out, but<br>only during night operation|0=No pulsing, 1=Pulsing cut-out, 2=Pulsing cut-out<br>night|F05|F05 FanPulseMode|
|Fan period time|Period time for pulsing of fan||F06|F06 Fan cycle|
|Fan ON cycle|ON time for fan. The ON period is set as a percentage<br>of the period time||F07|F07 Fan ON %|
|Fan stop high S5<br>temp.|Fan stop temperature The function stops the fans in<br>an error situation, so that they will not provide power<br>to the appliance. If the defrost sensor registers a high-<br>er temperature than the one set here, the fans will be<br>stopped. There will be re-start at 2 K below the set-<br>ting. The function is not active during a defrost or<br>start-up after a defrost.||F04|F04 FanStop temp|
|Fan at forced closing|You can set whether fans should be operational or<br>stopped if the function "Forced closing" is activated<br>here.<br>0: Fans are OFF<br>1: Fans are ON<br>2: Fans are OFF and defrost is not permitted<br>3: Fans are ON and defrost is not permitted|0=OFF, 1=ON, 2=OFF and suppress defrost, 3=ON and<br>suppress defrost|o90|o90 Fan ForcedCl|
|Fan stop at blinds<br>closing|When blinds are closing the fans are stopped in the<br>defined time delay in order to ensure that the blinds<br>are closed correctly||P65|P65 BlindFanStop|

### **Railheat control**

###### **Table 36: Railheat control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Dewpoint|Actual dewpoint received from system manager via<br>network||x18|--- Dew point|
|Rail heat|Actual status of output function|0=OFF, 1=ON|u61|u61 Railh. relay|
|Rail heat power|Readout of the actual rail power in %||u85|u85 Rail DutyC %|
|Rail heat PWM|Actual status of output function||U59|U59 Railheat PWM|
|Rail heat control<br>mode|The rail heat can be controlled in several ways:<br>0: Rail heat is running all the time<br>1: Pulse control is used with a timer function follow-<br>ing the day/night operation<br>2: Pulse control is used with a dewpoint function. This<br>function requires that a signal is received about the<br>dewpoint value. The value is measured by a system<br>manager and sent to the controller via the data com-<br>munication.|0=ON, 1=Day/Night timer, 2=Dewpoint ctrl.|o85|o85 Railh. mode|
|Rail heat ON cycle<br>day|Rail heat power during day time. The ON period is set<br>as a percentage of the period||o41|o41 Railh.ONday%|
|Rail heat ON cycle<br>night|Rail heat power during night time. The ON period is<br>set as a percentage of the period time||o42|o42 Railh.ONngt%|
|Rail heat period<br>time|Period time for pulsing of rail heat||o43|o43 Railh.cycle|
|Rail heat PWM - Peri-<br>od time|Period time for the pulse width modulation||P82|P82 RailCyclePWM|
|Rail heat min. ON<br>cycle|Lowest permitted rail heat power. When the meas-<br>ured dewpoint is below the defined minimum limit<br>the rail heat will run with the set minimum power||o88|o88 Rail Min ON%|
|Dewpoint min. limit|If the measuered dewpoint is below the set value the<br>rail heat is running at minimum heat||o86|o86 DewP Min lim|
|Dewpoint max. limit|If the measured dewpoint is above the set value the<br>rail heat is maximum||o87|o87 DewP Max lim|

### **Light/Cleaning control**

**Table 37: Li** **g ht/Cleanin** **g control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cutout, 12=Frost<br>protection S4, 13=Not_used, 14=Defrost, 15=Fan de-<br>lay, 16=Forced closing, 17=Door open, 18=Melt peri-<br>od, 19=Modulating temp. control, 20=Emergency<br>control, 23=Adaptive superheat control, 24=Start in-<br>jection, 25=Manual control, 26=No refrigerant selec-<br>ted, 29=Case cleaning, 30=Forced cooling, 31=Door<br>open, 32=Power-up delay, 33=Air heating, 45=Shut<br>down controller, 48=Adaptive liquid control|U83|U83 Ctrl.State C|
|Night condition|Status of the day/night operation (night operation:<br>on/off)|0=OFF, 1=ON|u13|u13 Night Cond.|
|Light|Actual status of output function|0=OFF, 1=ON|u63|u63 Light relay|
|Light control mode|Configuration of light function<br>1: Light is controlled via day/night status<br>2: Light is controlled via data communication and<br>master control parameter "MC Light signal"<br>3: Light is controlled by door contact on DI input.<br>When the door is opened the relay will cut in. When<br>the door is closed again there will be a time delay of<br>two minutes before the light is switched off.<br>4: As "2" but if there are any 15-minute network errors,<br>the light will switch on and the night blind will open.<br>5: Light is controlled via DI input signal|1=Day and night, 2=Network, 3=Door switch, 4=Net-<br>work (Fallback), 5=Digital input|o38|o38 Light config|
|Light at Main switch<br>OFF|Define how light and blinds are to be controlled at<br>Main switch OFF<br>0: Light is switched off and night blinds are open<br>when the main switch is off<br>1: Light and night blinds are independent of main<br>switch.|0=OFF, 1=Normal ctrl.|o98|o98 Light MS=Off|
|Case cleaning mode|The status of the function can be seen here or the<br>function can be started manually.<br>0 = Normal operation (no cleaning)<br>1 = Only fans are running to defrost the evaporator.<br>All other outputs are Off.<br>2 = Cleaning with stopped fans. All outputs are Off. If<br>the function is controlled by a digital input signal, the<br>relevant status can be seen here in the menu.|0=OFF, 1=Fans run, 2=Cleaning|o46|o46 Case clean|

### **Display control**

**Table 38: Dis** **p la** **y control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Display readout 1|Readout of the temperature shown on the display||u56|u56 Display air|
|Display readout 2|Readout of the temperature shown on the display||U35|U35 Display air2|
|Display readout|Select which temperature to show in the display|1=Ther. air A, 2=Average all, 3=Maximum all, 4=S4A<br>and S4B|o97|o97 Displ. Ctrl.|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Display readout ad-<br>justment|Correction of the display´s temperature.If the temper-<br>ature at the products and the temperature received<br>by the controller are not identical, an offset adjust-<br>ment of the display temperature can be carried out.||r04|r04 Disp. Adj. K|
|Temperature unit|Select whether temperatures are to be shown as °C or<br>as °F.|0=Celsius, 1=Fahrenheit|r05|r05 Temp.unit|
|Display keyboard<br>lock|With this setting it is possible to lock the keyboard<br>operation of the local display.<br>None: Display keyboard operation will never be<br>locked<br>Local: When not used for some time, the local display<br>will lock the keyboard operations and a special key<br>combination is required in order to enable the key-<br>board operations<br>Network: When the controller receives a master con-<br>trol signal (--- Key/BT lock) via the network, the dis-<br>play keyboard operations will be locked. The key-<br>board operations can only be activated again by set-<br>ting the master control signal OFF via the System<br>Manager.|0=None, 1=Local, 2=Network|P89|P89 LockDispKey|

### **Alarm relay priorities**

**Table 39: Alarm rela** **y p riorities**

|**Function**<br>Alarm relay|**Description**<br>Actual status of output function|**Values**<br>0=OFF, 1=ON|**Code**<br>u62|**Short name**<br>u62 Alarm relay|
|---|---|---|---|---|
|Alarm relay priority|Set which alarm priorities that are to activate the<br>alarm relay:<br>0=Not used. Alarm relay is not used<br>1=High. Alarm with high priority will activate relay<br>2=Medium. Alarms with high or medium priority will<br>activate the alarm relay<br>3=All. All alarms will activate alarm relay|0=Not used, 1=High Priority, 2=Medium priority,<br>3=All|P41|P41 Al.Rel.Prio|
|Mute alarm|When muting alarms, the alarm relay will stop signal-<br>ling the alarm until a new alarm arises|0=OFF, 1=ON|q38|q38 Mute Alarm|
|High temperature -<br>Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q28|q28 Hi Temp Prio|
|Low temperature -<br>Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q29|q29 Lo Temp Prio|
|Sensor errors - Prior-<br>ity|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q30|q30 Sensor Prio|
|DI alarms - Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q31|q31 DIAlarm Prio|
|Defrost - Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q32|q32 Defrost Prio|
|Miscellaneous - Pri-<br>ority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q33|q33 Misc Prio|
|Injection - Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q34|q34 Inject Prio|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Control stopped -<br>Priority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q35|q35 CtrlOFF Prio|
|Leak detection - Pri-<br>ority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q36|q36 Leak Prio|
|Humidity ctrl. - Pri-<br>ority|Select the priority of the alarms associated to the<br>alarm group. Be aware - by selecting "Disable" the<br>alarms will not be shown on the display or be routed<br>to the alarm relay or to the network.|0=Disabled, 3=Low, 2=Medium, 1=High|q37|q37 Humid Prio|

### **Miscellaneous**

**Table 40: Miscellaneous** → **Access codes**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Access code 3|Access code for local display||o05|o05 Acc. code 3|
|Access code 2|Access code for local display||o64|o64 Acc. code 2|
|Access code 1<br>**Table 41: Miscel**|Access code for local display<br>**laneous**→**Network**||P88|P88 Acc. code 1|
|**Function**|**Description**|**Values**|**Code**|**Short name**|
|Network status|Quality of the network communication||U45|U45 Comm. status|
|Network address|Network address of the controller||o03|o03 Unit addr.|
|Baudrate|Communication speed of network|1=Auto, 2=9600 Baud, 3=19200 Baud, 4=38400 Baud|x96|--- Bus baudrate|
|Parity and stop bit|Select parity and stop bit of Modbus messages|0=None, 1=Even, 2=Odd|x97|--- Parity bit|

###### **Table 41: Miscellaneous** → **Network**

###### **Table 42: Miscellaneous** → **Sensor ad** **j ustment**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|S2 Gas outlet A - Ad-<br>justment|Correction of sensor signal e.g. due to long sensor ca-<br>ble||r19|r19 Adjust S2|
|S4 Air OFF evap. A -<br>Adjustment|Correction of sensor signal e.g. due to long sensor ca-<br>ble||r09|r09 Adjust S4|
|S4 Air OFF evap. B -<br>Adjustment|Correction of sensor signal e.g. due to long sensor ca-<br>ble||q43|q43 Adjust S4B|
|S4 Air OFF evap. C -<br>Adjustment|Correction of sensor signal e.g. due to long sensor ca-<br>ble||q44|q44 Adjust S4C|
|S5 Evaporator A -<br>Adjustment|Correction of sensor signal e.g. due to long sensor ca-<br>ble||r11|r11 Adjust S5|
|**Table 43: Miscell**<br>**Function**|**aneous**→**Factory reset**<br>**Description**|**Values**|**Code**|**Short name**|
|Make new factory|With this command you save the controller’s actual<br>settings as a new basic setting (the earlier factory set-<br>tings are overwritten).|0=OFF, 1=ON|o67|o67 Make factory|
|Reset to factory set-<br>tings|Command which will revert all controller settings to<br>factory values.|0=OFF, 1=ON|z06|--- Reset factory|

###### **Table 43: Miscellaneous** → **Factor** **y reset**

### **Advanced**

**Table 44: Advanced** → **Advanced in** **j ection control**

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|Superheat ctrl.<br>mode A|Select how to control the superheat of the evapora-<br>tor. At adaptive control the superheat reference is<br>adapted automatically to give the best utilization of<br>the evaporator surface. At load based control the su-<br>perheat reference is increased at high loads|1=Adaptive, 2=Load based|n21|n21 SH mode|
|Superheat close A|Minimum superheat limit where the valve is closing||x68|--- SH close|
|Superheat close liq-<br>uid ctrl. A|Minimum limit of superheat where the valve is clos-<br>ing during adaptive liquid control||x87|--- SH close Liq|
|Superheat Kp min. A|Min limit for amplification factor of the PI controller<br>adjusting the valve opening degree (expert setting)||x70|--- SH Kp min|
|Superheat Kp max.<br>A|Max limit for amplification factor of the PI controller<br>adjusting the valve opening degree (expert setting)||x71|--- SH Kp max|
|Superheat Tn A|Integration time of the PI controller adjusting the<br>valve opening degree (expert setting)||x72|--- SH Tn|

|**Function**<br>|**Description**<br>|**Values**|**Code**<br>|**Short name**<br>|
|---|---|---|---|---|
|S2 stabillity A|Setting of required stability of S2 gas outlet tempera-<br>ture before the superheat reference is reduced (Ex-<br>pert setting)A higher value will allow more instabillity<br>in S2 signalA lower value will allow less instabillity in<br>S2 signal||Y33|--- S2 Stability|
|S2 Std deviation A|Expert injection setting - contact Danfoss for further<br>information||Y34|--- S2 Std Dev|
|Te feedback gain A|Gain factor for feedback of evaporating temperature<br>signal Te to the PI controller controlling the superheat<br>(expert setting)||x73|--- Te-gain|
|Kp MTR control A|Amplification factor for modulating temperature con-<br>trol (Expert setting)||x77|--- MTR Kpfactor|
|Tn MTR control A|Integration time for modulating temperature control<br>(Expert setting)||x78|--- MTR Tn sec|
|SH Band|Expert injection setting - contact Danfoss for further<br>information||Y28|--- SH Band|
|P-gain|Expert injection setting - contact Danfoss for further<br>information||Y31|--- P - Gain|
|Ther. duty cycle SP|Expert setting - contact Danfoss for further informa-<br>tion||Y29|--- ThDutyCycle|
|AFident A|Expert readout - contact Danfoss for further informa-<br>tion||x79|--- AFident|
|AFidentForce A|Expert setting - contact Danfoss for further informa-<br>tion||x69|--- AFidentForce|
|Calculated Max OD<br>A|Calculated maximum opening degree of the injection<br>valve (expert readout)||x80|--- Max OD %|
|OD Ctrl. status A|Readout showing which part of the injection function<br>that is in control of the valve opening degree|Values must be changed as per below:<br>0=Adaptive SH control<br>1=MOP<br>2=Superheat close<br>3=MTR|Y32|--- OD Status|
|Ther. duty cycle A|Expert injection setting - contact Danfoss for further<br>information||Y30|--- ActDutyCycle|
|AFident B|Expert readout - contact Danfoss for further informa-<br>tion||z23|--- AFident B|
|AFidentForce B|Expert setting - contact Danfoss for further informa-<br>tion||z03|--- AFidenForceB|
|S2 Std deviation B|Expert injection setting - contact Danfoss for further<br>information||Y37|--- S2 Std Dev B|
|Calculated Max OD<br>B|Calculated maximum opening degree of the injection<br>valve (expert readout)||z25|--- Max OD % B|
|OD Ctrl. status B|Readout showing which part of the injection function<br>that is in control of the valve opening degree|Values must be changed as per below:<br>0=Adaptive SH control<br>1=MOP<br>2=Superheat close<br>3=MTR|Y35|--- OD Status B|
|Ther. duty cycle B|Expert injection setting - contact Danfoss for further<br>information||Y36|--- ActDutyCyc B|
|AFident C|Expert readout - contact Danfoss for further informa-<br>tion||z24|--- AFident C|
|AFidentForce C|Expert setting - contact Danfoss for further informa-<br>tion||z04|--- AFidenForceC|
|S2 Std deviation C|Expert injection setting - contact Danfoss for further<br>information||Y40|--- S2 Std Dev C|
|Calculated Max OD<br>C|Calculated maximum opening degree of the injection<br>valve (expert readout)||z26|--- Max OD % C|
|OD Ctrl. status C|<br>Readout showing which part of the injection function<br>that is in control of the valve opening degree|Values must be changed as per below:<br>0=Adaptive SH control<br>1=MOP<br>2=Superheat close<br>3=MTR|Y38|--- OD Status C|
|Ther. duty cycle C|Expert injection setting - contact Danfoss for further<br>information||Y39|--- ActDutyCyc C|

**Table 45: Advanced** → **Master control**

|**Function**<br>|**Description**<br>|**Values**<br>f|**Code**<br>|**Short name**<br>|
|---|---|---|---|---|
|Control state A|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cut-out,<br>12=Frost protection S4, 13=Not_used, 14=Defrost,<br>15=Fan delay, 16=Forced closing, 17=Door open,<br>18=Melt period, 19=Modulating temp. control,<br>20=Emergency control, 23=Adaptive superheat con-<br>trol, 24=Start injection, 25=Manual control, 26=No re-<br>frigerant selected, 29=Case cleaning, 30=Forced cool-<br>ing, 31=Door open, 32=Power-up delay, 33=Air heat-<br>ing, 45=Shut down controller, 48=Adaptive liquid<br>control|u00|u00 Ctrl. state|
|Control state B|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cut-out,<br>12=Frost protection S4, 13=Not_used, 14=Defrost,<br>15=Fan delay, 16=Forced closing, 17=Door open,<br>18=Melt period, 19=Modulating temp. control,<br>20=Emergency control, 23=Adaptive superheat con-<br>trol, 24=Start injection, 25=Manual control, 26=No re-<br>frigerant selected, 29=Case cleaning, 30=Forced cool-<br>ing, 31=Door open, 32=Power-up delay, 33=Air heat-<br>ing, 45=Shut down controller, 48=Adaptive liquid<br>control|U74|U74 Ctrl.State B|
|Control state C|Readout of the actual control state of the controller|0=Normal ctrl., 1=Hold after defrost, 4=Drip off,<br>10=Main switch OFF, 11=Thermostat cut-out,<br>12=Frost protection S4, 13=Not_used, 14=Defrost,<br>15=Fan delay, 16=Forced closing, 17=Door open,<br>18=Melt period, 19=Modulating temp. control,<br>20=Emergency control, 23=Adaptive superheat con-<br>trol, 24=Start injection, 25=Manual control, 26=No re-<br>frigerant selected, 29=Case cleaning, 30=Forced cool-<br>ing, 31=Door open, 32=Power-up delay, 33=Air heat-<br>ing, 45=Shut down controller, 48=Adaptive liquid<br>control|U83|U83 Ctrl.State C|
|Regulation condi-<br>tion A|Readout of the actual control state of the controller|0=Main switch OFF, 1=Injection start, 2=Superheat<br>ctrl., 3=Fill evap., 4=Defrost, 5=Post defrost, 6=Forced<br>closing, 7=Injection fault, 8=Emergency control,<br>9=Modulating ctrl., 10=Melt period, 11=Door open,<br>12=Case cleaning, 13=Cutout, 14=Forced cooling,<br>15=Shut down|x62|--- Reg. Cond.|
|Regulation condi-<br>tion B|Readout of the actual control state of the controller|0=Main switch OFF, 1=Injection start, 2=Superheat<br>ctrl., 3=Fill evap., 4=Defrost, 5=Post defrost, 6=Forced<br>closing, 7=Injection fault, 8=Emergency control,<br>9=Modulating ctrl., 10=Melt period, 11=Door open,<br>12=Case cleaning, 13=Cutout, 14=Forced cooling,<br>15=Shut down|z01|--- Reg. Cond B|
|Regulation condi-<br>tion C|Readout of the actual control state of the controller|0=Main switch OFF, 1=Injection start, 2=Superheat<br>ctrl., 3=Fill evap., 4=Defrost, 5=Post defrost, 6=Forced<br>closing, 7=Injection fault, 8=Emergency control,<br>9=Modulating ctrl., 10=Melt period, 11=Door open,<br>12=Case cleaning, 13=Cutout, 14=Forced cooling,<br>15=Shut down|z02|--- Reg. Cond C|
|MC Actual cut-in<br>temp.|||x63|--- Cutin temp.|
|MC Actual cut-out<br>temp.|||x64|--- Cutout temp.|
|MC Ther. toggle|Master control signal used for switching case load<br>ON/OFF depending on the load condition|0=No action, 1=Toggle ON, 2=Toggle OFF|x81|--- TherToggle|
|MC Load request|Master control signal used to control the load balance<br>between multiple case controllers on the same suc-<br>tion line||x82|--- LoadReq|
|MC Max. Te offset|Requested offset to actual evporating temperature in<br>order to keep the air temperature at the actual set-<br>point||x84|--- MaxTeOffset|
|MC Liquid control|Master control signal allowing switch to adaptive liq-<br>uid control|0=OFF, 1=ON|x85|--- MC Liq. Ctrl|
|MC Night setback|Master control signal for changing between day and<br>night time operation|0=OFF, 1=ON|x06|--- Night setbck|
|MC Case shutdown|Master control signal used to shut down a case for a<br>time period. During shutdown there will be no alarm<br>monitoring|0=OFF, 1=ON|x17|--- Case shutdwn|
|MC Forced closing|Master control signal that will close the injection<br>valve|0=OFF, 1=ON|x07|--- Forced close|
|MC Forced cooling|Master control signal that will provide forced cooling|0=OFF, 1=ON|x08|--- Forced cool.|

|**Function**|**Description**|**Values**|**Code**|**Short name**|
|---|---|---|---|---|
|MC Defrost start|Master control signal for starting a defrost. At adap-<br>tive defrost the defrost might be skipped if the de-<br>frost is not needed|0=OFF, 1=ON|x13|--- MC def.start|
|MC Defrost state|Read out the actual state of the defrost|0=OFF, 1=ON|x14|--- DefrostState|
|MC Hold after de-<br>frost|Master control signal used for co-ordinated defrost<br>control to hold cabinets from returning to normal re-<br>frigeration after a defrost until all cabinets have termi-<br>nated defrost|0=OFF, 1=ON|x11|--- HoldAfterDef|
|MC Stop defrost|Master control signal used to prevent a defrost start in<br>a controller.|0=OFF, 1=ON|x12|--- Disable def.|
|MC Light signal|Master control signal for control of light via a data<br>communication signal from the system manager|0=OFF, 1=ON|o39|o39 Light remote|
|MC Actual dewpoint|Master control signal sending the actual measured<br>dewpoint from the system manager to the controller<br>over the network.||x03|--- Act.DewPoint|
|MC Po load factor|||x83|--- Load factor|
|MC Key/Bluetooth<br>lock|Master control signal that will lock down all Bluetooth<br>data communication and optionally also the opera-<br>tion of the display keys (depend upon selection in<br>P89 Display keyboard lock)|0=OFF, 1=ON|x33|--- Key/BT Lock|
|MC Min. delta T|Required minimum delta temperature across evapo-<br>rator (S3 - Te) in order to keep the air temperature at<br>the actual setpoint||y04|--- Min Delta T|
|No. of case sections|No. of sections in the case||z05|--- NoOfEvap|

### **Fault message**

In an error situation the alarm LED on the front will be on and the alarm relay will be activated (depending on priority). If you push the alarm button for 3 seconds you can see the alarm report in the display. (Alarm priorities can be changed. See Table 39: Alarm relay priorities.) Here are the messages that may appear:

|**Code**|**Alarm text**|**Description**|
|---|---|---|
|E01|Hardware failure|The controller has a hardware failure|
|E06|Clock lost time|Clock has lost valid time|
|E20|Pe Evap. pressure A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E24|S2 Gas outlet A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E26|S4 Air OFF evap. A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E27|S5 Evaporator A - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E37|S5 Evaporator B - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E59|Humidity sensor - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E60|S4 Air OFF evap. B - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E61|S4 Air OFF evap. C - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E62|S2 Gas outlet B - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|E63|S2 Gas outlet C - Sensor error|Sensor signal is out of range. Please check the sensor for correct operation|
|A01|High temperature alarm A|The alarm temperature has been above the max alarm limit for a longer time period than the set alarm delay.|
|A02|Low temperature alarm A|The alarm temperature has been below the min alarm limit for a longer time period than the set alarm delay.|
|A04|Door open alarm|The door has been open for a too long time|
|A05|Max defrost hold time exceeded|The controller has been waiting longer time than permitted after a co-ordinated defrost.|
|A11|Refrigerant not selected|The refrigerant has not been selected hence control can not be initiated|
|A15|DI alarm 1|Alarm signal from digital input signal|
|A16|DI alarm 2|Alarm signal from digital input signal|
|A45|Main switch set OFF|The controller manin switch has been set to either Stop or Manaual control. Alternatively a digital input set up for<br>"main switch" function, has stopped control|
|A59|Case in cleaning mode|A case cleaning operation has been started on a case|
|A70|High temperature alarm B|The alarm temperature has been above the max alarm limit for a longer time period than the set alarm delay.|
|A71|Low temperature alarm B|The alarm temperature has been below the min alarm limit for a longer time period than the set alarm delay.|
|AA2|CO2leak detected|CO2is leaking from the refrigerantion system|
|AA3|Refrigerant leak detected|Refrigerant is leaking from the refrigeration system|
|a02|High humidity alarm|The humidity level is too high|
|a03|Low humidity alarm|The humidity level is too low|
|a05|High temperature alarm C|The alarm temperature has been above the max alarm limit for a longer time period than the set alarm delay.|
|a06|Low temperature alarm C|The alarm temperature has been below the min alarm limit for a longer time period than the set alarm delay.|

|**Code**|**Alarm text**|**Description**|
|---|---|---|
|Z01|Max defrost time exceeded A|The last defrost cycle has stopped on time instead of set temperature|
|Z02|Max defrost time exceeded B|The last defrost cycle has stopped on time instead of set temperature|
|Z03|Max defrost time exceeded C|The last defrost cycle has stopped on time instead of set temperature|

 **NOTE:**

##### **Data communication**

The importance of individual alarms can be defined with a setting. The setting must be carried out in the group "Alarm destinations".

### **Operating status**

**Table 46: O** **p eratin** **g status**

|**Ctrl. State/**<br>**Code**|**Operating status**|**Description**|
|---|---|---|
||Push the info button for 3 seco<br>following meanings:|nds to see status. If there is a status code, it will be shown on the display. The individual status codes have the|
|S0|Normal ctrl.|The controller is running normal control. There is no other control taking priority|
|S1|Hold after defrost|The controller is waiting for other controllers to terminate coordinated defrost|
|S4|Drip off|The defrost has terminated and the controller is waiting for drip delay to expire, while the water is dripping off the<br>evaporator|
|S10|Main switch OFF|The controller has been stopped because the parameter r12 Main switch has been set in OFF or Service position or<br>the controller has been stopped via Main switch function on DI input|
|S11|Thermostat cut-out|The air temperature has reached the thermostat cut-out value|
|S14|Defrost|The controller is running a defrost cycle|
|S15|Fan delay|The evaporator fans are waiting to start after a defrost cycle (d07, Fan start delay and d08, Fan start temperature)|
|S16|Forced closing|The injection valve has been forced closed via a signal on a digital input or from the system manager (compressor<br>pack is restricted from starting)|
|S17|Door open|DI signal indicates that the cold room door is open|
|S18|Melt period|The controller has stopped refrigeration for a short while to turn ice crystals into water and thereby improve air<br>flow through the evaporator|
|S19|Modulating temp. control|The air temperature is controlled close to the set point via a modulating temperature control|
|S20|Emergency control<sup>**(1)**</sup>|The air temperature is controlled according to an emergency procedure due to sensor error (Pe, S2 or S4)|
|S23|Adaptive superheat control|The superheat of the evaporator is optimized|
|S24|Start injection|The liquid injection into the evaporator has started|
|S25|Manual control|Main switch has been set in Service position for manual control of outputs|
|S26|No refrigerant selected|The refrigerant type has not been selected (parameter o30 Refrigerant)|
|S29|Case cleaning|A case cleaning operation has been initiated via parameter o46 Case cleaning mode or via a signal on a digital<br>input or via the AK-CC55 Connect app|
|S30|Forced cooling|The thermostat has been overruled to run forced cooling via a signal on a digital input|
|S32|Power-up delay|The controller has just been powered up and the output control is waiting for the power-up delay to expire (pa-<br>rameter o01, Delay of outputs at power-up)|
|S33|Air heating|The air heater is energized in order to raise the air temperature (parameters r62, Air heater neutral zone and r63, Air<br>heater start delay)|
|S45|Shut down controller|The control has been stopped due to a digital input signal or from the system manager|
|S48|Adaptive liquid control|The superheat control is running adaptive liquid control with reduced superheat for transcritical CO2systems with<br>ejectors. Signal is provided via digital input or from the system manager|

> **(1) Emergency control:**

- **If Pe or S2 sensor fails, the controller will operate with a safe opening degree based on normally registered opening degree during day and night operation.**

- **If S4 sensor fails, the thermostat will operate with a registered ON/OFF duty cycle during day and night operation.**

### **Product specification**

### **Technical data**

### Electrical specifications

**Table 47: Electrical s** **p ecifications**

|**Electrical data**|**Value**|
|---|---|
|Supply voltage AC [V]|115 V / 230 V, 50/60 Hz|
|Power consumption [VA]|5 VA|
|Power ON indicator|Green LED|
|Electrical cable dimensioning [mm<sup>2</sup>]|Max.1.5 mm<sup>2</sup>multi-core cable|

### Sensor and measuring data

**Table 48: Sensor and measurin** **g data**

|**Sensor and measuring data**|**Value**|
|---|---|
|Sensor S2|Pt 1000 AKS11|
|Sensor S4, S5|Pt 1000 AKS11<br>PTC 1000 EKS111<br>NTC5K EKS211<br>NTC10K EKS221 sensor|
||(Both must be of the same type)|
|Temperature measuring accuracy|Pt1000: -60 – 120 °C. ±0.5 K<br>PTC1000: -60 – 80 °C. ±0.5 K<br>NTC5K: -40 – 80 °C. ±1.0 K<br>NTC10K: -40 – 120 °C. ±1.0 K|
|Pt1000 sensor specification|±0.3 K at 0 °C<br>±0.005 K per degree|
|Pe measuring|AKS 32R Ratiometric pressure transmitter: 10-90%|
|RH measuring|0 – 10 V<br>Ri > 10K ohm<br>Accuracy +/- 0,3% FS|

### Input and output relay specifications

**Table 49: In** **p ut and out** **p ut rela** **y s** **p ecifications**

|**Input and output relay specifications**|**Input/output**|**Description**|
|---|---|---|
|Digital input|DI1<br>DI2|Signal from dry contact functions<br>Requirements to contacts: Gold plating<br>Cable length must be max. 15 m<br>Use auxiliary relays when the cable is longer<br>Open loop: 12 V (SELV)<br>Contact 3.5 mA|
|Digital input|DI3|115 V / 230 V AC|
|Solid state output|DO1 (for AKV coil)<br>DO3|115 V / 230 V AC<br>Max. 0.5 A|
||DO7|DO3 and DO7 (No overload protection!)<br>Max. 1 x 20 W AKV for 115 V AC<br>2 x 20 W AKV for 230 V AC<br>**Note:**2 EC coils are not supported.|
|Relays|DO2<br>DO4|115 V / 230 V AC<br>Load max.: CE. 8 (6)A|
||DO5<br>DO6|UL. 8A res. 3FLA 18LRA<br>Load min.: 1VA<br>Inrush: DO5 DO6 TV-5 80A|
|Analogue output/ PWM|AO1|0 / 10 V Pulse Width Modulated<br>(PWM) max. 15 mA.<br>0 – 10 V variable, max. 2 mA|

 **NOTE:**

- DO2, DO4, DO5 and DO6 are 16 A relays.

- Max. load must be observed.

- DO5 / DO6 is recommended for load with high inrush current e.g. EC Fan and LED light.

- All relays are sealed for use with flammable refrigerant like Propane R290.

- Compliance with EN 60 335-2-89: 2010 Annex BB.

### Function data

**Table 50: Function data**

|**Function data**|**Value**|
|---|---|
|Display|LED 3 digit|
|External display, AK-CC55 Multi Coil|2 external displays|
|External display connection|RJ12|
|Max. display cable length [m]|100 m|
|Data communication built-in|MODBUS|
|Data communication option|AK-OB55 Lon RS485 module|
|Clock battery backup power reserve|4 days|
|Mounting|DIN rail|

### Environmental conditions

**Table 51: Environmental conditions**

|**Environmental conditions**|**Value**|
|---|---|
|Ambient temperature range, operation [°C]|0 – 55 °C|
|Ambient temperature range, transport [°C]|-40 – 70 °C|
|Enclosure rating IP|IP20|
|Relative humidity range [%]|20 – 80%, non-condensing|
|Shocks/Vibrations|No shocks and vibrations allowed|

### **Dimensions**

Measurements are in mm.

*[Figurtekst: Fi g ure 49: AK-CC55 Multi Coil Fi g ure 50: AK-UI55 Set]*

###### **Fi** **g ure 51: AK-OB55**

### **Ordering**

The list contains the components that make up an AK-CC55 Multi Coil setup. For other Danfoss products mentioned in the document, such as sensors and valves, refer to relevant product documentation.

**Table 52: Orderin** **g**

|**Type**|**Symbol**|**Function**|**Code no.**|
|---|---|---|---|
|AK-CC55 Multi Coil||Case controller for one, two or three AKV valves|**084B4084**|
|AK-UI55 Info||External display|**084B4077**|
|AK-UI55 Bluetooth||External display with Bluetooth operation|**084B4075**|
|AK-UI55 Set||External display with control buttons|**084B4076**|
|AK-UI55 Mounting Base|Danfoss<br>80G8236|Mounting kit for display types: AK-UI55 Set, AK-UI55 Bluetooth, AK-UI55 Info|**084B4099**|
|AK-UI cable||External display cable with RJ12 connector. 3 m|**084B4078**|
|AK-UI cable||External display cable with RJ12 connector. 6 m|**084B4079**|
|AK-OB55 Lon||Data communication module Lon<br>Can be mounted in Single Coil and Multi Coil versions|**084B4070**|
|MMIMYK|Danfoss<br>80G8284|Gateway between AK-CC55 and PC installed with KoolProg software|**080G0073**|

### **Certificates, declarations, and approvals**

The list contains all certificates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

Some approvals may change over time. You can check the most current status at danfoss.com or contact your local Danfoss representative if you have any questions.

**Table 53: Controller**

|**Control**|**Certification**|**Mark**|**Country**|
|---|---|---|---|
|Multi Coil|EMC/LVD/RoHS|CE|EU|
|Multi Coil|UL recognized|cURus|NAM (US and Canada)|
|Multi Coil|ACMA (EMC)|RCM|Australia/New Zealand|
|Multi Coil|LVE/EMC/RoHS|EAC|Russia, Kazakhstan, Belarus|
|Multi Coil|LVD/EMC/RoHS|UA|Ukraine|

###### **Table 54: Dis** **p la** **y module**

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

###### **Table 55: O** **p tion module**

|**Option module**|**Certification**<br>**Mark**<br>**Country**|
|---|---|
|AK-OB55 LoN|EMC/LVD<br>UA<br>Ukraine|

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
