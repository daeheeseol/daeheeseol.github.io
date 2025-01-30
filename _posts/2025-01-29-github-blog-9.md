---
title: ADC (Automatic Defect Classification) 란?
description: ADC에 대해 알아보기
author: SemiDS
date: 2025-01-29 12:00:00 +0900
categories: [Semiconductor, Inspection]
tags: [ADC]
pin: true
---

## ADC (Automatic Defect Classification) 란?
**ADC (Automatic Defect Classification)**는 반도체 제조 공정에서 발생하는 불량(Defect)을 종류, 모양, 크기 등에 따라서 자동으로 분류하는 기술을 의미합니다.  
반도체 제조 과정은 매우 복잡하며 포토(Photo), 식각(Etch), 세정(Clean) 등 여러 공정이 연속적으로 진행되기 때문에, 다양한 공정 진행 후 검출된 불량을 유형별로 분류해서 주요한 불량이 어느 공정에서 발생한건지 정확하게 파악해 해당 공정을 개선하는 과정이 수율 향상에 있어 매우 중요합니다.  
<br>
위와 같은 이유로 검출된 불량을 유형별로 분류하는 과정이 반드시 필요한데, 공정이 복잡한 만큼 발생하는 불량의 종류와 형태도 다양하기 때문에 실제 현장에서는 엔지니어(사람)가 육안으로 불량을 분류하는 방식으로 업무가 수행되고 있습니다.  
즉, 엔지니어의 수작업에 따른 작업 부담 및 실수를 줄이고 불량을 신속 정확하게 분류하기 위해 ADC 기술이 필요로 된다고 할 수 있습니다.

>**ADC의 이점 (by ChatGPT)**  
>- **정확도 향상**: 사람이 육안으로 검사할 때 발생할 수 있는 실수를 줄이고, 보다 세밀한 결함까지 감지할 수 있습니다.  
>- **속도 개선**: 대량의 데이터를 빠르게 처리하여 검사 시간을 단축합니다.  
>- **비용 절감**: 수율 저하를 방지하고, 효율적인 공정 제어로 비용을 절감합니다.  

>[![ADC](/assets/img/posting/2025-01-29-github-blog-3_1.png)](https://www.brique.co.kr/products/adc)
>[[출처: Brique]](https://www.brique.co.kr/products/adc)

ADC 기술은 크게 아래와 같은 2가지 방법으로 개발되고 있습니다.
>- Die-to-Database (D2DB)를 이용한 방법
>- AI(딥러닝) 모델을 이용한 방법

D2DB 기반 방법에서는 불량 이미지를 설계 도면과 비교해 다른점이 있는지를 감지하고, 불량에 대한 특성(모양, 음영차이 등)을 이미지에서 추출해 불량을 유형별로 분류합니다. [[`D2DB (Die-to-Database) 란?`]]({{ '/posts/github-blog-8/' | absolute_url }}) 

또한, 최근에 이미지를 처리하기 위한 AI 모델(CNN 등)의 성능이 급격하게 발전하면서, ADC를 위한 AI 모델이 많이 개발되고 있습니다. [`참고 Article`]

지금까지 ADC 기술이 많이 진보되었지만, 새로운 유형의 불량이나 검사 장비 및 공정 조건에 따라 불량 이미지가 다르게 보이는 경우 제대로 분류할 수 없다는 한계점이 존재합니다.  
아직은 엔지니어를 완벽하게 대체 하기엔 어려움이 있어 보이지만, ADC는 반도체 제조의 핵심 기술로 지속적으로 연구·개발이 진행되어 향후 개선된 모델이 현장에 적용된다면, 엔지니어의 작업 부담을 줄이고 수율 향상에 크게 기여할 것으로 기대됩니다.

<br>

-참고 Article
>[woof999.log님의 블로그 : Automatic Defect Classification Using Semi-Supervised Learning With Defect Localization](https://velog.io/@woof999/Automatic-Defect-Classification-UsingSemi-Supervised-Learning-WithDefect-Localization)   
>[anandh.log님의 블로그 : Optimal Feature Selection for Defect Classification in Semiconductor Wafers](https://velog.io/@anandh/Optimal-Feature-Selection-for-Defect-Classificationin-Semiconductor-Wafers)
