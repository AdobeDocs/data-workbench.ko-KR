---
description: 새 방문자 조건 은 데이터 집합에 포함할 방문자를 결정하는 웹 사이트 데이터와 함께 사용되는 조건 작업입니다.
title: 새 방문자 조건
uuid: e9733109-5bf3-47ce-974c-d68264291f19
exl-id: a0520edd-bde3-4f55-858c-8974d4224435
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 3%

---

# 새 방문자 조건{#new-visitor-condition}

새 방문자 조건 은 데이터 집합에 포함할 방문자를 결정하는 웹 사이트 데이터와 함께 사용되는 조건 작업입니다.

[!DNL New Visitor Condition] 은 데이터 집합에 사용할 방문자에 대한 첫 번째 로그 항목(시간별 순서)을 정의하며, 이 방문자의 모든 후속 로그 항목은 이 조건을 충족하는지 여부에 관계없이 데이터 세트에 포함됩니다. [!DNL New Visitor Condition]에는 방문자와 시간별로 데이터가 정렬되어야 하므로 데이터 집합 구성의 변환 단계 동안에만 적용됩니다.

이 예제에 표시된 [!DNL New Visitor Condition]은 이메일 캠페인에 응답하는 방문자에 대한 로그 항목만 포함하는 데이터 세트를 만듭니다. 이 작업은 [!DNL NotEmptyCondition] 테스트([비어 있지 않음](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1decb9d887894073a1b6b3d985729ac8) 참조)와 [!DNL x-campaign-email] 필드를 정규 표현식에 대한 입력으로 사용하여 수행됩니다. 조건을 충족하는 새 방문자가 식별되면 해당 방문자에 대한 모든 로그 항목이 캡처됩니다.

![](assets/cfg_Transformation_NewVisitorCondition.png)
