# Danfoss EKE 1 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.

## Indhold

1. User Guide – Superheat controller Type EKE 1A, 1B, 1C, 1D (PV04)
2. Data Sheet – Superheat controller and stepper valve driver Type EKE 1A,B,C (PV05), 1D (PV02)


---

## 1. User Guide – Superheat controller Type EKE 1A, 1B, 1C, 1D (PV04)

*Kilde: Danfoss-dokument BC398828796060en-000102.pdf*

**User Guide**

### Superheat controller Type **EKE 1A, 1B, 1C, 1D** (PV04)

For commercial air conditioning and pvo4 refrigeration applications

#### **Contents**

|**1**<br>**Intr**|**oduction**|**4**|
|---|---|---|
|**2**<br>**Port**|**folio overview**|**5**|
|**3**<br>**Inst**|**allation**|**7**|
|3.1|Environmental conditions|7|
|3.2|Mounting|7|
|3.3|General Connection’s overview|7|
|3.4|Cabling lengths for different connections|13|
|3.5|Connecting Relay Outputs|14|
|3.6|Temperature Sensor Mounting|15|
|3.7|Power and signal sharing|16|
||3.7.1<br>Sharing Power Sources|16|
||3.7.2<br>Sharing input signal|17|
||3.7.3<br>Sharing pressure sensor signal|17|
|**4**<br>**App**|**lications**|**20**|
|4.1|Controller Mode|20|
||4.1.1<br>Superheat control mode|20|
||4.1.2<br>Temperature control mode|20|
|4.2|Driver Mode|21|
|4.3|Typical EKE applications|22|
|**5**<br>**User**|**Interface**|**26**|
|5.1|Configuration using MMI Display|26|
||5.1.1<br>MMIGRS2 Setup and service|27|
||5.1.2<br>MMIGRS2 Main screen|28|
||5.1.3<br>ERR31 Error Alarm on the external display - MMIGRS2|30|
||5.1.4<br>Service mode through MMIGRS2|30|
|5.2|Configuration using KoolProg Software:|31|
|5.3|Quick Configuration|38|
|**6**<br>**Coni**|**figuration**|**40**|
|6.1|Driver Mode|40|
||6.1.1<br>Driver Mode using analog signal|40|
||6.1.2<br>Driver Mode using Communication Bus|41|
|6.2|Superheat Control Mode|41|
||6.2.1<br>Superheat Reference Calculation Parameters|42|

|6.2.2<br>Temperature Control Parameters|45|
|---|---|
|6.2.3<br>Offsetting Superheat, Temperature and OD Via External signal|48|
|6.2.4<br>Compressor feed Forward function|49|
|6.3<br>Other features and modes|50|
|6.3.1<br>Startup and Defrost Modes|50|
|6.3.2<br>Protection features|53|
|6.3.3<br>Manual Mode|58|
|6.3.4<br>Valve configuration|59|
|6.3.5<br>Adding user Defined Refrigerant|60|
|**7**<br>**Parameter List**|**62**|
|**8**<br>**Alarms and troubleshooting**|**73**|
|8.1<br>Alarms|73|
|8.1.1<br>Configuration errors|73|
|8.1.2<br>Sensor alarms/errors|74|
|8.1.3<br>Stepper alarms/errors|75|
|8.1.4<br>Bus alarms/errors|75|
|8.1.5<br>Application alarms|76|
|8.1.6<br>Thermostat alarms|76|
|8.1.7<br>Stop state alarm|77|
|8.1.8<br>Manual mode alarm|77|
|8.2<br>Troubleshooting|77|
|**9**<br>**Appendix**|**82**|
|**10**<br>**Ordering**|**83**|
|**11**<br>**Certificates, declarations, and approvals**|**84**|
|**12**<br>**Online support**|**85**|

#### **1 Introduction**

The flexible pre-programmed EKE superheat controller from Danfoss provides ultimate software control, allowing you to tailor the performance of your system to your exact requirements. EKE is ideal for controlling a wide range of commercial air conditioning and refrigeration applications, such control helps you to achieve the highest efficiency in the system reducing the operational cost by up to 20% with minimal effort. EKE is generally used where there is a requirement for accurate control of superheat or temperature control in connection with air conditioning and refrigeration. The superheat is regulated to the lowest possible value within a short period of time. It regulates the superheat of the evaporator by charging optimally even when there are great variations of load resulting in reduction of energy consumption and operational cost

##### **Typical Applications**

- Chillers

- Processing plant / Cabinet cooling

- Cold store (air coolers)

- A/C plant / Air conditioning

- Heat pumps. Residential Heat Pump

- Transport cooling

- Stepper Motor Driver

#### **2 Portfolio overview**

**Table 1: Portfolio overview**

|**Features**||**EKE 1**|**A**<br>**EKE 1B**|**EKE 1C**|**EKE 1D**|
|---|---|---|---|---|---|
|**Power supply**||||||
|Power Supply Type|24 V AC / DC ± 20%|•|•|•|•|
|Battery Backup input|18-24 V DC|•|•|•|•|
|Class of insulation||||Class II||
|**Data communication**||||||
|MODBus|RS 485 RTU||•|•||
|Wired CANbus||||• (4 wires)|• (3 wires)|
|CANbus RJ 12|Danfoss MMI service port|•|•|•|•|
|**Inputs**||||||
|Number of temperature<br>sensors||1|2|3|2|
|Temperature sensor types|PT1000|||•||
||NTC 10K, type EKS|•|•|•|•|
||NTC 10K, type ACCPBT|•|•|•|•|
||NTC 10K, type Sensata|•|•|•|•|
|Number of Pressure sen-<br>sor||1|1|2<sup>**(1)**</sup>|1|
|Pressure Transmitter|Ratiometric 0.5 - 4.5 V|•|•|•|•|
|types|Voltage signal 0 – 10 V|•|•|•|•|
||Current signal 0 – 20 mA|||•||
|Share Pressure Signal|Hardware (Up to 5 devi-<br>ces)|•|•||•|
||Via wired CANbus (not<br>possible to share ratio-<br>metric sensor)|||•|•|
||Via MODbus||•|•||
|Number of external refer-<br>ences||1|1|1|1|
|External reference|0-20mA|||•||
||User defined current|||•||
||0-10V|•|•|•|•|
||0- 5V|•|•|•|•|
||User defined voltage( max<br>10V)|•|•|•|•|
|Digital input Dry contact||3||2||
|**Outputs**||||||
|Digital output||||1||
|Relay|Normally Open||3A Gener|al purpose, 250V ac, 100k||
||Normally closed||2A Gener|al purpose, 250V ac, 100k||
|Relay Function|||Alarm relay or LLSV (Liquid Lin|e Solenoid Valve)||
|User interfaces|Koolprog Software tool|•|•|•|•|
||MMIGRS2 screen<br>Master controller|•|•<br>•|•<br>•|•<br>•|

> **(1) The 2nd pressure sensor is connect to AI4**

**Table 2: Accessories and Related** **p roducts**

*[Figurtekst: MMIGRS2 Display ACCCBI Cable MMIMYK Gateway · MMIMYK device is used as a gateway to connect EKEs · User interface module MMIGRS2 Display. ACCCBI cables for MMI display and gateway. and the KoolProg PC software for parameter setting · or data logging. · Table 3: Accessories and Related  p roducts · Pressure Transducer Temperature Sensor Power Supply · PT 1000 AKS is a High precision temp. sensor AKS 11 AK-PS Input: 100 - 240 V AC / 45 - 65 Hz Output: 24 V · AKS Pressure Transmitter,available with ratiometric · and 4 - 20 mA. NSK Ratiometric Pressure Probe. XSK (preferred), AKS 12, AKS 21 ACCPBT PT1000 NTC sen- DC: available with 18 VA, 36 VA and 60 VA ACCTRD IIn- · sors EKS 221 (NTC-10 Kohm) ACCPBT NTC Temp probe put: 230 V AC, 50 – 60 Hz Output: 24 V AC, available · Pressure probe 4 - 20 mA. · (IP 67 / 68) with 12 VA, 22 VA and 35 VA]*

**Table 4: Accessories and Related** **p roducts**

*[Figurtekst: Stepper motor valves M12 Angle Cables · EKE is compatible with Danfoss stepper motor valves i.e Danfoss ETS 5M, ETS 6, Various lengths of standard M12 cable are available for connecting stepper motor · ETS, KVS, ETS Colibri®, KVS colibri®, CTR, CCMT. valves.]*

#### **3 Installation**

#### **3.1 Environmental conditions**

**Table 5: Environmental conditions**

|Operating conditions|-20 – 60 °C, 90% RH non-condensing|
|---|---|
|Storage / Transport conditions|-30 – 80 °C, 90% RH non-condensing|
|Vibration and shock|According to IEC 60068-2-27 Ea|
|Integration|In Class I and / or II appliances|
|Index of protection|IP40 only on the front cover (General IP20)|
|PCB protection|None (no conformal coating)|
|Period of electric stress across insulating parts|Long|
|Resistance to heat and fire|Category D|
|Immunity against voltage surges|Category II|
|Approvals|CE compliance:<br>This product is designed to comply with the following EU standards:<br>• Low voltage guideline: 2014/35/EU<br>• Electromagnetic compatibility EMC: 2014/30/EU and with the following norms:<br>- EN61000-6-1. EN61000-6-3<br>(immunity and emission standard for residential. commercial and light industrial environments)<br>- EN61000-6-2. EN61000-6-4<br>(immunity and emission standard for industrial environments)<br>- EN60730-1 and EN60730-2-9<br>(Automatic electrical controls for household and similar use)<br>• RoHS compliance to 2011/65/EU and no components from negative list acc. to 500B0751|

#### **3.2 Mounting**

DIN rail mounting / demounting. The unit can be mounted onto a 35 mm DIN rail simply by snapping it into place and securing it with a stopper to prevent sliding. It is demounted by gently pulling the stirrup located in the base of the housing

*[Figurtekst: Fi g ure 1: Mountin g Fi g ure 2: De-mountin g · 1 · 2 · “Click” 3]*

#### **3.3 General Connection ’** **s overview**

This is an overview of all the different possible installation of the EKE 1x series, the connection details will be explained separately in the configuration section

###### **Fi** **g ure 3: EKE 1A connection overview**

*[Figurtekst: Master controller Optional · MMIGRS2 Display · CAN RJ · 080G0294 (optional) · C · *Note; IF Dl1(ON/Off) · Pressure Transmitter switch is not used it · Ratiometric 0.5 – 4.5 V AKS cable must be turned off in · connection Dl1 parameter · 1 060G1034 configuration MMIMYK · 3 Gateway · 2 · e.g.  AKS 32R CAN RJ · CAN RJ CAN RJ KoolProg PC tool · Superheat controller · EKE 1A - 080G5300 · C1 NC1 · Power · Power supply · 24 V AC± 20% – 24 V DC± 20% + C1 NO1 · + 18 V Relay Power · T2.5 A fuse backupBatt Normally open ornormally closed · (optional) (optional) (optional) · ETS 5M · solenoidON/OFF Alarm · valve · ETS 6 valve · ETS / KVS · Colibri ® · CCMT / CTR valve · DI2 COM NTC (S2) DI3 CANbus · DI1 (ON/OFF)* AI4 (voltage) 080G0075 (opt.) · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · Danfoss 80G311.10 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ +/~+/~ GND Bat+ A1 A2 B1 B2 NO1NO1 C1C1 NC1NC1 · brown black orange yellow · orange yellow red black · white black red green]*

**Table 6: EKE 1A** **p inout**

*[Figurtekst: COM Common · DI3 Digital input 3 Software configurable DI · AI2 Analog input NTC 10K S2 · AI3 Analog inputs 0 – 5 V / Ratiometric pressure transmitter Pe · AI4 analog inputs 0 – 10 V External Reference signal · COM Common · DI1 Digital input 1 Main switch (hardware) · DI2/3 Digital input 2 and 3 Software configurable DI · 5V+ Power output for Ratiometric pressure transmitter 0 – 5V · COM Common]*

- **NOTE:**

- If Dl1(On/Off) switch is not used it must be short circuited

- EKE 2U Backup power module is recommended to use to ensure closure of the electronic valves. in case of power failures

###### **Fi** **g ure 4: EKE 1B connection overview**

*[Figurtekst: Master controller · MMIGRS2 Display · CANBus · CAN RJ · 080G0294 (optional) · Supervisor EKE · network MMIMYK · AKS Cable  Gateway · connection · 060G1034 · 1 · 3 · 2 · Pressure transmitter CAN RJ · e.g. AKS 32R · KoolProg · CAN RJ PC tool · used it must be short circuited · Superheat controller · EKE 1B - 080G5350 · C1 NC1 · Power · Power supply · 24 V AC± 20% – 24 V DC± 20% + C1 NO1 · 18 V · + Relay Power · (optional)T fuse2.5 A (optional)backupBatt Normally open ornormally closed(optional) · ETS 5M · ON/OFF Alarm · solenoid · ETS 6 valve valve · ETS / KVS · Colibri ® · CCMT / CTR valve · CANBus · DI2 COM NTC (S2)  Optional · TC (S3/S4) N CANBus · I1 (ON/OFF)* D AI4 (0 / 10 V ) 080G0075 (opt.) · L H GND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · L H GND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · Danfoss  80G318.10 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ +/~+/~ GND Bat+ A1 A2 B1 B2 NO1NO1 C1C1 NC1NC1 · brown black orange yellow · orange yellow red black · white black red green]*

**Table 7: EKE 1B** **p inout**

|**COM**|**Common**||
|---|---|---|
|AI|Analog inputs NTC 10K|S3/S4 selectable via software|
|AI2|Analog input NTC 10K|S2|
|AI3|Analog inputs 0 – 5 V / Ratiometric pressure transmitter|Pe|
|AI4|analog inputs 0 – 10 V|External Reference signal|
|COM|Common||
|DI1|Digital input 1|Main switch (hardware)|
|DI2/3|Digital input 2 and 3|Software configurable DI|
|5V+|Power output for Ratiometric pressure transmitter 0 – 5V||
|COM|Common||

- **NOTE:**

- If Dl1(On/Off) switch is not used it must be short circuited

- EKE 2U Backup power module is recommended to use to ensure closure of the electronic valves. in case of power failures

###### **Fi** **g ure 5: EKE 1C - Front board connection overview**

*[Figurtekst: Master controller · *  Note : If Dl1(On/Off) switch · is not used it must be short · circuited · Pressure Transmitter · Ratiometric 0.5 – 4.5 V AKS cable · connection · 1 060G1034 · 3 C C C · 2 · e.g.  AKS 32R · Superheat controller Superheat controller · EKE 1C - 080G5400 · CAN RJ · CAN RJ · CANBus Local network CAN RJ RS485 RTU MODBus · EKE /  supervisor · master  network · controller · MMIGRS display MMIMYK KoolProg · 080G0294 (optional) Gateway PC tool · NTC S3/S4 (optional) AI4 (V/I) COM DI2* COM · (Optional) DI1 (ON/OFF) · NTC/PT 1000 (S2) NTC/PT 1000 (S3/S4) · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · 15V+ 5V+ COM AI5 AI4 AI3 AI2 AI1 COM COM DI2 DI1 COM · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · 15V+ 5V+ COM AI5 AI4 AI3 AI2 AI1 COM COM DI2 DI1 COM · R120 CANH CANL GND RGND D+ D- · Danfoss  80G315.10 · R120 CANH CANL GND RGND D+ D- · CANBus · 080G0075 (optional)]*

**Table 8: EKE 1C** **p inout**

*[Figurtekst: COM Common · AI1 Analog inputs temperature NTC 10K / PT1000 S3/S4 selectable via software · AI2 Analog inputs temperature NTC 10K / PT1000 S2 · AI3 Analog inputs voltage / current Pe · AI4 Analog inputs voltage / current Ext. Ref. or Pc · AI5 Analog inputs NTC temperature S3/S4 selectable via software · COM Common · 5V+ Power outputs for Ratiometeric pressure transmitter 0 – 5V · 15V+ Power output for current signal pressure transmitter · DI1 Digital input 1 Main switch (hardware) · DI2 Digital input 2 Software configurable DI · 24V+ Not used in EKE 1C · AO1 Not used in EKE 1C]*

- **NOTE:**

- EKE 2U Backup power module is recommended to ensure closure of the electronic valves. in case of power failures

- If Dl1(On/Off) switch is not used it must be short circuited

- EKE 1A/1B/1D only support Ratiometric 0.5 to 4.5V pressure transmitter

###### **Fi** **g ure 6: EKE 1C - Back board connection overview**

*[Figurtekst: Superheat controller Superheat controller · EKE 1C - 080G5400 · C1 NO1 · Power · p ower su– pp l y + C1 NC1 · 18 V · + · 24 V AC 24 V DC 2.5 A batt Normally open orAlarm Relay Power · ± 20% ± 20% T fuse backup normally closed · (optional) (optional) (optional) · ETS 5M · ON/OFF Alarm · solenoid · ETS 6 valve valve · ETS / KVS · Colibri ® · CCMT / CTR valve · Different types of 4 - 20 mA pressure Transmitters need different supply levels. Check the guide below · Table 9: EKE 1C  p ressure transmitters ran g e · Fi g ure 7: Connection for 4 - 20 mA · Pressure Transmitter · 4 - 20 mA · 1 · 3 · 2 · e.g.  AKS 33 · Danfoss  80G316.10 · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ /~/~ + GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · brown black orange yellow · orange yellow red black · white black red green · Danfoss 80G298.10 COM 15V+5V+ DI25V+ COMDI1 COMAI5 AI4 AI3 AI2 A 1D I 3 COM]*

|**User selection EKE connection**|**Signal**|**EKE Connection**|
|---|---|---|
|Not defined|-|-|
|AKS 32R|Ratiometric 10-90%|5V supply from EKE|
|112CP (Sensata)|Ratiometric 10-90%|5V supply from EKE|
|OEM Ratio|Defined by parameters|5V supply from EKE|
|NSK (Saginomiya)|Ratiometric 10-90%, 0.5 to 4.5V|5V supply from EKE|
|AKS 32 1-5V|1-5V|15V supply from EKE|
|OEM Voltage|Defined by parameters|15V supply from EKE|
|Bus shared|Via RS485 Modbus|-|
|AKS 32 1-6V|1-6V|15V supply from EKE|
|AKS 32 0-10V|0-10v|15V supply from EKE|
|AKS 33|4-20mA|15V supply from EKE|
|XSK (Saginomiya)|4-20mA|15V supply from EKE|
|OEM Current|Defined by parameters|15V supply from EKE|

######  **NOTE:**

- EKE 2U Backup power module is recommended to ensure closure of the electronic valves. in case of power failures

- If Dl1(On/Off) switch is not used it must be short circuited

- EKE 1A/1B/1D only support Ratiometric 0.5 to 4.5V pressure transmitter

###### **Fi** **g ure 8: EKE 1D connection overview**

*[Figurtekst: Master controller · MMIGRS2 Display · CANBus · CAN RJ · 080G0294 (optional) · Supervisor EKE · network MMIMYK · AKS Cable  Gateway · connection · 060G1034 · 1 · 3 · 2 · Pressure transmitter CAN RJ · e.g. AKS 32R · KoolProg · CAN RJ PC tool · used it must be short circuited · Superheat controller · EKE 1D - 080G5360 · C1 NC1 · Power · Power supply · 24 V AC± 20% – 24 V DC± 20% + C1 NO1 · 18 V · + Relay Power · (optional)T fuse2.5 A (optional)backupBatt Normally open ornormally closed(optional) · ETS 5M · ON/OFF Alarm · solenoid · ETS 6 valve valve · ETS / KVS · Colibri ® · CCMT / CTR valve · Table 10: EKE 1D  p inout · COM Common · AI Analog inputs NTC 10K S3/S4 selectable via software · AI2 Analog input NTC 10K S2 · AI3 Analog inputs 0 – 5 V / Ratiometric pressure transmitter Pe · AI4 analog inputs 0 – 10 V External Reference signal · COM Common · DI1 Digital input 1 Main switch (hardware) · DI2/3 Digital input 2 and 3 Software configurable DI · 5V+ Power output for Ratiometric pressure transmitter 0 – 5V · COM Common · CANBus · DI2 COM NTC (S2)  Optional · NTC (S3/S4) CANBus · DI1 (ON/OFF)* AI4 (0 / 10 V) 080G0075 (opt.) · L H GND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · L H GND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · Danfoss  80G318.10 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ +/~+/~ GND Bat+ A1 A2 B1 B2 NO1NO1 C1C1 NC1NC1 · brown black orange yellow · orange yellow red black · white black red green]*

 **NOTE:**

- EKE 2U Backup power module is recommended to ensure closure of the electronic valves. in case of power failures

- If Dl1(On/Off) switch is not used it must be short circuited

#### **3.4 Cabling lengths for dif f** **erent connections**

##### **Considerations:**

- The max. cable distance between the controller and the valve depends on many factors like shielded/unshielded cable, the wire size used in the cable, the output power for the controller and EMC.

- Keep controller and sensor wiring well separated from mains wiring.

- Connecting sensors by wires more than the specified length may decrease the accuracy of measured values.

- Separate the sensor and digital input cables as much as possible (at least 10 cm) from the power cables to the loads to avoid possible electromagnetic disturbance. Never lay power cables and probe cables in the same conduits (including those in the electrical panels).

- For the CANbus cable, it is best to use 24 AWG shielded twisted-pair cable with a shunt capacitance of 16 pF/ft and 100 Ω impedance.

- The controller provides a communication interface which is connected to the RJ and CAN terminals.

- Terminal resistors 120 Ω for terminal devices are recommended at both ends of the bus (first and last node) Terminal resistance between H and R terminals.

**Table 11: EKE controller su** **pp orts the followin** **g max. cable len** **g th**

|**Inputs**|**Cable length**|**Wire size (Min. / Max.)**|
|---|---|---|
|Analog inputs (Current/Voltage)|max. 10 m|0.14 /1.5 mm<sup>2</sup>|
|Temperature sensor|max. 10 m|-|
|Stepper valve connection|max. 30 m|0.14 /1.5 mm<sup>2</sup>|
|Power supply|max. 5 m|0.2 /2.5 mm<sup>2</sup>|
|Digital input|max. 10 m|0.14 /1.5 mm<sup>2</sup>|
|Digital output|-|0.2 /2.5 mm<sup>2</sup>|
|Digital MMI|max. 3 m over CAN RJ|-|
|Communication bus|max. 1000 m|0.14 /1.5 mm<sup>2</sup>|

- All valves are driven with a 24 V supply chopped to control the current (Current driver).

- The stepper motor is connected to the “Stepper Valve” terminals (see terminal assignment) with Danfoss M12 connection cable.

- To configure stepper motor valves other than Danfoss stepper motor valves, the correct valve parameters must be set as described in the Valve configuration section (see the configuration section for details).

- The correct valve must be defined in “Valve configuration”, i.e., parameter I067.

**Table 12: ETS Colibri / KVS Colibri / ETS / KVS / CCM / CCMT / CTR**

|**Danfoss M12 Cable**|**White**|**Black**|**Red**|**Green**|
|---|---|---|---|---|
|ETS Colibri® / KVS Colibri /<br>CCMT / CTR / CCM Pins|3|4|1|2|
|EKE terminals|A1|A2|B1|B2|
|**Table 13: ETS 6**|||||

|**Wire color**|**Orange**|**Yellow**|**Red**|**Black**|**Gray**|
|---|---|---|---|---|---|
|EKE terminals|A1|A2|B1|B2|Not connected|
|**Table 14: ETS 5M**||||||
|**Wire color**|**Brown**|**Black**|**Orange**|**Yellow**|**Red**|
|EKE terminals|A1|A2|B1|B2|Not connected|

###### **Fi** **g ure 9: ETS/KVS colibri**

*[Figurtekst: ETS / KVS · Colibri® and  ETS6 valve ETS5M valves · CCMT valves · white orange Brown A1 · black yellow black A2 · red red orange B1 · green black yellow B2 · Danfoss 80G298.11]*

##### **Guideline for long M12 cables on Danfoss stepper motor valves**

- Long cables will lead to degradation of performance

- You can overcome this degradation by changing the settings for the valve driver. This guideline is based on the cable type being the same type as the standard Danfoss stepper motor cable

**Table 15: Recommended wire size and cable distance (twisted** **p air) between EKE controller and ste** **pp er motor valve**

|**Cable length**|1 m – 15 m|15 m – 30 m|
|---|---|---|
|**Wire diameter**|0.52 / 0.33 mm<sup>2</sup>20 / 22 AWG|Min. 0.52 mm<sup>2</sup>20 AWG|

##### **Tip for updating I028 parameter for 15m - 30m cables:**

1. Use koolProg online service option (EKE should be connected)

2. Select the desired valve first

3. Again change to user defined option, the valve default settings of previous selected valve will be loaded automatically

4. Change only the I028 parameter. According to the value in below table

**Table 16: Parameter settin** **g for lon** **g M12 cable 15 - 30 m**

|**Product**|**I028 Valve drive current**|
|---|---|
|ETS 12C - ETS 100C<br>KVS 2C - KVS 5C|925mA peak|
|ETS 12.5 - ETS 400<br>KVS 15 - KVS 42||
|CTR 20|200 mA peak|
|CCMT 2 - CCMT 8||
|CCM 10 - CCM 40||
|ETS 6|270mA peak|
|CCMT 0|270mA peak|
|CCMT 1|400mA peak|
|CCMT 16 - CCMT 42|450mA peak|
|ETS 5M|190mA peak|

#### **3.5 Connecting Relay Outputs**

EKE1 series has 1 relay output

- Type SPDT relay. Digital Output can be used to connect either a solenoid valve or an alarm

###### **Fi** **g ure 10: SPDT rela** **y**

*[Figurtekst: Power · C1 NO1 · Relay Power · Normally open or · normally closed · (optional) · ON/OFF Alarm · solenoid · valve · NO1NO1 C1C1 NC1NC1]*

 **NOTE:**

The relays cannot be used for the direct connection of loads such as LEDs and ON/OFF control of EC motors. All loads with a switch-mode power supply must be connected to a suitable contactor or similar

#### **3.6 Temperature Sensor Mounting**

###### **Fi** **g ure 11: Tem** **p erature sensor mountin** **g**

*[Figurtekst: Danfoss · 84N403.10 · Evaporator Close to evaporatorClose to the · evaporat or]*

###### **Fi** **g ure 12: Tem** **p erature sensor mountin** **g**

*[Figurtekst: 1 2 3 · OD 112 - 16 mm/2 - 5/8 in. · 3/4 - 7/8 in. · OD 18 - 22 mm · conductive paste evaporator outlet OD 1 - 125 - 35 mm 3 /8 in. · 1 3 /8 in. and higher · OD 35 mm and higher · Danfoss 60G496.11 · nfoss N365.11 · Danfoss 84N366.12]*

######  **NOTE:**

- Mount sensor on a clean surface without any paints

- Remember to put on heat conducting paste and insulate the sensor

- Sensor mounting max. 5 cm from the outlet of the evaporator

- Physical temperature sensor can’t be shared

 **NOTE:**

Installation of the pressure transmitter is less critical. but mounting of pressure transmitter should be closer to the temperature sensor right after the evaporator and with its head in “upright position

#### **3.7 Power and signal sharing**

#### 3.7.1 Sharing Power Sources

The EKE 1x series can share common power supplies with multiple controllers because the power supply input of the EKE is galvanically isolated from the outputs. The external power supply must have enough power rating Watt/VA to operate multiple EKEs and most importantly enough power to run the valves. The Battery backup is an optional feature. If Battery backup is connected to EKE terminals, the EKE will close the stepper motor if the controller losses its supply voltage

1. A special attention is needed on sharing both external power supply as well as battery backup. it is not allowed to share AC power supply and DC EKE 2U backup battery simultaneously with multiple controllers

