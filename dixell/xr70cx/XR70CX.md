# Dixell XR70CX – Digital controller with defrost and fan management – XR70CX

Kilde: `XR70CX-GB.pdf` i denne mappe. Konverteret direkte fra PDF'en. Tabeller (parametre, alarmer, standardværdier) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra tegninger står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilket afsnit svaret kommer fra.
- Alarm- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer (Dixell, Danfoss, Carel). Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualen, så sig det i stedet for at gætte.

---

#### **Digital controller with defrost and fan management**

### **XR70CX**

1. GENERAL WARNING ________________________________________________________ 1 2. GENERAL DESCRIPTION ____________________________________________________ 1 3. CONTROLLING LOADS ______________________________________________________ 1 4. FRONT PANEL COMMANDS __________________________________________________ 1 5. MAX & MIN TEMPERATURE MEMORIZATION ____________________________________ 1 6. MAIN FUNCTIONS __________________________________________________________ 2 7. PARAMETERS _____________________________________________________________ 2 8. DIGITAL INPUTS ____________________________________________________________ 3 9. TTL SERIAL LINE – FOR MONITORING SYSTEMS ________________________________ 3 10. X-REP OUTPUT – OPTIONAL _________________________________________________ 3 11. INSTALLATION AND MOUNTING ______________________________________________ 4 12. ELECTRICAL CONNECTIONS _________________________________________________ 4 13. USE THE HOT KEY __________________________________________________________ 4 14. ALARM SIGNALS ___________________________________________________________ 4 15. TECHNICAL DATA __________________________________________________________ 4 16. CONNECTIONS _____________________________________________________________ 4 17. DEFAULT SETTING VALUES __________________________________________________ 4

#### **1. GENERAL WARNING**

##### **1.1 PLEASE READ BEFORE USING THIS MANUAL**

- This manual is part of the product and should be kept near the instrument for easy and quick reference.

- The instrument shall not be used for purposes different from those described hereunder. It cannot be used as a safety device.

- Check the application limits before proceeding.

- Dixell Srl reserves the right to change the composition of its products, even without notice, ensuring the same and unchanged functionality.

##### **1.2 SAFETY PRECAUTIONS**

- Check the supply voltage is correct before connecting the instrument.

- Do not expose to water or moisture: use the controller only within the operating limits avoiding sudden temperature changes with high atmospheric humidity to prevent  formation of condensation

- Warning: disconnect all electrical connections before any kind of maintenance.

- Fit the probe where it is not accessible by the End User. The instrument must not be opened.

- In case of failure or faulty operation send the instrument back to the distributor or to “Dixell S.r.l.” (see address) with a detailed description of the fault.

- Consider the maximum current which can be applied to each relay (see Technical Data).

- Ensure that the wires for probes, loads and the power supply are separated and far enough from each other, without crossing or intertwining.

- In case of applications in industrial environments, the use of mains filters (our mod. FT1) in parallel with inductive loads could be useful.

#### **2. GENERAL DESCRIPTION**

Model **XR70CX** , format 32x74mm, is microprocessor based controller, suitable for applications on medium or low temperature ventilated refrigerating units. It has four relay outputs to control compressor, fan, and defrost, which can be either electrical or reverse cycle (hot gas). The last one can be used as light, for alarm signalling or as auxiliary output. It is also provided with up to 4 NTC or PTC probe inputs, the first one for temperature control, the second one, to be located onto the evaporator, to control the defrost termination temperature and to managed the fan. The digital input can operate as third temperature probe.  The fourth one, to connect to the HOT KEY terminals, is used to signal the condenser temperature alarm or to display another temperature. The **HOT-KEY** output allows to connect the unit, by means of the external module XJ485-CX, to a network line **ModBUS-RTU** compatible such as the Dixell monitoring units of X-WEB family. It allows to program the controller by means the HOT-KEY programming keyboard. The instrument is fully configurable through special parameters that can be easily programmed through the keyboard.

#### **3. CONTROLLING LOADS**

##### **3.1 COMPRESSOR**

*[Figurtekst: The regulation is performed according  Temper. · to the temperature measured by the · thermostat probe with a positive  SET · differential from the set point: if the · temperature increases and reaches set  Time · point plus differential the compressor is · started and then turned off when the  Compr. · temperature reaches the set point value  ON · again. · In case of fault in the thermostat probe the start and stop of the compressor are timed through · parameters  Con  and  CoF .]*

##### **3.2 DEFROST**

Two defrost modes are available through the **tdF** parameter: defrost through electrical heater ( **tdF=EL** ) and hot gas defrost ( **tdF=in** ).

Other parameters are used to control the interval between defrost cycles ( **idF** ), its maximum length ( **MdF** ) and two defrost modes: timed or controlled by the evaporator’s probe ( **P2P** ). At the end of defrost dripping time is started, its length is set in the **Fdt** parameter. With **Fdt=0** the dripping time is disabled.

##### **3.3 CONTROL OF EVAPORATOR FANS**

The fan control mode is selected by means of the **FnC** parameter:

**FnC=C_n** , fans will switch ON and OFF with the compressor and **not run** during defrost. **FnC=o_n** , fans will run even if the compressor is off, and not run during defrost.

After defrost, there is a timed fan delay allowing for drip time, set by means of the **Fnd** parameter. **FnC=C_Y** , fans will switch ON and OFF with the compressor and **run** during defrost. **FnC=o_Y** , fans will run continuously also during defrost.

An additional parameter **FSt** provides the setting of temperature, detected by the evaporator probe, above which the fans are always OFF. This is used to make sure circulation of air only if his temperature is lower than set in **FSt** .

###### **3.3.1 Forced activation of fans**

This function managed by the **FCt** parameter is designed to avoid short cycles of fans, that could happen when the controller is switched on or after a defrost, when the room air warms the evaporator. **How it works:** if the temperature difference between evaporator probe and room probe is higher than the **FCt** parameter value, fans will be switched on. With **FCt=0** the function is disabled.

###### **3.3.2 Cyclical activation of the fans with compressor off.**

