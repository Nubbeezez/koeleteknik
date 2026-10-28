# Dixell XR75CX – Digital controller for medium-low temperature refrigeration applications – XR75CX

Kilde: `XR75CX-GB.pdf` i denne mappe. Konverteret direkte fra PDF'en. Tabeller (parametre, alarmer, standardværdier) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra tegninger står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilket afsnit svaret kommer fra.
- Alarm- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer (Dixell, Danfoss, Carel). Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualen, så sig det i stedet for at gætte.

---

#### **Digital controller for medium-low temperature refrigeration applications**

### **XR75CX**

##### **1. GENERAL WARNING**

##### **1.1 PLEASE READ BEFORE USING THIS MANUAL**

- This manual is part of the product and should be kept near the instrument for easy and quick reference.

- The instrument shall not be used for purposes different from those described hereunder. It cannot be used as a safety device.

- Check the application limits before proceeding.

- Dixell Srl reserves the right to change the composition of its products, even without notice, ensuring the same and unchanged functionality.

##### **1.2**<sup>**SAFETY PRECAUTIONS**</sup>

- Check the supply voltage is correct before connecting the instrument.

- Do not expose to water or moisture: use the controller only within the operating limits avoiding sudden temperature changes with high atmospheric humidity to prevent  formation of condensation

- Warning: disconnect all electrical connections before any kind of maintenance.

- Fit the probe where it is not accessible by the End User. The instrument must not be opened.

- In case of failure or faulty operation send the instrument back to the distributor or to “Dixell S.r.l.” (see address) with a detailed description of the fault.

- Consider the maximum current which can be applied to each relay (see Technical Data).

- Ensure that the wires for probes, loads and the power supply are separated and far enough from each other, without crossing or intertwining.

- In case of applications in industrial environments, the use of mains filters (our mod. FT1) in parallel with inductive loads could be useful.

##### **2. GENERAL DESCRIPTION**

Model **XR75CX** , format 32 x 74 mm, is microprocessor based controller, suitable for applications on medium or low temperature ventilated refrigerating units. It has 4 relay outputs to control compressor, fan, defrost, which can be either electrical or reverse cycle (hot gas) and light (configurable). It could be provided with a Real Time Clock which allows programming of up to 6 daily defrost cycles, divided into holidays and workdays. A “Day and Night” function with two different set points is fitted for energy saving. It is also provided with up to four NTC or PT1000 probe inputs, the first one for temperature control, the second one, to be located onto the evaporator, to control the defrost termination temperature and to managed the fan. One of the 2 digital inputs can operate as third temperature probe. The fourth probe is used to signal the condenser temperature alarm or to display a temperature.

The RS485 serial output allows to connect the unit to a network line **ModBUS-RTU** compatible such as the Dixell monitoring units of X-WEB family. The HOT key receptacle allows to program the controller by means the HOT KEY programming keyboard.

The instrument is fully configurable through special parameters that can be easily programmed through the keyboard.

##### **3. CONTROLLING LOADS**

##### **3.1 COMPRESSOR**

The regulation is performed according **Temper.** to the temperature measured by the thermostat probe with a positive **SET** differential from the set point: if the temperature increases and reaches set **Time** point plus differential the compressor is started and then turned off when the **Compr.** temperature reaches the set point value **ON** again.

In case of fault in the thermostat probe the start and stop of the compressor are timed through parameters “ **COn** ” and “ **COF** ”.

##### **3.2 DEFROST**

Two defrost modes are available through the “ **tdF** ” parameter: defrost through electrical heater ( **tdF = EL** ) and hot gas  defrost ( **tdF = in** ).

The defrost interval depends on the presence of the RTC (optional). If the RTC is present is controlled by means of parameter “ **EdF** ”:

- with EdF=in the defrost is made every “ **IdF** ” time – standard way for controller without RTC.

- - with EdF = “rtc”, the defrost is made in real time depending on the hours set in the parameters **Ld1..Ld6** on workdays and in **Sd1…Sd6** in holidays;

Other parameters are used to control defrost cycles: its maximum length (MdF) and two defrost modes: timed or controlled by the evaporator’s probe (P2P). At the end of defrost dripping time is started, its length is set in the Fdt parameter. With Fdt =0 the dripping time is disabled.

##### **3.3 CONTROL OF EVAPORATOR FANS**

The fan control mode is selected by means of the “ **FnC** ” parameter: **FnC = C_n:** fans will switch ON and OFF with the compressor and **not run** during defrost; **FnC = o_n** fans will run even if the compressor is off, and not run during defrost; After defrost, there is a timed fan delay allowing for drip time, set by means of the “ **Fnd** ” parameter. **FnC = C_Y** fans will switch ON and OFF with the compressor and **run** during defrost; **FnC = o_Y** fans will run continuously also during defrost

An additional parameter “ **FSt** ” provides the setting of temperature, detected by the evaporator probe, above which the fans are always OFF. This is used to make sure circulation of air only if his temperature is lower than set in “FSt”.

###### **3.3.1 Forced activation of fans**

This function managed by the **Fct** parameter is designed to avoid short cycles of fans, that could happen when the controller is switched on or after a defrost, when the room air warms the

evaporator. **Functioning:** if the difference of temperature between the evaporator and the room probes is more than the value of the Fct parameter, the fans are switched on. With Fct=0 the function is disabled.

###### **3.3.2 Cyclical activation of the fans with compressor off.**

When Fnc = c-n or c-Y (fans in parallel to the compressor), by means of the Fon and FoF parameters the fans can carry out on and off cycles even if the compressor is switched off. When the compressor is stopped the fans go on working for the Fon time. With Fon =0 the fans remain always off, when the compressor is off.

##### **3.4 LIGHT RELAY CONFIGURATION (PAR. OA3; TERM. 1-4)**

The functioning of the auxiliary relay (terminals. 1-4) can be set by the **oA3** parameter, according to the kind of application. In the following paragraph the possible setting:

###### **3.4.1 Light relay**

With oA3 = Lig the relay 1-4 operates as a light.

###### **3.4.2 Auxiliary relay – oA3 = AUS**

###### **a. Relay activation by digital input 2 (oA3 = AUS, i2F = AUS)**

With oA3 = AUS and i2F = AUS the relay 1-4 is switched on and off by digital.

###### **b. Auxiliary thermostat**

**I.E..** anti condensing heater) with the possibility of switching it on and off also by keyboard

###### **Parameters involved:**

- **ACH** Kind of regulation for the auxiliary relay: **Ht:** heating; **cL:** cooling **;**

- **SAA** Set point for auxiliary relay

- **SHy** Differential for auxiliary relay

- **ArP** Probe for auxiliary relay

- **Sdd** Auxiliary output off during defrost

By means of these 5 parameters the functioning of the auxiliary relay can be set.. The differential is given by the **SHy** parameter.

**NOTE:** Set **oA3 =AUS** and **ArP= nP** (no probe for auxiliary output).

In this case the relay 1-4 can be activated only by digital input with i1F or i2F = AUS.

