---
title: Photomask 란?
description: Photomask에 대해 알아보기
author: SemiDS
date: 2025-03-15 12:00:00 +0900
categories: [Semiconductor, Process]
tags: [Photomask]
pin: true
---

## Photomask 란?
반도체에서 **Photomask (이하 Mask)**는 Photolithography 공정에서 사용되는 회로 패턴이 새겨진 투명한 판으로, 빛을 차단하거나 통과시키는 역할(차광막)을 하여 웨이퍼에 패턴을 전사하는 데 사용되며, **Reticle**이라고도 불립니다.

반도체 칩 설계가 완료되면 해당 설계도는 Physical Design 단계를 거쳐 Layout(물리적인 회로 설계도)으로 변환되고, 이후 MDP(Mask Data Preparation) 과정을 통해 Photomask 제작을 위한 데이터 파일(Manufacturing Electron Beam Exposure System, MEBES))로 변환됩니다.[[`MDP 란?`]]({{ '/posts/github-blog-15/' | absolute_url }})  
Mask Shop에서는 해당 파일을 전달받아 E-beam Lithography를 통해 회로 패턴을 형성하고, 새겨진 패턴에 대한 CD(Critical Dimension) 계측 및 결함 검사(Inspection) 과정을 거쳐 Mask를 제작하게 됩니다.

ArF, KrF와 같은 투과형 광원에 대한 Mask는 투명한 Quartz(석영) 기판 위에 불투명한 Cr(크롬) 층을 패터닝해서 특정 부분만 빛이 선택적으로 통과할 수 있도록 제작됩니다. 반면, EUV(Extreme Ultra-Violet)의 경우 대부분의 물질에 흡수되는 성질로 인해 기존의 투과형 Mask를 사용할 수 없어, 다층 박막 구조를 이용한 반사형(거울)으로 제작하게 됩니다.

추가로, Mask는 목적에 따라 Binary Mask와 Phase Shift Mask(PSM)로 구분됩니다. Binary Mask는 빛이 통과하는 부분과 차단되는 부분만 명확히 구별된 가장 일반적인 형태의 Mask이고, PSM은 phase-shifter 물질을 추가로 사용하여 빛의 위상을 변화시키는 방식으로, 해상도를 향상시켜 더 작은 패턴을 구현할 수 있도록 설계된 Mask입니다.

<img src="/assets/img/posting/2025-03-15-github-blog-33-photomask_1.png" alt="photomask" width=450>  
<p style="text-align: center;"><a href="https://en.wikipedia.org/wiki/Photomask">[출처: Wikipedia]</a></p>

Mask에 새겨진 회로 패턴에 결함이 있을 경우 웨이퍼에 그대로 전사되어 불량을 유발할 수 있습니다. 이를 방지하기 위해 Mask에 대한 계측과 검사를 통해 결함을 확인하고 제거하는 것도 중요하지만, Mask는 공정에서 반복적으로 사용되기 때문에 먼지와 같은 오염으로부터 Mask를 보호하는 장치도 필요합니다. 이를 위해 **Pellicle(펠리클)**이라는 Mask 보호막이 사용됩니다. 그러나 EUV 공정에서는 기존의 투과형 Pellicle이 EUV 광원을 흡수하는 문제가 있어, EUV에 적합한 Pellicle이 필요하며 현재 활발히 개발되고 있습니다.

<img src="/assets/img/posting/2025-03-15-github-blog-33-photomask_2.png" alt="photomask" width=600>  
<p style="text-align: center;"><a href="https://www.etnews.com/20230110000158">[출처: etnews]</a></p>

Photomask는 반도체 공정에서 웨이퍼 위에 미세한 회로 패턴을 구현하는 필수적인 요소로, 반도체 제조 과정의 출발점이라 할 수 있습니다. 공정이 미세화될수록 마스크의 정밀도와 품질이 반도체 성능과 생산 수율을 결정짓는 중요한 요인이 되며, 이에 따라 제조 비용과 생산성에 미치는 영향성 또한 점차 커지고 있습니다.