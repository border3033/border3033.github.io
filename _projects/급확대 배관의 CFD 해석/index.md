---
layout: post
title: 급확대 배관의 CFD 해석 및 Mesh 최적화
description: STAR-CCM+ 기반 2D 축대칭 급확대 배관 CFD 해석을 수행하고, Mesh Refinement에 따른 유동 변화를 분석했습니다. 재순환/재부착/속도 분포 및 재발달 특성을 확인하고, PIV 실험 데이터와 비교했습니다.

skills:
  - STAR-CCM+
  - 전산유체역학(CFD)
  - 2D 축대칭 해석
  - Mesh Refinement 및 최적화
  - 수렴성 및 Mesh 민감도 분석
  - 유동 분리 및 재부착 분석

main-image: /coverpage.png
---

## 프로젝트 개요

- **프로젝트:** 급확대 배관의 CFD 해석 및 Mesh 최적
- **수행 기간:** 2025년 3월 ~ 2025년 4월
- **소속:** 영국 글래스고대학교 기계공학과
- **과제 유형:** Computational Fluid Dynamics 4 개인 과제

## 과제 목표

- STAR-CCM+를 활용한 **2D 축대칭 급확대 배관 CFD 모델 구축**
- M1~M4까지 단계적으로 Mesh를 개선하고 **Mesh Refinement에 따른 해석 수렴성 검증**
- 속도 분포와 Streamline을 통해 **유동 분리, 재순환 및 재부착 현상 분석**
- Hammad et al.의 **PIV 실험 데이터와 CFD 해석 결과를 비교하여 해석 정확도 평가** ([논문 보기 ↗](https://doi.org/10.1007/s003480050288))

## 결과 및 검토

- **해석 모델 구축:** 2D 축대칭 급확대 배관 모델에 Velocity Inlet, Pressure Outlet, Wall 및 Axis 경계조건 적용
- **Mesh 개선 및 수렴성 검토:** M1~M4까지 단계적으로 Mesh를 개선하여 급확대부/재부착 영역은 세분화하고 비관심 영역은 Coarse하게 구성했으며, Residual 및 압력 Monitor를 통해 수렴성 확인
- **유동 특성 분석:** 속도 분포와 Streamline을 통해 유동 분리, 역류, 재순환 및 재부착 현상 확인
- **PIV 실험 결과 비교:** 재부착 길이 **0.061 m**로 실험값 대비 약 **0.15% 차이**, 재발달 길이는 약 **10.7% 차이** 확인
- **추가 개선 방향:** Wake 영역 중심의 Mesh Refinement와 3D 모델 비교 필요성 검토

<br>
<div style="text-align: center; margin-top: 25px;">

  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/급확대%20배관의%20CFD%20해석/computational-domain.png"
    style="max-width: 85%; height: auto; display: block; margin: 0 auto 8px auto;"
    alt="급확대 배관의 2D 축대칭 해석 영역"
  >
  <p style="margin-bottom: 30px;"><b>그림 1. 급확대 배관의 2D 축대칭 해석 영역</b></p>

  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/급확대%20배관의%20CFD%20해석/boundary-condition.png"
    style="max-width: 75%; height: auto; display: block; margin: 0 auto 8px auto;"
    alt="STAR-CCM+ 경계조건"
  >
  <p style="margin-bottom: 30px;"><b>그림 2. STAR-CCM+ 해석 모델의 경계조건 설정</b></p>

  <img
    src="https://raw.githubusercontent.com/border3033/border3033.github.io/main/_projects/급확대%20배관의%20CFD%20해석/mesh.png"
    style="max-width: 90%; height: auto; display: block; margin: 0 auto 8px auto;"
    alt="최종 계산 격자 및 국부 Mesh Refinement"
  >
  <p><b>그림 3. 최종 계산 격자(M4) 및 국부 Mesh Refinement</b></p>

</div>
