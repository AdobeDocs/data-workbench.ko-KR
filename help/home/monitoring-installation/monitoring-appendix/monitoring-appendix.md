---
description: 이 문서에서는 Data Workbench 모니터링 프로필에 사용되는 필드, 차원 및 지표와 함께 프로필에 대해 설명합니다.
title: Data Workbench 프로필 차원 및 지표
uuid: 42ef154f-fd8b-4609-8685-96d9dbf32a3d
exl-id: cfad9897-2ea3-47e4-aa36-416e0fde9358
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 5%

---

# Data Workbench 프로필 차원 및 지표{#data-workbench-profile-dimensions-and-metrics}

이 문서에서는 Data Workbench 모니터링 프로필에 사용되는 필드, 차원 및 지표와 함께 프로필에 대해 설명합니다.

Data Workbench 서버를 모니터링하기 위해 특정 서버 정보도 캡처하는 동시에 세부 상태를 구문 분석하는 스크립트를 사용하여 데이터가 수집됩니다. 그런 다음 Data Workbench 서버 정보가 VSL 파일을 수집하고 저장하도록 Data Workbench 센서에 대한 페이지 태그 호출에 전달됩니다.

## Data Workbench 모니터링 프로필에 사용되는 프로필 {#section-b5b1234f55c3407dae8e68b031b7cd7f}

이러한 프로필은 서버 상태 및 성능 데이터를 볼 수 있는 차원 및 지표를 제공합니다.

* [인사이트 프로필 상태 프로필의 Dimension](../../../home/monitoring-installation/monitoring-appendix/monitoring-profile-status.md#concept-d4cd7da41c8a42bab4aea25418264e64)
* [Insight Server 상태 프로필의 Dimension](../../../home/monitoring-installation/monitoring-appendix/monitoring-servers-profile.md#concept-8cbeb91e99bc42e2b52b22d551423f8a)
* [인사이트 기록 프로필의 Dimension](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)
* [Insight 기록 모니터링 프로필의 지표](../../../home/monitoring-installation/monitoring-appendix/monitoring-hist-metrics.md#concept-8fece88b1f014637bbc7c8372ee93203)

상태 프로필을 사용하면 작업 관점에서 Data Workbench가 현재 어떻게 작동하는지 확인할 수 있습니다. **프로필 상태** 프로필 및 **서버 상태** 프로필은 세부 상태 및 Data Workbench 서버에서 데이터를 수집합니다. 수집된 모든 데이터는 사용할 `cs-uri-query` 필드에 배치됩니다.

**기록 프로필**&#x200B;을 사용하면 이전 데이터를 사용하여 구성 및 하드웨어 변경 사항이 미치는 영향을 평가할 수 있습니다. 이전 프로필은 시간에 따른 구성 및 하드웨어 변경의 영향을 평가할 수 있으므로 가장 유용할 수 있습니다.