###### **3.4.3 On/off  relay – oA3 = onF**

In this case the relay is activated when the controller is turned on and de-activated when the controller is turned off.

###### **3.4.4 Neutral zone regulation**

With **oA3 = db** the relay 1-4 can control a heater element to perform a neutral zone action. oA3 cut in = SET-HY oA3 cut out = SET

###### **3.4.5 Alarm relay**

With **oA3 = ALr** the relay 1-4 operates as alarm relay. It is activated every time an alarm happens. Its status depends on the **tbA** parameter: if “ **tbA = y** ”, the relay is silenced by pressing any key. If “ **tbA** = **n** ”, the alarm relay remains on until the alarm condition recovers.

###### **3.4.6 Night blind management during energy saving cycles**

With **oA3 = HES,** the relay 1-4 operates to manage the night blind: the relay is energised when the energy saving cycle is activated , by digital input, frontal button  or RTC (optional)

##### **4. FRONT PANEL COMMANDS**

- : To display target set point; in programming mode it  selects a parameter  or confirm an

- operation.

**(DEF)** To start a manual defrost

- ( **UP)** : To see the max. stored temperature; in programming mode it browses the parameter codes or increases the displayed value.

- ( **DOWN** ) To see the min stored temperature; in programming mode it browses the parameter codes or decreases the displayed value.

To switch the instrument off, if onF = oFF.

To switch the light, if oA3 = Lig.

###### **KEY COMBINATIONS:**

**+** To lock & unlock the keyboard **. +** To enter in programming mode. **+** To return to the room temperature display.

##### **4.1 USE OF LEDS**

Each LED function is described in the following table.

*[Figurtekst: LED  MODE  FUNCTION · ON  Compressor enabled · Flashing Anti-short cycle delay enabled · ON  Defrost enabled · Flashing Drip time in progress · ON  Fans enabled · Flashing Fans delay after defrost in progress. · ON  An alarm is occurring · ON  Continuous cycle is running · ON  Energy saving enabled · ON  Light on · ON  Auxiliary relay on · °C/°F  ON  Measurement unit · °C/°F  Flashing Programming phase]*

**5. MAX & MIN TEMPERATURE MEMORIZATION**

- **5.1 HOW TO SEE THE MIN TEMPERATURE**

1. Press and release the n key. 2. The “Lo” message will be displayed followed by the minimum temperature recorded. 3. By pressing the n key again or by waiting 5s the normal display will be restored.

- **5.2 HOW TO SEE THE MAX TEMPERATURE**

1. Press and release the o key.

2. The “Hi” message will be displayed followed by the maximum  temperature recorded.

3. By pressing the o key again or by waiting 5s the normal display will be restored.

- **5.3 HOW TO RESET THE MAX AND MIN TEMPERATURE RECORDED**

1. Hold press the SET key for more than 3s, while the max. or min temperature is displayed. (rSt message will be displayed)

2. To confirm the operation the “rSt” message starts blinking and the normal temperature will be displayed.

**6. MAIN FUNCTIONS**

- **6.1 TO SET THE CURRENT TIME AND DAY (ONLY FOR INSTRUMENTS WITH RTC)**

- When the instrument is switched on, it’s necessary to program the time and day. 1. Enter the Pr1 programming menu, by pushing the SET + n keys for 3s. 2. The rtc parameter is displayed. Push the SET key to enter the real time clock menu. 3. The Hur (hour) parameter is displayed. 4. Push the SET and set current hour by the UP and Down keys, then push SET to confirm the value..

- 5. Repeat the  same operations on the Min (minutes) and dAy (day) parameters.

- **To exit:** Push SET+UP keys or wait for 15 sec without pushing any keys.

##### **6.2 HOW TO SEE THE SET POINT**

*[Figurtekst: 1. Push and immediately release the  SET  key: the display will show the · Set point value; · 2. Push and immediately release the  SET  key or wait for 5 seconds to]*

*[Figurtekst: display the probe value again.]*

- **6.3 HOW TO CHANGE THE SET POINT**

1. Push the **SET** key for more than 2 seconds to change the Set point value; 2. The value of the set point will be displayed and the “ **°C” or “°F”** LED starts blinking; 3. To change the Set value push the o or n arrows within 10s. 4. To memorise the new set point value push the **SET** key again or wait 10s.

- **6.4 HOW TO START A MANUAL DEFROST**

*[Figurtekst: Push the  DEF  key for more than 2 seconds and a manual defrost will start.]*

##### **6.5 HOW TO CHANGE A PARAMETER VALUE**

To change the parameter’s value operate as follows:

1. Enter the Programming mode by pressing the **Set** + n keys for 3s (the “ **°C” or “°F”** LED starts blinking).

2. Select the required parameter. Press the “ **SET** ” key to display its value

3. Use “ **UP** ” or “ **DOWN** ” to change its value.

4. Press “ **SET** ” to store the new value and move to the following parameter. **To exit** : Press **SET + UP** or wait 15s without pressing a key. **NOTE** : the set value is stored even when the procedure is exited by waiting the time-out to expire.

##### **6.6 THE HIDDEN MENU**

The hidden menu Includes all the parameters of the instrument.

###### **6.6.1 HOW TO ENTER THE HIDDEN MENU**

1. Enter the Programming mode by pressing the **Set** + n keys for 3s (the “ **°C” or “°F”** LED starts blinking).

2. Released the keys, then push again the Set+ n keys for more than 7s. The Pr2 label will be displayed immediately followed from the HY parameter.

**NOW YOU ARE IN THE HIDDEN MENU.**

3. Select the required parameter.

4. Press the “ **SET** ” key to display its value

5. Use o or n to change its value.

6. Press “ **SET** ” to store the new value and move to the following parameter. **To exit** : Press **SET +** o or wait 15s without pressing a key.

**NOTE1:** if none parameter is present in Pr1, after 3s the “noP” message is displayed. Keep the keys pushed till the Pr2 message is displayed.

**NOTE2** : the set value is stored even when the procedure is exited by waiting the time-out to expire. **6.6.2 HOW TO MOVE A PARAMETER FROM THE HIDDEN MENU TO THE FIRST LEVEL AND VICEVERSA.**

Each parameter present in the HIDDEN MENU can be removed or put into “THE FIRST LEVEL” (user level) by pressing **“SET +** n **”** .

In HIDDEN MENU when a parameter is present in First Level the decimal point is on.

##### **6.7 HOW TO LOCK THE KEYBOARD**

1. Keep pressed for more than 3 s the **UP** + **DOWN** keys.

2. The “POF” message will be displayed and the keyboard will be locked. At this point it will be possible only to see the set point or the MAX o Min temperature stored

3. If a key is pressed more than 3s the “POF” message will be displayed.

##### **6.8 TO UNLOCK THE KEYBOARD**

Keep pressed together for more than 3s the o and n keys, till the **“Pon”** message will be displayed.

##### **6.9 THE CONTINUOUS CYCLE**

