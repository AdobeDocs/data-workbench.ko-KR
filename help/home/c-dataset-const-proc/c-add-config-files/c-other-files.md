---
description: 데이터 집합 디렉토리에는 소프트웨어 작업에 필요한 추가 파일 또는 Adobe 구현에 대한 추가 기능이 포함되어 있습니다.
title: 기타 파일
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
exl-id: 0a1fb37c-00ac-46d4-9d0a-904ebd3ccfba
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---

# 기타 파일{#other-files}

데이터 집합 디렉토리에는 소프트웨어 작업에 필요한 추가 파일 또는 Adobe 구현에 대한 추가 기능이 포함되어 있습니다.

* **[!DNL Client.cfg:]** 소프트웨어  [!DNL Client.cfg] 작업을 수행하려면 프로필에 대한 데이터  [!DNL Base] 세트 디렉토리 내의 파일이 필요합니다. [!DNL Client.cfg] 파일에서 매개 변수를 삭제하거나 수정하지 마십시오.

* **[!DNL Cluster.cfg:]** 소프트웨어  [!DNL Cluster.cfg] 작업을 수행하려면 프로필에 대한 데이터  [!DNL Base] 세트 디렉토리 내의 파일이 필요합니다. [!DNL Cluster.cfg] 파일에서 Data Workbench 서버 클러스터에서 처리할 데이터 세트를 구성하는 경우 정규화 서버 매개 변수만 수정해야 합니다. 정규화 서버 매개 변수를 수정하는 방법은 [클러스터에 대한 중앙 정규화 서버 만들기](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md)를 참조하십시오.

* **[!DNL Insight Transform.cfg]및  [!DNL Insight Transform Mode.cfg]:**  변환 기능을 사용하는 경우, 프로필에 대한 데이터 세트 디렉토리에 data workbench  [!DNL Transform.cfg] 및 data workbench [!DNL TransformMode.cfg]라는 두 개의 추가 구성 파일이  [!DNL Transform] 있습니다. 이러한 파일 및 매개 변수에 대한 자세한 내용은 [변환 기능](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html)을 참조하십시오.

* **PAServer.cfg** 파일입니다. Predictive Analytics 클러스터링 작업을 Insight Server에 제출하려면 서버측 클러스터링 제출을 처리하기 위해 [!DNL PAServer.cfg] 파일을 구성해야 합니다.
사용자 지정 프로필은 Predictive Analytics 프로필( [!DNL Server\Profiles\Predictive Analytics\Dataset])에서 [!DNL PAServer.cfg]을 상속해야 합니다.

   >[!IMPORTANT]
   >
   >이 파일에 *기본 Server*&#x200B;를 설정하고 [!DNL PAServer.cfg]를 구현 사이트에 저장합니다.
   >
   >
   ```
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```