When **FnC=C-n** or **C-Y** (fans working in parallel with the compressor), by means of the **Fon** and **FoF** parameters the fans can carry out on and off cycles even if the compressor is switched off. When the compressor is stopped the fans go on working for the **Fon** time. With **Fon=0** the fans remain always off, also when the compressor is off.

#### **4. FRONT PANEL COMMANDS**

To display target set point; in programming mode it selects a parameter or confirm an operation. ( **DEF** ) To start a manual defrost. ( **UP** ) To see the max stored temperature; in programming mode it browses the parameter codes or increases the displayed value. ( **DOWN** ) To see the min stored temperature; in programming mode it browses the parameter codes or decreases the displayed value. To switch the instrument on and off (when **onF=oFF** ). To switch on and off the light (when **oA3=LiG** ).

###### **KEY COMBINATIONS:**

*[Figurtekst: +  To lock & unlock the keyboard . · + To enter in programming mode. · + To return to the room temperature display.]*

##### **4.1 USE OF LEDS**

Each LED function is described in the following table.

*[Figurtekst: LED  MODE  FUNCTION · ON  Compressor enabled · Flashing Anti-short cycle delay enabled · ON  Defrost enabled · Flashing Drip time in progress · ON  Fans enabled · Flashing Fans delay after defrost in progress. · ON  An alarm is occurring · ON  Continuous cycle is running · ON  Energy saving enabled · ON  Light on · ON  Auxiliary relay on · ON  Measurement unit · °C/°F · Flashing Programming phase]*

#### **5. MAX & MIN TEMPERATURE MEMORIZATION**

##### **5.1 HOW TO: SEE THE MIN TEMPERATURE**

1. Press and release the **DOWN** key.

2. The “ **Lo** ” message will be displayed followed by the minimum temperature recorded.

3. By pressing the **DOWN** key again or by waiting 5 sec the normal display will be restored.

##### **5.2 HOW TO: SEE THE MAX TEMPERATURE**

1. Press and release the **UP** key.

2. The “ **Hi** ” message will be displayed followed by the maximum temperature recorded.

3. By pressing the **UP** key again or by waiting 5 sec the normal display will be restored.

- **5.3 HOW TO: RESET THE MAX AND MIN TEMPERATURE RECORDED**

1. Keep the **SET** key pressed more than 3 sec, while the max or min temperature is displayed. (“ **rSt** ” message will be displayed)

2. To confirm the operation the “ **rSt** ” message will start blinking and the normal temperature will be displayed.

#### **6. MAIN FUNCTIONS**

##### **6.1 HOW TO: SEE THE SET POINT**

1. Push and immediately release the **SET** key: the display will show the Set point value.

2. Push and immediately release the **SET** key or wait for 5 sec to display the probe value again.

##### **6.2 HOW TO CHANGE THE SET POINT**

1. Push the **SET** key more than 2 sec to change the Set point value.

2. The value of the set point will be displayed and the “ **°C** ” or “ **°F** ” LED will start blinking.

3. To change the Set value push the **UP** or **DOWN** arrows within 10 sec.

4. To save the new set point value, push the **SET** key again or wait for 10 sec.

##### **6.3 HOW TO START A MANUAL DEFROST**

Push the **DEF** key for more than 2 sec and a manual defrost will start.

##### **6.4 HOW TO: CHANGE A PARAMETER VALUE**

To change a parameter value, operate as follows:

1. Enter the Programming mode by pressing the **SET+DOWN** buttons for 3s (the **°C** or **°F** LED will start blinking).

2. Select the required parameter. Press the **SET** button to display its actual   value.

3. Use **UP** or **DOWN** buttons to change its value.

4. Press **SET** button to store the new value and move to the following parameter.

**To exit** : Press **SET + UP** buttons or waiting for 15s without pressing any key.

**NOTE** : the set value is stored even when the procedure is exited by waiting for the time-out to expire.

##### **6.5 THE HIDDEN MENU**

The hidden menu includes all the parameters of the instrument.

###### **6.5.1 HOW TO: ENTER THE HIDDEN MENU**

1. Enter the Programming mode by pressing the **SET+DOWN** buttons for 3 sec (the **°C** or **°F** LED will start blinking).

2. Released the buttons and then push again the **SET+DOWN** buttons for more than 7s. The Pr2 label will be displayed immediately followed from the **HY** parameter. **Now it is possible to browse the hidden menu.**

3. Select the required parameter.

4. Press the **SET** button to display its value.

5. Use **UP** or **DOWN** to change its value.

6. Press **SET** to store the new value and move to the following parameter.

**To exit** : Press **SET+DOWN** or wait 15 sec without pressing a key.

**NOTE1:** if no parameter is present in Pr1 menu, after 3 sec the “ **noP** ” message will be displayed. Keep the buttons pushed till the Pr2 message will be displayed.

**NOTE2:** the set value is stored even when the procedure is exited by waiting for the time-out to expire

###### **6.5.2 HOW TO: MOVE A PARAMETER FROM THE HIDDEN MENU TO THE FIRST LEVEL AND VICEVERSA.**

Each parameter present in the hidden menu (Pr2) can be moved into the user level (Pr1) by pressing **SET+DOWN** buttons. If a parameter is part of the user level, when showed in the hidden menu the decimal point will be lit.

##### **6.6 HOW TO: LOCK THE KEYBOARD**

1. Keep both **UP** and **DOWN** buttons pressed for more than 3 sec.

2. The “ **PoF** ” message will be displayed and the keyboard will be locked. At this point it will be possible only to see the set point or the MAX o Min temperature stored

3. If a button is pressed more than 3 sec the “ **PoF** ” message will be displayed

##### **6.7 HOW TO: UNLOCK THE KEYBOARD**

Keep pressed together for more than 3 sec the **UP** and **DOWN** keys till the **“Pon”** message will be displayed.

##### **6.8 THE CONTINUOUS CYCLE**

When defrost is not in progress, it can be activated by holding the **UP** key pressed for about 3 sec. The compressor operates to maintain the **CCS** set point for the time set through the **CCt** parameter. The cycle can be terminated before the end of the set time using the same activation key **UP** for 3 sec.

