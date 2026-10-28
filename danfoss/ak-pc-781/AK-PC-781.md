# Danfoss AK-PC 781 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Capacity controller with heat recovery AK-PC 781

*Kilde: Danfoss-dokument AJ080486423583en-000201.pdf*

**User Guide**

### **Capacity controller with heat recovery** AK-PC 781

ADAP-KOOL® Refrigeration control systems

##### **Menu list**

##### **Validity**

##### **Function groups**

This menu function can be used together with system software type AKM. The description is divided up into function groups that can be displayed on the PC screen. Within each group it is now possible to show the measured values, or settings. Regarding the use of AKM, reference is made to the AKM Manual.

**This menu operation (from March 2013) applies to controller type AK-PC 781, code number 080Z0186 / 080Z0187  / 080Z0188 / 080Z0189 / 080Z0190 with programme version 4.1x.**

The operation is divided up into several function groups. When a selection has been made, push “OK”, and you may continue to the next display. By way of example, “Suction capacity control” has been selected here.

From the measure line the different values can be read. The values are constantly updated.

In the list of settings the set values can be seen. If a setting has to be changed, select the parameter and proceed via “OK”.

##### **Measurements**

The various measurements can be read directly. If a graphic display of the measurements is required, up to eight of them can be shown. Select the required measurements and push “Trend”.

Settings can only be made for the daily operation. Configuration settings cannot be seen, changed or written out. They can only be made from the Service Tool programme.

There are four kinds of settings, ON/OFF settings, settings with a variable value, time settings and “reset alarms”.

Set the required value and push “OK”

Enter the new value or move the sliding scale up or down. The new value will apply, when “OK” is pushed.

2

Go through the individual functions one by one and make the required settings. When settings have been made for one controller, the set values may be used as basis in the other controllers of the same type and with the same software version. Copy the settings by using the copy settings function in the AKM programme, and adjust subsequently any settings where there are deviations.

NB! If a list is required for noting down the individual settings, a printout can be made of it with a function in the AKM programme. Read the next section, “Documentation”.

##### **Documentation**

Documentation of the settings of the individual controllers can be made with the print function in the AKM programme. Select the controller for which documentation of the settings is required and select the “Print Settings” function (cf. also the AKM Manual).

##### **Functions**

##### **Note**

Shown below are function groups with corresponding measurements and settings. A printout of the given settings can be made using the AKM function “Print Settings” (see above).

It has been necessary to make selections among the many measurements and settings coming from the controller.

The operation from the AKM programme cannot contain them all.

If there is a need for access to all measurements and settings, you should make use of Service Tool type AK-ST 500.

3

#### **Main settings**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Compr. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler External Main Switch Status of input “Extern Main Switch”. In pos. “OFF” the regulation is stopped by force Settings Main switch Main switch: ON: Regulation OFF: Controller stopped Configuration lock Lock of configuration. In order to select quick setup or select refrigerant type, the configuration lock must be “open”. Note: ”Main switch” must be OFF in order to set configuration lock in “open” position 0: Open 1: Locked Refrigerant type Po Select refrigerant type 0= not selected, 1=R12. 2=R22. 3=R134a. 4=R502. 5=R717. 6=R13. 7=R13b1. 8=R23. 9=R500. 10=R503. 11=R114. 12=R142b. 13=User defined 14=R32. 15=R227. 16=R401A. 17=R507. 18=R402A. 19=R404A. 20=R407C. 21=R407A. 22=R407B. 23=R410A. 24=R170. 25=R290. 26=R600. 27=R600a. 28=R744. 29=R1270. 30=R417A. 31=R422A. 32=R413A. 33=R422D. 34=R427A. 35=R438A. 36=XP10. 37=R407F.

#### **Suction capacity control**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Compr. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler MC dP0 offset K Actual displacement value for the suction pressure in connection with a “P0 Optimiser” function (Master control function in AKA gateway)

4

