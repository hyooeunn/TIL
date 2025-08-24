# 📌 Iteration (반복문)
## for, break, continue

## 반복문이란?
> 반복적으로 수행해야하는 동작을 처리하기 위해서 사용되는 제어문

## ☝️ for
``` javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
// 결과:
// 0
// 1
// 2
// 3
// 4
```

### 시작값 생략하기
``` javascript
let i = 0;
for (; i < 5; i++) {
  console.log(i);
}
// 결과: 위와 같음
```

### 증감 식 생략하기
``` javascript
for (let i = 0; i < 5;) {
  console.log(i++);
}
// 결과: 위와 같음(변화 없음) 
```

## ✌️ break
사용자가 원하는 시점에 반복문을 빠져나오게 할 수 있음

``` javascript
for (let i = 0; i < 10; i++) {
  // i가 7이 되면 반복문을 빠져나가게
  if (i === 7) {
    break;
  }

  console.log(i);
}
// 결과:
// 0
// 1
// 2
// 3
// 4
// 5
// 6
```

## 🤟 conntinue
> 현재 반복만 종료하고 다음 번 반복으로 넘기는 명령어

``` javascript
for (let i = 0; i < 5; i++) {
  // 3만 건너뛰고 출력
  if (i === 3) {
    continue;
  }
  console.log(i);
}

// 결과:
// 0
// 1
// 2
// 4
