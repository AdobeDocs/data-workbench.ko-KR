---
description: 대시보드를 시각화하는 각 DPU에는 Query API 라이센스가 있어야 합니다.
title: 쿼리 API 활성화 확인
uuid: deedd1a4-c476-49f6-9278-556d914d2b93
exl-id: 3dde2958-0f99-45f8-b65b-207a92362292
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 5%

---

# 쿼리 API 활성화 확인{#verifying-query-api-enablement}

{{eol}}

대시보드를 시각화하는 각 DPU에는 Query API 라이센스가 있어야 합니다.

다음은 Query API가 설치 및 활성화되어 있는지 확인하는 방법에 대한 몇 가지 지침입니다.

1. Data Workbench 서버의 인증서를 찾습니다.
1. 텍스트 편집기에서 이 인증서를 엽니다.
1. 줄을 확인합니다 `Product = Query API` 가 인증서에 포함되어 있습니다.
1. 에서 **[!UICONTROL Trace]** 폴더를 열고 [!DNL InsightServer64.log] 텍스트 편집기에서 을 참조하십시오.
1. 최신 시작 로그 항목에서 줄을 확인합니다 `Enabling Query API (licensed)` 이 나타납니다.

* 쿼리 API가 활성화되지 않으면 항목이 표시됩니다 `Not enabling Query API (not licensed)`.
* 로그 항목이 표시되지 않거나 쿼리 API가 추가된 후 Data Workbench 서버가 다시 시작되었다고 의심되는 경우 Data Workbench 서버를 다시 시작하고 로그를 확인하십시오.

   Query API가 활성화되어 있는지 확인할 수 없는 경우 ClientCare Adobe에 문의하여 지원을 받으십시오.
