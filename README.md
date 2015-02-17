# Arduino-digital-7-segment-counter-0-99
Counts 0-99 automatically with adjustable speed using a potentiometer. 

<div style="float: right;" a href="http://s76.photobucket.com/user/mpgoat/media/246B046F-F788-4248-A1C1-8BF425F00787_zpsxfrjvwbm.jpg.html" target="_blank"><img HEIGHT="500" WIDTH="350" src="http://i76.photobucket.com/albums/j8/mpgoat/246B046F-F788-4248-A1C1-8BF425F00787_zpsxfrjvwbm.jpg" border="0" alt="Board-00- photo 246B046F-F788-4248-A1C1-8BF425F00787_zpsxfrjvwbm.jpg" style="float:left;" alt="" /></a> <img HEIGHT="500" WIDTH="350" src="http://i76.photobucket.com/albums/j8/mpgoat/CFE0E901-F36D-4BA5-B2EB-747B0E92F4C6_zpsg1iohxtw.jpg" border="0" alt="board-99- photo CFE0E901-F36D-4BA5-B2EB-747B0E92F4C6_zpsg1iohxtw.jpg" style="float:left;" alt="" /></a>

# Code-for-Arduino
```c
int count = 0; // counter
int speedPin = A5; // potentiometer 
int speedValue = 0; // 
```
void **setup**() {
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

void **loop**() {
```c
speedValue = analogRead(speedPin); 
  
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 1);  
 digitalWrite(4, 1);  
 digitalWrite(5, 1);  //  Display 0 in ones place
 digitalWrite(6, 1);
 digitalWrite(7, 1);
 digitalWrite(8, 0);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 0);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 1);
 digitalWrite(5, 0);  //  Display 1 in ones place
 digitalWrite(6, 0);
 digitalWrite(7, 0);
 digitalWrite(8, 0);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 0);
 digitalWrite(5, 1);  //  Display 2 in ones place
 digitalWrite(6, 1);
 digitalWrite(7, 0);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 1);
 digitalWrite(5, 1);  //  Display 3 in ones place
 digitalWrite(6, 0);
 digitalWrite(7, 0);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 0);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 1);
 digitalWrite(5, 0);  //  Display 4 in ones place
 digitalWrite(6, 0);
 digitalWrite(7, 1);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 0);
 digitalWrite(4, 1);
 digitalWrite(5, 1);  //  Display 5 in ones place
 digitalWrite(6, 0);
 digitalWrite(7, 1);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 0);
 digitalWrite(4, 1);
 digitalWrite(5, 1);  //  Display 6 in ones place
 digitalWrite(6, 1);
 digitalWrite(7, 1);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 1);
 digitalWrite(5, 0);  //  Display 7 in ones place
 digitalWrite(6, 0);
 digitalWrite(7, 0);
 digitalWrite(8, 0);  //-------------
 delay(speedValue);

 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 1);
 digitalWrite(5, 1);  //  Display 8 in ones place
 digitalWrite(6, 1);
 digitalWrite(7, 1);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
 
 digitalWrite(2, 1);  //-------------
 digitalWrite(3, 1);
 digitalWrite(4, 1);
 digitalWrite(5, 0);  //  Display 9 in ones place
 digitalWrite(6, 0);
 digitalWrite(7, 1);
 digitalWrite(8, 1);  //-------------
 delay(speedValue);
```
This keep count of the tens place.
```c
 count++;
 
 if (count == 1){      // When count is 1 it displays 1 in tens place
   digitalWrite(9, 1);
   digitalWrite(10, 1);
 }
 
 if (count == 2){      // When count is 2 it displays 2 in tens place
   digitalWrite(10, 0);
   digitalWrite(A0, 1);
   digitalWrite(A1, 1);
   digitalWrite(12, 1);
   digitalWrite(11, 1);
 }
  if (count == 3){      // When count is 3 it displays 3 in tens place
   digitalWrite(10, 1);
   digitalWrite(12, 0);
 }
  if (count == 4){      // When count is 4 it displays 4 in tens place
   digitalWrite(A0, 0);
   digitalWrite(11, 0);
   digitalWrite(13, 1);
 }
  if (count == 5){      // When count is 5 it displays 5 in tens place
   digitalWrite(9, 0);
   digitalWrite(A0, 1);
   digitalWrite(11, 1);
 }
  if (count == 6){      // When count is 6 it displays 6 in tens place
   digitalWrite(12, 1);
 }
  if (count == 7){      // When count is 7 it displays 7 in tens place
   digitalWrite(10, 1);
   digitalWrite(13, 0);
   digitalWrite(9, 1);
   digitalWrite(A1, 0);
   digitalWrite(12, 0);
   digitalWrite(11, 0);
 }
  if (count == 8){      // When count is 8 it displays 8 in tens place
   digitalWrite(A1, 1);
   digitalWrite(12, 1);
   digitalWrite(11, 1);
   digitalWrite(13, 1);
   digitalWrite(11, 1);
 }
  if (count == 9){      // When count is 9 it displays 9 in tens place
   digitalWrite(12, 0);
   digitalWrite(11, 0);
 }
 if (count == 10){      // When count is 10. tens place becomes blank
   digitalWrite(9, 0);
   digitalWrite(10, 0);
   digitalWrite(11, 0);
   digitalWrite(12, 0);
   digitalWrite(13, 0);
   digitalWrite(A0, 0);
   digitalWrite(A1, 0);
   count = 0;            // Reset count back to 0
   }
```
}



Copyright (c) 2015 Michael Parson

  This program is free software; you can redistribute it and/or
  modify it under the terms of the GNU General Public License as
  published by the Free Software Foundation; either version 2 of the
  License, or (at your option) any later version.  See the file
  COPYING included with this distribution for more information.

