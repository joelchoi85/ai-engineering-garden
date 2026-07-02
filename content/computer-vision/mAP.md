---
title: mAP
tags:
  - 컴퓨터비전
  - 평가
  - 개념
publish: true
---

mean Average Precision. [[객체 인식|Object Detection]]모델의 성능을 평가하는 표준 지표.

먼저 각 클래스마다 [[Precision과 Recall]] 곡선의 아래 넓이(Average Precision)를 구하고, 모든 클래스에 대해 평균낸다. 박스가 "맞았다"의 기준은 [[IoU]] 임계값으로 정하는데, COCO 벤치마크는 IoU 0.5부터 0.95까지 여러 임계값의 평균(`mAP@0.5:0.95`)을 쓴다.

즉 "여러 클래스 × 여러 엄격도"에서의 검출 정밀도를 한 숫자로 종합한 것. [[Precision과 Recall]]이 박스 단위로 다시 등장하는 셈이다.
