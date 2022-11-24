---
layout: post
title:  "Google Analytic를 블로그에 적용하기"
date:   2022-11-16 17:58:03 +0900
comments: true
---

<img src="/assets/img/google_analytics.png" alt="">

<blockquote>구글 애널리틱스(Google Analytics)는 현재 구글 마케팅 플랫폼 브랜드 내의 플랫폼으로서, 웹사이트 트래픽을 추적하고 보고하는 구글이 제공하는 웹 애널리틱스 서비스이다. -위키백과-</blockquote>

오늘은 이 google analytics를 블로그에 적용하는 방법에 대해서 알아보겠습니다.

1. **[google analytics](https://analytics.google.com/analytics/web/provision/#/provision)**에 접속

<img src="/assets/img/11ga.png" alt="">

2. 계정정보를 기입합니다.

<img src="/assets/img/1ga.png" alt="">

3. 속성 설정을 하며 시간과 통화 등을 기입합니다.

<img src="/assets/img/2ga.png" alt="">

4. 고급옵션을 설정합니다.

<img src="/assets/img/5ga.png" alt="">

4. 비즈니스 정보 등을 간단하게 기입합니다.

<img src="/assets/img/3ga.png" alt="">

5. 약관에 동의를 합니다.

<img src="/assets/img/4ga.png" alt="">

6. 관리 -> 데이터 스트림에서 데이터를 수집할 소스를 생성해 줍니다. 저는 블로그이므로 웹을 선택합니다. 그리고 자신의 블로그 주소를 입력해 줍니다.

<img src="/assets/img/6ga.png" alt="">

<img src="/assets/img/7ga.png" alt="">

7. 관리 -> 추적 정보 -> 추적 코드에서 추적 아이디를 복사하여 `config.yml`에 다음과 같은 코드를 입력합니다.

```
analytics:
  provider        : "google"

  google:
    tracking_id   : "추적코드"
    anonymize_ip  : # true, false (default)
```

<img src="/assets/img/8ga.png" alt="">

8. _includes 파일의 analytics.html에 범용 사이트 태그 코드를 입력하고 head.html파일에 다음과 같이 입력해 줍니다.
(또는 범용 사이트 태그 코드를 head.html에 직접 입력할 수도 있습니다.)

<img src="/assets/img/9ga.png" alt="">

<img src="/assets/img/analytics.png" alt="">

<img src="/assets/img/head.png" alt="">

9. 다 완료가 되면 다음과 같은 화면을 볼 수 있습니다!!

<img src="/assets/img/10ga.png" alt="">

저는 추적코드를 사용하였지만 최근의 jekyll 테마는 업데이트된 Google Analytics에 맞추어 측정코드를 사용하기도 합니다.
추적코드는 구글링으로도 많은 사람이 시도한 것을 볼 수 있어서 추적코드를 사용했는데, 다음에는 측정 코드를 사용해 봅시다.