---
title: Cell State
tags:
  - 딥러닝
  - RNN
  - 개념
publish: true
---

[[LSTM]]이 [[장기 의존성]]을 푸는 진짜 비결. 장기 기억 전용 상태 $C_t$로, 시퀀스를 따라 한 줄로 흐르며 게이트로 조금씩만 수정된다.

$$C_t = f_t \odot C_{t-1} + i_t \odot \tilde{C}_t$$

($\odot$ 은 원소별 곱) 핵심은 **곱셈이 아니라 더하기로 누적**된다는 점이다. 기본 RNN처럼 가중치 행렬에 통과시켜 뭉개는 게 아니라, Forget 게이트로 일부 지우고($f_t \odot C_{t-1}$) 새 정보를 더할 뿐($+\,i_t \odot \tilde{C}_t$)이다.

그래서 그래디언트가 거슬러 흐를 때 이 경로에서 거의 손실 없이 통과한다 — 비유로 기본 RNN의 Hidden State가 **강물**(섞임)이라면 Cell State는 **고속도로**(거의 그대로 달림). 이 "더하기로 보존" 트릭은 [[Skip Connection]](ResNet)과 정확히 같은 발상이다.
