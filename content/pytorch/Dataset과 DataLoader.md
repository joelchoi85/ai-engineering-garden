---
title: Dataset과 DataLoader
tags:
  - PyTorch
  - 개념
---

큰 데이터를 [[미니배치 경사하강법|미니배치]]로 흘리는 도구. **Dataset**: 한 샘플씩 꺼내는 법(`__len__`,`__getitem__`). **DataLoader**: `(x_batch, y_batch)`로 묶어 던져줌(셔플·병렬 자동).
