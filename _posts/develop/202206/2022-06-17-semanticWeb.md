---
permalink: /develop/2
title: '시맨틱 웹 (Semantic Web)'
date: 2022-06-17 20:00:00 +0900
categories: 개발
tags: 웹 프론트엔드
---

## 시맨틱 웹이란?
<main>
  - Semantic Web. 의미 있는 웹. <br>
  - 인덱싱 효율을 높여서 검색이 더 잘되도록 구성된 웹. 검색엔진이 웹페이지를 크롤링 할 때 이 웹페이지가 검색되기 위한 목차를 만드는 과정을 인덱싱이라고 한다. <br>
  - [div, span, ...]과 같은 의미 없는 html 태그가 아닌, <strong>[header, nav, section, article, ...]과 같은 의미 있는 태그로 구성하자.</strong>
</main>
<center>
  <img width='50%' src='../../assets/images/post/Develop/building-structure.png' alt='sementic_web_tags'>
</center>

<details>
  <summary><span style='text-decoration:underline;'>시맨틱 태그 종류에 대해 알아보기</span></summary>
  <p>
    - <strong>header</strong> : 머리글, 제목, 헤더 <br>
    - <strong>nav</strong> : 네비게이션, 목차, 리스트 등 다른 페이지로의 이동을 위한 링크 공간을 위주로 표현하는 태그 <br>
    - <strong>aside</strong> : 좌측 혹은 우측 사이드 위치의 공간. 본문 외에 부수적인 내용을 주로 표현하는 태그 <br>
    - <strong>section</strong> : 주제, 카테고리 등 섹션을 구분하는 태그. <strong>같은 테마를 가진 여러개의 콘텐츠의 그룹화</strong> <br>
    - <strong>article</strong> : 기사, 블로그 등 <strong>텍스트 위주의 페이지</strong>를 구성하는 태그  <br>
    - <strong>footer</strong> : 바닥글, 문서 하단에 들어가는 정보 구분 공간을 표현하는 태그 <br>
    - <strong>details</strong> : 주변 문맥에서 표시된 구절의 관련성 또는 중요성으로 인해 참조 또는 표기 목적으로 표시하거나 강조하는 태그 <br>
    - <strong>summary</strong> : details 요소에 대한 요약, 캡션 또는 범례를 지정하는 태그. summary 클릭 시 details가 열리고 닫힌다. <br>
    - <strong>main</strong> : body 태그의 중심 주제, 주요 내용 또는 응용 프로그램의 중심 기능을 나타내는 태그 <br>
    - address : 콘텐츠 작성자나 사이트 소유자의 정보 등을 부가적으로 담는 태그 <br>
    - time : 시간의 특정 지점 또는 구간 태그. datetime과 같은 속성을 이용해 알림과 같은 기능을 구현한다. <br>
    - figure : 이미지, 다이어그램, 사진 등 독립적인 컨텐츠 정의시 사용하는 태그 <br>
    - figcaption : figure 요소의 설명 캡션을 정의하는 태그 <br>
    - hgroup : 제목과 관련된 부제목을 묶는 태그 <br>
    - mark : 현재 맥락에 관련이 깊거나 중요한 부분을 강조하는 태그
    </p>
</details>

<details>
  <summary><span style='text-decoration:underline;'>시맨틱 웹 장점은?</span></summary>
  <p>
    1. 검색 엔진 최적화 (SEO) : 검색 엔진 인덱싱 시 전달하고 싶은 의미 전달 가능<br>
    2. 유지보수 편리 : 가독성 있는 웹 태그
  </p>
</details>
