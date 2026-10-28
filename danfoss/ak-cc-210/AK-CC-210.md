# Danfoss AK-CC 210 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Controller for temperature control AK-CC 210

*Kilde: Danfoss-dokument BC029186426773en-000601.pdf*

**User Guide**

### **Controller for temperature control** AK-CC 210

ADAP-KOOL® Refrigeration control systems

#### **Contents**

|Introduction ....................................................................................................... 2|
|---|
|Operation ............................................................................................................ 3|
|Applications ....................................................................................................... 6|
|Survey of functions .......................................................................................... 8|

|Operation ..........................................................................................................18|
|---|
|Menu survey .....................................................................................................20|
|Ordering ............................................................................................................22|
|Connections .....................................................................................................23|
|Data .....................................................................................................................24|

#### **Introduction**

##### **Application**

- The controller is used for temperature control refrigeration appliances in supermarkets

- With many predefined applications one unit will offer you many options. Flexibility has been planned both for new installations and for service in the refrigeration trade

##### **Principle**

The controller contains a temperature control where the signal can be received from one or two temperature sensors. The thermostat sensors are either placed in the cold air flow after the evaporator, in the warm air flow just before the evaporator, or both. A setting will determine how great an influence the two signals are to have on the control.

A measurement of the defrost temperature can be obtained directly through the use of an S5 sensor or indirectly through the use of the S4 measurement. Four relays will cut the required functions in and out – the application determines which. The options are the following:

- Refrigeration (compressor or relay)

- Fan

- Defrost

- Rail heat

- Alarm

- Light

- Fans for hotgas defrost

- Refrigeration 2 (compressor 2 or relay 2)

The different applications are described on page 6.

##### **Advantages**

- Many applications in the same unit

- The controller has integrated refrigeration-technical functions, so that it can replace a whole collection of thermostats and timers

- Buttons and seal imbedded in the front

- Can control two compressors

- Easy to remount data communication

- Quick setup

- Two temperature references

- Digital inputs for various functions

- Clock function with super cap backup

- HACCP (Hazard Analysis and Critical Control Points)

- Temperature monitoring and registration of period with too high temperature (see also page 19)

- Factory calibration that will guarantee a better measuring accuracy than stated in the standard EN ISO 23953-2 without subsequent calibration (Pt 1000 ohm sensor)

2

#### **Operation**

##### **Sensors**

Up to two thermostat sensors can be connected to the controller. The relevant application determines how.

A sensor in the air before the evaporator: This connection is primarily used when control is based on area.

A sensor in the air after the evaporator:

This connection is primarily used when refrigeration is controlled and there is a risk of a too low temperature near the products.

A sensor before and after the evaporator: This connection offers you the possibility of adapting the thermostat, the alarm thermostat and the display to the relevant application. The signal to the thermostat, the alarm thermostat and the display is set as a weighted value between the two temperatures, and 50% will for example give the same value from both sensors.

The signal to the thermostat, the alarm thermostat and the display can be set independently of one another.

##### Defrost sensor

The best signal concerning the evaporator’s temperature is obtained from a defrost sensor mounted directly on the evaporator. Here the signal may be used by the defrost function, so that the shortest and most energy-saving defrost can take place.

If a defrost sensor is not required, defrost can be stopped based on time, or S4 can be selected.

##### **Control of two compressors**

This control is used for controlling two compressors of the same size. The principle for control is that one of the compressors connects at ½ the differential of the thermostat, and the other at the full differential.  When the thermostat cuts in the compressor with the fewest operating hours is started. The other compressor will only start after a set time delay, so that the load will be divided between them. The time delay has a higher priority than the temperature.

When the air temperature has dropped by half the differential the one compressor will stop, the other will continue working and not stop until the required temperature is achieved.

The compressors used must be of a type that is capable of starting up against a high pressure.

##### **Change of temperature reference**

In an impulse appliance, for example, used for various product groups. Here the temperature reference is changed easily with a contact signal on a digital input. The signal raises the normal thermostat value by a predefined amount. At the same time the alarm limits with the same value are displaced accordingly.

3

##### **Digital inputs**

There are two digital inputs both of which can be used for the following functions:

- Case cleaning

- Door contact function with alarm

- Starting a defrost

- Coordinated defrost

- Change-over between two temperature reference

- Retransmission of a contact’s position via data communication

##### **Case cleaning function**

This function makes it easy to steer the refrigeration appliance through a cleaning phase. Via three pushes on a switch you change from one phase to the next phase. The first push stops the refrigeration – the fans keep working ”Later”: The next push stops the fans ”Still later”: The next push restarts refrigeration The different situations can be followed on the display.

On the network a cleaning alarm is transmitted to the system unit. This alarm can be ”logged” so that proof of the sequence of events is provided.

##### **Door contact function**

In cold rooms and frost rooms the door switch can switch the light on and off, start and stop the refrigeration and give alarm if the door has remained open for too long.

|-|+|+|°C|
|---|---|---|---|
|1|÷|+|Fan|
|2|÷|÷|Off|
|3|+|+|°C|

##### **Defrost**

Depending on the application you may choose between the following defrost methods: Natural: Here the fans are kept operating during the defrost Electric: The heating element is activated Brine: The valve is kept open so that the brine can flow through the evaporator Hotgas: Here the solenoid valves are controlled so that the hotgas can flow through the evaporator

Hot gas application

|**Start of def**|**rost**|
|---|---|
|A defrost ca    f|n be started in different ways|
|Interval:|Defrost is started at fixed time intervals, say, every<br>eighth hour|
|Refrigeratio|n time:|
||Defrost is started at fixed refrigeration time inter-<br>vals, in other words, a low need for<br>refrigeration will ”postpone” the coming defrost|
|Schedule:|Here defrost can be started at fixed times of the<br>day and night. However, max. 6 times|
|Contact:|Defrost is started with a contact signal on a digital<br>input|
|Network:|The signal for defrost is received from a system unit<br>via the data communication|
|S5 temp|In 1:1 systems the efficiency of the evaporator can<br>be followed. Icing-up will start a defrost.|
|Manual:|An extra defrost can be activated from the control-<br>ler’s lower-most button. (Though not for<br>application 4).|

All the mentioned methods can be used at random – if just one them is activated a defrost will be started.


##### **Coordinated defrost**

There are two ways in which coordinated defrost can be arranged. Either with wire connections between the controllers or via data communication

##### Wire connections

One of the controllers is defined to be the controlling unit and a battery module may be fitted in it so that the clock is ensured backup. When a defrost is started all the other controllers will follow suit and likewise start a defrost. After the defrost the individual controllers will move into waiting position. When all are in waiting position there will be a change-over to refrigeration. (If just one in the group demands defrost, the others will follow suit).

##### Defrost via data communication

All controllers are fitted with a data communication module, and via the override function from a gateway the defrost can be coordinated.

##### **Defrost on demand**

- 1 Based on refrigeration time

When the aggregate refrigeration time has passed a fixed time, a defrost will be started.

- 2 Based on temperature

The controller will constantly follow the temperature at S5. Between two defrosts the S5 temperature will become lower the more the evaporator ices up (the compressor operates for a longer time and pulls the S5 temperature further down).   When the temperature passes a set allowed variation the defrost will be started.

This function can only work in 1:1 systems

##### **Extra module**

- The controller can afterwards be fitted with an insertion module if the application requires it.

- The controller has been prepared with plug, so the module simply has to be pushed in

- Battery module

The module guarantees voltage to the controller if the supply voltage should drop out for more than four hours. The clock function can thus be protected during a power failure.

- Data communication

If you require operation from a PC, a data communication module has to be placed in the controller.

- External display

If it is necessary to indicate the temperature on the front of refrigeration appliance, a display type EKA 163A can be mounted. The extra display will show the same information as the controller's display, but does not incorporate buttons for operation. If operation from the external display is needed a display type EKA 164A must be mounted.

5

#### **Applications**

S3 and S4 are temperature sensors. The application will determine whether either one or the other or both sensors are to be used. S3 is placed in the air flow before the evaporator. S4 after the evaporator.

Here is a survey of the controller’s field of application.

A setting will define the relay outputs so that the controller’s interface will be targeted to the chosen application.

