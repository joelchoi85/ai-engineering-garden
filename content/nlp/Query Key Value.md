---
title: Query Key Value
tags:
  - NLP
  - 개념
aliases:
  - QKV
publish: true
---

[[Attention]]을 계산하는 3총사. 도서관 비유로 잡으면 쉽다:
- **Query(Q)** — 내가 찾는 것("지금 이 단어를 만들려는데 입력 어디가 관련 있지?")
- **Key(K)** — 각 입력 단어가 내건 검색용 이름표
- **Value(V)** — 각 입력 단어가 실제로 담은 정보

$$\text{Attention}(Q,K,V) = \text{softmax}\!\left(\frac{QK^T}{\sqrt{d_k}}\right)V$$

왼쪽부터 한 조각씩: ① $QK^T$ = Query·Key **내적**으로 유사도 점수, ② $\div\sqrt{d_k}$ = 점수가 너무 커져 [[Softmax]]가 한쪽으로 쏠리는 걸 막는 크기 조절, ③ **Softmax** = 합이 1인 가중치로, ④ $\times V$ = 그 가중치로 Value들을 가중 평균 = 결과. 즉 "질문·이름표 대조 → 점수 → 내용을 점수대로 섞기"인 검색 한 판이다.
