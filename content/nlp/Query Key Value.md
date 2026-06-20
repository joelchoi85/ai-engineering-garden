---
title: Query Key Value
tags:
  - NLP
  - 개념
aliases:
  - QKV
---

[[Attention]]의 3총사(도서관 비유). **Query**=내가 찾는 것, **Key**=각 단어의 검색용 이름표, **Value**=각 단어의 실제 내용.

$$\text{softmax}\!\left(\frac{QK^T}{\sqrt{d_k}}\right)V$$

내적($QK^T$)으로 유사도 → $\sqrt{d_k}$로 크기 조절 → [[Softmax]]로 가중치 → Value 가중합.