2. In case both DC power supply and battery are shared between several units, it is recommended to have the negative poles of battery and power input shorted together at each unit. Such solution requires EMC test to be conducted on the final equipment by customer

###### **Fi** **g ure 13: Power sharin** **g from EKEs**

*[Figurtekst: CAN RJ CAN RJ CAN RJ · Superheat controller Superheat controller Superheat controller · EKE 1x - 080G5xxx EKE 1x - 080G5xxx EKE 1x - 080G5xxx · EKE 1C EKE 1C EKE 1C · Shared power supply type AC · Shared battery back u p DC · Fi g ure 14: Sharin g  a DC source and EKE 2U module with multi p le EKEs · CAN RJ CAN RJ CAN RJ · Superheat controller Superheat controller Superheat controller · EKE 1x - 080G5xxx EKE 1x - 080G5xxx EKE 1x - 080G5xxx · D– D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM D– D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM D– D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · Danfoss 80G295.10 · –/~ –/~ +/~ +/~ · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · Danfoss 80G338.10 · Danfoss 80G295.10 D– D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM D– D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM D– D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · –/~ –/~ +/~ +/~ · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1]*

Danfoss recommends using EKE 2U as the preferred battery backup device, for more details check the EKE 2U datasheet. The battery backup device power rating Watt/VA must match the valves requirements

 **NOTE:**

- The power supply terminals must be connected at every Unit.

- The battery voltage must not be connected from main power supply connected to EKE.

- A battery voltage lower than 16.5 V and higher than 27V will trigger the battery alarm.

- It is not allowed to shared AC power supply and DC backup battery simultaneously with multiple controllers.

- EKE 2U can only support a maximum of two valves for emergency closing, or only one valve in case the valve used consumes higher power. See EKE 2U documents for more details.

#### 3.7.2 Sharing input signal

The EKE cannot share digital inputs.The digital inputs (voltage free Contacts) cannot share the same signal directly or be connected to external power supply.To share a digital signal between multiple digital inputs, a special circuitry is needed. For example, Each DI can be provided with its own relay (or optocoupler) that must withstand 100mA impulses at15V. EKE 1 series (Except 1C) can share analog input between multiple controllers

###### **Figure 15: Possible circuitry to share a digital signal between Multiple EKE**

*[Figurtekst: 80G340.10 · Power supply · D0 · – · + · D1 · COM · Relay · EKE · D1 · COM · Relay · EKE · D1 · R · COM · Optocoupler · EKE]*

#### 3.7.3 Sharing pressure sensor signal

For **EKE 1A, EKE 1B, EKE 1D** up to 5 controllers can share one Ratiometric pressure transmitter readings. To get a correct acquisition on all the units all the three wires (GND, 5V and transmitter signal, output) must be routed to every unit

###### **Fi** **g ure 16: Si** **g nal sharin** **g between EKE 1A, 1B, 1C, 1D**

*[Figurtekst: EKE 1B EKE 1B EKE 1B · AKS · 32R · Si g nal · GND · S u pp l y · (GND, 5V and transmitter signal, output) must be routed to every unit · Danfoss 80G335.10 · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · Com AI1/ DI3 Ai2 A I3 AI4 C om DI1 DI2 5V + Com COM]*

 **NOTE:**

For a correct acquisition on all the units all the three wires (GND, 5V and transmitter signal, output) must be routed to every unit

In **EKE 1C** , a physical pressure transmitter can only be shared via wired CANBus or Modbus

**Sensor Signal sharing via CANBus in EKE 1C, 1D** in EKE 1C, 1D Signal can be broadcasted once per second to all the following parameters enable/disable broadcasting of local signals (refer to the configuration parameter section):

[G012 - Signal sharing Pe] [G013 - Signal sharing Pc] [G014 - Signal sharing S3]

- If two or more sensors are connected to same sharing group, the controller which start up as the first one will broadcast the signal.

- If the receiving controllers has not received a shared signal from another controller for 3 seconds (parameter G003 CAN bus min update interval) it will start broadcast the local sensor.

- When more controllers are connected via CANBus each end of the bus must be terminated with a jumper between CANH and R120

 **NOTE:**

Broadcasting is not possible via Modbus. In case of Sensor error, broadcast will stop.

Only EKEs from the same group address can share signals

- Group 1 address 1 to 31

- Group 2 address 32 to 63

- Group 3 address 64 to 95

- Group 4 address 96 to 125

A controller knows its own address and knows from which address the broadcast is coming, this information is used to discard broadcast signals for controllers outside own group.

Address 0 is invalid, Address 126 and 127 are reserved for remote displays.

###### **Fi** **g ure 17: Sensor Si** **g nal sharin** **g**

*[Figurtekst: Temperature · sensor · Pressure · transmitter · EKE 1C EKE 1C EKE 1C · CAN · Jumper Jumper · Danfoss 80G336.10 · RI 20 CAN H CAN L GND RI 20 CAN H CAN L GND RI 20 CAN H CAN L GND]*

**Receiving Sensor Signal via Modbus:** EKE 1B/1C controllers can receive the external sensor values like Po, Pc, S2, S3 and S4 via Modbus. In some applications, the suction pressure and/or the refrigerant temperature on the evaporator outlet, is measured by a system controller. In these cases, the sensors can be omitted from EKE, and the sensor values can be received via Modbus instead. This requires that the systems main controller continuously transmits these values to EKE, If no new sensor value is received within defined Modbus time interval in seconds i.e. G004 of the last transmission, the EKE will raise sensor alarm which will stop the regulation.

**Example** : The suction gas temperature S2 and the evaporator pressure Pe can be set by activating bus shared sensor configuration registers i.e “I040 = 5” and “I044 = 8” respectively.

**Fi** **g ure 18: Receivin** **g si** **g nal via Modbus**

*[Figurtekst: Master controller · RS485 MODbus · Sensor values · Temperature sensor · EKE controller · Pressure transmitter · Danfoss 80G337.10]*

#### **4 Applications**

EKE series devices are used where precise control of superheat in air conditioning system is needed. It helps achieving high energy efficiency and reliable operation

EKE serves 2 main applications:

- Controller Mode

- Standalone Superheat control

- Temperature control

- Driver Mode

The need for cooling can either be defined by the incoming media (S3) or the outgoing media (S4) temperature

#### **4.1 Controller Mode**

#### 4.1.1 Superheat control mode

EKE can serve as a PI controller for stepper motor valve that controls the superheat of the evaporator based on a pressure Pe and temperature (S2) sensors. In superheat mode the controller will control the superheat to be stable and close to the superheat reference. If superheat is too low the flow in the expansion is decreased and superheat will be higher

###### **Fi** **g ure 19: Su** **p erheat control a** **pp lication**

*[Figurtekst: EKE 1X · Pe · S2 · EEV · Danfoss 80G8222.01]*

#### 4.1.2 Temperature control mode

Temperature control Can be accomplished via a signal from temperature sensor S3 placed in the air flow before the evaporator or S4 placed in the air flow after the evaporator.

EKE has 2 methods of controlling temperature:

- ON/OFF thermostat

- Modulating thermostat (MTR)

The temperature control can be done using an ON/OFF thermostat that opens/closes the stepper valve as per S3/S4 temperature values or modulating thermostat that regulates the stepper valve more smoothly based on S3/S4 temperature setpoints. The need for cooling can either be defined by the incoming media (S3) or the outgoing media (S4) temperature

###### **Fi** **g ure 20: Tem** **p erature control a** **pp lication**

*[Figurtekst: Preset OD / Defrost Heat / cool mode · main switch · Battery · Power 24 V AC / 24 V DC · External reference · Optional connection EKE controller · Mandatory connection · Temperature control · S4 · Alarm indication · Normal close · S2 Pe · EEV S3 · Danfoss 80G8223.01]*

 **NOTE:**

EKE1A cannot support thermostatic modes

#### **4.2 Driver Mode**

A master is commanding the valve open degree to the EKE controller. The control signal can be fed for example by:

- Analog signal e.g., 0 – 10 V, a 0 – 20 mA

- Bus communication

###### **Fi** **g ure 21: EKE as Driver Mode**

*[Figurtekst: Battery Optional connection · Mandatory connection · Power 24 V AC / 24 V DC · ON/OFF signal · Modbus or Analog signal · EKE controller (in driver mode) · MASTER controller · Alarm indication · Normal close · Pe · S2 · EEV · Danfoss 80G8221.01]*

 **NOTE:**

'Normal closed' valve in front of EEV is optional alternative to a battery backup solution which closes the EEV in case of power fail. The Digital output can also be used as alarm indication to the master controller. The Master can send a start signal to EKE DI terminals

#### **4.3 Typical EKE applications**

The EKE 1x series can be used for various refrigeration applications like Chiller, Reversible Chillers, Reversible Heat pump, AC air handler, cold room Standalone, Multi evaporators ext.

**Chiller (cooling only)**

**Fi** **g ure 22: Chiller (coolin** **g onl** **y )**

*[Figurtekst: y · S4 · E · ETS Colibri® · S3 C · Pe · S2 · EKE · EKE controller · controller · Danfoss R64-3032.10]*

**Reversible chillers (Air to water) Fi** **g ure 23: Reversible chillers (Air to water)**

*[Figurtekst: S4 · E ETS Colibri® C · S4 · S3 · S3 · P Pe · S 2 · EKE  EK E · co ntrollerntroller · Danfoss R64-3030.10]*

##### **Reversible Chiller Heating**

**Fi** **g ure 24: Reversible Chiller Heatin** **g**

*[Figurtekst: S4 · C ETS Colibri® E · S4 · S 3 · S3 · P Pe · S2 · Reversible heat pump · Fi g ure 25: Air to water heat  p um p  coolin g · E · C ETS Colibri® · EK EKE E  Pe · co controllerntroller · S2 · Danfoss R64-3030.10 · Danfoss R64-3039.10]*

**Fi** **g ure 26: Air to water heat** **p um** **p coolin** **g**

*[Figurtekst: C · E ETS Colibri® · Pe · EKE · con trollertroller · S2 · AC air handler · Fi g ure 27: AC air handler · E ETS Colibri® · S3 S4 · C · Pe · S2 · Danfoss R64-3036.10 · Danfoss R64-3040.10]*

**Cold Room**

###### **Fi** **g ure 28: Cold Room**

*[Figurtekst: Cold room · EKE · controller · C · ETS Colibri® · S3 · E · S2 · Pe · In door Out door · Danfoss R64-3038.10]*

**Multi evaporator Fi** **g ure 29: Multi eva** **p orator**

*[Figurtekst: C · ETS Colibri® ETS Colibri® · EKE  EKE · controller controller · E E · S4 · S3 · S2 S2 Pe · Danfoss R64-3037.10]*

#### **5 User Interface**

In this section the user interfaces are described. EKE 1x controllers can be used with 2 main user interfaces:

- MMI display

- KoolProg Software

#### **5.1 Conf i** **guration using MMI Display**

MMIGRS2 is a graphical display. The connection with each EKE controller is made through the CAN RJ or CANBus network. All the information about the user interface is loaded inside the EKE controller. that’s why there is no need of programming the MMIGRS2 interface.

MMIGRS2 is powered externally or from the controller (while using RJ12) which it is connected to and automatically shows its user interface. EKE can be configured with basic settings quickly using the wizard setup and advanced settings can be made afterwards.

###### **Fi** **g ure 30: Connectin** **g MMIGRS interface**

*[Figurtekst: ACCCBI 080G0075 · CAN RJ · CAN RJ · MMIGRS2 · Superheat controller · EKE 1A - 080G5300 · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · Danfoss  80G313.10 · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1]*

When MMI is not connected to EKE via CANRJ12 the autodetection feature of the EKE CAN address will not work.

Therefore, check the following MMIGRS2 setting:

1. enter BIOS menu pressing and holding X + Enter keys for 5 s.

2. select “MCXselection”->” Manual Mode” and set the CAN address of the EKE you wish to connect to. CAN H-CAN R shorting should be done only on the first and last node of the network.

For the series EKE 1C and EKE 1D, to connect via MMI via the wired CAN, the R and H terminal of the MMI needs to be shorted.

###### **Fi** **g ure 31: MMIGR2 Back view**

*[Figurtekst: RJ CAN connector · Termination Jumper · between R and H · For cable >3m (only EKE 1C) · 2-way screw connector for · power supply · 4-way screw connector for · CANbus network · Danfoss 34G306.10]*

######  **NOTE:**

Even when connecting to the MMI via CAN RJ12 cable, it is still required to short R and H of the MMI.

#### 5.1.1 MMIGRS2 Setup and service

**Table 17: MMI setu** **p and service**

|**Setup and service**|**Setup description**|
|---|---|
|**Reference**|Main switch, Mode selection|
|**Control**|General control parameter for example selecting control mode, protection function ext..|
|**Defrost**|Parameters about the defrost mode|
|**Alarm configuration**|Alarm parameters|
|**IO config**|IO configuration<br>Sensor’s configuration<br>Valve Configuration<br>External reference configuration|
|**Display**|For:<br>Changing the language.<br>Login timeout.<br>Changing passwords.<br>Brightness.<br>Display unit (Metric or Imperial).<br>Opening Degrees Unit|
|**Communication**|Communication settings<br>Signal sharing, signal sharing update interval|
|**Service**|Service Mode allows Entering<br>-Manual mode, Service Mode and Applying factory default.|
|**Setup wizard**|The Wizard is a quick tool for configuration, the workflow is as follows<br>a. Language selection.<br>b. Application selection.<br>c. Input configuration.<br>d. Output configuration.<br>When using the Setup Wizard, repeat the following sequence for all parameter settings:<br>a. From Setup wizard, select relevant parameters.<br>b. Press ENTER to highlight 1st option<br>c. Scroll with UP / DOWN to your desired option<br>d. If the selected default value is acceptable, press DOWN to get to the next settings. Otherwise, press ENTER to set your choice<br>e. Scroll with DOWN to the next parameter (repeat sequence a. to e.)|

###### **Fi** **g ure 32: MMI setu** **p and service**

*[Figurtekst: 1 · Power on · 3 Login PW: · 2 Commissioning 300Service 200 · Press and hold  Daily 100 · enter · 5 · Esc · Status menu Setup and service · Reference · QR code Control · Controller info Defrost · Detailed status · SH trend 25 min · Display Display · Communication · Service 4 · Home menu Setup wizard · Controller name · Danfoss · 80G294.20]*

 **NOTE:**

For more parameter and settings refer to the parameter table

#### 5.1.2 MMIGRS2 Main screen

On the main screen the following data are displayed:

- The main analog inputs measurements or other information.

- The icon indicating operating status.

- The alarm or service icon.

###### **Fi** **g ure 33: MMIGRS2 Main screen**

*[Figurtekst: Up · Escape/Cancel · Right · Left · Enter · Down · Homescreen Navigation help · Controller name  Alarm indicator · R eference point · Primary readout · Operating status · Evap. temperature S 2 – S4 · Evap. pressure M edia · Valve O D t emperature]*

**Table 18: Navi** **g ation throu** **g h MMIGRS2**

|**Unit Status**|**Key**|**Function**<br>Home screen|**Description**<br>Shows the operating status.|
|---|---|---|---|
||Right x1|Active alarms|Access to Active alarm list. Press UP and<br>Down button to see complete list|
||Right x2|Trend SH 25 min|Shows logged Superheat graph for 25<br>minutes.|
||Right x3|Detail Status|Shows detail operating status. Press UP<br>and Down to see complete list.|
||Right x4|Controller info|Provides information about the product|
||Right x 5|QR code|QR code that directs you to the product<br>webpage for more info.|
||Holding Enter for 3 seconds|Log in / Setup and Service|If User has not logged in, Enter pass-<br>word. Press UP/Down to change digit<br>and Enter to confirm the value.|
||Escape/Cancel||Go back to main screen|
||Holding Escape for 3 Sec|Logged out|User logout|
|**Login**||||
||Up|+|Increment the selected digit|
||Down<br>Enter<br>Escape/cancel|-<br>ok|Decrement the selected digit<br>Confirm the vale and skip to the next<br>digit or execute login<br>Go back to main menu.|

**Table 19: Exam** **p les**

*[Figurtekst: Parameter Navigation Parameter change(R012) Factory re-setting of display: · Navigation and reading the status of the parameters For examples, parameter R012 (for the main switch). 1. Pressing the bottoms X and ENTER at the same · is possible. Can be changed through reference  =>  main switch time for 5 second · 2. Select MCX SELECTION · 3. Select CLEAR UI]*

*[Figurtekst:  WARNING: · H - R · Termination]*

#### 5.1.3 ERR31 Error Alarm on the external display - MMIGRS2

If the communication to the display is not carried out correctly, it will send an “ERR31” error notification. This may be caused by the displayed wires H to R not being shorted, or that there have been interruptions in data communication during the time when the display retrieves the basic information from the controller. Once the terminations have been inspected, you should then check the software version of the external display. This is done by holding down the Enter key and the X key for 5 seconds, until the Bios menu appears. Next, press the X key and read off the software version in the bottom right corner. The software version must be 1.13 or newer. Once the display’s software version has been checked, check the display’s settings as follows:

1. Hold the Enter key and the X key down for 5 seconds, until the Bios menu appears.

2. Select the “MCX selection” menu - Select the “Clear UI” line and press Enter - Select the “Autodetect” line and press Enter.

3. Press the X key to return to the Bios menu.

4. Select the “COM selection” menu - Select the “CAN” line and press Enter .

5. Press the X key to return to the Bios menu.

6. Select the “Startup mode” menu - Select the “Remote application” line and press Enter.

7. Press the X key to return to the Bios menu.

8. Select the “CAN” menu - Select the “Baudrate” line and check that it is 50K - Select the “Node ID” line and check that it is 126

9. Press the X key to return to the Bios menu.

10. Select the “Application” menu and press Enter. The display will once again retrieve data from the controller. This process will take about 5 minutes

#### 5.1.4 Service mode through MMIGRS2

Service mode is designed to provide a very simple way of operating the valve for diagnostic and service purpose. There is neither application nor protection in this mode. The user can open and close the valve using simple button presses on MMIGRS2.

######  **NOTE:**

This mode only has a home screen and do not have any menu structure. All function is carried out using the “Escape”, “Up”, “Down” and “Enter” buttons on MMIGRS2

Service mode is only available via MMIGRS2 display. This function is not possible in KoolProg

###### **Fi** **g ure 34: Service mode throu** **g h MMIGRS2**

*[Figurtekst: Service screen · Controller name Navigation help · Requested step · Actual step positio n position · Valve Type · Speed · Current (mA Peak) · Total no of step s]*

###### **Fi** **g ure 35: Service mode throu** **g h MMIGRS2**

*[Figurtekst: Up : Adjust requested step position upward · Escape: Leave service mode · Right , Left : Navigate to alarm list, status, · controller info · Enter short press: start edit of requested · position/accept change · Enter press for 2 sec: change valve selection · UP and Down together: set actual step · position to 0 step]*

#### **5.2 Conf i** **guration using KoolProg Software:**

KoolProg is a software tool that can configure the EKE Controllers in fast and easy way. The main features of the KoolProg are listed as follows

- Make Online changes to parameter configurations

- Monitor live status of inputs and outputs

- Quickly analyze controller behavior. and program patterns by using the graphical trending tool

###### **Fi** **g ure 36: Connectin** **g kool** **p ro** **g to EKE 1x**

*[Figurtekst: CANRJ · EKE · Power · supply · USB · MMIMYK Gateway · Danfoss 80G296B.10]*

- **NOTE:**

- Make sure to install the latest version of the EKE.

- The connection of the EKE to the koolprog software, must be done through the MMIKYK gateway.

- KoolProg software do not support multiple EKE controllers in a daisy chain network.

- EKE must be powered up before starting programming.

- To guarantee a reliable USB connection to a host device (e.g., industrial PC), you must: keep USB cable length < 1 m.

- When prgoramming with koolprog if there is any error with values set then EKE will go to factory defualt settings after restart. Make sure values entered are within range specfied for each parameter.

###### **Fi** **g ure 37: kool** **p ro** **g to EKE 1x**

- Create your own configuration files on your PC without • Quickly program one. or multiple controllers • Quickly analyze controller behavior and program having to connect a controller by using the progress and completion status patterns by using the graphical trending tool

- • Import a parameter configuration file to your PC from a indicators • Make Online changes to parameter configurations connected controller. Save the file and download it to • Monitor live status of inputs and outputs other controllers of the same model

- • Select the most frequently used parameters as your favorites

- • Find all the technical documentation for each controller model within one location

##### **4.2.1 Setting Up KoolProg**

KoolProg software supports wide range of Danfoss product, so first you need to select the EKE 1x series from the preferences.

###### **Fi** **g ure 38: Settin** **g U** **p KoolPro** **g**

Then if you want to setup, click the set parameter and select a new project

###### **Fi** **g ure 39: Settin** **g U** **p KoolPro** **g**

Then select the EKE variant you have

**Fi** **g ure 40: Settin** **g U** **p KoolPro** **g**

###### **Fi** **g ure 41: Settin** **g U** **p KoolPro** **g**

- **NOTE:**

- The product code number and product versions are found in the product label.

- The wizard tool is optional, it allows to go through a quick configuration for a specific application. You can still configure it through the koolprog main menu

##### **4.2.2 KoolProg Wizard for Rapid Controller Configuration:**

The KoolProg wizard, is a tool that allows you to quickly set the parameters for your specific application. The workflow for the wizard is as follows:

The Wizard is a quick tool for configuration, the workflow is as follows

1. Language selection

2. Application selection

3. Input configuration

4. Output configuration

**Fi** **g ure 42: Wizard for Ra** **p id Controller Confi** **g uration**

**Fi** **g ure 43: Wizard for Ra** **p id Controller Confi** **g uration**

###### **Fi** **g ure 44: Wizard for Ra** **p id Controller Confi** **g uration**

**Fi** **g ure 45: Wizard for Ra** **p id Controller Confi** **g uration**

*[Figurtekst: Fi g ure 46: Confi g uration usin g  KoolPro g  wizard]*

##### **4.2.3 KoolProg Set parameters menu**

The main menu is used to get a configuration file with the desired settings that can be uploaded to EKE 1x devices, you can customize the parameter according to your specific application. The parameters are organized in parameter groups. Also, you can use the search box to search for a parameter, however Search feature will only display the parameters relevant to your settings. Example I035, I034 min max external voltage reference only appears if you select R102 as 'Valve driver' and I033 as 'Voltage to OD'

- **NOTE:**

The parameters for various applications are illustrated in the configuration section

**Fi** **g ure 47: kool** **p ro** **g main menu, exam** **p le EKE 1C**

###### **Fi** **g ure 48: U** **p loadin** **g the settin** **g s to EKE**

**Table 20: KoolPro** **g main Menu Summar** **y**

|**Parameter Group**|**Setup description**|
|---|---|
|**Reference**|Main switch, Mode selection|
|**Control**|General control parameter for example selecting control mode, protection function ext.., it is divided into 3<br>sections:<br>Control Basic, Control Advanced, Control heatpump|
|**Defrost Sequence**|Parameters about the defrost mode|
|**Alarm configuration**|Alarm parameters|
|**IO config**|Confuguring For analog and digital inputs|
|**Sensor’s configuration**|Configuring pressure and temperature sensor|
|**Valve Configuration**|Configure settings for the valve|
|**External reference configuration**|For more settings for External reference and the AI4|
|**Display**|Display Settings of the MMI screen, and passwords and logout configuration|
|**Communication**|-Communication settings (controller address, communication baud rate for CANbus and Modbus)<br>-Signal Sharing settings|
|**Service**|Service Mode allows Entering<br>-Manual mode, Service Mode and Applying factory default.|

##### **4.2.4 Copy to device- Uploading configuration file to KoolProg:**

From the parameter selection menu, any change made can be saved as file using the saving options, save or save as, also you can know the folder containing these files by clicking the folder icon. To upload a configuration file. Click on browse, select the file you saved from the parameter selection menu, then click open, then Start.

###### **Fi** **g ure 49: U** **p loadin** **g files throu** **g h co** **py -to-device menu**

##### **4.2.5 KoolProg On-line service Menu:**

The service menu allows a quick analyze controller behavior and program patterns by using the graphical tool. It is also possible to make online changes to parameter configurations and monitor live status of inputs and outputs.

######  **NOTE:**

The service menu is only available in the service mode

###### **Fi** **g ure 50: KoolPro** **g service Menu**

The alarm Menu shows all the warnings or missing I/O in a dynamic way, that depends on the specific application. For example, if your application requires connecting a Sensor S2 and a pressure sensor Pe, and they are not connected, it will appear in the active alarms, if you connect the missing sensors the alarm will disappear

###### **Figure 51: Service Menu Active alarms**

Monitoring the operation is also possible through the koolprog datalogger tool. if you decide to log a parameter you need to select it first then, press the graph icon on top.

######  **NOTE:**

When the startup is complete with success you can setup the datalogger. The datalogger work over the service port so use of KoolProg / MMIGRS2 is not possible when datalogging is active. In case of need to check operation, it requires to stop the datalogger and reconnect KoolProg/MMIGRS2

###### **Fi** **g ure 52: Parameter lo** **gg in** **g**

###### **Fi** **g ure 53: Lo** **gg in** **g p arameters as** **g ra** **p hs**

#### **5.3 Quick Conf i** **guration**

Apart from wizard setup, users can also use the following section which describes quick parameter settings for general applications. For both mode Controller Mode or Driver Mode. The parameters are explained in more detail in the following section.

###### **Fi** **g ure 54: Quick** **g uide for** **p arameter selection**

*[Figurtekst: Driver Controller · Start : Main switch= Off Make sure that main switch is OFF before changing · the settings. The setting will depend on the system · requirement. · Parameter: R012 Main Switch · Select valve type Select predefined Danfoss valve type ETS, ETS C, KVS, · KVS C, CCM, CCMT, CTR, or user defined. · Parameter: I067 Valve configuration · Application mode Select how you want to use EKE: driver or superheat · Driver- Controller controller. · Parameter: R102 Operation mode · Analog signal type e.g1-5 V/0-20 mA Select Refrigerant Select the predefined refrigerant .Parameter: O030 Refrigerant  . · EKE 1A 1B 1 C 1D · Parameters · confireferenceDriver g uration - 1091 1033 1091 Select Temperature  Select Temperature sensor type: EKS, ACCPBT, MBT,Sensata 112CP, Bus Shared, AKS - · Voltage,LowEXT.ref. 1034 1034 1034 1034 Parameter for S2 sensor: I040 for 1C, I081 for 1B andI082 for EKE 1A. · EXT.ref. 1035 1035 1035 1035 Check parameter list for other sensors. · Voltage,high · Select Pressure transmitter · Current,LowEXT.ref. - - 1036 - Select Pressure transmitter type –AKS 32R,Sensata 112CP, OEM Ratio, NSK , AKS 32 1 - 5V, · EXT.ref. - - 1037 - OEM Voltage, Bus shared, AKS 32 1 - 6V, AKS 32 0 - 10V, · Current,high AKS 33, XSK, ACCPBP Current , OEM Current · Parameter for Pe transmitter: I043 for 1C and I085 for · EKE 1B. · Check parameter list for other sensors. · Define Min/Max Pressure  Define min and max Pressure transmitter in barg. · Parameter: O020 - Pe min., O021 Pe max., Check · parameter list for other sensors. · Select Superheat Control Select application control type SH control. 1: MSS, · 2: LoadAp, 3: Fixed, 4: Delta SH. · Parameter: N021 SH reference mode. · Set Min/Max Ref value Set the value for the selected control min./max. · superheat reference. · Parameter N009 SH max., N010 - SH min. · Optional – Force start up, MOP, LOP, Alarm, · Select Other features Thermostat function. · Check parameter list for details. · Remember to turn on main switch to start ‘ON’ . · Finish: main switch = ON Parameter R012 Main switch. · IF EKE 1A · DI1 = ON ON=Regulation start · Parameter O003 :0 = Not Used | 1 = Main Switch · IF EKE 1B or 1C · ‘ON’ = Regulation start · Parameter O002: 0 = Bus –> Start / Stop 1 = Main Switch · If DI1 is not used, make a short circuit with a wire · between DI1 and COM.]*

 **NOTE:**

