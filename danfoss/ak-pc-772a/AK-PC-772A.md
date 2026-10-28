# Danfoss AK-PC 772A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Pack controller Type AK-PC 772A

*Kilde: Danfoss-dokument BC186686443705en-000201.pdf*

#### **User Guide**

Pack controller Type **AK-PC 772A**

Capacity controller for transcritical CO2 booster control **SW Ver. 1.5x**

**www.danfoss.com**

|**1. Introduction**...............................................................................................**3**|
|---|
|1.1 Application ..........................................................................................3|
|1.2 Principles .............................................................................................4|
|**2. Design of a controller**.............................................................................**7**|
|2.1 Module survey ...................................................................................7|
|2.2 Common data for modules ...........................................................9|
|2.3 Dimensions .........................................................................................9|
|2.3 Controller ...........................................................................................10|
|2.3.1 Extension module AK-XM 101A ...................................12|
|2.3.2 Extension module AK-XM 102A / AK-XM 102B ......14|
|2.3.3 Extension module AK-XM 103A ...................................16|
|2.3.4 Extension module AK-XM 204A / AK-XM 204B ......18|
|2.3.5 Extension module AK-XM 205A / AK-XM 205B ......20|
|2.3.6 Extension module AK-XM 208C ...................................22|
|2.3.7 Extension module AK-OB 110 ......................................24|
|2.3.8 Extension module EKA 163A / EKA 164A .................25|
|2.3.9 Graphic display MMIGRS2 .............................................25|
|2.3.10 Power supply module|
|AK-PS 063 STEP3 / 130 STEP3 / 250 STEP3 ...............26|
|2.3.11 Communication module AK-CM 102 .........................27|
|2.4 Preface to design ............................................................................28|
|2.4.1 Functions .............................................................................28|
|2.4.2 Connections ........................................................................29|
|2.4.3 Limitations...........................................................................29|
|2.5 Design of a compressor and condenser control .................30|
|2.5.1 Procedure ............................................................................30|
|2.6 Ordering .............................................................................................38|
|**3. Mounting and wiring**..........................................................................**39**|
|3.1 Mounting of analog output module .......................................39|
|3.2 Mounting of extension module on the basic module ......40|
|3.3 Wiring  .................................................................................................41|
|**4. Configuration and operation**..........................................................**44**|
|4.1 Configuration ...................................................................................44|
|4.1.1 Connect PC..........................................................................44|
|4.1.2 Authorization .....................................................................46|
|4.1.3 Unlock the configuration of the controllers ............47|

|4.1.4 System set-up .....................................................................48|
|---|
|4.1.5 Set plant type .....................................................................49|
|4.1.6 Set control of MT compressors ....................................50|
|4.1.7 Set control of LT compressors ......................................54|
|4.1.8 Setup control of condenser fans .................................54|
|4.1.9 Setup control of high pressure ....................................56<br>|
|4.1.10 Setup control of receiver pressure..............................57|
|4.1.11 Setup control of  heat recovery ...................................58|
|4.1.12 Setup Display .....................................................................59|
|4.1.13 Setup Functions for General purpose .......................60|
|4.1.14 Configuration of inputs and outputs ..........................64|
|4.1.15  Set alarm priorities ...........................................................66|
|4.1.16  Lock configuration ...........................................................68|
|4.1.17  Check configuration ........................................................69|
|4.2 Check of connections ....................................................................71|
|4.3 Check of settings.............................................................................73|
|4.4 Schedule function ..........................................................................75|
|4.5 Installation in network ..................................................................76|
|4.6 First start of control ........................................................................77|
|4.6.1 Start the control ................................................................78|
|4.6.2 Manual capacity control .................................................79|
|**5. Regulating functions**...........................................................................**80**|
|5.1 Suction groups ................................................................................80|
|5.1.1 Controlling sensor ............................................................80|
|5.1.2 Reference .............................................................................80|
|5.1.3 Capacity control of compressors .................................81|
|5.1.4 Safety functions .................................................................90|
|5.2 Condenser / Gas cooler ................................................................92|
|5.2.1 Capacity control of condenser .....................................92|
|5.2.2 Reference for condensing pressure ...........................92|
|5.2.3 Heat recovery .....................................................................94|
|5.2.4 Capacity distribution .......................................................96|
|5.2.5 Circuits for control of CO2 gas pressure ....................98|
|5.3 General monitoring functions ................................................101|
|5.4 Miscellaneous ...............................................................................103|
|5.5 Appendix - Alarm texts ..............................................................107|

2 | BC186686443705en-000201

### **1. Introduction**

### **1.1 Application**

AK-PC 772A is complete regulating units for capacity control of compressors and gas cooler in a small CO2 refrigeration systems. Either as a compressor and condenser control on MT or as a booster system. There can be regulated with one parallel compressor.

The controller is with oil management, heat recovery function and CO2 gas pressure control.

In addition to capacity control the controllers can give signals to other controllers about the operating condition, e.g. forced closing of expansion valves, alarm signals and alarm messages.

The controller’s main function is to control compressors and gas cooler so that operation all the time takes place at the energyoptimum pressure conditions. Both suction pressure and gas pressure are controlled by signals from pressure transmitters and temperature sensors.

Among the different functions are:

- Capacity control of up to 3 compressors on high pressure (2 if also regulating with parallel compressor).

- Capacity control of up to 2 compressors on low pressure

- Up to 3 unloaders for each compressor

- Speed control of one or two compressors

- Up to 6 safety inputs for each compressor

- Option for capacity limitation to minimize consumption peaks

- When the compressor does not start, signals can be transmitted to other controllers so that the electronic expansion valves will be closed

- Control of liquid injection into suction line

- Safety monitoring of high pressure / low pressure / discharge temperature

- Capacity control of up to 4 fans

- Floating gas cooler reference with regard to outside temperature

- Heat recovery function

- CO2 gas cooler control and receiver control

- Parallel compression on transcritical CO2 system

- Step coupling, speed regulation or a combination

- Safety monitoring of fans

- The status of the outputs and inputs is shown by means of lightemitting diodes on the front panel

- Alarm signals can be generated via data communication

- Alarms are shown with texts so that the cause of the alarm is easy to see.

- Plus some completely separate functions that are totally independent of the regulation – such as alarm, thermostat, pressure and PI-regulating functions.

### **1.2 Principles**

The great advantage of this series of controllers is that it can be extended as the size of the plant is increased. It has been developed for refrigeration control systems, but not for any specific application – variation is created through the read-in software and the way you choose to define the connections. It is the same modules that are used for each regulation and the composition can be changed, as required. With these modules (building blocks) it is possible to create a multitude of various kinds of regulations. But it is you who must help adjusting the regulation to the actual needs – these instructions will assist you to find your way through all the questions so that the regulation can be defined and the connections made.

##### **Advantages**

- The controller’s size can “grow” as systems grow

- The software can be set for one or more regulations

- Several regulations with the same components

- Extension-friendly when systems requirements are changed

- Flexible concept:

- Controller series with common construction

- One principle – many regulation uses

- modules are selected for the actual connection requirements

- The same modules are used from regulation to regulation.

*[Figurtekst: Controller Extension modules · Top part · Bottom part · The controller is the cornerstone of the regulation. The module has inputs and  If the system grows and more functions have to be controlled, the regulation can be · outputs capable of handling small systems. extended. · • The bottom part – and hence the terminals – are the same for all controller types. With extra modules more signals can be received and more relays cut in and out – · • The top part contains the intelligence with software. This unit will vary according to  how many of them – and which – is determined by the relevant application. · controller type. But it will always be supplied together with the bottom part. · • In addition to the software the top part is provided with connections for data com- · munication and address setting. · Examples A regulation with few connections can  If there are many connections one or more · be performed with the controller module  extension modules have to be mounted · alone]*

4 | BC186686443705en-000201

##### **Direct connection**

Setup and operation of an AK controller must be accomplished via the “AK-Service Tool” software program.

The program is installed on a PC, and setup and operation of the various functions are carried out via the controller’s menu displays.

##### **Displays**

The menu displays are dynamic, so that different settings in one menu will result in different setting possibilities in other menus.

A simple application with few connections will give a setup with few settings.

A corresponding application with many connections will give a setup with many settings.

From the overview display there is access to further displays for the compressor regulation and the condenser regulation. At the bottom of the display there is access to a number of general functions, such as “time table”, “manual operation”, “log function”, “alarms”, and “service” (configuration).

##### **Network linking**

The controller can be linked up into a network together with other controllers in an ADAP-KOOL® refrigeration control system. After the setup operation can be performed at a distance with, say, our software program type AKM.

##### **Users**

The controller comes supplied with several languages, one of which can be selected and employed by the user. If there are several users, they may each have their choice of language. All users must be assigned a user profile which either gives access to full operation or gradually limits the operation to the lowest level that only allows you “to see”.

Language selection is part of the service tool settings. If the language selection is not available in the service tool for the current regulator, English texts will be displayed.

##### **External display**

An external display can be fitted in order for P0 (Suction) and Pc (Condensing) readings to be displayed.

A total of 4 displays can be fitted and with one setting it is possible to choose between the following readings: suction pressure, suction pressure in temperature, Ss, Sd, condenser pressure, condenser pressure in temperature, gas cooler temperature, etc. A graphical display with control buttons can also be fitted.

A number of light-emitting diodes makes it possible to follow the signals that are received and transmitted by the controller.

##### **Log**

From the log function you can define the measurements you wish to be shown.

The collected values can be printed, or you may export them to a file. You can open the file in Excel.

If you are in a service situation you can show measurements in a trend function. The measurements are then made real-time and displayed instantly.

##### **Alarm**

The display gives you an overview of all active alarms. If you wish to confirm that you have seen the alarm you can cross it off in the acknowledge field.

If you want to know more about a current alarm you can click on it and obtain an information display on the screen.

A corresponding display exists for all earlier alarms. Here you can upload information if you need further details about the alarm history.

*[Figurtekst: n Power Slow flash = OK · n Comm Quick flash = answer from gateway · n DO1  n Status Constantly ON = error · n DO2  n Service Tool Constantly OFF = error · n DO3  n LON · n DO4  n I/O Extension · n DO5  n Alarm Flash = active alarm/not cancelled · n DO6  n Constant ON = Active alarm/cancelled · n DO7  n Display · n DO8  n Service Pin]*

6 | BC186686443705en-000201

### **2. Design of a controller**

This section describes how the controller is designed. The controller in the system is based on a uniform connection platform where any deviations from regulation to regulation is determined by the used top part with a specific software and by which input and output signals the relevant application will require. If it is an application with few connections, the controller

module (top part with belonging bottom part) may be sufficient. If it is an application with many connections it will be necessary to use the controller module plus one or more extension modules. This section will give you a survey of possible connections plus assistance in selecting the modules required by your actual application.

### **2.1 Module survey**

- Controller module – capable of handling minor plant requirements.

- Extension modules. When the complexity becomes greater and additional inputs or outputs are required, modules can be attached to the controller. A plug on the side of the module will transmit the supply voltage and data communication between the modules.

- Top part

- The upper part of the controller module contains the intelligence. This is the unit where the regulation is defined and where data communication is connected to other controllers in a bigger network.

•  Connection types There are various types of inputs and outputs. One type may, for example, receive signals from sensors and switches, another may receive a voltage signal, and a third type may be outputs with relays etc. The individual types are shown in the table below.

- Optional connection

When a regulation is planned (set up) it will generate a need for a number of connections distributed on the mentioned types. This connection must then be made on either the controller module or an extension module. The only thing to be observed is that the types must not be mixed (an analog input signal must for instance not be connected to a digital input).

- Programming of connections

- The controller must know where you connect the individual input and output signals. This takes place in a later configuration where each individual connection is defined based on the following principle:

- to which module

- at which point (”terminals”)

- what is connected (e.g. pressure transmitter/type/pressure range).

*[Figurtekst: Extension module with addi- · tional relay outputs and additional · analog inputs. · Extension module with · additional analog inputs · External display for  Bottom part · suction pressure etc. · Controller with analog inputs and · relay outputs. · Top part · The module with additional relay outputs is also available in · a version where the top part is provided with change-over · switches so that the relays can be overridden. · Extension module with · 2x analog output signals · If the row of modules needs to be · interrupted due to length or external · positioning, a communication · module should be used. · © Danfoss | Climate Solutions | 2024.01 BC186686443705en-000201 | 7]*

|1. Controller|||
|---|---|---|
|**Type**|**Function**|**Application**|
|AK-PC 772A|Controller for capacity control of a small CO2 plant with booster.<br>A maximum of 3 compressors for high pressure, 2 for low pressure,<br>4 fans and a maximum of 120 inputs/outputs|Transcritical CO2 Booster control. Parallel com-<br>pression /Heat recovery / CO2gas pressure|

|2. Extension m|odules and surveyof|inputs and|outputs||||||
|---|---|---|---|---|---|---|---|---|
|**Type**|**Analog**<br>**inputs**|**On/Off out**|**f puts**|**On/off suppl**<br>**(DI signal)**|**f y voltage**|**Analog**<br>**outputs**|**Stepper**<br>**output**|**Module with**<br>**switches**|
||For sensors, pres-<br>sure transmitters<br>etc.|Relay<br>(SPDT)|Solid state|Low voltage<br>(max. 80 V)|High voltage<br>(max. 260 V)|0 – 10 V DC|For valves<br>with step<br>control|For override of<br>relay outputs|
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

The following extension module can be placed on the PC board in the controller module. There is onl y room for one module. AK-OB 110 2

##### 3. AK operation and accessories

|**Type**|**Function**|**Application**|
|---|---|---|
|**Operation**|||
|AK-ST 500|Software for operation of AK controllers|AK-operation|
|-|Cable between PC and AK controller|USB A-B(standard IT cable)|
|**Accessories**|**Power supply module 24 V DC**||
|AK-PS 063 STEP3|15 VA||
|AK-PS 130 STEP3|30 VA|Supply for controller|
|AK-PS 250 STEP3|60 VA||
|**Accessories**|**External display that can be connected to the controller mod**|**ule. For showing, say, the suctionpressure**|
|EKA 163A|Display||
|EKA 164A|Display with operation buttons||
|MMIGRS2|Graphic display with operation||
||Cable between display and controller|Length = 2 m, 6 m|
|-|Cable between graphic display and controller|Length = 1.5 m, 3 m|
|**Accessories**|**Communication modules for controllers where modules cann**|**ot be connected continuously**|
|AK-CM 102|Communication module|Data communication for external extension<br>modules|

On the following pages there is data specific to each module.

8 | BC186686443705en-000201

### **2.2 Common data for modules**

|Supplyvoltage|24 V d.c./a.c.  +/- 20%||
|---|---|---|
|Power consumption|AK-__ (controller)|8 VA|
||AK-XM 101,102,107,AK-CM 102|2 VA|
||AK-XM 204,205,208|5 VA|
|Analog inputs|Pt 1000 ohm /0°C|Resolution: 0.1°C<br>Accuracy: +/- 0.5°C<br>+/- 0,5°C between -50°C and +50°C<br>+/- 1°C between -100°C and -50°C<br>+/- 1°C between +50°C and +130°C|
||Pressure transmitter type AKS 32R / AKS<br>2050<br>AKS 32(1 – 5 V)|Resolution:1 mV<br>Accuracy +/- 10 mV<br>Max. connection of 5 pressure transmitters on one module|
||Other pressure transmitter:<br>Ratiometric signal<br>Min. and Max.pressure must be set||
||Voltage signal 0 – 10 V||
||Contact function (On/Off)|On at R < 20 ohm<br>Off at R > 2K ohm<br>(Gold -plated contacts not necessary)|
|On/off supply voltage inputs|Low voltage<br>0 / 80 V AC/AC|Off: U < 2 V<br>On: U > 10 V|
||High voltage<br>0 / 260 V AC|Off: U < 24 V<br>On: U > 80 V|
|Relay outputs|AC-1(ohmic)|4 A|
|SPDT|AC-15(inductive)|3 A|
||U|Min. 24 V<br>Max. 230 V<br>Low and high voltage must not be connected to the same<br>outputgroup|
|Solid state outputs|Can be used for loads that are cut in and<br>out frequently, e.g. :<br>Fans and AKV valves|Max. 240 V a.c. , Min. 48 V a.c.<br>Max. 0,5 A,<br>Leak < 1 mA<br>Max. 1 AKV|
|Stepper outputs|Used for valves with stepper input|20 – 500 step/s<br>Separate supplyto  stepper outputs : 24 a.c./d.c. / xx VA|
|Ambient temperature|Duringtransport|-40 – +70 °C|
||During operation|-20 – +55 °C ,<br>0 – 95% RH (non condensing)<br>No shock influences / vibrations|
|Enclosure|Material|PC / ABS|
||Density|IP10,VBG 4|
||Mounting|For mountingonpanel wall or DIN rail|
|Weight with screw terminals|Modules in 100- / 200- / controller-series|Ca. 200g/ 500g/ 600g|
|Approvals|EU low voltage directive and EMC require-<br>ments are complied with|LVD tested according to EN 60730<br>EMC tested<br>Immunity according to EN 61000-6-2<br>Emission accordingto EN 61000-6-3|
||UL 873,|UL file number: E166834 for XM and CM-modules<br>UL file number: E31024 for PC-modules|

The mentioned data applies to all modules.

If data is specific, this is mentioned together with the module in question.

### **2.3 Dimensions**

The module dimension is 72 mm. Modules in the 100-series consist of one module Modules in the 200-series consist of two modules Controllers consist of three modules The length of an aggregate unit = n x 72 + 8

### **2.3 Controller**

There are several controllers in the series. The function is determined by the programmed software, but outwardly the controllers are identical – they all have the same connection possibilities: 11 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

8 digital outputs, with 4 Solid state outputs and 4 relay outputs

24 V a.c. or d.c. to be connected to the controller.

The 24 V must **not** be retransmitted and used by other controllers as it is not galvanically separated from inputs and outputs. In other words, you **must** use a transformer for each controller. Class II is required. The terminals must **not** be earthed.

The supply voltage to any extension modules is transmitted via the plug on the right-hand side.

The size of the transformer is determined by the power requirement of the total number of modules.

The supply voltage to a pressure transmitter can be taken either from the 5 V output or from the 12 V output depending on transmitter type.

##### **Data communication**

If the controller is to be included in a system, communication must take place via the LON connection. The installation has to be made as mentioned in the separate instructions for LON communication.

##### **Address setting**

When the controller is connected to a gateway type AKA 245, the controller’s address must be set between 1 and 119. (If it is a system manager AK-SM .., then 1-999).

##### **Service PIN**

When the controller is connected to the data communication cable the gateway must have knowledge of the new controller. This is obtained by pushing the key PIN. The LED “Status” will flash when the gateway sends an acceptance message.

##### **Operation**

The configuration operation of the controller must take place from the software program “Service Tool”. The program must be installed on a PC, and the PC must be connected to the controller via the USB-B plug on the front of the unit.

There are two rows with LED’s. They mean: Left row:

- Voltage supply to the controller

*[Figurtekst: 24 V · OK · 24 V · PIN · Address · Keep the safety · distance! · Low and high · voltage must not · be connected to · the same output · group · n Power Slow flash = OK · n Comm Quick flash = answer from gateway · n DO1  n Status Constantly ON = error · n DO2  n Service Tool Constantly OFF = error · n DO3  n LON · n DO4  n I/O Extension · n DO5  n Alarm Flash = active alarm/not cancelled · n DO6  n Constant ON = Active alarm/cancelled · n DO7  n Display · n DO8  n Service Pin]*

A small module (option board) can be placed on the bottom part of the controller. The module is described later in the document.

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

Right row:

- Software status (slow flash = OK)

- Communication with Service Tool

- Communication on LON

- Communication with AK-CM 102

- Alarm when LED flashes

- 1 LED that is not used

- Communication with display on RJ11 plug

- “Service Pin” switch has been activated

10 | BC186686443705en-000201

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 9 10 11 Terminal 15 & 27: · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 AI9 AI10 AI11 12 V max. 100 mA in total. · Terminal 16 & 28: · 5 V max. 100 mA in total. · Terminal · Analog · inputs 17, 18, 29, 30: · on 1 - 11 (Cable screen) · The screen on the · pressure transmitter · cables must only be · connected at the end of · the controller. · Solid state outputs  Relay outputs on · on 12 - 15 16 - 19 · Relay or AKV coil · 24 and 25 used · fx 230 V a.c. · only when "Op- · tion board fitted" · Point 12 13 14 15 16 17 18 19 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Signal · type · S · Ss · Pt 1000 ohm/0°C Sd · SIG · Shr Pt 1000 · Sgc · GND Sc3 · Saux_ · P · 3: Brown · AKS 32R · 2: Blue AKS 32R / · P0 AKS 2050/ · 1: Black Pc MBS 8250 · Pgc -1 - xx bar · Prec · 3: Brown Paux AKS 32 · AKS 32 -1 - zz bar · 2: Black · 1: Red Signal Module Point  Terminal Signal type /Active at · 1  (AI 1) 1 - 2 · U 0 - 5 V · ... 0 - 10 V 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · On/Off Ext. · Main  Active at: 5  (AI 5) 9 - 10 · switch · Day/ Closed 6  (AI 6) 11 - 12 · Night / 7  (AI 7) 13 - 14 · Door · Level  Open 8  (AI 8) 19 - 20 · switch · 9  (AI 9) 21 - 22 · DO Active at: · 10  (AI 10) 23 - 24 · On · / 1  11  (AI 11) 25 - 26 · AKVComp Off 12  (DO 1) 31 - 32 · Fan · Alarm 13  (DO 2) 33 - 34 · Solenoid  14  (DO 3) 35 - 36 · valve · 15  (DO 4) 37 - 38 · 16  (DO 5) 39 - 40- 41 · 17  (DO6) 42 - 43 - 44 · Option Board Please see the signal · on the page with the  18  (DO7) 45 - 46 - 47 · module. · 19  (DO8) 48 - 49 - 50 · 24  - · 25  - · AKV]*

### **2.3.1 Extension module AK-XM 101A**

The module contains 8 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

Supply voltage to a pressure transmitter can be taken from either the 5 V output or the 12 V output depending on transmitter type.

Only the two top LED’s are used. They indicate the following:

- Voltage supply to the module

- Communication with the controller is active (red = error)

12 | BC186686443705en-000201

*[Figurtekst: Point Point 1 2 3 4 · Type AI1 AI2 AI3 AI4 · Terminal 9 & 15: · 12 V max. 100 mA in total. · At the top the  Terminal 10 & 16: · signal input is  5 V max. 100 mA in total. · the left of the · two terminals. Terminal · 11, 12, 13, 14: · (Cable screen) · The screen on the pressure · transmitter cables must · At the bottom  only be connected at the · the signal input  end of the controller. · is the right of the · two terminals. · Point 5 6 7 8 · Signal Signal  Type AI5 AI6 AI7 AI8 · type · S · Ss · Pt 1000 ohm/0°C Sd · SIG Shr Pt 1000 · Sgc · Sc3 · Saux_ · GND · P · AKS 32R · 3: Brown · 2: Blue AKS 32R / · AKS 2050/ · 1: Black P0 MBS 8250 · Pc · -1 - xx bar · Pgc · AKS 32 Prec · 3: Brown Paux AKS 32 · -1 - zz bar · 2: Black · 1: Red · U · Signal Module Point Terminal Signal type / · Active at · 0 - 5 V · ... 0 - 10 V 1  (AI 1) 1 - 2 · 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · On/Off Ext.  Active at: 4  (AI 4) 7 - 8 · Main · switch Closed 5  (AI 5) 17 - 18 · Day/ / · Night Open 6  (AI 6) 19 - 20 · Door · Level  7  (AI 7) 21 - 22 · switch · 8  (AI 8) 23 - 24]*

### **2.3.2 Extension module AK-XM 102A / AK-XM 102B**

The module contains 8 inputs for on/off voltage signals.

##### **Signal**

AK-XM 102A is for low voltage signals. AK-XM 102B is for high voltage signals.

They indicate:

- Voltage supply to the module

- Communication with the controller is active (red = error)

- Status of the individual inputs 1 to 8 (when lit = voltage)

   - When using pressure transmitters connected to extension modules, it's recommended to connect the enclosed 47 kΩ resistor to ensure proper detection of any sensor errors. For more information, refer to the Danfos s RI8HZ552 m anual.

*[Figurtekst: AK-XM 102A AK-XM 102B · Max. 24 V Max. 230 V · On/Off: On/Off: · On: DI > 10 V a.c. On: DI > 80 V a.c. · Off: DI <  2 V a.c. Off: DI < 24 V a.c.]*

14 | BC186686443705en-000201

