---
title: "Jekyll 블로그 포스트 마크다운 문서 코드 블록 html 기능 비활성화 하는 방법 (Chirpy 테마)"
author: kjw202288
date: 2025-05-04 12:00:00 +0800
categories: [IT, Network]
tags: [Network]
mermaid: true
---

코드블록을 작성하다 마크다운이 html을 지원하기 때문에 html 코드를 작성하면 그대로 적용해버리고 정작 코드블록에는 나타나지 않는 경우가 생긴다

```
(% raw %)
코드 블록
(% endraw %)
```
에서 () 괄호를 {}으로 바꿔서 코드블록을 그 사이에 넣어준다