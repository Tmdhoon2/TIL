<h1>06-10</h1>

<h3>π§ν΄λμ€</h3>

```java
class Car{
    String color;                                   // νλ μμ±        
    int speed;                                      // νλ μμ±        
    
    void upSpeed(int value){                        // upSpeed λ©μλ
        speed = speed + value;
    }
    void downSpeed(int value){                      // downSpeed λ©μλ
        speed = speed-value;
    }
}
public class Main2 {
    public static void main(String[] args) {
        Car mycar1 = new Car();                     // κ°μ²΄1 μμ±
        Car mycar2 = new Car();                     // κ°μ²΄2 μμ±
        Car mycar3 = new Car();                     // κ°μ²΄3 μμ±

        mycar1.color = "Black";                     // νλ μ¬μ©
        mycar2.color = "Red";                       // νλ μ¬μ©
        mycar3.color = "white";                     // νλ μ¬μ©

        mycar1.speed = 30;                          // νλ μ¬μ©
        mycar2.speed = 60;                          // νλ μ¬μ©    
        mycar3.speed = 90;                          // νλ μ¬μ©

        mycar1.upSpeed(30);                   // upSpeed λ©μλ μ¬μ©
        mycar2.downSpeed(20);                 // downSpeed λ©μλ μ¬μ©  
        mycar3.upSpeed(50);                   // upSpeed λ©μλ μ¬μ©

        System.out.println("μμ : " + mycar1.color + "\n" + "μλ : " + mycar1.speed + "\n");  // μΆλ ₯
        System.out.println("μμ : " + mycar2.color + "\n" + "μλ : " + mycar2.speed + "\n");  // μΆλ ₯      
        System.out.println("μμ : " + mycar3.color + "\n" + "μλ : " + mycar3.speed + "\n");  // μΆλ ₯
    }


}
```



## π€Car class

<code>String color;</code> 

<code>int speed;</code>

- νλ μμ±



```java
void upSpeed(int value){
    speed = speed + value;
}
void downSpeed(int value){
    speed = speed-value;
}
```

- upSpeed λ©μλ μμ±

μλ μ¦κ°!

- downSpeed λ©μλ μμ±

μλ κ°μ!



## πMain class

```java
Car mycar1 = new Car();
Car mycar2 = new Car();
Car mycar3 = new Car();
```

- κ°μ²΄ μμ±



```java
mycar1.color = "Black";
mycar2.color = "Red";                       
mycar3.color = "white";
```

-  Carclass μμ μ μΈν νλλ₯Ό μ¬μ©



```java
mycar1.speed = 30;                          
mycar2.speed = 60;    
mycar3.speed = 90;
```

- νλκ° λ³κ²½



```java
mycar1.upSpeed(30);                   
mycar2.downSpeed(20);                
mycar3.upSpeed(50);
```



- λ©μλ μ¬μ©





# 06-10

### πGetter setter

#### νλλ₯Ό μ§μ μ μΌλ‘ λ³κ²½νλ©΄ μ€λ₯κ° μκΈΈ μ μλ€.

- private μ¬μ©μ μΈλΆ ν΄λμ€μμμ μ κ·Όκ³Ό νλμ μ§μ μ μΈ μ κ·Όμ λ§λλ€.



### π₯Getter

<b> return μ ν΅ν΄ κ°μ λ°ν </b>



### π₯Setter

<b> νλλ₯Ό κ°μ μ μΌλ‘ μμ  </b>





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

        myCar1.setColor("λΉ¨κ°");                     // myCar1 color field setter
        myCar1.setSpeed(30);                        // myCar1 speed field setter

        myCar2.setColor("νλ");                     // myCar2 color field setter
        myCar2.setSpeed(80);                        // myCar2 speed field setter        

        myCar1.upSpeed(30);                         // myCar1 upSpeed method
        myCar2.downSpeed(10);                       // myCar2 downSpeed method

        System.out.println("μλμ°¨1μ μμ " + myCar1.getcolor() + "νμ¬μλλ " + myCar1.getSpeed() + "km μλλ€.");  // myCar1 color getter speed getter
        System.out.println("μλμ°¨2μ μμ " + myCar2.getcolor() + "νμ¬μλλ " + myCar2.getSpeed() + "km μλλ€.");  // myCar2 color getter speed getter
    }
}
```
