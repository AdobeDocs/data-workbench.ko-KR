---
description: 데이터 워크벤치 프로파일 상태 프로파일은 서버 지표나 내역 데이터가 아닌 프로파일을 기반으로 데이터 워크벤치 서버 상태에 대한 현재 정보를 제공합니다.
solution: Analytics
title: 데이터 워크벤치 프로파일 상태 작업 영역
topic: Data workbench
uuid: b54713c8-863d-4376-8ebf-4a2985e28c76
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 워크벤치 프로파일 상태 작업 영역{#data-workbench-profile-status-workspace}

데이터 워크벤치 프로파일 상태 프로파일은 서버 지표나 내역 데이터가 아닌 프로파일을 기반으로 데이터 워크벤치 서버 상태에 대한 현재 정보를 제공합니다.

## 데이터 워크벤치 프로파일 상태 {#section-65d1fa393cfd450cbacef3cba823fcc1}

이 상태 프로필은 에이전트가 10분마다 폴링되고 보고 기능에는 항상 10분 지연이 포함되기 때문에 현재 데이터 워크벤치 서버 정보를 제공하지만 실제 시간은 아닙니다. 보다 정확하게 말하자면, 이 프로필로 생성된 데이터 집합은 에이전트로부터 서버에 대한 최신 관찰을 제공하며, 이것은 대개 기본 폴링 기간이 10분입니다.

데이터 워크벤치 프로필 상태 프로필에 사용된 차원에 대한 추가 참조 정보는 인사이트 [프로필 상태 프로필을](../../../home/monitoring-installation/monitoring-profiles/monitoring-profile-using.md#concept-d4cd7da41c8a42bab4aea25418264e64)참조하십시오.

![](assets/Status_General_Status.png)

이 보고서는 구성 요소나 특정 트래픽 변동성이 아닌 작업 모니터링에 유용합니다.

![](assets/Status_General_page.png)

이는 누가 어떤 모드에 있는지를 알려줍니다.특정 프로필에 대한 빠른 입력 속도가 높은 경우 해당 프로필은 빠른 입력 모드입니다.

중단된 지표가 1이면 서버가 정지됩니다. 값이 0이면 서버가 중지되지 않습니다.

**대량 일괄 로드를 위한 로그 읽기**

![](assets/Status_General_stalled_log.png)

