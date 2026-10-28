# Danfoss AK-PC 530 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## Instructions – RI8LZ452 05-2010

*Kilde: Danfoss-dokument AN00008642753301-000401.pdf*

### **Instructions**

*[Figurtekst: Identification Dimensions · 084B8007 · Principle · NZ control PI or P control · Danfoss 84B2330.11]*

RI8LZ452  05-2010

**ENGLISH**

###### **Connections**

P0/Pc: AKS 32R: 1 = Black  = + 2 = Blue  = - 3 = Brown = s

Compressor control with temperature

o06 = 0 o81 = 1 Other combinations: see manual All inputs are low-voltage. All relay outputs may be high-voltage. Data communication

**Necessary connections** Terminals:

- 1-2 Supply voltage 24 V a.c.

- 4- 19 Relay outputs for either compressors, unloaders or fan

   - motors

22-24  Alarm relay *

- There is connection between 22 and 24 in alarm situa tions and when the controller is dead

27-28 24 V signal to start / stop of regulation

27-29 24 V signal from the safety circuit DO 1

27-30 24 V signal from the safety circuit DO 2

- 27-31 24 V signal from the safety circuit DO 3

- 27-32 24 V signal from the safety circuit DO 4

- 27-33 24 V signal from the safety circuit DO 5

- 27-34 24 V signal from the safety circuit DO 6

27-35 24 V signal from the safety circuit DO 7

- 27-36 24 V signal from the safety circuit DO 8

57-59 Suction pressure. Voltage signal from AKS 32R **

60-62 Condenser pressure. Voltage signal from AKS 32R **

###### **Application dependent connections**

- 20-21 AKD start/stop *

   - The relay cutin when the frequency converter have to start.

- 37-38 Voltage signal to external condenser control (see settings page 4)

- 39-41 Possibility of connecting an external display type EKA 163 for display of Pc

- 42-44 Possibility of connecting an external display type EKA 163 for display of P0, or EKA 165 for operation and display of P0

- 45-46 DI1 - Contact function for alarm signal

45-47 DI2 - Contact function for alarm signal

- 48-49 DI3 - Contact function for alarm signal

- 48-50 DI4 - Contact function for displacement of the suction pressure reference or for alarm signal.

- 51-52 DI5 - Contact function for displacement of the condenser pressure reference or for alarm signal.

- 51-53 Separate sensor Saux1. Sensor signal fra AKS 11, AKS 12 or EKS 111

- 54-55 Out temperature (Sc3). Sensor signal from AKS 11, AKS 12 or EKS 111 (mounted if r33 =2 or 4)

- 54-56 Air temperature at  condenser outlet. Sensor signal from AKS 11, AKS 12 or EKS 111

###### **Unloader**

If an output is used for an unloader it is not necessary to wire the belonging safety circuit. Ex. with an unloader on DO2 a connection on terminal 30 can be left out

*) Relays DO9 and DO10 may in special cases be reconfigurated so that they can be used as fan relays.

###### **Data communication**

25-26  Mount only, if a data communication module has been mounted.

For ethernet communication the plug connection RJ45 must be used. (LON FTT10 can also be connected in this way.

It i s important t hat the installation of the data communication cable be done correctly. Cf. separate literature No. RC8AC.

- **) • If the controller has to control only the comrpessor or the fans, respectively Pc and P0 sensor can be dispensed

- In brine systems temperature measurement at terminals 57-58 and 60-61 may be used instead of pressure measurement with AKS 32R. See also o06.


2

**Compressor configuration when o61 =1 or 2** (This is where you can choose between the options shown.) Setting "c16" will define the configuration. Setting "c08" will define coupling mode.

*[Figurtekst: Compressor connections Coupling · mode · Relay no. "C16"  Set  "C08"  Set · to to]*

###### **Capacity step**

**All** capacity steps are presumed to be identical. The only exception is the settings c16 = 4 and 21 to 26.

###### **Coupling mode**

Coupling mode 1 = sequential operation. Coupling mode 2 = cyclic operation. Coupling mode 3 = cyclic and binary operation where the compressor capacities are, as follows:

1: 9%

2: 18%

3: 36%

4: 36%

There is cyclic coupling at 3 and 4, and binary on 1, 2 and 3/4. (for c16=4 only)

###### **Couplings**

When there is cyclic operation and connections with unloaders there will in some capacity cutins and cutouts be overlappings where the unloaders from either one compressor or another may be active.

In such cases the unloaders on the compressor with the lowest number of hours will be cut in, and the others cut out.

The changeover will take place at 6- second intervals.

###### **Equalised operation**

When c16 = 21 to 26, compressor 1 + belonging unloader must have the same capacity as each of the subsequent compressors. The unloading function will equalise the cut-in capacity when the subsequent compressors are cut in and out. Compressor 1 will always be operating.

**Compressor configuration when  o61 = 3 or 4** (This is where you must define yourself how the relays are to be activated.)

|Surveyof r|elays in Mix and|Match|ope|ra|tion||||||||(Mix and Match used only on plants with up to 4 compressors.)|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Relay no.|Calculation<br>value|Comb|ina|ti|on of|relays tha|t m|ust be c|ut|in||||
|1|1|1||1||1<br>|1|1||1|1|1||
|2|2||2|2||2<br>|2||2|2||2<br>2||
|3|4||||4|4<br>4<br>|4|||4|4|4<br>4||
|4|8|||||||8<br>8|8|8<br>8|8|8<br>8||
|The sum o<br>ting value|f 1-8 is the set-<br>for each step|1<br>|2|3|4|5<br>6<br>|7|8<br>9 1|0|11 12|13 1|4 15||

Example 1

Settings: c17 to 1 c18 to 2 c19 to 3 c20 to 4 c21 to 5 c22 to 6 c23 to 7

Example 2

If capacity step 1 has to cut in relay number 3 only, you must set c17 to 4. If capacity step 2 has to cut in relay number 4 only, you must set c18 to 8. If capacity step 3 has to cut in relay numbers 3 and 4, you must set c19 to 12. Continue with a setting for c20 etc. until all capacity steps have been defined.

3

###### **Condenser couplings**

When the compressor relays have been established the turn comes to the fan relays.

The f i rst vacant relay ( DO1-DO8) will become the first fan relay. It will be followed by the subsequent relays. If more relays are required than the vacant DO relays, a relay module can be connected to the analog output. The function is, as follows:

If there are up to four external fans on an EKC 331:

Output signal from AK-PC 530 In EKC 331 the voltage range must be set to 0-5 V (“o10” = 6). In EKC 331 the number of steps must be set **to 4 (“o19” = 4)** (also when fewer fans are connected).

###### Connection

If there are more than four external fans on two EKC 331 units:

Output signal from AK-PC 530

In the first EKC 331, set 0-5 V (“o10” = 6).

In the second EKC 331, set 5-10 V (“o10” = 7).

In **both** EKC’s the number of steps must be set **to 4 (“o19” = 4)** (also when fewer fans are connected to the second EKC).

Connection

Alternating start-up of fans (only if c29 is 11 to 18)

The fans can be defined to start alternately when they have all been stopped.

The first time regulation is started, fan 1 will be started first – the regulation determines whether additional fans will be started. After the next time all fans are stopped, fan 2 will be the first to be started, and so on.

Fan 1 will again be the first fan to be started when the rotation has been through the total number of fans.

If there is more than one fan on an EKC 331, it will not be possible to start the other fans first. Here, the fan with the lowest voltage step will always be the one which is started first.

If the entire condenser capacity is to be controlled by a frequency converter, AK-PC 530 must send an analog signal about the required capacity (“c29” = 9). The signal varies from 0 to 10 V. Signal and capacity have the following context.

4

##### **Operation**

###### **Data communication**

If the controller is extended with data communication, the operation can be performed from a system unit.

The importance of the alarms that are sent can be defined with the setting: 1 (High), 2 (Medium), 3 (Low) or 0 (No alarm).

###### **Operation via external display**

The values will be shown with three digits, and with a setting you can determine whether the pressures are to be shown in SI units (°C / bar) or US units (°F / psig.). There are three options for the display.

To operate the controller and view the evaporation pressure. If the lowermost key is pressed, the condensation pressure will be shown briefly in the display. (If regulation is based only on the condensation pressure, the display will always show Pc).

During normal operation the light-emitting diodes in the display will indicate where regulation is taking place. Highest + second highest : ++Zone Second highest : +Zone "None" : Neutral zone Second lowest : -Zone Lowest+ second lowest : - - Zone

The other LEDs on the display will show the functions that are active:

- Relays for compressors

- Relays for fans

- Input signals for the digital inputs

- The optimisation LED will light up when the reference is 2 K or more over the set point.

If the condensation pressure is to be shown constantly, a display without operating keys can be connected.

###### **EKA 164**

To operate the controller and view the evaporation pressure. If the lowermost key is pressed, the condensation pressure will be shown briefly in the display. Like the EKA 165, the LEDs in the display will show where the regulation is located.

###### The buttons on the display

When you want to change a setting, the upper and the lower buttons will give you a higher or lower value depending on the button you are pushing. But before you change the value, you must have access to the menu. You obtain this by pushing the upper button for a couple of seconds - you will then enter the column with parameter codes. Find the parameter code you want to change and push the middle button. When you have changed the value, save the new value by once more pushing the middle button.

###### Or short:

1. Push the upper button (long push) until a parameter is shown

2. Push one of the buttons and find the parameter you want to change

3. Push the middle button until the setting value is shown

4. Push one of the buttons and select the new value

5. Push the middle button again to conclude the setting

- ( A brief pushing will show the active alarm codes.)

5

##### **Menu survey**

###### **Sequence**

**1.** o61 must be set as the first parameter. This parameter determines which of the four operating interfaces are activated. This must be set via the display keys. It cannot be set via data communication. (Active functions are shown below in shaded fields.)

**2.** Quick- start

To get the system up and running quickly so that cooling can be commenced, start it by setting the following parameters (these parameters can only be set when the regulation is stopped r12=0):

r23, r28 and then either (c08, c09 and c16) or (c17 to 28) – continue with c29, o06, o30, o75, o76, o81 and finally r12=1.

**3.** Once the regulation is under way, you can go through the other parameters and adjust them in situ.

SW: 1.3x

|**Function**|**Para-**<br>||**o6**|**1 =**|**Min.**|**Max.**|**Factory**<br>|
|---|---|---|---|---|---|---|---|
||**meter**|**1**|**2**|**3**<br>**4**|||**setting**|
|**Normal display**||||||||
|Shows P0 in EKA 165(displaywith buttons)|-|°C|P|°C<br>P|°C / bar|||
|Shows Pc in EKA 163|-|°C|P|°C<br>P|°C / bar|||
|**P0 reference**||||||||
|Neutral zone|r01||||0.1°C / 0.1 bar|20°C /5.0 bar|4.0°C / 0.4 bar|
|Correction of signal from P0 sensor|r04||||-50°C /-5.0 bar|50°C / 5.0 bar|0.0|
|Select view;SI or US. 0=SI(bar /°C),1=US(Psig/°F)|r05||||0|1|0|
|Start/Stopof regulation|r12||||OFF|ON|OFF|
|Reference offset for P0 (see also r27)|r13||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Set regulation setpoint for P0|r23||||-99°C / -1 bar|30°C / 60.0 bar|0.0°C / 3.5 bar|
|Shows total P0 reference<br>(r23 + various displacements)|r24|||||°C / bar||
|Limitation: P0 reference max. value<br>(also applies to regulation with reference displacement)|r25||||-99°C / -1.0 bar|30°C / 60.0 bar|30.0°C / 40.0 bar|
|Limitation: P0 referencen min. value<br>(also applies to regulation with reference displacement)|r26||||-99°C / -1.0 bar|30°C / 40.0 bar|-99.9°C / -1.0 bar|
|Displacement of P0 (ON=active “r13”)|r27||||OFF|ON|OFF|
|**Pc reference**||||||||
|Set regulation setpoint for Pc|r28||||-25°C / 0.0 bar|75°C / 110.0 bar|35°C / 15.0 bar|
|Shows total Pc reference|r29|||||°C / bar||
|Limitation: Pc referencen max. value|r30||||-99.9°C / -0.0 bar|99.9°C/130.0bar|55.0°C / 60.0 bar|
|Limitation: Pc referencen min. value|r31||||-99.9°C / 0.0 bar|99.9°C / 60.0 bar|-99.9°C / 0.0 bar|
|Correction of signal from Pc sensor|r32||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Pc reference variation.1 and 2 are PI-regulation<br>1: Fixed reference. “r28” is used<br>2: Variable reference. Outdoor temperature (Sc3) included<br>in the reference<br>3: As 1, but with P-regulation (Xp-band)|r33||||1|4|1|
|4: As 2,but with P-regulation(Xp-band)||||||||
|Reference offset for Pc|r34||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|The mean temperature difference across the condenser at<br>maximum load(dim tm K)|r35||||3.0|50.0|10.0|
|The mean temperature difference across the condenser at<br>the lowest relevant compressor capacity (min tm K)|r56||||3.0|50.0|8.0|
|This is where you can see the actual pressure (P0) that is<br>beingmeasured bythepressure transmitter.|r57|||||°C / bar||
|This is where you can see the actual pressure (T0) that is<br>part of the regulation. From the sensor which is defined|r58|||||°C||
|i<br>in “o81”||||||||
|**Capacity**||||||||
|Min. ON time for relays|c01||||0 min|30 min.|0|
|Min. timeperiod between cutins of same relay|c07||||0  min.|60 min|4|
|Definition of regulation mode<br>1: Sequential (step mode / FILO)<br>2: Cyclic (step mode / FIFO)<br>|c08||||1|3|1|
|3: Binary and cyclic||||||||
|If a regulation mode with unloaders is selected, the relay<br>must be defined to:<br>0: Cut in when more capacity is required<br>1: Cut out when more capacityis required|c09||||0|1|0|

To be continued

6

