# Orbit LFO

IN PROGRESS

![Orbit_Face](https://github.com/user-attachments/assets/19bf3e8d-ba15-47b2-9ec3-0fdd290280b1)

## Overview:
This is Orbit, an STM32-based Low Frequency Oscillator (LFO) that I designed for my custom modular 
synthesizer. It features controls for frequency, phase, and amplitude, as well as seven different selectable 
waveforms.

## Features:
The seven available waveforms are:
- sine
- square
- ramp
- sawtooth
- triangle
- random ramp
- random step

The waveform is selected via the "Wave" knob on the front, and the current waveform is indicated by an LED.
You can control the frequency of each waveform via the "Period" knob, through the Tap Tempo button, or by syncing it to an external 5V 
digital signal through the "Sync" input. The phase offset of the wave relative to the sync signal can be controlled by the
"Phase" knob, and the amplitude of the wave is controlled by the "Height" knob. The peak amplitude of each waveform is
quantized to a V/oct standard, with a range of 5 octaves. The module features one normal output and an inverted output that
subtracts the generated waveform from 5V.

## Hardware:
I developed this project on an STM32L432KC NUCLEO dev board, but the code should work on any STM32L4xxxx 
chip. If I get bored sometime I may try to make it work on an Arduino.
IMPORTANT: In order for the NUCLEO board to work properly, you will need to remove the SB15, SB16, and SB18 solder bridges
from the back of the board. This will disable the onboard LED, and disconnect PA5+PA6 from PB6+PB7, allowing them to be used
separately.
	
## Software:
The project is coded completely in bare-metal C, utilizing direct register manipulation rather than 
CubeIDE's HAL or LL functions. I tried to add comments to just about every line (mostly for my own sanity), 
so you should be able to reverse-engineer and/or modify my code if you would like.

## PCBs:
I have included the Gerber files, KiCAD schematic, and BOM for the project, which should be enough for you to recreate it
yourself. Please be aware that this is a 2U design, and thus will probably not work with your Eurorack case. I might make
a 3U version someday if I have the time, but no promises.
	
	
