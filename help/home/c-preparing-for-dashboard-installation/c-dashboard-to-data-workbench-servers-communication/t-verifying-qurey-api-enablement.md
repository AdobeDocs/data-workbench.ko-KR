---
description: 대시보드를 시각화하는 각 DPU에는 쿼리 API 라이선스가 있어야 합니다.
solution: Analytics
title: 쿼리 API 활성화 확인
topic: Data workbench
uuid: deedd1a4-c476-49f6-9278-556d914d2b93
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 쿼리 API 활성화 확인{#verifying-query-api-enablement}

대시보드를 시각화하는 각 DPU에는 쿼리 API 라이선스가 있어야 합니다.

다음은 쿼리 API가 설치 및 활성화되었는지 확인하는 방법에 대한 몇 가지 지침입니다.

1. 데이터 워크벤치 서버의 인증서를 찾습니다.
1. 텍스트 편집기에서 이 인증서를 엽니다.
1. 인증서에 줄이 `Product = Query API` 있는지 확인합니다.
1. 폴더에서 텍스트 편집기에서 **[!UICONTROL Trace]** [!DNL InsightServer64.log] 을 엽니다.
1. 최신 시작 로그 항목에서 줄이 `Enabling Query API (licensed)` 나타나는지 확인합니다.

* 쿼리 API가 활성화되지 않으면 항목이 `Not enabling Query API (not licensed)`표시됩니다.
* 로그 항목이 없거나 쿼리 API가 추가된 후 데이터 워크벤치 서버가 다시 시작되었다고 생각되는 경우 데이터 워크벤치 서버를 다시 시작하고 로그를 확인하십시오.

   쿼리 API가 활성화되어 있는지 확인할 수 없는 경우 Adobe ClientCare에 지원을 문의하십시오.