|Regulationparameter for + Zone<br>|c10<br>0.1 K / 0.1 bar<br><br>|20 K / 2.0 bar<br>|4.0 / 0.4 bar<br>|
|---|---|---|---|
|Regulationparameter for + Zone|c11<br>0.1 min|60 min|4.0|
|Regulationparameter for ++ Zone|c12<br>0.1 min.|20 min|2.0|
|Regulationparameter for - Zone|c13<br>0.1 K / 0.1 bar|20 K / 2.0 bar|4.0 / 0.3 bar|
|Regulationparameter for - Zone|c14<br>0.1 min.|60 min|1.0|
|Regulationparameter for - -  Zone<br>i|c15<br>0.02 min.|20 min|0.5|
|Definition of compressor connections.<br>See options onpage 3.|c16<br>1|26|0|
|Following "c17" to "c28" is another way to define compres-<br>sorw than with "c16"..A code will then have to be set for<br>the relays that are to be ON at the different steps:<br>Step1(M&M operation)|c17<br>0|15|0|
|Step2(M&M operation)|c18<br>0|15|0|
|Step3(M&M operation)|c19<br>0|15|0|
|Step4(M&M operation)|c20<br>0|15|0|
|Step5(M&M operation)|c21<br>0|15|0|
|Step6(M&M operation)|c22<br>0|15|0|
|Step7(M&M operation)|c23<br>0|15|0|
|Step8(M&M operation)|c24<br>0|15|0|
|Step9(M&M operation)|c25<br>0|15|0|
|Step10(M&M operation)|c26<br>0|15|0|
|Step11(M&M operation)|c27<br>0|15|0|
|Step12(M&M operation)|c28<br>0|15|0|
|Definition of condenser:<br>**1-8:**Total number of fan relays or voltage step on the<br>voltage output<br>||||
|**9:**Only via analog output and start of frequency con-<br>verter<br>**10:**Not used<br>**11- 18:**Total number of fan relays which are to be con-|c29<br>0/OFF|18|0|
|nected with alternatingstart-up.||||
|Cut in compressor capacity with manual control. See also<br>“c32”|c31<br>0%|100%|0|
|Manual control of compressor capacity (when ON, the<br>value in “c31” will be used)|c32<br>OFF|ON|OFF|
|Pump down limit. Limit value where the last compressor<br>is cut out.|c33<br>-99.9°C / -1.0 bar|100°C / 60 bar|100°C / 60 bar|
|Proportinal band Xpfor(P= 100/Xp)condenser regulation|n04<br>0.2 K / 0.2 bar|40.0 K / 10.0 bar|10.0 K / 3.0 bar|
|I: Integration time Tn for condenser regulation|n05<br>30 s|600 s|150|
|Cutin condenser capacity with manual control. See also<br>“n53”|n52<br>0%|100%|0|
|Manual control of condenser capacity (when ON, the<br>value in “n52” will be used)|n53<br>OFF|ON|OFF|
|Start speed The voltage for the speed regulation is kept<br>at 0V until the regulation requires a higher value than the<br>value set here.|n54<br>0%|75%|20%|
|Min. speed. The voltage for the speed regulation switches||||
|<br>to 0V when the regulation requires a lower value than the<br>|n55<br>0%|50%|10%|
|value set here.<br>||||
|**Alarm**||||
|Delaytime for a A32 alarm|A03<br>0 min.|90 min.|0 min.|
|Low alarm and safetylimit for P0|A11<br>-99°C / -1.0 bar|30°C / 40 bar|-40°C / 0.5 bar|
|Delaytime for a DI1 alarm|A27<br>0 min.(-1=OFF)|999 min.|OFF|
|Delaytime for a DI2 alarm|A28<br>0 min.(-1=OFF)|999 min.|OFF|
|Delaytime for a DI3 alarm|A29<br>0 min.(-1=OFF)|999 min.|OFF|
|Upper alarm and safetylimit for Pc|A30<br>-10 °C / 0.0 bar|200°C/200 bar|60.0°C / 60.0 bar|
|Upper alarm limit for sensor "Saux1"|A32<br>1°C(0=OFF)|140°C|OFF|
|Delaytime for a P0 alarm|A44<br>0 min.(-1=OFF)|999 min.|0 min.|
|Delaytime for a Pc alarm|A45<br>0 min.(-1=OFF)|999 min.|0 min.|
|**Miscellaneous**||||
|Controllers address|o03*<br>1|990||
|On/off switch(service-pin message)|o04*<br>-|-||

* this setting is only possible if data communication module is mounted in the controller

7

