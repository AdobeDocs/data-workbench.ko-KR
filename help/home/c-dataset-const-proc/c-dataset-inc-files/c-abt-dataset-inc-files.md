---
description: Adobe 애플리케이션에서 받은 내부 프로필의 대부분은 고유한 데이터 세트 구성 파일을 제공합니다.
solution: Analytics
title: 데이터 세트 포함 파일 정보
topic: Data workbench
uuid: e04d412e-7d73-4a7d-b0b6-0c2347c6201b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 세트 포함 파일 정보{#about-dataset-include-files}

Adobe 애플리케이션에서 받은 내부 프로필의 대부분은 고유한 데이터 세트 구성 파일을 제공합니다.

내부 프로필은 데이터 집합 프로필의 하위 프로필이므로 데이터 집합 구성 파일에는 로그 처리 또는 데이터 집합 구성의 변형 단계에 대한 추가 매개 변수를 제공하는 규칙이 들어 있습니다. 내부 프로필과 상속된 모든 프로필의 데이터 세트 구성 파일은 데이터 세트에 파일이 포함됩니다.

데이터 집합 포함 파일에는 데이터 집합 프로필의 기본 데이터 집합 구성 파일( [!DNL Log Processing.cfg] 또는 [!DNL Transformation.cfg])에 포함된 매개 변수의 하위 집합이 포함되어 있습니다. 데이터 집합에는 로그 처리와 관련된 매개 변수가 들어 있는 파일을 [!DNL Log Processing Dataset Include] 파일이라고 하는 반면 데이터 집합에는 [변환과 연결된 파일을](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab)파일이라고 하는 반면 데이터 집합은 [!DNL Transformation Dataset Include] 파일을 포함합니다. 변형 [데이터 세트 포함 파일을](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace)참조하십시오. 데이터 세트 구성 프로세스에서 사용할 수 있도록 여러 데이터 세트에 포함 파일을 만들 수 있습니다. 전체 데이터 집합에는 데이터 세트 프로필의 모든 데이터 세트 구성 파일에 정의된 모든 필드, 변형 및 확장 차원이 포함됩니다.
