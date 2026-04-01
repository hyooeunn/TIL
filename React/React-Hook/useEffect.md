# 📍 useEffect

### 2026. 04. 01.

<br>

## 💡 useEFfect란?

> 컴포넌트가 랜더링 될 때마다 특정 작업을 수행하는 Hook

<br>

### 기본형태

```js
useEffect(function, deps)
```

`function`: 수행하고자 하는 작업

`deps`: 이전 랜더링 시점과 현재 랜더링 시점에서 달라지면 `function`을 다시 수행함

<Br>

**불러오기**

```js
import { useEffect } from "react";
```

---

<br>

### 1. 랜더링 될 때 실행되는 코드

```js
useEffect(() => {
  console.log("랜더링 될 때마다 실행됩니다!");
});
```

`deps`(배열)이 생략된 코드로 랜더링이 될때마다 실행 된다.

#### 🚨 | 무한 루프나 불필요한 연산을 수행할 수 있음 (거의 사용 x)

---

<br>

### 2. 처음 랜더링 (mount) 될 때만 실행되는 코드

```js
useEffect(() => {
  console.log("마운트 될 때만 실행됩니당");
}, []);
```

화면에서 가장 처음 랜더링 될 때만 수행하고 싶으면 `deps` 자리에 빈 배열 `[]`을 넣는다.

- 주로 한 번만 실행되어야 할 때 사용된다.

<br>

---

### 3. Unmount나 업데이트 될 때 실행되는 코드

```js
useEffect(() => {
  console.log(name);
  console.log("name이 업데이트 될 때만 실행");
}, [count]);
```

```js
const mounted = useRef(false);

useEffect(() => {
  if (!mounted.current) {
    mounted.current = true;
  } else {
    console.log(name);
    console.log("업데이트 될 때마다 실행");
  }
}, [name]);
```

특정 값이 업데이트 될 때 실행하고 싶을 때는 `deps` 배열 안에 검사하고 싶은 값을 넣어준다.

- 업데이트 될 때만 실행 x, 마운트 될 때도 실행

<br>

---

### 4. 컴포넌트가 Unmount 되었을 때(사라질 때)나 업데이트 되기 직전에, 다음 효과가 실행되기 전에

```js
useEffect(() => {
  console.log("실행: ", id);

  return () => {
    console.log("정리: ", id);
  };
}, [id]);
```

<br>

## ❓ | useEffect에서의 무한루프 해결 방법

useEffect 무한루프가 일어나는 대부분의 원인은 useState와 연관이 높다.

setState를 호출해 state를 수정하면 **컴포넌트가 재 랜더링** 이 되므로 무한루프가 나타난다.

```js
useEffect(() => {
  setCount(count + 1);
});
```

`setCount`로 `count`를 1 증가 시키면 해당 컴포넌트는 업데이트가 되어 다시 랜더링 되고, 또 다시 랜더링 됨에 따라 count의 값이 바꼈기에 useEffect 안에 있는 코드가 돌고 돌며 무한 루프가 됨

<br>

### 특정 값이 변할 때만 코드가 실행되게 하기

```js
import { useState, useEffect } from 'react';

function CountChange() {
  const [value, setValue] = useState("");
  const [count, setCount] = useState(-1);

  useEffect(() => setCount(count + 1), [value]);

  return (
    // 출력 코드...
  )
}
```

`value`가 몇번 변경되었는지 확인해 `value`가 변경될 때마다, count를 갱신
