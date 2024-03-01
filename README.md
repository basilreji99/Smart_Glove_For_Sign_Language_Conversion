
**Smart Glove for Sign Language Conversion**

School of Engineering, CUSAT 

**Mini Project**

**SMART GLOVE FOR SIGN LANGUAGE CONVERTION**

SUBMITTED BY:
**BASIL REJI,
ANJALI RATHESH, 
APARNA S,
ANANTHU KRISHNA S,
ADERSH**

IN PARTIAL FULFILLMENT OF REQUIREMENT FOR THE AWARD OF DEGREE OF BACHELOR OF TECHNOLOGY IN **ELECTRICAL AND ELECTRONICS ENGINEERING**, DIVISION OF ELECTRICAL ENGINEERING, SCHOOL OF ENGINEERING, COCHIN UNIVERSITY OF SCIENCE AND TECHNOLOGY, COCHIN-682022


**CERTIFICATE**

Certified that the report entitled
**SMART GLOVE FOR SIGN LANGUAGE CONVERSION**
is a bonafide record of work done by
BASIL REJI (19180019)
ANJALI RATHESH (19180010)
APARNA S (19180012)
ANANTHU KRISHNA S (19180009)
ADERSH (19170003)
towards the partial fulfilment for the award of the degree of B. Tech in Electrical & Electronics Engineering of Cochin University of Science and Technology, Kochi-682022.
Dr. Asha E Daniel Ms. Jeena John Ms. Ragi R Menon
Head of Department Assistant Professor Assistant Professor
Division of Electrical Division of Electrical Division of Electrical
Engineering, SOE Engineering, SOE, Engineering, SOE,
CUSAT CUSAT CUSAT
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT Mini Project
ABSTRACT
This report is on the implementation of “SMART GLOVE FOR SIGN LANGUAGE CONVERSION”. Roughly 27.8% of the total population of India can’t either hear or speak. Sign language is a non-verbal form of communication method which is found among all deaf and dumb communities. Normal people do not learn sign language, it causes barriers in communication between deaf and dumb people. Hence to break this barrier we design a system which converts hand gestures into auditory speech as well as text. The system is being proposed with use of flex sensors and android technology. There are 2 modules, first is a glove with flex sensors and Atmel ATMEGA328 PU microcontroller and second is an android app with Google speech API.
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT Mini Project
CONTENTS
1. Introduction……………………………………………………………………....1
2. Block Diagram & Description …………………………………………………. 3
2.1) Block Diagram ………………….………………………………...…....4
2.2) Block Diagram Description…………………………………………… 5
2.2.1) Power Supply……………………………………………………... 5
2.2.2) Flex Sensor ………………………………………………………. 5
2.2.3) Microcontroller …………………………………………………… 5
2.2.4) LCD Display ……………………………………………………… 5
2.2.5) Bluetooth Module ……………………………………………….... 5
2.2.6) Android Application ………………………….…………………....6
3. Components & Specifications …………………………………………………...7
3.1) ATMEGA 328PU…………………………………………………….......8
3.2) Flex Sensors ………………………………………………………….......9
3.2.1) Pin Description………………………………………………………9
3.2.2) Features & Specifications …………………………………………10
3.2.3) Working …………………………………………………………...10
3.3) LCD 16x2 Display……………………………………………………….10
3.3.1) Features ……………………………………………………………11
3.4) HC-05 Bluetooth Module……………………………………………......11
3.4.1) Features ……………………………………………………….......11
3.5) LM 7805 Voltage Regulator …………………………………………....12
3.6) ADXL 335 Accelerometer ……………………………………………...12
4. Circuit Diagram & Explanation …………………………………………………….13
5. Software Section …………………………………………………………………....15
5.1) Arduino IDE …………………………………………………………....16
5.2) Proteus ………………………………………………………………….16
5.3) Android Application …………………………………………………....17
6. Flowchart …………………………………………………………………………. 18
7. Working …………………………………………………………………………....20
8. Conclusion & Future Scope ………………………………………………………. 23
9. References ………………………………………………………………………….25
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT Mini Project
10. Datasheets …………………………………………………………………………. 27
10.1) ATMEGA 328PU……………………………………………………... 28
10.2) Flex Sensors …………………………………………………………... 31
10.3) HC-05 Bluetooth Module……………………………………………... 32
10.4) LCD 16x2 Display……………………………………………………. 34
11. Figures & Tables …………………………………………………………………. 38
11.1) List of figures …………………………………………………………. 39
11.2) List of Tables …………………………………………………………. 39
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 1 Mini Project
1.INTRODUCTION
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 2 Mini Project
INTRODUCTION
About eighteen million people in the planet are dumb or deaf. The communication between a dumb and hearing person becomes difficult because sign languages are unknown to normal people. Also, even the communication among deaf people are a bit hard due the disparities of sign languages from nation to nation. This creates an extremely little house for them, with communication being an associate degree for elementary aspect of human life. The languages haven't got a typical origin and hence are hard to interpret. A dumb communication interpreter is also a tool that interprets the hand gestures to sensible speech.
The primary aim of this paper is to introduce an issue that will efficiently translate hand gestures into its equivalent textual and voice representation. The interpreter makes use of a glove totally based on the technique comprising of flex sensors. For each hand gesture created by the right hand, 5 sets of voltage combinations are formed by the sensors for further processing in the microcontroller. Then the controller matches the gesture with pre-stored inputs. The output is brought with the help of an android smartphone using an android app.
FIGURE 1
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 3 Mini Project
2. BLOCK DIAGRAM & DESCRIPTION
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 4 Mini Project
2.1) BLOCK DIAGRAM
FIGURE 2
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 5 Mini Project
2.2) BLOCK DIAGRAM DESCRIPTION
2.2.1) POWER SUPPLY
The power supply is designed to convert high DC voltage to low DC voltage for the electronic devices used in the circuit. The main power source of the circuit is 12V battery. But the most of the devices used in the circuit work on 5V DC supply. So we use 7805 Voltage regulator to covert 12V DC supply to 5V DC supply which in turn powers the Flex sensors and Microcontroller. The Bluetooth module and LCD Display are powered by microcontroller
2.2.2) FLEX SENSORS
Flex sensors are resistive carbon parts. When bent, the device develops a resistance output correlative to the bend radius. The variation in resistance is just about 10kΩ to 30kΩ. A global organization flexed device has 10kΩ resistance and once bent the resistance will increase to 30kΩ at 90o. The device incorporates within the device employing a potential divider network. The potential divider is employed to line the output voltage across 2 resistors connected non-parallel as shown in Figure 2. The electrical device and flex forms a potential divider that divides the input voltage by a quantitative relation determined by the variable and glued resistors.
2.2.3) MICROCONTROLLER
The ATMEGA328-PU is a low power CMOS 8 bit microcontroller based on the AVR enhanced RISC architecture. By executing powerful instructions in a single clock cycle, the ATMEGA328-PU achieves throughputs approaching 1MIPS per MHz allowing the system designed to optimize power consumption versus processing speed. The AVR core combines a rich instruction set with 32 general purpose working registers. All the 32 registers are directly connected to the Arithmetic Logic Unit (ALU), allowing two independent registers to be accessed in one single instruction executed in one clock cycle. The resulting architecture is more code efficient while achieving throughputs up to ten times faster than conventional CISC microcontrollers.
2.2.4) LCD.DISPLAY
We come across LCD displays everywhere around us. Computers, calculators, television sets, mobile phones, digital watches use some kind of display to display the time. An LCD is an electronic display module which uses liquid crystal to produce a visible image. The 16×2 LCD display is a very basic module commonly used in DIYs and circuits. The 16×2 translates a display 16 characters per line in 2 such lines. In this LCD each character is displayed in a 5×7-pixel matrix.
2.2.5) BLUETOOTH MODULE
It is used for many applications like wireless headset, game controllers, wireless mouse, wireless keyboard and many more consumer applications. It has range up to <100m which depends upon transmitter and receiver, atmosphere, geographic & urban conditions. HC-05 is a Bluetooth module which is designed for wireless communication. This module can be used
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 6 Mini Project
in a master or slave configuration. HC-05 is a Bluetooth module which is designed for wireless communication. This module can be used in a master or slave configuration.
2.2.6) ANDROID APPLICATION
In this project we are using an Android application for text to speech conversion. The microcontroller interprets the hand gesture and generate respective messages. These messages are send to the Android app through Bluetooth. The app converts these text messages to the respective audio messages which are transmitted by the phone’s speakers
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 7 Mini Project
3.COMPONENTS LIST AND SPECIFICATION
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 8 Mini Project
COMPONENTS LIST & SPECIFICATION
3.1) ATMEGA 328PU
This microcontroller is considered as the heart of the project. ATmega328 is an 8-bit and 28
Pins AVR Microcontroller, manufactured by Microchip, follows RISC Architecture and has a
flash type program memory of 32KB.It has an EEPROM memory of 1KB and its SRAM
memory is of 2KB,8 Pin for ADC operations, which all combines to form Port A ( PA0 –
PA7). It also has 3 built in Timers, two of them are 8 Bit timers while the third one is 16-Bit
Timer. It operation ranging from 3.3V to 5.5V but normally we use 5V as a standard.
FIGURE 3
FIGURE 4
We use Arduino nano which is a development board which uses ATMEGA 328PU as the
microcontroller. The Arduino Nano is programmed using the Arduino Software (IDE), our
Integrated Development Environment common to all Arduino boards and running
both online and offline
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 9 Mini Project
FIGURE 5
3.2) FLEX SENSORS
FLEX SENSOR is basically a VARIABLE RESISTOR whose terminal resistance increases
when the sensor is bent. So this sensor resistance increases depends on surface linearity. So it
is usually used to sense the changes in linearity. Flex sensors are usually available in two
sizes. One is 2.2 inch and another is 4.5 inch. Although the sizes are different the basic
function remains the same. They are also divided based on resistance. There are LOW
resistance, MEDIUM resistance and HIGH resistance types. Choose the appropriate type
depending on requirement. FLEX SENSOR terminal resistance changes when it is bent.
FIGURE 6
3.2.1) Pin description
FIGURE 7
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 10 Mini Project
PIN NUMBER DESCRIPTION
P1 Usually connected to positive of power
source
P2 Usually connected to ground
TABLE 1
3.2.2) Features and Specifications
• Operating voltage of FLEX SENSOR: 0-5V
• Can operate on LOW voltages
• Power rating : 0.5Watt (continuous), 1 Watt (peak)
• Life: 1 million
• Operating temperature: -45ºC to +80ºC
• Flat Resistance: 25K Ω
• Resistance Tolerance: ±30%
• Bend Resistance Range: 45K to 125K Ohms(depending on bend)
3.2.3) WORKING
FIGURE 8
As shown above figure, when the surface of flex sensor is completely linear it will be having
its nominal resistance. When it is bent 45º angle the flex sensor resistance increases to twice
as before. And when the bent is 90º the resistance could go as high as four times the nominal
resistance. So, the resistance across the terminals rises linearly with bent angle. So, in a sense
the flex sensor converts flex angle to resistance parameter.
3.3) LCD DISPLAY
LCD modules are very commonly used in most embedded projects, the reason being its cheap
price, availability and programmer friendly. Most of us would have come across these
displays in our day to day life, either at PCO’s or calculators.16×2 LCD is named so because;
it has 16 Columns and 2 Rows. There are a lot of combinations available like, 8×1, 8×2,
10×2, 16×1, etc. but the most used one is the 16×2 LCD.
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 11 Mini Project
FIGURE 9
3.3.1) FEATURES
• Operating Voltage is 4.7V to 5.3V
• Current consumption is 1mA without backlight
• Alphanumeric LCD display module, meaning can display alphabets and numbers
• Consists of two rows and each row can print 16 characters
• Each character is built by a 5×8 pixel box
• Can work on both 8-bit and 4-bit mode
• It can also display any custom generated characters
• Available in Green and Blue Backlight
3.4) BLUETOOTH MODULE HC-05
HC-05 module is an easy to use Bluetooth SPP (Serial Port Protocol) module, designed for transparent wireless serial connection setup. Serial port Bluetooth module is fully qualified Bluetooth V2.0+EDR (Enhanced Data Rate) 3Mbps Modulation with complete 2.4GHz radio transceiver and baseband. It uses CSR Blue core 04-External single chip Bluetooth system with CMOS technology and with AFH (Adaptive Frequency Hopping Feature). It has the footprint as small as 12.7mmx27mm. Hope it will simplify your overall design/development cycle.
FIGURE 10
3.4.1) FEATURES
• Serial Bluetooth module for Arduino and other microcontrollers
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 12 Mini Project
• Operating Voltage: 4V to 6V (Typically +5V)
• Operating Current: 30Ma
• Range: <100m
• Works with Serial communication (USART) and TTL compatible
• Follows IEEE 802.15.1 standardized protocol
• Uses Frequency-Hopping Spread spectrum (FHSS)
• Can operate in Master, Slave or Master/Slave mode
3.5) 7805 VOLTAGE REGULATOR
Voltage sources in a circuit may have fluctuations resulting in not providing fixed voltage
outputs. A voltage regulator IC maintains the output voltage at a constant value. 7805 IC, a
member of 78xx series of fixed linear voltage regulators used to maintain such fluctuations, is
a popular voltage regulator integrated circuit (IC).7805 IC provides +5 volts regulated power
supply with provisions to add a heat sink.
FIGURE 11
3.6) ACCELEROMETER ADXL335
The ADXL335 is a small, thin, low power, complete 3-axis accelerometer with signal
conditioned voltage outputs. Measures acceleration with a minimum full-scale range of ±3g.It
can measure the static acceleration of gravity in tilt-sensing applications, as well as dynamic
acceleration resulting from motion, shock, or vibration.
FIGURE 12
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 13 Mini Project
4) CIRCUIT DIAGRAM AND EXPLAINATION
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 14 Mini Project
4.1) CIRCUIT DIAGRAM AND EXPLAINATION
FIGURE 13
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 15 Mini Project
5) SOFTWARE SECTION
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 16 Mini Project
5) SOFTWARE SECTION
5.1) ARDUINO IDE
The Arduino Integrated Development Environment (IDE) is a cross-platform application (for Windows, macOS, Linux) that is written in functions from C and C++. It is used to write and upload programs to Arduino compatible boards.
The source code for the IDE is released under the GNU General Public License, version 2. The Arduino IDE supports the languages C and C++ using special rules of code structuring. The Arduino IDE supplies a software library from the Wiring project, which provides many common input and output procedures. User-written code only requires two basic functions, for starting the sketch and the main program loop, that are compiled and linked with a program stub main ( ) into an executable cyclic executive program with the GNU toolchain, also included with the IDE distribution. The Arduino IDE employs the program avrdude to convert the executable code into a text file in hexadecimal encoding that is loaded into the Arduino board by a loader program in the board's firmware.
The Atmega328p microcontroller, like any other microcontroller, can be quite tasking to use for a beginner. They usually require a certain set of tools, including a programmer (hardware), and a development platform (e.g. Atmel Studio) for writing code. These development platforms, unlike the Arduino IDE usually require high knowledge of C or other programming languages, without the shortcuts and simplified functions which the Arduino provides. To remove this difficulty, the microcontroller is flashed with the Arduino bootloader, which makes it ready for programming using the simpler and easy to use Arduino IDE.
To program the microcontroller using the Arduino IDE, the microcontroller must be connected via some sort of hardware to the computer. This is usually done via two major ways:
1. Using a USB to Serial/TTL Adapter
2. Using an Arduino board
Each of these approaches provides the microcontroller with an interface that enables interaction between the computer and the microcontroller.
5.2) PROTEUS
Proteus is software for microprocessor simulation, schematic capture, and printed circuit board (PCB) design. It is developed by Lab Centre Electronics. Proteus is considered as an important tool for computer aided design. It is a complete electronic design system which lets to simulate entire microprocessor design running actual processor machine code a real time. Proteus includes ISIS schematic capturing software, ProSpice (SPICE3FS) including auto placer and auto router and several virtual system modelling including 8051, 8052, PIC16F873 etc. It combines a super mixed mode circuit simulator based on industry standard SPICE3FS with animated components models and provides an architecture in which additional models can created by anyone including end user.
Consequently, the program allows professional engineers to run interactive simulations of real designs and reap the rewards of this approach to circuit simulation. Proteus features range of simulator models for popular microcontrollers and set of animated models for related peripheral devices such as LED, LCD display, keypads and RS232 terminals. The
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 17 Mini Project
software also includes various templates such as text styles and graphic colures ability to
export graphics (BMP, DXF, EPS, HGL and WMF)
5.3) ANDROID APPLICATION
The app we used in this project is “ARDUINO BLUETOOTH TEXT TO SPEECH”. Arduino
Bluetooth CH-05, CH-06 can communicate with the app by sending text. Arduino Bluetooth
CH-05, CH-06 can communicate with the app by sending text (new line at the end of each
transmission). It will convert the text received to speech.
Text to speech (TTS) makes an android device read the text and convert it to audio out via the
speaker. Android TTS supports multiple languages. TTS is a simple but powerful feature. It
can also be effectively used in mobile APPs dedicated to visually impaired people or in
educational app for kids or can be used in pronunciation learning app, etc. These are some of
the ways you can use TTS. Using Text to Speech enhances interaction between the user and
the mobile application.
FIGURE 14 FIGURE 15
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 18 Mini Project
6) FLOWCHART
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 19 Mini Project
6) FLOWCHART
NO
YES
NO
YES
FIGURE 16
START
POWER ON
GLOVE OF SIGN LANGUAGE
GLOVE CALIBERATED
VALUES ARE CAPTURED BY THE ADC OF THE MICROCONTROLLER
DOES THE 5 DIGITAL VALUES MATCH THE GIVEN VALUES PROVIDED BY THE MICROCONTROLLER?
NO OUTPUT DISPLAY ON LCD
OUTPUT DISPLAYED ON LCD
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 20 Mini Project
7) WORKING
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 21 Mini Project
7) WORKING
Disabled use these gloves to convert sign performed by them into speech. From the
convenience of simple flex sensors, a user is able to interact with others in more comfortable
and easier manner. This makes it possible for the user to not only interact with their
community but with others also and they can also live normal life. The end product will have
a cheap and simplistic design making it easy for users to interact with. The system is capable
of recognizing signs more quickly. Furthermore, real time recognition ratio of nearly 99%
can be easily achieved.
The averaging we do at each interval helps to account for any noise or glitches that the flex
sensors are sometimes prone to. The accuracy of the glove is also somewhat limited by the
size of the person’s hands. The accuracy of each flex sensor is limited beyond a certain point.
Smaller hands will result in a larger degree of bend. As a result, the difference between
slightly different signs with a lot of flex might be too small for users with small hands. The
device uses a low voltage environment, and extremely low frequency communication. The
sensors are well attached, and there are no sharp edges. As a result, we don’t see any large
safety issues associated with the glove. Furthermore, since all communication is done via
cables, our device does not interfere with other designs. The glove can be used by anyone
who fits into it, they would only have to train on it and generate new datasets if they wish for
a higher prediction accuracy than the standard or to incorporate new signs.
The message displayed on the “Arduino Bluetooth Text to Speech” app for the hand gesture
of ‘Hello’ is shown in the image below.
FIGURE 17
LCD display is as shown
1. Hello
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 22 Mini Project
FIGURE 18 FIGURE 19
2. Thanks
FIGURE 20 FIGURE 21
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 23 Mini Project
8) CONCLUSION AND FUTURE SCOPE
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 24 Mini Project
8) CONCLUSION AND FUTURE SCOPE
Sign language is a method used for communication by disabled person. Here we are converting sign language into text and speech so that communication is not limited between them only, utilizing data gloves communication barrier between two different communities is eliminated. Using smart gloves disabled person can also grow in their carrier and makes nation grow as percentage of disabled person are millions in count. Making their future better and hence making nation better.
This report gives a brief about the project that is useful for speech or hear impaired patients. This work was able to meet our expectations quite well. This project was meant to be a finished device to check the feasibility of recognizing sign languages using sensor gloves. The completion of this project suggests that sensor gloves can be used for partial sign language recognition.
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 25 Mini Project
9.REFERENCES
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 26 Mini Project
9) REFERENCES
1) K Abhijit Baskaran; Anoop G. Nair; K Deepak Ram; Krishnan Ananthanarayanan; H. R. Nandi Vardhan “Smart gloves for hand gesture recognition: Sign language to speech conversion system”, 2016 International Conference on Robotics and Automation for Humanitarian Applications (RAHA), IEEE Xplore, May 2017
2) Albert Mayan J, Dr. B. Bharathi, Challapalli Vishal, Chidipothu Vishnu Vardhan Subrahmanyam “Smart Glove For Hand Gesture Recognition Using Sign Language to Speech Conversion System”, International Journal of Pure and Applied Mathematics, Volume 119, pp. 12, 2018.
3) Shahrukh Javed1, Ghousia Banu S1, J Aarthy Suganthi Kani1 and Ateequeur Rahman2 “Wireless Glove for Hand Gesture Acknowledgment: Sign Language to Discourse Change Framework in Territorial Dialect”, Robotics and Automation Engineering Journal, June 26, 2018
4) Gupta, Dhiraj- “Design and development of a low-cost Electronic Hand Glove for deaf and blind”, 2nd International Conference on Computing for Sustainable Global Development (INDIA.Com), pp 501-505, 11-13 March 2015.
5) https://ieeexplore.ieee.org/
6) https://www.researchgate.net/
7) https://www.semanticscholar.org/
8) https://electronicsforu.com/
9) https://www.instructables.com/
10) https://en.wikipedia.org/
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 27 Mini Project
10. DATASHEETS
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 28 Mini Project
10) DATASHEET
10.1) ATMEGA 328PU
FIGURE 22
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 29 Mini Project
FIGURE 23
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 30 Mini Project
FIGURE 24
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 31 Mini Project
10.2) FLEX SENSORS
FIGURE 25
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 32 Mini Project
10.3) HC-05
FIGURE 26
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 33 Mini Project
FIGURE 27
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 34 Mini Project
FIGURE 28
10.4) 16 X 2 LCD
FIGURE 29
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 35 Mini Project
FIGURE 30
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 36 Mini Project
10.5) LM7805
FIGURE 31
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 37 Mini Project
FIGURE 31
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 38 Mini Project
11. FIGURES & TABLES
Smart Glove for Sign Language Conversion
School of Engineering, CUSAT 39 Mini Project
11.1) LIST OF FIGURES
FIG NO
FIGURE
PAGE NO
1
Sign Language
7
2
Block Diagram
9
3
ATMEGA 328PU pinout
13
4
ATMEGA 328PU
13
5
Arduino Nano
14
6
Flex Sensors
14
7
Flex Sensors Pin Description
14
8
Flex Sensor working
15
9
LCD 16x2 pinout
16
10
HC-05 Bluetooth Module connection diagram
16
11
7805 Voltage Regulator Pinout & connection
17
12
ADXL335 connection diagram
17
13
Circuit Diagram
18
14
Android App 1
22
15
Android App 2
22
16
Flowchart
24
17
Android App Display
26
18
Hello Sign
27
19
Hello Display
27
20
Thanks sign
27
21
Thanks display
27
22
ATMEGA 328PU Datasheet
33
23
ATMEGA 328PU Datasheet
34
24
ATMEGA 328PU Datasheet
35
25
Flex Sensor Datasheet
36
26
HC-05 Datasheet
37
27
HC-05 Datasheet
38
28
HC-05 Datasheet
39
29
LCD 16X2 Datasheet
39
30
LCD 16X2 Datasheet
10
31
LM 7805 Datasheet
41
32
LM 7805 Datasheet
42
TABLE 2
11.2) LIST OF TABLES
TAB NO
TABLE
PAGE NO
1
Pin Description of Flex Sensor
15
2
List of figures
44
3
List of Tables
44
TABLE 3
