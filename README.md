# linux_raspberrypi_book
Linux Driver Development with Raspberry Pi - Practical Labs

Embedded systems have become an integral part of our daily life. They are deployed in mobile devices, networking infrastructure, home and consumer devices, digital signage, medical imaging, automotive infotainment and many other industrial applications. The use of embedded systems is growing exponentially. Many of these embedded systems are powered by an inexpensive yet powerful system-on-chip (SoC) that is running a Linux operating system. The BCM2837 from Broadcom is one of these SoCs, running quad ARM Cortex A53 cores at 1.2Ghz. This is the SoC used in the popular Raspberry Pi 3 boards. 

This book follows the learning by doing approach, so you will be playing with your Raspberry Pi since the first chapter. Besides the Raspberry Pi board, you will use several low-cost boards to develop the hands-on examples. In the labs, it is described what each step means in detail so that you can use your own hardware components adapting the content of the book to your needs.

You will learn how to develop Linux drivers for the Raspberry Pi boards. You will start with the simplest ones that do not interact with any external hardware, then you will develop Linux drivers that manage different kind of devices: Accelerometer, DAC, ADC, RGB LED, Buttons, Joystick controller, Multi-Display LED controller and I/O expanders controlled via I2C and SPI buses. You will also develop DMA drivers, USB device drivers, drivers that manage interrupts and drivers that write/read on the internal registers of the SoC to control its GPIOs. To ease the development of some of these drivers, you will use different types of Linux kernel subsystems: Miscellaneous, LED, UIO, USB, Input and Industrial I/O. More than 30 kernel modules have been written (besides several user applications), which can be downloaded from the book's GitHub repository. 

This book uses the Long Term Support (LTS) Linux kernel 5.4, which was released on November 2019 and will be maintained until December 2025. 

This book is a learning tool to start developing drivers without any previous knowledge about this field, so the intention during its writing has been to develop drivers without a high level of complexity that both serve to reinforce the main driver development concepts and can be a starting point to help you to develop your own drivers. And, remember that the best way to develop a driver is not to write it from scratch. You can reuse free code from similar Linux kernel mainline drivers. All the drivers written throughout this book are GPL licensed, so you can modify and redistribute them under the same license.

The Linux drivers and applications developed in the labs have been ported to three different Raspberry Pi boards: Raspberry Pi 3 Model B, Raspberry Pi 3 Model B+ and Raspberry Pi 4 Model B. The specifications of these boards can be found at:

https://www.raspberrypi.org/products/raspberry-pi-3-model-b/

https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/

https://www.raspberrypi.org/products/raspberry-pi-4-model-b/

In this book, the demonstration sections and Device Tree settings used during the development of the labs are referred to the Raspberry Pi 3 Model B board. You can download the Linux drivers, applications and Device Tree files for the three Raspberry Pi boards from the GitHub of the book. Besides the Raspberry Pi board, to get the most out of the book (by working through the labs), you will need the following hardware:

MikroElektronika Color click accessory board (used in LAB 5.2, LAB 7.3, LAB 10.3 and LAB 11.1): https://www.mikroe.com/color-click

PCF8574 IO Expansion Board (used in LAB 6.1): https://www.waveshare.com/pcf8574-io-expansion-board.htm

Analog Devices LTC3206 I2C Multidisplay board DC749A (used in LAB 6.2 and LAB 13.4): https://www.analog.com/en/products/ltc3206.html#product-evaluationkit

MikroElektronika Button R click board (used in LAB 7.1, LAB 7.2 and LAB 7.3): https://www.mikroe.com/button-r-click 

MikroElektronika EXPAND 6 click board (used in LAB 7.4, LAB 7.5 and LAB 7.6): https://www.mikroe.com/expand-6-click 

MikroElektronika Accel click board (used in LAB 10.1, LAB 10.4 and LAB 12.1): https://www.mikroe.com/accel-click 	

Olimex MOD-Wii-UEXT-NUNCHUCK (used in LAB 10.2, LAB 10.3 and LAB 11.2): https://www.olimex.com/Products/Modules/Sensors/MOD-WII/MOD-Wii-UEXT-NUNCHUCK/open-source-hardware 

MikroElektronika PIXI click board (used in LAB 11.1): https://www.mikroe.com/pixi-click 

Microchip Curiosity PIC32MX470 Development Board (used in LAB 13.1, LAB 13.2, LAB 13.3 and LAB 13.4): https://www.microchip.com/DevelopmentTools/ProductDetails/dm320103#additional-summary
