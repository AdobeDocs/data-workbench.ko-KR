---
description: 데이터 워크벤치에서는 데이터 워크벤치 서버가 조회 데이터를 데이터 세트에 통합할 수 있도록 해주는 변형 세트를 제공합니다.
solution: Analytics
title: 조회 데이터 통합
topic: Data workbench
uuid: 35fd48f7-c0c4-4a83-919d-c15902f27495
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 조회 데이터 통합{#integrating-lookup-data}

데이터 워크벤치에서는 데이터 워크벤치 서버가 조회 데이터를 데이터 세트에 통합할 수 있도록 해주는 변형 세트를 제공합니다.

조회 데이터는 데이터 세트를 만들기 위해 이벤트 데이터와 결합할 수 있는 기업 데이터베이스 또는 조회 파일의 외부 데이터입니다. 일반적으로 조회 데이터를 사용하여 로그 소스에서 이벤트 데이터를 증가시킵니다. 개념적으로, 조회 데이터를 사용하여 이벤트 데이터 레코드를 추가 정보 열로 채울 수 있습니다.

조회 데이터를 사용하는 경우 데이터를 메모리 상주 조회 테이블로 로드합니다. 테이블의 열에는 이벤트 데이터 레코드에도 존재하는 공통 키가 있어야 합니다. 조회 테이블 자체에 있는 데이터는 플랫 파일 또는 ODBC 데이터 소스에서 로드할 수 있습니다. 데이터 집합 구성 프로세스의 로그 처리 또는 변형 단계에서 조회 데이터를 데이터 집합에 통합할 수 있습니다.

조회 데이터를 통합하려면 먼저 조회 파일을 생성하거나 SQL 데이터베이스에 액세스하는 데 필요한 정보를 가지고 있어야 합니다. 그런 다음 로그 처리 및 변환을 위해 데이터 세트 구성 파일에서 다음 변형 중 하나 이상을 정의해야 합니다.

**조회 데이터를 데이터 세트에 통합하려면**

1. 조회 파일을 생성합니다. 조회 [테이블 채우기를 참조하십시오](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-pop-lookup-table.md#concept-dd761338731a40e0997c33dfdabdcdf8).
1. 적절한 데이터 세트 구성 파일의 변형 매개 변수에서 다음 변형 유형 중 하나를 정의합니다.

   * [!DNL Categorize]
   * [!DNL FlatFileLookup]
   * [!DNL ODBCLookup]

>[!NOTE]
>
>변환은 [!DNL ODBCLookup] 파일 또는 [!DNL Transformation.cfg] [!DNL Transformation Dataset Include] 파일에서 정의된 경우에만 작동합니다.

