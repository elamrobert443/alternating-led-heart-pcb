# Alternating LED Heart PCB

A custom heart-shaped PCB designed as a gift project and created in KiCad.

![3D PCB Render](media/Gift%20project%20render.png)

## Features

- Heart-shaped PCB
- Red LED array forming an "M"
- White perimeter LED array
- Alternating blinking effect
- 555 timer oscillator
- BJT inverter for complementary signals
- MOSFET and BJT LED switching circuits
- 4×AA battery power supply

## Design Process

The PCB was designed in KiCad and manufactured through JLCPCB. Component selection included evaluating substitutions to reduce cost while maintaining functionality.

The circuit uses a 555 timer to generate a square wave. A BJT inverter creates the complementary signal needed to alternate between the two LED banks.
