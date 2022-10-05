---
description: 클러스터를 사용하려면 클러스터에서 하나의 Insight Server를 기본 Insight Server로 지정해야 합니다.
title: Insight Server 기본 설치
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
exl-id: 710f1ffe-f620-4920-b4f9-a644cc68d4cc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---

# Insight Server 기본 설치{#installing-the-master-insight-server}

{{eol}}

클러스터를 사용하려면 클러스터에서 하나의 Insight Server를 기본 Insight Server로 지정해야 합니다.

과 같은 클라이언트 구성 요소 [!DNL Insight] 또는 [!DNL Report] 마스터에 연결 [!DNL Insight Server] 세션 시작 시. 세션 중에 클라이언트가 다른 위치에 연결할 수 있습니다 [!DNL Insight Servers] 클러스터에서 쿼리를 수행할 수 있습니다. 클라이언트와 다른 사용자 간의 다음 연결 [!DNL Insight Servers] 클러스터에서 마스터가 중재하고 있습니다 [!DNL Insight Server] 클라이언트에게 투명합니다.

클라이언트와 다른 클라이언트 간의 연결 중개 외에도 [!DNL Insight Servers] 클러스터에서 마스터 [!DNL Insight Server] 전체 클러스터의 중앙 관리 지점으로 사용됩니다. 클러스터를 관리할 때 마스터를 업데이트합니다 [!DNL Insight Server]. 마스터에서 수행하는 관리 변경 사항 [!DNL Insight Server] 다른 방법으로 읽어들입니다 [!DNL Insight Servers] 입니다.

**마스터를 설치하려면[!DNL Insight Server]**

1. 마스터 역할을 할 컴퓨터 결정 [!DNL Insight Server].
1. 설치 및 구성 [!DNL Insight Server] (일반적으로 [!DNL Insight Server] FSU)에 설명되어 있습니다. [Insight Server](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md).
1. 설치 [!DNL Insight] 마스터에 대한 연결 구성 [!DNL Insight Server] 에 설명된 대로 *[!DNL Insight]사용 안내서*.
