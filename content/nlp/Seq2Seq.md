---
title: Seq2Seq
tags:
  - NLP
  - 모델
aliases:
  - 시퀀스 투 시퀀스
publish: true
---

시퀀스→시퀀스(번역 등). [[RNN]] 두 개: **Encoder**가 입력을 요약 메모([[Context Vector]])로 압축, **Decoder**가 그걸 받아 한 단어씩 자기회귀 생성(`<SOS>`~`<EOS>`).

입력을 다 듣고 출력을 시작하니 길이가 달라도 된다. 학습은 [[Teacher Forcing]]. 한계는 [[Context Vector]] 병목 → [[Attention]].
