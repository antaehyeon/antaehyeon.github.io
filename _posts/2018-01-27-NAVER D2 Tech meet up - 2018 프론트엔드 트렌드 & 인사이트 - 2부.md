---
layout: post
title: "NAVER D2 Tech meet up - 2018 프론트엔드 트렌드 & 인사이트 - 2부"
date: 2018-01-27 17:59:15 +0900
description:  (optional)
img: naver_d2_frontend_1.png # Add image post (optional)
tags: [NAVER, D2, Front-End, Tech meet up] # add tag
---

###1. 2018 프론트엔드 트렌드 & 인사이트

---

   <p align="center"><b> 2018 프론트엔드 트렌드 & 인사이트 </b><br> 네이버 김태훈 @ Engineering Growth<br> @ MTS : Member of Techincal Staff<br> 페이스북 프론트엔드 개발그룹 운영진</p>

<p align="center"><b> 당신이 스마트폰으로 주로 사용하는 앱은 손가락 안에 꼽을겁니다. </b><br><b>수익성은 앱이 아닌 웹에서 날 수 밖에 없고, 웹의 전성기는 아직입니다</b></p>

---

   - ### WebAssembly

     > 현대 웹브라우저에서 동작하는 새로운 형식의 코드<br>네이티브에 가까운 성능으로 동작<br>C/C++ 같은 저수준 어셈블리 언어를 웹에서 돌릴 수 있음<br>동시에 JavaScript도 동작 가능(서로 보완)

     - C와 C++이 지원된다면

     - 이전까지는 웹에서 돌려볼 수 없던 클라이언트 앱들을

     - 동작시킬 수 있게 만들 수 있음

     - 그리고 WebAssembly 가 **모듈로 제공**될 것이기 때문에

     - JavaScript와 **공생하는 관계**를 가지는 것

     - **웹 어셈블리의 (네이티브적 고성능) 특징 + 자바스크립트의 유연함**

     - **더 중요한건**

     - [W3C 웹 어셈블리 커뮤니티 그룹](https://www.w3.org/community/webassembly/)에서 `웹 표준으로 개발`되고 있음

     - 표준으로 자리잡히면, **성능 폭이 한번 더 크게 뛸 것**임

     - **웹 극 전성기!!**

       > 직접 체험해보고 싶다면<br>http://webassembly.org/demo/


   - ### FE Frameworks

     > 항상 흥미로운 주제입니다. 필자도 아직 프론트엔드를 접한지 갓 1달도 채 되지 않아서,<br>이에 대한 주제는 심오하게 다뤄볼 예정입니다.<br>여기서는 강연때 들은 키워드 위주로 작성해보겠습니다.

     ![](https://i.imgur.com/yJzk3vO.png)

     - 선택 포인트
       - React
         - Redux 짱
       - Angular
         - TypeScript(새 언어) 배워야 함
         - 처음에 진입하기 매우 어려움
         - RxJava, RSX
         - 이거 견뎌내고 익숙해지면
           - 엄청난 생산성
           - 엄청 아름다운 코드
       - Vue Js
         - 쉽게 접근할 수 있음
       - 각 프레임워크의 퍼포먼스는 이미 다 일정 수준 올라왔고(모두 빠름)
       - 다양한 도구들을 통해서 최적화가 가능함
       - **각 프레임워크의 컨셉을 파악**하고
         - Vue 같은 경우에는 아직까지 대규모 프로젝트에는 어울리지 않음
       - **프로젝트에 맞게 선택할 것**

- ### Payment Request API

  ![](https://i.imgur.com/8DR511j.gif)

  - 구글에서 만든 결제 API (서비스 가능하나 현재도 개발 진행중)
    - 브라우저가 판매자, 사용자 및 결제 방법 사이에서 중재자 역할을 하도록 지원
    - 결제 커뮤니케이션 흐름을 최대한 표준화
    - 다양한 보안 결제 방법을 원활하게 지원
  - 웹에서 바로 결제가 가능
    - 모든 브라우저, 기기 또는 플랫폼(모바일 또는 기타)에서 작동

- ### Machine Learning for FE

  ![](https://i.imgur.com/oT1yUUM.gif)

  > https://harthur.github.io/kittydar/
  >
  > https://deeplearnjs.org/

  - 브라우저에서 GL을 이용해서 **머신러닝을 구현**
    - 서버로 통신하는 개념이 아님
    - **웹 브라우저 자체에서 구동**
  - 아이디어
    - 추후 사용자의 환경 (왼손 스크롤링, 오른손 스크롤링) 에 따른 웹 규격을 변경
  - 기술
    - WEB GL
      - 그래픽 연산작업 처럼 속이며, GPU를 사용
    - WEBGUP API (Safari only)
      - Mac 계열에서 바로 GPU를 사용할 수 있게끔 제공

- ### [NAVER egjs 2.0](http://naver.github.io/egjs/)

  > 네이버의 노하우가 축적된 모던 웹 라이브러리<br>UI interactions, Effects, Utility 등으로 구성<br>jQuery의 의존성을 버림

  ![](https://i.imgur.com/XWVP6hS.gif)

  ![](https://i.imgur.com/aSfwOPy.gif)

  ​	이외에도 엄청 많음 !

- ### [billboard.js](https://naver.github.io/billboard.js/)

  ![](https://i.imgur.com/LtyOoWU.gif)

  > 차트를 이용하는 가장 쉬운 방법<br>By NAVER GitHub.io

2. ### 참고

   - [MDN web docs](https://developer.mozilla.org/ko/docs/Web/JavaScript/%EC%96%B8%EC%96%B4_%EB%A6%AC%EC%86%8C%EC%8A%A4)
   - [ES8 New Feature](https://hackernoon.com/es8-was-released-and-here-are-its-main-new-features-ee9c394adf66)
   - [Progressive Web Apps](https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/?hl=ko)
   - [Service Worker](https://developers.google.com/web/fundamentals/primers/service-workers/?hl=ko)
   - [AMP on Google](https://developers.google.com/amp/)
   - [WebAssembly](https://developer.mozilla.org/ko/docs/WebAssembly)

   ​

