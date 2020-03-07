---
description: 클러스터를 사용하려면 클러스터에서 하나의 Insight 서버를 지정하여 마스터 Insight Server로 행동해야 합니다.
solution: Insight
title: Master Insight Server 설치
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Master Insight Server 설치{#installing-the-master-insight-server}

클러스터를 사용하려면 클러스터에서 하나의 Insight 서버를 지정하여 마스터 Insight Server로 행동해야 합니다.

세션 시작 시 마스터 [!DNL Insight] 또는 [!DNL Report] 연결과 같은 클라이언트 구성 요소입니다 [!DNL Insight Server] . 세션이 진행되는 동안 클라이언트는 클러스터 [!DNL Insight Servers] 내의 다른 클라이언트에 연결하여 쿼리를 수행할 수 있습니다. 클라이언트와 클러스터의 다른 [!DNL Insight Servers] 연결 상태는 마스터에 의해 조정되며 클라이언트에 [!DNL Insight Server] 대해 투명합니다.

클러스터에서 클라이언트와 다른 클라이언트 간의 연결을 중개하는 것 외에도 마스터는 전체 클러스터의 중앙 관리 지점 역할을 [!DNL Insight Servers] [!DNL Insight Server] 합니다. 클러스터를 관리할 때 마스터를 업데이트합니다 [!DNL Insight Server]. 마스터에서 수행한 관리 변경 [!DNL Insight Server] 사항은 클러스터의 다른 [!DNL Insight Servers] 사용자가 읽어들입니다.

**마스터를 설치하려면[!DNL Insight Server]**

1. 마스터 역할을 할 컴퓨터를 [!DNL Insight Server]결정합니다.
1. Insight Server에 설명된 [!DNL Insight Server] 대로 이 컴퓨터에 [!DNL Insight Server] FSU를 설치하고 [구성합니다](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md).
1. 사용자 안내서에 설명된 [!DNL Insight] 대로 마스터 연결을 설치하고 [!DNL Insight Server] 구성합니다 *[!DNL Insight]*.
