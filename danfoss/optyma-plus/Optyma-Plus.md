# Danfoss Optyma Plus – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Controller for condensing unit Optyma™ Plus

*Kilde: Danfoss-dokument BC172686425380en-001201.pdf*

**User Guide**

**Controller for condensing unit** Optyma™ **Plus**

**SW Ver. 3.7x**

**www.danfoss.com**

### **Introduction**

### **Application**

Condensing unit control

#### **Advantages**

- Condensing pressure control in relation to outside temperature

- Fan variable speed regulation

- On/off or variable speed regulation of the compressor

- Heating element control in crankcase

- Day/night controller operation

- Built-in clock function with power reserve

- Built-in Modbus data communication

- Monitoring discharge temperature td

- Oil return management control at variable speed control

#### **Principle**

The controller receives a signal for demanded cooling, and it then starts the compressor.

If the compressor is controlled by variable speed, the suction pressure (converted to temperature) will be controlled according to a set temperature value.

Condenser pressure regulation is performed again following a signal from the ambient temperature sensor and the set reference. The controller will then control the fan, which allows the condensing temperature to be maintained at the desired value. The controller can also control the heating element in the crankcase so that oil is kept separate from the refrigerant. For excess discharge temperature, the liquid injection will be activated in the suction line (for compressors with the liquid injection option).

#### **Functions**

- Control of condensing temperature

- Control of fan speed

- On/off control or speed regulation of the compressor

- Control of heating element in crankcase

- Liquid injection into economizer port (if possible)

- Raising the condenser pressure regulation reference during night operation

- Extern start/stop via DI1

- Safety cut-out activated via signal from automatic safety control

#### **Regulation reference for condensing temperature**

The controller controls the condensing Reference, which is in detail the difference between condensing temperature and ambient temperature. The reference setpoint can be shown with a brief push on the middle button and adjusted with the upper and lower button. The reference can be raised at night to allow slower fan speeds to reduce fan noise. This is done via the night set back feature.

#### **This setting can be changed without entering the programming mode so care needs to be taken to not adjust unintentionally.**

#### Day/Night

The controller has an internal clock function which changes between daytime and night operation. During night operation, the reference is raised by the 'Night offset' value.

*[Figurtekst: Reference Night offset · Set Point · Tamb · Day Night Day]*

This day/night signal can also be activated in two other ways:

- Via an on/off input signal - DI2

- Via data communication.

2 | BC172686425380en-001201

#### **Fan operation**

The controller will control the fan so that the condensing temperature is maintained at the desired value above the outdoor temperature.

The user may select from different ways to control the fan:

- Internal speed regulation

- Here the fan is speed-controlled via terminal 5-6. At a need of 95% and above, the relay on terminal 15-16 are activated, while 5-6 are deactivated.

- External speed regulation

- For larger fan motors with insufficient internal outlet, an external speed regulation can be connected to terminal 54-55. A 0 – 10 V signal indicating the desired speed is then sent from this point. The relay on terminal 15-16 will be active when the fan is in operation.

In menu 'F17' the user can define which of the two controls to use.

#### Fan speed at start

When the fan is re-started after an idle period, it will be started at a speed that is set in the 'Jog Speed' function. This speed is maintained for 10 seconds, after which the speed changes to the regulation need.

#### Fan speed at low loads

At low loads between 10 and 30%, the speed will remain at that which is set in the 'FanMinSpeed' function.

#### Fan speed at low ambient temperatures

To avoid frequent start/stops in low ambient temperatures in which the fan's capacity is high, the internal amplification factor is lowered. This provides a smoother regulation. The 'Jog speed' is also lowered in the area from 10 °C and down to -20 °C.

At temperatures below -20 °C the 'Jog Low' value can be used.

*[Figurtekst: 15 – 16 · 54 – 55 · 15 – 16 · Speed · Jog · Min. · Required capacity · Speed · Jog · Jog low]*

#### Compressor compartment pre-ventilation

The condenser fan starts and operates for a period of time and speed before the compressor starts. This happens in case of any mildly flammable refrigerant selected via “o30 Refrigerant”, to get a safe atmosphere while sucking potential flammable A2Lrefrigerant gas out of the compressor compartment. There is a fixed delay of about 8 seconds between this preventilation and compressor start in order to reduce the airflow significantly and avoid any condensing problems on low ambient temperatures.

#### **Compressor control**

The compressor is controlled by a signal at the DI1 input. The compressor will start once the input is connected. Three restrictions have been implemented to avoid frequent start/ stops:

- One for minimum ON time

- One for minimum OFF time

- One for how much time must elapse between two starts. These three restrictions have the highest priority during regulation, and the other functions will wait until they are complete before regulation can continue. When the compressor is 'locked' by a restriction, this can be seen in a status notification. If the DI3 input is used as a safety stop for the compressor, an insufficient input signal will immediately stop the compressor. Variable speed compressors can be speed-controlled with a voltage signal at the AO2 output. If this compressor has been running for a long period at low speed, the speed is increased for a short moment for the purpose of oil-return.

#### **Maximum discharge gas temperature**

The temperature is recorded by sensor Td.

If variable speed control is chosen for the compressor, this control will initially reduce the compressor capacity if the Td temperature approaches the set maximum value.

If a higher temperature is detected than the set max. temperature, the fan's speed will be set to 100%. If this does not cause the temperature to drop, and if the temperature remains high after the set delay time, the compressor will be stopped. The compressor will only be re-started once the temperature is 10 K lower than the set value. The above mentioned re-start restrictions must also be complete before the compressor can start once again. If the delay time is set to '0', the function will **not** stop the compressor. The Td sensor can be deactivated (o63).

#### **Liquid injection into economizer port**

The controller can activate the liquid injection into economizer port if the discharge temperature is approaching the maximum allowable temperature.

Note: Liquid injection function use the Aux Relay if the relay is configured to this function.

#### **High pressure monitoring**

During regulation, the internal high pressure monitoring function is able to detect an over the limit condensing pressure so that the regulation can continue. However, if the c73 setting is exceeded, the compressor will be stopped and an alarm is triggered.

If, on the other hand, the signal comes from the interrupted safety circuit connected to DI3, the compressor will immediately be stopped and the fan will be set to 100%.

When the signal is once again 'OK' at the DI3 input, the regulation will resume.

#### **Low pressure monitoring**

During regulation, the internal low pressure monitoring function will cut out the compressor upon detecting a suction pressure that falls below the lower limit, but only once the minimum ON time is exceeded. An alarm will be issued (A2). This function will be time delayed, if the compressor starts at low ambient temperature.

#### **Pump down limit**

The compressor will be stopped if a suction pressure that falls below the set value is registered, but only once the minimum ON time is exceeded.

*[Figurtekst: DI off: · Alarm overview Di3 => A97 / DI2=1 => A97]*

