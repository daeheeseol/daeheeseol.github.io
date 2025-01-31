---
title: Github Blog by Chirpy theme (4) 각종 에러 해결
description: Chirpy theme로 Github Blog 만들기 (2025-01 기준)
author: SemiDS
date: 2025-01-17 20:00:00 +0900
categories: [Github Blog]
tags: [Github, Chirpy]
pin: false
---

## (1). ERROR `/assets/js/dist/home.min.js' not found
`/assets/js/~`경로안에 `dist/*.js` 파일들이 생성되지 않은 경우 위와 같은 에러가 발생합니다. 해당 파일이 생성되지 않으면 검색이나, TOC (Table of Contents: Posting 시 우측에 나오는 머릿글 순서 목록) 기능이 작동되지 않습니다.   

해결 방법은 node.js를 설치하고 `bundle install` 후
```shell
bundle install
```
아래와 같이 `npm install && npm run build`를 실행해주면 됩니다.

```shell
npm install && npm run build
```
npm build 후 local에서 jekyll 실행 시 `/assets/js/dist/*.js` 파일이 생성되는 것을 볼 수 있습니다.
```shell
jekyll serve
```

## (2). npm run build 에러
**npm install && npm run build** 실행시 아래와 같은 에러가 나는 경우가 있는데, 해당 에러의 경우 build를 실행한 경로에 문제가 있을 경우 발생하는 에러입니다.  
저의 경우는 경로 상에 `OneDrive\바탕 화면`가 포함되어 있어서 발생한 경우로, `OneDrive\바탕 화면`가 포함된 경로가 아닌 local 경로에 폴더를 만들고 실행하면 정상적으로 build 됩니다.

![(2)-1](/assets/img/posting/2025-01-16-github-blog-1_1.png)

## (3). Error: Can't find stylesheet to import.
Github Actions Deploy시 발생하는 위 에러는 `@use 'vendors/bootstrap';` 문구에서 보이는 바와 같이 vendors 경로에서 bootstrap stylesheet를 찾을 수 없어서 발생하는 경우입니다. 

![(2)-2](/assets/img/posting/2025-01-16-github-blog-1_2.png)

해결 방법은 아주 간단한데, .gitignore 파일에서 아래 부분을 주석처리 해주면 됩니다.

```shell
#_sass/vendors #주석 처리
```

## (4). Utterances에서 댓글이 업로드 되지 않는 에러
`Utterances`에서 댓글 작성 후 comment를 눌렀을 때 댓글이 정상적으로 업로드 되지 않는 에러가 발생한 경우는 `github-repository-settings`에서 issue의 활성화 여부를 확인하면 됩니다.  
아래 사진과 같이 `Features-issues` 부분이 체크가 되어 있으면 됩니다.

![(2)-3](/assets/img/posting/2025-01-16-github-blog-1_3.png)


