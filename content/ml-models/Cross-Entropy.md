---
title: Cross-Entropy
tags:
  - 머신러닝
  - 손실함수
  - 개념
aliases:
  - 교차 엔트로피
publish: true
---

분류의 표준 [[손실 함수]]. 정답 클래스에 모델이 매긴 확률이 높을수록 손실이 작아진다.

$$L = -\sum_k y_k \log \hat{p}_k$$

정답 클래스($y_k=1$)에 대한 $-\log(\text{예측확률})$만 남는다 — 정답에 1.0을 줬으면 손실 0, 0.1밖에 안 줬으면 손실이 크다.

본질은 **분류의 [[최대우도추정|MLE]]** — "정답 클래스 확률을 최대화 = 그 음의 로그를 최소화"가 곧 Cross-Entropy다([[손실 함수와 MLE]]). 그래서 분류엔 이걸 쓴다.

⚠️ PyTorch `nn.CrossEntropyLoss`는 [[Softmax]]가 **내장**돼 있으니, 모델 출력층에 Softmax를 또 붙이지 말고 raw logit을 넣어야 한다(흔한 실수).
