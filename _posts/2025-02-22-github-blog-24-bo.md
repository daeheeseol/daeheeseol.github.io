---
title: Bayesian Optimization 이란?
description: Bayesian Optimization에 대해 알아보기
author: SemiDS
date: 2025-02-22 12:00:00 +0900
categories: [Data Science, Machine Learning]
tags: [Bayesian Optimization]
pin: true
---

## Bayesian Optimization 이란?
**Bayesian Optimization**은 전역(Global) 최적화 기법 중 하나로, 확률적 모델(Surrogate Model)과 획득 함수(Acquisition Function)를 통해 목적 함수(Objective Function)의 최적점을 효과적으로 탐색하는 방법입니다.

최적화가 필요한 목적 함수를 수학적으로 표현하기 어렵거나 최적 조건을 찾는데 시간과 비용이 많이 들어가는 경우 Bayesian Optimization을 이용할 수 있으며, 대표적인 예시로 기계학습 모델의 하이퍼 파라미터 튜닝, 실험 조건 탐색 등이 있습니다.

반도체 식각(Etch) 공정을 예로 들면, 박막을 식각하기 위해서 가스 종류, 유량, 압력, 온도 등 다양한 변수들을 조절하게 되고 이 변수들의 조합에 따라 식각의 정도가 달라지게 됩니다. 하지만 변수들 간의 복잡한 상호 작용이 최종 결과에 미치는 영향을 명확한 수식으로 표현하기 어렵고, 가능한 모든 조합을 실험하여 최적의 공정 조건을 찾는 것은 시간과 비용 면에서 현실적으로 불가능합니다. 이런 경우, Bayesian Optimization을 통해 가장 적합한 변수 조합을 우선적으로 탐색해 최적화 과정의 효율을 극대화할 수 있습니다.

Bayesian Optimization은 일반적으로 아래와 같은 순서로 진행됩니다.  
1. 목적 함수의 확률적 모델링     
\- 수학적으로 표현하기 어려운 목적 함수를 불확실성을 고려한 확률적 모델(Surrogate Model)로 추정하는 과정으로 `Gaussian Process(GP)`와 같은 알고리즘을 사용합니다.
2. 획득 함수를 통한 최적점 후보 선정  
\- 추정된 목적 함수의 최적점 후보를 선정하는 과정으로 획득 함수(Acquisition Function)를 이용합니다. 획득 함수는 현재까지의 예측 정보를 바탕으로 `Exploration`과 `Exploitation` 사이의 균형을 조절해서 후보 지점을 선정하게 됩니다.
    >Exploration (탐색): 새로운 영역을 적극적으로 탐색하여 아직 평가하지 않은 값을 확인하는 전략  
    >Exploitation (활용): 현재까지 얻은 정보를 바탕으로, 이미 좋은 결과를 보인 영역을 집중적으로 확인하는 전략  
3. 모델 업데이트 및 반복을 통한 최적점 탐색  
\- 선정된 후보 지점에 대한 목표 함수의 결과를 확률적 모델에 반영한 뒤, 새로운 후보 지점을 다시 선정해서 결과를 평가하고 모델에 반영합니다. 이러한 과정을 반복적으로 수행하면서 최적점을 찾아가게 됩니다.

정리하면, Bayesian Optimization은 불확실성을 고려한 확률적 모델을 활용하여 전역 최적점을 효과적으로 찾는 강력한 기법입니다. 하지만 고차원 문제(변수가 많은 경우)나 데이터에 노이즈가 많은 경우에는 성능이 저하될 수 있으며, 이를 보완하기 위해 차원 축소 기법을 활용하여 변수의 수를 줄이는 등 다른 통계적 알고리즘을 함께 사용하는 접근 방법이 활용되고 있습니다.


