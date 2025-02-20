---
title: OCD (Opitcal Critical Dimension) 란?
description: OCD에 대해 알아보기
author: SemiDS
date: 2025-02-18 12:00:00 +0900
categories: [Semiconductor, Metrology & Inspection]
tags: [OCD]
pin: true
---

## OCD (Opitcal Critical Dimension) 란?
**OCD (Opitcal Critical Dimension)**는 주기적인(반복적인) 패턴을 가지고 있는 시료에 자외선/가시광선/적외선 대역폭의 빛을 입사한 후 회절되어 나오는 빛의 광학적 신호를 이용하여 시료의 3차원 구조 정보를 고해상도(나노미터 단위)로 계측하는 설비입니다.  
빛을 입사시키는 각도에 따라 SE(Spectroscopic Ellipsometry) 및 SR(Spectroscopic Reflectometry) 방식이 있으며 각 방법별 특징은 아래와 같습니다.

>- SE(Spectroscopic Ellipsometry): 광원에서 나온 빛을 입사시킨 후, 회절된 빛의 편광 상태 변화(편광 정도, 위상차이 등)를 통해 물질의 광학적 특성을 측정하는 방식, 복잡한 구조 측정에 적합
>- SR(Spectroscopic Reflectometry): 광원에서 나온 빛을 입사시킨 후, 반사된 빛의 강도(파장에 따른 신호 세기)를 통해 물질의 광학적 특성을 측정하는 방식, 단순한 두께 측정에 적합

SE/SR 방식 모두 시료에서 회절되어 나오는 빛을 파장에 따른 스펙트럼 형태로 측정하고, 해당 스펙트럼으로부터 시료의 구조 정보를 추출하기 위해 일반적으로 **RCWA (Rigorous Coupled-Wave Analysis)** 기반 구조 모델링을 이용합니다. RCWA는 주기적인 구조에서 빛의 회절 현상을 해석하기 위한 수치 해석 기법 중 하나로 광학정 모델링을 수행하기 위해 많이 활용됩니다.  

OCD에서 모델링 및 구조 정보 추출은 일반적으로 아래와 같은 순서로 진행됩니다.  
>1. RCWA를 통해 구조에 따라 달라지는 빛의 회절을 이론적으로 계산해서 구조-스펙트럼 라이브러리 구축
>2. 반복적인 구조를 가지는 시료에서 실제 회절 스펙트럼 측정
>3. 측정된 스펙트럼과 라이브러리 내 스펙트럼을 Fitting해서 실제와 가장 유사한 이론 스펙트럼 탐색
>4. 이론 스펙트럼이 계산된 모델 구조에 대한 정보를 역으로 추적해서 실제 시료의 구조 정보를 추출

<img src="/assets/img/posting/2025-02-18-github-blog-21_1.png" alt="OCD" width=550>  
<p style="text-align: center;"><a href="https://scienceon.kisti.re.kr/srch/selectPORSrchReport.do?cn=TRKO201600005516#;">[출처: [국가R&D연구보고서] 2D OCD(Optical Critical Dimension) system 개발]</a></p>

위와 같은 원리로 OCD는 시료의 3D 구조를 비파괴 방식으로 매우 빠르고 정밀하게 측정할 수 있기 때문에, 반도체 제조 공정에서 패턴의 CD(Critical Dimension), Thickness, SWA(Side-Wall Angle) 등 다양한 3D 구조를 계측하기 위해 필수적으로 사용됩니다.  
그러나, 수십 µm 이상의 주기적인 구조를 가지는 영역에서만 측정이 가능해 국부적인 정보는 측정하기 어렵다는 한계점이 존재하며, 이를 극복하기 위해 Beam 크기를 줄이거나 새로운 광학 모델을 적용하는 등 다양한 기술이 지속적으로 개발되고 있습니다.