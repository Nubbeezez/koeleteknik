# Danfoss AK-SM 800 (gammel model) – manual til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.

---

## AK-SM 800 – Quick Setup Guide (engelsk)

*Kilde: Danfoss AK-SM 800 Quick Setup Guide, dok. USCO.PI.R1.H2.02 (filnavn i Danfoss-arkiv: danfoss-ak-sm-850-manual-309509). Gælder den GAMLE AK-SM 800 – ikke AK-SM 800A (820A/850A/880A), som har sin egen fil. Montage, tilslutning, netværk, opsætning.*

**Quick Setup Guide**

### **AK-System Manager**

### AK-SM 800

ADAP-KOOL® Refrigeration Control System

#### **Contents**

|---|

#### **Document History**

#### **Document revision**

|**Document**<br>**Notes**|
|---|
|USCO.PI.R1.H1.02<br>First document release|

#### **Mounting Specifications**

The mounting location should be flat, dry and free of major vibrations. The AK-SM 800 should be mounted at eye level.

**Dimenstions:**

Unit Width 295 mm (11.6”) Unit Height 235 mm (9.3”) Unit Depth 65 mm (2.5”) Mounting holes 246 mm (9.7”) Width Mounting holes 175 mm (6.9”) Height **Operating temperature:** Screen: -10 to +55˚C (14 to 131˚F) @ 90% RH (non condensing) **Electrical range:** ~ 100 - 240 V a.c. (+ / - 10%) 50/60 Hz **Built in alarm relay** 240 V a.c. Class II 3 Amp inductive, 5 Amp. ohmic

**Approvals:** CE IP 20

**USB Access door**

Active USB Flash drive (use for load/save database and AK-SM software)

*[Figurtekst: Active USB Flash drive (use for load/save database and AK-SM software) 65 · Not currently Use d]*

**WARNING: To avoid risk of injury from electric shock, ensure correct electrical isolation is made before working within the enclosure.**

#### **Installation**

**Tools needed** Bubble level Small slotted screwdriver for connector screws Torx 8 screwdriver for releasing the electronic unit  and  for fastening the unit when recessed mounted Screwdriver for fixating the AK-SM 800 Pen for marking the 2 lower fixation holes Larger slotted screwdriver for releasing the Technician lid

**Wall Mounting- box** Attach screw to the wall Mount AK-SM 800 to the screw Loosen Technician lid (three sides) Remove Technician lid Level the AK-SM 800 If drilling is necessary, mark up 2 screws in Connector part. Attach the Connector part to the wall using another 2 screws

**Wall Mounting- wiring** Insert cables through the rubber grommets

Strip the cables

Strip the wires

Secure wires in connectors by screwdriver

Strain relief the cables

Carefully replace the keypad, ensure that it securely snaps into place

###### **Wall Mounting- Panel recessed**

From the front: A hole of the size 280 x 220 mm is machined The AK-SM 800 is inserted in the hole

From the backside: Slide the 3 fastener into the housing part The screws are inserted into the fasteners Secure the unit by tightening the screws

###### Remove Technician lid

From the back, push cables inside the housing

Strip the cables

Strip the wires

Secure wires in connectors by screwdriver

Strain relief the cables

Carefully replace the keypad, ensure that it securely snaps into place

#### **Connections**

The following chapter describes the available connections on your AK-SM 800.

Please note that not all connection points are currently active, please refer to the drawing below for more details

