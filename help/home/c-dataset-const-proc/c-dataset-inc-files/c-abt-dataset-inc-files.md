---
description: Adobe 애플리케이션과 함께 받은 대부분의 내부 프로필에는 고유한 데이터 세트 구성 파일이 포함되어 있습니다.
title: 데이터 세트 포함 파일 정보
uuid: e04d412e-7d73-4a7d-b0b6-0c2347c6201b
exl-id: a23d3f83-4e92-4787-9f77-ee9914cb8893
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 4%

---

# 데이터 세트 포함 파일 정보{#about-dataset-include-files}

{{eol}}

Adobe 애플리케이션과 함께 받은 대부분의 내부 프로필에는 고유한 데이터 세트 구성 파일이 포함되어 있습니다.

내부 프로필은 데이터 집합 프로필의 하위 프로필이므로 데이터 집합 구성 파일에는 데이터 집합 구성의 로그 처리 또는 변형 단계에 대한 추가 매개 변수를 제공하는 규칙이 포함되어 있습니다. 내부 프로필 및 생성한 상속된 프로필에 대한 데이터 집합 구성 파일을 데이터 집합에 포함 파일이라고 합니다.

데이터 집합 포함 파일에는 기본 데이터 집합 구성 파일( [!DNL Log Processing.cfg] 또는 [!DNL Transformation.cfg])을 클릭하여 데이터 집합 프로필을 만듭니다. 데이터 집합에 로그 처리와 연결된 매개 변수가 포함된 파일이 호출됩니다 [!DNL Log Processing Dataset Include] 파일( [로그 처리 데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab))인 반면, 데이터 집합에 변형과 연결된 파일이 포함되어 있으면 [!DNL Transformation Dataset Include] 파일. 자세한 내용은 [변형 데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace). 데이터 집합 구성 프로세스에서 사용할 여러 데이터 집합에 포함 파일을 만들 수 있습니다. 전체 데이터 세트에는 데이터 집합 프로필과 상속된 프로필의 모든 데이터 집합 구성 파일에 정의된 모든 필드, 변형 및 확장 차원이 포함됩니다.
