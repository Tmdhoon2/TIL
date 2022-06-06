# <b>05/25</b>

<b>1. 변수형의 크기 구하기</b>

<code>Byte.SIZE</code>

<b>2. Scanner 클래스 메서드</b>

<b>1) next() : 문자열 입력 (공백 X)</b>

<b>2) nextLine() : 문장 입력 (공백 O)</b>

<b>3) nextByte() : byte 형의 값 입력</b>

<b>4) nextInt() : int 형의 값 입력</b>

<b>5) nextBoolean() : boolean 형의 값 입력</b>

<b>6) nextShort() : short 형의 값 입력</b>

<b>7) nextLong() : long 형의 값 입력</b>

<b>8) nextFloat() : float 형의 값 입력</b>

<b>7) nextDouble() : double 형의 값 입력</b>



# <b>05-30</b>

### 😃<b>str.Length()</b>

<b>문자열의 길이를 받아온다.</b>

<code>b = a.length();</code>



### ✔<b>str.charAt(i)</b>

<b>C언어에서의 문자 배열과 같다.</b>

<code>System.out.printf("%c", a.charAt(i));</code>



# <b>06-02</b>



### <b>🧵str.startsWith()</b>											<b>⛑str.endsWith()</b>					

<b>문자열의 처음이 특정 문자열인지 확인</b>			                                          <b>문자열의 끝이 특정 문자열인지 확인</b>	

```java
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        if(!str.startsWith("(")){
            System.out.print("(");
        }
        System.out.print(str);
        if(!str.endsWith("(")){
            System.out.print(")");
        }
    }

}
```



### <b>🎑str.indexOf()</b>                                                    <b>🖼str.lastIndexOf()</b>

<b>특정 문자열의 위치를 앞에서부터 찾는다</b>			                                         <b>특정 문자열의 위치를 뒤에서부터 찾는다</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    System.out.println(a.indexOf("DMS"));
    System.out.println(a.lastIndexOf("DMS"));
}
```



### <b>🎫str.replace()</b>

<b>특정 문자열을 바꿔준다</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String str = sc.nextLine();
    String str_1 = str.replace("김은오", "정승훈");
    System.out.println(str_1);
}
```



### <b>🎡str.substring(a,b)</b>

<b>특정 문자열을 a부터b까지 추출하여 출력한다.</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    String b = a.substring(1,3);
    System.out.println(b);
}
```



### <b>🛒str.split(",")</b>

<b>문자열을 특정 문자 기준으로 분리한다.</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    String b[] = a.split("a");
    for(int i = 0; i<b.length; i++){
        System.out.println(b[i]);
    }
}
```



### <b>🥅str.toUpperCase()</b>

<b>문자를 대문자로 전환한다.</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    String b = a.toUpperCase();
    System.out.println(b);
}
```



### <b>💋str.toLowerCase()</b>

<b>문자를 소문자로 전환한다.</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    String b = a.toUpperCase();
    System.out.println(b);
}
```



# <b>06-03</b>



### <b>🛒str.trim()</b>

<b>문자열의 앞, 뒤 공백을 제거함</b>

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    System.out.println(a.trim());
}
```



# <b>06-05</b>



### 🐹<b>str.compareTo()								🐆str.contains()</b>								

<b>두 문자열 비교																		     문자열의 포함 확인 </b>																				

```java
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String first = "Hello my name is tmdhoon2";
    String second = "Hello my name is tmdhoon_2";
    System.out.println("문자열 1 ==> [" + first + "]");
    System.out.println("문자열 2 ==> [" + second + "]");

    System.out.println(first.compareTo(second));
    System.out.println(first.contains("tmdhoon"));
}
```



### <b>🐴str1==str2	</b>										🕸str1.equals(str2)					

<b>데이터 값, 저장된 위치 판별													    데이터의 값만 비교한다</b>	

```java
public static void main(String[] args) {
    String a = "Java Programming";
    String b = "Java Programming";
    String c = new String("Java Programming");

    System.out.println("원 문자열 1 ==> [" + a + "]");
    System.out.println("원 문자열 2 ==> [" + b + "]");
    System.out.println("원 문자열 3 ==> [" + c + "]\n");

    System.out.println("문자열 1 == 문자열 2 결과 : \t " + (a==b));
    System.out.println("문자열 1.equals(문자열 2) 결과 : " + a.equals(b));
    System.out.println("문자열 1 == 문자열 3 결과 : \t " + (a==c));
    System.out.println("문자열 1.equals(문자열 3) 결과 : " + a.equals(c));
}
```
