# LVGL ported to NXP FRDM-MCXN947

## Overview

This port is intended to use with the NXP FRDM-MCXN947 board. The idea of this project is to provide a quick start to users that have this board to deploy they first
LVGL application to it, by default this project execute the `lvgl_demo_benchmark` where a collection of
widgets get drawn on the display showing the perfomance of the LVGL across different scenarios.

This project is itended to be used with MCU Expresso IDE.

## Buy

The board combo can be acquired from the NXP Direct channel:

* https://www.nxp.com/part/FRDM-MCXN947
* https://www.nxp.com/part/LCD-PAR-S035


## Benchmark

It uses the software based rendering in a single thread mode, in the current optimization
level, it is possible to execute the widgets demo with a value between 30 and 45FPS, while complex container
rendering from the benchmark demo slowdowns to around 10FPS. This is achieved using 16-bit color depth and
extra optimization is done by making the DMA to handle the SPI transfer between the MCU and the LCD.

## Specification

### CPU and Memory
- **MCU:** NXP MCXN947 single ARM Core Cortex-M33
- **RAM:** 512KB of internal scattered RAM
- **Flash:** 2MB of internal Flash

### Display and Touch
- **Resolution:** 480 x 320
- **Display Size:** 3.5"
- **Interface:** SPI
- **Color Depth:** 16-bit RGB565 format
- **Technology:** IPS
- **Touch Pad:** Capacitive touch panel

### Connectivity
- 1x Ethernet
- 2x CAN Bus
- Serial peripherals: UART/SPI/I2C
- SD Card based on SDHC
- Arduino R1 connector standard

## Getting started

### Hardware setup
- First of all disconnect all power cables from the board
- Connect the display panel to the board using the header connector J8
- Connect USB cable to the J1 USB-C it provides both Debug port plus console

### Software setup
- You need to install the MCU-Expresso IDE from NXP website:
    * It is avaibalble to Linux, Windows or Mac
    * Refer the link: https://www.nxp.com/design/design-center/software/development-software/mcuxpresso-software-and-tools-/mcuxpresso-integrated-development-environment-ide:MCUXpresso-IDE


### Run the project
- Clone this repository repository
- Open the NXP MCU Expresso IDE:
    * Go to the toolbars and enter in the File menu
    * Then **Import->Existing Projects in the workspace**
    * Navigate to the path where you cloned this repo
    * Then hit OK
- Build the project:
    * On the project explorer do a right click on the imported project
    * Click on **Build Project**
- Run or Debug:
    * First build the project as instructed above
    * On the project explorer do a right click on the imported project
    * Click on the **Debug As...**
    * Select you debug probe configuration it can be:
        * MCU Expresso Link server
        * Jlink Probe
    * Select the discovered probe and then hit Debug
    * The firmware will be downloaded and the debug will be halted on the **main()**
    * just hit **F8** to resume the debuggin
### Debugging
- You can also complement the debug experience with the printf / Console:
    * With the board connected to the host computer find its **COM** number or **/dev/<serial>** node
    * Open your favorite terminal program;
    * Connnect to the serial port found with the following settings:
        * 8 bits
        * 115200 bps
        * No parity
        * No flow control
    * You should now see the logs reported by the demo application while it runs

## Known limitations:
There are no known limitations observed on this board yet.

## Contribution and Support

If you find any issues with the development board feel free to open an Issue in this repository. For LVGL related issues (features, bugs, etc) please use the main [lvgl repository](https://github.com/lvgl/lvgl).

If you found a bug and found a solution too please send a Pull request. If you are new to Pull requests refer to [Our Guide](https://docs.lvgl.io/master/CONTRIBUTING.html#pull-request) to learn the basics.

