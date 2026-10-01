---
layout: post
title: 베어링 브래킷의 구조응력 해석
description: Abaqus를 활용해 베어링 브래킷의 유한요소해석(FEA) 모델을 구축하고, 하중 및 경계조건에 따른 응력과 변형을 분석하여 구조적 안전성을 평가한 과제입니다.
skills: 
  - Abaqus
  - 유한요소해석(FEA)
  - 구조 응력 해석
  - 3D 모델링
  - 재료 물성 설정
  - 경계조건 및 하중 설정
  - 메싱
  - 응력 및 변형 분석
  - 구조 설계 검토
main-image: /coverpage.png
---


## 프로젝트 개요

- **프로젝트:** 베어링 브래킷 구조응력 해석
- **수행 기간:** 2023년 10월 ~ 2023년 11월
- **소속:** 영국 글래스고대학교 기계공학과
- **과제 유형:** 기계공학 4학년 유한요소해석(FEA) 과제
- **주요 수행 내용:** Abaqus 모델 구축, 재료 및 경계조건 설정, 메싱, 응력 및 변형 분석, 구조 안전성 평가


## 문제 정의

- 베어링 브래킷에 외력이 작용할 때 발생하는 **응력 집중과 변형**을 정량적으로 분석할 필요가 있음.
- 실제 구조물의 형상, 재료 특성 및 하중 조건을 반영한 **유한요소해석 모델 구축**이 필요함.
- 해석 결과를 바탕으로 구조적으로 취약한 영역과 설계 안전성을 평가해야 함.


## 과제 목표

- Abaqus를 활용해 베어링 브래킷의 **2D/3D 유한요소 모델 구축**
- 실제 사용 조건을 고려한 **재료, 하중 및 경계조건 설정**
- 요소 크기에 따른 결과 변화를 비교하여 **메시 수렴성 검토 및 계산 효율간 Trade-off 평가**
- 응력 및 변형 분포를 분석하여 **최대 등가응력 위치와 구조적 취약 부위 평가**
- 해석 결과를 바탕으로 구조 안전성을 유지하는 **경량화 설계안 제안**


<div style="display: flex; gap: 24px; justify-content: center; align-items: flex-start; flex-wrap: wrap; margin-top: 25px;">

  <!-- 구조 개념도 -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/schematic.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="베어링 브래킷 구조 개념도"
    >
    <figcaption style="margin-top: 8px;">
      그림 1. 베어링 브래킷 구조 및 하중 조건
    </figcaption>
  </figure>

  <!-- 계산 효율 -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/계산효율.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="요소 수에 따른 계산 시간"
    >
    <figcaption style="margin-top: 8px;">
      그림 2. 요소 수 증가에 따른 계산 시간 변화
    </figcaption>
  </figure>

</div>

<br>
## 결과 및 검토

- **메시 수렴성 검증:** 요소 수 증가에 따른 최대 등가응력 변화를 비교한 결과, 최종 메시 단계에서 주요 지점의 응력 변화가 **1% 이내**로 수렴함을 확인
- **응력 집중 위치 파악:** 최대 응력은 **볼트 홀 외곽 및 형상이 급격히 변화하는 곡률/필렛 부위**에 집중되는 것을 확인하여 구조적 취약 영역을 식별
- **2D/3D 모델 비교:** 3D 해석에서는 두께 방향(Z축) 효과가 반영되면서 A, B, C 지점의 응력값이 달라졌으며, 2D 모델보다 실제 구조의 응력 거동을 더 현실적으로 반영함
- **경량화 설계:** 최대 등가응력 수준을 유지하면서 **약 33% 질량 감소** 달성

<div style="display: flex; gap: 24px; justify-content: center; align-items: flex-start; flex-wrap: wrap; margin-top: 25px;">

  
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/2D메시수렴.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="2D메시수렴성"
    >
    <figcaption style="margin-top: 8px;">
      그림 3. 2D 모델의 요소 수에 따른 A, B, C 지점 최대 등가응력 수렴성
    </figcaption>
  </figure>

 
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/3D메시수렴.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="3D메시수렴성"
    >
    <figcaption style="margin-top: 8px;">
      그림 4. 3D 모델의 요소 수에 따른 A, B, C 지점 최대 등가응력 수렴성
    </figcaption>
  </figure>

</div>

<div style="display: flex; gap: 24px; justify-content: center; align-items: flex-start; flex-wrap: wrap; margin-top: 25px;">

  <!-- 홀 미적용 브래킷 -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/VMSwithoutHole.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="홀 미적용 브래킷의 등가응력 분포"
    >
    <figcaption style="margin-top: 8px;">
      그림 5. 홀 미적용 브래킷의 등가응력 분포 및 응력 집중 분석
    </figcaption>
  </figure>

  <!-- 홀 적용 브래킷 -->
  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/VMSHole.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="홀 적용 브래킷의 등가응력 분포"
    >
    <figcaption style="margin-top: 8px;">
      그림 6. 홀 적용 브래킷의 등가응력 분포 및 응력 집중 분석
    </figcaption>
  </figure>

</div>

<br>

## 경량화 설계안

<!-- 경량화 설계안 1 -->
<figure style="margin: 25px auto; text-align: center;">
  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/concept1.png"
    style="max-width: 100%; max-height: 330px; width: auto; height: auto; display: block; margin: 0 auto;"
    alt="경량화 설계안 1: 절삭 형상 적용"
  >
  <figcaption style="margin-top: 8px; text-align: center;">
    경량화 설계안 1. 절삭 형상 적용
  </figcaption>
</figure>


<!-- 경량화 설계안 2 -->
<figure style="margin: 25px auto; text-align: center;">
  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/concept2.png"
    style="max-width: 100%; max-height: 350px; width: auto; height: auto; display: block; margin: 0 auto;"
    alt="경량화 설계안 2: 외측 반경 축소"
  >
  <figcaption style="margin-top: 8px; text-align: center;">
    경량화 설계안 2. 외측 반경 축소
  </figcaption>
</figure>


<!-- 경량화 설계안 3 -->
<figure style="margin: 25px auto; text-align: center;">
  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/concept3.png"
    style="max-width: 100%; max-height: 350px; width: auto; height: auto; display: block; margin: 0 auto;"
    alt="경량화 설계안 3: 재료 변경"
  >
  <figcaption style="margin-top: 8px; text-align: center;">
    경량화 설계안 3. 재료 변경
  </figcaption>
</figure>


<!-- 경량화 설계안 4 -->
<figure style="margin: 25px auto; text-align: center;">
  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/베어링%20브래킷의%20구조응력%20해석/concept4.png"
    style="max-width: 100%; max-height: 350px; width: auto; height: auto; display: block; margin: 0 auto;"
    alt="경량화 설계안 4: 3개 설계안 통합 적용"
  >
  <figcaption style="margin-top: 8px; text-align: center;">
    경량화 설계안 4. 3개 설계안 통합 적용
  </figcaption>
</figure>


