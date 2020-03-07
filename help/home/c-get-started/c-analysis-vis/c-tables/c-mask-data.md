---
description: 마스크는 데이터의 하위 집합이나 차원의 요소 하위 집합을 선택하는 것을 의미합니다.
solution: Analytics
title: 마스크 데이터
topic: Data workbench
uuid: 81b5f4e0-826c-4803-9169-66a424a4ea9f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 마스크 데이터{#mask-data}

마스크는 데이터의 하위 집합이나 차원의 요소 하위 집합을 선택하는 것을 의미합니다.

분석에 포함되지 않을 요소를 마스크하거나 숨깁니다.

데이터 워크벤치에서는 차원 요소를 마스크하는 두 가지 방법을 제공합니다. 첫 번째 방법은 [!DNL Mask] 메뉴에서 사용할 수 있는 옵션을 사용합니다. 메뉴 옵션을 사용하여 [!DNL Mask] 표시할 요소를 선택하거나 마스크를 적용할 요소를 선택하거나 지표별로 데이터를 정렬할 때 최상위 요소를 표시할 수 있습니다. 차원 요소를 마스크하는 두 번째 방법은 검색을 사용합니다.

**데이터를 마스크하려면**

1. 요소 또는 원하는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]**&#x200B;클릭합니다.

   ![](assets/mnu_Table_Mask.png)

1. 다음 옵션 중 하나를 클릭합니다.

   * **[!UICONTROL Show all]**
   * **[!UICONTROL Show selected only]**
   * **[!UICONTROL Hide selected]**
   * **[!UICONTROL Show top > 5, 10, 25, 50, 100]**, 또는 **[!UICONTROL 500]** 표시된 요소의 지표 정렬
   * **[!UICONTROL Show top > All Positive]** 0보다 큰 값만 표시하려면
   * **[!UICONTROL Display “X more”]** 현재 마스크된 요소의 수를 표시하려면
   * **[!UICONTROL At least one >]***&lt; **[!UICONTROL countable dimension name]**>*(비정상 차원으로 작업할 때만 사용 가능)

      비정상 차원으로 작업할 때 이 옵션을 사용하면 계산 가능한 차원으로 차원을 마스크 처리할 수 있습니다. 이 옵션을 선택하면 선택된 계산 가능한 차원의 요소가 하나 이상 있는 요소만 표에 표시됩니다. 표에는 최대 1,023개의 요소가 표시됩니다.

>[!NOTE]
>
>Adobe는 임의의 순서로 데이터를 [!DNL Platform] 처리하기 때문에 하나 이상의 마스크 처리 결과 1,023개 이상의 요소가 발생하면 보다 일반적이고 큰 요소가 표에 포함될 가능성이 높습니다.

[맨 위 표시] 또는 [하나 이상]로 마스크를 적용하면 기본적으로 표의 순서는 해당 시점에 선택한 항목의 영향을 받은 값에 해당합니다. 나중에 선택 항목을 변경할 경우 표를 다시 사용하거나 동적 선택을 활성화하지 않는 한 원래 주문에서 순서가 변경되지 않습니다. > **[!UICONTROL Mask]** 를 클릭하면 **[!UICONTROL Dynamic Selection]**&#x200B;선택 항목을 변경할 때마다 표가 다시 사용됩니다.

**검색을 사용하여 데이터 마스크**

* 다음 검색 옵션 중 하나를 사용하여 데이터를 마스크 처리할 수 있습니다.

   * 요소 또는 원하는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Mask]**&#x200B;클릭한 다음 [!DNL Search] 상자에 검색할 구문을 입력합니다.

      ![](assets/mnu_Table_MaskSearch.png)

   * 요소 또는 원하는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]** > **[!UICONTROL Display search bar]**&#x200B;을 클릭한 다음 차원 레이블 셀에 표시되는 검색 상자에 검색할 구문을 입력합니다.

      ![](assets/vis_Table_Mask_searchBar.png)

      검색 구문을 입력하면 데이터 워크벤치가 일치하는 항목을 반영하도록 차원을 업데이트합니다.

검색 중에 마스크를 추가로 제한하려면 다음 방법 중 하나를 사용할 수 있습니다.

* 상자나 막대에 &quot;re:&quot;를 입력하여 검색어가 정규 표현식으로 해석되도록 할 수 있습니다. [!DNL search] 검색 구문에서 정규 표현식과 연관된 구문을 사용할 수 있습니다. 정규 표현식에 대한 자세한 내용은 데이터 세트 구성 안내서의 정규 *표현식 부록을 참조하십시오*.
* $ 기호를 검색 문자열에서 첫 번째 문자로 입력하여 입력한 문자열로 시작하는 구문을 찾거나 입력한 문자열로 끝나는 구문을 찾을 수 있습니다.
* 검색 문자열에서 첫 번째 문자로 공백을 입력하여 입력한 문자열로 시작하는 구문 내의 단어를 찾거나 입력한 문자열로 끝나는 구문에서 단어를 찾을 수 있습니다.

다음은 검색에서 문자열 &quot;on&quot;을 사용하여 표를 마스크하는 다양한 방법의 예입니다.

* &quot;on&quot;을 입력하면 구문의 아무 위치에나 &quot;on&quot; 문자열이 포함된 모든 구문이 표시됩니다.&quot;****&#x200B;온라인 뱅킹,&quot; &quot;******접점 구매자&quot;, &quot;** 지금 ****&#x200B;주화&quot;, &quot;****&#x200B;온라인 은행&#x200B;**&quot;, &quot;금**&#x200B;옵션&quot;, &quot;금지금&quot;
* &quot;$on&quot;을 입력하면 &quot;on&quot; 문자열로 시작하는 모든 구문이 표시됩니다.

   &quot;****&#x200B;온라인 뱅킹&quot; 및 &quot;**온라인**&#x200B;지불&quot;

* &quot;on$&quot;을 입력하면 &quot;on&quot; 문자열로 끝나는 모든 구문이 표시됩니다.

   &quot;**은괴들**&quot; 및 &quot;금괴&#x200B;**옵션**&quot;

* &quot;on&quot;을 입력하면 &quot;on&quot; 문자열로 시작하는 단어가 포함된 모든 구문이 표시됩니다.

   &quot;****&#x200B;온라인 뱅킹&quot; 및 &quot;은행 ****&#x200B;온라인&quot;

* &quot;on&quot;을 입력하면 &quot;on&quot; 문자열로 끝나는 단어가 포함된 모든 구문이 표시됩니다.

   &#39;**금화** &#39;와 &#39;은괴들&#39;****.

* &quot;on&quot;을 사용하면 문자열 &quot;on&quot;을 단어로 포함하는 모든 구문이 표시됩니다.

   &quot;**온라인** 은행&quot; 및 &quot;은행 **온라인** &quot;
