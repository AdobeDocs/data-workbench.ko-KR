---
description: 계층 보기는 사이트 또는 HBX 응용 프로그램을 사용하는 경우에만 사용할 수 있습니다.
title: 계층 보기 적용
uuid: 859a92af-4f7e-4bb5-9a98-917006894301
exl-id: 27a69404-40d3-44ab-bf5c-b2a5d8d836c2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# 계층 보기 적용{#apply-hierarchy-views}

{{eol}}

계층 보기는 사이트 또는 HBX 응용 프로그램을 사용하는 경우에만 사용할 수 있습니다.

계층 보기는 파일 이름별로 계층적으로 구성된 웹 사이트의 페이지를 알파벳순으로 정렬하여 표시합니다. 분석 자체에 유용하지만 계층 보기를 사용하여 프로세스 맵과 같은 고급 시각화를 설정할 수도 있습니다. 프로세스 맵에 대한 자세한 내용은 [프로세스 맵](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e).

>[!NOTE]
>
>데이터 세트가 클러스터의 여러 서버에서 실행되도록 구성된 경우 이 기능이 제대로 작동하려면 시스템 관리자가 중앙 표준화 서버로 사용할 컴퓨터 기능을 지정해야 합니다. 이 작업을 수행하는 방법은 *데이터 집합 구성 안내서*.

![](assets/vis_Table_CompareHierarchy.png)

**계층 보기를 활성화하거나 비활성화하려면**

* 페이지 또는 URI 시각화에서 요소 또는 페이지 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Hierarchy View]**.

   ![](assets/mnu_Table_HierarchyView.png)

   옵션 옆에 X가 표시되면 [!DNL hierarchy view] 이 활성화되어 있습니다.

   계층은 트리 구조를 사용하여 웹 사이트 섹션과 페이지로 구성됩니다. 섹션(노드)은 섹션 이름 옆에 있는 + 또는 - 기호를 사용하여 확장하거나 압축할 수 있습니다. 개별 페이지 옆에는 + 또는 - 기호가 없습니다.

   ![](assets/vis_Table_HierarchyView_Expanded.png)

## 계층 뷰에서 Dimension 요소 마스킹 {#section-e477c469934846da8d807f92fc2f3ed1}

마스킹은 데이터의 하위 집합이나 차원의 요소 하위 집합을 선택하는 것을 의미합니다. 분석에 포함하지 않을 요소를 마스크하거나 숨깁니다. 사용 [!DNL Mask] 계층 보기에 대한 메뉴 옵션에서 요소를 시각화에 표시해야 하는 지표의 최소 비율을 선택합니다.

**를 사용하여 데이터를 마스크하려면 [!DNL Mask] 메뉴 옵션**

1. 요소 또는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Mask]**.

   ![](assets/mnu_Table_HierarchyView_Masking.png)

1. 자세히 아래에서 적절한 비율을 클릭한 다음 마스크할 지표를 클릭합니다.

예를 들어, 0.1%를 클릭한 다음 페이지 보기 수를 클릭하면, 총 페이지 보기 수의 0.1% 미만인 요소를 마스킹(숨김)하고, 총 페이지 보기 수의 0.1%를 초과하는 요소를 표시합니다. 0%를 클릭하면 선택한 지표에 대해 값이 0(영)인 모든 요소가 마스킹됩니다.
