# Dixell XR20CX – Digital controller with off cycle defrost – XR20CX

Kilde: `XR20CX-GB.pdf` i denne mappe. Konverteret direkte fra PDF'en. Tabeller (parametre, alarmer, standardværdier) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra tegninger står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilket afsnit svaret kommer fra.
- Alarm- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer (Dixell, Danfoss, Carel). Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualen, så sig det i stedet for at gætte.

---

#### **Digital controller with off cycle defrost**

### **XR20CX**

|**CO**|**NTENTS**|
|---|---|
|1.|GENERAL WARNING ___________________________________________________ 1|
|2.|GENERAL DESCRIPTION _______________________________________________ 1|
|3.|CONTROLLING LOADS _________________________________________________ 1|
|4.|FRONT PANEL COMMANDS _____________________________________________ 1|
|5.|MAX & MIN TEMPERATURE MEMORIZATION _______________________________ 1|
|6.|MAIN FUNCTIONS _____________________________________________________ 1|
|7.|PARAMETERS ________________________________________________________ 2|
|8.|DIGITAL INPUT (ENABLED WITH P3P = N) _________________________________ 3|
|9.|TTL SERIAL LINE – FOR MONITORING SYSTEMS ___________________________ 3|
|10.|X-REP OUTPUT – OPTIONAL ____________________________________________ 3|
|11.|INSTALLATION AND MOUNTING _________________________________________ 3|
|12.|ELECTRICAL CONNECTIONS ____________________________________________ 3|
|13.|HOW TO USE THE HOT KEY _____________________________________________ 3|
|14.|ALARM SIGNALS ______________________________________________________ 3|
|15.|TECHNICAL DATA _____________________________________________________ 4|
|16.|CONNECTIONS _______________________________________________________ 4|
|17.|DEFAULT SETTING VALUES _____________________________________________ 4|
|**1. **|**GENERAL WARNING**|

- **1.1 PLEASE READ BEFORE USING THIS MANUAL**  This manual is part of the product and should be kept near the instrument for easy and quick reference.

- The instrument shall not be used for purposes different from those described hereunder. It cannot be used as a safety device.

- Check the application limits before proceeding.  Dixell Srl reserves the right to change the composition of its products, even without notice, ensuring the same and unchanged functionality.

##### **1.2**<sup>**SAFETY PRECAUTIONS**</sup>

- Check the supply voltage is correct before connecting the instrument.

- Do not expose to water or moisture: use the controller only within the operating limits avoiding sudden temperature changes with high atmospheric humidity to prevent formation of condensation

- Warning: disconnect all electrical connections before any kind of maintenance.

- Fit the probe where it is not accessible by the End User. The instrument must not be opened.

- In case of failure or faulty operation send the instrument back to the distributor or to “Dixell S.r.l.” (see address) with a detailed description of the fault.

- Consider the maximum current which can be applied to each relay (see Technical Data).

- Ensure that the wires for probes, loads and the power supply are separated and far enough from each other, without crossing or intertwining.

- In case of applications in industrial environments, the use of mains filters (our mod. FT1) in parallel with inductive loads could be useful.

##### **2. GENERAL DESCRIPTION**

Model **XR20C** , format 32 x 74 mm,  is a digital thermostat with off cycle defrost designed for refrigeration applications at normal temperature. It provides a relay output to drive the compressor.  It is also provided with 2 NTC or PTC probe inputs, the first one for temperature control, the second one, optional, to connect to the HOT KEY terminals to signal the condenser temperature alarm or to display a temperature. The digital input can operate as third temperature probe.

The HOT KEY output allows to connect the unit, by means of the external module XJ485-CX, to a network line **ModBUS-RTU** compatible such as the Dixell monitoring units  of X-WEB family. It allows to program the controller by means the HOT KEY programming  keyboard. The instrument is fully configurable through special parameters that can be easily programmed through the keyboard.

##### **3. CONTROLLING LOADS**

##### **3.1 COMPRESSOR**

|The<br>regulation<br>is<br>performed|**Temper.**|
|---|---|
|according<br>to<br>the<br>temperature<br>measured by the thermostat probe|**SET**|
|with a positive differential from the||
|set<br>point:<br>if<br>the<br>temperature|**Time**|
|increases and reaches set point plus|**Compr.**|
|differential the compressor is started<br>and then turned off when the|**ON**|
|temperature reaches the set point<br>value again.||
|In case of fault in the thermostat probe th<br>parameters “**COn**” and “**COF**”.|e start and stop of the compressor are timed through|

