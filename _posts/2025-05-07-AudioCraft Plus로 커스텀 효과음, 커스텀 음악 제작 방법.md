---
title: "AudioCraft Plus로 커스텀 효과음, 커스텀 음악 제작 방법"
author: kjw202288
date: 2025-05-06 12:00:00 +0800
categories: [IT, AI]
tags: [AI]
image: 
---

CUDA를 지원하는 최소 4GB 이상 정도의 VRAM이 필요하며 12GB VRAM이 권장된다 로컬 버전을 사용하거나 혹은 <https://colab.research.google.com/github/camenduru/MusicGen-colab/blob/main/MusicGen_ClownOfMadness_plus_colab.ipynb>에서 코랩 버전을 사용할수 있다

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
pip uninstall torch
pip install torch==2.1.0 --index-url https://download.pytorch.org/whl/cu121
```
입력해 torch의 CPU 버전을 2.1.0 torch CUDA 버전으로 재설치해준다 2.1.0 버전을 사용하는 이유는 AudioCraft Plus와 호환되기 때문이다 그런다음에
```
$env:HF_HUB_CACHE = "C:\huggingface\cache" # 사용자명이 한글일경우 허깅페이스 허브의 캐시 경로를 바꿔준다
python app.py
```
를 입력하여 AudioCraft Plus의 Webui 주소를 얻어 들어간다

6. 효과음 생성의 경우 AudioGen을, 음악 생성의 경우 MusicGen을 선택하고 프롬프트 수를 정한다음 Input Text에 원하는 텍스트 프롬프트를 입력한다.(Structure Prompts-Global Prompts의 경우 전역 프롬프트를 설정할수 있으며 Enable을 체크해 적용한다.) Duration으로 분량을 설정하고, Overlap을 조정하고 원하는 Seed를 설정한다음 Generate를 눌러 생성한다 프롬프트대로 생성되지 않는다면 시드값이 겹쳤는지 확인하고 시드를 -1(랜덤)로 바꿔준다 결과물 파일은 AudioCraft Plus 저장소 폴더의 output 폴더에서 찾을수 있다