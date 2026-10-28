# Carel ir33 platform – connections / user manual (ir33, ir33 power, ir33 DIN, powercompact, mastercella)

Kilde: `User-Manual-CAREL-Low-Temperature-Control.pdf` i denne mappe. Konverteret direkte fra PDF'en. Tabeller (parametre, alarmer, standardværdier) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra tegninger står som *[Figurtekst: …]*. PDF'en er tosproget (spansk/engelsk); kun den engelske del (fra side 29) er taget med. Bemærk: dette er tilslutningsmanualen for ir33-platformen (ledningsdiagrammer, elektriske data), ikke parameterlisten.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilket afsnit svaret kommer fra.
- Alarm- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer (Dixell, Danfoss, Carel). Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualen, så sig det i stedet for at gætte.

---

User manual

We wish to save you time and money! We can assure you that the thorough reading of this manual will guarantee correct installation and safe use of the product described.

###### IMPORTANT WARNINGS

CAREL bases the development of its products on decades of experience in HVAC, on the continuous investments in technological innovations to products, procedures and strict quality processes with in-circuit and functional testing on 100% of its products, and on the most innovative production technology available on the market.

CAREL and its subsidiaries nonetheless cannot guarantee that all the aspects of the product and the software included with the product respond to the requirements of the final application, despite the product being developed according to start-ofthe-art techniques. The customer (manufacturer, developer or installer of the final equipment) accepts all liability and risk relating to the configuration of the product in order to reach the expected results in relation to the specific final installation and/or equipment. CAREL may, based on specific agreements, acts as a consultant for the positive commissioning of the final unit/application, however in no case does it accept liability for the correct operation of the final equipment/system. The CAREL product is a state-of-the-art product, whose operation is specified in the technical documentation supplied with the product or can be downloaded, even prior to purchase, from the website www.carel.com.

Each CAREL product, in relation to its advanced level of technology, requires setup/configuration/programming/commissioning to be able to operate in the best possible way for the specific application. The failure to complete such operations, which are required/indicated in the user manual, may cause the final product to malfunction; CAREL accepts no liability in such cases. Only qualified personnel may install or carry out technical service on the product.

The customer must only use the product in the manner described in the documentation relating to the product. In addition to observing any further warnings described in this manual, the following warnings must be heeded for all CAREL products: • Prevent the electronic circuits from getting wet. Rain, humidity and all types of liquids or condensate contain corrosive minerals that may damage the electronic circuits. In any case, the product should be used or stored in environments that comply with the temperature and humidity limits specified in the manual.

- Do not install the device in particularly hot environments. Too high temperatures may reduce the life

   - of electronic devices, damage them and deform or melt the plastic parts. In any case, the product

   - should be used or stored in environments that comply with the temperature and humidity limits specified in the manual.

- Do not attempt to open the device in any way other than described in the manual.

- Do not drop, hit or shake the device, as the internal circuits and mechanisms may be irreparably damaged.

- Do not use corrosive chemicals, solvents or aggressive detergents to clean the device.

- Do not use the product for applications other than those specified in the technical manual.

All of the above suggestions likewise apply to the controllers, serial boards, programming keys or any other accessory in the CAREL product portfolio.

CAREL adopts a policy of continual development. Consequently, CAREL reserves the right to make changes and improvements to any product described in this document without prior warning.

The technical specifications shown in the manual may be changed without prior warning.

The liability of CAREL in relation to its products is specified in the CAREL general contract conditions, available on the website www.carel.com and/or by specific agreements with customers; specifically, to the extent where allowed by applicable legislation, in no case will CAREL, its employees or subsidiaries be liable for any lost earnings or sales, losses of data and information, costs of replacement goods or services, damage to things or people, downtime or any direct, indirect, incidental, actual, punitive, exemplary, special or consequential damage of any kind whatsoever, whether contractual, extra-contractual or due to negligence, or any other liabilities deriving from the installation, use or impossibility to use the product, even if CAREL or its subsidiaries are warned of the possibility of such damage.

###### <u>Disposing of the parts of the controller:</u>

The controller is made up of metal and plastic parts and a lithium battery. All these parts must be disposed of separately in compliance with the local standards in force on waste disposal.

4

### Contents

|1.  POWERCOMPACT|7|
|---|---|
|1.1  Dimensions ................................................................................<br>i|............................................................7<br>i|
|1.2  Electrical specifications ............................................................|i ............................................................7|
|1.3  Electrical connections ..............................................................|............................................................9|
|2.  POWERCOMPACT SMALL|10|
|2.1  Dimensions ................................................................................<br>i|............................................................10<br>i|
|2.2  Electrical specifications ............................................................|i ............................................................10|
|1.3  Electrical connections ..............................................................|............................................................12|
|3.  MASTERCELLA 2|13|
|3.1  Dimensions ................................................................................<br>i|............................................................13<br>i|
|3.2  Technical specifications ...........................................................|i ............................................................13|
|3.3  Electrical connections ..............................................................|............................................................14|
|4.  IR33|16|
|4.1  Dimensions ................................................................................<br>i|............................................................16<br>i|
|4.2  Electrical specifications ............................................................|i ............................................................|
|16||
|4.3  Electrical connections ..............................................................|............................................................18|
|5.  IR33POWER|20|
|5.1  Dimensions ................................................................................<br>i|............................................................20<br>i|
|5.2  Electrical specifications ............................................................|i ............................................................20|
|5.3  Electrical connections ..............................................................|............................................................22|
|6.  IR33 2HP|23|
|6.1  Dimensions ................................................................................|............................................................23|
|6.2  Technical specifications ...........................................................|i ............................................................23|
|6.3  Electrical connections ..............................................................|............................................................|
|6.  IR33DIN|25|
|6.1  Dimensions ................................................................................<br>i|............................................................25<br>i|
|6.2  Electrical specifications ............................................................|i ............................................................25|
|6.3  Electrical connections ..............................................................|............................................................27|

5

6

1.  POWERCOMPACT

##### **<u>1.1  Dimensions</u>**

*[Figurtekst: POWER COMPACT WIDE POWER COMPACT STANDARD · AUX · 183.4 167 · dima di foratura 1 2 · drilling template · 153.5 64 · 165 75 · 8 · Fig. 1.a · Legenda: · 1.  Drilling template Models standard: 138,5 x 29 mm · Models wide: de 138,5x29 mm a 150x31 mm · 2.  Version with faston + 8 mm · 39.4 36 · 28.2]*

##### **<u>1.2  Electrical specifications</u>**

|||voltage||power|
|---|---|---|---|---|
|Power supply|model E:|230 V~ 50/60<br>230 V~ 50/60|Hz;<br>Hz,16 A,8 A,8 A version;|3 VA, 25 mA~ max<br>3 VA,25 mA~ max|
||model A:|115 V~ 50/60<br>115 V~ 50/60|Hz;<br>Hz,16 A,8 A,8 A version;|3 VA, 50 mA~ max<br>3 VA,50 mA~ max|
||model H:|115-230 Vac 50|/60Hz|6 VA,50mA~ max|
||model 0:<br>|12 V~ , 50/60<br>12 Vdc, 12-18V<br>|Hz<br>dc<br>|4 VA, 300 mA~ max<br>TRADR4W012 transformer, 315 mA slow-blow fuse in secondary,<br>onlyuse SELVpower supply|
|Insulation guaranteed by the power<br>||voltage||power|
|supply|model E, A, H:|insulation from<br>insulation from|very low voltage parts<br>relayoutputs|reinforced.; 6 mm air, 8 mm surface; 3750 V insulation<br>basic;3 mm air,4 mm surface;1250 V insulation|
||model 0:|insulation from<br>insulation from|very low voltage parts<br>relayoutputs|to be guaranteed externally by safety transformer<br>basic;3 mm air,4 mm surface;1250 V insulation|
|Inputs|S1|NTC or PTC,de|pendingon the model||
||S2|NTC or PTC,de|pendingon the model||
||DI1<br>S3|voltage-free co<br>NTC or PTC,de|ntact, contact resistance < 10 ohm,<br> pendingon the model|closing current 6 mA|
||DI2<br>S4|voltage-free co<br>NTC or PTC,de|ntact, contact resistance < 10 ohm,<br> pendingon the model|closing current 6 mA|
||Maximum distanc<br>Note:in the install<br>cables.|e between probes<br>ation, keep the po|and digital inputs less than 10 m<br>wer supply and load connections s|eparate from the probe, digital inputs, repeater display and supervisor|
|Type of probe|Std. Carel NTC||10 kΩat 25 °C, range –50T90<br>measurement error: 1 °C in th<br>3 °C in th|°C<br>e range –50T50 °C<br>e range +50T90 °C|
||High temperature|NTC|50 kΩat 25 °C, range –40T15<br>measurement error: 1.5 °C in<br>4 °C in th|0 °C<br>the range –20T115 °C<br>e range outside of -20T115 °C|
||Std. Carel PTC (spi|ecific model)|985Ωat 25°C, range -50T150<br>measurement error: 2 °C in th<br>4 °C in th|°C<br>e range  –50T50 °C<br>e range +50T150 °C|

7

