---
title: U-Net
tags:
  - 컴퓨터비전
  - 모델
---

[[Image Segmentation]]의 대표. 사실상 [[AutoEncoder]]다 — 인코더로 줄여 의미 추출, 디코더로 해상도 복원, 픽셀별 클래스 예측. 결정적 차이는 [[Skip Connection]]으로 고해상도 디테일을 디코더에 직접 전달. [[Stable Diffusion]]의 노이즈 제거 엔진으로도 쓰인다.
