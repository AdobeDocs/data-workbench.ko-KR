---
description: Log Processing.cfg 파일은 데이터 소스(로그 소스라고 함)에서 비순차 데이터를 읽는 동안 데이터 집합 구성의 로그 처리 단계를 제어하며 데이터에 필터 및 변환이 적용됩니다.
title: 로그 처리 구성 파일 정보
uuid: 1f5f5d75-8a24-4122-adc8-8c8aef916631
exl-id: 11ee3298-272d-46c8-bcfe-e485b01606b1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 5%

---

# 로그 처리 구성 파일 정보{#about-the-log-processing-configuration-file}

{{eol}}

Log Processing.cfg 파일은 데이터 소스(로그 소스라고 함)에서 비순차 데이터를 읽는 동안 데이터 집합 구성의 로그 처리 단계를 제어하며 데이터에 필터 및 변환이 적용됩니다.

를 편집해야 합니다 [!DNL Log Processing.cfg] 다음 데이터 집합 구성 작업을 수행하는 파일입니다.

* 로그 소스를 지정합니다. 자세한 내용은 [로그 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md).
* 로그 처리 중에 데이터 집합에 들어가는 로그 항목을 결정합니다. 자세한 내용은 [데이터 필터](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md) 및 [로그 항목 조건](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).

* 대량의 이벤트 데이터를 사용하여 추적 ID 분할을 활성화합니다. 자세한 내용은 [키 분할](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).
* 파일 서버 단위로 실행되도록 Data Workbench 서버 구성 자세한 내용은 [Insight Server 파일 서버 유닛 구성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).
* 중앙 표준화 서버로 실행되도록 Data Workbench 서버 구성 자세한 내용은 [Insight Server 파일 서버 유닛 구성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

>[!NOTE]
>
>[!DNL Log Processing Dataset Include] 파일에는 데이터 집합 구성의 로그 처리 단계에 대한 추가 지침이 포함될 수 있습니다. 이 파일은 상속된 프로필의 데이터 집합\로그 처리 디렉터리에 있습니다. 일반적으로 응용 프로그램별 매개 변수(예: 사이트 응용 프로그램의 웹 특정 구성 매개 변수)를 정의합니다. 에 대한 자세한 정보 [!DNL Log Processing Dataset Include] 파일, [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). 사이트의 웹 특정 구성 매개 변수에 대한 자세한 내용은 [웹 데이터에 대한 구성 설정](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md).
