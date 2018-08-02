---
layout: post
title:  "[알고리즘] JavaScript 기술 정리글"
subtitle:   "알고리즘"
categories: devlog
tags: algorithm
comments: true
---

> JavaScript 로 알고리즘을 풀면서, 사용한 기술에 대해서 정리한 글 입니다.

- [자바스크립트 자료구조 - 배열](http://jinbroing.tistory.com/124)

- [배열 정렬](http://dudmy.net/javascript/2015/11/16/javascript-sort/)

  ```javascript
  // 기본 정렬 (ASCII)
  array.sort
  ```

  ```javascript
  // 내림차순 정렬
  array.sort((a, b) => {
      return b - a;
  });
  ```

  [Array.prototype.sort()](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)

- while 문 `O(n)` 을 계산식(나눗셈, 나머지 등)으로 대체하여 `O(1)` 을 만들 수 있다 - Lesson 03 FrogJmp

- javascript 기본 나눗셈은 소숫점까지 출력됨

  - Math.ceil() : 소수점 올림, 정수 반환
  - Math.floor() : 소수점 버림, 정수 반환
  - Math.round() : 소수점 반올림, 정수 반환