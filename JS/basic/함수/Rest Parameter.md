# 📌 Rest Parameter (나머지 매개 변수)
# 📌 Return 함수의 반환 값

## 나머지 매개 변수 (Rest Parameter)
3개 이상의 임자를 전달 받아서 사용하고 싶다면 Rest Parameter 쓰기!
``` javascript
function print(a, b ... rest) {
  console.log(a);
  console.log(b);
  console.log(rest);
}

print (10, 20, 30, 40, 50);
// 결과
// 10
// 20
// [30, 40, 50]

// rest는 나머지 인자 값을 하나의 배열로 받으며 출력
```

## return 함수의 반환 값
현재 함수를 종료하고 지정한 값을 함수로 호출한 곳으로 반환

``` javascript
function sum (a, b) {
  return a + b;
}

console.log(sum(10, 20));
// 결과: 30
```