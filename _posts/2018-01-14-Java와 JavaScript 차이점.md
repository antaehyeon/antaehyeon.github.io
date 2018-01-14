---
layout: post
title: "Java와 JavaScript의 차이점"
date: 2018-01-14 16:00:00 +0900
description: Java와 JavaScript의 차이점 (optional)
img: java_javascript_0.png # Add image post (optional)
tags: [Java, JavaScript, 차이점] # add tag
---

0. ### 서론

    안녕하세요. 오늘은 Java와 JavaScript의 차이점에 대해서 글을 작성해보려고 합니다. 저도 처음에는 Java 라는 단어때문에 Java와 JavaScript가 Java 기반으로 만들어진 언어인 줄 알았습니다. 근데 정말 큰 착각이였습니다. 비슷하긴 해요. JavaScript 는 Java와 비슷한 구문이 있지만 두 언어 모두 **C 언어의 기본 구문에 바탕을 두고 개발이 된 언어**입니다. 나라로 들자면 인도와 인도네시아 정도로 비교할 수 있겠네요.

    ![Start]({{site.baseurl}}/assets/img/java_javascript_2.png)

    > 인도와 인도네시아는 다른 나라입니다 !

1. ### Java

   Java는 썬 마이크로시스템즈에서 1995년 5월 23일에 발표된 언어입니다. 현재는 웹 애플리케이션 개발에 가장많이 사용하는 언어죠. 폭발적인 인기를 끌었던 이유는 자바로 개발된 애플리케이션은 **어느 플랫폼에서나 동일한 형태로 실행될 수 있었기 때문**이죠. 단, 느립니다.

   > JVM (Java Virtual Machine), 자바 가상머신

2. ### JavaScript

   JavaScript는 넷스케이프 커뮤니케이션즈 사에서 1995년 12월 4일에 발표된 언어입니다. 초반에는 Mocha 라는 이름으로 발표되었고 이후 LiveScript 로 변경되었지만 최종적으로는 JavaScript 로 이름이 변경되었습니다. 현재는 **웹 브라우저에서 주로 사용**되며, **서버 사이드 네트워크 프로그래밍(예: Node JS)**에서도 사용되고 있습니다.

   ![Start]({{site.baseurl}}/assets/img/java_javascript_1.png)

   웹 애플리케이션이 큰 인기를 끌면서 이에 적합한 JavaScript 가 2017년 기준으로 **Programming 언어 중 1위**를 기록하고 있습니다.

3. ### 차이점

   |          | Java                               | JavaScript                       |
   | -------- | ---------------------------------- | -------------------------------- |
   | 언어 Type  | 객체 지향적 프로그래밍 언어                    | 객체 지향 **스크립트** 프로그래밍 언어          |
   | Typing   | **정적** 형 지정 (Static Typing)        | **동적** 형 지정 (dynamic Typing)     |
   | Checking | **강한** 형 검사 (Strong Type Checking) | **약한** 형 검사 (Weak Type Checking) |

   - ### 언어 Type

     - ### Java

       Java 는 객체 지향적 언어 즉, `OOP 프로그래밍` 언어입니다. **가상 시스템** 또는 **브라우저에서 실행되는 응용프로그램**을 작성합니다. 그래서 오로지 클래스와 메소드로만 이루어져 있습니다. 계층구조(상속) 또한 명확하죠.

     - ### JavaScript

       JavaScript 는 `OOP 스크립팅 언어` 입니다. 해당 코드는 **브라우저에서만 작동**합니다. 쉬운 구문과 최소한의 사항만을 요구합니다.

   - ### Typing

     - ### Java

       Java 는 변수를 선언할 때 **int, String** 등등 `정적(Static)인 형태`로 지정됩니다.

     - ### JavaScript

       JavaScript는 변수는 물론 함수까지도 `var` 에 전부 담을 수 있습니다. `동적(dynamic)` 하죠.

   - ### Checking

     - ### Java

       변수부터 이미 Type이 지정되어 있어서, **검사가 조금 빡셉니다.** 그만큼 `안전(Safe)` 하다는 특성을 가지고 있죠.

     - ### JavaScript

       Java에 비해서 굉장히 자유롭습니다. 약간의 단점은 너무 자유로워서 에러가 어디서 났다는 것을 정확하게 알려주지 않을 때도 있습니다. (윾)

4. ### 결론

   이제 Java와 JavaScript의 차이점에 대해서 약간 이해가 가셨나요? 블로그에 글을 작성할 때에 최대한 객관적인 정보를 제공하기 위해서 많이 찾다보니 제가 몰랐던 사실도 알게되는 뜻 깊은 시간인 것 같습니다. 앞으로도 하루에 하나씩 써보는 것을 목표로 정해보려고 합니다. 감사합니다.

   > 아 ! 만약 틀린 정보가 있다면 댓글로 꼭 남겨주세요 ! 부탁드립니다 !

5. ### 기타

   > 역시 출처를 적습니다.

   - [JavaScript - 나무위키](https://namu.wiki/w/JavaScript)
   - [Java vs JavaScript](https://www.upwork.com/hiring/development/java-vs-javascript/)
   - [JavaScript - Wiki](https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8)
   - [Java - Wiki](https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94_(%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D_%EC%96%B8%EC%96%B4))
   - [JavaScript 소개](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/%EC%86%8C%EA%B0%9C)
   - [Java와 JavaScript의 다른 점은 무엇입니까?](https://www.java.com/ko/download/faq/java_javascript.xml)
   - [What does it mean that JavaScript is "dynamic"?](https://stackoverflow.com/questions/32476680/what-does-it-mean-that-javascript-is-dynamic)
   - [JAVA와 JAVASCRIPT의 차이점은 ?](http://blog.wishket.com/java%EC%99%80-javascript%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90%EC%9D%80-2/)

