---
title: LSTM
tags:
  - 딥러닝
  - 네트워크
  - 모델
aliases:
  - Long Short-Term Memory
publish: true
---

Long Short-Term Memory. 기본 [[RNN]]의 [[장기 의존성]] 문제를 **게이트**로 푼 모델. 핵심은 출력과 분리된 장기 기억 전용 상태 [[Cell State]]다.

```mermaid
flowchart LR
    Cin[이전 Cell State] --> F((× Forget))
    F --> Add((+ Input))
    Add --> Cout[새 Cell State]
    Cout --> O((× Output))
    O --> H[Hidden State 출력]
```

세 게이트가 정보 흐름을 조절한다:
- **Forget** — 이전 기억 중 뭘 버릴지
- **Input** — 새 입력 중 뭘 추가할지
- **Output** — 기억 중 뭘 이번 출력으로 내보낼지

게이트 식을 외우는 비법 한 줄: **시그모이드(0~1)는 "얼마나"(수도꼭지), tanh(-1~1)는 "무엇을"(정보).** 더 가벼운 변형이 [[GRU]]. 자세한 보존 원리는 [[Cell State]].
