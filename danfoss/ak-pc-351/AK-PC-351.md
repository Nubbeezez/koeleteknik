# Danfoss AK-PC 351 – manualer til fejlfinding

Konverteret direkte fra Danfoss' officielle PDF-manualer i denne mappe. Tabeller (parametre, alarmkoder, menuer) er bevaret som Markdown-tabeller. Billeder er udeladt; tekst fra diagrammer står som *[Figurtekst: …]*.

## Sådan bruges filen (til Claude)

- Svar på dansk ud fra indholdet i denne fil, og angiv hvilken manual og hvilket afsnit svaret kommer fra.
- Alarm-, fejl- og parameterkoder kan søges direkte på koden.
- Samme kode kan betyde noget forskelligt på forskellige regulatorer. Tjek altid hvilken model teknikeren arbejder på.
- Står svaret ikke i manualerne, så sig det i stedet for at gætte.

## Indhold

1. Instructions AK-PC 351 – Dimensions
2. Data sheet – Pack controller AK-PC 351


---

## 1. Instructions AK-PC 351 – Dimensions

*Kilde: Danfoss-dokument AN11728641565202-000201.pdf*

### **Instructions AK-PC 351**

*[Figurtekst: IP 20 · -20 - 60°C · (0 - 140°F) · RH max. 90% non condensing · 080G0289 = 24 V a.c. / d.c. 9 VA]*

#### **Dimensions**

*[Figurtekst: DIN rail only (IP 20)]*

RI8RB2ML  09-2014

**ENGLISH**

#### **Connection, lower level**

#### **Supply Voltage**

24 V a.c. or 24 V d.c.

*[Figurtekst: All 24 V or · all 230 V a.c.]*

#### **Connection, upper level**

The supply voltage of AI **may not** share the signal with other controllers.

#### **AI - Analogue inputs, 4 pcs. AI1 - AI4**

- AI1- Sc3: Pt 1000 ohm, AKS 11 or AKS 21.

- AI2 - Sd compressor 1: NTC 86K ohm @ 25°C, from digital scroll or Pt 1000 ohm

#### **DO - Digital outputs, 6 pcs. DO1 - DO6**

#### DO6 is solid state relay.

The relays are de-rated to the specified values.

If an alarm relay is defined, it will be driven under normal operation and it will drop in the event of alarms and insufficient power to the controller.

*[Figurtekst: DO DO1-DO5 DO6 · I Max. 5 A 0,5 A · (2) min. 50 mA · Ioff < 1,5 mA · U All 24 V or · all 230 V a.c.]*

- AI3: Presure transmitter Po or temperature sensor S4, Pt 1000

- ohm

- AI4: Pressure transmitter Pc or temperature sensor S7, Pt 1000 ohm

#### Pressure transmitters

- Ratiometric: 10-90% of supply, AKS 32R / AKS 2050

- Signal: 1-5 V, AKS 32

- Current: 0-20 mA / 4-20 mA, AKS 33 (supply = 12 V)

#### **DI - Digital switch inputs, 8 pcs. DI1 - DI8**

The connection may be a shut-down or interruption function. Select what is to be activated during configuration.

DI1-4: Safety circuits, compressor 1, 2, 3 and 4

DI5: Safety circuits, condenser fans

- DI6: External Main Switch

*[Figurtekst: AKS 32R 10-90% ratiometric · AKS 32 1-5 V · 0-20mA · AKS 33 4-20mA]*

DI7: Night signal or LP switch

DI8 General alarm or HP switch

#### **AO - Analogue output, 2 pcs. AO1 - AO2**

Must be used when using a frequency converter or EC motors. Obtain 0-10 volts from terminals COM and AO1 (compressor), respectively COM and AO2 (fans).

#### **Modbus**

It i s important t hat the installation of the data communication cable be done correctly. Cf. separate literature No. RC8AC. Remember termination at the bus termination.


AK-PC 351

2

#### **The capacity from the digital scroll compressor**

The capacity is divided into period times as "PWM per". 100% capacity is delivered when cooling takes place for the whole period. An off time is required by the capacity control valve within the period and an on time is also permitted. There is "no cooling" when the valve is on.

The controller itself calculates the capacity needed and will then vary it according to the cut-in time of the capacity control valve. A limit is introduced if low capacity is needed so that the cooling does not go below 10%. This is because the compressor can cool itself. This value can be increased if necessary.

The capacity can similarly be limited so that the compressor cannot deliver 100% capacity. It is not normally necessary to limit this max. capacity.

