# Danfoss AK-CC 750A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## User Guide – Controller for evaporator control AK-CC 750A

*Kilde: Danfoss-dokument BC228486437497en-000102.pdf*

**User Guide**

**Controller for evaporator control** AK-CC 750A

ADAP-KOOL® Refrigeration control systems

### **Contents**

|**1. Introduction .............................................................................3**|
|---|
|Application .................................................................................................. 3|
|Principles...................................................................................................... 4|
|**2. Design of a controller ..............................................................7**<br>|
|Module survey ........................................................................................... 8|
|Common data for modules .................................................................10|
|Controller ...........................................................................................12|
|Extension module AK-XM 101A .................................................14|
|Extension module AK-XM 102A / AK-XM 102B .....................16|
|Extension module AK-XM 103A .................................................18|
|Extension module AK-XM 204A / AK-XM 204B .....................20|
|Extension module AK-XM 205A / AK-XM 205B .....................22|
|Extension module  AK-XM 208C ................................................24|
|Extension module AK-OB 110 ....................................................26|
|Display module EKA 163B / EKA 164B .....................................27|
|Graphic display MMIGRS2 ............................................................27|
|Power supply module AK-PS 075 / 150 ...................................28|
|Communication module AK-CM 102 .......................................29|
|Preface to design ....................................................................................30|
|Functions ............................................................................................30|
|Connections ......................................................................................31|
|Limitations .........................................................................................31|
|Design of a evaporator control ..........................................................32|
|Procedure: ..........................................................................................32|
|Sketch ..................................................................................................32|
|Evaporator and refrigerator appliance functions ................32|
|Connections ......................................................................................34|
|Planning table ..................................................................................35|
|Length .................................................................................................36|
|Linking of modules .........................................................................36|
|Determine the connection points ............................................37|
|Connection diagram ......................................................................38|
|Supply voltage .................................................................................39|
|Ordering .....................................................................................................40|
|**3. Mounting and wiring .............................................................41**|
|Mounting ...................................................................................................42|
|Mounting of extension module on the basic module .......42|
|Wiring ..........................................................................................................43|

|**4. Configuration and operation ................................................45**|
|---|
|Configuration ...........................................................................................47|
|Connect PC ........................................................................................47|
|Authorization ....................................................................................48<br>i|
|Unlock the configuration of the controllers ..........................49|
|System setup ....................................................................................50|
|Set plant type ...................................................................................51|
|Definition of thermostat ...............................................................52|
|Definition of sections .....................................................................53|
|Definition of defrost functions ...................................................54|
|Definition of common functions ...............................................55|
|Setup general alarm inputs .........................................................57|
|Setup separate thermostat functions ......................................58|
|Setup separate voltage functions .............................................59|
|Configuration of inputs and outputs .......................................60|
|Set alarm priorities..........................................................................62|
|Lock configuration ..........................................................................64|
|Check configuration .......................................................................65|
|Check of connections ............................................................................66|
|Check of settings.....................................................................................67|
|Installation in network ..........................................................................70|
|First start of control ................................................................................71|
|Start the control ...............................................................................72|
|Setup logs ..........................................................................................73|
|Manual defrost .........................................................................................74|
|**5. Regulating functions .............................................................75**|
|Introduction ..............................................................................................76|
|Thermostat function ..............................................................................77|
|Temperature alarms ...............................................................................81|
|Common functions ................................................................................82|
|General monitoring functions ...........................................................85|
|Liquid injection ........................................................................................86|
|Defrost ........................................................................................................87|
|Miscellaneous ..........................................................................................92|
|Information ...............................................................................................95|
|Alarm texts ................................................................................................96|
|Appendix - Recommended connection Group 1 ........................98|
|Appendix - Recommended connection Group 2 ......................102|

2

### **1. Introduction**

#### **Application**

AK-CC 750A controllers are complete regulating units which together with valves and sensors constitute complete evaporator controls for refrigeration appliances and freezing rooms within commercial refrigeration.

Generally speaking they replace all other automatic controls containing, inter alia, day and night thermostats, defrost, fan control, rail heat control, alarm functions, light control, thermo valve control, solenoid valve, etc.

The controller is equipped with data communication and is operated via a PC.

In addition to evaporator control the controller can give signals to other controllers about the operating condition, e.g. forced closing of expansion valves, alarm signals and alarm messages.

###### **Advantages**

- Control of 1 to 4 evaporator sections

- Adaptive superheat control ensures optimum evaporator usage in all operational circumstances.

- Electronic injection with AKV valve or stepper valve

- Traditional temperature regulation using on/off or modulating control of solenoid valve for both DX and indirect brine system.

- Weighted thermostat and alarm thermostat

- Defrost on demand based on evaporator capacity

- Appliance cleaning function

- Light control using door switch or network signal depending on day/night operation

- Rail heat pulsing depending on day/night operation or dew point

- Monitoring of door alarm and control of light/refrigeration depending on location of door switch.

- Log function for registration of historical parameter values and alarm modes.

###### **Control**

The controller’s main function is to control the evaporator so that the system constantly operates with the most energy-friendly refrigeration.

A specific function for registration of the need for defrost will adapt the number of defrosts so that no energy is wasted on unnecessary defrosts and subsequent cooling-down cycles.

###### **Adaptive defrosting**

The AK-CC 750A includes an adaptive defrosting function. By using the injection valves opening degree as mass flow sensor for the supply of refrigerant, the controller can monitor ice formation on the evaporator. If the load is too large for the standard defrost programme, the controller initiates additional automatic defrost cycles to eliminate the need for expensive service calls due to iced-up evaporators.

Evaporator control of one, two, three or four evaporators

Control of cool or frost appliance

Control of cool or frost room

SW = 1.2x

3

#### **Principles**

The great advantage of this series of controllers is that it can be extended as the size of the plant is increased. It has been developed for refrigeration control systems, but not for any specific application – variation is created through the read-in software and the way you choose to define the connections. It is the same modules that are used for each regulation and the composition can be changed, as required. With these modules (building blocks) it is possible to create a multitude of various kinds of regulations. But it is you who must help adjusting the regulation to the actual needs – these instructions will assist you to find your way through all the open questions so that the regulation can be defined and the connections made.

###### **Advantages**

- The controller’s size can “grow” as systems grow

- The software can be set for one or more regulations

- Several regulations with the same components

- Extension-friendly when systems requirements are changed

- Flexible concept:

- Controller series with common construction

- One principle – many regulation uses

- Modules are selected for the actual connection requirements

- The same modules are used from regulation to regulation

*[Figurtekst: Controller Extension modules · Top part · Bottom part · The controller is the cornerstone of the regulation. The module has inputs and  If the system grows and more functions have to be controlled, the regulation can be · outputs capable of handling small systems. extended. · • The bottom part – and hence the terminals – are the same for all controller types. With extra modules more signals can be received and more relays cut in and out – · • The top part is the intelligence with software. This unit will vary according to con- how many of them – and which – is determined by the relevant application. · troller type. But it will always be supplied together with the bottom part. · • In addition to the software the top part is provided with connection for data com- · munication and address setting. · Examples A regulation with few connections can  If there are many connections one or more exten- · be performed with the controller module  sion modules have to be mounted · alone]*

4

###### **Direct connection**

Setup and operation of an AK controller must be accomplished via the “AK-Service Tool” software program.

The programme is installed on a PC, and setup and operation of the various functions are carried out via the controller’s menu displays.

###### **Displays**

The menu displays are dynamic, so that different settings in one menu will result in different setting possibilities in other menus.

A simple application with few connections will give a setup with few settings.

A corresponding application with many connections will give a setup with many settings.

From the overview display there is access to further displays for the regulation.

At the bottom of the display there is access to a number of general functions, such as “time table”, “manual operation”, “log function”, “alarms”, and “service” (configuration).

###### **Network linking**

The controller can be linked up into a LON-network together with other controllers in an ADAP-KOOL® refrigeration control system.

After the setup operation can be performed at a distance with, say, our software program type AKM.

###### **Users**

The controller comes supplied with several languages, one of which can be selected and employed by the user. If there are several users, they may each have their choice of language. All users must be assigned a user profile which either gives access to full operation or gradually limits the operation to the lowest level that only allows you “to see”.

###### **External display**

An external display can be fitted in order to show the air temperatures around the evaporators. In AK-CC 750A up to 4 displays can be mounted. A graphical display with control buttons can also be fitted.

5

A number of light-emitting diodes makes it possible to follow the signals that are received and transmitted by the controller.

###### **Log**

From the log function you can define the measurements you wish to be shown.

The collected values can be printed, or you may export them to a file. You can open the file in Excel or import in AKM. (The Log function is only available via AK-ST 500.)

If you are in a service situation you can show measurements in a trend function. The measurements are then made real-time and displayed instantly.

###### **Alarm**

The display gives you an overview of all active alarms. If you wish to confirm that you have seen the alarm you can cross it off in the acknowledge field.

If you want to know more about a current alarm you can click on it and obtain an information display on the screen.

A corresponding display exists for all earlier alarms. Here you can upload information if you need further details about the alarm history.

###### **Adaptive defrost**

AK-CC 750A is equipped with an adaptive defrost function. By using an AKV valve (ETS/CCMT Valve) as mass flow sensor for the supply of refrigerant the control can monitor ice formation on the evaporator.

Function can cancel planned defrosts which are not necessary, and on its own initiative start a defrost if the evaporator is about to be blocked by rime and ice.

*[Figurtekst: ■ Power Slow flash = OK · ■ Comm Quick flash = answer from gateway/ · ■ DO1  ■ Status installed in network · ■ DO2  ■ Service Tool Constantly ON = error · ■ DO3  ■ LON Constantly OFF = error · ■ DO4  ■ I/O Extension · ■ DO5  ■ Alarm · ■ DO6 Flash = active alarm/not acknowledged · ■ DO7  ■ Display Constant ON = Active alarm/acknowl- · ■ DO8  ■ Service Pin edged]*

6

### **2. Design of a controller**

This section describes how the controller is designed.

The controller in the system is based on a uniform connection platform where any deviations from regulation to regulation is determined by the used top part with a specific software and by which input and output signals the relevant application will require. If it is an application with few connections, the controller module (top part with belonging bottom part) may be sufficient. If it is an application with many connections it will be necessary to use the controller module plus one or more extension modules.

This section will give you a survey of possible connections plus assistance in selecting the modules required by your actual application.

7

#### Module survey

- Controller module – capable of handling minor plant requirements.

- Extension modules. When the numbers of evaporators becomes greater and additional inputs or outputs are required, modules can be attached to the controller. A plug on the side of the module will transmit the supply voltage and data communication between the modules.

- Optional connection

When a regulation is planned (set up) it will generate a need for a number of connections distributed on the mentioned types. This connection must then be made on either the controller module or an extension module. The only thing to be observed is that the types must not be mixed (an analog input signal must for instance not be connected to a digital input).

   - Programming of connections

- Top part

- The upper part of the controller module contains the intelligence. This is the unit where the regulation is defined and where data communication is connected to other controllers in a bigger network.

   - The controller must know where you connect the individual input and output signals. This takes place in a later configuration where each individual connection is defined based on the following principle:

   - to which module

   - at which point (”terminals”)

- Connection types There are various types of inputs and outputs. One type may, for example, receive signals from sensors and switches, another may receive a voltage signal, and a third type may be outputs with relays etc. The individual types are shown in the table below.

- what is connected (e.g. pressure transmitter/type/ pressure range)

*[Figurtekst: Extension module with additional · relay outputs and additional ana- · log inputs.]*

*[Figurtekst: relay outputs and additional ana- · log inputs. · Extension module with ad- · ditional analog inputs · External display · for appliance · Bottom part · temperature etc. · Controller with analog inputs and · relay outputs. · The module with additional relay outputs is · Top part · also available in a version where the top part · is provided with change-over switches so · that the relays can be overridden.]*

8

|1. Controller|||
|---|---|---|
|**Type**|**Function**|**Application**|
|AK-CC 750A|Controller for evaporator control|Refrigeration appliances control|

|2. Extension mo<br>|dules and surveyof<br>|inputs and<br>**f**|outputs<br>**f**|**f**|**f**||||
|---|---|---|---|---|---|---|---|---|
|**Type**|**Analog**<br>**inputs**|**On/Off out**|**f puts**|**On/off suppl**<br>**(DI signal)**|**f y voltage**|**Analoge**<br>**outputs**|**Stepper**<br>**output**|**Module with**<br>**switches**|
||For sensors, pres-<br>sure transmitters<br>etc.|Relay<br>(SPDT)|Solid state|Low voltage<br>(max. 80 V)|High voltage<br>(max. 260 V)|0 -10 V d.c.|For valves<br>with step<br>control|For override of<br>relay outputs|
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
|<br>The following e<br>There is onlyro|xtension module can<br>om for one module.|be placed on|the PC board in th|e controller mod|ule.||||
|AK-OB 110||||||2|||

|3. AK operation|and accessories||
|---|---|---|
|**Type**|**Function**|**Application**|
|**Operation**|||
|AK-ST 500|Software for operation of AK controllers|AK-operation|
|-|Cable between PC and AK controller|USB-A — USB-B (standard IT cable)|
|**Accessories**|**Power supply module 230 V / 115 V to 24 V**||
|AK-PS 075|18 VA,24 V d.c.|Sl f tll|
|AK-PS 150|36 VA,24 V d.c.|uppy or conroer|
|**Accessories**|**External display that can be connected to the controller module**|**. For showing, say, the refrigeration appliances**|
|EKA 163B|Display||
|EKA 164B|Display with operation buttons||
|MMIGRS2|Graphic display with operation buttons||
|-|Cable between EKA display and controller|Length = 2 m, 6 m|
|-|Cable between graphic display and controller|Length = 1,5 m, 3 m|
|**Accessories**|**Communication modules for controllers where modules cannot**|**be connected continuously**|
|AK-CM 102|Communication module|Data communication for external exten-<br>sion modules|

On the following pages there is data specific to each module.

9

#### **Common data for modules**

|Supply voltage|24 V d.c. / a.c.  +/- 20%||
|---|---|---|
|Power consumption|AK-__ (controller)|8 VA|
||AK-XM 101, 102, 103|2 VA|
||AK-XM 204, 205, 208|5 VA|
|Analog inputs|Pt 1000 ohm /0°C|Resolution: 0.1°C<br>Accurac:|
||PTC 1000 ohm /0°C|y<br>+/- 0.5°C (between -50°C and +50°C)<br>+/- 1°C between -100°C and -50°C<br>+/- 1°C between +50°C and +130°C|
||Pressure transmitter type AKS 32R / AKS<br>2050 / AKS 32 (1-5 V)|Resolution:1 mV<br>Accuracy +/- 10 mV<br>|
||Voltage signal 0-10 V|Max. connection of 5 pressure transmitters on one module|
||Contact function (On/Off)|On at R < 20 ohm<br>Off at R > 2K ohm<br>(Gold -plated contacts not necessary)|
|On/off supply voltage inputs|Low voltage<br>0 / 80 V a.c./d.c.|Off: U < 2 V<br>On: U > 10 V|
||High voltage<br>0 / 260 V a.c.|Off: U < 24 V<br>On: U > 80 V|
|Relay outputs<br>SPDT|AC-1 (ohmic)|4 A|
||AC-15 (inductive)|3 A|
||U|Min. 24 V<br>Max. 230 V<br>Low and high voltage must not be connected to the same<br>output group|
|Solid state outputs|Can be used for loads that are cut in and<br>out frequently, e.g. :<br>rail heat, fans and AKV valve|Max. 240 V a.c. , Min. 48 V a.c.<br>Max. 0.5 A,<br>Leak < 1 mA<br>Max. 1 AKV|
|Stepper outputs|Used for valves with stepper input|20-500 step/s<br>Separate supplyto  stepper outputs : 24 a.c./d.c./ xx VA|
|Ambient temperature|During transport|-40 to 70°C|
||During operation|-20 to 55°C ,<br>0 to 95% RH (non condensing)<br>No shock influences / vibrations|
|Enclosure|Material|PC / ABS|
||Density|IP10 , VBG 4|
||Mounting|For mounting on panel wall or DIN rail|
|Weight with screw terminals|modules in100- / 200- / controller-series|Ca. 200 g / 500 g / 600 g|
|Approvals|EU low voltage directive and EMC require-<br>ments are complied with|LVD tested according to EN 60730<br>EMC tested<br>Immunity according to EN 61000-6-2<br>Emission according to EN 61000-6-3|
|||E31024 for CC-module|
|||E357029 for XM and CM-modules|

The mentioned data applies to all modules.

If data is specific, this is mentioned together with the module in question.

10

###### **Dimensions**

The module dimension is 72 mm. Modules in the 100-series consist of one module Modules in the 200-series consist of two modules Controllers consist of three modules

The length of an aggregate unit = n x 72 + 8

11

##### **Controller**

There are several controllers in the series. The function is determined by the programmed software, but outwardly the controllers are identical – they all have the same connection possibilities: 11 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

8 digital outputs, with 4 Solid state outputs and 4 relay outputs

24 V a.c. or d.c. to be connected to the controller.

The 24 V must **not** be retransmitted and used by other controllers as it is not galvanically separated from inputs and outputs. In other words, you **must** use a transformer for each controller. Class II is required. The terminals must **not** be earthed.

The supply voltage to any extension modules is transmitted via the plug on the right-hand side.

The size of the transformer is determined by the power requirement of the total number of modules.

The supply voltage to a pressure transmitter can be taken either from the 5 V output or from the 12 V output depending on transmitter type.

###### **Data communication**

If the controller is to be included in a system, communication must take place via the LON connection. The installation has to be made as mentioned in the separate instructions for LON communication.

###### **Address setting**

When the controller is connected to a gateway type AKA 245, the controller’s address must be set between 1 and 119. (1-200 at AK-SM..).

###### **Service PIN**

*[Figurtekst: PIN · Address · Keep the safety · distance! · Low and high · voltage must not · be connected to · the same output · group]*

When the controller is connected to the data communication cable the gateway must have knowledge of the new controller. This is obtained by pushing the key PIN. The LED “Status” will flash fast when the gateway sends an acceptance message.

###### **Operation**

The configuration operation of the controller must take place from the software programme “Service Tool”. The program must be installed on a PC, and the PC must be connected to the controller via the network plug on the front of the unit.

There are two rows with LED’s. They mean: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

Right row:

- Software status (slow flash = OK)

- Communication with Service Tool

- Communication on LON

*[Figurtekst: Slow flash = OK · ■ Power Quick flash = answer from gateway · ■ Comm Installation in network · ■ DO1  ■ Status Constantly ON = error · ■ DO2  ■ Service Tool Constantly OFF = error · ■ DO3  ■ LON · ■ DO4  ■ I/O Extension · ■ DO5  ■ Alarm Flash = active alarm/not cancelled · ■ DO6 Constant ON = Active alarm/cancelled · ■ DO7  ■ Display · ■ DO8  ■ Service Pin]*

- Communication with AK-CM 102

- Alarm when LED flashes

- 1 LED that is not used

- Communication with display on RJ11 plug

- “Service Pin” switch has been activated

12

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 9 10 11 Terminal 15:  12 V · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 AI9 AI10 AI11 Terminal 16:  5 V · Terminal 27:  12 V · Terminal 28:  5 V · Terminal · Analog · 17, 18, 29, 30: · inputs · (Cable screen) · on 1 - 11 · The screen on the pressure · transmitter cables must · only be connected at the · end of the controller. · Relay outputs on · 16 - 19 · Solid state outputs · on 12 - 15 · Relay or AKV coil · 24 and 25 used · fx 230 V a.c. · only when "Op- · tion board fitted"  Point 12 13 14 15 16 17 18 19 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Signal · type · S · S2, · Pt 10 00  ohm/0°C S3 · S4, Pt 1000 · S5 · Saux · P · AKS 32R  3: Brown · AK S 2050 · 2: Blue AKS 32R · AKS 2050 · 1: Black P0 MBS 8250 · Pc · -1 - xx bar · Paux · 3: Brown AKS 32 · A KS 32 -1 - zz bar · 2: Black · 1: Red · Signal Module Point  Terminal Signal type / · Active at · U 1  (AI 1) 1 - 2 · 0 - 5 V 2  (AI 2) 3 - 4 · ... 0 - 10 V · 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · 5  (AI 5) 9 - 10 · On/Off Ext.  Active at: 6  (AI 6) 11 - 12 · Main · switch 7  (AI 7) 13 - 14 · Closed · / 8  (AI 8) 19 - 20 · Day/ · Open · Night 9  (AI 9) 21 - 22 · Door 10  (AI 10) 23 - 24 · Defrost · 1  11  (AI 11) 25 - 26 · DO Active at: 12  (DO 1) 31 - 32 · AKV On 13  (DO 2) 33 - 34 · Fan · Alarm  / 14  (DO 3) 35 - 36 · Off · LightRail heat 15  (DO 4) 37 - 38 · Defrost 16  (DO 5) 39 - 40- 41 · Night · blind 17  (DO6) 42 - 43 - 44 · Valves · 18  (DO7) 45 - 46 - 47 · Compres- · sor 19  (DO8) 48 - 49 - 50 · 24  - · Option Board Please see the signal  25  - · on the page with the · module. · AKV]*

13

##### **Extension module AK-XM 101A**

The module contains 8 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

Supply voltage to a pressure transmitter can be taken from either the 5 V output or the 12 V output depending on transmitter type.

Only the two top LED’s are used. They indicate the following:

- Voltage supply to the module

- Communication with the controller is active (red = error)

14

*[Figurtekst: Point Point 1 2 3 4 · Type AI1 AI2 AI3 AI4 · Terminal 9:   12 V · Terminal 10:   5 V · Terminal 15:   5 V · At the top the · Terminal 16:   12 V · signal input is · the left of the · two terminals. Terminal · 11, 12, 13, 14: · (Cable screen) · The screen on the pressure · transmitter cables must only · At the bottom  be connected at the end of the · controller. · the signal input · is the right of the · two terminals. · Point 5 6 7 8 · Signal Signal  Type AI5 AI6 AI7 AI8 · type · S · S2 · Pt 1000 ohm/0°C S3 · Pt 1000 · S4 · S5 · Saux · P · AKS 32R · AKS 2050  3: Brown · 2: Blue AKS 32R · AKS 2050 · 1: Black P0 MBS 8250 · Pc -1 - xx bar · Paux · AKS 32 3: Brown AKS 32 · -1 - zz bar · 2: Black · 1: Red · U · Signal Module Point Terminal Signal type / · Active at · 0 - 5 V · ... 0 - 10 V 1  (AI 1) 1 - 2 · 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · On/Off Active at: 4  (AI 4) 7 - 8 · Ext. · Main  Closed 5  (AI 5) 17 - 18 · switch · / · Day/ Open 6  (AI 6) 19 - 20 · Night · Door 7  (AI 7) 21 - 22 · Defrost · 8  (AI 8) 23 - 24]*

15

##### **Extension module AK-XM 102A / AK-XM 102B**

The module contains 8 inputs for on/off voltage signals.

###### **Signal**

AK-XM 102A is for low voltage signals. AK-XM 102B is for high voltage signals.

They indicate:

- Voltage supply to the module

- Communication with the controller is active (red = error)

**AK-XM 102A AK-XM 102B Max. 24 V Max. 230 V** On/Off: On/Off: On: DI > 10 V a.c./d.c. On: DI > 80 V a.c. Off: DI <  2 V a.c./d.c. Off: DI < 24 V a.c.

- Status of the individual inputs 1 to 8 (when lit = voltage)

16

*[Figurtekst: Point Point 1 2 3 4 · Type DI1 DI2 DI3 DI4 · Point 5 6 7 8 · Type DI5 DI6 DI7 DI8]*

*[Figurtekst: Point 5 6 7 8 · Type DI5 DI6 DI7 DI8 · Signal Active at · DI · AK-XM 102A: Max. 24 V  Ext. · AK-XM 102B: Max. 230 V Main · Closed · switch · (voltage on) · Day/ / · Night · Door  Open · (voltage off) · Defrost · (The module can not register a pulse signal from e.g. a · reset function or a case cleaning function.) · Signal Module Point Terminal Active at · 1  (DI 1) 1 - 2 · 2  (DI 2) 3 - 4 · 3  (DI 3) 5 - 6 · 4  (DI 4) 7 - 8 · 5  (DI 5) 9 - 10 · 6  (DI 6) 11 - 12 · 7  (DI 7) 13 - 14 · 8  (DI 8) 15 - 16]*

