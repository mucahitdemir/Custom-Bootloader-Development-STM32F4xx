# Custom-Bootloader-Development-STM32F4xx
Hello! 
In this repository, custom bootloader development functions were tested.
You can use and contribute to the improvement of the functions.

**Next Phase of this repository**

I am going to work on Firmware Update Over-the-Air **(OTA)**

"It requires twice the brain power to debug a piece of code than to write it”

_Brian Kernighan, The Elements Of Programming Style_


**Bootloaders**

A boot loader is a critical piece of software running on any system. Whenever a computing system is initially powered on, the first piece of code to be loaded and run is the boot loader. It provides an interface for the user to load an operating system and applications.

A bootloaders is used as a separate program in the program memory that executes when a new application needs to be reloaded into the rest of program memory. 
The bootloader will use a serial port, USB port, or some other means to load the application. 
Frequently a bootloader will always execute on restart to check if a new program is to be loaded or if the application is to be run.

Since storage capacity important for any restrained-source microcontroller, looking at **Build Analyzer & Static Stack Analyzer** is 
critical to check for learning _code size and function size _sepately.

<img width="597" alt="image" src="https://user-images.githubusercontent.com/43001724/169756637-6648494f-6481-49cc-82ef-bcae57d05566.png">

### Embedded System/Software Security

Today, most of the developers think that security of an embedded system should be handled at the systems-engineering level or by the hardware that surrounds their software. And indeed many things can be done at those levels, including:

•    Secure network communication protocols.

•    Firewalls.

•    Data encryption.

•    Authentication of data sources.

•    Hardware-assisted control-flow monitoring.



It is also recommended to cover **Advanced Debug Features for STM32 CubeIDE** Video series

Link: https://www.youtube.com/watch?v=4wT9NhlcWP4&list=PL7tUZeMaichqrlJN4PGu3-n6DbYrvoG-s&index=1

Bootloader basics: https://embetronicx.com/tutorials/microcontrollers/stm32/bootloader/bootloader-basics/
