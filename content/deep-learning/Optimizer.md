---
title: Optimizer
tags:
  - 딥러닝
  - 개념
publish: true
---

기본 [[경사하강법]]의 약점(안장점에 갇힘, 지그재그 진동)을 고친 것.

- **Momentum**: 관성. 이전 방향을 기억해 평평한 곳도 뚫고 진동 줄임.
- **RMSProp**: 파라미터마다 [[학습률]] 자동 조정.
- **[[Adam]]**: Momentum+RMSProp. 사실상 기본 선택.
