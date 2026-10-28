# Dixell XW60K – - XW60K AND T620T - T620 – V620 – CX620 – - 1 GENERAL WARNING ........................................................................................

Kilde: `XW60K-GB.pdf` i denne mappe. Konverteret direkte fra PDF'en. Tabeller (parametre, alarmer, standardværdier) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra tegninger står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilket afsnit svaret kommer fra.
- Alarm- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer (Dixell, Danfoss, Carel). Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualen, så sig det i stedet for at gætte.

---

- XW60K AND T620T - T620 – V620 – CX620

- 1 GENERAL WARNING ............................................................................................................. 1 2 GENERAL DESCRIPTION ...................................................................................................... 1 3 CONTROLLING LOADS ......................................................................................................... 1 4 SPECIAL FUNCTIONS ........................................................................................................... 1 5 KEYBOARDS .......................................................................................................................... 1 6 AUTOMATIC KEYBOARD LOCK (ONLY FOR T620T) ........................................................... 2 7 CONTROLLER INTERFACE ................................................................................................... 2 8 PARAMETER LIST ................................................................................................................. 3 9 DIGITAL INPUT....................................................................................................................... 4 10 INSTALLATION AND MOUNTING .......................................................................................... 4 11 ELECTRICAL CONNECTIONS ............................................................................................... 5 12 TTL/RS485 SERIAL LINE ....................................................................................................... 5 13 HOW TO: USE OF THE PROGRAMMING “HOT KEY” ........................................................... 5 14 ALARM SIGNALS ................................................................................................................... 5 15 TECHNICAL DATA ................................................................................................................. 5 16 CONNECTIONS ...................................................................................................................... 5 17 DEFAULT SETTING VALUES ................................................................................................ 5

### **1 GENERAL WARNING**

#### **1.1 PLEASE READ BEFORE USING THIS MANUAL**

- This manual is part of the product and should be kept near the instrument for easy and quick reference.

- The instrument shall not be used for purposes different from those described hereunder. It cannot be used as a safety device.

- Check the application limits before proceeding.

- Dixell Srl reserves the right to change the composition of its products, even without notice, ensuring the same and unchanged functionality.

#### 1.2 Safety Precautions

- Check the supply voltage is correct before connecting the instrument.

- Do not expose to water or moisture: use the controller only within the operating limits avoiding sudden temperature changes with high atmospheric humidity to prevent  formation of condensation

- Warning: disconnect all electrical connections before any kind of maintenance.

- Fit the probe where it is not accessible by the End User. The instrument must not be opened.

- In case of failure or faulty operation send the instrument back to the distributor or to “Dixell S.r.l.” (see address) with a detailed description of the fault.

- Consider the maximum current which can be applied to each relay (see Technical Data).

- Ensure that the wires for probes, loads and the power supply are separated and far enough from each other, without crossing or intertwining.

- In case of applications in industrial environments, the use of mains filters (our mod. FT1) in parallel with inductive loads could be useful.

### **2 GENERAL DESCRIPTION**

Model **XW60K** is microprocessor based controller suitable for applications on medium or low temperature refrigerating units. It has to be connected by means of a two-wire cable ( 1mm) at a distance of up to 10 meters to the keyboard **T620T** or **T620** or **V620** or **CX620** . It is provided with four relay outputs to control compressor, defrost - which can be either electrical or hot gas - the evaporator fans and light. It is also provided with 4 NTC or PTC probe inputs, one for temperature control, one to control the defrost end temperature of the evaporator and the third and fourth to control condenser temperature or to display another temperature.

The HOT KEY output allows to connect the unit, by means of the external module XJ485-CX, to a network line **ModBUS-RTU** compatible such as the Dixell monitoring units of X-WEB family. It allows to program the controller by means the HOT KEY programming keyboard. The instrument is fully configurable through special parameters that can be easily programmed through the keyboard.

### **3 CONTROLLING LOADS**

#### **3.1 THE COMPRESSOR**

The regulation is performed according to the temperature measured by the thermostat probe with a positive differential from the set point: if the temperature increases and reaches set point plus differential the compressor is started and then turned off when the temperature reaches the set point value again.

In case of fault in the thermostat probe the start and stop of the compressor are timed through parameters **Con** and **CoF** .

The relay of the second compressor is activated in parallel with the relay of the first compressor, with a possible delay set in the **AC1** parameter. Both the compressors are switched off at the same time.

#### **3.2 FAST FREEZING**

When defrost is not in progress, it can be activated by holding the **UP** key pressed for about 3 sec. The compressor operates to maintain the **CCS** set point for the time set through the **CCt** parameter. The cycle can be terminated before the end of the set time using the same activation key **UP** for 3 sec.

#### **3.3 DEFROST**

Two defrost modes are available through the **tdF** parameter: defrost through electrical heater ( **tdF = EL** ) and hot gas defrost ( **tdF = in** ).

- The defrost interval depends on the presence of the RTC (optional). If the RTC is present is controlled by means of parameter **EdF** :

- **EdF=in:** a defrost starts after elapsing the **idF** time (standard way for controller without RTC). **EdF=rtC:** defrosts are scheduled by using a real time clock system, depending on the hours set in the parameters **Ld1..Ld6** , during workdays, and in **Sd1…Sd6** during holidays. Other parameters are used to control defrost cycles: its maximum length ( **MdF** ) and two defrost modes: timed or controlled by the evaporator’s probe ( **P2P** ). At the end of defrost dripping time is started, its length is set in the **Fdt** parameter. With **Fdt=0** the dripping time is disabled.

#### **3.4 CONTROL OF EVAPORATOR FANS**

The fan control mode is selected by means of the **FnC** parameter:

**FnC = C_n:** fans will switch ON and OFF with the compressor and **not run** during defrost; **FnC = o_n** fans will run even if the compressor is off, and not run during defrost; After defrost, there is a timed fan delay allowing for drip time, set by means of the **Fnd** parameter. **FnC = C_Y** fans will switch ON and OFF with the compressor and **run** during defrost; **FnC = o_Y** fans will run continuously also during defrost.

An additional parameter **FSt** provides the setting of temperature, detected by the evaporator probe, above which the fans are always OFF. This is used to make sure circulation of air only if his temperature is lower than set in **FSt** .

- **3.4.1 Forced activation for fans**

This function, managed by the **FCt** parameter, is designed to avoid short cycles of fans, that could happen when the controller is switched on or after a defrost, when the room air warms the evaporator. If the difference between the evaporator temperature and the room temperature is higher than the **FCt** value, the controller will activate the fans. This function is disabled if **FCt=0** .

**3.4.2 Timed activation of the fans when the compressor is off.**

When **FnC=C-n** or **C-Y** (fans in parallel to the compressor), the fans will be able to carry out on and off cycles even if the compressor is switched off. The on and off interval of time follow the **Fon** and **FoF** parameters. When the compressor is stopped the fans will go on working for the **Fon** time. On the other side, with **Fon=0** the fans will stay always off when the compressor is off.

### **4 SPECIAL FUNCTIONS**

By means of the parameter **oA3** , it’s possible to configure the functions of the light relay (22-23), as

described in the following paragraphs:

#### **4.1 LIGHT RELAY (FACTORY SETTING, OA3 = LIG)**

By setting **oA3=Lig** the relay will work as light relay, it is switched on and off by the light button on the keyboard and is affected by status of the digital input when **i1F=dor** .

- **4.2 SECOND COMPRESSOR MANAGEMENT (OA3 = CP2)**

By setting **oA3=CP2** , the relay at terminals 22-23 will operate as “second compressor”. It will be activated in parallel with the relay of the first compressor, with a possible delay set in the **AC1** parameter (seconds). Both the compressors are switched off at the same time.

- **4.3 ON –OFF RELAY  (OA3 = ONF)**