When defrost is not in progress, it can be activated by holding the “ o ” key pressed for about 3 seconds. The compressor operates to maintain the “ **ccS** ” set point for the time set through the “ **CCt** ” parameter. The cycle can be terminated before the end of the set time using the same activation key “ o ” for 3 seconds.

##### **6.10 THE ON/OFF FUNCTION**

With “ **onF = oFF** ”, pushing the **ON/OFF** key, the instrument is switched off. The **“OFF”** message is displayed. In this configuration, the regulation is disabled. To switch the instrument on, push again the ON/OFF key.

**WARNING: Loads connected to the normally closed contacts of the relays are always supplied and under voltage, even if the instrument is in stand by mode.**

##### **7. PARAMETERS**

**rtc Real time clock menu (only for controller with RTC):** to set the time and date and defrost start time. **REGULATION Hy Differential** : (0,1 ÷ 25,5°C / 1÷255 °F) Intervention differential for set point. Compressor Cut IN is Set Point + differential (Hy). Compressor Cut OUT is when the temperature reaches the set point. **LS  Minimum set point:** (- 100°C÷SET/-148°F÷SET): Sets the minimum value for the set point. **US Maximum set point:** (SET÷110°C/ SET÷230°F). Set the maximum value for set point. **Ot  Thermostat probe calibration** : (-12.0÷12.0°C; -120÷120°F) allows to adjust possible offset of the thermostat probe. **P2P Evaporator probe presence: n** = not present: the defrost stops by time; **y=** present: the defrost stops by temperature. **OE Evaporator probe calibration:** (-12.0÷12.0°C; -120÷120°F). allows to adjust possible offset of the evaporator probe. **P3P Third probe presence (P3): n** = not present:, the terminals 18-20 operate as digital input.; **y=** present:, the terminals 18-20  operate as third probe. **O3 Third probe calibration  (P3):** (-12.0÷12.0°C; -120÷120°F). allows to adjust possible offset of the third probe. **P4P Fourth probe presence** : (n = Not present; y = present). **o4 Fourth probe calibration** : (-12.012.0°C) allows to adjust possible offset of the fourth probe. **OdS Outputs activation delay at start up:** (0÷255min) This function is enabled at the initial start up of the instrument and inhibits any output activation for the period of time set in the parameter. **AC  Anti-short cycle delay** : (0÷50 min) minimum interval between the compressor stop and the following restart. **rtr Percentage of the second and first probe for regulation (0÷100; 100 = P1, 0 = P2 ):** it allows to set the regulation according to the percentage of the first and second probe, as for the following formula (rtr(P1-P2)/100 + P2). **CCt Compressor ON time during continuous  cycle:** (0.0÷24.0h; res. 10min) Allows to set the length of the continuous cycle: compressor stays on without interruption for the CCt time. Can be used, for instance, when the room is filled with new products. **CCS Set point for continuous cycle:** (-100÷150°C) it sets the set point used during the continuous cycle. **COn Compressor ON time with faulty probe:** (0÷255 min) time during which the compressor is active in case of faulty thermostat probe. With COn=0 compressor is always OFF. **COF Compressor OFF time with faulty probe:** (0÷255 min) time during which the compressor is OFF in case of faulty thermostat probe. With COF=0 compressor is always active. **DISPLAY CF Temperature measurement unit: °C=** Celsius; **°F** =Fahrenheit. WARNING: When the measurement unit is changed the SET point and the values  of the parameters Hy, LS, US, Ot, ALU and ALL have to be checked and modified if necessary). **rES Resolution (for °C)** : (in = 1°C; dE = 0.1 °C) allows decimal point display. **Lod Instrument display** : (P1; P2, P3, P4,  SET, dtr): it selects which probe is displayed by the instrument: **P1** = Thermostat probe; **P2** = Evaporator probe; **P3** = Third probe(only for model with this option enabled); **P4** = Fourth probe, **SET** = set point; **dtr** = percentage of visualization. **rEd X- REP display (** **_optional_ )** : (P1; P2, P3, P4,  SET, dtr): it selects which probe is displayed by X- REP: **P1** = Thermostat probe; **P2** = Evaporator probe; **P3** = Third probe(only for model with this option enabled); **P4** = Fourth probe, **SET** = set point; **dtr** = percentage of visualization. **dLy Display delay:** (0 ÷20.0m; resul. 10s) when the temperature increases, the display is updated of 1 °C/1°F after this time.