|Relay outputs|voltage<br>power<br>dependingon the model|
|---|---|
||<br>5 A (*)<br>EN60730-1:<br>250 V~ 5 (1) A;<br>100000 operating cycles|
||<br> <br> <br>,<br>UL 873:<br>250 V~ 5A res 1FLA 6LRA C300;<br>30,000 operatingcycles|
||8 A (*)<br>EN60730-1:<br>250 V~ 8 (4) on N.O.,  6 (4) on N.C., 2 (2) on N.O. and N.C.; 100,000 operating cycles<br> <br>|
||UL 873:<br>250 V~ 8A res 2FLA 12LRA C300;<br>30,000 operatingcycles<br> <br> <br>|
||16 A (*)<br>EN60730-1:<br>250 V~ 10 (4) A up to 60°C on N.O., 12 (2) A on N.O. and N.C.;100,000 operating cycles<br> <br> <br>|
||UL 873:<br>250 V~ 12A res 5FLA 30LRA C300;<br>30,000 operatingcycles|
||2HP<br>EN60730-1:<br>250 V~ 10 (10) A;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 12FLA 72LRA;<br>30,000 operatingcycles|
||* Rl t itbl f flt ld  liht  tht  tt bllt ith h-hift it Flt l ith|
||(): eay no suae or luorescen oas (neon gs, ...) a use sarers (aass) w pases capacors. uorescen amps w<br>electronic control devices or withoutphase-shift capacitors can be used,within the operatinglimits specified for each type of relay.|
||insulation from verylow voltageparts<br>reinforced;6 mm air,8 mm surface;3750 V insulation<br>   <br>|
||insulation between the relayoutputs<br>basic;3 mm air,4 mm surface;1250 V insulation|
|Connections|Type of connection<br>Cross-sections<br>Maximum current<br>i<br>²<br>|
||fixed screw<br>for cables from 0.5 to 2.5 mm<br>12A<br>|
||plug-in for screw blocks<br>spade with crimped contact<br>|
||The correct sizing of the power and connection cables between the instrument and the loads is the responsibility of the installer.|
||In the max load and max operatingtemp. conditions,the cables used must be suitable for operation upto 105°C.<br>|
|Case|plastic: dimensions 36x167x75 mm;mountingdepth 64 mm|
|Assembly|smooth,hard and indeformablepanel: usingscrews from the front|
||drillingtemplate: dimensions 29x138.5 mm;distance between fasteningscrews 153.5mm|
||fasteningscrews: countersunk head with maximum thread diameter 3.9mm<br>|
|Wide vers. case<br>|plastic                                                                          dimensions: 39.4x183x75<br>|
|(power supplyE,A,H,O)|mountingdepth 63 mm|
|Assembly<br>|smooth,hard and indeformablepanel                          usingscrews from the front or brackets<br>|
|(power supply E, A, H, O)|drilling template                                                           dimensions: from 138.5x29 to 150x31|
|Wide versions|<br>distance between fasteningscrews: 165 mm or 1535|
|<br>Display|.<br>digits: 3 digit LED|
||display: from -99 to 999<br>|
|Keypad|operatingstatus: indicated withgraphic icons on the display<br>8 silicone rubber buttons|
|Infrared receiver|<br>available dependingon the model|
|Clock with backupbattery|available dependingon the model<br>|
|Buzzer|available in all models<br>l|
|Fasteningscrews<br>|countersunk with maximum thread diameter 3.9 mm for 165 mm spacing;for 153 spacing,flat head with maximum thread diameter 3 mm<br> <br>|
|Clock|Error at 25 °C:<br>± 10ppm(±5.3 min/year)|
||Error in the temperature range -10T60 °C:<br>- 50ppm(-27min/year)<br><br>|
||Ageing:<br>< ±5p pm(±2.7 min/year)|
||Discharge time:<br>typically6 months(8 months maximum)<br> <br>|
||Recharge time:<br>typically5 hours(< 8 hours maximum)|
|Operatingconditions|-10T65 °C;<90% relative humiditynon-condensing|
|Storage conditions|-20T70 °C;<90% relative humiditynon-condensing|
|Frontpanel index ofprotection|assemblyon smooth and indeformablepanel with IP65gasket|
|Environmentalpollution|2,normal situation|
|PTI of insulatingmaterials|printed circuits 250, plastic and insulatingmaterials 175|
|Period of stress across the insulating parts <br>i|long|
|Categoryof resistance to fire|categoryD and categoryB(UL 94-V0)|
|Class ofprotection against voltage surges<br>|categoryII<br>|
|Type of action and disconnection|1B relaycontacts(micro-disconnection)|
|Construction of the control device<br>i|electronic control device incorporated|
|Classification according to protection<br>against electric shock|class II when appropriately integrated|
|Device designed to he hand-held or<br>|no|
|integrated into equipment designed to<br>be hand-held||
|<br>Software class and structure|class A|
|Cleaning the front panel of the instru-<br>ment|only use neutral detergents and water|
|Serial interface for CAREL network|External,available in all models|
|Interface for repeater display|External,available in models with H and 0power supplies|
|Maximum distance between interface<br>and display|10 m|
|Programmingkey|Available in all models<br>|
||fastening screws                                                            countersunk head with maximum thread diameter 3.9 mm for 165 mm spacing<br>flat head for 153 mm spacing,maximum thread diameter 3 mm|

Table 1.a

8

##### **<u>1.3  Electrical connections</u>**

###### PB00S*E(N,R,C,B)*0 PB00S*E(A,M,L,T)*0

###### PB00Y*E(N,R,C,B)*0

###### PB00F*E(N,R,C,B)*0

###### PB00F*H(A,M,L,T)*0

###### PB00C*H(N,R,C,B,)*0

###### PB00H*H(N,R,C,B)*0

Fig. 1.b

9

#### 2.  POWERCOMPACT SMALL

*[Figurtekst: 2.1  Dimensions · WIDE · AUX · 40 · 183.4 · 45 · 8 · STANDARD · 1 · dima di foratura · drilling template · da 138.5 a 150 x 31mm · 167 · 153.5 · 165 · Fig. 2.a · 39.4 28.2 · 36]*

Key:

*[Figurtekst: 1.  drilling template standard models 138.5 x 29 mm. · wide models from 138,5 x 29 mm to 150x31 mm]*

##### **<u>2.2  Electrical specifications</u>**

||voltage<br>power|
|---|---|
|Power supply|model S:<br>115 - 230 V~ 50/60 Hz;<br>6 VA,50 mA~ max|
|Insulation guaranteed by the power supply|insulation from verylow voltageparts<br>reinforced;6 mm air,8 mm surface;3750 V insulation|
||insulation from relayoutputs<br>basic;3 mm air,4 mm surface;1250 V insulation|
|Inputs|S1<br>NTC or PTC,dependingon the model<br> <br>|
||S2<br>NTC or PTC,dependingon the model|
||DI1<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S3<br>NTC or PTC,dependingon the model|
||DI2<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S4<br>NTC or PTC,dependingon the model|
||Maximum distance between probes and digital inputs less than 10 m. Note: in the installation, keep the power supply and load connections<br>separate from theprobe,digital inputs,repeater displayand supervisor cables.|
|Type of probe|Std. Carel NTC<br>10 kΩat 25 °C, range –50 to 90 °C<br>measurement error: 1 °C in the range –50 to 50 °C<br>3 °C in the range +50 to 90 °C|
||High temperature NTC<br>50 kΩat 25 °C, range –40 to 150 °C<br>measurement error: 1.5 °C in the range –20 to 115 °C<br>4 °C in the range outside of -20 to 115 °C<br>i|
||Std. Carel PTC (specific model)<br>985Ωat 25°C, range -50 to 150 °C<br>measurement error: 2 °C in the range –50 to 50 °C<br>4 °C in the range +50 to 150 °C|
|Relay outputs|dependingon the model|
||5 A<br>EN60730-1:<br>250 V~ 5 (1) A;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 5A res 1FLA 6LRA C300;<br>30,000 operatingcycles|
||8 A<br>EN60730-1:<br>250 V~ 8 (4) on N.O.,  6 (4) on N.C.,  2 (2) on N.O. and N.C.; 100,000 operating cycles<br>UL 873:<br>250 V~ 8A res 2FLA 12LRA C300;<br>30,000 operatingcycles|
||30 A<br>EN60730-1:<br>250 V~ 12 (10) A;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 2HP 72LRA;<br>30,000 operatingcycles|
||Relay not suitable for fluorescent loads (neon lights, ...) that use starters (ballasts) with phase-shift capacitors. Fluorescent lamps with electro-<br>nic control devices or withoutphase-shift capacitors can be used,within the operatinglimits specified for each type of relay.|
||insulation from verylow voltageparts<br>reinforced;6 mm air,8 mm surface;3750 V insulation|
||insulation between the relayoutputs<br>basic;3 mm air,4 mm surface;1250 V insulation|
|Connections|Type of connection<br>Cross-sections<br>Maximum current<br>fixed screw<br>for cables from 0.5 to 2.5 mm<sup>2</sup><br>12A<br>plug-in for screw blocks<br>fixed screw vertical<br>spade with crimped contact|
||The correct sizing of the power and connection cables between the instrument and the loads is the responsibility of the installer.<br>Maximum current at terminals 4 and 7 is 12A. In the max load and max operating temp. conditions, the cables used must be suitable for ope-<br>ration upto 105°C.|

10

||voltage<br>power|
|---|---|
|Case|plastic: dimensions 36x167x51 mm;mountingdepth 40 mm|
|Assembly|smooth,hard and indeformablepanel: usingscrews from the front|
||drillingtemplate: dimensions 29x138.5 mm;distance between fasteningscrews 153.5 mm|
||fasteningscrews: countersunk head with maximum thread diameter 3.9 mm|
|Wide vers. case|plastic                                                                          dimensions: 39.4x183x45|
|(power supplyS)|mountingdepth  40 mm|
|Assembly<br>|smooth,hard and indeformablepanel                         usingscrews from the front or brackets<br>|
|(power supply S)<br>|drilling template                                                          dimensions: from 138.5x29 to150x31<br>|
|Wide versions|distance between fastening screws: 165 mm or 153.5<br>fastening screws                                                           countersunk head with maximum thread diameter 3.9 mm for 165 mm spacing<br>flat head for 153 mm spacing,maximum thread diameter 3 mm|
|Display|digits: 3 digit LED|
||display: from -99 to 999|
||operatingstatus: indicated withgraphic icons on the display|
|Keypad|8 silicone rubber buttons|
|Infrared receiver|available dependingon the model|
|Clock with backupbattery|available dependingon the model|
|Buzzer|available in all models|
|Clock|Error at 25 °C:<br>± 10ppm(±5.3 min/year)|
||Error in the temperature range –10T60 °C:<br>- 50ppm(-27min/year)|
||Ageing:<br>< ±5p pm(±2.7 min/year)|
||Discharge time:<br>typically6 months(8 months maximum)|
||Recharge time:<br>typically5 hours(< 8 hours maximum)|
|Operatingconditions|-10T65 °C;<90% relative umiditynon-condensing|
|Storage conditions|-20T70 °C;<90% relative umiditynon-condensing|
|Frontpanel index ofprotection|assemblyon smooth and indeformablepanel with IP65gasket|
|Environmentalpollution|2,normal situation|
|PTI of insulatingmaterials|printed circuits 250, plastic and insulatingmaterials 175|
|Period of stress across the insulating parts|long|
|Categoryof resistance to fire|categoryD and categoryB(UL 94-V0)|
|Class ofprotection against voltage surges|categoryII|
|Type of action and disconnection|1B relaycontacts(micro-disconnection)|
|Construction of the control device<br>i|electronic control device incorporated|
|Classification according to protection<br>against electric shock|to be integrated into class I appliances|
|Device designed to he hand-held or<br>integrated into equipment designed to<br>be hand-held|no|
|Software class and structure|class A|
|Cleaning the front panel of the|only use neutral detergents and water|
|<br>instrument||
|Serial interface forCAREL network|External,available in all models|
|Interface for repeater display|External,available in all models|
|Maximum distance between interface<br>|10 m|
|and display||
|Programmingkey|Available in all models|

