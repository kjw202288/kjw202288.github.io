---
title: "Github Issue에서 업로드한 이미지의 주소 CORS 정책 변경으로 Jekyll 블로그에서 작동안할때 해결방법"
author: kjw202288
date: 2025-05-03 12:00:00 +0800
categories: [IT, Network]
tags: [Network]
mermaid: true
---

1. 깃허브 이슈에서 새로운 이슈 만들기 선택후 이미지를 첨부한다

2. 생성되는 링크인
```
![Image](https://github.com/user-attachments/assets/(Custom))
```
부분에서 https~으로 시작하는 이미지 주소를 복사하여 브라우저 URL 창에 입력한다

3. 업로드한 이미지가 나오면 새페이지 URL 창에 새롭게 변경되어 나온 
```
https://github-production-user-asset-~~~
```
주소를 복사하여 이미지를 Jekyll 블로그에서 사용한다 