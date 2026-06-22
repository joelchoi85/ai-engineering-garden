---
title: Autograd
tags:
  - PyTorch
  - 개념
publish: true
---

PyTorch의 자동 미분 엔진. 손실의 기울기([[순전파와 역전파]]의 역전파)를 손으로 미분식 풀 필요 없이 자동 계산해준다.

단 세 줄이 핵심:
```python
x = torch.tensor(2.0, requires_grad=True)  # 1. 추적 표시
y = x ** 2                                  # 2. 연산 (계산 그래프 기록)
y.backward()                                # 3. 거꾸로 미분
print(x.grad)   # 4.0  (dy/dx = 2x, x=2)
```

`requires_grad=True`인 텐서로 연산하면 PyTorch가 그 과정을 **계산 그래프**로 기록해두고, `.backward()`를 부르면 연쇄법칙으로 각 변수의 `.grad`에 기울기를 채운다. 식이 아무리 복잡해도, 합성함수가 몇 겹이든 정확히 미분한다. 신경망 학습의 심장이며, 우리가 직접 짜면 끔찍한 [[그래디언트 소실]] 계산까지 다 자동이다.
