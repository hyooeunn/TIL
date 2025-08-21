# 📌 Spread Syntax (전개 구문)

``` javascript
const numbers = [1, 2, 3]

console.log(numbers)
// 결과: [1, 2, 3]

// 전개 연산자 - numbers가 가진 걸 쫙 펼쳐서 보여줌
console.log(...numbers)
// 결과: 1, 2, 3
```

## 전개 구문 배열 활용 예제

``` javascript
const numbers = [1, 2, 3];
const numbers2 = [4, 5, 6];

const newNumbers = [...numbers, numbers2];
console.log(newNumbers);
// 결과: [1, 2, 3, 4, 5, 6]
```