4 | BC172686425380en-001201

#### **Heating element in the crankcase**

The controller has a thermostat function which can control the heating element for the crankcase. Oil can thus be kept separate from the refrigerant. The function is active when the compressor has stopped.

The function is based on the ambient temperature and suction gas temperature. When the two temperatures are equal ± a temperature difference, power will be supplied to the heating element. The 'CCH off diff' setting indicates when power will no longer be supplied to the heating element.

The 'CCH on diff' indicates when 100% power will be sent to the heating element.

Between the two settings the controller calculates the wattage and connects to the heating element in a pulse/pause cycle which corresponds to the desired wattage.

The Taux sensor can be used to record the temperature in the crankcase if desired.

When the Taux sensor records a temperature lower than Ts+10 K, the heating element will be set to 100%, but only if the ambient temperature is below 0 °C.

#### **Separate thermostat function**

The taux sensor can also be used in a heating function with programmable temperature. Here, the AUX relay will connect the heating element.

#### **Digital inputs**

There are two digital inputs DI1 and DI2 with contact function and one digital input DI3 with high voltage signal. They can be used for the following functions:

- DI1: Starts and stops compressor

DI2: Here the user can select from various functions Signal from an external safety function External main switch / night setback signal / separate alarm function / Monitoring of input signal / signal from an external speed control

- DI3: Safety signal from low/high-pressure switch

#### **Data communication**

The controller is delivered with built-in MODBUS data communication.

If a different form of data communication is requested, a LON RS485 module can be inserted in the controller. The connection will then be made on terminal RS 485.

#### **Important**

All connections to the data communication must comply with the requirements for data communication cables. See literature: RC8AC.

#### **Display**

The controller has one plug for a display. Here display type EKA 163B or EKA 164B (max. length 15 m) can be connected. EKA 163B is a display for readings.

EKA 164B is both for readings and operation.

The connection between display and controller must be with a cable which has a plug at both ends.

A setting can be made to determine whether the Tc or Ts is to be read out. When the value is read out, the second read-out can be displayed by briefly pressing the lower button.

When a display is to be connected to the built-in MODBUS, the display can advantageously be changed to one of the same type, but with Index A (version with screw terminals).

The controllers address must be set higher than 0 in order for the display to be able to communicate with the controller.

*[Figurtekst: 100% · 0% · tamb - Ts · CCH on CCH off · diff diff · L · DI1 DI2 · LP · HP · DI3 · N · N · MODBUS · LON · MOD RS · LON · Max. 15 m Max. 1000 m · MOD · Address o03 > 0 · Function via data communication Day/Night schedule · Function in gateway/system manager Day/Night control / Time schedule · Used parameters in  Optyma™  Plus --- Night setback]*

If connection of two displays is required, one must be connected to the plug (max. 15 m) and the other must then be connected to the fixed data communication.

#### **Override**

The controller contains a functions which can be used together with the override function in the master gateway/system manager.

### **Survey of functions**

|**Function**|**Para-**<br>**meter**|**Parameter by operation via data**<br>**communication**|
|---|---|---|
|**Normal display**|||
|The display shows the temperature value for the suction pressure Ts or from the condensing<br>pressure Tc. Enter which of the two are to be displayed in o17.<br>During operation, when one of the two is shown in the display, the other value can be seen<br>by pressing and holding in the lower button.<br>||Ts / Tc<br>|
|**Thermostat**||**Thermostat control**|
|**Set point**<br>The controller's reference Tc is the outside temperature + set point + any applicable offset.<br>Enter the setpoint by pressingthe middle button. A offset can be entered in r13.||Reference|
|**Unit**<br>Set here if the display is to show SI-units or US-units<br>0: SI (°C and bar)<br>1: US (°F and Psig).|r05|Unit<br>°C=0. / °F=1<br>(Only °C on AKM, whatever the setting)|
|**Start / stop of refrigeration**<br>With this setting refrigeration can be started, stopped or a manual override of the outputs<br>can be allowed. (For manual control the value is set at -1. Then the relay outlets can be force-<br>controlled by the respective reading parameters (u58, u59 etc.). Here the read value can be<br>overwritten.)|r12|Main Switch<br>1: Start<br>0: Stop<br>-1: Manual control of outputs allowed|
|Start / stop of refrigeration can also be accomplished with the external switch function<br>connected to a DI input.|||
|If the external switch function is deselected, the input must be shorted.<br>Stopped refrigeration will give a ”Standby alarm”.|||
|**Night setback value**<br>The controller reference is raised by this value when the controller switches to night<br>operation.|r13|Night offset|
|**Reference Ts**<br>Here the reference is entered for the suction pressure Ts in degrees(only for Optyma**™**Plus<br>inverter)|r23|Ts Ref|
|**Reference Tc**<br>Here the current controller reference for condensing pressure Tc can be read out in degrees.|r29|Tc Ref|
|**External heating function**<br>Thermostat cut-in value for an external heating element (only when 069=2 and o40=1)<br>The relay activates when the temperature reaches the set value. Relay releases again when<br>the temperature has increased by5 K(the difference is set at 5 K).|r71|AuxTherRef|
|**Minimum condensing temperature**(lowest permitted regulation reference)<br>Here the lowest permitted reference is entered for the condensing temperature Tc.|r82|MinCondTemp|
|**Maximum condensing temperature**(highest permitted regulation reference)<br>Here the highest permitted reference is entered for the condensing temperature Tc.|r83|MaxCondTemp|
|**Maximum discharge  gas temperature**<br>Here the highest permitted discharge gas temperature is entered. The temperature is<br>measured by sensor Td. If the temperature is exceeded, the fan will be started at 100%. A<br>timer is also started which can be set in c72. If the timer setting runs out, the compressor will<br>be stopped and an alarm will be issued. The compressor will be reconnected 10 K below the<br>cut-out limit,but onlyafter the compressor's off timer has expired.|r84|MaxDischTemp|
|||Night setbck<br>(start of night signal.  0=Day, 1=Night)|
|**Alarm**||**Alarm settings**|
|The controller can give alarm in different situations. When there is an alarm all the light-<br>emitting diodes (LED) will flash on the controller front panel, and the alarm relay will cut in.||With data communication the<br>importance of the individual alarms<br>can be defined. Setting is carried out in<br>the “Alarm destinations” menu via AKM.|
|**Delay of a DI2 alarm**<br>A cut-out/cut-in input will result in alarm when the time delay has been passed. The function<br>is defined in o37.|A28|AI.Delay DI2|
|i<br>**High condensing temperature alarm limit**<br>The limit for the condensing temperature, set as difference above the instant reference<br>(parameter r29), at which the A80 Alarm is activated after expired delay (see parameter A71).<br>Parameter is set in Kelvin .|A70|Air flowDiff|
|Delaytime for alarm A80 - see alsoparameter A70. Set in minutes.|A71|Air flow del|
|||Reset alarm<br>Ctrl. Error|

