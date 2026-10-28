# Danfoss SM-800A – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.

## Indhold

1. AK-SM 800A series – User Guide (SW 5.1.x, engelsk) – Ny System Manager (AK-SM 820A/850A/880A). Komplet brugervejledning: opsætning, netværk, alarmer, avancerede funktioner.
2. AK-SM 820A / 850A / 880A – Data sheet (SW 5.0x, engelsk) – Tekniske data, varianter og bestillingsnumre for AK-SM 800A.
3. AK-SM 800A series – Installation Guide (engelsk) – Montage, forsyning og tilslutninger (relæer, MODBUS, LON/TP78, Ethernet).

*Udeladt for at spare plads: Security Guidance, konverteringsguide fra AK-SC 255/SM 800 og Offline utility tool. Se de originale Danfoss-PDF'er ved behov (AB485035014642, AB389443841539, AQ533024941003).*

---

## 1. AK-SM 800A series – User Guide (SW 5.1.x, engelsk)

*Kilde: Danfoss-dokument BC337629891709en-001101. Ny System Manager (AK-SM 820A/850A/880A). Komplet brugervejledning: opsætning, netværk, alarmer, avancerede funktioner.*

User Guide

### System Manager AK-SM 800A series

ADAP-KOOL® Refrigeration Control System **SW Ver. 5.1.x**

##### **Contents**

|---|
|5.14 Device Management<br>i|

|---|

##### **1. Product Introduction**

##### **1.1 Product Introduction**

Introducing the Danfoss System Manager 800A series. The System Manager AK-SM 800A series is an evolution of the global System Manager 800 and represents a significant investment by Danfoss in the Food Retail market. The AK-SM 800A maintains familiarity and a deep application feature set but is enhanced via several significant updates.

###### **Product headline features**

- All new Electronics platform supporting new Operating System (based on Linux)

- Implementation of IT industry standard security protocols (HTTPS, SSL/TSL 1.2, WPA2 encryption)

- Enhanced UI/UX - new yet familiar touch screen

- Full web browser, known as StoreView Web (SvW)

- Support of mobile devices

- Retro-fit ready – includes EoL and legacy control functions supporting smooth upgrade path

- Improved history collection and saving

- Secure Wi-Fi Access point – for site connection without disrupting WAN network

|**Series Features**(Model dependent)|**Benefits**|
|---|---|
|Built in standard IT security best practice and protocols|Secure web connection (HTTPS), Secure e-mail, Encrypted data and secure software<br>update packages. Software Package 4.0 and above now includes new Security menu<br>where session control attributes can be configured.|
|Full Web browser interface|Reduce tool complexity, utilization of modern web technology, full system view via built<br>in StoreView Web (SvW)|
|Mobile ready utilities|Connect via unit Wi-Fi access point and use Laptop / Mobile devices for SvW view|
|Refrigeration Control (centralized and de-centralized)|Control your refrigeration application via built in Rack control or via de-centralized<br>distributed network controls|
|Lighting Control (centralized and de-centralized)|Control your lighting application via built in control or via de-centralized distributed<br>network controls|
|HVAC Control (centralized and de-centralized)|Control your HVAC application via built in control or via de-centralized distributed<br>network controls|
|Energy saving technology (built in)|Energy saving functions built in - no additional licenses to enable savings|
|Master Schedules|Schedules Groups Central Defrost, Case lighting, Store / Outside Lighting, Night setback,<br>Shutdown|
|Flexible Alarm Routing / output|Flexible Alarm Routing / Output e-mail, IP address, relay|
|Built in field bus options|Serial Modbus, TCP Modbus, LonWorks®, SNMP IP, AK IP|
|Full color VGA Local touch screen|Password protected, controlled access to system|
|Built in Buzzer & 2-tone LED|Easy local level alarm notification|
|Custom graphics|Local screen custom graphics: Create simple & clear graphic screen with only ‘key<br>parameters’ shown|
|Extended History logging|Updated History function with 5.x and above firmware. Dedicated Active and Archive<br>directories for improved storage and visibility|
|Alsense™ ready|Supported by Alsense™, offering multiple digital services and reporting|

##### **1.2 Specif i** **cations**

The mounting location should be flat, dry and free of major vibrations. The AK-SM 800A should be mounted at eye level.

###### **Environmental Range**

Operating temperature:

-10 – 50 ˚C (14 – 122 ˚F) @ 95% RH (non condensing) IP20

###### Electrical range:

For supply connections, use 16 AWG or larger wires rated for at least 75 °C (167 °F). Use copper conductors only. ~ 100 – 240 V AC 50/60 Hz 12 W Built-in alarm relay

Contact voltage: Up to 240 V, Load: AC-1 (Ohmic) Current rating. 5 Amp AC-15 (inductive) Current rating. 3 Amp

###### **LCD Touch Screen**

Active TFT touch (thin-film transistor), SVGA 800 x 600

###### **Approvals**

UL file: E31024 61B5 Class 2 or LPS in accordance with NEC. Enclosure rating type 1 FCC ID: X02SPB209A IC ID: 8713A-SPB209A

###### **Size**

Unit Width 295 mm (11.6”), Unit Height 235 mm (9.3”), Unit Depth 65 mm (2.5”) Mounting holes 246 mm (9.7”) Width Mounting holes 175 mm (6.9”) Height

###### **Approvals:**

###### **Declaration of conformity info**

- Regulation 2005/37/EC

- EN 12830, 07-1999

###### **LCD Touch Screen – cleaning**

- Use a soft lint-free cloth.

- The cloth may be used dry, or lightly dampened with a mild soap cleaner or Ethanol.

- Cleaner with Ammonia can be used, but with percentage max of 4%.

- Be sure the cloth is only lightly dampened, not wet. Never apply cleaner directly to touch panel surface.

- Never use acidic or alkaline cleaners, or organic chemicals such as: paint thinner, acetone, tolulene, xylene, propyl or isopropyl alcohol, or kerosene.

- EN 13485, 11-2001

- HACCP 080R1215 - CE 080R1213 - C-Tick 080R1214 - UL E31024

**WARNING:** To avoid risk of injury from electric shock, ensure correct electrical isolation is made before working within the enclosure.

###### **International Certifications**

Este equipamento não tem direito à proteção contra interferência prejudicial e não pode causar interferência em sistemas devidamente autorizados. Para maiores informações, consulte o site da ANATEL - www.anatel.gov.br

###### **Statements for the AK-SM 800A**

###### **FCC COMPLIANCE STATEMENT**

CAUTION: Changes or modifications not expressly approved could void your authority to use this equipment This device complies with Part 15 of the FCC Rules. Operation to the following two conditions: (1) This device may not cause harmful interference, and (2) this device must accept any interference received, including interference that may cause undesired operation

###### **INDUSTRY CANADA STATEMENT**

This device complies with Industry Canada license-exempt RSS standard(s). Operation is subject to the following two conditions: (1) this device may not cause interference, and (2) this device must accept any interference, including interference that may cause undesired operation of the device.

Le présent appareil est conforme aux CNR d'Industrie Canada applicables aux appareils radio exempts de licence. L'exploitation est autorisée aux deux conditions suivantes : (1) l'appareil ne doit pas produire de brouillage, et (2) l'utilisateur de l'appareil doit accepter tout brouillage radioélectrique subi, même si le brouillage est susceptible d'en compromettre le fonctionnement.

###### **NOTICE**

###### **FCC COMPLIANT NOTICE**

This equipment has been tested and found to comply with the limits for a Class B digital device, pursuant to part 15 of the FCC Rules. These limits are designed to provide reasonable protection against harmful interference in a residential installation. This equipment generates, uses and can radiate radio frequency energy and, if not installed and used in accordance with the instructions, may cause harmful interference to radio communications. However, there is no guarantee that interference will not occur in a particular installation. If this equipment does cause harmful interference to radio or television reception, which can be determined by turning the equipment off and on, the user is encouraged to try to correct the interference by one or more of the following measures:

- Reorient or relocate the receiving antenna.

- Increase the separation between the equipment and receiver.

- Connect the equipment into an outlet on a circuit different from that to which the receiver is connected.

- Consult the dealer or an experienced radio/TV technician for help.

Modifications: Any modifications made to this device that are not approved by Danfoss may void the authority granted to the user by the FCC to operate this equipment.

Any regulatory related concerns contact: global_approvals@danfoss.com

Danfoss Cooling 11655 Crossroads Circle Baltimore, Maryland 21220 United States of America global_approvals@danfoss.com www.danfoss.com

###### **EU CONFORMITY NOTICE**

Hereby, Danfoss A/S declares that the radio equipment type AK-SM 800A is in compliance with Directive 2014/53/EU. The full text of the EU declaration of conformity is available at the following internet address: www.danfoss.com

Danfoss A/S Nordborgvej 81 6430 Nordborg Denmark global_approvals@danfoss.com www.danfoss.com

##### **2. Installation and start-up configuration**

##### **2.1 Installation**

###### **Tools needed**

1. Bubble level

2. Small slotted screwdriver for connector screws

3. Torx 8 screwdriver for releasing the electronic unit and for fastening the unit when recessed mounted

4. Screwdriver for fixing the AK-SM 800A

5. Pen for marking the 2 lower fixing holes

6. Larger slotted screwdriver for releasing the Technician lid

###### **Wall Mounting- box**<sup>1</sup> )

1. Attach screw to the wall

2. Mount AK-SM 800A to the screw

3. Loosen Technician lid (three sides)

4. Remove Technician lid

5. Level the AK-SM 800A

6. If drilling is necessary, mark up 2 screws in Connector part.

7. Attach the Connector part to the wall using another 2 screws

###### **Wall Mounting- wiring**

Insert cables through the rubber grommets

*[Figurtekst: T10 · Strip the cables Strip the wires]*

*[Figurtekst: 100 - 240 V AC · Relay 1/2 · Canbus · Ethernet 0 · MODBUS 1/2 · LON / TP78 · CANbus is not currently activated. · Secure wires in  Strain relief the cables · connectors by screwdriver]*

1) For installation in countries where UL Listing is required, please refer to the installation instruction provided with the product.

Carefully replace the cover, ensure that it securely snaps into place

###### **Wall Mounting- Panel recessed**

From the front:

A hole of the size 280 x 220mm is machined. The AK-SM 800A is inserted in the hole.

*[Figurtekst: a · b · Danfoss · 80G8145]*

From the backside:

Slide the 3 fastener into the housing part. The screws are inserted into the fasteners. Secure the unit by tightening the screws

Remove Technician lid

From the back, push cables inside the housing

##### **2.2 Connections**

The following chapter describes the available connections on your AK-SM 800A.

Please note that not all connection points are currently active, refer to the drawing below for more details

##### **2.3 Southbound Network topology**

Your AK-SM supports multiple southbound device topology formats. The term ‘southbound’ refers to controllers that reside on network(s) downstream of the System Manager. The System manager supports serial and digital formats (Modbus, Lon, Modbus/IP, AK-IP).

*[Figurtekst: USB 2.0 (x2) · CANbus Modbus 1 · Power Alarm Relay 2 Modbus 2 · Alarm Relay 1 LON (RS 485) or · Eth0 (WAN) Eth1 (Field) LON (TP78) · USB 2.0 Host (800 mA) · Future use]*

- When using the Lon RS485 network, ensure the Term. Switch on the AK-SM is in the ‘ON’ position (enable internal resistor). Any repeaters must also have 120 Ohm resistor in place. Additionally, ensure that the last controller on the network run also has its end of line resistor enabled.

For further detailed description of network connections please refer to document ‘Data Communication between ADAP-KOOL® Refrigeration controllers_RC8AC802’.

Follow the standard topology guidelines for Lon RS485, particularly with respect to:

- Maximum cable length

- When to use a repeater

- Suitable resistors

###### **Cable type**

Twisted pair cables must be used (with or without screen). Some types of communication require a cable with a screen to be used.

###### Examples:

For Lon RS485, MODBUS, RS485 Third party - General ‘EIA 485’ recommendation:

- Belden 9841, 24 AWG, 1 pair with screen

- Belden 3107A, 22 AWG, 2 pairs with screen

- Smartwire 043006AL, 22 AWG, 1 pair with screen

- Alpha wire 6453, 22 AWG, 1 pair with screen

- Carol C4841A, 24 AWG, 1 pair with screen

- Dätwyler Uninet 3002 4P 4 pairs with screen (CAT5 cable)

For Lon TP78 communication - Level 4 cable general recommendation:

- Belden 7703NH, 22 AWG, 1 pair with screen

- Belden 7704NH, 22 AWG, 2 pair with screen

- Smartwire 106500, 22 AWG, 1 pair with screen

Wires with larger cross-section than AWG 22 is not recommended

###### Cable length

