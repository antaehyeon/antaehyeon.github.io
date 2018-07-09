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

![](https://imgur.com/le01Lph.png)





































