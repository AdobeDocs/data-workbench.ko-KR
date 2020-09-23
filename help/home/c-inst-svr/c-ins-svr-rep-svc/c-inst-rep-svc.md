---
description: Insight ServerReplication Service를 사용하면 한 Insight Server 컴퓨터에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.
solution: Analytics
title: 복제 서비스 설치
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---


# 복제 서비스 설치{#installing-the-replication-service}

Insight ServerReplication Service를 사용하면 한 Insight Server 컴퓨터에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.

일반적으로 데이터가 수집 및 저장되는 시스템은 컴퓨터로 실행되도록 [!DNL Repeater] 구성됩니다. 반복 [기능을 참조하십시오](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). 파일 [!DNL Replication Service]에 의해 구성된 이 [!DNL Replicate.cfg] 파일을 사용하면 [!DNL Insight Server] 시스템에서 [!DNL Repeater] 데이터를 검색하고 로컬에 저장할 수 있습니다. 이 [!DNL Insight Server] 컴퓨터를 대상 기계라고 합니다. 여러 [!DNL Insight Server] DPU를 한 번에 연결하여 여러 데이터 세트에 포함할 이벤트 데이터 사본 [!DNL Repeater] 을 요청할 수 있습니다.

여러 레이어가 있는 네트워크 인프라 [!DNL Replication Service] 에서 방화벽으로 분리된 구성 요소 간에 단일 포트를 단일 포트로 연결하는 통신을 구현할 수 있습니다.

**To install the[!DNL Replication Service]**

설치 [!DNL Replicate.cfg] 시 해당 파일을 설치해야 [!DNL Insight Server] 합니다. 설치 디렉토리의 [!DNL Components] 폴더 내에서 해당 파일을 찾을 수 [!DNL Insight Server] 있습니다. 이 파일이 없으면 Adobe에 문의하십시오.
