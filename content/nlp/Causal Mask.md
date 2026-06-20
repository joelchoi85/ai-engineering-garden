---
title: Causal Mask
tags:
  - NLP
  - 개념
aliases:
  - 마스킹
---

[[Self-Attention]]에서 Decoder가 **미래 단어를 못 보게** 점수를 $-\infty$로 깔아 softmax 후 0으로 만드는 것. 다음 단어 예측에서 정답(미래)을 미리 보면 컨닝이니까. [[GPT와 BERT|GPT]]의 핵심.
