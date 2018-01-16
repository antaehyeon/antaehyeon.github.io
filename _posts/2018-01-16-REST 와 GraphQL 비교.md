---
layout: post
title: "REST 와 GraphQL 비교"
date: 2018-01-16 21:23:00 +0900
description: REST와 GraphQL에 대해서 비교해보겠습니다. (optional)
img: rest_graphQL.png # Add image post (optional)
tags: [REST, GraphQL] # add tag
---

0. ### 서론

      GitHub 의 데이터를 Parsing 해야하는 필요가 있어서, GitHub Developer 를 참고하던 도중 API Docs에 REST API와 GraphQL API가 눈에 들어왔습니다. GraphQL을 검색해보니 REST의 단점들을 해결하는 흥미로운 부분이 많아서 해당 주제로 글을 쓰면 좋겠다는 생각이 들어서 작성하게 되었습니다. 

1. ### REST API

      > Representational safe transfer (REST)

      2000 년에 소개된 REST는 **WWW(World Wide Web) 과 같은 분산 하이퍼미디어 시스템을 위한 소프트웨어 아키텍쳐의 한 형식**입니다. HTTP의 주요 저자 중 한 사람인 [Roy Fielding](https://www.google.co.kr/search?q=Roy+Fielding&oq=Roy+Fielding&aqs=chrome..69i57j69i59j69i60l2j0l2.988j0j4&sourceid=chrome&ie=UTF-8) 의 논문에 의해서 소개되었으며, 웹의 장점을 최대한 활용하기 위한 의도로 제작되었습니다.

      > 어떤 특정한 언어가 아닙니다. **네트워크 시스템의 architecture style** 입니다

      ---

      #### REST 에서의 리소스

      Resource 는 웹이 제공하는 **데이터**를 의미합니다. 예를 들어, 파일이나 이미지 같은 것들을 포함해서 모든 데이터들을요. 해당 이미지나 파일들에게는 각각의 **식별자(identifier)** 이 존재합니다. 우리는 이것을 **URI** 이라고 부릅니다.

      > URI : 통합 자원 식별자, Uniform Resource Identifier

      ![](https://i.imgur.com/E2oqZDm.png)

      클라이언트(웹 브라우저)는 URI 를 통해서 특정 Resource 를 서버에게 요청한 후 결과를 받습니다. 이후 사용자의 클라이언트에는 새로운 내용이 출력되면서 상태가 변경되는데 REST는 이러한 특성을 표현한 용어입니다.

      ---

      #### REST 의 특성 6가지

      1. 클라이언트/서버 구조
      2. 무상태(Stateless)
      3. 캐시 처리 가능(Cacheable)
      4. 유니폼 인터페이스(Uniform Interface)
      5. 자체 표현 구조 (Self-descriptiveness)

2. ### GraphQL

3. ### 차이점

4. ### 기타

5. ### 출처

      - [REST에서 GraphQL 과 RELAY로 갈아타기 - 이정우](https://www.slideshare.net/deview/112rest-graph-ql-relay)
      - [조대협의 블로그](http://bcho.tistory.com/953)
      - [Representational State Transfer(REST) 란?](http://egloos.zum.com/tiger5net/v/5202221)
      - [RESTFUL(Representational Safe Transfer)](http://egloos.zum.com/tiger5net/v/5202221)
      - [Building Web Services the REST Way](http://www.xfront.com/REST-Web-Services.html)
      - ​