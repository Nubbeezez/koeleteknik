# Danfoss AK-PC 551 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Pack controller Type AK-PC 551

*Kilde: Danfoss-dokument BC212486423949en-000501.pdf*

##### **User Guide**

### Pack controller Type **AK-PC 551**

Capacity control for double suction group compressor rack **SW Ver. 1.7**

**www.danfoss.com**

|**Contents**|1.<br>Introduction .........................................................................................................................................................................3|
|---|---|
||2.<br>Suction Group .....................................................................................................................................................................4|
||3.<br>Condenser .............................................................................................................................................................................5|
||4.<br>Safety functions ..................................................................................................................................................................6|
||5.<br>Display overview ................................................................................................................................................................7|
||6.<br>Set-up overview ..................................................................................................................................................................8|
||7.<br>Menu .......................................................................................................................................................................................9|
||8.<br>Connections used in “Quick configurations” .........................................................................................................21|
||9.<br>Alarm list .............................................................................................................................................................................23|
||10. Connections ......................................................................................................................................................................25|
||11. Data ......................................................................................................................................................................................27|
||12. External display ................................................................................................................................................................27|
||13. Ordering .............................................................................................................................................................................28|
||14. Mounting /Dimensions .................................................................................................................................................28|

2 | BC212486423949en-000501

#### **1. Introduction**

###### **Application**

The controller is used for capacity regulation of compressors and condensers in small refrigeration applications. A maximum of 8 compressors and one condenser can be regulated. For example:

- One suction group + one condenser group

- Two suction groups + one shared condenser (max. 4 + 4 steps)

- One compressor group, max. 8 steps

- One condenser group, max. 8 steps

###### **Advantages**

- Energy savings via:

-  Optimisation of suction pressure

-  Night time increase

-  Floating condensing pressure

-  Load limitation

###### **Input and output**

There are a limited number of available inputs and outputs. For each signal type, though, the following can be connected:

- Analogue inputs, max. 8 pcs.

- Signal from pressure transmitters, temperature sensors, voltage signal, etc.

- Digital inputs, max. 8 pcs. Signal from automatic safety control, day/night signal, etc.

- Relay outputs, max. 6 pcs. Connection of compressors, condenser fans

- Solid state outputs, max. 2 pcs.

-  Control of capacity valve on a Copeland digital scroll

-  Control of unloader on a Copeland stream compressor.

-  Control of both unloaders on a  Bitzer CRII

- If the outputs are not used for these functions, they can be used as ordinary relay outputs

- Analogue outputs, max. 4 pcs. (3 can be used by the application) Speed control of compressors or condenser fans.

###### **Operation**

The daily operation can be set up directly on the controller or via an external display device. During set-up, the display images will be adjusted so that only the relevant images are opened for additional setting and end-user operation.

The operation is password protected, and three levels of access can be granted.

The controller contains several languages. Select the preferred language at start-up.

###### **Data communication**

The controller has built-in modbus data communication, and it can be connected to an AK-SM 800 type system device.

#### **2. Suction Group**

###### **Compressor types**

The following types of compressors can be used for regulation:

- Single-step compressors (one can be speed-regulated)

- Compressor with unloaders

- Scroll compressors (one can be a digital scroll)

- Copeland Stream compressor with one unloader (4 cylinders)

- Bitzer CRII compressor with two unloaders (4-cylinders)

###### **Capacity distribution: Cyclical operation (FIFO)**

All compressors are of the same type and size, except the lead compressor if present. The compressors cuts in and cuts out in accordance with the "First In First Out" principle (FIFO) to equalise operating hours between the compressors. The lead compressor will always be cut in first, and the variable capacity is used to fill capacity gaps between the subsequent steps.

###### Timer restrictions and safety cut outs:

If a compressor is prevented from starting because it is “hanging” on the restart timer or is safety cut out, this step is replaced by another compressor.

###### **Capacity regulation**

The cut-in capacity is controlled by signals from the connected pressure transmitter/temperature sensor and the set reference. Set a neutral zone around the reference .

In the neutral zone, the regulating compressor controls the capacity so that pressure can be maintained. When it can no longer maintain the pressure within the neutral zone, the controller will cut out or cut in the next compressor in the sequence. When further capacity is either cut out or cut in, the capacity from the regulating compressor will be modified accordingly to maintain the pressure within the neutral zone (only where the compressor has variable capacity).

- When the pressure is higher than the “reference + a half neutral zone”, cut-in of the next compressor (arrow up) is permitted.

- When the pressure is lower than the “reference - a half neutral zone”, cut-out of a compressor (arrow down) is permitted.

- When the pressure is within the neutral zone, the process will continue with the currently activated compressors.

###### **Control sensor**

Normally, a suction group is controlled based on a signal from the Po pressure transmitter.

If control on a brine, the S4 sensor must be the control sensor. The Po pressure transmitter must also be installed, as it is used for frost protection.

###### **The reference**

At set or variable reference can be used for regulation. For example, the variable reference can be used for a night time increase or Po optimisation. Enter a set point here so that a contribution from the Po optimisation or night time increase is added. This contribution can raise or lower the reference, as determined by the momentary cooling need. To limit the reference from values that are too high or too low, set a max. and min. limit.

###### **Load shedding**

When the load shedding function is activated, the maximum permissible compressor capacity will be limited to the set limit. In this way, the total electrical load in the store is limited. The threshold value may not be set lower than the compressor’s lowest capacity step/”Start speed”.

*[Figurtekst: Po ref. · Max. · Min.]*

4 | BC212486423949en-000501

#### **3. Condenser**

###### **Fan control**

The fans can be controlled incrementally using the controller’s relays, or they can be speed-controlled via the controller’s analogue output.

Speed control can be via a frequency VLT-type transformer.

If the fans have EC motors, the 0 – 10 V signal can be used directly.

Step and speed simultaneously. (Parallel signals in step with each other.) This function is primarily used to control a frequency converter, but if the frequency converter fails, external wiring will switch over to step control.

During night operation, the noise level of the fans can be kept down. This is done by limiting the cutin capacity. For speed control, keep the number of revolutions low. Omit step cutin for step-by-step activation.

###### **VSD Max speed limitation**

The AO for fans are limited to VSD Max speed to decrease the noise level.

VSD Max. speed and night limitations are bypassed if safety functions Sd max. and Pc max. start to function.

*[Figurtekst: Night limitation:]*

###### **Control**

Regulation is carried out based on a signal from the Pc pressure transmitter or an S7 media temperature sensor. The signal is compared with the regulation reference.

The regulation reference can originate from one or more of the following functions:

- Fixed reference

- Variable reference, which follows the outdoor temperature. When the outdoor temperature drops, the reference will drop by a corresponding amount. This variable reference requires the installation of an Sc3 outdoor temperature sensor. The sensor must be positioned so that it registers the correct outdoor temperature. In other words, it must be shielded from direct sunlight and located near the airway of the condenser.

- This regulation requires setting a min. and max. reference, so that the regulation process is kept within the given limits.

- Increase the reference for heat recovery. Here the reference is raised to a fixed value when a signal is received on a DI input. The reference value can be higher than the set max. reference.

When the temperature of the heat recovery has been reached and the DI signal disappears, the reference will drop once again, though it will do so over the course of a few minutes to prevent abrupt changes in the reference.

###### **Media temperature**

If controlling a media temperature, the control sensor must be set to S7. This temperature sensor must be located in the desired medium.

The Pc pressure transmitter must also be installed. It is used for high-pressure monitoring.

*[Figurtekst: Max. ref. · Min. ref. · Ref. for heat recovery · Temperature sequence · for heat recovery]*

#### **4. Safety functions**

###### **Min./max. suction pressure Po**

The suction pressure is recorded continuously. If the measured value falls below the set minimum limit, the compressors will immediately cut out. If it exceeds the max. value, an alarm will be generated once the time delay has elapsed.

###### **Max. condensing pressure Pc**

If the condensing pressure reaches the upper permissible value, the controller will connect all condenser fans to keep the pressure down. At the same time, a portion of the compressor capacity will be disconnected. If the pressure remains near the threshold value, even more compressors will be disconnected.

All compressors will be disconnected immediately if the threshold value is exceeded.

###### **LP switch**

On/off signal on a DI input If a signal is received, all compressors will immediately be stopped.

###### **HP switch**

On/off signal on a DI input

If a signal is received, all compressors will immediately be stopped. Fan capacity will increase depending on how much the Pc measurement exceeds the reference.

###### **Sensor failure**

If lack of signal from one of the connected temperature sensors or pressure transmitters is registered an alarm will be given.

- In the event of a Po error, regulation will continue with a set capacity in daytime operation (e.g. 50%), and a set capacity in night operation (e.g. 25%), but with a minimum of one step.

- In the event of a Pc error, the condenser capacity that corresponds to how much compressor capacity is connected will cut in. Compressor regulation will remain normal.

- When there is an error on the Sd sensor the safety monitoring of the discharge gas temperature will be discontinued.

- When there is an error on the Ss sensor the monitoring of the superheat on the suction line will be discontinued.

- In the event of an error on the outdoor temperature sensor, Sc3, the permanent setting value will be used as a reference.

- In the event of an error on the S4 sensor, regulation will continue with the Po signal, but the reference will be lowered by 5 K.

- In the event of an error on the Saux sensor, the thermostat output will go to the rest position.

**Note:** A faulty sensor must be OK within 10 minutes before a sensor alarm is cancelled.

A sensor alarm can be reset manually by pushing  the "X-button" for 2 s when the alarm is shown in the display "Active alarms".

###### **General DI alarms**

###### **Min./max superheating via Ss measurement**

Temperature sensor on an AI input.

If superheating is higher or lower than the set limits, an alarm will be generated once the time delay has elapsed.

###### **Max. discharge gas temperature Sd**

Temperature sensor on an AI input.

A signal can be received from a Pt 1000 Ohm sensor on the pressure pipe.

- Common Sd for the whole compressor group If the temperature nears the set max. temperature, the capacity of the compressor will be reduced

- Compressor Sd if it is an Sd from a Copeland digital scroll, a Copeland stream or Bitzer CRII the capacity will be increased so that the compressor can cool down itself).

The compressors will be stopped if the temperature nears the set max. temperature value.

On/off signal on a DI input

The regulator contains three general alarm inputs, to which alarm text and delay times can be connected. Alarm and text will appear when the delay time has elapsed.

###### **General thermostat**

It is possible to install one general thermostat if there is a relay output and an analogue input available.

###### **Injection ON**

