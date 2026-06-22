---
title: nn.Linear
tags:
  - PyTorch
  - 개념
publish: true
---

가장 기본적인 신경망 층. 정체는 **[[행렬곱]] + 편향**:

$$y = xW^T + b$$

`nn.Linear(in_features, out_features)`로 만든다. 예: `nn.Linear(784, 10)`은 784개 입력(28×28 픽셀)을 받아 10개 출력(0~9 클래스 점수)을 내고, 내부 가중치 $W$는 `(10, 784)` 행렬, 편향 $b$는 길이 10 벡터다(둘 다 자동 생성, `requires_grad=True`).

이게 [[다중 선형 회귀]]의 $Xw+b$의 PyTorch 버전이다 — 선형대수 → 회귀 → 신경망이 같은 식. 여러 개를 쌓고 사이에 [[ReLU]]를 끼우면 [[MLP]]가 되고, CNN은 이 자리에 `nn.Conv2d`를, RNN은 `nn.LSTM`을 쌓는다. 관련: [[nn.Module]].