By setting **oA3=onF** , the relay will operate as “on-off” relay: it will be activated when the controller is switched on and it will be switched off when the controller is in stand-by status.

#### **4.4 AUXILIARY RELAY (OA3 = AUS)**

By setting **oA3=AUS** , the relay 22-23 will work as auxiliary thermostat (ex. anti condensing heater). **Parameters involved:**

- **ACH (cL, Ht):** Kind of regulation for the auxiliary relay: **Ht =** heating / **CL =** cooling **;**

- **SAA (-50÷150)** Set point for auxiliary relay

- **SHy (0÷25.5°C)** Differential for auxiliary output.

With ACH = CL: aux relay **cut in** is SAA+SHy, cut out SAA. With ACH = Ht: aux relay **cut in** is SAA-SHy, cut out SAA.

- **ArP (nP, P1, P2, P3, P4)** Probe for auxiliary relay

- **Sdd (n, Y)** Auxiliary output working during defrost

#### **4.5 ALARM RELAY (OA3 = ALR)**

By setting **oA3=ALr** the relay will work as alarm relay, it is switched on when an alarm happens. **Parameters involved:**

   - **tbA (n, y)** Alarm relay silencing

   - **AoP (cL; oP)** Alarm relay polarity

- **4.6 NEUTRAL ZONE (OA3 = DB)**

By setting **oA3=db** the controller will perform a

“neutral zone” regulation.

The heating element has to be connected to the **oA3** relay (22-23)

If the temperature increases and reaches set

point plus differential ( **HY** ) the **compresso** r is started and then turned off when the temperature reaches the set point value again. If the temperature decreases and reaches the set point minus differential ( **HY** ) the **oA3** output ( **heater** ) is switched on and then turned OFF when the temperature reaches again the set point.

### **5 KEYBOARDS**

##### **T620T**

##### **T620**

To display and modify target set point; in programming mode it selects a parameter or confirm an operation. By holding it pressed for 3 sec when max or min temperature is displayed it will be erased.

( **UP** ) To see the max stored temperature; in programming mode it browses the parameter codes or increases the displayed value. By holding it pressed for 3s the fast freezing cycle is started.

( **DOWN** ) To see the min stored temperature; in programming mode it browses the parameter codes or decreases the displayed value.

- ( **DEF** ) By holding it pressed for 3 sec the defrost is started.

( **LIG** ) Switch ON and OFF the cold room light.

( **ONOFF** ) Switch ON and OFF the instrument.

##### **KEY COMBINATIONS**

*[Figurtekst: +  To lock and unlock the keyboard. · +  To enter the programming mode. · +  To exit the programming mode.]*

#### **5.1 USE OF LEDS**

Each LED function is described in the following table.

|**LED**|**MODE**|**Function**|
|---|---|---|
||ON|The compressor is running|
||FLASHING|- Programming Phase (flashing with LED<br>)<br>- Anti-short cycle delayenabled|
||ON|The fan is running|
||FLASHING|Programming Phase (flashing with LED<br>)|
||ON|The defrost is enabled|
||FLASHING|Drip timeinprogress|
||ON|The Fast Freezing cycle is enabled|
||ON|- ALARM signal<br>- In “Pr2” indicates that the parameter is also presentin “Pr1”|
||ON|Continuous cycle is running|
||ON|Energysavingenabled|
||ON|Light on|
||ON|Auxiliaryrelay on(CX620 only)|
|**°C/°F**|ON|Measurement unit(CX620 only)|

### **6 AUTOMATIC KEYBOARD LOCK (ONLY FOR T620T)**

To avoid accidental modifications of the controller settings, **the T620T keyboard will be locked automatically if no key will be touched for 60 seconds.** The T620T will show “ **LoC** ” flashing for few seconds when it’s locking. The **light key** is operating even if the keyboard is locked.

#### **6.1 TO UNLOCK THE T620T**

1. Touch any key.

2. The keys will be lighted.

3. Keep a key pushed for few seconds till the “ **on** ” message is displayed.

### **7 CONTROLLER INTERFACE**

#### **SET THE CURRENT TIME AND DAY (ONLY WITH RTC)**

When the instrument is switched on, it’s necessary to program the time and day.

1. Enter the Pr1 programming menu, by pushing the **SET+ DOWN** keys for 3 sec.

2. The **rtC** parameter is displayed. Push the **SET** key to enter the real time clock menu.

3. The **Hur** (hour) parameter is displayed.

4. Push the **SET** and set current hour by the **UP** and **DOWN** keys, then push **SET** to confirm the value.

5. Repeat the same operations with **Min** (minutes), **dAy** (day), **dYM** (day of month), **Mon** (month) and **YAr** (year) parameters.

**To exit:** Push both **SET+UP** keys or wait for 15 sec without pushing any keys.

- **7.1 HOW TO SEE THE MIN TEMPERATURE**

1. Press and release the **DOWN** key.

2. The “Lo” message will be displayed followed by the minimum temperature recorded.

3. By pressing the **DOWN** key or waiting for 5 sec the normal display will be restored.

- **7.2 HOW TO SEE THE MAX TEMPERATURE**

1. Press and release the **UP** key.

2. The “Hi” message will be displayed followed by the maximum temperature recorded.

3. By pressing the **UP** key or waiting for 5 sec the normal display will be restored.

- **7.3 HOW TO RESET THE MAX AND MIN TEMPERATURE RECORDED**

- To reset the stored temperature, when max or min temperature is displayed:

1. Press **SET** key until “rST” label starts blinking.

**Note: after the installation remember to RESET the temperature stored.**

- **7.4 HOW TO SEE AND MODIFY THE SET POINT**

1. Push and immediately release the **SET** key: the display will show the Set point value;

2. To change the **SEt** value, push the **UP** or **DOWN** arrows within 10 sec.

3. To memorise the new set point value push the **SET** key again or wait for 10 sec.

- **7.5 TO START A MANUAL DEFROST**

   1. Push the **DEF** key for more than 2 sec and a manual defrost will start.

- **7.6 TO ENTER IN PARAMETERS LIST “PR1”**

To enter the parameter list “Pr1” (user accessible parameters) operate as follows:

1. Enter the Programming mode by pressing the Set and DOWN key

<sup>+</sup> for few seconds ( and<sup>start blinking).</sup> 2. The instrument will show the first parameter present in “Pr1”

#### **7.7 THE HIDDEN MENU**

In the hidden menu there are all the parameters of the instrument.

- **7.7.1 ENTERING THE HIDDEN MENU**

1. Enter the Programming mode by pressing the **SET+DOWN** keys for 3 sec (the “ **°C** ” or “ **°F** ” LED will start blinking).

2. Release the keys and then push again the **SET+DOWN** keys more than 7 sec. The “ **Pr2** ” label will be displayed immediately, followed from the **HY** parameter.

**NOW THE HIDDEN MENU IS DISPLAYED**

3. Select the required parameter.

4. Press **SET** key to display its actual value

5. Use **UP** or **DOWN** keys to change its value.

6. Press **SET** to store the new value and move to the following parameter.

**To exit** : Press **SET+UP** or wait for 15 sec without pressing any key.

**NOTE1:** if no parameter is present in the “ **Pr1** ” level, after the first 3 sec the “ **noP** ” message will be displayed. Keep **SET+DOWN** keys pushed till the “ **Pr2** ” message will be displayed.

**NOTE2** : the new set value will be stored even if the procedure is exited by waiting for the time-out to expire.

##### **7.7.2 HOW TO: MOVE A PARAMETER FROM THE HIDDEN MENU TO THE FIRST LEVEL AND VICEVERSA.**

Each parameter present in the HIDDEN MENU can be moved or put into “THE FIRST LEVEL” (user level) by pressing **SET+DOWN** keys. In HIDDEN MENU, if a parameter is present also in the First Level (Pr1), the decimal point will be lit.

