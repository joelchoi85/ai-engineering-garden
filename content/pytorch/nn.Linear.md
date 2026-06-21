---
title: nn.Linear
tags:
  - PyTorch
  - 개념
publish: true
---

선형 변환 층. 정체는 **[[행렬곱]] + 편향**: $y = Wx + b$. `nn.Linear(784, 10)`이면 784입력→10출력, 내부 W는 (10,784).

[[다중 선형 회귀]]·[[MLP]]의 한 층. 여러 개 쌓고 [[ReLU]]를 끼우면 신경망이 된다.
