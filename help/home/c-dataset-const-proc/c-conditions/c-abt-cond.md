---
description: 변형 및 차원은 조건을 사용하여 특정 지침이나 작업이 로그 필드에 적용되는 시기를 결정합니다.
title: 조건 정보
uuid: 882fe761-895c-4226-a019-270c50ae6da2
exl-id: 0d44282f-1327-4f11-90fc-7e6a2ef8dc76
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# 조건 정보{#about-conditions}

{{eol}}

변형 및 차원은 조건을 사용하여 특정 지침이나 작업이 로그 필드에 적용되는 시기를 결정합니다.

로그 항목 조건 매개 변수는 조건을 사용하여 데이터 집합 구성 프로세스에 포함해야 하는 로그 항목을 결정합니다. 이 부록에서는 Data Workbench 서버 내에서 사용할 수 있는 다양한 유형의 조건을 설명합니다.

조건은 다음 두 범주 중 하나에 속합니다.

* **[!DNL Test Operations]:** [!DNL Compare], [!DNL Not Empty], [!DNL Range], [!DNL Regular Expression], 및 [!DNL String Match] 조건은 사용 가능한 로그 필드에서 다양한 상태에 대해 테스트하는 데 사용됩니다.

* **[!DNL Boolean Operations]:** 다음 [!DNL And], [!DNL Or], 및 [!DNL Neither] 조건은 위에서 설명한 테스트 작업을 결합하는 데 사용됩니다. 예를 들어 [!DNL Range] 조건 및 [!DNL String Match] 적절한 작업을 수행하기 위해 둘 다 false여야 하는 조건에서는 이러한 두 작업 하위 항목이 [!DNL Neither] 조건. 다음 사항에 유의하십시오. [!DNL And] 조건은 시스템에서 모든 조건 테스트의 루트로 사용됩니다.
