---
작성일자: 2016년 5월 19일 목요일  

---

# Puzzle 03 - Photocell (조도센서)

## 소스코드

아두이노는 컴퓨터(호스트) 사이에 시리얼 통신을 지원한다.  
시리얼(직렬) 통신은 한 데이터 뭉치를 소량의 데이터로 나눠서 주고받는 통신 방법이고, 패러럴(병렬) 통신은 한 번에 대량의 데이터를 주고받는 통신 방법이다. 필자가 아는 한 아두이노는 패러럴 통신은 지원하지 않는다.

`Serial.begin()`, `Serial.println()` 함수는 시리얼 통신을 가능하게 하는 함수이다. `Serial.begin()` 함수는 `baudrate`을 매개변수로 받아서 아두이노가 얼마나 따른 속도로 시리얼 통신을 시작할 지를 설정한다. `Serial.println()`은 시리얼 콘솔 창에 문자열이나 값을 출력할 때 사용하는 함수이다.

```
int potpin = 0; //set analog interface #0 to connect photocell 
int ledpin=13;int val = 0; //define variable val
void setup() {    pinMode(ledpin, OUTPUT); //set digital interface #11 as output
    Serial.begin(9600);//set baud rate as 9600}
void loop() {    val = analogRead(potpin); //read analog 
    Serial.println(val);    delay(10);//delay 0.01 s}
```
