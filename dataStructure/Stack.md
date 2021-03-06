# Stack
## 1. Stack이란?
Stack은 LIFO(last in, first out) 구조이다. 나중에 들어온 요소가 가장 처음으로 나간다. 들어오고 나오는 입구가 1개밖에 없는 구조이기 때문이다.<br/>
실험용 실린더를 생각하면 쉽다. <br/>
첫번째로 들어간 요소가 가장 밑에 들어가있기 때문에 그 요소를 꺼내기 위해서는 위에 있는 요소부터 제거해야한다.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Data_stack.svg/300px-Data_stack.svg.png">

## 2. Stack 기능
### 2.1 데이터의 추가
<img src="http://www.javascripttutorial.net/wp-content/uploads/2016/08/JavaScript-Stack-Push-Operations.png"></img>
> (출처: JavaScript Tutorial)

Stack에 데이터를 추가하는 기능을 JavaScript로 구현하면 다음과 같다. 데이터가 뒤쪽으로 추가되도록 한다.<br/>
``` javascript
var Stack = function(){
  this.stack = [];
}
// element 추가
Stack.prototype.add = function(elem){
  this.stack.push(elem);
  return this.stack;
}
```
### 2.2 데이터의 삭제
<img src="http://www.javascripttutorial.net/wp-content/uploads/2016/08/JavaScrippt-Stack-Pop.png"></img>
> (출처: JavaScript Tutorial)

나중에 추가된 요소부터 삭제되도록 구현하면 된다.
``` javascript
// element 삭제
Stack.prototype.remove = function(){
  var removed = this.stack.pop();
  return removed;
}
```
