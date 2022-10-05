---
description: 데이터 집합 디렉토리에는 소프트웨어 작업에 필요한 추가 파일 또는 Adobe 구현에 대한 추가 기능이 포함되어 있습니다.
title: 기타 파일
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
exl-id: 0a1fb37c-00ac-46d4-9d0a-904ebd3ccfba
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 1%

---

# 기타 파일{#other-files}

{{eol}}

데이터 집합 디렉토리에는 소프트웨어 작업에 필요한 추가 파일 또는 Adobe 구현에 대한 추가 기능이 포함되어 있습니다.

* **[!DNL Client.cfg:]** 다음 [!DNL Client.cfg] 파일의 데이터 세트 디렉토리 [!DNL Base] 소프트웨어 작동에는 프로필이 필요합니다. 에서 매개 변수를 삭제하거나 수정하지 마십시오 [!DNL Client.cfg] 파일.

* **[!DNL Cluster.cfg:]** 다음 [!DNL Cluster.cfg] 파일의 데이터 세트 디렉토리 [!DNL Base] 소프트웨어 작동에는 프로필이 필요합니다. 에서 [!DNL Cluster.cfg] 파일에서, data workbench 서버 클러스터에서 처리할 데이터 세트를 구성하는 경우 정규화 서버 매개 변수만 수정해야 합니다. 정규화 서버 매개 변수를 수정하는 방법은 [클러스터의 중앙 표준화 서버 생성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]및 [!DNL Insight Transform Mode.cfg]:** 변환 기능을 사용하는 경우, Data Workbench라는 두 개의 추가 구성 파일이 있습니다 [!DNL Transform.cfg] 및 data workbench [!DNL TransformMode.cfg]를 채울 수 있습니다 [!DNL Transform] 프로필 참조. 이러한 파일 및 매개 변수에 대한 자세한 내용은 [변형 기능](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

* 다음 **PAServer.cfg** 파일. Predictive Analytics 클러스터링 작업을 Insight Server에 제출하려면 다음을 구성해야 합니다 [!DNL PAServer.cfg] 서버측 클러스터링 제출을 처리하기 위한 파일입니다.
사용자 지정 프로필은 [!DNL PAServer.cfg] 예측 분석 프로필( [!DNL Server\Profiles\Predictive Analytics\Dataset]).

   >[!IMPORTANT]
   >
   >설정 *기본 서버* 이 파일에서 [!DNL PAServer.cfg] 를 구현 사이트에 추가합니다.
   >
   >
   ```
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```
