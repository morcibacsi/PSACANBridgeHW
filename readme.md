# PSA CAN protocol bridge (hardware)

### What is it ?
This is the hardware needed for my [PSA CAN protocol bridge][psacanbridge] software.

### v1.4

It was designed using KiCad 7.0.6 as a standalone board with an ESP32-C3 SuperMini soldered in place. It uses the MCP2515 to connect to the CAN bus of the car and the internal CAN peripheral of the ESP32 for connecting to the retrofitted peripherals. The CAN transceiver used on this board is the TJA1050 (the schematics contains a TJA1042 but they are interchangeable).

### Schema

![schema.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/schema.jpg)

### PCB

![kicad_front.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/kicad_front.jpg)

![photo_front.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/photo_front.jpg)

![photo_enclosure.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/photo_enclosure.jpg)

### Assembly

The board was designed to be as compact as possible, so I suggest to send the manufacturing files to JLCPCB and order with assembly service. But in order to have a working board some soldering is also needed. You can find the necessary components in the next section.

💡 **By soldering JP1 and JP2 solder jumpers you can enable the CAN termination resistors (not needed in PSA cars)**

ESP32-C3 SuperMini

<img src="https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/SuperMini-ESP32-C3.jpg" width="200" height="200">

I bought a [DS3231 real time clock module for Raspberry Pi][DS3231] and disassembled that and placed its parts to J1 and U2.

<img src="https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/ds3231.jpg" width="200" height="200">

The board dimensions were designed to fit a [70 x 45 x 18mm case][enclosure].

<img src="https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.4/images/enclosure.jpg" width="200" height="150">

### BOM

I listed only those which aren't populated by the assembly company.

|Designator|Value         |Package                                         |
|----------|------------|------------------------------------------------|
|J1        |Coin battery for DS3231      |     |
|U2        |DS3231      |SOIC-16W_7.5x10.3mm_P1.27mm     |
|C7        |100uF       |Capacitor_THT:CP_Radial_D6.3mm_P2.50mm     |
|C8        |220uF       |Capacitor_THT:CP_Radial_D6.3mm_P2.50mm     |

The connector for the power and signal wires is a JST-XH6 2.54 mm


The full BOM is in the production folder as a csv.

[psacanbridge]: https://github.com/morcibacsi/PSACANBridge
[DS3231]: https://www.aliexpress.com/item/1005006116699524.html
[enclosure]: https://www.aliexpress.com/item/1005005467281776.html