##### **7.7.3 HOW TO CHANGE THE PARAMETER VALUE**

1. Enter the Programming mode.

2. Select the required parameter with **UP** or **DOWN** .

3. Press the “ **SET** ” key to display its value ( and LED starts blinking).

4. Use **UP** or **DOWN** to change its value.

5. Press **SET** to store the new value and move to the following parameter. **To exit** : Press **SET+UP** or wait for 15 sec without pressing any key.

**NOTE** : the new programming is stored even when the procedure is exited by waiting the time-out.

- **7.8 HOW TO LOCK THE KEYBOARD (MANUALLY)**

   1. Keep the **UP** and **DOWN** keys pressed together for more than 3 sec the **UP** and **DOWN** keys.

2. The “PoF” message will be displayed and the keyboard is locked. At this point it is only possible the viewing of the set point or the MAX o Min temperature stored and

+ to switch ON and OFF the light, the auxiliary output and the instrument.

##### **<u>TO UNLOCK THE KEYBOARD</u>**

Keep the **UP** and **DOWN** keys pressed together for more than 3 sec.

#### **7.9 ON/OFF FUNCTION (STAND BY)**

By pushing the **ON/OFF** key, the instrument shows “OFF” for 5 sec. and the ON/OFF LED is switched ON.

During the OFF status, all the relays are switched OFF and the regulations are stopped; if a monitoring system is connected, it does not record the instrument data and alarms. When the instrument is in stand by the keyboard displays “oFF”.

**N.B. During the OFF status the Light and AUX buttons are active.**

#### **7.10 TO SEE THE PROBE VALUES**

1. Enter in “ **Pr1** ” level. 2. Parameters “dP1”, “dP2”, “dP3” and “dP4” display the value of probes 1, 2, 3 and 4.

### **8 PARAMETER LIST**

|**rtC**<br>**REGULA**|**Real time clock menu (only for controller with RTC):**to set the time, date and defrost<br>start time.<br>**TION**|
|---|---|
|**HY**|**Differential:**(0.1 to 25.5°C; 1 to 45°F) intervention differential for set point. Compressor<br>Cut IN is Set Point + differential (**HY**). Compressor Cut OUT is when the temperature<br>reaches the setpoint.|
|**LS**|**Minimum set point:**(-55°C to SET; -67°F to SET) sets the minimum value for the set<br>point.|
|**US**<br>**ot**|**Maximum setpoint:** (SET to 150°C;SET to 302°F)set the maximum value for setpoint.<br>**Thermostat probe calibration:**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible<br>offset of the thermostatprobe.|
|**P2P**|**Evaporator probe presence:**(n; Y)**n**= not present, the defrost stops by time;<br>**Y**=presentthe defrost stops bytemperature.|
|**oE**|,    <br>**Evaporator probe calibration:**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible<br>offset of the evaporatorprobe.|
|**P3P**|<br>**Third probe presence (P3):**(n; Y)**n**= not present, the terminals 18-20 operate as digital<br>input; **Y**=present,the terminals 18-20 operate as thirdprobe.|
|**o3**|**Third probe calibration (P3):**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible<br>offset of the thirdprobe.|
|**P4P**|**Fourth probe presence:**(n; Y) n = Not present; Y = present.<br>**NOTE:** onlyfor**XW60LT**models.|
|**o4**|**Fourth probe calibration:**(-12.0 to 12.0°C; -21 to 21°F) allows to adjust possible offset<br>of the fourth probe.<br>**NOTE:**onlyfor**XW60LT**models.|
|**odS**|**Outputs activation delay at start up:**(0 to 255min) this function is enabled at the initial<br>start up of the instrument and inhibits any output activation for the period of time set in the<br>parameter.|
|**AC**|**Anti-short cycle delay:**(0 to 50min) minimum interval between the compressor stop and<br>thefollowingrestart.|
|**rtr**|**Percentage of the second and first probe for regulation:**(0 to 100; 100=P1, 0=P2) it<br>allows to set the regulation according to the percentage of the first and second probe, as<br>for the followingformula(**rtr**(P1-P2)/100 + P2).|
|**CCt**<br>**CCS**|**Compressor ON time during continuous cycle:**(0.0 to 24h00min, res. 10min) allows to<br>set the length of the continuous cycle. Compressor stays on without interruption during<br>**CCt**time. This is useful,for instance,when the room is filled with newproducts.<br>**Set point for continuous cycle:**(-55 to 150°C; -67 to 302°F) it sets the set point used<br>duringthe continuous cycle|
|**Con**|.<br>**Compressor ON time with faulty probe:**(0 to 255min) time during which the<br>compressor is active in case of faulty thermostat probe. With**Con=0**compressor is<br>always OFF|
|**CoF**|.<br>**Compressor OFF time with faulty probe:**(0 to 255min) time during which the<br>compressor is OFF in case of faulty thermostat probe. With**CoF=0**compressor is always<br>|
||active.|
|**DISPLAY**||
|**CF**|**Temperature measurement unit:**(°C; °F)**°C**= Celsius;**°F**= Fahrenheit.<br>**WARNING:**When the measurement unit is changed the SET point and the values of<br>the parameters**HY**,**LS**,**US**,**ot**,**ALU**and**ALL**have to be checked and modified (if<br>necessary)|
|**rES**|.<br>**Resolution(for °C):** (in=1°C;dE=0.1°C)allows decimalpoint display.|
|**Lod**|**Instrument display:**(P1; P2, P3, P4, SET, dtr) it selects which probe is displayed by<br>the instrument.**P1**= Thermostat probe;**P2**= Evaporator probe;**P3**= Third probe (only<br>for model with this option enabled);**P4**= Fourth probe,**SET**= set point;**dtr**=<br>percentage of visualization|
|**rEd**|.<br>**X-REP display (optional):**(P1; P2, P3, P4, SET, dtr) it selects which probe is<br>displayed by X- REP.**P1**= Thermostat probe;**P2**= Evaporator probe;**P3**= Third probe<br>(only for model with this option enabled);**P4**= Fourth probe,**SET**= set point;<br>**dtr**=percentage of visualization.|
|**dLY**|**Display delay:**(0 to 20min00s; res. 10s) when the temperature increases, the display<br>isupdatedof 1°Cor 1°Fafterthistime.|
|**dtr**|<br>**Percentage of the second and first probe for visualization when Lod=dtr:**(0 to 99;<br>100=P1, 0=P2) if**Lod=dtr**it allows to set the visualization according to the percentage<br>of the first and secondprobe,as for the followingformula(**dtr**(P1-P2)/100 + P2).|

