# 📌 function (함수)

## 함수란?
> 어떤 목적을 달성하거나 원하는 결과를 도출하기 위한 코드 집합
- 한번만 쓰는게 x 반복적인 동작을 처리하기 위해 쓰임
- 같은 이름으로 계속 재활용할 수 있음

### ◽ 함수 사용 예시
``` javascript
function 함수이름() {
  // 괄호는 함수에서 사용하려는 인자를 담는 공간 | 반드시 정의 x
}

함수이름();
```

```javascript
function bok(main) {
  console.log('${main} 볶음밥');
}

bok('새우');
bok('제육');
// 결과: 새우 볶음밥, 제육 볶음밥
```

### () 인자 두개
``` javascript
function sum(a, b) {
  console.log(a + b);
}

sum(10, 20);
// 결과: 30
```

__인자 (Arguments)__
- 함수의 입력 __값__

__매개 변수 (Parameter)__
- 함수의 입력 __변수__
- 함수를 정의할 때 작성하는 필요 인자

***

``` javascript
function a() {
  const b = 10; // <- 지역 변수
  console.log(b);
}

a ();
console.log(b);
// 결과
// 함수 안에서의 b의 값 10은 출력
// 함수 밖에서의 b의 값은 출력 x
```

## 지역변수
>변수를 사용할 수 있는 범위가 중괄호로 감싸진 블록 안으로 제한
(함수 뿐 아니라 조건문, 반복문도 마찬가지!)

- 즉 함수 내부에 선언된 변수는 함수 내부에서만 사용 가능!

***

``` javascript
const b = 10; // <- 전역 변수

function a() {
  console.log(b);
}

a ();
console.log(b);

// 결과
// 10
// 10
// 둘다 출력이 됨
```

### 전역 변수
함수 내부에서 접근 O, 그래서 함수에 b가 존재하지 않아도 외부에 존재하는 전역 변수 b를 출력할 수 있게 함!

***

## 지역 변수와 전역 변수
``` javascript
const b = 10; // 전역 변수

function a() {
  const b = 20; // 지역 변수
  console.log(b);
}

a (); // 20
console.log(b); // 10
```