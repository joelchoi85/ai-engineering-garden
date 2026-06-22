---
title: Stable Diffusion
tags:
  - 컴퓨터비전
  - 모델
aliases:
  - Latent Diffusion
publish: true
---

텍스트로 이미지를 만드는 대표 모델(=Latent Diffusion). **세 부품의 조립**이고, 셋 다 이미 배운 것이다:

1. **[[VAE]]** — 이미지를 작은 **잠재공간(latent)**으로 압축. 픽셀이 아니라 잠재에서 작업해 계산을 확 줄인다("Latent" Diffusion의 핵심, [[Bottleneck]] 발상).
2. **[[U-Net]]** — 잠재공간에서 노이즈를 제거([[Diffusion]]).
3. **Text Encoder** — 프롬프트를 벡터로([[Transformer]]). [[Attention]](cross-attention)으로 "고양이"라는 단어가 이미지 어디에 영향 줄지 연결.

즉 Stable Diffusion = VAE + U-Net + Diffusion + Attention 텍스트 조건. 완전히 새로운 게 아니라 내가 판 조각들의 조합이라는 게 핵심.
