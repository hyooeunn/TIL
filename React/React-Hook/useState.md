# 📍  useState
#### 2026. 03. 27. 목요일

<br>

## 💡 useState란?
> 함수형 컴포넌트에서 state(상태) 변수를 추가할 수 있는 React Hook

``` js
import { useState } = from 'react';

export function StatePage() {
  const [state, setState] = useState(초기값);
}
```
현재 상태 값은 state 변수에 있고, state를 변경하고 싶으면 setState 함수를 이용해 변경이 가능하다.

```state``` : 현재 상태 값 (상태 변수)

```setState``` : 상태를 업데이트할 수 있는 함수 (상태 변수 변경 함수)


  🚨 |  useState 뒤에는 null과 같이 초기 상태 값이 
  들어와야 함 (클래스형 컴포넌트, 조건문, 반복문 x)

<br>

### 예시
``` js
import { useState } = from 'react';

const [count, setCount] = useState(0) 
// 초기 값 0으로 설정

const handleClick() {
  setCount(count + 1);
}

export function CountPage() {
  return (
    <button>
      {count}
    </button>
  );
}
```
버튼을 누르면 1씩 숫자가 오름

## ⚠️ 주의할 점
- setState를 사용해 state를 변경하면, 다시 렌더링한다.
  
  상태가 변경되면 컴포넌트가 전체적으로 다시 렌더링 되어 변경된 상태가 반영되었다는 뜻이다!

- setState는 __비동기적으로 동작한다.__
  
  상태가 즉시 변경 x, 리렌더링 후에 새로운 상태가 적용된다.