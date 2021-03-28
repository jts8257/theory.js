<p> 책에서는 줄곳 ECMAScript명세를 참조하라느니, ES6가 어떻다느니 하는 이야기가 나온다. 도대체 ECMAScript는 뭘까</p>

### ECAM-262와 ECMAScript
<p> 우선 ECMA 는 Ecma인터네셔럴이라는 정보 통신에 대한 표준을 제정하는 비영리 표준화 기구를 뜻한다.<br>
  이 기구는 라는 ECMA-262표준을 제정하는데, 이 표준은 <b>범용 목적의 스크립트 언어에 대한 명세</b> 를 담고있다. 
인사이드 자바스크립트에서 언급되는 ECMAScript명세는 ECMA-262 표준을 준수하는 script명세를 의미한다.<br>
즉, ECMASCript는 ECMA-262에서 정의된 하나의 명세를 의미한다. ECMAScript는 스크립트어 언어가 준수해야 하는 규칙, 세부사항 및 지침을 제공한다.<p>
  
[ECMA-262](https://www.ecma-international.org/publications-and-standards/standards/ecma-262) 
  
### JS와 ECMAScript
<p> JS는 ECMAScript 명세를 준수하는 범용 스크립트 언어이다. ECMAScript를 읽으면 어떻게 스크립트 언어는 어떻게 생겨야 하는지를 알 수 있고
  JS문서를 읽으면 어떻게 스크립트 언어를 쓸 수 있는지 알 수 있다. 둘은 그러한 관계이다. </p>
  
  
### JS엔진과 ECMAScript
<p> JS엔진은 JS코드를 이해하고 실행하는 프로그램 또는 인터프리터이다. 일반적으로 웹 브라우저에서 찾아볼 수 있다.<br>
  그리고 각 웹 브라우저마다 JS엔진이 다른데, 크롬은 V8, 파이어폭스는 SpiderMonkey, 엣지는 Chakra 등을 제공한다. <br>
  각 JS엔진마다 지원하는 ECMAScript가 다른데, JS는 ECMAScript를 준수하는 언어이므로, 
  브라우저가 얼마나 JS를 잘 지원하느냐는 곧 <b>ECMAScript호환성</b>이 얼마나 되느냐와 같은 질문이다.</p>
 
### ES6와 ECMAScript
<p> 이제는 대충 알겠지만, ES는 ECMAScript의 줄임말이고, ES6는 ECMAScript6판을 의미한다.(2015년에 나왔으므로 ES 2015라고도 한다)<br>
  2015년 ES6이 제정된 이후 매년 새로운 버전이 제정되고 있는데, 현지 시점에서는 ES2019가 제정되어 있다. 
  하지만 현재 대부분의 JS엔진은 ES6까지 지원한다. </p>
  
  
