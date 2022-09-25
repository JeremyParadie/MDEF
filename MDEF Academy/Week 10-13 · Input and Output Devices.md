---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 9 · Molding and Casting|Last week]] - [[Week 14 · Networking and Communications|Next week]]_

_From [[MDEF Academy 1]] and [[MDEF Academy 2]]_

| Day                         | Description    |
|:--------------------------- |:-------------- |
| [[2022-03-30\|30/03]] · Wed | Output Devices |
| [[2022-04-20\|20/04]] · Wed | Input Devices  | 

## Links
- [Local reference: Output devices](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/outputs/)
- [Local reference: Output devices local class](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/outputs/local/)
- [Local reference: DIY outputs](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/outputs/diy/)
- [Global reference: Output devices](http://academy.cba.mit.edu/classes/output_devices/index.html)
- [Global recording: Output devices](https://vimeo.com/694104183)
- [Local reference: Input devices](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/inputs/)
- [Local reference: Input devices local class](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/inputs/local/)
- [Local reference: Digital signal processing](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/inputs/dsp/)
- [Local reference: DIY sensors](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/inputs/diy/)
- [Global reference: Input devices](http://academy.cba.mit.edu/classes/input_devices/index.html)
- [Global recording: Input devices](https://vimeo.com/701366158)

---

## Assignment
> [Week 10-13 · Input and Output Devices](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-10-output-devices-13-input-devices)
> - **You remember when you had to DESIGN A PCB for week 6? “design a pcb for an input or an output”** now it is time to fabricate it (finish the design - mill it - solder it)
> - Make the PCB you designed real and make it work (you have from these week until INPUT WEEK- included)

I fabricated the PCB that I designed in [[Week 6 · Electronics Design]]

![[20220919_141809.jpg]]

![[20220921_160358.jpg]]

![[20220921_160542.jpg]]

![[20220921_160752.jpg]]

![[20220921_162443.jpg]]

%%

the feeds and speeds below were what I gathered online. See my email for the feeds and speeds recommendations from John from PreciseBits
https://mail.google.com/mail/u/0/?zx=25hpy3o83w1o#inbox/KtbxLwgprDsCfSxBndzVpJFGnqgpWjRNVq

7000 rpm
0.0156in tool diameter
0.004in cut depth
3mm per second (default 4mm/s)

7000 rpm
0.0312in tool diameter
0.024in cut depth per pass
0.06889in total depth
1.5mm per second (default 4mm/s)

**Tool: 1/64" flat end mill**  
Feed rate: 5.669 in/min (144 mm/min)  
Plunge rate: 0.472 in/min (12 mm/min)  
Spindle speed: 12,000 RPM  
Max pass depth: 0.002" (0.05 mm)

**Tool: 1mm flat end mill**  
Feed rate: 14.173 in/min (360 mm/min)  
Plunge rate: 1.81 in/min (30 mm/min)  
Spindle speed: 12,000 RPM  
Max pass depth: 0.0055" (0.14 mm)

%%

## Reflection

#### Content 
These weeks we discussed electrical safety, power supplies, current measurement, LEDs, LED arrays, displays, video, audio, solenoids, motor drivers, servos, BLDC motors, stepper motors, solid state relays, piezoelectric elements, artificial muscles, pneumatics, hydraulics, switches, hall effect sensors, potentiometers, step-response, temperature sensors, light sensors, motion sensors, distance sensors, GPS, accelerometers, gyroscopes, magnetometers, microphones, force sensors, encoders, pressure sensors, heart pulse sensors, air pollution sensors, gas sensors, and cameras, among other things.

#### Feelings
These weeks I felt stressed, and exhausted after class. I am trying to get used to it I guess.

#### Learnings
These weeks I learned about the step-response sensing technique. I used something similar in the past, where I did capacitive pressure sensing, but this is a more general and extensible technique. 

#### Inspiration
I am looking forward to playing around more with the step-response sensing technique. I'd also like to play around with making tubular linear motor.

#### Notable references
- [Abstracted event sensing](https://youtu.be/aqbKrrru2co) 
- [Radio tracking through walls](https://www.youtube.com/watch?v=HgDdaMy8KNE)
- [Transistor type selection](https://www.allaboutcircuits.com/technical-articles/fet-vs-bjt-vs-igbt-whats-the-right-choice-for-your-power-stage-design/)
- [Dual core Arduino](https://docs.arduino.cc/tutorials/portenta-h7/por-ard-dcp) 
- [Tubular linear motor](https://www.youtube.com/watch?v=w6EEN4FDcuU)