---
layout: post
title:  "[CSS] CSS Specificity"
subtitle:   "코드스쿼드"
categories: devlog
tags: HTMLCSS
comments: true
---

## CSS Specificity

> CSS Specificity 에 대해서 코드를 작성하고, CSS의 우선순위를 파악할 글 입니다.

![CSS Specificity with Plankton, Fish and Sharks](https://i.imgur.com/YMr3mGc.png)

## 개요

CSS 는 여러가지 속성을 적용할 수 있다. 위의 CSS Specificity 그림에서도 알 수 있듯이 Class와 ID 속성을 이용해서 적용할 수 있는데, 여기에는 우선순위가 적용된다. 프로그램이 CSS를 해석할 때, 각 node의 속성에 따라서 Score 를 할당하는데 이 점수에 따라서 속성들이 적용된다. 다른 클래스에서 같은 속성들이 있을 때, 우선순위에 따라서 적용되는 것이다.

이 우선순위를 간단한 만화형식으로 나타낸 것이 위의 CSS Specificity 이다. 여기서는 앞으로 직접 코드를 작성해서 테스트 해보고 증명해볼 것이다.













































