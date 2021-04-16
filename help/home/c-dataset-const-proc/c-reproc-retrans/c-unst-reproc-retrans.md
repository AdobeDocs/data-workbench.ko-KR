---
description: 재처리 중에 데이터 워크벤치 서버는 로그 처리 및 변형 데이터 집합 구성 파일에 지정한 대로 데이터 집합을 다시 생성합니다.
title: 재처리 및 재변형 이해
uuid: 0253bc8c-8883-41eb-8a9f-e0685613ff5c
exl-id: 12c69935-a981-492c-9124-71f6f06ff77b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 2%

---

# 재처리 및 재변형 이해{#understanding-reprocessing-and-retransformation}

재처리 중에 데이터 워크벤치 서버는 로그 처리 및 변형 데이터 집합 구성 파일에 지정한 대로 데이터 집합을 다시 생성합니다.

이렇게 하려면 데이터 워크벤치 서버(InsightServer64.exe)가 로그 처리 단계와 데이터 집합 구성의 변형 단계를 모두 완료해야 합니다. 로그 처리가 완료되면 변형이 자동으로 수행되지만 로그 처리와 관계없이 변형이 발생할 수도 있습니다.

로그 처리 단계 중 데이터 워크벤치 사용자는 데이터 세트에 있는 데이터에 액세스할 수 없습니다. 변형 단계 중, 데이터 워크벤치 사용자는 최신 데이터에 액세스할 수 있지만, 데이터가 완전하지 않고 샘플링됩니다. 데이터 분석은 변환 중에도 계속 진행할 수 있지만, 쿼리가 변환이 일어나는 즉시 완료됩니다.

## {#section-92f1e46bf1534b3dba39e9493190b8ab} 재처리

다음 작업 중 하나를 완료할 때마다 데이터 세트 구성 파일에 지정한 대로 데이터 세트를 자동으로 재구성합니다.

* 새 데이터 소스를 추가합니다.
* [!DNL Profile.cfg] 파일의 클러스터에 새 데이터 워크벤치 서버를 추가합니다.
* [!DNL Cluster.cfg] 파일을 변경합니다.
* 다음을 포함하되 이에 제한되지 않는 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 파일을 변경합니다.

   * 새 매개 변수 추가
   * 변형 변경
   * 시작 시간 또는 종료 시간 매개 변수 변경

* [!DNL Insight Server.exe] 파일을 업그레이드합니다.

또한 [!DNL Log Processing.cfg] 파일의 재처리 매개 변수에 문자 또는 문자 조합을 입력하고 파일을 저장하여 언제든지 재처리를 시작할 수 있습니다.

>[!NOTE]
>
>재처리가 수행되려면 [!DNL Log Processing Mode.cfg] 파일의 Pause 매개 변수를 false로 설정해야 합니다. 이 매개 변수의 기본값은 false이므로 매개 변수를 변경할 필요가 없습니다. [!DNL Log Processing Mode.cfg]에 대한 자세한 내용은 [추가 구성 파일](/help/home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md)을 참조하십시오.

## {#section-02446744549940ada8eba0573ec5575f} 다시 변환

변형을 변경하거나 새 차원을 정의하는 등 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일의 정보를 변경할 때마다 변환이 자동으로 수행됩니다.

[!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일([!DNL Categorize], [!DNL FlatFileLookup] 및 [!DNL ODBCLookup] 변형에 대한 조회 파일 포함)에서 참조되는 조회 파일을 변경할 때마다 [!DNL Transformation.cfg] 파일의 Reprocess 매개 변수에 문자 또는 문자 조합을 입력하고 파일을 저장하여 변환을 시작해야 합니다.
