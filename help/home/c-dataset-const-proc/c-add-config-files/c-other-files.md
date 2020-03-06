---
description: Dataset 디렉토리에는 소프트웨어 작업에 필요하거나 Adobe 구현을 위해 추가 기능을 제공하는 추가 파일이 포함되어 있습니다.
solution: Analytics
title: 기타 파일
topic: Data workbench
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 기타 파일{#other-files}

Dataset 디렉토리에는 소프트웨어 작업에 필요하거나 Adobe 구현을 위해 추가 기능을 제공하는 추가 파일이 포함되어 있습니다.

* **[!DNL Client.cfg:]** 소프트웨어를 작동하려면 [!DNL Client.cfg] 프로필의 데이터 집합 디렉터리 내의 [!DNL Base] 파일이 필요합니다. 파일의 매개 변수를 삭제하거나 수정하지 마십시오. [!DNL Client.cfg]

* **[!DNL Cluster.cfg:]** 소프트웨어를 작동하려면 [!DNL Cluster.cfg] 프로필의 데이터 집합 디렉터리 내의 [!DNL Base] 파일이 필요합니다. 데이터 워크벤치 서버 클러스터에서 처리할 데이터 세트를 구성하는 경우 [!DNL Cluster.cfg] 파일에서 Normalize Server 매개 변수만 수정해야 합니다. Normalize Server 매개 변수를 수정하는 방법은 클러스터에 [대한 중앙 표준화 서버 만들기를 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]및[!DNL Insight Transform Mode.cfg]**변환 기능을 사용하는 경우, 데이터 워크벤치[!DNL Transform.cfg]및 데이터 워크벤치 두 개의 추가 구성 파일이 해당[!DNL TransformMode.cfg][!DNL Transform]프로필의 데이터 세트 디렉토리에 있습니다. 이러한 파일 및 매개 변수에 대한 자세한 내용은 변형[기능을 참조하십시오](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

* PAServer **.cfg** 파일. Insight 서버에 Predictive Analytics 클러스터링 작업을 제출하려면 서버측 클러스터링 제출 처리를 위해 [!DNL PAServer.cfg] 파일을 구성해야 합니다.
사용자 지정 프로필은 예측 분석 프로필 [!DNL PAServer.cfg] [!DNL Server\Profiles\Predictive Analytics\Dataset]()에서 상속해야 합니다.

   >[!IMPORTANT]
   >
   >이 *파일에서 마스터* 서버를 설정하고 을 구현 [!DNL PAServer.cfg] 사이트에 저장합니다.  >
   >
   >
   ```>
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```  >
   >