A percentage setting will determine according to what the control is to be based. S5 is a defrost sensor and is placed on the evaporator.

On page 20 you can see the relevant settings for the respective wiring diagrams.

DI1 and DI2 are contact functions that can be used for one of the following functions: door function, alarm function, defrost start, external main switch, night operation, change of thermostat reference, appliance cleaning, forced refrigeration or coordinated defrost. See the functions in settings o02 and o37.

*[Figurtekst: Refrigeration control with one compressor 1 · The functions are adapted to small refrigeration systems which · either may be refrigeration appliances or cold rooms. · The three relays can control the refrigeration, the defrost and the · fans, and the fourth relay can be used for either alarm function, · light control or rail heat control · • The alarm function can be linked up with a contact function · from a door switch. If the door remains open longer than al- · lowed there will be an alarm. · • The light control can also be linked up with a contact function · from a door switch. An open door will switch on the light and · it will remain lit for two minutes after the door has been closed · again. · • The rail heat function can be used in refrigeration or freezing · appliances or on the door’s heating element for frost rooms. 2 · The fans can be stopped during defrost and they may also follow · a door switch’s open/close situation. · There are several other functions for the alarm function as well · as the light control, rail heat control and fans. Please refer to the · respective settings. · 3 · Hot gas defrost 4 · This type of connection can be used on systems with hotgas · defrost, but only in small systems in, say, supermarkets – the · functional content has  not  been adapted to systems with large · charges. Relay 1’s change-over function can be used by the · bypass valve and/or the hotgas valve. · Relay 2 is used for refrigeration. · Danfoss 84B2428.12 · Danfoss 84B2429.13 · Danfoss 84B2430.13]*

6

*[Figurtekst: 5 · Refrigeration control with two compressors · This group of applications can be used if the controller is to cut · two compressors in and out. · The functions can be compared with wiring diagrams 1 to 3, but · instead of controlling fans the relay is here used for compressor · 2. · The two compressors must be of the same size. When the · controller demands refrigeration it will first cut in the compres- · sor with the shortest operating time. After the time delay the  6 · second compressor will be cut in. · When the temperature has dropped to ”the middle of the dif- · ferential”, the compressor with the longest operation time will be · cut out. · If the running compressor does not manage to reduce the tem- · perature to the cutout point, the other compressor will be cut in · again. This happens when the temperature reaches the top part · of the differential. If the temperature is instead ”stuck” in the dif- · ferential for two hours, there will be a change-over between the  7 · two compressors so that the operating time can be equalised. · The two compressors must be of a type that can start up against · a high pressure. · The compressors’s settings for ”Min On time” and ”Min Off time” · will always have top priority during normal regulation. But if one · of the override functions is activated, the ”Min On time” will be · disregarded. · 10 · If the controller is to cut 2 compressor and 1 fan in and out, relay · 4 must cut the fan in and out. · This function is activated in application 10. · 8 · Simple refrigeration with defrost · This application can be used where there is only regulation of · refrigeration and defrost. · Heating function 9 · This application is the same as under 1, but a heating function · has been added which protects the unit against too low tem- · perature. The defrost function’s heating element is here used for · heating. · This application is used where the temperature can go below · the set cutout temperature for the refrigeration. To ensure that · the temperature will not become too low the heating element is · activated x degrees below the reference value. · The S3 sensor must be mounted. It supplies the signal when · there is heating.]*

7

#### **Survey of functions**

|**Function**|**Para-**<br>**meter**|**Parameter by operation via data**<br>**communication**|
|---|---|---|
|**Normal display**|||
|Normally the temperature value from one of the two thermostat sensors S3 or S4 or a<br>mixture of the two measurements is displayed.<br>In o17 the ratio is determined.||Display air (u56)|
|**Thermostat**||**Thermostat control**|
|**Set point**<br>Regulation is based on the set value plus a displacement, if applicable. The value is set<br>via a push on the centre button.<br>The set value can be locked or limited to a range with the settings in r02 and r 03.<br>The reference at anytime can be seen in ”u28 Temp. ref”||Cutout °C|
|**Differential**<br>When the temperature is higher than the reference + the set differential, the com-<br>pressor relay will be cut in. It will cut out again when the temperature comes down to<br>the set reference.|r01|Differential|
|Ref.<br>Dif.|||
|**Setpoint limitation**<br>The controller’s setting range for the setpoint may be narrowed down, so that much<br>too high or much too low values are not set accidentally - with resulting damages.|||
|To avoid a too high setting of the setpoint, the max. allowable reference value must<br>be lowered.|r02|Max cutout °C|
|To avoid a too low setting of the setpoint, the min. allowable reference value must be<br>increased.|r03|Min cutout °C|
|**Correction of the display’s temperature showing**<br>If the temperature at the products and the temperature received by the controller are<br>not identical, an offset adjustment of the shown display temperature can be carried<br>out.|r04|Disp. Adj. K|
|**Temperature unit**<br>Set here if the controller is to show temperature values in °C or in °F.|r05|Temp. unit<br>°C=0. / °F=1<br>(Only °C on AKM, whatever the set-<br>ting)|
|**Correction of signal from S4**<br>Compensation possibility through long sensor cable|r09|Adjust S4|
|**Correction of signal from S3**<br>Compensation possibility through long sensor cable|r10|Adjust S3|
|**Start / stop of refrigeration**<br>With this setting refrigeration can be started, stopped or a manual override of the<br>outputs can be allowed.<br>Start / stop of refrigeration can also be accomplished with the external switch func-<br>tion connected to a DI input.<br>Stopped refrigeration willgive a ”Standbyalarm”.|r12|Main Switch<br>1: Start<br>0: Stop<br>-1: Manual control of outputs allowed|
|**Night setback value**<br>The thermostat’s reference will be the setpoint plus this value when the controller<br>changes over to night operation. (Select a negative value if there is to be cold ac-<br>cumulation.)|r13|Night offset|
|**Selection of thermostat sensor**<br>Here you define the sensor the thermostat is to use for its control function. S3, S4, or a<br>combination of them. With the setting 0%, only S3 is used (Sin). With 100%, only S4.<br>(For application 9 an S3 sensor must be used)|r15|Ther. S4 %|
|**Heating function**<br>The function uses the defrost function’s heating element for raising the temperature.<br>The function enters into force a number of degrees (r36) below the actual reference<br>and cuts out again with a differential of 2 degrees. Regulation is carried out with<br>100% signal from the S3 sensor. The fans will be operating when there is heating. The<br>fans and the heating function will stop if door function has been selected and the<br>dr i nd|r36|HeatStartRel|
|oo s opee.<br>Where this function is used an external safety cutout should also be installed, so that<br>superheating of the heating element cannot take place.<br>Remember to set D01 to electrical defrosting.|||

8

*[Figurtekst: Activation of reference displacement r39 Th. offset · When the function is changed to ON the thermostat reference will be displaced by · the value in r40. Activation can also take place via input DI1 or DI2 (defined in o02 or · o37). · Value of reference displacement r40 Th. offset K · The thermostat reference and the alarm values are shifted the following number of · degrees when the displacement is activated. Activation can take place via r39 or input · DI · Night setbck · ( start of ni g ht si g nal ) · Forced cool. · ( start of forced coolin g) · Alarm Alarm settings · The controller can give alarm in different situations. When there is an alarm all the  With data communication the impor- · light-emitting diodes (LED) will flash on the controller front panel, and the alarm relay  tance of the individual alarms can be · will cut in. defined. Setting is carried out in the · “Alarm destinations” menu. · Alarm delay  (short alarm delay) A03 Alarm delay · If one of the two limit values is exceeded, a timer function will commence. The alarm · will not become active until the set time delay has been passed. The time delay is set · in minutes. · Time delay for door alarm A04 DoorOpen del · The time delay is set in minutes. · The function is defined in o02 or in o37. · Time delay for cooling  (long alarm delay) A12 Pulldown del · This time delay is used during start-up, during defrost, immediately after a defrost. · There will be change-over to the normal time delay (A03) when the temperature has · dropped below the set upper alarm limit. · The time dela y  is set in minutes. · Upper alarm limit A13 HighLim Air · Here you set when the alarm for high temperature is to start. The limit value is set in · °C (absolute value). The limit value will be raised during night operation. The value is · the same as the one set for night setback, but will only be raised if the value is posi- · tive. · The limit value will also be raised in connection with reference dis p lacement r39. · Lower alarm limit A14 LowLim Air · Here you set when the alarm for low temperature is to start. The limit value is set in °C · (absolute value). · The limit value will also be raised in connection with reference dis p lacement r39. · Delay of a DI1 alarm A27 AI.Delay DI1 · A cut-out/cut-in input will result in alarm when the time delay has been passed. The · function is defined in o02. · Delay of a DI2 alarm A28 AI.Delay DI2 · A cut-out/cut-in input will result in alarm when the time delay has been passed. The · function is defined in o37 · Signal to the alarm thermostat A36 Alarm S4% · Here you have to define the ratio between the sensors which the alarm thermostat · has to use. S3, S4 or a combination of the two. · With settin g  0% onl y  S3 is used. With 100% onl y  S4 is used · Reset alarm · EKC error · Compressor Compressor control · The compressor relay works in conjunction with the thermostat. When the thermo- · stat calls for refrigeration will the compressor relay be operated. · Running times · To prevent irregular operation, values can be set for the time the compressor is to run · once it has been started. And for how long it at least has to be stopped. · The running times are not observed when defrosts start. · Min. ON-time  ( in minutes ) c01 Min. On time · Min. OFF-time  ( in minutes ) c02 Min. Off time]*

