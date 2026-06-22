---
title: Grad-CAM
tags:
  - 컴퓨터비전
  - 개념
publish: true
---

학습된 모델이 예측할 때 **이미지의 어디를 보고 판단했는지**를 히트맵으로 보여주는 도구(Gradient-weighted Class Activation Mapping).

"고양이"라고 판단한 근거가 진짜 고양이 얼굴인지, 엉뚱한 배경(식기 등)인지 눈으로 확인된다. 맞춘 이미지는 보통 동물 얼굴/몸을, 틀린 이미지는 엉뚱한 영역을 보고 있는 경우가 보인다.

정확도 숫자만으론 모를 **모델 해석가능성(interpretability)**을 준다. [[Confusion Matrix]](어떤 클래스를 헷갈리나) + 오분류 이미지 보기 + Grad-CAM(왜 그렇게 판단했나)이 모델 진단 3종 세트다. [[Attention]] 가중치 시각화도 같은 정신(모델이 어디에 집중하나).