17

##### **Extension module AK-XM 103A**

The module contains :

4 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

4 analog voltage outputs of 0 - 10 V

Supply voltage to a pressure transmitter can be taken from either the 5 V output or the 12 V output depending on transmitter type.

###### **Galvanic isolation**

The inputs are galvanically separated from the outlets. The outlets AO1 and AO2 are galvanically separated from AO3 and AO4.

Only the two top LED’s are used. They indicate the following:

- Voltage supply to the module

- Communication with the controller is active (red = error)

###### **Max. load**

I < 2.5 mA R > 4 kΩ

18

*[Figurtekst: Point Point 1 2 3 4 Terminal 9:   12 V · Type AI1 AI2 AI3 AI4 Terminal 10:  5 V · Terminal · 11, 12: · (Cable screen) · At the top the · The screen on the pressure · signal input is  transmitter cables must only · the left of the  be connected at the end of the · two terminals. controller. · Galvanic isolation: · AI 1-4 ≠ AO 1-2 ≠ AO 3-4 · At the bottom · the signal input · is the right of the · two terminals. · Point 5 6 7 8 · Signal Signal  Type AO1 AO2 AO3 AO4 · type · S · S2 · Pt 10 00  ohm/0°C S3 · Pt 1000 · S4 · S4 · S5 · Saux · P · AKS 32R · 3: Brown · 2: Blue AKS 32R / · AKS 2050 · 1: Black P0 MBS 8250 · -1 - xx bar · AKS 32 Paux · AKS 32 · 3: Brown -1 - zz bar · 2: Black · 1: Red · U · Si g nal Module Point Terminal Si g nal t yp e /Active at · 1  (AI 1) 1 - 2 · 0 - 5 V · ... 0 - 10 V 2  (AI 2) 3 - 4 · 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · On/Off Ext.  Active at: · Main  5  (AO 1) 17 - 18 · switch · Day/ Closed/ 6  (AO 2) 19 - 20 · Night · Open 7  (AO 3) 21 - 22 · Door · Level  8  (AO 4) 23 - 24 · switch · AO · 0-10 V]*

19

##### **Extension module AK-XM 204A / AK-XM 204B**

The module contains 8 relay outputs.

###### **AK-XM 204B only**

###### **Override of relay**

Eight change-over switches at the front make it possible to override the relay’s function.

Either to position OFF or ON.

In position Auto the controller carries out the control.

There are two rows with LED’s. They indicate the following: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

- Right row: (AK-XM 204B only):

- Override of relays

- ON = override

- OFF = no override

###### **Fuses**

Behind the upper part there is a fuse for each output.

*[Figurtekst: AK-XM 204A  AK-XM 204B]*

*[Figurtekst: Keep the safety distance! · Max. 230 V Low and high voltage · AC-1: max. 4 A (ohmic) must not be connected to · AC-15: max. 3 A (Inductive) the same output group]*

*[Figurtekst: AK-XM 204B · Override of relay]*

20

*[Figurtekst: Point 1 2 3 4 5 6 7 8 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8]*

*[Figurtekst: Signal Active at · DO Fan · Alarm · On · Light / · Railheat · Defrost Off · Night · blind · Valve · Compres- · sor]*

*[Figurtekst: Si g nal Module Point Terminal Active at · 1  (DO 1) 25 - 27 · 2  (DO 2) 28 - 30 · 3  (DO 3) 31 - 33 · 4  (DO 4) 34 -36 · 5  (DO 5) 37 - 39 · 6  (DO 6) 40 - 41 - 42 · 7  (DO 7) 43 - 44 - 45 · 8  (DO 8) 46 - 47 - 48]*

21

##### **Extension module AK-XM 205A / AK-XM 205B**

The module contains:

- 8 analog inputs for sensors, pressure transmitters, voltage signals and contact signals.

8 relay outputs.

###### **AK-XM 205B only**

###### **Override of relay**

Eight change-over switches at the front make it possible to override the relay’s function. Either to position OFF or ON.

In position Auto the controller carries out the control.

There are two rows with LED’s. They mean: Left row:

- Voltage supply to the controller

- Communication active with the bottom PC board (red = error)

- Status of outputs DO1 to DO8

- Right row: (AK-XM 205B only):

- Override of relays

- ON = override

- OFF = no override

###### **Fuses**

Behind the upper part there is a fuse for each output.

*[Figurtekst: AK-XM 205A  AK-XM 205B · max. 10 V · Max. 230 V Keep the safety distance! · AC-1: max. 4 A (ohmic) Low and high voltage · AC-15: max. 3 A (Inductive) must not be connected to · the same output group · AK-XM 205B · Override of relay]*

22

*[Figurtekst: Point Point 1 2 3 4 5 6 7 8 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8]*

*[Figurtekst: Terminal  9:  12 V · Terminal 10:  5 V · Terminal 21:  12 V · Terminal 22:  5 V · Terminal 11, 12, 23, 24 : · (Cable screen) · The screen on the pressure · transmitter cables must only · be connected at the end of the · controller. · Point 9 10 11 12 13 14 15 16 · Type DO1 DO2 DO3 DO4 DO5 DO6 DO7 DO8 · Signal Signal · type · S · S2, · Pt 1000 ohm/0°C S3 · Pt 1000 · S4, · S5 · Saux · P · AKS 32R · AKS 2050 3: Brown · 2: Blue AKS 32R · AKS 2050 · 1: Black P0 MBS 8250 · Pc -1 - xx bar · Paux · AKS 32 3: Brown AKS 32-1 - zz bar · 2: Black · 1: Red Signal Module Point Terminal Signal type / · Active at · 1  (AI 1) 1 - 2 · U · 2  (AI 2) 3 - 4 · 0 - 5 V · ... 0 - 10 V 3  (AI 3) 5 - 6 · 4  (AI 4) 7 - 8 · 5  (AI 5) 13 - 14 · On/Off Active at: 6  (AI 6) 15 - 16 · Ext. Main 7  (AI 7) 17 - 18 · switch Closed · Day/ / 8  (AI 8) 19 -20 · Night Open · Door 9  (DO 1) 25 - 26 - 27 · Defrost · 10  (DO 2) 28 - 29 - 30 · DO Active at: 11  (DO 3) 31 - 30 - 33 · Fan · AlarmLight on/ 12  (DO 4) 34 - 35 - 36 · Rail heat 13  (DO 5) 37 - 36 - 39 · Defrost Off · Night  14  (DO6) 40 - 41 - 42 · blind · Valve 15  (DO7) 43 - 44 - 45 · Compr. · 16  (DO8) 46 - 47 - 48]*

23

##### **Extension module  AK-XM 208C**

*[Figurtekst: The module contains: · 8 analog inputs for sensors, pressure transmitters, voltage signals · and contact signals. · 4 outputs for stepper motors. · Supply voltage · The supply voltage to the module comes from the previous mod- · ule in the row. Here supplied with 5 VA. · The supply voltage to the valves must be from a separate supply, · which must be galvanically separated from the supply for the · control range. Separate voltage · (Power requirements: 7.8 VA for controller + xx VA per valve). supply is required · A UPS may be necessary if the valves need to open/close during a  24 V d.c. Fx. 13 VA · power failure. max. 10 V · Light-emitting diodes · There is one row with LED’s. It indicate the following: · • Voltage supply to the module · • Communication active with the bottom PC board (red = error) · • Step1 to step4 OPEN: Green = Open · • Step1 to step4 CLOSE: Green = Close · • Red flash = Error on motor or connection · Output: · 24 V d.c. · 20-500 step/s · Max phase current  = 325 mA RMS · ∑ Pout   = max. 21 VA · The connection to the valve must not · be broken using a relay · L = max. 30 m]*

*[Figurtekst: Valve data · Type P · ETS 12.5 - ETS 400 1.3 VA · KVS 15 - KVS 42 · CCMT 2 - CCMT 8 · CCM 10 - CCM 40 · CTR 20 · CCMT 16 - CCMT 42 5.1 VA]*

###### **Power supply to AK-XM 208C:**

Fx: 7.8 + (4 x 1.3) =  13 VA  AK-PS 075

Fx: 7.8 + (4 x 5.1) = 28.2 VA  AK-PS 150

24

*[Figurtekst: Point 1 2 3 4 5 6 7 8 · Type AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 · Terminal 17:  12 V · Terminal 18:  5 V · Terminal 19, 20: · (Cable screen) · The screen on the pressure · transmitter cables must only · be connected at the end of · the controller. · Point 9 10 11 12 · Step 1 2 3 4 · Type AO · 1 25 26 27 28 · Step / 2 29 30 31 32 · Terminal 3 33 34 35 36 · 4 37 38 39 40 · ETS · CCM / CCMT · White Black Red Green · CTR · KVS]*

###### **Point**

*[Figurtekst: Valve Module Ste p Terminal · 1 (point 9) 25 - 28 · 2 (point 10) 29 - 32 · 3 (point 11) 33 - 36 · 4 (point 12) 37 - 40]*

25

##### **Extension module AK-OB 110**

*[Figurtekst: Function · The module contains two analog voltage outputs of 0 – 10 V. · Supply voltage · The supply voltage to the module comes from the controller · module. · Placing · The module is placed on the PC board in the controller module. · Point · The two outputs have points 24 and 25. They are shown on the · earlier page where the controller is also mentioned. · Galvanic isolation · The outlets AO1 and AO2 are galvanically separated from the · controller module, but  not  from each other. · Max. load · I < 2.5 mA · R > 4 kohm · Module 1 · AO Point 24 25 · AO 0 - 10 V AO2 · Type AO1 AO2 · AO1]*

26

##### **Display module EKA 163B / EKA 164B**

Display of important measurements from the controller, e.g. appliance temperature. Setting of the individual functions can be performed by using the display with control buttons.

It is the controller used that determines the measurements and settings that can occur.

*[Figurtekst: settings that can occur. · Connection · The extension module is connected to the controller module via · EKA 163B   EKA 164B · a cable with plug connections. You have to use one cable per · module. The cable is supplied in various lengths. · Both types of display (with or without control buttons) can be · connected to either display output A, B, C and D. · When the controller starts up, the display will show the output · that is connected. · - - 1 = output A · - - 2 = output B · etc. · Placing · The extension module can be placed at a distance of up to 15 m · from the controller module. · Point · No point has to be defined for a display module – you simply · connect it. · Graphic display MMIGRS2 · Function · Setting and display of values in the controller. · Connection · The display connects to the controller via a cable with RJ11 plug · connections. · Supply voltage · Received from the controller via cable and RJ11 connector. · Termination · The display must be terminated. Mount a connection between the · terminals H and R. · (AK-CC 750A is terminated internally.) · Placing · The display can be placed at a distance of up to 3 m from the · controller. · Point / Address · No point has to be defined for a display – you simply connect it. · However, the address must be verified. See the instructions ac-]*

No point has to be defined for a display – you simply connect it. However, the address must be verified. See the instructions accompanying the controller.

27

##### **Power supply module AK-PS 075 / 150**

24 V supply for controller.

230 V a.c or 115 V a.c. (from 100 V a.c. to 240 V a.c.)

###### **Placing**

On DIN-rail

Class II

###### **Effect**

|**Type**|**Output tension**|**Output current**|**Power**|
|---|---|---|---|
|AK-PS 075|24 V d.c.|0.75 A|18 VA|
|AK-PS 150|24 V d.c.<br>(adjustable)|1.5 A|36 VA|

|**Dimension**|||
|---|---|---|
|**Type**|**High**|**Width**|
|AK-PS 075|90 mm|36 mm|
|AK-PS 150|90 mm|54 mm|

###### **Supply to a controller**

###### **Connections**

*[Figurtekst: AK-PS 075 AK-PS 150]*

28

##### **Communication module AK-CM 102**

The module is a new communication module, meaning the row of extension modules can be interrupted.

The module communicates with the regulator via data communication and forwards information between the controller and the connected extension modules.

###### **Connection**

Communication module and controller fitted with RJ 45 plug connectors.

**Nothing** else should be connected to this data communication; a maximum of 5 communication modules can be connected to one controller.

###### **Communication cable**

One metre of the following is enclosed: ANSI/TIA 568 B/C CAT5 UTP cable w/ RJ45 connectors.

###### **Positioning**

Max. 30 m from the controller (The total length of the communication cables is 30 m)

24 volt AC or DC should be connected to the communication module.

The 24 V can be sourced from the same supply that supplies the controller. (The supply for the communication module is galvanically separated from the connected extension modules). The terminals must **not** be earthed.

The power consumption is determined by the power consumption of the total number of modules.

The controller strand load must not exceed 32 VA. Each AK-CM 102 strand load must not exceed 20 VA.

###### **Point**

Connection points on the I/O modules should be defined as if the modules were an extension of each other.

###### **Address**

The address for the first communication module should be set to 1. Any second module should be set to 2.  A maximum of 5 modules can be addressed.

###### **Termination**

The termination switch on the final communication module should be set to ON.

The controller should permanently be set to = ON.

###### **Warning**

Additional modules may only be installed following the installation of the final module. (Here following module no. 11; see the sketch.)

After configuration, the address must not be changed.

*[Figurtekst: Max. 32 VA · Max. 20 VA · Max. 20 VA]*

29

#### **Preface to design**

Be aware of the following when the number of extension modules is being planned. A signal may have to be changed, so that an additional module may be avoided.

- An ON/OFF signal can be received in two ways. Either as a contact signal on an analog input or as voltage on a low or highvoltage module.

- An ON/OFF output signal can be given in two ways. Either with a relay switch or with solid state. The primary difference is the permitted load and that the relay switch contains a cutout switch.

Mentioned below is a number of functions and connections that may have to be considered when a regulation has to be planned. There are more functions in the controller than the ones mentioned here, but those mentioned have been included in order that the need for connections can be established.

##### **Functions**

###### **Clock function**

Clock function and change-over between summer time and winter time are contained in the controller. The clock setting is maintained for at least 12 hours at a power failure.

The clock setting is kept updated if the controller is linked up in a network with a system manager.

###### **Start/stop of regulation**

Regulation can be started and stopped via the software. External start/stop can also be connected.

###### **Alarm function**

If the alarm is to be sent to a signal transmitter, a relay output will have to be used.

###### **Extra temperature sensors and pressure sensors**

If additional measurements have to be carried out beyond the regulation, sensors can be connected to the analog inputs.

###### **Forced control**

The software contains a forced control option. If an extension module with relay outputs is used, the module’s top part can be with change-over switches – switches that can override the individual relays into either OFF or ON position.

###### **Data communication**

The controller module has terminals for LON data communication. The requirements to the installation are described in a separate document.  Literature number RC8AC.

30

##### **Connections**

In principle there are the following types of connections:

###### **Analog inputs ”AI”**

- This signal must be connected to two terminals. Signals can be received from the following sources: • Temperature signal from Pt 1000 ohm temperature sensor

- • Pulse signal or reset signal • Contact signal where the input is shortcircuited or ”opened”, respectively

- • Voltage signal from 0 to 10 V • Signal from pressure transmitter AKS 32, AKS 32R, AKS 2050 or MBS 8250. The supply voltage is supplied from the module’s terminal board where there is both a 5 V supply and a 12 V supply. When programming the pressure transmitter’s pressure range must be set.

**ON/OFF voltage inputs ”DI”** This signal must be connected to two terminals.

- The signal must have two levels, either 0 V or ”voltage” on the input. There are two different extension modules for this signal type:

- low-voltage signals, e.g. 24 V

- high-voltage signals, e.g. 230 V

###### **ON/OFF output signals ”DO”**

There are two types, as follows:

• Relay outputs All relay outputs are with change-over relay so that the required function can be obtained when the controller is without voltage.

• Solid state outputs Primarily for AKV valves which connect quickly. But output can cut an external relay in and out, as with a relay output. The output is only found on the controller module.

When programming the function must be set:

- Active when the output is activated

- Active when the output is not activated.

###### **Analog output signal ”AO”**

This signal is to be used if a control signal is to be transmitted to an external valve or to fans with EC motors. When programming the signal range must be defined: 0-5 V, 1-5 V, 0-10 V or 2-10 V.

Pulse signal for the stepper motors. This signal is used by valve motors of the type ETS, KVS, CCMT and CTR. The valve type should be set during programming.

When programming the function must be set:

- Active when the input is without voltage

- Active when voltage is applied to the input.

##### **Limitations**

As the system is very flexible  regarding the number of connected units you must check whether your selection complies with the few limitations there are.

The complexity of the controller is determined by the software, the size of the processor, and the size of the memory. It provides the controller with a certain number of connections from which data can be downloaded, and others where coupling with relays can be performed.

The controller **is not** made for use on plate heat exchanger.

- ✔ The sum of connections cannot exceed **80.**

- ✔ The number of extension modules must be limited so that the total power will not exceed **32** VA (including controller).

- ✔ No more than **5** pressure transmitters may be connected to one controller module.

- ✔ No more than **5** pressure transmitters may be connected to one extension module.

###### **Common pressure transmitter**

If several controllers receive a signal from the same pressure transmitter, the supply to the affected controllers must be wired so that it is not possible to switch off one of the controllers without also switching off the others. (If one controller is switched off, the signal will be pulled down, and all the other controllers will receive a signal which is too low)

31

#### **Design of a evaporator control**

##### **Procedure:**

1. Make a sketch of the system in question

2. Check that the controller’s functions cover the required application

**Follow these 12 steps**

3. Consider the connections to be made

4. Use the planning table. / Note down the number of connections ./ add up

5. Are there enough connections on the controller module? – If not, can they be obtained by changing an ON/OFF input signal from voltage signal to contact signal, or will an extension

- module be required?

6. Decide which extension modules are to be used

7. Check that the limitations are observed

8. Calculate the total length of modules

9. The modules are linked together

10. The connection sites are established

11. Draw a connection diagram or a key diagram

12. Size of supply voltage/transformer

##### **1**

##### **Sketch**

Make a sketch of the system in question.

##### **2Evaporator and refrigerator appliance** **functions**

||AK-CC<br>750A|
|---|---|
|**Application**||
|Control of cold room or freezing room|x|
|Control of refrigeration or freezing appliances|x|
|Regulation of evaporators|1 - 4|
|**Thermostat function**||
|Common thermostat function for all sections|x|
|Thermostat function for each section|x|
|On/off thermostat with AKV / ETS or solenoid valve|x|
|Modulating thermostat with AKV / ETS valve|x|
|Change between two thermostat references (thermostat band)|x|
|Day/night switch|x|
|Displacement of  reference via analog input signal|x|
|Thermostat sensor before or after evaporator|x|
|Thermostat sensor both before and after the evaporator (weighted<br>thermostat)|x|
|Alarm thermostat (weighted)|x|
|**Common functions**||
|Fan control (pulsation or EC motor)|x|
|Rail heat control (pulsation)|x|
|Compressor control. Relay active when refrigeration is demanded|x|
|Appliance cleaning function|x|
|Appliance shut down|x|
|Door contact function|x|
|Light function|x|
|Night blind|X|
|Forced closing|x|
|Alarm output|x|
|Start / stopof regulation|x|

32

|Receive external on/off alarm signal|10|
|---|---|
|Receive external analog alarm signal|5|
|Product sensor with alarm function|4|
|**Liquid injection**||
|Control of AKV / stepper valves|4|
|Control of solenoid valves in liquid line|4|
|Superheat regulation wit P0 and S2 measurement|x|
|MOP control|x|
|Refrigerant choice|x|
|**Defrost function**||
|Electrical defrost|4|
|Warm Brine defrost, Hot gas defrost|x|
|Smelt function|x|
|Drip tray heat|X|
|Adaptive defrost|x|
|Defrost stop on temperature or time|x|
|Coordinated defrost via network|x|
|**Miscellaneous**||
|Dedicated alarm for refrigerant leak|x|
|Alarm priorities|x|
|Sensor correction|x|
|Option for connection of separate display|4|
|Separate thermostats|5|
|Separatepressostats|5|
|**System signals via data communication**||
|Signal for P0-optimasation|x|
|Night setback|x|
|Inject ON-signal (forced closing)|x|
|Light control|x|
|Coordinated defrost|x|
|Forced cooling|x|

###### **A bit more about the functions**

###### **Common  thermostat**

The thermostat temperature can be either a weighting of the S3 and S4 sensors in section A.

Alternatively, the thermostat temperature can be a minimum value, a maximum value or an average value of all S3 or S4 sensors for the refrigeration sections used.

###### **Modulating thermostat**

AKV / stepper:

The function can only be used on central plant.

The opening degree of the valve is adjusted so that an accurate, constant temperature is maintained. .

###### **Day/night signal for raising the reference**

The built-in week diagram can be used for raising the thermostat reference, but it is also possible to use an external ON/OFF signal or a signal via the network.

###### **Product sensors**

Each appliance section has a separate product sensor which can be used for monitoring/registering the temperature.

###### **Appliance cleaning function**

A switch function with pulse pressure will activate the function whereupon refrigeration will be stopped. The fans continue operating.

”Later”: Next push on the switch will stop the fans. ”Still later”: Next push on the switch will restart refrigeration. When a display is mounted at the appliance the various situations may be followed by the readout:

Normal operation: Appliance temperature

1st push: Fan

2nd push: OFF

3rd push: Appliance temperature

###### **Appliance shut down**

Signal about shutdown can be received via data communication or from a contact on a On/Off input.

###### **Door switch function**

In freezing and cold rooms the door switch is used for switching the light on and off, for starting and stopping the refrigeration, and for sounding the alarm if the door has been open for a long time

###### **Light function**

The light function can be activated by the door switch, the internal time diagram or a signal via the network.

###### **Defrost sensor S5**

On long evaporators it may be necessary to mount two sensors in order to ensure the correct defrost of the evaporator. The sensors are for example named S5A-1 and S5A-2.

###### **“Inject ON” override function**

The function closes expansion valves on the evaporator control when all compressors are stopped.

The function can take place via the data communication, or it may be wired via a relay output.

###### **Adaptive defrost**

The function requires signals from S3 and S4 as well as from condensing pressure Pc.  The expansion valve must furthermore be type AKV.

The function cannot be used in combination with pulsation of fans.

Solenoid valve:

This function can be used on both central systems and on indirect refrigeration appliances. The valve's duty cycle is adapted so that optimum temperature regulation is achieved on the basis of a specific time period. The valve's duty cycle is desynchronised so that an even load is achieved across the entire system

###### **If you want to know more about the functions, go to chapter 5.**

###### **Changeover between two thermostat references**

The function is used for appliances where contents are frequently changed and where a different thermostat reference is required. Changeover between the two references can take place by means of a switch function.

33

##### **3**

###### **Connections**

Here is a survey of the possible connections. The texts can be read in context with the planning table in point 4.

###### **Analog inputs**

Temperature sensors each section

- S3 air sensor at evaporator inlet

- S4 air sensor at evaporator outlet (one of the S3/S4 sensors may be omitted)

- .• S5 defrost sensor. Two may be used for long sections

- Product sensor. Extra sensor that only checks the product temperature

- S2 gas sensor at evaporator outlet (control of AKV valve).

- Saux 1-4, extra sensors, which can be used for general thermostats or monitoring.

- External start/stop of regulation

- Pulse pressure (on a analogue input) used for the ”appliance cleaning” function

- Switch for changeover between two temperature referenc

- Inject ON. Signal from a compressor control

- Pulse pressure (on a analogue input) for start of defrost

- Pulse pressure (on a analogue input) for opening/closing Night blind

- Door switch in coldroom

- External day/night signal (raises the temperature reference when Night blind is used)

- Up to 10 general DI inputs for signals from other automatic controls serving to activate the controller’s alarm function

###### **On/off-output**

###### Relay outputs

- Defrost (one each section)

###### Pressure transmitters

- P0 For registration of the evaporating pressure (control of AKV valve).

- Pc For registration of the condensing pressure. Can be used in connection with adaptive defrost, or the signal can be received via data communication.

- Paux 1-3, extra  transmitters, which can be used for general pressostats or monitoring.

- A pressure transmitter type AKS 32R can supply signals to five controllers

###### Voltage signal

Ext. Ref. is used if the thermostat reference is to be displaced with a signal from another control.

- General 0-10 V inputs. Up to 5 inputs, which can be used for monitoring and alarm function.

###### **On/Off-inputs**

Contact function (on an analog input) or voltage signal (on an extension module)

- Rail heat

- Fan motor