9

|**Time delay for couplings of two compressors**<br>Settings indicate the time that has to elapse from the first relay cuts in and until the<br>next relayhas to cut in.|c05|Step delay|
|---|---|---|
|**Reversed relay function for D01**<br>0: Normal function where the relay cuts in when refrigeration is demanded<br>1: Reversed function where the relay cuts out when refrigeration is demanded (this<br>wiring produces the result that there will be refrigeration if the supply voltage to the<br>controller fails).|c30|Cmp relay NC|
|The LED on the controller’s front will show whether refrigeration is in progress.||Comp Relay<br>Here you can read the status of the<br>compressor relay, or you can force-<br>control the relay in the ”Manual<br>control” mode|
|**Defrost**||**Defrost control**|
|The controller contains a timer function that is zeroset after each defrost start.<br>The timer function will start a defrost if/when the interval time is passed.<br>The timer function starts when voltage is connected to the controller, but it is dis-<br>placed the first time by the setting in d05.<br>If there is power failure the timer value will be saved and continue from here when<br>the power returns.<br>This timer function can be used as a simple way of starting defrosts, but it will always<br>act as safety defrost if one of the subsequent defrost starts is not received.<br>The controller also contains a real-time clock. By means of settings of this clock and<br>times for the required defrost times, defrost can be started at fixed times of the day.<br>If there is a risk of power failure for periods longer than four hours, a battery module<br>should be mounted in the controller.<br>Defrost start can also be accomplished via data communication, via contact signals or<br>|||
|manual start-up.<br>All starting methods will function in the controller. The different functions have to be<br>set, so that defrosts do not ”come tumbling” one after the other.<br>Defrost can be accomplished with electricity, hotgas or brine.<br>|||
|The actual defrost will be stopped based on time or temperature with a signal from a<br>temperature sensor.|||
|<br>**Defrost method**<br>Here you set whether defrost is to be accomplished with electricity, gas, brine or<br>"non".|d01|Def. method<br>0 = non<br>1 = El|
|During defrost the defrost relay will be cut in.||2 = Gas|
|<br>(With brine the ”refrigeration control valve” will be kept open during defrost)||3= Brine|
|**Defrost stop temperature**<br>The defrost is stopped at a given temperature which is measured with a sensor (the<br>sensor is defined in d10).<br>|d02|Def. Stop Temp|
|The temperature value is set.|||
|**Interval between defrost starts**<br>The function is zero set and will start the timer function at each defrost start. When<br>the time has expired the function will start a defrost.<br>The function is used as a simple defrost start, or it may be used as a safeguard if the<br>normal signal fails to appear.<br>If master/slave defrost without clock function or without data communication is used,<br>the interval time will be used as max. time between defrosts.<br>If a defrost start via data communication does not take place, the interval time will be<br>used as max. time between defrosts.<br>When there is defrost with clock function or data communication, the interval time<br>must be set for a somewhat longer period of time than the planned one, as the<br>interval time will otherwise start a defrost which a little later will be followed by the<br>|d03|Def Interval<br>(0=off)|
|planned one.<br>In connection with power failure the interval time will be maintained, and when the<br>power returns the interval time will continue from the maintained value.<br>The interval time is not active when set to 0.|||
|**Max defrost duration**|d04|Max Def time|
|**.**<br>This setting is a safety time so that the defrost will be stopped if there has not already<br>been a stop based on temperature or via coordinated defrost.||.|
|**Time staggering for defrost cut ins during start-up**<br>The function is only relevant if you have several refrigeration appliances or groups<br>where you want the defrost to be staggered in relation to one another. The function is<br>furthermore only relevant if you have chosen defrost with interval start (d03).<br>The function delays the interval time d03 by the set number of minutes, but it only<br>does it once, and this at the very first defrost taking place when voltage is connected<br>|d05|Time Stagg.|
|to the controller.<br>The function will be active after each and every power failure.|||

10

|**Drip-off time**<br>Here you set the time that is to elapse from a defrost and until the compressor is to<br>start again. (The time when water drips off the evaporator).|d06|DripOff time|
|---|---|---|
|**Delay of fan start after defrost**<br>Here you set the time that is to elapse from compressor start after a defrost and until<br>the fan may start again. (The time when water is “tied” to the evaporator).|d07|FanStartDel|
|**Fan start temperature**<br>The fan may also be started a little earlier than mentioned under “Delay of fan start<br>after defrost”, if the defrost sensor S5 registers a lower value than the one set here.|d08|FanStartTemp|
|**Fan cut in during defrost**<br>Here you can set whether fan is to operate during defrost.<br>0: Stopped (Runs during pump down)<br>1: Running (stopped during  "fan delay")<br>2: Runningduring pumpdown and defrost. After that stopped|d09|FanDuringDef|
|**Defrost sensor**<br>Here you define the defrost sensor.<br>0: None, defrost is based on time<br>1: S5<br>2: S4|d10|DefStopSens.|
|**Pumpdown delay**<br>Set the time where the evaporator is emptied of refrigerant prior to the defrost.|d16|Pump dwn del.|
|**Drain delay (only in connection with hotgas)**<br>Set the time where the evaporator is emptied of condensed refrigerant after the<br>defrost.|d17|Drain del|
|**Defrost on demand – aggregate refrigeration time**<br>Set here is the refrigeration time allowed without defrosts. If the time is passed, a<br>defrost will be started.<br>With setting= 0 the function is cut out.|d18|MaxTherRunT|
|**Defrost on demand – S5 temperature**<br>The controller will follow the effectivity of the evaporator, and via internal calcula-<br>tions and measurements of the S5 temperature it will be able to start a defrost when<br>the variation of the S5 temperature becomes larger than required.<br>Here you set how large a slide of the S5 temperature can be allowed. When the value<br>is passed, a defrost will start.<br>The function can only be used in 1:1 systems when the evaporating temperature<br>will become lower to ensure that the air temperature will be maintained. In central<br>systems the function must be cut out.<br>With setting= 20 the function is cut out|d19|CutoutS5Dif.|
|**Delay of the hot gas  injection**<br>Can be used when vales of the type PMLX and GPLX are used. Time is set  so that the<br>valve is closed completelybefore the hotgas is turned on.|d23|--|
|If you wish to see the temperature at the defrost sensor, push the controller’s lower-<br>most button.||Defrost temp.|
|If you wish to start an extra defrost, push the controller’s lowermost button for four<br>seconds.<br>You can stop an ongoing defrost in the same way||Def Start<br>Here you can start a manual defrost|
|The LED on the controller’s front will indicate whether a defrost is going on.||Defrost Relay<br>Here you can read the defrost relay<br>status or you can force-control the<br>relay in “Manual control” mode.|
|||Hold After Def<br>Shows ON when the controller is<br>operatingwith coordinated defrost.|
|||Defrost State<br>Status on defrost<br>1=pumpdown / defrost|
|**Fan**||**Fan control**|
|**Fan stopped at cut-out compressor**<br>Here you can select whether the fan is to be stopped when the compressor is cut out|F01|Fan stop CO<br>(Yes = Fan stopped)|
|**Delay of fan stop when compressor is cut out**<br>If you have chosen to stop the fan when the compressor is cut out, you can delay the<br>fan stop when the compressor has stopped.<br>Hereyou can set the time delay.|F02|Fan del. CO|

