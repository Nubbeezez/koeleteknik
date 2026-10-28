# Carel easy – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.


---

## easy / easy compact / easy split – electronic digital thermostats with defrost control

*Kilde: Danfoss-dokument User-Manual-CAREL-PJEZ-Controllers.pdf*

#### **easy / easy compact / easy split**

electronic digital thermostats with defrost control

### **User manual**

*[Figurtekst: NO POWER · & SIGNAL · CABLES · TOGETHER · READ CAREFULLY IN THE TEXT!]*

I n t e g r a t e d C o n t r o l S o l u t i o n s & E n e r g y S a v i n g s

###### WARNINGS

CAREL bases the development of its products on decades of experience in HVAC, on the continuous investments in technological innovations to products, procedures and strict quality processes with in-circuit and functional testing on 100% of its products, and on the most innovative production technology available on the market. CAREL and its subsidiaries nonetheless cannot guarantee that all the aspects of the product and the software included with the product respond to the requirements of the final application, despite the product being developed according to start-of-theart techniques. The customer (manufacturer, developer or installer of the final equipment) accepts all liability and risk relating to the configuration of the product in order to reach the expected results in relation to the specific final installation and/or equipment. CAREL may, based on specific agreements, acts as a consultant for the positive commissioning of the final unit/application, however in no case does it accept liability for the correct operation of the final equipment/system.

The CAREL product is a state-of-the-art device, whose operation is specified in the technical documentation supplied with the product or can be downloaded, even prior to purchase, from the website www.carel.com. Each CAREL product, in relation to its advanced level of technology, requires setup/configuration/programming/commissioning to be able to operate in the best possible way for the specific application. The failure to complete such operations, which are required/indicated in the user manual, may cause the final product to malfunction; CAREL accepts no liability in such cases. Only qualified personnel may install or carry out technical service on the product.

The customer must only use the product in the manner described in the documentation relating to the product. In addition to observing any further warnings described in this manual, the following warnings must be heeded for all CAREL products

- prevent the electronic circuits from getting wet. Rain, humidity and all types of liquids or condensate contain corrosive minerals that may damage the electronic circuits. In any case, the product should be used or stored in environments that comply with the temperature and humidity limits specified in the manual.

- do not install the device in particularly hot environments. Too high temperatures may reduce the life of electronic devices, damage them and deform or melt the plastic parts. In any case, the product should be used or stored in environments that comply with the temperature and humidity limits specified in the manual.

- do not attempt to open the device in any way other than described in the manual.

- do not drop, hit or shake the device, as the internal circuits and mechanisms may be irreparably damaged.

- do not use corrosive chemicals, solvents or aggressive detergents to clean the device.

**NO POWER & SIGNAL CABLES TOGETHER**

**READ CAREFULLY IN THE TEXT!**

Separate as much as possible the probe and digital input signal cables from the cables carrying inductive loads and power cables to avoid possible electromagnetic disturbance.

Never run power cables (including the electrical panel wiring) and signal cables in the same conduits.

###### DISPOSAL: INFORMATION FOR USERS

Fig. 1              Fig.2

###### PLEASE READ AND KEEP

With reference to European Union directive 2012/19/EU issued on 4 July 2012 and related national legislation, please note that:

   1. Waste Electrical and Electronic Equipment (WEEE) cannot be disposed of as municipal waste but must be collected separately so as to allow subsequent recycling, treatment or disposal, as required by law;

   2. users are required to take Electrical and Electronic Equipment (EEE) at end-of-life, complete with all essential components, to the WEEE collection centres identified by local authorities. The directive also provides for the possibility to return the equipment to the distributor or retailer at end-of-life if purchasing equivalent new equipment, on a one-to-one basis, or one-to-zero for equipment less than 25 cm on their longest side;

   3. this equipment may contain hazardous substances: improper use or incorrect disposal of such may have negative effects on human health and on the environment;

   4. the symbol (crossed-out wheeled bin – Fig.1) even if, shown on the product or on the packaging, indicates that the equipment must be disposed of separately at end-of-life;

   5. if at end-of-life the EEE contains a battery (Fig. 2), this must be removed following the instructions provided in the user manual before disposing of the equipment. Used batteries must be taken to appropriate waste collection centres as required by local regulations;

   6. in the event of illegal disposal of electrical and electronic waste, the penalties are specified by local waste disposal legislation.

- do not use the product for applications other than those specified in the technical manual.

All of the above suggestions likewise apply to the controllers, serial boards, programming keys or any other accessory in the CAREL product portfolio.

CAREL adopts a policy of continual development. Consequently, CAREL reserves the right to make changes and improvements to any product described in this document without prior warning.

The technical specifications shown in the manual may be changed without prior warning.

The liability of CAREL in relation to its products is specified in the CAREL general contract conditions, available on the website www.carel.com and/or by specific agreements with customers; specifically, to the extent where allowed by applicable legislation, in no case will CAREL, its employees or subsidiaries be liable for any lost earnings or sales, losses of data and information, costs of replacement goods or services, damage to things or people, downtime or any direct, indirect, incidental, actual, punitive, exemplary, special or consequential damage of any kind whatsoever, whether contractual, extra-contractual or due to negligence, or any other liabilities deriving from the installation, use or impossibility to use the product, even if CAREL or its subsidiaries are warned of the possibility of such damage.

3

###### **Content**

|**1.  INTRODUCTION**<br>**7**|
|---|
|1.1 Main characteristics ............................................................................................7|
|1.2  Models .......................................................................................................................7<br>f|
|1.3  Main differences between easy, easy compact and easy split .........8|
|1.4  NTC and PTC probes .........................................................................................9|
|1.5  Accessories ..............................................................................................................9<br>i|
|1.6  Definitions ...............................................................................................................9|
|**2.  ASSEMBLY AND INSTALLATION**<br>**10**|
|2.1  Assembly ...............................................................................................................10|
|2.2 Electrical connections ....................................................................................11|
|2.3  Wiring diagram for multiple units  ........................................................13|
|**3.  USER INTERFACE AND START UP**<br>**14**|
|3.1 easy ............................................................................................................................14|
|3.2 easy compact ......................................................................................................14|
|3.3 easy split .................................................................................................................14<br>i|
|3.4 Preliminary configurations ..........................................................................15|
|3.5 Functions available from the keypad....................................................15|
|**4.  FUNCTIONS AND PARAMETERS**<br>**16**|
|4.1 Temperature probe settings .......................................................................16|
|4.2  Temperature display .......................................................................................16|
|4.3 Temperature control  ......................................................................................17|
|4.4  Duty Setting ........................................................................................................17|
|4.5  Continuous cycle   ...........................................................................................17|
|4.6 Compressor protection .................................................................................18|
|4.7  Defrost ....................................................................................................................18|
|4.8  Alarm parameters ............................................................................................20|
|4.9  Door open/closed management ...........................................................23|
|4.10  Evaporator fan management parameters .....................................24|
|4.11 Clock and time band parameters .........................................................25|
|4.12  Rapid parameter set selection (EZY) .................................................26|
|4.13  Other settings    ..............................................................................................26|
|**5.  TABLES OF ALARMS AND PARAMETERS**<br>**28**|
|5.1  Table of alarms and signals ........................................................................28|
|5.2 Description of the main signals and alarms .....................................29|
|5.3 Data error ...............................................................................................................29|
|5.4  Modifying the parameters..........................................................................29|
|5.5  Setting the default parameters ...............................................................30|
|5.6  Table of easy parameters .............................................................................30|
|5.7  Table of easy compact parameters .......................................................31|
|5.8  Table of easy split parameters ..................................................................32|
|5.9  Table of EZY parameter sets ......................................................................33|
|5.10  Troubleshooting.............................................................................................35|
|**6.  TECHNICAL SPECIFICATIONS**<br>**36**|
|6.1  Easy technical specifications .....................................................................36|
|6.2  easy compact technical specifications ...............................................36<br>i|
|6.3 easy split technical specifications  ..........................................................37<br>|
|6.4  Electromagnetic compatibility ................................................................38|
|6.5  Flammable refrigerant gases ....................................................................38|

5

###### **1.  INTRODUCTION**

easy, easy compact and easy split are electronic microprocessor controllers with LED display, developed for the management of refrigerating units, display cabinets and showcases. They exploit the experience and the success of the previous PJ32 range, with the objective of offering a product that is simpler and more economical. The structure of the parameters has been enhanced with new functions for more

dynamic and effective management of the temperature control and defrost.

easy compact the smallest, most economical easy model, with one relay only, and a simplified display.

easy split model with separate terminal and power board.

###### **<u>1.1 Main characteristics</u>**

The following table lists the main features of the easy, easy compact and easy split controllers.

|Features||Models||
|---|---|---|---|
||easy<br>|easy compact<br>|easy split<br>|
|Ergonomic polycarbonate keypad with three buttons|P<br>|P<br>|P<br>|
|Keypad protection to prevent tampering<br> i|P<br>|P<br>|P<br>|
|Access to the configuration parameters by password|P|P|P|
|Digit display|-199…999<br>|-99...99<br>|-199…999<br>|
|Decimal point|P|P|P|
|Display in°C or°F|P|P|P|
|LED display||||
|Defrost (*)<br>- by stopping the compressor|P<br>|P|P<br>|
|- heater|P|-|P|
|- hot gas|P|-|P|
|-heater with temperature control|P|-|P|
|Duty setting function<br>|P<br>|P<br>|P<br>|
|Continuous cycle function|P|P|P|
|Relay outputs (*)||||
|Up to two analogue inputs for NTC or PTC probes (*)<br>|P|P|-<br>|
|Up to two analogue inputs for NTC/NTC-HT probes|-<br>|-|P<br>|
|Multifunction analogue or digital input (*)<br>|P<br>|-<br>|P<br>|
|In the models with at least 2 probes: display second/third probe (*)|P<br>|P<br>|P<br>|
|Input for CAREL IROPZKEY**programming key (*)|P|P|P|
|Input for external CAREL IROPZ485 connector (RS485 network) (*)|P<br>|P|P<br>|
|Buzzer (audible alarm signals) (*)|P|-|P|
|Fixed or removable terminals|P<br>|P<br>|-<br>|
|Fastening from rear or front<br> i|P<br>|P<br>|P<br>|
|Easy Set (rapid instrument configuration selection)|P|P|P<br>**Table 1.a**|

(*) Check that this is available on the model in question.

Important: each of the features should be checked for the model

in question.

###### **<u>1.2  Models</u>**

The easy and easy compact controllers differ as regards operation, and the number inputs and outputs. easy split models feature a separate terminal and power board. PQEZ* controllers are specifically designed for use in applications with flammable refrigerants.

easy models:

P(J,Q)EZS (0, 1, 6, 7)*; P(J,Q)EZ(X, Y)*; P(J,Q)EZC* controllers and P(J,Q) EZM(0, 1, 6, 7)* thermometer only. easy compact models: P(J,Q)EZS(N, P)* controller and PJEZM(N,P)* thermometer only. easy split models: PJEZ*8**** controllers with one relay used for the light output.

###### **Models and features**

###### X and Y models P(J,Q)EZX*, P(J,Q)EZY*

These are designed for the management of static units operating at low temperature (that is, below 0ºC), which require active defrost using electric heaters or the injection of hot gas. The P(J,Q)EZ(Y,X)*, in fact, as well as working as a thermometer and a thermostat (like the P(J,Q) EZS), also manages the defrost actuator. The frequency and duration of the defrost can be set. The end defrost can occur according to the temperature reached (connecting a probe to the evaporator) or by time. In addition these models feature two probe inputs, for the control probe (room), the defrost probe, and a digital input (this can also be configured as a probe). There are two outputs, for controlling the actuator (compressor ) and the defrost . Models P(J,Q)EZY and P(J,Q)EZX differ in that:

- P(J,Q)EZY has relays that are electrically connected together;

- P(J,Q)EZX has independent relays.

###### S models P(J,Q)EZS*

The ideal solution for the management of static refrigeration units (that is, without fan on the evaporator), operating at normal temperature (above 0 °C). This model, in fact, performs the functions of thermometer, displaying the temperature of the unit, and electronic thermostat, activating the compressor (or the solenoid valve in the case of multiplexed units) so as to maintain the required temperature. In addition, it features compressor protection algorithms and automatic defrost function by shutting down the compressor.

###### C models P(J,Q)EZC*

The most complete solution for low temperature ventilated units, with three relays for complete control of the compressor, fan and defrost functions. The three relays are included in the very compact case in the versions with 230 V or 115 V power transformer, without compromising the performance or reliability of the product.

###### M models P(J,Q)EZM*

Solution for simply measuring the temperature.

7

Summary table of the functions associated with the models

|function|see||||easy|||||easy co|mpact||eas|y split|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
||par.|mod.|mod.|mod.|mod.S||mod.|M|mo|d.S|m|od.M|mod|.<br>mod.|
|||C|X|Y|2 probes +<br>multifun.<br>input|1<br>probe|2 probes +<br>multifun.<br>input|1<br>probe|2<br>prbs|1<br>probe|2<br>prbs|1<br>probe|S|C|
|temperature display|4.2|P|P|P|P|P|P|P|P|P|P|P|P|P|
|<br>temperature measurement in°C/°F|4.2|P|P|P|P|P|P|*|P|P|P|*|P|P|
|parameter access using password|5.4|P|P|P|P|P|P|*|P|P|P|*|P|P|
|<br>set point modification|3.5|P|P|P|P|P|P|*|P|P|P|*|P|P|
|night-time set point management|4.3|P|P|P|P|-|P|-|-|-|-|-|P|P|
|<br>enable/disable direct probe 2 alarm|4.2|-|-|-|-|-|P|-|-|-|P|-|-|-|
|temperature probe calibration|4.1|P|P|P|P|P|P|*|P|P|P|*|P|P|
|temperature control in DIRECT mode|4.3|P|P|P|P|P|-|-|P|P|-|-|P|P|
|<br>temperature control in REVERSE mode|4.3|P|P|P|P|P|-|-|P|P|-|-|P|P|
|compressor protectors|4.6|P|P|P|P|P|-|-|P|P|-|-|P|P|
|duty setting|4.4|P|P|P|P|P|-|-|P|P|-|-|P|P|
|<br>continuous cycle|4.5|P|P|P|P|P|-|-|P|P|-|-|P|P|
|defrost|4.7|P|P|P|P|P|-|-|P|P|-|-|P|P|
|high/low temperature alarm|4.8|P|P|P|P|P|P|*|P|P|P|*|P|P|
|dirty condenser alarm|4.8|P|P|P|P|-|P|-|P|-|P|-|P|P|
|evaporator fan management|4.10|P|-|-|-|-|-|-|-|-|-|-|-|P|
|<br>ON/OFF<br>i|3.5|P|P|P|P|P|P|*|P|P|P|*|P|P|
|AUX output configuration|4.13|P|P|P|P|P|P|*|P|P|P|*|P|P|
|i<br>enable/disable keypad|4.13|P|P|P|P|P|P|*|P|P|P|*|P|P|
|<br>enable/disable buzzer<br>i|4.13|P|P|P|P|P|P|*|-|-|-|-|P|P|
|modified parameter detection|4.13|P|P|P|P|P|P|*|P|P|P|*|P|P|
|i<br>rapid parameter set selection|4.12|P|P|P|P|P|-|-|P|P|-|-|P|P|
|<br>clock and time band management|4.11|P|P|P|-|-|-|-|-|-|-|-|P|P|
|door switch with light management|4.8|-|-|-|-|-|-|-|-|-|-|-|P|P|
|<br>disable high temperature alarm when<br>starting|5.1|-|-|-|-|-|-|-|-|-|-|-|P|P|
|second compressor output in parallel|4.13|-|-|-|-|-|-|-|-|-|-|-|P|P|
|<br>second comp. output with two step control<br>with or without rotation|<br>4.13|-|-|-|-|-|-|-|-|-|-|-|P|P|
|fan management with comp. of|4.10|-|-|-|-|-|-|-|-|-|-|-|-|P|
|night-time operation with light|4.11|-|-|-|-|-|-|-|-|-|-|-|P|P|
|management||||||||||||||**Table 1.b**|

* available but cannot be set from the keypad nor the programming key.

###### **<u>1.3  Main diferences between easy, easy compact and easy splitf</u>**

Unlike the easy and easy compact models, the easy split models feature a separate terminal and power board. There are also other differences, such as the auxiliary multifunction relay for managing the light output or a second compressor, and new software functions. The table below highlights the differences and indicates the page showing the related explanation.

|topic|easy, easy<br>compact|easy split|easy split<br>parameter|page|
|---|---|---|---|---|
|type of probes connectable (selectable by parameter, easy split only)|NTC, PTC|NTC, NTC-HT|/P|9|
|dedicated relay for the light output<br>f|NO|YES|H1=4|29|
|light on/offfrom the keypad|defrost only|YES|H1=4|16|
|probe display rate function|NO|YES|/3|17|
|curtain switch (night-time operation) with light management<br>f|NO|YES|A4=4|24|
|light not managed/ managed with door switch and evaporator fan off|NO|YES|A4=7, 10|25|
|light not managed/ managed with door switch and evaporator fan and compressor of|NO|YES|A4=8, 11|25|
|door open/closed management|NO|YES|Ado|25|
|second compressor output in parallel with dedicated relay|NO|YES|H1=5|29|
|second compressor output with two step control with or without rotation|NO|YES|H1=7/6|29|
|second compressor delay|NO|YES|c11|19|
|fan management with compressor of|NO|YES|F2=2, F4, F5|27|
|night-time operation with light management|NO|YES|A4=4, H1=4|24|
|year, month, day of month setting|NO|YES|YEr, MOn, dMO|28|
|disable high temperature alarm when starting|NO|YES|-|31|
|maintenance request signal (SrC)|NO|YES|HMP, HMd, HMr|30|
|||||**Table 1.c**|

8

###### **<u>1.4  NTC and PTC probes</u>**

All easy and easy compact models use PTC and NTC probes conforming to the CAREL standard, with resistance values of 985Ω at 25°C for the PTC, and 10 kΩ for the NTC. The type of probe installable depends on the model (order code). The easy split models, on the other hand, only use NTC and high temperature NTC probes (50 KΩ at 25°C), selected by parameter. Below are some codes of the more common CAREL.

|code|description|operating<br>range|index of<br>protection|
|---|---|---|---|
|NTC***HP00|NTC probe, 6x15 mm<br>bulb, plastic|-50T50°C|IP67|
|NTC***HT00|High temp. NTC probe,<br>5x20 bulb mm, polyester|0T120 °C<br>(max 150 °C for<br>3000 h)|IP55|
|NTC***WP00|NTC probe , 6x40 mm<br>bulb,metal|-50T100°C|IP67|
|PTC***W000|PTC probe, 6x40 mm<br>bulb,metal,1.5 m long|-50T100°C|IP67|
||||**Table 1.d**|

###### **<u>1.5  Accessories</u>**

- CAREL IROPZKEY* programming key (for duplicating the parameters);

- CAREL IROPZ485S0 RS485 converter (for the RS485 supervisory network).

- CAREL USB/RS485 converter CVSTDUMOR0 to interface a RS485 network to a personal computer via the USB port;

- VPM, program downloadable from http://ksa.carel.com. This tool, running on a computer, can be used to commission the controller, program the parameters and update the firmware;

- COM TOOL, program downloadable from http://ksa.carel.com. This tool can be used to program the controller from any PC, save the different configurations in files that can be recalled during final programming, create custom sets of parameters for rapid programming and configure the different users with password protected access profiles. Connection to the PC requires the USB/RS485 converter code CVSTDUMOR0;

- connection cable between terminal and power board (easy split only). Available in different lengths (PEOPZC1500=1.5 m, PEOPZC3000=3.0 m, PEOPZC5000=5.0 m).

###### **<u>1.6  Definitions</u>**

Continuous cycle: function that runs the compressor for the set time.

Defrost: function that controls the defrost of the evaporator.

Duty  setting: safety function that in the event of control probe faults starts the compressor at set time intervals.

easy: trademark of the P(J,Q)EZ(S, X, Y, C, M)* thermostats.

easy compact: more compact and economical version of the easy. Available in models PJEZ(S, M)*.