6 | BC172686425380en-001201

|**Compressor**<br>i||**Compressor control**|
|---|---|---|
|The start/stop of the controller can be defined in several ways.<br>Internal only: Here, only the internal main switch in r12 is used.<br>External: Here, input DI1 is used as a thermostat switch. With this setting, input DI2 can be<br>defined as an 'external safety' mechanism that can stopthe compressor.|||
|**Running times**<br>To prevent irregular operation, values can be set for the time the compressor is to run once it<br>has been started. And for how long it at least has to be stopped.|||
|Min. ON-time (in seconds)|c01|Min. On time|
|Min. OFF-time (in seconds)|c02|Min. Off time|
|**Minimum time between cut-in of relay **(in minutes)|c07|Restart time|
|**Pump down Limit**<br>Pressure value at which the compressor stops|c33|PumpDownLim|
|**Compressor min. speed**<br>Here the minimum allowable speed for the compressor is set.|c46|CmpMinSpeed|
|**Compressor start speed**<br>The compressor will not start before the required speed can be achieved|c47|CmpStrSpeed|
|**Compressor max. speed**<br>Upper limit for compressor speed|c48|CmpMaxSpeed|
|**Compressor max. speed during night operation**<br>Upper limit for compressor speed during night operation. During night operation, the c48<br>value is reduced to thepercentage value set here|c69|CmpMax % Ngt|
|**Definition of compressor control mode**<br>0: No compressor - Condensing unit OFF<br>1: Fixed speed - Input DI1 used to start / stop of fixed speed compressor<br>2: Variable speed - Input DI1 used for start / stop of variable speed-controlled compressor<br>with a 0 – 10 V signal on AO2|c71|Comp mode|
|**Delay time for high discharge  gas temperature**(in minutes)<br>When sensor Td records a temperature higher than the limit value entered in r84, the timer<br>will start. When the delay time expires, the compressor will be stopped if the temperature is<br>still too high. An alarm will also be issued.|c72|Disch. Del|
|**Max. pressure (Max. condensing pressure)**<br>The maximum permitted condensing pressure is set here. If the pressure increases, the<br>compressor will be stopped.|c73|PcMax|
|**Difference  for max. pressure (Condensing pressure)**<br>Difference for re-start of compressor if it is cut out due to PcMax.<br>(All timers must expire before re-start is permitted)|c74|Pc Diff|
|**Minimum suction pressure**<br>Enter the lowest permitted suction pressure here. The compressor is stopped if the pressure<br>drops below the minimum value.|c75|PsLP|
|**Suction pressure difference**<br>Difference for re-start of compressor if it is cut out due to PsLP.<br>(All timers must expire before re-start ispermitted)|c76|PsDiff|
|**Amplification factor Kp for compressor regulation**<br>If the Kpvalue is lowered, the regulation will be slower|c82|Cmp Kp|
|**Integration time Tn for compressor regulation**<br>If the Tn value is increased, regulation will run more smoothly|c83|Comp Tn sec|
|**Liquid Injection Offset**<br>The liquid injection relay is activated when the temperature is over “r84” minus “c88” (but<br>only if the compressor is running).|c88|LI Offset|
|**Liquid Injection hysterese**<br>The liquid injection relay is then deactivated when the temperature has dropped to “r84”<br>minus “c88” minus “c89”.|c89|LI Hyst|
|**Compressor stop delay after Liquid injection**<br>Compressor ON-time after relay "Aux relay" is went OFF|c90|LI Delay|
|Desired compressor speed in connection with pressure transmitter faults.<br>Speed during emergency operation.|c93|CmpEmrgSpeed|
|Min On time during Low Ambient Temperature and Low Pressure|c94|c94 LpMinOnTime|
|Measured Tc for which the Comp min speed is raised to StartSpeed|c95|c95 TcSpeedLim|
|The LED on the controller’s front will show whether refrigeration is in progress.|||

|**Fan**<br>**i**||**Fan control**<br>|
|---|---|---|
|**Amplification factor Kp**<br>If the KP value is lowered,the fan speed will change.|n04|Kp factor|
|**Integration Time Tn**<br>If the Tn value is increased,the fan speed will change.|n05|Tn sec|
|**Amplification factor Kp max**<br>The regulation uses this Kp, when the measured value is far from reference|n95|Cmp kp Max|
|**Fan speed**<br>The actual fan speed is read out here as a % of nominal speed.|F07|Fan Speed %|
|**Change in fan speed**<br>A permitted change in fan speed can be entered for when the fan speed is to be lowered.<br>The settingcan be entered as apercentage valueper second.|F14|DownSlope|
|**Jog speed**<br>Set the fan's start-up speed here. After ten seconds the function jog function will stop and<br>the fan speed will then be controlled bythe normal regulation.|F15|Jog Speed|
|**Jog speed at low temperatures**<br>Enter the desired jog speed for outside temperatures of -20 °C and lower here.<br>(For outside temperatures between +10 and -20, the controller will calculate and utilise a<br>speed between the twojogsettings.)|F16|LowTempJog|
|**Fan control definition**<br>f|F17|FanCtrlMode|
|0: Off<br>1: The fan is connected to terminal 5-6 and is speed-controlled by an internal phase cut. The<br>relay on terminal 15-16 connects at speed requirements of 95% or higher.<br>2: The fan is connected to an external speed control device. The speed control signal is<br>connected to terminals 28-29. The relay on terminal 15-16 will connect when regulation is<br>required.(Duringexternal control,the settings F14,F15 and F16 will remain in force)|||
|**Minimum fan speed**<br>Set the lowest permitted fan speed here. The fan will be stopped if the user enters a lower<br>speed.|F18|MinFanSpeed|
|**Maximum fan speed**<br>The fan's top speed can be limited here. The value can be entered by setting the nominal<br>speed of 100% to the desiredpercentage.|F19|MaxFanSpeed|
|**Manual fan speed control**<br>An override of the fan speed control can be performed here. This function is only relevant<br>when the main switch is in service mode.|F20|Manual Fan %|
|Phase compensation<br>The value minimises the electrical noise emitted during phase control. The value<br>should only be changed by specially trained staff.|F21|Fan Comp|
|The condenser fan will pre-ventilate the compressor compartment  to ensure a safe<br>environment before compressor start on selected A2L-refrigerants via o30|F23|FanVent Time|
|The LED on the controller’s front will show whether Fan is in progress supplied either<br>through fan speed control output or fan relay.|||
|**Real time clock**|||
|When using data communication the clock is automatically adjusted by the system unit. If<br>the controller is without data communication, the clock will have a power reserve of four<br>hours.||(Times cannot be set via data<br>communication. Settings are only<br>relevant when there is no data<br>communication).|
|**Switch to day operation**<br>Enter the time at which the control reference becomes the entered setpoint.|t17|Day start|
|**Change to night operation**<br>|t18|Night start|
|Enter the time at which the control reference is raised with r13.|||
|Clock: Hour setting|t07||
|Clock: Minute setting|t08||
|Clock: Date setting|t45||
|Clock: Month setting|t46||
|Clock: Year setting|t47||
|**Miscellaneous**||Miscellaneous|
|If the controller is built into a network with data communication, it must have an address, and<br>the system unit of the data communication must then know this address.|||
|The address is set between 0 and 240, depending on the system unit and the selected data<br>communication.|o03||
|The function is not used when the data communication is MODBUS. It is retrieved here via<br>the system's scan function.|o04||

