# 📌 Local Storage (로컬 스토리지)
### 2025. 07. 22. 월요일

## 💡 로컬 스토리지란?
> 페이지를 변경하거나 브라우저를 닫아도 반 영구적으로 유지되는 저장소
- 직접 초기화하거나 제거하지 않는 이상 만료기간은 존재하지 않는다
- 브라우저를 닫아도 값은 유지된다
- 도메인이 다른 경우에는 로컬 스토리지에 접근할 수 없다

## 💪 로컬 스토리지 사용하기
### ✅ __setItem__ - 데이터 저장 
``` javascript 
localStorage.setItem("username", "효은"); // username에 효은이란 값을 저장 
```

### 📖 __getItem__ - 데이터 읽기
``` javascript 
const name = localStorage.getItem("username"); 
```

### ❌ __removeItem__ - 데이터 제거
``` javascript
localStorage.removeItem("username");
```

### ⚠️ __clear__ - 전체 삭제
``` javascript
localStorage.clear();
```
### 🗝️ __key(index)__ – 인덱스(index)에 해당하는 키를 받아옵니다.
### 💠 __length__ – 저장된 항목의 개수를 얻습니다.
***
## ⭐ 객체 사용하기
localStorage는 문자열만 저장되기 때문에
객체나 배열을 저장하려면 __JSON.stringify()__ 를 써야하고
불러올 때는 __JSON.parse()__ 를 사용하면 된다.

``` javascript
// 객체 불러오기
const user = {name: "효은", age: 17}
localStorage.setItem("user", JSON.stringify("user"));

// 객체 불러오기
const savedUser = JSON.parse(localStorage.getItem("user"));
console.log(savedUser.name);
console.log(savedUser.age);
```
