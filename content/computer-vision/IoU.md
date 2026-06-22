---
title: IoU
tags:
  - 컴퓨터비전
  - 개념
publish: true
---

Intersection over Union. 예측 박스와 정답 박스가 **얼마나 겹치는지** 재는 값:

$$\text{IoU} = \frac{\text{교집합 넓이}}{\text{합집합 넓이}}$$

0(안 겹침)~1(완전 일치). 보통 0.5 이상이면 "맞게 검출했다"고 본다. [[객체 인식]]의 박스 정답 판정 기준이자, [[NMS]](중복 제거)와 [[mAP]](평가)의 핵심 재료다. 분할에서도 마스크 겹침을 재는 데 쓴다(IoU 기반 Dice loss 등).
