---
description: 클러스터를 사용하려면 클러스터에서 하나의 Insight 서버를 마스터 Insight 서버로 지정해야 합니다.
title: Insight Server 기본 설치
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
exl-id: 710f1ffe-f620-4920-b4f9-a644cc68d4cc
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---

# Insight Server 기본 설치{#installing-the-master-insight-server}

클러스터를 사용하려면 클러스터에서 하나의 Insight 서버를 마스터 Insight 서버로 지정해야 합니다.

[!DNL Insight] 또는 [!DNL Report] 같은 클라이언트 구성 요소는 세션을 시작할 때 마스터 [!DNL Insight Server]에 연결됩니다. 세션이 진행되는 동안 클라이언트는 클러스터의 다른 [!DNL Insight Servers]에 연결하여 쿼리를 수행할 수 있습니다. 클라이언트와 클러스터에 있는 다른 [!DNL Insight Servers] 간의 후속 연결은 마스터 [!DNL Insight Server]에 의해 중재되며 클라이언트에 투명하게 표시됩니다.

클라이언트와 클러스터의 다른 [!DNL Insight Servers] 간의 연결 중개 외에도 마스터 [!DNL Insight Server]은 전체 클러스터의 중앙 관리 지점 역할을 합니다. 클러스터를 관리할 때 마스터 [!DNL Insight Server]을 업데이트합니다. 마스터 [!DNL Insight Server]에서 수행한 관리 변경 사항은 클러스터의 다른 [!DNL Insight Servers]에 의해 검색됩니다.

**마스터를 설치하려면[!DNL Insight Server]**

1. 마스터 [!DNL Insight Server] 역할을 할 컴퓨터를 결정합니다.
1. [Insight Server](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md)에 설명된 대로 이 컴퓨터에 [!DNL Insight Server](일반적으로 [!DNL Insight Server] FSU)을 설치하고 구성합니다.
1. [!DNL Insight]을(를) 설치하고 *[!DNL Insight]사용 안내서*&#x200B;에 설명된 대로 마스터 [!DNL Insight Server]에 대한 연결을 구성합니다.