|Access code<br>Used sensor type for Sc3, Sc4 and "Saux1"|o05|||1(0=OFF)|100|OFF|
|---|---|---|---|---|---|---|
|<br>**0=**PT1000,**1=**PTC1000<br>2-7=variations with temperature sensor on P0 and Pc. See|o06|||0|7 (1)|0|
|<br>earlier in the manual|||||||
|.<br>Set supplyvoltage frequency|o12|||50 Hz|60 H|0|
|Manual control of outputs:<br>**0:**No override|||||||
|**1-10:**1 will cut in relay 1, 2 relay 2, etc.<br>**11-18:**Gives voltage signal on the analog output. (11<br>|o18|||0|18|0|
|gives 1.25 V,and so on in steps of 1.25 V|||||||
|P0pressure transmitter’s workingrange - min. value|o20|||-1 bar|0 bar|-1.0|
|P0pressure transmitter’s workingrange - max. value<br>f|o21|||1 bar|200 bar|12.0|
|Use o DI4-input<br>**0=**not used.**1=**P0 displacement.**2=**alarm function.<br>Alarm="A31"|o22|||0|2|0|
|Operating hours of relay 1 (value time 1000)|o23|||0.0 h|99.9 h|0.0|
|Operating hours of relay 2 (value time 1000)|o24|||0.0 h|99.9 h|0.0|
|Operating hours of relay 3 (value time 1000|o25|||0.0 h|99.9 h|0.0|
|Operating hours of relay 4 (value time 1000)|o26|||0.0 h|99.9 h|0.0|
|Setting of refrigerant<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.  6=R13.<br>7=R13b1.  8=R23.  9=R500.  10=R503.  11=R114.<br>12=R142b. 13=User defined. 14=R32. 15=R227.<br>16=R401A.  17=R507. 18=R402A.  19=R404A. 20=R407C.<br>21=R407A.  22=R407B.  23=R410A.  24=R170.  25=R290.<br>26=R600.  27=R600a.  28=R744.  29=R1270.  30=R417A.<br>31=R422A. 32=R413A. 33=R422D. 34=R427A. 35=R438A.|o30|||0|35|0|
|Use of DI5-input<br>**0=**not used.**1=**Pc displacment.**2=**alarm function.<br>Alarm="A32"|o37|||0|2|0|
|Pcpressure transmitter’s workingrange - min. value|o47|||-1 bar|0 bar|-1.0|
|Pcpressure transmitter’s workingrange - max. value|o48|||1 bar|200 bar|34.0|
|Read temperature at sensor "Saux1"|o49|||||°C|
|Operating hours of relay 5 (value time 1000)|o50|||0.0 h|99.9 h|0.0|
|Operating hours of relay 6 (value time 1000)|o51|||0.0 h|99.9 h|0.0|
|Operating hours of relay 7 (value time 1000)|o52|||0.0 h|99.9 h|0.0|
|Operating hours of relay 8 (value time 1000)|o53|||0.0 h|99.9 h|0.0|
|Selection of application<br>1. Show temperature and "c16" mode<br>2: Show pressure and "c16" mode<br>3. Show temperature and M&M mode<br>4. Showpressure and M&M mode|o61|1<br>2|3|4<br>1|4|1|
|Function for relay output DO9:<br>0. Start / stop of speed regulation<br>1.  Inject on signal for evaporator control<br>2. Boost ready (at least one compressor is on)<br>3. Start /stopof condenser fan|o75|||0|3|0|
|Function for relay output DO10:<br>0. Alarm relay<br>1. Start / stopof condenser fan|o76|||0|1|0|
|Definition of alarm message at DI1 signal:<br>0. Not used<br>1. Fan failure (A34)<br>2. DI1 alarm(A28)|o78|||0|2|0|
|<br>Settings at water cooler application<br>Definition of signal input to the compressor regulation<br>when regulation with temperature signal:<br>0. Temperature sensor on 57-58<br>1. Temperature sensor on Saux<br>|o81|||0|2|0|
|2. Temperature sensor on Sc4<br>If frost protection is required the setting must be 1 or 2|||||||
|,<br>and apressure transmitter has to be mounted on P0|||||||
|Display connection<br>Off: EKA 164<br>On: EKA 165(extended displaywith light-emittingdiodes)|o82|||Off|On|Off|


|**Service**|||
|---|---|---|
|Status on DI1 input|u10||
|Status on DI2 input|u37||
|Read temperature at sensor "Sc3"|u44|°C|
|Read temperature at sensor "Sc4"|u45|°C|
|Status on DI3 input|u87||
|Status on DI4 input|u88||
|Status on DI5 input|u89||

*[Figurtekst: The controller can give the following messages · E1 Error Fault in controller · message · E2 Regulation is outside the range, or the control · signal is defective * · A2 Alarm  Low P0 · message · A11 Refrigerant not selected · A17 High Pc · A19 Compressor 1 error · A20 Compressor 2 error · A21 Compressor 3 error The actual compressors · safety circuit is · A22 Compressor 4 error interrupted. · A23 Compressor 5 error That is to say the signal · is missing on one of the · A24 Compressor 6 error terminals 29-36 · A25 Compressor 7 error · A26 Compressor 8 error · A27 Room temperature alarm (Saux1 temp.) · A28 DI 1 alarm. Terminal 46 interrupted · A29 DI 2 alarm. Terminal 47 interrupted · A30 DI 3 alarm. Terminal 49 interrupted · A31 DI 4 alarm. Terminal 50 interrupted · A32 DI 5 alarm. Terminal 52 interrupted · A34 Fan alarm. There is no signal on DI1 input · A45 Regulation stopped · S0 Status Regulation · message · S2 Wait for “c01” · S5 Wait for “c07” · S8 Wait for “c11” or “c12” · S9 Wait for “c14” or “c15” · S10 Refrigeration stopped by the internal or external · start/stop function · S25 Manual control of outputs · S34 Safety cutout. Setting A30 is exceeded or all · safety inputs (29-36) are open · PS Info Access code is required before you have access to · the settings]*

Messages can be brought up on the display by briefly pressing the uppermost key. If there is more than one alarm, they can be scrolled through

###### Factory setting

If you need to return to the factory-set values, it can be done in this way:

- Cut out the supply voltage to the controller

- Keep the middle button pressed at the same time as you reconnect the supply voltage

* At water cooler management without frost protection may alarm from a not mounted P0 input suppressed by connecting the signal from the PC (terminal 61) to P0 (terminal 58).

9

**DANSK**

###### **Tilslutninger**

P0/Pc: AKS 32R: 1 = Sort  = + 2 = Blå  = - 3 = Brun  = s Kompressorregulering efter temperatur o06 = 0 o81 = 1 Andre kombinationer: se manual Alle indgange er lavvolt. Alle relæudgange kan være højvolt. Datakommunikation

**Nødvendige tilslutninger Applicationbestemte tilslutninger** Klemme: 20-21 AKD start/stop * 1-2 Forsyningsspænding 24 V a.c.

Relæet slutter når frekvensomformeren skal starte.

4- 19 Relæudgange til enten kompressorer, aflastninger eller ventilatormotorer

- 37-38 Spændingssignal til ekstern kondensatorstyring

   - (se indstillinger side 12)

22-24  Alarmrelæet *

- 39-41 Mulighed for at tilslutte et eksternt display type EKA 163 (Pc-visning)

Der er forbindelse imellem 22 og 24 i alarmsituationer, og når regulatoren er spændingsløs.

- 42-44 Mulighed for at tilslutte et eksternt display type EKA 163 til P0-visning, eller EKA 165 til betjening og P0-visning

27-28 24 V signal til start / stop af reguleringen

- 45-46 DI1 - Kontaktfunktion til alarmsignal

27-29 24 V signal fra sikkerhedskredsen DO 1

- 45-47 DI2 - Kontaktfunktion til alarmsignal

27-30 24 V signal fra sikkerhedskredsen DO 2

- 48-49 DI3 - Kontaktfunktion til alarmsignal

27-31 24 V signal fra sikkerhedskredsen DO 3

- 48-50 DI4 - Kontaktfunktion til forskydning af sugetryksreferencen eller til alarmsignal.

27-32 24 V signal fra sikkerhedskredsen DO 4

27-33 24 V signal fra sikkerhedskredsen DO 5

- 51-52 DI5 - Kontaktfunktion til forskydning af kondensatortryksreferencen eller til alarmsignal.

27-34 24 V signal fra sikkerhedskredsen DO 6

27-35 24 V signal fra sikkerhedskredsen DO 7

- 51-53 Separat føler Saux1. Følersignal fra AKS 11, AKS 12 eller EKS 111

27-36 24 V signal fra sikkerhedskredsen DO 8 57-59 Sugetryk. Spændingssignal fra AKS 32R ** 60-62 Kondensatortryk. Spændingssignal fra AKS 32R **

- 54-55 Udetemperatur (Sc3). Følersignal fra AKS 11, AKS 12 eller EKS 111 (monteres hvis r33 = 2 eller 4).

- 54-56 Lufttemperatur ved kondensatorens afgang. Følersignal fra AKS 11, AKS 12 eller EKS 111

###### **Aflastning**

Hvis en udgang anvendes til en aflastning, er det ikke nødvendigt, at fortråde den tilhørende sikkerhedskreds. Fx. ved en aflastning på DO2 kan en tilslutning på klemme 30 udelades

###### **Datakommunikation**

25-26  Monteres kun, hvis der også er monteret et datakommunikationsmodul.

Hvis det er en ethernetkommunikation skal stiktilslutningen RJ45 anvendes. (LON FTT10 kan også tilsluttes på denne måde.)

Det e r vigtigt, a t installationen af datakommunikationskablet udføres korrekt. Se separat litteratur nr. RC8AC..

Relæerne DO9 og DO10 kan i specialtilfælde omkonfigureres, så de kan anvendes til ventilatorrelæ.

- Hvis regulatoren kun skal styre kompressorer eller kun skal styre ventilatorer, kan Pc henholdsvis Pc føleren undværes.

- På brineanlæg kan der i stedet for trykmåling med AKS 32R anvendes temperaturmåling på klemme 57-58 og 60-61. Se også o06.

10

**Kompressorkonfiguration når o61 = 1 eller 2** (Her kan du vælge imellem de viste muligheder.) Indstilling "c16" vil definere konfigurationen.

*[Figurtekst: Indstilling "c08" vil definere koblingsmåden. · Kompressor tilslutninger Koblings- · måde · Relæ nr Indstil  "C16"  Indstil "C08" · til til]*

###### **Kapacitetstrin**

**Alle** kapacitetstrin forudsættes at være lige store. Eneste undtagelse er indstillingerne c16 = 4 og 21 til 26.

###### **Koblingsmåde**

Koblingsmåde 1 er sekventiel drift. Koblingsmåde 2 er cyklisk drift. Koblingsmåde 3 er cyklisk og binær drift. Hvor kapaciteten på kompressorerne er følgende:

1: 9%

2: 18%

3: 36%

- 4: 36%

- Her kobles der cyklisk på 3 og 4, og binært på 1, 2 og 3/4. (Kun for c16 = 4)

###### **Omkoblinger**

Ved cyklisk drift og tilslutninger med aflastninger, vil der ved nogle kapacitetsindkoblinger være overlapninger, hvor aflastningerne fra enten den ene eller den anden kompressor kunne være aktiv. I disse tilfælde vil aflastningerne på kompressoren med det laveste timetal blive koblet ind, og de andre blive koblet ud. Omkoblingen vil ske med et interval på 6 sekunder.

###### **Udjævnet drift**

Ved c16 = 21 til 26 skal kompressor 1 + den tilhørende aflastning have samme kapacitet som hver af de efterfølgende kompressorer.

Aflastningen vil udglatte den indkoblede kapacitet, når de efterfølgende kompressorer bliver ind- og udkoblet. Kompressor 1 vil altid være i drift.

**Kompressorkonfiguration når o61 = 3 eller 4** (Her skal du selv definere, hvordan relæerne skal aktiveres.)

*[Figurtekst: Oversi g t over relæer i Mix o g  Match drift (Mix og Match anvendes kun på anlæg med op til 4 kompressorer.) · Relæ-nr. Re g neværdi Kombination af relæer, der skal være trukket · 1 1 1 1 1 1 1 1 1 1 · 2 2 2 2 2 2 2 2 2 2 · 3 4 4 4 4 4 4 4 4 4 · 4 8 8 8 8 8 8 8 8 8 · Sum af 1-8 er indstillings- 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 · værdien for hvert trin. · Eksempel 1 Eksempel 2 · Her indstilles:  Hvis kapacitetstrin 1 skal koble relænummer 3 som det eneste, skal du indstille c17 til 4. · c17 til 1 Hvis kapacitetstrin 2 skal koble relæmummer 4 som det eneste, skal du indstille c18 til 8. · c18 til 2 Hvis kapacitetstrin 3 skal koble relæmummer 3 og 4, skal du indstille c19 til 12. · c19 til 3 Fortsæt med en indstilling for c20 osv. indtil alle kapacitetstrin er defineret. · c20 til 4 · c21 til 5 · c22 til 6 · c23 til 7 · Kapacitetstrin]*

11

###### **Kondensatorkoblinger**

Når kompressorrelæerne er lagt fast, kommer turen til ventilatorrelæerne. Det første ledige relæ ( DO1-DO8) bliver det første ventilatorrelæ. Derefter kommer de efterfølgende. Er der flere end de ledige DO-relæer på regulatoren, kan der tilsluttes et relæmodul på den analoge udgang. Funktionen er følgende:

Hvis der er op til 4 eksterne ventilatorer på en EKC 331:

Udgangssignal fra AK-PC 530 I EKC 331 skal spændingsområdet indstilles til 0-5 V ("o10"=6). I EKC 331 skal antal trin indstilles **til 4 ("o19"=4)** (også selv om der er tilsluttet færre ventilatorer).

Tilslutning

Hvis der er flere end 4 eksterne ventilatorer på 2 stk. EKC 331:

Udgangssignal fra AK-PC 530

I den første EKC 331 indstilles 0-5 V ("o10"=6).

I den anden EKC 331 indstilles 5-10 V ("o10"=7).

I **begge** EKC 331 skal antal trin indstilles **til 4  ("o19"=4)** (også selv om der på den anden er tilsluttet færre ventilatorer).

Tilslutning

Skiftevis start af ventilatorer (kun hvis c29 er 11 til 18) Ventilatorerne kan defineres til at starte på skift, når de alle har været stoppet.

Første gang reguleringen startes, vil ventilator 1 blive startet som den første — reguleringen bestemmer, om der skal startes yderligere. Næste gang alle har været stoppet, vil ventilator 2 blive startet som den første o.s.v. Ventilator 1 bliver igen den første, når rotationen har været omkring det **totale** antal ventilatorer.

Hvis der er mere end én ventilator på en EKC 331, vil de resterende ikke kunne starte som den første. Her vil det **altid** være den med det laveste spændingstrin, der er den første.

Hvis hele kondensatorkapaciteten skal styres af en frekvensomformer, skal AK-PC 530 afgive et analogt signal om den ønskede kapacitet ("c29"=9). Signalet varierer fra 0 til 10 V. Signal og kapacitet har følgende sammenhæng.

12

##### **Betjening**

###### **Datakommunikation**

Hvis regulatoren bliver udbygget med datakommunikation kan betjeningen foretages fra en systemenhed.

Vigtigheden af de sendte alarmer kan defineres med indstillingen: 1 (høj), 2 (middel), 3 (lav) eller 0 (ingen alarm).

###### **Betjening via eksternt display**

Værdierne bliver vist med tre cifre, og med en indstilling kan du bestemme, om trykket skal vises i SI-enheder (°C /bar) eller USenheder (°F / psig).

Der er tre muligheder for display

Til betjening af regulatoren og visning af fordampningstrykket. Ved kort tryk på den nederste knap kan kondenseringstrykket vises kortvarigt i displayet. (Hvis der kun reguleres på kondenseringstrykket vil displayet altid vise Pc.)

Under normaldrift viser lysdioderne i displayet hvor reguleringen befinder sig. Øverste + næst øverste : ++Zonen Næst øverste : +Zonen "Ingen" : Neutralzonen Næst nederste : -Zonen Nederste + næst nederste : - - Zonen

De øvrige lysdioder på pladen viser hvilke funktioner, der er aktive:

- Relæer til kompressorer

- Relæer til ventilatorer

- Indgangssignaler på de digitale indgange

- Optimeringslysdioden vil lyse, når referencen er 2 K eller mere over setpunktet.

Hvis der er behov for en konstant visning af kondenseringstrykket, kan der tilsluttes et display uden betjeningsknapper.

###### **EKA 164**

Til betjening af regulatoren og visning af fordampningstrykket. Ved kort tryk på den nederste knap kan kondenseringstrykket vises kortvarigt i displayet. Lysdioderne i displayet vil i lighed med EKA 165 vise, hvor reguleringen befinder sig.

###### Knapperne på displayet

Når du vil ændre en indstilling, vil den øverste og den nederste knap give en højere eller en lavere værdi. Men før du kan ændre værdien, skal du have adgang ind i menuen. Det får du ved at trykke på den øverste knap i et par sekunder – så kommer du ind i rækken med parameterkoder. Find den parameterkode du vil ændre, og tryk så på den midterste knap. Når du har ændret værdien, gemmer du den nye værdi ved igen at trykke på den midterste knap.

###### Eller kort:

1. Tryk på den øverste knap (langt tryk) til der vises en parameter

2. Tryk på en af knapperne og find hen til den parameter, du vil indstille

3. Tryk på den midterste knap så indstillingsværdien vises

4. Tryk på en af knapperne og vælg den nye værdi

5. Tryk igen på den midterste knap for at afslutte indstillingen.

(Et kort tryk vil vise de alarmkoder, der er aktive.)

13

##### **Menuoversigt**

###### **Rækkefølge**

**1.** o61 **skal** indstilles som den første parameter. Den bestemmer hvilke af de 4 betjeningsflader, der bliver aktiveret. Den **skal** indstilles via displayets knapper. Den kan **ikke** indstilles via datakommunikation. (Aktive funktioner er vist herunder med tonede felter.)

**2.** Quick- start

Hvis du vil have anlægget igang i en fart, så nedkølingen kan påbegyndes, kan du starte med at indstille følgede parametre (de kan kun indstilles, når reguleringen er stoppet, **r12=0** ):

r23, r28 og så enten(c08, c09 og c16) eller(c17 til 28) - fortsæt med c29, o06, o30, o75, o76, o81 **og til sidst r12=1** .

**3.** Når reguleringen derefter er igang, kan du gå igennem de øvrige parametre og justere dem på plads.

SW: 1.3x

|**Funktion**|**Para-**<br>|**o61**|**=**||**Min.**|**Max.**|**Fabriks-**<br>|
|---|---|---|---|---|---|---|---|
||**meter**|**1**<br>**2**|**3**|**4**|||**indstilling**|
|**Normalbillede**||||||||
|P0 vises i EKA 165(den med betjeningsknapper)|-|°C<br>P|°C|P||°C / bar||
|Pc vises i EKA 163|-|°C<br>P|°C|P||°C / bar||
|**P0 reference**||||||||
|Neutralzone<br>|r01||||0.1°C / 0.1 bar|20°C /5.0 bar|4.0°C / 0.4 bar|
|Korrektion af signalet fra P0-føleren|r04||||-50°C /-5.0 bar|50°C / 5.0 bar|0.0|
|VælgSI eller US visning0=SI(bar,°C). 1=US(Psig/ °F)|r05||||0|1|0|
|Start/Stopaf kølingen|r12||||OFF|ON|OFF|
|Referenceoffset for P0 (se også r27)|r13||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Setpunktindstillingen for P0|r23||||-99°C / -1 bar|30°C / 60.0 bar|0.0°C / 3.5 bar|
|Her vises den samlede P0-reference<br>(r23 + diverse forskydninger)|r24|||||°C / bar||
|Begrænsning: P0-referencens max. værdi<br>(gælder også ved reguleringmed referenceforskydning)|r25||||-99°C / -1.0 bar|30°C / 60.0 bar|30.0°C / 40.0 bar|
|Begrænsning: P0-referencens min. værdi<br>|r26||||-99°C / -1.0 bar|30°C / 40.0 bar|-99.9°C / -1.0 bar|
|(gælder også ved reguleringmed referenceforskydning)||||||||
|Forskydningaf P0 (ON=aktiv "r13")|r27||||OFF|ON|OFF|
|**Pc reference**||||||||
|Setpunktsindstillingen for Pc|r28||||-25°C / 0.0 bar|75°C / 110.0 bar|35°C / 15.0 bar|
|Her vises den samlede Pc-reference|r29|||||°C / bar||
|Begrænsning: Pc-referencens max. værdi|r30||||-99.9°C / -0.0 bar|99.9°C/130.0bar|55.0°C / 60.0 bar|
|Begrænsning: Pc-referencens min. værdi|r31||||-99.9°C / 0.0 bar|99.9°C / 60.0 bar|-99.9°C / 0.0 bar|
|Korrektion af signalet fra Pc-føleren<br>|r32||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Pc-referencens variation.<br>1 og 2 er PI regulering<br>1: Fast reference.  "r28" anvendes<br>2: Variabel reference. Udetemperaturen (Sc3) indgår i<br>referencen<br>3: Som 1, men med P-regulering (Xp-bånd)|r33||||1|4|1|
|4: Som 2,men med P-regulering (Xp-bånd)||||||||
|Referenceoffset for Pc|r34||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Middeltemperaturdifferencen over kondensatoren ved<br>maksimium belastning (dim tm K)|r35||||3.0|50.0|10.0|
|Middeltemperaturdifferencen over kondensatoren ved<br>den laveste aktuelle kompressorkapacitet(min tm K)|r56||||3.0|50.0|8.0|
|Her kan du aflæse det aktuelle tryk (P0), der måles med<br>tryktransmitteren|r57|||||°C / bar||
|Her kan du aflæse det aktuelle tryk (T0), der indgår i regu-<br>leringen.  Fra føleren der er defineret i "o81"|r58|||||°C||
|**Kapacitet**||||||||
|Min. On-tid for relæer|c01||||0 min|30 min.|0|
|Min.periodetid imellem indkoblingaf det samme relæ|c07||||0  min.|60 min|4|
|Definition af reguleringsmåden||||||||
|1: Sekventiel (step mode / FILO)<br>2: Cyklisk (step mode / FIFO)<br>3: Binær ogcyklisk|c08||||1|3|1|
|Hvis der vælges en reguleringsmåde med aflastninger<br>skal relæet defineres til at:<br>0: Slutte ved krav om mere kapacitet|c09||||0|1|0|
|1: Bryde ved krav om mere kapacitet||||||||
|Reguleringsparameter for + Zone|c10||||0.1 K / 0.1 bar|20 K / 2.0 bar|4.0 / 0.4 bar|

Fortsættes

14

|Reguleringsparameter for + Zone<br>|c11<br>0.1 min<br><br>|60 min<br>|4.0<br>|
|---|---|---|---|
|Reguleringsparameter for ++ Zone|c12<br>0.1 min.|20 min|2.0|
|Reguleringsparameter for - Zone|c13<br>0.1 K / 0.1 bar|20 K / 2.0 bar|4.0 / 0.3 bar|
|Reguleringsparameter for - Zone|c14<br>0.1 min.|60 min|1.0|
|Reguleringsparameter for - -  Zone|c15<br>0.02 min.|20 min|0.5|
|Definition af kompressortilslutninger.<br>Se mulighederne side 11.|c16<br>1|26|0|
|Følgende "c17" til "c28" er en anden måde, at definere kom-<br>pressorer på end med "c16".<br>Der skal her indstilles en kode for hvilke relæer, der er on|c17<br>0|15|0|
|<br>ved de forskellige step: Step1(M&M drift)||||
|Step2(M&M drift)<br>|c18<br>0|15|0|
|Step3(M&M drift)<br>Step4(M&M drift)|c19<br>0<br>c20<br>0|15<br>15|0<br>0|
|Step5(M&M drift)|c21<br>0|15|0|
|Step6(M&M drift)|c22<br>0|15|0|
|Step7(M&M drift)|c23<br>0|15|0|
|Step8(M&M drift)|c24<br>0|15|0|
|Step9(M&M drift)|c25<br>0|15|0|
|Step10(M&M drift)|c26<br>0|15|0|
|Step11(M&M drift)|c27<br>0|15|0|
|Step12(M&M drift)<br>i|c28<br>0|15|0|
|Definition af kondensator:||||
|i<br>**1-8:**Total antal ventilatorrelæer eller spændingstrin på<br>spændingsudgangen||||
|**9:**Kun via analog udgang og start af frekvensomformer<br>**10:**Benyttes ikke<br>**11- 18:**Total antal ventilatorrelæer, der skal koble med|c29<br>0/OFF|18|0|
|skiftevis start||||
|Indkoblet kompressorkapacitet ved manuel styring. Se<br>også "c32"|c31<br>0%|100%|0|
|Manuel styring af kompressorkapacitet (ved ON bliver<br>værdien i "c31" anvendt)|c32<br>OFF|ON|OFF|
|Pump down grænse. Grænseværdi hvor den sidste kom-<br>pressor bliver udkoblet|c33<br>-99.9°C / -1.0 bar|100°C / 60 bar|100°C / 60 bar|
|Proportionalbånd Xp for (P = 100/Xp) kondensatorregu-<br>leringen|n04<br>0.2 K / 0.2 bar|40.0 K / 10.0 bar|10.0 K / 3.0 bar|
|I: Integrationstid Tn for kondensatorreguleringen|n05<br>30 s|600 s|150|
|Indkoblet kondensatorkapacitet ved manuel styring. Se<br>også "n53"|n52<br>0%|100%|0|
|Manuel styring af kondensatorkapacitet (ved ON bliver<br>værdien i "n52" anvendt)|n53<br>OFF|ON|OFF|
|Start hastighed. Spændingen til hastighedsreguleringen<br>bliver holdt på 0 V, indtil reguleringen kræver en højere<br>værdi end den her indstillede|n54<br>0%|75%|20%|
|Min.  hastighed. Spændingen til hastighedsreguleringen<br>||||
|skifter til 0 V, når reguleringen kræver en lavere værdi end|n55<br>0%|50%|10%|
|den her indstillede||||
|**Alarm**||||
|Forsinkelsestid for en A32 alarm|A03<br>0 min.|90 min.|0 min.|
|Nedre alarm- ogsikkerhedsgrænse for P0<br>Forsinkelsestid for en DI1-alarm|A11<br>-99°C / -1.0 bar<br>A27<br>0 min.(-1=OFF)|30°C / 40 bar<br>999 min.|-40°C / 0.5 bar<br>OFF|
|Forsinkelsestid for en DI2-alarm|A28<br>0 min.(-1=OFF)|999 min.|OFF|
|Forsinkelsestid for en DI3-alarm|A29<br>0 min.(-1=OFF)|999 min.|OFF|
|Øvre alarm- ogsikkerhedsgrænse for Pc|A30<br>-10 °C / 0.0 bar|200 °C / 200 bar|60.0°C / 60.0 bar|
|Øvre alarmgrænse for føleren "Saux1"|A32<br>1°C(0=OFF)|140°C|OFF|
|Forsinkelsestid for en P0 alarm|A44<br>0 min.(-1=OFF)|999 min.|0 min.|
|Forsinkelsestid for en Pc alarm|A45<br>0 min.(-1=OFF)|999 min.|0 min.|
|**Diverse**||||
|Regulatorens adresse|o03*<br>1|990||
|On/off omskifter(service-pin meddelelse)|o04*<br>-|-||
|f <br>Adgangskode|o05<br>1(0=OFF)|100|OFF|

*) Denne indstilling vil kun være mulig, hvis der er monteret et datakommunikationsmodul i regulatoren.

Fortsættes

15

|Anvendt følertype til Sc3, Sc4 og "Saux1"<br>**0=**Pt1000,**1=**PTC1000<br>2-7= variationer med temperaturføler på P0 og Pc. Se<br>tidligere i manualen.|o06|||0|7 (1)|0|
|---|---|---|---|---|---|---|
|Indstille forsyningsspændingens frekvens|o12|||50 Hz|60 H|0|
|Manuel styring af udgange:<br>**0:**Ingen overstyring<br>**1-10:**1 vil trække relæ 1, 2 relæ 2, osv.<br>**11-18:**Giver spændingssignal på den analoge udgang.<br>(11giver 1,25 V ogellers videre i step på 1,25 V.)|o18|||0|18|0|
|P0-tryktransmitterens arbejdsområde - min. værdi|o20|||-1 bar|0 bar|-1.0|
|P0-tryktransmitterens arbejdsområde - max. værdi<br>|o21|||1 bar|200 bar|12.0|
|DI4-indgangens anvendelse<br>**0=**benyttes ikke.**1=**P0-forskydning.**2=**alarmfunktion.<br>Alarm="A31"|o22|||0|2|0|
|Driftstid af relæ 1 (værdi gange 1000)|o23|||0.0 h|99.9 h|0.0|
|Driftstid af relæ 2 (værdi gange 1000)|o24|||0.0 h|99.9 h|0.0|
|Driftstid af relæ 3 (værdi gange 1000)|o25|||0.0 h|99.9 h|0.0|
|Driftstid af relæ 4 (værdi gange 1000)|o26|||0.0 h|99.9 h|0.0|
|Kølemiddelindstilling<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.  6=R13.<br>7=R13b1.  8=R23.  9=R500.  10=R503.  11=R114.<br>12=R142b. 13=Brugerdefineret. 14=R32. 15=R227.<br>16=R401A.  17=R507. 18=R402A.  19=R404A. 20=R407C.<br>21=R407A.  22=R407B.  23=R410A.  24=R170.  25=R290.<br>26=R600.  27=R600a.  28=R744.  29=R1270.  30=R417A.<br>31=R422A. 32=R413A. 33=R422D. 34=R427A. 35=R438A.|o30|||0|35|0|
|DI5-indgangens anvendelse<br>**0=**benyttes ikke.**1=**Pc-forskydning.**2=**alarmfunktion.<br>Alarm="A32"|o37|||0|2|0|
|Pc-tryktransmitterens arbejdsområde - min. værdi|o47|||-1 bar|0 bar|-1.0|
|Pc-tryktransmitterens arbejdsområde - max. værdi|o48|||1 bar|200 bar|34.0|
|Aflæse temperaturen ved føleren "Saux1"|o49|||||°C|
|Driftstid af relæ 5 (værdi gange 1000)|o50|||0.0 h|99.9 h|0.0|
|Driftstid af relæ 6 (værdi gange 1000)|o51|||0.0 h|99.9 h|0.0|
|Driftstid af relæ 7 (værdi gange 1000)|o52|||0.0 h|99.9 h|0.0|
|Driftstid af relæ 8 (værdi gange 1000)|o53|||0.0 h|99.9 h|0.0|
|Valg af application<br>1. Temperaturvisning og "c16" mode<br>2: Trykvisning og "c16" mode<br>3. Temperaturvisning og M&M mode|o61|1<br>2|3<br>4|1|4|1|
|4. TrykvisningogM&M mode|||||||
|Funktion for relæudgang DO9:<br>0. Start / stop af hastighedsstyring<br>1.  Inject on signal til fordamperstyringer<br>2. Boost ready (mindst en kompressor er on)<br>3. Start /stopaf kondensatorblæser|o75|||0|3|0|
|Funktion for relæudgang DO10:<br>0. Alarmrelæ<br>1. Start / stopaf kondensatorblæser|o76|||0|1|0|
|Definition af alarmmeddelelse ved DI1-signal:<br>0. Benyttes ikke<br>1. Blæser fejl (A34)<br>2. DI1 alarm(A28)|o78|||0|2|0|
|Indstilling ved vandkøleranvendelse<br>Definition af signalindgang til kompressor-reguleringen,<br>når der reguleres med temperatursignal:<br>0. Temperaturføler til 57-58<br>1. Temperaturføler til Saux<br>2. Temperaturføler til Sc4<br>Kræves frostsikring skal indstillingen være 1 eller 2, og der<br>skal monteres en tryktransmitterpå P0.|o81|||0|2|0|
|Displaytilslutning<br>Off: EKA 164<br>On: EKA 165(udvidet displaymed lysdioder)|o82|||Off|On|Off|

16

|**Service**|||
|---|---|---|
|Statuspå DI1-indgangen|u10||
|Statuspå DI2-indgangen|u37||
|Aflæse temperaturen ved føleren "Sc3"|u44|°C|
|Aflæse temperaturen ved føleren "Sc4"|u45|°C|
|Statuspå DI3-indgangen|u87||
|Statuspå DI4-indgangen|u88||
|Statuspå DI5-indgangen|u89||

*[Figurtekst: Re g ulatoren kan  g ive føl g ende meddelelser: · E1 Fejl- Fe j l i re g ulatoren · meddelelse Reguleringen er uden for området, eller styre- · E2 · si g nalet er defekt * · A2 Alarm- Lav P0 · A11 meddelelse Der er ikke val g t kølemiddel · A17 Hø j  Pc · A19 Kom p ressor 1 fe j l · A20 Kom p ressor 2 fe j l · Den aktuelle kompres- · A21 Kom p ressor 3 fe j l sors sikkerhedskreds er · A22 Kom p ressor 4 fe j l afbrudt. · A23 Kom p ressor 5 fe j l Dvs. der mangler signal · A24 Kom p ressor 6 fe j l på en af klemmerne · 29-36. · A25 Kom p ressor 7 fe j l · A26 Kom p ressor 8 fe j l · A27 Rumtem p eraturalarm (Saux1 tem p .) · A28 DI 1 alarm. Klemme 46 er afbrudt · A29 DI 2 alarm. Klemme 47 er afbrudt · A30 DI 3 alarm. Klemme 49 er afbrudt · A31 DI 4 alarm. Klemme 50 er afbrudt · A32 DI 5 alarm. Klemme 52 er afbrudt · Blæseralarm. Der er ingen signal på DI1- · A34 · ind g an g en · A45 Re g ulerin g en er sto pp et · S0 Status- Der re g uleres · S2 meddelelser Afventer "c01" · S5 Afventer "c07" · S8 Afventer "c11" eller "c12" · S9 Afventer "c14" eller "c15" · Kølingen er stoppet med den interne eller · S10 · eksterne start/sto p · S25 Manuel st y rin g  af ud g an g e · Sikkerhedsudkobling. · S34 Indstilling A 30 er overskredet, eller alle sikker- · hedsind g an g e  ( 29-36 )  er åbne. · Adgangskoden er påkrævet inden du får adgang · PS Info · til indstillin g er.]*

Meddelelser kan kaldes frem i displayet ved et kort tryk på den øverste knap. Er der mere end en alarm, kan de "rulles" igennem.

###### Fabriksindstilling

Hvis du får behov for at vende tilbage til de fabriksindstillede værdier, kan det ske således:

- Afbryd forsyningsspændingen til regulatoren

- Hold den midterste knap inde samtidig med at du igen tilslutter forsyningsspændingen.

*) Ved vandkølerstyring uden frostsikring kan alarmen fra en ikke monteret P0indgang undertrykkes ved at forbinde signalet fra PC (klemme 61) til P0 (klemme 58).

