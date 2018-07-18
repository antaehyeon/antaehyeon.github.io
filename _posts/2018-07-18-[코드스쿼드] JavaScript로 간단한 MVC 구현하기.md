---
layout: post
title:  "[코드스쿼드] JavaScript 로 간단한 MVC 모델 구현하기"
subtitle:   "코드스쿼드"
categories: devlog
tags: HTMLCSS
comments: true
---

> 코드스쿼드에서  HTML 을 배우는 과정 중 JavaScript 로 간단한 MVC를 구현하는 법을 기록한 글입니다

# MVC

이번 코드스쿼드 레벨3 과정 중 MV* 에 대한 개념과 실습을 배우는 부분이 있었다. 뭐 개발자라면 한번씩 다 들었을 정도로 유명한 개념인 것 같다. 하지만 본인은 정작 구현해본 적이 없어서 특별히 뭐가 좋은지 안좋은지 모르고 있었다. Model-View-Controller 로 분리해서 구현하는 정도(?) 만 알고있었던지라 여기서 굉장히 많은 난항을 겪었다. 동시에 값진 경험을 얻기도 해서 이것을 까먹지 않기 위해서 글을 작성한다.

그래서 해당 글에서 프론트엔드 과정을 진행하면서 HTML과 JavaScript 로 간단한 MVC 예제를 구현하는 과정과 여기서의 이슈사항들을 기록해보려고 한다.

만약에 MV 부분에 대해서 잘 모르겠다면 [이글](https://antaehyeon.github.io/devlog/2018/07/14/%EC%BD%94%EB%93%9C%EC%8A%A4%EC%BF%BC%EB%93%9C-MV%EC%97%AD%ED%95%A0%EB%82%98%EB%88%84%EA%B8%B0/) 을 참고하면 좋을 것이다.

