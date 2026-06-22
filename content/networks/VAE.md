---
title: VAE
tags:
  - 딥러닝
  - 네트워크
  - 모델
aliases:
  - Variational AutoEncoder
publish: true
---

Variational AutoEncoder. [[AutoEncoder]]의 잠재 $z$를 "점 하나"가 아니라 **분포**(평균·분산)로 보고, 거기서 샘플링해 **새 데이터를 생성**한다.

일반 AE의 잠재공간은 군데군데 비어 있어 아무 점이나 디코딩하면 깨진 이미지가 나오는데, VAE는 잠재공간을 매끄러운 분포로 정규화해 샘플링한 점도 그럴듯한 이미지가 되게 한다. 그래서 생성 모델로 쓸 수 있다.

[[이미지 생성]] 세 계보(VAE/GAN/[[Diffusion]]) 중 하나이고, 결과가 다소 흐릿한 약점이 있다. 한편 [[Stable Diffusion]]에서는 이미지를 잠재공간으로 압축하는 단계로 VAE가 쓰인다([[Bottleneck]] 발상).
