---
description: Log Processing.cfg 파일의 특정 매개 변수에 대한 추가 정보에 대한 링크입니다.
title: 로그 처리 매개 변수
uuid: 97b25665-f588-4f44-8f71-2382600d1b6f
exl-id: f373e954-6827-4afa-9557-73e0a884a602
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 2%

---

# 로그 처리 매개 변수{#log-processing-parameters}

Log Processing.cfg 파일의 특정 매개 변수에 대한 추가 정보에 대한 링크입니다.

<!--
c_data_filters.xml
-->

## 데이터 필터 {#data-filters}

[!DNL Log Processing.cfg] 파일에 정의된 필터는 다음과 같습니다.

* 종료 시간
* 해시 임계값
* 시작 시간

이러한 매개 변수에 의해 정의된 필터링은 로그 항목이 디코더를 떠난 후, 변환 후, [!DNL Log Entry Condition]에 의해 평가되기 전에 발생합니다. 일반적으로 이러한 매개 변수를 변경하면 데이터 집합 구성이 변경됩니다.

데이터 소스를 사용하여 특정 기간을 포함하는 데이터 세트를 구성하는 데 권장되는 기술은 데이터 세트에 대해 시작 시간 및 종료 시간 매개 변수를 사용하는 것입니다.[!DNL Sensor]

시작 시간 및 종료 시간 매개 변수를 사용하여 로그 파일을 디렉터리별로 구분하는 등의 다른 기술보다 사용하는 것이 좋습니다. 데이터 집합에 대한 시작 및 종료 시간을 설정하여 Data Workbench 서버는 지정된 간격 내에 발생한 로그 항목만 자동으로 사용합니다. 종료 시간이 과거라고 가정할 경우, Data Workbench 서버는 일반적으로 데이터 세트를 새 변형 추가와 같이 업데이트하더라도 동일한 로그 항목 세트를 사용하여 데이터 세트를 업데이트합니다.

<!--
c_log_entry_con.xml
-->

## 로그 항목

기본적으로 사용 가능한 로그 항목에 대한 필터링 프로세스입니다. [!DNL Log Entry Condition]에서 false 값을 반환하면 사용 가능한 로그 항목 집합에서 로그 항목이 필터링됩니다.

[!DNL Log Entry Condition]은(는) 조건 작업을 사용하여 설명되며( [조건](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md) 참조), [!DNL Sensor]에서 수집한 입력 필드( *Data Workbench [!DNL Sensor] 안내서* 참조) 또는 [!DNL Log Processing.cfg] 파일 내에 포함된 변형으로 생성된 확장 필드를 사용하여 테스트 조건을 정의할 수 있습니다. [!DNL Log Entry] 조건은 로그 처리 중에 적용되며 변환 중에 선택적으로 적용할 수 있습니다.

이 예제에서는 웹 사이트 데이터에 [!DNL log entry condition] 을 사용하는 방법을 보여줍니다. [!DNL Log Entry Condition] 을 사용하여 웹 사이트의 특정 부분에 중점을 두는 데이터 세트를 만들거나 사이트에서 특정 작업을 수행하는 방문자가 만들 수 있습니다.

이 예제의 [!DNL Log Entry Condition]은(는) 사이트 저장소의 일부인 로그 항목만 포함하는 데이터 집합을 만듭니다. 정규 표현식에 대한 입력으로 [!DNL RECondition test] 패턴과 [!DNL "/store/.*"] 필드를 사용하여 [!DNL cs-uri-stem] 문자열을 사용하여 [!DNL "/store/"] 문자열로 시작하는 웹 페이지만 데이터 집합에 포함됩니다.

![](assets/cfg_LogProcessing_LogEntryCondition.png)

<!--
c_key_split.xml
-->

## 키 분할 {#key-split}

데이터 집합에 있는 추적 ID 수는 인위적으로 증가하지만, Data Workbench 서버에서 처리하는 총 로그 항목 수는 인위적으로 증가되지 않으므로 데이터 집합에 있는 계산 가능한 총 이벤트 수를 유지합니다. 단일 요소에 대한 데이터가 분할되면 데이터는 두 개의 다른 추적 ID와 영구적으로 연결되므로 관련될 수 없습니다.

예를 들어 웹 데이터를 사용하는 경우 각 추적 ID는 고유한 방문자를 나타냅니다. 키 분할을 활성화하면 대량의 이벤트 데이터가 있는 데이터 세트에 있는 방문자는 여러 방문자로 분할됩니다. 데이터 세트에 있는 방문자 수가 인위적으로 증가하더라도, 페이지 보기 수 또는 예약과 같이 계산할 수 있는 총 이벤트 수는 인위적으로 증가하지 않습니다. 분할이 발생하면 하위 방문자에 대한 데이터는 관련될 수 없습니다.

키 분할은 확률적 알고리즘을 사용합니다. 그 결과 메모리 사용량, 실패 가능성, 키 분할 임계값( [!DNL Split Key Bytes]) 및 데이터 세트 크기 간에 트레이드오프가 발생합니다. 권장 설정(아래에 나열됨)을 사용하면 실패 비율이 낮습니다. 이벤트 데이터가 키 분할 임계값을 초과하는 요소 중 약 22,000년(일반적으로 데이터 세트당 1개 미만)의 데이터 일부는 분할되지 않고 잘립니다.

키 분할 없이 각 매개 변수에 대해 권장되는 값은 다음 표에 나와 있습니다.

| 매개 변수 | 키 분할 없음 | 키 분할 |
|---|---|---|
| 그룹 최대 키 바이트 | 1e6 | 2e6 |
| 키 버킷 공간 분할 | 6e6 | 6e6 |
| 분할 키 바이트 | 0 | 1e6 |
| 분할 키 공간 비율 | 10 | 10 |

[!DNL Group Maximum Key Bytes] 단일 추적 ID에 대해 처리할 수 있는 최대 이벤트 데이터 양을 지정합니다. 이 제한을 초과하는 데이터는 데이터 집합 구성 프로세스에서 필터링됩니다. [!DNL Split Key Bytes] 단일 추적 ID가 여러 요소로 분할되는 바이트 수를 나타냅니다. 요소는 확률 분포에 따라 약 이 바이트 수로 분할됩니다. [!DNL Split Key Space Ratio] 키  [!DNL Split Key Bucket Space] 분할의 메모리 사용률 및 실패 비율을 제어합니다.

>[!NOTE]
>
>[!DNL Group Maximum Key Bytes]키  [!DNL Split Key Bytes]분할이 제대로 작동하려면 ,  [!DNL Split Key Space Ratio] 및  [!DNL Split Key Bucket Space] 모두를 선언해야 합니다. 컨설팅 Adobe 없이 이러한 매개 변수의 값을 변경하지 마십시오.
