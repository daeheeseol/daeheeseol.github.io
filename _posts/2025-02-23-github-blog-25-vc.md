---
title: VC (Voltage Contrast) 란?
description: VC에 대해 알아보기
author: SemiDS
date: 2025-02-23 12:00:00 +0900
categories: [Semiconductor, Metrology & Inspection]
tags: [VC]
pin: true
---

## VC (Voltage Contrast) 란?
전자현미경에서 **VC (Voltage Contrast)**란 시료에 전자빔을 조사할 때 방출되는 2차 전자(Secondary Electron, SE)의 양에 따라 이미지에서 특정 영역이 밝거나 어둡게 보이는 현상을 의미합니다. 시료의 특정 부분에서 전자가 많이 방출되면 밝게, 전자가 적게 방출되면 어둡게 나타나게 되고, 이를 BVC(Bright Voltage Contrast)와 DVC(Dark Voltage Contrast)로 지칭합니다.  

반도체 공정에서는 패턴의 전기적인 결함을 분석하기 위해 VC를 활용합니다. 방출되는 전자의 양에 따라 이미지에 명암 차이가 발생하는 것을 이용해 비정상적인 패턴 상태를 검출하는 방식입니다. 예를 들어, 특정 패턴이 정상적으로 Open 되지 않은 경우에는 방출되는 전자의 양이 줄어 DVC로 보이고, 반대로 패턴간 Short이 생긴 경우에는 전자가 많이 방출되어 BVC로 보이게 됩니다.

일반적으로 ebeam 설비를 통해 VC 검사를 진행하게 되는데[[`ebeam 이란?`]]({{ '/posts/github-blog-13/' | absolute_url }}), In-line에서 비파괴 방식으로 패턴간 전기적 연결 상태를 확인할 수 있는 매우 중요한 검사 기법 중 하나입니다. 추가로, VC 검사는 In-line 공정에서뿐만 아니라 Failure Analysis(FA)에서도 불량 위치를 탐지하기 위한 목적으로도 많이 활용됩니다.

<img src="/assets/img/posting/2025-02-23-github-blog-25-vc_1.png" alt="VC" width=500>  
<p style="text-align: center;"><a href="https://ieeexplore.ieee.org/document/4263674">[출처: Mechanism and Application of Negative Charging Mode of Electron Beam Inspection for PMOS Leakage Detection]</a></p>

이와 같은 VC는 검사하고자 하는 패턴이 NMOS인지 PMOS인지, 외부에서 인가하는 전기장이 양전압(Positive)인지 음전압(Negative)인지에 따라 명암 차이가 달라지기 때문에, 경우에 따라서는 불량이 발생했더라도 명암 차이로 구별할 수 없는 경우도 있습니다. 또한, 절연막이 너무 두꺼워서 전자가 제대로 방출되지 않거나, 표면에 전하가 축적(Charging)되어 신호가 왜곡되는 등의 한계점도 존재합니다.  
그럼에도 불구하고, 반도체 공정이 점점 미세화됨에 VC 검사를 통한 전기적 불량 분석의 중요성은 더욱 커지고 있으며, 이를 활용한 ebeam 설비 또한 반도체 검사 및 분석에서 핵심적인 역할을 수행하고 있습니다.
