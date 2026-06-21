---
title: Skip Connection
tags:
  - 딥러닝
  - 개념
aliases:
  - 잔차 연결
  - Residual Connection
publish: true
---

블록 출력에 입력을 그대로 더하는 것: `return F(x) + x`. [[그래디언트 소실]]을 막는 "직통 통로(×1)"를 뚫어 152층까지 안정적으로 학습 가능하게 한다([[ResNet]]).

이 "더하기로 그래디언트 살리기"는 [[Cell State]](LSTM), [[Transformer]] 잔차연결, [[U-Net]]과 **같은 트릭**이다.
