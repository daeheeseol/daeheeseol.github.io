---
title: Github Blog by Chirpy theme (2) Github Actions 실행 및 Utterances 추가
description: Chirpy theme로 Github Blog 만들기 (2025-01 기준)
author: SemiDS
date: 2025-01-15 20:00:00 +0900
categories: [Github Blog, Utterances]
tags: [Github, Chirpy]
pin: false
---

## (1). Github Actions 실행
Chirpy theme에 대한 환경 변수, 이미지 등 기본적인 정보 설정이 완료 되었다면 (`Github Blog by Chirpy theme (1)편 참고`), Github에 push후 블로그를 build 하는 과정이 필요합니다.   
해당 과정은 Github Actions 기능을 통해 수행되며, 아래 사진과 같은 순서로 진행하면 됩니다.
> Actions -> New workflow -> Github Pages Jekyll -> Branch 이름 확인 후 Commit changes
{: .prompt-tip }

(사진을 클릭하면 확대됩니다.)
![(4)-1](/assets/img/posting/2025-01-24-github-blog-1_1.png)

위 과정을 진행한 후 정상적으로 build 및 deploy 까지 완료 되면 `[username].github.io`를 통해 블로그 접속이 가능해집니다 

## (2). Utterances를 통한 댓글 기능 추가
**Utterances**를 통해서 Posting 아래쪽에 댓글 기능을 추가할 수 있습니다. Github issue와 연동되어 사용되며 repository의 설정 부분에서 issue 부분이 활성화 되어 있어야 사용할 수 있습니다. (`Github Blog by Chirpy theme (3)편 참고`)   
[Utterances 설치 페이지](https://github.com/apps/utterances)에 접속 해서 Install을 진행한 후 repository 등록을 진행합니다. 그 후 아래 사진과 같이 `_layouts/post.html` 파일 아랫 부분에 스크립트를 추가하시면 됩니다.

(사진을 클릭하면 확대됩니다.)
![(4)-2](/assets/img/posting/2025-01-24-github-blog-1_2.png)

스크립트 추가 후 블로그를 확인해 보면 아래와 같은 댓글창이 생성된 걸 볼 수 있습니다.

![(4)-3](/assets/img/posting/2025-01-24-github-blog-1_3.png)
