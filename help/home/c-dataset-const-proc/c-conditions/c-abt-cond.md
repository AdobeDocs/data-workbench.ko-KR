---
description: 변환 및 차원은 조건을 사용하여 특정 지침 또는 작업이 로그 필드에 적용되는 시기를 결정합니다.
title: 조건 정보
uuid: 882fe761-895c-4226-a019-270c50ae6da2
exl-id: 0d44282f-1327-4f11-90fc-7e6a2ef8dc76
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# 조건 정보{#about-conditions}

변환 및 차원은 조건을 사용하여 특정 지침 또는 작업이 로그 필드에 적용되는 시기를 결정합니다.

로그 항목 조건 매개 변수는 조건을 사용하여 데이터 집합 구성 프로세스에 포함할 로그 항목을 결정합니다. 이 부록은 데이터 워크벤치 서버 내에서 사용할 수 있는 다양한 유형의 조건에 대해 설명합니다.

조건은 다음 두 가지 카테고리 중 하나에 해당됩니다.

* **[!DNL Test Operations]사용 가능한 로그** [!DNL Compare] 필드 [!DNL Not Empty]에서 [!DNL Range] 다른 상태를 테스트하는 데 :,  [!DNL Regular Expression] [!DNL String Match] ,및조건이 사용됩니다.

* **[!DNL Boolean Operations]:** 위 [!DNL And]에 설명된 테스트 작업을 조합하는 데  [!DNL Or]  [!DNL Neither] 및 조건을 사용합니다. 예를 들어 [!DNL Range] 조건과 [!DNL String Match] 조건이 모두 false여야 적절한 작업을 수행할 때 모두 false여야 하는 경우 이러한 두 작업 중 [!DNL Neither] 조건의 하위 항목으로 지정합니다. [!DNL And] 조건은 시스템에서 모든 조건 테스트의 루트로 사용됩니다.
