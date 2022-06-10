<h1>06-10</h1>

<h3>🧐클래스</h3>

```java
class Car{
    String color;                                   // 필드 생성        
    int speed;                                      // 필드 생성        
    
    void upSpeed(int value){                        // upSpeed 메소드
        speed = speed + value;
    }
    void downSpeed(int value){                      // downSpeed 메소드
        speed = speed-value;
    }
}
public class Main2 {
    public static void main(String[] args) {
        Car mycar1 = new Car();                     // 객체1 생성
        Car mycar2 = new Car();                     // 객체2 생성
        Car mycar3 = new Car();                     // 객체3 생성

        mycar1.color = "Black";                     // 필드 사용
        mycar2.color = "Red";                       // 필드 사용
        mycar3.color = "white";                     // 필드 사용

        mycar1.speed = 30;                          // 필드 사용
        mycar2.speed = 60;                          // 필드 사용    
        mycar3.speed = 90;                          // 필드 사용

        mycar1.upSpeed(30);                   // upSpeed 메소드 사용
        mycar2.downSpeed(20);                 // downSpeed 메소드 사용  
        mycar3.upSpeed(50);                   // upSpeed 메소드 사용

        System.out.println("색상 : " + mycar1.color + "\n" + "속도 : " + mycar1.speed + "\n");  // 출력
        System.out.println("색상 : " + mycar2.color + "\n" + "속도 : " + mycar2.speed + "\n");  // 출력      
        System.out.println("색상 : " + mycar3.color + "\n" + "속도 : " + mycar3.speed + "\n");  // 출력
    }


}
```



## 🤔Car class

<code>String color;</code> 

<code>int speed;</code>

- 필드 생성



```java
void upSpeed(int value){
    speed = speed + value;
}
void downSpeed(int value){
    speed = speed-value;
}
```

- upSpeed 메소드 생성

속도 증가!

- downSpeed 메소드 생성

속도 감소!



## 😋Main class

```java
Car mycar1 = new Car();
Car mycar2 = new Car();
Car mycar3 = new Car();
```

- 객체 생성



```java
mycar1.color = "Black";
mycar2.color = "Red";                       
mycar3.color = "white";
```

-  Carclass 에서 선언한 필드를 사용



```java
mycar1.speed = 30;                          
mycar2.speed = 60;    
mycar3.speed = 90;
```

- 필드값 변경



```java
mycar1.upSpeed(30);                   
mycar2.downSpeed(20);                
mycar3.upSpeed(50);
```



- 메소드 사용





# 06-10

### 😚Getter setter

#### 필드를 직접적으로 변경하면 오류가 생길 수 있다.

- private 사용시 외부 클래스에서의 접근과 필드의 직접적인 접근을 막는다.



### 😥Getter

<b> return 을 통해 값을 반환 </b>



### 😥Setter

<b> 필드를 간접적으로 수정 </b>





```java
class Car{
    private String color;                           // color field
    private int speed;                              // speed field

void upSpeed(int value){                            // upSpeed method
        speed = speed + value;
    }

void downSpeed(int value){
        speed = speed - value;
}

    String getcolor(){                              // color getter
        return color;
    }

    int getSpeed(){                                 // speed getter
        return speed;
    }

    void setColor(String color){                    // color setter
        this.color = color;
    }

    void setSpeed(int speed){                       // speed setter
        this.speed = speed;
    }
}


public class Main3 {                                // Main class
    public static void main(String[] args) {        // Main method
        Car myCar1 = new Car();                     // new Car1
        Car myCar2 = new Car();                     // new Car2

        myCar1.setColor("빨강");                     // myCar1 color field setter
        myCar1.setSpeed(30);                        // myCar1 speed field setter

        myCar2.setColor("파랑");                     // myCar2 color field setter
        myCar2.setSpeed(80);                        // myCar2 speed field setter        

        myCar1.upSpeed(30);                         // myCar1 upSpeed method
        myCar2.downSpeed(10);                       // myCar2 downSpeed method

        System.out.println("자동차1의 색상 " + myCar1.getcolor() + "현재속도는 " + myCar1.getSpeed() + "km 입니다.");  // myCar1 color getter speed getter
        System.out.println("자동차2의 색상 " + myCar2.getcolor() + "현재속도는 " + myCar2.getSpeed() + "km 입니다.");  // myCar2 color getter speed getter
    }
}
```
