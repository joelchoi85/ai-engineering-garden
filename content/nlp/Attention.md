---
title: Attention
tags:
  - NLP
  - 개념
aliases:
  - 어텐션
---

[[Context Vector]] 병목의 해법. "Decoder가 단어를 만들 때마다 **입력 전체를 다시 보되 지금 필요한 곳에 가중치**를 둬서 본다". 매 시점 맞춤 요약을 만든다.

계산: [[Query Key Value]]. 자기 자신을 보면 [[Self-Attention]] → [[Transformer]].
