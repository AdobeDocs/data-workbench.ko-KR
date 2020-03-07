---
description: 변형 및 차원은 조건을 사용하여 특정 지침 또는 작업이 로그 필드에 적용되는 시기를 결정합니다.
solution: Analytics
title: 조건 정보
topic: Data workbench
uuid: 882fe761-895c-4226-a019-270c50ae6da2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 조건 정보{#about-conditions}

변형 및 차원은 조건을 사용하여 특정 지침 또는 작업이 로그 필드에 적용되는 시기를 결정합니다.

로그 항목 조건 매개 변수는 조건을 사용하여 데이터 집합 구성 프로세스에 포함할 로그 항목을 결정합니다. 이 부록에서는 데이터 워크벤치 서버 내에서 사용할 수 있는 다양한 유형의 조건에 대해 설명합니다.

조건은 다음 두 카테고리 중 하나에 해당됩니다.

* **[!DNL Test Operations]:**사용 가능한 로그[!DNL Compare]필드에서 다른 상태에 대해 테스트하는 데[!DNL Not Empty][!DNL Range],[!DNL Regular Expression]및[!DNL String Match]조건이 사용됩니다.

* **[!DNL Boolean Operations]:**이[!DNL And],[!DNL Or]및[!DNL Neither]조건은 위에 설명된 테스트 작업을 결합하는 데 사용됩니다. 예를 들어, 적절한 작업을 수행하기 위해 둘 다 false여야 하는[!DNL Range]조건과[!DNL String Match]조건이 있는 경우, 이러한 두 작업 하위[!DNL Neither]조건을 만듭니다. 이[!DNL And]조건은 시스템에서 모든 조건 테스트의 루트로 사용됩니다.