*[Figurtekst: Point Point 1 2 3 4 · Type DI1 DI2 DI3 DI4 · Point 5 6 7 8 · Type DI5 DI6 DI7 DI8 · Signal Active at · DI Ext. · Main · switch · AK-XM 102A: Max. 24 V · AK-XM 102B: Max. 230 V · Day/ Closed · Night · (voltage on) · Comp. / · safety 1 · Open · Comp. · (voltage off) · safety 2 · Level · switch · (The module can not register a pulse signal from e.g. a · reset function.) · Signal Module Point Terminal Active at · 1  (DI 1) 1 - 2 · 2  (DI 2) 3 - 4 · 3  (DI 3) 5 - 6 · 4  (DI 4) 7 - 8 · 5  (DI 5) 9 - 10 · 6  (DI 6) 11 - 12 · 7  (DI 7) 13 - 14 · 8  (DI 8) 15 - 16]*

### **2.3.3 Extension module AK-XM 103A**

The module contains :

4 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

4 analog voltage outputs of 0 - 10 V

Supply voltage to a pressure transmitter can be taken from either the 5 V output or the 12 V output depending on transmitter type.

##### **Galvanic isolation**

The inputs are galvanically separated from the outlets. The outlets AO1 and AO2 are galvanically separated from AO3 and AO4.

Only the two top LED’s are used. They indicate the following:

- Voltage supply to the module

- Communication with the controller is active (red = error)

##### **Max. load**

I < 2.5 mA R > 4 kΩ

When using pressure transmitters connected to extension modules, it's recommended to connect the enclosed 47 kΩ resistor to ensure proper detection of any sensor errors. For more information, refer to the Danfos s RI8HZ552 m anual.

16 | BC186686443705en-000201

*[Figurtekst: Point Point 1 2 3 4 Terminal 9: · Type AI1 AI2 AI3 AI4 12 V max. 100 mA in total. · Terminal 10: · 5 V max. 100 mA in total. · At the top the  Terminal 11, 12: · signal input is  (Cable screen) · the left of the  The screen on the pressure · two terminals. transmitter cables must only · be connected at the end of the · controller. · Galvanic isolation: · At the bottom  AI 1-4 ≠ AO 1-2 ≠ AO 3-4 · the signal input · is the right of the · two terminals. · Point 5 6 7 8 · Signal Signal  Type AO1 AO2 AO3 AO4 · type · S · Ss · Pt 1000 ohm/0°C Sd · Shr Pt 1000 · SIG Sgc · Sc3 · Saux_ · GND · P · AKS 32R · 3: Brown · AKS 32R / · 2: Blue P0 AKS 2050 / · MBS 8250 · 1: Black Pc -1 - xx bar · Pgc · Prec · AKS 32 Paux AKS 32 · -1 - zz bar · 3: Brown · 2: Black · 1: Red · U · Si g nal Module Point Terminal Si g nal t yp e /Active at · 1  (AI 1) 1 - 2 · 0 - 5 V · ... 0 - 10 V 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · On/Off Ext.  Active at: · Main  5  (AO 1) 17 - 18 · switch · Closed · Day/ / 6  (AO 2) 19 - 20 · Night · Open 7  (AO 3) 21 - 22 · Door · Level  8  (AO 4) 23 - 24 · switch · AO · 0 – 10 V]*

### **2.3.4 Extension module AK-XM 204A / AK-XM 204B**

The module contains 8 relay outputs.

##### **AK-XM 204B only**

##### **Override of relay**

Eight change-over switches at the front make it possible to override the relay’s function.

AK-XM 204A

AK-XM 204B

Either to position OFF or ON.

In position Auto the controller carries out the control.

There are two rows with LED’s. They mean: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

- Right row: (AK-XM 204B only):

- Override of relays ON = override

- OFF = no override

##### **Fuses**

Behind the upper part there is a fuse for each output.

Max. 230 V **Keep the safety distance!** AC-1: max. 4 A (ohmic) Low and high voltage AC-15: max. 3 A (Inductive) must not be connected to the same output group

*[Figurtekst: AK-XM 204B · Override of relay]*

18 | BC186686443705en-000201

##### **Point**

*[Figurtekst: Point 1 2 3 4 5 6 7 8 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8]*

*[Figurtekst: Signal Active at · DO Comp. 1 · On · Comp. 2 / · Fan 1 Off · Alarm · Solenoid · valve · Si g nal Module Point Terminal Active at · 1  (DO 1) 25 - 27 · 2  (DO 2) 28 - 30 · 3  (DO 3) 31 - 33 · 4  (DO 4) 34 -36 · 5  (DO 5) 37 - 39 · 6  (DO 6) 40 - 41 - 42 · 7  (DO 7) 43 - 44 - 45 · 8  (DO 8) 46 - 47 - 48]*

### **2.3.5 Extension module AK-XM 205A / AK-XM 205B**

The module contains:

8 analog inputs for sensors, pressure transmitters, voltage signals and contact signals. 8 relay outputs.

##### **AK-XM 205B only**

*[Figurtekst: AK-XM 205A  AK-XM 205B]*

##### **Override of relay**

Eight change-over switches at the front make it possible to override the relay’s function. Either to position OFF or ON.

In position Auto the controller carries out the control.

There are two rows with LED’s. They mean: Left row:

- Voltage supply to the controller

• Communication active with the bottom PC board (red = error) • Status of outputs DO1 to DO8 Right row: (AK-XM 205B only): • Override of relays ON = override OFF = no override

##### **Fuses**

Behind the upper part there is a fuse for each output.

When using pressure transmitters connected to extension modules, it's recommended to connect the enclosed 47 kΩ resistor to ensure proper detection of any sensor errors. For more information, refer to the Danfos s RI8HZ552 m anual.

*[Figurtekst: Max. 230 V Keep the safety distance! · AC-1: max. 4 A (ohmic) Low and high voltage · AC-15: max. 3 A (Inductive) must not be connected to · the same output group]*

*[Figurtekst: AK-XM 205B · Override of relay]*

20 | BC186686443705en-000201

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 · Terminal 9 & 21: · 12 V max. 100 mA in total. · Terminal 10 & 22: · 5 V max. 100 mA in total. · Terminal 11, 12, 23, 24 : · (Cable screen) · The screen on the pressure · transmitter cables must only · be connected at the end of · the controller. · Point 9 10 11 12 13 14 15 16 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Signal · type · S · Ss · Pt 1000 ohm/0°C Sd · SIG Shr Pt 1000 · Sgc · Sc3 · Saux_ · GND · P · AKS 32R · 3: Brown · 2: Blue AKS 32R / · AKS 2050 / · 1: Black P0 MBS 8250 · Pc · -1 - xx bar · Pgc · AKS 32 Prec · AKS 32 · 3: Brown Paux -1 - zz bar · 2: Black · 1: Red Signal Module Point Terminal Signal type / · Active at · 1  (AI 1) 1 - 2 · U · 2  (AI 2) 3 - 4 · 0 - 5 V · ... 0 - 10 V 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · 5  (AI 5) 13 - 14 · On/Off Active at: 6  (AI 6) 15 - 16 · Ext. Main · switch 7  (AI 7) 17 - 18 · Closed · Day/Night / 8  (AI 8) 19 -20 · Door Open · Level  9  (DO 1) 25 - 26 - 27 · switch · 10  (DO 2) 28 - 29 - 30 · DO Active at: 11  (DO 3) 31 - 30 - 33 · Comp on 12  (DO 4) 34 - 35 - 36 · / · Fan 13  (DO 5) 37 - 36 - 39 · Alarm Off · Solenoid  14  (DO6) 40 - 41 - 42 · valve · 15  (DO7) 43 - 44 - 45 · 16  (DO8) 46 - 47 - 48]*

### **2.3.6 Extension module AK-XM 208C**

The module contains:

8 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

4 outputs for stepper motors.

The supply voltage to the module comes from the previous module in the row. Here supply with 5 VA.

An additional and separated power supply must be installed, which must be galvanically separated from the supply for the control range. Class II is required. (Power requirements: 7.8 VA for controller + xx VA per valve). 2 separated UPS´s are recommended, one for the pack controller and another AK-XM 208C module if the valves need to open/ close during a power failure. If the AK-CM 102 module is installed it is also recommended a separated UPS.

There is one row with LED’s. It indicate the following:

- Voltage supply to the module

- Communication active with the bottom PC board (red = error)

- Step1 to step4 OPEN: Green = Open

- Step1 to step4 CLOSE: Green = Close

- Red flash = Error on motor or connection

   - When using pressure transmitters connected to extension modules, it's recommended to connect the enclosed 47 kΩ resistor to ensure proper detection of any sensor errors. For more information, refer to the Danfos s RI8HZ552 m anual.

*[Figurtekst: Valve data · Type P · ETS 12.5 - ETS 400 1.3 VA · KVS 15 - KVS 42 · CCMT 2 - CCMT 8 · CCM 10 - CCM 40 · CTR 20 · CCMT 16 - CCMT 42 5.1 VA · CCMT - 3L/5L/8L/10L 4.0 VA]*

*[Figurtekst: Separate voltage · supply is required · 24 V AC/DC fx. 13 VA max. 10 V · Output: · 24 V DC · 20 – 500 step/s · Max phase current  = 325 mA RMS · ∑ Pout   = max. 21 VA · The connection to the valve must not be broken using a relay. · L = max. 30 m]*

**Power supply to AK-XM 208C:**

Fx: 7.8 + (4 x 1.3) =  13 VA    AK-PS 063 STEP3

Fx: 7.8 + (4 x 5.1) = 28.2 VA  AK-PS 130 STEP3

22 | BC186686443705en-000201

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 · Terminal 17: 12 V max. 100 mA in total. · Terminal 18: 5 V max. 100 mA in total. · Terminal 19, 20: · (Cable screen) · Point 9 10 11 12 · Step 1 2 3 4 · Type AO · 1 25 26 27 28 · Step / 2 29 30 31 32 · Terminal 3 33 34 35 36 · 4 37 38 39 40 · ETS · CCM / CCMT · White Black Red Green · CTR · CCM KVS · CCMT]*

*[Figurtekst: Valve Module Ste p Terminal · 1 (point 9) 25 - 28 · 2 (point 10) 29 - 32 · 3 (point 11) 33 - 36 · 4 (point 12) 37 - 40]*

### **2.3.7 Extension module AK-OB 110**

*[Figurtekst: Function · The module contains two analog voltage outputs of 0 – 10 V. · Supply voltage · The supply voltage to the module comes from the controller · module. · Placing · The module is placed on the PC board in the controller module. · Point · The two outputs have points 24 and 25. They are shown on the · earlier page where the controller is also mentioned. · Max. load · I < 2.5 mA · R > 4 kohm · Accuracy · Analog outputs: +100 mV · Module 1 · Point 24 25 · AO2 · AO Type AO1 AO2 · AO 0 - 10 V AO1]*

24 | BC186686443705en-000201

### **2.3.8 Extension module EKA 163A / EKA 164A**

Display of important measurements from the controller, e.g. appliance temperature, suction pressure or condensing pressure. Setting of the individual functions can be performed by using the display with control buttons. It is the controller used that determines the measurements and settings that can occur.

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

No point has to be defined for a display module – you simply conect it.

### **2.3.9 Graphic display MMIGRS2**

Setting and display of values in the controller.

##### **Connection**

The display connects to the controller via a cable with RJ11 plug connections.

Received from the controller via cable.

##### **Termination**

The display must be terminated. Mount a connection between the terminals H and R. (AK-PC 772A is terminated internally.)

##### **Placing**

The display can be placed at a distance of up to 3 m from the controller.

##### **Point / Address**

No point has to be defined for a display – you simply connect it. However, the address must be verified. See the instructions accompanying the controller.

*[Figurtekst: EKA 163A   EKA 164A]*

*[Figurtekst: (2 m: 0847298) · (6 m: 0847299) · Brown · Green · White Danfoss 80Z991]*

To create access, the display must be connected and the address of MMIGRS2 must be activated.

##### Setting:

1. Press both the "x-button" and "enter button" and hold for 5 seconds. Subsequently the Bios menu is shown.

2. Select the line "MCX selection", press "enter"

3. Select the line "Man selection", press "enter"

4. The address is shown now. Please check that it is 001, press "enter". Then data is downloaded from the controller.

### **2.3.10 Power supply module AK-PS 063 STEP3 / 130 STEP3 / 250 STEP3**

24 V supply for controller.

**Supply voltage** 100 – 240 V AC, -15 – +10 % 110 – 250 V DC, -20 – +40 % (for DC, connect a suitable fuse)

**Placing** On DIN-rail

*[Figurtekst: Effect · Type Output tension Output current Power · AK-PS 063 STEP3 24 V DC 0.63 A 15 VA · AK-PS 130 STEP3 24 V DC 1.3A 30 VA · AK-PS 250 STEP3 24 V DC 2.5 A 60 VA]*

##### **Supply to a controller**

##### **Dimension**

|**Type**|**High**|**Width**|anfoss<br>Z992|
|---|---|---|---|
|AK-PS 063 STEP3|90 mm|18 mm|D<br>80|
|AK-PS 130 STEP3|90 mm|36 mm||
|AK-PS 250 STEP3|90 mm|54 mm||

##### **Connections**

*[Figurtekst: AK-PS 063 STEP3 AK-PS 130 STEP3 AK-PS 250 STEP3 · 24 V DC 24 V DC 24 V DC · +    _ +    _ +    _ · 100 – 240 V AC, -15 – +10 % 100 – 240 V AC, -15 – +10 % 100 – 240 V AC, -15 – +10 % · 110 – 250 V DC, -20 – +40 %   110 – 250 V DC, -20 – +40 %   110 – 250 V DC, -20 – +40 % · (for DC, connect a suitable fuse)  (for DC, connect a suitable fuse)  (for DC, connect a suitable fuse) · Danfoss 80Z993 Danfoss 80Z995 Danfoss 80Z994]*

26 | BC186686443705en-000201

### **2.3.11 Communication module AK-CM 102**

The module is a new communication module, meaning the row of extension modules can be interrupted.

The module communicates with the regulator via data communication and forwards information between the controller and the connected extension modules.

##### **Connection**

Communication module and controller fitted with RJ 45 plug connectors.

**Nothing** else should be connected to this data communication; a maximum of 5 communication modules can be connected to one controller.

##### **Communication cable**

One metre of the following is enclosed: ANSI/TIA 568 B/C CAT5 UTP cable w/ RJ45 connectors.

##### **Positioning**

Max. 30 m from the controller (The total length of the communication cables is 30 m)

24 volt AC or DC should be connected to the communication module.

The 24 V can be sourced from the same supply that supplies the controller. (The supply for the communication module is galvanically separated from the connected extension modules). The terminals must **not** be earthed.

The power consumption is determined by the power consumption of the total number of modules.

The controller strand load must not exceed 32 VA. Each AK-CM 102 strand load must not exceed 20 VA.

##### **Point**

Connection points on the I/O modules should be defined as if the modules were an extension of each other.

##### **Address**

The address for the first communication module should be set to 1. Any second module should be set to 2.  A maximum of 5 modules can be addressed.

##### **Termination**

The termination switch on the final communication module should be set to ON.

The controller should permanently be set to = ON.

Additional modules may only be installed following the installation of the final module. (Here following module no. 11; see the sketch.)

*[Figurtekst: Max. 32 VA · Max. 20 VA · Max. 20 VA]*

After configuration, the address must not be changed.

### **2.4 Preface to design**

Be aware of the following when the number of extension modules is being planned. A signal may have to be changed, so that an additional module may be avoided.

- An ON/OFF signal can be received in two ways. Either as a contact signal on an analog input or as voltage on a low or high-voltage module.

Mentioned below are a number of functions and connections that may have to be considered when a regulation has to be planned. There are more functions in the controller than the ones mentioned here, but those mentioned have been included in order that the need for connections can be established.

- An ON/OFF output signal can be given in two ways. Either with a relay switch or with solid state. The primary difference is the permitted load and that the relay switch contains a cutout switch.

### **2.4.1 Functions**

##### **Clock function**

Clock function and change-over between summer time and winter time are contained in the controller.

The clock setting is maintained for at least 12 hours at a power failure.

The clock setting is kept updated if the controller is linked up in a network with a system manager.

##### **Start/stop of regulation**

Regulation can be started and stopped via the software. External start/stop can also be connected.

The function stops all regulation, including any high-pressure regulation. Excess pressure can lead to a loss of charge.

##### **Start/stop of compressors**

External start/stop can be connected.

##### **Alarm function**

If the alarm is to be sent to a signal transmitter, a relay output will have to be used.

##### **I'm alive function**

A relay can be reserved which is pulled during normal regulation. The relay will be released if the regulation stops with the main switch or if the controller fails.

##### **Extra temperature sensors and pressure sensors**

If additional measurements have to be carried out beyond the regulation, sensors can be connected to the analog inputs.

##### **Forced control**

The software contains a forced control option. If an extension module with relay outputs is used, the module’s top part can be with change-over switches – switches that can override the individual relays into either OFF or ON position. Wiring should be done with a safety relay. See Regulating functions.

##### **Data communication**

The controller module has terminals for LON data communication. The requirements to the installation are described in a separate document.

28 | BC186686443705en-000201

### **2.4.2 Connections**

In principle there are the following types of connections:

##### **Analog inputs ”AI”**

- This signal must be connected to two terminals. SIG Signals can be received from the following GND sources: • Temperature signal from Pt 1000 ohm temperature sensor

- • Contact signal where the input is shortcircuited or ”opened”, respectively

- • Voltage signal from 0 to 10 V • Signal from pressure transmitter AKS 32, AKS 32R / AKS 2050 / MBS 8250. The supply voltage is supplied from the module’s terminal board where there is both a 5 V supply and a 12 V supply. When programming the pressure transmitter’s pressure range must be set.

##### **ON/OFF output signals ”DO”**

There are two types, as follows:

- Relay outputs All relay outputs are with change-over relay so that the required function can be obtained when the controller is without voltage.

- Solid state outputs Reserved for AKV valves, but output can cut an external relay in and out, as with a relay output. The output is only found on the controller module.

When programming the function must be set:

- Active when the output is activated

- Active when the output is not activated.

##### **ON/OFF voltage inputs ”DI”**

This signal must be connected to two terminals.

- The signal must have two levels, either 0 V or ”voltage” on the input. There are two different extension modules for this signal type: - low-voltage signals, e.g. 24 V

- high-voltage signals, e.g. 230 V

When programming the function must be set:

- Active when the input is without voltage • Active when voltage is applied to the input.

##### **Analog output signal ”AO”**

This signal is to be used if a control signal is to be transmitted to an external unit, e.g. a frequency converter. When programming the signal range must be defined: 0 – 5 V, 1 – 5 V, 0 – 10 V or 2 – 10 V.

Pulse signal for the stepper motors. This signal is used by valve motors of the type ETS, KVS, CCM and CCMT. The valve type should be set during programming.

### **2.4.3 Limitations**

As the system is very flexible  regarding the number of connected units you must check whether your selection complies with the few limitations there are.

The complexity of the controller is determined by the software, the size of the processor, and the size of the memory. It provides the controller with a certain number of connections from which data can be downloaded, and others where coupling with relays can be performed.

- The sum of connections cannot exceed 120 (AK-PC 772A).

- The number of extension modules must be limited so that the total power in a row will not exceed **32** VA (including controller).

- If the AK-CM 102 communication module is used, each row of AK-CM 102 must not exceed 20 VA (incl. AK-CM 102).

##### **Common pressure transmitter**

If several controllers receive a signal from the same pressure transmitter, the supply to the affected controllers must be wired so that it is not possible to switch off one of the controllers without also switching off the others. (If one controller is switched off, the signal will be pulled down, and all the other controllers will receive a signal which is too low)

   - No more than **5** pressure transmitters may be connected to one controller module.

   - No more than **5** pressure transmitters may be connected to one extension module.

- There must not be more than a total of 12 modules (controller + 11 modules).

### **2.5 Design of a compressor and condenser control**

### **2.5.1 Procedure:**

1. Make a sketch of the system in question

2. Check that the controller’s functions cover the required application

3. Consider the connections to be made

4. Use the planning table. / Note down the number of connections ./ add up

5. Are there enough connections on the controller module? – If not, can they be obtained by changing an ON/OFF input signal from voltage signal to contact signal, or will an extension module be required?

6. Decide which extension modules are to be used

7. Check that the limitations are observed

8. Calculate the total length of modules

9. The modules are linked together

10. The connection sites are established

11. Draw a connection diagram or a key diagram

12. Size of supply voltage/transformer

##### **1. Sketch**

Make a sketch of the system in question.

##### **2. Compressor and condenser functions**

||AK-PC<br>|Max. number of steps|4|
|---|---|---|---|
||772A|Speed regulation|x|
|**Application**||Stepand speed regulation|x|
|Regulation of a compressorgroupMT<br>|x|Speed regulation first step|x|
|Regulation of a condensergroupLT|x|Limitation of speed duringnight operation|x|
|Regulation of aparallel compression IT|x|Heat recoveryfunction for domestic water or room|x|
|Regulation of agas cooler|x|**Gas coolerpressure reference**||
|Regulation of CO2 receiverpressure|x|Floating pressure reference|x|
|**Regulation of compressor capacity**||Settingof references for heat recoveryfunctions|x|
|Regulation sensor = P0|x|**High pressure control**||
|PI-regulation|x|If needed, offset forgreater compressor capacity|x|
|Max. number of compressor steps on MT + IT|3|f<br>Offset when there are requirements for heat recovery|x|
|Max. number of compressor steps on LT|2|**Safety functions**||
|Max. number of unloaders each compressor|3|Min. suctionpressure|x|
|Identical compressor capacities|x|Max. suctionpressure|x|
|Different compressor capacities|x|Max. condensing pressure|x|
|Speed regulation of 1 or 2 compressors|x|Max. dischargegas temperature|x|
|Run time equalisation|x|Min. / Max. superheat|x|
|Min. restart time|x|Safetymonitoringof compressors|x|
|Min. On-time|x|Common highpressure monitoringof compressors|x|
|Liquid injection in suction line|x|Safetymonitoringof condenser fans|x|
|External start/stopof compressors|x|General alarm functions with time delay|10|
|**Oil management**||**Miscellaneous**||
|Oil equalisation|x|Inject On function|x|
|**Suctionpressure reference**||Option for connection of separate display|4 +1|
|Override via P0 optimization|x|Separate thermostat function|1|
|Override via “night setback”|x|Separatepressostat function|1|
|Override  via "0 -10 V signal"|x|Separate voltage measurement|1|
|**Regulation ofgas cooler**||PI regulation|1|
|Regulation sensor = Sgc|x|Max. input and output|120|
|Stepregulation|x|||

30 | BC186686443705en-000201

##### **A bit more about the functions**

##### **Compressor**

Regulation of up to 3 compressors on MT and 2 on LT Up to 3 unloaders per compressor. Compressor No. 1 or 2 can be speed-regulated. P0 - Suction pressure is used as a regulation sensor. When regulating with parallel compression (IT circuit), 2 compressors can be used to regulate MT, one on IT and along with 2 on LT.

##### **Safety circuit**

If signals are to be received from one or more parts of a safety circuit, each signal must be connected to an ON/OFF input.

##### **Day/night signal for raising the suction pressure**

The clock function can be used, but an external ON/OFF signal may be used instead.

If the “P0 optimization” function is used, no signal will be given concerning the raising of the suction pressure. The P0 optimization will see to this.

If regulating on MT only, 3 compressors can be used to regulate.

##### **“Inject ON” override function**

##### **Gas cooler**

##### Regulation of up to 4 fans.

Fans can be speed-regulated. Either all on one signal or only the first fan of several. EC motor can be used. Relay outputs and solid state outputs may be used, as desired. An Sgc temperature sensor is used as a regulation sensor at the gas cooler discharge.

##### **Speed regulation of condenser fans**

The function requires an analog output module. A relay output may be used for start/stop of the speed regulation. The fans may also be cut in and out by relay outputs.

##### **Pulse wide modulating unloading**

When using a compressor with PWM-unloading, the unloading should be connected to one of the four solid state outputs in the controller.

##### **Heat recovery**

There are adjustment options for hot water containers for domestic hot water or for heating.

The function closes expansion valves on evaporator controls when all compressors are prevented from starting. The function can take place via the data communication, or it may be wired via a relay output.

##### **Separate thermostat and pressure control functions**

A number of thermostats can be used according to your wishes. The function requires a sensor signal and a relay output. In the controller there are settings for cutin and cutout values. An associated alarm function may also be used.

##### **Separate voltage measurement**

A voltage measurement can be used according to your wishes. The signal can for example be 0 – 10 V. The function requires a voltage signal and a relay output. In the controller there are settings for cutin and cutout values. An associated alarm function may also be used.

If you want to know more about the functions, go to chapter 5.

##### **3. Connections**

