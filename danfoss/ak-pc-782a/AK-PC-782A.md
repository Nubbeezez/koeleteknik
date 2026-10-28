# Danfoss AK-PC 782A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.

## Indhold

1. AK-PC 782A – User Guide (SW 4.3x, engelsk) – Pack controller / kapacitetsregulator til transkritisk CO2 booster-anlæg. Funktioner, parametre, alarmer, ledningsdiagrammer.
2. Strategy for heat recovery on CO2 transcritical rack – Programming Guide (engelsk) – Strategi og opsætning af varmegenvinding på CO2-transkritisk anlæg med pack controller.
3. Sharing a ratiometric pressure transmitter between controllers – Operating Guide (engelsk) – Om ét ratiometrisk tryktransmitter-signal kan deles mellem flere Danfoss-regulatorer.

---

## 1. AK-PC 782A – User Guide (SW 4.3x, engelsk)

*Kilde: Danfoss-dokument BC245386497365en-001201. Pack controller / kapacitetsregulator til transkritisk CO2 booster-anlæg. Funktioner, parametre, alarmer, ledningsdiagrammer.*

#### **User Guide**

Pack controller Type **AK-PC 782A**

Capacity controller for transcritical CO2 booster control **SW Ver. 4.3x**

**www.danfoss.com**

### **1. Introduction**

### **1.1 Application**

SW = 4.3x

AK-PC 782A are complete regulating units for capacity control of compressors and condensers in a transcritical CO2 booster system with parallel compressor.  The controller is with oil management, heat recovery function and CO2 gas pressure control.

In addition to capacity control, the controllers can give signals to other controllers about the operating condition, e.g. forced closing of expansion valves, alarm signals and alarm messages. The controller’s main function is to control compressors and condensers so that operation all the time takes place at the energy-optimum pressure conditions. Both suction pressure and condensing pressure are controlled by signals from pressure transmitters.

Capacity control must be carried out by suction pressure P0. (The P0 signal for the parallel compressor is supplied by the pressure transmitter on the receiver).

*[Figurtekst: Traditional capacity control]*

Among the different functions are:

- Capacity control of up to 10 compressors on MT and 8 on IT

- Capacity control of up to 4 compressors on LT

- Up to 3 unloaders for each compressor

- Control of oil separator and oil receiver

- Speed control of one or two compressors in each group

- Up to 6 safety inputs for each compressor

- Option for capacity limitation to minimize consumption peaks

- If the compressor does not start, signals can be transmitted to other controllers so that the electronic expansion valves will be closed

- Regulation of liquid injection into suction line

- Safety monitoring of high pressure / low pressure / discharge temperature

- Capacity control of up to 8 fans

- Floating reference with regard to outside temperature

- Heat recovery function

- CO2 gas cooler control  and receiver control

- Ejector regulation: HP, LE (liquid)

- Safety monitoring of fans

- The status of the outputs and inputs is shown by means of lightemitting diodes on the front panel

- Alarm signals can be generated via data communication

- Alarms are shown with texts so that the cause of the alarm is easy to see.

- Plus some completely separate functions that are totally independent of the regulation – such as alarm, thermostat, pressure and PI-regulating functions.

Heat recovery functions, controlling the condensing pressure and receiver pressure

### **1.2 Principles**

The great advantage of this series of controllers is that it can be extended as the size of the plant is increased. It has been developed for refrigeration control systems, but not for any specific application – variation is created through the read-in software and the way you choose to define the connections. The same modules that are used for each regulation and the composition can be changed, as required. With these modules (building blocks) it is possible to create a multitude of various kinds of regulations. But it is you who must help adjusting the regulation to the actual needs – these instructions will assist you to find your way through all the questions so that the regulation can be defined and the connections made.

##### **Advantages**

- The controller’s size can “grow” as systems grow

- The software can be set for one or more regulations

- Several regulations with the same components

- Extension-friendly when systems' requirements are changed

- Flexible concept:

- Controller series with common construction

- One principle – many regulation uses

- modules are selected for the actual connection requirements

- The same modules are used from regulation to regulation

*[Figurtekst: Extension modules · Controller · Top part · Bottom part · The controller is the cornerstone of the regulation. The module has  If the system grows and more functions have to be controlled, the · inputs and outputs capable of handling small systems. regulation can be extended. · • The bottom part – and hence the terminals – are the same for all  With extra modules more signals can be received and more relays cut in · controller types. and out – how many of them – and which – is determined by the relevant · • The top part contains the intelligence with software. This unit will vary  application. · according to controller type. But it will always be supplied together · with the bottom part. · • In addition to the software, the top part is provided with connections · for data communication and address setting. · Examples A regulation with few connections  If there are many connections, one or more · can be performed with the controller  extension modules have to be mounted. · module alone.]*

##### **Direct connection**

Setup and operation of an AK controller must be accomplished via the “AK-Service Tool” software program. The program is installed on a PC, set up and operation of the various functions is carried out via the controller’s menu displays.

##### **Displays**

The menu displays are dynamic, so that different settings in one menu will result in different setting possibilities in other menus. A simple application with few connections will give a set-up with few settings.

A corresponding application with many connections will give a set-up with many settings.

From the overview display there is access to further displays for the compressor regulation and the condenser regulation. At the bottom of the display there is access to a number of general functions, such as “time table”, “manual operation”, “log function”, “alarms”, and “service” (configuration).

##### **Network linking**

The controller can be linked up to a network together with other controllers in an ADAP-KOOL® refrigeration control system. After the set-up, operation can be performed at a distance with e.g. our software program type AKM.

##### **Users**

The controller comes supplied with several languages, one of which can be selected and employed by the user. If there are several users, they may each have their choice of language. All users must be assigned a user profile which either gives access to full operation or gradually limits the operation to the lowest level that only allows you “to see”.

Language selection is part of the Service Tool settings. If the language selection is not available in the Service Tool for the current regulator, English texts will be displayed.

##### **External display**

An external display can be fitted in order for P0 (Suction) and Pc (Condensing) readings to be displayed.

A total of 4 displays can be fitted and with one setting it is possible to choose between the following readings: suction pressure, suction pressure in temperature, Ss, Sd, condenser pressure, condenser pressure in temperature, S7 gas cooler temperature, hot tap water at heat recovery and heat exchanger temperature at heat recovery.

A graphical display with control buttons can also be fitted.

A number of light-emitting diodes makes it possible to follow the signals that are received and transmitted by the controller.

##### **Log**

From the log function you can define the measurements you wish to be shown.

The collected values can be printed, or you may export them to a file. You can open the file in Excel.

If you are in a service situation, you can show measurements in a trend function. The measurements are then made real-time and displayed instantly.

##### **Alarm**

The display gives you an overview of all active alarms. If you wish to confirm that you have seen the alarm you can cross it off in the acknowledge field.

If you want to know more about a current alarm you can click on it and obtain an information display on the screen.

A corresponding display exists for all earlier alarms. Here you can upload information if you need further details about the alarm history.

*[Figurtekst: n Power Slow flash = OK · n Comm Quick flash = answer from gateway · n DO1  n Status Constantly ON = error · n DO2  n Service Tool Constantly OFF = error · n DO3  n LON · n DO4  n I/O Extension · n DO5  n Alarm Flash = active alarm/not cancelled · n DO6 Constant ON = Active alarm/cancelled · n DO7  n Display · n DO8  n Service Pin]*

### **2. Design of a controller**

This section describes how the controller is designed. The controller in the system is based on a uniform connection platform where any deviations from regulation to regulation is determined by the used top part with a specific software and which input and output signals the relevant application will require. If it is an application with few connections, the controller

module (top part with belonging bottom part) may be sufficient. If it is an application with many connections, it will be necessary to use the controller module plus one or more extension modules. This section will give you a survey of possible connections plus assistance in selecting the modules required by your actual application.

### **2.1 Module survey**

**Controller module** – capable of handling minor plant requirements.

##### **Extension modules**

When the complexity becomes greater and additional inputs or outputs are required, modules can be attached to the controller. A plug on the side of the module will transmit the supply voltage and data communication between the modules.

##### **Top part**

The upper part of the controller module contains the intelligence. This is the unit where the regulation is defined and where data communication is connected to other controllers in a bigger network.

##### **Optional connection**

When a regulation is planned (set up), it will generate a need for a number of connections distributed on the mentioned types. This connection must then be made on either the controller module or an extension module. The only thing to be observed is that the types must not be mixed (an analogue input signal must for instance not be connected to a digital input).

##### **Programming of connections**

The controller must know where you connect the individual input and output signals. This takes place in a later configuration where each individual connection is defined based on the following principle:

- to which module?

##### **Connection types**

There are various types of inputs and outputs. One type may, for example, receive signals from sensors and switches. Another may receive a voltage signal, and a third type may be outputs with relays etc. The individual types are shown in the table below.

- at which point (”terminals”)?

- what is connected (e.g. pressure transmitter/type/pressure range)?

*[Figurtekst: Extension module with additional · relay outputs and additional · analogue inputs. · Extension module with · additional analogue inputs · External display for · suction pressure etc. · Bottom part · Controller with analogue inputs · and relay outputs. · Top part The module with additional relay outputs is · also available in a version where the top part · is provided with change-over switches so · that the relays can be overridden. · Extension module with · 2x analogue output signals · If the row of modules needs to · be interrupted due to length or · external positioning, a communi- · cation module should be used.]*

|1. Controller|||
|---|---|---|
|**Type**|**Function**|**Application**|
||Controller for capacity control of MT (10 compressors), IT (8 compressors) and|Transcritical CO2 booster control, parallel|
|AK-PC 782A|LT (4 compressors).<br>Up to 3 unloaders per compressor, 8 fans and max. 220 inputs/outputs.|compression / Oil management  / Heat recovery<br>/ CO2 gas pressure|

|2. Extension m|<br>odules and surveyof|**f**<br>inputs and|**f**<br>outputs|**f**|**f**||||
|---|---|---|---|---|---|---|---|---|
|**Type**|**Analogue**<br>**inputs**|**On/Off out**|**f puts**|**On/off suppl**<br>**(DI signal)**|**f y voltage**|**Analogue**<br>**outputs**|**Stepper**<br>**output**|**Module with**<br>**switches**|
||For sensors,<br>pressure<br>transmitters etc.|Relay<br>(SPDT)|Solid state|Low voltage<br>(max. 80 V)|High voltage<br>(max. 260 V)|0 – 10 V DC|For valves<br>with step<br>control|For override of<br>relay outputs|
|Controller|11|4|4|-|-|-||-|
|Extension mod|ules||||||||
|AK-XM 101A|8||||||||
|AK-XM 102A||||8|||||
|AK-XM 102B|||||8||||
|AK-XM 103A|4|||||4|||
|AK-XM 204A||8|||||||
|AK-XM 204B||8||||||x|
|AK-XM 205A|8|8|||||||
|AK-XM 205B|8|8||||||x|
|AK-XM 208C|8||||||4||
|<br>The following e<br>There is onlyro|xtension module can<br>om for one module.|be placed on|the PC board in t|he controller mod|ule.||||
|AK-OB 110||||||2|||

##### 3. AK operation and accessories

|**Type**|**Function**|**Application**|
|---|---|---|
|**Operation**|||
|AK-ST 500|Software for operation of AK controllers|AK-operation|
|-|Cable between PC and AK controller|USB A-B(Standard IT cable)|
|**Accessories**|**Power supply module 24 V DC**||
|AK-PS 063 STEP3|15 VA||
|AK-PS 130 STEP3|30 VA|Supply for controller|
|AK-PS 250 STEP3|60 VA||
|**Accessories**|**External display that can be connected to the controller mod**|**ule. For showing e.g. the suctionpressure**|
|EKA 163A|Display||
|EKA 164A|Display with operation buttons||
|MMIGRS2|Graphic display with operation||
||Cable between EKA display and controller|Length = 2 m, 6 m|
|-|Cable between graphic display and controller|Length = 1.5 m, 3.0 m|
|**Accessories**|**Communication modules for controllers where modules cann**|**ot be connected continuously**|
|AK-CM 102|Communication module|Data communication for external extension<br>modules|

On the following pages there is data specific to each module.

### **2.2 Common data for modules**

|Supplyvoltage|24 V DC/AC  ±20%||
|---|---|---|
|Power consumption|AK-__ (controller)|8 VA|
||AK-XM 101, 102, 103, 107, AK-CM 102|2 VA|
||AK-XM 204, 205, 208|5 VA|
|Analogue inputs|Pt 1000 ohm /0 °C|Resolution: 0.1 °C<br>Accuracy: ±0.5 °C<br>±0.5 °C between -50 °C and 50 °C<br>±1 °C between -100 °C and -50 °C<br>±1 °C between 50 °C and 130 °C|
||Pressure transmitter type AKS 32R / AKS 2050<br>MBS 2050 / AKS 32 (1 – 5 V)|Resolution:1 mV<br>Accuracy +/- 10 mV|
||Other pressure transmitter:<br>Ratiometric signal<br>Min. and Max.pressure must be set|Max. connection of 5 pressure transmitters on one<br>module|
||Voltage signal 0 – 10 V||
||Contact function (On/Off)|On at R < 20 ohm<br>Off at R > 2K ohm<br>(Gold-plated contacts not necessary)|
|Analogue outputs|0 – 10 V|Accuracy+/- 100 mV|
|On/off supply voltage inputs|Low voltage<br>0 / 80 V AC/DC|Off: U < 2 V<br>On: U > 10 V|
||High voltage<br>0 / 260 V AC|Off: U < 24 V<br>On: U > 80 V|
|Relay outputs|AC-1(ohmic)|4 A|
|SPDT|AC-15(inductive)|3 A|
||U|Min. 24 V<br>Max. 230 V<br>Low and high voltage must not be connected to the<br>same outputgroup|
|Solid state outputs|Can be used for loads that are cut in and out<br>frequently,<br>e.g. Ejector valves, Oil valves, fans and AKV valves|Max. 240 V AC, Min. 48 V AC<br>Max. 0,5 A,<br>Leak < 1 mA<br>Max. 1 AKV|
|Stepper outputs|Used for valves with stepper input|20 – 500 step/s<br>Separate supplyto  stepper outputs : 24 AC/DC|
|Ambient temperature|Duringtransport|-40 – 70 °C|
||During operation|-20 – 55 °C ,<br>0 – 95% RH (non condensing)<br>No shock influences / vibrations|
|Enclosure|Material|PC / ABS|
||Class|IP10,VBG 4|
||Mounting|For mountingonpanel wall or DIN rail|
|Weight with screw terminals|Modules in 100- / 200- / controller-series|Ca. 200 g / 500 g / 600 g|
|Approvals|EU low voltage directive and EMC requirements<br>are complied with|LVD tested according to EN 60730<br>EMC tested<br>Immunity according to EN 61000-6-2<br>Emission according to EN 61000-6-3|
|||E31024 for PC-module|
|||E357029 for XM and CM-modules|

The mentioned data applies to all modules.

If data is specific, this is mentioned together with the module in question.

##### **Dimensions**

The module dimension is 72 mm. Modules in the 100-series consist of one module. Modules in the 200-series consist of two modules. Controllers consist of three modules. The length of an aggregate unit = n x 72 + 8

### **2.3 Controller**

There are several controllers in the series. The function is determined by the programmed software, but on the outside the controllers are identical – they all have the same connection possibilities:

11 analogue inputs for sensors, pressure transmitters, voltage signals and contact signals.

8 digital outputs, with 4 Solid state outputs and 4 relay outputs.

24 V AC or DC to be connected to the controller.

The 24 V must **not** be retransmitted and used by other controllers as it is not galvanically separated from inputs and outputs. In other words, you **must** use a transformer for each controller. Class II is required. The terminals must **not** be earthed. The supply voltage to any extension module is transmitted via the plug on the right-hand side.

The size of the transformer is determined by the power requirement of the total number of modules.

The supply voltage to a pressure transmitter can be taken either from the 5 V output or from the 12 V output depending on transmitter type.

##### **Data communication**

If the controller is to be included in a system, communication must take place via the LON connection.

The installation has to be made as mentioned in the separate instructions for LON communication.

##### **Address setting**

If it is a system manager AK-SM .., then 1-999

##### **Service PIN**

When the controller is connected to the data communication cable, the gateway must have knowledge of the new controller. This is obtained by pushing the key PIN. The LED “Status” will flash when the gateway sends an acceptance message.

##### **Operation**

The configuration operation of the controller must take place from the software program “Service Tool”. The program must be installed on a PC, and the PC must be connected to the controller via the USB-B plug on the front of the unit.

There are two rows with LEDs indicating: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

Right row:

- Software status (slow flash = OK)

- Communication with Service Tool

*[Figurtekst: 24 V · OK · 24 V · PIN · Address · Keep the safety distance! · Low and high voltage must · not be connected to the · same output group · n Power Slow flash = OK · n Comm Quick flash = answer from gateway · n DO1  n Status Constantly ON = error · n DO2  n Service Tool Constantly OFF = error · n DO3  n LON · n DO4  n I/O Extension · n DO5  n Alarm Flash = active alarm/not cancelled · n DO6 Constant ON = Active alarm/cancelled · n DO7  n Display · n DO8  n Service Pin]*

A small module (option board) can be placed on the bottom part of the controller. The module is described later in the document.

- Communication on LON

- Communication with AK-CM 102

- Alarm when LED flashes

- 1 LED that is not used

- Communication with display on RJ11 plug

- “Service Pin” switch has been activated

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 9 10 11 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 AI9 AI10 AI11 · Terminal 15 & 27: · 12 V max. 100 mA in total. · Terminal 16 & 28: · 5 V max. 100 mA in total. · Terminal · Analogue  17, 18, 29, 30: · inputs (Cable screen) · on 1 - 11 The screen on the · pressure transmitter · cables must only be · connected at the end of · the controller. · Solid state outputs · on 12 - 15 Relay outputs on · 16 - 19 · Relay or AKV coil · fx 230 V AC 24 and 25 used only · when "Option board  Point 12 13 14 15 16 17 18 19 · fitted"  Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Signal type · S S1 · S2 · SIG · Pt 1000 ohm/0°C Saux_ · SsA Pt 1000 · SdA · GND Shr · Stw · S g c · P · 3: Brown · AKS 32R · 2: Blue P0A AKS 32R / · AKS 2050 · P0B · 1: Black PcA MBS 8250 · -1 - xx bar · PcB · Paux · AKS 32 · AKS 32 3: Brown Pgc -1 - zz bar · Prec · 2: Black Signal Module Point  Terminal Signal t y pe /Active at · 1: Red 1  (AI 1) 1 - 2 · 2  (AI 2) 3 - 4 · U · 0 - 5 V · ... 0 - 10 V 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · 5  (AI 5) 9 - 10 · On/Off Ext. Main  Active at: 6  (AI 6) 11 - 12 · switch Closed 7  (AI 7) 13 - 14 · Day/ · / · Night 8  (AI 8) 19 - 20 · Door Open · Level  9  (AI 9) 21 - 22 · switch · 10  (AI 10) 23 - 24 · DO Active at: · 1 11  (AI 11) 25 - 26 · AKV On 12  (DO 1) 31 - 32 · Comp 1 / · Comp 2 Off 13  (DO 2) 33 - 34 · Fan 1 · Alarm  14  (DO 3) 35 - 36 · Light 15  (DO 4) 37 - 38 · Rail heat · Defrost 16  (DO 5) 39 - 40- 41 · Solenoid · valve 17  (DO6) 42 - 43 - 44 · 18  (DO7) 45 - 46 - 47 · 19  (DO8) 48 - 49 - 50 · Option Board Please see the signal · on the page with the  24  - · module. · 25  - · AKV]*

### **2.3.1 Extension module AK-XM 101A**

The module contains 8 analogue inputs for sensors, pressure transmitters, voltage signals and contact signals.

The supply voltage to the module comes from the previous module in the row. Supply voltage to a pressure transmitter can be taken from either the 5 V output or the 12 V output depending on transmitter type.

Only the two top LEDs are used. They indicate the following:

- Voltage supply to the module

- Communication with the controller is active (red = error)

*[Figurtekst: Point Point 1 2 3 4 · Type AI1 AI2 AI3 AI4 · Terminal 9 & 15: · 12 V max. 100 mA in total. · Terminal 10 & 16: · At the top, the  5 V max. 100 mA in total. · signal input is · the left of the  Terminal · two terminals. 11, 12, 13, 14: · (Cable screen) · The screen on the pressure · transmitter cables must · only be connected at the · At the bottom, · end of the controller. · the signal input · is the right of the · two terminals. · Point 5 6 7 8 · Signal Signal  Type AI5 AI6 AI7 AI8 · type · S S1 · S2 · Pt 1000 ohm/0°C SIG Saux · Pt 1000 · SsA · SdA · GND Shr · Stw · Sgc · P · AKS 32R · 3: Brown · 2: Blue P0A AKS 32R / · P0B AKS 2050 · 1: Black PcA MBS 8250 · PcB -1 - xx bar · AKS 32 Paux · 3: Brown Pgc AKS 32 · Prec -1 - zz bar · 2: Black · 1: Red · U · Signal Module Point Terminal Signal type / · Active at · 0 - 5 V · ... 0 - 10 V 1  (AI 1) 1 - 2 · 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · On/Off Ext.  Active at: 4  (AI 4) 7 - 8 · Main · switch Closed 5  (AI 5) 17 - 18 · Day/ / · Night Open 6  (AI 6) 19 - 20 · Door · Level  7  (AI 7) 21 - 22 · switch · 8  (AI 8) 23 - 24]*

### **2.3.2 Extension module AK-XM 102A / AK-XM 102B**

The module contains 8 inputs for on/off voltage signals.

##### **Signal**

AK-XM 102A is for low voltage signals. AK-XM 102B is for high voltage signals.

The supply voltage to the module comes from the previous module in the row.

They indicate:

- Voltage supply to the module

- Communication with the controller is active (red = error)

- Status of the individual inputs 1 to 8 (when lit = voltage

*[Figurtekst: AK-XM 102A AK-XM 102B · Max. 24 V Max. 230 V · On/Off: On/Off: · On: DI > 10 V AC/DC On: DI > 80 V AC · Off: DI <  2 V AC/DC Off: DI < 24 V AC]*

*[Figurtekst: Point Point 1 2 3 4 · Type DI1 DI2 DI3 DI4 · Point 5 6 7 8 · Type DI5 DI6 DI7 DI8 · Signal Active at · DI Ext. · Main · switch · AK-XM 102A: Max. 24 V · AK-XM 102B: Max. 230 V Day/ Closed · (voltage on) · Night · / · Comp. · safety 1 · Open · (voltage · Comp. · off) · safety 2 · Level · switch · (The module can not register a pulse signal from e.g. a · reset function.)]*

*[Figurtekst: Signal Module Point Terminal Active at · 1  (DI 1) 1 - 2 · 2  (DI 2) 3 - 4 · 3  (DI 3) 5 - 6 · 4  (DI 4) 7 - 8 · 5  (DI 5) 9 - 10 · 6  (DI 6) 11 - 12 · 7  (DI 7) 13 - 14 · 8  (DI 8) 15 - 16]*

### **2.3.3 Extension module AK-XM 103A**

The module contains :

4 analogue inputs for sensors, pressure transmitters, voltage signals and contact signals.

4 analogue voltage outputs of 0 - 10 V

The supply voltage to the module comes from the previous module in the row.

Supply voltage to a pressure transmitter can be taken from either the 5 V output or the 12 V output depending on transmitter type.

##### **Galvanic isolation**

The inputs are galvanically separated from the outlets. The outlets AO1 and AO2 are galvanically separated from AO3 and AO4.

Only the two top LEDs are used. They indicate the following:

• Voltage supply to the module

• Communication with the controller is active (red = error)

##### **Max. load**

I < 2.5 mA R > 4 kΩ

##### **Accuracy**

Analog inputs: +/- 10 mV Analog outputs: +/- 100 mV

*[Figurtekst: Point Point 1 2 3 4 Terminal 9: · Type AI1 AI2 AI3 AI4 12 V max. 100 mA in total. · Terminal 10: · 5 V max. 100 mA in total. · At the top, the  Terminal 11, 12: · signal input is  (Cable screen) · the left of the  The screen on the pressure · two terminals. transmitter cables must only · be connected at the end of the · controller. · Galvanic isolation: · At the bottom,  AI 1-4 ≠ AO 1-2 ≠ AO 3-4 · the signal input · is the right of the · two terminals. · Point 5 6 7 8 · Signal Signal  Type AO1 AO2 AO3 AO4 · type · S S1 · SIG S2 · Pt 1000 ohm/0°C Saux · Pt 1000 · SsA · SdA · GND · Shr · Stw · Sgc · P · AKS 32R · 3: Brown · 2: Blue P0A AKS 32R / · AKS 2050 · 1: Black P0B MBS 8250 · PcA · -1 - xx bar · PcB · AKS 32 Paux · AKS 32 · 3: Brown Pgc -1 - zz bar · Prec · 2: Black · 1: Red · U · Signal Module Point Terminal Signal type /Active at · 0 - 5 V 1  (AI 1) 1 - 2 · ... 0 - 10 V 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · On/Off Ext. Main  Active at: 5  (AO 1) 17 - 18 · switch · Closed 6  (AO 2) 19 - 20 · Day/ / · Night Open 7  (AO 3) 21 - 22 · Door 8  (AO 4) 23 - 24 · Level · switch · AO · 0 – 10 V]*

### **2.3.4 Extension module AK-XM 204A / AK-XM 204B**

The module contains 8 relay outputs.

The supply voltage to the module comes from the previous module in the row.

##### **AK-XM 204B only**

##### **Override of relay**

Eight change-over switches at the front make it possible to override the relay’s function. Either to position OFF or ON.

In position Auto the controller carries out the control.

There are two rows with LEDs. They indicate the following: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

- Right row: (AK-XM 204B only):

- Override of relays

- ON = override

- OFF = no override

##### **Fuses**

Behind the upper part there is a fuse for each output.

*[Figurtekst: Max. 230 V Keep the safety distance! · AC-1: max. 4 A (ohmic) Low and high voltage must · AC-15: max. 3 A (Inductive) not be connected to the · same output group]*

*[Figurtekst: AK-XM 204B · Override of relay]*

##### **Point**

*[Figurtekst: Point 1 2 3 4 5 6 7 8 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Active at · DO Comp. 1 · On · Comp. 2 / · Fan 1 Off · Alarm · Solenoid · valve · Si g nal Module Point Terminal Active at · 1  (DO 1) 25 - 27 · 2  (DO 2) 28 - 30 · 3  (DO 3) 31 - 33 · 4  (DO 4) 34 -36 · 5  (DO 5) 37 - 39 · 6  (DO 6) 40 - 41 - 42 · 7  (DO 7) 43 - 44 - 45 · 8  (DO 8) 46 - 47 - 48]*

### **2.3.5 Extension module AK-XM 205A / AK-XM 205B**

The module contains:

8 analogue inputs for sensors, pressure transmitters, voltage signals and contact signals. 8 relay outputs.

The supply voltage to the module comes from the previous module in the row.

##### **AK-XM 205B only**

##### **Override of relay**

Eight change-over switches at the front make it possible to override the relay’s function. Either to position OFF or ON.

In position Auto the controller carries out the control.

There are two rows with LEDs. They indicate the following: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

- Right row: (AK-XM 205B only):

- Override of relays

- ON = override

- OFF = no override

##### **Fuses**

Behind the upper part there is a fuse for each output.

*[Figurtekst: AK-XM 205A  AK-XM 205B]*

*[Figurtekst: Max. 230 V Keep the safety distance! · AC-1: max. 4 A (ohmic) Low and high voltage · must not be connected to · AC-15: max. 3 A (Inductive) · the same output group]*

*[Figurtekst: AK-XM 205B · Override of relay]*

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 · Terminal 9 & 21: · 12 V max. 100 mA in total. · Terminal 10 & 22: · 5 V max. 100 mA in total. · Terminal 11, 12, 23, 24 : · (Cable screen) · The screen on the pressure · transmitter cables must only · be connected at the end of · the controller. · Point 9 10 11 12 13 14 15 16 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Signal · type · S S1 · S2 · Pt 1000 ohm/0°C SIG Saux Pt 1000 · SsA · SdA · Shr · GND Stw · Sgc · P · AKS 32R · 3: Brown · AKS 32R / · 2: Blue P0A AKS 2050 · P0B · 1: Black PcA MBS 8250 · -1 - xx bar · PcB · Paux · AKS 32 AKS 32 · 3: Brown PgcPrec -1 - zz bar · 2: Black · 1: Red Si g nal Module Point Terminal Si g nal t yp e /Active at · 1  (AI 1) 1 - 2 · U · 2  (AI 2) 3 - 4 · ... 0 - 5 V0 - 10 V 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · 5  (AI 5) 13 - 14 · On/Off Ext. Main · 6  (AI 6) 15 - 16 · switch Active at: · Day/ 7  (AI 7) 17 - 18 · Night Closed · Door / 8  (AI 8) 19 -20 · Level  Open 9  (DO 1) 25 - 26 - 27 · switch · 10  (DO 2) 28 - 29 - 30 · DO · Comp 1 11  (DO 3) 31 - 30 - 33 · Comp 2 · Fan 1 Active at: 12  (DO 4) 34 - 35 - 36 · Alarm · Light on 13  (DO 5) 37 - 38 - 39 · Rail heat / 14  (DO6) 40 - 41 - 42 · Defrost Off · Solenoid  15  (DO7) 43 - 44 - 45 · valve · 16  (DO8) 46 - 47 - 48]*

### **2.3.6 Extension module AK-XM 208C**

*[Figurtekst: Function · The module contains: · 8 analogue inputs for sensors, pressure transmitters, voltage · signals and contact signals. · 4 outputs for stepper motors. · Supply voltage · The supply voltage to the module comes from the previous · module in the row. Here supplied with 5 VA. · An additional and separated power supply must be installed, · which must be galvanically separated from the supply for the  Separate voltage supply · control range. Class II is required. is required max. 10 V · (Power requirements: 7.8 VA for controller + xx VA per valve). 24 V AC/DC / fx. 13 VA · 2 separated UPS´s are recommended, one for the pack controller · and another AK-XM 208C module if the valves need to open/ close · during a power failure. If the AK-CM 102 module is installed it is · also recommended a separated UPS. · Light-emitting diodes · There is one row with LEDs, indicating the following: · • Voltage supply to the module · • Communication active with the bottom PC board (red = error) · • Step1 to step4 OPEN: Green = Open · • Step1 to step4 CLOSE: Green = Close · • Red flash = Error on motor or connection · Output: · 24 V DC · 20-500 step/s · Max. Phase current  = 325 mA RMS · ∑ Pmax.   = 21 VA · The connection to the valve must · not be broken using a relay. · L = max. 30 m]*

*[Figurtekst: Valve data · Type P · ETS 12.5 - ETS 400 1.3 VA · KVS 15 - KVS 42 · CCMT 2 - CCMT 8 · CCM 10 - CCM 40 · CTR 20 · CCMT 16 - CCMT 42 5.1 VA · CCMT - 3L/5L/8L 4.0 VA]*

##### **Power supply to AK-XM 208C:**

Fx: 7.8 + (4 x 1.3) = 13 VA  AK-PS 063 STEP3 Fx: 7.8 + (4 x 5.1) = 28.2 VA  AK-PS 130 STEP3

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 · Terminal 17: 12 V max. 100 mA in total. · Terminal 18: 5 V max. 100 mA in total. · Terminal 19, 20: · (Cable screen) · Point 9 10 11 12 · Step 1 2 3 4 · Type AO · 1 25 26 27 28 · Step / 2 29 30 31 32 · Terminal 3 33 34 35 36 · 4 37 38 39 40 · ETS · CCM / CCMT · White Black Red Green · CTR · CCMT KVS]*

*[Figurtekst: Valve Module Ste p Terminal · 1 (point 9) 25 - 28 · 2 (point 10) 29 - 32 · 3 (point 11) 33 - 36 · 4 (point 12) 37 - 40]*

### **2.3.7 Extension module AK-OB 110**

*[Figurtekst: Function · The module contains two analogue voltage outputs of 0 – 10 V. · Supply voltage · The supply voltage to the module comes from the controller · module. · Placing · The module is placed on the PC board in the controller module. · Point · The two outputs have points 24 and 25. They are shown on the · earlier page where the controller is also mentioned. · Max. load · I < 2.5 mA · R > 4 kohm · Accuracy · Analog outputs: +/- 100 mV · Module 1 · Point 24 25 · AO2 · AO Type AO1 AO2 · AO 0 - 10 V AO1]*

### **2.3.8 Extension module EKA 163A / EKA 164A**

Display of important measurements from the controller, e.g. appliance temperature, suction pressure or condensing pressure. Setting of the individual functions can be performed by using the display with control buttons.

It is the controller used that determines the measurements and settings that can occur.

##### **Connection**

The extension module is connected to the controller module via a cable with plug connections. You have to use one cable per module. The cable is supplied in various lengths.

Both types of display (with or without control buttons) can be connected to either display output A, B, C and D. Ex.

A: P0. Suction pressure in °C.

B: Pc. Condensing pressure in °C.

When the controller starts up, the display will show the output that is connected.

- - 1 = output A - - 2 = output B etc.

##### **Placing**

The extension module can be placed at a distance of up to 15 m from the controller module.

##### **Point**

*[Figurtekst: EKA 163A   EKA 164A]*

*[Figurtekst: (2 m: 0847298) · (6 m: 0847299) · Brown · Green · White Danfoss 80Z991]*

No point has to be defined for a display module – you simply connect it.

### **2.3.9 Graphic display MMIGRS2**

Setting and display of values in the controller.

##### **Connection**

The display connects to the controller via a cable with RJ11 plug connections.

Received from the controller via cable and RJ11 connector. Do not connect a seperate power supply for this display.

##### **Termination**

The display must be terminated. Mount a connection between the terminals H and R. (AK-PC 782A is terminated internally.)

##### **Placing**

The display can be placed at a distance of up to 3 m from the controller.

##### **Point / Address**

No point has to be defined for a display – you simply connect it. However, the address must be verified. See the instructions accompanying the controller.

To create access, the display must be connected and the address of MMIGRS2 must be activated.

##### Setting:

1. Press both the "x-button" and "enter button" and hold for 5 seconds. Subsequently the Bios menu is shown.

2. Select the line "MCX selection", press "enter"

3. Select the line "Man selection", press "enter"

4. The address is shown now. Please check that it is 001, press "enter". Then data is downloaded from the controller.

### **2.3.10 Power supply module AK-PS 063 STEP3 / 130 STEP3 / 250 STEP3**

24 V supply for controller.

**Supply voltage** 100 – 240 V AC, -15 – +10 % 110 – 250 V DC, -20 – +40 % (for DC, connect a suitable fuse)

##### **Placing**

On DIN-rail

|**Effect**||||
|---|---|---|---|
|**Type**|**Output tension**|**Output current**|**Power**|
|AK-PS 063 STEP3|24 V DC|0.63 A|15 VA|
|AK-PS 130 STEP3|24 V DC|1.3A|30 VA|
|AK-PS 250 STEP3|24 V DC|2.5 A|60 VA|

##### **Dimension**

|**Type**|**High**|**Width**|
|---|---|---|
|AK-PS 063 STEP3|90 mm|18 mm|
|AK-PS 130 STEP3|90 mm|36 mm|
|AK-PS 250 STEP3|90 mm|54 mm|

##### **Supply to a controller**

##### **Connections**

*[Figurtekst: AK-PS 063 STEP3 AK-PS 130 STEP3 AK-PS 250 STEP3 · 24 V DC 24 V DC 24 V DC · +    _ +    _ +    _ · 100 – 240 V AC, -15 – +10 % 100 – 240 V AC, -15 – +10 % 100 – 240 V AC, -15 – +10 % · 110 – 250 V DC, -20 – +40 %   110 – 250 V DC, -20 – +40 %   110 – 250 V DC, -20 – +40 % · (for DC, connect a suitable fuse)  (for DC, connect a suitable fuse)  (for DC, connect a suitable fuse) · Danfoss 80Z993 Danfoss 80Z995 Danfoss 80Z994]*

### **2.3.11 Communication module AK-CM 102**

The module is a new communication module, meaning the row of extension modules can be interrupted. The module communicates with the regulator via data communication and forwards information between the controller and the connected extension modules.

##### **Connection**

Communication module and controller fitted with RJ 45 plug connectors.

**Nothing** else should be connected to this data communication; a maximum of 5 communication modules can be connected to one controller.

##### **Communication cable**

One metre of the following is enclosed: ANSI/TIA 568 B/C CAT5 UTP cable w/ RJ45 connectors.

##### **Positioning**

Max. 30 m from the controller (The total length of the communication cables is 30 m)

24 volt AC or DC should be connected to the communication module.

The 24 V can be sourced from the same supply that supplies the controller. (The supply for the communication module is galvanically separated from the connected extension modules). The terminals must **not** be earthed.

The power consumption is determined by the power consumption of the total number of modules. The controller strand load must not exceed 32 VA. Each AK-CM 102 strand load must not exceed 20 VA.

##### **Point**

Connection points on the I/O modules should be defined as if the modules were an extension of each other.

##### **Address**

The address for the first communication module should be set to 1. Any second module should be set to 2.  A maximum of 5 modules can be addressed.

##### **Termination**

The termination switch on the final communication module should be set to ON.

*[Figurtekst: Max. 32 VA · Max. 20 VA · Max. 20 VA]*

The controller should permanently be set to = ON.

Additional modules may only be installed following the installation of the final module. (Here following module no. 11; see the sketch.) After configuration, the address must not be changed.

### **2.4 Preface to design**

Be aware of the following when the number of extension modules is being planned. A signal may have to be changed, so that an additional module may be avoided.

- An ON/OFF signal can be received in two ways. Either as a contact signal on an analogue input or as voltage on a low or high-voltage module.

Mentioned below are a number of functions and connections that may have to be considered when a regulation has to be planned. There are more functions in the controller than the ones mentioned here, but those mentioned have been included in order for the need for connections to be established.

- An ON/OFF output signal can be given in two ways. Either with a relay switch or with solid state. The primary difference is the permitted load and that the relay switch contains a cut-out switch.

##### **Functions**

##### **Clock function**

Clock function and change-over between summer time and winter time are contained in the controller. The clock setting is maintained for at least 12 hours at a power failure.

The clock setting is kept updated if the controller is linked up in a network with a system manager.

##### **Start/stop of regulation**

Regulation can be started and stopped via the software. External start/stop can also be connected.

The function stops all regulation, including any high-pressure regulation. Excess pressure can lead to a loss of charge.

##### **Start/stop of compressors**

External start/stop can be connected.

##### **Alarm function**

##### **I'm alive function**

A relay can be reserved which is pulled during normal regulation. The relay will be released if the regulation stops with the main switch or if the controller fails.

##### **Extra temperature sensors and pressure sensors**

If additional measurements have to be carried out beyond the regulation, sensors can be connected to the analogue inputs.

##### **Forced control**

The software contains a forced control option. If an extension module with relay outputs is used, the module’s top part can be with change-over switches – switches that can override the individual relays into either OFF or ON position. Wiring should be done with a safety relay. See Regulating functions.

##### **Data communication**

The controller module has terminals for LON data communication. The requirements to the installation are described in a separate document.

If the alarm is to be sent to a signal transmitter, a relay output will have to be used.

##### **Connections**

In principle there are the following types of connections:

##### **Analogue inputs ”AI”**

This signal must be connected to two SIG terminals. Signals can be received from the following GND sources:

- Temperature signal from Pt 1000 ohm temperature sensor

- Pulse signal or reset signal

- Contact signal where the input is shortcircuited or ”opened”, respectively

- Voltage signal from 0 to 10 V

- Signal from pressure transmitter AKS 32, AKS 32R, AKS 2050 or MBS 8250.

- The supply voltage is supplied from the module’s terminal board where there is both a 5 V supply and a 12 V supply. When programming, the pressure transmitter’s pressure range must be set.

##### **ON/OFF voltage inputs ”DI”**

This signal must be connected to two terminals.

- The signal must have two levels, either 0 V or ”voltage” on the input. There are two different extension modules for this signal type:

- low-voltage signals, e.g. 24 V

- high-voltage signals, e.g. 230 V

When programming, the function must be set:

- Active when the input is without voltage

ON/OFF output signals ”DO” There are two types, as follows:

- **Relay outputs**

- All relay outputs are with change-over relay so that the required function can be obtained when the controller is without voltage.

- **Solid state outputs**

- Reserved for ejector valves, oil valves and AKV valves, but output can cut an external relay in and out, as with a relay output.

The output is only found on the controller module.

When programming, the function must be set:

- Active when the output is activated

- Active when the output is not activated.

##### **Analogue output signal ”AO”**

This signal is to be used if a control signal is to be transmitted to an external unit, e.g. a frequency converter. When programming, the signal range must be defined: 0-5 V, 1-5 V, 0-10 V or 2-10 V.

Pulse signal for the stepper motors. This signal is used by valve motors of the type ETS, KVS, CCM and CCMT. The valve type should be set during programming.

- Active when voltage is applied to the input.

##### **Limitations**

As the system is very flexible  regarding the number of connected units, you must check whether your selection complies with the few limitations there are.

The complexity of the controller is determined by the software, the size of the processor, and the size of the memory. It provides the controller with a certain number of connections from which data can be downloaded, and others where coupling with relays can be performed.

##### **Common pressure transmitter**

If several controllers receive a signal from the same pressure transmitter, the supply to the affected controllers must be wired so that it is not possible to switch off one of the controllers without also switching off the others. (If one controller is switched off, the signal will be pulled down, and all the other controllers will receive a signal which is too low).

##### **Ejector valves**

-  The sum of connections cannot exceed **220** (AK-PC 782A).

If ejector valves are used, the smallest ones must be connected to the solid state outputs.

-  The number of extension modules must be limited so that the total power in a row will not exceed **32** VA (including controller). If the AK-CM 102 communication module is used, each row of AK-CM 102 must not exceed 20 VA (incl. AK-CM 102). There must not be more than a total of 18 modules (controller + 17 modules).

-  No more than **5** pressure transmitters may be connected to one controller module.

-  No more than **5** pressure transmitters may be connected to one extension module.

### **2.5 Design of a compressor and condenser control**

Procedure:

1. Make a sketch of the system in question

2. Check that the controller’s functions cover the required application

3. Consider the connections to be made

4. Use the planning table  Note down the number of connections  add up

5. Are there enough connections on the controller module? – If not, can they be obtained by changing an ON/OFF input signal from voltage signal to contact signal, or will an extension module be required?

6. Decide which extension modules are to be used

7. Check that the limitations are observed

8. Calculate the total length of modules

9. The modules are linked together

10. The connection sites are established

11. Draw a connection diagram or a key diagram

12. Size of supply voltage/transformer

##### **1. Sketch**

*[Figurtekst: Make a sketch of the system in question.]*

##### **2. Compressor and condenser functions**

||AK-PC 782A|**Oil management**||
|---|---|---|---|
|**Application**||Receiverpressure control|x|
|Both compressorgroupand condensergroup|x|Monitoringof oil level in receiver|x|
|Boostergroup|x|Management of oil level in oil separator|x|
|Parallel compressor|x|**Suctionpressure reference**||
|**Regulation of compressor capacity**||Override via P0 optimization|x|
|Regulation sensor. P0|x|Override via “night setback”|x|
|PI-regulation|x|Override  via "0 -10 V signal"|x|
|Max. number of compressor steps: MT+IT / LT|10+8/4|**Regulation of condenser capacity**||
|Max. number of unloaders each compressor|3|Regulation sensor. Sgc  or S7|x|
|Identical compressor capacities|x|Stepregulation|x|
|Different compressor capacities|x|Max. number of steps|8|
|Speed regulation of 1 or 2 compressors|x|Speed regulation|x|
|Run time equalisation|x|Stepand speed regulation|x|
|Min. restart time|x|Speed regulation first step|x|
|Min. On-time|x|Limitation of speed duringnight operation|x|
|Ejector regulation|x|Heat recoveryfunction for tapwater control|x|
|Liquid injection in suction line|x|Heat recoveryfunction for heating|x|
|Liquid injection in cascade heat exchanger|x|Controlling the gas cooler (high pressure valve). parallel  valve, if|x|
|External start/stopof compressors|x|applicable||

|**Condenserpressure reference**||Safetymonitoringof condenser fans|x|
|---|---|---|---|
|Floatingcondensing pressure reference|x|General alarm functions with time delay|10|
|Settingof references for heat recoveryfunctions|x|**Miscellaneous**||
|**Safety functions**||Extra sensors|7|
|Min. suctionpressure|x|Inject On function|x|
|Max. suctionpressure|x|Option for connection of separate display|4 + 1|
|Max. condensing pressure|x|Separate thermostat functions|10|
|Max. dischargegas temperature|x|Separatepressostat functions|5|
|Min. / Max. superheat|x|Separate voltage measurements|5|
|Safetymonitoringof compressors|x|PI regulation|3|
|Common highpressure monitoringof compressors|x|Max. input and output|220|

##### **A bit more about the functions**

##### **Compressor**

Regulation of up to 10 MT and 8 IT compressors and up to 4 LT compressors. All with up to 3 unloaders per compressor. Compressor No. 1 or 2 can be speed-regulated.

The following can be used as control sensor: P0 - Suction pressure

##### **Condenser**

Regulation of up to 8 condenser steps.

Fans can be speed-regulated. Either all on one signal or only the first fan of several. EC motor can be used. Relay outputs and solid state outputs may be used, as desired. The following can be used as control sensor:

1) Sgc -Temperature at the gas cooler outlet (one or two Sgc sensors can be configured).

2) S7 - Warm brine temperature (Pc is used here for high-pressure safety.)

##### **Speed regulation of condenser fans**

The function requires an analogue output module. A relay output may be used for start/stop of the speed regulation. The fans may also be cut in and out by relay outputs.

##### **Safety circuit**

If signals are to be received from one or more parts of a safety circuit, each signal must be connected to an ON/OFF input.

##### **Day/night signal for raising the suction pressure**

The clock function can be used, but an external ON/OFF signal may be used instead.

If the “P0 optimization” function is used, no signal will be given concerning the raising of the suction pressure. The P0 optimization will see to this.

##### **“Inject ON” override function**

The function closes expansion valves on evaporator controls when all compressors are prevented from starting. The function can take place via the data communication, or it may be wired via a relay output.

##### **Separate thermostat and pressure control functions**

A number of thermostats can be used according to your wishes. The function requires a sensor signal and a relay output. In the controller there are settings for cut-in and cut-out values. An associated alarm function may also be used.

##### **Separate voltage measurements**

##### **Pulse wide modulating unloading**

When using a compressor with PWM-unloading, the unloading should be connected to one of the four solid state outputs in the controller.

##### **Heat recovery**

There are adjustment options for hot water and heat containers for heating.

A number of voltage measurements can be used according to your wishes. The signal can for example be 0-10 V. The function requires a voltage signal and a relay output. In the controller there are settings for cut-in and cut-out values. An associated alarm function may also be used.

If you want to know more about the functions, go to chapter 5.

The controller manages, in order of priority: 1-tap water, 2-heating, 3-gas cooler, which removes the remaining excess heat.

##### **3. Connections**

Here is a survey of the possible connections. The texts can be read in context with the table on the following page.

##### **Analogue inputs**

###### **Temperature sensors**

- Ss (suction gas temperature)

- Must always be used in connection with compressor regulation.

- Sd (discharge gas temperature) Must always be used in connection with compressor regulation.

- Sc3 (outdoor temperature) Must be used when regulation is performed with floating condenser reference.

- S7 (warm brine return temperature) Must be used when the control sensor for condenser has been selected as S7.

- Saux (1-4), any extra temperature sensors Up to four additional sensors for monitoring and data collection may be connected. These sensors can be used for general thermostat functions.

- Stw2, 3, 4 and 8 (temperature sensors for heat recovery) Must be used when adjusting hot tap water.

- Shr2, 3, 4 and 8 (temperature sensors for heat recovery) Must be used when adjusting the heat receiver for heating.

- Sgc (temperature sensor for gas cooling controls) Shall be placed within one metre after the gas cooler.

- Shp (temperature sensor, if the refrigerant can be routed outside of the gas cooler)

###### **Pressure transmitters**

- P0 Suction Pressure

- Must always be used in connection with compressor regulation (frost protection).

- Pc Condensing Pressure Must always be used in connection with compressor or condenser regulation

- Prec. Oil receiver pressure. Must be used for receiver pressure regulation.

- Pgc Gas cooler pressure.

- Prec. Pressure reading in the CO2 receiver.

- Paux (1-5)

Up to 5 extra pressure transmitters can be connected for monitoring and data collection. These sensors can be used for general pressure switch functions.

Note: A pressure transmitter type AKS 32, AKS 32R or MBS 8250 can supply signals to a maximum of five controllers.

##### **Voltage signal**

- Ext. Ref

Used if a reference override signal is received from another control.

- Voltage inputs (1-5)

Up to 5 extra voltage signals can be connected for monitoring and data collection. These signals are used for general voltage input functions.

##### **On/Off-inputs**

**Contact function** (on an analogue input) or

- Level contacts

##### • Level contact on suction accumulator **On/off-outputs Relay outputs**

- Compressors

- Unloaders

- Fan motor

- Injection On function (signal for evaporator controls. One per suction group).

- Start/stop of liquid injection in suction line

- Start/stop of 3-way valves at heat recovery

- ON/OFF signal for start/stop of speed regulation

- Alarm relay. I'm alive relay.

- Status relay: Floating allowed / not allowed

- On/off signals from general thermostats (1 – 10), pressure switches (1 – 5) or voltage input functions (1 – 5).

- Oil valves

**voltage signal** (on an extension module)

##### **Solid state outputs**

- Common safety input for all compressors (e.g. common highpressure/low-pressure pressure switch)

These are primarily for ejector valves, oil valves and AKV valves. The solid state outputs on the controller module may be used for the same functions as those mentioned under “relay outputs”. (The output will always be “OFF” when the controller has a power failure).

- Up to 6 signals from the safety circuit of each compressor

- Signal from the condenser fan's safety circuit

- Any signal from the frequency converter’s safety circuit

- External start/stop of regulation

Analogue outputs

- External day/night signal (raise/lower the suction pressure reference). The function is not used if the “P0 optimization” function is used.

   - Speed regulation of the condenser’s fans.

   - Speed regulation of the compressor

   - Speed control of pumps for heat recovery

- DI alarm (1-10) inputs

- Control signal for high pressure valve Vhp. (stepper signal - if applicable)

Up to 10 no. extra on/off signals for general alarm for monitoring and data collection can be connected.

   - Stepper signal for hot gas by-pass valve

- Flow switch for heat recovery

##### **Example**

**High pressure controls:**

   - LT: Po max = -5 °C, Po min = -45 °C

- Heat recovery for tap water

- LT: Pc max = 40 bar

##### **Compressor group:**

- Gas cooler

- LT: Sd max = 100 °C

MT circuits:

- 3 compressors with "cyclic". One speed controlled

- Fans, speed controlled **Receivers:**

   - SH min =  5 °C, SH max = 35 °C **Other:**

- Safety monitoring of each compressor

      - Start/stop of heat recovery to Tw

   - Optimal CO2 reveiver pressure

- Common high-pressure monitoring

- Monitoring CO2-level in the receiver

   - External main switch used Data from this example is used on the next page. The result is that the following modules should be used:

- Po setting -10 °C, Po optimization from the system unit

- LT circuits:

   - Monitoring of high and low pressure

   - Controlling the tap water receiver temperature, 55°C

- 2 x compressors with "cyclic". One speed controlled

##### **Fan in plant room**

   - AK-PC 782A controller

- Thermostat control of fan in engine room

   - AK-XM 205A input and output module

- Safety monitoring of each compressor

##### **Safety functions:**

      - AK-XM 208C stepper output module • AK-XM 103B analogue input and output module

   - Monitoring of Po, Pc, Sd and superheat in

- Common high pressure monitoring

- Po setting –30 °C, Po optimization from the system unit

- IT circuit:

suction line

      - AK-OB 110 analogue output module

   - MT: Po max = -5 °C, Po min = -35 °C

   - MT: Pc max = 110 bar

- 1 compressor, speed controlled

   - MT: Sd max = 120 °C

- Receiver set point 36 bar

|**4. Planning table**<br>The table helps you establish whether there are enough inputs<br>and outputs on the basic controller.<br>If there are not enough of them, the controller must be extended<br>by one or more of the mentioned extension modules.|**e input signal**|**f oltage signal**|**f oltage signal**|**f utput signal**|**utput signal 0-10 V**<br>**utput**|**7**<br>**ons**|
|---|---|---|---|---|---|---|
|Note down the connections you will require and add them up|**Analogu**<br>Example|**On/off v**<br>Example|**On/off v**<br>Example|**On/Off o**<br>Example|**Analogue o**<br>**Stepper o**<br>Example|**Limitati**|
|**Analogue inputs**|||||||
|Temperature sensors, Ss, Sd, Sc3, S7, Stw.., Shr.., Sgc<br>|13<br>||||||
|Extra temperature sensor / separate thermostats /PI-regulation|1||||||
|Pressure transmitters, P0, Pc, Pctrl. Prec / separate pressostats|5|||||P = Max.**5**/ module|
|Voltage signal from other regulation, separate signals<br>|||||||
|Heat recoveryvia thermostat|||||||
|**On/off inputs**|Contact|24 V|230 V||||
|Safetycircuits, common for all compressors|2|||||Max.1/suction group|
|Safetycircuits, Oilpressure||||||Max. 1/Comp.|
|Safetycircuits, comp. Motorprotection|||||||
|Safetycircuits, comp. Motor temp.|||||||
|Safetycircuits, comp. Highpres. thermostat|||||||
|Safetycircuits, comp. Highpres.pressostat<br>|||||||
|Safetycircuits,general for each compressor|6||||||
|Safetycircuits, condenser fans, frequencyconverter<br>l||||||Max. 1/ fan|
|Safetycircuits, flow switch<br>External start/sto|1||||||
|p<br>Night setback of suctionpressure|||||||
|Separate alarm functions via DI|||||||
|Load shedding<br>||||||K|
|Start of Heat recovery|1|||||O|
|Liquid level receiver / suction accumulator, Oil level<br>|1|||||=>|
|Pulsationpressure||||||d|
|**On/off outputs**||||||ede|
|Compressors, motors||||6||ce|
|Unloaders||||||e ex|
|Fan motors, circulationpumps||||3||ar|
|Alarm relay, I'm alive relay, floatingallowed||||||ns|
|Inject ON<br>||||||Max. 2<br>atio|
|Separate thermostat and pressostat functions and voltage measurements||||1||Max. 10+5+5<br>mit|
|Heat recoveryfunction via thermostat||||||Max.1<br>le:<br>e li|
|Liquid injection in suction line / heat exchanger. Heatgas dump||||1||Max.1<br>mp<br>th|
|Solenoid valve for Oil, ejector valve.||||||xa<br>of|
|3-wayvalve||||1||he e<br>one|
|||||||T<br>N|
|**Analogue control signal, 0-10 V**|||||||
|<br>Frequencyconverter, Compressor, fans,pumps, valves etc.|||||5||
|**Valves with stepper motor. Parallel valves, if applicable**|||||3||
|**Sum of  connections for the regulation**|30|0|0|12|5+3|Sum = max.**220**|
|Number of connections on a controller module|11<br>11|0<br>0|0<br>0|8<br>8|0<br>0<br>0||
|**5. Missing connections, if applicable**|19|-|0|4|5+3||
|**6. The missing connections to be supplied by one or more exte**|**nsion mo**|**dules:**||||Sum of power|
|AK-XM 101A**(8 analogue inputs)**<br>AK-XM 102A**(8 digital low voltage inputs)**||||||___pcs. á 2 VA = __<br> pcs. á 2 VA =|
|<br>AK-XM 102B**(8 digital high voltage outputs)**||||||_____<br>___pcs. á 2 VA = __|
|AK-XM 103A**(4 analogue inputs 4 analogue outputs)**|1||||1|pcs. á 2 VA =|
|**, **<br>AK-XM 204A / B**(8 relay outputs)**||||||_____<br>___pcs. á 5 VA = __|
|AK-XM 205A / B**(8 analogue inputs + 8 relay output)**|1|||1||___pcs. á 5 VA = __|
|AK-XM 208C**(8 analogue inputs + 4 stepper outputs)**|1||||1|___pcs. á 5 VA = __|
|AKOB 110**2 l **|||||1|á 0 VA   0|
|_**( anaogue outputs)**||||||___pcs.    =|
|||||||1pcs. á 8 VA = 8<br>Sum =<br>Sum = max.**32**VA|

##### **8. Length**

If you use many extension modules, the controller’s length will grow accordingly. The row of modules is a complete unit which cannot be broken.

If the row becomes longer than desired, the row can be broken by using AK-CM 102.

The module dimension is 72 mm. Modules in the 100-series consist of one module. Modules in the 200-series consist of two modules. The controller consist of three modules. The length of an aggregate unit = n x 72 + 8

or in an other way:

|**Module**|**Type**|**No.**|**at**|**Length**|
|---|---|---|---|---|
|Controller module||1|x  224|= 224 mm|
|Extension module|200-series|_|x 144|= ___ mm|
|Extension module|100-series|_|x<br>72|= ___ mm|
|**Total length**||||= ___ mm|

##### **9. Linking of modules**

Start with the controller module and then mount the selected extension modules. The sequence is of no importance.

However, you must **not** change the sequence, i.e. rearrange the modules, after you have made the set-up where the controller is told which connections are found on which modules and on which terminals.

The modules are attached to one another and kept together by a connection which at the same time transmits the supply voltage and the internal data communication to the next module.

Mounting and removal must always be performed when there is no voltage.

The protective cap mounted on the controller’s plug connection must be moved to the last vacant plug connection so that the plug will be protected against short-circuit and dirt.

When the regulation has started, the controller will check all the time whether there is connection to the connected modules. This status can be followed by the light-emitting diode.

When the two catches for the DIN rail mounting are in open position, the module can be pushed into place on the DIN rail – no matter where in the row the module is found. Removal is likewise carried out with the two catches in the open position.

Example continued: Controller module + 2 extension modules in 200-series + 1 extension module in 100 series = 224 + 144 + 144 + 72 = 584 mm.

*[Figurtekst: Example continued]*

##### **10. Determine the connection points**

All connections must be programmed with module and point, so in principle it does not matter where the connections are made, as long as it takes place on a correct type of input or output.

- The controller is the first module, the next one is 2, etc.

- A point is the two or three terminals belonging to an input or output (e.g. two terminals for a sensor and three terminals for a relay).

The preparation of the connection diagram and the subsequent programming (configuration) should take place at the present time. It is most easily accomplished by filling in the connection survey for the relevant modules.

Principle:

|**Name**|**On module**|**On Point**|**Function**|
|---|---|---|---|
|fx Compressor 1|x|x|Close|
|fx Compressor 2|x|x|Close|
|fx Alarm relay|x|x|NC|
|fx Main switch|x|x|Close|
|fx P0|x|x|AKS 2050-1 to 159 bar|

The connection survey from the controller and any extension modules are uploaded from the paragraph "Module survey. E.g. controller module:

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|||**1**(AI 1)|**1 - 2**||
|||**2**(AI 2)|**3 - 4**||
|||**3**(AI 3)|**5 - 6**||

*[Figurtekst: Module  Point · Mind the numbering. · The right-hand part of the · controller module may look like a · separate module. But it  is not.]*

**Note:** The safety relays should not be fitted onto a module with override changeovers, as they can be put out of operation by an incorrect setting.

- Columns 1, 2, 3 and 5 are used for the programming.

- Columns 2 and 4 are used for the connection diagram.

###### Example continued

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Discharge temperature - Sd-MT||**1**(AI 1)|**1 - 2**|Pt 1000|
|Suction gas temperature- Ss-MT||**2**(AI 2)|**3 - 4**|Pt 1000|
|Discharge temperature - Sd-IT||**3**(AI 3)|**5 - 6**|Pt 1000|
|Suction gas temperature- Ss-MT||**4**(AI 4)|**7 - 8**|Pt 1000|
|Thermostat sensor in plant room<br>- Saux1||**5**(AI 5)|**9 - 10**|Pt 1000|
|Suction pressure - P0-MT||**6**(AI 6)|**11 - 12**|AKS 2050-59|
|Condensing  pressure - Pc-MT||**7**(AI 7)|**13 - 14**|AKS 2050-159|
|Tap water temperature - Stw8||**8**(AI 8)|**19 - 20**|Pt 1000|
|Temp. gas cooler output Sgc||**9**(AI 9)|**21 - 22**|Pt 1000|
|Gas cooler pressure Pgc|**1**|**10**(AI 10)|**23 - 24**|AKS 2050-159|
|Refrigerant receiver, Prec CO2||**11**(AI 11)|**25 - 26**|AKS 2050-159|
|Hot gas dump||**12**(DO 1)|**31 - 32**|ON|
|Circulation pump tw||**13**(DO 2)|**33 - 34**|ON|
|||**14**(DO 3)|**35 - 36**||
|||**15**(DO 4)|**37 - 38**||
|MT Compressor 1 (VLT start)||**16**(DO 5)|**39 - 40 - 41**|ON|
|MT Compressor 2||**17**(DO6)|**42 - 43 - 44**|ON|
|MT Compressor 3||**18**(DO7)|**45 - 46 - 47**|ON|
|IT Compressor (VLT start)||**19**(DO8)|**48 - 49 - 50**|ON|
|Speed control MT compressor||**24**|**-**|0-10 V|
|Speed control IT compressor||**25**|**-**|0-10 V|
|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|Temp.  by-pased gas Shp||**1**(AI 1)|**1 - 2**|Pt 1000|
|Level switch, CO2 receiver||**2**(AI 2)|**3 - 4**|Open|
|Start/stop heat recovery tw||**3**(AI 3)|**5 - 6**|Closed|
|Outdoor temperature, Sc3||**4**(AI 4)|**7 - 8**|Pt 1000|
|Speed control LT compressor|**2**|**5**(AO 1)|**9 - 10**|0 - 10 V|
|Speed control, gas cooler fan||**6**(AO 2)|**11 - 12**|0 - 10 V|
|Speed control, pump - tw||**7**(AO 3)|**13 - 14**|0 - 10 V|
|||**8**(AO 4)|**15 - 16**||

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|MT compressor 1 safety circuits||**1**(AI 1)|**1 - 2**|Open|
|MT compressor 2 safety circuits||**2**(AI 2)|**3 - 4**|Open|
|MT compressor 3 safety circuits||**3**(AI 3)|**5 - 6**|Open|
|||**4**(AI 4)|**7 - 8**||
|LT compressor 1 safety circuits||**5**(AI 5)|**9 - 10**|Open|
|LT compressor 2 safety circuits|**3**|**6**(AI 6)|**11 - 12**|Open|
|Heat recovery tw2||**7**(AI 7)|**13 - 14**|Pt 1000|
|Heat recovery tw3||**8**(AI 8)|**15 - 16**|Pt 1000|
|Signal to by-pass valve, Vrec||**9 (step 1)**|**25 - 26 - 27 - 28**|CCMT|
|Signal to high pressure valve, Vhp||**10 (step 2)**|**29 - 30 - 31 - 32**|CCMT|
|Signal to 3-way valve V3gc||**11 (step 3)**|**33 - 34 - 35 - 36**|CTR|
|||**12 (step 4)**|**37 - 38 - 39 - 40**||
|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|Discharge temperature - Sd-LT||**1**(AI 1)|**1 - 2**|Pt 1000|
|Suction gas temperature - Ss-LT||**2**(AI 2)|**3 - 4**|Pt 1000|
|External main switch||**3**(AI 3)|**5 - 6**|Closed|
|MT Compressors common safety<br>circuits||**4**(AI 4)|**7 - 8**|Open|
|IT Compressors common safety<br>circuits||**5**(AI 5)|**13 - 14**|Open|
|LT Compressors common safety<br>circuits||**6**(AI 6)|**15 - 16**|Open|
|Heat recovery tw4||**7**(AI 7)|**17 - 18**|Pt 1000|
|Suction pressure - P0-LT|**4**|**8**(AI 8)|**19 - 20**|AKS 2050-59|
|LT Compressor 1 (VLT start)||**9**(DO 1)|**25 - 26 - 27**|ON|
|LT Compressor 2||**10**(DO 2)|**28 - 29 - 30**|ON|
|Fan motors (VLT start)||**11**(DO 3)|**31 - 32 - 33**|ON|
|||**12**(DO 4)|**34 - 35 - 36**||
|3-way valve, tap water, Vtw||**13**(DO 5)|**37 - 38 - 39**|ON|
|||**14**(DO6)|**40 - 41 - 42**||
|Room fan||**15**(DO7)|**43 - 44 - 45**|ON|
|||**16**(DO8)|**46 - 47 - 48**||

##### **11. Connection diagram**

Drawings of the individual modules may be ordered from Danfoss. Format = dwg and dxf.

You may then yourself write the module number in the circle and draw the individual connections.

Example continued:

The supply voltage for the pressure transmitter should be taken from the same module that receives the pressure signal. The screen on the pressure transmitter cables must only be connected at the end of the controller.

##### **12. Supply voltage**

Supply voltage is only connected to the controller module. The supply to the other modules is transmitted via the plug between the modules.

The supply must be 24 V +/-20%. One power supply must be used for each controller. The power supply must be a  class II. The 24 V must not be shared by other controllers or units. The analogue inputs and outputs are **not** galvanically separated from the supply.

The + and – 24V input must **not** be earthed.

If using stepper motor valves, the supply for these must be provided from a separate power supply.

For CO2 facilities, it will also be necessary to safeguard the voltage to the controller and valves using UPS.

##### **Power supply size**

The power consumption grows with the number of modules used:

|Module|Type|No.|á|Effect||
|---|---|---|---|---|---|
|Controller||1|x|8 =|8 VA|
|Extension module|200 series|_|x|5 =|_ VA|
|Extension module|100 series|_|x|2 =|_ VA|
|Total|||||_ VA|

##### **Common pressure transmitter**

If several controllers receive a signal from the same pressure transmitter, the supply to the affected controllers must be wired so that it is not possible to switch off one of the controllers without also switching off the others. (If one controller is switched off, the signal will be pulled down, and all the other controllers will receive a signal which is too low)

Example continued:

|Controller module|8 VA|
|---|---|
|+ 2 extension modules in 200 series|10 VA|
|+ 1 extension module in 100 series|2 VA|
||------|
|Power supply size (least)|20 VA|

+ Separate power supply for the module with the stepper motors: 7.8 + 1.3 + 1.3 + 5.1 = 15.5 VA.

### **2.6 Ordering**

##### 1. Controller

|**Type**|**Function**|**Application**|**Language**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|---|
|AK-PC 782A|Controller for capacity control of MT-, LT-,<br>IT- compressors and condensers. With oil<br>management,  multi ejector and high pres-<br>sure regulation|Transcritical CO2<br>booster control|English, German, French, Dutch, Italian,<br>Spanish, Portuguese, Danish, Finnish,<br>Russian, Czech, Polish|**080Z0192**|**X**|

##### 2. Extension modules and surve y for inputs and outputs

|**Type**|**Analogue**<br>**inputs**|**On/Off ou**|**f tputs**|**On/off supp**<br>**(DI signal)**|**f ly voltage**|**Analogue**<br>**outputs**|**Stepper**<br>**outputs**|**Module**<br>**with**<br>**switches**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|---|---|---|---|---|---|
||For sensors,<br>pressure<br>transmitters<br>etc.|Relay<br>(SPDT)|Solid state|Low volt-<br>age<br>(max. 80 V)|High volt-<br>age<br>(max. 260<br>V)|0-10 V DC|For valves<br>with step<br>control|For override<br>of relay<br>outputs|With screw<br>terminals||
|Controller|11|4|4|-|-|-||-|-||
|Extension mo|dules||||||||||
|AK-XM 101A|8||||||||**080Z0007**||
|AK-XM 102A||||8|||||**080Z0008**||
|AK-XM 102B|||||8||||**080Z0013**||
|AK-XM 103A|4|||||4|||**080Z0032**|**x**|
|AK-XM 204A||8|||||||**080Z0011**||
|AK-XM 204B||8||||||x|**080Z0018**||
|AK-XM 205A|8|8|||||||**080Z0010**|**x**|
|AK-XM 205B|8|8||||||x|**080Z0017**||
|AK-XM 208C|8||||||4||**080Z0023**|**x**|
|<br>The following<br>There is onlyr|extension modu<br>oom for one mo|le can be pl<br>dule.|aced on the PC|board in the c|ontroller mod|ule.|||||
|AK-OB 110||||||2|||**080Z0251**|**x**|

##### 3. AK o p eration and accessories

|**Type**|**Function**|**Application**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|
|**Operation**|||||
|AK-ST 500|Software for operation of AK controllers|AK-operation|**080Z0161**|**x**|
|-|Cable between PC and AK controller|USB A-B(standard IT cable)|**-**|**x**|
|**Accessories**|**Power supply module 24 V DC**||||
|AK-PS 063 STEP3|15 VA||**080Z0057**|**x**|
|AK-PS 130 STEP3|30 VA|Supply for controller|**080Z0058**|**x**|
|AK-PS 250 STEP3|60 VA||**080Z0059**||
|**Accessories**|**External display that can be connected to the con**|**troller module. For showing, say, the suctionpressu**|**re**||
|EKA 163A|Display||**084B8562**<sup>1)</sup>||
|EKA 164A|Displaywith operation buttons||**084B8563**<sup>1)</sup>||
|MMIGRS2|Graphic displaywith operation||**080G0294**||
||Cbl b EKA dil d ll|Length = 2 m|**084B7298**||
|-|ae etween  spay an controer|Length = 6 m|**084B7299**||
||Cable between graphic display type MMIGRS2 and|Length = 1.5 m|**080G0075**||
|-|controller (controller with RJ11 plug)|Length  = 3 m|**080G0076**||
|**Accessories**|**Communication modules for controllers where m**|**odules cannot be connected continuously**|||
|AK-CM 102|Communication module|Data communication for external extension modules|**080Z0064**||

1) Please, check instruction sheet RI8KB700 for a proper cable connection between EKA display and controller.

### **3. Mounting and wiring**

This section describes how the controller:

- is fitted

- is connected

We have decided to work on the basis of the example we went through previously, i.e. the following modules:

- AK-PC 782A controller module

- AK-XM 205A input and output module

- AK-XM 208C analogue input module + stepper output module

- AK-XM 103B analogue input and output module

- AK-OB 110 analogue output module

### **3.1 Mounting**

##### **Mounting of analogue output module**

The basic module must not be connected to voltage.

1. Lift the top part off the basic module

Press in the plate on the left-hand side of the light-emitting diodes and the plate on the right-hand side for the red address changers.

Lift the top part off the basic module.

2. Mount the extension module in the basic module

The analogue extension module will supply a signal to frequency converter on MT and IT.

*[Figurtekst: There are two outputs.]*

3. Put the top part back onto the basic module

##### **Mounting of extension module on the basic module**

*[Figurtekst: 1. Move the protective cap]*

1. Remove the protective cap from the connection plug on the right-hand side of the basic module.

Place the cap on the connection plug to the right of the extension module that is to be mounted on the extreme right-hand side of the AK assembly.

##### 2. Assemble the extension module and the basic module.

The basic module must not be connected to voltage.

In our example, three extension modules are to be fitted to the basic module. We have chosen to fit the module with analogue outlets directly on the basic module and then the following module. The sequence is thus:

All the subsequent settings that affect the three extension modules are determined by this sequence.

When the two snap catches for the DIN rail mounting are in the open position, the module can be pushed into place on the DIN rail – regardless of where the module is on the row. Disassembly is thus done with the two snap catches in the open position.

Mounting and wiring - continued

### **3.2 Wiring**

Decide during planning which function is to be connected and where this will be.

##### **1. Connect inputs and outputs**

Remember the isolation amplifier.

If signals are received from different controls, e.g. heat recovery for one of the inputs, a galvanically insulated module should be inserted.

Here are the tables for the example:

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Discharge temperature - Sd-MT||**1**(AI 1)|**1 - 2**|Pt 1000|
|Suction gas temperature- Ss-MT||**2**(AI 2)|**3 - 4**|Pt 1000|
|Discharge temperature - Sd-IT||**3**(AI 3)|**5 - 6**|Pt 1000|
|Suction gas temperature- Ss-MT||**4**(AI 4)|**7 - 8**|Pt 1000|
|Thermostat sensor in plant room<br>- Saux1||**5**(AI 5)|**9 - 10**|Pt 1000|
|Suction pressure - P0-MT||**6**(AI 6)|**11 - 12**|AKS 2050-59|
|Condensing  pressure - Pc-MT||**7**(AI 7)|**13 - 14**|AKS 2050-159|
|Tap water temperature - Stw8||**8**(AI 8)|**19 - 20**|Pt 1000|
|Temp. gas cooler output Sgc||**9**(AI 9)|**21 - 22**|Pt 1000|
|Gas cooler pressure Pgc|**1**|**10**(AI 10)|**23 - 24**|AKS 2050-159|
|Refrigerant receiver, Prec CO2||**11**(AI 11)|**25 - 26**|AKS 2050-159|
|Hot gas dump||**12**(DO 1)|**31 - 32**|ON|
|Circulation pump tw||**13**(DO 2)|**33 - 34**|ON|
|||**14**(DO 3)|**35 - 36**||
|||**15**(DO 4)|**37 - 38**||
|MT Compressor 1 (VLT start)||**16**(DO 5)|**39 - 40 - 41**|ON|
|MT Compressor 2||**17**(DO6)|**42 - 43 - 44**|ON|
|MT Compressor 3||**18**(DO7)|**45 - 46 - 47**|ON|
|IT Compressor (VLT start)||**19**(DO8)|**48 - 49 - 50**|ON|
|Speed control MT compressor||**24**|**-**|0-10 V|
|Speed control IT compressor||**25**|**-**|0-10 V|

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Temp.  by-pased gas Shp||**1**(AI 1)|**1 - 2**|Pt 1000|
|Level switch, CO2 receiver||**2**(AI 2)|**3 - 4**|Open|
|Start/stop heat recovery tw||**3**(AI 3)|**5 - 6**|Closed|
|Outdoor temperature, Sc3|**2**|**4**(AI 4)|**7 - 8**|Pt 1000|
|Speed control LT compressor||**5**(AO 1)|**9 - 10**|0 - 10 V|
|Speed control, gas cooler fan||**6**(AO 2)|**11 - 12**|0 - 10 V|
|Speed control, pump - tw||**7**(AO 3)|**13 - 14**|0 - 10 V|
|||**8**(AO 4)|**15 - 16**||

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|MT compressor 1 safety circuits||**1**(AI 1)|**1 - 2**|Open|
|MT compressor 2 safety circuits||**2**(AI 2)|**3 - 4**|Open|
|MT compressor 3 safety circuits||**3**(AI 3)|**5 - 6**|Open|
|||**4**(AI 4)|**7 - 8**|Open|
|LT compressor 1 safety circuits||**5**(AI 5)|**9 - 10**|Open|
|LT compressor 2 safety circuits|**3**|**6**(AI 6)|**11 - 12**|Open|
|Heat recovery tw2||**7**(AI 7)|**13 - 14**|Pt 1000|
|Heat recovery tw3||**8**(AI 8)|**15 - 16**|Pt 1000|
|Signal to by-pass valve, Vrec||**9 (step 1)**|**25 - 26 - 27 - 28**|CCM T|
|Signal to high pressure valve, Vhp||**10 (step 2)**|**29 - 30 - 31 - 32**|CCMT|
|Signal  to 3-way valves V3gc||**11 (step 3)**|**33 - 34 - 35 - 36**|CTR|
|||**12 (step 4)**|**37 - 38 - 39 - 40**||

The function of the switch functions can be seen in the last column.

There are pressure transmitters AKS 32R and AKS 2050 available for several pressure ranges. Here there are two different ones. One up to 59 bar and two up to 159 bar.

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Discharge temperature - Sd-LT||**1**(AI 1)|**1 - 2**|Pt 1000|
|Suction gas temperature - Ss-LT||**2**(AI 2)|**3 - 4**|Pt 1000|
|External main switch||**3**(AI 3)|**5 - 6**|Closed|
|MT Compressors common safety<br>circuits||**4**(AI 4)|**7 - 8**|Open|
|IT Compressors common safety<br>circuits||**5**(AI 5)|**13 - 14**|Open|
|LT Compressors common safety<br>circuits||**6**(AI 6)|**15 - 16**|Open|
|Heat recovery tw4||**7**(AI 7)|**17 - 18**|Pt 1000|
|Suction pressure - P0-LT|**4**|**8**(AI 8)|**19 - 20**|AKS 2050-59|
|LT Compressor 1 (VLT start)||**9**(DO 1)|**25 - 26 - 27**|ON|
|LT Compressor 2||**10**(DO 2)|**28 - 29 - 30**|ON|
|Fan motors (VLT start)||**11**(DO 3)|**31 - 32 - 33**|ON|
|||**12**(DO 4)|**34 - 35 - 36**||
|3-way valve, tap water, Vtw||**13**(DO 5)|**37 - 38 - 39**|ON|
|||**14**(DO6)|**40 - 41 - 42**||
|Room fan||**15**(DO7)|**43 - 44 - 45**|ON|
|||**16**(DO8)|**46 - 47 - 48**||

The connections for the example can be seen here.

Warning! Keep signal cables separate from cables with high voltage.

The screen on the pressure transmitter cables must only be connected at the end of the controller.

The supply voltage for the pressure transmitter should be taken from the same module that receives the pressure signal.

Remember separate power supply for AK-XM 208C.

##### **2. Connect LON communication network**

The installation of the data communication must comply with the requirements set out in document RC8AC.

##### **3. Connect supply voltage**

The supply voltage is 24 V, and the supply must not be used by other controllers or devices. The terminals must not be earthed.

##### **4. Follow light-emitting diodes**

When the supply voltage is connected, the controller will go through an internal check. The controller will be ready in just under one minute when the light-emitting diode ”Status” starts flashing slowly.

##### **5. When there is a network**

Set the address and activate the Service Pin.

##### **6. The controller is now ready to be configured.**

*[Figurtekst: Internal communication · between the modules: · Quick flash = error · Slow flash = OK · Constantly On = error Quick flash = answer from gateway in 10 min. · after network installation · n Power Constantly ON = error · n Comm Constantly OFF = error · n DO1  n Status · n DO2  n Service Tool · n DO3  n LON External communication · n DO4  n I/O extension Communication to AK-CM 102 · n DO5  n Alarm Flash = active alarm/not cancelled · n DO6 Constant ON = Active alarm/cancelled · n DO7  n Display · n DO8  n Service Pin · Network installation · Status on output 1-8]*

### **4. Configuration and operation**

This section describes how the controller:

- is configured

- is operated

We have decided to work on the basis of the example we went through previously, i.e. MT-, LT-, IT-control, high pressure control, heat recovery and gas cooler.

### **4.1 Configuration**

### **4.1.1 Connect PC**

PC with the program “Service Tool” is connected to the controller.

For connecting and operating the "AK service tool" software, please see the manual for the software.

The first time the Service Tool is connected to a new version of a controller, the start-up of the Service Tool will take longer than usual while information is retrieved from the controller. Time can be followed on the bar at the bottom of the display.

The controller must be switched on first and the LED “Status” must flash before the Service Tool program is started.

##### **Start Service Tool programme**

Login with user name SUPV

When the controller is supplied the SUPV access code is 123. When you are logged into the controller, an overview of it will always appear.

Select the name **SUPV** and key in the access code.

In case the overview is empty: this is because the controller has not yet been set up.

The red alarm bell at the bottom right tells you that there is an active alarm in the controller. In our case the alarm is due to the fact that the time in the controller has not yet been set.

##### Refrigerating plant example:

We have decided to describe the setup by means of an example comprising an MT-, LT- and IT group. The example is the same as the one given in the "Design" section, i.e. the controller is an AK-PC 782A + extension modules.

##### **Compressor Group**

##### MT circuits

- 3 compressors with "cyclic". One speed controlled

- Safety monitoring of each compressor

- Common high-pressure monitoring

- Po setting -10°C, Po optimization from the system unit

##### LT circuits

- 2 x compressors with "cyclic". One speed controlled

- Safety monitoring of each compressor

- Common high pressure monitoring

- Po setting –30°C, Po optimization from the system unit

##### IT circuit

- 1 compressor, speed controlled

- Receiver set point 36 bar

##### **Fan in plant room**

- Thermostat control of fan in engine room

##### **Safety functions:**

- Monitoring of Po, Pc, Sd and superheat in suction line

- MT: Po max = -5°C, Po min = -35°C

- MT: Pc max = 110 bar

- MT: Sd max = 120°C

- LT: Po max = -5°C, Po min = -45°C

- LT: Pc max = 40 bar

- LT: Sd max = 100°C

- SH min =  5 °C, SH max = 35 °C

##### **Other:**

- Start/stop of heat recovery to Tw

- External main switch used

##### **High pressure controls:**

- Heat recovery for tap water

- Gas cooler

- Fans, speed controlled

##### **Receivers:**

There is also an internal main switch as a setting. Both this and the external main switch must be “ON” before any adjustment is made.

- Optimal CO2 reveiver pressure

- Monitoring CO2-level in the receiver

- Monitoring of high and low pressure

- Controlling the tap water receiver temperature, 55°C

The main switch will stop all regulations, including high-pressure regulation.

### **4.1.2 Authorization**

   - Press the orange set-up button with the spanner at the bottom of the display.

*[Figurtekst: 2. Select Authorization]*

When the controller is supplied, it has been set with standard authorization for different user interfaces. This setting should be changed and adapted to the plant. The changes can be made now or later. You will use this button again and again whenever you want to get to this display. On the left-hand side are all the functions not shown yet. There will be more here the further into the set-up we go. Press the line **Authorization** to get to the user set-up display.

##### 3. Change setting for the user ‘SUPV‘

Mark the line with the user name **SUPV.** Press the button **Change.**

##### 4. Select user name and access code

5. Carry out a new login with the user name and the new access code

This is where you can select the supervisor for the specific system and a corresponding access code for this person. The controller will utilize the same language that is selected in the service tool but only if the controller contains this language. If the language is not contained in the controller, the settings and readings will be shown in English. To activate the new settings you must carry out a new login to the controller with the new user name and the relevant access code. You will access the login display by pressing the icon at the top left corner of the display.

### **4.1.3 Unlock the configuration of the controllers**

2. Select Lock/Unlock configuration

The controller can only be configured when it is unlocked. The values can be changed when it is locked, but only for those settings that do not affect the configuration.

3. Select Configuration lock Press the blue field with the text **Locked**

##### 4. Select Unlocked

##### Select **Unlocked.**

### **4.1.4 System set-up**

2. Select System setup

##### 3. Set system settings

All settings can be changed by pressing in the blue field with the setting and then indicating the value of the required setting. In the first field you enter a name for what the controller will be controlling.  The text written in this field can be viewed at the top of all screens, together with the controller's address. When the time is set, the PC’s time can be transferred to the controller. When the controller is connected to a network, date and time will automatically be set by the system unit in the network. This also applies to change-over Daylight saving. In case of power failure, the clock will be kept running for at least 12 hours.

### **4.1.5 Set plant type**

2. Select plant type

###### General:

If you want to know more about the different configuration options, they are listed in the right column. The number refers to the number and picture in the column on the left.

As the screen only shows the settings and readings that are required for a given set-up, all possible settings have also been included in the right column.

Press the line **Select plant type** .

##### 3. Set plant type

##### 4. Further plant settings

##### 5. Disable alarm router

Our example: **3 - Plant type** The comments for the **Application selection** example are shown on the Select between one of the 4 applications where: following pages, in the midHP = High pressure control. MT=middle temperature. LT=low temperature. dle column. IT=parallel compression **3- after application selection Refrigerant** Only for CO2 systems. The refrigerant cannot be changed **Condenser fan control** Fan control is defined here: Step, step+speed, just speed or speed for the first fan+step for the rest In our example, the **No of fans** controller must regulate Set the number of relay outputs that will be used a Booster System, High **Heat recovery** Pressure Control and IT Select the type of heat recovery circuit (See section 5.7 for details.): Compressor. None Tap water Heat reclaim Subsequent options are Tap and heat then available, but only Heat Recovery (HRU) those options allowed by Heat Recovery (DIR) the current selection. **Oil management** Oil control enabled Choose between:

Our example: The comments for the example are shown on the following pages, in the middle column.

The settings for our example can be viewed in the display.

###### **Select quick set-up**

Here, you can reset all the controller settings back to the factory settings

There are several underlying pages. The black bar in this field tells you which of the pages is currently displayed.

###### **4 - Additional system definitions Compressor combinations**

Browse the pages using the + and - buttons.

###### **No of compressors**

Alarm transmission to the front-end can be disabled. This can be used to avoid “Alarm Router full” message when the controller is disconnected from the front-end. The menu can only be accessed if “show advanced settings” is enabled (present under “Select plant type”).

Set the number of compressor units that will be used

**External main switch** A switch may be connected for starting and stopping the regulation. (Also opens UPS selection) **Mon. Ext. Power loss** (signal from an UPS) Monitoring of external voltage. When selecting "yes", a digital input is allocated

###### **Alarm output**

Here you may set whether or not it should be an alarm relay, and which priorities will activate it

**I'm alive relay**

A relay will "release" if the regulation fails

###### **Night selected via DI**

The switch to night mode takes place when the signal is received **Show advanced settings** This function opens the advanced settings in the various menus **Comp. cap. out to AO**

To reenable the alarm transmission a re-scan must be executed from the front-end.

If selecting "yes", an analogue output indicates the running capacity

**Note:** The alarm transmission should only be disabled with great care as critical alarms will not be transmitted to the front-end. This could result in food loss or other damage.

### **4.1.6 Set control of suction group MT**

##### **3 - Reference mode**

- Displacement of suction pressure as a function of external signals 0: Reference = set reference + night offset + offset from external

- 0-10 V signal

##### 2. Select Suction group

##### 3. Set values for the reference

4. Set values for capacity control

The configuration menu in the Service Tool has changed now. It  shows the possible settings for the selected plant type.

In our example we select the settings: - P0 optimization - Suction set point =

- -10 °C

The settings are shown here in the display.

If a "Variable" or "screw compressor" is chosen in the first line, its type must be determined in the next line.

In our example we select: -VSD + single step - 3 compressors - Cyclic

**Note** : The two parameters ‘Control sensor’ and ‘Psuc max offset’ are used to configure an application with Low Pressure Multi Ejectors. They are only visible when no IT suction group has been defined“.

1: Reference = set reference + offset from P0 optimization **Setpoint** ( -80 – 30°C) Setting of required suction pressure in °C **Offset via Ext. Ref** Select whether a 0-10V external reference override signal is required **Offset at max input** (-100 – 100 °C) Displacement value at max. signal (10) **Offset at min input** (-100 – 100 °C) Displacement value at min. signal (0 V) **Offset filter** (10 - 1800 Sec)

Here you can set how quickly the reference must become effective **Night Offset via DI**

Select whether a digital input is required for activation of night operation. Night operation can alternatively be controlled via internal weekly schedule or via a network signal **Night Offset** (-25 – 25 K)

Displacement value for suction pressure in connection with an active night setback signal (set in Kelvin) **Max reference** (-50 – 80 °C) Max. permissible suction pressure reference **Min reference** (-80 – 25 °C) Min. permissible suction pressure reference

##### **4 - Compressor application**

Select one of the available compressor configurations here:

##### **Lead compressor type**

- Variable

- The following options are available for variable: – Speed – FlexxCO2-4 – FlexxCO2-6 – Digital Scroll – Stream 4 – Stream 6 – CRII 4 – CRII 6

- **No. of compressors** Set number of compressors (total)

##### **No. of unloaders**

Set number of unloader valves

**Ext. compressor stop** An external switch can be connected which will start and stop the compressor control

##### **Control sensor**

- Select the sensor for the compressor controller: -  “Po-MT” to control on the Po-MT sensor

-  “Po-MT + Psuc-MT” to control both “Po-MT” and “Psuc-MT”. The compressors will be controlled on the sensor that is most above to its reference **Psuc max offset** Set the difference between Psuc-MT and Po-MT references **Step control mode** Select coupling pattern for compressors: Cyclic: Runtime equalisation between compressors (FIFO) Best fit:  Compressors are cut in/out in order to make the best possible fit to actual load

##### **External coordination MT/LT**

Select "yes" if you want to coordinate with an external LT controller **Ext. Coordination MT/LT**

Visible if the controller is configured as "One pack + HP" ("plant type"  "application selection").

MT/LT coordination is automatically enabled for booster packs. For “One pack” applications, it can be enabled to operate using DI/DO.

##### **MT/LT coord. threshold**

Select when to start the MT compressor:

- “Neutral zone” to start when Po is in or above the neutral zone.

- “Reference” to start when above the Po reference.

- “Plus zone” to start when Po is in the plus zone.

##### **LT coord. stop**

Select when to stop the LT compressors:

- “MT compr.” to stop when MT is not ready.

• “MT Po” to stop when MT should start but is not ready. **Pump down** Select whether a pump down function is required on the last running compressor

**Synchronous speed** No: There will be two analogue outputs available. Yes: There will be one analogue output. **Early stop enable** Select this to limit the time that the last compressor is allowed to run inside the minus zone

##### **Early stop delay**

Set the maximum time that the last compressor is allowed to run inside the minus zone.

**Pump down limit Po** (-80 – +30 °C) Set the actual pump down limit **VSD min speed** (0.5 – 60 Hz) Min. speed where the compressor must cut out **VSD start speed** (20 – 60 Hz) Minimum speed for start of Variable speed drive (must be set higher than “VSD Min. Speed Hz”) **VSD max speed** (40 – 120 Hz) Highest permissible speed for the compressor motor **VSD safety monitoring** Select this if input for monitoring of the frequency converter is required **PWM period time** Period time for by-pass valve (on time + off time) **PWM Min. capacity** Minimum capacity in the period time (without a minimum capacity the compressor will not be cooled)

**PWM Start capacity**

Minimum capacity at which the compressor will start (must be set to a higher value than "PWM Min. capacity")

##### **Load shed limits**

Select which signal to be used for load limitation (only via network, a DI + network or two DI + network) **Load limitation period**

Set the maximum time permitted for load limitation

##### **Load shed limit 1**

Set max. capacity limit for load shed input 1 **Load shed limit 2**

Set max. capacity limit for load shed input 2

##### **Override limit T0**

Any load below the limit value is freely permitted. If the T0 exceeds the value, a time delay is started. If the time delay runs out, the load limit is cancelled

**Override delay 1** Max. time for load shed limit, if T0 is too high

##### **Override delay  2** Max. time for load shed limit, if T0 is too high **Easy PI Selection**

Group setting for the 4 control parameters: Kp, Tn, + acceleration and - acceleration. If the setting is set to “user defined” the 4 control parameters can be fine-tuned:

**Kp To** (0.1 – 10.0)

Amplifications factor for PI regulation

##### **Tn To**

Integration time for PI-regulation

**+ Zone acceleration (A**<sup>**+**</sup> **)** Higher values result in a faster regulation **- Zone acceleration (A**<sup>**-**</sup> **)** Higher values result in a faster adjustment

**Advanced settings To filter** Reduce fast changes in the To reference

##### **Pc filter**

Reduce fast changes in the Pc reference

**Initial start time** (15 – 300 s)

The time after start-up where the cut-in capacity is limited to the first compressor step.

**Unloading mode** Select whether one or two capacity controlled compressors are allowed to be unloaded at the same time at decreasing capacity.

**Comp. running DO** If "yes" is selected, an output is reserved that shows if the compressors are operating.

##### **AO filter**

Reduce fast changes at the analogue output

**AO max. limit** Limit the voltage on the analogue output.

##### 5. Set values for capacity of the compressors

6. Set values for main step and any unloaders

##### 7. Set values for safe operation

The compressor capacity is set in displaced volume per hour. m<sup>3</sup> /h. See compressor data.

In our example there are no unloaders and hence no changes.

- In our example we select: - Safety limit for discharge temperature = 120°C

- - Safety limit for high condensing pressure = 100 bar

- Safety limit for low suction pressure =  -40°C

- - Alarm limit for high suction pressure = -5°C

- Alarm limit for min. and max. superheat, respectively = 5 and 35 K.

##### **5 - Compressors**

In this screen, the capacity distribution between the compressors is defined. Capacities that need to be set depend upon the “compressor application” and “Step control mode” that has been selected. **Nominal capacity** (1 – 1000 m<sup>3</sup> /h) Set the nominal capacity for the compressor in question. For compressors with variable speed drive the nominal capacity must be set for the mains frequency (50/60 Hz)

**Unloader**

Number of unload valves for each compressor (0-3)

##### **6 - Capacity distribution**

The installation is dependent on the combination of compressors and coupling pattern

**Main step** Set the nominal capacity of the main step (Set the percentage of the relevant compressor’s nominal capacity) 0 – 100% **Unload**

Readout of the capacity on every unloading 0 – 100%

**7 - Safety Emergency cap. day** The desired cut-in capacity for day operation in the case of emergency operations resulting from error in the suction pressure sensor/ media temperature sensor **Emergency cap. night** The desired cut-in capacity for night operations in the case of emergency operations resulting from error in the suction pressure sensor/ media temperature sensor

**Sd max limit** Max. value for discharge gas temperature. 10 K below the limit, the compressor capacity should be reduced and the entire condenser capacity will be cut in. If the limit is exceeded, the entire compressor capacity will be cut out

**Pc Max limit** Maximum value for the condenser pressure in bar. The entire condenser capacity will be cut-in, and the compressor capacity reduced 3-4 bar below the limit. 4 bar is used for transcritical Pc Max lmit (PcMax > 67 bar), 3 bar is used for subcritical Pc Max limit. A smooth transition from 3 to 4 bar is guaranteed around the Pc Max limit = 67 bar.

If the limit is exceeded, the entire compressor capacity will be cut out. **Tc max. limit** Limit value read in °C (If selected for display in the condenser configuration) **Pc Max alarm delay** Time delay for the alarm Pc max. **T0 Min limit** Minimum value for the suction pressure in °C If the limit is reduced, the entire compressor capacity will be cut out **T0 Max alarm** Alarm limit for high suction pressure P0 **T0 Max delay** Time delay before alarm for high suction pressure P0 **Safety restart time** Common time delay before restarting the compressor. (Applicable to the functions: "Sd max. limit", Pc max. limit" and "P0 min. limit) **SH Min alarm** Alarm limit for min. superheat in suction line **SH Max alarm** Alarm limit for max. superheat in suction line **SH alarm delay** Time delay before alarm for min./max. superheat in suction line

##### 8. Set monitoring of compressor

##### 9. Set operation time for compressor

##### 10. Set Misc. functions

In our example we use: - Common high-pressure pressure control for all compressors - One general safety monitoring unit for each compressor

(The remaining options could have been selected if specific safety controls for each compressor had been required).

Set min. OFF-time for the compressor relay. Set min. ON-time for the compressor relay. Set how often the compressor is allowed to start.

The settings only apply to the relay that cuts the compressor motor in and out.

They do not apply to unloaders.

If the restrictions overlap, the controller will use the longest restriction time.

In our example we do not use these functions.

##### **8 - Compressor safety Common safety**

Choose whether an overall, common safety input for all compressors is desired. If the alarm is activated, all compressors will be cut out.

**Oil pressure etc** Define here whether this type of protection should be connected. For "General" there is a signal from each compressor. **Sd sensor pr. compressor** Select whether an Sd measurement should be made for each individual compressor

**Max discharge temp.** Cut-out temperature.

**Sd compressor alarm delay** Delay time for the alarm **Sd compressor safety cutout**

Set whether safety cut-out should be enabled

##### **9 - Minimum operation times**

Configure the operation times here so "unnecessary operation" can be avoided. Recycle time is the time interval between two consecutive starts. **Safety timer Cutout delay**

The time delay resulting from drop-out of automated safety measures and until the compressor-error is reported. This setting is common for all safety inputs for the relevant compressor.

**Recycle delay** Minimum time before a compressor should be OK after a safety cut-out. After this interval it can start again.

##### **10 - Misc. functions**

##### **Ctrl. of Injection On**

DO: Select this function if a relay must be reserved for the function. (The function must be wired to controllers with expansion valves in order to close liquid injection for the safety cut-out of the last compressor.)

Network: The signal is sent to the controllers via data communication. **Compressor start delay** Delay time for compessor start **Injection Off delay** Delay time for "Injection off" **Liq. inj suction line** Select this function if a liquid injection is required in the suction line in order to keep the discharge gas temperature down. Regulation can be done either using a solenoid valve and a TEV, or using an AKV valve.

**AKV OD suction line** Readout of opening degree of the valve in % **Inject start SH** Superheat value where the liquid injection starts **Inject diff SH** Differential of superheat for the injection control **Inject start Sd temp.** Start temperature for liquid injection in suction line **Inject diff Sd temp.** Differential when adjusted on Sd **SH Min suction line** Minimum superheat in suction line **SH Max suction line** Maximum superheat in suction line **AKV period time** Periode time for AKV valve **Inject delay at start up** Delay time for liquid injection at start-up

Afterwards, the settings for the LT group and IT group continue. In principle, the same settings are carried out.

### **4.1.7 Set oil management**

2. Set Oil management

##### 3. Set Oil receiver

##### 4. Set oil separator

In our example, oil management has not been included.

The settings are only displayed for information purposes and apply to the “Fixed pressure” control which is configured in the "Plant Type display".

In our example, we have two level switches in the receiver. Both one high and one low.

The process is as follows: When a signal is given from the level switch, the discharging process to the receiver commences. This pulsates three times with one minute intervals. Each pulse lasts one second. If the level switch does not register an oil drop at this point, an alarm is given when the delay time has expired.

##### **3**

**Level switch receiver** Define the desired level sensors: High Both Low and High **Level alarm delay** Delay time for level alarm **Actual pressure** Measured value **Actual state** Status of oil separation **Cut out pressure** Receiver pressure for shutting off oil **Cut in pressure** Receiver pressure for turning on oil **High alarm limit** An alarm is given if a higher pressure is registered **High alarm delay** Time delay for alarm

**Low alarm limit**

An alarm is given if a lower pressure is registered **Low alarm delay** Time delay for alarm

**4 Separator** Select whether there should be one shared separator for all the compressors or two separators (MT and IT)

##### **Level detection**

Select whether the separator is to be controlled by "Full sequence", "To Level" or "low and high" level switches

##### **Level alarm delay**

Alarm given when using a level switch for low level

##### **Repeat oil return cycle**

Time period between repeat emptying processes from the separator if the level switch stays at high level

##### **No oil sep. alarm delay**

Alarm delay when a signal is given that oil is not being separated ("high" level contact not activated).

##### **No of periods**

No. of times the valve should open in emptying sequence

##### **Period time**

Time between valve openings

##### **Open time**

The open time of the valve

### **4.1.8 Set up control of condenser fans**

##### 2. Select Condenser fan control

##### 3. Set control mode and reference

##### 4. Set values for capacity regulation

In our example, the condenser pressure is controlled on the basis of the Sgc and from Sc3 (floating reference). The settings shown here in the display.

In our example we use a number of fans that are all speed-controlled in parallel. The settings are shown here in the display.

For your information, the function ”Monitor fan safety” will require an input signal from each fan.

##### **3 - Sensor and Reference Control sensor**

Sgc: The temperature at the outlet of the gas cooler S7: Medium temperature is used for regulation **Reference Mode**

Choice of condenser pressure reference:

Fixed setting: Used if a permanent reference is required = “Setting” Floating: Used if the reference is changed as a function of Sc3 the external temperature signal, the configured "Dimensioning tm K"/"Minimum tm K" and the actual cut-in compressor capacity. (Floating is recommended for CO2 and heat recovery.)

##### **Setpoint**

Setting of desired condensing pressure in temperature

##### **Min. tm**

Minimum average temperature difference between Sc3 air and Pc condensing temperature with no load

##### **Dimensioning tm**

Dimensioning average temperature differential between Sc3 air and Pc condensing temperature at maximum load (tm difference at max load, typically 2-4 K)

##### **Sgc max reference**

Maximum permissible gas cooler outlet temperature. This function limits the reference for Sgc when heat recovery is not active

##### **Show Tc**

Set whether Tc should be displayed

##### **Forcing fan speed via DI**

Set to "Max Speed" or "Prop%CMP" for using an external DI to force fan speed (at max speed or proportionally to the compressor load), close V3gc and calculate Pgc pressure reference based on Sgc sensor. When DI is not activated, fan and V3gc are controlled as usual.

##### **4 - Capacity control Capacity control mode**

Select control mode for condenser: Step: Fans are step-connected via relay outputs Step/speed: The fan capacity is controlled via a combination of speed control and step coupling Speed: The fan capacity is controlled via speed control Speed 1.step: First fan speed controlled, rest step coupling 2 groups with speed: The capacity is divided into groups

**No of fans**

Set number of fans

(If two groups are selected, this setting is the number in group 1). **Number of fans in group 2**

The number in group 2 must be greater than or equal to the number in group 1.

##### **Speed limit for group 1**

The speed can be limited to minimize the noise

**Monitoring  fan safety** Safety monitoring of fans. A digital input is used to monitor each fan.

##### **Fan speed type**

VSD (and normal AC motors)

EC motor = DC controlled fan motors

**VSD start speed**

Minimum speed for start of speed control (must be configured higher than "VSD Min. Speed").

**VSD min Speed**

Minimum speed whereby speed control is cut out (low load). **VSD safety monit.**

Choice of safety monitoring of frequency converter. A digital inlet is used for monitoring the frequency converter.

##### **EC Start capacity**

The regulation awaits this need to arise before supplying voltage to the EC motor **EC min.**

Voltage value at minimum capacity (20% = 2 V @ 0 – 10 V) **EC max.**

Voltage value at 100% capacity (80% = 8 V @ 0 – 10 V) **EC abs. max.** Permissible live voltage for EC motor (overcapacity)

**Absolut max Sgc** Max value for temperature at Sgc.  If the value is exceeded, the EC voltage will be raised to the value in “EC Voltage abs. max.” **Fan control mode** Choice of control strategy P-band: The fan capacity is regulated via P-band control. The P band is "100/Kp"

PI-Control: The fan capacity is regulated by the PI controller

**Kp** Amplification factor for P/PI controller

**Tn** Integration time for PI controller

**Capacity limit at night** Setting of maximum capacity limit during night operations. Can be used to limit fan speed at night in order to limit the noise level **V3gc**

Indicates whether a gas by-pass valve is used on the gas cooler. On/off: Three-way valve controlled by a relay Step valve: Modulating CTR type three-way valve Voltage: Three-way valve, e.g. controlled using 0 – 10 V at on/off:

**Bypass low limit - Shp** If the sensor Sgc records a temperature that is lower than the selected value, the gas will be routed outside of the gas cooler (e.g. start-up during very low ambient temperatures) **Bypass min. off time** Minimum time during which the gas must be fed through the gas cooler before bypass is permitted. At Stepper and Voltage:

**Kp**

Amplifcation factor for the PI controller.

**Tn** Integration time for PI controller. **Min. opening degree Max. opening degree**

### **4.1.9 Set-up of high pressure control**

##### 2. Select HP control

##### 3. Set regulation values

##### 4. Set ejector function

The settings are shown here in the display

We do not use ejector control in our example.

##### **3 - HP control**

##### **Vhp output type**

Select the signal type for controlling the high pressure valve:

- Voltage signal

- Stepper motor signal via AK-XM 208C

- 2 Stepper motor signals for parallel valves **Extra capacity offset**

Adjust how much the pressure shall be increased, when the "Extra refrigeration capacity ("extra compressor")" function is activated **Pgc min.**

Min. acceptable pressure in the gas cooler

**Pgc max.**

Max. acceptable pressure in the gas cooler

##### **Advanced settings**

**Vhp min. OD** Restriction of the valve's closing degree **Pgc max. limit P-band**

P-band under "Pgc max" where the valve's opening degree is increased

##### **dT Subcool**

Desired subcooling temperature

##### **Kp**

Amplification factor

##### **Tn**

Integration time

**Pgc HR min.**

Read the min. acceptable pressure in the high pressure circuit during heat recovery

##### **Pgc HR max**

Read permissible pressure during heat recovery

Note: Anyway "Pgc ref" is allowed to be higher than "Pgc HR Max", when "Extra refrigeration capacity ("extra compressors") function is activated.

##### **Ramp down bar/min.**

Here you may select how quickly the reference must be changed after a completed heat recovery

**Temp. at 100 bar**

Temperature at 100 bar. Here you may define the regulation curve during transcritical operation. Set the required temperature value.

##### **4 - Ejector control**

Select the Multi Ejector's capacity. The size will then be shown for each valve’s capacity. The function is described on page 118.

In the next display, the capacity is adjusted for liquid ejectors. The next display is not visible if liquid ejectors are configured in the previous display.

If the regulation is stopped during high-pressure regulation, the pressure will rise.

The system must be dimensioned to the higher pressure; otherwise there will be a loss of charge.

### **4.1.10 Set up control of receiver pressure**

##### **3. Receiver reference**

##### **Prec ref Mode**

2. Select Receiver control

##### 3. Set parameters for receive reference

Select one of the available reference options for the IT compressor control:

- "Fixed SP” for a constant reference,

- “Ext. Offset” for a constant reference plus an offset from an analogue input,

- “IT Optimize” for automatic calculation of the optimum reference,

- “Delta P” for a constant offset above MT suction pressure reference (using Delta P reference parameter).

##### **Prec set point / Prec reference**

Select the setpoint or display actual reference for the receiver pressure

##### **Trec set point / Prec reference**

Display saturated temperature for Prec setpoint / Prec reference

##### **Prec max.**

Max. permissible pressure in the receiver. Exceeding this limit results in an alarm.

**Prec min.**

Min. permissible pressure in the receiver. Overpassing this limit results in an alarm

##### **Enable Delta P min**

When enabled, receiver reference is calculated to guarantee minimum pressure difference with MT suction pressure reference.

##### **Delta P reference**

Minimum pressure difference between actual receiver reference and MT suction pressure reference.

##### **Show Trec on overview**

Set whether Trec should be shown in overview display

##### **Ext. Offset max**

When the reference mode is “Ext. Offset”, then set the maximum offset.

##### **Prec min  reference / Prec max reference**

When the reference mode is “IT optimize” or “Delta P” then set the minimum and maximum values for receiver reference. Select this to minimize the floating range of receiver pressure indicating the amount of gas entering the receiver.

##### **AC support**

Enable request signal (DI) and release signal (DO) for air conditioning AC. When AC is released, the controller is expecting AC load to contribute to receiver load.

##### **AC Prec min ref / AC Prec max ref**

Additional limitation to the pressure range of receiver reference that only applies when AC is requested via DI. Select the option to guarantee a maximum and minimum AC temperature.

##### **Receiver inlet min vapour**

Maintains a minimum gas pressure in the receiver. The % value indicates the minimum allowed quality of vapour at receiver inlet.

##### 4. Set control parameters

##### **4. Receiver control**

##### **Monitor liquid level**

Choose whether liquid level should be monitored:

- “Low Level Switch”

- “High Level Switch”

- “High and Low Level Switch”

##### **Liquid alarm delay**

Time delay for the alarm

##### **Receiver Valve**

The following settings are specific to Vrec receiver valve(s):

##### **Vrec output type**

Select the Vrec output type for gas by-pass valve:

- “1 Stepper” for a single stepper motor signal via AK-XM 208C

- “2 Stepper (synchronic)” for two stepper motor signals operated simultaneously

- “2 Stepper (sequential)” for two stepper motor signals operated in sequence

- “Voltage (AO)” for a voltage signal

##### **Vrec min. OD**

Limitation of the Vrec valve's closing degree

##### **Vrec max. OD**

Limitation of the Vrec valve's opening degree

##### **Easy PI selection**

Group setting for the control parameters: Kp, Tn. If the setting is set to “user defined”, the control parameters can be fine-tuned:

##### **Vrec Kp**

Amplification factor for PI regulation

##### **Vrec Tn**

Integration time for PI regulation

##### **Hot gas dump enable**

Select whether hot gas should be supplied if the receiver pressure falls too low

##### **Hot gas dump cut-in**

Receiver pressure at which hot gas is turned on

##### **Hot gas dump delta**

Difference at which hot gas is turned off again

##### **IT Coordination**

The following settings are specific for coordinating with suction group IT:

##### **IT Smart start enable**

Enable automatic calculation of  “IT Start Vrec OD”, depending on Vrec valve types, IT size and operating conditions.

##### **IT Start Vrec OD**

Opening degree for the Vrec valve when the IT compressor is to start.

##### **IT Start tuning**

Allow the user to modify “IT Start Vrec OD” when “IT Smart start” is enabled. A value of zero makes the controller aim for minimum speed of the first IT compressor, a negative value makes the IT start earlier (lower flow rate) and a higher value makes the IT start later (higher flow rate).

##### **IT Start delay filter**

Time constant for filtering Vrec OD when it is compared against "IT Start Vrec OD" for starting the IT compressors

##### **IT End delay**

The duration that the IT compressor must have been stopped before regulation is transferred to Vrec.

##### **IT Comp. Sgc min.**

The temperature limit for operation with an IT compressor. This will not start when a lower value is detected, regardless of the opening degree of the Vrec valve.

##### **Emergency Action**

Enable specific control emergency action from other controllers as a result of too low/high receiver pressure.

##### **Vhp close on high Prec**

Enable override of maximum OD for high pressure valve Vhp as action against high receiver pressure.

##### **Vhp open on low Prec**

Enable override of minimum OD for high pressure valve Vhp as action against low receiver pressure.

##### **MT Cut-on high Prec**

Enable to cut off MT compressor capacity as action against high receiver pressure.

### **4.1.11 Set-up Receiver Reference with Low Pressure Multi Ejectors**

Designed to work with Low Pressure Multi Ejectors, this mode is available when the MT suction control is configured to alternate between two pressure transducers (Po-MT and PsucMT).

Receiver reference is always calculated as offset from MT suction reference. It uses a higher or a lower offset, determined by a digital input.

The related parameters are explained to the right.

For information on how to set these parameters, please see the application guide: “Low pressure lift ejector system”

##### **Delta P reference**

Display the current pressure difference between the Prec reference and Po-MT reference.

##### **LP Ej Delta P low**

Specify the pressure difference between the Prec reference and Po-MT reference for the lower Prec reference (DI deactived).

##### **LP Ej Delta P high**

Specify the pressure difference between the Prec reference and Po-MT reference for the higher Prec reference (DI active).

##### **LP Ej Delta P high delay**

After deactivating the digital input for the reference "Delta P high", the parameter “LP Ej Delta P high delay” delays switching back to the reference "Delta P low" for the specified time. After activating the digital input, a 30 sec delay is always applied to switching back to the reference "Delta P high".

### **4.1.12 Set up control of heat recovery**

##### 2. Select heat circuits

##### 3. Setup values for (hot) tap water circuit

When in the menu "Select Plant type", heat recover is selected, the "Heat circuits" menu appears.

The menu for hot tap water is empty when regulation is only carried out on heat reclaim for room heating.

**3 - Heat recovery - (Hot) Tap water circuit** (settings are available only when there shall be regulated on a circuit for tap water) **V3tw output type**

DO: The valve is controlled by a relay output

Stepper (On/Off): The valve is controlled by a stepper valve **Control mode** : Here the regulation of the circuit can be started (auto) and stopped (off)

**Setpoint** : The required temperature for the sensor Stw8 can be set here

##### **Use ext. ref. offset**

A 0 – 10 V signal must displace the temperature reference **Max. Ext. ref. offset**

Reference displacement at max. signal (10 V)

**Thermostat band** : The acceptable temperature variation around the reference:

**Control signal**

Choose between:

Stw8: if regulation shall be done using only this sensor Stw4-Stw3: if the controller shall regulate using this temperature difference, until the Stw8 reference is met. (During Stw4-Stw3 regulation, the pump must always be speed-regulated).

Stw8 + Stw8A: if two temperature sensors are installed in the hot water receiver

Stw4: regulation is done using this sensor

**Delta T:** Setpoint as difference in temperature during Stw4-Stw3 regulation

**Variable speed:** Here the pump type is selected. Either variable speed or on/off

**Advanced settings:**

The following options are made available:

- Flow switch: Must normally be selected for safety purposes

Flowswitch delay: Duration of stable signal before the new status is used in the regulation

Kp: Amplification factor

Tn: Integration time Enable Pump Exerciser: run the water pump for 30 s at minimum speed (atleast 30%) after 24 h of inactivity.

Min. pump speed: Pump speed for start/stop

Max. pump speed: The pump's max. permissible speed

##### 4. Setup values for heat reclaim circuit

The menu for room heating is empty when regulation is only carried out on hot tap water.

##### **4 - Heat recovery - Heat reclaim circuit V3hr output type**

DO: The valve is controlled by a relay output Stepper (On/Off): The valve is controlled by a stepper valve

##### **Heat reclaim type for heating**

Here you define how the gascooler pressure (HP) shall be regulated when the recovery circuit for heating requires heat:

- No HP offset (simple control)

- HP offset. Here the controller must receive a voltage signal. The offset values that apply to the max. value must be defined in the heat circuit settings. See next page.

- Max heat reclaim. Here the controller must receive a voltage signal, but the regulation is increased to also control pump activation and deactivation and the by-pass valve.

**Control mode** : Here the regulation of the circuit can be started (auto) and stopped (off) **Setpoint** : Here the required temperature of sensor Shr8 (or Shr4) is set

##### **Use ext. ref. offset**

A 0 – 10 V signal must displace the temperature reference **Max. Ext. ref. offset**

Reference displacement at max. signal (10 V) **Thermostat band** : The permissible temperature variation around the reference:

**Control signal** : Choose between: Shr8: if regulation shall be done using only this sensor Shr4-Shr3: if the controller shall regulate using this temperature difference, until the Shr8 reference is met. (During Shr4-Shr3 regulation, the pump must always be speed-regulated.) Shr4: regulation is done using this sensor

**Variable speed:** Here the pump type is selected. Either variable speed or on/off

**Heat consumers** : (Only when the condensation pressure shall be increased during heat recovery). The number of signals that can be received are set here. The signal can be either 0 – 10 V or 0 – 5 V. (Settings under "Advanced" will be used 0 – 100% for the signal)

##### **Heat consumer filter**

Reduce fast changes in heat consumer signal

##### **Additional heat output**

The function will reserve a relay. The relay will energize when the signal for the heat removers reaches 95%.

**Advanced settings** : The following options are made available: Flow switch: Must normally be selected for safety purposes Flowswitch delay: Duration of stable signal before the new status is used in the regulation Kp: Amplification factor Tn: Integration time Tc max HR: Value at which the bypass of the gas cooler will terminate (also known as “V3gc bypass stop T” in Direct heat reclaim  settings) HR PUMP CONTROL Enable Pump Exerciser: run the water pump for 30 s at minimum speed (at least 30%) after 24 h of inactivity. Min. pump speed: Pump speed for start/stop Max. pump speed: The pump's max. permissible speed HR stop limit: Signal in % at which the pump is stopped again HR start limit: Signal in % at which the pump is started HR end delay - MT stop: time delay after last MT compressor stops before the pump goes in shutting down mode (heat recovery being not available) HP CONTROL Pgc HR min: Basic reference for the pressure when external voltage signal is received. Pgc HR max: Max pressure reference  when external voltage signal is received. Note: Anyway "Pgc ref" is allowed to be higher than "Pgc HR Max", when "Extra refrigeration capacity ("extra compressors") function is activated. Ref. offset low limit: Signal in % at which "Pgc HR min." comes into force Ref.offset high limit: Signal in % at which "Sgc max" value is used BYPASS CONTROL (at on/off regulation) V3gc bypass stop limit: Signal in % at which the gas cooler connects again after completed disconnect V3gc bypass start limit: Signal in % at which the gas cuts out

5. Setup values for Direct heat reclaim circuit **5 - Heat recovery - Direct Heat reclaim (DIR) Control mode** : Here the regulation of the circuit can be started (Auto) and stopped (OFF) **Show advanced settings:** Parameters indicated by “(Advanced Settings)” appear when set to Yes. For direct heat reclaim the user interface allows flexible feature selections for heat recovery. Check section 5.7.4 for more details. === Config. Settings=== **Start signal:** Select the signal used by the controller to start (and stop) heat recovery: • Only Digital Input • HC Analog + Digital: Heat consumer analog input and digital input are both required to start/keep heat recovery. **HP offset signal:** Select whether the heat consumer analog input is used to offset the gas cooler pressure and temperature references during heat recovery. **GC Bypass signal:** Enable gas cooler bypass using On-Off V3gc via heat consumer analog input. **DO recirculator:** Enable DO for the secondary fluid recirculation. When disabled circulation during heat recovery needs to be guaranteed by the external controller. **V3hr output type:** Select the output type for V3hr valve: • DO: The on/off valve is controlled by a relay output • Stepper: The valve is controlled by a stepper output • AO: The modulating valve is controlled by an analog signal === Analog Input === When Start signal, HP offset signal, Gc Bypass signal are set to use an analog input, the following user settings may be available: **Heat consumers:** The number of signals that can be received are set here. These signals can be either 0 – 10 V or 0 – 5 V. **Heat consumer filter:** (Advanced Settings) Reduce fast changes in heat consumer signal **HR start limit:** Signal limit in % at which the heat recovery will start (default 10%) **HR stop limit:** Signal limit in % at which the heat recovery will stop (default 5%)

=== Temp. Control === This section defines user settings for temperature regulation of heat recovery.

**Temp. Ctrl. Actuator:** Set which actuator is used for temperature control.

- None (Extern AI): None of the heat circuit actuators are used for temperature control

- CO2 valve (V3hr): V3hr is used for temperature control (V3hr must be a modulating bypass valve)

- Sec.fl. valve (V3sf): V3sf is used for temperature control (V3sf must be a modulating bypass valve)

**V3sf output type:** Shows the output type for V3sf valve:

• AO: The modulating valve is controlled by an analog signal **Controlled temp.:** Control sensor used for temperature control (not selectable)

**Setpoint Tctrl.:** Set the required temperature setpoint for the current controlled temperature sensor

**Kp:** (Advanced Settings) Temperature control Amplification factor **Tn:** (Advanced Settings) Temperature control Integration time **Enable S4 check:** Enable safety check, stopping heat recovery when Shr4 is too high (“S4 check”)

**S4 check limit:** Maximum limit for Shr4 sensor value before heat recovery is stopped. “Shr4 check” fails when the sensor value is above this limit.

=== CO2 Delta P Control === Collection of settings for Delta P control across the heat recovery heat exchanger. Not available when V3hr is already used for temperature control.

**CO2 Delta P Control:** User can configure Delta P control **DPhr setpoint:** The setpoint for the Delta P control **V3hr max. OD:** Max opening degree of V3hr **P1 source:** (Advanced Settings) User selection of inlet pressure sensor between Pc or Phr1

**P2 source:** (Advanced Settings) User selection of outlet pressure sensor between Pgc or Phr2

**Kp:** (Advanced Settings) Delta P control Amplification factor **Tn:** (Advanced Settings) Delta P control Integration time

##### === Other Settings ===

**Flow switch:** (Advanced Settings) Must normally be selected for safety purposes

**Flow switch delay:** (Advanced Settings) Duration of stable signal before the new status is used in the regulation

**HR end delay - MT stop:** time delay after last MT compressor stops before the heat recovery goes to shutdown mode (heat recovery being not available)

=== GC Bypass control === Collection of gascooler bypass settings **V3gc valve:** Indicates whether an On/Off gas bypass valve is used on the gas cooler. **V3gc bypass stop limit:** (Advanced Settings) Signal in % at which

the gas cooler connects again after completed disconnect (default 80%)

**V3gc bypass start limit:** (Advanced Settings) Signal in % at which the gas cuts out (default 95%)

**V3gc bypass stop T.:** (Advanced settings) Value at which the bypass of the gas cooler will terminate (also known as “Tc max HR” in Condenser fan control settings)

**V3gc bypass min off time:** (Advanced Settings) Minimum time during which the gas must be fed through the gas cooler before bypass is permitted.

=== HP control === Collection of gascooler pressure reference settings **Ref. offset low limit:** Signal in % at which "Pgc HR min." comes into force (default 25%)

**Ref.offset high limit:** Signal in % at which "Sgc max" value is used (default 70%)

**Pgc max.:** Max. acceptable pressure in the gas cooler

**Pgc max. limit P-band:** P-band under "Pgc max" where the valve's opening degree is increased

**Pgc HR max:** Max pressure reference when external voltage signal is received.

Note: Anyway "Pgc ref" is allowed to be higher than "Pgc HR Max", when "Extra refrigeration capacity ("extra compressors") function is activated.

**Pgc HR min:** Basic reference for the pressure when external voltage signal is received.

**Pgc min.:** Min. acceptable pressure in the gas cooler

### **4.1.13 Set up KPI and COP calculation**

##### 2. Select KPI setup

In our example, KPI control is not used. The settings are included here for information.

##### **2 - KPI Setup**

**KPI calculation** (KPI = Key Performance Indicator) If "Yes" is selected, the function will optionally request a signal from the sensor liquid line (Sliquid temp)

##### **Selected RFG** The system’s refrigerant type is read here **Total swept volume MT**

The system’s refrigerant type is read here

The total swept volume for all of the MT compressors is read here **Total swept volume IT**

The total swept volume for all of the IT compressors is read here **Total swept volume LT**

The total swept volume for all of the LT compressors is read here **HR active**

The system's Heat Recovery state (active or not) is read here

**Coldest cabinet MT**

Set the desired temperature of the MT circuit’s coldest refrigeration case

**Coldest cabinet LT**

Set the desired temperature of the LT circuit’s coldest refrigeration case

### **4.1.14 Set up Display**

##### 2. Select Display setup

##### 3. Define which readings are to be shown for the individual outputs

In our example, separate displays are not used. The setting is included here for information.

##### **3 - Display set-up**

##### **Display**

The following can be read for the four outputs: Comp. control sensor P0 in temperature P0 in barSs Sd Cond. control sensor Tc Pc bar S7 Sgc Pgc bar Prec bar Trec Speed Compressor

##### **Unit readout**

Choose whether readings are to be in SI units (°C and bar) or (USunits °F and psi)

### **4.1.15 Set-up Functions for General purpose**

2. Select General purpose

3. Define number of required functions

In our example we select one thermostat function for temperature control in the compressor room.

The following number of different functions can be defined: 10 thermostats 5 pressostats 5 voltage signals 10 alarm signals 6  PI-regulations

### **4.1.16 Separate thermostats**

1. Select thermostats

2. Select actual thermostat

##### **3 - Thermostats**

The general thermostats can be used to monitor the temperature sensors that are used, as well as 4 extra temperature sensors. Each thermostat has a separate outlet to control external automation. **For each thermostat adjust:**

- Whether the thermostat should also be shown in overview

display 1. (The function is always shown in overview display 2)

   - Name

3. Define the required thermostat functions

In our example we select one thermostat function for monitoring the plant room temperature.

We have subsequently entered a name for the function.

- Which of the sensors /(Signal) is used

**Actual temp** . Temperature measurement on the sensor that is attached to the thermostat

**Actual state** Actual status on the thermostat outlet **Cut out temp.** Cut-out value for the thermostat **Cut in temp.** Cut-in value for the thermostat **High alarm limit** High alarm limit **Alarm delay high** Time delay for high alarm **Alarm text high** Indicate alarm text for the high alarm **Low alarm limit** Low alarm limit **Alarm delay low** Time delay for low alarm **Alarm text low** Indicate alarm text for low alarm

### **4.1.17 Separate pressostats**

1. Select pressostats

2. Select actual pressostat

In our example, separate pressostat functions are not used.

**3 - Pressostats** Settings as the thermostats

3. Define the required pressostat functions

### **4.1.18 Separate voltage signals**

1. Select Voltage inputs

2. Select actual voltage signal

3. Define the required names and values attached to the signal

In our example we do not use this function, so the display has been included for your information only. The name of the function may be xx and further down in the display the alarm texts may be entered.

The values ”Min. and Max. Readout” are your settings representing the lower and upper values of the voltage range.  2V and 10V, for example. (The voltage range is selected during the I/O setup). For each voltage input defined the controller will reserve a relay output in the I/O setup. It is not necessary to define this relay if all you require is an alarm message via the data communication.

##### **3 - Voltage inputs**

The general volt inlet can be used to monitor external voltage signals. Each volt inlet has a separate outlet to control external automatic controls.

Set the number of general voltage inputs, specify 1-5:

**Show on overview Name Select sensor (signal, voltage)** Select the signal which the function should use **Actual value** = readout of the measurement **Actual state** = readout of outlet status **Min. readout** State readout values at minimum voltage signal **Max. readout** State readout values at maximum voltage signal **Cutout** Cut-out value for outlet (scaled value) **Cutin** Cut-in value for outlet (scaled value) **Cutout delay** Time delay for cut-out **Cut in delay** Time delay for cut-in **High alarm limit** High alarm limit **High alarm delay** Time delay for high alarm **High alarm text** Set alarm text for high alarm **Low alarm limit** Low alarm limit **Low alarm delay** Time delay for low alarm **Low alarm text** Indicate alarm text for low alarm

### **4.1.19 Separate alarm inputs**

1. Select General alarm inputs

2. Select actual alarm signal

3. Define the required names and values attached to the signal

In our example we select one alarm function for monitoring the liquid level in the receiver. We have subsequently selected a name for the alarm function and for the alarm text.

**3 - General alarm input** This function can be used to monitor all kinds of digital signals. **No. of inputs** Set the number of digital alarm inputs

**Adjust for each input:**

- Show on overview

- Name

- Delay time for DI alarm (common value for all)

- Alarm text

### **4.1.20 Separate PI functions**

1. Select PI functions

2. Select actual PI-function

3. Define the required names and values attached to the function in case of selecting "1 Input" as input mode

In our example we do not use this function, so the display has been included for your information only.

Define the required names and values attached to the function in case of selecting "2 Inp SuperHeat" as input mode.

##### **3 - General PI Control**

The function can be used for optional regulation

##### **Adjust for each regulation:**

- Show on overview

- Name

- Quick settings Here is a list of suggestions for PI regulations:

- Control mode: Off, Manual or Auto

- Control type: P or PI

- External DI ctrl: Adjusted to "On" if there is an external switch that can start/stop the regulation.

- Input Mode: Choose which input mode should the PI function use: 1 input, 2 Inp Superheat

- Input type select: Choose which signal the regulation shall receive: Temperature, pressure, pressure converted to temperature, voltage signal, Tc, Pc, Ss, Sd etc.

- Input1 Temp. select: Choose which temperature type the first probe shall receive in case of "2 Inp Superheat" as input mode. Choose between: Temperature; Ss-MT suction; Saux#1-3

- Input2 Pres. select: Choose which pressure type the second probe shall receive in case of "2 Inp Superheat" as input mode. Choose between: Pressure; Po-MT; Po-LT; Psuc-MT; Paux#1-3

- Input ref. select: Either fixed or signal for the variable reference: Choose between: : Non, temperature, pressure, pressure converted to temperature, voltage signal, Tc, Pc, Ss, DI etc.

- Setpoint: If fixed reference is chosen

- Input 1: Reading the value of input 1

- Input 2: Reading the value of input 2 (saturation temperature converted from pressure value selected for input 2 in case of "2 Inp Superheat" for input mode)

- Input Mode: reading the selected input mode.

- PI input: input signal to the PI controller.

- Reference: Reading the total reference

- Output type select: Here you select the outlet function (PWM = pulse width modulated (e.g. AKV valve)), Stepper signal for a stepper motor or voltage signal

- Alarm mode: Choose whether an alarm shall be attached to the function. If it is set to "On", alarm texts and alarm limits can be entered

- Advanced ctrl. settings:

- Ref. X1, Y1 and X2,Y2: Points that define and limit the variable reference

- PWM period time: Period during which the signal has been on and off.

- Kp: Amplification factor

- Tn: Integration time

- Filter for reference: Duration for smooth changes to the reference

- Max. error:  Maximum permissible fault signal at which the integrator remains in the regulation

- Min. control output: Lowest permitted output signal

- Max. control output: Maximum permitted output signal

- Start-up time: Time at start-up at which the output signal is force-controlled

- Start-up output: The output signal size at the start-up time.

- Stop output signal. Size of the output signal when regulation is off

### **4.1.21 Configuration of inputs and outputs**

##### 2. Select I/O configuration

##### 3. Configuration of Digital outputs

##### 4. Set up On/off inputs

Press the + button to go to the next page.

|he following displays w<br>efinitions. The displays<br>arlier settings will requi<br>hown earlier.<br>Digital outputs<br>Digital inputs<br>Analogue outputs<br>Analogue inputs|ill depen<br>i   will show<br>re. The t|d on the<br>i     which<br>ables are|earlier<br>i      connec<br>the sa|<br>i      tions the<br>me as|**3 - Outputs**<br>The possible functions are the<br>following:<br>Comp. 1<br>Unloader 1-1<br>Unloader 1-2<br>Unloader 1-3<br>Do for Compressor. 2-8<br>Oil valve comp. 1-2<br>Injection suction line<br>Injection ON<br>Fan 1 / VSD<br>Fan 2 - 8|
|---|---|---|---|---|---|
|**Load**|**Output**|**Module**|**Point**|**Active at**|HP Control|
|Hot gas dump|DO1|1|12|ON|Ejector|
|Circulation pump tw|DO2|1|13|ON|Valve gas cooler V3gc<br>|
|MT Compressor 1 (VLT start)|DO5|1|16|ON|Hot gas Dump<br>H|
|MT Compressor 2|D06|1|17|ON|eat recovery<br>Valve tap water V3tw|
|MT Compressor 3|DO7|1|18|ON|<br>Pump tap water tw|
|IT Compressor (VLT start)|DO8|1|19|ON|Valve heat recov. V3hr<br>|
|LT Compressor 1 (VLT start)|DO1|4|9|ON|Pump heat recov. hr<br>Additional heat|
|LT Compressor 2|DO2|4|10|ON|<br>Alarm|
|Fan motors (VLT start)|DO3|4|11|ON|I'm alive relay|
|3-way valve, tap water, Vtw|DO5|4|13|ON|Thermostat 1 – 10<br>|
|Room fan|DO7|4|15|ON|Pressostat 1 – 5<br>Volt input 1 – 5<br>PI 1 – 3 PWM|

The following displays will depend on the earlier definitions. The displays will show which connections the earlier settings will require. The tables are the same as shown earlier.

- Digital outputs

- Digital inputs

- Analogue outputs

- Analogue inputs

We set up the controller’s digital outputs by keying in which module and point on this module each one of these has been connected to.

|e se up e conroers g<br>module and point on this mo<br>onnected to.<br>We furthermore select for ea<br>ctive when the output is in<br>ttention! Relay outputs mus<br>alves. The controller inverts<br>here will be no voltage at th<br>ompressor is not in operatio<br>efore the compressor is star|a oup<br>dule eac<br>ch outpu<br>pos.**ON**o<br>t not be<br>the funct<br>e by-pas<br>n. Power<br>ted.|s y e<br>h one of t<br>t whether<br>r**OFF**.<br>inverted a<br>ion itself.<br>s valves w<br>is connec|ng n<br>hese ha<br>the loa<br>t unload<br> <br>hen the<br>ted imm|c<br>s been<br>d is to be<br>er<br> <br>ediately|**4 - Digital inputs**<br>The possible functions are the<br>following:<br>Ext. Main switch<br>Ext. compr. stop<br>Ext. power loss<br>Night setback<br>Load shed 1<br>Load shed 2<br>All compressors:<br>Common safety<br>Comp. 1<br>Oil rr ft|
|---|---|---|---|---|---|
|**Function**|**Input**|**Module**|**Point**|**Active at**|pessue saey<br>Over current safety|
|Level switch, CO2 receiver|AI2|2|2|Open|<br>Motor protect. safety|
|Start/stop of heat recovery tw|AI3|2|3|Closed|Disch. temp. safety<br>|
|MT Compressor 1 Gen.  Safety|AI1|3|1|Open|Disch. press. safety<br>General safety|
|MT Compressor 2 Gen.  Safety|AI2|3|2|Open|<br>VSD comp. Fault|
|MT Compressor 3 Gen.  Safety|AI3|3|3|Open|Do for Comp. 2-8<br>|
|IT Compressor Gen.  Safety|AI4|3|4|Open|Fan 1 safety<br>Do for fan 2-8|
|LT Compressor 1 Gen.  Safety|AI5|3|5|Open|<br>VSD cond safety|
|LT Compressor 2 Gen.  Safety|AI6|3|6|Open|<br>Oil receiver low<br>|
|External main switch|AI3|4|3|Closed|Oil receiver high<br>Oil searator low 1-2|
|MT compressors common<br>safety|AI4|4|4|Open|p<br>Oil separator high 1-2<br>AC limit|
|LT compressors common safety|AI6|4|6|Open|<br>Rec. low liquid level|
||||||<br>Rec. high liquid level|
|We set up the controller’s dig<br>hich module and point on t<br>een connected to.|ital input<br>his mod|function<br>ule each o|s by keyi<br>ne of th|ng in<br>ese has|Heat recovery<br>tw enable<br>hr enable<br>|
|We furthermore select for ea<br>e active when the output is<br>pen has been selected here|ch outpu<br>in pos.**C**<br>for all th|t whether<br>**losed**or<br>e safety c|the fun<br>**Open**.<br>ircuits. T|ction is to<br>his means|Flow switch tw<br>Flow switch hr<br>DI 1 Alarm input<br>DI 2-10 ...|
|hat the controller will receiv<br>egister it as a fault if the sign|e signal u<br>al is inter|nder nor<br>rupted.|mal oper|ation and|PI-1 Di ref<br>External DI PI-1|

We furthermore select for each output whether the load is to be active when the output is in pos. **ON** or **OFF** .

Attention! Relay outputs must not be inverted at unloader valves. The controller inverts the function itself. There will be no voltage at the by-pass valves when the compressor is not in operation. Power is connected immediately before the compressor is started.

We set up the controller’s digital input functions by keying in which module and point on this module each one of these has been connected to.

We furthermore select for each output whether the function is to be active when the output is in pos. **Closed** or **Open** . Open has been selected here for all the safety circuits. This means that the controller will receive signal under normal operation and register it as a fault if the signal is interrupted.

5. Configuration of Analogue outputs

##### 6. Configuration of Analogue Input signals

||||||**5 - Analogue outputs**<br>The possible signals are the<br>|
|---|---|---|---|---|---|
|**Function**|**Output**|**Module**|**Point**|**Type**|following:<br>0 – 10 V|
|Speed control, MT compressor|AO1|1|24|0 – 10 V|<br>2 – 10 V<br>|
|Speed control, IT compressor|AO2|1|25|0 – 10 V|0 – 5 V<br>1 – 5 V|
|Speed control, LT compressor|AO1|2|5|0 – 10 V|10 – 0 V<br>|
|Speed control, fan gas cooler|AO2|2|6|0 – 10 V|5 – 0 V<br>|
|Speed control, pump tw|AO3|2|7|0 – 10 V|Stepper output<br>Steer outut 2|
|Signal to by-pass ventil, Vrec|Step 1|3|9|CCMT|pp p<br>Stepper user defined and Valve set-|
|Signal to high pressure valve, Vhp|Step 2|3|10|CCMT|i<br>up: see section "Miscellaneous"|
|3-way valve, gas cooler, V3gc|Step 3|3|11|CTR|**6 - Analogue inputs**|
||||||<br>The possible signals are the<br>following:<br>Temperature sensors:<br>•  Pt1000<br>•  PTC 1000<br>Pressure transmitters:<br>•  AKS 32, -1 – 6 bar<br>•  AKS 32R, -1 – 6 bar<br>•  AKS 32, - 1 – 9 bar<br>•  AKS 32R, -1 – 9 bar<br>•  AKS 32, - 1 – 12 bar<br>•  AKS 32R, -1 – 12 bar<br>•  AKS 32, - 1 – 20 bar|
|**Sensor**|**Input**|**Module**|**Point**|**Type**|•  AKS 32R, -1 – 20 bar|
|Discharge gas temperature  - Sd-MT|AI1|1|1|<br>Pt 1000|•  AKS 32, - 1 – 34 bar<br>|
|Suction gas temperature - Ss-MT|AI2|1|2|Pt 1000|•  AKS 32R, -1 – 34 bar<br>|
|Discharge gas temperature  - Sd-IT|AI3|1|3|Pt 1000|•  AKS 32, - 1 – 50 bar<br>|
|Suction gas temperature - Ss-IT|AI4|1|4|Pt 1000|•  AKS 32R, -1 – 50 bar<br>AKS 2050 1  59 b|
|Thermostat sensor in plant room<br>- Saux1|AI5|1|5|Pt 1000|•   , - –  ar<br>•  AKS 2050, -1 – 99 bar|
|Suction pressure - P0-MT|AI6|1|6|AKS 2050-59|•  AKS 2050, -1 – 159 bar|
|Condenser pressure - Pc-MT|AI7|1|7|AKS 2050-159|•  MBS 8250, -1 – 159 bar|
|Tap water temperature - Stw8|AI8|1|8|Pt 1000|•  User defined (ratiometric 10 – 90%<br>|
|Temp.  gas cooler outlet Sgc|AI9|1|9|Pt 1000|of 5 V supply). Min. and max. value<br>of the sensor range must be set in|
|Gas cooler pressure Pgc|AI10|1|10|AKS 2050-159|<br>relative pressure.|
|Refrigerant receiver, Prec CO2|AI11|1|11|AKS 2050-159|<br>|
|Temp.  by-passed gas Shp|AI1|2|1|Pt 1000|Po suction pres.<br>S ti|
|Outdoor temp, Sc3|AI4|2|4|Pt 1000|s sucon gas<br>Sd disch temp|
|Heat recovery tw2|AI7|3|7|Pt 1000|. .<br>Pc Cond. Pres.|
|<br>Heat recovery tw3|AI8|3|8|Pt 1000|S7 Warm brine|
|<br>Discharge gas temperature - Sd-LT|AI1|4|1|Pt 1000|Sc3 air on<br>E Rf Sil|
|Suction gas temperature - Ss-LT|AI2|4|2|Pt 1000|xt. e. gna<br>• 0 – 5 V,|
|Heat recovery tw4|AI7|4|7|Pt 1000|<br>• 0 – 10 V|
|Suction pressure - P0-LT|AI8|4|8|AKS 2050-59|Oil receiver|

Oil receiver HP control Pgc Prec Sgc Shp Stw2,3,4,8 Shr2,3,4,8 HC 1-5 Heat recovery Saux 1 - 4 Paux 1 - 3 Voltage input 1 - 5 • 0 – 5 V, • 0 – 10 V,

- 1 – 5 V,

• 2 – 10 V PI-in temp PI-ref temp PI- in voltage PI-in pres. PI-ref pres.

### **4.1.22 Set alarm priorities**

2. Select Alarm priorities

##### 3. Set priorities for Suction group

Many functions have an alarm connected. Your choice of functions and settings has connected all the relevant alarms that are current. They will be shown with text in the three pictures.

All alarms that can occur can be set for a given order of priority:

- ”High” is the most important one

- ”Log only” has lowest priority

• ”Disconnected” gives no action The interdependence between setting and action can be seen in the table.

|**Setting**|**Log**|**Alarm**|**relay sele**|**ction**|**Net-**|**AKM-**|
|---|---|---|---|---|---|---|
|||Non|High|Low - High|**work**|**dest.**|
|High|X||X|X|X|1|
|Medium|X|||X|X|2|
|Low|X|||X|X|3|
|Log only|X|||||4|
|Disconnected|||||||

See also alarm text page 131.

##### 4. Set alarm priorities for condenser

In our example we select the settings shown here in the display.

5. Set alarm priorities for thermostat and extra digital signals

In our example we select the settings shown here in the display.

### **4.1.23 Lock configuration**

2. Select Lock/Unlock configuration

3. Lock Configuration

The controller will now make a comparison of selected functions and define inputs and outputs. The result can be seen in the next section where the set-up is controlled.

Press the field **Configuration lock.** Select **Locked** . The set-up of the controller has now been locked. If you subsequently want to make any changes in the controller’s set-up, remember to unlock the configuration first.

### **4.1.24 Check configuration**

This control requires that the set-up is locked. (Only when the set-up is locked, are all settings for in- and outputs activated).

##### 2. Select  I/O configuration

##### 3. Check configuration of Digital Outputs

##### 4. Check configuration of Digital Inputs

**An error has occurred, if you see the following:**

The set-up of the digital outputs appears as it is A **0 – 0** next to a defined function. supposed to according If a setting has reverted to 0-0, you must to the wiring made. control the set-up again. This may be due to the following: • A selection has been made of a combination of module number and point number that does not exist **•** The selected point number on the selected module has been set up for something different The error is corrected by setting up the output correctly. Remember that the set-up must be unlocked before you can change module and point numbers.

The set-up of the digital inputs appears as it is The settings are shown on a **RED** supposed to according background. to the wiring made. If a setting has turned red, you must control the set-up again. This may be due to the following: • The input or the output has been set up; but the set-up has later been changed so that it should no longer be applied. The problem is corrected by setting **module number to 0 and point number to 0.** Remember that the set-up must be unlocked before you can change module and point numbers.

5. Check configuration of Analogue Outputs

6. Check configuration of Analogue Inputs

|The set-up of the analogue outputs appears as it is supposed to<br>according to the wiring made.<br>The set-up of the analogue inputs appears as it is supposed to<br>according to the wiring made.|
|---|

### **4.2 Check of connections**

##### 2. Select I/O status and manual

##### 3. Check Digital Outputs

##### 4. Check Digital Inputs

|Before the control is started, we check that all inputs and<br>outputs have been connected as expected.<br>**This control requires that the set-up is locked.**|
|---|
|By means of the manual control of each output it can be<br>checked whether the output has been correctly connected.|
|**AUTO**<br>The output is controlled by the controller<br>**MAN OFF**<br>The output is forced to pos. OFF<br>**MAN ON**<br>The output is forced to pos ON|
|Cut out the safety circuit for compressor 1.<br>Check that LED DI1 on the extension module (module 2) goes<br>out.|
|Check that the value of the alarm for the safety monitoring of<br>compressor 1 changes to**ON.**<br>The remaining digital inputs are checked in the same way.|
|In "MAN" mode, for some DO (for example "Oil valve separator<br>.." or  "..AKV valves..") it is just possible to set the duration of a<br>single ON pulse with a range between 0 – 30000<sup>1)</sup>ms. After<br>this single ON pulse, the controller will maintain the OFF<br>position for the selected DO, till a new duration setting or till<br>return switch to "Auto" mode.<br>1)negative values are not considered.|

##### 5. Check Analogue outputs

Set Control of output voltage to manual Press in the **Mode** field. Select **MAN** .

Press in the **Value** field Select for example **50%** . Press **OK** .

On the output you can now measure the expected value: In this example 5 volts

6. Put the control of the output voltage back to automatic

##### 7. Check Analogue inputs

Example of the connection between a defined output signal and a manual set value.

|**Definition**||**Setting**||
|---|---|---|---|
||0 %|50 %|100 %|
|**0 - 10 V**|0 V|5 V|10 V|
|**1 - 10 V**|1 V|5.5 V|10 V|
|**0 - 5 V**|0 V|2.5 V|5 V|
|**2 - 5 V**|2 V|3.5 V|5 V|
|**10 - 0 V**|10 V|5 V|0 V|
|**5 - 0 V**|5 V|2,5 V|0 V|

Check that all sensors show sensible values. In our case we have no values. This may be due to the following:

- The sensor has not been connected.

- The sensor is short-circuited.

- The point or module number has not been set up correctly.

- The configuration is not locked.

**AUTO:** The analog input value is managed by the controller. **MAN:** The analog input is forced to a user defined value. Note: when the analog input is in MAN the alarm "Manual override IO" appears on the alarm list. It is recommended to use the MAN mode just during supervised commissioning phases.

The type of "AI voltage" can be set in MAN mode only if the measured voltage value (at the assigned point) is lower than 0.1%.

If the measured value is higher than this value, the controller will automatically switch to AUTO and consider the measured value as a valid input.

### **4.3 Check of settings**

1. Go to the overview

Before the control starts, we check that all the settings are as they should be. The overview display will now show one line for each of the general functions. Behind each icon there is a number of displays with the different settings. All these settings have to be checked.

2. Select suction group

3. Move on through all the individual displays for the suction group

Change displays with the + button. Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

|The last page contains control data.|
|---|

4. Check the individual pages

5. Go back to the overview. Repeat for IT and LT

6. Select condenser group

7. Move on through all the individual displays for the condenser group.

Change displays with the + button. Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

8. Check the individual pages

The last page contains reference settings.

##### 9. Go back to the overview and move on to the rest of the functions

##### 10. General functions

When all the functions in overview display 1 have been reviewed, it is time to look at the "General functions" in overview display 2. Press the + button to access.

The first is the thermostat group

Check the settings.

11. Then the pressure switch group

Check the settings.

12. Proceed with the remaining functions

All the defined general functions are shown in overview display 2. In addition to always being shown in display 2, functions can be selected to be shown in display 1. Individual functions can be selected for display in display 1 via the "Show in overview display" setting.

13. The controller set-up has been completed

### **4.4 Schedule function**

2. Select schedule

Before regulation is started, we will set the schedule function for the night setback of the suction pressure. In other cases where the controller is installed in a network with one system unit, this setting may be made in the system unit which will then transmit a day/night signal to the controller.

3. Set up schedule

Press a day of the week and set the time for the day period. Continue with the other days. A complete weekly sequence is shown in the display.

### **4.5 Installation in network**

1. Set the address (here, for example 3) Turn the right-hand address switch so that the arrow will point at 3.

The arrow of the two other address switches must point at 0.

2. Push the Service Pin Press down the Service Pin and keep it down until the Service Pin LED lights up.

3. Wait for answer from the system unit Depending on the size of the network it may take up to one minute before the controller receives an answer as to whether it has been installed in the network.

   - When it has been installed, the Status LED will start to flash faster than normal (once every half second). It will continue with this for about 10 minutes.

4. Carry out new login via Service Tool

If the Service Tool was connected to the controller while you installed it in the network, you must carry out a new login to the controller via the Service Tool.

The controller has to be remote-monitored via a network. In this network we assign address number 3 to the controller. The same address must not be used by more than one controller in the same network.

##### **Requirement to the system unit**

The system unit must be:

- AK-SM 720.

- AK-SM 800 serie.

If there is no answer from the system unit:

If the Status LED does not start flashing faster than normal, the controller has not been installed in the network. The reason for this may be one of the following:

**The controller has been assigned an address out of range** Address 0 cannot be used.

##### **The selected address is already being used by another controller or unit in the network:**

The address setting must be changed to another (vacant) address.

**The wiring has not been carried out correctly. The termination has not been carried out correctly.** The data communication requirements are described in the document: ”Data communication connections to ADAPKOOL® Refrigeration Controls” RC8AC.

### **4.6 First start of control**

##### **Check alarms**

1. Go to the overview

Press the blue overview button with the compressor and condenser at the bottom left of the display.

2. Go to the Alarm list

Press the blue button with the alarm bell at the bottom of the display.

3. Check active alarms

In our case, we have a series of alarms. We will tidy them up so that we only have those that are relevant.

4. Remove cancelled alarm from the alarm list

Press the red cross to remove cancelled alarms from the alarm list.

5. Check active alarm again

In our case an active alarm remains because the control has stopped. This alarm must be active when control has not started. We are now ready for the start-up of control. Please note that active plant alarms are automatically cancelled when the main switch is in pos. OFF. If active alarms appear when the control is started, the reason for these should be found and remedied.

### **4.6.1 Start the control**

1. Go to Start/Stop display

Press the blue manual control button at the bottom of the display.

2. Start control

Press in the field against **Main switch** . Select **ON** . The controller will now start controlling the compressors and the fans. Note: Control does not start until both the internal and external switches are “ON”. Any external compressor stop breaker must be "ON" for the compressors to start.

### **4.6.2 Manual capacity control**

1.  Go to overview

2. Select suction group

Press the suction group button for the suction group that is to be controlled manually.

3. Set capacity control to manual

4. Set capacity in percentage Press in the blue field **Manual capacity** .

|If you need to manually adjust the capacity of the compressors,<br>you can use the following procedure:|
|---|
|Press the blue field**Control mode.**<br>Select**MAN**.|
|Set the capacity to the required percentage.<br>Press**OK**.|

### **5. Regulating functions**

This section describes how the different functions work.

### **5.1 Suction group**

##### **Controlling sensor**

The capacity distributor can regulate according to the suction pressure P0.

The IT compressors are also regulated according to the suction pressure, but the signal is received from the receiver - Prec. See page 118 for IT description

An error in the controlling sensor will mean that regulation continues with fx. 50% cut-in in daily operation and e.g. 25% cut-in at night, but for a minimum of one step.

The reference for the regulation can be defined in 2 ways: Either P0Ref = P0 setting + P0 optimization + night displacement

or P0Ref = P0 setting + Ext. Ref + night displacement

##### **P0 setting**

A basic value for the suction pressure is set.

##### **P0 optimization**

This function displaces the reference so that regulation will not take place with a lower suction pressure than required. The function cooperates with controllers on the individual refrigeration appliances and a system manager. The system manager obtains data from the individual regulations and adapts the suction pressure to the optimum energy level. The function is described in the manual for the system manager. With this function you can read which appliance is most heavily loaded at the moment as well as the displacement allowed for the suction pressure reference.

##### **Night displacement**

The function is used to change the suction pressure reference for night time operation as an energy saving function. With this function the reference can be displaced by up to 25 K in positive or negative direction. (When you displace to a higher suction pressure, a positive value is set). Displacement can be activated in three ways:

- Signal on an input

- From a system unit override function

- Internal time schedule

If a short change in the suction pressure is needed (for example, up to 15 minutes in connection with defrosting), the functions can be applied. Here the PO-optimisation will not have time to compensate for the change.

##### **Override with a 0 - 10 V signal**

When a voltage signal is connected to the controller, the reference can be displaced. In the set-up it is defined how big a displacement is to take place at max. signal (10 V) and at min. signal.

##### **Limitation of reference**

To safeguard yourself against a too high or too low regulation reference, a limitation of the reference must be set.

*[Figurtekst: P0 ref · Max. · Min.]*

##### **Forced operation of the compressor capacity in the suction**

##### **group**

A forced operation of the capacity can be carried out which disregards the normal regulation. Depending on the selected form of forced operation, the safety functions will be cancelled.

##### **Forced operation via overload of requested capacity**

The control is set to manual and the desired capacity is set in % of the possible compressor capacity.

##### **Forced operation via overload of digital outlets**

The individual outputs can be set to MAN ON or MAN OFF in the software. The control function disregards this, but an alarm is sent out that the outlet is being overridden.

##### **Forced operation via change-over switches**

If the forced operation is done with the switch-over on the front of an expansion model, this is not registered by the control function and no alarm is sounded. The controller continues to run and couples with the other relays.

##### **Coordination between the LT and MT compressors**

The LT (low pressure) compressors are only permitted to start when MT (medium pressure) is ready, but has not necessarily started the compressors.

LT will then start when required.

When this happens, MT will register the pressure increase and immediately start the MT compressors in line with the desired pressure.

The “night displacement” function should not be used when regulation with the override function “P0-optimisation” is performed. (Here the override function itself will adapt the suction pressure to the max. permissible).

### **5.2 Capacity control of compressors**

##### **Capacity control**

AK-PC 782A can control 3 compressor groups - MT, IT and LT. Each compressor can have up to 3 unloaders. One or two of the compressors can be equipped with speed regulation.

The cut-in capacity is controlled by signals from the connected pressure transmitter and the set reference. Set a neutral zone around the reference .

In the neutral zone, the regulating compressor controls the capacity so that pressure can be maintained. When it can no longer maintain the pressure within the neutral zone, the controller will cut out or cut in the next compressor in the sequence.

When further capacity is either cut out or cut in, the capacity from the regulating compressor will be modified accordingly to maintain the pressure within the neutral zone (only where the compressor has variable capacity).

- When the pressure is higher than the “reference + a half neutral zone”, cut-in of the next compressor (arrow up) is permitted.

- When the pressure is lower than the “reference - a half neutral zone”, cut-out of a compressor (arrow down) is permitted.

- When the pressure is within the neutral zone, the process will continue with the currently activated compressors. Unload valves (if present) will activate, depending on whether suction pressure is above or below the reference value.

4 compressors of equal size  - The capacity curve will look like this

*[Figurtekst: Requested · capacity % · C4 · C3 C3 C3 · C2 C2 C2 C2 C2 · C1 C1 C1 C1 C1 C1 C1 · Time]*

Cut-out of the last compressor stage: Normally, the last compressor step will only be cut out when the required capacity is 0% and the suction pressure is below the neutral zone.

##### **Operation time first step**

At start-up the refrigeration system must have time to be stable before the PI controller takes over the control.  For this purpose, at start-up of a plant, a limitation is made of the capacity so that only the first capacity step will cut in after a set period (to be set via "runtime first step").

##### **Pump down function:**

*[Figurtekst: Suction pressure P0]*

##### **Change capacity**

The controller will cut in or cut out capacity based on these basic rules:

To avoid too many compressor starts/stops with low load, it is possible to define a pump down function for the last compressor.

If the pump down function is used, the compressors will be cut out when the actual suction pressure is down to the configured pump down limit.

When the pump down limit is approaching the neutral zone, it will be limited to NZ minus 1 K. This can occur if receiver pressure has been optimized.

Note that the configured pump down limit should be set higher than the configured safety limit for low suction pressure "Min Po".

For the IT compressor, pump down will be controlled by the receiver and MT temperature.

##### **Increase capacity:**

The capacity distributor will start extra compressor capacity as soon as the requested capacity has increased to a value which allows the next compressor step to start. Referring to below example - a compressor step is added as soon as there is “Room” for this compressor step below the requested capacity curve.

##### **Decrease capacity:**

The capacity distributor will stop compressor capacity as soon as the requested capacity has decreased to a value which allows the next compressor to stop. Referring to below example - a compressor step is stopped as soon as there is no more “Room” for this compressor step above the requested capacity curve.

##### **Variable integration time**

There are two parameters to make Tn variable. This allows control to be more rapid the further pressure deviates from the reference. The A+ setting will lower Tn when the pressure is above the reference, and the A- setting will lower Tn when the pressure is below the reference.

Tn has been set to 120 s in the graph below, and falls to 60 s if the pressure is above the reference and to 40 s if the pressure is below the reference.

Above the reference: Set Tn divided by the A+ value. Below the reference: Set Tn divided by the A- value. The controller calculates the curve in such a manner that regulation is smooth.

##### **Regulation  parameters**

To make it easier to start up the system, we have grouped regulation parameters into sets of commonly used values, called "Easy-settings". Use these to choose between sets of settings appropriate for a system which responds slowly or quickly. The factory setting is 5.

If you need to fine-tune the control, select the "User defined" setting. All parameters can then be freely adjusted.

|**Easy-**||**Regulation**|**parameters**||
|---|---|---|---|---|
|**Settings**|**Kp**|**Tn**|**A+**|**A-**|
|1 = Slowest|1.0|200|3.5|5.0|
|2|1.3|185|3.5|4.8|
|3 = Slower|1.7|170|3.5|4.7|
|4|2.1|155|3.5|4.6|
|5 = Default|2.8|140|3.5|4.4|
|6|3.6|125|3.5|4.2|
|7 = Faster|4.6|110|3.5|4.1|
|8|5.9|95|3.5|4.0|
|9|7.7|80|3.5|3.8|
|10= Fastest|9.9|65|3.5|3.5|
|User defined|1.0  - 10.0|10 - 900|1.0 - 10.0|1.0-10.0|

### **5.2.1 Capacity distribution methods**

The capacity distributor can work based on 2 distribution principles.

##### **Coupling pattern – Cyclical operation:**

This principle is used if all compressors are of the same type and size.

The compressor cuts in and cuts out in accordance with the "First In First Out" principle (FIFO) to equalise operating hours between the compressors.

Speed-regulated compressors will always be cut in first, and the variable capacity is used to fill capacity gaps between the subsequent steps.

##### Timer restrictions and safety cut outs

If a compressor is prevented from starting because it is “hanging” on the restart timer or is safety cut out, this step is replaced by another compressor.

##### **Coupling pattern – Best fit operation**

This principle is used if the compressors are of different sizes. The capacity distributor will cut-in or cut-out the compressor capacity in order to ensure the least possible capacity jump. Speed-regulated compressors will always be cut in first, and the variable capacity will be used to fill capacity gaps between the subsequent steps.

##### Timer restrictions and safety cut outs

If a compressor is prevented from starting because it is “hanging” on the restart timer or is safety-cut out, this step is replaced by another compressor or another combination.

If a compressor with unloaders is not allowed to start due to a timer striction, no single step compressor is allowed to start. When the timer restriction has expired the compressor with unloaders will start.

If a compressor with unloaders is not allowed to start due to a timer striction, no single step compressor is allowed to start. When the timer restriction has expired the compressor with unloaders will start.

##### **Operating time equalisation**

The operating hour equalizing is carried out between compressors of the same type with the same total capacity.

- At the different start-ups, the compressor with the lowest number of operating hours will be started first.

- At the different stops, the compressor with the highest number of operating hours will be stopped first.

- For compressors with several steps, the operating time equalizing is carried out between the compressors’ main steps.

- The left column shows the operating hours, according to which the controller equalises.

- The middle column shows (as a percentage) to what extent the individual compressor has been activated within the last 24 hours.

- The right column shows the compressor's current operating time. The value should be reset when the compressor is replaced.

### **5.2.2 Power pack types – compressor combinations**

The controller is able to control power packs with compressors of various types:

- One or two speed controlled compressors

- Capacity controlled piston compressors with up to 3 unloader valves

- Single step compressors – piston

The chart below shows the compressor combination which the controller is capable of controlling. The chart also shows which coupling pattern can be set for the individual compressor combinations.

|Combination|Description|Cou<br>patt|pling<br>ern|
|---|---|---|---|
|||Cyclical|Best fit|
||One-step compressors. *1|x|x|
||A compressor with an unload<br>valve, combined with one-step<br>compressors. *2|x||
||Two compressors with unload<br>valves, combined with one-step<br>compressors. *2|x||
||All compressors with unload<br>valves. *2|x||
||A speed-regulated compressor<br>combined with one-step<br>compressors. *1 and *3|x|x|
||A speed-regulated compressor<br>combined with a  compressor<br>with unload valve(s) and one-step<br>compressors. *1 and *3|x||
||A speed-regulated compressor<br>combined with several<br>compressors with unload valves.<br>*2 and *3|x||
||Two speed-regulated<br>compressors combined with one-<br>step compressors *4|x|x|

- *1) For a cyclical coupling pattern, the one-step compressors must be the same size

- *2) For compressors with unload valves, it is generally true that they must have the same size, the same number of unload valves (max 3) and the same sized main steps. If compressors with unload valves are combined with one-step compressors, all compressors should be the same size

- *3) Speed-regulated compressors can have different sizes in relation to subsequent compressors

- *4) When two speed-regulated compressors are used, they must have the same frequency range. For cyclical coupling patterns, the two speed-regulated compressors should be the same size and the subsequent one-step compressors should also be the same size.

In appendix A there is a more detailed description of the coupling patterns for the individual compressor applications with associated examples.

The following is a description of some general rules for handling capacity-regulated compressors, speed-regulated compressors and also for two speed-regulated compressors.

##### **Capacity-regulated compressors with unload valves**

"Unloader control mode" determines how the capacity distributor should handle these compressors.

##### Unloader control mode = 1

Here the capacity distributor allows only one of the compressors to be unloaded at a time. The advantage of this setting is that it avoids operating with several compressors unloaded, which is not energy efficient.

Two capacity-regulated compressors of 20 kW, each with 2 unload valves, cyclical coupling pattern.

*[Figurtekst: Pc Sd Cap.% C2.2 · Ss Po · C2.1 C2.1 C2.2 · C2 C2 C2 C2.1 C2.2 · C1.2 C1.2 C1.2 C1.2 C2 C2.1 C2.2 · C1.1 C1.1 C1.1 C1.1 C1.1 C1.1 C2 C2.1 C2.1 · 20 kW 20 kW C1 C1 C1 C1 C1 C1 C1 C1 C2 C2 C2 t]*

- For decreasing capacity, the compressor with the most operating hours is unloaded (C1).

- When C1 is completely unloaded, it is cut out before compressor C2 is unloaded.

##### Unloader control mode = 2

Here the capacity distributor allows two compressors to be unloaded while capacity is decreasing. The advantage of this setting is that it reduces the number of compressor start/stops.

Two capacity-regulated compressors of 20 kW, each with 2 unload valves, cyclical coupling pattern.

*[Figurtekst: Pc Sd Cap.% C2.2 · Ss Po · C2.1 C2.1 C2.2 · C2 C2 C2 C2.1 C2.2 · C1.2 C1.2 C1.2 C1.2 C2 C2.1 C2.1 · C1.1 C1.1 C1.1 C1.1 C1.1 C1.1 C2 C2 C2.1 · 20 kW 20 kW C1 C1 C1 C1 C1 C1 C1 C1 C1 C2 C2 t]*

- For decreasing capacity, the compressor with the most operating hours is unloaded (C1).

- When C1 is completely unloaded, compressor C2 with one-step is unloaded before C1 is cut out.

##### Attention!

Relay outputs must not be inverted at unloader valves. The controller inverts the function itself. There will be no voltage at the by-pass valves when the compressor is not in operation. Power is connected immediately before the compressor is started.

##### **Speed control compressors:**

The controller is able to use speed control on the leading compressor in different compressor combinations. The variable part of the speed controlled compressor is used to fill in capacity gaps of the following compressor steps.

##### General regarding handling:

One or two of the defined capacity steps for the compressor regulation may be connected to a speed control unit that may be a frequency converter type VLT, for example.

An output is connected to the frequency converter’s ON/OFF input and at the same time an analogue output ”AO” is connected to the frequency converter’s analogue input.

The ON/OFF signal will start and stop the frequency converter and the analogue signal will indicate the speed. It is only the compressor defined as compressor 1 (1+2) that can be speed controlled.

When the step is in operation, it will consist of a fixed capacity and a variable capacity. The fixed capacity will be the one that corresponds to the mentioned min. speed and the variable one will lie between the min. and max. speed. To obtain the best regulation, the variable capacity must be bigger than the subsequent capacity steps that it has to cover during the regulation. If there are major short-term variations in the plant’s capacity requirement it will increase the demand for variable capacity.

##### This is how you cut the step in and out:

*[Figurtekst: Max. · Start · Min. · 0 t · ON · OFF]*

##### Controlling – increasing capacity

If the need for capacity becomes larger than “Max. Speed”, then the subsequent compressor step will be cut in. At the same time, the speed on the capacity step will be reduced so the capacity is reduced with a size that corresponds to exactly the cut-in compressor step. Thereby a completely "frictionless" transition is achieved without capacity holes (refer also to sketch).

*[Figurtekst: V · Max . · V Max . · Star t 2 Star t · Mi n. V Min . V · 1 1]*

##### Controlling – decreasing capacity

If the capacity requirement becomes less than “Min. speed” then the subsequent compressor step will be cut out. At the same time, the speed on the capacity step is increased so the capacity is increased with a size that corresponds to exactly the cut-out compressor step.

##### Cut-out

The capacity step will be cut out when the compressor has reached “Min. Speed” and the requested capacity has dropped to 1%.

##### Timer restriction on speed controlled compressor

If a speed controlled compressor is not allowed to start due to a timer restriction, no other compressor is allowed to start. When the timer restriction has expired the speed controlled compressor will start.

##### Safety cut-out on speed controlled compressor

If the speed controlled compressor is cut out on safety, other compressors are allowed to start. As soon as the speed controlled compressor is ready to start it will be the first compressor to start.

As mentioned before the variable part of the speed capacity should be bigger than the capacity of the following compressor steps in order to achieve a capacity curve without “holes”. In order to illustrate how the speed control will react at different pack combinations a couple of examples will be given here:

##### Cut-in

The speed-controlled compressor will always be the first to start and the last to stop. The frequency converter will be started when a capacity requirement corresponding to the mentioned ”Start speed” arises (the relay output changes to ON and the analogue output is supplied with a voltage corresponding to this speed). It is now up to the frequency converter to bring the speed up to ”Start speed”.

The capacity step will now be cut in and the required capacity determined by the controller. The start speed always ought to be set so high that a fast lubrication of the compressor  is obtained during the start.

##### **a) Variable capacity bigger than following compressor steps:**

##### **b) Variable part smaller than following compressor steps:**

When the variable part of the speed controlled compressor is bigger than the following compressors, there will be no “holes” in the capacity curve. Example:

If the variable part of the speed controlled compressor is smaller than the following compressors there will be “holes” in the capacity curve.

1 speed controlled compressor with a nominal capacity at 50Hz of 10kw - Variable speed range 30 – 90Hz 2 one step compressors of 10 kW

1 speed controlled compressor with a nominal capacity at 50Hz of 20kw - Variable speed range 25 – 50Hz 2 one step compressors of 20 kW Fixed capacity =  25 HZ / 50 HZ x 20 kW =  10 kW Variable capacity = 25 HZ / 50Hz x 20 kW = 10 kW

Fixed capacity =  30 HZ / 50 HZ x 10 kW =  6 kW Variable capacity = 60 HZ / 50Hz x 10 kW = 12 kW

The capacity curve will look like this:

The capacity curve will look like this:

*[Figurtekst: Requested · 60 kW capacity % · Pc Sd · Ss Po 50 Hz C1 50 Hz · 40 k W · 25 Hz 25 Hz · C1 C3 C3 C1 · 20 k W · Start spee d · 20 kW 20 kW 20 kW Min. spee d · 25 – 50 Hz C1 C2 C2 C2 C2 C1 · Time · Danfoss 80Z8160.10]*

*[Figurtekst: Requested · Pc Sd 40 kW capacity % · Ss Po · 90 Hz C1 C1 80 Hz · 20 kW · 40 Hz · 30 Hz · C1 C3 C3 C1 · Start spee d · 10 kW 10 kW 10 kW Min. speed · 30 – 90 Hz C1 C2 C2 C2 C2 C1 · Time]*

As the variable part of the speed controlled compressor is smaller than the following compressor steps, the capacity curve will have some holes that cannot be filled out by the variable capacity.

As the variable part of the speed controlled compressor is bigger than the following compressor steps, the capacity curve will be without holes.

- 1 The speed controlled compressor will be cut in when the requested capacity has reached the start speed capacity

   - 1) The speed controlled compressor will be cut in when the requested capacity has reached the start speed capacity

- 2) The speed controlled compressor will increase speed until it reaches max speed at a capacity of 18 kW

   - 2) The speed controlled compressor will increase speed until it reaches max. speed at a capacity of 20 kW

- 3) The one-step compressor C2 of 10 kW is cut in and the speed on C1 is reduced too so that it corresponds to 8kW (40Hz)

   - 3) The speed controlled compressor will stay at max. speed until the requested capacity has increased to 30 kW

- 4) The speed controlled compressor will increase speed until the total capacity reaches 28 kw at max. speed

   - 4) The one-step compressor C2 of 20 kW is cut in and the speed on C1 is reduced to min. so that it corresponds to 10kW (25Hz). Total capacity = 30 kW.

- 5) The one-step compressor C3 of 10 kW is cut in and the speed on C1 is reduced too so that it corresponds to 8kW (40Hz)

   - 5) The speed controlled compressor will increase speed until the total capacity reaches 40 kW at max. speed

- 6) The speed controlled compressor will increase speed until the total capacity reaches 38 kW at max. speed

   - 6) The speed controlled compressor will stay at max. speed until the requested capacity has increased to 50 kW

- 7) When reducing capacity, the one-step compressors will be cut out when the speed on C1 is at minimum

- 7) The one-step compressor C3 of 20kW is cut in and the speed on C1 is reduced to min. so that it corresponds to 10kW (25Hz). Total capacity = 50 kW

- 8) The speed controlled compressor will increase speed until the total capacity reaches 60 kw at max speed

- 9) When reducing capacity, the one step compressors will be cut out when the speed on C1 is at minimum speed.

*[Figurtekst: Analogue output · Max. speed · Start speed · Min. speed · Time · Comp. 1 · Comp. 2 · Comp. 3]*

##### **Two speed-regulated compressors**

The controller is capable of regulating the speed of two compressors of the same or different sizes. The compressors can be combined with one-step compressors of the same or different sizes, depending on the choice of coupling pattern.

##### General regarding handling:

Generally, the two speed-regulated compressors are managed according to the same principle as for one speed-regulated compressor. The advantage of using two speed-regulated compressors is that it allows for a very low capacity, which is an advantage for low loads. At the same time, it produces a very large, variable regulating area.

Compressor 1 and 2 both have their own relay outlets to start/stop separate frequency converters, for example of type VLT. Both frequency converters use the same analogue output signal AO which is connected to the frequency converters’ analogue signal input (they can, however, be configured to run individual signals). The relay outputs will start and stop the frequency converter and the analogue signal will indicate the speed.

##### Controlling – decreasing capacity

The speed-regulated compressors will always be the last compressors running.

When the capacity requirement during cyclical operations becomes less than "Min. speed" for both compressors, the speedregulated compressor with the most operating hours will be cut-out. At the same time, the speed of the last speed-regulated compressor increases so that the capacity is increased to the level that matches the cut-out compressor’s step.

The precondition for using this regulating method is that both compressors have the same frequency range.

The speed-regulated compressors will always be the first to start and the last to stop.

##### Cut-out

The last speed-regulated compressor will be cut-out when the compressor has reached ”Min. speed” and the capacity requirement (desired capacity) has decreased to under 1% (see however the section on the pump down function).

*[Figurtekst: Pc Sd · Ss Po · 20 kW 20 kW 40 kW · 30 – 60 Hz]*

##### Timer restriction and safety cut-outs

Timer limits and safety cut-outs on speed-regulated compressors should be managed in accordance with the general rules for individual coupling patterns.

Short descriptions and examples are given below of the handling of two speed-regulated compressors for the individual coupling patterns. For a more detailed description, refer to the appendix at the end of the chapter.

##### Cut-in

The first speed-regulated compressor will be started when there is a capacity requirement which matches the setting. The "Start speed" (relay outlet changes to on and the analogue outlet is supplied with a voltage that matches this speed). It is now up to the frequency converter to bring the speed up to the "Start speed". The capacity step will now be cut in and the desired capacity determined by the controller.

##### Cyclical operation

For cyclical operations, both speed-regulated compressors will have the same size and operating hours will be equalized between the compressors in accordance with the First-in-First-Out Principle (FIFO). The compressor with the least operating hours will be the first to start. The following speed-regulated compressor will be cut in when the first compressor runs at max.  speed and the desired capacity has reached a value that allows the cut-in of the next speed-regulated compressor at start speed. Afterwards, both compressors will be cut in together and they will run in parallel. The following one-step compressors will be cut in and out in accordance with First-In-First-Out principle in order to equalise operating hours.

The start speed should always be set so high that a good lubrication of the compressor is quickly reached during start-up. For a cyclical coupling pattern, the subsequent speed-regulated compressor will be cut in when the first compressor runs at max. speed and the desired capacity has reached a value that allows the cut-in of the next speed-regulated compressor at start speed. Afterwards, both compressors will be cut in together and will run in parallel. The following one-step compressors will be cut in and out in accordance with the selected coupling pattern.

### **5.2.3 Compressor timers**

- Two speed-regulated compressors with a nominal capacity of 20 kW and frequency range 25 – 60 Hz

##### **Time delays for cut-ins and cut-outs**

To protect the compressor against frequent restarts, three time delays can be put in:

- Two one-step compressors, each of 20 kW

*[Figurtekst: Ss Po Pc Sd Cap. % · 60 Hz · C2 C2 50 Hz · 20 kW 20 kW 20 kW 20 kW 35 Hz C2 C1 C1 C2 25 Hz · C 2 C1 C4 C4 C1 · 25 – 60 Hz Start spee d C2 · Min. speed C1C1 C3 C3 C3 C4 C1 t]*

- A minimum time to run from a compressor’s start-up and until it may be restarted

- A minimum time (ON-time) for the compressor to operate before it may be stopped again

- A minimum OFF time to run from a compressor stops and until it may be restarted

When unloaders are cut in and out, the time delays will not be used.

##### Best fit

##### **Timer**

During best-fit operations, the speed-regulated compressors can have different sizes and they will be handled in such a way that the best possible capacity adjustment is achieved. The smallest compressor will be started first, then the first will be cut out and the second compressor will cut in. Finally, both compressors will be cut in together and will run in parallel.

The operating time of a compressor motor is registered continuously. You can read out:

- operating time for the previous 24-hour period

- total operating time since the timer was last set to zero-set

##### **Equalizing operating hours**

The following one-step compressors will, in every case, be handled in accordance with the best-fit coupling pattern.

Operating hours are also summed in the "Equalization time" field. During cyclical operation, this field is used for equalizing operating hours.

- Two speed-regulated compressors with a nominal capacity of 10 kW and 20 kW respectively

##### Coupling counter

The number of relay cut-ins and cut-outs is registered continuously. The number of starts can be read out here:

- Frequency range of 25-60 Hz

- Two one-step compressors of 20 and 40 kW respectively

- Number during the previous 24-hour period

- Total number since the counter was last set to zero-set

*[Figurtekst: Ss Po Pc Sd Cap. % · 90 Hz · C2 C2 63.3 Hz · 10 kW 20 kW 20 kW 40 kW 56.7 Hz C2 C1 C1 C 2 30 Hz · 30 – 90 Hz 30 – 90 Hz 45 Hz90 HzC2 CC1 2 C1 C3 C3 C1 CC1 2 · Start speeMin. speed d C2C1C3C4 C4 C4 C4 C3 C C12 t]*

### **5.2.4 Compressor with variable capacity**

##### **Digital scroll compressor**

The capacity is divided into period times as "PWM per". 100% capacity is delivered when cooling takes place for the whole period.

An off time is required by the by-pass valve within the period and an on time is also permitted. There is "no cooling" when the valve is on.

##### **Two independent speed-regulated compressors**

If the two speed-regulated compressors need to be controlled asynchronously, they must each have their own analogue voltage signal.

The controller itself calculates the capacity needed and will then vary it according to the cut-in time of the by-pass valve. A limit is introduced if low capacity is needed so that the cooling does not go below 10%. This is because the compressor can cool itself. This value can be increased if necessary.

The controller first starts one of the speed-regulated compressors. If more capacity is required, the other speed-regulated compressor is started, and then the single compressors.

*[Figurtekst: Refrigeration · No refrigeration · Period time · Min. capacity]*

*[Figurtekst: Analogue outputs · Max. spee d · Nomina l · Start spee d · Min. spee d]*

The first is run up to maximum speed. Number two is then activated and run up to nominal speed – and kept there. The speed of number one is reduced at the same time, so the capacity is balanced. All variations are now handled by number one.  If number one reaches maximum speed, number two will also be raised.

If number one reaches minimum speed, it will be kept there while number two takes over the variation below its nominal speed. When engaging and disengaging, the total hours of operation for the compressors is compared, so they are run an equal number of hours.

##### **BOCK flexxCO2CONTROL**

##### flexxCO2NTROL 4:

The pulse signal can also be used to control one CRII with two unloaders (4-cylinder version).

The compressor capacity can be controlled from 10% to 100%, depending on the pulsation of the unloaders. The compressor start signal is connected to a relay output, and the unloaders are connected to solid state output e.g. DO1 and DO2.

*[Figurtekst: Unloader 1 · Unloader 2]*

##### flexxCO2NTROL 6:

The pulse signal can also be used to control one CRII with three unloaders (6-cylinder version).

The compressor signal is connected to one relay output. The two unloaders are connected to solid state output fx DO1 and DO2. The third is connected to a relay output. The compressor capacity can be controlled from 10 – 67%, depending on the pulse of the unloaders. The relay is then connected to the third unloader. When this relay is off, the capacity will be controlled between 33% and 100%.

##### **Individual Sd monitoring**

When regulating with Sd monitoring, variable capacity compressor types will increase capacity if the temperature nears the Sd limit. This will result in better cooling of the unloaded compressor.

*[Figurtekst: Unloader 2 follows unloader 1, · but it remains displaced by a · half period.]*

##### **Bitzer CRII**

Followed the same principle (for Bitzer Ecoline CRII 4 and CRII 6) as described above, for BOCK .

##### **Copeland Stream compressor**

The PWM signal can also be used to control one stream compressor with one unloader valve (Stream 4) or one with two unloaders (Stream 6).

- Stream 4: The compressor capacity is distributed by up to 50% for

   - one relay and the remaining 50-100% for the unloader.

- Stream 6: The compressor capacity is distributed by up to 33%  for one relay and the remaining 33-100% for the unloader.

### **5.2.5 Load shedding**

On some installations there is the desire to limit the cut-in compressor capacity so that one can limit the total electrical load in the store for periods. (The IT circuit is not directly affected)

This limitation can be activated in the following way:

- Via signal from the network

- Via signal on one DI input + signal via the network

### **5.2.6 Injection ON**

The electronic expansion valves in the refrigeration appliances must be closed when all the compressors are prevented from starting. In this way the evaporators will not be filled with liquid which is subsequently passed on to a compressor when regulation is restarted.

One of the compressor control relays may be used for this function, or the function can be obtained via data communication.

- Via signal on two DI inputs + signal via the network

The signal via the network will result in the same function as if the signal was received on DI 1.

For each digital inlet a limit value is attached for the maximum allowable cut-in compressor capacity so that one can carry out the capacity limitation in 2 steps.

When a digital inlet is activated, the maximum allowable compressor capacity is limited to the set limit. This means that if the actual compressor capacity upon activation of the digital inlet is higher than this limit, then so much compressor capacity is cut out that it will then be on or under the set maximum limit value for this digital inlet.

The threshold value may not be set lower than the compressor's lowest capacity step/"Start speed".

*[Figurtekst: Comp. cap. % · 100% · 80% · 60% Load limit 1 · 40% Load limit 2 · 20% · Load shed DI 1 · Load shed DI 2]*

When both load-shedding signals are active, the lowest limit value for the capacity will be the one that is applicable.

##### **Max. time**

A max. period with low compressor capacity can be set. When the period expires, the system switches to normal regulation until the suction pressure is once again in place. Load shedding will then be permitted.

##### **Overriding of load shedding:**

To avoid load shedding leading to temperature problems for the chilled products, an overriding function is fitted.

A overriding limit is set for the suction pressure as well as a delay time for each digital inlet.

If the suction pressure during load shedding exceeds the set P0 overriding limit and the attached delay times for the two digital inlets expire, then load shedding overrides the signals so that the compressor capacity can be increased until the suction pressure is again under the normal reference value. The load shedding can then be activated again.

##### **Alarm:**

When a load shedding digital inlet is activated, an alarm will be activated to inform that the normal control has been bypassed. This alarm can however be suppressed if so desired.

*[Figurtekst: with data communication]*

The function is described based on the sequence of events below: T1) The last compressor is cut out

- T2) The suction pressure has increased to a value corresponding to Po Ref + ½ NZ + 2 K” but no compressor can start due to restart timers or safety cut-out

- T3) The time delay “Injection OFF delay” elapses and the injection valves are forced to close via relay signal or via network signal

- T4) The first compressor is now ready to start. The forced closure signal via the network is now cancelled.

- T5) The time delay “Comp. Start delay” expires and the forced closure signal via the relay switch is cancelled simultaneously with the first compressor being allowed to start

The reason why the forced closure signal via the network is cancelled before the first compressor starts, is that it will take some time to distribute the signal to all appliance controllers via the network.

### **5.2.7 MT/LT coordination**

In a booster configuration or when Ext.Coordination MT/LT is enabled, coordination between the MT and the LT packs ensures that the LT cannot run unless the MT is able to handle the load. The LT sends a request to the MT indicating that it needs to start but delays start until the MT sends a release.

immediately (alarms, timers) and the Po MT is in neutral or minus zone.

3. The MT will start a compressor when the Po MT is above the limit selected by the MT/LT Coord. threshold:

   - Neutral zone: In or above the neutral zone.

   - Reference: Above the Po MT reference.

In booster configuration, the coordination is handled internally. When the Ext.Coordination is used, a digital input is used for the request signal, a digital output for the release signal.

Upon receiving a request, the MT will:

1. Send the release immediately when it is already running.

2. When not already running, the MT will release when it can start

- Plus zone: In the plus zone.

The release will be cancelled when there is no request or when the MT stops and cannot be restarted immediately (alarms, timers). When LT coord. stop is set to MT Po, the release will not be cancelled until the Po MT enters the plus zone.

### **5.2.8 Liquid injection in common suction line**

The discharge pressure gas temperature can be kept down by means of liquid injection into the suction line (not IT circuit). With a thermostatic expansion valve in series with a solenoid valve.  The solenoid valve is connected to the controller.

*[Figurtekst: Ss Po Sd · NC · Inject diff. Sd · Inject start Sd · Sd · Ss · Inject diff. SH · Inject start SH]*

Control can be carried out in two ways:

1. The liquid injection is exclusively controlled on the basis of the superheat in the suction line. Two values are set – a starting value and a differential where the injection is stopped again.

2. The liquid injection is both controlled by the superheat (as described above) and by discharge temperature Sd. Four values are set – two as mentioned above and two for the Sd function, a starting value and a differential. The liquid injection is started when both starting values have been passed, and is stopped again when just one of the two functions cuts out.

Direct using an electrically operated expansion valve of the type AKV

*[Figurtekst: Calculation of OD% for the injection into the suction line · AKV OD% as function of SH AKV OD% as function of Sd]*

Four values are adjusted - a start value for the Sd temperature, min. and max. values for overheating and a period time for the AKV valve.

Actual used OD for the liquid injection is the highest of the two above (see above fig.)

The width of the P-Band for the Sd control is hardcoded to be 20K and cannot be changed.

The valve will be closed too, when all compressors are stopped.

##### **As a safety function the AKV valve will be closed anyway, as soon as the SH gets below 8K, to protect the compressors from getting liquid into the suction port.**

The pulse width modulating signal for the AKV valve shall be taken from one of the controller's four solid state outputs.

##### Time delay

A time delay can be set which ensures that the injection is delayed with the set value after start-up of the first compressor.

### **5.2.9 Safety functions**

##### **Signal from the compressor’s safety controls**

The controller can monitor the status of each compressor’s safety circuit. The signal is taken directly from the safety circuit and connected to an input.

(The safety circuit must stop the compressor without involving the controller).

If the safety circuit is cut out, the controller will cut out all output relays for the compressor in question and give an alarm. Regulation will continue with the other compressors.

##### **Time delays with safety cut-out:**

In connection with safety monitoring of a compressor it is possible to define two delay times:

Cut-out delay time: Delay time from signal from the safety circuit until the compressor relays cut out and alarm is given (note that the delay time is common to all security inlets for the compressor concerned)

Safety re-start time: The minimum time a compressor must be OK after a safety cut-out until it may start again.

##### **Monitoring of superheat**

###### General safety circuit

If a low-pressure switch is placed in the safety circuit it must be placed at the end of the circuit. It must not cut out the DI signals. (There is a risk that the regulation will become locked and that it will not start again). This also applies to the example below.

If an alarm is needed which also monitors the low-pressure thermostat, a “general alarm” can be defined (an alarm that does not affect the control). See the following section “General monitoring functions”.

Extended safety circuit

Instead of a general monitoring of the safety circuit this monitoring function can be extended. In this way, a detailed alarm message is issued which tells you which part of the safety circuit has dropped out. The sequence of the safety circuit must be established as shown, but not all of them need necessarily be used.

This function is an alarm function which continuously receives measured data from suction pressure P0 and suction gas Ss. If superheat is registered which is lower or higher than the set limit values, an alarm will be given when the time delay has passed.

##### **Monitoring of max. discharge gas temperature (Sd)**

##### Common Sd monitoring

The function gradually cuts out compressor steps if the discharge temperature becomes higher than permitted. The cut-out limit can be defined in the range from 0 to +195°C.

The function is started at a value that is 10 K below the set value. At this point the entire condenser capacity is cut in at the same time as 25% of the compressor capacity is cut out (but minimum one step). This is repeated every 30 seconds. The alarm function is activated.

If the temperature rises to the set limit value all compressor steps are immediately cut out.

The alarm is cancelled and renewed cut-in of compressor steps is permitted when the following conditions are met:

- the temperature has dropped to 10 K below the limit value

- the time delay prior to restart has been passed (see later) Normal condenser control is permitted again when the temperature has dropped to 10 K below the limit value.

Oil pressure safety Over current safety Motor protect. safety Discharge  temp. safety Discharge pressure safety

##### Individual Sd monitoring

The affected compressor will be disconnected here when the temperature exceeds the threshold value.

- The piston compressor will be reconnected when the temperature has dropped 10 K

- The screw compressor will be reconnected when the temperature has dropped 20 K

- The capacity of compressors with variable capacity is increased if the temperature is approaching the limit. Once it has been cut out, it will only be connected when the temperature has dropped 10 K.

If signals are also obtained from the embedded NTC sensor, the disconnect value for this temperature will always remain at 130 °C and the reconnect value at 120 °C.

###### Common safety circuit

A common safety signal can also be received from the whole suction group. All compressors will be cut out when the safety signal cuts out. The function may not be connected to an external main switch.

##### **Monitoring of min. suction pressure (P0)**

The function promptly cuts out all compressor steps if the suction pressure becomes lower than the permitted value. The cut-out limit can be defined in the range from -120 to +30°C. The suction is measured with pressure transmitter P0.

##### At cut-out the alarm function is activated:

The alarm is cancelled and renewed cut-in of compressor steps is permitted when the following conditions are met: - the pressure (temperature) is above the cut-out limit

If the pressure continues to increase exceeding the actual safety limit "Pc max. limit MT", the following will happen: - all MT compressor steps will immediately be cut out - condenser fan capacity remains fully active

- “High Pressure Pc-MT” alarm is activated

The alarm will be cancelled, cut-in of compressor steps is permitted again and condenser fan stops to be forced at maximum when the following conditions are met: - the pressure falls below the "Pc max avoid limit MT” limit

- the time delay for restart has been passed

- the time delay has elapsed (see later).

##### **Monitoring of max. condensing pressure (Pc)**

The condensing pressure, measured by pressure transmitter Pc, is continuously monitored to guarantee safety of the plant when pressure exceeds the user safety limit " Pc max limit MT". This functionality is part of the MT suction group safety.

A preventive action is initiated when the pressure reaches a threshold 3 to 4 bar lower than the safety limit, known as the "Pc max. avoid limit MT".

When triggered, the controller performs the following actions: - The entire condenser fan capacity is immediately cut-in - MT compressor steps are sequentially cut-out every 30 sec. More precisely, 25% of the current compressor capacity is cut-out (minimum one step) which is repeated every 30 seconds until minimum compressor capacity is reached.

The actual difference between the safety limit “ Pc max. limit MT" and the threshold of preventive action "Pc max avoid limit MT" can vary between 3 to 4 bar.

- A difference of 3 bar is used when “Pc max. limit MT” is below 67 bar

- A difference of 4 bar is used when “Pc max. avoid limit MT” is above 67 bar

The controller guarantees smooth transition between the 3 bar and 4 bar difference round 67 bar. The actual value is displayed inside “SetPoint Manager” menu in the HP control page

The feature is also available for IT suction group with user safety limit "Pc max. limit IT".

The pressure sensor is Pc, “High Pressure Pc-IT” alarm and  IT compressors cut-out will be triggered, similarly as described for MT.

The feature is also available for LT suction group with user safety limit "Pc max. limit LT". The pressure sensors monitored is Po-MT, “High Pressure Pc-LT” alarm and LT compressors cut-out will be triggered, similarly as described for MT.

##### **Delay of Pc max alarms**

It is possible to delay the “Pc max alarm" message. The controller will still disconnect the compressors, but the sending of the alarm itself is delayed.

The delay is useful on cascade systems where the max. Pc limit is used to disconnect compressors in the low-pressure circuit if the high-pressure compressors have not started.

##### **Time delay**

There is a joint time delay for “Monitoring of max. discharge gas temperature” and “Min. suction pressure”. After a cut-out, regulation cannot be recommenced until the time delay has been passed.

The time delay starts when the Sd temperature has again dropped to 10 K below the limit value or P0 has risen above the P0 min. value.

##### **Alarm for too high suction pressure**

An alarm limit can be set which will become effective when the suction pressure becomes too high. An alarm will be transmitted when the set time delay has been passed. The regulation continues unchanged.

##### **Monitoring max. receiver pressure**

If the receiver pressure is approaching the max. value, the compressors will be cut out as described under ‘Monitoring max. condenser pressure’. An alarm will be transmitted when this limit is exceeded.

### **5.3 Oil management**

The controller can control the pressure in an oil receiver and ensure the evacuation of two oil separators. The evacuation is carried out with a number of pulses, e.g. of 1 second duration followed by a pause of 1 minute.

The system can be controlled by signal from:

- Level switch on oil separator

- Pressure transmitter on oil receiver

All oil valves are closed when "Main switch" is Off.

*[Figurtekst: Examples of oil circuits:]*

*[Figurtekst: Separator 1 Separator 1 · Receiver · Separator 2 · Receiver]*

##### **Control principle for emptying the oil separator in the receiver**

##### **Control principle for pressure in the receiver**

Pressostat

The oil level in the separator can be controlled with either one or two level switches. The oil is drained into the oil receiver via a pulsing solenoid valve, that can be operated in two different, user defined, cycling sequences.

##### **Systems with one level switch**

Full sequence:

When the level switch registers oil, the oil is emptied into the receiver running all periods. Users define the pulse length, period time between pulses and number of periods.

##### To level:

Here the pulse sequence starts at activation of the switch, but the sequence stops immediately once the oil level falls below the level switch.

For both, If the level switch is still registering oil after the total number of periods has finished, an alarm is given for high oil level in the separator.

In the case of lack of pressure difference to fill the MT compressors, the solenoid valve is opened in user defined pulses and the pressure is taken from the oil separator. The pulse length and the period time between the pulses is determined by the system and are the same as those set for the oil separator.

##### Regulation acc. to pressure

When the pressure transmitter registers the required pressure, the pulses are stopped.

Structure according to time

Here, the controller uses a timer function to determine the pressure build-up in the receiver. There is no regulation.

##### Differential pressure

Here, regulation is performed based on the receiver pressure and the pressure in the CO2 receiver (Prec). The controller will regulate in accordance with the desired differential pressure.

##### Monitoring

##### **Systems with two level switches**

Here, the high-level switch will start the pulse sequence, and the low-level switch will stop the pulse sequence. If the high level switch is still registering oil after the total number of pulses has finished, an alarm is given for high oil level in the separator.

High and low level signals can be received from the receiver. These signals are only used for monitoring and alarms.

If the low level switch is still registering oil after the total number of pulses is finished, an alarm is given for remaining oil in the separator.

An alarm for signal failure is also given if the high level switch registers oil while a low level switch does not register oil. If either the high or low level switch is not activated in the set “No oil sep. alarm delay”, a "no oil separated" alarm is given.

### **5.4 Condenser / Gas cooler**

The condenser in a transcritical CO2 system is also called a gas cooler. Unlike in an HFC system, sub-cooling is not controlled by a condenser, but by the high-pressure valve Vhp.

The gas cooler control must regulate the temperature in the gas cooler’s discharge, so that it has the lowest possible value and the energy consumption of the fans is minimal. However, this should not be so low as to prevent the receiver pressure from being maintained.

Capacity control of the condenser (gas cooler) can be accomplished via  step regulation or speed control of the fans.

- EC motors An analogue output signal is used here, which controls the fans from 0 to maximum capacity.

- Step regulation The controller can control up to 8 condenser steps that are cut in and out sequentially.

- Speed control

The analogue output voltage is connected to a speed control. All fans will now be controlled from 0 to max. capacity. If an ON/ OFF signal is required it can be obtained from a relay output. Regulation can be carried out based on one of the following principles:

- all fans operate at the same speed

- Only the necessary number of fans is cut in.

- Combination of speed regulated and the step regulation.

##### **Condenser fan control status description**

##### **Control status describes what the controller is doing:**

**OFF :** Main switch is OFF **Standby :** Controller is ready to start. **Manual :** Control Mode Manual **Manual OFF :** Control mode OFF. **Idle :** Requested cap. is zero. waiting for compressors to start.

**Normal ctrl. :** Normal control. **Sensor error :** Control sensor error. **Sensor error idle :** Control sensor error. **V3gc Coor. :** Fans are not running, and V3gc bypass valve is controlling.

**Night Limit :** Requested cap. is limited by night limit.

- **Forced by DI :** Fan requested capacity is enforced by "Forcing fan speed via DI" being active.

Step regulation

*[Figurtekst: Speed control and step · regulation]*

Speed control

Speed control on the first. Step regulation on the others

##### **Forced off**

- **by DI :** Fan requested capacity is enforced by "Forcing fan speed via DI" being active.

- **High Sgc idle :** Requested cap. is increased because Sgc is too high.

- **High Sgc :** Requested cap. is increased because Sgc is too high.

**High Pc :** Requested capacity is increased to avoid High Pc. **High Sd :** Requested capacity is increased to avoid High Sd. **High Prec :** Requested cap. is increased because receiver

- **:** Requested capacity is increased to avoid High Sd.

- **:** Requested cap. is increased because receiver pressure is too high.

**High Pgc**

- **:** Requested cap. is increased because Pgc is too high.

Speed control of the 2 groups. Group 1 must have less or same number as group 2

### **5.4.1 Capacity control of condenser**

The gas cooler outlet temperature is controlled with the fan capacity and the 3-way by-pass valve V3gc. Regulation is performed by a PI controller which may however be changed into a P controller if the design of the plant necessitates this.

##### **PI regulation**

The controller cuts in capacity in such a way that the deviation between the actual condensing pressure and the reference value becomes as small as possible.

##### **P regulation**

The controller cuts in capacity that depends on the deviation between the actual condensing pressure and the reference value. The proportional band Xp indicates the deviation. The adjustments are carried out using amplification factor Kp, where Xp = 100/Kp.

*[Figurtekst: ⁰C · Xp · Pc Ref · 0% 50% 100% Cond. · cap. %]*

##### **Regulating sensor selection**

The capacity distributor can either regulate from a temperature sensor, Sgc, placed at the outlet of the gas cooler or based on a medium temperature, S7.

Cap. Ctrl sensor = Sgc / S7

If the regulation sensor is selected for medium temperature S7, then Pc is still used as the safety function for high condenser pressure and will therefore ensure cut-out of the compressor capacity when condenser pressure is too high.

##### 2 Sgc sensors:

If the option 2 sgc sensors is chosen, then the sensor with the highest value is used for control. An alarm is given if the difference between the two sensor values is higher than the user-set "Delta before alarm" parameter.

##### Handling sensor errors on Sgc and S7:

In case of sensor error, the fans switch to emergency operation. The fans are then controlled according to the compressor capacity and Sc3, if this is installed.

### **5.4.2 Reference for gas cooler temperature**

The reference for the regulation can be defined in two ways. Either as a fixed reference or as a reference that varies according to the outdoor temperature.

**Note:** In case S7 is selected as regulating sensor, the heat exchange between external temperature and brine must be considered. In this case it is suggested to increase the subcooling value used for Pgc reference calculation by 2K (see HP control section).

##### **Floating reference** (recommended)

This function allows the condensing pressure’s reference value to vary within a defined range. The reference varies according to the outdoor temperature and the connected compressor capacity. By combining floating condensing pressure with electronic expansion valves, a lot of energy saving can be achieved. The electronic expansion valves enable the controller to decrease the condensing pressure according to outdoor temperature and thereby reduce energy consumption by around 2% for each degree the temperature can be decreased.

The measured outdoor temperature is also used by the controller to optimise the regulation algorithm. The function can be compared to a variable Kp value, which is higher during warm periods and lower during cold periods. There is no setting.

The reference is based on:

- the outdoor temperature measured with Sc3 sensor

- the minimum temperature difference between the air temperature and the condensing temperature at 0% compressor capacity.

- the condenser’s dimensioned temperature difference between the air temperature and the condensing temperature at 100% compressor capacity (Dim tmK)

- how large a part of the compressor capacity has been cut in.

*[Figurtekst: Pc Ref. ⁰C · Sc3 + Dim tm K · Pc Ref at · 50% Comp. · capacity · Sc3 + Min tm K · Sc3 · 0% 50% 100% Comp. · cap. % · ⁰C · Xp · Sc3+3K · 0% 50% 100% Cond. · cap. %]*

The minimum temperature difference (min tm) at low load should be set at approximately 2 K as this will eliminate the risk that all fans will be running when no compressors are running. Set the dimensioned difference (dim tm) at max. load (e.g. 4 K).

The controller will now contribute with a value to the reference which depends on how large a part of the compressor capacity has been cut in.

##### **P-regulation**

The reference is calculated as for PI regulation. The set-up is carried out using the amplification factor Kp (Xp = 100/Kp).

##### **Fixed reference**

The reference for the condensing pressure is set in °C.

##### **Max gas cooler temperature**

Set a max. gas cooler temperature if it needs to be limited. If the max. limit is reached, the fans will increase speed to the max. fan speed.

##### **Adaptive minimum reference**

The minimum reference is controlled in an adaptive way. The receiver is controlled by letting gas escape through the bypass Vrec valve. Thus when there is no gas entering the receiver, this valve will be closed and the receiver pressure is uncontrolled. This puts a limit on the outlet of the gas cooler. For this reason it is possible to set a "receiver inlet min. vapour" quality threshold.

The controller will keep the inlet quality above this limit. This results in a minimum Sgc and Pgc reference.

*[Figurtekst: Minimum Pgcref, Sgcref · P · Receiver inlet min. vapour · Prohibited zone]*

##### **Special operation modes for condenser fans**

Forced operation of the capacity can be arranged where the normal regulation is ignored.

The safety functions are cancelled during forced operation.

Forced operation via setting The regulation is set to Manual. The capacity is set in percentage of the regulated capacity.

##### Forced operation of relays

If the forced operation is carried out with the switches at the front of an extension module, the safety function will register any exceeding of values and transmit alarms, if required, but the controller cannot cut the relays in or out in this situation.

##### Forced operation due to high receiver pressure

In case of high receiver pressure, the condenser fans will be activated in the high Pband of receiver pressure.

##### Fans' behavior with compressor off:

When MT and IT compressors are off, the fans are operated from 0 – 100% in a band from 5 – 15 K above Sgc reference.

##### **Forcing fan speed via DI**

When configured and activated by DI, fan requested capacity is forced to (depending by the settings):

- MaxSpeed: Fan forced to maximum speed. (100% for VSD fan type or "EC max." for EC fan type)

- Prop%CMP: Fan capacity forced to linear increase from 30% to 100% based on the highest capacity between MT and IT compressor.

The safety functions are not canceled during this forced operation, but request capacity is zero when MT and IT compressors are off except for High Pc/Sd.

### **5.4.3 Capacity distribution**

##### **Step regulation**

Cut-ins and cut-outs are carried out sequentially. The last cut-in unit will be cut out first.

##### **Speed regulation**

When an analogue output is used, the fans can be speed regulated, e.g. with a frequency converter type VLT or a EC motor.

##### **Joint speed regulation**

The analogue output voltage is connected to the speed regulation. All fans will now be regulated from 0 to max. capacity. If an ON/OFF signal is required for the frequency converter, so that the fans can be stopped completely, a relay output can be defined.

*[Figurtekst: Speed % (RPM) · Start · Min. · Req. cap %]*

The controller starts the frequency converter when the capacity requirement corresponds to the set starting speed. The controller stops the frequency converter when the capacity requirement becomes lower than the set minimum speed.

##### **Speed regulation + step regulation**

*[Figurtekst: Speed % (RPM) · Start · Min. · Req. cap %]*

The controller starts the frequency converter and the first fan when the capacity requirement corresponds to the set starting speed.

The controller cuts in several fans step by step as the capacity requirement grows and then adapts the speed to the new situation.

The controller cuts out fans when the capacity requirement becomes lower than the set minimum speed.

**Note:** This feature increases the risk of receiver pressure to collapse, if too cold liquid will result from the fan action. It is not recommended to activate this feature in cold weather condition or with heat recovery.

##### **EC Motor**

The voltage signal to the EC motor is defined by the following settings:

EC min. (typically 20% corresponding to 2 V at 0-10 volt signal) EC max. (typically 80% corresponding to 8 V at 0-10 volt signal) EC absolute max. (typically 100% corresponding to 10 V)

In the configuration of the controller’s outputs it will be the output “FanA1”” that will start and stop the frequency converter.

##### **Speed regulation of first fan + step regulation of the rest**

*[Figurtekst: EC [V] · If (sgc>Sgc absolute max) · EC abs. max · EC Max · Start · Min · Fan req [%]]*

If the Sgc temperature exceeds the defined “Absolute Max Sgc temperature”, the output voltage will be allowed to increase to the EC absolute maximum value.

##### **Capacity limitation during night operation**

The function is used to reduce the noise from the fans to a minimum. It is primarily used in conjunction with a speed control, but it will also be active when steps are cut in and out. The setting is arranged as a percentage of the max. capacity.

The controller starts the frequency converter and increases the speed of the first fan. If additional capacity is required, the next fan cuts in at the same time as the first fan switches to minimum speed. From here, the first fan can increase speed again, etc.

##### **Speed regulation for fans divided into 2 groups**

At low loads, only group 1 will be cut in. When the load increases and a calculated start value for group 2 is exceeded, group 2 will be started.

When group 2 is cut in, the speed will be the same for both groups. The number of fans in the two groups can be the same, but if there is a difference, group 1 must be smaller.

The limitation will be disregarded when safety functions Sd max. and Pc max. take effect.

##### **Fans status overview:**

##### **Fan status overview page describes:**

- Summary of the fan running condition for the full set of fans

- Running status for fan1

- Running status for fan2 and so on

**When “Condenser fan control” is step or “Fan speed type” is VSD, the summary status shows: Stopped :** Fans are not running.

**Running :** Fans are running below 100%. **At max. :** Fans are running at 100%. **Instead, when “Fan speed type” is EC, the summary status shows: Stopped :** Fans are not running. **Running :** Fans are running below “EC max.". **At max. :** Fans are running at “EC max.". **Above max. :** Fans are running above “EC max.", and below “EC abs.max." limit.

**At abs. max. :** Fans are running at “EC abs.max." limit.

### **5.5 Condenser couplings**

##### **Coupling of condenser steps**

There are no time delays in connection with cut-in and cut-out of condenser steps beyond the time delay inherent in the PI/Pregulation.

##### **Timer**

The operating time of a fan motor is registered continuously. You can read out:

- operating time for the previous 24-hour period

- total operating time since the timer was last set to zero-set

##### **Coupling counter**

The number of couplings is registered continuously. Here the number of starts can be read out:

- number during the previous 24-hour period

- total number since the counter was last set to zero-set

##### **Exercising fans**

The last fans are unlikely to be activated during winter months. To ensure that the fans are 'exercised', a test will be carried out every 24 hours to check whether all relays have been in operation. The relays that have not been used will now be activated for 5 sec. (from 13:00) but with a pause of 5 min. hour between individual relays. A speed control is run at "Start speed".

### **5.6 Safety functions for condenser**

##### **Signal from fan and frequency converter’s safety controls**

The controller can receive signals on the status of each individual condenser step’s safety circuit.

The signal is obtained directly from the safety circuit and connected to a “DI” input.

If the safety circuit is cut out, the controller will give alarm. Regulation continues with the remaining steps.

The ancillary relay outlet is not cut out. The reason for this is that the fans are often connected in pairs but with one safety circuit. With fault on one of the fans, the other will continue to operate.

##### **Modulating gas cooler by-pass valve (V3gc)**

It can happen that the gas cooler outlet temperature is too low even though the fans are off. Typically this happens in very cold weather or when the reference is raised during heat recovery. The modulating by-pass valve can then be used to raise this temperature.

The gas cooler has a tendency to fill up with cold liquid when it is fully by-passed. This can be avoided by a maximum limit on the opening degree of the gas cooler by-pass valve.

### **5.7 CO2 transcritical system and heat recovery**

##### **General**

In CO2 systems, the higher pressure and temperature makes it possible to recover heat for tap water and heating. The excess heat is removed using a gas cooler.

Regulation is carried out during transcritical and subcritical states and the controller will control the gas pressure/condensing pressure so that the system achieves the optimum COP when the recovered heat is taken into account.

The two heat recovery circuits can be considered as independent circuits - also with regard to the cooling system. First, the circuit for hot tap water will take the energy it needs to use. The remaining energy is then available for use by the next circuit. This also takes what is available. If there is then any excess energy this is removed via the gas cooler.

There must be a cooling requirement in order to supply for heat recovery.

The regulation of the heat recovery circuits is done with regard to the cooling system. When the regulation is facing operational constraints, the cooling system will have priority over the heat recovery.

*[Figurtekst: Direct Heat Reclaim Heat Recovery Unit · Recirculator Shr8 FShr 60 °C · M 18 °C · V3sf M Pump hr · M Shr4 Fshr Shr4 Shr3 · 5 °C Shr2 30 °C Shr2 · M V3hr · M V3hr · Tap Water Stw8 Heat Reclaim Shr8 · FStw 55 °C FShr 40 °C · Pump Pump · tw hr · Pc Stw4 Stw3 Shr4 Shr3 CTR M M · Sd Stw2 Shr2 · M V3tw M V3hr V3gc Sgc · Sc3 · CCMT · Pgc Important: · This sensor must be placed · CCMT Shp immediately at the gas · Vhp cooler outlet. · Prec · Vrec Co2 · Lco2 · rec]*

##### **Info**

In normal operating conditions, the temperature at Sd will be between 60 and 70 °C - depending on whether it is winter or summer.

If the "Heat reclaim" function is to raise the condensing pressure, the temperature may increase to 90° or higher.

The Sc3 sensor should be positioned so that it measures the air intake temperature for the gas cooler. If it measures a temperature that is too high, the system's COP will become impaired.

The Sgc signal must be stable. When this cannot be done using a system sensor, it may be necessary to use an immersion tube sensor.

There are safety functions for the individual regulation functions, for example:

- Boiling at S3, S4 and S8

- An S3 temperature must be lower than the gas temperature that can be sent into the heat exchanger. If the S3 temperature is higher, the circuit is not connected.

The pump is kept running for a little while before and after the gas valves connect. It can take up to 2 minutes for the gas valve to change position.

**Note:** the diagram above describes four different combinations of heat recovery unit. The user can select as follows:

1. 'Tap water'

2. 'Heat reclaim'

3. Both 'Tap water' and 'Heat reclaim'

##### **Remember the isolation amplifier**

If signals are received from different controls, e.g. heat recovery for one of the inputs, a galvanically insulated module should be inserted.

4. 'Heat Recovery Unit'

5. 'Direct heat reclaim'

### **5.7.1 Heat recovery - Circuit for hot tap water**

*[Figurtekst: Reference · Band]*

This regulation makes it possible to supply hot gas for heating a receiver vessel.

##### **The pump - Pump tw**

Pump can be on/off or variable speed. When on/off, the pump start/stop signal is the combination of the two heat recovery requests previously described. When variable speed, the pump speed is regulated by the control signal and the heat recovery requests provide only the start/stop signal to the pump.

Regulation is done for a tap water temperature of typically 55°C, where the value is adjustable. A temperature sensor Stw8 is installed in the hot water receiver, and the temperature is held in a band around the adjusted value.

Pump regulation depends on the control signal as following:

- Only Stw8. The pump can be controlled on/off or variably

If Stw8 or Stw4 is selected as the controller sensor, the reference can be displaced based on an external 0 – 10 V signal. 0 V result in no displacement. 10 V result in a displacement indicated by the set value.

- Only Stw4. The pump has to be variably controlled.

- Stw4 - Stw3. Here "Delta T" over the heat exchanger is used for pump regulation. Here the pump must be controlled using variable speed

- Stw8 and Stw8a: The pump is controlled via on/off

*[Figurtekst: Reference · Band]*

**Valve  -** V3tw

When tap water heating is required, the gas valve changes over and routes the gas in through the heat exchanger. When the temperature goes above the reference plus half the band, the gas will be routed outside of the heat exchanger.

##### **Heat recovery request**

Regulation of heat recovery if determined by an external heat recovery request via digital input (Tw enable) and an internal thermostat. Both requests must be present to allow opening the V3tw valve and starting the pump control. The internal thermostat request gets activated when the selected thermostat sensor is below reference minus half of the band and it stays active until temperature is above reference plus half of the band.

It is recommended to use a pump with variable speed, so that the finer temperature regulation minimize fluctuations in the condensing pressure.

To avoid the pump being blocked after long period of inactivity, enable "Pump Exerciser" functionality (disable by default). The controller will run the pump for 30 s at minimum speed after 24 h of inactivity.

**Flow switch -** FShr

A flow switch should be installed for safety reasons, in case of flow fault. The controller will then disconnect the entire recovery circuit.

**Sensors -** Stw2, Stw3, Stw4 and Stw8

All sensors must be installed due to safety reasons: Stw2: The controller must know the temperature of the gas that is sent for condensation Stw3: Heat exchanger cold access. Used for temperature regulation Stw4: Heat exchanger hot outlet. Used for temperature regulation Stw8: Receiver temperature and in relation to the reference.

The thermostat sensor is always one the following:

- Stw8 (with  “Stw8” or “Stw4 - Stw3” as control signal).

- Stw4 (with “Stw4” as control signal).

- Stw8 and Stw8a (with “Stw8 and Stw8a” as control signal). Here regulation is done using the two temperature sensors in the receiver. Stw8 is placed at the top and Stw8a further down. The pump is controlled via on/off and is connected when Stw8 is below the reference plus half the difference. It is disconnected when Stw8a is above the reference plus half the difference.

##### **Start and Stop conditions**

The purpose of the heat recovery functionality is to recover heat when  requested guaranteeing the safety of the refrigeration system and the hydraulic loops. This section describes start and stop conditions for tap water circuit and the overview page “Hot tap water status”.

In the “Hot tap water status” page, the controller monitors the presence of heat recovery requests (Active or None) and the fulfilment of the safety checks (OK or Failure). In cases the safety check or the request is not applicable, "Unconfigured" is shown.

|Tap water status|
|---|
|Actuators states|
|Request status|
|Safety checks|
|Timer checks|

- 4.9. Sd and Stw3 check is OK: “Sd MT” is  higher than Stw3 brine temp.

   - If “Control signal” = “Stw8” or “Stw4”, then “Sd MT" must be higher than (Stw3 +1K)

   - If “Control signal” = “Stw4 – Stw3”, then “Sd MT” must be higher than (Stw3 + Delta T)

- 4.10 Receiver safety is OK: No low Prec pressure (check “Actions on low receiver pressure” in Receiver control)

When all conditions are fulfilled, the following start sequence will be carried out:

1. The pump will be started (if not already running)

2. The by-pass valve will switch position and the discharge gas will be looped through the heat exchanger.

3. DO “Tw Heat delivered” is activated.

##### **Stop conditions**

The heat recovery will be stopped at one of the following conditions:

1. Control mode is set to OFF

2. The external heat request signal on the DI is stopped

3. Internal Thermostat request is “None”: Thermostat sensor is above reference plus half of the band

4. One of the following safety check fails:

- 4.1. Anti Boiling check Fails:  Risk of boiling is detected and Antiboiling safety is active

- 4.2. Anti Boiling sensor error check fails:  Sensor error for any of sensor used for antiboiling

- 4.3. Flow Check fails: The flow switch reports“Flow Error”,  if configured

- 4.4. Sd error check fails: Sensor error on "Sd MT"

- 4.5. MT Compressor stable running fails: all MT compressors stopped

- 4.6. Receiver safety fails: Prec is too low (check “Actions on low receiver pressure” in Receiver control)

When one of the stop conditions is active, the following stop

sequence will be initiated:

1. The three way valve V3tw will switch position and bypass the gas.

2. DO “Tw Heat delivered” is OFF.

3. A shut down stage gets activated. The pump will continue to run 180 sec in order to remove the excessive heat in the heat exchanger. If a new heat request arises within the 180 sec, the pump will keep running.

##### **Start conditions**

The following conditions must be fulfilled on order to start the tap water heat recovery function:

1. Control mode is set to “Auto”

2. DI external Heat request is “Active”: Tw enable ON. 3. Internal Thermostat request is “Active”: thermostat sensor is below reference minus half of the band

4. All safety checks are OK, specifically:

- 4.1. Anti Boiling is OK: No risk of boiling is detected 4.2. Anti Boiling sensor error is OK: No sensor error for all the sensors used for antiboiling

- 4.3. Flow Check is OK: Flow switch report "Flow OK" (if configured)

- 4.4. Sd error check is OK: No sensor error on "Sd MT"

- 4.5. MT Compressor stable running is OK: At least one MT compressor must have been running for at least 10 sec

- 4.6. Stw2 error check is OK:  No sensor error on Stw2

- 4.7. Stw2 check is OK: Stw2 must be higher than "S2 check limit" 4.8. Stw3 error check is OK: No sensor error on Stw3

##### **Pause conditions**

When a stop condition is reached a shutdown stage is triggered and it can takes minutes before heat recovery is available again. To prevent that, V3tw valve will by-pass heat exchanger without activating a shutdown cycle after a pause condition is triggered then the following sequence will be initiated instead:

1. The three way valve V3tw will switch position and bypass the gas. The valve will change position without delay as soon all safety checks are OK

2. DO “Tw Heat delivered” is OFF.

3. The pump will continue to run and control normally.

Pause conditions are listed below:

1. Stw2 check fails: Stw2 is lower than "S2 check limit"

2. Sd and Stw3 check fails: “Sd MT” is not high enough compared to Stw3 brine temp.

- If “Control signal” = “Stw8” or “Stw4”, then “Sd MT" must be higher than (Stw3 +1K)

- If “Control signal” = “Stw4 – Stw3”, then “Sd MT” must be higher than (Stw3 + Delta T)

3. Stw2 error check fails:  Sensor error on Stw2

4. Stw3 error check fails: Sensor error on Stw3 (when Stw4 - Stw3 is not selected as control signal)

### **5.7.2 Heat recovery - Circuit for heat reclaim for heating**

Regulation can be carried out using one of the following three principles, when the circuit calls for heat:

1. Basic control (no HP offset).

2. Offset of the condensing pressure (HP offset)

3. Offset and regulation of the gas cooler and pump (max. hr)

##### **Generally, for all three principles:**

**Valve  -** V3hr

When heating of the circuit is required, the gas valve will change over and route the gas in through the heat exchanger. When the temperature goes above the reference plus half the band, the gas will be routed outside of the heat exchanger and the pump shuts down after 180 sec.

##### **Heat recovery Request**

Regulation of heat recovery requires an external heat request via DI. For “no HP offset” and “HP offset”, request from internal thermostat is also needed.  For max heat reclaim, the internal thermostat is replaced by an external analog input request (consumer request). The two requests must be present simultaneously to allow opening the V3hr valve and starting the pump control.

##### **The pump - Pump hr**

Pump can be on/off or variable speed. For both configuration the pump start/stop signal is the combination of the two heat recovery requests previously described, the pump speed will be 0% or 100% based on that signal. When variable speed, the pump speed will be determined based on the deviation between the setpoint and the actual temperature using one of following control sensors:

- Only Shr8. The pump can be controlled on/off or variable speed.

- Only Shr4. Variable speed only.

- Shr4 - Shr3. Here "Delta T" over the heat exchanger is used for pump regulation. Variable speed only.

It is recommended to use a pump with variable speed, so that the finer temperature regulation minimize fluctuations in the condensing pressure.

To avoid the pump being blocked after long period of inactivity, enable "Pump Exerciser" functionality (disable by default). The controller will run the pump for 30 s at minimum speed after 24 h of inactivity.

##### **1. Basic control (no HP offset)**

Regulation is done using a receiver temperature of e.g. 40 °C, the value is adjustable. A temperature sensor Shr8 is installed in the receiver, and the temperature is maintained in a band around the selected value.

The reference can be displaced variably using an external 0 – 10 V signal. 0 V result in no displacement. 10 V result in a displacement indicated by the set value.

*[Figurtekst: Reference · Band]*

##### **Internal thermostat request**

The internal thermostat requests heat when the thermostat sensor is below reference minus half of the band. The internal thermostat request stays active until temperature is above reference plus half of the band.

The thermostat sensor is always one the following:

- Shr8 (with Shr8 or Shr4 - Shr3 as control signal)

- Shr4 (with Shr4 as control signal).

The V3gc valve type is not included in this regulation. All gas is led through the gas cooler.

##### **Flow switch -** FShr

A flow switch should be installed for safety reasons, in case of flow fault. The controller will then disconnect the entire recovery circuit.

**Sensors  -** Shr2, Shr3, Shr4 and Shr8  (Stw2/Sd)

All sensors must be installed due to safety reasons: Shr2: The controller must know the temperature of the gas that is sent for condensation

Shr3: Heat exchanger cold access. Used for temperature regulation Shr4: Heat exchanger hot outlet. Used for temperature regulation Shr8: Receiver temperature and in relation to the reference Stw2 or Sd: The regulation must know the temperature of the gas that is sent into the heat exchanger.

##### **2. Heat reclaim mode: Hp offset and temperature reference**

Regulation is done using a heat exchanger temperature/receiver temperature of e.g. 40 °C, the value is adjustable. A temperature sensor Shr8 is installed in the receiver and the temperature is maintained in a band around the selected value.

The reference can be displaced variably using an external 0 – 10 V signal. 0 V result in no displacement. 10 V result in a displacement indicated by the set value.

##### **Internal thermostat request**

The internal thermostat requests heat when the thermostat sensor is below reference minus half of the band. The internal thermostat request stays active until temperature is above reference minus half of the band.

The thermostat sensor is always one the following:

- Shr8 (with Shr8 or Shr4 - Shr3 as control signal)

- Shr4 (with Shr4 as control signal).

The V3gc valve type is not included in this regulation. All gas is led through the gas cooler.

##### **Increasing the condensing pressure and temperature**

When the selected regulation sensor is below reference and heat recovery is running, the gas cooler pressure reference, Pgc ref, and the gas cooler outlet temperature reference, Sgc ref, can be increased.

The pressure is measured using the pressure transmitter Pgc and controlled by the Vhp valve.

How much the pressure and the temperature shall be increased by is determined using a setting and an analogue voltage signal. The signal must be a 0 – 10 V signal or a 0 – 5 V signal.

*[Figurtekst: Max. · Sgc normal 1/3 · control Sgc ref · Max. · Min. · 2/3 1/3 · U · 0 10 V · (5V) · Pgc HR · Sgc · 2/3 gcP ref]*

When heat recovery is activated (with a digital signal), the gas cooler pressure reference (Pgc ref), is increased to “Pgc HR min”. At 2/3 signal (e.g. 6.6 V) the pressure reference will increase to the setting "Pgc HR max". Anyway "Pgc ref" is allowed to be higher than "Pgc HR Max", when "Extra refrigeration capacity ("extra compressors") function is activated.

Below 2/3 of the heat recovery request signal SgcRef is not directly affected by the signal. From 2/3 to 3/3 of the signal, the SgcRef will start increasing calculated by the controller based on the setting "Pgc HR max".

Up to 5 signals can be received from external regulations. They can all increase the pressure, and the controller will use the signal that requires the largest offset.  The signal employed is filtered over a time period. The length of the period can be set.

##### **Relay output**

A relay can be reserved that will pull in if the received signal exceeds 9.5 V (4.75 V) for more than 10 mins. The relay is defined in the function: "Additional heat output".

##### **Remember the isolation amplifier**

If signals are received from different controls, e.g. heat recovery for one of the inputs, a galvanically insulated module should be inserted.

##### **3. Heat reclaim mode: Max. heat reclaim**

In the “Max heat reclaim mode” the regulation is solely based upon the external heat request (consumer request) on an analogue input and a start signal on a digital input. Note, there is no active thermostat control for the heat recovery mode. To prevent any boiling in the system, the heat recovery will be stopped, as soon as any of the Shr3, Shr4 or Shr8 temperatures are above 95 °C.

##### **Increasing the condensation pressure**

Up to 5 different signals can be received from external heat consumers. The controller will use the signal that requires the highest capacity. The resulting signal is filtered over a time period. The filter time is adjustable (Heat consumer filter).

An external heat controller will send a heat request signal between 0 and 10 V (0 – 5 V), which will be used to start the following functions in order to achieve maximum heat recovery:

1. Signal on DI input for heat recovery is received (mandatory, to enable the function) and the reference for the pressure Pgc is increased to "Pgc HR min." If the external signal is above HR start limit.

2. The external voltage signal is registered (the higher the value, the greater the need for heat). The signal is converted by the controller to 0 – 100% capacity and will have the following impact:

   - a. ON/OFF control of pump and by-pass valve V3hr The pump is released to start, when the request signal reaches the “HR start limit” and the by-pass valve V3hr opens for the heat recovery. The valve V3hr goes into "bypass" when the "HR stop limit" is reached, and the pump is stopped after 180 sec.

*[Figurtekst: 2/3 1/3 · Sgc ref 100% · offset · 0% · Pgc ref Max · offset · Min · Pump · Gas c. · bypass · 5% 10% 25% 70% 80% 95% · HR request · 5%  HR stop limit 70% Ref offset high · 10%  HR start limit 80%  V3gc bypass stop limit · 25% Ref offset low 95%  V3gc bypass start limit]*

- b. Pressure and temperature increase The pressure is measured with the pressure transmitter Pgc and controlled with the High pressure valve Vhp. Based on the Heat request, the pressure reference “Pgc ref” will be raised from “Pgc HR min” to “Pgc HR Max”. If the "Extra refrigeration capacity function ("extra compressors") is activated, “Pgc ref” may exceed “Pgc HR max”. Once “Pgc ref” reaches “Pgc HR max” the gas cooler temperature setpoint “Sgc ref” is increased up to “Sgc HR Max”. Raising the gas cooler temperature reference results first in a reduction of fan speed and then in the activation of modulating V3gc (if configured). The parameter “Sgc HR Max” is calculated by the controller based on the setting "Pgc HR max".

- c1. V3gc is modulating: The controller controls the fans and the valve, to maintain energy optimized control (bypassing of the gas cooler will only be allowed when the fans are at 0% and vice versa). Shp is the control sensor when the gascooler is bypassed.

- c2. V3gc is set to an on/off valve (see illustration): the fans will be stopped and the valve V3gc routes the gas outside the gas cooler. If the HR request is between V3gc bypass stop limit & V3gc bypass start limit, the V3gc won't bypass unless Shr2 & Sgc are lower than "TC max HR".

The “Heat recovery status” picture shows the current regulation status.

**Relay output** (additional heat output)

A relay can be reserved that will pull in if the received signal exceeds 9.5 V (4.75 V) for more than 10 minutes. The relay will be cut out when the signal is lower than 9.3 V (4.65 V). The relay is defined in the function: "Additional heat output", and can be used to start e.g. a heat pump  evaporator.

##### **4. Start and Stop conditions**

The purpose of the heat recovery functionality is to recover heat when  requested guaranteeing the safety of the refrigeration system and the hydraulic loops. This section describes start and stop conditions for heat reclaim circuit and the overview page “Heat reclaim status”. The start/stop conditions are intended for all heat reclaim types (No HP offset, HP offset and Max Heat reclaim) when not explicitly specified.

In the “Heat reclaim status” page, the controller monitors heat recovery requests (Active or None) and the fulfilment of the safety checks (OK or Failure). In cases the safety check or the request is not applicable, "Unconfigured" is shown.

|Hr status|
|---|
|Actuator states<br>Request status|
|Safety checks|
|Timer checks|

##### **Start conditions**

The following conditions must be fulfilled on order to start the heat reclaim function:

1. Control mode is set to AUTO

2. DI external heat request is “Active”: “Hr enable” ON.

3. AI external heat request is “Active”:  “Consumer request” is higher than “HR start limit”. The check  is engaged when Heat reclaim type is “Max heat reclaim”, otherwise “Unconfigured” is shown

4. Internal thermostat request is “Active”. Thermostat sensor is below reference minus half of the band. The check  is only engaged  when Heat reclaim type is “No HP offset” or “HP offset”, otherwise “Unconfigured” is shown.

5. All safety checks are OK, specifically:

- 5.1. Anti Boiling is OK:  No risk of boiling is detected

- 5.2. Anti Boiling sensor error is OK:  No sensor error for all the sensors used for antiboiling

- 5.3. Flow Check is OK: Flow switch report “Flow OK” (if configured)

- 5.4. Sd error check is OK: No sensor error on “Sd MT”

- 5.6. MT Compressor stable running is OK: At least one MT compressor must have been running for at least 10 sec

- 5.7. Shr2 error check is OK:  No sensor error on Shr2

- 5.8. Shr2 check is OK: Shr2 is higher than "S2 check limit"

- 5.9. Shr3 error check is OK: No sensor error on Shr3

- 5.10. Shr1 and Shr3 check is OK: Shr1 is higher than Shr3 brine temp. Shr1 is “Sd MT” or “Stw2” (if tap water reclaim is active)

   - If “Control signal” = “Shr8” or “Shr4”, then “Shr1" must be higher than (Shr3 +1K)

   - If “Control signal” = “Shr4 – Shr3”, then “Shr1 must be higher than (Shr3 + Delta T)

- 5.11. Receiver safety is OK: No low Prec pressure (check “Actions on low receiver pressure” in Receiver control)

When all conditions are fulfilled, the following start sequence will be carried out:

1. The pump will be started (if not already running)

2. The by-pass valve will switch position and the discharge gas will be looped through the heat exchanger.

3. DO “Hr Heat delivered” is activated.

##### **Stop conditions**

The heat recovery will be stopped at one of the following conditions:

1. Control mode is set to OFF

2. DI external heat request is “None”: Hr enable OFF.

3. Internal Thermostat request is “None”: Thermostat sensor is above reference plus half of the band. The check is only engaged when Heat reclaim type is “No HP offset” or “HP offset”, otherwise “Unconfigured” is shown

4. AI external heat request is “None”: “Consumer request” signal goes below “HR stop limit”. The check is engaged when Heat reclaim type is “Max heat reclaim”, otherwise “Unconfigured” is shown

5. One of the following safety check fails:

- 5.1. Anti Boiling check fails:  Risk of boiling is detected and Anti-boiling safety is active

- 5.2. Anti Boiling sensor error check fails:  Sensor error for any of sensor used for antiboiling

- 5.3. Flow check fails: The flow switch reports“Flow Error”,  if configured

- 5.4. Sd error check fails: Sensor error on “Sd MT”

- 5.5 Shr1 error check fails: sensor error on virtual sensor Shr1. Shr1 selection depends by configuration; Shr1 is “Stw2 “ sensor (if tap water reclaim is active), otherwise is “Sd MT” sensor.

- 5.6. MT Compressor stable running fails: All MT compressors stopped. When heat reclaim type is “Max heat reclaim”, the stop condition requires that all MT compressors stopped for longer than "HR end delay – MT stop"

- 5.7. Receiver safety fails: Prec is too low (check “Actions on low receiver pressure” in Receiver control)

When one of the stop conditions is active, the following stop sequence will be initiated:

   1. The three way valve V3hr will switch position and bypass the gas.

   2. DO “Hr Heat delivered” is OFF.

   3. A shut down stage gets activated. The pump will continue to run 180 sec in order to remove the excessive heat in the heat exchanger. If a new heat request arises within the 180 sec, the pump will keep running.

- 5.5. Shr1 error check is OK: No sensor error on virtual sensor Shr1. Shr1 selection depends by configuration; Shr1 is “Stw2 “ sensor (if tap water reclaim is active),  otherwise is “Sd MT” sensor.

##### **Pause conditions**

When a stop condition is reached a shutdown stage is triggered and it can take minutes before heat recovery is available again.

To prevent that, V3tw valve will by-pass heat exchanger without activating a shutdown cycle after a pause condition is triggered then the following sequence will be initiated instead:

1. The three way valve V3tw will switch position and bypass the gas. The valve will change position without delay as soon all safety checks are OK

2. DO “Tw Heat delivered” is OFF.

3. The pump will continue to run and control normally.

Pause conditions are listed below:

1. MT Compressor stable running fails: MT compressor has stopped for less than "HR end delay – MT stop" (behavior available only with Heat reclaim type is “Max heat reclaim”)

2. Shr2 error check fails:  Sensor error on Shr2

3. Shr2 check fails: Shr2 is lower than "S2 check limit"

4. Shr3 error check fails: Sensor error on Shr3 (when Shr4-Shr3 is not selected as control signal)

5. Shr1 and Shr3 check fails: Shr1 is not high enought compared to Shr3 brine temp. Shr1 is “Sd MT” or Stw2 (if tap water reclaim is active)

- If “Control signal” = “Shr8” or “Shr4”, then “Sd MT" must be higher than (Shr3 +1K)

If “Control signal” = “Shr4 – Shr3”, then “Sd MT” must be higher than (Shr3 + Delta T)

### **5.7.3 Heat recovery - Circuit for Danfoss Heat Recovery Unit**

*[Figurtekst: Heat Recovery Unit · FShr 60 °C · Pump hr · Shr4 Shr3 · CTR M M · Shr2 · M V3hr V3gc Sgc · Sc3 · ICMTS · Sgc · Vhp Shp]*

*[Figurtekst: 2/3 1/3 · Sgc ref 100% · offset · 0% · Pgc ref Max · offset · Min · V3hr · Gas C. bypass · (V3gc bypass · limit) · 20% 25% 70% 80% 95% · HR request · 0%  HR stop limit 70% Ref offset high limit · 20%  HR start limit 80%  V3gc bypass stop limit · 25% Ref offset low limit 90%  V3gc bypass start limit]*

##### **Increasing the condensing pressure and temperature**

This regulation makes it possible to configure heat recovery compatibly with Danfoss Heat Recovery Unit (HRU), in a similar configuration as in “Max heat reclaim mode” for “Heat reclaim” circuit . AK-PC 782A will not control the water pump, such component is integrated in the HRU dedicated controller.

Before the pack controller starts the HRU, it checks the conditions of the Shr4 and Sd MT. How much the pressure and the temperature shall be increased is determined using an analog voltage signal. The signal must be a 0 – 10 V signal coming from the HRU controller.

The pack reacts to the HRU request and accordingly, it has an impact on the by-pass valve of the heat recovery (V3hr), Pressure and temperature increase, and gas cooler bypass valve (V3gc). As illustrated in the above picture.

This means that the regulation is based on external heat request (Consumer request) on an analog input as a percentage of voltage from 0 – 10 V. The Digital input to the pack controller is still needed as it is considered a start signal and it indicates the pump is running in the Danfoss Heat Recovery Unit.

1. The signal should be above 20% to start bypassing the gas into the heat exchanger (using V3hr), then the reference for the pressure Pgc is increased to "Pgc HR min.

2. The external voltage signal is registered (the higher the value, the greater the need for heat). The signal is converted by the controller to 0 – 100% capacity and will have the following impact:

##### **Valve - V3hr**

When heating of the circuit is required, the gas valve will change over and route the gas in through the heat exchanger. This is based on an external heat request.

- a. ON/OFF by-pass valve V3hr

##### **Flow switch - FShr**

- When the pump is released to start in the new Danfoss HRU, and the request signal reaches the “HR start limit”, the bypass valve V3hr opens for the heat recovery. The valve V3hr goes into "bypass" when the "HR stop limit" is reached.

A flow switch could be installed for safety reasons. The pack controller will then disconnect the entire recovery circuit.

##### **Sensors - Shr2, Shr3, Shr4, Sd**

- b. Pressure and temperature increase

All sensors must be installed due to safety reasons: Shr2: The controller must know the temperature of the gas that is sent for condensation Shr3: Heat exchanger cold access Shr4: Heat exchanger hot outlet Sd: The controller must know the temperature of the gas that is sent into the heat exchanger.

- The pressure is measured with the pressure transmitter Pgc and controlled with the High pressure valve Vhp. Based on the Heat request, the pressure reference “Pgc ref” will be raised from “Pgc HR min” to “Pgc HR Max”. If the "Extra refrigeration capacity function ("extra compressors") is activated, “Pgc ref” may exceed “Pgc HR max”. Once “Pgc ref” reaches “Pgc HR max” the gas cooler temperature setpoint “Sgc ref” is increased up to “Sgc HR Max”. Raising the gas cooler temperature reference results first in a reduction of fan speed and then in the activation of modulating V3gc (if configured). The parameter “Sgc HR Max” is calculated by the controller based on the setting "Pgc HR max".

##### **Consumer request:**

Only one signal can be received from an external heat consumer. The controller uses this signal after filtering it over a period, the filter is adjusted by the “Heat consumer filter”. To activate the Heat recovery unit and let the V3hr route the gas into the heat exchanger, it then should react to the consumer request. The signal coming from the integrated HRU controller is between 0 and 10 volts which will be used to start the heat recovery unit. If the signal is below 20% then the pack doesn’t start the HRU. If the signal is above 20%, then the pack starts and V3hr bypasses. Another signal on the digital input DI is received (mandatory, to enable the function). This DI signal indicates the pump is running. The Heat recovery unit is a simple version as the pump control is excluded from the pack controller and it is handled in the Danfoss heat recovery unit.

- c1. V3gc is modulating: The controller controls the fans and the valve, to maintain energy-optimized control (bypassing of the gas cooler will only be allowed when the fans are at 0% and vice versa). Shp is the control sensor when the gas cooler is bypassed.

- c2. V3gc is set to an on/off valve (see illustration): the fans will be stopped and the valve V3gc routes the gas outside the gas cooler. If the HR request is between V3gc bypass stop

limit & V3gc bypass start limit, the V3gc won't bypass unless Shr2 & Sgc are lower than "TC max HR".

The “Heat recovery status” picture shows the current regulation status.

exceeds 9.5 V for more than 10 min. The relay will be cut out when the signal is lower than 9.3 V. The relay is defined in the function: "Additional heat output", and can be used to start e.g. a heat pump evaporator.

##### **Relay output (additional heat output)**

A rela y can be reserved that will p ull in if the received si g nal

##### **Start and Stop conditions**

The purpose of the heat recovery functionality is to recover heat when  requested guaranteeing the safety of the refrigeration system and the hydraulic loops. This section describes start and stop conditions for heat reclaim circuit and the overview page “Heat reclaim status” using Danfoss Heat Recovery Unit. In the “Heat reclaim status” page, the controller monitors heat recovery requests (Active or None) and the fulfilment of the safety checks (OK or Failure). In cases the safety check or the request is not applicable, "Unconfigured" is shown.

|Actuator states<br>Request status<br>Hr status|
|---|
|Safety checks|
|Timer checks|

- 4.11. Receiver safety is OK: No low Prec pressure (check “Actions on low receiver pressure” in Receiver control)

When all conditions are fulfilled, the following start sequence will be carried out:

1. Hr Status shows “Start”, waiting for starting-up timer to expired

2. The by-pass valve will switch position and the discharge gas will be looped through the heat exchanger.

3. Hr Status shows “Heat reclaim”

4. DO “Hr Heat delivered” is activated.

##### **Stop conditions**

The heat recovery will be stopped at one of the following conditions:

1. Control mode is set to OFF (Hr status shows “OFF”)

2. DI external heat request is “None”: Hr enable OFF.

3. AI external heat request is “None”: Consumer request signal goes below 20%.

4. One of the following safety check fails:

   - 4.1. Anti Boiling check Fails:  Risk of boiling is detected and Antiboiling safety is active (Shr3 & Shr4)

   - 4.2. Anti Boiling sensor error check fails:  Sensor error for any of sensor used for antiboiling  (Shr3 & Shr4)

   - 4.3. Flow Check fails: The flow switch (if configured) has detected no flow for more than 180 s and it reports“Flow Error”

   - 4.4. Sd error check fails: Sensor error on “Sd MT”

   - 4.5. MT Compressor stable running fails: All MT compressors stopped for longer than "HR end delay – MT stop"

   - 4.6. Receiver safety fails: Prec is too low (check “Actions on low receiver pressure” in Receiver control)

When one of the stop conditions is active, the following stop sequence will be initiated:

1. The three way valve V3hr will switch position and bypass the gas.

2. DO “Hr Heat delivered” is OFF.

##### **Start conditions**

The following conditions must be fulfilled on order to start the heat reclaim function:

1. Control mode is set to AUTO

2. DI external Heat request is “Active”: Hr enable ON.

3. AI external Heat request is “Active”: Consumer request is above 20%

4. All safety checks are OK, specifically:

   - 4.1. Anti Boiling is OK: No risk of boiling is detected (Shr3 & Shr4)

   - 4.2. Anti Boiling sensor error is OK: No sensor error for all the sensors used for antiboiling (Shr3 & Shr4)

   - 4.3. Flow Check is OK: Flow switch report “Flow OK” (if configured)

   - 4.4. Sd error check is OK: No sensor error on “Sd MT”

   - 4.5. Shr1 error check is OK: No sensor error on virtual sensor Shr1. Shr1 selection is always “Sd MT” for HRU;

   - 4.6. MT Compressor stable running is OK: At least one MT compressor must have been running for at least 10 sec

   - 4.7. Shr2 error check is OK: No sensor error on Shr2

   - 4.8. Shr2 check is OK: Shr2 is higher than "S2 check limit"

   - 4.9. Shr3 error check is OK: No sensor error on Shr3

   - 4.10. Shr1 and Shr3 check is OK: “Sd MT” is higher than Shr3 brine temp +1K

3. Hr Status shows “Shutdown”, waiting for shutdown timer to expired (180 sec)

4. Then, Hr status shows “Idle”, that means the system is ready to reactivate heat recovery function if needed. This happens when condition 2 or 3 fail but  condition 1 and all safety checks (conditions 4) are okay.

##### **Pause conditions**

When a stop condition is reached a shutdown stage is triggered and it can take minutes before heat recovery is available again. To prevent that, V3hr valve will by-pass heat exchanger without activating a shutdown cycle after a pause condition is triggered then the following sequence will be initiated instead:

1. The three way valve V3hr will switch position and bypass the gas. The valve will change position without delay as soon all safety checks are OK

2. DO “Hr Heat delivered” is deactivated.

Pause conditions are listed below:

1. MT Compressor stable running fails: MT compressor has stopped for less than "HR end delay – MT stop"

2. Shr2 error check fails:  Sensor error on Shr2

3. Shr2 check fails: Shr2 is lower than "S2 check limit"

4. Shr3 error check fails: Sensor error on Shr3 (when Shr3 is not a control signal)

5. Shr1 and Shr3 check fails:“Sd MT" must be higher than Shr3 +1K

### **5.7.4 Heat recovery - Circuit for direct heat reclaim**

Direct Heat Reclaim is specifically designed for direct heat rejection into HVAC system, useful for cold regions. The heat circuit is not intended to be used for water or other fluids with the risk of boiling.

**Heat exchanger valve -** V3hr

This valve can be a modulating 3-way valve if the valve is used for temperature or pressure control, otherwise an On/Off 3-way valve can be used. When heating of the circuit is required, the gas valve will change over and route the gas in through the heat exchanger.

##### **Secondary fluid valve -** V3sf

The secondary fluid valve (V3sf) controls the recirculation of the secondary fluid (e.g., air) within a secondary loop. V3sf may consist of a single valve or multiple valves operating in coordination by the same control signal.

At fully open position, full recirculation of the secondary fluid with no addition of new fluid is held.

At fully closed position, complete integration of new fluid, with no recirculation of the existing fluid is maintained.

##### **Recirculator Fan**

A recirculator fan must be installed on the secondary fluid loop to make the flow. The recirculator can be either activated by the controller or can be configured to be controlled externally.

##### **Flow switch -** FShr

A Flow switch can be installed for safety reasons, in case of flow fault. The controller will then disconnect the entire heat recovery circuit.

##### **Sensors**

Shr2: The controller must know the temperature of the gas that is sent for condensation.

Shr8: The return air temperature.

Shr4: The supply air temperature, at the heat exchanger outlet. To ensure protection against overheating, it is strongly recommended to install the Shr4 sensor immediately downstream of the heat exchanger coil, at the highest point. Phr1/Pc: The inlet refrigerant pressure. At least one of the sensors, Phr1 or Pc must be installed when the Delta P control is configured by the user.

Phr2/Pgc: The outlet refrigerant pressure. At least one of the sensors, Phr2 or Pgc must be installed when the Delta P control is configured by the user.

##### **Flexible configuration**

The configuration is built around flexible, user-selectable features that can be enabled by the user as needed:

1. Start signal

2.   HP offset signal

3.   Gas cooler bypass signal

4.   DO for recirculator

5.   Temperature control

6.   Delta P control

Some of the features require to configure analog input (heat consumer request). The signal must be a 0 – 10 V signal or a 0 – 5 V signal. Up to 5 signals can be received from external regulations. The controller will use the signal that requests the largest heat consumption. The signal employed is filtered over a period. The length of the period can be set.

If signals are received from diferent controls, e.g. heat recovery for one of the inputs, a galvanically insulated module should be inserted.

##### **1. Start signal**

The Start signal defines the conditions required to activate and deactivate heat recovery. Depending on the selected configuration, heat demand is determined by either a digital request alone or a digital enable signal combined with an analog heat-consumer request.

The following configurations are available:

- **Only Digital Input:** Heat recovery is enabled by an active DI and disabled when the DI becomes inactive.

- **HC Analog + Digital:** Heat recovery is enabled when the DI is active and the heat-consumer request exceeds “HR start limit”. It is disabled when the DI becomes inactive or the heat-consumer request falls below “HR stop limit”.

*[Figurtekst: Hr Start · signal · 5% 10% 25% 70% 80% 95% · Heat consumer request · 5%  HR stop limit · 10%  HR start limit]*

##### **2. HP offset signal**

The HP offset feature allows the plant to operate at higher gas cooler pressure and gas cooler outlet temperature references during heat recovery, increasing the heat available for recovery. How much the pressure and the temperature shall be increased by is based on “HC Analog Input” (heat consumer request). When heat recovery is activated, the gas cooler pressure reference (Pgc ref), is increased to “Pgc HR min”.

Gas cooler references (PgcRef, SgcRef) are increased when heat consumer request is within ”Ref offset low limit” and ”Ref offset high limit” in the following order:

1. From ”Ref offset low limit” to 2/3 of the offset range (default 25%-55%), Pgc ref starts to increase from “Pgc HR min” to “Pgc HR max”.

2. When heat consumer signal is above 2/3 of the offset range, Sgc ref is increased from “Sgc min” to reach “Sgc max” when the heat consumer signal is at “Ref offset high limit”.

*[Figurtekst: 2/3 1/3 · Sgc ref 100% · offset · 0% · Pgc ref Max · offset · Min · 5% 10% 25% 70% 80% 95% · Heat consumer request · 25% Ref offset low 70% Ref offset high]*

##### **3. Gas cooler bypass signal**

When Gc Bypass signal is configured by the user, “HC Analog Input” (heat consumer request) will be used to bypass the gas cooler using V3gc.

This feature can only be configured when V3gc is set to an on/off valve.

V3gc will bypass gas cooler, when the heat recovery is activated and the HC request is above “V3gc bypass start limit” and Shr2 & Sgc are lower than "V3gc bypass stop T".

V3gc will route the gas to the gas cooler if Heat recovery is not active, Shr2 or Sgc are above "V3gc bypass stop T" or HC request is below “V3gc bypass stop limit”.

Nonetheless, V3gc will not be bypassed again before the valve has routed the gas to the gas cooler for at least the user-defined duration of “V3gc bypass min off time”.

*[Figurtekst: Gas C. · bypass · 5% 10% 25% 70% 80% 95% · Heat consumer request · 80%  V3gc bypass stop limit · 95%  V3gc bypass start limit]*

##### **4. DO for recirculator**

A digital signal from controller can be configured to be used directly to turn the recirculator ON or OFF. The signal guarantee that circulation of secondary fluids happens during heat recovery and for 180 s after is stopped.

##### **5.  Temperature control**

Temperature control regulates heat delivery during heat recovery operation. While the “Start signal” determines when heat recovery is enabled or disabled, temperature control adjusts the system to maintain the target temperature.

One of the following options for temperature control in heat recovery should be configured in Direct heat reclaim

1. External temperature control

2. Shr8 temperature control using V3hr valve

3. Shr4 temperature control using V3sf valve

##### **External temperature Control**

When the temperature control is configured to “None (Extern AI)”, no temperature regulation will be performed by the controller. The responsibility of regulation is assumed to be handled externally. When heating of the circuit is required, V3hr valve will change over to the maximum allowable opening degree and route the gas through the heat exchanger. If heat recovery should stop, V3hr valve will be closed and route the gas to bypass the heat exchanger.

##### **Shr8 temperature control using V3hr valve**

To control the air temperature, PI regulation is done on return air temperature to reach “Setpoint T ctrl”. A temperature sensor Shr8 is installed in the return air inlet, and the temperature is regulated by controlling the delivered heat. The controller adjusts the opening degree of the V3hr valve in the following way: Opening of the valve corresponds to more hot gas flow through the gas heat exchanger (and thereby more heat to be delivered). Closing the V3hr results in bypassing the heat exchanger (less to no heat delivery).

##### **Shr4 temperature control using V3sf valve**

The user can configure control of Shr4 with V3sf valve to control the supply air temperature. A PI regulation is done on supply air temperature to reach “Setpoint T ctrl”, e.g., 30 **°** C. The controller adjusts the opening degree of the V3sf valve in the following way: Opening of V3sf causes bypass of the outside air and allows the Shr4 temperature to increase. Closing V3sf will route the air circulation to outside allowing Shr4 temperature to cool down.

##### **Shr4 check**

A maximum temperature limit can be applied to the supply air temperature outlet of the heat exchanger by enabling S4 check. In this case, the user can make sure that heat recovery will stop if Shr4 temperature is above a user-defined value “S4 check limit”. V3hr will bypass the refrigerant gas from the heat exchanger to prevent increasing the supply-air temperature above this limit to protect HVAC facilities from the damage by high-temperature air.

##### **6. Delta P control**

The user can configure Delta P control to regulate the gas pressure drop on the heat recovery heat exchanger via V3hr valve. This option is available if V3hr valve is not configured for temperature control. A PI regulation is done on the pressure difference (Delta P) between two pressure sensors to reach “DPhr setpoint”, e.g. 1 bar. In this case, Delta P is the pressure drop from the pressure before V3hr valve (P1) to the pressure after the heat recovery heat exchanger (P2).

P1 pressure can be chosen to be from the Pc pressure sensor or from another pressure sensor (Phr1) installed before V3hr valve. P2 pressure can be chosen to be from the Pgc pressure sensor or from another pressure sensor (Phr2) installed after heat exchanger gas outlet.

##### **Start and Stop conditions**

The purpose of the heat recovery functionality is to recover heat when requested guaranteeing the safety of the refrigeration system and the secondary loops. This section describes start and stop conditions for Direct heat reclaim circuit and the overview page “Direct heat reclaim status”.

The controller adjusts the opening degree of the V3hr valve in the following way: Consequently, Delta P is expected to increase when more gas flow is routed to the heat exchanger.

Opening of the valve corresponds to more hot gas flow through the gas heat exchanger and thereby more heat to be Closing the V3hr results in bypassing the heat exchanger (less to no heat delivery). In this case, DeltaP is expected to decrease, as the gas flow bypasses the heat exchanger.

##### **Remember sensor calibration**

Temperature dependency to sensor calibration can affect the performance of heat recovery if Delta P control is activated. It is highly recommended to calibrate the pressure sensors at the operating temperature range according to the manufacturer guidelines!

*[Figurtekst: H eat Recovery status · A ctuator states · R equest status · S afety checks · T imer checks]*

The start/stop conditions are intended for all applicable features. In the “Direct heat reclaim status” page, the controller monitors heat recovery requests (Active or None) and the fulfilment of the safety checks (OK or Failure). In cases the safety check or the request is not applicable, "Unconfigured" is shown.

##### **Start conditions**

The following conditions must be fulfilled on order to start the Direct heat reclaim function:

1. Control mode is set to AUTO

2. DI external Heat request is “Active”: Hr enable ON.

3. AI external heat request is “Active”: “Consumer request” is higher than “HR start limit” (If “Start signal” is chosen to be “HC Analog + Digital”)

4. Following safety checks are OK (all other safety checks not mentioned in this list are not applicable for Direct heat reclaim and “Unconfigured” is shown):

   - 4.1. Flow Check is OK: Flow switch report “Flow OK” for a duration of “Flowswitch delay” (if configured)

   - 4.2. MT Compressor stable running is OK: At least one MT compressor must have been running for at least 10 sec

   - 4.3. Temp.ctrl sensor error is OK: No sensor error on the controlled temperature sensor (if temperature control is configured)

   - 4.4. Receiver safety is OK: No low Prec pressure (check “Actions on low receiver pressure” in Receiver control)

   - 4.5. Shr4 error check is OK: No sensor error on Shr4 (if Shr4 is used as temperature control sensor or if “S4 Check” safety is enabled)

   - 4.6. Shr4 check is OK: Shr4 is not above “S4 check limit” (if “S4 Check” is enabled)

   - 4.7. Delta P error is OK: No sensor error on any of the pressure sensors used for Delta pressure control (If Delta pressure control is configured)

When all conditions are fulfilled, the following start sequence will be carried out:

1. The DO “Hr recirculator” will be ON (if configured)

2. Hr Status shows “Start”, waiting for startup timer to expire

3. The three-way valve V3hr will switch position, and the gas will be looped through the heat exchanger

4. DO “Hr Heat delivered” is activated and Hr Status shows “Heat reclaim”

5. Regulations of temperature or pressure will start control of the actuator(s) (if configured)

##### **Stop conditions**

The heat recovery will be stopped at one of the following conditions:

1. Control mode is set to OFF

2. DI external heat request is “None”: “Hr enable” OFF.

3. AI external heat request is “None”: “Consumer request” signal goes below “HR stop limit” (If “Start signal” is chosen to be “HC Analog + Digital”)

4. One of the following safety checks fails:

   - 4.1. Flow check fails: The flow switch reports “Flow Error” for a duration of “Flowswitch delay” (if configured)

   - 4.2. MT Compressor stable running fails: All MT compressors stopped for longer than "HR end delay – MT stop"

- 4.3. Temp.Ctrl sensor error fails: Sensor error on the controlled temperature sensor (if temperature control is using Shr4 or Shr8)

- 4.4. Receiver safety fails: Prec is too low (check “Actions on low receiver pressure” in Receiver control)

- 4.5. Shr4 error check fails: Sensor error on Shr4 (if Shr4 is used as temperature control sensor or if “S4 Check” safety is enabled)

- 4.6. Shr4 check fails: Shr4 is above “S4 check limit” (if “S4 Check” is enabled)

- 4.7. Delta P error fails: Sensor error on any of the pressure sensors used for Delta pressure control (If Delta pressure control is configured)

When one of the stop conditions is active, the following stop sequence will be initiated:

1. The three-way valve V3hr will switch position and bypass the heat exchanger.

2. DO “Hr Heat delivered” is OFF.

3. The three-way valve V3sf will switch position and route the air circulation to outside to allow cooling down the supply air temperature.

4. A shut down stage gets activated. The DO “Hr recirculator” will be ON for 180 sec in order to distribute the excessive heat in the heat exchanger. If after 180 seconds, either one of the stop conditions 4.1 or 4.6 are still failing, the DO “Hr recirculator” will remain ON until the failure(s) are resolved.

5. DO “Hr recirculator” will be OFF unless new heat request is raised.

##### **Pause conditions**

When a stop condition is reached, a shutdown stage is triggered, and it can take minutes before heat recovery is available again. To prevent that, V3hr valve will bypass heat exchanger without activating a shutdown cycle after a pause condition is triggered, then the following sequence will be initiated insted:

1. The three-way valve V3hr will switch position and bypass the Heat exchanger. The valve will change position without delay as soon as all following safety checks are OK.

2. The three-way valve V3sf will switch position and route the air circulation to outside to allow cooling down the supply air temperature.

3. Hr Status shows “Paused”.

4. DO “Hr Heat delivered” is OFF.

5. The DO “Hr recirculator” will be ON.

Pause conditions are listed below:

1. MT Compressor stable running fails: MT compressor has stopped for less than "HR end delay – MT stop"

2.  Temp.ctrl check fails: The controlled temperature is higher than the setpoint for some time (if temperature control is configured to control the V3hr valve)

3.  Delta P check fails: Pressure difference on the refrigerant side of the heat exchanger is higher than the reference for some time (If Delta pressure control is configured)

4.  Flow switch timer is waiting: Flow switch was not stable for the configured “Flowswitch delay” period (if Flow switch is configured)

### **5.7.5 Circuits for control of CO2 gas pressure**

##### **Overview**

The controller regulates the pressure in the gas cooler (condenser) so that the system achieves the optimal COP. The controller will always optimise to a subcritical state.

The pressure in the gas cooler is controlled by the Vhp valve. Instead of an ICMTS valve, an ejector or a CCMT valve with stepper motor can be used.

Regulation must have inputs from both a pressure transmitter Pgc and a temperature sensor Sgc. Both must be fitted in the outlet immediately after the gas cooler. If the gas cooler can be bypassed, an Shp sensor **must** be installed. Should the Shp sensor record too high a temperature, the refrigerant will be passed through the gas cooler.

The opening degrees of the valves can be restricted with both a minimum and a maximum opening degree. The setting OD Min. can be adjusted as % of the opening degree and will restrict the voltage signal for the valve.

In applications with very low outdoor temperatures, the OD min. setting is used to prevent the accumulation of cold liquid in the gas cooler.

##### Reference curve

##### Maximum COP control

During normal operation without override, the controller will maintain the optimum pressure in the transcritical area.

The controller is pre-programmed to follow the optimal COP from the pressure/enthalpy chart. The top point is defined at 100 bar, 39 °C. (Optimal theoretical COP is achieved at the curve that passes through 100 bar and 39 °C. The point of intersection can be changed by setting a value other than the default). Regulation will now follow the set reference curve, but will never go above the set permitted max. pressure for the gas cooler. The current reference can be read from the controller's overview screen.

##### Sub-cooling

It is also possible to configure the sub-cooling in the sub-critical area.

##### Pgc reference

The Pgc reference is normally calculated based on the Maximum COP curve and the condenser reference (Sgc ref).

If the Sgc is significantly above reference, then the Pgc reference is raised and it is calculated based on the actual Sgc measurement.

It is possible to limit the maximum Sgc reference ("Sgc max reference" parameter). In this case, the Pgc will be calculated on the Sgc reference until it reaches the maximum value.

The Pgc reference can be increased due to heat recovery (see Circuit for recovery for heating).

The limits for Pgc reference are "Pgc Min" and "Pgc Max - Pgc max. limit Pband". The Pgc reference will always be kept inside these limits.

*[Figurtekst: P · Pgc,max · Pgc max. limit Pband · Pgc,min]*

##### **Forcing fan speed via DI**

When "Forcing fan speed via DI" is configured and DI active, gascooler temperature and pressure control operates without condenser reference (Sgc reference). Pgc reference is calculated based on Sgc measurement instead of condenser reference (Sgc reference). When the DI state is OFF, the calculation returns using Sgc reference.

##### **Receiver inlet minimum vapour**

It is possible to limit how low the vapour quality entering the receiver (i.e. the minimum vapour fraction) may be. This will limit the Pgc ref and Sgc references, avoiding operating conditions that provide a lower quality.

The parameter is configurable in the Receiver control config. pages.

##### **Extra refrigeration capacity (“extra compressor”)**

This function increases the system’s refrigeration capacity by raising the pressure in the gas cooler in accordance with "Extra capacity offset" parameter. The function will start when the compressor capacity has been at 100% for 5 minutes. The cooling performance increases to Q0+dh0.

The function also increases the load on the compressor motor as pressure increases. Power consumption increases to Qm+dQm.

##### **Bypass of gas cooler at a very low temperature**

It will be necessary to route the gas outside of the gas cooler if the gas temperature is too low.

Temperature limits are set under the function **"Bypass low limit - Shp".** When the function is active, the gas temperature is measured by the Shp sensor. When the sensor records a value that is 5K higher than the set value, it will switch back again so that the gas is routed through the gas cooler.

In general, the temperature is regulated first by fan control, and the fans stop when the temperature gets too low. The valve then takes over to keep the temperature above the desired temperature.

With modulating by-pass valve, the OD min. and OD max. settings can be set as percentage open and define the valve’s range of operation.

OD min. will ensure a minimum flow in the by-pass pipe.

##### **At on/off by-pass valve**

If the controller has had the gas cooler bypassed due to heat recovery, then a timer function will start when the system switches over once again to gas cooler operation. The timer function will keep the regulation in gas cooler mode for **"Bypass min off time"** , until a bypass is permitted again.

Remember that the controller controls the gas pressure. If the regulation is stopped by the internal or external main switch, this control will stop as well.

If the compressors are stopped via the function "External compressor stop", control of the gas pressure will continue.

### **5.7.6 Ejector control**

The ejector effect is achieved when the motive mass flow from the gas cooler is pushed through a jet tube and then subsequently drives the gas / liquid from the MT part into a mixing chamber. The mixture is released to the receiver.

*[Figurtekst: High pressure lift application]*

##### **Multi Ejector**

The Multi Ejector is available in several versions where jet tube, suction pipe and mixing chamber is optimized to: **"High pressure lift"** (HP) — an ejector that can lift a less mass flow, but higher pressure lift.

**"Low Pressure lift"** (LP) — an ejector that can lift more mass flow, but lower pressure lift.

**"Liquid Ejector"** (LE) — an ejector designed to lift liquid at low pressure conditions in a gas cooler.

The ejectors are an integral part of the gas cooler pressure control strategy. The preferred ejector type is determined by the ejector envelopes. Depending on system layout there will be different priorities:

1. Preferred ejector type as long as a the preferred ejector capacity is available

2. Non-preferred ejector type

3. High pressure valve when there is no more ejector capacity available.

The ejector block consists of several fixed ejectors with different capacity sizes. The sizes are binary as for the four smallest and cyclic as for the largest. The ejectors are activated in a binary pattern to achieve the desired capacity.

- For "High pressure lift" (HP) they can, for example be:  125, 250, 500, 1000, 1000 and 1000) kg/h.

- For "liquid lift" they can, for example be: 200, 400 or 200+400 or 400+400 kg/h.

- The combi block can also be a combination of gas and liquid ejectors, using one or more liquid ejector valves.

##### Example

*[Figurtekst: Capacity · [kg/h]]*

*[Figurtekst: Cutin ejector · valve number]*

Shown here is the start of a "High pressure lift" control with four ejector valves. The total capacity can be controlled up to approx. 1875 kg/h.

If an HP ejector with 6 ejector valves is used, it can handle up to 3875 kg/h. Ejector step 4, 5 and 6 are the same size (1000 kg/h) and are operated in order to have the same number of cycles. The control strategy is the same for LP ejectors, but the mass flow capacities are approximately half of what they are for HP ejectors.

##### **Requirements**

The four smallest ejector valves, that are controlled on/off more frequently than the larger ejector valves, **must be controlled by the controller's solid state relays.** The mechanical relays will not be able to withstand this high number of couplings.

##### **Control**

The control is regulated by a signal from the pressure transmitter Pgc. The neutral zone is above the reference. The controller will switch ejectors when the pressure gets outside the neutral zone.

*[Figurtekst: Po-MT · MT evap.]*

HP ejector control is an extension of the control with parallel compression. In this case, a part of the mass flow gets a high lift from MT suction group to IT compressors.

##### **Low pressure lift - summer mode**

*[Figurtekst: Psuc-MT · Po-MT Vrec2 · Vrec1]*

LP ejector control has no parallel compression. Here the whole mass flow rate is raised from MT evaporators to receiver. The check valve prevents back flow to MT evaporators. LT compressors discharge to MT compressor's suction line after the check valve.

##### **Low pressure lift - winter mode**

*[Figurtekst: Psuc-MT · Po-MT Vrec2 · Vrec1]*

*[Figurtekst: Liquid lift · Po-MT · MT evap.]*

Ejectors move liquid from a suction accumulator to the receiver. In systems with LE and HP ejectors - depending on the ejector envelopes - either LE or HP ejectors will have priority to lift liquid. When liquid is not present, vapor will be lifted.

The control for HP and LP ejector systems are shown with the Vhp valve mounted in parallel with the ejectors. If ejector capacities are sufficient to manage the total gas cooler mass flow (up to 4 ejector blocks can be mounted in parallel), it is not necessary to have a Vhp valve. However, the controller will require that settings and output signal are present as if the valve was there.

In systems with adaptive liquid control (ALC), an accumulator must be mounted in the suction line. The ejectors will move liquid from the suction accumulator and over in the receiver. If the ejector cannot move enough liquid, the liquid level will rise. There is thus a risk of compressor breakdown. The controller must have a signal for liquid level in the suction accumulator. If the liquid level gets too high or if the ejectors are outside the application envelope, the controller can send a signal on the data communication and also activate a relay.

The evaporator controls must receive the signal on an excessively high liquid level, either via wiring or via data communication (if received via data communication, it is necessary for the system unit used to be able to convey this communication). When the evaporator controls receive this signal, they will change the superheating regulation from "liquid flow allowed" to dry expansion.

##### **Settings**

The setting is made under HP control page 2

##### **Readings from the overview display**

T he opening degree of the defined ejector valves.

##### **The type and size of the ejector**

The first 6 are gas ejectors for a high pressure lift. Following these are combinations of gas and liquid ejectors, which are mounted in the same block. A combined gas-liquid setting is only possible when the ejectors are mounted in the same block. If the unit has a separate block for liquid, the "gas block" must be selected as gas only. The "liquid block" must then be set separately, as in the subsequent image.

##### **Number of blocks**

If more than one block is selected, there will be a difference in how the electrical connection to an ejector is carried out. Gas: Here one output is reserved for each ejector valve in block 1. If there are more blocks, the subsequent blocks must be connected parallel to the first.

Liquid: Here one output is reserved for each ejector valve, regardless of the number of blocks and regardless of whether it is a combined gas/fluid block. Each fluid ejector valve has its own connection, i.e. there must be no parallel connection of fluid ejector valves.

##### **MC Ad. Liq. Ctrl**

The function is enabled if the evaporator controllers allow operation with "MC Ad. Liq. Ctrl". If enabled, AK-PC 782A must receive a level signal from the suction accumulator. The ejector control will then follow this signal and cancel "MC Ad. Liq. Ctrl" if the level in the suction accumulator becomes too high. The ejector regulation will also cancel "MC Ad. Liq. Ctrl" if pressure conditions around the ejector deviate from those expected. That is, if the ejectors cannot keep up with the movement of liquid.

##### **MC ALC via DO**

If enabled, then a relay output will be reserved.

The output will be activated when the ejector control can recommend operation with a "MC Ad. Liq. Ctrl" and deactivated if "MC Ad. Liq. Ctrl" must stop. When the evaporator controllers receive a "stop MC Ad. Liq. Ctrl" signal, they will change their superheating regulation to dry expansion. **MC ALC discard map**

MC Ad. Liq. Ctrl using only high level switch and timer.

##### **Ejector stop via DI**

If you want to use an external contact function that can stop the ejector function, it should be added here.

MC ALC status description: **Main Switch Off:** Main switch is off on the controller. **High Level:** The level in the suction accumulator is too High. **No lift:** No ejectors are being operated inside their application envelope. **No Ej.Cap:** Ejectors are off and can therefore not provide enough flow. **Timer:** The controller is decreasing the Liquid level in the suction accumulator before MC ALC control is permitted. **Permitted:** The Timer has expired and the ejectors can handle active ALC. This timer shows the remaining time, before the MC ALC control is released again after it was stopped, e.g. due to no ej. cap signal, “the ejectors are outside their application envelope” or because the “Liquid level” switch has detected a full separator. An ejector valve should not disconnect more than once every minute over an average of 24 hours. If the change is more frequent, the control parameters Pgc neutral zone, Kp and Tn should be changed. The values in fields are total values since the last reset.

##### **Recommended connections**

*[Figurtekst: 4 steps · Ejector HP · kg/h · 1 125 · 2 250 · 3 500 · 4 1000 · 5 1000 · 6 1000 · Coil = 6 W · 6 steps, 3875 kg/h · Coil = 6 W · When ejectors of the same size have to be coupled, the · one with the lowest number of cycles will cut in first. · This is followed by the next shortest, and then by the · third. · 6 steps, 7750 kg/h · Coil = 6 W · NB · Up to four ejectors of equal size may be · connected in parallel to the same solid state · relay. Liquid ejectors are not connected · parallel. Each liquid ejector has its own outlet. · Alarm text · Settings Priority  English alarm texts Description · (factory) · Ejector · - · High Ejector Emergency No signal from Pgc. The opening degree of the ejector valves are forcefully · controlled to an average registered opening degree. · - · High Manual Ejector control The ejector control has been stopped manually]*

### **5.7.7 Receiver control**

*[Figurtekst: External T · Delta P · Set reference is maintained as low as possible, keeping a delta P · above MT pressure reference. Delta P is set in “Delta P reference”. · Prec ref · DeltaP reference · PoMT ref · Time · With ej · Without ej · Prec ref · Pressure]*

The receiver pressure can be controlled so that it is kept at the requested reference point. To do so, the receiver control coordinates the actions of the following actuators, if configured:

- Receiver valve Vrec

- IT compressor group (optional)

- Hot gas dump (optional)

- Additional valve Vrec (optional), operated simultaneously or in sequence with the previous one.

A pressure transmitter needs to be installed in the receiver.

##### **Receiver Reference**

Pressure can be regulated in one of the following modes, depending on the method used to calculate receiver reference, set in “Prec ref. Mode”:

##### **Fixed SP**

In every mode, the reference is limited between “Prec min reference” and “Prec max reference”.

The receiver control operates on a fixed set point defined by the user.

In all modes, except “Delta P” mode, when selecting the option “Enable Delta P min” it is possible to maintain the reference value higher than PoMT + “Delta P reference”. Further limitation can optionally be applied when air conditioning support is enabled. (See the air conditioning section for more details.)

*[Figurtekst: Prec setpoint · Time · Ext. Offset · This has the same reference as a fixed set point, but it can be offset · with an analogue input up to the max. value “Ext. Offset max”. · Ext offset max · Prec setpoint · 10 V · 0 V · Time · Prec reference · Prec ref · Ext off]*

In assisted or automatic mode, the SetPoint Manager may change receiver reference (see the SetPoint Manager section in this user guide).

The Vrec valve and the IT group share the same reference. The control strategy decides the best actuator in the current running conditions and controller state.

##### **Vrec Valve**

Receiver valve regulation is based on a PI algorithm. The user can specify minimum and maximum opening degree for the actuator. To prevent releasing CO2 from the suction line, the valve is fully closed (overwriting OD min) when all MT compressors are not available, e.g. when all MT compressors in alarm.

When the IT compressor group is in control, the valve is used as secondary actuator, operating on a higher (+4 bar) reference. Below such reference, the valve is kept closed if already closed. Above, it is controlled by means of a regular PI algorithm.

##### **IT Optimize**

Receiver pressure is optimized to maximize COP. The optimal reference is calculated considering IT compressors or ejectors if installed.

When Sgc is between 15 – 20 °C, the receiver reference is reduced to 2 bar above the MT reference.

##### **Hot gas dump**

In very cold climate, the receiver pressure risks to systematically get too close to MT circuit. The difference in the evaporators might then not be enough to guarantee cooling.

To prevent to reach such a condition, a hot gas dump valve can be installed, connecting the discharge pipe of the compressors with the receiver. In order to quickly recover pressure in the receiver, the controller will turn on the hot gas to the receiver if the pressure becomes lower than the “Cut-in”. The hot gas will shut off again when the pressure exceeds the “Cut-out”.

*[Figurtekst: HGD · ON · State · OFF · Cut-in Cut-out Prec]*

##### **IT Compressor group (parallel compressors)**

The parallel compression (intermediate temperature, ‘IT’) is controlled by the IT suction group that executes the request coming from receiver control. For more details check the section “Parallel compression”.

##### **Emergency Capacity**

When receiver pressure sensor error occurs, the receiver control coordinates the actuators in the following way:

- Vrec is set to emergency OD, scaled proportionally with Sgc sensor and MT running capacity

- IT is set to emergency capacity, scaled proportionally with MT running capacity

- Hot gas dump is closed

During normal operating conditions, the controller stores the average actuator position for Vrec (last 24 h) and IT (last 1 h), taking into account the current running plant conditions.

The average for Vrec is calculated considering only the periods when Vrec is controlling the receiver reference (i.e. it is the primary actuator).

It is possible to set limits for the Prec reference to be used when AC is released (parameter “AC Prec limits”): the reference for the receiver pressure will be kept inside the user-set limits (“AC Prec min/max ref”). When the signal is stopped once again, the restriction of the receiver references will not be applied anymore.

*[Figurtekst: DI DO · External · AC request · AC · controller AC release]*

### **5.7.8 Safety procedures**

In case of high or low receiver pressure, it is possible to configure safety actions inside two proportional bands.

*[Figurtekst: Prec max · Prec max Pband Hi · Prec max Pband · Prec max Pband Lo · Prec min Pband Hi · Prec min Pband · Prec min Pband Lo · Prec min]*

Below is the description of the actions.

##### **Actions on high receiver pressure**

Avoiding high receiver pressure is important for the safety of the system, but drastic actions compromise the functionality of other subsystems therefore AK-PC 782A provides different options:

|Cancelling AC|always active|
|---|---|
|Limiting Heat recovery|always active|
|Increasing fan capacity|always active|
|Decreasing MT capacity|optional, default on|
|Decreasing ejector and Vhp capacity|optional, default off|

##### **Air Conditioning**

It is possible to enable operation with air conditioning with the parameter “AC support”. When the function is enabled, the input signal “AC Request” and output signal “AC release” will be available in the I/O configuration.

When a signal from an external controller is received at the “AC request” input, the controller will release AC if the current conditions allow it.

“AC status” provides the information on AC release or the reason why it is not released:

- **Prec sensor error** : Receiver Pressure sensor error

- **Low Prec:** Prec below “AC Frost Protection” (2 °C, not configurable)

- **High Prec:** Prec above “AC Disable” (see details in "Safety Procedures")

- **High Po-MT** : PoMt above “To max Alarm” for MT

- **IT not available** : IT pack is not available in a plant with parallel compression (compressor in alarm)

- **Timer** : AC not released, waiting for the timer to expire

Actions on high receiver pressure is taken when the Prec measurement gets between Prec max Pband Lo and Prec max Pband Hi, this range is referred to as max P-band.

##### **AC Disable**

As soon as the receiver pressure enters the P-band, air conditioning will be deactivated. Once deactivated, it remains deactivated for a preset time.

##### **Limiting Heat recovery**

If Prec is in the max P-band, then the Sgc reference is not increased due to the heat recovery request.

##### **Decreasing MT capacity (optional):**

This is active when MT Cut-out on high Prec is enabled.

When the receiver pressure reaches 75% of the max. P-band, the MT will cut out 25% of current running capacity every 30 sec. There is a delay before the capacity is allowed to increase again.

- **Not Requested** : No AC Request

- **Active** : Air Conditioning is released

**Fan speed increase and Vhp, ejector decrease (optional)** This set of gas cooler actions depends on the user setting “Vhp close on high Prec” and if ejectors are installed.

Case 1: “Vhp close on high Prec” option is disabled: The minimum fan speed is gradually raised from 0 – 100% over the full P-band”.

*[Figurtekst: 100% · 0% · P-band Prec · Case 2: ”Vhp close on high Prec” option is enabled – no ejectors · installed: · In the lower half of the P-band, the minimum fan speed is raised · from 0 – 100%. · In the upper half, the maximum opening degree of the high- · pressure valve will be lowered from 100% to Min OD. · 100% · Min. OD · 0% 100% · P-band Prec · min · fan speed · max · Vhp OD · min · fan speed]*

Case 3: ”Vhp close on high Prec” option is enabled– with ejectors installed:

In the lower half of the max. P-band, the minimum fan speed is raised from 0 – 100%.

In the 50 – 75% of the max. P-band, the maximum opening degree of the high-pressure valve is lowered from 100% to Min OD. The minimum opening degree of the high-pressure valve still applies to ensure a reliable Sgc sensor reading.

In the 75 – 100% of the max. P-band, the ejectors are gradually closed.

*[Figurtekst: 100% · 0% · 100% · Min. OD · 100% · 0% · P-band Prec · max Ej OD · max · Vhp OD · min · fan speed]*

### **5.7.9 Actions on low receiver pressure**

Avoiding low receiver pressure is important for ensuring cooling and beside from using the receiver actuators for raising the receiver pressure, the heat recovery is disabled and the user can enable the option ”Vhp open on low Prec” in the config.: receiver control menu.

##### **Canceling heat recovery**

Heat recovery has lower priority than keeping the receiver pressure high enough. Therefore the controller disables the Heat recovery if Prec is lower than “HR disable”. After deactivation, the minimum deactivation time is 10 minutes.

##### **Pausing heat recovery (preventive action)**

Canceling heat recovery typically takes several minutes before it can be reactivated. As a preventive action, the system will pause heat recovery when the heat recovery outlet temperature Stw2/ Shr2 is below "S2 check limit" ("S2 check" safety condition failing).

"S2 check limit” is calculated based on the receiver reference values "HR Disable" and "Receiver inlet min. vapour". This method enables the controller to limit how cold the refrigerant becomes after heat recovery, in relation to the receiver’s current configuration.

##### **Cancelling AC for Frost Protection**

When the temperature level in the receiver is too low, the AC pipes might risk frost damage. To prevent this, air conditioning will be deactivated, when the receiver pressure is below “AC Frost Limit”. Once deactivated, it remains deactivated for a preset time. “AC Frost Limit” is the pressure corresponding to a saturated temperature of 2 °C.

##### **Vhp open on low Prec:**

When this feature is enabled, the minimum OD for Vhp is gradually increased from “Vhp min. OD” to “Vhp Max OD low Prec” as a P-band control when the receiver pressure decreases from “Prec min Pband Hi” to “Prec min Pband Lo”. After 5 min the last compressor stops, and the Vhp can close fully, disregarding any minimum OD.

*[Figurtekst: Low Prec · OD max · Min. OD · P-band Prec · max · Vhp OD]*

In case of operation in cold conditions: If Shp is colder than the saturated temperature of “Prec min Pband hi”, the function is disabled. It is assumed that low Sgc is the problem and not a low charge condition.

*[Figurtekst: Lower PoMT,ref on low Prec · The setpoint management will maintain a difference of at least 3 · bar between the MT and receiver references. · Prec,ref · It is possible that the controller cannot hold the Prec at its setpoint. · This can for example happen when the outdoor temperature is · very low and the load is low. If necessary, the Po ref for the MT will · be lowered to 3 bar below the measured Prec. · Prec (measured) · Min. · 3 bar · Min. · 3 bar · PoMT,ref · Lower PoMT,ref on low Prec · The setpoint management will maintain a difference of at least 3 · bar between the MT and receiver references. · Prec,ref · It is possible that the controller cannot hold the Prec at its setpoint. · This can for example happen when the outdoor temperature is · very low and the load is low. If necessary, the Po ref for the MT will · Prec (measured) · be lowered to 3 bar below the measured Prec. · It is possible to disable this function changing the parameter  Min. · "Lower Po on low Prec" to "No" just if also the parameter called  3 bar · "Setpoint management" (in Config. : Select plant type) is set to  Min.3 bar · "Manual". · If the parameter called "Setpoint management" is set to "Assisted", · then the parameter "Lower Po on low Prec" is automatically · converted to "Yes"and other selections are not permitted PoMT,ref]*

### **5.7.10 Parallel Compression**

On transcritical systems installed in slightly warmer surroundings, the COP will be significantly improved by using parallel compression. One or more compressors are used to help maintain the receiver pressure during warm periods when the outdoor temperature becomes high — primarily during the summer. The parallel compression (intermediate temperature, ‘IT’) is controlled by the IT suction group.

It receives the request from the receiver control starting the compressor as needed, so that the receiver pressure is kept at the desired level.

On the page about “Cap. ctrl status IT” it is possible to see the “IT-Comp. Request”, i.e. the current requested regulation by the receiver control algorithm. Below is the list of possible values:

- Free running: control pressure as regular suction group

- Force Start: control pressure, but the start is forced above minus zone

- No cap change: capacity is kept locked to current capacity

- Full Stop: compressors are force-stopped

- Rcv. Emergency: apply the calculated emergency request capacity during Prec sensor error

The IT suction group might not be in the condition to execute the receiver request, e.g. as result of compressors in alarms. In that case receiver control will use Vrec as primary actuator.

##### **Requirements to allow IT**

Receiver control will avoid operating with parallel compression in conditions that might be inefficient for the plant or dangerous for the compressors.

Below are the conditions that must be true before starting the IT compressor:

*[Figurtekst: Internal Heat Exchanger · Sgc / Shp · Hot Gas Dump · IT Compr. group · P Prec Vrec valve · Pgc · Vhp · Prec · Vrec · PMT · IT · MT]*

- Sgc reference higher than "IT Comp. Sgc Min".

- Shp sensor higher than "IT Comp. Sgc Min". In case of Shp sensor error or if Shp is not configured, Shp is used instead.

- MT compressors not in minus zone

- Low-pass filtered opening degree for Vrec is greater than the "IT Start Vrec OD"

If one of these conditions is not true, the request from the receiver control will be “Full stop” and "Status Info" displays the reason for it.

When the IT compressor is running, the only condition to continue running is that Sgc reference is above "IT Comp. Sgc Min" minus 2 K.

**Note:** During emergency conditions, the above requirements are simplified if using IT can protect main cooling: i.e. inefficient operation is allowed.

##### **Receiver load ramp-up**

After starting the controller, the Vrec valve is in charge of controlling receiver pressure ( **1** ). Vrec will continue to control Prec until the filtered (see the end of this paragraph) opening degree is greater than the value "IT Start Vrec OD" limit - then the IT compressor will start up ( **2** ). Status for the Vrec/IT switch is shown in “IT-Start counter” on the page about receiver status. This reaches 100% when the Vrec valve has been open enough to switch to IT control.

The controller will now speed-regulate the IT compressor so that the pressure in the receiver is kept at the desired level. When the IT compressor starts, the Vrec valve will be closed immediately by the value of the parameter "IT Comp. Start" and continue to control as safety with a higher reference.

The parameter “IT Start delay filter” is the time constant for filtering Vrec, delaying the time when the IT compressor takes over. This to ensure that the load is consistently high enough to start the IT compressor.

If IT reaches the max. capacity, its capacity is locked and the Vrec reference is decreased to the current Prec reference. The Vrec controls Prec at the current reference ( **3** ).

If the user parameter “High VrecRef IT max” is set to YES, when the IT reaches the max capacity, its capacity is locked at MAX and the Vrec reference is maintained at higher reference ( **3a** ). The effect is to reduce the amount of vapour going thought Vrec valve when IT is at max. This condition implies that receiver pressure is allowed to fluctuate between Prec reference and the higher reference, instead of being control at Prec reference. In a plant that requires a sharp control of receiver pressure (for example for efficiency of liquid ejector), it is recommended to set “High VrecRef IT max” to No.

##### **Receiver load ramp-down**

When vapour load in the receiver decreases, the Vrec remains in control of Prec to the current reference until it is closed. ( **4** ) As soon as the Vrec is closed, control is switched to IT. IT controls Prec until the current Vrec reference is increased ( **5** ). IT is stopped when it reaches pump-down limit. With IT stopped, the Vrec controls Prec to the current reference.

The parameter “IT end delay” defines the time that the IT compressor must be stopped before regulation is transferred to the valve. A higher value will increase the operating hours of the IT compressor.

*[Figurtekst: 1 2 3 4 5 6 7 · Capacity is too low  IT pack in control IT capacity is locked at  IT capacity locked IT pack in control Vrec in control with  Vrec in control with · to start IT: Vrec is in  Vrec reference is increased maximum Vrec takes control Vrec in control Vrec reference is increased increased reference normal reference · control · When the flow is large enough · to run the IT pack, the valve · closes and the pack starts · IT end dela y · 0 bar 4 bar 0 bar 0 bar 4 bar 0 bar · OFF ON ON OFF · 1 2 3a 4a 5 6 7 · IT capacity is locked at  IT capacity locked · maximum Vrec takes control Vrec in control · 0 bar 4 bar 4 bar 4 bar 4 bar 0 bar · OFF ON ON OFF · Delay in IT response · Despite that the IT pack is controlling, its response might be  1 2 3 4 · delayed by a compressor timer. In this case Vrec is used to keep  Prec, hi g h-ref · pressure under control. · See the picture below. · Prec starts to rise ( 1 ). Prec, ref · Prec reaches the activation limit ( 2 ) for the by- pass valve which · starts to assist the IT-pack. The valve control works as safety on the  Comp timer · higher reference. · When the compressor timer expires ( 3 ), the IT pack starts the · compressor. Prec starts to fall quickly. · The Vrec valve closes and is deactivated ( 4 ). · The IT-pack is controlling as normal. · Total capacity · Vrecref o�set · IT · state · Total capacity · Vrecref offset · IT · state · Prec · IT capacity · Vrec OD]*

*[Figurtekst: Precref · Vrec OD]*

##### **IT Smart start**

The ideal setting for IT Start Vrec OD changes with operating conditions – both Receiver pressure and MT suction pressure reference are often floating references.

The controller can automatically calculate IT Start Vrec OD if IT smart start is enabled, the correct sizes and speed are set for the IT compressors and the Vrec valve are set-up.

To activate the feature, the user select ”Yes” to **IT Smart start enable** . (If this parameter is set to ”No” the switch from Vrec to IT will be at a fixed IT Start Vrec OD.)

The model is based on **Vrec valve type** information in I/O configuration.

Using supported **Danfoss valves** , no more information are needed: the controller will use internal model correlation.

For **other types of valves** , ”User Defined” can be selected. The user specifies:

- Motor properties (only for stepper valves)

- Kv valve [m<sup>3</sup> /h]: Kv parameter of the valve

- Flow at 50% [%]: Flowrate % at OD=50%, depending by the valve characteristics. It defines the shape of the valve curve.

*[Figurtekst: 100 · 90 · 80 · 70 · 60 · 50 · 40 · Flow at 50% · 30 · 20 · 10 · 0           10           20            30           40          50           60           70           80           90         100 · Opening [%] · % of capacity full open]*

In status page, the following readouts show the behavior of the control.

##### **IT Start Vrec OD:**

Current calculated bypass valve opening degree  that determine when to switch from the bypass valve to the IT compressors.

##### **IT start counter:**

Indicator on the distance from switching point. The switch from Vrec to IT happens whn this value reaches 100%.

List of supported valves: ETS 5T 8L-10L-14L-18L (only Stepper) CCM 10-20-30-40 (only Stepper) CCMT 3L-5L-8L-10L (only Stepper) CCMT 2-4-8-16-24-30-42 (only Stepper) ICM 20A, 25A, 32A, 40A, 50A, 65A (only Voltage AO) ICM 20A-33, 25A-33 (only Voltage AO)

##### **Readings from the overview display**

Control information Control sensor and references

Actuator specific info

Other controls

“Control status” describes what the controller is doing:

“Ctrl status reason” describes what the controller is responding to: **Low Sgc ref:** Low Sgc Reference **Low Sgc:** Low Sgc temperture **Low Shp:** Low Shp temperature **MT in –zone:** MT in Minus Zone **Low Vrec flow:** Too low flow via Vrec **Normal:** No impediments, normal Control **Vrec Manual:** Vrec valve is in manual mode **IT at max:** IT is at maximum capacity **IT not available:** IT is not able to start (compressor alarms) **MT not available:** MT is not able to start (compressor alarms/timers) **Prec sensor error:** Prec Sensor Error **IT end delay:** IT stays in control after stopping, allowing a restart **Default:** Nothing to add to the status

**OFF:** Main Switch is off **Fault/Emergency** Receiver sensor error **Valve ctrl.** Receiver valve is the primary controller **IT ctrl.** IT group is the primary controller **Hot gas dump** Hot gas dump is active **Standby** No control action

### **5.8 Setpoint Management**

##### **Introduction**

The complexity of CO2 packs has dramatically increased over the last ten years. The strong interaction between gas cooler and receiver, the introduction of parallel compressor and ejectors are just examples of this.

There has been a corresponding increase in the number of setpoints which have become difficult to handle, especially when setpoints are optimized on-line by the controller.

AK-PC 782A, includes setpoint management. Three modes are available, enabling different features:

##### Manual mode

- New section “Setpoint management” in Service tool

- Clear overview over all pressure related setpoints

##### Assisted mode

- Ensure the correct order of setpoints so that control actions take place in the right order

- Adapt references according to floating setpoint: avoid crossing reference values

- Avoid low/high pressure alarms

##### Automatic mode

- Set and optimize automatically many of the parameters

- Reduce the number of user-set parameters

##### **Setpoint management overview screens**

Setpoint column: Central place to configure setpoints.

Reference column: Overview over the actually used references. All in pressure units for easy comparison.

V column: Indication about the source of the references:

U = Reference as specified by the user.

- S = Controller moved a user specified setpoint to ensure correct control.

A = Automatically set by the controller.

##### **Assisted Setpoint management**

In assisted mode, the setpoint management ensures that references adjust to floating references to guarantee that they remain in the correct order and with minimum distances between them.

1. The MT reference drops, for example because of the Po optimization or because of the external offset. So far, there is no action from the setpoint management.

2. The neutral zone approaches the pump-down limit. To ensure the correct order, the pump-down limit is pushed down (min. ½ bar below the neutral zone).

3. The pump-down limit cannot be pushed further down because of the PoMin limit (min. ½ bar). Now the neutral zone is squeezed down to keep the neutral zone above the pumpdown limit.

4. The neutral zone is now only 3 K and will not be reduced any further. There is no more space for the MT reference to go further down.

##### **Application range for suction groups**

User-specified alarm limits will only be moved to force them into the physical limits of a CO2 plant:

- Above 66 bar (approx. 27 °C), the liquid and vapour become so alike in density that the separation in the receiver will not work properly anymore. Even the Po,max limit must be below this value.

- Below 4.2 bar (at -56 °C), CO2 freezes. The Po,min limit must be above 6 bar (approx. -53 °C).

Otherwise, nothing will move the alarm limits.

When the alarm limits are set too close to each other to fit all references in between, then the maximum reference will take precedence over the lower reference. This will typically result in frequent low-pressure alarms.

*[Figurtekst: User setpoint User-set · Reference modifier · Different functions can · Floating reference request to modify the · reference · Checks order and differences · Setpoint Management between the relevant · references · Actual references Actually used references · 1 2 3 4 · 29 · Po, ref · 28 NZ · PumpDown · 27 PoMin · 26 · 25 · 24 · 23 · 22 · 21 · 2 0 · 19 · Pressure [bar]]*

*[Figurtekst: Po,max · Min. ½ bar · Po,min and Po,max · Min. 3 K Po,ref Neutral are too close to fit · zone all references in. · Min. ½ bar · Po,min · Pump-down]*

##### **Assisted references for MT and LT packs**

The user-specified setpoint for the PoMT and the PoLT references can be offset by the Po optimization or by the external offset. The results are then subjected to the setpoint management to give the actually used references.

The various setpoints around the MT and LT references are treated in the same way.

The setpoint management will maintain the correct order:

- Maximum Po reference (Po,max)

- Upper limit for Neutral zone (NZ top)

- Current Po Reference (Po,ref)

- Lower limit of Neutral zone (NZ bottom)

- PumpDown Limit (PumpDown)

- Minimum Po reference (Po,min)

The setpoint management will enforce the minimum distances between the references as shown in the figure.

When the user sets the neutral zone width larger than 3 K, it may be squeezed down, but, it will not be widened when the user sets the NZ lower than 3 K.

*[Figurtekst: Po,max (max. 66 bar) · Min. ½ bar · Min. 3 K Po,ref Neutral zone · Min. ½ bar · Pump-down limit · Min. ½ bar · Po,min (min. 5 bar)]*

##### **Assisted setpoints for the IT pack**

When working in assisted or automatic mode, the different setpoints for IT pack will be maintained in the order shown in the picture.

When the IT is in control, the Vrec reference is calculated as the maximum of:

- Prec,ref + 4 bar,

- top of the neutral zone plus 2 bar, otherwise, it equals the Prec,ref.

The MT cut-out P limit is located at 75% of the upper P-band.

AC disable and HR disable respectively are at the bottom and at the top of the max. and min. P-bands.

*[Figurtekst: Prec max (max. 66 barg) · Min. 0 bar · MT cut-out P · Min. 2 bar 75% Prec max P-band · Min. 0 bar · AC Disable · Min. ½ bar · Vrec P ref · See text · Min. 3 K · Prec,ref Neutral zone · Min. ½ bar · Pump-down · Min. ½ bar · HR disable · Min. 0 bar · Min. 2 bar Prec min P-band · Min. 0 bar · Prec min]*

*[Figurtekst: Assisted setpoints for hot gas dump · The cut-in limit must be below the pump-down limit or the hot · gas dump might prevent reaching the pump-down limit. · Prec,ref Neutral zone · The cut-in limit should be above the Prec min Pband, because in  Min. 0 bar · Cut-out limit · this P-band the plant will effectively use hot gas loop to raise the · receiver pressure. This is very inefficient. · Pump-down · Hot gas dump · min. 1 bar Min. · Cancel HR · ½ bar · Cut-in limit · Prec min P-band · Prec min · Automatic setpoints · For ease of use, the setpoint management offers  automatic mode . · This can be selected for each suction group individually (shown · is the LT group). This can be used to reduce the need to specify · setpoints in general. When you revert back to assisted mode, it will · restore all original setpoints. · The setpoint management will fill out selected setpoints automatically · when in  automatic mode . They are no longer set by the user. · Automatic mode  is only available in combination with the  assisted · mode . After the AK-PC 782A has filled out the automatic setpoints, · they are subjected to all rules that apply in  assisted mode .]*

*[Figurtekst: Automatic setpoints · For ease of use, the setpoint management offers  automatic mode . · This can be selected for each suction group individually (shown · is the LT group). This can be used to reduce the need to specify · setpoints in general. When you revert back to assisted mode, it will · restore all original setpoints. · The setpoint management will fill out selected setpoints automatically · when in  automatic mode . They are no longer set by the user. · Automatic mode  is only available in combination with the  assisted · mode . After the AK-PC 782A has filled out the automatic setpoints, · they are subjected to all rules that apply in  assisted mode . · Manual setpoints for HP Control · Provide a clear overview of all pressure related setpoints for  Pgc max. · HP control ensuring right order and the minimum distance  (max./min. 129/29 bar) · between the parameters, as show in the figure. Setting setpoint  Min. 1 bar · management to “Manual” or “Assisted” do not affect this feature. · Pgc max. limit P-band · (max./min. 20/1 bar) · User can change one parameter per time. · When “Pc max. limit MT” or “Pc max limit IT” are changed, no  Min. 0 bar · special rules are applied. Pgc HR max. · Min. 1 bar · When “Pgc max.” , “Pgc min.” or “Pgc max. limit P-band”  (high  (max./min. 122/28 bar) · priority parameters) are changed, the controller will adapt  Min. 1 bar Min. 2 bar · current user choice to fit in minimum distances reported in the · Pgc HR min. · picture, leaving unchanged the others two.  This can always  (max./min. 121/27 bar) · trigger changes to “Pgc HR max” and “Pgc HR min” (low priority · parameters). Min. 1 bar · When “Pgc HR max” or “Pgc HR min” is changed by the user, the  Pgc min · controller will adapt the changed parameter to fit in (see picture).  (max./min. 120/9 bar) · Other parameter are not changed. · This approach is respected even if heat reclaim is not configured. · (i.e : “Pgc HR max.” and “Pgc HR min.” are not visible).]*

### **5.9 General monitoring functions**

**General alarm inputs** (10 units)

An input can be used for monitoring an external signal.

The individual signal can be adapted to the relevant use as it is possible to give the alarm function a name and to indicate your own alarm text.

A time delay can be set for the alarm.

##### **General thermostat functions** (10 units)

The function may freely be used for alarm monitoring of the plant temperatures or for ON/OFF thermostat control. An example could be thermostat control of the fan in the compressor compartment.

**General voltage input with ancillary relay** (5 units) 5 general voltage inputs are accessible for monitoring of various voltage measurements of the installation. Examples are monitoring of a leak detector, moisture measurement and level signal - all with ancillary alarm functions. The voltage inputs can be used to monitor standard voltage signals (0 – 5 V, 1 – 5 V, 2 – 10 V or 0 – 10 V). If required, one can also use 0 – 20 mA or 4 – 20 mA if external resistance is placed at the inlet to adjust the signal to the voltage. A relay outlet can be attached to the monitoring so that one can control external units.

For each inlet, the following can be set/read out:

- Freely definable name

- Selection of signal type (0 – 5 V, 1 – 5 V, 2 – 10 V, or 0 – 10 V) or other signal

- Scaling of readout so it corresponds to measuring unit

- High and low alarm limit including delay times

*[Figurtekst: Saux max . · min .]*

The thermostat can either use one of the sensors used by the regulation (Ss, Sd, Sc3) or an independent sensor (Saux1, Saux2, Saux3, Saux4).

Cut-in and cut-out limits are set for the thermostat. Coupling of the thermostat’s output will be based on the actual sensor temperature. Alarm limits can be set for low and high temperature, respectively, including separate alarm delays.

The individual thermostat function can be adapted to the relevant application as it is possible to give the thermostat a name and to indicate alarm texts.

##### **General pressure control functions** (5 units)

(If the receiver is being pressure controlled, one of the five is used for this function. This means that subsequently there are four general pressure switches.)

The function may freely be used for alarm monitoring of plant pressure or for ON/OFF pressure control regulation.

*[Figurtekst: max. · min. · Paux]*

The pressure control can either use one of the sensors used by the control function (Po, Pc) or an independent sensor (Paux1, Paux2, Paux3).

Cut-in and cut-out limits are set for the pressure control. Coupling of the pressure control’s output will be based on the actual pressure.

Alarm limits can be set for low and high pressure, respectively, including separate alarm delays.

The individual pressure control function can be adapted to the relevant application as it is possible to give the pressure control a name and indicate alarm texts.

- Freely definable alarm text

- Attach a relay output with cut-in and cut-out limits including delay times

*[Figurtekst: Saux max . · min .]*

##### **General PI functions** (6 units)

The function can be freely used for controlling a required function, or it can be used to send signals to the controller regarding operating states. An example could be an out/in control for the use of the heat recovery function.

*[Figurtekst: 0 – 10 V · S U · P]*

Signals can be received from e.g.:

- Temperature sensor

- Pressure transmitter

- Saturation temperature

- Voltage signal

- Internal signals such as: Tc, Pc, Ss and Sd Signals are shown on the next page.

- Calculated superheat using "2 Inp superheat" input mode. The superheat is calculated between input 1 as temperature type and input 2 as pressure type converted to saturation temperature. Calculated superheat = input 1 - input 2(converted to saturation temperature).

Incase of sensor error or when the pressure is of range, the user will be notified by a superheat calculation failure alarm.

Signals can be sent to the following: Voltage signal Valve with stepper motor PWM (pulse width modulated) signal for AKV valve.

The PI function is shown overleaf.

*[Figurtekst: Danfoss 80Z746.10]*

*[Figurtekst: Input Mode: Input Mode: · 1 Input 2 Inp Superheat · Input 1 · Superheat Calculation · Input 2 Function]*

##### prepared examples

Settings

General

Signal and setting values are converted and adjusted as a percentage value of the signal.

A slow process will normally not be critical for the setting of P-part and I-part.

However, if the process is quick, more careful set-up is required.

A general balancing might be:

- Check max. and min. settings

- Increase the integration time so that it is not mixed up with the balancing

- Reduce Kp to start with

- Start the process

- Adjust Kp until the process starts fluctuating and is constantly fluctuating

- Adjust Kp to half the value

- Adjust Tn down until the process starts fluctuating again

- Adjust Tn to double values

Further information: Application guide. Literature number RA8AK.

### **5.10 Miscellaneous**

If the power supply to AK-PC 782A or the stepper motor valves fails, the system cannot be controlled. It is recommended to install an emergency supply (UPS) for at least the valve drivers, to ensure proper closing of the valve. An alarm can only be sent when the base module is also connected to a UPS. For remote monitoring, a relay output in the UPS must be connected to a dedicated DI in the controller. This is a pure monitoring function, without any further control functionality.

##### **Main switch**

The main switch is used to stop and start the controlling function.

The switch-over has 2 positions: - Normal controlling state (Setting = ON)

- Control stopped (Setting = OFF)

In addition, one can also choose to use a digital input as an external main switch.

If the switch-over or the external main switch is set at OF F, all the control ’ s functions are inactive a nd an alarm is generated to draw attention to this – all other alarms cease.

##### **External switch for stopping compressors**

The switch will stop the compressors, but all other functions will continue to be regulated.

##### **Clock function**

The controller contains a clock function. The clock function is used only to change between day/night. The year, month, date, hour and minutes must be set.

In the event of a power failure, the time setting will be remembered for at least 12 hours.

If the controller is connected to an installation with an AK system manager, this will automatically reset the clock function.

##### **Alarms and messages**

In connection with the controller’s functions, there are a number of alarms and messages that become visible in cases of fault or erroneous operation.

##### **Alarm history**

The controller contains an alarm history (log) that contains all active alarms as well as the last 40 historical alarms. In the alarm history you can see when the alarm began and when it stopped. In addition, one can see the priority of each alarm as well as when the alarm has been acknowledged and by which user.

##### **Alarm priority**

Differentiation is made between important and not-so-important information. The importance – or priority – is set for some alarms whilst others can be changed voluntarily (this change can only be done with attachment of AK-ST 500 Service Tool software to the system and settings must be made in each individual controller).

##### **Refrigerant**

For CO2 only.

##### **Sensor failure**

If lack of signal from one of the connected temperature sensors or pressure transmitters is registered an alarm will be given.

• When there is a P0 error, regulation will continue with 50% cutin capacity during day operation and 25% cut-in capacity during night operation – but minimum one step.

• When there is a Pc error 100% condenser capacity will be cut in, but the compressor regulation will remain normal.

• In the event of Prec failure, regulation continues using the average Vrec OD recorded for the last 6 hours. The opening degree is then adjusted according to the MT capacity.

• When there is an error on the Sd sensor the safety monitoring of the discharge gas temperature will be discontinued.

• When there is an error on the Ss sensor the monitoring of the superheat on the suction line will be discontinued.

• When there is an error on the outdoor temperature sensor Sc3 it cannot regulate with variable condensing pressure reference. Instead you use the PC ref. min. value as reference.

• In the event of Sgc faults, further adjustments are carried out using the Shp signal. Note: An incorrect sensor must be in order for 10 minutes before the sensor alarm deactivates.

##### **Safety disconnection signal**

Unexpected disconnection of the compressor, condensation fan or frequency convertor can result in unexpected temperature increases in the system. If necessary, use the necessary safety signals to ensure that the controller receives signals about disconnections.

The setting decides which sorting / action must be carried out when an alarm is sounded.

• “High” is the most important

• “Log only” is the lowest

- “Interrupted” results in no action

##### **Alarm relay**

One can also choose whether one requires an alarm output on the controller as a local alarm indication. For this alarm relay it is possible to define which alarm priority it must react to – one can choose between the following:

• “Non” – no alarm relay is used

• “High” – Alarm relay is activated only with alarms with high priority

• “Low - High” – Alarm relay is activated only with alarms with “low” priority, “medium” or “high” priority.

The relationship between alarm priority and action appears in the schedule below.

|Setting|Log|Alarm r|elay||Send|AKM des-|
|---|---|---|---|---|---|---|
|||Non|High|Low-High|Network|tination|
|High|X||X|X|X|1|
|Medium|X|||X|X|2|
|Low|X|||X|X|3|
|Log only|X|||||4|
|Interrupted|||||||

##### **Sensor calibration**

The input signal from all connected sensors can be corrected. A correction will only be necessary if the sensor cable is long and has a small cross-sectional area. All displays and functions will reflect the corrected value.

##### **Alarm acknowledgement**

If the controller is connected to a network with a system manager as alarm receiver, this will automatically acknowledge the alarms that are sent to this.

##### **I'm alive relay**

The function reserves a relay that is pulled under normal regulation.

The relay will be released if:

If the controller on the other hand is not included in a network, the user must acknowledge all alarms.

##### **Alarm transmission**

Alarm transmission is enabled in the pack controller when connected to a frontend with alarm transmission enabled.

Alarm transmission can be disabled in the Pack controller by Configuration menu → System setup → Disable alarm router (see page 50).

**Very important:** By disabling alarm transmission, no alarm will be sent from the controller to the front-end. Missing alarms could cause serious damage to the plant.

This feature is only active in Advanced user mode and protected by Configuration Lock. Finally, there is a 2-stage accept level.

This feature does not prevent the communication of the pack controller with the frontend. It only disables the sending of the alarms.

Reenabling the alarm transmission, requires a rescan or pressing the service pin of the pack controller.

**Notes:** Service pin only works with SM350 & SM720.

##### **Alarm acknowledgement**

If the controller is connected to a network with a system manager as alarm receiver, this will automatically acknowledge the alarms that are sent to this.

If the controller on the other hand does not have alarm transmission activated, then the user must acknowledge all alarms.

##### **Alarm LED**

The alarm LED on the front of the controller indicates the controller’s alarm status.

Blinking: There is an active alarm or an unacknowledged alarm. Fixed light: There is an active alarm that has been acknowledged. Switched off: There are no active alarms and no unacknowledged alarms.

- The regulation is stopped by the internal or external main switch

- The controller fails

##### **IO Status and manual**

The function is used in connection with installation, servicing and fault-finding on the equipment. With the help of the function, the connected outputs are controlled.

##### **Measurements**

The status of all inlets and outlets can be read and controlled here.

##### **Forced operation**

One can carry out an override of all outlets here to control whether these are correctly attached.

Note: There is no monitoring when the outlets are overridden.

##### **Logging/registration of parameters**

As a tool for documentation and fault-finding, the controller provides the possibility of logging of parameter data in the internal memory. Via AK-ST 500 Service Tool software one can:

- a) Select up to 10 parameter values the controller will continuously register

b) State how often they must be registered

The controller has a limited memory but as a rule of thumb, the 10 parameters can be saved, which are registered every 10 minutes for 2 days.

Via AK-ST 500 one can subsequently read the historical values in the form of graph presentations.

(The log only works when the clock has been set.)

##### **Forced operation via network**

The controller contains settings that can be operated from the system unit's forced operation function via data communication.

When the forced operation function asks about one change, all the connected controllers on this network will be set simultaneously. There are the following options:

- Change to night operation

- Forced closure of injection valves (Injection ON)

- Optimization of suction pressure (Po)

##### **Operating AKM / Service Tool**

The set-up of the controller itself can only be carried out via AK-ST 500 service tool software. The operation is described in fitters' on-site guide.

If the controller is included in a network with a system unit, one can subsequently carry out the daily operation of the controller via AKM system software, i.e. one can see and change daily readouts/ settings.

Note: AKM system software does not provide access to all configuration settings of the controller. The settings/readouts that may be made appear in the AKM menu operation (see also Literature overview).

##### **Authorisation / Passwords**

The controller can be operated with System software type AKM and Service Tool software AK-ST 500.

Both methods of operation provide the possibility for access to several levels according to the user’s insight into the various functions.

System software type AKM:

The various users are defined here with initials and key word. Access is then opened to exactly the functions that the user may operate.

The operation is described in the AKM manual.

Service Tool software AK-ST 500:

The operation is described in fitters' on-site guide.

When a user is created, the following must be stated: a) State a user name b) State a password c) Select user level

d) Select units – either US (e.g. °F and PSI) or Danfoss SI (°C and Bar) e) Select language

Access is given to four user levels:

1. DFLT – Default user – Access without use of password

   - See daily settings and readouts.

2. Daily – Daily user Set selected functions and carry out acknowledgement of alarms

3. SERV – Service user

   - All settings in the menu system except for creation of new users

4. SUPV – Supervisor user

   - All settings including the creation of new users.

##### **Display of suction pressure and condensing pressure**

|r92|Set point suction pressure LT-circuit<br>Settingof required suctionpressure reference in °C|
|---|---|
|t49|<br>Hot water. Reference for Stw8-temperature|
|t50|Hot water. Settingof hot water control mode: Automatic/off|
|u21|Superheat in suction line MT-circuit|
|u44|Sc3 out door temperature in °C|
|u48|Actual regulation  status on condenser<br>1: Stopped (Main switch off or set manually off)<br>5: Standby (Fans are not running)<br>11: Running (Fans are running)|
|u49|Cut in condenser capacityin %|
|u50|Reference for condenser capacityin %|
|u51|Actual regulation status on suction group MT<br>1: Normal Ctrl. (Normal PI control of compressor capacity)<br>2: Alarm comp. (Compressor capacity cannot be increased due to an<br>alarm on a compressor)|
||<br>3: ON timer (Compressor capacity cannot be reduced due to a minimum<br>Oi|
||n-tmer)<br>4: OFF timer (Compressor capacity cannot be increased due to a<br>minimum Off-timer or restart timer)<br>5: Normal Ctrl. (No compressor switching inside the neutral zone)<br>6: Inj. ON delay (Start delay after enabling the injection ON signal)<br>7: Coordination (Waiting for the release signal from MT, in LT<br>applications)|
||8: 1st comp.delay (Initial runtime for the first compressor, before<br>additional steps are cut in)|
||<br>9: Pump down (Last compressor cannot be stopped before the pump<br>down limit has been reached)<br>10: Sensor error (Compressors run at emergency capacity, due to a sensor<br>|
||error)<br>11: Load shed (Compressor capacity limited due to a load shed request)<br>12: Sd High (Stepwise reduction of compressor capacity due to a high<br>discharge temperature)<br>13: Pc High (Stepwise reduction of compressor capacity due to a high<br>discharge pressure)<br>14: Manual ctrl. (Requested compressor capacity set manually)<br>15: OFF (Main switch is off)<br>16: Inrush guard (Waiting for minimum delay between compressor starts<br>(5 seconds))<br>19: Prec high (Stepwise reduction of compressor capacity due to a high<br>receiver pressure)<br>20: Vrec ctrl (IT is off while the receiver pressure is controlled by the by-<br>pass valve)|
|u52|Cut in compressor capacityin % MT-circuit|
|u53|Reference for compressor capacityMT-circuit|
|u54|Sd dischargegas temperature in °C MT-circuit|
|u55<br>|Ss Suctiongas temperature in °C MT-circuit<br>|
|u98|Actual temperature for S7 media sensor|
|U01|Actual Pc condensing pressure in °C|
|U46|Read out of "Req.CapA %" LT-Circuit|
|U47|Read out of  "Comp.Cap%" LT-circuit|
|U48|Read out of "Suction status" LT-circuit|
|U49|Read out of "Tc" i LT-circuit|
|U50|Read out of "Ss" i LT-circuit|
|U51|Read out of "Sd" i LT-circuit|
|U52|Read out of "Sh" in LT-circuit|
|AL1|Alarm suctionpressure|
|AL2|Alarm condenser|
|- - 1|<br>Initiation,Displayis connected to output  "A", (- - 2 = output "B" etc.)|
|**Note:**|the Koolcode app showin the parameter list and alarms/|
|<br>status|g<br>is available for free download in App Store and Google Play.|
|If you|want to see one of the values for what is given under|
|<br>"funct|<br>ion" you should use the buttons in the following way:|

One to four separate displays can be connected to the controller. Connection is accomplished by means of wires with plug connections. The display may be placed in a control box front, for example.

When a display is connected, it will show the value for what is indicated in the set-up. It can be: compressors' regulation sensor P0 in temperature, MT, LT P0 in bar, MT, LT Ss, MT, LT, IT Sd, MT, LT, IT Condensors regulation sensor Tc, MT Pc bar, MT S7 Sgc Pgc bar Prec bar Trec Speed Compressor, , MT, LT, IT

|Display|Primary readout *|Secondary readout|
|---|---|---|
|A|Regulation sensor suctionpressure|Cutin capacityMT|
|B|Regulation sensor condenser|Cutin capacityLT|
|C|Ss|Cutin capacityIT|
|D|Sd|Openingdegree|

* The primary reading can be changed to other measurements, if required.

When (on plug A) a display with control buttons is chosen, a simple operation via a menu system can be performed in addition to the display of suction pressure and condensing pressure:

|No.|Function|u53<br>Reference for compressor capacityMT-circuit|
|---|---|---|
|o57|Capacity settings for condenser|u54<br>Sd dischargegas temperature in °C MT-circuit|
||0: MAN,1: OFF,2: AUTO|u55<br>Ss Suctiongas temperature in °C MT-circuit|
|058|Manual settingof condenser capacity|u98<br>Actual temperature for S7 media sensor|
|o59|Capacity setting for suction group MT|U01<br>Actual Pc condensing pressure in °C|
||0: MAN,1: OFF,2: AUTO|U46<br>Read out of "Req.CapA %" LT-Circuit|
|o60|Manual settingof suctionpressure capacityMT circuit|U47<br>Read out of  "Comp.Cap%" LT-circuit|
|h15|Highpressure. Settingof Pgc minimum|U48<br>Read out of "Suction status" LT-circuit|
|h16|Highpressure. Settingof HP-control mode: Automatic/manual|U49<br>Read out of "Tc" i LT-circuit|
|h17|Highpressure.  Manuel mode. Settingof valves openingdegree|U50<br>Read out of "Ss" i LT-circuit|
|h18|Heat recovery. Reference for Shr8-temperature|U51<br>Read out of "Sd" i LT-circuit|
|h19|Heat recovery. Settingof heat recoverycontrol mode: Automatic/off|U52<br>Read out of "Sh" in LT-circuit|
|P62|Manual settingof suctionpressure capacityLT circuit||
|P63|Capacity setting for suction group LT<br>|AL1<br>Alarm suctionpressure|
||0: MAN,1: OFF,2: AUTO<br>|AL2<br>Alarm condenser|
|r12|Main switch<br>0: Controller stopped<br>1: Regulating|**Note:**the Koolcode app showing the parameter list and alarms/<br>- - 1<br>Initiation,Displayis connected to output  "A", (- - 2 = output "B" etc.)|
|r23|Set point suction pressure MT-circuit<br>Settingof required suctionpressure reference in °C|<br>status is available for free download in App Store and Google Play.|
|r24|Suction pressure reference MT-circuit<br>Actual reference temperature for compressor capacity|If you want to see one of the values for what is given under<br>"function" you should use the buttons in the following way:|
|r28|Set point condenser<br>Settingof required condenserpressure in  °C|<br>1. Press on the upper button until a parameter is shown<br>2 Press on the uer or lower button and find the arameter ou|
|r29|Condenser reference<br>Actual  reference for temperature for condenser capacity|.    pp     i  p y<br>want to read<br>|
|r57|Po MT evaporating pressure in °C|3. Press on the middle button until the value of the parameter<br>|
|r86|Receiver control. Reference for Prec|is displayed. After a short time, the display will return<br>|
|r87|Receiver control. Setting of the receiver control mode : Automatic /<br>manual|automatically to the "Read out display".|
|r88|Receiver control. Manual mode. Settingof the valves openingdegree||
|r90|Po LT evaporating pressure in °C||
|r91|Suction pressure reference LT-circuit<br>Actual reference temperature for compressor capacity||

##### **Light-emitting diodes on the controller**

*[Figurtekst: Internal communication · between the modules: · Quick flash = error · Constantly On = error · Status of output 1-8 · Slow flash = OK · Quick flash = answer from gateway · n Power remains on for 10 mins after network · n Comm registration · n DO1  n Status Constantly ON = error · n DO2  n Service Tool Constantly OFF = error · n DO3  n LON · External communication · n DO4  n I/O extension · Communication to AK-CM 102 · n DO5  n Alarm · n DO6 Flash = active alarm/not cancelled · n DO7  n Display Constant ON = Active alarm/cancelled · n DO8  n Service Pin · Network installation]*

##### **Graphic display MMIGRS2**

With the display one has access to most of the controller functions. For access, connect the display to the controller and activate the address on MMIGRS2. (A separate power supply does **not** need to be connected). Power is supplied directly from the controller via the cable.

##### Setting:

- 1.Press both the "x" and "enter" buttons and hold in for 5 seconds. The BIOS menu is then displayed.

2. Select the "MCX selection" line and press "enter"

3. Select the "Man selection" line and press "enter"

4. The address will be displayed. Check that it is 001, press "enter". Data will then be collected from the controller.

(If you are logged on to the controller via the Service tool, you cannot also log on using MMIGRS2. Or vice-versa. Only the first user logged in has operator access.)

##### **Valve Set-up**

When Vrec is connected to an AO, an ETS, ICM, CCM or CCMT valve can be selected in the drop-down menu.

If the connected valve cannot be selected in the list, then Kv and Flow at 50 must be set. See description under Stepper Motor Valves on how to set the values correctly.

##### **Stepper Motor Valves**

When selecting a Danfoss stepper motor valve, all settings are factory set. Here, it is only necessary to select the type of valve. If a valve from other manufacturers is used, the following settings have to be made. Get data from the valve manufacturer:

##### Max Operating Steps.

The number of steps that correspond to a valve position of 100%. This value is limited to a range of 0 – 10,000 steps.

##### Hysteresis

The number of steps needed to correct for mechanical hysteresis when a reduction gear is part of the valve design. This adjustment is only applied, if an additional opening of the valve is requested.

If this is the case, the valve opens an additional amount equal to this value, before driving the valve in the closing direction by this same value.

This value is limited to 0 – 127 steps.

##### Step Rate

The desired valve drive rate in steps per second. This value is limited to 20 – 500 steps / sec.

##### Holding Current

The percentage of the programmed Max Phase Current that should be applied to each phase of the stepper output when the valve is stationary.  If required, this current ensures that the valve maintains its last programmed position.  This value is limited to a range of 0 – 70% given in 10% steps.

##### Overdrive at Valve Init

During valve initialization, the amount to overdrive the valve, beyond the 0% position, to ensure that the valve has fully closed. This value is limited to a range of 0 - 31%.

##### Phase current

The phase current applied to each phase of the stepper motor during the actual valve movement can be set in the range 0 – 325 mA. The value of the phase current is set in RMS – be aware that some valve manufacturers are using peak currents in the data sheet (multiply the peak current by 0.71 to convert to the RMS value). ( **Note:** the actual phase current can be higher due to stepper driver resolution)

##### Soft Landing after Valve Init

At power on, the valve is performing a valve Initialization i.e. closing the valve  with “Max Operating Steps” plus “Overdrive At Valve Init “steps to generate a zero-point calibration of the system. Hereafter a “Soft landing after Valve Init” is made to  minimize the closing force on the valve seat with a few opening steps according to setting of  “Hysteresis” or  min. 20 steps.

##### Failsafe Position

During failsafe mode of operation (e.g. resulting from a loss of communications to this module), the default valve position is specified. This value is limited to a range of 0 – 100%.

##### Kv (Vrec only)

Kv is the maximum flowrate of the valve in m<sup>3</sup> /h that can be read in the valve data sheet.

##### Flow at 50% (Vrec only)

The relative flowrate “Flow at 50%” must be read from the characteristic curve in the valve data sheet and entered in the valve config menu.

An example for reading Flow at 50% is shown in page 122.

### **5.11 KPI and COP calculations**

The controller can calculate the primary KPI (Key Performance Indicator) parameters and provide an estimate of suction group efficiency (e.g. the Coefficient Of Performance, COP) These are calculated for each suction group (MT, LT, IT) reflecting the efficiencies in providing cooling to the corresponding suction pressure levels.

The KPIs and COPs are calculated as if the plant consists of three single stage cooling cycles: MT, LT and IT. LT cools at the LT level and rejects heat at the MT level (see detailed descriptions in LT suction group KPIs). IT works as single stage  in parallel with MT, reducing the cooling MT has to deliver.

The relative low number of sensors and compressors status used for each suction group KPIs provide easier setup verification during plant commitioning and system trouble shooting (see details for each suction group KPI). Estimates are given for the cooling capacity, the compressor power and the rejected heat.

**Note:** The COP relies on the operational conditions and is a realtime estimation of the efficiency under those conditions.

##### **Preconditions**

- Control of both the compressor group and gascooler.

- Heat reclaim is not included in the calculation.

- Not valid when MT suction control may alternate between two pressure transducers (P0 and Psuc - typically used with Low Pressure Multi Ejectors).

- Only the floating reference mode for the gascooler (with outdoor air temperature) is supported.

- Additional heat exchanger installed after the gas cooler can only be internal heat exchanger (no external sub-cooling).

- De-superheating is not supported.

- (Screw) compressors with economizer are not supported.

- Forced cooling of compressors is not supported.

##### **Discharge temperature sensors**

These sensors are generally used for the purpose of compressor and plant safety and high accuracy is generally not required. When used for KPI and COP calculation, the accuracy of the measurements become critical, for this reason:

- Discharge temperature sensors at each compressor are highly recommended because it is more accurate than a common sensor.

- When a common discharge temperature is used then it must be placed close to the compressors and the pipe must not shared with other suction groups. If the plant configuration does not allow that then individual discharge sensors are required.

- All the discharge pipes and sensors must be thermally insulated.

*[Figurtekst: AK-PC 782B · CTR · Sliq · MT suction group KPIs Pgc Pc · The COP provides information how efficient  the MT suction group · is performing for the single stage cycle visualized in the picture · below. · “Cooling Capacity” is the cooling effect produced by the by the MT  Prec · compressors. This includes cooling down the discharge gas from · the LT compressors. “Heat rejection” is the heat that is rejected · from the MT discharge gas. · The following sensors must be configured and measure realistic  PoMT · plant conditions: Ss, Po, Sd (all for MT suction group) and Pc, Pgc, · Sc3, Shp (Sgc for configuration without Shp sensor). · PoLT · IT · MT · LT]*

##### **LT suction group KPIs**

The COP provides information how efficient  the LT suction group is performing for the single stage cycle visualized in the picture below.

“Cooling Capacity” is the cooling effect at LT suction pressure (PoLT). “Heat rejection” correspond to the heat that LT suction group contributes to the MT load, cooling down the discharge gas from the LT compressors into high pressure liquid.

The following sensors must be configured and measure realistic plant conditions: Ss, Po, Sd (all for LT suction group) and Prec, PoMT.

For best accuracy it is recommended to mount an Sliq sensor on the liquid line after the receiver, especially when an internal heat exchanger is used to sub-cool the liquid.

##### **IT suction group KPIs**

The COP provides information how efficient  the IT suction group is performing for the single stage cycle visualized in the picture below.

“Cooling Capacity” is the cooling effect produced by the IT compressors at Prec pressure level.

This increases when the IT compressors or vapour ejectors are utilized because these move load from MT to IT. “Heat rejection” is the heat that is rejected from the IT discharge gas.

The following sensors must be configured and measure realistic plant conditions: Ss, Sd (all for IT suction group), Prec, Pc, Pgc, Sc3, Shp (Sgc for configuration without Shp sensor).

##### **Settings and readouts for KPI:**

##### **Estimated KPI's**

Set the frequency with which KPI calculation should be visualized. The options are:

- Current: continuously updated. Variation in the system might take 10 – 15 min before they can be noticed.

*[Figurtekst: Pgc Pc · Prec · PoMT · PoLT · Pgc Pc · Prec · PoMT · PoLT · IT · MT · LT · IT · MT · LT]*

- Hourly: Average for the previous hour

- Daily: Average for the previous day

##### **KPI status** (validity)

"When "Current" view is selected, here you can see if the calculated KPIs are considered valid or not.  Dynamics in the system, such as start-up and shutdown, as well as invalid sensor readings, too low or too high performance can lead to invalid calculations. When "Hourly" or "Daily" view is selected, the percentage of valid data sample for the previous hour/day calculation is shown. When the percentage is  below 30%, the data should generally not be trusted. A well set-up system is expected to have 80-95% validity.

##### **Cooling capacity**

Estimated cold production at suction pressure

##### **Compressor power**

Estimated electrical power to the compressors

##### **Heat rejection**

Estimation of how much heat (energy) is rejected at discharge pressure level.

##### **COP**

The estimated COP (Co-efficiency Of Performance) of the compressors. Calculated as the ratio between delivered energy (cooling capacity) and consumed energy (compressor power).

##### **Verification of the set-up**

- For each suction group, verify that all relevant sensors are connected, correctly placed and insulated

- Verify compressors can and do accumulate running. The setup cannot be verified with a standing still suction group .

- 5 – 10 min after the start-up of the compressors, check “KPI Status” shows “Valid”.

- Let the suction group run for 2 – 3 hours with enough load, then verify “KPI validity” (hourly) is high (80 – 100%).

### **5.12 Appendix A – Compressor combinations and coupling patterns**

In this section, there is a more detailed description of the compressor combinations and the associated coupling patterns.

##### **Compressor application 1 – single step**

The capacity distributor is capable of managing up to 10 one-step compressors according to the following coupling patterns:

• Cyclical

##### **Compressor application 2 – 1 x unload + single step**

The controller is able to control a combination of one capacity controlled compressor and multiple single step compressors. The advantage

of this combination is that the unloader valves will be used to fill in capacity gaps and thereby achieve many capacity steps via few compressors.

- Best fit

Here, all compressors are of the same size and the compressors are cut in and cut out in accordance with the First-In-First-Out (FIFO) principle, in order to equalize operating hours between the compressors.

*[Figurtekst: Cap. % · Pc Sd · Ss Po C4 · C3 C3 C4 · C2 C2 C2 C3 C4 · C1 C1 C1 C1 C2 C3 C4 · 20 kW 20 kW 20 kW 20 kW t]*

- There is operating time equalizing between all compressors

- The compressor with the fewest running hours starts first

- The compressor with the most running hours stops first.

##### Best fit - example

Here at least two compressors are of different sizes. The capacity distributor will cut in and cut out the compressors to produce the best possible capacity fit (the least possible capacity jump).

*[Figurtekst: Cap. % · Pc Sd · Ss Po · C2 · C1 C1C2 · C2 · C1 C1 C4 C4 C4 C4 C2 · C2 · 10 kW 10 kW 20 kW 20 kW C1 C1 C3 C3 C3 C3 C3 C3 C4 C4 C2 t]*

- There is operating time equalizing between the compressors 1 and 2 (same size in example)

- There is operating time equalizing between the compressors 3 and 4 (same size in example)

- All compressors are the same size

- The capacity-regulated compressor can have up to three unload valves

- The main step and the unload valves can be different sizes, i.e. 50%, 25% and 25%.

This compressor combination can be handled in the following coupling patterns:

- Cyclical

##### General regarding Handling:

##### Cut-in

The capacity-regulated compressors with unloader valves start before one-step compressors. The capacity-controlled compressor will always be fully loaded before cutting-in of subsequent one-step compressors.

##### Cut-out

The capacity-regulated compressor will always be the last to stop. The capacity-controlled compressor will always be fully loaded before cut-in of subsequent one-step compressors.

Unloader valves

At cyclical operation unloader valves are used to close capacity holes from the subsequent one-step compressors.

Anti-cycle timer restrictions

In case a capacity-controlled compressor is prevented in starting due to anti-cycle timer restrictions, then the start of any subsequent one-step compressors is not allowed. The capacity-controlled compressor is started when the timer restriction has expired.

The one-step compressors will be cut in and cut out in accordance with The First-In-First-Out (FIFO) principle in order to equalize operating hours between the compressors.

*[Figurtekst: Cap. % · Pc Sd · Ss Po · C1.1 · C1 C1 C1 · C1.1 C1.1 · C 1  C 1  C3 C3 C3 C 1  C 1 · C1.1 C1.1 · 10+10 kW 20 kW 20 kW C1 C1 C2 C2 C2 C2 C2 C3 C3 C1 C1 t]*

- The capacity-controlled compressor is the first to start and the last to stop.

- Unloader valves are used to close capacity holes

- There is operating time equalizing between the compressors 2 and 3 (same size in example).

##### **Compressor application 3 – 2 x unload + single step**

The controller is able to control a combination of capacity controlled compressors and multiple single step compressors. The advantage

of this combination is that the unloader valves will be used to fill in capacity gaps and thereby achieve many capacity steps via few compressors.

- All compressors are the same size

- The capacity-regulated compressors have the same number of unload valves (max 3)

- The main step on the capacity-regulated compressors have the same size

- The main step and the unload valves can be different sizes, i.e. 50%, 25% and 25%.

##### **Compressor application 4 – Only capacity controlled compressors**

The controller is capable of controlling capacity-regulated piston compressors of the same size with up to 3 unload valves.

- All compressors are the same size

- The capacity-regulated compressors have the same number of unload valves (max 3)

- The main step on the capacity-regulated compressors are the same size

- The main step and the unload valves can be different sizes, i.e. 50%, 25% and 25%.

This compressor combination can be handled in the following coupling patterns:

- Cyclical

This compressor combination can be handled in accordance with the following coupling patterns:

- Cyclical

In general, regarding handling of the capacity-regulated compressors: Cut-in

The capacity-regulated compressors with unloader valves start before one-step compressors. The capacity-controlled compressor will always be fully loaded before cutting-in of subsequent one-step compressors.

##### Cut-out

The capacity-regulated compressor will always be the last to stop. Handling of the unload valves depends on the setting of "unloader ctrl mode".

##### Unloader valves

At cyclical operation, unloader valves are used to close capacity holes from the subsequent one-step compressors.

Anti-cycle timer restrictions

In case a capacity-controlled compressor is prevented in starting due to anti-cycle timer restrictions, then the start of any subsequent one-step compressor is not allowed. The capacity-controlled compressor is started when the timer restriction has expired.

The one-step compressors will be cut in and cut out in accordance with the First-In-First-Out (FIFO) principle in order to equalize operating hours between the compressors.

*[Figurtekst: Cap. % C2.1 · C2.1 C2 C2.1 · Ss Po Pc Sd C2.1 C2 C1.1 C2 C2.1 · C2.1 C2 C1 C1 C1 C2 C2.1 · C2.1 C2 C1.1 C1.1 C2 C2.1 · C2 C2 C1 C1 C4 C4 C4 C1 C1 C2 C2.1 · C1.1 C1.1 C1.1 C1.1 C2 C2 · 10+ 10+ 20 kW 20 kW C1 C1 C1 C1 C3 C3 C3 C3 C3 C4 C4 C1 C1 C1 C2 · 10 kW 10 kW t]*

- The capacity-controlled compressor is the first to start and the last to stop.

- Operating hours are equalized between the capacity-regulated compressors

- The unload valve on the capacity-regulated compressor is used to fill capacity gaps

- Operating hours are equalized between the one-step compressors 3 and 4.

The compressors are cut in and cut out in accordance with the First-In-First-Out (FIFO) principle to equalize operating hours between compressors.

*[Figurtekst: Cap. % · Ss Po Pc Sd C2.1 · C2 C2 C2.1 · C1.1 C1.1 C1.1 C2 C2.1 · C1 C1 C1 C1 C1 C2 C2 · 20 kW 20 kW t]*

- For cyclical operation, the compressor with the fewest running hours starts (C1)

- Only when compressor C1 is completely loaded, should compressor C2 be cut in

- For cut-out, the compressor with the most operating hours should be unloaded (C1)

- When this compressor is completely unloaded, the second compressor is unloaded by one step before the main step on the completely unloaded compressor (C1) is cut out.

##### **Compressor application 5 – 1 x Speed + single step**

The controller is capable of controlling one speed-regulated compressor combined with one-step compressors of the same or different sizes.

- A speed-regulated compressor that can be of a different size than the following one-step compressors

- Up to 3 one-step compressors of the same or different capacity (depending on coupling pattern)

This compressor combination can be handled in accordance with the following coupling patterns:

- Cyclical

- Best fit

##### Handling the speed-regulated compressor.

For more information on the general handling of the speedregulated compressor, refer to section "Power pack types".

Here, the one-step compressors are of the same size.

The speed-regulated compressor is always the first to start and the last to stop.

One-step compressors should be cut in and cut out in accordance with the First-In-First-out principle in order to equalize operating hours.

The speed-regulated compressor is used to fill the capacity gaps between the one-step compressors.

- When the one-step compressor is cut in, the speed is reduced on the speed-regulated compressor (40 Hz) equivalent to the capacity of the cut-in capacity

*[Figurtekst: Ss Po Pc Sd Cap. % · 90 Hz · 80 Hz · C1 C1 · 40 Hz · 10 kW 10 kW 10 kW Start spee d C1 C3 C3 C1 30 Hz · 30 – 90 Hz Min. speed C1 C2 C2 C2 C3 C1 · t]*

- The speed-regulated compressor starts when the desired capacity equals the start speed

- The following one-step compressor with the smallest number of operating hours cuts in when the speed-regulated compressor is running at full speed (90 Hz)

- When a one-step compressor cuts in, the speed-regulated compressor reduces speed (40 Hz) equivalent to the capacity of the one-step compressor.

- The following one-step compressors with the most operating hours should be cut out when the speed-regulated compressor reaches minimum speed (30 Hz)

- When a one-step compressor is cut out, the speed-regulated compressor’s speed increases (80 Hz), equivalent to the capacity of the one-step compressor

- The speed-regulated compressor is the last compressor to be cut out when the preconditions for this are fulfilled.

##### Best fit - example:

Here, at least two of the one-step compressors are of different sizes.

The speed-regulated compressor is always the first to start and last to stop.

The capacity distributor cuts in and cuts out the one-step compressors in order to achieve the best possible capacity fit (least possible capacity jump).

The speed-regulated compressor is used to fill out the capacity gaps between the one-step compressors.

*[Figurtekst: Requested · Ss Po Pc Sd capacity % · 100 k W · 90 Hz C1 C1 80 Hz · C1 C2 C2 C1 · 30 – 90 Hz20 kW 20 kW 40 kW Start speed40 Hz C1 C1 30 Hz · Min. speed C1 C2 C3 C3 C3 C3 C2 C1 t]*

- The speed-regulated compressor starts when the desired capacity matches the start speed

- The smallest one-step compressor is cut in when the speedregulated compressor runs at full-speed (90 Hz)

- When the speed-regulated compressor again reaches max. speed (90 Hz), the smallest one-step compressor is cut out (C2) and the big one-step compressor (C3) is cut in

- When the speed-regulated compressor again reaches max. speed (90 Hz), the smallest one-step compressor (C2) is cut in again.

- The small one-step compressor is cut out when the speedregulated compressor has reached minimum speed (30 Hz)

- When the speed-regulated compressor again reaches minimum speed (30 Hz), the smallest one-step compressor (C2) is cut out and the big one-step compressor (C3) is cut in

- When the speed-regulated compressor again reaches min. speed (30 Hz), the large one-step compressor (C3) is cut out and the small one-step compressor (C2) is cut in again

- When the speed-regulated compressor again reaches min. speed (30 Hz), the small one-step compressor (C2) is cut in

- The speed-regulated compressor is the last compressor to be cut out when the requirements for this are fulfilled

- When the one-step compressor’s capacity is cut out, the speedregulated compressor increases speed (80 Hz) equivalent to the cut out capacity.

##### **Compressor application 6 – 1 x Speed + 1x unloader + single step**

The controller can operate one speed-regulated compressor and one compressor with unloader combined and multiple single step compressors of the same size.

The advantage of this combination is that the variable part of the speed-regulated compressor only needs to be large enough to cover the following unload valves in order to achieve a capacity curve without gaps.

A single speed-regulated compressor that can be of a different size than the following compressors.

A compressor with unloaders that can be of a different size and have a number of unload valves (max. 3).

The steps on the capacity-regulated compressors are of the same size . The main step and the unload valves can be different sizes, i.e. 50%, 25% and 25%.

This compressor combination can be handled in the following coupling patterns:

- Cyclical

##### Handling the speed-regulating compressor

For further information on the general handling of the speedregulated compressor, refer to section "Power pack types".

The speed-regulated compressor is always the first to start and last to stop.

The unloaded compressor is the second one to start and the second to last to stop.

The fixed step are cut in and cut out in accordance with the First-In-First-out principle in order to equalize operating hours. The speed-regulated compressor is used to fill the capacity gaps between the unload valves/main steps.

*[Figurtekst: Cap. % · Ss Po Pc Sd 90 Hz C1 C1 80 Hz · 40 Hz C1 C2.1 C2.1 C1 30 Hz · C1 C2 C2 C2 C2 C1 · 20 kW 10+ 20 kW Start spee d C1 C2.1 C2.1 C1 · 30 – 90 Hz 10kW Min. spee d C1 C2 C2 C3 C3 C3 C3 C2 C2 C1]*

The speed-regulated compressor starts when the desired capacity equals the start speed.

The main step on the capacity-regulated compressor (C2) is cut in when the speed-regulated compressor runs at full speed (90 Hz). The unload valves (C2.1) are cut in gradually as the speedregulated compressor again reaches max. speed (90 Hz).

The main step on the fixed step compressor (C3) is cut in when the speed-regulated compressor again reaches max. speed (90 Hz). The unload valves are cut in gradually as the speed-regulated compressor again reaches max. speed (90 Hz).

When the main step or unload valves are cut in, the speed is reduced on the speed-regulated compressor (40 Hz) to equivalent to the capacity of the cut in capacity.

The capacity-regulated compressor (C2) cuts out an unload valve when the speed-regulated compressor has reached min. speed (30 Hz).

- When the speed-regulated compressor again reaches min. speed (30 Hz) and when the unloader compressor have reached minimum capacity the fixed step compressor is cut out

- The unload valve cut in the capacity-regulated compressor (C2.1) to compensate for capacity gab and the variable speed adjust is capacity

- When the speed-regulated compressor again reaches min. speed (30 Hz), the capacity-regulated compressor is unloaded (C2)

- When the speed-regulated compressor again reaches min. speed (30 Hz), the main step is cut out on the capacityregulated compressor with the most operating hours (C2)

- When the speed-regulated compressor again reaches min. speed (30 Hz), the main step is cut out on the last capacityregulated compressor (C3)

- The speed-regulated compressor is the last compressor that is cut out when the conditions for this are fulfilled

##### **Compressor application 7 – 1 x Speed + unloader**

The controller can operate one speed-regulated compressor combined with several capacity-regulated compressors of the same size and with the same number of unloaders. The advantage of this combination is that the variable part of the speed-regulated compressor only needs to be large enough to cover the following unload valves in order to achieve a capacity curve without gaps.

- A single speed-regulated compressor that can be of a different size than the following compressors

- The capacity-regulated compressors are the same size and have the same number of unload valves (max. 3)

- The main step on the capacity-regulated compressors are the same size

- The main step and the unload valves can be different sizes, i.e. 50%, 25% and 25%.

This compressor combination can be handled in the following coupling patterns:

• Cyclical

The capacity-regulated compressors are cut in and cut out in accordance with the First-in-First-Out principle in order to equalize operating hours.

The speed-regulated compressor is used to fill the capacity gaps between the unload valves/main steps.

*[Figurtekst: Ss Po Pc Sd Cap.% · C1 50 Hz · 60 Hz · C1 C3.1 C1 · 20 kW 10+ 10+ 35 Hz C1 C3 C3 C3.1 C1 25 Hz · 25 – 60 Hz 10 kW 10 kW Start speed C1 C2.1 C2.1 C2.1 C3 C3 C1 · Min. speed C1 C2C2 C2 C2 C2C2 C3C1 · t]*

- The speed-regulated compressor starts when the desired capacity matches the start speed

- The main step on the capacity-regulated compressor with fewest operating hours (C1) is cut in when the speed-regulated compressor runs at full speed (60 Hz)

- The unload valves are cut in gradually as the speed-regulated compressor again reaches max. speed (60 Hz)

- The main step on the last capacity-regulated compressor (C2) is cut in  when the speed-regulated compressor again reaches max. speed (60 Hz)

- The unload valves are cut in gradually as the speed-regulated compressor again reaches max. speed (60 Hz)

- When the main step or unload valves are cut in, the speed is reduced on the speed-regulated compressor (35 Hz) to equivalent to the capacity of the cut in capacity.

- The capacity-regulated compressor with the most operating hours (C2) cuts out an unload valve when the speed-regulated compressor has reached min. speed (25 Hz)

- When the speed-regulated compressor again reaches min. speed (25 Hz), the unload valve is cut out on the next capacityregulated compressor (C3)

- When the speed-regulated compressor again reaches min. speed (25 Hz), the main step is cut out on the capacity-regulated compressor with the most operating hours (C2)

- When the speed-regulated compressor again reaches min. speed (25 Hz), the main step is cut out on the last capacityregulated compressor (C3)

- The speed-regulated compressor is the last compressor that is cut out when the conditions for this are fulfilled

- When the main step or unload valves are cut out, the speed of the speed-regulated compressor increases (50 Hz) to equivalent to the cut out capacity

##### **Compressor application 8 – 2 x Speed + single**

The controller can control two speed-regulated compressors combined with several one-step compressors that may be the same or different in size (depending on the selected coupling pattern).

The advantage of using two speed-regulated compressors is that it is then possible to reach a very low capacity, which is an advantage with low loads, while at the same time a very high variable regulating range is possible.

##### Handling the speed-regulating compressor

For further information on the general handling of the speedregulated compressor, refer to section "Power pack types".

The speed-regulated compressor is always the first to start and last to stop.

- Two speed-regulated compressors which can be of a different size than the following one-step compressors

- The speed-regulated compressors can be the same or different sizes (depending on the choice of coupling pattern)

- The same frequency band for both speed-regulated compressors

- One-step compressors of the same or different sizes (depending on the choice of coupling pattern)

This compressor combination can be handled in accordance with the following coupling patterns:

- Cyclical

- Best fit

##### Handling the speed-regulated compressor

For more information on the general handling of the speedregulated compressors, refer to section "Power pack types".

Here the speed-regulated compressors are the same size. The one-step compressors should also be the same size.

The speed-regulated compressor is always the first to start and the last to stop.

The other compressors cut in and cut out in accordance with the operating time (First-In-First-Out principle). The speed-regulated compressor is used to fill the capacity gaps between the following one-step compressors.

*[Figurtekst: Ss Po Pc Sd Cap. % · 60 Hz · C2 C2 50 Hz · 20 kW 20 kW 20 kW 20 kW 35 Hz C2 C1 C1 C2 25 Hz · C 2 C1 C4 C4 C1 · 25 – 60 Hz Start spee d C2 · Min. speed C1C1 C3 C3 C3 C4 C1 t]*

- The speed-regulated compressor with the least operating hours (C1) starts when the desired capacity equals the start speed

- The following speed-regulated compressor C2 is cut in when the first speed-regulated compressor (C1) has reached max. speed (60 Hz) so that the compressors run in parallel

- When the two speed-regulated compressors reach full speed (60 Hz) the one-step compressor with the fewest operating hours is cut in (C3)

- When the two speed-regulated compressors again reach full speed (60 Hz), the last one-step compressor cuts in (C4)

- When one-step compressors are cut in, the speed is reduced on the speed-regulated compressor (35 Hz) equivalent to the cut-in capacity.

- The one-step compressor with the most operating time (C3) is cut out when the speed-regulated compressor reaches min. speed (25 Hz)

- When the two speed-regulated compressors again reach min. speed (25 Hz), the last one-step compressor is cut out (C4)

##### Best fit - examples

Here, either the two speed-regulated compressors are of different sizes, or the following one-step compressors are of different sizes. The speed-regulated compressors are always the first to start and the last to stop.

The capacity distributor cuts in and cuts out both speed-regulated compressors and one-step compressors in order to reach the best possible capacity adjustment (least possible capacity jump).

##### Example 1

In this example, the speed-regulated compressors are of the same size and the following one-step compressors are of different sizes.

*[Figurtekst: Ss Po Pc Sd Cap. % · 90 Hz C2 C2 50 Hz · 20 kW 20 kW 20 kW 40 kW C2 C1 C1 C 2 25 Hz · 35 Hz C2 C1 C3 C3 C1 · 25 – 60 Hz C 2 · Start spee d C 2 C1 C1 C2 · Min. speed C1 C1C3 C4 C4 C4 C4 C3 C1 t]*

- The speed-regulated compressor with the least operating hours (C1) starts when the desired capacity equals the start speed

- When the first speed-regulated compressor (C1) has reached max. speed (60 Hz), the second speed-regulated compressor (C2) cuts in so that the compressors run in parallel

- When the two speed-regulated compressors reach full speed (60 Hz), the small one-step compressor (C3) is cut in

- When the two speed-regulated compressors again reach full speed (60 Hz), the large one-step compressor (C4) is cut in and the small one-step compressor (C3) is cut out

- When the two speed-regulated compressors again reach full speed (60 Hz), the small one-step compressor (C4) is cut in again

- When the one-step compressor is cut in, the speed is reduced on the speed-regulated compressor (35 Hz) corresponding to the cut-in capacity.

   - The small one-step compressor (C3) is cut out when the speedregulated compressor reaches the min. speed (25 Hz)

   - When the two speed-regulated compressors again reach min. speed (25 Hz), the big one-step compressor (C4) is cut out and the small one-step compressor (C3) is cut in

   - When the two speed-regulated compressors again reach min. speed (25 Hz), the small one-step compressor (C3) is cut out

   - When the two speed-regulated compressors again reach min. speed (25 Hz), the speed-regulated compressor with the most operating hours (C1) is cut out

   - The last speed-regulated compressor (C2) is cut out when the requirements for this are fulfilled

   - When one-step compressors cut out, the speed-regulated compressors increase speed (50 Hz), corresponding to the cutout capacity.

- When the two speed-regulated compressors again reach min. speed (25 Hz), the speed-regulated compressor with the most operating hours is cut out (C1)

- The last speed-regulated compressor (C2) is cut out when the requirements for this are fulfilled

- When one-step compressors are cut out, the speed-regulated compressors’ speed increases (50 Hz), equivalent to the cut out capacity.

##### Example 2:

In this example, the speed-regulated compressors are of different sizes and the following one-step compressors are also of different sizes.

*[Figurtekst: Ss Po Pc Sd Cap. % · 90 Hz · C2 C2 63.3 Hz · 10 kW 20 kW 20 kW 40 kW 56.7 Hz C2 C1 C1 C 2 30 Hz · 30 – 90 Hz 30 – 90 Hz 45 Hz90 HzC2 CC1 2 C1 C3 C3 C1 CC1 2 · Start speeMin. speed d C2C1C3C4 C4 C4 C4 C3 C C12 t]*

- The smallest speed-regulated compressor (C1) starts when the desired capacity equals the start speed

- When the smallest speed-regulated compressor (C1) has reached max. speed (90 Hz), the large speed-regulated compressor (C2) cuts in and the small speed-regulated compressor cuts out

   - The small one-step compressor (C3) is cut out when the speedregulated compressor reaches min. speed (30 Hz)

   - When the two speed-regulated compressors again reach min. speed (30 Hz) the big one-step compressor (C4) cuts out and the small one-step compressor (C3) cuts in

   - When the two speed-regulated compressors again reach min. speed (30 Hz), the small one-step compressor (C3) cuts out

   - When the two speed-regulated compressors again reach min. speed (30 Hz), the small speed-regulated compressor (C1) cuts out

   - When the big speed-regulated compressor reaches min. speed (30 Hz), it is cut out and the small speed-regulated compressor is cut in (C1)

   - The small speed-regulated compressor (C1) is cut out when the conditions for this are met

   - When the one-step compressors are cut out, the speedregulated compressors' speed increases (63.3 Hz) to the equivalent to the cut-out capacity.

- When the large speed-regulated compressor reaches max. speed (90 Hz), the small speed-regulated compressor (C1) cuts in again so that the compressors run in parallel

- When the two speed-regulated compressors reach full speed (90 Hz), the small one-step compressor (C3) is cut in

- When the two speed-regulated compressors again reach full speed (90 Hz), the big one-step compressor (C4) cuts in and then the small one-step compressor (C3) cuts out

- When the two speed-regulated compressors again reach full speed (90 Hz), the small one-step compressor (C3) is cut in again

- When the one-step compressors are cut in, the speed decreases on the speed-regulated compressor (56.7 Hz) corresponding to the cut-in capacity

### **5.13 Appendix B – Alarm texts**

|**Settings**|**Priority**<br>**(factory)**|**English alarm texts**|**Description**|
|---|---|---|---|
|**Suction group**||||
|Low suction pressure P0|Low|Low pressure P0|Minimum safety limit for suction pressure P0 has been exceeded|
|High suction pressure P0|High|High pressure P0|High alarm limit for P0 has been exceeded|
|Low pressure Psuc-MT|Low|Low pressure Psuc-MT|Minimum safety limit for suction pressure Psuc has been exceeded|
|High pressure Psuc-MT|High|High pressure Psuc-MT|High alarm limit for Psuc has been exceeded|
|High/Low superheat Ss|Medium|High superheat suction A|Superheat in suction line too high|
|||Low superheat section A|Superheat in suction line too low|
|Load shedding|Medium|Load Shed active|Load shedding has been activated|
|P0 sensor error|High|P0A sensor error|Pressure transmitter signal from P0is defective|
|||Psuc sensor error|Pressure transmitter signal from Psuc is defective|
|||Sgc sensor error|Temperature signal from gas cooler is defective|
|||Prec sensor error|Pressure transmitter signal from the receiver is defective|
|||Pgc sensor error|Pressure transmitter signal from the gas cooler is defective|
|||SsA sensor error|Temperature signal from Ss suction gas temp. is defective|
|||SdA sensor error|Temperature signal from Sd discharge gas temp. is defective|
|||Sc3 sensor error|Temperature signal from Sc3 air on condenser defective|
|Misc. sensor error|Medium|Heat recovery sensor error|Temperature signal from Shrec heat recovery thermostat defective|
|||Stw sensor error|Temperature signal from hot water circuit is defective|
|||Shr sensor error|Temperature signal from heat circuit is defective|
|||Saux_ sensor error|Signal from extra Temp.sensor Saux_ is defective|
|||Paux_ sensor error|Signal from extra pressure sensor Paux_ is defective|
|All compressors||||
|Common safety|High|Common compr. Safety<br>cutout|All compressors have been cut out on common safety input|
|||Comp. X oil pressure cut out|Compressor no. x has been cut out on oil pressure safety|
|Comp. 1 safety||Comp. x over current cut out|Compressor no. x has been cut out on over-current safety|
|<br>Comp. 2 safety<br>||Comp. 1 motor prot. cut out|Compressor no. x has been cut out on motor protection safety|
|Comp. 3 safety<br>_________________|Medium|Comp. 1 disch. Temp cut out|Compressor no. x has been cut out on discharge temperature safety|
|Comp. x safety||Comp. 1 disch. Press. Cut out<br>Comp. 1 General safety cut<br>out|Compressor no. x has been cut out on discharge pressure safety<br>Compressor no. x has been cut out on general safety|
|VSD safety|Medium|Comp. 1 FCD safety error|Variable speed drive for comp. x has been cut out on safety|
|Separator alarms|Medium|Low oil in separator x|Oil level too low in separator x|
|||No oil separated sep. x|No oil in oil separator x|
|||To high oil in separator x|Oil level too high in separator x|
|||Remaining oil separator x|Separator x can not be emptied completely for oil|
|Receiver alarm||Oil recv. high level|Oil level too high in receiver|
||Medium|Oil recv. low level|Oil level is too low in receiver|
|Rec. high pressure|Medium|Recv. High pressure alarm|Pressure too high in receiver|
|Rec. low pressure|Medium|Recv. Low pressure alarm|Pressure too low in receiver|
|Rec. High liquid level|High|Rec. High liquid level alarm|Liquid level too high in the receiver|
|Rec. Low liquid level|High|Rec. Low liquid level alarm|Liquid level too low in the receiver|
|**Condensor**||||
|High Sd temp.|High|High disch. temp. SdA|Safety limit for discharge temperature has been exceeded|
|High  Pc pressure|High|High pressure Pc|High safety limit for condensing pressure Pc has been exceeded|

|Pc/S7 Sensor error|High|PcA sensor error|Pressure transmitter signal from Pc is defective|
|---|---|---|---|
|||S7A sensor error|Temperature signal for S7 medium temperature sensor is defective|
|||Fan Alarm 1|Fan  no. X is reported defective via safety input|
|Fan/VSD safety|Medium|Fan VSD alarm|Variable speed drive for condenser fans has been cut out on safety|
|**Various alarms**||||
|Standby mode|Medium|Control stopped,<br>MainSwitch=OFF|The control has been stopped via the setting ”Main switch” = Off or  the<br>external Main switch is off|
|Thermostat x – Low temp.<br>alarm|Low|Thermostat x - Low alarm|The temperature for thermostat no. x has been below the low alarm limit for<br>longer time than set delay|
|Thermostat x – High temp.<br>alarm|Low|Thermostat x - High alarm|The temperature for thermostat no. x has been above the high alarm limit<br>for longer time than set delay|
|Pressostat x – Low pressure<br>alarm|Low|Pressostat x - Low alarm|The pressure for pressostat no. x has been below the low alarm limit for<br>longer time than set delay|
|Pressostat x – alarm limit<br>high pressure|Low|Pressostat x - High alarm|The pressure for pressostat no. x has been above the high alarm limit for<br>longer time than set delay|
|Voltage input x – Low alarm|Low|Analogue input x - Low alarm|The voltage signal has been below the low alarm limit for longer time than<br>set delay|
|Voltage input x – High<br>alarm|Low|Analogue input x - High alarm|The voltage signal has been above the high alarm limit for longer time than<br>set delay|
|User def. alarm text|Low|Custom alarm x -define text|Alarm on general  alarm input DI x|
|No flow|High|Flow switch alarm|There is no flow in the heating circuit. Check the pump|
|Boiling alarm|High|Boiling alarm|The temperature in the heat circuit is too high|
|Receiver alarm|High|Prec...|Alarm from the receiver|
|External power loss|High|External power loss|Supply is interrupted. A message alert. All other alarms stopped.|
|Steppervalve|High|Stepper - Vhp, Vrec, PI, Vliq.<br>Open coil, Shorted output,<br>Error, Power failure|Check the supply to the current valve.<br>In the event of an error or power failure: check the supply to the stepper<br>module.|
|**System alarms**||||
|The alarm priority can not be|altered on|system alarms||
|Control mode|Low|Manual comp. cap. Control A|Compressor's capacity control runs i manual mode|
|Control mode|Low|Manual cond. cap. Control A|Condense capacity control runs i manual mode|
||Medium|Time has not been set|Time has not been set|
||Medium|System Critical exception|An unrecoverable critical system failure has occurred – exchange the<br>controller|
||Medium|System alarm exception|A minor system failure has occurred – power off controller|
||Medium|Alarm destination disabled|When this alarm is activated, the alarm transmission to the alarm receiver<br>has been deactivated.  Check and wait.<br>When the alarm is cleared the alarm transmission to the alarm receiver has<br>been activated again|
||Medium|Alarm route failure|Alarms cannot be transmitted to alarm receiver – check communication|
||High|Alarm router full|The internal alarm buffer has an overrun – this might occur if the control-<br>ler cannot send the alarms to the alarm receiver. Check communication<br>between controller and system unit|
||Medium|Device is restarting|The controller is restarting after flash updating of the software|
||Medium|Common IO Alarm|There is a communication fault between the controller module and the<br>extension modules – the fault must be corrected as soon as possible|
|**Manual control**||||
||Low|MAN CONTROL|The function in question has been put in manual control mode via the AK-<br>ST 500 Service Tool software|
||Low|Man set ....|The output in question has been put in manual control mode via the AK-ST<br>500 Service Tool software|
||Low|Man control .....|The output in question has been put in manual control mode via the AK-ST<br>500 Service Tool software|

##### **Installation considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown.

Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation, for example, could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss will not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer's responsibility to check the installation thoroughly, and to fit the necessary safety devices.

Special reference is made to the necessity of signals to the controller when the compressor is stopped and to the need of liquid receivers before the compressors.

Your local Danfoss agent will be pleased to assist with further advice, etc.

---

## 2. Strategy for heat recovery on CO2 transcritical rack – Programming Guide (engelsk)

*Kilde: Danfoss-dokument AU479234099123en-000101. Strategi og opsætning af varmegenvinding på CO2-transkritisk anlæg med pack controller.*

#### **Programming Guide**

### **Strategy for heat recovery on CO2 transcritical rack (Pack Control)**

**1. In Pack Controller** A. Heat reclaim request can be based on a number of user selected options including:

   - heat exchanger outlet temp

   - heat exchanger inlet/outlet TD

   - fluid temperature

   - B. Once there is a call for heat reclaim based on the above, 3-way modulating valve is energized as long as safety conditions are met:

   - Flow switch, if used, confirms proper flow

   - temp sensors on heat exchanger inlet/outlet, fluid temp, and CO2 discharge line after 3-way valve all measure below boiling (212 °F).

   - C. ‘HP offset’. with heat reclaim valve energized, control of condensation pressure can be altered based on a 0 – 10 V signal into the pack controller.

   - during heat reclaim and a signal of 0 V, pressure target is increased to setting for ‘gas cooler-heat recovery minimum pressure’

   - during heat reclaim and a signal of 10 V, pressure target is increased to setting for ‘gas cooler heat recovery offset pressure’

   - during heat reclaim and a signal between 0 – 10 V, pressure target is increased linearly to a value that corresponds to range between min pressure and offset pressure.

   - in the event multiple 0 – 10 V sources are being used (up to 5), maximum voltage signal will be used for control signal.

   - D. ‘Max heat reclaim’. the following control occurs within the pack controller

   - during heat reclaim and a signal of 0 – 2.5 V, pressure target is increased to setting for ‘gas cooler heat recovery minimum pressure’

   - during heat reclaim and a signal of 7 V, pressure target is increased to setting for ‘gas cooler heat recovery offset pressure’

   - during heat reclaim and a signal between 2.5 – 7 V, pressure target is increased linearly to a value that corresponds to range between min pressure and offset pressure.

   - during heat reclaim and a signal between 6.5 – 8 V, gas cooler fan capacity is decreased proportionally (voltage increase results in larger capacity decrease). At 8 V or greater, gas cooler fans are disabled.

   - if piping exists, valve to fully bypass gas cooler for maximum recovery can be utilized. Bypass would occur at a voltage signal of 9.5 V. Bypass valve would be disabled once voltage signal drops below 8 V.

**2. In EMS controller** A. 0 – 10 V signal(s) generated based on desired amount of heat reclaim, signal(s) sent to pack controller.

---

## 3. Sharing a ratiometric pressure transmitter between controllers – Operating Guide (engelsk)

*Kilde: Danfoss-dokument AQ470237575633en-000201. Om ét ratiometrisk tryktransmitter-signal kan deles mellem flere Danfoss-regulatorer.*

### **Operating Guide**

Is it possible to share the same ratiometric pressure transmitter with more than one Danfoss controller?

*[Figurtekst: More than one AK-CC55 Pressure · (Yes, it is possible) transmitter · 1 3 2 · 40 41 42 40 41 42 · Vdc s Vdc s · AK-CC55 AK-CC55]*

*[Figurtekst: The signal from one pressure transmitter can be shared by up to 10 controllers. More details in the · User Guide of the AK-CC55: · AKS 32R info AKS 32R · out · The signal from one pressure transmitter can be · received by up to 10 controllers. · There must not be a significant pressure drop · from the pressure transmitter's position in the · suction line to the individual evaporators. · One AK-CC 750A and Pressure · AK-CC55 transmitter · (Possible, but not  1 3 2 · recommended) · 28 25 26 40 41 42 40 41 42 · Vdc s Vdc s Vdc s · x3 · AK-CC55 AK-CC55 AK-CC55 · Black Brown Blue]*

The signal from one pressure transmitter can be received from up to 5 controllers. For example: 1x AK-CC 750A and 4x AK-CC55.

**Limitation** : Electrically it´s possible to share the pressure transmitter, and the signal is displayed correctly, but this is not recommended by Danfoss. In case an AK-CC750A unit is disconnected or loses supply voltage, this unit will affect the pressure signal.

The signal from the pressure sensor may change only slightly, so the system still sees the signal as valid.

**AK2 platform controllers with AK-XM extension modules** (Possible, but not recommended)

*[Figurtekst: Pressure · transmitter · 1 3 2 · 28 25 26 5V S GND 5V S GND · Vdc s · AK-PC 782A CM XM XM CM XM XM]*

If all controllers have **separated power supply** , it is possible to connect more than one controller to one pressure transmitter.

**Limitation** : Electrically it´s possible to share the pressure transmitter, and the signal is displayed correctly. Up to 10 AK2 units can share the signal from a pressure transmitter, but this is not recommended by Danfoss. In case an AK2 unit is disconnected or loses supply voltage, this unit will affect the pressure signal. The signal from the pressure sensor may change only slightly, so the system still sees the signal as valid. If third party controllers are involved, then Danfoss is not responsible for the installation of the pressure transmitters sharing. **MCX controllers** No, MCX controllers are not designed to share sensors with a physical connection. (Not recommended) The recommendation is to use the CANBus to share the sensor data reading with other controllers. **AK2 platform controllers** No, AK2 platform controllers are not designed to share sensors with physical connection with devices **with different platforms (AK2** based on other platforms. **x MCX or AK2 x Alsmart or Alsmart x MCX)** (Not recommended) **Appendix** For more informations on pressure transmitters sharing, check other documents: Title: Transmitter fault detection for AK-XM 101A, AK-XM 205A, AK-XM 205B Document ID : RI8HZ552 Title: Transmitter fault detection for AK..., ECL..., ECA... Document ID : RI8HZ452