Some important Parameters e.g., Superheat close function, P control[SO1] , valve neutral zone are enabled in a default setting. Make sure that you activate other feature/function/ alarm as per the application requirement before you start the controller. Refer to the configuration section for more details.

#### **6 Configuration**

#### **6.1 Driver Mode**

In this mode The EKE 1x is acting as stepper motor valve driver, where master is commanding the valve opening degrees to the EKE controller. In this mode, no sensor is needed as we are not doing any superheat control. The control signal can be:

- Analog signal e.g., 0 – 10 V or 4 – 20 mA

- Bus communication via RS485 (Modbus RTU)

**Table 21: Driver mode**

*[Figurtekst: EKE 1A 1B 1C 1D · Applicable · Voltage signal · Current signal · - - - · Bus · -]*

#### 6.1.1 Driver Mode using analog signal

The signal can be used to drive the valve’s opening degree to a desired position. This feature is used to drive the stepper motor valve to the desired level.

**Fi** **g ure 55: Driver Mode usin** **g analo** **g Si** **g nals Parameters**

*[Figurtekst: Valve Opening · Degree % · Analog Input Signal · 100% OD · Analog Input Signal · 0% OD · 0 V 10 V · 4 mA 20 mA · Voltage signal · Current signal · Danfoss 80G8271.01]*

**Table 22: Driver Mode usin** **g analo** **g Si** **g nals Parameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|RI02|Operation mode|1 = valve Driver, select 1 to operate as valve driver|
|I091|Driver reference configuration for 1B, 1D|0 = Voltage to OD|
|I033|Driver reference configuration for 1C|0 = Voltage to OD<br>3 = Current to OD|
|I034|Ext ref voltage low|If I091 or I033 = 0, define min reference voltage|
|I035|Ext ref. voltage high|If I091 or I033 = 0, define max reference voltage|
|I036|Ext ref. current low|If I033 = 3, define min reference current|
|I037|Ext ref. current high|If I033 = 3, define max reference current|

EKE 1A can implement Voltage to OD only

#### 6.1.2 Driver Mode using Communication Bus

##### **Driver Mode using Communication Bus**

The opening degree of a stepper valve can be operated manually between 0% and 100% OD via communication bus.

**Table 23: Driver Mode usin** **g Communication Bus**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|RI02|Operation mode|Mode selection, select 1 to operate as valve driver<br>1 = valve Driver,|
|||Select reference configuration,|
|I091|Driver reference configuration for 1B|1- Modbus to OD| the controller receives opening degrees from<br>the bus|
|||2- Modbus to steps| the controller receives opening degrees<br>from the bus|
|I033|Driver reference configuration for 1C|1 = Bus to OD|<br>2 = Bus to step|
|O045|Manual OD|Set the desired OD in percent|
|B100|Manual step|Set the desired OD in number of steps|
|X004|Modbus main switch|1 = ON, 0 = OFF|
|X002|Modbus preset OD|1 = ON, 0 = OFF|

#### **6.2 Superheat Control Mode**

In this section some important parameters for SH control mode and other sub modes are described.

For basic superheat control, one temperature sensor S2, and one pressure sensor Pe are needed. The actual superheat is calculated based on these two sensor readings, and the controller will adjust the OD of the valve to bring the superheat to the desired reference. If superheat is too low the flow in the expansion is decreased and superheat will be higher and vice versa. For advanced SH control the use of additional temperature and pressure sensors are needed.

###### **Fi** **g ure 56: EKE as SH controller**

*[Figurtekst: EKE 1X · Pe · S2 · EEV · Danfoss 80G8222.01]*

**Table 24: Su** **p er Heat Control Parameters**

|**Parameter**|**Function**|**Selector**|**Description**|
|---|---|---|---|
|**Reference**||||
|R012|Main switch|On|• The software main switch is used to start / or stop refrigerating<br>• The hardware main switch (DI) can be used also.<br>• If the main switch is on changes are not allowed.|
|R102|Operation mode|SH control|Selected to use EKE in the superheat control mode|
|||0-Not Used||
|R014|Thermostatic Mode|1-Cut-in/cut-out mode<br>2-MTR modulating thermostat<br>mode.|If you select Not used, only superheat is regulated regardless of the me-<br>dia temperature.|

|**Parameter**<br>R009|**Function**<br>Temperature<br>Sensor S2<br>correction|**Selector**<br>Defined by the user in K|**Description**<br>Correction value for temperature sensor. This value is defined by the<br>user.|
|---|---|---|---|
|R107|Pressure sensor<br>Pe correction|Defined by the user in Brag|Correction value for pressure sensor. This value is defined by the user.|
|**Sensor configur**|<br>**iation**<br>|||
|I082|S2 sensor<br>configuration|Select based on the supported<br>temperature sensors|Selection of the used temperature sensor.|
|I086|Pe transmitter<br>configuration|Select based on the supported<br>pressure sensors|Selection of the used pressure sensor.|
|**Control Basic**|||dfid f  bl b l d dfi|
|O030|Refrigerant|Select from variety of refrigerants.|User eine rerigerant is possie y Seecting**R user**an eine An-<br>toine constants A1, A2, A3|
|N102|Startup mode|0-Prop.cntrl<br>1-Fix OD with protection<br>2-fix OD without protection|This feature is used when it is necessary to open the valve Quickly when<br>the compressor turns on, to prevent too low suction pressure|
|N021|SH Reference Mode|0-Fixed step<br>1-Loadap<br>2-MSS<br>3-DeltaTemp|Used to choose how the superheat reference is calculated|
|I066|Minimum OD||The valve minimum OD can be set to a required minimum opening posi-<br>tion.<br>Default: 0%|
|N032|Maximum OD||To limit the maximum OD of an oversized valve used in the system. This<br>maximum OD % can be set to lower value if required.<br>Default: 100%|
|**Control Advanc**|**ed**|||
||||If SH control sensor S2, S3*, Pe has an error, then an action can be set<br>top position the valve OD.|
|N143|SH control sensor<br>error action|0-Stop<br>1- Fixed OD<br>2-Average|• Stop: Close the valve and SH control.<br>• Fixed OD: set OD to a fixed value defined by parameter N145<br>• Average OD: set OD to be the average OD for the last hour.|
||||*only in delta-temp operation|
||||If a thermostatic sensor error as happened (S3 and S4) has an error.<br>• Stop: Close the valve and SH control.<br>• Fixed OD: set OD to a fixed value defined by parameter N145|
|N144|Thermostatic<br>sensor error<br>action|0-Stop<br>1- Fixed OD<br>2-Average|i  i<br>• Average:<br>◦<br>▪Cutin /cutout use average on and off time to continue cool-<br>ing.<br>◦MTR use reduced OD based average OD (70% of average OD).|

#### 6.2.1 Superheat Reference Calculation Parameters

As mentioned in the previous section, in superheat mode the controller will control the superheat to be stable and closer to the superheat reference. The Superheat reference is determined and calculated based on following different methods:

- Fixed Superheat reference

- MSS

- Load AP

- Delta Temperature Reference

###### **Fixed Superheat reference**

In this method, the EKE tries to keep the superheat at a fixed value determined by the user. SH fixed setpoint can be varied according to the need of application.

**Table 25: Fixed Su** **p erheat reference**

|**EKE**<br>**1A**<br>**1B**<br>**1C**<br>**1D**|
|---|
|**Applicable**|

**Table 26: Fixed su** **p erheat** **p arameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|R102|Operation mode|0 = SH Control|
|N021|SH reference mode|0 = Fixed Superheat|
|N107|SH fixed setpoint|The fixed superheat reference defined by the user.|
|||Safety feature to prevent the flooding of the liquid into the compressor.|
|N117|SH close Function|When the measured superheat goes bellow the SH close setpoint (parameter<br>N119)|
|||0 = Off | 1 = On, default = 1|
|N119|SH close setpoint|It is recommended to set the SH close setpoint 2k below the minimum SH.<br>Default value =2 K (recommended).|
|I082|S2 sensor configuration|-Selection of the used evaporator temperature sensor S2|
|I086|Pe transmitter configuration|-Selection of the used evaporator pressure sensor Po|

###### **Minimum Stable Superheat (MSS)**

The controller will be searching for the minimum stable superheat between an upper and lower boundary specified by the user. Then if the superheat is stable at a certain value, the controller decreases the superheat reference, if the SH gets unstable, the SH reference is raised again.

The goal of this method is to search for the lowest possible superheat that can be obtained while still maintaining a stable system.

**Table 27: Minimum Stable Su** **p erheat (MSS)**

|**EKE**<br>**1A**<br>**1B**<br>**1C**<br>**1D**<br>**Applicable**|
|---|

###### **Fi** **g ure 57: Minimum stable Su** **p erheat**

*[Figurtekst: Qo · 100 % · 40 % · 10 % · Min. SH Max. SH Superheat · Unstable region Stableregion (dry) · (wet) · Danfoss 84B1487.10]*

**Table 28: MSS** **p arameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|R102|Operation mode|0 = SH Control|
|N021|SH reference mode|2 = MSS|
|N009|SH max. value|Maximum allowed SH reference in the range.|
|N010|SH min. value|Minimum allowed SH reference in the range.|
|N018|MSS Stability|The amount of allowed fluctuation in the superheat before the reference is changed (the range at which the SH<br>is considered stable)|
|N129|T0 variant factor (Value from 0 to<br>1)|Defines how Pressure variation (From Pe) influence the SH reference.|

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N117|SH close Function|Safety feature to prevent the flooding of the liquid into the compressor. When the measured superheat goes<br>bellow the SH close setpoint (parameter N119) 0 = Off | 1 = On, default = 1|
|N119|SH close setpoint|It is recommended to set the SH close setpoint 2k below the minimum SH.<br>Default value =2 K (recommended).|
|I082|S2 sensor configuration|-Selection of the used evaporator temperature sensor S2|
|I086|Pe transmitter configuration|-Selection of the used evaporator pressure sensor Po|

###### **Load AP**

In Load ap application, SH reference follows a defined curve as shown in the diagram. This two-point curve is defined by SH max and SH min. These two values must be selected in such a way that the curve is situated between the MSS curve and the curve for average temperature difference ΔTm (temperature difference between media temperature and evaporating temperature). This makes the regulation more stable compare to MSS because it does not seek a usability.

Besides the Temperature Sensor S2 and pressure sensor Pe, in this mode a third temperature sensor is needed S3.

**Table 29: Load AP**

*[Figurtekst: EKE 1A 1B 1C 1D · Applicable]*

###### **Fi** **g ure 58: Load AP** **p arameters**

*[Figurtekst: Qo · 100 % · 90 % · 10 % · Min. SH Max. SH Superheat · Unstable region · (wet) · region (dry)Stable · Danfoss 84B1489.10]*

**Table 30: Load AP** **p arameter**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|R102|Operation mode|0 = SH Control|
|N021|SH reference mode|1 = LoadAp|
|N009|SH max. value|SH max. defines the reference for OD between 90-100% SH max.<br>must be greater than or equal to SH min.|
|N010|SH min. value|SH min defines the SH reference for OD between 0 and 10 %.<br>Note: SH min. value must be >0.5K higher than SH close value, if<br>N117=1|
|N117|SH close function|0 = Off | 1 = On, default = 1|
|N119|SH close setpoint|It is recommended to set the SH close setpoint 2k below the<br>minimum SH.<br>Default value =2 K (recommended).|
|I082|S2 sensor configuration|-Selection of the used evaporator temperature sensor S2|
|I086|Pe transmitter configuration|-Selection of the used evaporator pressure sensor Po|
|I041|S3 Temperature sensor|-Selection of the used Media temperature S3|

###### **Delta Temperature Reference**

**Table 31: Delta Tem** **p erature Reference**

|**EKE**<br>**1A**<br>**1B**<br>**1C**<br>**1D**<br>**Applicable**|
|---|

In delta temperature, the reference is calculated using evaporator pressure Po and Media temperature S3. It is based on the fact that most evaporators have a good efficiency if the SH reference is set to be 0.65 multiplied by temperature difference from inlet temperature to evaporating temperature. The temperature difference is calculated as follows **SH = Delta temp factor * (S3-T0)** .

T0: temperature corresponding to evaporator pressure Po S3: Media temperature

###### **Fi** **g ure 59: Delta Tem** **p erature Reference**

*[Figurtekst: S2 · SH · Danfoss 80G354.10]*

In this mode the response of the controller is quicker in case of load changes.

**Table 32: Delta Tem** **p erature Reference**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|R102|Operation mode|0 = SH Control|
|N021|SH reference mode|3 =Delta temp|
|N009|SH max. value|Maximum allowed SH reference in the range.|
|N010|SH min value|Minimum allowed SH reference in the range.|
||.|Note: Value must be >0.5K higher than SH close value, if N117=1|
|N116|SH f dlt t ft|Note: this value should be between 0.4 and 0.1. Lower value may flood the|
||re. ea emp acor|compressor whereas higher values will result in low efficiency|
|N117|SH close function|0 = Off | 1 = On, default = 1|
|N119|SH close setpoint|It is recommended to set the SH close setpoint 2k below the minimum SH.<br>Default value =2 K (recommended).|
|I082|S2 sensor configuration|-Selection of the used evaporator temperature sensor S2|
|I086|Pe transmitter configuration|-Selection of the used evaporator pressure sensor Po|
|I041|S3 Temperature sensor|-Selection of the used Media temperature S3|

#### 6.2.2 Temperature Control Parameters

EKE has 2 methods of controlling the superheat while considering the temperature of the incoming media (using temperature sensor S3) or based on the outgoing media (using temperature sensor S4).

The 2 methods are:

- ON/OFF thermostat.

- Modulating thermostat (MTR).

**Table 33: Tem** **p erature Control Parameters**

|**EKE**|**1A**<br>**1B**<br>**1C**<br>**1D**|
|---|---|
|**Applicable**|-|

These modes require one extra temperature sensor S3 or S4, the user can select only one sensor not both.

Superheat control with Thermostatic Mode is not available on EKE 1A.

###### **ON/OFF thermostat**

In this mode, if temperature is above the set point + differential cooling is started with maximum cooling capacity. In maximum capacity superheat is controlled to be on superheat set point. Cooling is active until the temperature is below set point. In a startup, cooling will be active if temperature is above temperature set point.

###### **Fi** **g ure 60: ON/OFF thermostat**

*[Figurtekst: S3 Pe S2 · T R T · “Warm” brine / water · Plate heat exchanger · S4 · T · EEV · “Cooled” brine / water · Expansion valve · Danfoss 80G365.10]*

Need for Defrosting During cooling is not considered. If defrosting is needed another system must ensure defrosting is done when needed.

###### **Fi** **g ure 61: ON/OFF thermostat**

*[Figurtekst: Temperature · Cutout · Differential · Cutin · Setpoint · thermostat Off On Off On Off On · Time · Valve OD · Time · Danfoss 80G300.10]*

**Table 34: ON/OFF thermostat** **p arameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|||-Uses a temperature setpoint (parameter R101), and the differential con-<br>stant(R001).|
|R014|Thermostatic Mode (1-Cutin /cutout)|-The temperature media is maintained at a level defined by the set point.|
|||-If the temperature is higher than the reference + the differential, the supper heat<br>control will start, and it stops when the temperature goes below the reference.|
|R015|Sensor|Select the used sensor S3 or S4|
|I041|S3 Temperature sensor|Only if S3 is selected in R015, Selection of the used Media temperature S3|
|I041|S4 Temperature sensor|Only if S4 is selected in R015, Selection of the used Media temperature S4|
|B101|Temperature setpoint, Deg C|Desired media temperature|
|R001|Differential|Differential constant.|
|U118|Operational Status|7 = Thermo, cutout, (read value)|

###### **Modulating thermostat (MTR)**

When the temperature is well above the MTR set point (The MTR reference is defined by temperature set point + ½ differential) cooling capacity is at maximum and superheat is controlled to be on superheat reference. When temperature is getting close to the MTR reference the cooling capacity gradually reduce so that the

temperature can be stable on the MTR reference and the superheat will be floating.

###### **Fi** **g ure 62: Modulatin** **g thermostat (MTR)**

*[Figurtekst: Temperature S3/S4 · Compressor startup · MTR start · 1/2 erential · Temperature · setpoint · Valve OD Time · Time · Danfoss 80G308.10]*

**Table 35: Modulatin** **g thermostat (MTR)** **p arameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|R014|Thermostatic Mode (2-MTR)|• Uses a temperature setpoint (parameter R101), and the differential con-<br>stant(R001).<br>• The goal is to maintain the temperature media at the level defined by the set<br>point.<br>• If the temperature is higher than the reference + the differential, the supper<br>heat control will start, and it stops when the temperature goes below the ref-<br>erence.|
|R015|Sensor|Select the used sensor S3 or S4|
|I041|S3 Temperature sensor|Only if S3 is selected in R015, Selection of the used Media temperature S3|
|I041|S4 Temperature sensor|Only if S4 is selected in R015, Selection of the used Media temperature S4|
|B101|Temperature setpoint, Deg C|Desired media temperature|
|R001|Differential|Differential constant.|
|U118|Operational Status|11= Injection MTR, (read value)|

#### 6.2.3 Offsetting Superheat, Temperature and OD Via External signal

Temperature and superheat references can be displaced in positive or negative direction using a current signal (EKE1C only), voltage signal or via Modbus.

**Table 36: Offsettin** **g Su** **p erheat, Tem** **p erature and OD Via External si** **g nal**

*[Figurtekst: EKE 1A 1B 1C 1D · Offset via External current · signal - - - · Offset via Voltage current sig‐ · nal · Offset via Bus · -]*

**Fi** **g ure 63: Offsettin** **g Su** **p erheat, Tem** **p erature and OD Via External si** **g nal**

*[Figurtekst: Offset Offset · R006 R006 · Ext. ref offset max. 5 Ext. ref offset max. 4 · R106 I036 · Ext. ref offset min Ext ref. current low · 0 10 Voltage 4 20 Current · Ext ref. voltage lowI034 Ext ref. voltage highI035 Ext. ref offset minR106 -2 Ext ref. current highI037 · Danfoss 80G354.10 Danfoss 80G356.10]*

 **NOTE:**

Offset can be done in positive and negative direction. Extra care must be taken while doing this setting.

**Table 37: Offsettin** **g references for EKE 1A**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I021|AI4 Configuration|Ext. reference|
|R106|Ext. ref offset min.|This setting determines how large the offset is when input signal is at min.|
|R006|Ext. ref offset max|This setting determines how large the offset is when input signal is at max.|
|||Define how the external reference signal is used|
|O089|Ext ref. supply|0 = V->SH: Displacement of SH reference given by External voltage signal.|
|||1 = V->Temp: Displacement of temperature given External voltage signal.|
|I034|Ext ref voltage low|Define min. reference Voltage|
|I035|Ext ref. voltage high|Define max. reference Voltage|

**Table 38: Offsettin** **g references for EKE 1B, 1D**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I021|AI4 Configuration|Ext. reference|
|R106|Ext. ref offset min.|This setting determines how large the offset is when input signal is at min.|
|R006|Ext. ref offset max|This setting determines how large the offset is when input signal is at max.|
|||Define how the external reference signal is used|
|||1 = V->SH: Displacement of SH reference given by External voltage signal.|
|O089|Ext ref. supply|3 = V->Temp: Displacement of temperature given External voltage signal.|
|||4 = Bus -> SH: Displacement of SH reference given via Modbus.|
|||6 = Bus -> T: Displacement of temperature given via Modbus|
|I034|Ext ref voltage low|Define min. reference Voltage|
|I035|Ext ref. voltage high|Define max. reference Voltage|

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I036|Ext ref. current low|Define min. reference current|
|I037|Ext ref. current high|Define max. reference current|
|X010|Bus ext. ref|Readout offset in Kelvin|

###### **Table 39: Offsettin** **g p arameters EKE 1C**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I021|AI4 Configuration|Ext. reference|
|R106|Ext. ref offset min.|This setting determines how large the offset is when input signal is at min.|
|R006|Ext. ref offset max|This setting determines how large the offset is when input signal is at max.|
|||Define how the external reference signal is used|
|||1 = V->SH: Displacement of SH reference given by External voltage signal.|
|||2 = V->Max OD: Maximum opening degree of the valve given by external voltage<br>signal|
|||3 = V->Temp: Displacement of temperature given External voltage signal.|
|O010|Ext ref. supply|4 = Bus -> SH: Displacement of SH reference given via Modbus.<br>5 = Bus->Max OD: Maximum opening degree of the valve given via Modbus.|
|||6 = Bus -> T: Displacement of temperature given via Modbus|
|||7 = mA->SH: Displacement of SH reference given by External current signal.|
|||8= Bus->Max OD: Maximum opening degree of the valve given by External cur-<br>rent signal.|
|||9 = mA->Temp: Displacement of temperature given External current signal.|
|I034|Ext ref voltage low|Define min. reference Voltage|
|I035|Ext ref. voltage high|Define max. reference Voltage|
|I036|Ext ref. current low|Define min. reference current|
|I037|Ext ref. current high|Define max. reference current|
|X010|Bus ext. ref|Readout offset in Kelvin|

- SH reference is not allowed to offset the signal below SH min.

- Only analog input AI4 can be set as an analog external reference for displacing references

- EKE1D receives reference parameter via wired CANBus, while EKE 1C, EKE 1B receive it via Modbus.

#### 6.2.4 Compressor feed Forward function

When a compressor speed changes, system dynamics change correspondingly. Hence, Compressor speed feed forward function changes the PI parameter values according to the actual compressor speed, which means the reactivity of the controller is changed.

For example, when the speed of the compressor is low, this feature increases the integration time which leads to a slower response of the PI controller.

To use this feature bus communication is needed and the master controller must send a feed-back about the compressor speed to the EKE controller.

**Table 40: Com** **p ressor feedforward function**

|**EKE**|**1A**<br>**1B**<br>**1C**<br>**1D**|
|---|---|
|**Applicable**|-|

This function is basically used in one-to-one systems and requires a Modbus (Or CANBus in EKE 1D) to feed the compressor speed. This functionality may not be used in multi-evaporator system.

###### **Fi** **g ure 64: Com** **p ressor feedforward function**

*[Figurtekst: Compressor speed signal via MODbus · Master · control · TT P · S2 · EEV · Danfoss 80G8305.10]*

**Table 41: Com** **p ressor feed Forward**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N135|Comp. speed feed forward function|0 = Off | 1 = On, default Off|
|R100|Compressor Capacity|compressor capacity value in percentage via Modbus|
|N136|FF low capacity turning point|The point where SH control is starting to slow. Below this speed<br>superheat control is slower|
|N137|FF maximum factor for Tn turning|Define max. reference current|

#### **6.3 Other features and modes**

#### 6.3.1 Startup and Defrost Modes

A Startup mode allows the valve to open faster on start-up to avoid any unwanted low-pressure situation. EKE 1x controllers implements 3 different modes for startup, and one sequence for startup.

**Table 42: Startu** **p and Defrost Modes**

|**EKE**<br>**1A**<br>**1B**<br>**1C**<br>**1D**<br>**Applicable**|
|---|

###### **P-control**

The controller is programmed for auto proportional control that will quickly Change the opening degree based on the superheat of the system. The proportional control is active during the Minimum start time set by the user, and until the Super heat crosses the reference.

If SH didn’t cross the Superheat reference after the **minimum stop time** (N104), the Proportional control will stop after the **start time** (N105), set by the user.

###### **Fi** **g ure 65:** **p ro** **p ortional control startu** **p mode**

*[Figurtekst: SH · Min start · Start time · time · The Pctrl is active in · the min start time and · until SH cross the · reference · SH ref · SH crosses the SH · reference after the “min · start time” = > the · proportional control id · Danfoss  80G361.10 disabled after that]*

**Table 43: The** **p arameters to setu** **p this mode is illustrated in the followin** **g table:**

|**Paramete**|**r Function**|**Description**|
|---|---|---|
|N102|Startup<br>mode|0 = Prop. Ctrl|
|N104|Minimum<br>startup<br>time|Min value: 1 second | Max value: 240 seconds<br>If the SH crosses the reference between minimum startup time, and startup time the Proportional control is disabled.|
|N105|Startup<br>time|Min value: 1 second | Max value: 600 seconds<br>After startup time the Proportional control is disabled even if the SH didn’t cross the reference.|
|N017|Startup OD|Starting OD degree of the valve.<br>**WARNING:**<br>This parameter has lower priority then limiters (LOP, SH close, MOP.)|

###### **Start OD with protection**

This function will provide a start opening degree during a fixed start time. If the limiters such as LOP has been activated, the valve will do the auto adjustment-based set limitations.

###### **Fi** **g ure 66: Fixed OD with** **p rotection**

*[Figurtekst: Forced opening  of valve · Auto control · OD% OD set by limiters · (LOP, MOP, SH close..) · Valve OD% · Reg. OD% · Startup OD% · (Minimum) · Forced OD% Normal Reg. · Time for start · Start Start up time  1 ) · Danfoss 80G8237.01]*

**Table 44: Start OD with** **p rotection**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N102|Startup<br>mode|1 = Minimum OD with protection|
|N105|Startup<br>time|Min value: 1 second | Max value: 600 seconds<br>After startup time the Startup OD is Disabled, and controller will switch to the set control mode.|
|N017|Startup OD|Starting OD degree of the valve.<br>**WARNING:**<br>This parameter has lower priority then limiters (LOP, SH close, MOP…)|

###### **Start OD without protection**

This function will provide a start opening degree during a set time. This function is not affected by the limiters such as LOP.

###### **Fi** **g ure 67: Start OD without** **p rotection**

*[Figurtekst: Forced opening  of valve · Auto control · OD% · Valve OD% · Startup OD% · Forced OD% Normal Reg. · Time for start · Start Start up time · Danfoss 80G8235.01]*

**Table 45: Start OD without** **p rotection**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N102|Startup mode|2 = Minimum OD without protection|
|N105|Startup time|Min value: 1 second | Max value: 600 seconds<br>After startup time the Startup OD is Disabled, and controller will switch to the set control mode.|
|N017|Startup OD|Starting OD degree of the valve.|

###### **Defrost sequence**

Defrost Sequence must be initiated by the master controller. In a standalone configuration, the defrost mode is not possible.

To initiate defrost, the system mode is changed from Heat pump to A/C, hereby the outdoor unit will act as a condenser and the hot discharge gas from the compressor will defrost the coil. In some system electrical heaters are used instead of reversible system but defrost sequence can still be used.

###### **Fi** **g ure 68: Defrost se** **q uence**

*[Figurtekst: Injection  Defrost  Defrost end  Startup · OD % Defrost end · Defrost start signal received · signal received · Defrost OD · Defrost · end OD · 0 · time · Defrost start time Defrost end Defrost end · closed time OD time · Danfoss 80G360.10]*

The user sets the Defrost OD, the Defrost end OD, defrost start and end time (see table below).

The defrost start/end commands are received from one of the following options:

1. Modbus register (nonvolatile memory) – default OFF at power-up

2. DI’s for use as defrost start/stop. Only one DI can be assigned for defrost start/stop. Start is defined as a transition from off to on, a transition from on to off is a stop signal.

**Table 46: Defrost Se** **q uence** **p arameters**