*[Figurtekst: not currently  not currently · used used · Modbus field · bus · Power Supply Alarm relay Boot switch Address swicth Lon (RS485) · (used to place unit in  (used when configuring  field bus · boot loader mode) multiple SM units]*

RJ 45 LAN, Use shielded Ethernet cable

#### **Network topology**

Your AK-SM supports both Modbus and Lon RS485 local bus connections.  For further detailed description of network connections please refer to document ‘ **Data Communication between ADAP-KOOL® Refrigeration controllers_RC8AC602** ’

###### **Lon RS485**

Follow standard topology guidelines for Lon RS485, with particular respect to maximum cable length, when to use a repeater and ensuring suitable resistors are in place.

When using the Lon RS485 network, ensure the Term. Switch on the AK-SM is in the ‘ON’ position (enable internal resistor).  Any repeaters must also have 120Ohm resistor in place.  Finally, ensure that the last controller on the network run also has its end of line on line resistor enabled.

###### **Cable type**

Cables twisted in pairs must be used, and they may be provided with a screen. Some types of communication require a cable with a screen to be used.  The conductor’s cross section must be at least 0.60 mm.  Examples of cable types:

Belden 7701NH, single-thread 1 x 2 x 0.65 mm, without screen Belden 7702NH, single-thread 2 x 2 x 0.65 mm, without screen Belden 7703NH, single-thread 1 x 2 x 0.65 mm, with screen Belden 7704NH, single-thread 2 x 2 x 0.65 mm, with screen LAPP UNITRONIC Li2YCY (TP), multi-thread 2 x 2 x 0.65 mm, with

###### screen

Dätwyler Uninet 3002 4P, single-thread 4 x 2 x 0.6 mm, with screen

###### Cable length

A cable length must not exceed 1200m (4000 foot).  A repeater (Part # 084B2241 ) must be used for longer lengths.

###### **Lon RS485 Topology**

The cable connection must be connected from controller to controller, and no branches are allowed on the cable.  If the cable length exceeds 1200 m a repeater must be inserted.  If the data communication cable runs through an electrically noisy environment which impairs the data signal, one or more repeaters must be added to stabilise the signal.

When configuring Lon devices on the control bus, the highest device address that can be can be used is 127 (max. 120 controller in total)

###### **Conductors**

The two wires are looped from device to device. There are no polarisation requirements. (On some controllers, the clamps are designated A and B. On others there is no designation. Otherwise the connections are identical.)  If a screen is used, it must be connected to the system device and any repeaters.  A screen must always be looped from device to device.

The screen must not be connected to anything else.

(The screen is earthed inside the screen and must not be earthed in any other way.)

###### Modbus topology

The cable must be with screen.  The cable is connected from controller to controller, and no branches are allowed on the cable. If the cable length exceeds 1200 m a repeater must be inserted One repeater must be added for every 32 controllers.  If the data communication cable runs through an electrically  noisy environment which impairs the data signal, one or more repeaters must be added to stabilise the signal.

When configuring Modbus devices on the control bus, the highest device address that can be used is 127 (max. 120 controller in total)

The wires are looped from device to device. A is connected to A B is connected to B.

The screen must be connected to the system device, all controller and any repeaters.

A screen must always be looped from device to device. The screen must not be connected to anything else.

*[Figurtekst: AK-SM · 32 32 · AK-SM]*

#### **Remote Management Tool (RMT)**

The Remote Management Tool (RMT) is a PC software application tool that is designed to support the AK-SM, both in commissioning and service.  The RMT is a powerful tool that allows full offline programming and simulation of AK-SM databases, providing the opportunity to save considerable on site commissioning times. In addition, the RMT tool has various remote management features, facilitating complete system management.  Creating custom images for the AK-SM web browser is also another function of the RMT tool.  The following features can be seen in the RMT;

- **Offline web Programming**

   - Launch offline web simulator(s) to allow full offline AK-SM database programming, with controller simulation you can fully pre-program your application and save the resulting database to USB for on site install.

- **Program simulation** From within the web browser session simulate board and point variables to test calculations and system behaviour

- **Custom Graphics**

Use your own Jpeg or bitmap file to crate custom images, mapped with any configured system data point

- **F TP** (File Transfer Protocol) Remotely connect, load and access system files (html web & EDF device files) Retrieve data points

- **Address Book**

Save your most commonly connected site details to allow for one click connection

- **Tools**

Download System software, backup (save) & load database files.

- **Language**

Compatible in multi- languages

The RMT tool is available from your Danfoss sales office with associated supporting documentation.

###### Required IP ports

As the AK-SM uses IP networking standards to create remote access  it may be necessary to configure any site routers to allow incoming connections, either from a LAN or WAN view.  The figure below shows a simple IP connection with the AK-SM connected to a standard network router with a typical factory IP address range. From within the LAN any remote connections should ‘point’ to the master IP address of the AK-SM, in this example http://192.168.1.100.  If however the remote connection is on a WAN then the LAN router may need to be configured to allow this inbound connection, with the addition of the web port added tot he end of the http sting.

Please refer to the port allocation table below  for remote IP connections

**Master IP 192.168.1.100** Default Gateway 192.168.1.1 Network Mask 255.255.255.0 _(AK-SM factory set http port = 80)_

LAN Network Router IP 192.168.1.1

LAN Network Router WAN IP 172.28.6.108

#### **AK-SM**

For WAN access port forwarding is required

1. The port number is required to be typed into the URL address ONLY if the web port is NOT configured as 80.  For example, if the port number is configured as 8080, then Computer A needs to type in **_http://192.168.1.100:8080_** , while Computer B needs to type in **_http://172.68.6.108:8080_** to access the website of the unit.

2. If the port number is defined as default number 80, then it is not necessary to type in “:80” in the URL address, this is because the HTTP protocol uses 80 as default port. If  the router port forwarding is correctly configured, it is not required in WAN access either.

Computer A type ‘http://192.168.1.100’ to access AK-SM

*[Figurtekst: Computer B · type ‘http://172.28.6.108 to access AK-SM]*

Port allocation table

|**IP Port**||**Use**|**Notes**|
|---|---|---|---|
|||**- LAN side -**||
|80|web browser||Thisport is user configurable but factoryset to 80|
|21|RMT tool||Thisport is user configurable but factoryset to 21|
|25|e-mail||e-mail output|
|3001|XML||Used for XML communications|

###### **Notes for FTP port forwarding in AK-SM units**

In AK-SM units, FTP service is a convenient way to download/ upload files and updating database/code. **Open FTP server ports to the public internet is not considered as a safe network practice.  To avoid these issues, Danfoss strongly suggests FTP functionality in LAN network only .  This would reduce the risk of open FTP ports and enhance network security.   However, to make the FTP work on WAN side, it must have configured FTP server port opened and forwarded to the public internet.**

#### **Initial Configuration - language**

The following section describes the recommended actions to get your AK-SM up and running.

###### **Local keypad - button layout**

*[Figurtekst: Home · (System View) Menu Alarms Configuration · Escape · Numeric keypad · Back  Shift · Previous  Page Up  Menu Navigation · Next Page Down]*

###### **Setting language for local SM display**

**Your AK-SM can display several different languages.  The factory default the unit will display English, in addition your required language can also be enabled.  Follow the simple steps below to display your preferred language in the local screen;**

- **1/ Press the Configuration button, and if required enter the factory default user name and password (Supervisor, 12345)**

- **2/ Using the arrow keys, navigate to the ‘System’ memu.**

- **3/ Using the down arrow, navigate to the Language line and select your required language**

- **4/ Select your language for ‘Display’.  The unit will then request a re-set.**

Select language

Display language

#### **Initial Configuration - Wizard**

The following section describes the current Web Wizards, used for simplifying initial settings and Refrigeration layout.  The Web Wizards can be used in an offline or online configuration. Danfoss recommends using the AK-SM web environment for commission tasks.

Establish a web connection to your AK-SM (if working online, enter the valid IP address of the AK-SM and apply the factory user name and password).  Navigate to the **Configuration** menu

Web Wizard Navigation

Back          Close                            Progress   Forward

**Preferences Wizard** (Language, store names, units, preferences, time, date, daylight savings)

- 1/ To easily configure your units preferences, launch the Preferences wizard.  Use the Wizard navigation controls to move thought the Wizard screens.

- 2/ To make changes, double click on the relevant line and continue until the final screen.

- 3/ Press the finish button to complete and close the wizard (return to main wizard screen)

**Users Wizard** (Create, modify users, user groups, authorization levels)

- 1/  Enter number of users required (max 22), set password and browser language for each user

- 2/ Enter the number of authorization types (max 7), against the settings line double click to modify the scope of system access

- 3/ Press the Finish button to complete the Web Wizard

**Licensing Wizard** (Enter new license functionality) Not currently used

**Refrigeration layout Wizard** (used to define your refrigeration layout, grouping case with packs, forming associations) One of the main features of the refrigeration layout wizard allows the user to make use of a network scan.  The principle is that the wizard is initially used to initiate a network scan, discover and list what is found.  This discovery is then used to easily define the Pack and Case controller relationships (suction groups).  The wizard allows for easy drag and drop association, the net result is that once completed the refrigeration layout is built in the AK-SM. The Refrigeration layout Wizard can be used during a live connection to your AK-SM or can be used when programming offline.

limitations:  Whilst the wizard will layout the Pack and Case relationships, further controller configuration may be required. Refer to section 6 under ‘ Configuration’ for guidance on any remaining configuration areas required.  Currently the wizard is intended for  Pack and Case devices, any controls not designated as such will have to be configured using traditional config methods (see Configuration section).

Open the Refrigeration layout wizard and follow the described steps, each step has some description for the available actions. The following wizard screens are available in sequential order; **Network** (select and perform network scan) **Discovery** (list scanned devices) **Compressors** (Input Pack controller name, view address, model, add, copy, remove) **Circuits** (Input Evaporator controller name, view address, model, add, copy, remove) **Suction Group mapping** (Drag and drop your evap controllers under each pack) **Summary** (view your groupings before finishing wizard and thus processing your selections to the AK-SM)

After the relevant networks have been selected an scanned the ‘Discovery’ screen will show all detected devices.  Once satisfied with the correct content press the forward button to continue the wizard.

The ‘Compressors’ screen allows for custom text input.  If working offline (programming a database not being connected to a AK-SM) the Add, Copy and Remove buttons can be used.

Double click the ‘Name’ line to enter a custom description for the device.  Pressing return will automatically focus on the next device name in the list.

Use the Add button when creating offline nodes.  Double click the ‘model’ line to bring up a selection of nodes

If your scanned list has known devices that are standalone (not associated with a Pack) these must be mapped under ‘No Compressor’.  Manually add a new compressor and double click the model line and select ‘No Compressor’.  When the final wizard screen is presented any standalone controls can be mapped under this ‘No Compressor’ group.

The ‘Circuits’ screen follows the same principle as the Compressors screen.

The ‘Suction group mapping’ screen allows for the defined evaporator devices to be ‘mapped’ under the required Pack controller.  This mapping forms a relationship or grouping between the pack and the evaporator devices.  This grouping association will then be seen in the AK-SM configuration and dashboard screens (and can be used to easily set up master control functions like Suction optimization).

As the user description indicates, use a drag and drop action to group your controls.  Use the CTRL key and multi-select cases to save time when making bulk actions.  You can remove any case devices by simply dragging back to the available case list.

The check box labelled ‘Allow multi-case circuit creation’ is to support Centralized refrigeration control configuration, where multiple case circuits are available’.  Leave this check box empty if you are using a de-centralized control strategy (i.e. Case and pack controllers)

Once satisfied with the mapping, press the forward button and the summary screen will be shown.  Pressing the finish button will then send your configuration layout to the AK-SM.  During this time a progress bar will be shown and finally a status dialogue box.

This completed wizard process will layout your refrigeration application.  Typically some additional configuration tasks will then need to be completed (i.e. define alarms, setpoint changes, configure history), please refer to the following section for further details on detailed configuration.

#### **Configuration**

The following section describes the typical steps required for commissioning and configuration of your AK-SM.  Although site applications can differ from one site to another, many setup procedures are common.  This setup section assumes the AK-SM is mounted and all necessary power, network cabling and controllers are in place.  The described work flow is based around the AK-SM web browser interface, but would equally apply if being done via the local screen.  Further detailed commissioning instructions are found though out this user guide.

The AK-SM offers unique control flexibility in that both centralized and de-centralized control methods are supported.  The term ‘centralized’ is used to describe the control of refrigeration Racks via I/O (Danfoss Input / Output modules).  Under this method of control the refrigeration control is managed directly from the front end (AK-SM), with field bus I/O.  De-centralized control is the term used to describe the full support of Danfoss Pack and Case controllers.  Under this method, each Pack or Case controller on the network can be seen as self contained, with control logic built in.  The front end (AK-SM) under this type of application is more of a network manager, providing full read / write access and energy saving functions.

###### **De-Centralized**

When configuring your application, have in mind which control strategy you wish to utilise.

###### **Centralized**

Pack & Case

Rack I/O

When starting your system configuration you will have the opportunity to select either Centralized or De-centralized (or a mix of both) control methods.

The following areas of system configuration will be covered in this section;

- 1 **Network Nodes** (Network scan/ Node overview, Points, scan /config status, duplicates, upload/download)

- 2 **Time** (Set time/date, time zone, operating Hours, Daylight savings, Holidays) 3 **System** (Store / Region Names, Units preferences, Authorization levels and users) 4 **Communication** (DNS, DHCP, IP Ports) 5 **Alarms** (XML, e-mail, Routing) 6 **Control (** Configure Refrigeration, Lighting, Miscellaneous, Energy meters and Gas detection)

Once successfully logged into the AK-SM (web) and assuming you have the required authorization, system configuration is done via the central ‘ **Configuration tab** ’.  Clicking this tab reveals the configuration ‘sub tabs’.  Depending on your selection, these sub tabs will change dependent on content. Using the menu structure seen in the ‘Configuration’ page, a step by step process can be applied when setting up your AK-SM.

_Navigation ‘bread-crumb’_

_Central configuration menu_

###### **Network Nodes** 1

If your application already has controllers and/or I/O modules set and powered you may wish to perform a network scan to validate their connection to the AK-SM.  Follow this section to perform a network scan

From the Configuration tab select the ‘ **Network Nodes** ’ sub-tab. When your field network is complete and all controllers are on line a network scan can be initiated.  The operation of a network scan allows the AK-SM to be aware of any controller devices on the network, allowing the AK-SM to communicate and function with the controllers on the field bus.

###### **Duplicates Tab**

Use this screens to perform network scan

**Relays | Sensors | On/Off | Variable Output**

‘Use this screens to view status of your assets (Online)

This tab relates to any AK I/O configured points, the term **_points_** relates to AK I/O relay, sensors, On/Off Inputs and variable outputs.  Any control questions that have required AK I/O control will be seen in these tabs.  The purpose of these tabs is to allow the viewing of the I/O point status.

###### **All nodes | Controllers | I/O boards | Other nodes**

The scan status menu/tabs allows the user to view any scanned nodes found on the network. **All Nodes:** Central list will display configured devices and points. Only configured controllers will be visible in this list. **Controllers:** view any scanned generic controllers.  This screen will also reflect address and controller type **I/O Boards:** Display AK Board & Point status. **Other Nodes:** List of other nodes

Ensure the appropriate network channel is selected,  and press the ‘complete rescan’ line.  The AK-SM will now scan the network to identify any connected and addressed controller nodes.  The text on the screen will reflect the scan progress, after a scan the time & date will be shown (indicating last scan) For SLV support, select Modbus channel

Check this list to make sure no two devices have been assigned the same network address.  Any duplicate address will be shown in this list.  Correct any address issues and re-scan.

###### **Upload Tab**

The upload tab will list any controllers that have been uploaded. The upload function can be performed in the Configuration>Control area (one controller at a time) or here (multiple devices with one command).  The process of an upload takes the current parameter settings and values from the controller(s) and loads them into the AK-SM database.  This operation ensures that the AK-SM database is synchronised with any pre-configured controllers  on the control network.  Any upload failure will be shown on this screen, else a time / date stamp will be shown when successful

###### **Download Tab**

The download tab will list any controllers that have been processed for download (where the AK-SM sends parameter data to the device).  The download function can be performed individually under the Configuration->Control page or here, where multiple controllers can be selected for download (using one command).  The process of a download takes the AK-SM database values and downloads them to the selected controller(s).   Any upload failure will be shown on this screen, else a time / date stamp will be shown

After the network scan has completed, any resulting count will be seen against the **Nodes Scanned on Network** line - this reflects the number of found nodes on the scan just completed.  The corresponding line below ( **Nodes configured in database** ) reflects the current total of  network nodes actually configured in the AK-SM database.

The last group in this table refers to the following node types;

OI (Output|Input) RO (Relay output) SI (Sensor Input) V02 (Variable output) Utility Meter (WattNode, Veris, Carlo Garvazzi) Generic (Danfoss case / pack controllers) AK-CM (AK- Communication Modules) Calculations

Each node (type) has a column that reflects any configured or scanned status.

2 **System configuration (Time settings / preferences)**

The Time tab allows the **_system time, time zone, operating hours, daylight savings and holidays_** to be configured.  Double click a line to make any changes.

The following examples can be seen for the time zone;

London (GMT) = 000

Central Europe = 100

East Coast USA = -500

The operating hours can be set that reflect your store operating hours.  Any times set in this section can then be referenced to via a ‘Relative schedule’ .  Relative schedules are found under the ‘Lighting’ and ‘HVAC’ application areas and apply a (user selectable) offset which references the operating hours schedule.

3 **System configuration (Time settings / preferences)**

After completing the required settings in the ‘time’ tab, navigate to the ‘system’ tab.  Under the system tab add the store name and region / preference setting and information.

The system report screen allows the user to define what content should be included. Alarms, Schedules, scanned devices, Audit trail and controller database are available options. To generate a system report go the main web menu and select File/Download Report

The Auth (Authorization) Levels tab allows the definition of up to 7 authorization types.  Custom authorization types can be configured with certain system privileges / access.  In the example below, 4 auth levels have been defined (factory setting is 3).  Level 1 (Supervisor) cannot have the settings changed.  To change the level of access of other auth levels, navigate to the desired line and select from the Authorization pop up dialog box. As factory standard, 3 levels are predefined (Supervisor, Service, Daily User), the service and daily user levels can be changed as required.

To add/delete auth levels select the ‘Number of authorization types’ line (max 7 levels)

The Supervisor name can be changed but the level of access / privileges are factory set.

Adding new auth levels allows new users to have specific access to key system areas.  Once new auth types have been created, enter custom name and define level of access by selecting the Settings line (Authorization pop up box will appear)

The following areas of authorization are available;

###### **<u>Configuration</u>**

**System:** Access to the System tab **Authorization:** Access to the Authorization tab **Refrigeration:** Access to Refrigeration configuration **HVAC:** Access to HVAC configuration **Lighting:** Access to Lighting configuration **Miscellaneous:** Access to Misc configuration **Schedules:** Access to Schedule configuration **Calculations:** Access to Calculations configuration

###### **<u>Manual Operation (seen under Service tab in device detail page)</u>**

**Refrigeration:** Allow user to perform the following operations on Danfoss case controllers ;

Main Switch, Defrost, Cleaning, Lights, Night Setback, Shutdown **HVAC:** Allow user to perform the following operations to Relay, Inputs & sensor overrides

**Lighting:** Allow user to perform the following operations -override relay **Miscellaneous:** Allow user to perform the following operations -override relay, sensor inputs **<u>Alarms</u> Configuration:** Allow user to configure alarms **Routing:** Access to the alarm routing **Acknowledge:** Allow user to acknowledge **Clear:** Allow user to clear alarms **Log:** Allow user to set alarm level to log

###### **<u>Other</u>**

**Main Menu:** Allow user to access main menu **Device History:** Allow user to access device history **Use Menu:** Allow access to Menu function **Use USB:** Allow use of USB flash **Rescan Network:** Allow user to rescan network

###### **Users tab**

The next tab (user tab) allows the definition of up to 20 users.  A custom name and password can be given for each user.  The appropriate level (defined in Auth Level tab) can be assigned to each user.  The AK-SM always maintains a single user in the system profile and this level is factory set to the Supervisor level. To add users simply enter the required value in the **_‘number of users’_** line.  The Browser language line reflects what language will be displayed in the web browser upon this user logging on [via browser access].

To add users select the ‘Number of users’ and enter required number Enter custom name, password and auth level for user. Browser Language:  This defines the language that will be displayed when the user log on via the web browser access.

**Communication** 4

The Comm (Communications) screen allows for IP network settings to be configured.  Follow the question lines on the screen to configure your AK-SM according to site requirements.  Any changes in IP configuration will require an AK-SM system reset.

Select ‘Yes’ if a DNS service is to be used.  Prefered host name can be entered if setup in router config Select ‘Yes’ if AK-SM is to be connected to a DHCP server Select yes and manually enter the IP address that the AK-SM will use if DHCP fails.

Master IP address - if using multiple AK-SM controllers in a host network, enter the Master (unit address 0) IP address

Internet IP address - Specify public IP address which is used to contact your AK-SM via an Internet based connection.  Factory web (HTTP) port is 80 & FTP port is 20 and 21, both can be changed to suit your network application.

If your network supports NTP, select ‘yes’ to the question ‘Network timing support?’

The Alarms screen has a sub set of screen [Connections, Service, Alarm Routing, Relays, System, I/O Comm].  Go through each sub tab to ensure all areas are correctly configured as per site requirements.

**Connections screen** - Define the number of connections, then select the connection type.  Your AK-SM can offer the following alarm IP based alarm output;

e-mail, Remote (Danfoss Electronic delivered services) and XML. Depending on your configuration the screen will reflect the required inputs in order to satisfy the output.  In order for any alarms to be routed out of your AK-SM please ensure a schedule is configured.  Failure to set a schedule will inhibit any alarm output.

To configure a netwrok connection select ‘Number of network connections’ Type (e-mail | Remote | XML) Ensure a schedule is defined to allow alarm ouput

Example of e-mail configuration

Enter valid server name (or IP) for e-mail server If your e-mail service requires user authorization, enter user name and password Send to: Add the e-mail address for intended recipients Reply to:           A mandatory field that must have a valid entry (address with same domain name).  An abbreviated message would have reduced text in the alarm message Configure a schedule to enable the alarm e-mail output **3G Wireless routers** 3G technology offers many benefits over standard dial up connections.  Utilizing a 3G connection the full range of AK-SM services can be used, including web browser, and RMT.  Where Internet / Intranet connection is not available, Danfoss recommends considering 3G as a means of offering IP connectivity. Please consult your local Danfoss sales office with regard to 3G connectivity.

###### **Service tab**

Use the service screen to send test alarms.  You may configure the alarm type and alarm action logic (1-8).  In addition, scheduled or repeat test alarms can be configured on this screen.   The internal alarm relay cam also be tested from this screen. **Disabled** = No alarms will activate on this point **Log Only** = When an alarm occurs on this alarm point it will only register in the AK-SM alarm log - no physical alarm output **Normal** =  When alarm is active the output will be sent once (alarm may get re-triggered if the stop condition is set for repeat) **Severe** = When alarm is active the output will get re-sent every xx min

**Critical** = Same as Severe but with separate re-trigger time - when alarm is active the output will get re-sent every xx min **Delete** = Removes any applied alarm settings

###### **Routing tab**

Select Alarm Action type (defined under Alarm routing)

Auto Test:

Scheduled:  Configure days & time for test alarm Repeated:  Configure interval time for test alarm

Suspend alarms generation (suspend All alarms in the system from being sent):  Set time period (min/Hrs) to stop alarms being sent

Any relays configured for alarm output can be forced on / off for testing purposes.

Remember to leave in Auto position after testing

The AK-SM utilizes an Alarm Action Matrix that allows a high degree of flexibility for various alarm routing options. At the heart of the alarm configuration is the ‘ **Alarm Routing** ’ page, where different routing options can be defined, along with time delays and alarm output stop conditions.

The central alarm action matrix allows various output options (known as alarm **_actions_** ) and alarm handling configuration to be centrally assigned.  Once the alarm action matrix has been defined, any controller or I/O point can be given an alarm **_action_** number. The alarm **_action_** number corresponds to the appropriate output. (as defined in the alarm routing page).  Alarm output options include;

- 5 external (AK I/O) relay outputs

- Local AK-SM buzzer

- Local AK-SM front LED

- Internal alarm relay

- 2 Network connections

- 6 IP / e-mail addresses

- Serial printer output.

The following example can be seen as a guide to configuring your AK-SM alarm logic options;

To configure an alarm action, navigate to the required output line (I.E. Relay A) and press enter.  The resulting screen allows the configuration of the alarm actions, any pre delays, duration times and stop conditions.   The results of this configuration will be shown in the alarm routing page.

###### **Alarm Actions (1-8)**

Up to 8 alarm actions can be defined.  Each alarm action can have multiple outputs, making the AK-SM alarm output options very flexible.  ‘Look down’ each alarm action number column and any associated outputs will be seen in the left hand column

###### **Component Column (alarm output)**

Select from the options seen in this column;

###### **Delay**

Once an alarm action is defined the associated time delay for the action can be set.  This delay is in addition to any delay already defined in any controller (i.e. EKC) or monitoring points (i.e. I/O) defined in the system.

- Relay A-E

- Front LED

- Buzzer

- Int. Relay

- Network 1

- Network 2

###### **Duration**

A duration time is available when either Time or Time/Repeat are selected as stop conditions. The duration setting defines the length of time the alarm output will be active for (irrespective if the alarm is still active or acknowledged or not) Available in second or minute selections.  0 Sec/Min duration will result in the alarm output remaining off. Min = 0 Sec/Min Max = 99 Sec/Min

###### **Stop**

The stop condition defines when the alarm output will stop or return to configured position.  The following definitions apply; **Time** = Stop on time (set under duration) **Ack** = Stop on alarm being acknowledged **Clear** = Stop when alarm clears **Time/Rep** = Stop after time delay but repeat if alarm is still active **Ack/Rep** = Stop after alarm is acknowledged. If alarm still active after acknowledge repeat alarm action (repeat

###### **Example configuration**

This example will describe the steps to configure an alarm actions.  Alarm action **1** will be defined according to the following;

- **Relay A** should trigger after a 10 second pre delay.  This relay will energize any time and will only reset when the alarm clears.

- **The Front LED** should activate (de-activate LED when alarm clears)

- **The Buzzer** should only activate during the Day (Buzzer stops when alarm is Acknowledged)

- Alarm message should also be sent out via **e-mail**

The above alarm outputs are associated with action 1 - ‘look down’ the alarm action 1 column and the relevant outputs can be seen in the left of the page. To define the alarm output options navigate down the page and double click the relevant line.

This opens another page that allows the configuration for that output to be set.  In the example below **Relay A** and the **Buzzer** can be seen.  Follow the same process for the other outputs.  For e-mail output, navigate to the Network 1 line and press enter.  Here, set the action, time delay & stop conditions.  (The actual e-mail configuration is done in the Alarm ‘Connections’ page).

_‘Look down’ Alarm action 1 column_

The results of the alarm output configuration can be seen in the central Alarm Routing page.   Follow this process for other actions. _Relay A Configuration page_

###### **Action settings:**

Once in the actual output page, navigate through the lines and set the relevant Action.  Each action can have the following settings;

**Not Selected:** No action **Enabled:** Will enable this output action (any time of day) **Day:** Enable this output during day status (based on store opening times (Configuration->Time) **Night:** Enable this output during night status (based on time **Delay, Units & Stop settings:** outside of store opening times (Configuration->Time) To complete the output configuration set the time delay, units & stop conditions should be set.  Stop conditions;

**Time** = Stop on time (set under duration) **Ack** = Stop on alarm being acknowledged **Clear** = Stop when alarm clears **Time/Rep** = Stop after time delay but repeat if alarm is still active **Ack/Rep** = Stop after alarm is acknowledged. If alarm still active active after acknowledge repeat

###### **Relay tab**

If the alarm output includes relay(s) the **Relays** tab should be accessed to configure the board & point address for these relays. The example below shows relay A & C, with the associated (AK I/O) board & point address.

Enter the AK I/O board & point location for the relay(s)

Select N-Open / N-Closed as required

###### **System tab**

AK-SM system based alarm conditions should be set under the **System** tab.  The alarms seen in this page are factory set but can be changed as per site requirements.  Navigate down each line and configure (pressing the enter key) as required.  The following items can be seen and changed under the System tab;

**I/O Network Fail:** Alarm if communications to AK I/O fails **Flash Memory fail:** Alarm if AK-SM system memory fails **Database Cleared:** Alarm if AK-SM database is cleared **File Error:** Alarm if critical files do not load / not present on AK-SM system (I.E. Device list missing) **Alarm send fail:** Alarm if any active alarms were unable to be sent out

**NTP Failure:** Alarm if the network time protocol fails Host Comm: Alarm If host communication fails Host Count: Alarm if one or more AK-SM units disconnect from host netwok

Ram Disk Full: Alert alarm if Ram is getting full (due to EDF files)

Factory settings can be changed as per customer requirements.

Alarm level & Actions can be changed

###### **I/O Comm tab**

If Controllers (Danfoss Evap & Pack, Power meters) and, I/O has been used in the control configuration (Lighting, HVAC, Refrigeration etc.), these devices can be seen under the I/O Comm tab.

The I/O Comm tab allows any offline communication alarms to be configured.  The example below shows an evaporator controller (address 1) with the alarm level set to ‘Normal’ & alarm action ‘1’. These factory settings can be changed in this page.

Any AK I/O points used in the AK-SM system can be found on this page, with the associated alarm level and actions set.  The factory settings can be changed as required.

###### Calculations & Other

If any calculations have been defined in the AK-SM system, alarms can be associated with these.  Use the Calculations tab to set appropriate alarm levels and actions.

###### 6 **Control tab**

The control tab is the central configuration page for your control requirements.  It lays out the different application areas and allows the Commissioning Engineer to define what applications are on site.  Once the application areas are defined on this page, more detailed commissioning is done in the dedicated application tabs (covered in following section).  Note that depending on your license version, different applications may be visable (or not). Please also note that the SM provides the ability to configure centralized or de-centralized control. **Centralized** control is where your SM has the control logic built in and uses Danfoss I/O to provide refrigeration control. **De-centralized** is the control method via the use of Danfoss Pack and case controllers

For centralized control, ensure the control type is set to IO (input/Output).  This alerts the SM that you wish to use Danfoss Board and Point configuration for your refrigeration application

For de-centralized control, ensure the control type is set to your required controller type (via drop down menu)

###### **De-Centralized**

**Centralized**

Pack & Case

Rack I/O

###### **Number of Racks  / Packs (max 12):**

###### **Show only scanned devices:**

Enter the required amount of suction groups.

Select ‘yes’ if your controller devices are already on the network, with valid addresses and connected to the AK-SM.  By setting to ‘yes’ and after a network scan (covered in next section) only discovered devices will be shown in the drop down boxes.  If your controllers are not yet on the network, keep this selection to no.

**Rack type** (Use I/O selection for centralized control, select controller type if using de-centralized)

**AK IO** = built in control via AK I/O **No Compressor** = No Compressor control **Device selection** = select required controller _Note: Variable Speed can be selected as a pack controller._

**Suction groups** (Suction group or Evaporator control)

Add your required quantity of suctions groups (centralized logic) OR enter how many evaporator controls are available under your Pack (de-centralized)

_Note:  suction group / evap configuration is then done under the Refrigeration tab_

The following screen shots below represent an example of de-centralized configuration (Pack and Case control). The AK-SM has been configured for two pack controllers (AK-PC 730 and the AK-PC 840), with 5 Evaporator controllers under each pack.   Selection for each Pack controller was made via the pop up box that appears when the Rack line is double clicked.

Double click to select your required Pack device

Once the Pack controllers have been defined and the number of case controllers under each pack have been set, continue to the Refrigeration tab for detailed configuration.

First, navigate to the ‘Address’ tab.  Enter a valid network address, corresponding to the address already set in the field controllers.

**Note:** If your field controllers have already been configured with the relevant parameters set, you may wish to perform an ‘Upload’. This function forces the AK-SM to pull back the controller settings and thus synchronize the AK-SM database.  Only use the ‘Download’ function if you have finished controller configuration on the AK-SM and you wish then to send these settings ‘down’ to the controller.

A one click option for this (upload/download) can be found under the Configuration->Network Nodes tab

Set a custom name for your control devices

Enter address that matches the physical address in the pack and case controllers

_See above note about Download / Upload_

Once all the addresses and custom naming is complete escape out of the addresses menu and navigate to the ‘Suction’ tab.  This will allow for configuration of the Pack Controller(s).  Use the drop down (Suction) menu to access each Pack controller and the corresponding menus.   Please note that any online controller devices will invoke a dialogue box which asks if you wish to retrieve the data from this controller.  This dialogue box is intended to direct the choice of either uploading data from a controller (overwriting any previous settings held in the AK-SM database) or not.  If you have existing controllers on the network which have already been configured, choose the upload option (this need only be done once for each controller you view).

Controller menu selection.  Use this drop down list to access the different controller menus.

Controller parameters, to modify or change double click line and press the enter key.  The new value will be sent to the controller*

*Controller must be online *Some controller types require the main switch (R12 parameter) to be off before certain changes can be made

When to use Upload / Download function: The AK-SM holds a database in which all the system configuration is held.  This includes any actual controller devices connected or just devices that have been selected ready for configuration.  It is important to recognise when to perform an upload or download function so that any preset configuration is not overwritten by automatic upload by the AK-SM.

###### **Upload**

This function may be required where the case and pack controllers have already been configured and all parameters are set according to customer specifications.  In this instance the need is to typically perform an upload function, thus updating the AK-SM database to fully reflect the controllers commissioned settings. Once this has been done, changes to the controller settings can be done directly from the AK-SM.

###### **Download**

The opposite to this would be where the controller devices have not been set per customer specification and the AK-SM should be used as the commissioning tool or window into the controllers. By navigating through all the controller screens in the AK-SM it is possible to configure the controller parameters and then send these setting to the connected controllers via the download function.

###### **Copy function**

To aid the commissioning process, the AK-SM offers a settings copy function which can be used to copy one device settings and alarm configuration to other (similar) device(s).  This function works when copying settings to and from same controller version / type devices.  The procedure described below is one example of the copy /paste function.

Use the Copy tab to open the copy page, where any same controller type devices can be copied to.  The actual device page will act as the copy base, so ensure the correct circuit is selected (in the drop down list).  Select **all** or **individual** controllers that will be copied to, then press the copy to line.

- The copy function copies controller parameters etc from once device to the AK-SM database, to complete the operation the (copied) settings need to be **_downloaded_** to the required controllers.

The Global download function can be seen under the Network Nodes -> Download section

###### **Import SI | OI function**

Use the **Import SI (Sensor Input)** and **Import OI (On/Iff)** function to gain access to ‘generic’ controller (Evap & Pack) parameters that are normally not accessible for alarm / logging / Boolean use. This function can be used to alarm on specific parameters not in the factory alarm list and / or can be used to import controller parameters in the Boolean logic calculator.  Up to sixteen points can be selected per controller.  This function extends the flexibility of controller support in the AK-SM and opens up the generic controllers parameter list for more customer specific needs.  The following steps highlight the procedure in ‘Importing’

From the import page(s) double click an import line to present a pop up box that shows all available parameters.  Select the parameter that you wish to ‘import’ from the controller (you may give it a custom name).

In the example below, the parameter Po Set point has been selected.  This parameter can now be seen in the miscellaneous calculator.

###### **Extended Config function**

Extended configuration (changing what parameter is seen in the System View, Dashboard & Device detail status) Using the extended configuration tab the factory standard parameter that is used for ‘System View’ status can be changed. This feature is useful in giving the end user more flexibility in showing the relevant sensor at the system and device detail views. By changing the **_overview value_** the AK-SM will then display the new selected parameter or status in the system view, Dashboard and device detail pages.

###### **Alarms and Alarm Select**

Use the Alarm tab to define the alarm actions associated with this device.  Use the Alarm select tab to select  up to 300 alarm points (max 300 per AK-PC controller)

###### **Configuration -> HISTORY**

The AK-SM history section allows the collection and recording of control parameters, values and status.  The central history function allows up to 600 ‘points’ to be configured, a point being a temperature, pressure, status, relay, etc.  The collection of history allows further analysis using the AK-SM or remote web browser, where a graphical representation of this data can be made.

To configure history, navigate to the Setup tab (Configuration>History).  The following setup lines are visible; **Auto Configure History:** Use this function to auto select typical points needed for logging (the AK-SM will select key points in the Refrigeration, HVAC, Lighting and Misc control areas.  Manual configuration can be done to override these selections or add more as required. **Clear History Configuration:** Use this function to clear history configuration (points selected for history & the frequency of samples)

**Clear History log:** Use this function to clear stored history in the AK-SM

**Start / Suspend History:** Once the relevant points have been selected for history collection (using either the Auto history, manual or a combination of both) press this line to Start the collection.  Press again to Stop collection **Status:** Displays the current status of history collection (Collecting or Suspended)

**No of Configured datapoints:** Displays the number of configured history points (max 600)

Note:  Ensure the correct time & date are set in the AK-SM.  Make sure the history collection function is running to ensure the collection of datapoints.  Use the ‘ **Start History** ’ line and check that the status reflects ‘ **Collecting’**

Auto Configure History

When selecting the auto configure history function the AK-SM presents the option to select the history collection sample rate.

These can be later changed & modified under the relevant history device type (Controllers/Relays/ Sensors/On/Off/Variable/Other)

###### **Configuration -> HISTORY** Controllers

If any controllers are configured for history collection, these can be seen in the **‘Controllers’** tab.  The example below shows a evaporator controller with the various control groups accessible via a drop down menu.  Any auto history settings will be seen in these controller group lists, manual configuration of any parameter can be done in this page.

Navigate and select appropriate points for history collection, via the drop down menu selector.  Double click a required line, a pop up selection box allows the choice of sample rates; **1,2,10,30 mins 1 Hr**

**Relays, Sensors, On/Off Inputs, Variable Outputs & Other** Depending on the defined control criteria, other points may be viewed and modified under the respective tabs.

#### **Service Tool Support**

Your AK-SM supports the Danfoss Service Tool (version 3.23 and above).  The Service Tool (CT) must be connected via an IP interface.  Once an connection is established the ST will show the AK-SM and all AK2 platform devices.  Note that non AK2 platform based devices will not show up in the ST device list.

When creating a new connection in your ST make sure you select TCP/IP channel.

Assuming the factory default user name and password, enter **Supervisor** for the Destination name **12345** for the Pass code

Once connected, navigate to your required controller in the available list.  Access to all AK2 parameters is available via this connection.

#### **General navigation, operation and use (via web)**

Once your AK-SM has been configured, general navigation and daily use is done via the Dashboard screen.  The Dashboard screen acts as the central system home page, where further system details can be reached.  The Dashboard and subsequent device screens have been developed to provide an easy to use navigation environment for the user, where typical status and setting can be found.

##### **Connecting to your AK-SM:**

##### **Dashboard view:**

Once the correct user name and password has been entered the Dashboard screen will load.  The Dashboard screen will only reflect what your application configuration has been set to.  For example, if your application does not have any HVAC configured the Dashboard will not show the HVAC panel.  Dashboard panels are automatically generated depending on the configuration, no user action is required to build the panels.

Using a standard web browser or your StoreView Desktop application, enter your AK-SM IP address

The factory default User name & password: User Name: Supervisor Password: 12345

To guarantee the best experience when connecting to your AK-SM, ensure you PC has the latest version of Adobe® Flash®

Translation Tool (used for local language translation) Download Report (system report of configuration) Log Off

Dashboard screen System View screen Schedule screen Histroy (logs) On board quick setup guide Use the simulator tool to Global alarms (all Device detail screen Info screen (softCentral AK-SM configuration simulate configured Misc connected AK-SM units) ware version, etc) screens points

*[Figurtekst: Data poll refresh info · Expand panel button Refrigeration panel HVAC panel data communication status · Active alarm panel · Lighting panel Misc panel Energy panel]*

*[Figurtekst: HVAC panel data communication status]*

*[Figurtekst: Misc panel Energy panel]*

Once the correct user name and password has been entered the Dashboard screen will load.  The Dashboard screen will only reflect what your application configuration has been set to.  For example, if your application does not have any HVAC configured the Dashboard will not show the HVAC panel.  Dashboard panels are automatically generated depending on the configuration, no user action is required to build the panels.

Upon the Dashboard loading, if any active alarms are present the built in alarm buzzer can be heard.  To silence the alarm press the silence button.  This does not acknowledge or clear any alarms.

##### **Managing alarms:**

Any active alarms will be shown in the Dashboard alarm panel. To view more details regarding the alarm double click the relevant alarm line.  A alarm info box will appear with further details regarding the alarm.

In addition to more information, the info box also allows the authorized user to Mute/Acknowledge the alarm and to jump to the device detail screen.

Use the Mute/Ack button to acknowledge the alarm.  When pressed the alarm will ‘move’ to the Acknowledge list

_Alarm info pop up_

Click the detail button to jump to the device detail screen

To view all system alarms (known as global alarms) use the Alarms tab (found on the main menu)

_Global alarm screen_

Global acknowledge list Status and Service screens Export Alarms Global active alarm list Export to CSV file Global cleared alarm list

###### _Service screen_

Under the service screen tab, test alarms can be configured and set.

##### **Device detail:**

Whilst the Dashboard screen will show basic asset information (AK-SM unit address, Asset Name, Value, Status and alarm), more detailed information can be found by double clicking an asset line in the Dashboard.  The resulting device detail screen will reflect more details and settings.  The device detail screen is designed to provide key status and operational settings for the selected device.  Easy navigation to other assets is done via the navigation tree.  The screen image below highlights some of the main areas of the device detail screen.

Device alarms/History/Schedules ‘Snap shot’ history Navigation Tree and Advanced View

Controller group menu (based on the controller type)

Full screen button

Status | Settings | Manual Operation tabs

###### **Status**

Under the status tab, common read only datapoints are shown

###### **Settings**

Under the settings tab, read and write values can be shown. Double click a line to make changes (if authorized)

###### **Manual Operation**

Under the Manual Operation tab, key user override functions are available

Use the ‘Advanced view’ screen to access Measurements and Settings side by side.  This screen is useful to access all read/write parameters for the particular controller

###### _Advanced screen_

##### **System view:**

The system view provides a generic yet graphical view of your configured controls.

The same principle of the navigation tree can be seen in the left side of the screen.  The system view screen shows any configured Rack or Pack, with associated evaporator circuits.  To see additional information, hover your mouse pointer over an icon, a pop up box will appear showing additional information.  To view additional information and gain access to settings click the ‘show Detail’ button.  A dashboard will slide across, where a Status, Settings and Manual operation can be seen.  Simply click an asset to highlight and the detail table will update with reference to this selected device.  Once complete with the device settings, close the dashboard by clicking the  ‘Hide Detail’ button.

_System View (Refrigeration)_

Gain access to more details via the ‘Show Details’ button

##### **Schedule view:**

The schedule view provides a system wide view of schedules (previously configured) in your AK-SM or host of controllers. The following schedules are currently supported under the schedule view;

Shutdown (Generic controllers - i.e. AK-CC) Defrost (Generic controllers - i.e. AK-CC) Case Lights (Generic controllers - i.e. AK-CC) Night Setback (Generic controllers - i.e. AK-CC)

If a host network of AK-SM units are configured, a full system view can be seen by selecting the folder icon, for a (AK-SM) unit display click the relevant heading under the folder view.  The schedule screen includes a mouse hover over, that indicates (per circuit) the schedule times.

Change the graphical view to text (table) form, Print, save as PDF or save as CSV

#### **History (Logs)**

To access your AK-SM history, select the history tab. Upto 8 datapoints can be viewed at any given time on the history screen.

###### **History Tool bar**

When viewing data in the history view the tool bar has a set of functions to enable various actions to be performed.

###### **Export history function**

Export to .hst or csv file format.  Saving the collected history points (as .hst) will allow the user to re-load these at a later date (via the ‘load history from file’ button

*[Figurtekst: Load history from file · Load a saved .hst file to view · Convert history file to .CSV · Zoom · Load history group · from file · Preferences · Print · Page control · Save history group to file · (Creates a file that contains defined parameters. · This saves time locating the parameters when loading a graph)]*

##### **Collecting and viewing history**

1/ from the history page, press the collect button

2/ Select the required datapoints and time/date range.  Multiple points can be collected but only 8 can be later shown in the history screen at any given time.  After the datapoints have been downloaded, a dialogue box will appear which provides two options: Select points to draw Save to .hst file (for later view)

3/ The graph will be presented for view and analysis.  Use the zoom buttons or hold the left mouse button and hold for zoom area.  Moving the mouse pointer will show a tool tip with point description, time/date and value.

Show curves (provides a computed rounding of the analog curve)

Show Symbols (each symbol represents a sample)

**Save History Group to file (saving time for frequent datapoint**

###### **selections)**

This feature allows the user to save a set of history datapoints. Typically this feature would be used when a set of datapoints is frequently needed to be loaded and viewed.  Once the datapoints are saved, this history group can then be easily loaded - thus saving time in selecting datapoints.

###### **Load History Group from file**

Use this feature to load any previously save datapoint groups. When opening the history group file the system will prompt for the file location.  Once loaded a ‘select datapoint’ box will appear with the datapoints already pre-selection

###### **Export History data**

This feature allows the user to export the previously collected history data.  A pop up window asks the user to select a file format, the following formats are possible; .hst (Danfoss history file format) .csv (Excel compatible spreadsheet) Saving any collected history as a file allows for future loading and view, use the ‘Load history from file’ button to load any saved <u>history files.</u>

#### **Updating Software (via USB Flash Drive)**

The AK-SM can read & write to USB flash based drives.  Upon insertion (or via main menu option 7), the USB menu window will be shown (for DIN units read following section).  A typical example of the resulting pop up screen can be seen below, with descriptions for each option.  The menu reflects  supported files located on the USB memory stick, and may vary from the example below.  Ensure relevant software files are located in the USB root directory.   When updating your AK-SM it is recommended to first update the ‘Bootloader’ (if specified), followed by the Master Application Image (MAI).  The MAI contains AK-SM firmware, EDF and Web files needed.

###### **Flash Drive options**

Option 1: The Bootloader file can be updated via USB connection. Option 2: The Application software can be updated via USB connection.

Option 3: Master Application Image (MAI).  This is the recommended file to update your AK-SM, it contains firmware, EDF and Web files

Option 4: Save AK-SM database via USB

Option 5: Load AK-SM database via USB Option 6: Save report (txt file format, containing main system configuration details)

Option 7: Save Report (txt file format, containing configured system status, not full configuration details)

Bootloader file- used for AK-SM system file management

AK-SM Application code (does not include EDF/HTML files) Master Application Image (includes firmware, EDF and HTML files)

Save AK-SM database (does not include any graphic view files)

Load a SM-800 database

Save AK-SM system configuration as .txt file

|**File type / Description**|**Method of loading**|
|---|---|
|**Boot.csi**/ Boot Loader file (required for system file management)|USB Flash drive|
|**CSI**/ Application code for AK-SM.  Includes all system EDF files|USB Flash drive or RMT tool|
|**MAI**/ Master Application code for AK-SM.  Includes all firmware, EDF and Web files|USB Flash drive or RMT|
|**FAI**/ Factory Application Image|USB|

**Remotely Upgrading you AK-SM unit - what is the FAI file** Your AK-SM has the ability to be upgraded via a remote connection (RMT).  Upgrading via remote offers several advantages, the obvious one being time saving.  However, this is increased risk when preforming remote upgrades (i.e. quality of connectivity, power..).  Software version 03_051 (and above) comes with an additional extension, FAI (Factory Application Image).  The FAI software file contains special code designed to support remote software upgrades.  The FAI file provides a ‘fall back’ state, if at any time a later remote upgrade fails or gets corrupted.  Rather than leave a unit in a unstable state in the event of a corrupted remote upgrade, the factory image ensures you can always make contact to re-install code again.  In addition, the FAI contains the MAI, which also contains all relevant web and EDF files.  Via the Info screen, check if your AK-SM unit has a Factory Application installed.  For future remote upgrades it is recommended that the FAI is installed if it is not already present in your system.   The AKSM can run without the FAI, with firmware updates being done via the MAI file.

_Under the Info->Information tab, check to see if a Factory Application is installed (FAI)._

_If you intend to perform remote software updates, Danfoss recommends the loading of the FAI file._

###### **Recommended method for upgrading your AK-SM - Boot-**

###### **loader**

The AK-SM bootloader file is a critical file that manages system boot up sequence and system management.  The Bootloader can **not** be loaded remotely.   Updating the bootloader can be done in application mode (normal AK-SM operation) or when placed in bootloder mode.  The following description of how to upgrade your Bootloder version is via normal AK-SM operation mode.

###### **Bootloader**

1/ Back up current database (via USB flash drive or RMT)

2/ Load the latest Bootloader on to the **root directory** of a suitable USB flash Drive and insert in the AK-SM.  The Bootloader file is shown under option 1 of the resulting USB pop up window. A progress dialog box will appear, to confirm loading status. 3/ Upon finishing the Bootloader file installation the AK-SM will reset.  Your AK-SM will reset in Bootloder mode.  Manually reset the AK-SM by pressing and holding down the CPU reset button, located behind the front USB access door.  The system will now boot into normal application mode.

CPU Reset button (Press and hold for 5 seconds)

Located inside USB access door

###### **Firmware**

Danfoss recommends using the Master Application Image software (MAI), as it contains all relevent files for correct operation (Firmware, Web and EDF).  The following steps describe how to update whilst in normal operation mode.

1/ Back up current database (via USB flash drive or RMT) if not already done so 2/ Load the latest AK-SM firmware (i.e. MAI file) in the **root directory** of a suitable USB flash Drive and insert in the AK-SM. The MAI file should be shown under option 3 of the resulting USB pop up window.  Follow on screen instructions.

3/ Allow the MAI to fully install and write to system flash memory

4/ After a few minutes the unit will reset and return to normal operation, using the latest code.

###### **www.danfoss.com**

ADAP-KOOL® Refrigeration Control Systems is a trademark of Danfoss A/S, www.danfoss.com

Danfoss can accept no responsibility for possible errors in catalogs, brochures, or other printed material.  Danfoss reserves the right to alter its products without notice. This also applies to products already on order provided that alterations can be made without subsequent changes being necessary in specifications already agreed. All trademarks in this material are property of the respective companies. Danfoss and the Danfoss logotype are trademarks of Danfoss A/S.  All rights reserved.

