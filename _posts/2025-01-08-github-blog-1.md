---
title: Chirpy theme로 Github 블로그 만들기 (1) 환경 변수 및 이미지 변경 하기
description: Chirpy theme로 Github 블로그 만들기
author: Daehee
date: 2025-01-14 20:00:00 +0900
categories: [Github Blog]
tags: [Github, Chirpy]
pin: true
---

## (1). _config.yml 파일 내 환경 변수 변경하기

Chirpy theme를 개인 블로그로 변경을 하기 위해서는 `_config.yml` 파일 내 환경 변수들에 대한 변경이 필요합니다.  
아래는 _config.yml 내 존재하는 다양한 변수들 중 변경이 필요한 일부만 적어놓은 것으로, 아래 변수들을 본인 정보에 맞춰서 변경하면 됩니다.

```yaml
lang: en # or ko-KR

timezone: Asia/Seoul

title: SemiDS # the main title

tagline: Data Scientist for Semiconductor # it will display as the subtitle

description: SemiDS's Blog toward Semiconductor Data Scientist

url: "https://daeheeseol.github.io"

github:
  username: daeheeseol # change to your GitHub username

social: 
  name: SemiDS
  email: daeheeseol@gmail.com # change to your email address
  links: # 저의 경우는 github밖에 없어서 다른 SNS 링크는 삭제했습니다.
    - https://github.com/daeheeseol # change to your GitHub homepage

theme_mode: light # or dark

#cdn: "https://chirpy-img.netlify.app" # 아바타 사진 변경을 위해 해당 줄은 주석 처리

avatar: "assets/img/avatar.jpg" # 블로그 메인 이미지 변경을 위한 이미지 경로 입력
```
***
<br>

## (2). _data/authors.yml에 author 추가하기
`_data/authors.yml`에 아래와 같은 형태로 author 정보를 추가해야 합니다. Author 정보를 추가하지 않으면 나중에 posting을 할때 by 뒤에 author 정보가 나타나지 않습니다.

```yaml
Daehee:
  name: SemiDS
  url: https://github.com/daeheeseol/
```
***
<br>


## (3). 블로그 아바타 이미지 변경하기
블로그 좌측상단 메인 아바타 이미지 변경을 위해 파일을 `assets/img/~` 경로에 저장한 후에 `_config.yml` 내 avartar 환경 변수를 수정하면 됩니다.  
저의 경우는 아바타 이미지를 `assets/img/avatar.jpg`로 저장해두고 사용중 입니다.  
***
<br>

## (4). 블로그 사이드바 배경 이미지 변경하기
블로그 좌측 사이드바의 배경 이미지를 변경하기 위해서는 css 파일에 변경하고자 하는 이미지 경로를 아래와 같이 입력해주면 됩니다.  
저의 경우는 사이드바 이미지를 `assets/img/sidebar.jpg`로 저장해두고 사용중 입니다. 
`_sass/layout/_sidebar.scss` 
```scss
#sidebar {
  @include mx.pl-pr(0);

  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  overflow-y: auto;
  width: v.$sidebar-width;
  border-right: 1px solid var(--sidebar-border-color);
  background: url('/assets/img/sidebar.jpg'); // 추가, 이미지 경로 입력력
  background-size: auto 100%; // 추가, 이미지에 맞춰서 수정
  background-position: -10px; // 추가, 이미지에 맞춰서 수정

  ...
```

\- 환경 변수 및 이미지 변경 후 블로그 메인 화면
![blog_main](/assets/img/posting/2025-01-08-github-blog-1_1.png)