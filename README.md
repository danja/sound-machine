# Sound Machine

A testbed for trying out sound synthesis ideas built from off-the-shelf modules.

## Hello World!

The current hardware. Hotglued to an A4 aluminium panel (with plastic standoffs).

Click image for YouTube video.

[![Sound Machine Hardware](https://github.com/danja/sound-machine/blob/main/docs/images/hardware_2020-10-16.jpeg?raw=true)](https://www.youtube.com/watch?v=Jbs1Wkpez20 "Sound Machine : Hello World!")

Right now my main focus is still on [Chatterbox](https://github.com/danja/chatterbox), but prompted by that I wanted to have a setup with more power and flexibility (Chatterbox has just an ESP32 with external DAC).

*Probably* the first bits I'll be playing with will be around delay lines and granular synthesis.

**PS. very soon after uploading the above, decided to add an Arduino Mega 2560.**

The software for this module I'm putting in a separate Github repo : [sound-machine-mega2560](https://github.com/danja/sound-machine-mega2560).

![Sound Machine Hardware](https://github.com/danja/sound-machine/blob/main/docs/images/hardware_2020-10-16-later.jpeg?raw=true)

## Components

* Arduino Due : main audio processing
* Arduino Mega 2560 : user interface (keypad, display(s), rotary encoders)
* ESP32 : I/O (Wifi/Web, MIDI, Bluetooth)
* External stereo ADC (I2S)
* External stereo DAC (I2S)
* 4x4 Keypad (matrix)
* 20x4 LCD (I2C)
* Rotary Encoders
* External PSU

*I may well add a little TFT graphic display*

## Code

I'm using PlatformIO on VSCode (on Ubuntu). This seems **much** more convenient for larger projects than the Arduino IDE.

## Current Status

More frequent updates will appear in [notes.md](https://github.com/danja/sound-machine/blob/main/docs/notes.md)

**2020-10-16**

So far I've just hooked up the keypad and display to check they work (yes!). 
Libs:
* https://github.com/Chris--A/Keypad
* https://gitlab.com/tandembyte/LCD_I2C 
  * see also : https://randomnerdtutorials.com/esp32-esp8266-i2c-lcd-arduino-ide/

## Design Notes

It may seem perverse using 3 fairly low-capability modules rather than, say, putting everything on a Raspberry Pi. The coding there would almost certainly be easier. But I reckon I can still keep the total cost down, I already have these modules (!) and also any finished machine doesn't necessarily have to use all the modules. It's also modular! The *blocks*, eg. Mega + UI components, could be used alongside a completely different system. 
What's more this should be more fun! 





