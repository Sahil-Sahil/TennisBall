## Humber Institute of Technology and Advanced Learning
# Solenoid (PingPong Machine)
## Created by: Sahil Sahil
-------------

![Fianl](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1428%20(1).jpg?raw=true)

#

## Introduction

Solenoid is the generic term for a coil of wire used as an electromagnet. It also refers to any device that converts electrical energy to mechanical energy using a solenoid. The device creates a magnetic field from electric current and uses the magnetic field to create linear motion.

#

## Table of Contents
* [Introduction](#introduction)

* [Parts Required and Budget](#Part-Required-and-Budget)

* [Time Commitment](#time-Commitment)

* [Setting up Raspberry Pi](#setting-Up-Raspberry-Pi)

* [Hardware Testing](#Hardware-Testing)

* [Assembling ](#Assembly)

* [PCB & Soldering ](#PCB-and-Soldering)
 
* [Enclosure](#Enclosure)

* [Testing](#testing)

* [Production-Testing](#Production-testing)

* [Final Product](#final-product)

#


## Parts Required and Budget

The Parts Required for the project -:

* [Raspberry Pi 4B Kit](https://www.amazon.ca/Raspberry-Pi-Computer-Model-4GB/dp/B07W4JM192/ref=sr_1_4?crid=38D5SW1ETTEZ5&keywords=raspberry+pi+4&qid=1576171042&sprefix=ras%2Caps%2C251&sr=8-4) - CAD$100.05
* [Solenoid](https://www.amazon.ca/gp/product/B00LBQ229Y/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) - CAD$20
* [Transistor IRL 520N](https://www.amazon.ca/CanaKit-Raspberry-Complete-Starter-Kit/dp/B01CCF6V3A/ref=sr_1_5?s=pc&ie=UTF8&qid=1516324581&sr=1-5&keywords=Raspberry+Pi+3) - CAD$15
* [Diode 1N4001-TP](https://www.amazon.ca/gp/product/B008UG13UW/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) - CAD$10
* [Resistor 2.2k/300 ohm](https://www.amazon.ca/ELEGOO-Values-Resistor-Assortment-Ohm-1M/dp/B071HJWJZB/ref=sr_1_8?crid=5U1W9IPQ0MI2&keywords=resistor+kit&qid=1576171176&s=hi&sprefix=resistor%2Ctools%2C180&sr=1-8) - Price depends on You
* [Circuit Board](https://github.com/Sahil-Sahil/TennisBall/blob/master/Electronics-PCB/Sahil_SmartPingpongBallMachineV4.zip) - These are Files for PCB(Gerber files) and Circuit send them for printing while you ordering the parts for project
* [CAse Design Files](https://github.com/Sahil-Sahil/TennisBall/blob/master/Mechanical-3D%2C%20Printing%20Files/Enclosur.cdr) - These are Files for Case design send them for printing while you ordering the parts for project. You may have to make some some changes as your project needs.

#

## Time Commitment
This project can be done in one weekend. It will take about 2 to 4 days to recieve the parts. If you want to skip breadboarding then you can get started with the soldering which would take about 10 minutes but testing can take about 2 hours. After getting address, it should take one more hour to run the python script and get the readings.

#

## Setting up Raspberry Pi
First step after getting your raspberry pi is to set it up. Follow the steps below:(I Used Ethernet Cable to Connect to pi By RDP)
1. Download [Raspbian](https://www.raspberrypi.org/downloads/) to be installed on your raspberry pi.
2. Use [SDCardFormatter](https://www.sdcard.org/downloads/formatter_4/) to format your SD card and flash downloaded OS on your SD card.
3. Insert SD card in raspberry pi 
4. Download [Xming](https://sourceforge.net/projects/xming/) software into your PC and run
5. connect your raspberry pi to Laptop or Pc by ethernet cable or connector
6. Open putty Typing "raspberrypi.mshome.net" or the "Ip address" of pi which you can get by running advance ip scanner.
4. Add when you open the terminal you see your pi running.

#

## Hardware Testing

After software installation, i made the connections using jumper wires from sensor to breadboard and breadboard to raspberry pi. which you can see in Circuit breadboard design.

Wiring:
---
- Raspberry Pi PIN 3 to as Ground
- Raspberry Pi GPIO 11 to solenoid

### Circuit
This wiring diagram could be helpful to make the connections on breadboard

![Breadboard Design](Electronics-PCB/STennisBall_bb.jpg)

#

## Assembly
Now you have got every part we are goung o connect all the parts on breadboard so we can design a PCB later. to connect all the parts on breadboard you can see the fritizzin image above or downone. 

![Breadboard Design](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1338%20(1).jpg?raw=true)

Make sure all the connection are right connected to ground and Please make sure to connect a multimeter accros the solenoid because it throws huge amount of current when it turns on and off and it cna damage your whole circuit becaus eof that  i had to order whole bunch of transistors again, and i short-out my raspberry pi GPIO pin 4.

#

## PCB and Soldering
If your breadboard circuit works we are goin to design PCB for designing PCB you can use [Fritzzing](https://fritzing.org/download/)
and down is the image how its going to look alike.

![PCB Design](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/STennisBall2_pcb.jpg?raw=true)

and when  your PCB iss ready we are going to solder all the components on it and its going to be looklike down Image.

![PCB Soldering](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1424%20(1).jpg?raw=true)
![PCB Soldering](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1425%20(1).jpg?raw=true)

If your PCB is ready then we are goin to desig enclosur for our project

#

## Enclosur
For designing the case you can use CoralDrwa or another free software that you can use is InkSpace its easy to use and free
My design for enclosur is [here](https://github.com/Sahil-Sahil/TennisBall/blob/master/Mechanical-3D%2C%20Printing%20Files/Enclosur.cdr)
![PCB Soldering](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1426%20(1).jpg?raw=true)

#

## Testing
Now we have every thing we are going to run it for the we going to connect it to raspberry pi and run the Phyton [Code](https://github.com/Sahil-Sahil/TennisBall/blob/master/Firmware-Sensor%2C%20Effector%20Intertface%20Code/solenoidP.py)
![testing](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/Annotation%202019-12-12%20135026.jpg?raw=true)

#

## Final-Product
Here is the final product a workig solenoid which will act as valve in PinPong ball project to control the number of balls.
I'm unable to combine every thing because it will take another day but my project is due on 21/12/2019
![Final Piece](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1428%20(1).jpg?raw=true)

Without solenoid Connected
![Final Piece](https://github.com/Sahil-Sahil/TennisBall/blob/master/Images/IMG_1427%20(1).jpg?raw=true)