Table 2.a

11

**<u>2.3  Electrical connections</u>**

##### PB00S*S(N,R,C,B)*0

##### PB00S*S(A,M,L,T)*0

##### PB00Y*S(N,R,C,B)*0

##### PB00Y*S(A,M,L,T)*0

##### PB00F*S(N,R,C,B)*0

##### PB00C*S(N,R,C,B)*0

Fig. 2.b

12

3.  MASTERCELLA 2

##### **<u>3.1  Dimensions</u>**

Fig. 3.a

##### **<u>3.2  Technical specifications</u>**

||voltage<br>power|
|---|---|
|Power supply|model E:<br>230 V~ 50/60 Hz;<br>11,3 VA,50 mA~ max|
||model A:<br>115 V~ 50/60 Hz;<br>11,3 VA,100 mA~ max|
|Insulation guaranteed by the power supply|voltage<br>power|
||model E, A:<br>insulation from very low voltage parts<br>reinforced; 6 mm air, 8 mm surface; 3750 V insulation<br>insulation from relayoutputs<br>basic;3 mm air,4 mm surface;1250 V insulation|
|Inputs|S1<br>NTC or PTC,dependingon the model|
||S2<br>NTC or PTC,dependingon the model|
||DI1<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S3<br>NTC or PTC,dependingon the model|
||DI2<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S4<br>NTC or PTC,dependingon the model|
||DI3<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S5<br>NTC or PTC,dependingon the model|
||Maximum distance between probes and digital inputs less than 10 m. Note: in the installation, keep the power supply and load connec-<br>tions separate from theprobe,digital inputs,repeater displayand supervisor cables.|
|Type of probe|Std. Carel NTC<br>10 kΩat 25 °C, range -50 to 90 °C<br>measurement error:  1 °C in the range -50 to 50 °C<br>3 °C in the range +50 to 90 °C|
||High temperature NTC<br>50 kΩat 25 °C, range -40 to 150 °C<br>measurement error: 1.5 °C in the range -20 to 115 °C<br>4 °C in the range outside of -20 to 115 °C|
||Std. Carel PTC (specific model)<br>985Ωat 25°C, range -50 to 150 °C<br>measurement error: 2 °C in the range -50 to 50 °C<br>4 °C in the range +50 to 150 °C|
|Relay outputs|dependingon the model|
||8 A (*)<br>EN60730-1:<br>250 V~ 8 (4) on N.O.,  6 (4) on N.C.,  2 (2) on N.O. and N.C.; 100,000 operating cycles<br>UL 873:<br>250 V~ 8A res 2FLA 12LRA C300;<br>30,000 operatingcycles|
||16 A (*)<br>EN60730-1:<br>250 V~ 10 (4) A up to 60°C on N.O., 12 (2) A on N.O. and N.C.;100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 5FLA 30LRA C300;<br>30,000 operatingcycles|
||2HP<br>EN60730-1:<br>250 V~ 10 (10) A;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 12FLA 72LRA;<br>30,000 operatingcycles|
||30 A (*)<br>EN60730-1:<br>250 V~ 12 (10) A;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 2HP 72LRA;<br>30,000 operatingcycles|
||(*): relay not suitable for fluorescent loads (neon lights, ...) that use starters (ballasts) with phase-shift capacitors. Fluorescent lamps with<br>electronic control devices or withoutphase-shift capacitors can be used,within the operatinglimits specified for each type of relay.<br>  <br>|
||insulation from verylow voltageparts<br>reinforced;6 mm air,8 mm surface;3750 V insulation|
||insulation between the relayoutputs<br>basic;3 mm air,4 mm surface;1250 V insulation|
|Connections|Type of connection<br>Cross-sections<br>Maximum current<br>i|
||<br>fixed screw<br>for cables from 0.5 to 2.5 mm<sup>2</sup><br>12A|
||i<br>plug-in for screw blocks<br>spade with crimped contact|
||wire cross-section forprobes and digital inputs:<br>0.25 to 2.5 mm2(from 20 to 13 AWG)|
||wire cross-sectionperpower supplyand loads:<br>1.5 to 2.5 mm2(from 15 to 13 AWG)|
||The correct sizing of the power and connection cables between the instrument and the loads is the responsibility of the installer.<br>In the max load and max operatingtemp. conditions,the cables used must be suitable for operation upto 105°C.|

13

||voltage<br>power|
|---|---|
|Case|plastic: dimensions 200x240x93 mm;mountingdepth 64 mm|
||open main board and frontpanel: base dimensions 178x86x40 mm;frontpanel dimensions 100x90x12 mm|
|Assembly|wall mounting (withplastic case):<br>usingfasteningscrews;<br>spacing162.5x218.5 mm|
||panel installation(withplastic frontpanel):  usingfasteningscrews;<br>spacing159.5x197.5 mm|
||open board:<br>usingfasteningscrews for main board and frontpanel|
|Display|digits: 3 digit LED<br>|
||display: from -99 to 999|
||operatingstatus: indicated with LEDs andgraphic icons made in thepolycarbonate label applied to theplastic case|
|Keypad|8 mechanical buttons,keypad made in thepolycarbonate label applied to theplastic case|
|Infrared receiver|available dependingon the model|
|Clock with backupbattery|available dependingon the model|
|Buzzer|available in all models|
|Clock|Error at 25 °C:<br>± 10ppm(±5.3 min/year)|
||Error in the temperature range -10T60 °C:<br>- 50ppm(-27min/year)|
||Ageing:<br>< ± 5ppm(±2.7 min/year)|
||Discharge time:<br>typically6 months(8 months maximum)|
||Recharge time:<br>typically5 hours(< 8 hours maximum)|
|Operating conditions|open board:<br>-10T65 °C;<90% RH non-condensing|
||with plastic case:<br>-10T50 °C; <90% RH non-condensing<br>With the following current configurations:<br>Relay 1 12 A, Relay 2 0 A, Relay 3 4 A, Relay 4 4 A, Relay 5 4 A<br>Relay 1 0 A, Relay 2 12 A, Relay 3 4 A, Relay 4 4 A, Relay 5 4 A<br>The currents indicated above will be reduced accordingto the relays used.|
|Storage conditions|-20T70 °C;<90% RH non-condensing|
|Frontpanel index ofprotection|withplastic case<br>IP65 without disconnectingswitch|
||panel installation withplastic frontpanel<br>IP54 with disconnectingswitch|
|Environmentalpollution|2,normal situation|
|PTI of insulatingmaterials|printed circuits 250, plastic and insulatingmaterials 175|
|Period of stress across the insulating parts<br>i|long|
|Categoryof resistance to fire|categoryD and categoryB(UL 94-V0)|
|Class ofprotection against voltage surges|categoryII|
|Type of action and disconnection|1B relaycontacts(micro-disconnection)|
|Construction of the control device|electronic control device incorporated|
|Classification according to protection against<br>electric shock|class II when appropriately integrated|
|Device designed to he hand-held or integra-|no|
|ted into equipment designed to be hand-held||
|Software class and structure|class A|
|Cleaningthe frontpanel of the instrument|onlyuse neutral detergents and water|
|Serial interface forCAREL network|Built-in,available in all models,upon request|
|Interface for repeater display|Built-in,available in all models,upon request|
|Maximum distance between interface and|10 m|
|display||
|Programmingkey|Available in all models|

Table 3.a

##### **<u>3.3  Electrical connections</u>**

Note: Colors referring to cable PSTCON**00

*[Figurtekst: REMOTE DISPLAY and · MD33D****0 VL (green) · SERIAL INTERFACE · GND · (brown+yellow) · Rx/Tx (white) · PROGRAMMING Network 485 · KEY · Network 485 · Bare board: IP00 · Plastic case: IP65 GND · Plastic case and · disconnecting switch: IP54 · -10T65 Bare board · -10T50 With plastic case · maximum current on r1-r5, · 12 A, 0 A, 4 A, 4 A, 4 A or · 0 A, 12 A, 4 A, 4 A, 4 A · 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 · R1 AUX1 R4 AUX2 R5 · E: 230 V~ · 50mA~ max L · A: 115 V~ N · 100mA~ max · H: 115 V~ · 110mA~ max · 33 · 32 · 31 · 30 · 29 · 28 · 27 · 26 3 DI · 25 · 24 2 DI · 23 · 22 1 DI · 21 · 2 · 20 · 19 PROBES · 1 · 18]*

Fig. 3.b

14

||||Relè 1||Relè 2|Relè 5|
|---|---|---|---|---|---|---|
|MD33A0***0|EN60730-1<br>UL 873|250 V|12(2) A<br>12A 5FLA<br>30LRA|8(2) A<br>8A 2FLA<br>30LRA||12(2) A<br>12A 5FLA<br>30LRA|
|MD33A1***0|EN60730-1<br>UL 873|250V|10(10) A<br>12A 12FLA<br>72LRA|8(4) A<br>8A 2FLA<br>12LRA||10(10) A<br>12A 12FLA<br>72LRA|
|MD33A2***0|EN60730-1<br>UL 873|250V|12(10) A<br>12A 12FLA<br>72LRA 2hp|8(4) A<br>8A 2FLA<br>12LRA||12(2) A<br>12A 5FLA<br>30LRA|
|MD33A3***0|EN60730-1<br>UL 873|250V|12(2) A<br>12A 5FLA<br>30LRA|8(4) A<br>8A 2FLA<br>12LRA||10(10) A<br>12A 12FLA<br>72LRA|
|MD33A4***0|EN60730-1<br>UL 873|250V|10(10) A<br>12A 12FLA<br>72LRA|8(4) A<br>8A 2FLA<br>12LRA||12(2) A<br>12A 5FLA<br>30LRA|
|MD33A5***0|EN60730-1<br>UL 873|250V|12(10) A<br>12A 12FLA<br>72LRA 2hp|8(4) A<br>8A 2FLA<br>12LRA||10(10) A<br>12A 12FLA<br>72LRA|

