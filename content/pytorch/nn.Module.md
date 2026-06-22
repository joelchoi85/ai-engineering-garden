---
title: nn.Module
tags:
  - PyTorch
  - 개념
publish: true
---

PyTorch에서 모델을 정의하는 표준 방식. 가중치와 forward 동작을 한 객체에 묶는다([[객체지향]]). 모든 모델이 이걸 [[상속과 다형성|상속]]한다.

```python
class MLP(nn.Module):
    def __init__(self):
        super().__init__()              # 빼먹으면 작동 안 함!
        self.fc1 = nn.Linear(784, 128)  # 층 선언
        self.relu = nn.ReLU()
        self.fc2 = nn.Linear(128, 10)
    def forward(self, x):               # 데이터 흐름 정의
        return self.fc2(self.relu(self.fc1(x)))
```

- `__init__`에서 쓸 층을 선언, `forward`에서 입력이 흐르는 순서를 정의.
- 호출은 `model(x)` — `model.forward(x)`가 아니라(자동 호출, `__call__` [[던더 메소드]] 덕분).
- `model.parameters()`로 모든 가중치를 [[Optimizer]]에 한 번에 넘긴다.

관련: [[nn.Linear]], [[model.eval과 no_grad]].