|**DEFROS**<br>**EdF**|**T**<br>**Defrost mode (only for controller with RTC):**|
|---|---|
||<br>- **rtC:** **Real Time Clock mode**. Defrost time follows**Ld1 to Ld6**parameters on<br>workdays and**Sd1 to Sd6**on holidays.<br>- **in:** **interval mode**. The defrost starts when the time**idf**is expired.|
|**tdF**<br>**dFP**|**Defrost type:** (EL;in) **EL**= electrical heater; **in**= hotgas.<br>**Probe selection for defrost termination:**(nP; P1; P2; P3; P4)**nP**= no probe;<br>**P1**=thermostat probe;**P2**= evaporator probe;**P3**=configurable probe;**P4**= Probe on<br>Hot Key plug.|
|**dtE**|**Defrost termination temperature:**(-55 to 50°C; -67 to 122°F) (enabled only when<br>**EdF=Pb**) sets the temperature measured by the evaporator probe, which causes the<br>end of defrost|
|**idF**|.<br>**Interval between defrost cycles:**(0 to 120hours) determines the interval of time<br>between two defrost cycles.|
|**MdF**|**(Maximum) length for defrost:**(0 to 255min) when**P2P=n**, (not evaporator probe:<br>timed defrost) it sets the defrost duration. When**P2P=Y**(defrost end based on<br>temperature)it sets the maximum length for defrost.|
|**dSd**|**Start defrost delay:**(0 to 99min) this is useful when different defrost start times are<br>necessarto avoid overloadinthelant|
|**dFd**|y g p.<br>**Temperature displayed during defrost:**(rt; it; SEt; dEF)**rt**= real temperature;<br>**it**= tt t dft tt**SEt**= tit**dEF**= “**dEF**” lbl|
|**dAd**|emperaure a eros sar; sepon;  ae.<br>**MAX display delay after defrost:**(0 to 255min) sets the maximum time between the<br>end of defrost and the restartinof the real room temerature disla|
|**Fdt**|g p py.<br>**Drip time:**(0 to 120min) time interval between reaching defrost termination temperature<br>and the restoring of the control’s normal operation. This time allows the evaporator to<br>eliminate water drops that might have formed due to defrost.|
|**dPo**<br>**dAF**|**First defrost after start-up:** (n;Y) **n**= after the**idF**time, **Y**= immediately.<br>**Defrost delay after continuous cycle:**(0.0 to 24h00min, res. 10min) time interval<br>between the end of the fast freezingcycle and the followingdefrost related to it.|
|**FANS**||
|**FnC**|**Fans operating mode:**(C-n; o-n; C-Y; o-Y)**C-n**= runs with the compressor, OFF during<br>defrost;**o-n**= continuous mode, OFF during defrost;**C-Y**= runs with the compressor, ON<br>|
|**Fnd**|duringdefrost; **o-Y**= continuous mode,ON duringdefrost.<br>**Fans delay after defrost:**(0 to 255min) interval between end of defrost and evaporator<br>f|
|**FCt**|ans start.<br>**Temperature differential to avoid fan short cycles:**(0 to 59°C; 0 to 90°F) (N.B.:**FCt=0**<br>means function disabled) if the difference of temperature between the evaporator and the<br>roomprobes is higher than**FCt**valuethe fans will be switched on.|
|**FSt**|, <br>**Fans stop temperature:**(-55 to 50°C; -67 to 122°F) setting of temperature, detected by<br>evaoratorrobeabove which fans are alwas OFF|
|**Fon**<br>**FoF**|p p, y.<br>**Fan ON time:**(0 to 15min) with**Fnc=C_n**or**C_Y**, (fan activated in parallel with<br>compressor) it sets the evaporator fan ON cycling time when the compressor is off. With<br>**Fon=0**and**FoF≠0**the fan are always off,with**Fon=0**and**FoF=0**the fan are always off.<br>**Fan OFF time:**(0 to 15min)<br>With**FnC=C_n**or**C_Y**, (fan activated in parallel with compressor) it sets the evaporator<br>fan off cycling time when the compressor is off.<br>With**Fon=0**and**FoF≠0**the fan are always off, with**Fon=0**and**FoF=0**the fan are always<br>|
|**FAP**|off.<br>**Probe selection for fan management:**(nP; P1; P2; P3; P4)**nP**= no probe;<br>**P1**=thermostat probe;**P2**= evaporator probe;**P3**=configurable probe;**P4**= Probe on Hot<br>Key plug.|
|**OA3 = A**<br>|**US: AUXILIARY THERMOSTAT CONFIGURATION(terms. 22-23)**<br>|
|**ACH**<br>**SAA**|**Kind of regulation for auxiliary relay:** (Ht;CL) **Ht**= heating; **CL**= cooling.<br>**Set Point for auxiliary relay:**(-55.0 to 150.0°C; -67 to 302°F) it defines the room<br>|
|**SHY**<br>**ArP**|temperature setpoint to switch auxiliaryrelay.<br>**Differential for auxiliary output:**(0.1 to 25.5°C; 1 to 45°F) intervention differential for<br>auxiliary output set point.<br><br>**ACH=CL**, AUX Cut in is [**SAA+SHY**]; AUX Cut out is**SAA**.<br><br>**ACH=Ht**,AUX Cut in is[**SAA–SHY]**;AUX Cut out is**SAA**.<br>**Probe selection for auxiliary:**(nP; P1; P2; P3; P4)**nP**= no probe, the auxiliary relay is<br>switched only by the digital input;**P1**= Probe 1 (Thermostat probe);**P2**= Probe 2<br>tb**P3**= Pb 3dilb**P4**= Pb 4|
|**Sdd**|(evaporaorproe); roe(spay proe); roe .<br>**Auxiliary relay off during defrost:**(n; Y)**n**= the auxiliary relay operates during defrost.<br>**Y**= the auxiliaryrelayis switched off duringdefrost.|
|**ALARMS**||
|**ALP**|**Probe selection for alarm:**(nP; P1; P2; P3; P4)**nP**= no probe, the temperature alarms<br>are disabled;**P1**= Probe 1 (Thermostat probe);**P2**= Probe 2 (evaporator probe);<br>**P3**= Probe 3(displayprobe);**P4**= Fourthprobe|
|**ALC**|.<br>**Temperature alarms configuration:**(Ab; rE)**Ab**= absolute temperature, alarm<br>temperature is given by the**ALL**or**ALU**values.**rE**= temperature alarms are referred to<br>the set point. Temperature alarm is enabled when the temperature exceeds the<br>[**SET+ALU**]or[**SET-ALL**]values|
|**ALU**|.<br>**MAXIMUM temperature alarm:**<br><br>If**ALC=Ab**: [ALL to 150.0°C or ALL to 302°F]<br><br>If**ALC=rE**: [0.0 to 50.0°C or 0 to 90°F]<br>when this temperature is reached the alarm is enabled,after the**ALd**delaytime.|
|**ALL**|**Minimum temperature alarm:**<br><br>If**ALC=Ab**: [-55°C to ALU; -67 to ALU]<br><br>If**ALC=rE**: [0.0 to 50.0°C or 0 to 90°F]<br>when this temperature is reached the alarm is enabledafter the**ALd**delatime|
|**AFH**|,  y.<br>**Differential for temperature alarm recovery:**(0.1 to 25.5°C; 1 to 45°F) intervention<br>difftil ff tt l|
|**ALd**|erena or recoveryo emperaure aarm.<br>**Temperature alarm delay:**(0 to 255 min) time interval between the detection of an alarm<br>nditin nd lrm inllin|
|**dAo**|coo a aa sgag.<br>**Exclusion of temperature alarm at start-up:**(0.0 to 24h00min, res. 10min) time interval<br>between the detection of the temperature alarm condition after instrument power on and<br>alarm signalling.|