##### **6.9 THE ON/OFF FUNCTION**

With “ **onF = oFF** ”, pushing the **ON/OFF** key, the instrument is switched off. The **“OFF”** message is displayed. In this configuration, the regulation is disabled.

To switch the instrument on, push again the ON/OFF key.

**WARNING: Loads connected to the normally closed contacts of the relays are always supplied and under voltage, even if the instrument is in stand by mode.**

#### **7. PARAMETERS**

|**REGUL**<br>**HY**|**ATION**<br>**Differential:**(0.1 to 25.5°C; 1 to 45°F) intervention differential for set point.<br>Compressor Cut IN is Set Point + differential (**HY**). Compressor Cut OUT is when the<br>|
|---|---|
|**LS**|temperaturereaches the set point.<br>**Minimum set point:**(-100°C to SET; -148°F to SET) sets the minimum value for the<br>|
|**US**|set point.<br>**Maximum set point:**(SET to 150°C; SET to 302°F) set the maximum value for set<br>|
|**ot**|point.<br>**Thermostat probe calibration:**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust<br>possibleoffsetofthethermostatprobe.|
|**P2P**|<br>**Evaporator probe presence:**(n; Y)**n**= not present, the defrost stops by time;<br>**Y**=tthdfttbtt|
|**oE**|presen, e eros sops y emperaure.<br>**Evaporator probe calibration:**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible<br>fffh|
|**P3P**|oset o te evaporatorprobe.<br>**Third probe presence (P3):**(n; Y)**n**= not present, the terminals 18-20 operate as<br>diital inut;**Y**=resenttheterminals18-20oerateasthirdrobe|
|**o3**|g p  p,    p   p.<br>**Third probe calibration (P3):**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible<br>offsetofthethirdrobe|
|**P4P**<br>**o4**|p.<br>**Fourth probe presence: **(n;Y)n = Not present;Y =present.<br>**Fourth probe calibration:**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible<br>offsetofthefourthrobe|
|**odS**|p.<br>**Outputs activation delay at start up:**(0 to 255min) this function is enabled at the<br>initial start up of the instrument and inhibits any output activation for the period of time<br>titht|
|**AC**|sene parameer.<br>**Anti-short cycle delay:**(0 to 50min) minimum interval between the compressor stop<br>andthefollowinrestart|
|**rtr**|g .<br>**Percentage of the second and first probe for regulation:**(0 to 100; 100=P1, 0=P2)<br>it allows to set the regulation according to the percentage of the first and second probe,<br>asforthefollowinformula(**rtr**(P1-P2)/100+ P2)|
|**CCt**|g   .<br>**Compressor ON time during continuous cycle:**(0.0 to 24h00min, res. 10min)<br>allows to set the length of the continuous cycle. Compressor stays on without<br>interruption during**CCt**time. This is useful, for instance, when the room is filled with<br> dt|
|**CCS**|newproucs.<br>**Set point for continuous cycle:**(-55 to 150°C; -67 to 302°F) it sets the set point<br>ddithtil|
|**Con**|use urng e connuous cyce.<br>**Compressor ON time with faulty probe:**(0 to 255min) time during which the<br>compressor is active in case of faulty thermostat probe. With**Con=0**compressor is<br>|
|**CoF**|always OFF.<br>**Compressor OFF time with faulty probe:**(0 to 255min) time during which the<br>compressor is OFF in case of faulty thermostat probe. With**CoF=0**compressor is<br>alwasactive|
|**DISPLA**|y .<br>**Y**|
|**CF**|**Temperature measurement unit:**(°C; °F)**°C**= Celsius;**°F**= Fahrenheit.<br>**WARNING:**When the measurement unit is changed the SET point and the values of<br>the parameters**HY**,**LS**,**US**,**ot**,**ALU**and**ALL**have to be checked and modified (if<br>nr|
|**rES**<br>**Lod**|ecessay).<br>**Resolution (for °C):** (in=1°C; dE=0.1°C) allows decimalpoint display.<br>**Instrument display:**(P1; P2, P3, P4, SET, dtr) it selects which probe is displayed by<br>the instrument.**P1**= Thermostat probe;**P2**= Evaporator probe;**P3**= Third probe (only<br>for model with this option enabled);**P4**= Fourth probe,**SET**= set point;**dtr**=<br>f|
|**rEd**|percentage ovisualization.<br>**X-REP display (optional):**(P1; P2, P3, P4, SET, dtr) it selects which probe is<br>displayed by X- REP.**P1**= Thermostat probe;**P2**= Evaporator probe;**P3**= Third probe<br>(only for model with this option enabled);**P4**= Fourth probe,**SET**= set point;<br>**dtr**=percentageof visualization|
|**dL**<br>**Y**|.<br>**Display delay:**(0 to 20min00s; res. 10s) when the temperature increases, the display<br>idtdf 1°C1°Fft thiti|
|<br>**dtr**|s upae o  oraers me.<br>**Percentage of the second and first probe for visualization when Lod=dtr:**(0 to 99;<br>100=P1, 0=P2) if**Lod=dtr**it allows to set the visualization according to the percentage<br>|
|**DEFRO**<br>|ofthefirst and second probe, asforthefollowingformula (**dtr**(P1-P2)/100+ P2).<br>**ST**<br>|
|**tdF**<br>**dFP**|**Defrost type:** (EL;in) **EL**=electrical heater; **in**= hot gas.<br>**Probe selection for defrost termination:**(nP; P1; P2; P3; P4)**nP**= no probe;<br>**P1**=thermostat probe;**P2**= evaporator probe;**P3**=configurable probe;**P4**= Probe on<br>HotKelu|
|**dtE**|y pg.<br>**Defrost termination temperature:**(-55 to 50°C; -67 to 122°F) (enabled only when<br>**EdF=Pb**) sets the temperature measured by the evaporator probe, which causes the<br>|
|**idF**|end ofdefrost.<br>**Interval between defrost cycles:**(0 to 120hours) determines the interval of time<br>|
|**Md**<br>**F**|betweentwo defrost cycles.<br>**(Maximum) length for defrost:**(0 to 255min) when**P2P=n**, (not evaporator probe:<br>timed defrost) it sets the defrost duration. When**P2P=Y**(defrost end based on<br>ih ilh f df|
|**dSd**|temperature) t sets temaxmumengt orerost.<br>**Start defrost delay:**(0 to 99min) this is useful when different defrost start times are<br>|
|**dFd**<br>**dAd**|necessary to avoid overloading the plant.<br>**Temperature displayed during defrost:**(rt; it; SEt; dEF)**rt**= real temperature;<br>**it**=temperature at defrost start; **SEt**=set point; **dEF**= “**dEF**” label.<br>**MAX display delay after defrost:**(0 to 255min) sets the maximum time between the<br>endofdefrostandtherestartinofthereal roomtemeraturedisla|
|**Fdt**|g     p py.<br>**Drip time:**(0 to 120min) time interval between reaching defrost termination|
||temperature and the restoring of the control’s normal operation. This time allows the<br>evaporatorto eliminatewaterdrops thatmighthaveformed due to defrost.|