easy split: version with separate terminal and power board. Versions available with (PJEZ*8R***) or without (PJEZ*8I***) RTC, and the power board can be supplied with (PJEZ*8**5*) or without (PJEZ*8**4*) plastic case.

9

###### **2.  ASSEMBLY AND INSTALLATION**

###### **<u>2.1  Assembly</u>**

   - Avoid installing the boards in environments with the following characteristics:

- relative humidity greater than 90% or where there is condensation;

- strong vibrations or knocks;

- exposure to continuous water sprays;

- exposure to aggressive and polluting atmospheres(e.g.: sulphur and ammonia fumes, saline mist, smoke) so as to avoid corrosion and/or oxidation;

- strong magnetic and/or radio frequency interference (there avoid installing the units near transmitting antennae);

- near transmitting antennae and to the elements in general;

- large and rapid fluctuations in the ambient temperature;

- environments where explosives or mixes of flammable gases are present;

- exposure to dust (formation of corrosive patina with possible oxidation and reduction of insulation.

To install easy, easy compact and easy split: make an opening in the panel based on the drilling template, 71x29 mm.

###### **Panel installation using 2 rear brackets (Figs. 2.a and 2.b)**

- insert the instrument in the opening (phase 1);

- repeat the same operation for the top screw (phase 2);

- apply the front frame (phase 3).

*[Figurtekst: 1 2 3 · (*) · max 2,5]*

**Fig. 2.c**

(*) do not ove r-tighte3 mm n the screws.

###### **Dismantling using the screws from the front**

   - unclip the front frame;

   - unscrew the bottom screw, at the moment the front panel detaches from the panel keep pressure on the screw and unscrew a further 90° to make the catch go back into its slot;

   - repeat for the top screw;

   - remove the instrument from panel, keeping it horizontal

- secure the instrument by sliding the brackets in the guides on the instrument until compressing them against the panel (phase 2);

###### easy

*[Figurtekst: 1 2 · Fig. 2.a · easy compact, easy split · 1 2 · Fig. 2.b · PUSH · PUSH]*

###### **easy split: power board dimensions and assembly**

Assembly is performed using plastic spacers or plastic turrets. The power board is supplied upon fitted in a standard case for panel mounting, dimensions 190x140x70.

*[Figurtekst: 117 · 36 8.5 · 103.5 5 · Ø 4 · L · RL1 RL4 RL3 RL2 · L · N · N · 7 · 5 · 98 88 · 5]*

**Fig. 2.d**

###### **Removing from the panel with brackets**

- release the instrument by pressing both brackets where marked “push” and sliding it back on the guides.

- the connection cables must guarantee insulation at least up to 90 °C;

- spade terminals with max. operating temperature at least 100°C

###### **Panel installation from the front using screws (Fig. 2.c)**

- the thickness of the fastening panel must not exceed 3 mm;

- remove the front frame and make sure that the two catches are in place (these must not protrude from the outline of the drilling template). If necessary, unscrew the two screws. Do not unscrew excessively, the screws must not be detached from the front panel (phase 1);

- insert the instrument in the opening in the panel and hold it in position by the centre of the front panel (phase 1);

   - if the board is installed in an electrical panel with metal cabinet, allow at least 10 mm distance between the cabinet and any point on the board (rear, edges and assembly holes);

   - the probe and digital input connections must be less than 10 m long, adopt suitable measures to separate the cables for compliance with immunity standards;

   - suitably fasten the output connection cables to avoid contact with extra low voltage components.

- usi ~~n~~ g the screwdriver, tigh ~~ten~~ th e bottom screw 90° ~~,~~ the catch must co ~~me ou~~ t of ~~its slo~~ t and click onto the ~~pane~~ l, then tighte ~~n unti~~ l the front pa ~~nel is s~~ ec ~~ure. D~~ o not over-tighten ~~, whe~~ n the front ~~panel~~ is secured blocks simply make another ½ turn to compress the gasket; If the catch does not click onto the panel, unscrew the screw, applying pressure at the same time with the screwdriver so that the catch moves back. Do not unscrew too much, the head of the screw must not be raised from the surface of the front panel (phase 2);

10

###### **<u>2.2 Electrical connections</u>**

- the electrical connections must only be completed by a qualified electrician;

- a power supply other than the type specified may seriously damage the system;

- on easy split models supplied with plastic case, given the high maximum power supply current (16 A), the unit may heat up: in this case, make sure the maximum temperature allowed is not exceeded. See the table of technical specifications;

- separate as much as possible the probes and digital input signal cables from the cables carrying inductive loads and power cables to avoid possible electromagnetic disturbance. Never lay power cables (including the electrical cables) and probe signal cables in the same conduits. Do not install the probe cables in the immediate vicinity of power devices (contactors, circuit breakers or similar);

- reduce the path of the probe and sensor cables as much as possible, and avoid spiral paths that enclose power devices. The probes must be connected using shielded cables (minimum cross-section of each wire: 0.5 mm<sup>2</sup> );

- avoid direct contact with internal electronic components;

- connection errors (and connections other than those indicated in this manual) may involve danger to the safety of the users and cause faults on the instruments and the components connected;

- fit the unit with all the electromechanical safety devices required to guarantee correct operation and the complete safety of the user.

Information:

- the probes can be installed up to a maximum distance of 30 m from the controller (10 m for easy split). To extend the distance of the probes, use cables with a minimum cross-section of 1 mm², shielded where possible. In this case, the shield must be connected to the common of the probe. Do not earth the other end of the shield (the sensor end);

- only use IP67 probes as end defrost probes; place the probes with the vertical bulb upwards, so as to assist the drainage of any condensate. The thermistor temperature probes (NTC or PTC) have no polarity, so the order of connection of the ends is not important;

- use cable ends suitable for the corresponding terminals. Loosen each screw and insert the cable ends, then tighten the screws. When the operation is completed, slightly tug the cables to check they are sufficiently tight.

The connections of the inputs and outputs, depending on the models, may be made:

- using traditional screw terminals;

- using plug-in terminals with screw cable connection blocks;

- using plug-in terminals with crimped cable connection blocks.

- using plug-in terminals, which significantly simplify the connection of the instrument both during installation and maintenance. This also avoids connection errors, as there are three connection blocks with a different number of pins.

- Connect the inputs and the outputs following the diagram shown on the instrument label.

###### For the 12 Vac versions:

- if the power supply available is mains, a safety transformer is required to ensure double insulation between the power supply and the very low voltage electronics. If required, a fuse must be installed in series with the primary (32 mAT for code TRA12VDE00). The transformerinstrument connection must be as short as possible;

- if the power supply available is already low voltage, but not 12 Vac, a suitable adapting transformer must be used: double insulation between the primary and secondary and definition for surge on the primary to the appropriate level (2000 V for applications in industrial environments.

- as double insulation cannot be guaranteed between the power supply connectors and the relay outputs, only use loads powered at safety extra low voltage (effective rating up to 42 V).

The voltage supplied to these terminals (see the wiring diagrams)  must correspond, within the specified tolerances, to the value shown on the instrument connection label. The insulation of the instrument, for versions with mains power supply (230 Vac and 115 Vac), is reinforced. The versions with 12 Vac/Vdc power supply, on the other hand, do not feature such insulation.

###### For easy split:

Refer to the following wiring diagram;

- power supply L, N, PE: use cables with a suitable cross-section for the load (2.5 mm<sup>2</sup> for current ratings up to 16 A and 4 mm<sup>2</sup> for current ratings up to 24 A);

- load connection: terminate with 6.3 mm female spade contacts, cable cross-section 2.5 mm<sup>2</sup> for current ratings up to 16 A;

- use:

- cables with max. operating temperature at least 90 °C

- spade terminals with max. operating temperature at least 100 °C

- internal jumpers for power supply to loads as per the previous point;

- probe and digital input connections with 0.5 to 1.5 mm<sup>2</sup> cables;

- terminal connection using specified cables.

###### easy wiring diagrams

*[Figurtekst: P(J,Q)EZ(S, X)* · -10T50 SERIAL · Compressor CONV · relay 16A NTC/PTC PROG.KEY · PROBES · 1    2     3   4    5 6   7 8 9 10 11 · LN orAUX 12 Vac/Vdc115 Vac or230Vac orL N or · P(J,Q)EZ(S, X)* -10T50 SERIAL · Compressor  CONV · PROG. · relay 2HP NTC/PTC KEY · PROBES · 1    2    3    4    5 6   7 8 9 10 11 · LN orAUX 12 Vac/Vdc115 Vac or230Vac orL N or · P(J,Q)EZ(S, Y)* -10T50 SERIAL · Compressor CONV · PROG. · relay 30A NTC/PTC KEY · PROBES · 1    2     3   4   5 6   7 8 9 10 11 · L N · or 230Vac or or · AUX 115 Vac · L · N · P(J,Q)EZ(C, Y)* -10T50 SERIAL · Compressor CONV · PROG. · relay 2HP NTC/PTC KEY · PROBES · 1    2     3   4   5 6   7 8 9 10 11 · L N · or 230Vac or or · AUX 115 Vac or · L 12 Vac/Vdc · N · P(J,Q)EZ(C)* -10T50 SERIAL · Compressor CONV · PROG. · relay 30A NTC/PTC KEY · PROBES · 1    2    3   4    5 6   7 8 9 10 11 · L N · or 230Vac or or · AUX 115 Vac · L · N · P(J,Q)EZ(M)* -10T50 SERIAL · CONV · PROG. · NTC/PTC KEY · PROBES · 1     2   3     4   5 6   7 8 9 10 11 · AUX L N · L 230Vac or or · N 12 Vac/Vdc115 Vac or · DI / PROBE · AMB. T. DEF. T. · DI / PROBE · AMB. T. DEF. T. · DI / PROBE · AMB. T. DEF. T. · DI / PROBE · AMB. T. DEF. T. · DI / PROBE · AMB. T. DEF. T. · DI / PROBE · AMB. T. DEF. T.]*

**Fig. 2.e**

11

###### easy compact wiring diagrams

*[Figurtekst: PJEZS***0** PJEZS***E** · PJEZS***1** · 1 2 3 PROG.KEY SERIALCONV NTC PROBES 4 5 6 1 2 3 NTC PROBES 4 5 · L N L N · PJEZM*N*0** PJEZM*N*E** · PJEZM*N*1** · 1 2 PROG.KEY SERIALCONV NTC PROBES 3 4 5 1 2 NTC PROBES 3 4 · L N L N · 12V~ 12V~ · PJEZM*P*0** PJEZM*P*E** · PJEZM*P*1** · 1 2 3 PROG.KEY SERIALCONV NTC PROBES 4 5 6 1 2 3 NTC PROBES 3 4 · AUX AUX · L N L N]*

**Fig. 2.f**

easy split wiring diagram

**Fig. 2.g**

(*) For codes PJEZ*8**5* the temperature range is -10T50 °C and the maximum current is 16 A. See the table of technical specifications.

----------- = recommended internal power supply connections.

12

###### **<u>2.3  Wiring diagram for multiple units</u>**

The RS485 converter (IROPZ485S0) is used to connect the easy, easy compact and easy split instruments to the supervisor network, allowing complete control and monitoring of the easy units connected. The system allows:

- up to 207 easy units without RTC to be connected together.

- up to 30 easy units with RTC to be connected together. Maximum length of 1000 m.

The connection requires the standard accessories (RS485-USB converter, CAREL code CVSTDUMOR0) and two 120 Ω terminal resistors. Connect the RS485 converter to the easy, easy compact or easy split using a four-wire cable  and make the connections as shown in the figure. The line should be started and ended with a 120 Ω 1/4 W resistor. For the allocation of the serial address see parameter H0. The recommended connection cable is a twisted pair with shield and cross-section from 0.5 to 1.5 mm<sup>2</sup> (AW6 22-24).

*[Figurtekst: USB · CVSTDUMOR0 · - + . . . easy · 120 ohm GND+- IROPZ485S0 · max. 207 · easy units · GND · +- IROPZ485S0 · easy · GND · 120 ohm +- IROPZ485S0 · GND · RS485 · RS485]*

**Fig. 2.h**

###### **easy split:**

The serial connection for the easy split models with 4 relays depends on the setting of parameter H7, as the management of the fourth relay (RL4) and serial communication are mutually exclusive.

The factory setting is H7=1, which means the fourth relay is enabled. To enable connection to the supervisor network:

1. power down the controller;

2. disconnect the 4-wire cable from the rear of the display;

3. connect the display to converter code IROPZ485S0 and this to the RS485 network;

4. power up the controller and set H7=0 and the network address for parameter H0.

To restore the fourth relay output (RL4):

1. power down the controller;

2. disconnect converter code IROPZ485S0 from the rear of the display;

3. connect the 4-wire cable from the power board to the display;

4. power up the controller and set H7=1.

- the RS485 converter (IROPZ485S0)  is sensitive to electrostatic discharges, and therefore must be handled with extreme care;

- check the technical documents on the CAREL IROPZ485S0 option for the description of the connection methods so as to avoid damaging the instrument;

- suitably fasten the converter so as to avoid disconnections;

- perform the wiring with the power supply disconnected;

- keep the IROPZ485S0 serial option cables separate from the power wires (relay outputs and power supply).

13

###### **3.  USER INTERFACE AND START UP**

###### **<u>3.1 easy</u>**

###### **Display**

*[Figurtekst: 1 7 · 2 · 3 · 4 · 5 · 6 · Fig. 3.a · but. function normal operation  start up · ON OFF flash · 1 compressor on of call ON · 2 fan on of call ON · 3 defrost on of call ON · 4 auxiliary output  output active output not active - ON · (AUX) · 5 clock (RTC) RTC available, enabled  RTC not available or  ON (if the · (tEN=1)  and at least  not enabled (tEN=0)  clock is · one time band has  or no time band set fitted) · been set · 6 alarm alarm in progress no alarm in progress - ON · 7 digits three digits with decimal point and range -199 to 999. See · parameters /4, /5, /6 for the type of probe displayed, values in · °C/°F  and decimal point]*

**Table 3.a**

###### **Keypad (models C, S, X, Y)**

*[Figurtekst: 1 · 2 · 3 · Fig. 3.b]*

*[Figurtekst: but.  normal operation start up · pressing the button alone pressing with · other buttons · 1 more than 3 s: switch ON/OFF pressed together  - · with 3 activates / · deactivates the · continuous cycle · 2 - 1 s: displays/sets the set point - for 1 s RESET  pressed · - more than 3 s: accesses the  current EZY  together · parameter setting menu (enter  set (2 and 3) · password 22) activate · - mutes the audible alarm (buzzer) parameter · 3 more than 3 s: activates / pressed together  for 1 s displays  reset · deactivates the defrost with 1 activates / firmware  procedure · deactivates the  version · continuous cycle · Table 3.b]*

###### **<u>3.2 easy compact</u>**

###### **Display**

*[Figurtekst: 1 · 2 · Fig. 3.c · but.  function normal operation  start up · no. ON OFF flash · 1 compressor on of call ON · 2 digits two digits with sign and decimal point, -99 to 99(*). See · parameters /4, /5, /6 for the type of probe displayed, values · in °C/°F  and decimal point]*

**Table 3.c**

(*) The parameters that feature three digit values can be set from the supervisor. In this case, the display will show “--” .

###### **Keypad (model S)**

**Fig. 3.d**

*[Figurtekst: but.  normal operation start up · pressing the button alone pressing with · other buttons · 1 more than 3 s: switch ON/OFF pressed together  - · with 3 activates / · deactivates the · continuous cycle · 2 - 1 s: displays/sets the set point - for 1 s RESET  pressed · - more than 3 s: accesses the  current EY  together · parameter setting menu (enter  set (2 and 3) · password 22) activate · - mutes the audible alarm (buzzer) parameter · 3 more than 3 s: activates / pressed together  for 1 s  reset · deactivates the defrost with 1 activates / displays  procedure · deactivates the  firmware · continuous cycle version]*

**Table 3.d**

###### **Keypad functions for easy and easy compact M models (models with keypad only)**

*[Figurtekst: 1 · 2 · 3 · Fig. 3.e]*

*[Figurtekst: but. normal operation start up · pressing the button alone · 1 more than 3 s: switch ON/OFF - · 2 - 1 s: displays/sets the set point - pressed · - more than 3 s: accesses the parameter setting  together · menu (enter password 22) activate · - mutes the audible alarm (buzzer) parameter · 3 rapid selection of probe displayed for 1 s displays  reset · firmware version procedure · Table 3.e]*

###### **<u>3.3 easy split</u> Display**

*[Figurtekst: 1 7 · 2 · 3 · 4 · 5 · 6]*

**Fig. 3.f**

*[Figurtekst: but. function normal operation  start up · ON OFF flash · 1 compressor 1/2 on of call ON · 2 fan on of call ON · 3 defrost on of call ON · 4 auxiliary output  output active output not  - ON · (AUX) - light active · 5 clock (RTC) RTC available,  RTC not  ON (if the · enabled (tEN=1)  available or  clock is · and at least one  not enabled  fitted) · time band has  (tEN=0) or no · been set time band set · 6 alarm alarm in  no alarm in  - ON · progress progress · 7 digits three digits with decimal point and range -199 to 999. See · parameters /4, /5, /6 for the type of probe displayed, values · in °C/°F  and decimal point]*

**Table 3.f**

14

###### **Keypad**

*[Figurtekst: 1 · 2 · 3 · Fig. 3.g]*

*[Figurtekst: but.  normal operation start up · pressing the button alone pressing with other · buttons · 1 more than 3 s: switch ON/OFF  pressed together  - · light (H1=4) or defrost with 3 activates / · deactivates the · continuous cycle or · defrost (see par. H6) · 2 - 1 s: displays/sets the set point - for 1 s RESET  pressed · - more than 3 s: accesses the  current EZY  together · parameter setting menu (enter  set (2 and 3) · password 22) activate · - mutes the audible alarm  parameter · (buzzer) reset · 3 more than 3 s: activates / pressed together  for 1 s displays  procedure · deactivates light (H1=4) or  with 1 activates / firmware · defrost deactivates the  version · continuous cycle or · defrost (see par. H6) · Table 3.g]*

While the following are enabled:

- temperature display, alternating with the message “OFF”;

- parameter display and setting;

- alarms: “E0”, “E1”, “E2”;

- the internal timer relating to parameter ‘dI’ is updated. If ‘dI’ expires in OFF status, a defrost is performed when restarting;

- auxiliary relay management, only in the following configurations: – H1= = 1/2 (“E0” alarm only);

- H1= 3, A4= 6;

- H1=4 (easy split only).

Note: when exiting OFF status, the following settings are set to zero (that is, are not saved prior to OFF): evaporator fan alarm hysteresis and management (A0), temperature control hysteresis (rd), cht pre-alarm hysteresis (AE). In addition, the delays are set to zero for the display of the temperature alarms (Ad, d8, c6), dripping (dd) and postdripping (Fd).

- when first connected, easy is already on and ready to be used;

- the instrument can be switched on from a supervisor PC and via an external contact (setting A4= 5). The latter has priority over the other modes.

###### **Set point setting (desired temperature value)**

###### **<u>3.4 Preliminary configurations</u>**

Once the electrical connections have been completed, simply power-up the controller to make it operative.

CAREL then recommends to check that the display does not show any alarm signals (see par. “5.1 Table of alarms and signals” on page 31), then set the time and date (in the models fitted with RTC, see par. “4.11 Clock and time band parameters” page. 28), and finally set the parameters as desired. The main parameters are as follows:

###### <u>Control parameters</u>

|st|set point<br>f|
|---|---|
|rd|set point differential|
|/P (only easy split)|select type of probe|
|Defrost parameters||
|d0|type of defrost|
|dl|interval between two defrosts|
|dt|end defrost temperature|
|dP|maximum defrost duration|
|Alarm parameters||
|Ad|temperature alarm delay|
|AL|low temperature alarm threshold/deviation|
|AH|high temperature alarm threshold/deviation<br>f|
|A0|alarm and fan temperature differential|

**Table 3.h**

Note: The procedure for modifying the parameters is described in par. “5.4 Modifying the parameters” page 32.

###### **<u>3.5 Functions available from the keypad</u>**

###### **On and off**

Switching the instrument ON: press UP for more than 3 s (when pressing the button, the display shows ON).

Switching the instrument OFF: press UP for more than 3 s. The display shows the message “OFF”, alternating with the temperature measured by the set probe.

In off status, the following functions are disabled (if featured by the model):

- compressor control / duty setting / continuous cycle;

- defrost;

- fan control;

- alarms : ‘LO’, ‘HI’, ‘IA’, ‘cht’, ‘CHT’;

- door switch:

- easy, easy compact: A4=7/8;

- easy split: A4=7/8/10/11;

The easy, easy compact and easy split devices control the desired temperature (set point) inside the cabinet or cold room directly and dynamically.

To view and modify the set point:

- press SET for 1 s, the set value will start flashing;

- increase or decrease the value using UP or DOWN;

- press SET to confirm the new value.

Important: the PJEZM* models fitted with keypad simply monitor the deviation from the set point and where necessary signal an alarm. On these models, the set point can only be modified using parameter “St”.

###### **Manual defrost**

Not available on the easy thermometer (M) and easy compact models. Press DOWN for more than 3 s (activated only if the temperature conditions are right, for easy split only if the light output is not set, H1≠4). Alternatively, on easy split models, if the light output is set (H1=4), the defrost can be activated by pressing UP and DOWN together, when H6=1).

###### **Continuous cycle**

Not available on the easy thermometer (M) and easy compact models. Press UP+DOWN for more than 3 s (activated only if the temperature conditions are right and for easy split only when H6=0).

The continuous cycle is used to maintain refrigeration active in the cabinet or cold room, regardless of the temperature inside the unit. This may be useful for rapidly bringing the temperature below the set point value.

###### **Light (easy split only)**

As already mentioned, when a light output is configured (H1=4), the DOWN button switches the light on/off, otherwise it starts/stops the defrost.

###### **Rapid display of the temperature read by the other probes (only available for easy and easy compact thermometer models - M)**

Press the DOWN button to scroll the temperatures read by the probes. Each time the DOWN button is pressed, the display will show the name of the probe Pr1, Pr2 or Pr3 (only on the models with 3 inputs and with multifunction input configured as a probe) and after 1 s the temperature measured by the selected probe will be displayed. To display the other probes, press DOWN again.

To return to the normal display, wait 3 s without pressing any buttons (exit by timeout).

- buzzer (when available).

15

###### **4.  FUNCTIONS AND PARAMETERS**

This chapter describes all the functions of the easy, easy compact and easy split. See Table 1.b for the compatibility of the functions with the model used.

###### Important:

the easy compact models only display two digits. In the range below -99 and above 99, the terminal will display “- -”. The parameter codes with 3 digits are converted as follows:

*[Figurtekst: easy, easy split easy compact · /C1 -C1 · /C2 -C2 · EZY EY · Table 4.a]*

/C1/C2/C3: probe 1, 2, 3 offset

These parameters are used to correct the temperature measured by the probes (/C1 probe 1, /C2 probe 2 and /C3 probe 3), with an offset in tenths of a degree. The value assigned to this parameter is in fact added to (/C1/C2/C2>0) or subtracted from (/C1/C2/C3<0) the temperature measured by the related probe.

Important: parameter /C3 is not available on the easy compact models.

###### /P: select type of probe (easy split only)

Used to select the type of probe used for the measurements:

- /P=0 standard NTC: -50T90°C;

- /P=1 high temperature NTC: -40T150°C.

While the messages become:

*[Figurtekst: easy, easy split easy compact · OFF OF · dEF dF · Pr1 P1 · Pr2 P2 · SEt St]*

###### **<u>4.2  Temperature display</u>**

The temperature displayed, the unit of measure and the decimal resolution can be set according to the following parameters: /4, /5 and /6.

**Table 4.b**

###### /4 : select probe displayed

###### **<u>4.1 Temperature probe settings</u>**

Depending on the models, the easy and easy compact controllers feature one or two analogue inputs. The easy controllers, in addition, also feature a multifunction input (analogue or digital). All easy split models have two analogue inputs and one multifunction input (analogue or digital). After installation, the values measured by the temperature probes can be corrected and stabilised using the following parameters.

Used to choose whether to display the temperature read by the control probe (Probe 1), Probe 2 or the status of the multifunction input (analogue or digital).

Digital input =0: contact closed. Digital input =1: contact open.

Parameter /4 selects the probe shown on the display, all the other display and control modes remain unchanged.

Important: the easy compact models can display up to 2 probes.

###### /2: probe measurement stability

Coefficient used to stabilise the temperature measured by the probes. /2 acts as a “filter” on the minimum variations in the temperature measurement, and at the same time calculates the average of the readings.

- low values assigned to /2 allow a prompt response of the sensor to temperature variations (the reading becomes more sensitive to disturbance);

- high values slow down the response, but guarantee greater immunity to disturbance (more stable and more precise reading).

###### /3: probe display rate (easy split only)

This parameter is used to set the rate at which the temperature display is updated. The temperature shown on the display tends to follow rapid deviations away from the set point very slowly, and vice-versa, moves very quickly in the event where the temperature displayed is approaching the set point. If the control temperature exceeds the high or low temperature thresholds and an AL or AH alarm is activated, the filtering is immediately bypassed and the temperature displayed is the temperature effectively measured, until all the alarms are reset. The action of parameter ‘/3’ only affects the temperature displayed, and not the temperature used for the control functions. The update rate decreases as the value of the parameter increases, from 1 to 15.

<u>Parameter /3</u> Value <u>0 = disabled 1 = fast update … 15 = slow update</u>

###### /5: select °C/°F

Defines the unit of measure used for temperature control.

- /5=0 to work in °C

- /5=1 to work in °F.

###### Warning:

- when changing from one unit of measure to the other, all the values of the temperature parameters must be modified to the new unit of measure.

- The max and min limits of the absolute temperature parameters are the same for both °C that °F. The range of temperatures allowed is therefore different between °C and °F:

###### /6: disable decimal point

Used to enable or disable the temperature display with the resolution to the tenths of a degree between -20 and + 20 (easy and easy split) or -10 and +10 (easy compact).

- /6= 0 temperature displayed to the tenth of a degree;

- /6=1 temperature displayed without the tenths of a degree.

Note: the decimal point is only disabled in relation to the reading shown on the display (the calculations performed by the controller remain unchanged).

###### **Table 4.c**

###### /7: enable probe 2 alarm (M models only)

Example: In the case of bottle coolers, typically used in supermarkets, when the doors are opened frequently, due to the greater thermal inertia of the liquids compared to the air, and the fact that the probe is positioned in the air and not directly on the products, the instrument measures a temperature that is higher than effective temperature of the soft drinks, thus displaying a quite “unrealistic” temperature. Setting parameter ‘/3’ to a value other than 0, any abrupt variations in temperature are “filtered” on the display, showing a temperature trend that is “closer” to the actual trend of the product temperature.

In the thermometer models (M), fitted with two probes, setting /7= 1 enables the alarm relating to the second probe (E1).

16

###### **<u>4.3 Temperature control</u>**

The following parameters are used to control the temperature: St, r1, r2, r3, r4 and rd.

###### St: set point, r1 minimum value and r2 maximum value of the set point

Parameter St determines the desired temperature to be maintained inside the cabinet or cold room (set point). Parameters r1 (minimum value) and r2 (maximum) set the range of temperatures for setting the set point.

Note: the set point can be set by pressing the SET button (see par. “Setting the set point (desired temperature value)” page  16).

###### r3: select direct/reverse operation

Defines the operating mode of the device:

- r3=0:  direct with defrost. Used to request the activation of the compressor when the temperature measured by probe 1 rises above the set point. This mode also includes defrost (also called “cooling” mode, see Fig. 4.a)

- r3=1: direct without defrost (Fig. 4.a)

- r3=2: reverse without defrost (Fig. 4.a). Used to request the activation of the compressor when the temperature measured by probe 1 falls below the set point. This mode does NOT include defrost (also called “heating” mode, see Fig. 4.a).

*[Figurtekst: “Direct” mode (cooling) “Reverse” mode (heating) · 1 1 · ON ON · OFF OFF · 2 2 · set point set point · rd rd]*

**Fig. 4.a**

Important: the compressor can also be safeguarded using the parameters that limit the number of activations/hour and the minimum off time (see par. “4.6 Compressor protection” page 19).

###### **<u>4.4  Duty Setting</u>**

Safety function that ensures the operation of the compressor even in the event of a control probe fault. If alarm E0 occurs, duty setting ensures the operation of the compressor until the fault is resolved. The compressor, not being able to be activated according to temperature, works cyclically with an ON time equal to the value assigned to parameter c4 (in minutes) and a fixed OFF time of 15 minutes, see Fig. 4.b.

*[Figurtekst: C4 C4 · ON · compressor OFF · OFF= 15 min.]*

**Fig. 4.b**

###### c4: compressor on time with duty setting

|c4= 0|in the event of an ambient probe fault, the<br>compressor willbe always off|
|---|---|
|c4= 100|the compressor will remain always on; and the<br>f|
|(c4=99<br>foreasy compact)|15 minute off time is not considered.|
|0<c4<100|at the moment a probe error (E0) is detected, the|
|(0<c4<99|duty setting cycle starts from the current status|
|for easy compact)|of the compressor (that is, the status of the<br>compressor is maintained) and the time already<br>elapsed is ignored. The compressor times set by<br>parameters c1, c2, c3 are always observed.|

*[Figurtekst: 1. compressor request;]*

2. probe 1

Important: the operating mode can also be set by external contact connected to the multifunction digital input (parameter A4=9). In this case, the contact controls operation (direct/reverse) with priority over parameter r3.

###### r4: night-time set point delta

Value that automatically increases the set point temperature during the night-time operation time bands.

r4=0: night-time set point= St

r4>0: night-time set point= St + r4

###### Important:

1. to enable night-time operation, not only does r4 need to be set >0, but the digital input must also be enabled and configured (see parameter A4=4 curtain switch/night-time operation) or a night-time time band enables (see par. “4.11 Clock and time band parameters” page 28);

2. night-time operation does not necessarily mean at night, but rather the time bands in which the value of the set point is modified. This usually corresponds to the period in which the refrigerated cabinet is not used (shop closed) and when the curtain is down.

###### rd  Control differential

Value that is added to (or subtracted from, in ‘reverse’ mode) the temperature set point. rd= low values:

- more precise temperature control;

- high compressor On/Off switching frequency in the event of minimum temperature deviations (with the risk of causing damage).

- rd= high values:

- less precise temperature control;

- low compressor On/Off switching frequency in the event of minimum temperature deviations.

###### Duty setting and defrost

If the control probe error occurs when the controller is in defrost mode, the function is not stopped but rather is completed as required; in addition, the defrost can still be performed when called. During the defrost, the duty setting timer is not stopped but rather keeps counting the ON and OFF times.

###### Duty setting and continuous cycle

If the continuous cycle is operating, the controller instantly exits this status and activates duty setting (also for safety reasons, given that during the continuous cycle the low temperature alarm is disabled). To re-activate continuous cycle operation, the ambient probe fault must be resolved. If the probe error is no longer present, the unit returns to normal operation. The compressor again takes on the logic of the control, respecting the times c1, c2, c3.

###### **<u>4.5  Continuous cycle</u>**

The continuous cycle is used to maintain refrigeration continuously active, regardless of the temperature inside the unit. The  function is used to rapidly lower the product temperature, even below the set point, for example after filling the cabinets. In this phase, the temperature may fall below the set point. To activate or deactivate the continuous cycle from the keypad, see paragraph 3.5, the display shows “cc” and the icon flashes (2 flashes, pause).

###### cc: continuous cycle duration

This represents the time in hours that the compressor operates continuously for so as to lower the temperature, even below the set point. If cc=0 the continuous cycle is not activated. The controller exits the continuous cycle procedure after the time set for parameter “cc” has expired, or when reaching the minimum temperature (see the minimum temperature alarm, parameter AL).

17

###### c6: temperature alarm bypass after continuous cycle

This is the time in hours during which all the temperature alarms are deactivated after a continuous cycle. If the temperature of the refrigerated unit, after the continuous cycle, lowers due to inertia below the minimum temperature threshold (set point-AL), the activation of the low temperature alarm is delayed for the time c6. In any case, the continuous cycle is deactivated at the temperature (set point-AL).

###### **<u>4.6 Compressor protection</u>**

The easy, easy compact and easy split controllers are fitted with an automatic compressor protection system to avoid continual starts or stops of the unit. The protection is based on the times in minutes set for parameters c0; c1; c2; c3:

###### c11: second compressor delay (easy split only)

This parameter determines the delay in the activation of the second compressor compared to the main compressor. The parameter has no effect on the deactivation of the compressor.

Important: select the auxiliary output as the second compressor output in parallel (H1 = 5), second compressor with two step control, without rotation (H1 = 6) or second compressor with two step control, with rotation (H1=7).

###### **<u>4.7  Defrost</u>**

For the correct and safe use of the easy, easy compact and easy split controllers, it is essential to program defrost cycles.

###### Type of defrost (parameter d0):

###### c0 compressor and fan start delay on power-up

When the controller is powered-up, this delays the start of the compressor and the evaporator fan (see Fig. 4.c).

###### c1 minimum time between consecutive compressor starts

- Delay between two consecutive starts of the compressor (see Fig. 4.d). Note:

- if the maximum number of starts/hour allowed is 10, simply set c1=6 to ensure this limit is observed.

- as well as c1, also remember that parameter “dd” (dripping time) stops the compressor and the evaporator fan after a defrost..

###### c2/c3 minimum compressor off/on time

These determine the minimum off time (c2) and on time (c3) for the compressor. The compressor will not be controlled until times c2 and c3 have elapsed (see Figs. 4.e and 4.f).

*[Figurtekst: ON · 1 OFF · ON · 2 OFF · ON · 3 OFF · C0 · Fig. 4.c · ON · 2 OFF · ON · 3 OFF · C1 · Fig. 4.d · ON · 2 OFF · ON · 3 OFF · C2 · Fig. 4.e · ON · 2 OFF · ON · 3 OFF · C3 · Fig. 4.f]*

Key to Figs 4.c…4.f

- 1  instrument power-up;

- 2  compressor call;

The defrost may be performed by stopping the compressor, heater or hot gas.

In addition, it can be managed:

- by temperature: using the defrost probe located on the evaporator. In any case, the defrost will end after a maximum settable safety duration. The end defrost for maximum duration alarm “Ed” (parameter A8) can be disabled.

- by time: when there is no defrost probe.

- by time with temperature control (heater only); for a programmable time: the defrost output is only activated when the temperature is below the end defrost threshold, guaranteeing energy saving and defrosting of the evaporator even in more extreme situations (see Fig. 4.g).

*[Figurtekst: 1 · dP · ON · OFF · t · 2 · dt · dt-1 °C · 3 t · ON · OFF · t]*

**Fig. 4.g**

Key

- 1 defrost call;

- 2  defrost temperature probe;

- 3  defrost heater.

|d0|type ofdefrost|type ofend defrost|
|---|---|---|
|0|heater|by temperature|
|1|hotgas||
|2|heater|by time|
|3|hotgas||
|4|heater with temperature control||

**Table 4.e**

Important: on the easy and easy compact models and the easy models without defrost relay, defrost can only be performed by stopping the compressor. In these cases, the defrost may be managed by time (recommended d0=2) or temperature (if the defrost probe is present, recommended d0=0).

3  compressor

18

How to start the defrost:

- from the keypad pressing the DOWN button for 3 s (manual defrost) (for easy split H1 must be ≠4. If H1=4 the UP and DOWN buttons can be pressed together, when H6=1);

- by digital input (in the models where fitted, setting parameter A4=3);

- from the supervisor;

- setting the time bands (if RTC available /enabled);

- at the end of the interval between two defrosts (parameter dI>0);

- when switching the instrument on (parameter d4=1).

Important: the easy compact models, not having the RTC nor the digital input, cannot be set with defrost time bands and cannot be connected to an external contact for defrost management.

###### The defrost may be called, but not activated, in the following cases:

- continuous cycle;

dt: end defrost temperature set point/defrost temperature threshold with temp. control

For the models fitted with end defrost probe, this parameter allows an evaporator temperature to be set at which the defrost is stopped (the evaporator temperature is measured by the defrost probe). The end defrost temperature differential is fixed at 1° C (defrost with temperature control, d0= 4).

If at the start of a defrost cycle with the controlled output by temperature (d0=0, 1) the temperature measured by the probe is greater than the value set for “dt”, the defrost is not performed.

In the event of defrost probe failure, the controller performs a timed defrost with a duration equal to the value set for “dP”. The same is true if the end defrost set point can not be reached, the defrost is stopped after a maximum time equal to the value of dP, and the error Ed is displayed (if enabled by A8) and stays on until a correct defrost cycle is performed.

- dripping (dd>0);

- post-dripping ( Fd>0);

- compressor protectors;

- off status;

- disabling from digital input(A4=2);

- setting the time delay (d5>0) for the defrost function when the instrument is switched on (d4=1);

- direct control mode only without defrost (r3=1) or reverse (r3=2)  (in this case the defrost is not called);

- defrost by temperature (d0=0, 1) and temperature measured by the defrost probe above the end defrost set point (dt).

The defrost ends correctly:

- at the end of the pre-set time (see parameter “dP”);

- once having reached the set temperature  (dt).

When the defrost ends correctly, the dripping (equal to the time set for parameter dd) and post-dripping (parameter Fd) phases start.

The defrost ends early:

- from the keypad, pressing the DOWN button for 3 s (manual end defrost, for easy split H1 must be ≠4 or pressing UP+DOWN together 3 s when H6=1);

- due to an immediate external alarm “IA” ;

- due to a dirty condenser alarm “CHt”;

- by setting direct mode only without defrost (r3=1) or reverse (r3=2);

- switching off;

- when requested from the supervisor;

- from digital input (see parameter A4=2) (the defrost call remains pending).

In these cases, the early end of the defrost is not followed by dripping and post-dripping.

###### Important:

- the defrost is only available in direct mode, that is, when parameters r3=0 or A4=9 (the latter has priority over r3);

- using parameter d0, and according to the model available, type of defrost to be activated can be selected;

- the defrost has priority over normal temperature control; it may also have priority over the compressor protectors (see parameter d9);

- during the defrost, the temperature display can be frozen (see parameter d6);

- the continuous cycle has priority over the defrost

###### Parameters for configuring the defrost dI: interval between defrosts

The defrost is performed periodically at a frequency of every “dI” (in hours or minutes, see parameter dC).

The interval starts counting from the start of the current defrost. If the time is equal to 0 (dI=0), the defrost is not performed, except when activated from the keypad, by digital input, from the supervisor or by time band.

During defrosts the temperature alarms are inhibited.

###### dP: maximum defrost duration

Determines the maximum duration of the defrost (in minutes or seconds, see parameter dC). When defrost by time is set (d0= 2/3/4) dP represents the effective duration of the defrost.

###### d4: defrost when switching the instrument on

Starts a defrost when switching the instrument on (d4= 1). This has priority over the activation of the compressor and the continuous cycle. Running a defrost when switching the instrument on may be useful in special situations (e.g. frequent power failures).

###### Case 1: the system is subject to frequent power failures

In the event of power failures the instrument’s internal clock, which calculates the interval between two defrosts, starting from zero, is reset. If the frequency of the power failure were, in an extreme case, greater than the defrost frequency (e.g. a power failure every 8 hours against a defrost every 10 hours), the controller would never perform a defrost. In this type of situation it is better to activate the defrost when the unit is turned on (d4=1), above all if the defrost is controlled by temperature (probe on the evaporator), so unnecessary defrosts are avoided or at least reduced in duration.

###### Case 2: Systems with many refrigeration units

In this situation, if the defrost on power-up is activated (d4= 1) after a power failure all the units will start a defrost. This may cause overloads. To avoid this, parameter “d5” can be exploited, which allows a delay to be set before the defrost starts, a delay which obviously must be different for each unit.

*[Figurtekst: ON 2 · OFF · ON · dP (1) · OFF unit 1 · [d4(1)= 1] · ON · d5 (2) dP (2) · OFF unit 2 · [d4(2)= 1] · ON · d5 (3) dP (3) · OFF unit 3 · [d4(3)= 1] · 1 · Fig. 4.h]*

*[Figurtekst: Key: · 1  power-up 2  voltage]*

d5: defrost delay on power-up or when enabled by digital input Represents the time which must elapse between when the controller is turned on and the start of the defrost.

The digital input can be used to start a defrost from external contact (see parameter A4=3); d5 represents the delay between when the defrost is enabled, or called, and when it effectively starts.  The defrost from digital input can be exploited to perform defrosts in real time when is the RTC option is not fitted. Simply connect a timer to the multifunction digital input.

19

The defrost will be activated when the timer contact is closed. In the case where more than unit is connected to the same timer, it is recommended to set parameter d5 to delay the defrosts to a different time for each unit. Furthermore, to avoid unnecessary defrosts controlled by the instrument’s internal clock, it is suggested to set parameter dI=0 (only manual defrosts from the keypad or multifunction contact) or to set dI to a value which is greater than the maximum set interval.

###### <u>A4 Meaning d5 3 start defrost on closing delay between call and efective start f</u>

###### **Table 4.f**

The parameter dC=1 can be useful to:

- test the operation of the defrost function with reduced times;

- manage air driers. The defrost cycle thus becomes the condensate drain cycle, which must occur at close intervals (minutes) and for very brief durations (seconds).

Important: this parameter should not be used (dC= 1) if the defrost requires the activation of the compressor (hot gas) and when d9=1, as otherwise the compressor may be damaged due to a number high of consecutive starts.

###### d6: freeze control temperature display during defrost

This function locks the display of the ambient temperature during the defrost cycle at the last value read before the current defrost (d6= 1).

d6= 0 display the message “dF” alternating with the temperature measured by the control probe;

d6= 1 freeze the display on the last temperature measured before the defrost.

The display normally returns when the measurement first reaches the set point or, in any case, after the set alarm bypass time after defrost (parameter d8).

The freeze mode is also valid for the display of the second and third probe, if enabled (parameter /4).

###### dd: dripping time

This parameter forces the compressor and the evaporator fans off after a defrost, in order to allow the evaporator to drip.

The value of this parameter indicates the number of minutes the compressor and fan are off. If dd = 0 no dripping is set, therefore at end defrost the compressor starts immediately.

*[Figurtekst: 1 ON · OFF · ON · 2 OFF · ON · 3 OFF · dd · Fig. 4.i]*

- 1  defrost;

###### **<u>4.8  Alarm parameters</u>**

The alarms can be set as regards the threshold, type and activation delays. When an alarm occurs, the unit may stop normal operation and warn that the alarm situation has occurred, based on the type of alarm.

###### A0: alarm and fan temperature differential

This represents the differential used to activate the high and low temperature alarms (“AH”, “AL”) and for the management of the fan. In the event of an alarm, as seen in the figure, the value of “A0” determines the actual activation of the temperature alarms.

The value of “A0” (negative or positive) defines the nature of alarms “AL” and “AH” (absolute or relative, respectively), in detail:

- A0≤ 0 AL and AH expressed as absolutes

A0> 0 AL and AH expressed relative to the set point (St or St + r4 in night-time operation)

*[Figurtekst: 1 2 · A0 A0 · AL AH · set point · Fig. 4.j]*

*[Figurtekst: 1  low temperature alarm; · 2  high temperature alarm.]*

2  start compressor call;

3  compressor.

###### d8: alarm bypass time after defrost

The parameter has two effects:

1. it delays the temperature alarm signal after a defrost;

2. it delays the temperature alarm signal after opening the door. In this case, it is only active when A7=0.

###### d9: defrost priority over compressor protectors

Cancels the compressor protection times (c0, c1, c2, c3) at the start of the defrost. The possible values are:

AL: absolute or relative temperature for low temperature alarm Determines the activation threshold of the low temperature alarm.

|AL|Low temperature|Low temperature|Alarm disabled|
|---|---|---|---|
||alarm (normal) if...|alarm (night-time)<br>if...|if...|
|absolute|temp.probe 1 ≤ AL|temp.probe 1 ≤ AL|AL= -50|
|relative|temp. probe 1 ≤<br>St - AL|temp. probe 1 ≤ St +<br>r4 - AL|AL= 0|

###### **Table 4.h**

d9= 0 protection times observed;

d9= 1 protection times ignored; the defrost has higher priority and the compressor times are not observed.

It is useful, for example, with hot gas defrost to avoid delaying the defrost in the case where the compressor has just stopped and there is a minimum time between two starts. Remember, however, that in this case the maximum number of activations per hour of the compressor may not be respected.

###### d/: defrost probe reading

Used to display the value measured by the defrost probe on the instruments where this is fitted.

###### dC: time base

Used to modify the unit of measure used to count the times for parameters dI (defrost interval) and dP (defrost duration). The following values are available:

AH: absolute or relative temperature for high temperature alarm Determines the activation threshold of the high temperature alarm.

|AH|High temperature<br>alarm (normal) if...|High temperature<br>alarm (night-time)<br>if...|Alarm disabled<br>if...|
|---|---|---|---|
|absolute|temp.probe 1 ≥ AH|temp.probe 1 ≥ AH|AH= 150|
|relative|Temp. probe 1 ≥ St<br>+ AH|temp. probe 1 ≥ St +<br>r4 + AH|AH= 0|
||||**Table 4.i**|

Note: the low and high temperature alarms are automatically reset - this means that if the temperature returns within the allowed range, the alarm signal is automatically cancelled. During a high or low temperature alarm, the message “HI” or “LO”, respectively, flashes on the display alternating with the temperature; if fitted, the buzzer is activated.

|dC|dI<br>|dP|
|---|---|---|
|0|hours|minutes<br>|
|1|minutes|seconds<br>**Table 4.g**|

20

###### Ad: temperature alarm delay

Indicates after how many minutes the temperature alarm is signalled from when it is detected. If the temperature, after the delay Ad, is within the allowed limits, the alarm is not signalled. Setting a delay to signal of the temperature alarms may help eliminate false alarms due to interference on the probe signal or situations lasting a short time (for example, opening the cold room door briefly). The temperature alarm delay has no effect on two special functions: defrost and continuous cycle. To delay any temperature alarms after these functions, parameter d8 for defrost and c6 for continuous cycle must be modified. Remember that during defrost and continuous cycle no temperature alarms are generated. Def.: Ad=0 (instant temperature alarm).

A4:  3rd input configuration (easy compact)

The multifunction input is only available on the easy models with three inputs; is not available on the easy compact models. This parameter is used to set the functions of the input.

- easy, easy compact <u>A4 Meaning 0 Input not active</u> 1 External alarm: instant (A7= 0) or delayed (A7>0) Input open= alarm <u>Input closed= ok</u>

- 2 Enable defrost Input open= disabled <u>Input closed= enabled</u>

- 3 Start defrost when closing MODEL M: select probe displayed Input open= probe 1 <u>Input closed= probe 2</u>

- 4 Curtain switch or night-time operation Input open= normal set point <u>Input closed= night-time set point [r4]</u>

- 5 Remote ON – OFF Input open= OFF <u>Input closed= ON</u>

- 6 Direct operation of AUX output when H1= 3 Input open= AUX de-energised <u>Input closed= AUX energised</u>

- 7 Door switch with evaporator fans off ‘dor’ alarm:  - instant (A7= 0) or delayed (A7>0) - operation of AUX output (H1= 3) Input open= door open <u>Input closed= door closed</u>

- 8 Door switch with evaporator fans and compressor off ‘dor’ alarm:  - instant (A7= 0) or delayed (A7>0)

- operation of AUX output (H1= 3) Input open= door open <u>Input closed= door closed</u>

- 9 Direct / reverse operating mode IF r3 = 0 input open= direct + defrost input closed= reverse

- IF r3 = 1 / 2 input open= direct <u>input closed= reverse</u>

- <u>10 Probe for dirty condenser alarm 11 Product probe</u>

###### **Table 4.j**

###### <u>A4=0 multifunction input disabled</u>

The multifunction input is not activated and cannot be used as a digital or analogue input.

###### <u>A4=1 external alarm</u>

contact open= alarm detected contact closed= normal operation.

When A4=1 easy can be connected to an external contact for immediately signalling alarms. The alarm signal can be delayed by setting parameter A7.

The activation of the alarm brings about a message on the display ((see par. “5.1 Table of alarms and signals” on page 31), activates the buzzer (if featured), and stops the compressor due to external alarm (immediate if A7=0), while the fan continues operating according to parameters F0, F1, F2, F3, Fd.

If the external alarm is detected during a defrost or a continuous cycle, the controller stops these (without completing dripping and postdripping for defrosts). When the alarm ceases, the unit resumes normal operation, and then:

- the continuous cycle (cc) can be performed again;

- defrosts can be performed;

- the compressor will start after the time set for parameter c2 (minimum compressor off time.

###### <u>A4=2 Enable defrost</u>

contact open= not enabled contact closed= enabled.

When A4=2 easy can be connected to an external contact for enabling the defrost; this will then be activated only if the contact is closed and after the delay set for parameter d5.

If the contact is closed when a defrost in progress, the defrost is immediately stopped and the unit resumes normal operation (without performing the dripping or post-dripping phases). The LED starts flashing indicating that the defrost call is still pending, awaiting enabling (closing of the contact), when the defrost restarts (the timer dP is set to zero).

###### <u>A4=3 Start defrost on closing</u>

The defrost call is generated when the digital input switches from open to closed.

When A4=3 easy can be connected to an external contact for starting the defrost when the contact closes. Setting dI=0 (no interval between two defrosts) and without any time bands enabled, closing the external contact will immediately start the defrost.

This function is useful for running timed defrosts without the RTC on board (used to set the defrost time bands). To do this, simply connect a mechanical or electronic timer to the digital input and set A4=3 to guarantee the defrost cycles.

A series of units can be connected to the same timer. In this case, to prevent all the defrosts from starting at the same time, set parameter d5 to different times for each unit connected (see Fig. 4.k).

In models PJEZM* this is used to select the probe whose value is displayed by the instrument: contact open= probe 1 contact closed= probe 2.

*[Figurtekst: 2 · 3 · dP (1) · unit 1 · d5 (2) dP (2) · unit 2 · d5 (3) dP (3) · unit 3 · 1 · Fig. 4.k · Key: · 1 defrost call; · 2  open; · 3  closed.]*

<u>A4=4  Curtain switch and night-time operation</u>

contact open=  curtain raised, normal operation

contact closed= curtain lowered and night-time operation

When A4=4 easy can be connected to an external contact for managing the opening and the closing of the curtain on the refrigerated cabinet and activating night-time operation.

21

###### Important:

1. when the contact is closed the temperature set point becomes the night-time setting and consequently the value of “st” is increased (“direct” mode) or decreased (“reverse” mode) by the value of r4;

2. night-time operation does not necessarily mean at night, but rather the time bands in which the value of the set point is modified. This usually corresponds to the period in which the refrigerated cabinet is not used (shop closed) and when the curtain is down.

|Contact|Operation|Operating mode|Set point|
|---|---|---|---|
|open|normal|direct / reverse|St|
|closed|night-time|direct|St + r4|
|||reverse|St-r4|
||||**Table 4.k**|

###### <u>A4=5 Remote ON – OFF</u> contact open= controller off

contact closed=  controller on.

When A4=5 easy can be connected to an external contact for switching instrument on/off. ON–OFF from external contact has priority over the keypad and the supervisor.

See par. “3.5 Functions available from the keypad” page 15 for further details on the functions of the instrument when OFF.

###### <u>A4=6 Direct operation of AUX output with H1=3</u>

contact open= AUX output not active

contact closed=  AUX output active

When A4=6 easy can be connected to an external contact for controlling the auxiliary output (H1=3 auxiliary output linked to the digital input).

###### <u>A4=7 Door switch with evaporator fans off</u>

contact open= door open contact closed=  door closed

This is used to signal the door open alarm and stop the evaporator fan. See paragraph 4.9 “Door open/closed management“.

- “cht” dirty condenser pre-alarm:

- indicates that the limit between Ac and AE has been exceeded (deriving from the calculation: Ac-AE/2, see Fig. 4.l);

- easy continues normal operation;

- automatic reset (if the temperature measured by probe 3 falls below Ac-AE);

- “cht” is shown on the display, alternating with the current temperature.

“CHt” dirty condenser alarm:

- indicates that the temperature set point Ac has been exceeded (see Fig. 4.l);

- the delay time Acd has elapsed;

- easy stops all functions;

- the buzzer sounds (to mute this, press SET or to disable deactivate set H4=1);

- “CHt” is shown on the display, alternating with “cht” and the current temperature.

Important: the “CHt” alarm (see par. “5.1 Table of alarms and signals” on page 31) can only be reset manually, or alternatively by switching the controller off, pressing UP for 3 s or powering down (on power-up, if the temperature is still above the “Ac”, the alarm will go off again).

*[Figurtekst: 3 · AC-AE/2 · 1 · AC-AE AC · 2 · Fig. 4.l]*

- 1  condensing temperature;

- 2  “cht” pre-alarm, display only (automatic reset);

- 3  “CHt” alarm and refrigeration “OFF” (manual reset).

###### <u>A4= 11: Product probe</u>

- 3rd input (terminal 11) configured as product probe

###### <u>A4=8 Door switch with evaporator fan and compressor of</u>

contact open= door open

contact closed=  door closed

See A4=7 with the addition of shutting down the compressor during the pre-alarm (A7 or d8). Enabling the digital input A4=8 has priority over the compressor protection parameters (c0, c1, c2, c3). See paragraph 4.9 “Door open/closed management“.

###### <u>A4= 9 Direct/reverse operating mode</u>

contact open= direct operation

contact closed= reverse operation

Parameter A4=9 has priority over parameter r3; only r3= 0 specifies the activation of the defrost control.

|r3|contact|result|
|---|---|---|
|0|open|Direct operation with defrost control|
||closed|Reverse operation|
|1|open|Direct operation|
||closed|Reverse operation|
|2|open|Direct operation|
||closed|Reverse operation|

###### **Table 4.l**

###### <u>A4= 10 Probe for dirty condenser alarm</u>

Multifunction analogue alarm input and dirty condenser pre-alarm, using the third probe.

To enable this function, set:

1. third probe;

2. parameter Ac: temperature set point above which easy signals the dirty condenser alarm;

3. parameter AE: temperature differential that, together with Ac, determines the dirty condenser pre-alarm;

4. parameter Acd: dirty condenser alarm signal delay;

5. parameter A4=10: enable the probe and dirty condenser alarm.

The input is used in analogue mode for probe 3 (product).

Below is a summary table of the relation between parameter A4 and the actuators:

||alarm|outpu<br>AUX|ts<br>FAN|COMP|
|---|---|---|---|---|
|A4= 1|”IA”|-|-|P|
|A4= 6|-|P|-|-|
|A4= 7|”dor”|P|P|-|
|A4= 8|”dor”|P|P|P|
|||||**Table 4.m**|

A4:  3rd input configuration (easy split)

This paragraph highlights the differences in the setting of parameter A4 for easy, easy compact and easy split.

- easy split <u>A4 Meaning 0 Input not active</u> 1 Instant (A7= 0) or delayed (A7 >0) external alarm Input open= alarm <u>Input closed= ok</u>

- 2 Enable defrost Input open= disabled <u>Input closed= enabled</u>

- 3 Start defrost when closing FOR MODEL M: select probe displayed Input open=probe 1 <u>Input closed=probe 2</u>

- 4 Curtain switch or night-time operation Input open= normal set point and light on (H1=4) <u>Input closed= night-time set point [r4] and light off (H1=4)</u>

- 5 Remote ON–OFF Input open= OFF <u>Input closed= ON</u>

- 6 Direct operation of AUX output when H1=3 Input open= AUX de-energised <u>Input closed= AUX energised</u>

22

###### easy split

- <u>A4 Meaning</u> 7 Door switch with fan off and light not managed (see parameter Ado) “dor” alarm: - instant (A7= 0) or delayed (A7 >0) - operation of AUX output (H1= 3)

- Input open = door open <u>Input closed = door closed</u>

- 8 Door switch with fan and compressor off and light not managed (see parameter  Ado) “dor” alarm : - instant (A7= 0) or delayed (A7 >0) - operation of AUX output (H1= 3)

- Input open = door open <u>Input closed = door closed</u>

- 9 Direct / reverse operating mode IF r3= 0 input open= direct + defrost input closed= reverse

- IF r3= 1/2 input open= direct <u>input closed= reverse</u>

- 10 Door switch with evaporator fan off and light managed (see parameter <u>Ado)</u>

- 11 Door switch with evaporator fan and compressor off and light <u>managed (see parameter Ado)</u>

- <u>12 Select EASY SET from digital input 13 Probe for dirty condenser alarm 14 Product probe</u>

###### **Table 4.o**

<u>A4=0, 1, 2, 3:</u> see A4=0, 1, 2, 3 for easy, easy compact in previous paragraph.

###### **Other alarm parameters**

A7: digital input alarm delay

Sets the delay (in minutes) for detecting the external alarm when A4= 1, 7 or 8. For easy split A4 must be =1,7,8,10,11.

A8: enable alarm “Ed” (end defrost by timeout)

The alarm ‘Ed’ signals the end defrost due to the “maximum defrost time” (dP) being reached. This can be disabled, by setting A8=0. The signal “Ed” disappears when the next defrost is called.

Ac: Dirty condenser alarm set point

Sets the temperature set point above which the dirty condenser alarm “CHt” is signalled (see parameter A4=10 for easy, easy compact and A4=13 for easy split).

AE: Dirty condenser alarm differential temperature

Sets the temperature value for determining the dirty condenser prealarm “cht” interval (see parameter A4=10 for easy, easy compact and A4=13 for easy split).

Acd: dirty condenser alarm delay

Sets the delay in minutes before activating the dirty condenser alarm “CHt”’ (see par. A4=10 for easy, easy compact and A4=13 for easy split).

<u>A4=4 Curtain switch and night-time operation</u>

See the previous paragraph. In easy split models if the light output is configured (H1=4) in normal operation the light is on and in night-time operation it is off.

<u>A4=5, 6</u> see A4=5, 6 for easy, easy compact in previous paragraph.

<u>A4=7 Door switch with evaporator fan off and light not managed</u>

See A4=7 for easy, easy compact in previous paragraph. In easy split models with light output configured (H1=4), the status of the light output remains unchanged. See paragraph 4.9 “Door open/closed management”.

<u>A4=8 Door switch with evap. fan and comp. of and light not managed. f</u>

See A4=8 for easy, easy compact in previous paragraph. In easy split models with light output configured (H1=4), the status of the light output remains unchanged. See paragraph 4.9 “Door open/closed management”.

<u>A4=9:</u> See A4=9 for easy, easy compact in previous paragraph.

<u>A4=10: Door switch with evaporator fan off and light managed</u>

See paragraph 4.9 “Door open/closed management”.

<u>A4=11: Door switch with evaporator fan and comp. of and light managedf</u>

See paragraph 4.9 “Door open/closed management”.

<u>A4=12: Select EASY SET from digital input</u>

Used to select the set of control parameters control according to the status of the digital input.

Digital input open = easy set 1

Digital input closed = easy set 2

The easy set from digital input has higher priority than parameter EZY; this means that any attempt to change the easy set using parameter EZY is ignored if A4 = 12.

<u>A4 = 13: Probe for dirty condenser alarm</u>

See A4=10 for easy, easy compact in previous paragraph.

<u>A4 = 14: Product probe</u>

See A4=11 for easy, easy compact in previous paragraph.

Summary table of relationship between parameter A4 and the actuators:

||||output|||
|---|---|---|---|---|---|
||alarm|light|AUX|FAN|COMP|
|A4=1|”IA”|-|-|-|P|
|A4=6|-|-|P|-|-|
|A4=7|”dor”|-|P|P|-|
|A4=8|”dor”|-|P|P|P|
|A4=10|-|P|P|P|-|
|A4=11|-|P|P|P|P|

###### **<u>4.9  Door open/closed management</u>**

Procedure for setting the digital input:

1. make sure that the cold room door is fitted with a contact for signalling when the door is opened and closed;

2. establish the time required (parameters: A7 time in minutes or d8 in hours ≠0) to enable the pre-alarm on the display and to stop the evaporator fan;

3. enable the digital input A4=7, 8. For easy split A4 must be =7,8,10,11.

When the door is opened, the controller will start counting the prealarm time if A7 or d8 are other than zero. If, on the other hand, A7=0 and d8=0 the alarm will be activated immediately and the display will show “dor” alternating with the temperature reading. The alarm can only be reset when the door is closed, or alternatively when switching off the controller by pressing UP for 3 s (on power-up, if the door is still open, the pre-alarm time will start counting again).

Important: setting A7=0 and d8=0 ignores the pre-alarm times, the display will show “dor” alternating with the temperature and the fan will not stop.

Special cases:

- continuous cycle: performed normally, however the evaporator fan is stopped based on the times set for A7;

- defrost: performed normally and the activation of the fan is controlled using parameter F3 (evaporator fan status during defrost). If F3=1 the digital input will only signal the opening of the door, without having any effect on the fan.

###### **Easy and easy compact**

During the pre-alarm (A7 or d8≠0):

- the fan is stopped;

- the LEDs and temperature display flash (excluding the compressor LED, if on);

- the high temperature alarms are disabled.

During the “dor” alarm (at the end of the pre-alarm A7 or d8):

- the fan resumes normal operation;

- the display will show “dor” alternating with the temperature;

- the high temperature alarms are enabled;

- the buzzer sounds (to mute this, press SET or to disable set H4=1);

- if the auxiliary AUX output is “linked” to the digital input (H1=3) the auxiliary relay will be activated.

**Table 4.p**

23

Example: Setting A4=7 and A7=10 on a cold room with door contact, when the door is opened, the LED and the temperature will flash on the display for 10 minutes (excluding the compressor LED) and the fan will stop. After 10 minutes, if the door is still open, the fan will resume normal operation and the display will show the “dor” signal alternating with the temperature value displayed.

<u>Closing the door the first time:</u>

the controller maintains the previous status:

- the fans and/or compressor (see parameter ‘A4’) remain off;

- the light is kept on if an output is configured as the light output (H1 = 4);

- the temperature and the alarm icon (bell) flash;

- the high temperature alarms remains disabled.

###### **Easy split**

In easy split models the algorithm for managing the door depends on the type of unit selected, according to parameter Ado, and the setting of parameter A4.

###### Ado = 0: display case

###### <u>Opening the door:</u>

When opening the door, if parameter A7 or d8 ≠0, the controller goes into pre-alarm status:

- the temperature displayed and the alarm icon (bell) flash;

- the high temperature alarm is disabled;

- if A4=7, 10 the fan is stopped;

- if A4=8, 11 the fan and the compressor are stopped;

- if A4=10, 11 and if the light output is configured (H1=4), the light is on.

<u>If the door remains open for a time greater than A7, the controller goes</u> into alarm status:

- the temperature displayed flashes alternating with ‘dor’;

- the buzzer is activated;

- the light remains on if an output is configured as the light output (H1=4);

- the high temperature alarm is enabled, after the delay Ad;

- the auxiliary relay is activated if H1 = 3;

- the fan is ON;

- if A4=8, 11 the compressor is restarted, observing any protection times (‘c’ parameters);

###### <u>Closing the door:</u>

The controller resumes normal operation:

- the fans and the compressor are started if called (observing any protection times – ‘c’ parameters)

- the light is switched off if an output is configured as the light output (H1= 4);

- the auxiliary relay is deactivated if H1 = 3;

- the buzzer is deactivated;

- the temperature stops flashing and the alarm icon (bell) goes off;

- the high temperature alarm is enabled after the delay Ad.

###### Ado = 1: cold room

Assuming the user enters the cold room, closing the door behind him, and then exits the room, closing the door a second time. If the user enters the cold room and then leaves immediately, closing the door, the controller waits until the door is opened a second time and if this does not occur within a certain time (A7 or d8), normal operation resumes.

###### <u>Opening the door the first time:</u>

When opening the door, if parameters A7 and d8 are≠0, the controller goes into pre-alarm status:

- the temperature displayed and the alarm icon (bell) flash;

- the high temperature alarm is disabled;

- if A4=7, 10 the fan is stopped;

- <u>If, after first closing, the door remains closed for a time greater than  A7,</u>

the controller resumes normal operation:

- the fans and/or compressors are switched on if called; when the compressor restarts the protection times must be observed (‘c’ parameters)

- the light remains on if an output is configured as the light output (H1 = 4);

- the high temperature alarm is enabled after the delay Ad;

- the temperature stops flashing and the alarm icon (bell) goes off.

Note: assuming the user has already left the cold room, and in that case will be able to turn off the light from the outside by pressing the DOWN button, or alternatively is still working inside. If, after first closing, the light is switched off manually (the user is outside the cold room), the controller resumes normal operation without waiting for the door to open a second time:

- the fans and/or compressors are switched on if called; when the compressor restarts the protection times must be observed (‘c’ parameters);

- the high temperature alarm is enabled after the delay Ad;

- the temperature stops flashing and the alarm icon (bell) goes off.

<u>Opening the door the second time: status unchanged.</u>

###### <u>Closing the door the second time:</u>

- the fans and/or compressors are switched on if called; when the compressor restarts the protection times must be observed (‘c’ parameters)

- the high temperature alarm is enabled after the delay Ad;

- the light is off if an output is configured as the light output (H1= 4).

###### **4.10  Evaporator fan management** **<u>parameters</u>**

The fan is activated based on the parameter settings and the status of the controller.

The evaporator fan control temperature is measured by probe 2, (connector 10).

To know which output is associated with the fan, see the wiring diagram for the “easy” model used (see par. “2.2 Electrical connections” page 11).

Important: these parameters are not available in the compact models.

In normal operation, the evaporator fan can be managed as follows:

   - always on (F0= 0);

   - on according to the evaporator temperature (F0= 1; F1);

   - off when the compressor is off (F2= 1);

   - activated in cyclical on/off mode (when the compressor is off - easy split only).

- if A4=8, 11 the fan and the compressor are stopped;

- if A4=10, 11 and if the light output is configured (H1=4), the light is activated;

<u>If the door remains open for a time greater than A7, the controller goes</u> into alarm status:

- the fans and compressor are started if called; when restarting the compressor the protection times are observed (‘c’ parameters);

- the light remains on if an output is configured as the light output (H1= 4);

- the auxiliary relay is energised if H1 = 3;

- the temperature displayed flashes alternating with ‘dor’;

- the buzzer is activated;

- the high temperature alarm is enabled after the delay Ad.

During defrost, the status of the evaporator fan is determined by parameter F3:

- controlled according to F0 (F3= 0);

- off (F3= 1).

The fan remains off:

- during the dripping period, if parameter dd≠0;

- during the post-dripping period, if parameter Fd≠0;

- for a time equal to c0 after instrument power-on, if parameter c0≠0.

- F0: enable evaporator fan control

F0= 0 the fan is on;

F0= 1 the fan is controlled based on a set point (see parameter F1). If the evaporator probe is faulty, the fan operates.

24

###### F1: evaporator fan control set point

The controller starts the fans only when the temperature of the evaporator is below the value F1-A0. F1 is the real temperature value and not the deviation from the set point. Once off, the fans start again when the difference between the probe reading and the set point is equal to +A0, where A0 is the fan controller differential.

###### When F0= 1:

- evaporator temperature < F1– A0, the fan is ON;

- evaporator temperature > F1, the fan is off.

*[Figurtekst: evap. temp. · F1 · F1-A0 · ON · evap. · fan t · OFF · Fig. 4.m]*

###### F2: stop evaporator fans if compressor stops

- F2= 0 the fan operates according to F0 even when the compressor is off; F2= 1 the fan is off when the compressor is off;

F2=2 (easy split only): the fan is managed in cyclical on/off mode. The on and off times can be configured by parameters F4 and F5 respectively. The on and off sequence after control is deactivated starts with the ON phase, so as to exploit the fact that the evaporator is still cold.

*[Figurtekst: ON · CP · OFF · t · ON · FAN · OFF · t · F4 F5 F4 F4 F5 F4 F5]*

*[Figurtekst: F4 Fan ON time t time · F5 Fan OFF time FAN fans · CP Compressor]*

###### **<u>4.11 Clock and time band parameters</u>**

The RTC (Real Time Clock), not available on the easy compact models, is used to manage the defrost function, curtain switch/night-time operation and AUX output in real time. The user can enable/disable the clock and set the current time using dedicated parameters.

In particular, up to 4 time bands can be set for managing the defrosts, one band for managing night-time operation and one for activating the AUX output.

The clock alarm fault “EtC” is activated only if the clock is effectively used, that is, has been enabled, the time has been set and there is at least one valid time band.

###### Setting the clock:

1. press the SET button for more than 3 s (if there are active alarms, first mute the buzzer) the display shows the parameter code “PS” (password);

2. press the SET button to access the password setting and use the UP and DOWN buttons to scroll the numbers until displaying “22” (password to access the configuration parameters);

3. press the SET button to confirm the password;

4. use the UP and DOWN buttons to scroll the names of the parameters until reaching the parameter tEn;

5. press SET to display the value associated with the parameter;

6. use the UP and DOWN buttons until reaching the value 1 for enabling the clock;

7. press SET to temporarily save the new value and display the parameter again;

8. repeat the operation to set the values of the parameters dAY (day of the week), hr (hours), Min (minutes). For easy split, also set YEr, Mon, dMo;

9. at the end of the operations, press the SET button for more than 3 seconds to permanently save the selected values and exit.

###### Setting the time bands:

Perform the operations from point 1 to point 7 above, then:

- select the parameter relating to the required band (e.g. d1d= DEFROST TIME BAND 1 DAY setting);

- press SET to display the status of the parameter;

- use the UP and DOWN buttons until reaching the desired value;

- press SET to temporarily save the new value and return to the previous display;

- repeat the operation to set the values of the parameters d1h (TIME BAND 1 HOUR setting), d1m (TIME BAND 1 MINUTES setting)

- at the end of the operations, press the SET button for more than 3 seconds to permanently save the selected values and exit.

###### F3: evaporator fan status during defrost

F3= 0 the fan is on during the defrost; F3= 1 the fan is off during the defrost.

###### Fd: post-dripping time

The fans, after the defrost, can stay off for a further period (in minutes) beyond dd, defined by the value of Fd. This is useful to allow the evaporator to return to operating temperature after defrost, thus avoiding blowing “warm” air into the refrigerated environment.

If management by fan controller is selected, no time needs to be set for Fd as the controller starts the fans again when the evaporator has reached the correct temperature. If the fan controller is active (F0 = 1), setting to Fd a value ≠ 0, the fans remain off for a time equal to the value of Fd regardless of the evaporator temperature.

###### F4: fan ON time (with F2 = 2) (easy split only)

This parameter only has meaning when F2 = 2.

It defines the time expressed in minutes within the period (F4 + F5) during which the fans are on without being called.

###### RTC clock parameters

tEn enable RTC (tEn=1 RTC enabled) YEr (easy split only): current year; Mon (easy split only): current month; dMo (easy split only): day of the month; dAY: current day of the week (1…7= Monday to Sunday); hr current hour (24 h) Min current minutes

Example: to set the current time and date to 15.07 on Thursday 3 May 2007, set: tEn=1,

YEr=07, Mon=05, dMo=03 (easy split only) dAY=4, hr=15, Min=7

The controller will save the time and the day of the week, month and year (on easy and easy compact controllers the month and year are ignored).

Note: the instrument does not manage automatic changeover to daylight saving.

###### F5: fan OFF time (with F2 = 2) (easy split only)

This parameter only has meaning when F2 = 2.

It defines the time expressed in minutes within the period (F4 + F5) during which the fans are off without being called.

25

Parameters for setting up to 4 defrost time bands d1d…d4d Defrost event day setting

d1d…d4d=0 no defrost event

d1d…d4d=1…7 Monday to Sunday d1d…d4d=8 from Monday to Friday d1d…d4d=9 from Monday to Saturday d1d…d4d=10 Saturday & Sunday d1d…d4d=11 every day

d1h…d4h Defrost event hour setting (24h) d1M…d4M Defrost event minutes setting

###### **<u>4.12  Rapid parameter set selection (EZY)</u>**

The easy, easy compact and easy split controllers feature the EZY parameter (on the compact models, this is called EY), which is used to quickly choose a list of parameters, with corresponding values, for the control of the refrigeration system.

By setting parameter EZY=1, 2, 3, 4, one of the 4 lists made up of a maximum of 25 parameters (for the lists see par. “5.9 Table of EZY parameter sets” page 36). The values in the chosen list overwrite the corresponding operating parameters.

###### Note:

Example: To program a defrost call (d1d) every Saturday & Sunday at 19.31, set: d1d=10 (days) d1h=19 (hours), d1M=31 (min).

**Important:** the defrost event only involves a defrost call. Whether the defrost is effectively run and the duration of the cycle depend on the status of the controller when the call is activated.

Parameters for setting the night-time set point time band

nOd Night-time set point time band day setting nOd= 0 no event set nOd= 1…7 Monday to Sunday nOd= 8 from Monday to Friday nOd= 9 from Monday to Saturday nOd= 10 Saturday & Sunday nOd=11 every day nOh Night-time band set point start hours nOM Night-time band set point start minutes nFd Night-time band set point end day nFh Night-time band set point end hours nFM Night-time band set point end minutes

In easy split models, entering night time band involves the automatic modification of the set point and the light output (if H1=4)

Example: To program the night-time set point (nOd) every day from 12.31 to 13.29, set: nOd=11 (days), nOh=12 (start hours), nOM=31 (start minutes), nFh=13 (end hours) and nFM=29 (end minutes). During night-time operation, the set point is varied: night-time set point = st +r4 (in direct mode), night-time set point = st -r4 (in reverse mode). Where featured, the protective curtain also closes the cabinet (A4=4).

###### Parameters for setting the AUX output activation time band

AOd AUX output activation time band day setting AOd= 0 no event set AOd= 1…7 Monday to Sunday AOd= 8 from Monday to Friday AOd= 9 from Monday to Saturday AOd= 10 Saturday & Sunday AOd= 11 every day AOh AUX output activation time band start hours AOM AUX output activation time band start minutes AFd AUX output deactivation time band end day AFh AUX output activation time band end hours AFM AUX output activation time band end minutes

Example: To program the activation of the AUX output every day from 12.31 at 13.29, set: AOd=11 (days), AOh=12 (start hours), AOM=31 (start minutes), AFh=13 (end hours) and AFM=29 (end minutes).

**Important** : the activation the AUX output activation time band is linked to parameters H1=3 and A4≠6/7/8 and for easy split A4≠10,11.

- to restore the selected rapid parameter set at any time, turn the controller off and on again, while holding SET. The display shows “CE” to indicate that the selected rapid set (EZY= 1, 2, 3, 4) has again overwritten the operating parameters, thus restoring the original set of parameters;

- to restore all the parameters and return to the original default values (factory settings), turn the controller off and on again while holding DOWN and SET, until the display shows “CF”. Use this procedure with extreme care, as it may compromise the fundamental control settings;

- EZY=0 brings no change;

- on the thermometer models (PJEZM*), the EZY parameter (EY for the easy compact models) is not featured.

###### **<u>4.13  Other settings</u>**

The operation of the device is completed by a series of additional functions, such as the assignment of a supervisor serial network address, the configuration of the AUX relay, the enabling of the keypad and the buzzer.

###### H0: serial address

Assigns the instrument an identification address for connecting to a supervisory or telemaintenance system (def. H0=1).

###### H1: AUX output configuration

Establishes the operating logic of the auxiliary relay; in particular defines whether it is used as an alarm output or as an auxiliary output linked to the digital input. On easy split models there are also the light and second compressor outputs, with or without rotation.

- H1= 0 no function associated with the output H1=1 alarm output: norm. energised (relay de-energised with alarm)

- H1=2 alarm output: norm. de-energised (relay energised with alarm)

- H1=3 AUX output related to Dig. in. - easy, easy compact : A4 = [6/7/8]; - easy split: A4 = [6/7/8/10/11]; Dig. in. OPEN = AUX de-energised Dig. in. CLOSED = AUX energised + LED “AUX” display”

- H1=4 light output (easy split only): the light can be switched on pressing the corresponding button from the keypad or when opening the door if the door switch is activated with light management (see parameter Ado)

- H1=5 second compressor output in parallel (easy split only): the output is activated a few seconds after the activation of the first compressor (delay = c11). The second compressor observes the protection times c0, c1, c2, c3 for the first compressor;

- H1=6 second compressor output with two step control without rotation (easy split only): the second compressor is called when the temperature measured by the room probe deviates by more than half the differential (rd/2) from the set point;

26

*[Figurtekst: AMB_T · St+rd · St+rd/2 · St · t · ON · CP1 · OFF · t · ON · CP2 · OFF · t · ON · CP2 D · OFF · ON · CP1 D · OFF · t · rd/2 rd/2 · St · Fig. 4.o · Key · AMB_T Control probe CP2 Compressor 2 · CP1 Compressor 1 rd Differential · t time St Set point]*

- H1=7 second compressor output with two step control with rotation (easy split only). The roles of main and secondary compressor alternate following each shutdown, so that when next started (stopped) the output not involved in the previous start (stop). will be activated (deactivated). Both the compressors must observe the protection times c0, c1, c2 and  c3.

###### Examples of operation:

*[Figurtekst: example 1 · ON · REQ1 · OFF · t · ON · REQ2 · OFF · t · ON · CP1 · OFF · t · ON · CP2 · OFF · t · Fig. 4.p]*

*[Figurtekst: example 2 · ON · REQ1 · OFF · t · ON · REQ2 · OFF · t · ON · CP1 · OFF · t · ON · CP2 · OFF · t · Fig. 4.q · example 3 · ON · REQ1 · OFF · t · ON · REQ2 · OFF · t · CP1 ON · OFF · t · ON · CP2 · OFF · t · Fig. 4.r · example 4 · ON · REQ1 · OFF · t · ON · REQ2 · OFF · t · ON · CP1 · OFF · t · ON · CP2 · OFF · t · Fig. 4.s · Key · REQ1 Compressor 1 call CP1 Compressor 1 · REQ2 Compressor 2 call CP2 Compressor 2 · t time]*

27

###### Note:

- in mode H1= 1/2, the alarms that act on the AUX output are: “LO”,  “HI”, “E0”, “IA”, “CHT”;

- mode H1= 1 is useful for signalling an alarm when a power failure occurs

###### H2: enable keypad

Used to prevent the set point and the other operating parameters from being changed when the instrument is located in a place that is accessible to the public.

- H2= 0 keypad disabled:

- F parameters read-only

- C parameters modifiable (with password)

- no set point modification

- no manual defrost

- no continuous cycle

- no ON/OFF

H2=1 keypad enabled H2=2 keypad enabled except for ON/OFF

###### H4: disable buzzer

Setting H4= 1 disables the operation of the audible buzzer.

###### H5: ID code

Display-only value: this can only be modified via serial connection (key or supervisor). When set to a positive value (values from 0 to 31 are used by CAREL for the basic models), if a parameter, including the set point, is modified from the keypad, the value becomes negative. This allows any modifications made the parameters compared to the initial settings to be monitored.

H6: select control associated with UP + DOWN buttons (easy split only) The following values are allowed:

- H6 = 0: start/stop continuous cycle;

- H6 = 1: start/stop defrost.

H7: management of fourth relay/serial communication (easy split only) This parameter is used to enable the fourth relay output (RL4). In models with four relays, management of the fourth relay and serial communication are mutually exclusive.

H7 = 0: fourth relay disabled and serial communication enabled; H7 = 1: fourth relay enabled and serial communication disabled. (see paragraph “2.3 Wiring diagram for multiple units” page 13).

###### PS: password

Protection code for modifying the configuration parameters (default= 22). The value of the password can be customised from the supervisor.

HMP: Maximum maintenance interval (easy split only) This function requires the internal clock (RTC) to be enabled (tEn=1). If HMP = 0, the maintenance request is deactivated. Parameter HMP, expressed in days, is used to set the maximum time interval after which the controller generates a maintenance request (the counter HMd has exceeded the threshold HMP), which involves a message shown on the display (SrC) and the alarm icon on. The signal can be deactivated by setting parameter HMr = 1 from the keypad or supervisor. This operation saves the current date and restarts the counter HMd.

HMd: Days elapsed since last maintenance (easy split only) Read-only parameter. See the explanation of parameter HMP.

HMr: reset maintenance signal and restart HMd (easy split only) If set to 1, this deactivates the signal SrC and restarts the counter HMd. Operation available from the keypad and supervisor.

###### **5.  TABLES OF ALARMS AND PARAMETERS**

###### **<u>5.1  Table of alarms and signals</u>**

When an alarm is activated, the display shows the corresponding message that flashes alternating with the temperature; if fitted and enabled, the buzzer and the alarm relay are also activated. All the alarms have automatic reset (that is, they stop when the causes are no longer present), except for alarm ‘CHt’ which has manual reset (instrument on/off using the UP button or by disconnecting the power supply). Pressing the SET button mutes the buzzer, while the code displayed and the alarm relay only go off when the causes of the alarm have been resolved. The alarm codes are shown in the table below:

Note: in easy split controllers, when starting control (powering up the controller and/or switching from OFF status), the high temperature alarm signal is disabled until the first time the compressor stops, to avoid false signals. The first time the compressor stops indicates that the set temperature has been reached, and, consequently, the high temperature alarm signal is enabled. This function is always active.

The possible alarm codes are shown in the following table:

|alarm<br>code|buzzer and<br>alarm relay|LED|alarm description|reset|ENABLE ALARM parameters<br>involved|easy|easy<br>compact|easy<br>split|
|---|---|---|---|---|---|---|---|---|
|E0|active|ON|probe 1 error= control|automatic|-||||
|E1|not active|ON|probe 2 error= defrost|automatic|d0= 0/1/4,F0= 1||||
|E2|not active|ON|probe 3 error= condenser/product|automatic|easy, easy compact [A4=10/11]<br>easysplit[A4=13/14]||-||
|IA|active|ON|external alarm|automatic|[A4 = 1] [+A7]||-||
|dOr|active|ON|open door alarm|automatic|easy, easy compact  [A4=7/8][+A7]<br>easysplit[A4=7/8/10/11][+A7]||-||
|LO|active|ON|low temperature alarm|automatic|[AL] [Ad]||||
|HI|active|ON|high temperature alarm|automatic|[AH] [Ad]||||
|EE|not active|ON|unitparameter error|notpossible|-||||
|EF|not active|ON|operating parameter error|manual<br>i|-||||
|Ed|not active|ON|defrost ended by timeout|on first defrost ended<br>correctly|[dP] [dt] [d4] [A8]||||
|dF|not active|OFF|defrost running|automatic|[d6=0]||||
|cht|not active|ON|dirty condenser pre-alarm|automatic|easy, easy compact [A4=10]<br>easysplit[A4=13]||-||
|CHt|active|ON|dirty condenser alarm|manual|easy, easy compact [A4=10]<br>easysplit[A4=13]||-||
|EtC|not active|ON|clock alarm|bysettingthe time|if bands are active||-||
|SrC (easy<br>split only)|not active|ON|maintenance request signal|manual,<br>set HMr=1|[HMP] [HMd] [HMr]|-|-||

**Table 5.a**

28

###### **5.2 Description of the main signals and** **<u>alarms</u>**

###### LED flashing

The activation of the corresponding function is delayed by a timer, awaiting an external signal or disabled by another procedure that is already in progress. e.g. if is a continuous cycle in progress and a defrost is called, the latter will remain pending until the end of the continuous cycle, and the corresponding LED (defrost) will flash.

###### **<u>5.3 Data error</u>**

In certain operating conditions, the instrument may detect errors in the data saved. These errors may compromise the correct operation of the instrument. If the microprocessor detects a data saving error, the display shows the message “EE”. If the fault persists, the controller needs to be replaced. If, on the other hand, the message disappears, it can continue to be used. When “EE” error occurs frequently and/or remains for some time, the controller should be checked, as the original precision may not be guaranteed.

E0 steady or flashing

control probe error:

- probe not working: the probe signal is interrupted or short-circuited;

- probe not compatible with the instrument;

The alarm signal E0 is steady if it is the only active alarm (the temperature value is not displayed), while it flashes if other alarms are active or the second probe is displayed.

###### E1 flashing

evaporator probe or food conservation probe error:

- probe not working, the probe signal is interrupted or short-circuited;

- probe not compatible with the instrument;

###### E2 flashing

condenser probe or food conservation probe error:

- probe not working, the probe signal is interrupted or short-circuited;

- probe not compatible with the instrument;

###### IA flashing

immediate or delayed alarm from multifunction digital input:

- check the multifunction input and parameters A4 and A7.

###### dOr flashing

open door alarm:

- check the multifunction input and parameters A4 and A7.

###### LO flashing

low temperature alarm. The probe has measured a temperature lower than the set point by a value that exceeds parameter AL:

- check parameters AL, Ad and A0.

The alarm is automatically reset when the temperature returns within the set limits (see parameter AL).

###### HI flashing

high temperature alarm. The probe has measured a temperature higher than the set point by a value that exceeds parameter AH.

- check parameters AH, Ad and A0.

The alarm is automatically reset when the temperature returns within the set limits (see parameter AH).

EE displayed during operation or on power-up

unit parameter reading error. See Data errors.

EF displayed during operation or on power-up

operating parameter reading error. See Data errors.

###### **<u>5.4  Modifying the parameters</u>**

###### **Parameter navigation**

The operating parameters, modifiable using the keypad, are divided into two types: frequent (type F) and configuration (type C). Access to the latter is protected by password (default= 22) to prevent accidental or unauthorised modifications.

###### Accessing the type F parameters:

- press the SET button for more than 3 s (if there are active alarms, mute the buzzer). The display shows the parameter code ‘PS’ (password);

- use the UP and DOWN buttons to scroll the parameters. The LED corresponding to the category of parameters will be on (see Table 5.b);

- press SET to display the value associated with the parameter

- increase or decrease the value using the UP or DOWN button respectively;

- press SET to temporarily save the new value and display the param. again;

- repeat the procedure for any other parameters that need to be modified;

- press the SET button for more than 3 s to permanently save the parameters and exit the parameter setting procedure.

###### Accessing the type C parameters:

- press the SET button for more than 3 s (if there are active alarms, mute the buzzer), the display shows the parameter code “PS” (password);

- press the SET button to access the password setting;

- use the UP and DOWN buttons to scroll the numbers until displaying “22” (password to access the parameters);

- press the SET button to confirm the password;

- use the UP and DOWN buttons to scroll the parameters. The LED corresponding to the category of parameters will be on (see Table 5.b);

- press SET to display the value associated with the parameter;

- increase or decrease the value using the UP or DOWN button respectively;

- press SET to temporarily save the new value and display the param. again;

- repeat the procedure for any other parameters that need to be modified;

- press the SET button for more than 3 s to permanently save the parameters and exit the parameter setting procedure.

###### Ed flashing

The last defrost ended after exceeding the maximum duration rather than when reaching the end defrost set point.

- check parameters dt, dP and d4;

Warnings: if no button is pressed for 60 s, all the changes made to the parameters, temporarily saved in the RAM, will be cancelled and the previous settings restored.

- check the efficiency of the defrost.

The message disappears when the next defrost ends correctly.

###### dF flashing

defrost running:

- this is not an alarm signal, but rather a message that the instrument is running a defrost. Only shown if d6= 0.

###### cht flashing

dirty condenser pre-alarm:

- check parameters A4, Ac, AE and Acd.

###### CHt flashing

dirty condenser alarm:

- check parameters A4, Ac, AE and Acd.

EtC flashing internal clock error.

The dAY, hr, Min dMo*, Mom*, YEr* parameters are not restored, as these are saved instantly when entered(*= easy split only).

If power is disconnected from the instrument before saving the settings (pressing the SET button for 3 s), all the changes made to the parameters and temporarily saved will be lost.

|Category|Initial|Icon|
|---|---|---|
|Probe parameters|/|-|
|Control parameters|r|-|
|Compressor parameters|c||
|Defrost parameters|d||
|Alarm parameters|A||
|Fan parameters|F||
|AUX output configuration parameters|H1||
|RTC parameters|-||
|||**Table 5.b**|

SrC flashing (easy split only) Maintenance request signal. Displayed only if parameter HMP≠0.

29

###### **<u>5.5  Setting the default parameters</u>**

running this procedure overwrites any custom parameter settings.

To reset the default parameters:

- disconnect power from the instrument;

- reconnect power while holding the SET and DOWN buttons;

- the display will show the message “CF”;

- after a few seconds the instrument starts operating with the default configuration. Any different parameter settings will need to be updated.

###### **<u>5.6  Table of easy parameters</u>**

|Par.|Description|Type|Min|Max|UOM.|Def.|Parameter visible in models|
|---|---|---|---|---|---|---|---|
|PS|password|F|0|200|-|22|M/S (with 1 & 2 probes) X Y C|
|/2|probe measurement stability|C|1|15|-|4|, , ,<br>M/S (with 1 & 2 probes), X, Y, C|
|/4|select probe displayed|F|1|3|-|1|M/ S (with 2 probes) X Y C|
|/5|<br>select°C/°F|C|0(°C)|1(°F)|-|0|, , ,<br>M/ S (with 1 &  2 probes), X, Y, C|
|/6|disable decimal point|C|0|1|-|0|M/S (with 1 & 2 probes), X, Y, C|
|/7|<br>enable probe 2 alarm (model M only)<br>f|C|0|1|-|0|<br>M|
|/C1|probe 1 offset<br>f|F|-50.0|50.0|(°C/°F)|0|M/S (with 1 & 2 probes), X, Y, C|
|/C2|f<br>probe 2 offset<br>f|F|-50.0|50.0|(°C/°F|0|M/S (with 2 probes), X, Y, C|
|/C3|f<br>probe 3 offset|F|-50.0|50.0|(°C/°F)|0|M/S (with 2 probes), X, Y, C|
|St|set point<br>f|S|r1|r2|°C/°F|4|M/S (with 1 & 2 probes), X, Y, C|
|rd|control differential<br>|F|0|19.0|°C/°F|2|S (with 1 & 2 probes), X, Y, C<br>|
|r1|minimum set point value|C|-50|r2|°C/°F|-50|M/S (with 1 & 2 probes), X, Y, C|
|r2|maximum set point value|C|r1|200|°C/°F|90|S (with 1 & 2 probes), X, Y, C|
|r3|select direct/reverse operation|C|0|2|-|0|M/S (with 2 probes), X, Y, C|
|r4|night-time set point delta|C|-50|50|°C/°F|3|S (with 1 & 2 probes), X, Y, C|
|c0|compressor and fan start delay on power-up|C|0|100|min|0|S (with 1 & 2 probes), X, Y, C|
|c1|<br>minimum time between consecutive compressor starts<br>f|C|0|100|min|0|S (with 1 & 2 probes), X, Y, C|
|c2|minimum compressor offtime|C|0|100|min|0|S (with 1 & 2 probes), X, Y, C|
|c3|minimum compressor on time<br>|C<br>|0|100|min|0|S (with 1 & 2 probes), X, Y, C<br>|
|c4|compressor on time with duty setting|C|0|100|min|0|S (with 1 & 2 probes), X, Y, C|
|cc|<br>continuous cycle duration|C|0|15|h|4|<br>S (with 1 & 2 probes), X, Y, C|
|c6|temperature alarm bypass after continuous cycle|C|0|15|h|2|S (with 1 & 2 probes), X, Y, C|
|d0|type of defrost|C|0|4|-|0|S (with 1 & 2 probes), X, Y, C|
|dI|<br>interval between defrosts|F|0|199|h/min (see dC)|8|<br>S (with 1 & 2 probes), X,Y, C|
|dt|end defrost temperature set point/defrost temperature|F|-50|130|°C/°F|4|S (with 2 probes), X, Y, C|
||<br>threshold with temp. control|||||||
|dP|<br>maximum defrost duration|F|1|199|min/s (see dC)|30|S (with 1 & 2 probes), X, Y, C|
|d4|defrost when switching the instrument on|C|0|1|-|0|<br>S (with 1 & 2 probes), X, Y, C|
|d5<br>|defrost delay on power-up or when enabled by digital input<br>|C<br>|0<br>|199<br>|min|0<br>|S (with 1 & 2 probes), X, Y, C<br>|
|d6<br>dd|freeze control temperature display during defrost<br>dripping time|C<br>F|0<br>0|1<br>15|-<br>min|1<br>2|S (with 1 & 2 probes), X, Y, C<br>S (with 1 & 2 probes), X, Y, C|
|d8|<br>alarm bypass time after defrost|F|0|15|h|1|<br>S (with 1 & 2 probes), X, Y, C|
|d9|defrost priority over compressor protectors|C|0|1|-|0|S (with 1 & 2 probes), X, Y, C|
|d/|<br>defrost probe reading (2)|F|-|-|°C/°F|-|<br>S (with 2 probes), X, Y, C,|
|dC|time base|C|0|1|-|0|S (with 1 & 2 probes), X, Y, C|
|A0|alarm and fan temperature differential|C|-20|20.0|°C/°F|2|M/S (with 1 & 2 probes), X, Y, C|
|AL|f<br>absolute/relative temperature for low temperature alarm|F|-50|250|°C/°F|0|M/S (with 1 & 2 probes), X, Y, C|
|AH|absolute/relative temperature for high temperature alarm|F|-50|250|°C/°F|0|M/S (with 1 & 2 probes) X Y C|
|Ad|<br>temperature alarm delay<br>i|C|0|199|min|0|, , ,<br>M/S (with 1 & 2 probes), X, Y, C|
|A4<br>|3rd input configuration<br>|C<br>|0<br>|11<br>|-<br>|0<br>|M/S (with 2 probes), X, Y, C<br>|
|A7<br>A8|digital input alarm delay<br>enable alarm“Ed”(end defrost by timeout)|C<br>C|0<br>0|199<br>1|min<br>-|0<br>0|M/S (with 2 probes), X, Y, C<br>S (with 2 probes) X Y C|
|Ac|<br>set point dirty condenser alarm<br>f|C|-50|250|°C/°F|70|, , ,<br>M/S (with 2 probes), X, Y, C|
|AE|dirty condenser alarm differential temperature|C|0.1|20.0|°C/°F|5.0|M/S (with 2 probes),X, Y, C|
|Acd|f <br>dirty condenser alarm delay|C|0|250|min|0|<br>M/S (with 2 probes), X, Y, C|
|F0|enable evaporator fan control|C|0|1|-|0|C|
|F1<br>|evaporator fan control set point<br>|F<br>|-50<br>|130<br>|°C/°F|+5<br>|C<br>|
|F2|stop evaporator fan if compressor of|C|0|1|-|1|C|
|F3|evaporator fan status during defrost|C|0|1|-|1|C|
|Fd|<br>post-dripping time|F|0|15|min|1|C|
|H0|serial address|C|0|207|-|1|M/S (with 1 & 2 probes), X, Y, C|
|H1<br>|AUX output configuration<br>|C<br>|0<br>|3|-|0|<br>M/S (with 1 & 2 probes), X, Y, C<br>|
|H2|enable keypad|C|0|1|-|1|M/S (with 1 & 2 probes), X, Y, C|
|H4|<br>disable buzzer|C|0|1|-|0|<br>M/S (with 1 & 2 robes) X Y C|
|H5|<br>ID code (read-only)|F|0|199|-|-|p, , ,<br>M/S (with 1 & 2 probes), X, Y, C|
|EZY|rapid parameter set selection|C|0|4|-|0|<br>S (with 1 & 2 probes), X, Y, C|
|tEn|enable RTC|C|0|1|-|0|X Y C (*)|
|d1d|<br>defrost time band 1st day|C|0|11|days|0|, ,<br>X, Y, C (*)|
|d1h|<br>time band 1st hour|C|0|23|h|0|<br>X, Y, C (*)|
|d1M<br>d2d|time band 1st minute<br>defrost time band 2nd da|C<br>C|0<br>0|59<br>11|min<br>das|0<br>0|X, Y, C (*)<br>X Y C (*)|
|d2h|y<br>time band 2nd hour|C|0|23|y<br>h|0|, ,<br>X, Y, C (*)|

30

|Par.|Description|Type|Min|Max|UOM.|Def.|Parameter visible in models|
|---|---|---|---|---|---|---|---|
|d2M|time band 2nd minute|C|0|59|min|0|X, Y, C (*)|
|d3d|defrost time band 3rd day|C|0|11|days|0|X, Y, C (*)|
|d3h|time band 3rd hour|C|0|23|h|0|X, Y, C (*)|
|d3M|time band 3rd minute|C|0|59|min|0|X, Y, C (*)|
|d4d|defrost time band 4th day|C|0|11|days|0|X, Y, C (*)|
|d4h|time band 4th hour|C|0|23|h|0|X, Y, C (*)|
|d4M|time band 4th minute|C|0|59|min|0|X, Y, C (*)|
|nOd|night time band ON day|C|0|11|days|0|X, Y, C (*)|
|nOh|night time band ON hours|C|0|23|h|0|X, Y, C (*)|
|nOM|night time band ON minutes|C|0|59|min|0|X, Y, C (*)|
|nFd|night time band OFF day|C|0|11|days|0|X, Y, C (*)|
|nFh|night time band OFF hours|C|0|23|h|0|X, Y, C (*)|
|nFM|night time band OFF minutes|C|0|59|min|0|X, Y, C (*)|
|AOd|AUX time band ON day|C|0|11|days|0|X, Y, C (*)|
|AOh|AUX time band ON hours|C|0|23|h|0|X, Y, C (*)|
|AOM|AUX time band ON minutes|C|0|59|min|0|X, Y, C (*)|
|AFd|AUX time band OFF day|C|0|11|days|0|X, Y, C (*)|
|AFh|AUX time band OFF hours|C|0|23|h|0|X, Y, C (*)|
|AFM|AUX time band OFF minutes|C|0|59|min|0|X, Y, C (*)|
|dAY|RTC day of the week|C|1|7|days|1|X, Y, C (*)|
|hr|RTC hours|C|0|23|h|0|X, Y, C (*)|
|Min|RTC minutes|C|0|59|min|0|X, Y, C (*)|

**Table 5.c**

(*) Parameters not visible in models without RTC

###### **<u>5.7  Table of easy compact parameters</u>**

|Par.|Description|Type|Min|Max|UOM.|Def.|Parameter visible in models|
|---|---|---|---|---|---|---|---|
|PS|password|F|0|99|-|22|S (with 1 & 2 probes),  M (with 1 & 2 probes)|
|/2<br>|probe measurement stability<br>|C<br>|1|15|-|4|S (with 1 & 2 probes),  M (with 1 & 2 probes)<br>|
|/4|select probe displayed|F|1|2|-|1|S (with  2 probes), M (with 2 probes).|
|/5|select°C/°F|C|0|1|-|0|S (with 1 & 2 probes), M (with 1 & 2 probes)|
|/6|disable decimal point|C|0|1|-|0|S (with 1 & 2 probes), M (with 1 & 2 probes)|
|/7|enable probe 2 alarm (model M only)<br> f|C|0|1|0|0|M<br>|
|/C1|probe 1 offset<br> f|F|-50.0|50.0|°C/°F|0|S (with 1 & 2 probes), M (with 1 & 2 probes)<br>|
|/C2|probe 2 offset|F|-50.0|50.0|°C/°F|0|S (with  2 probes), M (with 2 probes)|
|St|set point<br>f|S|r1|r2|°C/°F|4|S (with 1 & 2 probes),  M (with 1 & 2 probes)|
|rd|control differential|F|0|19.0|°C/°F|2|S (with 1 & 2 probes)|
|r1|minimum set point value|C|-50.0|r2|°C/°F|-50|S (with 1 & 2 probes),  M (with 1 & 2 probes)|
|r2|maximum set point value|C|r1|99|°C/°F|90|S (with 1 & 2 probes),  M (with 1 & 2 probes)|
|r3|select direct/reverse operation|C|0|2|-|0|S (with 1 & 2 probes)|
|c0|compressor and fan start delay on power-up|C|0|100|min|0|S (with 1 & 2 probes)|
|c1|minimum time between consecutive compressor starts<br> f|C|0|100|min|0|S (with 1 & 2 probes)|
|c2|minimum compressor offtime|C|0|100|min|0|S (with 1 & 2 probes)|
|c3|minimum compressor on time|C|0|100|min|0|S (with 1 & 2 probes)|
|c4|compressor on time with duty setting|C|0|100|min|0|S (with 1 & 2 probes)|
|cc|continuous cycle duration|C|0|15|h|4|S (with 1 & 2 probes)|
|c6|temperature alarm bypass after continuous cycle|C|0|15|h|2|S (with 1 & 2 probes)|
|d0|type of defrost|C|0|4|-|0|S (with 1 & 2 probes)|
|dI|interval between defrosts|F|0|199|h/min(dC)|8|S (with 1 & 2 probes)|
|dt|end defrost temperature set point|F|-50|130|°C/°F|4|S (with 2 probes)|
|dP|maximum defrost duration|F|1|199|min/s (dC)|30|S (with 1 & 2 probes)|
|d4|defrost when switching the instrument on|C|0|1|-|0|S (with 1 & 2 probes)|
|d5|<br>defrost delay on power-up or when enabled by digital input|C|0|199|min|0|<br>S (with 1 & 2 probes)|
|d6|freeze control temperature display during defrost|C|0|1|-|1|S (with 1 & 2 probes)|
|dd|dripping time|F|0|15|min|2|S (with 1 & 2 probes)|
|d8<br>|alarm bypass time after defrost<br>|F<br>|0<br>|15|h|1<br>|S (with 1 & 2 probes)<br>|
|d9<br>|defrost priority over compressor protectors<br>|C|0|1|-|0|S (with 1 & 2 probes)<br>|
|d/|defrost probe reading (2)|F|-|-|°C/°F|-|S (with 2 probes)|
|dC|<br>time base|C|0|1|-|0|<br>S (with 1 & 2 probes)|
|A0|alarm and fan temperature differential|C|-20|+20|°C/°F|2|S (with 1 & 2 probes)|
|AL|f<br>absolute/relative temperature for low temperature alarm|F|-50|+99|°C/°F|0|<br>S (with 1 & 2 probes)|
|AH|absolute/relative temperature for high temperature alarm|F|-50|+99|°C/°F|0|S (with 1 & 2 probes)|
|Ad|temperature alarm delay|C|0|199|min|0|S (with 1 & 2 probes)|
|A8|enable alarm“Ed”(end defrost by timeout)|C|0|1|-|0|S (with 2 probes)|
|H0|serial address<br>i|C|0|207|-|1|S (with 1 & 2 probes), M (with 1 & 2 probes)|
|H1|AUX output configuration|C|0|2|-|0|S (with 1 & 2 probes), M (with 1 & 2 probes)|
|H2|i<br>enable keypad|C|0|2|-|1|<br>S (with 1 & 2 probes), M (with 1 & 2 probes)|
|H5|<br>ID code (read-only)|F|1|+199|-|0|S (with 1 & 2 probes), M (with 1 & 2 probes)|
|EY|rapid parameter set selection|C|0|4|-|0|S (with 1 & 2 probes)|
||||||||**Table 5.d**|

Warning  the easy compact models only display two digits. If the range is below -99 and above 99, the terminal will display “- - “.

31

###### **<u>5.8  Table of easy split parameters</u>**

|Par.<br>PS|Description<br>Type<br>Min<br>Max<br>password<br>F<br>0<br>200|UOM<br>-|Def.<br>Visibility<br>22<br>SC|
|---|---|---|---|
|/2<br>|probe measurement stability<br>C<br>1<br>15<br> <br><br><br>|-|,<br>4<br>S,C<br><br>|
|/3<br>|probe display rate<br>C<br>0<br>15<br> <br><br><br>|-|0<br>S,C<br><br>|
|/4<br>/5<br>/6|select probe displayed<br>F<br>1<br>3<br>select°C/°F<br>C<br>0<br>1<br>disable decimal point<br>C<br>0<br>1|-<br>-<br>-|1<br>S,C<br>0<br>S,C<br>0<br>SC|
|/C1<br>|<br><br><br><br>probe 1 offset<br>F<br>-50<br>50<br> f<br><br><br>|(°C/°F)<br>°°|,<br>0<br>S,C<br><br>|
|/C2<br>/C3|probe 2 offset<br>F<br>-50<br>50<br>probe 3 offset<br>F<br>-50<br>50|(C/F)<br>(°C/°F)|0<br>S,C<br>0<br>S,C|
|/P|f<br>select type of probe<br>C<br>0<br>1|-|0<br>S,C|
|St<br>|set point<br>F<br>r1<br>r2<br>f<br><br><br>|°C/°F<br>°°|4<br>S,C<br><br>|
|rd<br>r1|differential<br>F<br>0<br>19<br>minimum set point value<br>C<br>-50<br>r2|C/F<br>°C/°F|2<br>S,C<br>-50<br>S,C|
|r2<br>r3|maximum set point value<br>C<br>r1<br>300<br>select direct/reverse operation<br>C<br>0<br>2|°C/°F<br>-|90<br>S,C<br>0<br>SC|
|r4<br>|<br><br><br><br>night-time set point delta<br>C<br>-50<br>+50<br> <br><br><br>|°C/°F<br>|,<br>3<br>S,C<br><br>|
|c0|compressor and fan start delay on power-up<br>C<br>0<br>100<br> <br>|min|0<br>S,C<br>|
|c1|minimum time between consecutive compressor starts<br>C<br>0<br>100<br>f|min|0<br>S,C|
|c2<br>c3|minimum compressor offtime<br>C<br>0<br>100<br>minimum comressor on time<br>C<br>0<br>100|min<br>min|0<br>S,C<br>0<br>SC|
|c4<br>|p<br><br><br><br>compressor on time with duty setting<br>C<br>0<br>100<br> <br><br><br>|min<br>|,<br>0<br>S,C<br><br>|
|cc<br>c6|continuous cycle duration<br>C<br>0<br>15<br>temperature alarm bypass after continuous cycle<br>C<br>0<br>15|h<br>h|4<br>S,C<br>2<br>S,C|
|c11<br>d0|<br>second compressor delay<br>C<br>0<br>250<br>te of defrost<br>C<br>0<br>4|s<br>-|4<br>S,C<br>0<br>SC|
|dI|yp<br> <br> <br> <br>interval between defrosts<br>F<br>0<br>199|h/min<br>(see dC)|<br>,<br>8<br>S,C|
|dt<br>dP|end defrost temperature set point/defrost temperature threshold with temp. control<br>F<br>-50<br>300<br>maximum defrost duration<br>F<br>1<br>199|°C/°F<br>min/s|4<br>S,C<br>30<br>SC|
|d4<br>|<br> <br> <br> <br>defrost when switching the instrument on<br>C<br>0<br>1<br>  <br> <br> <br>|<br>-<br>|<br>,<br>0<br>S,C<br> <br>|
|d5|defrost delay on power-up or when enabled by digital input<br>C<br>0<br>199|min|0<br>S,C|
|d6|freeze control temperature display during defrost<br>C<br>0<br>1|-|1<br>S,C|
|dd|<br>dripping time<br>F<br>0<br>15|min|2<br>SC|
|d8<br>|<br> <br> <br> <br>alarm bypass time after defrost<br>F<br>0<br>15<br> <br> <br> <br>|<br>h|<br>,<br>1<br>S,C<br> <br>|
|d9<br>d/<br>dC|defrost priority over compressor protectors<br>C<br>0<br>1<br>defrost probe reading<br>F<br>-<br>-<br>time base<br>C<br>0<br>1|-<br>°C/°F<br>-|0<br>S,C<br>-<br>S,C<br>0<br>S,C|
|A0<br>AL|alarm and fan temperature differential<br>C<br>-20<br>20<br>absolute/relative temerature for low temerature alarm<br>F<br>-50<br>300|°C/°F<br>°C/°F|2<br>S,C<br>0<br>SC|
|AH<br>|p   p<br> <br> <br> <br>absolute/relative temperature for high temperature alarm<br>F<br>-50<br>300<br> <br> <br> <br>|<br>°C/°F<br>|<br>,<br>0<br>S,C<br> <br>|
|Ad|temperature alarm delay<br>C<br>0<br>199<br>i|min|0<br>S,C|
|A4|3rd input configuration<br>C<br>0<br>14|-|0<br>S,C|
|A7<br>A8|i <br>digital alarm input delay<br>C<br>0<br>199<br>bl l“Ed”d df b i<br>C<br>0<br>1|min|0<br>S,C<br>0<br>SC|
|Ac<br>|enae aarm(en erost y tmeout)<br> <br> <br> <br>dirty condenser alarm set point<br>C<br>-50<br>300<br> f <br>|-<br>°C/°F<br>|<br>,<br>70<br>S,C<br>|
|AE<br>Acd|dirty condenser alarm differential temperature<br>C<br>0.1<br>20.0<br>dirty condenser alarm delay<br>C<br>0<br>250|°C/°F<br>min|5<br>S,C<br>0<br>S,C|
|Ado<br>|<br>door management algorithm<br>C<br>0<br>1<br>bl  f l<br> <br> <br>|-|0<br>S,C<br> <br>|
|F0<br>|enae evaporator an contro<br>C<br>0<br>1<br> <br> <br> <br>|-<br>°°|0<br>C<br> <br>|
|F1|evaporator fan control set point<br>F<br>-50<br>300<br> f|C/F|5<br>C|
|F2|stop evaporator fan if compressor off<br>C<br>0<br>2|-|1<br>C|
|F3|f<br>evaporator fan status during defrost<br>C<br>0<br>1|-|1<br>C|
|Fd<br>F4<br>|<br>post-dripping time<br>F<br>0<br>15<br>fan ON time (when F2=2)<br>C<br>0<br>100<br>  <br> <br> <br>|min<br>min<br>|1<br>C<br>5<br>C<br> <br>|
|F5|fan OFF time (when F2=2)<br>C<br>0<br>100|min|10<br>C|
|H0|serial address<br>C<br>0<br>207|-|1<br>S,C|
|H1|AUX output configuration<br>C<br>0<br>7|-|4<br>SC|
|H2|i <br><br> <br> <br>enable kead<br>C<br>0<br>2|-|<br>,<br>1<br>SC|
|H4<br>|yp<br> <br> <br> <br>disable buzzer<br>C<br>0<br>1<br>  <br><br> <br>|-|<br>,<br>0<br>S,C<br> <br>|
|H5|ID code (read-only)<br>F<br>1<br>199|-|0<br>S,C|
|H6|select control associated with UP + DOWN buttons<br>C<br>0<br>1|-|1<br>S,C|
|H7|management of fourth relay/serial communication<br>C<br>0<br>1|-|1<br>C|
|EZY<br>|<br> <br> <br> <br>rapid parameter set selection<br>C<br>0<br>4<br> <br> <br> <br>|-|<br><br>0<br>S,C<br> <br> *|
|tEn<br>d1d<br>d1h|enable RTC<br>C<br>0<br>1<br>defrost time band 1st day<br>C<br>0<br>11<br>time band 1st hour<br>C<br>0<br>23|-<br>day<br>h|0<br>S,C ()<br>0<br>S,C (*)<br>0<br>S,C (*)|
|d1M|time band 1st minutes<br>C<br>0<br>59|min|<br>0<br>SC (*)|
|d2d<br>|<br> <br> <br> <br>defrost time band 2nd day<br>C<br>0<br>11<br> <br> <br> <br>|<br>day<br>|<br>,<br>0<br>S,C (*)<br> <br> *|
|d2h<br>d2M|time band 2nd hours<br>C<br>0<br>23<br>time band 2nd minutes<br>C<br>0<br>59|h<br>min|0<br>S,C ()<br>0<br>S,C (*)|
|d3d|defrost time band 3rd day<br>C<br>0<br>11|day|0<br>S,C (*)|
|d3h|<br>time band 3rd hours<br>C<br>0<br>23|<br>h|<br>0<br>SC (*)|
|d3M<br>d4d|<br> <br> <br> <br>time band 3rd minutes<br>C<br>0<br>59<br>defrost time band 4th day<br>C<br>0<br>11|<br>min<br>day|<br>,<br>0<br>S,C (*)<br>0<br>S,C (*)|
|d4h|time band 4th hours<br>C<br>0<br>23|h|0<br>S,C (*)|
|d4M|time band 4th minutes<br>C<br>0<br>59|min|0<br>S,C (*)|
|nOd<br>nOh<br>|night time band ON day<br>C<br>0<br>11<br>night time band ON hours<br>C<br>0<br>23<br> <br>|day<br>h|<br>0<br>S,C (*)<br>0<br>S,C (*)<br>|
|nOM<br>nFd|night time band ON minutes<br>C<br>0<br>59<br>night time band OFF day<br>C<br>0<br>11|min<br>day|0<br>S,C (*)<br>0<br>S,C (*)|

32

|Par.|Description|Type|Min|Max|UOM|Def.|Visibility|
|---|---|---|---|---|---|---|---|
|nFh|night time band OFF hours|C|0|23|h|0|S,C (*)|
|nFM|night time band OFF minutes|C|0|59|min|0|S,C (*)|
|AOd|AUX time band ON day|C|0|11|day|0|S,C (*)|
|AOh|<br>AUX time band ON hours|C|0|23|<br>h|0|S,C (*)|
|AOM|AUX time band ON minutes|C|0|59|min|0|S,C (*)|
|AFd|AUX time band OFF day|C|0|11|day|0|S,C (*)|
|AFh|AUX time band OFF hours|C|0|23|h|0|S,C (*)|
|AFM|AUX time band OFF minutes|C|0|59|min|0|S,C (*)|
|YEr|RTC: year|C|0|99|year|0|S,C (*)|
|Mon|RTC: month|C|1|12|month|1|S,C (*)|
|dMo|RTC: day of the month|C|1|31|day|1|S,C (*)|
|dAY|RTC: day of the week|C|1|7|day|1|S,C (*)|
|hr|RTC: hours|C|0|23|h|0|S,C (*)|
|MIn|RTC: minutes|C|0|59|min|0|S,C (*)|
|HMP|maximum maintenance interval|C|0|999|day|0|S,C (*)|
|HMd|days elapsed since last maintenance|C|0|999|day|0|S,C (*)|
|HMr|reset maintenance signal and restart HMd|F|0|1|-|0|S,C (*)|
||||||||**Table 5.e**|

(*) Parameters not visible in models without RTC

###### **<u>5.9  Table of EZY parameter sets</u>**

easy parameter sets (EZY)

|Par.|Description|mo|dels S-X (no|rmal tempe|rature)|m|odels Y-C  (l|ow temper|ature)|
|---|---|---|---|---|---|---|---|---|---|
|||EZY=1|EZY=2|EZY=3|EZY=4|EZY=1|EZY=2|EZY=3|EZY=4|
|/4|select probe displayed|1|1|1|1|-|-|-|-|
|/5|select°C/°F<br>f|0|0|0|0|-|-|-|-|
|rd|control differential|3.0|3.0|5.0|2.0|3.0|4.0|5.0|2.0|
|r1|f<br>minimum set point value|-10.0|-15.0|-20.0|-30.0|-30.0|-30.0|-30.0|-30.0|
|r2|maximum set point value|15.0|20.0|20.0|40.0|20.0|20.0|30.0|40.0|
|r3|select direct/reverse operation|1|0|2|0|||||
|r4|night-time set point delta<br>|-|-|-|-|5.0|5.0|2.0|4.0|
|c1|minimum time between consecutive compressor<br>starts<br>f|3|5|0|6|4|5|3|6|
|c2|minimum compressor offtime|2|4|0|4|2|3|0|5|
|d0|type of defrost|2|2|0|4|1|2|3|4|
|dl|interval between defrosts|6|10|6|12|5|7|10|12|
|dt|end defrost temperature set point/defrost temperature<br>threshold with temp. control|5.0|5.0|5.0|5.0|5.0|5.0|5.0|4.0|
|dP|maximum defrost duration|40|40|40|40|20|40|10|50|
|d6|freeze control temperature display during defrost|1|1|1|1|-|-|-|-|
|dC|time base<br>f|0|0|0|0|0|0|0|0|
|A0|alarm and fan temperature differential|2.0|2.0|2.0|2.0|2.0|2.0|2.0|2.0|
|AL|f<br>temperature alarm threshold/deviation|20.0|25.0|20.0|20.0|22.0|15.0|18.0|20.0|
|AH|high temperature alarm threshold/deviation|20.0|25.0|20.0|20.0|22.0|25.0|20.0|25.0|
|Ad|<br>temperature alarm delay<br>i|60|70|60|60|20|40|30|25|
|A4|3rd input configuration|-|-|-|-|0|4|1|0|
|A7|digital input alarm delay|-|-|-|-|0|20|30|20|
|Ac|set point dirty condenser alarm<br>f|55.0|50.0|70.0|55.0|55.0|55.0|55.0|55.0|
|AE|dirty condenser alarm differential temperature|10.0|8.0|10.0|10.0|10.0|10.0|10.0|10.0|
|Acd|f<br>dirty condenser alarm delay|60|40|200|60|60|60|60|60|
|F0|enable evaporator fan control|-|-|-|-|1|0|1|0|
|F1|<br>evaporator fan control set point|-|-|-|-|5.0|5.0|5.0|5.0|
|F2|stop evaporator fan if compressor of|-|-|-|-|1|1|1|1|
|F3|evaporator fan status during defrost|-|-|-|-|1|1|1|1|
|Fd|post-dripping time|-|-|-|-|3|4|5|6<br>**Table 5.f**|

|EZY=|normal temperature<br>|low temperature<br>|
|---|---|---|
|1|no defrost|defrost by hot gas|
|2|defrost by time|automatic night-time set point variation from digital input|
|3|heating output (reverse)|digital input alarm management|
|4|defrost with temp. control (d0=4)|defrost by temperature (d0=4)|

33

###### easy compact parameter sets (EY)

|Par.|Description|S|models (no|rmal tempe|rature)|
|---|---|---|---|---|---|
|||EY=1|EY=2|EY=3|EY=4|
|/4|select probe displayed|1|1|1|1|
|/5|select°C/°F<br>f|0|0|0|0|
|rd|control differential|3.0|3.0|5.0|2.0|
|r1|f<br>minimum set point value|-10.0|-15.0|-20.0|-30.0|
|r2|maximum set point value|15.0|20.0|20.0|40.0|
|r3|select direct/reverse operation|1|0|2|0|
|c1|minimum time between consecutive compressor starts<br>f|3|5|0|6|
|c2|minimum compressor offtime|2|4|0|4|
|d0|type of defrost|2|2|0|4|
|dI|<br>interval between defrosts|6|10|6|12|
|dt|end defrost temperature set point|5.0|5.0|5.0|5.0|
|dP|maximum defrost duration|40|40|40|40|
|d6|freeze control temperature display during defrost|1|1|1|1|
|dC|time base<br>f|0|0|0|0|
|A0|alarm and fan temperature differential|2.0|2.0|2.0|2.0|
|AL|f<br>absolute temperature or deviation for low temperature alarm|20.0|25.0|20.0|20.0|
|AH|<br>absolute temperature or deviation for high temperature alarm|20.0|25.0|20.0|20.0|
|Ad|temperature alarm delay|60|70|60|60|
||||||**Table 5.g**|

|Key:||
|---|---|
|EY=|normal temperature|
|1|no defrost|
|2|defrost by time|
|3|heating output (reverse)|
|4|defrost with temp. control (d0=4)|

###### easy split parameter sets (EZY)

|Par.|Description|mo|dels S-X (no|rmal tempe|rature)||models Y-C (|low temper|ature)|
|---|---|---|---|---|---|---|---|---|---|
|||EZY=1|EZY=2|EZY=3|EZY=4|EZY=1|EZY=2|EZY=3|EZY=4|
|/4<br>|select probe displayed<br>|1|1|1|1|-|-|-|-|
|/5|select°C/°F<br>f|0|0|0|0|-|-|-|-|
|rd|control differential|3.0|3.0|5.0|2.0|3.0|4.0|5.0|2.0|
|r1|minimum set point value|-10.0|-15.0|-20.0|-30.0|-30.0|-30.0|-30.0|-30.0|
|r2|maximum set point value|15.0|20.0|20.0|40.0|20.0|20.0|30.0|40.0|
|r3|select direct/reverse operation|1|0|2|0|||||
|r4|night-time set point delta|-|-|-|-|5.0|5.0|2.0|4.0|
|c1|minimum time between consecutive compressor<br>starts<br>f|3|5|0|6|4|5|3|6|
|c2|minimum compressor offtime|2|4|0|4|2|3|0|5|
|d0|type of defrost|2|2|0|4|1|2|3|4|
|dl|interval between defrosts<br>|6<br>|10|6|12|5|7|10|12|
|dt|end defrost temperature set point/defrost temperature<br>threshold with temp. control|<br>5.0|5.0|5.0|5.0|5.0|5.0|5.0|4.0|
|dP<br>|maximum defrost duration<br>|40|40|40|40|20|40|10|50|
|d6<br>|freeze control temperature display during defrost<br>|1|1|1|1|-|-|-|-|
|dC|time base<br> f|0|0|0|0|0|0|0|0|
|A0|alarm and fan temperature differential|2.0|2.0|2.0|2.0|2.0|2.0|2.0|2.0|
|AL|temperature alarm threshold/deviation|20.0|25.0|20.0|20.0|22.0|15.0|18.0|20.0|
|AH|high temperature alarm threshold/deviation|20.0|25.0|20.0|20.0|22.0|25.0|20.0|25.0|
|Ad|temperature alarm delay<br> i|60|70|60|60|20|40|30|25|
|A4|3rd input configuration|-|-|-|-|0|4|1|0|
|A7|digital input alarm delay<br>|-|-|-|-|0|20|30|20|
|Ac|set point dirty condenser alarm<br>f|55.0|50.0|70.0|55.0|55.0|55.0|55.0|55.0|
|AE|dirty condenser alarm differential temperature|10.0|8.0|10.0|10.0|10.0|10.0|10.0|10.0|
|Acd|dirty condenser alarm delay|60|40|200|60|60|60|60|60|
|F0|enable evaporator fan control|-|-|-|-|1|0|1|0|
|F1|evaporator fan control set point|-|-|-|-|5.0|5.0|5.0|5.0|
|F2|stop evaporator fan if compressor of|-|-|-|-|1|1|1|1|
|F3|evaporator fan status during defrost|-|-|-|-|1|1|1|1|
|Fd|post-dripping time|-|-|-|-|3|4|5|6|

**Table 5.h**

|EZY=|normal temperature<br>|low temperature<br>|
|---|---|---|
|1|no defrost|defrost by hot gas|
|2|defrost by time|automatic night-time set point variation from digital input|
|3|heating output (reverse)|digital input alarm management|
|4|defrost with temp. control (d0=4)|defrost by temperature (d0=4)|

34

###### **<u>5.10  Troubleshooting</u>**

The following table shows a number of anomalous situations that may

occur on the various models.

The most frequent causes and corresponding checks are described:

|problem|cause|checks|
|---|---|---|
|the compressor does not start (signalled by the<br>compressor LED flashing)|• compressor delay set<br>• defrostpost drippinginprogress|parameters c0, c1 and c2 and dd|
|the temperature is over the set limits but there is<br>no alarm message and the buzzer, if fitted, does not<br>sound|alarm delay set|parameters Ad, c6, d8|
|alarm IA is signalled (multifunction input) without<br>actuallybeingactive|the multifunction input generates an alarm when<br>the contact opens|connection of the input and whether this is closed in<br>normal operation|
|the alarm connected to the multifunction input is<br>not detected|alarm delay set or parameter programming error|1. if A4=1<br>2. the status of digital input A7|
|the defrost is not activated|• defrost duration too short (dP)<br>• interval between defrosts dI=0: in this case the<br>defrost is not activated|parameters dP and dI and H1 for S models|
||the end defrost temperature is too low or the<br>evaporator temperature is too high|parameters dt and d/ (defrost probe)|
|the manual defrost is not activated and the defrost<br>LED flashes|compressor protection times set|parameter d9 (select d9=1)|
|l<br>the high temperature alarm is shown after a defrost|the alarm delay after defrost is too short or the alarm<br>threshold is too low|parameters d8 and AH|
|the display remains frozen even after the defrost|the ambient temperature has not yet reached the<br>setpoint or alternativelythe time d8 has not elapsed|wait or reduce d8|
|after modifying a parameter the controller continues<br>working with the old values|the instrument has not updated the old value or<br>alternatively the parameter setting procedure has<br>not been ended correctly by pressing the SET button<br>for 3 s|turn the instrument off and on again or alternatively<br>reprogram the parameters correctly|
|for C models, the fan does not start|1. a compressor and fan start delay has been set<br>2. if F0=1 (fan managed by fan controller)<br>• the evaporator is “hot”: the evaporator<br>temperature can be read by selecting<br>parameter /d;<br>• dripping in progress;<br>• F1 (evaporator fan control set point) too low.<br>• post-dripping delay set<br>3. if F0=0<br>• F2=1 and the compressor is off<br>• dripping in progress<br>•post-drippinginprogress|1. parameter  c0<br>2. parameters F0, F1, Fd, dd and d/<br>3. parameters F0, F2, dd and Fd|

###### **Table 5.i**

35

###### **6.  TECHNICAL SPECIFICATIONS**

###### **<u>6.1  Easy technical specifications</u>**

|power supply<br>230 Vac +10 /-1|5% 50/60 Hz;|
|---|---|
|(*)<br>115 Vac +10 /-1<br>12 Vac 10/-15 %<br>|5% 50/60 Hz<br>, 50/60 Hz class 2<br>|
|12 Vdc (11…16|Vdc) class 2|
|<br>rated power<br>1.5 VA||
|inputs  (*)<br>NTC or PTC pro|bes, 1 or 3 inputs. Digital input as alternative|
|to third probe<br>relay outputs (*)||
|PJEZ|PQEZ|
|2 HP<br>UL: 12 A Res. 12 FLA 72 LRA - 240 Vac (|***),<br>UL60730: 12 A Res. 8 FLA 48 LRA - 240 Vac,|
|relay<br>UL: 12 A Res. 10 FLA 60 LRA - 240 Vac (<br>EN60730-1: 10(10) A 250 Vac (**)|****)<br>EN60730: 10(6) A 250 Vac|
|<br>16 A<br>UL: 12 A Res. 5 FLA 30 LRA - 240 Vac C3|00,<br>UL60730: 12 A Res. 5 FLA 30 LRA - 240 Vac C300,|
|relay<br>EN60730-1: 12(2) A NO/NC, 10(4) A u|p to 60 °C NO,<br>EN60730: 12(2) A NO 100k cycles, 12(2)A NC 30k|
|2(2) A CO-250 Vac|cycles, 2(2) A CO 30k cycles-250 Vac|
|8 A<br> <br>UL: 8 A Res. 2 FLA 12 LRA - 240 Vac C30<br>|<br>0,<br>  <br>UL60730: 8 A Res. 2 FLA 12 LRA - 240 Vac C300,<br>|
|relay<br>EN60730-1: 8(4) A NO, 6(4) A NC, 2(2)A|CO-250 Vac<br>EN60730: 8(3) A NO, 6(3) A NC, 2(2) A CO-250 Vac|
|30 A<br>relay<br>UL: 16 A Res. 16 FLA 96 LRA - 240 Vac (<br>EN60730-1: 20(10) A 250 Vac (**)<br>UL: 12 A Res. 12 FLA 72 LRA - 240 Vac<br>EN60730-1: 12(10) A 250 Vac|**)<br>UL60730: 12 A Res. 12 FLA 72 LRA - 240 Vac<br>EN60730: 12(10) A 250 Vac|
|5 A<br>UL: 5 A Res. 1 FLA 6 LRA - 240 Vac C300,|UL60730: 5 A Res. 1 FLA 6 LRA - 240 Vac C300,|
|relay<br>EN60730-1: 5(1) A-250 Vac|EN60730: 5(1) A-250 Vac|
|probe type (*)<br>Std CAREL NTC<br>Std CAREL PTC|10 KΩ at 25 °C<br>985 Ω at 25°C|
|connections<br>(*)<br>screw terminals<br>to 1.5 mm<sup>2</sup>. Plu<br>crimped conta<br>Maximum rate|for cables with cross-sect. from 0.5 mm<sup>2</sup><br>g-in terminals for screw blocks or with<br>cts (cable cross-sect. up to 2.5 mm<sup>2</sup>).<br>d current per terminal 12 A.|
|assembly (*)<br>terminal: using|screws from the front or with rear brackets|
|<br> <br>display<br>3 digit LED disp|<br>lay with sign, -199 to 999 and decimal|
|<br>point; six status|<br>LEDs|
|operating conditions|-10T50 °C - humidity <90% RH non-<br>condensing|
|storage conditions|-20T70 °C - humidity <90% RH non-<br>condensing|
|detection range|-50T90°C (-58T194°F)-resolution 0.1°C/°F|
|front panel index of protection|panel installation with IP65 gasket|
|case<br>i|plastic terminal, 81x36x65 mm|
|classification according to<br>|Class 2 when suitably integrated|
|protection against electric shock||
|<br>environmental pollution|normal|
|<br>PTI of the insulating materials|250 V|
|period of stress across the|long|
|insulating parts||
|<br>category of resistance to heat<br> i|category D (UL94 - V0)|
|and fire||
|i<br>immunity against voltage surges|category 1|
|<br>type of action and|<br>1 C relay contacts|
|disconnection||
|no. of relay automatic|EN60730:  100,000 operations|
|<br>operatingcycles(*)|<br>UL:  30,000 operations(250 Vac)|
|software class and structure|Class A|
|cleaning the instrument|only use neutral detergents and water|
|<br>max. cable length|<br>1 km serial;  30 m probes;  10 m relay|

###### **Table 6.a**

- (*) The features shown depend on the model.

- (**) Minimum T OFF between two starts must be greater than 1 min.

- (***) only for models PJEZ (M, S, X) *.

(****) only for models PJEZ (C, Y) *.

###### **<u>6.2  easy compact technical specifications</u>**

|power supply  (*)|230 Vac, -10+15 % 50/60 Hz;<br>115 Vac, -10+15 % 50/60 Hz;<br>12 Vdc ±10% or 12 Vac, ±10% 50/60 Hz (PJEZM*<br>only, without AUX relay);|
|---|---|
|rated power|0.5 VA|
|inputs  (*)<br>|NTC or PTC probes, 1 or 2 inputs<br>|
|relay output (*)|2HP relay:<br>UL: 12A 10 FLA 60 LRA 250 Vac 30000 cycles;<br>EN60730-1: 10(10)A 250Vac 100000 cycles (**);<br>16A relay<br>UL: 12A resistive 5FLA, 30LRA 250Vac 30000 cyc.<br>EN60730-1: 12(2)A or 10(4)A (N.O. only) 250VAC<br>100000 cycles;|
|Type of probe (*)|Std CAREL NTC 10 KΩ at 25 °C<br>Std CAREL PTC 985 Ω at 25°C|
|Power supply/relay<br>|screw terminals, 5 mm pitch for cables with cross-<br>|
|output connector (*)|sect. from 0.5 mm<sup>2</sup>to 1.5 mm<sup>2</sup>; 12A max;<br>plug-in terminals, 5.08 mm pitch for screw blocks<br>or with crimped contacts for cables with cross-<br>|
||sect. from 0.5 mm<sup>2</sup>up to 2.5 mm<sup>2</sup>; 12A max;|
|Probe connector (*)|screw terminals:<br>- 2 pin, 5 mm pitch for models with 1 probe<br>(cable cross-section from 0.5 mm<sup>2</sup>to 1.5 mm<sup>2</sup>);<br>12A max;<br>- 3 pin, 3.81 mm pitch for models with 2 probes<br>(cable cross-section from 0.08 mm<sup>2</sup>to 1.5 mm<sup>2</sup>);<br>6A max;<br>|
||plug-in terminals for screw blocks or with<br>crimped contact:-<br>2 pin, 5.08 mm pitch for models with 1 probe<br>(cable cross-section from 0.5 mm<sup>2</sup>to 1.5 mm<sup>2</sup>);<br>12A max;<br>- 3 pin, 3.81 mm pitch for models with 2 probes<br>(cable cross-section from 0.08 mm<sup>2</sup>to 1.5 mm<sup>2</sup>);<br>8 A max;|
|Serial connector|1 connector for the network of supervisor<br>connection or for the parameter programming<br>key (only on the models where featured);|
|Assembly<br>|using screws from the front or with rear brackets<br>|
|Display|LED display, 2 digits plus sign, decimal point and<br>compressor icon|
|Keypad|3 membrane buttons|

**Table 6.b**

- (*) The features shown depend on the model.

- (**) Minimum T OFF between two starts must be greater than 1 min.

*[Figurtekst: 74 · 81 31 10 · 38,29 3 · 71x29 · 33 36 28.5]*

**Fig. 6.b**

Warning: do not run the power cable less than 3 cm from the bottom of the device or the probes; for the connections, only use copper wires.

*[Figurtekst: 74 · 81 58 10 · 65,29 3 · 71x29 · 33 36 28.5]*

**Fig. 6.a**

36

###### **<u>6.3 easy split technical specifications</u>**

|power supply (*)|230 Vac +10/-15%, 50/60 Hz;<br>|
|---|---|
||115 Vac +10/-15%, 50/60 Hz|
|power input (controller only)|<br>7 VA: 30 mA~ at 230 Vac;<br>7 VA: 60 mA~at 115Vac<br>|
|inputs<br>|2 probe inputs, NTC (-50T90°C) or HT NTC(-40T150°C);<br>1 digital input as alternative to third probe<br>|
|relay outputs (***)|RL1:<br>EN60730-1: 12(10)A 250Vac 100000 cycles,<br>|
||UL: 16A Res. 16FLA 96LRA 250Vac (**) 30000 cycles<br><br>|
||RL4:<br>EN60730-1: 12(10)A 250Vac 100000 cycles,|
||UL: 12A Res. 12FLA 72LRA 250Vac (**) 30000 cycles|
||RL3, RL2:<br>EN60730-1: 12(2)A 250Vac 100000 cycles (N.O. contact only),|
||UL: 12A Res. 2FLA 12LRA 250Vac (**) 30000 cycles<br>|
|type of probe|Std CAREL NTC 10kΩ ±1% at 25°C|
||Std CAREL NTC-HT 50kΩ ±1% at 25°C|
|connections|- input/output signals: screw terminals with cables from 0.5 to 1.5 mm<sup>2</sup>;|
||- faston terminals: recommended cable cross-section 2.5 mm2 for current ratings up to 16 A;<br>- use:<br>- cables with max. operating temperature at least 90 °C;<br>|
||- fully insulated faston terminals with max. operating temperature at least 100 °C;<br>- power supply: cable cross-section 2.5 mm<sup>2</sup>for current ratings up to 16 A and 4 mm<sup>2</sup>for current ratings up<br>to 24 A;<br>-earth connections: see the instructions about power supply connections.<br>|
||PJEZ*8**4*(without plastic case): maximum supply current 24 A|
||<br>PJEZ*8**5*(with plastic case): maximum supply current 16 A<br>|
|assembly|- terminal: using screws from front panel or with rear brackets|
||-power board: on models PJEZ*8**5*supplied with plastic case<br>|
|display<br>|3 digit LED display with sign-199 to 199 and decimal point, 6 status LEDs<br> <br>|
|operating conditions|PJEZ*8**4* (without plastic case):-<br>PJEZ*8**5* (with plastic case):|
||- 10T60°C for power board;<br>- 10T50°C for power board;|
||- 10T60°C for display; humidity <90% RH non-<br>- 10T60°C for display; humidity <90% RH non-|
||condensing.<br>condensing.<br>°|
|storage conditions|-20T70C, humidity <90% RH non-condensing|
|range of measurement|- NTC probe: -50T90°C(-58T194°F), resolution 0.1 °C/°F<br>-NTC-HT probe:-40T150°C(-40T302°F), resolution 0.1°C/°F|
|index of protection|- display (front): IP65|
||-box-mounted power board: IP00|
|dimensions|plastic terminal: 81x36x38.29 mm<br>|
|i|power board: plastic box 190x140x70 mm<br>i<br>|
|classification according to protection against electri|i     c<br>class 1|
|shock||
|environmental pollution|grade 3|
|PTI of insulating materials|250 V|
|period of stress across the insulating parts<br>i|long|
|category of resistance to heat and fire<br>|category D (UL94–V0)<br>|
|immunity against voltage surges|category 3|
|<br>type of action and disconnection|<br>1C relay contacts|
|construction of the control device|integrated electronic control device|
|no. of relay automatic operating cycles|EN60730-1: 100000 operations;UL873: 30000 operations.|
|software class and structure|class A|
|cleaning|only use neutral detergents and water|
|max cable length|serial: 1 km; probes/digital inputs: 10 m; relay: 10 m|
|conformity|EN60730-1, EN61000-6-1, EN61000-6-2, EN61000-6-3, EN61000-6-4, EN61000-4-2, EN61000-4-3,|
||EN61000-4-4, EN61000-4-5, EN61000-4-6, EN61000-4-11|

*) The features shown depend on the model.

(**) Minimum T OFF between two starts must be greater than 1 min.

(***) Conformity to UL873 only corresponds to models without plastic case.

*[Figurtekst: 74 · 81 31 · 38,29 5 · 71x29 · Fig. 6.c · 33 36]*

*[Figurtekst: 117 · 36 8.5 · 103.5 5 · Ø 4 · L · RL1 RL4 RL3 RL2 · L · N · N · 7 · 5 · 98 88 · 5]*

**Fig. 6.d**

37

###### **<u>6.4  Electromagnetic compatibility</u>**

The easy and easy compact series is compliant with the EU standards on electromagnetic compatibility:

- for household appliances EN 55014-2 and EN 55014-1;

- for residential, commercial and light industrial environments EN 500821 and EN 50081-1;

- for industrial environments EN 50082-2 and EN 50082-1;

- as regards safety, the devices are compliant with standards EN60730-1 and EN60730-2-9.

###### **<u>6.5  Flammable refrigerant gases</u>**

The PJEZ models of easy series use components and, more specifically, electromechanical relays tested in accordance to UL 60079-15 ed. 4 / ISA 12.12.01:2013 (Sealed or Enclosed Break Device). Acceptability of these relays in end use application where flammable refrigerants are employed shall be reviewed and judged in the end use application.

For use of PQEZ models of easy series with flammable refrigerant gases, the controllers have been evaluated and judged compliant with the following requirements of IEC 60335 series standards:

- Annex CC of IEC 60335-2-24:2010 referenced by clause 22.109 and Annex BB of IEC 60335-2-89:2010 referenced by clause 22.108; components that produce arcs or sparks during normal operation have been tested and found to comply with the requirements in UL/ IEC 60079-15;

- IEC/EN/UL 60335-2-24 (clauses 22.109, 22.110) for household refrigerators and freezers

- IEC/EN/UL 60335-2-40 (clauses 22.116, 22.117) for electrical heat pumps, air-conditioners and dehumidifiers

- IEC/EN/UL 60335-2-89 (clauses 22.108, 22.109) for commercial refrigerated appliances

The controllers have been verified for the maximum temperatures of all components, which during the tests required by IEC 60335 cl. 11 and 19 do not exceed 272 ° C.

Acceptability of these controllers in end use application where flammable refrigerant gases are used shall be reviewed and judged in the end use application.

38

Agenzia / _Agency_ :

**CAREL INDUSTRIES - HQs** Via dell’Industria, 11 - 35020 Brugine - Padova (Italy) Tel. (+39) 049.9716611 -  Fax (+39) 049.9716600 e-mail: carel@carel.com - www.carel.com