17

**DEUTSCH**

###### **Anschlüsse**

P0/Pc: AKS 32R: 1 = Schwarz = + 2 = Blau  = - 3 = Braun = s Verdichterregelung nach Temperatur

o06 = 0 o81 = 1 Andere Kombinationen: siehe das Manual Alle Eingänge sind nur für Niederspannung geeignet. Alle Relaisausgänge sind für Hochspannung ausgelegt. Datenkommunikation

###### **Benötigte Anschlüsse** Klemme:

- 1-2 Versorgungsspannung 24 V a.c.

4- 19 Relaisausgänge für entweder Verdichter, Entlastungen oder Lüftermotoren

22-24  Alarmrelais *

Es besteht Verbindung zwischen 22 und 24 in Alarmsituationen, und wenn der Regler Spannungslos ist.

27-28 24 V Signal für Start / Stop der Regelung 27-29 24 V Signal vom Sicherheitskreis DO 1

27-30 24 V Signal vom Sicherheitskreis DO 2

27-31 24 V Signal vom Sicherheitskreis DO 3

27-32 24 V Signal vom Sicherheitskreis DO 4

27-33 24 V Signal vom Sicherheitskreis DO 5

27-34 24 V Signal vom Sicherheitskreis DO 6

27-35 24 V Signal vom Sicherheitskreis DO 7

27-36 24 V Signal vom Sicherheitskreis DO 8

57-59 Saugdruck. Spannungssignal vom AKS 32R **

60-62 Verflüssigungsdruck. Spannungssignal vom AKS 32R **

**Anwendungsbestimte Anschlüsse** 20-21 AKD Start/stop *

Das Relais schliesst wenn der Frequenzumrichter starten soll.

37-38 Spannungssignal für eksterne Verflüssigerregelung (Siehe Einstellungen Seite 20)

- 39-41 Anschlussmöglichkeit für ein eksternes Display von Typ EKA 163 (Pc-anzeige)

- 42-44 Anschlussmöglichkeit für ein eksternes Display von Typ EKA 163 für P0-anzeige, oder EKA 165 zur Bedienung und P0-Anzeige

45-46 DI1 - Kontaktfunktion für Alarmsignal

45-47 DI2 - Kontaktfunktion für Alarmsignal

48-49 DI3 - Kontaktfunktion für Alarmsignal

- 48-50 DI4 - Kontaktfunktion für verschiebung des Saugdruck Sollwerts oder für Alarmsignal.

51-52 DI5 - Kontaktfunktion für verschiebung  des Verflüssigerdruck Sollwerts oder für Alarmsignal.

- 51-53 Separate Fühler Saux1. Fühlersignal von AKS 11, AKS 12 oder EKS 111

54-55 Aussentemperatur (Sc3). Fühlersignal vom AKS 11, AKS 12 oder EKS 111 (wird montiert wenn r33 =2 oder 4 ist)

54-56 Lufttemperatur am Verflüssiger abgang. Fühlersignal von AKS 11, AKS 12 oder EKS 111

###### **Entlastungen**

###### **Datenkommunikation**

Wird ein Ausgang für eine Entlastung benutzt, ist Verdrahtung zu den zugehörigen Sicherheitskreis nicht notwendig. z.B. bei einer Entlastung auf DO2 kann ein Anschluss an Klemme 30 ausgelassen werden

Die Relais DO9 und DO10 lassen sich in speziellen Fällen umkonfigurieren, um  als Lüfterrelais eingesetzt werden zu können.

25-26  Nur bei montiertem Datenkommunikationsmodul anzuschließen.

Erfolgt die Kommunikation über ein Ethernet, sind Steckanschlüsse RJ45 anzuwenden. (LON FTT10 kann ebenfalls auf diese Weise angeschlossen werden.) Bitte beachten, dass die Installation des Datenkommunikationskabels korrekt vorgenommen wird. Siehe separate Literatur Nr. RC8AC..

- Wenn der Regler nur die Verdichter oder die Lüfter regeln soll, kann Pc beziehungsweise Pc Fühler entbehrt werden.

- Bei Soleanlagen kann anstatt der Druckmessung mittels AKS 32R eine Temperaturmessung an den Klemmen 57-58 und 60-61 erfolgen. Siehe auch o06.

18

**Verdichterkonfiguration wenn = 1 oder 2** (Hier haben Sie die Auswahl unter den gezeigten Möglichkeiten.) Einstellung "c16" wird die Konfiguration definieren Einstellung "c08" wird die Konfiguration definieren

*[Figurtekst: Verdichteranschluss Schal- · tungsart · Relais Nr. Einstell  "C16"  Einstell "C08"]*

###### **Leistungsstufen**

Es wird vorausgesetzt, dass **alle** Leistungsstufen gleich groß sind. Einzige Ausnahme sind die Einstellungen c16 = 0, 4 und 21 bis 26.

###### **Schaltungsart**

Schaltungsart 1 gilt für sequenziellen Betrieb.

Schaltungsart 2 gilt für zyklischen Betrieb. Schaltungsart 3 gilt für zyklischen und binären  Betrieb. Bei folgenden Verdichterleistungen:

