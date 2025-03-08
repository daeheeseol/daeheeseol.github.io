---
title: MPT (Multi Patterning Technology) 란?
description: MPT에 대해 알아보기
author: SemiDS
date: 2025-03-07 12:00:00 +0900
categories: [Semiconductor, Process]
tags: [MPT]
pin: true
---

## MPT (Multi Patterning Technology) 란?
반도체 공정에서 **MPT (Multi Patterning Technology)**는 Photolithography 공정에서 사용되는 ArF, KrF 등의 광원이 가진 파장 한계를 극복하고, 보다 미세한 선폭(Pitch)의 패턴을 형성하기 위해 사용되는 기술입니다.

광학적인 해상도의 한계로 인해 단일 노광(Exposure)으로는 구현할 수 없는 패턴을 만들기 위해 사용되며, 주요 방식으로는 패턴을 분할하여 노광을 여러번 진행하는 방식과 Spacer를 활용해 선폭을 줄이는 Self-aligned 방식이 있습니다.

> **(1) LELE (Litho-Etch-Litho-Etch)**  
> \- 구현하고자 하는 패턴을 분할해서(Coloring) 노광을 여러번 진행하는 방법  
> \- 노광(Lihto) → 식각(Etch) → 노광(Lihto) → 식각(Etch)의 순서를 반복해서 진행  
> \- 장점 : 구현할 수 있는 패턴의 자유도가 높고 기술적으로 구현하기가 비교적 용이함   
> \- 단점 : 공정 수가 늘어나 생산성이 떨어지고, 비용이 증가함. 패턴 정렬(Overlay) 문제 발생 가능[[`Overlay 란?`]]({{ '/posts/github-blog-28-overlay/' | absolute_url }})  
>
>**(2) SADP (Self-Aligned Double Patterning)**  
> \- Spacer 증착을 통해서 패턴의 선폭을 감소시키는 방법  
> \- 노광을 통해 Mandrel 역할을 하는 Bar 패턴을 형성하고 양측 벽에 Spacer를 증착한 뒤, 이를 Blocking Mask로 활용해 식각을 진행  
> \- SAQP (Self-Aligned Quadruple Patterning): SADP를 2번 진행해서 선폭을 1/4배로 감소  
> \- 장점 : Self-Aligned 방식이기 때문에 패턴 정렬(Overlay) 문제 없음  
> \- 단점 : LELE에 비해 공정이 복잡하고 추가적인 공정(식각, 증착 등)이 필요  

<img src="/assets/img/posting/2025-03-07-github-blog-30-mpt_1.png" alt="mpt" width=400>  
<p style="text-align: center;"><a href="https://en.wikipedia.org/wiki/Multiple_patterning">[출처: Wikipedia]</a></p>

최근에는 `EUV(Extreme Ultraviolet)` 노광 기술이 도입되면서, 기존에 ArF 기반 MPT를 통해 형성하던 패턴을 EUV로 한 번에 구현하는 것이 가능해졌습니다. 그러나 EUV로도 한번에 구현할 수 없는 초미세 선폭의 경우 여전히 LELE와 같은 MPT 방법이 사용되고 있습니다. 즉, MPT는 Photo 공정의 해상도를 높이는 데 필수적인 핵심 기술로, 앞으로도 반도체 미세화가 지속됨에 따라 중요한 역할을 계속해서 수행할 것으로 예상됩니다.