Here is a survey of the possible connections. The texts can be read in context with the table on the following page.

• Prec.  Pressure i CO2 reciever Must always be used

- Paux

##### **Analog inputs**

##### **Temperature sensors**

- Ss (suction gas temperature)

- Must always be used in connection with compressor regulation.

- Sd (discharge gas temperature) Must always be used in connection with compressor regulation.

- Sc3 (outdoor temperature)

- To be used when regulation is performed with floating condenser reference.

- Saux (extra temperature sensor)

For monitoring, data collection or separate thermostat function.

- Shr (temperature sensors for heat recovery) Must be used when adjusting the heat tank.

- Sgc (temperature sensor for gas cooling controls)

- Shall be placed within one metre after the gas cooler.

- Shp (temperature sensor, the refrigerant may be bypassed gas cooler)

##### **Pressure transmitters**

- P0 Suction Pressure

- Must always be used

- Pc Condensing Pressure Must always be used

- Pgc Gas cooler pressure. Must always be used

- One extra pressure transmitters can be connected for monitoring and data collection.

##### **Voltage signal**

- Ext. Ref

Used if a reference override signal is received from another control.

- Voltage input

One extra voltage signal can be connected for monitoring and data collection

##### **On/Off-inputs**

Contact function (on an analog input) or

voltage signal (on an extension module)

- Common safety input for all compressors (e.g. common highpressure/low-pressure pressure switch)

- Up to 6 signals from the safety circuit of each compressor

- Signal from the condenser fans safety circuit

- External start/stop of regulation

- External day/night signal (raise/lower the suction pressure reference). The function is not used if the “P0 optimization” function is used.

- DI alarm (1-10) inputs

- Up to 10 no. extra on/off signals for general alarm for monitoring and data collection can be connected.

- Level contacts

##### **On/off-outputs**

Relay outputs

- Compressors

- Unloaders

- Fan motor

- Injection On function (signal for evaporator controls. One per suction group).

- Start/stop of liquid injection in suction line

- Start/stop of valve and circulation pump for heat recovery

- ON/OFF signal for start/stop of speed regulation

- Alarm relay. I'm alive relay.

- On/off signals from general thermostat (1), pressure switch (1) or voltage input function (1).

##### **Solid state outputs**

The solid state outputs on the controller module may be used for the same functions as those mentioned under “relay outputs”. (The output will always be “OFF” when the controller has a power failure).

- Should be used if controlled using a digital scroll compressor.

##### **Analog output**

- Speed regulation of the condenser’s fans.

- Speed regulation of the compressor

- Stepper signal for high pressure valve

- Stepper signal for hot gas by-pass valve

##### **Example Compressor group:**

MT circuit

- 3 x compressors with “Cyclical”. One speedcontrolled

- Safety monitoring of each compressor

- Common high pressure monitoring

- P0 setting –10°C, P0 optimisation LT circuit

- 2 x compressors with “Cyclical”. One speedcontrolled

- Safety monitoring of each compressor

- Common high pressure monitoring

- P0 setting –30°C, P0 optimisation

##### **Containers:**

- Control of pressure in CO2 receiver

- Controlling the tank temperature for domestic water, 55 °C

**Safety functions:**

- Monitoring of Po, Pc, Sd and superheat in suction line

- MT-Po max = -5 °C, Po min = -35 °C

- MT-Pc max = 110 bar

- MT-Sd max = 120 °C

- LT-Po max = -5 °C, Po min = -45 °C

- LT-Pc max = 40 bar

- LT-Sd max = 120 °C

Data from this example is used on the next page. The result is that the following modules should be used:

   - AK-PC 772A controller

   - AK-XM 208C stepper output module

   - AK-XM 103A analog input and output module

- SH min =  5 °C, SH max = 35 °C

##### **Gas cooling control:**

- Fans, speed controlled

- Pressure regulation Pgc with reference from Sc3 and Sgc

- Pressure increase for heat recovery

32 | BC186686443705en-000201

|**4. Planning table**<br>The table helps you establish whether there are enough<br>inputs and outputs on the basic controller.<br>If there are not enough of them, the controller must be<br>extended by one or more of the mentioned extension<br>modules.<br>Note down the connections you will require and add<br>them up|**Analog input signal**<br>Example|**On/off voltage signal**<br>Example|**On/off voltage signal**<br>Example|**On/Off output signal**<br>Example|**Analog output signal 0-10 V**<br>**Stepper output**<br>Example|**7**<br>**Limitations**|
|---|---|---|---|---|---|---|
|**Analog inputs**|||||||
|Temperature sensors, Ss, Sd, Sc3, Sgc|6||||||
|<br>Extra temperature sensor / separate thermostats /PI-regulation|||||||
|Pressure transmitters, P0, Pc, Prec / separatepressostat<br>|5|||||P = Max.**5**/ module|
|Voltage signal from other regulation, separate signals|||||||
|Heat recoveryvia thermostat Shr|1||||||
|**On/off inputs**|Contact|24 V|230 V||||
|Safetycircuits, common for all compressors|2|||||Max.2|
|Safetycircuits, Oilpressure||||||Max. 1/ Comp.|
|Safetycircuits, comp. Motorprotection<br>|||||||
|Safetycircuits, comp. Motor temp.|||||||
|Safetycircuits, comp. Highpres. thermostat<br>|||||||
|Safetycircuits, comp. Highpres.pressostat|||||||
|Safetycircuits,general for each compressor|5||||||
|Safetycircuits, condenser fans, frequencyconverter||||||Max. 1/ fan|
|External start/stop|||||||
|Night setback of suctionpressure|||||||
|Separate alarm functions via DI|||||||
|Load shedding<br>|||||||
|Start of Heat recovery||||||> OK|
|**On/off outputs**||||||ed =|
|Compressors, motors||||5||eed|
|Unloaders||||||xc|
|F  ili||||||e|
|an motors, crcuatonpumps||||1||are|
|Alarm relay, I'm alive relay<br>||||||<br>ons|
|Inject ON||||||Max. 2<br>ti|
|Separate thermostat and pressostat functions and voltage measure-<br>ments||||||Max. 1+1+1<br>e:<br>limita|
|Heat recoveryfunction via thermostat||||1||Max.1<br>pl<br>he|
|Liquid injection in suction line||||||Max.1<br>xam<br>of t|
|Hotgas dump||||1||The e<br>None|
|**Analog control signal, 0 – 10 V**<br>|||||||
|Frequencyconverter, Compressor, fans, valves etc.|||||3||
|**Valves with stepper motor Parallel valves if applicable**|||||2||
|**.  ,**<br>**Sum of  connections for the regulation**|19|0|0|8|3+2|Sum = max.**120**|
|Number of connections on a controller module|11<br>11|0<br>0|0<br>0|8<br>8|0<br>0<br>0||
|**5. Missing connections, if applicable**|8|-|0|0|3+2||
|**6. The missing connections to be supplied by one or mo**|**re extens**|**ion modu**|**les:**|||Sum ofpower|
|AK-XM 101A**(8 analog inputs)**||||||___pcs. á 2 VA = __|
|AK-XM 102A**(8 digital low voltage inputs)**||||||___pcs. á 2 VA = __|
|AK-XM 102B**(8 digital high voltage outputs)**||||||___pcs. á 2 VA = __|
|AK-XM 103A**(4 analog inputs, 4 analog outputs)**<br> **l **|1||||1|___pcs. á 2 VA = __<br>á|
|AK-XM 204A / B**(8 reay outputs)**||||||___pcs.  5 VA = __|
|AK-XM 205A / B**(8 analog inputs. + 8 relay output)**||||||___pcs. á 5 VA = __|
|AK-XM 208C**(8 analog inputs + 4 stepper outputs)**|1||||1|___pcs. á 5 VA = __|
|AK_OB 110**(2 analog outputs)**||||||___pcs. á 0 VA =  0|
|||||||1 pcs. á 8 VA = 8<br>Sum =<br>Sum = max.**32**VA|

##### **8. Length**

If you use many extension modules the controller’s length will grow accordingly. The row of modules is a complete unit which cannot be broken.

If the row becomes longer than desired, the row can be broken by using AK-CM 102.

The module dimension is 72 mm. Modules in the 100-series consist of one module Modules in the 200-series consist of two modules The controller consist of three modules The length of an aggregate unit = n x 72 + 8

or in an other way:

|**Module**|**Type**|**Number**||**at**|**Length**|
|---|---|---|---|---|---|
|Controller module||1|x|224|= 224 mm|
|Extension module|200-series|_|x|144|= ___ mm|
|Extension module|100-series|_|x|72|= ___ mm|
|**Total length**|||||= ___ mm|

Example continued: Controller module + 1 extension module in 200-series + 1 extension module in 100 series = 224 + 144 + 72  = 440 mm.

##### **9. Linking of modules**

Start with the controller module and then mount the selected extension modules. The sequence is of no importance.

However, you must **not** change the sequence, i.e. rearrange the modules, after you have made the setup where the controller is told which connections are found on which modules and on which terminals.

The modules are attached to one another and kept together by a connection which at the same time transmits the supply voltage and the internal data communication to the next module.

Mounting and removal must always be performed when there is no voltage.

The protective cap mounted on the controller’s plug connection must be moved to the last vacant plug connection so that the plug will be protected against short-circuit and dirt.

When the regulation has started the controller will all the time check whether there is connection to the connected modules. This status can be followed by the light-emitting diode.

When the two catches for the DIN rail mounting are in open position the module can be pushed into place on the DIN rail – no matter where in the row the module is found. Removal is likewise carried out with the two catches in the open position.

34 | BC186686443705en-000201

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
|fx P0|x|x|AKS 32R 1-6 bar|

The connection survey from the controller and any extension modules are uploaded from the paragraph "Module survey. E.g. controller module:

*[Figurtekst: Module  Point · Mind the numbering. · The right-hand part of the · controller module may look like · a separate module. But it  isn’t.]*

**Note:** The safety relays should not be fitted onto a module with override changeovers, as they can be put out of operation by an incorrect setting.

- Columns 1, 2, 3 and 5 are used for the programming.

- Columns 2 and 4 are used for the connection diagram.

###### Example continued

*[Figurtekst: Signal Module Point  Terminal Signal type / · Active at · 1  (AI 1) 1 - 2 · Shr Receiver temperature 2  (AI 2) 3 - 4 Pt 1000 · 3  (AI 3) 5 - 6 · Suction gas temperature - Ss MT 4  (AI 4) 7 - 8 Pt 1000 · Discharge temperature - Sd MT 5  (AI 5) 9 - 10 Pt 1000 · Suction pressure - P0 MT 6  (AI 6) 11 - 12 AKS 2050-59 · Condensing  pressure - Pc MT 7  (AI 7) 13 - 14 AKS 2050-159 · 8  (AI 8) 19 - 20 · Suction gas temperature - Ss LT 9  (AI 9) 21 - 22 Pt 1000 · Discharge temperature - Sd LT 10  (AI 10) 23 - 24 Pt 1000 · Suction pressure - P0 LT 1  11  (AI 11) 25 - 26 AKS 2050-59 · Compressor 1 MT 12  (DO 1) 31 - 32 ON · Compressor 2 MT 13  (DO 2) 33 - 34 ON · Compressor 3 MT 14  (DO 3) 35 - 36 ON · Compressor 1 LT 15  (DO 4) 37 - 38 ON · Compressor 2 LT 16  (DO 5) 39 - 40 - 41 ON · Valve and circulation pump HR 17  (DO6) 42 - 43 - 44 ON · Fan motors 18  (DO7) 45 - 46 - 47 ON · Hot gas dump 19  (DO8) 48 - 49 - 50 ON · 24  - · 25  -]*

*[Figurtekst: Signal Module Point/Step Terminal Signal type · Compressor 1 MT Gen. Safety 1  (AI 1) 1 - 2 Open · Compressor 2 MT Gen. Safety 2  (AI 2) 3 - 4 Open · Compressor 3 MT Gen. Safety 3  (AI 3) 5 - 6 Open · All compressors common safety MT 4  (AI 4) 7 - 8 Open · Compressor 1 LT Gen. Safety 5  (AI 5) 9 - 10 Open · Compressor 2 LT Gen. Safety 6  (AI 6) 11 - 12 Open · All compressors common safety LT 2 7  (AI 7) 13 - 14 Open · 8  (AI 8) 15 - 16 · Stepper signal to by-pass valve, · 9 (step 1) 25 - 26 - 27 - 28 CCM (ETS) · CCM · 10 (step 2) 29 - 30 - 31 - 32 · Stepper signal to high pressure · 11 (step 3) 33 - 34 - 35 - 36 CCMT · valve, CCMT · 12 (step 4) 37 - 38 - 39 - 40]*

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type**|
|---|---|---|---|---|
|Outdoor temperature Sc3||**1**(AI 1)|**1 - 2**|Pt 1000|
|Temp.  gas  cooler outlet Sgc||**2**(AI 2)|**3 - 4**|Pt 1000|
|Gas cooler pressure Pgc||**3**(AI 3)|**5 - 6**|AKS 2050-159|
|Receiver pressure Prec|**3**|**4**(AI 4)|**7 - 8**|AKS 2050-159|
|Speed control, compressor MT||**5**(AO 1)|**9 - 10**|0 - 10 V|
|Speed control, compressor LT||**6**(AO 2)|**11 - 12**|0 - 10 V|
|Speed control, compressor, EC||**7**(AO 3)|**13 - 14**|0 - 10 V|
|||**8**(AO 4)|**15 - 16**||

Continued next page

##### **11. Connection diagram**

Drawings of the individual modules may be ordered from Danfoss. Format = dwg and dxf.

The supply voltage for the pressure transmitter should be taken from the same module that receives the pressure signal.

You may then yourself write the module number in the circle and draw the individual connections.

##### Example continued:

36 | BC186686443705en-000201

##### **12. Supply voltage**

Supply voltage is only connected to the controller module. The supply to the other modules is transmitted via the plug between the modules.

The supply must be 24 V +/-20%. One power supply must be used for each controller. The power supply must be a  class II. The 24 V must not be shared by other controllers or units. The analog inputs and outputs are **not** galvanically separated from the supply.

The + and – 24V input must **not** be earthed.

If using stepper motor valves, the supply for these must be provided from a separate power supply.

CO2 regulation makes it necessary to safeguard the voltage to the controller and valves using UPS.

##### **Power supply size**

|The power consum|ption grows|with the nu|mber of|modules used:|
|---|---|---|---|---|
|**Module**|**Type**|**Number**|**á**|**Effect**|
|Controller||1<br>x|8 =|8 VA|
|Extension module|200 series|_<br>x|5 =|__ VA|
|Extension module|100 series|_<br>x|2 =|__ VA|
|Total||||___ VA|

##### **Common pressure transmitter**

If several controllers receive a signal from the same pressure transmitter, the supply to the affected controllers must be wired so that it is not possible to switch off one of the controllers without also switching off the others. (If one controller is switched off, the signal will be pulled down, and all the other controllers will receive a signal which is too low)

Example continued:

|Controller module|8 VA|
|---|---|
|+ 1 extension modules in 200 series|5 VA|
|+ 1 extension modules in 100 series|2 VA|
||------|
|Power supply size (least)|15 VA (AK-PS 130 STEP3)|

|+ Separate power supply for the|module with the stepper motors:|
|---|---|
|Modules valve control|7.8 VA|
|CCM valve|1.3 VA|
|CCMT valve fx.|1.3 VA|
||-------|
|Power supply size (least)|10.4 VA (AK-PS 063 STEP3)|

### **2.6 Ordering**

##### 1. Controller

|**Type**|**Function**|**Application**|**Language**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|---|
|AK-PC 772A|Controller for capacity control of compres-<br>sors and condensers. With high pressure<br>control andparallel compressor(optional)|A small CO2 plant with<br>booster|English, German, French, Italian,<br>Spanish, Portuguese, Russian, Polish,<br>Chinese<sup>1)</sup>, Dutch,Danish,Finnish,Czech|**080Z0201**|**X**|

1) Chinese is not available in MMI display. It is available only in PC via ST-500 (Service Tool).

##### 2. Extension modules and surve y for inputs and outputs

|**Type**|**Analog**<br>**inputs**|**On/Off ou**|**f tputs**|**On/off supp**<br>**(DI signal)**|**f ly voltage**|**Analog**<br>**outputs**|**Stepper**<br>**outputs**|**Module**<br>**with**<br>**switches**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|---|---|---|---|---|---|
||For sensors,<br>pressure<br>transmitters<br>etc.|Relay<br>(SPDT)|Solid state|Low volt-<br>age<br>(max. 80 V)|High volt-<br>age<br>(max. 260<br>V)|0 – 10 V DC|For valves<br>with step<br>control|For override<br>of relay<br>outputs|With screw<br>terminals||
|Controller|11|4|4|-|-|-||-|-||
|Extension mo|dules||||||||||
|AK-XM 101A|8||||||||**080Z0007**||
|AK-XM 102A||||8|||||**080Z0008**||
|AK-XM 102B|||||8||||**080Z0013**||
|AK-XM 103A|4|||||4|||**080Z0032**|**x**|
|AK-XM 204A||8|||||||**080Z0011**||
|AK-XM 204B||8||||||x|**080Z0018**||
|AK-XM 205A|8|8|||||||**080Z0010**||
|AK-XM 205B|8|8||||||x|**080Z0017**||
|AK-XM 208C|8||||||4||**080Z0023**|**x**|
|<br>The following<br>There is onlyr|extension modu<br>oom for one mo|le can be pl<br>dule.|aced on the PC|board in the c|ontroller mod|ule.|||||
|AK-OB 110||||||2|||**080Z0251**||

##### 3. AK o p eration and accessories

|**Type**|**Function**|**Application**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|
|**Operation**|||||
|AK-ST 500|Software for operation of AK controllers|AK-operation|**080Z0161**|**x**|
|-|Cable between PC and AK controller|USB A-B(standard IT cable)|**-**|**x**|
|**Accessories**|**Power supply module 24 V DC**||||
|AK-PS 063 STEP3|15 VA||**080Z0057**|**x x**|
|AK-PS 130 STEP3|30 VA|Supply for controller|**080Z0058**||
|AK-PS 250 STEP3|60 VA||**080Z0059**||
|**Accessories**|**External display that can be connected to the con**|**troller module. For showing, say, the suctionpressure**|||
|EKA 163A|Display||**084B8562**<sup>1)</sup>||
|EKA 164A|Displaywith operation buttons||**084B8563**<sup>1)</sup>||
|MMIGRS2|Graphic displaywith operation||**080G0294**||
|||Length = 2 m|**084B7298**||
|-|Cable between EKA display and controller|Length = 6 m|**084B7299**||
||Cable between graphic display type MMIGRS2 and|Length = 1.5 m|**080G0075**||
|-|<br>controller (controller with RJ11 plug)|Length  = 3 m|**080G0076**||
|**Accessories**|**Communication modules for controllers where m**|**odules cannot be connected continuously**|||
|AK-CM 102|Communication module|Data communication for external extension modules|**080Z0064**||

1) Please, check instruction sheet RI8KB700 for a proper cable connection between EKA display and controller.

38 | BC186686443705en-000201

### **3. Mounting and wiring**

This section describes how the controller:

• Is fitted

• Is connected

We have decided to work on the basis of the example we went through previously, i.e. the following modules:

- AK-PC 772B controller module

- AK-XM 208C analog input module + stepper output module

- AK-XM 103A analog input and output module

### **3.1 Mounting of analog output module**

1. Lift the top part off the basic module

- The basic module must not be connected to voltage.

Press in the plate on the left-hand side of the light-emitting diodes and the plate on the right-hand side for the red address changers. Lift the top part off the basic module.

2. Mount the extension module in the basic module

The analogue extension module used for mounting inside the control module is displayed for information purposes only. This is not used in the example.

*[Figurtekst: There are two outputs.]*

3. Put the top part back on the basic module

### **3.2 Mounting of extension module on the basic module**

##### 1. Move the protective cap

Remove the protective cap from the connection plug on the righthand side of the basic module.

Place the cap on the connection plug to the right of the extension module that is to be mounted on the extreme right-hand side of the AK assembly.

In our example two extension modules are to be fitted to the basic module. We have chosen to fit the module with stepper output directly on the basic module and then the following module. The sequence is thus:

All the subsequent settings that affect the two extension modules are determined by this sequence.

##### 2. Assemble the extension module and the basic module

The basic module must not be connected to voltage.

When the two snap catches for the DIN rail mounting are in the open position, the module can be pushed into place on the DIN rail – regardless of where the module is on the row. Disassembly is thus done with the two snap catches in the open position.

40 | BC186686443705en-000201

### **3.3 Wiring**

Decide during planning which function is to be connected and where this will be.

##### 1. Connect inputs and outputs

##### **Remember the isolation amplifier**

If signals are received from different controls, e.g. heat recovery for one of the inputs, a galvanically insulated module should be inserted.

Here are the tables for the example:

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|||**1**(AI 1)|**1 - 2**||
|Shr container temperature||**2**(AI 2)|**3 - 4**|Pt 1000|
|||**3**(AI 3)|**5 - 6**||
|Suction gas temperature - Ss MT||**4**(AI 4)|**7 - 8**|Pt 1000|
|Discharge temperature - Sd MT||**5**(AI 5)|**9 - 10**|Pt 1000|
|Suction pressure - P0 MT||**6**(AI 6)|**11 - 12**|AKS 2050-59|
|Condensing  pressure - Pc MT||**7**(AI 7)|**13 - 14**|AKS 2050-159|
|||**8**(AI 8)|**19 - 20**||
|Suction gas temperature - Ss LT||**9**(AI 9)|**21 - 22**|Pt 1000|
|Discharge temperature - Sd LT||**10**(AI 10)|**23 - 24**|Pt 1000|
|Suction pressure - P0 LT|**1**|**11**(AI 11)|**25 - 26**|AKS 2050-59|
|Compressor 1 MT||**12**(DO 1)|**31 - 32**|ON|
|Compressor 2 MT||**13**(DO 2)|**33 - 34**|ON|
|Compressor 3 MT||**14**(DO 3)|**35 - 36**|ON|
|Compressor 1 LT||**15**(DO 4)|**37 - 38**|ON|
|Compressor 2 LT||**16**(DO 5)|**39 - 40 - 41**|ON|
|Valve and circulation pump HR||**17**(DO6)|**42 - 43 - 44**|ON|
|Fan motors||**18**(DO7)|**45 - 46 - 47**|ON|
|Hot gas dump||**19**(DO8)|**48 - 49 - 50**|ON|
|||**24**<br>**25**|**-**<br>**-**||

The function of the switch functions can be seen in the last column.

There are pressure transmitters AKS 32R and AKS 2050 available for several pressure ranges. Here there are two different ones. One up to 59 bar and two up to 159 bar.

|**Signal**|**Module**|**Point/Step**|**Terminal**|**Signal type**|
|---|---|---|---|---|
|Compressor 1 MT Gen. Safety||**1**(AI 1)|**1 - 2**|Open|
|Compressor 2 MT Gen. Safety||**2**(AI 2)|**3 - 4**|Open|
|Compressor 3 MT Gen. Safety||**3**(AI 3)|**5 - 6**|Open|
|All compressors common safety<br>MT||**4**(AI 4)|**7 - 8**|Open|
|Compressor 1 LT Gen. Safety||**5**(AI 5)|**9 - 10**|Open|
|Compressor 2 LT Gen. Safety||**6**(AI 6)|**11 - 12**|Open|
|All compressors common safety LT|**2**|**7**(AI 7)|**13 - 14**|Open|
|||**8**(AI 8)|**15 - 16**||
|Stepper signal to by-pass valve,<br>CCM||**9 (step 1)**|**25 - 26 - 27 - 28**|CCM (ETS)|
|||**10 (step 2)**|**29 - 30 - 31 - 32**||
|Stepper signal to high pressure<br>valve, CCMT||**11 (step 3)**|**33 - 34 - 35 - 36**|CCMT|
|||**12 (step 4)**|**37 - 38 - 39 - 40**||

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type**|
|---|---|---|---|---|
|Outdoor temperature Sc3||**1**(AI 1)|**1 - 2**|Pt 1000|
|Temp.  gas  cooler outlet Sgc||**2**(AI 2)|**3 - 4**|Pt 1000|
|Gas cooler pressure Pgc||**3**(AI 3)|**5 - 6**|AKS 2050-159|
|Receiver pressure Prec|**3**|**4**(AI 4)|**7 - 8**|AKS 2050-159|
|Speed control, compressor MT||**5**(AO 1)|**9 - 10**|0 - 10 V|
|Speed control, compressor LT||**6**(AO 2)|**11 - 12**|0 - 10 V|
|Speed control, compressor, EC||**7**(AO 3)|**13 - 14**|0 - 10 V|
|||**8**(AO 4)|**15 - 16**||