|**CONDEN**<br>|**SER TEMPERATURE ALARM**<br>|
|---|---|
|**AP2**|**Probe selection for temperature alarm of condenser:**(nP; P1; P2; P3; P4)<br>**nP**= no probe;**P1**= thermostat probe;**P2**= evaporator probe;**P3**= configurable probe;<br>**P4**= Pb  Ht Kl|
|**AL2**<br>**Au2**|roe on o ey pug.<br>**Low temperature alarm of condenser:**(-55 to 150°C; -67 to 302°F) when this<br>temperature is reached the**LA2**alarm is signalled, possiblyafter the Ad2 delay.<br>**High temperature alarm of condenser:**(-55 to 150°C; -67 to 302°F) when this<br>temperature is reached the**HA2**alarm is signalled, possiblyafter the**Ad2**delay.|
|**AH2**<br>**Ad2**|**Differential for temperature condenser alarm recovery:**0.1 to 25.5°C;1 to 45°F.<br>**Condenser temperature alarm delay:**(0 to 255 min) time interval between the detection<br>of the condenser alarm condition and alarm signalling.|
|**dA2**<br>**bLL**|**Condenser temperature alarm exclusion at start up:**0.0 to 24h00min,res. 10min.<br>**Compressor off with low temperature alarm of condenser:**(n; Y)**n**= compressor<br>keeps on working;**Y**= compressor is switched off till the alarm is present, in any case<br>regulation restarts after**AC**time at minimum|
|**AC2**|.<br>**Compressor off with high temperature alarm of condenser:**(n; Y)**n**= compressor<br>keeps on working;**Y**= compressor is switched off till the alarm is present, in any case<br>regulation restarts after**AC**time at minimum.|
|**RELAY**|**OA3(22-23) CONFIGURATION**|
|**tbA**|**Alarm relay silencing (with oAx =ALr):**(n; Y)**n**= silencing disabled: alarm relay stays<br>on till alarm condition lasts.**Y**= silencing enabled: alarm relay is switched OFF by<br>pressinga keyduringan alarm.|
|**oA3**|**Third relay configuration (X60LT: terminals 1-3, XW60LRT: terminals 5-6):**(dEF;<br>FAn; ALr; LiG; AUS; onF; db; dEF2; HES)**dEF**= defrost;**FAn**= do not select it;**ALr**=<br>alarm;**LiG**= light;**AUS**= Auxiliary relay;**onF**= always on with instrument on;**db**=<br>neutral zone**dEF2**=donotselectit**HES**= nihtblind|
|**AoP**|;     ;  g .<br>**Alarm relay polarity:**(CL; oP) it set if the alarm relay is open or closed when an alarm<br>occurs.**CL**= terminals closed duringan alarm; **oP**= terminals open duringan alarm.|
|**DIGITAL**|**INPUT**|
|**i1P**|**First digital input polarity:**(oP; CL)**oP**= the digital input is activated by opening the<br>contact;**CL**= the digital input is activated byclosingthe contact.|
|**i1F**<br>**did**|<br>**First digital input configuration:**(EAL; bAL; PAL; dor; dEF; ES; AUS; Htr; FAn; HdF;<br>onF; Sbt)**EAL**= external alarm: “**EA**” message is displayed;**bAL**= serious alarm “**CA**”<br>message is displayed;**PAL**= pressure switch alarm, “**CA**” message is displayed;**dor**=<br>door switch function;**dEF**= activation of a defrost cycle;**ES**= energy saving;**AUS**=<br>auxiliary relay activation with**oA2=AUS**;**Htr**= type of inverting action (cooling or heating);<br>**FAn**= fan;**HdF**= Holiday defrost (enable only with RTC);**onF**= to switch the controller<br>off; **Sbt**= to activate Sabbath mode.<br>**Digital input 1 alarm delay:**(0 to 255 min) delay between the detection of the external<br>alarm condition and its signalling.<br>When**i1F= PAL**, it is the interval of time to calculate the number of pressure switch<br>titi|
|**nPS**|acvaon.<br>**Number of pressure switch activation:**(0 to 15) Number of activation, during the**did**or<br>**d2d**interval, before signalling an alarm event (**i1F, i2F=PAL**).<br>If the**nPS**activation during**did**or**d2d**time is reached, switch off and on the instrument to<br>restart normal regulation.|
|**odC**<br>**rrd**|**Compressor status when open door:**(no; FAn; CPr;F_C;)**no**= normal;<br>**FAn**= normal; **CPr**= compressor OFF, **F_C**= compressor OFF.<br>**Outputs restart after door open alarm:**(n; Y)**n**= outputs follow the**odC**parameter.<br>**Y**= outputs restart with a door open alarm.|
|**LES**<br>**HES**|**Light off during Energy Saving status:**n;Y.<br>**Delta temperature during an Energy Saving cycle:**(-30.0 to 30.0°C; -54 to 54°F) it<br>sets the increasingvalue of the setpoint**[SET+HES]**duringthe EnergySavingcycle.|
|**CURREN**|**T TIME AND WEEKLY HOLIDAYS(ONLY FOR MODELS WITH RTC)**|
|**Hur **|**Current hour:**0 to23h.|
|**Min**|**Current minute:**0 to 59min.|
|**dAY**<br>**dYM**<br>**Mon**|**Current day:**Sun to SAt.<br>**Day of the month:**1 to 31.<br>**Month:**1 to 12|
|<br>**YAr**<br>**Hd1**|.<br>**Year:**00 to 99.<br>**First weekly holiday:**(Sun to nu) set the first day of the week which follows the holiday<br>i|
|**Hd2**|tmes.<br>**Second weekly holiday:**(Sun to nu) set the second day of the week which follows the<br>|
|**N.B.: Hd**|holidaytimes.<br>**1, Hd2**can be set also as**“nu”**value (Not Used).|
|**ENERGY**|**SAVING TIMES(ONLY FOR MODELS WITH RTC)**|
|**ILE**|**Energy Saving cycle start during workdays:**(0 to 23h50min) during the Energy Saving<br>cycle the set point is increased by the value in HES so that the operation set point is<br>**SET+HES**|
|**dLE**|.<br>**Energy Saving cycle length during workdays:**(0 to 24h00min) sets the duration of the<br>ESi l  kd|
|**ISE**<br>**dSE**|nergyavngcyce on worays.<br>**Energy Saving cycle start on holidays:**0 to 23h50min.<br>**Energy Saving cycle length on holidays:**0 to 24h00min.|
|**TO SET**|**DEFROST TIMES(ONLY FOR MODELS WITH RTC)**|
|**Ld1...L**|**d6**<br>**Workday defrost start:**(0 to 23h50min) these parameters set the beginning of the<br>6 programmable defrost cycles during workdays. Ex: when**Ld2=12.4**the second|
|**Sd1...S**|<br>defrost starts at 12.40 duringworkdays.<br>**d6**<br>**Holiday defrost start:**(0 to 23h50min) these parameters set the beginning of the 6<br>programmable defrost cycles on holidays. Ex: when**Sd2=3.4**the second defrost<br>starts at 3.40 on holidays.|
|**N.B.:to**|**disable a defrost cycle set it to“nu” (not used).**|
|**OTHER**||
|**Adr**|**Serial address:**(1 to 247) identifies the instrument address when connected to a<br>ModBUS compatible monitoringsystem.|

|**PbC**|**Type of probe:**(PtC; ntC) it allows to set the kind of probe used by the instrument:<br>-<br>**PtC**= PTC probe;<br>-<br>**ntC**= NTC probe.|
|---|---|
|**onF**|**On/Off key enabling:** (nU;oFF;ES) **nU**= disabled; **oFF**= enabled; **ES**= not set it.|
|**dP1**|Thermostatprobe display.|
|**dP2**|Evaporatorprobe display.|
|**dP3**|Thirdprobe display.|
|**dP4**|Fourthprobe display (onlyfor XW60LT models).|
|**rSE**|Real set point: it shows the set point used during the energy saving cycle or during the<br>continuous cycle.|
|**rEL**|Software release for internal use.|
|**Ptb**|Parameter table code: readable only.|

### **9 DIGITAL INPUT**

The free voltage digital input is programmable in different configurations by the **i1F** parameter.

#### **9.1 DOOR SWITCH INPUT  (I1F = DOR)**

It signals the door status and the corresponding relay output status through the **odC** parameter: **no** = normal (any change); **Fan** = Fan OFF; **CPr** = Compressor OFF; **F_C** = Compressor and fan OFF. Since the door is opened, after the delay time set through parameter **did** , the door alarm is enabled, the display shows the message “ **dA** ” and **the regulation restarts is rtr = yES.** The alarm stops as soon as the external digital input is disabled again. With the door open, the high and low temperature alarms are disabled.

#### **9.2 GENERIC ALARM (I1F = EAL)**

As soon as the digital input is activated the unit will wait for **did** time delay before signalling the “ **EAL** ” alarm message. The outputs status doesn’t change. The alarm stops just after the digital input is deactivated.

#### **9.3 SERIOUS ALARM MODE (I1F = BAL)**

