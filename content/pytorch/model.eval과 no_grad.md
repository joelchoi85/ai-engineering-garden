---
title: model.eval과 no_grad
tags:
  - PyTorch
  - 개념
publish: true
---

추론(예측)할 때 함께 쓰는 두 가지. **서로 다른 일**을 하므로 둘 다 필요하다.

| 도구 | 역할 |
|------|------|
| `model.eval()` | 모델 안 층들을 **추론 모드**로 전환. [[Dropout]]은 끄고(다 켬), [[배치 정규화]]는 저장된 통계를 쓰게 함 |
| `torch.no_grad()` | **[[Autograd]]를 끔**. 계산 그래프를 안 만들어 메모리·속도 절약 |

```python
model.eval()
with torch.no_grad():
    pred = model(x_new)
```

⚠️ 흔한 실수: `no_grad()`만 쓰고 `model.eval()`을 빼먹으면 → [[Dropout]]이 켜진 채라 예측이 매번 달라지고, [[배치 정규화]]도 엉뚱한 통계를 써서 결과가 망가진다. 다시 학습으로 돌아갈 땐 `model.train()`. [[nn.Module]]이 이 모드 전환을 지원한다.
