---
title: U-Net
tags:
  - 컴퓨터비전
  - 모델
publish: true
---

[[Image Segmentation]](특히 semantic)의 대표 모델. **사실상 [[AutoEncoder]]다** — 인코더로 이미지를 줄여 의미를 뽑고(다운샘플), 디코더로 다시 원래 해상도로 키우며(업샘플) 픽셀별 클래스를 예측한다(모래시계 모양).

결정적 차이는 **[[Skip Connection]]** — 인코더의 고해상도 정보를 같은 단계의 디코더로 직접 이어줘 경계를 또렷하게 살린다(U자 모양의 가로 연결). 이게 ResNet/LSTM의 "더하기로 정보 보존"과 같은 발상.

활용 폭이 넓다 — 의료영상 분할의 표준이고, [[Stable Diffusion]]에서는 잠재공간의 노이즈 제거 엔진으로 쓰인다([[Diffusion]]).