|**Parameter**|**Function**|**Description**|**Default**|
|---|---|---|---|
|||The defrost sequence starts by closing<br>the valve, which is kept closed until the<br>‘D101 Defrost start low pressure limit’ is<br>reached or D102 ‘Defrost start time’ is||
|D101|Defrost start low pressure limit|exceeded.<br>**WARNING:**<br>This parameter is valid only if the de-<br>frost start time >0|1.0 brag|
|D102|Defrost start time|The defrost sequence starts by closing<br>the valve, which is kept closed until the<br>‘D102 ‘Defrost start time’ is exceeded or<br>‘D101 Defrost start low pressure limit’ is<br>reached|0 s|
|D100|Defrost OD|Sets the valve opening degree after the<br>Defrost start time is passed.|0%|
|D104|Defrost end closed time|After the defrost stop signal, the valve<br>closes and will open again after ‘Defrost<br>end closed time’ is exceeded|1s|
|D103|Defrost end OD time|End of the defrost, start of the startup<br>mode.|1s|
|D105|Defrost end OD|Sets the valve opening degree after De-<br>frost end closed time.|50%|

#### 6.3.2 Protection features

EKE 1x series has protection features that prevents the system from operating under bad conditions, these protection features are:

- Fail safe operation

- Superheat close

- LOP (Low operating pressure)

- MOP (Maximum operating pressure)

- HCTP (High condensing temperature protection)

- Min. S4 (Minimum S4 temperature)

###### **Fi** **g ure 69: Protection features (limiters)**

*[Figurtekst: HCTP · Superheat · close · MOP · LOP · Superheat · reference · Enthalpy (H) · Danfoss 80G8227.01 · Pressure (P)]*

###### **Fail Safe Operation**

In the case of sensor error, the EEV controller will go into an emergency mode (“safe mode”). where the valve opening degree is defined by desired OD scheme as described below

User can read the failure status via [U118 Operation status].

EKE 1x implements two Failsafe mode:

- SH control Failsafe mode

- Thermostat Failsafe mode

###### **Table 47: SH control Failsafe mode**

|**SH control Failsafe mode:**|**Description**|
|---|---|
|SH control needs Pe and S2 signal. so, if one of these<br>signal fails, SH control based on the actual superheat<br>is not possible.|**Stop**<br>User can via parameter [**N143]**SH control sensor error action, under control advanced. configure the relevant<br>option<br>valve forced closed and SH control (default)|
||**Fixed OD**<br>valve at fixed position (Fail safe OD), this keeps the refrigeration unit running|
||**Use average OD**<br>(calculated as an average of the last hour) to set a reduced OD which will be fixed dur-|
||ing error period. This keeps the refrigeration unit running|

###### **Table 48: SH control Failsafe mode** **p arameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N143|SH control sensor error|0 = Stop | 1 = Fixed OD | 2 = Average OD|
|N145 [only if N143= 1]|Fixed OD during<br>emergency cooling|define fixed OD % during Emergency cooling|
|N138 [only if N144= 2]|Average OD|Calculated When superheat control/ Temperature control is active and stored in<br>EEPROM. Its value is updated every 3 hours. Reset to factory will not delete the<br>calculated average values. Used in average OD|

###### **Table 49: Thermostat Failsafe mode**

|**Thermostat Failsafe mode**|**Description**|
|---|---|
|Thermostat sensor error.<br>Thermostat operation needs the signal selected in [R015 Sensor select] to oper-<br>ate the thermostat function, if this signal fails operation based on actual tempera-<br>ture is not possible|**Stop**<br>User can via parameter**[N144]**Thermostat sensor error action] configure the rel-<br>evant option.<br>valve forced closed, SH control and Temperature control (default)|
||**Fixed OD**<br>valve at fixed position (Fail safe OD). This Keeps the refrigeration|
||running|
||**Use Average OD**<br>Cutin /cutout use average on and off time to continue cool-|
||ing<br>MTR use reduced OD based average OD (70% of average<br>OD).|

###### **Table 50: Thermostat Failsafe mode** **p arameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N144|Thermostat sensor error action|0 = Stop | 1 = Fixed OD | 2 = Average OD|
|N145 [only if N144= 1]|Fixed OD during emergency cooling|Define fixed OD % during Emergency cooling|
|N138 [only if N144= 2]|Average OD|Calculated When superheat control/ Temperature control is ac-<br>tive and stored in EEPROM. Its value is updated every 3 hours.<br>Reset to factory will not delete the calculated average values.<br>Used in average OD|

###### **Superheat close**

SH close ensures that superheat is on or above ‘SH close set point to avoid liquid getting back to the compressor. If the media inlet temperature drops or if compressor goes down in capacity, the superheat may drop below the SH close setpoint, then the flow in the expansion valve is reduced to bring superheat up to SH close setpoint as shown in the figure below.

###### **Fi** **g ure 70: SH close o** **p eration**

*[Figurtekst: Superheat Auto SH control reducing OD fast SH close is active   Auto SH control · to get SH back to · reference · SH Ref Superheat · OD · SH close · setpoint · Compressor capacity · Time · Danfoss 80G357.10]*

**Table 51: Su** **p erheat close Parameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N117|SH close function|0 = Off | 1 = On, default Valve = On|
|N119|SH close setpoint|Default value =2 K|

###### **Lowest Operating Pressure (LOP)**

Lowest Operating Pressure (LOP) will make sure that the evaporating pressure (Pe) is kept above LOP set point, this will prevent the compressor from stopping due to low suction pressure. If the pressure comes below this limit the controller will quickly open the valve.

###### **Fi** **g ure 71: Lowest O** **p eratin** **g**

*[Figurtekst: Compressor · start · Valve is opening to · avoid Te going lower · Outdoor · temp · Te evaporator temperature · OD · Lop setpoin t · Superheat · Danfoss 80G358.10]*

**Table 52: Lowest O** **p eratin** **g Pressure (LOP) Parameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N140|LOP function|0 = Off | 1 = On, default Valve = Off|
|N141|LOP setpoint °C|Lowest Operating Pressure setpoint.<br>Setpoint unit is saturated temperature in evaporator|
|N142|LOP priority mode|In case of conflict between low pressure and SH close, LOP function can be set to<br>override SH close actions. (Could be needed for startup in low ambient tempera-<br>tures)<br>On: LOP can override low superheat<br>0 = Off | 1 = On, default= Of<br>**WARNING:**|
|||As default, controller will not be allowed to open the valve when the superheat is<br>low. If such feature is needed for a short time, parameter” N142 LOP priority<br>mode” can be set to ON. This will allow LOP to have higher priority than bringing<br>the superheat out of low superheat for the time defined in” N131 LOP max. time”.|
|||**WARNING:**<br>A specialCare should be taking that compressor can handle this condition.|
|N131|LOP max. time|Maximum time for LOP to override SH close|

###### **Maximum Operating Pressure (MOP)**

Maximum Operating Pressure (MOP) will make sure that the evaporating pressure (P0) is kept below the MOP setpoint set by the user. This is achieved by lowering the flow in the expansion valve. When this mode is active this Super heat reference will be higher, the controller will switch back to superheat control once the pressure Po is kept on the MOP setpoint.This feature is helpful especially during startup During startup and pulldown to avoid overload of the compressor.

###### **Fi** **g ure 72: Maximum O** **p eratin** **g Pressure (MOP)**

*[Figurtekst: Temperature · MOP · setpoint · Room Temperature · Te evaporator · temperature · Room temperature · re · Danfoss  80G360.10]*

**Table 53: Maximum O** **p eratin** **g Pressure (MOP) Parameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N130|MOP function|0 = Off | 1 = On, default value = Of|
|N011|MOP setpoint|Setpoint unit is saturated temperature in evaporator. If the suc-<br>tion pressure reaches the set MOP limit, the valve will close faster<br>irrespective of superheat.|

###### **High Condensing Temperature Protection**

This protection mode reduces the load on the condenser in case the high condensing temperature by reducing the OD of the valve. The high condensing temperature is defined by the user through the parameter N134 ‘High cond. temp. protection setpoint’, this value is converted from pressure input.

**Fi** **g ure 73: Hi** **g h condensin** **g tem** **p erature** **p rotection**

*[Figurtekst: Pc · C · E · S2 Pe · EEV · Danfoss 80G8230.01]*

###### **Fi** **g ure 74: Hi** **g h condensin** **g tem** **p erature** **p rotection**

*[Figurtekst: Tc condenser · temperature · HCTP setpoint · If condenser is above HCTP · setpoint the massflow is · reduced giving less load on · condenser · During high condenser · temperature the SH will not · follow SH reference · SH · SH ref · OD · Danfoss  80G359.10]*

 **NOTE:**

HCTP feature requires mounting pressure transducer Pc at compressor discharge line or getting its value via Bus

**Table 54: Hi** **g h condensin** **g tem** **p erature** **p rotection Parameters**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N133|High cond. temp. protection function|0 = Off | 1 = ON|
|N134|High cond. temp. protection setpoint (converted from pressure|High condensing temperature protection setpoint unit is satura-|
||value from sensor Pc).|ted temperature in condenser.|

###### **Minimum S4/leaving media (freeze protection)**

This protection modes keeps the temperature of leaving media out of the evaporator (given by temperature sensor S4) on or above of minimum temperature set by the user. This is achieved by lowering the flow in the expansion valve. When this mode is active this Super heat reference will be higher, the controller will switch back to superheat control once the Temperature of leaving media goes above S4 min

###### **Fi** **g ure 75: Minimum S4/leavin** **g media**

*[Figurtekst: S3 p0 S2 · T R T · °C · “Warm” brine / water · S3 · Plate heat · exchanger · S4 · S4 · T EEV S4 minS4 min · “Cooled” brine / water Time · Electric expansion valve · Danfoss 80G8232.01 · Danfoss 80G365.10]*

 **NOTE:**

An undershoot below the Min S4 is possible, so a frost protection is still needed to secure that the compressor is stopped before the braze plate heater is destroyed by ice.

**Table 55: Minimum S4/leavin** **g media** **p arameter table**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|N126|Min. S4 mode|0 = Off | 1 = ON|
|N127|Min. S4 setpoint|Minimum S4 (media outlet) protection setpoint|

##### **Priority of Protection features:**

To overcome conflicts between different limiters, a priority function is implemented as follows:

1. Superheat close (it is always important to avoid liquid back to the compressor)

2. LOP (Low operating pressure) 3. HCTP (High condensing temperature protection)

4. Min. S4 (Minimum S4 temperature)

5. MOP (Maximum operating pressure)

As an example, if the pressure is low and at the same time the superheat is low. LOP control would like to open the valve to raise the pressure. but SH close will decrease the flow to regain a safe superheat. In this case the LOP demand is overruled by SH close. So, in the end if the conflict still is active the mechanical low-pressure switch will need stop the compressor.

#### 6.3.3 Manual Mode

In the manual mode, the user can select actions based on signals from digital inputs DI2/DI3. In the manual mode we can use 4 different options:

1. Manual OD from preset parameter via DI

2. Manual control of Relay

3. Manual control Valve

4. Manual Homing

 **NOTE:**

Too often use of Manual Homing could wear out the valve. For normal operation use overdriving feature.

Manual OD When DI 2 is configured as Preset OD, the valve OD will be positioned as defined by valve OD parameter [I078 - Preset OD].

**Table 56: Manual OD**

|**Digital input**|**O022 DI2 configuration**|**2 = Preset OD**|
|---|---|---|
||O037 DI3 configuration (only in<br>EKE 1A)|2 = Preset OD|
|Manual Preset via DI|078 Preset OD|desired Valve OD %|

When manual mode becomes active, the state of alarm output will remain the same and be transferred to the parameter(s) for Manual relay DO1. When manual mode becomes inactive the actual state of Manual relay DO1 will be the starting point for the next mode.

**Table 57: Manual control of Rela** **y :**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|O018|Manual mode|1 = On|
|B101|Manual mode timeout|time in sec. When timed out the parameter [O018 - Manual Mode] will be set to of|
|B103|Manual relay DO1|0 = Off | 1 = ON|

When DI2 /DI 3 is configured as Preset OD, the valve OD will be positioned as defined by valve OD parameter [I078 - Preset OD].

**Table 58: Manual Control Valve:**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|O018|Manual mode|1 = On|
|B101|Manual mode timeout|time in sec. When timed out the parameter [O018 - Manual Mode] will be set to Off|
|O045|Manual OD|Set desired OD in Percentage %|

Used to calibrate the valve at Zero OD %. When the user set the manual homing, a full closing operation will be performed (same as initial closing). After the operation is performed the manual homing parameter [B104 - Manual Homing] will be set back to off and the parameter for [O045 Manual OD] will be set to 0%. When manual mode becomes inactive the actual OD will be the starting point for automatic control

**Table 59: Manual Homin** **g :**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|O018|Manual mode|1 = On|
|B101|Manual mode timeout|time in sec. When timed out the parameter [O018 - Manual Mode] will be set to Off|
|O045|Manual OD|Set desired OD in Percentage %|

###### **Fi** **g ure 76: Switchin** **g between Auto and manual mode**

*[Figurtekst: Auto control Manual mode  ON Auto control · Time · Valve OD · Danfoss 80G301.10]*

#### 6.3.4 Valve configuration

**Table 60: Valve Confi** **g uration**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I067|Valve Configuration|Danfoss stepper motor are easily selected from Valve configuration list. On selecting the valve, the<br>controller will automatically load pre-defined default values. The user is not required to set other<br>stepper motor parameters for a selected valve from the valve configuration list.<br>**NOTE:**<br>I028 parameter (Valve drive current) needs to be adjusted if the chosen cable length is between<br>15 and 30m, refer to the installation section|
|||If a valve from other manufacturers is used, such valve can be defined as|
|I067|User Defined valve|1.<br>2.<br>Set I067 to ‘’User defined Valve’’<br>Enter the Valve parameters (Parameters described below).|

**Table 61: Parameters Non-Danfoss valves: for Danfoss vales these parameters are preconfigured, if the user decides to use a valve from a different manufacturer, then these** **p arameters must be** **p rovided b** **y the user.**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I027|Valve Motor Type|Define a type of motor used in the stepper valve (Unipolar/Bipolar).|
|I028|Valve drive current|Setting the Peak current requirement of the motor in mA.<br>**NOTE:**<br>Please be aware that this value must be set in a Peak value. Some valve manufacturers are<br>using RMS current (1mA RMS = 1.41mA Peak).|
|||Defines which position step the valve motor should stop, while changing the opening degree<br>of the valve.<br>Choose between:|
|I029|Valve step positioning|• Full-step<br>• Half-step<br>• Auto - controller will automatically choose based on the valve type right arrow Half step if<br>Unipolar valve |Full step whereas Bipolar valves|
|I030|Valve Total Steps|The number of steps that correspond to a valve position of 100%. The total no of steps will<br>vary according to the selected Valve motor type. For example: ETS 6 has total number of 480<br>half steps on driving with half phase excitation whereas only 240 full steps on driving with<br>Full phase excitation.|
|||The desired valve drive rate in steps per second.<br>**NOTE:**|
|I031|Valve speed|Higher valve speed will produce a lower torque. If the valve is used in system having high<br>differential pressure, it is better to operate the valve with lower step rate|
|||Valve initial speed as % of the valve speed (I031). The parameter Is used to avoid high acceler-<br>ation rate of the stepper motor.|
|I032|Valve start speed|**NOTE:**<br>Make sure to select a start speed which is recommended for the used valve.|
|I061|Valve emergency speed|During power failure conditions, the valve can be driven at higher speed when required to<br>close faster. To run this feature, it is required to connect EKE with backup battery.|
|||To control the torque in the start and stop sequence, the unit is % of the normal valve driving<br>current I028 (I031). Note that the torque of the motor is directly proportional to the supplied|
|I062|Valve acceleration current|current<br>**NOTE:**<br>Make sure not to exceed the rated current of the valve motor, because this might damage it.|
|I063|Valve Acceleration Time|Defines the time of the acceleration/ deacceleration in the start/stop of the motor.|

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I077|Holding Current|For some valves, this represents the percent of the programmed Max Phase Current that<br>should be applied to each phase of the stepper motor to maintain the valve at its last pro-<br>grammed position. Not all valve designs require a holding current, make sure to check this<br>with your valve manufacturer|
|I064|Valve step Mode|Stepper motor can be driven with various step excitation method, which depends valve re-<br>quirements as well as operating conditions of an application.<br>The user can choose<br>• Full stepping 1/1<br>• Half stepping 1/2<br>• Micro-stepping (1/4, 1/8, 1/16)<br>**NOTE:**<br>For half and micro stepping, the risk of step loss is higher because the torque provided is low-<br>er|
|||Danfoss recommends using 1/8 stepping mode as this provides a good balance between tor-<br>que, speed, and smooth operation.|
|I065|Valve duty cycle|Defines the valve motion and stop time in a window of 60 seconds.|
|I070|Start Backlash|The parameter defines the operation of the start backlash function. The valve will normally<br>open from this point onwards.|
|I071|Start backslash|The number of steps needed to correct for mechanical hysteresis when a reduction gear is<br>part of the valve design.|
|I072|Overdrive|The extra steps taken to secure the closure of the valve.it is defined as a percentage of the full<br>opening.|
|I076|Valve Excitation Time After Stop|The time that the drive current is applied after the motor has stopped before going to hold-<br>ing current. This will make sure that the valve has achieved the final position before going to<br>holding current.|

**Table 62: Common Valve** **p arameters (For Danfoss/Non-Danfoss valves)**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|I069|Valve OD During Stop|For some application, it is required that the valve remains open after the control-<br>ler is off. This parameter defines that OD in %.<br>**NOTE:**<br>This parameter requires connecting a Battery Backup|
|I073|Overdrive Enable OD|The Overdrive happens only after Exceeding Override Enable OD.|
|||To limit how frequent overdrive can performed the parameter [I074 - Overdrive<br>block time] defines the minimum time between 2 overdrive actions. The default<br>value is 10 minutes<br>Actual opening degree|
|I074|Overdrive Block time|Danfoss<br>80G8350.10<br>No overdrive<br>No overdrive<br>Overdrive<br>Overdrive<br>1073<br>Override<br>Enabled OD<br>1074 - Override Block Time|
|I078|Preset OD|The DI can be used to force the valve to go to this opening degree.|
|I068|Valve neutral Zone|EKE controller has a complex algorithm implemented to handle oscillation issues<br>related to output valve OD by defining some neutral zone. In neutral zone, the<br>valve will not move until it overcomes the definite variation in the valve opening<br>degree.<br>The benefit of using such techniques will not affect the performance of the sys-<br>tem but will reduce the problem related with the fluctuating signal, step loss and<br>hysteresis in the valve.|

######  **NOTE:**

**Failsafe Position:** During failsafe mode of operation (e.g., SH control sensor error or Thermostat sensor error) the valve position can be set to full close, fixed opening degree or average calculated OD. For detail check section Failsafe operation and parameter list under section control advance sub section Diagnostic SH and Emergency cooling.

#### 6.3.5 Adding user Defined Refrigerant

Most of the used common Refrigerants have been defined as a pre selectable profile under “Refrigerant list para O030”. for unlisted refrigerants, user defined refrigerants can be used.

**Table 63: Addin** **g user defined refri** **g erants**

|**Parameter**|**Function**|**Description**|
|---|---|---|
|O030|Refrigerant|13 = R User. to select user defined refrigerant|
|O100|Antoine Constant A1|Antoine Constant A1 for the user defined refrigerant. Available only if O030 is on R user option.|
|O101|Antoine Constant A2|Antoine Constant A2 for the user defined refrigerant. Available only if O030 is on R user option.|
|O102|Antoine Constant A3|Antoine Constant A3 for the user defined refrigerant. Available only if O030 is on R user option.|

#### **7 Parameter List**

**Table 64: Parameter list**

||**Label**|**Parameter**<br>**name**|**Vari**|**ants**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Reference**|||||||||||||
|Refrigeration<br>on/of|R012|Main switch|||0|1|0||3001|550B|B8|0 = Off | 1 = On|
||R102|Operation<br>mode|||0|1|0||3002|550B|B9|0 = SH control | 1 = Valve<br>driver|
|Application con-<br>figuration|R100|Compressor<br>capacity|||0|100|0|%|4001||||
||R015|Sensor|1B, 1|C, 1D|0|1|0||3004|550B|BB|0 = S3 | 1 = S4|
||R101|Temperature<br>setpoint|||-70|70|3|°C|3006|550B|BD||
||R001|Differential|||0.1|10|2|K|3007|550B|BE||
|Temperature<br>control|R014|Thermostat-<br>ic mode|1B, 1|C, 1D|0|2|0||3005|550B|BC|0 = Not Used | 1 = CutIn/<br>CutOut | 2 = MTR|
||N100|MTR Tn|||20|3600|1800||3015|550B|C6||
||N101|MTR Kp|||0.2|20|3||3016|550B|C7||
|External refer-<br>|R006|External ref-<br>erence off-<br>set max.|||-50|50|0|K|3008|550B|BF||
|ence signal|R106|External ref-<br>erence off-<br>set min.|||-50|50|0|K|3009|550B|C0||
||R009|S2 Correc-<br>tion|||-10|10|0|K|3010|550B|C1||
||R010|S3 Correc-<br>tion|1B, 1|C, 1D|-10|10|0|K|3011|550B|C2||
|Sensor/transmit-<br>ter correction|R105|S4 Correc-<br>tion|1B, 1|C, 1D|-10|10|0|K|3012|550B|C3||
||R107|Pe Correc-<br>tion|||-5|5|0|barg|3013|550B|C4||
||R108|Pc Correc-<br>tion|||-5|5|0|barg|3014|550B|C5||
|**Valve configura**|**ition**||||||||||||
||I027|Valve motor<br>type|||0|1|0||3133|550C|3C|0 = Unipolar | 1 = Bipolar|
||I028|Valve drive<br>current|||10|1000|10|mA|3134|550C|3D||
||I029|Valve step<br>positioning|||0|2|0||3135|550C|3E|0 = Fullstep | 1 = Half-<br>step | 2 = Auto|
||I030|Valve total<br>steps|||1|8000|1|stp|3136|550C|3F||
||I031|Valve speed|||10|400|10|PPS|3137|550C|40||
||I032|Valve start<br>speed|||1|100|20|%|3138|550C|41||
||I061|Valve emen-<br>gency speed|||50|200|100|%|3139|550C|42||
||I062|Valve accel-<br>eration cur-<br>rent|||100|150|100|%|3140|550C|43||
||I063|Valve accel-<br>eration time|||10|150|10|ms|3141|550C|44||
||I064|Valve step<br>mode|||0|4|3||3143|550C|46|0 = Full | 1 = Half | 2 =<br>1/4 | 3 = 1/8 | 4 = 1/16|
||I065|Valve duty<br>cycle|||5|100|100|%|3144|550C|47||
||N032|Maximum<br>OD|||0|100|%||3146|550C|49||
||I066|Minimum<br>OD|||0||0|%|3145|550C|48||

|**Label**|**Parameter**<br>**name**|**Varia**|**nts**<br>**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|
|I067|Valve con-<br>figuration||0|32|0||3132|550C|3B|0 = no valve | 1 = User-<br>Def | 2 = ETS 12C | 3 =<br>ETS 24C | 4 = ETS 25C | 5<br>= ETS 50C | 6 = ETS 100C<br>| 7 = ETS 6 | 8 = ETS 12.5 |<br>9 = ETS 25 | 10 = ETS 50 |<br>11 = ETS 100 | 12 = ETS<br>250 | 13 = ETS 400 | 14 =<br>KVS 2C | 15 = KVS 3C | 16<br>= KVS 5C | 17 = KVS 15 |<br>18 = KVS 42 | 19 = CCMT<br>0 | 20 = CCMT 1 | 21 =<br>CCMT 2 | 22 = CCMT 4 |<br>23 = CCMT 8 | 24 = CCMT<br>16 | 25 = CCMT 24 | 26 =<br>CCMT 30 | 27 = CCMT 42<br>| 28 = CCM 10 | 29 = CCM<br>20 | 30 = CCM 30 | 31 =<br>CCM 40 | 32 = CTR 20|
|I068|Valve neu-<br>tral zone||0|5|0.5|%|3156|550C|53||
|I069|Valve OD<br>during stop||0|100|0|%|3147|550C|4A||
|I070|Start back-<br>lash||0|50|0|%|3148|550C|4B||
|I071|Compensa-<br>tion back-<br>lash||0|10|0|%|3149|550C|4C||
|I072|Overdrive||0|20|4|%|3150|550C|4D||
|I073|Overdrive<br>enable OD||0|100|0|%|3151|550C|4E||
|I074|Overdrive<br>block time||0|1440|10|min|3152|550C|4F||
|I076|Valve excita-<br>tion time af-<br>ter stop||0|1000|10|ms|3154|550C|51||
|I077|Valve hold-<br>ing current||0|100|0|%|3142|550C|45||
|I078<br>**IO configuration**|Preset OD||0|100|50|%|3155|550C|52||
|I020|AI1 configu-<br>ration|1B, 1|C, 1D<br>0|2|0||3098|550C|19|0 = Not Used | 1 = S3 | 2<br>= S4|
|I021|AI4 configu-<br>ration||0|2|0||3099|550C|1A|0 = Not Used | 1 = ExtRef<br>| 2 = pc|
|I022|AI5 configu-<br>ration|1C|0|2|0||3100|550C|1B|0 = Not Used | 1 = S3 | 2<br>= S4|
|I080|AI4 configu-<br>ration||0|1|0||3260|550C|BB|0 = Not Used | 1 = ExtRef|
|O013|DO1 config-<br>uration||0|2|0||3104|550C|1F|0 = Alarm | 1 = LLSV | 2 =<br>Max cap|
|O003|DI1 configu-<br>ration|1A|0|1|0|||||0 = Not Used | 1 = Main<br>Switch|
|O002|DI1 configu-<br>ration|1B, 1|C, 1D<br>0|1|1||3101|550C|1C|0 = Bus->Start/Stop | 1 =<br>Main Switch|
|O022|DI2 configu-<br>ration||0|4|0||3102|550C|1D|0 = Not Used | 1 = De-<br>frost Start | 2 = Preset<br>OD | 3 = Heat/Cool | 4 =<br>PWR Backup|
|O037<br>**Sensor configuration**|DI3 configu-<br>ration|1A|0|4|0|||||0 = Not Used | 1 = De-<br>frost Start | 2 = Preset<br>OD | 3 = Heat/Cool | 4 =<br>PWR Backup|

||**Label**|**Parameter**<br>**name**|**Variants**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Sub**<br>**index**|**‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|
||I040|S2 sensor<br>configura-<br>tion|1C|0|6|0||3105|550C|20|0 = Not defined | 1 = EKS<br>221 | 2 = ACCPBT<br>NTC10K | 3 = MBT 153<br>10K | 4 = 112CP | 5 = Bus<br>Shared | 6 = AKS|
||I041|S3 sensor<br>configura-<br>tion|1C|0|6|0||3106|550C|21|0 = Not defined | 1 = EKS<br>221 | 2 = ACCPBT<br>NTC10K | 3 = MBT 153<br>10K | 4 = 112CP | 5 = Bus<br>Shared | 6 = AKS|
|||S4 sensor|||||||||0 = Not defined | 1 = EKS<br>221 | 2 = ACCPBT|
||I042|configura-<br>tion|1C|0|6|0||3107|550C|22|NTC10K | 3 = MBT 153<br>10K | 4 = 112CP | 5 = Bus<br>Shared | 6 = AKS|
||||||||||||0 = Not defined | 1 = EKS|
|Temperature||S2 sensor|||||||||221 | 2 = ACCPBT|
|sensor type|I081|configura-<br>tion|1B, 1D|0|5|0||3266|550C|C1|NTC10K | 3 = MBT 153<br>10K | 4 = 112CP | 5 = Bus<br>Shared|
||I082|S2 sensor<br>configura-<br>tion|1A|0|4|0|||||0 = Not defined | 1 = EKS<br>221 | 2 = ACCPBT<br>NTC10K | 3 = MBT 153<br>10K | 4 = 112CP|
|||S3 sensor|||||||||0 = Not defined | 1 = EKS<br>221 | 2 = ACCPBT|
||I083|configura-<br>tion|1B, 1D|0|5|0||3264|550C|BF|NTC10K | 3 = MBT 153<br>10K | 4 = 112CP | 5 = Bus<br>Shared|
||I084|S4 sensor<br>configura-<br>tion|1B, 1D|0|5|0||3262|550C|BD|0 = Not defined | 1 = EKS<br>221 | 2 = ACCPBT<br>NTC10K | 3 = MBT 153<br>10K | 4 = 112CP | 5 = Bus<br>Shared|