8 | BC172686425380en-001201

|**Access code 1 (Access to all settings)**<br>If the settings in the controller are to be protected with an access code you can set a<br>numerical value between 0 and 100. If not, you can cancel the function with setting 0 (99 will<br>alwaysgiveyou access).|o05|Acc. code|
|---|---|---|
|**Controller software version**|o08|SW ver|
|**Select signal for the display**<br>Here you define the signal to be shown by the display.<br>1: Suction pressure in degrees, Ts.|o17|Display mode|
|<br>2: Condensing pressure in degrees,Tc.|||
|**Pressure transmitter settings for Ps**<br>Working range for pressure transmitter-min. value|o20|MinTransPs|
|<br>**Pressure transmitter settings for Ps**<br>Working range for pressure transmitter-max. value|o21|MaxTransPs|
|<br>**Refrigerant setting**(only if "r12" = 0)<br>Before refrigeration is started, the refrigerant must be defined. You may choose between the<br>followin refrierants|o30|Refrigerant|
|g g<br>2=R22.  3=R134a. 13=User defined. 17=R507. 19=R404A. 20=R407C. 21=R407A. 36=R513A.<br>37=R407F. 40=R448A.  41=R449A. 42=R452A. 39=R1234yf. 51=R454C. 52=R455A<br>|||
|Warning: Wrong selection of refrigerant may cause damage to the compressor.<br>Other refrigerants: Here setting 13 is selected and then three factors -Ref.Fac a1, a2 and a3 -<br>via AKM must be set.|||
|**Digital input signal - DI2**<br>The controller has a digital input 2 which can be used for one of the following functions:|o37|DI2 config.|
|0: The input is not used.<br>1: Signal from a safety circuit (short-circuited =ok for compressor operation). Disconnected =<br>compressor stop and A97 alarm).<br>2: Main switch. Regulation is carried out when the input is short-circuited, and regulation is<br>stopped when the input is put in pos. OFF.<br>3: Night operation. When the input is short-circuited, there will be regulation for night<br>ti|||
|operaon.<br>4: Separate alarm function. Alarm will be given when the input is short-circuited.<br>5: Separate alarm function. Alarm will be given when the input is opened.<br>6: Input status, on or off (DI2 status can be tracked via data communication).<br>7: Alarm from the compressor's external speed control.<br>|||
|**Aux relay function**<br>0: The relay is not used|o40|AuxRelayCfg|
|<br>1: External heating element (temperature setting in r71, sensor definition in 069)<br>2: Used for liquid injection (temperature setting in r84)|||
|<br>3: Oil return management function must activate the relay<br>|||
|**Pressure transmitter settings for PC**<br>Working range for pressure transmitter-min. value|o47|MinTransPc|
|<br>**Pressure transmitter settings for PC**<br>Working range for pressure transmitter-max. value|o48|MaxTransPc|
|<br>**Select the type of condensing unit.**<br>|o61|Unit type|
|Factory set.<br>After the first setting, the value is 'locked' and can only be changed once the controller has<br>been reset to its factory setting.|||
|When entering the refrigerant setting, the controller will ensure that the 'Unit type' and|||
|<br>refrigerant are compatible.|||
|**S3 Configuration**<br>|o63|S3 config|
|0 = S3 input not used|||
|1 = S3 input used for measuringof discharge temperature|||
|**Save as factory setting**|o67|-|
|<br>With this setting you save the controller’s actual settings as a new basic setting (the earlier<br>factorysettings are overwritten).|||
|**Define the use of the Taux sensor (S5)**<br>0 Nt d|o69|Taux Config|
|: o use<br>1: Used to measure oil temperature|||
|<br>2: Used to measure the temerature of the external heatin function|||
|p    g<br>3: Other use. Measuringof optional temperature|||
|**Period time for heating element in crankcase**<br>Within this period the controller will itself calculate an OFF and ON period.<br>The time is entered in seconds.|P45|PWM Period|
|**Difference for the heating elements 100% ON point**<br>The difference applies to a number of degrees below the 'Tamb minus Ts = 0 K' value|P46|CCH_OnDiff|
|**Diff f th hti lt fll OFF it**|P47|CCHOffDiff|
|**ference or e eang eemens u  pon**<br>The difference applies to a number of degrees above the 'Tamb minus Ts = 0 K' value||_ff|

|**Operating time for condensing unit**<br>The condensing unit's operating time can be read out here. The read-out value must be<br>multiplied by 1,000 in order to obtain the correct value.<br>(The displayed value can be adjusted if required)|P48|Unit  Runtime|
|---|---|---|
|**Operating time for the compressor**<br>The compressors operating time can be read out here. The read-out value must be multi-<br>plied by 1,000 in order to obtain the correct value.<br>(The displayed value can be adjusted if required)|P49|Comp Runtime|
|**Operating time for heating element in crankcase**<br>The heating element's operating time can be read out here. The read-out value must be<br>multiplied by 1,000 in order to obtain the correct value (the displayed value can be adjusted<br>if required).|P50|CCH Runtime|
|**Number of HP alarms**<br>The number of HP alarms can be read out here<br>(the displayed value can be adjusted if required).|P51|HP Alarm Cnt|
|**Number of LP alarms**<br>The number of LP alarms can be read out here<br>(the displayed value can be adjusted if required).|P52|LP Alarm Cnt|
|**Number of discharge alarms**<br>The number of Td alarms can be read out here<br>(the displayed value can be adjusted if required).|P53|DisAlarm Cnt|
|**Number of blocked condenser alarms**<br>The number of blocked condenser alarms can be read out here<br>(the displayed value can be adjusted if required).|P90|BlckAlrm Cnt|
|**Oil return management Speed limit**<br>If the compressor speed exceeds this limit, a time counter will be increased. It will be<br>decreased if the compressor speed falls down below this limit.|P77|ORM SpeedLim|
|**Oil return management time**<br>Limit value of the above described time counter. If the counter exceeds this limit, the<br>compressor speed will be raised to the boost speed.|P78|ORM Time|
|**Oil return management Boost speed**<br>This compressor speed ensures that the oil returns to the compressor|P79|ORM BoostSpd|
|**Oil return management Boost time.**<br>The time the compressor must operate at Boost speed|P80|ORM BoostTim|
|**Service**||**Service**|
|Readpressure Pc|u01|Pc bar|
|Read temperature Taux|u03|T_aux|
|Status on DI1 input. On/1=closed|u10|DI1 status|
|Status on night operation (on or off) on =night operation|u13|NightCond|
|Read Superheat|u21|Superheat SH|
|Read temperature at S6 sensor|u36|S6 temp|
|Read the compressor capacityin %|u52|CompCap%|
|Status on DI2 input. On/1=closed|u37|DI2 status|
|Status on relayfor compressor|u58|CompRelay|
|Status on relayfor fan|u59|Fan relay|
|Status on relayfor alarm<br>|u62|Alarm relay<br>|
|Status on relay"Aux"|u63|Aux Relay|
|Status on relayfor heatingelement in crankcase|u71|CCH Relay|
|Status on input DI3 (on/1 = 230 V)|u87|DI3 status|
|Read condensing pressure in temperature|U22|Tc|
|Readpressure Ps|U23|Ps|
|Read suctionpressure in temperature|U24|Ts|
|Read ambient temperature Tamb|U25|T_ambient|
|Read discharge temperature Td|U26|T_Discharge|
|Read suctiongas temperature at Ts|U27|T_Suction|
|Voltage on the analogue output AO1|U44|AO_1 Volt|
|Voltage on the analogue output AO2|U56|AO_2 Volt|

