---
layout: post
title:  "Jekyll"
date:   2022-11-23
description: 지킬에 대한 간단한 설명입니다.

comments: true

---

<p> 오늘은 정적 웹사이트를 생성하는데 필요한 지킬에 대해 간단히 알아보자
</p>

## Jekyll

<img src="/assets/img/jekyll.png" alt="">

<blockquote>지킬은 정적 사이트 생성기이다. 깃허브의 공동 설립자가 루비 언어로 개발했다. -위키백과-</blockquote>

홈페이지: <https://jekyllrb-ko.github.io/>

## 정적 웹사이트와 동적 웹사이트

웹은 정적 웹과 동적 웹으로 나누어 집니다. 지킬 지반의 블로그는 정적 웹 환경을 위한 환경입니다. 정적으로 웹사이트를 구성하면 정적파일만으로 사이트를 생성하여 빠르고 가볍습니다. 

정적 웹사이트:

* 요청에 따라미리 저장된 페이지를 응답한다.
* 웹 서버가 필요하지 않으므로 서버의 영향이 적다.
* Back-end 코드가 없어 제작이 간편하다
* 추가, 수정, 삭제의 작업이 모두 수동으로 이루어져 관리가 힘들다.

동적 웹사이트:

- 서버에 있는 데이터드을 가공처리한 후 생성되어 전달한다.
- 서버는 사용자의 요청을 해석하여 데이터를 가공한 후 웹 페이지를 보낸다.
- 상황, 시간, 요청 등에 따라 웹 페이지가 달라진다.
- 사용자에게 웹 페이지를 전달하기 전 전처리 과정이 필요해 느리다.

[![explanatino of static and dynamic web](/assets/images/dynamic.jpg "Static web site vs Dynamic web site")](https://about.gitlab.com/blog/2016/06/03/ssg-overview-gitlab-pages-part-1-dynamic-x-static/)

지킬은 markdown이라는 양식을 따르기 때무에 글 작성에 있어서 편리함을 느끼는 사람이 많다. 그래서 최근에는 위드프레스라는 사이트 개발과 블로그 툴에서 지킬로 변경하는 사람들이 늘어나고 있다고 한다! 하지만 사람에 따라서는 익숙한 워드프레스를 선호하는 사람도 많다.