||**Label**|**Parameter**<br>**name**|**Variants**|**Min**|**Max**|**Defaul**|**t**<br>**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|
||I038|Pc current<br>low|1C|0|10|4|mA|3122|550C|31||
||I039|Pc current<br>high|1C||20|20|mA|3123|550C|32||
||I043|Pe transmit-<br>ter configu-<br>ration|1C|0|14|0||3108|550C|23|0 = Not defined | 1 = AKS<br>32R | 2 = ACCPBP Ratio |<br>3 = 112CP | 4 = OEM Ra-<br>tio | 5 = NSK | 6 = AKS 32<br>1-5V | 7 = OEM Voltage |<br>8 = Bus shared | 9 = AKS<br>32 1-6V | 10 = AKS 32<br>0-10V | 11 = AKS 33 | 12<br>= XSK | 13 = ACCPBP<br>Current | 14 = OEM Cur-<br>rent|
||I044|Pc transmit-<br>ter configu-<br>ration|1C|0|14|0||3117|550C|2C|0 = Not defined | 1 = AKS<br>32R | 2 = ACCPBP Ratio |<br>3 = 112CP | 4 = OEM Ra-<br>tio | 5 = NSK | 6 = AKS 32<br>1-5V | 7 = OEM Voltage |<br>8 = Bus shared | 9 = AKS<br>32 1-6V | 10 = AKS 32<br>0-10V | 11 = AKS 33 | 12<br>= XSK | 13 = ACCPBP<br>Current | 14 = OEM Cur-<br>rent|
||I045|Pe ratio. low||3|97|10|%|3109|550C|24||
||I046|Pe ratio high||3|97|90|%|3110|550C|25||
||I047|Pe voltage<br>low|1C|0|10|0|V|3111|550C|26||
||I048|Pe voltage<br>high|1C|0|10|10|V|3112|550C|27||
||I049|Pe current<br>low|1C|0|10|4|mA|3113|550C|28||
|Pe and Pc Pres-<br>sure Transmitter|I050|Pe current<br>high|1C|0|20|20|mA|3114|550C|29||
||I051|Pc transmit-<br>ter configu-<br>ration|1B, 1D|0|8|0||3308|550C|EB|0 = Not defined | 1 =<br>8=Bus shared|
||I023|Pc ratio. low|1C|3|1|3|%|3118|550C|2D||
||I024|Pc ratio high|1C|3|97|97|%|3119|550C|2E||
||I025|Pc voltage<br>low|1C|0|10|0|V|3120|550C|2F||
||I026|Pc voltage<br>high|1C|0|10|10|V|3121|550C|30||
||O047|Pc transmit-<br>ter min.|1C|-1|0|-1|barg|3124|550C|33||
||O048|Pc transmit-<br>ter max|1C|1|200|34|barg|3125|550C|34||
||O020|Pe transmit-<br>ter min.||-1|0|-1|barg|3115|550C|2A||
||O021|Pe transmit-<br>ter max.||1|200|12|barg|3116|550C|2B||
||||||||||||0 = Not defined | 1 = AKS|
||I085|Pe transmit-<br>ter configu-<br>ration|1B, 1D|0|8|0||3270|550C|C5|i<br>32R | 2 = ACCPBP Ratio |<br>3 = 112CP | 4 = OEM Ra-<br>tio | 5 = NSK | 6 = AKS 32<br>1-5V | 7 = OEM Voltage |<br>8 = Bus shared|
||I086|Pe transmit-<br>ter configu-<br>ration|1A|0|7|0|||||0 = Not defined | 1 = AKS<br>32R | 2 = ACCPBP Ratio |<br>3 = 112CP | 4 = OEM Ra-<br>tio | 5 = NSK | 6 = AKS 32<br>1-5V | 7 = OEM Voltage|
||I087|Pe voltage<br>low|1A, 1B, 1D|0||0|V|3276|550C|CB||
||I088|Pe voltage<br>high|1A, 1B, 1D||5|5|V|3274|550C|C9||

||**Label**|**Parameter**<br>**name**|**Variants**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|
||I090|Ext ref. con-<br>figuration|1A|0|2|0|||||0 = Not Used | 1 = V->SH<br>| 2 = V->Max OD<br>|
||I089|Ext ref. con-<br>figuration|1B, 1D|0|6|0||3278|550C|CD|0 = Not Used | 1 = V->SH<br>| 2 = V->Max OD | 3 = V-<br>>Temp | 4 = Bus->SH | 5<br>= Bus->Max OD | 6 =<br>Bus->Temp|
||O010|Ext ref. con-<br>figuration|1C|0|9|0||3126|550C|35|0 = Not Used | 1 = V->SH<br>| 2 = V->Max OD | 3 = V-<br>>Temp | 4 = Bus->SH | 5<br>= Bus->Max OD | 6 =<br>Bus->Temp | 7 = mA-<br>>SH | 8 = mA->Max OD |<br>9 = mA->Temp|
|External refer-<br>|I035|Ext ref. volt-<br>age high|1A, 1B, 1D||10|10|V|3129|550C|38||
|ence signal|I036|Ext ref. cur-<br>rent low|1C|0||4|mA|3128|550C|37||
||I037|Ext ref. cur-<br>rent high|1C||20|20|mA|3127|550C|36||
||I034|Ext ref. volt-<br>age low|1A, 1B, 1D|0||0|V|3130|550C|39||
||I091|Driver refer-<br>ence config-<br>uration|1B, 1D|0|2|0||3282|550C|D1|0 = Voltage to OD | 1 =<br>Bus to OD | 2 = Bus to<br>steps|
||I033|Driver refer-<br>ence config-<br>uration|1C|0|3|0||3131|550C|3A|0 = Voltage to OD | 1 =<br>Bus to OD | 2 = Bus to<br>steps | 3 = Current to OD|
||I079|AI4 lowpass<br>bandwidth||0|5|5||3257|550C|B8|0 = None | 1 = 4 Hz | 2 =<br>2 Hz | 3 = 1 Hz | 4 = 1/2<br>Hz | 5 = 1/5 Hz|
|**Control Basics**||||||||||||
||O030|Refrigerant||0|49|0||3017|550B|C8|0 = Undef | 1 = R12 | 2 =<br>R22 | 3 = R134a | 4 =<br>R502 | 5 = R717 | 6 = R13<br>| 7 = R13b1 | 8 = R23 | 9<br>= R500 | 10 = R503 | 11 =<br>R114 | 12 = R142b | 13 =<br>R user | 14 = R32 | 15 =<br>R227 | 16 = R401A | 17 =<br>R507 | 18 = R402A | 19 =<br>R404A | 20 = R407C | 21<br>= R407A | 22 = R407B |<br>23 = R410A | 24 = R170 |<br>25 = R290 | 26 = R600 |<br>27 = R600a | 28 = R744 |<br>29 = R1270 | 30 = R417A<br>| 31 = R422A | 32 =<br>R413A | 33 = R422D | 34<br>= R427A | 35 = R438A |<br>36 = R513A | 37 = R407F<br>|
|Refrigerant con-<br>figuration|||||||||||| 38 = R1234ze | 39 =<br>R1234yf | 40 = R448A |<br>41 = R449A | 42 = R452A<br>| 43 = R450A | 44 =<br>R452B | 45 = R454B | 46<br>= R1233zdE | 47 =<br>R1234zeZ | 48 = R449B |<br>49 = R407H|
||O100|Antoine<br>constant A1||8|12|9.8||3018|550B|C9||
||O101|Antoine<br>constant A2||-3000|-1300|-2250||3019|550B|CA||
||O102|Antoine<br>constant A3||210|300|253||3020|550B|CB||
||O103|Refrigerant<br>min. tem-<br>perature||-100||-100|°C|3021|550B|CC||
||O104|Refrigerant<br>max. tem-<br>perature|||100|100|°C|3022|550B|CD||

||**Label**|**Parameter**<br>**name**|**Varia**|**nts**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
||N102|Startup<br>mode|||0|2|0||3023|550B|CE|0 = Prop. Ctrl | 1 = Fix OD<br>w prot | 2 = Fix OD wo<br>prot|
|Start up|N015|Startup time|||1|600|90|s|3024|550B|CF||
||N104|Minimum<br>startup time|||1|240|15|s|3025|550B|D0||
||N017|Startup OD|||1|100|32|%|3026|550B|D1||
||N021|SH reference<br>mode|||0|3|2||3027|550B|D2|0 = Fixed sp. | 1 = Loa-<br>dap | 2 = MSS | 3 = Delta<br>temp|
||N107|SH fixed set-<br>point|||2|40|7|K|3028|550B|D3||
||N009|SH maxi-<br>mum||||40|9|K|3029|550B|D4||
|Superheat con-<br>figuration|N010|SH mini-<br>mum<br>|||2||4|K|3030|550B|D5||
||N116|SH reference<br>delta temp.<br>factor|||20|100|65|%|3035|550B|DA||
||N005|SH Tn|||20|900|90|s|3031|550B|D6||
||N019|SH Kp Min.|||0.1|1|0.6||3032|550B|D7||
||N004|SH Kp|||0.1|20|1.5||3033|550B|D8||
||N020|SH KpTe|||0|20|3||3034|550B|D9||
|**Control Advanc**|**ed**||||||||||||
||N117|SH close<br>function|||0|1|1||3036|550B|DB|0 = Off | 1 = On|
||N119|SH close set-<br>point|||-5|20|2|K|3037|550B|DC||
|SH Close|N120|SH close Tn<br>divide|||1|5|3||3038|550B|DD||
||N121|SH close Kp<br>factor|||0.5|10|1.5||3039|550B|DE||
|S4 Temperature|N126|Minimum S4<br>mode|1B, 1|C, 1D|0|1|0||3042|550B|E1|0 = Off | 1 = On|
|protection|N127|Minimum S4<br>setpoint|1B, 1|C, 1D|-50|60|5|°C|3043|550B|E2||
||N123|Limit Kp|||1|20|5||3040|550B|DF||
|Sht|N125|Limit Tn|||20|900|45|s|3041|550B|E0||
|uperea con-<br>figuration Ad-<br>vance|N018|MSS Stabili-<br>ty|||0|10|5||3044|550B|E3||
||N129|MSS T0 sta-<br>bility factor|||0|1|0||3045|550B|E4||
||N130|MOP func-<br>tion|||0|1|0||3046|550B|E5|0 = Off | 1 = On|
||N011|MOP set-<br>point|||-70|60|0|°C|3047|550B|E6||
||N140|LOP func-<br>tion|||0|1|0||3048|550B|E7|0 = Off | 1 = On|
|MOP/LOP|N141|LOP setpoint|||-90|40|-40|°C|3049|550B|E8||
||N142|LOP priority<br>mode|||0|1|0||3050|550B|E9|0 = Off | 1 = On|
||N131|LOP maxi-<br>mum time|||0|600|120|s|3051|550B|EA||
||N132|LOP oscilla-<br>tion detec-<br>tion|||0|1|1||3052|550B|EB|0 = Off | 1 = On|
|||High con-<br>|||||||||||
||N133|densing<br>temp. pro-<br>tection func-<br>tion|1B, 1|C, 1D|0|1|0||3053|550B|EC|0 = Off | 1 = On|
|HCTP||High con-<br>densin|||||||||||
||N134|g<br>temp. pro-<br>tection set-<br>point|1B, 1|C, 1D|0|100|50|°C|3054|550B|ED||

||**Label**|**Parameter**<br>**name**<br>**Varia**|**nts**<br>**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|
||N135|Compressor<br>speed feed-<br>forward<br>function|0|1|0||3055|550B|EE|0 = Off | 1 = On|
|Compressor<br>Feed Forward|N136|FF low ca-<br>pacity turn-<br>ing point|0|100|25|%|3056|550B|EF||
||N137|FF maxi-<br>mum factor<br>for Tn tun-<br>ing|1|5|2||3057|550B|F0||
|Diagnostic SH|N143|SH control<br>sensor error<br>action|0|2|0||3058|550B|F1|0 = Stop | 1 = Fixed OD |<br>2 = Average|
|Emergency cool-|N144|Thermostat-<br>ic sensor er-<br>ror action<br>1B, 1C|, 1D<br>0|2|0||3059|550B|F2|0 = Stop | 1 = Fixed OD |<br>2 = Average|
|<br>||Fixed OD|||||||||
|ing|N145|<br>during<br>emergency<br>cooling|0|100|0|%|3060|550B|F3||
||N112|Heat startup<br>time|1|600|s|0|3061|550B|F4||
||N103|Heat mini-<br>mum start-<br>up time|1|240|s|0|3062|550B|F5||
||N105|Heat startup<br>OD|1|100|%|0|3063|550B|F6||
||N106|Heat SH<br>fixed set-<br>point|2|40|K|1|3064|550B|F7||
||N108|Heat SH<br>maximum||40|K|1|3065|550B|F8||
||N109|Heat SH<br>minimum|2||K|1|3066|550B|F9||
|Control Heat-|||||||||||
|<br>pump setup|N115|Heat SH ref.<br>delta temp.<br>factor|20|100|%|0|3067|550B|FA||
||N110|Heat SH Tn|20|900|s|0|3068|550B|FB||
||N111|Heat SH Kp<br>minimum|0.1|1||1|3069|550B|FC||
||N113|Heat SH Kp|0.1|20||1|3070|550B|FD||
||N114|Heat SH<br>KpTe|0|20||1|3071|550B|FE||
||N118|Heat SH<br>close set-<br>point|-5|20|K|1|3072|550B|FF||
||N124|Heat limit Tn|20|900|s|0|3073|550C|00||
||N122|Heat limit<br>Kp|1|20||1|3074|550C|01||
||D102|Defrost start<br>time|0|600|s|0|3076|550C|03||
|Defrost se-|D100|Defrost OD|0|100|%|1|3077|550C|04||
|<br>quence|D104|Defrost end<br>closed time|0|600|s|0|3078|550C|05||
|**Alarm configura**|D103<br>**ition**|Defrost end<br>OD time|0|600|s|0|3079|550C|06||

|**Label**|**Parameter**<br>**name**<br>**Varia**|**nts**<br>**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|
|A100|Low Min S4<br>delay|0|1200|s|0|3081|550C|08||
|A101|Low Min S4<br>band|0|30|K|1|3082|550C|09||
|A001|Upper tem-<br>perature<br>alarm|0|40|K|1|3083|550C|0A||
|A002|Lower tem-<br>perature<br>alarm|0|40|K|1|3084|550C|0B||
|A003|Temperature<br>alarm delay|0|90|min|0|3085|550C|0C||
|A034|Battery<br>alarm|0|1||0|3086|550C|0D|0 = Off | 1 = On|
|A103|MOP alarm<br>delay|0|1200|s|0|3087|550C|0E||
|A104|MOP alarm<br>differential|0|40|K|1|3088|550C|0F||
|<br>A105|LOP alarm<br>delay|0|1200|s|0|3089|550C|10||
|Alarm and Errors<br>A106|LOP alarm<br>differential|0|40|K|1|3090|550C|11||
|A107|Condensing<br>temp. alarm<br>delay|0|1200|s|0|3091|550C|12||
|A113|Condensing<br>temp. alarm<br>differential|0|40|K|1|3092|550C|13||
|A108|High SH<br>alarm delay|0|1800|s|0|3093|550C|14||
|A109|High SH<br>alarm differ-<br>ential|0|40|K|1|3094|550C|15||
|A110|Low SH<br>alarm delay|0|1200|s|0|3095|550C|16||
|A102|Low SH<br>alarm differ-<br>ential|0|40|K|1|3096|550C|17||
|A112|Lack of ca-<br>pacity alarm<br>delay|0|120|min|0|3097|550C|18||
|**Display**||||||||||
|O011|Language|0|0||0|3157|550C|54|0 = $ActiveLanguageList|
|K004|Login time-<br>out|1|120|min|0|3158|550C|55||
|K006|Backlight<br>timeout|0|120|min|0|3159|550C|56||
|O005|Password<br>daily|0|999||0|3160|550C|57||
|K002|Password<br>service|0|999||0|3161|550C|58||
|K003|Password<br>commission|0|999||0|3162|550C|59||
|K005|Contrast|0|100|%|0|3163|550C|5A||
|K001|Brightness|0|100|%|0|3164|550C|5B||
|R005|Display unit|0|1||0|3165|550C|5C|0 = MET | 1 = IMP|
|K010<br>**Communication**|Opening de-<br>gree unit|0|1||0|3166|550C|5D|0 = Percentage | 1 = Step|

||**Label**|**Parameter**<br>**name**|**Variants**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|
||G001|Controller<br>address||1|127||0|3167|550C|5E||
||G005|Modbus<br>baudrate|1B, 1C|0|8||0|3170|550C|61|0 = 0 | 1 = 1200 | 2 =<br>2400 | 3 = 4800 | 4 =<br>9600 | 5 = 14400 | 6 =<br>19200 | 7 = 28800 | 8 =<br>38400|
||G008|Modbus<br>mode|1B, 1C|0|2||0|3171|550C|62|0 = 8N1 | 1 = 8E1 | 2 =<br>8N2|
|CAN/MODBus|G007|Modbus<br>mapping|1B, 1C|0|1||0|3172|550C|63|0 = Operation | 1 = Con-<br>figuration|
||G002|CANbus<br>baudrate||0|5||0|3173|550C|64|0 = 20k | 1 = 50k | 2 =<br>125k | 3 = 250k | 4 =<br>500k | 5 = 1M|
||G004|Bus sharing<br>minimum<br>update in-<br>terval|1B, 1C, 1D|1|60|s|0|3169|550C|60||
||G003|Signal shar-<br>ing mini-<br>mum up-<br>date interval||1|60|s|0|3168|550C|5F||
||G012|Signal shar-<br>ing Pe||0|1||0|3174|550C|65|0 = Off | 1 = On|
|Signal sharing<br>via BUS|G013|Signal shar-<br>ing Pc|1B, 1C, 1D|0|1||0|3175|550C|66|0 = Off | 1 = On|
||G014|Signal shar-<br>ing S3||0|1||0|3176|550C|67|0 = Off | 1 = On|
|**BUS Settings**||||||||||||
||X001|Bus shared<br>Heating||0|1||0|4043|550F|CA|0 = Off | 1 = On|
|Modbus DI sig-|X002|Bus shared<br>Preset OD||0|1||0|4044|550F|CB|0 = Off | 1 = On|
|nal|X003|Bus shared<br>Defrost start||0|1||0|4045|550F|CC|0 = Off | 1 = On|
||X004|Bus shared<br>Main switch||0|1||0|4046|550F|CD|0 = Off | 1 = On|
||X005|Bus shared<br>Pc||-1|200|barg|2|4047|550F|CE||
||X006|Bus shared<br>Pe||-1|200|barg|2|4048|550F|CF||
|Modbus Sensor|X007|Bus shared<br>S2||-200|200|°C|1|4049|550F|D0||
|signal|X008|Bus shared<br>S3||-200|200|°C|1|4050|550F|D1||
||X009|Bus shared<br>S4||-200|200|°C|1|4051|550F|D2||
||X010|Bus shared<br>Ext. ref.||-100|100||1|4052|550F|D3||
||X015|Number of<br>active<br>alarms||0|100||0|4055|550F|D6||
||X016|Alarm notifi-<br>cation||0|1||0|4056|550F|D7|0 = No alarms | 1 =<br>Alarms active|
|Alarms status|X040|Alarm status||0|1||0|4057|550F|D8|0 = Off | 1 = On|
||X017|Warning sta-<br>tus||0|1||0|4058|550F|D9|0 = Off | 1 = On|
||X018|Error status||0|1||0|4059|550F|DA|0 = Off | 1 = On|
||X027|Valve cur-<br>rent position||0|10000|steps|0|4068|550F|E3||
|Valve status|X028|Valve target<br>position||0|10000|steps|0|4069|550F|E4||
||X031|Service<br>number of<br>steps||-32767|32767||0|4072|550F|E7||

||**Label**|**Parameter**<br>**name**|**Variants**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Su**<br>**index**|**b‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|
||X037|User con-<br>trols LEDs||0|1||0|4074|550F|E9|0 = Off | 1 = On|
|User control<br>LEDs|X038|Green LED<br>pattern||0|65535||0|4075|550F|EA||
||X039|Red LED pat-<br>tern||0|65535||0|4076|550F|EB||
|**Service**||||||||||||
||||||||||||0 = Power up | 1 = Stop |<br>2 = Manual | 3 = Service |<br>4 = Safe State | 5 = De-<br>frosting | 6 = Valve driver<br>| 7 = Ther. Cutout | 8 =<br>Emer. cooling | 9 = SH<br>ctrl err | 10 = SH start|
|Status Readout|U118|Operation<br>status||0|20||0|4005|550F|A4|.<br>Pctrl | 11 = SH start fix<br>OD | 12 = SH ctrl normal<br>| 13 = SH ctrl MTR | 14 =<br>SH ctrl LOP | 15 = SH ctrl<br>minPC | 16 = SH ctrl<br>MOP | 17 = SH ctrl<br>maxPc | 18 = SH ctrl SH<br>cl | 19 = SH ctrl minS4 |<br>20 = SH ctrl Tc|
||U022|Actual SH<br>reference||0|100|K|1|4006|550F|A5||
||U021|Actual su-<br>perheat||0|100|K|1|4007|550F|A6||
||U024|Actual OD||0|100|%|1|4008|550F|A7||
||U100|Actual step||0|10000|stp|0|4009|550F|A8||
||U028|Actual tem-<br>perature ref-<br>erence||0|100|K|1|4010|550F|A9||
||U020|S2 suction<br>pipe||-50|150|°C|1|4011|550F|AA||
||U027|S3 media in-<br>let|1B, 1C, 1D|-50|150|°C|1|4012|550F|AB||
||U016|S4 media<br>outlet|1B, 1C, 1D|-50|150|°C|1|4013|550F|AC||
||U025|Pe evapora-<br>tor||-1|200|barg|2|4014|550F|AD||
||U026|Te saturated<br>evaporation<br>temperature||0|100|°C|1|4015|550F|AE||
||U104|Pc condens-<br>er|1B, 1C, 1D|-1|200|barg|2|4016|550F|AF||
||U105|Tc saturated<br>condenser<br>temperature|1B, 1C, 1D|0|100|°C|1|4017|550F|B0||
||U101|Actual bat-<br>tery voltage||0|30|V|1|4018|550F|B1||
||U058|Liquid line<br>solenoid<br>valve||0|1||0|4026|550F|B9|0 = Off | 1 = On|
||U114|Alarm relay<br>||0|1||0|4027|550F|BA|0 = Off | 1 = On|
||U007|External ref-<br>erence sig-<br>nal|1A, 1B, 1D|0|12|V|1|4028|550F|BB||
||U006|External ref-<br>erence sig-<br>nal|1C|0|24|mA|1|4029|550F|BC||
||U107|Act. ext. ref.<br>temperature<br>offset||0|40|K|1|4030|550F|BD||
||U108|f<br>Act. ext. ref.<br>SH offset||0|40|K|1|4031|550F|BE||
||U124|Act. ext. ref.<br>maximum<br>OD||0|100|%|1|4092|550F|FB||
|Digital Input<br>Readout|U109|DI main<br>switch||0|1||0|4032|550F|BF|0 = Off | 1 = On|

||**Label**|**Parameter**<br>**name**<br>|**Vari**|**ants**|**Min**|**Max**|**Default**|**Unit**|**Modbus**<br>**PNU**|**Can In‐**<br>**dex**|**Can Sub**<br>**index**|**‐**<br>**Enumeration**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
||U110|DI defrost<br>start|||0|1||0|4033|550F|C0|0 = Off | 1 = On|
||U111|DI preset OD|||0|1||0|4034|550F|C1|0 = Off | 1 = On|
||U112|DI heating|||0|1||0|4035|550F|C2|0 = Off | 1 = On|
||U113|DI PWR<br>Backup sig-<br>nal|||0|1||0|4093|550F|FC|0 = Off | 1 = On|
||U115|PWR Backup<br>status|||0|4||0|4094|550F|FD|0 = Initializing | 1 =<br>Ready | 2 = Charge | 3 =<br>Replace | 4 = Failure|
||U018|Thermostat<br>cut-in time|||0|16300|min|0|4019|550F|B2||
||U119|Thermostat<br>average cut-<br>in time|||0|16300|min|0|4020|550F|B3||
||U120|Thermostat<br>average cut-<br>out time|||0|16300|min|0|4021|550F|B4||
||U122|Average<br>temperature|||0|100|°C|1|4091|550F|FA||
||U121|Average SH|||0|100|K|1|4090|550F|F9||
||U123|Average OD|||0|100||0|4002|550F|A1||
||U125|Estimated<br>KpTe|||0|100||1|4003|550F|A2||
||U126|Average del-<br>ta tempera-<br>ture<br>|1B, 1|C, 1D|0|50||1|4004|550F|A3||
|Manual opera-<br>tion|O018|Manual<br>mode|||0|1||0|4036|550F|C3|0 = Off | 1 = On|
||B101|Manual<br>mode time-<br>out|||0|3600|s|0|3177|550C|68||
||O045|Manual OD|||0|100|%|1|4037|550F|C4||
||B100|Manual step|||0|8000|stp|0|4038|550F|C5||
||B104|Manual<br>homeing|||0|1||0|4039|550F|C6|0 = Off | 1 = On|
||B103|Manual relay<br>DO1|||0|1||0|4040|550F|C7|0 = Off | 1 = On|
||B007|Apply de-<br>faults|||0|3||0|4041|550F|C8|0 = None | 1 = Factory | 2<br>= EKD 316 like | 3 = EKC<br>316 like|
||B105|Enter service<br>state|||0|1||0|3178|550C|69|0 = Off | 1 = On|

#### **8 Alarms and troubleshooting**

Depending on the application, the EKE 1x series implements error codes and alarms to help the user troubleshoot and correct parameters easily. When an alarm occurs, the following actions generally ensue:

- the “Alarm” or “Warning” relay is activated

- an icon and the alarm code are displayed on the screen

The alarms are reset automatically. The alarm is deactivated as soon as the alarm condition ceases. Otherwise, the user must follow the deactivation procedure once the alarm conditions is over. When the alarm is eliminated the alarm, relay is deactivated, and the alarm code will no longer be displayed.

###### **Fi** **g ure 77: LED indication**

- A Two status LEDs to indicate operational status

   - Steady green = power ON

   - Flashing green = data transmission / initialization

   - Flickering red = alarm / error condition

- B Two status LEDs to indicate valve operation

   - Flashing red = valve closing

   - Steady red = valve fully closed

   - Flashing green = valve opening

   - Steady green = valve fully open

   - Both green and red flashing = valve-related alarm

#### **8.1 Alarms**

#### 8.1.1 Configuration errors

