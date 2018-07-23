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

<br/>

<br/>

## base HTML Code

```html
할일입력 <input type="text" name="todo">
<button>등록</button>
    
<h4>해야할 일들</h4>
<ul class="todolist"></ul>
```

body 부분만 캡쳐한 코드이다. 각자 HTML을 구성해서 body 태그 안에 넣어주면 된다. 간단한 코드라서 바로 해석이 될수도 있겠다.

할일을 입력받는 input 태그가 존재하며 등록버튼을 누르면 해야할 일들에 추가되는 것을 구현할 것이다.

<br/>

<br/>

## JavaScript - Model

> 일단 현재 구현되어 있는 Model 은 완전히 틀린 개념입니다. 멘토한테 피드백을 통해서 올바른 Model 로 고쳐나갈 예정입니다. 해당 메뉴에서는 필자가 어떤식으로 구현하였는지에 대한 관점으로 지켜보시면 됩니다.















































