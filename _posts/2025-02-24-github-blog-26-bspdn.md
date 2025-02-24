---
title: BSPDN (Back Side Power Delivery Network) 이란?
description: BSPDN에 대해 알아보기
author: SemiDS
date: 2025-02-24 12:00:00 +0900
categories: [Semiconductor, Design]
tags: [BSPDN]
pin: true
---

## BSPDN (Back Side Power Delivery Network) 이란?
반도체 칩을 동작시키기 위해서는 트랜지스터에 전력을 공급하기 위한 `전력선(Power Rail)`과 연산 결과를 전송하기 위한 `신호선(Signal Line)`이 필요합니다.  
이와 같은 전력선과 신호선은 다층의 금속 배선(Routing)을 통해 구현되는데, 두개의 선을 모두 Wafer의 전면(Front Side)에 배치하는 방식을 **FSPDN (Front Side Power Delivery Network)**, 전력선을 Wafer의 후면(Back sdie)에 배치해서 신호선과 분리하는 방식을 **BSPDN (Back side Power Delivery Network)**이라고 합니다.

<img src="/assets/img/posting/2025-02-24-github-blog-26-bspdn_1.png" alt="BSPDN" width=450>  
<p style="text-align: center;"><a href="https://www.thelec.kr/news/articleView.html?idxno=18342">[출처: 전자부품 전문 미디어 디일렉]</a></p>

반도체 공정이 점점 미세화됨에 따라(노드가 작아질수록) 트랜지스터의 집적도가 증가하고, 동일한 면적에 배치해야 할 신호선과 전력선의 수 또한 증가하면서 배선은 얇아지고 간격은 더 좁아지게 됩니다. 이로 인해 기존의 FSPDN 방식에서는 아래와 같은 문제가 점점 더 커지고 있습니다.

>**FSPDN 방식의 한계점 (by ChatGPT)**
>1. 신호 간섭  
>\- 신호선과 전력선이 매우 가까운 거리에 배치되면서 기생 커패시턴스 및 인덕턴스가 증가하고 이로 인한 신호 왜곡 및 전력 노이즈 유발  
>2. IR Drop 증가  
>\- 금속 배선이 얇아지고 길어지면서 배선의 저항이 커지고 이로 인한 IR Drop(전압 강하) 증가  
>\- 트랜지스터에 도달하는 전압이 일정하지 않게 되어, 성능 저하 및 전력 낭비 발생  
>3. 발열 및 신뢰성 문제 증가  
>\- IR Drop으로 인한 발열 문제 증가  
>\- 높은 전류 밀도로 인한 Electromigration(EM) 등 신뢰성 문제 발생

이러한 문제를 해결하기 위해 도입된 기술이 **BSPDN**으로 전력선을 Wafer 후면에 배치하여 신호선과 전력선 간의 간섭을 줄이고, IR Drop 및 발열을 감소시키며, Wafer 전면부의 Routing 혼잡도를 개선할 수 있다는 장점이 있습니다.  

그러나, Wafer 후면 공정 추가로 인한 비용 문제뿐만 아니라, Bonding, Grinding, Overlay 등의 기술적 어려움 등 아직 해결해야 할 과제가 많이 남아있습니다. 현재 주요 파운드리 기업들이 BSPDN 기술을 활발히 연구·개발 중이며, 향후 차세대 반도체 설계 및 제조에서 핵심적인 역할을 할 것으로 예상됩니다.