11

|**Fan stop temperature**<br>The function stops the fans in an error situation, so that they will not provide power<br>to the appliance. If the defrost sensor registers a higher temperature than the one set<br>here, the fans will be stopped. There will be re-start at 2 K below the setting.<br>The function is not active during a defrost or start-up after a defrost.<br>With setting+50°C the function is interrupted.<br>The LED on the controller’s front will indicate whether the fan is running.|F04|FanStopTemp.<br>Fan Relay<br>Here you can read the fan relay status,<br>or force-control the relay in “Manual<br>control” mode.|
|---|---|---|
|**HACCP**||**HACCP**|
|HACCP temperature<br>Hereyou can see the temperature measurement that transmits signal to the function|h01|HACCP temp.|
|Last too high HACCP temperature was registered in connection with: (Value can be<br>read out)|h02|-|
|.<br>H01: Temperature exceeding during normal regulation.<br>H02: Temperature exceeding during power failure. Battery backup controls the times.<br>H03: Temperature exceedingduring power failure. No control of times.|||
|Last time the HACCP temperature was exceeded: Year|h03|-|
|Last time the HACCP temperature was exceeded: Month|h04|-|
|Last time the HACCP temperature was exceeded: Day|h05|-|
|Last time the HACCP temperature was exceeded: Hour<br>|h06<br>|-|
|Last time the HACCP temperature was exceeded: Minute|h07|-|
|Last exceeding: Duration in hours|h08|-|
|Last exceeding: Duration in minutes|h09|-|
|Peak temperature<br>The highest measured temperature will continuously be saved when the temperature<br>exceeds the limit value in h12. The value can be read out until the next time the tem-<br>perature exceeds the limit value. After that it is overwritten with the new measure-<br>ments.|h10|Max.temp.|
|Selection of function<br>0: No HACCP function|h11|HACCP sensor|
|<br>1: S3 and/or S4 used as sensor. Definition takes place in h14.<br>2: S5 used as sensor.|||
|Alarm limit<br>Here you set the temperature value at which the HACCP function is to enter into<br>force. When the value becomes higher than the set one,the time delaystarts.|h12|HACCP limit|
|Time delay for the alarm (only during normal regulation).<br>When the time delayhas beenpassed the alarm is activated.|h13|HACCP delay|
|Selection of sensors for the measuring|h14|HACCP S4%|
|<br>If the S4 sensor and/or the S3 sensor is used, the ratio between them must be set.<br>At setting100% onlyS4 is used. At setting0% onlyS3 is used.|||
|**Internal defrosting schedule/clock function**|||
|(Not used if an external defrosting schedule is used via data communication.)<br>|||
|Upto six individual times can be set for the defrost start throughout the day.|||
|Defrost start,hour setting|t01-t06||
|Defrost start, minute setting (1 and 11 belong together, etc.)|t11-t16||
|<br>When all t01 to t16 equal 0 the clock will not start defrosts.|||
|Real-time clock<br>Setting the clock is only necessary when there is no data communication.<br>In the event of a power failure of less than four hours, the clock function will be saved.<br>When mounting a battery module the clock function can preserved longer.|||
|There is also a date indication used for registration of temperature measurements.|||
|Clock: Hour setting|t07||
|Clock: Minute setting|t08||
|Clock: Date setting|t45||
|Clock: Month setting|t46||
|Clock: Year setting|t47||
|**Miscellaneous**||Miscellaneous|
|**Delay of output signal after start-up**<br>Start-up after a power failure the controller’s functions can be delayed so that over-<br>loading of the electricity supply network is avoided.<br>Here you can set the time delay.|o01|DelayOfOutp.|


|**Digital input signal - DI1**<br>The controller has a digital input 1 which can be used for one of the following func-<br>tions:<br>Off: The input is not used<br>1) Status display of a contact function<br>2) Door function. When the input is open it signals that the door is open. The refrig-<br>eration and the fans are stopped. When the time setting in “A4” is passed, an alarm<br>will be given and refrigeration will be resumed.<br>3) Door alarm. When the input is open it signals that the door is open. When the time<br>setting in “A4” is passed, there will be alarm.<br>4) Defrost. The function is started with a pulse signal. The controller will register when<br>the DI input is activated. The controller will then start a defrost cycle. If the signal<br>is to be received by several controllers it is important that ALL connections are<br>mounted the same way (DI to DI and GND to GND).<br>5) Main switch. Regulation is carried out when the input is short-circuited, and regula-<br>tion is stopped when the input is put in pos. OFF.<br>6) Night operation. When the input is short-circuited, there will be regulation for<br>night operation.<br>7) Reference displacement when DI1 is short-circuited. Displacement with “r40”.<br>8) Separate alarm function. Alarm will be given when the input is short-circuited.<br>9) Separate alarm function. Alarm will be given when the input is opened.   (For 8 and<br>9 the time delay is set in A27)<br>10) Case cleaning. The function is started with a pulse signal. Cf. also description on<br>page 4.<br>11)Forced refrigeration at hotgas defrost when the input is short-circuited.|o02|DI 1 Config.<br>Definition takes place with the nu-<br>merical value shown to the left.<br>(0 = off)<br>DI state<br>(Measurement)<br>The DI input’s present status is shown<br>here. ON or OFF.|
|---|---|---|
|If the controller is built into a network with data communication, it must have an<br>address, and the master gateway of the data communication must then know this<br>address.<br>These settings can only be made when a data communication module has been<br>mounted in the controller and the installation of the data communication cable has<br>been finished.<br>This installation is mentioned in a separate document “RC8AC”.||After installation of a data communi-<br>cation module the controller can be<br>operated on an equal footing with the<br>other controllers in ADAP-KOOL®<br>refrigeration controls.|
|The address is set between 1 and 60 (119), gateway determined|o03||
|The address is sent to the gateway when the menu is set in pos. ON<br>IMPORTANT: Before you set o04, you MUST set o61. Otherwise you will be transmit-|o04||
|tingincorrect data.|||
|**Access code 1 (Access to all settings)**<br>If the settings in the controller are to be protected with an access code you can set a<br>numerical value between 0 and 100. If not, you can cancel the function with setting 0.<br>(99 will alwaysgiveyou access).|o05|-|
|**Sensor type**<br>Normally a Pt 1000 sensor with great signal accuracy is used. But you can also use<br>a sensor with another signal accuracy. That may either be a PTC  1000 sensor (1000<br>ohm) or an NTC sensor (5000 Ohm at 25°C).<br>All the mounted sensors must be of the same type.|o06|SensorConfig<br>Pt = 0<br>PTC = 1<br>NTC = 2|
|**Display step**<br>Yes: Gives steps of 0.5°<br>No: Gives steps of 0.1°|o15|Disp. Step = 0.5|
|**Max. standby time after coordinated defros**t<br>When a controller has completed a defrost it will wait for a signal which tells that the<br>refrigeration may be resumed. If this signal fails to appear for one reason or another,<br>the controller will itself start the refrigeration when this standbytime has elapsed.|o16|Max HoldTime|
|**Select signal for the display S4%**<br>Here you define the signal to be shown by the display.<br>S3, S4, or a combination of  the two.<br>With setting0% onlyS3 is used. With 100% onlyS4.|o17|Disp. S4%|

13

