---
title: SVRF (Standard Verification Rule Format) 란?
description: SVRF에 대해 알아보기
author: SemiDS
date: 2025-01-28 12:00:00 +0900
categories: [Semiconductor, Layout]
tags: [SVRF, TVF]
pin: true
---

## SVRF (Standard Verification Rule Format) 란?
SVRF는 `Standard Verification Rule Format`의 약자로 Siemens EDA (구 Mentor Graphics)사의 Calibre라는 프로그램에서 사용되는 언어의 이름입니다. SVRF는 반도체 설계 Layout에 대한 _DRC (Design Rule Check)_, _LVS (Layout Versus Schematic)_, _LVL (Layout Versus Layout)_ 등의 검증(Verification)을 수행하기 위한 스크립트(보통 ruledeck이라고 지칭)를 작성하는데 사용됩니다.
<br>

> [Calibre SVRF 기술 소개](https://www.sw.siemens.com/ko-KR/sw-terms/svrf-tvf-technology/ "Calibre SVRF")


`GDS (Graphics Design System`)나 `OASIS (Open Artwork System Interchange Standar)` 포맷으로 만들어진 반도체 Layout 도면 파일 안에는 다양한 형태의 Polygon으로 이루어진 Layer들이 존재하는데, Layer들에 대한 width, space 등을 검증(DRC라고 부름)하기 위해 SVRF 문법에 맞춰서 ruledeck을 작성하고 이를 수행해서 error가 있는지 확인하는 방식입니다.
<br>

SVRF는 위에서 언급한 반도체 설계 Layout에 대한 검증 뿐만 아니라, Boolean operation (AND, OR, NOT 등)을 통한 Layer 생성 및 수정, Layout Pattern 분석, Defect(불량) 분석 등을 위해서도 다양하게 활용되며, 반도체에서 Layout Architecture 업무를 수행하기 위해서 필수로적으로 사용된다고 할 수 있습니다.
<br>

그러나, SVRF의 경우 반복문(for, foreach)이나 조건문(if, else if)과 같은 프로그래밍 언어로서의 기능이 없어, 복잡한 ruledeck을 작성해야 하는 경우 스크립트가 매우 복잡해지고 길어지는 등 효율적인 작성이 어렵다는 한계점이 있습니다. 
<br>

이를 개선하기 위해, 리눅스 환경에서 많이 사용되는 프로그래밍 언어 중 하나인 [Tcl (Tool Command Language)](https://www.tcl-lang.org/)을 SVRF와 결합한 `TVF (Tcl Verification Format)`라는 언어가 개발되었습니다. TVF에서는 Tcl 문법에 기반한 반복문, 조건문 및 사용자 정의 함수(Tcl에서는 procedure라고 부름) 등을 사용할 수 있고 이를 통해, 훨씬 더 효율적으로 ruledeck을 작성할 수 있습니다.

