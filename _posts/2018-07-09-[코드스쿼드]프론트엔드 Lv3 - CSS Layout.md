---
layout: post
title:  "[코드스쿼드] CSS Layout"
subtitle:   "코드스쿼드"
categories: devlog
tags: HTMLCSS
comments: true
---

### CSS Layout

---

Element를 화면에 배치하는 것을 `Layout 작업`이라고 하고, `Rendering 과정`이라고도 한다. (편의상 배치라고 명칭)

기본적으로 **위에서 아래로 순서대로** 블럭을 이루며 배치된다. 하지만, 웹사이트의 배치는 다양하게 표현 가능해야 하기 때문에, 이를 다양한 방식으로 배치할 수 있도록 CSS에는 추가적인 속성을 제공한다.





### 중요하게 이해해야할 속성들

---

- **display**
  - block : 영역을 가진 기본 속성들
  - inline : span, anker(?) 태그들은 기본으로 inline 속성을 지님 (block이 없기 때문에 좌-우)
  - inline-block
- **position**
  - static
  - absolute
  - relative
  - fixed
- **float** (하늘에 둥둥 떠다닌다는 표현으로 사용)
  - left
  - right





### 블록으로 쌓이는 엘리먼트 (display: block)

---

`display: block` 또는 `display: inline-block` 이라면, 해당 엘리먼트는 벽돌이 되어 쌓임 (위-아래)

```html
<div>block1</div>
<p>block2</p>
<div>block3</div>
```

대부분 엘리먼트들은 `display: block` 속성을 가지고 있음





### 옆으로 흐르는 엘리먼트 (display: inline)

---

`display: inline` 은 우측으로, 아래쪽으로 빈자리를 차지하며 흐른다. 참고로, inline 속성이 지정된 엘리먼트는 **높이와 넓이를 지정해도 반영되지 않음**

```html
<div>
  <span>나는 어떻게 배치되나요?</span>
  <span>좌우로 배치되는군요</span>
  <a>링크는요?</a>
  <strong>링크도 강조도 모두 좌우로 흐르는군요</strong>
</div>
```





### 좀 다르게 배치시키기 (position 속성)

---

`block` 이나 `inline` 을 통해서 좌-우, 위-아래 로만 배치시키면 원하는 곳에 배치를 시키기가 어렵다. 그래서 `position` 속성을 이용해 `상대적/절대적` 으로 어떤 위치에 엘리먼트를 배치하는 것이 수월하다.

1. position 속성의 기본값은 static 이다. (순서대로 배치됨)
2. absolute는 기준점에 따라서 특별한 위치에 배정됨
   - top, left, right, bottom 으로 설정
   - 기준점은 상위 엘리먼트 중 static 이 아닌 엘리먼트로 지정함
   - top, left 속성을 꼭 주는것이 중요함 ! (0, 0 이라도)
3. relative는 원래 자신이 위치해야 할 곳을 기준으로 이동함
   - top, left, right, bottom 으로 설정
4. fixed는 viewport(전체화면=body) 좌측, 맨위를 기준으로 동작함





### 간격을 다르게해서 배치하기 (margin: 10px)

---

`margin : 위 오른쪽 아래 왼쪽;` 순으로 적용됨

`margin-top`, `margin-left`, `margin-bottom`, `margin-left` 으로 개별적으로 설정할 수 있음

`margin: 위-아래 오른쪽-왼쪽;` 순으로도 적용할 수 있음



