|**Digital input signal - D2**<br>The controller has a digital input 2 which can be used for one of the following func-<br>i|o37|DI2 config.|
|---|---|---|
|tons:<br>Off: The input is not used.<br>1) Status display of a contact function<br>2) Door function. When the input is open it signals that the door is open. The refrig-<br>eration and the fans are stopped. When the time setting in “A4” is passed, an alarm<br>will be given and refrigeration resumed.<br>3) Door alarm. When the input is open it signals that the door is open. When the time<br>setting in “A4” is passed an alarm will be given.<br>4) Defrost. The function is started with a pulse signal. The controller will register when<br>the DI input is activated. The controller will then start a defrost cycle. If the signal<br>is to be received by several controllers it is important that ALL connections are<br>mounted the same way (DI to DI and GND to GND).<br>5) Main switch. Regulation is carried out when the input is short-circuited, and regula-<br>tion is stopped when the input is put in pos. OFF.<br>6) Night operation. When the input is short-circuited, there will be regulation for<br>niht oeration|||
|g p.<br>7) Reference displacement when DI2 is short-circuited. Displacement with “r40”.<br>8) Separate alarm function. Alarm will be given when the input is short-circuited.<br>9) Separate alarm function. Alarm will be given when the input is opened.<br>10) Case cleaning. The function is started with a pulse signal. Cf. also description on<br>page 4.<br>11) Forced refrigeration at hotgas defrost when the input is short-circuited.<br>12) The input is used for coordinated defrost in conjunction with other controllers of<br>the same type|||
|**Configuration of light function**(relay 4 in applications 2 and 6)<br>1) The relay cuts in during day operation<br>2) The relay to be controlled via data communication<br>3) The relay to be controlled by the door switch defined in either o02 or o37 where<br>the setting is selected to either 2 or 3. When the door is opened the relay will cut in.<br>When the door is closed again there will be a time delay of two minutes before the<br>light is switched off.|o38|Light config|
|**Activation of light relay**<br>The light relay can be activated here, but only if defined in o38 with setting 2.|o39|Light remote|
|**Rail heat during day operation**<br>The ONperiod is set as apercentage of the time|o41|Railh.ON day%|
|**Rail heat during night operation**<br>The ONperiod is set as apercentage of the time|o42|Railh.ON ngt%|
|**Rail heat cycle**|o43|Railh. cycle|
|<br>Theperiod of time for the aggregate ON time + OFF time is set in minutes|||
|**Case cleaning**<br>The status of the function can be followed here or the function can be started manu-<br>ll|o46|Case clean|
|ay.<br>0 = Normal operation (no cleaning)<br>1 = Cleaning with fans operating. All other outputs are Off.<br>2 = Cleaning with stopped fans. All outputs are Off.<br>If the function is controlled by a signal at the DI1 or DI2 input, the relevant status can<br>be seen here in the menu.|||
|**Selection of application**<br>The controller can be defined in various ways. Here you set which of the 10 applica-<br>tions is required. On page 6 you can see a survey of applications.<br>This menu can onlybe set when regulation is stopped,i.e. “r12” is set to 0.<br>**Transfer a set of presetting to the controller**<br>It is possible to select a quick setting of a number of parameters. It depends on<br>whether an application or a room is to be controlled and whether defrost is to be<br>stopped based on time or based on temperature. The survey can be seen on page 22.<br>This menu can only be set when regulation is stopped, i.e. “r12” is set to 0.|o61<br>o62|--- Appl. Mode (only output in Danfoss<br>only)<br>-|
|After the setting the value will return to 0. Any subsequent adjustment/setting of<br>parameters can be made,as required.|||
|**Access code 2 (Access to adjustments)**<br>There is access to adjustments of values, but not to configuration settings. If the set-<br>tings in the controller are to be protected with an access code you can set a numeri-<br>cal value between 0 and 100. If not, you can cancel the function with setting 0. If the<br>function is used,access code 1(o05) **must also**be used.|o64|-|
|**Copy the controller’s present settings**<br>With this function the controller’s settings can be transferred to a programming key.<br>The key can contain up to 25 different sets. Select a number. All settings except for<br>Application (o61) and Address (o03) will be copied. When copying has started the dis-<br>play returns to o65. After two seconds you can move into the menu again and check<br>whether the copying was satisfactory.<br>Showing of a negative figure spells problems. See the significance in the Fault Mes-<br>sage section.|o65|-|

14

|**Copy from the programming key**<br>This function downloads a set of settings earlier saved in the controller. Select the<br>relevant number.<br>All settings except for Application (o61) and Address (o03) will be copied. When copy-<br>ing has started the display returns to o66. After two seconds you can move back into<br>the menu again and check whether the copying was satisfactory. Showing of a nega-<br>tive figure spellsproblems. See the significance in the Fault Message section.|o66|-|
|---|---|---|
|**Save as factory setting**<br>With this setting you save the controller’s actual settings as a new basic setting (the<br>earlier factorysettings are overwritten).|o67|-|
|||- - - Night Setback<br>0=Day<br>1=Night|
|**Service**||**Service**|
|Temperature measured with S5 sensor|u09|S5 temp.|
|Status on DI1 input. on/1=closed|u10|DI1 status|
|Temperature measured with S3 sensor|u12|S3 air temp|
|Status on night operation(on or off)1=closed|u13|Night Cond.|
|Temperature measured with S4 sensor|u16|S4 air temp|
|Thermostat temperature|u17|Ther. air|
|Read thepresent regulation reference|u28|Temp. ref.|
|Status on DI2 output. on/1=closed|u37|DI2 status|
|Temperature shown on display|u56|Displayair|
|Measured temperature for alarm thermostat|u57|Alarm air|
|** Status on relayfor cooling|u58|Comp1/LLSV|
|** Status on relayfor fan|u59|Fan relay|
|** Status on relayfor defrost|u60|Def. relay|
|** Status on relayfor railheat|u61|Railh. relay|
|** Status on relayfor alarm|u62|Alarm relay|
|** Status on relayfor light|u63|Light relay|
|** Status on relayfor valve in suction line|u64|SuctionValve|
|** Status on relayfor compressor 2|u67|Comp2 relay|
|*) Not all items  will be shown. Only the function belonging to the selected applica-<br>tion can be seen.|||

15

|**Fault message**|**Alarms**|
|---|---|
|In an error situation the LED’s on the front will flash and the alarm relay will be acti-<br>vated. If you push the top button in this situation you can see the alarm report in the<br>display. If there are more keep on pushing to see them.<br>There are two kinds of error reports - it can either be an alarm occurring during the<br>daily operation, or there may be a defect in the installation.<br>A-alarms will not become visible until the set time delay has expired.<br>E-alarms, on the other hand, will become visible the moment the error occurs.<br>(An A alarm will not be visible as long as there is an active E alarm).<br>Here are the messages that mayappear:|1 = alarm|
|A1: High temperature alarm|High t. alarm|
|A2: Low temperature alarm|Low t. alarm|
|A4: Door alarm|Door Alarm|
|A5: Information. Parameter o16  is expired|Max Hold Time|
|A15: Alarm. Signal from DI1 input|DI1 alarm|
|A16: Alarm. Signal from DI2 input|DI2 alarm|
|A45: Standby position (stopped refrigeration via r12 or DI input)<br>(Alarm relaywill not be activated)|Standby mode|
|A59: Case cleaning. Signal from DI1 or DI2 input|Case cleaning|
|A60: High-temperature alarm for the HACCP function|HACCP alarm|
||Max. def time|
|E1: Faults in the controller|EKC error|
|E6: Fault in real-time clock. Check the battery / reset the clock.|-|
|E25: Sensor error on S3|S3 error|
|E26: Sensor error on S4|S4 error|
|E27: Sensor error on S5|S5 error|
|When copying settings to or from a copying key with functions o65 or o66, the fol-<br>lowing information may appear:<br>0: Copying concluded and OK<br>4: Copying key not correctly mounted<br>5: Copying was not correct. Repeat copying<br>6: Copying to EKC incorrect. Repeat copying<br>7: Copying to copying key incorrect. Repeat copying<br>8: Copying not possible. Order number or SW version do not match<br>9: Communication error and timeout<br>10: Copying still going on<br>(The information can be found in o65 or o66 a couple of seconds after copying has<br>been started).||
||**Alarm destinations**|
||The importance of the individual<br>alarms can be defined with a setting<br>(0, 1, 2 or 3)|

16