The function is used to interrupt refrigerant injection to evaporators when no compressors are available to start.

The pack controller will keep the "injection ON" signal, when a compressor is running, but also when all compressors are stopped but can be started.

Only when none of the compressors are allowed to start due to:

- pending restart timer

- minimum off timer

- safety cut-out or common safety cut-out and the suction saturation temperature exceeds 2 K above the Neutral Zone for more than 120 s (default), the "injection ON" signal is switched OFF and case controller are stopped.

The communication with case controller can use a DI or Network signal.

6 | BC212486423949en-000501

#### **5. Display overview**

###### **End-user overview**

The images in this daily user interface will depend on how the set-up is made. They will illustrate what is regulated. For example: One or two suction groups, one condenser group, or a combination. See examples below:

1 suction groupe

*[Figurtekst: 1 condenser · group]*

*[Figurtekst: 2 suction groups]*

*[Figurtekst: 2 suction groups · and · 1 condenser · group]*

Each of the four rows above is continued with three additional displays. The arrow in the top corner of the display shows the way to the next display in the same area of operation. By clicking the right arrow you can see these three displays:

*[Figurtekst: Cleared Alarms  Information on the controller]*

When an alarm is sent from the controller, you must advance to this display to see the alarm text.

#### **6. Set-up overview**

There are three ways in which the controller can be set up. Select the one that is easiest for you: either “Wizard”, “Quick settings” or a review of “all parameters”.

###### Start screen upon delivery

###### **Operating principles**

1. Select position using arrow keys

2. Select using “Enter” 

3. Use the “X” to return

Hold “Enter”  down The default password upon for 2 seconds to come to delivery is 300. Use the arrow password entry keys to set the password. End by pressing “Enter” 

Select a set-up method. End by pressing “Enter” 

**Main Menu** The first setting is the Plant type

When the Plant type has been selected, it will allow several settings to be made. For example:

###### **Wizard**

Here you will be led through a series of settings, after which the controller will be ready for start. Image 1 of 28 is displayed here.

###### **Quick**

Select from the different combinations of compressors and fans here. Also see the overview on pages 18 and 19.

- 3CDA + 2CB + FS 2CDA + 2CB + 3F

- 3CSA + 2CB + FS

###### **Example:**

3CDA + 2CB + FS = 3 Compressors, one Digital, suction group A + 2 Compressors, suction group B +

- 2CSA + 2CB + 3F

- 4CA + 3CB + FS

3CA + 2CB + FS 2CA + 2CB + 3F

4CDA + FS

3CDA + FS

3CDA + 3F

one fan, Speed controlled

2CDA + 2F

- 4CSA + FS 4CA + FS 4CA + 4F 3CSA + FS 3CA + FS 3CA + 3F None

The following options are available here: 2 Comp + 1 Cond = suction group A + B and condenser Comp. + Cond. = suction group A and condenser Condenser = condenser only Compressor = suction group A only None

Continue to the next menus. All settings are explained on the pages that follow.

8 | BC212486423949en-000501

#### **7. Menu**

SW: 1.7

|**Start/stop**<br>**Main switch**|**Main switch**<br>Start and stop regulating here.<br>The configuration settings will require that regulating is stopped.<br>If you try to enter a configuration setting when regulating has started, the controller will<br>ask if regulating should be stopped.<br>When all settings have been made and the main switch is set to “ON”, the controller will<br>enable the display of the various measurements. Regulation will start. (If an external main<br>switch has been defined,it must also be “ON” before regulatingstarts.)|On / Off|
|---|---|---|
|**Extern Main swich**|**External main switch**<br>It is possible to connect an external switch which can be used to start and stop regulating.<br>Both the internal and external main switch must be ON before regulating starts.<br>An external main switch can be defined in the menu “Plant type” - “Main switch via DI”.||
|**Plant type**|||
|**Select Plant type**|**Plant settings:**<br>The following must be regulated:<br>• Compressor group<br>• Condenser group<br>• One compressor group (A) + One condenser group<br>• Two compressorgroups(A)and(B)+ One condensergroup|Fac: None|
|**Refrigerant type**|**Refrigerant setting**<br>Before refrigeration is started, the refrigerant must be defined. You may choose between<br>the following refrigerants:<br>R12,  R22,  R134a,  R502,  R717,  R13,  R13b1,  R23,  R500,  R503,  R114,  R142b, user defined,<br>R32, R227,  R401A,  R507, R402A,  R404A, R407C,  R407A,  R407B,  R410A,  R170,  R290,  R600,<br>R600a,  R744,  R1270,  R417A,  R422A, R413A, R422D, R427A, R438A, R513A (XP10), R407F,<br>R1234ze, R1234yf, R448A, R449A, R452A.<br>Warning: Wrong selection of refrigerant may cause damage to the compressor.<br>Other refrigerants: Here Setting "user defined" is selected and then three factors - fac1, fac2<br>and fac3 and temperatureglide(if necessary).|Fac: None|
|**Unit of setpoints**|Device for controlling compressor and condenser<br>Select pressure or saturation temperature.<br>(Can be set duringinitial set-upand must**not**be subsequentlychanged.)|Temp. / press<br>Fac: Saturated|
|**Night signal via DI**|**Night time operation via DI signal**<br>Define an external switch here, so that the regulation reference can be raised and lowered<br>externally.<br>1. Set the function to “Yes”<br>2. Go to I/O configuration and select an available digital input. Set this input to<br>“Night condition”<br> i|**DI-demand**<br>No / Yes<br>Fac: No|
||3. Next,define whether the function is to be active when the signal is ON,or when it is OFF.||
|**Main Switch via DI**|i<br>**Main switch via DI**<br>Define an external main switch here, so that regulation can be started and stopped<br>externally.<br>1. Set the function to “Yes”<br>2. Go to I/O configuration and select an available digital input. Set this input to “Main switch”<br>3. Next,define whether the function is to be active when the signal is ON,or when it is OFF.|**DI-demand**<br>No / Yes<br>Fac: No|
|**Mains frequency**|**Frequency**<br>Set the net frequency|50 Hz / 60 Hz<br>Fac: 50 Hz|
|**Alarm output**|**Alarm relay**<br>Define an alarm relay here that will be activated in the event of an alarm.<br>1. Select the alarm priority that will activate the relay<br>• No relay<br>• Critical alarm<br>• Severe alarm<br>• All alarms<br>2. Go to I/O configuration and select an available digital output. Set this output to “Alarm”<br>3. Next, define whether the relay will be active (pulled) when the alarm is ON, or when it is<br>OFF.|**DO-demand**<br>Fac: No relay|
|**Alarm buzzer**|**Alarm sound**<br>Here the sound generator can be defined to emit a sound in the event of an alarm.<br>Select which alarm priority will activate the sound generator:<br>• No buzzer<br>• Critical alarm<br>• Severe alarm<br>• All alarms<br>(In the event of an alarm, the sound generator can be stopped by moving across the<br>active alarm screen;seepage 6)|Fac: No buzzer|

|**Suction A**<br>**Control status**|**Regulation status**||
|---|---|---|
|Control status|Read the status of the control circuit here e.g.:<br>• No comp. - No compressor capacity available<br>• Normal ctrl - Normal control<br>• Alarm Comp. - Cannot start compressor due to alarm condition<br>• ON timer - Cannot stop compressor due to ON timer restriction<br>• Start timer - Cannot start compressor due to Start timer restriction<br>• Normal ctrl - Normal control - no compressor staging<br>• Inj. On Delay - Waiting for injection on delay to expire<br>• Cascade<br>• 1st comp del - First compressor run timer<br>• Pump down - Last compressor running to pump down limit<br>• Sensor error - Emergency control due to sensor error<br>• Load shed - Load shedding function active<br>• Sd High - Capacity control in High Sd safety prevention mode<br>• Pc High - Capacity control in High Pc safety prevention mode<br>• Manual ctrl - Capacity control in manual mode<br>• Main switch OFF - OFF||
|Actuel zone|You will be able to see how the regulation is in relation to the reference here:<br>P0 error: No regulation<br>- Zone: The desired pressure is below the reference value<br>NZ: The pressure is in place in relation to the reference value<br>+ Zone: The desiredpressure is above the reference value||
|Control temp.|The current value of the regulation sensor can be read here||
|Reference|The total regulation reference can be read here||
|Runningcapacity|Here the connected capacitycan be read as a % of total capacity||
|Requested capacity|Here thepreferred connected capacitycan be read as a % of total capacity||
|No. of runningcomp.|The number of compressors in operation can be read here||
|PoA Pressure|The measuredpressure for the PoApressure transmitter can be read here||
|ToA Saturated temp.|The measured PoApressure converted to temperature can be read here||
|MC PoA offset|The size of a reference displacement on Po required from the system unit||
||(suctionpressure optimisation function)can be read here||
|Pc Pressure|The measuredpressure forpressure transmitter Pc can be read here||
|Tc Saturated temp.|The measured Pcpressure converted to temperature can be read here||
|Day/ Night status|The status of the day/night function can be read here||
|Load shed|The status of the load shed function can be read here||
|Injection ON A|The status of the injection ON signal sent to the evaporator controllers can be read here||
|MC Load Shedding|The status of the load shed signal received from the system device can be read here||
|MC Night Setback<br>**Control settings**|The status of the night increase signal received from the system device can be read here<br>**Regulation settings**||
|Control mode|Regulation type<br>The regulation is normally set to “Auto”, but it can be changed to “Off” or “Manual”.<br>When setting to “Manual”, a forced capacity setting can subsequently be entered in %.|MAN / OFF / AUTO<br>Fac: AUTO<br>Min: 0 %<br>Max: 100%|
|Setpoint|Enter the set point for the regulation (regulation reference = set point + different offsets) here<br>An offset can originate from a night increase signal or from an override function on the<br>system device.|Min: -80°C (-1.0 bar)<br>Max: 30°C (50 bar)<br>Fac: -15°C (3.5 bar)|
|Neutral zone|Set the neutral zone around the reference here. Also see the illustration on page 3.|Min: 0,1 K (0.1 bar)<br>Max: 20 K (5.0 bar)<br>Fac: 6 K (0.4 bar)|
|Night offset|If necessary, set the value by which the reference will be raised at night.<br>Keep the setting at 0 if regulating with Po optimisation from a system device.|Min: -25 K (-5.0 bar)<br>Max: 25 K (5.0 bar)<br>Fac: 0 K (0.0 bar)|
|Max Reference|Set the highest permissible regulation reference here|<br>Min: -50°C (-1.0 bar)<br>Max: 80°C (50.0 bar)<br>Fac: 80°C (40.0 bar)|
|Min Reference|Set the lowest permissible regulation reference here|<br>Min: -80°C (-1.0 bar)<br>Max: 25°C (40.0 bar)<br>Fac: -80°C (-1.0 bar)|
|PI control selection|Set how quickly the PI regulation must react here: 1 = slowly, 10 = very quickly.<br>(For “Custom” setting 0, the special settings options will open, i.e. Kp, Tn and time settings<br>around the neutral zone. These options are onlyfor trained staff.)|<br>Min: 0 (custom)<br>Max: 10<br>Fac: 5|
|Gain factor Kp|The amplification factor, Kp (can only be seen and set when the previous menu is set to “0”)||
|Integration time Tn|Integration time Tn(see above)||
|+ Zone rate of change|Change coefficient for + zone (see above)||
|<br>- Zone rate of change|fi<br>Change coefficient for - zone (see above)||

