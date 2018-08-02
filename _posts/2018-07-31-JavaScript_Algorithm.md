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

- JavaScript 배열 (array) 특정 값으로 초기화하기

  ```javascript
  Array.apply(null, new Array(5)).map(Number.prototype.valueOf, 0);
  Array.apply(null, new Array(5)).map(String.prototype.valueOf, 'HI');
  ```

- 배열에서 숫자를 찾는것은 `Arrays.indexOf(value)` 이다.

- 숫자의 절대값을 반환하는 것은 `Math.abs()` 이다.

- 배열의 총 합을 구하는 메서드 [reduceRight](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/ReduceRight) `Array.reduceRight((a,b)=>{return a+b;});`

- [배열 중 최소값 또는 최대값을 리턴하는 메서드](http://programmingsummaries.tistory.com/108)

  ```javascript
  var array = [1, 10, 5, 11, 2];
  
  //최대값
  var max = array.reduce( function (previous, current) { 
  	return previous > current ? previous:current;
  });
  
  //최소값
  var min = array.reduce( function (previous, current) { 
  	return previous > current ? current:previous;
  });
  ```

  꼭 배열을 이용할 필요가 없다면, min 값을 두고 비교하면서 최솟값을 찾을 것