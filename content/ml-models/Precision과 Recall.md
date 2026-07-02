---
title: Precision과 Recall
tags:
  - 머신러닝
  - 평가
  - 개념
publish: true
aliases:
  - 정밀도와 재현율
---

[[Confusion Matrix]]에서 나오는 두 핵심 지표.

- **Precision(정밀도)** — 모델이 "양성"이라 한 것 중 진짜 양성 비율. "거짓 경보가 적은가". (스팸함에 넣은 것 중 진짜 스팸 비율)
  $$\frac{TP}{TP+FP}$$
- **Recall(재현율)** — 진짜 양성 중 모델이 잡아낸 비율. "놓치지 않는가". (실제 스팸 중 걸러낸 비율)
  $$\frac{TP}{TP+FN}$$
- **F1** — 둘의 조화평균. 한쪽만 높은 걸 방지.

![Precision-Recall 곡선](https://cdn.ul.run/i/f37cb774ce8d91ae1d16ace87ec3abee.avif)


둘은 보통 **트레이드오프**다 — 기준을 빡빡하게 하면 Precision↑ Recall↓. 문제마다 뭐가 중요한지 다르다: **암 진단은 Recall이 중요**(놓치면 큰일), 스팸 분류는 Precision도 중요(정상 메일을 스팸 처리하면 곤란). 딥러닝 분류 진단에서도 그대로 쓴다.
