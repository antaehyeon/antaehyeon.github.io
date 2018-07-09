---
layout: post
title:  "[코드스쿼드] DOM API & Event"
subtitle:   "코드스쿼드"
categories: devlog
tags: HTMLCSS
comments: true
---

### DOM (Document Object Model)

---

HTML 태그는 실제로 어떠한 node 형태로 저장된다. 이렇게 저장된 정보를 `DOM Tree` 라고 지칭함

즉, HTML element는 Tree형태로 저장됨

![](https://imgur.com/NolOrrM.png)

이렇게 복잡한 DOM tree를 탐색하기 위해서 JavaScript 로 탐색 알고리즘을 구현하는것이 너무 힘든 작업임

그래서, 브라우저에서 DOM(Document Object Model) 개념을 통해서 다양한 DOM API를 제공하고 있음

브라우저의 DOM Tree를 찾고 조작하는 것을 쉽게 도와주는 여러가지 메서드들(DOM API)을 제공함





### 1-1. getElementById()

---

![](https://imgur.com/BbJt1Ow.png)

```html
element = document.getElementById(id); <!-- id는 ""로 지정됨 -->
```

id가 존재하지 않으면, `null` 을 반환함





### 1-2. 다양한 APIs

---

`document` 에서 사용 가능한 API : [The Document Object](https://www.w3schools.com/jsref/dom_obj_document.asp)

`element` 에서 사용 가능한 API : [The Element Object](https://www.w3schools.com/jsref/dom_obj_document.asp)





### 1-3. querySelector()

---

DOM을 찾는데 유용한 메서드임. querySelectorAll() 과 비슷한데, 해당 선택자에 해당하는 모든 요소를 가져옴

반환값은 nodeList 이며, for문 또는 foreach문을 통해서 객체를 반환한다.

```javascript
// querySelector()
element = document.querySelector(selectors);
var el = document.querySelector(".myclass");

// querySelectorAll()
var matches = document.querySelectorAll("p");
var matches = document.querySelectorAll("div.note, div.alert");
var matches = container.querySelectorAll("li[data-active=1]");

// querySelectorAll - forEach
var highlightedItems = userList.querySelectorAll(".highlighted");
highlightedItems.forEach(function(userItem) {
  deleteUser(userItem);
});
```



![](https://imgur.com/le01Lph.png)





### 1-4. DOM 탐색 APIs

---

- [tagName](https://developer.mozilla.org/en-US/docs/Web/API/Element/tagName) : 엘리먼트의 타입이름을 얻을 수 있다.

  XHTML(또는 XML) 타입에서는 **소문자**로 출력되며, `HTML` 에서는 무조건 **대문자**로 출력된다.

  ```HTML
  <span id="born">When I was born...</span>
  ```

  ```javascript
  var span = document.getElementById("born");
  console.log(span.tagName); // "SPAN"
  ```

- [textContent](https://developer.mozilla.org/ko/docs/Web/API/Node/textContent) : 노드와 그 자손의 텍스트 내용을 표시하고, 설정도 가능하다.

  ```javascript
  // <span id="born">HE<span>L</span>LO</span>
  
  console.log(span.textContent); // "HELLO"
  console.log(span.innerHTML); // "HE<span>L</span>LO"
  console.log(span.innerText); // "HELLO"
  ```

  - innerText 와의 차이점
    - textContent 는 <script>와 <style> 요소를 포함한 모든 요소들의 내용을 가져옴. 반면, innerText 는 그렇지 않음
    - innerText 는 style 을 인지하고 숨겨진 요소들의 텍스트를 반환하진 않지만 textContent 는 반환함
    - innerText 는 CSS 스타일링을 인지하기 때문에 레이아웃의 변화를 가져올 수 있지만, textContent는 그렇지 않음
    - innerText 는 요소의 자식노드를 지우는 것 뿐만아니라, 텍스트 노드의 모든 자손을 영구적으로 제거함
  - innerHTML 과의 차이점
    - innerHTML 은 HTML을 반환함
    - textContent가 텍스트를 HTML로 파싱하지 않기 때문에 종종 더 좋은 성능을 보여줌
    - textContent는 XSS 를 방지할 수 있음

- [nodeType](https://developer.mozilla.org/ko/docs/Web/API/Node/nodeType) : `elements` `text` `comments` 처럼 서로 다른 종류의 노드를 구별하는데 사용할 수 있음

  ![](https://imgur.com/U6j3zkl.png)

- [childNodes](https://developer.mozilla.org/ko/docs/Web/API/Node/childNodes) : 주어진 요소의 자식 노드 모음 (collection)을 반환함 (NodeList)

  ```javascript
  // parg는 <p> 요소 개체 참조
  if (parg.hasChildNodes())
  // 그래서, 먼저 개체가 찼는 지(자식 노드가 있는 지) 검사
   {
     var children = parg.childNodes;
     for (var i = 0; i < children.length; i++) 
     {
     // children[i]로 각 자식에 무언가를 함 
     // 주의: 목록은 유효해(live), 자식 추가나 제거는 목록을 바꿈
     };
   };
  ```

- [firstChild](https://developer.mozilla.org/ko/docs/Web/API/Node/firstChild) : 트리에서 노드의 첫 번째 자식이나 null(노드가 자식이 없으면)을 반환함

  ```javascript
  <p id="para-01">
    <span>First span</span>
  </p>
  
  <script type="text/javascript">
    var p01 = document.getElementById('para-01');
    alert(p01.firstChild.nodeName)
  </script>
  ```

- [firstElementChild](https://developer.mozilla.org/en-US/docs/Web/API/ParentNode/firstElementChild)

  ```html
  <ul id="foo">
      <li>First  (1)</li>
      <li>Second (2)</li>
      <li>Third  (3)</li>
  </ul>	
  ```

  ```javascript
  var foo = document.getElementById('foo');
  console.log(foo.firstElementChild.textContent); // "First  (1)"
  ```

- [parentElement](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentElement) : 현재 노드에서 부모 노드를 가리킨다.

  ```javascript
  if (node.parentElement) {
      node.parentElement.style.color = "red";
  }
  ```

- [nextSibling](https://developer.mozilla.org/ko/docs/Web/API/Node/nextSibling)

  부모의 `childNodes` 목록에서 지정된 노드 **바로 다음에 있는 노드를 반환**하거나 지정된 노드가 해당 목록의 마지막 노드이면 `null`을 반환 (#text 데이터를 가져온다는 것을 중점으로 볼 것)

  ```HTML
  <div id="div-01">Here is div-01</div>
  <div id="div-02">Here is div-02</div>
  
  <script type="text/javascript">
  var el = document.getElementById('div-01').nextSibling,
      i = 1;
  
  console.log('Siblings of div-01:');
  
  while (el) {
    console.log(i + '. ' + el.nodeName);
    el = el.nextSibling;
    i++;
  }
  
  </script>
  
  /**************************************************
     로드될 때 다음과 같이 콘솔에 기록됩니다. :
  
       Siblings of div-01
  
        1. #text
        2. DIV
        3. #text
        4. SCRIPT
  
  **************************************************/
  ```

- [nextElementSibling](https://developer.mozilla.org/en-US/docs/Web/API/NonDocumentTypeChildNode/nextElementSibling)

  ```HTML
  <div id="div-01">Here is div-01</div>
  <div id="div-02">Here is div-02</div>
  
  <script type="text/javascript">
    var el = document.getElementById('div-01').nextElementSibling;
    console.log('Siblings of div-01:');
    while (el) {
      console.log(el.nodeName);
      el = el.nextElementSibling;
    }
  </script>
  
  /**************************************************
     로드될 때 다음과 같이 콘솔에 기록됩니다. :
  
      Siblings of div-01:
      DIV
      SCRIPT
  
  **************************************************/
  ```

  



### 1-5. DOM 조작 API

---

삭제, 추가, 이동, 교체를 위해 사용하는 DOM API 이다.

- [removeChild()](https://developer.mozilla.org/ko/docs/Web/API/Node/removeChild) : 자식의 엘리먼트를 삭제하는 문법

  ```javascript
  // Get the <ul> element with id="myList"
  var list = document.getElementById("myList");   
  list.removeChild(list.childNodes[0]); // Remove <ul>'s first child node (index 0)
  ```

- [appendChild()](https://developer.mozilla.org/ko/docs/Web/API/Node/appendChild) : 한 노드를 특정 부모 노드의 자식 노드 리스트 중 **마지막 자식으로** 붙임

  ```javascript
  // 새로운 단락 요소를 생성하고 문서에 있는 바디 요소의 끝에 붙입니다.
  var p = document.createElement("p");
  document.body.appendChild(p);
  ```

- [insertBefore()](https://developer.mozilla.org/en-US/docs/Web/API/Node/insertBefore)

  ```HTML
  <ul id="myList">
    <li>Coffee</li>
    <li>Tea</li>
  </ul>
  
  <p>Click the button to insert an item to the list.</p>
  
  <button onclick="myFunction()">Try it</button>
  
  <script>
  function myFunction() {
      var newItem = document.createElement("LI");
      var textnode = document.createTextNode("Water");
      newItem.appendChild(textnode);
  
      var list = document.getElementById("myList");
      list.insertBefore(newItem, list.childNodes[0]);
  }
  </script>
  
  <!-- 
  Example explained:
  First create a LI node,
  then create a Text node,
  then append the Text node to the LI node.
  Finally insert the LI node before the first child node in the list.
  -->
  ```

  - nextSibling 를 통해서 삽입하는 경우도 있음

    ```HTML
    <div id="parentElement">
      <span id="childElement">foo bar</span>
    </div>
    
    <script>
    // Create a new, plain <span> element
    var sp1 = document.createElement("span");
    
    // Get a reference to the element, before we want to insert the element
    var sp2 = document.getElementById("childElement");
    // Get a reference to the parent element
    var parentDiv = sp2.parentNode;
    
    // Insert the new element into the DOM before sp2
    parentDiv.insertBefore(sp1, sp2);
    </script>
    ```

    ```HTML
    parentDiv.insertBefore(sp1, sp2.nextSibling);
    ```

- [cloneNode()](https://developer.mozilla.org/ko/docs/Web/API/Node/cloneNode)

  ```javascript
  var dupNode = node.cloneNode(deep);
  ```

  - node : 복제되어야 할 node
  - dupNode : 복제된 새로운 node
  - deep
    - true : 해당 node의 childern 까지 복사
    - false : 해당 node만 복사

- [replaceChild()](https://developer.mozilla.org/ko/docs/Web/API/Node/replaceChild)

  ```javascript
  replaceNode = parentNode.replaceChild(newChild, oldChild);
  ```

  - replaceNode 는 교체된 노드로서, oldChild 와 동일한 노드이다.
  - newChild 는 oldChild를 교체할 새로운 노드이다. (만약 이미 DOM 안에 존재한다면 가장 먼저 제거됨?)
  - oldChild 는 이미 존재하는, 교체될 자식 노드이다.

  ```javascript
  // <div>
  //  <span id="childSpan">foo bar</span>
  // </div>
  
  // 텅빈 요소 노드를 하나 생성합니다.
  // ID도, 속성도, 컨텐츠도 없습니다.
  var sp1 = document.createElement("span");
  
  // 'newSpan'이란 id 속성을 부여합니다.
  sp1.id = "newSpan";
  
  // 새로운 요소를 위한 컨텐츠를 생성합니다.
  var sp1_content = document.createTextNode("new replacement span element.");
  
  // 컨텐츠를 생성한 요소에 붙입니다.
  sp1.appendChild(sp1_content);
  
  // DOM에 존재하던, 교체되야할 노드를 참조합니다.
  var sp2 = document.getElementById("childSpan");
  var parentDiv = sp2.parentNode;
  
  // 이미 존재하던 sp2 노드를 새로운 span 요소인 sp1으로 교체합니다.
  parentDiv.replaceChild(sp1, sp2);
  
  // 결과:
  // <div>
  //   <span id="newSpan">new replacement span element.</span>
  // </div>
  ```

  































