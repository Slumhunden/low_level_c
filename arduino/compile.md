# Compiling

## Windows

## Mac
In the following you will find the commands to compile the code on Mac for the Arduino Uno/nano.

### avrdude
- avrdude is a program that is used to upload the code to the Arduino.
- the commands to run avrdude are:
- Find the port: ```ls /dev/tty.*``` in the terminal
- Run the command: ```avrdude -c arduino -p m328p -P /dev/tty.usbserial-110 -b 115200 -D -U flash:w:itsbinfun.hex:i```


avr-gcc -Os -mmcu=atmega328p -DF_CPU=16000000UL itsbinfun.c -o itsbinfun.elf

avr-objcopy -O ihex itsbinfun.elf itsbinfun.hex

avrdude -c arduino -p m328p -P /dev/tty.usbserial-BG000IJ7 -b 57600 -D -U flash:w:itsbinfun.hex:i

## A good idea would be to make a Makefile for this.

## That has been done!

### Using the Makefile
- Check the makefile in the folder for the correct variables.
    - Variables to check out are:
        - MCU
        - F_CPU
        - PROGRAMMER
        - BAUD
        - PORT
*If making the Makefile with copilot, delete any indentations and make them with **TAB** instead.*