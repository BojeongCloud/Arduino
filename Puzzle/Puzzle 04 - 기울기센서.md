---
작성일자: 2016년 5월 19일  


---

# Puzzle 04 기울기 센서

##
!


## 소스코드

```
int LED = 2; 
int tilt = 12; 

void setup()
{    pinMode(LED, OUTPUT); // set digital 2 for LED output    pinMode(tilt, INPUT); // set digital 12 for tilt sensing 
}
void loop(){ 
    if (digitalRead(tilt) == HIGH)    {        digitalWrite(LED, HIGH); //light up led    } 
    else//otherwise 
    {        digitalWrite(LED, LOW); //turn off led 
    }}
```