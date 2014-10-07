=============================================================================================================
Readme about Sanguino
=============================================================================================================
You can follow Sanguino on Facebook
http://www.facebook.com/Sanguino1284p

contributors
Siddharth Sharangpani
siddharth(dot)sharangpani(@)gmail.com


Sanguino is a bigger cousin of Arduino UNO, The Sanguino core was well maintained by Zach till Arduino 0017, 
The Arduino team did not include Sanguino in the main Arduino core, hence to make Sanguino work
with the Arduino IDE lot of modifications were needed. The last working Sanguino
with Arduino IDE was with Arduino 0022, and Sanguino best worked with Arduino 0017 version software.

To make Sanguino work was always a pain in the neck, We have a good customer based who were
using Sanguino in their applications, even in industrial products because of two things.

1. Arduino IDE support
2. Bigger memory and more number of pins.

We tried communicating with the team who were maintaining the Sanguino core, but it seemed at
that time the team was not interested in our patches. The sanguino core had been modified till
Arduino 0022 and after that the libraries which were supported by Arduino were not working with
Sanguino.

We did dump the original code and started fresh.

And this was the result.
A fully working and operational Sanguino with the latest Arduino 1.0.x support

===========================================================================================
Change Log, taking the best of all the sides.
===========================================================================================

1. We moved to Arduino core thereby removing any core new requirement
2. Sanguino upload protocol used STK500 we moved to arduino for ISP
3. Sanguino used 57600 bps, mighty-1284p uses 115200 bps for upload, we shifted to 115200 bps
4. Sanguino uses old bootloader, we shifted to the optiboot bootloader also used in Arduino UNO

===========================================================================================

Testing with Atmega1284P/Atmega32A controllers

1. ASCII Table : OK : Serial Port test print
2. Digital output : OK , LED blink
3. Digital input : button press, LED blink
4. Analog input : LM35 : test okay, temperature on serial monitor : tested
5. Analog output : PWM LED  : Tested Okay, Pin 15
6: SPI : SD card tested : OK using SDFAT Library QuickStart, SDInfo programs
7: I2C : DS1307 Date Read, after every 5 seconds.
8: Interrupt : 2Hz led flashing interrupt programming using Timer1
9. EEPROM : tested
10. SPI Ethernet working

Atmega16A Testing

1. ASCII Table : OK : Serial Port test print, OKAY
2. Digital output : OK , LED blink, OKAY
3. Digital input : button press, LED blink, tested, OKAY
4. Analog input : LM35 : test okay, temperature on serial monitor : tested
5. Analog output : PWM LED  : Tested Okay, Pin 15, OKAY
6: SPI : Sketch too big to fit SDFAT Library
7: I2C : DS1307 Date Read, after every 5 seconds, after 10 minutes without setting time, read time, 
		time had elapsed, means RTC was powered from CR2032 and maintaining time., OKAY
8: Interrupt : 2Hz led flashing interrupt programming using Timer1 , OKAY
9. EEPROM : tested, OKAY


=============================================================================================


