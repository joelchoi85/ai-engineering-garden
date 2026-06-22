---
title: GridSearchCV
tags:
  - 머신러닝
  - 도구
  - 개념
publish: true
---

[[하이퍼파라미터]] 후보들을 격자(grid)로 늘어놓고 **모든 조합을 [[교차 검증]]으로 시도해** 가장 좋은 조합을 자동으로 찾아주는 sklearn 도구.

```python
GridSearchCV(model, {'alpha':[0.1,0.5,1.0]}, cv=5)
```

위는 alpha 3개 후보를 각각 5-fold 교차검증으로 평가해 best를 고른다. "여러 후보 × 교차검증"을 한 번에 묶은 것. 후보가 너무 많으면 조합이 폭발하므로(예: 3×3×3=27), 무작위로 일부만 보는 RandomizedSearch나 베이지안 최적화를 쓰기도 한다.