When the digital input is activated, the unit will wait for **did** delay before signalling the “ **CA** ” alarm message. The relay outputs are switched OFF. The alarm will stop as soon as the digital input is deactivated.

#### **9.4 PRESSURE SWITCH (I1F = PAL)**

If during the interval time set by **did** parameter, the pressure switch has reached the number of activation of the **nPS** parameter, the “ **CA** ” pressure alarm message will be displayed. The compressor and the regulation are stopped. When the digital input is ON the compressor is always OFF. **If the nPS activation in the did time is reached, switch off and on the instrument to restart normal regulation.**

#### **9.5 AUXILIARY OUTPUT SWITCHING  (I1F =AUS)**

With **oA3=AUS** and **i1F=AUX** it switches the fourth relay (22-23).

#### **9.6 START DEFROST (I1F = DFR)**

It starts a defrost if there are the right conditions. After the defrost is finished, the normal regulation will restart only if the digital input is disabled otherwise the instrument will wait until the **MdF** safety time is expired.

- **9.7 KIND OF ACTION: HEATING OR COOLING (I1F = HTR)**

This function allows to invert the regulation of the controller: from cooling to heating and viceversa.

- **9.8 ENERGY SAVING (I1F = ES)**

The Energy Saving function allows to change the set point value as the result of the **SET+HES** (parameter) sum. This function is enabled until the digital input is activated.

#### **9.9 DIGITAL INPUTS POLARITY**

The digital input polarity depends on the **i1P** parameter: **i1P=CL** : the input is activated by closing the contact. **i1P=OP** : the input is activated by opening the contact

### **10 INSTALLATION AND MOUNTING**

**T620** keyboard shall be mounted on vertical panel, in a 150x31 mm hole, and fixed using two screws  3 x 2mm. To obtain an IP65 protection grade use the front panel rubber gasket (mod. RG-L). **V620** keyboard shall be mounted on vertical panel, in a 72x56 mm hole, and fixed using two screws  3 x 2mm. To obtain an IP65 protection grade use the front panel rubber gasket (mod. RG-V). **CX620** keyboard shall be mounted on vertical panel, in a 29x71 mm hole, and fixed using the special bracket supplied.

The controller **XW60K** shall be mounted in a din rail

It must be connected to the keyboard by means of a two-wire cable ( 1mm). The temperature range allowed for correct operation is 0 to 60°C. Avoid places subject to strong vibrations, corrosive gases, excessive dirt or humidity. The same recommendations apply to probes. Let the air circulate by the cooling holes.

#### **10.1 XW60K – 8 DIN CASE - DIMENSIONS**

### **11 ELECTRICAL CONNECTIONS**

**XW60K** is provided with screw terminal blocks to connect cables with a cross section up to 2.5 mm<sup>2</sup> for the RS485 (optional) and the keyboard. To connect the other inputs, power supply and relays, **XW60K** is provided with Faston connections (6.3mm). Heat-resistant cables have to be used. Before connecting cables make sure the power supply complies with the instrument’s requirements. Separate the probe cables from the power supply cables, from the outputs and the power connections. Do not exceed the maximum current allowed on each relay, in case of heavier loads use a suitable external relay.

**NOTE: the maximum current allowed for all the loads is 20A.**

#### **11.1 PROBE CONNECTIONS**

The probes shall be mounted with the bulb upwards to prevent damages due to casual liquid infiltration. It is recommended to place the thermostat probe away from air streams to correctly measure the average room temperature. Place the defrost termination probe among the evaporator fins in the coldest place, where most ice is formed, far from heaters or from the warmest place during defrost, to prevent premature defrost termination.

### **12 TTL/RS485 SERIAL LINE**

The TTL connector allows, by means of the external module TTL/RS485 **(XJ485CX)** , to connect the unit to a network line **ModBUS-RTU** compatible as the Dixell monitoring system. The same TTL connector is used to upload and download the parameter list of the “ **HOT-KEY** ”.

### **13 HOW TO: USE OF THE PROGRAMMING “HOT KEY”**

#### **13.1 PROGRAM A HOT-KEY FROM AN INSTRUMENT (UPLOAD)**

1. Program one controller with the front keypad.

2. When the controller is <u>ON, insert the “</u> **HOT-KEY** ” and push **UP** button; the “ **uPL** ” message appears followed a by a flashing “ **End** ” label.

3. Push **SET** button and the “ **End** ” will stop flashing.

4. <u>Turn OFF the instrument, remove the “</u> **HOT-KEY** ” and then turn it ON again.

**NOTE** : the “ **Err** ” message appears in case of a failed programming operation. In this case push again

button if you want to restart the upload again or remove the “ **HOT-KEY** ” to abort the operation.

#### **13.2 PROGRAM AN INSTRUMENT BY USING A HOT-KEY (DOWNLOAD)**

1. Turn OFF the instrument.

2. Insert a **pre-programmed** “ **HOT-KEY** ” **into the 5-PIN receptacle** and then turn the Controller ON.

3. The parameter list of the “ **HOT-KEY** ” will be automatically downloaded into the Controller memory. The “ **doL** ” message will blink followed a by a flashing “ **End** ” label.

4. After 10 seconds the instrument will restart working with the new parameters.

5. Remove the “ **HOT-KEY** ”.

**NOTE:** the message “ **Err** ” is displayed for failed programming. In this case turn the unit off and then on if you want to restart the download again or remove the “ **HOT-KEY** ” to abort the operation.

### **14 ALARM SIGNALS**

|**Message **|**Cause**|**Outputs**|
|---|---|---|
|P1|Thermostat probe failure|Alarm output ON; Compressor output according to<br>parameters**Con**and**CoF**.|
|P2|Evaporatorprobe failure|Alarm output ON;Other outputs unchanged|
|P3|Probe 3probe failure|Alarm output ON;Other outputs unchanged|
|P4|Probe 4probe failure|Alarm output ON;Other outputs unchanged|
|HA|Maximum temperature alarm|Alarm output ON;Other outputs unchanged|
|LA|Minimum temperature alarm|Alarm output ON;Other outputs unchanged|
|HA2|Condenser hightemperature|It depends onthe **AC2** parameter|
|LA2|Condenser low temperature|It depends on the**bLL** parameter<br>|
|dA|Door open|Compressor and fans restarts|
|EA|External alarm|Output unchanged.|
|CA|Serious external alarm(i1F=bAL)|All outputs OFF.|
|CA|Pressure switchalarm(i1F=PAL)|Alloutputs OFF|
|EE|Data or memoryfailure|Alarm output ON;Other outputs unchanged|

The alarm message is displayed until the alarm condition is recovery.

All the alarm messages are showed alternating with the room temperature except for the “P1” which is flashing.

To reset the “EE” alarm and restart the normal functioning press any key, the “ **rSt** ” message is displayed for about 3 sec.

#### **14.1 SILENCING BUZZER**

Once the alarm signal is detected the buzzer can be silenced by pressing any key. Buzzer is mounted in the keyboard and it is an option.

#### **14.2 “EE” ALARM**

The Dixell instruments are provided with an internal check for the data integrity. The “EE” alarm flashes when a failure in the memory data occurs. In such cases the alarm output is enabled.

#### **14.3 ALARM RECOVERY**

Probe alarms: “ **P1** ” (probe1 faulty), “ **P2** ”, “ **P3** ” and “ **P4** ”; they automatically stop 10 sec after the probe restarts normal operation. Check connections before replacing the probe. Temperature alarms “ **HA** ”, “ **LA** ” “ **HA2** ” and “ **LA2** ” automatically stop as soon as the temperature returns to normal values. Alarms **“EA”** and **“CA”** (with **i1F=bAL** ) recover as soon as the digital input is disabled. Alarm “ **CA”** (with **i1F=PAL** ) recovers only by **switching off and on** the instrument.

### **15 Technical data**

##### **<u>Keyboards</u>**