The connections for the example can be seen here.

Warning Keep signal cables separate from cables with high voltage.

The screen on the pressure transmitter cables must only be connected at the end of the controller.

The supply voltage for the pressure transmitter should be taken from the same module that receives the pressure signal.

42 | BC186686443705en-000201

2. Connect LON communication network

- The installation of the data communication must comply with the requirements set out in document RC8AC.

3. Connect supply voltage

- Is 24 V, and the supply must not be used by other controllers or devices. The terminals must not be earthed.

4. Follow light-emitting diodes

- When the supply voltage is connected the controller will go through an internal check. The controller will be ready in just under one minute when the light-emitting diode ”Status” starts flashing slowly.

5. When there is a network

- Set the address and activate the Service Pin.

6. The controller is now ready to be configured.

*[Figurtekst: Internal communication · between the modules: · Quick flash = error · Slow flash = OK · Constantly On = error Quick flash = answer from gateway in 10 min. · after network installation · n Power Constantly ON = error · n Comm Constantly OFF = error · n DO1  n Status · n DO2  n Service Tool · n DO3  n LON External communication · n DO4  n I/O extension Communication to AK-CM 102 · n DO5  n Alarm Flash = active alarm/not cancelled · n DO6 Constant ON = Active alarm/cancelled · n DO7  n Display · n DO8  n Service Pin · Network installation · Status on output 1-8]*

### **4. Configuration and operation**

This section describes how the controller:

- Is configured

- Is operated

We have decided to work on the basis of the example we went through previously, i.e. compressor control with 3 compressors for MT and 2 compressors for LT and high pressure control using heat recovery and gas cooler.

The example is shown two pages in.

### **4.1 Configuration**

### **4.1.1 Connect PC**

PC with the program “Service Tool” is connected to the controller.

The controller must be switched on first and the LED “Status” must flash before the Service Tool program is started.

Start Service Tool programme

Login with user name SUPV

For connecting and operating the "AK service tool" software, please see the manual for the software.

The first time the Service Tool is connected to a new version of a controller the start-up of the Service Tool will take longer than usual while information is retrieved from the controller. Time can be followed on the bar at the bottom of the display.

When the controller is supplied the SUPV access code is 123. When you are logged into the controller an overview of it will always appear.

Select the name **SUPV** and key in the access code.

In case the overview is empty. This is because the controller has not yet been set up. The red alarm bell at the bottom right tells you that there is an active alarm in the controller. In our case the alarm is due to the fact that the time in the controller has not yet been set.

44 | BC186686443705en-000201

##### **Refrigerating plant example**

We have decided to describe the setup by means of an example comprising a MT & LT compressor group and a high pressure control.

The example is the same as the one given in the "Design" section, i.e. the controller is an AK-PC 772A + extension modules.

##### **Example**

##### **Compressor Group**

MT circuit

- 3 x compressors with “Cyclical”. One speed-controlled

- Safety monitoring of each compressor

- Common high pressure monitoring

Here, only the internal main switch is used to initiate regulation. If disconnected during operation, it will stop all regulation, including high pressure regulation.

- P0 setting –10 °C, P0 optimisation

##### LT circuit

- 2 x compressors with “Cyclical”. One speed-controlled

- Safety monitoring of each compressor

- Common high pressure monitoring

- P0 setting –30 °C, P0 optimisation

##### **Gas cooling control:**

- Fans, speed-controlled

- Pressure regulation Pgc with reference from Sc3 and Sgc

- Pressure increase for heat recovery

##### **Containers:**

- Control of pressure in CO2 receiver

- Controlling the tank temperature for domestic water, 55 °C

##### **Safety functions:**

- Monitoring of Po, Pc, Sd and superheat in suction line

- MT-Po max = -5 °C, Po min = -35 °C

- MT-Pc max = 110 bar

- MT-Sd max = 120 °C

- LT-Po max = -5 °C, Po min = -45 °C

- LT-Pc max = 40 bar

- LT-Sd max = 120 °C

- SH min =  5 °C, SH max = 35 °C

### **4.1.2 Authorization**

Press the orange setup button with the spanner at the bottom of the display.

When the controller is supplied it has been set with standard authorization for different user interfaces. This setting should be changed and adapted to the plant. The changes can be made now or later.

##### 2. Select Authorization

You will use this button again and again whenever you want to get to this display. On the left-hand side are all the functions not shown yet. There will be more here the further into the setup we go.

Press the line **Authorization** to get to the user setup display.

##### 3. Change setting for the user ‘SUPV‘

##### 4. Select user name and access code

5. Carry out a new login with the user name and the new access code

Mark the line with the user name **SUPV** . Press the button **Change**

This is where you can select the supervisor for the specific system and a corresponding access code for this person.

The controller will utilize the same language that is selected in the service tool but only if the controller contains this language. If the language is not contained in the controller, the settings and readings will be shown in English.

To activate the new settings you must carry out a new login to the controller with the new user name and the relevant access code.

You will access the login display by pressing the icon at the top left corner of the display.

46 | BC186686443705en-000201

### **4.1.3 Unlock the configuration of the controllers**

2. Select Lock/Unlock configuration

The controller can only be configured when it is unlocked. The values can be changed when it is locked, but only for those settings that do not affect the configuration.

3. Select Configuration lock Press the blue field with the text **Locked**

4. Select Unlocked Select **Unlocked.**

### **4.1.4 System set-up**

2. Select System setup

3. Set system settings

All settings can be changed by pressing in the blue field with the setting and then indicating the value of the required setting.

In the first field you enter a name for what the controller will be controlling.  The text written in this field can be viewed at the top of all screens, together with the controller's address.

When the time is set the PC’s time can be transferred to the controller. When the controller is connected to a network, date and time will automatically be set by the system unit in the network. This also applies to change-over Daylight saving. Power failure, the clock will be kept running for at least 12 hours.

48 | BC186686443705en-000201

### **4.1.5 Set plant type**

##### 2. Select plant type

##### Press the line **Select plant type** .

##### 3. Set plant type

Our example The comments for the example are shown on the following pages, in the middle column.

In our example, the controller must regulate a Booster System, High Pressure Control Subsequent settings will then be available.

###### General

If you want to know more about the different configuration options, they are listed in the right column. The number refers to the number and picture in the column on the left. As the screen only shows the settings and readings that are required for a given setup, all possible settings have also been included in the right column.

##### **3 - Plant type Application selection**

Select one of the four controls

##### **Refrigerant**

The refrigerant is always CO2

**Condenser fan control**

Select whether the controller should control the condenser component / gas cooler. To be set later. **No of fans**

Set the number of relay outputs that will be used.

**Heat recovery**

##### 4. Set Common functions

##### 5. Quick basis setup

There are several pages, one after the other. The black bar in this field tells you which of the pages is currently displayed. Move between the pages using the + and - buttons. The settings for our example can be viewed in the display.

###### **Adjust only the lines with "Smart"**

Here you **must** adjust the overall pressure values for the system

- Regulation Pgc max

- Regulation Receiver reference.

The controller will then suggest values for all settings connected with this. The values can be seen in this display, but also later in the relevant setup. Fine adjustments can be made if necessary.

Heat recovery enabled. To be adjusted later on. **Quick setup** Not used

##### **4- Plant type continued**

##### **Select compressor application and no. of comp. MT**

##### **Select compressor application and no. of comp. LT**

##### **Select compressor application for IT**

##### **External main switch**

A switch may be connected for starting and stopping the regulation.

**Mon. Ext. Power loss** (signal from an UPS) Monitoring of external voltage. When selecting "yes", a digital input is allocated.

##### **Alarm output**

Here you may set whether or not it should be an alarm relay, and which priorities will activate it.

**I'm alive relay**

A relay will "release" if the regulation is stopped.

**Night select via DI**

Change to night-time operation at the signal for a DI input.

**Show advanced settings**

This function opens the advanced settings in the various menus.

##### **5 – Quick relative setup**

Easy Pgc max. provides a group setting for the overall pressure values.

Easy Prec ref. provides a group setting for the receiver controller..

### **4.1.6 Set control of MT compressors**

2. Select Suction group MT

##### 3. Set values for the reference

##### 4. Set values for capacity control

The configuration menu in the Service Tool has changed now. It  shows the possible settings for the selected plant type.

In our example we select the settings:

- P0 optimisation

- Suction pressure = -10 °C The settings are shown here in the display.

In our example we select: -VSD + single step

- 3 compressors

- P0 as signal to the regulation

- Cyclic

##### **3 - Reference mode**

Displacement of suction pressure as a function of external signals 0: Reference = set reference + night offset + offset from external 0 – 10 V signal

1: Reference = set reference + offset from P0 optimization **Setpoint** ( -80 – +30 °C) Setting of required suction pressure in °C

##### **Offset via Ext. Ref**

Select whether a 0 – 10 V external reference override signal is required

**Offset at max input** (-100 – +100 °C) Displacement value at max. signal (10) **Offset at min input** (-100 – +100 °C) Displacement value at min. signal (0 V) **Offset filter** (10 – 1800 sec)

Here you can set how quickly the reference must become effective.

##### **Night Offset via DI**

Select whether a digital input is required for activation of night operation. Night operation can alternatively be controlled via internal weekly schedule or via a network signal **Night Offset** (-25 – +25 K) Displacement value for suction pressure in connection with an active night setback signal (set in Kelvin) **Max reference** (-50 – +80 °C) Max. permissible suction pressure reference **Min reference** (-80 – +25 °C)

Min. permissible suction pressure reference

##### **4 - Compressor application**

Select the compressor application required

##### **Lead compressor type (For LT only)**

**•** Variable

The following options are available for variable: Speed FlexxCO2-4 FlexxCO2-6 Digital Scroll Stream 4 Stream 6 CRII 4 CRII 6

**No. of compressors** Set number of compressors (Total)

(max. 2 if parallel compressor is also selected)

**No. of unloaders** Set number of unloader valves **Ext. compressor stop** An external switch can be connected which will start and stop the compressor control.

##### **Control sensor**

Po is used for control

##### **Step control mode**

Select coupling pattern for compressors Cyclic: Runtime equalisation between compressors (FIFO) Best fit:  Best possible adaptation of capacity (minimum capacity jump)

50 | BC186686443705en-000201

##### **Pump down**

Select whether a pump down function is required on the last running compressor

**Pump down limit To** (-80 to +30 °C) Set the actual pump down limit

##### **Synchronous speed**

No: There will be two analog outputs available. Yes: There will be one analog output. **VSD min speed** (0.5 – 60.0 Hz)

Min. speed where the compressor must cutout **VSD start speed** (20.0 – 60.0 Hz)

Minimum speed for start of Variable speed drive (Must be set higher than “VSD Min. Speed Hz”) **VSD max speed** (40.0 – 120.0 Hz)

Highest permissible speed for the compressor motor

**VSD safety monitoring** Select this if input for monitoring of the frequency converter is required

**PWM period time** Period time for bypass valve (on time + off time)

**PWM Min. capacity** Minimum capacity in the period time (without a minimum capacity the compressor will not be cooled)

**PWM Start capacity** Minimum capacity at which the compressor will start (must be set to a higher value than "PWM Min. capacity")

##### **Load shed limits**

Select which signal is to be used for load limitation (only via network, a DI + network or two DI + network) **Load shed limit 1** Set max capacity limit for load shed input 1 **Load shed limit 2** Set max capacity limit for load shed input 2 **Override limit T0**

Any load below the limit value is freely permitted. If the T0 exceeds the value, a time delay is started. If the time delay runs out, the load limit is cancelled

##### **Override delay 1**

Max. time for capacity limit, if P0 is too high **Override delay  2** Max. time for capacity limit, if P0 is too high

##### **Easy PI Selection**

Group setting for the 4 control parameters: Kp, Tn, + acceleration and - acceleration. If the setting is set to “user defined” the 4 control parameters can be fine-tuned.

**Kp T0** (0.1 – 10.0)

Amplifications factor for PI regulation

##### **Tn T0**

Integration time for PI-regulation **+ Zone acceleration (A**<sup>**+**</sup> **)** Higher values result in a faster regulation **- Zone acceleration (A**<sup>**-**</sup> **)** Higher values result in a faster adjustment

##### **Advanced settings**

Select whether the advanced capacity control settings should be visible

##### **T0 filter**

Reduce changes in the Po reference

##### **Pc filter**

Reduce changes in the Pc reference

##### **Minimize cycling**

The control zone may vary for connections and disconnections. See Section 5.

**Initial start time** (15 – 900 s)

The time after start-up where the cut-in capacity is limited to the first compressor step.

##### **Unloading mode**

Select whether one or two capacity controlled compressors are allowed to be unloaded at the same time at decreasing capacity **AO filter**

Absorber changes at the analog output

##### **AO max. limit**

Limit the voltage on the analog output.

**5 - Compressors** In this screen the capacity distribution between the compressors is defined. Capacities that need to be set depend upon the “compressor apThe compressor capacity is set plication” and “Step control mode” that has been selected. in displaced volume per hour. m<sup>3</sup> /h. **Nominal capacity** (0.0 – 1000,0 m<sup>3</sup> /h) See compressor data. Set the nominal capacity for the compressor in question. For compressors with variable speed drive the nominal capacity must be set for the mains frequency (50/60 Hz) **Unloader**

##### 5. Set values for capacity of the compressors

Number of unload valves for each compressor (0-3)

**6 - Capacity distribution** The installation is dependent on the combination of compressors and coupling pattern. **Main step** Set the nominal capacity of the main step (Set the percentage of the relevant compressor’s nominal capacity)  0 – 100%. **Unload** Readout of the capacity on every unloading 0 – 100%.

##### 6. Set values for main step and any unloaders

**7 - Safety Emergency cap. day** The desired cut-in capacity for daily use in the case of emergency operations resulting from error in the suction pressure sensor/ media temperature sensor. **Emergency cap. night** The desired cut-in capacity for night operations in the case of In our example there are emergency operations resulting from error in the suction pressure no unloaders and hence no sensor/ media temperature sensor. changes. **Sd max limit** Max. value for discharge gas temperature 10 K below the limit, the compressor capacity should be reduced and the entire condenser capacity will be cutin. If the limit is exceeded, the entire compressor capacity will be cutout **Pc Max limit** Maximum value for the condenser pressure in bar 3 K below the limit, the entire condenser capacity will be cutin and the compressor capacity reduced. If the limit is exceeded, the entire compressor capacity will be In our example we select: cutout. - Safety limit for discharge **Tc max. limit** temperature = 120 °C Limit value read in °C - Safety limit for high condensing pressure = **Pc Max delay** 103.0 bar Time delay for the alarm Pc max - Safety limit for low suction **T0 Min limit** pressure =  -40 °C Minimum value for the suction pressure in °C If the limit is reduced, the entire compressor capacity will be cutout. **T0 Max alarm** Alarm limit for high suction pressure P0 **T0 Max delay** Time delay before alarm for high suction pressure P0. **Safety restart time** Common time delay before restarting the compressor. (Applicable to the functions: "Sd max. limit", Pc max. limit" and "T0 min. limit). **SH Min alarm** Alarm limit for min. superheat in suction line. **SH Max alarm** Alarm limit for max. superheat in suction line. **SH alarm delay** Time delay before alarm for min./max. superheat in suction line.

7. Set values for safe operation In our example we select: - Safety limit for discharge temperature = 120 °C

- Safety limit for high condensing pressure = 103.0 bar

- Safety limit for low suction pressure =  -40 °C

52 | BC186686443705en-000201

##### 8. Set monitoring of compressor

##### 9. Set operation time for compressor

##### 10. Set Misc. functions

**8 - Compressor safety Common safety** Choose whether an overall, common safety input for all compressors is desired. If the alarm is activated, all compressors will be cutout.

In our example we use:

- Common high-pressure pressure control for all compressors

**Oil pressure etc** Define here whether this type of protection should be connected. For "General", there is a signal from each compressor. **Individuel Sd pr. compressor** Select whether an Sd measurement should be made for each compressor.

- One general safety monitoring unit for each compressor

(The remaining options could have been selected if specific safety controls for each compressor had been required).

**Max discharge temp.** Cutout temperature. **Sd compressor alarm delay** Delay time for the alarm **Sd compressor safety cutout**

Set whether safety cut-out should be enabled

**9 - Minimum operation times** Configure the operation times here so "unnecessary operation" can be avoided. Restart time is the time interval between two consecutive starts. Set min. OFF-time for the **Safety timer** compressor relay **- Cutout delay** Set min. ON-time for the The time delay resulting from drop-out of automated safety compressor relay Set how often the compressor measures and until the compressor-error is reported. This setting is is allowed to start common for all safety inputs for the relevant compressor. **- Restart delay** Minimum time that a compressor should be OK after a safety cutThe settings only apply out. After this interval it can start again. to the relay that cuts the compressor motor in and out. **10 - Misc. functions** They do not apply to **Injection On** unloaders. Select this function if a relay must be reserved for the function. (The function must be wired to controllers with expansion valves If the restrictions overlap, the controller will use the longest in order to close liquid injection for the safety cut-out of the last restriction time. compressor.) Network: The signal is sent to the controllers via data communication. **Compressor start delay** Delay time for compessor start **Injection Off delay** Delay time for "Injection off" **Liq. inj suction line** Select the function if a liquid injection is required in the suction In our example we do not use line in order to keep the discharge gas temperature down. these functions. Regulation can be done either using a solenoid valve and a TEV, or using an AKV valve.

**AKV OD suction line** Opening degree of the valve in % **Inject start SH** Superheat value where the liquid injection starts **Inject diff SH** Differential when adjusted for superheat **Inject start Sd temp.** Start temperature for liquid injection in suction line **Inject diff. Sd temp.** Differential when adjusted on Sd **SH Min suction line** Minimum superheat in suction line **SH Max suction line** Maximum superheat in suction line **AKV period time** Periode time for AKV valve **Inject delay at start up** Delay time for liquid injection at start-up

### **4.1.7 Set control of LT compressors**

##### 2. Select Suction group LT

###### **In principle, the functions are the same as for MT.**

In principle, the same settings are carried out, but in the LT group it will be possible to select compressors with variable capacity. Speed FlexxCO2-4 FlexxCO2-6 Digital Scroll Stream 4 Stream 6 CRII 4 CRII 6

For the IT group the compressors must be speed controlled.

### **4.1.8 Setup control of condenser fans**

##### 2. Select Condenser fan control

In our example the condenser pressure is controlled on the basis of the Sgc and from Sc3 (floating reference). The settings shown here in the display.

##### **3 - PC reference**

##### **Control sensor** Sgc: The temperature at the outlet of the gas cooler **Reference Mode**

Choice of condenser pressure reference Fixed setting: Used if a permanent reference is required = “Setting” Floating: Used if the reference is changed as a function of Sc3 the external temperature signal, the configured "Dimensioning tm K"/"Minimum tm K" and the actual cut in compressor capacity. (Liquid is recommended for CO2 and heat recovery.)

##### **Setpoint**

Setting of desired condensing pressure in temperature **Min. tm**

Minimum average temperature difference between Sc3 air and Pc condensing temperature with no load.

##### **Dimensioning tm**

##### 3. Set control mode and reference

In our example we use a number of fans that are all speed-controlled in parallel. The settings shown here in the display.

Dimensioning average temperature differential between Sc3 air and Pc condensing temperature at maximum load (tm difference at max load, typically 2-3 K at CO2).

##### **Min reference**

Min. permitted condenser pressure reference

##### **Max reference**

Max. permitted condenser pressure reference

##### **Show Tc**

Set whether Tc should be displayed.

##### **4 - Capacity control Capacity control mode**

Select control mode for condenser Step: Fans are step-connected via relay outputs Step/speed: The fan capacity is controlled via a combination of speed control and step coupling Speed: The fan capacity is controlled via speed control (frequency converter) Speed 1.step: First fan speed controlled, rest step coupling **No of fans**

Set number of fans.

##### **Monitoring  fan safety**

Safety monitoring of fans. A digital input is used to monitor each fan.

##### **Fan speed type**

VSD (and normal AC motors) EC motor = DC controlled fan motors

54 | BC186686443705en-000201

4. Set values for capacity regulation

For your information the function ”Monitor fan safety” will require an input signal from each fan.

##### **VSD start speed**

Minimum speed for start of speed control (Must be configured higher than "VSD Min. Speed %")

**VSD min Speed**

Minimum speed whereby speed control is cut-out (low load).

**VSD safety monit.**

Choice of safety monitoring of frequency converter. A digital inlet is used for monitoring the frequency converter.

**EC Start capacity**

The regulation awaits this need to arise before supplying voltage to the EC motor

**EC voltage min**

Voltage value in % at 0% capacity

**EC voltage max**

Voltage value in % at 100% capacity

**EC Voltage abs. max**

Permissible live voltage for EC motor in % (overcapacity)

##### **Absolut max Sgc**

Max value for temperature at Sgc.  If the value is exceeded, the EC voltage will be raised to the value in “EC Voltage abs. max.”

##### **Control type**

Choice of control strategy P-band: The fan capacity is regulated via P-band control. The P band is "100/Kp"

PI-Control: The fan capacity is regulated by the PI controller. **Kp** Amplification factor for PI controller

##### **Tn**

Integration time for PI controller

##### **Capacity limit at night**

Setting of maximum capacity limit during night operations. Can be used to limit fan speed at night in order to limit the noise level.

### **4.1.9 Setup control of high pressure**

##### 2. Select HP control

##### 3. Set regulation values

The settings are shown here in the display

(The read outs "Pgc HR min" and "Pgc HR offset" are visible when Heat recovery is selected ON)

##### **3 - HP control Vhp output type**

Select the signal type for controlling the high pressure valve. - Voltage signal (ICMTS must have 0 – 10 V signal) - Stepper motor signal via AK-XM 208C

- 2 Stepper motor signals for parallel valves **Extra capacity offset**

Adjust how much the pressure shall be increased by when the function "Extra  capacity offset" is activated. **Pgc min.** Min. acceptable pressure in the gas cooler **Pgc max.** Max. acceptable pressure in the gas cooler

**Advanced settings Vhp min. OD** Restriction of the valve's degree of closing **Vhp max. OD** Restriction of the valve's degree of opening **Pgc max. limit P-band** P-band under "Pgc max" where the valve's degree of opening is increased **dT Subcool** Desired subcooling temperature **Kp** Amplification factor **Tn** Integration time **Pgc HR min.** Read the min. acceptable pressure in the high pressure circuit during heat recovery **Pgc HR offset** Set the pressure increase during heat recovery **Ramp down bar/min.** Here you may select how quickly the reference must be changed after a completed heat recovery **Temp. at 100 bar** Temperature at 100 bar. Here you may define the regulation curve during transcritical operation. Set the required temperature value.

If the regulation is stopped during high-pressure regulation, the pressure will rise.

The system must be dimensioned to the higher pressure; otherwise, there will be a loss of charge.

56 | BC186686443705en-000201

### **4.1.10 Setup control of receiver pressure**

2. Select Receiver control

##### 3. Set regulation values

The settings are shown here in the display

**3 - Receiver control Vrec output type** Select the signal type for controlling the gas bypass valve: - Voltage signal - Stepper motor signal via AK-XM 208C - 2 stepper motor signal  for parallel valves **Vrec min. OD** Limitation of the Vrec valve's degree of closing **Vrec max. OD** Limitation of the Vrec valve's degree of opening. **Show Trec** Set whether Trec should be shown in overview display 1. **Prec set point** Select the set point for the pressure in the receiver when IT compressor is stopped **Kp** Amplification factor **Tn** Integration time **Prec min.** Min. permissible  pressure in the receiver **Prec max.** Max. permissible pressure in the receiver (Also becomes regulation reference if the compressors are stopped with the "External compressor stop" function) **Prec min. limit P-band** P-band under "Prec min" where the ICMTS valve's degree of opening is increased **Prec max. limit P-band** P-band over "Prec max" where the ICMTS valve's degree of opening is decreased **Monitor liquid level** Choose whether liquid level should be monitored **Liquid alarm delay** Time delay for the alarm **Use hot gas dump** Select whether hot gas should be supplied if the receiver pressure falls too low

**Prec hot gas dump** Receiver pressure at which hot gas is turned on **Prec gas dump diff.** Difference at which hot gas is turned off again. **Show advanced settings IT Comp. start** Opening degree for the Vrec valve when the IT compressor is to start.

**IT Comp. delay**

The opening degree of the Vrec must be higher during the entire delay time before the relay pulls, thereby sending a signal to the IT controller.

**IT End delay**

The duration the IT compressor must have been stopped before regulation is transferred to Vrec

**IT Comp. Sgc min.**

The temperature limit for operation with IT compressor. Will not start when a lower value is detected, regardless of the opening degree of the Vrec valve.