Note: Colors referring to cable PSTCON**00

*[Figurtekst: REMOTE DISPLAY and · MD33D****0 VL (green) · SERIAL INTERFACE GND · (brown+ yellow) · Rx/Tx (white) · Bare board: IP00Plastic case: IP65 PROGRAMMING Network 485 · KEY · Plastic case and  Network 485 · disconnecting switch: IP54 · GND · -10T65 Bare board · -10T50 With plastic case · maximum current on r1-r5, · 12 A, 0 A, 4 A, 4 A, 4 A or · 0 A, 12 A, 4 A, 4 A, 4 A · 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 · R1 R2 R3 AUX1 R4 AUX2 R5 · E: 230 V ˜ · 50 mA ˜ max L · A: 115 V ˜ N · 100 mA ˜ max · 293031323328 · 3 DI · 2 DI · 1 DI · 2 PROBES · 1 · 23242526272218192021]*

Fig. 3.c

||||Relè 1|Relè 2|Relè 3|Relè 4|Relè 5|
|---|---|---|---|---|---|---|---|
|MD33D0***0|EN60730-1<br>UL 873|250 V|12(2) A<br>12A 5FLA<br>30LRA|12(2) A<br>12A 5FLA<br>30LRA|8(4)A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|12(2) A<br>12A 5FLA<br>30LRA|
|MD33D1***0|EN60730-1<br>UL 873|250V|10(10) A<br>12A 12FLA<br>72LRA|8(4) A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|10(10) A<br>12A 12FLA<br>72LRA|
|MD33D2***0|EN60730-1<br>UL 873|250V|12(10) A<br>12A 12FLA<br>72LRA 2hp|8(4) A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|12(2) A<br>12A 5FLA<br>30LRA|
|MD33D3***0|EN60730-1<br>UL 873|250V|12(2) A<br>12A 5FLA<br>30LRA|8(4) A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|10(10) A<br>12A 12FLA<br>72LRA|
|MD33D4***0|EN60730-1<br>UL 873|250V|10(10) A<br>12A 12FLA<br>72LRA|8(4) A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|12(2) A<br>12A 5FLA<br>30LRA|
|MD33D5***0|EN60730-1<br>UL 873|250V|12(10) A<br>12A 12FLA<br>72LRA 2hp|8(4) A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|8(4)A<br>8A 2FLA<br>12LRA|10(10) A<br>12A 12FLA<br>72LRA|

15

4.  IR33

##### **<u>4.1  Dimensions</u>**

###### Appearance and ergonomics:

The appearance has been designed to fit in harmoniously with the new lines of the refrigeration units.

The main characteristic is its compactness: the dimensions are in fact 34.4 x 76.2 x 65 mm, and 34.4 x 76.2 x 79 mm for the version with traditional transformer. The drilling templates for both versions are 29 x 71 mm.

||76.2|70.5<br>79<br>1||
|---|---|---|---|
|38.6|34.4||3|
||80.6|56.5||
|ey:<br>. version O, L, H;<br>. version E, A;<br>. drilling template 71x29 mm<br>**4.2  Electrical specifica**|**tions**|65<br>2<br>Fig. 4.a||
||voltage||power|
|Power supply|E:<br>230 V~ 50/60|Hz;|3 VA,25 mA~ max|
||A:<br>115 V~ 50/60<br>|Hz;|3 VA,50 mA~ max|
|Insulation guaranteed by the power|voltage||power|
|<br>supply|E, A:insulation from<br>insulation fro<br>for I, L, M, N<br>insulation fro<br>for A, B, C, D,|very low voltage parts<br>m relay outputs for model E, A,<br>connections only<br>m relay outputs for model E, A,<br>E, F, G, H connections only|reinforced; 6 mm air, 8 mm surface; 3750 V insulation<br>basic; 3 mm air, 4 mm surface; 1250 V insulation<br>basic; 3 mm air, 4 mm surface; 1250 V insulation|
|Inputs|S1<br>NTC or PTC,d<br> <br>|ependingon the model<br>||
||S2<br>NTC or PTC,d|ependingon the model||
||DI1<br>voltage-free co<br>S3                           dependingon|ntact, contact resistance < 10Ω, closing c<br>the model|urrent 6 mA NTC or PTC|
||DI2<br>voltage-free co<br>S4<br>dependingon<br>|ntact, contact resistance < 10Ω, closing c<br>the model<br>|urrent 6 mA NTC or PTC|
||Maximum distance between probe<br>Note:in the installation, keep the p<br>cables.|s and digital inputs less than 10 m<br>ower supply and load connections separa|te from the probe, digital inputs, repeater display and supervisor|
|Type of probe|Standard Carel NTC<br> <br>|10 kΩat 25 °C, range -50T90 °C<br>measurement error: 1 °C in the ra<br>3 °C in the ra|nge -50T50 °C<br>nge +50T90 °C|
||High temperature NTC<br> <br>|50 kΩat 25 °C, range -40T150  °C<br>measurement error: 1.5 °C in the r<br>4 °C in the ra|<br>ange -20T115 °C<br>nge outside of -20T115 °C|
||Standard Carel PTC|985Ωat 25°C range -50T150 °C||
||<br>(specific model)|,<br>measurement error: 2 °C in the ra|nge -50T50 °C|
||i<br> <br>|<br>4 °C in the ra|<br>nge +50T150 °C|
|Relay outputs|dependingon the model|||
|||EN60730-1<br><br>|UL 873<br> <br><br>|
||modello<br>IRxxxx(EA)(PQSUVXYZ)xxx|relè<br>250V~<br>R2 (*)<br>5 (1) A|cicli di manovra<br>250V~<br>cicli di manovra<br>100000<br>5A res 1FLA 6LRA C300<br>30000|
||,,,,,,,,<br>IRxxxx(E,A)(N,R,C,B,A,M,L,T)xxx|<br> <br>R3(*)<br>5 (1) A|<br><br>100000<br>5A res 1FLA 6LRA C300<br>30000|
||IRxxxx(E,A)(N,R,C,B,A,M,L,T)xxx<br>IRxxxx(0,L,H)(N,R,C,B,A,M,L,T)xxx<br>|R1,R2<br>R2,R3,R4<br><br>8 (4) A su N.O.<br>6 (4) A su N.C.<br>|100000<br>8A res 2FLA 12LRA C300<br>30000|
||IRxxxx(0,L,H)(H,I,E,F,G,K,O,W))xxx|R2,R3,R4(*)<br>2 (2) A su N.O. e N.C.||
||IRxxxx(E,A)(P,Q,S,U,V,X,Y,Z)xxx<br>IRxxxx(0LH)(NRCBAMLT)xxx0|<br>R1<br>R1(*)<br>12 (2) A su N.O. e N.C.|100000<br>12A res 5FLA 30LRA C300 30000|
||,,,,,,,,,<br>IRxxxx(0,L,H)(H,I,E,F,G,K,O,W))xxx|R1<br>10 (10) A|100000<br>12A res 12FLA 72LRA<br>Toff minimum 60 seconds<br>30000|

Key:

1. version O, L, H;

2. version E, A;

3. drilling template 71x29 mm

##### **<u>4.2  Electrical specifications</u>**

(*): relay not suitable for fluorescent loads (neon lights, ...) that use starters (ballasts) with phase-shift capacitors. Fluorescent lamps with electronic control devices or without phase-shift capacitors can be used, within the operating limits specified for each type of relay. insulation from very low voltage parts reinforced; 6 mm air, 8 mm surface; 3750 V insulation insulation between the relay outputs indipendent basic; 3 mm clearance, 4 mm creepage; 1250 V insulation

16

||voltage<br>power|
|---|---|
|Connections|Type of connection<br>Cross-sections<br>Max current.<br>i|
||fixed screw 16A<br>for cables from 0.5 to 4.2 mm<sup>2</sup><br>16A<br>i|
||fixed screw<br>for cables from 0.5 to 2.5  mm<sup>2</sup><br>12A<br>estraibiliper blocchetti a vite|
||The correct sizing of the power and connection cables between the instrument and the loads is the responsibility of the installer.<br>Depending on the model, the maximum current at the common terminals is 12A or 16A. In the max load and max operating temp. conditions,<br>the cables used must be suitable for operation upto 105°C.|
|Case|plastic:<br>E, A dimensions 34.4x76.2x65 mm  -  mounting depth 56.5 mm<br>O,L,H  dimensions 34,4x76,2x79 mm  -  mountingdepth 70,5 mm|
|Assembly|smooth,hard and indeformablepanel: side fasteningbrackets,to bepressed in fully|
||drillingtemplate: dimensions 28.8 ± 0.2 x 70.8 ± 0.2 mm|
|Display|digits: 3 digit LED|
||display: from -99 to 999|
||operatingstatus: indicated withgraphic icons on the display|
|Keypad|4 silicone rubber buttons|
|Infrared receiver|available dependingon the model|
|Clock with backupbattery|available dependingon the model|
|Buzzer|available in all models|
|Clock|error at 25 °C:<br>± 10ppm(±5.3 min/year)|
||error in the temperature range -10T60 °C:<br>- 50ppm(-27min/year)|
||ageing:<br>< ± 5ppm(±2.7 min/year)|
||discharge time:<br>typically6 months(8 months maximum)|
||recharge time:<br>typically5 hours(< 8 hours maximum)|
|Operating temperature|IRxxxx(E,A)(P,Q,S,U,V,X,Y,Z)xxx<br>IRxxxx(E,A,0,L,H)(N,R,C,B,A,M,L,T)xxx<br>IRxxxx(0,L)(H,I,E,F,G,K,O,W))xxx<br>-10T60 °C|
|Operatinghumidity|<90% RH non-condensing|
|Storage temperature|-20T70 °C|
|Frontpanel index ofprotection|assemblyon smooth and indeformablepanel with IP65gasket|
|Environmentalpollution|2,normal situation|
|PTI of insulatingmaterials|printed circuits 250, plastic and insulatingmaterials 175|
|Period of stress across the insulating parts|long|
|Categoryof resistance to fire|categoryD and categoryB(UL 94-V0)|
|Class ofprotection against voltage surges|categoryII|
|Type of action and disconnection|1B relaycontacts(micro-disconnection)|
|Construction of the control device|electronic control device incorporated|
|Classification according to protection<br>against electric shock|class II when appropriately integrated|
|Device designed to he hand-held or<br>|no|
|integrated into equipment designed to<br>be hand-held||
|Software class and structure|class A|
|Cleaning the front panel of the instru-<br>ment|only use neutral detergents and water|
|Serial interface for CAREL network|External,available in all models|
|Programmingkey|Available in all models|

