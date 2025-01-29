---
title: DFM (Design For Manufacturability) 란?
description: DFM에 대해 알아보기
author: SemiDS
date: 2025-01-29 12:00:00 +0900
categories: [Semiconductor, Layout]
tags: [DFM]
pin: true
---

## DFM (Design For Manufacturability) 란?
`DFM`을 직역하면 **제조를 위한 설계**인데 이는 제조하기 쉬운 방식으로 제품을 설계해 제품의 생산성을 높이기 위한 일반적인 설계 방법론으로, DFM의 주요목적은 아래와 같습니다. 

>DFM의 주요 목적 (by ChatGPT)  
>- 제조 수율 향상: 공정에서 발생할 수 있는 결함을 최소화하여 생산된 칩의 양품 비율을 높입니다.  
>- 생산 비용 절감: 설계와 제조 간의 불일치를 줄여 재작업이나 폐기를 최소화합니다.  
>- 제조 공정 최적화: 설계가 제조 공정의 물리적 한계를 넘어가지 않도록 조정하여, 공정 장비와 재료의 성능을 최대로 활용합니다.

즉, DFM은 반도체 제조에서만 사용되는 방법론은 아니지만 반도체 제조 과정이 점점 더 미세화되고 복잡해짐에 따라 DFM의 필요성이 점차 커지고 있으며, 반도체 제조 과정이 매우 복잡하기 때문에 DFM의 적용 방법 및 범위 또한 매우 다양해지고 있습니다.  
<br>
아래는 DFM을 적용하는 일부 예시를 나열한 것으로 워낙 광범위하기 때문에 한 부서에서 전부 담당하기는 어렵고 다양한 부서가 유기적으로 연결되어 DFM을 수행한다고 할 수 있습니다.

>- Floorplanning & PnR (Place and Route) 최적화 
>- Design rule 설정을 통한 취약 Pattern 설계 제약
>- Dummy (Fill) Layer 삽입을 통한 Pattern Uniformity 최적화
>- OPC (Optical proximity correction)를 통한 Layout Pattern 보정
>- Hotspot Analysis를 통한 취약 Pattern 발굴 및 수정
{: .prompt-info }

위와 같은 DFM Solution들은 Siemens, Synopsys, Cadence 등 다양한 Electronic Design Automation (EDA) 업체에 의해 개발되고 있으며, 최근에는 AI/ML 기술도 통합해 최적의 DFM을 위한 다양한 방법론을 제공하고 있습니다.  
<br>
예를 들어, Siemens사의 경우는 Hotspot Analysis를 위한 _Calibre SONR_, _Calibre LFD_ 등의 ML 기반 platform을 구축해서 제공하고 있으며, 이외에도 다양한 platform들이 현재도 지속적으로 개발되고 있습니다.

>Calibre SONR is a feature-based machine learning platform that transfers the layout and process information to features. Calibre SONR machine-learning models can be used for various full-chip applications, including hotspot prediction and analysis, pattern reduction, and coverage check.
>
>![Calibre SONR](/assets/img/posting/2025-01-29-github-blog-1_1.png)
>[[출처: Siemens EDA]](https://eda.sw.siemens.com/en-US/ic/calibre-manufacturing/fab-solutions/calibre-sonr/)

<br>

-참고 Article
>[반도체 설계 자동화의 핵심, EDA(Electronic Design Automation) 트렌드](https://s-core.co.kr/insight/view/%EB%B0%98%EB%8F%84%EC%B2%B4-%EC%84%A4%EA%B3%84-%EC%9E%90%EB%8F%99%ED%99%94%EC%9D%98-%ED%95%B5%EC%8B%AC-edaelectronic-design-automation-%ED%8A%B8%EB%A0%8C%EB%93%9C/)  