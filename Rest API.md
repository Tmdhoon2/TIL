# <b>Rest API</b>

## <b>Representational State Transfer API</b>



### 🥼<b>장점</b>

#### <b>1. 통합</b>

API는 새로운 애플리케이션을 기존 소프트웨어 시스템과 통합하는데 사용된다. 각 기능을 처음부터 작성할 필요가 없기 때문에 개발 속도가 빨라진다.



#### <b>2. 혁신</b>

기업은 신속하게 대응하고 혁신적인 서비스의 신속한 배포를 지원해야 한다. 전체 코드를 다시 작성 할 필요 없이 API 수준에서 변경하여 이를 수행할 수 있다.



#### <b>3. 확장</b>

API는 기업이 고객의 요구 사항을 충족할 수 있는 고유한 기회를 제공한다. 어느 기업이나 무료 또는 유료 API를 사용하여 내부 데이터베이스에 유사한 액세스 권한을 부여할 수 있다.



#### <b>4. 유지 관리의 용이성</b>

API는 두 시스템 간의 게이트웨이 역할을 하는데,  API가 영향을 받지 않도록 각 시스템은 내부적으로 변경해야 한다. -> 한 시스템의 향후 코드 변경이 다른 시스템에 영향을 미치지 않는다.



### 📍<b>주의</b>

#### <b>1. URI는 동사보다는 명사를, 대문자보다는 소문자를 사용</b>

<b>Bad Example</b> : http://khj93.com/Running/

<b>Good Example</b> :  http://khj93.com/run/



#### <b>2. 마지막에 슬래시를 포함하지 않는다</b>

<b>Bad Example</b> : http://tmdhoon2.com/test/

<b>Good Example</b> : http://tmdhoon2.com/test



#### <b>3. 언더바 대신 하이픈 사용</b>

<b>Bad Example</b> : http://tmdhoon2.com/test_blog

<b>Good Example</b> : http://tmdhoon2.com/test-blog



#### <b>4. 파일확장자는 URI에 포함하지 않는다</b>

<b>Bad Example</b> : http://tmdhoon2.com/photo.jpg

<b>Good Example</b> : http://tmdhoon2.com/photo



#### <b>5. 행위를 포함하지 않는다</b>

<b>Bad Example</b> : http://tmdhoon2.com/delete-post/1

<b>Good Example</b> : http://tmdhoon2.com/post/1