A cable length must not exceed 1200 m (4000 foot). A repeater (Part # 084B2241 ) must be used for longer lengths.

###### **2.3.1 Lon RS485 topology**

The cable connection must be wired from controller to controller, and no branches are allowed on the cable. If the cable length exceeds 1200 m a repeater must be inserted. If the data communication cable runs through an electrically noisy environment which impairs the data signal, one or more repeaters must be added to stabilise the signal.

When configuring Lon devices on the field bus, the highest device address that can be can be used is 127.

Remember to use 120 Ohm terminators on the last field bus controller device. Note also to enable (ON) the Termination Switch, located above each network connection point on the AK-SM 800A, this will enable the built in terminator(s) for each network point on the AK-SM 800A.

###### **Conductors**

The wire pairs are looped from device to device. There are no polarisation requirements. (On some controllers, the clamps are designated A and B, while on others there is no designation. The connectors are otherwise identical. If a screen wire is used, it must be connected to the system device and any repeaters. A screen must always be looped from device to device.

The screen must not be connected to anything else. (The screen is earthed inside the screen and must not be earthed in any other way.)

###### **Mid network connection**

This example shows the AK-SM 800A series RS485 version used in the middle of a network run. In this example ensure that both ends of the controller run are fitted with 120 Ohm terminators. Over the past several years Danfoss has offered versions of the AK-SC 255 and AK-SC 355 which has a LonWorks® option of TP78. As a physical layer of the LonWorks® protocol these older systems offered x5 network connection points. Due to the global phase out of the TP78 option by the OEM, Danfoss has made available a special order version of the AK-SM 880A (080Z4029), which comes pre-installed with a LonWorks® TP78 options card. This ‘special’ version of the AK-SM 880A is designed to support customers who wish to migrate from existing AK-SC 255 and AK-SC 355 and AK-SM 800 TP78 systems.

**Note:** this version of the AK-SM 880A is not intended or available in Europe and offers x4 TP 78 connection points.

*[Figurtekst: R=120 ohm · AK-SM · max. 1200 m · RS 485 · R=120 ohm · AK-SM]*

*[Figurtekst: RS 485 RS 485 · R=120 ohm R=120 ohm · AK-SM]*

*[Figurtekst: TP 78-Version · MODBUS 1 MODBUS 2 TP 78 TP 78 TP 78 TP 78 · (Danfoss) (RS485) LON 1 LON 2 LON 3 LON 4]*

###### **2.3.2 MODBUS topology**

When running software package version V3.2.x and above, the AKSM 800A offers two Modbus channels, including 3<sup>rd</sup> party support for (Modbus) Refrigeration and utility meter device. Both channels can be enabled at the same time but must have unique node addressing for every node regardless of the channel/s in use.

**Note:** See system capacity tables at end of this document for details on node capacity etc.

MOD#1 supports Danfoss and pre-coded devices, as such this channel does not require any custom configuration.

MOD#2 supports Danfoss and 3<sup>rd</sup> party devices and offers a degree of configuration to accommodate non Danfoss controls.

MOD1&2 offers the ability to configure scan address range, thus making scanning more efficient (only scan for known address rages).

For additional details on Modbus configuration see section ‘5.9 Configuration → Network Nodes’.

Master control (Po Optimization) is supported in distributed use case where Pack is on Lon and associated cases are on MOD#1 and MOD#2.

The cable must be with screen. The cable is connected from controller to controller, and no branches are allowed on the cable. If the cable length exceeds 1200 m a repeater must be inserted. If the data communication cable runs through an electrically noisy environment which impairs the data signal, one or more repeaters must be added to stabilise the signal.

*[Figurtekst: AK-SM · max. 1200 m · MODBUS MODBUS · R=120 ohm R=120 ohm · AK-SM · MODBUS#1 · R=120 ohm · MODBUS#2 · AK-SM · R=120 ohm]*

When configuring MODBUS devices on the field bus, the highest device address that can be used is 199.

‘The System Manager can be inserted in middle of network, ensure System Manager termination is OFF. Refer to Danfoss document ‘RC8AC802 Data Communication’.

*[Figurtekst: The wires are looped from device to device. · A is connected to A. · B is connected to B. · The screen must be connected to the system device, all controller · and any repeaters. · A screen must always be looped from device to device. · The screen must not be connected to anything else. · Be sure to configure the MODBUS repeater AKA 222 · Repeater · (code#084B2240) to the correct baud rate. · See notes section at the back of this guide for MODBUS device · baud rate properties. · Refer to Danfoss Instructions RI8KN402 for further details on the · AKA 222 repeater’. ON · Termination · ON · Baudrate: · DANBUSS: · MODBUS: 19.2 · MODBUS: 38.4 · OFF · ONON · OFF OFF · ON ON · OFFOFF · ON ON]*

###### **2.3.3 MODBUS / IP**

Your AK-SM 800A supports Modbus/IP southbound communications. In particular Danfoss AK-CC case controllers and the new X-Gate.

*[Figurtekst: System Manager · (AK-SM 800A) · Case controller · Modbus 2 Case controller · Modbus 1 · Ethernet 0 Ethernet 1 · UDP/IP Modbus / IP · (AK-CC55) · DHCP router · Customer LAN LAN · network LAN · Protocol interface · (AK-PI 200) · USB · AK-ST 500 · AK-XM · Pack controller · (AK-PC 782B) · System Manager · (AK-SM 800A) · Ethernet 0 Ethernet 1 · UDP/IP · Note:  Current behavior and workflow for adding X-Gate via · Modbus/TCP with Modbus#2 (Serial) · X-Gate · New configurations:  Enable the Modbus#2 serial channel · Customer first, then enable X-Gate via Modbus/TCP. · network · Existing configurations:  If X-Gate via Modbus/TCP is · already enabled before Modbus#2, you must: · • Disable the Modbus/TCP channel · • Enable the Modbus#2 Serial channel · CANbus · Modbus RTU • Re-enable the Modbus/TCP channel · BACNet SM/TP · Device Device · Device]*

##### **2.4 First time startup**

To establish basic settings, an initial wizard is presented upon first powering up your AK-SM 800A. This wizard appears only once upon first time power up from new (out of the box) or if the system database has been cleared (an option in the system configuration). The following screens are presented;

1/8 Language (set required primary unit language)

2/8 Setup Administrator (create highest level user who later can then create additional users.

- **Caution:** Remember user/password as Danfoss does not have access to user profiles or passwords. Danfoss is not responsible for the management of user passwords. If the user/password is forgotten the ‘forgot password’ workflow will need to be applied).

The following characters are not accepted for the passwords:

“&’()+,-./:;<=>?[]\^_`{}|~ and spaces

3/8 Setup Date/Time/Format

4/8 Setup system units

5/8 Notification of connectors (take note of connector locations and what connectors are available)

6/8 Setup Network

7/8 Security (session control)

8/8 Important software update notification (To ensure optimum operation, security and the latest features ensure your AK-SM 800A is updated with the latest software. Follow on screen prompts or visi t ak - sm800a.danfoss.com f or the latest software packages. Also refer to chapter 4.3 for more information on how to update your AK-SM 800A.) After completion of the settings wizard the AK-SM 800A Series will request a reset, where settings will saved. Commissioning activities can now continue using Web wizards and control screens.

###### **Local screen login**

For security purposes, no system information or status is available on the AK-SM 800A until a valid username and password has been entered. To assist in the confirmation of inputting of credentials, use the ‘show’ check box – this will show each character as you input.

###### **Forgot Credentials**

This button can be used if you have forgotten your user name or password. Danfoss cannot access or recover any user name or password in the system, as these are stored in an encrypted format. If your log in credentials are forgotten you will need to enter new credentials, previous user credentials are not recoverable. Please note that it is expected that one administrator can always gain access to the system and thereby delete the original user profile of the user who has forgotten their credentials and create a new one, where the user would input a new password.

If the administrator is not available or cannot perform this action, the reset password workflow will need to be initiated. Follow the on-screen prompts and press the ‘Reset password’ button, see section 3.1 for more details.

**Note:** For security purposes, resetting of the password requires specific unit information that is ONLY possible when in front of the local AK-SM 800A screen.

##### **2.5  IP Conf i** **guration and suggested security settings**

Danfoss takes security and the integrity of its applications seriously and is continuously investing in bringing to market products and services that have best-in-class security features and technologies. Danfoss products are Engineered to last many years and, as technologies and security risks evolve, it is important to ensure basic best practices are in place so that no matter how old your product is, you can have a level of core security that will continue to support your business needs.

###### **Important:**

The current generation of Danfoss refrigeration controller frontends are embedded devices designed to be installed behind secure networks and firewalls. Due to the longevity of several Danfoss products installed in the field it is important that key security steps are taken to ensure protected operations. Please consider the important recommendations below to ensure your application has a suitable level of network security and integrity.

- Ensure your AK-SM 800A system(s) are NOT connected to an open or public network

- Use ‘strong password’ for user accounts

- Configure Session Control to ‘Strict’ (see section 5.x)

- Enable HTTPS for remote communications

- Do not share or publish any username and passwords

- Keep your System Managers updated with the latest software packages from Danfoss (ADAP-KOOL™ Downloads)

Consult available industry standards (i.e. ISO/IEC 27002:2013) for further reference and guidance on organizational information security standards and information security management practices.

Communication and Security settings on your AK-SM 800A can be found in section 5.x

###### **General IT security / Recommendations**

The AK-SM 800A series device is an embedded controller designed to be installed behind an appropriate router and firewall. Whilst the AK-SM 800A offers many IT industry security technologies (HTTPS, encrypted Wi-Fi, encrypted passwords...). Danfoss strongly recommends the deployment using IT security best practices and protocols.

The AK-SM 800A controller supports auto negotiated 10/100 Ethernet speeds. The AK-SM 800A controller supports auto negotiated full / half duplex Ethernet communications.

###### **AK-SM 800A port table**

|**Port**|**Description**|**Use**|**User Configurable**|
|---|---|---|---|
|5136|UDP|SNMP|No|
|1041|UDP|PI-200|No|
|443|TCP|HTTPS Secure Web browser communications|Yes|
|80|TCP|HTTP Web browser communications|Yes|
|5003, 5005|UDP|Host network communication UDPports|No|

###### **Security session control**

System software includes additional Northbound (remote UI and XML) security functionality to further harden against malicious attacks and network vulnerabilities. Danfoss recommends enabling strict security settings in the System Manager, with coordination and alignment within applicable IT security departments.

Refer to the section 5.x Configuration → Security - Session Control for more details.

##### **3. Navigation and use (Local screen)**

##### **3.1 Log in screen**

For security purposes, no system information or status is available on the AK-SM 800A until a valid username and password has been entered. To assist in the confirmation of inputting of credentials, use the ‘show’ check box – this will show each character as you input.

###### **Forgot Credentials**

This button can be used if you have forgotten your user name or password. **Danfoss cannot access or recover any user name or password in the system, as these are stored in an encrypted format. If your log in credentials are forgotten you will need to enter new credentials, previous user credentials are not recoverable.**

Please note that it is expected that one administrator can always gain access to the system and thereby delete the original user profile of the user who has forgotten their credentials and create a new one, where the user would input a new password. If the administrator is not available or cannot perform this action, the reset password workflow will need to be initiated. Follow the onscreen prompts following ‘Reset password’ button.

Note: For security purposes, resetting of the password requires specific unit information that is ONLY possible when in front of the local AK-SM 800A screen.

**Note:** For the North American region, Alsense™ can be called to initiate a password reset. The phone number will be shown in the reset popup window, as shown below.

Depending on the AK-SM 800A region (country) configuration, the initial contact point may differ. In essence, your first action is to contact Danfoss Technical support for your region. Upon receipt of your request to reset a password, Danfoss Technical support will raise a support ticket capturing relevant details and ultimately will provide a one off, time restricted (16 hours) user/password so entry can be established. Upon using this code to gain access to the AK-SM 800A you must update your user credentials with a new password.

##### **3.2 Home screen / Dashboard**

After logging in, by default the dashboard screen will be presented. Note that a system preference is available under the Configuration  System  screen where the option to define either Dashboard, Equipment or Graphics as home screen is available.

The home screen (indicated by the home icon) offers access to different functions, described below;

###### **USB Flash Drive**

Access to the USB Flash drive (when inserted) is via the USB flash drive icon. The 800A supports FAT32 formatted USB flash drives with a usable file size of 4 GB. When a compatible USB flash drive is inserted into any one of the three USB ports, the USB icon changes to solid, indicating successful detection. Pressing this icon will bring up the USB menu options.

**Note:** Be sure to correctly eject the USB drive, via the top menu selection, corruption to the USB may occur if this is not done.

###### **USB Flash Drive menu options**

- Eject USB Drive: use this to correctly eject flash drive

- Update Software: Use this option to update the AK-SM 800A via compatible software package (obtained via Danfoss ADAPKOOL support site)

- Export:

- Database

- HACCP Data

- Refrigeration Report

- System Report

- Cleared Alarms

- Audit Trail

- Advanced Diagnostics

- Import:

- Database

- Device File pkg (.epk)

###### **AK-SM 800A Wi-Fi Access Point**

Your AK-SM 800A may offer Wi-Fi access point functionality, depending on model. If your unit has Wi-Fi Access point enabled, the Wi-Fi icon can be seen on the local screen, if this icon is not shown, your model does not have Wi-Fi available - use Ethernet for web connectivity.

The AK-SM 800A is equipped with built in Wi-Fi access, designed to support direct unit/user access. By default, Wi-Fi is disabled, only authorized users can enable this feature. The AK-SM 800A Wi-Fi access point can be used to connect a mobile device (smart phone, tablet) or laptop/PC and when enabled will remain active for 8 hours.

When connecting to the AK-SM 800A Wi-Fi, look for the wireless network SSD name and select. The SSD name will reflect the host address (rotary switch), since this is a point to point connection only (host network view not supported).

Once connection to the AK-SM 800A network has been established, open a compatible web browser (Google Chrome™ / Apple Safari™, Chromium based Microsoft Edge™) and enter the IP address shown on the Wi-Fi screen, the AK-SM 800A.

Web log on screen will be shown. Enter the AK-SM 800A user name and password.

Note: If the Wi-Fi is enabled and the AK-SM 800A resets, for security purposes, Wi-Fi will revert to disabled.

###### **Info button**

The info button hosts a drop down menu selection, where the following is available;

About:

Shows unit information, software version, MAC and IP address

Licensing:

This screen will show any applied licenses

Terms:

End user terms and disclosure

Connections:

A technical view of active connections available on the AK-SM 800A.

###### **Log out**

Press the log out icon to exit and log out of the AK-SM 800A.

**Note:** The AK-SM 800A will detect inactivity and will auto log off after a period of 20 minutes. This can be changed via the Configuration->System screen (Idle timeout).

##### **3.3 Home Screen –** **Menu Bar**

The second level of meu bar on the home screen offers the following;

###### **Fly-in Menu**

Pressing the ‘grid button’ will trigger the fly-in menu. The purpose of this menu is to provide quick links / utilities to important areas of the AK-SM 800A.

###### **Dashboard**

With the Dashboard in focus (note grey focus line under Dashboard), the left hand section of the screen will display active alarms. The active alarm count will be shown as a red digit, followed by the active alarm list. Press the ‘Open Alarm list’ button to open a dedicated alarm screen.

The active alarm screen will show all current active alarms in the AK-SM 800A unit. An active alarm is one where no user action has occurred, for example the alarm(s) have not been acknowledged.

Use the check boxes to select or de-select different application types (HVAC, Refrigeration, Lighting, Misc.). A search field can be used to quickly search on device name.

Alarms on this list can be acknowledged individually or on bulk. To perform a bulk acknowledgement ‘check’ the device box and all entries will be selected – press the Acknowledge button to execute this action. Note that this will be recorded in the Audit trail.

Additional functions can be found along the top of the screen, Cleared, service, status and info

###### **Cleared**

This screen will show all alarms that have been set to cleared.

###### **Service**

This screen allows the user to send test alarms, suspend alarms, clear alarm log and delete alarm configuration. In addition, the internal relay (found on the AK-SM 800A) can be configured.

###### **Status**

Provides a quick status view (offline) of your connected devices.

###### **Top 5 alarming assets (past 7 days)**

The upper right segment of the screen shows a rolling analysis of what devices (top 5) are highest in terms of alarm occurrences. This is for information only and may help guide the operator on what to focus on to reduce alarm counts.

###### **Enabled Energy Features**

The AK-SM 800A includes several energy functions that provide autonomous control and continuous savings of operational efficiency, when combined with Danfoss controls. Any built-in energy feature enabled in the system will show green in the list. This information panel is designed to prompt users in ensuring enablement of these included features, thus maximizing energy efficiency of the store.

###### **Custom Screen**

The AK-SM 800A offers the ability to create a custom screen, populated with up to 15 points (OI, RO, SI, VO, Generic device). Once configured, the custom screen can be seen by pressing the second screen (2) button, found at the bottom right of the dashboard screen.

Note: To configure datapoints to show in the custom screen, navigate to the Configuration  System  Custom Screen. Here a selection can be made – in the example opposite, point 1 has been defined as a generic device (GN), Case 32 and the parameter u36 S6 Temp is selected.

Repeat this process for additional datapoints, upon completion press the 2 button to view the points. The values on this screen will auto refresh to provide an up to date status.

###### **Equipment**

To view a list of installed equipment, navigate to the equipment screen from the dashboard (grey bar will be indicated under Equipment menu).

Use the radio buttons to select which application type should be listed (Refrigeration, HVAC, Lighting, Misc) – by default Refrigeration is preselected.

A list of devices, grouped into Rack / Packs will be shown (reflecting the configuration).

To view more information on a particular device, press the > button, which will then show the device detail screen.

###### **Graphics**

To view any graphics loaded in the AK-SM 800A, navigate to the graphics screen from the dashboard (grey bar will be indicated under graphics menu)

**Note:** See the section on Utilities to get an overview on how to configure and deploy graphics on your AK-SM 800A.

##### **4. Embedded SvW remote user interface**

Once initial connection configurations have been established, often it is more convenient to use the System Managers built in web browser pages (SvW) for full commissioning. After your System Manager has established an IP address you can connect to the unit by typing in this IP address on your PC’s browser (assuming your PC/Browser is on the same network or can be routed to the IP address). The term ‘embedded’ is used to describe the System Manager Web browser pages because no additional tools or software is needed, all web browser pages are contained within the System Manager – hence the term ‘embedded’.

After you type the URL/IP address for the system manager, the initial login splash screen will be presented. If you don’t wish to see this splash screen for this unit again, simply check the ‘Don’t show again’ check box. Proceed via the ‘ **Continue to Login** ’ button.

The following screen will present the Username and Password input boxes – input user credentials as defined in the initial setup of the System Manager.

This section describes the built in (web) browser interface of the AK-SM 800A, known as the StoreView Web (SvW). From software release 5.0.x and above, SvW replaces SvB5 as the default remote user interface.

Your AK-SM 800A includes web server technology that ‘serves’ data that is then displayed in a web browser. SvW provides full access to all system screens and in some instances provides additional features not available in the local touch screen due to the preferred user interface (i.e. setup wizards are only found in SvW)

For ease of use, no special tools and setup is required, simply open a browser and type the URL/ IP address of your AK-SM 800A unit, for example; https://192.168.1.50 (Note: Danfoss always recommends HTTPS)

**Note:** At the time of user guide publication, Google™ Chrome™, Microsoft™ Edge™, Firefox™ and Apple Safari™ have been known to work satisfactory.

**Note:** You may observe that your browser provides a warning, suggesting that the connection to this site is not secure. In fact, the browser is providing this user warning as it has detected a selfsigned certificate which it cannot verify from a public database. In this instance you will need to continue to connect via the ‘proceed to…’ option (depending on your browser choice).

##### **4.1 SvW menu options**

Several of the key features / areas of SvW can be easily accessed via short cut buttons. These can be found by clicking the top left square multi-dot menu button.

Upon pressing the menu button, a fly-in menu of shortcuts will appear. The table below highlights each shortcut and provides a brief description.

Be aware that short cut buttons correspond to user authorization levels, so depending on user level, not all buttons will be seen.

|**Short cut button**|**Description**|
|---|---|
|Dashboard|The Dashboard represents configured application areas in separate 'panels'.|
|Equipment|The Equipment screen shows all configired equipment, shown in an expandable tree navigation format.|
|Alarms|Main alarm screen showing Active Alarms, Acknowledged Alarms, Cleared Alarms and Alarm Status/Service.|
|Schedules|Shows a graphical presentation of any configured schedule (i.e. defrost, lighting etc).|
|History|This History screen is the central page for loading and viewing saved History data.|
|Reports|The Report screen provides access to Refrigeraion, System and HACCP reports.|
|Graphic Editor|The Graphic Editor screen allows for the creation of custom graphics, then to be viewed on local or SvW .|
|Configuration|The Configuration screen is the central page for System Manager setup. From this page multiple sub menus are available for all<br>areas of system Configuration.|
|System|The System screen facilitates System Manager software updates, including device files. The import and export of the System<br>Manager database is also found under System.|

###### **4.1.1 Dashboard (via SvW)**

The Dashboard presents the central screen where configured applications are shown and are automatically updated, reflecting latest system/device status.

1. Menu button, providing quick access to other key system areas (subject to user permissions)

2. Home button defaults to Dashboard screen, but can be modified to show other screens via Config → SystemPreferences - Home screen

3. If the system manager has graphics deployed, the ‘Site Views’ link will be shown. Pressing this will present the custom graphics

4. Store Name (as configured in Configuration → System – Store Name)

   - **Note:** the following characters are not permitted in the site name fields

      6. Information button showing

         - a. SvW application version

         - b. Unit (800A) Store Name, License, sw version, IP address

         - c. Site primary/secondary units, IP/port details

      7. Browser certificate and SvW Alarm Preferences

         - a. Browser certificate (see page 107)

         - b. SvW Alarm Preferences – Enable alarm sound on your PC/ Alarm actions

      8. Log Out / Username who is logged in / SvW Portal<sup>(1)</sup> / Danfoss learning<sup>(1)</sup>

      9. Manual refresh button

      10. Expand button – use this to expand the Application panel

   - !”#$%&’()*+,-./:;<=>?@[\]^_`{|}~

5. Alarms Screen, defaulting to Active Alarms tab, access to Acknowledged, Cleared and Alarm Status/Service

> (1) Requires internet access

###### **4.1.2 Equipment view**

The Equipment view provides easy access to configured devices, driven via an expandable accordion menu on the left of the screen. Use the Equipment view to quickly navigate to devices, sensors and Inputs configured in your system manager(s)

###### **Device detail**

The Device detail screen presents additional details specific to a device or asset. Depending on device type and user privileges the menus and data will vary, but in a typical controller connected via the field bus, the following aspects can be seen.

1. Status – designed as a quick overview, providing initial status information

2. Alarms – access Active/Ack alarms or view cleared alarms

3. Settings – access to device menus status and settings (user permission dependent)

4. Graph – view history specific to that asset/device

5. Drop down navigation menu – depending on configuration, use this to easily navigate to other device detail screens

6. Additional info bar – view additional details about the asset/ device or point

###### **4.1.3 Managing Alarms**

Any active alarms will be shown in the Dashboard alarm panel. To view more details regarding the alarm, click the relevant alarm line or the Alarm bell in the upper right of the main screen bar. The Alarm screen provides details of alarms, easy navigation to Acknowledged and cleared alarms, together with additional functionality – see below for an overview of each of these aspects.

1. Active Alarms screen – where all alarms that are active (not Acknowledged)

2. Acknowledged Alarms screen – shows alarms that have been Acknowledged

      7. Export Alarms – Active, Ack, Cleared

      8. Manual refresh – manually refresh alarm screen

      9. Link to more details – Pop up box showing alarm details and where applicable, link to live details

3. Cleared Alarms screen – where alarms that are no longer in active state

4. Alarm Status / Service

   - a. Status Menu – list of alarms and alarm configuration threshold

   - b. Service Menu – Configure / Schedule / Send System Test alarms

   - c. Info Menu – for XML configured alarms showing connection status

5. Alarm Icon – Short cut to Active Alarms screen 6. Acknowledge button

###### **4.1.4 Schedule view**

The Schedule overview offers a graphical representation of any configured schedule. The following schedules can be seen via the lefthand menu (if configured).

- Store Open hours / Holidays

- Refrigeration Defrost

- Refrigeration Case lighting

- Lighting (store / car lot..)

- HVAC

An export icon can be seen in the far right corner, CSV and PDF options are available

###### **4.1.5 History (viewing)**

Your System manager can store datapoints from field bus devices and IO modules on a scheduled (frequency basis). The History screen allows you to request this saved history information and view it in graphical form. The Key aspects and functions of the History screen are described below

1. Select the desired time frame for history collection

2. Filter (search) for any history data point (for example Ther Air..)

3. Scroll list of all configured History datapoints available for selection

4. Draw or plot the selected History points

5. Datapoint ‘key’ showing logging interval, Min, Max and Average over sample period

6. Export History data

   - a. Export as .hst – this is a Danfoss proprietary file format that can then be imported for later viewing

   - b. Export as CSV

   - c. Export as PDF

7. History view unit of measure (Date, time, Pressure, Temperature and light level

8. Reset Zoom – you can zoom into a portion of the plotted graph by left clicking, holding, drag and select zoom area and release mouse button. Use the rest zoom button to clear your zoom

9. History time span over several days may result in pageanted view – use the arrow buttons to scroll through pages back and forth

10. Use this button to maximize screen for history graph

11. History (file) button – use this button to enter a new screen from where you can import .hst file. Upon importing file the history points contained within that .hst file will be shown in the equipment list, along with the time period saved to file.

###### **4.1.6 Reports**

Your SM-800A offers reporting, based on your configuration. Advanced reporting, analytics and many other enterprise grade functionality is available via Alsense.

###### **Refrigeration**

The refrigeration report will capture a live ‘snap shot’ of configured Refrigeration assets. Where applicable, the current value, Setpoint, alarm, defrost status and address is included in the report. PDF, CSV, Print

###### **System**

The System Report is a text file that includes many areas of a configured system Manager and can be used as a hand over document, as it captures all asset configuration, settings etc.

###### **HACCP**

See the section for HACCP for extended details.

###### **4.1.7 Graphic Editor**

Your System manager offers the ability to display custom graphics via it’s local screen and/or the remote web browser UI (StoreView Web). To build and manage files the built-in graphics editor is used. The main aspects of the Graphic Editor are described below.

1. Create new graphic - dialog box

   - Graphic files stored in the SvW cloud (available via SvW cloud, SvWDesktop with Internet)

   - Graphic files stored on System Manager (viewed via all SvW instances)

   - Graphic files stored (viewed on local screen)

2. Replace Background image

3. Import graphic files (stored in SvW cloud)

4. Export Graphic files

5. Graphic views – files viewed via remote UI (SvW) panel

6. Graphic views – files viewed via local screen panel

###### **Build and deploy graphics – hosted in SvW cloud (requires Internet connection)**

When connecting to your System Manager via SvW online (https:// svw.danfoss.com) the first option in the New Graphics dialog box is available. Select this option and enter a suitable name for the file (this name will then also be shown in the SiteViews menu).

Typically (not mandatory) a background image is included in the graphics project, use the browse button to locate the image (jpeg, png) then save. From the Graphic View panel, you will now see the new graphic file, to edit the file simply click on the file name.

Assuming there are already configured devices in the system manager, use the Equipment menu (1) to locate and then drag and drop data points to the background image.

**Important:** When a graphic file has been created and deployed via the SvW Cloud method, it is visible via SvW cloud and SvWDesktop (internet connected), not SvW Embedded.

Menu bar (2) allows the following actions / functionality

- Zoom In / Out / Reset

- Replace background image

- Save

- Edit panel – select Asset name / Parameter Name / Measurement Units / Address / Font size / font color / background color

- **Tip:** Hold down the Ctrl button and multi- select datapoints for editing.

###### **Build and deploy graphics – hosted in 800A (no internet required)**

When connecting to your System Manager via its IP / DNS address and using a web browser, SvW ‘embedded’ will be presented. Via this connection method, the SvW Cloud option will be greyed out, but the option to save graphic files to the System Manager is available. The name of the graphic file is fixed to sitefp1.flp, sitefp2. flp etc.

Follow the same procedure as described for the SvW Cloud option to add background image, mapping datapoints and editing / saving the graphics file.

**Note:** When adding a graphic via the SvW embedded method/ hosted in 800A, you will also see this shown in SvW Cloud and SvWDestop internet connections.

###### **Operating Notes for Graphic Editor**

Design and deployment options

|**Build & Deploy options**|**View Graphics via**|**File format**|**# of Files**<br>**(per SM)**|**Pre-requisites**|
|---|---|---|---|---|
|**Graphics hosted / stored in Danfoss**|**SvW Cloud**||||
|SvW Cloud (svw.danfoss.com)|• svw.danfoss.com|j / n|10|Internet connection|
|SvWDesktop (Internet accessible)|• SvWDesktop (internet enabled)|.pg  .pg||required|
|**Graphics hosted / stored in AK-SM 8**|**00A**||||
|• SvW embedded Browser<br>• SvW Desktop<br>• SvW Cloud|• SvW embedded Browser<br>• SvW Desktop<br>• SvW Cloud|.png<br><1 MB per<br>graphic|5|- No internet<br>connection required<br>except SvW Cloud|
|Local screen graphic<br>• SvW embedded Browser<br>• SvW Desktop<br>• SvW Cloud|• Individual local touch screen|.png<br>800 x 450<br>8 or 24 bit|5|- No internet<br>connection required|

###### **Existing graphics**

Prior to installing SW 5.0 it may be noted that the current application already has graphics deployed. The following section highlights the outcome of existing graphics under different use cases.

###### **Use Case: HTTP 800A v3.x,4.x upgrade to SW 5.0 maintain SvDesktop**

HTTP configured 800A unit(s) that currently has a graphics project deployed (hosted within 800A) and are viewed via SvDesktop.

After the 5.0 update the original graphic(s) can still be seen in SvDesktop (http only).

|**System Manager**|**migration?**|**Visible in SvDesktop?**|**Edit in SvDesktop?**|
|---|---|---|---|
|800A (http)|n/a|Yes (httponly)|No – need to toggle to SvB5 UI and edit there|

###### **Use Case: AK-SM 800A v3.x,4.x upgrade SW 5.0 maintain SvB5**

AK-SM 800A units that currently has a graphics project deployed and are viewed via SvB5.

After the 5.0 update the original graphic(s) can still be seen in SvB5 by toggling Remote UI to SvB5 in 800A Comm settings.

|**System Manager**|**migration?**|**Visible in SvB5?**|**Edit in SvB5?**|
|---|---|---|---|
|800A|n/a|Yes (http/https)|Yes – need to toggle to SvB5 UI and edit there|

###### **Use Case: AK-SM  v3.x,4.x to 5.0 view in SvW (all variants)**

800A units that currently have graphics project deployed (hosted in 800A) and are viewed via SvB5. If you want to upgrade to 5.x and then view in SvW (embedded).

After the 5.0 update the original graphic(s) can be seen in SvW, no user actions needed.

|**System Manager**|**migration?**|**Visible in SvW?**|**Edit in SvW?**|
|---|---|---|---|
|800A|auto|Yes|Yes|

###### **Migration**

Migration is the term used to describe the function of moving (migrating) graphic files originally hosted locally in the System Manager to the Danfoss SvW Cloud. Migrating graphic files keeps the original files in place but now also hosted in the SvW cloud, cloud services can now view the same graphics.

Vi a svw.danfoss.com o r SvWDesktop (internet connected), navigate to the Dashboard (Home) screen. Next to the Dashboard screen, the Site views menu can be seen. Within that screen, click on the Import button and then ‘Migrate’.

Assuming there is already a graphic already deployed in the System Manager and locally hosted, the Import dialog box will show a preview image and offer the ability to import various attributes.

Check all relevant attributes then click OK – this will migrate the graphics to the SvW Cloud. From there you will now see the graphic vi a svw.danfoss.com o r internet accessible SvWDesktop.

###### **General Graphic Editor Q & A**

- Q. I have new AK-SM 800A units in a Primary / Secondary configuration running 5.0 s/w and want to create some new Graphic project files. I’ll be creating my graphics using data points from all 800A units on the host network. When I save the project, where do the images and mapped points get saved?

- A. For SW 5.0 there is a known behavior that impacts where graphics are designed and deployed. This behavior will be revised in future updates, but for SW 5.0 it is recommended for Primary/Secondary host systems that all graphics are designed and deployed to the Primary unit. Subsequent connections should be to the Primary unit, resulting in full graphic views, including data points from any Secondary units.

   - In future updates it will not matter which unit is connected to for the Graphic design and deploy, until then, it is recommended to use Primary for all graphic design and deploy.

- Q. I have a AK-SM 800A that is running v4.x s/w and currently I can see the graphics via SvB5 remote UI. When I upgrade, can I see these graphics in SvW and if I want SvB5?

A. Yes

**Note:** SvB5 will be removed from AK-SM 800A in future updates.

##### **5. Configuration**

The following section describes the typical steps required for commissioning and configuration of your AK-SM. Although site applications can differ from one site to another, many setup procedures are common. This section assumes the AK-SM is mounted and all necessary power, network cabling and controllers are in place. The described workflow is based around the AKSM web browser interface (SvW), but would equally apply if being done via the local screen. Further detailed commissioning instructions are found throughout this user guide.

The AK-SM offers unique control flexibility in that both centralized and de-centralized control methods are supported. The term ‘centralized’ is used to describe the control of refrigeration Racks via I/O (Danfoss Input / Output modules). Under this method of control, the refrigeration control is managed directly from the front end (AK-SM), with field bus I/O. De-centralized control is the term used to describe the full support of Danfoss Pack and Case controllers. Under this method, each Pack or Case controller on the network can be seen as self-contained, with control logic built

in. The front end (AK-SM) under this type of application is more of a network manager, providing full read / write access and energy saving functions.

When starting your system configuration, you will have the opportunity to select either Centralized or De-centralized (or a mix of both) control methods.

The following areas of system configuration will be covered in this section:

1. Unit selector: if a host network is configured a drop-down menu will be visible, allowing quick access to each units configuration menu

2. Configuration menus

   - Quick Setup / Time / System / Comm / Security / Alarms / Control / Network Nodes / History / Schedules

##### **5.1 Quick setup / Wizards**

The quick setup buttons provide access to key areas of the System Manager or Wizards that provide a step-by-step configuration guide for key aspects. The Quick setup buttons / actions are only available via the Web interface.

###### **5.1.1 Quick Setup** → **System Setup**

###### **Preferences**

Configure the following details and preferences: Store Name, address, Unit name, your preferred SvW home screen, local screen time out Idle timeout (3 min – 24 Hr), Unit of measure, Generic Device Write Errors – used in conjunction with suspend polling – see section XXX, Offline status Indicator (when enabled, a * will be shown if communication to a field bus device is no longer active), Show Configuration Warning Pop-ups (active for local screen only and intended to warn if the user inadvertently

removes or reduces key configuration settings – i.e. # of Racks/ Packs reduced from 2 to 1, a pop up warning will be shown to avoid unwanted deletion of configuration).

**Note:** Following characters not permitted in the User Name, Site Name fields !”#$%&’()*+,-./:;<=>?@[\]^_`{|}~

###### **Users Wizard**

Create, modify users, user groups, authorization levels. For security purposes strong passwords must be used - at least eight characters long, one uppercase letter, a digit, and a ‘special’ character !@#$%

**Note:** The following characters are not accepted for the passwords “&’()+,-./:;<=>?[]\^_`{}|~ and spaces.

Enter number of users required (max 99), set password and browser language for each user

Enter the number of authorization types (max 7), against the settings line double click to modify the scope of system access

Press the Finish button to complete the Web Wizard.

###### **Refrigeration Layout Wizard**

The Refrigeration layout wizard is designed to improve on-site / connected initial setup and mapping of control devices. The wizard captures a workflow including scanning of configured field bus nodes, addressing and naming of the devices and finally allowing refrigeration devices mapping to form suction groups.

**Licensing Wizard** (Enter new license functionality) Not currently used.

The Refrigeration Layout wizard is intended for Danfoss Pack and Case (Evap) controllers that are addressed and connected to an operational field bus (i.e. Modbus/LonWorks).

**Limitations:** Whilst the wizard will layout the Pack and Case relationships, further controller configuration may be required. Currently the wizard is intended for Pack and Case devices and HVAC devices, any controls not designated as such will have to be configured using traditional config methods (see Configuration section).

###### **Starting the wizard**

From the configuration menu, start the layout wizard in the refrigeration section (the wizard will assume the relevant control devices (Danfoss Pack / Case) are addressed and connected via the field bus.

The wizard has 5 core steps:

1. **Network:** set your applications field bus channels

2. **Discovery:** perform a network scan and the resulting discovered devices will be shown in a table

3. **Compressors/Packs:** Define Pack devices. Please note the comments shown on this screen for limitations

4. **Circuits:** Any discovered evaporator controls / circuits will be listed in table form. You can easily change default names and if programming offline, add network addresses

5. **Suction groups:** here the Pack devices are shown in the left and the evap devices are shown in the right. Expand the Pack device and click on the resulting Suction icon, then in the righthand column select (check) the circuits that are intended to be part of that suction group. Continue with all other Pack / Circuit devices. Finally press the Finish button – the SM800A will configure it’s database with the corresponding layout.

###### **Copy Wizard**

Before performing the copy function it is recommended to ensure your SM 800A database is in sync with any control devices online – navigate to the Configuration → Network Nodes → Upload to perform this action.

The copy wizard is designed to speed up the commissioning workflow by providing the ability to define a ‘source’ device and then copy the settings to like type devices. In addition to controller settings, the copy wizard also provides the ability to define and copy alarm controller configuration and history point configuration.

During normal operations, your AK-SM 800A auto polls certain online controller parameters to sustain communications and to refresh key parameters at regular intervals. Please note that during the copy wizard process auto polling is temporarily suspended. Polling stops when you reach the parameter configuration screen. Auto polling will resume after a max 2Hr timeout or completion of wizard task or if wizard is cancelled, whichever is first. To cancel the wizard at any time only use the top left close ‘X’ button.

Some Danfoss controllers require that the ‘Main switch’ is OFF before allowing any parameter changes. To accommodate this fact, the copy wizard will automatically turn off the main switch for the source and destination controller(s). The main switch will be reverted to original position after the copy or copy/download is completed. Since the copy wizard changes the state of the device main switch, please pay special attention to operational conditions (i.e. food temperature) during this operation and validate all devices are correctly running after copy completion or cancellation of copy wizard. Failure to review device status may result in devices being left with main switch off (i.e. no refrigeration).

###### **Important limitations**

The copy wizard is currently not designed to fully support the Danfoss AK2 platform of devices (i.e. AK-PC 781, AK-CC 750..) since these devices have a different framework than other Danfoss controllers. When using the copy wizard in an on-line environment (connect to active controller network) the copy wizard will only allow ‘Alarms and History’ points to be set and copied. For full configuration of AK2 device parameters Danfoss recommends using the available Service Tool to facilitate commissioning on these device types.

Note: The copy function will only work against same device, application/code type and is not designed to fully support Danfoss AK2 style controllers.

###### **Preparation - Online Configuration**

For onsite (online) commissioning, the copy wizard assumes all relevant controller devices are installed on the network, have correct addressing, and if relevant application type set. Naming of the asset will also help in the copy wizard due to easy recognition of your devices. The ‘Layout wizard’ can assist in this preliminary task. During the final copy/download phase, the main switch of the target device(s) will be switched off then on after the copy/ download is complete.

###### **Important: Be sure to validate main switch status after copy wizard.**

Note: When assigning history points to a controller device a recommended max of 100 points per device is allowed.

##### **5.2 Conf i** **guration** → **Time**

The Time tab allows the system time, time zone, operating hours, daylight savings and holidays to be configured. Click a line to make any changes.

The following examples can be seen for the time zone London (GMT) = 000 Central Europe = 100 East Coast USA = -500

The operating hours can be set, that reflects your store operating hours. Any times set in this section can then be referenced to via a ‘Relative schedule’ . Relative schedules are found under the ‘Lighting’ and ‘HVAC’ application areas and apply a (user selectable) offset which references the operating hours schedule.

Holidays for full days must be operated with 00:00 open to 00:00 close and not 00:00 open and 23:59 close or 00:01 open and 00:00 close.

##### **5.3 Conf i** **guration** → **System**

Under the System menu, several sub menus are available

1. **System:** here the store details can be entered – these are the same as already described under the Quick setup → System setup

2. **Users:** these are the same as already described under the Quick setup – Users wizard

3. **Licensing:** not currently applicable

4. **System Report:** Under the SvW Menu ‘Reports’ a System Report can be found. Here, you can configure what aspects should be included in this report. In addition, there are some technical reports designed for Danfoss only.

   - Send Diagnostic Log to Danfoss: will send an e-mail to Danfoss Tech support with diagnostic data

   - Performance Log to Danfoss: will send an e-mail to Danfoss Tech support with performance data

5. **Files:** here you can see all the files required for SvW, Device files, Device management

6. **Custom Screen:** Use this screen to configure up to 15 points that will then be shown on the AK-SM 800A dashboard local screen (selected by button 2).

Assuming there is configured nodes available, click the Device Type line and select from the drop down menu. **Tip:** Select GN for generic or field bus controllers! Select the device and then the parameter. The resulting value will be shown.

##### **5.4 Conf i** **guration**  **Comm**

The Comm (Communications) screen allows for IP network settings to be configured. Follow the question lines on the screen to configure your AK-SM 800A according to site requirements. Any changes in IP configuration must be followed by system initialization (performed by the ‘press to initialize’ line at the top of the screen). The AK-SM 800A has two ethernet connections, eth(0) and eth(1). With software package R3.1 and above, eth(1) is enabled and is intended to support Danfoss Pack controller that uses IP for field bus communications.

###### **Press to Initialize (Press/OK)**

After any changes to settings on the Comm screen use the initialize function to perform an IP settings soft reset (unit itself will not reset).

###### **Press to reset this unit (Press/OK)**

To physically reset the SM 800A unit, press the OK button. **Ethernet 0** - Located inside of SM 800A and intended for corporate WAN/Host network.

**Ethernet 1** - Intended for ‘southbound’ field bus communications (Danfoss Pack IP controller).

###### **Internet (enable/disable - Yes/No)**

Enable this to allow remote communications (StoreViewBrowser 5, StoreViewWeb..) to your AK-SM 800A. **Select remote UI interface**

Default as SvW but SvB5 is available, toggle and refresh browser **Use HTTPS (enable/disable - Yes/No)**

Recommended for secure communications between AK-SM 800A and remote connections. **Note:** by default port 443 is used. **Use Secure TLS (enable/disable - Yes/No)**

By default will be enabled when selecting HTTPS. Disable for legacy Danfoss remote services.

###### **Use Header Authentication (enable / disable – Yes/No)**

New feature in Release 3.3 – see important note below For enhanced ‘Northbound’ communications (i.e. cloud / enterprise) enable this function. By default, ‘Use Header Authentication’ action is disabled to avoid the breakage of existing XML connections.

###### **Use DNS (enable/disable - Yes/No)**

Select ‘Yes’ if a DNS service is to be used. Preferred host name can be subsequently configured.

###### **Important:**

Consult with customer / 3<sup>rd</sup> party XML users before enabling this feature.

**Note:** By default, ‘Use Header Authentication’ is disabled to avoid the breakage of existing XML connections. If enabled, it will require current XML commands to be updated (all inbound XML communications must include user/password in header). Failure to do so will break existing XML communications.

**Host Network (enable/disable - Yes/No)** Enable/Yes if your application will use more than one System Manager interconnected on a host (IP) network. If enabled, enter number of units expected on host network Node to be used as – select Master for unit zero (as set by rotary address switch behind front panel cover) or ‘Slave’ for other units on host network (each unit must have different address switch addresses).

Slave IP address – enter the IP address for the slave(s). **Note:** If the requirement is to access the AK-SM 800A host network over the Internet you must configure the # of Ext Internet and Internet web port settings (continue to read below).

###### **Use DHCP (enable/disable - Yes/No)**

Select ‘enable / Yes’ if AK-SM 800A is to be connected to a DHCP server. Select yes and manually enter the IP address that the AKSM will use if DHCP fails.

##### **5.5 Conf i** **guration**  **Security**

Danfoss takes security seriously and as part of our continued improvements, new measures are being implemented. **Please review below important security updates included in the latest AK-SM 800A software update that may impact your upgrade experience.**

System Manager 800A software package v4.0x and above enhances your product’s security features to meet internationally recognized regulations such as the NIS2 and CRA Directives. Also following the global standard IEC 62443-4-1 Standard in regard to security by design p ractices, and to comply to NIS2 and CRA European regulation requirements (Danfoss keeps the focus on IT Security) . In compliance with IT best practice and mandatory standards, Danfoss is now defaulting to a strong security posture on the System Manager 800A, via software package 4.0.x and above. This feature is called **Session Control** and when combined with HTTPS improves overall security of your product.

###### **What is Session Control?**

Session control in the AK-SM 800A is an authentication rules engine/module and is intended to improve the overall security posture of your system. Session control offers different configuration settings (Backward compatibility, Permissive and Strict). Depending on how these settings are configured, the remote interface will need to comply accordingly.

###### **What is a remote Interface?**

The term remote interface refers to StoreView Browser 5 (SvB5), StoreView Web (SvW), Alsense™ (Danfoss Digital services) and 3<sup>rd</sup> party XML1.0. SvB5, SvW and Alsense™ already support Session control. 3<sup>rd</sup> party XML1.0 users will need to update requests if Strict mode remains selected (see below).

###### **What are these Session Control settings?**

###### **After AK-SM 800A software package 4.0.x is installed, Strict mode is default, what does this mean?**

- Your AK-SM 800A now requires secure Internet standard of HTTPS (encrypts all data in transit)

- In Strict mode, 3<sup>rd</sup> Party XML communications to the AK-SM 800A cannot contain usernames/passwords and must provide the session token in the AKSM-auth header

- For AK-SM 800A systems that have 3<sup>rd</sup> party XML interfaces, Danfoss has supporting documentation, please contact Danfoss Technical Support , Salesforce “ New Case Creation ” .

- Depending on your method of upgrade a pop-up message will be presented, informing of Strict mode but also allowing fall back to Backward compatible

- Depending on your method of upgrade your remote browser session my be lost. In this event you may need to manually type https in front of your system managers IP/DNS name

- After the software installation you may revert back to (weaker configuration) by selecting ‘Backward Compatible’ mode – Danfoss recommends Strict mode.

###### **Important installation notes for System Manager R4.0.x**

Before upgrading to R4.0, take a moment to review your current implementation. For instance: check how your AK-SM 800A network is configured, are any 3<sup>rd</sup> Party XML entities involved?

After installation of System Manager software package 4.0x the unit will reboot an d **will immediately default to Strict enforce level** .

**Note:** If you are uncertain about your AK-SM 800A’s current configuration for web communications, we strongly recommend performing on-site update only or having personnel on-site or contact Danfoss Technical support for further guidance.

**If your AK-SM 800A application is already configured for HTTPS** , the remote update will not require any additional manual steps apart from confirming Strict mode.

**If your AK-SM 800A application is configured for HTTP** , there will be a workaround to support a remote update dependent on network setting (detailed guidelines will follow), but in case of any doubt an **on-site update is always recommended** .

The important aspect to note is that immediately after installing System Manager 800A software package 4.0.x and above, Strict mode is set by default. These settings can always be managed via the System Manager Configuration  Security menu.

|**Session Control**<br>**setting**|**Description**|
|---|---|
|Backward<br>Compatible|Not recommended but when selected, http is<br>available, and no session tokens needed.|
|Permissive (used<br>as a transition to<br>strict level)|Set this level to view any error responses so that<br>adjustments can be made in preparation for<br>strict mode. Permissive is allowing both the old<br>authentication and the new authentication scheme<br>at the same time.|
|**Strict (default**<br>**immediately**<br>**after R4.0**<br>**install)**|Require HTTPS connection XML requests cannot<br>contain usernames and passwords. Must provide<br>session token in the AKSM-auth header. HTTPS<br>becomes mandatory and authentication moves from<br>plain-text to session-based authentication. Strict<br>mode will sanitize all strings in the Northbound<br>connection of XML, rejecting any commands that<br>conflict with the sanitization.|

##### **5.6 Conf i** **guration**  **Alarms**

The Alarms screen has a sub-set of screens; Connections, Service, Alarm Routing, Relays, System, Offline

Go through each sub tab to ensure all areas are correctly configured as per site requirements.

###### **Connections (e-mail, remote, XML)**

Define the number of connections (up to 4), then select the connection type. The AK-SM 800A can offer the following alarm IP based alarm output;

e-mail, Remote (Danfoss Electronic delivered services) and XML.

Depending on your configuration the screen will reflect the required inputs in relation to your selection. Below is a description of alarm type

Disabled = No alarms will activate on this point

Log Only = When an alarm occurs on this alarm point it will only register in the AK-SM 800A alarm log - no physical alarm output Normal = When alarm is active the output will be sent once (alarm may get re-triggered if the stop condition is set for repeat) Severe = When alarm is active the output will re-send every xx min Critical = Same as Severe but with separate re-trigger time - when alarm is active the output will get re-sent every xx min Delete = Removes any applied alarm settings

Select Alarm Action type (defined under Alarm routing) Auto Test: Scheduled: Configure days & time for test alarm Repeated: Configure interval time for test alarm Suspend alarms generation (suspend All alarms in the system from being sent): Set time period (min/Hrs) to stop alarms being sent Any relays configured for alarm output can be forced on / off for testing purposes.

Remember to leave in Auto position after testing.

**Note:** To ensure alarms are sent correctly, please ensure a schedule is configured. Failure to set a schedule will inhibit any alarm output.

###### Connection type: Remote

- Use this option if the AK-SM 800A is subscribed to Alsense™

###### Connection type: XML

Connection Type: e-mail

- Enter valid server name (or IP) for e-mail server

- Your AK-SM 800A supports SSL/TLS e-mail encryption standards, be sure to enter the relevant username and password

- Send to: Add the e-mail address for intended recipients

- Reply to: mandatory field that must have a valid entry (address with same domain name).

- An abbreviated message would have reduced text in the alarm message

- Use this option if the AK-SM 800A is to send alarms to a 3<sup>rd</sup> party XML based service.

###### **Service**

The service tab is designed to allow test alarms to be generated. There is also an auto alarm test that can either be on a scheduled or repeated basis.

The suspension of alarm output is also possible, with user options of selecting the interval period

- Configure a schedule to enable the alarm e-mail output

Clear alarm log will clear logs seen in the system. **Note:** Under the utilities section of StoreView Browser 5, the cleared alarm log will maintain a full audit log of ALL cleared alarms, irrespective is the clear alarm log selection is made in the service screen.

Delete alarm configuration is available in the screen.

The AK-SM 800A internal relays can be configured per site requirements.

of the alarm configuration is the ‘Alarm Routing’ page, where different routing options can be defined, along with time delays and alarm output stop conditions.

The central alarm action matrix allows various output options (known as alarm actions) and alarm handling configuration to be centrally assigned. Once the alarm action matrix has been defined, any controller or I/O point can be given an alarm action number. The alarm action number corresponds to the appropriate output. (as defined in the alarm routing page). Alarm output options include:

- 5 external (AK I/O) relay outputs

The line item AK(2) Generic Device –‘ Send alarm route clear’ is used, to clear the alarm route in ALL connected Ak2 controllers and is required if the AK2 controller was connected to another Danfoss system prior to getting connected to the AK-SM 800A series (i.e. AKA Gateway/SM720).

- Local AK-SM buzzer

- Local AK-SM front LED

- Internal alarm relay

- 2 Network connections

- 6 IP / e-mail addresses (3 per alarm receiver)

Change the parameter to YES and a scan will be initiated, the alarm route in AK2 will be reset, and your AK2 devcie(s) will now have valid alarm routing.

###### **Alarm Routing**

The AK-SM utilizes an Alarm Action Matrix that allows a high degree of flexibility for various alarm routing options. At the heart of the alarm configuration is the ‘Alarm Routing’ page, where different routing options can be defined, along with time delays and alarm output stop conditions.

The AK-SM utilizes an Alarm Action Matrix that allows a high degree of flexibility for various alarm routing options. At the heart

The following example can be seen as a guide to configuring your AK-SM alarm logic options;

###### **Relays**

If the alarm output includes relay(s) the Relays tab should be accessed to configure the board & point address for these.

To configure an alarm action, navigate to the required output line (I.E. Relay A) and press enter. The resulting screen allows the configuration of the alarm actions, any pre delays, duration times and stop conditions. The results of this configuration will be shown in the alarm routing page.

*[Figurtekst: Alarm Actions (1-8) · Up to 8 alarm actions can be defined. Each alarm action can have multiple · outputs, making the AK-SM alarm output options very flexible. ‘Look down’ · each alarm action number column and any associated outputs will be seen in · the left hand column. · Delay · Once an alarm action is defined the · associated time delay for the action can be · set. This delay is in addition to any delay · Component Column (alarm output) 1 2 3 4 5 6 7 8 Del Dur Stop already defined in any controller (i.e. EKC) · Select from the options seen in this · column; Relay A - - - - - - - - or monitoring points (i.e. I/O) defined in the · system. · • Relay A-E Relay B - - - - - - - - · • Front LED Relay C - - - - - - - - · Duration · • Buzzer Relay D - - - - - - - - A duration time is available when either · • Int. Relay Relay E - - - - - - - - Time or Time/Repeat are selected as stop · • Network 1 Front LED - - - - - - - - conditions. The duration setting defines · • Network 2 Buzzer - - - - - - - - the length of time the alarm output will be · Int. Relay - - - - - - - - active for (irrespective if the alarm is still · Phone 1 - - - - - - - - active or acknowledged or not)Available in second or minute selections. · Danfoss80Z8115 0 Sec/ Min duration will result in the alarm output remaining off. · Min = 0 Sec/Min Max = 99 Sec/Min · Stop · The stop condition defines when the alarm · output will stop or return to configured · position. The following definitions apply; · Time  = Stop on time (set under duration) · Ack  = Stop on alarm being acknowledged · Clear  = Stop when alarm clears · Time/Rep  = Stop after time delay but repeat · if alarm is still active · Ack/Rep  = Stop after alarm is · acknowledged. If alarm still active after · acknowledge repeat alarm action (repeat]*

Alarm Actions (1-8) Each alarm action can have multiple relays, IP address, etc assigned

Custom text that better reflects the alarm relays **Delays & Stop** can be entered. conditions Set pre Use the ‘component delay, duration and name display’ to toggle stop conditions (for between custom text & each alarm output factory name (Relay A, selection). Relay B...). **Alarm output options** Select the appropriate ‘component’ (i.e relay, network) and configure by double clicking on the appropriate line.

###### **Example configuration**

- This example will describe the steps to configure an alarm actions. Alarm action 1 will be defined according to the following;

- Relay A should trigger after a 10 second pre delay. This relay will energize any time and will only reset when the alarm clears.

- The Front LED should activate (de-activate LED when alarm clears)

- The Buzzer should only activate during the Day (Buzzer stops when alarm is Acknowledged)

This opens another page that allows the configuration for that output to be set. In the example below Relay A and the Buzzer can be seen. Follow the same process for the other outputs. For e-mail output, navigate to the Network 1 line and press enter.

Here, set the action, time delay & stop conditions. (The actual e-mail configuration is done in the Alarm ‘Connections’ page). The results of the alarm output configuration can be seen in the central Alarm Routing page. Follow this process for other actions.

- Alarm message should also be sent out via e-mail

To define the alarm output options navigate down the page and double click the relevant line.

The above alarm outputs are associated with action 1 - ‘look down’ the alarm action 1 column and the relevant outputs can be seen in the left of the page.

‘Look down’ Alarm action 1 column

Relay A Configuration page

###### **Action settings:**

Once in the actual output page, navigate through the lines and set the relevant Action. Each action can have the following settings;

**Not Selected :** No action **Enabled :** Will enable this output action (any time of day) **Day :** Enable this output during day status (based on store opening times (Configuration Time)

**Night :** Enable this output during night status (based on time outside of store opening times

(Configuration  Time)

###### **Delay, Units & Stop settings:**

To complete the output configuration set the time delay, units & stop conditions should be set. Stop conditions;

**Time** = Stop on time (set under duration) **Ack** = Stop on alarm being acknowledged **Clear** = Stop when alarm clears **Time/Rep** = Stop after time delay but repeat if alarm is still active **Ack/Rep** = Stop after alarm is acknowledged. If alarm still active active after acknowledge repeat

###### **Relays**

If the alarm output includes relay(s) the Relays tab should be accessed to configure the board & point address for these relays. The example below shows relay A & C, with the associated (AK I/O) board & point address.

###### **System**

AK-SM system based alarm conditions should be set under the System tab. The alarms seen in this page are factory set but can be changed as per site requirements. Navigate down each line and configure (pressing the enter key) as required. The following items can be seen and changed under the System tab;

**Host Comm error Host count error**

**I/O Network Fail** : Alarm if communications to AK I/O fails Flash Memory fail: Alarm if AK-SM system memory fails Database Cleared: Alarm if AK-SM database is cleared

**File Error** : Alarm if critical files do not load / not present on AK-SM system (I.E. Device list missing)

**Alarm fail remote Alarm fail e-mail Alarm fail XML**

Alarm if any active alarms were unable to be sent out **NTP Failure** : Alarm if the network time protocol fails Host Comm: Alarm If host communication fails **Host Count** : Alarm if one or more AK-SM units disconnect from host netwok

**Ram Disk Full** : Alert alarm if Ram is getting full (due to EDF files) **Freq Response On Ethernet Fail Static IP fail DHCP failure Load level high History collection failure**

###### **Offline**

If Controllers (Danfoss Evap & Pack, Power meters) and, I/O has been used in the control configuration (Lighting, HVAC, Refrigeration etc.), these devices can be seen under the I/O Comm tab.

The I/O Comm tab allows any offline communication alarms to be configured. The example below shows an evaporator controller (address 1) with the alarm level set to ‘Normal’ & alarm action ‘1’. These factory settings can be changed in this page.

Any AK I/O points used in the AK-SM system can be found on this page, with the associated alarm level and actions set. The factory settings can be changed as required.

###### **Calculations & Other**

If any calculations have been defined in the AK-SM system, alarms can be associated with these. Use the Calculations tab to set appropriate alarm levels and actions.

##### **5.7 Conf i** **guration**  **Control**

The control tab is the central configuration page for your control requirements. It lays out the different application areas and allows the Commissioning Engineer to define what applications are on site. Once the application areas are defined on this page, more detailed commissioning is done in the dedicated application tabs (covered in following section).

Please also note that the SM provides the ability to configure centralized or de-centralized control.

Centralized control is where your SM has the control logic built in and uses Danfoss I/O to provide refrigeration control. Decentralized is the control method via the use of Danfoss Pack and case controllers.

**Note:** depending on your license version, different applications may be visible (or not).

For de-centralized control, ensure the control type is set to your required controller type (via drop down menu).

Pack & Case

For centralized control, ensure the control type is set to IO (input/Output). This alerts the SM that you wish to use Danfoss Board and Point configuration for your refrigeration application.

###### **Show only scanned devices:**

Select ‘yes’ if your controller devices are already on the network, with valid addresses and connected to the AK-SM. By setting to ‘yes’ and after a network scan (covered in next section) only discovered devices will be shown in the drop down boxes. If your controllers are not yet on the network, keep this selection to no.

###### **Number of racks/packs (max 12):**

Enter the required amount of suction groups.

###### **Rack type**

(Use I/O selection for centralized control, select controller type if using de-centralized)

**AK IO** = built in control via AK I/O **No Compresso** r = No Compressor control **Device selection** = select required controller

**Note:** Variable speed drive can be selected as a pack controller.

**Suction groups** (Suction group or Evaporator control) Add your required quantity of suctions groups (centralized logic) OR enter how many evaporator controls are available under your Pack (de-centralized)

**Note:** suction group / evap configuration is then done under the Refrigeration tab.

The following screen shots below represent an example of decentralized configuration (Pack and Case control).

The AK-SM has been configured for two pack controllers (AK-PC 730 and the AK-PC 840), with 5 Evaporator controllers under each pack. Selection for each Pack controller was made via the pop up box that appears when the Rack line is double clicked.

Double click to select your required Pack device.

Once the Pack controllers have been defined and the number of case controllers under each pack have been set, continue to the Refrigeration tab for detailed configuration.

First, navigate to the ‘Address’ tab. Enter a valid network address, corresponding to the address already set in the field controllers.

**Note:** If your field controllers have already been configured with the relevant parameters set, you may wish to perform an ‘Upload’.

This function forces the AK-SM to pull back the controller settings and thus synchronize the AK-SM database. Only use the ‘Download’ function if you have finished controller configuration on the AK-SM and you wish then to send these settings ‘down’ to the controller.

A one click option for this (upload/download) can be found under the Configuration  Network Nodes tab.

Once all the addresses and custom naming is complete escape out of the addresses menu and navigate to the ‘Suction’ tab. This will allow for configuration of the Pack Controller(s). Use the drop down (Suction) menu to access each Pack controller and the corresponding menus. Please note that any online controller devices will invoke a dialog box which asks if you wish to retrieve the data from this controller. This dialog box is intended to direct the choice of either uploading data from a controller (overwriting any previous settings held in the AK-SM database) or not. If you have existing controllers on the network which have already been configured, choose the upload option (this need only be done once for each controller you view).

The AK-SM holds a database in which all the system configuration is held. This includes any actual controller devices connected or just devices that have been selected ready for configuration. It is important to recognize when to perform an upload or download function so that any preset configuration is not overwritten by automatic upload by the AK-SM.

###### **Upload**

This function may be required where the case and pack controllers have already been configured and all parameters are set according to customer specifications. In this instance the need is to typically perform an upload function, thus updating the AK-SM database to fully reflect the controllers commissioned settings. Once this has been done, changes to the controller settings can be done directly from the AK-SM.

###### **Download**

The opposite to this would be where the controller devices have not been set per customer specification and the AK-SM should be used as the commissioning tool or window into the controllers. By navigating through all the controller screens in the AK-SM it is possible to configure the controller parameters and then send

###### **Copy function**

To aid the commissioning process, the AK-SM offers a settings copy function which can be used to copy one device settings and alarm configuration to other (similar) device(s). This function works when copying settings to and from same controller version / type devices. The procedure described below is one example of the copy /paste function.

Use the Copy tab to open the copy page, where any same controller type devices can be copied to. The actual device page will act as the copy base, so ensure the correct circuit is selected (in the drop down list). Select **all** or **individual** controllers that will be copied to, then press the copy to line.

these setting to the connected controllers via the download function.

- Controller must be online

- Some controller types require the main switch (R12 parameter) to be off before certain changes can be made

**Note:** the copy function copies controller parameters etc from once device to the AK-SM database, to complete the operation the (copied) settings need to be downloaded to the required controllers.

The Global download function can be seen under the Network Nodes Download section.

###### **Import SI | OI function**

Use the **Import SI (Sensor Input)** and **Import OI (On/Off)** function to gain access to ‘generic’ controller (Evap & Pack) parameters that are normally not accessible for alarm / logging / Boolean use. This function can be used to alarm on specific parameters not in the factory alarm list and / or can be used to import controller parameters in the Boolean logic calculator. Up to sixteen points can be selected per controller. This function extends the flexibility of controller support in the AK-SM and opens up the generic controllers parameter list for more customer specific needs. The following steps highlight the procedure in ‘Importing’.

From the import page(s) double click an import line to present a pop up box that shows all available parameters. Select the parameter that you wish to ‘import’ from the controller (you may give it a custom name).

In the example below, the parameter Po Setpoint has been selected. This parameter can now be seen in the miscellaneous calculator.

###### **Extended Config function**

Extended configuration (changing what parameter is seen in the System View, Dashboard & Device detail status) Using the extended configuration tab the factory standard parameter that is used for ‘System View’ status can be changed. This feature is useful in giving the end user more flexibility in showing the relevant sensor at the system and device detail views. By changing the overview value the AK-SM will then display the new selected parameter or status in the system view, Dashboard and device detail pages.

###### **Important note:**

Dependent on the load of the system it can take up to a minute, before the imported value can used in e.g. a calculation for further use.

If the import of a value is basis for a secure operation we strongly recommend to find other ways to secure the system.

###### **Alarms and Alarm Select**

Use the Alarm tab to define the alarm actions associated with this device. Use the Alarm select tab to select up to 300 alarm points (max 300 per AK-PC controller)

##### **5.8 Conf i** **guration**  **Network Nodes**

If your application already has controllers and/or I/O modules set and powered, you may wish to perform a network scan to validate their connection to the AK-SM. Follow this section to perform a network scan.

###### **Node Overview**

Under Node Overview your network ‘type’ can be selected, and subsequent scanning of the field bus can be initiated.

###### **Modbus configuration**

System Manager software includes improvements for managing serial Modbus devices, in particular the following updates can be seen:

- Ability to define Modbus (Channels 1 & 2) node address scan ranges – this will improve scan efficiency time, rather than the previous default full Modbus address range (1 – 199), you may specify an address range specific to the controls installed on the Modbus channel.

- Ability to use Modbus#2 for 3<sup>rd</sup> party Refrigeration and utility controls (Non Danfoss).

Modbus channel 2 enables additional device connectivity via the support of non-Danfoss Modbus controls, commonly known as 3<sup>rd</sup> party. This is done via user configurable Modbus configuration ‘slots’, where each ‘slot’ may represent Modbus device type(s). Once configured and the relevant device file (EDF) has been loaded via StoreView Web, it is possible to establish Modbus communications and show device parameters in the AK-SM 800A.

From the Configuration tab select the ‘Network Nodes’ sub-tab. When your field network is complete, and all controllers are on line a network scan can be initiated. The operation of a network scan allows the AK-SM to be aware of any controller devices on the network, allowing the AK-SM to communicate and function with the controllers on the field bus.

###### **Notes:**

1. Due to the varying implementation of Modbus Protocol in different devices seen in the market, it may not be possible to support all 3<sup>rd</sup> party devices or parameters. At time of writing Refrigeration and utility meter types are supported

2. At this time, creation of 3<sup>rd</sup> party Modbus device file(s) is managed by Danfoss ECS Technical support – please contact ADAP-KOOL support concerning 3<sup>rd</sup> party topi c https://danfoss. lightning.force.com

3. Modbus channel 1 is designed for Danfoss only (including existing 3<sup>rd</sup> party devices built into AK-SM 800A firmware).

4. Danfoss Modbus devices support and default to autobaud rate detection. This presents a challenge when trying to mix other devices that need to operate on fixed baud rates.

**Note:** do not initiate a network scan via this screen and in parallel start the layout wizard (which would set an additional scan process). If scanning for network nodes either use this screen or the layout wizard - not both concurrently.

**Rule:** Danfoss Modbus controls should only be mixed with 3<sup>rd</sup> party devices on Modbus#2 if all 3<sup>rd</sup> party devices can be configured to the same Modbus properties. All 3<sup>rd</sup> party devices must be set to either, 9600|even|8|200<sup>1)</sup> , 19200|even|8|200<sup>1)</sup> or 38400|even|8|200<sup>1)</sup> . If the 3<sup>rd</sup> party device cannot support these settings Danfoss controls should not be placed on Modbus#2.

You may have differing 3<sup>rd</sup> party device configurations (i.e. baud rates) without Danfoss controls ONLY IF those devices do not use auto-baudrate switching.

1) You may modify the timeout property (keeping other properties the same) if your 3<sup>rd</sup> party Modbus device requires slower response time.

###### **Channel SNMP**

SNMP is an Ethernet based southbound field bus technology.  It is important to note for reliable scanning the IP Network Polls should be set to 2.

The Rescan Range type can be Subnet or IP address, configure Subnet Range1, 2,3 applicable to application.

Auto Scan if All Nodes offline – This is a feature (default off) that then enabled will trigger a scan automatically.  This is intended to automatically recover from intermittent server or network-based issues. Will only trigger if all configured nodes are marked offline.

Auto Scan if Node/IP Mismatch found – when enabled (default as disabled) will perform a full re-scan.  This could occur if SNMP modules are on a DHCP enabled router, in which a device will be issued a different IP address.

###### **Example A: Modbus configuration (Danfoss + 3**<sup>**rd**</sup> **party on Modbus#2)**

In the below example the AK-SM 800A (running R3.2) has been configured to communicate with Danfoss and 3<sup>rd</sup> party devices. Both Modbus 1 and 2 have been enabled with appropriate scan ranges to ensure efficient scan performance – see below table. This example shows the AK-SM 800A configured for 150 case controls, using Modbus channels 1 & 2

- Modbus channel 1 has 120 Danfoss controls

- Modbus channel 2 has 20 Danfoss evap devices + 10 3<sup>rd</sup> party

- Totalling 150

|**Serial Modbus devices**|**Unique**<br>**control device**<br>**address range**|**# Modbus**<br>**configurations**|
|---|---|---|
|Modbus channel 1 (Danfoss)|1 – 120|n/a|
|Modbus channel 2 (Danfoss + 3<sup>rd</sup><br>party)|130 – 160|1|

###### **Modbus#1 Configuration**

As Modbus 1 is used exclusively for Danfoss controls there is no configuration needed, except if required, to adjust the address range for the Modbus scan as noted in table. In this example there are 120 controls, with address range 1 – 120. As a result, the scan address range can be set to 1 – 120 as indicated in the image below.

###### **Modbus#2**

As Modbus 2 is used for Danfoss and 3<sup>rd</sup> party controls, some configuration is needed (in addition to the scan range configuration if required). In this example it is assumed that the 3<sup>rd</sup> party device file has previously been loaded into the AK-SM 800A via StoreView Web and the AK-SM 800A unit was re-set to auto populate the internal device file table. This example also assumes that the 3<sup>rd</sup> party devices have the ability to set Modbus properties (i.e. baud rate etc) to comply with ‘note 4’ and are set to match the max speed default in Danfoss AKC and AK-CC evaporator controllers.

Each red box indicates required configuration:

1. Configure scan range (in this example 130 – 160).

2. As there are two device types on Modbus channel 2 (Danfoss & 3<sup>rd</sup> party) but they share the same Modbus configuration profile (i.e baud rates) this is set to 1.

3. Configuration 1 is set for Danfoss and 3<sup>rd</sup> party controls (38400|Even|8|200).

Scan, detect and map

After configuring the Modbus channels, initiate a rescan and observe controls being detected via the Configuration → Network Nodes → Node overview table.

From the Node overview screen, navigate to the Configuration → Network Nodes → Scan Status and then → Controllers screen. Here you will see all scanned generic devices, including 3<sup>rd</sup> party. **An important note is that this screen may reflect your 3**<sup>**rd**</sup> **party device as a model type other than expected.** It is common that 3<sup>rd</sup> party controls do not declare what device type they are during a scan so initially the AK-SM 800A makes a ‘best guess’. The (unique) network address will be the key identifier, from which to locate the 3<sup>rd</sup> party device(s).

To correct this device model type, double click the associated gear icon or press the ‘>’ on local screen. The resulting > Device Type screen will then allow the correct device file association via a dropdown list.

After selecting the correct device file from the drop-down menu, the controller will correctly reflect model type and can be seen as a generic device in the AK-SM 800A.

**Note:** Currently, Danfoss AK-RC 2xx, 3xx (Optyma™ room controllers) are compatible only on Modbus#1.

###### **Example B: Modbus configuration (two 3**<sup>**rd**</sup> **party device types on Modbus#2)**

In the below example the AK-SM 800A (running R3.2) has been configured to communicate with Danfoss and 3<sup>rd</sup> party devices. In this example two different 3<sup>rd</sup> party device types are installed on Modbus#2 and because they have differing Modbus profiles (Baud rates etc) have 2 configurations and Danfoss controls are not installed on Modbus#2.

Both Modbus 1 and 2 have been enabled with appropriate scan ranges to ensure efficient scan performance – see below table. This example shows the AK-SM 800A configured for 150 case controls, using Modbus channels 1 & 2

- Modbus channel 1 has 120 Danfoss controls

- Modbus channel 2 has 30 3<sup>rd</sup> party devices (two types)

- Totalling 150

###### **Points**

Under the Points menu, sub tabs of Relay, Sensors, On/Off Inputs and Variable Outputs will be shown. This tab relates to any AK I/O configured points, the term points relates to AK I/O relay, sensors, On/Off Inputs and variable outputs. Any control questions that have required AK I/O control will be seen in these tabs. The purpose of these tabs is to allow the viewing of the I/O point status.

###### **Scan Status**

Under the scan status menu, sub tabs of All nodes, Controllers, I/O Boards and Other Nodes will be seen. Use these screens to check that your expected devices or I/O are seen and listed as expected. All Nodes : Central list will display configured devices and points. Only configured controllers will be visible in this list.

Controllers : To view any scanned generic controllers. This screen will also reflect address and controller type

I/O Boards : Display AK Board & Point status. Other Nodes : List of other nodes

|**Serial Modbus devices**|**Unique**<br>**control device**<br>**address range**|**# Modbus**<br>**configurations**|
|---|---|---|
|Modbus channel 1 (Danfoss)|1 – 120|n/a|
|Modbus channel 2 (3<sup>rd</sup>party, two<br>types)|130 – 150|2|

###### **Modbus#1 Configuration**

Refer to example 1, no change in this configuration.

###### **Modbus#2**

As Modbus 2 is used exclusively for 3<sup>rd</sup> party controls, some configuration is needed (in addition to the scan range configuration if required). In this example it is assumed that the 3<sup>rd</sup> party device files have previously been loaded into the AK-SM 800A via StoreView Web and the AK-SM 800A unit was re-set to auto populate the internal device file table. This example assumes that the two 3<sup>rd</sup> party devices have differing Modbus properties (i.e. baud rate etc) and so to comply with note 4 Danfoss controls are not installed on this channel.

Each red box indicates required configuration:

1. Configure scan range (in this example 130 – 150).

2. As there are two 3<sup>rd</sup> party device types on Modbus channel 2 and each have differing Modbus profiles, 2 configurations are set.

3. Configuration 1 is set for 3<sup>rd</sup> party control type 1 (38400|Even|8|200).

4. Configuration 2 is set for 3<sup>rd</sup> party control type 2 (19200|Even|8|175).

###### **Config Status**

A list of nodes that reflect address, status (online / offline) and model type.

###### **Duplicates Tab**

Check this list to make sure no two devices have been assigned the same network address. Any duplicate address will be shown in this list. Correct any address issues and re-scan.

###### **Files**

Under the Files menu, sub tabs of Device Files, Device Management and MCX Upgrade will be seen. Use these screens Device Files : A complete list of EDF files Device Management : Groups of same device type MCX Upgrade :

###### **Upload Tab**

The upload tab will list any controllers that have been uploaded. The upload function can be performed in the **Configuration**  **Control** area (one controller at a time) or here (multiple devices with one command). The process of an upload takes the current parameter settings and values from the controller(s) and loads them into the AK-SM database. This operation ensures that the AKSM database is synchronized with any pre-configured controllers on the control network. Any upload failure will be shown on this screen, else a time / date stamp will be shown when successful.

###### **Download Tab**

The download tab will list any controllers that have been processed for download (where the AK-SM sends parameter data to the device). The download function can be performed individually under the **Configuration**  **Control** page or here, where multiple controllers can be selected for download (using one command). The process of a download takes the AK-SM database values and downloads them to the selected controller(s). Any upload failure will be shown on this screen, else a time/date stamp will be shown.

After the network scan has completed, any resulting count will be seen against the Nodes Scanned on Network line - this reflects the number of found nodes on the scan just completed. The corresponding line below (Nodes configured in database) reflects the current total of network nodes actually configured in the AK-SM database. The last group in this table refers to the following node types:

- OI (Output|Input)

- RO (Relay output)

- SI (Sensor Input)

- V02 (Variable output)

- Utility Meter (WattNode, Veris, Carlo Gavazzi)

- Generic (Danfoss case / pack controllers)

- AK-CM (AK- Communication Modules) Calculations

Each node (type) has a column that reflects any configured or scanned status.

Scan, detect and map

The remaining steps are common with the previous example.

**X-Gate Integration (Southbound - via AK-SM 800A Ethernet channel 1)** The following description focuses on the recommended method to integrate X-Gate on the AK-SM 800A via Ethernet 1 port (using Modus TCP). Before you begin the configuration process, carefully review the following notes:

- Currently the AK-SM 800A supports one X-Gate to integrate field devices (southbound).

- Ensure your System Manager is running minimum of software package 4.2.4 or later.

- Ensure your X-Gate is running the latest software package v5.26 or later.

- Consult the X-Gate user guide for more information – (User Guide) .

- Review information on the Danfoss support web site (X - Gate, Danfoss) .

- Devices connected to the X-Gate must have a corresponding device file installed both the AK-SM800A and X-Gate. Refer to X-Gate user guide to create these device files.

- Load corresponding device EPK files on AK-SM 800A.

- Danfoss recommends configuring the X-Gate using Static IP address.

- Ensure your connected X-Gate on AK-SM 800A via ETH1 port.

**Steps to configure X-Gate on AK-SM 800A** On the AK-SM 800A, via local screen or remote browser, navigate to the **Configuration**  **Comm screen** and ensure Ethernet 1 is enabled (following any adjustment in the comm screen make sure to initialize or reset the unit to ensure setting are adopted by the AK-SM 800A).

- On the AK-SM 800A, via local screen or remote browser, navigate to the **Configuration**  **Network Nodes**  **Node Overview** and select either ’X-Gate Address’ or ’Modbus TCP and X-Gate’

- Select ’Modbus TCP and X-Gate’ if your network has or will have an X-Gate and Danfoss Modbus/TCP controls

- Select ’X-Gate Address’ if only an X-Gate will be present on the Modbus/IP channel.

**Suspend Polling function (Network Nodes)** The new ‘suspend polling’ function can be found in AK-SM 800A release R4.1. It is designed to assist in the commissioning process of generic field bus devices (i.e. Case, Pack controllers), specifically where a previous (offline configured) AK-SM 800A database can be imported to a target (Online) AK-SM 800A unit without concern that the field bus polling will overwrite the original configured settings. This feature is designed for Danfoss field bus devices (e.g. AK-CC55, AK-CC550, etc.) and improves support for using previously configured AK-SM 800A databases for onsite commissioning

Polling is the automatic function of the AK-SM 800A communicating with configured southbound devices, where the AK-SM 800A will retrieve parametric data from the controls (settings/values..) and updates the AK-SM 800A database.

The use case below describes typical usage expectations and how the new suspend polling feature aids in the commissioning process, by improved support for pre-programming on an offline AK-SM 800A unit.

- Ensure ETH1 is selected (recommended).

- Manually enter the IP address for the X-Gate (recommend static IP).

- To speed up network scan it is possible to define a scan range and the address range within this scan. For example, you have x50 BACnet nodes, address 1-50, set Number of X-Gate scan range to 1.

- Enter the low address of the expected device connected to the X-Gate (e.g 1).

- Enter the high address of the expected device connected to the X-Gate (e.g 50).

- Press the “Press for complete rescan” button. Depending on the other channels, the scan can take several minutes.

- Verify successful scanning results, navigate to ConfigurationNetwork NodesScan StatusControllers

- Press the “Details” button (or > on local screen) to see additional information.

After this process, the devices can be configured in the AK-SM 800A according to their application category / type, once EPK files (device files) were loaded on AK-SM 800A.

###### **Use Case**

“As a commissioning Eng I want to pre-program a customer application database via my home/office AK-SM 800A unit. The home/office unit is not physically connected to any devices, however, I still can pre-program as the AK-SM 800A has the built in device files. Of particular interest is the programming of settings for generic filed bus devices (i.e. case controls). After programming settings for the controls, I save the database to USB flash drive. I then travel to site where I expect an AK-SM 800A to be mounted and associated devices available on the southbound network. I expect to update the site AK-SM 800A to the latest firmware and to load my previously saved database. I will expect to perform a network scan (discover the devices) and then to ‘download’ my settings previously made and contained within the database to the live southbound devices”.

###### **Step 1: Home/Office Unit**

1. Disable Generic Device Write Errors (Config  System)

2. Configure 800A unit to match expected site unit configuration/ device settings etc (i.e. Network channels, # of controllers, controller type, controller settings…)

###### **How to use the suspend polling function**

*[Figurtekst: Home/Office Site (Ver. 4.1 and above) · Config  System  Config  Network Nodes  Node Overview · Generic Device Errors = disable (off) Polling Config = suspended]*

- Disable Generic Device Write Errors (Config  System)

- Configure system per site requirements

- Field bus channels, Devices, addresses, device settings

- Main Switch of controllers<sup>1)</sup>

- Force an internal database refresh by soft resetting the unit • (Config  Comm  ’ **Press to reset unit** ’

   - Polling Configuration suspended

   - Load (import) database

   - **Allow unit to complete network scan** (if configured in DB or manually scan to detect devices)

   - Download settings to controllers

   - Resume polling

- Save (export) database to USB

1) The following assumes you have a home/office ‘offline’ 800A where you wish to pre-program device settings, save the DB and load into the site unit.

**Note: Pay special attention to controller main switch state, as this will be reflected in the site unit post download sequence. I.E. if you have the device(s) main switch to OFF then the ‘site unit’ post Download step will keep the device in OFF mode!**

3. To ensure your configuration settings are fully updated to the database, force a database update by initiating a soft reset (re-boot). This can be done via Config  Comm and using the **press to reset unit function (do not power cycle the unit!)**

4. Save 800A DB to USB or .dpk file via remote UI (SvW / SvB5)

###### **Step 2: Site Unit (Ver. 4.1 and above)**

1. Suspend polling (Configuration  Network Nodes  Node Overview)

2. Import home/office 800A DB (USB/.dpk), unit will reboot as part of this process

3. Network rescan (if set to do so) or manually perform network scan – allow to complete

4. Use download function to ‘push’ settings from configured DB to live devices on field bus

5. After download, resume polling (pop up message will prompt you-local screen only), else after time elapse (45 min) polling will resume automatically.

###### **Feature notes:**

- New suspend function found in Config  Network Nodes  Node Overview screen

- New suspend function set to default as ‘disabled’ (i.e Polling is enabled!)

- Fixed 45 min suspension (unless user stops after popup prompt-local screen only), then auto polling resumes automatically

- Even after initial download of settings a Pop-up message offers the user the ability to re-start polling, the user can decline and make additional setting changes without fear of polling starting (until timer elapses)- thus giving user option to resume polling or not

- All user actions associated with this new function is recorded in Audit trail

- During polling suspension, a persistent (flashing) message is shown to inform the user (local screen)

- **During polling suspension (because the 800A is not retrieving live data from the controllers) alarms will not be able to be processed, nor history collection. Upon polling re-start, alarm conditions from controllers will then function as normal**

- **Always check you application and system configuration prior to leaving site, ensuring alarms and full communication to all devices are active**

##### **5.9 Conf i** **guration**  **History**

Your System Manager with SW 5.0.x supports the following History logging capabilities.

|**Polled history points**<br>Points where the System Manager will on a selected timed basis collect and save|3000<sup>(1)</sup>|
|---|---|
|**Event driven history points**|2000|
|Points where the user makes a change to a parameter. Example: Main switch parameter is configured<br>in Event history and will record when the state changes (generic controls only, not IO).||
|**Polled history point frequency**|1,2,5,10,15,30 mins|
|Selectable time intervalsperpoint to be collected|1,2,6,24 hours|
|**Active history database size**|8GB|
|**Archive history database size**|2GB|

(1) It may not be possible to log 3000 points at max frequency (1 min) on slow field bus (i.e. Serial Modbus) – in this case the sample rates can be increased.

1. Access History configuration via Configuration → History → Setup 2. Clear History Configuration – use to clear configuration (all history will be cleared) 3. Clear History Log – use this to clear all current history saved (all logs will be deleted) 4. Auto Configure History – see following section (Option 1) 5. Start / Suspend History – after configuration, start History collection or suspend 6. Current status of History service 7. Status – totals of recording points / type 8. Individual History type status - totals

To configure devices and sensors already configured in the System Manager, navigate through the controllers, relays, sensors…list (1).

The Controllers menu (if multiple devices are connected/configured) will show a drop down menu, making it easy to navigate through the controller you wish to set for History (2). Multiple pages containing all the controllers’ parameters will be shown (3).

Review the device parameters and select from the following options

- HACCP – enable point associated with HACCP logging

- Sample rate selection – select required sample rate

**Tip:** Remember to start history collection once all parameters have been selected.

There are several ways to configure history collection based on your specific applications needs. The following section describes these options and assumes the field bus devices are already installed, scanned and communicating with the System Manager(s).

###### **Configuration – Option 1** (Auto Configuration of History)

This feature takes advantage of pre-selected history points in the device file and any configured I/O type points. Each Danfoss controller that has a device file will have pre-selected history points that when used with the ‘Auto Configure’ function will automatically be configured ready for History collection as long as a valid address is assigned. All I/O points will be selected for history collection that have valid addresses.

From the Configuration → History → Setup screen, locate the option for ‘Auto Configure History’. From the associated dropdown selection list, select your preferred same rate (as described in table above). This action will set all valid generic and I/O points for history collection preparation at the sample rate selected.

Press the ‘ **Start History** ’ button to initiate history collection.

**Configuration – Option 2** (manually select required parameters)

This option allows full control as to what datapoints are selected for history collection and at what frequency.

**Tip:** This option can also be used to ‘fine tune’ by add/remove/ change sample rate of data collection points defined in Option 1.

From the Configuration → History → Controllers Menu, select each controller and via the associated pages, enable / select frequency sample rate.

Press the ‘ **Start History** ’ button to initiate history collection (History Setup page).

###### **Configuration – Option 3 (copy wizard)**

Using this option allows you to configure not only the device settings, alarms but also History. The Copy wizard can be used in a ‘live’ setup where you have direct access to the field bus devices and for all same type / firmware version devices will copy settings to your selected targets. Alternatively, you can define a controller reference template and save as a file – later to be used for any same time device for copy.

From the Configuration → Quick Setup menu, select the Copy wizard. Follow the Copy wizard steps, including the History configuration and either save as file or copy to x selected devices at the end of the wizard.

Press the ‘ **Start History** ’ button to initiate history collection (History Setup page).

###### **Difference in field bus topology**

Different field bus topologies offer different performance characteristics in terms of available collection performance against number of devices. For example, when using TCP based devices over ethernet (i.e. SNMP or Modbus/TCP), a greater number of devices can be sampled at the highest frequency rate because ethernet based communications is faster to respond than serial, meaning more devices can be polled at higher frequency.

This is important to note because even though the System Manager can collect 3000 Polled history points, the performance and assured collection of this amount will be dependent on the field bus and set frequency. The system manager makes some background estimates against the different network topologies (Modbus serial, Ethernet, IO) and based on this assessment may present a warning message ‘ **Warning: Too many history points configured for selected rate** ’.

Upon viewing this message, it is advised to either reduce the number of selected points or amend sample rates to a longer rate.

###### **System Manager History Storage (SW version 5.0.x and above)**

The System Manager stores history in two repositories: Active and Archive.

Navigate to: Configuration → History → Status.

###### **Active Database**

- History is stored in monthly files.

- The memory usage is shown at the top of the Active Status screen.

- When memory nears full capacity, the oldest month is automatically moved to the Archive directory. Two-week countdown until moved.

- Moved files are converted to CSV format and zipped for efficiency.

- All Active data is viewable via the SvW and Local UI history screens and marked as Available.

###### **Archive Database**

- Stores history for long-term monthly compressed files in csv format.

- Data can be viewed by downloading selected files to your PC (SvW only).

- Memory usage is shown at the top of the Archive Status screen.

- Due to compression, many months can be stored before deletion occurs.

- When nearing capacity, the oldest Archive file is deleted. Onemonth countdown until file is removed.

- Recommendation: Periodically check Archive memory and download older files if needed.

###### **Estimated system capacity for storing Polled History datapoints**

Precisely determining the length of time monthly files reside in Active or Archive is difficult as it depends on how many samples points are being collected and at what frequency. However, as a general guideline, and using Option 1 as the reference, we can

take the following use case to explore the expected time stored in the System Manager.

Use Case: (History configuration – Option 1)

Application has max 168 Case Controllers (i.e. AK-CC55 Modbus) with Two Pack Controllers (i.e. AK-PC782AB AK IP).

|**Device**|**Filed Bus**|**Frequency of Log**|**Estimated time in Active**|
|---|---|---|---|
|AK-CC55 x 168|Modbus (serial)|1 min|~2 Months before being transitioned to Archive|
|AK-PC782AB x2|AK IP||directory|
|Total Polled points 1,200||||

Decreasing the frequency of history collection (i.e. from 1 min to 5min), will increase the amount of time (months) the files will remain in the Active directory, the above example is a ‘worse’ case using the Option 1 method.

###### **Operational Notes for History function when upgrading to SW 5.0.x**

System Manager SW 5.0.x has an updated history architecture compared to previous releases, please be aware of the following notes when upgrading from older SW versions.

- After installing SW 5.0.x the System Manager will ‘parse’ (analyze) the old history and convert it to the new format / architecture

- Depending on original History configuration (how many points and at what frequency) it may take some hours for this parsing to complete – this is expected and system control will continue as normal.

- **During this time, it is not recommended to reset / reboot your System Manager. During the parsing / analyses period the System Manager will allow max 3 resets – any more than that (i.e. upon the 4**<sup>**th**</sup> **reset) all history that has not been already converted to the new format will be deleted.**

##### **5.10 Food Safety Logging (HACCP)**

From software release V9.000.15x and above, the AK-SM 800A offers a special logging function that can facilitate food safety reports.

**Note:** that the functionality now included in your AK-SM 800A does not replace enterprise advanced logging and reporting available via Danfoss digital services (Alsense™). Highlights of the new System Manager feature are shown below:

- Designed for individual System Manager logging only (for multiunit, multi-site / Enterprise data collection and view please consider Danfoss digital services - Alsense™)

- Manually select history datapoints and tag as ‘HACCP’

- Any available parameter can be selected for HACCP logging (but typical use case is cabinet air temperature or product sensor)

- Danfoss I/O points and Generic devices (de-centralized field bus controls) supported

- Where available (device dependent) the HACCP report will automatically capture defrost status

- HACCP tagged points will be secured in the System Manager for 18 months before being overridden

- Report generation for stored data on tagged HACCP points accessible via local screen and browser

- Ability to export daily HACCP report (csv from local screen, PDF from browser)

- Ability to configure scheduled daily e-mail export (CSV attached)

- Ability to export (csv) HACCP report from local screen USB

- 200 history points are available for HACCP logging and fixed at 15 min. sample rates

- Configuration supported in Copy Wizard

- The same datapoint can be selected for both service logging and HACCP (note if same point is double configured, only service log frequency will be seen in main history view)

###### **Configuring your System Manager for Food Safety Logging**

**Note:** this can be performed on local touch screen or browser. For typical food safety monitoring it is recommended to select only 1 designated sensor per asset or control device (for example S6 on a Danfoss Evap controller).

- Log on with supervisor level access

- Navigate to Configuration → History

- Navigate to your required control device that has available sensors (in this example a Danfoss Case controller)

- Select your chosen HACCP point by enabling the HACCP line (factory set for 15 min sample)

- If required, the same point can also be select for ‘service logs’ – here select your frequency

- Continue with all other devices that are configured and available – note that the copy wizard (available in browser) can be used to simplify this task if there are multiple same type devices configured

- Return to the Configuration → History Setup screen and ensure logging is enabled. This screen will also reflect how many HACCP points have been tagged (enabled) and how many service log points

**Configuring a schedule for your HACCP reports – e-mail export** Your System Manager has the ability to automatically export daily HACCP reports via e-mail at a scheduled time (or on demand ‘now’)

- Navigate to the Configuration → History → Other screen and select Schedule HACCP Report

- Configure e-mail (see section 5.6 for information on e-mail configuration)

- Under the ‘Schedule Report’ section you may send a report ‘now’ or configure a schedule. If selecting a schedule, the daily time and day(s) can be selected

**Note:** Via the ‘HACCP Email Log’ menu a view of successful (or not) e-mail transmissions can be seen.

###### **Viewing options for configured HACCP reports**

After successfully configuring your System Manager for HACCP logging and after at least 24 hrs of data collection, you have different options to view and export.

###### **a. Viewing HACCP report via browser**

Via the utilities button, select HACCP. By default, the prior 24 hrs period to the current date will be retrieved and presented, as HACCP logs are daily reports only.

The HACCP report consists of 24 hrs shown in 1-hour increments (0-23) and will list all configured assets on the left vertical column. If the system manager detected a defrost input in association with the asset a Y / N will be shown (representing Yes or No), else n/a is shown. Each hour will display a value, which is the average of 4 samples for that hour. If a defrost state is detected at any of these 4 samples the asset will show Y for that hour.

**Note:** The selected sample rate for the ‘service logs’ point does not affect the predefined 15 min. sample rate of HACCP logging.

- There is a max. of 200 history points reserved for HACCP logging, a warning message will pop up if more than 200 points are attempted

There is a date picker and an export button at the top of the report screen. The export button will allow the creation of a PDF, which is downloaded to your browser downloads folder. Numbered pages will be shown at the bottom of the screen, allowing the navigation though all the assets.

**Note:** for large systems with many sample points it can take several seconds to build this report, this is normal, and a spinning circle is shown during this ‘compiling time’.

###### **b. Viewing HACCP report via Local Touch screen**

Using the same principle and process as previously described, the HACCP report can also be seen via the touch screen. Via the utilities menu selector (9 dot menu button), a HACCP button can be seen. As in the browser, a date selector and report can be found, with the export button allowing CSV file export to USB Flash Drive.

**Note:** Via the USB flash drive main menu you also have access to HACCP data (fixed at previous days log collection).

##### **5.11 AK -** **SM 800A Host Network Conf i** **guration**

The following section describes how to configure your AK-SM 800A to facilitate a host network. The AK-SM 800A host network can support up to a max of 10 interconnected AK-SM 800A units. The practice of interconnecting on a host network allows for support of larger applications or to separate discrete control applications onto dedicated AK-SM 800A units. For example, HVAC and Refrigeration control could be done via dedicated AK-SM 800A units. The host network requires an IP Ethernet connection to each AK-SM 800A unit. Once configured all AK-SM 800A units can be viewed in a consolidated format via a web browser.

**Note:** Ensure a common user / password is applied to all units in the host network. A consolidation view is only available via SvB5, not local screens.

###### **Primary device configuration**

Make sure you have suitable fixed IP or DHCP addresses for each of your AK-SM 800A units you wish to deploy on the host network. Also ensure all Ethernet cables are connected.

Make sure the rotary address switch (located behind cover plate) is set to 0 (Zero), which will define your AK-SM 800A as the Primary node on the host network.

**Note:** Do not mix legacy System Manager 800 units on the same host network as System Manager 800A. These different unit types are not compatible and require separate host networks.

Navigate to the Configuration/Comm screen and check your unit has a valid Primary IP address. Set the ‘Host Network’ question to Enabled. Enter the number of System Manager units you intend to have on the host network.

After all changes are complete reset the Primary AK-SM 800A unit.

##### **5.12 Secondary device conf i** **guration**

Make sure the rotary address switch (located behind cover plate) is set to the appropriate number. For example, setting the switch to 1, will define the unit as a Secondary device address 1. All units in the host network must have unique host network addresses (address 0 is always Primary).

Once you have set the rotary address switch, reset the unit and allow the AK-SM 800A to boot up. Navigate to the Configuration/ Comm screen and check your unit shows the Primary IP address.

Set the ‘Host Network’ slider to Enabled. Enter the number of System Manager units you intend to have on the host network (matching what you have already set in the Primary unit)

Make sure the Secondary unit has a valid IP address.

To validate the host network has been correctly configured and all System Managers can see each other refer to the Network status screen. Here you should see all AK-SM 800A on the host network via the local screen slide in menu, select ‘Ethernet’.

##### **5.13 Device Upload / Download**

###### **When to use Upload / Download function**

Understanding the concept of these difference methods will help in determining the use of the Upload or Download feature. Upload = Retrieve field bus controller device settings and sync with AK-SM 800A database Download = Send controller device settings held in the SM800A to the field bus controller.

The **UPLOAD** function is used to ‘retrieve’ or ‘pull back’ control device settings and update the SM800A database. Once the upload is performed and completed any subsequent device setpoint changes done via the SM800A will get immediately sent to the field device (no need to perform upload/download)

Example for Upload: A legacy Danfoss front end controller (i.e. AK-SC255) is to be replaced by the AK-SM 800A. The application has multiple field bus controllers, for example EKC-CC550 evap controller. Upon installing the AK-SM 800A to the established control network and completing a network scan an upload function is performed. This upload function will sync the AK-SM 800A database with the settings that exist in the field bus control devices. Once the upload is complete the contractor can continue to configure via the AK-SM 800A and change settings in the control devices.

The **DOWNLOAD** function is used to ‘push’ control device settings from the SM800A database to the field bus controller(s).

Example for Download: A contractor is planning a visit where a new AK-SM 800A will be installed with new field bus controllers. To save time on site, the contractor (who has access to the new AK-SM 800A) pre-programs the devices in the AK-SM 800A. Upon visiting the site, the AK-SM 800A is mounted and powered up. After a successful network scan (that matches the previously configuration) the contractor uses the download function to ‘push’ the settings from the AK-SM 800A to all the selected nodes on the field bus.

##### **5.14 Device Management (Conf i** **guration/ System/Device Management)**

The purpose of the Device Management feature is to control the amount of active device files at any given time in the AK-SM00A, thus conserving system memory resources.

By default, the most common controller types are set to ‘Enabled’. Groups which are not enabled (Disabled) are not actively loaded into system RAM. To enable any controller group simply slide the selection switch on for the group required

As device files are Enabled / Disabled the file counter will reflect the total number of active device files (seen in the Device Files menu). The term ‘Files’ in this case, is actually the total number of device selections available. For example, a controller such as an AK-CC 550 has 10 different applications. Therefore, each application is a ‘selection’. Then the number of selections is multiplied over several software versions that may be available for that device.

This means that once the controller selection reaches 1000, you will need to disable groups of those devices not being used, in order to keep this number at, or below 1000. A message will be presented to alert if the capacity has been reached.

Make sure to always disable all device groups that are not in use. When performing a re-scan, device groups are activated automatically if any devices within the groups are detected.

Using the network scan or Refrigeration layout/scan wizard will automatically enable any group is detected on a scan (even if the device file was previously set to ‘disabled’).

EDF’s not packaged within the AK-SM 800A will be available via the Danfoss Support web sit e http://www.ak - sm800a.danfoss.com. When installing the latest AK-SM 800A firmware package, recently released / new EDF device files may not be included.

##### **6. Master Control Functions**

###### **(Energy saving features, scheduling and load shedding configuration)**

This section will discuss rail heat control, schedules, HVAC, and lighting. Please refer to this section when configuring more advanced areas of your AK-SM.

##### **6.1 Rail Heat**

The AK-SM can be used to manage the energy output to the case trim heaters (Rail Heat). There are different ways to approach the solution to rail heat control, listed below are three main possibilities.

**1. Use a Night Setback Schedule**

From the Control screen navigate to Refrigeration then Rail Heat (Configuration  Refrigeration  Rail Heat).

   - Many Danfoss controls have a function whereby the output to the rail heat elements can be pulsed in a percentage of time ratio. If set in the controller, the night setback signal from the AK-SM will allow the controller to vary the output depending on the time period. Consult specific controller manual for more details.

**2. Use AK I/O relays to control rail heater connections** (using ‘Calculated’ or physical Dew point)

   - By means of utilizing temperature and relative humidity sensors the AK-SM can calculate the relative Dew point. Based on this Dew point reference and against a set point the output to the rail heat elements can be controlled. This represents ‘tighter’ control based on the calculated Dew point.

**3. Use Adaptive Rail heat control**

   - Adaptive rail heat is a feature that groups together a collection of compatible evaporator controllers that receive signals of the current calculated dew point from an installed dew point / temperature sensor. The installed humidity / temperature sensor connects to the AK-SM (via I/O) and the resulting calculated dew point value is sent to the connected evaporator controllers.

###### **AK I/O relay method**

Select ‘No’ to the question line ‘Use Adaptive Rail heat’. Define how many relays will be used in the control of the rail heat elements (max 30).

Cycle time: Used to determine what amount of time the relays are energized, used in combination with the output percentage as set in the Dew point setpoint.

Dewpoint method:

- Calculated dewpoint (Using a combined temperature / humidity sensor - type: EMHS3-1 is recommended. See below for wiring example)

- Dewpoint (Utilize direct output from dewpoint sensor)

Selecting Use HVAC humidity to “yes” Rail heat dew point will be calculated using Rail Temp and Inside RH sensor inputs. A Rail hum point will not be generated by the SM800.

Selecting Use HVAC humidity to “no” Rail heat dew point will be calculated using Rail Temp and Rail hum sensor inputs.

*[Figurtekst: BACK PLATE · ORANGE - Temp Out (1K PT Therm) · GREEN - Humidity Out (0 – 5 V DC) · BLACK - Ground · RED - 12 V DC* · Power (4-20 Send) Common RH Out (4-20 Return) T Out (4-20 Return) RTDV Override RTDV Override Slider Right Slider Wiper Slider Left]*

*[Figurtekst: EMHS -3-1 Humidity Sensor (combined Humidity & Temperature): · 12 V / 24 V supply via I/O modules · 0 – 5V Relative Humidity · Temperature Sensor]*

Example: With a Dew point target range of -4.0 – 8.0 °C and the Cycle time set for 10 minutes the following behavior will be true. At -4.0 °C : Dewpoint the relay output will be 0% At 8.0 °C : Dewpoint the relay output will be 100% At 2.0 °C : Dewpoint the relay output will be 50% of the cycle time (5 mins on, 5 mins off)

At 7.0 °C : Dewpoint the relay output will be 90% of the cycle time (9 mins on, 1 min off)

*[Figurtekst: 8.0 Example of Target Dewpoint & relay output % ratio · 7.0 · 2.0 · -4.0 · 0% 50% 90% 100% · (5 mins on) (9 mins on) · (0 mins) (5 mins off) (1 min off) · Relay output percentage (based on cycle time setting) · Target Dewpoint Ran ge]*

###### **Adaptive method (with compatible Danfoss evaporator controllers)**

Adaptive rail heat is a feature that groups together a collection of compatible evaporator controllers that receive signals of the current calculated dew point from an installed dew point / temperature sensor. The installed humidity / temperature sensor connects to the AK-SM (via I/O) and the resulting calculated dew point value is sent to the connected evaporator controllers. By controlling rail heat according to the actual dew point measured in the store, significant energy savings can be achieved. The following section highlights how to configure active rail heat via the Danfoss AK-CC 550 evaporator controller (which has the ability to utilize calculated dew point over the communications bus). Select ‘Yes’ to the question line ‘Use Adaptive Rail heat’, and (in this example) select ‘Calculated Dewpoint’ as the dewpoint method. Upon answering these questions the AK-SM will automatically build sensor points to allow for the humidity and temperature sensors to be defined. As the diagram below shows, the EMHS31 sensor has humidity and temperature wired in to an AK I/O module, the points at which these sensors are connected can then be added under the sensor page (Configuration  Control  Refrigeration-Addresses).

When using the EMHS3-1 sensor the humidity & temperature output will be connected to AK I/O. Use the ‘Addresses’ tab to locate the sensor sub- tab, where the appropriate board & point can be set (in line with the physical connections on the AK I/O).

*[Figurtekst: 01-1.3 · 01-1.4 · AK I/O modules · EMHS3-1 Humidity & · Temperature sensor · Controller bus · Calculated Dew point sent to · controllers on bus · Rail Heat Relay · Rail Heat Relay]*

For adaptive rail heat to function correctly ensure the AK-CC 550 controllers are set correctly. Review parameters o85, o86 and o87, as noted below. The screen image below highlights the AK-CC 550 controller (Miscellaneous menu), where parameter o85, o86 and o87 are set for rail heat control over the bus.

##### **6.2 Schedules**

(used in combination with Danfoss controllers)

###### **Configuration**  **Control**  **Refrigeration**  **Schedules**

Under the schedules section multiple schedules can be added and configured according to your needs.

Enter the number of schedules required. The desired number of schedules will be shown (in this example 3 schedules have been requested). Initially each new schedule is set to disabled, move the cursor to the required schedule line and press ‘Enter’. The resulting page allows the definition of the schedule, the following configuration settings can be made:

**Rail heat settings in the AK-CC550 o85** = Rail heat control

(select option 2, pulse control with dew point function) **o86** = Dew Point MIN limit **o87** = Dew point Max limit

At a dew point which is equal to or lower than the value in 086, the effect will be the value indicated in o88. In the area between the two dew point values the controller will manage the power to the rail heat.

*[Figurtekst: Rail cycle % · 100% · O88 Rail Min ON % · Dewpoint °C · O86 DewP min lim O87 DewP max lim]*

- Enable this schedule (ensure this is set to ‘YES’ to engage schedule)

- Schedule usage (Choose from Case Lighting, Night Setback, Shutdown, Defrost, Coord Defrost)

- Description (Add custom description for schedule)

- Schedule control (Choose between Time, Digital, Time & Digital, Time or Digital)

- Number of schedules (select the number of sub schedules required)

- Start, Stop, Days and Holidays (Define the Start / Stop times, days and holidays)

Each schedule line will also reflect the current status False = schedule not active True = schedule is active Disabled = Not Active (Enable in schedule setup page)

The example screen below highlights the different areas of schedule configuration, in this example the (Case Lights) schedule has been set to start at 04:00AM until 01:00AM based on Time [AKSM time] or a Digital Input.

For this example the Digital Input had already been defined under the Miscellaneous ON/OFF section, using AK I/O input **01-1.1** . The schedule will now become true (ON) if either the Digital switch is made OR the Time falls between the set Start / Stop times.

The example also has active schedule days seen as -MTWRFA. Sunday (S) has been deselected (-) therefore the schedule is only relevant Monday  Saturday. i.e. S= Sunday, M=Monday, T=Tuesday, W=Wednesday, R=Thursday, F=Friday, A=Saturday.

After the schedule has been created the associated circuit [Evap] controllers must be selected - do this via the **Controllers** tab.

**Note:** A start / stop time of 12:00AM - 12:00AM = always ON

Navigate to the **Controllers** tab and any configured evaporator controllers will be listed (if no controllers are listed make sure the appropriate controller type is set, as defined in the main control page). Navigate to the required controller and double click the relevant line. This will toggle the controller ‘Selected’ or ‘Not Selected’. Any controller set as ‘Selected’ will become part of the schedule.

Once all configuration of the schedule is complete, navigate back to the Schedules tab & select ‘Enable this schedule’ to **YES** .

For test or commissioning purpose or use of groups outside of the programmed interval it’s possible to override the schedule. In case this feature is needed, go to **Configuration**  **Control**  **Refrigeration**  **Schedules** and double click in the selected schedule on the line “Press to turn on”

The status is changing from Auto to manual on. **Note:** It is not possible to turn off and the feature is only available for defrost and not for setback, shutdown or other features.

To associate controllers with the schedule, use the Controllers tab.

Set to YES to enable schedule.

Press the enter key to select the pre-defined ON/OFF input.

Use the ‘Enter’ key to select or not select any controller(s).

##### **6.3 Customized control**

Select the Customized Control Schedule to allow your AK-SM 800A to trigger on/off events based on user configured control trigger such as a time schedule and/or a digital input. The Customized Control Schedule is designed to switch a specific controller parameter to establish certain run conditions (only one parameter selection per control device must be selected). For example, a master control parameter may be toggled for control purposes. The customized control schedule can be used to control (on=1/ off=0) parameter, based on demand (digital input).

In the example below, the user defines a Danfoss AK I/O point as the digital input ‘source’ and selects the required control parameter via the ‘select device parameter’ question. As an option, an alarm or alert can be configured upon schedule activation or on schedule de-activation (Invert alarm option). An alarm action may be selected as well.

On the associated tab called ‘Controllers’, those controllers which hold the selected On/Off device parameter can be selected. Unselect those controllers that should not be included in the customized control.

When the digital input is active, the AK-SM 800A will broadcast the value ‘1’ to the selected controller(s), as defined in the ‘Select device parameter’ line and on the ‘Controllers’ tab. When the input signal is de-active, the AK-SM 800A broadcasts the value ‘0 to the controller parameters – thus toggling on/off the selected parameter. With the setting ‘Master Control mode’ set to ‘Enabled’, the parameter value is re-regularly broadcasted. Disabling this feature prevents re-broadcasting more than 1 time even when the trigger state condition remains ‘True’.

**Note:** A customized control schedule is designed to action on one parameter only. It is not possible to use multiple customized control schedules on the same target controller. It is possible to define one customized control and only controllers of the same EDF file type may be selected. Since the customized control may interact with a large network of field bus devices, appropriate time must be allowed for the customized control to respond to a state change in the selected Schedule control parameter. By setting Default to ‘On’ the schedule function will continue to broadcast the value ‘1’ in case communication to the digital input is lost. If communication the digital input is lost with the ‘Default’ set to ‘Off’ the schedule function stops broadcasting to the controllers.

##### **6.4 Suction Pressure Optimization**

The Adaptive Suction Pressure function in your AK-SM makes it possible to automatically optimize the suction pressure so that it will be adapted to the systems actual load. During optimization, data is collected that tells the system which refrigeration appliances are most heavily loaded. This energy saving function can make substantial savings directly whilst also saving on compressor wear and tear and also providing an analysis tool for refrigeration appliances.

The individual controllers handle the temperature control in the refrigeration appliances. The load and operating conditions of each are continuously collected by the AK-SM via the data communication system. The collected data is computed and the “most heavily loaded” refrigeration points are identified.

An adaptation can now be made of the Suction Pressure, whilst ensuring the air temperature at the refrigeration appliance is maintained. It is the AK-SM that collects data from the refrigeration appliances and it is the AK-SM that transmits any offset to the compressor pack control so that suction pressure reference is changed to suit the needs of the “most heavily loaded” refrigeration point. It is always the temperature at the appliance that takes top priority and in fact the suction pressure can float down if necessary.

The time during which a refrigeration point has been designated “the most heavily loaded” will be summed up in the log (history) within the AK-SM.

The pack suction (Po) pressure is optimized in accordance with the current refrigeration demand, taking into account shortterm changes (day/night setback/defrost) and long-term effects (seasonal/weather changes).

In order to get the best efficiency out of the Po Optimization function it is highly recommended that a plant survey is done before enabling this function. A poorly running site will not be corrected by Po Optimization and the maximum benefits will not be seen - ensure all plant & evaporator cases are running close to

their designed setpoints and that defrost are operating correctly. Also ensure any manual plant override systems are set accordingly to allow the floating up of suction pressure.

It is highly recommended to always use the latest firmware available a t AK - SM 800A Series.

###### **Theory of operation**

The Po Optimize function uses a calculation on all controllers to determine a “Load Factor”. This has been developed by Danfoss and is available in your AK-SM. By use of the Load Factor the Most Loaded Case (MLC) is constantly updated. Floating of the Suction Setpoint is then determined at any given time by the MLC

1. The AK-SM continuously receives operating information from each (Po enabled) controller connected on the network. The AK-SM is looking for the ‘Most loaded case’ (MLC). Each evaporator is analyzed to see if it’s current operating temperature is within a calculated MLC ‘target window’. During defrost and including after defrost recovery, the Po Optimization will temporarily remove the case from the Po calculation loop. This ensures that normal system fluctuations (due to defrost etc) do not effect the overall operation of Po Optimization.

2. In effect the continuous Po Optimization is looking for the evaporator that is under the heaviest load (the one that has to work the hardest to maintain temperature), but still falls within the MLC target ‘window’

3. Based on the MLC the Po optimization function will then send a control signal to the Pack controller to optimize the running suction pressure, i.e. float the pressure up (based on the max limit set in the Pack configuration page). As the Pack controller allows the suction pressure to increase the AK-SM monitors the complete network and ensures that the refrigerating system as a whole is stable. This then is a continuous function that once set runs automatically and ensures the refrigeration system is running to the best conditions.

*[Figurtekst: � Get Case Control Data AK-SM 800A · � Identify Critical Case · � Optimize Pack Po  This feature is available on all supported · AK-SM Evap & Pack controllers. · Pack Control · � · Po · Pc · � · Evap Control �]*

##### **6.5 Conf i** **guration of suction optimization**

Assuming a pack and evaporator suction group has already been defined, go to the Pack controller configuration screen. Locate the line ‘suction optimization’ and set to ‘yes’.

**Note:** The settings may vary depending on the configured Pack Controller.

This automatically sets all evaporators associated with this suction group to also operate in Po optimization mode. If required, individual evaporator devices can be manually removed from the optimization loop under the individual evaporator configuration screens (Detail tab).

- Set an appropriate Maximum float pressure (shown in ‘k’) change that the optimization algorithm can make to the pack controller.

- Enter a post defrost delay (The time period that the Po Optimization algorithm ignores the evaporator device after a defrost. This allows the evaporator to recover from a defrost without effecting the Po Optimization algorithm).

- Define Po stop and alarm conditions (if x controllers enter off line state, then stop optimization)

Once set, the Po optimization operation can be seen under the pack controller screen (optimization tab)- refer to (local screen) examples below.

Enable suction optimization by selecting ‘Yes’. All evap controllers associated with the Pack will then be tagged ‘yes’.

*[Figurtekst: Evap device detail (settings)]*

It is possible to remove any evap controller in the optimization function by selecting ‘No’ in the (evap) device detail (settings) screen.

**Note:** If your AK-SM is configured for degrees C, Suction Optimization is “K”. If set to degrees F Suction Optimization is “F”.

##### **6.6 Adaptive Liquid Management**

The new CO2 Adaptive Liquid Management (CALM) solution allows full utilization of the evaporator surface in display cases and cold rooms, improving energy savings with CO2 refrigeration in any store. CALM is a complete solution: It includes The Liquid Ejector, a compatible Pack Controller, and the Adaptive Liquid Control case controller algorithm. To make best use of your System Manager as a component in a CALM solution, make sure to utilize only compatible Case and Pack controllers manufactured by Danfoss.

*[Figurtekst: AK-SM8XX · ALC Allow ALC · AK-CC AK-CC AK-CC AK-CC Pc]*

To enable automatic CALM control in the AK-SM 800A Series System Manager the Pack controller must be able to determine when to allow liquid control. Similarly, the Case controllers must be able to operate in CALM mode. Please consult your local sales presentative for more details about supported case and pack controllers.

The CALM feature can be enabled by changing the setting ‘Adaptive Liquid Management’ to ‘Yes’. Doing so will continuously monitor the associated Pack controller and distribute the CALM signal to supported Case controllers. It is possible to configure this functionality per suction group if this is supported by the pack controller itself.

It is possible to exclude selected Case controllers from the CALM functionality by navigating to the ‘Circuit configuration’ area and set the “Adaptive Liquid Management’ setting to ‘No’. By default, all supported Case controllers will be set to “Yes” and thereby included in the CALM master control as illustrated in the picture.

In the event that the system does not send or receive correct ‘Allow CALM’ signals in time, the CALM feature is designed to return into normal MSS control meaning disabling the CALM feature in all the configured Case controllers. These situations include:

1. Communication error (Offline) to the Pack controller

2. Pack Controller sends “Liquid Control NOT allowed”

3. Case Controller is configured to “Liquid Control NOT allowed”

4. The Pack controller does not support CALM

5. The Case controller does not support CALM

Should the Case controllers not receive a CALM signal from the System Manager within 15 minutes, the Case controllers will return to normal MSS operation.

**Note:** When the ‘Adaptive Liquid Management’ feature is enabled in the System Manager, it is important that NO custom schedules are configured for utilizing the same master control parameters (‘--- MC. Liq. Ctrl.’, ‘MC Liq.ctrl’ or ‘---Flooding’). Failing to do so could compromise system integrity and result in compressor damage!

##### **6.7 AKC ON (Evap shutdown when injection of f** **)**

One of the main features of the AKC On function is that the SM will detect if there is a pack shutdown condition. The SM does this by monitoring the pack controller for such conditions. If configured to do so, and upon detecting a pack shut down, the SM will issue a signal to all (configured) evap controllers under the pack suction group to close their AKV valves. The effect of closing the local AKV valve is to limit liquid flow in the evaporator. Due to the AKV valve being closed during a pack shutdown period there is a greatly reduced risk of liquid hammer or compressor damage upon pack / compressor start up. The AKC ON function must be configured for each pack suction group. By default, the associated evap controllers are set to ‘yes’ under the selection choice of Evap shutdown when injection off. If a evap controller is not required to be part of the suction group AKC ON function, set this value to ‘No’.

###### **AKC injection ON**

For commissioning, retrofit and filter change mode it is necessary to simulate the signal from pack controller. Means, close valves manually.

In case the menu “Evap shutdown when injection off” a new menu appears in manual operation section, which enables the user to select between injection ON, OFF and AUTO mode.

###### **Evap Configuration**

If the Evap is not required to be part of the AKC ON function, modify the question. Evap shutdown when injection off to ‘No’

**Pack Configuration** Under the settings / Summary screen set the question Evap shutdown when injection off to ‘YES’

**Note:** make sure that the Pack controller has the field Ctrl. Of Injection ON set to Network, for AK2 style devices you may need the Danfoss Service Tool in order to see this parameter

##### **6.8 Coordinated Adaptive Defrost**

Danfoss offers a range of ADAP-KOOL® controllers that have an adaptive defrost function which allows the case controller to skip scheduled defrost cycles that are not necessary to carry out. Adaptive defrost is based on a real time monitoring of the evaporator performance.

By using the electronic expansion valve as a mass flow meter, it is possible to compare the energy balance between the refrigerant side and air side of the evaporator. By means of this comparison, it is possible to calculate the airflow through the evaporator when it is clean.

By monitoring the degrading air flow through the evaporator, it is possible to estimate the ice build-up on the evaporator. In order to calculate the mass flow of the refrigerant, the case controller uses the opening degree of the electronic expansion valve as well as the pressure differential across the valve.

Refrigerated cases are normally defrosted in groups corresponding to how they are placed physically in the store, for instance all case sections of a refrigerated island are defrosted at the same time. If multiple case sections share the same air flow, the defrost cycle must be co-ordinated, so that all case sections start defrost at the same time and start refrigeration when all cases of the group have terminated defrost.

In order to maximize the number of saved defrost, the case controllers have to be grouped into smaller sub-groups of controllers sharing the same air flow. It is more likely that a group of 3 case controllers all are willing to skip defrost compared to a group of 8 case controllers.

The ‘ADAP-KOOL® system’ offers a failsafe procedure that ensures that the refrigerated cases are defrosted in case of error conditions (e.g. lost communication).

###### **Status display**

For each evaporator it is possible to display the current operating status for adaptive defrost:

- 0: OFF Function not activated

- 1: Sensor error state – waiting for sensor OK

- 2: Tuning Function carries out automatic tuning

- 3: OK – no ice build-up

- 4: Slight ice build-up

- 5: Medium ice build-up

- 6: Heavy ice build-up

###### **Supported Danfoss Parameters to enable Adaptive Defrost functionality**

The table below gives an overview of the defrost parameters required for the adaptive defrost start co-ordination. **Before configuring any adaptive defrost scheduling please check that the case controls used in your application are compatible.**

The pack controller provides a filtered value of the condensing pressure Pc converted into saturated temperature Tc. For pack controllers handling trans-critical CO2 systems, the liquid receiver pressure must be distributed to the case controllers. This filtered value of the condensing/liquid receiver temperature is used by the adaptive defrost algorithm in the case controllers.

###### **Automatic adaptation to the evaporator**

When adaptive defrost is activated it will carry out an automatic “tuning” in order to adapt itself to the relevant evaporator. The first tuning takes place after the first defrost so that tuning can be carried out on an evaporator without ice formation. New tuning subsequently takes place after each defrost (but not during night with night blinds using defrost function 2). In a few cases it may happen that the function is not correctly adapted to the relevant evaporator. This is usually because the automatic adjustment has been made under abnormal operating conditions at start-up/ or testing the system. This will result in the function reporting an error state. If this happens, a manual reset of the function should take place while briefly setting the adaptive function switch to “0” (OFF).

##### **7. Advanced features and configurations**

##### **7.1 Managers Override**

#### **Configuration**  **Control**

From the Configuration Control menu select the number of managers override required.

To configure the override, navigate to the ‘Override’ menu tab and follow the below guidelines.

The managers override function allows the authorized user to place Lighting zones and or HVAC units into an override state. The expected implementation for this feature is to provide some mechanical switch in the store managers office or loading bay. The following options can be seen in the configuration of the manager’s override;

###### **Timed Override** (Yes/No)

- YES - The override will last for the time selected in the ‘duration (in Hours)’ line. The point will return to normal operation after this time has elapsed.

- NO - The override will last until it’s switch on the override box is operated a second time

###### **Interrupt enabled** (Yes/No)

- YES - The override can be interrupted by a second operation of the override switch

- NO - The override cannot be interrupted, the point will remain in override status for the duration of the selected time

###### **Bluetooth Interface**

Override for securing wireless BT interface in supported controllers (e.g. AK-CC 55).

Override all zones (Yes/No)

YES - All lighting zones will be overridden

- NO - One or more lighting zone (see details below) will be overridden

Override all units (Yes/No)

YES- All HVAC units will be overridden

NO - One or more HVAC unit (see details below) will be overridden

The ‘Select zones’ and ‘Select units’ buttons appear as needed to let you choose the lighting zones and HVAC units to be overridden. Each will give you a list from which you can select the specific zones or units to be overridden

###### Configuration for ‘Other Unit’ Overrides

If the point to be overridden is on another controller, you must configure a Managers override for that unit. Usually, there will not be an actual override box on the remote unit. Use the same board and point number you used for the actual override box. It is a good idea to make the name of the point the same too. Then make sure to configure the board & point with the same board and point number used for the actual override box, and set the Bcast point to Rec.

###### **Bluetooth® Override**

Some Danfoss controllers provide a Bluetooth communication interface for mobile devices.

###### **Bluetooth® Lock for support devices**

Some controllers provide a Bluetooth® communication interface for mobile devices. To prevent accidental or unauthorized configuration changes to these controllers, the system manager can send out a lock signal continuously on the fieldbus to keep the Bluetooth® interface in the controllers locked. The system manager is able to override the Bluetooth® lock in four different ways:

Use the ‘Managers Override” and the “Addresses” tab to configure a digital input as a Bluetooth® override. This requires an available IO point e.g. via an AK-XM extension module. Use the “Device Access” tab to manually override the Bluetooth® lock and enable automatic unlock when a user logs into the System Manager on the local interface. For both options is it possible to define a timeout which automatically re-engages the Bluetooth® lock in supported controllers.

**Note:** it is not possible to enable both methods at the same time.

1. Manually

2. Automatic at login

3. Digital input (D) override

4. Timeout fallback

##### **7.2 Light**

###### **7.2.1 Lighting Configuration**

###### **Configuration**  **Control**  **LIGHT**

Your AK-SM has the built in ability to support lighting schedules and control via Danfoss I/O modules or via lighting panel communications.

Typically the built in lighting control function is used to manage general store lighting applications. The initial lighting configuration is set out under the Configuration  Control page. The initial control question asks how many lighting zones are required. The AK-SM has the ability to share any indoor photocell configured and to define how many photocells are required. Once these initial control questions have been completed the remaining configuration is done under the Configuration  Control  Light. Lighting control is done via built in AK-SM schedules, and the optional use of photocells. The following section describes a typical lighting configuration, using AK-SM control.

Detailed configuration is done under the Light tab (ConfigurationControlLight).

The initial Lighting configuration is done under the ConfigurationControl page.

Danfoss recommends wiring any lighting circuits in **Normally Closed** position. This will ensure that if power fails to the AK-SM or I/O modules the lighting systems will ‘fail safe’ ‘ON’

###### **AK-SM Built in LIGHTING control (Using AK Input / Output / schedules & Photocells)**

The following control options can be seen in the Lighting tab, navigate and press the enter key to change / configure any relevant points.

**Zone Name:** Custom description (User Def) or select from a drop down list.

**User Defined Name:** Enter required name

**Photocell:** None (no photocell), Inside photocell, Outside photocell or Skylight

###### **Control Sensor**

**Min:** The lowest-reading photocell at any given time will be used as the control sensor.

**Max:** The highest-reading photocell at any given time will be used as the control sensor.

**Average:** All photocells are averaged, and the average value is used as the control sensor value. Photocell ID#1 (etc.): If any specific photocell is selected , its value alone will be used as the control sensor value.

**Num of Schedules:** The number of schedules for this point. **Control Method:** Schd and photo: For this point to be on, two conditions have to be satisfied: (1) the schedule must be true; and (2) the photocell must be above trip level. Once those two conditions are satisfied, the pre-delay timer will start. Schd or photo: For this point to be on, either of two conditions must be satisfied: (1) the schedule must be true; or (2) the photocell must be above trip level. Once one of those two conditions is satisfied, the pre-delay timer will start.

**Tip:** For outside lighting control via photocell, the light level needs to be below the trip level. In the case of interior lighting, turn off lights when we’re above a trip level.

**Num of control relays:** Each zone is controlled by a relay output (digital output) on the I/O network.

**Trip Level %:** The % level at which the photocell condition will be true and act to turn the lights on. (If multiple relays are configured, there will be one trip level per relay.) **Range:** +/- : The range selected creates a dead band.

**Pre Delay:** When lights are off, the number of minutes that the lighting condition must be satisfied before lights will be turned on.

**Post Delay:** When lights are on, the number of minutes that the lighting condition must be false before lights will be turned off.

**Minimum on Time:** When lights are turned on, the number of minutes that they must remain on before being turned off.

**Minimum off Time:** When lights are turned off, the number of minutes that they must remain off before being turned on.

**Override Switch:** (Yes / No) Whether or not there is an override switch assigned to the zone.

**Override Duration:** The duration of an override when the override switch is used.

**Burglar Override:** When this zone’s lights are turned off, whether they are to be turned on when a monitored burglar alarm is sensed.

**Fire Override:** When this zone’s lights are turned off, whether they are to be turned on when a monitored fire alarm is sensed. There is no pre-delay for fire alarms.

**Enable Dimmer output:** Whether or not a dimmer variable output will be controlled.

**Target %:** The photocell level that the controller will seek to maintain by operation of the dimmer. **Minimum output (0.0v):** The minimum dimmer level. **Maximum output (10.0v):** The maximum dimmer level.

###### **Algorithm sensitivity:**

Algorithm interval: Max rate of change (% / Sec):

**Tip:** Target % applies if ‘inside’ or ‘outside’ photocell used. If a skylight photocell used, then the min output/max output (slope between 2 points) approach is enabled.

###### **Schedules:**

Type 1: Standard (directly linked with AK-SC lighting schedule), Relative (a time that is defined before or after the scheduled start / stop times).

Start1: Scheduled Start time Stop 1: Scheduled Stop time Days 1: Days of the week that will apply to this schedule Holidays: Holidays that will apply to this schedule

###### **7.2.2 Addresses**

**Configuration**  **Control**  **Light**  **Addresses** After the relevant Lighting control questions have been configured, appropriate AK I/O addresses need to be applied. The address inputs correspond to the Board & Point address of the AK I/O modules. Depending on the control definition made in the previous (Configuration  Control  Light) screen various inputs will require board & point addresses. Navigate through the Relays, Sensors, On/Off Inputs & variable tabs to define the relevant outputs (Skip the controllers tab as all control is done via AK I/O).

**Tip:** Standard schedule (eg. on / off time 8 am to 10pm)

Navigate through the various control lines, enter custom description & valid address (Board & Point) that reflect the location on the AK I/O network.

Relative means, relative to the open/closed hours. I.E. Open hours are 8 am until 10 pm and a certain lighting zone needs to come on 15 minutes prior to start of open hours until 30 minutes after closing, the schedule would look like the following; -0015 on  +0030 off (so, being relative, the lights are on at 7:45 am and off at 10:30 pm.

###### **7.2.3 Alarms**

**Configuration**  **Control**  **Light**  **Alarms** After the relevant Lighting control questions and appropriate AK I/O addresses have been applied, check the alarms tab. Depending on the Lighting control configuration alarm points will be seen under the alarm tab.

##### **7.3 Dimming control via AK I/O**

The AK-SM 800A offers the ability to dim lighting controls via the use of Danfoss AK I/O dimming systems. The following section describes initial setup and configuration.

From the Configuration menu, navigate to the ‘Control’ screen’. Enter the number of lighting zones required.

From the ConfigurationControl screen navigate to the Light (Lighting) sub tab. The control method setup MUST be ‘ **Schd and photo’** . To use the dimmer night setback option, ensure ‘ **Skylight** ’ is selected.

###### Select Number of control points

Trip level: 2000fc A middle range setpoint. Trip Range +/- : The value added to the trip level to turn Sales Lights OFF and allow them back ON. Trip level of 2000 fc “plus” 200 trip range will turn lights OFF at 2200 fc.

Trip level of 2000 fc “minus” 200 trip range will allow sales lights back ON at 1800 fc.

**Pre delay** : Delay in minutes before the zone can come ON. (Scheduled time)

**Post delay** : Delay in minutes before the zone can be turned OFF. **Minimum ON time** : The time that must elapse once the zone has been turned OFF, before the zone can be turned OFF again. **Minimum OFF time** : The time the zone MUST stay stay OFF before coming back ON.

The ‘Min Out & Max Out’ fields would are interpreted as follows: **Min Out at:** If the skylight sensor indicated a reading greater than or equal to **1800** footcandles (fc), the dimmer would be set to **2%** . ( **Minimum output** ).

###### **Max out at:**

If the skylight sensor indicated a reading at or below **800** fc, the dimmer would be set to **65 % (Maximum output** .) All readings between these 2 extremes would set the dimmer output per the following:

(‘Min out at’ – sensor)

---------------------- x (‘Max. output’ – ‘Min. output’) + ‘Min. output’ (‘Min out at’ – ‘Max out at’)

Thus, a sensor reading of 1200 fc would result in a dimmer output of:

(1800 – 1200) 600

----------------- x (65% - 2%) + 2 % = ------ x 63% + 2% = 39.8% (1800 – 800) 1000

Based on “default” setpoints, the algorithm will work as follows: **Dimming Algorithm Reference Table**

|**Actual foot candle**|**VO%**|
|---|---|
|800|65% (Max)|
|850|62%|
|900|59%|
|950|55%|
|1000|51%|
|1050|49%|
|1100|45%|
|1150|43%|
|1200|40%|
|1250|37%|
|1300|32%|
|1350|30%|
|1400|27%|
|1450|24%|
|1500|20%|
|1550|17%|
|1600|15%|
|1650|11%|
|1700|8%|
|1750|5%|
|1800|2% (Min)|

**Algorithm interval** is the algorithm cycle.

**Max rate of change** is the percentage of adjustment per second. With a setting of 1 % for a 1 second algorithm cycle, and a 2% minimum and 65 % maximum output, the full range can be covered in 63 seconds. (1 percent per second for 63 steps.) This schedule turns the zone ON and OFF on a time base. (Setup for 24 hours).

Once the main configuration screen is complete, navigate to the Variable Outputs tab, where a board and point address can be added for the 0-10 vdc board.

Setup of analog inputs: Skylight sensor to PHOTO-SKY type Dimmer feedback to misc. conversion factor DIM FEEDBK

Once the lighting configuration is complete the details can be seen in the zone lighting detail screen. The detail screen will reflect status, Settings and Service tabs.

*[Figurtekst: Skylight Sensor · MAS/S (5000FC) · AK2LBDD · Ballast · Isolation 24 V DC · Amplifier Power supply]*

##### **7.4 HVAC Conf i** **guration**

###### **Configuration**  **Control**  **HVAC**

The AK-SM 820 and AK-SM 880 both offer HVAC control and support. Both the AK-SM 820 and 880 offer the same HVAC functionality, the only difference is the number of HVAC units that can be configured. HVAC control and support can be via centralized or de-centralized control. Centralized control offers the ability to control HVAC systems via Danfoss AK I/O modules. The de-centralized method allows support for specific field bus nodes.

Initially, navigate to the ‘Configuration Control’ screen, and then declare how many HVAC units you require. In addition to the number of HVAC units, the following questions will also be populated;

### of phase loss monitors

### of humidity sensors

### of dewpoint sensors

The example below describes a typical centralized control method. As seen in the Refrigeration section, the built in HVAC control is based around a list of control questions. When answering these questions, the control inputs / outputs are being built and will be visible in the Address tab. Navigate to the ‘Configuration  Control  HVAC’ screen; here you will need to declare what type of HVAC control method is to be used.

For centralized control, select ‘AHU’ or ‘RTU’ from the drop down list. If you require de-centralized (field bus) control, select the controller type from the drop down list. Once selected use the setup tab to continue configuration. In the example below, AHU has been selected.

**Number of Zone sensors:** The number of zone sensors in the area of the store served by this HVAC unit. **Fan Type** : 1-Speed: The unit has a single-speed fan. 2-Speed: The unit has a two-speed fan.

**Fan control OPEN hours** : Continuous: The fan will run continuously during open hours. Store open hours are defined in the ConfigurationTime tab. On demand: The fan will run on demand during open hours. “On demand” means that the fan will run whenever conditions calling for heating, cooling, dehumidification, or venting are met.

**Fan control CLOSED hours** : Continuous: The fan will run continuously during Closed hours. Store Closed hours are defined in the ConfigurationTime tab (the closed period is from Close time to Open time). On demand: The fan will run on demand during Closed hours. “On demand” means that the fan will run whenever conditions calling for heating, cooling, dehumidification, or venting are met.

**Post delay** : The number of minutes that the fan will run after the last stage of heating, cooling, etc. is turned off. Lockout on proof failure: Yes: The fan will be locked out if fan proof is lost for five minutes. Human intervention will be needed to restart the fan by using the “Clear” button on the status screen. Evidence of the locked out condition, and the means of ending the lockout, are found on the status screen for cooling or heating function. No: The fan will not be locked out on proof failure.

**Monitor Phase Loss** : Whether or not a phase loss monitor will be monitored. Which phase loss monitor: All available phase loss monitors are shown.

**Shutdown on phase loss** : Whether or not the unit is to be shut down when its phase loss detector input is on. Shutdown on digital input: HVAC unit will shut down based on a digital input

**Shutdown on smoke detection** : Whether or not the unit is to be shut down when its smoke detector is on. **Shutdown on fire alarm** : Whether or not the unit is to be shut down when a monitored fire alarm is detected. **No. of return air sensors** : (1-3) **No. of supply air sensors** : (1-3)

###### **Cooling:**

**Num of cooling stages** : (1-3) The number of cooling stages in this HVAC unit. **Proof** : Cooling stage will be monitored for it’s actual run status **Stage x** (where x is either stage 1,2 or 3) **Target** : Enter required target temperature

**Pre Delay** : The number of minutes that must elapse after target plus range is reached before the stage will come on. **Post Delay** : The number of minutes that must elapse after target - range is reached before the stage will be turned off. **Range +/-** : The range selected creates a dead band. For example, if the target is 72 and the range is 2, the stage will come on at 74, and will not be turned off until the temperature reaches 70. **Ambient temp lockout** : Whether or not there is to be a lockout based on low outside ambient temperature. **No Cooling below** : The ambient temperature below which cooling will be locked out.

**Range +/- :** The range selected creates a dead band. For example, if the lockout is 50 and the range is 2, cooling will be locked out at 48 and will be allowed on at 52. **Default fan Speed** : The fan speed for cooling. A different fan speed can be chosen for dehumidification when it is configured.

**Max suction press safety** : Lists every configured pressure sensor. Any may be selected. Only the suction pressure for the cooling compressor in this rooftop should be used. **No cooling above** : The pressure value of the sensor selected on the previous line at and above which cooling will be cut out. Cooling will not cut in again until the pressure falls below this value and the pre delay specified in the HVAC control page.

###### **Freeze protection** :

**Sensor Input** : There is a leaving air temperature for each stage of cooling, near the coil. At and below the setpoint (next line), the cooling stage will be turned off.

**On/Off Input** : A single digital input that when ON will turn off all stages of cooling in the RTU (Roof Top Unit) **None** : There is no freeze protection to configure. **Night Setback** : Whether or not the cooling setpoints are to be raised by an offset (next line) during scheduled times (next page) when cooling requirements are not as critical; for example, when the building is closed.

**Night Setback offset** : The amount by which the cooling setpoint is to be raised when night setback schedules (next page) are in effect. **Num of schedules** : The number of cooling night setback schedules.

**Override switch** : Whether or not there is a switch to override night setback. **Override duration** : The number of minutes after, activation of the override switch, that night setback will be overridden.

###### **Night Setback schedules** :

Type: Standard = based on start / stop times configured in following lines. Relative = based on store schedule with offset time applied Start : Start time Stop: Stop time Holidays: Any holidays, as defined under ConfigurationTime

###### **Heating:**

**Auxiliary Heat type** : None: There is no auxiliary heat. Staging: Auxiliary heat is staged. Gas Valve: Auxiliary heat is regulated by a modulating gas valve, Gas/Staging xxx

Stage x

**Target** : Heating target temperature

**Gas Valve** : Control from: Supply Target: Control gain (% degree): Integral time: Min valve opening: Max valve opening: Low fire position: Low fire duration: Ambient heat lockout: High Supply temp lockout: Fan Speed: Night setback: Night setback offset: Num of schedules: Override switch: Night setback schedules: Dehumidification: ‘None’ or ‘cooling’ (humidity, dewpoint or calculated dewpoint, and related setpoints and delays) Air Damper: If set to ‘yes’ it provides pre-delay, post-delay, ambient air temperature lockout and schedule options

###### **AK-SC Built in HVAC control (Using AK Input / Output)**

Following from the Controllers tab, the Relay, Sensor, On/Off Inputs & Variable Outputs tabs allow the adding of the relevant I/O modules required for built in HVAC. Each line would have been ‘built’ depending on the answers given in the various HVAC setup screens (previously described).

If required, enter unique description. Enter correct address for the Board & Point input. Type can be changed according to the selections in the type drop down list.

###### **HVAC Alarms - Alarms Tab**

The alarms for the individual HVAC unit can be found under the Alarms tab.

Scroll down each appropriate line and press enter to change the alarm level, the available options being the same as found in previous alarm tab configurations. In addition to the alarm level, an alarm action number can be set (1-8), configure the alarm actions in the central alarm routing page (Configuration  Alarms).

**Note:** For alarms to correctly activate, the central alarm routing page must also be configured. See Configuration  Alarms

Define the Alarm Action for each alarm output - this links with the central Alarms  Routing page.

Define the Alarm level (Disabled, Log Only, Normal, Severe, Critical, Delete).

##### **7.5 Miscellaneous Conf i** **guration**

###### **Configuration**  **Control**  **MISC**

The term Miscellaneous refers to the ability to monitor and control miscellaneous areas of an application using Danfoss AK I/O (modules). For example, a miscellaneous relay output may be required for an exhaust fan, a dispenser that adds chemicals, an oven, a produce fogger, or any other device that can’t or shouldn’t be treated like an ordinary refrigeration, HVAC, or lighting asset. Miscellaneous on/off, sensor inputs can be used in defining the control strategy for miscellaneous relay outputs. Any miscellaneous points configured can be monitored for history, and may be configured strictly for that purpose, or for alarms. Routable alarms can be created for any Miscellaneous point. For sensor inputs, the AK-SM allows custom conversion for non-Danfoss sensors that have a linear response (known as Conversion factors)

The initial Miscellaneous definition is set out in the **Configuration**  **Control screen** (see left). In addition to Relay, Sensor, On/Off Inputs and variable outputs the Misc section also has Conversion Factors & Calculations. Further details on conversion factors and calculations can be seen in this section.

Once the required misc points have been set (number required), configuration is done under the **Misc** tab.

In this example a miscellaneous sensor has been configured, but the same principle will apply if configuring Relays, On/Off and variable outputs. Under the Misc tab, navigate to the sensors tab. Enter a suitable description for the sensor, then under the Bd-Pt line, enter the board & point address for the sensor in question. In this example the address 01-1.2 has been assigned. Review the remaining items in the list and configure according to your site requirements.

Example of I/O module line up. The communication module (AK CM 101A) has an address set as 1, with module 1 having the sensor in location 2. This is then entered in the AK-SM as 01-1.2

###### Configuration  Control screen

For this example the board and point address 01-1.2 is assigned

*[Figurtekst: Communication Module 1 Module 2 Up to 9 modules can be connected to · Module (address 1) ONE Communication Module · Sensor (01-1.2) · Rotary address switches]*

###### **Relays Tab**

The example below shows the Misc Relays tab. Navigate down the control lines and configure as required.

**Relay Tab** Depending on control requirements the screen layout may differ. Navigate though the options, adding custom name, AK I/O address, alarms, pre and post delays etc. **Note:** Setting Broadcast to yes will make available the relay status on the AK-SM host network. If a control input is needed to operate your misc relay, this can be selected on the Control Input line (you will need to configure your control input in advance)

If configured, navigate to additional relays via the drop down box

**Name:** Enter custom description for relay

**Minimum Off:** Define a min off time period to stop short cycling **Pre Delay:** Define a pre time delay before the relay activates **Minimum On:** Define a min on time period to stop short cycling **Post Delay:** Define a post time delay to minimize short cycling **Number of alarms:** Enter the amount of alarms (max 3)

**Bd-Pt:** Enter a valid Board & Point address (using AK I/O modules)

**Broadcast:**

**No:** The value of the point will not be broadcast to be used in logic on other controllers.

**Send:** The value of the point (whether it is ON or OFF) will be available on the host network for use by other controllers. Be sure that each sending Board-Point combination is unique throughout the system. (If the controller at address #01 is sending from its Bd-Pt address 1-02, then no other controller can have an output at its Bd-Pt address 1-02 sending.

**Alarm 1:** Enter the alarm level (Disabled, Log only, Normal, Severe, Critical)

**Type:** Alarm if ON, Alarm if OFF, Cycles (enter number of cycles) **Delay:** Enter delay time **Units:** Seconds, Minutes, Hours **From:** Defines alarm output time window **To:** Defines alarm output time window **Days:** Define the days associated with alarm

**Rec** : The value of the point is being received from another controller on the host network. You must enter, in the Bd-Pt fields, the Bd-Pt address of the sending point.

**Action:** Define the alarm action

**Type:** Normally Closed or Normally Open **Control Input:** It is possible to use other defined points (including calculations) to act as the control Input - these will be seen in a drop down list

**Note:** Any Misc points configured in the AK-SM system will be shown in the ‘System View’ under the Power/Misc window

###### **Sensors Tab**

The example below shows the Misc Sensors tab. Navigate down the control lines and configure as required.

**Name:** Enter custom description for sensor

**Bd-Pt:** Enter a valid Board & Point address (using AK I/O modules)

###### **Broadcast:**

- **No:** The value of the point will not be broadcast to be used in logic on other controllers.

**Send:** The value of the point (whether it is ON or OFF) will be available on the host network for use by other controllers. Be sure that each sending Board-Point combination is unique throughout the system. (If the controller at address #01 is sending from its Bd-Pt address 1-02, then no other controller can have an output at its Bd-Pt address 1-02 sending.

**Rec** : The value of the point is being received from another controller on the host network. You must enter, in the Bd-Pt fields, the Bd-Pt address of the sending point.

**Type:** Select from various option in the drop down list (this example uses a PT1000 sensor)

**Control Input:** It is possible to use other defined points (including calculations) to act as the control Input, these will be seen in a drop down list

**Number of alarms:** Enter the amount of alarms (max 3)

**Alarm 1:** Enter the alarm level (Disabled, Log only, Normal, Severe, Critical)

- **Type:** Alarm if above or if below limit (seen below)

**Limit:** Enter the alarm limit

**Delay:** Enter delay time

**Units:** Seconds, Minutes, Hours

**From:** Defines alarm output time window

**To:** Defines alarm output time window

**Days:** Define the days associated with alarm

**Action:** Define the alarm action

**Sensor fail alarms:** Enter the alarm level to issue alarm if sensor fails (Disabled, Log only, Normal, Severe, Critical)

###### **On/Off Tab**

The example below shows the Misc On/Off tab. Navigate down the control lines and configure as required.

**Name:** Enter custom description for Input **Bd-Pt:** Enter a valid Board & Point address (using AK I/O modules)

###### **Broadcast:**

**No:** The value of the point will not be broadcast to be used in logic on other controllers.

**Send:** The value of the point (whether it is ON or OFF) will be available on the host network for use by other controllers. Be sure that each sending Board-Point combination is unique throughout the system. (If the controller at address #01 is sending from its Bd-Pt address 1-02, then no other controller can have an output at its Bd-Pt address 1-02 sending. **Rec** : The value of the point is being received from another controller on the host network. You must enter, in the Bd-Pt fields, the Bd-Pt address of the sending point.

**Type:** Select from various option in the drop down list **Voltage:** Voltage Input **No Voltage:** No Voltage Input **Latching:** Latching Input **Closed:** Closed Input **Open:** Open Input **Number of alarms:** Enter the amount of alarms (max 3) **Alarm 1:** Enter the alarm level (Disabled, Log only, Normal, Severe, Critical)

**Type:** Alarm if above or if below limit (seen below) **Limit:** Enter the alarm limit **Delay:** Enter delay time **Units:** Seconds, Minutes, Hours **From:** Defines alarm output time window **To:** Defines alarm output time window **Days:** Define the days associated with alarm

**Action:** Define the alarm action

###### **Variable outputs**

Using a 0 – 10V water mixing valve application as an example, the following screen can be used on the AK-SM to provide control. The same principles can be applied against a wide range of control needs. Variable output control can also be seen in certain AK-SM Refrigeration, HVAC and Lighting control screens. Using the Miscellaneous area of the AK-SM a variable output point can be created. After authorization, navigate to the **Configuration**  **Control page** . Enter the required quantity of variable outputs, remembering to also add a sensor input (which will be later used as a water temperature reference).

Next, navigate to the Misc tab and scroll to the variable output tab. Enter a descriptive name and the board & point allocation (the point number will be 1 to 4). Define the working voltage

range, here a 0 – 10 V range is set. The previously configured sensor input (water temp) can be defined, along with the output % range and is used as the control reference point.

An override relay or switch can be added if required (not used in this example). Finally an analog output fail safe can be configured. The fail safe feature is to ensure safe operation during power outages, network disturbances etc.

The following options are available;

- Stay unchanged - upon failure keep output voltage unchanged

- Maximum output - set output to 100%

- Minimum output - set output to 0%

- Predefined value - user set value %

**Name:** Enter custom description for Output **Bd-Pt:** Enter a valid Board & Point address. Variable output is done via VO2 board (described opposite) **Range:** Select from various option in the drop down list: 0 – 10, 10 – 0, 0 – 5 Volts **Control Sensor Output 0% Output 100% Override type** (Relay Output, On/Off) **Override point Failsafe Type** (Stay unchanged, Maximum output, Minimum output, predefined value - user definable) **Number of alarms:** Enter the amount of alarms (max 3) **Alarm 1:** Enter the alarm level (Disabled, Log only, Normal, Severe, Critical)

**Type:** Alarm if above or if below limit (seen below) **Limit:** Enter the alarm limit **Delay:** Enter delay time **Units:** Seconds, Minutes, Hours **From:** Defines alarm output time window **To:** Defines alarm output time window **Days:** Define the days associated with alarm **Action:** Define the alarm action

###### **AK-XM 103A Variable Output board**

Your AK-SM fully supports the family of Danfoss I/O modules. The I/O family consists of various analog inputs, digital outputs, and relays. New to the I/O family is the AK-XM 103A (080Z0032) analog input /output module. This new module offers x4 analog inputs and x4 analog outputs, allowing easy control of a variety of control applications.

*[Figurtekst: Terminal 9:  12 V max 100 mA · Terminal 10:  5 V max 25 mA · Terminal 11, 12: · Terminal 2, 4, 6, 8:   GND-AI 1-4 · Terminal 17, 19:   GND-AO 1+2 · Terminal 21, 23:   GND-AO 3+4 · Galvanic isolation: · AI 1-4 ≠ AO 1-2 ≠ AO 3-4]*

###### **Conversion Factors**

Conversion factors are used for sensors that have an output range or range-to-value relationship not already defined as one of the named “types” in the sensor input configuration list box. The following example highlights the Conversion Factor screen.

**No of conversion factors:** Enter the required amount of

conversion factors

**Conv 1:** Name for conversion factor (user changeable) **Units:** Select from a range of unit types:

psi Bar °F % °C ppm (Parts Per million) V (Volts) Amp Kw kWh Hz gpm (gallons per min) fps pH fc lpm (litres per minute) lps (litres per second) Minimum Input: Maximum Input: Minimum output: Maximum output: Lux:

**Conversion Factor Tab** Depending on control requirements the screen layout may differ.

###### **Detail View**

###### **Status**

###### **Settings (see also configuration)**

###### **Service**

###### **Consumption**

The place for the address of the utility meter pulse did not change. Still available here under sensors

|**Parameter**|**Description**|
|---|---|
|Manual defrost start|Used to start a defrost cycle on a case controller. If this parameter is set ON the case controller will always<br>initiate a defrost cycle.<br>(Few exceptions does exist e.g. if Main Switch is set OFF, Defrost control is not Enabled, Case cleaning is<br>ongoing, Case is in shutdown mode, forced closing condition with disabled defrost).|
|MC defrost start|Also a defrost start signal, but this signal will not initiate a defrost cycle if the adaptive defrost function in<br>the case controller allows to skip the scheduled defrost.<br>If the case controller is not set up for adaptive defrost, the signal will initiate a defrost cycle.|
|Request defrost|If the case controller is setup for adaptive defrost skip functionality, this parameter indicates whether the<br>controller will initiate the next scheduled defrost.<br>ON: Case controller will initiate a defrost cycle if the MC defrost start signal is set ON.|
||OFF: Case controller will skip the next defrost cycle if the MC defrost start signal is set ON and the skip<br>defrost counter will count 1 up.|
|Defrost state|Parameter that indicates the actual defrost status of the controller. This parameter is already used by the<br>standard defrost co-ordination function in AK-SM850.|
|Tc mean|Filtered condensing pressure (converted to saturated temperature) read by AK-SM 850 from the associated<br>suction group In pack controller) and distributed/written to the case controllers every 10 minutes. If the<br>signal is not updated every 15 minutes in the case controller, the value will fall back to a default value.|

###### **Methodology of adaptive defrost**

The following section describes the methodology of adaptive defrost.

When the defrost schedule reaches a defrost initiation time the following will happen for **each subgroup of controllers** ;

AK-SM 800A will read if any of the case controllers are requesting a defrost cycle. The “Defrost request” status can be read from all case controllers supporting adaptive defrost with skip.

###### **Exception handling**

If a case is not configured for adaptive defrost or has no adaptive defrost function, it will always execute a defrost, members in the subgroup will also be (forced) into defrost. In this situation, all case controllers must start a defrost cycle. If the defrost request signal cannot be read from one or more case controllers at the time of defrost initiation, AK-SM 800A will start a defrost cycle on all case controllers in the sub-group by setting the “Manual defrost start” parameter ON.

If just one controller requests a defrost cycle, AK-SM 800A will start a defrost cycle on all case controllers of the sub group in question by setting the “Manual defrost start” parameter to ON.

If none of the case controllers are requesting a defrost cycle, AKSM 800A will send a “MC defrost start” signal to the case controllers of the sub group in question. The reason for sending the “MC defrost start” parameter is to enable the case controller to count the number of skipped defrost.

###### **Process diagram**

The diagram below shows the process for defrost initiation for each sub group of controllers.

###### **Coordinated Adaptive Defrost schedule and sub-grouping of controllers**

###### **Setting up an (coordinated) adaptive defrost schedule**

Prior to any defrost schedule configuration, it is required that the relevant case controls are configured to accept adaptive defrost (i.e. set controller d21 AD Mode =4).

Under the Configuration  Control  Refrigeration  Schedules tab, create a new schedule – type Adaptive Defrost.

*[Figurtekst: Defrost schedule · No · Time for · Wait for scheduled start · defrost · Yes · No Read Read the "Request defrost" · defrost request parameter for all controllers · status in the sub group · Yes · No Defrost Is the "Defrost request" signal · request OFF on all controllers => · OFF on all Meaning they all want to skip. · Yes · Send "MC defrost start"I · Send "MC defrost  to all controllers => Only · reason is for the controllers · start" to controllers · to count up no. of skipped · defrost · Wait for · 1 minute · Yes · Check that no controllers have · No Defrost state started defrost cycle. · OFF on all A double check ensuring that · exceptions are handled. · Yes · Send "Man. def. start · signal" to controllersand run standard Defrost start processended - wait for · defrost coordination next scheduled · defrost · on group]*

Selection of adaptive defrost schedule

The next step is to associate select case controllers to the (Adaptive) defrost schedule. Next, group the controllers into sub groups, corresponding to case controllers that share same airflow in the refrigerated cabinets.

The reason for putting controllers into sub groups is to maximize the defrost savings – i.e. 3 controllers are more likely to agree upon skipping a defrost cycle than 8 controllers.

Example:

An island of refrigerated cases consists of totally 8 case sections (evaporators) – 3 case sections on each side and two individual end sections. In this example the user must be able to divide the group of controllers into 4 sub-groups:

Sub group 1: 3 case controllers on one side Subgroup 2: 3 controllers on the other side Subgroup 3: End section Subgroup 4: End section

To support this configuration a master ‘Adaptive Defrost’ schedule is defined, with the controllers then getting grouped together using the sub-group option. This grouping effectively provides the coordination feature so that all cases are in sync during defrost / refrigeration cycles.

*[Figurtekst: Sub group 1 · Sub group 2 · Sub group 4 AK-CC 550 AK-CC 550 Sub group 3]*

###### **Manual defrost**

The user can manually start a defrost at an individual case level (via device detail screen  Manual tab) or a schedule wide command can be performed. To initiate a schedule wide (all controls associated with that particular master defrost schedule) navigate to the schedule screen (Configuration  Control  Refrigeration  Schedules) and double click or press the ‘turn on now’ action line. The status ‘defrost group’ will then be shown under this schedule screen.

##### **7.6 Energy**

###### **Energy Configuration**

###### **Configuration**  **Control**  **ENERGY [Pulse input from meter]**

From the Configuration  Control page, navigate to the **Energy** tab. This example will describe the configuration of a **Pulse** meter type. Choose this ‘type’ if a non supported power meter has a pulse output that can be connected to a pulse AK I/O module (AK-XM 107A).

Under the **Meter Setup** tab the following screen can be seen;

###### **Configuration**  **Control**  **ENERGY**

The AK-SM system can monitor Danfoss-approved energy meters which have a network interface. In addition to the network meter models, pulse inputs can be fed from a wide range of non supported meters to AK I/O pulse boards & thus basic kWh monitoring can be done. Once either a supported meter or pulse input has been configured, the AK-SM can display current electrical status and log data for history purposes. In addition to viewing and recording electrical data, demand limiting can be performed on lighting and HVAC loads.

The AK-SM system can have a max of 80 meters, only **one** of the meters connected to an AK-SM can be used for demand limiting. The following section describes the configuration of Pulse and network meter types, and highlights the demand limiting function.

The Danfoss approved power meters can be seen when selecting meter type under the control question in ConfigurationControl page and are described in the example below.

Detailed configuration is done under the Energy tab (Configuration  Control  Energy)

The initial meter configuration is done under the Configuration  Control page. Define how many Meters are required, then select meter type..

###### Energy meter choices:

**Pulse/Vol** = used to record volume via pulse (set to Liter, Gallon, Cubic meter (m<sup>3</sup> ), Cubik feet (ft<sup>3</sup> )

**Pulse** = Output from meter fed in to AK I/O module **WN Plus** = WattNode + brand meter (supplied by Danfoss). **CG_EM24** AV0, AV5,AV6,AV9 = Carlo Gavazzi EM24 (Note NOT compatible with other MODBUS nodes on network) **VER_EH8035/36** = Veris modbus meter Carlo Gavazzi WM30AV5 is compatible with other MODBUS devices on the same MODBUS network

Meter **Setup** Tab. All meter types can be seen in this window. In this example, pulse meter has been selected.

###### Enter custom name for meter

If using the pulse meter input for demand limiting, answer ‘yes’ to the question ‘use for demand limiting’ See descriptions below for further details.

###### **Name:** Enter custom description for meter

**Window Size:** [Visible only when demand limiting set to yes] The window width is set to 15, 20, or 30 minutes. Every minute, the window “slides” forward so that it always contains the most recent period of time. Each minute the accumulated KW during that minute is recorded.

**Watt-hours per pulse:** Enter relevant value- Watt-hour per pulse

**Collect History:** Select yes to collect history from this meter

**Use for demand limiting:** Whether or not this meter is to be used for demand limiting.

**Normal Load 01 - 24 Hrs:** Enter the upper demand limit you do not wish to exceed for the given hour of the day (defined by each hour line) under normal operating conditions (when using normal power). There is one field for each hour of the day, from 01 to 24.

**Maximum Emergency Load:** Enter the upper demand limit that you do not wish to exceed when the emergency generator is running.

**Start Shedding at:** Enter the percent of maximum load at which you want to start shedding loads.

**Start restoring at:** Enter the percent of maximum load at which you want to start restoring loads which have been shed.

**Enable coupling switch:** In installations where there are two transformers and/or two emergency generators, a coupling switch can be used to connect both loads to one source in case the other source fails.

**Number of normal steps:** The number of steps (levels) which you will allow to be shed under normal conditions.

**Number of emergency steps:** The number of steps (levels) which you will allow to be shed when the emergency generator is running.

###### **Normal:**

**Soft start begin level:** 0 to the number of normal steps set above, up to 10; if 8 normal steps are configured, for example, the upper limit of this entry is 8) This entry specifies the level down to which loads will be turned on when the emergency generator starts. A level will be added each minute unless the specified emergency load for shedding to start is reached. **Couple begin level:** [Visible when coupling switch = yes] Emergency generator control - Enter the upper demand limit you do not wish to exceed for the given hour of the day under normal operating conditions (when using normal power). There is one field for each hour of the day, from 00 to 23. This screen has two pages in order to list all the hours of the day.

###### **Emergency:**

**Soft start begin level:** [Emergency generator control] 0 to the number of emergency steps set above, up to 10; (if 8 emergency steps are configured, for example, the upper limit of this entry is 8) This entry specifies the level down to which loads will be turned on when the emergency generator starts. A level will be added each minute unless the specified emergency load for shedding to start is reached. **Coupling begin level:** [Emergency generator control] Enter the upper demand limit you do not wish to exceed for the given hour of the day under normal operating conditions (when using normal power). There is one field for each hour of the day, from 00 to 23. This screen has two pages in order to list all the hours of the day.

###### Note about soft starts:

The effect of a soft start is to slowly add load to the generator after it starts. If, for instance, soft start begin level is set to 6, when the generator starts only refrigeration loads and loads assigned level 7 through 11 will be on. After one minute, if the load is below the “start shedding at” percentage of maximum emergency load, level 6 will be turned on. After another minute, the same decision will be made for level 5, and so on down to level one. If at any time the load reaches the “start shedding at” percentage, load shedding will begin again until the system reaches the “start restoring at” percentage.

**DEMAND LIMITING TAB** (see dedicated section on Demand Limiting).

**Configuration**  **Control**  **Energy**  **Addresses**

After the relevant Energy control questions have been configured, appropriate AK I/O addresses need to be set for the pulse meter input. The address input corresponds to the Board & Point address of the AK I/O module - **only use module type AK-XM 107A for pulse meter inputs.** Navigate to the **Addresses** Tab (Demand limiting will be shown in later section). Enter appropriate Board & Point location for the pulse input, under the Sensors tab (as shown below).

Enter custom name for pulse input Enter unique Board & Point address. This input address should have the pulse input (via the power meter) connected

A ny Emergency or Coupling Switch (defined in meter setup) will require address configuration.

Add these relevant address’s via the On/Off Input tab

###### **Configuration**  **Control**  **ENERGY [Danfoss Supported Power meter]**

As previously described, the AK-SM offers communication support to the WattNode +, Veris and Carlo Gavazzi EM24 power meters. These meters offer increased parameters that can be viewed and logged in the AK-SM.

**Note-** due to differing baud rate specifications the Carlo Gavazzi power meter should not be connected on the MODBUS channel if an existing network of Danfoss EKC modbus devices is established.

- **WattNode ® + (Continental Control Systems)** meter requires LonWorks® FTT10 interface - Use Danfoss (part #TP78-02) TP78 to FTT10 network bridge to allow correct communications .

- **WattNode ®+ MODBUS (Continental Control Systems)** meter, connects over the AK-SM modbus network

- **Carlo Gavazzi EM24** supported meters have built in MODBUS communications - connect directly to the AK-SM MODBUS port.

- **Veris EH35/36 (Veris Industries®)** MODBUS energy meters

*[Figurtekst: MODBUS Port on AK-SM RS485 / MODBUS Port on · Carlo Gavazzi Meter · GND B+ · DY- A- · DX+ GND · Danfoss80Z8116]*

###### **WattNode Plus (MODBUS power Meters)**

The Wattnode modbus power meter (Danfoss code 080Z2146) is a device which is compatible with other approved modbus devices on the AK-SM 800A network.

*[Figurtekst: AK-SM 800 · Modbus · A+B- Ground · Shield Neutral · L Phase A L · O I · Phase B · A N · D Phase C E]*

The following steps must be followed to ensure correct scan and communications

###### Step 1:

Ensure all devices on the modbus network are connected and have a valid and unique network address. Via the Configuration / Network Nodes screen, perform a network scan, enabling the MODBUS-RS485 - Ensure SLV/ECFan is set to NO.

**Note** : The WattNode MODBUS meter (080Z2146) has the ability to run at 38400 or 19200 baud rates. Out of the box the meter is set to 38400. If there are no SLV devices on the network, perform a network scan without selecting the SLV options. This will allow the AK-SM 800A to scan at the same baud rate and thus the meter will be detected.

If you have SLV devices on the same field bus as the meter you need to first communicate with the meter at 38400, then once scanned you select the SLV option to ‘yes’ and re-scan. This will then set the meter to the slower rate of 19200, the same as the SLV, thus making them compatible on the same field bus.

###### **Danfoss preferred Carlo Gavazzi power meter support EM511 / EM530**

New in release 4.0, the AK-SM 800A supports Carlo Gavazzi EM511 and EM530 power meters. Danfoss ordering information below:

|**Codes**|**Description**|
|---|---|
|080Z2130|3PH energymeter CT 5A RS485|
|080Z2131|1PH energymeter 45A Direct Conn. RS485|
|080Z2132|CTD-2x Bus-Bar current transformer 100A|
|080Z2133|CTD-3x Bus-Bar current transformer 200A|
|080Z2134|CTA-6x split core current transformer 400A|

Both meters are implemented within the SM800A in the same manner as previous Carlo Gavazzi models, with additional aspects described below. EM511 and EM530 are Modbus meters and come factory default as 9600 Baud, No parity and 8 stop bits (9600N8).

###### **Modbus#1: use case example - Danfoss approved devices + new Carlo Gavazzi meters**

The table below is an example where the application has Danfoss EKC based controllers on Modbus#1, and there is a need to include the new Carlo Gavazzi meters also. In this use case the meters must be manually reconfigured for the appropriate Modbus settings – as shown in the table below.

**Modbus#1: use case example – New Carlo Gavazzi meters only** In this use case, only the Carlo Gavazzi meters will be installed on Modbus#1. Using factory defaults for Carlo Gavazzi meter(s) (9600N8) ensure SLV/CSENSE is disable d and no Danfoss devices are connected.

###### **Options when using Modbus Channel 2**

The AK-SM 800A Modbus channel 2 is intended to accommodate devices in addition to Danfoss, adding flexibility on multiple Modbus configurations. Within the Configuration  Network Nodes screen, it is possible to define up to 5 Modbus 2 configurations. Depending on selection it may be necessary to manually adjust Carlo Gavazzi meter Modbus settings. The table below is an example of possible mixing of Modbus devices (higher baud rate device in configuration 1).

|**MODBUS 2**|**Modbus**|**Modbus**|
|---|---|---|
|**Danfoss + other devices**|**settings**|**configuration**|
|Danfoss EKC|38400,E,8|1|
|3<sup>rd</sup>PartyCase controls|19200,N,8|2|
|EM511 / EM530 new|9600,N,8|3|
|Other..||4|
|Other..||5|

|**MODBUS 1**<br>**Danfoss**<br>**approved**<br>**devices only**|**Configuration**<br>**Network**<br>**Nodes -**<br>**SLV Disabled**|**Configuration**<br> **Network**<br>**Nodes -**<br>**SLV Enabled**|**Configuration**<br> **System -**<br>**Control Enabled**|
|---|---|---|---|
|Danfoss EKC|38400,E,8|19200,E,8|n/a|
|EM511 – new<br>EM530 - new|38400, E, 8|19200, E, 8|n/a|

**Note:** there is no need to modify the Danfoss EKC controls as they have an auto baud rate feature.

###### **Carlo Gavazzi ® power meter configuration (used in junction with RS485 AK-SM Model)**

The following section describes the required steps to connect & configure the Carlo Gavazzi EM24xx meter over a Modbus network connection.

Before any configuration can take place, ensure the meter is securely wired, has a valid network address (different from any other nodes on the ‘Controller’ network) and has a baud rate set to 9600- consult the meter manual for specific information on how to set the network address & baud rate. The data format is 1 start bit, 8 data bit, no parity and 1 stop bit.

Once set, ensure correct interconnection to the RS485 modbus port on the AK-SM.

(1) To avoid errors due to the signal reflections or line coupling, it is necessary to terminate the bus at the beginning and at the end (inserting a 120 ohm 1/2W 5% resistor between line B and A in the last instrument and in the Host interface).

(2) The network termination is necessary even in case of point-topoint connection and/or of short distances.

(3) For connections longer than 1200m a signal repeater is necessary.

Once all communication wiring has been set, perform a network scan- details of how to perform network scans can be seen in the Network Nodes Section of this user guide. Ensure MODBUS channel is checked in the Node Overview page.

###### **Configuration**  **Control**  **ENERGY [Danfoss Supported Power meter]**

This example highlights a Danfoss supported meter **WattNode + MODBUS.** Having already defined the power meter as ‘WN Plus/ MB’ under the control page, navigate to the ConfigurationControlEnergy page. Under type, select WattNode MB (MODBUS).

The physical connection to the MODBUS network should keep the polarity (+ terminal should be to the + terminal on the Wattnode)

**Name:** Enter custom description for meter **Amperage:** Select the amperage of the CT’s connected to the Wattnode +. **Collect History:** Select yes to collect history from this meter **Power Update:** Interval to which power is measured. **Energy Update:** The interval over which energy (the integral of power over time) is calculated.

**Reactive Update:** The interval over which reactive components are recalculated.

**Demand Period:** The interval over which demand is calculated. Demand is defined as average power over a specified time interval.

**Demand Subintervals:** The # of divisions of the demand period used when calculating a “rolling demand” using a “sliding window.”

After the relevant Energy control questions have been configured, the meter must have the address correctly configured. To add the WattNode + modbus meter to the AK-SM network, ensure all network wiring is in place and that power has been applied to the WattNode + meter. Navigate to the addresses tab and then enter the same address that is already set in the meter. Perform a network scan to bring the WattNode + meter on line.

Using the drop down list, the WattNode + meter has been selected.

Select the address tab to enter the address which has been assigned in the Wattnode meter (bit switches)

**Note:** Remember to correctly wire and use the appropriate Modbus port on the AK-SM.

##### **7.7 Energy Measurement / Load shed**

###### **Feature Introduction**

A new feature introduced in SM800A version 08.053 and above allows the measurement and subsequent load shedding of electrical loads. This feature allows the consideration of tariff data, which can be then used to load shed equipment associated with a digital input. The use of Danfoss AK-IO modules is required for this feature.

###### **Feature highlights**

- Measuring period synchronization

- 3 Tariffs in kW (High Tariff, Normal Tariff, Strong Tariff)

- Scale factor for current and voltage transformers

- Pulse / unit

###### **Load shed based on**

- Start and stop shed borders

- Shed level

- Min OFF, Pre and Post delay in minutes

- Maximum OFF in seconds

###### **Additional features**

- Preset of counters

- Self-synchronization possibility

- Alarm on load shed limit

- Neutral zone in period

- Reset for average, value yesterday, value last week, kWh, kW or all in one go

###### **Configuration**

Follow the guidelines in this section in order to configure energy measurement and load shed Go to Configuration  Control Change the number of meters (max. 80)

Go to Configuration  ControlEnergy Select Pulse / kW

Go to Tab Setup Select Pulse / unit Give counter a name and fill in all appropriate details

###### **Self sync Period.**

In case the external contact in not working properly, SM800A will synchronize the measuring period internally

###### **Self sync Timeout**

If the last time sync is not a self sync timeout, the SM800A will wait for xx sec, before it will synchronize the measuring period internally

###### **Type of metering**

Conventional way is unit/pulse. The new way is pulse/unit

###### **Sync.mode**

Special: Measuring period synchs on tariff change Normal: Tariff changes after external synch

###### **Pulse/unit**

Pulse meter constant

###### **Scale factor**

Factor, to adapt the pulse meter constant to current and/or voltage transformers.

###### **Preset counter**

Set SM800A kWh to the value of the utility meter. Clear counter will reset the value.

###### **Collect history**

Enable SM800A to collect data for consumption view from this particular meter

###### **Use unit for demand limitation**

Enable SM800A to use this (and only this) meter for load shed.

###### **Start shedding at**

SM800A is constantly calculating the energy which is allowed until the rest of the period without the risk to pass the max. limit. In this example the load shed starts if 90% of the max value is reached

###### **Start restoring at**

SM800A is constantly calculating the energy which is allowed until the rest of the period without the risk to pass the max. limit. If the energy consumption is decreasing and the system is satisfied with the calculation the restoring of the levels starts. In this example the restoring starts if the consumption falls below 85% of the max value.

###### **Alarm if above**

If the system is passing above the limit an alarm will be created. In this example the alarm will be send out if the limit is 50% above the max value.

###### **Maximum level**

The system can handle max 4 levels (priorities) for load shed

###### **Tariff limit HT/NT/ST**

Maximum value in kW

###### **Neutral time**

Time in sec. for the beginning of a period where load shed is inactive

###### **Level time**

Time how long the calculation stays in a level before it goes to next level

###### **Period Peak duration**

Basis time for calculation on the peak

###### **Addressing:**

Go to Tab Addresses and On/Off Inputs to find the addresses for synch and tariffs.

NT does not need an address because it is NT, if it is not HT. If ST is active it doesn’t matter which status NT or HT has.

##### **7.8 Detail**  **Energy**

Under detail  energy the Sm8xx supports following information to the user:

1. Status

   - a. total consumption since start

   - b. Current power in kW

   - c. Peak power in kW

2. Settings (example shows pulse meter)

- a. Name

- b. Window size for demand limit

- c. Pulse rate in Wh/pulse

- d. Collect history (yes or no)

e. Use this meter for demand limitation

###### 3.Service

a. Reset kWh

b. Reset peak

4. Consumption (to present consumption and peak from history) a. View total, monthly, weekly or daily values

- b. Select time frame

- i. Total from/to

ii. previous month and next month

iii. previous week and next week

iv. previous day and next day

In case of total view it is possible to delete history for this particular meter.

##### **7.9 Enterprise Load Shed (via Danfoss EDS Service)**

Your AK-SM has built in functionality to facilitate enterprise demand limiting, via the Danfoss Electronic Delivered Services (EDS) offering.

Contact your local Danfoss sales rep for more details

The term Load Shed in the AK-SM is used to describe a function that allows an enterprise connection to schedule and actively turn off / on configured electrical loads for a period of time.

Once locally configured, your AK-SM can be fully managed via the Danfoss EDS (Electronic Delivered Services). Once logged on, the demand response enterprise dashboard allows retailers to participate in demand response incentive programs via a single, web-based portal. All site configuration, job scheduling, execution, status monitoring, and meter data extraction is completed from one web application.

###### **Configuration**

This section will focus on the local (AK-SM) configuration, and assumes some HVAC and Lighting have been previously configured.

The available load Shed Points ( **HVAC, Lighting Zones, Misc** ) are configured within the AK-SM. From the Configuration/Control/ Energy/Demand Response screen select the **Load Shed** tab. Any previously configured HVAC, Lighting or Misc Relay will be visible.

The example below shows the HVAC and Lighting sections. The two HVAC units are shown and a load shed index of ‘4’ has been entered. The available index range is from 0-4 and once set in the AK-SM is used in the enterprise service to dictate what level of load shed the scheduled job (via the enterprise) will execute. The Lighting tab has been set to load shed level index 3.

###### Why Demand Response?

Participate in demand response programs. Quickly curtail energy usage across your enterprise. Single web portal for all configuration, execution, and utility reporting. For further details, contact your local Danfoss representative.

###### Minimum requirements:

AK-SM version V08_001 or higher of firmware. A connection between customer stores and Danfoss EDS –via VPN connection.

Enter load shed index (0-4)

The power rating slot can be used as a note to what the load is. This has no functional purpose except for notification purposes

Enter a required post delay. This ensures once the load shed event has finished not all system loads will start up at the same time, which could result in electrical overload conditions

###### **Results**

Now the AK-SM has been set for load shed, with the appropriate levels set, the enterprise user can now schedule load shed jobs. Once logged in to the enterprise dashboard the user can select multiple sites and select a time and duration, with a load shed level action.

In our example above, if the enterprise user wishes to reduce maximum load for a period of time, a job would be created in the enterprise dashboard and the index ‘4’ would be issued to all selected AK-SM units across the customers estate. The effect is that ALL applications that have an index of 4 and below will turn off for that period of time (and re-start after any post delays). The result in our example here is that all HVAC and lighting will switch off. Another example would be using the load shed index of 3. This would then only shut down ALL applications set at 3 and below. In this example that would be the Lighting, the HVAC would continue to operate.

##### **7.10  Demand Limiting**

The AK-SM Demand Limiting function is based on a designated utility power meter. Only one meter can be assigned Demand limiting, even though up to 80 meters can be connected to the AK-SM. Once a meter has been selected, the Demand Limit function can be applied against any Lighting and HVAC load.

Utility demand is monitored every minute. Every minute, the most recent **n** minutes are averaged (where **n** is the width of the configured window, 15, 20, or 30 minutes defined in the meter set up window ConfigurationControlEnergy). If the average reaches the configured “start shedding at” percentage of configured maximum demand, Step one (all lighting zones and HVAC units assigned to level 1) will be turned off. After one minute, when the average is calculated again, if the demand is still above the configured percentage of configured maximum demand, level two will be shed, and so on. When demand has dropped to the “start restoring at” level, the last level shed will be restored, and then the others in descending order, so that the last load restored will be the one which was shed first. Restoration will continue as long as the load remains below the “start shedding at” percentage.

###### **Emergency level**

The priority for shedding when the emergency generator is running. If a load is assigned level 0 (zero) for either normal or emergency

conditions, the load will never come on under those conditions.

###### **Configuration**  **Control**  **Energy Demand Limiting**

As previously mentioned the Demand Limiting function is applied against HVAC and Lighting loads. This example assumes that both HVAC and lighting have been defined in the AK-SM and that a meter has been selected for Demand Limiting. Navigate to the Demand Limiting tab. The HVAC and lighting systems will be seen in this page, allowing the configuration of shed levels.

If both normal and emergency load limits are to be established, the relative on/off input for the automatic transfer switch must be wired and configured. In addition, if the site has a coupling switch, you must wire and configure an on/off input for the coupling switch.

###### **Priority Levels (normal conditions)**

Levels are shed in ascending order: level 1, then level 2, and so on up to the highest level configured, limited by the number of steps allowed. Levels above the number of steps configured will not be shed unless the meter configuration is changed (ConfigurationControlEnergy meter setup). Since there are only up to ten steps, loads assigned level 11 will never be shed. It is recommended that loads which are not to be shed are left at level 11, the default value.

Enter the required Shed levels & Emergency levels for the HVAC & Lighting systems.

##### **7.11  Boolean Logic / Calculations**

###### **Calculations**

Miscellaneous calculations are used to create custom logic. The AK-SM has the capacity for a total of 96 calculations which can be used to ‘drive’ miscellaneous logic where special applications are required. There are several ways to formulate calculations for a given requirement, but testing as you go is a ‘must’ in order to confirm desired results. A calculated point created here can be used anywhere a board & point address can be referenced. The calculated points processor is a true boolean processor, with a full complement of argument types and operators. Every configured calculated point will be listed. The fields are as follows:

###### **New Calc**

When first entering the calculations screen a line called New Calc is shown. To configure a new point, double click this field.

###### **Description**

The type of point (OI or SI). If an SI, the description will usually include the units.

###### **Point**

(Ca-01 to Ca-96) The name of the calculated point.

**Value**

The current value or state of the point. This will be on or off for OI points, and a value for SI points.

**Status**

(Online, Offline, Error)

###### Example of Calculations Tab

After adding a new calculation, a default screen will be shown (similar to the example below). The screen is divided into three areas, which from top to bottom are the following:

**Rules area** This is the area that will contain the logical statements that determine whether the point is on or off (OI) or the value (SI) that is used. At the bottom of the area is the current value of the result.

**Heading area** The heading of the screen tells what type and style of calculation point will be created.

**Data definitions area** This area contains information that identifies points that will be used in the logical statements in the next area, and the current value of each. The area by default has lines for two definitions, but it can be enlarged by double clicking the ***Press to insert new line ****. You will see this done in a few pages during the presentation of our first example.

###### **Simple Calculation example:**

Calculate the average of 3 different temperature sensors. Show this resulting average value in a miscellaneous sensor driven by the calculation

**1.** Creating the miscellaneous points for this calculation- Sensor inputs:

Create 3 sensor inputs (the 3rd is used to display the average through the calculation).

##### **8. Device support**

##### **8.1 Danfoss AKC Support (Via AK -** **PI 200)**

The following section describes the configuration of the Protocol Interface -200 (PI-200) in the System Manager. For detailed PI-200 installation instructions and please refer to the PI-200 manual (RS8EX202). The AK-PI 200 is a network device allowing legacy AKC and AKL type controllers to be operated via your System Manager. Any connected DANBUSS controller will be presented similarly to other refrigeration controllers (i.e. LON RS 485 / MODBUS devices).

Note: PI-200 must have firmware 2.25 installed to ensure correct operation and communication with AKC devices and AK-SM 800A.

###### **Important limitations**

*[Figurtekst: Router/switch · PI-200 PI-200 · max. 60 max. 60]*

Up to 60 AKC controllers can be connected to a single AK-PI 200. If there are more than 60 controllers, two AK-PI 200 units must be used. Up to four AK-PI 200 units can be connected to a single System Manager.

The link between the System Manager and the AK-PI 200 is via a TCP/IP. Ensure when connecting your AK-PI200 to the network be sure to use a router or switch, not a network hub. The AK-PI 200 will not function correctly if network hubs are used.

###### **Preparation / Addressing**

Both the System Manager and the AK-PI 200 must have valid addressing set before any configuration can take place. Consider the following steps when setting up your System Manager and PI-200.

1. Ensure System Manager has a valid IP address and is connected on the LAN.

*[Figurtekst: 2 3 2 3 2 3 · 1 4 1 4 1 4 · 0 5 0 5 0 5 · 9 6 9 6 9 6 · 8 7 8 7 8 7 · x 100 x 10 x 1]*

2. Use AK-Service Tool and make direct connection to the PI-200, under IP setup check correct IP address mode (Dynamic/Static), Port Number (default 1041 in PI-200 and System Manager).

3. Set physical Danbuss address for PI-200 by using the rotary address switches on the PI-200. A unique address must be assigned for PI-200, with no duplicate with generic devices on any field bus’.

###### **PI-200 configuration in System Manager (via web wizard)**

The following text will describe the workflow when adding PI-200(s) to your System Manager, including scanning and mapping of AKC devices.

Note: Using the layout wizard assumes no other Refrigeration configuration has been previously performed. Using the wizard on a pre-existing configuration may result in loss of configuration, use manual method described in this user guide.

Under the ‘Configuration’ tab, locate the Refrigeration ‘Layout’ wizard, and start the process, under the network screen select the PI-200 to enabled.

The next screen shows details of the PI-200. If multiple PI-200 units are installed you should select only the PI units which will be associated with the particular System manager.

Follow the remaining wizard screens to format device names and map case to pack controls to form suction ‘groups’.

###### **PI-200 configuration in System Manager (via manual configuration)**

If there are existing devices already on your System Manager you may want to manually add the PI-200 / AKC via the manual method. This section covers how to scan PI-200 and configure the AKC nodes.

1. Via the Configuration Network Nodes tab, select Channel PI-200 (checking correct port address, as previously described)

2. Initiate a network scan by selecting the ‘Press for complete rescan’ line entry

3. Under the Scan Status tab navigate to the PI-200 sub tab, here any detected PI-200 units will be shown and can be selected for use with the System Manager.

4. Under the ‘PI-200 Status’ sub tab you can view the address, version, status, signal quality and number of devices under each PI-200.

5. Once the above process is complete the next step is to define the number of devices you wish to add to the System Manager. Under the Configuration  Control tab enter ‘Number of racks/packs’ and select the relevant Pack controller. Tip! Use the ‘show only scanned devices’ line to only show only the controllers that the System Manager has previously scanned, this will reduce the list of available devices to select from.

6. Navigate to the Refrigeration  Circuits tab to set which case type is to be used

The remaining configuration tasks are already described earlier sections of this user guide.

###### **Presentation of the AKC devices**

Once connected to the PI-200 and configured, the AKC devices will be represented in the same format as any other refrigeration device. The AKC devices will be shown in the main screen dashboard under Refrigeration. Selecting a device will then show the device detail screen, where (if authorized) the user can view and make setpoint changes.

**Note:** The response times over a Danbuss network and via the PI-200 is somewhat slower than traditional LonWorks networking, any delay in retrieving data is not an indication of system fault, but due to Danbuss network performance.

###### **Monitoring Points**

Your AK-SM offers a simple yet effective way to display temperature sensors that also include dedicated alarming and inhibiting functions. The following section describes the configuration of monitoring points and their associated functions.

###### **Adding monitoring points manually**

From the Configuration  Control menu select the required amount of circuits, then navigate to the Refrigeration  Circuits page and under type, select ‘Monitoring’. The selection of ‘Monitoring’ in the drop down selection list offers the user a means to capture, record and display sensors and to present them in the ‘Misc’ section of the home dashboard screen. This method of sensor input is in addition to the miscellaneous sensor inputs used elsewhere in the AK-SM system and can be used to monitor board & point inputs or sensors from connected network controllers (i.e. AKC, AK2, EKC).

Once set to Monitoring navigate to the Setup tab, using the drop down menu to select the recently defined monitoring points.

To setup monitoring points follow the ‘standard’ method in refrigeration configuration - Main Menu / Configuration / Refrigeration / Add Controls. Answer ‘No’ to the question ‘Pack controller required?’ and navigate to the lower section of the screen and describe how many monitoring sensor points are required (still described as No of case controllers.?’)

Click on the Setup button and then select the **Type** drop down list Choose **Monitoring** from the drop down list

###### **Monitor temp input**

Select ‘Yes’ to allow monitoring of a board & point sensor or a sensor via a connected network controller

###### **Defrost Input**

If required a Defrost input can be configured. A Defrost input would be used to effectively inhibit the alarms whilst the equipment was in ‘defrost mode’. Once a Defrost input has been configured it can be used in conjunction with further sensor setups (select Existing option for this)

**No:** No Defrost input required

**Yes:** Define Defrost input **Existing** Pick from previously set Defrost inputs Monitoring setup page

###### **Monitor temp input**

Select ‘Yes’ to allow monitoring of a board & point sensor or a sensor via a connected network controller

###### **Post defrost alarm delay**

Enter the required time delay that the AK-SM 800A will apply after it has detected a defrost has completed - this can stop nuisance alarms

###### **Generate Cleaning input**

Select ‘Yes’ if a cleaning input is required (typical example could be voltage or switch). When the assigned switch is made the monitoring point will detect this change of state and will stop any alarms from being transmitted. After the cleaning input is re-set any future alarms will be transmitted - after any post clean alarm delay timer has elapsed.

###### **Post clean alarm delay**

Enter the required time delay that the AK-SM 800A will apply after it has detected the cleaning input has reset

A custom name can be given to each input. For each input enter the corresponding board & point address for local I/O to enter a controller address (see next section for further details on entering controller address). Finally make sure the type is correctly defined for the input (via a drop down list). Page Down to define any alarms for the inputs. Continue to configure any remaining sensors, once complete you can view the sensors in the Evap Overview list, via the Main Menu. As in the generic format simply click on the sensor to view a summary screen. The detail page for the monitoring point contains current status & temperature, the ability to inhibit (stop alarm from occurring) and alarm settings (if configured).

###### **Additional monitoring of dedicated HACCP sensors**

Using the monitoring feature as previously described, dedicated HACCP sensors can be displayed in the main Dashboard overview screen and subsequently logged for history and alarm limits can be assigned.

Danfoss offers a dedicated HACCP sensor (AK-HS 1000) which is supported by some of the evaporator range of AK-CC controllers. In this example the AK-CC 550 evaporator controller will be used to highlight the required steps to monitor this dedicated HACCP sensor. In the example below an amount of (AK-CC 550) evaporator controllers have been defined and a corresponding amount of monitoring points also defined. Once in the monitoring point configuration screen select ‘yes’ to the question ‘Monitor temp input’. Enter a suitable name for the sensor (Case 1 HACCP in this example) and add the relevant controller network address in the form of 001:1 is controller address 1, 002:1 is controller address2... The principle is that by adding the controllers address in the Bd-Pt box the parameters for that controller become available. The final step is to define the HACCP sensor connected to this AK-CC550 (parameter u56 in this example) -this is done via the drop down list against the Pt# line. Page down to set any alarms associated with this sensor and duplicate for the remaining monitoring points - using the relevant controller address to access the parameter list. The defined HACCP sensors will now be seen in the Evap overview screen and can also be set for history collection.

###### **Monitor digital input**

Select ‘Yes’ to allow monitoring of a digital input via a board & point input or a digital input via a connected network controller

###### **Input configuration**

After selecting ‘Yes’ to any of the questions in the upper part of the monitoring configuration screen the resulting input is shown below.

##### **8.2 Service Tool Support**

Your AK-SM 800A supports the latest Danfoss Service Tool version. It is important to note that this version of the Service Tool supports encryption and authentication, as required by the AK-SM 800A – versions below this will not work.

The Service Tool (CT) must be connected via an IP interface. Once an connection is established the ST will show the AK-SM and all AK2 platform devices. Note that non AK2 platform based devices will not show up in the ST device list.

When creating a new connection in your ST make sure you select TCP/IP channel.

Enter username and password that reflects a supervisor level in the AK-SM 800A you are connecting to.

Once connected, navigate to your required controller in the available list. Access to all AK2 parameters is available via this connection.

##### **8.3 CoreSense ™** **(MODBUS) Support**

Danfoss AK-SM 800A series version 08.053 and higher supports select Emerson modules within the CoreSense™ range. In particular, the following two module types are supported (see important notes below for supported versions).

###### **CoreSense™ Protection for Discuss Compressors**

Module type R112 (529-0170) is supported via the available device file;

529-0170 CSProtect 512 0 25 001x 529-0170.ed3 |(529-0170) CSProtection for Discuss

###### **CoreSense™ Diagnostics**

Module type R1011 (526-9996) is supported via the available device files; 526-9996 CSDiagnost 512 0 25 001x 526-9996.ed3 |(526-9996) CSDiagnostics for K5 526-9998 CSDiagnost 512 0 25 001x 526-9998.ed3 |(526-9998) CSDiagnostics for K5

Only the above versions of CoreSense™ Protection modules are supported, please observe the following requirements. CoreSense™ Modules that have 10 dip switch must have firmware version F33 or newer.

CoreSense™ compressor support requires a valid MODBUS network to be in place, following standard MODBUS topology rules (point to point, no star connections). Ensure each module follows the manufacturer’s recommendation for unique addressing (via module) bit switch and correct terminal wiring. Ensure the last node on the MODBUS network has 120 Ohm resistor in place.

Each module must be set for ‘Stand Alone Mode’, else invalid module alarms will occur. To set the modules for ‘Stand Alone Mode’ use the relevant bit switches on the module-refer to the CoreSense™ user guide for more details.

Once all network cabling, node addressing, and Stand Alone Mode are defined, the SM800A can now scan the MODBUS network to discover the nodes. Enter valid authorization and navigate to the Network Nodes screen. The Channel MODBUS RS-485 must be enabled and ‘SLV/CSENSE’ must be set to “Yes” for the 19,200 Baudrate (default Baudrate) before pressing rescan. The MODBUS address must be unique across all channels.

*[Figurtekst: JP5 · Network Termination · Unterminated 220 V · or · JP3 Module 110 V · Terminated Power 2 · Contactor M · See Dipswitch · Legend Below Line L · Alarm A · SP1 3 2 1 JP4 Protective GND · Earth · 1-2 ECT Modbus · 2-3 Standard Modbus · JP1 · Do Not Remove · 35689101247]*

*[Figurtekst: 10 DIP switch version. · Only firmware version F33 or newer is supported.]*

*[Figurtekst: 10 Position Jumper Settings on CoreSense Protection Modules Prior to 2015]*

*[Figurtekst: + Grnd – (Modbus) 220 V · – Grnd + (E2) or · Module 110 V · Power · 2 · Contractor M · JP3 · 1-2 RS485 Line L · 1 2 3 Terminated · 2-3 RS485 · Unterminated Alarm A · Protective GND · JP4 Earth · 1-2 2 Stop bits · 3 2 1 2-3 1 Stop bits · 12 DIP switch version. · Only firmware versions supported. · 12 · 3568910 11 1247]*

Default Jumper Settings on CoreSense Protection Modules 2015 and After

After the rescan is completed, verify the “Nodes Scanned on Network” for the new scanned nodes. Also, verify the “Generic” Node types for the new scanned nodes after a successful rescan. The address, type and the software version of the detected Coresense™ modules can be viewed under the Configuration  Network Nodes  Scan Status tab.

Once the scan is complete, the Coresense™ modules can be configured under the “ConfigurationControlRefrigeration” tab of the SM800A series Control Tab. The number of Coresense™ modules to be configured must be entered for each suction group. Select the relevant ED3 file for the module (under the “Type” Tab Configuration  Control  CompView  Type for each configured Coresense™ module). Enter a unique address for each Coresense™ module under the “Addresses” tab. Under the “Setup” tab it will show 6 other tabs to:

1. Alarms: Enable or disable the alarms for a generic device

2. Copy: Copy devices in the offline configuration

3. Upload: Upload the parameters from the device

4. Download: Download the parameters to the device

5. Import SI: Import the parameters as SI

6. Import OI: Import the parameters as OI

##### **8.4 Danfoss Drives –** **Modbus integration**

Your System Manager SW version 5.1 now supports Danfoss drive integration over Modbus. The following drives are currently supported (consult with Drive Tech support for firmware update on drives).

- FC-101 v06.5x

- FC-102 v07.81

- FC-103 v03.70

- FC-280 v02.0x, 03.3x

Follow the steps below to onboard the Drives to SM800A v5.1, the below assumes factory default drive.

###### **Step 1:** Network connection to Drive

Connect the drive(s) via Modbus communications to the SM800A. SM800A Modbus#1 is generally regarded as the recommended channel for Danfoss devices, leaving Modbus#2 for 3rd party, but this is not mandatory, as Modbus#2 can be used.

**Step 2:** Configure drive for Modbus RTU, set address and baud rate

For the drive to be detected by the System Manager, the drive needs to be configured for Modbus communications, a unique net address and suitable baud rate settings must be applied. From Drive Main Menu select option 8 (Comm & Options) where all these settings can be accessed.

1. Configure drive for Modbus RTU (menus 8-3, 8-30, 8-31, 8-32). Menu 8-33 & 8-34 refer to Modbus parity and stop bits, check that these are set to ‘Parity’ and ‘1’

2. Configure drive unique Modbus net address

- a.  Configure drive baud rate 38400

- i.  Required for Modbus channel 1

- ii.  Recommend Modbus channel 2

**Step 3:** Perform a network scan via the AK-SM800A, via the Configuration Network Nodes

**Step 4:** Configure Drive(s) in 800A as standalone devices, this can be done via configuring a Rack/Pack as either ‘no compressor’ or selecting a Pack device (i.e. AK-PC782A).  Once set, Drive configuration can be done within these (no compressor or actual Pack device) configurations – a maximum of 3 Drives can be defined per no compressor or Pack group.  Example – Adding drives as stand-alone devices under the ‘no compressor’ configuration, name the group (example Danfoss Drives), then under the Refrigeration menu select the number of drives required (max 3) and select the corresponding Drive type.  Add the corresponding network address for each drive (via Address) menu

##### **9. System: updating SW and databases**

The System menu provides access to System level functionality, focusing on software, OS (Operating System), EDF update management. This is the screen used to update your System Manager, and each button will cover the respective workflow.

1. Software Management Tab

2. Database Tab

3. Visualization of current System Manager SW versions (if connected via Internet the system can ‘call home’ to identify if any (Software and OS) updates are available).

4. Action buttons

   - a. Software update – use this to upgrade your system manager(s) main SW

   - b. OS (Operating System) update - use this to upgrade your system manager(s) main OS

   - c. EDF update - use this to update EDF (device files) to your system manager(s)

   - d. Diagnostic Report – Use this to export zip file, this is intended for Danfoss only and contains Technical System operational data (no personal information is contained in this file)

- e. Diagnostic Log – same as Diagnostic Report but presented on screen

##### **9.1 Updating system software**

The software update workflow allows for updating of your System Manager in a structed way.  Updating the software via a .spk SW package is possible via two methods, locally stored on your computer or via online (requires Internat access) and will pull from Danfoss SW server.

**Important Note:** Once the System Manager is updated to SW 5.0.x there is no rollback functionality due to the significant structural changes of the database in SW 5.0.x.  The ‘Backup current software version’ check box is intended for older SW versions

**Note: Ensure power is not interrpted during any system updates.**

###### **OS Update**

The System Manager operating system can be updated and follows the same workflow logic as described in the Software Update.

###### **EDF update**

EDF are devices files that virtually represent physical devices and inform the System manager of the devices parameters, menus, groupings and several other devices specific aspects.  Device file updates can be managed via the EDF update workflow, using a similar workflow as described in software update.

After initial download (staging) a dialog box will appear, highlighting the new/updated EDF files, along with your current files.  After installing, your System Manger will reset.

##### **9.2 Exporting/importing database**

The Database management screen is provided to facilitate the importing or exporting of system database.  As part of best practice, always Export (backup) any System Manager before updating software or making major changes.

Use the Import database function to load a database intended for your specific application – importing a database will override any existing database.

**Note:** As part of best security practices, User credentials are not saved in the database.

##### **10. Technical data**

##### **10.1 Technical data**

|**AK-SM 800A version comparison**|**AK-SM 820A**<br>**Small store**|**AK-SM 850A**<br>**Refrigeration**|**AK-SM 880A**<br>**Full**|
|---|---|---|---|
|**Refrigeration Control**||||
|All AK-SM 800A variants come with Centralized I/O and Pack /<br>||||
|Case control options.<br>EKC<br>AK2<br>SLV|Max. 32<br>generic device support|Max. 170<br>generic support<br>(see 8.7 Specifications)|Max. 170<br>generic support<br>(see 8.7 Specifications)|
|FC102||||
|**Lighting Control**||||
|All AK-SM 800A variants come with built in lighting control via<br>I/O modules.|10|30|30|
|The number of zones differ.||||
|**HVAC**||||
|Only the AK-SM 820A and AK-SM 880A support built in HVAC<br>control via I/O|10|n/a|45|
|**Alarms**||||
|Capacity|500|500|500|
|Miscellaneous points (via IO modules)||||
|Relay (R), Sensor (S), ON / OFF (O / F),<br>Variable(V)|R=20, S=20, O / F=20, V=20|R=70, S=80, O / F=70, V=70|R=70, S=80, O / F=70, V=70|
|**Master control**||||
|Po Optimization, Master Schedules, AKC ON<br>Note: Adaptive Defrost not currentlysupported|Yes|Yes|Yes|
|**Misc Calculations**||||
|Boolean Logic statements|96|96|96|
|**History**||||
|The AK-SM 800A includes a History function, allowing the<br>collection, save and view of history points.<br>Sample rate options 1,2,5,10,15,30 mins / 1,2,6,24 hr||||
|• Polled points: points collected on a scheduled time basis (i.e.<br>every5 mins).|3000 polled points|3000 polled points|3000 polled points|
|• Event-driven points: only get collected if a change of state is<br>seen(i.e. a setpoint is modified).|2000 event-driven points|2000 event-driven points|2000 event-driven points|
|HistoryHACCP|200 totalpoints|200 totalpoints|200 totalpoints|
|**Leak Detectors**||||
|Refrigerantgas detectors(connected via AK I/O)|10|50|50|
|**Energy Meters**||||
|Pulse Input (via I/O module), Carlo Garvazi, Wattnode, Wattnode<br>Plus MODBUS,Veris MODBUS,Schneider PM3255 and iEM3250|32|80|80|

##### **10.2 Generic capacity -** **A**

|**Features**|**Max # of nodes**|**Modbus properties**|
|---|---|---|
|**Danfoss Modbus**|||
|Danfoss Modbus controller devices(EKC,AK-CC,AK-PC 3,4,5x,MCX)|170|PARITY_EVEN,38400,DATA_8_BITS|
|Danfoss Gas Sensors(DGS)|50|PARITY_EVEN,38400,DATA_8_BITS|
|Danfoss SLV,WattNode MODBUS(MODBUS)|120|PARITY_EVEN,19200,DATA_8_BITS|
|**Danfoss SNMP**|||
|Danfoss SNMP controller devices|160|n/a|
|**Danfoss Lon (RS485/TP78)**|||
|AK2 Multi-Case controllers(maxper front end / no furthergeneric devices allowed)|60|n/a|
|AK2 Pack Controllers|12|n/a|
|**Danfoss Danbuss (Legacy AKC)**|||
|Danfoss Danbuss via PI-200(max X4 PI-200per front end)|120||

##### **10.3 Generic capacity -** **B**

|Typical mix examples|Field bus deployment examples|
|---|---|
|Danfoss Pack(x12)+ Danfoss Case(x158)= 170 max|12 LonWorks,120 Mod#1,38 Mod#2|
|Danfoss Pack(x10)+ Danfoss Case(x110)+ Danfoss Gas sensors(x50)= 170 max|10 LonWorks,120 Mod#1,40 Mod#2|
|Danfoss Pack(x10)+ Danfoss AK2 Multi-EvapCase(x50)= 60 max|60 LonWorks|
|Danfoss Rack I/O(x12)+ Danfoss Case(x170)= 170 max|LonWorks,85 Mod#1,85 Mod#2|

**Note:** Max. 120 Modbus nodes per Modbus channel (170 max. in total between Mod#1 and Mod#2). **Note:** Software Package 4.0 and above supports 160 circuits per Pack suction group.

##### **10.4 Specif i** **cations**

|**Data communication**|||
|---|---|---|
|Ethernet(WAN/Host network)|1||
|Ethernet 1(AK-Pack IP field bus)|1||
|USB|2(Host)+ 1(800 mA)||
|Wi-Fi(Point-to-point access)|1||
|Alarm relays|2 Contact voltage: upto 240 V,Current rating: max. 5 Ampfor AC-1(Ohmic l|oad),Max. 3 Ampfor AC-15(inductive load)|
|**Field Bus Support**|||
|RS485 Modbus|2||
|RS485 LON|1||
|TP78|4(optional code #)||
|CANbus|1(future)||
|Ethernet 1|1||
|**Hardware specifications**|||
|Enclosure|IP20||
|Dimensions(WxDxH)|295 mm(11.6”)x 65 mm(2.5”)x 235 mm(9.3”)||
|Weight(gross)|2,408 kg||
|**WiFi transmitter**|||
|WIFI Type|Wi-Fi Access Point||
|Transmitter type|Wi-Fi 2.4 GHz / 5 GHz(IEEE 802.11a/b/g/n/ac)||
|Transmit Frequency|2412 – 2472 MHz,4900 – 5925 MHz(frequencies limited bySoftware)||
|Receive Frequency|2412 – 2472 MHz,4900 – 5925 MHz||
|Antenna Gain|2.4 GHzgain: 1.8 dBi,5 GHzgain: 4.9 dBi||
|**Communication standards**|||
|Modbus|||
|Modbus IP(Danfoss AK-CC55 con|trols)||
|Lonworks|||
|Danbus(via PI-200)|||
|SNMP|||
|AK-Pack IP controller(UDP/TCP)|||
|**Port**|**Description**<br>**Use**|**User Configurable**|
|5136|UDP<br>SNMP|No|
|1041|UDP<br>PI-200|No|
|443|TCP<br>HTTPS Secure Web browser communications|Yes|
|80|TCP<br>HTTP Web browser communications|Yes|
|5003,5005|UDP<br>Host network communication UDPports|No|

##### **10.5 Security**

The System Manager 800A series has been designed to reside behind appropriately configured firewalls and secure LAN. Do not install on any public or non secure network.

###### **Session control**

System Manager 800A software package v4.0x and above enhances your product’s security features to meet internationally recognized regulations such as the NIS2 and CRA directives. Also following the global standard IEC 62443-4-1 in regard to security by design practices, and to comply to NIS2 and CRA European regulation requirements.

In compliance with IT best practice and mandatory standards, Danfoss is now defaulting to a strong security posture on the System Manager 800A, via software package 4.0.x and above. This feature is called session control and when combined with HTTPS improves overall security of your product.

Session control is an authentication rules engine/module and is intended to improve the overall security posture of your system. Session control offers different configuration settings (backward compatibility, permissive and strict). Depending on how these settings are configured, the remote interface will need to comply accordingly – **installing software release 4.0 and above will** **default to strict mode.** Consult with the AK-SM800A user guide for additional details.

###### **General**

- Access to USB application functions (USB flash drive) based on user authentication level/permission

- Factory set Linux OS firewall enabled - all non -required ports closed

- Linux OS updates available via Danfoss secure update server

- FTP - not available nor used in system

- Linux firewall between wireless access point and host network

- Linux firewall between Ethernet 0 and Ethernet 1

###### **DISCLAIMER: Professional use only**

This product is not subject to the UK PSTI regulation, as it is for supply to and use only by professionals with the necessary expertise and qualifications. Any misuse or improper handling may result in unintended consequences. By purchasing or using this product, you acknowledge and accept the professional-useonly nature of its application. Danfoss does not assume any liability for damages, injuries, or adverse consequences (“damage”) resulting from the incorrect or improper use of the product and you agree to indemnify Danfoss for any such damage resulting from your incorrect or improper use of the product.

###### **Remote encrypted communications**

- HTTPS web browser support (Chrome / Safari / Edge (Chromium))

- HTTPS XML

###### **Communication ports**

- 443 HTTPS (user configurable)

- Wi-Fi access point

###### **System passwords / user access**

- All passwords stored in encrypted format

- User authentication required for unit access (no view only mode)

- Passwords comply with min 8 characters (1 capital, 1 special character, 1 numeral)

- User accounts and passwords not stored in system application database

- Password reset via authenticated unit check and issue of temporary code

- Danfoss does not have access nor can view passwords

###### **Software update**

- System software (application/device files/OS) stored and distributed via Danfoss software server

- Software payloads have digital signature to ensure authentic source

###### **E-mail alarm notifications**

- TLS 1.2

###### **Wi-Fi user wireless access point (point to point connection to unit)**

- WPA2 encryption

- Default state off, enabled only via authorized users for 120 mins

- Isolated from WAN / Host network

- Password protected SSID associated with unit host #, password

##### **11. Appendix**

###### **Utilities- Browser Certificate**

###### **Browser certificate management tool**

Communication with the system manager via web interface is encrypted when (as default) HTTPS is enabled. The AK-SM 800A uses a self-signed certificate (SSC) and whilst the connection is secure, your web browser will likely mark the connection as not trusted. To facilitate a trusted connection between your web browser and the AK-SM 800A, the SM800A browser certificate must be signed by an authority known to the browser. The browser certificate feature under the Utilities section is a tool intended for customer use and allows the creation of a CRS (Certificate Signing Request) allowing the customer to self-sign or obtain a Certificate Authority (CA) signed certificate. Once signed, the certificate is uploaded back to the SM800A - thus creating a root of trust between SM800A and browser. Key notes:

- When the generate request is made, a new private key with 2048 bits is created using RSA

- The hash function uses 256 bits

- The certificate will expire after 365 days

The following procedure can be followed for the browser certificate management tool, where a Certificate Signing Request (CSR) will be initiated, resulting in a configuration file containing a new private key with 2048 bit RSA encryption.

1. Navigate to the Utilities section of the SvB5 and select browser certificate

2. The info screen will be shown

3. Navigate to the ‘Generate’ screen and fill in the following information

4. Country

5. Domain

6. IP Address

7. Organization

8. Press the generate button which will output a csr file

9. This crs file then must be signed by a trusted authority, usually via the following options

10. The user pays an internationally trusted CA (e.g. VeriSign, DigiCert) to sign the certificate. In this case the browser already has the root and intermediate certificate installed.

11. The user acts as a certificate authority to sign the CSR, installs root and intermediate certificates in user browser

12. Once the CSR is signed the user uploads the file through the web interface (Upload menu). The system manager first checks if the uploaded certificate is valid and ensures that a matching <domain>.key file exists. Finally, it runs a test to check if the uploaded certificate matches the private key (<domain>.key) that was created along with CSR. If the test passed, the current certificate is replaced, else the changes are rolled back and an error is returned. If the update was successful a summary of the new certificate is sent back as response.

- The image below is a graphical representation of this workflow.

*[Figurtekst: Certificate Authority (CA) Web Browser sm.domain.net · Generate  Certificate Signing Request (CSR) · for sm.domain.net · Download csr · CSR to be signed by CA · Receive signed CSR (PEM file) · Upload Signed Certificate]*

##### **12. Ordering**

Contact your local Danfoss sales office.

###### **Variants with LON Modules**

|**Type**|**Description**|**Code no.**|
|---|---|---|
|AK-SM 820A|C-Store (Refrigeration / HVAC / Lighting)|080Z4024|
|AK-SM 850A|Refrigeration (includingLighting)|080Z4021|
|AK-SM 850A - no WiFi|No Wi-Fi, Refrigeration (includingLighting)|080Z4022|
|AK-SM 880A|Full (Refrigeration / HVAC / Lighting)|080Z4028|
|AK-SM 880A  - TP78|Retro-fit Full (Refrigeration / HVAC / Lighting)|080Z4029|

###### **Variants without LON Modules**

|**Type**|**Description**|**Code no.**|
|---|---|---|
|AK-SM 820A|C-Store (Refrigeration / HVAC / Lighting)|080Z4044|
|AK-SM 850A|Refrigeration (includingLighting)|080Z4041|
|AK-SM 880A|Full (Refrigeration / HVAC / Lighting)|080Z4048|

##### **13. Certificates, declarations and approvals**

The list contains all certificates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

When you click on the link you will be directed to the latest version of the ‘Declaration of Conformity’. Products developed and sold before this date of issue conform to the directives/standards in force at the time of their sale.

|**Approval type**|**Title**|**Certification body**|**Approval topic**|
|---|---|---|---|
|EAC Declaration|ЕАС KZ 7100841.13.12.01062|EAC - Eurasian Customs Union|EMC|
|Electrical SafetyCertificate|ЕАС KZ 7100841.01.01.01245|EAC - Eurasian Customs Union|LVD, EMC|
|Export Control Declaration|AK-SM 800/800A SYSTEM MANAGERS|Danfoss||
|Manufacturer's Declaration|Danfoss MD 080R1221.02|Danfoss|China RoHS|
|EU-UK Declaration|Danfoss EU-UK 080R1236.01|Danfoss|LVD, EMC, EU RoHS, UK RoHS|
|Manufacturer's Declaration|Danfoss MD 080R1244.00|Danfoss|EAEU RoHS|
|EU-UK Declaration|Danfoss EU-UK 080R1231.01|Danfoss|EU RoHS, UK RoHS, RED|
|Radio Equipment Certificate|MIIT 2021AJ8486|MIIT - Ministry of Industry & Information<br>Technologyof China|Wireless|
|Wireless Certificate|RSM CF 14616_NZ-Rev.00|RSM - Radio Spectrum Management|RCM|
|UA Declaration|UA 2024-06-27 electr. protection units<br>for<br>compressors|Danfoss|LVD, EMC|
|UK Declaration|Danfoss UK 080R1236.00|Danfoss|EMC, UK RoHS, RED|
|UA Declaration|Danfoss UA 8537|Danfoss|UA RoHS|
|Electrical SafetyCertificate|UL E31024|UL - Underwriters Laboratories inc.||
|Radio Equipment Certificate|ICASA TA-20210214|ICASA - Independent Communication<br>Authorityof South Africa|Wireless|
|Wireless Certificate|ACMA CF14616_AU-Rev.00|ACMA - Australian Communication and Media<br>Authority|RCM|
|Radio Equipment Certificate|MIIT 2021-8491|MIIT - Ministry of Industry & Information<br>Technologyof China|Wireless|

The AK-SM 800A (software version 4.3 and above) complies with various cyber security standards and regulations.

**The Radio Equipment Directive (RED) 2014/53/EU** sets essential requirements for radio equipment marketed in the EU, ensuring safety, electromagnetic compatibility, and efficient use of the radio spectrum. Recent updates to the Directive, specifically under Delegated Regulation (EU) 2022/30, introduce new cybersecurity and privacy requirements, effective from August 1, 2025.

These new provisions mandate that radio equipment with internet connectivity or the ability to process personal data must incorporate safeguards to:

- Protect against network and service misuse

- Prevent unauthorized access and data breaches

Manufacturers must now integrate cybersecurity-by-design principles, conduct conformity assessments, and update technical documentation to demonstrate compliance. Products affected include smartphones, wearables, connected toys, and IoT devices.

As part of our commitment to security and regulatory alignment, our product development processes are certified under IEC 62443-4-1, the international standard for secure product development lifecycle. This certification validates our systematic approach to identifying, managing, and mitigating cybersecurity risks throughout the product lifecycle and supports compliance with RED’s enhanced security requirements.

This proactive approach ensures that our products not only comply with EU regulations but also adhere to globally recognized cybersecurity best practices, strengthening trust and reliability in connected technologies.

**CISA (Cybersecurity and Infrastructure Security Agency) NIS2 Directive (Directive (EU) 2022/2555)**

##### **14. Document history**

|**Document**|**Notes**|
|---|---|
|BC337629891709en-000101|First document release|
|BC337629891709en-000201|Updated for the release of ver. 2.0|
|BC337629891709en-000301|Updated for the release of ver. 3.0|
|BC337629891709en-000401|Revised IPport table / minor updates|
|BC337629891709en-000501|Updated for the release of ver. 3.2x|
|BC337629891709en-000601|Updated for the release of ver. 3.3x|
|BC337629891709en-000701|Updated for the release of ver. 4.0|
|BC337629891709en-000801|Updated for the release of ver. 4.1|
|BC337629891709en-000901|Updated for the release of ver. 4.2|
|BC337629891709en-001001|Updated for the release of ver. 5.0|

##### **15. Glossary of terms**

Viz Visual file. Used in the RMT tool and sent to the AK-SM for graphic Site View SvW StoreView Web (remote UI for System manager, cloud or desktop) SvW ‘embedded’ Remote UI included in the System Manager System view Central page of AK-SM that displays all configured control points Site view Custom graphic page with mapped system parameters AK I/O Danfoss AK Input / Output modules Bd-Pt Board & Point address location Alarm levels Disabled = no alarm action Log Only = logs alarm in database - no external action Normal = Activate alarm output (once) Severe = Activate alarm output (repeat based on severe repeat time) Critical = Activate alarm output (repeat based on critical repeat time) IP Internet Protocol EDF/ED3 Extended Device File (a file that represents the physical device) CAT (seen in EDF list) Category (1=Evap, 2=Pack, 8=HVAC, 16=Energy meter, 34=AKD102) Relative schedule When set a relative schedule will offset against the operating hours (set under config/time) Host communications The connection (via Ethernet) of one or more AK-SM units. The connection between units is known as ‘host network’ Danfoss http://danfoss.com Danfoss software http://food-retail.danfoss.com/knowledge-center/software/ak-sm-800/ Veris Industries™ http://www.veris.com/ Carlo Gavazzi™ http://www.carlogavazzi.com/ Continental Control Systems™ http://www.ccontrolsys.com/w/Home CALM CO2 Adaptive Liquid Management ALC Adaptive Liquid Control Bluetooth® The Bluetooth logos and word marks referenced in the Services and Content are the trademarks of Bluetooth SIG and its affiliates. Session control Session control in the AK-SM 800A is an authentication rules engine/module and is intended to improve the overall security posture of your system. Session control offers different configuration settings (Backward compatibility, Permissive and Strict), When configured to Permissive or Strict, Northbound communications require HTTPS and encryption of all data ensuring that XML requests do not contain usernames and passwords, thus enhancing the overall security of your system.

Explore our solutions danfoss.com

##### **16. Contact details**

##### **Online support**

Danfoss offers a wide range of support along with our products, including digital information, software, mobile apps and expert guidance. See the possibilities below.

###### **The Danfoss Design center**

Discover the Design Center, our advanced digital platform that streamlines product selection. With integrated tools and enhanced type pages, it's simpler than ever to access product information and documentation, and to select the right products. Check the availability of Danfoss products at partner locations and enjoy seamless transitions from selection to purchase with our basket-to-basket functionality. Whether you're buying from our distributors or directly from the Product Store, the Design Center simpli�es your experience. Learn more at: designcenter.danfoss.com.

###### **The Danfoss product store**

The Danfoss Product Store is a one-stop shop available 24/7 for our customers, no matter where you are in the world or what area of industry you work in. Browse our catalog, check product details and documentation, view your prices and product availability, and �uickly �nalize your purchase. Start browsing at: store.danfoss.com.

###### **Danfoss Partner Portal/Product Data tool**

Designed to support you with easy access to product data extracts, essential resources, tools, and information. The Partner Portal provides a centralized hub for product documentation, training materials, marketing assets, and technical support, ensuring you have everything you need to succeed and grow your business with Danfoss. The Partner Portal is available 24/7 at: partner.danfoss.com and is ready to support your business.

###### **Find technical documentation**

Find technical documentation you need to get your project up running. Get direct access to our official collection of data sheets, certi�cates and declarations, manuals and guides, �D models and drawings, case stories, brochures, and much more. Start searching now at: documentation.danfoss.com.

Danfoss Learning is a free online learning platform. �t features courses and materials speci�cally designed to help engineers, installers, service technicians, and wholesalers better understand the products, applications industry topics, and trends that will help you do your job better. Find your local Danfoss website here: learning.danfoss.com.

###### **Get local information and support**

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest reginal news, or connect with a nearby expert - all in your own language. Find your local Danfoss website here: danfoss.com.

---

## 2. AK-SM 820A / 850A / 880A – Data sheet (SW 5.0x, engelsk)

*Kilde: Danfoss-dokument AI354138789910en-000901. Tekniske data, varianter og bestillingsnumre for AK-SM 800A.*

**Data sheet**

### System manager AK-SM 820A / AK-SM 850A / AK-SM 880A

SW ver. 5.0x Global control and supervisory solution for food retail industry

#### **Description**

The System Manager controller from Danfoss is the global control and supervisory solution for food retail industry. The System Manager uses the latest technology to provide maximum bene�t to the end user, both in terms of energy saving optimization, control options and full web user access. Designed speci�cally for the food retail and food processing / handling market, the System Manager provides comprehensive functionality and support tools to cover small to large stores.

##### **Features & bene�ts**

- Global food retail electronics platform, supporting multiple applications Implementation of IT industry standard security protocols

- Enhanced UI/UX – new yet familiar touch screen

- Full built in web server and browser interface, known as StoreView Web (SvW)

- Secure Wi-Fi access point

- Retro-�t ready – includes EoL and legacy control functions supporting smooth upgrade path

- Built-in, license free, energy saving functions

#### **Ordering**

##### **Product code numbers**

###### **Table: AK-SM 800A variants**

|**Type**|**Description**|**Code no.**|
|---|---|---|
|AK-SM 820A|C-Store (Refrigeration / HVAC / Lighting)|080Z4024|
|AK-SM 850A|Refrigeration (includingLighting)|080Z4021|
|AK-SM 850A - no WiFi|No Wi-Fi, Refrigeration (including Lighting)|080Z4022|
|AK-SM 880A|Full (Refrigeration / HVAC / Lighting)|080Z4028|
|AK-SM 880A - TP78|Retro-�t Full (Refrigeration / HVAC / Lighting)|080Z4029|

###### **Table: AK-SM 800A variants without LonWorks®**

|**Type**|**Description**|**Code no.**|
|---|---|---|
|AK-SM 820A|C-Store (Refrigeration / HVAC / Lighting)|080Z4044|
|AK-SM 850A|Refrigeration (includingLighting)|080Z4041|
|AK-SM 880A|Full (Refrigeration / HVAC / Lighting)|080Z4048|

#### **Product details**

##### **General data**

**Table: Features (based on software 5.0 and above)**

|**Main feature**|**Description**|
|---|---|
|Designed and created for food<br>retail|Built-in control logic covering centralized (rack I/O) and de-centralized (Pack, Case<br>controllers) application formats<br>Built-in misc. boolean logic tool<br>Built-in energy optimizations providing continuous energy savings and efficiency<br>Built-in security for corporate connectivity<br>Flexible alarm logic, monitoring and management<br>Supporting full range of Danfoss devices<br>Supporting 3<sup>rd</sup>party devices (non-Danfoss)<br>Open data transfer (XML)|
|Versions|AK-SM 820A small store (Wi-Fi & no Wi-Fi versions)<br>AK-SM 850A refrigeration (Wi-Fi & no Wi-Fi versions)<br>AK-SM 880A full store (inc. lighting control)<br>AK-SM 880A TP78 retro�t (x4 TP78 channels designed for retro�t applications)|
|Connectivity|x3 USB port connections<br>Secure Wi-Fi access point for mobile or laptop connection<br>Ethernet (x2)<br>Multiple �eldbus connections and topology (LON, Modbus, Modbus/TCP, SNMP, AK-IP)<br>Northbound (cloud / WAN)<br>Southbound (�eld bus)|
|IT Security best practice|Secure web connection (HTTPS)<br>Secure e-mail, encrypted data and secure software update packages<br>Vulnerability scan tested<br>Session control (default to strict mode)<br>Encrypted user accounts / use of strong password supported/recommended|
|Enhanced user interface|Color touch screen<br>Built in web interface – StoreView Web<br>Quick Links menus help navigate faster though the system<br>Wizards to improve setup work streams|
|Modern computing platform|Responsive system performance<br>Extended device support via increased system memory<br>Extended log point collection for future view, export or sync with cloud|
|Remote interface / cloud<br>integration|Utilization of standard Web browsers<br>Operational efficiency through the Alsense food retail cloud platform and connected<br>services.<br>Open data access for enterprise systems|

###### **Table: Technical data**

|**AK-SM 800A version comparison**|**AK-SM 820A**<br>**Small store**|**AK-SM 850A**<br>**Refrigeration**|**AK-SM 880A**<br>**Full**|
|---|---|---|---|
|**Refrigeration control**||||
|All AK-SM 800A variants come with centralized I/O<br>and Pack / Case control options.<br>EKC<br>AK2<br>SLV<br>AK-CC|Max. 32 generic device<br>support|Max. 170 generic device<br>- see_Table: Speci�cations_|Max. 170 generic device<br>- see_Table: Speci�cations_|
|**Lighting control**||||
|All AK-SM 800A variants come with built-in lighting<br>control via I/O modules. The number of zones<br>differ.|10|30|30|
|**HVAC**<br>Only the AK-SM 820A and AK-SM 880A support<br>built-in HVAC control via I/O|10|n/a|45|
|**Alarms (active)**||||
|Capacity|500|500|500|
|Miscellaneous points (via IO modules)||||
|Relay (R), Sensor (S),<br>ON/OFF (O/F), Variable (V)|R=20, S=20,<br>O/F=20, V=20|R=70, S=80,<br>O/F=70, V=70|R=70, S=80,<br>O/F=70, V=70|
|**Master control**||||
|Po optimization, master schedules, AKC ON<br>Note: Adaptive defrost not currentlysupported|Yes|Yes|Yes|
|**Misc calculations**||||
|Boolean logic statements|96|96|96|
|**History**||||
|The AK-SM 800A includes a History function,<br>allowing the collection, save and view of history<br>points.<br>Sample rate options 1, 2, 5, 10, 15, 30 mins / 1, 2, 6,<br>24 hr||||
|Polled points: points collected on a<br>scheduled time basis (i.e. every 5 mins).|3000 polled<br>points|3000 polled<br>points|3000 polled<br>points|
|Event-driven points: only get collected if<br>a change of state is seen (i.e. a setpoint is<br>modi�ed).|2000 event-driven<br>points|2000 event-driven<br>points|2000 event-driven<br>points|
|HistoryHACCP|200 totalpoints|200 totalpoints|200 totalpoints|
|**Leak detectors**||||
|Refrigerantgas detectors (connected via AK I/O)|10|50|50|
|**Energy meters**||||
|**Pulse input**(via I/O module)<br>**Preferred Modbus meters:**Carlo Gavazzi<br>EM511, EM530<br>**Other Modbus meters:**Wattnode Plus,<br>Veris EH8035, EH8036, Schneider Electric,<br>PM3255 and iEM3250, Carlo Gavazzi<br>EM24AV5, AV6, AV9<br>**Other LonWorks meters:**WattNode|32|80|80|

###### **Table: Generic capacity**

|**Features**|**Max # of nodes**|**Modbusproperties**|
|---|---|---|
|**Danfoss Modbus**|||
|Danfoss Modbus controller devices (EKC, AK-CC, AK-PC<br>3,4,5x, MCX)|170 total across both<br>channels (Mod#1 / Mod#2)|PARITY_EVEN, 38400, DATA_8_BITS|
|Danfossgas sensors (DGS)|50|PARITY_EVEN, 38400, DATA_8_BITS|
|Danfoss SLV, WattNode Modbus (Modbus)|120|PARITY_EVEN, 19200, DATA_8_BITS|
|Danfoss drives: FC103, FC1-2, FC280, FC101|3 per rack/pack|PARITY_EVEN, 38400, DATA_8_BITS<br>PARITY_EVEN, 19200, DATA_8_BITS|
|**Danfoss Modbus/TCP**|||
|Danfoss Alsmart/TCP|170|n/a|
|**Danfoss SNMP**|||
|Danfoss SNMP controller devices|160|n/a|
|**Danfoss Lon (RS485/TP78)**|||
|AK2 multi-case controllers (max per front end / no further<br>generic devices allowed)|60|n/a|
|AK2 Pack controllers|12|n/a|
|**Danfoss Danbuss (legacy AKC)**|||
|Danfoss Danbuss via PI-200 (max X4 PI-200per front end)|120||

###### **Table: Generic capacity**

|**Typical mix examples**|**Field bus deployment examples**|
|---|---|
|Danfoss Pack (x12) + Danfoss Case (x158) = 170 max.|12 LonWorks, 120 Mod#1, 38 Mod#2|
|Danfoss Pack (x10) + Danfoss Case (x110) + Danfoss Gas Sensors (x50) = 170 max.|10 LonWorks, 120 Mod#1, 40 Mod#2|
|Danfoss Pack (x10) + Danfoss AK2 multi-evapcase (x50) = 60 max.|60 LonWorks|
|Danfoss Rack I/O (x12) + Danfoss Case (x170) = 170 max.|LonWorks, 85 Mod#1, 85 Mod#2|

**Note:** Max. 120 Modbus nodes per Modbus channel (170 max. in total between Mod#1 and Mod#2).

##### **Main functionalities**

###### **Table: Speci�cations**

|**Data communication**|1|
|---|---|
|Ethernet 0 (WAN/Host network)|**Note:**Do not mix legacy System Manager 800 units on the same host network as System<br>Manager 800A. These different unit types are not compatible and require separate host<br>networks.|
|Ethernet 1 (AK-Pack IP �eld bus)|1|
|USB|2 (host) + 1 (800 mA)|
|Wi-Fi (point-to-point access)|1|
|Alarm relays|2 contact voltage: up to 240 V<br>Current rating: max. 5 A for AC-1 (ohmic load), max. 3 A for AC-15 (inductive load)|
|**Field Bus Support**||
|RS485 Modbus|2|
|RS485 LON|1|
|TP78|4 (optional code #)|
|CANbus|1 (future)|
|Ethernet 1 Southbound �eldbus|AK-IP, Modbus TCP, SNMP, PI-200|
|**Hardware speci�cations**||
|Enclosure|IP20|
|Dimensions (WxDxH)|295 mm (11.6 in) x 65 mm (2.5 in) x 235 mm (9.3 in)|
|Weight (gross)|2.408 kg|
|**Wi-Fi transmitter**||
|Wi-Fi Type|Wi-Fi accesspoint|
|Transmitter type|Wi-Fi 2.4 GHz / 5 GHz (IEEE 802.11a/b/g/n/ac )|
|Transmit frequency|2412 – 2472 MHz, 4900 – 5925 MHz (frequencies limited bysoftware)|
|Receive frequency|2412 – 2472 MHz, 4900 – 5925 MHz|
|Antennagain|2.4 GHzgain: 1.8 dBi, 5 GHzgain: 4.9 dBi|
||Modbus (serial)<br>LonWorks (TP78/RS485)|
|**Communication standards**|Danbus (via PI-200)<br>SNMP|
||AK-Pack IP controller (UDP/TCP)<br>Modbus-TCP|
|**Ports open**|**Description**<br>**Use**<br>**User con�gurable**|
|5136|UDP<br>SNMP<br>No|
|1041|UDP<br>PI-200<br>No|
|443|TCP<br>HTTPS secure web browser communications<br>Yes|
|80|TCP<br>HTTP web browser communications<br>Yes|
|5003, 5005|UDP<br>Host network communication UDPports<br>No|

###### **Security**

The System Manager 800A series has been designed to reside behind appropriately con�gured �rewalls and secure LAN. Do not install on any public or non secure network.

###### **Session control**

System Manager 800A software package v4.0x and above enhances your product's security features to meet internationally recognized regulations such as the NIS2 and CRA directives. Also following the global standard IEC 62443-4-1 in regard to security by design practices, and to comply to NIS2 and CRA European regulation requirements.

In compliance with IT best practice and mandatory standards, Danfoss is now defaulting to a strong security posture on the System Manager 800A, via software package 4.0.x and above. This feature is called **session control** and when combined with HTTPS improves overall security of your product.

Session control is an authentication rules engine/module and is intended to improve the overall security posture of your system. Session control offers different con�guration settings (backward compatibility, permissive and strict). Depending on how these settings are con�gured, the remote interface will need to comply accordingly – **installing software release 4.0 and above will default to** **<u>strict mode.</u>** Consult with the AK-SM800A user guide for additional details.

###### **Remote encrypted communications**

HTTPS web browser support (Chrome / Safari / Edge (Chromium)) HTTPS XML

###### **Communication ports**

443 HTTPS (user con�gurable)

Wi-Fi access point

###### **System passwords / user access**

All passwords stored in encrypted format

User authentication required for unit access (no view only mode)

Passwords comply with min 8 characters (1 capital, 1 special character, 1 numeral)

User accounts and passwords not stored in system application database

Password reset via authenticated unit check and issue of temporary code

Danfoss does not have access nor can view passwords

###### **Software update**

System software (application/device �les/OS) stored and distributed via Danfoss software server

Software payloads have digital signature to ensure authentic source

###### **E-mail alarm noti�cations**

TLS 1.2

###### **Wi-Fi user wireless access point (point to point connection to unit)**

WPA2 encryption

Default state off, enabled only via authorized users for 120 mins

Isolated from WAN / Host network

Password protected SSID associated with unit host #, password

###### **General**

Access to USB application functions (USB �ash drive) based on user authentication level/permission

Factory set Linux OS �rewall enabled - all non -required ports closed

Linux OS updates available via Danfoss secure update server

FTP - not available nor used in system

Linux �rewall between wireless access point and host network Linux �rewall between Ethernet 0 and Ethernet 1

###### **DISCLAIMER: Professional use only**

This product is not subject to the UK PSTI regulation, as it is for supply to and use only by professionals with the necessary expertise and quali�cations. Any misuse or improper handling may result in unintended consequences. By purchasing or using this product, you acknowledge and accept the professional-use-only nature of its application. Danfoss does not assume any liability for damages, injuries, or adverse consequences (“damage”) resulting from the incorrect or improper use of the product and you agree to indemnify Danfoss for any such damage resulting from your incorrect or improper use of the product.

#### **Certi�cates, declarations and approvals**

The list contains all certi�cates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

When you click on the link you will be directed to the latest version of the ‘Declaration of Conformity’. Products developed and sold before this date of issue conform to the directives/standards in force at the time of their sale.

|**Approval type**|**Title**|**Certi�cation body**|**Approval topic**|
|---|---|---|---|
|EAC Declaration|ЕАС KZ 7100841.13.12.01062|EAC - Eurasian Customs Union|EMC|
|Electrical Safety Certi�cate|ЕАС KZ 7100841.01.01.01245|EAC - Eurasian Customs Union|LVD, EMC|
|Export Control Declaration|AK-SM 800/800A SYSTEM<br>MANAGERS|Danfoss||
|Manufacturer's Declaration|Danfoss MD 080R1221.02|Danfoss|China RoHS|
|EU-UK Declaration|Danfoss EU-UK 080R1236.01|Danfoss|LVD, EMC, EU RoHS, UK RoHS|
|Manufacturer's Declaration|Danfoss MD 080R1244.00|Danfoss|EAEU RoHS|
|EU-UK Declaration|Danfoss EU-UK 080R1231.01|Danfoss|EU RoHS, UK RoHS, RED|
|Radio Equipment Certi�cate|MIIT 2021AJ8486|MIIT - Ministry of Industry &<br>Information Technology of<br>China|Wireless|
|Wireless Certi�cate|RSM CF 14616_NZ-Rev.00|RSM - Radio Spectrum<br>Management|RCM|
|UA Declaration|UA 2024-06-27 electr.<br>protection units for<br>compressors|Danfoss|LVD, EMC|
|UK Declaration|Danfoss UK 080R1236.00|Danfoss|EMC, UK RoHS, RED|
|UA Declaration|Danfoss UA 8537|Danfoss|UA RoHS|
|Electrical Safety Certi�cate|UL E31024|UL - Underwriters Laboratories<br>inc.||
|Radio Equipment Certi�cate|ICASA TA-20210214|ICASA - Independent<br>Communication Authority of<br>South Africa|Wireless|
|Wireless Certi�cate|ACMA CF14616_AU-Rev.00|ACMA - Australian<br>Communication and Media<br>Authority|RCM|
|Radio Equipment Certi�cate|MIIT 2021-8491|MIIT - Ministry of Industry &<br>Information Technology of<br>China|Wireless|

The AK-SM 800A (software version 4.3 and above) complies with various cyber security standards and regulations.

**The Radio Equipment Directive (RED) 2014/53/EU** sets essential requirements for radio equipment marketed in the EU, ensuring safety, electromagnetic compatibility, and efficient use of the radio spectrum. Recent updates to the Directive, speci�cally under Delegated Regulation (EU) 2022/30, introduce new cybersecurity and privacy requirements, effective from August 1, 2025.

These new provisions mandate that radio equipment with internet connectivity or the ability to process personal data must incorporate safeguards to:

Protect against network and service misuse

Prevent unauthorized access and data breaches

Manufacturers must now integrate cybersecurity-by-design principles, conduct conformity assessments, and update technical documentation to demonstrate compliance. Products affected include smartphones, wearables, connected toys, and IoT devices.

As part of our commitment to security and regulatory alignment, our product development processes are certi�ed under IEC 62443-4-1, the international standard for secure product development lifecycle. This certi�cation validates our systematic approach to identifying, managing, and mitigating cybersecurity risks throughout the product lifecycle and supports compliance with RED’s enhanced security requirements.

This proactive approach ensures that our products not only comply with EU regulations but also adhere to globally recognized cybersecurity best practices, strengthening trust and reliability in connected technologies.

**CISA** (Cybersecurity and Infrastructure Security Agency) **NIS2** Directive (Directive (EU) 2022/2555)

#### **Contact details**

##### **Online support**

Danfoss offers a wide range of support along with our products, including digital information, software, mobile apps and expert guidance. See the possibilities below.

###### **The Danfoss Design center**

Discover the Design Center, our advanced digital platform that streamlines product selection. With integrated tools and enhanced type pages, it's simpler than ever to access product information and documentation, and to select the right products. Check the availability of Danfoss products at partner locations and enjoy seamless transitions from selection to purchase with our basket-to-basket functionality. Whether you're buying from our distributors or directly from the Product Store, the Design Center simpli�es your experience. Learn more at: designcenter.danfoss.com.

###### **The Danfoss product store**

The Danfoss Product Store is a one-stop shop available 24/7 for our customers, no matter where you are in the world or what area of industry you work in. Browse our catalog, check product details and documentation, view your prices and product availability, and quickly �nalize your purchase. Start browsing at: store.danfoss.com.

###### **Danfoss Partner Portal/Product Data tool**

Designed to support you with easy access to product data extracts, essential resources, tools, and information. The Partner Portal provides a centralized hub for product documentation, training materials, marketing assets, and technical support, ensuring you have everything you need to succeed and grow your business with Danfoss. The Partner Portal is available 24/7 at: partner.danfoss.com and is ready to support your business.

###### **Find technical documentation**

Find technical documentation you need to get your project up running. Get direct access to our official collection of data sheets, certi�cates and declarations, manuals and guides, 3D models and drawings, case stories, brochures, and much more. Start searching now at: documentation.danfoss.com.

Danfoss Learning is a free online learning platform. It features courses and materials speci�cally designed to help engineers, installers, service technicians, and wholesalers better understand the products, applications industry topics, and trends that will help you do your job better. Find your local Danfoss website here: learning.danfoss.com.

###### **Get local information and support**

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest reginal news, or connect with a nearby expert - all in your own language. Find your local Danfoss website here: danfoss.com.

###### **Danfoss A/S**

Climate Solutions . danfoss.com . +45 7488 2222

Any information, including, but not limited to information on selection of product, its application or use, product design, weight, dimensions, capacity or any other technical data in product manuals, catalogues description, advertisements, etc. and whether made available in writing, orally, electronically, online or via download, shall be considered informative, and is only binding if and to the extent, explicit reference is made in a quotation or order con�rmation. Danfoss cannot accept any responsibility for possible errors in catalogues, brochures, videos and other material. Danfoss reserves the right to alter its products without notice. This also applies to products ordered but not delivered provided that such alterations can be made without changes to form, �t or function of the products. All trademarks in this material are property of Danfoss A/S or Danfoss group companies. Danfoss and the Danfoss logo are trademarks of Danfoss A/S. All rights reserved.

---

## 3. AK-SM 800A series – Installation Guide (engelsk)

*Kilde: Danfoss-dokument AN307930531782en-000301. Montage, forsyning og tilslutninger (relæer, MODBUS, LON/TP78, Ethernet).*

#### **Installation Guide**

### System Manager Type **AK-SM 800A series**

UL file: E31024 61B5

*[Figurtekst: -10 °C < tamb < 50 °C · 14 °F < tamb < 120 °F · 0 – 95% RH, non condensing · IP20]*

Class 2 or LPS in accordance with NEC. For supply connections, use 16 AWG or larger wires rated for at least 75 °C (167 °F). Use copper conducters only. Enclosure rating type 1 FCC ID: X02SPB209A IC ID: 8713A-SPB209A

*[Figurtekst: Panel mount · 43mm · Front side · T 8 · Wall mount · 100 - 240 V AC · Relay 1/2 · Canbus · Ethernet 0 · MODBUS 1/2 · LON / TP78 · T10 · mm · CANbus is not currently activated. · Supply  Relay 1  Relay 2 LON-version · MODBUS 1 MODBUS 2 LON · 100 – 240 V AC · TP 78-version · Canbus · MODBUS 1 MODBUS 2 TP 78 TP 78 TP 78 TP 78 · (Danfoss) (RS485) LON 1 LON 2 LON 3 LON 4 · CAN bus · (for future use) · mm · mm · mm]*

Selve installationen af datakommunikationskablet skal overholde de krav, som er nævnt i dokumentet “Datakommunikation imellem ADAP-KOOL® Køleanlægsstyringer”. Litteraturnummer = RC8AC901.

The actual installation of the data communication cable must comply with the requirements mentioned in the document “Data communication between ADAP-KOOL® Refrigeration controls”. Literature sheet number = RC8AC902.

Beim Verlegen des Datenkommunikationskabels sind die im dokument “Datenkommunikation zwischen ADAP-KOOL® Kälteanlagenregelsysteme“ enthaltenen Anforderungen einzuhalten. Literaturnummer = RC8AC903.

L’installation elle-même du câble de transmission de données doit respecter les contraintes citées dans le document “Transmission de données ADAP-KOOL® Commande d’installation frigorifiques”. Référence documentaire = RC8AC904.

La instalación práctica del cable de comunicación de datos debe cumplir con los requisitos mencionados en el documento “Comunicación de datos entre controles de refrigeración ADAP-KOOL®”. Número de documento = RC8AC907.

*[Figurtekst: Terminering · Termination Out · Terminierung 120 Ω · Terminaison · Terminación · System unit · MODBUS · LON · TP78 · Canbus · Repeater · When all cables have been mounted on the different units, the · cable must be terminated. · A section must be terminated at both ends. The section must · be terminated using either an external resistor or a contact. · Please see the relevant device. · System unit · A repeater will normally terminate two cable sections. · Termination = 120 Ω · The termination should be made with a 120-ohm resistor. (The · resistor can be in the range 100 – 130 ohms.) · A repeater will always terminate two cable sections. · Connectivity · Ethernet WiFi Access point · Ethernet 0 (WAN) Ethernet 1 1. Activate WiFi access point from local screen · (Recessed inside) (Accessible outside) 2. Follow on-screen instructions]*

*[Figurtekst: First time start-up IMPORTANT! · AK-SM 820A · AK-SM 850A · AK-SM 880A · SOFTWARE UPDATE · Address · Adresse 0 = Master · Dirección 1 - 9 = Slave · Method 1: Offline · Initial settings: · Download firmware from · 1. Legal terms ak - sm800a.danfoss.com · 2. Select language for local screen · 3. Set up user · 4. Set Date/time · AK-SM 800 · 5. Select Units · Initial settings wizard · 6. Set Communication · 7. OK and Finish · Method 2: Online · Use software update utility in the web · interface.]*

##### **Statements for the AK-SM 800A**

###### **FCC COMPLIANCE STATEMENT**

CAUTION: Changes or modifications not expressly approved could void your authority to use this equipment This device complies with Part 15 of the FCC Rules. Operation to the following two conditions: (1) This device may not cause harmful interference, and (2) this device must accept any interference received, including interference that may cause undesired operation

###### **INDUSTRY CANADA STATEMENT**

This device complies with Industry Canada license-exempt RSS standard(s). Operation is subject to the following two conditions: (1) this device may not cause interference, and (2) this device must accept any interference, including interference that may cause undesired operation of the device.

Le présent appareil est conforme aux CNR d'Industrie Canada applicables aux appareils radio exempts de licence. L'exploitation est autorisée aux deux conditions suivantes : (1) l'appareil ne doit pas produire de brouillage, et (2) l'utilisateur de l'appareil doit accepter tout brouillage radioélectrique subi, même si le brouillage est susceptible d'en compromettre le fonctionnement.

###### **NOTICE**

###### **FCC COMPLIANT NOTICE**

This equipment has been tested and found to comply with the limits for a Class B digital device, pursuant to part 15 of the FCC Rules. These limits are designed to provide reasonable protection against harmful interference in a residential installation. This equipment generates, uses and can radiate radio frequency energy and, if not installed and used in accordance with the instructions, may cause harmful interference to radio communications. However, there is no guarantee that interference will not occur in a particular installation. If this equipment does cause harmful interference to radio or television reception, which can be determined by turning the equipment off and on, the user is encouraged to try to correct the interference by one or more of the following measures:

- Reorient or relocate the receiving antenna.

- Increase the separation between the equipment and receiver.

- Connect the equipment into an outlet on a circuit different from that to which the receiver is connected.

- Consult the dealer or an experienced radio/TV technician for help.

Modifications: Any modifications made to this device that are not approved by Danfoss may void the authority granted to the user by the FCC to operate this equipment.

Any regulatory related concerns contact: global_approvals@danfoss.com

Danfoss Cooling 11655 Crossroads Circle Baltimore, Maryland 21220 United States of America global_approvals@danfoss.com www.danfoss.com

###### **EU CONFORMITY NOTICE**

Hereby, Danfoss A/S declares that the radio equipment type AK-SM 800A is in compliance with Directive 2014/53/EU. The full text of the EU declaration of conformity is available at the following internet address: www.danfoss.com

Danfoss A/S Nordborgvej 81 6430 Nordborg Denmark global_approvals@danfoss.com www.danfoss.com

###### **DISCLAIMER: Professional Use Only**

This product is not subject to the UK PSTI regulation, as it is for supply to and use only by professionals with the necessary expertise and qualifications. Any misuse or improper handling may result in unintended consequences.

By purchasing or using this product, you acknowledge and accept the professional-use-only nature of its application. Danfoss does not assume any liability for damages, injuries, or adverse consequences (“damage”) resulting from the incorrect or improper use of the product and you agree to indemnify Danfoss for any such damage resulting from your incorrect or improper use of the product.

###### **SUBTEL technical declaration (Chile):**

---
