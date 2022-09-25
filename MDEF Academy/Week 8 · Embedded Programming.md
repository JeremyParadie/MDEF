---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 7 · Computer-Controlled Machining|Last week]] - [[Week 9 · Molding and Casting|Next week]]_

_From [[MDEF Academy 1]]_

| Day                         | Description          |
|:--------------------------- |:-------------------- |
| [[2022-03-16\|16/03]] · Wed | Embedded Programming | 

## Links
- [Local reference: Embedded programming](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week08/)
- [Global reference: Embedded programming](http://academy.cba.mit.edu/classes/embedded_programming/index.html)
- [Global recording: Embedded programming](https://vimeo.com/689983001)

---

## Assignment
> [Week 8 · Embedded Programming](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-8-embedded-programming)
> - Use your programmer ([HUZZAH32, ESP32 Feather](https://learn.adafruit.com/adafruit-huzzah32-esp32-feather)) to program a circuit with a “led and a button” to do something
> - **The circuit board, could be done as a shield, breadboard or vinyl cutter**


I made a circuit and programmed a microcontroller so that pressing the button does something- it toggles the state of the LED between off, dim, bright, and flashing. 

![[20220910_023430.mp4]]

Code:

``` Arduino

int buttonPin = 7;
int ledPin = 9;
int state = 0;
bool ledState = false;

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {
  if(digitalRead(buttonPin)==HIGH){
    delay(50);
    while(digitalRead(buttonPin)==HIGH){}
    state++;
  }
  if (state==0){
    digitalWrite(ledPin,LOW);
  }
  if (state==1){
    analogWrite(ledPin,32);
  }
  if (state==2){
    analogWrite(ledPin,255);
  }
  if (state==3){
    digitalWrite(ledPin,ledState);
    ledState=!ledState;
    delay(100);
  }
  if (state==4){
    state=0;
  }
}

```

## Reflection

#### Content 
This week we discussed computer architectures, memory, peripherals, vendors, packages, programmers, programming languages, integrated development environments, frameworks, boards, clocks, communication protocols, Microchip microcontroller families, interpreters, operating systems, system-on-chips, and debugging, among other things.

#### Feelings
This week I felt apathetic. I don't know.

#### Learnings
This week I learned that there are embeded GPU and multicore processors intended for artificial intelligence applications.

#### Inspiration
I am looking forward to next week. I have not done much with molding or casting in the past.

#### Notable references
- [Nvidia embedded GPU](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/)