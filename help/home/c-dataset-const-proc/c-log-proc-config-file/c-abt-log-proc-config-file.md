---
description: Log Processing.cfg 파일은 데이터 소스(로그 소스)에서 순서가 없는 데이터를 읽고 데이터에 필터 및 변형을 적용하는 데이터 세트 구성의 로그 처리 단계를 제어합니다.
title: 로그 처리 구성 파일 정보
uuid: 1f5f5d75-8a24-4122-adc8-8c8aef916631
exl-id: 11ee3298-272d-46c8-bcfe-e485b01606b1
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 5%

---

# 로그 처리 구성 파일 정보{#about-the-log-processing-configuration-file}

Log Processing.cfg 파일은 데이터 소스(로그 소스)에서 순서가 없는 데이터를 읽고 데이터에 필터 및 변형을 적용하는 데이터 세트 구성의 로그 처리 단계를 제어합니다.

다음 데이터 집합 구성 작업을 수행하려면 [!DNL Log Processing.cfg] 파일을 편집해야 합니다.

* 로그 소스 지정을 참조하십시오. [로그 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md)를 참조하십시오.
* 로그 처리 중에 데이터 세트에 입력하는 로그 항목을 확인합니다. [데이터 필터](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md) 및 [로그 항목 조건](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md)을 참조하십시오.

* 대량의 이벤트 데이터로 추적 ID 분할 활성화. [키 분할](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md)을 참조하십시오.
* 파일 서버 단위로 실행되도록 데이터 워크벤치 서버를 구성합니다. [Insight 서버 파일 서버 단위 구성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md)을 참조하십시오.
* 중앙 표준화 서버로 실행되도록 데이터 워크벤치 서버를 구성합니다. [Insight 서버 파일 서버 단위 구성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md)을 참조하십시오.

>[!NOTE]
>
>[!DNL Log Processing Dataset Include] 파일에는 데이터 집합 구성의 로그 처리 단계에 대한 추가 지침이 들어 있을 수 있습니다. 이러한 파일은 상속된 프로필의 데이터 세트\로그 처리 디렉터리 내에 있습니다. 일반적으로 응용 프로그램별 매개 변수(예: 사이트 응용 프로그램의 웹 특정 구성 매개 변수)를 정의합니다. [!DNL Log Processing Dataset Include] 파일에 대한 자세한 내용은 [데이터 세트에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오. 사이트에 대한 웹 특정 구성 매개 변수에 대한 자세한 내용은 [웹 데이터에 대한 구성 설정](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md)을 참조하십시오.
