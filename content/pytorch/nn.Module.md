---
title: nn.Module
tags:
  - PyTorch
  - 개념
publish: true
---

PyTorch에서 모델을 정의하는 표준 방식. 가중치와 forward 동작을 한 객체에 묶는다. `__init__`에서 층 선언, `forward`에서 흐름 정의. `model(x)`로 호출(`forward` 자동).

[[상속과 다형성]]의 상속 패턴. 관련: [[nn.Linear]], [[Optimizer]].
