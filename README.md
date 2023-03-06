# Embedded_Arm_Blackberry

This is a project with the aim of producing a lookalike blackberry device that is capable of running embedded linux/android with a physical keyboard.

# Goals
I am writing this before I start the project to set goals for performance, and to avoid project scope creep (A problem I struggle with).  
The device should comfortably be able to run linux terminal and limited GUI.  It should have the following capabilities:
- access to wifi to be able to ssh into a more powerful computer remotely if it needs additional computing power.
- at least an hour of battery life
- a pretty enclosure 
- a fully capable blackberry keyboard
- IO avaliable to interface with UART/I2C/SPI devices
- High resolution screen for usable terminal
- Integrated RP2040 to handle keyboard and touch screen and report to cpu as a HID device -- this modular setup allows for easy testing of subcircuits

# Inspiration
This project would not be possible without this documentation detailing the Blackberry Q10 keyboard:
https://github.com/arturo182/BBQ10KBD
This project served as inspiration for the functionality of the device, as a portable small linux environment.
https://www.crowdsupply.com/f-secure/usb-armory-mk-ii
