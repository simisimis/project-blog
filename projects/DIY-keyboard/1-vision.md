# `DeeDee` ⌨️

_Ooo.. What does this button do.._

## Main objectives
- Frankenstein my own DIY keyboard from the shared wisdom of the internet.
- Write/use a firmware for it.
- Document it well and share parts of it.

## Design idea(subject to change)
- DIY!
- Column staggered monoblock split (Absolem like) 
- Low profile Kailh Choc v1 Sunset 36key: 2x 18key(15 + 3 for thumb cluster ).
- Addressable LEDs
- 2 rotary encoders  EC11. Perhaps EC12 for low profile.
- Cirque trackpad.
- 64×48 OLED(Seeed Studio Grove SSD1306 0.66")
- Controller that could run as USB or BLE HID
- Bluetooth

## Goals that define basic success
1. Designed and 3d printed case
2.  Wiring:
	- Plan A: Designed and ordered pcb with reset buttons, power leds and switches broken out on the case etc etc etc.
	-  Plan B: Handwired.
3. Encoder, trackpad and display in place even if they aren't going to be connected. 
4. Connected through USB 

## End goal of unachievable completion
- Runs on keyberon rust firmware
- Secondary parts support
	1. Trackpad
	2. Encoders
	3. Display support 
	4. LEDs