### **4.1.11 Setup control of  heat recovery**

*[Figurtekst: 2. Select heat recovery]*

##### 3. Set regulation values

The settings are shown here in the display

##### **3 -Heat recovery Heat recovery mode**

Thermostat: Heat recovery operated from thermostat Digital input: Heat recovery operated from signal on a digital input.

##### **Heat recovery relay**

Choose whether an output is required that should be activated during heat recovery.

##### **Heat recovery cutout**

Temperature value where the thermostat cuts-out the heat recovery.

##### **Heat recovery  cutin**

Temperature value where the thermostat cuts-out the heat recovery.

##### **Use extern HR offset**

Here you define how the condensing pressure (HP) shall be regulated when the recovery circuit for heating requires heat:

- No. No HP offset (simple control) - Yes. Here the controller must receive a voltage signal or a temperature signal from an external source. The offset values that apply to the max. value must be defined.

##### **Input type select**

**-** Temperature control A signal from a temperature sensor must be received. Set the reference temperature.

- Consumer A 0 – 10 V or 0.5 V signal must be received.

- **Control type**

Regulation with external offset: select P or PI control **Temperature reference**

Reference settings at temperature control

##### **Kp**

Ampflication factor

##### **Tn consumer filter**

Averaging the consumer signal

##### **Fan HR min.**

Set point for fan control in the condenser when heat recovery is called for

##### **Fan HR offset**

Temperature increase from 50% to 100% in consumer signal

**Pgc HR min.**

Pressure value when heat recovery is called for

**Pgc HR offset**

Pressure increase from 0 to 50% in consumer signal.

58 | BC186686443705en-000201

### **4.1.12 Setup Display**

##### **3 - Display setup**

*[Figurtekst: 2. Select Display setup]*

##### 3. Define which readings are to be shown for the individual outputs

In our example, separate displays are not used. The setting is included here for information.

##### **Display**

The following can be read for the four outputs.. Comp. control sensor P0 in temperature P0 in barSs Sd Cond. control sensor Tc Pc bar Sgc Pgc bar Prec bar Trec Speed Compressor

##### **Unit readout**

Choose whether readings are to be in SI units (°C and bar) or (USunits °F and psi)

### **4.1.13 Setup Functions for General purpose**

*[Figurtekst: 1. Go to Configuration menu · 1 thermostat · 2. Select General purpose 1 pressostat · 1 voltage signal · 10 alarm signals · In our example, we do not · 1  PI-regulation · use functions for general · purposes, so the picture is · included for orientation. · Each function is described on · the following pages. · 3. Define number of required · functions]*

The following number of different functions can be defined: 1 thermostat

60 | BC186686443705en-000201

##### **Separate thermostat**

1. Select thermostat

2. Select actual thermostat

3. Define the required thermostat functions

In our example, separate thermostat functions are not used.

##### **3 - Thermostats**

The general thermostat can be used to monitor a temperature. The thermostat has a separate outlet to control external automation.

##### **Settings**

- Whether the thermostat should also be shown in overview display 1.

- (The function is always shown in overview display 2)

• Name • Which of the sensors is used **Actual temp** . Temperature measurement on the sensor that is attached to the thermostat **Actual state** Actual status on the thermostat outlet **Cut out temp.** Cut-out value for the thermostat **Cut in temp.** Cut-in value for the thermostat **High alarm limit** High alarm limit **Alarm delay high** Time delay for high alarm **Alarm text high** Indicate alarm text for the high alarm **Low alarm limit** Low alarm limit **Alarm delay low** Time delay for low alarm **Alarm text low** Indicate alarm text for low alarm

##### **Separate pressostat**

1. Select pressostat

**3 - Pressostat** Settings as the thermostat

In our example, separate 2. Select actual pressostat pressostat functions are not used.

3. Define the required pressostat functions

##### **Separate voltage signal**

1. Select Voltage input

2. Select actual voltage signal

##### 3. Define the required names and values attached to the signal

In our example we do not use this function, so the display has been included for your information only.

The name of the function may be xx and further down in the display the alarm texts may be entered.

The values ”Min. and Max. Readout” are your settings representing the lower and upper values of the voltage range.  2V and 10V, for example. (The voltage range is selected during the I/O setup).

The controller will reserve a relay output in the I/O setup. It is not necessary to define this relay if all you require is an alarm message via the data communication.

**3 - Voltage input** The general volt inlet can be used to monitor a external voltage signal. The function has a separate outlet to control external automatic controls.

##### **Settings:**

**Show on overview Name Select sensor (signal, voltage)** Select the signal which the function should use **Actual value** = read-out of the measurement **Actual state** = read-out of outlet status **Min. readout** State read-out values at minimum voltage signal **Max. readout** State read-out values at maximum voltage signal **Cutout** Cut-out value for outlet (scaled value) **Cutin** Cut-in value for outlet (scaled value) **Cutout delay** Time delay for cut-out **Cut in delay** Time delay for cut-in **High alarm limit** High alarm limit **High alarm delay** Time delay for high alarm **High alarm text** Set alarm text for high alarm **Low alarm limit** Low alarm limit **Low alarm delay** Time delay for low alarm **Low alarm text** Indicate alarm text for low alarm

##### **Separate alarm inputs**

1. Select General alarm inputs

2. Select actual alarm signal

3. Define the required names and values attached to the signal

In our example we do not use this function, so the display has been included for your information only.

**3 - General alarm input** This function can be used to monitor all kinds of digital signals. **No. of inputs** Set the number of digital alarm inputs **Adjust for each input**

- Show on overview

- Name

- Delay time for DI alarm (common value for all)

- Alarm text

62 | BC186686443705en-000201

##### **Separate PI function**

1. Select PI function

##### **3 - General PI Control**

The function can be used for optional regulation. **Adjust for each regulation**

   - Show on overview

2. Select actual PI-function

3. Define the required names and values attached to the function

In our example we do not use this function, so the display has been included for your information only.

- Quick settings Here is a list of suggestions for PI regulations:

- PI Name

- Control mode: Off, Manual or Auto

- Control type: P or PI

- External DI ctrl: Adjusted to On if there is an external switch that can start/stop the regulation.

- Input type: Choose which signal the regulation shall receive: Temperature, pressure, pressure converted to temperature, voltage signal, Tc, Pc, Ss, Sd etc.

- Reference: Either fixed or signal for the variable reference:: Choose between: : Non, temperature, pressure, pressure converted to temperature,  voltage signal, Tc, Pc, Ss, DI etc..

- Setpoint: If fixed reference is choosen

- Reading the total reference

- Output. Here you select the outlet function (PWM = pulse width modulated (fx AKV valve)), Stepper signal for a stepper motor or voltage signal.

- Alarm mode: Choose whether an alarm shall be attached to the function. If it is set to ON, alarm texts and alarm limits can be entered.

- Advanced ctrl. settings:

- Ref. X1, Y1 and X2,Y2: Points that define and limit the variable reference

- PWM period time: Period during which the signal has been on and off.

- Kp: Amplification factor

- Tn: Integration time

- Filter for reference: Duration for smooth changes to the reference

- Max. error:  Maximum permissible fault signal at which the integrator remains in the regulation

- Min. control output: Lowest permitted output signal

- Max. control output: Maximum permitted output signal

- Start up time: Time at startup at which the output signal is force-controlled

- Startup output: The output signal size at the startup time.

- Stop output signal. Size of the output signal when regulation is off.

### **4.1.14 Configuration of inputs and outputs**

##### 2. Select I/O configuration

##### 3. Configuration of Digital outputs

##### 4. Setup On/off inputs

The following displays will depend on the earlier definitions. The displays will show which connections the earlier settings will require. The tables are the same as shown earlier.

- Digital outputs

- Digital inputs

- Analog outputs

- Analog inputs

|**Load**|**Output**|**Module**|**Point**|**Active at**|
|---|---|---|---|---|
|Compressor 1 MT|DO1|1|12|ON|
|Compressor 2 MT|DO2|1|13|ON|
|Compressor 3 MT|DO3|1|14|ON|
|Compressor 1 LT|DO4|1|15|ON|
|Compressor 2 LT|DO5|1|16|ON|
|Valve and circulation pump hr|D06|1|17|ON|
|Fan|DO7|1|18|ON|
|Hot gas dump|DO8|1|19|ON|

We set up the controller’s digital outputs by keying in which module and point on this module each one of these has been connected to.

We furthermore select for each output whether the load is to be active when the output is in pos. **ON** or **OFF** .

|**Function**|**Input**|**Module**|**Point**|**Active at**|
|---|---|---|---|---|
|Compressor 1 MT Safety|AI1|2|1|Open|
|Compressor 2 MT Safety|AI2|2|2|Open|
|Compressor 3 MT Safety|AI3|2|3|Open|
|All compressors common safety MT|AI4|2|4|Open|
|Compressor 1 LT Safety|AI5|2|5|Open|
|Compressor 2 LT Safety|AI6|2|6|Open|
|All compressors common safety LT|AI7|2|7|Open|

We set up the controller’s digital input functions by keying in which module and point on this module each one of these has been connected to.

We furthermore select for each output whether the function is to be active when the output is in pos. **Closed** or **Open** . Open has been selected here for all the safety circuits. This means that the controller will receive signal under normal operation and register it as a fault if the signal is interrupted.

**3 - Outputs** The possible functions are the following: Comp. 1 Unloader 1-1 Unloader 1-2 Unloader 1-3 Do for Compressor. 2 and 3 Compressor run IT compressor release Injection suction line Injection ON Fan 1 / VSD Fan 2 - 4 HP Control Hot gas dump Heat recovery Alarm I'm alive relay Thermostat 1 Pressostat 1 Volt input 1 PI 1-PWM

**4 - Digital inputs** The possible functions are the following: Ext. Main switch Ext. compr. stop Ext. power loss Night setback Load shed 1 Load shed 2 All compressors: Common safety Comp. 1 Oil pressure safety Over current safety Motor protect. safety Disch. temp. safety Disch. press. safety General safety VSD comp. 1 Fault Do for Comp. 2 and 3 Fan 1 safety Do for fan 2-4 VSD cond safety AC limit Rec. low liquid level Rec. high liquid level Heat recovery DI 1 Alarm input DI 2-10 ... PI-1 Di ref External DI PI-1

64 | BC186686443705en-000201

##### 5. Configuration of Analog outputs

##### 6. Configuration of Analog Input signals

##### **5 - Analog outputs**

The possible signals are the following:

0 – 10 V

2 – 10 V

*[Figurtekst: 0 – 5 V · Function Output Module Point Type · 1 – 5V · Stepper signal for by-pass valve, CCM Step 1 2 9 CCM · Stepper output · Stepper signal for high pressure valve, CCMT Step 3 2 11 CCMT Stepper output 2 · Speed control, compressor MT AO1 3 5 0 - 10 V Stepper user defined: See · Speed control, compressor LT AO2 3 6 0 - 10 V section  "Miscellaneous" · Speed control, EC AO3 3 7 0 - 10 V · 6 - Analog inputs]*

##### **6 - Analog inputs**

The possible signals are the following: Temperature sensors:

- Pt1000

- PTC 1000

Pressure transmitters:

- AKS 32, -1 – 6 bar

- AKS 32R, -1 – 6 bar

- AKS 32, - 1 – 9 bar

- AKS 32R, -1 – 9 bar

- AKS 32, - 1 – 12 bar

- AKS 32R, -1 – 12 bar

- AKS 32, - 1 – 20 bar

*[Figurtekst: Sensor Input Module Point Type  • AKS 32R, -1 – 20 bar · Heat reclaim temperature Shr AI2 1 2 Pt 1000 • AKS 32, - 1 – 34 bar · Suction gas temperature - Ss MT AI4 1 4 Pt 1000 • AKS 32R, -1 – 34 bar · Disch. gas temperature - Sd MT AI5 1 5 Pt 1000 • AKS 32, - 1 – 50 bar · Suction pressure - P0 MT AI6 1 6 AKS 2050-59 • AKS 32R, -1 – 50 bar · Condenser pressure - Pc MT AI7 1 7 AKS 2050-159 • AKS 2050, -1 – 59 bar · Suction gas temperature - Ss LT AI9 1 9 Pt 1000 • AKS 2050, -1 – 99 bar · Disch. gas temperature - Sd LT AI10 1 10 Pt 1000 • AKS 2050, -1 – 159 bar · Suction pressure - P0 LT AI11 1 11 AKS 2050-59 • MBS 8250, -1 – 159 bar · Outdoor temp. Sc3Temp.  gas cooler outlet Sgc AI1AI2 33 12 Pt 1000Pt 1000 • User defined (only ratiomet- · ric, min. and max value of the · Gas cooler pressure Pgc AI3 3 3 AKS 2050-159 · Receiver pressure Prec AI4 3 4 AKS 2050-159 pressure range must be set)]*

Po suction pres. Ss suction gas Sd disch. temp. Pc Cond. Pres. Sc3 air on Ext. Ref. Signal

• 0 – 5 V, • 0 -10 V HP control Pgc Prec Sgc Shr Saux 1 Paux 1 Voltage input 1

- 0 -5 V,

- 0 -10 V,

- 1 – 5 V,

• 2 – 10 V PI-in temp PI-ref temp PI- in voltage PI-in pres. PI-ref pres.

### **4.1.15  Set alarm priorities**

2. Select Alarm priorities

##### 3. Set priorities for Suction group

Very many functions have an alarm connected. Your choice of functions and settings has connected all the relevant alarms that are current. They will be shown with text in the three pictures.

All alarms that can occur can be set for a given order of priority:

- ”High” is the most important one

- ”Log only” has lowest priority

• ”Disconnected” gives no action The interdependence between setting and action can be seen in the table.

|**Setting**|**Log**|**Ala**|**rm relay**|**selection**|**Net-**|**AKM-**|
|---|---|---|---|---|---|---|
|||Non|High|Low - High|**work**|**dest.**|
|High|X||X|X|X|1|
|Medium|X|||X|X|2|
|Low|X|||X|X|3|
|Log only|X|||||4|
|Discon-<br>nected|||||||

See also alarm text at the end of the manual.

##### 4. Set alarm priorities for condenser

In our example we select the settings shown here in the display

66 | BC186686443705en-000201

5. Set alarm priorities for thermostat and extra digital signals In our example we select the settings shown here in the display

### **4.1.16  Lock configuration**

##### 2. Select Lock/Unlock configuration

Press in the field against **Configuration lock.** Select **Locked** .

The setup of the controller has now been locked. If you subsequently want to make any changes in the controller’s setup, remember first to unlock the configuration.

##### 3. Lock Configuration

**The controller will now make a comparison of selected functions and define inputs and outputs. The result can be seen in the next section where the setup is controlled.**

68 | BC186686443705en-000201

### **4.1.17  Check configuration**

##### 2. Select  I/O configuration

##### 3. Check configuration of Digital Outputs

##### 4. Check configuration of Digital Inputs

The setup of the digital outputs appears as it is supposed to according to the wiring made.

The setup of the digital inputs appears as it is supposed to according to the wiring made.

##### **This control requires that the setup is locked**

(Only when the setup is locked are all settings for in- and outputs activated.)

##### **An error has occurred, if you see the following:**

- A **0 – 0** next to a defined function. If a setting has reverted to 0-0, you must control the setup again. This may be due to the following: • A selection has been made of a combination of module number and point number that does not exist.

- **•** The selected point number on the selected module had been set up for something different.

- The error is corrected by setting up the output correctly. Remember that the setup must be unlocked before you can change module and point numbers.. The settings are shown on a **RED** background. If a setting has turned red, you must control the setup again. This may be due to the following: • The input or the output has been set up; but the setup has later been changed so that it should no longer be applied.

- The problem is corrected by setting **module number to 0 and point number to 0.** Remember that the setup must be unlocked before you can change module and point numbers.

|5. Check configuration of Analog||
|---|---|
|i<br>Outputs||
||The setup of the analog outputs appears as it is supposed to<br>according to the wiring made.|
|Press the + button to go to<br>the next page||
|6. Check configuration of Analog<br>Inputs||
||The setup of the analog inputs appears as it is supposed to ac-<br>cording to the wiring made.|

70 | BC186686443705en-000201

### **4.2 Check of connections**

##### 2. Select I/O status and manual

##### 3. Check Digital Outputs

##### 4. Check Digital Inputs

Before the control is started we check that all inputs and outputs have been connected as expected. **This controls requires that the setup is locked** By means of the manual control of each output it can be checked whether the output has been correctly connected.

**AUTO** The output is controlled by the controller **MAN OFF** The output is forced to pos. OFF **MAN ON** The output is forced to pos ON Cut out the safety circuit for compressor 1. Check that LED DI1 on the extension module (module 2) goes out. Check that the value of the alarm for the safety monitoring of compressor 1 changes to **ON.** The remaining digital inputs are checked in the same way.

5. Check Analog outputs

Set Control of output voltage to manual Press in the **Mode** field. Select **MAN** .

Press in the **Value** field Select for example **50%** .

Press **OK** .

On the output you can now measure the expected value: In this example 5 volts

Example of the connection between a defined output signal and a manual set value.

*[Figurtekst: Definition Settin g · 0 % 50 % 100 % · 0 - 10 V 0 V 5 V 10 V · 1 - 10 V 1 V 5,5 V 10 V · 0 - 5 V 0 V 2,5 V 5 V · 2 - 5 V 2 V 3,5 V 5 V]*

6. Put the control of the output voltage back to automatic

##### 7. Check Analog inputs

Check that all sensors show sensible values. In our case we have no values. This may be due to the following:

- The sensor has not been connected.

- The sensor is short-circuited.

- The point or module number has not been set up correctly.

- The configuration is not locked.

72 | BC186686443705en-000201

### **4.3 Check of settings**

1. Go to the overview

2. Select suction group

3. Move on through all the individual displays for the suction group

Before the control starts, we check that all the settings are as they should be.

The overview display will now show one line for each of the general functions. Behind each icon there is a number of displays with the different settings. It is all these settings that have to be checked.

Change displays with the +- button. Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

4. Check the individual pages

The last page contains control data

5. Go back to the overview. Repeat for LT

6. Select condenser group

7. Move on through all the individual displays for the condenser group.

Change displays with the +- button. Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

8. Check the individual pages

9. Go back to the overview and move on to the rest of the functions.

##### 10. General functions

When all the functions in overview display 1 have been reviewed, it is time to look at the "General functions" in overview display 2. Press the + button to access.

The first is the thermostat group

Check the settings.

11. Then the pressure switch group

The last page contains reference settings.

All the defined general functions are shown in overview display 2.

In addition to always being shown in display 2, functions can be selected to be shown in display 1. Individual functions can be selected for display in display 1 via the "Show in overview display" setting.

Check the settings.

12. Proceed with the remaining functions.

13. The controller setup has been completed.

74 | BC186686443705en-000201

### **4.4 Schedule function**

2. Select schedule

3. Setup schedule

|Before regulation is started we will set the schedule function for<br>the night setback of the suction pressure.<br>In other cases where the controller is installed in a network with<br>one system unit, this setting may be made in the system unit<br>which will then transmit a day/night signal to the controller.|
|---|
|Press a weekday and set the time for the day period.<br>Continue with the other days.<br>A complete weekly sequence is shown in the display.|

### **4.5 Installation in network**

##### 1. Set the address (here, for example 3)

Turn the right-hand address switch so that the arrow will point at 3. The arrow of the two other address switches must point at 0.

##### 2. Push the Service Pin

Press down the service pin and keep it down until the Service Pin LED lights up.

##### 3. Wait for answer from the system unit

Depending on the size of the network it may be up to one minute before the controller receives an answer as to whether it has been installed in the network.

When it has been installed the Status LED will start to flash faster than normal (once every half second). It will continue with this for about 10 minutes

##### 4. Carry out new login via Service Tool

The controller has to be remote-monitored via a network. In this network we assign address number 3 to the controller. The same address must not be used by more than one controller in the same network.

##### **Requirement to the system unit**

The system unit must be:

- AK-SM 720

- AK-SM 800 series

- AK-SM 8xxA series

If there is no answer from the system unit

If the Status LED does not start flashing faster than normal, the controller has not been installed in the network. The reason for this may be one of the following:

**The controller has been assigned an address out of range** Address 0 cannot be used.

Check the reserved addresses in Chapter 2.3 Controller.

##### **The selected address is already being used by another controller or unit in the network:**

The address setting must be changed to another (vacant) address.

**The wiring has not been carried out correctly. The termination has not been carried out correctly.**

The data communication requirements are described in the document: ”Data communication connections to ADAP-KOOL® Refrigeration Controls” RC8AC.

If the Service Tool was connected to the controller while you installed it in the network, you must carry out a new login to the controller via the Service Tool.

76 | BC186686443705en-000201

### **4.6 First start of control**

##### **Check alarms**

1. Go to the overview

Press the blue overview button with the compressor and condenser at the bottom left of the display.

##### 2. Go to the Alarm list

Press the blue button with the alarm bell at the bottom of the display.

##### 3. Check active alarms

In our case, we have a series of alarms. We will tidy them up so that we only have those that are relevant.

##### 4. Remove cancelled alarm from the alarm list

Press the red cross to remove cancelled alarms from the alarm list.

##### 5. Check active alarm again

In our case an active alarm remains because the control has stopped. This alarm must be active when control has not started. We are now ready for the startup of control. Please note that active plant alarms are automatically cancelled when the main switch is in pos. OFF. If active alarms appear when the control is started the reason for these should be found and remedied.

### **4.6.1 Start the control**

1. Go to Start/Stop display

Press the blue manual control button at the bottom of the display.

Press in the field against **Main switch** . Select **ON** .

2. Start control

The controller will now start controlling the compressors and the fans. Note: Control does not start until both the internal and external switch are “ON”. Any external compressor stop breaker must be ON for the compressors to start.

78 | BC186686443705en-000201

### **4.6.2 Manual capacity control**

1.  Go to overview

2. Select suction group

If you need to manually adjust the capacity of the compressors, you can use the following procedure:

Press the suction group button for the suction group that is to be controlled manually.

3. Set capacity control to manual

4. Set capacity in percent Press in the blue field against **Manual capacity** .

##### **WARNING!**

If you force control the compressors, the oil management will be shut down. This could cause compressor damages. (If the wiring of the compressors includes safety relays, monitoring will continue. See Regulating functions.) Press the blue field against **Control mode** Select **MAN** . Set the capacity to the required percentage. Press **OK** .

### **5. Regulating functions**

This section describes how the different functions work

### **5.1 Suction groups**

### **5.1.1 Controlling sensor**

The capacity distributor can regulate according to the suction pressure P0.

The IT compressors are also regulated according to the suction pressure, but the signal is received from the receiver - Prec. See page 108 for IT description

An error in the controlling sensor will mean that regulation continues with fx. 50% cutin in daily operation and fx. 25% cut-in at night, but for a minimum of one step.

### **5.1.2 Reference**

The reference for the regulation can be defined in 2 ways:

Either

P0Ref = P0 setting + P0 optimization or

P0Ref = P0 setting + night displacement + Ext. Ref

##### **P0 setting**

A basic value for the suction pressure is set.

##### **P0 optimization**

This function displaces the reference so that regulation will not take place with a lower suction pressure than required. The function cooperates with controllers on the individual refrigeration appliances and a system manager. The system manager obtains data from the individual regulations and adapts the suction pressure to the optimum energy level. The function is described in the manual for the System manager. With this function you can read which appliance is most heavily loaded at the moment as well as the displacement allowed for the suction pressure reference.

If a short change in the suction pressure is needed (for example, up to 15 minutes in connection with defrosting) the functions can be applied. Here the PO-optimisation will not have time to compensate for the change.

##### **Override with a 0 - 10 V signal**

When a voltage signal is connected to the controller the reference can be displaced. In the setup it is defined how big a displacement is to take place at max. signal (10 V) and at min. signal.

##### **Limitation of reference**

To safeguard yourself against a too high or too low regulation reference, a limitation of the reference must be set.

*[Figurtekst: P0 ref · Max. · Min.]*

##### **Forced operation of the compressor capacity in the suction group**

A forced operation of the capacity can be carried out which disregards the normal regulation. Depending on the selected form of forced operation, the safety functions will be cancelled.

##### **Forced operation via overload of requested capacity**

The control is set to manual and the desired capacity is set in % of the possible compressor capacity.

##### **Forced operation via overload of digital outlets**

The individual outputs can be set to MAN ON or MAN OFF in the software. The control function disregards this but an alarm is sent out that the outlet is being overridden.

##### **Forced operation via change-over switches**

If the forced operation is done with the switch-over on the front of an expansion model, this is not registered by the control function and no alarm is sounded. The controller continues to run and couples with the other relays.

##### **Night displacement**