- Light

- Compressor (demand on cooling)

- Alarm relay

- Solenoid valve (EVR)

- Drain valve, Suction line valve

- Night blind

- Drip tray heat recovery

- General functions

###### AKV Solid state outputs

The solid state outputs on the controller module are primarily used for AKV valves, but may also be used for the functions mentioned under ”relay outputs”.

(The output will always be “OFF” when the controller is hit by power failure).

###### **Analog output**

- 0-10 V signal for valve regulation or fan with EC motor

- Stepper signal to ETS/CCMT valve

###### **Example**

- Freezing appliance with three sections

- AKV is used for injections (S2 and P0)

- Electric defrost with stop based on temperature (S5)

- Two thermostat sensors per section (S3 and S4)

- Control of fans and rail heat

- External start/stop (Main switch)

- Switch signal for appliance cleaning

- 3 display for monitoring of appliance temperature

###### **Data from this example is used in the planning table on the next page.**

###### **The result is that the following modules should be used:**

- AK-CC 750A controller

- AK-XM 101A

- 3 pcs. EKA 163B

If the result had demonstrated that an additional output was needed, AK-XM 205A or B would have been the required exten- sion.

34

|**4**<br>**Planning table**|||||**7**|
|---|---|---|---|---|---|
|The table helps you establish whether there are enough inputs<br>and outputs on the basic controller.<br>If there are not enough of them, the controllers must be<br>extended by one or more of the mentioned extension<br>modules.<br>Note down the connections you will require and add them<br>up|**Analog input signal**<br>Example|**On/off voltage signal**<br>Example|**On/off voltage signal**<br>Example|**On/Off output signal**<br>Example|**Analog output 0-10 V**<br>**Stepper output**<br>Example<br>**Limitations**|
|**Analog inputs**<br>Temperature sensors S2 S3 S4 S5|12|||||
|, , , ,<br>Extra temperature sensor / Separate thermostats|0|||||
|Pressure transmitter , P0, Pc, Separatepressostats|1||||P = Max.**5**/ module|
|Voltage signal from an other regualtion, separate signals||||||
|Displacement of  reference with analogsignal||||||
|**On/off inputs**|Kontakt|24 V|230 V|||
|External start/stop(Main switch)|1|||||
|Case cleaning(pulsepressure). Shutdown<br>|1|||||
|Switch between two temperature references||||||
|Inject ON<br>Start of defrost (pulsepressure)||||||
|Door contact||||||
|Night setback||||||
|General DI alarm inputs (1-10)||||||
|Open/ close Night blind (pulsepressure)|||||=> OK|
|**On/off outputs**<br>|||||eded|
|AKV valves||||3|ce|
|Solenoid valves in liquid line<br>|||||e ex|
|Fans<br>Defrost (electric or hotgas valves)||||1<br>3|ions ar|
|Drain valve, suction line valve|||||at|
|Rail heat||||1|imit|
|Light<br>Night blind|||||mple:<br>the 3 l|
|Driptrayheat<br>|||||exa<br>e of|
|Compressor<br>Alarm|||||The<br>Non|
|General: Thermostat1-5, Pressostat 1-5, Voltage.1-5||||||
|**Analog control signal, 0-10 V**<br>||||||
|External valve regulation / EC motor||||||
|**Valves with stepmotor**||||||
|**Sum of connections for the regulation**|15|||8|Sum = max.**80**|
|Number of connections on a controller module|11<br>11|0<br>0|0<br>0|8<br>8|0<br>0<br>0|
|**5**<br>**Missing connections, if applicable**|4|||-||
|**6**<br>**The missing connections to be updated from one or more extension m**|**odules:**||||Sum ofpower|
|AK-XM 101A**(8 analog inputs)**|1||||pcs. á 2 VA =|
|<br>AK-XM 102A**(8 digital low voltage inputs)**|||||_____<br>___pcs. á 2 VA = __|
|AK-XM 102B**(8 digital high voltage inputs)**|||||___pcs. á 2 VA = __|
|AK-XM 103A**(4 analog inputs,  4 analog outputs)**|||||___pcs. á 2 VA = __|
|AK-XM 204A / B**(8 relay outputs)**|||||___pcs. á 2 VA = __|
|AK-XM 205A / B**(8 analog inputs + 8 relay outputs)**|||||___pcs. á 5 VA = __|
|AK-XM 208C**(8 analog inputs + 4 stepper  outputs)**|||||___pcs. á 5 VA = __|
|AK-OB 110**(2 analog outputs)**|||||pcs. á 0 VA =  0|
||||||___ <br>1 pcs. á 8 VA = 8<br>Sum =<br>Sum = max.**32**VA|

35

##### **8**

##### **Length**

##### **9**

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

##### **Linking of modules**

Start with the controller module and then mount the selected extension modules. The sequence is of no importance.

However, you must **not** change the sequence, i.e. rearrange the modules, after you have made the setup where the controller is told which connections are found on which modules and on which terminals.

Example continued: Controller module + 1 extension module in 100-series = 224 + 72 = 296 mm.

The modules are attached to one another and kept together by a connection which at the same time transmits the supply voltage and the internal data communication to the next module.

Mounting and removal must always be performed when there is no voltage.

The protective cap mounted on the controller’s plug connection must be moved to the last vacant plug connection so that the plug will be protected against short-circuit and dirt.

When the regulation has started the controller will all the time check whether there is connection to the connected modules. This status can be followed by the light-emitting diode.

When the two catches for the DIN rail mounting are in open position the module can be pushed into place on the DIN rail – no matter where in the row the module is found. Removal is likewise carried out with the two catches in the open position.

36

##### **10**

##### **Determine the connection points**

All connections must be programmed with module and point, so in principle it does not matter where the connections are made, as long as it takes place on a correct type of input or output.

• The controller is the first module, the next one is 2, etc.

• A point is the two or three terminals belonging to an input or output (e.g. two terminals for a sensor and three terminals for a relay).

The preparation of the connection diagram and the subsequent programming (configuration) should take place at the present time. It is most easily accomplished by filling in the connection survey for the relevant modules.

Principle:

|**Name**|**On module**|**On Point**|**Function**|
|---|---|---|---|
|fx Compressor 1|x|x|ON|
|fx Compressor 2|x|x|ON|
|fx Alarm relay|x|x|OFF|
|fx Main switch|x|x|Close|
|fx P0|x|x|AKS 32R 1-6 bar|

The connection survey from the controller and any extension modules are uploaded from the paragraph "Module survey. E.g. controller module:

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|||**1**(AI 1)|**1 - 2**||
|||**2**(AI 2)|**3 - 4**||
|||**3**(AI 3)|**5 - 6**||
|||**4**(AI 4)|**7 - 8**||

*[Figurtekst: Module  Point · Mind the numbering. · The right-hand part of the · controller module may look like · a separate module. But it  isn’t.]*

###### Tip

The Appendix shows 80 general installation types. If your plant closely resembles one of those shown, you can use the connection points indicated for it.

- Columns 1, 2, 3 and 5 are used for the programming.

- Columns 2 and 4 are used for the connection diagram.

###### Example continued:

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Air temperature - S3A||**1**(AI 1)|**1 - 2**|Pt 1000|
|Air temperature- S3B||**2**(AI 2)|**3 - 4**|Pt 1000|
|Air temperature- S3C||**3**(AI 3)|**5 - 6**|Pt 1000|
|Air temperature - S4A||**4**(AI 4)|**7 - 8**|Pt 1000|
|Air temperature - S4B||**5**(AI 5)|**9 - 10**|Pt 1000|
|Air temperature - S4C||**6**(AI 6)|**11 - 12**|Pt 1000|
|Defrost sensor - S5A||**7**(AI 7)|**13 - 14**|Pt 1000|
|Defrost sensor - S5B||**8**(AI 8)|**19 - 20**|Pt 1000|
|Defrost sensor - S5C||**9**(AI 9)|**21 - 22**|Pt 1000|
|Gas temperature - S2A||**10**(AI 10)|**23 - 24**|Pt 1000|
|Evaporator pressure - P0|**1**|**11**(AI 11)|**25 - 26**|AKS32R-12|
|AKV A||**12**(DO 1)|**31 - 32**|-|
|AKV B||**13**(DO 2)|**33 - 34**|-|
|AKV C||**14**(DO 3)|**35 - 36**|-|
|Fans||**15**(DO 4)|**37 - 38**|ON|
|Defrost A||**16**(DO 5)|**39-40-41**|ON|
|Defrost B||**17**(DO6)|**42-43-44**|ON|
|Defrost C||**18**(DO7)|**45-46-47**|ON|
|Rail heat||**19**(DO8)|**48-49-50**|ON|
|||**24**|**-**||
|||**25**|**-**||

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Gas temperature - S2B||**1**(AI 1)|**1 - 2**|Pt 1000|
|Gas temperature - S2C||**2**(AI 2)|**3 - 4**|Pt 1000|
|External Start/stop||**3**(AI 3)|**5 - 6**|Closed|
|Case cleaning (pulse pressure)||**4**(AI 4)|**7 - 8**|Closed|
||**2**|**5**(AI 5)|**17 - 18**||
|||**6**(AI 6)|**19 - 20**||
|||**7**(AI 7)|**21 - 22**||
|||**8**(AI 8)|**23 - 24**||

37

##### **11**

##### **Connection diagram**

Drawings of the individual modules may be ordered from Danfoss. Format = dwg and dxf.

You may then yourself write the module number in the circle and draw the individual connections.

Example continued:

*[Figurtekst: 1 3 5 7 8 10 1 3 · 2 4 6 9 11 2 4 · 1 2 · 12 14 16 18 · 13 15 17 19 · S3A S3C S4B  S5A  S5B S2A  S2B Start/stop · S3B  S4A S4C S5C P0  S2C Case cleaning · 3 x EKA 163B · AKV  A  AKV  C Def. A Def.. C · AKV  B  Fans Def.. B   Rail heat]*

38

##### **12**

Supply voltage is only connected to the controller module. The supply to the other modules is transmitted via the plug between the modules. The supply must be 24 V +/-20%. One transformer must be used for each controller. The transformer must be a  class II. The 24 V must not be shared by other controllers or units. The analog inputs and outputs are not galvanically separated from the supply.

###### **Transformer size**

|The power consum|ption grows|with the nu|mber o|f modules used:|
|---|---|---|---|---|
|**Module**|**Type**|**Number**|**á**|**Effect**|
|Controller||1<br>x|8 =|8 VA|
|Extension module|200-series|_<br>x|5 =|__ VA|
|Extension module|100-series|_<br>x|2 =|__ VA|
|Total||||___ VA|

The + and – 24V input must **not** be earthed.

If using stepper motor valves, the supply for these must be provided from a separate power supply. See AK-XM 208C.

It will also be necessary to safeguard the voltage to the controller and valves using UPS.

###### **Common pressure transmitter**

If several controllers receive a signal from the same pressure transmitter, the supply to the affected controllers must be wired so that it is not possible to switch off one of the controllers without also switching off the others. (If one controller is switched off, the signal will be pulled down, and all the other controllers will receive a signal which is too low)

Example continued:

Controller module 8 VA + 1 extension module in 100-series 2 VA -----Transformer size (least) 10 VA

39

#### **Ordering**

###### 1. Controller

|**Type**|**Function**|**Application**|**Language**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|---|
|AK-CC 750A|Controller for evaporator control|1, 2, 3 or 4 sections|English, German, French,<br>Dutch, Italian, Spanish, Portu-<br>guese, Danish, Finnish, Polish,<br>Russian,Czech|**080Z0140**|**X**|

|2. Extension m<br>|odules and sur<br>|veyfor inp<br>**f**|uts and outpu<br>**f**|ts<br>**f**|**f**||||||
|---|---|---|---|---|---|---|---|---|---|---|
|**Type**|**Analog**<br>**inputs**|**On/Off ou**|**f tputs**|**On/off supp**<br>**(DI signal)**|**f ly voltage**|**Analog**<br>**outputs**|**Stepper**<br>**outputs**|**Module**<br>**with**<br>**switches**|**Code no.**|**Example**<br>**continued**|
||For sensors,<br>pressure<br>transmitters<br>etc.|Relay<br>(SPDT)|Solid state|Low volt-<br>age<br>(max. 80 V)|High volt-<br>age<br>(max. 260<br>V)|0-10 V d.c.|For valves<br>with step<br>control|For override<br>of relay<br>outputs|With screw<br>terminals||
|Controller|11|4|4|-|-|-||-|-||
|Extension mo|dules||||||||||
|AK-XM 101A|8||||||||**080Z0007**|**x**|
|AK-XM 102A||||8|||||**080Z0008**||
|AK-XM 102B|||||8||||**080Z0013**||
|AK-XM 103A|4|||||4|||**080Z0032**||
|AK-XM 204A||8|||||||**080Z0011**||
|AK-XM 204B||8||||||x|**080Z0018**||
|AK-XM 205A|8|8|||||||**080Z0010**||
|AK-XM 205B|8|8||||||x|**080Z0017**||
|AK-XM 208C|8||||||4||**080Z0023**||
|<br>The following<br>There is onlyr|extension modu<br>oom for one mo|le can be pl<br>dule.|aced on the PC|board in the c|ontroller mod|ule.|||||
|AK-OB 110||||||2|||**080Z0251**||

###### 3. AK o p eration and accessories

|**Type**|**Function**|**Application**|**Code no.**|**Example**<br>**continued**|
|---|---|---|---|---|
|**Operation**|||||
|AK-ST 500|Software for operation of AK controllers|AK-operation|**080Z0161**|**x**|
|-|Cable between PC and AK controller|USB A - USB B (standard IT cable)|**-**|**x**|
|**Accessories**|**Power supply module 230 V / 115 V to 24 V**||||
|AK-PS 075|18 VA|Sl f ll|**080Z0053**|**x**|
|AK-PS 150|36 VA|uppy or controer|**080Z0054**||
|**Accessories**|**External display that can be connected to the cont**|**roller module. For showing, say, the appliance temp**|**erature**||
|EKA 163B|Display||**084B8574**|**xxx**|
|EKA 164B|Display with operation buttons||**084B8575**||
|MMIGRS2|Graphic display with operation||**080G0294**||
||Cbl bt EKA dil d tll|Length = 2 m|**084B7298**|**xxx**|
|-|ae eween  spay an conroer|Length = 6 m|**084B7299**||
||Cable between graphic display type MMIGRS2 and|Length = 1.5 m|**080G0075**||
|-|controller (controller with RJ11 plug)|Length  = 3 m|**080G0076**||
|**Accessories**|**Communication modules for controllers where mo**|**dules cannot be connected continuously**|||
|AK-CM 102|Communication module|Data communication for external extension mod-<br>ules|**080Z0064**||


### **3. Mounting and wiring**

This section describes how the controller:

- Is fitted

- Is connected

We have decided to work on the basis of the example we went through previously, i.e. the following modules:

- AK-CC 750A controller module

- AK-XM 101A analog output module

- 3 pcs. EKA 163B display

41

#### **Mounting**

##### **Mounting of extension module on the basic module**

1. Move the protective cap

Remove the protective cap from the connection plug on the right-hand side of the basic module.

Place the cap on the connection plug to the right of the extension module that is to be mounted on the extreme right-hand side of the AK assembly.

2. Assemble the extension module and the basic module

The basic module must not be connected to voltage.

In our example one extension module is to be fitted to the basic module. The sequence is thus:

All the subsequent settings that affect the two extension modules are determined by this sequence.

When the two snap catches for the DIN rail mounting are in the open position, the module can be pushed into place on the DIN rail – regardless of where the module is on the row. Disassembly is thus done with the two snap catches in the open position.

42

M ou n t in g a n d wirin g - co n t in ued

#### **Wiring**

Decide during planning which function is to be connected and where this will be.

###### 1. Connect inputs and outputs

Here are the tables for the example:

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Air temperature - S3A||**1**(AI 1)|**1 - 2**|Pt 1000|
|Air temperature- S3B||**2**(AI 2)|**3 - 4**|Pt 1000|
|Air temperature- S3C||**3**(AI 3)|**5 - 6**|Pt 1000|
|Air temperature - S4A||**4**(AI 4)|**7 - 8**|Pt 1000|
|Air temperature - S4B||**5**(AI 5)|**9 - 10**|Pt 1000|
|Air temperature - S4C||**6**(AI 6)|**11 - 12**|Pt 1000|
|Defrost sensor - S5A||**7**(AI 7)|**13 - 14**|Pt 1000|
|Defrost sensor - S5B||**8**(AI 8)|**19 - 20**|Pt 1000|
|Defrost sensor - S5C||**9**(AI 9)|**21 - 22**|Pt 1000|
|Gas temperature - S2A||**10**(AI 10)|**23 - 24**|Pt 1000|
|Evaporator pressure - P0|**1**|**11**(AI 11)|**25 - 26**|AKS32R-12|
|AKV A||**12**(DO 1)|**31 - 32**|-|
|AKV B||**13**(DO 2)|**33 - 34**|-|
|AKV C||**14**(DO 3)|**35 - 36**|-|
|Fans||**15**(DO 4)|**37 - 38**|ON|
|Defrost A||**16**(DO 5)|**39-40-41**|ON|
|Defrost B||**17**(DO6)|**42-43-44**|ON|
|Defrost C||**18**(DO7)|**45-46-47**|ON|
|Rail heat||**19**(DO8)|**48-49-50**|ON|
|||**24**|**-**||
|||**25**|**-**||

The function of the switch functions can be seen in the last column.

