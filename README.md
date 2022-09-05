# AMSKeyboard
AMSKeyboard - PS/2 Keyboard interface for the Amstrad CPC

This so far is the first revision of a modification of the PS/2 edition of the C64keyboard project by Robert VanHazinga for the Amstrad CPC range of computers. So far only tested with the Amstrad CPC 6128 and only providing regular keys on such.
Diagrams and tables of mappings will follow, but as a basis they are simply modifications of the C64keyboard project.

I'd originally attempted this using the CPC connected straight to io lines - on the Pi with GPIO via level converters as well as an awkward mapping on Arduino. Both worked out badly. Rob "Peepo" Taylor pointed me in the direction of the C64keyboard project which uses the MT88xx chip as an intermediate device and here we are.

Requirements

* Arduino Nano (ATMega328)
* MT8812/8816
* PS/2 Keyboard
* Amstrad CPC
* Way of connecting things together

Basic Rules

* The numeric keypad F keys will work on the PS/2 numeric keypad with Num Lock on. These keys are also on the PS/2 F keys.
* The code allows for switching between two keymaps, and I've only done the one so far, largely representing the keys from the 6128 keyboard in their physical position on the PC keyboard. My thoughts for a second map will be to naturalise the PC keyboard onto the CPC - basically, the other way round.
* There aren't enough lines on the MT8808 for the Amstrad CPC, so if you're going to try that, you'll have to forgo something.

Known Issues

* It's British English layout right now.
* Only tested on an Arduino Nano
* Only tested with an MT8816
* Only tested on the CPC 6128, and there will be keys missing on other models
* Tab doesn't work
* Backtick doesn't work
* Right Ctrl key isn't mapped yet (forgot)
* Some keymashes seem to press seemingly random keys
* Typing too quickly sometimes has issues

These latter two issues might prove unresolvable. Any suggestions welcome.

Update: 05/09/2022. Added prototype (tested) gerber for 6128. Overlays IC101 (74LS145) and IC102 (AY) leaving keyboard connectors exposed. Requires 17-20mm pin headers.
