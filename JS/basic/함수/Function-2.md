# 📌 Function-2

## 함수의 표현식
``` javascript
// function sum(a, b) {
//   console.log(a + b);
// };

//함수 이름을 변수로
const sum = function (a, b) {
  console.log(a + b);
};

sum(10, 20);
```

## ⬆ 화살표 함수
함수의 표현식보다 더 심플함

``` javascript
const sum = (a, b) => console.log(a + b);
// 함수에서 function이라는 키워드를 없애고 좀더 단순한 표현방식으로 바꿈
```
명령어가 한 줄일때 중괄호를 생략하면 return 생략 가능
값이 자동으로 return

``` javascript
const sum = (a, b) => {
  console.log(a + b);
};
```
이렇게 중괄호가 있을 때는 return을 써 줘야함
``` javascript
const sum = (a, b) => {
  return a + b;
};

console.log(sum(10, 20));
// 이렇게!
```
***
❗ 인자가 __하나__ 일때 괄호 생략 가능
``` javascript
const sum = a => {
  return a + b;
};