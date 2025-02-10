Overview
========
A demo application runs different functions for benchmark test.

SDK version
===========
- Version: 2.16.100

Toolchain supported
===================
- IAR embedded Workbench  9.60.1
- Keil MDK  5.39.0
- GCC ARM Embedded  13.2.1
- MCUXpresso  11.10.0

Hardware requirements
=====================
- Type-C USB cable
- FRDM-MCXN947 board
- TFT Proto 5" CAPACITIVE board by Mikroelektronika (www.mikroe.com) HW REV 1.01
- 3.5" TFT LCD module by NXP (P/N PAR-LCD-S035) Rev.A (optional with Mikroeletronika LCD)
- Personal Computer

Board settings
==============
Attach the LCD shield to the FRDM board.

Prepare the Demo
================
1.  Power the board using a type-c USB cable connected to J2 USB port on the board, attach debugger to J5 connector
2.  Add compiler macro `BOARD_LCD_S035=1` to toolchain project if NXP 3.5" LCD is being used
3.  Build the project.
4.  Download the program to the target board.
5.  Reset the SoC and run the project.

Running the demo
================
If this example runs correctly, the sample GUI is displayed.
