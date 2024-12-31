---
title: "Applio(RVC 기반)로 커스텀보이스 제작"
author: kjw202288
date: 2024-01-01 12:00:00 +0800
categories: [GitHub, RVC]
tags: [RVC]
mermaid: true
---

1. Applio Github에서 코랩 버전의 Applio.ipynb를 다운받는다 <https://github.com/IAHispano/Applio?tab=readme-ov-file>
2. 구글 드라이브에서 설정에 들어가 연결앱에 colab을 설치한뒤 드라이브에 Applio.ipynb를 업로드하여 실행한다
3. 코랩 상에서 Install Applio을 실행시킨다음 설치가 완료되면 Start Applio을 실행시켜 그라디오 링크를 얻어낸다음 들어간다
4. 다운로드 부분에 들어가 <https://voice-models.com/>에서 원하는 보이스 모델 허깅페이스 다운로드 링크를 붙여넣기 한다음 다운로드 버튼을 누르거나 파일을 업로드한다
5. TTS에 들어가 다운받은 음성모델을 선택하고 TTS음성에서 성별을 고른뒤 합성할 텍스트를 적어 변환하여 커스텀보이스 결과물을 얻는다