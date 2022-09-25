---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 4 · Electronics Production|Last week]] - [[Week 6 · Electronics Design|Next week]]_

_From [[MDEF Academy 1]]_

| Day                         | Description              |
|:--------------------------- |:------------------------ |
| [[2022-02-23\|23/02]] · Wed | 3D Printing and Scanning | 

## Links
- [Local reference: 3D printing and scanning](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week05/)
- [Local recording: 3D printing and scanning overview](https://www.youtube.com/watch?v=ZfrgBuCVfgo)
- [Local recording: 3D Printing paste and photogrammetry](https://www.youtube.com/watch?v=T4qJKZOWU8o)
- [Local recording: Firefly for grasshopper](https://www.youtube.com/watch?v=WFQLSY9NmDg)
- [Global reference: 3D printing and scanning](http://academy.cba.mit.edu/classes/scanning_printing/index.html)
- [Global recording: 3D printing and scanning](https://vimeo.com/681665210)

---

## Assignment
> [Week 5 · 3D Printing and Scanning](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-5-3d-printing-scanning)
> - 3D print an object **you have modelled** (not something you have downloaded) that could only be made with Additive manufacturing techniques
> - Your 3d printed object **cannot be bigger than 70x70x70mm or take more than 3 hours**

I designed a cube in Onshape where each face has a hole in its center that goes to the parallel face's hole, but the holes from orthogonal faces are separated and do not interfere with each other. The design has inaccessible curved internal geometry that is incompatible with subtractive techniques but can be manufactured additively.

Before boolean subtraction:

![[Pasted image 20220820200811.png]]

After subtraction with section view:

![[Pasted image 20220820200603.png]]

Printing:

![[20220820_225954.jpg]]

Complete:

![[20220831_203521.jpg]]

## Reflection

#### Content 
This week we discussed 3d printing and 3d scanning: constraints, materials, processes, machines, file formats, and software, among other things.

#### Feelings
This week I felt a bit better because I found something external that I resonated with but things were still frustrating. I was genuinely impressed with the paste 3d printer end effector and software toolchain that [[Eduardo Chamorro|Eduardo]] developed, and was equally as confused when he said he had not documented it online for people to reproduce.

#### Learnings
This week I learned that grasshopper can be used to define the toolpath directly. This is in contrast to designing the model and having a separate slicer software generate the toolpath. There is significant potential benefit from this approach because you have full control over the G-code, similar to the FullControl G-code designer Excel/VBA project. 

With Firefly in Grasshopper, you can do real-time sensing and control, which is pretty powerful- you could basically code a robot in Grasshopper, although I'm sure performance issues would significantly effect things as the project gets bigger.

#### Inspiration
I am looking forward to testing out the new python FullControl G-code designer when it comes out. 

Neural Radiance Fields (NeRF) are a sort of new take on photogrammetry that is quite exciting. I'd love to someday have view synthesis playback of what is going on at the end effector during digital manufacturing. It would be a great way to debug during the development of novel path planning algorithms or geometry that is difficult to manufacture.

#### Notable references
- [FullControl G-code designer](https://fullcontrolgcode.com/)
- [Firefly for Grasshopper](https://www.food4rhino.com/en/app/firefly)
- [Neural Radiance Fields](https://www.matthewtancik.com/nerf)