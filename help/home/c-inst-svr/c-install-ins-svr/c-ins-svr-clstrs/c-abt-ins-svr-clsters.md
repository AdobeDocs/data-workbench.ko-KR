---
description: Insight Server 클러스터는 처리하려는 데이터의 양과 Insight 및 Report 사용자가 액세스할 수 있는 액세스 권한이 단일 Insight Server의 용량을 초과하는 경우에 필요합니다.
title: Insight Server 클러스터 정보
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
exl-id: b26e0f63-76db-461d-91e7-0968624aa0f7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 2%

---

# Insight Server 클러스터 정보{#about-insight-server-clusters}

Insight Server 클러스터는 처리하려는 데이터의 양과 Insight 및 Report 사용자가 액세스할 수 있는 액세스 권한이 단일 Insight Server의 용량을 초과하는 경우에 필요합니다.

[!DNL Insight Server] 클러스터를 설정하면 한 클러스터의 여러 컴퓨터에 단일 분석 데이터 세트를 배포하여 여러 [!DNL Insight Servers]의 처리 능력을 활용할 수 있습니다.

[!DNL Insight Server] 클러스터 구현의 첫 번째 단계는 클러스터에 [!DNL Insight Server] 컴퓨터를 할당하는 것입니다. 설정한 첫 번째 [!DNL Insight Server] 컴퓨터는 마스터 [!DNL Insight Server](기본 [!DNL Insight Server]라고도 함)입니다.

>[!NOTE]
>
>[!DNL Insight Server] FSU(파일 서버 장치)를 사용하는 경우 FSU를 마스터 [!DNL Insight Server]으로 구성하는 것이 좋습니다. FSU 구성에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

마스터 [!DNL Insight Server]은(는) 클러스터의 다른 [!DNL Insight Servers](처리 서버라고도 함 또는 쿼리 서버라고도 함)과 [!DNL Insight] 및 [!DNL Report]의 인스턴스 간 통신을 관리합니다. 지정된 데이터 집합의 경우 로그 파일 처리가 [!DNL Insight Server] 구성 파일에 지정된 하나 이상의 [!DNL Insight Servers](마스터 또는 처리)에서 수행됩니다. 클러스터 환경에서 작업할 때 [!DNL Insight] 설치가 마스터 [!DNL Insight Server]에 액세스하도록 구성되지만 클러스터 내의 [!DNL Insight Servers]에 의해 쿼리를 처리할 수 있습니다.

>[!NOTE]
>
>**PAServer.cfg** 파일. Insight 서버에 Predictive Analytics 클러스터링 작업을 제출하려면 서버측 클러스터링 제출 처리를 위해 [!DNL PAServer.cfg] 파일을 구성해야 합니다. 사용자 지정 프로필은 예측 분석 프로필([!DNL Server\Profiles\Predictive Analytics\Dataset])에서 [!DNL PAServer.cfg]을 상속해야 합니다. 이 파일에서 *기본 Server*&#x200B;을 설정하고 [!DNL PAServer.cfg]를 구현 사이트에 저장합니다.
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
>이 장의 지침은 5(5) [!DNL Insight Servers] 이상으로 구성된 [!DNL Insight Server] 클러스터 만들기에 적용되지 않습니다. 5 [!DNL Insight Servers]보다 큰 클러스터의 시스템 요구 사항과 프로필 구성 권장 사항을 얻으려면 Adobe에 문의하십시오.
