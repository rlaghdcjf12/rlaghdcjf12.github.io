---
permalink: /develop/5
title: '리액트의 Life Cycle'
date: 2022-06-29 20:00:00 +0900
categories: 개발
tags: 웹 프론트엔드
---

회사 첫 웹 스택 프로젝트를 Nuxt.js로 했었는데, Life Cycle을 이용해서 웹 페이지를 사용자에게 띄우기 전에 데이터를 미리 받아와서 처리하고 그랬었다. React에는 어떤 Life Cycle이 있는 지 알아보자.

## 리액트의 Life Cycle과 Hook

**Life Cycle : 클래스형 컴포넌트에서 사용**  
Hook : 함수형 컴포넌트에서 사용

## 리액트 컴포넌트의 라이프사이클

<img style='width: 80%; margin: 0 10%;' src='https://cdn.filestackcontent.com/ApNH7030SAG1wAycdj3H' alt='리액트 컴포넌트의 생명주기'/>

<details>
    <summary>레거시(구버전) 라이프사이클</summary>
    <div>
        <img style='width: 80%; margin: 0 10%;' src='https://velog.velcdn.com/images/st2702/post/adbd06c3-50ad-4251-a374-57622e21bc12/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-10-22%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%2011.12.17.png' alt='구버전 리액트 컴포넌트의 생명주기'/>
    </div>
</details>

## 간단 순서

1. 페이지에 필요한 컴포넌트들을 **마운트**한다.
2. 상황에 따라 props와 state를 변경이 되면 컴포넌트를 **업데이트**한다.
3. 렌더 이전에 필요한 작업을 하는 단계와 렌더 이후 작업을 하는 단계가 있다.
4. 컴포넌트가 필요 없어지면 컴포넌트를 **언마운트** 한다.

### 1. Mount

- start ~ running 단계. 처음 컴포넌트가 만들어지는 단게.
- 컴포넌트를 만드는 constructor 단계 이후 WillMount - render - DidMount의 단계로 렌더링 되기 전에 처리해야할 것과 렌더링 이후에 처리되는 것들을 나눠서 다룰 수 있다.

<details>
    <summary>Mount 단계 상세</summary>
    <div style='margin-left: 20px;'>
        <strong>1. constructor()</strong>
        <ul style='margin-left: 20px;'>
            <li> 메소드 바인딩, state 초기화(생성자는 this.state를 직접 할당할 수 있는 유일한 곳)
            <li> setState 사용 불가
            <li> DOM 접근 불가
        </ul>
    </div>
    <div style='margin-left: 20px; color:lightgrey;'>
        <span>2. getDerivedStateFromProps(props, state)</span>
        <ul style='margin-left: 20px;'>
            <li> 렌더링 시마다 실행됨
            <li> 컴포넌트 인스턴스 접근 불가
            <li> 이 메소드는 사용하지 않는 것을 권고
            <li> 구버전의 componentWillReceiveProps와는 다르다. CWRP는 부모 컴포넌트가 재 렌더링 시에만 실행됨
        </ul>
    </div>
    <div style='margin-left: 20px;'>
        <strong>3. componentDidMount()</strong>
        <ul style='margin-left: 20px;'>
            <li> 외부에서 데이터를 가져오기 좋은 위치
            <li> 데이터바인딩 가능 - 이 경우 Unmount시 바인딩 해제 필요
        </ul>
    </div>
</details>

### 2. Update

- 컴포넌트에서 사용되는 props나 state가 변경되었을 때 이뤄지는 단계.
- props 변경 시 state 변경 시보다 WillReceiveProps 단계가 추가되어 있다.
- 이후 shouldComponentUpdate - WillUpdate - render - DidUpdate 순이다.

<details>
    <summary>Update 단계 상세</summary>
    <div style='margin-left: 20px; color:lightgrey;'>
        <span>1. shouldComponentUpdate</span>
        <ul style='margin-left: 20px;'>
            <li> state/props의 변화가 컴포넌트의 출력에 영향을 미치는 지 확인 (기본값 true)
            <li> false를 반환함으로써 componentWillUpdate, render, 그리고 componentDidUpdate가 호출되지 않음. (재 렌더링되지 않음)
            <li> 이 메소드는 사용하지 않는 것을 권고
            <li> 구버전의 componentWillReceiveProps와는 다르다. CWRP는 부모 컴포넌트가 재 렌더링 시에만 실행됨
        </ul>
    </div>
    <div style='margin-left: 20px;'>
        <strong>2. componentDidUpdate(prevProps, prevState, snapshot)</strong>
        <ul style='margin-left: 20px;'>
            <li> 컴포넌트가 갱신되었을 때 DOM 조작 시 사용
            <li> 이전 컴포넌트와 props/state를 비교하여 데이터 통신을 요청하는 데 사용
        </ul>
    </div>
</details>

### 3. Unmount

- 컴포넌트가 페이지에서 없어지는 단계.

<details>
    <summary>Unmount 단계 상세</summary>
    <div style='margin-left: 20px;'>
        <strong>1. componentWillUnmount(prevProps, prevState, snapshot)</strong>
        <ul style='margin-left: 20px;'>
            <li> 컴포넌트가 마운트 해제되기 직전 호출됨
            <li> 타이머 제거, 네트워크 요청 취소, 이전에 등록한 데이터 바인딩 해제 등 정리 작업 시 사용
        </ul>
    </div>
</details>
