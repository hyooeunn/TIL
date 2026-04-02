# 📍 useMemo

### 2026. 04. 02.

<br>

## 💡 useMemo란?

> 연산 결과를 memoization하여 불필요한 재계산 방지

> 메모리를 메모로 저장해서 필요할 때 꺼내 쓰는 것

- memoization: 메모리에 넣기

### 구조

```js
const value = useMemo(() => {
  return calculate();
}, [item]);
```

**useMemo**는 ***useEffect***처럼 첫 번째 인자로 콜백 함수, 두 번째 인자로 의존성 배열을 받는다.

- 배열 안에 값이 업데이트 될 때에만 콜백 함수를 호출해 메모리에 저장된 값을 업데이트한다.

<hr>
<br>

#### ‼️ | 만약 빈 배열을 넣는다면?

```js
const value = useMemo(() => {
  return calculate();
}, []);
```

***useEffect***와 마찬가지로 마운트 될 때에만 값을 계산
그 이후론 계속 memoization된 값을 꺼내와 사용!

<br>

### 같은 값을 반환하는 함수를 반복적으로 호출해야한다?

→ 처음 값을 계산할 때 해당 값을 메모리에 저장

→ 필요할 때마다 다시 계산 x

→ **메모리에 꺼내서 재사용!**

<br>

#### 비용이 큰 연산 결과를 캐싱한다.

- 계산하기 힘들거나 오래 걸리는 일은 한 번만 제대로 하고, 그 결과값을 메모지에 적어서 잘 보이는 곳에 붙여두는 것

#### dependency가 바뀔 때만 재계산 그 외에는 이전 값을 반환

```js
const sorteList = useMemo(() => {
  // items 또는 filter가 바뀔 때만 재계산
  return items
    .filter((i) => i.active === filter)
    .sort((a, b) => a.name.localCompare(b.name));
}, [itmes, fileter]);
```

<br>

### useMemo의 장점

같은 계산을 반복해야할 때, 이전에 계산한 값을 메모리에 저장해 같은 계산을 반복 / 수행을 제거하며 프로그램 실행 속도를 높인다!
