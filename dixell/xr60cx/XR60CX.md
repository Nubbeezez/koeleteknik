# Dixell XR60CX – manual til fejlfinding

Digital controller with defrost and fans management – **XR60CX**. Kilde: Dixell-dokument 1592020060 XR60CX GB r1.1 (27.04.2015), filen `XR60CX-GB.pdf` i denne mappe.

Konverteret direkte fra PDF'en og sat op i Markdown. Tabeller (parametre, alarmer, LED'er, standardværdier) er bevaret som Markdown-tabeller. Billeder og tilslutningstegninger er udeladt; tekst fra tegningerne står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilket afsnit svaret kommer fra.
- Alarmbeskeder (fx `HA`, `P1`, `CA`) og parameterkoder (fx `Hy`, `IdF`, `FnC`) kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer (Dixell vs. Danfoss). Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualen, så sig det i stedet for at gætte.

---

## Indhold (fra manualen)

1. General warning
2. General description
3. Controlling loads
4. Front panel commands
5. Max & min temperature memorization
6. Main functions
7. Parameters
8. Digital input (enabled with P3P = n)
9. TTL serial line – for monitoring systems
10. X-REP output – optional
11. Installation and mounting
12. Electrical connections
13. How to use the HOT KEY
14. Alarm signals
15. Technical data
16. Connections
17. Default setting values

## 1. General warning

### 1.1 Please read before using this manual

- This manual is part of the product and should be kept near the instrument for easy and quick reference.
- The instrument shall not be used for purposes different from those described hereunder. It cannot be used as a safety device.
- Check the application limits before proceeding.
- Dixell Srl reserves the right to change the composition of its products, even without notice, ensuring the same and unchanged functionality.

### 1.2 Safety precautions

- Check the supply voltage is correct before connecting the instrument.
- Do not expose to water or moisture: use the controller only within the operating limits avoiding sudden temperature changes with high atmospheric humidity to prevent formation of condensation.
- Warning: disconnect all electrical connections before any kind of maintenance.
- Fit the probe where it is not accessible by the End User. The instrument must not be opened.
- In case of failure or faulty operation send the instrument back to the distributor or to "Dixell S.r.l." (see address) with a detailed description of the fault.
- Consider the maximum current which can be applied to each relay (see Technical Data).
- Ensure that the wires for probes, loads and the power supply are separated and far enough from each other, without crossing or intertwining.
- In case of applications in industrial environments, the use of mains filters (our mod. FT1) in parallel with inductive loads could be useful.

## 2. General description

Model XR60CX, format 32 x 74 mm, is microprocessor based controller, suitable for applications on medium or low temperature ventilated refrigerating units. It has three relay outputs to control compressor, fan, and defrost, which can be either electrical or reverse cycle (hot gas). It is also provided with three NTC or PTC probe inputs, the first one for temperature control, the second one, to be located onto the evaporator, to control the defrost termination temperature and to managed the fan, the third one, optional, to connect to the HOT KEY terminals to signal the condenser temperature alarm or to display a temperature. The digital input can operate as fourth temperature probe.

The HOT KEY output allows to connect the unit, by means of the external module XJ485-CX, to a network line ModBUS-RTU compatible such as the Dixell monitoring units of X-WEB family. It allows to program the controller by means the HOT KEY programming keyboard. The instrument is fully configurable through special parameters that can be easily programmed through the keyboard.

## 3. Controlling loads

### 3.1 Compressor

The regulation is performed according to the temperature measured by the thermostat probe with a positive differential from the set point: if the temperature increases and reaches set point plus differential the compressor is started and then turned off when the temperature reaches the set point value again.

*[Figurtekst: Temper. · SET · Compr. ON · Time]*

In case of fault in the thermostat probe the start and stop of the compressor are timed through parameters "COn" and "COF".

### 3.2 Defrost

Two defrost modes are available through the "tdF" parameter: defrost through electrical heater (tdF = EL) and hot gas defrost (tdF = in). Other parameters are used to control the interval between defrost cycles (IdF), its maximum length (MdF) and two defrost modes: timed or controlled by the evaporator's probe (P2P). At the end of defrost dripping time is started, its length is set in the Fdt parameter. With Fdt = 0 the dripping time is disabled.

### 3.3 Control of evaporator fans

The fan control mode is selected by means of the "FnC" parameter:

- **FnC = C_n:** fans will switch ON and OFF with the compressor and **not run** during defrost.
- **FnC = o_n:** fans will run even if the compressor is off, and not run during defrost.
- After defrost, there is a timed fan delay allowing for drip time, set by means of the "Fnd" parameter.
- **FnC = C_Y:** fans will switch ON and OFF with the compressor and **run** during defrost.
- **FnC = o_Y:** fans will run continuously also during defrost.

An additional parameter "FSt" provides the setting of temperature, detected by the evaporator probe, above which the fans are always OFF. This is used to make sure circulation of air only if his temperature is lower than set in "FSt".

#### 3.3.1 Forced activation of fans

This function managed by the Fct parameter is designed to avoid short cycles of fans, that could happen when the controller is switched on or after a defrost, when the room air warms the evaporator. **Functioning:** if the difference of temperature between the evaporator and the room probes is more than the value of the Fct parameter, the fans are switched on. With Fct = 0 the function is disabled.

#### 3.3.2 Cyclical activation of the fans with compressor off

