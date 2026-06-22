---
title: Series
tags:
  - Pandas
  - 개념
publish: true
---

[[DataFrame]]의 한 열(또는 한 행). 1차원 데이터다.

[[NumPy]]의 1차원 배열과 비슷하지만 결정적 차이는 **인덱스가 함께 붙는다**는 것 — 각 값에 라벨(행 번호나 이름)이 따라다녀, 정렬·정합·결측 처리가 편하다.

관계를 기억하면 쉽다: **DataFrame은 여러 Series를 모은 것**이고, DataFrame에서 한 열을 꺼내면 Series가 된다(`df['age']`). 평균·합 같은 집계(`s.mean()`)나 조건 필터(`s > 30`)를 바로 적용할 수 있다.
