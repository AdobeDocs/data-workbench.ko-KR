---
description: 클러스터를 사용하려면 클러스터에서 하나의 Insight Server를 지정하여 마스터 Insight Server로 행동해야 합니다.
solution: Analytics
title: Insight Server 기본 설치
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# Insight Server 기본 설치{#installing-the-master-insight-server}

클러스터를 사용하려면 클러스터에서 하나의 Insight Server를 지정하여 마스터 Insight Server로 행동해야 합니다.

세션 시작 시 마스터 [!DNL Insight] 또는 [!DNL Report] 연결과 같은 클라이언트 구성 [!DNL Insight Server] 요소입니다. 세션이 진행되는 동안 클라이언트는 클러스터 [!DNL Insight Servers] 의 다른 클라이언트에 연결하여 쿼리를 수행할 수 있습니다. 클라이언트와 클러스터의 다른 연결 [!DNL Insight Servers] 은 마스터에 의해 조정되며 클라이언트에 [!DNL Insight Server] 대해 투명하게 처리됩니다.

클러스터 내 다른 클라이언트와 연결 [!DNL Insight Servers] 을 중개하는 것 외에도, 마스터는 전체 클러스터의 중앙 관리 지점 [!DNL Insight Server] 역할을 합니다. 클러스터를 관리할 때 마스터를 업데이트합니다 [!DNL Insight Server]. 마스터에서 수행하는 관리 변경 사항 [!DNL Insight Server] 은 클러스터의 다른 [!DNL Insight Servers] 사용자에 의해 검색됩니다.

**마스터를 설치하려면[!DNL Insight Server]**

1. 마스터 역할을 할 컴퓨터를 결정합니다 [!DNL Insight Server].
1. Insight [!DNL Insight Server] Server에 설명된 대로 이 컴퓨터에 [!DNL Insight Server] FSU를 설치하고 [구성합니다](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md).
1. 사용자 안내서 [!DNL Insight] 에 설명된 대로 마스터 [!DNL Insight Server] 에 대한 연결을 설치하고 *[!DNL Insight]구성합니다*.
