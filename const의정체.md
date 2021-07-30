const는 stack 영역을 상수로 만드는 것이다.  <br>
따라서 힙 영역에 저장되는 배열, 객체, 함수를 const로 선언한다 하더라도 변경하는 메서드를 이용할 수 있다. <br>


```javascript
const a = 10;
const b = [1,2,3];
a = 20 // 에러
b.push(4); // 에러 아님

```