10 | BC172686425380en-001201

|**Operating status**||**(Measurement)**|
|---|---|---|
|The controller goes through some regulating situations where it is just waiting for the next<br>point of the regulation. To make these “why is nothing happening” situations visible, you<br>can see an operating status on the display. Push briefly (1s) the upper button. If there is a<br>status code, it will be shown on the display. The individual status codes have the following<br>meanings:||Ctrl. state:|
|Normal regulation|S0|0|
|When the compressor is operatingit must run for at least x minutes.|S2|2|
|When the compressor is stopped, it must remain stopped for at least x minutes.|S3|3|
|Refrigeration stopped bymain switch. Either with r12 or a DI-input|S10|10|
|Manual control of outputs|S25|25|
|No refrigerant selected|S26|26|
|Safetycut-out Max. condensing pressure exceeded. All compressors stopped.|S34|34|
|Other displays:|||
|Password required.  Setpassword|PS||
|Regulation is stopped  via main switch|OFF||
|No refrigerant selected|ref||
|No type has been selected for the condensingunit.|typ||

#### **Fault messa** **g e**

In an error situation the LED’s on the front will flash and the alarm relay will be activated. If you push the top button in this situation you can see the alarm report in the display.

There are two kinds of error reports - it can either be an alarm occurring during the daily operation, or there may be a defect in the installation. A-alarms will not become visible until the set time delay has expired. E-alarms, on the other hand, will become visible the moment the error occurs. (An A alarm will not be visible as long as there is an active E alarm). Here are the messages that may appear:

|**Code / Alarm text via data**<br>**communication**|**Description**|**Action**|
|---|---|---|
|A2/---  LP alarm|Low suction pressure|See instructions for the condensing unit|
|A11/--- No Rfg. sel.|No refrigerant selected|Set o30|
|A16 /--- DI2 alarm|DI2 alarm|Check the function that sends a signal at the DI2 input|
|A17 / ---HP Alarm|C73 / DI3 Alarm  (High / low pressure alarm)|See instructions for the condensing unit|
|A45 /--- Standby mode|Standby position (stopped refrigeration via r12 or DI1-input)|r12 and/or DI1 input will start the regulation|
|A80 / --- Cond. blocked|Air flow has decreased.|Clean the condensing unit|
|A96 / --- Max Disc. Temp|Discharge gas temperature is exceeded|See instructions for the condensing unit|
|A97 / --- Safety alarm|Safety function on DI2 or DI 3 is activated|Check the function that sends a signal at the DI2 or DI3<br>input and the direction of rotation of the compressor|
|A98 / --- Drive alarm|Alarm from speed regulation|Check speed regulation|
|E1 /---  Ctrl. Error|Faults in the controller||
|E20 /--- Pc Sensor Err|Error on pressure transmitter Pc||
|E30 /--- Taux Sensor Err|Error on Aux sensor, S5||
|E31/---Tamb Sensor Err|Error on air sensor, S2|Check sensor and connection|
|E32 / ---Tdis Sensor Err|Error on discharge sensor, S3||
|E33 / ---Tsuc Sensor Err|Error on suction gas sensor, S4||
|E39/--- Ps Sensor Err|Error on pressure transmitter Ps||
|**Data communication**|||

|<br>The importance of indiv    i|<br>idual alarms can be defined with|i  a setting. The|i     setting must|<br>i       be carried out|i          in the group "A|<br>i             larm destinations"|
|---|---|---|---|---|---|---|
|Settings from|Settings from|Log||Alarm relay||Send via|
|System manager|AKM (AKM destination)||Non|High|Low-High|Network|
|High|1|X||X|X|X|
|Middle|2|X|||X|X|
|Low|3|X|||X|X|
|Log only||X|||||
|Disabled|||||||

### **Operation**

#### **Display**

The values will be shown with three digits, and with a setting you can determine whether the temperature is to be shown in °C or in °F.

#### **Light-emitting diodes (LED) on front panel**

The LED’s on the front panel will light up when the relevant relay is activated.

- = Refrigeration

- = heating element in crankcase is on

Cutout alarm relay / receipt alarm/see alarm code

- A short press of the upper button

- If there are several alarm codes they are found in a rolling stack. Push the uppermost or lowermost button to scan the rolling stack.

#### Set point

1. Push the middle button until the temperature value is shown

2. Push the upper or the lower button and select the new value

3. Push the middle button again to conclude the setting.

Reading the temperature at Ts (if Tc is the primary display) or Tc (if Ts is the primary display)

   - A short press of the lower button

- =  Fan running

The light-emitting diodes will flash when there is an alarm. In this situation you can download the error code to the display and cancel/sign for the alarm by giving the upper button a brief push.

#### **The buttons**

When you want to change a setting, the upper and the lower button will give you a higher or lower value depending on the button you are pushing. But before you change the value, you must have access to the menu. You obtain this by pushing the upper button for a couple of seconds - you will then enter the column with parameter codes. Find the parameter code you want to change and push the middle buttons until value for the parameter is shown. When you have changed the value, save the new value by once more pushing the middle button. (If not operated for 20 (5) seconds, the display will change back to the Ts/Tc temperature display).

#### **Get a good start**

With the following procedure you can start regulation very quickly:

