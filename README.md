# Ultrasonic Theremin

An instrument and memory game running on a PIC18F4321 microcontroller, written in PIC assembly. The player programs a sequence using a keypad and plays it back by moving their hand over an ultrasonic sensor.

## How it works

- The HC-SR04 sensor measures distance. The firmware maps the measured interval to one of seven notes.
- A timer generates the waveform for the speaker and a PWM signal positions the servo score indicator.
- A keypad records the target sequence, with debouncing and EEPROM-based decoding.

[Photos of the prototype](docs/hardware-implementation.pdf)

## Build

Open `assembly-musical.X` in MPLAB X IDE, select the PIC18F4321 device and the XC8 PIC Assembler (pic-as), then build the project. The original configuration uses pic-as 3.00. MPLAB X generates the local makefiles using the toolchain installed on your machine. The assembly source is in [code.asm](assembly-musical.X/code.asm).

## Project credits

Academic team project by Jofre Tura Centelles and Guillem Gil at La Salle Campus Barcelona. The [original repository](https://github.com/guillemgpide/pic18f-ultrasonic-theremin) was published by Guillem Gil. This portfolio copy is based on revision `88794b2403bd`.

The original MIT license and copyright notice are included in [LICENSE](LICENSE).
