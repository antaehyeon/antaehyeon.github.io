---
layout: post
title: "생활코딩 JavaScript(nodejs) 정리본"
date: 2018-01-21 22:15:00 +0900
description: 생활코딩 JavaScript(nodejs) 정리본입니다. (optional)
img: nodejs_0.png # Add image post (optional)
tags: [] # add tag
---

0. ### 서론

     맨 처음에 프론트엔드 개발자는 단순히 HTML, CSS, JS 를 기본으로만 하면 되는줄 알았습니다. 하지만, 백엔드의 개념도 가지고 있어야 하고(어느정도의 구현까지는) JavaScript 기반으로 된 언어 및 프레임워크가 너무 많아서 각 FrameWork에 대한 개념 task runner, Module Loader/Bundler, Testing 등 알아야 할것들이 너무 많았습니다. 

     그 과정 중 JavaScript를 기반으로 만들어진 node js. 즉, 백엔드를 배우기 위하여 생활코딩 이고잉님의 JavaScript(nodejs) 강의를 전부 수강하였습니다. 그 과정중 정리한 내용을 공유합니다.

     ---

     [생활코딩 중 JavaScript (nodejs) 수강](https://opentutorials.org/course/2136)

     - [서버 측 자바스크립트와 nodejs 소개](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EC%99%80%20nodejs%20%EC%86%8C%EA%B0%9C.md)
     - nodejs 설치 및 실행
       - [설치](https://www.youtube.com/watch?v=60zErcCmBfM)
       - [실행](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%8B%A4%ED%96%89.md)
     - 간단한 웹 에플리케이션 만들기
       - [간단한 웹앱 만들기 1 : 실행](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EC%9B%B9%EC%95%B1%20%EB%A7%8C%EB%93%A4%EA%B8%B0%201%20:%20%EC%8B%A4%ED%96%89.md)
       - [간단한 웹앱 만들기 2 : 인터넷의 동작방법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EC%9B%B9%EC%95%B1%20%EB%A7%8C%EB%93%A4%EA%B8%B0%202%20:%20%EC%9D%B8%ED%84%B0%EB%84%B7%EC%9D%98%20%EB%8F%99%EC%9E%91%EB%B0%A9%EB%B2%95.md)
       - [간단한 웹앱 만들기 3 : 정리](https://www.youtube.com/watch?v=MZAzeKVMMp0)
     - 모듈과 NPM
       - [모듈 1 : 기초](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EB%AA%A8%EB%93%88%201%20:%20%EA%B8%B0%EC%B4%88.md)
       - [모듈 2 : NPM 소개](https://opentutorials.org/course/2136/11854)
       - [모듈 3 : NPM 독립적인 앱 설치](https://opentutorials.org/course/2136/11854)
       - [모듈 4 : npm으로 모듈설치](https://opentutorials.org/course/2136/11854)
     - [콜백(callback) 함수](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%BD%9C%EB%B0%B1(callback)%20%ED%95%A8%EC%88%98.md)
     - [동기와 비동기 프로그래밍](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EB%8F%99%EA%B8%B0%EC%99%80%20%EB%B9%84%EB%8F%99%EA%B8%B0%20%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D.md)
     - Express
       - [도입](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20Express-1.md)
       - [설치](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20Express-1.md)
       - [간단한 웹앱 만들기](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20Express-1.md)
     - 연결성
     - Express
       - [정적 파일을 서비스 하는 법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20Express-2.md)
       - [웹페이지를 표현하는 방법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20Express-2.md)
       - 템플릿 엔진 (Jade)
         - [소개](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%85%9C%ED%94%8C%EB%A6%BF%20%EC%97%94%EC%A7%84%20(Jade).md)
         - [사용법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%85%9C%ED%94%8C%EB%A6%BF%20%EC%97%94%EC%A7%84%20(Jade).md)
         - [Jade의 문법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%85%9C%ED%94%8C%EB%A6%BF%20%EC%97%94%EC%A7%84%20(Jade).md)
       - URL을 이용한 정보의 전달
         - [쿼리 스트링이란?](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20URL%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC.md)
         - [Express의 query 객체의 사용](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20URL%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC.md)
         - [query 객체의 활용](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20URL%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC.md)
         - [의미론적인 URL (semantic url)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20URL%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC.md)
       - POST 방식을 이용한 정보의 전달
         - [POST 방식을 이용한 정보의 전달 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20POST%20%EB%B0%A9%EC%8B%9D%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC%201.md)
         - [POST 방식을 이용한 정보의 전달 2 : form](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20POST%20%EB%B0%A9%EC%8B%9D%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC%202%20-%20form.md)
         - [POST 방식을 이용한 정보의 전달 3 : POST](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20POST%20%EB%B0%A9%EC%8B%9D%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC%203%20-%20POST.md)
         - [POST 방식을 이용한 정보의 전달 4 : GET과 POST의 용도](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20POST%20%EB%B0%A9%EC%8B%9D%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EC%A0%95%EB%B3%B4%EC%9D%98%20%EC%A0%84%EB%8B%AC%204%20-%20GET%EA%B3%BC%20POST%20%EC%9A%A9%EB%8F%84.md)
     - [팁 - Nodejs를 자동으로 재시작](https://opentutorials.org/course/2136/11951)
     - 웹 애플리케이션 제작
       - [오리엔테이션](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%9B%B9%20%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98%20%EC%A0%9C%EC%9E%91%201%2C2%2C3.md)
       - [라우팅](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%9B%B9%20%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98%20%EC%A0%9C%EC%9E%91%201%2C2%2C3.md)
       - [본문 저장](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%9B%B9%20%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98%20%EC%A0%9C%EC%9E%91%201%2C2%2C3.md)
       - [글 목록 만들기](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%204%20-%20%EA%B8%80%20%EB%AA%A9%EB%A1%9D%20%EB%A7%8C%EB%93%A4%EA%B8%B0.md)
       - [본문 읽기](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%205%20-%20%EB%B3%B8%EB%AC%B8%20%EC%9D%BD%EA%B8%B0.md)
       - [코드의 개선](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%206%20-%20%EC%BD%94%EB%93%9C%EC%9D%98%20%EA%B0%9C%EC%84%A0.md)
     - 파일 업로드
       - [소개 및 준비](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%8C%8C%EC%9D%BC%20%EC%97%85%EB%A1%9C%EB%93%9C.md)
       - [업로드 폼](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%8C%8C%EC%9D%BC%20%EC%97%85%EB%A1%9C%EB%93%9C.md)
       - [multer 사용법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%8C%8C%EC%9D%BC%20%EC%97%85%EB%A1%9C%EB%93%9C.md)
       - [multer 심화](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/%EC%84%9C%EB%B2%84%20%EC%B8%A1%20JS%20-%20%ED%8C%8C%EC%9D%BC%20%EC%97%85%EB%A1%9C%EB%93%9C.md)
     - 데이터베이스
       - OrientDB로 웹앱 제작
         - [소개](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%201.md)
         - [설치](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%202%2C%203.md)
         - [기본 사용법](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%202%2C%203.md)
         - [orient js 설정](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%204.md)
         - [SELECT](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%205%2C%206.md)
         - [INSERT & UPDATE & DELETE](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%205%2C%206.md)
       - OrientDB로 웹앱 제작
         - [구현 계획](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%207%2C%208.md)
         - [읽기 1 - 글목록](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%207%2C%208.md)
         - [읽기 2 - 상세보기](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%209.md)
         - [글추가](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Orientdb%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%2010.md)
         - [글 편집 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Orientdb%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%2011%2C%2012.md)
         - [글 편집 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Orientdb%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%2011%2C%2012.md)
         - [글 삭제](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/OrientDB%EB%A1%9C%20%EC%9B%B9%EC%95%B1%20%EC%A0%9C%EC%9E%91%20-%2013.md)
       - MySQL 소개 및 기본 사용법
         - [MySQL 소개](https://opentutorials.org/course/2136/12020)
         - [MySQL 설치 - 맥 (OSX)](https://opentutorials.org/course/2136/12020)
         - [MySQL 구조](https://opentutorials.org/course/2136/12020)
         - [MySQL 사용하기](https://opentutorials.org/course/2136/12020)
         - [MySQL - UPDATE & DELETE](https://opentutorials.org/course/2136/12020)
         - [node-mysql 1 : 접속](https://opentutorials.org/course/2136/12020)
         - [node-mysql 2 : SELECT & INSERT](https://opentutorials.org/course/2136/12020)
         - [node-mysql 3 : UPDATE & DELETE](https://opentutorials.org/course/2136/12020)
       - MySQL로 웹 애플리케이션 구현
         - [글 목록](https://opentutorials.org/course/2136/12021)
         - [글 상세보기 구현](https://opentutorials.org/course/2136/12021)
         - [글 추가기능 구현](https://opentutorials.org/course/2136/12021)
         - [글 편집기능 구현 1](https://opentutorials.org/course/2136/12021)
         - [글 편집기능 구현 2](https://opentutorials.org/course/2136/12021)
         - [글 삭제 구현](https://opentutorials.org/course/2136/12021)
     - [HTTP](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/HTTP.md)
     - cookie1
       - [intro](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/cookie%201%20:%20intro.md)
       - [counter](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/cookie%202%20%3A%20counter.md)
     - cookie2
       - [shopping cart 1](https://github.com/antaehyeon/WinterVacation_Project/tree/master/README/cookie%203%20%3A%20shopping%20cart%201.md)
       - [shopping cart 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/cookie%204%20:%20shopping%20cart%202.md)
       - [shopping cart 3](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/cookie%205%20:%20shopping%20cart%203.md)
       - [cookie & Security](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/cookie%206%20:%20cookie%20%26%20security.md)
     - Session 1
       - [intro](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%201%20:%20intro.md)
       - [counter 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%202%20:%20counter%201.md)
       - [counter 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%203%20:%20counter%202.md)
     - Session 2
       - [login 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%204%20:%20login%201.md)
       - [login 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%205%20:%20login%202.md)
       - [login 3](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%206%20:%20login%203.md)
       - [login 4](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%207%20:%20login%204.md)
     - Session 3
       - [Session store - file](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%208%20:%20session%20store%20-%20file.md)
       - [Session store - mysql](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%20%2B%20Auth%20:%20orientdb%201.md)
       - [Session store - orientdb](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20session%209%20:%20session%20store%20-%20orientd.md)
     - Multi user (다중 사용자)
       - [intro](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Multi%20user%201%20:%20intro.md)
       - [register](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Multi%20user%202%20:%20register.md)
       - [authentication](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Multi%20user%203.md)
     - Security - Password (비밀번호 보안)
       - [Security Password 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Security%20Password%201.md)
       - [Security Password 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Security%20Password%202.md)
       - [Security Password 3 : salt](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Security%20Password%203:%20salt.md)
       - [Security Password 4 : pbkdf2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Security%20Password%204%20:%20pbkdf2.md)
       - [Security Password 5](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Security%20Password%205.md)
       - [Security Password 6 : register](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Security%20Password%206%20:%20register.md)
     - Passportjs
       - [Passport Introduction (패스포트 소개)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Passportjs%201%20:%20intro.md)
       - [Configuration](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Passportjs%202%20:%20configure.md)
       - [Route](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Passportjs%203%20:%20route.md)
       - [Serialize](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Passportjs%204%20:%20serialize.md)
       - [logout(로그아웃)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Passportjs%205%20-%20logout.md)
       - [review(복습)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Passportjs%206%20:%20review.md)
     - Federation Authentication (타사 인증)
       - [Intro (소개)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Federation%20authentication%201%20:%20intro.md)
       - [Facebook (페이스북 연동)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Federation%20authentication%202%20:%20faceb.md)
       - [Route](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Federation%20authentication%203.md)
       - [login](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Federation%20authentication%204.md)
       - [Facebook permission (페이스북 세부 권한 설정)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Federation%20authentication%205.md)
     - Auth - Orientdb
       - [Intro](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Auth%20orientdb%201.md)
       - [Session store](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Auth%20orientdb%202%20session%20store.md)
       - [Reigster (회원 등록)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Auth%20orientdb%203%20register.md)
       - [login](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Auth%20orientdb%204%20login.md)
       - [federation auth (타사 인증)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Auth%20orientdb%205%20:%20federation.md)
     - Auth - MySQL
       - [Session store](https://opentutorials.org/course/2136/12257)
       - [register](https://opentutorials.org/course/2136/12257)
       - [login](https://opentutorials.org/course/2136/12257)
       - [federation](https://opentutorials.org/course/2136/12257)
     - 정리 정돈의 기술
       - jade - extends
         - [jade extends 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20side%20javascript%20-%20jade%20extends1.md)
         - [Jade extends 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Jade%20extends%202.md)
       - 사용자 정의모듈 만들기
         - [Create module 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Create%20module%201.md)
         - [Create module 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Create%20module%202.md)
       - 라우트 분리하기
         - [Routes separate 1](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Routes%20separate%201.md)
         - [Routes separate 2](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Routes%20separate%202.md)
         - [Routes separate 3](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20Routes%20separate%203.md)
       - 글작성+인증(CRUD+Auth) - MySQL 1
         - [CRUD + Auth - mysql 1 (Auth views)](https://opentutorials.org/course/2136/12488)
         - [CRUD + Auth - mysql 2 (Auth route)](https://opentutorials.org/course/2136/12488)
         - [CRUD + Auth - mysql 3 (Auth config)](https://opentutorials.org/course/2136/12488)
       - 글작성+인증(CRUD+Auth) - MySQL 2
         - [CRUD + Auth - mysql 4 (CRUD views)](https://opentutorials.org/course/2136/12490)
         - [CRUD + Auth - mysql 5 (CRUD route)](https://opentutorials.org/course/2136/12490)
         - [CRUD + Auth - mysql 6](https://opentutorials.org/course/2136/12490)
       - 글작성+인증(CRUD+Auth) - Orient DB 1
         - [CRUD + Auth - Orient DB 1 (Auth views)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%20%2B%20Auth%20:%20orientdb%201.md)
         - [CRUD + Auth - Orient DB 2 (Auth route)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%20%2B%20Auth%20:%20orientdb%202.md)
         - [CRUD + Auth - Orient DB 3 (Auth config)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%20%2B%20Auth%20:%20orientdb%203.md)
       - 글작성+인증(CRUD+Auth) - Orient DB 2
         - [CRUD + Auth - Orient DB 4 (crud views)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%2BAuth%20:%20orientdb%204.md)
         - [CRUD + Auth - Orient DB 5 (Crud routes)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%20%26%20Auth%20:%20orientdb%205.md)
         - [CRUD + Auth - Orient DB 6 (final)](https://github.com/antaehyeon/WinterVacation_Project/blob/master/README/Server%20Side%20JavaScript%20-%20CRUD%20%26%20Auth%20:%20orientdb%206.md)

     ---



1. ### 출처

   - [생활코딩 JavaScript(nodejs) 강의](https://opentutorials.org/course/2136)
   - [WinterVacation Project - GitHub](https://github.com/antaehyeon/WinterVacation_Project)


