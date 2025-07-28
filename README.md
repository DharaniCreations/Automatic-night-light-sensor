Overview
This project demonstrates a simple light-sensitive switch: it turns lights OFF during the day and ON at night. Ideal for street lights, garden illumination, or home automation.

Materials Required
LDR (Light Dependent Resistor / photoresistor)

BC547 (or equivalent) NPN transistor

Relay module (e.g. 12 V coil, SPDT)

Resistors (e.g., 10 kΩ, 330 Ω)

Zero PCB board or breadboard

Power supply (e.g. 9–12 V DC)

Diode (e.g. 1N4007) for back‑EMF protection

Optional: manual switch, LED indicator

Circuit Diagram
LDR forms half of a voltage divider, paired with a fixed resistor.

The voltage divider’s output is fed to the transistor base.

When it’s bright (day), the LDR resistance is low → base voltage low → transistor OFF → relay OFF → light OFF.

In darkness (night), LDR resistance increases → base voltage rises → transistor switches ON, activating the relay and powering the light 
YouTube
+5
YouTube
+5
YouTube
+5
Instructables
.

Step-by-Step Instructions
Construct the voltage divider: LDR + fixed resistor → center node to transistor base through ~1 kΩ resistor.

Use BC547 as a switch: emitter to ground, collector to relay coil.

Relay coil powered from 12 V; diode placed antiparallel across coil.

Connect the relay’s output contacts to drive the external lighting circuit or LED.

Power the circuit with a steady DC supply.

(Optional) Add a manual override switch in series with load or relay.

Calibration & Tips
Adjust fixed resistor to set light/dark threshold; can use a potentiometer for tuning 
Arduino Forum
.

Add hysteresis or time delay (e.g. via averaging or capacitor) to avoid flickering from passing shadows or clouds.

Install LDR away from the controlled light source to prevent feedback switching.

Example Arduino Variant
Some variations use an Arduino to read analog input from LDR and control a relay with code thresholds (e.g., activate when LDR reading drops below ~700) 
roboticsinsighto.com
learn.voltaat.com
.

Applications
Street and outdoor lighting control

Automated garden lights

Emergency lighting systems

Home automation for energy saving

Safety Notes
When switching AC mains, take proper insulation precautions or use a solid‑state relay.

For DC loads, ensure transistor and relay ratings are adequate.

Always include a flyback diode across relay coils to protect transistor.
