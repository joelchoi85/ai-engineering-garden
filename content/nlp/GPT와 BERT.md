---
title: GPT와 BERT
tags:
  - NLP
  - 모델
  - 개념
publish: true
---

같은 [[Transformer]] 블록을 쓰지만 조립이 다른 두 갈래.

| | GPT 계열 | BERT 계열 |
|---|---|---|
| 구조 | Decoder-only([[Causal Mask]] O) | Encoder-only(양방향) |
| 학습 | 다음 단어 맞히기 | 가린 단어 맞히기 |
| 잘하는 일 | **생성**(글쓰기·대화) | **이해**(분류·검색) |

- **GPT** — [[Causal Mask]]로 미래를 가린 채 "지금까지의 말 → 다음 단어"를 예측. 내가 쓰는 ChatGPT·Claude가 이 Decoder-only를 거대하게 키운 것. [[Seq2Seq]] Decoder의 자기회귀가 여기까지 이어진다.
- **BERT** — 마스킹 없이 양방향으로 문맥을 봐서 문장을 깊이 이해. 분류·검색에 강함.

둘 다 [[전이 학습]]으로 쓴다 — 대량 텍스트로 사전학습한 뒤 미세조정.
