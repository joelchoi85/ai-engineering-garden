---
title: model.eval과 no_grad
tags:
  - PyTorch
  - 개념
publish: true
---

추론할 때 둘 다 쓰는 게 규칙(다른 일을 함):

- `model.eval()`: 층을 추론 모드로. [[Dropout]]·[[배치 정규화]]는 학습/추론 동작이 다름.
- `torch.no_grad()`: [[Autograd]]를 꺼 메모리·속도 절약.

`no_grad()`만 쓰고 `eval()`을 빼먹으면 Dropout이 켜진 채라 예측이 매번 달라진다.
