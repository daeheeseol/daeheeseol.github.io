---
title: Standard Cell 이란?
description: Standard Cell에 대해 알아보기
author: SemiDS
date: 2025-02-26 12:00:00 +0900
categories: [Semiconductor, Design]
tags: [Standard Cell]
pin: true
---

## Standard Cell 이란?
반도체에서 **Standard Cell**은 AND, OR, NOT 같은 논리 게이트나 플립플롭(Flip-Flop)과 같은 디지털 회로 요소들을 Layout 형태로 미리 설계해둔 표준화된 Component로 ASIC(Application-Specific Integrated Circuit)과 같은 주문형 반도체의 설계를 위해 활용됩니다.  

<img src="/assets/img/posting/2025-02-26-github-blog-27-stdcell_1.png" alt="stdcell" width=400>  
<p style="text-align: center;"><a href="https://www.vlsispace.com/2024/06/standard-cells-in-dgital-designvlsi.html">[출처: VLSI SPACE]</a></p>

Standard Cell은 Semi-Custom 설계 방식으로, 성능과 전력 소비를 최적화하면서 Full-Custom 대비 빠르고 효율적인 설계를 가능케 하는 핵심 기술이라고 할 수 있습니다. 이러한 Standard Cell은 공정에 맞춰 최적화된 라이브러리(Library) 형태로 제작되며, Gate-level Netlist 생성을 위한 논리 합성(Logic Synthesis)부터 Physical Design을 위한 PnR(Place & Route)까지 다양한 단계에서 사용됩니다.[[`Physical Design 이란?`]]({{ '/posts/github-blog-18/' | absolute_url }})

>**Standard Cell의 장점 (By ChatGPT)**
>- **설계 시간 단축**: Full-Custom 설계 대비 빠르게 설계 가능
>- **면적 및 성능 최적화**: 반도체 공정에 맞춰 최적화된 라이브러리 형태로 제작
>- **설계 자동화 가능**: EDA(Electronic Design Automation) Tool을 이용하여 자동화된 설계 가능
>- **재사용 가능성**: 미리 설계된 라이브러리를 반복적으로 사용 가능

일반적으로 Auto PnR 등의 자동화된 설계를 위해 Standard Cell은 높이(Height)는 일정하게 유지하고 폭(width)은 복잡도에 따라 가변적인 형태로 만들어집니다.  
그러나, 라이브러리에는 동일한 기능을 수행하는 Cell이라도 높이가 다른 여러 버전이 포함되어 있습니다. 이는 Cell의 높이에 따라 전력 소비, 성능, 면적 등의 특성이 달라지기 때문으로, 높이가 낮은 Cell은 저전력이 필요한 모바일이나 IoT 기기 칩, 높이가 높은 Cell은 고성능이 요구되는 서버, 고성능 프로세서 칩 등의 설계에 활용됩니다.  
즉, 설계자가 원하는 목표에 따라 적절한 Cell을 선택해서 사용할 수 있게 라이브러리를 구성해서 제공합니다.

Standard Cell은 반도체 설계의 핵심 요소로, 논리 합성부터 PnR, 검증까지 다양한 단계에서 사용됩니다. 자동화된 설계 흐름을 지원하고 동시에 성능과 전력 효율을 최적화할 수 있으며, 이를 통해 설계 효율성과 생산성을 높이는 데 중요한 역할을 하고 있습니다.