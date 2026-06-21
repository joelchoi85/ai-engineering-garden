---
title: AutoEncoder
tags:
  - 딥러닝
  - 네트워크
  - 모델
aliases:
  - 오토인코더
  - AE
publish: true
---

입력을 그대로 복원하게 학습하되, 가운데를 강제로 좁혀([[Bottleneck]]) 핵심 특징만 압축하게 만드는 모델. 인코더-디코더(모래시계) 구조.

**정답(라벨)이 필요 없다**(입력 자신이 정답). 변형: [[Denoising AE]], [[VAE]]. [[PCA]]의 압축을 신경망으로 확장한 것.