**Housing:** self extinguishing ABS **Case: T620 and T620T:** facia 38x185 mm; depth 23mm **V620:** facia 72x56 mm; depth 23mm

**CX620:** facia 75x36 mm; depth 23mm

**Mounting: T620T** panel mounting in a 150x31 mm panel cut-out with the 2 metal brackets supplied. **T620:** panel mounting in a 150x31 mm panel cut-out with two screws.  3 x 2mm. Distance between the holes 165mm **V620:** panel mounting in a 56x72 mm panel cut-out with two screws.  3x2mm. Distance between the holes 40mm **CX620:** panel mounting in a 71x29mm panel cut-out **Protection:** IP20; **Frontal protection:** IP65 with frontal gasket **Connections:** Screw terminal block  2.5 mm<sup>2</sup> **Power supply:** from **XW60K** power module **Display** : 3 digits, red LED, 14.2 mm high **Optional** output: buzzer.

##### **<u>Power module XW60K</u>**

**Case: 8 DN:** 140X176X148 **Connections:** Screw terminal block  2.5 mm<sup>2</sup> heat-resistant wiring and 6.3mm Faston **Power supply:** 230Vac or. 110Vac  10% or 24Vac **Power absorption:** 10VA max **Inputs** : 4 NTC or PTC probes **Digital inputs** : 1 free voltage **Relay outputs:** **_<u>Total current on loads MAX. 20A</u>_ Compressor:** relay SPST 20(8) A, 250Vac; EN60730: 100K cycles **Fan:** relay SPST 8(3) A, 250Vac **Defrost:** relay SPST 16(5) A, 250Vac **Light (oA3):** relay SPST 16(5) A, 250Vac **Serial output:** TTL standard **Communication protocol:** Modbus - RTU **Data storing** : on the non-volatile memory (EEPROM) **Kind of action:** 1B **Pollution degree:** normal **Software class:** A **Operating temperature:** 0 to 60°C (32 to 140°F) **Storage temperature:** -25 to 60°C (-13 to 140°F) **Relative humidity:** 20 to 85% (no condensing) **Measuring and regulation range: NTC probe:** -40 to 110°C (-58 to 230°F) **PTC probe:** -50 to 150°C (-58 to 302°F) **Resolution:** 0.1°C or 1°C or 1°F (selectable) **Accuracy (ambient temp. 25°C):** ±0.5°C ±1 digit

### **16 CONNECTIONS**

#### **16.1 XW60K**

### **17 Default setting values**

|**Label**|<br>**Name**|**Range **<br>**REGULATION**|**Default**|<br>**Level**|
|---|---|---|---|---|
|**SEt**|Setpoint|LS;US|-5.0|- - -|
|**rtC***|Real time clock menu|-|-|Pr1|
|**Hy**|Differential|[0.1 to 25.5°C]<br>[1 to 45°F]|2.0|Pr1|
|**LS**|Minimum set point|[-55.0°C to SET]<br>[-67°F to SET]|-50.0|Pr2|
|**US**|Maximum set point|[SET to 150°C]<br>[SET to 302°F]|110|Pr2|
|**ot**|Thermostat probe calibration|[-12 to 12°C]<br>[-21 to 21°F]|0.0|Pr1|

|**Label**<br>**P2P**|<br>**Name**<br>Evaporatorprobepresence|**Range **<br>n=notpresent;Y=pres.|**Default**<br>Y|<br>**Level**<br>Pr1|
|---|---|---|---|---|
|**oE**|Evaporator probe calibration|[-12 to 12°C]<br>[-21 to 21°F]|0.0|Pr2|
|**P3P**|<sup>Third probe presence (1st cond.</sup><br>probe)|n=not present; Y=pres.|n|Pr2|
|**o3**|Third probe calibration|[-12 to 12°C]<br>[-21 to 21°F]|0|Pr2|
|**P4P**|<sup>Fourth probe presence (2nd</sup><br>cond.probe)|n=not present; Y=pres.|n|Pr2|
|**o4**|Fourth probe calibration|[-12 to 12°C]<br>[-21 to 21°F]|0|Pr2|
|**odS**|<sup>Outputs activation delay at start</sup><br>up|0 to 255 min|0|Pr2|
|**AC**<br>**Ac1**|Anti-short cycle delay<br>Second compressor delay|0 to 30 min<br>0 to 255 sec|1<br>5|Pr1<br>Pr2|
|**rtr**|P1-P2percentage for regulation|0 to 100(100=P1,0=P2)|100|Pr2|
|**CCt**|<sup>Compressor ON time during fast</sup><br>freezing|0.0 to 23h50min, res. 10 min|0.0|Pr2|
|**CCS**|Set point for continuous cycle|[-55.0 to 150.0°C]<br>[-67 to 302°F]|-5|Pr2|
|**Con**|<sup>Compressor ON time with faulty</sup><br>probe|0 to 255 min|15|Pr2|
|**CoF**|<sup>Compressor OFF time with faulty</sup><br>probe|0 to 255 min<br>|30|Pr2|
|**CF**<br>**rES**|Temperature measurement unit<br>Resolution(inteer/decimaloint)|**DISPLAY**<br>°C;°F<br>in;dE|°C<br>dE|Pr2<br>Pr1|
|<br>**rEd**|g p<br>Remote display|<br>P1;dtr|<br>P1|<br>Pr2|
|<br>**dLy **<br>|<br>Displaytemperature delay<br>|<br>0.0 to 20min00sec,res. 10 sec<br>|<br>0<br>|<br>Pr2<br>|
|**dtr **|P1-P2percentagefordisply|1;100<br>|50|Pr2|
|**tdF**<br>|Defrost type<br>|**DEFROST**<br>EL;in|EL|Pr1|
|**dFP**|<sup>Probe selection for defrost</sup><br>termination|nP; P1; P2; P3; P4|P2|Pr2|
|**dtE**|Defrost termination temperature|[-50.0 to 150°C]<br>[-58 to 302°F]|8.0|Pr1|
|**idF**<br>**MdF **|Interval between defrost cycles<br>(Maximum)lenth for 1°defrost|1 to 120 h<br>0to255min|6<br>30|Pr1<br>Pr1|
|<br>**dSd**|g  <br>Start defrost delay|<br>0 to 99 min|0|<br>Pr2|
|<br>**dFd**<br>**dAd**|<br>Displayingduringdefrost<br>MAX dildlft dft|<br>rt;it;SEt;dEF;dEG<br>0 t 255 i|<br>it<br>30|<br>Pr2<br>P2|
|<br>**Fdt**<br>|spayeayaer eros<br>Drainingtime<br>|o  mn<br>0 to 60 min<br>|<br>0|r<br>Pr2<br>|
|**dPo **<br>**dAF**|First defrost afterstart up<br>Defrost delayafter fast freezing|n;Y<br>0.0 to 23h50min,res. 10 min<br>**FANS**|n<br>0.0|Pr2<br>Pr2|
|**FnC**<br>**Fnd**|Fans operatingmode<br>Fans delayafter defrost|C-n;C-y;O-n;O-y<br>0 to 255 min|o-n<br>10|Pr1<br>Pr1|
|<br>**FCt**|<br><sup>Differential of temperature for</sup><br>forced activation of fans|<br>[0 to 50°C]<br>[0 to 90°F]<br>|<br>10|<br>Pr2|
|**FSt**<br>|Fans stop temperature<br>|[-55.0 to 50°C]<br>[-67to 302°F]<br>|2<br>|Pr1<br>|
|**Fon**<br>**FoF**|Fan on time with compressor off<br>Fan off time with compressor off|0 to 15 min<br>0 to 15 min|0<br>0|Pr2<br>Pr2|
|**FAP**|<sup>Probe selection for fan</sup><br>management|nP; P1; P2; P3; P4|P2|Pr2|
|**ACH**|**AUXIL**<br> Kind of action for auxiliaryrelay|**IARY THERMOSTAT**<br>CL;Ht|CL|Pr2|
|**SAA**|Set Point for auxiliary relay|[-55.0 to 150°C]<br>[-67to302°F]|0.0|Pr2|
|**SHy**|Differential for auxiliary relay|<br>[0.1 to 25.5°C]<br>[1to45°F]|2.0|Pr2|
|**ArP**<br>|Probe selection for auxiliaryrelay<br>|<br>nP;P1;P2;P3<br>|nP|Pr2<br>|
|**Sdd**|Aux.output workingduringdefrost|n;Y<br>**ALARMS**|n|Pr2|
|**ALP**|<sup>Probe setting for temperature</sup><br>alarm|P1; P2; P3; P4|P1|Pr2|
|**ALC**|<br>Temperature alarms configuration|rE;Ab|rE|Pr2|
|**ALU**|MAXIMUM temperature alarm|[-55.0 to 150.0°C]<br>[-67to302°F]|10.0|Pr1|
|**ALL**|minimum temperature alarm|<br>[-55.0 to 150.0°C]<br>[-67 to 302°F]|10.0|Pr1|
|**AFH**|<sup>Temperature alarm and fan</sup><br>|<br>[0.1 to 25.5°C]<br>°|2.0|Pr2|
|**ALd**|differential<br>Temperature alarm delay|[1 to 45F]<br>0 to 255 min|15|Pr2|
|**dAo**|<sup>Delay of temperature alarm at</sup><br>start up|0.0 to 23h50min, res. 10 min|1.3|Pr2|
|**AP2**|<sup>Probe for temperat. alarm of</sup><br>condenser|nP; P1; P2; P3; P4|P4|Pr2|
|**AL2**|<br><sup>Condenser for low temperat.</sup><br>alarm|[-55.0 to 150.0°C]<br>[-67 to 302°F]|-40|Pr2|
|**AU2**|<br><sup>Condenser for high temperat.</sup><br>alarm|<br>[-55.0 to 150.0°C]<br>[-67 to 302°F]|110|Pr2|
|**AH2**|<br><sup>Differential for condenser</sup><br>temerature alarm recover|<br>[0.1 to 25.5°C]<br>[1 to 45°F]|5|Pr2|
|**Ad2**|p y<br><sup>Condenser temperature alarm</sup><br>delay|<br>0 to 254 min , 255=nU|15|Pr2|
|**dA2**|<sup>Delay of cond. temper. alarm at</sup><br>start up|0.0 to 23h50min, res. 10 min|1.3|Pr2|
|**bLL**|<sup>Compressor off because of</sup><br>condenser low temperature alarm|n(0); Y(1)|n|Pr2|