#### Sd monitoring

When regulating with Sd monitoring, the controller will increase capacity if the temperature nears the Sd limit. This will result in better cooling of the digital scroll compressor.

*[Figurtekst: Refrigeration · No refrigeration · PWM  p eriod time · PWM Min. Cycle PWM Max. Cycle]*

#### **Stream kompressor**

The PWM signal can also be used to control one stream compressor with one relief valve.

The compressor capacity is distributed by up to 50% for one relay and the remaining 50-100% for the unloader. The unloader is connected to DO6.

Sd can be monitored like a scroll compressor.


AK-PC 351

3

**Português**

#### **Conexões, nível mais baixo**

#### **Conexões, nível superior**

**Todas 24 V ou todas 230 V c.a.**

#### **Advertência**

A tensão de alimentação do AI pode não compartilhar o sinal com outros controladores.

#### **Fonte de alimentação**

24 V c.a. **ou** 24 V c.c.

#### **AI - entradas analógicas, 4 pcs. AI1 - AI4**

AI1- Sc3: Pt 1000 ohm, AKS 11 ou AKS 21.

AI2 - Sd compressor 1: NTC 86K ohm @ 25°C, a partir de digital scroll ou Pt 1000 ohm

#### **DO - saídas digitais, 6 pcs. DO1 - DO6**

DO6 são relé de estado sólido.

É feito derate dos relés para os valores especificados.

Caso um relé de alarme seja definido, ele será acionado

AI3: Transmissor de pressão Po ou sensor de temperatura S4, Pt 1000 ohm

AI4: Transmissor de pressão Pc ou sensor de temperatura S7, Pt 1000 ohm

durante a operação normal e desarmará em caso de alarmes

e de tensão insuf i ciente para o controlado r.

*[Figurtekst: DO DO1-DO5 DO6 · I Max. 5 A 0,5 A · (2) mín. 50 mA · Ioff < 1,5 mA · U Todas 24 V ou · todas 230 V CA]*

#### Transmissores de pressão

- Ratiometric: 10-90% do fornecimento, AKS 32R / AKS2050

• Sinal: 1-5 V, AKS 32

• fonte de alimentação: 0-20 mA / 4-20 mA, AKS 33 (fornecimento = 12 V)

#### **DI - Entradas digital chave, 8 pcs. DI1 - DI8**

A conexão pode ser um desligamento ou função de interrupção. Selecione o que deverá ser ativado durante a configuração. DI1-4: Os circuitos de segurança, compressor1, 2, 3 e 4 DI5: Os circuitos de segurança, ventiladores do condensador DI6:External Interruptor principal

DI7: Sinal Noite ou chave BP

DI8 Alarme geral ou chave AP

*[Figurtekst: AKS 32R 10-90% ratiometric · AKS 32 1-5 V · 0-20mA · AKS 33 4-20mA]*

#### **AO - saída analógica, 2 pcs. AO1 - AO2**

Deverão ser utilizadas ao usar um conversor de frequência ou motores EC.

Obtenha 0-10 volts dos terminais COM e AO1 (compressor), respectivamente COM e AO2 (ventilador).

#### **Modbus**

É importante que a instalação do cabo de comunicação de dados seja feita corretamente. Consulte a literatura separada nº RC8AC… Lembre-se: terminação na terminação do barramento.


4

#### **A capacidade do compressor de rolagem digital**

A capacidade é dividida em períodos de tempo como “PWM per”. É fornecida 100% da capacidade quando o resfriamento acontece durante todo o período. Um tempo desligado é necessário para a válvula de bypass dentro do período e um tempo ligado também é permitido. Não há “resfriamento” quando a válvula estiver ligada.

O controlador por si próprio calcula a capacidade necessária e então irá variá-la de acordo com o tempo de ligar da válvula de controle de capacidade.

Um limite é introduzido se uma baixa capacidade for necessária de modo que o resfriamento não caia para baixo de 10%. Isto é porque o compressor pode resfriar-se a si próprio. Esse valor poderá ser aumentado, se necessário.

De modo análogo, a capacidade pode ser limitada, de maneira que o compressor não possa fornecer 100% da capacidade. Normalmente não é necessário limitar essa capacidade máxima.

#### Monitoramento Sd

Ao regular com o monitoramento Sd, o controlador irá aumentar a capacidade se a temperatura aproximar do limite Sd. Isso irá resultar em um melhor resfriamento do compressor de rolagem digital.

