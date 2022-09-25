---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 6 · Electronics Design|Last week]] - [[Week 8 · Embedded Programming|Next week]]_

_From [[MDEF Academy 1]]_

| Day                         | Description                   |
|:--------------------------- |:----------------------------- |
| [[2022-03-09\|09/03]] · Wed | Computer-Controlled Machining | 

## Links
- [Local reference: Computer-controlled machining](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week07/)
- [Global reference: Computer-controlled machining](http://academy.cba.mit.edu/classes/computer_machining/index.html)
- [Global recording: Computer-controlled machining](https://vimeo.com/686741866)

---

## Assignment
> [Week 7 · Computer-Controlled Machining](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-7-computer-controlled-machining-cnc)
> - Design something big IN PAIRS! You can use up to a maximun of half full board (that means 1200x1200mm) of the available material per student. 15 mm thick pine plywood boards.
> - **You will cut your design with your teammate, so you will cut the whole panel at once.**

I adjusted my parametric design from [[Week 2 · Computer-Aided Design]] to be compatible with CNC machining by tweaking the parameters for the larger scale and adding dog bone features in the concave corners.



%%
Finalize design based on circuit board router dimensions and bit
Pick a milling bit
Figure out feeds and speeds

pass depth 1-2x bit diameter. so 0.25 depth per pass. yes, I should take two passes. 

110ipm

plunge/ramp down should be half of the feed rate

2x diameter depth of cut - reduce feed rate by 25%

machine absolute max feed rate 360ipm
machine spindle only 109W

10000rpm
80-120ipm

amazon listing says
18,000 rpm
0.004 chipload
100ipm 
0.25 depth of cut

https://www.amanatool.com/46180-cnc-solid-carbide-compression-spiral-1-8-dia-x-13-16-x-1-8-inch-shank.html

https://www.amanatool.com/pub/media/productattachments/Solid-Carbide-Compression-Spirals-v12.pdf

18,000 RPM
30ipm
0.25in depth of cut
.0011chip load per tooth
15ipm ramp down

To find RPM: (SFM x 3.82) / diameter of tool 
To find SFM: 0.262 x diameter of tool x RPM 
To find Feed Rate IPM: RPM x # of flutes x chip load 
To find Chip Load: Feed Rate IPM / (RPM x # of flutes) 
To find Ramp Down: Feed Rate IPM / # of flutes


%%

#MDEFTODO post picture of assembled plywood box and cad assembly and outline

## Reflection

#### Content
This week we discussed larger-scale projects, CNC router and milling machines, materials, suppliers, services, bits, parameters, lubrication, grinding/abrasives, fixturing, spoilboard, dust collection, flexures, fasteners, glues, joinery, toolpaths, CAM, file formats, and safety, among other things.

#### Feelings
This week I felt better. I learned some things.

#### Learnings
This week I spent a long time learning about feeds and speeds, trying to understand the mechanical dynamics and complexity of what is happening at the cutting head. There are a lot of parameters to tune and the stakes are high; the bits are easily damaged with the wrong settings and cost money. 

#### Inspiration
It would be really nice if there was a comprehensive parameters calculator that takes into account much more than just feeds and speeds like material, cutter geometry, spindle power, depth of cut, machine rigidity, etc. Maybe that could be a future project, characterizing all the parameters. 

#### Notable references
- [Japanese Wood Joints](https://www.thingiverse.com/thing:169723)