|**dPo**|**First defrost after start-up:**(n; Y)<br><br>**n**= after the**idF**time,<br><br>|
|---|---|
|**dAF**|<br>**Y**= immediately.<br>**Defrost delay after continuous cycle:**(0.0 to 24h00min, res. 10min) time interval<br>betweenthe end ofthefastfreezing cycle and thefollowing defrostrelated toit.|
|**FANS**||
|**FnC**<br>**Fnd**|**Fans operating mode:**(C-n; o-n; C-Y; o-Y)**C-n**= runs with the compressor, OFF<br>during defrost;**o-n**= continuous mode, OFF during defrost;**C-Y**= runs with the<br>compressor, ONduring defrost; **o-Y**=continuousmode, ONduring defrost.<br>**Fans delay after defrost:**(0 to 255min) interval between end of defrost and evaporator<br>fansstart|
|**FCt**<br>**FSt**|.<br>**Temperature differential to avoid fan short cycles:**(0 to 59°C; 0 to 90°F) (N.B.: if<br>**FCt=0**function disabled) if the difference of temperature between the evaporator and<br>theroomprobesishigherthan**FCt**value, thefanswillbe switched on.<br>**Fans stop temperature:**(-55 to 50°C; -67 to 122°F) setting of temperature, detected<br>bt bbhih flOFF|
|**Fon**|y evaporaorproe, aovewc ans are aways .<br>**Fan ON time:**(0 to 15min) with**Fnc=C_n**or**C_Y**, (fan activated in parallel with<br>compressor) it sets the evaporator fan ON cycling time when the compressor is off.<br>With**Fon=0**and**FoF≠0**the fan are always off, with**Fon=0**and**FoF=0**the fan are<br>alwaysoff|
|**FoF**|.<br>**Fan OFF time:**(0 to 15min) With**FnC=C_n**or**C_Y**, (fan activated in parallel with<br>compressor) it sets the evaporator fan off cycling time when the compressor is off.<br>With**Fon=0**and**FoF≠0**the fan are always off, with**Fon=0**and**FoF=0**the fan are<br>alwaysoff.|
|**FAP**|<br>**Probe selection for fan management:**(nP; P1; P2; P3; P4)**nP**= no probe;<br>**P1**=thermostat probe;**P2**= evaporator probe;**P3**=configurable probe;**P4**= Probe on<br>HotKey plug.|
|**ALARM**|**S**|
|**ALC**<br>**ALU**<br>**ALL**<br>**AFH**|**Temperature alarms configuration:**(Ab; rE)**Ab**= absolute temperature, alarm<br>temperature is given by the**ALL**or**ALU**values.**rE**= temperature alarms are referred<br>to the set point. Temperature alarm is enabled when the temperature exceeds the<br>[**SET+ALU**] or[**SET-ALL**]values.<br>**MAXIMUM temperature alarm:**<br><br>If**ALC=Ab**: [ALL to 150.0°C or ALL to 302°F]<br><br>If**ALC=rE**: [0.0 to 50.0°C or 0 to 90°F]<br>whenthis temperatureisreached the alarm is enabled, afterthe **ALd** delay time.<br>**Minimum temperature alarm:**<br><br>If**ALC=Ab**: [-100°C to ALU; -148 to ALU]<br><br>If**ALC=rE**: [0.0 to 50.0°C or 0 to 90°F]<br>whenthis temperatureisreached the alarm is enabled, afterthe **ALd** delay time.<br>**Differential for temperature alarm recovery:**(0.1 to 25.5°C; 1 to 45°F) intervention<br>|
|**ALd**|differential for recovery oftemperature alarm.<br>**Temperature alarm delay:**(0 to 255 min) time interval between the detection of an<br>alarmconditionandalarmsignalling|
|**dAo**|.<br>**Exclusion of temperature alarm at start-up:**(0.0 to 24h00min, res. 10min) time<br>interval between the detection of the temperature alarm condition after instrument<br>oweronandalarmsinallin|
|**CONDE**|p    gg.<br>**NSER TEMPERATURE ALARM**|
|**AP2**|**Probe selection for temperature alarm of condenser:**(nP; P1; P2; P3; P4)<br>**nP**= no probe;**P1**= thermostat probe;**P2**= evaporator probe;**P3**= configurable<br>|
|**AL2**|probe; **P4**= Probe on HotKey plug.<br>**Low temperature alarm of condenser:**(-100 to 150°C; -148 to 302°F) when this<br>temperatureisreachedthe**LA2**alarm issignalledpossiblyaftertheAd2delay|
|**Au2**|,     .<br>**High temperature alarm of condenser:**(-100 to 150°C; -148 to 302°F) when this<br>temperatureisreachedthe**HA2**alarm issignalledpossiblyafterthe**Ad2**delay|
|**AH2**<br>**Ad2**|,     .<br>**Differential for temperature condenser alarm recovery:** 0.1to25.5°C;1to45°F<br>**Condenser temperature alarm delay:**(0 to 255 min) time interval between the<br>detectionofthecondenseralarmconditionandalarmsinallin|
|**dA2**<br>**bLL**|gg.<br>**Condenser temperature alarmexclusion at start up:** 0.0 to24h00min,res. 10min.<br>**Compressor off with low temperature alarm of condenser:**(n; Y)**n**= compressor<br>keeps on working;**Y**= compressor is switched off till the alarm is present, in any case<br>regulation restartsafter**AC**timeatminimum.|
|**AC2**|<br>**Compressor off with high temperature alarm of condenser:**(n; Y)**n**= compressor<br>keeps on working;**Y**= compressor is switched off till the alarm is present, in any case<br>regulation restarts after**AC** time atminimum.|
|**FOURTH**|**RELAY**|
|**tbA**<br>**oA3**|**Alarm relay silencing (with oA3 =ALr):**(n; Y)**n**= silencing disabled: alarm relay<br>stays on till alarm condition lasts.**Y**= silencing enabled: alarm relay is switched OFF by<br>pressing akey during analarm.<br>**Second relay configuration (1-4):**(dEF; FAn; ALr; LiG; AUS; onF; db; dEF2; HES)<br>**dEF**= defrost;**FAn**= do not select it;**ALr**= alarm;**LiG**= light;**AUS**= Auxiliary relay;<br>**onF**= always on with instrument on;**db**= neutral zone;**dEF2**= do not select it;**HES**=<br>|
|**AoP**|night blind.<br>**Alarm relay polarity:**(CL; oP) it set if the alarm relay is open or closed when an alarm<br>occurs.**CL**= terminals 1-4 closed during an alarm;**oP**= terminals 1-4 open during an<br>alarm|
|**DIGITAL**|.<br>**INPUTS**|
|**i1P**|**Second digital input polarity:**(oP; CL)**oP**= the digital input is activated by opening<br>|
|**i1F**|the contact; **CL **=the digital inputis activated by closing the contact.<br>**Second digital input configuration:**(EAL; bAL; PAL; dor; dEF; ES; AUS; Htr; FAn;<br>HdF; onF)**EAL**= external alarm: “**EA**” message is displayed;**bAL**= serious alarm “**CA**”<br>message is displayed;**PAL**= pressure switch alarm, “**CA**” message is displayed;**dor**=<br>door switch function;**dEF**= activation of a defrost cycle;**ES**= energy saving;**AUS**=<br>auxiliary relay activation with**oA3=AUS**;**Htr**= type of inverting action (cooling or<br>heating);**FAn**= fan;**HdF**= Holiday defrost (enable only with RTC);**onF**= to switch the<br>controlleroff.|

