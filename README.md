# arduino-uno-r3-atmega328p-linux
Minimal boilerplate for developing software for the Arduino Uno R3 on Ubuntu 16.04 x86_64 using GCC and avrdude.

## Usage

Install the cross compiler, standard C library for Atmel AVR development and the flash tool.

`sudo apt-get install gcc-avr avr-libc avrdude`

To be able to access and use /dev/ttyACM0 for programming we have to add ourself to the dialout group.

`sudo usermod -a -G dialout <username>`

Compile.

`make`

Flash the AVR device.

`make flash`