When Fnc = c-n or c-Y (fans in parallel to the compressor), by means of the Fon and FoF parameters the fans can carry out on and off cycles even if the compressor is switched off. When the compressor is stopped the fans go on working for the Fon time. With Fon = 0 the fans remain always off, when the compressor is off.

## 4. Front panel commands

| Key | Function |
|---|---|
| SET | To display target set point; in programming mode it selects a parameter or confirm an operation. |
| DEF | To start a manual defrost. |
| UP (o) | To see the max. stored temperature; in programming mode it browses the parameter codes or increases the displayed value. |
| DOWN (n) | To see the min stored temperature; in programming mode it browses the parameter codes or decreases the displayed value. |
| ON/OFF | To switch the instrument off, if onF = oFF. |
| (light key) | Not enabled. |

**Key combinations:**

| Combination | Function |
|---|---|
| UP + DOWN | To lock & unlock the keyboard. |
| SET + DOWN | To enter in programming mode. |
| SET + UP | To return to the room temperature display. |

*(I PDF'en er tasterne vist som symboler. Kombinationerne ovenfor følger rækkefølgen i manualen og stemmer med afsnit 6.4–6.7.)*

### 4.1 Use of LEDs

Each LED function is described in the following table.

| LED | Mode | Function |
|---|---|---|
| Compressor | ON | Compressor enabled |
| Compressor | Flashing | Anti-short cycle delay enabled |
| Defrost | ON | Defrost enabled |
| Defrost | Flashing | Drip time in progress |
| Fan | ON | Fans enabled |
| Fan | Flashing | Fans delay after defrost in progress |
| Alarm | ON | An alarm is occurring |
| Continuous cycle | ON | Continuous cycle is running |
| Energy saving | ON | Energy saving enabled |
| °C/°F | ON | Measurement unit |
| °C/°F | Flashing | Programming phase |

## 5. Max & min temperature memorization

### 5.1 How to see the min temperature

1. Press and release the DOWN (n) key.
2. The "Lo" message will be displayed followed by the minimum temperature recorded.
3. By pressing the DOWN (n) key again or by waiting 5 s the normal display will be restored.

### 5.2 How to see the max temperature

1. Press and release the UP (o) key.
2. The "Hi" message will be displayed followed by the maximum temperature recorded.
3. By pressing the UP (o) key again or by waiting 5 s the normal display will be restored.

### 5.3 How to reset the max and min temperature recorded

1. Hold press the SET key for more than 3 s, while the max. or min temperature is displayed. ("rSt" message will be displayed.)
2. To confirm the operation the "rSt" message starts blinking and the normal temperature will be displayed.

## 6. Main functions

### 6.1 How to see the setpoint

1. Push and immediately release the SET key: the display will show the Set point value.
2. Push and immediately release the SET key or wait for 5 seconds to display the probe value again.

### 6.2 How to change the setpoint

1. Push the SET key for more than 2 seconds to change the Set point value.
2. The value of the set point will be displayed and the "°C" or "°F" LED starts blinking.
3. To change the Set value push the UP (o) or DOWN (n) arrows within 10 s.
4. To memorise the new set point value push the SET key again or wait 10 s.

### 6.3 How to start a manual defrost

Push the DEF key for more than 2 seconds and a manual defrost will start.

### 6.4 How to change a parameter value

To change the parameter's value operate as follows:

1. Enter the Programming mode by pressing the SET + DOWN (n) keys for 3 s (the "°C" or "°F" LED starts blinking).
2. Select the required parameter. Press the "SET" key to display its value.
3. Use "UP" or "DOWN" to change its value.
4. Press "SET" to store the new value and move to the following parameter.

To exit: Press SET + UP or wait 15 s without pressing a key.

NOTE: the set value is stored even when the procedure is exited by waiting the time-out to expire.

### 6.5 The hidden menu

The hidden menu includes all the parameters of the instrument.

#### 6.5.1 How to enter the hidden menu

1. Enter the Programming mode by pressing the SET + DOWN (n) keys for 3 s (the "°C" or "°F" LED starts blinking).
2. Release the keys, then push again the SET + DOWN (n) keys for more than 7 s. The Pr2 label will be displayed immediately followed from the HY parameter. NOW YOU ARE IN THE HIDDEN MENU.
3. Select the required parameter.
4. Press the "SET" key to display its value.
5. Use UP (o) or DOWN (n) to change its value.
6. Press "SET" to store the new value and move to the following parameter.

To exit: Press SET + UP (o) or wait 15 s without pressing a key.

NOTE 1: if none parameter is present in Pr1, after 3 s the "noP" message is displayed. Keep the keys pushed till the Pr2 message is displayed.

NOTE 2: the set value is stored even when the procedure is exited by waiting the time-out to expire.

#### 6.5.2 How to move a parameter from the hidden menu to the first level and viceversa

Each parameter present in the HIDDEN MENU can be removed or put into "THE FIRST LEVEL" (user level) by pressing "SET + DOWN (n)". In HIDDEN MENU when a parameter is present in First Level the decimal point is on.

### 6.6 How to lock the keyboard

1. Keep pressed for more than 3 s the UP + DOWN keys.
2. The "POF" message will be displayed and the keyboard will be locked. At this point it will be possible only to see the set point or the MAX or Min temperature stored.
3. If a key is pressed more than 3 s the "POF" message will be displayed.

### 6.7 To unlock the keyboard

Keep pressed together for more than 3 s the UP (o) and DOWN (n) keys, till the "Pon" message will be displayed.

### 6.8 The continuous cycle

When defrost is not in progress, it can be activated by holding the UP (o) key pressed for about 3 seconds. The compressor operates to maintain the "ccS" set point for the time set through the "CCt" parameter. The cycle can be terminated before the end of the set time using the same activation key UP (o) for 3 seconds.

### 6.9 The ON/OFF function

With "onF = oFF", pushing the ON/OFF key, the instrument is switched off. The "OFF" message is displayed. In this configuration, the regulation is disabled. To switch the instrument on, push again the ON/OFF key.

**WARNING:** Loads connected to the normally closed contacts of the relays are always supplied and under voltage, even if the instrument is in stand by mode.

## 7. Parameters

### Regulation

| Code | Name | Range / values | Description |
|---|---|---|---|
| Hy | Differential | 0.1 ÷ 25.5 °C / 1 ÷ 255 °F | Intervention differential for set point. Compressor Cut IN is Set Point + differential (Hy). Compressor Cut OUT is when the temperature reaches the set point. |
| LS | Minimum set point | -50 °C ÷ SET / -58 °F ÷ SET | Sets the minimum value for the set point. |
| US | Maximum set point | SET ÷ 110 °C / SET ÷ 230 °F | Set the maximum value for set point. |
| Ot | Thermostat probe calibration | -12.0 ÷ 12.0 °C; -120 ÷ 120 °F | Allows to adjust possible offset of the thermostat probe. |
| P2P | Evaporator probe presence | n / y | n = not present: the defrost stops by time; y = present: the defrost stops by temperature. |
| OE | Evaporator probe calibration | -12.0 ÷ 12.0 °C; -120 ÷ 120 °F | Allows to adjust possible offset of the evaporator probe. |
| P3P | Third probe presence (P3) | n / y | n = not present: the terminal operates as digital input; y = present: the terminal operates as third probe. |
| O3 | Third probe calibration (P3) | -12.0 ÷ 12.0 °C; -120 ÷ 120 °F | Allows to adjust possible offset of the third probe. |
| P4P | Fourth probe presence | n / y | n = not present; y = present. |
| o4 | Fourth probe calibration | -12.0 ÷ 12.0 °C | Allows to adjust possible offset of the fourth probe. |
| OdS | Outputs activation delay at start up | 0 ÷ 255 min | This function is enabled at the initial start up of the instrument and inhibits any output activation for the period of time set in the parameter. |
| AC | Anti-short cycle delay | 0 ÷ 50 min | Minimum interval between the compressor stop and the following restart. |
| rtr | Percentage of the second and first probe for regulation | 0 ÷ 100 (100 = P1, 0 = P2) | Allows to set the regulation according to the percentage of the first and second probe, as for the following formula: rtr(P1-P2)/100 + P2. |
| CCt | Compressor ON time during continuous cycle | 0.0 ÷ 24.0 h; res. 10 min | Allows to set the length of the continuous cycle: compressor stays on without interruption for the CCt time. Can be used, for instance, when the room is filled with new products. |
| CCS | Set point for continuous cycle | -50 ÷ 150 °C | Sets the set point used during the continuous cycle. |
| COn | Compressor ON time with faulty probe | 0 ÷ 255 min | Time during which the compressor is active in case of faulty thermostat probe. With COn = 0 compressor is always OFF. |
| COF | Compressor OFF time with faulty probe | 0 ÷ 255 min | Time during which the compressor is OFF in case of faulty thermostat probe. With COF = 0 compressor is always active. |

### Display

| Code | Name | Range / values | Description |
|---|---|---|---|
| CF | Temperature measurement unit | °C = Celsius; °F = Fahrenheit | WARNING: When the measurement unit is changed the SET point and the values of the parameters Hy, LS, US, Ot, ALU and ALL have to be checked and modified if necessary. |
| rES | Resolution (for °C) | in = 1 °C; dE = 0.1 °C | Allows decimal point display. |
| Lod | Instrument display | P1; P2; P3; P4; SET; dtr | Selects which probe is displayed by the instrument: P1 = Thermostat probe; P2 = Evaporator probe; P3 = Third probe (only for model with this option enabled); P4 = Fourth probe; SET = set point; dtr = percentage of visualization. |
| rEd | X-REP display (optional) | P1; P2; P3; P4; SET; dtr | Selects which probe is displayed by X-REP: P1 = Thermostat probe; P2 = Evaporator probe; P3 = Third probe (only for model with this option enabled); P4 = Fourth probe; SET = set point; dtr = percentage of visualization. |
| dLy | Display delay | 0 ÷ 20.0 min; res. 10 s | When the temperature increases, the display is updated of 1 °C / 1 °F after this time. |
| dtr | Percentage of the second and first probe for visualization when Lod = dtr | 0 ÷ 100 (100 = P1, 0 = P2) | If Lod = dtr it allows to set the visualization according to the percentage of the first and second probe, as for the following formula: dtr(P1-P2)/100 + P2. |

### Defrost

| Code | Name | Range / values | Description |
|---|---|---|---|
| dFP | Probe selection for defrost termination | nP; P1; P2; P3; P4 | nP = no probe; P1 = thermostat probe; P2 = evaporator probe; P3 = configurable probe; P4 = probe on Hot Key plug. |
| tdF | Defrost type | EL; in | EL = electrical heater; in = hot gas. |
| dtE | Defrost termination temperature | -50 ÷ 50 °C / -58 ÷ 122 °F | (Enabled only when EdF = Pb.) Sets the temperature measured by the evaporator probe, which causes the end of defrost. |
| IdF | Interval between defrost cycles | 0 ÷ 120 h | Determines the time interval between the beginning of two defrost cycles. |
| MdF | (Maximum) length for defrost | 0 ÷ 255 min | When P2P = n (no evaporator probe: timed defrost) it sets the defrost duration; when P2P = y (defrost end based on temperature) it sets the maximum length for defrost. |
| dSd | Start defrost delay | 0 ÷ 99 min | This is useful when different defrost start times are necessary to avoid overloading the plant. |
| dFd | Temperature displayed during defrost | rt; it; SEt; dEF | rt = real temperature; it = temperature at defrost start; SEt = set point; dEF = "dEF" label. |
| dAd | MAX display delay after defrost | 0 ÷ 255 min | Sets the maximum time between the end of defrost and the restarting of the real room temperature display. |
| Fdt | Drip time | 0 ÷ 120 min | Time interval between reaching defrost termination temperature and the restoring of the control's normal operation. This time allows the evaporator to eliminate water drops that might have formed due to defrost. |
| dPo | First defrost after start-up | y; n | y = immediately; n = after the IdF time. |
| dAF | Defrost delay after continuous cycle | 0 ÷ 23.5 h | Time interval between the end of the fast freezing cycle and the following defrost related to it. |

### Fans

| Code | Name | Range / values | Description |
|---|---|---|---|
| FnC | Fans operating mode | C-n; o-n; C-Y; o-Y | C-n = runs with the compressor, OFF during defrost; o-n = continuous mode, OFF during defrost; C-Y = runs with the compressor, ON during defrost; o-Y = continuous mode, ON during defrost. |
| Fnd | Fans delay after defrost | 0 ÷ 255 min | Interval between end of defrost and evaporator fans start. |
| Fct | Temperature differential avoiding short cycles of fans | 0 ÷ 59 °C (Fct = 0 function disabled) | If the difference of temperature between the evaporator and the room probes is more than the value of the Fct parameter, the fans are switched on. |
| FSt | Fans stop temperature | -50 ÷ 50 °C / 122 °F | Setting of temperature, detected by evaporator probe, above which fans are always OFF. |
| Fon | Fan ON time | 0 ÷ 15 min | With Fnc = C_n or C_y (fan activated in parallel with compressor) it sets the evaporator fan ON cycling time when the compressor is off. With Fon = 0 and FoF ≠ 0 the fan are always off, with Fon = 0 and FoF = 0 the fan are always off. |
| FoF | Fan OFF time | 0 ÷ 15 min | With Fnc = C_n or C_y (fan activated in parallel with compressor) it sets the evaporator fan off cycling time when the compressor is off. With Fon = 0 and FoF ≠ 0 the fan are always off, with Fon = 0 and FoF = 0 the fan are always off. |
| FAP | Probe selection for fan management | nP; P1; P2; P3; P4 | nP = no probe; P1 = thermostat probe; P2 = evaporator probe; P3 = configurable probe; P4 = probe on Hot Key plug. |

### Alarms

| Code | Name | Range / values | Description |
|---|---|---|---|
| ALC | Temperature alarms configuration | Ab; rE | Ab = absolute temperature: alarm temperature is given by the ALL or ALU values. rE = temperature alarms are referred to the set point. Temperature alarm is enabled when the temperature exceeds the "SET+ALU" or "SET-ALL" values. |
| ALU | MAXIMUM temperature alarm | SET ÷ 110 °C; SET ÷ 230 °F | When this temperature is reached the alarm is enabled, after the "ALd" delay time. |
| ALL | Minimum temperature alarm | -50.0 ÷ SET °C; -58 ÷ 230 °F | When this temperature is reached the alarm is enabled, after the "ALd" delay time. |
| AFH | Differential for temperature alarm / fan recovery | 0.1 ÷ 25.5 °C; 1 ÷ 45 °F | Intervention differential for recovery of temperature alarm. It's also used for the restart of the fan when the FSt temperature is reached. |
| ALd | Temperature alarm delay | 0 ÷ 255 min | Time interval between the detection of an alarm condition and alarm signalling. |
| dAO | Exclusion of temperature alarm at startup | 0.0 min ÷ 23.5 h | Time interval between the detection of the temperature alarm condition after instrument power on and alarm signalling. |

### Condenser temperature alarm

| Code | Name | Range / values | Description |
|---|---|---|---|
| AP2 | Probe selection for temperature alarm of condenser | nP; P1; P2; P3; P4 | nP = no probe; P1 = thermostat probe; P2 = evaporator probe; P3 = configurable probe; P4 = probe on Hot Key plug. |
| AL2 | Low temperature alarm of condenser | -55 ÷ 150 °C | When this temperature is reached the LA2 alarm is signalled, possibly after the Ad2 delay. |
| Au2 | High temperature alarm of condenser | -55 ÷ 150 °C | When this temperature is reached the HA2 alarm is signalled, possibly after the Ad2 delay. |
| AH2 | Differential for temperature condenser alarm recovery | 0.1 ÷ 25.5 °C; 1 ÷ 45 °F | |
| Ad2 | Condenser temperature alarm delay | 0 ÷ 255 min | Time interval between the detection of the condenser alarm condition and alarm signalling. |
| dA2 | Condenser temperature alarm exclusion at start up | 0.0 min ÷ 23.5 h, res. 10 min | |
| bLL | Compressor off with low temperature alarm of condenser | n; Y | n = no: compressor keeps on working; Y = yes, compressor is switched off till the alarm is present, in any case regulation restarts after AC time at minimum. |
| AC2 | Compressor off with high temperature alarm of condenser | n; Y | n = no: compressor keeps on working; Y = yes, compressor is switched off till the alarm is present, in any case regulation restarts after AC time at minimum. |

### Digital input

| Code | Name | Range / values | Description |
|---|---|---|---|
| i1P | Digital input polarity | oP; CL | oP: the digital input is activated by opening the contact; CL: the digital input is activated by closing the contact. |
| i1F | Digital input configuration | EAL; bAL; PAL; dor; dEF; AUS; Htr; FAn; ES | EAL = external alarm: "EA" message is displayed; bAL = serious alarm: "CA" message is displayed; PAL = pressure switch alarm: "CA" message is displayed; dor = door switch function; dEF = activation of a defrost cycle; AUS = not enabled; Htr = kind of action inversion (cooling – heating); FAn = not set it; ES = Energy saving. |
| did | Digital input alarm delay | 0 ÷ 255 min | With i1F = EAL or i1F = bAL: delay between the detection of the external alarm condition and its signalling. With i1F = dor: door open signalling delay. With i1F = PAL: time for pressure switch function: time interval to calculate the number of the pressure switch activation. |
| nPS | Pressure switch number | 0 ÷ 15 | Number of activation of the pressure switch, during the "did" interval, before signalling the alarm event (i1F = PAL). If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation. |
| odc | Compressor and fan status when open door | no; FAn; CPr; F_C | no = normal; FAn = Fan OFF; CPr = Compressor OFF; F_C = Compressor and fan OFF. |
| rrd | Outputs restart after doA alarm | no; yES | no = outputs not affected by the doA alarm; yES = outputs restart with the doA alarm. |
| HES | Temperature increase during the Energy Saving cycle | -30.0 ÷ 30.0 °C / -22 ÷ 86 °F | Sets the increasing value of the set point during the Energy Saving cycle. |

### Other

| Code | Name | Range / values | Description |
|---|---|---|---|
| Adr | Serial address | 1 ÷ 247 | Identifies the instrument address when connected to a ModBUS compatible monitoring system. |
| PbC | Type of probe | PtC; ntc | Allows to set the kind of probe used by the instrument: PtC = PTC probe, ntc = NTC probe. |
| onF | on/off key enabling | nu; oFF; ES | nu = disabled; oFF = enabled; ES = not set it. |
| dP1 | Thermostat probe display | – | |
| dP2 | Evaporator probe display | – | |
| dP3 | Third probe display (optional) | – | |
| dP4 | Fourth probe display | – | |
| rSE | Real set point | readable only | Shows the set point used during the energy saving cycle or during the continuous cycle. |
| rEL | Software release | – | For internal use. |
| Ptb | Parameter table code | readable only | |

## 8. Digital input (enabled with P3P = n)

The free voltage digital input is programmable in different configurations by the "i1F" parameter.

### 8.1 Door switch input (i1F = dor)

It signals the door status and the corresponding relay output status through the "odc" parameter: no = normal (any change); FAn = Fan OFF; CPr = Compressor OFF; F_C = Compressor and fan OFF. Since the door is opened, after the delay time set through parameter "did", the door alarm is enabled, the display shows the message "dA" and the regulation restarts if rrd = yES. The alarm stops as soon as the external digital input is disabled again. With the door open, the high and low temperature alarms are disabled.

### 8.2 Generic alarm (i1F = EAL)

As soon as the digital input is activated the unit will wait for "did" time delay before signalling the "EAL" alarm message. The outputs status don't change. The alarm stops just after the digital input is de-activated.

### 8.3 Serious alarm mode (i1F = bAL)

When the digital input is activated, the unit will wait for "did" delay before signalling the "CA" alarm message. The relay outputs are switched OFF. The alarm will stop as soon as the digital input is deactivated.

### 8.4 Pressure switch (i1F = PAL)

If during the interval time set by "did" parameter, the pressure switch has reached the number of activation of the "nPS" parameter, the "CA" pressure alarm message will be displayed. The compressor and the regulation are stopped. When the digital input is ON the compressor is always OFF. If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation.

### 8.5 Start defrost (i1F = dFr)

It starts a defrost if there are the right conditions. After the defrost is finished, the normal regulation will restart only if the digital input is disabled otherwise the instrument will wait until the "MdF" safety time is expired.

### 8.6 Inversion of the kind of action: heating-cooling (i1F = Htr)

This function allows to invert the regulation of the controller: from cooling to heating and viceversa.

### 8.7 Energy saving (i1F = ES)

The Energy Saving function allows to change the set point value as the result of the SET + HES (parameter) sum. This function is enabled until the digital input is activated.

### 8.8 Digital inputs polarity

The digital input polarity depends on the "i1P" parameter. i1P = CL: the input is activated by closing the contact. i1P = OP: the input is activated by opening the contact.

## 9. TTL serial line – for monitoring systems

The TTL serial line, available through the HOT KEY connector, allows by means of the external TTL/RS485 converter, XJ485-CX, to connect the instrument to a monitoring system ModBUS-RTU compatible such as the X-WEB500/3000/300.

## 10. X-REP output – optional

As optional, an X-REP can be connected to the instrument, through the HOT KEY connector. The X-REP output EXCLUDES the serial connection.

To connect the X-REP to the instrument the following connectors must be used: CAB-51F (1 m), CAB-52F (2 m), CAB-55F (5 m).

## 11. Installation and mounting

Instrument XR60CX shall be mounted on vertical panel, in a 29 x 71 mm hole, and fixed using the special bracket supplied. The temperature range allowed for correct operation is 0 ÷ 60 °C. Avoid places subject to strong vibrations, corrosive gases, excessive dirt or humidity. The same recommendations apply to probes. Let air circulate by the cooling holes.

## 12. Electrical connections

The instrument is provided with screw terminal block to connect cables with a cross section up to 2.5 mm². Before connecting cables make sure the power supply complies with the instrument's requirements. Separate the probe cables from the power supply cables, from the outputs and the power connections. Do not exceed the maximum current allowed on each relay, in case of heavier loads use a suitable external relay.

### 12.1 Probe connection

The probes shall be mounted with the bulb upwards to prevent damages due to casual liquid infiltration. It is recommended to place the thermostat probe away from air streams to correctly measure the average room temperature. Place the defrost termination probe among the evaporator fins in the coldest place, where most ice is formed, far from heaters or from the warmest place during defrost, to prevent premature defrost termination.

## 13. How to use the HOT KEY

### 13.1 How to program a HOT KEY from the instrument (upload)

1. Program one controller with the front keypad.
2. When the controller is ON, insert the "Hot key" and push the UP (o) key; the "uPL" message appears followed by a flashing "End".
3. Push "SET" key and the End will stop flashing.
4. Turn OFF the instrument, remove the "Hot Key", then turn it ON again.

NOTE: the "Err" message is displayed for failed programming. In this case push again the UP (o) key if you want to restart the upload again or remove the "Hot key" to abort the operation.

### 13.2 How to program an instrument using a HOT KEY (download)

1. Turn OFF the instrument.
2. Insert a programmed "Hot Key" into the 5 PIN receptacle and then turn the Controller ON.
3. Automatically the parameter list of the "Hot Key" is downloaded into the Controller memory, the "doL" message is blinking followed by a flashing "End".
4. After 10 seconds the instrument will restart working with the new parameters.
5. Remove the "Hot Key".

NOTE: the message "Err" is displayed for failed programming. In this case turn the unit off and then on if you want to restart the download again or remove the "Hot key" to abort the operation.

## 14. Alarm signals

| Message | Cause | Outputs |
|---|---|---|
| P1 | Room probe failure | Compressor output acc. to par. "COn" and "COF" |
| P2 | Evaporator probe failure | Defrost end is timed |
| P3 | Third probe failure | Outputs unchanged |
| P4 | Fourth probe failure | Outputs unchanged |
| HA | Maximum temperature alarm | Outputs unchanged |
| LA | Minimum temperature alarm | Outputs unchanged |
| HA2 | Condenser high temperature | It depends on the "AC2" parameter |
| LA2 | Condenser low temperature | It depends on the "bLL" parameter |
| dA | Door open | Compressor and fans restarts |
| EA | External alarm | Output unchanged |
| CA | Serious external alarm (i1F = bAL) | All outputs OFF |
| CA | Pressure switch alarm (i1F = PAL) | All outputs OFF |

### 14.1 Alarm recovery

Probe alarms "P1", "P2", "P3" and "P4" start some seconds after the fault in the related probe; they automatically stop some seconds after the probe restarts normal operation. Check connections before replacing the probe.

Temperature alarms "HA", "LA", "HA2" and "LA2" automatically stop as soon as the temperature returns to normal values.

Alarms "EA" and "CA" (with i1F = bAL) recover as soon as the digital input is disabled.

Alarm "CA" (with i1F = PAL) recovers only by switching off and on the instrument.

### 14.2 Other messages

| Message | Meaning |
|---|---|
| Pon | Keyboard unlocked. |
| PoF | Keyboard locked. |
| noP | In programming mode: none parameter is present in Pr1. On the display or in dP2, dP3, dP4: the selected probe is not enabled. |
| noA | None alarm is recorded. |

## 15. Technical data

| Item | Value |
|---|---|
| Housing | Self extinguishing ABS |
| Case | XR60CX frontal 32 x 74 mm; depth 60 mm |
| Mounting | XR60CX panel mounting in a 71 x 29 mm panel cut-out |
| Protection | IP20 |
| Frontal protection | XR60CX IP65 |
| Connections | Screw terminal block ≤ 2.5 mm² wiring |
| Power supply | According to the model: 12 Vac/dc ±10 %; 24 Vac/dc ±10 %; 230 Vac ±10 %, 50/60 Hz; 110 Vac ±10 %, 50/60 Hz |
| Power absorption | 3 VA max |
| Display | 3 digits, red LED, 14.2 mm high |
| Inputs | Up to 4 NTC or PTC probes |
| Digital input | Free voltage contact |
| Relay outputs – compressor | SPST 8(3) A, 250 Vac; SPST 16(6) A 250 Vac or 20(8) A 250 Vac |
| Relay outputs – defrost | SPDT 8(3) A, 250 Vac |
| Relay outputs – fan | SPST 8(3) A, 250 Vac or SPST 5(2) A |
| Data storing | On the non-volatile memory (EEPROM) |
| Kind of action | 1B |
| Pollution grade | 2 |
| Software class | A |
| Rated impulsive voltage | 2500 V |
| Overvoltage category | II |
| Operating temperature | 0 ÷ 60 °C |
| Storage temperature | -30 ÷ 85 °C |
| Relative humidity | 20 ÷ 85 % (no condensing) |
| Measuring and regulation range | NTC probe: -40 ÷ 110 °C (-40 ÷ 230 °F); PTC probe: -50 ÷ 150 °C (-58 ÷ 302 °F) |
| Resolution | 0.1 °C or 1 °C or 1 °F (selectable) |
| Accuracy (ambient temp. 25 °C) | ±0.7 °C ±1 digit |

## 16. Connections

The X-REP output excludes the TTL output. It's present in the following codes: XR60CX-xx2xx, XR60CX-xx3xx.

### 16.1 XR60CX – 8A or 16A comp. relay – 12 Vac/dc or 24 Vac/dc

*[Figurtekst: Terminals 1–8 (power side) and 9–12 (probes) · Evap. · Room · N.C. · Def · Fan · Comp · Line · 8(3)A · Max 16A · 8(3)A 250V~ · Hot Key / IV probe / TTL or X-REP output]*

NOTE: The compressor relay is 8(3)A or 16(6)A according to the model. 24 Vac/dc supply: connect to the terminals 7 and 8.

### 16.2 XR60CX – 8A or 16A comp. relay – 120 Vac or 230 Vac

*[Figurtekst: Terminals 1–7 (power side) and 9–12 (probes) · Evap. · Room · N.C. · Def · Fan · Comp · Line · 8(3)A · Max 16A · 8(3)A 250V~ · Hot Key / IV probe / TTL or X-REP output]*

NOTE: The compressor relay is 8(3)A or 16(6)A according to the model. 120 Vac supply: connect to the terminals 6 and 7.

### 16.3 XR60C – 20A comp. relay – 120 Vac or 230 Vac

*[Figurtekst: Terminals 1–8 (power side) and 9–12 (probes) · Evap. · Room · Line · Fan · Comp · Def · N.C. · 20(8)A 250V~ · Max 20A · 5(1)A · 8(3)A 250V~ · Hot Key / IV probe · TTL or X-REP output]*

120 Vac supply: connect to the terminals 5 and 6.

## 17. Default setting values

Level: **Pr1** = first (user) level, **Pr2** = hidden menu (see 6.5).

| Label | Name | Range | Default | Level |
|---|---|---|---|---|
| Set | Set point | LS ÷ US | -5.0 | – |
| Hy | Differential | 0.1 ÷ 25.5 °C / 1 ÷ 255 °F | 2.0 | Pr1 |
| LS | Minimum set point | -50 °C ÷ SET / -58 °F ÷ SET | -50.0 | Pr2 |
| US | Maximum set point | SET ÷ 110 °C / SET ÷ 230 °F | 110 | Pr2 |
| Ot | Thermostat probe calibration | -12 ÷ 12 °C / -120 ÷ 120 °F | 0.0 | Pr1 |
| P2P | Evaporator probe presence | n = not present; Y = pres. | Y | Pr1 |
| OE | Evaporator probe calibration | -12 ÷ 12 °C / -120 ÷ 120 °F | 0.0 | Pr2 |
| P3P | Third probe presence | n = not present; Y = pres. | n | Pr2 |
| O3 | Third probe calibration | -12 ÷ 12 °C / -120 ÷ 120 °F | 0 | Pr2 |
| P4P | Fourth probe presence | n = not present; Y = pres. | n | Pr2 |
| O4 | Fourth probe calibration | -12 ÷ 12 °C / -120 ÷ 120 °F | 0 | Pr2 |
| OdS | Outputs delay at start up | 0 ÷ 255 min | 0 | Pr2 |
| AC | Anti-short cycle delay | 0 ÷ 50 min | 1 | Pr1 |
| rtr | P1-P2 percentage for regulation | 0 ÷ 100 (100 = P1, 0 = P2) | 100 | Pr2 |
| CCt | Continuous cycle duration | 0.0 ÷ 24.0 h | 0.0 | Pr2 |
| CCS | Set point for continuous cycle | -55.0 ÷ 150.0 °C / -67 ÷ 302 °F | -5 | Pr2 |
| COn | Compressor ON time with faulty probe | 0 ÷ 255 min | 15 | Pr2 |
| COF | Compressor OFF time with faulty probe | 0 ÷ 255 min | 30 | Pr2 |
| CF | Temperature measurement unit | °C ÷ °F | °C | Pr2 |
| rES | Resolution | in = integer; dE = dec. point | dE | Pr1 |
| Lod | Probe displayed | P1; P2 | P1 | Pr2 |
| rEd ² | X-REP display | P1 – P2 – P3 – P4 – SEt – dtr | P1 | Pr2 |
| dLy | Display temperature delay | 0 ÷ 20.0 min (10 sec.) | 0 | Pr2 |
| dtr | P1-P2 percentage for display | 1 ÷ 99 | 50 | Pr2 |
| tdF | Defrost type | EL = el. heater; in = hot gas | EL | Pr1 |
| dFP | Probe selection for defrost termination | nP; P1; P2; P3; P4 | P2 | Pr2 |
| dtE | Defrost termination temperature | -50 ÷ 50 °C | 8 | Pr1 |
| IdF | Interval between defrost cycles | 1 ÷ 120 h | 6 | Pr1 |
| MdF | (Maximum) length for defrost | 0 ÷ 255 min | 30 | Pr1 |
| dSd | Start defrost delay | 0 ÷ 99 min | 0 | Pr2 |
| dFd | Displaying during defrost | rt, it, SEt, DEF | it | Pr2 |
| dAd | MAX display delay after defrost | 0 ÷ 255 min | 30 | Pr2 |
| Fdt | Draining time | 0 ÷ 120 min | 0 | Pr2 |
| dPo | First defrost after startup | n = after IdF; y = immed. | n | Pr2 |
| dAF | Defrost delay after fast freezing | 0 ÷ 23 h 50' | 0.0 | Pr2 |
| Fnc | Fan operating mode | C-n, o-n, C-y, o-Y | o-n | Pr1 |
| Fnd | Fan delay after defrost | 0 ÷ 255 min | 10 | Pr1 |
| Fct | Differential of temp. for forced fan activation | 0 ÷ 50 °C | 10 | Pr2 |
| FSt | Fan stop temperature | -50 ÷ 50 °C / -58 ÷ 122 °F | 2 | Pr1 |
| Fon | Fan on time with compressor off | 0 ÷ 15 min | 0 | Pr2 |
| FoF | Fan off time with compressor off | 0 ÷ 15 min | 0 | Pr2 |
| FAP | Probe selection for fan management | nP; P1; P2; P3; P4 | P2 | Pr2 |
| ALc | Temperature alarms configuration | rE = related to set; Ab = absolute | Ab | Pr2 |
| ALU | MAXIMUM temperature alarm | Set ÷ 110.0 °C; Set ÷ 230 °F | 110 | Pr1 |
| ALL | Minimum temperature alarm | -50.0 °C ÷ Set / -58 °F ÷ Set | -50.0 | Pr1 |
| AFH | Differential for temperature alarm recovery | 0.1 ÷ 25.5 °C / 1 ÷ 45 °F | 1 | Pr2 |
| ALd | Temperature alarm delay | 0 ÷ 255 min | 15 | Pr2 |
| dAO | Delay of temperature alarm at start up | 0 ÷ 23 h 50' | 1.3 | Pr2 |
| AP2 | Probe for temperature alarm of condenser | nP; P1; P2; P3; P4 | P4 | Pr2 |
| AL2 | Condenser low temperature alarm | -55 ÷ 150 °C / -67 ÷ 302 °F | -40 | Pr2 |
| AU2 | Condenser high temperature alarm | -55 ÷ 150 °C / -67 ÷ 302 °F | 110 | Pr2 |
| AH2 | Differential for condenser temp. alarm recovery | 0.1 ÷ 25.5 °C / 1 ÷ 45 °F | 5 | Pr2 |
| Ad2 | Condenser temperature alarm delay | 0 ÷ 254 min, 255 = nU | 15 | Pr2 |
| dA2 | Delay of condenser temperature alarm at start up | 0.0 ÷ 23 h 50' | 1.3 | Pr2 |
| bLL | Compressor off for condenser low temp. alarm | n(0) – Y(1) | n | Pr2 |
| AC2 | Compressor off for condenser high temp. alarm | n(0) – Y(1) | n | Pr2 |
| i1P | Digital input polarity | oP = opening; CL = closing | cL | Pr1 |
| i1F | Digital input configuration | EAL, bAL, PAL, dor, dEF, Htr, AUS | dor | Pr1 |
| did | Digital input alarm delay | 0 ÷ 255 min | 15 | Pr1 |
| nPS | Number of activations of pressure switch | 0 ÷ 15 | 15 | Pr2 |
| odc | Compressor and fan status with open door | no; Fan; CPr; F_C | F-c | Pr2 |
| rrd | Regulation restart with door open alarm | n – Y | y | Pr2 |
| HES | Differential for Energy Saving | -30 ÷ 30 °C / -54 ÷ 54 °F | 0 | Pr2 |
| PbC | Kind of probe | Ptc; ntc | ntc | Pr2 |
| Adr | Serial address | 1 ÷ 247 | 1 | Pr2 |
| onF | on/off key enabling | nu; oFF; ES | nu | Pr1 |
| dP1 | Room probe display | – | – | Pr2 |
| dP2 | Evaporator probe display | – | – | Pr1 |
| dP3 | Third probe display | – | – | Pr1 |
| dP4 | Fourth probe display | – | – | Pr1 |
| rSE | Actual set point | actual set | – | Pr2 |
| rEL | Software release | – | – | Pr2 |
| Ptb | Map code | – | – | Pr2 |

² Only for models XR60CX-xx2xx, XR60CX-xx3xx.

*Note fra konverteringen: Nederst i PDF'ens tabel er kolonnen med standardværdier forskudt én plads. Værdierne for PbC (ntc), Adr (1) og onF (nu) er derfor sat ud fra parametrenes gyldige værdier. Tjek på displayet ved tvivl.*
