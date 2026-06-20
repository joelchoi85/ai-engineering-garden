---
title: ReLU
tags: [딥러닝, 개념, 활성화함수]
aliases: [Rectified Linear Unit]
---

$\text{ReLU}(x) = \max(0, x)$ — 음수면 0, 양수면 그대로. 가장 널리 쓰이는 [[활성화 함수]].

- 양수 영역 기울기가 1로 일정 → 그래디언트 소실 완화
- 계산이 매우 빠름
- 한계: 음수만 들어오면 죽는 뉴런(Dead ReLU)
