---
title: Stable Diffusion
tags:
  - 컴퓨터비전
  - 모델
aliases:
  - Latent Diffusion
---

텍스트→이미지. 세 부품 조립: **[[VAE]]**(이미지를 잠재공간으로 압축) + **[[U-Net]]**(잠재공간에서 [[Diffusion|노이즈 제거]]) + **Text Encoder**([[Transformer]], [[Attention]]으로 텍스트 조건). 잠재공간에서 작업해 빠르다(Latent Diffusion).
