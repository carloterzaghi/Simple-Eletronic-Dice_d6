# Simple Electronic Dice Using 4017BD and 555 Timer

## Overview
This project implements a simple electronic dice circuit using a 4017BD decade counter IC and a 555 timer IC. The circuit simulates a dice roll by lighting up a pattern of LEDs (LED1 to LED6) to represent numbers 1 to 6. A pushbutton triggers the dice roll, and the 555 timer generates a clock signal to cycle through the 4017BD counter outputs, which control the LEDs.

## Features
- Simulates a dice roll using 6 LEDs to represent numbers 1 to 6.
- Uses a 555 timer to generate a clock signal for random LED selection.
- Utilizes a 4017BD decade counter to drive the LEDs.
- Triggered by a pushbutton for user interaction.
- Powered by a 9V supply.
- PCB design included (Gerber files available in the project directory).

## Hardware Requirements
- **4017BD Decade Counter IC**: Drives the LEDs to display the dice roll result.
- **555 Timer IC**: Generates a clock signal to cycle the counter.
- **LEDs (LED1 to LED6)**: Represent the dice faces (1 to 6).
- **Pushbutton (SW1)**: Triggers the dice roll.
- **Resistors**:
  - R1: 4.7kΩ (pull-down for pushbutton)
  - R2 to R7: 330Ω (current limiting for LEDs)
  - R8: 10kΩ (timing resistor for 555)
- **Capacitors**:
  - C1: 100nF (decoupling for 555)
  - C2: 10nF (timing capacitor for 555)
- **Power Supply**: 9V (via a 2-pin connector).
- **Connectors**: For power input (9V and GND).

## Schematic and PCB
- **Schematic**: The schematic diagram is provided below. It includes the 555 timer, 4017BD counter, LED connections, and power supply circuit.

  <div style="text-align: center;">
    <img src="schematic.png" alt="Schematic Diagram">
    </br></br>
  </div>

- **PCB Layout**: The PCB layout is shown below, matching the schematic with labeled connections for easy assembly. Gerber files are available in the project directory for manufacturing.

  <div style="text-align: center;">
    <img src="pcb_layout.png" alt="PCB Layout">
    </br></br>
  </div>

- **3D Render**: A 3D render of the assembled PCB is shown below, illustrating the component placement.

  <div style="text-align: center;">
    <img src="3d_pcb_image.png" alt="PCB 3D Render">
  </div>

## Usage
1. Assemble the circuit as per the schematic or use the provided PCB.
2. Connect a 9V power supply to the 2-pin connector (VCC and GND).
3. Press the pushbutton (SW1) to simulate a dice roll.
4. The LEDs (LED1 to LED6) will light up in a pattern representing a number from 1 to 6.

## Notes
- The 555 timer operates in astable mode, generating a clock signal to cycle the 4017BD counter outputs until the pushbutton is released.
- The 4017BD counter's outputs (Q0 to Q5) are connected to the LEDs to display the dice roll result.
- Ensure proper grounding (GND) to avoid noise issues.
- The timing of the 555 timer can be adjusted by changing the values of R8 and C2 if a different roll speed is desired.