1: 9% 2: 18%

3: 36% 4: 36%

Hier wird zyklisch auf 3 und 4 geschaltet, und binär auf 1, 2 und 3/4. (Nur bei c16 = 4)

###### **Umschaltungen**

Bei zyklischem Betrieb und Anschlüssen mit Entlastungen treten bei bestimmten Leistungszuschaltungen Überlappungen

auf, wobei die Entlastungen entweder des einen oder anderen Verdichters aktiv sein können.

In diesen Fällen werden die Entlastungen des Verdichters mit der niedrigsten Betriebsstundenzahl ein- und die anderen abgeschaltet. Die Umschaltung erfolgt mit einem Intervall von 6 Sekunden.

###### **Ausgeglichener Betrieb**

Bei c16 = 21 bis 26 muss Verdichter 1 + die zugehörige Entlastung die gleiche Leistung haben, wie jeder der nachfolgenden Verdichter.

Die Entlastung gleicht die zugeschaltete Leistung aus, wenn die nachfolgenden Verdichter zu- und abgeschaltet werden. Verdichter 1 ist immer in Betrieb.

###### **Verdichterkonfiguration wenn o61 = 3 oder 4** (Hier können Sie festlegen, auf welche Weise die Relais aktiviert werden sollen.)

*[Figurtekst: Übersicht über Relais in Mix und Match Betrieb (Mix und Match wird nur in Anlagen mit bis zu 4 Verdichtern · Kalkulations- verwendet.) · Relais-Nr. faktor Kombination der Relais, die angezogen sein sollen · 1 1 1 1 1 1 1 1 1 1 · 2 2 2 2 2 2 2 2 2 2 · 3 4 4 4 4 4 4 4 4 4 · 4 8 8 8 8 8 8 8 8 8 · Die Summe von 1-8 ist der · 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 · Einstellwert für jede Stufe · Beispiel 1 Beispiel 2 · Hier einstellen:  Soll bei Leistungsstufe 1 nur die Relaisnummer 3 geschaltet werden, ist c17 auf 4 · c17 bis 1 einzustellen. · c18 bis 2 Soll bei Leistungsstufe 2 nur die Relaisnummer 4 geschaltet werden, ist c18 auf 8 · c19 bis 3 einzustellen. · c20 bis 4 · Leistungsstufe]*

Beispiel 2 Hier einstellen: Soll bei Leistungsstufe 1 nur die Relaisnummer 3 geschaltet werden, ist c17 auf 4 c17 bis 1 einzustellen. c18 bis 2 Soll bei Leistungsstufe 2 nur die Relaisnummer 4 geschaltet werden, ist c18 auf 8 c19 bis 3 einzustellen. c20 bis 4 Sollen bei Leistungsstufe 3 die Relaisnummern 3 und 4 geschaltet werden, ist c19 auf 12 c21 bis 5 einzustellen. c22 bis 6 Bitte mit der Einstellung von c20 usw. fortsetzen, bis alle Leistungsstufen festgelegt sind. c23 bis 7

19

###### **Verflüssigerschaltungen**

Nachdem die Verdichterrelais festgelegt wurden, sind die Lüfterrelais an der Reihe.

Das erste freie Relais ( DO1-DO8) wird zum ersten Lüfterrelais. Anschließend alle weiteren. Werden mehr als die freien DO-Relais am Regler benötigt, kann am Analogausgang ein Relaismodul mit folgender Funktion angeschlossen werden:

Wenn mehr als 4 externe Lüfter bei einem EKC 331 vorhanden sind:

Wenn mehr als 4 externe Lüfter an 2 EKC 331 angeschlossen sind:

###### Ausgangssignal vom AK-PC 530

In EKC 331 ist der Spannungsbereich auf 0-5 V (“o10”=6) einzustellen. In EKC 331 ist die Stufenanzahl **auf 4 (“o19”=4)** einzustellen (auch, wenn weniger Lüfter angeschlossen sein sollten).

###### Anschluss

Ausgangssignal vom AK-PC 530

Ist im ersten EKC 331 auf 0-5 V (“o10”=6) einzustellen.

Ist im zweiten EKC 331 auf 5-10 V (“o10”=7) einzustellen.

In **beiden** EKC 331 ist die Stufenanzahl **auf 4 (“o19”=4)** einzustellen (auch, wenn weniger Lüfter angeschlossen sein sollten).

Anschluss

Wechselweiser Start der Lüfter (nur wenn c29 11 bis 18 ist) Es kann definiert werden, dass die Lüfter wechselweise starten, wenn alle angehalten waren.

Beim ersten Anlaufen der Regelung wird Lüfter 1 als erstes gestartet – die Regelung bestimmt, ob weitere gestartet werden müssen. Beim nächsten Mal, wenn alle angehalten haben, wird Lüfter 2 als erstes gestartet usw.

Lüfter1 ist dann wieder als erste Lüfter gestartet, wenn alle Lüfter als erste gestartet worden sind.

Wenn sich an einem EKC 331 mehr als ein Lüfter befindet, kann kein wechselweiser Start stattfinden. Hier ist immer der Lüfter mit der niedrigsten Spannungsstufe als erster gestartet.

Soll die gesamte Verflüssigerleistung mit einem Frequenzumrichter geregelt werden, muss AK-PC 530 ein der gewünschten Leistung entsprechendes analoges Signal (“c29”=9) abgeben.

Das Signal variiert von 0 bis 10 V. Signal und Leistung hängen wie folgt zusammen.

20

##### **Bedienung**

###### **Datenkommunikation**

Wenn der Regler um Datenkommunikation erweitert wird, kann die Bedienung von der Systemeinheit aus erfolgen. Die Wichtigkeit der übermittelten Alarme kann mit folgenden Einstellungen definiert werden: 1 (hoch), 2 (mittel), 3 (niedrig) oder 0 (kein Alarm).

###### **Bedienung durch externes Display**

Die Wertdarstellung erfolgt dreistellig. Es besteht die Wahl zwischen Anzeige in SI-Einheiten (°C / Bar) oder ob die Anzeige in US-Einheiten (°F / psig) sein soll. Es gibt drei verschiedene Displays

Zur Bedienung des Reglers und zur Anzeige des Verdampfdrucks. Durch Antippen der unteren Taste wird der Verflüssigungsdruck kurz im Display angezeigt. (Wenn nur der Verflüssigungsdruck geregelt wird, zeigt das Display immer Pc.)

|Bei Normalbetrieb zeigen di<br>|e Leuchtdioden im Display den Regel-|
|---|---|
|zustand an.||
|Oberste + zweitoberste|:<br>++Zone|
|Zweitoberste|:<br>+Zone|
|"Keine"|:<br>Neutralzone|
|Zweitunterste|:<br>-Zone|
|Unterste + zweitunterste|:<br>- - Zone|

Die sonstigen Leuchtdioden auf der Tafel zeigen, welche Funktionen aktiv sind:

- Relais für Verdichter

- Relais für Lüfter

- Eingangssignale an den digitalen Eingängen

- Die LED „Optimierung“ leuchtet auf, wenn der Wert 2 K oder mehr über dem Sollwert liegt.

Wenn Bedarf an einer konstanten Anzeige des Verflüssigungsdrucks besteht, kann ein Display ohne Bedientasten angeschlossen werden.

###### **EKA 164**

Zur Bedienung des Reglers und zur Anzeige des Verdampfdrucks. Durch Antippen der unteren Taste wird der Verflüssigungsdruck kurz im Display angezeigt.

Die Leuchtdioden im Display zeigen wie beim EKA 165 an, wo die Regelung steht.

###### **Tasten am Display**

Mit den Tasten lassen sich die Einstellungen ändern. Je nachdem, welche Taste Sie betätigen, ergibt sich ein höherer oder niedrigerer Wert. Bevor Werte geändert werden können, muss Zugang zum Menü hergestellt werden. Durch einige Sekunden langes Betätigen der obersten Taste erhält man Zugang zu einer Reihe von Parametercodes. Wählen Sie den zu ändernden Parametercode aus, und betätigen Sie anschließend die mittlere Taste. Nach Änderung des Werts lässt sich der neue Wert speichern, indem erneut die mittlere Taste betätigt werden.

Kurz zusammengefasst:

1. Die oberste Taste betätigen (lange drucken), bis ein Parameter zur Anzeige gelangt.

2. Eine der Tasten betätigen, um zum gewünschten Parameter zu gelangen.

3. Die mittlere Taste betätigen, bis der Wert des Parameters zur Anzeige kommt.

4. Eine der Tasten betätigen, und einen neuen Wert festlegen.

5. Erneut die mittlere Taste betätigen, um den Einstellvorgang zu beenden.

(Ein kurzes Drücken zeigt, welche Alarmmitteilungen aktiv sind.)

21

##### **Menüübersicht**

###### **Reihenfolge**

**1.** o61 muss als erster Parameter eingestellt werden. Er bestimmt, welche der 4 Bedienflächen aktiviert wird. Er muss über die Tasten des Displays eingestellt werden. Er kann nicht per Datenkommunikation eingestellt werden. (Aktive Funktionen werden untenstehend grau hinterlegt angezeigt.)

**2.** Schnell-Start

Soll die Anlage schnell angefahren werden, um die Abkühlung zu beginnen, lassen sich folgende Parameter einstellen. (Sie lassen sibh nur Einstellen, wenn die Regelung gestoppt ist, r12=0):

r23, r28 und dann entenweder(c08, c09 und c16) oder (c17 bis 28) - fortsetzen mit c29, o06, o30, o75, o76, o81 und zuletzt r12=1.

**3.** Nach Anlauf der Regelung kann sie mittels der übrigen Parameter zweckgemäß eingestellt werden.

SW: 1.3x

|**Funktion**|**Para-**<br>||**o61**<br>|**=**<br>||**Min.**|**Max.**|**Werks-**<br>|
|---|---|---|---|---|---|---|---|---|
||**meter**|**1**|**2**|**3**|**4**|||**einstellung**|
|**Normalbild**|||||||||
|P0 anzeige in EKA 165(mit Bedienungstasten)|-|°C|P|°C|P|°C / bar|||
|Pc anzeige in EKA 163|-|°C|P|°C|P|°C / bar|||
|**P0 Sollwert**|||||||||
|Neutralzone|r01|||||0.1°C / 0.1 bar|20°C /5.0 bar|4.0°C / 0.4 bar|
|Korrektion des Signals vom P0 Fühler|r04|||||-50°C /-5.0 bar|50°C / 5.0 bar|0.0|
|Wähle SI oder US Anzeige. 0=SI(bar/°C). 1=US(Psig/°F)|r05|||||0|1|0|
|Start/Stopder Regelung|r12|||||OFF|ON|OFF|
|Sollwert offset für P0 (siehe auch r27)|r13|||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Setpunkt-Einstellungfür P0|r23|||||-99°C / -1 bar|30°C / 60.0 bar|0.0°C / 3.5 bar|
|Hier wird die gesamte P0-sollwert angeziegt<br>(r23 + diverse Verschiebungen)|r24||||||°C / bar||
|Begrenzung: P0-Sollwert max. Wert<br>(gilt auch bei Regelungmit Sollwert Verschiebung)|r25|||||-99°C / -1.0 bar|30°C / 60.0 bar|30.0°C / 40.0 bar|
|Begrenzung: P0-Sollwert min. Wert<br>il h bi Rli Sll Vhib|r26|||||-99°C / -1.0 bar|30°C / 40.0 bar|-99.9°C / -1.0 bar|
|(gt auc e egeungmt owert ersceung)|||||||||
|Verschiebungdes P0 (ON=aktiv "r13")|r27|||||OFF|ON|OFF|
|**Pc Sollwert**|||||||||
|Setpunkt-Einstellungfür Pc|r28|||||-25°C / 0.0 bar|75°C / 110.0 bar|35°C / 15.0 bar|
|Hier wird diegesamte Pc-sollwert angeziegt|r29||||||°C / bar||
|Begrenzung: Pc-Sollwert max. Wert|r30|||||-99.9°C / -0.0 bar|99.9°C/130.0bar|55.0°C / 60.0 bar|
|Begrenzung: Pc-Sollwert min. Wer|r31|||||-99.9°C / 0.0 bar|99.9°C / 60.0 bar|-99.9°C / 0.0 bar|
|Korrektion des Signals vom Pc Fühler|r32|||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Pc-Sollwert Variation.<br>1 und 2 sind PI-Regelung<br>1: Fester Sollwert.  "r28" wird verwendet<br>2: Variabler Sollwert. Aussentemperatur (Sc3) ist im Soll-<br>wert eingeschlossen<br>3: Wie 1, aber mit P-Regelung (Xp-Band)|r33|||||1|4|1|
|4: Wie 2,aber mit P-Regelung (Xp-Band)|||||||||
|Sollwert offset für Pc|r34|||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Die mittlere Temperaturdifferenz über dem Verflüssiger<br>bei maximaler Belastung (dim tm K)|r35|||||3.0|50.0|10.0|
|Die mittlere Temperaturdifferenz über dem Verflüssiger<br>bei niedrigster aktueller Verdichterleistung (min tm K)|r56|||||3.0|50.0|8.0|
|Hier lässt sich der aktuelle, mit dem Druckmessumformer<br>ermittelte Druck(P0)ablesen.|r57||||||°C / bar||
|Hier lässt sich der aktuelle Druck (T0) ablesen, der mit<br>i|r58||||||°C||
|dem Fühler(definiert in o81)ermittelt wurde.|||||||||
|**Leistung**|||||||||
|Min. On-Zeit für Relais|c01|||||0 min|30 min.|0|
|Min. Periodendauer zwischen Zusschaltungen  des<br>gleichen Relais|c07|||||0  min.|60 min|4|
|<br>Festlegung des Regelverfahrens<br>1: Sequenziell  (step mode / FILO)<br>2: Zyklisch (step mode / FIFO)<br>|c08|||||1|3|1|
|3: Binär und Zyklisch|||||||||
|<br>Wenn ein Regelverfahren mit Entlastungen gewählt wird<br>müssen die Relais wie folgt festgelegt werden:<br>0: Schliesen bei Mehrbedarf an Leistung<br>Öf|c09|||||0|1|0|
|1: ffnen bei Mehrbedarf an Leistung|||||||||
|Regelungsparameter für + Zone|c10|||||0.1 K / 0.1 bar|20 K / 2.0 bar|4.0 / 0.4 bar|

Fortsetzung nächste Seite

22