**Table 65: Confi** **g uration errors**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|E101|Configuration error|Auto operation<br>blocked|Active when: - D12 and D13<br>have the same mapping config-<br>uration. - All and AI5 have the<br>same mapping configuration.|Correct application settings|One or more configuration errors is block-<br>ing operation to start. Check the other ac-<br>tive alarms to identify the configuration<br>problem.|
|E011|No refrigerant selec-<br>ted|Auto operation<br>blocked|0030 refrigerant set to none|Set 0030 refrigerant set to an<br>actual refrigerant|No refrigerant is selected, configure the<br>correct refrigerant. See "0030 Refrigerant"|
|E104|SH reference too<br>close to SH close set<br>point|Auto operation<br>blocked|SH close is used and SH close<br>set pint is too close the actual<br>reference/ reference minimum|Disable SH close or correct the<br>actual SH reference / reference<br>minimum to have 0.5K differ-<br>ence to SH close set point|SH reference can come to close to the SH<br>close safety functions et point. which can<br>result in unstable operation. Keep min.<br>0.5K separation between minimum SH ref-<br>erence and N119 SH close set point.|
|E105|LOP set point too<br>close to MOP set<br>point|Auto operation<br>blocked|If MOP and LOP is used, Mop<br>set point - Lop set point must ><br>5K|Disable MOP or LOP, or adjust<br>the difference on MOP-LOP set<br>point >= 5K|The set point for the 2-pressure safety<br>function Lop and Mop is to close. Keep<br>min. 5K separation between NO11 MOP<br>set point and N140 LOP set point|
|E129|No sensor config-<br>ured for S4|Auto operation<br>blocked|Application need a S4 signal for<br>either thermostat or Min S4.<br>but S4 signal is configured|Disable the functions needing<br>S4 or configure a S4 signal|Operation is configured to use S4 (media<br>out) sensor, but no S4 sensor is configured.<br>Correct I020 All configuration or AI5 con-<br>figuration and check I042 S4 sensor config-<br>uration|
|E106|No sensor config-<br>ured for S3|Auto operation<br>blocked|Thermostat need a S3 signal<br>and no s3 signal is configured|Disable the functions needing<br>S4 or configure a S4 signal|Operation is configured to use S3 (media<br>in) sensor, but no S3 sensor is configured,<br>Correct 1020 All configuration or AI5 con-<br>figuration and check I041 S3 sensor config-<br>uration|

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|E107|SH min higher than<br>SH max|Auto operation<br>blocked|SH max lower than SH low|Adjust SH max or SH low, SH<br>Max >=SH low|NO10 SH min. is set higher than N009 SH<br>max.|
|E108|OD min higher than<br>OD max|Auto operation<br>blocked|OD max lower than OD low|Adjust OD max or OD low, OD<br>Max >=0D low|1066 Minimum OD is set higher than NO32<br>Maximum OD|
|E109|No transmitter con-<br>figured for Pc|Auto operation<br>blocked|Application needs PC signal for<br>high condensing temperature<br>protection|Disable High condensing tem-<br>perature protection or config-<br>ure PC transmitter|Operation is configured to use Pc transmit-<br>ter. but no Pc transmitter is configured.<br>Correct I022 Al4 configuration and check<br>I044 Pc transmitter configuration|
|E125|Al5 can't operate<br>with AKS sensor|Auto operation<br>blocked|ON EKE 1C AI5 configuration is<br>setup as AKS sensor|Set AI5 configuration to the of<br>NTC1OK type|EKE 1C don't support AKS sensor on AI5.<br>Please use a temperature sensor on NTC<br>type on AI5. Correct, I022 AI5 configura-<br>tion|
|E132|No sensor config-<br>ured for S2|Auto operation<br>blocked|S2 Sensor configuration = Not<br>defined||No sensor type defined for S2|
|E133|No transmitter con-<br>figured for Pe|Auto operation<br>blocked|Pe transmitter configuration =<br>Not defined||No pressure transmitter type defined for<br>Pe|
|E134|Ext. ref. configura-<br>tion error|||Correct setting|Check the ext. ref. signal and the ext. ref.<br>configuration.|

#### 8.1.2 Sensor alarms/errors