- **1** Open parameter r12 and stop the regulation (in a new and not previously set unit, r12 will already be set to 0 which means stopped regulation.

- **2** Select refrigerant via parameter o30

- **3** Open parameter r12 and start the regulation. Start/stop at input DI1 or DI2 must also be activated.

- **4** Go through the survey of factory settings. Make any necessary changes in the respective parameters.

- **5** For network.

- Set the address in o03

- Activate scan function in the system manager.

#### Examples

#### Set menu

1. Push the upper button until a parameter r05 is shown

2. Push the upper or the lower button and find that parameter you want to change

3. Push the middle button until the parameter value is shown

4. Push the upper or the lower button and select the new value

5. Push the middle button again to freeze the value.

#### Note

When delivering the condensing unit, the controller will be set to the condensing unit type (setting o61). This setting will be compared with your refrigerant setting. If you select a "nonpermitted refrigerant", the display will show "ref" and await a new setting.

(In the event of a controller change, 061 must be set as indicated in the instructions from Danfoss)

12 | BC172686425380en-001201

|**Menu survey**||||||SW = 3.7x|
|---|---|---|---|---|---|---|
|**Parameter**|||||||
|**Function**||Code|**Min. value**|**Max. value**|**Factory**<br>**setting**|**Actual**<br>**setting**|
|**Normal operation**|||||||
|Set point (regulation reference follows the number of degrees above the outside temperature<br>Tamb)||- - -|2.0 K|20.0 K|8.0 K||
|**Regulation**|||||||
|Select SI or US display. 0=SI (bar and °C). 1=US (Psigand °F)||r05|0/°C|1/F|0/°C||
|Internal Main Switch. Manual and service = -1, Stopregulation = 0, Start regulation =1||r12|-1|1|0||
|Offset duringnight operation. Duringnight operation the reference is raised bythis value||r13|0 K|10 K|2 K||
|Setpoint for suctionpressure Ts(onlyfor Optyma**™**Plus inverter)||r23|-30 °C|10 °C|-7 °C||
|Readout of reference for Tc||r29||||-|
|Thermostat cut-in value for an external heatingelement (069=2 and o40=1)||r71|-30,0 °C|30,0 °C|-25 °C||
|Min. condensingtemperature (lowestpermitted Tc reference)||r82|0 °C|40 °C|25 °C||
|Max. condensingtemperature (highestpermitted Tc reference)||r83|20 °C|50 °C|40 °C||
|Max. dischargegas temperature Td||r84|50 °C|140 °C|125 °C||
|**Alarms**|||||||
|Alarm time delayon signal on the DI2 input. Active onlyif o37=4 or 5.||A28|0 min.|240 min.|30 min.||
|Alarm for insufficient coolingin condenser. Temperature difference 30.0 K = Alarm disabled||A70|3.0 K|30.0 K|10.0 K||
|Delaytime for A80 alarm. See alsoparameter A70.||A71|5 min.|240 min.|30 min.||
|**Compressor**|||||||
|Min. ON-time||c01|1 s|240 s|5 s||
|Min. OFF-time||c02|3 s|240 s|120 s||
|Min. time between compressor starts||c07|0 min.|30 min.|5 min.||
|Pumpdown limit at which the compressor is stopped (setting0.0 = no function)|***|c33|0,0 bar|6,0 bar|0,0 bar||
|Min. compressor speed||c46|25 Hz|70 Hz|30 Hz||
|Start speed for compressor||c47|30 Hz|70 Hz|50 Hz||
|Max. compressor speed||c48|50 Hz|100 Hz|100 Hz||
|Max. compressor speed duringnight operation (%-value of c48)||c69|50%|100%|70%||
|Definition of compressor control mode|*|c71|0|2|1||
|0: No compressor - Condensing unit OFF<br>1: Fixed speed - Input DI1 used to start / stop of fixed speed compressor<br>2: Variable speed - Input DI1 used for start / stop of variable speed-controlled compressor<br>with a 0 – 10 V signal on AO2|||||||
|Time delayfor high Td. The compressor will stopwhen time expires.||c72|0 min.|20 min.|1 min.||
|Max.pressure. Compressor stops if a higherpressure is recorded|***|c73|7,0 bar|31,0 bar|23,0 bar||
|Difference for max.pressure (c73)||c74|1,0 bar|10,0 bar|3,0 bar||
|Min. suctionpressure Ps. Compressor stops if a lowerpressure is recorded|***|c75|-0,3 bar|6,0 bar|1,4 bar||
|Difference for min. suctionpressure andpumpdown||c76|0,1 bar|5,0 bar|0,7 bar||
|Amplification factor Kp for compressors PI-regulation||c82|3,0|30,0|20,0||
|Integration time Tn for compressors PI-regulation||c83|30 s|360 s|60 s||
|Liquid Injection Offset||c88|0,1 K|20,0 K|5,0 K||
|Liquid Injection hysterese||c89|3,0 K|30,0 K|15,0 K||
|Compressor stopdelayafter Liquid injection||c90|0 s|10 s|3 s||
|Desired compressor speed if the signal from thepressure transmitter Ps fails||c93|25 Hz|70 Hz|60 Hz||
|Min On time duringLow Ambient LP||c94|0 s|120 s|0 s||
|Measured Tc for which the Compmin speed is raised to StartSpeed||c95|10,0 °C|70,0 °C|50,0 °C||
|**Control parameters**|||||||
|Amplification factor Kpfor PI-regulation||n04|1.0|20.0|7.0||
|Integration time Tn for PI-regulation||n05|20|120|40||
|Kpmax for PI regulation when the measurement is far from reference||n95|5,0|50,0|20,0||
|**Fan**|||||||
|Readout of fan speed in %||F07|-|-|-||
|Permitted change in fan speed(to a lower value)%per second.||F14|1,0%|5,0%|5,0%||
|Jogspeed(speed as a % when the fan is started)||F15|40%|100%|40%||

|**continued**||**Code**|**Min.**|**Max.**|**Fac.**|**Actual**|
|---|---|---|---|---|---|---|
|Jogspeed at low temperature||F16|0%|40%|10%||
|Definition of fan control: 0=Off;Internal control(AC Fan);External speed control(EC Fan)||F17|0|2|1||
|i    f<br>Minimum fan speed. Decreased need will stopthe fan.||F18|0%|40%|10%||
|Maximum fan speed||F19|40%|100%|100%||
|Manual control of the fan's speed.(Onlywhen r12 is set to -1)|**|F20|0%|100%|0%||
|Phase compensation(should onlybe changed byspeciallytrainedpersonnel.)||F21|0|50|20||
|Pre-Ventilation time on A2L-refrigerants before compressor start||F23|30|180|30||
|**Real time clock**|||||||
|Time at which theyswitch to dayoperation<br>||t17|0 hrs<br>|23 hrs<br>|0||
|Time at which theyswitch to night operation||t18|0 hrs|23 hrs|0||
|Clock - Setting of hours||t07|0 hrs|23 hrs|0||
|Clock - Setting of minute||t08|0 min.|59 min.|0||
|Clock - Setting of date||t45|1 day|31 days|1||
|Clock - Setting of month||t46|1 mon.|12 mon.|1||
|Clock - Setting of year||t47|0year|99years|0||
|**Miscellaneous**|||||||
|Network address||o03|0|240|0||
|On/Off switch (Service Pin message)||o04|0/Off|1/On|0/Off||
|IMPORTANT! o61**must**be set prior to o04<br>(used at LON 485 only)|||||||
|Access code(access to all settings)||o05|0|100|0||
|Readout of controllers software version||o08|||||
|Select signal for display view.  1=Suction pressure in degrees, Ts. 2=Condensing pressure in||o17|1|2|1||
|degrees,Ts|||||||
|Pressure transmitter workingrange Ps - min. value||o20|-1 bar|5 bar|-1||
|Pressure transmitter workingrange Ps- max. value||o21|6 bar|200 bar|12||
|Refrigerant setting:<br>2=R22. 3=R134a. 13=User defined. 17=R507. 19=R404A. 20=R407C. 21=R407A. 36=R513A.<br>37=R407F. 40=R448A. 41=R449A. 42=R452A. 39=R1234yf. 51=R454C. 52=R455A|*|o30|0|42|0||
|Input signal on DI2. Function:<br>(0=not used, 1=External safety function. Regulate when closed, 2=external main switch,<br>3=Night operation when closed, 4=alarm function when closed, 5=alarm function when<br>open.  6=on/off Status for monitoring. 7=Alarm from speed regulation||o37|0|7|0||
|Aux relay function:|***|o40|0|3|1||
|(0=not used,1=External heatingelement,2=liquid injection,3=oil return function)|||||||
|Pressure transmitter workingrange Pc – min. value||o47|-1 bar|5 bar|0 bar||
|Pressure transmitter workingrange Pc – max. value||o48|6 bar|200 bar|32 bar||
|Setting of condensing unit type (is factory set when the controller is mounted and cannot be<br>subsequentlychanged)|*|o61|0|77|0||
|The sensor input S3 is to be used to measure the dischargegas temperature (1=yes)||o63|0|1|1||
|Replace the controllers factorysettings with thepresent settings||o67|Off (0)|On (1)|Off (0)||
|Defines the use of the Taux sensor: 0=not used; 1=measuring of oil temperature;||o69|0|3|0||
|2=measurement from external heat function 3=other optional use|||||||
|Period time for heatingelement in crankcase(ON + OFFperiod)||P45|30 s|255 s|240 s||
|Difference for heatingelements 100% ONpoint||P46|-20 K|-5 K|-10 K||
|Difference for heatingelements 100% OFFpoint||P47|5 K|20 K|10 K||
|Read-out of operating time for condenser unit. (Value must be multiplied by 1,000). The value||P48|-|-|0 h||
|can be adjusted.|||||||
|Read-out of compressor operating time. (Value must be multiplied by 1,000). The value can||P49|-|-|0 h||
|be adjusted.|||||||
|Read-out of operating time of heating element in crankcase. (Value must be multiplied by<br>1,000). The value can be adjusted.||P50|-|-|0 h||
|Read-out of number of HP alarms. The value can be adjusted.||P51|-|-|0||
|Read-out of number of LP alarms. The value can be adjusted.||P52|-|-|0||
|Read-out of number of Td alarms. The value can be adjusted.||P53|-|-|0||
|Read-out of number of blocked condenser alarms. The value can be adjusted||P90|-|-|0||
|<br>Oil return management. Compressor speed for the counter starting point||P77|25 Hz|70 Hz|40 Hz||

14 | BC172686425380en-001201

|**continued**|**Code**|**Min.**|**Max.**|**Fac.**|**Actual**|
|---|---|---|---|---|---|
|Oil return management. Limit value for counter|P78|5 min.|720 min.|20 min.||
|Oil return management. Boost-speed|P79|40 Hz|100 Hz|50 Hz||
|Oil return management. Boost-time.|P80|10 s|600 s|60 s||
|**Service**||||||
|Readoutpressure on Pc|u01|bar||||
|Readout temperature Taux|u03|°C||||
|Status on DI1 input. 1=on=closed|u10|||||
|Status on night operation (on or off) 1=on=night operation|u13|||||
|Readout superheat|u21|K||||
|Readout temperature at S6 sensor|u36|°C||||
|Status on DI2 input. 1=on=closed|u37|||||
|Readout the compressor capacityin %|u52|%||||
|Status on relayto compressor. 1=on=closed|**<br>u58|||||
|Status on relayto fan. 1=on=closed|**<br>u59|||||
|Status on relayto alarm. 1=on=closed|**<br>u62|||||
|Status on relay"Aux". 1=on=closed|**<br>u63|||||
|Status on relayto heatingelement in crank case. 1=on=closed|**<br>u71|||||
|Status on high voltage input DI3. 1=on=230 V|u87|||||
|Readout condensing pressure in temperature|U22|°C||||
|Readout pressure Ps|U23|bar||||
|Readout suction pressure in temperature|U24|°C||||
|Readout ambient temperature Tamb|U25|°C||||
|Readout discharge temperature Td|U26|°C||||
|Readout suction gas temperature Ts|U27|°C||||
|Readout the voltage on the output AO1|U44|V||||
|Readout the voltage on the output AO2|U56|V||||

*) Can only be set when regulation is stopped (r12=0)

**) Can be controlled manually, but only when r12=-1

