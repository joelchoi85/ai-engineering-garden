---
title: Transformer
tags:
  - NLP
  - 네트워크
  - 모델
publish: true
---

RNN을 빼고 [[Self-Attention]]만으로 가는 모델(2017, "Attention is all you need"). 현대 LLM(GPT·Claude)의 뼈대.

CNN이 Conv 블록을, RNN이 시점을 쌓듯, Transformer는 **블록을 쌓는다**. 블록 하나는 네 부품:
1. [[Multi-Head Attention]] (단어들이 서로 봄)
2. Add & Norm ([[Skip Connection|잔차]] + LayerNorm)
3. Feed-Forward (단어별 작은 MLP)
4. Add & Norm

순서 정보는 [[위치 인코딩]]으로 따로 넣는다. 핵심 이점은 **병렬 처리** — RNN의 순차 족쇄를 풀어 거대한 데이터로 빠르게 학습할 수 있게 됐고, 이게 LLM 폭발의 토대다. 잔차연결·LayerNorm은 이미 배운 부품([[Skip Connection]]·[[배치 정규화]] 사촌)의 재조립이라, 진짜 새 건 어텐션·위치인코딩뿐이다.
