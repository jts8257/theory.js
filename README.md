# Inside_JS

<h3>자바스크립트 데이터 타입과 연산자</h3>

<h4>(1)기본타입 {숫자,문자열,불린값,undifined, null}</h4>
<h4>(2)참조타입_객체{배열,함수,정규표현식}</h4>
<h4>(3)주요 연산자</h4>

<h4>(1)기본타입 {숫자,문자열,불린값,undifined, null}</h4>
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

<h5>[1-1] 숫자형 </h5>
<p> JS는 숫자형 데이터를 int나 float, double 등으로 구분하지 않고 number로 인식한다. 
  즉, <b>JS는 하나의 숫자형 number만 존재하며, 모든 숫자를 64비트 부동 소수점 형태로 저장한다.</b><br>
  JS는 모든 숫자형 데이터를 실수로 취급하기 때문에 나눗셈을 할때 모든 값들이 실수로 반환된다. 
  만약 C언어의 int형 나눗셈과 같이 정수 부분만 구하고 싶다면, <b>'Math.floor()'</b> 자바스크립트 메소드를 이용해야한다. </p>

```
  var num = 5 / 2;
  console.log(num); // 출력값 : 2.5
  console.log(Math.floor(num)); // 출력값 : 2
```
  
<h5>[1-2] 문자열 </h5>
<p> 작은 따옴표, 큰 따옴표로 문자열을 생성한다. C언어와는 다르게 char 형태로 하나의 문자를 저장하는 데이터 타입이 없다.<br>
  따라서 예제의 singleChar 처럼 길이가 1인 문자열을 사용해야한다.<br>
  기본적으로 문자'열'이기 때문에 C언어와 같이 index를 통해 하나의 문자에만 접근은 가능하다.하지만 JS에서는 <b>한번 정의된 문자열은 읽기만 가능하고 수정은 불가능하다.</b></p>

```
var str = 'test';
console,log(str[0], str[1], str[2], str[3]); // 출력값 : test
str[0] = 'T';
console.log(str); // 출력값 : test
```

<h5>[1-3] null과 undefined </h5>
<p> null과 undefined는 모두 값이 비어있음을 나타낸다. <br>
  자바스크립 환경내에서 기본적으로 값이 할당되지 않은 변수는 undefined 타입이며, 해당 변수의 값 또한 undefined 이다. <b>undefined는 데이터 타입이자 값 그 자체이다.</b> <br>
  반면 null은 개발자가 명시적으로 해당 변수가 비어있음을 나타내는데 사용한다. 이때 null타입 데이터는 typeof 메소드에서는 null이 아닌 object가 반환된다. 따라서 해당 변수가 null 타입인지 알아보기 위해서는 일치 연산자 (===) 를 사용해야한다.</p>

```
var nullVar = null;
console.log(nullVar === null); // 출력값 : true
console.log(typeof nullVar === null); // 출력값 : false
```

<h4>(2)참조타입_객체{배열,함수,정규표현식}</h4>
<p> 자바스크립트에서 객체는 단순히 [key : value] 형태의 프로퍼티들을 저장하는 컨테이너로서, 컴퓨터 과학 분야에서 해시라는 자료구조와 상당히 유사하다.<br>자바스크립트에서 기본타입은 하나의 값만 가지는것과 달리 참조 타입(객체)은 여러개의 프로퍼티들을 포함할 수 있으며, 이러한 객체의 프로퍼티는 기본 타입의 값을 포함하거나, 다른 객체를 가리킬 수도 있다. 이러한 프로퍼티의 성질에 따라 객체의 프로퍼티는 함수로 포함할 수 있으며, JS에서는 이러한 프로퍼티를 메소드라고 부른다.</p>

<h5>[2-1] 객체 생성 </h5>
<p> JS의 객체 개념은 생성 방법과 상속 방식 등에서 C++이나 JAVA와 같은 OOP 언어의 객체 개념과는 다르다.<br>
  JAVA는 클래스를 정의하고, 클래스의 인스턴스를 생성하는 과정에서 객체가 만들어진다. 이에 비해 JS는 클래스의 개념이 없고, 객체 리터럴이나 생성자 함수 등 별도의 생성 방식이 존재한다. </p>
<p> JS는 object() 함수 이용, 객체 리터럴, 생성자 함수라는 세가지 방법으로 객체를 생성하는데, 이번 장에서는 object와 객체리터럴만 다루고 다음 장에서 생성자 함수와의 차이점을 다룬다. </p>


<object를 이용한 객체의 생성>

```
var foo = object(;
foo.name = 'foo';
foo.age = 30;
foo.gender = 'male';

console.log(typeof foo) // 출력값 : object
console.log(foo) // 출력값 : {name : 'foo', age : 30, gender = 'male'}
```

<객체 리터럴을 이용한 객체의 생성>
<p> 객체 리터럴이란 객체를 생성하는 표기법이다.</p>

```
var foo {
  name : 'foo',
  age : 30,
  gender = 'male'
}; 

console.log(typeof foo) // 출력값 : object
console.log(foo) // 출력값 : {name : 'foo', age : 30, gender = 'male'}
```


  
  
  