The function is used to change the suction pressure reference for night time operation as an energy saving function. With this function the reference can be displaced by up to 25 K in positive or negative direction. (When you displace to a higher suction pressure, a positive value is set). Displacement can be activated in three ways:

- Signal on an input

- From a master gateway’s override function

- Internal time schedule

The “night displacement” function should not be used when regulation with the override function “P0-optimisation” is performed. (Here the override function will itself adapt the suction pressure to the max. permissible).

80 | BC186686443705en-000201

### **5.1.3 Capacity control of compressors**

##### Example:

3 compressor of equal size  - The capacity curve will look like this

##### **Capacity control**

AK-PC 772A can control up to 3 compressors on MT and 2 on LT. (For parallel compressor operation, however, the system can only control 2 on MT and 2 on LT.) Each compressor can have up to 3 unloaders. One or two of the compressors can be equipped with speed regulation.

The cut-in capacity is controlled by signals from the connected pressure transmitter/temperature sensor and the set reference. Set a neutral zone around the reference .

In the neutral zone, the regulating compressor controls the capacity so that pressure can be maintained. When it can no longer maintain the pressure within the neutral zone, the controller will cut out or cut in the next compressor in the sequence. When further capacity is either cut out or cut in, the capacity from the regulating compressor will be modified accordingly to maintain the pressure within the neutral zone (only where the compressor has variable capacity).

- When the pressure is higher than the “reference + a half neutral zone”, cut-in of the next compressor (arrow up) is permitted.

- When the pressure is lower than the “reference - a half neutral zone”, cut-out of a compressor (arrow down) is permitted.

- When the pressure is within the neutral zone, the process will continue with the currently activated compressors. Unload valves (if present) will activate, depending on whether suction pressure is above or below the reference value.

*[Figurtekst: Suction pressure P0]*

Cut-out of the last compressor stage:

Normally, the last compressor step will only be cut-out when the required capacity is 0% and the suction pressure is below the neutral zone.

##### **Operation time first step**

At start-up the refrigeration system must have time to be stable before the PI controller takes over the control.  For this purpose at start-up of a plant  a limitation is made of the capacity so that only the first capacity step will cutin after a set period (to be set via "runtime first step").

##### **Pump down function:**

To avoid too many compressor starts/stops with low load, it is possible to define a pump down function for the last compressor.

If the pump down function is used, the compressors will be cutout when the actual suction pressure is down to the configured pump down limit.

Note that the configured pump down limit should be set higher than the configured safety limit for low suction pressure "Min Po".

For the IT compressor, pump down will be controlled by the receiver and MT temperature.

##### **Change capacity**

The controller will cutin or cutout capacity based on these basic rules:

##### Increase capacity:

The capacity distributor will start extra compressor capacity as soon as the requested capacity has increased to a value, which allows the next compressor step to start. Referring to below example - a compressor step is added as soon as there is “Room” for this compressor step below the requested capacity curve.

##### Decrease capacity:

The capacity distributor will stop compressor capacity as soon as the requested capacity has decreased to a value, which allows the next compressor to stop. Referring to below example - a compressor step is stopped as soon as there is no more “Room” for this compressor step above the requested capacity curve.

##### **Variable integration time**

There are two parameters, so Tn can be made variable. This allows control to be more rapid, the further pressure deviates from the reference.

The A+ setting will lower Tn when the pressure is above the reference, and the A- setting will lower Tn when the pressure is below the reference.

Tn has been set to 120 s in the graph below, and falls to 60 s if the pressure is above the reference and to 40 s if the pressure is below the reference.

Above the reference: Set Tn divided by the A+ value. Below the reference: Set Tn divided by the A- value. The controller calculates the curve, such that regulation is smooth.

##### **Regulation  parameters**

To make it easier to start up the system, we have grouped regulation parameters into sets of commonly used values, called "Easysettings". Use these to choose between sets of settings appropriate for a system which responds slowly or quickly. The factory setting is 5.

If you need to fine tune the control, select the "User defined" setting. All parameters can then be freely adjusted.

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

### **Capacity distribution methods**

The capacity distributor can work based on 2 distribution principles.

##### **Coupling pattern – Cyclical operation:**

This principle is used if all compressors are of the same type and size.

The compressor cuts-in and cuts-out in accordance with the "First In First Out" principle (FIFO) to equalise operating hours between the compressors.

Speed-regulated compressors will always be cut in first, and the variable capacity is used to fill capacity gaps between the subsequent steps.

##### Timer restrictions and safety cut outs

If a compressor is prevented from starting because it is “hanging” on the restart timer or is safety cut out, this step is replaced by another compressor.

##### Operating time equalisation

The operating hour equalizing is carried out between compressors of the same type with the same total capacity.

- -At the different startups the compressor with the lowest number of operating hours will be started first.

- At the different stops the compressor with the highest number of operating hours will be stopped first.

- For compressors with several steps, the operating time equalizing is carried out between the compressors’ main steps.

- The left column shows the operating hours, according to which the controller equalises.

- The middle column shows (as a percentage) to what extent the individual compressor has been activated within the last 24 hours.

- The right column shows the compressor's current operating time. The value should be reset when the compressor is replaced.

##### **Coupling pattern – Best fit operation**

This principle is used if the compressors are of different sizes. The capacity distributor will cut-in or cut-out the compressor capacity in order to ensure the least possible capacity jump. Speed-regulated compressors will always be cut in first, and the variable capacity will be used to fill capacity gaps between the subsequent steps.

##### Timer restrictions and safety cut outs

If a compressor is prevented from starting because it is “hanging” on the restart timer or is safety-cut out, this step is replaced by another compressor or another combination.

82 | BC186686443705en-000201

### **Power pack types – compressor combinations**

The controller is able to control power packs with compressors of various types:

##### Unloading mode = 1

Here the capacity distributor allows only one of the compressors to be unloaded at a time. The advantage of this setting is that it avoids operating with several compressors unloaded , which is not energy efficient.

- One or two speed controlled compressor

- Capacity controlled piston compressors with up to 3 unloader valves

- Single step compressors – piston

The chart below shows the compressor combination which the controller is capable of controlling. The chart also shows which coupling pattern can be set for the individual compressor combi- nations.

|Combination|Description|Coup<br>patte|ling<br>rn|
|---|---|---|---|
|||Cyclical|Best fit|
||One-step compressors. *1|x|x|
||A compressor with an unload<br>valve, combined with one-step<br>compressors. *2|x||
||Two compressors with unload<br>valves, combined with one-step<br>compressors. *2|x||
||All compressors with unload<br>valves. *2|x||
||A speed-regulated compres-<br>sor combined with one-step<br>compressors. *1 and *3|x|x|
||A speed-regulated compres-<br>sor combined with several<br>compressors with unload valves.<br>*2 and *3|x||
||Two speed-regulated compres-<br>sors combined with one-step<br>compressors *4|x|x|

##### For example:

Two capacity-regulated compressors of 20 kW, each with 2 unload valves, cyclical coupling pattern.

*[Figurtekst: Pc Sd Cap.% C2.2 · Ss Po · C2.1 C2.1 C2.2 · C2 C2 C2 C2.1 C2.2 · C1.2 C1.2 C1.2 C1.2 C2 C2.1 C2.2 · C1.1 C1.1 C1.1 C1.1 C1.1 C1.1 C2 C2.1 C2.1 · 20 kW 20 kW C1 C1 C1 C1 C1 C1 C1 C1 C2 C2 C2 t]*

- For decreasing capacity, the compressor with the most operating hours is unloaded (C1).

- When C1 is completely unloaded, it is cut-out before compressor C2 is unloaded.

##### Unloading mode = 2

Here the capacity distributor allows two compressors to be unloaded while capacity is decreasing.

The advantage of this setting is it reduces the number of compressor start/stops.

##### For example:

Two capacity-regulated compressors of 20 kW, each with 2 unload valves, cyclical coupling pattern.

*[Figurtekst: Pc Sd Cap.% C2.2 · Ss Po · C2.1 C2.1 C2.2 · C2 C2 C2 C2.1 C2.2 · C1.2 C1.2 C1.2 C1.2 C2 C2.1 C2.1 · C1.1 C1.1 C1.1 C1.1 C1.1 C1.1 C2 C2 C2.1 · 20 kW 20 kW C1 C1 C1 C1 C1 C1 C1 C1 C1 C2 C2 t]*

   - For decreasing capacity, the compressor with the most operating hours is unloaded (C1).

   - When C1 is completely unloaded , compressor C2 with one-step is unloaded before C1 is cut out.

- *1) For a cyclical coupling pattern, the one-step compressors must be the same size.

*2) For compressors with unload valves, it is generally true that they must have the same size, the same number of unload valves (max 3) and the same sized main steps. If compressors with unload valves are combined with one-step compressors, all compressors should be the same size.

- *3) Speed-regulated compressors can have different sizes in relation to subsequent compressors.

*4) When two speed-regulated compressors are used, they must have the same frequency range. For cyclical coupling patterns, the two speed-regulated compressors should be the same size and the subsequent one-step compressor should also be the same size.

##### Attention!

Relay outputs must not be inverted at unloader valves. The controller inverts the function itself.

There will be no voltage at the bypass valves when the compressor is not in operation.

Power is connected immediately before the compressor is started.

The following is a description of some general rules for handling capacity-regulated compressors, speed-regulated compressors and also for two speed-regulated compressors.

##### **Capacity-regulated compressors with unload valves**

"Unloader control mode" determines how the capacity distributor should handle these compressors.

##### **Speed control compressors:**

The controller is able to use speed control on the leading compressor in different compressor combinations. The variable part of the speed controlled compressor is used to fill in capacity gaps of the following compressor steps.

##### General regarding handling:

One of the defined capacity steps for the compressor regulation may be connected to a speed control unit that may be a frequency converter type VLT, for example.

An output is connected to the frequency converter’s ON/OFF input and at the same time an analog output ”AO” is connected to the frequency converter’s analog input.

The ON/OFF signal will start and stop the frequency converter and the analog signal will indicate the speed. It is only the compressor defined as compressor 1 (1+2) that can be speed controlled.

When the step is in operation it will consist of a fixed capacity and a variable capacity. The fixed capacity will be the one that corresponding to the mentioned min. speed and the variable one will lie between the min. and max. speed. To obtain the best regulation the variable capacity must be bigger than the subsequent capacity steps it has to cover during the regulation. If there are major short-term variations in the plant’s capacity requirement it will increase the demand for variable capacity.

##### This is how you cut the step in and out:

*[Figurtekst: Max. · Start · Min. · 0 t · ON · OFF]*

##### Cutin

##### Controlling – increasing capacity

If the need for capacity becomes larger than “Max. Speed” then the subsequent compressor step will be cut-in. At the same time, the speed on the capacity step will be reduced so the capacity is reduced with a size that corresponds to exactly the cut-in compressor step. Thereby a completely "frictionless" transition is achieved without capacity holes (refer also to sketch).

*[Figurtekst: V · Max . · V Max . · Star t 2 Star t · Mi n. V Min . V · 1 1]*

##### Controlling – decreasing capacity

If the capacity requirement becomes less than “Min. speed” then the subsequent compressor step will be cut-out. At the same time, the speed on the capacity step is increased so the capacity is increased with a size that corresponds to exactly the cut-out compressor step.

##### Cut-out

The capacity step will be cut-out when the compressor has reached “Min. Speed” and the requested capacity has dropped to 1%.

Timer restriction on speed controlled compressor

If a speed controlled compressor is not allowed to start due to a timer restriction, no other compressor is allowed to start. When the timer restriction has expired the speed controlled compressor will start.

##### Safety cutout on speed controlled compressor

If the speed controlled compressor is cutout on safety other compressors are allowed to start. As soon as the speed controlled compressor is ready to start it will be the first compressor to start.

As mentioned before the variable part of the speed capacity should be bigger than the capacity of the following compressor steps in order to achieve a capacity curve without “holes”. In order to illustrate how the speed control will react at different pack combinations a couple of examples will be given here:

The speed-controlled compressor will always be the first to start and the last to stop. The frequency converter will be started when a capacity requirement corresponding to the mentioned ”Start speed” arises (the relay output changes to ON and the analog output is supplied with a voltage corresponding to this speed). It is now up to the frequency converter to bring the speed up to ”Start  speed”.

The capacity step will now be cut in and the required capacity determined by the controller. The start speed always ought to be set so high that a fast lubrication of the compressor  is obtained during the start.

84 | BC186686443705en-000201

##### **a) Variable capacity bigger than following compressor steps:**

When the variable part of the speed controlled compressor is bigger than the following compressors there will be no “holes” in the capacity curve.

##### Example:

1 speed controlled compressor with a nominal capacity at 50Hz of 10kw - Variable speed range 30 – 90Hz 2 one step compressors of 10 kW

Fixed capacity =  30 HZ / 50 HZ x 10 kW =  6 kW Variable capacity = 60 HZ / 50Hz x 10 kW = 12 kW

##### The capacity curve will look like this:

*[Figurtekst: Requested · Pc Sd 40 kW capacity % · Ss Po · 90 Hz C1 C1 80 Hz · 20 kW · 40 Hz · 30 Hz · C1 C3 C3 C1 · Start spee d · 10 kW 10 kW 10 kW Min. speed · 30 – 90 Hz C1 C2 C2 C2 C2 C1 · Time]*

As the variable part of the speed controlled compressor is bigger than the following compressor steps, the capacity curve will be without holes.

- 1) The speed controlled compressor will be cutin when the requested capacity has reached the start speed capacity.

- 2) The speed controlled compressor will increase speed until it reaches max speed at a capacity of 18 kW.

- 3) The one step compressor C2 of 10 kW is cut in and the speed on C1 is reduced too so that it corresponds to 8kW (40Hz)

- 4) The speed controlled compressor will increase speed until the total capacity reaches 28 kw at max speed

- 5) The one step compressor C3 of 10 kW is cut in and the speed on C1 is reduced too so that it corresponds to 8kW (40Hz)

- 6) The speed controlled compressor will increase speed until the total capacity reaches 38 kw at max speed

- 7) When reducing capacity the one step compressors will be cut out when the speed on C1 is at minimum

##### **b) Variable part smaller than following compressor steps:**

If the variable part of the speed controlled compressor is smaller than the following compressors there will be “holes” in the capacity curve.

##### Example:

1 speed controlled compressor with a nominal capacity at 50Hz of 20kw - Variable speed range 25 – 50Hz 2 one step compressors of 20 kW Fixed capacity =  25 HZ / 50 HZ x 20 kW =  10 kW Variable capacity = 25 HZ / 50Hz x 20 kW = 10 kW

##### The capacity curve will look like this:

*[Figurtekst: Requested · 60 kW capacity % · Pc Sd · Ss Po · 50 Hz C1 50 Hz · 40 k W · 25 Hz 25 Hz · C1 C3 C1 · 20 k W · 20 kW 20 kW 20 kW Start spee d · 25 – 50 Hz Min. spee d · C1 C2 C2 C2 C2 C1 · Time]*

As the variable part of the speed controlled compressor is smaller than the following compressor steps the capacity curve will have some holes that can not be filled out by the variable capacity.

- 1) The speed controlled compressor will be cutin when the

- requested capacity has reached the start speed capacity.

- 2) The speed controlled compressor will increase speed until it reaches max speed at a capacity of 20 kw.

- 3) The speed controlled compressor will stay at max speed until the requested capacity has increased to 30 kW.

- 4) The one step compressor C2 of 20 kW is cut in and the speed on C1 is reduced to min. so that it corresponds to 10kW (25Hz). Total capacity = 30 kW.

- 5) The speed controlled compressor will increase speed until the total capacity reaches 40 kW at max speed

- 6) The speed controlled compressor will stay at max speed until the requested capacity has increased to 50 kW.

- 7) The one step compressor C3 of 20kW is cut in and the speed on C1 is reduced to min. so that it corresponds to 10kW (25Hz). Total capacity = 50 kW

- 8) The speed controlled compressor will increase speed until the total capacity reaches 60 kw at max speed

- 9) When reducing capacity the one step compressors will be cut out when the speed on C1 is at minimum speed.

##### **Two speed-regulated compressors**

The controller is capable of regulating the speed of two compressors of the same or different sizes. The compressors can be combined with one-step compressors of the same or different sizes, depending on the choice of coupling pattern.

##### General regarding handling:

Generally, the two speed-regulated compressors are managed according to the same principle as for one speed-regulated compressor. The advantage of using two speed-regulated compressors is that it allows for a very low capacity, which is an advantage for low loads. At the same time, it produces a very large, variable regulating area.

Compressor 1 and 2 both have their own relay outlets to start/ stop separate frequency converters, for example of type VLT. Both frequency converters use the same analog output signal AO which is connected to the frequency converters’ analog signal input (they can, however, be configured to run individual signals). The relay outputs will start and stop the frequency converter and the analog signal will indicate the speed.

The precondition for using this regulating method is that both compressors have the same frequency range.

The speed-regulated compressors will always be the first to start and the last to stop.

*[Figurtekst: Pc Sd · Ss Po · 20 kW 20 kW 40 kW · 30 – 60 Hz]*

##### Cut-in

The first speed-regulated compressor will be started when there is a capacity requirement which matches the setting. The "Start speed" (relay outlet changes to on and the analog outlet is supplied with a voltage that matches this speed). It is now up to the frequency converter to bring the speed up to the "Start speed".

The capacity step will now be cut in and the desired capacity determined by the controller.

The start speed should always be set so high that a good lubrication of the compressor is quickly reached during start-up. For a cyclical coupling pattern, the subsequent speed-regulated compressor will be cut in when the first compressor runs at max. speed and the desired capacity has reached a value that allows the cut-in of the next speed-regulated compressor at start speed. Afterwards, both compressors will be cut in together and will run in parallel. The following one-step compressors will be cut in and out in accordance with the selected coupling pattern.

*[Figurtekst: Analogue output · Max. speed · Start speed · Min. speed · Time · Comp. 1 · Comp. 2 · Comp. 3]*

##### Controlling – decreasing capacity

The speed-regulated compressors will always be the last compressors running.

When the capacity requirement during cyclical operations becomes less than "Min. speed" for both compressors, the speedregulated compressor with the most operating hours will be cut-out. At the same time, the speed of the last speed-regulated compressor increases so that the capacity is increased to the level that matches the cut-out compressor’s step.

##### Cutout

The last speed-regulated compressor will be cut-out when the compressor has reached ”Min. speed” and the capacity requirement (desired capacity) has decreased to under 1% (see however the section on the pump down function).

##### Timer restriction and safety cut-outs

Timer limits and safety cut-outs on speed-regulated compressors should be managed in accordance with the general rules for individual coupling patterns.

Short descriptions and examples are given below of the handling of two speed-regulated compressors for the individual coupling patterns. For a more detailed description, refer to the appendix at the end of the chapter.

##### Cyclical operation

For cyclical operations, both speed-regulated compressors will have the same size and operating hours will be equalized between the compressors in accordance with the First-in-First-Out Principle (FIFO). The compressor with the least operating hours will be the first to start. The following speed-regulated compressor will be cut in when the first compressor runs at max.  speed and the desired capacity has reached a value that allows the cut-in of the next speed-regulated compressor at start speed. Afterwards, both compressors will be cut in together and they will run in parallel. The following one-step compressors will be cut in and out in accordance with First-In-First-Out principle in order to equalise operating hours.

86 | BC186686443705en-000201

##### **Two independent speed-regulated compressors**

If the two speed-regulated compressors need to be controlled asynchronously, they must each have their own analogue voltage signal.

The controller first starts one of the speed-regulated compressors. If more capacity is required, the other speed-regulated compressor is started, and then the single compressors.

*[Figurtekst: Analogue outputs · Max. speed · Nominal · Start speed · Min. speed]*

The first is run up to maximum speed. Number two is then activated and run up to nominal speed – and kept there. The speed of number one is reduced at the same time, so the capacity is balanced. All variations are now handled by number one.  If number one reaches maximum speed, number two will also be raised. If number one reaches minimum speed, it will be kept there while number two takes over the variation below its nominal speed. When engaging and disengaging, the total hours of operation for the compressors is compared, so they are run an equal number of hours.

### **Compressor timers**

##### **Time delays for cutins and cutouts**

To protect the compressor against frequent restarts three time delays can be put in.

- A minimum time to run from a compressor’s startup and until it may be restarted.

- A minimum time (ON-time) for the compressor to operate before it may be stopped again.

- A minimum OFF time to run from a compressor stops and until it may be restarted

When unloaders are cut in and out, the time delays will not be used.

##### **Timer**

The operating time of a compressor motor is registered continuously. You can read out:

- operating time for the previous 24-hour period

- total operating time since the timer was last set to zero-set.

##### **Equalizing operating hours**

Operating hours are also summed in the "Equalization time" field. During cyclical operation, this field is used for equalizing operating hours.

##### **Coupling counter**

The number of relay cutins and cutouts is registered continuously. The number of starts can be read out here:

- Number during the previous 24-hour period

- Total number since the counter was last set to zero-set.

### **Compressor with variable capacity**

##### **Digital scroll compressor**

The capacity is divided into period times as "PWM per". 100% capacity is delivered when cooling takes place for the whole period. An off time is required by the by-pass valve within the period and an on time is also permitted. There is "no cooling" when the valve is on.

The controller itself calculates the capacity needed and will then vary it according to the cut-in time of the by-pass valve. A limit is introduced if low capacity is needed so that the cooling does not go below 10%. This is because the compressor can cool itself. This value can be increased if necessary.

*[Figurtekst: Refrigeration · No refrigeration · Period time · Min. capacity]*

##### **Extra refrigeration capacity (“extra compressor”)**

This function improves the system’s refrigeration capacity by increasing the pressure in the gas cooler.  The function will start when the compressor capacity has been at 100% for 5 minutes. The cooling performance increases to Q0+dh0.

The function also increases the load on the compressor motor as pressure increases. Power consumption increases to Qm+dQm.

##### **BOCK flexxCO2NTROL**

flexxCO2NTROL 4:

The pulse signal can also be used to control one CRII with two unloaders (4-cylinder version).

The compressor capacity can be controlled from 10% to 100%, depending on the pulsation of the unloaders. The compressor start signal is connected to a relay output, and the unloaders are connected to solid state output e.g. DO1 and DO2.

*[Figurtekst: Unloader 1 · Unloader 2]*

##### flexxCO2NTROL 6:

The pulse signal can also be used to control one CRII with three unloaders (6-cylinder version).

The compressor signal is connected to one relay output. The two unloaders are connected to solid state output fx DO1 and DO2. The third is connected to a relay output. The compressor capacity can be controlled from 10 – 67%, depending on the pulse of the unloaders.

The relay is then connected to the third unloader. When this relay is off, the capacity will be controlled between 33% and 100%.

##### **Individual Sd monitoring**

When regulating with Sd monitoring, variable capacity compressor types will increase capacity if the temperature nears the Sd limit. This will result in better cooling of the unloaded compressor.

*[Figurtekst: Unloader 2 follows unloader 1, · but it remains displaced by a · half period.]*

##### **Bitzer CRII**

Followed the same principle (for Bitzer Ecoline CRII 4 and CRII 6) as described above, for BOCK.

##### **Copeland Stream compressor**

The PWM signal can also be used to control one stream compressor with one unloader valve (Stream 4) or one with two unloaders (Stream 6).

Stream 4: The compressor capacity is distributed by up to 50% for

one relay and the remaining 50 – 100% for the unloader.

Stream 6: The compressor capacity is distributed by up to 33%  for one relay and the remaining 33 – 100% for the unloader.

88 | BC186686443705en-000201

### **Load shedding**

On some installations there is the desire to limit the cut-in compressor capacity so that one can limit the total electrical load in the store for periods. (The IT circuit is not directly affected)

This limitation can be activated in the following way:

- Via signal from the network

- Via signal on one DI input + signal via the network

- Via signal on two DI inputs + signal via the network

The signal via the network will result in the same function as if the signal were received on DI 1.

For each digital inlet a limit value is attached for the maximum allowable cut-in compressor capacity so that one can carry out the capacity limitation in 2 steps.

When a digital inlet is activated, the maximum allowable compressor capacity is limited to the set limit. This means that if the actual compressor capacity upon activation of the digital inlet is higher than this limit, then so much compressor capacity is cut-out that it will then be on or under the set maximum limit value for this digital inlet.

The threshold value may not be set lower than the compressor's lowest capacity step/"Start speed".

*[Figurtekst: Comp. cap. % · 100% · 80% · 60% Load limit 1 · 40% Load limit 2 · 20% · Load shed DI 1 · Load shed DI 2]*

When both load-shedding signals are active, the lowest limit value for the capacity will be the one that is applicable.

##### Definition of load shedding:

The function is defined in the MT group. Once defined, it will open up the settings of max. capacity of the MT group and the  max. capacity of the LT group.

##### Overriding of load shedding:

