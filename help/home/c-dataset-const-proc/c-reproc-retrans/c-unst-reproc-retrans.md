---
description: 재처리 중에 데이터 워크벤치 서버는 로그 처리 및 변형 데이터 세트 구성 파일에 지정한 대로 데이터 세트를 재구성합니다.
solution: Analytics
title: 재처리 및 재변형 이해
topic: Data workbench
uuid: 0253bc8c-8883-41eb-8a9f-e0685613ff5c
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 재처리 및 재변형 이해{#understanding-reprocessing-and-retransformation}

재처리 중에 데이터 워크벤치 서버는 로그 처리 및 변형 데이터 세트 구성 파일에 지정한 대로 데이터 세트를 재구성합니다.

이렇게 하려면 데이터 워크벤치 서버(InsightServer64.exe)가 로그 처리 단계와 데이터 세트 구성의 변환 단계를 모두 완료해야 합니다. 로그 처리가 완료되면 변환이 자동으로 수행되지만, 변환은 로그 처리와는 별도로 발생할 수도 있습니다.

로그 처리 단계 동안 데이터 워크벤치 사용자는 데이터 세트에 있는 데이터에 액세스할 수 없습니다. 변환 단계 동안 데이터 워크벤치 사용자는 최신 데이터에 액세스할 수 있지만 데이터가 완전하지 않고 샘플링됩니다. 데이터 분석은 변환 중에 계속 진행할 수 있지만, 쿼리는 전환이 이루어지는 한 빨리 완료됩니다.

## 재처리 {#section-92f1e46bf1534b3dba39e9493190b8ab}

다음 작업 중 하나를 완료할 때마다 데이터 세트 구성 파일에 지정한 대로 데이터 세트를 자동으로 재구성합니다.

* 새 데이터 소스를 추가합니다.
* 새 데이터 워크벤치 서버를 [!DNL Profile.cfg] 파일의 클러스터에 추가합니다.
* 파일을 [!DNL Cluster.cfg] 변경합니다.
* 다음을 포함하되 이에 한정되지 않는 파일 [!DNL Log Processing.cfg] 또는 [!DNL Log Processing Dataset Include] 파일을 변경합니다.

   * 새 매개 변수 추가
   * 변형 변경
   * 시작 시간 또는 종료 시간 매개 변수 변경

* 파일 [!DNL Insight Server.exe] 업그레이드

또한 파일의 재처리 매개 변수에 문자 또는 문자 조합을 입력하고 파일을 저장하여 언제든지 재처리를 시작할 수 [!DNL Log Processing.cfg] 있습니다.

>[!NOTE]
>
>재처리를 수행하려면 [!DNL Log Processing Mode.cfg] 파일의 Pause 매개 변수를 false로 설정해야 합니다. 이 매개 변수의 기본값은 false이므로 매개 변수를 변경할 필요가 없습니다. 자세한 내용은 추가 [!DNL Log Processing Mode.cfg]구성 [파일을 참조하십시오](/help/home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md).

## 재변형 {#section-02446744549940ada8eba0573ec5575f}

변형이나 새 치수 정의 등 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일에서 정보를 변경할 때마다 변환이 자동으로 수행됩니다.

파일 또는 [!DNL Transformation.cfg] 파일에서 참조되는 조회 파일( [!DNL Transformation Dataset Include] 조회 파일, [!DNL Categorize]및 [!DNL FlatFileLookup]변형에 대한 조회 파일 포함)을 변경할 때마다 [!DNL ODBCLookup] [!DNL Transformation.cfg] 파일의 재처리 매개 변수에 문자 또는 문자 조합을 입력하고 파일을 저장하여 변환을 시작해야 합니다.
