# arduino-uno-r3-atmega328p-linux
Minimal boilerplate for developing software for the Arduino Uno R3 on Ubuntu 16.04 x86_64 using the standard GCC toolchain (i.e., not Arduino IDE).

## Requirements
- Ubuntu 16.04 x86_64 or similar GNU/Linux distribution
- GNU Make
- gcc-avr - GNU C compiler (cross compiler for avr)
- avr-libc - Standard C library for Atmel AVR development
- avrdude - software for programming Atmel AVR microcontrollers

## Usage
Install the cross compiler, standard C library for Atmel AVR development and the flash tool.

`$ sudo apt-get install gcc-avr avr-libc avrdude`

To be able to access and use /dev/ttyACM0 for programming we have to add ourself to the dialout group.

`$ sudo usermod -a -G dialout <username>`

Compile.

`$ make`

Flash the AVR device.

`$ make flash`
