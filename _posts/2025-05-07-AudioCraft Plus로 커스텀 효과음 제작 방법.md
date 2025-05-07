---
title: "AudioCraft Plus로 커스텀 효과음 제작 방법"
author: kjw202288
date: 2025-05-06 12:00:00 +0800
categories: [IT, CG]
tags: [CG]
image: 
---

1. Python 3.10을 설치하는데 Add python.exe to PATH를 반드시 체크한다

2. C++ 빌드 툴을 설치한다 <https://visualstudio.microsoft.com/ko/visual-cpp-build-tools/> 설치할떄 C++를 사용한 데스크톱 개발만 체크하며 설치 세부정보에서 선택사항에 C++ Clang 도구와 Windows 11 SDK를 추가로 선택한다

3. AudioCraft Plus를 설치할 폴더에 오른쪽 마우스-파워셀 열기를 클릭하여 터미널을 연다음 아래의 코드를 순서대로 입력한다 중간에 pytorch를 업데이트해야한다면 안내문대로 업데이트해준다
```
pip install 'torch>=2.0'
pip install -U audiocraft
pip install -U git+https://git@github.com/GrandaddyShmax/audiocraft_plus#egg=audiocraft
```

4. AudioCraft Plus 사이트 <https://github.com/GrandaddyShmax/audiocraft_plus>에 들어가서 다운받은다음 설치할 폴더에 압축을 푼다

5. AudioCraft Plus 폴더에 들어가 오른쪽마우스-파워셀 열기로 다시 터미널을 열어준다음
```
pip install -e .
```
를 입력한다음
```
python app.py
```
를 입력하여 AudioCraft Plus의 Webui 주소를 얻어 들어간다