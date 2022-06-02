<b>05/25</b>

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



<b>05-30</b>

😃<b>str.Length()</b>

<b>문자열의 길이를 받아온다.</b>

<code>b = a.length();</code>



✔<b>str.charAt(i)</b>

<b>C언어에서의 문자 배열과 같다.</b>

<code>System.out.printf("%c", a.charAt(i));</code>



<b>06-02</b>



<b>🧵str.startsWith()</b>

<b>문자열의 처음이 특정 문자열인지 확인</b>

```
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

 <b>⛑str.endsWith()</b>

<b>문자열의 끝이 특정 문자열인지 확인</b>



<b>🎑str.indexOf()</b>

<b>특정 문자열의 위치를 앞에서부터 찾는다</b>

```
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.nextLine();
    System.out.println(a.indexOf("DMS"));
    System.out.println(a.lastIndexOf("DMS"));
}
```



<b>🖼str.lastIndexOf()</b>

<b>특정 문자열의 위치를 뒤에서부터 찾는다</b>



<b>🎫str.replace()</b>

<b>특정 문자열을 바꿔준다</b>

```
public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String str = sc.nextLine();
    String str_1 = str.replace("김은오", "정승훈");
    System.out.println(str_1);
}
```

