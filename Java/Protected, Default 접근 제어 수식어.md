# 06-12

### 😆default 와 protected 접근 제어 수식어







#### 접근 제어 수식어		같은 클래스		같은 패키지		하위 클래스	    외부 클래스

#### public					 	접근 O			 	접근 O	        	접근 O                접근 O

#### protected			  	접근 O             	접근 O            	접근 O                접근 X

#### default                   	접근 O             	접근 O            	접근 X                접근 X

#### private                   	접근 O             	접근 X            	접근 X                 접근 X		 



```java
class Car{                                                          // Car 슈퍼클래스
    protected String color;                                         // 외부 클래스에서 접근이 불가능한 protected로 필드 지정
    int speed;
}

class Sedan extends Car{                                            // Car 클래스를 상속받는 Sedan 서브클래스
    void setSpeed(int speed){                                       // speed Setter
        this.speed = speed;
    }

    void setColor(String color){                                    // color Setter
        this.color = color;
    }
}

public class Main1 {                                                // 메인 클래스
    public static void main(String[] args) {                        // 메인 메서드

        Sedan sedan1 = new Sedan();                                 // Sedan 인스턴스

        sedan1.setSpeed(300);                                       // 서브 클래스의 메서드 호출
        sedan1.setColor("빨강");                                     // 서브 클래스의 메서드 호출
        System.out.println("승용차 속도 ==> " + sedan1.speed);        // 상속받은 speed 필드에 접근
        System.out.println("승용차 색상 ==> " + sedan1.color);        // 상속받은 color 필드에 접근
    }
}
```





<code>protected String color;</code>

- protected 로 필드를 지정함으로써 외부 클래스의 접근을 막음