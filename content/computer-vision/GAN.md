---
title: GAN
tags:
  - 컴퓨터비전
  - 모델
publish: true
---

Generative Adversarial Network. **생성자(Generator)**와 **판별자(Discriminator)**가 경쟁하며 학습하는 [[이미지 생성]] 모델.

생성자는 가짜 이미지를 만들고, 판별자는 진짜/가짜를 구분한다 — 위조범 vs 감별사. 서로 이기려 하며 생성자가 점점 진짜 같은 이미지를 만들게 된다.

선명한 이미지를 만들지만 약점이 있다: **mode collapse**(다양성을 잃고 비슷한 것만 생성), 학습 불안정(두 네트워크 균형 맞추기가 까다로움). 이 어려움 때문에 요즘은 안정적이고 고품질인 [[Diffusion]]에 주류를 내줬다.
