---
title: Image Segmentation
tags:
  - 컴퓨터비전
  - 개념
aliases:
  - 세그멘테이션
publish: true
---

[[객체 인식]]의 네모 박스를 넘어, **픽셀 하나하나에 라벨**을 붙이는 것. 박스 안엔 배경 픽셀도 섞이지만, 분할은 객체의 정확한 윤곽을 딴다. 자율주행(도로/차/사람), 의료영상(종양 영역)에 필수.

세 종류:
- **Semantic** — 픽셀마다 클래스만(고양이 3마리가 다 같은 색)
- **Instance** — 개체까지 구분(고양이1·2·3 다른 색)
- **Panoptic** — 둘 통합(사물은 개체별, 배경은 클래스별로 빈틈없이)

대표 모델: [[U-Net]](semantic), Mask [[R-CNN]](instance), [[SAM]](프롬프트 기반). 손실은 픽셀별 [[Cross-Entropy]] + IoU 기반(Dice) 등.
