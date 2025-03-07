---
title: "Jekyll 자바스크립트 작동안함 해결방법(Chirpy 테마)"
author: kjw202288
date: 2025-01-01 12:00:00 +0800
categories: [IT, Web]
tags: [Web]
mermaid: true
---

1. node.js를 설치한다
2. Powershell을 열어 
```text
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
Get-ExecutionPolicy -Scope CurrentUser
npm --version
```
을 차례대로 입력하여 실행정책을 RemoteSigned로 변경한뒤 확인하고 npm의 버전도 확인한다
3. VSCode로 jekyll 웹사이트 폴더를 연다음 터미널을 열어
```text
npm install
npm run build 
```
를 차례로 입력한다
4. 터미널에
```text
bundle exec jekyll serve
```
를 입력하여 자바스크립트가 작동하는지 확인한다
5. 완료
