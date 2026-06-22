---
title: Confusion Matrix
tags:
  - 머신러닝
  - 평가
  - 개념
publish: true
---

분류 결과를 "실제 vs 예측"의 격자로 펼친 표. 행=실제 클래스, 열=예측 클래스. 대각선이 정답, 대각선 밖이 오답이다.

전체 정확도 하나로는 모델의 약점을 모른다 — 어떤 클래스를 어떤 클래스로 헷갈리는지 봐야 진짜 행동이 보인다(예: 비슷한 두 품종끼리 자주 혼동). `sklearn.metrics.confusion_matrix` + `seaborn.heatmap`으로 시각화한다.

여기서 [[Precision과 Recall]], F1이 계산된다. `classification_report`로 클래스별 지표를 한 표로 본다. 딥러닝에서도 그대로 쓰여 — 이미지 분류 모델 진단의 기본 도구이고, [[Grad-CAM]]과 함께 "왜 틀리나"를 파악한다.
