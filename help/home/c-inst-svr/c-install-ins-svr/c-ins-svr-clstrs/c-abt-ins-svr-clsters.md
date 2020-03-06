---
description: Insight Server 클러스터는 Insight 및 Report 사용자가 처리하고 액세스할 수 있는 데이터 양이 단일 Insight Server의 용량을 초과하는 경우에 필요합니다.
solution: Insight
title: Insight Server 클러스터 정보
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Insight Server 클러스터 정보{#about-insight-server-clusters}

Insight Server 클러스터는 Insight 및 Report 사용자가 처리하고 액세스할 수 있는 데이터 양이 단일 Insight Server의 용량을 초과하는 경우에 필요합니다.

클러스터를 설정하면 [!DNL Insight Server] 클러스터의 여러 시스템에 단일 분석 데이터 세트를 배포하여 여러 시스템의 처리 능력을 활용할 수 [!DNL Insight Servers]있습니다.

클러스터 구현의 첫 번째 단계는 [!DNL Insight Server] 클러스터의 [!DNL Insight Server] 시스템을 할당하는 것입니다. 첫 번째 [!DNL Insight Server] 컴퓨터가 마스터 [!DNL Insight Server] (기본 시스템이라고도 함)입니다 [!DNL Insight Server].

>[!NOTE]
>
>FSU(File Server [!DNL Insight Server] Unit)를 사용하는 경우 FSU를 마스터로 구성하는 것이 좋습니다 [!DNL Insight Server]. FSU 구성에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.

마스터는 클러스터의 다른 서버(처리 서버라고도 함, 쿼리 서버라고도 함)와 [!DNL Insight Server] 및 [!DNL Insight Servers] 인스턴스 간의 통신을 [!DNL Insight] [!DNL Report]관리합니다. 지정된 데이터 집합의 경우 로그 파일 처리가 구성 파일에 지정된 하나 이상의 지정된 [!DNL Insight Servers] (마스터 또는 처리)에서 [!DNL Insight Server] 수행됩니다. 클러스터 환경에서 작업할 때 [!DNL Insight] 설치는 마스터에 액세스할 수 있도록 구성되지만 [!DNL Insight Server]클러스터 [!DNL Insight Servers] 내 모든 서버에서 쿼리를 처리할 수 있습니다.

>[!NOTE]
>
>PAServer **.cfg** 파일. Insight 서버에 Predictive Analytics 클러스터링 작업을 제출하려면 서버측 클러스터링 제출 처리를 위해 [!DNL PAServer.cfg] 파일을 구성해야 합니다. 사용자 지정 프로필은 예측 분석 프로필 [!DNL PAServer.cfg] [!DNL Server\Profiles\Predictive Analytics\Dataset]()에서 상속해야 합니다. 이 *파일에서 마스터* 서버를 설정하고 을 구현 [!DNL PAServer.cfg] 사이트에 저장합니다.>
>
```>
>PAServer = PAServerConfig: 
>   Master Server = serverInfo: 
>       Address = string: 
>       Port = int: 80
>       Use SSL = bool: false
>```>



>[!IMPORTANT]
>
>이 장의 지침은 5개 이상으로 구성된 [!DNL Insight Server] 클러스터를 만드는 경우에는 적용되지 않습니다 [!DNL Insight Servers]. 5개 이상의 클러스터에 대한 시스템 요구 사항과 프로필 구성 권장 사항을 얻으려면 Adobe에 문의하십시오 [!DNL Insight Servers].