||S4 media temp. °C|Actual media temperature measured at S4 sensor<br>(Only used if S4 is selected as control sensor)|
|---|---|---|
||Pctrl °C|<br>Actual regulation pressure measured with Pctrl pressure transmitter (cascade<br>pressure)|
||Suction status|0: Power up Controller has been powered up (power supply re-connected)<br>1: Stopped<br>Capacity control has been stopped ("Main switch" = OFF or<br>"Control mode" = OFF)<br>2: Manual<br>Capacity is controlled manually ("Control mode" =  MAN)<br>3: Alarm<br>Capacity control is in alarm condition (fx. alarm on Po Min<br>or Pc Max)|
|||<br>4: Restart<br>Capacity control is waiting for elapse of “Restart time”<br>5: Standby<br>Capacity control is ready to start<br>6: State off timer<br>7-10: State on timer<br>11: Unloaded<br>12-14: Unload cutin<br>15: Full loaded All capacity cutin|
||Actual Zone|16: Running Capacity control is running<br>Actual zone for capacity regulation:<br>0: P0-error<br>1: - - Zone<br>2: - Zone<br>3: NZ<br>4: + Zone|
|||5: + + Zone|
||Suction superheat K|Actual superheat|
||<br>Night Setback|<br>Status of night setback function<br>ON: Night (An increase of the evaporating pressure is permitted)<br>OFF: Normal situation|
||Load shed 1<br>Load shed 2|Actual status on Load shed input 1<br>Actual status on Load shed input 2|
||Injection ON|Status of the “Injection ON” function (earlier mentioned “AKC ON”)<br>0: Forced closing of all AKV valves<br>1: Normal operation of AKC controllers|
||MT release output<br>MT request input<br>LT request output<br>LT release input<br>No of compressors|<br>Actual status on ”Comp. release” output signal from MT controller<br>Actual status on ”Comp. request” input signal on MT controller<br>Actual status on ”Comp. request” output signal from LT controller<br>Actual status on ”Comp. release” input signal on LT controller<br>Defined number of compressors|
||.<br>Comp. application|i<br>Select the compressor application required (see the manual for further details)<br>0: Single step only<br>1: 1xComp. w. unloaders + Single step<br>2: 2xComp. w. unloaders + Single step<br>3: Comp. w. unloaders only<br>4: 1xVariable speed + Single step<br>5: 1xVariable speed + Comp. w. unloaders<br>6: 2xVariable speed + Single step|
||Step control mode|<br>Selected coupling pattern for compressors<br>Sequential: Compressors are cut in/out in strict accordance<br>with compressor number<br>Cyclic: Runtime equalisation between compressors<br>Best fit: Compressors are cut in/out in order to<br>make the best possible fit to actual load<br>0: Sequential<br>2: Cyclic<br>3: Best fit|
|Settings|Main switch|Main switch:<br>ON:<br>Regulation<br> <br>|
||Cap. control mode<br>Manual capacity %|OFF:<br>Controller stopped<br>0: MAN (The compressor capacity will be controlled manually)<br>1: OFF (The capacity control will be stopped)<br>2: AUTO (The capacity is controlled by the PI controller)<br>Manual setting of compressor capacity<br>The value is in % of total caacit controlled b the controller|
||Reference mode|py  y<br>Displacement of suction pressure as a function of external signals<br>0: Reference = set reference + night offset + offset from external 0-10 V signal<br>1: Reference = set reference + offset from P0 optimization + night offset|

5

