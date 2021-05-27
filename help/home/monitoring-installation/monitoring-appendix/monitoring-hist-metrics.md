---
description: 다음은 Data Workbench 내역 모니터링 프로필에 포함된 지표와 이러한 지표의 파생 방법을 나열합니다.
title: Data Workbench 내역 모니터링 프로필의 지표
uuid: 47b874f7-8acb-4593-9ac9-5997d5279e52
exl-id: 65f0f605-f128-45bb-8f6c-95284b2da740
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 2%

---

# Data Workbench 내역 모니터링 프로필의 지표{#metrics-in-the-data-workbench-historical-monitoring-profile}

다음은 Data Workbench 내역 모니터링 프로필에 포함된 지표와 이러한 지표의 파생 방법을 나열합니다.

| **경고 임계값** | 각 Ping에 대한 경고 위기 차원의 합계입니다. |
|---|---|
| **경고 다운** | 각 Ping에 대한 경고 다운 차원의 합계. |
| **경고 경고** | 각 Ping에 대한 경고 차원의 합계. |
| **모든 구성 요소** | 구성 요소 확인 성공 이 &quot;1&quot;인 Ping의 카운트를 Ping 지표에 100을 곱한 값으로 나눈 값입니다. |
| **지연 시간(분)** | 이 지표는 각 Ping에 대한 지연 시간 분 의 합계로, Ping 지표로 나눈 값입니다. |
| **블록** | 각 블록에 대한 1의 합계. |
| **모두 차단** | 모든 블록. |
| **전체 용량** | 능력 크기 측정 단위는 2에 능력 행 측정 단위가 3으로 나누어집니다. |
| **용량 행** | 각 Ping에 대한 능력 행 백분율 차원의 합계를 Ping 지표로 나눈 값입니다. |
| **용량 크기** | 각 Ping에 대한 용량 크기 백분율 차원의 합계를 Ping 지표로 나눈 값입니다. |
| **통신** | 빠른 확인 성공 이 &quot;1&quot;과 일치하는 Ping 수를 Ping 지표로 나눈 값입니다. |
| **자세한 확인 시간(초)** | Ping 유형이 &quot;서버&quot;인 각 Ping에 대한 Detailed Check Seconds 차원의 합계를 Ping 지표로 나눈 값입니다. |
| **Dimension GigaBytes** | 각 Ping에 대한 Dimension GB의 합계를 Ping 지표로 나눈 값입니다. |
| **디스크 &quot;x&quot;** | 디스크 지표는 각 Ping에 대해 사용된 디스크 백분율의 합계를 Ping 지표로 나누어 계산됩니다. |
| **예상 청소 시간(분)** | 이 값은 각 Ping에 대한 예상 쓸기 예상 지표의 합계이며, 예상 쓸기 감소율이 0보다 큰 Ping 지표로 나누어져 모두 6으로 나누어집니다. |
| **빠른 입력 시간(분)** | 각 Ping에 대한 빠른 입력 MegaBytes/Minute 합은 빠른 입력 MegaBytes/Minute가 0보다 큰 경우 Ping 수로 나누어집니다. |
| **빠른 입력 모드** | 처리 모드 차원이 Ping으로 나눈 &quot;빠른 입력&quot;과 동일한 Ping입니다. |
| **분당 빠른 병합 MegaBytes** | 각 Ping에 대한 초당 빠른 병합 MB의 합계로 Ping 지표로 분할됩니다. |
| **빠른 병합 모드** | 처리 모드가 &quot;빠른 병합&quot;과 같은 Ping은 Ping 지표로 나누어집니다. |
| **필드 GigaBytes** | 각 Ping에 대한 필드 GB 차원의 합계를 Ping 지표로 나눈 값입니다. |
| **로드** | 각 Ping에 대한 로드 평균 차원의 합계로 Ping 지표로 분할됩니다. |
| **로그 읽기** | 각 Ping에 대한 로그 읽기 처리 차원의 합계를 Ping 지표로 나눈 값으로, 모두 10으로 나눕니다. |
| **메모리 페이지** | 각 Ping에 대한 메모리 페이지 파일 백분율의 합계를 Ping 지표로 나눈 값입니다. |
| **메모리 물리적** | 각 Ping에 대한 메모리 실제 비율 차원의 합계를 Ping 지표로 나눈 값입니다. |
| **메모리 쿼리** | 각 Ping에 대한 메모리 쿼리 비율 합계를 Ping 지표로 나눈 값입니다. |
| **메모리 총 GB** | 각 Ping에 대한 메모리 실제 MegaBytes 총 차원의 합계로서 Ping 지표로 분할됩니다. |
| **네트워크 연결** | 각 Ping에 대한 네트워크 연결 합계를 Ping 지표로 나눈 값입니다. |
| **Ping x 용량 전체** | Ping 지표에 전체 능력 지표를 곱한 값입니다. |
| **폴링 지연 시간 밀리초** | 각 Ping에 대한 폴링 지연 센티미터 차원의 합과 Ping 지표를 모두 10으로 나눈 값입니다. |
| **쿼리 실행 중** | 예상 청소 손실이 &quot;0&quot;보다 큰 각 Ping에 대해 1의 합계를 Ping 유형이 &quot;서버&quot;인 Ping 지표로 나눈 값입니다. |
| **빠른 확인 초** | Ping 유형이 &quot;서버&quot;와 동일한 각 Ping에 대한 빠른 확인 초 의 합계를 Ping 지표로 나눈 값입니다. |
| **출력 행** | 각 Ping에 대한 출력 행 차원의 합과 Ping 지표를 곱하는 100000. |
| **실시간 모드** | 처리 모드 차원이 &quot;실시간&quot;과 같은 Ping의 수를 Ping 지표로 나눈 값으로 모두 100을 곱합니다. |
| **재처리 모드** | 100에서 처리 모드가 &quot;실시간&quot;과 같은 Ping 수를 Ping 지표로 나눈 100과 곱한 값입니다. |
| **정지** | 인사이트 [프로필 상태](../../../home/monitoring-installation/monitoring-appendix/monitoring-profile-status.md#concept-d4cd7da41c8a42bab4aea25418264e64) 프로필의 처리 정지된 차원의 합계. |
| **임시 DB** | 각 Ping에 대한 Temp DB 공간 백분율의 합계를 Ping 지표로 나눈 값입니다. |
| **변환** | 각 Ping에 대한 변형 백분율의 합계를 Ping 지표로 나눈 값은 모두 10으로 나누어집니다. |
