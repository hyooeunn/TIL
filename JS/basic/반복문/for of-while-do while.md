# 📌 for of, while, do while

## ☝️ for of
> 주어진 객체를 차례대로 순회하면서 주어진 코드를 실행하는 방식
for문이랑 비슷하지만
__() 안에 사용할 변수, of 라는 키워드, 반복이 가능한 객체__ 를 집어 넣음

``` javascript 
const arr = [1, 2, 3];

// 괄호 안에 i라는 변수와 of 반복이 가능한 배열
for (const i of arr) {
  console.log(i);
}

// 결과: 배열 안의 요소들이 나옴
// 1
// 2
// 3
```

## ✌️ while
> 괄호 안에 지정된 조건이 만족할 동안 내부 코드를 반복
조건이 참일동안 반복

```javascript
let i = 0;

while (i < 10>) {
  console.log(i++)
}
```

## 🤟 do while

``` javascript
let i = 0;

do {
  console.log(i++);
} while (i < 10);
```
코드를 먼저 보고 다음 반복문으로 넘어가기 전에 조건식을 판별
