---
description: Insight 서버 클러스터는 처리하려는 데이터의 양과 Insight 및 Report 사용자가 액세스할 수 있는 데이터가 단일 Insight Server의 용량을 초과하는 경우에 필요합니다.
solution: Insight
title: Insight Server 클러스터 정보
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
translation-type: tm+mt
source-git-commit: 2c1b2adfe8bf479c2a8cbd150ed006be2336022c
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Insight Server 클러스터 정보{#about-insight-server-clusters}

Insight 서버 클러스터는 처리하려는 데이터의 양과 Insight 및 Report 사용자가 액세스할 수 있는 데이터가 단일 Insight Server의 용량을 초과하는 경우에 필요합니다.

클러스터를 설정하여 한 [!DNL Insight Server] 클러스터의 여러 컴퓨터에 단일 분석 데이터 세트를 배포하여 여러 시스템의 처리 능력을 활용할 수 있습니다 [!DNL Insight Servers].

클러스터 구현의 첫 번째 단계는 [!DNL Insight Server] 클러스터의 [!DNL Insight Server] 컴퓨터를 할당하는 것입니다. 설정한 첫 번째 [!DNL Insight Server] 컴퓨터는 마스터 [!DNL Insight Server] (경우에 따라 기본 컴퓨터라고도 함)입니다 [!DNL Insight Server].

>[!NOTE]
>
>FSU( [!DNL Insight Server] 파일 서버 장치)를 사용하는 경우 FSU를 마스터로 구성하는 것이 좋습니다 [!DNL Insight Server]. FSU 구성에 대한 자세한 내용은 데이터 세트 *구성 안내서를 참조하십시오*.

마스터는 클러스터 내 [!DNL Insight Server] 의 다른 것(처리 서버라고도 함, 쿼리 서버라고도 함)과 [!DNL Insight Servers] 및 [!DNL Insight] [!DNL Report]인스턴스 간의 통신을 관리합니다. 지정된 데이터 세트에 대해 로그 파일 처리가 구성 파일에 지정된 하나 이상의 지정된 [!DNL Insight Servers] (마스터 또는 처리)에서 [!DNL Insight Server] 발생합니다. 클러스터 환경에서 작업할 때 설치 [!DNL Insight] 는 마스터에 액세스하도록 구성되지만 클러스터 내 [!DNL Insight Server]에서 쿼리를 처리할 수 [!DNL Insight Servers] 있습니다.

>[!NOTE]
>
>PAServer.cfg **** 파일. 예측 Analytics 클러스터링 작업을 Insight 서버에 제출하려면 서버측 클러스터링 제출 처리를 위해 [!DNL PAServer.cfg] 파일을 구성해야 합니다. 사용자 지정 프로필은 예측 Analytics 프로필 [!DNL PAServer.cfg] ([!DNL Server\Profiles\Predictive Analytics\Dataset])에서 상속해야 합니다. 이 파일에서 *서버기본을* 설정하고 [!DNL PAServer.cfg] 를 구현 사이트에 저장합니다.
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
>이 장의 지침은 5개 이상으로 구성된 [!DNL Insight Server] 클러스터를 만드는 경우에는 적용되지 않습니다 [!DNL Insight Servers]. 5개 이상의 클러스터에 대한 시스템 요구 사항과 프로필 구성 권장 사항을 얻으려면 Adobe에 문의하십시오 [!DNL Insight Servers].
