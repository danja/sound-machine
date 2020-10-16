# Sound Machine

A testbed for trying out sound synthesis ideas built from off-the-shelf modules.

Right now my main focus is still on [Chatterbox](https://github.com/danja/chatterbox), but prompted by that I wanted to have a setup with more power and flexibility (that has just an ESP32 with external DAC).

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

I am very tempted to add an Arduino Mega to handle UI. 

## Code

I'm using PlatformIO on VSCode. This seems **much** more convenient for larger projects than the Arduino IDE.



