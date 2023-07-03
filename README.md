# Embedded_Arm_Cyberdeck

This is a project with the aim of producing a cyberdeck device that is capable of running embedded linux/android with a physical keyboard, with various hardware interfaces like I2C, CAN, SPI and GPIO

# Goals
I am writing this before I start the project to set goals for performance, and to avoid project scope creep (A problem I struggle with).  
The device should comfortably be able to run linux terminal and limited GUI.  It should have the following capabilities:
- access to wifi to be able to ssh into a more powerful computer remotely if it needs additional computing power.
- at least an hour of battery life
- a pretty enclosure 
- a fully capable blackberry keyboard
- IO avaliable to interface with UART/I2C/SPI/CAN devices
- High resolution screen for usable terminal
- A budget of no more than $75 AUD
- Integrated RP2040 to handle keyboard and touch screen and report to cpu as a HID device -- this modular setup allows for easy testing of subcircuits

# Potential MPUs
 - TI Sitara AM625 1.4GHz quad-core Arm Cortex-A53, PRU and M4 microcontroller $30
    - Can base design off beaglebone
    - open source
    - existing linux support
 - STM32MP135DAE7 Arm Cortex-A7 1GHz $16
 - STM32MP157C 800MHz dual core ARM Cortex A7 $30
    - Very cool little chip
    - huge software support
    - TFT/MIPI display driver
    - 2x CAN channels
 - Texas instruments AM6232ATCGGAALW 	1.4 GHz 4 core ARM Cortex A53 $36
 - NXP i.MX6 SLL 1GHz single core ARM Cortex A9 $34
 - Rockchip RK3568 Quad core ARM Coretec A55 1.8GHz $35  
 - Rockchip RK3399 Dual-core Cortex-A72 1.8GHz Quad-core Cortex-A53 1.4GHz $53
    - Open source !
    - cheaper of the high performance MPUs
    - USB C
 - NXP i.MX 6Solo/6DualLite dual core ARM Cortex A9 $60
 - Allwinner A33 ARM Cortex a7 $6.5
    - AXP223 power management ic
    - availiable ECAD Model
    - very cheap

# Display
The choice of display will depend greatly on integrated hardware onboard the MPU, as some chips may not support certain displays.

# Peripherals
I can use a TCA8418E IC to allow for HID keyboard control over I2C with exisiting linux kernal support.
Wifi can be done with a WL1807MOD transceiver or a NINA-W10x IC which both offer Wifi and BT with linux kernal support

# Inspiration
This project would not be possible without this documentation detailing the Blackberry Q10 keyboard:
https://github.com/arturo182/BBQ10KBD
This project served as inspiration for the functionality of the device, as a portable small linux environment.
https://www.crowdsupply.com/f-secure/usb-armory-mk-ii
