---
title: "[Github] Chirpy로 jekyll 블로그 구축"
author: kjw202288
date: 2022-01-01 10:00:00 +0800
categories: [Microsoft, Github]
tags: [Jekyll]
---

## 블로그 구축하기

<details>
  <div markdown="1">

1. 웹에서 username.github.io 형식의 이름으로 깃허브 저장소 생성
2. 깃허브 데스크탑을 실행해서 clone 한다. jekyll과 ruby,git의 최신버전을 설치한다
3. username.github.io 형식의 폴더에서 오른쪽 마우스 클릭하여 git bash here를 선택한다음 아래의 것들을 입력해준뒤 jekyll serve를 입력하여 테스트해본다


```
gem install webrick
```
```
 gem install jekyll bundler
```
```
 jekyll new ./
```
```
 bundle install
```
```
 bundle add webrick
```
4. chirpy 테마를 username.github.io 폴덩에 복붙한뒤 chirpy-starter도 복붙한다. 
5. config.yml에서 주소를 수정한뒤 깃허브 데스크탑에서 push해준다음 저장소 사이트에 들어가서 settings - pages - Build and deployment 부분을 Github Actions로 바꿔준다음 .github/jekyll.yml를 만든다음 jekyll.yml과 commitlin.yml를 제외하고 나머지는 전부 삭제한다

 </div>
</details>
