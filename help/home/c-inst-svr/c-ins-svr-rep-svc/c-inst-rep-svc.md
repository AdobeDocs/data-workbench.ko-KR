---
description: Insight ServerReplication Service를 사용하면 한 Insight Server 컴퓨터에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.
title: 복제 서비스 설치
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
exl-id: a235fe75-a6d0-4c20-8ea2-8b1cbad12da7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---

# 복제 서비스 설치{#installing-the-replication-service}

Insight ServerReplication Service를 사용하면 한 Insight Server 컴퓨터에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.

일반적으로 데이터가 수집 및 저장되는 시스템은 [!DNL Repeater] 시스템으로 실행되도록 구성됩니다. [반복 기능](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md)을 참조하십시오. [!DNL Replicate.cfg] 파일로 구성된 [!DNL Replication Service]을 사용하면 [!DNL Insight Server] 컴퓨터에서 [!DNL Repeater] 컴퓨터에서 데이터를 검색하고 로컬에 저장할 수 있습니다. [!DNL Insight Server] 컴퓨터는 대상 컴퓨터라고 합니다. 여러 개의 [!DNL Insight Server] DPU를 하나의 [!DNL Repeater]에 연결하여 여러 데이터 집합에 포함할 수 있도록 이벤트 데이터의 복사본을 요청할 수 있습니다.

방화벽이 있는 여러 레이어가 있는 네트워크 인프라에서 [!DNL Replication Service]을 사용하여 방화벽으로 분리된 구성 요소 간의 단일 포트 간 통신을 수행할 수 있습니다.

**를 설치하려면[!DNL Replication Service]**

[!DNL Replicate.cfg] 파일은 [!DNL Insight Server] 설치의 일부로 설치해야 합니다. [!DNL Insight Server] 설치 디렉토리의 [!DNL Components] 폴더에서 파일을 찾을 수 있습니다. 이 파일이 없으면 Adobe에 문의하십시오.
