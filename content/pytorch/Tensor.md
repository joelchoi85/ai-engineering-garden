---
title: Tensor
tags:
  - PyTorch
  - 개념
publish: true
---

PyTorch의 기본 자료구조. [[NumPy]]의 `ndarray`와 거의 똑같이 생긴 다차원 배열이고, `torch.zeros`·인덱싱·`@`(행렬곱)까지 사용법이 같다. 결정적 차이 둘:

1. **[[Autograd]]** — 자동 미분. `requires_grad=True`를 붙이면 연산을 기록해 기울기를 자동 계산.
2. **GPU 가속** — `.to(device)`로 연산을 GPU(Mac은 mps)로 보내 수십~수백 배 빠르게.

차원: 0D 스칼라, 1D [[벡터]], 2D [[행렬]], 그 이상 텐서. 신경망은 보통 `(배치, 채널, 높이, 너비)` = `(N, C, H, W)` 모양을 기대한다.

> 💡 디버깅의 절반은 `tensor.shape`와 `tensor.dtype` 확인이다. 에러의 대부분이 모양·타입 불일치다.
