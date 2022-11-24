---
layout: post
tags: [git, github, eureka!, workflow]
title:  "Git*Github"
date:   2022-11-21
description: 이 포스트는 git&github에 대한 내용입니다.

comments: true

---

<p class="intro">오늘은 개발자라면 프로젝트 및 개발을 하는데 있어서 필수적인 git과 github에 대해서 알아보도록 한다.</p>

## Git:

<img src="/assets/img/git.png" alt="">

<blockquote>
    깃(Git /ɡɪt/[5])은 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 스냅샷 스트림 기반의 분산 버전 관리 시스템이다. 또는 이러한 명령어를 가리킨다.    -위키백과-
</blockquote>


더 설명하자면, 깃은 리누스 토발스에 의해 개발된 분산 버전관리 시스템이다.  깃은 여러 명의 개발자가 하나의 소프트웨어 개발 프로젝트에 참여할 때, 소스 코드를 관리하는데 사용된다. 로컬로 실행되는 소프트웨어로 인터넷 연결이 되지 않는 곳에서도 개발을 진행할 수 있고, 분산 버전관리를 하므로 중앙 저장소가 삭제되어도 원상복구가 가능하다는 장점이 있다.

## 작업의 흐름

우리의 로컬 저장소는 git이 관리하는 세 그루의 나무로 구성된다.

1. 작업 디렉토리(Working directory): 실제 파일로 구성
2. 인덱스(index): 준비 영역(Staging Area)
3. HEAD: 최종 확정본(commit)

[![gitflow](/assets/images/gitflow.jpg "git workflow")](https://www.reddit.com/r/git/comments/99ul9f/git_workflow_diagram_showcasing_the_role_of/)

## Git의 명령어 알아보기

<dl>
  <dt>추가(add)->Staging Area</dt>
  <dd>변경된 파일을 인덱스에 추가한다</dd>
  <dt>확정(commit)->HEAD</dt>
  <dd>변경 내용을 확정한다</dd>
<dl>
  <dt>발행(push)->remote server</dt>
  <dd>로컬 저장소 속 내용을 원격 서버로 올린다</dd>
  <dt>갱신(pull)</dt>
  <dd>로컬 저장소를 원격 저장소에 맞추어 갱신한다</dd>
  <dt>병합(merge)</dt>
  <dd>다른 가지의 변경 내용을 현재 가지에 병합한다</dd>
</dl>

간단하게 표로 정리하면 아래와 같습니다.

## 핵심용어

| 용어         | 설명                                                         |
| ------------ | ------------------------------------------------------------ |
| Repository   | 저장소                                                       |
| Working Tree | 저장소를 바라보는 작업자의 시점                               |
| Staging Area | 저장소에 커밋하기 전에 커밋을 준비하는 위치                    |
| Commit       | 현재 변경된 작업 상태를 확정하고 저장소에 저장                 |
| Head         | 현재 작업 중인 Branch를 가리킴                                | 
| Branch       | 가지 또는 분기점                                              |
| Merge        | 다른 가지의 내용을 현재 가지로 가져와 합치는 작업이제 Git의 작업의 흐름 및 핵심용어들을 알게 되었으니 직접적으로 사용하는 방법을 배워봅시다. |

## Git 사용방법

1. 새로운 저장소 만들기

   `git init`

   폴더를 하나 선정하여 git bash를 실행시켜 준 후, git init을 통해 로컬 저장소를 생성합니다.

2. 저장소 받아오기

   `git clone /로컬/저장소/경로(로컬 저장소를 복제) (저장소 이름)`

   `git clone 사용자명@호스트:/원격/저장소/경로(원격 서버의 저장소를 복제) (저장소 이름)` 

   위와 같이 다른 저장소를 받아오기 위해서 클론을 사용하며, 다른 저장소의 경로를 복사하여 붙여넣고 저장소 이름을 임의 지정하고 싶으면 마지막에 저장소 이름을 입력해 줍니다.

3. 추가와 확정

   로컬 저장소의 내용을 변경하면 Staging Area로 추가합니다.

   `git add <파일 이름>`

   `git add *`

   변경 내용을 확정하기 위해서 커밋을 해 주어 HEAD에 반영합니다.

   `git commit -m "파일 변경 완료"`

4. 변경 내용 발행하기

   자 이제 변경된 내용을 로컬 저장소의 HEAD에서 원격 저장소로 이동시킵시다.

   `git push origin master(Branch)`

   만약 기존의 원격 저장소를 복제한 것이 아니라면 원격 저장소의 주소를 git에게 알려주어야 합니다!

   `git remote add origin <원격 서버 주소>`

   

   이 과정은 로컬 저장소의 내용을 원격 저장소로 발행하는 과정입니다.

   반대로 원격 저장소의 내용으로 로컬 저장소를 갱신하기 위해서는 

   `git pull`의 명령어를 사용하면 됩니다.

## Github:

   <img src="/assets/img/Github-Logo.png" alt="">

<blockquote>
    깃허브(GitHub, /'ɡɪtˌhʌb/, 원래 이름: Logical Awesome LLC)[1]는 루비 온 레일스로 작성된 분산 버전 관리 툴인 깃 저장소 호스팅을 지원하는 웹 서비스이다. 깃허브는 영리적인 서비스와 오픈소스를 위한 무상 서비스를 모두 제공한다.    -위키백과-
</blockquote>


- 원격 저장소를 호스팅하는 플랫폼
- 소프트웨어 프로젝트를 저장, 추적 및 협업하는데 사용
- 자신의 코드 파일을 업로드하고 오픈 소스 프로젝트에서 동료 개발자와 협업 가능
- 개발자들이 공개적으로 네트워크 연결, 협업 및 피칭을 할 수 있는 소셜 네트워킹 사이트

<img src="/assets/img/mygithub.png" alt="">