---
title: RET (Resolution Enhancement Technique) 란?
description: RET에 대해 알아보기
author: SemiDS
date: 2025-02-20 12:00:00 +0900
categories: [Semiconductor, Process]
tags: [RET]
pin: true
---

## RET (Resolution Enhancement Technique) 란?
**RET (Resolution Enhancement Technique)**는 반도체 공정에서 노광(Photolithography) 설비의 광학적 한계를 극복하기 위해 도입된 기술로, Wafer에 전사되는 패턴을 보다 정밀하게 구현하기 위해 사용하는 방법입니다.

Photo 공정의 해상도(Resolution)는 사용되는 광원의 파장과 밀접한 관련이 있고 EUV(Extreme Ultraviolet)와 같은 단파장 광원을 활용하여 해상도를 개선하고 있지만, 설비 개발의 복잡성과 높은 공정 비용 등의 문제로 실제 공정에서는 파장을 줄이는 것만으로는 선폭을 감소시키는데 한계가 있습니다.

즉, RET는 위와 같은 한계점을 극복하기 위해 노광 설비(파장)를 변경하지 않고 다른 광학적 방법을 이용해 패턴의 해상도를 개선하는 방법이라고 할 수 있습니다.

RET에는 여러 가지 기법이 있으며, 대표적인 예시는 아래와 같습니다.
>1. OAI (Off-Axis Illumination)
>- 빛을 Photomask에 비스듬하게 입사시켜 0차 및 1차 회절광을 모두 활용헤 해상도를 높이는 기술
>2. PSM (Phase Shift Mask)
>- Photomask내 특정 부분의 Phase(위상)을 180도 이동시켜 간섭 효과를 유도하여 해상도를 높이는 기술
>3. SMO (Source Mask Optimization)
>- 노광 장비의 광원(Source)과 Photomask 디자인을 최적화하여 해상도를 높이는 기술
>4. OPC (Optical Proximity Correction)
>- 광학적 회절(diffraction)과 근접 효과(proximity effect)로 인해 패턴이 제대로 형성되지 않는 문제를 보정해서 해상도를 높이는 기술
>5. SRAF (Sub-Resolution Assist Feature)
>- 주요 패턴 주변에 작은 보조 패턴(실제로 패터닝이 되지 않는)을 추가해서 해상도를 높이는 기술

<img src="/assets/img/posting/2025-02-20-github-blog-23-ret_1.png" alt="VM" width=500>  
<p style="text-align: center;"><a href="https://spie.org/publications/spie-publication-resources/optipedia-free-optics-information/fg06_p77_resolution_enhancement/">[출처: Resolution Enhancement Technologies]</a></p>

이와 같은 RET는 반도체 미세 공정을 구현하는데 있어 핵심적인 기술 중 하나로, 노드가 점점 더 미세화됨에 따라 그 중요성 역시 더욱 커지고 있습니다.
