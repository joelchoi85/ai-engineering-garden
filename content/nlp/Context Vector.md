---
title: Context Vector
tags:
  - NLP
  - 개념
aliases:
  - 문맥 벡터
publish: true
---

[[Seq2Seq]] Encoder가 입력 문장 전체를 압축한 벡터 하나(마지막 Hidden State). Decoder는 이 하나만 보고 출력을 만든다.

문제: 긴 문장도 벡터 하나에 욱여넣어야 해 앞이 샌다(병목). 이 병목을 푼 게 [[Attention]].
