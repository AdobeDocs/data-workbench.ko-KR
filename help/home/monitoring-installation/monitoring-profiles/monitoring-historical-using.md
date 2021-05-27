---
description: Data Workbench 기록 프로필을 사용하여 구성, 하드웨어 및 기타 변경 사항이 시간에 따른 성능, 안정성 및 서버 성능에 어떻게 영향을 주는지 확인하십시오.
title: Data Workbench 기록 작업 영역
uuid: 61c45cae-f255-4d20-bb6b-f318c8dd8214
exl-id: e6d7e924-641e-468c-a828-16ebe1c8724f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 2%

---

# Data Workbench 기록 작업 영역{#data-workbench-historic-workspace}

Data Workbench 기록 프로필을 사용하여 구성, 하드웨어 및 기타 변경 사항이 시간에 따른 성능, 안정성 및 서버 성능에 어떻게 영향을 주는지 확인하십시오.

기록 프로필에는 프로필 기반 [프로필 성능](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-184a86f9de054970bf68515bb9dea85d) 데이터 세트와 **[!UICONTROL Performance]** 탭 아래에 있는 서버 기반 [서버 성능](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5dad5870384b40e094d50173fcd90a09) 데이터 세트가 포함되어 있습니다. 이는 Data Workbench 서버 성능에 대한 이전 관점에서 본 가장 일반적으로 사용되는 데이터 세트입니다. 또한 **[!UICONTROL Up Time]** 탭을 선택하여 [구성 요소](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) 및 [처리 모드](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66)를 볼 수 있습니다.

![](assets/Historic_Performance.png)

또한 **[!UICONTROL Up Time]** 탭을 선택하여 [구성 요소](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) 및 [처리 모드](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66)를 볼 수 있습니다.

Data Workbench 내역 프로필에 사용되는 차원에 대한 추가 참조 정보는 Insight 내역 프로필의 [Dimension을 참조하십시오.](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)

## 프로필 성능 작업 공간 {#section-184a86f9de054970bf68515bb9dea85d}

이 데이터 세트에는 Data Workbench 모니터링을 위한 다음 관련 지표가 포함되어 있습니다.

* 빠른 입력 MegaBytes/Minute—초기 로그 처리 중 대량의 데이터 입력을 표시하는 지표.
* 빠른 병합 분당 MegaBytes—변형을 표시하는 지표.

![](assets/Historic_Profile_Performance.png)

>[!NOTE]
>
>프로필에 대한 실제 성능 평가를 수행하려면 경과된 달력 시간이 아닌 속도를 확인합니다. 이 비율은 10분마다 폴링 사이에 변경된 값으로 측정됩니다.

## 서버 성능 작업 공간 {#section-5dad5870384b40e094d50173fcd90a09}

이 데이터 집합은 포함된 프로필의 범위를 넘어 서버 지표를 모니터링하고 Data Workbench 모니터링을 위한 다음과 같은 관련 서버 지표를 포함합니다.

* 예상 청소 시간(분) - 예상 쿼리 해결 시간입니다.
* 폴링 지연 시간 밀리초 — 모든 구성 요소를 제공하는 전체 주기를 통과하는 데 걸리는 시간을 측정하여 소프트웨어의 사용 빈도를 나타냅니다.

![](assets/Historic_Server_Performance.png)

## 구성 요소 작업 공간 {#section-5be7223abb384784bafe7b37c764ea66}

이 데이터 세트는 업 시간 탭 아래에 있습니다.

![](assets/Up_Time.png)

구성 요소 데이터 세트에는 구성 요소 상태에 대한 두 가지 측면이 포함되어 있습니다.

* 통신 지표 — Data Workbench 서버 프로세스가 응답했습니까?
* 모든 구성 요소 지표 — 세부 상태 페이지 맨 위에는 호스트가 Data Workbench 서버 프로세스 내에서 서비스하고 있는 구성 요소 목록이 있습니다. 구성 요소가 오류 상태에 있으면 오류 테이블의 구성 요소 아래에 나열됩니다.

![](assets/Up_Time_components.png)

## 처리 모드 작업 공간 {#section-3e1dedb9474e4b4ba513240943e76817}

이 작업 공간은 업 시간 탭 아래에 있습니다. 이 작업 공간을 사용하면 빠른 입력, 빠른 병합 및 실시간 모드에서 걸리는 시간을 관찰할 수 있습니다.

![](assets/Up_Time_Processing_mode.png)

이 데이터 집합은 대상 데이터 로드 식별과 같은 중요한 서버 로드 특성을 제공합니다

* 요일(예: 화요일과 수요일의 빠른 입력 비율),
* 시간(빠른 입력 모드에 있는 날짜 비율은 얼마입니까?)
