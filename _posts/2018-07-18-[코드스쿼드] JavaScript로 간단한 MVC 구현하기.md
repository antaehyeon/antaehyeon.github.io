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

## 파일을 나눠보자

일단 파일을 좀 나눠보았다. 

- app.js : model, view, controller 을 관리하기 위한 main 의 개념정도로 생각했다
- model.js
- view.js
- controller.js

나머지는 [여기](https://antaehyeon.github.io/devlog/2018/07/14/%EC%BD%94%EB%93%9C%EC%8A%A4%EC%BF%BC%EB%93%9C-MV%EC%97%AD%ED%95%A0%EB%82%98%EB%88%84%EA%B8%B0/) 에서 배운대로 구현하기 위해서 나눴다.

<br/>

<br/>

## JavaScript - Model

> 일단 현재 구현되어 있는 Model 은 완전히 틀린 개념입니다. 멘토한테 피드백을 통해서 올바른 Model 로 고쳐나갈 예정입니다. 해당 메뉴에서는 필자가 어떤식으로 구현하였는지에 대한 관점으로 지켜보시면 됩니다.

맨 처음에 Model 을 보고 `어떻게 구현해야 겠다` 라는 관점을 맞춘 곳은 `갱신` `추가` `변경` `제거` `획득` 중 **획득** 이였다.

Document 에서 querySelector 이나 getElement 메서드를 이용해서 **node를 획득** 하는 것인 줄 알았다.

```javascript
/* Model 에 대해 완전히 틀린 코드이므로, 주의하시기 바랍니다 */
class TodoModel {

    constructor() {
        this.todoInputBox = document.getElementsByName("todo")[0];
        this.registerationTodoData = document.getElementsByTagName("button");
        this.todoListParentUlTag = document.getElementsByClassName("todolist")[0];
    }

    registerTask(todoData) {
        const todoListItemNode = this.createListItemNode(todoData);
        this.todoListParentUlTag.appendChild(todoListItemNode);
    }

    createListItemNode(textData) {
        const listItemNode = document.createElement("li");
        const textNode = document.createTextNode(textData);
        listItemNode.appendChild(textNode);

        return listItemNode;
    }

    getTodoInputBox() {
        return this.todoInputBox;
    }

    getTodoListParentUlTag() {
        return this.todoListParentUlTag;
    }

}
```

그래서 위와 같이 생성자 부분에서 document 를 이용해 노드들을 **획득** 했다고 생각했다. ListItem 을 만들 노드들을 생성하는 **추가** 작업도 있고, 꽤 괜찮게 구현했다고 생각했다 **(하지만 완전틀림)**

여기서 멘토의 피드백을 받았다.

1. Model 이라는 것이 **DOM node 를 뜻하는 것이 절대 아님** (절대절대절대)
2. Model 의 데이터는 DOM 에 있는 것을 찾는게 아니고 **자료구조**로 가지고 있는 것
3. 당장 화면에 보여지지 않는 데이터까지 가지고 있는것이 Model ? (당장화면에 보여지지 않는 데이터까지 모두 다 화면에 존재하지 않을테니까요.)
  Ex > this.todolist = [];

그렇다. Model 은 **DOM 노드** 를 뜻하는 것이 아니고, **자료구조** 로 가지고 있는 것이다. 그래서 아래와 같이 리팩토링을 진행했다.

```javascript
/* 1차 리팩토링 */
class TodoModel {

    constructor() {
        this.currentInputTodoData;
        this.todoList = [];
    }

    getCurrentInputTodoData() {
        return this.todoInputData;
    }

    setCurrentInputTodoData(data) {
        this.todoInputData = data;
    }

    getTodoList() {
        return this.todoList;
    }

    pushTodoListData(data) {
        this.todoList.push(data);
    }

    createListItemNode() {
        const listItemNode = document.createElement("li");
        const textNode = document.createTextNode(this.getCurrentInputTodoData());
        listItemNode.appendChild(textNode);

        return listItemNode;
    }
}
```

현재는 @crong 의 피드백을 기다리고 있는중...















































