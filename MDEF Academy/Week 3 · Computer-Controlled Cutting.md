---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 2 · Computer-Aided Design|Last week]] - [[Week 4 · Electronics Production|Next week]]_

_From [[MDEF Academy 1]]_

| Day                         | Description                 |
|:--------------------------- |:--------------------------- |
| [[2022-02-09\|09/02]] · Wed | Computer-Controlled Cutting | 

## Links
- [Local reference: Computer-controlled cutting](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week03/)
- [Local recording: Computer-controlled cutting overview](https://www.youtube.com/watch?v=4_IVxQ89wnA)
- [Local recording: MDEF review + Parametric class](https://www.youtube.com/watch?v=rV26JKDbYvo)
- [Local recording: Rhino tips for laser cutting](https://www.youtube.com/watch?v=bSoLYqWG738)
- [Global reference: Computer-controlled cutting](http://academy.cba.mit.edu/classes/computer_cutting/index.html)
- [Global recording: Computer-controlled cutting](https://vimeo.com/675651241)

---

## Assignment
> [Week 3 · Computer-Controlled Cutting](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-3-computer-controlled-cutting)
> - Create a small object using parametric design tools. The object should be assembled in a press-fit way (no use of glue, screws etc).
> - Complete the [Machine test](https://docs.google.com/forms/d/e/1FAIpQLScgRrkBb5JOtW_vhQUCHzT6of2vkIXgqccfY8HtWmpQAJoiZA/viewform) with the **100%** of the score

I completed the machine test google form.

I created a parametric design using Onshape. 

![[parametric.mp4]]

Six copies of the same part are used to assemble the object. This is the full assembly.

![[Pasted image 20220829140101.png]]

I incorporated parametric kerf compensation to help with adjusting to get a good press-fit.

![[Pasted image 20220829140232.png]]

Laser bed layout:

![[laser_bed.svg]]

Final assembled object:

![[20220909_210538.jpg]]

## Reflection

#### Content 
This week we discussed laser cutting and vinyl cutting: tools, CAD, CAM, applications, materials, and settings, among other things.

#### Feelings
This week I felt bored and frustrated. Bored because I've done this stuff before, and frustrated because I find the policies to be alienating and counter to the spirit of the course.

#### Learnings
This week I learned that finger-jointed cube faces can all be identical geometry and still assemble correctly, even with all faces pointing out. Of course, the corners are void if the model is restricted to a single profile extrusion, but I consider that to be acceptable given the restriction. 

I learned that you can add masking tape to the surface of MDF when cutting it on the laser to prevent the final piece from getting scorch marks. The tape and scorch marks can easily be peeled off.

I also learned that intentionally defocusing the laser cutter can be used to apply heat to an acrylic workpiece which can selectively melt it, which, if unsupported, can bend due to gravity. 

#### Inspiration
I am looking forward to experimenting with flexures. They are a potentially inexpensive way to get precision linear motion.

#### Notable references
- [LaserOrigami video](https://youtu.be/arjRtCjI9AQ)
- [Synthesis and analysis of parallel kinematic XY flexure mechanisms thesis](https://academy.cba.mit.edu/classes/computer_cutting/56836505.pdf)