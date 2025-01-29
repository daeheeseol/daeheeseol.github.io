---
title: D2DB (Die-to-Database) 란?
description: D2DB에 대해 알아보기
author: SemiDS
date: 2025-01-29 12:00:00 +0900
categories: [Semiconductor, Layout]
tags: [D2DB]
pin: true
---

## D2DB (Die-to-Database) 란?
반도체에서 `D2DB (Die-to-Database)`는 Wafer에 구현된 **Die(반도체 Chip)**와 **Database(반도체 설계 도면)**을 비교해서 검사 및 검증을 하는 방법론을 의미합니다.

>Die: Wafer 상에 구현된 개별 반도체 Chip  
>Database: 반도체 설계 도면(Layout), GDS나 OASIS 형식으로 저장

이와 같은 D2DB 방법론은 반도체 칩 제조 과정 중에 발생한 불량을 자동으로 탐지하고 분류하거나 (Automatic Defect Classification, ADC) 설계 데이터와 실제 Die 내 구현된 Pattern의 불일치 정도를 수치화해서(width, edge placement error 등) 공정 개선에 피드백을 하는 등 다양한 측면에서 활용되고 있습니다.  

<br>
D2DB에서 Die의 Pattern은 SEM(Scanning Electron Microscopy, 전자현미경)을 통해 이미지화 되고, 이렇게 얻어진 SEM 이미지와 설계 도면에 있는 Layer를 직접적으로 비교해 달라진 점이 있는지 감지합니다. 설계 도면 데이터를 reference로 사용하기 때문에 매우 정밀하다는 점 등 다양한 장점이 있습니다.

>**Die-to-Database의 장점 (by ChatGPT)**  
>**정밀한 결함 탐지**: 설계 데이터와 비교하므로, 제조 공정에서 발생하는 미세 결함을 놓치지 않습니다.  
>**자동화된 분석**: 검사 장비와 S/W를 결합하여, 대량 생산 공정에서도 빠르고 효율적인 검사 수행이 가능합니다.  
>**피드백 제공**: 분석 결과를 설계 및 공정에 피드백하여 개선 루프를 형성합니다.  

그러나, D2DB의 경우 이미지 프로세싱, 설계 데이터 핸들링, 이미지-설계 매칭 및 비교 등 고도화된 데이터 처리 능력과 경험에 기반한 엔지니어링이 필요로 되기 때문에 사용자 입장에서는 진입 장벽이 비교적 높은 편이라는 단점도 존재합니다.   

<br>
그럼에도 불구하고, 해당 기술의 중요성은 공정이 점차 미세화됨에 따라 더욱 커지고 있으며, 반도체 Chip의 품질과 수율을 개선하는 데 핵심적인 역할을 하고 있습니다.

추가로 다양한 업체에서 D2DB Solution을 구축해서 제공하고 있으며 대표적으로 KLA Tencor (구 Anchor Semiconductor)사의 [D2DB-Pattern Monitor](https://anchorsemi.com/Products/D2DB-PM/), Siemens 사의 [Calibre Defect Management](https://eda.sw.siemens.com/en-US/ic/calibre-manufacturing/fab-solutions/calibre-defect-management/) 등이 있습니다.

>![D2DB-PM](/assets/img/posting/2025-01-29-github-blog-2_1.png)
>[[출처: Anchor Semiconductor]](https://anchorsemi.com/Products/D2DB-PM/)