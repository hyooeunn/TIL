# 📌 switch - 조건문

``` javascript
const number = 10;

switch (number) {
  // 만약 number 변수의 값이 1이면 case 1 실행
  case 1:
    console.log(number);
    // 실행이 끝나는 부분애는 break로 닫아주기
    break;
  case 10:
    console.log(number);
    break;

    // 조건문에 else 처럼 가장 마지막에 위치!
    // 위에 나열된 case 중 참이 없는 경우 제일 마지막에 실행
    default:
      console.log('아무것도 해당되지 않아요');
}
```

## break의 중요성!
``` javascript
const number = 13;

switch(number) {
  case 13:
    console.log('13인데여?');
    
  case 1:
    console.log('1이에오');
    break;
}

// 실행 결과:
// 13인데여?
// 1이에오
```
이처럼 case가 break을 만날때까지 실행되기 때문에
case 13이 참이여도 break를 만날때까지 그 안에 있는 것들이 실행 됨

__그래서 case를 사용할 때 break랑 한쌍으로 사용해야함!__

## if와 switch문 비교
모듈러 홀짝
``` javascript
const number = 10;

if (number % 2 == 0) {
  console.log('짝수');
}
else {
  console.log('홀수');
}
// 결과: 짝수

switch (number % 2) {
  case 0:
    console.log('짝수');
    break;
  case 1:
    console.log('홀수');
    break;
}
// 결과: 짝수
```