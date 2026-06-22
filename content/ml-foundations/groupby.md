---
title: groupby
tags:
  - Pandas
  - 개념
publish: true
---

"그룹으로 묶어 집계"하는, 데이터 분석의 핵심 무기. 패턴은 **쪼개기(split) → 적용(apply) → 합치기(combine)**.

```python
df.groupby('sex')['survived'].mean()
# 성별로 묶어 → 생존율 평균 → 결과 표
```

이 한 줄로 "성별 생존율", "객실 등급별 평균 요금" 같은 인사이트가 바로 나온다. 탐색적 분석의 대부분은 "질문 → 무엇으로 그룹지을지 정하기 → 어떤 값을 집계할지 정하기" 패턴으로 풀린다.

여러 표를 키로 합치는 `merge`(SQL join), 위아래로 쌓는 `concat`과 함께 쓰면 강력하다. 관련: [[DataFrame]].
