# 📌 Conditional Statement (조건문)
## if, else, else if

```javascript
const a = 10;
const b = 20;
const c = 20;

// if -------
if (a < b) {
  console.log("a가 더 작아요!");
}

// 이렇게도 작성 가능!
if (a < b) console.log("a가 더 작아요!");

// else ------
if (a < b) {
  console.log("a가 더 작아요!");
} else {
  console.log("거짓!");
}

// else if ------
if (a < b) {
  console.log("a가 더 작아요!");
} else if (b === c) {
  console.log("b와 c는 같습니다!");
} else {
  console.log("여기는 언제 출력될까요?");
}
```
