---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 5 · 3D Printing and Scanning|Last week]] - [[Week 7 · Computer-Controlled Machining|Next week]]_

_From [[MDEF Academy 1]]_

| Day                         | Description        |
|:--------------------------- |:------------------ |
| [[2022-03-02\|02/03]] · Wed | Electronics Design | 

## Links
- [Local reference: Electronics design](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week06/)
- [Local recording: Electronics design overview and Kicad](https://www.youtube.com/watch?v=-_Ww6-VPfP0)
- [Global reference: Electronics design](http://academy.cba.mit.edu/classes/electronics_design/index.html)
- [Global recording: Electronics design](https://vimeo.com/683965879)

---

## Assignment
> [Week 6 · Electronics Design](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-6-electronic-design)
> - Design a PCB board **also called breakout-board** for your ESP32 HUZZAH 32 microcontrollers (or other board that you want to use raspberry pi, etc.) that allows you to connect an input (sensor) or an output (actuator) to your commercial board without cables.
> - Include the design files in your webpage and explain well the process on how you did it.

I designed a single-sided PCB shield for my Arduino Nano. It has through holes for pin headers for the Arduino Nano, a momentary pushbutton, a light-dependent resistor, a light-emitting diode, a potentiometer, and the supporting resistors. Because it will be a single-sided board with the Arduino Nano secured with through-hole soldering and I want the board to sit flat on the table, I decided to use through-hole components so all the parts will be on the same side of the board. This was my first time using KiCAD; I have used Altium to design PCBs in the past. The button is connected to D7, the LDR is connected to A2, the LED is connected to D9, and the Potentiometer is connected to A0. I started with the schematic, then chose footprints for the components, then arranged the footprints on the PCB, then routed the traces, then tweaked everything, then exported the files for manufacturing.

Schematic:

![[Pasted image 20220904181345.png]]

Screenshot from PCB Editor from the front (traces are on the front layer, jumper and components are on the back):

![[Pasted image 20220904190521.png]]

Board routing render:

![[Pasted image 20220904190910.png]]

Design files:

![[NanoShield.zip]]

## Reflection

#### Content 
This week we discussed electronic components, circuits, design software, and test equipment, among other things.

#### Feelings
This week I felt disengaged during the classes, which were long and boring and very difficult to follow. I felt engaged when skipping through and watching the important bits of the recording specific to KiCAD at 2.5x speed and teaching myself a well-rounded understanding of KiCAD through the process of making a PCB.

#### Learnings
This week I learned how to use KiCAD. I used the `d` key to drag components in the PCB layout without disconnecting traces. The grid was my friend. I used a grid size equal to the track width and clearance of 0.025in, which seemed like a good value for 0.1in pitch through hole components with 1.6mm pads. If the tracks or clearance was any larger, tracks would not have enough clearance to diagonally enter the through-hole pads. If the components were metric, I'd have used a metric grid and a metric track width. Through-holes seem to be 1mm diameter, with 1.6mm diameter for the pads. I started by using vias that were the same as the through holes because I will be soldering a single wire jumper as my second layer of the board, but since vias in filled zones don't have thermal relief, I replaced each via with a custom single through-hole component with the same dimensions as a via. 

#### Inspiration
I am looking forward to seeing how good the integration between KiCAD and FreeCAD is. Also I'd like to look at the KiCAD plugins and python scripting.

#### Notable references
- [How does KiCad know which symbol pin represents which pad of the footprint?](https://forum.kicad.info/t/how-does-kicad-know-which-symbol-pin-represents-which-pad-of-the-footprint/11889)
- [Measuring distance in Kicad layout](https://forum.kicad.info/t/measuring-distance-in-kicad-layout/2066)
- [Moving PCB footprint with wires connected?](https://forum.kicad.info/t/moving-pcb-footprint-with-wires-connected/22006)
- [How to fill a zone within a zone](https://forum.kicad.info/t/how-to-fill-a-zone-within-a-zone/7788)
- [VIAs thermal relief](https://forum.kicad.info/t/vias-thermal-relief/1561)
- [Thermal spoke orientation](https://forum.kicad.info/t/thermal-spoke-orientation/21626)

