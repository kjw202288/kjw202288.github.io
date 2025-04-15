---
title: "Applio(RVC 기반)로 커스텀보이스 제작 방법"
author: kjw202288
date: 2025-01-01 12:00:00 +0800
categories: [Info, AI]
tags: [AI]
mermaid: true
---

1. Applio Github에서 코랩 webui 버전의 Applio.ipynb를 다운받거나 로컬 webui 버전을 다운받는다 <https://github.com/IAHispano/Applio?tab=readme-ov-file>
2. 코랩 webui
- 구글 드라이브에서 설정에 들어가 연결앱에 colab을 설치한뒤 드라이브에 Applio.ipynb를 업로드하여 실행한다
- 코랩 상에서 Install Applio을 실행시킨다음 설치가 완료되면 Start Applio을 실행시켜 그라디오 링크를 얻어낸다음 들어간다
2. 로컬 webui(학습의 경우 4GB 이상의 VRAM 필요)
- run-install.bat을 실행시켜 Applio를 설치한다. 사용자 폴더 이름이 한글일 경우 bat 파일을 메모장으로 열어 set "MINICONDA_DIR=(Custom)" 부분을 재설정하여 그곳에 미리 Miniconda를 설치해놓는다
- run-applio.bat을 실행시켜 webui 주소 링크를 얻어낸다음 들어간다
4. 모델을 학습시키거나 다운로드하여 원하는 모델을 적용시킬수 있다
- 학습 탭에 들어가서 모델명을 정하고 데이터셋 생성기에서 이름을 정하고 원하는 음성파일을 업로드하여 데이터셋을 생성하고 전처리 버튼을 눌러 전처리한다. 피치 추출알고리즘과 임베더 모델을 선택하고 피처를 추출한다. 훈련 설정값을 설정해주고 에포크 수량을 설정해준뒤 학습을 시작한다. pth파일과 index 파일이 저장완료되면 내보내기해준다
- 다운로드 탭에 들어가 <https://voice-models.com/>에서 원하는 보이스 모델 허깅페이스 다운로드 링크를 붙여넣기 한다음 다운로드 버튼을 누르거나 모델 파일(pth나 index)을 업로드한다
5. TTS에 들어가 원하는 음성모델을 선택하고 TTS음성에서 성별을 고른뒤 합성할 텍스트를 적어 변환하여 커스텀보이스 결과물을 얻는다