---
description: 이 문서에서는 데이터 워크벤치 모니터링 프로필에 사용되는 필드, 차원 및 지표가 있는 프로필에 대해 설명합니다.
solution: Analytics
title: 데이터 워크벤치 프로필 차원 및 지표
topic: Data workbench
uuid: 42ef154f-fd8b-4609-8685-96d9dbf32a3d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 워크벤치 프로필 차원 및 지표{#data-workbench-profile-dimensions-and-metrics}

이 문서에서는 데이터 워크벤치 모니터링 프로필에 사용되는 필드, 차원 및 지표가 있는 프로필에 대해 설명합니다.

데이터 워크벤치 서버를 모니터링하기 위해 특정 서버 정보를 캡처하는 동시에 세부 상태를 구문 분석하는 스크립트를 사용하여 데이터가 수집됩니다. 그런 다음 데이터 워크벤치 서버 정보가 데이터 워크벤치 센서가 수집하고 VSL 파일에 저장할 페이지 태그 호출로 전달됩니다.

## 데이터 워크벤치 모니터링 프로필에 사용되는 프로필 {#section-b5b1234f55c3407dae8e68b031b7cd7f}

이러한 프로필은 서버 상태 및 성능 데이터를 볼 수 있도록 해주는 차원 및 지표를 제공합니다.

* [인사이트 프로필 상태 프로필의 차원](../../../home/monitoring-installation/monitoring-appendix/monitoring-profile-status.md#concept-d4cd7da41c8a42bab4aea25418264e64)
* [Insight 서버 상태 프로필의 차원](../../../home/monitoring-installation/monitoring-appendix/monitoring-servers-profile.md#concept-8cbeb91e99bc42e2b52b22d551423f8a)
* [통찰력 내역 프로파일의 차원](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)
* [통찰력 내역 모니터링 프로필의 지표](../../../home/monitoring-installation/monitoring-appendix/monitoring-hist-metrics.md#concept-8fece88b1f014637bbc7c8372ee93203)

상태 프로필을 사용하면 데이터 워크벤치가 현재 운영 관점에서 어떻게 작동하는지 확인할 수 있습니다. 프로필 **상태** 프로파일과 서버 상태 **** 프로필은 세부 상태 및 데이터 워크벤치 서버에서 데이터를 수집합니다. 수집된 모든 데이터는 사용하기 위해 `cs-uri-query` 필드에 배치됩니다.

내역 **프로필을** 사용하면 내역 데이터를 사용하여 구성 및 하드웨어 변경의 영향을 평가할 수 있습니다. 내역 프로파일은 시간이 지남에 따라 구성 및 하드웨어 변경의 영향을 평가할 수 있도록 해주므로 가장 유용할 수 있습니다.
