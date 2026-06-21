---
title: Cell State
tags: [딥러닝, RNN, 개념]
publish: true
---

[[LSTM]]의 장기 기억 전용 상태 $C_t$. 핵심은 갱신이 곱셈이 아니라 **더하기**라는 것:

$$C_t = f_t \odot C_{t-1} + i_t \odot \tilde{C}_t$$

곱셈으로 뭉개지지 않고 게이트로 일부만 조절하며 더해지니, 그래디언트가 거슬러 흘러도 거의 손실 없이 통과한다("정보 고속도로"). 이 더하기 트릭은 ResNet의 Skip Connection과 같은 발상이다.
