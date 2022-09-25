---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 14 · Networking and Communications|Last week]] - [[Week 16 · Wildcard Week|Next week]]_

_From [[MDEF Academy 2]] during [[Micro Challenge 3]]_

| Day                         | Description                           |
|:--------------------------- |:------------------------------------- |
| [[2022-05-04\|04/05]] · Wed | Interface and Application Programming | 

## Links
- [Local reference: Interface and application programming](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week12/)
- [Global reference: Interface and application programming](http://academy.cba.mit.edu/classes/interface_application_programming/index.html)
- [Global recording: Interface and application programming](https://vimeo.com/706238356)

---

## Assignment
> [Week 15 · Interface and Application Programming](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week-15-interface-application-programming)
> - Code/program an interface with the tools provided during the ( processing,P5JS, MitAppInventor,Aframe,NodeRed) or other alternatives software that interfaces a user with an input and/or output device that you want to use.
> - Interpret and implement design and programming protocols to create a Graphic User Interface (GUI).


I made a needle gauge in Processing that displays the analog value from the potentiometer from the Arduino. When the needle gauge approaches the redline, it sends brightness information to the Arduino to light the LED.

![[20220910_104406.mp4]]

Arduino code:

``` Arduino

void setup(){
  Serial.begin(9600);
}

void loop(){
  Serial.write(char(map(analogRead(A7),0,1023,0,255)));
  if(Serial.available()>0){
    analogWrite(3,Serial.read());
  }
  delay(50);
}

```

Processing code:

``` Processing

import processing.serial.*;

Serial myPort;
int value=0;
float scale=2;

void setup(){
  size(1600, 850);
  colorMode(HSB);
  myPort = new Serial(this, "COM9", 9600);
}

void draw(){
  background(255/2);
  if (myPort.available() > 0) {
    value = myPort.readChar() & 0xff;
    byte output = byte(int(calculateOverdrive(value,255))& 0xff);
    myPort.write(output);
  }  
  println(value);
  translate(width/2,height/2);
  scale(scale);
  pushMatrix();
  rotate(radians(-45));
  renderRedline();
  stroke(0);
  strokeWeight(3.5);
  renderTics(8,10);
  strokeWeight(2);
  renderTics(32,5);
  strokeWeight(1);
  renderTics(128,2);
  rotate(radians(map(value,0,256,0,270)));
  stroke(0,255,255);
  line(-200,0,0,0);
  popMatrix();
  pushMatrix();
  translate(0,height/(5*scale));
  textAlign(CENTER,TOP);
  textSize(44);
  fill(0,calculateOverdrive(value,256),map(calculateOverdrive(value,256),0,255,255*0.15,255*0.45));
  text(value,0,0);
  popMatrix();
  rotate(radians(-45));
  renderOutline();
}

void renderTics(float divisions, int size){
  float angle=270/divisions;
  for(int i=0; angle*i<=270; i++){
    pushMatrix();
    rotate(radians(angle*i));
    stroke(0,calculateOverdrive(angle*i,270),map(calculateOverdrive(angle*i,270),0,255,255*0.15,255*0.45));
    line(-200,0,-200+size,0);
    popMatrix();
  }
}

void renderOutline(){
  strokeWeight(3);
  for(float i=0; i<=270; i=i+0.05){
    pushMatrix();
    rotate(radians(i));
    stroke(0,calculateOverdrive(i,270),map(calculateOverdrive(i,270),0,255,255*0.15,255*0.45));
    point(-202,0);
    popMatrix();
  }
}

void renderRedline(){
  strokeWeight(.05);
  for(float i=0; i<=270; i=i+0.05){
    pushMatrix();
    rotate(radians(i));
    stroke(0,calculateOverdrive(i,270),map(calculateOverdrive(i,270),0,255,255/2,255));
    line(-200,0,-200+12,0);
    popMatrix();
  }
}


float calculateOverdrive(float number,int range){
  return constrain(map(number,range*0.625,range*0.875,0,range),0,range);
}


```

## Reflection

#### Content 
This week we discussed programming languages, device interfaces, data interfaces, user interfaces, graphics, audio, video, extended reality, math, machine learning, performance, deployment, and security, among other things.

#### Feelings
This week I felt disappointed about policy as usual and perhaps slightly optimistic that I am putting a plan together to be able to graduate. 

#### Learnings
This week I learned that Java doesn't have unsigned primitive datatypes. I had to add a conversion step when receiving from or sending to the Arduino. 

#### Inspiration
I am looking forward to using WebGPU in Rust and compiling to WebAssembly to run high performance applications in the web browser.

#### Notable references
- [Unsigned bytes in java](https://mkyong.com/java/java-convert-bytes-to-unsigned-bytes)
- [WebGPU in Rust](https://wgpu.rs/)