---
title: "Stable Audio로 커스텀 효과음 제작 방법"
author: kjw202288
date: 2025-05-06 12:00:00 +0800
categories: [IT, AI]
tags: [AI]
image: 
---

CUDA를 지원하는 최소 4GB 이상 정도의 VRAM이 필요하며 12GB VRAM이 권장된다

1. Python 3.10을 설치하는데 Add python.exe to PATH를 반드시 체크한다

2. 필요시 파이토치를 설치하며 Stable Audio를 설치할 위치에서 파워셀을 열고
```
pip install stable-audio-tools
```
를 입력하여 설치한다

3. <https://github.com/Stability-AI/stable-audio-tools>에서 Stable Audio를 다운받은다음 해당 폴더에서 아래와 같은 명령어를 입력한다
```
pip install .
```

4. <https://huggingface.co/stabilityai/stable-audio-open-1.0>에서 Files and Version에 들어가 
model.ckpt와 model_config.json를 다운받은뒤 아까 Stable Audio를 설치한 폴더로 들어가 ckpt라는 이름의 폴더를 생성한뒤 그곳에 넣어준다 그런다음 상위 폴더인 Stable Audio 폴더에서 파워셀을 열어 아래와 같은 명령어를 입력해 그라디오 주소를 얻는다
```
python run_gradio.py --ckpt-path ".\ckpt\model.ckpt" --model-config ".\ckpt\model_config.json"
```

5. 그라디오 주소로 들어간다음 원하는 프롬프트와 부정 프롬프트를 입력하고 seconds total에 원하는 생성시간을 입력한다음 학습할 스텝을 정해준다 그런다음 프롬프트 반영도인 CFG 스케일을 설정후 시드는 랜덤 생성의 경우 -1로 맞춰놓고 generate를 눌러 효과음을 생성한다 