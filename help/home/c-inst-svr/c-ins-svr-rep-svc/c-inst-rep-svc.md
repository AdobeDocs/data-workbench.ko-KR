---
description: Insight Server 복제 서비스를 사용하면 한 Insight Server 시스템에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.
title: 복제 서비스 설치
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
exl-id: a235fe75-a6d0-4c20-8ea2-8b1cbad12da7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---

# 복제 서비스 설치{#installing-the-replication-service}

{{eol}}

Insight Server 복제 서비스를 사용하면 한 Insight Server 시스템에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.

일반적으로 데이터가 수집되고 저장되는 시스템은 [!DNL Repeater] 시스템. 자세한 내용은 [반복 기능](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). 다음 [!DNL Replication Service]: [!DNL Replicate.cfg] 파일, 사용 [!DNL Insight Server] 시스템에서 데이터를 검색합니다. [!DNL Repeater] 로컬에 머시닝하여 저장합니다. 다음 [!DNL Insight Server] 시스템을 타겟 머신이라고 합니다. 다중 [!DNL Insight Server] DPU는 단일 [!DNL Repeater] 여러 데이터 세트에 포함할 이벤트 데이터의 사본을 요청하려면

를 사용할 수 있습니다 [!DNL Replication Service] 방화벽의 여러 계층이 있는 네트워크 인프라에서 방화벽에 의해 분리된 구성 요소 간에 단일 포트-단일 포트 통신을 수행할 수 있습니다.

**를 설치하려면[!DNL Replication Service]**

다음 [!DNL Replicate.cfg] 파일은 [!DNL Insight Server] 설치. 에서 파일을 찾을 수 있습니다 [!DNL Components] 폴더 [!DNL Insight Server] 설치 디렉토리. 이 파일이 없는 경우 Adobe에 문의하십시오.