10 | BC212486423949en-000501

|First step runtime|At start-up, the cooling system must have time to cool down before PI regulation takes over<br>the regulation role and can cut in the next compressor.<br>Set the time before the next compressor maybe started here.|Min: 0 s<br>Max: 300 s<br>Fac: 120 s|
|---|---|---|
|Pump down|Pump-down function<br>To avoid too many compressor starts/stops at a low load, it is possible to define a pump-<br>down function for the last compressor. In this case, the compressor will be cut out when the<br>current suction pressure is down at the set “Pump-down limit Po”.<br>(The setting must be greater than the safety limit for low suction pressure “PoA Min Limit”.)|Yes /No<br>Fac: No<br>Min: -80°C (-1.0 bar)<br>Max: 30°C (50.0 bar)<br>Facb: -40°C (0.3 bar)|
|Load shed  limit|Capacity limitation at “low shed signal”<br>Set how much compressor capacity can be cut in when a signal is received from either a DI<br>input or a system device via data communication.|Min: 0 %<br>Max: 100%<br>Fac: 100%|
|Emergency cap. day|Emergency capacity in the event of a malfunction of the regulation sensor (suction pressure<br>sensor)<br>Set the desired capacity that will apply during daytime operation.<br>(If the S4 media temperature sensor becomes damaged/defective,use Po for regulation.)|Min: 0 %<br>Max: 100%<br>Fac: 50%|
|Emergency cap. night|Emergency capacity in the event of a malfunction of the regulation sensor (suction pressure<br>sensor)<br>Set the desired capacity that will apply during night operation.<br>(If the S4 media temperature sensor becomes damaged/defective,use Po for regulation.)|Min: 0 %<br>Max: 100%<br>Fac: 25%|
|Comp. start delay|Delay of compressor start after forced closing of expansion valves (at the end of a forced<br>close signal)<br>The delay will result in the system device receiving a start signal for all the evaporator con-<br>trols involved before the first compressor is started.|Min: 0 s<br>Max: 180 s<br>Fac: 30 s|
|Injection OFF delay|Delay of the forced closing of expansion valves, if the controller calls for cut in of compres-<br>sors, but the compressors are in a locked situation and therefore cannot start.|Min: 0 s<br>Max: 300 s<br>Fac: 120 s|
|**Configuration**|**Configuration**||
|Control sensor|Select the regulating sensor for the suction circuit:<br>• Pressure transmitter Po<br>• Media temperature sensor S4 (brine regulation). (Po is used for safety)|**AI-demand**<br>Po / S4<br>Fac: Po|
|Compressor mode|Set the type of compressor to be used for regulation:<br>• Multi all:****<sup>)</sup>All compressors have unloaders<br>• Multi + Single:****<sup>)</sup>First compressor has unloaders. The remaining ones are one-step units<br>• Speed+Multi: ***<sup>)</sup>First compressor is speed-controlled. The remaining ones are with unload-<br>ers.<br>• Speed+Single: ***<sup>)</sup>First compressor is speed-controlled. The remaining ones are<br>one-step units<br>• CRII4+Multi **<sup>)</sup>First compressor is CRII4 compressor. The remaining ones are with unloaders<br>• CRII4+Single **<sup>)</sup>First compressor is CRII4 compressor. The remaining ones are<br>one-step units<br>• Stream 4+Multi: **<sup>)</sup>First compressor is a stream compressor. The remaining ones are with<br>unloaders<br>•  Stream 4+Single: **<sup>)</sup>First compressor is a stream compressor. The remaining ones are<br>one-step units<br>• Digital scroll: *<sup>)</sup>First compressor is a digital scroll. The remaining ones are one-step units<br>• Single-step only: All are one-step compressors<br>• None:|**DO-demand /**<br>**AO-demand**<br>Fac:<br>Single step only|
|No. of compressors|Set the number of compressors on the suction circuit<br>This is a total amount.<br>(If both suction groups are selected, the max. number will be 4 for A and 4 for B.)|**DO-demand**<br>Min: 1<br>Max: 8<br>Fac: 0|
|Lead comp. size|Set the nominal compressor capacity for the first compressor (it is defined under<br>“Compressor mode”)<br>That is, the capacity of either a “Digital scroll”, “Stream”, “Variable speed CRII” or<br>“First compressor with unloaders”|Min: 1 kW<br>Max: 100 kW<br>Fac: 1 kW|
|Comp. size|Set the nominal compressor capacity of the other compressors<br>For single-step only:  All are of the same size, including the first.<br>For unloader all:  All are of the same size,includingthe first.|Min: 1 kW<br>Max: 100 kW<br>Fac: 1 kW|
|VSD Min. speed|i<br>***:  For speed<br>Min. speed at which the compressor will cut out|Min: 10 Hz<br>Max: 60 Hz<br>Fac: 30 Hz|
|VSD Start speed|***:  For speed<br>Minimum speed at which the compressor will start (must be set to a higher value than<br>“VSD Min. speed”)|Min: 20 Hz<br>Max: 60 Hz<br>Fac: 45 Hz|
|VSD Max speed|***:  For speed<br>Highest permitted speed for compressor|Min: 40 Hz<br>Max: 120 Hz<br>Fac: 60 Hz|

|PWM period time|*, **:  For “Scroll” and “Stream”<br>Set the period time for the unloader valve (on time + off time)|Min: 10 s<br>Max: 20 s<br>Fac: 20 s|
|---|---|---|
|CRII Period time|**:  For CRII<br>Set the period time for the unloader valve (on time + off time)|Min: 10 s<br>Max: 20 s<br>Fac: 60 s|
|Comp. 1 min cap.|*:  For scroll and CRII<br>Minimum capacity in the time period (without a minimum capacity the compressor<br>will not be cooled)|Min: 10%<br>Max: 50%<br>Fac: 10%|
|Comp. 1 start cap|*:  For scroll and CRII<br>Start capacity: the compressor will only start when the capacity requirement reaches<br>the value|Min: 10%<br>Max: 60%<br>Fac: 30%|
|Comp. 1 Sd temp.|*, **:  For “Scroll”, “Stream” and CRII<br>Define whether the controller should monitor the discharge gas temperature Sd from the<br>compressor (NTC 86K or Pt 1000 Ohm).|**AI-demand**<br>No / Yes<br>Fac: No|
|Comp. 1 Sd max.|*, **:  For Scroll, Stream, CRII and**yes**to “Comp.1 Sd temp”<br>Set the maximum Sd temperature|Min: 0°C<br>Max: 195°C<br>Fac: 125°C|
|No.of unloaders|****:  For compressor with unloaders<br>Set how many unloaders there are on the compressor|**DO-demand**<br>Min: 1<br>Max: 3<br>Fac: 1|
|Comp. safety input|Compressor safety circuit<br>Define whether a DI input should be reserved for registration of each compressor safety<br>circuit|**DI-demand**<br>Yes /No<br>Fac: Yes|
|LP switch via DI|Low pressure safety circuit<br>Define whether a DI input should be reserved for registration of the signal from an LP switch|**DI-demand**<br>Yes /No<br>Fac: No|
|Load shedding via DI|Load limitation<br>Define whether a DI input should be reserved for registration of the signal from<br>a power meter<br>•  None:<br>•  DI: Load limitation must follow a DI input<br>•  Night Mode: Load limitation must follow the status of the day/night signal.<br>(The day/night signal can be received via a DI input,via time schedule or network.)|**DI-demand**<br>Yes /No<br>Fac: No|
|Sd disch. gas temp.|Shared discharge temperature<br>Define whether signals from a common Sd sensor on the suction line (Pt 1000) should be<br>received|**AI-demand**<br>Yes /No<br>Fac: No|
|Ss suction superheat|Monitoring of superheat<br>Define whether a signal from a common Ss sensor on the suction line should be received|**AI-demand**<br>Yes /No<br>Fac: No|
|Injection ON function|Stop injection into evaporators<br>If the compressors are prevented from starting, stop injection into the evaporators.<br>Here define whether the function should be active and how the signal should be<br>communicated.<br>No: The function is not used<br>Network: The controller sends a signal to the system unit, which then forwards it to<br>the evaporator controls<br>Relay: The function reserves a relay that pulls in if all compressors are stopped.<br>All evaporator controls must be wired to this signal from the relay.|**DO-demand**<br>No /Network /Relay<br>Fac: No|
|**Compressor timers**|**Compressor timers**||
|Lead comp. Min ON|Min. On-time for first compressor<br>Set a forced On-time here during which the compressor will remain in operation before it<br>can be switched off again. The setting is to prevent incorrect operation.<br>To prevent a compressor breakdown, the setting must be made in accordance with the<br>requirements of the compressor supplier.|Min:  0 min<br>Max:  60 min<br>Fac: 0 min|
|Lead comp. Min OFF|Min. Off-time for first compressor<br>Set the forced Off-time during which the compressor must be off before it can be switched<br>on again. The settingis toprevent incorrect operation.|Min:  0 min.<br>Max: 30 min<br>Fac: 0 min|
|Lead comp. Restart|Min. period of time for re-starting the first compressor.<br>Set the forced Off-time during which the compressor must be off before it can be switched<br>on again. The setting is to prevent incorrect operation.<br>To prevent a compressor breakdown, the setting must be made in accordance with the<br>requirements of the compressor supplier.|Min:  1 min.<br>Max:  60 min<br>Fac: 4 min|
|Lead comp. Safety<br>delay|Delay time before compressor no. 1 cut out for reasons of safety<br>The time begins when a signal is received on the DI input (configure the DI input via<br>“Configuration” and “Comp. safetyinlet”).|Min:  1 min.<br>Max:  10 min<br>Fac: 1 min|

12 | BC212486423949en-000501

|Comp. Min ON|Min. On-time for remaining compressors<br>Set a forced On-time here durin which the comressor will remain in oeration before it|Min:  0 min.<br>Max:  60 min|
|---|---|---|
||g   p    p<br>can be switched off again. The settingis toprevent incorrect operation.|Fac: 0 min|
|Comp. Min OFF|f<br>Min. Off-time for remaining compressors<br>Set the forced Off-time during which the compressor must be off before it can be switched<br>on again. The settingis toprevent incorrect operation.|Min:  0 min.<br>Max:  30 min<br>Fac: 0 min|
|Comp. Restart|Min. period of time for restarting remaining compressors<br>Set the forced Off-time during which the compressor must be off before it can be<br>switched on again. The settingis toprevent incorrect operation.|Min:  1 min.<br>Max:  60 min<br>Fac: 4 min|
|Comp. Safety delay|Delay time before compressors cut out for reasons of safety<br>The time begins when a signal is received on the DI input (configure the DI input via<br>“Configuration” and “Comp. safetyinlet”).|Min:  1 min.<br>Max:  10 min<br>Fac: 0 min|
|**Compressor status**|**Compressor status**||
|Comp. 1 Sdgas|Read the Sd temperature of the compressor here.||
|Comp. 1 status|Read the operating status for compressor 1 here. The following information may appear:<br>Alarm - Alarm situation<br>Main Sw. off - Compressor is stopped<br>Manual ctrl. - Compressor is cut out on safety input (DI safety input)<br>High Sd temp. - Stopped due  to high Sd temperature<br>Ready - Compressor is ready to start<br>OFF timer - Compressor is waiting for Min OFF timer to expire<br>Min. ON timer - Compressor is waiting for Min ON timer to expire<br>Running - Compressor is running||
||<br>Disabled - Compressor has been taken out of operation(compressor service)||
|Comp. 2....<br>|The same function for the remainingcompressors<br>||
|**Compressor capacity**|**Compressor capacity**||
|Comp. 1 cap|Read the connected capacityof the compressor(0-100%)here||
|Comp. 2......|The same function for the remainingcompressors||
|**Compressor runhours**|**Compressor run hours**||
|Reset runtime/cycles|Reset all of the hour counters and start counters for the subsequent compressors here.||
|Comp.1 Runtime L|Read the total operatingtime of the compressor(in hours)here||
|Comp.2.....|The same function for the remainingcompressors||
|**Compressor cycles**|**Compressor cycles**||
|Comp.1 Cycle total|Read the number of times the compressor has been started here||
|Comp.2.....|The same function for the remainingcompressors||
|**Compressor service**|**Compressor service**||
|Comp.1 out of service|The compressor can be taken out of operation, so that the controller regulates without this<br>compressor.<br>No = Normal regulation|Yes /No<br>Fac: No|
||<br>Yes = Regulatingis carried out without this compressor,and no alarms aregenerated byit.||
|Comp.2.....|The same function for the remainingcompressors||
|**Suction B**|||
||Suction group B. Please see descriptions under suction group A<br>(Bitzer CRII can not be used in suctiongroupB.)||
|**Condenser**|||
|**Control status**|**Regulation status**||
|Control status|Here you can read the status of the condenser circuit, e.g.:<br>• Main Sw. off - Main switch = OFF<br>• Ready - Capacity control is ready<br>• Running - Capacity control is in normal run mode<br>• Capacity control is stopped because all compressors are stopped<br>• Manual ctrl - Capacity control is set in manual control mode<br>• High Pc/Sd - Capacity forced to 100% due to High Pc/High Sd prevention functions<br>• Safety limit - Capacity forced to 100% due to external HP switch/HP safety/Sd safety limit<br>violation||
||• Night limit - Capacitycontrol limited due to night silencer limitation||
|Control temp.|The current value of the regulation sensor can be read here||
|Reference|The total regulation reference can be read here||
|Runningcapacity|Here the connected capacitycan be read as a % of total capacity||
|Requested capacity|Here thepreferred connected capacitycan be read as a % of total capacity||
|No. of runningfans|The number of fans in operation can be read here||
|Tc Saturated temp.|The measured Pcpressure converted to temperature can be read here||
|Pc Pressure<br>|The measuredpressure forpressure transmitter Pc can be read here<br>||
|S7 Media|Here the measured media temperature with sensor S7 can be read (only if S7 has been<br>selected as the regulation sensor during“Fan configuration”)||

|Sc3 air on cond.<br>Heat recoverystatus|The measured outdoor temperature with sensor Sc3 can be read here<br>Here the status of the heat recoveryfunction can be read||
|---|---|---|
|<br>HP safetyswitch|<br>The status of the HP safetyswitch can be read here||
|**Control settings**|**Control settings**||
|Control mode|Regulation type<br>The regulation is normally set to “Auto”, but it can be changed to “Off” or “Manual”.<br>When setting to “Manual”, capacity can then be forced set in %.|MAN / OFF / AUTO<br>Fac: AUTO<br>Min: 0 %<br>Max: 100%|
|Setpoint|Enter the set point for the condenser regulation here.<br>Also set a value if regulating with a fluid reference (set point value used in the event of an<br>outside temperature sensor error).|Min: -25°C (-1.0 bar)<br>Max: 90°C (159 bar)<br>Fac: 35°C (15.0 bar)|
|Sc3 offset|Temperature offset for regulation with fluid reference.<br>Regulation reference = Sc3 measurement + Sc3 offset|Min: 0 K<br>Max: 20 K<br>Fac: 6 K|
|Min. reference|Set the lowest permissible regulation reference here|Min: -25°C (-1.0 bar)<br>Max: 100°C (159 bar)<br>Fac: 10°C (5.0 bar)|
|Max. reference|Set the highest permissible regulation reference here|Min: -25°C (-1.0 bar)<br>Max: 100°C (159 bar)<br>Fac: 50°C (35.0 bar)|
|Heat recocery SP|Temperature set point for heat recovery function (only when the function is selected during<br>configuration)|Min: 20°C (-1.0 bar)<br>Max: 90°C (159 bar)<br>Fac: 50°C (30.0 bar)|
|Heat rec. ramp down|Ramp-down of regulation reference after heat recovery<br>Set how quickly the reference for condenser pressure should be made after heat recovery<br>ends. Enter the change in degrees Kelvinper minute.|Min: 0,1 K<br>Max: 100 K<br>Fac: 1 K|
|Capacity limit night|Capacity limitation at night<br>The speed of the fans can be limited here when regulating using speed control.<br>Duringstep-by-stepactivation,the start of the step-by-step process is limited.|Min: 0 %<br>Max: 100%<br>Fac: 100%|
|Gain factor Kp|Amplification factor for PI regulation<br>If the Kp value is lowered, regulation runs more smoothly|Min: 0.5<br>Max: 50<br>Fac: 10|
|Integration time Tn|Integration time for PI regulation<br>If the Tn value is increased, regulation will run more smoothly|Min: 10 s<br>Max: 900 s<br>Fac: 180 s|
|**Fan configuration**|**Configuration of fans**||
|**i**<br>Control sensor|**i**<br>Selection of regulation sensor:<br>• Pc pressure transmitter<br>• S7 media temperature sensor (Pc must be installed for safety monitoring)|**AI-demand**<br>Pc / S7<br>Fac: Pc|
|Reference mode|Set the reference for regulation here<br>• Fixed reference; the reference here will be the defined set point<br>• Variable reference; the reference here will follow the outside temperature, which is meas-<br>ured with Sc3.|**AI-demand**<br>Setpoint / Floating<br>Fac: Setpoint|
|Capacity ctrl. mode|Set the way in which the fans should be controlled here<br>• Variable; the fans are controlled by a 0-10 V signal from an analogue output. If it is defined in<br>“VSD Start via DO”, a relay will be able to start and stop the frequency converter.<br>• Step; on/off control of fans will be via relays<br>• Variable + step. The signals are parallel, so external wiring can switch over to step, e.g. if the<br>frequencyconverter fails.|**AO-demand**<br>Step / Speed<br>Fac: Step|
|No. of fans|Enter the number of fans here.<br>For step-by-step activation, select the number of relays. The relays will cut in/out sequentially,<br>e.g. 123-321.<br>For speed control, select 1 or higher. No relay is reserved, but the setting makes it possible to<br>define the monitoringof fans.|**DO-demand**<br>Min: 0<br>Max: 8<br>Fac: 0|
|Control type|i<br>Normally, PI-regulation is used, but this can be changed to a P-regulation if the design of the<br>system necessitates this.<br>• PI Ctrl: Regulation is carried out here with as little deviation between the reference and<br>measurement as possible.<br>• P-band ctrl: Capacityis cut in here afterproportional regulation.|P / PI<br>Fac: PI|
|VSD Start speed|<br>Set the start value of the frequency converter here.<br>The value must be higher than the VSD min. speed value.|Min: 0%<br>Max: 60%<br>Fac: 35%|
|VSD Min. speed|Set the minimum speed of the frequency converter here.<br>If lower capacity is required, this minimum speed should be maintained all the way down to<br>0% capacity. At 0% capacity,the system stops completely.|Min: 0%<br>Max: 40%<br>Fac: 20%|
|VSD Max. speed|Set the maximum speed of the frequency converter here.<br>|Min: 61%<br>M 100%|
||The maximum speed used under normal control.<br>In case of high PC or high Sd then VSD maxspeed is ignored.|ax:<br>Fac: 80%|

14 | BC212486423949en-000501

||VSD Start via DO|Define whether a relay should be connected to the frequency converter start/stop function<br>here:<br>• No: no relay<br>• Yes: the relay pulls in when the frequencyconverter needs to be in operation.|**DO-demand**<br>Yes / No<br>Fac: No|
|---|---|---|---|
||Monitor fan safety|Define whether safety monitoring of the condenser fans should be performed.<br>• None: no monitoring<br>• Individual: a DI input is reserved for each fan<br>• Common: a DI input that is common for all condenser fans is reserved .|**DI-demand**<br>Common /Indi-<br>vidual<br>Fac: None|
||Fan at comp. OFF|Select the way in which the fans should be controlled when all the compressors have<br>stopped.<br>• Normal regulation: Fans to be controlled in compliance with normal regulation.<br>• Energy-optimised: Fan capacity will be maintained at between 0 and 49% in a p-band of 5 –<br>15 K above reference.|Normal/Optimized<br>Fac.: Normal|
||Heat recovery via DI|Define whether a heat recovery cycle should be started with a signal on a DI input here.<br>• No: No function<br>• Yes: A DI input is reserved. When a signal is registered, the heat recovery function reference<br>will become active.|**DI-demand**<br>Yes / No<br>Fac: No|
||**Fan status**|**Fan status**||
||Fan speed|Here a readingof the desired condenser fan capacityisprovided in %||
||VSD start/stop|Fan operation(frequencyconverter)status can be read here||
||Fan 1<br>|The status of relay1(step1 or relayfor frequencytransformer)is indicated here<br>||
||Fan 2.....|The status of relay2,3,etc.(step2,3,etc.)is indicated here||
||**Fan Runhours**|**Fan Run hours**||
||VSD Runtime total|The number of hours the fans have been in operation (frequency converter operation) can<br>be read here||
||Fan 1 Runtime total|The number of hours fan relay 1 has been in the On-position (frequency transformer<br>has been On)is indicated here||
||Fan 2.....|The same function for the remainingfans||
||**Fan cycles**|Number of fans starting||
||VSD cycles|The number of fan starts(frequencyconverter)can be read here||
||Fan 1 Cycles total|The number of times fan relay 1 has been in the On-position (frequency converter<br>has been on) is indicated here<br>The controller checks that the fan has been active within the last 24 hours. If not,<br>it will be forced to start in 5 minutes,in rotation with the other fans.||
||Fan 2...|The same function for the remainingfans||
|**Safety**|**monitoring**|||
||**PoA Min limit**|**Safety limits for min. PoA**<br>If a low value is registered, all compressors will cut out|Min: -120°C (-1.0 bar)<br>Max: 30°C (159 bar)<br>Fac: -40°C (0.5 bar)|
||**PoA Max alarm**|**Alarm limit for high PoA**<br>If a high value is registered, an alarm will be generated<br>If a higher value is registered during a load limitation, the load limitation will be cancelled<br>until Po has returned to the reference.|Min: -30°C (-1.0 bar)<br>Max: 100°C (159 bar)<br>Fac: 100°C (5.0 bar)|
||**PoA Max delay**|**Delay time for issuing a PoA max. alarm**|Min: 0 min.<br>Max: 240 min.<br>Fac: 5 min.|
||**Superheat Min lim A**|**Alarm limit for insufficient superheating**<br>(Superheating is measured in the suction line by PoA and SsA.)|Min: 0 K<br>Max: 20 K<br>Fac: 0 K|
||**Superheat Max lim A**|**Alarm limit for excess superheating**|Min: 20 K<br>Max: 80 K<br>Fac: 80 K|
||**Superheat delay A**|**Delay time before alarm is generated for insufficient or excess superheating**|Min: 0 min.<br>Max: 60 min.<br>Fac: 5 min.|
||**SdA Max limit**|**Safety limit for max. SdA**<br>At 10 K under the set value, the compressor capacity will be reduced, and the entire<br>condenser capacity will cut in.<br>If the threshold is exceeded,the entire compressor capacitywill cut out.|Min: 0°C<br>Max: 195°C<br>Fac: 80°C|
||**PoB Min limit**|**Same settings for a suction group B**||
||**PoB Max alarm**|||
||**PoB Max delay**<br>**Superheat Min lim B**|||
||**Superheat Max lim B**<br>|||
||**Superheat delay B**<br>**SdB Max limit**|||

||**Pc max limit**|**Safety limit for max. Pc**<br>If Pc exceeds the value set here minus 3 K, the entire condenser capacity will cut in,<br>and compressor capacity will be reduced by 1/3 for every 30 seconds.<br>If Pc exceeds the threshold value, the entire compressor capacity will immediately cut out,<br>and an alarm will begenerated when the delaytime expires.|Min: -1 bar<br>Max: 159 bar<br>Fac: 40 bar|
|---|---|---|---|
||**Tc Max limit**|**Safety limit for max. Tc**<br>The above settingfor Pc max. limit can be read as a temperature here.|-|
||**Pc Max delay**|**Time delay for Pc max. alarm**<br>The alarm will only be generated when the time delay has elapsed.|Min: 0 min.<br>Max: 240 min.<br>Fac: 0 min.|
||**HP switch via DI**|**Signal from an HP switch**<br>Define whether a signal is to be received on a DI input here.<br>The status of the signal can be read, and an alarm can be linked to it.<br>Once a signal is received,compressor capacitywill cut out.|**DI-demand**<br>Yes /No<br>Fac: No|
||**Safety restart time**|**Delayed start-up following safety cut-out**<br>If a safety cut-out has occurred due to “Sd max. limit”, “Pc max. limit” or “Po min. limit”,<br>the compressors must be kept stopped for a defined period of time. The amount of<br>time can be set here.|Min: 0 min.<br>Max: 60 min.<br>Fac: 1 min.|
||**Sensor alarm reset**<br>|**Reset alarm after sensor error**<br>When a sensor error has occurred, an O.K. signal must be registered within a specified<br>number of minutes before the controller resets the alarm. The regulation will be resumed<br>as soon as the sensor signal is O.K.|Min: 0 min.<br>Max: 30 min.<br>Fac: 10 min.|
|**Gener**|**al functions**<br>**Digital input alarms**|**General on/off alarm**<br>Here you can define up to 3 alarms that are not related to the regulation function. When<br>a signal is received on the input, the controller will generate an alarm, but only after the<br>related delay time has elapsed.<br>The alarm can be defined to be active for an on/off signal.<br>An alarm text can be entered for the alarm. This text can be seen in the display and can<br>be sent to a system device.||
|||1. Define the appurtenant alarm text<br>2. Set the delay time for the alarm<br>3. Go to I/O configuration and select an available digital input. Set this input to “General<br>alarm (no.)”<br>4. In the subsequent menu,define whether the alarm is to be active for an on/off signal.||
||No. of DI alarm fct.|1. Define how many general alarms there should be|**DI-demand**<br>Min: 0<br>Max: 3<br>Fac: 0|
||DI1 Alarm text|The following alarm texts can be selected:<br>• General alarm<br>• High pressure alarm<br>• Low pressure alarm<br>• High temperature alarm<br>• Low temperature alarm<br>• Oil level alarm<br>• Oil temperature alarm<br>• Liquid level alarm<br>• Leak detection alarm<br>• Inverter fault||
||Di1 Alarm delay|Delay time for the DI1 alarm|Min: 0 min.<br>Max: 360 min.<br>Fac: 5 min.|
||DI2....3|The same settingoption for a DI2 alarm and a DI3 alarm.||
||**Thermostat**|**General thermostat**<br>One general thermostat can be defined.<br>1. Define the function<br>2. Go to I/O configuration and select an available analogue input. Set this input to<br>“Saux thermostat”<br>3. Go to I/O configuration and select an available relayoutput. Set the output to “thermostat”.|**AI-demand**<br>Yes / No<br>Fac: No|
||Thermostat cut in|Here set the temperature value at which the thermostat will cut in|Min: -50°C<br>Max: 150°C<br>Fac: 5°C|
||Thermostat cut out|Here set the temperature value at which the thermostat will cut out|Min: -50°C<br>Max: 150°C<br>Fac: 10°C|
||Thermostat temp.|The current sensor temperature of the thermostat can be read here<br>(But onlyonce the sensor input has been defined and the main switch has been set to “On”.)|-|

16 | BC212486423949en-000501

|**System**||||
|---|---|---|---|
||**Display**|**Select views on the display**|-|
||Language|Choose from the following languages:<br>English, German, French, Danish, Spanish, Italian, Portuguese, Dutch, Russian, Polish, Czech,<br>Turkish,Hungarian,Croatian,Serbian,Romanian|Fac: UK English|
||Engineering units|Device<br>Select SI or Imperial (when settingthe compressor capacitywith U.S. values).|SI / Imperial<br>Fac: SI|
||Pressure units|Pressure unit<br>Select bar or PSIG|Bar / PSIG<br>Fac: bar|
||Temperature units|Temperature unit<br>Select °C or °F.|°C / °F<br>Fac: °C|
||Time format|Time format<br>Choose 12-hour or 24-hour format.|12 / 24<br>Fac: 24 h|
||Screen saver time|Screen saver time<br>If no buttons have been pushed for a specific period of time, the light in the display will be<br>minimised.<br>The light level will be restored upon renewed activity.|Min: 1 min.<br>Max: 60 min.<br>Fac: 1 min.|
||User logout time|Log-off time<br>If buttons have not been pressed within a specified period of time, the screen will return to<br>the overview display.  Afterwards, the user will have to log on again.<br>If the time is changed, the new time will apply the next time the user logs in.<br>If you log out here without waiting for the time-out period to elapse, go to the overview<br>displayand hold down the “X” button for 3 seconds.|Min: 1 min.<br>Max: 60 min.<br>Fac: 2 min.|
||Display contrast|Adjust contrast|Min: 0<br>Max: 100<br>Fac: 30|
||**Password**|**Access code**<br>||
||Password level 1|The settings in the controller can be protected with three levels of access codes.<br>|Fac: 100|
||Password level 2|Level 1: End user settings, such as changing the weekly plan<br>Level 2: Adjusting installer level|Fac: 200|
||Password level 3|<br>Level 3: Configuration of system settings (configuration menu)<br>The access code is a number between 001 and 999.<br>**Note:**If thepassword is duplicated then logon is for the highest level user.|Fac: 300|
||**Real time clock**|**Date and time**<br>Used byweekly plan and alarm function.|Year, month, date<br>Hours, minutes|
||**Weekly schedule**|**Weekly plan**<br>Set the opening and closing hours of the store here<br>The times can be used to change the regulation reference for suction pressure and for lower<br>fan speeds at night.|-|
||Mondayopen|Time of opening,Monday|Hours, minutes|
||Mondayclose|Time of closing,Monday|Hours, minutes|
||Tuesdayop.....|Times for remainingweekdays|-|
||**Network**|**Network**|**-**|
||Modbus Address|Set the address of the controller here if it is connected to a system device via data<br>communication.|Min: 0 1<br>Max: 120<br>Fac: 1|
||Baudrate|The system unit usually communicates with 38.4.<br>If it is changed in the system unit to for example, "SLV" mode (19.2), setting must also be<br>changed to 19.2 here in the controller.|Fac: 384|
||Serial mode|The value must not be changed|Fac: 8E1|
||**Reset to factory**|**Return to factory settings**<br>If this function is set to “YES”, all settings will be returned to factory default settings, and the<br>alarm list will be cleared.||

|**I/O con**|**figuration**|||
|---|---|---|---|
||Here you can select functio<br>have been set up via the coi<br>For digital outputs, define w<br>For digital inputs, define wh          f<br>For analogue outputs, defin<br>For analogue inputs, define:<br>Temperature sensors:<br>Normally, the sensor type is<br>86K @ 25 °C can also be sel<br>Calibration value (+/- 10°C)<br>Pressure sensors:<br>Signal type: 0 – 20 mA, 4 – 2<br>Minimum and maximum pr<br>Calibration value (+/- 5.0 ba<br>If you have used “Quick coni<br>set up (for additional inform    i<br>Limitations:<br>PWM outputs for digital scr<br>Pressure transmitters with a<br>**Note:**<br>If a function has been conn            i<br>in question will be marked<br>configuration,or deselect t|ns for the individual inputs and outputs. To prevent faulty settings, only select functions that<br>nfiguration menus for the suction groups and the condenser.<br>i hether the function will be active for an activated or deactivated relay.<br>i ether the function/alarm will be active for an interrupted or shut-off switch.<br>ie whether the output signal should be 0 – 5 V or 0 – 10 V<br>a Pt1000 model, but for digital scroll/stream discharge gas temperature monitoring, an NTC<br>ected.<br>0 mA, AKS32 (1 – 5 V) or AKS32R (10 – 90% ratiometric of 5 V supply voltage)<br>essure range<br>r)<br>figurations” or “Wizard” to set up the controller, the inputs and outputs will be automatically<br>ation, see the “Quick configuration” or “Wizard” sections)<br>oll or stream compressors can only be selected on DO5 or DO6<br>current signal of 0 – 20 mA or 4 – 20 mA must be placed on analogue inputs AI1-AI4<br>ected to an input or output and is subsequently deselected in the configuration, the function<br>with an exclamation mark (!). In this case, you must either activate the function in the<br>he function on the input or output inquestion.||
||**Digital outputs**<br>1:<br>2:<br>3:<br>4:<br>.<br>.<br>8:|**On/off outputs**<br>When a function that needs to use an output is defined, it will be possible to select<br>this function on one of the available relay outputs.<br>Select a relay and continue with the setting. In the last setting you will have the option<br>of selecting the function you wish to connect to the relay and whether the function is to<br>be active when the relay is activated or deactivated. Attention! Relay outputs must not be<br>inverted at unloader valves. The controller inverts the function itself.<br>There will be no voltage at the bypass valves when the compressor is not in operation.<br>Power is connected immediately before the compressor is started.<br>If it is a function that requires frequent switching between on/off (e.g. unloader on a scroll<br>compressor, a Stream or a Bitzer CRII), use the solid state relay for this connection. There are<br>solid state relays on output numbers 5 and 6.|On<br>Off|
||**Digital inputs**<br>1:<br>2:<br>3:<br>.<br>8:|**On/off inputs**<br>When a function is defined that uses an input, it will be possible to select this function<br>on one of the available on/off inputs.<br>Select an input and continue on into the setting. In the final setting you will have be able to<br>select which function you wish to connect to the input.|On<br>Off|
||**Analog outputs**<br>1:<br>2:<br>3:<br>4:|**0 – 10 V outputs**<br>When a function has been defined that needs to use a variable voltage outlet, it will be pos-<br>sible to select this function on one of the available AO outputs (AO 1-4 is available).<br>Select one output and continue on in the setting process. In the last setting you will have the<br>option of selecting which function you wish to link to the output.|0 – 10 V<br>0 – 5 V|
||**Analog inputs**<br>1:<br>2:<br>3:<br>4:<br>.<br>.<br>8:|**Analogue inputs**<br>When a function is defined that needs to use a temperature sensor or a pressure transmitter,<br>it will be possible to select this function on one of the available AI inputs.<br>Select an input and continue on into the setting. In the final setting you will be able to select<br>which function you wish to connect to the input.<br>Saux is a sensor for a general thermostat.<br>(A type AKS 2050 pressure transmitter, for high pressure, emits a signal as an AKS 32R.)|Pressure signal:<br>AKS 33<br>AKS 32R<br>AKS 32<br>2 – 10 V<br>0 – 20 mA<br>0 – 10 V<br>0 – 5 V<br>Temperature signal:<br>NTC-86K<br>Pt 1000 ohm<br>None|

18 | BC212486423949en-000501

|**I/O Status**|||
|---|---|---|
|**Digital outputs**<br>1:<br>.<br>8:|**Status of on/off outputs**<br>Here you can see if the function is on or off.||
|**Digital inputs**<br>1:<br>.|**Status of on/off inputs**<br>Here you can see the status of the function/alarm.||
|8:|||
|**Analogue outputs**<br>1:<br>2:<br>3:<br>4:|**Status of analogue outputs**<br>Here you can see the size of the output signals as a % of max. signal.||
|**Analog inputs**<br>1:<br>.<br>8:|**Status of analogue inputs**<br>Here you can see pressure and temperature values received by the controller.<br>The values include calibration||
|**I/O Summary**<br>DO: Max 8, Used:__<br>DI: Max 8, Used:__<br>AO: Max 4, Used:__<br>AI: Max 8,Used:__<br>**I/O Manual control**|**Inputs and outputs used**<br>Here you can see how many of the different inputs and outputs are available.<br>You can also compare this amount with how many have been configured.<br>If too many have been defined, an exclamation mark (!) will appear.||
|**Digital outputs**|**Manual control of a relay output**<br>Under normal regulation, the function of the relay will be in “Auto”.<br>In the event of an override, the function will be switched to either “On” or “Off”.<br>Remember to switch to “Auto” when the override is to be completed.|Auto / On / Off|
|**Analog outputs**|**Manual control of analogue output**<br>During normal regulation, the function of the output will be “Auto”.<br>In the event of an override, the function must first be changed to “Manual”,<br>after which the output signal can be changed from 0-100%.<br>Remember to switch to “Auto” when the override is to be completed.|Auto / Man<br>0-100%|
|**Alarm priorities**|||
|**General**<br>Standby mode:<br>Sensor error:<br>Refrigerant:<br>Output in MANUAL:<br>**Suction group A**<br>Low pressure:<br>High pressure:<br>Compressor safety:|**Alarm priorities**<br>The controller will issue an alarm notification if a specific incident occurs.<br>Each incident is set to indicate the importance of each alarm, but it is possible to modify the<br>importance of each. Choose from between the following priority levels:<br>**Critical:**Important alarms that require a high level of attention.<br>**Severe:**Alarms of intermediate importance<br>**Normal:**No important alarms<br>**Disable:**Alarms set to this priority level will be cancelled.<br>Factory setting for the alarm can be seen on page 21.|Critical<br>Servere<br>Normal<br>Disable|
|**Suction group B**<br>Low pressure:<br>High pressure:<br>Compressor safety:|||
|**Condenser**<br>High pressure:<br>Fan safety:|||

*[Figurtekst: Quick setup · Quick configurations This setting will reserve inputs and outputs for the following compressors and fans: · The various connections are shown on the next page. · App. no. Display Suction group A Suction group  Condenser · B · Speed Digital 1-step 1-step Step Speed · (Scroll / steam) · 17 3CDA + 2CB + FS 1 2 2 x · 16 2CDA + 2CB + 3F 1 1 2 3 · 15 3CSA + 2CB + FS 1 2 2 x · 14 2CSA + 2CB + 3F 1 1 2 3 · 13 4CA + 3CB + FS 4 3 x · 12 3CA + 2CB + FS 3 2 x · 11 2CA + 2CB + 3F 2 2 3 · 10 4CDA + FS 1 3 x · 9 3CDA + FS 1 2 x · 8 3CDA + 3F 1 2 3 · 7 2CDA + 2F 1 1 2 · 6 4CSA + FS 1 3 x · 5 4CA + FS 4 x · 4 4CA + 4F 4 4 · 3 3CSA + FS 1 2 x · 2 3CA + FS  3 x · 1 3CA + 3 F 3 3 · 0 None After makin g  a selection ,  the settin g  will return to “None” · After making a selection you must: · 1. Set the type of refrigerant · 2. Check the types of pressure transmitters · 3. Check the min. and max. settings on the pressure transmitters · Factory setting: · Po A/B = AKS 32R, min=-1.0 bar, max.=12 bar · Pc = AKS 32R, min. = -1.0 bar, max. = 34 bar · SdA = NTC 86K · Setup Wizard This wizard will lead you through the necessary settings, i.e. a total of approximately · 20 to 35 display screens, depending on what is selected along the way. · The selection will also result in a connection to a given input and output. You yourself · will see this connection in the IO confi g uration menu. If a pp licable ,  see  p a g e 20.]*

20 | BC212486423949en-000501

||**DI6**<br>**DI7**<br>**DI8**|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|C2B<br>C3B<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.|Main<br>Sw.<br>Fan<br>safe.||
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|gital|**DI5**|C2B||C2B||C1B|C2B|||||||||||||
|Di|**DI4**|C1B|C2B|C1B|C2B|C4A|C1B|CB2|C4||||C4|C4|C4|||||
||**DI2**<br>**DI3**|C2A<br>C3A|C2A<br>C1B|C2A<br>C3A|C2A<br>C1B|C2A<br>C3A|C2A<br>C3A|C2A<br>C1B|C2<br>C3|C2<br>C3|C2<br>C3|C2|C2<br>C3|C2<br>C3|C2<br>C3|C2<br>C3|C2<br>C3|C2<br>C3||
|**Input**|**AI8**<br>**DI1**|C1A|C1A|C1A|C1A|C1A|C1A|C1A|C1|C1|C1|C1|C1|C1|C1|C1|C1|C1||
||**AI6**<br>**AI7**|||||||||||||||||||
|nalog|**AI5**|SdA<br>Digi|SdA<br>Digi||||||SdA<br>Digi|SdA<br>Digi|SdA<br>Digi|SdA<br>Digi||||||||
|A|**AI4**|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|Sc3|olled|
||**AI3**|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|Pc|contr|
||**AI2**|PoB|PoB|PoB|PoB|PoB|PoB|PoB|||||||||||speed-|
||**AI1**|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|PoA|n, are|
||**AO4**|Fan<br>Speed||Fan<br>Speed||Fan<br>Speed|Fan<br>Speed||Fan<br>Speed|Fan<br>Speed|||Fan<br>Speed|Fan<br>Speed||Fan<br>Speed|Fan<br>Speed||one fa|
|og|**AO3**|||C1A<br>Speed|C1A<br>Speed||||||||C1<br>Speed|||C1<br>Speed|||up B +|
|Anal|**AO2**|||<br>|<br>||||||||<br>|||<br>|||tion gro|
||**AO1**||||||||||||||||||rs, suc|
||**DO8**|Alarm|Fan3|Alarm|Alarm|Alarm|Alarm|Alarm|Alarm|Alarm|Alarm|Alarm|Alarm|Alarm|Fan4|Alarm|Alarm|Alarm|mpresso|
|**utput**|**DO7**|Fan<br>VSD|Fan2|Fan<br>VSD|Fan3|C3B|Fan<br>VSD|Fan3|Fan<br>VSD|Fan<br>VSD|Fan3||Fan<br>VSD|Fan<br>VSD|Fan3|Fan<br>VSD|Fan<br>VSD||+ 2 co|
|**O**|**DO6**|C2B|Fan1||Fan2|C2B||Fan2|||Fan2||||Fan2|||Fan3|oup A|
|/Off|f<br>**DO5**|C1A<br>PWM|C1A<br>PWM|C2B|Fan1|C1B|C2B|Fan1|C1<br>PWM|C1<br>PWM|C1<br>PWM|C1<br>PWM|||Fan1|||Fan2|ion gr|
|Onf|f<br>**DO4**|C1B|C2B|C1B|C2B|C4A|C1B|C2B|C4||Fan1|Fan2|C4|C4|C4|||Fan1|al, suct|
||**DO3**|C3A|C1B|C3A|C1B|C3A|C3A|C1B|C3|C3|C3|Fan1|C3|C3|C3|C3|C3|C3|s digit|
||**DO2**|C2A|C2A|C2A|C2A|C2A|C2A|C2A|C2|C2|C2|C2|C2|C2|C2|C2|C2|C2|s, one i|
||**DO1**|C1A|C1A|C1A|C1A|C1A|C1A|C1A|C1|C1|C1|C1|C1|C1|C1|C1|C1|C1|**w:**<br>ressor|
|**Display**||3CDA + 2CB + FS|2CDA + 2CB + 3F|3CSA + 2CB + FS|2CSA + 2CB + 3F|4CA + 3CB + FS|3CA + 2CB + FS|2CA + 2CB + 3F|4CDA + FS|3CDA + FS|3CDA + 3F|2CDA + 2F|4CSA + FS|4CA + FS|4CA + 4F|3CSA + FS|3CA + FS|3CA + 3 F<br>None|**le of display vie**<br>**2CB + FS =**3 comp|
|**pp. no.**||7|6|5|4|3|2|1|0||||||||||**amp**<br>**DA +**|
|**A**||1|1|1|1|1|1|1|1|9|8|7|6|5|4|3|2|1<br>0|**Ex**<br>**3C**|

###### **Connections when using Setup Wizard**

If you have used the Setup Wizard for the configuration, the controller will automatically assign the selected functions to inputs and outputs in accordance with the following prioritised order:

Digital outputs (DO1-DO8):

- Digital inputs (DI1-DI8):

   - Analogue outputs (AO1-AO4)

- Pulse output for control of the capacity valves for digital scroll, stream or Bitzer CRII will be located on solid state outputs DO5 and DO6

- Compressor safety inputs • Compressor speed control for suction groups A and B, for suction groups A and B, respectively respectively

- Fan safety input

      - Condenser speed control

   - External main switch (start/stop)

- Compressor start and unloaders • HP safety switch for suction groups A and B, • LP safety switch for suction

- respectively groups A and B, respectively

- Fans

   - Night status

- Injection ON

   - Heat recovery

- Alarm

- Load sheeding

- General alarm inputs DI1-DI3

Analogue inputs (AI1-AI8)

- PoA and PoB suction pressure is located on AI1 and AI2, respectively

- Pc condensation pressure is located on AI3

- Sc3 outside temperature is located on AI4

- S4A and S4B media temperature

- S7 media temperature, condenser

- Sd comp. 1 discharge gas temperature for digital scroll/ stream compressor for suction groups A and B, respectively

- Ss suction gas temperature for section groups A and B, respectively

The assignment of functions on the respective inputs and outputs can be regulated in “IO configuration”. Here is an example of 3 compressors and 3 fans:

- Sd discharge gas temperature for suction groups A and B, respectively

- Saux for general thermostat

In this image you can see how many outputs and inputs your settings have provided.

22 | BC212486423949en-000501

#### **9. Alarm list**

|**Alarm text**|**Reason**|**Priority**<br>**setting**|**Default**<br>**value**|
|---|---|---|---|
|General alarms||||
|Standbymode (Main sw. OFF)|Alarm when control is stopped byinternal or external Main Switch (DI input "Main Switch")|Standbymode|Normal|
|PoA sensor error|Pressure transmitter signal from PoA defective|||
|PoB sensor error|Pressure transmitter signal from PoB defective|||
|S4A sensor error|Temperature signal from S4A media temp. sensor defective<br>|||
|S4B sensor error|Temperature signal from S4B media temp. sensor defective|||
|SsA sensor error|Temperature signal from SsA suctiongas temp. defective|||
|SsB sensor error|Temperature signal from SsB suctiongas temp. defective|||
|SdA sensor error|Temperature signal from SdA dischargegas temp. Sd defective|||
|SdB sensor error|Temperature signal from SdB dischargegas temp. Sd defective|Sensor error|Normal|
|Pc sensor error|Pressure transmitter signal from Pc defective|||
|S7 sensor error|Temperature signal from S7 media sensor on condenser defective|||
|Sc3 sensor error|Temperature signal from Sc3 air on condenser defective|||
|Sd Comp. 1A sensor error|Temperature signal from "Sd comp. 1A" discharge gas temp. on digital scroll/Stream compressor is<br>defective|||
|Sd Comp. 1B sensor error|Temperature signal from "Sd comp. 1B" discharge gas temp. on digital scroll/Stream compressor is<br>defective|||
|Saux - sensor error|Temperature signal from Saux thermostat sensor is defective|||
|Refrigerant not selected|Alarm if no refrigerant has been selected|Refrigerant not set|Normal|
|Output in manual mode|An output is set in manual mode|Output in MAN mode|Normal|
|IO configuration error|Not all inputs and output functions have been assigned to hardware Inputs or outputs*|(can not be set)|Normal|
|GA1 - "Alarm text"|Alarm ongeneral alarm input DI 1 (DI input "Gen. Alarm 1 - alarm text depend upon configured text)|General alarm 1|Normal|
|GA2 - "Alarm text"|Alarm ongeneral alarm input DI 2 (DI input "Gen. Alarm 2 - alarm text depend upon configured text)|General alarm 2|Normal|
|GA3 - "Alarm text"|Alarm ongeneral alarm input DI 3 (DI input "Gen. Alarm 3 - alarm text depend upon configured text)|General alarm 3|Normal|
|Suction A alarms||||
|PoA Low suctionpressure|Minimum safetylimit for suctionpressure PoA has been violated|Low ressure PoA|Normal|
|LP A  safetyswitch cut out|Low safetylimit for external lowpressure switch has been violated (DI input "LP switch A")|p||
|PoA High suctionpressure|High alarm limit for PoA has been exceeded|Highpressure PoA|Critical|
|SsA High superheat|Superheat in suction line A too high (measured byPoA and SsA)|Superheat A|Normal|
|SsA Low superheat|Superheat in suction line A too low (measured byPoA and SsA)|||
|SdA High discharge temp.|Safety prevention limit for SdA discharge temperature has been exceeded (10K below safetylimit)|High disch. temp.SdA|Critical|
|Comp. 1A High disch. temp|Safetylimit for dischargegas temperature of digital scroll/Stream/CRII compressor has been exceeded|||
|Compressor 1-8A safety cut|Compressor no. 1-8 A has been cut out on general safety input (DI input "Comp.1-8 A safety")|Compressor safety A|Normal|
|out||||
|Suction B alarms||||
|PoB Low suctionpressure|Minimum safetylimit for suctionpressure PoB has been violated|Low pressure PoB|Normal|
|LP B  safetyswitch cut out|Low safetylimit for external lowpressure switch has been violated (DI input "LP switch B")|||
|PoB High suctionpressure|High alarm limit for PoB has been exceeded|Highpressure PoB|Critical|
|SsB High superheat|Superheat in suction line B too high (measured byPoB and SsB)|Sht B|Nl|
|SsB Low superheat|Superheat in suction line B too low (measured byPoB and SsB)|uperea|orma|
|SdB High discharge temp.|Safety prevention limit for SdB discharge temperature has been exceeded (10K below safetylimit)|High disch. temp.SdB|Critical|
|Comp. 1B High disch. temp|Safetylimit for discharge temperature of digital scroll/Stream compressor has been exceeded|||
|Compressor 1-4B safety cut|Compressor no. 1-4 B has been cut out on general safety (DI input "Comp.1-4 B safety")|Compressor safety B|Normal|
|out||||
|Condenser alarms||||
|Pc High condensing pressure|Highprevention safetylimit for condensing pressure Pc has been violated (3K below safetylimit)|Hih  P|Citil|
|HP safetyswitch cutout|High safetylimit for external highpressure switch has been violated (DI input "HP switch")|g pressure c|rca|
|Common fan safetycut out|A Fan is reported defective via common safetyinput (DI input "Fan safety")|F f|Nl|
|Fan 1 safetycut out|Fan no. 1-8 is reported defective via individual safetyinput (DI input "Fan 1-8 safety")|an saety|orma|

* The alarm "IO configuration error" is activated if not all IO functions have been assigned to a hardware Input or output. Often the reason is that too many functions have been selected via the configuration of the controller.

Go to the menu point "Main menu => IO status => IO summary".

In this screen you can see if you have configured too many functions of a certain type - indicated by an exclamation mark " ! " Please refer to the screen example, were too many DO functions have been configured. Solve the problem by adapting the DO functions to the max. No of DO outputs.

###### Sensor alarms

Sensor alarms shut off automatically when the sensor has been O.K. for 10 minutes.

If you have corrected the sensor error and want to perform a manual, forced removal of the alarm, go to the “Alarm detail display” Press and hold the “X” key for 2 seconds here.

###### ERR31

Alarm on the external display - MMIGRS2

If the communication to the display is not carried out correctly, it will send an “ERR31” error notification.

This may be caused by the displayed terminations not being installed, or that there have been interruptions in data communication during the time when the display retrieves the basic information from the controller.

Once the terminations have been inspected, you should then check the software version of the external display. This is done by holding down the Enter key and the X key for 5 seconds, until the Bios menu appears. Next, press the X key and read off the software version in the bottom right corner. The software version must be 1.13 or newer.

Once the display’s software version has been checked, check the display’s settings as follows:

In case RJ11 cable is used to connect the display, it is mandatory to short circuit the connectors as shown in this figure.

1. Hold the Enter key and the X key down for 5 seconds, until the Bios menu appears.

2. Select the “MCX selection” menu

   -  Select the “Clear UI” line and press Enter

   -  Select the “Autodetect” line and press Enter

3. Select the “COM selection” menu

   -  Select the “CAN” line and press Enter

4. Select the “Start up mode” menu

   -  Select the “Remote application” line and press Enter

5. Select the “CAN” menu

   -  Select the “Baudrate” line and then select the “Autobaud” setting and press Enter

   -  Select the “Node ID” line and set the value to 126 and press Enter

6. Press the X key to return to the Bios menu

7. Select the “Application” menu and press Enter. “Data” will be shown.

The display will once again retrieve data from the controller. This process will take upto 5 min.

24 | BC212486423949en-000501

#### **10. Connections**

###### **Connection, lower level**

*[Figurtekst: Modbus · B– · Power A+ · ÷ · L N L H R – + · DO 1 2 3 4 5 6 7 8 · DO DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 Σ 1-8 · I Max. 10 A 10 A 6 A 6 A 0.5 A 0.5 A 6 A 6 A 32 A · (3.5) (3.5) (4) (4) min. 50 mA min. 50 mA (4) (4) · Ioff < 1,5 mA Ioff < 1,5 mA · U All 24 V or all 230 V AC]*

**Supply Voltage** .

The supply voltage is either 24 V **or** 110 – 230 V. See the label on the reverse side of the controller.

###### **÷ = Plugs normally not used**

However, if connecting to an external display, a jumper must be inserted between the connections "H" and "R".

###### **Connection, upper level**

*[Figurtekst: External · 24 V AKS 32R 1=Black = + · 2=Blue = – · AC/DC 0 – 10 V 1 2 3 3=Brown = s · 0 – 10 V + – s SC3 · AI 1 = PoA · AI 2 = PoB · – 1 2 N L 3 4 + + + + – – – 1 2 3 4 AI 3 = Pc · AI 4 = Sc3 · COM AO 5 V     12 V     COM           AI · DI DI AI · 1 2 3 4 – 5 6 7 8 – – 5 6 7 8 · Warning · The supply voltage of AI may not share · the signal with other controllers. · Separate  supply! · COM COM COM]*

###### **Electric noise**

Signal cables for sensors, DI inputs, data communication and display must be kept separate from high voltage (230 V) electric cables:

- Use separate cable trays

- Keep a distance between high voltage and signal cables of at least 10 cm

- Cables longer than 3 m at the DI input should be avoided

###### **AO - Analogue output, 4 pcs. AO1 - AO4**

Must be used when using a frequency converter or EC motors. Connect 24 V on N and L only on AO3 and AO4 outputs (external supply). Avoid earth fault current. Use double-insulated transformer. The secondary side must not be earthed. Obtain 0 – 10 V from terminals N and AOx PAY ATTENTION TO THE POLARITY of N.

###### **Modbus**

It i s important t hat the installation of the data communication cable be done correctly. Cf. separate literature No. RC8AC. Remember termination at the bus termination.

###### **DO - Digital outputs, 8 pcs. DO1 - DO8**

DO5 and DO6 are solid state relays. The relays are de-rated to the specified values. If an alarm relay is defined, it will be driven under normal operation and it will drop in the event of alarms and insufficient power to the controller.

*[Figurtekst: AKS 32R 10 – 90% ratiometric · AKS 32 1 – 5 V · AKS 33 0 – 20 mA · 4 – 20 mA]*

###### **AI - Analogue inputs, 4 pcs. AI1 - AI4**

Pressure transmitters

- Ratiometric: 10 – 90% of supply, AKS 32R

- Signal: 1 – 5 V, AKS 32

- Power: 0 – 20 mA / 4 – 20 mA, AKS 33 (supply = 12 V) Temperature sensor

- Pt 1000 ohm, AKS 11 or AKS 21

- NTC 86K ohm @ 25 °C, from digital scroll

- Factory settings

- AI1=PoA, AI2=PoB, AI3=Pc, AI4=Outdoor temperature SC3.

###### **DI - Digital switch inputs, 8 pcs. DI1 - DI8**

The connection may be a shut-down or interruption function. Select what is to be activated during configuration.

###### **÷ = Plugs normally not used**

###### **AI - Analogue inputs, 4 pcs. AI5 - AI8**

Pressure transmitters

- Ratiometric: 10 – 90% of supply, AKS 32R

- Signal: 1 – 5 V, AKS 32

- Temperature sensor

- Pt 1000 ohm, AKS 11 or AKS 21.

- NTC 86K ohm @ 25 °C, from digital scroll

###### **The capacity from the digital scroll compressor**

*[Figurtekst: Only DO5 or DO6]*

The capacity is divided into period times as "PWM period time". 100% capacity is delivered when cooling takes place for the whole period. An off time is required by the bypass valve within the period and an on time is also permitted. There is "no cooling" when the valve is on.

The controller itself calculates the capacity needed and will then vary it according to the cut-in time of the capacity control valve. A limit is introduced if low capacity is needed so that the cooling does not go below 10%. This is because the compressor can cool itself. This value can be increased if necessary.

*[Figurtekst: Refrigeration · No refrigeration · Period time · Min. Capacity]*

###### **Copeland Stream compressor**

The pulse signal can also be used to control one stream compressor with one unloader valve *(4 cylinders version). The compressor capacity is distributed by up to 50% for one relay and the remaining 50-100% for the unloader. The unloader is connected to DO5 or DO6.

###### **Bitzer CRII**

The pulse signal can also be used to control one of the CRII with 2 unloaders (4 cylinders version). Compressor capacity can be controlled from 10 – 100% depending on the pulsation of the unloaders. The unloaders are connected to DO5 and DO6.

*[Figurtekst: Unloader 1 · Unloader 2 · Unloader 2 follows unloader 1 · but is offset  a ½ period.]*

###### **Sd monitoring**

When regulating with Sd monitoring, one of the three compressor types will increase capacity if the temperature nears the Sd limit. This will result in better cooling of the unloaded compressor.

###### **Injection off**

The electronic expansion valves in the cooling appliances must be closed when all the compressors are prevented from starting. As a result, the evaporators will not be filled with fluid that can be led to a compressor when the regulation process restarts. One of the compressor control relays can be used for this function, or the function can be prompted via data communication.

26 | BC212486423949en-000501

#### **11. Data**

#### **12. External display**

|Supply voltage|24 V AC +/-15% 50/60 Hz, 17 VA<br>24 V DC (20 – 60 V), 17 VA<br>230 AC(85 – 265 V)50/60 Hz,20 VA|An external display is only for  front assembly (IP 20)<br>Connection only via cable with plug. See ordering.|
|---|---|---|
|8 analog Input|Pressure meauring:<br>Ratiometric pressure transmitter type AKS 32R<br>1 – 5 volt  pressure transmitter type AKS 32<br>0 – 20(4 – 20)mApressure transmitter type AKS 33<br>Temperature measurement<br>Pt 1000 ohm/0°C<br>NTC - 86K from digital scroll / stream|**Important!!**<br>**Termination**<br>**Connect H-R**<br>**Termination**<br>**Connect H-R**|
|8 digital input|From contact function<br>E.g. to:<br>Start/stop of regulation<br>Monitoring of safety circuits<br>General alarm function|H<br>R|
||4 pcs. SPDT (8A)<br>AC-1: 6 A (ohmic)<br>AC-15: 4 A(inductive)||
|Relay output to|2 pcs. SPST (16A)<br>AC-1: 10 A (ohmic)<br>AC-15: 3.5(inductive)||
|capacity control|2 pcs. Solid State.<br>PWM for scroll -<br>unload<br>Imax. = 0.5 A<br>Imin. = 50 mA.<br>Leak<1.5 mA<br>Not short-circuitprotected|Danfoss<br>80G51|
|4 Voltage output|0 – 10 V DC, Ri = 1kohm<br>Separate 24 V supplyrequired||
|Displayoutput|For  type MMIGRS2||
|Data<br>communication|Modbus<br>for AK-SM 800||
||-20 – +60 °C, During operations<br>-40 – +70 °C, Duringtransport||
|Environments|20 – 80% Rh, not condensed||
||No shock influence / vibrations||
|Enclosure|IP 20||
|Weight|0,4 kg||
|Mounting|DIN-rail||
|Connection<br>terminals|max. 2.5 mm<sup>2</sup>multi core||
||EU Low Voltage Directive and EMC demands re CE-<br>marking complied with||
|Approvals|LVD tested acc. EN 60730-1 and EN 60730-2-9<br>EMC-tested acc. EN61000-6-2 and 3<br>UL approval||

###### **Pressure transmitter / temperature sensor**

Kindly refer to catalogue RK0YG...

###### **Capacitive load**

The relays are not suitable for the direct coupling of the capacitive loads such as LED and on / off control of EC motors. All loads with a switch mode power supply has to be connected with a suitable contactor or the like.

#### **13. Ordering**

|**Type**|**Function**|**Operation**|**Supply voltage**|**Code no.**|
|---|---|---|---|---|
||||230 V|**080G0281**|
|AK-PC 551|Caacit controller|With buttons and display|24 V|**080G0283**|
||py||230 V|**080G0282**|
|||With external display and<br>1.5 m wire for display unit|24 V|**080G0288**|
|MMIGRS2|Display unit|With buttons and display|-|**080G0294**|
||Wire for displayunit|L = 1.5 m,1pcs.||**080G0075**|
||Wire for displayunit|L = 3 m, 1pcs.||**080G0076**|

#### **14. Mounting /Dimensions**

For DIN rail mounting only (IP 20)

###### **Installation considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown.

###### **List of literature**

Installation guide for extended operation RC8AC Here you can see how a data communication connection to ADAP-KOOL® Refrigeration control systems can be established.

Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation, for example, could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss will not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer's responsibility to check the installation thoroughly, and to fit the necessary safety devices.

Special reference is made to the necessity of signals to the controller when the compressor is stopped and to the need of liquid receivers before the compressors. Your local Danfoss agent will be pleased to assist with further advice, etc.
