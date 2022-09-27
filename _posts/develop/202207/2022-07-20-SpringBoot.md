---
permalink: /develop/12
title: 'SpringBoot'
date: 2022-07-20 20:00:00 +0900
categories: 개발
tags: 웹 백엔드
---

나는 프론트엔드 개발자를 지향했으나, 현재 투입된 프로젝트에서 백엔드를 다뤄볼 기회도 얻게 되어 스프링 부트를 사용한 자바 백엔드 개발도 같이 하고 있다. 처음 백엔드를 하다보니, 모르는 것이 너무 많다. 앞으로 차근차근 알아가 보자.

# Spring이란?

- JAVA 기반의 웹 애플리케이션을 개발할 수 있는 프레임워크.
- 국내 대부분의 많은 기업들이 제공하는 서비스의 백엔드 개발에 사용됨

# Spring Boot란?

- Spring을 좀 더 쉽게 사용하기 위한 도구.
- Spring을 이용하여 서비스를 개발할 때 이것저것 필요한 세팅들이 많은데, 이를 좀 더 간단하게 설정할 수 있게 많은 부분들을 자동화해서 인프라 쪽에 사용할 에너지를 아낄 수 있도록 한다.

# Spring Boot의 구조

![리액트-스프링부트][리액트-스프링부트]{: .align-center}

솔직히 백날천날 구조를 눈으로 보기만 하면 머리에 안 들어온다. 현재 프로젝트를 진행하면서 이 구조를 몸으로 체득했다.
- 리액트와 같은 프론트엔드에서 API를 호출한다. 가령 [GET] /exchange/trading/coin/btcusd 라는 API라고 해보자. 거래소에서 거래를 위해 btc를 usd단위로 하는 코인의 정보를 GET한다는 것이다. (이처럼 uri 설계를 할 때는 굉장히 직관적으로 네이밍을 하는 것이 BEST이다.)
- 그러면 스프링부트에서 coinRestController.java에 해당 uri path를 찾아서 service를 호출하게 됩니다.

[리액트-스프링부트]: ../../../assets/images/post/Develop/react-springBoot.png
