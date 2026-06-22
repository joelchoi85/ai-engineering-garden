---
title: CNN 발전사
tags:
  - 딥러닝
  - 개념
publish: true
---

CNN의 발전은 각 모델의 "핵심 혁신 한 줄"로 요약된다 — 의외로 짧다.

| 모델 | 연도 | 핵심 한 방 |
|------|------|-----------|
| LeNet | 1998 | Conv→Pool→FC라는 기본 골격 정립 |
| AlexNet | 2012 | [[ReLU]] + [[Dropout]]로 깊은 CNN 학습 가능 |
| VGG | 2014 | 3×3 필터만 깊게 반복(단순함의 힘) |
| GoogLeNet | 2014 | Inception(1×1·3×3·5×5 동시 적용) |
| [[ResNet]] | 2015 | [[Skip Connection]] `F(x)+x` |

AlexNet이 ImageNet 오류율을 26%→16%로 떨군 게 딥러닝 폭발의 신호탄이었고, ResNet의 잔차 연결이 "깊이의 벽"을 넘었다. 코드로 보면 각 혁신이 짧은 변경이라는 게 인상적이다.
