# Arduino-digital-7-segment-counter-0-99
Counts 0-99 automatically with adjustable speed using a potentiometer. 

<div style="float: right;" a href="http://s76.photobucket.com/user/mpgoat/media/246B046F-F788-4248-A1C1-8BF425F00787_zpsxfrjvwbm.jpg.html" target="_blank"><img HEIGHT="500" WIDTH="350" src="http://i76.photobucket.com/albums/j8/mpgoat/246B046F-F788-4248-A1C1-8BF425F00787_zpsxfrjvwbm.jpg" border="0" alt="Board-00- photo 246B046F-F788-4248-A1C1-8BF425F00787_zpsxfrjvwbm.jpg" style="float:left;" alt="" /></a> <img HEIGHT="500" WIDTH="350" src="http://i76.photobucket.com/albums/j8/mpgoat/CFE0E901-F36D-4BA5-B2EB-747B0E92F4C6_zpsg1iohxtw.jpg" border="0" alt="board-99- photo CFE0E901-F36D-4BA5-B2EB-747B0E92F4C6_zpsg1iohxtw.jpg" style="float:left;" alt="" /></a>

# Code-for-Arduino
```c
int count = 0; // counter
int speedPin = A5; // potentiometer 
int speedValue = 0; // 
```
void *setup*() {
```c
//The individual segments of a 2 digit seven-segment display.
// 1 being the first digit 2 being the second digit
  pinMode(2, OUTPUT);  //A1
  pinMode(3, OUTPUT);  //B1
  pinMode(4, OUTPUT);  //C1
  pinMode(5, OUTPUT);  //D1
  pinMode(6, OUTPUT);  //E1
  pinMode(7, OUTPUT);  //F1
  pinMode(8, OUTPUT);  //G1
  pinMode(9, OUTPUT);  //B2
  pinMode(10, OUTPUT);  //C2
  pinMode(11, OUTPUT);  //D2
  pinMode(12, OUTPUT);  //E2
  pinMode(13, OUTPUT);  //F2
  pinMode(A0, OUTPUT);  //A2
  pinMode(A1, OUTPUT);  //G2
```
}



Copyright (c) 2015 Michael Parson

  This program is free software; you can redistribute it and/or
  modify it under the terms of the GNU General Public License as
  published by the Free Software Foundation; either version 2 of the
  License, or (at your option) any later version.  See the file
  COPYING included with this distribution for more information.

