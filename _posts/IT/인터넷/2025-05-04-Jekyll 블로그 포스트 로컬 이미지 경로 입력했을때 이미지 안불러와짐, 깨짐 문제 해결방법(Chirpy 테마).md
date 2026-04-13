---
title: "Jekyll 블로그 포스트 로컬 이미지 경로 입력했을때 이미지 안불러와짐, 깨짐 문제 해결방법(Chirpy 테마)"
author: kjw202288
date: 2025-05-04 12:00:00 +0800
categories: [IT, 인터넷]
tags: [인터넷]
mermaid: true
---

1. CDN을 따로 설정하지 않는 경우 config.yml에서 cdn: "" 으로 변경해준다

2. 이미지 파일이 assets 폴더 안에 있는지 확인한다 _posts와 같이 언더바가 포함된 로컬 경로는 작동하지 않는다

3. 역슬래시 \ 가 아닌 슬래시 / 로 경로를 표시하여야 한다 html 코드가 아래와 같이 상대 경로를 사용하는 경우 더욱 그렇다

{% raw %}
```
<img src="{{ '이미지 경로' | relative_url }}" alt="image">
```
{% endraw %}