|Regelungsparameter für + Zone<br>Regelungsparameter für ++ Zone|c11<br>c12|0.1 min<br>0.1 min.|60 min<br>20 min|4.0<br>2.0|
|---|---|---|---|---|
|Regelungsparameter für - Zone|c13|0.1 K / 0.1 bar|20 K / 2.0 bar|4.0 / 0.3 bar|
|Regelungsparameter für - Zone|c14|0.1 min.|60 min|1.0|
|Regelungsparameter für - -  Zone<br>i|c15|0.02 min.|20 min|0.5|
|Definition der Verdichteranschlüsse.<br>Siehe Möglichkeiten Seite 11.|c16|1|26|0|
|Folgende “c17” bis “c28” sind eine andere Art zur Definition<br>der Verdichter als “c16”|||||
|.<br>Es ist ein Code einzustellen, welche Relais auf den ver-<br>schiedenen Stufen eingeschaltet sein sollen:<br>Stufe 1(M&M Betrieb)|c17|0|15|0|
|Stufe 2(M&M Betrieb)|c18|0|15|0|
|Stufe 3(M&M Betrieb)|c19|0|15|0|
|Stufe 4(M&M Betrieb)|c20|0|15|0|
|Stufe 5(M&M Betrieb)|c21|0|15|0|
|Stufe 6(M&M Betrieb)|c22|0|15|0|
|Stufe 7(M&M Betrieb)|c23|0|15|0|
|Stufe 8(M&M Betrieb)|c24|0|15|0|
|Stufe 9(M&M Betrieb)|c25|0|15|0|
|Stufe 10(M&M Betrieb)|c26|0|15|0|
|Stufe 11(M&M Betrieb)|c27|0|15|0|
|Stufe 12(M&M Betrieb)|c28|0|15|0|
|Definition des Verflüsigers:|||||
|i  l<br>**1-8:**Totale Anzahl von Lüfterrelais oder Spannungsstufe<br>|||||
|am Spannungsausgang<br>**9:**Nur bei Analogen Ausgang und bei star von Druckmes-<br>sumformern<br>**10:**Wird nicht benutzt|c29|0/OFF|18|0|
|**11- 18:**Gesamtanzahl Lüfterrelais, die mit wechselweisem<br>Startgeschaltet werden sollen|||||
|Eingeschaltete Verdichterleistung bei manueller<br>Steuerung. Siehe auch “c32”|c31|0%|100%|0|
|Manuelle Steuerung der Verdichterleistung (bei ON wird<br>der Wert in “c31” verwendet)|c32|OFF|ON|OFF|
|Absauggrenzwert (Pump down). Hierbei handelt es<br>sich um den Grenzwert, bei dem der letzte Verdichter<br>abschaltet.|c33|-99.9°C / -1.0 bar|100°C / 60 bar|100°C / 60 bar|
|Proportionalband Xpfür(P = 100/Xp)Verflüssigerregelung|n04|0.2 K / 0.2 bar|40.0 K / 10.0 bar|10.0 K / 3.0 bar|
|I: Integrationszeit für Verflüssigerregelung|n05|30 s|600 s|150|
|Eingeschaltete Verflüssigerleistung bei manueller rege-<br>lung. Siehe auch "n53"|n52|0%|100%|0|
|Manuelle Regelung der Verflüssigerleistung (bei ON wird|53|OFF|ON|OFF|
|der Wert in "n52" angewandt)|n||||
|Startgeschwindigkeit. Die Spannung zur Geschwindig-<br>keitsregelung wird auf 0 V gehalten, bis die Regelung<br>einen höheren Wert als den hier eingestellten anfordert|n54|0%|75%|20%|
|Mindestgeschwindigkeit. Die Spannung zur Geschwindig-<br>|||||
|keitsregelung wechselt auf 0 V, wenn die Regelung einen<br>niedrigeren Wert als den hier eingestellten anfordert|n55|0%|50%|10%|
|**Alarm**|||||
|Verzögerungszeit eines A32 alarms|A03|0 min.|90 min.|0 min.|
|Untere Alarm- und Sicherheitsgrenze für P0|A11|-99°C / -1.0 bar|30°C / 40 bar|-40°C / 0.5 bar|
|Verzögerungszeit für einen DI1-Alarm|A27|0 min.(-1=OFF)|999 min.|OFF|
|Verzögerungszeit für einen DI2-Alarm|A28|0 min.(-1=OFF)|999 min.|OFF|
|Verzögerungszeit für einen DI3-Alarm|A29|0 min.(-1=OFF)|999 min.|OFF|
|Obere Alarm- und Sicherheitsgrenze für Pc|A30|-10 °C / 0.0 bar|200°C /200 bar|60.0°C / 60.0 bar|
|Obere Alarmgrenze für den Fühler "Saux1"|A32|1°C(0=OFF)|140°C|OFF|
|Verzögerungszeit für ein P0 Alarm|A44|0 min.(-1=OFF)|999 min.|0 min.|
|Verzögerungszeit für ein Pc Alarm|A45|0 min.(-1=OFF)|999 min.|0 min.|
|**Sonstiges**<br>|*||||
|Regleradresse<br>AUS/EIN-Wechselschalter(Service-PIN-Mitteilun)|o03<br>o04*|1<br>-|990<br>-||
|g<br>Zugangskode|o05|1(0=OFF)|100|OFF|

* Diese Einstelung is nur möglich, wenn ein Datenkommunikationsmodul im Regler montiert ist.

23

|Angewandter Fühlertype für Sc3, Sc4 und "Saux1"<br>**0=**PT1000,**1=**PTC1000<br>2-7= variationen mit Temperaturfühler an P0 und Pc. Siehe<br>andere stellie im diesem Manual.|o06||||0|7 (1)|0|
|---|---|---|---|---|---|---|---|
|Einstellungs der Spannungsversorgungsfrequen|o12||||50 Hz|60 H|0|
|Manueller Betrieb der Ausgänge:<br>**0:**Keine übersteuerung||||||||
|<br>**1-10:**1 Schliesst das Relais 1, 2 Relais 2, usw.<br>**11-18:**Gibt Spannungssignal an den Analogen ausgang.<br>(11 bringt 1,25 V und so weiter in Stufen von 1,25 V.)|o18||||0|18|0|
|P0-Arbeitsbereich des Druckmessumformers - min. Wert<br>P0-Arbeitsbereich des Druckmessumformers - max. Wert<br>|o20<br>o21||||-1 bar<br>1 bar|0 bar<br>200 bar|-1.0<br>12.0|
|DI4-Eingang festlegen:<br>**0=**wird nicht benutzt.**1=**P0-verschiebung.**2=**Alarmfunk-<br>tion. Alarm="A31"|o22||||0|2|0|
|Betriebszeit von Relais 1 (Wert x 1000)|o23||||0.0 h|99.9 h|0.0|
|Betriebszeit von Relais 2 (Wert x 1000)|o24||||0.0 h|99.9 h|0.0|
|Betriebszeit von Relais 3 (Wert x 1000)|o25||||0.0 h|99.9 h|0.0|
|Betriebszeit von Relais 4 (Wert x 1000)|o26||||0.0 h|99.9 h|0.0|
|Kältemitteleinstellung<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.  6=R13.<br>7=R13b1.  8=R23.  9=R500.  10=R503.  11=R114.<br>12=R142b. 13=Benutzerdef. 14=R32. 15=R227.<br>16=R401A.  17=R507. 18=R402A.  19=R404A. 20=R407C.<br>21=R407A.  22=R407B.  23=R410A.  24=R170.  25=R290.<br>26=R600.  27=R600a.  28=R744.  29=R1270.  30=R417A.<br>31=R422A. 32=R413A. 33=R422D. 34=R427A. 35=R438A.|o30||||0|35|0|
|DI5-Eingang festlegen<br>**0=**wird nicht benutzt.**1=**Pc-verschiebung**2=**Alarmfunktion.<br>Alarm="A32"|o37||||0|2|0|
|Pc-Arbeitsbereich des Druckmessumformers - min. Wert|o47||||-1 bar|0 bar|-1.0|
|Pc-Arbeitsbereich des Druckmessumformers - max. Wert|o48||||1 bar|200 bar|34.0|
|Temp. anzeige beim Fühler "Saux1"|o49||||||°C|
|Betriebszeit von Relais 5 (Wert x 1000)|o50||||0.0 h|99.9 h|0.0|
|Betriebszeit von Relais 6 (Wert x 1000)|o51||||0.0 h|99.9 h|0.0|
|Betriebszeit von Relais 7 (Wert x 1000)|o52||||0.0 h|99.9 h|0.0|
|Betriebszeit von Relais 8 (Wert x 1000)|o53||||0.0 h|99.9 h|0.0|
|Wahl der Anwendung<br>||||||||
|1. Temperaturanzeige und "c16" mode<br>2: Druckanzeige und "c16" mode<br>3. Temperaturanzeige und M&M mode|o61|1|2|3|4<br>1|4|1|
|4. Druckanzeige und M&M mode||||||||
|Funktion für Relaiausgang DO9:<br>0. Start / stop der Geschwindigheitsregelung<br>1.  Inject on signal für Verdampferregelungen<br>2. Boost ready (mindestens ein Verdichter ist on)<br>3. Start /stopder Verflüssigerlüfter|o75||||0|3|0|
|l<br>Funktion für Relais ausgang DO10:||||||||
|0. Alarmrelais<br>1. Start / stopder Verflüssigerlüftr|o76||||0|1|0|
|l<br>Definition der Alarmmitteilung vei DI1 Signal:<br>0. Wird nicht benutzt<br>1. Lüfter fehler (A34)|o78||||0|2|0|
|2. DI1 Alarm(A28)||||||||
|Einstellung bei Wasser Kühler Anwendung<br>Definition des Signaleingang für Verdichter-Regelung,<br>wenn mit Temperatursignal geregelt wird:<br>0. Temperaturfühler an 57-58<br>1. Temperaturfühler an Saux<br>2. Temperaturfühler Sc4<br>Ist eine Frostsicherung erforderlich, muss die Einstellung<br>1 oder 2 betragen und ein Druckmessumformer muss am<br>P0 montiert sein.|o81||||0|2|0|
|Displayanschluss<br>Off: EKA 164<br>On: EKA 165(erweitertes  Displaymit Leuchtdioden)|o82||||Off|On|Off|


|**Service**|||
|---|---|---|
|Status am DI1-Eingang|u10||
|Status am DI2-Eingang|u37||
|Anzeige der Temperatur am Fühler "Sc3"|u44|°C|
|Anzeige der Temperatur am Fühler "Sc4"|u45|°C|
|Status am DI3-Eingang|u87||
|Status am DI4-Eingang|u88||
|Status am DI5-Eingang|u89||

|**Der R**|**egler kann folg **|**ende mitteilungengeben:**|
|---|---|---|
|E1|**Fehler-**|Fehler im Regler|
|E2|**mitteilung**|Die Regelung ist auserhalb des Bereiches oder<br>das Steuersignal ist Defekt *|
|A2|**Alarm-**<br>|NiedrigP0|
|A11|**mitteilung**|Kältemittel nichtgewählt|
|A17||Hoch Pc|
|A19||Verdichter 1 Fehler|
|A20||D ktll Sihhit<br>Verdichter 2 Fehler|
|A21||er auee cere-<br>skreis des Verdichters is<br>Verdichter 3 Fehler|
|A22||unterbrochen.<br>Verdichter 4 Fehler|
|A23||D.h. es fehlt ein Signal<br> <br>Verdichter 5 Fehler|
|A24||an einer der Klemmen<br>29-36<br>Verdichter 6 Fehler|
|A25||.<br>Verdichter 7 Fehler|
|A26||Verdichter 8 Fehler|
|A27||Raumtemperaturalarm (Saux1 temp.)|
|A28||DI 1 Alarm. Klemme 46 ist unterbrochen|
|A29||DI 2 Alarm. Klemme 47 ist unterbrochen|
|A30||DI 3 Alarm. Klemme 49 ist unterbrochen|
|A31||DI 4 Alarm. Klemme 50 ist unterbrochen|
|A32||DI 5 Alarm. Klemme 52 ist unterbrochen|
|A34||Lüfteralarm. Kein Signal am DI1-Eingang|
|A45||Die Regelungistgestoppt|
|S0|**Status-**|Es wirdgeregelt|
|S2|**mitteilungen**|"c01" abwarten|
|S5||"c07" abwarten|
|S8||"c11" oder "c12" abwarten|
|S9||"c14" oder "c15" abwarten|
|S10||Die Kühlung ist gestoppt mit der internen oder<br>die externe Start/Stopp|
|S25||Manuelle Regelund der Ausgänge|
|S34||Sicherheitsausschaltung. Einstellung A30 ist<br>überschritten oder alle Sicherheitseingänge<br>(29-36)sind offen.|
|PS|**Info**|Zugangskode ist erfordert bevor zugang zu den<br>Einstellungengegeben wird|

Mitteilungen können durch Antippen der oberen Taste im Display angezeigt werden. Gibt es mehr als einen Alarm, kann “geblättert” werden.

###### Werkseinstellung

Die Rückkehr zu den ab Fabrik eingestellten Werten lässt sich wie folgt vornehmen:

- Die Spannungszufuhr zum Regler unterbrechen.

- Die mittlere Taste betätigt halten und gleichzeitig die Spannungszufuhr wieder einschalten.

> * Bei Wasser Kühlersteuerung ohne Frostsicherung kann der Alarm von ein nicht montierter P0-Eingang unterdruckt werden durch verbinden des Signals von PC (Klemme 61) an P0 (Klemme 58).

25

**FRANCAIS**

**Raccordements** P0/Pc: AKS 32R: 1 = Noir  = + 2 = Bleu  = - 3 = Marron = s Régulation du compresseur avec la température o06 = 0 o81 = 1 Autres combinaisons: voir manual Toutes les entrées sont à bas voltage. Toutes les sorties de relais peuvent être à haut voltage Transmission de données

###### **Raccordements nécessaires**

