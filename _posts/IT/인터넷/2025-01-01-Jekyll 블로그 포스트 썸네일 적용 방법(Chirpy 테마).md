---
title: "Jekyll 블로그 포스트 썸네일 적용 방법(Chirpy 테마)"
author: kjw202288
date: 2025-01-01 12:00:00 +0800
categories: [IT, 인터넷]
tags: [인터넷]
mermaid: true
---

VSCode로 jekyll 웹사이트 폴더를 열어 _layouts\home.html의 해당 부분을 다음과 같이 수정해준뒤 저장한다

{% raw %}
```text
<div id="post-list" class="flex-grow-1 px-xl-1">
  {% for post in posts %}
    <article class="card-wrapper card">
      <a href="{{ post.url | relative_url }}" class="post-preview row g-0 flex-md-row-reverse">
        {% assign card_body_col = '12' %}

        <div class="col-md-{{ card_body_col }}">
          <div class="card-body d-flex flex-column">
        
            <div>
            {%- if post.image -%} 
            <img src="{{- post.image | relative_url -}}" alt="image" class="blog-roll-image">
            {%- else -%}
            {%- endif -%}
            <h1 class="card-title my-2 mt-md-0">{{ post.title }}</h1>

            <div class="card-text content mt-0 mb-3">
              <p>{% include post-description.html %}</p>
            </div>
            </div>
```
{% endraw %}

2. _sass\layout에서 _panel.scss에 맨 아래 빈공간에 아래와 같은 코드를 추가해준뒤 저장한다
```text
.blog-roll-image {
  width: 75px;
  height: 75px;
  object-fit: cover;
  float: left;
  margin: 2px 1em 0 auto;
}
```

3. 터미널에
```text
bundle exec jekyll serve
```
를 입력하여 자바스크립트가 작동하는지 확인하고 깃허브 데스크탑에서 push해준다

4. 포스트 작성시에
```text
---
image: 썸네일 주소
---
```
형식으로 작성해준다

5. 완료 

