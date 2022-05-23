# Custom-Bootloader-Development-STM32F4xx
Hello! 
In this repository, custom bootloader development functions were tested.
You can use and contribute to the improvement of the functions.

**Next Phase of this repository**
I am going to work on Firmware Update Over-the-Air **(OTA)**
Best

**Bootloaders**

A boot loader is a critical piece of software running on any system. Whenever a computing system is initially powered on, the first piece of code to be loaded and run is the boot loader. It provides an interface for the user to load an operating system and applications.

A bootloaders is used as a separate program in the program memory that executes when a new application needs to be reloaded into the rest of program memory. 
The bootloader will use a serial port, USB port, or some other means to load the application. 
Frequently a bootloader will always execute on restart to check if a new program is to be loaded or if the application is to be run.

Since storage capacity important for any restrained-source microcontroller, looking at **Build Analyzer & Static Stack Analyzer** is 
critical to check for learning _code size and function size _sepately.

<img width="597" alt="image" src="https://user-images.githubusercontent.com/43001724/169756637-6648494f-6481-49cc-82ef-bcae57d05566.png">
