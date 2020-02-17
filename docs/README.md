# ModbusBox Hardware For Makers
ModbusBox device hardware design.

### Introduction.

**ModbusBox**    allows the integration of Modbus RTU networks to a WiFi connection. It is capable to  read data registers  from Modbus slaves (tested with 4 )  then send data periodically  to cloud services using the very popular MQTT protocol. Data is serialized  using  Json format , the information can be processed and displayed in dashboards  by many open source IOT platforms like Node-red, Influxdb & Grafana,  Ubidots educational and  its pay platform which is very powerfully and easy to use. 

**ModbusBox**  has been tested and optimized to be connected to  Variable frequency drives that uses  modbus RTU as base protocol , but it can be used with any other device that uses modbus rtu over RS485. protocol .

------

### Hardware features.

**Processor :** ESP32-WROOM-32 

**DC Input :** 7~ 26v ( step down dc buck regulator).

**Current consumption:** <100ma when DC input =20 ~27v

**Hardware interfaces.**

- 1x RS485 port (RJ45), non insolated.
- 1x programing connection (tx0/rx0).
- 1x SPI port.
- 1xI2c port.
- 3x micro buttons for ESP programing mode and device setup.

**Led indication.**

- 1x power led.
- 1 x MQTT activity ( msg send/received).
- 1x  Neopixel  RGB  led for device status indication.
- 1x Modbus TX led.
- 1x Modbus RX led.

**Additional Features**.

- Dc input voltage measurement (voltage divider connected to GPIO35).
- DC input capacitor act as short voltage backup , when  combined with the voltage divider measurement   can be used in the ESP32 program to send  and alarm ( for example an MQTT message )  before the voltage stored in the capacitor reach 3.3 volts.

**WiFi Specs**.

IEEE 802.11 b/g/n

Freq Band: 2.4 ~ 2.462 GHZ.

Integrated Antenna.

------

### PCB  DESING 

![Electronic Schematic](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/mboxschematic.jpg)

[PDF SCHEMATIC](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/docs/modbusbox.pdf)

**Unassembled top layer  PCB photo**.

![TOP](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/tpcb1.jpg)

**Unassembled bottom  layer  PCB photo**

![Bottom](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/bpcb1.jpg)

**PCB Photos** 

![ASSEMBLED PCB](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/mbx2.jpg)

![](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/mbx3.jpg)

### Modbus  Box Assembled  

![](https://github.com/iotbits-us/mbox-hardware-mk/blob/master/images/Mbox%20Connector.jpg)

------

###  Modbus Box & ControlTechniques AC drives.

The Modbus Box had been tested successfully  with several AC drives  models of the recognized brad Nidec Control techniques , some of the  drive models tested are : M200/300/400 and C200.  Modbus Box can be connected directly to the drive AI-485 adaptor which also have 24 volts , there is no requirement for additional power supply . An ethernet cable Cat5e  can be used to  make the connection  between the Modbus box and the drive RS485 port.

![](https://github.com/iotbits-us/mbox-hardware-mk/blob/master/images/Mbox-CT%20drives.jpg)

------

### Connecting Modbus Box to other Modbus slaves.

In order to connect Modbus box to other Modbus slaves we recommend the following  connecting accessories  that can be found on eBay or Aliexpress.

- RJ45 Female To Screw Terminal 8 Pin Connector :  [ebay link](https://www.ebay.com/itm/RJ45-Female-To-Screw-Terminal-8-Pin-Connector-Ethernet-Cable-Extender-Adapter/254014714403?hash=item3b2474f223:g:BGoAAOSwa6NcCMWQ), [aliexpress link](https://www.aliexpress.com/item/32999037495.html?spm=a2g0o.productlist.0.0.21a565d7lVaozt&algo_pvid=d795203f-b1a4-4b95-bd85-08aafb6c9047&algo_expid=d795203f-b1a4-4b95-bd85-08aafb6c9047-3&btsid=baff936b-99e3-4e44-be2d-e5796b4b197a&ws_ab_test=searchweb0_0%2Csearchweb201602_3%2Csearchweb201603_52).
- Ethernet cable Cat6e 0.5m ...50m : [aliexpress link](https://www.aliexpress.com/item/32694241950.html?spm=a2g0o.productlist.0.0.9092403dVuzqNC&algo_pvid=769067d0-d6fb-4676-b6cb-d6e4e51600fe&algo_expid=769067d0-d6fb-4676-b6cb-d6e4e51600fe-0&btsid=7b7bc02a-cc6a-4bed-9a7c-db1720ab03a8&ws_ab_test=searchweb0_0%2Csearchweb201602_3%2Csearchweb201603_52).
- DC 24 or 12 volts 1 amp  power supply : [aliexpress link ](https://www.aliexpress.com/item/33014882564.html?spm=a2g0o.productlist.0.0.2c112a5dqVQcpi&algo_pvid=156211e4-a33d-4b1b-8fa4-83e324b6f369&algo_expid=156211e4-a33d-4b1b-8fa4-83e324b6f369-2&btsid=9af3999f-a54b-44a6-b236-d98386595c6f&ws_ab_test=searchweb0_0%2Csearchweb201602_3%2Csearchweb201603_52)

![RJ45 Female To Screw Terminal ](https://github.com/iotbits-us/mbox-hardware-mk/blob/master/images/Modbus%20Adaptor.jpg)

### Connecting Modbus Box to SDM230-Modbus.

![SDM230-Modbus](https://github.com/iotbits-us/mbox-hardware-mk/blob/master/images/SDM230-Modbus.jpg)

[Library to test the ModbusBox ](https://github.com/luisgcu/SensorModbusMaster)



































 

