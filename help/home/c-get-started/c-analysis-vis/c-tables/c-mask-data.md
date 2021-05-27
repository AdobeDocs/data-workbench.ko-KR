---
description: 마스킹은 데이터의 하위 집합이나 차원의 요소 하위 집합을 선택하는 것을 의미합니다.
title: 마스크 데이터
uuid: 81b5f4e0-826c-4803-9169-66a424a4ea9f
exl-id: 3029e08e-827f-40d7-b5a1-45630876a097
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 1%

---

# 마스크 데이터{#mask-data}

마스킹은 데이터의 하위 집합이나 차원의 요소 하위 집합을 선택하는 것을 의미합니다.

분석에 포함하지 않을 요소를 마스크하거나 숨깁니다.

Data Workbench은 차원 요소를 마스킹하는 두 가지 방법을 제공합니다. 첫 번째 방법은 [!DNL Mask] 메뉴에서 사용할 수 있는 옵션을 사용합니다. [!DNL Mask] 메뉴 옵션을 사용하면 마우스를 사용하여 표시하거나 숨길 요소를 선택하거나, 지표별로 데이터를 정렬할 때 최상위 요소를 표시할 수 있습니다. 차원 요소를 마스킹하는 두 번째 방법은 검색을 사용합니다.

**데이터를 마스크하려면**

1. 요소 또는 원하는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]** 을 클릭합니다.

   ![](assets/mnu_Table_Mask.png)

1. 다음 옵션 중 하나를 클릭합니다.

   * **[!UICONTROL Show all]**
   * **[!UICONTROL Show selected only]**
   * **[!UICONTROL Hide selected]**
   * **[!UICONTROL Show top > 5, 10, 25, 50, 100]**&#x200B;또는 지표 **[!UICONTROL 500]** 로 정렬된 표시된 요소 중
   * **[!UICONTROL Show top > All Positive]** 0보다 큰 값만 표시하려면
   * **[!UICONTROL Display “X more”]** 현재 마스킹된 요소의 수를 표시합니다.
   * **[!UICONTROL At least one >]***&lt;>>*(비정상 차원으로 작업할 때만 사용 가능)**[!UICONTROL countable dimension name]**

      비정상 차원으로 작업할 때 이 옵션을 사용하면 가산 차원별로 차원을 마스크할 수 있습니다. 선택한 경우, 테이블에는 선택한 가산 차원의 요소가 하나 이상 있는 요소만 표시됩니다. 테이블에는 최대 1,023개의 요소가 표시됩니다.

>[!NOTE]
>
>Adobe [!DNL Platform]은(는) 임의 순서로 데이터를 처리하므로 하나 이상의 마스킹으로 인해 1,023개 이상의 요소가 발생할 경우 일반적으로 더 큰 요소가 테이블에 포함될 가능성이 높습니다.

[맨 위 표시] 또는 [하나 이상 표시]로 마스크하는 경우 기본적으로 테이블의 순서는 해당 시간에 선택 항목의 영향을 받는 값에 해당합니다. 나중에 선택 영역을 변경할 경우, 테이블을 사용하거나 동적 선택을 활성화하지 않는 한 순서는 원래 주문에서 변경되지 않습니다. **[!UICONTROL Mask]** > **[!UICONTROL Dynamic Selection]** 를 클릭하면 선택 항목을 변경할 때마다 테이블이 다시 사용됩니다.

**검색을 사용하여 데이터를 마스크하려면**

* 다음 검색 옵션 중 하나를 사용하여 데이터를 마스크할 수 있습니다.

   * 요소 또는 원하는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]** 을 클릭한 다음 [!DNL Search] 상자에서 검색할 구문을 입력합니다.

      ![](assets/mnu_Table_MaskSearch.png)

   * 요소 또는 원하는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]** > **[!UICONTROL Display search bar]** 을 클릭한 다음 차원 레이블 셀에 표시되는 검색 상자에서 검색할 구문을 입력합니다.

      ![](assets/vis_Table_Mask_searchBar.png)

      검색 구문을 입력하면 Data Workbench이 일치 항목을 반영하도록 차원을 업데이트합니다.

검색 중에 마스킹을 추가로 제한하려면 다음 방법 중 하나를 사용할 수 있습니다.

* [!DNL search] 상자나 막대에 &quot;re:&quot;를 입력하여 검색 구문을 정규 표현식으로 해석할 수 있습니다. 검색 구문에서 정규 표현식과 연관된 구문을 사용할 수 있습니다. 정규 표현식에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;의 정규 표현식 부록을 참조하십시오.
* 입력한 문자열로 시작하는 구문을 찾거나 입력한 문자열로 끝나는 구문을 찾을 마지막 문자로 $ 기호를 입력할 수 있습니다.
* 검색 문자열에서 첫 번째 문자로 공백을 입력하여 입력한 문자열로 시작하는 구문에서 단어를 찾거나 입력한 문자열로 끝나는 구문에서 단어를 찾을 마지막 문자로 입력할 수 있습니다.

다음은 검색에서 문자열 &quot;on&quot;을 사용하여 테이블을 마스크하는 다양한 방법의 예입니다.

* &quot;on&quot;을 입력하면 구문의 모든 위치에 문자열 &quot;on&quot;이 포함된 모든 구문이 표시됩니다.&quot;**라인 뱅킹,&quot; &quot;c**&#x200B;정확한 구매자,&quot; &quot;b **접촉자&quot; &quot;bulli**&#x200B;입력&#x200B;**주화&quot;, &quot;bank** on **라인,&quot; &quot;gold opti** s&quot; 및 &quot;silver bulli **on**&#x200B;라인 뱅킹&quot;****
* &quot;$on&quot;을 입력하면 문자열 &quot;on&quot;으로 시작하는 모든 구문이 표시됩니다.

   &quot;**on**&#x200B;라인 뱅킹&quot; 및 &quot;**on** 라인 결제&quot;

* &quot;on$&quot;을 입력하면 문자열 &quot;on&quot;으로 끝나는 모든 구문이 표시됩니다.

   &quot;silver bulli **on**&quot; 및 &quot;gold opti **on**&quot;

* &quot;on&quot;을 입력하면 문자열 &quot;on&quot;으로 시작하는 단어가 포함된 모든 구문이 표시됩니다.

   &quot;**라인 뱅킹&quot; 및 &quot;bank** on **라인&quot;**

* &quot;on&quot;을 입력하면 문자열 &quot;on&quot;으로 끝나는 단어가 포함된 모든 구문이 표시됩니다.

   &quot;bulli **on** coins&quot; 및 &quot;silver bulli **on**&quot;

* &quot;on&quot;을 사용하면 문자열 &quot;on&quot;을 단어로 포함하는 모든 구문이 표시됩니다.

   &quot;**on** line banking&quot; 및 &quot;bank **on** line&quot;
