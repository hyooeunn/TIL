# 📍 React Hook (리액트 훅)
####  2026. 03. 26. 수요일

<br>

## 💡 React Hook이란?
> 함수형 컴포넌트에서 상태나 생명주기 같은 기능을 사용할 수 있게 해주는 기능
- 리액트 v16.8에 새로 도입된 기능
- 대표적인 예) useState, useEffect 등이 존재

## Hook 규칙
### 1. 최상위에서만 Hook을 호출한다.
- React에서는 Hook이 호출된 순서에 의존하기 때문
  ``` js
  // ❌ 잘못된 예
  if (isLogin) {
    useEffect(() => {});
  }

  // ✅ 올바른 예
  useEffect(() => {
  if (isLogin) {
    조건
  }
  }, [isLogin]);
  ```

<br />

- 조건문, 반복문, 중첩 함수 안에서 사용 금지
  ``` js
  // ❌ 잘못된 예
  for (let i = 0; i < 3; i++) {
    useState(0);
  }
  ```
  - 👆 랜더링 될때마다 Hook의 개수가 달라질 수 있음

---

### 2. React 함수 내에서만 Hook을 호출한다.
- React 함수 컴포넌트 또는 ❕Custom Hook 에서만 사용해야한다
  ``` js
  // ❌ 잘못된 예 / 일반 함수에서 Hook 사용 x
  function Hyoeun() {
    useState(0);
  }

  // ✅ 올바른 예
  function Hyoeun() {
    const [count, setCount] = useState(0);
  }
  ```

  <br>

- 의존성 배열 정확하게 작성!
  ``` js
  useEffect(() => {
    console.log(count);
  }, [count]); // 반드시 관련 값 포함!!!
  ```
  👆 빠트리면 버그 생기기 쉽당... 🐛

<br>

## ❕Custom Hook이란?
> 여러 컴포넌트에서 반복되는 로직을 하나의 함수로 분리해 재사용하는 것
- 코드의 중복을 줄이고 코드 파악이 좀 더 수월함!


### 🤷‍♀️ -  하나의 컴포넌트에 여러 상태를 거느려야할 때!
- 🚨 |

  복잡한 상태

  코드의 양이 많아져 컴포넌트를 재사용, 파악이 어려워짐

이러한 경우에 **Custom Hook**을 사용해 코드의 양을 줄이고 파악에 수월하게끔 함!

<br>

## 👻 | 마무링
25년 11월 이후 처음으로 적는 til 이자너 ㅎ...

이번에 프로젝트를 하면서 개념이 많이 부족하다는 걸 깨달았다... 그래서 새학기인만큼! 마음을 다잡고 다시 개념 공부한다고 생각하며 열심히 써봐야징!

이번에 React Hook을 알아보았으니 다음에는 useState와 useEffect!