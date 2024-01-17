---
title: "Github로 Chirpy 테마 블로그 구축"
author: kjw202288
date: 2023-01-01 10:00:00 +0800
categories: [Computer, Github]
tags: [Github]
---

1. 웹에서 username.github.io 형식의 이름으로 깃허브 저장소 생성
2. 깃허브 데스크탑을 실행해서 clone 한다. jekyll과 ruby,git의 최신버전을 설치한다
3. chirpy 테마를 username.github.io 폴더에 복붙한다 
4. config.yml에서 주소를 수정한뒤 깃허브 데스크탑에서 push해준다음 저장소 사이트에 들어가서 settings - pages - Build and deployment 부분을 Github Actions로 바꿔준다음 Configure를 눌러 .github/jekyll.yml를 만든다

