# core-v-mcu-devkit
The CORE-V MCU DevKit is an evaluation platform for the OpenHW RISC-V CV32E40P core IP (v1.0.0).  More information can be found at the [CV32E40P repo](https://github.com/openhwgroup/cv32e40p0).

## Organization

1. Project Parts - parts not built into kicad required for the devkit
2. kicad - kicad schematics and pcb files
3. images - image files to support this document

## About the devkit

This devkit has the following features:
1. CORE-V MCU (including CV32E40P (v1.0.0) RISC-V core and Quicklogic ArcticPro2 Embedded FPGA)
2. 4MB Flash memory to hold programs and EFPGA bit images
3. Onboard Ashling Opella LD JTAG debugger + Serial Consol interface
4. Offboard JTAG Connector
5. Every signal of the MCU brought out to test pins
6. I2C temperature sensor
7. CSI Camera interface with Himax camera
8. 2 LED's controllable by the MCU or by the EFPGA
9. 1 button for input to the MCU or to the FPGA
10. [mikroBUS](https://www.mikroe.com/mikrobus) socket for system expansion
11. Espressif AWS IoT ExpressLink interface for cloud learning

![devkit image](images/OpenHW%20DevKit%20-%20top.png)

<!-- [Schematic](file://OpenHW%20CORE-V%20MCU%20DevKit.pdf) -->

## Power
The devkit can be powered from 5 - 18V.  This can be easily accomplished via the 2.1mm DC barrel jack.  The USB-C connector will negotiate 5v from the USB source.

## Voltage levels
The CORE-V-MCU has a 1.8v I/O pad ring.  The 3.3v peripherals are interfaced to the 1.8v MCU with 7 level shifters.  The pins directly around the MCU are connected directly to the MCU pads and will be 1.8v logic.  The QSPI program flash memory is also at 1.8v logic.  The JTAG interface to the Ashling Opella LD is level shifted.  The enable signals on the JTAG level shifters is connected to jumper J4.  Inserting a jumper will disable the level shifters to the on-board JTAG interface allowing the JTAG header to be used.  


> Note: the JTAG header is directly connected to the CORE-V-MCU and will require 1.8v logic.

## mikroBUS
The microBUS header provides a UART, GPIO, I2C and SPI interface.  The UART interface is shared with the AWS IoT ExpressLink.  The CORE-V-MCU has an I/O multiplexer and an alternate pin mode allows the UART interface to be switched between two sets of I/O pins.
The microBUS is fully wired except for the 5v power option.  5v is not available to microBUS so ensure any CLICK's are configured for 3.3v.

