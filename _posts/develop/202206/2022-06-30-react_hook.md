---
permalink: /develop/6
title: '리액트의 Hook'
date: 2022-06-30 20:00:00 +0900
categories: 개발
tags: 웹 프론트엔드
---

나는 주로 함수형 컴포넌트를 사용하는데, 함수형 컴포넌트에서는 Life Cycle이 아닌 Hook을 사용한다고 하니 이를 알아보자.

## 리액트의 Life Cycle과 Hook

Life Cycle : 클래스형 컴포넌트에서 사용  
**Hook : 함수형 컴포넌트에서 사용**

## Hook의 사용

- 리액트 16.8버전부터 사용
- 클래스 컴포넌트 방식에서 벗어나 함수형 컴포넌트 방식으로 더 직관적으로 작업할 수 있도록 함

**1. STATE HOOK - useState()**

```
const [age, setAge] = useState(42);
```

- state 훅은 위와 같이 사용된다.
- age라는 state, 이 age state의 값을 변경하는 setAge, age의 초기값을 설정해주는 useState로 이루어진다.

**2. EFFECT HOOK - useEffect()**

```
useEffect(() => {
    document.title = `You clicked ${count} times`;
});
```

- effect 훅은 위와 같이 사용된다.
- 렌더링을 할 때 마다 effect가 실행된다.
- Life Cycle의 componentDidMount, componentDidUpdate와 비슷하다.
- 컴포넌트 안에 선언되었기 때문에 props/state에 접근 가능하다.

**3. REF HOOK - useRef()**

```
const scrollRef = useRef(null);
```

- DOM의 특정 엘리먼트를 선택할때 사용
- .current 프로퍼티에 전달된 인자로 초기화된, 변경 가능한 ref 객체를 반환
- 반환된 객체는 컴포넌트의 전 생애주기를 통해 유지

**4. CONTEXT HOOK - useContext()**

**5. REDUCER HOOK - useReducer()**

**6. MEMO HOOK - useMemo()**

**7. CALLBACK HOOK - useCallback()**
