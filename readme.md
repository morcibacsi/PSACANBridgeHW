# PSA CAN protocol bridge (hardware)

### What is it ?
This is the hardware needed for my [PSA CAN protocol bridge][psacanbridge] software.

### v1.1

It was designed as a shield for the ESP32 dev board. It uses the MCP2515 to connect to the CAN bus of the car and the internal CAN peripheral of the ESP32 for connecting to the retrofitted peripherals. The CAN transceiver used on this board is the MCP2551.
The board was designed in a way that the LM7805 can be easily replaced by a step down converter shield.

I have included a buzzer and some spare connection points for future use, but they weren't ever tested if they work. This is the reason why the BOM below doesn't contain the components related to the buzzer.

💡 **Make sure you don't populate R3 and R4 resistors!**

If you want to build the board for yourself take the photo as a reference as that contains all you need to make it work.

### PCB

![kicad_front.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.1/images/kicad_front.jpg)

![kicad_back.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.1/images/kicad_back.jpg)

![photo.jpg](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.1/images/photo.jpg)

![assembled.gif](https://github.com/morcibacsi/PSACANBridgeHW/raw/v1.1/images/assembled.gif)

### BOM

|Designator|Val         |Package                                         |
|----------|------------|------------------------------------------------|
|C1        |22pF        |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|C2        |22pF        |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|C3        |33uF        |CP_EIA-3528-21_Kemet-B_Pad1.50x2.35mm_HandSolder|
|C4        |100nF       |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|C5        |100nF       |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|C6        |100nF       |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|C7        |100nF       |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|C8        |47uF        |CP_EIA-3528-21_Kemet-B_Pad1.50x2.35mm_HandSolder|
|C9        |100nF       |C_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|D1        |D_ALT       |D_SMA                                           |
|Q2        |BSS138      |SOT-23                                          |
|Q3        |BSS138      |SOT-23                                          |
|Q4        |BSS138      |SOT-23                                          |
|Q5        |BSS138      |SOT-23                                          |
|R1        |2.2K        |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R2        |2.2K        |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R3        |120         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R4        |120         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R5        |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R6        |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R7        |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R8        |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R11       |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R12       |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R13       |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R14       |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R15       |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|R16       |10K         |R_0603_1608Metric_Pad1.05x0.95mm_HandSolder     |
|U1        |MCP2515-xSO |SOIC-18W_7.5x11.6mm_P1.27mm                     |
|U2        |TJA1042T    |SOIC-8_3.9x4.9mm_P1.27mm                        |
|U3        |TJA1042T    |SOIC-8_3.9x4.9mm_P1.27mm                        |
|U6        |LM7805_TO220|TO-252-2                                        |

[psacanbridge]: https://github.com/morcibacsi/PSACANBridge