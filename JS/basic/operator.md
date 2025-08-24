# 📌 operator (연산자)

### 🧮 산술 연산자
+, -, *, /
나머지 %
제곱 **

### 📈 증감 연산자 📉
- 숫자를 증가하거나 감소시키는 연산자
__++__ (숫자 값이 1 증가)
__--__ (수샂 값이 1 감소)

### 🤷‍♀️ 비교 연산자
__<, >, <=, >=__
__===__ (양변의 값 비교)
__!==__ (양변이 같은지 다른지 비교)

### 🧠 논리 연산자
__&&__ (모두 참일 때 참)
__||__ (하나만 참이어도 참)
__!__ (부정)

``` javascript
const a = 2 < 3;
const b = 30 > 50;

console.log(a && b);
// false

console.log(a || b);
// true

console.log(!a);
// ture -> false
```

### 삼항 연산자
- __조건 ? 첨 일때 실행될 부분 : 거짓일 때 실행될 부분__

``` javascript
console.log(2 > 3 ? '참' : '거짓');
```

### 널리쉬(Nullish) 연산자
__??__
- 여러 개의 피연산자 중 값이 확정되어 있는 변수를 찾음
``` javascript
const a = undefind;
const b = null;
const c = '이효은';

console.log(a ?? b ?? c);
// 결과 : 이효은
```

### 비트 연산자
__&(and), |(or), ~(not), ^(xor), <<(left shift) >>(right shift)__

### 대입 연산자
__+=, -=, *=, /=, %=, **=__

``` javascript
let number = 10;
number = number + 2;

// 복합 연산자 대입
number += 2;

number %= 2;
// number = number % 2;이거와 같음
```