Setpoint °C Setting of required suction pressure in °C Min.Reference °C Min. permissible suction pressure reference Max.Reference °C Max. permissible suction pressure reference Night offset K Displacement value for suction pressure in connection with an active night setback signal (set in Kelvin) ++Zone delay s Time delay between step cut-ins in the regulation band over the “+Zone band” Set in seconds +Zone delay s Time delay between step cut-ins in the regulation band over the neutral zone Set in seconds +Zone band K Regulation band over the neutral zone Neutral zone K Neutral zone for suction pressure -Zone band K Regulation band under the neutral zone -Zone delay s Time delay between step cut-outs in the regulation band under the neutral zone Set in seconds --Zone delay s Time delay between step cut-outs in the regulation band under the “-Zone band” Set in seconds. Kp Po Ampliflication factor for P0 regulation VSD Min. speed Hz Minimum allowed speed before stop of Variable Speed drive (Low load condition) VSD Start speed Hz Minimum speed for start of Variable speed drive (Must be set higher than “VSD Min. Speed Hz”) VSD Max. speed Hz Highest permissible speed for the compressor motor Sd max. limit °C Alarm at too high Sd Sd comp. alarm delay Time delay for Sd alarm P0 min. limit °C Alarm at too low P0 P0 max. alarm °C Alarm at too high P0 P0 max. delay m Time delay for P0 alarm SH min. alarm K Alarm at too low superheat SH max. alarm K Alarm at too high superheat SH alarm delay m Time delay for SH alarm Load shed limit 1 Set max capacity limit for load shed input 1 Load shed limit 2 Set max capacity limit for load shed input 2 MT release delay s Time delay on output signal ”Comp. release” on MT controller MT request delay s Time delay on input signal for ”Comp. request” on MT controller LT request delay s Time delay on output signal ”Comp. request” on LT controller LT release delay s Time delay on input signal for ”Comp. release” on LT controller Po pump down Select if a pump down function on the last compressor is requested Po pump down limit °C Set the actual pump down limit for the last compressor Initial start time The time after start-up where the cut-in capacity is limited to the first compressor step. Safety restart time Time delay before restart of compressors

#### **Suction compressor status**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure

6

Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler VSD 1 safety Status on safety input for variable speed controller on compressor 1 ON: Alarm OFF: No alarm VSD 2 safety Status on safety input for variable speed controller on compressor 2 ON: Alarm OFF: No alarm VSD Speed % The present speed of the compressor motor controlled by the frequency converter Comp. 1 Status 0: Power up Controller has been powered up/Compressor is not used 1: Stopped Compressor hat been stopped 2: Manual Compressor capacity is controlled manually 3: Alarm Compressor is in alarm condition (cut out on safety) 4: Restart Compressor is waiting for elapse of “Recycle time” 5: Standby Compressor is ready to start 6-10: Status_RUN_Timer 11: unloaded 12-14: Unloads cutin 15: Full loaded  All capacity cutin 16: Running Capacity control is running Comp 2 … Status As above for compressor no. 2 to 8 Comp 1 capacity % Actual cut-in capacity on this compressor Comp 2 …capacity % As above for compressor no. 2 to 8 Comp 1 Cycles / 24 h Number of compressor starts during the past 24 hours Comp 2 …Cycles / 24 h As above for compressor no. 2 to 8 Settings Main switch Main switch: ON: Regulation OFF: Controller stopped 1 Min. ON-time m Minimum duration of ON period 2 …Min. ON-time m As above for compressor no. 2 to 8 1 Min. OFF-time m Minimum duration of OFF period 2 …Min. OFF-time m As above for compressor no. 2 to 8 1 Recycle time m Minimum period of time between two successive starts. 2 …Recycle time m As above for compressor no. 2 to 8 1 runtime h Compressor’s total run time in hours 2 …runtime h As above for compressor no. 2 to 8

#### **High pressure control**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Shp °C Read temperature at high pressure valve Vhp OD% Read opening degree of high pressure valve

7

Rec. Status 0: Off 1: Standby 2: Normal 3: Emergency operation 4: Manual Prec Bar Read pressure of receiver Vrec OD% Read opening degree of receiver valve Settings Main switch Main switch: ON: Regulation OFF: Controller stopped HP control ManAut Control of high pressure valve: 1=automatic, 2=manual override Vhp manual OD% Manual setting of opening degree of high pressure valve Pgc min. Bar Setting of gas coolers min. pressure Pgc max. Bar Setting of gas coolers max. pressure Extra capacity offs Set requested pressure increase if the "extra cooling capacity" is activated dT Subcool K Set requested sub cooling in the sub critical range Rec. Control ManAut Control of receiver valve: 1=automatic, 2=manual override Rec. Manual OD% Manual setting of opening degree of the receiver valve Prec setpoint Bar Set requested receiver pressure

#### **Oil management**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Rec. pressure Actual pressure in receiver Rec. pres. buildup Status of oil separator

Main switch Main switch: ON: Regulation OFF: Controller stopped Interval time Time between breaks. (Simple oil equalisation) Equalisation time Duration of oil equalisation (Simple oil equalisation) Rec. pres. cutin Bar Reciever pressure, which to cutin for the oil Rec.pres.cutout  Bar Receiver pressure, which to cutout for the oil High alarm limit Bar Alarm limit high Low alarm limit Bar Alarm limit low High alarm delay m Delay time for high pressure alarm Low alarm delay m Delay time for low pressure alarm Lvl. alarm delay s Delay time for Level alarm

