<h4> (4.4) 함수 호출과 this </h4>

<h5> [4.4.1] arguments 객체 </h5>
<p> C와 같은 엄격한 언어와 달리, JS는 함수를 호출할 때 함수 형식에 맞춰 인자를 넘기지 않더라도 에러가 발생하지 않는다. </p>

```
// 인자 형식을 맞추지 않은 함수

function func(arg1, arg2) {
    console.log(arg1, arg2);
}

func(); // undefined undefined
func(1); // 1 undefined
func(1,2); // 1 2
func(1,2,3); // 1 2
```

<p> JS의 이러한 특징 때문에 함수 코드 작성할 때, 
  런타임 시에 호출된 인자의 개수를 확인하고 이에 따라 동작을 다르게 해줘야 할 경우가 있다.
  이를 가능케 하는 것이 바로 arguments 객체다. arguments 객체는 함수를 호출할 때 넘긴 인자들이 배열 형태로 저장된 객체인데,
  함수를 호출할때 인수들과 함께 암묵적으로 arguments 객체가 함수 내부로 전달된다.
  특이한 점은 이 arguments 객체가 <b>유사 배열 객체</b>라는 점이다.
</p>

```
// arguments 객체 확인
function add(a, b) {
    console.dir(arguments);
    return a + b;
}

console.log(add(1)); // NaN
console.log(add(1, 2)); // 3
console.log(add(1, 2, 3)); // 3

          /* console.log(add(1,2)) 경우만 보면 
          Arguments(2)
          0: 1
          1: 2
          callee: ƒ add(a, b)
          length: 2
          Symbol(Symbol.iterator): ƒ values()
          __proto__: Object
          */
```

<p> Arguemnt(n) 에서 n은 인자 갯수를 나타낸다. 이 n에 따라 length 가 정해진다. 즉, length는 인자의 개수다. 
  callee 는 현재 실행중인 함수의 참조값을 의미한다. arguments 는 비록 length 프로퍼티가 있지만, 유사 배열 객체이지
  배열이 아니기 때문에 표준 배열 메소드를 이용할 수 없다. <b>하지만 call 과 apply 매소드를 이용하면 가능하다.</b>
</p>

<p> argument 객체는 매개변수 개수가 정확하게 정해지지 않은 함수를 구현하거나, 
  전달된 인자의 개수에 따라 서로 다른 처리를 해줘야 하는 함수를 개발하는 데 유용하게 사용할 수 있다.</p>
  
```
function sum() {
    var result = 0;
    
    for(var i = 0 ; i < argument.length ; i++) {
        result += argument[i];
    };
    return result;
};

console.log(sum(1,2,3)); // 6
console.log(sum(1,2,3,4,5,6,7,8,9)); // 45
```

<h5> [4.4.2] 호출 패턴과 this 바인딩</h5>
<p> </p>

<p> </p>

<p> </p>

<p> </p>

<p> </p>
