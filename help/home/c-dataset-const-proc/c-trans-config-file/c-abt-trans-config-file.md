---
description: Transformation.cfg 파일은 데이터 세트 생성의 변형 단계를 제어하여 로그 처리 중에 이미 처리된 데이터에 추가 데이터 변형을 적용하여 분석에 사용할 확장 차원을 만듭니다.
solution: Analytics
title: 변환 구성 파일 정보
topic: Data workbench
uuid: 56e11b71-1a86-47d4-8d2a-2795532b0770
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 변환 구성 파일 정보{#about-the-transformation-configuration-file}

Transformation.cfg 파일은 데이터 세트 생성의 변형 단계를 제어하여 로그 처리 중에 이미 처리된 데이터에 추가 데이터 변형을 적용하여 분석에 사용할 확장 차원을 만듭니다.

다음 데이터 집합 구성 작업을 수행하려면 [!DNL Transformation.cfg] 파일을 편집해야 합니다.

* 변환을 정의하여 로그 처리에서 데이터를 [!DNL log entry condition] 필터링합니다.
* 시간 차원 생성 및 시간 변환에 사용할 표준 시간대 설정 시간대를 [참조하십시오](../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956).

>[!NOTE]
>
>[!DNL Transformation Dataset Include] 파일에는 데이터 세트 구성의 변환 단계에 대한 추가 지침이 들어 있을 수 있습니다. 이러한 파일은 상속된 모든 프로파일의 Dataset\Transformation 디렉토리 내에 있으며 일반적으로 애플리케이션별 매개 변수(예: 응용 프로그램의 웹 특정 구성 매개 변수)를 정의합니다. [!DNL Site] 파일에 대한 자세한 내용은 [!DNL Transformation Dataset Include] 데이터 세트 포함 [파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md). 사이트에 대한 웹 특정 구성 매개 변수에 대한 자세한 내용은 웹 [데이터에 대한 구성 설정을 참조하십시오](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

