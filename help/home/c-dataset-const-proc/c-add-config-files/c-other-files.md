---
description: Dataset 디렉토리에는 소프트웨어 작업에 필요하거나 Adobe 구현을 위한 추가 기능을 제공하는 추가 파일이 포함되어 있습니다.
solution: Analytics
title: 기타 파일
topic: Data workbench
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
translation-type: tm+mt
source-git-commit: 98452ba81d71db65c75e3d07712eefa18c003f53
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# 기타 파일{#other-files}

Dataset 디렉토리에는 소프트웨어 작업에 필요하거나 Adobe 구현을 위한 추가 기능을 제공하는 추가 파일이 포함되어 있습니다.

* **[!DNL Client.cfg:]** 소프트웨어 [!DNL Client.cfg] 작업을 수행하려면 프로필의 데이터 세트 디렉터리 [!DNL Base] 내의 파일이 필요합니다. 파일의 매개 변수를 삭제하거나 수정하지 [!DNL Client.cfg] 마십시오.

* **[!DNL Cluster.cfg:]** 소프트웨어 [!DNL Cluster.cfg] 작업을 수행하려면 프로필의 데이터 세트 디렉터리 [!DNL Base] 내의 파일이 필요합니다. 데이터 워크벤치 서버 클러스터에서 처리할 데이터 세트를 구성하는 경우 [!DNL Cluster.cfg] 파일에서 표준화 서버 매개 변수만 수정해야 합니다. 표준화 서버 매개 변수 수정에 대한 지침은 클러스터의 [중앙 표준화 서버 만들기를 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]및[!DNL Insight Transform Mode.cfg]** 변형 기능을 사용하는 경우, 데이터 워크벤치 [!DNL Transform.cfg] 와 데이터 워크벤치 [!DNL TransformMode.cfg]라는 두 개의 추가 구성 파일이 [!DNL Transform] 프로필의 데이터 세트 디렉터리에 있습니다. 이러한 파일 및 매개 변수에 대한 자세한 내용은 [변형 기능을 참조하십시오](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

* PAServer.cfg **** 파일. Insight 서버에 Predictive Analytics 클러스터링 작업을 제출하려면 서버측 클러스터링 제출 처리를 위해 [!DNL PAServer.cfg] 파일을 구성해야 합니다.
사용자 지정 프로필은 예측 분석 프로필 [!DNL PAServer.cfg] [!DNL Server\Profiles\Predictive Analytics\Dataset]()에서 상속해야 합니다.

   >[!IMPORTANT]
   >
   >이 파일에서 *서버기본을* 설정하고 [!DNL PAServer.cfg] 를 구현 사이트에 저장합니다.
   >
   >
   ```
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```

