---
title: Causal Mask
tags:
  - NLP
  - 개념
aliases:
  - 마스킹
publish: true
---

[[Self-Attention]]에서 Decoder가 **미래 단어를 못 보게** 막는 장치. 다음 단어를 예측하는 모델이 정답(미래)을 미리 보면 컨닝이니까.

방법: attention 점수 행렬에서 미래 위치(자기보다 뒤)의 점수를 $-\infty$로 깔면, [[Softmax]] 통과 후 $e^{-\infty}=0$이라 가중치가 0이 된다. 즉 "지금까지 나온 단어만" 보고 다음을 예측하도록 강제(상삼각 마스킹).

이 마스킹 하나가 [[GPT와 BERT|GPT]] 계열의 핵심이다 — GPT는 마스킹된 Self-Attention으로 "다음 단어 맞히기"를 거대하게 키운 것. [[Seq2Seq]] Decoder의 자기회귀 원리와 같은 정신.
