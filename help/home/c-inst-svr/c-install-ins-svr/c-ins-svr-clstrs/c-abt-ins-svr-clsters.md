---
description: Insight Server 및 보고서 사용자가 처리하고 액세스할 수 있는 데이터 양이 단일 Insight Server의 용량을 초과하는 경우 Insight Server 클러스터가 필요합니다.
title: Insight Server 클러스터 정보
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
exl-id: b26e0f63-76db-461d-91e7-0968624aa0f7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 2%

---

# Insight Server 클러스터 정보{#about-insight-server-clusters}

{{eol}}

Insight Server 및 보고서 사용자가 처리하고 액세스할 수 있는 데이터 양이 단일 Insight Server의 용량을 초과하는 경우 Insight Server 클러스터가 필요합니다.

다음을 설정하여 [!DNL Insight Server] 클러스터를 사용하면 클러스터의 여러 시스템에 단일 분석 데이터 세트를 배포하여 여러 시스템의 처리 능력을 활용할 수 있습니다 [!DNL Insight Servers].

를 구현하는 첫 번째 단계입니다 [!DNL Insight Server] 클러스터는 [!DNL Insight Server] 클러스터의 컴퓨터. 첫 번째 [!DNL Insight Server] 설정한 시스템이 마스터 [!DNL Insight Server] (경우에 따라 기본 [!DNL Insight Server]).

>[!NOTE]
>
>를 사용하는 경우 [!DNL Insight Server] 파일 서버 유닛(FSU), Adobe은 FSU를 마스터로 구성하는 것을 권장합니다 [!DNL Insight Server]. FSU 구성에 대한 자세한 내용은 *데이터 집합 구성 안내서*.

마스터 [!DNL Insight Server] 다른 사람 간의 통신을 관리합니다 [!DNL Insight Servers] 클러스터(처리 서버라고 함) 및 [!DNL Insight] 및 [!DNL Report]. 지정된 데이터 세트에 대해 지정된(하나 이상)에서 로그 파일 처리가 수행됩니다 [!DNL Insight Servers] (마스터 또는 처리)에 지정된 대로 [!DNL Insight Server] 구성 파일. 클러스터 환경에서 작업할 경우 [!DNL Insight] 설치는 마스터에 액세스할 수 있도록 구성됩니다 [!DNL Insight Server]하지만 쿼리는 모든 [!DNL Insight Servers] 클러스터 내에서 지원됩니다.

>[!NOTE]
>
>다음 **PAServer.cfg** 파일. Predictive Analytics 클러스터링 작업을 Insight Server에 제출하려면 다음을 구성해야 합니다 [!DNL PAServer.cfg] 서버측 클러스터링 제출을 처리하기 위한 파일입니다. 사용자 지정 프로필은 [!DNL PAServer.cfg] 예측 분석 프로필([!DNL Server\Profiles\Predictive Analytics\Dataset]). 설정 *기본 서버* 이 파일에서 [!DNL PAServer.cfg] 를 구현 사이트에 추가합니다.
>
>
```
>PAServer = PAServerConfig: 
>   Master Server = serverInfo: 
>       Address = string: 
>       Port = int: 80
>       Use SSL = bool: false
>```

>[!IMPORTANT]
>
>이 장의 지침은 [!DNL Insight Server] 5개 이상으로 구성된 클러스터 [!DNL Insight Servers]. 5개 이상의 클러스터에 대한 시스템 요구 사항과 프로필 구성 권장 사항을 얻으려면 Adobe에 문의하십시오 [!DNL Insight Servers].
