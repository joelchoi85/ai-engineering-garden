---
title: Dataset과 DataLoader
tags:
  - PyTorch
  - 개념
publish: true
---

큰 데이터를 [[미니배치 경사하강법|미니배치]]로 흘려보내는 표준 도구. 데이터가 6만 개(MNIST)면 한 번에 못 넣으니 쪼개야 한다.

- **`Dataset`** — "내 데이터가 무엇이고 어떻게 한 샘플씩 꺼내는가". `__len__`(전체 개수), `__getitem__`(idx로 한 샘플 반환) 두 메소드를 구현.
- **`DataLoader`** — Dataset을 받아 `(x_batch, y_batch)` 미니배치로 묶어 던져준다. 셔플, 병렬 로딩도 자동.

```python
loader = DataLoader(my_dataset, batch_size=64, shuffle=True)
for x_batch, y_batch in loader:   # 학습 루프에서 한 배치씩
    ...
```

[[배치 사이즈]]를 여기서 정한다. 학습 루프는 이 loader를 돌며 forward→loss→backward→step을 반복한다.
