# Inside_JS

<h4>자바스크립트 데이터 타입과 연산자</h4>

<h5>(1)기본타입 {숫자,문자열,불린값,undifined, null}</h5>
<h5>(2)참조타입_객체{배열,함수,정규표현식}</h5>
<h5>(3)주요 연산자</h5>

<p>자바스크립트는 <b>느슨한 타입 체크언어</b>다. C언어가 변수를 선언할때 변수타입을 정의하는것과는 다르게
var 라는 하나의 키워드로 변수를 선언하고, 이렇게 선언된 변수에 어떤 타입의 데이터라도 저장하는 것이 가능하다.</p>

```
  var intNum = 0;
  var floatNum = 0.1;
  var singleQuoteStr = 'single quote str';
  var doubleQuoteStr = 'double quote str';
  var singleChar = 'a';
  var boolean = true;
  var emptyVar; //undefined type
  var nullVar = null;
  
  typeof intNum;
  typeof floatNum;
  typeof singleQuoteStr;
  typeof doubleQuoteStr;
  typeof boolean;
  typeof emptyVar;
```

<p> 출력값 : number, number, string, string, boolean, undefined </p>

<h6>[1-1] 숫자형 </h6>
<p> JS는 숫자형 데이터를 int나 float, double 등으로 구분하지 않고 number로 인식한다. 
  즉, <b>JS는 하나의 숫자형 number만 존재하며, 모든 숫자를 64비트 부동 소수점 형태로 저장한다.</b><br>
  JS는 모든 숫자형 데이터를 실수로 취급하기 때문에 나눗셈을 할때 모든 값들이 실수로 반환된다. 
  만약 C언어의 int형 나눗셈과 같이 정수 부분만 구하고 싶다면, <b>'Math.floor()'</b> 자바스크립트 메소드를 이용해야한다. </p>
 <p></p>
  ```
  var num = 5 / 2;
  console.log(num); // 출력값 : 2.5
  console.log(Math.floor(num)); // 출력값 : 2
  ```
<p></p>
<h6>[1-2] 문자열 </h6>
<p> 작은 따옴표, 큰 따옴표로 문자열을 생성한다. C언어와는 다르게 char 형태로 하나의 문자를 저장하는 데이터 타입이 없다.<br>
  따라서 예제의 singleChar 처럼 길이가 1인 문자열을 사용해야한다.<br>
  기본적으로 문자'열'이기 때문에 C언어와 같이 index를 통해 하나의 문자에만 접근은 가능하다.<br>
  하지만 JS에서는 <b>한번 정의된 문자열은 변하지 않는다.</b></p>
  
  
  
