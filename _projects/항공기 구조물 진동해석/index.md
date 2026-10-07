---
layout: post
title: 항공기 구조물의 진동 모달 해석 및 EMA/FEA 비교
description: 항공기 구조물을 대상으로 실험 모달 해석(EMA)과 Abaqus 기반 유한요소해석(FEA)을 수행하고, 고유진동수, 모드 형상, 주파수 응답 함수(FRF)를 비교하여 실험과 해석 결과의 차이 및 원인을 분석한 과제입니다.

skills:
  - Abaqus
  - 실험 모달 해석(EMA)
  - 유한요소해석(FEA)
  - 진동 및 모달 해석
  - 주파수 응답 함수(FRF) 분석
  - 고유진동수 및 모드 형상 분석
  - Shaker 기반 진동 실험
  - 실험/해석 결과 비교 및 검증

main-image: /coverpage.png
---

## 프로젝트 개요

- **프로젝트:** 항공기 구조물의 진동 모달 해석 및 실험·해석 비교
- **수행 기간:** 2025년 3월 ~ 2025년 4월
- **소속:** 영국 글래스고대학교 기계공학과
- **과제 유형:** 기계공학 4학년 진동(Vibration) 과제


## 문제 정의

- 항공기 구조물의 동적 특성을 정확히 평가하려면 **고유진동수, 모드 형상 및 공진 특성**을 파악해야 함.
- 실험 모달 해석(EMA)은 실제 구조물의 감쇠, 경계조건 및 제작 오차를 반영하지만, 측정 위치와 센서 조건에 영향을 받음.
- 유한요소해석(FEA)은 구조 거동을 예측할 수 있으나, 이상화된 재료, 형상, 경계조건 및 메쉬 설정으로 인해 실제 실험과 차이가 발생할 수 있음.
- 따라서 EMA와 FEA 결과를 직접 비교하여 **차이의 원인과 각 해석 방법의 한계**를 검토할 필요가 있음.

## 과제 목표

- Shaker, Force Transducer와 가속도계를 이용해 항공기 구조물의 **실험 모달 해석(EMA)** 수행
- Abaqus를 활용해 항공기 구조물의 **3D FEA 모델 구축**
- **자유진동 해석(Free Vibration)**을 통해 고유진동수와 모드 형상 추출 및 비교
- **강제진동 해석(Forced Vibration)**을 통해 주파수별 응답 및 FRF 분석 및 비교
- 날개상의 **10개 측정 지점**에서 FRF를 추출하고, 측정 위치에 따른 진동 응답 비교
- EMA의 **Modal Peaks Function(MPF)**을 이용해 주요 공진 주파수를 식별하고 FEA 결과와 비교
- EMA와 FEA의 **고유진동수, 모드 형상 및 FRF 차이**를 분석하고 모델링 한계 및 개선 방향 검토

<div style="display: flex; gap: 24px; justify-content: center; align-items: flex-start; flex-wrap: wrap; margin-top: 25px; margin-bottom: 35px;">

  <!-- EMA -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/항공기%20구조물%20진동해석/EMA.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="EMA Hardware Setup"
    >
    <figcaption style="margin-top: 8px;">
      그림 1. 실험 모달 해석(EMA) 실험 구성
    </figcaption>
  </figure>

  <!-- Abaqus -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/항공기%20구조물%20진동해석/abaqus.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="Abaqus 3D FEA Model"
    >
    <figcaption style="margin-top: 8px;">
      그림 2. Abaqus 기반 항공기 구조물 3D FEA 모델
    </figcaption>
  </figure>

</div>


## 결과 및 검토

- **EMA–FEA 공진 주파수 비교:** EMA에서 **8개 고유진동수**를 확인했으며, MPF 분석을 통해 **23, 75, 130, 390 Hz의 4개 주요 공진 주파수**를 식별함. FEA에서는 **6개 공진 주파수**를 확인했으며, 이 중 **23 Hz 및 125–130 Hz 구간**에서 EMA와 가장 높은 일치성을 확인함.
- **측정 위치에 따른 FRF 변화:** 날개상의 **10개 지점**에서 FRF를 비교한 결과 FEA에서는 **6개의 주요 공진 피크**가 공통적으로 나타났으며, 서로 가까운 두 측정점에서도 **200 Hz 이상에서 FRF가 크게 달라지는 현상**을 확인함. 이를 통해 고주파 영역에서 센서 위치와 국부 강성에 대한 민감도가 증가함을 확인함.
- **실험–해석 차이 및 한계 분석:** 저/중주파에서는 EMA와 FEA의 고유진동수 및 모드 형상이 비교적 유사했으나, **325.71 Hz(EMA)와 328.39 Hz(FEA)** 부근에서는 주파수는 유사해도 모드 형상 차이가 크게 나타남. 이는 EMA의 **날개 10개 측정점 제한**, FEA의 **감쇠 미적용, 홀/조인트/제작 오차 생략 및 0.02 m 고정 메쉬** 등 실험/모델링 조건 차이에 따른 것으로 분석함.



<div style="text-align: center; margin-top: 25px;">

  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/항공기%20구조물%20진동해석/1.png"
    style="max-width: 75%; height: auto; display: block; margin: 0 auto 30px auto;"
    alt="EMA와 FEA의 고유진동수 및 모드 형상 비교"
  >

  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/항공기%20구조물%20진동해석/2.png"
    style="max-width: 75%; height: auto; display: block; margin: 0 auto;"
    alt="EMA와 FEA의 고유진동수 및 모드 형상 비교"
  >

</div>

<div style="display: flex; gap: 24px; justify-content: center; align-items: flex-start; flex-wrap: wrap; margin-top: 25px;">

  <!-- FEA -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/항공기%20구조물%20진동해석/FRF10.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="FEA 10개 측정 지점의 FRF"
    >
    <figcaption style="margin-top: 8px;">
      FEA: 날개 10개 측정 지점의 주파수 응답 함수(FRF)
    </figcaption>
  </figure>

  <!-- EMA -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/항공기%20구조물%20진동해석/EMA10.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="EMA 10개 측정 지점의 FRF"
    >
    <figcaption style="margin-top: 8px;">
      EMA: 날개 10개 측정 지점의 주파수 응답 함수(FRF)
    </figcaption>
  </figure>

</div>

