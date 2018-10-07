---
layout: post
title:  "[코드스쿼드] What is Babel?"
subtitle:   "코드스쿼드"
categories: devlog
tags: javascript
comments: true
---

> JavaScript Babel 을 검색하면서 배운 내용들을 기록한 글입니다.

##  What is Babel ?

---

Babel is a toolchain that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments.

바벨(Babel)은 주로 현재 및 이전 브라우저 또는 환경에서 ECMAScript 2015+ 코드를 이전 버전과 호환되는 JavaScript 버전으로 변환하는 데 사용되는 툴체인입니다.

원리는 다양한 작은 모듈들이 코드를 컴파일합니다. 그래서, 바벨(Babel)은 다양한 작은 모듈(Presets)들을 담는 일종의 상자역할을 담당합니다.

> 툴체인(toolchain) : 주로 다른 컴퓨터 또는 시스템의 소프트웨어 제품을 만드는 데 사용되는 컴퓨터 프로그램 개발 도구들의 집합

`.babelrc` 은 babel 에 대한 환경설정을 담고있는 파일입니다. "preset" 을 지정할 수도 있으며, 다양한 설정들이 존재합니다. 그 중에서도 babel-preset 에는 stage 로 구분합니다.

1. stage 0 : `just an idea` possible Babel plugin.
2. stage 1 : `Proposal` this is worth working on.
3. stage 2 : `Draft` initial spec.
4. stage 3 : `Candidate` complete spec and initial browser implementations.
5. stage 4 : `Finished` will be added to the next yearly release.

단, STAGE 3 전 까지는 마치 베타버전과 같기때문에 **주의** 해서 사용해야 합니다.

그 외 babel 에는 다양한 기능들도 제공되어 있습니다. `babel-cli` 는 babel 에서 Command Line 을 사용할 수 있게 지원해줍니다. 이 외에도 `babel-polyfill` 와 같이 런타임에 존재하지 않는 함수들을 지원해주기도 합니다.