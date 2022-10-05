---
description: Adobe 서버 제품이 설치된 시스템이 최소 시스템 요구 사항 문서에 정의된 최소 시스템 요구 사항을 충족하는지 확인해야 합니다.
title: 시스템 상태 확인
uuid: 6d132865-36ab-40fc-be24-e031f356fce2
exl-id: 543f7592-dd3c-47ba-b174-5f12e9586378
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 5%

---

# 시스템 상태 확인{#confirming-your-systems-are-healthy}

{{eol}}

Adobe 서버 제품이 설치된 시스템이 최소 시스템 요구 사항 문서에 정의된 최소 시스템 요구 사항을 충족하는지 확인해야 합니다.

**권장 빈도:** 5-10분마다

또한 다음 사항을 모니터링하되 이에 국한되지 않고 특정 하드웨어를 동작하기 위한 모범 사례에 따라 시스템을 모니터링해야 합니다.

* CPU 사용
* 디스크 공간
* 하드웨어 시스템 메시지
* 내부 시스템 온도
* 메모리 사용
* 전원 공급 장치 조건
* RAID 또는 디스크 컨트롤러 성능 및 오류

Adobe은 서버 컴퓨터의 시스템 매개 변수가 설정한 임계값을 초과할 경우 관리자에게 경고하도록 관리 도구를 구성할 것을 권장합니다.

대상 [!DNL Insight Server] 시스템, Adobe은 각 [!DNL Insight Server] 설정된 최소 디스크 공간 제한에 도달하는 시기를 나타냅니다. 이러한 경고에 대한 자세한 내용은 [관리 경고 구성](../../../home/c-inst-svr/c-admin-inst-svr/t-config-adm-alrts.md#task-0858f588da4941aa9d4952f6592681aa).