Table 4.a

17

##### **<u>4.3  Electrical connections</u>**

IRxxC(0,7) H (N,R,C,B) (0,2)xx

Maximum total current on terminal 3: 12 A

*[Figurtekst: N R1 R2 R3 R4 · R3 R4 AUX L EN60730-1 12 (2) A 8 (4) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA 8A 2FLA 8A 2FLA · 13 14 15 16 17 18 30LRA 12LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · L N tLAN · N L PROBES DI DI interface · 115...230 V~ 50mA~ max]*

IRxxF(0,7) (E,A) (N,R,C,B) (0,1,2,3,5)xx Maximum total current on terminal 1: 12 A

*[Figurtekst: R1 R2 R3 · EN60730-1 8 (4) A 8 (4) A 5 (1) A · UL 873 250 V~ 8A 2FLA 8A 2FLA 5A 1FLA · 12LRA 12LRA 6LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · L 1 2 1 · N L N · R3 R1 R2 PROBES DI · IRxxxxExxxx: 230 V~ 25mA~ max · IRxxxxAxxxx: 115 V~ 50mA~ max]*

###### IRxxC(0,7) (0,L) (N,R,C,B) (0,2)xx Maximum total current on terminal 3: 12 A

*[Figurtekst: N R1 R2 R3 R4 · R3 R4 AUX L EN60730-1 12 (2) A 8 (4) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA 8A 2FLA 8A 2FLA · 13 14 15 16 17 18 30LRA 12LRA 12LRA 12LRA · SERIAL · -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · tLAN · N L PROBES DI DI interface · IRxxxx0xxxx: 12 V~ 300mA~ max, 12...18 Vdc 300mAdc max · IRxxxxLxxxx: 12...24 V~ 300mA~ max, 12...30 VDC 300mAdc max]*

IRxxF(0,7) H (N,R,C,B) (0,2)xx Maximum total current on terminal 3: 12 A

*[Figurtekst: N R1 R2 R3 · R3 L EN60730-1 12 (2) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA 8A 2FLA · 13 14 15 30LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · tLAN · L N · N L PROBES DI DI interface · 115...230 V~ 50mA~ max]*

IRxxF(0,7) (0,L) (N,R,C,B) (0,2)xx Maximum total current on terminal 3: 12 A

*[Figurtekst: N R1 R2 R3 · R3 L EN60730-1 12 (2) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA 8A 2FLA · 13 14 15 30LRA 12LRA 12LRA · SERIAL · -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · tLAN · N L PROBES DI DI interface · IRxxxx0xxxx: 12 V~ 300mA~ max, 12...18 Vdc 300mAdc max · IRxxxxLxxxx: 12...24 V~ 300mA~ max, 12...30 Vdc 300mAdc max]*

IRxxM(0,7) (E,A,0) (N,R,C,B) (0,1,2,3,5)xx (NO R1) IRxxM(0,7) (E,A) (A,M,L,T) (0,1,2,3,5)xx

*[Figurtekst: R1 · EN60730-1 8 (4) A · UL 873 250 V~ 8A 2FLA12LRA SERIAL · and KEY · SUPPLYPOWER -10T60 · 1 2 3 4 7 8 9 10 11 12 · L R1 AUX 1 2 1 · N · L N · PROBES DI · IRxxxxExxxx: 230 V~ 25mA~ max · IRxxxxAxxxx: 115 V~ 50mA~ max · IRxxMx0(N,R,C,B)xxx: 12 V~ 300mA~ max, 12...18 Vdc 300mAdc max]*

IRxxM(0,7) (L) (N,R,C,B) (0,2)xx (NO R1)

IRxxM(0,7) (0,L) (A,M,L,T) (0,2)xx

*[Figurtekst: R1 · EN60730-1 12 (2) A · UL 873 250 V~ 12A 5FLA · 30LRA SERIAL · and KEY · -10T60 · 1 2 3 6 7 8 9 10 11 12 · R1 AUX · 1 2 1 2 · N L PROBES DI DI · IRxxxx0xxxx: 12 V~ 300mA~ max, 12...18 Vdc 300mAdc max · IRxxxxLxxxx: 12...24 V~ 300mA~ max, 12...30 Vdc 300mAdc max]*

ir 33 platform “connecti ons” +030 220447 - rel. 2.3 - 31.05.2016

18

IRxxS(0,7) (E,A) (N,R,C,B) (0,1,2,3,5)xx (NO R2) IRxxS(0,7) (E,A) (A,M,L,T) (0,1,2,3,5)xx Maximum total current on terminal 1: 12 A

*[Figurtekst: R1 R2 · EN60730-1 8 (4) A 8 (4) A · UL 873 250 V~ 8A 2FLA 8A 2FLA · 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · L AUX 1 2 1 · N L N · R1 R2 PROBES DI · IRxxxxExxxx: 230 V~ 25mA~ max · IRxxxxAxxxx: 115 V~ 50mA~ max · IRxxS(0,7) H (A,M,L,T) (0,2) xx · Maximum total current on terminal 3: 12 A · R1 R2 · EN60730-1 12 (2) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA · 30LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 AUX · 1 2 1 2 · tLAN · L N · N L PROBES DI DI interface · 115...230 V~ 50mA~ max]*

IRxxY(0,7) (E,A) (N,R,C,B) (0,1,2,3,5)xx (NO R3) IRxxY(0,7) (E,A) (A,M,L,T) (0,1,2,3,5)xx Maximum total current on terminal 1: 12 A

*[Figurtekst: R1 R2 R3 · EN60730-1 8 (4) A 8 (4) A 5 (1) A · UL 873 250 V~ 8A 2FLA 8A 2FLA 5A 1FLA · 12LRA 12LRA 6LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · L AUX 1 2 1 · N L N · R3 R1 R2 PROBES DI · IRxxxxExxxx: 230 V~ 25mA~ max · IRxxxxAxxxx: 115 V~ 50mA~ max]*

IRxxY(0,7) H (N,R,C,B) (0,2)xx (NO R3) IRxxY(0,7) H (A,M,L,T) (0,2)xx Maximum total current on terminal 3: 12 A

*[Figurtekst: N R1 R2 R3 · AUX R3 L EN60730-1 12 (2) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA 8A 2FLA · 13 14 15 30LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · tLAN · L N · N L PROBES DI DI interface · 115...230 V~ 50mA~ max]*

IRxxS(0,7) (E,A) (P,Q,S,U) (0,1,2,3,5)xx (NO R2) IRxxS(0,7) (E,A) (V,X,Y,Z) (0,1,2,3,5)xx Maximum total current on terminal 5: 12 A

*[Figurtekst: R1 R2 · EN60730-1 12 (2) A 5 (1) A · UL 873 250 V~ 12A 5FLA 5A 1FLA · 30LRA 6LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 3 4 5 6 7 8 9 10 11 12 · L · AUX 1 2 1 · N R2 R1 L N PROBES DI tLANinterface · IRxxxxExxxx: 230 V~ 25mA~ max · IRxxxxAxxxx: 115 V~ 50mA~ max]*

IRxxS(0,7) (0,L) (N,R,C,B) (0,2)xx (NO R3) IRxxS(0,7) (0,L) (A,M,L,T) (0,2)xx Maximum total current on terminal 3: 12 A

*[Figurtekst: R1 R2 · EN60730-1 12 (2) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA · 30LRA 12LRA · SERIAL · -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 AUX · 1 2 1 2 · tLAN · N L PROBES DI DI interface · IRxxxx0xxxx: 12 V~ 300mA~ max, 12...18 Vdc 300mAdc max · IRxxxxLxxxx: 12...24 V~ 300mA~ max, 12...30 Vdc 300mAdc max]*

IRxxY(0,7) (E,A) (P,Q,S,U) (0,1,2,3,5)xx Maximum total current on terminal 5: 12 A

*[Figurtekst: R1 R2 · EN60730-1 12 (2) A 5 (1) A · UL 873 250 V ~ ac 12A 5FLA 5A 1FLA · 30LRA 6LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 3 4 5 6 7 8 9 10 11 12 · L · 1 2 1 · N L N · R2 R1 PROBES DI · IRxxxxExxxx: 230 V~ 25mA~ max · IRxxxxAxxxx: 115 V~ 50mA~ max]*

###### IRxxY(0,7) (0,L) (N,R,C,B) (0,2)xx (NO R3) IRxxY(0,7) (0,L) (A,M,L,T) (0,2)xx Maximum total current on terminal 3: 12 A

*[Figurtekst: N R1 R2 R3 · AUX R3 L EN60730-1 12 (2) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 5FLA 8A 2FLA 8A 2FLA · 13 14 15 30LRA 12LRA 12LRA · SERIAL · -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · N L PROBES DI DI · IRxxxx0xxxx: 12 V~ 300mA~ max, 12...18 Vdc 300mAdc max · IRxxxxLxxxx: 12...24 V~300mA~ max, 12...30 Vdc 300mAdc max]*

Fig. 4.b

19

5.  IR33POWER

##### **<u>5.1  Dimensions</u>**

See “Dimensions” for the chapter on the ir33.

##### **<u>5.2  Electrical specifications</u>**

