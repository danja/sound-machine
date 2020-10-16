# Sound Machine

A testbed for trying out sound synthesis ideas built from off-the-shelf modules.

## Hello World!

The current hardware. Hotglued to an A4 aluminium panel (with plastic standoffs).

Click image for YouTube video.

[![Sound Machine Hardware](https://github.com/danja/sound-machine/blob/main/docs/images/hardware_2020-10-16.jpeg?raw=true)](https://www.youtube.com/watch?v=Jbs1Wkpez20 "Sound Machine : Hello World!")

Right now my main focus is still on [Chatterbox](https://github.com/danja/chatterbox), but prompted by that I wanted to have a setup with more power and flexibility (Chatterbox has just an ESP32 with external DAC).

*Probably* the first bits I'll be playing with will be around delay lines and granular synthesis.

## Components

* Arduino Due : main audio processing
* ESP32 : user interface & I/O
* External stereo ADC (I2S)
* External stereo DAC (I2S)
* 4x4 Keypad (matrix)
* 20x4 LCD (I2C)
* Rotary Encoders
* External PSU

A minor snag so far is that the keypad is taking 8 GPIO lines from the ESP32. I want a lot of knobs to twiddle so may look at multiplexing the keypad and/or rotary encoders. The Due has quite a few GPIO lines, but I want to keep this device's processing focussed on the audio.

I am very tempted to add an Arduino Mega to handle UI, the ESP32 for IO only. These modules are so inexpensive, and I need to look at inter-module comms anyway, for ESP32-Due. 

## Code

I'm using PlatformIO on VSCode (on Ubuntu). This seems **much** more convenient for larger projects than the Arduino IDE.

So far I've just hooked up the keypad and display to check they work (yes!). 
Libs:
* https://github.com/Chris--A/Keypad
* https://gitlab.com/tandembyte/LCD_I2C