### **Injection ON**

The electronic expansion valves in the refrigeration appliances must be closed when all the compressors are prevented from starting. In this way the evaporators will not be filled with liquid which is subsequently passed on to a compressor when regulation is restarted.

One of the compressor control relays may be used for this function, or the function can be obtained via data communication.

*[Figurtekst: with data communication]*

The function is described based on the sequence of events below: T1) The last compressor is cut-out

- T2) The suction pressure has increased to a value corresponding to Po Ref + ½ NZ + 2 K but no compressor can start due to re-start timers or safety cut-out

- T3) The time delay “Injection OFF delay” elapses and the injection valves are forced to close via relay signal or via network signal.

- T4) The first compressor is now ready to start. The forced closure signal via the network is now cancelled.

- T5) The time delay “Comp. Start delay” expires and the forced closure signal via the relay switch is cancelled simultaneously with the first compressor being allowed to start.

The reason why the forced closure signal via the network is cancelled before the first compressor starts, is that it will take some time to distribute the signal to all appliance controllers via the network.

To avoid load shedding leading to temperature problems for the chilled products, an overriding function is fitted.

A overriding limit is set for the suction pressure as well as a delay time for each digital inlet.

If the suction pressure during load shedding exceeds the set overriding limit and the attached delay times for the two digital inlets expire then load shedding overrides the signals so that the compressor capacity can be increased until the suction pressure is again under the normal reference value. The load shedding can then be activated again.

##### Alarm:

When a load shedding digital inlet is activated, an alarm will be activated to inform that the normal control has been bypassed. This alarm can however be suppressed if so desired.

### **Liquid injection in common suction line**

The discharge pressure gas temperature can be kept down by means of liquid injection into the suction line. (Not IT circuit).

- With a thermostatic expansion valve in series with a solenoid valve.  The solenoid valve is connected to the controller.

*[Figurtekst: Ss Po Sd · NC · Inject diff. Sd · Inject start Sd · Sd · Ss · Inject diff. SH · Inject start SH]*

Control can be carried out in two ways:

1. The liquid injection is exclusively controlled on the basis of the superheat in the suction line. Two values are set – a starting value and a differential where the injection is stopped again.

2. The liquid injection is both controlled by the superheat (as described above) and by discharge temperature Sd. Four values are set – two as mentioned above and two for the Sd function, a starting value and a differential. The liquid injection is started when both starting values have been passed, and is stopped again when just one of the two functions cuts out.

- Direct using an electrically operated expansion valve of the type AKV

Four values are adjusted -- a start value for the Sd temperature, min. and max. values for overheating and a period time for the AKV valve.

The pulse width modulating signal for the AKV valve shall be taken from one of the controller's four solid state outputs.

##### **Time delay**

A time delay can be set which ensures that the injection is delayed during start up.

### **5.1.4 Safety functions**

##### **Signal from the compressor’s safety controls**

The controller can monitor the status of each compressor’s safety circuit. The signal is taken directly from the safety circuit and connected to an input.

(The safety circuit must stop the compressor without involving the controller).

If the safety circuit is cut out the controller will cut out all output relays for the compressor in question and give an alarm. Regulation will continue with the other compressors.

###### General safety circuit

**If a low-pressure switch is placed in the safety circuit it must be placed at the end of the circuit. It must not cut out the DI signals. (There is a risk that the regulation will become locked and that it will not start again). This also applies to the example below. If an alarm is needed which also monitors the low-pressure thermostat, a “general alarm” can be defined (an alarm that does not affect the control). See the following section “General monitoring functions”.**

###### Extended safety circuit

Instead of a general monitoring of the safety circuit this monitoring function can be extended. In this way a detailed alarm message is issued which tells you which part of the safety circuit has dropped out.

The sequence of the safety circuit must be established as shown, but not all of them need necessarily be used.

*[Figurtekst: Oil pressure safety · Over current safety · Motor protect. safety · Discharge  temp. safety · Discharge pressure safety]*

###### Common safety circuit

A common safety signal can also be received from the whole suction group. All compressors will be cut out when the safety signal cuts out. The function may not be connected to an external main switch.

90 | BC186686443705en-000201

Time delays with safety cut-out: In connection with safety monitoring of a compressor it is possible to define two delay times:

Cut-out delay time: Delay time from alarm signal from the safety circuit until the compressor outlet cuts out (note that the delay time is common to all security inlets for the compressor concerned)

Safety re-start time: The minimum time a compressor must be OK after a safety cut-out until it may start again.

##### **Monitoring of min. suction pressure (P0)**

The function promptly cuts out all compressor steps if the suction pressure becomes lower than the permitted value. The cutout limit can be defined in the range from -120 to +30°C. The suction is measured with pressure transmitter P0.

At cutout the alarm function is activated:

The alarm is cancelled and renewed cutin of compressor steps is permitted when the following conditions are met: - the pressure (temperature) is above the cutout limit

- the time delay has elapsed (see later).

##### **Monitoring of superheat**

This function is an alarm function which continuously receives measured data from suction pressure P0 and suction gas Ss. If superheat is registered which is lower or higher than the set limit values, an alarm will be given when the time delay has passed.

##### **Monitoring of max. discharge gas temperature (Sd)**

The function gradually cuts out compressor steps if the discharge temperature becomes higher than permitted. The cutout limit can be defined in the range from 0 to +195°C.

The function is started at a value that is 10 K below the set value. At this point the entire condenser capacity is cut in at the same time as 25% of the compressor capacity is cut out (but minimum one step). This is repeated every 30 seconds. The alarm function is activated.

If the temperature rises to the set limit value all compressor steps are immediately cut out.

The alarm is cancelled and renewed cutin of compressor steps is permitted when the following conditions are met: - the temperature has dropped to 10 K below the limit value

- the time delay prior to restart has been passed. (see later) Normal condenser control is permitted again when the temperature has dropped to 10 K below the limit value.

##### Individual Sd monitoring

The affected compressor will be disconnected here when the temperature exceeds the threshold value.

- The piston compressor will be reconnected when the temperature has dropped 10 K.

- The capacity of compressors with variable capacity is increased if the temperature is approaching the limit.  Once it has been cut out, it will only be connected when the temperature has dropped 10 K.

If signals are also obtained from the embedded NTC sensor, the disconnect value for this temperature will always remain at 130°C and the reconnect value at 120°C.

##### **Monitoring of max. condensing pressure (Pc)**

The function cuts in all condenser steps and cuts out compressor steps one by one if the condensing pressure becomes higher than permitted. The cutout limit is set in bar. The condensing pressure is measured with pressure transmitter Pc_.

The function takes effect at a value which is 3 K below the set value. At this time the entire condenser capacity is cut in at the same time as 33% of the compressor capacity is cut out (but min. one step). This is repeated every 30 seconds. The alarm function is activated.

If the temperature (pressure) rises to the set limit value, the following will happen:

- all compressor steps will immediately be cut out

- the condenser capacity will remain cut in

The alarm will be cancelled and renewed cutin of compressor steps is permitted when the following conditions are met: - the temperature (pressure) falls to 3 K below the limit value

- the time delay for restart has been passed.

##### Delay of Pc max alarms

It is possible to delay the “Pc max alarm" message. The controller will still disconnect the compressors, but the sending of the alarm itself is delayed.

The delay is useful on cascade systems where the max. Pc limit is used to disconnect compressors in the low-pressure circuit if the high-pressure compressors have not started.

##### **Time delay**

There is a joint time delay for “Monitoring of max. discharge gas temperature” and “Min. suction pressure”.

After a cutout, regulation cannot be recommenced until the time delay has been passed.

The time delay starts when the Sd temperature has again dropped to 10 K below the limit value or P0 has risen above the P0 min. value.

##### **Alarm for too high suction pressure**

An alarm limit can be set which will become effective when the suction pressure becomes too high. An alarm will be transmitted when the set time delay has been passed. The regulation continues unchanged.

### **5.2 Condenser / Gas cooler**

##### **Principle**

The condenser in a transcritical CO2 system is also called a gascooler. Unlike in an HFC system, subcooling is not controlled by a condenser, but by the high-pressure valve Vhp.

The gas-cooler control must regulate the temperature in the gascooler’s discharge, so that it has the lowest possible value and the energy consumption of the fans is minimal. However, this should not be so low as to prevent the receiver pressure from being maintained.

Capacity control of the condenser (gas cooler) can be accomplished via step regulation or speed control of the fans.

- EC motors

An analogue output signal is used here, which controls the fans from 0 to maximum capacity.

- Step regulation The controller can control up to 4 condenser steps that are cut in and out sequentially.

- Speed control

The analog output voltage is connected to a speed control. All fans will now be controlled from 0 to max. capacity. If an ON/ OFF signal is required it can be obtained from a relay output. Regulation can be carried out based on one of the following principles:

- all fans operate at the same speed

- Only the necessary number of fans is cut in.

- Combination with one fan speed regulated and the rest step regulated.

### **5.2.1 C apacity control of condenser**

The cut-in condenser capacity is controlled by the condenser pressure’s actual value and depends on whether the pressure is rising or falling. Regulation is performed by a PI controller. The controller cuts in capacity in such a way that the deviation between the actual condensing pressure and the reference value becomes as small as possible.

##### **Regulating sensor selection**

The capacity distributor regulates from the temperature sensor Sgc, located at the outlet for the gas cooler.

Cap. Ctrl sensor = Sgc

Pc is used as the safety function for high condenser pressure and will therefore ensure cut-out of the compressor capacity when condenser pressure is too high.

### **5.2.2 Reference for condensing pressure**

The reference for the regulation can be defined in two ways. Either as a fixed reference or as a reference that varies according to the outdoor temperature.

##### **Fixed reference**

The reference for the condensing pressure is set in °C.

##### **Floating reference (recommended)**

This function allows the condensing pressure’s reference value to vary according to the outdoor temperature within a defined area.

The reference is based on:

- the outdoor temperature measured with Sc3 sensor

- The minimum temperature difference between the air temperature and the condensing temperature at 0% compressor capacity.

- the condenser’s dimensioned temperature difference between the air temperature and the condensing temperature at 100% compressor capacity (Dim tmK)

- how large a part of the compressor capacity has been cut in.

*[Figurtekst: Sc3 + Dim tm K Pc Ref. ⁰C · Pc Ref at · 50% Comp. · capacity · Sc3 + Min tm K · Sc3 · 0% 50% 100% Comp. · cap. %]*

The minimum temperature difference (min tm) at low load should be set at approximately 2 K as this will eliminate the risk that all fans will be running when no compressors are running. Set the dimensioned difference (dim tm) at max. load (e.g. 3 K).

The controller will now contribute with a value to the reference which depends on how large a part of the compressor capacity has been cut in.

##### **Heat recovery**

The condensing pressure may be increased during heat recovery. This is mentioned in the “Heat recovery” section.

##### **Limitation of the reference**

To safeguard yourself against a too high or too low regulation reference, a limitation of the reference must be set.

*[Figurtekst: PcRef · Max · Min]*

(The maximum value can be overridden by the heat recovery function).

##### Handling sensor errors:

In the event of Sgc failure the controller switches over to an "emergency cooler sequence" that attempts to maintain regulation.

92 | BC186686443705en-000201

##### **Forced operation of condenser capacity**

Forced operation of the capacity can be arranged where the normal regulation is ignored.

The safety functions are cancelled during forced operation.

##### **Info**

In normal operating conditions, the temperature at Sd will be between 60 and 70°C - depending on whether it is winter or summer.

If the "Heat reclaim" function is to raise the condensing pressure, the temperature may increase to 90° or higher.

Forced operation via setting

The regulation is set to Manual. The capacity is set in percent of the regulated capacity.

The Sc3 sensor should be positioned so that it measures the air intake temperature for the gas cooler. If it measures a temperature that is too high, the system's COP will become impaired.

Forced operation of relays

If the forced operation is carried out with the switches at the front of an extension module, the safety function will register any exceeding of values and transmit alarms, if required, but the controller cannot cut the relays in or out in this situation.

The Sgc signal must be stable. If this cannot be done using a system sensor, it may be necessary to use an immersion tube sensor.

If the power supply to AK-PC 772A or the high pressure valve Vhp fails, the system cannot be controlled. We recommend installing an emergency supply (UPS) for both the controller and the valve to avoid faults. A relay in the UPS should be incorporated into the controllers safety circuit so that it can restart safely.

### **5.2.3 Heat recovery**

The heat recovery function can be used on the installation when you want to make use of warm gas for heating purposes. When the function is activated the reference for the condenser temperature will be raised to a set value. If the controller must also activate a pump and/or a valve, a relay must be selected for the function.

The regulation of the heat recovery circuits is done with regard to the cooling system. In the event of conflict, the safety situation is that the cooling system has higher priority than the recovery circuits.

There must be a cooling requirement in order to supply for heat recovery.

2. Use of a thermostat for the function. This function can be used with advantage where the heat recovery is used to warm up a water tank. A temperature sensor is used to activate/deactivate the heat recovery function. When the temperature sensor becomes lower than the set cut in limit, the heat recovery function is activated and the reference for the condenser temperature will be raised to a set value and simultaneously the chosen relay outlet is used to activate the valve which leads the warm gas through the heat exchanger in the water tank. When the temperature in the tank has reached the set value, the heat recovery is cut-out again.

In both cases it applies that when the heat recovery function is de-activated, the reference for the condensing temperature will then decline slowly.

##### **The function can be activated in two ways:**

1.  A digital input signal is received

- In this instance, the heat recovery function is activated via an external signal from, for example a building management system. When the function is activated the reference for the condenser temperature will be raised to a set value and the attached relay outlet is used to activate valve and pump.

94 | BC186686443705en-000201

##### **Overview of control options**

|Control option|HR offset|Regulation using|Input signals|Settings|Output|
|---|---|---|---|---|---|
||No|-|Temperature sensor|Temperature cut in / cut out<br>Pgc HR min, fan HR min||
|Thermostat|Yes|Temperature control|2 temperature sensors|Temperature cut in / cut out<br>Pgc HR min, fan HR min<br>HR reference temperature<br>Pgc HR offset, fan HR offset||
|||Consumer signal|Temperature sensor<br>0 - 10 V|Temperature cut in / cut out<br>Pgc HR min, fan HR min<br>Pgc HR offset, fan HR offset|A relay can be<br>selected|
||No|-|On / Off|Pgc HR min, fan HR min||
|Digital input|Yes|Temperature control|On / Off<br>Temperature sensor|Pgc HR min, fan HR min<br>HR reference temperature<br>Pgc HR offset, fan HR offset||
|||Consumer signal|On / Off<br>0 - 10 V|Pgc HR min, fan HR min<br>Pgc HR offset, fan HR offset||

##### **Increasing pressure reference with heat recovery**

Heat recovery is initiated with an On signal when the thermostat calls for heat or a DI signal is received.

##### Without HR offset

The pressure reference is increased to the “Pgc HR min” setting The gas cooler reference is increased to the “Fan HR min” setting.

##### With HR offset

1. The pressure reference is increased to the “Pgc HR min” setting The gas cooler reference is increased to the “Fan HR min” setting.

2. Afterwards it is adjusted with either a signal for the PI regulation or with a voltage signal from an external source. This signal will be between 0 and 100%.

##### **Info**

##### Remember the isolation amplifier

If signals are received from other controls, e.g. heat recovery for one of the inputs, a galvanically insulated module should be inserted.

The relay can engage both the gas valve and the circulation pump.

When the relay pulls in and releases, the three-way valve will be switched around.

It can take up to 2 minutes for the valve to change position. Installing a time delay to cut out the circulation pump is recommended.

- a. At between 0 and 50%, the pressure reference will be a variable between “Pgc HR Min” and “Pgc HR offset”.

- b. At over 50%, the pressure reference will be “Pgc HR offset”.

- c. At between 50 and 100%, the fans will be controlled so that the temperature in the gas cooler is increased.

*[Figurtekst: Consumer · reference · Consumer · reference · Overview]*

### **5.2.4 Capacity distribution**

### **EC motor**

The voltage signal to the EC motor is defined by the following settings:

EC min (typically 20% corresponding to 2 V at 0 – 10 volt signal) EC max (typically 80% corresponding to 8 V at 0 – 10 volt signal) EC absolute max (typically 100% corresponding to 10 V)

If the Sgc temperature exceeds the defined “Absolute Max Sgc temperature”, the output voltage will be increased to the EC absolute maximum value.

### **Step regulation**

Cut-ins and cutouts are carried out sequentially. The last cut-in unit will be cut out first.

The controller starts the frequency converter when the capacity requirement corresponds to the set starting speed. The controller stops the frequency converter when the capacity requirement becomes lower than the set minimum speed.

##### **Speed regulation + step regulation**

The controller starts the frequency converter and the first fan when the capacity requirement corresponds to the set starting speed.

The controller cuts in several fans step by step as the capacity requirement grows and then adapts the speed to the new situation.

The controller cuts out fans when the capacity requirement becomes lower than the set minimum speed.

### **Speed regulation**

When an analog output is used the fans can be speed regulated, e.g. with a frequency converter type VLT or a EC motor.

In the configuration of the controller’s outputs it will be the output “FanA1”” that will start and stop the frequency converter.

##### **Joint speed regulation**

The analog output voltage is connected to the speed regulation. All fans will now be regulated from 0 to max. capacity. If an ON/ OFF signal is required for the frequency converter, so that the fans can be stopped completely, a relay output can be defined.

96 | BC186686443705en-000201

##### **Speed regulation of first fan + step regulation of the rest**

The controller starts the frequency converter and increases the speed of the first fan.

If additional capacity is required, the next fan cuts in at the same time as the first fan switches to minimum speed. From here, the first fan can increase speed again, etc.

##### **Capacity limitation during night operation**

The function is used to reduce the noise from the fans to a minimum. It is primarily used in conjunction with a speed control, but it will also be active when steps are cut in and out. The setting is arranged as a percentage of the max. capacity.

The limitation will be disregarded when safety functions Sd max. and Pc max. take effect.

### **Condenser couplings**

##### **Coupling of condenser steps**

There are no time delays in connection with cutin and cutout of condenser steps beyond the time delay inherent in the PIregulation.

##### **Timer**

The operating time of a fan motor is registered continuously. You can read out:

- operating time for the previous 24-hour period

- total operating time since the timer was last set to zero-set.

##### **Coupling counter**

The number of couplings is registered continuously. Here the number of starts can be read out:

- number during the previous 24-hour period

- total number since the counter was last set to zero-set.

##### **Exercising fans**

The last fans are unlikely to be activated during winter months. To ensure that the fans are 'exercised' a test will be carried out every 24 hours to check whether all relays have been in operation. The relays that have not been used will now be activated for 5 minutes (from 13:00) but with a pause of one hour between individual relays. A speed control is run at "Start speed".

### **Safety functions for condenser**

##### **Signal from fan and frequency converter’s safety controls**

The controller can receive signals on the status of each individual condenser step’s safety circuit.

The signal is obtained directly from the safety circuit and connected to a “DI” input.

If the safety circuit is cut out the controller will give alarm. Regulation continues with the remaining steps.

The ancillary relay outlet is not cut-out. The reason for this is that the fan are often connected in pairs but with one safety circuit. With fault on the one fan, the other will continue to operate.

### **5.2.5 Circuits for control of CO2 gas pressure**

##### **Application**

##### **Overview**

The controller regulates the pressure in the gas cooler (condenser) so that the system achieves the optimal COP. The controller will always optimise to a subcritical state.

*[Figurtekst: Important · This sensor must be placed · immediately at the gas · cooler outlet.]*

The pressure in the gas cooler is controlled by the valve CCMT valve with stepper motor can be used. Regulation must have inputs from both a pressure transmitter Pgc and a temperature sensor Sgc. Both must be fitted in the outlet immediately after the gas cooler. The valve is an CCMT valve, which has been specially developed for the pressure conditions that exist in a transcritical CO2 system. The valve's degree of opening can be restricted both at the closing point and in the entire open point.

##### Reference curve

The settings OD Min. and OD max. are adjusted as % of the degree of opening.

##### Maximum COP control

During normal operation without override, the controller will maintain the optimum pressure in the transcritical area.

Remember that the controller controls the gas pressure. If the regulation is stopped by the internal or external main switch, this control will stop as well. Risk of loss of charge.

If the compressors are stopped via the function "External compressor stop", control of the gas pressure will continue.

The controller is pre-programmed to follow the optimal COP from the pressure/enthalpy chart. The top point is defined at 100 bar, 39 °C. (Optimal theoretical COP is achieved at the curve that passes through 100 bar and 39 °C. The point of intersection can be changed by setting a value other than the default). Regulation will now follow the set reference curve, but will never go above the set permitted max. pressure for the gas cooler. The current reference can be read from the controller's overview screen.

##### Subcooling

It is also possible to configure the subcooling in the sub-critical area..

98 | BC186686443705en-000201

### **Receiver control**

The receiver pressure can be controlled so that it is kept at the requested reference point. This control requires the installation of a receiver valve Vrec (fx type CCM) and a pressure transmitter. It is possible to regulate using two parallel valves.

##### **Regulation method**

Pressure regulation can be carried out with one of the following definitions:

- Fixed setpoint

- Displacement of the setpoint with an external signal

- Optimisation, where the IT circuit maintains pressure at the most energy-efficient level

- Delta P, where the reference is a pressure difference between the receiver and Po on the MT circuit

##### **P-band**

There are two safety functions for the receiver. They are only available for gas-cooled regulation. A P-belt must be installed to be able to regulate the function, but both are standard set to zero, which makes the function inactive.

##### **Receiver pressure's max. limit**

Set a max. receiver pressure that will typically be the maximum receiver pressure. If the controller records that the receiver pressure slips into the P-band, shutdown of the high-pressure valve Vhp commences. The opening degree will be linear through the p-band so that the Vhp will be totally closed by pressing 'set max. receiver pressure' (A complete shutdown assumes that the configuration for the high-pressure valve - “Min. OD% is set to 0%)

##### **Receiver pressure's min. limit:**

A minimum receiver pressure limit can be set. If the controller register receiver pressure below the set value, the Vhp valve will be opened. The opening degree will be linear through the p-band, and the maximum permitted opening degree of the Vhp will be present by pressing 'set min. receiver pressure' minus 'set-p-band'. If the setting of the valve's opening degree is limited and it cannot be fully opened,  the set opening degree value will be at the pressure 'set min. receiver pressure' minus 'set p-band'. When the suction pressure for MT is increased (e.g. by Po optimisation), it will be necessary to maintain a certain differential pressure so that the refrigeration units can continue to be regulated.  The setting “delta P MT” will ensure the necessary receiver pressure.

Regulation limitations of the receiver pressure

##### **Note**

The PI regulation of the receiver pressure must have space to regulate without restrictions.

This means that there should be sufficient space for the PI regulation to move around the reference, i.e. at least 2-3 bars – both over and below the reference.

The value is very dependent on the tuning of the PI regulation and the system dynamics.

An example may be a 40-bar plant in which the receiver's reference pressure is set to 35 bars. Here the system can interfere with normal regulation because the high pressure limit is very stringent.

##### **Hot gas dump**

The controller has a function that can turn on the hot gas to the receiver if the pressure becomes lower than the set value. The hot gas will shut off again when the pressure exceeds the difference.

##### **Stop of compressors**

If the MT compressors are stopped via the function "External compressor stop",  the reference for the receiver control will be to the setting "Max. receiver pressure"  minus the P-band. If IT compressors are in operation, the IT compressors will continue and the reference for the receiver control will be set to Max. minus the P-band

### **Parallel compression**

##### **Principle**

On transcritical systems installed in slightly warmer surroundings the COP will be significantly improved by using parallel compression.

One compressor is used to help maintain the receiver pressure during warm periods when the outdoor temperature becomes high — primarily during the summer months. The parallel compression (intermediate temperature, ‘IT’) is controlled by the IT suction group. It receives signals from two pressure transmitters and it will start the compressor as needed, so that the receiver pressure is kept at the desired level. The compressor capacity will be variable, and the controller will emit a 0 – 10 V signal that indicates the desired capacity.

The function is activated by the IT control, which regularly records the opening degree of the Vrec valve. When the opening degree is greater than the set value, the IT compressor will start up. But it only starts up if the temperature at Sgc is higher than the set value in IT setting "IT Comp. Sgc min."

The controller will now speed-regulate the IT compressor so that the pressure in the receiver is kept at the desired level.

The parameter “IT comp delay” defines the time that the valve will continue to regulate before the compressor takes over. The parameter “IT end delay” defines the time that the IT compressor must be stopped before regulation is transferred to the valve. A high value will increase the operating hours of the IT compressor.

When the IT compressor starts, the Vrec valve will be closed by increasing the reference for the receiver pressure to max. minus the P-band.

