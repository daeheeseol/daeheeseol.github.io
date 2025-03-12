---
title: DFT (Design For Testability) 란?
description: DFT에 대해 알아보기
author: SemiDS
date: 2025-03-09 12:00:00 +0900
categories: [Semiconductor, Design]
tags: [DFT]
pin: true
---

## DFT (Design For Testability) 란?
**DFT (Design for Testability)**는 제조된 반도체 칩이 정상적으로 동작하는지 효율적으로 테스트하기 위해, 설계 단계에서부터 테스트 용이성(Testability)을 고려하여 회로를 설계하는 기법입니다.

일반적으로 칩 제조가 완료되면, 웨이퍼 상태에서 각 개별 칩이 정상적으로 동작하는지 확인하는 과정이 필요합니다. 이를 보통 웨이퍼 테스트(Wafer Test)라고 부르며, 테스트 장비(ATE, Automated Test Equipment)의 프로브(Probe Card)를 통해 개별 칩에 테스트 신호를 입력하고, 출력이 논리적으로 정상인지 확인해서 양품과 불량품을 구별하게 됩니다.  

그러나 반도체 회로의 복잡도가 증가함에 따라, 테스트를 위한 입출력 신호의 경우의 수가 기하급수적으로 늘어나면서 모든 경우를 확인하여 양품과 불량품을 판별하는 것이 시간과 비용 측면에서 현실적으로 불가능해졌고, 이를 해결하기 위해 DFT 기법이 도입되었습니다.

> **DFT가 필요한 이유 (By ChatGPT)**  
>\- 결함 검출 능력 향상: 제조 과정에서 발생할 수 있는 결함을 빠르고 정확하게 찾아낼 수 있음  
>\- 테스트 비용 절감: 테스트 시간을 단축하고 장비의 부담을 줄일 수 있음  
>\- 수율(Yield) 개선: 불량품을 조기에 판별하여 전체적인 생산 품질을 높일 수 있음  
>\- 디버깅(Debugging) 용이성 향상: 설계 및 테스트 단계에서 문제를 신속하게 분석하고 수정 가능  

디지털 회로의 경우우 입력 값을 기반으로 출력이 결정되는 Combinational Logic (AND, OR, NOT, XOR 등)과 이전 상태와 입력값에 의해서 출력이 결정되는 Sequential Logic (Flip-Flop 등)의 두 가지 기본적인 유형으로 나뉘어집니다. 비교적 테스트가 간단한 Combinational Logic에 비해 Sequential Logic의 경우 출력이 입력뿐 아니라 이전 상태(과거 값)에도 영향을 받기 때문에 위에서 언급한 바와 같이 테스트 패턴이 매우 복잡해진다는 문제가 있습니다.

위와 같은 문제를 해결하기 위해, Flip-Flop에 Multiplexer(MUX)를 연결하여 Sequential Logic을 Combinational Logic처럼 테스트를 가능하게 해주는 `SCAN`, 테스트 패턴을 자동으로 생성하여 불량을 효과적으로 검출하는 `ATPG(Automatic Test Pattern Generation)` 등의 DFT 기법이 사용되며, 추가로 Memory 블록을 테스트하기 위해 테스트 패턴을 생성하는 논리 회로와 고장 여부를 판단하는 논리 회로를 함께 설계하는 `MBIST(Memory Built-In Self-Test)` 기법도 많이 활용됩니다.

현대 반도체 설계에서는 위와 같은 DFT 기법이 반도체 칩의 품질 보증, 테스트 효율성 향상, 비용 절감 등 다양한 측면에서 중요한 역할을 하고 있으며, 반도체 회로가 점점 더 복잡해짐에 따라 그 중요성은 점차 더 커질 것으로 예상됩니다. 

<br>

-참고 Article
>[ASJoon님의 블로그](https://asjoon.tistory.com/18)  
>[narabaljeon님의 블로그](https://blog.naver.com/PostView.naver?blogId=narabaljeon&logNo=220796663739)