*[Figurtekst: Refrigeração · Sem refrigeração · PWM  p eriod time · PWM Min. Cycle PWM Max. Cycle]*

#### **Compressor de fluxo**

O sinal de PWM também pode ser usado para controlar um compressor de fluxo com uma válvula de descarregador. A capacidade do compressor é distribuída por até 50% para um relé e os restantes 50-100% para o descarregador. O descarregador está conectado em DO6.

O Sd pode ser monitorado como um compressor de rolagem.


AK-PC 351

5

The Product contains electrical components A nd may not be disposed together with domestic waste. Equipment must be separate collected with Electrical and Electronic waste. According to Local and currently valid legislation.


AK-PC 351

6

---

## 2. Data sheet – Pack controller AK-PC 351

*Kilde: Danfoss-dokument AI136086419666en-000201.pdf*

**Data sheet**

Pack controller AK-PC 351

### **Description**

The AK-PC 351 is a pack controller designed for managing compressor and condenser systems. It offers a range of features to ensure optimal performance and safety in refrigeration applications. The controller is equipped with multiple inputs and outputs, allowing for precise control and monitoring of various parameters. It supports MODBUS communication, making it compatible with other systems and devices. The AK-PC 351 is designed for easy installation and operation, with a user-friendly interface and robust construction.

#### **Features & bene�ts**

- Safety with low pressure protection

   - Ensures the system operates within safe pressure limits to prevent damage and maintain efficiency.

- Comprehensive compressor safeguards

   - Protects compressors from potential hazards, ensuring longevity and reliability.

- Efficient condenser management

   - Optimizes condenser pressure for improved energy efficiency and performance.

- Advanced temperature monitoring

- Monitors and controls the temperature of the suction gas to prevent overheating and ensure optimal operation.

- Maximize energy savings with heat recovery

Utilizes waste heat for other applications, enhancing overall energy efficiency.

- Smart load management

Reduces load during peak times to prevent system overload and save energy.

- Alerts with built-in buzzer

- Provides audible alerts for various system conditions, ensuring prompt attention and action.

- Optimize performance with P0 optimization

Fine-tunes system parameters for maximum efficiency and performance.

High pressure and discharge gas temperature safety

Protects the system from excessive pressure, ensuring safe and reliable operation. Monitors and controls the temperature of the discharge gas to prevent overheating and ensure optimal operation. User-friendly interface with built-in LCD display

Provides a clear and intuitive interface for easy monitoring and control.

*[Figurtekst: Applications · Application Description · Single step · Single step compressors of same size · Speed on lead · Speed compressor of one size single step compressors of another size · Digital scroll on lead · Digital scroll of one size single step compressors of another size · Stream 4 cycle on lead · Stream 4 cycle of on size single step compressors of another size · Multistep compressors · Multistep compressors with same no. of unloader valves and of same size]*

### **Ordering**

#### **Product code numbers**

|**Type**|**Supply voltage [V] AC**|**Supply voltage [V] DC**|**Communication type**|**Code number**|
|---|---|---|---|---|
|AK-PC 351|24|24|MODBUS|080G0289|

### **Product details**

#### **General data**

**Table: Technical data**

|**Features**|**Description**||
|---|---|---|
|**Supply voltage**|24 V AC ± 15% 50/60 Hz, 9 VA<br>24 V DC (20 – 60 V), 9 VA||
|**4 analog inputs**|Pressure measuring:<br>Ratiometric pressure transmitter type<br>1 – 5 volt pressure transmitter type A<br>0 – 20 (4 – 20) mA pressure transmitt|AKS 32R<br>KS 32<br>er type AKS 33|
||Temperature measurement<br>Pt 1000 ohm/0 °C<br>NTC - 86 K from digital scroll/stream||
|**8 digital inputs**|From contact function<br>E.g. to:<br>Start/stop of regulation<br>Monitoring of safety circuits<br>General alarm function||
|**Relay output to capacity control**|5 pcs. SPST (5 A)|AC-1: 5 A (ohmic)<br>AC-15: 2 A (inductive)|
||1 pc. solid state|Imax. = 0.5 A|
||PWM for scroll-unload|Imin. = 50 mA|
|||Leak < 1.5 mA<br>Not short-circuit protected|
|**2 voltage outputs**|0 – 10 V DC, Ri = 1 kohm||
|**Data communication**|Modbus for AK-SM 800||
|**Environments**|-20 – 60 °C, during operations||
||-40 – 70 °C, during transport||
||20 – 80% Rh, not condensed||
||No shock in�uence/vibrations||
|**Density**|IP20||
|**Weight**|0.2 kg||
|**Mounting**|DIN-rail||
|**Connection terminals**|Max. 2.5 mm<sup>2</sup>multi core||

