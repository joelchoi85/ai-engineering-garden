---
title: Autograd
tags:
  - PyTorch
  - 개념
publish: true
---

자동 미분. 손실의 기울기를 손으로 미분할 필요 없이 PyTorch가 계산해준다. 세 줄:

```python
x = torch.tensor(2.0, requires_grad=True)
y = x ** 2
y.backward()   # x.grad == 4.0
```

[[순전파와 역전파]]의 역전파를 자동화. 신경망 학습의 심장.