#### **Condenser capacity control**

Measurements

AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any)

8

Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Tc max. limit °C Readout limit value for max condenser pressure S7 brine temp °C Actual media temperature measured at S7 sensor (Only used if S7 is selected as control sensor) Condenser status 0:  Power up       Controller has been powered up (power supply re-connected) 1:  Stopped Capacity control has been stopped (“Main switch” = OFF or “Control mode” = OFF) 2:  Manual Capacity is controlled manually (“Control mode” = MAN) 3:  Alarm Capacity control is in alarm condition (f.ex. Pc Max or Sd Max) 4:  Restart Capacity control is waiting for elapse of “Restart time” 5:  Standby Capacity control is ready to start 6:  Unloaded 7-9 Part loaded 10: Full loaded    All capacity cutin 11: Running Capacity control is running Air flow status 0: No RFG. select No refrigerant has been selected (monitoring of air flow can not start) 1: Tuning Monitoring function adapts to the condenser in question 2: OFF Monitoring function is switched OFF 3: OK Air flow is OK 4: Little dirt The amount of dirt decreases the performance of the condenser, clean when possible 5: Dirty The amount of dirt leads to considerable air flow problems, clean as soon as possible 6: Blocking The amount of dirt might lead to high pressure problems, clean now Sc3 Air on  °C Outdoor temperature in °C measured with Sc3 temperature sensor No. of fans Defined number of fans VSD Speed % Status of analogue output signal “AO” for variable speed drive (in percent of full scale f.ex. 0 -10 V d.c.) VSD safety Status of safety monitoring input for Variable Speed Drive ON: Alarm on VSD A safety monitoring input OFF: No alarm on VSD A safety monitoring input Main switch Main switch: ON: Regulation OFF: Controller stopped Condenser ctrl mode 0: MAN (The condenser capacity will be controlled manually) 1: OFF (The capacity control will be stopped) 2: AUTO (The capacity is controlled by the PI controller) Manual capacity % Manual setting of condenser capacity The value is in % of total capacity controlled by the controller Pc Ref. mode 0: Set point Reference = “PcA setpoint °C” 1: Floating Reference is changed as a function of the outdoor temperature measured by the “Sc3 air on” sensor, the set “Dimensioning tm K” and the actual compressor load. Cond. Setpoint °C Setting of required discharge pressure in °C Dimensioning tm K Dimensioning mean temperature differential between air- and condensing temperature at full load for the condenser in question (Typical 8 – 15K).

9

Min. tm k tm value at minimum load. Min. Reference °C Min. permissible condensing pressure reference Max. Reference °C Max. permissible condensing pressure reference Capacity Lim. night % Capacity limitation during night operation Kp Amplification factor P/PI controller Tn s Integration time for PI controller VSD Min. speed % Minimum allowed speed before stop of Variable Speed drive (Low load condition) VSD Start speed % Minimum speed for start of Variable speed drive (Must be set higher than “VSD Min. Speed %”) Pc max limit Bar Max. limit for condensing pressure Pc max alarm delay m Time delay for "Pc max alarm"

#### **Condenser fan status**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Compr. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc bar Actual gas cooler pressure Pgc reference bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Fan1/VSD status Status of the Fan 1 ON: Fan is running OFF: Fan is not running Fan2.... status As above for fan 2 to 8 Settings Main switch Main switch: ON: Regulation

Main switch: ON: Regulation OFF: Controller stopped

#### **Heat recovery**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Compr. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control.

