---
description: 부울 연산은 부울 연산의 자식으로 작동하는 테스트 작업의 결과를 결합합니다.
title: 부울 작업
uuid: 01143bc2-c867-434c-8028-86d4708e8b80
exl-id: 5b01e614-5603-43ff-9be4-aa329cca1645
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---

# 부울 작업{#boolean-operations}

부울 연산은 부울 연산의 자식으로 작동하는 테스트 작업의 결과를 결합합니다.

테스트 작업에 대한 자세한 내용은 [테스트 작업](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-ops.md#concept-c4bf6cb9e7a94cc7ac49ca9b0b1a2144)을 참조하십시오. [!DNL boolean] 작업을 정의할 때 작업에 대해 0개 이상의 하위 항목을 정의할 수 있습니다.

**부울 작업에 자식 조건을 추가하려면**

1. 이름 또는 [!DNL Boolean] 작업에 해당하는 번호를 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL Add new child]**&#x200B;을 클릭하고 추가할 사용 가능한 조건 유형 중 하나를 선택합니다.
1. [!DNL Boolean] 작업에 대해 원하는 모든 하위 조건을 추가할 때까지 1단계와 2단계를 반복합니다.

   >[!NOTE]
   >
   >이름 또는 [!DNL Boolean] 작업에 해당하는 번호를 마우스 오른쪽 단추로 클릭하면 [!DNL Add new sibling] 메뉴 옵션이 표시됩니다. 형제 자매는 오른쪽 클릭한 [!DNL Boolean] 작업과 같은 조건 계층 구조의 상대 위치에 있는 다른 조건입니다. [!DNL Boolean] 작업에 대해 새 동위 멤버를 추가하는 것은 [!DNL Condition] 또는 [!DNL Log Entry Condition] 매개 변수를 마우스 오른쪽 단추로 클릭하여 새 조건을 추가하는 것과 같습니다.

**부울 작업에서 하위 조건을 제거하려면 다음을 수행합니다.**

1. [!DNL Boolean] 작업에서 제거할 자식 조건에 해당하는 숫자나 자식 조건의 이름을 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>을 클릭합니다. 여기서 number는 제거할 하위 조건에 해당하는 숫자입니다.

이 섹션에서는 다음 조건에 대해 설명합니다.

* [And](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a14dba4b07cc4ab9aeb20868f773db7c)
* [둘 다](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-7e48b61266aa43ecbc48b979bf5e939b)
* [또는](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a3aa0f56b6234f2680fa81939228326b)

## And {#section-a14dba4b07cc4ab9aeb20868f773db7c}

[!DNL And] 조건에는 0개 이상의 하위 조건이 있을 수 있으며 자식 노드가 false를 반환하지 않으면 true를 반환합니다.

[!DNL And] 조건은 데이터 워크벤치 서버 내의 모든 조건 테스트의 루트 작업을 형성합니다. [!DNL And] 조건에 자식이 없으면 조건이 true로 평가되고 관련 작업이 진행됩니다. 이 때문에 조건 테스트로서 [!DNL And] 조건만 있는 작업이 항상 실행되고 모든 조건 테스트의 루트로 사용되는 이유가 됩니다.

이 예에서는 2006년에 로그 항목의 날짜가 모두 발생하고 요청된 페이지가 [!DNL /products/purchase.asp]일 때 [!DNL And] 조건이 모두 발생할 때 [!DNL Copy] 변환이 발생하는 방법을 보여 줍니다.

![](assets/cfg_Condition_AndCondition.png)

## {#section-7e48b61266aa43ecbc48b979bf5e939b} 모두 아님

[!DNL Neither] 조건에는 0개 이상의 하위 조건이 있을 수 있으며 자식 조건이 true로 평가되는 경우 false를 반환합니다. [!DNL Neither] 조건에 자식이 없으면 해당 자식 중 어느 것도 true를 반환하지 못합니다. 따라서 [!DNL Neither] 조건은 true로 평가됩니다.

다음 예제에서는 두 개의 [!DNL Range] 조건이 자식으로 있는 [!DNL Neither] 조건을 보여 줍니다. [!DNL Neither] 조건은 2007년 1월 1일부터 2007년 1월 10일 사이 또는 2007년 1월 12일 기간 동안 2007년 1월 14일까지 발생한 로그 항목을 제외합니다. 이러한 조건을 [!DNL Log Entry Condition]으로 사용하여 수집된 데이터에 알려진 문제가 있었던 기간 동안 데이터 세트에서 트랜잭션을 제거할 수 있습니다.

![](assets/cfg_Condition_NeitherCondition.png)

## 또는 {#section-a3aa0f56b6234f2680fa81939228326b}

[!DNL Or] 조건에는 0개 이상의 자식 조건이 있을 수 있으며, 자식 조건 중 하나 이상이 true로 평가되는 경우 true를 반환합니다. [!DNL Or] 조건에 자식이 없으면 해당 자식 중 어느 것도 true를 반환하지 못합니다. 따라서 [!DNL Or] 조건은 false로 평가됩니다.

이 예제는 [!DNL String Match] 조건이 있는 [!DNL Or] 조건과 [!DNL Range] 조건이 자식으로 표시됩니다. [!DNL Or] 조건은 로그 항목에 [!DNL x-hasproblem] 값이 yes로 설정되어 있거나 2007년 1월 1일 - 2007년 1월 10일 동안 로그 항목이 발생한 경우에만 만족됩니다.

![](assets/cfg_Condition_OrCondition.png)
