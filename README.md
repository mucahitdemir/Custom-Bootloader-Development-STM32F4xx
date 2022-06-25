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

Today, most of the developers think that security of an embedded system should be handled at the hardware that surrounds their software. And indeed many things can be done at those levels, including:

•    Secure network communication protocols.

•    Firewalls.

•    Data encryption.

•    Authentication of data sources.

•    Hardware-assisted control-flow monitoring.
Don't forget that our attackers have a big advantage when it comes to embedded systems: Most embedded software has severe execution time constraints, often a mixture of hard real-time and soft real-time tasks. This coaxes us to design application software that is “lean and mean,” by reducing to a minimum intensive run-time limit checking and reasonableness checking (for example, invariant assertions) in order to meet timing requirements. Our attackers have no such execution time constraints: They are perfectly happy to spend perhaps weeks or months researching, preparing, and running their attacks–possibly trying the same attack millions of times in the hope that one of those times it might succeed, or possibly trying a different attack each day until one hits an open “attack window.”

**How can attackers attack via our own software?**
Quite often embedded software developers dismiss the issue of embedded software security, saying: “Hey, our device will never connect to the Internet or to any other external communication link. So we're immune to attack.” Unfortunately, this is naïve and untrue. I'd like to present a counterexample:

Many embedded devices use analog-to-digital-converters (ADCs) for data acquisition. These ADCs may be sampled on a regular timed basis, and the data samples stored by application software in an array. Application software later processes the array of data. But an attacker could view this in a totally different way: “What if I fed the ADC with electrical signals that, when sampled, would be exactly the hexadecimal representation of executable code of a nasty program I could write?” In that way, the attacker could inject some of his software into your computer. No network or Internet needed.

Can you think of an easier way for an attacker to develop an attack on your current project?
What's a software developer to do?
During embedded systems software design, you can enhance software security by keeping several fundamental ideas in mind:2

**Mindframe #1: Distrustful decomposition**
Separate the functionality of your software into mutually untrusting chunks , so as to shrink the attack windows into each chunk. (In embedded software, we sometimes call these chunks processes or subsystems or CSCIs.)

Design each chunk under the assumption that other software chunks with which it interacts have been attacked, and it is attacker software rather than normal application software that is running in those interacting chunks. Do not trust the results of interacting chunks. Do not expose your data to other chunks via shared memory. Use orderly inter-process communication mechanisms instead, like operating system message queues, sockets, or TIPC (Transparent Inter-process Communication). Check the content you receive. As a result of mutually untrusting chunking, your entire system will not be given into the hands of an attacker if any one of its chunks has been compromised.




It is also recommended to cover **Advanced Debug Features for STM32 CubeIDE** Video series

Link: https://www.youtube.com/watch?v=4wT9NhlcWP4&list=PL7tUZeMaichqrlJN4PGu3-n6DbYrvoG-s&index=1

Bootloader basics: https://embetronicx.com/tutorials/microcontrollers/stm32/bootloader/bootloader-basics/
