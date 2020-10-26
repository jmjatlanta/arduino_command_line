The Arduino Bootloader is a .hex file that is burned onto the Atmel ATMega 328. The bootloader looks for a new program coming in. If none is found, it begins looping through the program it has.

According to https://learn.sparkfun.com/tutorials/installing-an-arduino-bootloader

an AVR Programmer can push the bootloader to the arduino. I've seen elsewhere that you can do it with an FTDI but it is very slow.