|**did**|**Digital input 1 alarm delay:**(0 to 255 min) delay between the detection of the<br>external alarm condition and its signalling.<br>When**i1F= PAL**, it is the interval of time to calculate the number of pressure switch<br>activation.|
|---|---|
|**nPS**|**Number of pressure switch activation:**(0 to 15) Number of activation, during the**did**<br>or**d2d**interval, before signalling an alarm event (**i1F, i2F=PAL**).<br>If the**nPS**activation during**did**or**d2d**time is reached, switch off and on the instrument<br>torestartnormal regulation.|
|**odC**|**Compressor status when open door:**(no; FAn; CPr;F_C;)**no**= normal;<br>**FAn**= normal; **CPr**=compressorOFF, **F_C**=compressorOFF.|
|**rrd**|**Outputs restart after door open alarm:**(n; Y)**n**= outputs follow the**odC**parameter.<br>**Y**=outputsrestartwitha dooropenalarm.|
|**HES**<br>**THER**|**Delta temperature during an Energy Saving cycle:**(-30.0 to 30.0°C; -54 to 54°F) it<br>sets theincreasingvalue ofthe set point **[SET+HES]** during theEnergy Saving cycle.|
|**Adr**|**Serial address:**(1 to 247) identifies the instrument address when connected to a<br>ModBUS compatiblemonitoring system.|
|**PbC**|**Type of probe:**(PtC; ntC) it allows to set the kind of probe used by the instrument:<br>**PtC **= PTC probe, **ntC**= NTC probe.|
|**onF**|**On/Off key enabling:** (nU; oFF;ES) **nU**=disabled; **oFF**=enabled; **ES**= not setit.|
|**dP1**|Thermostat probe display.|
|**dP2**|Evaporatorprobe display.|
|**dP3**|Third probe display-optional.|
|**dP4**|Fourthprobe display.|
|**rSE**|Real set point: it shows the set point used during the energy saving cycle or during the<br>continuous cycle.|
|**rEL**|Softwarereleasefor internaluse.|
|**Ptb**|Parametertable code: readable only.|

###### **OTHER**

#### **8. DIGITAL INPUTS**

The free voltage digital input is programmable by the **i1F** parameter.

**8.1 GENERIC ALARM (I1F = EAL)**

As soon as the digital input is activated the unit will wait for **did** time delay before signalling the **EAL** alarm message. The outputs statuses don’t change. The alarm stops just after the digital input is deactivated.

##### **8.2 SERIOUS ALARM MODE (I1F = BAL)**

When the digital input is activated, the unit will wait for **did** delay before signalling the **CA** alarm message. The relay outputs are switched OFF. The alarm will stop as soon as the digital input is deactivated.

##### **8.3 PRESSURE SWITCH (I1F = PAL)**

If during the interval time set by **did** parameter, the pressure switch has reached the number of activation of the **nPS** parameter; the **CA** pressure alarm message will be displayed. The compressor and the regulation are stopped. When the digital input is ON the compressor is always OFF. **If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation.**

##### **8.4 DOOR SWITCH INPUT (I1F = DOR)**

It signals the door status and the corresponding relay output status through the **odC** parameter: **no** = normal (any change); **FAn** = Fan OFF; **CPr** = Compressor OFF; **F_C** = Compressor and fan OFF. Since the door is opened, after the delay time set through parameter **doA** , the door alarm is enabled, the display shows the message **dA** and **the regulation restarts is rtr=YES.** The alarm stops as soon as the external digital input is disabled again. With the door open, the high and low temperature alarms are disabled.

