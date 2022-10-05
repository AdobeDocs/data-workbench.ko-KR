---
description: 재처리 중에 Data Workbench 서버는 로그 처리 및 변형 데이터 세트 구성 파일에 지정한 대로 데이터 세트를 다시 구성합니다.
title: 재처리 및 재변형 이해
uuid: 0253bc8c-8883-41eb-8a9f-e0685613ff5c
exl-id: 12c69935-a981-492c-9124-71f6f06ff77b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 2%

---

# 재처리 및 재변형 이해{#understanding-reprocessing-and-retransformation}

{{eol}}

재처리 중에 Data Workbench 서버는 로그 처리 및 변형 데이터 세트 구성 파일에 지정한 대로 데이터 세트를 다시 구성합니다.

이렇게 하려면 Data Workbench 서버(InsightServer64.exe)에서 로그 처리 단계와 데이터 집합 구성의 변환 단계를 모두 완료해야 합니다. 로그 처리가 완료되면 변환을 자동으로 트리거하지만 변환은 로그 처리와는 별도로 발생할 수도 있습니다.

로그 처리 단계 동안 Data Workbench 사용자는 데이터 집합에 있는 데이터에 액세스할 수 없습니다. 변환 단계 동안 Data Workbench 사용자는 최신 데이터에 액세스할 수 있지만 데이터가 완료되지 않고 샘플링됩니다. 데이터 분석은 변환 중에 계속 진행될 수 있지만, 쿼리는 변환이 일어나는 한 빨리 완료됩니다.

## 재처리 {#section-92f1e46bf1534b3dba39e9493190b8ab}

다음 작업 중 하나를 완료할 때마다 로그 처리 및 변환이 데이터 집합 구성 파일에 지정한 대로 데이터 집합을 자동으로 재구성합니다.

* 새 데이터 소스를 추가합니다.
* 새 Data Workbench 서버를 [!DNL Profile.cfg] 파일.
* 변경 [!DNL Cluster.cfg] 파일.
* 변경 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 다음을 포함하되 이에 국한되지 않는 파일:

   * 새 매개 변수 추가
   * 변형 변경
   * 시작 시간 또는 종료 시간 매개 변수 변경

* 업그레이드 [!DNL Insight Server.exe] 파일.

페이지의 Reprocess 매개 변수에 문자 또는 문자 조합을 입력하여 언제든지 재처리를 시작할 수도 있습니다 [!DNL Log Processing.cfg] 파일을 저장하고 파일을 저장합니다.

>[!NOTE]
>
>재처리가 수행되도록 하려면 [!DNL Log Processing Mode.cfg] 파일을 false로 설정해야 합니다. 이 매개 변수의 기본값은 false이므로 매개 변수를 변경할 필요가 없습니다. 에 대한 자세한 정보 [!DNL Log Processing Mode.cfg]를 참조하십시오. [추가 구성 파일](/help/home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md).

## 재변형 {#section-02446744549940ada8eba0573ec5575f}

매번 정보를 변경할 때마다 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 변형 변경 또는 새 차원 정의 등의 파일은 자동으로 변형됩니다.

에서 참조되는 조회 파일을 변경할 때마다 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일(조회 파일 포함) [!DNL Categorize], [!DNL FlatFileLookup], 및 [!DNL ODBCLookup] 변환)의 Reprocess 매개 변수에 문자 또는 문자 조합을 입력하여 변환을 시작해야 합니다 [!DNL Transformation.cfg] 파일을 저장하고 파일을 저장합니다.
