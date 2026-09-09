# Alternating LED Heart PCB

A custom heart-shaped PCB designed as a Mother's Day gift.

![3D PCB Render](media/Gift%20project%20render.png)

## Features

- Heart-shaped PCB
- Red LED bank forming an "M"
- White perimeter LED bank
- Alternating blinking effect (see video in the "media" folder)
- 555 timer oscillator
- BJT inverter for complementary signals
- MOSFET and BJT LED switching circuits
- 4xAAA battery power supply
- Custom 3D-printed stand

## Overview of Design Decisions
The circuit uses a 555 timer to generate a square wave in its astable oscillator configuration. A design requirement was to have the different colored LED banks to turn on when the other is off (e.g. if the white LEDs are on, turn the red ones off, and vice versa). I opted to implement this behavior with transistors, as doing so with a microcontroller would've been overkill. A BJT inverter creates the complementary signal needed for the two LED banks to blink in an alternating fashion, with the complemented signal tied to the base of the driving transistor of one bank, and the direct 555 timer output tied to the base of the other bank's transistor. Why do transistors control the LED banks? One goal of the design was to maximize each LED's brightness to ensure visibility during daytime. With the amount of LEDs wired in parallel on each bank, transistors were necessary to handle each bank's loads in order to avoid approaching or exceeding the 555 timer's maximum rated output current. 

In the event that debugging the board was required, multimeter test points were added to relevant points in each net, but I never ended up needing to use them beyond checking continuity before plugging in the batteries. Including the test points, most components chosen for this board ended up being through-hole in order to give myself more soldering experience without needing a ton of additional equipment. However, I opted for surface mount technology for parts such as resistors or ceramic capacitors as I didn't have much (or any) of either in my electronics inventory.

The PCB was designed in KiCad and manufactured through JLCPCB. Component selection included evaluating part substitutions when ordering from JLCPCB to reduce cost while maintaining functionality. The custom plastic stand for this board was designed with Autodesk Fusion and printed with a Bambu P1P using standard PLA. To prevent the assembled gift from tipping over, the stand was designed so that the weight of the board's batteries minimized the height of the gift's center of gravity. 

This is my first PCB, and was made at the tail end of my freshman year at college (thus before I took any Electrical Engineering classes). Feel free to leave comments or critiques at this email (rfe295@tamu.edu).