##### **8.5 START DEFROST (I1F = DEF)**

It starts a defrost if there are the right conditions. After the defrost is finished, the normal regulation will restart only if the digital input is disabled otherwise the instrument will wait until the “MdF” safety time is expired.

- **8.6 SWITCH THE AUXILIARY RELAY (I1F = AUS)**

With oA3 = AUS the digital input switched the status of the auxiliary relay

- **8.7 INVERSION OF THE KIND OF ACTION: HEATING-COOLING (I1F=HTR)**

This function allows to invert the regulation of the controller: from cooling to heating and viceversa.

- **8.8 ENERGY SAVING (I1F = ES)**

The Energy Saving function allows to change the set point value as the result of the SET+ HES (parameter) sum. This function is enabled until the digital input is activated.

- **8.9 ON OFF FUNCTION (I1F = ONF)**

To switch the controller on and off.

- **8.10 DIGITAL INPUT POLARITY**

The digital input polarity depends on the **i1P** parameter. **i1P = CL** : the input is activated by closing the contact. **i1P = oP** : the input is activated by opening the contact

#### **9. TTL SERIAL LINE – FOR MONITORING SYSTEMS**

The TTL serial line, available through the HOT KEY connector, allows to connect the instrument to a monitoring system **ModBUS-RTU** compatible such as the **XWEB500** .

#### **10. X-REP OUTPUT – OPTIONAL**

As optional, an X-REP can be connected to the instrument, trough the dedicated connector.

To connect the X-REP to the instrument the following connectors must be used CAB-51F(1m), CAB52F(2m), CAB-55F(5m),

#### **11. INSTALLATION AND MOUNTING**

Instrument **XR70CX** shall be mounted on vertical panel, in a 29x71 mm hole, and fixed using the special bracket supplied. The temperature range allowed for correct operation is 0 to 60°C. Avoid places subject to strong vibrations, corrosive gases, excessive dirt or humidity. The same recommendations apply to probes. Let air circulate by the cooling holes.

#### **12. ELECTRICAL CONNECTIONS**

The instrument is provided with screw terminal block to connect cables with a cross section up to 2.5mm<sup>2</sup> . Before connecting cables make sure the power supply complies with the instrument’s requirements. Separate the probe cables from the power supply cables, from the outputs and the power connections. Do not exceed the maximum current allowed on each relay, in case of heavier loads use a suitable external relay.

##### **12.1 PROBE CONNECTION**

The probes shall be mounted with the bulb upwards to prevent damages due to casual liquid infiltration. It is recommended to place the thermostat probe away from air streams to correctly measure the average room temperature. Place the defrost termination probe among the evaporator fins in the coldest place, where most ice is formed, far from heaters or from the warmest place during defrost, to prevent premature defrost termination.

#### **13. USE THE HOT KEY**

##### **13.1 HOW TO: PROGRAM A HOT KEY FROM THE INSTRUMENT (UPLOAD)**

1. Program one controller with the front keypad.

2. When the controller is <u>ON, insert the “</u> **HOT-KEY** ” and push **UP** button; the “ **uPL** ” message appears followed a by a flashing “ **End** ” label.

3. Push **SET** button and the “ **End** ” will stop flashing.

4. <u>Turn OFF the instrument, remove the “</u> **HOT-KEY** ” and then turn it ON again.

**NOTE** : the “ **Err** ” message appears in case of a failed programming operation. In this case push again button if you want to restart the upload again or remove the “ **HOT-KEY** ” to abort the operation.

##### **13.2 HOW TO: PROGRAM AN INSTRUMENT USING A HOT KEY (DOWNLOAD)**

1. Turn OFF the instrument.

2. Insert a **pre-programmed** “ **HOT-KEY** ” **into the 5-PIN receptacle** and then turn the Controller ON.

3. The parameter list of the “ **HOT-KEY** ” will be automatically downloaded into the Controller memory. The “ **doL** ” message will blink followed a by a flashing “ **End** ” label.

4. After 10 seconds the instrument will restart working with the new parameters.

5. Remove the “ **HOT-KEY** ”.

**NOTE:** the message “ **Err** ” is displayed for failed programming. In this case turn the unit off and then on if you want to restart the download again or remove the “ **HOT-KEY** ” to abort the operation.

#### **14. ALARM SIGNALS**

|**Message**|**Cause**|**Outputs**|
|---|---|---|
|“P1”|Roomprobefailure|Compressoroutput acc.to par.**Con** and **CoF**|
|“P2”|Evaporatorprobefailure|Defrost endis timed|
|“P3”|Third probefailure|Outputs unchanged|
|“P4”|Fourthprobefailure|Outputs unchanged|
|“HA”|Maximumtemperature alarm|Outputs unchanged.|
|“LA”|Minimumtemperature alarm|Outputs unchanged.|
|"HA2"|Condenser hightemperature|It depends onthe **AC2** parameter|
|"LA2"|Condenser lowtemperature|It depends onthe **bLL** parameter|
|“dA”|Dooropen|Compressorandfansrestarts|
|“EA”|Externalalarm|Output unchanged.|
|“CA”|Serious externalalarm(**i2F=bAL**)|Alloutputs OFF.|
|“CA”|Pressure switchalarm(**i2F=PAL**)|Alloutputs OFF|
|“rtc”|Real time clock alarm|Alarm output ON; Other outputs unchanged;<br>Defrosts according to par.**idF**Set real time clock<br>has to be set|
|rtF|Real time clock board failure|Alarm output ON; Other outputs unchanged;<br>Defrosts according to par.**idF** Contact the service|

##### **14.1 ALARM RECOVERY**

Probe alarms **P1** ”, “ **P2”,** “ **P3** ” and “ **P4** ” start some seconds after the fault in the related probe; they automatically stop some seconds after the probe restarts normal operation. Check connections before replacing the probe.

