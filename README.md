# AMSKeyboard
AMSKeyboard - PS/2 Keyboard interface for the Amstrad CPC

This so far is the first revision of a modification of the PS/2 edition of the C64keyboard project by Robert VanHazinga for the Amstrad CPC range of computers. So far only tested with the Amstrad CPC 6128 and only providing regular keys on such.
Diagrams and tables of mappings will follow, but as a basis they are simply modifications of the C64keyboard project.

I'd originally attempted this using the CPC connected straight to io lines - on the Pi with GPIO via level converters as well as an awkward mapping on Arduino. Both worked out badly. Rob "Peepo" Taylor pointed me in the direction of the C64keyboard project which uses the MT88xx chip as an intermediate device and here we are.

Requirements

* Arduino Nano
* MT8812/8816
* PS/2 Keyboard
* Amstrad CPC
* Way of connecting things together

Basic Rules

* The numeric keypad F keys will work on the PS/2 numeric keypad with Num Lock on. These keys are also on the PS/2 F keys.
* The code allows for switching between two keymaps, and I've only done the one so far, largely representing the keys from the 6128 keyboard in their physical position on the PC keyboard.

Known Issues

* It's British English layout.
* Only tested on an Arduino Nano
* Only tested with an MT8816
* Only tested on the CPC 6128, and there will be keys missing on other models
* TAB doesn't work
* Backtick doesn't work
* Right CTRL key isn't mapped yet
* Some keymashes seem to press seemingly random keys
* Typing too quickly also has issues

These latter two issues might prove unresolvable. Please help if you can.
