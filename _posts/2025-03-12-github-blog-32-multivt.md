---
title: Multi Vt (Multi-Threshold Voltage) 란?
description: Multi Vt에 대해 알아보기
author: SemiDS
date: 2025-03-12 12:00:00 +0900
categories: [Semiconductor, Design]
tags: [Multi Vt]
pin: true
---

## Multi Vt (Multi-Threshold Voltage) 란?
반도체(디지털) 회로의 기본 소자 중 하나인 MOSFET(Metal-Oxide-Semiconductor Field-Effect Transistor)의 게이트(Gate)에 일정한 전압을 가하면 채널(Channel)이 형성되어 전류가 흐르기 시작합니다. 이때, 전류가 흐르기 시작하는 최소한의 게이트 전압을 **Threshold Voltage (Vt)**라고 합니다. 

즉, Vt는 MOSFET이 스위칭(ON 상태)되기 위해 필요한 최소한의 전압을 의미하며, **Multi Vt (Multi-Threshold Voltage)**는 하나의 반도체 칩을 설계할 때 서로 다른 Vt를 갖는 트랜지스터를 사용하여 성능과 전력 소모를 최적화하는 방법입니다.

이와 같은 Multi Vt가 필요한 이유는 반도체 소자는 성능과 전력 소비 간의 아래와 같은 상충 관계가 존재하기 때문입니다.

> **Low-Vt (LVT)**  
>\- 장점: 전류가 빠르게 흐를 수 있어 속도가 비교적 빠름  
>\- 단점: 누설 전류(Leakage Current)가 크기 때문에 대기 전력 소비가 큼  

> **High-Vt (HVT)**  
>\- 장점: 누설 전류가 작아 대기 전력 소비가 적음  
>\- 단점: 속도가 비교적 느림

<img src="/assets/img/posting/2025-03-12-github-blog-32-multivt_1.png" alt="mpt" width=600>  
<p style="text-align: center;"><a href="https://semiwiki.com/finfet/287465-multi-vt-device-offerings-for-advanced-process-nodes/">[출처: Semiwiki]</a></p>

즉, 칩을 설계할 때 CPU나 GPU처럼 연산 속도가 중요한 경우에는 LVT 트랜지스터를 사용하고, 저전력이 필요한 경우에는 HVT 트랜지스터를 활용하여 성능과 전력 소비의 균형을 맞추게 됩니다.

공정적으로 Multi Vt를 구현하기 위해서는 채널의 도핑(Doping) 농도를 조절하거나, Metal과 Oxide 계면에서 산소 확산(Oxygen Diffusion)을 통해 Dipole을 형성하는 방식 등이 사용되며, 파운드리(Foundry) 업체는 다양한 Vt 옵션을 팹리스(Fabless)에 제공하는 것이 공정 경쟁력을 결정하는 중요한 요소 중 하나라고 할 수 있습니다. 이를 통해 팹리스 업체는 설계 목표에 맞춰 성능과 전력 효율을 최적화할 수 있으며, 고성능 컴퓨팅부터 저전력 IoT 기기까지 다양한 반도체 제품을 개발할 수 있습니다.