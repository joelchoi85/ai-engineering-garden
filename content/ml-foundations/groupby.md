---
title: groupby
tags:
  - Pandas
  - 개념
publish: true
---

"그룹으로 묶어 집계"하는 데이터 분석의 핵심 무기. `df.groupby('sex')['survived'].mean()` 한 줄로 "성별 생존율" 같은 인사이트가 나온다.

패턴: 질문 → groupby로 쪼개기 → 집계. 관련: [[DataFrame]].
