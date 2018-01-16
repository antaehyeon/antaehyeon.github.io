---
layout: post
title: "Github Blog Jekyll 테마 적용해보기"
date: 2018-01-17 00:17:00 +0900
description: Github Blog에 Jekyll 테마를 적용해봅시다. (optional)
img: jekyll_0.png # Add image post (optional)
tags: [Github Blog, Github Blog 만들기, 깃허브블로그, 깃헙블로그, 테마, 깃블로그 테마] # add tag
---

0. ### 서론

      GitHub Blog 에 대한 내용으로 2번 째 글을 작성하게 되었습니다. 저번 포스트에서는 GitHub Pages 에서 기본으로 제공하는 Theme 들을 적용하는 것 까지 소개드렸습니다. 이번에는 여러 사용자들이 직접 만든 Github Theme를 적용해보도록 하겠습니다. 

      아, 블로그 프레임워크에는 Jekyll만 존재하는것이 아닙니다. [Hexo](https://hexo.io/) 또는 [HUGO](https://gohugo.io/) 도 있습니다. 각각의 장단점이 있는데 그것을 설명한 페이지는 이곳 [링크](https://qvil.github.io/blog/why-jekyll/)로 대체하겠습니다. 해당 사이트를 참고하셔서 각자 원하는 프레임워크를 선택하시면 될 듯 합니다. 

      해당 글에서는 **Jekyll 을 사용**할 것이며, 약간의 설정이 필요합니다. 그러나, 오픈소스 프로젝트 특성상 설정이 모두 획일적이지는 않을 것 입니다. 그래서 여러개의 테마를 통해서 다른 부분이 있는지 비교해보고 그 내용까지 최대한 추가해서 모두가 GitHub 블로그를 만드는데 어려움이 없었으면 좋겠습니다.

      >아, 그리고 SourceTree를 통해서 Commit-Push 를 진행할 것입니다. 커맨드가 편하신분들은 커맨드를 그대로 사용하시면 되고, UI적으로 해당 글을 그대로 따라하셔야 되는 분들은 SourceTree 를 설치해주세요!

1. ### Jekyll Theme

      ![](https://i.imgur.com/O8TWN8S.png)

      일단 공식사이트는 [이곳](https://jekyllrb-ko.github.io/) 입니다. 원래 이렇게 개인적인 웹을 구성하기 위해서는 해당 프레임워크를 **GitHub Pages로 호스팅**하는 것입니다. 테마는 구글에 'Jekyll theme' 라는 키워드로 [검색](https://jekyllthemes.io/)하면, 여러가지가 나옵니다. 그 중에서도 [Jekyll Themes](http://jekyllthemes.org/) 에서의 [Prologue 테마](http://jekyllthemes.org/themes/jekyll-theme-prologue/)를 예시로 글을 작성해보겠습니다.

      대부분의 테마는 각자의 GitHub(만든사람)를 가지고 있고 가이드가 README로 소개되어 있습니다. Prologue 테마 역시 [홈페이지](http://jekyllthemes.org/themes/jekyll-theme-prologue/) 에서 확인하실 수 있습니다. 

2. ### 테마 적용

      ![](https://i.imgur.com/LJ6stxK.png)

      일단은 1편에서 만들었던 Repository 를 **로컬저장소로 복사**합니다. 저는 소스트리를 이용 할 것입니다.

      ![](https://i.imgur.com/NDq32Cc.png)

      복사된 로컬 경로에는 2가지 파일이 존재할 것입니다. 이제 여기에다가 테마파일을 덮어 씌울 것 입니다. 아까 [Prologue 페이지](http://jekyllthemes.org/themes/jekyll-theme-prologue/)에 가서 [Download](https://github.com/chrisbobbe/jekyll-theme-prologue/archive/master.zip) 를 합니다.

      ![](https://i.imgur.com/cYGU9nd.png)

      해당 압축파일을 풀게되면 각 파일들이 구성되어 있는것을 확인할 수 있습니다. 윈도우의 경우도 각 파일을 다운로드 받은 곳으로 가서 확인하면 됩니다. 이제 이 파일들을 **Local Repository 경로에 붙여넣습니다.** (동일한 파일도 덮어씌우시면 됩니다)

      ![](https://i.imgur.com/BAHxcLc.png)

      이제 **_config.yml** 을 열면 (파일을 여는것은 자신이 쓰는 툴 아무거나 사용하셔도 됩니다. 저는 Atom을 사용하겠습니다) 다음과 같은 내용들이 있습니다. 우리는 일단 최우선으로 깃허브 블로그를 만드는 것이 최우선이기 때문에 한 항목만 수정해서 바로 블로그를 만들어보도록 하겠습니다.

      ![](https://i.imgur.com/OGKOY7l.png)

      **baseurl**의 항목을 위와같이 `baseurl: ""` 만들면 됩니다. baseurl은 github Pages로 호스팅을 할 때 base가 되는 url 입니다. 그냥 비워두시면 됩니다. 그리고 **저장**하신 후

      ![](https://i.imgur.com/mfaI3MH.png)

      **SourceTree 에서 Commit 후 Push** 하시면 됩니다. 

      > 저는 뭐 간단히 `Prologue Theme적용` 정도의 내용으로 Commit을 진행하였습니다.

3. ### 완료

      성공적으로 Repository 에 적용이 되었다면 `https://자신의깃허브ID.github.io` 로 접속하시면 아까 적용했던 Prologue의 테마를 확인할 수 있습니다. 다음 글에서는 블로그의 여러가지 정보를 수정하는 법과 Github 블로그에 글을 올리는 법으로 찾아뵙도록 하겠습니다. 고생하셨습니다 !

4. ### 출처

      - [Jekyll 테마사이트](https://jekyllthemes.io/)
      - [Jekyll 테마사이트](http://jekyllthemes.org/)