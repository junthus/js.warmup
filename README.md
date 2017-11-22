![img](cover_small.jpg) 뀨

# 깃북이 머여
문서작성 + 호스팅 플랫폼. 기본적으로 검색창을 지원하는게 최고의 장점.
* SaaS 로만 제공한다고.[단호박질](https://help.gitbook.com/basics/can-i-run-gitbook-on-premise.html). github.io 가 있어서인듯.
* [데스크탑 에디터](https://www.gitbook.com/editor)가 있긴 한데 마크다운 편집기가 구타유발툴이라 npm 설치를 추천. (gitbook 코어? 자체가 버전 변경이 좀 있는듯 하기도 하고)
```bash
$ npm install gitbook-cli -g
```

* cli는 이런 명령어를 지원
```bash
$ gitbook init (./newDir) 
$ gitbook serve
```
    * `init` : 기본 파일 두 세개 생성.
    * `serve` : 로컬 서버 + 변경사항 watch => 빌드 & 리프레시 지원, `__book`이란 디렉터리에 빌드 결과물 업데이트.

* 파일 컨벤션
    * README.md (필수)
    * SUMMARY.md (toc용)
    * GLOSSARY.md (용어집 - 자동 색인되어 문서에서 링크되어서 보여짐)
    * book.json (gitbook 설정)
    * cover.jpg, cover_small.jpg (커버이미지라는데 아직 확인 못함)

# 어또케 호스팅 ?
* 일단 깃헙 계정을 준비한다. (org에 문서를 호스팅하려는 경우 그 계정으로 로긴해야 한다.)
* https://www.gitbook.com/ 접속, 깃헙 계정으로 로긴하면 이메일로 컨펌이 온다. 그걸 누르면 아래 페이지로 감.
* ![설정페이지](static/img/gb_setting_github.png)
    * 파란색 인테그레이션 버튼을 누르면 깃헙 리포에 깃북을 설치(?) 해줌

* create 시에 `GITHUB` 항목을 선택해서 github repo 연동하는게 편리. 
    * 나머지 메뉴는 웹 에디터를 자꾸 열어주면서 쓰라고 하는데 마크다운 유저로썬 복장 터지는 인터페이스라...
* 그러나 

{{ file.path }}  
{{ page.title }}  

Availability

## See More
* [gitbook toolchain doc](https://www.gitbook.com/book/gitbookio/docs-toolchain/details)
