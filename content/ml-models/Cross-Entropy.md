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

분류의 표준 손실. "정답 클래스에 모델이 매긴 확률"을 최대화 = 그 음의 로그를 최소화. 즉 **분류의 [[최대우도추정|MLE]]**이다 → [[손실 함수와 MLE]].

PyTorch `nn.CrossEntropyLoss`는 [[Softmax]]가 내장돼 있어 출력층에 Softmax를 또 붙이면 안 된다.
