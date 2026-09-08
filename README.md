# Alternating LED Heart PCB

A custom heart-shaped PCB designed as a Mother's Day gift.

![3D PCB Render](media/Gift%20project%20render.png)

## Features

- Heart-shaped PCB
- Red LED array forming an "M"
- White perimeter LED array
- Alternating blinking effect (see video in the "media" folder)
- 555 timer oscillator
- BJT inverter for complementary signals
- MOSFET and BJT LED switching circuits
- 4×AA battery power supply
- Custom 3D-printed stand

## Overview
The circuit uses a 555 timer to generate a square wave. A BJT inverter creates the complementary signal needed for the two LED banks to blink in an alternating fashion. The design had the goal of maximizing each LED's brightness to ensure visibility during daytime. With the amount of LEDs wired in parallel on each bank, transistors were necessary to handle each bank's loads in order to avoid exceeding the 555 timer's maximum rated output current.

The PCB was designed in KiCad and manufactured through JLCPCB. Component selection included evaluating part substitutions when ordering from JLCPCB to reduce cost while maintaining functionality. The custom plastic stand for this board was designed with Autodesk Fusion and printed with a Bambu P1P using standard PLA. To prevent the assembled gift from tipping over, the stand was designed so that the weight of the board's batteries minimized the height of the gift's center of gravity.

This is my first PCB, and was made at the tail end of my freshman year at college (thus before I took any Electrical Engineering classes). Feel free to leave comments at rfe295@tamu.edu