**Table 66: Sensor alarms/errors**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|E024|S2 suction pipe sen-<br>sor error|Alarm if backup sig-<br>nal is found, error if<br>no backup possible,<br>emergency cooling|Local sensor problem local sen-<br>sor outside range + hysteresis|Get the local sensor inside sig-<br>nal range|S2 suction pipe sensor signal is found to<br>be out of out of range, please check con-<br>nection and I040 S2 sensor configuration|
|E025|S3 media inlet sen-<br>sor error|Alarm if backup sig-<br>nal is found, error if<br>no backup possible,<br>emergency cooling|If S3 is used: local sensor prob-<br>lem local sensor outside range<br>+ hysteresis|S3 not used or get the local<br>sensor inside signal range|S3 media inlet sensor signal is found to be<br>out of out of range, please check connec-<br>tion and I041 S3 sensor configuration|
|E026|S4 media outlet sen-<br>sor error|Alarm if backup sig-<br>nal is found, error if<br>no backup possible,<br>emergency cooling|If S4 is used: local sensor prob-<br>lem local sensor outside range<br>+ hysteresis|S4 not used or get the local<br>sensor inside signal range|S4 media outlet sensor signal is found to<br>be out of out of range, please check con-<br>nection and I042 S4 sensor configuration|
|E020|Pe evaporator trans-<br>mitter error|Alarm if backup sig-<br>nal is found, error if<br>no backup possible,<br>emergency cooling|Local sensor problem local sen-<br>sor outside range + hysteresis|Get the local sensor inside sig-<br>nal range|Pe evaporator transmitter signal is found<br>to be out of out of range, please check<br>connection and I043 Pe transmitter config-<br>uration|
|E121|Pc condenser trans-<br>mitter error|Alarm if backup sig-<br>nal is found, error if<br>no backup possible|Local sensor problem local sen-<br>sor outside range + hysteresis|Pc not used or get the local sen-<br>sor inside signal range|Pc transmitter signal is found to be out of<br>out of range, please check connection and<br>I044 Pc transmitter configuration|
|A982|Thermostatic signal<br>missing|Emergency Cooling<br>thermostat|If thermostat is used and S3 or<br>S4 signal missing (depending<br>on sensor select|Get valid signal on S3 or S4|Signal for thermostat is missing due to<br>sensor errors, check S3 or S4|
|A981|SH control signal<br>missing|Emergency cooling<br>SH control|Pe or S2 signal missing|Get valid signal on Pe and S2|Signal for superheat calculation is missing,<br>check S2 and Pe|
|E019|External reference<br>signal alarm||External reference out of range<br>+ hysteresis|get external signal inside range|External offset/reference signal is out of<br>range, please check connection and 0010<br>Ext ref configuration and relevant<br>high/low settings|
|A999|Dl1 unstable input|DI is set to off|DI is unstable, loose connection<br>more than 10 transition per mi-<br>nute|DI has stable low or high signal,<br>below 6 transitions per minute|DI1 is found be unstable (many on/off<br>within a Short time). Dl1 is set off until sta-<br>ble value is present. Check connection|
|A998|DI2 unstable input|DI2 is set to off|DI2 is unstable, loose connec-<br>tion more than 10 transitions<br>per minute|DI2 has stable low or high sig-<br>nal, below 6 transitions per mi-<br>nute|DI2 is found be unstable (many on/off<br>within a Short time). DI2 is set off until sta-<br>ble value is present. Check connection|
|A983|DI3 unstable input|DI3 is set to off|DI3 is unstable, loose connec-<br>tion more than 10 transitions<br>per minute|DI3 has stable low or high sig-<br>nal, below 6 transitions per mi-<br>nute|DI3 is found be unstable (many on/ off<br>within a Short time). DI3 is set off until sta-<br>ble value is present. Check connection|
|E102|Sensor supply over-<br>load|Bios make power<br>state on the actual<br>supply, automatic<br>operation blocked|Too much current draw on +5V<br>150mA+ or +15V (200mA+)|+5V below 50mA and +15V be-<br>low 30mA|Sensor supply is overloaded. The output is<br>set off until the load is reduced, Check for<br>Short to COM|
|E123|Low supply voltage|Operation is<br>blocked (main<br>switch is set to off;<br>stepper is not op-<br>erational)|Stepper voltage below 16V|Stepper voltage above 16V|Supply voltage is found to be lower than<br>expected tolerance|

#### 8.1.3 Stepper alarms/errors

**Table 67: Ste** **pp er alarms/errors**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|E103|No valve configured|Auto operation<br>blocked|I067 valve configuration set<br>none|I067 valve configuration set a<br>valve from the list|No valve selected. Please configure the<br>correct valve in I067 Valve configuration|
|E100|Valve configuration<br>error|Auto operation<br>blocked|One or more stepper configura-<br>tion errors|Correct stepper config|One or more valve configuration errors is<br>blocking operation of stepper valve. Check<br>the other active alarms to identify the<br>valve configuration problem|
|E114|check valve step<br>mode vs positioning|Auto operation<br>blocked|Stepper mode is full step and<br>half as final is requested|If full step mode is wanted set<br>final positioning to full. If half<br>step as final position is wanted,<br>set step mode to minimum half<br>step|With 1064 Valve step mode set to "full"<br>and IO29 Valve step positioning set Half<br>step operation is possible, Correct either<br>IO29 or IO64|
|E115|Valve speed too fast|Auto operation<br>blocked|Combination of step mode and<br>speed give too few micro speed<br>per sec (below 8)|Adjust valve speed and/ or<br>valve step mode to be with lim-<br>its|Number of micro steps/sec is too high<br>(higher than 12800 micro step/sec), Re-<br>duce IO31 Valve speed or use less micro<br>step per full step (IO64 Valve step mode)|
|E116|Valve speed to slow|Auto operation<br>blocked|Combination of step mode and<br>speed give too many micro<br>speed per sec (higher than<br>12800)|Adjust valve speed and/ or<br>valve step mode to be with lim-<br>its|Number of micro steps/sec is low (higher<br>than 8 micro step/sec), increase IO31 Valve<br>speed or increase IO32 Valve start speed or<br>use more micro step per full step (IO64<br>Valve step mode)|
|E117|Valve emergency<br>speed too fast|Auto operation<br>blocked|Combination of step mode and<br>speed give too few micro speed<br>per sec (below 8)|Adjust valve speed and/ or<br>valve step mode to be with lim-<br>its|Number of micro steps/sec is too high<br>(higher than 12800 micro step/sec), Re-<br>duce IO61 Valve emergency speed|
|E118|Valve emergency<br>speed too slow|Auto operation<br>blocked|Combination of step mode and<br>speed give too many micro<br>speed per sec (higher than<br>12800)|Adjust valve speed and/ or<br>valve step mode to be with lim-<br>its|Number of micro steps/sec is low (higher<br>than 8 micro step/sec), increase IO61 Valve<br>emergency speed|
|E119|Valve start speed<br>too slow|Auto operation<br>blocked|Combination of step mode and<br>speed give too few micro speed<br>pr sec (below 8)|Adjust valve speed and/ or<br>valve step mode to be with lim-<br>its|Number of micro steps/sec is low (higher<br>than 8 micro step/sec), increase IO31 Valve<br>speed or increase IO32 Valve start speed or<br>use more micro step per full step (IO64<br>Valve step mode)|
|E126|Valve Short circuit or<br>driver too hot|Auto operation<br>blocked, stepper will<br>try to recover every<br>10 secs|Stepper driver report thermal<br>Shutdown,|Stepper driver has recovered<br>from thermal overload|Valve driver is unable to drive valve. Check<br>for Short the coils or if ambient is higher<br>than 60 °C|
|A997|Battery critical low<br>voltage||Battery input below 12V|Battery input above 12.2V|Battery voltage is found to be critical low;<br>valve will not be closed in case of power<br>fail. Replace battery /check connections|
|A996|Battery too high<br>voltage||Battery input above 27V|Battery input below 25V|Battery voltage is too high. Valve will not<br>be closed in case of power fail. Replace<br>battery with one of correct type (18-24V.).|
|W001|Battery low voltage||Battery input below 17V|Battery input above 17.2V|Battery voltage is found to be low, replace<br>battery.|
|E124|Open circuit on<br>valve|Auto operation<br>blocked; stepper will<br>try to recover every<br>10 secs|Stepper detect one or 2 open<br>coils|Current in both coils match<br>valve profile|Valve have an open circuit on one or more<br>coils. Check connections to valve.|

#### 8.1.4 Bus alarms/errors

**Table 68: Bus alarms/errors**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|E122|Shared signal time-<br>out||One or more signals (S2, S3, S4,<br>P0, PC) are not Shared through<br>CAN within "CAN bus Min. up-<br>date interval" or Modbus with”<br>Modbus min. update interval<br>seconds".|All needed signal is updated at<br>right frequency|A needed control / sensor / reference sig-<br>nal via CAN bus is missing. Check CAN bus<br>connection and operation of other CAN<br>bus controllers.|
|E128|Ext. ref. via Modbus<br>timeout|If bus signal via<br>Modbus|Bus ext ref. needs to be upda-<br>ted within "Modbus min. up-<br>date interval seconds".|Ext reference signal updated<br>within Modbus min. update in-<br>terval|A needed control / sensor / reference sig-<br>nal via Modbus is missing. Check Modbus<br>connection and operation of other Mod-<br>bus controllers.|

#### 8.1.5 Application alarms

**Table 69: A** **pp lication alarms**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|A994|Low S4 media outlet<br>temperature||Injection active and Min S4<br>function active and S4 below<br>MIN S4 set point - Low Min S4<br>band and Low Min S4 delay ex-<br>pired|Injection not active or Min S4<br>function disabled or S4 above<br>MIN S4 set point - Low Min S4<br>band|Media out temperature is below alarm lim-<br>it and alarm delay has expired.|
|A991|High evaporation<br>pressure (MOP)||Injection active and Mop active<br>and Te higher than mop set<br>point + MOP alarm differential<br>and MOP alarm delay expired|Injection not active or Mop dis-<br>abled or Te below mop set<br>point + MOP alarm differential|Pe /Te is higher than alarm limit and alarm<br>delay has expired.|
|A990|Low evaporation<br>pressure (LOP)||Injection active and Lop active<br>and Te lower than lop set point<br>- LOP alarm differential and<br>Cond temp alarm delay expired|Injection not active or Lop disa-<br>bled or Te above lop set point +<br>LOP alarm differential|Pe /Te is lower than alarm limit and alarm<br>delay has expired.|
|A989|High condensing<br>temperature||Injection active and HCTP ac-<br>tive and Tc above HCTP set<br>point + Cond. temp.alarm dif-<br>ferential and LOP alarm delay<br>expired|Injection not active or HCTP<br>disabled or Tc below HCTP set<br>point + Cond. temp.alarm dif-<br>ferential|Pc / Tc is higher than alarm limit and alarm<br>delay has expired.|
|A988<sup>**(1)**</sup>|High superheat||Injection active and SH above<br>SH reference +High SH alarm<br>differential and High SH alarm<br>delay expired|Injection not active or SH below<br>SH reference +High SH alarm<br>differential|Superheat is higher than alarm limit and<br>alarm delay has expired.|
|A987<sup>**(2)**</sup>|Low superheat||Injection active and SH below<br>SH reference - low SH alarm dif-<br>ferential and low SH alarm de-<br>lay expired|Injection not active or SH above<br>SH reference - low SH alarm dif-<br>ferential|Superheat is below alarm limit and alarm<br>delay has expired.|
|A986|Lack of valve capaci-<br>ty||Injection active and OD higher<br>than max OD - 5% for more<br>than 90 96 of Lack of capacity<br>alarm delay time|Injection not active or OD high-<br>er OD - 5% in less than 88% for<br>Lack of capacity alarm delay<br>time|Valve is running close to full capacity for<br>long time.|
|E135|Error in Heat/Cold in<br>thermostat mode||Use of DI as H/C function in<br>thermostat mode.|Avoid H/C function in DI while<br>in thermostat mode.|H/C function not available in thermostat<br>mode.|

- **(1) • Length of monitoring window for High superheat detection can be adjusted using parameter [A108 – High SH alarm delay]. If the parameter is set to 0 the function is disabled.**

- **The high superheat limit is def** i **ned by the user through parameter [A109 – High SH alarm dif** f **erential] High superheat limit= SH ref+ High SH alarm dif** f **erential.**

- **(2) • Length of monitoring window for Low superheat detection can be adjusted using parameter [A110 – Low SH alarm delay]. If the parameter is set to 0 the function is disabled.**

- **The high superheat limit is def** i **ned by the user through parameter [A998 - Low SH alarm dif** f **erential] Low superheat limit= SH ref- Low SH alarm dif** f **erential, If Low superheat limit is lower than SH close set point, then**

**Low superheat limit= SH close set point.**

#### 8.1.6 Thermostat alarms

**Table 70: Thermostat alarms**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|A993|High temperature||Thermostat active and thermo-<br>stat temperature (s4/ S3) above<br>actual reference + Upper tem-<br>perature alarm for Temperature<br>alarm delay time|Thermostat not active or ther-<br>mostat temperature (s4/S3) be-<br>low actual reference + Upper<br>temperature alarm|Thermostat temperature is higher than<br>alarm limit and alarm delay has expired|
|A992|Low temperature||Thermostat active and thermo-<br>stat temperature (s4/ S3) below<br>actual reference - lower tem-<br>perature alarm for Temperature<br>alarm delay time|Thermostat not active or ther-<br>mostat temperature (s4/S3)<br>above actual reference - lower<br>temperature alarm|Thermostat temperature is lower than<br>alarm limit and alarm delay has expired|

#### 8.1.7 Stop state alarm

**Table 71: Sto** **p state alarm**

|**Label**<br>W002|**Alarm**<br>**descrip‐**<br>**tion**<br>Standby<br>mode|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**<br>Controller is in stop state|**How to clear the alarm**<br>Controller not in stop state|**Remark**<br>The controller is standby due R012 Main<br>switch and/or DI main switch is off|
|---|---|---|---|---|---|

#### 8.1.8 Manual mode alarm

**Table 72: Manual mode alarm**

|**Label**|**Alarm description**|**Actions during ac‐**<br>**tive**|**Trigger (how the alarm IS**<br>**raised)**|**How to clear the alarm**|**Remark**|
|---|---|---|---|---|---|
|W003|Manual control||Controller is in manual state|Controller not in manual state|The controller is manual control, no auto-<br>matic control is active, and many alarms<br>are disabled|

#### **8.2 Troubleshooting**

###### **Table 73: Troubleshootin** **g**

|**ID**<br>**Symptom**|**Possible cause/Reaction**|**Solution**|
|---|---|---|
|1<br>Regulation does not start on<br>using control modes i.e.|DI is not connected, if defined as ON/OFF hardware switch.|• Turn on DI switch.|
|,<br>MSS|Sensor / transmitter error.|• Check and clear alarm.|
||Alarm configuration conflict i.e. S2 sensor not defined or<br>no refrigerant selected.|• Clear and clear Alarm.|
||Alarm: standby mode active i.e. Parameter R012 is OFF.|• Set R012 main switch to 1.|
|2<br>Suction pressure too low|Pressure drops across evaporator too high.|• Check refrigerant ahead of expansion valve, If valve is<br>placed much higher than condenser outlet.<br>• Check pressure difference.|
||Lack of sub cooling ahead of expansion valve.|• Limit max opening degree of the valve setting in con-<br>troller.<br>• Check refrigeration system capacity and compare with<br>expansion valve capacity.<br>• Use proper valve size, Suitable for the system.|
||Evaporator superheat too high.|• Check the section " High Superheat".|
||Pressure drop across the expansion valve less than valve is<br>sized for.|• Check pressure drop across expansion valve. Replace<br>with larger valve.|
||Expansion valve too small.|• Check refrigeration system capacity and compare with<br>expansion valve capacity. Replace with larger valve if<br>necessary.<br>• Check selected valve type in the controller valve list.|
||Expansion valve block with foreign material.|• Remove valve and examine the orifice /piston.|
||Wrong selection of Refrigerant in the controller settings.|• Choose the correct Refrigerant from the pre-defined<br>list.|
||Lack of Charge in the system.|• Charge the system with appropriate refrigerant capaci-<br>ty.<br>• Check for leakage in the system.|
||Pressure transmitter ranges or type is wrongly defined.|• Define the correct pressure range.|
||MOP set point is defined very low.|• Check the MOP setting, if Modbus is used, check if the<br>values have been scaled as indicated in the parameter<br>list|
||Evaporator wholly or partly iced up.|• De-ice evaporator.|
||Low chilled water flow|• Check flow as per design|
||chilled water temp too low|• Check temp set points as per Design|
|3<br>Low pressure cut out due to<br>|Missing start signal.|• Check for digital input DI signal or its settings.|
|compressor cut in and cut<br>out|Startup problem.|• Check section start- up problem and its solution.|

|**ID**<br>**Symptom**<br>4<br>Liquid hammer in compres-<br>sor (noisy or unusual com-<br>|**Possible cause/Reaction**<br>Superheat reference set too low.|**Solution**<br>• Increase the SH reference by changing the SH min.<br>max. parameter.|
|---|---|---|
|pressor sound) and /or frost<br>on the suction line|Superheat is too low.|• Make sure SH Close function is ON.<br>• Increase the values of SH close and SH min.<br>• Also check section "Too low superheat"|
||Inaccurate SH measurement or slow response in S2 sen-<br>sors.|• Ensure that S2 sensor is secured on suction line.<br>• Insulate temperature sensor properly.<br>• Check the product installation guide section tempera-|
|||ture sensor.|
||Refrigerant or pressure transmitter is not set correctly.|• Check the related parameters.|
|5<br>Too Low superheat|Min. SH parameter is too low set.<br>Valve Cannot Close fully.|• Raise the min. SH parameter.<br>• Reduced the Valve OD or forced opening time at Start|
|||up.|
||Valve OD too large at start up.|• Use P-control.<br>• Reduce Start OD.|
||Inaccurate superheat.|• Mounting position of Temperature sensor. Place sensor<br>close to evaporator.|
||High-pressure drop-in suction line.|• Mounting position of the pressure transmitter. Place<br>the transmitter close to evaporator.<br>• Check the product installation guide section tempera-<br>ture sensor.|
||Valve is stuck at open.|• Check valve installation.|
||Liquid returns to compressor.|• Check section Liquid hammering.|
|6<br>High superheat|Lack of sub-cooling.|• Limit max opening degree of the valve setting in con-<br>troller.<br>• Check refrigeration system capacity and compare with<br>expansion valve capacity. Use proper valve size suitable<br>for the system.|
||Controller is not setup/tuned properly.|• Check the controller superheat settings SH min, SH max<br>and sensors connected to it.<br>• Tune PID parameters in the controller.|
||Wrong valve selected from the controller list or undersized<br>valve installed.|• Check the right valve type and setting or use the ap-<br>propriate valve size for the needed condition.|
||Seasonally high load condition or overloaded the system.|• Check the heat exchanger for dirt's.<br>• Check superheat performance.|
|7<br>Too high or too low meas-<br>ured superheat|Wrong sensor type, refrigerant type, pressure transmitter<br>type and/or range.|• Check the related setting and range.<br>• In case of offset in sensor or pressure transmitter, per-<br>form the sensor correction.<br>• Always use accurate pressure transmitter|
|8<br>Measured Superheat is<br>higher than reference -<br>more than 5K for 5 - 10 min.|Load condition has changed, and the superheat controller<br>is too slow to adapt to the change.|• TN can be adjusted to 20% lower and Kp can be adjus-<br>ted to be 20% higher, monitor that the adjustment<br>doesn’t make the valve OD and Pe/Te oscillate.|
||Compressor capacity has changed, and the superheat con-<br>troller is too slow to adapt to the change.|• Compensation for compressor change is done with<br>KpTe in this case KpTe can be adjusted to be 20% high-<br>er.|
||Missing valve capacity.|• Check if valve OD is close to 100 %, if so, the valve is<br>missing capacity, check if sub cooling is OK.<br>• System might have loss charge.|
|Measured Superheat is low-<br>er than reference - lower 3K|SH close parameter is disabled or not setup optimally.|<br>• Enable the SH close function and set the setpoint 2K<br>below the reference.|
||Compressor capacity has changed, and the superheat con-<br>troller is act too aggressive to adapt to the change.|• Compensation for compressor change is done with<br>KpTe in this case KpTe can be adjusted to be 20% lower.|
|9<br>Fluctuating superheat|The S2 sensor not in good contact with the suction line.<br>Fast change in load and ambient condition.|• Check proper mounting of the temperature sensor.<br>• Wait for the stable condition and check again.|
||Periodic flash gas at the valve inlet.|• Secure stable sub cooling|
||Aggressive gain Kp and Kp Te parameter.|• Decrease gain in the controller, ex set SH Tn to be 20 %<br>higher and reduce Kp 20%, if still SH is fluctuating, re-<br>duce KpTe by 20%.<br>• Try with the higher SH reference.|
|10<br>Negative superheat|Wrong sensor type, refrigerant type, pressure transmitter<br>type and range.|• Check the related setting and range.|
||During start up suction pressure is low because of low Am-<br>bient temperature.|• Check the startup problem.|
||<br>System is not running.|• Check the system.|

|**ID**|**Symptom**<br>|**Possible cause/Reaction**<br>|**Solution**|
|---|---|---|---|
|11|Superheat outside the de-<br>fined range or does not<br>reached the setpoint|Wrong valve selected or its valve parameter.<br>Loss of refrigerant in the system.|• Check the right valve type and its setting.<br>• Charge the system with appropriate refrigerant capaci-<br>ty.<br>• Check for leakage in the system.|
|||Expansion valve too small.<br>Step loss in the valve.|• Replace with larger valve if necessary.<br>• Check the selected valve in the controller valve list.<br>• Drive the stepper valve with the recommended Speed.<br>• Too high or too low speed could result in loss step in<br>the valve.<br>• For the user defined valves, check the other valve set-<br>tings such as current, duty cycle, holding current and<br>another relevant parameter.|
||||• Use overdrive features to mitigate the loss steps. Use<br>the correct overdriving values with respect to the used<br>value.<br>• Wrong defined valve type or its setting.<br>• Longer cables mounted than specified for the control-<br>ler.<br>• Separate Valve cable from other high-power cables and<br>do not bundle the cables.|
||||• Obstruction in the valve or high friction in the valve.<br>• MOPD exceeded than specified in the valve specifica-<br>|
||||tion.|
|12|Takes too long to settle SH<br>at reference point|Too low gain Kp and KpTe or long integration time Tn.|• Increase Kp by factor of 1.5%<br>• Decrease Tn 25% of the set value<br>• Perform 1 and 2 in a loop if needed.|
|||At start up. the pull-down time for SH or temp is longer.|• Use start with P. control and increase start OD.<br>• If the superheat in general is 4K higher than reference 1<br>minute alter start up. the startup OD can be adjusted to<br>be 20 % higher.|
|||Wrong selection of the valve.|• Check the valve type and in setting.|
|||Wrong selection of the reference point.|• Correctly define the min, max SH setting and/or refer-<br>ence type i.e MSS/Load defined ap / Fixed/delta Temp.<br>• Also check section, High superheat and ‘Too high and<br>too low superheat’|
|13|Startup problem|low pressure cut out at start up|• Check the LEO Alarm connection.<br>• Missing synchronization with controller and the com-<br>pressor Le. D4 not connected to EKE.<br>• Wrong Of missing valve connection. Check the M12 ca-<br>ble connection to the valve and to the controller.<br>• Check other component in the suctions liquid 'Meta<br>any keel of blockage.<br>• Use the LOP feature during start up.|
|||Unsynchronized signals.|• Make sure that main switch signal and the compressor<br>start are synchrony, it ok to have until 2 sec delay.|
|||High Superheat after startup.|• Check section Too high or too low superheat.|
|14|Startup problem after de-<br>frost|low suction cut out|• Use EKE defrost sequence feature.<br>• Use LOP feature<br>• Use P- control at start method and prolong the start<br>tine|
||||• Check the right signal from the controller.|
|15|Unable to maintain media<br>temperature|Lack of sub-cooling ahead of expansion valve|<br>• Limit max opening degree of the valve setting in con-<br>troller.<br>• Check refrigeration system capacity and compare with<br>expansion valve capacity. Use proper valve size suitable<br>for the system.|
|||Check section High superheat and Low suction Pressure||
|||Wrong selection of temperature sensor and or installation.|• Check for the right sensor configuration|
|||Check Working condition of the unit|• Check Superheat.|

|**ID**|**Symptom**|**Possible cause/Reaction**|**Solution**|
|---|---|---|---|
|16|Flash gas|Loud refrigerant or undercharged refrigerant.|• Charge the system with appropriate refrigerant capaci-<br>|
||||ty.<br>• Check for leakage is the system.<br>• If the valve is placed much higher than condenser<br>tweet check pressure difference.|
|||Flash gas can lead to high SH or low suction pressure<br>i|• Use the right valve size.<br>• Also refer to section “High Superheat” and “Suction<br>pressure too low”|
|||Pressure drops across filter.|• Check and replace the Stet.|
|17|Steppe valves open/ close<br>l|Incorrect selection of valve type.|• Dane the correct valve type.|
||too sow|Incorrect valve installation.|• Check the physical vale and cable and intake in light<br>way.|
|||MOPD is higher than valve specification.|• Check the valve spec and choose the correct vane.|
|||Check valve speed setting.|• Drive the stepper valve with the recommended Speed.<br>• Too high or too low speed could result in loss step in<br>the valve.<br>• For the user defined valves, check the other valve set-<br>tings such as current, duty cycle, holding current and<br>other relevant parameter.|
|18|Opening degree of valve at<br>maximum OD for longer<br>|Lack of cooling capacity.|• Check the cooling capacity in the system Also check<br>section, expansion valve too small|
||time period|The condenser pressure is too low.|• Check the ambient temperature.<br>• Adjust the condenser controller.|
|||The filter drier is blocked by dirt|• Replacement Filter drier.|
|||Flash gas in liquid line due to loss of refrigerant or under-<br>charge of refrigerant.|• Check section flash gas.|
|||Wrong valve setting.|• Check valor setting matching installed valve.|
|||Pressure transmitter is wrongly defined.|• Oita pressure range and correct pressure transmitter<br>type.|
|||Wrong refrigerant selected|• Choose the correct refrigerant in the controller.|
|19|Hunting or fluctuation valve<br>position|Too high gain (Kp and KpTe) or too low integration time<br>(Tn).|• Decrease Kp by factor of 1.5%<br>• Increase Tn 25% of the set value.<br>• Perform 1 and 2 in loop if needed.|
|||S2 thermal contact.|• Check mounting of S2 sensor, Check the installation<br>guide section temperature sensor mounting.|
|||Fluctuating Al signal for SH reference.|• Check Al signal quality.|
|||Fluctuating pressure signal.|• Check section Fluctuating pressure signal.|
|||Fluctuating Superheat.|• Check section Fluctuating Superheat.|
|20|Unstable OD on driving the<br>valve in Valve driver mode|Fluctuating Al signal.|• Check the Al signal quality.<br>• Use the Valve neutral zone feature.|
|21|Internal Leakage in the valve|Wrong selection of the valve.|• Check the valve type and its setting.|
|||Step loss in stepper motor valve.|• Power cycle the controller.<br>• Enable the step loss feature i.e. overdriving. choose the|
||||<br>recommended overdrive value with respect to the in-<br>stalled valve.|
||||• Drive the stepper valve with the recommended speed.<br>• Too high or too low speed could result in loss step in<br>the valve.|
||||• Longer cables mounted than specified for the control-<br>ler.<br>• Separate Valve cable from other high-power cables and<br>do not bundle the cables.|
||||• Blockage in the valve or high friction in the valve.|
||||• MOM, exceeded than specified in the valve specifica-<br>tion.|

|**ID**|**Symptom**|**Possible cause/Reaction**|**Solution**|
|---|---|---|---|
|22|Valve does not move|Valve neutral zone has been defined.|• Check Valve parameter in chapter Stepper motor valve.|
|||Loose or incorrect M12 cable connection.|• Check proper and firm connection of valve cable wires<br>to ENE terminals.<br>• Also check section Valve rotates in opposite direction'.|
|||Change in valve setting or other configurations.|• Check for the correct valve parameters.<br>• Check for the correct state of R12 ON/OFF regulation or<br>Dl connection.<br>• If Al or Modbus signal is used, make sure that the cor-<br>rect signal is connected to the controller.|
|||Incorrect voltage supplies to the controller.|• Check the power supply and measure input voltage to<br>the controller.|
|||Valve got stuck.|• Check the valve installation.<br>• Check for the dirt inside the valve.|
|||Valve motor is damaged; resistance of the motor varies a<br>lot than specified for a valve.|• Check the resistance in the motor between each coil.<br>• Make sure you consider some tolerances for cable or<br>temperature deviation.<br>• Replace the valve.|
|23|Valve rotates in opposite di-<br>rection|Valve M12 cable wire is wrongly connected to the control-<br>ler.|• Check the connection of wire color codes as stated in<br>Installation guide.<br>• For other valves than Danfoss, check with valve suppli-<br>er for the right connection.|
|||Wrong connection of wires at cable joint, if there is exten-<br>sion cable to the main Valve cable.|• Check for the right color configuration at the joint.|
|24|Valve is overdriven to Zero<br>position|EKE performs valve calibration in the following situation as<br>a normal procedure|• Normal operation|
|||Wrong defining of valve type.||
|||Valve overdrive feature is enabled, and OD is dosed to fully<br>closed position or the overdriving timer is ON.||
|||Alarm or Error condition will bring the valve to Zero posi-<br>tion and stop regulation||
|||On setting DI = Off when DI is set as ON/OFF regulation||
|25|Fluctuating pressure signal|Change in load of the system.<br>Faulty pressure sensor.|• Observe the change in the load of the system.<br>• Replace faulty pressure transmitter.|
|||Flash gas in the system.|• Check the section flash gas.|
|26|Compressor thermal cut out<br>(Mop is not working or go-<br>ing higher than set value)|MOP is not enabled, or wrongly defined.<br>Change in operating condition.|• Check mop settings.<br>• Observe the operating condition.<br>• Controller need time to adjust to the stable condition.|
|27|LOP protection doesn't work<br>at low pressure|if low superheat and low suction pressure exist same time<br>for some time, LOP function is disabled.|• Check operating condition and settings.|
|||Fast change in operating condition.|• Controller need time to adapt to the change condition.|
|28|Controller is in safe state<br>(check LED or display)|Internal error i.e., EEPROM error in controller software ex-<br>ceptions.|• Power cycle the controller, if continue to get the same<br>error then replace controller.|
|29|Controller freeze. nothing<br>|loose connections.|• Check the connection in the EKE.|
||happens|Incorrect voltage supplies to the controller.|• Check the power supply and measure input voltage to<br>the controller.|
||||• Power cycle controller and observe the LEDs, IF no LEDs<br>are lighting during power cycle, replace controller.|
|30|No communication (Indica-<br>ted by LEDs)|Wrong Modbus settings.|• Check Modbus address, baud rate, and protocol.<br>• EKE only supports Modbus RS 485 RTU, it does not sup-<br>port Modicon conventions.|
|||Loose connection or no termination.|• Check the Modbus terminals and use terminations.|
|||Check power supply to EKE controller|• If off, power on the controller|

#### **9 Appendix**

**Table 74: A** **pp endix 1: Acron** **y ms and abbreviations used in this document**

|**Full name**|**Abbreviation**|
|---|---|
|Compressor|Comp.|
|Capacity|cap|
|Controller|cont|
|Actual|act|
|Temperature at evaporator outlet|S2|
|Media inlet temperature|S3|
|Media out temperature|S4|
|Saturated temperature in evaporator|To /To|
|Pressure in evaporator|Pe / PO|
|Saturated temperature in condenser|To|
|Pressure in condenser|Pc|
|Proportional gain constant|Kp|
|Integration time|Tn|
|Proportional gain constant on saturated temperature|KpTe|
|Opening degree|OD|
|Superheat|SH|
|Minimum|Min.|
|Maximum|Max.|
|Reference|Ref.|
|Temperature|Temp.|
|Factor|Fac.|
|Oscillation|Osc.|
|Condensator|Cond.|
|Feed forward|FF|
|Set point|Sp.|
|Ratiometric|Ratio.|
|External|Ext.|
|Address|Adr.|
|Pulse per second|PPS|
|Step|Stp|
|Loss of charge indication|LOC|
|Temperature difference between media temperature and evaporating tempera-<br>ture|ATm|
|Maximum operating pressure|MOP|
|Minimum stable superheat|MSS|
|Parameter number|PNU|

#### **10 Ordering**

**Table 75: Product** **p art numbers**

|**Description**|**Pack format**|**CodeNo.**|
|---|---|---|
|Electronic controller EKE 1A|Single pack|080G5300|
|Electronic controller EKE 1B|Single pack|080G5350|
|Electronic controller EKE 1C|Single pack|080G5400|
|Electronic controller EKE 1D|Single pack||

###### **Table 76: Accessories** **p art numbers**

|**Description**|**Pack format**|**CodeNo.**|
|---|---|---|
|MMIGRS2 Remote Display|Single pack|080G0294|
|MMIMYK gateway|Single pack|080G0073|
|ACCCBI telephone cable user interface connector 1.5 m|Single pack|080G0075|

#### **11 Certificates, declarations, and approvals**

The list contains all certificates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

Some approvals may change over time. You can check the most current status at danfoss.com or contact your local Danfoss representative if you have any questions.

**Table 77: Certificates, declarations, and a** **pp rovals**

|**Document name**|**Document type**|**Document topic**|**Approval authority**|
|---|---|---|---|
|080R4003.01|EU Declaration of conformity|EMC directive 2014/30/EU:<br>EN61000-6-3: 2007 +A1: 2011<br>EN61000-6-2: 2005<br>LVD directive 2014/35/EU:<br>EN60730-1: 2011<br>EN60730-2-9: 2010<br>RoHS directive 2011/65/EU|Danfoss|

#### **12 Online support**

Danfoss offers a wide range of support along with our products, including digital product information, software, mobile apps, and expert guidance. See the possibilities below.

##### **The Danfoss Product Store**

The Danfoss Product Store is your one-stop shop for everything product related—no matter where you are in the world or what area of the cooling industry you work in. Get quick access to essential information like product specs, code numbers, technical documentation, certifications, accessories, and more.

Start browsing at store.danfoss.com.

##### **Find technical documentation**

Find the technical documentation you need to get your project up and running. Get direct access to our official collection of data sheets, certificates and declarations, manuals and guides, 3D models and drawings, case stories, brochures, and much more.

Start searching now at www.danfoss.com/en/service-and-support/documentation.

Danfoss Learning is a free online learning platform. It features courses and materials specifically designed to help engineers, installers, service technicians, and wholesalers better understand the products, applications, industry topics, and trends that will help you do your job better.

Create your Danfoss Learning account for free at www.danfoss.com/en/service-and-support/learning.

##### **Get local information and support**

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest regional news, or connect with a nearby expert—all in your own language.

Find your local Danfoss website here: www.danfoss.com/en/choose-region.

---

## 2. Data Sheet – Superheat controller and stepper valve driver Type EKE 1A,B,C (PV05), 1D (PV02)

*Kilde: Danfoss-dokument AI197986442906en-000502.pdf*

##### **Data Sheet**

### Superheat controller and stepper valve driver Type **EKE 1A,B,C (PV05), 1D (PV02)**

For air conditioning, commerical/Industrial heatpumps and refrigeration applications

The flexible pre-programmed EKE superheat controller from Danfoss provides ultimate software control, allowing you to tailor the performance of your system to your exact requirements. EKE is ideal for controlling a wide range of commercial air conditioning and refrigeration applications, such control helps you to achieve the highest efficiency in the system reducing the operational cost by up to 20% with minimal effort. EKE is generally used where there is a requirement for accurate control of superheat or temperature control in connection with air conditioning and refrigeration. The superheat is regulated to the lowest possible value within a short period of time. It regulates the superheat of the evaporator by charging optimally even when there are great variations of load resulting in reduction of energy consumption and operational cost

###### **Typical Applications**

- Chillers

- Processing plant / Cabinet cooling

- Cold store (air coolers)

- A/C plant / Air conditioning

- Commercial and Industrial heat pumps

- Transport cooling

- Stepper Motor Driver

#### **Portfolio overview**

**Table 1: Portfolio overview**

|**Features**||**EKE 1A**|**EKE 1B**|**EKE 1C**|**EKE 1D**|
|---|---|---|---|---|---|
|**Power supply:**||||||
|Power Supply Type|24 V AC / DC ± 20%|•|•|•|•|
|Battery Backup input|18-24 V DC|•|•|•|•|
|**Class of insulation**||||Class II||
|**Data communication**||||||
|MODBus|RS 485 RTU||•|•||
|Wired CANbus||||(4 wires)|(3 wires)|
|CANbus RJ 12|Danfoss MMI service port|•|•|•|•|
|**Inputs:**:||||||
|Number of temperature<br>sensors||1|2|3|2|
|Temperature sensor types|PT1000|||•||
||NTC 10K, type EKS|•|•|•|•|
||NTC 10K, type ACCPBT|•|•|•|•|
||NTC 10K, type Sensata|•|•|•|•|
|Number of Pressure sen-<br>sor||1|1|2*|1|
|Pressure Transmitter|Ratiometric 0.5 - 4.5 V|•|•|•|•|
|types|Voltage signal 0 – 10 V|•|•|•|•|
||Current signal 0 – 20 mA|||•||
|Share Pressure Signal|Hardware (Up to 5 devi-<br>ces)|•|•||•|
||Via wired CANbus (not<br>possible to share ratio-<br>metric sensor)|||•|•|
||Via MODbus||•|•||
|Number of external refer-<br>ences||1|1|1|1|
|External reference|0-20mA|||•||
||Userdefinedcurrent|||•||
||0-10V|•|•|•|•|
||0- 5V|•|•|•|•|
||Userdefinedvoltage( max<br>10V)|•|•|•|•|
|Digital input Dry contact||3||2||
|**Outputs**||||||
|Digital output||||1||
|Relay|Normally Open||3A Gener|al purpose, 250V ac, 100k||
||Normally closed||2A Gener|al purpose, 250V ac, 100k||
|Relay Function||Alarm rela|y or LLSV (Liquid Lin|e Solenoid Valve)||
|User interfaces|Koolprog Software tool|•|•|•|•|
||MMIGRS2 screen|•|•|•|•|
||Master controller||•|•|•|

*The 2nd pressure sensor is mounted on AI4

#### **Functions**

The EKE 1x products supports a wide range of functionalities illustrated in table 3 and 4. Check the user guide for more detail about configurations and other detailed options.

**Table 2: Hardware functions**

|**Hardware functions**|Used to interact with the EKE for systems where the EKE|is not connected to a system controller via data communica-|
|---|---|---|
||tion.||
|Digital inputs|The available digital inputs DI can be used for the follow|ing functions:|
||<br>**a.**Injection control ON/OFF(DI1).**b.**Defrost sequence (D<br>(DI2)|<br>I2).**c.**Heating and cooling selection mode (DI2)**d.**Preset OD|
||• The relay for the liquid line solenoid valve will operat<br>• The contact of the relay is closed in alarm situations<br>• The digital output DO1 O013 can beconfiguredfor s|e when refrigeration is required<br>and when the controller is de-energized.<br>olenoid valve, max capacityor for alarm function.|
||NC1+C1||
||Power On|NO|
||Power On +Alarm|NC|
|Digital Output (Relay)|Power Off|NC|
||NO1+C1||
||Power On|NC|
||Power On +Alarm|NO|
||Power Off|NO|
||For safety reasons the liquidflowto the evaporator mus<br>will remain open in power failure situation<br>|t be cutoffin case of power failure. The valve’s stepper Motor|
||There are two ways of coping with this situation||
|Handling power failure|One of the following two solutions can be applied in the|system|
||• Mounting of a solenoid valve in front of EEV (using L<br>• Mounting of a battery backup for EEV valve (Use Dan|LSV relay signal from EKE)<br>foss EKE 2U)|
||External Reference Signal:<br>Used for:||
|Analog Inputs|• Driving the stepper motor valve to a desired opening<br>• Displacing temperature reference, superheat referen|degree (Driver Mode)<br>ce or max OD|
||The voltage signal e.g., 0 – 10 V can be used in all EKE co<br>available in EKE 1C|ntrollers whereas current signal e.g 0 – 20 mA signal is only|
|Communication: RS485 Modbus / CANbus|The controller can be provided with data communicatio<br>In this case, monitoring and data collection can be perfo<br>the diagnostic or during the installation processes.<br>For example, it is possible to substitute the physical sens<br>frequency of update should be according to the Modbu|n for connecting to other devices in the systems.<br>rmed from one device i.e., PLC – which will bebeneficialfor<br>ors of the EKE controller by writing sensor values via Bus. The<br>s maximum update interval G004 (Refer to parameter list)|
||Two sets of light-emitting diodes make it possible to foll<br>indicate the following<br>• Power/data transmission and Alarm/Error indication<br>• Stepper valve operational status|ow the operation status of the valve and the controller. They|
||LED status:||
|Light-emitting diodes (LEDs)|Red constant<br>valve is closed||
||Green constant<br>valve is fully open||
||Flashing red<br>valve is moving in close direction||
||Flashing green<br>valve is moving in open direction||
||Flashing red and green<br>Error||

**Table 3: Control Functions**

|Valve Driver|The EKE controls the opening degree of the valve, the control signal can be an analog signal or a value via communica-<br>tion bus|
|---|---|
||•**Fixed Superheat**The controller keep the superheat at afixedreference value determined by the user. SHfixedsetpoint<br>can be varied according to the need of application.|
||•**Minimum Stable Superheat (MSS):**The superheat control algorithm will attempt to regulate the superheat down to<br>the lowest stable value between the minimum superheat setting, “Min SH” and the maximum superheat setting, “Max.<br>SH”.|
|Superheat Reference Calculation|•**LoadAP Superheat LoadAP**is a kind of preprogrammed MSS curve. In Load ap application, SH reference follows a<br>definedcurve as shown in the diagram. This two-point curve isdefinedby SH max and SH min, this method will give a<br>robust SH reference and can in many cases be the bestfitfor systems.|
||•**Delta temp. superheat**SH reference is calculated as a ratio between the media temperature and evaporator tempera-<br>ture. This reference mode is only possible if media temperature (S3) sensor is available and if the system usesfinand tube<br>evaporator.|
||EKE has a feature to regulate the temperature control. This can be done with either|
|Temperature Control *|•**Thermostat cut in/cut out function:**if temperature is above the set point +differential,cooling is started with maxi-<br>mum cooling capacity. In maximum capacity superheat is controlled to be on superheat set point. Cooling is active until<br>the temperature is below set point.|
||•**Modulating Thermostat (MTR):**When temperature is getting close to the MTR reference the cooling capacity gradually<br>reduce so that the temperature can be stable on the MTR reference and the superheat will befloating.|
||•**Failsafe operation:**During operation if sensors error occurs, the valve position can be set to full close,fixed<br>opening degree or average calculated OD as required.|
||•**Superheat close:**When the superheat is below a set minimum value, the valve will close faster to protect the compres-<br>sor from the risk of getting liquid in the suction line and bring the superheat back to superheat reference.|
||•**Maximum Operating Pressure (MOP):**To reduce the strain on the compressor, a maximum operating pressure is set. If<br>the pressure comes above this limit the controller will control the valve to provide a lower pressure instead of a low su-<br>|
|Protection Functions|perheat.|
||•**Low Operating Pressure (LOP):**known as Cold start feature, it allows applications such as heat pumps to operate at<br>lower ambient conditions to prevent compressor from stopping due to low suction pressure in the startup phase.|
||•**High Condensing temperature protection (HCTP)**:**High condensing temperature protection will make sure that<br>the load on the condenser is reduced in case a too high condensing temperature is reached. This is done by limiting the<br>valve opening degree.<br>•**Minimum S4/leaving media (freeze protection) *:**Lowers theflowin the expansion valve if temperature of leaving<br>media out of the evaporator is below a minimum value set by the user.|
||•**Fast Start up:**Quickly open an EEV valve when compressor turns ON to prevent too low suction pressure as well as for<br>faster stabilization of superheat or temperature set point. This can be ensured by setting either P-control, Start opening<br>degree with protection or Fixed opening degree without protection. This start up condition is kept until the start time<br>expire or superheat reaches at setpoint.|
||•**Defrost sequence:**The controller does not itself handle defrost of the evaporator. It is however possible to enter a spe-|
|Other Functions|<br>cial defrost sequence which will overrule the normal control of the valve.|
||•**Manual control:**The valve can be controlled manually by setting the desired opening degree via Analog signal or com-<br>munication bus used for commissioning purpose. A special service mode is also available for service and testing purpose.|
||•**Service mode:**Service mode is designed to provide a very simple way of operating the valve for diagnostic and service<br>purpose. There is neither application nor protection in this mode. The user can open and close the valve using simple<br>button presses on MMIGRS2.|

*Not available in EKE 1A

**Only Available EKE 1C

#### **Applications**

EKE series devices are used where precise control of superheat in air conditioning system is needed. It helps achieving high energy efficiency and reliable operation

EKE serves 2 main applications:

- Driver Mode

- Controller Mode

1. Superheat controller 2. Temperature controller

#### **Driver mode**

**Driver Mode:** A master is commanding the valve open degree to the EKE controller. The control signal can be fed for example by:

- Analog signal e.g., 0 – 10 V, a 4 – 20 mA

- Bus communication via RS485 (Modbus RTU).

###### **Fi** **g ure 1: EKE as Driver Mode**

*[Figurtekst: Battery Optional connection · Mandatory connection · Power 24 V AC / 24 V DC · ON/OFF signal · Modbus or Analog signal · EKE controller (in driver mode) MASTER controller · Alarm indication · Normal close · TT Pe · S2 · EEV · Danfoss  80G8221.01]*

 **NOTE:**

'Normal closed' valve in front of EEV is optional alternative to a battery backup solution which closes the EEV in case of power fail. The Digital output can also be used as alarm indication to the master controller. The Master can send a start signal to EKE DI terminals

#### **Controller Mode**

###### **Controller Mode:**

**Superheat Control:** EKE can serve as a PI controller that controls the superheat of the evaporator based on a pressure Pe and temperature (S2) sensors. In superheat mode the controller will control the superheat to be stable and close to the superheat reference. If superheat is too low the flow in the expansion is decreased and superheat will be higher

###### **Fi** **g ure 2: Su** **p erheat control a** **pp lication**

*[Figurtekst: EKE 1X · TT Pe · S2 · EEV · Danfoss  80G8222.01]*

**Temperature controller** The temperature control is an ON/OFF thermostat that opens/closes the stepper valve or modulating thermostat that regulates temperature more smoothly following a temperature reference point. The temperature control can be accomplished via a signal from temperature sensor S3 placed in the air flow before the evaporator or S4 placed in the air flow after the evaporator.

EKE has 2 methods of controlling temperature:

- ON/OFF thermostat

- Modulating thermostat (MTR)

The need for cooling can either be defined by the incoming media (S3) or the outgoing media (S4) temperature

###### **Fi** **g ure 3: Tem** **p erature control a** **pp lication**

*[Figurtekst: Preset OD · Defrost · Heat / cool mode · External main switch · Battery · Power 24 V AC / 24 V DC · External reference · Optional connection · EKE controller · Mandatory connection · Temperature control · TT S4 · Alarm indication · Normal close · S2TT Pe · EEV TT S3 · Danfoss  80G8223.01]*

 **NOTE:**

EKE1A can only work in the driver mode or superheat control mode as it supports only one temperature sensor input

#### **Product specification**

#### **Technical data**

**Table 4: General s** **p ecification**

|**Feature**|**Description**|
|---|---|
|Power supply|Galvanic isolation by switch mode power supply<br>Input voltage rating (AC): 24 V AC ± 20 % (min.19.2 V AC - max. 28.8 V AC<br>Input frequency (AC): 50 / 60 Hz<br>Input voltage rating (DC): 24 V DC (min. 20 - max. 40 V DC)<br>Provides 5 W at 5 V and 15 V outputs isolated from the 24 V input<br>Insulation between power supply and the extra-low voltage.<br>Class of insulation Class II|
|Power Consumption|Total Power consumption with following valve in operation and MMIGRS2 con-<br>nected to the controller:<br>CCMT 16 - CCMT 42: 15VA/10W<br>ETS 8M (Bipolar), CCMT L<br>ETS 6: 11 VA / 7.5W<br>ETS 12C - ETS 100C: 20VA / 14W<br>KVS C: 20VA / 14W<br>ETS 12.5 - ETS 400 7 VA / 5W<br>CCMT 2 - CCMT 8 7 VA / 5W<br>CTR 20: 7 VA / 5W|
|Plastic Housing|• DIN rail mounting complying with EN 50022<br>• Self-extinguishing V0 according to IEC 60695-11-10 and glowing / hot wire<br>test at 960 °C according to IEC 60695-2-12<br>• Material used for Enclosure are UL94-V0 and RoHS compliant<br>• Ball test: 125 °C according to IEC 60730-1<br>• Leakage current: ≥ 250 V according to IEC 60112|
|Connectors|• Plug able Screw connector Pitch 3.5 mm, relay and power connector Pitch 5<br>mm, CAN MMI: Modular Jack 6P4C<br>• Material used for connectors are RoHS and UL approved|

**Table 5: Electrical s** **p ecification**

|**Feature**|**Type**|**Description**|
|---|---|---|
||Short circuit|Motor driver: dissipative over current protection|
|Protection|Over voltage|Analog input: current limit and internal clamp diode<br>Digital input: current limit and internal clamp diode<br>Communication: transceiver IC|
||Over Temperature|Motor driver: thermal shutdown at 150 °C|
||Unstable Digital Input|Continuous variation of the digital input state|

**Table 6: In** **p ut/Out** **p ut**

|**I/O**|**Type**|**Specifications**|
|---|---|---|
|||• Max. 15 V input voltage<br>• Open circuit HW diagnostics available for voltage input on: AI3, AI4<br>(EKE 1C) AI4 (EKE 1A and EKE 1B).<br>**WARNING:**<br>Do not connect voltage sources without current limitation (overall 80<br>mA) to analog inputs while unit is not powered.|
||0 – 5 V|EKE 1C (AI3, AI4) and EKE1A/1B/1D AI3 | Accuracy ± 40 mV, resolution 1.2<br>mV.|
||0 – 10 V|EKE 1C (AI3, AI4) and EKE1A/1B/1D AI3 | Accuracy ± 50 mV, resolution 2.5<br>mV.|
|Analog inputs|0 – 20 mA (EKE 1C only)|Accuracy ± 100 μA, resolution 10 μA.<br>Input resistance: <100 Ω|
||NTC Sensor|NTC temperature probes: 10 kΩ at 25 °C range: 300 kΩ to 100 Ω<br>Accuracy: 50 – 120 °C: 1.5 K, -40 – 50 °C: 0.4 K, 0 °C: 0.2 K<br>Resolution: ≤ 0.1 K, ≤ 0.3 K (EKC 1C, AI5)|
||Pt1000 sensor|Range: 723 Ω to 1684 Ω<br>Accuracy: ≤ 0.5 K<br>Resolution: ≤ 0.1K|
|||Type: Ratiometric|
|||• Accuracy: 1.6 %|
||Pressure Sensor|• Range: 0.5 – 4.5 V<br>• Resolution: 1.2 mV<br>• Supply voltage: 5 V DC / 15 mA, overload protection approximately<br>150 mA|

|**I/O**|**Type**|**Specifications**<br>Steady current of 1 mA (EKE 1C only). A cut-in input will activate a func-<br>tion.<br>|
|---|---|---|
|Digital Input DI|Voltage free contacts|Cleaning current of 100 mA at 15 V DC.<br>On: RIL <= 300 Ω .Off:RIH >= 3.5kΩ.<br>No destructive if Vbat + is connected to DI (only for DI on bottom pcb).<br>Min. pulse time 64 ms.|
|Digital output (D01)|Relay|Normally Open: 3 A General purpose, 250 V AC, 100 k cycle<br>Normally Open: 3 A Inductive (AC-15), 250 V AC, 100 k cycle<br>Normally Closed: 2 A General purpose, 250 V AC, 100 k cycle|
|||Other Valves:|
|Stepper motor|Bipolar stepper Motor Output|• speed 10 - 400 pps<br>• drive mode full step, half step, 1/8 microstep<br>• max. peak phase current: 1.2 A (848 mA RMS)<br>• max. output power 12 W|
|Battery backup||VBATT: 18 – 24 V DC:<br>Leakage: <15 μA @30 V DC<br>Optional: critical low alarm below 12V<br>Optional: low alarm at 17 V, high voltage alarm at 27 V<br>The valve will not close at power fail if voltage is higher than 27 V<br>Required power to do 1 closing of stepper valve:<br>ETS 6: 110 J / 30 VmAh<br>ETS 12.5 - ETS 400: 60 J / 17 VmAh<br>KVS 15 / KVS 42: 60 J / 17 VmAh<br>ETS 12C - ETS 100C: 55 J / 15 VmAh<br>KVS 2C / KVS 5C: 55 J / 15 VmAh<br>CCMT 2 - CCMT 8: 60 J / 17 VmAh<br>CCMT 16 - CCMT 42: 175 J / 49 VmAh<br>CTR 20: 60 J / 17 VmAh<br>**NOTE:**<br>Danfoss recommends using EKE 2U as a battery backup|
||RS-485 RTU (only for EKE 1B and<br>1C)|Galvanic isolation. No Built-in termination.<br>Supported commands with max. of 50 ms response time: 0 x 03, 0 x 04, 0<br>x 06<br>Supported commands withoutdefinedmax response time : 0x08, 0x10,<br>0x14, 0x15,0x2b|
|||• EKE 1A/1B: CANOpen over RJ12 connector.|
|Communication||• EKE 1C: CANOpen over CAN 4pin terminal and RJ12 connector.<br>• EKE 1D: CANOpen over CAN 3pin terminal and RJ12 connector.|
|||**NOTE:**|
||CAN|• For EKE EKE 1A/1B, RJ12 connector is used directly connect and sup-<br>ply a user interface MMI<br>• Refer to the user guide for information about type of connection ca-<br>bles|

#### **Environmental conditions:**

**Table 7: Environmental conditions**

|**Feature**|**Description**|
|---|---|
|Operating conditions|-20 – 60 °C, 90% RH non-condensing|
|Storage / Transport conditions|-30 – 80 °C, 90% RH non-condensing|
|Vibration and shock|According to IEC 60068-2-27 Ea|
|Integration|In Class I and / or II appliances|
|Index of protection|IP40 only on the front cover (General IP20 )|
|PCB protection|None (no conformal coating)|
|Period of electric stress across insulating parts|Long|
|Resistance to heat andfire|Category D|
||Immunity against voltage surges Category II|
|Approvals|1.<br>2.<br>3.<br>CE compliance:<br>This product is designed to comply with the following EU standards:<br>• Low voltage guideline: 2014/35/EU<br>• Electromagnetic compatibility EMC: 2014/30/EU and with the following norms<br>EN61000-6-1. EN61000-6-3, (immunity and emission standard for residential. commercial and lightin-<br>dustrial environments)<br>EN61000-6-2. EN61000-6-4, (immunity and emission standard for industrial environments)<br>EN60730-1 and EN60730-2-9 (Automatic electrical controls for household and similar use)<br>• RoHS compliance to 2011/65/EU and no components from negative list acc. to 500B0751|

#### **Identif i** **cation**

Product label is positioned in the front of the product

###### **Fi** **g ure 4: Exam** **p le EKE 1C**

*[Figurtekst: Product nam e · Product type - code no . Product QR code · Electrical specification · Product version PV04 SW2.04 Country of origin · Approval s Manufacturer address · Example: EKE 1C]*

#### **Dimensions and weights**

**Fi** **g ure 5: EKE 1A, EKE 1B, EKE 1C, EKE 1D Dimensions**

*[Figurtekst: CAN RJ · 70 60 · 130 110]*

*[Figurtekst: Danfoss · 80G8215.11]*

###### **Net Weight:**

- EKE 1C: 170 g

- EKE 1A / EKE 1B / EKE 1D: 130 g

#### **Connections:**

*[Figurtekst: Fi g ure 6: EKE 1A connectors Fi g ure 7: EKE 1B connectors · ANALOG / DIGITAL INPUT CAN - RJ · RS485 ANALOG / DIGITAL INPUT CAN - RJ · CAN RJ · CAN RJ · EKA 1A - 080G5300 · EKA 1B - 080G5350 · PWR 24V Vbat STEPPER VALVE DIGITAL OUTPUT · PWR 24V Vbat STEPPER VALVE DIGITAL OUTPUT · Danfoss 80G8286.01 · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · D – D+ RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 AI1 COM · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1]*

###### **Fi** **g ure 8: EKE 1D connectors**

*[Figurtekst: CAN ANALOG / DIGITAL INPUT CAN - RJ · CAN RJ · Superheat controller · EKA 1D- 080G5360 · PWR 24V Vbat STEPPER VALVE DIGITAL OUTPUT · Danfoss 80G8286.01 · L H RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 AI1 COM · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1]*

*[Figurtekst: Fi g ure 9: EKE 1C connectors: Front Fi g ure 10: EKE 1C connectors: Back · ANALOG INPUT 1-5 DIGITAL INPUT 1-2 · EKE 1C - 080G5400 · EKE 1C - 080G5400 · CAN RJ · CAN CAN RJ RS485 · PWR 24V Vbat STEPPER VALVE DIGITAL OUTPUT · Danfoss  80G8286.01 · Danfoss 80G8286.01 · Not used 15V+ 5V+ COM AI5 AI4 AI3 AI2 AI1 COM COM DI2 DI1 COM · R120 CANH CANL GND RGND D+ D- · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1]*

#### **Connection diagrams**

###### **Fi** **g ure 11: EKE 1A connection overview**

*[Figurtekst: Master controller Optional · MMIGRS2 Display · CAN RJ · 080G0294 (optional) · C · *Note; IF Dl1(ON/Off) · Pressure Transmitter switch is not used it · Ratiometric 0.5 – 4.5 V AKS cable must be turned off in · connection Dl1 parameter · 1 060G1034 configuration MMIMYK · 3 Gateway · 2 · e.g.  AKS 32R CAN RJ · CAN RJ CAN  KoolProg PC tool · Superheat controller · EKE 1A - 080G5300 · C1 NC1 · Power · Power supply · 24 V AC± 20% – 24 V DC± 20% + C1 NO1 · + 18 V Relay Power · T2.5 Afuse backupBatt Normally open ornormally closed · (optional) (optional) (optional) · ETS 6 / ETS 8M solenoidON/OFF Alarm · Bipolar valves valve · ETS / KVS · Colibri ® · CCMT / CTR valve · DI2 COM NTC (S2) DI3 CANbus · DI1 (ON/OFF)* AI4 (voltage) 080G0075 (opt.) · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · Danfoss 80G311.10 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ +/~+/~ GND Bat+ A1 A2 B1 B2 NO1NO1 C1C1 NC1NC1 · orange yellow red black · white black red green]*

Table 8: EKE 1A p inout

*[Figurtekst: COM Common · DI3 Digital input 3 Software configurable DI · AI2 Analog input NTC 10K S2 · AI3 Analog inputs 0 – 5 V / Ratiometric pressure transmit- Pe · ter · AI4 analog inputs 0 – 10 V External Reference signal · COM Common · DI1 Digital input 1 Main switch (hardware) · DI2/3 Digital input 2 and 3 Software configurable DI · 5V+ Power output for Ratiometric pressure transmitter 0 – · 5V · COM Common]*

 NOTE: If Dl1(On/Off) switch is not used it must be short circuited

###### Fi g ure 12: EKE 1B connection overview

*[Figurtekst: Master controller · MMIGRS2 Display · MODBus · CAN RJ · 080G0294 (optional) · Supervisor EKE · network MMIMYK · AKS Cable  Gateway · connection · 060G1034 · 1 · 3 · 2 · Pressure transmitter CAN RJ · e.g. AKS 32R · KoolProg · CAN RJ PC tool · used it must be short circuited · Superheat controller · EKE 1B - 080G5350 · C1 NC1 · Power · Power supply · 24 V AC± 20% – 24 V DC± 20% + C1 NO1 · 18 V · + Relay Power · (optional)T fuse2.5 A (optional)backupBatt Normally open ornormally closed(optional) · ETS 6 / ETS 8M ON/OFF Alarm · Bipolar valves solenoid · valve · ETS / KVS · Colibri ® · CCMT / CTR valve · MODBus · DI2 COM NTC (S2)  Optional · NTC (S3/S4) CANBus · DI1 (ON/OFF)* AI4 (0 / 10 V) 080G0075 (opt.) · D+ D- RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · D+ D- RGND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · Danfoss 80G318.10 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ +/~+/~ GND Bat+ A1 A2 B1 B2 NO1NO1 C1C1 NC1NC1 · orange yellow red black · white black red green]*

Table 9: EKE 1B p inout

*[Figurtekst: COM Common · AI Analog inputs NTC 10K S3/S4 selectable via software · AI2 Analog input NTC 10K S2 · AI3 Analog inputs 0 – 5 V / Ratiometric pressure transmit- Pe · ter · AI4 analog inputs 0 – 10 V External Reference signal · COM Common · DI1 Digital input 1 Main switch (hardware) · DI2/3 Digital input 2 and 3 Software configurable DI · 5V+ Power output for Ratiometric pressure transmitter 0 – · 5V · COM Common]*

 NOTE: If Dl1(On/Off) switch is not used it must be short circuited

###### Fi g ure 13: EKE 1C - Front board connection overview

*[Figurtekst: Master controller · *  Note : If Dl1(On/Off) switch · is not used it must be short · circuited · Pressure Transmitter · Ratiometric 0.5 – 4.5 V AKS cable · connection · 1 060G1034 · 3 C C C · 2 · e.g.  AKS 32R · Superheat controller Superheat controller · EKE 1C - 080G5400 · CAN RJ · CAN RJ · CANBus Local network CAN RJ RS485 RTU MODBus · EKE /  supervisor · master  network · controller · MMIGRS display MMIMYK KoolProg · 080G0294 (optional) Gateway PC tool · NTC S3/S4 (optional) AI4 (V/I) COM DI2* COM · (Optional) DI1 (ON/OFF) · NTC/PT 1000 (S2) NTC/PT 1000 (S3/S4) · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · 15V+ 5V+ COM AI5 AI4 AI3 AI2 AI1 COM COM DI2 DI1 COM · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · 15V+ 5V+ COM AI5 AI4 AI3 AI2 AI1 COM COM DI2 DI1 COM · R120 CANH CANL GND RGND D+ D- · Danfoss  80G315.10 · R120 CANH CANL GND RGND D+ D- · CANBus · 080G0075 (optional)]*

Table 10: EKE 1C p inout

|COM|Common||
|---|---|---|
|AI1|Analog inputs temperature NTC 10K / PT1000|S3/S4 selectable via software|
|AI2|Analog inputs temperature NTC 10K / PT1000|S2|
|AI3|Analog inputs voltage / current|Pe|
|AI4|Analog inputs voltage / current|Ext. Ref. or Pc|
|AI5|Analog inputs NTC temperature|S3/S4 selectable via software|
|COM|Common||
|5V+|Power outputs for Ratiometeric pressure transmitter 0<br>– 5V||
|15V+|Power output for current signal pressure transmitter||
|DI1|Digital input 1|Main switch (hardware)|
|DI2|Digital input 2|SoftwareconfigurableDI|
|24V+|Not used in EKE 1C||
|AO1|Not used in EKE 1C||

 NOTE:

If Dl1(On/Off) switch is not used it must be short circuited

###### Fi g ure 14: EKE 1C - Back board connection overview

*[Figurtekst: Superheat controller Superheat controller · EKE 1C - 080G5400 · C1 NO1 · Power · p ower su– pp l y + C1 NC1 · 18 V · + · 24 V AC 24 V DC 2.5 A batt Normally open orAlarm Relay Power · ± 20% ± 20% T fuse backup normally closed · (optional) (optional) (optional) · ETS 6 / ETS 8M ON/OFF Alarm · Bipolar valves solenoidvalve · ETS / KVS · Colibri ® · CCMT / CTR valve · Danfoss 80G316.10 · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ /~/~ + GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · orange yellow red black · white black red green]*

Different types of 4 - 20 mA pressure Transmitters need different supply levels. Check the guide bellow

Table 11: EKE 1C p ressure transmitters ran g e

|User selection EKE connection|Signal|EKE Connection|
|---|---|---|
|Notdefined|-|-|
|AKS 32R|Ratiometric 10-90%|5V supply from EKE|
|112CP (Sensata)|Ratiometric 10-90%|5V supply from EKE|
|OEM Ratio|Definedby parameters|5V supply from EKE|
|NSK (Saginomiya)|Ratiometric 10-90%, 0.5 to 4.5V|5V supply from EKE|
|AKS 32 1-5V|1-5V|15V supply from EKE|
|OEM Voltage|Definedby parameters|15V supply from EKE|
|Bus shared|Via RS485 Modbus|-|
|AKS 32 1-6V|1-6V|15V supply from EKE|
|AKS 32 0-10V|0-10v|15V supply from EKE|
|AKS 33|4-20mA|15V supply from EKE|
|XSK (Saginomiya)|4-20mA|15V supply from EKE|
|OEM Current|Definedby parameters|15V supply from EKE|

 NOTE:

EKE 1A/1B/1D only support ratiometric 0.5 to 4.5V pressure transmitter

###### Fi g ure 15: Connection for 4 - 20 mA

###### Fi g ure 16: EKE 1D connection overview

*[Figurtekst: Master controller · MMIGRS2 Display · CANBus · CAN RJ · 080G0294 (optional) · Supervisor EKE · network MMIMYK · AKS Cable  Gateway · connection · 060G1034 · 1 · 3 · 2 · Pressure transmitter CAN RJ · e.g. AKS 32R · KoolProg · CAN RJ PC tool · used it must be short circuited · Superheat controller · EKE 1D - 080G5360 · C1 NC1 · Power · Power supply · 24 V AC± 20% – 24 V DC± 20% + C1 NO1 · 18 V · + Relay Power · (optional)T fuse2.5 A (optional)backupBatt Normally open ornormally closed(optional) · ETS 6 / ETS 8M ON/OFF Alarm · Bipolar valves solenoid · valve · ETS / KVS · Colibri ® · CCMT / CTR valve · CANBus · DI2 COM NTC (S2)  Optional · NTC (S3/S4) CANBus · DI1 (ON/OFF)* AI4 (0 / 10 V) 080G0075 (opt.) · L H GND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · L H GND COM 5V+ DI2 DI1 COM AI4 AI3 AI2 D I A 13 COM · Danfoss 80G318.10 –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1 · –/~–/~ +/~+/~ GND Bat+ A1 A2 B1 B2 NO1NO1 C1C1 NC1NC1 · orange yellow red black · white black red green]*

Table 12: EKE 1D p inout

|COM|Common||
|---|---|---|
|AI|Analog inputs NTC 10K|S3/S4 selectable via software|
|AI2|Analog input NTC 10K|S2|
|AI3|Analog inputs 0 – 5 V / Ratiometric pressure transmit-<br>ter|Pe|
|AI4|analog inputs 0 – 10 V|External Reference signal|
|COM|Common||
|DI1|Digital input 1|Main switch (hardware)|
|DI2/3|Digital input 2 and 3|SoftwareconfigurableDI|
|5V+|Power output for Ratiometric pressure transmitter 0 –<br>5V||
|COM|Common||

#### Mounting

DIN rail mounting / demounting. The unit can be mounted onto a 35 mm DIN rail simply by snapping it into place and securing it with a stopper to prevent sliding. It is demounted by gently pulling the stirrup located in the base of the housing

*[Figurtekst: Fi g ure 17: Mountin g Fi g ure 18: De-mountin g · 1 · 2 · “Click” 3]*

#### User interface

#### Koolprog software tool

KoolProg is a software tool that can configure the EKE Controllers in fast and easy way

The main features of the KoolProg are listed as follows

- Make Online changes to parameter configurations

- Monitor live status of inputs and outputs

- Quickly analyze controller behavior. and program patterns by using the graphical trending tool. KoolProg Software is available for download free of charge at http://koolprog.danfoss.com. The customer will first be guided through a registration process before download can commence

 NOTE:

For updated EKE software versions it is required to install the latest KoolProg software versions to have the full compatibility To guarantee a reliable USB connection to a host device (e.g. industrial PC), you must: keep USB cable length < 1 m. Kool Prog software do not support multiple EKE controllers in a daisy chain network. EKE must be powered up before starting programming. The user must make the program for EKE based on the product version and software version. EKE will not be programmed correctly if uploaded program with wrong version

- Create your own configuration files on your PC without • Quickly program one. or multiple controllers • Quickly analyze controller behavior and program having to connect a controller by using the progress and completion status patterns by using the graphical trending tool

- • Import a parameter configuration file to your PC from a indicators • Make Online changes to parameter configurations connected controller. Save the file and download it to • Monitor live status of inputs and outputs other controllers of the same model

- Select the most frequently used parameters as your favorites

- Find all the technical documentation for each controller model within one location

#### User interface Display MMIGRS2

MMIGRS2 is a remote interface that connects with EKE controller through the CAN RJ or CANbus network. All the information about the user interface is loaded inside the EKE controller; that’s why there is no need of programming the MMIGRS2 interface. MMIGRS2 is powered externally or from the controller which it is connected to and automatically shows its user interface.

*[Figurtekst: Fi g ure 19: MMIGRS2 Dis p la y  connection with EKE Fi g ure 20: MMIGRS2 Main screen · ACCCBI 080G0075 · CAN RJ Up : Adjust requested step position upward · CAN RJ Escape: Leave service mode · Right , Left : Navigate to alarm list, status, · controller info · Enter short press: start edit of requested · position/accept change · MMIGRS2 Enter press for 2 sec: change valve selection · UP and Down together: set actual step · position to 0 step · Superheat controller · EKE 1A - 080G5300 Homescreen Navigation help · RJ CAN connector · Controller name  Alarm indicator · Termination Jumper  between R and H Reference point · For cable >3m (only EKE 1C)  Primary readout · 2-way screw connector for · power supply 4-way screw connector for CANbus network  Operating statusEvap. temperature S2 – S4 · Evap. pressure Media · Valve OD temperature · COM 5V+ DI2 DI1 COM AI4 AI3 AI2 DI3 COM · Danfoss 34G306.10 · Danfoss  80G313.10 · –/~ +/~ GND Bat+ A1 A2 B1 B2 NO1 C1 NC1]*

On the main screen the following data are displayed:

- the main analog inputs measurements or other information

- the icon indicating if unit is operating in superheat mode or temperature mode

- shows the status of the controller

- the alarm or service icon

######  NOTE:

When MMI is not connected to EKE via telephone cable the autodetection feature of the EKE CAN address will not work. Therefore check the following MMIGRS2 setting: 1) enter BIOS menu pressing and holding X + Enter keys for 5 s 2) select “MCXselection”->” Manual Mode” and set the CAN address of the EKE you wish to connect to.