|**Signal**|**Module**|**Point**|**Terminal**|**Signal type /**<br>**Active at**|
|---|---|---|---|---|
|Gas temperature - S2B||**1**(AI 1)|**1 - 2**|Pt 1000|
|Gas temperature - S2C||**2**(AI 2)|**3 - 4**|Pt 1000|
|External Start/stop||**3**(AI 3)|**5 - 6**|Closed|
|Case cleaning (pulse pressure)||**4**(AI 4)|**7 - 8**|Closed|
||**2**|**5**(AI 5)|**17 - 18**||
|||**6**(AI 6)|**19 - 20**||
|||**7**(AI 7)|**21 - 22**||
|||**8**(AI 8)|**23 - 24**||

43

Mountin g and wirin g - continued

*[Figurtekst: The connections for the example can be seen here. · The screen on the pressure transmitter · Warning cables must only be connected at the · Keep signal cables separate from  end of the controller. · cables with high voltage. · Case cleanng]*

The connections for the example can be seen here.

###### 2. Connect LON communication network

The installation of the data communication must comply with the requirements set out in document RC8AC.

3. Connect supply voltage

Is 24 V, and the supply must not be used by other controllers or devices. The terminals must not be earthed.

4. Follow light-emitting diodes

When the supply voltage is connected the controller will go through an internal check. The controller will be ready in just under one minute when the light-emitting diode ”Status” starts flashing slowly.

###### 5. When there is a network

Set the address and activate the Service Pin. When the controller is set correct on the network the LED "status" will flash quickly for 10 minutes.

6. The controller is now ready to be configured.

*[Figurtekst: Internal communication · between the modules: · Quick flash = error · Constantly On = error Slow flash = OK · Quick flash = answer from gateway · in 10 min. after network · ■ Power                   installation · ■ Comm Constantly ON = error · ■ DO1  ■ Status Constantly OFF = error · ■ DO2  ■ Service Tool · External communication · ■ DO3  ■ LON · ■ DO4  ■ I/O Extension · ■ DO5  ■ Alarm Flash = active alarm/not acknowledged · ■ DO6 Constant ON = Active alarm/acknowledged · ■ DO7  ■ Display · ■ DO8  ■ Service Pin · Network installation · Status on output 1-8]*

44

### **4. Configuration and operation**

This section describes how the controller:

- Is configured

- Is operated

We have decided to work on the basis of the example we went through previously, i.e. a frost appliance with 3 evaporators. The example is shown overleaf.

45

##### **Refrigerating plant example**

We have decided to describe the setup by means of an example comprising a freezing appliance with 3 evaporators. The example is the same as the one given in the "Design" section, i.e. the controller is an  AK-CC 750A + extension modules.

###### **Freezing appliance**

- Refrigerant R134a

- 3 evaporators

- Electric defrost on each section

- Fans

- Rail heat

- 3 displays for monitoring of temperature in the sections

###### **Refrigeration:**

- 3 AKV valves

- Superheat measured with P0 and 3 S2-sensors

- S3 is alarm sensor

- S4 is thermostat sensor

- Night setback on 3K

###### **Defrost:**

- The defrost is stopped individually based on temperature (S5)

- Refrigeration starts when both defrosts have been accomplished

###### **Fans:**

- Operates during defrost

###### **Cleaning:**

- Pulse pressure for start and later stop of cleaning

###### **Other:**

There is also an internal main switch as a setting. Both must be “ON” before any adjustment is made.

- External start/stop used (Main switch)

The modules used are selected in the design phase.

###### **For the example shown we use the following modules:**

- AK-CC 750A controller

- AK-XM 101A analog output module

46

#### **Configuration**

##### **Connect PC**

PC with the program “Service Tool” is connected to the controller.

The controller must be switched on first and the LED “Status” must flash before the Service Tool programme is started.

For connecting and operating the "AK service tool" software, please see the manual for the software.

The first time the Service Tool is connected to a new version of a controller the start-up of the Service Tool will take longer than usual while information is retrieved from the controller.

Time can be followed on the bar at the bottom of the display.

###### Start Service Tool programme

###### Login with user name SUPV

When the controller is supplied the SUPV access code is 123. When you are logged into the controller an overview of it will always appear.

Select the name **SUPV** and key in the access code.

*[Figurtekst: (In case the overview is empty. This is because the controller has not yet · been set up.)]*

The red alarm bell at the bottom right tells you that there is an active alarm in the controller. In our case the alarm is due to the fact that the time in the controller has not yet been set.

47

##### **Authorization**

Press the orange setup button with the spanner at the bottom of the display.

2. Select Authorization

*[Figurtekst: 3. Change setting for the user ‘SUPV‘]*

4. Select user name and access code

When the controller is supplied it has been set with standard authorization for different user interfaces. This setting should be changed and adapted to the plant. The changes can be made now or later.

You will use this button again and again whenever you want to get to this display. On the left-hand side are all the functions not shown yet. There will be more here the further into the setup we go.

*[Figurtekst: Press the line  Authorization  to get to the user setup display.]*

*[Figurtekst: Mark the line with the user name  SUPV . · Press the button  Change · This is where you can select the supervisor for the specific system and a · corresponding access code for this person. · The controller will utilize the same language that is selected in the · service tool but only if the controller contains this language. If the · language is not contained in the controller, the settings and readings · will be shown in English.]*

5. Carry out a new login with the user name and the new access code

*[Figurtekst: To activate the new settings you must carry out a new login to the con- · troller with the new user name and the relevant access code. · You will access the login display by pressing the icon at the top left · corner of the display.]*

48

##### **Unlock the configuration of the controllers**

###### 2. Select Lock/Unlock configuration

The controller can only be configured when it is unlocked. It can only be adjusted when it is locked.

Changes to the input and output settings are only enabled when the controller is “Locked”

The values can be changed when it is locked, but only for those settings that do not affect the configuration.

If you want to know more about the different configuration options, they are listed below. The number refers to the number and picture in the column on the left.

###### **3Main Switch**

Used to start and stop regulation. When the main switch is set to Off, all outputs are in standby mode and all alarms are cancelled.

The main switch must be set to Off before the Configuration lock can be Unlocked.

###### **Configuration lock**

The controller can only be fully configured when the configuration lock is set to Unlocked.

The settings are only applied when it is set to Locked again. At this point, the controller checks the functions set and compares them with the input and output settings. Important settings can then no longer be changed unless the configuration is unlocked again.

###### 3. Select Configuration lock

- Press the blue field with the text **Locked**

###### 4. Select Unlocked

*[Figurtekst: Select  Unlocked  and press  OK.]*

**In general Many settings are dependent on previous settings. This is shown by the fact that a function can only be seen (and thus set) if an earlier parent function allows access to this subordinate function**

For example, the “Configuration lock” line will not be shown if the main switch is set to On. Only when the main switch is set to Off, and regulation has therefore been stopped, is it possible to set the configuration lock.

49

Conf i guration - continued

##### **System setup**

2. Select System setup

###### 3. Set system settings

###### **General**

All system settings can be changed by pressing in the blue field with the setting and then indicating the value of the required setting.

**3-**

**Controller name**

In the first field you enter a name for what the controller will be controlling.

###### **Main frequency**

Set frequency.

###### **Alarm language**

Select the language that alarm text should be displayed in here. Alarm text can be in a different language to the operating language.

###### **Clock**

When the time is set the PC’s time can be transferred to the controller. When the controller is connected to a network, date and time will automatically be set by the system unit in the network. This also applies to change-over Daylight saving. Power failure, the clock will be kept running for at least 12 hours.

50

Conf i guration - continued

##### **Set plant type**

###### 2. Select plant type

Press the line **Select plant type** .

###### 3. Set plant type

###### 4. Other settings

After the selection of application we will go through the other setup displays to check whether changes will have to be made on some of the predefined settings.

In our example we have to select a refrigerant, (which is done on the screen shown above) and we must add external start/stop settings (which is done in the subsequent “Common functions” screen).

When the installation type is to be configured, it can be done in two ways: Either one of these two

In the example, we have decided to use the second method. Here we select:

- 3 evaporators

- AKV valve

- Refrigerant = R134a

- Defrost

- Defrost = electric

###### **3-**

###### **Select pre-configured application Group 1**

Or group 2

This setting give a choice between a number of predefined combinations, which at the same time determine the connection points.

At the end of the manual there is an overview of the options and connection points.

After configuration of this function, the controller will shut down and restart. After the restart, a large number of settings will have been made. These include the connection points. Continue with the settings and check the values.

If you change some of the settings, the new values will come into force.

###### **Number of evaporators**

- **Check the settings opposite the individual functions**

Select the number of evaporators that you want the controller to regulate.

###### **Valve type**

Select the relevant type of valve here. AKV valve LLSV, solenoid valve (at thermostatic expansion valve).' STEP (ETS / CCM / CCMT valve)

AO (analog voltage)

###### **Scaling factor for step valve and AO**

The valve capacity can be minimized here. LLSV, Solenoid valve (at stepper valve) LLSV delay off

Delay time after stepper begins to close until solenoid valve closes.

###### **Refrigerant**

Here you can select from a range of pre-defined refrigerants. If you cannot find the refrigerant you want in the list, select “User-defined”. You can then set 3 constants which represent the refrigerant. You can obtain these 3 constants from Danfoss.

###### **Defrost control**

Select whether you want the evaporators to regulate with defrost.

###### **Defrost type**

You can select either natural defrost or electrical defrost, hot g as defrost or warm brine defrost.

51

##### **Definition of thermostat**

2. Select Common control

###### 3. Select functions for thermostat

**Depending on your settings, further settings may then be available for the selected functions. This list in the right-hand column contains all the possible functions that may be made available in one way or another.**

**If you want to know more about the individual functions than the brief description below, you will find additional information in Chapter 5 of the manual.**

The setup menu has now changed. It now shows more settings all of which are based on the selected plant type. For example, earlier we selected 3 evaporators. This means that 3 sections are now displayed.

###### **3 -**

###### **Thermostat type**

Choose from the following thermostat functions:

- 1 valve for all /common ON-OFF thermostat Here, only one valve is used for all evaporators. The temperature is controlled by an ON/OFF thermostat on the basis of the settings in the A section.

- 1 valve per evap/ common ON/OFF thermostat Here, one valve per evaporator is used. The temperature is controlled in all evaporator sections by an ON/OFF thermostat on the basis of the settings in the A section.

- 1 valve per evaporator / individual ON/OFF thermostat Here, one valve per evaporator is used. The temperature is controlled individual by ON/OFF in each evaporator section.

- 1 valve per evaporator /individual modulating thermostat Here, one valve per evaporator is used. The temperature is controlled individually in each evaporator section according to a modulating principle

In our example we select:

###### **External reference via voltage**

- On/off thermostat

• Individual thermostat on each Select whether to use an external voltage signal for dissection placement of the thermostat reference. • Night setback **Offset at max. signal** • No melt function, as this is a frost Offset value at max. signal (5 or 10V). appliance **Offset at min. signal** Offset value at min. signal (0,1 or 2V).

**Day/ night control**

- The settings are shown here in the display.

Select whether the thermostat temperature is raised for night operation (Night offset values must be set in the individual sections and in Kelvin)

###### **Night displacement via DI**

Select whether night displacement is to take place with an input signal. (Alternatively, the signal can be generated from the internal weekly schedule or from the system administrator via data communication.)

###### **Thermostat band**

Select whether you want the thermostat to switch between two reference settings (the values can be set in the individual sections)

Select whether the switch should be initialised by pulse pressure or by a switch.

###### **Thermostat band select via DI**

Select whether the reference is to be made with a signal on a DI input.

###### **Melt function**

Select whether you want the controller to perform a melting function

###### **Melt interval**

Set the time period between two melting intervals

**Melt time**

Set the melting time

**Flood Evap**

Choose from the following functions:

- Disconnected. Liquid flow is not permitted

- Liquid flow SH only. Stopped by a signal from the system device.

- Liquid flow Common DI. Stopped by a common DI signal

52

###### **3 -**

##### **Definition of sections**

2. Select Section A

3. Set values for thermostat A

4. Set values for alarm thermostat

5. Define the other sections

There are several pages, one after the other. The black bar in this field tells you which of the pages is currently displayed.

Move between the pages using the + and - buttons.

Repeat the steps above for each section.

In our example, the settings are the same for all 3 sections.

###### **Stepper valve**

ETS 12½, 25, 50, 100, 250, 400, CCM, CCMT or User selection. At User selection: + Max operating steps, Hysterese, Step rate, Holding current, Overdrive init, Phase current, Soft landing unit, Failsafe pos.

###### **Thermostat temperature**

In the case of a common thermostat: Choose which sensors are to be included in temperature regulation: Weighted S3A-S4A, lowest of all S3s, average of all S3s, highest of all S3s, lowest of all S4s, average of all S4s or highest of all S4s.

###### **Air temperature S4 Day**

Sensor selection for the thermostat during day operation At 100%, only S4 is used. At a lower value, S3 is also used in the thermostat function. At 0%, only S3 is used in the thermostat function.

###### **Air temperature S4 Night**

As above, but for night operation

###### **Cutout 1**

The thermostat’s cutout temperature - Thermostat band 1 **Differential 1**

Differential on regulation according to Thermostat band 1 **Cutout 2**

The thermostat’s cutout temperature - Thermostat band 2 **Differential 2**

Differential on regulation according to Thermostat band 2 **Night setback** Displacement of the reference during night operation **Display  control**

Select whether you want to connect to display type EKA 163B / EKA 164B to indicate the appliance temperature for section A. Settings are: non, weighted S3/S4 or product temperature sensor.

###### **Display unit**

Select whether you want temperatures and pressure displayed in SI units (°C) or US units (°F)

###### **Display S4 %**

Sensor selection for the temperature shown on the display At 100%, only S4 is used. At a lower value, S3 is also used. At 0%, only S3 is displayed.

###### **Display Offset**

Any offset for the display readout

**Max. Disp -d- delay**

Max. duration of -d- in display.

###### **S4 Frost protection**

Select whether an alarm is triggered in the case of low S4 temperature

###### **S4 Frost limit**

Set the alarm level for the S4 sensor.

**4-**

###### **Alarm thermostat**

Select whether you want to activate the alarm thermostat **Alarm air S4%** Set the weighting of the S4 sensor for the alarm thermostat **High alarm limit 1** Alarm limit for high temperature alarm, thermostat band 1 **High alarm limit 2** Alarm limit for high temperature alarm, thermostat band 2

**High delay** Time delay for a high temperature alarm

**High delay pulldown** Time delay during pull-down and after defrost **Low alarm limit 1** Alarm limit for a low temperature alarm, thermostat band 1 **Low alarm limit 2** Alarm limit for a low temperature alarm, thermostat band 2 **Low delay** Time delay for a low temperature alarm

**Product sensor**

Indicate whether a product sensor is used **High alarm limit 1** Alarm limit for high product temperature, thermostat band 1 **High alarm limit 2** Alarm limit for high product temperature, thermostat band 2 **High delay**

Time delay for a high product temperature alarm

**High delay pulldown** Time delay during pull-down and after defrost **Low alarm limit 1**

Alarm limit for a low product temperature, band 1 **Low alarm limit 2** Alarm limit for a low product temperature, band 2

**Low delay**

Time dela y for a low p roduct tem p erature alarm

53

##### **Definition of defrost functions**

###### Note!

If the injection is controlled with a analog signal to a 3rd party valve the setting "Adaptive defrost" is not recommended.

###### 2. Select Defrost function

###### **3 -**

###### **Defrost control**

Select whether you want the controller to control defrost. **Defrost type**

Choose a defrost method (electric / natural / hot gas or warm brine)

###### **Adaptive defrost**

The function can be set to: "Not used"/"Monitor ice"/"Permit cancellation of defrost for day (Skip day)"/"Skip day/ night"/"Full adaptive defrost".

**Min. time between defrosts**

Set how often defrosting is allowed.

###### **Pc signal for AD (Adaptive defrost)**

Choose which signal is to be followed: an internal signal (Local) or a signal via data communications (Network).

**Defrost schedule**

Choose which schedule is to be followed: an internal schedule or an external schedule from the system unit

###### 3. Set functions

If the controller’s internal defrost schedule is used to start defrost, the start times must be set using the everyday user interface. See page 65.

###### **Defrost start via DI**

Select whether defrost should start when a signal is received

on a DI input

###### **Max. defrost interval between defrosts**

Defrost is started at the set interval if it is not started using other methods (manual start, weekly schedule, network, DI). If defrost is started using a schedule, “Max. interval” should be set to a value greater than the longest period between two defrosts in the schedule.

**Fan run during defrost** Specify whether the fans should be on during defrost. **Defrost stop method**

Define whether defrost is to be concluded with:

• Time, Temperature individual in each section or  Temperature common for all sections

###### **Defrost term sensor**

Select the sensor that you want to give the signal for defrost stop

###### **Stop temperature A, B, C, D**

Set the temperature at which defrost should stop

**Max. defrost time** Defrost will stop after this period, even if the defrost temperature has not been reached

**Min. defrost time** Defrosting **cannot** be stopped until the set time has expired. The setting has higher priority than  "Max. defrost time"

**Pump down delay**

Time delay before defrost when the fluid injection stops and the evaporator is emptied of liquid

**Hot gas delay**

Delay time before opening of hot gas valve

**Drip off delay**

Time delay after defrost to allow water droplets to drip off the evaporator before refrigeration is restarted

**Drain delay**

Delay in which the drain valve is kept open in order to ensure pressure equalisation

**Fan delay**

Maximum permitted fan delay following defrost

**Fan start temperature**

The fans will start when the temperature at the defrost sensor falls below this value.

**Drip tray heater** Set whether there is to be heating in the drip tray **Drip tray heater delay** Set heating time (time from the point at which defrost stops ) **Max. Hold time**

Maximum hold time that the controller will wait for the signal to restart refrigeration (used with coordinated defrost) **Show advanced adaptive defrost**

All settin g s for this function are ex p ert settin g s.

54

##### **Definition of common functions**

###### 3-

Common functions for fans and rail heat

###### **Fan control**

Select required fan control:

   - Single fan (one relay)

2. Select Common functions

- two speed fan (two relais)

- EC fan (analogue voltage output)

- VSD fan (analogue voltage output + one start relay) **Fan pulsing at cutout**

Select whether you want the fans to pulse during the thermostat’s cutout period. Pulsing can be restricted to either: “night operation only” (appliance with night cover) or “both day and night operation” (cold storage room) **Fan eco during thermostat cutout**

Select when the fans should run on low speed:

- Never

- Both day and night

- Night only

**Fan ON %** (at single fan)

Set how long the fans should be ON during pulsing. Enter as a percentage of the pulse period. **Fan duty cycle** (at single fan)

Set the fan’s operation period for pulsing **Fan day** (at EC or VSD)

Fan speed during normal day operation **Fan night** (at EC or VSD)

3. Set functions in the first display

4. Set the functions in another display

Fan speed during normal night operation

**Fan day eco** (at EC or VSD)

Fan speed during day operation and thermostat cutout- **Fan night eco** (at EC or VSD)

Fan speed during night operation and thermostat cutout **EC min start speed** (at EC or VSD)

Lowest speed the first 10 seconds after start

###### **Fan stop on S5**

Select whether the fans should stop if the S5A temperature is too high. Used to stop the fans if refrigeration is not working.

###### **Fan stop temp.**

Set the temperature limit for the S5A sensor at which the fans stop **Rail heat control**

Select whether to use pulsing/rail heat control. Non/Timer or Dew point. **Rail ON at day**

Set how long the rail heat should be ON for during day operation. Enter as a percentage of the rail heat pulse period **Rail heat at night** Set how long the rail heat should be ON for during night operation. Enter as a percentage of the rail heat pulse period.

**Dew point max. limit** At a dew point above this value, rail heat is 100%. **Dew point min limit**

At a dew point below this value, rail heat is controlled with the next setting "Min ON".

**Rail heat Min ON%**

Period in which the dew point is below the min. limit. **Rail heat cycle time** Rail heat pulse period.

**Rail heat during defrost** Select whether you want the rail heat to be OFF during defrost.

4-

Common functions for compressor and case cleaning **Compressor control** Select whether you want to use compressor control **Min. ON time** Set the minimum runtime for the compressor once it has started **Min. Restart time**

Set the minimum time between the compressor stopping and restarting

**Runtime total** Set any runtime for the compressor **Case cleaning** Select whether you want an case cleaning function

55

###### **Case cleaning via DI**

5. Set the functions in the third display

Select whether to use a digital input to activate the case cleaning function. Alternatively the case cleaning function can be activated from the display or using a parameter setting

###### **Defrost at case cleaning**

Select whether to activate the case cleaning function with a defrost sequence. Used for frost appliances to achieve fast defrost of the appliance before cleaning.

###### **Appliance shutdown**

Select function for light and fans when appliance shut down 5-

Common functions for door, light etc.

###### **Door switch mode**

Select the function of any door switch. The door switch can be used in one of the following two ways:

- Alarm only, if the door has been left open for too long

- Stop refrigeration and fans when the door is open, along with an alarm if the door has been left open for too long

###### **Light off delay**

Set how long the light should remain on after the door has been closed (requires a light control to be set up and controlled via the door switch)

###### **Restart refrig. delay**

Set how long the door may be open before refrigeration and fans are restarted. Prevents exposure of the products to too high a temperature if someone forgets to close the door.

###### **Door alarm delay**

If the door has been open for more than the time delay set here, a door alarm is triggered **Light control**

Select whether the light should be controlled by a door switch, a day/night signal or by a signal via data communication

###### **Light at Main SW = Off**

Choose whether the light is to be switched off when the main switch is set to off, or if the light is to follow the standard light control.

###### **Control of Blinds control**

Set whether the blinds are to be controlled by a relay.

###### **Open/close blinds via DI**

Set whether the controller is to receive a signal which activates the blinds. This must be a pulse signal.

###### **Fan stop during close night blinds**

Set the number of seconds the fans must be switched off.

###### **Refrigerant leak**

A DI input is reserved for the refrigerant alarm **Alarm delay**

Time delay before alarm is transmitted

###### **Forced closing via DI**

Select whether a digital input is used for the forced closing of injection

###### **Fan at forced closing**

Select whether or not you want the fans to operate during forced closing and whether defrosting is to be permitted during this period.

###### **Alarm relay**

Select the alarm relay function.

The alarm relay must be activated by alarm priorities:

- low to high

- low to medium

- high

The alarm relay can be activated either by all alarm priorities from low to high or only by high priority alarms

###### **Ext. main switch**

Select whether you want a main switch via a digital input. When the main switch is set to Off, all regulation is stopped, all outputs are set to standby and all alarms are cancelled.

56

Co nfi gu r at i o n - co n t in ued

##### **Setup general alarm inputs**

2. Select General alarm inputs

###### 3. Define the required alarm functions

In our example we are not using this function so the image is more for information purposes. The name of the function can be xx and the alarm text can be entered further down the screen).

**3 - General alarm input** This function can be used to monitor all kinds of digital signals.

**No. of inputs** Set the number of digital alarm inputs **Adjust for each input**

- **Delay time for DI alarm**

- **Alarm text**

57

Co nfi gu r at i o n - co n t in ued

##### **Setup separate thermostat functions**

2. Select Thermostats

3. Define the required thermostat function

In our example we are not using this function so the image is more for information purposes.

The name of the function can be xx and the alarm text can be entered further down the screen).

Via the +- button you can move to similar settings for the pressure control functions. (Not used in the example)

###### **3 - Thermostats**

The general thermostats can be used to monitor the temperature sensors that are used in the control, as well as 4 extra temperature sensors. Each thermostat has a separate outlet to control external automation.

- **No. of thermostats**

Set the number of general thermostats. (1-5) **For each thermostat adjust**

- Name

- Which of the sensors is used **Actual temp** .

- Temperature measurement on the sensor that is attached to the thermostat **Actual state** Actual status on the thermostat outlet **Cut out temp.** Cut-out value for the thermostat **Cut in temp.** Cut-in value for the thermostat **High alarm limit** High alarm limit **Alarm delay high** Time delay for high alarm

**Alarm text high** Indicate alarm text for the high alarm

**Low alarm limit** Low alarm limit

**Alarm delay low** Time delay for low alarm **Alarm text low** Indicate alarm text for low alarm

###### **3b - Pressostats**

There are equal settings for up to 5 pressostat functions

58

Co nfi gu r at i o n - co n t in ued

##### **Setup separate voltage functions**

2. Select General Voltage inputs

3. Define the required names and values attached to the signal

In our example we are not using this function so the image is more for information purposes.

The name of the function can be xx and the alarm text can be entered further down the screen).

The values ”Min. and Max. Readout” are your settings representing the lower and upper values of the voltage range.  2V and 10V, for example. (The voltage range is selected during the I/O setup).

For each voltage input defined the controller will reserve a relay output in the I/O setup. It is not necessary to define this relay if all you require is an alarm message via the data communication.

**3 - Voltage inputs** The general volt inlet can be used to monitor external voltage signals. Each volt inlet has a separate outlet to control external automatic controls.

**No. of voltage inp.** Set the number of general voltage inputs, specify 1-5: **Name**

**Actual value**

- = read-out of the measurement **Actual state**

- = read-out of outlet status **Min. readout**

State read-out values at minimum voltage signal **Max. readout** State read-out values at maximum voltage signal **Cutout** Cut-out value for outlet (scaled value) **Cutin** Cut-in value for outlet (scaled value) **Cutout delay** Time delay for cut-out **Cut in delay** Time delay for cut-in **Limit alarm high** High alarm limit **Alarm delay high** Time delay for high alarm **Alarm text high** Set alarm text for high alarm **Limit alarm low** Low alarm limit **Alarm delay low** Time delay for low alarm **Alarm text low** Indicate alarm text for low alarm

59

##### **Configuration of inputs and outputs**

###### 2. Select I/O configuration

###### 3. Configuration of Digital outputs

The following displays will depend on the earlier definitions. The displays will show which connections the earlier settings will require. The tables are the same as shown earlier.

- Digital outputs

- Digital inputs

- Analog outputs

• Analog inputs Important! An AKV function can only be set for module 1 and only for points 12, 13, 14 and 15

*[Figurtekst: Mod- · Load Output Point Active at · ule · AKV A DO1 1 12 - · AKV B DO2 1 13 - · AKV C DO3 1 14 - · Fan DO4 1 15 ON · Defrost A DO5 1 16 ON · Defrost B DO6 1 17 ON · Defrost C DO7 1 18 ON · Rail heat DO8 1 19 ON]*

We set up the controller’s digital outputs by keying in which module and point on this module each one of these has been connected to. We furthermore select for each output whether the load is to be active when the output is in pos. **ON** or **OFF** .

###### **3 - Outputs**

The possible functions are the following: AKV or solenoid valve LLSV_ (Solenoid valve) Defrost (el/hot gas) Common defrost Suction line valve Drain valve Drip tray heat Night blind Compressor Rail heat Light Fan Alarm Thermostat 1 - 5 Pressostat 1 - 5 Voltage input 1 - 5

###### 4. Setup On/off input functions

|**Function**|**Input**|**Mod-**<br>**ule**|**Point**|**Active at**|
|---|---|---|---|---|
|External start/stop|AI3|2|3|Closed|
|Case cleaning (pulse<br>pressure)|AI4|2|4|Closed|

We set up the controller’s digital input functions by keying in which module and point on this module each one of these has been connected to.

We furthermore select for each output whether the function is to be active when the output is in pos. **Closed** or **Open** .

**4 - Digital inputs** The possible functions are the following: Night displacement Door alarm Forced closing Ext. Main switch Thermostat band Defrost start Case cleaning Appliance shutdown Open / close Night blinds DI  alarm input 1-10 Refrigerant alarm (CO2)

**Analog output** (settings are not shown) The possible signals are as follow:

- 0 – 10 V

- 2 – 10 V

- 0 – 5 V

- 1 – 5V

The type of Step valve defined in earlier sectons.

60

###### 5. Configuration of Analog

###### Input signals

|**Sensor**|**Input**|**Module**|**Point**|**Type**|
|---|---|---|---|---|
|Air temperatureS3 A|AI1|1|1|Pt 1000|
|Air temperatureS3 B|AI2|1|2|Pt 1000|
|Air temperatureS3 C|AI3|1|3|Pt 1000|
|Air temperatureS4 A|AI4|1|4|Pt 1000|
|Air temperatureS4 B|AI5|1|5|Pt 1000|
|Air temperatureS4 C|AI6|1|6|Pt 1000|
|Defrost sensorS5 A|AI7|1|7|Pt 1000|
|Defrost sensorS5 B|AI8|1|8|Pt 1000|
|Defrost sensorS5 C|AI9|1|9|Pt 1000|
|Gas temperature-S2 A|AI10|1|10|Pt 1000|
|Evaporating pressure- P0|AI11|1|11|AKS32R-12|
|Gas temperature-S2 B|AI1|2|1|Pt 1000|
|Gas temperature-S2 C|AI2|2|2|Pt 1000|

We set up the analog inputs for the sensors.

**5 - Analog inputs** The possible signals are the following:

Temperature sensors: S2 Evaporating temp. (A,B,C,D) S3 Air temp. before evaporator (A,B,C,D) S4 Air temp. after evaporator (A,B,C,D) S5-1 Defrost sensor (A,B,C,D) S5-2 Defrost sensor (A,B,C,D) Saux 1 - 4 Product temperature (A,B,C,D) Setting: • Pt1000

- PTC 1000

Pressure transmitters: P0 evaporator pressure Pc Cond. pressure Paux 1 - 3 Setting:

- AKS 32, -1 – 6 Bar

- AKS 32R, -1 – 6 Bar

- AKS 32, - 1 – 9 Bar

- AKS 32R, -1 – 9 Bar3

- AKS 32, - 1 – 12 Bar

- AKS 32R, -1 – 12 Bar

- AKS 32, - 1 – 20 Bar

- AKS 32R, -1 – 20 Bar

- AKS 32, - 1 – 34 Bar

- AKS 32R, -1 – 34 Bar

- AKS 32, - 1 – 50 Bar

- AKS 32R, -1 – 50 Bar

- AKS 2050, 1 – 59 Bar

- AKS 2050, -1 – 99 bar

- AKS 2050, -1 – 159 bar

- MBS 8250, -1 – 159 Bar

Voltage signals for reference displacement: Ext. Ref. Signal General voltage inputs 1 - 5 Setting:

- 0 - 5 V,

- 1 - 5 V,

- 0 -10 V,

- 2 - 10 V

61

##### **Set alarm priorities**

*[Figurtekst: 2. Select Alarm priorities]*

3. Set priorities for Temperature alarms

4. Set Alarm priorities for sensor error

Very many functions have an alarm connected. Your choice of functions and settings has connected all the relevant alarms that are current. They will be shown with text in the three pictures.

All alarms that can occur can be set for a given order of priority:

- ”High” is the most important one

- ”Log only” has lowest priority

- ”Disconnected” gives no action

The interdependence between setting and action can be seen in the table.

*[Figurtekst: Setting Log Alarm rela y  selection Net- AKM- · Non Hi g h Low - Hi g h work  dest. · Hi g h X X X X 1 · Medium X X X 2 · Low X X X 3 · Lo g  onl y X 4 · Discon- · nected]*

In our example we select the settings shown here in the display

In our example we select the settings shown here in the display

62

5. Set Alarm priorities for "Various alarms"

6. Set Alarm priorities for General functions

In our example we select the settings shown here in the display

There are no general alarms in our example.

63

##### **Lock configuration**

2. Select Lock/Unlock configuration

###### 3. Lock Configuration

Press in the field against **Configuration lock.** Select **Locked** .

The setup of the controller has now been locked. If you subsequently want to make any changes in the controller’s setup, remember first to unlock the configuration.

**The controller will now make a comparison of selected functions and define inputs and outputs. The result can be seen in the next section where the setup is controlled.**

64

##### **Check configuration**

2. Select  I/O configuration

3. Check configuration of Digital Outputs

4. Check configuration of Digital Inputs

5. Check configuration of Analog Outputs

###### **This control requires that the setup is locked**

(Only when the setup is locked are all settings for in- and outputs activated.)

**An error has occurred, if you see the following:**

The setup of the digital outputs appears as it is supposed to according to the wiring made.

A **0 – 0** next to a defined function. If a setting has reverted to 0-0, you must control the setup again. This may be due to the following:

- A selection has been made of a combination of module number and point number that does not exist.

- The selected point number on the selected module had been set up for something different.

The error is corrected by setting up the output correctly.

- Remember that the setup must be unlocked before you can change module and point numbers..

The setup of the digital inputs appears as it is supposed to according to the wiring made.

- The settings are shown on a **RED** background. If a setting has turned red, you must control the setup again. This may be due to the following:

- The input or the output has been set up; but the setup has later been changed so that it should no longer be applied.

The problem is corrected by setting **module number to 0 and point number to 0.**

(In our  example we do not use the analoge outputs)

- Remember that the setup must be unlocked before you can change module and point numbers.

The setup of the Analog inputs appears as it is supposed to according to the wiring made.

65

#### **Check of connections**

*[Figurtekst: 2. Select I/O status and manual]*

###### 3. Check Digital Outputs

*[Figurtekst: 4. Check Digital Inputs]*

###### 5. Check Analog inputs

Before the control is started we check that all inputs and outputs have been connected as expected. **This controls requires that the setup is locked**

By means of the manual control of each output it can be checked whether the output has been correctly connected.

*[Figurtekst: AUTO The output is controlled by the controller · MAN OFF The output is forced to pos. OFF · MAN ON The output is forced to pos ON]*

- Activate the various functions (the door switch and the main switch). Check that the controller registers the activation – i.e. whether the ON/ OFF value is changed in the last column. Check the other digital inputs in the same way. (In our  example we do not use the analoge outputs) Check that all sensors show sensible values. In our case we have no value. This may be due to the following: • The sensor has not been connected. • The sensor is short-circuited/interrupted • The point or module number has not been set up correctly. • The configuration is not locked.


#### **Check of settings**

1. Go to the overview

Before the control starts, we check that all the settings are as they should be.

The overview display will now show one line for each of the general functions. Behind each icon there is a number of displays with the different settings. It is all these settings that have to be checked.

2. Select evaporator A

3. Settings for thermostat

4. Move on with the next display for the section.  Here the alarm thermostat

Press the blue overview button at the bottom left of the display.

5. Settings for alarm thermostat

Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

Page 2 shows a summary of the temperature sequence over the past 24 hours.

Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.”

67

Check of settin g s - continued

6. Move on with the next display for the section.  Here the expansion valve function

   - Press the blue overview button at the bottom left of the display..

7. Settings for the injection function

Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

The settings can be reviewed in the same way as for section A.

8. Repeat for Evaporator B and later again for C

   - ,

9. Go to defrost display

Press the blue overview button at the bottom left of the display and then press the defrost symbol

   - ,

10. Settings for defrost

Remember the settings at the bottom of the pages – the ones that can only be seen via the ”Scroll bar”.

11. Go to defrost schedule

Press the **schedule** button to continue to the defrost schedule

68

###### 12. Setup defrost schedule

In our example, the defrost schedule is set to defrost twice a day.

13. Press a weekday and set the times for the various defrost starts.

Use the copying functions if there are several days with identical defrosts.

The end result with two defrosts per 24 hours can be seen here above.

###### 14. Go to common functions

- Press the blue overview button at the bottom left of the display and then on common functions

##### ,

###### 15. The settings for the common functions

Go through the individual functions.

16. The controller setup has been completed.

69

#### **Installation in network**

1. Set the address (here, for example 3) Turn the right-hand address switch so that the arrow will point at 3.

The arrow of the two other address switches must point at 0.

2. Push the Service Pin Press down the service pin and keep it down until the Service Pin LED lights up.

3. Wait for answer from the system unit Depending on the size of the network it may be up to one minute before the controller receives an answer as to whether it has been installed in the network. When it has been installed the Status LED will start to flash faster than normal (once every half second). It will continue with this for about 10 minutes

4. Carry out new login via Service Tool

If the Service Tool was connected to the controller while you installed it in the network, you must carry out a new login to the controller via the Service Tool.

The controller has to be remote-monitored via a network. In this network we assign address number 3 to the controller.

The same address must not be used by more than one controller in the same network.

###### **Requirement to the system unit**

The system unit must be a gateway type AKA 245 with software version 6.0 or higher. It is capable of handling up to 119 AK controllers. Alternatively, it can be an AK-SM 720. It is capable of handling up to 200 AK controllers.

###### If there is no answer from the system unit

If the Status LED does not start flashing faster than normal, the controller has not been installed in the network. The reason for this may be one of the following:

**The controller has been assigned an address out of range** Address 0 cannot be used.

If the system unit in the network is an AKA 243B Gateway only the addresses between 1 and 10 can be used.

**The selected address is already being used by another controller or unit in the network:**

The address setting must be changed to another (vacant) address.

###### **The wiring has not been carried out correctly.**

###### **The termination has not been carried out correctly.**

The data communication requirements are described in the document: ”Data communication connections to ADAP-KOOL® Refrigeration Controls” RC8AC.

70

#### **First start of control**

##### **Check alarms**

1. Go to the overview

Press the blue overview button at the bottom left of the display.

2. Go to the Alarm list

Press the blue button with the alarm bell at the bottom of the display.

###### 3. Check active alarms

In our case, we have a series of alarms. We will tidy them up so that we only have those that are relevant.

4. Remove cancelled alarm from the alarm list

Press the red cross to remove cancelled alarms from the alarm list.

5. Check active alarm again

In our case an active alarm remains because the control has stopped. This alarm must be active when control has not started. We are now ready for the startup of control.

Please note that active plant alarms are automatically cancelled when the main switch is in pos. OFF.

If active alarms appear when the control is started the reason for these should be found and remedied.

71

First start of control - continued

##### **Start the control**

1. Go to Start/Stop display

Press the blue manual control button at the bottom of the display.

2. Start control

Press in the field against **Main switch** . Select **ON** .

The controller will now start the controlling when the external function switch is also activated to ON.

If you wish to start an extra defrost cycle, it can be done via this display and also from the defrost screen.

72

##### **Setup logs**

1. Go to the overview

Press the blue overview button with the log symbol.

###### 3. New logs

The top line gives access to definition of new logs and to changes of already established logs. The next line enables you to see a selection of the defined logs

Here is the start display for new logs Start by defining which type of log has to be defined

Here it is determined which parameters have to be included in the setup of data. Select a function here, then a parameter, and finish with OK. Press hereafter "Arrow right"

Here is the survey of all the parameters that are collected in the log.

If a parameter has to be removed from the log collection, you must select the parameter and then press "Arrow left".

A LOG CAN ONLY BE DISPLAYED IF:

- THE CLOCK HAS BEEN SET AND

- THE CONFIGURATION IS LOCKED

73

#### **Manual defrost**

If you want to carry out manual defrost, proceed as follows.

2. Select defrost

3. Start defrost

74

### **5. Regulating functions**

This section describes how the different functions work

75

#### **Introduction**

###### **Application**

AK-CC 750A controllers are complete regulating units which together with valves and sensors constitute complete evaporator controls for refrigeration appliances and freezing rooms within commercial refrigeration.

Generally speaking they replace all other automatic controls containing, inter alia, day and night thermostats, defrost, fan control, rail heat control, alarm functions, light control, etc. The controller is equipped with data communication and is operated via a PC.

In addition to evaporator control the controller can give signals to other controllers about the operating condition, e.g. forced closing of expansion valves, alarm signals and alarm messages..

###### **Examples**

The controller has been designed to control one of the following four plant types.

Through the programming you determine which one.

Evaporator control of one, two, three or four evaporators

Control of cool or defrost room

Control of cool or defrost appliance

The controller’s main function is to control the evaporator so that the system constantly operates with the most energy-friendly refrigeration.

A specific function for registration of the need for defrost will adapt the number of defrosts so that no energy is wasted on unnecessary defrosts and subsequent cooling-down cycles.

Among the different functions can briefly be mentioned:

- Control of up to four evaporator sections

- Electronic injection with AKV or stepper valve

- ON/OFF or modulating temperature control

- Weighted thermostat and alarm thermostat

- Defrost on demand based on evaporator capacity

- Appliance cleaning function

• Appliance shutdown via data communication (The functions may not be mixed across the various sections of the evaporator.)

- The refrigerant is either regulated by means of:

- expansion valve type AKV/stepper or

- solenoid valve and thermostatic expansion valve

The complete survey of controllers and functions can be seen in the manual chapter 2 in section "Design o a evaporator control".

76

#### **Termostat function**

###### **Valve type and thermostat**

The thermostat can control the temperature via:

- a signal from the S3/S4 sensors in section A, or

- min/max or average temperatures in all the sections used (see the section on sensor selection)

###### Principle

Up to 4 valves can be connected to the controller; one for every solid state output.

It is possible to use electrically controlled expansion valves type AKV (ETS) for regulation, or else injection can take place using thermostatic expansion valves (TEV) in which the temperature is regulated using solenoid valves in the liquid line (LLSV), e.g. Danfoss type EVR.

The thermostat function can be defined in different ways depending on which application it is used for. For example:

- regulation principle /

- what sensors are to be used /

- whether the user wishes to toggle between two temperature settings, etc.

It is necessary for at least one air sensor to be fitted for every evaporator section. This is applicable irrespective of which thermostat function is selected – including " **no** " thermostat. The thermostat's cut-out temperature also has to be set to the correct air temperature as this value is used by the injection function.

###### Thermostat type= ON/OFF

One common valve for all evaporators + common ON/OFF ther - mostat

###### AKV valve

This principle can also be used with electronic expansion valves type AKV; e.g. refrigeration appliances where one valve is used for two evaporators. These appliances are specially designed for this application as the evaporator area is divided over two refrigeration sections in order to achieve a consistent load over the two circuits.

One valve for every evaporator + common ON/OFF thermostat Here, one valve is used per evaporator and the temperature is controlled according to the ON/OFF principle in accordance with the thermostat settings in section A

The thermostat can control the temperature via:

- a signal from the S3/S4 sensors in section A, or

- min/max or average temperatures in all the sections used (see the section on sensor selection)

A line up of refrigeration appliances which are to be regulated to the same temperature is a typical example.

The temperature is controlled according to the ON/OFF principle in accordance with the thermostat settings in section A.

77

One valve for every evaporator + individual ON/OFF thermostat Here, one valve is used per evaporator and the temperature is controlled individually in each evaporator section according to the ON/OFF principle.

The thermostat in each section controls the temperature via the S3/S4 sensors in each section.

During cooling and in the case of major load variations in which the temperature falls outside of the thermostat limits, injection is regulated so that the evaporator operates with the minimum possible stable superheating. This ensures that the cooling process takes place as quickly as possible.

In the case of stable loads, the thermostat will reduce the opening time for the AKV valve, so the through flow of refrigerant is restricted to precisely the amount that is required to maintain the temperature at the required reference (area control).

The reference temperature will be the set cut-out temperature + half the difference.

The cut-out temperature and difference are set as in the case of a standard On/Off thermostat. The difference should **not** be set to less than 2K. (In the case of a smaller difference, load changes could interfere with the modulating thermostat function.)

One solenoid valve for each evaporator + modulating thermostat Here, one valve is used per evaporator and the temperature is controlled individually in each evaporator section according to the modulating thermostat principle.

The thermostat in every section controls the temperature via the S3/S4 sensors in every section (where appropriate, see the section on sensor selection).

###### Thermostat type = Modulating

Modulating temperature regulation maintains a more constant temperature and also equalises the load on the system so that the compressors have better operating conditions.

- This function can only be used on:

- central systems with AKV valves

- central systems with solenoid valves

- brine systems with solenoid valves.

- Each of the individual evaporator sections is controlled individually using a modulating thermostat function.

- Cut-out value and difference **must** be set as with an ON/OFF thermostat.

One AKV valve for each evaporator + modulating thermostat Here, one valve is used per evaporator and the temperature is controlled individually in each evaporator section according to the modulating thermostat principle.

With solenoid valves, a pulse modulating principle is used with an adjustable period. The valve is opened and closed within a period (e.g. 5 minutes). A PI controller calculates how long the valve needs to be open in order to maintain the most constant temperature.

The reference temperature will be the set cut-out temperature + half the difference.

The cut-out temperature and difference are set as in the case of a standard On/Off thermostat. The difference should not be set to less than 2K. (In the case of a smaller difference, load changes could interfere with the modulating thermostat function.)

The current load on the appliance can be read off in the form of the valve's opening time as a percentage of the set period.

78

###### Desynchronisation of valve openings

To achieve even loading on the compressors, a desynchronising function has been built in which ensures that the times for solenoid valve opening are displaced.

If AKV (stepper) valves are used, at least one sensor must **always** be used in every section, irrespective of the choice of thermostat function. This measurement is used by the injection function for the superheat controller.

###### Within the same controller

If several valves are used on the same controller, the opening times are displaced in relation to one another. For example, if two valves are used, the opening of these is displaced in relation to one another by half a period.

###### Between controller

Displacement of the opening of the solenoid valves takes place on the basis of the controllers' address settings. If a period time of 300 seconds (factory default) is used, the opening of the solenoid valves for the A section will be displaced by 15 seconds x last digit in the address setting, e.g.:

Addresses 0, 10, 20: are shifted by 0 seconds Addresses 1, 11, 21: are shifted by 15 seconds, etc.

*[Figurtekst: This desynchronisation between controller takes place during · start-up and once a day at around midnight, 00:00 · Address / Section · 10 / A · 10 / B · 11 / A · 11 / B · 12 / A · 12 / B · 22 / A · 22 / B]*

###### **Thermostat sensor**

###### Individual thermostat

When individual thermostat control is used in every section, the temperature is controlled on the basis of the air temperature sensors S3, S4 or both.

###### Common thermostat

When a common thermostat is used, the thermostat settings in section A are used to control the air temperature.

The thermostat temperature can be either a weighting of the S3 and S4 sensors in section A, as described for the individual thermostat. This will typically be used in cold storage rooms and freezer rooms in which several evaporators are controlled according to a common temperature.

*[Figurtekst: ing to a common temperature.]*

Alternatively, the thermostat temperature can be a minimum value, a maximum value or an average value of all S3 or S4 sensors for the refrigeration sections used. This will typically be used where one solenoid valve is used for several appliance sections and where it is necessary to ensure that the thermostat is taking into account the temperature in all sections.

*[Figurtekst: Min. S4  / · Max. S4  / · S4 average · Min. S3  / · Max. S3  / · S3 average]*

Definition of the thermostat temperature takes place using one setting, which is based on the S4 value. With a setting of 100%, only the S4 measurement will be used. With a setting of 0%, only S3 will be used. With a value between 0 and 100%, both measurements will be used.

79

###### **Swithc between two thermostat band (two references)**

It is a good idea to use this function for refrigeration appliances containing impulse purchases where the products are often exchanged. Via a switch function it is possible to change between two thermostat settings depending on the products contained in the appliance. The change-over between two thermostat bands is activated via a contact or via a pulse signal of at least three seconds’ duration – as a rule via a key switch placed on the appliance. When the switch is activated the thermostat settings as well as the limits for the alarm thermostat and the product sensor will change.

The changeover between the two thermostat bands can also be seen on the display, but only if the shift is set to take place with a pulse signal.

The signal may be a 0-5V, 0-10V, 1-5V or 2-10V voltage signal. Two offset values must be set, one indicating the displacement at minimum signal and another indicating the displacement at maximum signal. The displacement will apply to all sections. The displacement will not affect the alarm limits.

###### **Melting function**

This function will stop the air flow in the evaporator from being reduced by frost created by uninterrupted operation for a long time. The function is activated if the thermostat temperature has remained in the range between -5°C and +10°C for a longer period than the set melting interval. The refrigeration will then be stopped during the set melting period. The frost will be melted so that the air flow and hence the evaporator’s capacity will be greatly improved.

The settings for melting interval and melting period are common to all sections, but the controller will displace the melting time for the different sections so that no synchronisation will take place. If there are several controllers in the same defrost group the time between the two meltings should be set differently in the individual controllers. In this way a synchronisation of the thermostats’ cutin times will be avoided.

When a change-over is activated the display will show to which thermostat band the change goes.

###### **Displacement of reference for thermostat**

###### **Timer for compressor relay**

If a compressor relay has been selected, the relay’s timer function will have higher priority than the thermostat function.

In refrigeration appliances there may be big load differences between the shop’s opening and closing hours, especially if Night blinds/curtains are used. The thermostat reference may be raised here without it having any effect on the product temperature. Change-over between day and night operation can take place, as follows:

- via the built-in weekly schedule

- via an external switch signal

- via a signal from the data communication

When night operation starts the thermostat reference will be displaced with an offset value that normally will be positive. It must however be negative if cold accumulation is to take place. When a Night blind is used the distribution of air in the appliance will change radically. A change of the thermostat’s weighted S3/ S4 ratio will therefore be required. As a rule the S4 share is set at a lower value during the night than during the day.

The thermostat reference can be displaced via an external voltage signal which is particularly useful for process cooling.

80

#### **Temperature alarms**

###### **Alarm thermostat**

The function is used for sounding the alarm before the product temperature at the refrigeration site becomes critical. You can set alarm limits and time delays for high and low temperatures. Alarm will be given if the set limit is exceeded, but not until the time delay has expired.

There will be no alarms when refrigeration has been stopped due to cleaning of the appliance or if the main switch is set in pos. OFF. The alarm sensor may be chosen independently of the sensor used for the thermostat function.

###### Alarm sensor

The alarm sensor may be selected as either S3 or S4, or a weighted value of both of them.

- Curve 1: Cooling stage (1): Time delay has been exceeded. . Alarm  be comes active.

- Curve 2: Normal regulation where the temperature becomes too high (2): Time delay has been exceeded. . Alarm  be comes active.

- Curve 3: Temperature becomes too low (3): Time delay has been exceeded. . Alarm  be comes active.

If regulation is carried out with two thermostat bands there will be a set of alarm limits for each band. Time delays will be common to the two bands.

The setting is performed as a percentage value of S4.

The weighting need not be the same as for the thermostat

function. In other words, the thermostat may regulate according to S4 and the alarm thermostat may give alarm according to S3.

###### Alarm limits

Different alarm limits can be set for the individual sections. The alarm limits are set as absolute values in °C.

If thermostat bands are used, separate limits can be set for each thermostat band. The alarm limits are not affected if there is an external reference displacement via a voltage signal. During night operation the value for upper limit will raise with the same value as night operation is raised with (a negative night setback will not change the limit value).

###### **Product sensor with alarm function**

An extra temperature sensor may be connected to each section. The sensor will function independently of the other functions.

Alarm limits and time delays can be set, as for the alarm thermostat.

###### Time delay

Three time delays are set for alarms:

- For too low temperature

- For too high temperature during normal regulation

- For too high temperature during cooling down

- after activation of internal or external start/stop

- during a defrost

- after a power failure

- after appliance cleaning.

- The time delay will apply until the actual air temperature has dropped below the “upper alarm limit”..

###### Example

###### **Frost alarm**

If the thermostat is controlled according to the S3 temperature or a weighting of S3/S4, there could be a risk (on the refrigeration shelves) that the evaporator’s S4 discharge temperature may become so cold that the products at the back of the shelves become exposed to unintended frost temperatures.

To prevent this, the controller has a built-in frost alarm. If the S4 temperature falls below a set frost limit an alarm will be given so that the cause of the cold outlet temperature can be found and corrected.

*[Figurtekst: N:  Thermostat cut-in value · OUT:  Thermostat cut-out value · Lim:  Alarm limit for high temperature and low temperature · S:  Alarm ceases]*

81

#### **Common functions**

###### **Fan control**

To obtain energy savings it is possible to reduce the power supply to the fans at the evaporators. The reduction can be done:

- during the thermostat’s cutout period (cold room)

- during night operation and during the thermostat’s cutout period (appliance with Night blind)

It can be controlled by one of the following 4 fan types:

###### Single speed fan

One relay is used here to control the fans. This relay can be pulse controlled, but only when all sections/evaporators are cut out

A period of time is set as well as the percentage of this period of time where the fans have to be operating.

###### 2-speed fans

Two relays are used here to control the fans. One relay will provide full speed for the fans, and when the second relay triggers, the speed of the fan motors is reduced. The relay for reduced speed will be referred to as 'eco' in the setup of outputs.

###### Fan with EC motor

Here the controller must use an analogue output module that can deliver the desired voltage to the EC motor. 0 - 10 V, 2 - 10 V, 0 - 5 V or 1 - 5 V.

The desired fan speed is given as a percentage of the output signal i.e. 0 - 100 %. For example, 90 % during normal daytime operation and 70 % during eco operation.

Different values can be set for the four operating modes: Normal day, Normal night, Day with thermostat disconnected, Night with disconnected thermostat.

A minimum start speed can be set. This setting will only apply for 10 seconds after the start.

###### **Rail heat control**

It is possible to pulse-control the power to the rail heat in order to save energy. Pulse control can either be controlled according to day/night load or dew point.

Pulse control according to day and night

Various ON periods can be set for day and night operation.

A period time is set as well as the percentage part of the period in which the rail heat is ON.

###### Pulse control according to dew point

In order to use this function a system manager of the type AK-SM 720, 850, AK-SC 255 or 355 is required which can measure dew point and distribute the current dew point to the appliance controllers. For this the rail heat’s ON period is controlled from the current dew point.

*[Figurtekst: Effect · Railheat. · Min. ON% · Dew point]*

Two dew point values are set in the appliance control:

- One where the effect must be max. i.e.100%.

- One where the effect must be min.

###### Fans that are controlled by a frequency converter (VSD)

The controller must use an analog output module for these with a starting relay for on/off control of the converter. The settings are the same as for EC motors

###### Stop of fans if cooling is missing

If the refrigeration in a breakdown situation stops, the temperature in the cold room may rise quickly as a result of the power supply from large fans. In order to prevent this situation the controller can stop the fans if the temperature at S5 exceeds a set limit value. The function can also be used as a sort of MOP function during start-up with a hot evaporator. The fans will not start until the S5 temperature has been reached below the set limit value. In other words, the evaporator and hence the compressor wll not be so heavily loaded during the startup phase. The function uses the S5 sensor from section A.

At a dew point which is equal to or lower than the value, the effect will be the value indicated in "Rail heat min ON%".

In the area between the two dew point values the controller will manage the power to be supplied to the rail heat.

The current dew point and duty cycle for rail heat can be read off as status values.

If the dew point signal cannot be distributed to a controller, the rail heat will revert to day/night control.

###### During defrost the rail heat will always be 100% ON.

If rail heat ON is selected, it will run at 100% during defrost + the time after defrost if the thermostat temperature is above the cutin limit (but max. 15 minutes).

The function is not active when refrigeration has stopped.

82

###### **Compressor control**

The controller has a function that can be used for compressor control. When the function is selected ON a relay will automatically follow the status of the thermostat functions. The relay is ON when the thermostat demands refrigeration. If the thermostat function is selected OFF the compressor output will constantly be ON. A minimum ON time and a minimum restart time for the relay belong to the function. The relay will be OFF during defrost. There is display of:

- operating hours during the past 24 hours

- total number of operating hours

- number of couplings during the past 24 hours

- total number of couplings

###### **Appliance cleaning**

This function makes it easy for the shop’s staff to carry out a cleaning of the appliance according to a standard procedure.

Appliance cleaning is activated via a pulse signal of minimum three seconds’ duration – as a rule via a key switch placed on the appliance. It can however also be activated via data communication. Appliance cleaning is carried out via three phases:

- 1 - at the first activation the refrigeration is stopped, but the fans keep on operating in order to defrost the evaporators. ”Fan” is shown on the display.

- 2 - at the second activation the fans are also stopped and the appliance can now be cleaned. ”OFF” is shown on the display.

- 3 - At the third activation refrigeration is recommenced. The display will show the actual appliance temperature.

To carry out cleaning of a frost appliance as quickly as possible cleaning can be started with a defrost sequence.

When appliance cleaning is activated a cleaning alarm is transmitted to the normal alarm recipient. A later processing of these alarms will document that the appliance has been cleaned as often as planned. The function saves information on when the last appliance cleaning was carried out and how long it lasted.

###### **Appliance shutdown**

This function makes it possible to shut down a refrigeration appliance using data communication or a switch signal. When the signal is received, refrigeration and alarm monitoring stops.

Fans and lights will do the following depending on the setup:

- Fans continue. The light will follow the standard setup.

- Fans stop immediately. The light immediately switches off.

- Fans stop when the delay time expires. The light will follow the standard light control.

- Fans stop when the delay time expires. The light switches off when the delay time expires.

The shutdown delay time is adjustable and applies to both fans and lights.

Any night curtain output will follow the light function.

###### **Door contact**

The door contact function can be defined for two different applications:

- Door alarm The controller monitors the door contact and delivers an alarm message if the door has been opened for a longer period than the set alarm delay.

- Stop of refrigeration + door alarm When the door is opened the refrigeration is stopped, i.e. the injection and the fan are stopped. If the door remains open for a longer time than the set restart time, refrigeration will be resumed. This will ensure that refrigeration is maintained even if the door is left open or the door contact should be defective. If the door remains open for a longer period than the set alarm delay an alarm will also be sounded.

In both applications the alarm function will also contain a local reminder which is activated when 75% of the set time has been passed.  This reminder only appears on the connected display and the intention of it is that the door must be closed before the alarm for open door is released.

###### From the controller the following can be read:

- the duration of the last open period

- the total open period during the past 24 hour

- number of openings during the past 24 hours

Defrost has higher priority than the door function. That is to say, refrigeration and fans will not be started until defrost is complete.

The door contact function can also activate the light function so that the light is turned on and kept on for a period of time after the door has again been closed. Cf. the section on light function.

###### **Light function**

The function can be used for controlling the light in a refrigeration appliance or in a cold room. It can also be used for controlling a motorised night curtain.

The light function can be defined in three ways:

- the light is controlled via a signal from a door contact. Together with this function a time delay can be set so that the light is kept burning for a period of time after the door has been closed.

- the light is controlled via the day/night function

- the light is controlled via the data communication from a system unit.

It is possible to set whether the light is to be switched on or off when the main controller switch is activated. This is set in the function "Light at main switch=off". If "Light at main switch=off" is set to ON, the normal light function will be maintained when the main switch is switched off. If OFF is selected for this setting, the light will stay off when the main switch is switched off.

###### **Night blind**

Motorised night blind can be controlled automatically from the controller. The night blinds will follow the status of the light function. When the light is switched on, the night blinds opens and when the light is switched off, the night blinds close again. When the night blinds are closed, it is possible to open them using a switch signal on the digital input. If this input is activated, the night blinds will open and the refrigeration appliance can be filled with new products. If the input is activated again, the blinds close again.

When the night blind function is used, the thermostat function can control with different weighting between the S3 and S4 sensors. A weighting during day operation and another when the blind is closed.

83

A night blind is open when the appliance cleaning function is activated.

To ensure the correct position of the night blind the fans can be switched off in the period during which the night blinds roll down.

###### **Forced closing**

The AKV (stepper) valves can be closed with an external signal (the “Inject ON signal”). The function must be used in connection with the compressor’s safety circuit, so that there will be no injection of liquid into the evaporator when the compressor is stopped by the safety controls. (However not at low pressure – LP).

The signal can also be received from the DI-input or be received via the data communication.

During a forced closing the fans can be defined to be stopped or in operation.

Defrosting can also be permitted or omitted during this period. If defrosting has been requested within 10 minutes of the end of forced closing, defrosting will restart the moment forced closing ends.

###### **Alarm relay**

If the controller is to give alarm at a relay output, the relay must be defined.

A setting determines when the relay is activated:

- Only for alarms with “high” priority

- For alarms with “low” and “medium” priority

- For alarms with “low”, “medium” and “high” priority.

The controller can receive a signal from a leak detector. This signal will not activate the alarm relay; but the alarm will be shown on any displays that are connected.

###### **Start/stop of regulation (main switch)**

A software setting is used for starting and stopping the regulating function.

ON = normal regulating function OFF = Regulation stopped. All outputs will be set in standby mode. All alarms are stopped. An alarm can however be transmitted to the effect that regulation has stopped. The function applies to all sections.

You can also define an external switch for start/stop of the regulation.

If an external switch is defined regulation will only be carried out when both switches are in position ”ON”.

84

#### **General monitoring functions**

**General alarm inputs** (10 units) An input can be used for monitoring an external signal.

The individual signal can be adapted to the relevant use as it is possible to give the alarm function a name and to indicate your own alarm text.

A time delay can be set for the alarm.

###### **General thermostat functions** (5 units)

The function may freely be used for alarm monitoring of the plant temperatures or for ON/OFF thermostat control. An example could be thermostat control of the fan in the compressor compartment.

The thermostat can either use one of the sensors used by the regulation (Ss, Sd, Sc3) or an independent sensor (Saux1, Saux2, Saux3, Saux4).

Cutin and cutout limits are set for the thermostat. Coupling of the thermostat’s output will be based on the actual sensor temperature. Alarm limits can be set for low and high temperature, respectively, including separate alarm delays.

The individual thermostat function can be adapted to the relevant application as it is possible to give the thermostat a name and to indicate alarm texts.

**General voltage input with ancillary relay** (5 units) 5 general voltage inputs are accessible for monitoring of various voltage measurements of the installation. Examples are monitoring of a leak detector, moisture measurement and level signal - all with ancillary alarm functions. The voltage inputs can be used to monitor standard voltage signals (0-5V, 1-5V, 2-10V or 0-10V). If required, one can also use 0-20mA or 4-20mA if external resistance is placed at the inlet to adjust the signal to the voltage. A relay outlet can be attached to the monitoring so that one can control external units.

For each inlet, the following can be set/read out:

- Freely definable name

- Selection of signal type (0-5V, 1-5V, 2-10V, or 0-10V)

- Scaling of read-out so it corresponds to measuring unit

- High and low alarm limit including delay times

- Freely definable alarm text

- Attach a relay output with cut in and cut-out limits including delay times

###### **General pressure control functions** (5 units)

The function may freely be used for alarm monitoring of plant pressure or for ON/OFF pressure control regulation.

The pressure control can either use one of the sensors used by the control function (Po, Pc) or an independent sensor (Paux1, Paux2, Paux3).

Cutin and cutout limits are set for the pressure control. Coupling of the pressure control’s output will be based on the actual pressure. Alarm limits can be set for low and high pressure, respectively, including separate alarm delays.

The individual pressure control function can be adapted to the relevant application as it is possible to give the pressure control a name and indicate alarm texts.

85

#### **Liquid injection**

###### **Principle**

Up to four valves can be connected. One for each solid state output.

Control can be carried out with electrically operated expansion valves type AKV, ETS or CCMT.

Or injection can take place with thermostatic expansion valves (TEV) where the temperature will then be regulated with solenoid valves type EVR or similar.

If both a stepper valve and a solenoid valve are installed in the liquid line, any liquid trapped between the two valves will be returned if the valve is a Danfoss EVR.

###### Functions:

- Disconnected. Liquid flow is not permitted

- Liquid flow is permitted. Stopped by a common DI signal

• Liquid flow is permitted. Stopped by a signal from the system device. The signal is common to all sections.

When regulating with a flooded evaporator, three separate superheat settings are used.

**It is the installer’s responsibility to ensure that signal loss to the controller will not result in liquid throughput to the compressor. Danfoss accepts no responsibility for damage resulting from inadequate installation.**

###### **Scaling factor for the valve**

The valve’s staging area can be limited when a step valve is chosen or it can be guided using an analogue output signal. The setting applies to all sections.

###### **Pressure transmitter signal**

One pressure transmitter can supply signals to several controllers if they regulate refrigeration points on the same suction line. But if a valve is mounted in an evaporator’s suction line, say, a KVP / KVQ or PM, the pressure transmitter must be placed before the valve. The signal can now only be used by the relevant controller.

###### **Refrigerant**

###### **Adaptive superheat with AKV (stepper) valve**

The evaporating temperature is measured with pressure transmitter P and the superheat with the pressure transmitter and the S2 sensor.

The function contains an adaptive algorithm that independently adjusts the valve’s opening degree, so that the evaporator constantly delivers optimum refrigeration at lowest possible superheat.

The superheat reference will be limited by the settings for min. and max. superheat.

If the superheat is very low, the valve may be closed very quickly using the "SH closed" setting. When the superheat has dropped to 1 K over the "SH closed" limit, this function will reduce the degree of opening of the valve so that the valve will with certainty remain closed if the superheat fall to the "SH closed" value. To ensure that the close function does not generate the general superheat regulation, the "SH closed" setting must be at least 1K lower than "SH min".

###### **Flooded evaporator**

This function allows liquid flow in the evaporator, but only when a signal is received. If the signal disappears, then the regulation switches over to “adaptive superheat”.

Before regulation can be commenced, the refrigerant must be defined.

You can directly select one of the current refrigerants:

|1 R12|13User defined|25 R290|37 R407F|
|---|---|---|---|
|2 R22|14 R32|26 R600|38 R1234ze|
|3 R134a|15 R227|27 R600a|39 R1234yf|
|4 R502|16 R401A|28 R744|40 R448A|
|5 R717|17 R507|29 R1270|41 R449A|
|6 R13|18 R402A|30 R417A|42 R452A|
|7 R13b1|19 R404A|31 R422A||
|8 R23|20 R407C|32 R413A||
|9 R500|21 R407A|33 R422D||
|10 R503|22 R407B|34 R427A||
|11 R114|23 R410A|35 R438A||
|12 R142b|24 R170|36 R513A||

If a new refrigerant is demanded which is not as yet contained on the list you may select ”User-defined” which is subsequently set with data for the refrigerant in question. The values can be ordered from Danfoss.

Warning: Incorrect selection of refrigerant can cause damage to the compressor.

###### **MOP control**

(MOP = Max. Operating Pressure)

The MOP function limits the valve’s degree of opening as long as the evaporating temperature measured by S1 is higher than the set MOP temperature. The function can only be active when the AKV injection valve function is ON.

###### **Start/stop of injection**

The injection can be stopped separately for each evaporator sec- tion.

86

#### **Defrost**

There is a common defrost start for all evaporator sections. Defrost stop can be common or individual when based on temperature. Refrigeration will not be re-started until defrost has been accomplished in all sections.

Fan control during defrost

Choose whether the fans should be running or stopped during the defrost sequence.

###### Coordinated defrost

If there are several controllers that are to perform defrost at the same time they can be grouped from the system unit. The system unit will start the defrosts, and when the defrost of the individual controllers is later finished they will go into ”stand-by” position until all the defrosts have been terminated. Refrigeration is then resumed.

*[Figurtekst: Hot gas defrost]*

During hot gas defrost, the controller regulates valves in the liquid line, hot gas valves, a suction line valve and a drain valve. A time delay can be set which defers opening of the hot gas valve.

###### **Defrost start**

###### Drip tray heating element

It is possible to control a heating element in the drip tray for hot gas defrost. When defrost is commenced, the heating element is activated. The heating element remains activated until a set time after defrost has ended by time or temperature.

###### **Defrost type**

###### Electric defrost

Defrost can be started in several ways. Once started it will continue until a ”defrost stop” signal is received.

- Manual defrost

Manual defrost can be enabled via a setting in the controller or via the bottom button on the display. After activation the setting moves back to position OFF when the defrost has been completed.

- External signal on input

Defrost start is done with a signal on a DI input. The signal must be an impulse signal of at least three seconds’ duration. Defrost starts when the signal moves from OFF to ON.

- Schedule – weekly programme

When there is electric defrost, the individual sections’ heating elements are controlled separately.

###### Natural defrost

Defrost can be started via an internal schedule or via an external schedule placed in the network's system unit.

- Internal schedule

Defrost is started by means of a weekly programme that is set in the controller. The times have relation to the controller’s clock function. Up to eight defrosts per 24 hours can be set. The schedule can be found via the ”Overview display” / ”Defrost” / ”Schedule”.

- External schedule

Defrost is started via a signal from the network's system unit

- Interval

Defrost is accomplished here by the fans circulating air through the evaporator.

###### Warm brine defrost

Defrost starts with set intervals, e.g. every eight hours. An interval must ALWAYS be set to a "higher" value than the period set between two defrosts when a schedule or network signal is used. Defrost according to intervals ensures that defrost always takes place, even if no signal is received from the network's system unit.

- Adaptive defrost

Warm brine defrost can be used on indirect refrigeration systems with solenoid valves. During warm brine defrost, the solenoid valve is kept open during defrost so that the warm brine can run through the "evaporator".

This function can cancel planned defrosts which are not necessary, and on its own initiative it can start a defrost if the evaporator is about to be blocked by rime and ice. (The "Adaptive defrost" function is described at the end of the section.)

###### **Defrost sequence**

Every defrost runs through the following sequence:

87

- emptying of evaporator (pump down) (state 1)

- defrost is initiated (state 3)

- waiting position (used for coordinated defrost) (state 4)

For large evaporators there should be two S5 sensors – S5-1 and S5-2. The defrost is stopped when both temperatures have attained the set value.

- drip-off (injection delay) (state 5)

- Pressure equalisation where the drain valve opens (hot gas defrost only) (state 6)

- fan delay (state 7)

###### Emptying of evaporator (state 1)

Before the defrost heating elements are started it is possible to carry out emptying of the evaporator. During a set time delay (hot gas delay), the valve in the liquid line remains closed, the fans run and the evaporator is drained of refrigerant. When the delay time has expired it will continue to state 3.

###### Defrost (state 3)

- Electric defrost

The electric heating elements are activated here.

- Natural defrost

If the defrost time exceeds the set max. defrost time, the defrost stops. This will happen even if the defrost stop temperature has not been reached (max. defrost time will function as safeguard). When the defrost is stopped on time, the alarm message “Max. def. period exceeded” will appear for the section in question. If the alarm is not acknowledged within five minutes, it will automatically be cancelled.

When there is an error in a defrost sensor, an alarm appears and the defrost stop will then be based on time in the relevant section. Defrost stop for the remaining sections will still be based on temperature.

   - Common stop using temperature and with time as security In the case of electric and hot gas defrost, only one output is used for all evaporators, i.e. one output for heating element / common hot gas valve.

- Here, the fans run in order to defrost the evaporator using air circulation alone.

- Hot gas defrost

- Here, the drain valve and suction line valve are closed. The hot gas valve opens in order to feed hot gas through the evaporator.

- Warm brine defrost

Here, the solenoid valve is held open so that warm brine can be fed through the evaporator.

###### Defrost stop

There are four kinds of defrost stop to choose from.

- Individual stop using temperature and with time as security In the case of electric and hot gas defrost, one output per evaporator is used here, i.e. an individual heating element / hot gas valve per evaporator.

Example of hot gas usage with common hot gas valve for all evaporators

The temperatures of each evaporator are measured using a sensor. Once all the evaporator temperatures are equal to or greater than the set temperature for defrost stop, defrosting is stopped in all sections and the defrost sequence continues.

The selection of defrost stop sensor as well as the "safeguard" stop on time if stop temperature can not reached is exactly as described for individual stop.

- Stop based on time

A fixed defrost time is set here. When this time has elapsed, the defrost will be stopped and cooling will be resumed. (When stop on time the controllers does not check whether one or more of the evaporators still require defrost.

Example of hot gas usage with individual stop per evaporator

The temperatures of each evaporator are measured using a sensor. When this temperature is then equal to or greater than the set temperature for defrost stop, defrost stops in the section in question. The defrost sequence continues only when all sections have completed defrost.

When there is electric defrost, S5 is normally selected as defrost sensor, but S3, S4 or S2 may also be selected (S3 is an air sensor placed in the evaporator inlet, and S4 is an air sensor placed in the evaporator outlet).

- Minimum defrost time

A time can be set which must pass before defrosting can be concluded. This time setting has higher priority than Max. defrost time.

- Manual stop

Defrost in progress can be stopped manually by enabling the "Stop defrosting" function."

If a signal on forced closing during a defrost is received,   the selected setting determines whether defrosting is to be stopped.

88

###### Coordinated defrost (state 4)

Via a system unit it is possible to perform a group defrost with other appliance controllers. The system unit will in that case start a defrost with a start signal via the data communication. When the first section of a controller has finished defrost, the controller starts the “Max. hold time” function and when all sections have finished defrost, this is recorded by the system unit. The controller will then move into waiting position until it receives a signal to restart refrigeration. This happens when all controllers in the group have concluded their defrosts. If this message has not been received within the “Max. holding time” time, the controller will resume refrigeration under all circumstances.

###### Drip - of f delay (state 5)

A time delay can be put in so that any drops of water may drip off the evaporator before refrigeration is resumed. In this way it is ensured that the evaporator as far as possible is free from water when refrigeration is restarted.

###### Example

Below is an example of a defrost sequence using hot gas defrost.

The following are used in the example:

- Hot gas defrost with common hot gas valves

Drain delay / pressure equalisation during hot gas defrost (state 6)

When the drip delay is completed, it is possible to add a drain delay in which the smaller drain valve opens up to the suction line so that pressure equalisation takes place. Once the drain delay has expired, the main valve in the suction line opens and cooling is resumed.

###### Delayed fan start (state 7)

Regardless of whether the fans are running or have stopped during the defrost sequence, the fans can be stopped during this delay.

Drops of water left on an evaporator after defrost should be bound to the evaporator (primarily used in freezing rooms). After defrost, the liquid injection is started, the evaporator is cooled down, but the fans will be started a little later. During this period the controllers operate the expansion valve by force, but they constantly monitor the superheat.

The temperature at which the fans are to be started is set (measured always with the S5 sensors).  The max. permissible time delay in minutes is set.

The time delay for fan start will not commence until the time delay for liquid injection, if applicable, has run out.

Only when all the S5 sensors register a lower temperature than the set  will the fans be started. If all S5 sensors do not register a lower temperature than the set by the delay time has elapsed, the fans will start. At the same time alarm is given  that Maximum delay time for fan is exceeded for the section in question. If the alarm is not acknowledged within five minutes, it will automatically be cancelled.

If some of the S5 sensors are defective, the signal from sensors that remain intact will be used.

- Defrost using the evaporators is stopped individually using the S5 temperature

- The fans are stopped during defrost

###### The defrost sequence will be as follows:

- Pump down (state 1)

- The AKV (ETS) valve closes, the heating element in the drip tray is activated and the fans run.

- Time delay before the next phase (hot gas time delay, state 2)• Defrost (state 3)

The fans stop, the main valve and the drain valve in the suction line are closed and the hot gas valve opens. Defrost is terminated when the S5 sensor has reached its stop temperature.

- Hold (state 4)

If coordinated defrost is being used, the controller will wait for a release signal from the network's system unit before continuing with the sequence. Alternatively, the hold stops once the maximum hold time has expired.

- Drip delay (state 5) Cooling is delayed so that any drops of water can run off the evaporator.

- Drain delay / pressure equalisation (state 6) The drain valve opens so that pressure equalisation takes place in the evaporator.

- Fan delay (state 7)

The main valve in the suction line opens and liquid injection is resumed. The fans are delayed so that the remaining drops of water are bound to the evaporator. The fans start when the required fan start temperature has been reached on the S5 sensor,

89

###### or when the set delay time has expired.

- Drip tray heating element

The drip tray heating element is switched off when the set delay time has expired. This delay time is applicable from the end of defrost (state 3).

schedule in the system unit. Other defrost start signals will always result in defrost.

This function will only cancel defrost if all evaporator sections so permit.

###### Function selection

###### **Adaptive defrost**

This function can cancel planned defrosts which are not necessary, and on its own initiative it can start a defrost if the evaporator is about to be blocked by rime and ice.

This function is based on a registration of the air flow through the evaporator. By using the AKV (stepper) valve as mass flowmeter for the refrigerant flow it is possible to compare the energy admission on the refrigerant side with the energy emission on the air side. Via this comparison the air flow through the evaporator can be determined and hence also the amount of ice/frost build-up on the evaporator surface.

###### Automatic adaptation to the evaporator

When adaptive defrost is activated it will carry out an automatic tuning in order to adapt itself to the relevant evaporator. The first tuning takes place after the first defrost so that tuning can be carried out on an evaporator without ice/rime formation. New tuning subsequently takes place after each defrost (but not at night with night blinds). In a few cases it may happen that the function is not correctly adapted to the relevant evaporator. This is usually because the automatic adjustment has been made under abnormal operating conditions at start-up/on testing the system. This will result in the function reporting an error state. If this happens, a manual reset of the function should take place while briefly setting the function switch to "OFF".

###### Status display

For each evaporator it is possible to display the current operating status for adaptive defrost:

- 0: OFF Function not activated

- 1: Error Reset to be carried out

- 2: Tuning Function carries out automatic tuning

- 3: OK - no ice build-up

- 4: Slight ice build-up

- 5: Medium ice build-up

- 6: Heavy ice build-up

###### Restrictions and sensor signals:

The following connections/signals must be used:

- Expansion valve type AKV/ETS/CCMT

- Temperature signal from both S3 and S4

- It is essential that the S3 and S4 sensors are located in the air flows of the evaporator inlet and evaporator outlet. The sensors must be mounted in such a way that the effects of external heat sources, such as fan motors, are minimised as far as possible.

- Pressure signal from condensation pressure Pc The Pc signal can be received from a pressure transmitter which is connected to the controller, or it may be received via data communications from the system unit. (Several controllers may share the same Pc signal.) If the controller does not receive a Pc signal, it will use a constant value for the condensation pressure.

- Adaptive defrosting cannot be used if one of the following refrigerants are used for regulation: R23, R513B, R13B1 or userdefined.

This function can be set to operate in one of the following ways:

0. OFF:

The function is stopped. Any alarms are removed and the function is reset.

1. Monitoring only:: The function is used exclusively to monitor the formation of ice on the evaporator – the function will not cancel planned defrosts.

If the function detects severe ice/rime formation on an evaporator, an alarm "Appliance A – air flow reduced" is transmitted. The alarm is removed at the start of the next defrost.

2. Skipping of defrosts by day (appliances with night blinds) This setting is used if function is only to cancel unnecessary defrosts by day, and if night blind is used for the appliance. This function undertakes new tuning only when defrost takes place during day operation.

- The controller MUST be set to night state when night time cover is set for the appliance – this may take place via a schedule in the controller or alternatively via a signal from the system unit. This is because there is a risk of the function detecting the formation of rime/ice on the evaporator when night blind is set for the appliance. (A greater reduction in air flow may occur as a consequence of a small distance between night blinds and products.

It is important for night time cover to be removed from the appliance when the controller switches to day operation. If not, there is a risk of incorrect tuning, and hence missing data for cancelling defrosts. Correct tuning will take place only after the next defrost.

3. Skip defrost day and night (refrigeration rooms and appliances without night blind) This setting is used if the function is to cancel defrosts for rooms and appliances without night blind. New tuning of the function takes place after each defrost.

4. Full adaptive defrost

This setting is used if the function is to start defrosts on its own initiative. The setting can ideally be used in refrigeration/ frost rooms where the time of defrost is not as important. In refrigeration/frost rooms, this setting can ensure major savings as defrosts take place only when necessary.  Scheduled defrosts will always be carried out. That is to say, a basic schedule can be input and the adaptive function will then start extra defrosts itself where necessary..

###### Minimum time between defrosts

It is possible to enter a minimum time between defrosts. In this way it can be avoided that planned defrosts according to the weekly schedule be carried out immediately after the termination of a adaptive defrost. The time span is from the termination of a adaptive defrost and until a planned defrost is again allowed.

This function can only cancel planned defrosts which start from a defrost schedule – either an internal schedule or an external

90

###### Documentation on saving

It is possible to read the number of planned defrosts and the number of cancelled defrosts.

###### Alarms

###### • Appliance not defrosted

If this function detects ice formation shortly after defrost, the "Appliance not defrosted" alarm is generated. This error may be due to the evaporator not being defrosted correctly as a consequence of faults in heating elements or fans. After this alarm, the function will not cancel defrosts.

This alarm is removed at the start of the next defrost, at which point cancellation of defrosts will be permitted again.

###### • Air flow reduced

If this function detects severe ice formation on the evaporator, the alarm "Appliance X – air flow reduced" is transmitted. This error will typically be due to severe ice formation on the evaporator, but it may also be due to reduced air flow as a consequence of severe over stacking of goods or dropout of fans. After this alarm, the function will not cancel defrosts. This alarm is removed at the start of the next defrost, at which point cancellation of defrosts will be permitted again.

###### • Sensor error

The controller cannot carry out a tuning calculation for use in the adaptive defrosting.

After this alarm, the function will not cancel defrosts. This alarm is removed at the start of the next defrost, at which point cancellation of defrosts will be permitted again.

###### • Flash gas alarm

This function will monitor whether there is any flash gas at the expansion valve. If flash gas is detected over a fairly long period, the alarm "Appliance X – Flash gas alarm" is triggered. This alarm is removed when flash gas disappears or at the start of the next defrost.

###### • Valve

The function is suitable for application of a valve from Danfoss. Valves from other manufacturers is not recommended.

91

#### **Miscellaneous**

###### **Alarm priorities**

The different alarms that can be generated by the controller can be given a priority.

“priority” will activate the alarm relay if it has been so defined. The alarms are entered in the alarm log and also transmitted to the data communication if connected.

The “Log only” priority will as mentioned only be entered in the

alarm log.

|**Setting**|**Log**||**Selecti**|**on Alarm relay**||**Grid**|**AKM-**|
|---|---|---|---|---|---|---|---|
|||Non|High|Low - Mid-<br>dle|Low -<br>High|**work**|**dest.**|
|High|X||X||X|X|1|
|Medium|X|||X|X|X|2|
|Low|X|||X|X|X|3|
|LogOnly|X|||||||
|Disabled||||||||

###### **Sensor correction**

The input signal from all connected sensors can be corrected. A correction will only be necessary if the sensor cable is long and has a small cross-sectional area. All displays and functions will reflect the corrected value.

###### **Clock function**

The controller contains a clock function, that can be used together with schedules for defrost and day/night operation. In the event of a power failure, the time setting will be remembered for at least 12 hours

If the controller is linked up to a System Manager via the data communication, the System Manager will reset the clock.

###### **Signals via data communication**

The controller contains a number of functions that can be activated/overridden by the network’s system unit:

###### Night operation

The day/night operation of the individual controllers can be controlled from a central weekly schedule in the system unit.

###### Interruption of injection

The system unit can ensure that all appliance and room controllers force-close their valves if all compressors in the belonging central plant stop due to operation breakdowns and are prevented from starting again.

###### Forced refrigeration

The controller will undertake refrigeration when this signal is received. Refrigeration will continue until the signal is removed. The function will ignore the thermostat function, but forced cooling will be stopped if there is a low temperature alarm.  (If a setting means that forced cooling and defrosting are required at the same time, defrosting will have the higher priority.)

###### **Display signal**

The air temperatures measured at the evaporator can be read from a display. This display must be of display type EKA 163B or EKA 164B. The display is normally mounted on the appliance so that the customer can see the air temperature. Up to four displays per controller can be fitted.

Connection is effected by means of wires with plug connectors. The display can be placed on an appliance front, for example. When a display with operating buttons is selected, the unit can be operated with ease by means of a menu system as well as displaying temperatures and operating situations.

###### Display signal

Temperature display can be selected for a product sensor, or alternatively a weighted condition between air sensors S3 and S4. Setting is expressed as a percentage of the S4 signal. The display is independent of the thermostat function. An Offset can be set for the display.

Values are displayed by means of three digits, and one setting allows you

to decide whether the temperature is to be displayed in °C or °F.

###### LEDs on the front

The LEDs will come on when the associated relay is activated: 2nd LED = refrigeration 3rd LED = defrost 4th LED = ventilator operational

The LEDs will flash when an alarm has been triggered. In this situation, you can call up the error code on the display by briefly pressing the top button. At the same time, any alarm relays will be deactivated.

###### Light control

In appliance controllers the light can be controlled via a central weekly schedule in the system unit.

###### Coordinated defrost

Several appliance controllers can be grouped in the system unit so that they will start a defrost at the same time and subsequently start up after defrost at the same time.

###### Adaptive defrosting

By using the "Adaptive Defrosting" function the controller must receive a condensing pressure signal Pc. This signal must be received from the System Manager.

###### Optimization of suction pressure

The appliance/room controllers can supply the necessary information to the system unit so that it can optimise the suction pressure based on the appliance with the heaviest load.

###### The buttons

When you want to change a setting, the top and bottom buttons will give a higher or a lower value depending on which button you press. Before you can change the value, you must access the menu. This is done by holding down the top button for a couple of seconds; this takes you into the list of parameter codes. Find the parameter code you want to change, then press the centre button to display the parameter value. When you have changed this value, save the new value by pressing the centre button again

###### Examples:

Setting a menu

1. Press the top button to display a parameter

2. Press the top or bottom button and find the parameter you want to set

3. Press the centre button to display the value

92

4. Press the top or bottom button and set the new value

5. Press the centre button again to save the value.

Read the temperature at the defrost sensor)

- Briefly press the bottom button

Manual start or stop of defrost

- Press the bottom button for 4 seconds.

###### Read codes

Normally the selected temperature signal can be read from the display, but under certain conditions the display may show other codes in order to notify the user of various operating states.

|Function|Display read|
|---|---|
|Main switch|When the "main switch" is set to OFF, the display will<br>read "OFF"|
|Defrost|During defrost, the display will read "-d-".<br>The display will switch to normal temperature display<br>when the thermostat temperature is in place, but not<br>until after the delay period “Max. Disp. -d- delay”.|
|Case clean-<br>ing|When appliance cleaning is activated, the display will<br>read "Fan" to indicate that the fans are running in order<br>to defrost the evaporator. When the second stage of ap-<br>pliance cleaning is activated, the display reads "OFF" in<br>order to indicate that the appliance can now be cleaned<br>as all outputs are in standby position.|
|PAS|Requirement for access code. If operation of the display<br>is to be protected by an access code, both the defini-<br>tion and the access code must be set in the controllers'<br>authorisation menu for the local display (LOCD).|
|Alarm|The three LED's will flash if an alarm is triggered. The<br>alarm code can be viewed by pressing the top button.|
|CO2|FLASHING. There is a signal from a refrigerant leak<br>sensor|
|- - -|When three dashes appear, the valid temperature read-<br>ing is faulty (sensor switched off or short-circuited), or<br>else the display has been deactivated.|
|th1/th2|When the thermostat bank is changed by pressing a<br>button, the display will display for 10 seconds which<br>thermostat band is active.|
|AL 1|Alarm from section A. 2=B. etc.|
|- - 1<br>- - 2|Initiation, Display is connected to output A<br>Output B. etc.|

###### Get off to a good start when use of display

The following procedure will start regulation as quickly as possible:

1. Open parameter r12 and stop regulation (in a new appliance not set previously, r12 will already be set to 0, which means regulation stopped)

2. Open parameter o93 and set the configuration lock to a value of 0 (=OFF)

3. Open parameter 062 = Select a predefined use on the basis of the electrical connections which appear at the end of the manual. After configuration of this function, the controller will shut down and restart.

4. Once the controller has restarted, open parameter 093 and the configuration lock is opened = value 0.

###### Menu overview:

A display can be connected for each evaporator section. In each display, the following settings/readings can be undertaken for the evaporator section in question.

|Paramet<br>name|er<br>Function<br>A|t start-<br>up|
|---|---|---|
|r12|Main switch:<br>0: Controller stopped<br>1: Regulation|x|
|r22|Select thermostat band:<br>1 = Thermostat band 1 is active<br>2 = Thermostat band 2 is active||
|r37|Setting of cut-out value for the thermostat in section<br>A/B/C/D||
|r38|Setting of cut-out value for thermostat band 2||
|o30|Setting of refrigerant (must be set if AKV / stepper<br>valves are used)<br>0= not selected, 1=R12. 2=R22. 3=R134a. 4=R502.<br>5=R717. 6=R13. 7=R13b1. 8=R23. 9=R500. 10=R503.<br>11=R114. 12=R142b. 13=User def. 14=R32. 15=R227.<br>16=R401A. 17=R507. 18=R402A. 19=R404A.<br>20=R407C. 21=R407A. 22=R407B. 23=R410A.<br>24=R170. 25=R290. 26=R600. 27=R600a. 28=R744.<br>29=R1270. 30=R417A. 31=R422A. 32=R413A.<br>33=R422D. 34=R427A. 35=R438A. 36=R513A.<br>37=R407F. 38=R1234ze. 39=R1234yf. 40=R448A.<br>41=R449A. 42=R452A.|x|
|o46|Case cleaning function. Set:<br>0: Case cleaning not started<br>1: Only fan running (evaporator defrost)<br>2: All outputs are OFF (cleaning may be carried out)||
|P81|Selection of pre-set application group:<br>1= group 1: o62 + page 98-101<br>2= group 2: o62 + page 102-105|x|
|o62|(P81 must be set before o62 can be set)<br>Selection of predefined configuration.<br>This setting will give a choice from a series of prede-<br>fined combinations, which at the same time establish<br>the connection points.<br>At the end of the manual there is an overview of the<br>options and connection points.<br>After configuration of this function, the controller will<br>shut down and restart.|x|
|o93|Configuration lock<br>You can only select a preset configuration or change<br>refrigerant when the configuration lock is open.<br>0 = Configuration open<br>1 = Configuration locked|x|
|u17|Actual air temperature for the thermostat in section<br>A/B/C/D||
|u20|Actual temperature at S2 sensor. Section A/B/C/D||
|u21|Actual superheat. Section A/B/C/D||
|u24|AKV valve opening degree. Section A/B/C/D||
|u26|Actual evaporating temperature. Section A/B/C/D||
|u36|Actual air temperature for product sensor in section<br>A/B/C/D||
|u68|Actual air temperature for alarm thermostat in sec-<br>tion A/B/C/D||

5. If AKV (stepper) valves are used, you must also select refrigerant via parameter o30.

6. Open parameter r12 and start regulation.

7. When there is a network: set the address for the address switch in the controller.

X = When the controller is not set up, the display will only read the marked settings

8. Send this address to the system unit by activating a service pin.

93

###### **Stepper Motor Valves**

###### **AKS 32R info**

When selecting a Danfoss stepper motor valve, all settings are factory set. Here, it is only necessary to select the type of valve. If a valve from other manufacturers is used the following settings has to be made. Get data from the valve manufacturer:

###### Max Operating Steps.

The number of steps that correspond to a valve position of 100%. This value is limited to a range of 0 - 10,000 steps.

###### Hysteresis

The number of steps needed to correct for mechanical hysteresis when a reduction gear is part of the valve design. This adjustment is only applied, if an additional opening of the valve is requested.

The signal from one pressure transmitter can be received from up to 5 controllers

If this is the case the valve opens an additional amount equal to this value, before driving the valve in the closing direction by this same value.

This value is limited to 0 – 127 steps.

###### Step Rate

###### **Graphic display MMIGRS2**

The desired valve drive rate in steps per second. This value is limited to 20 – 500 steps / sec.

###### Holding Current

The percent of the programmed Max Phase Current that should be applied to each phase of the stepper output when the valve is stationary.  If required, this current ensures that the valve maintains its last programmed position.  This value is limited to a range of 0 – 70% given in 10% steps.

###### Overdrive at Valve Init

During valve initialization, the amount to overdrive the valve, beyond the 0% position, to ensure that the valve has fully closed. This value is limited to a range of 0 - 31%.

###### Phase Current

The current applied to each phase of the stepper motor during actual valve movement.  This value is limited to 7 bits and a range of 0 – 325 mA given in 10ma steps. Verify the range against the stepper valve controller in the actual design. Please be aware, that this value hat to be set in a RMS value. Some valve manufacturers are using peak current!

A display gives access to most of the controller functions . For access, connect the display to the controller and activate the address on MMIGRS2. (A separate power supply does **not** need to be connected) Power is supplied directly from the controller via the cable.

###### Setting:

- 1.Press both the "x" and "enter" buttons and hold in for 5 seconds. The BIOS menu is then displayed.

2. Select the "MCX selection" line and press "enter"

3. Select the "Man selection" line and press "enter"

4. The address will be displayed. Check that it is 001, press "enter". Data will then be collected from the controller.

###### Soft Landing after Valve Init

At power on the valve is performing a valve Initialization i.e. closing the valve  with “Max Operating Steps” plus “Overdrive At Valve Init “steps to generate a zero point calibration of the system . Hereafter a “Soft landing after Valve Init” is made to  minimize the closing force on the valve seat with a few opening steps according to setting of  “Hysteresis” or  min 20 steps

###### Failsafe Position

During failsafe mode of operation (e.g., resulting from a loss of communications to this module), specifies the default valve position.  This value is limited to a range of 0 – 100%.

###### **Light-emitting diodes on the controller**

*[Figurtekst: Internal communication · between the modules: · Quick flash = error · Constantly On = error · Status of output 1-8 · Slow flash = OK · Quick flash = answer from gateway · ■ Power remains on for 10 mins after network · ■ Comm registration · ■ DO1  ■ Status Constantly ON = error · ■ DO2  ■ Service Tool Constantly OFF = error · ■ DO3  ■ LON External communication · ■ DO4  ■ I/O extension Communication to AK-CM 102 · ■ DO5  ■ Alarm · ■ DO6 Flash = active alarm/not acknowledged · ■ DO7  ■ Display Constant ON = Active alarm/acknowledged · ■ DO8  ■ Service Pin · Network installation]*

94

#### **Information**

The controller offers quite a number of status displays which are invaluable in connection with operational start-up and optimisation.

###### **Thermostat function**

Display of S3 air admission Display of S4 air emission Display of weighted S3/S4 thermostat temperature Min., Max. and Average thermostat temperature / 24 hours Average thermostat coupling in % / 24 hours Running time for cutin period in progress or for the last cutin period

###### **Alarm thermostat**

Display of weighted S3/S4 alarm temperature Min., Max. and Average alarm temperature / 24 hours Percentage of time where the alarm temperature was outside the limits / 24 hours

###### **Product sensor**

Display of the temperature at the product sensor Min., Max and Average of product temperature / 24 hours Percentage of time where the product temperature was outside the limits / 24 hours

###### **Injection function**

AKV /ETS/CCMT opening degree in % Average opening degree / 24 hours Evaporating pressure S2 gas temperature Superheat Superheat reference

###### **Input and output status**

Status display of all inputs and outputs Manual overriding of all outputs

NB: Not all displays are available via AKM – Cf. the AKM menu description for further details.

###### **Regulating  status**

The controller goes through some regulating situations. You can see the actual situation here. When operating with AK-ST the text is written on the screen for the section. When operating from AKM the operating status is a numerical value. The values are, as follows: 0: Refrigeration stopped from Main Switch 1: Start-up phase for the injection function 2: Adaptive regulation of the superheat 3: - 4: Defrost 5: Start-up after defrost 6: Forced closing 7: Injection function failure 8: Sensor error and emergency refrigeration 9: Modulating thermostat control 10: Melting function is active 11: Open door 12: Case cleaning 13: Thermostat cutout 14: Forced refrigeration 15: Shut down

Defrost state

###### **Defrost**

Actual defrost status Degree of icing-up of evaporator Duration of on-going or last defrost Average duration of the last ten defrosts Duration of cooling-down after defrost Defrost sensor temperature Number of planned and skipped defrosts

###### **Compressor**

Operating time last 24 hours Total operating time Number of couplings last 24 hours Total number of couplings

###### **Door contact**

Door contact status Duration of last opening Number of openings last 24 hours Opening time last 24 hours

###### **Rail heat**

Dew point Actual duty cycle

During and immediately after a defrost the defrost status will be: 1: Evaporator is emptied 3: Defrost 5: Evaporating pressure is lowered 6: The liquid injection is delayed 7: Fan delay

###### **Installation  considerations**

Accidental damage, poor installation, or site conditions, can give rise to malfunctions of the control system, and ultimately lead to a plant breakdown.

Every possible safeguard is incorporated into our products to prevent this. However, a wrong installation, for example, could still present problems. Electronic controls are no substitute for normal, good engineering practice.

Danfoss will not be responsible for any goods, or plant components, damaged as a result of the above defects. It is the installer’s responsibility to check the installation thoroughly, and to fit the necessary safety devices.

Particular attention is drawn to the need for a “force closing” signal to controllers in the event of compressor stoppage, and to the requirement for suction line accumulators.

Your local Danfoss agent will be pleased to assist with further advice, etc.

###### **Appliance cleaning**

Time of last cleaning Duration of last cleaning

The controller is not built for use on plate heat exchangers.

###### NH3 + AKVA

Please contact Danfoss if you require help concerning the positioning of sensors, transmitters, etc.

95

#### **Alarm texts**

|**Setting of priority**|**Default**<br>**priority**|**Alarm text**|**Description**|
|---|---|---|---|
|**Temperature alarms**||||
|High air temp. A|High|High air temp. (A,B,C,D)|The air temperature has been above the high alarm limit for longer time than set delay|
|Low air temp. A|High|Low air temp. (A,B,C,D)|The air temperature has been below the low alarm limit for longer time than set delay|
|Frost protect A|High|Frost protection, too low S4<br>(A,B,C,D)|The air off temperature (S4) is below the set frost protection limit|
|High Prod. temp. A|High|High Prod. temp. (A,B,C,D)|The product temperature has been above the high alarm limit for longer time than set delay|
|Low prod. temp. A|High|Low prod. temp. (A,B,C,D)|The product temperature has been below the low alarm limit for longer time than set delay|
|Same for B,C,D||||

###### **Sensor errors**

|Pe sensor error|Low|Po sensor error|Pressure transmitter signal for evaporating pressure faulty|
|---|---|---|---|
|S2A sensor error|High|S2A sensor error (B,C,D)|S2A temp. sensor signal faulty|
|S3A sensor error|High|S3A sensor error (B,C,D)|S3A temp. sensor signal faulty|
|S4A sensor error|High|S4A sensor error (B,C,D)|S4A temp. sensor signal faulty|
|S5-1A sensor error|High|S5-1A sensor error (B,C,D)|S5-1A temp. sensor signal faulty|
|S5-2A sensor error|High|S5-2A sensor error (B,C,D)|S5-2A temp. sensor signal faulty|
|Prod. sensor error A|High|Product temp. A sensor error<br>(B,C,D)|Product temp. sensor signal faulty|
|Same for B,C,D||||
|Saux1 sensor error|High|Saux1 sensor error|Saux1 temp. sensor signal faulty|
|Saux2 sensor error|High|Saux2 sensor error|Saux2 temp. sensor signal faulty|
|Saux3 sensor error|High|Saux3 sensor error|Saux3 temp. sensor signal faulty|
|Saux4 sensor error|High|Saux4 sensor error|Saux4 temp. sensor signal faulty|
|Pc sensor error|High|Pc sensor error|Pressure transmitter signal  for condensing pressure faulty|
|Paux1 sensor error|High|Paux1 sensor error|Paux1 pressure transmitter  signal faulty|
|Paux2 sensor error|High|Paux2 sensor error|Paux2 pressure transmitter  signal faulty|
|Paux3 sensor error|High|Paux3 sensor error|Paux3 pressure transmitter  signal faulty|

|**Various alarms**||||
|---|---|---|---|
|Standby mode|Medium|Control stopped,<br>MainSwitch=OFF|The control has been stopped via the setting ”Main switch” = ON or via the external Main switch input|
|Refrigerant changed|Low|Refrigerant changed|The refrigerant setting has been changed|
|Refrigerantleak alarm||Refrigerant leak|A signal is being received from a leak detector<br>(The alarm relay on AK-CC 750A will not be activated)|
|Case cleaning|High|Case cleaning initiated|A case cleaning has been initiated|
|Door open pre alarm|Low|Door open pre alarm|The door has been open for longer time than 75% of the set alarm delay|
|Door open alarm|Medium|Door open alarm|The door has been open for longer time than set alarm delay|
|Injection problem A, B, C, D|Medium|Injection problem (A,B,C,D)|The AKV valve can not control the superheat of the evaporator|
|Max def period A,B,C,D|Low|Max defrost time exceeded<br>(A,B,C,D)|The last defrost cycle has terminated on time instead of temperature|
|Max fan del exceeded<br>A,B,C,D|Low|Max fan del ay time exceeded<br>(A,B,C,D)|The fans have been started on time instead of temperature after a defrost|
|Max hold time A,B,C,D|Low|Max defrost hold time<br>(A,B,C,D)|After a defrost cycle the evaporator has restarted cooling as it did not get a release signal via the defrost co-<br>ordination setup in the network manager (AKA gateway)|
|Air flow alarm A,B,C,D|Low|AD - Case X - Air flow reduced|The air flow at the evaporator is greatly reduced – either as a consequence of severe ice formation, a fan fault or<br>other obstruction.|
|AD – Case A not defrosted<br>(B,C,D)|Low|AD - Case X not defrosted|The air flow is continuously reduced after defrost has been carried out|
|AD – Fault case A,B,C,D|Low|AD - Sensor error A,B,C,D|Tuning problem in adaptive defrost|

96

|AD – Flash gas evapora.<br>A,B,C,D|Low|AD – Flash gas detect A,B,C,D|Flash gas has been detected at the valve for a relatively long time|
|---|---|---|---|
|**General alarms**||||
|Thermostat x – Low temp.<br>alarm|Low|Thermostat x - Low alarm|The temperature for thermostat no. x has been below the low alarm limit for longer time than set delay|
|Thermostat x – High temp.<br>alarm|Low|Thermostat x - High alarm|The temperature for thermostat no. x has been above the high alarm limit for longer time than set delay|
|Pressostat x – Low pressure<br>alarm|Low|Pressostat x - Low alarm|The pressure for pressostat no. x has been below the low alarm limit for longer time than set delay|
|Pressostat x – High pressure<br>alarm|Low|Pressostat x - High alarm|The pressure for pressostat no. x has been above the high alarm limit for longer time than set delay|
|Voltage input x – Low alarm|Low|Analog input x - Low alarm|The voltage signal has been below the low alarm limit for longer time than set delay|
|Voltage input x – High alarm|Low|Analog input x - High alarm|The voltage signal has been above the high alarm limit for longer time than set delay|
|DIx alarm input|Low|DIx alarm|Alarm on general  alarm input DI x|
|Stepper valve|High|Stepper - Inj. A, B, C. D.<br>Open coil, Shorted output,<br>Error, Power failure|Check supply to the actual valve|

###### **System alarms**

|The alarm priority can not be altered on syste|m alarms||
|---|---|---|
|Medium|Clock has not been set|Time has not been set|
|Medium|System Critical exception|A unrecoverable critical system failure has occurred – exchange the controller|
|Medium|System alarm exception|A minor system failure has occurred – power off controller|
|Medium|Alarm destination disabled|When this alarm is activated the alarm transmission to the alarm receiver has been deactivated.<br>When the alarm is cleared the alarm transmission to the alarm receiver has been activated.|
|Medium|Alarm route failure|Alarms can not be transmitted to alarm receiver – check communication|
|High|Alarm router full|The internal alarm buffer has an overrun – this might occur if the controller can not send the alarms to the alarm<br>receiver. Check communication between controller and AKA gateway.|
|Medium|Device is restarting|The controller is restarting after flash updating of the software|
|Medium|IO module error|There is a communication fault between the controller module and the extension modules – the fault must be cor-<br>rected as soon as possible|
|Low|Manual override IO|The input/ output in question has been put in manual control mode via the AK-ST 500 service tool software|

97

#### **Appendix - Recommended connection Group 1**

The controller has a setting where you can choose between various types of installation. If you use these settings, the controller will suggest a series of connection points for the different functions. These points are shown below.

Even if your installation is not 100% as described below, you can still use the function. After use, you need only adjust the divergent settings.

The given connection points in the controller can be changed if you wish.

###### **Room**

|**Appl.**|**No. of**|**Def.**|**Air**|**Cont**|**roller -**|**(Mod**|**ule no.**|**1 poin**|**t 1-19)**|||||||||||
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**type**|**AKV**|**type**|**sensor**|AI1|AI2|AI3|AI4|AI5|AI6<br>AI7|AI8|AI9|AI10|AI11|DO1|DO2|DO3|DO4|DO5|DO6|
|||||**pt1**|**pt2**|**pt3**|**pt4**|**pt5**|**pt6**<br>**pt 7**|**pt8**|**pt 9**|**pt10**|**pt 11**|**pt 12**|**pt 13**|**pt 14**|**pt 15**|**pt 16**|**pt 17**|
|Room|1|Air|S3|S2A|S3A|||||For. cl.|Door|Main s.|Po|AKV A|||Light|Rail heat|Comp.|
|Room|1|El|S3|S2A|S3A||S5A|||For. cl.|Door|Main s.|Po|AKV A|Def.||Light|Rail heat|Comp.|
|Room|1|Gas|S3|S2A|S3A||S5A|||For. cl.|Door|Main s.|Po|AKV A|Def.|Drain|Suction|Rail heat|Comp.|
|Room|2|Air|S3|S2A|S3A|S2B||||For. cl.|Door|Main s.|Po|AKV A|AKV B||Light|Rail heat|Comp.|
|Room|2|El|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Rail heat|Comp.|
|Room|2|El|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Light|Comp.|
|Room|2|Gas|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
|Room|2|Gas|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Suction|Comp.|
|Room|3|Air|S3|S2A|S3A|S2B||S2C||For. cl.|Door|Main s.|Po|AKV A|AKV B|AKV C|Light|Rail heat|Comp.|
|Room|3|El|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
|Room|3|Gas|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
|Room|4|Air|S3|S2A|S3A|S2B||S2C|S2D|For. cl.|Door|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Rail heat|Comp.|
|Room|4|El|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
|Room|4|Gas|S3|S2A|S3A||S5A|S2B|S5B|For. cl.|Door|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|

98

|||||||||||||**Mo**|**dule 2= A**|**K-XM 20**|**5)**||||||**App.no a**<br>|**t setting**<br>|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|DO7|DO8|AI1|A|I2|A|I3|A|I4|AI5|AI6|AI7|AI8|DO1|DO2|DO3|DO4|DO5|DO6|DO7|DO8|**via AKM**|**or display**|
|**pt 18**|**pt 19**|**pt1**|**p**|**t2**|**p**|**t3**|**p**|**t4**|**pt5**|**pt6**|**pt 7**|**pt8**|**pt 9**|**pt10**|**pt 11**|**pt 12**|**pt 13**|**pt 14**|**pt 15**|**pt 16**|**High**<br>**temp.**|**Low**<br>**temp.**|
|Fan|Alarm||||||||||||||||||||1||
|Fan|Alarm||||||||||||||||||||2|3|
|Fan|Alarm||||||||||||||||||||4|5|
|Fan|Alarm||||||||||||||||||||6||
|Fan|Alarm||||||||||||||||||||7|8|
|Fan|Alarm||||||||||||||||||||47|48|
||||||||||||||Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light||10|12|
|Fan|Alarm||||||||||||||||||||9|11|
|Fan|Alarm||||||||||||||||||||13||
|Def. C|||||||||||||Rail heat|Comp.|Fan|Alarm|||Light||14|15|
|Def. C||S2C|||||S|5C|||||Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light||16|17|
|Fan|Alarm||||||||||||||||||||18||
|Def. C|Def. D|S2C|||||S|5C|S2D|||S5D|Rail heat|Comp.|Fan|Alarm|||||19|20|
|Def. C|Def. D|S2C|||||S|5C|S2D|||S5D|Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light||21|22|

99

###### **Cases**

|**Appl.**<br>|**No. of**<br>|**Def.**<br>|**Air**<br>|**Cont**|**roller -**|**(Mod**|**ule no.**|**1 poin**|**t 1-19)**||||||||||||
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**type**|**AKV**|**type**|**sensor**|AI1|AI2|AI3|AI4|AI5|AI6|AI7|AI8|AI9|AI10|AI11|DO1|DO2|DO3|DO4|DO5|DO6|
|||||**pt1**|**pt2**|**pt3**|**pt4**|**pt5**|**pt6**|**pt 7**|**pt8**|**pt 9**|**pt10**|**pt 11**|**pt 12**|**pt 13**|**pt 14**|**pt 15**|**pt 16**|**pt 17**|
||1|Air|S3 + S4|S2A|S3A|S4A||||||For. cl.|Main s.|Po|AKV A||Light||Rail heat|Comp.|
||1|Air|S3 + S4|S2A|S3A|S4A|||||Blinds|For. cl.|Main s.|Po|AKV A||Light|Blinds|Rail heat|Comp.|
||1|El|S3 + S4|S2A|S3A|S4A|S5A|||||For. cl.|Main s.|Po|AKV A|Def. A|Light||Rail heat|Comp.|
|2 evap.|1|El|S3 + S4|S2A|S3A|S4A|S5-1A|S5-2A|S6A|||For. cl.|Main s.|Po|AKV A|Def. A|Light||Rail heat|Comp.|
||1|El|S3 + S4|S2A|S3A|S4A|S5A||||Blinds|For. cl.|Main s.|Po|AKV A|Def. A|Light|Blinds|Rail heat|Comp.|
|CO2|1|El|S3 + S4|S2A|S3A|S4A|S5A|||||For. cl.|Main s.|Po|AKV A|Def. A|Light||Rail heat|Comp.|
|CO2<br>2 evap.|<br>1|El|S3 + S4|S2A|S3A|S4A|S5-1A|S5-2A|S6A|||For. cl.|Main s.|Po|AKV A|Def. A|Light||Rail heat|Comp.|
||1|Gas|S3 + S4|S2A|S3A|S4A|S5A|||||For. cl.|Main s.|Po|AKV A|Def.|Drain|Suction|Rail heat|Comp.|
||1|Gas|S3 + S4|S2A|S3A|S4A|S5A|||||For. cl.|Main s.|Po|AKV A|Def.|Drain|Suction|Light|Comp.|
||1|Gas|S3 + S4|S2A|S3A|S4A|S5A|||||For. cl.|Main s.|Po|AKV A||||Def.||
||2|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B||For. cl.|Main s.|Po|AKV A|AKV B|Light||Rail heat|Comp.|
||2|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B|Blinds|For. cl.|Main s.|Po|AKV A|AKV B|Light|Blinds|Rail heat|Comp.|
||2|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Rail heat|Comp.|
||2|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Light|Comp.|
|2 evap.|2|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
||2|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
|CO2|2|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Rail heat|Comp.|
|CO2|2|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
|CO2<br>2 evap.|<br>2|El|S3 + S4|S2A|S3A|S4A|S5-1A|S2B|S3B|S4B|S5-1B|For. cl.|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
||2|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|Def. A|Def. B|Suction|Comp.|
||2|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
||2|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|||Def. A|Def. B|
||3|Air|S3 + S4|S2A|S3A|S4A|S2B|S3B|S4B|S2C|S3C|S4C|Main s.|Po|AKV A|AKV B|AKV C|Light|Rail heat|Comp.|
||3|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B||For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Rail heat|Comp.|
||3|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B|Blinds|For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Rail heat|Comp.|
||3|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
||3|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
|CO2|3|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
||3|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
||3|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C||Def. A|Def. B|
||4|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B||For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Rail heat|Comp.|
||4|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B|Blinds|For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Rail heat|Comp.|
||4|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
||4|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
|CO2|4|El|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
||4|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
||4|Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B||For. cl.|Main s.|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|

100

|||||||||||**Mo**|**dule 2= A**|**K-XM 20**|**5)**||||||**App.no a**<br>|**t setting**<br>|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|DO7|DO8|AI1|A|I2|AI3|AI4|AI5|AI6|AI7|AI8|DO1|DO2|DO3|DO4|DO5|DO6|DO7|DO8|**via AKM**|**or display**|
|**pt 18**|**pt 19**|**pt1**|**p**|**t2**|**pt3**|**pt4**|**pt5**|**pt6**|**pt 7**|**pt8**|**pt 9**|**pt10**|**pt 11**|**pt 12**|**pt 13**|**pt 14**|**pt 15**|**pt 16**|**High**<br>**temp.**|**Low**<br>**temp.**|
|Fan|Alarm||||||||||||||||||23||
|Fan|Alarm||||||||||||||||||69||
|Fan|Alarm||||||||||||||||||24|25|
|Fan|Alarm|||||||||||||||||||52|
|Fan|Alarm||||||||||||||||||65||
|Fan|Alarm|||||||||||||||||||54|
|Fan|Alarm|||||||||||||||||||59|
|Fan|Alarm||||||||||||||||||26|27|
|Fan|Alarm||||||||||||||||||45|46|
|||||||||||Blinds|Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light|Blinds||61|
|Fan|Alarm||||||||||||||||||28||
|Fan|Alarm||||||||||||||||||70||
|Fan|Alarm||||||||||||||||||29|30|
|Fan|Alarm||||||||||||||||||49|50|
|||S6A|S|6B|||S5-2A|S5-2B|||Rail heat|Comp.|Fan|Alarm|||Light|||53|
|||||||||||Blinds|Rail heat|Comp.|Fan|Alarm|||Light|Blinds|66||
|Fan|Alarm|||||||||||||||||||55|
||||||||||||Rail heat|Comp.|Fan|Alarm|||Light|||56|
|||S6A|S|6B|||S5-2A|S5-2B|||Rail heat|Comp.|Fan|Alarm|||Light|||60|
|Fan|Alarm||||||||||||||||||31|33|
||||||||||||Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light||32|34|
|||||||||||Blinds|Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light|Blinds|62||
|Fan|Alarm||||||||||||||||||35||
|Fan|Alarm|S2C|S|3C|S4C||||||||||||Light||51||
|Fan|Alarm|S2C|S|3C|S4C||||||||||||Light|Blinds|71||
|Def. C||S2C|S|3C|S4C|S5C|||||Rail heat|Comp.|Fan|Alarm|||Light||36|37|
|Def. C||S2C|S|3C|S4C|S5C||||Blinds|Rail heat|Comp.|Fan|Alarm|||Light|Blinds|67||
|Def. C||S2C|S|3C|S4C|S5C|||||Rail heat|Comp.|Fan|Alarm|||Light|||57|
|Def. C||S2C|S|3C|S4C|S5C|||||Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light||38|39|
|Def. C||S2C|S|3C|S4C|S5C||||Blinds|Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light|Blinds|63||
|Fan|Alarm|S2C|S|3C|S4C||S2D|S3D|S4D||||||||Light||40||
|Fan|Alarm|S2C|S|3C|S4C||S2D|S3D|S4D||||||||Light|Blinds|72||
|Def. C|Def. D|S2C|S|3C|S4C|S5C|S2D|S3D|S4D|S5D|Rail heat|Comp.|Fan|Alarm|||Light||41|42|
|Def. C|Def. D|S2C|S|3C|S4C|S5C|S2D|S3D|S4D|S5D|Rail heat|Comp.|Fan|Alarm|||Light|Blinds|68||
|Def. C|Def. D|S2C|S|3C|S4C|S5C|S2D|S3D|S4D|S5D|Rail heat|Comp.|Fan|Alarm|||Light|||58|
|Def. C|Def. D|S2C|S|3C|S4C|S5C|S2D|S3D|S4D|S5D|Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light||43|44|
|Def. C|Def. D|S2C|S|3C|S4C|S5C|S2D|S3D|S4D|S5D|Rail heat|Comp.|Fan|Alarm|Suction|Drain|Light|Blinds|64||

101

#### **Appendix - Recommended connection Group 2**

The controller has a setting where you can choose between various types of installation. If you use these settings, the controller will suggest a series of connection points for the different functions. These points are shown below.

Even if your installation is not 100% as described below, you can still use the function. After use, you need only adjust the divergent settings.

The given connection points in the controller can be changed if you wish.

###### **AKV valves**

|**Appl.**<br>|**No.**<br>|**Def.**<br>|**Air**<br>|**Contr**|**oller - (**|**Mod**|**ule no.**|**1 poin**|**t 1-19)**||||||||||||
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**type**|**of**<br>**AKV**|**type**|**sensor**|AI1|AI2|AI3|AI4|AI5|AI6|AI7|AI8|AI9|AI10|AI11|DO1|DO2|DO3|DO4|DO5|DO6|
|||||**pt1**|**pt2**|**pt3**|**pt4**|**pt5**|**pt6**|**pt 7**|**pt8**|**pt 9**|**pt10**|**pt 11**|**pt 12**|**pt 13**|**pt 14**|**pt 15**|**pt 16**|**pt 17**|
|Room|1|Air|S3A + S4A|S2A|S3A|S4A|||||||Door|Po|AKV A|||||Rail heat|
|||EL|S3A + S4A|S2A|S3A|S4A|S5A||||||Door|Po|AKV A|Def.||||Rail heat|
|||Gas|S3A + S4A|S2A|S3A|S4A|S5A||||||Door|Po|AKV A|Def.|Suction|Drain||Rail heat|
||2|Air|S3A + S4A|S2A|S3A|S4A||S2B|||||Door|Po|AKV A|AKV B||||Rail heat|
|||EL|S3A + S4A|S2A|S3A|S4A|S5A|S2B|S5B||||Door|Po|AKV A|AKV B|Def. A|Def. B||Rail heat|
|||Gas|S3A + S4A|S2A|S3A|S4A|S5A|S2B|S5B||||Door|Po|AKV A|AKV B|Def. A|Def. B|Suction|Drain|
||3|Air|S3A + S4A|S2A|S3A|S4A||S2B||S2C|||Door|Po|AKV A|AKV B|AKV C|||Rail heat|
|||EL|S3A + S4A|S2A|S3A|S4A|S5A|S2B|S5B|S2C|S5C||Door|Po|AKV A|AKV B|AKV C|Def. A|Def. B|Def. C|
|||Gas|S3A + S4A|S2A|S3A|S4A|S5A|S2B|S5B|S2C|S5C||Door|Po|AKV A|AKV B|AKV C|Def. A|Def. B|Def. C|
||4|Air|S3A + S4A|S2A|S3A|S4A|S2B||S2C||S2D||Door|Po|AKV A|AKV B|AKV C|AKV D||Rail heat|
|||EL|S3A|S2A|S3A|S5A|S2B|S5B|S2C|S5C|S2D|S5D|Door|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
|||Gas|S3A|S2A|S3A|S5A|S2B|S5B|S2C|S5C|S2D|S5D|Door|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
|Case|1|Air|S3 +S4|S2A|S3A|S4A||||||Clean|Blinds|Po|AKV A||||Blinds|Rail heat|
|||EL|S3 + S4|S2A|S3A|S4A|S5A|||||Clean|Blinds|Po|AKV A|Def.|||Blinds|Rail heat|
|||Gas|S3 + S4|S2A|S3A|S4A|S5A|||||Clean|Blinds|Po|AKV A|Def.|Suction|Drain|Blinds|Rail heat|
||2|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B||Clean|Blinds|Po|AKV A|AKV B|||Blinds|Rail heat|
|||EL|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|Clean|Blinds|Po|AKV A|AKV B|Def. A|Def. B|Blinds|Rail heat|
|||Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|Clean||Po|AKV A|AKV B|Def. A|Def. B|Suction|Drain|
||3|Air|S3 + S4|S2A|S3A|S4A|S2B|S3B|S4B|S2C|S3C|S4C|Blinds|Po|AKV A|AKV B|AKV C||Blinds|Rail heat|
|||EL|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B||Clean|Po|AKV A|AKV B|AKV C|Def. A|Def. B|Def. C|
|||Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|Clean|Blinds|Po|AKV A|AKV B|AKV C|Def. A|Def. B|Def. C|
||4|Air|S3 + S4|S2A|S3A|S4A||S2B|S3B|S4B||Clean|Blinds|Po|AKV A|AKV B|AKV C|AKV D|Blinds|Rail heat|
|||EL|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|Clean|Blinds|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|
|||Gas|S3 + S4|S2A|S3A|S4A|S5A|S2B|S3B|S4B|S5B|Clean|Blinds|Po|AKV A|AKV B|AKV C|AKV D|Def. A|Def. B|

102

*[Figurtekst: (Module 2 =  AK-XM 101A) · (Module 2  =  AK-XM 204) · (Module no. 2 = AK-XM 205) · Module 2 App.no at set- · ting via AKM or · DO7 DO8 AI1 AI2 AI3 AI4 AI5 AI6 AI7 AI8 DO1 DO2 DO3 DO4 DO5 DO6 display · pt 18 pt 19 High Low · temp. temp. · Light Fan 6 · Light Fan 7 8 · Light Fan 9 10 · Light Fan 16 · Light Fan 17 18 · Light Fan 19 20 · Light Fan 26 · Light Fan 27 28 · Suction Drain Rail heat Light Fan 29 30 · Light Fan 36 · Def. C Def. D Rail heat Light Fan 37 38 · Def. C Def. D Rail heat Light Fan Suction Drain 39 40 · Light Fan 1 · Light Fan 2 3 · Light Fan 4 5 · Light Fan 11 · Light Fan 12 13 · Light Fan 14 15 · Light Fan 21 · Light Fan S2C S3C S4C S5C 22 23 · Suction Drain S2C S3C S4C S5C Rail heat Light Fan Blinds 24 25 · Light Fan S2C S3C S4C S2D S3D S4D 31 · Def. C Def. D S2C S3C S4C S5C S2D S3D S4D S5D Rail heat Light Fan Blinds 32 33 · Def. C Def. D S2C S3C S4C S5C S2D S3D S4D S5D Rail heat Light Fan Blinds Suction Drain 34 35]*

103

###### **Solenoid valves**

|**Appl.**|**No.**<br>|**Def.**|**Air**|**Contr**|**oller - (**|**Mod**|**ule no.**|**1 poin**|**t 1-19)**||||||||||||
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**type**|**of**<br>**LLSV**|**type**|**sensor**|AI1|AI2|AI3|AI4|AI5|AI6|AI7|AI8|AI9|AI10|AI11|DO1|DO2|DO3|DO4|DO5|DO6|
|||||**pt1**|**pt2**|**pt3**|**pt4**|**pt5**|**pt6**|**pt 7**|**pt8**|**pt 9**|**pt10**|**pt 11**|**pt 12**|**pt 13**|**pt 14**|**pt 15**|**pt 16**|**pt 17**|
|Room|1|Air|S3A + S4A|S3A|S4A|||||||||Door|LLSV A|||||Rail heat|
|||EL|S3A + S4A|S3A|S4A|S5A||||||||Door|LLSV A|Def.||||Rail heat|
|||Gas|S3A + S4A|S3A|S4A|S5A||||||||Door|LLSV A|Def.|Suction|Drain||Rail heat|
||2|Air|S3A + S4A|S3A|S4A|||||||||Door|LLSV A|LLSV B||||Rail heat|
|||EL|S3A + S4A|S3A|S4A|S5A|S5B|||||||Door|LLSV A|LLSV B|Def. A|Def. B||Rail heat|
|||Gas|S3A + S4A|S3A|S4A|S5A|S5B|||||||Door|LLSV A|LLSV B|Def. A|Def. B|Suction|Drain|
||3|Air|S3A + S4A|S3A|S4A|||||||||Door|LLSV A|LLSV B|LLSV C|||Rail heat|
|||EL|S3A + S4A|S3A|S4A|S5A|S5B|S5C||||||Door|LLSV A|LLSV B|LLSV C|Def. A|Def. B|Def. C|
|||Gas|S3A + S4A|S3A|S4A|S5A|S5B|S5C||||||Door|LLSV A|LLSV B|LLSV C|Def. A|Def. B|Def. C|
||4|Air|S3A + S4A|S3A|S4A|||||||||Door|LLSV A|LLSV B|LLSV C|LLSV D||Rail heat|
|||EL|S3A + S4A|S3A|S4A|S5A|S5B|S5C|S5D|||||Door|LLSV A|LLSV B|LLSV C|LLSV D|Def. A|Def. B|
|||Gas|S3A + S4A|S3A|S4A|S5A|S5B|S5C|S5D|||||Door|LLSV A|LLSV B|LLSV C|LLSV D|Def. A|Def. B|
|Case|1|Air|S3 +S4|S3A|S4A||||||||Clean|Blinds|LLSV A||||Blinds|Rail heat|
|||EL|S3 + S4|S3A|S4A|S5A|||||||Clean|Blinds|LLSV A|Def.|||Blinds|Rail heat|
|||Gas|S3 + S4|S3A|S4A|S5A|||||||Clean|Blinds|LLSV A|Def.|Suction|Drain|Blinds|Rail heat|
||2|Air|S3 + S4|S3A|S4A||S3B|S4B|||||Clean|Blinds|LLSV A|LLSV B|||Blinds|Rail heat|
|||EL|S3 + S4|S3A|S4A|S5A|S3B|S4B|S5B||||Clean|Blinds|LLSV A|LLSV B|Def. A|Def. B|Blinds|Rail heat|
|||Gas|S3 + S4|S3A|S4A|S5A|S3B|S4B|S5B||||Clean|Blinds|LLSV A|LLSV B|Def. A|Def. B|Suction|Drain|
||3|Air|S3 + S4|S3A|S4A||S3B|S4B||S3C|S4C||Clean|Blinds|LLSV A|LLSV B|LLSV C||Blinds|Rail heat|
|||EL|S3 + S4|S3A|S4A|S5A|S3B|S4B|S5B|S3C|S4C|S5C|Clean||LLSV A|LLSV B|LLSV C|Def. A|Def. B|Def. C|
|||Gas|S3 + S4|S3A|S4A|S5A|S3B|S4B|S5B|S3C|S4C|S5C|Clean|Blinds|LLSV A|LLSV B|LLSV C|Def. A|Def. B|Def. C|
||4|Air|S3 + S4|S3A|S4A|S3B|S4B|S3C|S4C|S3D|S4D||Clean|Blinds|LLSV A|LLSV B|LLSV C|LLSV D|Blinds|Rail heat|
|||EL|S4|S4A|S5A|S4B|S5B|S4C|S5C|S4D|S5D||Clean|Blinds|LLSV A|LLSV B|LLSV C|LLSV D|Def. A|Def. B|
|||Gas|S4|S4A|S5A|S4B|S5B|S4C|S5C|S4D|S5D||Clean|Blinds|LLSV A|LLSV B|LLSV C|LLSV D|Def. A|Def. B|

104

|||||**Mod**|**ule 2 =**|**AK-XM**|**204**||**App.no**<br>|**at set-**<br>|
|---|---|---|---|---|---|---|---|---|---|---|
|DO7|DO8|DO1|DO2|DO3|DO4|DO5|DO6|DO7|**ting via**<br>**display**<br>DO8|**AKM or**|
|**pt 18**|**pt 19**|**2-pt1**|**2-pt2**|**2-pt3**|**2-pt4**|**2-pt5**|**2-pt6**|**2-pt7**|**2-pt8**<br>**High**|**Low**|
||||||||||**temp.**|**temp.**|
|Light|Fan||||||||46||
|Light|Fan||||||||47|48|
|Light|Fan||||||||49|50|
|Light|Fan||||||||56||
|Light|Fan||||||||57|58|
|Light|Fan||||||||59|60|
|Light|Fan||||||||66||
|Light|Fan||||||||67|68|
|Suction|Drain|Rail heat|Light|Fan|||||69|70|
|Light|Fan||||||||76||
|Def. C|Def. D|Rail heat|Light|Fan|||||77|78|
|Def. C|Def. D|Rail heat|Light|Fan||Suction|Drain||79|80|
|Light|Fan||||||||41||
|Light|Fan||||||||42|43|
|Light|Fan||||||||44|45|
|Light|Fan||||||||51||
|Light|Fan||||||||52|53|
|Light|Fan||||||||54|55|
|Light|Fan||||||||61||
|Light|Fan||||||||62|63|
|Suction|Drain|Rail heat|Light|Fan|||||64|65|
|Light|Fan||||||||71||
|Def. C|Def. D|Rail heat|Light|Fan|Blinds||||72|73|
|Def. C|Def. D|Rail heat|Light|Fan|Blinds|Suction|Drain||74|75|

105

Danfoss can accept no responsibility for possible errors in catalogues, brochures and other printed material. Danfoss reserves the right to alter its products without notice. This also applies to products already on order provided that such alternations can be made without subsequential changes being necessary in specifications already agreed.

All trademarks in this material are property of the respecitve companies. Danfoss and Danfoss logotype are trademarks of Danfoss A/S. All rights reserved.

106
