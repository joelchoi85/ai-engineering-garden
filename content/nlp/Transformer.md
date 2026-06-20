---
title: Transformer
tags:
  - NLP
  - 네트워크
  - 모델
---

RNN을 빼고 [[Self-Attention]]만으로 가는 모델(2017, "Attention is all you need"). 블록을 쌓는다: [[Multi-Head Attention]] + Add&Norm([[Skip Connection|잔차]]+LayerNorm) + FFN + Add&Norm.

순서는 [[위치 인코딩]]으로. 병렬 학습이 가능해 [[GPT와 BERT|LLM]]의 토대가 됐다.
