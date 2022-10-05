---
description: 부울 작업은 부울 작업의 하위 기능인 테스트 작업의 결과를 결합합니다.
title: 부울 작업
uuid: 01143bc2-c867-434c-8028-86d4708e8b80
exl-id: 5b01e614-5603-43ff-9be4-aa329cca1645
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---

# 부울 작업{#boolean-operations}

{{eol}}

부울 작업은 부울 작업의 하위 기능인 테스트 작업의 결과를 결합합니다.

테스트 작업에 대한 자세한 내용은 [테스트 작업](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-ops.md#concept-c4bf6cb9e7a94cc7ac49ca9b0b1a2144). 을(를) 정의할 때 [!DNL boolean] 작업에 대해 0개 이상의 하위 항목을 정의할 수 있습니다.

**부울 작업에 하위 조건을 추가하려면**

1. 이름 또는 [!DNL Boolean] 작업.
1. 클릭 **[!UICONTROL Add new child]** 추가할 사용 가능한 조건 유형 중 하나를 선택합니다.
1. 에 대해 원하는 모든 하위 조건을 추가할 때까지 1단계와 2단계를 반복합니다 [!DNL Boolean] 작업.

   >[!NOTE]
   >
   >이름을 마우스 오른쪽 단추로 클릭하거나 [!DNL Boolean] 작업, [!DNL Add new sibling] 메뉴 옵션. 동위 조건은 조건 계층 구조에서 다음과 같은 상대적 위치에 있는 다른 조건입니다 [!DNL Boolean] 마우스 오른쪽 단추를 클릭한 작업입니다. 에 대해 새 동위 멤버 추가 [!DNL Boolean] 작업은 을 마우스 오른쪽 단추로 클릭하여 새 조건을 추가하는 것과 같습니다 [!DNL Condition] 또는 [!DNL Log Entry Condition] 매개 변수.

**부울 작업에서 하위 조건을 제거하려면 다음을 수행합니다.**

1. 자식 조건 이름 또는 자식 조건에서 제거할 자식 조건에 해당하는 숫자를 마우스 오른쪽 단추로 클릭합니다. [!DNL Boolean] 작업.
1. 클릭 **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***> 여기서 number 는 제거할 하위 조건에 해당하는 번호입니다.

이 섹션에서는 다음 조건을 설명합니다.

* [And](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a14dba4b07cc4ab9aeb20868f773db7c)
* [둘 다](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-7e48b61266aa43ecbc48b979bf5e939b)
* [또는](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a3aa0f56b6234f2680fa81939228326b)

## And {#section-a14dba4b07cc4ab9aeb20868f773db7c}

다음 [!DNL And] 조건은 0개 이상의 하위 조건을 가질 수 있으며 해당 하위 노드 중 어느 하나도 false를 반환하지 않으면 true를 반환합니다.

다음 [!DNL And] 조건은 data workbench 서버 내의 모든 조건 테스트의 루트 작업을 형성합니다. 만약 [!DNL And] 조건이 하위 항목을 포함하지 않으며 조건이 true로 평가되고 관련 작업이 진행됩니다. 이러한 이유로 [!DNL And] 조건 테스트는 항상 실행되며 모든 조건 테스트에 대한 루트로 사용되는 이유입니다.

이 예는 다음과 같은 [!DNL And] 조건은 [!DNL Copy] 변환은 로그 항목이 2006년에 발생한 날짜와 요청한 페이지가 모두 발생한 경우에만 발생합니다 [!DNL /products/purchase.asp].

![](assets/cfg_Condition_AndCondition.png)

## 둘 다 {#section-7e48b61266aa43ecbc48b979bf5e939b}

다음 [!DNL Neither] 조건은 0개 이상의 하위 조건을 가질 수 있으며 자식 조건이 true로 평가되는 경우 false를 반환합니다. 만약 [!DNL Neither] 조건은 하위 항목을 포함하지 않으며, 하위 항목은 true를 반환하지 않습니다. 따라서, [!DNL Neither] 조건은 true로 평가됩니다.

다음 예는 를 보여줍니다. [!DNL Neither] 2인 조건 [!DNL Range] 그 아이들의 조건들. 정의된 대로 [!DNL Neither] 조건은 2007년 1월 1일부터 2007년 1월 10일 사이 또는 2007년 1월 12일 동안 발생한 로그 항목을 2007년 1월 14일까지 제외합니다. 이러한 조건은 [!DNL Log Entry Condition] 수집된 데이터에 알려진 문제가 있는 기간 동안 데이터 세트에서 트랜잭션을 제거하려면 다음을 수행합니다.

![](assets/cfg_Condition_NeitherCondition.png)

## 또는 {#section-a3aa0f56b6234f2680fa81939228326b}

다음 [!DNL Or] 조건은 0개 이상의 하위 조건을 가질 수 있으며 해당 하위 조건 중 하나 이상이 true로 평가되면 true를 반환합니다. 만약 [!DNL Or] 조건은 하위 항목을 포함하지 않으며, 하위 항목은 true를 반환하지 않습니다. 따라서, [!DNL Or] 조건은 false로 평가됩니다.

이 예는 를 보여줍니다. [!DNL Or] 조건이 [!DNL String Match] 조건 및 [!DNL Range] 조건을 자녀로 합니다. 다음 [!DNL Or] 로그 항목에 [!DNL x-hasproblem] 값을 yes로 설정하거나 로그 항목이 2007년 1월 1일 ~ 2007년 1월 10일 동안 발생했습니다.

![](assets/cfg_Condition_OrCondition.png)