Temperature alarms “ **HA** ”, “ **LA** ” “ **HA2** ” and “ **LA2** ” automatically stop as soon as the temperature returns to normal values.

Alarms **“EA”** and **“CA”** (with **i2F=bAL** ) recover as soon as the digital input is disabled.

Alarm “ **CA”** (with **i2F=PAL** ) recovers only by **switching off and on** the instrument.

##### **14.2 OTHER MESSAGES**

**Pon** Keyboard <u>unlocked.</u> **PoF** Keyboard locked **noP In programming mode** : none parameter is present in Pr1 **<u>On the display</u>** <u>or in dP2, dP3, dP4: the selected probe is nor enabled</u>

#### **15. TECHNICAL DATA**

**Housing:** self extinguishing ABS. **Case:** frontal 32x74 mm; depth 60mm; **Mounting:** panel mounting in a 71x29mm panel cut-out **Protection:** IP20; **Frontal protection:** IP65 **Connections:** Screw terminal block  2.5 mm<sup>2</sup> wiring **Power supply:** according to the model 12VAC/DC, ±10% 110AC 10%, 50/60Hz 230VAC 10%, 50/60Hz **Power absorption:** 3VA max **Display** : 3 digits, red LED, 14.2 mm high **Inputs** : Up to 4 NTC or PTC probes **Digital inputs:** free voltage contact **Relay outputs: compressor** SPST 8(3) A, 250VAC or SPST 16A 250VAC **Defrost:** SPDT 8(3) A, 250VAC **Fan:** SPST 5A, 250VAC **Aux:** SPDT 8(3) A, 250VAC **Buzzer:** optional **Data storing** : on the non-volatile memory (EEPROM) **Internal clock back-up:** 24 hours **Kind of action:** 1B **Pollution degree:** 2 **Software class:** A **Rated impulsive voltage** : 2500V **Overvoltage Category** : II **Operating temperature:** 0 to 55°C **Storage temperature:** -25 to 60°C **Relative humidity:** 20 to 85% (no condensing) **Measuring and regulation range: NTC probe:** -40 to 110°C (-40 to 230°F) **PTC probe:** -100 to 150°C (-148 to 302°F) **Resolution:** 0.1°C or 1°C or 1°F (selectable) **Accuracy (ambient temp. 25°C)** :  ±0.7°C ±1 digit

**16. CONNECTIONS The X-REP output excludes** the TTL output.. It’s present in the following codes: XR70CX- xx **2** xx, XR70CX –xx **3** xx;

##### **16.1 XR70CX – 8A OR 16A COMP. RELAY - 230VAC OR 110VAC**

**NOTE:** The compressor relay is 8(3)A or 16(6)A according to the model. **24Vac supply** : connect to the terminals 5 and 6.

**16.2 XR70CX – 4 X 16A - 12VAC/DC**

#### **17. DEFAULT SETTING VALUES**

|**Label **|<br>**Name**|**Range**|**Value**|**Level **|
|---|---|---|---|---|
|**SEt**|Set point|LS; US<br>|-5.0|- - -|
|**HY**|Differential|[0.1 to 25.5°C]<br>[1to45°F]<br>|2.0|Pr1|
|**LS**|Minimum set point|[-100°C to SET]<br>[-148°Fto SET]|-50.0|Pr2|
|**US**|Maximum set point|[SET to 150°C]<br>[SETto 302°F]|110|Pr2|
|**ot**|Thermostat probe calibration|[-12.0 to 12.0°C]<br>[-21to21°F]|0.0|Pr1|
|**P2P**|Evaporatorprobe presence|n;Y|Y|Pr1|
|**oE**|Evaporator probe calibration|[-12.0 to 12.0°C]<br>[-21to21°F]|0.0|Pr2|
|**P3P**|Third probe presence|n;Y|n|Pr2|
|**o3**|Third probe calibration|[-12.0 to 12.0°C]<br>[-21to21°F]|0|Pr2|
|**P4P**|Fourthprobe presence|n;Y|n|Pr2|
|**o4**|Fourth probe calibration|[-12.0 to 12.0°C]<br>[-21to21°F]|0|Pr2|
|**odS**|Outputs delay at start up|0 to255min|0|Pr2|
|**AC**|Anti-short cycle delay|0 to 50min|1|Pr1|
|**rtr**|P1-P2percentagefor regulation|0 to100 (100=P1, 0=P2)|100|Pr2|
|**CCt**|Continuous cycle duration|0.0 to24h00min,res. 10min|0.0|Pr2|
|**CCS**|Set point for continuous cycle|[-100 to 150.0°C]<br>[-148 to 302°F]|-5|Pr2|

