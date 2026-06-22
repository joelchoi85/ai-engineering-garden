---
title: GRU
tags:
  - 딥러닝
  - 네트워크
  - 모델
publish: true
---

Gated Recurrent Unit(2014). [[LSTM]]을 더 가볍게 만든 버전.

LSTM은 게이트가 3개라 파라미터가 많고 느린데, GRU는:
- 게이트 2개(**Update**, **Reset**)로 단순화
- [[Cell State]] 없이 Hidden State 하나로 통합

**Update Gate**가 LSTM의 Forget+Input을 합친 역할("이전 걸 얼마나 유지하고 새 걸 얼마나 넣을지"를 한 번에), **Reset Gate**는 "새 후보를 만들 때 이전 상태를 얼마나 무시할지"를 정한다. 가볍고 빠르며 성능은 LSTM과 비슷한 경우가 많아, 둘 중 뭘 쓸지는 보통 둘 다 해보고 정한다.