### **Certi�cates, declarations and approvals**

The list contains all certi�cates, declarations, and approvals for this product type. Individual code number may have some or all of these approvals, and certain local approvals may not appear on the list.

When you click on the link you will be directed to the latest version of the ‘Declaration of Conformity’. Products developed and sold before this date of issue conform to the directives/standards in force at the time of their sale.

|**Approval type**|**Title**|**Certi�cation body**|**Approval topic**|
|---|---|---|---|
|EU-UK Declaration|Danfoss EU-UK 080R1224.02|Danfoss|LVD|
|Manufacturer's Declaration|Danfoss MD 080R4002.01|Danfoss|China RoHS|
|Export Control Declaration|Pack controllers (Mid End)|Danfoss||
|Manufacturer's Declaration|Danfoss MD 080R1237.01|Danfoss|EAEU RoHS|
|UA Declaration|Danfoss UA 8537|Danfoss|UA RoHS|
||UA 2024-06-27 electr.|||
|UA Declaration|protection units for|Danfoss|LVD|
||compressors|||
|EAC Declaration|ЕАС KZ 7100841.13.12.01062|EAC - Eurasian Customs Union|EMC|
|Electrical Safety Certi�cate|ЕАС KZ 7100841.01.01.01245|EAC - Eurasian Customs Union|LVD|
|Electrical Safety Certi�cate|UL E31024|UL - Underwriters Laboratories<br>inc.||

### **Contact details**

#### **Online support**

Danfoss offers a wide range of support along with our products, including digital information, software, mobile apps and expert guidance. See the possibilities below.

##### **The Danfoss Design center**

Discover the Design Center, our advanced digital platform that streamlines product selection. With integrated tools and enhanced type pages, it's simpler than ever to access product information and documentation, and to select the right products. Check the availability of Danfoss products at partner locations and enjoy seamless transitions from selection to purchase with our basket-to-basket functionality. Whether you're buying from our distributors or directly from the Product Store, the Design Center simpli�es your experience. Learn more at: designcenter.danfoss.com.

##### **The Danfoss product store**

The Danfoss Product Store is a one-stop shop available 24/7 for our customers, no matter where you are in the world or what area of industry you work in. Browse our catalog, check product details and documentation, view your prices and product availability, and quickly �nalize your purchase. Start browsing at: store.danfoss.com.

##### **Danfoss Partner Portal/Product Data tool**

Designed to support you with easy access to product data extracts, essential resources, tools, and information. The Partner Portal provides a centralized hub for product documentation, training materials, marketing assets, and technical support, ensuring you have everything you need to succeed and grow your business with Danfoss. The Partner Portal is available 24/7 at: partner.danfoss.com and is ready to support your business.

##### **Find technical documentation**

Find technical documentation you need to get your project up running. Get direct access to our official collection of data sheets, certi�cates and declarations, manuals and guides, 3D models and drawings, case stories, brochures, and much more. Start searching now at: documentation.danfoss.com.

Danfoss Learning is a free online learning platform. It features courses and materials speci�cally designed to help engineers, installers, service technicians, and wholesalers better understand the products, applications industry topics, and trends that will help you do your job better. Find your local Danfoss website here: learning.danfoss.com.

##### **Get local information and support**

Local Danfoss websites are the main sources for help and information about our company and products. Find product availability, get the latest reginal news, or connect with a nearby expert - all in your own language. Find your local Danfoss website here: danfoss.com.

###### **Danfoss A/S**

Climate Solutions . danfoss.com . +45 7488 2222

Any information, including, but not limited to information on selection of product, its application or use, product design, weight, dimensions, capacity or any other technical data in product manuals, catalogues description, advertisements, etc. and whether made available in writing, orally, electronically, online or via download, shall be considered informative, and is only binding if and to the extent, explicit reference is made in a quotation or order con�rmation. Danfoss cannot accept any responsibility for possible errors in catalogues, brochures, videos and other material. Danfoss reserves the right to alter its products without notice. This also applies to products ordered but not delivered provided that such alterations can be made without changes to form, �t or function of the products. All trademarks in this material are property of Danfoss A/S or Danfoss group companies. Danfoss and the Danfoss logo are trademarks of Danfoss A/S. All rights reserved.
