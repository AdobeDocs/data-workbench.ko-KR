---
description: Data Workbench을 구현할 때 마케팅 환경에 적합한 비즈니스 질문을 수집하고 설명합니다.
title: Data Workbench 검색 및 요구 사항
uuid: 436f0c32-b4e2-41dd-a8e9-531e0a195276
exl-id: 25cc2940-800a-4ad2-a7bb-c343e3d65500
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 8%

---

# Data Workbench 검색 및 요구 사항{#data-workbench-discovery-and-requirements}

{{eol}}

Data Workbench을 구현할 때 마케팅 환경에 적합한 비즈니스 질문을 수집하고 설명합니다.

이 섹션에서는 Data Workbench(DWB)에서 솔루션을 구축하는 데 필요한 질문 및 작업에 대한 입력을 수집하여 이러한 질문을 정확하고 모호하게, 기술에 관계없이 비즈니스 용어 및 Adobe Analytics Premium 솔루션에 대한 참조를 제공할 수 있습니다. 이 섹션에서는 이러한 목표 및 관련 요구 사항에 대한 정보를 제공합니다.

## 1단계: 주요 비즈니스 목표/목표 {#section-bb8f3d6071bf48d9a546ac2b80341e1d}

다음 표에서는 고객 기반을 식별하고 DWB 구현의 구성을 분석하라는 메시지를 표시합니다.

* 고객 기반 이해
* 특정 비즈니스 사례 이해(예: 셀프 서비스 및 기타 데이터 채널/오프라인 데이터 소스의 효율성)

**고객 기반 이해**

고객이 사이트를 사용하는 이유, 고객이 직면하는 과제 및 DWB가 비즈니스 모델을 기반으로 사용자에게 어떤 도움을 주는지 이해합니다. 예를 들어, 다른 제품 및 서비스를 교차 판매하도록 고객을 측정, 모니터링 및 분석하고, 활성 사용자 및 계정 침투 목록 및 기타 목표를 얻는 방법을 알아봅니다.

| ID | 비즈니스 질문/요구 사항 | 우선 순위 | 단계 | 종속성 |
|---|---|---|---|---|
| 1a | 특정 비즈니스 질문 1 | 높음/중간/낮음 | 1 | 공통 키, 다른 키 등에 따라 다름 |
| 1b | 특정 비즈니스 질문 2 | 높음 | 1 | 모든 종속성 |

분석 건설

<table id="table_6CA959E521964E27804BB2A65EC4BBDE"> 
 <tbody> 
  <tr> 
   <td colname="col1">작업 공간 분석 데이터 소스</td> 
   <td colname="col2"> 작업 공간 이름 추가 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필요한 작업 공간 Dimension 및 지표 </p> </td> 
   <td colname="col2"> <p>Dimension 식별: </p> <p>지표 식별: </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필요한 작업 공간 필터, 플래그 및 도구 </td> 
   <td colname="col2"> <p>세그먼트 식별: </p> <p>도구 식별: </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이 분석에서 파생될 수 있는 작업은 무엇입니까? </td> 
   <td colname="col2"> 특정 DWB 작업 공간을 사용하여 작업 및 컨텐츠를 이해합니다. </td> 
  </tr> 
 </tbody> 
</table>

## 2단계: 특정 비즈니스 사례 이해 {#section-309d7ec6f631458c9c9e6bd2cef2fa4c}

다른 데이터 소스 및 채널을 파악하고 이러한 기능이 비즈니스 사례와 어떻게 연결되는지 알아봅니다.

<table id="table_733CCD9F4E9048C2865758B8E8D027DC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> ID </th> 
   <th colname="col2" class="entry"> 비즈니스 질문/요구 사항 </th> 
   <th colname="col3" class="entry"> 우선 순위 </th> 
   <th colname="col04" class="entry"> 단계 </th> 
   <th colname="col4" class="entry"> 종속성 </th> 
   <th colname="col5" class="entry"> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 2a </td> 
   <td colname="col2"> 특정 비즈니스 요구 사항 1 </td> 
   <td colname="col3"> <p>높음/중간/낮음 </p> </td> 
   <td colname="col04"> 1 </td> 
   <td colname="col4"> <p>일반 키, 일부 다른 키, 계정 플래그/식별자 등에 따라 다릅니다. </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2b </td> 
   <td colname="col2"> <p>특정 비즈니스 요구 사항 2 </p> </td> 
   <td colname="col3"> 높음/중간/낮음 </td> 
   <td colname="col04"> 1 </td> 
   <td colname="col4"> <p>모든 종속성 </p> </td> 
   <td colname="col5"> </td> 
  </tr> 
 </tbody> 
</table>

**분석 구성**

<table id="table_680C5D257CBF42519EFB8B96A00543C5"> 
 <tbody> 
  <tr> 
   <td colname="col1">작업 공간 분석 데이터 소스
     </td> 
   <td colname="col2">
     샘플 작업 공간 이름 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필요한 작업 공간 Dimension 및 지표 </p> </td> 
   <td colname="col2"> <p>Dimension: 필요한 차원을 정의합니다. </p> <p>지표: 필요한 지표를 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필요한 작업 공간 필터, 플래그 및 도구 </td> 
   <td colname="col2"> <p>세그먼트: 고객 세그먼트를 식별합니다. </p> <p>도구: 필요한 도구를 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이 분석에서 파생될 수 있는 작업은 무엇입니까? </td> 
   <td colname="col2"> 이 작업 영역에서 알아야 할 사항 </td> 
  </tr> 
 </tbody> 
</table>

**데이터 소스**

| 데이터 소스 | 우선 순위 | 데이터를 받는 빈도는 얼마나 됩니까? |
|---|---|---|
| 사이트 1 이름 보고서 세트(RSID) | 1 | 시간별 |
| 사이트 2 이름(있는 경우)(RSID) | 1 | 시간별 |
| 데이터 소스 1(해당되는 경우) | 2개 | 일별? |
| 데이터 소스 2(해당되는 경우) | 3 | 일별? |
