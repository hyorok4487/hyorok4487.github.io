![preview Long Haul](/preview.jpg)
#### [View Demo](http://brianmaierjr.com/long-haul)

- [Dark Mode support](https://github.com/brianmaierjr/long-haul/blob/master/preview-dark.png) via [prefers-color-scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme) 

나는 위의 테마를 나의 블로그에 적용하였다.     

## 1. 루비 및 지킬 설치
지킬은 루비(Ruby) 기반 정적 웹사이트 생성기로 지킬(jekyll)을 사용해서 블로그를 만들 것이다.
일단 나의 컴퓨터는 윈도우 운영체제 이므로 ruby를 설치한다
https://rubyinstaller.org/downloads/ (Ruby + Devkit을 설치한다)
이후, 지킬 사이트(https://jekyllrb-ko.github.io/)에서 설치 가이드를 따라서 설치를 진행한다.

## 2. Git & Github를 활용하여 로컬 & 원격 저장소 형성
# (1) 원격 저장소 생성
<p>지킬을 설치한 후 깃허브 사이트에 들어가 새 원격 저장소를 만들어 준다. 이때 이름은 username.github.io로 설정한다.(username은 자신의 깃허브 이름)</p>


# (2) 로컬 저장소와 연동
<p>자신의 원격 저장소의 주소를 복사한 후 컴퓨터에 블로그 내용을 저장할 새 파일을 생성 후, 그곳에 Git을 사용해서 클론을 통해 원격 저장소와 동일한 내용의 로컬 저장소를 생성한다.
이후 vscode 등으로 예시 html 파일을 만들고 Git으로 로컬 저장소에 추가 및 커밋과 푸시를 한다. 그리고 자신의 원격 저장소의 'Github Pages'라는 곳에서 url을 클릭해주면 예시 파일이 구현되어 있는 것을 확인할 수 있다.</p>

## 3. 지킬 테마 적용하기
<p>이제 밋밋한 블로그에 테마를 입혀줄 차례다.  

https://jekyllthemes.io/theme/long-haul

위와 같은 여러 지킬 테마 제공 사이트에서 자신의 마음에 드는 테마를 선택 후 zip파일을 다운로드한다. 

그리고 다운로드한 파일을 나의 로컬 저장소 폴더에 덮어쓰기하여 붙여 넣는다.(혹시 이전에 작성한 post와 같은 글이 있으면 따로 빼 놓거나 그 post만 덮어쓰지 않는다.)

그리고 로컬 저장소에서 git bash창을 열고 git status를 입력하면 수 많은 에러가 나타난다. 

  git bash에서 저장하라는 것은 저장하고 삭제하라는 것은 삭제하며 점차 오류를 줄여나가면
.
.
.

테마가 적용된 자신의 블로그를 볼 수 있다! 이 과정이 가장 힘들다... 고칠 것이 매우 많고 또 예상치 못한 에러도 발생하기 때문에 구글링을 많이 해서 문제를 해결해야 한다.

나는 오류가 어디서부터 무슨 문제가 생겼는지 알 수 없을 때 커밋한 내용을 되돌려서 알아내는 방법을 선택했다.

일단 git log --oneline를 입력하면 커밋 메시지와 문자와 숫자가 혼합된 주소(?)가 나오고 커밋 메시지에 해당하는 곳으로 되돌아 가고 싶으면 git reset --hard <주소>를 입력하고 git push -f origin main를 통해 강제 푸쉬하면 성공적으로 커밋 이전으로 되돌릴 수 있다.</p>

## 4. 테마 수정하기
기존의 테마는 기본 테마이자 베포자의 필요에 따라서 제작이 되었다. 따라서 나만의 블로그를 만들기 위해서는 테마도 수정을 하여 나의 필요에 맞추어나갈 필요가 있다.
  
나는 다음과 같은 테마의 요소들을 수정하였다.
- 네비게이션 바
- 제목
- 파비콘
- 댓글

다음과 같은 요소들을 수월하게 수정하기 위해서 나의 블로그를 웹페이지에 띄워 놓아 개발자 브라우저의 개발자 도구를 활용하여 수정하고자 하는 부분의 코드를 파악하며 수정을 해 나갔다.
  
또한, vscode의 검색 기능을 활용하여 바꾸고자 하는 부분을 쉽게 찾을 수 있었다.
  
1. 네이게이션 바
  config.yml 파일의 navigation: 부분을 수정한다.
2. 제목
  config.yml 파일의 title: 부분을 수정한다.
  ![navigation and title](/navtitle.png)
3. 파비콘
  1. [flaticon](https://www.flaticon.com/)과 같은 사이트에서 파비콘으로 사용할 그림을 찾는다.
  2. [realfivicongenerator](https://realfavicongenerator.net/)에 파비콘으로 원하는 그림을 넣는다.
  3. 이후 웹사이트에서 제공하는 다운로드 파일을 다운로드한 후, assets파일에 logo.ico파일을 만들고 다운로드한 파일을 넣는다.
  4. Generate your Favicons and HTML code 버튼을 눌러 코드를 복사하고 _includes 폴더 > head.html에 코드를 붙여넣어 저장해 주면 파비콘이 적용된다.
  ![favicon](/favicon.png)
4. 댓글
  
## 5. post 작성
자신이 쓰고자 하는 글을 마크다운 문법에 따라 포스트로 작성
