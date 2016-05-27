---
작성일자: 2016년 5월 19일 목요일  


---


# Puzzle 02 - Traffic Light

![Schematic](./images/02_Traffic_Light_schem.ps.png)

## 소스코드

`delay()` 함수는 밀리세컨드를 단위로 매개변수로 받아서 매개변수의 값 만큼 아무 동작도 수행하지 않고 기다리게 한다.

```
int REDpin = 6;int YELLOWpin = 5; 
int GREENpin = 4; 

void setup() {    pinMode(REDpin, OUTPUT); 
    pinMode(YELLOWpin, OUTPUT); pinMode(GREENpin, OUTPUT);}
void loop() {    digitalWrite(REDpin, HIGH); 
    delay(5000);
        digitalWrite(REDpin, LOW); 
    digitalWrite(YELLOWpin, HIGH); 
    delay(1000);
    
    digitalWrite(YELLOWpin, LOW); 
    digitalWrite(GREENpin, HIGH); 
    delay(5000);
    
    digitalWrite(GREENpin, LOW);}
```
