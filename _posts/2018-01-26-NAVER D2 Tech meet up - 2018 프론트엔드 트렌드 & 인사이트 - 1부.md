---
layout: post
title: "NAVER D2 Tech meet up - 2018 프론트엔드 트렌드 & 인사이트 - 1부"
date: 2018-01-26 17:59:15 +0900
description:  (optional)
img: naver_d2_frontend_0.png # Add image post (optional)
tags: [NAVER, D2, Front-End, Tech meet up] # add tag
---

0. ### 서론

    필자는 세종대학교의 En#에서 활동하고 있습니다. En#은 NAVER D2 CAMPUS 에 속해있는데, 2018년 01월 26일에 **프론트엔드 개발자** 주제로 세미나가 열려서 참석하게 되었습니다. 2018년 부터 프론트엔드 개발자로 첫 걸음을 내딛는 과정을 진행중인데, 현재까지도 많은 시행착오도 있고 아직까지 모르는것도 많은 상태입니다. 그래서 네이버에서 직접 일하는 프론트엔드 개발자 분들의 세미나를 들어 볼 수 있는 기회가 너무 좋았고, 세미나 내용과 네트워킹 시간 때 느낀점을 공유해보도록 하겠습니다.

    > 아직 미완성된 글입니다. 해당 발표자료가 올라오면 사진자료를 포함한 글로 바꿀 계획입니다.

1. ### NAVER D2

   ---

   <p align="center"><b> FOR DEVELOPERS, BY DEVELOPERS </b></p>

   ---

   네이버에서 진행하는 개발자를 위한 지원사업(?) 입니다. [홈페이지](http://d2.naver.com/home)를 방문하시면 더 많은 정보를 얻을 수 있습니다. 그리고 **대학생을 지원**해주는 `D2 CAMPUS` 가 있습니다. 여기서 대학생들을 위한 [지원사업](https://developers.naver.com/d2/d2campus/)이 굉장합니다. 자세한 내용은 링크를 클릭하시면 됩니다.

   > 대학생이고, 학술동아리라면 신청해서 좋은 혜택들을 많이 누리세요 :)
   >
   > 일반 커뮤니티도 지원합니다! 하지만 대학생 동아리보다 활동이 꾸준하게 이어지지 않아서 중단된 커뮤니티도 많다고 합니다!

