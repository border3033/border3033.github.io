---
layout: post
title: 최소침습 의료용 로봇 설계 및 실험
description: 6개월간 외부 연구원으로 리즈대학교에서 자기장으로 구동되는 최소침습 의료용 연성 로봇에 Fibre Jamming 기반 가변강성 구조를 적용하는 연구를 수행했습니다.
skills: 
- Fusion 360 (Autodesk)
- MATLAB
- 3D 프린팅
- 파라메트릭 실험
- lightBurn (레이저 커팅)
main-image: /MSCR main.png
---

## 프로젝트 개요

- **프로젝트:** Design, Fabrication, and Characterisation of Magnetic Soft Continuum Robots with Variable Stiffness via Fibre Jamming
- **연구 기간:** 2025년 7월 ~ 2025년 12월 
- **연구 기관:** 영국 리즈대학교 STORM Lab
- **연구 형태:** 기계공학 석사 논문 (외부 연구원)
- **담당 역할:** 로봇 설계 · 제작 · 실험 시스템 구축 · 파라메트릭 실험 · 데이터 분석 및 성능 검증

<!-- 대표 사진 1장: 완성된 로봇 또는 전체 실험 셋업 -->



## 문제 정의

- **MSCR이란?** 자기장을 이용해 비접촉으로 구동되는 초소형 연성 로봇으로, 높은 유연성과 낮은 조직 손상 위험을 바탕으로 최소침습 의료 분야에 활용될 수 있음.

- **유연성과 강성의 상충관계:** 부드러운 구조는 인체 조직에 가해지는 부담을 줄이지만, 심혈관 및 폐 등에서 외력이 작용할 경우 형태와 위치를 유지하기 어려움. 따라서 필요에 따라 강성을 조절하는 기술이 요구됨.

- **기존 소재의 한계:** 기존 MSCR은 주로 실리콘 기반으로 제작됨. 본 연구에서는 두께 **38 μm의 열가소성 엘라스토머(TPE)** 필름을 활용하여 가변 강성 구조를 구현하고자 함.

- **미검증 설계 특성:** TPE 필름은 양압 구동 연성 로봇에 활용된 사례가 있으나, 섬유 재밍과 음압 적용 및 비대칭 구조에 따른 **방향별 강성 변화**에 대한 연구가 부족함.



## 연구 목표

- MSCR 내부에 **Fibre Jamming 기반 가변 강성 구조** 설계 및 통합
- TPE sleeve, 구리 섬유, NdFeB 자석을 활용하여 **직접 제조**
- 섬유 수, 진공압, 굽힘 방향을 변화시키는 **파라메트릭 실험 수행**
- MATLAB을 활용한 변형 **데이터 분석** 및 Soft/Rigid 상태의 강성 변화 정량화
- 이론 모델과 실험 결과 비교를 통한 **성능 검증**


{% include image-gallery.html images="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/setup.png" height="400" %}

<p align="center">
  그림 1. MSCR 실험 장치 구성
</p>




## 결과 및 검증

- **최대 강성 변화율(SCF): X.XX**
- Fibre 수와 진공압에 따른 강성 변화 경향 확인
- 로봇 방향에 따른 구조적 비대칭 및 강성 차이 확인
- 실험 결과와 이론 모델을 비교하여 설계 성능 검증

<!-- 결과 그래프 1~2개 -->