|Power supply|voltage<br>power<br>model E:<br>230 V~ 50/60 Hz;<br>3 VA25 mA~ max|
|---|---|
||<br>  <br> , <br>model A:<br>115 V~ 50/60 Hz;<br>3 VA,50 mA~ max|
|Insulation guaranteed by the power|voltage<br>power|
|<br>supply|model E, A, H:<br>insulation from very low voltage parts:<br>reinforced; 6 mm air, 8 mm surface; 3750 V insulation<br>insulation from relay outputs for model<br>E, A for I, L, M, N connections only:<br>basic; 3 mm air, 4 mm surface; 1250 V insulation<br>insulation from relay outputs  with model|
||<br>E, A for A, B, C, D connections only:<br>Do not insulate from the power supply as one<br> phase is taken from the relaycommon|
|Inputs|S1<br>NTC or PTC,dependingon the model|
||S2<br>NTC or PTC,dependingon the model|
||DI1<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA|
||S3<br>NTC or PTC,dependingon the model|
||DI2<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA|
||S4<br>NTC or PTC,dependingon the model|
||Maximum distance between probes and digital inputs less than 10 m. Note: in the installation, keep the power supply and load connections|
||<br>separate from theprobe,digital inputs,repeater displayand supervisor cables.|
|Type of probe|NTC std. Carel<br>10 kΩat 25 °C, range –50 to 90 °C|
||<br>measurement error: 1 °C in the range –50 to 50 °C<br>3 °C in the range +50 to 90 °C|
||High temperature NTC<br>50 kΩat 25 °C, range –40 to 150 °C<br>|
||measurement error: 1.5 °C in the range –20 to 115 °C      4 °C C in the range outside of -20 to 115 °C|
||Std. Carel PTC (specific model)<br>985Ωat 25°C, range -50 to 150 °C|
||measurement error: 2 °C in the range –50 to 50 °C          4 °C in the range +50 to 150 °C|
|Relay outputs|<br>dependingon the model|
||R3<br>EN60730-1:<br>250 V~ 5(1) A;<br>100,000 operating cycles|
||UL 873:<br>250 V~ 1A res 1FLA 6LRA C300;<br>30,000 operatingcycles|
||R2<br>EN60730-1:<br>250 V~ 8(4) A on N.O.,  6(4) A on N.C.,  2(2) A on N.O. and N.C.; 100,000 operating cycles|
||UL 873:<br>250 V~ 12A res 5FLA 30LRA C300;<br>30000 operatingcycles|
||R1<br>EN60730-1:<br>250 V~ 10 (10) A;<br>100,000 operating cycles|
||UL 873:<br>250 V~ 12A res 12HP 72LRA;<br>30,000 operatingcycles|
||(*): relay not suitable for fluorescent loads (neon lights, ...) that use starters (ballasts) with phase-shift capacitors. Fluorescent lamps with<br>electronic control devices or withoutphase-shift capacitors can be used,within the operatinglimits specified for each type of relay.<br>insulation from verylow voltageparts<br>reinforced;6 mm air,8 mm surface;3750 V insulation|
||insulation between the relayoutputs independent basic;3 mm air,4 mm surface;1250 V insulation|
|Connections|Type of connection<br>Cross-sections<br>Maximum current|
||<br>fixed screw 16A<br>for cables from 0.5 to 4.5 mm²<br>16 A<br>i<br>|
||fixed screw<br>for cables from 0.5 to 2.5 mm²<br>12 A|
||i<br>plug-in for screw blocks<br>for cables from 0.5 to 2.5 mm²<br>12 A|
||The correct sizing of the power and connection cables between the instrument and the loads is the responsibility of the installer. Depending<br>on the model the maximum current at the common terminals is 12A or 16A. In the max load and max operating temp. conditions, the cables<br>|
||used must be suitable for operation upto 105°C.|
|Case|plastic =  O,L,H dimensions: 34.4x76.2x79 mm,<br>mountingdepth:  70.5 mm|
|Assembly|smoothhard and indeformablepanel:  side fasteningbracketsto bepressed in fully|
||,   ,  <br>drillingtemplate: dimensions 28.8±0.2 x 70.8±0.2 mm|
|Display|digits: 3 digit LED|
||display: from -99 to 999|
||<br>operatingstatus: indicated withgraphic icons on the display|
|Keypad|4 silicone rubber buttons|
|Infrared receiver|available dependingon the model|
|Clock with backupbattery|available dependingon the model|
|Buzzer|available in all models|
|Clock|Error at 25 °C:<br>± 10ppm(±5.3 min/year)|
||Error in the temperature range -10T60 °C:<br>- 50ppm(-27min/year)|
||Ageing:<br>< ± 5ppm(±2.7 min/year)|
||Discharge time:<br>typically6 months(8 months maximum)|
||Recharge time:<br>typically5 hours(< 8 hours maximum)|
|Operatingconditions|-10T60 °C;<90% RH non-condensing|
|<br>Storage conditions|<br>-20T70 °C;<90% RH non-condensing|
|Frontpanel index ofprotection|assemblyon smooth and indeformablepanel with IP65gasket|
|Environmentalpollution<br>PTI of insulatingmaterials|2,normal situation<br>printed circuits 250, plastic and insulatingmaterials 175|

20

Table 5.a

|Period of stress across the insulating parts<br>i|long|
|---|---|
|Categoryof resistance to fire|categoryD and categoryB(UL 94-V0)|
|Class ofprotection against voltage surges|categoryII|
|Type of action and disconnection|1B relaycontacts(micro-disconnection)|
|Construction of the control device|electronic control device incorporated|
|Classification according to protection<br>against electric shock|class II when appropriately integrated|
|Device designed to he hand-held or<br>integrated into equipment designed to be<br>hand-held|no|
|Software class and structure|class A|
|Cleaningthe frontpanel of the instrument|onlyuse neutral detergents and water|
|Serial interface for CAREL network|External,available in all models|
|Interface for repeater display|External,available in models withpower supplies H,L and 0|
|Maximum distance between interface and<br>display|10 m|
|Programmingkey|Available in all models|

The IR33 Power range fitted with the standard Carel NTC probe is compliant with standard EN 13485 on thermometers for measuring the air temperature in applications on units for the conservation and sale of refrigerated, frozen and deep-frozen food and ice cream. Designation of the instrument: EN13485, air, S, A, 1, -50T90°C. The standard Carel NTC probe is identifiable by the printed laser code on “WP” models, or the code “103AT-11” on “HP” models, both visible on the sensor part.

21

**<u>5.3  Electrical connections</u>** “RELE 2” MODELS WITH “DEPENDENT” COMMON

“RELE 2” MODELS WITH “INDEPENDENT” COMMON

*[Figurtekst: (connection A, B) · (connection C, D)]*

*[Figurtekst: (connection A, B) · (connection C, D)]*

Fig. 5.a

22

6.  IR33 2HP

##### **<u>6.1  Dimensions</u>**

See “Dimensions” for the chapter on the ir33.

##### **<u>6.2  Technical specifications</u>**

|P l|Model<br>Voltage<br>Power<br>d H<br>115230 V 5060 H<br>6 VA 50 A||
|---|---|---|
|ower suppy|mo :<br>mod L:<br>mod O:<br>... ~, / z<br>12...24 V~, 50/60 Hz, 12...30 Vdc<br>12 V~, 50/60 Hz, 12...18 Vdc<br>,  m~ ma<br>3 VA, 300 mA~ /m<br>Use only SELV powe|<br>Adc max<br>r supply|
||insulation in reference<br> <br>reinforced<br>||
||to very low voltage parts<br>6 mm clearance, 8<br>3750 V ilti|creepage|
||mod H:<br>nsuaon<br>insulation from relay outputs<br>basic<br>||
|Ilti td|3 mm clearance, 4|creepage|
|nsuaon guaranee<br>|<br>1250 V insulation||
|by the power supply|<br>insulation in reference<br>da garantire estern|amente|
||to very low voltage parts<br>con trasformatore|di sicurezza (SELV)|
||mod O, L:<br>insulation from relay outputs<br>reinforced||
||<br> <br>6 mm clearance, 8|creepage|
||3750 V insulation||
|Input|S1 (probe 1)<br>NTC (IRxxx0xxxxx) o NTC e PTC (IRxxx7xxxxx)||
||S2 (probe 2)<br>NTC (IRxxx0xxxxx) o NTC e PTC (IRxxx7xxxxx)||
||DI1<br>free contact, contact resistance < 10Ω, closing current 6 mA||
||S3 (probe 3)<br>NTC (IRxxx0xxxxx) o NTC e PTC (IRxxx7xxxxx)<br>||
||DI2<br>free contact, contact resistance < 10Ω, closing current 6 mA||
||S4 (probe 4)<br>  <br>NTC (IRxxx0xxxxx) o NTC e PTC (IRxxx7xxxxx)<br>||
||Maximum ditance of probes and digital inputs less than 10 m.||
||<br>Nota:during installation keep the power and loads connection separate from probe cables, digital input<br>system.<br> <br>|s, repeater display and supervisory|
|Probe type|NTC std. CAREL<br>10 kΩa 25 °C, range da –50T90 °C||
||measurement error:<br>1°Cin the –50T50°C<br>|range<br>|
||3°Cin the –50T90°C|range|
||<br>NTC high temperature<br>50 kΩa 25 °C, range da –40T150 °C<br>|<br>|
||measurement error<br>1,5°Cin the –20T115|°C range|
||<br>4 °C nel range esterno a<br>i|<br>-20T115 °C|
||PTC std. CAREL (specific model)<br>985Ωa 25 °C, range da -50T150 °C||
||measurement error<br>2 °Cin the–50T50 °C|range|
||4 °C in the  –50T150 °C|range|
|Relay outputs|Rating xdon the model IRxx(S,Y,F,C)x(0,L,H)(H,I,E,G,K,O,W)xxx||
||EN 60730-1<br>UL 873||
||relè<br>250 Vac<br>operating cycles<br>250 Vac|operating cycles|
||R1<br>10 (10)A<br>100000<br>12A resistive 12 FLA 72<br>LR, Toff minimum 60<br>seconds(*), pilot duty<br>C 300|30000|
||R2(**)<br>8 (4)A<br>100000<br>8A resistive 2 FLA 12 LRA,<br>pilot duty C300|<br>30000|
||<br>R3(**)<br>8 (4)A<br>100000<br>8A resistive 2 FLA 12 LRA,<br>|<br>30000|
||pilot duty C300||
||<br>R4(**)<br>8 (4)A<br>100000<br>8A resistive 2 FLA 12 LRA,<br>|<br>30000|
||pilot duty C300||
||<br>insulation from very low voltage parts reinforced<br>rinforzato: 6 mm i|n aria, 8 superficiali|
||3750 V isolament<br> <br>|o<br> i|
||insulation between the relay outputs indipendent<br>principale: 3 mm in aria|, 4 superficiali|
||<br>1250 V isolament<br>|o<br>|
||(*): between the OFF status and the following ON status of the relay at least 1 minute have to elapse<br>(**): Relay not suitable for fluorescent loads (neon lights, ...) that use starters (ballasts) with phase-sh<br>electroniccontroldevicesor withoutphase-shiftcapacitorscan beusedwithintheoperatinglimitssp|.<br>l          ift capacitors. Fluorescent lamps with<br>ecifiedforeachtypeof relay|
|Connections|,     <br>Type of connection<br>Cross-section|i     .<br>Max. current|
||Model<br>Rela<br>P Sul<br>Probes<br>for wires from 05 to|12 A|
||y<br>. ppy<br><br>,<br>2,5 mm<sup>2</sup><br>0<br>screw/faston<br>screw<br>screw||
||<br>2<br><br>bli<br>bl<br>bl||
||removae<br>removae<br>removae<br>the installer has to provide the correct dimensioning of the power supply and cable connection betw<br>Depending on the model, the maximum current in the common terminals 1, 3 or 5 is 12 A. When using the<br>tt d fll ld  bl fti  i ti tt f 105°C t lt|een the instruments and the loads.<br>controller at maximum operating|
|Case|emperaure an u oa, use caes eaurng a maxmum operang emperaure oa eas.<br>plastic<br>Models: O, L, H<br>dimensions|34,4 x 76,2 x 79 mm|

