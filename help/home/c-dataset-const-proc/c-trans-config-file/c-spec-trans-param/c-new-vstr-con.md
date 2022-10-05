---
description: 새 방문자 조건 은 데이터 집합에 포함할 방문자를 결정하는 웹 사이트 데이터와 함께 사용되는 조건 작업입니다.
title: 새 방문자 조건
uuid: e9733109-5bf3-47ce-974c-d68264291f19
exl-id: a0520edd-bde3-4f55-858c-8974d4224435
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 3%

---

# 새 방문자 조건{#new-visitor-condition}

{{eol}}

새 방문자 조건 은 데이터 집합에 포함할 방문자를 결정하는 웹 사이트 데이터와 함께 사용되는 조건 작업입니다.

다음 [!DNL New Visitor Condition] 데이터 세트에 사용할 방문자에 대한 첫 번째 로그 항목(시간별 순서)을 정의하고 이 방문자의 모든 후속 로그 항목은 이 조건을 충족하는지 여부에 관계없이 데이터 세트에 포함됩니다. 왜냐하면 [!DNL New Visitor Condition] 를 사용하려면 데이터가 방문자 및 시간별로 정렬되어야 하며 데이터 세트 구성의 변환 단계 동안에만 적용됩니다.

다음 [!DNL New Visitor Condition] 이 예제에 표시된 는 이메일 캠페인에 응답하는 방문자에 대한 로그 항목만 포함하는 데이터 세트를 만듭니다. 이 작업은 를 사용하여 수행됩니다 [!DNL NotEmptyCondition] 테스트( [비어 있지 않음](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1decb9d887894073a1b6b3d985729ac8)) 및 [!DNL x-campaign-email] 정규 표현식에 입력되는 필드입니다. 조건을 충족하는 새 방문자가 식별되면 해당 방문자에 대한 모든 로그 항목이 캡처됩니다.

![](assets/cfg_Transformation_NewVisitorCondition.png)
