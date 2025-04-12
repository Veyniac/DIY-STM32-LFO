# DIY-STM32-LFO

Overview:
	This project is an STM32-based Low-Frequency Oscillator (LFO) that I designed for my custom modular 
synthesizer. It features controls for frequency, phase, and amplitude, as well as seven different selectable 
waveforms.

Features:

The seven available waveforms are:
- sine
- square
- ramp
- sawtooth
- triangle
- random quantized ramp
- random quantized step


	The waveform is selected via the "Wave" knob on the front, and the current waveform is indicated by an LED.
You can control the frequency of each waveform via the "Frequency" knob or by syncing it to an external 5V 
digital signal. The phase offset of the wave relative to the sync signal can be controlled by the  "Phase" 
knob, and the amplitude of the wave is controlled by the "Amplitude" knob. The quantized outputs conform to a 
V/oct standard, with increments of 1 semitone.

Hardware:
	I developed this project on an STM32L432KC NUCLEO dev board, but the code should work on any STM32L4xxxx 
chip. 
	
Software:
	The project is coded completely in bare-metal C, utilizing direct register manipulation rather than 
CubeIDE's HAL or LL functions. I tried to add comments to just about every line (mostly for my own sanity), 
so you should be able to reverse-engineer and/or modify my code if you would like.