10

Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Shr2 °C (ONLY at CO2). Temperature at sensor Shr2 Stw2 °C (ONLY at  CO2). Temperature at sensor Stw2 Status heat circuit (ONLY at  CO2). 0=off. 1=waiting. 2=started. 3=standard. 4=variable offset 5=max recovery. 6=stopped. 7=error. Tw Stw8 °C (ONLY at  CO2). Temperature at sensor Stw8. Tap water Tw Status (ONLY at  CO2). 0=off. 1=waiting. 2=started. 3=hot tap water. 5=manual. 6= stopped. 7=error. 8=Flow error. 9=sensor error. 10=boiling. Tw enable (ONLY at  CO2). Readout about tap water circuit can be activated automatically Hr Shr8 °C (ONLY at  CO2).Temperature at sensor Shr8. Heat circuit Hr Status (ONLY at  CO2). 0=off. 1=waiting. 2=started. 3=heat circuit. 5=manual. 6= stopped. 7=error. 8=Flow error. 9=sensor error. 10=boiling. Hr enable (ONLY at CO2). Readout about heat circuit can be activated automatically HR thermostat temp°C (Not at  CO2). Actual temperature at sensor for heat recovery function Heat recovery status (Not at  CO2). Status on heat recovery function (on/off) Settings Main switch Main switch: ON: Regulation OFF: Controller stopped Tw setpoint °C (ONLY at  CO2). Set point for tap water temperature Hr setpoint °C (ONLY at  CO2). Set point for heat circuit temperature Pgc HR max. offset (ONLY at  CO2). Displacement pressure of max. signal Pgc HR min. Bar (ONLY at  CO2). Set point at min. signal Heat recovery SP °C (Not at CO2). Reference for condenser pressure when heat recovery is on HR temp. cutin °C (Not at  CO2). Temperature value when thermostat switch to heat recovery HR temp. cutout °C (Not at  CO2). Temperature value when thermostat switch off the heat recovery

#### **Alarm priorities**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Settings Main switch Main switch: ON: Regulation OFF: Controller stopped The alarm priority of the following alarms can be changed: High priority is defined with setting = 1 Medium priority is defined with setting = 2 Low priority is defined with setting = 3 Log only = 4 Overriding the alarms is defined with setting = 0 Main Switch 0/1/2/3/4 Low P0 0/1/2/3/4

11

*[Figurtekst: High P0  0/1/2/3/4 · High Pc/Sd  0/1/2/3/4 · Hpcontrol / Receive  0/1/2/3/4]*

High P0 0/1/2/3/4 High Pc/Sd 0/1/2/3/4 Hpcontrol / Receive 0/1/2/3/4 Superheat Min/Max 0/1/2/3/4 Load shedding 0/1/2/3/4 P0/S4/Pctrl error 0/1/2/3/4 Misc. sensors 0/1/2/3/4 Comp. common safety 0/1/2/3/4 Comp. VSD safety 0/1/2/3/4 Comp. 1 safety 0/1/2/3/4 Comp. 2 safety 0/1/2/3/4 Comp. 3 safety 0/1/2/3/4 Comp. 4 safety 0/1/2/3/4 Comp. 5 safety 0/1/2/3/4 Comp. 6 safety 0/1/2/3/4 Comp. 7 safety 0/1/2/3/4 Comp. 8 safety 0/1/2/3/4 Pc/S7 sensor error 0/1/2/3/4 Blocked air flow 0/1/2/3/4 Fan safety 0/1/2/3/4 Comp. Low Oil lvl 0/1/2/3/4 Comp. High Oil lvl 0/1/2/3/4 Oil Separator alarm 0/1/2/3/4 Oil Receiver alarm 0/1/2/3/4 Oil Recv High press 0/1/2/3/4 Oil Recv. Low press 0/1/2/3/4 Tw boiling alarm 0/1/2/3/4 Hr boiling alarm 0/1/2/3/4

#### **General alarm inputs**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Compr. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler DI 1 input Alarm status on the function defined as a DI1 alarm ON: Alarm is activ OFF: No alarm, normal situation DI 2.... Input As above, but for the alarm functions 2 to 6 Settings Main switch Main switch: ON: Regulation OFF: Controller stopped DI 1 Alarm delay m Time delay for the alarm "DI 1 Alarm" DI 2.... Alarm delay m As above, but for the alarm functions 2 to 6

12

