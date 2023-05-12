---
title: "[코이카츠] BetterRepack(베리팩)"
author: kjw202288
date: 2022-02-01 12:00:00 +0800
categories: [Microsoft, Unity]
tags: [Unity]
image: https://user-images.githubusercontent.com/76558033/204128470-6d8d9267-db29-4466-a82f-f19ad1514958.png
---

Original, BetterRepack, Sideloader Studio ModPack이 포함

![화면 캡처 2022-11-27 183533](https://user-images.githubusercontent.com/76558033/204128470-6d8d9267-db29-4466-a82f-f19ad1514958.png)

1. 베리팩 & 사이드로더  <https://dl.betterrepack.com/public/>에서 베리팩과 사이드로더를 다운받는다.

2. 베리팩이 설치된 경로의 mods 폴더에 사이드로더팩 파일들을 모두 넣는다

3. 한글패치 & Kplug <https://mega.nz/file/8cxjjYaA#ygMFiIL0unfM8JwvsufB1pJSPRDwjJDwXPFpDRZzbkg>를 다운받아 한글패치, 추가 플러그인 폴더와 Kplug 폴더에 있는 파일들을 베리팩 설치폴더에 넣고 아래파일들을 삭제한다
- BepInEx\plugins\GeBo_Plugins\KK_GameDressforSuccess.dll
- BepInEx\plugins\GeBo_Plugins\KK_TranslationHelper.dll
- BepInEx\plugins\GeBo_Plugins\KK_TranslationCacheCleaner.dll
- BepInEx\plugins\KK_Becometrap.dll
- BepInEx\plugins\RealPOV.Koikatu.dll

4. InitSetting에서 태극기 모양을 눌러 한국어로 설정한뒤  XUnity.AutoTranslator <https://github.com/bbepis/XUnity.AutoTranslator/releases>에서 XUnity.AutoTranslator-BepInEx를 다운받아 BepInEX폴더를 게임 설치폴더에 넣는다.

5. 아래 항목들을 전부 다운받고 각각의 폴더의 압축을 푼뒤 안에 들어있는 BepInEX 폴더들을 모아 게임이 설치된 폴더에 일괄적으로 넣어준다.
- IllusionModdingAPI <https://github.com/IllusionMods/IllusionModdingAPI/releases>
- BepisPlugins <https://github.com/IllusionMods/BepisPlugins/releases>
- XUnity.ResourceRedirector-BepInEx <https://github.com/bbepis/XUnity.AutoTranslator/releases>
- MaterialEditor(설명란에 있음) <https://github.com/IllusionMods/KK_Plugins>
- Illusion-Overlay-Mods <https://github.com/ManlyMarco/Illusion-Overlay-Mods>
