---
description: Insight ServerReplication Service를 사용하면 한 Insight Server 컴퓨터에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.
solution: Insight
title: 복제 서비스 설치
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 복제 서비스 설치{#installing-the-replication-service}

Insight ServerReplication Service를 사용하면 한 Insight Server 컴퓨터에 수집되고 저장된 이벤트 데이터를 다른 Insight Server 시스템으로 전송할 수 있습니다.

일반적으로 데이터가 수집되고 저장되는 시스템은 [!DNL Repeater] 컴퓨터로 실행되도록 구성됩니다. 반복 [기능을 참조하십시오](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). 이 [!DNL Replication Service]파일을 통해 구성된 [!DNL Replicate.cfg] 파일을 사용하면 [!DNL Insight Server] [!DNL Repeater] 컴퓨터에서 데이터를 검색하여 로컬에 저장할 수 있습니다. 이 [!DNL Insight Server] 시스템을 대상 시스템이라고 합니다. 여러 [!DNL Insight Server] DPU를 한 DPU에 연결하여 여러 데이터 세트에 포함할 수 있도록 이벤트 데이터의 복사본을 요청할 [!DNL Repeater] 수 있습니다.

방화벽이 여러 레이어로 구성된 네트워크 [!DNL Replication Service] 인프라에서 이 기능을 사용하여 방화벽으로 분리된 구성 요소 간에 단일 포트-단일 포트 통신을 수행할 수 있습니다.

**To install the[!DNL Replication Service]**

이 [!DNL Replicate.cfg] 파일은 [!DNL Insight Server] 설치의 일부로 설치해야 합니다. 설치 디렉토리의 [!DNL Components] 폴더 내에서 해당 파일을 찾을 수 [!DNL Insight Server] 있습니다. 이 파일이 없는 경우 Adobe에 문의하십시오.