23

|||mount-in depth<br>70,5 mm|
|---|---|---|
|Mounting|smooth and stiff panel using side fastening brackets, pressed until stop||
||drilling template<br>|dimensions 28.8 ± 0.2 x 70.8 ± 0.2 mm<br>|
|Display|digits<br>|3 digit LED<br>|
||display range<br>|from–99 to 999<br>|
||operating status|indicated by graphic icons on the display|
|Keypad<br>|4 rubber silicon buttons<br>||
|No options<br>|mod H<br>||
|Infrared receiver<br>|mod I,F,K,W<br>||
|Clock with backup battery|mod E,F,O,W||
|Alarm or auxiliary relay<br> i|G,K,O,W<br>||
|Custom param. or firmware<br>|IRccxxxxxnx; cc customer; n custom made parameters list<br>||
|Package|IRxxxxxxxxi: blank singol; 1 or 5 multiple; K kit with probes<br>||
|Buzzer|available on all the models||
|Clock|error at 25°C<br>|±10 ppm (±5.3 min/year)|
||error in the temperature range-10T60°C<br>|-50 ppm (-27 min/year)<br>|
||ageing|< ±5 ppm (±2.7 min/year)|
||discharge time|typical 6 months (max. 8 months)|
||recharge time|typical 5 hours (<max. 8 hours)|
|Operating temperature<br>|-10T60 °C for the versions IRxxxx(0,L)(H,I,E,F,G,K,O,W)xx<br>-10T50°C for the versions IRxxxx(H)(H,I,E,F,G,K,O,W)xx<br>||
|Operating humidity|<90% r.H. non-condensing<br>||
|Storage temperature<br>|-20T70°C<br>||
|Storage humidity<br>|<90% relative humidity. non-condensing<br>||
|Front panel degree of protection<br>|montaggio a pann. liscio e indeform. con guarniz. IP65<br>||
|Control pollution status|2 (normal situation)||
|PTI of the insulating material<br>|printed circuit board 250, insulation 175<br>||
|Period of electric stress across insulating parts <br> i|long<br>||
|Heat and fire resistance category|category D and category B (UL 94-V0)||
|Class of protection against voltage surges<br>|category II<br>||
|Type of disconnection or interruption<br>|1.B relay contacts (micro-disconnection)<br>||
|Construction of control<br>i|incorporated control, electronically<br>||
|Classification according to protection against<br>electric shock|Class II, by appropriate incorporation||
|The control is either to be hand-held or is|no||
|intented for a hand-held equipment<br>|||
|Software class and structure|Class A||
|Front panel cleaning|use only neutral detergents and water||
|<br>Serial interface for CAREL network|<br>external, available on all models||
|Interface for repeater display|external, available on IRxxxx(0,L,H)xxxx||
|Maximum distance between interface and|10 m||
|display<br>|||
|Programming key|available on all models||
|||Table 6.a|

24

##### **<u>6.3  Electrical connections</u>**

*[Figurtekst: IRxxS*H (G,K,O,W)*0 · Corrente massima totale su terminale 3: 12A · Maximum current on terminal 3: 12A · R1 R2 · EN60730-1 10 (10) A 8 (4) A · UL 873 250 V~ 12A 12FLA 8A 2FLA · 72LRA 12LRA · SERIAL · SUPPLYPOWER -10T50 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 AUX · 1 2 1 2 · N L N tLAN · L PROBES DI DI interface · 115...230 V~ 50mA~ max]*

*[Figurtekst: IRxxC* H (H,I,E,F)*0 · IRxxF* H (H,I,E,F)*0 senza/ without R4 · Corrente massima totale su terminale 3: 12A · Maximum current on terminal 3: 12A · R3 R4 AUX NL EN60730-1 10 ( R1 10) A 8  R2 (4) A 8 ( R3 4) A 8  R4 (4) A · UL 873 250 V~ 12A 12FLA 8A 2FLA 8A 2FLA 8A 2FLA · 13 14 15 16 17 18 72LRA 12LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T50 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · N L N tLAN · L PROBES DI DI interface · 115...230 V~ 50mA~ max · IRxxS* (L,0) (G,K,O,W) *0 · IRxxS* (L,0) (H,I,E,F)*0 senza/ without R2 · Corrente massima totale su terminale 3: 12A · Maximum current on terminal 3: 12A · R1 R2 · EN60730-1 10 (10) A 8 (4) A · UL 873 250 V~ 12A 12FLA 8A 2FLA · 72LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · L · AUX 1 2 1 2 · N R1 R2 L N PROBES DI tLANinterface · IRxxxx0xxxx: 12 V~, 300mA~ max · 12...18VDC, 300mADC max · IRxxxxLxxxx: 12/24 V~ 300mA~ max · 12...30VDC, 300mADC max]*

*[Figurtekst: IRxxY*H (G,K,O,W)*0 · IRxxY*H (H,I,E,F)*0 senza/ without R3 · Corrente massima totale su terminale 3: 12A · Maximum current on terminal 3: 12A · N R1 R2 R3 · R3 AUX L EN60730-1 10 (10) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 12FLA 8A 2FLA 8A 2FLA · 13 14 15 72LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T50 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · N L N tLAN · L PROBES DI DI interface · 115...230 V~ 50mA~ max]*

*[Figurtekst: IRxxM*(L,0) (G,K,O,W)*0 · R1 · EN60730-1 10 (10) A · UL 873 250 V~ 12A 12FLA72LRA SERIAL · and KEY · SUPPLYPOWER -10T60 · 1 2 3 4 5 6 7 8 9 10 11 12 · tLAN · R1 AUX 1 2 1 2 interface · N L L N · PROBES DI · IRxxxx0xxx: 12 V~  300mA~ max · 12...18VDC, 300mADC max · IRxxxxLxxx: 12/24 V~ 300mA~ max · 12...30VDC, 300mADC max]*

*[Figurtekst: IRxxY* (L,0) (G,K,O,W) *0 · IRxxY* (L,0) (H,I,E,F) *0 senza/ without R3 · Corrente massima totale su terminale 3: 12A · Maximum current on terminal 3: 12A · N R1 R2 R3 · R3 AUX L EN60730-1 10 (10) A 8 (4) A 8 (4) A · UL 873 250 V~ 12A 12FLA 8A 2FLA 8A 2FLA · 13 14 15 72LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · N L N tLAN · L PROBES DI interface · IRxxxx0xxx: 12V~, 300mA~ max · 12...18VDC, 300mADC max · IRxxxxLxxx: 12/24V~, 300mA~ max · 12...30VDC, 300mADC max]*

*[Figurtekst: IRxxC* (L,0) (H,I,E,F)*0 · IRxxF* (L,0) (H,I,E,F)*0 senza/ without R4 · Corrente massima totale su terminale 3: 12A · Maximum current on terminal 3: 12A · R3 R4 AUX NL EN60730-1 10  R1 (10) A 8  R2 (4) A 8  R3 (4) A 8 ( R4 4) A · UL 873 250 V~ 12A 12FLA 8A 2FLA 8A 2FLA 8A 2FLA · 13 14 15 16 17 18 72LRA 12LRA 12LRA 12LRA · SERIAL · SUPPLYPOWER -10T60 and KEY · 1 2 3 4 5 6 7 8 9 10 11 12 · R1 R2 · 1 2 1 2 · N L N tLAN · L PROBES DI interface · IRxxxx0xxx: 12V~, 300mA~ max · 12...18VDC, 300mADC max · IRxxxxLxxx: 12/24V~, 300mA~ max · 12...30VDC, 300mADC max]*

Fig. 6.a

25

7.  IR33DIN

##### **<u>7.1  Dimensions</u>**

The dimensions of the ir33DIN are 60x111x70.4 mm for all versions, with the drilling template measuring 40x70 mm.

###### DIN rail assembly

*[Figurtekst: 70.4 60 · HACCP · DIN · 111]*

Fig. 7.a

##### **<u>7.2  Electrical specifications</u>**

