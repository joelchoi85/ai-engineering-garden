---
title: Self-Attention
tags:
  - NLP
  - 개념
publish: true
---

[[Query Key Value|Q·K·V]]를 **같은 문장에서** 뽑아 문장이 자기 자신을 보는 것. 단어끼리 서로 가중치를 매겨 "it이 누구를 가리키나" 같은 관계를 직접 잡는다.

RNN처럼 순차가 아니라 **모든 단어가 모든 단어를 동시에** 본다 → 병렬화 가능 → [[Transformer]].
