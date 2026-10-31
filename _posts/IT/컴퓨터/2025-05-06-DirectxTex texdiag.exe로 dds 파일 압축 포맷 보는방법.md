---
title: "DirectXTex texdiag.exe로 dds 파일 압축 포맷 보는방법"
author: kjw202288
date: 2025-05-06 12:00:00 +0800
categories: [IT, 컴퓨터]
tags: [컴퓨터]
image: 
---

1. DirectXTex 링크로 들어가서 texdiag.exe를 다운로드한다 <https://github.com/microsoft/DirectXTex>

2. texdiag.exe를 분석하고자 하는 텍스쳐가 있는 폴더에 옮겨준다

3. 폴더에 오른쪽 마우스 버튼을 눌러 Powershell을 열어준뒤

```
.\texdiag info 텍스쳐이름.dds
```
과 같은 명령어를 입력한다

BCx 형태로 포맷이 나타나며 format에 _UNORM만 있는경우는 unsigned나 Linear를 의미하고 _SRGB가 붙으면 sRGB를 의미한다 _SNORM은 signed를 의미한다