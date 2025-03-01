---
title: Overlay 란?
description: Overlay에 대해 알아보기
author: SemiDS
date: 2025-02-28 12:00:00 +0900
categories: [Semiconductor, Metrology & Inspection]
tags: [Overlay]
pin: true
---

## Overlay 란?
반도체에서 **Overlay (오버레이)**는 Photo 공정을 통해 형성되는 상하부 Layer 간의 정렬(Alignment) 정도를 정량적으로 계측하는 과정을 지칭합니다.  
반도체 칩은 Wafer 위에 여러 개의 Layer를 순차적으로 쌓아가며 제작되는데, 각 Layer들이 정확하게 정렬되지 않으면 불량 발생으로 인한 성능 저하 및 수율 감소로 이어질 수 있습니다. 따라서, Photo 공정 진행 시 Overlay를 계측하고 해당 값을 보정한 후 노광을 진행하는 과정이 필수적이라 할 수 있습니다.

Overlay 계측은 일반적으로 광학 기반 측정 방식이 사용되며, 가시광~적외선 영역의 광원을 사용하여 이미지를 측정해 정렬 정도를 계측하는 IBO (Image-Based Overlay) 방식, 반사된 빛의 회절(Diffraction) 패턴을 통해 계측하는 DBO (Diffraction-Based Overlay) 방식이 있습니다.  
IBO와 DBO 방식 모두 Overlay 계측을 위해 별도로 제작된 Key에서 측정되며, Layer의 형태나 박막의 물성 등에 따라 적절한 방식을 선택해서 사용하게 됩니다. 이렇게 계측된 Overlay 데이터는 회귀 분석(Regression Analysis)을 통해 X/Y 방향의 Shift, Rotation 등 다양한 성분으로 세분화되고, 이를 Photo 장비에 피드백하여 정렬 오차를 보정합니다.

<img src="/assets/img/posting/2025-02-28-github-blog-28-overlay_1.png" alt="overlay" width=400>  
<p style="text-align: center;"><a href="https://www.semanticscholar.org/paper/Multiobjective-optimization-for-target-design-in-Shi-Li/b5c15bec77382f663b58b87db77032afeb5a14e5">[출처: Multiobjective optimization for target design in diffraction-based overlay metrology]</a></p>

일반적으로 광학 기반 Overlay는 비교적 큰 크기를 가지는 Key에서 측정되는데, Overlay Key와 실제 소자 패턴의 크기 차이로 인해 오차가 발생할 수 있습니다. 이와 같은 오차를 보완하기 위해 실제 소자 패턴에서 Overlay 값을 측정하고 추가적으로 보정하는 과정이 필요한데, 이를 **OCO (On-Cell Overlay)**라고 부릅니다. OCO는 미세한 소자 패턴에서 정밀한 측정이 필요하기 때문에, 해상도가 높은 전자현미경을 통해 진행하게 됩니다.[[`SEM 이란?`]]({{ '/posts/github-blog-13/' | absolute_url }})

이와 같은 Overlay 계측은 반도체 제조 공정에서 필수적으로 수행되는 과정으로, 반도체의 성능과 수율에 직접적인 영향을 미치기 때문에 주기적인 모니터링과 이를 통한 반복적인 보정이 매우 중요하다고 할 수 있습니다.