|**dtr**|**Percentage of the second and first probe for visualization when Lod = dtr (0÷100; 100 =**<br>**P1, 0 = P2 ): if Lod = dtr**it allows to set the visualization according to the percentage of the<br>first and secondprobe,as for the followingformula(dtr(P1-P2)/100 + P2).|
|---|---|
|**DEF**|**ROST**|
|**EdF**|**Defrost mode (only for controller with RTC):**<br>**rtc**=**Real Time Clock mode**. Defrost time follows**Ld1÷Ld6**parameters on workdays and<br>**Sd1÷Sd6**on holidays.<br> “”|
|**tdF**|**in**=**interval mode**. The defrost starts when the time**Idf**is expired.<br>**Defrost type**: EL = electrical heater; in = hot gas|
|<br>**dFP**|<br>**Probe selection for defrost termination: nP**= no probe;**P1**=thermostat probe;**P2 =**<br>evaporator probe;**P3**=configurable probe;**P4**= Probe on Hot Key plug.|
|**dtE**|**Defrost termination temperature**: (-50÷50 °C/<br>-58÷122°F) (Enabled only when EdF=Pb) sets the temperature measured by the evaporator<br>probe which causes the end of defrost.|
|**IdF**|,<br>**Interval between defrost cycles**: (0÷120h) Determines the time interval between the<br>|
|**MdF**|beginning of two defrost cycles.<br>**(Maximum) length for defrost**: (0÷255min) When**P2P = n**, (not evaporator probe: timed<br>defrost) it sets the defrost duration, when**P2P = y**(defrost end based on temperature) it sets<br>the maximum lenth for defrost|
|**dSd**|g  .<br>**Start defrost delay**: ( 0÷99min) This is useful when different defrost start times are necessary<br>|
|**dFd**|to avoid overloading the plant.<br>**Temperature displayed during defrost**: (**rt**= real temperature;**it**= temperature at defrost<br>tt**SEt**= t it**dEF**= “dEF” lbl|
|**dAd**|sar;se pon;ae)<br>**MAX display delay after defrost**: (0÷255min). Sets the maximum time between the end of<br>|
|**Fdt**|defrost and the restarting of the real room temperature display.<br>**Drip time**: (0120 min) time interval between reaching defrost termination temperature and the<br>restoring of the control’s normal operation. This time allows the evaporator to eliminate water<br>drops that might have formed due to defrost|
|**dPo**<br>**dAF**|.<br>**First defrost after start-up**: (y = immediately; n = after the IdF time)<br>**Defrost delay after continuous cycle**: (023.5h) time interval between the end of the fast<br>freezinccle and the followindefrost related to it|
|**FAN**|g y g.<br>**S**|
|**FnC**|**Fans operating mode**:**C-n**= runs with the compressor, OFF during defrost;<br>**o-n**= continuous mode, OFF during defrost;|
||**C-Y**= runs with the compressor, ON during defrost;<br>**o-Y**= continuous mode ON during defrost;|
|**Fnd**|,<br>**Fans delay after defrost:**(0÷255min) Interval between end of defrost and evaporator fans<br>|
|**Fct**|start.<br>**Temperature differential avoiding short cycles of fans**(0÷59°C; Fct=0 function disabled). If<br>the difference of temperature between the evaporator and the room probes is more than the<br>l f th Ft t th f  ithd|
|**FSt**|vaue o e c parameer, e ans are swce on.<br>**Fans stop temperature**: (-50÷50°C/122°F) setting of temperature, detected by evaporator<br>|
|**Fon**|probe, above which fans are always OFF.<br>**Fan ON time:**(0÷15 min)**with**Fnc = C_n or C_y, (fan activated in parallel with compressor). it<br>sets the evaporator fan ON cycling time when the compressor is off. With Fon =0 and FoF ≠ 0<br>|
|**FoF**|the fan are always off, with Fon=0 and FoF =0 the fan are always off.<br>**Fan OFF time:**(0÷15 min)**with**Fnc = C_n or C_y, (fan activated in parallel with compressor). it<br>sets the evaporator fan off cycling time when the compressor is off. With Fon =0 and FoF ≠ 0|
|**FAP**|the fan are always off, with Fon=0 and FoF =0 the fan are always off.<br>**Probe selection for fan management: nP**= no probe;**P1**=thermostat probe;**P2 =**evaporator<br>probe; **P3**=configurableprobe; **P4**= Probe on Hot Key plug.|
|**AUX**|**ILIARY THERMOSTAT CONFIGURATION(terms 1-4) – OA3 = AUS**|
|<br>**ACH**<br>**SAA**|**.**<br>**Kind of regulation for auxiliary relay**:**Ht**= heating;**CL**= cooling<br>**Set Point for auxiliary relay:**(-100÷150°C; -148÷302°F) it defines the room temperature set<br>|
|**SHy**|point  to switch auxiliary relay.<br>**Differential for auxiliary output:**(0,1 ÷ 25,5°C / 1÷255 °F) Intervention differential for<br>|
||auxiliary output set point.<br>**With ACH = cL**AUX Cut in is SAA + SHy; . AUX Cut  out is SAA<br>**With ACH = Ht**AUX Cut in is SAA - SHy; . AUX Cut out  is SAA|
|**ArP**|<br>**Probe selection for auxiliary**: nP = no probe, the auxiliary relay is switched only by the digital|
||<br>input;**P1 =**Probe 1 (Thermostat probe);**P2 =**Probe 2 (evaporator probe);**P3 =**Probe 3|
|**Sdd**|<br>(display probe);**P4 =**Probe 4.<br>**Auxiliary relay off during defrost: n =**the auxiliary relay operates during defrost|
|<br>|.<br>**y =**the auxiliaryrelayis switched off duringdefrost.<br>|
|**ALA**<br>**ALP**|**RMS**<br>**Probe selection for alarm**: nP = no probe, the temperature alarms are disabled;**P1 =**Probe 1<br>(Thermostat probe);**P2 =**Probe 2 (evaporator probe);**P3 =**Probe 3 (display probe);**P4 =**<br>Fourth probe.|
|**ALC**|<br>**Temperature alarms configuration:**(Ab; rE)|
||<br>**Ab**= absolute temperature: alarm temperature is given by the ALL or ALU values.**rE**=<br>temperature alarms are referred to the set point. Temperature alarm is enabled when the<br>temperature exceeds the “SET+ALU” or “SET-ALL” values|
|**ALU**|.<br>**MAXIMUM temperature alarm**: (SET÷150°C; SET÷302°F) when this temperature is reached<br>f  “”|
|**ALL**|the alarm is enabled, ater the ALd delay time.<br>**Minimum temperature alarm**: (-100 ÷ SET °C; -148÷230°F when this temperature is reached<br>“”|
||the alarm is enabled, after the ALd delay time.<br> ° °|
|**AFH**|**Differential for temperature alarm/ fan recovery:**(0,1÷25,5C; 1÷45F) Intervention<br>differential for recovery of temperature alarm. It’s also used for the restart of the fan when the<br>|
|**ALd**|FSt temperature is reached<br>**Temperature alarm delay**: (0÷255 min) time interval between the detection of an alarm|
|**dAO**|condition and alarm signalling.<br>**Exclusion of temperature alarm at start-up**: (from 0.0 min to 23.5h) time interval between the|
|**CON**|detection of the temperature alarm condition after instrumentpower on and alarm signalling.<br>**DENSER TEMPERATURE ALARM**|
|<br>**AP2**|<br>**Probe selection for temperature alarm of condenser: nP**= no probe;**P1**=thermostat probe;<br>|
||**P2 =**evaporator probe;**P3**=configurable probe;**P4**= Probe on Hot Key plug.<br>|
|**AL2**|**Low temperature alarm of condenser**: (-100÷150°C) when this temperature is reached the<br>|
|**Au2**|LA2 alarm is signalled, possibly after the Ad2 delay.<br>**High temperature alarm of condenser**: (-100÷150°C) when this temperature is reached the|
|**AH2**|HA2 alarm is signalled, possibly after the Ad2 delay.<br>**Differential for temperature condenser alarm recovery**: (0,1÷25,5°C; 1÷45°F)|

|**Ad2**|**Condenser temperature alarm delay**: (0÷255 min) time interval between the detection of the<br>condenser alarm condition and alarm signalling.|
|---|---|
|**dA2**<br>**bLL**|<br>**Condenser temperature alarm exclusion at start up**: (from 0.0 min to 23.5h, res. 10min)<br>**Compressor off with low temperature alarm of condenser**:**n = no:**compressor keeps on<br>working**; Y = yes,**compressor is switched off till the alarm is present, in any case regulation<br>restarts after AC time at minimum|
|**AC2**|.<br>**Compressor off with high temperature alarm of condenser**:**n = no:**compressor keeps on<br>working**; Y = yes,**compressor is switched off till the alarm is present, in any case regulation<br>restarts after AC time at minimum.|
|**AUXI**|**LIARY RELAY**|
|**tbA**<br>**oA3**|**Alarm relay silencing (with oA3 =ALr):**<br>**n**= silencing disabled: alarm relay stays on till alarm condition lasts,<br>**y**=silencing enabled: alarm relay is switched OFF by pressing a key during an alarm<br>**Fourth relay configuration (1-4):** **dEF, FAn:**do not select it!.**ALr**: alarm;**Lig**: light;**AuS**:<br>Auxiliary relay;**onF**: always on with instrument on;**db=**neutral zone;**cP2 =**do not select it!;<br>|
|**AoP**|**dEF2:**do not select it!;.**HES:**. night blind<br>**Alarm relay polarity:**it set if the alarm relay is open or closed when an alarm happens.**CL**=<br>terminals 1-4 closed duringan alarm; **oP**= terminals 1-4 open duringan alarm|
|**DIGI**|**TAL INPUTS**|
|<br>**i1P**|<br>**Digital input polarity (18-20): oP:**the digital input is activated by opening the contact;**CL:**the<br>|
|**i1F**|digital input is activated by closing the contact.<br>**Digital input configuration (18-20):** **dor**= door switch function;**dEF**= activation of a defrost<br>|
|**i2P**|cycle;<br>**2**<sup>**nd**</sup>**digital input polarity (18-19): oP:**the digital input is activated by opening the contact;**CL:**<br>the digital input is activated by closing the contact|
|**i2F**|.<br>**2**<sup>**nd**</sup>**digital input configuration (18-19): EAL**= external alarm: “EA” message is displayed;<br>**bAL**= serious alarm “CA” message is displayed.**PAL**= pressure switch alarm, “CA” message is<br>displayed;**dor**= door switch function;**dEF**= activation of a defrost cycle;**ES**= energy saving;<br>**AUS**=auxiliary relay activation with 0A3 = AUS;**Htr**= kind of action inversion (cooling –<br>heating);**FAn**= fan;**HdF**= Holiday defrost (enable only with RTC);**onF =**to switch the<br>|
|**did**(|controller off.<br>0255 min)**with** **i2F= EAL or i2F = bAL digital input alarm delay (18-20):**delay between the<br>detection of the external alarm condition and its signalling.<br>**with i2F= PAL: time for pressure switch function:**time interval to calculate the number of<br>the pressure switch activation.|
|**doA**<br>**nPS**|<br>**Door open signalling delay**(0255 min):<br>**Prr ith nmbr**015 Nmbr f titin f th rr ith drin th “**did**”|
||**essue swc ue:**() ue o acvao o e pessue swc, ug e <br>interval, before signalling the alarm event (I2F= PAL).<br>**If the nPS activation in the did time is reached, switch off and on the instrument to**<br>|
|**odc**|**restart normal regulation.**<br>**Compressor and fan status when open door:** **no**= normal;**Fan**= Fan OFF;**CPr**=<br>Compressor OFF;**F_C**= Compressor and fan OFF.|
|**rrd**|**Outputs restart after doA alarm: no=**outputs not affected by the doA alarm;**yES =**outputs|
|**HES**|restart with the doA alarm.<br>**Temperature increase during the Energy Saving cycle:**<br>(-300°C300°C)it sets the increasingvalue of the setpoint duringthe EnergySavingcycle|
|**TO S**<br>**Hur**|,,      .<br>**ET CURRENT TIME AND WEEKLY HOLIDAYS(ONLY FOR MODELS WITH RTC)**<br>**Current hour**(0 ÷ 23 h)|
|**Min**|**Current minute**(0 ÷ 59min)|
|**dAY**<br>**Hd1**|<br> <br>**Current day**(Sun ÷ SAt)<br>**First weekly holiday**(Sun ÷ nu) Set the first day of the week which follows the holiday<br>ti|
|**Hd2**|mes.<br>**Second weekly holiday**(Sun ÷ nu) Set the second day of the week which follows the<br>hli i|
|**N.B.**|oday tmes.<br> <br>**Hd1,Hd2**can be set also as**“nu”**value(Not Used).|
|**TO S**|**ET ENERGY SAVING TIMES(ONLY FOR MODELS WITH RTC)**|
|**ILE**|**Energy Saving cycle start during workdays**: (0 ÷ 23h 50 min.) During the Energy Saving<br>cycle the set point is increased by the value in HES so that the operation set point is SET +<br>|
||HES.<br>|
|**dLE**|**Energy Saving cycle length during workdays**: (0 ÷ 24h 00 min.) Sets the duration of the<br>|
|**ISE**<br>**dSE**|Energy Saving cycle on workdays.<br>**Energy Saving cycle start on holidays**. (0 ÷ 23h 50 min.)<br>**Energy Saving cycle length on holidays** (0 ÷ 24h 00 min.)|
|**TO S**<br>**Ld1÷**|**ET DEFROST TIMES(ONLY FOR MODELS WITH RTC)**<br>**Ld6 Workday defrost start**(0 ÷ 23h 50 min.) These parameters set the beginning of the 6<br>programmable defrost cycles during workdays. Ex. When**Ld2**= 12.4 the second defrost starts<br>|
|**Sd1÷**|at 12.40 during workdays.<br>**Sd6 Holiday defrost start**(0 ÷ 23h 50 min.) These parameters set the beginning of the 6|
||programmable defrost cycles on holidays. Ex. When**Sd2**= 3.4 the second defrost starts at|
||3.40 on holidays.<br>**N.B. :To disable a defrost cycle set it to“nu”(not used).****_Ex._**_If_**_Ld6_**_=nu_**_;_**_the sixth defrost_<br>_cycle is disabled_|
|**OTH**|<br>**ER**|
|**Adr**|**Serial address**(1÷244): Identifies the instrument address when connected to a ModBUS|
|**PbC**|compatible monitoring system.<br>**Type of probe:**it allows to set the kind of probe used by the instrument:**Pt1**= Pt1000 probe,<br>**ntc =**NTC probe.|
|**onF**|<br>**on/off key enabling: nu =**disabled;**oFF =**enabled;**ES = not set it**|
|<br>**dP1**<br>**dP2**|.<br>**Thermostat probe display**<br>**Ertr rb dil**|
|<br>**P**|**vapoao poe spay**<br>**Thi  il****_il_**|
|**d3**<br>**dP4**<br>|**rd probe dspay**-**_optona_**.<br>**Fourth probe display**.<br>|
|**rSE**|**Real set point:**it shows the set point used during the energy saving cycle or during the<br>|
|**rEL**<br>**Ptb**|continuous cycle.<br>**Software release**for internal use**.**<br>**Parameter table code:**readable only**.**|
|**8. **|**DIGITAL INPUTS**|

The first digital input 18-20 is enabled  with P3P = n. With P3P = n and i1F = i2F the second digital input is disabled The free voltage digital inputs are programmable by the “ **i1F** ” and i2F  parameters.

##### **8.1 GENERIC ALARM (i2F = EAL)**

As soon as the digital input is activated the unit will wait for “ **did** ” time delay before signalling the “ **EAL** ” alarm message. The outputs status don’t change. The alarm stops just after the digital input is de-activated.

##### **8.2 SERIOUS ALARM MODE (i2F =  bAL)**

When the digital input is activated, the unit will wait for “ **did** ” delay before signalling the “ **CA** ” alarm message. The relay outputs are switched OFF. The alarm will stop as soon as the digital input is deactivated.

##### **8.3 PRESSURE SWITCH (i2F = PAL)**

If during the interval time set by “ **did** ” parameter, the pressure switch has reached the number of activation of  the “ **nPS** ” parameter, the “ **CA** ” pressure alarm message will be displayed. The compressor and the regulation are stopped. When the digital input is ON the compressor is always OFF. **If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation.**

##### **8.4 DOOR SWITCH INPUT  (i1F or i2F = dor)**

It signals the door status and the corresponding relay output status through the “ **odc** ” parameter: **no** = normal (any change); **Fan** = Fan OFF; **CPr** = Compressor OFF; **F_C** = Compressor and fan OFF. Since the door is opened, after the delay time set through parameter “ **doA** ”, the door alarm is enabled, the display shows the message “ **dA** ” and **the regulation restarts is rtr = yES.** The alarm stops as soon as the external digital input is disabled again. With the door open, the high and low temperature alarms are disabled.

- **8.5 START DEFROST (i1F or i2F = dEF)**

It starts a defrost if there are the right conditions. After the defrost is finished, the normal regulation will restart only if the digital input is disabled otherwise the instrument will wait until the “MdF” safety time is expired.

- **8.6 SWITCH THE AUXILIARY RELAY (i2F = AUS)**

With oA3 = AUS the digital input switched the status of the auxiliary relay

- **8.7 INVERSION OF  THE KIND OF ACTION: HEATING-COOLING (i2F=Htr)**

This function allows to invert the regulation of the controller: from cooling to heating and viceversa.

- **8.8 ENERGY SAVING (i2F = ES)**

The Energy Saving function allows to change the set point value as the result of the SET+ HES (parameter) sum. This function is enabled until the digital input is activated.

- **8.9 HOLIDAY DEFROST (i2F = HDF) –ONLY FOR MODELS WITH RTC**

This function enabled the holiday defrost setting.

- **8.10 ON OFF FUNCTION (i2F = onF)**

To switch the controller on and off.

- **8.11 DIGITAL INPUTS POLARITY**

The digital input polarity depends on the “ **i1P** ” and **“i2P”** parameters. **i1P or i2P =CL** : the input is activated by closing the contact.

**i1P or i2P=OP** : the input is activated by opening the contact

**9. RS485 SERIAL LINE – FOR MONITORING SYSTEMS**

The RS485 serial line,  allows to connect the instrument to a monitoring system **ModBUS-RTU** compatible  such as the  X-WEB500/3000/300.

##### **10. X-REP OUTPUT – OPTIONAL**

As optional, an X-REP can be connected to the instrument, trough the dedicated

connector.

To connect the X-REP to the instrument the following connectors must be used CAB-51F(1m), CAB52F(2m), CAB-55F(5m),

##### **11. INSTALLATION AND MOUNTING**

Instrument **XR75CX** shall be mounted on vertical panel, in a 29x71 mm hole, and fixed using the special bracket supplied. The temperature range allowed for correct operation is 060 °C. Avoid places subject to strong vibrations, corrosive gases, excessive dirt or humidity. The same recommendations apply to probes. Let air circulate by the cooling holes.

##### **12. ELECTRICAL CONNECTIONS**

The instrument is provided with screw terminal block to connect cables with a cross section up to 2,5 mm<sup>2</sup> . Before connecting cables make sure the power supply complies with the instrument’s requirements. Separate the probe cables from the power supply cables, from the outputs and the power connections. Do not exceed the maximum current allowed on each relay, in case of heavier loads use a suitable external relay.

##### **12.1 PROBE CONNECTION**

The probes shall be mounted with the bulb upwards to prevent damages due to casual liquid infiltration. It is recommended to place the thermostat probe away from air streams to correctly measure the average room temperature. Place the defrost termination probe among the evaporator fins in the coldest place, where most ice is formed, far from heaters or from the warmest place during defrost, to prevent premature defrost termination.

**13. HOW TO USE THE HOT KEY**

- **13.1 HOW TO PROGRAM A HOT KEY FROM THE INSTRUMENT (UPLOAD)**

1. Program one controller with the front keypad.

2. When the controller is <u>ON, insert the “</u> **Hot key** ” and push o key; the **"uPL"** message appears followed a by flashing **“End”**

3. Push “ **SET”** key and the **End** will stop flashing.

4. <u>Turn OFF the instrument remove the</u> **“Hot Key”,** then turn it ON again.

**NOTE** : the “ **Err** ” message is displayed for failed programming. In this case push again o key if you want to restart the upload again or remove the “ **Hot key** ” to abort the operation.

##### **13.2 HOW TO PROGRAM AN INSTRUMENT USING A HOT KEY**

##### **<u>(DOWNLOAD)</u>**

1. Turn OFF the instrument.

2. Insert  a **programmed “Hot Key” into the 5 PIN receptacle** and then turn the Controller ON. 3. Automatically the parameter list of the **“Hot Key”** is downloaded into the Controller memory, the “ **doL** ” message is blinking followed a by flashing **“End”.**

4. After 10 seconds the instrument will restart working with the new parameters.

5. Remove the **“Hot Key”.** .

**NOTE** the message “ **Err** ” is displayed for failed programming. In this case turn the unit off and then on if you want to restart the download again or remove the “ **Hot key** ” to abort the operation.

##### **14. ALARM SIGNALS**

|**Message**|**Cause**|**Outputs**|
|---|---|---|
|“P1”|Roomprobe  failure|Compressor output acc. topar. “Con” and “COF”|
|“P2”|Evaporatorprobe  failure|Defrost end is timed|
|“P3”|Thirdprobe  failure|Outputs unchanged|
|“P4”|Fourthprobe  failure|Outputs unchanged|
|“HA”|Maximum temperature alarm|Outputs unchanged.|
|“LA”|Minimum temperature alarm|Outputs unchanged.|
|"HA2"|Condenser high temperature|It depends on the “Ac2”parameter|
|"LA2"|Condenser low temperature|It depends on the “bLL”parameter|
|“dA”|Door open|Compressor and fans restarts|
|“EA”|External alarm|Output unchanged.|
|“CA”|Serious external alarm(i1F=bAL)|All outputs OFF.|
|“CA”|Pressure switch alarm(i1F=PAL)|All outputs OFF|
|“rtc”|Real time clock alarm|Alarm output ON; Other outputs unchanged;<br>Defrosts according to par. “IdF” Set real time clock<br>has to be set|
|rtF|Real time clock board failure|Alarm output ON; Other outputs unchanged;<br>Defrosts according to par. “IdF” Contact the<br>service|

##### **14.1 SILENCING BUZZER / ALARM RELAY OUTPUT**

If “ **tbA = y** ”, the buzzer and the relay are is silenced by pressing any key.

If “ **tbA** = **n** ”, only the buzzer is silenced while the alarm relay is on until the alarm condition recovers.

##### **14.2 ALARM RECOVERY**

Probe alarms **P1** ”, “ **P2”,** “ **P3** ” and “ **P4** ” start some seconds after the fault in the related probe; they automatically stop some seconds after the probe restarts normal operation. Check connections before replacing the probe.

Temperature alarms “ **HA** ”, “ **LA** ” “ **HA2** ” and “ **LA2** ” automatically stop as soon as the temperature

returns to normal values.

Alarms **“EA”** and **“CA”** (with i1F=bAL) recover as soon as the digital input is disabled.

Alarm “ **CA”** (with i1F=PAL) recovers only by **switching off and on** the instrument.

|**14.3 **|**OTHER MESSAGES**|
|---|---|
|**Pon**|Keyboard unlocked.|
|**PoF**|Keyboard locked|
|**noP**|**In programming mode**: none parameter is present in Pr1|
||**On the display**or in dP2,dP3,dP4: the selectedprobe is nor enabled|

##### **15. TECHNICAL DATA**

**Housing:** self extinguishing ABS. **Case:** frontal 32x74 mm; depth 60mm; **Mounting:** panel mounting in a 71x29mm panel cut-out **Protection:** IP20; **Frontal protection:** IP65

**Connections:** Screw terminal block  2,5 mm<sup>2</sup> wiring.

**Power supply:** according to the model 24Vac, ±10%;  230Vac 10%, 50/60Hz, 110Vac 10%, 50/60Hz

**Power absorption:** 3VA max

**Display** : 3 digits, red LED, 14,2 mm high; **Inputs** : Up to 4 NTC or PT1000 probes. **Digital inputs:** free voltage contact **Relay outputs: compressor** SPST 8(3) A, 250Vac or  SPST 16A 250Vac **defrost:** SPDT 8(3) A, 250Vac **fan:** SPST 5A, 250Vac **aux:** SPDT 8(3) A, 250Vac or SPST 16(6)A 250Vac **Data storing** : on the non-volatile memory (EEPROM). **Internal clock back-up:** 24 hours

**Kind of action:** 1B; **Pollution grade:** 2; **Software class:** A.; **Rated impulsive voltage** : 2500V; **Overvoltage Category** : II **Operating temperature:** 0÷55°C; **Storage temperature:** -30÷85 °C.

**Relative humidity:** 2085% (no condensing)

**Measuring and regulation range: NTC probe:** -40÷110°C (-40÷230°F);

**PT1000 probe:** -100÷150°C (-148÷302°F)

**Resolution:** 0,1 °C or 1°C or 1 °F (selectable); **Accuracy (ambient temp. 25°C)** :  ±0,7 °C ±1 digit

##### **16. CONNECTIONS**

**Supply: 120Vac or 24Vac:** connect to terminals 5-6. **The X-REP output** is optional

##### **17. DEFAULT SETTING VALUES**

|**Label **<br>**Name**<br>**Set**Setoint|**Range**<br>LS÷US|**Value**<br>-50|**Level **<br>- - -|
|---|---|---|---|
|p<br>**rtc***Realtime clock menu|-|.<br>-|<br>Pr1|
|**Hy **Differential|0,125.5°C/1255°F|2.0|Pr1|
|**LS**Minimum setpoint|-100CSET/-58°FSET|-50.0|Pr2|
|**US**Maximum setpoint|SET110°C/ SET230°F|110|Pr2|
|**Ot**Thermostatprobe calibration|-1212°C /-120120°F|0.0|Pr1|
|**P2P**Evaporatorprobe presence|n=not present;Y=pres.|Y|Pr1|
|**OE**Evaporatorprobe calibration|-1212°C /-120120°F|0.0|Pr2|
|**P3P**Third probe presence|n=not present;Y=pres.|n|Pr2|
|**O3**Thirdprobe calibration|-1212°C /-120120°F|0|Pr2|
|**P4P**Fourthprobe presence|n=not present;Y=pres.|n|Pr2|
|**O4**Fourthprobe calibration|-1212°C /-120120°F|0|Pr2|
|**OdS**Outputsdelayatstartup|0÷255min|0|Pr2|
|<br>**AC**Anti-short cycle delay|<br>0  50min|1|<br>Pr1|
|**rtr**P1-P2percentagefor regulation|0÷ 100 (100=P1, 0=P2)|100|Pr2|
|**CCt**Continuous cycle duration|0.0÷24.0h|0.0|Pr2|
|**CCS**Set pointforcontinuous cycle|(-100÷150,0°C) (-67÷302°F)|-5|Pr2|
|**COn**Compressor ON time with faulty probe|0 255min|15|Pr2|
|**COF**Compressor OFF time with faulty probe|0 255min|30|Pr2|
|**CF**Temperature measurement unit|°C °F|°C|Pr2|
|**rES**Resolution|in=integer; dE=dec.point|dE|Pr1|
|**Lod**Probe displayed|P1;P2|P1|Pr2|
|**rEd**<sup>**2**</sup>X-REPdisplay|P1 – P2 – P3– P4 –SEt–dtr|P1|Pr2|
|**dLy **Display temperature delay|0÷ 20.0min(10 sec.)|0.0|Pr2|
|**dtr **P1-P2percentagefordisplay|1 ÷99|50|Pr2|
|**EdF***Kind of interval fordefrost|rtc÷in|rtc|Pr2|
|**tdF**Defrost type|EL=el. heater;in= hot gas|EL|Pr1|
|**dFP**Probe selection fordefrost termination<br>|nP;P1;P2;P3;P4<br>°|P2<br>|Pr2<br>|
|**dtE**Defrost termination temperature|-50  50 C|8|Pr1|
|**IdF**Interval between defrost cycles|1120ore|6|Pr1|
|<br>**MdF**(Maximum)length for defrost|<br>0 255min|<br>30|<br>Pr1|
|**dSd**Start defrost delay<br>|0÷99min<br>|0<br>|Pr2<br>|
|**dFd**Displaying during defrost|rt,it, SEt,DEF|it|Pr2|
|**dAd**MAXdisplay delay afterdefrost|0÷ 255min|30|Pr2|
|**Fdt**Draining time|0÷120min|0|Pr2|
|**dPo**First defrost afterstart-up<br>|n=after IdF; y=immed.<br>|n<br>|Pr2<br>|
|**dAF**Defrost delay after fastfreezing|0÷ 23he 50’|0.0|Pr2|
|**Fnc**Fanoperatingmode|C-n, o-n, C-y, o-Y|o-n|Pr1|
|**Fnd**Fandelay afterdefrost|0÷255min|10|Pr1|
|**Fct**Differential of temperature for forced<br>activationof fans|<br>0÷50°C|10|Pr2|
|**FSt**Fanstop temperature|-50÷50°C/-58÷122°F|2|Pr1|
|**Fon **Fanontimewithcompressoroff|0÷15 (min.)|0|Pr2|
|**FoF **Fanofftimewithcompressoroff|0÷15 (min.)|0|Pr2|
|**FAP**Probe selection for fan management|nP;P1;P2;P3;P4|P2|Pr2|
|**ACH **Kind ofaction forauxiliaryrelay|CL;Ht|cL|Pr2|
|**SAA**SetPointforauxiliaryrelay|-100÷110°C /-58÷230°F|0,0|Pr2|
|**SHy **Differential for auxiliaryrelay|0,125.5°C/1255°F|2,0|Pr2|
|**ArP**Probe selection forauxiliaryrelay|nP/P1/P2/P3/P4|nP|Pr2|
|**Sdd **Auxiliaryrelay operating during defrost|n÷y|n|Pr2|
|**ALP**Alarmprobe selection|nP;P1;P2;P3;P4|P1|Pr2|
|**ALc**Temperat. alarms configuration|rE= related to set;<br>Ab=absolute|Ab|Pr2|
|**ALU**MAXIMUM temperature alarm|<br>Set110.0°C; Set÷230°F|110,0|Pr1|
|**ALL**Minimum temperature alarm|-100°CSet/-58°FSet|-50,0|Pr1|
|**AFH**Differential fortemperat.alarm recovery|(0,1°C÷25,5°C) (1°F÷45°F)|2,0|Pr2|
|**ALd**Temperature alarm delay|0 255min|15|Pr2|
|**dAO**Delayof temperature alarm at start up|0 23he 50’|1,3|Pr2|
|**AP2**Probefortemperatalarmofcondenser|nP;P1;P2;P3;P4|P4|Pr2|
|.   <br>**AL2**Condenser for lowtemperat.alarm|<br>(-100÷ 150°C) (-67÷302°F)|<br>-40|<br>Pr2|
|**AU2 **Condenser for hightemperat.alarm<br>|(-100÷ 150°C) (-67÷302°F)<br>|110<br>|Pr2<br>|
|**AH2**Differ. forcondensertemp.alar. recovery <br>**Ad2 **Condensertemeraturealarmdela|[0,1°C÷ 25,5°C] [1°F ÷ 45°F]<br>0÷ 254(min)255=nU|5<br>15|Pr2<br>Pr2|
|p  y<br>**dA2**Delay ofcond.temper.alarmat start up|. , <br>0.0÷ 23h50’|1,3|<br>Pr2|

|**Label **|<br>**Name**<br> <br> <br> <br> <br>|**Range**<br>|**Value**|**Level **|
|---|---|---|---|---|
|**bLL**|Compr.<br>off<br>for<br>condenser<br>low<br>temperature alarm|<br>n(0)- Y(1)|n|Pr2|
|**AC2 **|Compr.<br>off<br>for<br>condenser<br>high<br>temperature alarm|<br>n(0)- Y(1)|n|Pr2|
|**tbA**|Alarm relay disabling|n=no; y=yes|y|Pr2|
|**oA3**|Fourth relay configuration|ALr = alarm; dEF = do not select<br>it; Lig =Light; AUS =AUX;<br>onF=always on; Fan= do not<br>select it; db = neutral zone; cP2<br>= second compressor; dF2 = do|Lig|Pr2|
|||not selectit;HES= night blind|||
|**AoP**<br>|Alarm relay polarity (oA3=ALr)<br>|oP; cL<br>|cL<br>|Pr2<br>|
|**i1P**|Digital input polarity (18-20)|oP=opening;CL=closing|cL|Pr1|
|**i1F**|Digital input1configuration(18-20)|dor; dEF;|dor|Pr1|
|**i2P**|Digital inputpolarity (18-19)|oP=opening;CL=closing|cL|Pr2|
|**i2F**|Digital input configuration (18-19)|EAL - bAL- PAL - dor  - dEF -<br>ES - AUS - Htr - FAn - HdF -<br>|EAL|Pr2|
|||onF|||
|**did**|Digital input alarmdelay (18-20)|0÷255min|15|Pr1|
|**doA**|Dooropenalarmdelay|0÷255min|15|Pr1|
|**Nps **|Numberofactivationofpressure switch|0÷15|15|Pr2|
|**odc**|Compress and fan status when open<br>door|<br>no; Fan; CPr; F_C|F-c|Pr2|
|**rrd**|Regulation restartwithdooropenalarm|n – Y|y|Pr2|
|**HES**|Differential for Energy Saving|(-30°C÷30°C) (-54°F÷54°F)|0|Pr2|
|**Hur***|Currenthour|0÷ 23|-|Pr1|
|**Min***|Currentminute|0÷59|-|Pr1|
|**dAY***|Current day|Sun ÷SAt|-|Pr1|
|**Hd1***|Firstweeklyholiday|Sun÷SAt– nu|nu|Pr1|
|**Hd2***|Secondweeklyholiday|Sun÷SAt– nu|nu|Pr1|
|**ILE***|Energy<br>Saving<br>cycle<br>start during<br>workdays|<br>0 ÷ 23h 50 min.|0.0|Pr1|
|**dLE***|Energy Saving cycle length during<br>workdays|<br>0 ÷ 24h 00 min.|0|Pr1|
|**ISE***|Energy Saving cycle start on holidays|0÷ 23h50min.|0.0|Pr1|
|**dSE***|Energy Saving cyclelengthon holidays|0÷ 24h00min.|0|Pr1|
|**Ld1***|1<sup>st</sup>workdays defrost start|0÷ 23h50min. - nu|6.0|Pr1|
|**Ld2***|2<sup>nd</sup>workdays defrost start|0÷ 23h50min. - nu|13.0|Pr1|
|**Ld3***|3<sup>rd</sup>workdays defrost start|0÷ 23h50min. - nu|21.0|Pr1|
|**Ld4***|4<sup>th</sup>workdays defrost start|0÷ 23h50min. - nu|nu|Pr1|
|**Ld5***|5<sup>th</sup>workdays defrost start|0÷ 23h50min. - nu|nu|Pr1|
|**Ld6***|6<sup>th</sup>workdays defrost start|0÷ 23h50min. - nu|nu|Pr1|
|**Sd1***|1<sup>st</sup>holiday defrost start|0÷ 23h50min. - nu|6.0|Pr1|
|**Sd2***|2<sup>nd</sup>holiday defrost start|0÷ 23h50min. - nu|13.0|Pr1|
|**Sd3***<br>|3<sup>rd</sup>holiday defrost start<br>|0÷ 23h50min. - nu|21.0|Pr1|
|**Sd4***|4<sup>th</sup>holiday defrost start|0÷ 23h50min. - nu|nu|Pr1|
|**Sd5***|5<sup>th</sup>holiday defrost start|0÷ 23h50min. - nu|nu|Pr1|
|**Sd6***|6<sup>th</sup>holiday defrost start|0÷ 23h50min. - nu|nu|Pr1|
|**Adr**|Serialaddress|1÷247|1|Pr2|
|**PbC**|Kindofprobe|Pt1000;ntc|ntc|Pr2|
|<br>**onF**|<br>on/off key enabling|<br>nu, oFF;ES|nu|<br>Pr2|
|**dP1**|Roomprobe display|--|-|Pr1|
|**dP2**|Evaporatorprobedisplay|--|-|Pr1|
|<br>**dP3**|<br>Third probe display|<br>--|<br>-|<br>Pr1|
|**dP4**|Fourthprobe display|--|-|Pr1|
|**rSE**|Realset|actualset|-|Pr2|
|**rEL**|Softwarerelease|--|2.6|Pr2|
|<br>**Ptb**|<br>Map code|<br>--|-|<br>Pr2|

*** Only for model with real time clock**

2 Only for XR75CX with X-REP output