##### **3.2 DEFROST**

Defrost is performed through a simple stop of the compressor. Parameter “ **IdF** ” controls the interval between defrost cycles, while its length is controlled by parameter “ **MdF** ”.

XR20C

##### **4. FRONT PANEL COMMANDS**

   - : To display target set point; in programming mode it  selects a parameter  or confirm

   - an operation.

- **(DEF)** To start a manual defrost ( **UP)** : To see the max. stored temperature; in programming mode it browses the parameter codes or increases the displayed value. ( **DOWN** ) To see the min stored temperature; in programming mode it browses the parameter codes or decreases the displayed value. To switch the instrument off, if onF = oFF. Not enabled

- **KEY COMBINATIONS: +** To lock & unlock the keyboard **. +** To enter in programming mode. **+** To return to the room temperature display.

##### **4.1 USE OF LEDS**

Each LED function is described in the following table.

|**LED**|**MODE**|**FUNCTION**|
|---|---|---|
||ON|Compressor enabled|
||Flashing|Anti-short cycle delay enabled|
||ON|Defrost enabled|
||ON|An alarm is occurring|
||ON|Continuous cycle is running|
||ON|Energysavingenabled|
|**°C/°F**|ON|Measurement unit|
|**°C/°F**|Flashing|Programming phase|

##### **5. MAX & MIN TEMPERATURE MEMORIZATION**

- **5.1 HOW TO SEE THE MIN TEMPERATURE** 1. Press and release the n key. 2. The “Lo” message will be displayed followed by the minimum temperature recorded. 3. By pressing the n key again or by waiting 5s the normal display will be restored. **5.2 HOW TO SEE THE MAX TEMPERATURE** 1. Press and release the o key. 2. The “Hi” message will be displayed followed by the maximum  temperature recorded. 3. By pressing the o key again or by waiting 5s the normal display will be restored.

- **5.3 HOW TO RESET THE MAX AND MIN TEMPERATURE RECORDED** 1. Hold press the SET key for more than 3s, while the max. or min temperature is displayed. (rSt message will be displayed)

- 2. To confirm the operation the “rSt” message starts blinking and the normal temperature will be displayed.

##### **6. MAIN FUNCTIONS**

##### **6.1 HOW TO SEE THE SETPOINT**

1. Push and immediately release the **SET** key: the display will show the Set point value;

2. Push and immediately release the **SET** key or wait for 5 seconds to

display the probe value again. **6.2 HOW TO CHANGE THE SETPOINT** 1. Push the **SET** key for more than 2 seconds to change the Set point value; 2. The value of the set point will be displayed and the “ **°C” or “°F”** LED starts blinking; 3. To change the Set value push the o or n arrows within 10s. 4. To memorise the new set point value push the **SET** key again or wait 10s. **6.3 HOW TO START A MANUAL DEFROST** Push the **DEF** key for more than 2 seconds and a manual defrost will start.

##### **6.4 HOW TO CHANGE A PARAMETER VALUE**

To change the parameter’s value operate as follows:

1. Enter the Programming mode by pressing the **Set** + n keys for 3s (the “ **°C” or “°F”** LED starts blinking).

2. Select the required parameter. Press the “ **SET** ” key to display its value

3. Use “ **UP** ” or “ **DOWN** ” to change its value.

4. Press “ **SET** ” to store the new value and move to the following parameter.

**To exit** : Press **SET + UP** or wait 15s without pressing a key. **NOTE** : the set value is stored even when the procedure is exited by waiting the time-out to expire.

##### **6.5 THE HIDDEN MENU**

The hidden menu Includes all the parameters of the instrument.

###### **6.5.1 HOW TO ENTER THE HIDDEN MENU**

1. Enter the Programming mode by pressing the **Set** + n keys for 3s (the “ **°C” or “°F”** LED starts blinking).

2. Released the keys, then push again the Set+ n keys for more than 7s. The Pr2 label will be displayed immediately followed from the HY parameter.

**NOW YOU ARE IN THE HIDDEN MENU.**

