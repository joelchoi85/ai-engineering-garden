---
title: Seq2Seq
tags:
  - NLP
  - 모델
aliases:
  - 시퀀스 투 시퀀스
publish: true
---

시퀀스를 받아 시퀀스를 내놓는 모델(번역, 요약). [[RNN]] 두 개로 구성된다.

- **Encoder** — 입력 문장을 한 단어씩 읽어 요약 메모 하나([[Context Vector]])로 압축.
- **Decoder** — 그 메모를 받아 출력 문장을 한 단어씩 생성. `<SOS>`(시작)로 시작해 자기가 뱉은 단어를 다음 입력으로 다시 먹으며(자기회귀) `<EOS>`(끝)까지.

입력을 **다 읽고 나서** 출력을 시작하므로 입력·출력 길이가 달라도 된다(영어 4단어 → 프랑스어 3단어). 학습은 [[Teacher Forcing]], 평가는 [[BLEU]].

한계: 긴 문장도 [[Context Vector]] 하나에 욱여넣어야 해 앞부분 정보가 샌다(병목) → 이를 푼 게 [[Attention]]이고, 그 흐름이 [[Transformer]]로 이어진다.
