---
작성일자: 2016년 8월 4일 목요일

---

# Puzzle 06 7-Segment FND

## 한 자리 FND 제어

### 회로도
키트 구성품 18번(74HC595 Shift Register)과 19번(한 자리 FND 소자)을 사용한다.

#### 7 - Segment FND
![애노드와 캐소드 소자의 차이점]
(http://cfile8.uf.tistory.com/image/191466494ED872E502BF8A)

FND는 크게 두 가지 종류로 나눌 수 있는데,  
우리가 사용하는 소자는 common-cathod type 이다.

#### 74HC595 Shift Register
![74HC595 - Serial to Parallel Shift Register]
(./images/06_74HC595_Pinning.tiff)

![Pin Description](./images/06_74HC595_Pin_Description.tiff)

![Function Table]
(./images/06_74HC595_Function.tiff)

소자에 파여있는 홈으로 상하를 구분할 수 있다.  
그리고 핀 배치도와 설명은 위 그림과 같다.


##### `OE'` (Output Enable)  

| 입력 | 설명      |
| :--  | :--       |
| LOW  | 출력 허용 |
| HIGH | 출력 제한 |

##### `MR'` (Master Reset)

| 입력 | 설명                        |
| :--  | :--                         |
| LOW  | 소자를 초기 상태로 되돌린다 |
| HIGH | 소자의 현 상태를 유지한다   |

##### `SHCP` (Shift Register Clock Input)


##### `STCP` (Storage Register Clock Input)


### 소스코드

```
int latchPin = 11; 
int clockPin = 12;
int  dataPin = 10; 

// 좌측부터 DP, G, F ... B, A
    0b00000110, 
    0b01011011, 
    0b01001111, 
    0b01100110, 
    0b01101101, 
    0b01111100, 
    0b00000111,
    0b01111111, 
    0b01100111
};

    pinMode(latchPin, OUTPUT);

        // take the latchPin low so the LEDs don't change 
        // while you're sending in bits: 
        digitalWrite(latchPin, LOW); 
        
        // shift out the bits:
        
        //take the latch pin high so the LEDs will light up:
        
        // pause before next value: 
        delay(300);
}
```

## 4자리 FND 제어

### 회로도

### 소스코드

다소 길다. 하지만 길기만 할 뿐, 전혀 이해하기 어렵지 않다.

```
//set the cathode interface 
int a = 1;

int d4 = 9;

//set variable

//fine-tuning value for clock
    pinMode(d2, OUTPUT); 
    pinMode(d3, OUTPUT); 
    pinMode(d4, OUTPUT); 
    pinMode(a, OUTPUT); 
    pinMode(b, OUTPUT); 
    pinMode(c, OUTPUT); 
    pinMode(d, OUTPUT); 
    pinMode(e, OUTPUT); 
    pinMode(f, OUTPUT); 
    pinMode(g, OUTPUT); 
    pinMode(p, OUTPUT);

    delayMicroseconds(del); 
    
    clearLEDs();
    delayMicroseconds(del); 
    
    clearLEDs();
    delayMicroseconds(del); 
    
    clearLEDs();
    delayMicroseconds(del);
    
    }
}

//define pickDigit(x),to open dx port
    digitalWrite(d2, HIGH); 
    digitalWrite(d3, HIGH);
    digitalWrite(d4, HIGH); 
    
    switch (x) {
            break;
            break;
            break;
            break;
}
        default:
        case 1: 
            one();
        case 2: 
            two();
        case 3:
        case 4:
        case 5:
        case 6: 
            six();
        case 7:
        case 8:
            break; 
        case 9:
    }

//set to start the decimal point
}

//clear contents 
    digitalWrite(b, LOW); 
    digitalWrite(c, LOW); 
    digitalWrite(d, LOW); 
    digitalWrite(e, LOW); 
    digitalWrite(f, LOW); 
    digitalWrite(g, LOW); 
    digitalWrite(p, LOW);

// 이하 함수는 FND 소자에서 특정 숫자를 표시하기 위해
// 각 핀에 입력하는 값을 설정해놓았다.

//define 0 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, HIGH); 
    digitalWrite(f, HIGH); 
    digitalWrite(g, LOW );

// define 1 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, LOW ); 
    digitalWrite(e, LOW ); 
    digitalWrite(f, LOW ); 
    digitalWrite(g, LOW );

// define 2 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, LOW ); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, HIGH); 
    digitalWrite(f, LOW ); 
    digitalWrite(g, HIGH);

}

// define 3 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, LOW ); 
    digitalWrite(f, LOW ); 
    digitalWrite(g, HIGH);

// define 4 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, LOW ); 
    digitalWrite(e, LOW ); 
    digitalWrite(f, HIGH); 
    digitalWrite(g, HIGH);

// define 5 as cathode pin switch
    digitalWrite(b, LOW ); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, LOW ); 
    digitalWrite(f, HIGH); 
    digitalWrite(g, HIGH);

// define 6 as cathode pin switch
    digitalWrite(b, LOW ); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, HIGH); 
    digitalWrite(f, HIGH); 
    digitalWrite(g, HIGH);

// define 7 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, low ); 
    digitalWrite(e, LOW ); 
    digitalWrite(f, LOW );
    digitalWrite(g, LOW ); 
}

// define 8 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, HIGH); 
    digitalWrite(f, HIGH); 
    digitalWrite(g, HIGH);

// define 9 as cathode pin switch
    digitalWrite(b, HIGH); 
    digitalWrite(c, HIGH); 
    digitalWrite(d, HIGH); 
    digitalWrite(e, LOW ); 
    digitalWrite(f, HIGH); 
    digitalWrite(g, HIGH);
```