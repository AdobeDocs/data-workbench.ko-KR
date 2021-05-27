---
description: Transformation.cfg 파일은 데이터 집합 구성의 변환 단계를 제어하여 로그 처리 중에 이미 처리된 데이터에 추가 데이터 변형을 적용하여 분석에 사용할 확장 차원을 생성합니다.
title: 변환 구성 파일 정보
uuid: 56e11b71-1a86-47d4-8d2a-2795532b0770
exl-id: 860562d7-6ed3-486b-9f62-1bd06878bf7e
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 5%

---

# 변환 구성 파일 정보{#about-the-transformation-configuration-file}

Transformation.cfg 파일은 데이터 집합 구성의 변환 단계를 제어하여 로그 처리 중에 이미 처리된 데이터에 추가 데이터 변형을 적용하여 분석에 사용할 확장 차원을 생성합니다.

다음 데이터 집합 구성 작업을 수행하려면 [!DNL Transformation.cfg] 파일을 편집해야 합니다.

* 변환을 위해 [!DNL log entry condition]을(를) 정의하여 로그 처리에서 데이터를 필터링합니다.
* 시간 차원을 만들고 시간 변환을 만드는 데 사용할 시간대를 설정합니다. [시간대](../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956)를 참조하십시오.

>[!NOTE]
>
>[!DNL Transformation Dataset Include] 파일에는 데이터 집합 구성의 변환 단계에 대한 추가 지침이 포함될 수 있습니다. 이러한 파일은 상속된 프로파일에 대한 Dataset\Transformation 디렉터리 내에 있으며 일반적으로 응용 프로그램별 매개 변수(예: [!DNL Site] 응용 프로그램에 대한 웹 특정 구성 매개 변수)를 정의합니다. [!DNL Transformation Dataset Include] 파일에 대한 자세한 내용은 [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오. 사이트의 웹 특정 구성 매개 변수에 대한 자세한 내용은 [웹 데이터에 대한 구성 설정](../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)을 참조하십시오.
