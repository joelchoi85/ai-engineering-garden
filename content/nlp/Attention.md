---
title: Attention
tags:
  - NLP
  - 개념
aliases:
  - 어텐션
publish: true
---

[[Seq2Seq]]의 [[Context Vector]] 병목을 푸는 메커니즘. 한 줄: **"Decoder가 단어를 만들 때마다 입력 전체를 다시 보되, 지금 필요한 곳에 더 큰 가중치를 둬서 본다."**

메모 하나가 아니라 매 출력 시점마다 새로 계산한 "맞춤 요약"을 본다. "étudiant(학생)"를 만들 땐 입력의 "student"에 집중한 요약, 다른 단어를 만들 땐 또 다른 곳에 집중. 입력 정보가 벡터 하나에 갇히지 않아 긴 문장에 강하다.

계산 방식은 [[Query Key Value]]: 유사도 점수 → [[Softmax]] 가중치 → 값의 가중합. 가중치를 시각화하면 "출력↔입력" 정렬이 보여 해석가능성도 준다([[Grad-CAM]]처럼). Q·K·V를 같은 문장에서 뽑으면 [[Self-Attention]] → [[Transformer]].