**Raccordements nécessaires Raccordements selon les applications Bornes :** 20-21 Marche/arrêt AKD* 1-2 Tension d’alimentation 24 V a.c. Le relais se ferme lorsque le variateur de fréquence doit 4- 19 Sorties de relais pour compresseurs, étages de compres démarrer. sion ou moteurs de ventilateurs 37-38 Signal de tension pour une commande externe de 22-24  Relais d'alarme * condenseur. (Voir reglages page 28) Il y a liaison entre 22 et 24 en cas d’alarme et si le régula39-41 Raccordement possible d’un afficheur externe EKA 163 teur est hors tension. (affichage Pc) 27-28 Signal 24 V pour marche/arrêt de la régulation 42-44 Raccordement possible d’un afficheur externe EKA 163 27-29 Signal 24 V provenant du circuit de protection du DO 1 pour affichage P0 ou EKA 165 pour programmation et 27-30 Signal 24 V provenant du circuit de protection du DO 2 affichage P0 27-31 Signal 24 V provenant du circuit de protection du DO 3 45-46 DI1 - Fonction de contact pour signal d’alarme 27-32 Signal 24 V provenant du circuit de protection du DO 4 45-47 DI2 - Fonction de contact pour signal d’alarme 27-33 Signal 24 V provenant du circuit de protection du DO 5 48-49 DI3 - Fonction de contact pour signal d’alarme 27-34 Signal 24 V provenant du circuit de protection du DO 6 48-50 DI4 - Fonction de contact pour décalage de la référence 27-35 Signal 24 V provenant du circuit de protection du DO 7 de pression d’aspiration ou pour un signal d’alarme. 27-36 Signal 24 V provenant du circuit de protection du DO  8 51-52 DI5 - Fonction de contact pour décalage de la référence 57-59 Pression d’aspiration. Signal de tension de l’AKS 32R ** de pression de condensation ou pour un signal 60-62 Pression de condensation. Signal de tension de l’AKS 32R ** d’alarme. 51-53 Sonde à part Saux1. Signal provenant du capteur AKS 11, AKS 12 ou EKS 111 54-55 Température extérieure (Sc3). Signal provenant du capteur AKS 11, AKS 12 ou EKS 111 (A raccorder si r33 = 2 ou 4). 54-56 Température de l’air à la sortie du condenseur. Signal **Etages de capacité** provenant du capteur AKS 11, AKS 12 ou EKS 111

Si une sortie est affectée à un étage de capacité, il n’est pas nécessaire de connecter le circuit de sécurité annexe. Ex. avec un réducteur de puissance sur DO2, une connexion sur la borne 30 peut être omise.

###### **Transmission de données éventuelle**

25-26   Ne faire ce raccordement qu’après installation du module de transmission de données. S’il s’agit d’une ligne Ethernet, utiliser le connecteur RJ45. (On peut aussi raccorder LON FTT10 de cette façon.) Il es très  important que l'intallation du câble du transmission soit effectuée correctement. Se reporter au document spécifique RC8AC---.

En cas spécial, on peut reconfigurer les relais DO9 et DO10 et les utiliser pour la ventilation.

- Si le régulateur doit commander uniquement des compresseurs ou uniquement des ventilateurs, on peut se passer de la pression Pc et du capteur Pc.

- Pour les installations à la saumure, on peut remplacer le contrôle de pression avec AKS 32R par un contrôle de température aux bornes 57-58 et 60-61. Voir aussi o06.

26

**Configuration de compresseur quand o61 = 1 ou 2** (C’est là qu’on choisira entre les possibilités affichées.) Le réglage « c16 » définit la configuration.

Le réglage « c08 » définit le mode d’enclenchement/déclenchement.

###### **Etages de capacité**

*[Figurtekst: Etages de capacité · Raccords de compresseurs Mode de déclench.  Tous  les étages de capacité sont · /réenclench. présumés être égaux. La seule exception · Relais n° Réglage  Réglage · "c16"  "c08"  étant les réglages c16 = 4 et 21 à 26. · à à · Mode de déclenchement/réenclenche- · ment · Le mode d’enclenchement 1 est le fonc- · tionnement séquentiel. · Le mode 2 est le fonctionnement · cyclique. · Le mode 3 est le fonctionnement cy- · clique et binaire. Ce qui donne la capacité · suivante pour les compresseurs : · 1: 9% · 2: 18% · 3: 36% · 4: 36% · Fonctionnement cyclique pour 3 et 4, et · binaire pour 1, 2 et 3/4 · (pour c16 = 4 seulement)]*

Le mode 3 est le fonctionnement cyclique et binaire. Ce qui donne la capacité suivante pour les compresseurs : 1: 9% 2: 18% 3: 36% 4: 36%

###### **Réenclenchements**

En cas de fonctionnement cyclique avec étages raccordés, certains enclenchements de capacité sont susceptibles de créer des chevauchements puisque les étages de l’un ou de l’autre des compresseurs risquent d’être actifs. Les étages du compresseur ayant assuré le moins d’heures de fonctionnement seront alors enclenchés, les autres déclenchés. Le réenclenchement a lieu en l’espace de 6 secondes.

###### **Fonctionnement égalisé**

Si c16 est réglé entre 21 et 26, il faut que le compresseur 1 + son étage assure la même capacité que chacun des compresseurs suivants. L’étage égalise la capacité enclenchée lorsque les compresseurs suivants sont enclenchés et déclenchés. Le compresseur 1 est toujours en fonctionnement.

###### **Configuration de compresseur quand o61 = 3 ou 4 (C’est là que vous pourrez définir vous-même comment les relais** **p euvent être mis en fonction.** **)**

*[Figurtekst: Résumé des relais du fonctionnement « Mix & Match » (Mix et Match ne sont utilisés que sur un appareil équipé de 4 com- · Valeur  presseurs max.) · Relais n° Combinaison de relais fermés · théorique · 1 1 1 1 1 1 1 1 1 1 · 2 2 2 2 2 2 2 2 2 2 · 3 4 4 4 4 4 4 4 4 4 · 4 8 8 8 8 8 8 8 8 8 · La somme de 1 à 8 est la · valeur de réglage pour  1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 · chaque étage. · Exemple 1 Exemple 2 · Réglages:  Pour que l’étage de capacité 1 enclenche le seul relais n° 3, réglez « c17 » à 4. · c17 à 1 Pour que l’étage de capacité 2 enclenche le seul relais n° 4, réglez « c18 » à 8. · c18 à 2 Pour que l’étage de capacité 3 enclenche les relais n°s 3 et 4, réglez « c19 » à 12. · c19 à 3 Continuez avec le réglage de « c20 », etc. jusqu’à ce que tous les étages de capacité · c20 à 4 soient définis. · c21 à 5 · c22 à 6 · c23 à 7 · Etagesde capacite]*

27

###### **Enclenchements de condenseurs**

Une fois les relais de compresseurs définis, on passe à la définition des relais ventilateurs.

Le premier relais disponible (DO1-DO8) sera le premier relais de ventilateur. Ensuite viennent les suivants. Si les relais DO du régulateur ne suffisent pas, on peut raccorder un module de relais à la sortie analogique. Voici l’explication de cette fonction :

En cas d’un maximum de 4 ventilateurs externes pour un seul EKC 331 :

En cas de plus de 4 ventilateurs externes pour deux EKC 331 :

1. 2.

Signal de sortie émis par l’AK-PC 530 Dans l’EKC 331, régler plage de tension à 0-5 V (“o10”=6). Dans l’EKC 331, régler le nombre d’étages **à 4 (« o19 » =4)** (même si le nombre de ventilateurs raccordés est inférieur).

###### Raccordement

Signal de sortie émis par l’AK-PC 530

Dans le premier EKC 331, régler la plage de tension à 0-5 V (« o10 » = 6). Dans le second EKC 331, régler la plage de tension à 5-10 V (« o10 »=7). Dans les **deux** EKC 331, régler le nombre d’étages **à 4 (« o19 » = 4)** (même si le nombre de ventilateurs raccordés sur le second EKC est inférieur)

Raccordement

Démarrage alternatif des ventilateurs (uniquement si c29 est en 11 à 18) Les ventilateurs peuvent être programmés à démarrer chacun leur tour une fois qu’ils ont tous été stoppés. La première fois que la régulation sera entamée, le ventilateur 1 s’enclenchera le premier —la régulation décidera s’il faut en démarrer d’autres.

La prochaine fois qu’ils ont tous été arrêtés, le ventilateur 2 démarrera le premier et ainsi de suite…

Le ventilateur 1 sera de nouveau le premier à démarrer quand la rotation aura vu tous les ventilateurs être engagés. S’il y a plus d’un ventilateur sur un EKC 331, les autres restant ne pourront démarrer les premiers. Dans ce cas de figure, ce sera toujours celui qui a le seuil de tension le plus bas qui sera le premier.

Si toute la capacité de condensation doit être régulée par un variateur de vitesse, l’AK-PC 530 doit émettre un signal analogique concernant la capacité désirée (« c29 » = 9). Ce signal varie entre 0 et 10 V. Le rapport entre signal et capacité est le suivant :

28

##### **Utilisation**

###### **Transmission de données**

Si le régulateur a été équipé de transmission de données, sa gestion peut être assurée par une unité du système.

L’importance des alarmes émises peut être graduée de la façon suivante : 1 (haute), 2 (moyenne), 3 (basse) ou 0 (aucune alarme).

###### **Commande via un affichage externe**

Les valeurs sont affichées avec trois chiffres, et avec une mise au point vous pouvez définir si la pression doit s’afficher en SI unités (C°/bar) ou US unités (°F/psig). Il y a trois possibilités d’affichage :

Pour la commande du régulateur et l’affichage de la pression d’évaporation.

En tapant brièvement sur le bouton inférieur on peut faire apparaître brièvement la pression de condensation à l’affichage. (S’il suffit de réguler la pression de condensation l’écran affichera toujours Pc.)

En fonctionnement normal, les diodes indiquent où se trouve actuellement la régulation. Diode sup. + second : Zone++ second : Zone+ « Néant » : Zone neutre avant dernière : ZoneDiode inf. + l’avant dernière : Zone- -

Les autres LED du tableau montrent les entrées et les sorties qui sont en fonctions :

- Relais compresseurs

- Relais ventilateurs

- Signaux d’entrées

- La diode d’optimisation s’allumera quand la référence est de 2 K ou plus au-dessus du point de réglage

EKA 163 Si l’on a besoin d’un affichage permanent de la pression de condensation, on peut connecter un écran sans boutons de commande. **EKA 164** Pour la commande du régulateur et l’affichage de la pression d’évaporation. EKA 164 En tapant brièvement sur le bouton inférieur on peut faire apparaître brièvement la pression de condensation à l’affichage. Les leds de l’affichage montreront de même qu’avec EKA 165 où se trouve la régulation.

###### Les boutons à l’affichage

Quand vous désirez modifier un réglage, les boutons supérieurs et inférieurs indiqueront une valeur supérieure ou inférieure. Mais il faut d’abord avoir accès au menu: appuyer quelques secondes sur le bouton supérieur. Apparaissent alors la série de codes de paramétrage. Chercher le code à modifier et appuyer sur le bouton central.  Après la modification, mémoriser la nouvelle valeur en appuyant à nouveau sur celui-ci.

###### Ou bref:

1. Appuyer sur le bouton supérieur jusqu’à apparition d’un paramètre.

2. Appuyer sur l’un des boutons pour trouver le paramètre à régler.

3. Appuyez sur le bouton central et la valeur de réglage s’affichera

4. Appuyer sur l’un des boutons pour choisir la nouvelle valeur.

5. Appuyer à nouveau sur le bouton central pour valider le réglage.

(Une courte pression affichera les codes d’alarmes qui sont armées.)

29

##### **Sommaire des menus**

###### **Séquencement**

**1.** o61 **doit** être programmé comme premier paramètre. Il détermine laquelle des 4 zones d’utilisation est activée. La mise au point **doit** être effectuée par les boutons de l’écran d’affichage. Cette configuration ne peut pas s’effectuer par voie informatique de transmission de données (fonctions actives affichées ci-dessous par zones colorées).

###### **2. Démarrage rapide**

Si vous désirez obtenir un démarrage éclair du dispositif pour que la réfrigération puisse commencer, vous pouvez commencer par programmer les paramètres suivants (programmables si la régulation est arrêtée, r12=0) :

r23, r28 et soit (c08, c09 et c16) soit (c17 à 28) – puis continuer par c29, o06, o30, o75, o76, o81 et enfin r12=1.

**3.** Après la mise en route de la régulation, procéder à l’ajustage correct des autres paramètres.

SW: 1.3x

|**Fonction**|**Para-**<br>**métre**|**1**|**o61**<br>**2**|**=**<br>**3**|**4**|**Min.**|**Max.**|**Réglage départ**<br>**usine**|
|---|---|---|---|---|---|---|---|---|
|**Image normale**|||||||||
|P0 sera indiqué sur l’EKA 165 (appareil à boutons)|-|°C|P<br>|°C|P|°C / bar|||
|Pc sera indiqué sur l’EKA 163|-|°C|P<br>|°C|P|°C / bar|||
|**P0 référence**|||||||||
|Zone neutre<br>|r01|||||0.1°C / 0.1 bar<br>|20°C /5.0 bar<br>|4.0°C / 0.4 bar|
|Correction du signal du capteur P0<br>|r04<br>|||||-50°C /-5.0 bar<br>|50°C / 5.0 bar<br>|0.0<br>|
|Choix SI ou US 0=bar et°C.  1=Psig et°F)|r05|||||0|1|0|
|Marche/arrêt de la réfrigération|r12|||||OFF|ON|OFF|
|Offset de référencepour P0 (voir aussi r27)|r13|||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Réglage dupoint de consigne P0|r23|||||-99°C / -1 bar|30°C / 60.0 bar|0.0°C / 3.5 bar|
|Limitation : Valeur maxi, référence P0<br>( r23 + divers décalages)|r24||||||°C / bar||
|Limitation : Valeur maxi, référence P0<br>(vaut également pour la régulation par décalage de<br>référence)|r25|||||-99°C / -1.0 bar|30°C / 60.0 bar|30.0°C / 40.0 bar|
|Limitation : Valeur mini, référence P0<br>(vaut également pour la régulation par décalage de|r26|||||-99°C / -1.0 bar|30°C / 40.0 bar|-99.9°C / -1.0 bar|
|référence)|||||||||
|Décalage de P0 (ON = actif « r13 »)|r27|||||OFF|ON|OFF|
|**Pc référence**|||||||||
|Réglage dupoint de consigne Pc|r28|||||-25°C / 0.0 bar|75°C / 110.0 bar|35°C / 15.0 bar|
|Affichage de la référence Pc totale|r29||||||°C / bar||
|Limitation : Valeur maxi, référence Pc|r30|||||-99.9°C / -0.0 bar|99.9°C / 130.0bar|55.0°C / 60.0 bar|
|Limitation : Valeur mini, référence Pc|r31|||||-99.9°C / 0.0 bar|99.9°C / 60.0 bar|-99.9°C / 0.0 bar|
|Correction du signal du capteur Pc|r32|||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|Variation de la référence Pc<br>1 et 2 : régulation PI<br>1: Référence fixe.  « r28 » est utilisé.<br>2: Référence variable. La température extérieure (Sc3) est<br>incluse dans la référence.|r33|||||1|4|1|
|3: Comme 1, mais avec régulation P (bande Xp)|||||||||
|4: Comme 2,mais avec régulation P(bande Xp)|||||||||
|Offset de référencepour Pc<br>f|r34|||||-50°C / -5.0 bar|50°C / 5.0 bar|0.0|
|La différence de température moyenne au condenseur en<br>charge maximum (dim. tm K).|r35|||||3.0|50.0|10.0|
|Différence de température moyenne au condenseur en<br>capacité de compresseur actuelle la plus basse (min. tm K).|<sup>r56</sup>|||||3.0|50.0|8.0|
|Là, vous pouvez relever la pression réelle (P0) mesurée par<br>le transmetteur depression.|<br>r57||||||°C / bar||
|Là, vous pouvez relever la pression réelle (T0) qui partic-<br>i|<sup>r58</sup>||||||°C||
|ipe de la régulation. De la sondequi est définie dans "o81"|||||||||
|i<br>**Capacité**|||||||||
|Temps de marche min.pour relais|c01|||||0 min|30 min.|0|
|Période min. entre deux enclenchements du même relais|c07|||||0  min.|60 min|4|
|Définition du mode de régulation|||||||||
|i<br>1 : séquentiel (step mode / FILO)<br>2 : cyclique (step mode / FIFO)<br>3: Binaire et cyclique|c08|||||1|3|1|
|En mode de régulation utilisant les étages de compression,<br>il faut définir le relais comme suit :<br>0:  : fermeture à la demande de plus de capacité|<br>c09|||||0|1|0|
|<br>1 : ouverture à la demande deplus de capacité|||||||||