3. Select the required parameter.

4. Press the “ **SET** ” key to display its value

5. Use o or n to change its value.

6. Press “ **SET** ” to store the new value and move to the following parameter.

**To exit** : Press **SET +** o or wait 15s without pressing a key.

**NOTE1:** if none parameter is present in Pr1, after 3s the “noP” message is displayed. Keep the keys pushed till the Pr2 message is displayed. **NOTE2** : the set value is stored even when the procedure is exited by waiting the time-out to expire.

###### **6.5.2 HOW TO MOVE A PARAMETER FROM THE HIDDEN MENU TO THE FIRST LEVEL AND VICEVERSA.**

Each parameter present in the HIDDEN MENU can be removed or put into “THE FIRST LEVEL” (user level) by pressing **“SET +** n **”** .

In HIDDEN MENU when a parameter is present in First Level the decimal point is on.

##### **6.6 HOW TO LOCK THE KEYBOARD**

1. Keep pressed for more than 3 s the **UP** + **DOWN** keys.

2. The “POF” message will be displayed and the keyboard will be locked. At this point it will be possible only to see the set point or the MAX o Min temperature stored

3. If a key is pressed more than 3s the “POF” message will be displayed.

##### **6.7 TO UNLOCK THE KEYBOARD**

Keep pressed together for more than 3s the o and n keys, till the **“Pon”** message will be displayed.

##### **6.8 THE CONTINUOUS CYCLE**

When defrost is not in progress, it can be activated by holding the “ o ” key pressed for about 3 seconds. The compressor operates to maintain the “ **ccS** ” set point for the time set through the “ **CCt** ” parameter. The cycle can be terminated before the end of the set time using the same activation key “ o ” for 3 seconds.

##### **6.9 THE ON/OFF FUNCTION**

With “ **onF = oFF** ”, pushing the **ON/OFF** key, the instrument is switched off. The **“OFF”** message is displayed. In this configuration, the regulation is disabled. To switch the instrument on, push again the ON/OFF key.

WARNING: Loads connected to the normally closed contacts of the relays are always supplied and under voltage, even if the instrument is in stand by mode.

##### **7. PARAMETERS**

###### **REGULATION**

**Hy Differential** : (0,1 ÷ 25,5°C / 1÷255 °F) Intervention differential for set point. Compressor Cut IN is Set Point + differential (Hy). Compressor Cut OUT is when the temperature reaches the set point.

**LS  Minimum set point:** (- 50°C÷SET/-58°F÷SET): Sets the minimum value for the set point. **US Maximum set point:** (SET÷110°C/ SET÷230°F). Set the maximum value for set point. **Ot  Thermostat probe calibration** : (-12.0÷12.0°C; -120÷120°F) allows to adjust possible offset of the thermostat probe.

- **P3P Third probe presence (P3): n** = not present:, the terminal operates as digital input.; **y=** present:, the terminal operates as third probe.

- **O3 Third probe calibration  (P3):** (-12.0÷12.0°C; -120÷120°F). allows to adjust possible offset of the third probe.

- **P4P Fourth probe presence** : (n = Not present; y = present).

- **o4 Fourth probe calibration** : (-12.012.0°C) allows to adjust possible offset of the fourth probe.

- **OdS Outputs activation delay at start up:** (0÷255min) This function is enabled at the initial start up of the instrument and inhibits any output activation for the period of time set in the parameter.

- **AC  Anti-short cycle delay** : (0÷50 min) minimum interval between the compressor stop and the following restart.

**CCt Compressor ON time during continuous  cycle:** (0.0÷24.0h; res. 10min) Allows to set the length of the continuous cycle: compressor stays on without interruption for the CCt time. Can be used, for instance, when the room is filled with new products.

XR20C

