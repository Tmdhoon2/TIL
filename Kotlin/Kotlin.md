<b>05/24</b>

<b>1.코틀린의 기본 함수 형식</b>

<code>fun add(a : Int, b : Int) : Int{    return a+b }</code>

<b>👍변수형을 변수 뒤에 쓴다!</b>



<b>2.문자열 출력</b>

<code>val name = "tmdhoon2"    println("my name is $name")</code>

<b>👌코틀린의 $가 C언어의 % 역할을 한다.</b>



<b>05-27</b>



<b>3. String Template</b>

<code>val name = "tmdhoon2"</code>

<code>val club = " DMS"</code>

<code>println("My name is ${name + club}")</code>

<code>println("Is this true or false 9==11? : ${9==11}")</code>

😒<b>문자열을 합칠때에는 연산자 + 로 합친다. ex) &{name + club} = tmdhoon2 DMS</b>



<b>4. 조건문</b>

<code>fun maxBy(a : Int, b : Int) : Int{</code>

<code>if(a>b){</code>

​       <code> return a    </code>

<code>}else {</code>

​        <code>return b    }</code>

 <code>}</code>

😢<b>변수 선언후에 변수형을 한번 더 선언해준다.. (그 외 if~, else if~ 문은 C언어와 동일)</b>



<b>05-29</b>



<b>5. when 문</b>

<b>when 문은 자바와 코틀린에서의 switch문과 같다.</b>

<code>when(score){</code>

<code>        in 90..100 -> println("Your are genius")</code>

<code>        in 10..80 -> println("not bad")</code>

<code>        else -> println("okay")</code>    

<code>}</code>

🤳 <b>90..100 은 90<=score<=100 일때 실행 된다.</b>



<b>6.Array and List</b>

<b>List : 읽기만</b>

<b>MutableList : 읽고 쓰기가 모두 가능</b>

<code>fun array(){</code>

<code>val array = arrayOf(1,2,3)</code>

<code>val list = listOf(1,2,3)</code>

<code>val array2 = arrayOf(1,"d",3.4f)</code>

<code>val list2 = listOf(1,"d",11L) </code>

<code>array[0] = 3    </code>

<code>var result = list.get(0)     </code>

<code>val arrayList = arrayListOf<Int>()</code>

<code>arrayList.add(10)</code>

<code>arrayList.add(20)</code>

<code>arrayList[0] = 20</code>

<code>}</code>

<b>🎶Array Lists 는 C언어의 배열과 같다.</b>