|**Labe **<br>**Con**|**l**<br>**Name**<br> CompressorONtimewith faultyprobe|**Range**<br>0to255min|**Value**<br>15|**Level **<br>Pr2|
|---|---|---|---|---|
|<br>**CoF**<br>|<br> CompressorOFFtimewith faulty probe<br>|<br>0 to255min<br>|30<br>|<br>Pr2<br>|
|**CF**<br>|Temperaturemeasurement unit<br>|°C;°F<br>|°C<br>|Pr2<br>|
|**rES**<br>**Lod**<br>**Ed**<sup>**2**</sup>|Resolution<br> Probe displayed<br> XREPdil|dE;in<br>P1;P2;P3;P4; SEt; dtr<br>P1P2P3P4SEtdt|dE<br>P1<br>P1|Pr1<br>Pr2<br>P2|
|**r** <br>|-spay<br>|; ; ; ; ; r<br>|<br>|r<br>|
|**dLY**<br>**dtr**|Display temperature delay<br>P1-P2percentagefordisplay|0.0 to20min00sec,res. 10 sec<br>1to 99|0.0<br>50|Pr2<br>Pr2|
|**tdF**|Defrosttype|EL;in|EL|Pr1|
|<br>**dFP**|<br> Probe selection fordefrost termination|<br>nP;P1;P2;P3;P4<br>|<br>P2|<br>Pr2|
|**dtE**|Defrost termination temperature|[-55 to 50.0°C]<br>[-67to122°F]|8|Pr1|
|**idF**<br>|Intervalbetweendefrost cycles<br>|0 to120hours<br>|6<br>|Pr1<br>|
|**MdF**<br>|(Maximum)length fordefrost<br>|0 to255min<br>|30<br>|Pr1<br>|
|**dSd**<br>**dFd**<br>**dAd**|Startdefrostdelay<br> Displaying during defrost<br> MAXdisplaydelayafterdefrost|0to255min<br>rt;it; SEt; dEF<br>0to255min|0<br>it<br>30|Pr2<br>Pr2<br>Pr2|
|<br>**Fdt**|<br>Diiti|<br>0t255i|0|<br>P2|
|<br>|ranng me<br>|o mn<br>||r<br>|
|**dPo**<br>**dAF**|First defrost afterstart-up<br> Defrost delay after fastfreezing|n;Y<br>0.0 to24h00min,res. 10min|n<br>0.0|Pr2<br>Pr2|
|**FnC**<br>**Fnd**<br>|Fanoperatingmode<br> Fandelay afterdefrost<br>|C-n; o-n; C-Y; o-Y<br>0 to255min<br>|o-n<br>10|Pr1<br>Pr1|
|**FCt**|<sup>Differential of temperature for forced</sup>|[0 to 50°C]|10|Pr2|
||<br>activationof fans|[0 to 90°F]|||
|**FSt**|Fan stop temperature|[-55 to 50.0°C]<br>[-67to122°F]|2|Pr1|
|**Fon**<br>**FoF**|Fanontimewithcompressoroff<br> Fanofftimewithcompressoroff|<br>0 to15min<br>0 to15min|0<br>0|Pr2<br>Pr2|
|**FAP**|Probe selection for fan management|nP;P1;P2;P3;P4|P2|Pr2|
|**ALC**|Temperat.alarms configuration|rE;Ab<br>°   °|Ab|Pr2|
|**ALU**|MAXIMUM temperature alarm|Rel: [0.0 to 50.0C] [0 to 90F]<br>AbS:[ALLto150°C] [ALLto 302°F]|<sup>110.0</sup>|Pr1|
|**ALL**|Minimum temperature alarm|Rel: [0.0 to 50.0°C] [0 to 90°F]<br>AbS: [-100°C to ALU] [-148°F to|-500|Pr1|
|||<br>ALU]|.||
|**AFH**|Differential for temperat. alarm recovery|<br>[0.1 to 25.5°C]<br>[1to45°F]|1.0|Pr2|
|**ALd**|Temperature alarmdelay|<br>0 to255min|15|Pr2|
|**dAo**<br>|Delay oftemperature alarmat start up<br>|0.0 to24h00min,res. 10min<br>|1.3<br>|Pr2<br>|
|**AP2**|Probefortemperat.alarmofcondenser|nP;P1;P2;P3;P4|P4|Pr2|
|**AL2**|Condenser for low temperat. alarm|[-100 to 150°C]<br>[-148 to 302°F]|-40|Pr2|
|**AU2**|Condenser for high temperat. alarm|[-100 to 150°C]<br>[-148to302°F]|110|Pr2|
|**AH2**|<sup>Differ. for condenser temp. alar.</sup><br>recovery|<br>[0.1 to 25.5°C]<br>[1to45°F]|5|Pr2|
|**Ad2**|Condensertemeraturealarmdela|0to254 min255(nu)|15|Pr2|
|<br>**dA2**|p  y<br> Delay ofcond.temper.alarmat start up|, <br>0.0 to24h00min,res. 10min|1.3|<br>Pr2|
|**bLL**|<sup>Compr. off for condenser low</sup>|Y||P2|
||<br>temperature alarm|n;|n|r|
|**AC2**|<sup>Compr. off for condenser high</sup><br>temeraturealarm|n; Y|n|Pr2|
|**tbA**|p  <br> Alarm relay disabling|n;Y|Y|Pr2|
|||ALr = alarm; dEF = do not select it;<br>LiG =Light; AUS =AUX; onF=always|||
|**oA3**|Fourth relay configuration|<br>on; FAn= do not select it; db = neutral<br>|<br>ALr|Pr2|
|||zone; CP2 = second compressor;<br>dF2 =donot selectit|||
|**AoP**|Alarm relay polarity (oA3=ALr)|oP; CL|CL|Pr2|
|**i1P**|Digital input polarity (18-19)|oP; CL<br>|CL|Pr1|
|**i1F**|Digital input configuration (18-19)|EAL; bAL; PAL; dor; dEF; ES; AUS;<br>Htr;FAn;HdF; onF|dor|Pr1|
|**did**|Digital input alarmdelay (18-20)|0 to255min|15|Pr1|
|**nPS**|Numberofactivationofpressure switch|0 to15|15|Pr2|
|<br>**odC**|<br> <sup>Compress and fan status when open</sup><br>d|no; FAn; CPr; F-C|F-C|Pr2|
|**rrd**|oor<br>Regulation restartwithdooropenalarm|n;Y|Y|Pr2|
|**HES**|Differential for Energy Saving|[-30 to 30°C]<br>[-54to54°F]|0|Pr2|
|**Adr**<br>|Serialaddress<br>|<br>0 to247|1|Pr2|
|**PbC**|Kind ofprobe|PtC;ntC|ntC|Pr2|
|**onF**<br>**dP1**|on/off key enabling<br> Rmrbdil|nu; oFF;ES<br>rb l|nu<br>|Pr2<br>Pr1|
|<br>**dP2**<br>**dP3**|oo poe spay<br> Evaporatorprobe display<br> Third probe display|poevaue<br>probevalue<br>probevalue|-<br>-<br>-|<br>Pr1<br>Pr1|
|**dP4**<br>**SE**|Fourthprobe display<br> Rlt|probevalue<br>tlt|-<br>|Pr1<br>P2|
|**r**<br>|ea se<br>|acua se<br>|-|r<br>|
|**rEL**<br>**Ptb**|Softwarerelease<br> Map code|read only<br>read only|-<br>-|Pr2<br>Pr2|