à suivre

30

|Paramètre de régulationpour +Zone<br>Paramètre de régulationpour +Zone|c10<br>c11|0.1 K / 0.1 bar<br>0.1 min|20 K / 2.0 bar<br>60 min|4.0 / 0.4 bar<br>4.0|
|---|---|---|---|---|
|Paramètre de régulationpour ++Zone|c12|0.1 min.|20 min|2.0|
|Paramètre de régulationpour –Zone|c13|0.1 K / 0.1 bar|20 K / 2.0 bar|4.0 / 0.3 bar|
|Paramètre de régulationpour –Zone|c14|0.1 min.|60 min|1.0|
|Paramètre de régulationpour –  Zone|c15|0.02 min.|20 min|0.5|
|Définition des raccordements de compresseurs.. Reportez-<br>vous àpage 11pour connaître lespossibilités.<br>i|c16|1|26|0|
|« c17 » suivant au « c28 » est un autre moyen de définir les|||||
|compresseurs après « c16 »<br>Il faut alors régler un code concernant les relais qui doivent<br>être ON aux différentes phases :|c17|0|15|0|
|Etage 1 (mode M&M)|||||
|<br>Etage 2(mode M&M)|c18|0|15|0|
|Etage 3(mode M&M)|c19|0|15|0|
|Etage 4(mode M&M)|c20|0|15|0|
|Etage 5(mode M&M)|c21|0|15|0|
|Etage 6(mode M&M)|c22|0|15|0|
|Etage 7(mode M&M)|c23|0|15|0|
|Etage 8(mode M&M)|c24|0|15|0|
|Etage 9(mode M&M)|c25|0|15|0|
|Etage 10(mode M&M)|c26|0|15|0|
|Etage 11(mode M&M)|c27|0|15|0|
|Etage 12(mode M&M)<br>i|c28|0|15|0|
|Définition du condenseur :<br>**1-8**: Nombre total de relais de ventilateurs ou le seuil de<br>tension à la sortie de tension<br>|||||
|**9**: Uniquement par une sortie analogique et un variateur<br>de vitesse|c29|0/OFF|18|0|
|**10:**Ne s’utilise pas<br>|||||
|**11- 18:**Nombre total de ventilateurs qui doivent être con-|||||
|nectés en démarrages alternatifs<br>|||||
|Capacité de compresseur enclenchée en mode manuel.<br>Voir aussi « c32 »|c31|0%|100%|0|
|Commande manuelle de capacité de compresseur (avec<br>ON la valeur de « c31 » est utilisée)|c32|OFF|ON|OFF|
|Le seuil pump down. La valeur limite quand le dernier<br>compresseur a été débrayé|c33|-99.9°C / -1.0 bar|100°C / 60 bar|100°C / 60 bar|
|Bande proportionnelle Xp pour la régulation de condensa-<br>tion (P=100/Xp)|n04|0.2 K / 0.2 bar|40.0 K / 10.0 bar|10.0 K / 3.0 bar|
|<br>I: Temps d’intégration Tn pour la régulation de condensa-<br>tion|n05|30 s|600 s|150|
|Capacité de condenseur enclenchée en mode manuel. Voir|<br>||||
|<br>aussi « n 53 »<br>|<br>n52<br>|0%|100%|0|
|Commande manuelle de capacité de condenseur (avec ON<br>la valeur de « c52 » est utilisée)|<br>n53|OFF|ON|OFF|
|Vitesse de démarrage. La tension de la régulation de<br>vitesse est maintenue à 0 V, jusqu’à ce que la régulation<br>exige une valeur supérieure à celle qui était définie|n54|0%|75%|20%|
|i<br>Vitesse min. La tension de la régulation de vitesse passe à<br>d l l   l f  ll|||||
|0 V, quan a réguation exige une vaeur inérieure à cee<br>qui était définie|n55|0%|50%|10%|
|i<br>**Alarme**|||||
|Temporisation de l’alarme A32|A03|0 min.|90 min.|0 min.|
|Limite inférieure d’alarme et deprotectionpour P0|A11|-99°C / -1.0 bar|30°C / 40 bar|-40°C / 0.5 bar|
|Temps de retard d’une alarme DI1|A27|0 min(-1=OFF)|999 min|OFF|
|<br>Temps de retard d’une alarme DI2|A28|.<br>0 min.(-1=OFF)|.<br>999 min.|OFF|
|Temps de retard d’une alarme DI3|A29|0 min.(-1=OFF)|999 min.|OFF|
|Limite supérieure d’alarme et deprotectionpour Pc|A30|-10 °C / 0.0 bar|200°C / 200.0 bar|60.0°C / 60.0 bar|
|Limite supérieure d’alarmepour la sonde « Saux1 »|A32|1°C(0=OFF)|140°C|OFF|
|Temps de retard d’une alarme P0|A44|0 min.(-1=OFF)|999 min.|0 min.|
|Temps de retard d’une alarme Pc|A45|0 min.(-1=OFF)|999 min.|0 min.|
|**Divers**|||||
|Adresse du régulateur|o03*|1|990||
|Commutateur ON/OFF(message broche service)|o04*|-|-||
|Code d’accés|o05|1(0=OFF)|100|OFF|

* Ce réglage n'est possible qui si un module de transmission de données est installé dans le régulateur.

31

|Type de sonde installé pour Sc3, Sc4 et “Saux1”<br>**0**=PT1000**1**=PTC1000|||||||
|---|---|---|---|---|---|---|
|,<br>27  ii  l d d é  P0  P|o06|||0|7 (1)|0|
|- = varatons avec a sone e temprature sur  et c.<br>Voir ci-dessus dans ce manuel.|||||||
|Choisir la fréquence d’alimentations<br>|o12|||50 Hz|60 H|0|
|Commande manuelle des sorties :<br>|||||||
|0: Aucune régulation<br>**1-10**: 1 enclenche le relais n* 1, 2 le relais n* 2 et ainsi de<br>suite.<br>**11-18**: Donne un signal de tension sur la sortie<br>analogique. (11 donne 1,25 V et ainsi de suite par crans de|o18|||0|18|0|
|<br>125 V)|||||||
|, .<br>P0-Plage du transmetteur depression,valeur min.|o20|||-1 bar|0 bar|-1.0|
|P0-Plage du transmetteur depression,valeur max.<br>’|o21|||1 bar|200 bar|12.0|
|Utilisation de lentrée DI4<br>**0**= inutilisée**1**= décalage P0**2**= fonction d’alarme<br>Alarme=« A31 »|o22|||0|2|0|
|<br>Temps de marche relais 1(valeur multipliéepar 1000)|o23|||0.0 h|99.9 h|0.0|
|Temps de marche relais 2(valeur multipliéepar 1000)|o24|||0.0 h|99.9 h|0.0|
|<br>Temps de marche relais 3(valeur multipliéepar 1000)|o25|||<br>0.0 h|<br>99.9 h|0.0|
|Temps de marche relais 4(valeur multipliéepar 1000)<br>i|o26|||0.0 h|99.9 h|0.0|
|Définition du réfrigérant<br>1=R12.  2=R22.  3=R134a.  4=R502.  5=R717.  6=R13.<br>7=R13b1.  8=R23.  9=R500.  10=R503.  11=R114.<br>12=R142b. 13=utilisateur. 14=R32. 15=R227.  16=R401A.<br>17=R507. 18=R402A.  19=R404A. 20=R407C.  21=R407A.<br>22=R407B.  23=R410A.  24=R170.  25=R290.  26=R600.<br>27=R600a.  28=R744.  29=R1270.  30=R417A. 31=R422A.<br>|o30|||0|35|0|
|32=R413A. 33=R422D. 34=R427A. 35=R438A.<br>Utilisation  de l’entrée DI5|||||||
|**0**= inutilisée**1**= décalage Pc**2**= fonction d’alarme Alarme|<br>o37|||0|2|0|
|<br>=A32|<br>||||||
|«  »<br>Pc-Plage du transmetteur depression,valeur min.|o47|||-1 bar|0 bar|-1.0|
|Pc-Plage du transmetteur depression,valeur max.|o48|||1 bar|200 bar|34.0|
|Relever la température du capteur "Saux1"|o49|||||°C|
|Temps de marche relais 5(valeur multipliéepar 1000)|o50|||0.0 h|99.9 h|0.0|
|Temps de marche relais 6(valeur multipliéepar 1000)<br>Temps de marche relais 7(valeur multipliéepar 1000)|o51<br>o52|||0.0 h<br>0.0 h|99.9 h<br>99.9 h|0.0<br>0.0|
|Temps de marche relais 8(valeur multipliéepar 1000)<br>|o53|||0.0 h|99.9 h|0.0|
|Choix d’application|||||||
|1. L'affichage de température et mode « c16 »|||||||
|fi<br>2: L'affichage de pression et mode « c16 »<br>3. L'affichage de température et mode « M&M »|o61|1<br>2|3<br>4|1|4|1|
|4. L'affichage de pression et mode « M&M »<br>Fi d i li DO9|||||||
|oncton e sorte reas  :<br>0. Début/Arrêt de commande de vitesse<br>1. Fonction arrêt détendeurs commandes d’évaporateur<br>2. Fonction booster autorisée (au moins un compresseur<br>|o75|||0|3|0|
|est en marche)<br>3. Début/Arrêt de ventilateur de condenseur|||||||
|Fonction de sortie relais DO10 :|||||||
|0. Relais d’alarme<br>l|o76|||0|1|0|
|1. Début/Arrêt de ventiateur de condenseur<br>Définition du message d’alarme en signal DI1 :|||||||
|0. Ne s’utilise pas<br>1. Défaut ventilateur (A34)<br>2 DI1 l (A28)|o78|||0|2|0|
|.  aarme<br>**Réglages pour une application de refroidisseur**<br>**de liquide.**<br>Définition de l’entrée de signal lorsque la régulation de<br>compresseur est commandée par un signal émis par une<br>sonde de température :<br>0. Signal de température à la borne 57-58 (l’entrée P0)<br>1. Signal de température à l’entrée Saux<br>2. Signal de température à l’entrée Sc4<br>Si une protection antigel est nécessaire, le paramètre doit|o81|||0|2|0|
|être sur 1 ou 2 et le transmetteur de pression doit être<br>monté sur P0|||||||
|.<br>Connexion d’affichage<br>f||||f||f|
|Off : EKA 164<br>fi|o82|||Off|On|Off|
|On : EKA 165 (affichage amélioré avec Leds)|||||||
|fi <br>**Service**<br>’|||||||
|État dentrée DI1<br>État d’entrée DI2|u10<br>u37||||||

32

|Relever la température du capteur "Sc3"|u44<br>°C|
|---|---|
|Relever la température du capteur "Sc4"|u45<br>°C|
|État d’entrée DI3|u87|
|État d’entrée DI4|u88|
|État d’entrée DI5|u89|

|**Le ré**|**gulateurpeut**|**émettre les messages sui**|**vants :**|
|---|---|---|---|
|E1|**Message**<br>|Erreur dans le régulateu|r|
|E2|**d’erreure**|La régulation dépasse la<br>signal de commande est|plage admise ou le<br>défectueux. *|
|A2|**Message**<br>**’**|P0 bas||
|A11|**dalarme**|Omission du choix de ré|frigérant|
|A17||Pc haut||
|A19||Compresseur 1 erreur||
|A20||Compresseur 2 erreur|d  d|
|A21||Compresseur 3 erreur|Le circuit e sécurité u<br>compresseur actuel est|
|A22||Compresseur 4 erreur|<br>interrompu.<br>i|
|A23||Compresseur 5 erreur|Cela signifie qu’il n’y a<br>’|
|A24||Compresseur 6 erreur|pas de signal sur lune<br>des bornes 29-36|
|A25||Compresseur 7 erreur|.|
|A26||Compresseur 8 erreur||
|A27||Alarme température inté|rieure (Saux1 temp.)|
|A28||Alarme DI1. La borne 46|est ouverte|
|A29||Alarme DI2. La borne 47|est ouverte|
|A30||Alarme DI3. La borne 49|est ouverte|
|A31||Alarme DI4. La borne 50|est ouverte|
|A32||Alarme DI5. La borne 52|est ouverte|
|A34||Alarme ventilateur. Il n’y<br>DI1.|a pas de signal à l’entrée|
|A45||La régulation a été arrêt|ée|
|S0|**Message**|Régulation||
|S2|**d'etat**|Attente « c01 »||
|S5||Attente "c07"||
|S8||Attente "c11" ou "c12"||
|S9||Attente "c14" ou "c15"||
|S10||La réfrigération est arrêt<br>interne ou externe|ée par l’arrêt/marche|
|S25||Commande manuelle d’|entrée|
|S34||Arrêt sécurité. La valeur<br>dépassée, ou bien toute<br>(29-36)sont ouvertes|du réglage A30 est<br>s les entrées de sécurité|
|PS|**Infos**|Il faut un code d’accèsp|our toucher les réglages.|

Les messages peuvent être sollicités à l’affichage par une courte pression sur le bouton supérieur. S’il y a plus d’une alarme, elles peuvent être « déroulées »

- Réglage départ usine Pour retrouver éventuellement les valeurs réglées en usine, procéder ainsi :

- Couper la tension d’alimentation du régulateur. - **Maintenir le bouton central enfoncés en remettant le régula-** teur sous tension.

33

The Product contains electrical components A nd may not be disposed together with domestic waste. Equipment must be separate collected with Electrical and Electronic waste. According to Local and currently valid legislation.

34
