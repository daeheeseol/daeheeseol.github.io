---
title: LLE (Local Layout Effect) 란?
description: LLE에 대해 알아보기
author: SemiDS
date: 2025-03-06 12:00:00 +0900
categories: [Semiconductor, Design]
tags: [LLE]
pin: true
---

## LLE (Local Layout Effect) 란?
반도체에서 **LLE (Local Layout Effect)** 또는 **LDE (Layout Dependent Effect)**는 Layout 구조가 소자(트랜지스터)의 전기적 특성에 영향을 주는 현상을 지칭합니다.  
반도체 칩 설계 과정에서 Layout이란, 논리적으로 구현된 회로 설계도를 실제 Photomask로 제작하기 위해 물리적인 도형(Polygon)의 형태로 변환하는 것을 지칭합니다.[[`Physical Design 이란?`]]({{ '/posts/github-blog-18/' | absolute_url }}) 

논리 회로 설계(Gate-level Netlist)를 물리적인 도면(Layout)으로 변환하고 공정을 통해 칩을 제조하게 되면, 소자 자체의 구조(Standard Cell)나 소자 간 배치(Place & Routing)에 따라 문턱 전압(Threshold Voltage), 전자/정공 이동도(Electron/Hole Mobility) 등의 전기적 특성이 특정한 방향(증가 또는 감소)으로 변하게 됩니다.

대표적인 LLE 현상으로는 WPE(Well Proximity Effect), STI(Shallow Trench Isolation) Stress 등이 있으며, 이는 설계 단계에서 의도한 소자의 특성과 실제 Wafer에 구현된 소자의 특성 간 차이를 만드는 원인이 됩니다.

이를 줄이기 위해, 설계 단계에서 LLE의 영향을 고려하여 소자의 특성을 시뮬레이션하는 것이 필요하며, 이를 위해 `SPICE(Simulation Program with Integrated Circuit Emphasis)` 모델 파라미터에 LLE의 영향성을 반영하고 이를 토대로 시뮬레이션을 진행하게 됩니다. 즉, 설계 단계에서 시뮬레이션된 소자의 성능과 실제 제조된 칩의 성능 차이를 최소화하기 위해 SPICE 모델 파라미터에 LLE의 영향성을 정확하게 반영하는 것이 필수적이라고 할 수 있습니다.

특히, 반도체 공정이 미세화될수록 트랜지스터의 크기가 작아지고 소자의 밀도가 증가함에 따라 Layout이 미치는 영향이 더욱 커지기 때문에, 다양한 LLE 인자를 정확히 분석하고 이를 설계와 시뮬레이션 과정에 반영하는 것이 점점 더 중요해지고 있습니다.