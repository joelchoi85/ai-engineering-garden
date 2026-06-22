---
title: Adam
tags:
  - 딥러닝
  - 개념
publish: true
---

[[Optimizer]]의 사실상 기본값. **Momentum(관성)** 과 **RMSProp(파라미터별 학습률 자동 조정)** 을 합쳐, 안장점도 잘 빠져나오고 파라미터마다 적절한 보폭으로 움직인다.

실무에서 "뭘 써야 할지 모르겠으면 Adam"이라 할 만큼 안정적이고 빠르게 수렴한다. PyTorch에선 SGD에서 Adam으로 바꾸는 데 한 줄이면 된다:

```python
optimizer = torch.optim.Adam(model.parameters(), lr=0.001)
```

[[학습률]]을 자동 조정해주지만 초기 lr은 여전히 정해야 한다(보통 0.001). 관련: [[경사하강법]], [[학습률 스케줄링]].