|**Operating status**|**(Measurement)**|
|---|---|
|The controller goes through some regulating situations where it is just waiting for<br>the next point of the regulation. To make these “why is nothing happening” situations<br>visible, you can see an operating status on the display. Push briefly (1s) the upper but-<br>ton. If there is a status code, it will be shown on the display.<br>The individual status codes have the followingmeanings:|EKC State:<br>(Shown in all menu displays)|
|S0: Regulating|0|
|S1: Waiting for end of the coordinated defrost|1|
|S2: When the compressor is operating it must run for at least x minutes.|2|
|S3: When the compressor is stopped, it must remain stopped for at least x minutes.|3|
|S4: The evaporator drips off and waits for the time to run out|4|
|S10: Refrigeration stopped by main switch. Either with r12 or a DI-input|10|
|S11: Refrigeration stopped by thermostat|11|
|S14: Defrost sequence. Defrost in progress|14|
|S15: Defrost sequence. Fan delay — water attaches to the evaporator|15|
|S17: Door is open. DI input is open|17|
|S20: Emergency cooling *)|20|
|S25: Manual control of outputs|25|
|S29: Case cleaning|29|
|S30: Forced cooling|30|
|S32: Delay on outputs during start-up|32|
|S33: Heat function r36 is active|33|
|Other displays:||
|non: The defrost temperature cannot be displayed. There is stop based on time||
|-d-: Defrost in progress / First cooling after defrost||
|PS: Password required.  Set password||

*) Emergency cooling will take effect when there is lack of signal from a defined S3 or S4 sensor. The regulation will continue with a registered average cutin frequency. There are two registered values – one for day operation and one for night operation.

Warning ! Direct start of compressors *

To prevent compressor breakdown parameter c01 and c02 should be set according to suppliers requirements or in general : Hermetic Compressors c02 min. 5 minutes

Semihermetic Compressors c02 min. 8 minutes and c01 min. 2 to 5 minutes ( Motor from 5 to 15 KW )

* ) Direct activating of solenoid valves does not require settings different from factory (0)

17

#### **Operation**

##### Set temperature

##### **Display**

The values will be shown with three digits, and with a setting you can determine whether the temperature are to be shown in °C or in °F.

1. Push the middle button until the temperature value is shown

2. Push the upper or the lower button and select the new value

3. Push the middle button again to conclude the setting.

Reading the temperature at defrost sensor

- Push short the lower button

Manuel start or stop of a defrost

- Push the lower button for four seconds. (Though not for application 4).

##### **Light-emitting diodes (LED) on front panel**

HACCP = HACCP function is active

The other LED’s on the front panel will light up when the belonging relay is activated.

##### See HACCP registration

- = Refrigeration

- = Defrost

- = Fan running

1. Give the middle button a long push until h01 appears

2. Select required h01-h10

3. See value by giving the middle button a short push

The light-emitting diodes will flash when there is an alarm. In this situation you can download the error code to the display and cancel/sign for the alarm by giving the top knob a brief push.

##### **Defrost**

During defrost a –d- is shown in the display. This view will continue up till 15 min. after the cooling has resumed. However the view of –d- will be discontinued if: - The temperature is suitable within the 15 minutes

##### **Get a good start**

With the following procedure you can start regulation very quickly:

- The regulation is stopped with “Main Switch”

- A high temperature alarm appears

- **1** Open parameter r12 and stop the regulation (in a new and not previously set unit, r12 will already be set to 0 which means stopped regulation.)

##### **The buttons**

When you want to change a setting, the upper and the lower buttons will give you a higher or lower value depending on the button you are pushing. But before you change the value, you must have access to the menu. You obtain this by pushing the upper button for a couple of seconds - you will then enter the column with parameter codes. Find the parameter code you want to change and push the middle buttons until value for the parameter is shown. When you have changed the value, save the new value by once more pushing the middle button.

##### Examples

##### Set menu

1. Push the upper button until a parameter r01 is shown

2. Push the upper or the lower button and find that parameter you want to change

3. Push the middle button until the parameter value is shown

4. Push the upper or the lower button and select the new value

   - **2** Select electric connection based on the drawings on page 6

   - **3** Open parameter o61 and set the electric connection number in it

   - **4** Now select one of the preset settings from the table on page 22.

   - **5** Open parameter o62 and set the number for the array of presettings. The few selected settings will now be transferred to the menu.

   - **6** Open parameter r12 and start the regulation

   - **7** Go through the survey of factory settings. The values in the grey cells are changed according to your choice of settings. Make any necessary changes in the respective parameters.

   - **8** For network. Set the address in o03 and then transmit it to the gateway/system unit with setting o04.

5. Push the middle button again to freeze the value.

##### Cutout alarm relay / receipt alarm/see alarm code

- Push short the upper button

If there are several alarm codes they are found in a rolling stack. Push the uppermost or lowermost button to scan the rolling stack.

18

##### **HACCP**

This function will follow the appliance temperature and sound an alarm if the set temperature limit is exceeded. The alarm will come when the time delay has elapsed.

When the temperature exceeds the limit value it will continuously be registered and the peak value will be saved until the later readout. Saved together with the value will be the time and duration of the temperature exceeding.

The readout of the various values in the HACCP function can take place with a long push on the middle button. The readouts are, as follows:

h01: The temperature

h02: Readout of the controller’s status when temperature was exceeded:

H1 = normal regulation.

H2 = power failure. Times are saved.

H3 = power failure. Times not saved.

Examples of temperature exceeding:

Exceeding during normal regulation

Exceeding in connection with power failure where the controller can keep on registering the time performance.

Exceeding in connection with power failure when the controller has lost its clock function and hence also its time performance.

h03: Time. Year

h04: Time. Month h05: Time: Day h06: Time. Hour h07: Time. Minute

h08: Duration in hours

h09: Duration in minutes

h10: The registered peak temperature

(Setup of the function takes place just like the other setups. See menu survey on the next page).

19

SW = 2.3x

#### **Menu survey**

