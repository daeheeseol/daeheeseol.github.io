---
title: VM (Virtual Metrology) 이란?
description: VM에 대해 알아보기
author: SemiDS
date: 2025-02-19 12:00:00 +0900
categories: [Semiconductor, Metrology & Inspection]
tags: [VM]
pin: true
---

## VM (Virtual Metrology) 이란?
**VM (Virtual Metrology, 가상 계측)**은 반도체 제조 공정에서 실제 계측 장비를 사용하지 않고, 공정 설비 내 장착되어 있는 센서(Sensor)에서 수집된 데이터를 통해 공정 결과(Wafer의 품질 등)를 예측하는 방법입니다.  

일반적으로 반도체 공정에서는 다양한 계측과 검사를 통해 Wafer의 품질, 상태, 이상 유무 등을 확인하는데 시간과 비용 등의 문제로 일부 Wafer만 샘플링해서 진행하게 됩니다. 그러나, 이러한 방식은 샘플링되지 않은 Wafer에 이상이 있을 가능성을 배제할 수 없고, 공정 조건이 미세하게 변화할 경우 이를 즉각적으로 감지하기 어렵다는 한계가 있습니다.  

이러한 한계를 보완하기 위해 **VM** 기술이 도입되었으며, 공정 장비에서 수집되는 센서 데이터(온도, 압력, 전류 등)를 통계적 기법이나 머신러닝 알고리즘을 통해 Wafer의 품질을 대변할 수 있는 데이터로 재생성하고 이를 통해 공정이 진행된 모든 Wafer에 대한 품질을 예측하는 방식입니다. 또한, 설비의 이상을 감지하거나 불량을 예측하는 데에도 활용되며 필요할 경우 추가적인 계측·검사를 수행하거나 공정을 즉각적으로 조정하기 위해서도 활용됩니다.  

<img src="/assets/img/posting/2025-02-19-github-blog-22-vm_1.png" alt="VM" width=400>  
<p style="text-align: center;"><a href="https://news.skhynix.com/gauss-labss-ai-based-virtual-metrology-solution/">[출처: SK hynix Newsroom]</a></p>

VM은 반도체 제조에서 비용 절감, 생산성 향상, 공정 최적화 등을 위해 활용되는 중요한 기술이지만, 예측 정확도 문제나 공정 변화 대응 한계 등의 이유로 실제 계측을 완전히 대체하기보다는 보완적인 역할로 활용되고 있습니다. 그러나, 최근 AI/ML 기술이 급격하게 발전하면서 더욱 다양한 데이터를 활용한 정교한 예측이 가능해지고 있으며, 이에 따라 VM의 적용 범위도 점차 확대되고 있습니다.

<br>

-참고 Article  
>[Virtual metrology in semiconductor manufacturing: Current status and future prospects](https://www.sciencedirect.com/science/article/abs/pii/S095741742400424X)  
>[https://www.brique.co.kr/products/vm](https://www.brique.co.kr/products/vm)

