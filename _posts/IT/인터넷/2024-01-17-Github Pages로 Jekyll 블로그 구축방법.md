---
title: "Github Pages로 Jekyll 블로그 구축방법"
author: kjw202288
date: 2024-01-17 12:00:00 +0800
categories: [IT, 인터넷]
tags: [인터넷]
mermaid: true
---

1. 웹에서 username.github.io 형식의 이름으로 깃허브 저장소 생성
2. 깃허브 데스크탑을 실행해서 로컬 저장소로 clone 한다. ruby와 git의 최신버전을 설치한다
3. chirpy 테마를 username.github.io 폴더에 복붙한다 VSCode로 폴더를 연다음 터미널을 열어  
```text
chcp 65001
bundle install
bundle update
gem install bundlers
gem install jekyll bundler
```
를 차례로 입력해 jekyll을 설치한다. config.yml에서 url 부분을 수정한다 CDN 부분의 경우 반드시 지워 로컬 이미지가 안나타나는 현상을 겪지 않도록 한다 필요한 경우에는 CDN을 따로 추가해준다. 
```text
bundle exec jekyll serve
```
을 터미널에 입력해 사이트를 테스트 해본뒤 깃허브 데스크탑에서 push해준다
4. 저장소 사이트에 들어가서 settings - pages - Build and deployment 부분을 Github Actions로 바꿔준다음 Configure를 눌러 .github/jekyll.yml를 생성하는데 
Build with Jekyll위에 아래와 같은 부분을 추가해준다
```text
  - name: npm build
       run: npm install && npm run build
  - name: Build with Jekyll
```
     그리고 
```text
  - name: Setup Ruby
       uses: ruby/setup-ruby@8575951200e472d5f2d95c625da0c7bec8217c42 # v1.161.0
```
     부분을
```text
  - name: Setup Ruby
       uses: ruby/setup-ruby@v1
```
     와 같이 바꿔준뒤 생성해준다
5. 완료