***) This parameter depends on parameter o30 and o61 settings

##### Factory setting

If you need to return to the factory-set values, it can be done in this way:

- Cut out the supply voltage to the controller

- Keep upper and lower button depressed at the same time as you reconnect the supply voltage

#### **Reset of unit statistics parameters**

All the Unit status parameters (P48 to P53 and P90) can be set / cleared using the following procedure

- Set Main Switch to 0

- Change the Statistics parameters - like setting Alarm counters to 0

- Wait 10 seconds - to ensure write to EEROM

- Make a repower of the Controller - transfer new settings to "statistics function"

- Set Main Switch ON - and the parameters is set to the new value

### **Connections**

*[Figurtekst: AKS32R AKS32R - + - + · 24 25 26 27 28 29 30 31 32 33 34 35 36 373839 4041 4243 51 52 53 54 55 56 57 60 61 62 · S2 S3 S4 S5 S6 · DI1 DI2 Pc Ps EKA RS AO1 AO2 MODBUS · Display 485 · FAN · Alarm Comp CCH Fan Aux · L N DI3 · 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 22 23 · LP · HP · 230 V 230 V 230 V 230 V 230 V 230 V 230 V 230 V · 0 – 10 V 0 – 10 V · R=120 Ω R=120 Ω]*

#### **DI1**

