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


<div style="max-width: 850px; margin: 20px auto;">
  <iframe
    width="100%"
    style="aspect-ratio: 16/9; border: none;"
    src="https://www.youtube.com/embed/7Td5GKU64RE"
    title="MSCR 프로젝트 실험 영상"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>



## 문제 정의

- **MSCR이란?** 자기장을 이용해 비접촉으로 구동되는 초소형 연성 로봇으로, 높은 유연성과 낮은 조직 손상 위험을 바탕으로 최소침습 의료 분야에 활용될 수 있음.

- **유연성과 강성의 상충관계:** 부드러운 구조는 인체 조직에 가해지는 부담을 줄이지만, 심혈관 및 폐 등에서 외력이 작용할 경우 형태와 위치를 유지하기 어려움. 따라서 필요에 따라 강성을 조절하는 기술이 요구됨.

- **기존 소재의 한계:** 기존 MSCR은 주로 실리콘 기반으로 제작됨. 본 연구에서는 두께 **38 μm의 열가소성 엘라스토머(TPE)** 필름을 활용하여 가변 강성 구조를 구현하고자 함.

- **미검증 설계 특성:** TPE 필름은 양압 구동 연성 로봇에 활용된 사례가 있으나, 섬유 재밍과 음압 적용 및 비대칭 구조에 따른 **방향별 강성 변화**에 대한 연구가 부족함.



## 연구 목표

- MSCR 내부에 **Fibre Jamming 기반 가변 강성 구조** 설계 및 통합
- TPE sleeve, 구리 섬유, NdFeB 자석을 활용하여 **직접 제조**
- 섬유 수, 진공압, 굽힘 방향 및 작업 채널 유무에 따른 강성 변화 분석 (**파라메트릭 실험 수행**)
- MATLAB을 활용한 변형 **데이터 분석** 및 Soft/Rigid 상태의 강성 변화 정량화
- 이론 모델과 실험 결과 비교를 통한 **성능 검증**


{% include image-gallery.html images="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/setup.png" height="400" %}

<p align="center">
  그림 1. MSCR 실험 장치 구성
</p>

<div style="display: flex; gap: 24px; align-items: flex-start; flex-wrap: wrap;">

  <figure style="flex: 1; margin: 0; min-width: 300px;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/setup%202.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="카메라 시점에서 본 MSCR"
    >
    <figcaption style="text-align: center; margin-top: 8px;">
      그림 2. 카메라 시점에서 본 헬름홀츠 코일 내 MSCR
    </figcaption>
  </figure>

  <figure style="flex: 1; margin: 0; min-width: 300px;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/rear%20tube%20assembly.png"
      style="width: 100%; height: 400px; object-fit: contain;"
      alt="후방 튜브 어셈블리"
    >
    <figcaption style="text-align: center; margin-top: 8px;">
      그림 3. 후방 튜브 어셈블리
    </figcaption>
  </figure>

</div>


## 결과 및 검증

- **최대 강성 변화율(SCF) 7.67 달성:** 작업 채널을 통합한 구조에서 최대 성능 기록. 작업 채널이 없는 비교 구조 대비 약 **33% 향상**
- **섬유 수 최적화:** 작업 채널이 없는 구조에서 600가닥의 섬유를 적용했을 때 가장 높은 강성 변화율 기록.
- **진공압 최적화:** 진공압 증가에 따라 SCF가 향상되었으나, -40~-80 kPa 구간에서 성능 증가 폭이 둔화됨. 높은 진공압에 따른 추가적인 성능 향상은 제한적임.
- **방향별 특성:** 작업 채널이 없는 비교 구조에서는 굽힘 방향에 따른 성능 차이가 제한적이었음.
- **TPE 기반 제작:** 두께 38 μm의 TPE 필름과 섬유 재밍을 결합하여 가변 강성 구현 및 구조 맞춤화 가능성 확인.

<!-- 섬유 수 비교 그래프: 단독 가운데 정렬 -->
<figure style="margin: 25px auto; text-align: center;">
  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/섬유수비교.png"
    style="max-width: 100%; max-height: 400px; width: auto; height: auto;"
    alt="섬유 수 비교"
  >
  <figcaption style="margin-top: 8px;">
    그림 4. 작업 채널이 없는 600가닥 MSCR의 자기장 증가·감소 사이클에 따른 형상 변화: 대기압(상) 및 -40 kPa 진공 상태(하)
  </figcaption>
</figure>


<!-- SCF + 진공압 변화: 한 줄에 2개 -->
<div style="display: flex; gap: 24px; justify-content: center; align-items: flex-start; flex-wrap: wrap; margin-top: 25px;">

  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/SCF.jpg"
      style="width: 100%; height: 300px; object-fit: contain;"
      alt="강성 변화율 비교"
    >
    <figcaption style="margin-top: 8px;">
      그림 5. 섬유 수에 따른 굽힘 방향별 강성 변화율(SCF)
    </figcaption>
  </figure>

  <figure style="flex: 1 1 0; max-width: 48%; min-width: 300px; margin: 0; text-align: center;">
    <img
      src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/최소침습%20로봇/진공압변화.png"
      style="width: 100%; height: 300px; object-fit: contain;"
      alt="진공압 변화"
    >
    <figcaption style="margin-top: 8px;">
      그림 6. 진공압에 따른 굽힘 방향별 정규화 처짐
    </figcaption>
  </figure>

</div>


## 연구 한계 및 향후 개선

- **제작 공정:** 구조적 비대칭에 따른 방향 의존성을 개선하고, 제작 시간 단축 및 공정 재현성 확보 필요
- **소형화:** 실제 최소침습 의료 환경에 적합한 로봇 직경 축소 필요
- **안전성:** 인체 내 적용을 위한 적정 진공압 및 작동 안전성 검증 필요
- **제어 성능:** 정밀 조향 및 복잡한 인체 환경에서의 이동·제어 기술 고도화 필요

<div style="max-width: 850px; margin: 20px auto;">
  <iframe
    width="100%"
    style="aspect-ratio: 16/9; border: none;"
    src="https://www.youtube.com/embed/atpv-xisPTs"
    title="MSCR 프로젝트 실험 영상"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
