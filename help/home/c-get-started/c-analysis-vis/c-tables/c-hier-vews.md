---
description: 계층 보기는 사이트 또는 HBX 응용 프로그램을 사용하는 경우에만 사용할 수 있습니다.
title: 계층 보기 적용
uuid: 859a92af-4f7e-4bb5-9a98-917006894301
exl-id: 27a69404-40d3-44ab-bf5c-b2a5d8d836c2
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# 계층 보기 적용{#apply-hierarchy-views}

계층 보기는 사이트 또는 HBX 응용 프로그램을 사용하는 경우에만 사용할 수 있습니다.

계층 보기는 파일 이름으로 계층적으로 구성된 웹 사이트의 페이지를 표시하고 알파벳순으로 정렬합니다. 분석 자체에는 유용하지만 계층 보기를 사용하여 프로세스 맵으로 고급 시각화를 설정할 수도 있습니다. 프로세스 맵에 대한 자세한 내용은 [프로세스 맵](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e)을 참조하십시오.

>[!NOTE]
>
>데이터 세트가 한 클러스터의 여러 서버에서 실행되도록 구성된 경우 이 기능이 제대로 작동하려면 시스템 관리자가 어떤 컴퓨터 기능을 Central Standardization Server로 지정해야 합니다. 이 작업을 수행하려면 *데이터 집합 구성 안내서*&#x200B;의 로그 처리 구성 파일 장을 참조하십시오.

![](assets/vis_Table_CompareHierarchy.png)

**계층 보기를 활성화하거나 비활성화하려면**

* 페이지 또는 URI 시각화에서 페이지 차원의 요소나 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Hierarchy View]**&#x200B;을 클릭합니다.

   ![](assets/mnu_Table_HierarchyView.png)

   [!DNL hierarchy view]이(가) 활성 상태일 때 옵션 옆에 X가 표시됩니다.

   계층 구조는 트리 구조를 사용하여 웹 사이트 섹션 및 페이지로 구성됩니다. 섹션 이름 옆에 있는 + 또는 - 기호를 사용하여 섹션(노드)을 확장하거나 확장할 수 있습니다. 개별 페이지에는 옆에 + 또는 - 기호가 없습니다.

   ![](assets/vis_Table_HierarchyView_Expanded.png)

## 계층 보기 {#section-e477c469934846da8d807f92fc2f3ed1}에서 Dimension 요소 마스크

마스크는 데이터의 하위 집합이나 차원의 요소 하위 집합을 선택하는 것을 말합니다. 분석에 포함하지 않을 요소를 마스크하거나 숨깁니다. 계층 보기에 대해 [!DNL Mask] 메뉴 옵션을 사용하여 시각화에 요소를 표시해야 하는 지표의 최소 백분율을 선택합니다.

**[!DNL Mask] 메뉴 옵션을 사용하여 데이터를 마스크하려면**

1. 요소 또는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]**&#x200B;을 클릭합니다.

   ![](assets/mnu_Table_HierarchyView_Masking.png)

1. 초과 값에서 적절한 비율을 클릭한 다음 마스크할 지표를 클릭합니다.

예를 들어, 0.1%를 클릭한 다음 페이지 보기를 클릭하면 총 페이지 보기 수의 0.1% 미만인 모든 요소를 마스크(숨김)하고 총 페이지 보기 수의 0.1%를 초과하는 요소를 표시합니다. 0%를 클릭하면 선택한 지표에 대해 값이 0(영)인 모든 요소에 마스킹합니다.
