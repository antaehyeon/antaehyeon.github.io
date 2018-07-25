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

## JavaScript - app



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
        this.todoRegisterationBtn = document.getElementsByTagName("button");
        this.todoListParentUlTag = document.getElementsByClassName("todolist")[0];
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

    getTodoInputData() {
        this.todoInputBox.value;
    }

    getTodoListParentUlTag() {
        return this.todoListParentUlTag;
    }

    getTodoRegisterationBtn() {
        return this.todoRegisterationBtn;
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

<br/>

<br/>

## JavaScript - View

> View 역시 Model 의 소개글과 같습니다. 아직 불완전한 코드이니, 맹신하시면 안됩니다-!

View 는 너무 명확했다. `DOM 조작에만 집중` `데이터를 받아 그대로 DOM에 추가` 명확했는데도 구현하기가 약간 까다로웠다.

해당 HTML 코드에서는 버튼을 클릭하면, 입력된 내용이 할일로 추가되는 부분이니 그 할일을 추가하는 부분을 구현하면 되겠다고 생각했다.

```javascript
class TodoView {

    constructor() { }
    
    registerTask(parentNode, childNode) {
        parentNode.appendChild(childNode);
    }
}
```

`registerTask` 라는 메서드를 만들고, 부모노드(parentNode) 와 자식노드(childNode) 를 받아서 부모노드에 추가해주는 `appendChild` 메서드를 사용하였다.

해당 HTML 에서는 **ul태그**가 부모노드가 될 것이고, 새로운 자식노드(li태그)를 만들어서 추가하는 경우가 될 것이다.

여기서 @crong의 피드백은 아래와 같다.

1. view는 진짜 **렌더링에 집중**하는 경우가 많음
2. Controller 를 통해서 데이터를 받아, 화면을 렌더링하는 코드 (현재, 괜춘함) 이나, View 에서 Model을 접근해서 가져오기도 함

<br/>

<br/>

## JavaScript - Controller

Controller 은 처음에 내용을 보고 `관제탑` 같다는 느낌을 받았다. 왜냐하면 `Model` 과 `View` 간 변경사항을 연결하는 것이 주된 목표였기 때문이다. 

근데 처음에는 변경사항을 연결한다는 부분에서 이해를 잘 못했다. 일단은 버튼에 클릭이벤트를 장착하고 Model 과 View 의 메서드를 이용해서 기능을 연결시키는 것 정도로 이해했다.

```javascript
class TodoController {
    constructor(model) {
        this.todoModel = model;
        this.todoRegisterationBtn = model.getTodoRegisterationBtn();
        this.todoRegisterationBtn.onclick = function() {
            const todoModel = new TodoModel();
            const todoView = new TodoView();
            
            const todoListParentUlTag = todoModel.getTodoListParentUlTag();

            const todoInputData = todoModel.getTodoInputData();
            const listItemNode = todoModel.createListItemNode(todoInputData);
    
            todoView.registerTask(todoListParentUlTag, listItemNode);
        }
    }
}
```

@crong 피드백

1. 왜 클릭 이벤트 함수 안에서 model 과 view 를 초기화 하나요?
2. onclick과 addEventListener의 차이점을 찾아볼 것 (onclick은 추천하지 않는 방법이다)
3. controller 가 model 과 view 를 연결해주는 점에서 괜찮게 구현함

여기서 1번은 onclick 으로 등록해주는데, 자꾸 view와 model이 undefined 가 떠서 해결하기 위해 새로 new 를 통해 새로운 객체를 만들어 주었지만, 정말 쓰면 안되는 방법이다. (인자로 model을 받아와 놓고..)

```javascript
/* 1차 리팩토링 */
class TodoController {

    constructor(model, view) {
        this.model = model;
        this.view = view;
        this.registrationBtn = this.view.findElementByTagName("button");
        this.registerEventListener(this.registrationBtn, this.addTodoListData(model, view));
    }

    registerEventListener(node, handler) {
        node.addEventListener("click", this.addTodoListData());
    }

    addTodoListData(model, view) {
        const currentInputData = view.findElementByName("todo").value;
        model.setCurrentInputTodoData(currentInputData);
        const todoItemNode = model.createListItemNode();
        const todoListParentNode = view.findElementByClassName("todolist");
        view.registerTask(todoListParentNode, todoItemNode);
    }
}
```

그리고 나머지 onclick 을 addEventListener 로 대체하는 것으로 마무리 하였다.















































