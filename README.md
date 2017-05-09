# Microbit Presentation


### Introduction

The Microbit is a microcontroller created by the BBC in a continuing trend to bring younger generations into the world of programming and IOT.  And to that end, I think the makers of the Microbit did a fantastic job:
* The device is fitted with a number of onboard sensors, buttons, leds, and more.  
* The libraries available for the Microbit's programming are numerous and incredibly easy to work with.  
* The power consumption is incredibly low compared to a pi or arduino. Two triple A batteries that last as long as two weeks when idling, several days on full load http://www.reuk.co.uk/wordpress/microbit-battery-capacity/
* Numerous programming languages work well with the micro bit, including drag and drop languages for newcomers
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

### What do the libraries offer?

For those new to programming, a library is a file containing code for use in projects.  A library is no different from the scripts that a programmer typically writes: all programming logic remains the same. By "importing" a library, you are able to use the functions contained in that library.  This has the benefit of keeping your application easy to read and reducing repetition while adding new functionality.

What functions are offered by the Microbit library? Everything and the kitchen sink, practically:
1. robotic speech library.  Connect headphones to pins 0 and ground with alligator clips and listen! The sound is fait, a separately powered speaker might be ideal.
2. neopixel library - control arrays of neopixels wth your microbit!  The microbit can power up to 8 neopixels at a time on its own, or all of them if the neopixels are powered separately.
3. Gestures library - because we have an accelerometer on board, the microbit is also able to sense gestures such as shake, up, down, left, right, or fall.
4. LED Library - Easily light up the matrix with the images provided by the library.  You can also input some text that will be displayed in a scroll fashion across the leds (this feature is very handy and is used in runtime error reporting).

### Programming Languages and Editors

There are a number of languages available for the microbit:
* Microsoft Touch
* Microsoft Blocks
* Javascript (Code Kindom)
* Micropython (Mu offline text editor is what I have used, located here https://github.com/mu-editor/mu)

Note: I have used Mu on Raspberry Pi and Windows without issue, Ubuntu was problematic.

More information on available editors at https://www.microbit.co.uk/create-code

### Full Example of the Microbit using Micropython and the Mu editor

Lets say that you want the microbit to display "hello" every time button a is pressed.  The code would be as follows:

```
import microbit                            # import the microbit library, which contains functions for button_a and display

while True:                                # This while statement causes the code below it to loop forever
    if microbit.button_a.was_pressed():    # This statement checks to see if the a button was pressed on this loop cycle
        microbit.display.scroll("hello")   # Scroll the text across the screen
        
                                           # Thats it! Easy peasy.
                                  
```

### Getting Started

To get started programming with mu, visit the following repository: https://github.com/mu-editor/mu
OR
Visit the following link: https://codewith.mu/

There are great instructions to guide you on installation, for the Raspberry Pi and Windows it was a breeze.


1. Once installed, open the mu text editor.  In Windows this is as simple as clicking on the downloaded file.
2. Connect your microbit to the pc
3. Copy or write any code you would like into the editor
4. Click save
5. Click flash.  You should see the microbit blink a yellow light on the back to show the script is loading. Then the script should begin.

### Demonstration Projects

I have create some additional projects.  The code is very heavily commented to help newcomers understand what each piece of code does.

**Basic Examples** - https://github.com/mabiesen/microbit_basic_examples

**Space-Invaders** - https://github.com/mabiesen/microbit_space_invader

**In Home Alarm System** - https://github.com/mabiesen/microbit_alarm_system

**LED Reusable Drip Class** - https://github.com/mabiesen/microbit_matrix_drips

**My version of the Firefly project** - https://github.com/mabiesen/microbit_pass_the_light

**Control a Laserpointer by moving microbit** - https://github.com/mabiesen/microbit_pi_laser_pointer
