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





### 기본 배치에서 벗어나서 떠있기 (float: left)

---

float 속성으로 원래 flow에서 벗어날 수 있고 둥둥 떠다닐 수 있다. float는 일반적인 배치에서 벗어난 형태로 특별히 배치된다.

따라서, 뒤에 block 엘리먼트를 의식하지 못하고 중첩되서 배치된다.

그래서 레이아웃 배치를 양쪽으로 할 때, `float:left` 속성을 이용해서 배치한다.

![](https://imgur.com/y0P3Yck.png)

이런식으로, `float: left` 속성을 이용해 각 div 를 수평배열 시킬 수 있다 (float를 해제하면 아래로 떨어짐, block 형태로)





### 하나의 블록엘리먼트는 BOX 형태임 (Box-model)

---

[The CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)

블록 엘리먼트의 경우 Box의 크기와 간격에 관한 속성으로 배치를 추가 결정함 

- margin, padding, border, outline 으로 생성됨
- box-shadow 는 border 밖에 테두리를 그릴 수 있는 속성임

![](https://i.imgur.com/uplUqG7.png)





### 엘리먼트의 크기는 부모의 크기가 기본

---

블록 엘리먼트의 크기는 기본적으로 부모의 크기만큼을 가진다. 예를들어, `width: 100%` 는 부모의 크기만큼을 다 갖는 것과 같다.





### box-sizing 과 padding

---

`padding` 속성이 너무 커지면, `width` 와 `height` 속성에 영향을 주기 때문에 엘리먼트가 커지게 됨

그래서 본인의 엘리먼트와 인접한 엘리먼트의 속성에 `box-sizing` 속성을 지정하면 해당 엘리먼트가 최대한 본연의 성질을 유지하려고 함

```css
div {
  width:100px;
  height:100px;
  border:1px solid red;
  padding:100px;
  font-size:0.8em;
}

.box-content {
  box-sizing:content-box;
}

.box-border {
  box-sizing:border-box;
}
```





### 그래서, Layout 구현 방법은?

---

- 전체 레이아웃은 `float` 속성을 이용해서 2단, 3단 컬럼 배치를 구현
- 최근에는 `css-grid` 나 `flex` 속성을 이용해서 구현함 (브라우저 지원범위를 잘 확인)
  - 그러나, float 속성을 쓰지 않는것은 아님! (2018년 모바일 네이버 홈페이지도 float 속성을 사용)
- 특별한 위치에 배치하기 위해서는 position absolute 를 사용하고, 기준점을 relative로 설정
- fixed 를 이용해서 화면에 고정시키기도 함
- 간단한 메뉴(네비게이션)들은 inline-block 형태로 구현하기도 함
- 엘리먼트 안 텍스트의 간격과, 다른 엘리먼트간의 간격은 padding과 margin속성을 잘 활용해서 위치시킴





















