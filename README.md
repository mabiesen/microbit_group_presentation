# Microbit Presentation


### Introduction

The Microbit is a microcontroller created by the BBC in a continuing trend to bring younger generations into the world of programming and IOT.  And to that end, I think the makers of the Microbit did a fantastic job:
* The device is fitted with a number of onboard sensors, buttons, leds, and more.  
* The libraries available for the Microbit's programming are incredibly easy to work with.  
* The power consumption is incredibly low compared to a pi or arduino
* Numerous programming languages work well with the micro bit
* A basic kit, complete with micro-to-usb cable and triple A battery pack, is about 17 dollars(with shipping around 25 dollars)

Interested? They can be purchased at the following link https://www.adafruit.com/product/3362.

### Truly Basic Specs

A couple of basic details:  ARM Cortex-M0 32 bit processor, 16KB RAM, nRF51 Application Processor

Full specs available at http://tech.microbit.org/hardware/

### What are the Microbit's IO capabilities?

1. Accelerometer
2. Compass, both for direction and detection of magnetic field strength
3. 25 LEDs
4. 2 programmable buttons
5. bluetooth (not compatible with micropython)
6. 2.4 GHZ transceiver for radio
7. 3 GPIO pads, 3v out, and ground connection.  Additionally, one can use the led pins for a total of 19 pins.
8. temperature sensor – meant for the cpu but does an okay job detecting ambient room temp

### Programming Languages and Editors

There are a number of languages available for the microbit:
* Microsoft Touch
* Microsoft Blocks
* Javascript (Code Kindom)
* Micropython (Mu text editor is what I have used, located here https://github.com/mu-editor/mu)

Note: I have used Mu on Raspberry Pi and Windows without issue, Ubuntu was problematic.

More information on available editors at https://www.microbit.co.uk/create-code

### Demonstration Projects

I have create a few projects to demonstrate the capabilities of the microbit.  Links may be found below:

**Basic Examples** - https://github.com/mabiesen/microbit_basic_examples

**In Home Alarm System** - https://github.com/mabiesen/microbit_alarm_system

**My version of the Firefly project** - https://github.com/mabiesen/microbit_pass_the_light
