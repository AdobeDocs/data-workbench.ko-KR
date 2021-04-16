---
description: Adobe 서버 제품이 설치된 컴퓨터가 최소 시스템 요구 사항 문서에 정의된 최소 시스템 요구 사항을 충족하는지 확인해야 합니다.
title: 시스템 상태 확인
uuid: 6d132865-36ab-40fc-be24-e031f356fce2
exl-id: 543f7592-dd3c-47ba-b174-5f12e9586378
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 5%

---

# 시스템 상태 확인{#confirming-your-systems-are-healthy}

Adobe 서버 제품이 설치된 컴퓨터가 최소 시스템 요구 사항 문서에 정의된 최소 시스템 요구 사항을 충족하는지 확인해야 합니다.

**권장 빈도:** 5-10분마다

또한 다음을 모니터링하는 것을 포함하되 이에 제한되지 않는 특정 하드웨어를 운영하기 위한 모범 사례에 따라 시스템을 모니터링해야 합니다.

* CPU 사용량
* 디스크 공간
* 하드웨어 시스템 메시지
* 내부 시스템 온도
* 메모리 사용
* 전원 공급 장치 조건
* RAID 또는 디스크 컨트롤러 성능 및 오류

Adobe에서는 서버 컴퓨터의 시스템 매개 변수가 설정한 임계값을 초과할 때 관리자에게 경고하도록 관리 도구를 구성하는 것이 좋습니다.

[!DNL Insight Server] 컴퓨터의 경우 설정한 최소 디스크 공간 제한에 도달하는 시기를 나타내도록 각 [!DNL Insight Server]을 구성하는 것이 좋습니다. 이러한 경고에 대한 자세한 내용은 [관리 경고 구성](../../../home/c-inst-svr/c-admin-inst-svr/t-config-adm-alrts.md#task-0858f588da4941aa9d4952f6592681aa)을 참조하십시오.
