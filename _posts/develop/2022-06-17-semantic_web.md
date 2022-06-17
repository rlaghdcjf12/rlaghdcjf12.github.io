---
permalink: /develop/2
title: "시맨틱 웹 (Semantic Web)"
date: 2022-06-17 20:00:00 +0900
categories: 개발
tags: 웹
---

## 시맨틱 웹이란?
<main>
  - Semantic Web. 의미 있는 웹. <br>
  - 검색엔진이 웹페이지를 크롤링 해서 이 웹페이지가 검색되기 위한 목차를 만드는데, 검색이 더 잘되도록 구성된 웹. <br>
  - [div, span, ...]과 같은 의미 없는 html 태그가 아닌, <strong>[header, nav, section, article, ...]과 같은 의미 있는 태그로 구성하자.</strong>
</main>
<center>
  <img width='50%' src='../../assets/images/post/Develop/building-structure.png' alt='sementic_web_tags'>
</center>

<details>
  <summary>시맨틱 태그 종류</summary>
  <p>
    - header : 머리글, 제목, 헤더 <br>
    - nav : 네비게이션, 목차, 리스트 등 다른 페이지로의 이동을 위한 링크 공간을 위주로 표현 <br>
    - aside : 좌측 혹은 우측 사이드 위치의 공간. 본문 외에 부수적인 내용을 주로 표현하는 태그 <br>
    - section : 주제, 카테고리 등 섹션을 구분. 같은 테마를 가진 여러개의 콘텐츠의 그룹화 <br>
    - article : 기사, 블로그 등 텍스트 위주의 페이지를 구성할때 주로 사용.  <br>
    - footer : 바닥글, 문서 하단에 들어가는 정보 구분 공간을 표현하는 태그 <br>
    - address : 콘텐츠 작성자나 사이트 소유자의 정보등을 부가적으로 담는 기능 <br>
    - hgroup : 제목과 관련된 부제목을 묶는 태그 <br>
    - main : 이름처럼 문서 body 태그의 중심 주제, 주요 내용 또는 응용 프로그램의 중심 기능과 직접 관련되어나 확장되는 콘텐츠를 나타낸다. <br>
    - figure : 이미지, 다이어그램, 사진 등 독립적인 컨튼츠 정의시 사용 <br>
    - figcaption : figure 요소의 설명 캔션(caption) 정의 <br>
    - mark : 현재 맥락에 관련이 깊거나 중요한 부분 강조 <br>
    - time : 시간의 특정 지점 또는 구간, datetime과 같은 속성을 이용해 알림같은 기능 구현 <br>
    - details : 주변 문맥에서 표시된 구절의 관련성 또는 중요성으로 인해 참조 또는 표기 목적으로 표시되거나 강조된 텍스트를 나타냅니다. <br>
    - summary : details 요소에 대한 요약, 캡션 또는 범례를 지정합니다. summary 요소를 클릭하면 상위 details 요소의 상태가 열리고 닫힙니다.
    </p>
</details>

<details>
  <summary>시맨틱 웹 장점</summary>
  <p>
    1. 검색 엔진 최적화 (SEO) : 검색 엔진 인덱싱 시 전달하고 싶은 의미 전달 가능<br>
    2. 유지보수 편리 : 가독성 있는 웹 태그
  </p>
</details>