#### **Thermostat/pressostats**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity Pc Bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler Thermostat 1 °C Temperature measurement of function defined in Thermostat 1. Thermostat 2 °C Temperature measurement of function defined in Thermostat 2. Thermostat 3 °C Temperature measurement of function defined in Thermostat 3. Pressostat 1 Bar Pressure measurement of function defined in Pressostat 1 Pressostat 2 Bar As above but for Pressostat 2 Pressostat 3 Bar As above but for Pressostat 3 Settings Main switch Main switch: ON: Regulation OFF: Controller stopped T1 Cutin °C Cutin value for function defined in ”Thermostat 1”. T1 Cutout °C Cutout value for function defined in ”Thermostat 1”. T1 High Alarm °C High alarm  limit "Thermostat 1" T1 Low Alarm °C Low alarm limit "Thermostat 1" T1 High Al delay m Time delay for high alarm "Thermostat 1" T1 Low Al delay m Time delay for low alarm "Thermostat 1" P1 Cutin press Bar Cutin value for function defined in ” Pressostat 1”. P1 Cutout press Bar Cutout value for function defined in ”Pressostat 1”. P1 High Al limit Bar High alarm limit "Pressostat 1" P1 Low Al limit Bar Low alarm limit "Pressostat 1" P1 High Al delay m Time delay for high alarm "Pressostat 1" P1 Low Al delay m Time delay for  low alarm "Pressostat 1"

(Use Service Tool if data concerning thermostats 2 to 5 or from Pressostat 2 to 5 have to be downloaded).

#### **Voltage  and PI inputs**

Measurements AK error When “ON”, the controller is in alarm condition. Comp. ctrl. temp °C Actual temperature for control sensor (Po or S4) Comp. ctrl. ref. °C Actual reference temp. for compressor capacity (incl. external reference signal, if any) Compressor cap. % Cut-in compressor capacity in % (of total capacity) Request Comp. Cap % Reference for compressor capacity (deviations may be due to time delays) P0 °C Suction pressure in °C.  (Measured with the pressure transmitter) Ss Suction gas °C Actual suction gas temperature Cond. ctrl. temp °C Actual temperature for control sensor (Pc or S7) Cond. ctrl. ref. °C Actual reference temp. for condenser capacity (incl. external contributions, if any) Cond. cap.  % Cut-in condenser capacity in % (of total capacity) Request Cond. cap % Reference for condenser capacity

13

Pc bar Condensing pressure (measured with the pressure transmitter) Tc °C Condensing pressure in °C. (measured with the pressure transmitter) Gc status Actual gas cooler operation: 0=Off.  1=Standby.  2=Max COP operation. 3=Heat recovery. 4=Extra capacity. 5=Manual control. Pgc Bar Actual gas cooler pressure Pgc reference Bar Actual reference for gas cooler pressure Sd discharge gas °C Actual discharge gas temperature Sgc °C Actual temperature at outlet from the gas cooler V1 Actual input Voltage measurement on the function defined in Volt 1. V2 Actual input Voltage measurement on the function defined in Volt 2. V3 Actual input Voltage measurement on the function defined in Volt 3. PI1 State PI function state PI1 Alarm state PI function alarm condition PI1 Input Input signal PI1 Reference Reference PI1 Output value Output value PI1 Output type Output type: PWM. Stepper. Voltage

Main switch Main switch: ON: Regulation OFF: Controller stopped V1 Cutin The value where the relay is to cut in V1 Cutout The value where the relay is to cut out V1 Cutin delay m Time delay for cutin of relay V1 Cutout delay m Time delay for cutout of relay V1 High Al Limit The value for the high alarm limit V1 Low Al Limit The value for the low alarm limit V1 High Al delay m Time delay for high alarm V1 Low Al delay m Time delay for low alarm PI1 Off Aut Man Control of PI function. 0: Off, 1: Automatic, 2: Manual PI1 Manual OD Manual setting of opening degree for PI function

(Use Service Tool if data concerning Volt 2, 3, 4, 5 and PI2 /PI3 are to be downloaded).

#### **AKM menu: "For DANFOSS only"**

This menu contains data and setting values for special internal controller functions. **Do not change the stated values.**

All trademarks in this material are property of the respecitve companies. Danfoss and Danfoss logotype are trademarks of Danfoss A/S. All rights reserved.

Danfoss can accept no responsibility for possible errors in catalogues, brochures and other printed material. Danfoss reserves the right to alter its products without notice. This also applies to products already on order provided that such alternations can be made without subsequential changes being necessary in specifications already agreed.

14