|**Label**<br>|<br>**Name**<br>|**Range **|**Default**|<br>**Level**|
|---|---|---|---|---|
|**AC2**|<sup>Compr. off for condenser high</sup><br>temperature alarm|n(0); Y(1)|n|Pr2|
||<br>**A**|**UXILIARY OUTPUT**|||
|**tbA**|Alarm relaydisabling|n=no;Y=yes|Y|Pr2|
|**oA3**|Fourth relay configuration|ALr = alarm; dEF = do not select it; Lig<br>=Light; AUS =AUX; onF=always on; Fan=<br>do not select it; db = do not select it; dF2 =<br>do not select it|Lig|Pr2|
|**AoP **|Alarm relay polarity (oA3=ALr)|oP; CL<br>**DIGITAL INPUT**|CL|Pr2|
|**i1P**<br>**i1F**|Digital inputpolarity<br>Digital input configuration|oP=opening;CL=closing<br>EAL;bAL;PAL;dor;dEF;Htr;AUS|CL<br>dor|Pr1<br>Pr1|
|**did**|Digital input alarm delay|0 to 255 min|15|Pr1|
|**nPS**|<sup>Number of activation of pressure</sup><br>switch|0 to 15|15|Pr2|
|**odC**|<sup>Compress and fan status when</sup><br>open door|no; FAn; CPr; F_C|F-C|Pr2|
|**rrd**|<sup>Regulation restart with door open</sup><br>alarm|n; Y|Y|Pr2|
|**LES**|<sup>Light off during energy saving</sup><br>status|n; Y|Y|Pr2|
|**HES**|Differential for Energy Saving|[-30 to 30°C]<br>[-54 to 54°F]|0|Pr2|
|||**RTC**|||
|**Hur***|Current hour|read only|-|rtc|
|**Min***<br>**dAY***|Current minute<br> Current day|read only<br>read only|-<br>-|rtc<br>rtc|
|**dYM***|Dayof the month|read only|-|rtc|
|**Mon**|Month|read only|-|rtc|
|**YAr**|Year|read only|-|rtc|
|**Hd1***|First weeklyholiday|Sun to SAt;nu|nu|rtc|
|**Hd2***<br>|Secondweeklyholiday<br>|Sunto SAt;nu|nu|rtc|
|**ILE***|<sup>Energy Saving cycle start during</sup><br>workdays|0.0 to 23h50min|0|rtc|
|**dLE***|<sup>Energy Saving cycle length during</sup><br>workdays|0.0 to 24h00min|0|rtc|
|**ISE***|<sup>Energy Saving cycle start on</sup><br>holidays|0.0 to 23h50min|0|rtc|
|**dSE***|<sup>Energy Saving cycle length on</sup><br>holidays|0.0 to 24h00min|0|rtc|
|**Ld1***|1<sup>st</sup>workdays defrost start|0.0 to 23h50min;nu|6.0|rtc|
|**Ld2***|2<sup>nd</sup>workdays defrost start|0.0 to 23h50min;nu|13.0|rtc|
|**Ld3***|3<sup>rd</sup>workdays defrost start|0.0 to 23h50min;nu|21.0|rtc|
|**Ld4***|4<sup>th</sup>workdays defrost start|0.0 to 23h50min;nu|0.0|rtc|
|**Ld5***|5<sup>th</sup>workdays defrost start|0.0 to 23h50min;nu|0.0|rtc|
|**Ld6***|6<sup>th</sup>workdays defrost start|00 to 23h50min;nu|00|rtc|
|<br>**Sd1***|<br> 1<sup>st</sup>holidaydefrost start|. <br>0.0 to 23h50min;nu|.<br>6.0|<br>rtc|
|**Sd2***<br>**Sd3***|2<sup>nd</sup>holidaydefrost start<br> 3<sup>rd</sup>holidaydefrost start|0.0 to 23h50min;nu<br>0.0 to 23h50min;nu|13.0<br>21.0|rtc<br>rtc|
|**Sd4***|4<sup>th</sup>holidaydefrost start|0.0 to 23h50min;nu|0.0|rtc|
|**Sd5***|5<sup>th</sup>holidaydefrost start|0.0 to 23h50min;nu|0.0|rtc|
|<br>**Sd6***|<br> 6<sup>th</sup>holidaydefrost start|<br>0.0 to 23h50min;nu<br>**OTHER**|<br>0.0|<br>rtc|
|**Adr**|Serrial address|1 to 247|1|Pr1|
|<br>**PbC**|<br>Kind ofprobe|<br>PtC;ntC|<br>ntC|<br>Pr2|
|**onF**|on/off keyenabling|nu,oFF;ES|oFF|Pr2|
|**dP1**|Roomprobe display|read only|-|Pr1|
|**dP2**|Evaporatorprobe display|read only|-|Pr1|
|**dP3**|Thirdprobe display|read only|-|Pr1|
|**dP4**|Fourthprobe display|read only|-|Pr1|
|**rSE**<br>**rEL**|Current setpoint<br>Software release|read only<br>read onl|-|Pr1<br>Pr2|
|<br>**Ptb**|<br>Mapcode|y<br>read only|<br>-|<br>Pr2|

*** Only for model with real time clock**
