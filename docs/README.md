# mbox-hardware-mk
ModbusBox device hardware design.

### Introduction.

**ModbusBox**    allows the integration of Modbus RTU networks to a WiFi connection. It is capable to  read data registers  from modbus slaves  then send data periodically  to cloud services using the very popular MQTT protocol. Data is serialized  using  Json format , the information can be processed and displayed in dashboards  by many open source IOT platforms like Node-red, Influxdb & Grafana,  Ubidots educational and  its pay platform which is very powerfully and easy to use. 

**ModbusBox**  has been tested and optimized to be connected to  Variable frequency drives that uses  modbus RTU as base protocol .

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

**WiFi Specs**.

IEEE 802.11 b/g/n

Freq Band: 2.4 ~ 2.462 GHZ.

Integrated Antenna.

**Unassembled top layer  PCB photo**.

![TOP](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/tpcb1.jpg)



**Unassembled bottom  layer  PCB photo.**



![Bottom](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/bpcb1.jpg)



### Electronic Schematic.

![](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/mboxschematic.jpg)

[PDF SCHEMATIC](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/docs/modbusbox.pdf)

## PCB PHOTOS 

![ASSEMBLED PCB](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/mbx2.jpg)

![](https://github.com/iotbits-llc/mbox-hardware-mk/blob/master/images/mbx3.jpg)

### Modbus  Box Assembled  

![](https://github.com/iotbits-us/mbox-hardware-mk/blob/master/images/Mbox%20Connector.jpg)

###  Modbus Box & ControlTechniques AC drives.

The Modbus Box had been tested successfully  with several AC drives  models of the recognized brad Nidec Control techniques , some of the  drive models tested are : M200/300/400 and C200.  Modbus Box can be connected directly to the drive AI-485 adaptor which also have 24 volts , there is no requirement for additional power supply . An ethernet cable Cat5e  can be used to  make the connection  between the Modbus box and the drive RS485 port.

![](https://github.com/iotbits-us/mbox-hardware-mk/blob/master/images/Mbox-CT%20drives.jpg)





To be continued.. 



























 