|**Parameters**<br>**Function**|||**Codes**|**EL-diagram number (pa**<br>**1**<br>**2**<br>**3**<br>**4**<br>**5**<br>**6**<br>**7**|**ge 6)**<br>**8**<br>**9**<br>**10**|**Min.-**<br>**value**|**Max.-**<br>**value**|**Factory**<br>**setting**|**Actual**<br>**setting**|
|---|---|---|---|---|---|---|---|---|---|
|**Normal operation**<br>T  i||||||00°C|00°C|20°C||
|emperature(setpont)<br>|||---|||-5.|5.|.||
|**Thermostat**<br>Differential<br>Max limitation of setpoint setting|*<br>*|*<br>*|*<br>r01<br>*<br>r02|||0.1 K<br>-490°C|20.0K<br>50°C|2.0 K<br>500°C||
|. <br>Min limitation of setoint settin|*|*|*<br>r03|||.<br>-500°C|490°C|.<br>-500°C||
|.p g<br>Adjustment of temperature indication|||r04|||.<br>-20.0 K|.<br>20.0 K|.<br>0.0 K||
|Temperature unit(°C/°F)<br>Correction of the signal from S4|||r05<br>r09|||°C<br>-10.0 K|°F<br>+10.0 K|°C<br>0.0 K||
|Correction of the signal from S3<br>|||r10<br>|||-10.0 K<br>|+10.0 K<br>|0.0 K<br>||
|Manual service,stopregulation,start regulation(-1,0,1)<br>Displacement of reference duringnight operation|||r12<br>r13|||-1<br>-10.0 K|1<br>10.0 K|0<br>0.0 K||
|Definition and weighting, if applicable, of thermostat sensors<br>-S4% (100%=S4  0%=S3)|||r15|||0%|100%|100%||
|,<br>The heating function is started a number of degrees below the<br>|||r36|||-15.0 K|-3.0 K|-15.0 K||
|thermostats cutout temperature<br>Activation of reference displacement  r40|||r39|||OFF|ON|OFF||
|Value of reference displacement(activate via r39 or DI)<br>**Alarm**|||r40|||-50.0 K|50.0 K|0.0 K||
|Delayfor temperature alarm<br>|||A03<br><br>|||0 min<br>|240 min<br>|30 min<br>||
|Delayfor door alarm<br>||*|A04<br>|||0 min<br>|240 min<br>|60 min<br>||
|Delayfor temperature alarm after defrost<br>High alarm limit|*|*|A12<br>*<br>A13|||0 min<br>-50.0°C|240 min<br>50.0°C|90 min<br>8.0°C||
|Low alarm limit|*|*|*<br>A14|||-50.0°C|50.0°C|-30.0°C||
|<br>Alarm delayDI1<br>|||A27<br>|||0 min<br>|240 min<br>|30 min<br>||
|Alarm delayDI2<br>Signal for alarm thermostat. S4%(100%=S4,0%=S3)|||A28<br>A36|||0 min<br>0%|240 min<br>100%|30 min<br>100%||
|**Compressor**<br>Min. ON-time|||c01|||0 min|30 min|0 min||
|Min. OFF-time<br>|||c02<br>|||0 min<br>|30 min<br>|0 min<br>||
|Time delayfor cutin of comp.2<br>Compressor relay 1 must cutin and out inversely|||c05<br>c30|||0 sec<br>0|999 sec<br>1|0 sec<br>0||
|(NC-function)<br>**Defrost**||||||OFF|ON|OFF||
|Defrost method(none/EL/GAS/BRINE)<br>|||d01<br>|||no<br>|bri<br>|EL<br>||
|Defrost stoptemperature|||d02|||0.0°C|25.0°C|6.0°C||
|Interval between defrost starts|||d03|||0 hours|240<br>hours|8 hours||
|Max. defrost duration<br>|||d04<br>|||0 min<br>|180 min<br>|45 min<br>||
|Displacement of time on cutin of defrost at start-up<br>f|||d05<br>|||0 min<br>|240 min<br>|0 min<br>||
|Dripoff time<br>Delayfor fan start after defrost|||d06<br>d07|||0 min<br>0 min|60 min<br>60 min|0 min<br>0 min||
|Fan start temperature<br>Fan cutin durin defrost|||d08<br>d09|||-15.0°C<br>0|0.0°C<br>2|-5.0°C<br>1||
|g<br>0: Stopped||||||||||
|1: Running||||||||||
|<br>2: Running during  pump down and defrost<br>Dft(0ti1S52S4)|||d10|||0|2|0||
|eros sensor=me,=,=<br>Pumpdown delay<br>Drain delay|||d16<br>d17|||0 min<br>0 min|60 min<br>60 min|0 min<br>0 min||
|Max. aggregate refrigeration time between two defrosts|||d18|||0 hours|48 hours|<br>0 hours||
|Defrost on demand - S5 temperature’s permitted variation dur-|||d19|||00 K|200 k|200 K||
|<br>ing frost build-up. On central plant choose 20 K (=off)<br>||||||.<br>|.<br>|.<br>||
|Delayof hotgas defrost<br>|||d23|||0 min|60 min|0 min||
|**Fan**<br>Fan stopat cutout compressor<br>Delaof fan sto|||F01<br>F02|||no<br>0 min|yes<br>30 min|no<br>0 min||
|y p<br>F  S|||F|||<br>°C|<br>°C|<br>°C||
|an stoptemperature(5)<br>|||04|||-50.0|50.0|50.0||
|**HACCP**<br>Actual temperature measurement for the HACCP function|||h01|||||||
|Last registered peak temperature<br>Selection of function and sensor for the HACCP function. 0 = no<br>|||h10<br>h11|||0|2|0||
|HACCP function. 1=S4 used (maybe also S3). 2=S5 used<br>Alarm limit for the HACCP function|||h12|||-50.0°C|50.0°C|8.0°C||
|Time delay for the HACCP alarm<br>Select signal for the HACCP function. S4% (100% = S4, 0% = S3)|||h13<br>h14|||0 min.<br>0%|240 min.<br>100%|<br>30 min.<br>100%||
|<br>**Real time clock**||||||||||
|<br>Six start times for defrost.|||t01-t06|||0 hours|23 hours|<br>0 hours||
|Setting of hours.<br>||||||||||
|0=OFF<br>Six start times for defrost.|||t11-t16|||0 min|59 min|0 min||
|Setting of minutes.<br>||||||||||
|0=OFF<br>Clock - Settingof hours|*|*|*<br>t07|||0 hours|23 hours|<br>0 hours||
|Clock - Settingof minute|*|*|*<br>t08|||0 min|59 min|0 min||
|Clock - Settingof date<br>Clock - Settinof month|*<br>*|*<br>*|*<br>t45<br>*<br>t46|||1<br>1|31<br>12|1<br>1||
|g <br>Clock - Settingofyear<br>|*|*|*<br>t47|||0|99|0||
|**Miscellaneous**<br>Delayof output signals afterpower failure|||o01|||0 s|600 s|5 s||

20

|Int sinal on DI1 Fnction||o02|**1**<br>**2**<br>**3**<br>**4**<br>**5**<br>**6**<br>**7**<br>**8**|**9**<br>**10**|1|11|0|
|---|---|---|---|---|---|---|---|
|pu g  . u:<br>0=not used. 1=status on DI1. 2=door function with alarm when<br>open. 3=door alarm when open. 4=defrost start (pulse-signal).<br>5=ext.main switch. 6=night operation 7=change reference<br>(activate r40). 8=alarm function when closed. 9=alarm function<br>when open. 10=case cleaning (pulse signal). 11=forced cooling||||||||
|at hot gas defrost.||||||||
|Network address||o03|||0|240|0|
|On/Off switch (Service Pin message)<br>||o04|||OFF|ON|OFF|
|IMPORTANT! o61**must**be set prior to o04||||||||
|Access code 1(all settings)||o05|||0|100|0|
|Used sensor type(Pt/PTC/NTC)||o06|||Pt|ntc|Pt|
|Displaystep= 0.5(normal 0.1 at Pt sensor)||o15|||no|yes|no|
|Max hold time after coordinated defrost||o16|||0 min|60 min|20|
|Select signal for displayview.  S4%(100%=S4,0%=S3)||o17|||0%|100%|100%|
|Input signal on DI2. Function:<br>||o37|||0|12|0|
|(0=not used. 1=status on DI2. 2=door function with alarm when<br>open. 3=door alarm when open. 4=defrost start (pulse-signal).<br>5=ext. main switch 6=night operation 7=change reference<br>(activate r40). 8=alarm function when closed. 9=alarm function<br>when open. 10=case cleaning (pulse signal). 11=forced cooling||||||||
|<br>at hot gas defrost.). 12=coordinated defrost)||||||||
|<br>Configuration of light function (relay 4)<br>1=ON during day operation. 2=ON / OFF via data communica-<br>tion. 3=ON follows the DI-function when DI is selected to door||o38|||1|3|1|
|,<br>function or to door alarm||||||||
|Activation of light relay (onlyif o38=2)||o39|||OFF|ON|OFF|
|Rail heat On time duringdayoperations||o41|||0%|100%|100|
|Rail heat On time duringnight operations||o42|||0%|100%|100|
|Rail heat period time (On time + Offtime)||o43|||6 min|60 min|10 min|
|f <br>Case cleaning. 0=no case cleaning. 1=Fans only. 2=All output<br>Off|***|o46|||0|2|0|
|f.<br>Selection of  EL diagram. See overviewpage 6|*|o61|||1|10|1|
|Download a  set of predetermined settings. See overview next<br>page.|*|o62|||0|6|0|
|<br>Access code 2(partlyaccess)|***|o64|||0|100|0|
|Save the controllers present settings to the programming key.||o65|||0|25|0|
|<br>Select your own number.||||||||
|<br>Load a set of settings from the programming key (previously||o66|||0|25|0|
|saved via o65 function)||||||||
|Replace the controllers factory settings with the present set-<br>||o67|||OFF|On|OFF|
|tings||||||||
|**Service**||||||||
|Status codes are shown onpage 17||S0-S33||||||
|Temperature measured with S5 sensor|***|u09||||||
|Status on DI1 input. on/1=closed<br>||u10<br>||||||
|Temperature measured with S3 sensor<br>Status on night operation(on or off)1=closed|***<br>***|u12<br>u13||||||
|Temperature measured with S4 sensor<br>Thermostat temperature|***|u16<br>u17||||||
|Read thepresent regulation reference||u28||||||
|Status on DI2 output. on/1=closed||u37||||||
|Temperature shown on display||u56||||||
|Measured temperature for alarm thermostat||u57||||||
|Status on relayfor cooling|**|u58||||||
|Status on relayfor fan|**|u59||||||
|<br>Status on relayfor defrost|**|u60||||||
|Status on relayfor railheat<br>|**|u61||||||
|Status on relayfor alarm|**|u62||||||
|Status on relayfor light|**|u63||||||
|Status on relayfor valve in suction line|**|u64||||||
|<br>Status on relayfor compressor 2|**|u67||||||