||voltage<br>power|
|---|---|
|Power supply|model E:<br>230 V~ 50/60 Hz;<br>3 VA,25 mA~ max|
||model A:<br>115 V~ 50/60 Hz;<br>3 VA,50 mA~ max|
||model H:<br>115-230 V~ 50/60 Hz;<br>6 VA,50 mA~ max|
||model L:<br>12...24 V~ 50/60 Hz;<br>4 VA, 300 mA~ max<br> <br>|
||12 Vdc, 12 - 30 Vdc<br>TRADR4W012 transformer, 315 mA slow-blow fuse in secondary,<br>onlyuse SELVpower supply|
||model O:<br>12 V~ 50/60 Hz;<br>4 VA, 300 mA~ max<br>12 Vdc, 12 - 18 Vdc<br>TRADR4W012 transformer, 315 mA slow-blow fuse in secondary,<br>onlyuse SELVpower supply|
|Insulation guaranteed by the power|voltage<br>power|
|supply|model E, A, H:<br>insulation from very low voltage parts:<br>reinforced; 6 mm air, 8 mm surface; 3750 V insulation<br>insulation from relayoutputs:<br>basic;3 mm air,4 mm surface;1250 V insulation|
||model O, L:<br>insulation from very low voltage parts:<br>to be guaranteed externally by safety transformer<br>insulation from relayoutputs:<br>basic;6 mm air,8 mm surface;3750 V insulation|
|Inputs|S1<br>NTC or PTC,dependingon the model|
||S2<br>NTC or PTC,dependingon the model|
||DI1<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S3<br>NTC or PTC,dependingon the model|
||DI2<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S4<br>NTC or PTC,dependingon the model|
||DI3<br>voltage-free contact, contact resistance < 10 ohm, closing current 6 mA<br>S5<br>NTC or PTC,dependingon the model|
||Maximum distance between probes and digital inputs less than 10 m<br>Note:in the installation, keep the power supply and load connections separate from the probe, digital inputs, repeater display and supervisor<br>cables.|
|Type of probe|Std. Carel NTC<br>10 kΩat 25 °C, range -50 to 90 °C<br>measurement error: 1 °C in the range -50 to 50 °C<br>3 °C in the range +50 to 90 °C|
||High temperature NTC<br>50 kΩa 25 °C, range -40 to 150 °C<br>measurement error: 1.5 °C in the range -20 to 115 °C<br>4 °C in the range outside of -20 to 115 °C|
||Std. Carel PTC (specific model)<br>985Ωat 25°C, range -50 to 150 °C<br>measurement error: 2 °C in the range -50 to 50 °C<br>4 °C in the range +50 to 150 °C|
|Relay outputs|dependingon the model|
||8 A (*)<br>EN60730-1:<br>250 V~ 8(4) A on N.O., 6(4) A on N.C., 2(2) A on N.O. and N.C.;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 8A res 2FLA 12LRA C300;<br>30,000 operatingcycles|
||16 A (*)<br>EN60730-1:<br>250 V~ 10(4) on up to 60 °C on N.O., 12(2) A on N.O. and N.C.;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 5FLA 30LRA C300;<br>30,000 operatingcycles|
||2HP<br>EN60730-1:<br>250 V~ 10 (10) A;<br>100,000 operating cycles<br>UL 873:<br>250 V~ 12A res 12FLA 72LRA;<br>30,000 operatingcycles|
||(*): Relay not suitable for fluorescent loads (neon lights, ...) that use starters (ballasts) with phase-shift capacitors. Fluorescent lamps with<br>electronic control devices or withoutphase-shift capacitors can be used,within the operatinglimits specified for each type of relay.|
||insulation from verylow voltageparts<br>reinforced;6 mm air,8 mm surface;3750 V insulation|
||insulation between the separate relayoutputs<br>basic;3 mm air,4 mm surface;1250 V insulation|

26

||voltage<br>power||
|---|---|---|
|Connections|Type of connection<br>Cross-sections<br>i|Maximum current|
||fixed screw 16A<br>for cables from 0.5 to 2.5 mm2|12 A|
||i<br>plug-in for screw blocks<br>for cables from 0.5 to 2.5 mm2|12 A|
||spade with crimped contact<br>for cables from 0.5 to 2.5 mm2|12 A|
||Wire cross-section forprobes and digital inputs<br>0.5 to 2.5 mm2(from 20 to 13 AWG)||
||Wire cross-section forpower supplyand loads<br>1.5 to 2.5 mm2(from 15 to 13 AWG)||
||The correct sizing of the power and connection cables between the instrument and the loads is th<br>In the max load and max operatingtemp. conditions,the cables used must be suitable for operati|e responsibility of the installer.<br>on upto 105°C.|
|Case|plastic<br>dimensions: 111x70.4x60 mm||
|Assembly|DIN rail:<br>usingbuilt-in fasteningsystem||
||drillingtemplate for frontpanel:<br>dimensions 45x70mm||
|Display|digits: 3 digit LED||
||display: from -99 to 999||
||operatingstatus: indicated withgraphic icons on the display||
|Keypad|4 silicone rubber buttons||
|Infrared receiver|available dependingon the model||
|Clock with backupbattery|available dependingon the model||
|Buzzer|available in all models||
|Clock|Error at 25 °C:<br>± 10ppm(±5.3 min/year)||
||Error in the temperature range -10T60 °C:<br>- 50ppm(-27min/year)||
||Ageing:<br>< ± 5ppm(±2.7 min/year)||
||Discharge time:<br>typically6 months(8 months maximum)||
||Recharge time:<br>typically5 hours(< 8 hours maximum)||
|Operating conditions|power supply  O, L, H:<br>-10T55 °C;  <90% RH non-condensing<br>power supplyE,A:<br>-10T50 °C;<90% RH non-condensing||
|Storage conditions|-20T70 °C;<90% RH non-condensing||
|Frontpanel index ofprotection|frontpanel IP40,complete controller IP20||
|Environmentalpollution|2,normal situation||
|PTI of insulatingmaterials|printed circuits 250, plastic and insulatingmaterials 175||
|Period of stress across the insulating parts|long||
|Categoryof resistance to fire|categoryD and categoryB(UL 94-V0)||
|Class ofprotection against voltage surges|categoryII||
|Type of action and disconnection|1B relaycontacts(micro-disconnection)||
|Construction of the control device<br>i|electronic control device incorporated||
|Classification according to protection|class II when appropriately integrated||
|against electric shock|||
|Device designed to he hand-held or|no||
|integrated into equipment designed to be<br>hand-held|||
|Software class and structure|class A||
|Cleaningthe frontpanel of the instrument|onlyuse neutral detergents and water||
|Serial interface for CAREL network|Built-in,available in all models,upon request||
|Interface for repeater display|Built-in,available in all models,upon request||
|Maximum distance between interface|10 m||
|and display|||
|Programmingkey|Available in all models||

Table 7.a

###### EN13485 certification

The ir33 platform range fitted with the standard Carel NTC probe is compliant with standard EN 13485 on thermometers for measuring the air temperature in applications on units for the conservation and sale of refrigerated, frozen and deep-frozen food and ice cream.

Designation of the instrument: EN13485, air, S, A, 1, -50 +90°C. The standard Carel NTC probe is identifiable by the printed laser code on “WP” models, or the code “103AT-11” on “HP” models, both visible on the sensor part.

27

**<u>7.3  Electrical connections</u>**

###### **DN33 (S,Y,F)*0,L (N-R-C-B)*0 senza/** **_without R3_ DN33 (S,T)*0,L (A-M-L-T)*0**

*[Figurtekst: R2 10 (4) A R5 8 (4) A · 8A 2FLA 12LRA 8A 2FLA 12LRA · R2]*

*[Figurtekst: R5 · POWER 12/24 V~ 300mA~ max · SUPPLY 12V~ 300mA~ max]*

###### **DN33 (S,Y,F)*0,L (H-I-E-F)*0 senza/** **_without R3_ DN33 (S,T)*0,L (G-K-O-W)*0**

*[Figurtekst: R2 R5 · 10 (10) A 10 (4) A 8 (4) A · 12A 12FLA 72LRA 12A 5FLA 30LRA 8A 2FLA 12LRA · R2 · R5 · POWER 12/24 V~ 300mA~ max · SUPPLY 12V~ 300mA~ max]*

###### **DN33(S,Y,F)*H (N-R-C-B)*0 senza** **_/ without R3_ DN33(S,Y)*H (A-M-L-T)*0**

*[Figurtekst: R2 R5 · 10 (10) A 10 (4) A 8 (4) A · 12A 12FLA 72LRA 12A 5FLA 30LRA 8A 2FLA 12LRA · R2 AUX1 R3 · R5 · SUPPLYPOWER 115/230 V~ 50mA~ max]*

###### **DN33(C)*(0,L) (N-R-C-B)*0 senza/** **_without R4_ DN33(H)*(0,L) (N-R-C-B)*0**

*[Figurtekst: R2 R5 · 10 (4) A R4 8 (4) A 8 (4) A · 12A 5FLA 30LRA 8A 2FLA 12LRA 8A 2FLA 12LRA · R2 AUX2 R4 AUX1 R3 · R5 · POWER 12/24 V~ 300mA~ max · SUPPLY 12V~ 300mA~ max]*

###### **DN33(C,M)*(0,L) (H-I-E-F)*0 senza/** **_without R3_**

*[Figurtekst: R2 R5 · 10 (10) A 10 (4) A R4 8 (4) A 8 (4) A · 12A 12FLA 72LRA 12A 5FLA 30LRA 8A 2FLA 12LRA 8A 2FLA 12LRA · R2 AUX2 R4 AUX1 R3 · R5 · POWER 12/24 V~ 300mA~ max · SUPPLY 12V~ 300mA~ max]*

###### **DN33(C)*H (N-R-C-B)*0 senza/** **_without R4_ DN33(H)*H (N-R-C-B)*0**

*[Figurtekst: R2 R5 · 10 (10) A 10 (4) A R4 8 (4) A 8 (4) A · 12A 12FLA 72LRA 12A 5FLA 30LRA 8A 2FLA 12LRA 8A 2FLA 12LRA · R2 AUX2 R4 AUX1 R3 · R5 · SUPPLYPOWER 115/230 V~ 50mA~ max]*

###### **DN33(S,Y,F)* (E-A) (N-R-C-B)*0 senza/** **_without R3_ DN33(S,Y,F)* (E-A) (A-M-L-T)*0**

*[Figurtekst: R2 R5 · 10 (4) A 10 (4) A 8 (4) A · 12A 5FLA 30LRA 12A 5FLA 30LRA 8A 2FLA 12LRA · R2 AUX1 R3 · R5 · POWER E: 230 V~ 25mA~ max · SUPPLY A: 115 V~ 50mA~ max]*

Fig. 7.b

28

Agenzia / _Agency_ :

**CAREL INDUSTRIES HQs** Via dell’Industria, 11 - 35020 Brugine - Padova (Italy) Tel. (+39) 049.9716611 -  Fax (+39) 049.9716600 e-mail: carel@carel.com - www.carel.com
