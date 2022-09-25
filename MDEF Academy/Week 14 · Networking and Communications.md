---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 10-13 · Input and Output Devices|Last week]] - [[Week 15 · Interface and Application Programming|Next week]]_

_From [[MDEF Academy 2]]_

| Day                         | Description                   |
|:--------------------------- |:----------------------------- |
| [[2022-04-27\|27/04]] · Wed | Networking and Communications | 

## Links
- [Local reference: Networking and communications](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/networking/)
- [Local reference: Networking and communications introduction local class](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/networking/local/)
- [Local reference: Networking and wired communications local class](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/networking/wired/)
- [Local reference: Networking and wireless communications local class](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/networking/wireless/)
- [Local reference: How the internet works](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/networking/onions/)
- [Local reference: MQTT basics](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/networking/mqtt/)
- [Local reference: Networking and communications examples](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/extras/networking/examples/)
- [Global reference: Networking and communications](http://academy.cba.mit.edu/classes/networking_communications/index.html)
- [Global recording: Networking and communications](https://vimeo.com/703833815)

---

## Assignment
> [Week 14 · Networking and Communications](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-14-networking-and-communications)
> - Send a message between two microcontrollers (boards/ esp32 feathers or boards you made). The task could be done by pairs
> - Communication can be done by cable or wireless

I connected two Arduino Nanos together through SoftwareSerial on digital pins 2 and 3. They both ran the same code. They forward messages they receive on a serial port to the other serial port. Messages are sent from the computer through USB to a microcontroller, which forwards the message through the jumper wires with the SoftwareSerial library to the other microcontroller, which forwards the message through USB back to the computer. This works in either direction.

![[20220910_035635.jpg]]

![[2022-09-10 04-15-52.mp4]]

``` Arduino

#include <SoftwareSerial.h>

SoftwareSerial Serial1(3, 2);

void setup() {
  Serial.begin(9600);
  Serial1.begin(9600);
}

void loop() {
  if (Serial1.available() > 0) {
    char incomingByte = Serial1.read();
    Serial.print (incomingByte);
  }
 
  if (Serial.available() > 0) {
    char incomingByte = Serial.read();
    Serial1.write(incomingByte);
  }
}
  
```

## Reflection

#### Content 
This week we discussed reasons for communication, wired protocols, OSI layers, physical media, modulation, channel sharing, error management, networking protocols, and radios, among other things.

#### Feelings
This week I felt frustrated with the change in zoom and recording policy, as well as the lack of care for what is said in the lectures. It is misinformation at worst and misleading at best. For example, [[Eduardo Chamorro|Eduardo]] said that the reason why you have less Wi-Fi signal strength when you move away from the access point is because the air blocks the signal. This is simply false. It is because of the inverse square law. Atmospheric attenuation at 2.4GHz is negligible on the scale of kilometers. 

#### Learnings
This week I learned that ESP-NOW is a third option for wireless communication between ESP boards besides Wi-Fi and Bluetooth. It appears to function in a similar way to packet radios that I have used in the past.  

#### Inspiration
This week I was inspired to help other students with the assignment because they were overwhelmed and overcomplicating it.

#### Notable references
- [Getting started with ESP-NOW](https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/)