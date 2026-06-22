---
title: Context Vector
tags:
  - NLP
  - 개념
aliases:
  - 문맥 벡터
publish: true
---

[[Seq2Seq]]에서 Encoder가 입력 문장 전체를 압축한 벡터 하나(보통 Encoder RNN의 마지막 Hidden State). Decoder는 이 벡터 하나만 보고 출력 전체를 생성한다.

비유하면 통역사가 긴 문장을 한 번 통째로 듣고 외운 뒤, 메모도 안 보고 옮기는 것. 짧은 문장은 괜찮지만 **길어질수록 벡터 하나에 다 못 담아 앞부분 정보가 샌다**(정보 병목).

이 병목이 [[Attention]] 등장의 직접적 동기다 — Attention은 메모 하나가 아니라 매 출력 시점마다 입력 전체를 다시 보고 필요한 곳을 골라 본다. [[AutoEncoder]]의 [[Bottleneck]]과 닮은 "하나로 압축"의 한계를 보여주는 개념.
