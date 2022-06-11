# 06-11

### 😂 static

```java
class Car{
    String color;
    int speed;
    static int count = 0;

    Car(){
        count++;
    }
}

public class Main7 {
    public static void main(String[] args) {
        Car myCar1 = new Car();
        System.out.println("현재 생산된 자동차 숫자 ==> " + myCar1.count);

        Car myCar2 = new Car();
        System.out.println("현재 생산된 자동차 숫자 ==> " + myCar2.count);

        Car myCar3 = new Car();
        System.out.println("현재 생산된 자동차 숫자 ==> " + myCar3.count);
    }
}
```





## 😊상속

#### 😮기존의 클래스가 가지고 있는 필드와 메소드를 그대로 물려받음

```java
package com.example.javapractice;

class Car{                          // Car 클래스
    String color;                   // color 필드
    int speed;                      // speed 필드

    void upSpeed(int value){        // upSpeed 메서드
        speed = speed + value;
    }

    void downSpeed(int value){      // downSpeed 메서드
        speed = speed - value;
    }
}

class Sedan extends Car{            // Car 클래스를 상속받는 Sedan 클래스
    int seatNum;                    // 좌석 수

    int getSeatNum(){               // 좌석 수 getter
        return seatNum;             // 좌석 수 반환
    }
}

class Truck extends Car{            // Car 클래스를 상속받는 Truck 클래스
    int capacity;                   // 적재량

    int getCapactiy(){              // 적재량 getter
        return capacity;            // 적재량 반환
    }
}

public class Main9 {                            // 메인 클래스
    public static void main(String[] args) {    // 메인 메서드
        Sedan sedan1 = new Sedan();             // 승용차 인스턴스
        Truck truck1 = new Truck();             // 트럭 인스턴스

        sedan1.upSpeed(300);              // upSpeed 메서드 호출
        truck1.upSpeed(100);              // upSpeed 메서드 호출

        sedan1.seatNum = 5;                    // 좌석 수 지정
        truck1.capacity = 50;                  // 적재량 지정

        System.out.println("승용차 속도는 " + sedan1.speed + "km, 좌석수는 " + sedan1.getSeatNum() + "개 입니다");    // getter로 출력
        System.out.println("트럭 속도는 " + truck1.speed + "km, 적재량은 " + truck1.getCapactiy() + "톤 입니다");
    }
}
```





## 🤩class Sedan extends Car

```java
class Sedan extends Car{            // Car 클래스를 상속받는 Sedan 클래스
    int seatNum;                    // 좌석 수

    int getSeatNum(){               // 좌석 수 getter
        return seatNum;             // 좌석 수 반환
    }
}
```

- extends 를 통해 Car 클래스 상속
- getSeatNum 을 통해 좌석 수 반환



## 🤩class Truck extends Car

```java
class Truck extends Car{            // Car 클래스를 상속받는 Truck 클래스
    int capacity;                   // 적재량

    int getCapactiy(){              // 적재량 getter
        return capacity;            // 적재량 반환
    }
}
```



- extends 를 통해 Car 클래스 상속
- getCapacity 를 통해 적재량 반환