######  NOTE:

To use EKE 1x controllers with MMI using RJ 12 cable, The CAN R and H terminals behind MMI should be shorted. If CAN wired connections are used, the first and the last node in the CAN connection should be terminated using 120ohm resistor

#### Operation System Master

EKE 1x superheat controller can be interfaced with a System Master the over the network or via analog or digital signals. The master could be e.g., a Danfoss MCX controller or a PLC system

Fi g ure 21: EKE controller o p eration with s y stem master

*[Figurtekst: Danfoss  Master  PLC · MMIGRS 2 Controller · Modbus RTU over RS485 wired · KoolProg EKE 1D EKE 1C EKE 1B EKE 1A · PC Tool Connected  Connected  Connected  No network · via CAN or  via CAN or  via MODbus  possible · MODbus MODbus only · Danfoss  MMIMYK USB to  Service port CAN-RJ12 (point to point connection only). · CAN converter connects to  Either MMIGRS2 or KoolProg PC Tool (via MMIMYK gateway) · the service port of EKE 1A,  can be connected to the RJ12 connector. · EKE 1B and EKE 1C. · Danfoss  80G8212.10 · Analog signal (main switch,  ext.  reference, alarm outputs etc.)]*

#### Alarms

Table 13: Alarms

|Label|Alarm name<br> i|Modbus PNU|Bit number|Can Index|Can Subindex|Bit number|
|---|---|---|---|---|---|---|
|E100|Valveconfiguration<br>error|1901|8|5507|6C|0|
|E101|Configurationerror|1901|9|5507|6C|1|
|E102|Sensor supply over-<br>load|1901|10|5507|6C|2|
|E024|S2 suction pipe sen-<br>sor error|1901|11|5507|6C|3|
|E025|S3 media inlet sensor<br>error|1901|12|5507|6C|4|
|E026|S4 media outlet sen-<br>sor error|1901|13|5507|6C|5|
|E020|Pe evaporator trans-<br>mitter error|1901|14|5507|6C|6|
|E121|Pc condenser trans-<br>mitter error|1901|15|5507|6C|7|
|E019|External reference sig-<br>nal alarm|1901|0|5507|6C|8|
|E011|No refrigerant selec-<br>ted|1901|1|5507|6C|9|
|E103|No valveconfigured|1901|2|5507|6C|10|
|E122|Shared signal timeout|1901|3|5507|6C|11|
|E128|Ext. ref. signal timeout|1901|4|5507|6C|12|
|A997|Battery critical low<br>voltage|1901|5|5507|6C|13|
|A996|Battery too high volt-<br>age|1901|6|5507|6C|14|
|W001|Battery low voltage|1901|7|5507|6C|15|
|A994|Low S4 media outlet<br>temperature|1902|8|5507|6C|16|
|A993|High temperature|1902|9|5507|6C|17|
|A992|Low temperature|1902|10|5507|6C|18|
|A991|High evaporation<br>pressure (MOP)|1902|11|5507|6C|19|
|A990|Low evaporation pres-<br>sure (LOP)|1902|12|5507|6C|20|
|A989|High condensing tem-<br>perature|1902|13|5507|6C|21|
|A988|High superheat|1902|14|5507|6C|22|
|A987|Low superheat|1902|15|5507|6C|23|
|A986|Lack of valve capacity|1902|0|5507|6C|24|
|W002|Standby mode|1902|1|5507|6C|25|
|W003|Manual control|1902|2|5507|6C|26|
|E104|SH reference too close<br>to SH close setpoint|1902|3|5507|6C|27|
|E105|LOP setpoint too close<br>to MOP setpoint|1902|4|5507|6C|28|
|E129|No sensorconfigured<br>for S4|1902|5|5507|6C|29|
|E106|No sensorconfigured<br>for S3|1902|6|5507|6C|30|
|E107|SH min higher than<br>SH max|1902|7|5507|6C|31|
|E108|OD min higher than<br>OD max|1903|8|5507|6E|0|
|E109|No transmitterconfig-<br>uredfor Pc|1903|9|5507|6E|1|
|E114|Check valve step<br>mode vs positioning|1903|10|5507|6E|2|
|E115|Valve speed too fast|1903|11|5507|6E|3|
|E116|Valve speed too slow|1903|12|5507|6E|4|

|Label<br>E117|Alarm name<br>Valve emergency<br>speed too fast|Modbus PNU<br>1903|Bit number<br>13|Can Index<br>5507|Can Subindex<br>6E|Bit number<br>5|
|---|---|---|---|---|---|---|
|E118|Valve emergency<br>speed too slow|1903|14|5507|6E|6|
|E119|Valve start speed too<br>slow|1903|15|5507|6E|7|
|A999|DI1 unstable input|1903|0|5507|6E|8|
|A998|DI2 unstable input|1903|1|5507|6E|9|
|A983|DI3 unstable input|1903|2|5507|6E|10|
|E125|AI5 cant operate with<br>AKS sensor|1903|4|5507|6E|12|
|E126|Valve short circuit or<br>driver too hot|1903|5|5507|6E|13|
|A982|Thermostatic signal<br>missing|1903|6|5507|6E|14|
|A981|SH control signal<br>missing|1903|7|5507|6E|15|
|E123|Low supply voltage|1904|8|5507|6E|16|
|E132|No sensorconfigured<br>for S2|1904|9|5507|6E|17|
|E133|No transmitterconfig-<br>uredfor Pe|1904|10|5507|6E|18|
|E134|Ext. refconfiguration<br>error|1904|11|5507|6E|19|
|E135|DI H/C cant operate<br>with the thermostat|1904|12|5507|6E|20|
|A984|PWR Backup module<br>failure|1904|13|5507|6E|21|
|A985|Replace PWR Backup<br>module|1904|14|5507|6E|22|

#### Ordering

Table 14: Product p art numbers

|Description|Pack format|CodeNo.|
|---|---|---|
|Electronic controller EKE 1A|Single pack|080G5300|
|Electronic controller EKE 1B|Single pack|080G5350|
|Electronic controller EKE 1C|Single pack|080G5400|
|Electronic controller EKE 1D|Single pack|080G5360|

Table 15: Accessories p art numbers

|Description|Pack format|CodeNo.|
|---|---|---|
|MMIGRS2 Remote Display|Single pack|080G0294|
|MMIMYK gateway|Single pack|080G0073|
|ACCCBI telephone cable user interface connector 1.5|Single pack|080G0075|
|m|||
|Backup power module, EKE 2U|Single pack|080G5555|
|Power supply, AK-PS 063 STEP3|Single pack|080Z0057|
|Power supply, AK-PS 130 STEP3|Single pack|080Z0058|
|Power supply, AK-PS 250 STEP3|Single pack|080Z0059|

#### **Certificates,** declarations, and approvals

The list contains all certificates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

Some approvals may change over time. You can check the most current status at danfoss.com or contact your local Danfoss representative if you have any questions.

Table 16: Valid a pp rovals

*[Figurtekst: File name Document type Document topic Approval authority · EMC directive 2014/30/EU: · EN61000-6-3: 2007 +A1: 2011 · EN61000-6-2: 2005 · 080R4003.01 EU Declaration of conformity LVD directive 2014/35/EU: Danfoss · EN60730-1: 2011 · EN60730-2-9: 2010 · RoHS directive 2011/65/EU]*

Table 17: A pp rovals

#### Online support

Danfoss offers a wide range of support along with our products, including digital product information, software, mobile apps, and expert guidance. See the possibilities below.

###### The Danfoss Product Store

The Danfoss Product Store is your one-stop shop for everything product related—no matter where you are in the world or what area of the cooling industry you work in. Get quick access to essential information like product specs, code numbers, technical documentation, certifications, accessories, and more.

Start browsing at store.danfoss.com.

###### Find technical documentation

Find the technical documentation you need to get your project up and running. Get direct access to our official collection of data sheets, certificates and declarations, manuals and guides, 3D models and drawings, case stories, brochures, and much more.

Start searching now at www.danfoss.com/en/service-and-support/documentation.

Danfoss Learning is a free online learning platform. It features courses and materials specifically designed to help engineers, installers, service technicians, and wholesalers better understand the products, applications, industry topics, and trends that will help you do your job better.

Create your Danfoss Learning account for free at www.danfoss.com/en/service-and-support/learning.

###### Get local information and support

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest regional news, or connect with a nearby expert—all in your own language.

Find your local Danfoss website here: www.danfoss.com/en/choose-region.