2. ### 2018 프론트엔드 트렌드 & 인사이트

   ---

   <p align="center"><b> 2018 프론트엔드 트렌드 & 인사이트 </b><br> 네이버 김태훈 @ Engineering Growth<br> @ MTS : Member of Techincal Staff<br> 페이스북 프론트엔드 개발그룹 운영진</p>

   ---

   - ### ES8 (ECMA-262 2017) 이 출시되었습니다 ! ECMAScript 2017 (제8판) 이며, 현재 진행중인 작업입니다.

     - 새로운 기능을 살펴보자면
       - String Padding
       - Object.value
       - Object.entries
       - Object.getOwnPropertyDescriptors
       - Trailing commas
       - Async functions
     - 정도가 있습니다. 해당 기능에 대한 내용은 추후 추가할 예정입니다.

   - ### Progressive Web APPs

     - Google 에서 미치도록 밀고 있는 기술

     - 웹의 장점과 앱의 장점을 결합한 환경

     - 설치가 필요 없음

       - 홈 화면에 아이콘으로 제공

     - 느린 네트워크에서도 빠르게 로딩됨

     - 앱이 아닌데도 웹 레벨에서 Push 알림 가능

     - **사용자가 브라우저를 통해서 앱의 경험을 그대로 받는 것이 목표**

     - ### 특징

       - Progressive : 어떤 브라우저에서든 모든 사용자에게 적합함

       - 반응형 : 데스크탑, 모바일, 태블릿 모든 폼 팩터에 맞음

       - 연결 독립적 : Service Worker 를 통해 불안정한 네트워크에서도 동일하게 동작

         > Service Worker : 간단하게 진화된 Cache Client/Server 라고 보면 됩니다.<br>중간에서 데이터통신을 대신 해주거나, 대신 받아와서 뿌려줍니다.<br>단 Cache와 성격이 비슷하지만 진보적인 (기능이 더 많고 확장가능한) 백그라운드 서비스 입니다.

       - 앱과 유사함 : 앱 스타일(상호작용 및 탐색)의 경험을 사용자에게 제공

       - 최신 상태 : Service Worker을 통해서 항상 최신상태를 유지할 수 있음

       - 안전 : HTTPS

       - 검색 가능 : W3C와 Manifest, Service Worker로 인해서 검색엔진에서 제공됨

         > 즉, 웹 앱 구분없이 검색됩니다. (홍보효과 극대화)

       - 재참여 가능 : Service Worker을 통해서 Push 알림기능이 가능하기 때문에 앱처럼 재접속이 가능

       - 설치 가능 : 앱 스토어에서 복잡하게 받을 필요 없이, 바로 설치 가능함

       - 링크 연결 가능 : URL을 통해서 간단하게 공유할 수 있으며, 불필요한 설치작업 필요 없음

     - ### 누가 썼는가?

       - Twitter : 이미 2017 년 부터 PWA 기반의 [Twitter Lite](https://blog.twitter.com/en_us/topics/product/2017/introducing-twitter-lite.html) 출시
       - Trivago : 다음 세대의 필수적인 기술이라며 준비중 ([링크](https://www.thinkwithgoogle.com/intl/en-gb/consumer-insights/trivago-embrace-progressive-web-apps-as-the-future-of-mobile/))
       - Google : 이미 이에 대한 기술 개발이 매우 활발적임
       - Apple : 얘네 때문에 Google이 미치도록 개발하는 중
       - Samsung.. 나머지 대기업들도 이미 착수중

   - ### AMP (Accelerated Mobile Pages) on Google

     [AMP JS](https://www.ampproject.org/ko/)

     - AMP가 제공하는 컴포넌트를 사용하면

     - **뛰어난 퍼포먼스** 제공 보장

     - 예를들어, 웹에서 JavaScript로 구현해야 할 기능들을

     - 간단한 **HTML 형식 태그**로 사용 가능

     - **커스텀 엘리먼트** 사용

       - HTML 요소도 물론 사용 가능

     - AMP를 이용해서 만든 페이지는

       - **Google CDN에 저장**
         - CDN에 직접적으로 저장하려면 비용이 기하급수적으로 증가
         - 전 세계에 위치해 있는 CDN 에 저장되는 기회
         - 어떤나라에서든 구글에서 클릭 시 **딜레이 없음** (CDN에 저장되어 있기 때문에)

     - EX> AMP-CAROUSEL

       > 네이버 웹툰같이 사진 옆으로 넘기는 기능

       - JavaScript로 구현하려면 꽤나 힘든 작업이지만

       ```html
         <amp-carousel height="300" layout="fixed-height" type="carousel">
           <amp-img src="/img/image1.jpg" width="400" height="300" alt="a sample image"></amp-img>
           <amp-img src="/img/image2.jpg" width="400" height="300" alt="another sample image"></amp-img>
           <amp-img src="/img/image3.jpg" width="400" height="300" alt="and another sample image"></amp-img>
         </amp-carousel>
       ```

       - AMP-CAROUSEL 쓰면 위의 코드로 바로 구현 가능
       - 까놓고 말하면
       - 너네가 JS로 짜도 우리만큼의 성능 안나올꺼 암
       - 그냥 우리꺼 써
       - 우리가 웹 컴포넌트 형식으로 굉장히 쉽게 사용해줄 수 있도록 제공해주고 있어
       - 코드 내부 자체를 3개월동안 분석 (네이버 김태훈님)
         - 코드 자체가 **극 퍼포먼스 위주**
           - 프레임 자체가 60fps 아래로 떨어지질 않음
       - [GDG DevFest Seoul 2016 - AMP는 어떻게 웹 페이지의 성능을 높일 수 있나?](https://www.youtube.com/watch?v=e6slMlFgdCQ&feature=youtu.be)

     - ### AMP NEXT

       - **1년동안 굉장한 성공**을 보임
       - 86만여개 도메인, 17억개의 AMP 페이지 생성
       - 매주 3500만개의 AMP가 생성됨
       - PWA를 결합하기 위한 시도를 펼치고 있음
       - 컴포넌트 방식 혹은 iframe / shadow DOM
       - 혹시 시작해보고 싶다면 [AMP Start](https://ampstart.com/)
       - 배우고 싶다면 [Learn AMP by Example](https://ampbyexample.com/)

   - ### WebAssembly

     > 현대 웹브라우저에서 동작하는 새로운 형식의 코드<br>네이티브에 가까운 성능으로 동작<br>C/C++ 같은 저수준 어셈블리 언어를 웹에서 돌릴 수 있음<br>동시에 JavaScript도 동작 가능(서로 보완)

     - C와 C++이 지원된다면

     - 이전까지는 웹에서 돌려볼 수 없던 클라이언트 앱들을

     - 동작시킬 수 있게 만들 수 있음

     - 그리고 WebAssembly 가 **모듈로 제공**될 것이기 때문에

     - JavaScript와 **공생하는 관계**를 가지는 것

     - **웹 어셈블리의 (네이티브적 고성능) 특징 + 자바스크립트의 유연함**

     - ### **더 중요한건**

     - [W3C 웹 어셈블리 커뮤니티 그룹](https://www.w3.org/community/webassembly/)에서 `웹 표준으로 개발`되고 있음

     - 표준으로 자리잡히면, **성능 폭이 한번 더 크게 뛸 것**임

     - ### 웹 극 전성기!!

       > 직접 체험해보고 싶다면<br>http://webassembly.org/demo/

3. ### 참고

   - [MDN web docs](https://developer.mozilla.org/ko/docs/Web/JavaScript/%EC%96%B8%EC%96%B4_%EB%A6%AC%EC%86%8C%EC%8A%A4)
   - [ES8 New Feature](https://hackernoon.com/es8-was-released-and-here-are-its-main-new-features-ee9c394adf66)
   - [Progressive Web Apps](https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/?hl=ko)
   - [Service Worker](https://developers.google.com/web/fundamentals/primers/service-workers/?hl=ko)
   - [AMP on Google](https://developers.google.com/amp/)
   - [WebAssembly](https://developer.mozilla.org/ko/docs/WebAssembly)

   ​

