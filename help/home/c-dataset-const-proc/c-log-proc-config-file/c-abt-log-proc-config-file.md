---
description: Log Processing.cfg 파일은 데이터 소스(로그 소스)에서 순서가 없는 데이터를 읽는 동안 데이터 세트 구성의 로그 처리 단계를 제어하고 필터 및 변형을 데이터에 적용합니다.
solution: Analytics
title: 로그 처리 구성 파일 정보
topic: Data workbench
uuid: 1f5f5d75-8a24-4122-adc8-8c8aef916631
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 로그 처리 구성 파일 정보{#about-the-log-processing-configuration-file}

Log Processing.cfg 파일은 데이터 소스(로그 소스)에서 순서가 없는 데이터를 읽는 동안 데이터 세트 구성의 로그 처리 단계를 제어하고 필터 및 변형을 데이터에 적용합니다.

다음 데이터 집합 구성 작업을 수행하려면 [!DNL Log Processing.cfg] 파일을 편집해야 합니다.

* 로그 소스 지정을 참조하십시오. 로그 [소스를 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md).
* 로그 처리 중에 데이터 세트에 들어오는 로그 항목을 결정합니다. 데이터 [필터](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md) 및 [로그 항목 조건을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).

* 대량의 이벤트 데이터로 추적 ID 분할 활성화. 키 [분할을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md).
* 파일 서버 단위로 실행되도록 데이터 워크벤치 서버를 구성합니다. Insight [Server 파일 서버 단위 구성을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).
* 중앙 표준화 서버로 실행되도록 데이터 워크벤치 서버를 구성합니다. Insight [Server 파일 서버 단위 구성을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

>[!NOTE]
>
>[!DNL Log Processing Dataset Include] 파일에는 데이터 집합 구성의 로그 처리 단계에 대한 추가 지침이 들어 있을 수 있습니다. 이러한 파일은 상속된 모든 프로필에 대해 데이터 집합\로그 처리 디렉터리 내에 있습니다. 일반적으로 응용 프로그램별 매개 변수(예: 사이트 응용 프로그램의 웹 특정 구성 매개 변수)를 정의합니다. 파일에 대한 자세한 내용은 [!DNL Log Processing Dataset Include] 데이터 세트 포함 [파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). 사이트에 대한 웹 특정 구성 매개 변수에 대한 자세한 내용은 웹 [데이터에 대한 구성 설정을 참조하십시오](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md).