When the capacity requirement of IT decreases and the pressure in the receiver reaches Prec.Min, the compressor will stop and the pressure control will be assumed by the Vrec valve.

100 | BC186686443705en-000201

### **5.3 General monitoring functions**

**General alarm inputs** (10 units)

An input can be used for monitoring an external signal.

The individual signal can be adapted to the relevant use as it is possible to give the alarm function a name and to indicate your own alarm text.

A time delay can be set for the alarm.

##### **General thermostat function** (1 unit)

The function may freely be used for alarm monitoring of the plant temperatures or for ON/OFF thermostat control. An example could be thermostat control of the fan in the compressor compartment.

*[Figurtekst: Saux max . · min .]*

The thermostat can either use one of the sensors used by the regulation (Ss, Sd, Sc3) or an independent sensor (Saux1). Cutin and cutout limits are set for the thermostat. Coupling of the thermostat’s output will be based on the actual sensor temperature. Alarm limits can be set for low and high temperature, respectively, including separate alarm delays. The individual thermostat function can be adapted to the relevant application as it is possible to give the thermostat a name and to indicate alarm texts.

**General voltage input with ancillary relay** (1 unit)

A voltage input are accessible for monitoring a measurement of the installation. Examples are monitoring of a leak detector, moisture measurement and level signal - all with ancillary alarm functions. The voltage input can be used to monitor a standard voltage signal (0 – 5 V, 1 – 5 V, 2 – 10 V or 0 – 10 V). If required, one can also use 0 – 20 mA or 4 – 20 mA if external resistance is placed at the inlet to adjust the signal to the voltage. A relay outlet can be attached to the monitoring so that one can control external units.

##### Following can be set/read out:

##### - Freely definable name

- Selection of signal type (0 – 5 V, 1 – 5 V, 2 – 10 V, or 0 – 10 V).

- Scaling of read-out so it corresponds to measuring unit

- High and low alarm limit including delay times

- Freely definable alarm text

- Attach a relay output with cut in and cut-out limits including

- delay times

*[Figurtekst: Saux max . · min .]*

##### **General PI function** (1 units)

The function can be freely used for controlling a required function, or it can be used to send signals to the controller regarding operating states. An example could be an out/in control for the use of the heat recovery function.

*[Figurtekst: 0 – 10 V · S U · P]*

##### **General pressure control function** (1 unit)

The function may freely be used for alarm monitoring of plant pressure or for ON/OFF pressure control regulation.

*[Figurtekst: max. · min. · Paux]*

The pressure control can either use one of the sensors used by the control function (Po, Pc) or an independent sensor (Paux1). Cutin and cutout limits are set for the pressure control. Coupling of the pressure control’s output will be based on the actual pressure. Alarm limits can be set for low and high pressure, respectively, including separate alarm delays.

Signals can be received from the following fx.:

- Temperature sensor

- Pressure transmitter

- Saturation temperature

- Voltage signal

- Internal signals such as: Tc, Pc, Ss and Sd Signals are shown on the next page.

Signals can be sent to the following: Voltage signal Valve with stepper motor PWM (pulse width modulated) signal for AKV valve.

The PI function is shown overleaf.

The individual pressure control function can be adapted to the relevant application as it is possible to give the pressure control a name and indicate alarm texts.

##### General

Signal and setting values are converted and adjusted as a percentage value of the signal.

A slow process will normally not be critical for the setting of P-part and I-part.

Settings

###### Prepared examples

However, if the process is quick, more careful setup is required.

A general balancing might be:

- Check max. and min. settings

- Increase the integration time so that it is not mixed up with the balancing

- Reduce Kp to start with

- Start the process

- Adjust Kp until the process starts fluctuating and is constantly fluctuating

- Adjust Kp to half the value

- Adjust Tn down until the process starts fluctuating again

- Adjust Tn to double values

102 | BC186686443705en-000201

### **5.4 Miscellaneous**

If the power supply to AK-PC 772A or the stepper motor valves fails, the system cannot be controlled. It is recommended to install an emergency supply (UPS) for at least the valve drivers, to ensure proper closing of the valve. An alarm can only be sent when the base module is also connected to a UPS. For remote monitoring, a relay output in the UPS must be connected to a dedicated DI in the controller. This is a pure monitoring function, without any further control functionality.

##### **Sensor calibration:**

The input signal from all connected sensors can be corrected. A correction will only be necessary if the sensor cable is long and has a small cross-sectional area. All displays and functions will reflect the corrected value.

##### **Clock function**

The controller contains a clock function.

The clock function is used only to change between day/night. The year, month, date, hour and minutes must be set.

##### **Main switch**

The main switch is used to stop and start the controlling function.

The switch-over has 2 positions:

- Normal controlling state (Setting = ON)

- Control stopped. (Setting = OFF)

In the event of a power failure, the time setting will be remembered for at least 12 hours.

If the controller is connected to an installation with an AKAgateway or an AK system manager, this will automatically reset the clock function.

In addition, one can also choose to use a digital input as an external main switch.

If the switch-over or the external main switch is set at OF F, all the control ’ s functions are inactive a nd an alarm is generated to draw attention to this – all other alarms cease.

##### **Alarms and messages**

In connection with the controller’s functions, there are a number of alarms and messages that become visible in cases of fault or erroneous operation.

##### **External switch for stopping compressors**

The switch will stop the compressors, but all other functions will continue to be regulated.

##### **Refrigerant**

For CO2 only

##### **Sensor failure**

- If lack of signal from one of the connected temperature sensors or pressure transmitters is registered an alarm will be given.

- When there is a P0 error regulation will continue with 50% cut-in capacity during day operation and 25% cut-in capacity during night operation – but minimum one step.

- When there is a Pc error 100% condenser capacity will be cut in, but the compressor regulation will remain normal.

- When there is an error on the Sd sensor the safety monitoring of the discharge gas temperature will be discontinued.

- When there is an error on the Ss sensor the monitoring of the superheat on the suction line will be discontinued.

- When there is an error on the outdoor temperature sensor Sc3 the Pc value is used as reference.

Note: An incorrect sensor must be in order for 10 minutes before the sensor alarm deactivates.

##### Safety disconnection signal

Unexpected disconnection of the compressor, condensation fan or frequency convertor can result in unexpected temperature increases in the system. If necessary, use the necessary safety signals to ensure that the controller receives signals about disconnections.

##### **Alarm history:**

The controller contains an alarm history (log) that contains all active alarms as well as the last 40 historical alarms. In the alarm history you can see when the alarm began and when it stopped. In addition, one can see the priority of each alarm as well as when the alarm has been acknowledged and by which user.

##### **Alarm priority:**

Differentiation is made between important and not-so-important information. The importance – or priority – is set for some alarms whilst others can be changed voluntarily (this change can only be done with attachment of AK-ST service tool software to the system and settings must be made in each individual controller).

The setting decides which sorting / action must be carried out when an alarm is sounded.

- “High” is the most important

- “Log only” is the lowest

- “Interrupted” results in no action

##### **Alarm relay**

One can also choose whether one requires an alarm output on the controller as a local alarm indication. For this alarm relay it is possible to define on which alarm priority it must react to – one can choose between the following:

- “Non” – no alarm relay is used

- “High’ – Alarm relay is activated only with alarms with high priority

- “Low - High’ – Alarm relay is activated only with alarms with “low” priority, “medium” or “high” priority.

The relationship between alarm priority and action appears in the schedule below.

|Setting|Log||Alarm rela|y|Send|AKM des-|
|---|---|---|---|---|---|---|
|||Non|High|Low-High|Network|tination|
|High|X||X|X|X|1|
|Medium|X|||X|X|2|
|Low|X|||X|X|3|
|Log only|X|||||4|
|Inter-<br>rupted|||||||

##### Alarm acknowledgement

If the controller is connected to a network with an AKA gateway or an AK system manager as alarm receiver, these will automatically acknowledge the alarms that are sent to them.

If the controller on the other hand is not included in a network, the user must acknowledge all alarms.

##### Alarm LED

The alarm LED on the front of the controller indicates the controller’s alarm status.

Blinking: There is an active alarm or an unacknowledged alarm. Fixed light: There is an active alarm that has been acknowledged. Switched off: There are no active alarms and no unacknowledged alarms.

##### **Forced operation via network**

The controller contains settings that can be operated from the gateway’s forced operation function via data communication.

When the forced operation function asks about one change, all the connected controllers on this network will be set simultaneously.

There are the following options:

- Change to night operation

- Forced closure of injection valves (Injection ON)

- Optimization of suction pressure (Po)

##### **Operating AKM / Service tool**

The setup of the controller itself can only be carried out via AK-ST 500 service tool software. The operation is described in fitters on site guide.

If the controller is included in a network with an AKA gateway one can subsequently carry out the daily operation of the controller via AKM system software, i.e. one can see and change daily readouts/settings.

Note: AKM system software does not provide access to all configuration settings of the controller. The settings/read-outs that may be made appear in the AKM menu operation (see also Literature overview).

##### **Authorisation / Passwords**

##### **I'm alive relay**

The function reserves a relay that is pulled under normal regulation.

The relay will be released if:

- The regulation is stopped by the internal or external main switch

- The controller fails

##### **IO Status and manual**

The function is used in connection with installation, servicing and fault-finding on the equipment. With the help of the function, the connected outputs are controlled.

##### Measurements

The status of all inlets and outlets can be read and controlled here.

##### Forced operation

One can carry out an override of all outlets here to control whether these are correctly attached.

Note: There is no monitoring when the outlets are overridden.

##### **Logging/registration of parameters**

As a tool for documentation and fault-finding, the controller provides the possibility of logging of parameter data in the internal memory. Via AK-ST 500 service tool software one can:

a) Select up to 10 parameter values the controller will

continuously register

b) State how often they must be registered

The controller can be operated with System software type AKM and service tool software AK-ST 500.

Both methods of operation provide the possibility for access to several levels according to the user’s insight into the various functions.

System software type AKM:

The various users are defined here with initials and key word. Access is then opened to exactly the functions that the user may operate.

The operation is described in the AKM manual.

Service tool software AK-ST 500:

The operation is described in fitters on site guide.

When a user is created, the following must be stated: a) State a user name b) State a password c) Select user level

d) Select units – either US (e.g. °F and PSI) or Danfoss SI (°C and Bar)

e) Select language

Access is given to four user levels.

- 1) DFLT – Default user – Access without use of password See daily settings and read-outs.

2) Daily – Daily user

Set selected functions and carry out acknowledgement of alarms.

3) SERV – Service user

The controller has a limited memory but as a rule of thumb, the 10 parameters can be saved, which are registered every 10 minutes for 2 days.

Via AK-ST 500 one can subsequently read the historical values in the form of graph presentations. (The log only works when the clock has been set.)

All settings in the menu system except for creation of new users 4) SUPV – Supervisor user All settings including the creation of new users.

104 | BC186686443705en-000201

##### **Display of suction pressure and condensing pressure**

One to four separate displays can be connected to the controller. Connection is accomplished by means of wires with plug connections. The display may be placed in a control box front, for example.

When a display is connected, it will show the value for what is indicated in the setup. It can be: Suction control Temperature T0-MT P0-MT pressure T0-LT P0-LT pressure Ss-MT Sd-MT Ss-LT Sd-LT Cond. control sensor Tc-MT Pc-MT pressure Sgc Pgc Prec MT Speed compressor LT Speed compressor

When (on plug A) a display with control buttons is chosen, a simple operation via a menu system can be performed in addition to the display of suction pressure and condensing pressure:

|**No.**|**Function**|
|---|---|
|o57|Capacity settings for condenser<br>0: MAN,1: OFF,2: AUTO|
|058|Manual settingof condenser capacity|
|o59|MT Capacity setting for suction group<br>0: MAN,1: OFF,2: AUTO|
|o60|MT Manual settingof suction capacity|
|o93|Lock of configuration<br>It is only possible to select a predefined configuration or change refrigerant when the<br>configuration lock is open.<br>0 = Configuration open<br>1 = Configuration locked|
|P62|LT Manual settingof suction capacity|
|P63|LT Capacity setting for suction group<br>0: MAN,1: OFF,2: AUTO|
|r23|MT Set point suction pressure<br>Settingof required suctionpressure reference in °C|
|r24|MT Suction pressure reference<br>Actual reference temperature for compressor capacity|
|r12|Main switch<br>0: Controller stopped<br>1: Regulating|
|r28|Set point condenser<br>Settingof required condenserpressure in  °C|
|r29|Condenser reference<br>Actual  reference for temperature for condenser capacity|
|r57|MT To evaporating pressure in °C|
|r90|LT To evaporating pressure in °C|
|r91|LT Suctionpressure reference|
|r92|LT Setpoint suctionpressure|
|u21|MT Superheat in suction line|
|u44|Sc3 out door temperature in °C|

*[Figurtekst: u48 Actual regulation  status on condenser · 0: Power up · 1: Stopped · 2: Manuel · 3: Alarm · 4: Restart · 5: Standby · 6: Unloaded · 7-9: Part loaded · 10: Full loaded · 11: Runnin g · u49 Cut in condenser ca p acit y  in % · u50 Reference for condenser ca p acit y  in % · u51 MT Actual regulation status on suction group · Actual regulation status on suction group MT circuit · 0: Standby · 1: Normal control · 2: Compressor alarm · 3: ON timer active · 4: OFF timer active · 5: Normal control · 6: Injection ON delay · 7: Coordination · 8: Compressor 1 delay active · 9: Pump down · 10: Sensor error · 11: Load shed is active · 12: High Sd · 13: High Pc · 14: Manual control · 15: OFF · u52 MT Cut in com p ressor ca p acit y  in % · u53 MT Reference for com p ressor ca p acit y · u54 MT Sd dischar g e  g as tem p erature in °C · u55 MT Ss Suction  g as tem p erature in °C · U01 MT Actual Pc condensin g p ressure in °C · U46 LT Reference for com p ressor ca p acit y · U47 LT Cut in com p ressor ca p acit y  in % · U48 LT Actual re g ulation status on suction  g rou p ( see value in u51 ) · U49 LT Actual Pc condensin g p ressure in °C · U50 LT Ss Suction  g as tem p erature in °C · U51 LT Sd dischar g e  g as tem p erature in °C · U52 LT Su p erheat in suction line · AL1 Alarm suction  p ressure · AL2 Alarm condenser · - - 1 Initiation ,  Dis p la y  is connected to out p ut  "A" , ( - - 2 = out p ut "B" etc. )]*

If you want to see one of the values for what is given under "function" you should use the buttons in the following way:

1. Press on the upper button until a parameter is shown

- 2.Press on the upper or lower button and find the parameter you want to read

3. Press on the middle button until the value of the parameter is displayed.

- After a short time, the display will return automatically to the "Read out display".

##### **Light-emitting diodes on the controller**

*[Figurtekst: Internal communication · between the modules: · Quick flash = error · Constantly On = error · Status of output 1-8 · Slow flash = OK · Quick flash = answer from gateway · n Power remains on for 10 mins after network · n Comm registration · n DO1  n Status Constantly ON = error · n DO2  n Service Tool Constantly OFF = error · n DO3  n LON External communication · n DO4  n I/O extension Communication to AK-CM 102 · n DO5  n Alarm · n DO6  n Flash = active alarm/not cancelled · n DO7  n Display Constant ON = Active alarm/cancelled · n DO8  n Service Pin · Network installation]*

##### **Graphic display MMIGRS2**

With the display is access to most of the controller functions. For access, connect the display to the controller and activate the address on MMIGRS2. (A separate power supply does **not** need to be connected) Power is supplied directly from the controller via the cable.

Setting:

- 1.Press both the "x" and "enter" buttons and hold in for 5 seconds. The BIOS menu is then displayed.

2. Select the "MCX selection" line and press "enter"

3. Select the "Man selection" line and press "enter"

4. The address will be displayed. Check that it is 001, press "enter". Data will then be collected from the controller.

##### **Stepper Motor Valves**

When selecting a Danfoss stepper motor valve, all settings are factory set. Here, it is only necessary to select the type of valve. If a valve from other manufacturers is used the following settings has to be made. Get data from the valve manufacturer:

##### Max Operating Steps.

The number of steps that correspond to a valve position of 100%. This value is limited to a range of 0 – 10,000 steps.

##### Hysteresis

The number of steps needed to correct for mechanical hysteresis when a reduction gear is part of the valve design. This adjustment is only applied, if an additional opening of the valve is requested.

If this is the case the valve opens an additional amount equal to this value, before driving the valve in the closing direction by this same value. This value is limited to 0 – 127 steps.

##### Step Rate

The desired valve drive rate in steps per second. This value is limited to 20 – 500 steps / sec.

##### Overdrive at Valve Init

During valve initialization, the amount to overdrive the valve, beyond the 0% position, to ensure that the valve has fully closed. This value is limited to a range of 0 – 31%.

##### Phase Current

The phase current applied to each phase of the stepper motor during the actual valve movement can be set in the range 0 – 325 mA.

The value of the phase current is set in RMS – be aware that some valve manufacturers are using peak currents in the data sheet (multiply the peak current by 0.71 to convert to the RMS value). (Note: the actual phase current can be higher due to stepper driver resolution)

##### Soft Landing after Valve Init

At power on the valve is performing a valve Initialization i.e. closing the valve  with “Max Operating Steps” plus “Overdrive At Valve Init “steps to generate a zero point calibration of the system . Hereafter a “Soft landing after Valve Init” is made to  minimize the closing force on the valve seat with a few opening steps according to setting of  “Hysteresis” or  min 20 steps

##### Holding Current

The percent of the programmed Max Phase Current that should be applied to each phase of the stepper output when the valve is stationary.  If required, this current ensures that the valve maintains its last programmed position.  This value is limited to a range of 0 – 70% given in 10% steps.

##### Failsafe Position

During failsafe mode of operation (e.g., resulting from a loss of communications to this module), specifies the default valve position.  This value is limited to a range of 0 – 100%.

106 | BC186686443705en-000201

### **5.5 Appendix - Alarm texts**

|**Settings**|**Priority**<br>**(factory)**|**English alarm texts**|**Description**|
|---|---|---|---|
|**Suction group**||||
|Low suction pressure P0|Low|Low pressure P0|Minimum safety limit for suction pressure P0 has been exceeded|
|High suction pressure P0|High|High pressure P0|High alarm limit for P0 has been exceeded|
|||High superheat suction A|Superheat in suction line too high|
|High/Low superheat Ss|Medium|Low superheat section A|Superheat in suction line too low|
|Load shedding|Medium|Load Shed active|Load shedding has been activated|
|||P0 sensor error|Pressure transmitter signal from  P0 is defective|
|||Sgc sensor error|Temperature signal from gas cooler is defective|
|P0 sensor error|High|Prec sensor error|Pressure transmitter signal from the receiver is defective|
|||Pgc sensor error|Pressure transmitter signal from  the gas cooler is defective|
|||Ss sensor error|Temperature signal from Ss suction gas temp. is defective|
|||Sd sensor error|Temperature signal from Sd discharge gas temp. is defective|
|||Sc3 sensor error|Temperature signal from Sc3 air on condenser defective|
|Misc. sensor error|Medium|Heat recovery sensor error|Temperature signal from Shrec heat recovery thermostat defective|
|||Shr sensor error|Temperature signal from heat circuit is defective|
|||Saux_ sensor error|Signal from extra Temp.sensor Saux_ is defective|
|||Paux_ sensor error|Signal from extra pressure sensor Paux_ is defective|
|All compressors||||
|Common safety|High|Common compr. Safety<br>cutout|All compressors have been cut out on common safety input|
|||Comp. X oil pressure cut out|Compressor no. x has been cut out on oil pressure safety|
|||Comp. x over current cut out|Compressor no. x has been cut out on over current safety|
|Comp. 1 safety||Comp. 1 motor prot. cut out|Compressor no. x has been cut out on motor protection safety|
|Comp. 2 safety<br>Comp. 3 safety|Medium|Comp. 1 disch. Temp cut out|Compressor no. x has been cut out on discharge temperature safety|
|||Comp. 1 disch. Press. Cut out|Compressor no. x has been cut out on discharge pressure safety|
|||Comp. 1 General safety cut<br>out|Compressor no. x has been cut out on general safety|
|VSD safety|Medium|Comp. 1 FCD safety error|Variable speed drive for comp. x has been cut out on safety|
|Rec. high pressure|Medium|Recv. High pressure alarm|Pressure too high in receiver|
|Rec. low pressure|Medium|Recv. Low pressure alarm|Pressure too low in receiver|
|**Condensor**||||
|High Sd temp.|High|High disch. temp. Sd|Safety limit for discharge temperature has been exceeded|
|High  Pc pressure|High|High pressure Pc|High safety limit for condensing pressure Pc has been exceeded|
|Pc Sensor error|High|Pc sensor error|Pressure transmitter signal from Pc is defective|
|||Fan Alarm 1|Fan  no. X is reported defective via safety input|
|Fan/VSD safety|Medium|Fan VSD alarm|Variable speed drive for condenser fans has been cut out on safety|

|**Various alarms**|||||
|---|---|---|---|---|
|Standby mode|Medium||Control stopped,<br>MainSwitch=OFF|The control has been stopped via the setting ”Main switch” = Off or<br>the external Main switch is off|
|Thermostat x – Low<br>temp. alarm|Low||Thermostat x - Low alarm|The temperature for thermostat no. x has been below the low alarm<br>limit for longer time than set delay|
|Thermostat x – High<br>temp. alarm|Low||Thermostat x - High alarm|The temperature for thermostat no. x has been above the high alarm<br>limit for longer time than set delay|
|Pressostat x – Low pres-<br>sure alarm|Low||Pressostat x - Low alarm|The pressure for pressostat no. x has been below the low alarm limit<br>for longer time than set delay|
|Pressostat x – alarm limit<br>high pressure|Low||Pressostat x - High alarm|The pressure for pressostat no. x has been above the high alarm<br>limit for longer time than set delay|
|Voltage input x – Low<br>alarm|Low||Analog input x - Low alarm|The voltage signal has been below the low alarm limit for longer<br>time than set delay|
|Voltage input x – High<br>alarm|Low||Analog input x - High alarm|The voltage signal has been above the high alarm limit for longer<br>time than set delay|
|User def. alarm text|Low||Custom alarm x -define text|Alarm on general  alarm input DI x|
|Receiver alarm|High||Prec...|Alarm from the receiver|
|External power loss|High||External power loss|Supply is interrupted. A message alert. All other alarms stopped.|
|Steppervalve|High|Defect supply to valve coil|Stepper - Vhp, Vrec, PI, Vliq.<br>Open coil, Shorted output,|Check the supply to the actual valve.<br>In the event of an error or power failure: check the supply to|
||||Error, Power failure|the stepper module.|
|**System alarms**|||||
|The alarm priority can not|be altered o|n system alarms|||
|Control mode|Low||Manual comp. cap. Control A|Compressors capacity control runs i manual mode|
|Control mode|Low||Manual cond. cap. Control A|Condense capacity control runs i manual mode|
|Refrigerant changed|Low||Refrigerant changed|Refrigerant type has been changed|
||Medium||Time has not been set|Time has not been set|
||Medium||System Critical exception|A unrecoverable critical system failure has occurred – exchange the<br>controller|
||Medium||System alarm exception|A minor system failure has occurred – power off controller|
||Medium||Alarm destination disabled|When this alarm is activated the alarm transmission to the alarm<br>receiver has been deactivated.  Check and wait.<br>When the alarm is cleared the alarm transmission to the alarm<br>receiver has been activated again|
||Medium||Alarm route failure|Alarms can not be transmitted to alarm receiver – check communi-<br>cation|
||High||Alarm router full|The internal alarm buffer has an overrun – this might occur if the<br>controller can not send the alarms to the alarm receiver. Check com-<br>munication between controller and system unit.|
||Medium||Device is restarting|The controller is restarting after flash updating of the software|
||Medium||Common IO Alarm|There is a communication fault between the controller module and<br>the extension modules – the fault must be corrected as soon as<br>possible|
|**Manual control**|||||
||Low||MAN DI……….|The in put in question has been put in manual control mode via the<br>AK-ST 500 service tool software|
||Low||MAN DO………|The output in question has been put in manual control mode via the<br>AK-ST 500 service tool software|
||Low||Man set ....|The output in question has been put in manual control mode via the<br>AK-ST 500 service tool software|
||Low||Man control .....|The output in question has been put in manual control mode via the<br>AK-ST 500 service tool software|

108 | BC186686443705en-000201

##### **Installation considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown.

Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation, for example, could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss will not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer's responsibility to check the installation thoroughly, and to fit the necessary safety devices.

Special reference is made to the necessity of signals to the controller when the compressor is stopped and to the need of liquid receivers before the compressors.

Your local Danfoss agent will be pleased to assist with further advice, etc.
