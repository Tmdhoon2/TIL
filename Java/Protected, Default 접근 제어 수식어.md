# 06-12

### ๐default ์ protected ์ ๊ทผ ์ ์ด ์์์ด







#### ์ ๊ทผ ์ ์ด ์์์ด		๊ฐ์ ํด๋์ค		๊ฐ์ ํจํค์ง		ํ์ ํด๋์ค	    ์ธ๋ถ ํด๋์ค

#### public					 	์ ๊ทผ O			 	์ ๊ทผ O	        	์ ๊ทผ O                ์ ๊ทผ O

#### protected			  	์ ๊ทผ O             	์ ๊ทผ O            	์ ๊ทผ O                ์ ๊ทผ X

#### default                   	์ ๊ทผ O             	์ ๊ทผ O            	์ ๊ทผ X                ์ ๊ทผ X

#### private                   	์ ๊ทผ O             	์ ๊ทผ X            	์ ๊ทผ X                 ์ ๊ทผ X		 



```java
class Car{                                                          // Car ์ํผํด๋์ค
    protected String color;                                         // ์ธ๋ถ ํด๋์ค์์ ์ ๊ทผ์ด ๋ถ๊ฐ๋ฅํ protected๋ก ํ๋ ์ง์ 
    int speed;
}

class Sedan extends Car{                                            // Car ํด๋์ค๋ฅผ ์์๋ฐ๋ Sedan ์๋ธํด๋์ค
    void setSpeed(int speed){                                       // speed Setter
        this.speed = speed;
    }

    void setColor(String color){                                    // color Setter
        this.color = color;
    }
}

public class Main1 {                                                // ๋ฉ์ธ ํด๋์ค
    public static void main(String[] args) {                        // ๋ฉ์ธ ๋ฉ์๋

        Sedan sedan1 = new Sedan();                                 // Sedan ์ธ์คํด์ค

        sedan1.setSpeed(300);                                       // ์๋ธ ํด๋์ค์ ๋ฉ์๋ ํธ์ถ
        sedan1.setColor("๋นจ๊ฐ");                                     // ์๋ธ ํด๋์ค์ ๋ฉ์๋ ํธ์ถ
        System.out.println("์น์ฉ์ฐจ ์๋ ==> " + sedan1.speed);        // ์์๋ฐ์ speed ํ๋์ ์ ๊ทผ
        System.out.println("์น์ฉ์ฐจ ์์ ==> " + sedan1.color);        // ์์๋ฐ์ color ํ๋์ ์ ๊ทผ
    }
}
```





<code>protected String color;</code>

- protected ๋ก ํ๋๋ฅผ ์ง์ ํจ์ผ๋ก์จ ์ธ๋ถ ํด๋์ค์ ์ ๊ทผ์ ๋ง์