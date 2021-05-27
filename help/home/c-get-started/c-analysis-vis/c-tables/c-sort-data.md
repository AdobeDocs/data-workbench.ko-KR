---
description: 데이터를 정렬하는 단계입니다.
title: 테이블의 데이터 정렬
uuid: 66869478-922d-41e1-915d-3ed7bff3b08d
exl-id: 9cacb9bc-1bad-417b-b506-ca54e644de00
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 5%

---

# 테이블의 데이터 정렬{#sort-data-in-a-table}

데이터를 정렬하는 단계입니다.

테이블에 차원이 하나만 있으면 데이터를 정렬할 지표의 레이블을 클릭하면 됩니다.

1. 정렬할 요소나 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Sort]** 을 클릭합니다.

   ![](assets/mnu_Table_Sort.png)

1. 다음 옵션 중 하나를 클릭합니다.

   * **[!UICONTROL By ordinal]** 요소의 자연어 순서에 따라 요소를 정렬하기 위해 예를 들어 시간 차원의 요소는 시간 순서대로 표시됩니다. 레퍼러나 URI와 같이 차원에 자연어 순서가 없는 경우 정렬 순서는 유용하지 않으므로 사전순 또는 지표로 정렬하도록 선택해야 합니다.
   * **[!UICONTROL Alphabetically]** 차원을 요소 이름별로 알파벳순으로 정렬하려면
   * **[!UICONTROL By metric]** 데이터를 정렬할 지표를 선택하려면 다음을 수행하십시오. 예를 들어, 세션 지표로 레퍼러 차원을 정렬하여 사이트에서 가장 많은 세션을 제공하는 레퍼러를 확인할 수 있습니다.

      지표로 정렬하면 기본적으로 테이블의 순서는 해당 시간의 선택 내용에 영향을 받는 지표의 값에 해당합니다. 나중에 선택을 변경할 경우, 차원을 사용하거나 동적 선택을 활성화하지 않는 한 정렬된 순서는 원래 주문에서 변경되지 않습니다. **[!UICONTROL Sort]** > **[!UICONTROL Dynamic Selection]** 를 클릭하면 선택 항목을 변경할 때마다 테이블이 다시 사용됩니다.
   테이블의 기존 지표로 정렬하려면 지표 레이블을 클릭합니다.

1. (선택 사항) 오름차순이나 내림차순으로 정렬할지 여부를 선택하려면 정렬할 요소나 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Sort]** > **[!UICONTROL Order]** > **[!UICONTROL Ascending]** 또는 **[!UICONTROL Sort]** > **[!UICONTROL Order]** > **[!UICONTROL Descending]**&#x200B;를 클릭합니다.

   테이블에 차원이 하나만 있으면 지표의 레이블을 클릭하여 정렬 순서를 취소할 수 있습니다. 레이블을 다시 클릭하면 정렬 순서가 바뀝니다.
