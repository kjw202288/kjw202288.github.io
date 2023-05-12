---
title: "[기계학습] StableDiffusion WebUI"
author: kjw202288
date: 2022-01-02 12:00:00 +0800
categories: [Google, Colab]
tags: [ML]
---

## 프롬프트

### positive

<details>
best quality, masterpiece, high quality, highres,best quality,anime girl,detailed eyes, no shadow, distinct_image,detailed cute anime face
</details>

### negative

<details>
asymmetrical eyes, Heterochromia, long_eyelashes, heavy_eyelashes,Lowres, bad hands, error,missing fingers,extra digit,fewer digits,cropped,worst quality,low quality,normal quality,jpeg artifacts,signature,watermark,username,blurry,bad feet,ugly,duplicate,trannsexual,hermaphrodite,out of frame,extra fingers,mutated hands,poorly drawn hands,poorly drawn face,mutation,deformed,blurry ,bad proportions,extra limbs,cloned face,disfigured,more than 2 nipples,out of frame,ugly,extra limbs,gross,worst quality,low quality,normal quality,signature,watermark,username,blurry,proportions,malformed limbs,missing arms,missing legs,extra arms,extra legs,mutated hands,fused fingers,too many fingers,long neck, multiple breasts, (mutated hands and fingers:1.5), (long body :1.3), (mutation, poorly drawn :1.2), black-white, bad anatomy, liquid body, liquidtongue, disfigured, malformed, mutated, anatomical nonsense, text font ui, error, malformed hands, long neck, blurred, lowers, low res, bad anatomy, bad proportions,bad shadow, uncoordinated body, unnatural body, fused breasts, bad breasts, huge breasts, poorly drawn breasts, extra breasts, liquid breasts, heavy breasts, missingbreasts, huge haunch, huge thighs, huge calf, bad hands, fused hand, missing hand, disappearing arms, disappearing thigh, disappearing calf, disappearing legs, fusedears, bad ears, poorly drawn ears, extra ears, liquid ears, heavy ears, missing ears, fused animal ears, bad animal ears, poorly drawn animal ears, extra animal ears, liquidanimal ears, heavy animal ears, missing animal ears, text, ui, error, missing fingers, missing limb, fused fingers, one hand with more than 5 fingers, one hand with less than5 fingers, one hand with more than 5 digit, one hand with less than 5 digit, extra digit, fewer digits, fused digit, missing digit, bad digit, liquid digit, colorful tongue, blacktongue, cropped, watermark, username, blurry, JPEG artifacts, signature, 3D, 3D game, 3D game scene, 3D character, malformed feet, extra feet, bad feet, poorly drawnfeet, fused feet, missing feet, extra shoes, bad shoes, fused shoes, more than two shoes, poorly drawn shoes, bad gloves, poorly drawn gloves, fused gloves, bad cum,poorly drawn cum, fused cum, bad hairs, poorly drawn hairs, fused hairs, big muscles, ugly, bad face, fused face, poorly drawn face, cloned face, big face, long face, badeyes, fused eyes poorly drawn eyes, extra eyes, malformed limbs, more than 2 nipples, missing nipples, different nipples, fused nipples, bad nipples, poorly drawnnipples, black nipples, colorful nipples, gross proportions. short arm, (((missing arms))), missing thighs, missing calf, missing legs, mutation, duplicate, morbid, mutilated,poorly drawn hands, more than 1 left hand, more than 1 right hand, deformed, (blurry), disfigured, missing legs, extra arms, extra thighs, more than 2 thighs, extra calf,fused calf, extra legs, bad knee, extra knee, more than 2 legs, bad tails, bad mouth, fused mouth, poorly drawn mouth, bad tongue, tongue within mouth, too longtongue, black tongue, big mouth, cracked mouth, bad mouth, dirty face, dirty teeth, dirty pantie, fused pantie, poorly drawn pantie, fused cloth, poorly drawn cloth, badpantie, yellow teeth, thick lips, bad camel toe, colorful camel toe, bad asshole, poorly drawn asshole, fused asshole, missing asshole, bad anus, bad pussy, bad crotch, badcrotch seam, fused anus, fused pussy, fused anus, fused crotch, poorly drawn crotch, fused seam, poorly drawn anus, poorly drawn pussy, poorly drawn crotch, poorlydrawn crotch seam, bad thigh gap, missing thigh gap, fused thigh gap, liquid thigh gap, poorly drawn thigh gap, poorly drawn anus, bad collarbone, fused collarbone,missing collarbone, liquid collarbone, strong girl, obesity, worst quality, low quality, normal quality, liquid tentacles, bad tentacles, poorly drawn tentacles, split tentacles,fused tentacles, missing clit, bad clit, fused clit, colorful clit, black clit, liquid clit, QR code, bar code, censored, safety panties, safety knickers, beard, furry,pony, pubic hair,mosaic, excrement, faeces, shit, futa, testis
</details>

### 이슈

1. <https://novelai.app/>(사용가능한 prompt 정리)
2. <http://dev.kanotype.net:8003/deepdanbooru/>(Image를 인식하여 prompt 생성)
- 한번에 복사시 크롬창에 F12누른뒤 콘솔창에 아래 텍스트를 입력
```javascript
console.log(Array.from(document.querySelectorAll('tbody>tr>td:nth-child(1)')).map(tr=>tr.textContent).join(', '));
```
3. <https://waifu2x.udp.jp/index.ko.html>(저해상도를 고해상도로 Upscaling)

## Error

1. 장시간 사용에 따른 Runtime Error 방지
- 크롬창에 F12누른뒤 콘솔창에 아래 텍스트를 입력

```javascript
function KeepClicking(){console.log("Clicking");document.querySelector("colab-connect-button").click()}setInterval(KeepClicking,60000)
```





