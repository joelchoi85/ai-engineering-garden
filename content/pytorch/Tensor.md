---
title: Tensor
tags:
  - PyTorch
  - 개념
publish: true
---

PyTorch의 다차원 배열. [[NumPy]] 배열과 거의 같지만 두 가지가 더 있다: **[[Autograd]]**(자동 미분), **GPU 가속**(`.to(device)`).

디버깅의 절반은 `shape`와 `dtype` 확인. 신경망은 보통 `(N, C, H, W)` 모양을 기대한다.
