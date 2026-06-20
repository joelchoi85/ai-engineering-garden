---
title: LSTM
tags: [딥러닝, RNN, 개념]
aliases: [Long Short-Term Memory]
---

기본 RNN의 장기 의존성 문제를 게이트로 푼 모델. 핵심은 [[Cell State]]라는 별도 메모장.

```mermaid
flowchart LR
    Cin[이전 Cell State] --> F((× Forget))
    F --> Add((+ Input))
    Add --> Cout[새 Cell State]
    Cout --> O((× Output))
    O --> H[Hidden State 출력]
```

세 게이트(Forget/Input/Output)는 시그모이드(0~1, "얼마나"), 후보는 tanh(-1~1, "무엇을"). 자세히는 [[Cell State]] 참고.
