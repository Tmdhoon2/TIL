# 06-11

### ๐ static

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
        System.out.println("ํ์ฌ ์์ฐ๋ ์๋์ฐจ ์ซ์ ==> " + myCar1.count);

        Car myCar2 = new Car();
        System.out.println("ํ์ฌ ์์ฐ๋ ์๋์ฐจ ์ซ์ ==> " + myCar2.count);

        Car myCar3 = new Car();
        System.out.println("ํ์ฌ ์์ฐ๋ ์๋์ฐจ ์ซ์ ==> " + myCar3.count);
    }
}
```





## ๐์์

#### ๐ฎ๊ธฐ์กด์ ํด๋์ค๊ฐ ๊ฐ์ง๊ณ  ์๋ ํ๋์ ๋ฉ์๋๋ฅผ ๊ทธ๋๋ก ๋ฌผ๋ ค๋ฐ์

```java
package com.example.javapractice;

class Car{                          // Car ํด๋์ค
    String color;                   // color ํ๋
    int speed;                      // speed ํ๋

    void upSpeed(int value){        // upSpeed ๋ฉ์๋
        speed = speed + value;
    }

    void downSpeed(int value){      // downSpeed ๋ฉ์๋
        speed = speed - value;
    }
}

class Sedan extends Car{            // Car ํด๋์ค๋ฅผ ์์๋ฐ๋ Sedan ํด๋์ค
    int seatNum;                    // ์ข์ ์

    int getSeatNum(){               // ์ข์ ์ getter
        return seatNum;             // ์ข์ ์ ๋ฐํ
    }
}

class Truck extends Car{            // Car ํด๋์ค๋ฅผ ์์๋ฐ๋ Truck ํด๋์ค
    int capacity;                   // ์ ์ฌ๋

    int getCapactiy(){              // ์ ์ฌ๋ getter
        return capacity;            // ์ ์ฌ๋ ๋ฐํ
    }
}

public class Main9 {                            // ๋ฉ์ธ ํด๋์ค
    public static void main(String[] args) {    // ๋ฉ์ธ ๋ฉ์๋
        Sedan sedan1 = new Sedan();             // ์น์ฉ์ฐจ ์ธ์คํด์ค
        Truck truck1 = new Truck();             // ํธ๋ญ ์ธ์คํด์ค

        sedan1.upSpeed(300);              // upSpeed ๋ฉ์๋ ํธ์ถ
        truck1.upSpeed(100);              // upSpeed ๋ฉ์๋ ํธ์ถ

        sedan1.seatNum = 5;                    // ์ข์ ์ ์ง์ 
        truck1.capacity = 50;                  // ์ ์ฌ๋ ์ง์ 

        System.out.println("์น์ฉ์ฐจ ์๋๋ " + sedan1.speed + "km, ์ข์์๋ " + sedan1.getSeatNum() + "๊ฐ ์๋๋ค");    // getter๋ก ์ถ๋ ฅ
        System.out.println("ํธ๋ญ ์๋๋ " + truck1.speed + "km, ์ ์ฌ๋์ " + truck1.getCapactiy() + "ํค ์๋๋ค");
    }
}
```





## ๐คฉclass Sedan extends Car

```java
class Sedan extends Car{            // Car ํด๋์ค๋ฅผ ์์๋ฐ๋ Sedan ํด๋์ค
    int seatNum;                    // ์ข์ ์

    int getSeatNum(){               // ์ข์ ์ getter
        return seatNum;             // ์ข์ ์ ๋ฐํ
    }
}
```

- extends ๋ฅผ ํตํด Car ํด๋์ค ์์
- getSeatNum ์ ํตํด ์ข์ ์ ๋ฐํ



## ๐คฉclass Truck extends Car

```java
class Truck extends Car{            // Car ํด๋์ค๋ฅผ ์์๋ฐ๋ Truck ํด๋์ค
    int capacity;                   // ์ ์ฌ๋

    int getCapactiy(){              // ์ ์ฌ๋ getter
        return capacity;            // ์ ์ฌ๋ ๋ฐํ
    }
}
```



- extends ๋ฅผ ํตํด Car ํด๋์ค ์์
- getCapacity ๋ฅผ ํตํด ์ ์ฌ๋ ๋ฐํ