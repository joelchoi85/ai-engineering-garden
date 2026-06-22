---
title: R-CNN
tags:
  - 컴퓨터비전
  - 모델
publish: true
---

**2-stage** [[객체 인식]] 모델 계열(2014~). ① 먼저 "객체가 있을 법한 영역"을 후보로 제안하고 → ② 각 영역을 [[CNN]]으로 분류하고 박스를 정밀화한다.

R-CNN → Fast R-CNN → Faster R-CNN으로 발전하며 빨라졌다. [[YOLO]] 같은 1-stage보다 느리지만 정확도가 높은 편.

확장형 **Mask R-CNN**은 검출에 **픽셀 마스크 분기**를 하나 더 붙여 [[Image Segmentation]](instance segmentation)을 한다 — "검출 + 각 박스 안 픽셀 마스크". 객체 인식이 분할로 자연스럽게 이어지는 지점.