> *) Can only be set when regulation is stopped (r12=0)

> **) Can be controlled manually, but only when r12=-1

> ***) With access code 2 the access to these menus will be limited

Factory setting

If you need to return to the factory-set values, it can be done in this way:

> - Cut out the supply voltage to the controller

> - Keep both buttons depressed at the same time as you recon nect the supply voltage

21

|Auxiliary table for settings<br>||**Case**|||**Room**||
|---|---|---|---|---|---|---|
|(quick-setup)|Defrost stop on<br>time|Defrost<br>on S|stop<br>5|Defrost  stop on<br>time|Defrost<br>on S|stop<br>5|
|**Preset settings**(o62)|**1**|**2**|**3**|**4**|**5**|**6**|
|Temperature (SP)|4°C|2°C|-24°C|6°C|3°C|-22°C|
|Max. temp. setting (r02)|6°C|4°C|-22°C|8°C|5°C|-20°C|
|Min. temp. setting (r03)|2°C|0°C|-26°C|4°C|1°C|-24°C|
|Sensor signal for thermostat. S4% (r15)||100%|||0%||
|Alarm limit high (A13)|10°C|8°C|-15°C|10°C|8°C|-15°C|
|Alarm limit low (A14)|-5°C|-5°C|-30°C|0°C|0°C|-30°C|
|Sensor signal for alarm funct.S4% (A36)||100%|||0%||
|Interval between defrost (d03)|6 h|6h|12h|8h|8h|12h|
|Defrost sensor: 0=time, 1=S5, 2=S4 (d10)|0|1|1|0|1|1|
|DI1 config. (o02)|Ca|se cleaning(=10)||D|oor function (=3)||
|Sensor signal for display view S4% (017)||100%|||0%||

##### **Override**

The controller contains a number of functions that can be used together with the override function in the master gateway  / System Manager.

|**Function via data communication**|**Functions to be used in the gateway’s**<br>**override function**|**Used parameter in AK-CC 210**|
|---|---|---|
|Start of defrosting|Defrost control<br>Time schedule|- - - Def.start|
|Coordinated defrost|Defrost control|- - - HoldAfterDef<br>u60 Def.relay|
|Night setback|Day/night control<br>Time schedule|- - - Night setbck|
|Light control|Day/night control<br>Time schedule|o39 Light Remote|

#### **Ordering**

|**Type**|**Function**|**Co**|**de no.**|
|---|---|---|---|
|AK-CC 210|Refrigeration controller without data communica-<br>tion but prepared for mounting of one module|**230 V a.c**<br>**115 V a.c.**|**084B8520**<br>**084B8534**|
|EKA 178A|Data communication module<br>MOD-BUS|**084**|**B8564**|
|EKA 179A|Data communication module<br>LON RS 485|**084**|**B8565**|
|EKA 181C|Battery module that will protect the clock in case<br>of lengthy power failure|**084**|**B8577**|
|EKA 182A|Copy key EKC - EKC|**084**|**B8567**|
|EKA 163A|External display for AK-CC 210|**084**|**B8562**|

22

#### **Connections**

##### **Power supply**

##### **Relays**

The general uses are mentioned here. See also page 6 where the different applications are shown.

DO1: Refrigeration. The relay will cut in when the controller demands refrigeration

- DO2: Defrost. The relay will cut in when defrost is in progress DO3: For either fans or refrigeration 2

Fans: The relay will cut in when the fans have to operate Refrigeration 2: The relay will cut in when refrigeration step 2 has to be cut in

- DO4: For either alarm, rail heat, light or hotgas defrost Alarm: Cf. diagram. The relay is cut in during normal operation and cuts out in alarm situations and when the controller is dead (de-energised)

   - Rail heat: The relay cuts in when rail heat is to operate Light: The relay cuts in when the light has to be switched on Hotgas defrost: See diagram. The relay will cut out when defrost has to be done

230 V a.c.

##### **Sensors**

S3 and S4 are thermostat sensors.

A setting determines whether S3 or S4 or both of them are to be used.

S5 is a defrost sensor and is used if defrost has to be stopped based on temperature.

##### **Data communication**

The controller is available in several versions where data communication can be carried out with one of the following systems: MOD-bus or LON-RS485.

If data communication is used, it is important that the installation of the data communication cable is performed correctly. See separate literature No. RC8AC…

##### **Digital On/Off signals**

A cut-in input will activate a function. The possible functions are described in menus o02 and o37.

##### **Electric noise**

##### **External display**

Connection of display type EKA 163A (EKA 164A).

Cables for sensors, DI inputs and data communication **must** be kept separate from other electric cables:

- Use separate cable trays

- Keep a distance between cables of at least 10 cm

- Long cables at the DI input should be avoided

Coordinated defrost via cable connections

The following controllers can be connected up in this way: AK-CC 210, AK-CC 250, AK-CC 450, AK-CC 550 Max. 10. Refrigeration is resumed when all controllers have “released” the signal for defrost.

Coordinated defrost via data communication

23

#### **Data**

|Supplyvoltage|230 V a.c. +10/-15|%. 2.5 VA,50/60 Hz|
|---|---|---|
|Sensors 3 pcs off<br>either|Pt 1000 or<br>PTC 1000 or<br>NTC-M2020(5000|ohm / 25°C)|
||Measuringrange|-60 to +99°C|
|Accuracy|Controller|±1 K below -35°C<br>±0.5 K between -35 to +25°C<br>±1 K above +25°C|
||Pt 1000 sensor|±0.3 K at 0°C<br>±0.005 Kpergrad|
|Display|LED, 3-digits||
|External display|EKA 163A||
|Digital inputs|Signal from conta<br>Requirements to c<br>Cable length mus<br>Use auxiliaryrelay|ct functions<br>ontacts: Gold plating<br>t be max. 15 m<br>s when the cable is longer|
|Electrical con-<br>nection cable|Max.1,5 mm<sup>2</sup>mult|i-core cable|
|||CE<br>(250 V a.c.)<br>UL ***<br>(240 V a.c.)|
||DO1.<br>Refrigeration|8 (6) A<br>10 A Resistive<br>5FLA, 30LRA|
||DO2. Defrost|8 (6) A<br>10 A Resistive<br>5FLA, 30LRA|
|Relays*|DO3. Fan|6 (3) A<br>6 A Resistive<br>3FLA, 18LRA<br>131 VA Pilot<br>duty|
||DO4. Alarm|4 (1) A<br>Mi 100 A**<br>4 A Resistive<br>131 VA Pilot|
|||n.  m<br>duty|
||0 to +55°C, During<br>-40 to +70°C, Duri|operations<br>ngtransport|
|Environments|20 - 80% Rh,not c|ondensed|
||No shock influenc|le / vibrations|
|Density|IP 65 from front.<br>Buttons andpacki|ngare imbedded in the front.|
|Escapement<br>reserve for the<br>clock|4 hours||
|Approvals|EU Low Voltage D<br>marking complied|irective and EMC demands re CE-<br>with|
||<br>LVD tested acc. EN<br>EMC tested acc. E|<br>60730-1 and EN 60730-2-9, A1, A2<br>N61000-6-3 and EN 61000-6-2|

* DO1 and DO2 are 16 A relays. The mentioned 8 A can be increased up to 10 A, when the ambient temperature is kept below 50°C. DO3 and DO4 are 8 A relays. Max. load must  be kept.

** Gold plating ensures make function with small contact loads

*** UL-approval based on 30000  couplings.

Danfoss can accept no responsibility for possible errors in catalogues, brochures and other printed material. Danfoss reserves the right to alter its products without notice. This also applies to products already on order provided that such alternations can be made without subsequential changes being necessary in specifications already agreed.

All trademarks in this material are property of the respecitve companies. Danfoss and Danfoss logotype are trademarks of Danfoss A/S. All rights reserved.

24