**CCS Set point for continuous cycle:** (-50÷150°C) it sets the set point used during the continuous cycle. **COn Compressor ON time with faulty probe:** (0÷255 min) time during which the compressor is active in case of faulty thermostat probe. With COn=0 compressor is always OFF. **COF Compressor OFF time with faulty probe:** (0÷255 min) time during which the compressor is OFF in case of faulty thermostat probe. With COF=0 compressor is always active. **CH Type of action:** CL = cooling; Ht = heating. **DISPLAY CF Temperature measurement unit: °C=** Celsius; **°F** =Fahrenheit. WARNING: When the measurement unit is changed the SET point and the values  of the parameters Hy, LS, US, Ot, ALU and ALL have to be checked and modified if necessary). **rES Resolution (for °C)** : (in = 1°C; dE = 0.1 °C) allows decimal point display. **dLy Display delay:** (0 ÷20.0m; risul. 10s) when the temperature increases, the display is updated of 1 °C/1°F after this time. **DEFROST IdF  Interval between defrost cycles** : (0÷120h) Determines the time interval between the beginning of two defrost cycles. **MdF  (Maximum) length for defrost** : (0÷255min) When **P2P = n** , (not evaporator probe: timed defrost) it sets the defrost duration, when **P2P = y** (defrost end based on temperature) it sets the maximum length for defrost. **dFd  Temperature displayed during defrost** : ( **rt** = real temperature; **it** = temperature at defrost start; **SEt** = set point; **dEF** = “dEF” label) **dAd MAX display delay after defrost** : (0÷255min). Sets the maximum time between the end of defrost and the restarting of the real room temperature display. **ALARMS ALC  Temperature alarms configuration:** (Ab; rE) Ab= absolute temperature: alarm temperature is given by the ALL or ALU values.  rE = temperature alarms are referred to the set point. Temperature alarm is enabled when the temperature exceeds the “SET+ALU” or “SET-ALL” values. **ALU  MAXIMUM temperature alarm** : (SET÷110°C; SET÷230°F) when this temperature is reached  the alarm is enabled, after the “ALd” delay time. **ALL Minimum temperature alarm** : (-50.0 ÷ SET°C; -58÷230°F when this temperature is reached  the alarm is enabled, after the “ALd” delay time. **AFH Differential for temperature alarm recovery:** (0,1÷25,5°C; 1÷45°F) Intervention differential for recovery of temperature alarm. **ALd  Temperature alarm delay** : (0÷255 min) time interval between the detection of an alarm condition and alarm signalling. **dAO Exclusion of temperature alarm at startup** : (from 0.0 min to 23.5h) time interval between the detection of the temperature alarm condition after instrument power on and alarm signalling. **CONDENSER TEMPERATURE ALARM (detected by the fourth probe) AP2 Probe selection for temperature alarm of condenser: nP** = no probe; **P1** =thermostat probe; **P2 =** evaporator probe; **P3** =configurable probe; **P4** = Probe on Hot Key plug. **AL2 Low temperature alarm of condenser** : (-55÷150°C) when this temperature is reached the LA2 alarm is signalled, possibly after the Ad2 delay. **Au2 High temperature alarm of condenser** : (-55÷150°C) when this temperature is reached the HA2 alarm is signalled, possibly after the Ad2 delay. **AH2 Differential for temperature condenser alarm recovery** : (0,1÷25,5°C; 1÷45°F) **Ad2 Condenser temperature alarm delay** : (0÷255 min) time interval between the detection of the condenser alarm condition and alarm signalling. **dA2 Condenser temperature alarm exclusion at start up** : (from 0.0 min to 23.5h, res. 10min) **bLL Compressor off with low temperature alarm of condenser** : **n = no:** compressor keeps on working **; Y = yes,** compressor is switched off till the alarm is present, in any case regulation restarts after AC time at minimum. **AC2 Compressor off with high temperature alarm of condenser** : **n = no:** compressor keeps on working **; Y = yes,** compressor is switched off till the alarm is present, in any case regulation restarts after AC time at minimum. **DIGITAL INPUT i1P Digital input polarity: oP:** the digital input is activated by opening the contact; **CL:** the digital input is activated by closing the contact. **i1F Digital input configuration: EAL** = external alarm: “EA” message is displayed; **bAL** = serious alarm “CA” message is displayed. **PAL** = pressure switch alarm, “CA” message is displayed; **dor** = door switch function; **dEF** = activation of a defrost cycle; **AUS** = not enabled; **Htr** = kind of action inversion (cooling – heating); **FAn = do not set it; ES =** Energy saving. **did** : (0255 min) **with i1F= EAL or i1F = bAL digital input alarm delay:** delay between the detection of the external alarm condition and its signalling. **with i1F= dor: door open signalling delay with i1F = PAL: time for pressure switch function:** time interval to calculate the number of the pressure switch activation. **nPS Pressure switch number:** (0 15) Number of activation of the pressure switch, during the “ **did** ” interval, before signalling the alarm event (I2F= PAL). **If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation. odc Compressor status when open door: no; Fan** = normal; **CPr** ; **F_C** = Compressor OFF. **rrd Outputs restart after doA alarm: no =** outputs not affected by the doA alarm; **yES =** outputs restart with the doA alarm; **HES Temperature increase during the Energy Saving cycle :** (-30,0°C30,0°C/-22÷86°F) it sets the increasing value of the set point during the Energy Saving cycle.

###### **OTHER**

**Adr  Serial address** (1÷244): Identifies the instrument address when connected to a ModBUS compatible monitoring system.

**PbC Type of probe:** it allows to set the kind of probe used by the instrument: **PbC** = PBC probe, **ntc =** NTC probe.

**onF on/off key enabling: nu =** disabled; **oFF =** enabled; **ES = not set it** .

**dP1 Thermostat probe display dP3 Third probe display** - **_optional_** . **dP4 Fourth probe display** .

**rSE Real set point:** (readable only), it shows the set point used during the energy saving cycle or during the continuous cycle. **rEL Software release** for internal use **.**

**Ptb Parameter table code:** readable only **.**

##### **8. DIGITAL INPUT (ENABLED WITH P3P = N)**

The free voltage digital input is programmable in different configurations by the “ **i1F** ” parameter.

**8.1 DOOR SWITCH INPUT  (i1F = dor)** It signals the door status and the corresponding relay output status through the “ **odc** ” parameter: **no, Fan** = normal (any change); **CPr, F_C** = Compressor OFF. Since the door is opened, after the delay time set through parameter “ **did** ”, the door alarm is enabled, the display shows the message “ **dA** ” and **the regulation restarts is rtr = yES.** The alarm stops as soon as the external digital input is disabled again. With the door open, the high and low temperature alarms are disabled.

##### **8.2 GENERIC ALARM (i1F = EAL)**

As soon as the digital input is activated the unit will wait for “ **did** ” time delay before signalling the “ **EAL** ” alarm message. The outputs status don’t change. The alarm stops just after the digital input is de-activated.

##### **8.3 SERIOUS ALARM MODE (i1F = bAL)**

When the digital input is activated, the unit will wait for “ **did** ” delay before signalling the “ **CA** ” alarm message. The relay outputs are switched OFF. The alarm will stop as soon as the digital input is de-activated.

##### **8.4 PRESSURE SWITCH (i1F = PAL)**

If during the interval time set by “ **did** ” parameter, the pressure switch has reached the number of activation of  the “ **nPS** ” parameter, the “ **CA** ” pressure alarm message will be displayed. The compressor and the regulation are stopped. When the digital input is ON the compressor is always OFF.

**If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation.**

##### **8.5 START DEFROST (i1F = dFr)**

It starts a defrost if there are the right conditions. After the defrost is finished, the normal regulation will restart only if the digital input is disabled otherwise the instrument will wait until the “MdF” safety time is expired.

##### **8.6 INVERSION OF  THE KIND OF ACTION: HEATING-COOLING (i1F = Htr)**

This function allows to invert the regulation of the controller: from cooling to heating and viceversa.

##### **8.7 ENERGY SAVING (i1F = ES)**

The Energy Saving function allows to change the set point value as the result of the SET+ HES (parameter) sum. This function is enabled until the digital input is activated.

##### **8.8 DIGITAL INPUTS POLARITY**

The digital input polarity depends on the “ **i1P** ” parameter. **i1P=CL** : the input is activated by closing the contact. **i1P=OP** : the input is activated by opening the contact

##### **9. TTL SERIAL LINE – FOR MONITORING SYSTEMS**

The TTL serial line, available through the HOT KEY connector, allows by means of the external TTL/RS485 converter, **XJ485-CX** , to connect the instrument to a monitoring system **ModBUS-RTU** compatible  such as the  X-WEB500/3000/300.

##### **10. X-REP OUTPUT – OPTIONAL**

As optional, an X-REP can be connected to the instrument, trough the HOY KEY connector. The X-REP output **EXCLUDES** the serial connection.

To connect the X-REP to the instrument the following connectors must be used CAB51F(1m), CAB-52F(2m), CAB55F(5m),

XR20C

##### **11. INSTALLATION AND MOUNTING**

Instrument **XR20CX** shall be mounted on vertical panel, in a 29x71 mm hole, and fixed using the special bracket supplied. The temperature range allowed for correct operation is 060 °C. Avoid places subject to strong vibrations, corrosive gases, excessive dirt or humidity. The same recommendations apply to probes. Let air circulate by the cooling holes.

##### **12. ELECTRICAL CONNECTIONS**

The instrument is provided with screw terminal block to connect cables with a cross section up to 2,5 mm<sup>2</sup> . Before connecting cables make sure the power supply complies with the instrument’s requirements. Separate the probe cables from the power supply cables, from the outputs and the power connections. Do not exceed the maximum current allowed on each relay, in case of heavier loads use a suitable external relay.

##### **12.1 PROBE CONNECTION**

The probes shall be mounted with the bulb upwards to prevent damages due to casual liquid infiltration. It is recommended to place the thermostat probe away from air streams to correctly measure the average room temperature. Place the defrost termination probe among the evaporator fins in the coldest place, where most ice is formed, far from heaters or from the warmest place during defrost, to prevent premature defrost termination.

##### **13. HOW TO USE THE HOT KEY**

##### **13.1 HOW TO PROGRAM A HOT KEY FROM THE INSTRUMENT (UPLOAD)**

1. Program one controller with the front keypad.

2. When the controller is ON, insert the “ **Hot key** ” and push o key; the **"uPL"** message appears followed a by flashing **“End”**

3. Push “ **SET”** key and the **End** will stop flashing.

4. <u>Turn OFF the instrument remove the</u> **“Hot Key”,** then turn it ON again.

**NOTE** : the “ **Err** ” message is displayed for failed programming. In this case push again o key if you want to restart the upload again or remove the “ **Hot key** ” to abort the operation.

##### **13.2 HOW TO PROGRAM AN INSTRUMENT USING A HOT KEY**

##### **<u>(DOWNLOAD)</u>**

1. Turn OFF the instrument.

2. Insert  a **programmed “Hot Key” into the 5 PIN receptacle** and then turn the Controller ON.

3. Automatically the parameter list of the **“Hot Key”** is downloaded into the Controller memory, the “ **doL** ” message is blinking followed a by flashing **“End”.**

4. After 10 seconds the instrument will restart working with the new parameters.

5. Remove the **“Hot Key”.** .

**NOTE** the message “ **Err** ” is displayed for failed programming. In this case turn the unit off and then on if you want to restart the download again or remove the “ **Hot key** ” to abort the operation.

##### **14. ALARM SIGNALS**

|**Message**|<br>**Cause**|**Outputs**|
|---|---|---|
|“P1”|Room probe  failure|Compressor output acc. to par. “Con” and<br>“COF”|
|“P3”|Thirdprobe  failure|Outputs unchanged|
|“P4”|Fourthprobe  failure|Outputs unchanged|
|“HA”|Maximum temperature alarm|Outputs unchanged.|
|“LA”|Minimum temperature alarm|Outputs unchanged.|
|"HA2"|Condenser high temperature|It depends on the “Ac2”parameter|
|"LA2"|Condenser low temperature|It depends on the “bLL”parameter|
|“dA”|Door open|Compressor accordingto rrd|
|“EA”|External alarm|Output unchanged.|
|“CA”|Serious<br>external<br>alarm<br>(i1F=bAL)|<br>All outputs OFF.|
|“CA”|Pressure<br>switch<br>alarm<br>(i1F=PAL)|<br>All outputs OFF|

##### **14.1 ALARM RECOVERY**

Probe alarms **P1** ”, “ **P3** ” and “ **P4** ” start some seconds after the fault in the related probe; they automatically stop some seconds after the probe restarts normal operation. Check connections before replacing the probe.

Temperature alarms “ **HA** ”, “ **LA** ” “ **HA2** ” and “ **LA2** ” automatically stop as soon as the temperature returns to normal values.

Alarms **“EA”** and **“CA”** (with i1F=bAL) recover as soon as the digital input is disabled. Alarm “ **CA”** (with i1F=PAL) recovers only by **switching off and on** the instrument.

##### **14.2 OTHER MESSAGES**

**Pon** Keyboard unlocked. **PoF** Keyboard locked **noP In programming mode** : none parameter is present in Pr1 **On the display** or in dP2, dP3, dP4: the selected probe is nor enabled **noA None alarm is recorded.**

##### **15. TECHNICAL DATA**

**Housing:** self extinguishing ABS. **Case: XR20CX** frontal 32x74 mm; depth 60mm; **Mounting: XR20CX** panel mounting in a 71x29mm panel cut-out **Protection:** IP20; **Frontal protection: XR20CX** IP65 **Connections:** Screw terminal block  2,5 mm<sup>2</sup> wiring. **Power supply:** according to the model: 12Vac/dc, ±10%; 24Vac/dc, ±10%;  230Vac 10%, 50/60Hz, 110Vac 10%, 50/60Hz **Power absorption:** 3VA max **Display** : 3 digits, red LED, 14,2 mm high; **Inputs** : Up to 4 NTC or PTC probes. **Digital input:** free voltage contact **Relay outputs: compressor** SPST 8(3) A, 250Vac; or 20(8)A 250Vac **Data storing** : on the non-volatile memory (EEPROM). **Kind of action:** 1B; **Pollution grade:** 2; **Software class:** A.; **Rated impulsive voltage** : 2500V; **Overvoltage Category** : II **Operating temperature:** 0÷60 °C; **Storage temperature:** -30÷85 °C. **Relative humidity:** 2085% (no condensing) **Measuring and regulation range: NTC probe:** -40÷110°C (-40÷230°F);

**PTC probe:** -50÷150°C (-58÷302°F) **Resolution:** 0,1 °C or 1°C or 1 °F (selectable); **Accuracy (ambient temp. 25°C)** :  ±1 °C ±1 digit

##### **16. CONNECTIONS**

**The X-REP output excludes** the TTL output.. It’s present in the following codes: XR20CX- xx **2** xx, XR20CX –xx **3** xx;

*[Figurtekst: 16.1 XR20CX – 8A COMPRESSOR · 9 10 11 12 · 8(3)A250V · 1 2 3 6 7 8 · Hot Key/IV Probe · Comp N.C. TTL or X-REP output · Line · 9-40Vdc supply : connect to the terminals 7 and 8. · 12Vac/dc supply : connect to the terminals 7 and 8. · 24Vac/dc supply : connect to the terminals 7 and 8. · 120Vac supply : connect to the terminals 7 and 8. · Room]*

##### **16.2 XR20CX – 20A COMPRESSOR**

*[Figurtekst: 9 10 11 12 · 20(8)A250V · 4 5 6 7 8 · Hot Key/IV Probe · Comp TTL or X-REP output · Line · 9-40Vdc supply : connect to the terminals 7 and 8. · 12Vac/dc supply : connect to the terminals 7 and 8. · 24Vac/dc supply : connect to the terminals 7 and 8. · 120Vac supply : connect to the terminals 7 and 8. · Room]*

|**17. **<br>|**DEFAULT SETTING VALUES**<br><br>|<br>|||
|---|---|---|---|---|
|**Labe**|**Name**|**Range **|**°C/°F**||
|**Set**|Setpoint|LS÷US|3.0|- - -|
|**Hy **|Differential|0,125.5°C/ 1255°F|2.0|Pr1|
|**LS**|Minimum setpoint|-50°CSET/-58°FSET|-50.0|Pr2|
|**US**|Maximum setpoint|SET110°C/ SET230°F|110|Pr2|
|**Ot**|Thermostatprobe calibration|-1212°C /-120120°F|0.0|Pr1|
|**P3P**|Thirdprobepresence|n=notpresent;Y=pres.|n|Pr2|
|**O3**|Thirdprobe calibration|-1212°C /-120120°F|0|Pr2|
|**P4P**|Fourthprobepresence|n=notpresent;Y=pres.|n|Pr2|
|**O4**|Fourthprobe calibration|-1212°C /-120120°F|0|Pr2|
|**OdS**|Outputs delayat start up|0÷255 min|0|Pr2|
|**AC**|Anti-short cycle delay|050 min|1|Pr1|
|**CCt**|Continuos cycle duration|0.0÷24.0h|0.0|Pr2|
|**CC**<br>**S**|Set point for continuous cycle<br>|(-55.0÷150,0°C) (-67÷302°F)|3|Pr2|
|**CO**<br>**n**|Compressor ON time with faulty probe|0255 min|15|Pr2|
|**CO**<br>**F**|Compressor OFF time with faulty<br>probe<br>|0255 min|30|Pr2|
|**CH**|Kind of action|CL=cooling;Ht= heating|cL|Pr1|

XR20C

|**CF**|Temperature measurement unit|°C°F|°C|Pr2|
|---|---|---|---|---|
|**rES**|Resolution|in=integer; dE= dec.point|dE|Pr1|
|**dLy **|Displaytemperature delay|0 ÷ 20.0 min(10 sec.)|0|Pr2|
|**IdF**|Interval between defrost cycles|1120 ore|8|Pr1|
|**MdF**|(Maximum) length for defrost|0255 min|20|Pr1|
|**dFd**|Displayingduringdefrost|rt, it, SEt, DEF|it|Pr2|
|**dAd**|MAX displaydelayafter defrost|0 ÷ 255 min|30|Pr2|
|**ALc**|Temperat. alarms configuration|rE= related to set;<br>Ab = absolute|Ab|Pr2|
|**ALU**|MAXIMUM temperature alarm|Set110.0°C; Set÷230°F|110|Pr1|
|**ALL**|Minimum temperature alarm|-50.0°CSet/ -58°FSet|-50.0|Pr1|
|**AFH**|Differential for temperat. alarm<br>recovery|(0,1°C÷25,5°C) (1°F÷45°F)|1|Pr2|
|**ALd**|Temperature alarm delay|0255 min|15|Pr2|
|**dAo**|Delayof temperature alarm at start up|023h e 50’|1.3|Pr2|
|**AP2**|Probe for temperat. alarm of<br>condenser|nP; P1; P2; P3; P4|P4|Pr2|
|**AL2**|Condenser for low temperat. alarm|(-55 ÷ 150°C) (-67÷ 302°F)|-40|Pr2|
|**AU2**|Condenser for high temperat. alarm|(-55 ÷ 150°C) (-67÷ 302°F)|110|Pr2|
|**AH2**|<br>Differ. for condenser temp. alar.<br>recovery|<br>[0,1°C ÷ 25,5°C]  [1°F ÷<br>45°F]|5|Pr2|
|**Ad2**|Condenser temperature alarm delay|0 ÷ 254(min.) ,255=nU|15|Pr2|
|**dA2**|<br>Delay of cond. temper. alarm at start<br>up|<br>0.0 ÷ 23h  50’|1,3|Pr2|
|**bLL**|<br>Compr.<br>off<br>for<br>condenser<br>low<br>temperature alarm|<br>n(0)- Y(1)|n|Pr2|
|**AC2**|<br>Compr. off for condenser high<br>temperature alarm|<br>n(0)- Y(1)|n|Pr2|
|**i1P**|Digital inputpolarity|oP=opening;CL=closing|cL|Pr1|
|**i1F**|Digital input configuration|EAL, bAL, PAL, dor; dEF; Htr,<br>AUS|dor|Pr1|
|**did**|Digital input alarm delay|0÷255min|15|Pr1|
|**nPS**|Number of activation of pressure<br>switch|<br>0 ÷15|15|Pr2|
|**odc**|Compress status when open door|no;Fan;CPr;F_C|no|Pr2|
|**rrd**|Regulation restart with door open<br>alarm|n – Y|y|Pr2|
|**HES**|Differential for EnergySaving|(-30°C÷30°C) (-54°F÷54°F)|0|Pr2|
|**Adr**|Serial address|0÷247|1|Pr2|
|**PbC**|Kind ofprobe|Ptc;ntc|ntc|Pr1|
|**onF**|on/off keyenabling|nu,oFF;ES|nu|Pr2|
|**dP1**|Roomprobe display|--|--|Pr1|
|**dP3**|Thirdprobe display|--|--|Pr1|
|**dP4**|Fourthprobe display|--|--|Pr2|
|**rSE**|Real setpoint value|actual set|--|Pr2|
|**rEL**|Software release|--|--|Pr2|
|**Ptb**|Mapcode|--|--|Pr2|