Digital input signal. Used to start/stop cooling (room thermostat) Starts when the input is short-circuited.

#### **AO1, terminal 54, 55**

Output signal, 0 – 10 V. Must be used if the fan is equipped with internal speed control and 0 – 10 V DC input, e.g. EC-motor.

#### **AO2, terminal 56, 57**

#### **DI2**

Digital input signal.

The defined function is active when the input is short-circuited/ opened. The function is defined in o37.

Output signal, 0 – 10 V. Must be used if the compressor is speed controlled.

#### **MODBUS (terminal 60, 61, 62)**

Built in Modbus data communication.

#### **Pc**

Pressure transmitter, ratiometric AKS 32R, 0 to 32 bar Connect to terminal 28, 29 and 30.

#### **Ps**

Pressure transmitter, ratiometric e.g. AKS 32R, -1 to 12 bar Connected to terminal 31, 32 and 33.

#### **S2**

Air sensor, Tamb. Pt 1000 ohm sensor, eg. AKS 11

#### **S3**

Discharge gas sensor, Td. Pt 1000 ohm sensor, eg. AKS 21

#### **S4**

Suction gas temperature, Ts. Pt 1000 ohm sensor, eg. AKS 11

If data communication is used, it is important that the installation of the data communication cable is performed correctly. See separate literature No. RC8AC… (Alternatively the terminals can be connected to an external display type EKA 163A or 164A, but then they cannot be used for data communication. Any data communication must then be carried out by one of the other methods.)

#### **Supply voltage**

230 V AC (This must be the same phase for all 230 V connections).

#### **FAN**

Fan connection. Speed controlled internally.

#### **Alarm**

There is a connection between terminal 7 and 8 in alarm situations and when the controller is without power.

#### **S5,**

Extra temperature measurement, Taux. Pt 1000 ohm sensor, eg. AKS 11

#### **Comp**

Compressor. There is a connection between terminal 10 and 11, when the compressor is running.

#### **S6,**

Extra temperature measurement, S6. Pt 1000 ohm sensor, eg. AKS 11

#### **EKA Display**

If there is be external reading/operation of the controller, display type EKA 163B or EKA 164B can be connected.

#### **RS485 (terminal 51, 52,53)**

For data communication, but only if a data communication module is inserted in the controller. The module can be Lon. If data communication is used, it is important that the installation of the data communication cable is performed correctly. See separate literature No. RC8AC…

#### **CCH**

Heating element in the crankcase There is connection between terminals 12 and 14 when heating takes place.

#### **Fan**

There is connection between terminals 15 and 16 when the fan's speed is raised to over 95%. (Fan signal changes from terminal 5-6 to 15-16. Connect wire from terminal 16 to the fan.)

16 | BC172686425380en-001201

#### **Aux**

Liquid injection in suction line / external heating element / oil return function for speed-controlled compressor There is connection between terminals 17 and 19, when the function is active.

#### **DI3**

Digital input signal from low/high pressure monitoring. The signal must have a voltage of 0 / 230 V AC.

#### **Electric noise**

Cables for sensors, DI inputs and data communication **must** be kept separate from other electric cables:

- Use separate cable trays

- Keep a distance between cables of at least 10 cm.

- Long cables at the DI input should be avoided

#### **Installation considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown. Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation, for example, could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss will not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer's responsibility to check the installation thoroughly, and to fit the necessary safety devices. Special reference is made to the necessity of signals to the controller when the compressor is stopped and to the need of liquid receivers before the compressors. Your local Danfoss agent will be pleased to assist with further advice, etc.

### **Data**

|Supplyvoltage|230 V AC +10/-15|%. 5 VA,50 / 60 Hz|
|---|---|---|
|Sensor S2, S3,<br>S4, S5, S6|Pt 1000||
||Measuring range|<sup>-60 – 120 °C</sup><br>(S3 to 150 °C)|
|Accuracy|Controller|±1 K below -35°C<br>± 0.5 K between -35 – 25 °C;<br>±1 K above 25 °C|
||Pt 1000 sensor|±0.3 K at 0 °C<br>±0.005 Kper degree|
|Measuring of<br>Pc,Ps|Pressure<br>transmitter|Ratiometric. eg. AKS 32R, DST-P110|
|Display|LED, 3-digits||
|External display|EKA 163B or 164B|(anyEKA 163A or 164A)|
|Digital inputs<br>DI1, DI2|Signal from conta<br>Requirements to c<br>Cable length must<br>Use auxiliaryrelay|ct functions<br>ontacts: Gold plating<br>be max. 15 m<br>s when the cable is longer|
|Digital input DI3|230 V AC from safe|ty pressostat. Low/highpressure|
|Electrical con-<br>nection cable|Max.1.5 mm<sup>2</sup>mult|i-core cable|
|||Max 240 V AC Min 28 V AC|
|Triac output|Fan|.   , .<br>Max. 2.0 A<br>Leak < 1 mA|
|||CE  (250 V AC)|
|Relays*|Comp, CCH|4 (3) A|
||Alarm, Fan, Aux|4 (3) A|
|Analog output|2 pcs. 0 – 10 V DC<br>(For external spee<br>Min. load = 10 K o|d control of fans and compressors)<br>hm.(Max. 1 mA)|
||-25 – 55 °C, During<br>-40 – 70 °C, During|operations<br>transport|
|Environments|20 - 80% Rh,not c|ondensed|
||No shock influenc|le / vibrations|
|Density|IP 20||
|Mounting|DIN-rail or wall||
|Weight|0.4 kg||
|Data communi-|Fixed|MODBUS|
|cation|Extension options|LON|
|Power reserve<br>for the clock|4 hours||
|Approvals|EC Low Voltage Di<br>marking complied<br>LVD tested acc. EN<br>EMC-tested acc. EN|rective and EMC demands re CE-<br>with<br>60730-1 and EN 60730-2-9, A1, A2<br>61000-6-2 and EN 61000-6-3|

*  Comp and CCH are 16 A relays. Alarm and Fan are 8 A relays. Max. load must be observed

### **Ordering**

|**Type**|**Function**|**Code no.**|
|---|---|---|
|Optyma™**Plus**|Condensing unit controller<br>Prepared for data communication<br>Plug for screw terminals not enclosed|**084B8080**|
|Plug|Plug with screw terminals|**084B8166**|
|EKA 175|Data communication module LON RS485|**084B8579**|
|EKA 163B|External display with plug for direct connection|**084B8574**|
|EKA 164B|External display with operation buttons and plug for direct<br>connections|**084B8575**|
|EKA 163A|External display with screw terminals|**084B8562**|
|EKA 164A|External display with operation buttons and screw terminals|**084B8563**|
|Wire with plug|Wire for display unit (9 m, with plug)|**084B7630**<br>**(24 pcs.)**|
|EKA 183A|Programming key|**084B8582**|
