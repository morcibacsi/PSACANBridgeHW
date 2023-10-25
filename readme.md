# PSA CAN protocol bridge (hardware)

### What is it ?
This is the hardware needed for my [PSA CAN protocol bridge][psacanbridge] software.

### v1.3

It was designed as a shield for the ESP32 dev board. It uses the MCP2515 to connect to the CAN bus of the car and the internal CAN peripheral of the ESP32 for connecting to the retrofitted peripherals. The CAN transceiver used on this board is the MCP2551.

### PCB

![kicad_front.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.3/images/kicad_front.jpg)

![kicad_back.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.3/images/kicad_back.jpg)

![photo_front.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.3/images/photo_front.jpg)

![photo_back.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.3/images/photo_back.jpg)


### Assembly

The board was designed to be as compact as possible, so I suggest to send the manufacturing files to JLCPCB and order with assembly service. But in order to have a working board some soldering is also needed. You can find the necessary components in the next section.

I bought a [DS3231 real time clock module for Raspberry Pi][DS3231] and disassembled that and placed its parts to J3 and U7. But it can be put directly into the connector found below U7.

<img src="https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.3/images/ds3231.jpg" width="200" height="200">

You can use the LM7805 voltage regulator alone, but it can get quite hot. So I suggest to populate the [MP1584 DC-DC Step Down Power Supply Module][MP1584EN] on the back marked with U3. Set the output voltage to between 7.5-9 volts.

<img src="https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.3/images/mp1584.jpg" width="200" height="200">

💡 **Make sure you solder the jumper marked with red above the LM7805 (+ and VIN)!**

💡 **Make sure you don't populate R3 and R4 resistors!**


### BOM

|Designator|Value         |Package                                         |
|----------|------------|------------------------------------------------|
|U3        |MP1584 DC-DC converter       |     |
|J3        |Coin battery for DS3231      |     |
|U7        |DS3231      |SOIC-16W_7.5x10.3mm_P1.27mm     |
|C3        |330nF       |CP_Radial_D4.0mm_P2.00mm     |
|C8        |100nF       |CP_Radial_D4.0mm_P2.00mm     |
|U6        |LM7805|TO-252-2                                        |

The connector on the right for the power and signal wires is a JST-XH6 2.54 mm


The full BOM is in the production folder as a csv.

[psacanbridge]: https://github.com/morcibacsi/PSACANBridge
[MP1584EN]: https://www.aliexpress.com/item/1005004531735516.html
[DS3231]: https://www.aliexpress.com/item/1005006116699524.html