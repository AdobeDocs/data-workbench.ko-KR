---
description: 프로필의 데이터 세트 구성 요소, 쿼리 모델 구성 요소 또는 작업 영역, 보고서, 메뉴 옵션 및 지구 레이어를 종속성 맵에 표시하도록 선택할 수 있습니다.
solution: Analytics
title: 프로필 구성 요소 표시
topic: Data workbench
uuid: c904dcb7-6bb9-445c-be55-0573f88928ad
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 프로필 구성 요소 표시{#display-profile-components}

프로필의 데이터 세트 구성 요소, 쿼리 모델 구성 요소 또는 작업 영역, 보고서, 메뉴 옵션 및 지구 레이어를 종속성 맵에 표시하도록 선택할 수 있습니다.

**표시할 구성 요소를 선택하려면**

1. 종속성 맵 내에서 마우스 오른쪽 단추를 클릭하고 을 **[!UICONTROL Display]**&#x200B;클릭합니다.
1. 맵에 표시할 다음 옵션 중 하나 이상을 선택합니다. 활성화한 각 디스플레이 옵션 왼쪽에 X가 나타납니다.

   * **데이터 집합** 구성 요소를 표시하는 데이터 집합. 데이터 [집합 구성 요소를 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-dataset-comp.md#concept-4afe28ad29d14eca8a5000847254c293). 데이터 집합 구성 요소를 표시하도록 선택하는 경우 [!DNL Include File Blocks] 맵에 표시할 옵션이 있습니다. 파일 [블록](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wkg-file-blocks.md#concept-3652bbabfbd34449a5f842d8aa598efc)작업을 참조하십시오.

   * **쿼리 모델을** 사용하여 쿼리 모델 구성 요소를 표시합니다. 쿼리 [모델 구성 요소를 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-qry-mod-comp.md#concept-32c6dadd32f74179b026c7e96d47710f).

   * **작업 영역 및 시각화를** 사용하여 작업 영역, 보고서, 메뉴 옵션 및 지구 레이어를 표시할 수 있습니다. 작업 [영역 및 시각화를 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wksps-vis.md#concept-abbd4fb115ff47f49f879466ce274921). 이 옵션은 [!DNL Query Model] 표시 옵션이 활성화된 경우에만 작동합니다.

>[!NOTE]
>
>표시 옵션을 선택할 때 [!DNL Query Model] 표시 옵션이 활성화되지 않으면 오류 메시지가 [!DNL Workspaces and Visualizations] 나타납니다.

맵에서 모든 노드를 볼 수 없는 경우 맵을 이동하거나 확대 또는 축소하여 전체 맵을 표시하거나 특정 섹션에 집중할 수 있습니다. 확대/축소에 대한 자세한 내용은 시각화 [확대를 참조하십시오](../../../../../home/c-get-started/c-vis/c-zoom-vis.md#concept-7e33670bb5344f78a316f1a84cc20530).

노드를 클릭하면 해당 노드에 의존하는 모든 노드 및 해당 노드가 종속된 모든 노드가 강조 표시되고 해당 이름이 표시됩니다.

![](assets/vis_DependencyMap_HighlightedPath.png)

>[!NOTE]
>
>종속성 맵에서 강조 표시된 경로가 선택 항목을 구성하지 않습니다.

노드를 마우스 오른쪽 단추로 클릭하면 맵에 표시된 각 구성 요소에 대한 식별 정보를 볼 수 있고 구성 요소에 대한 자세한 내용을 보거나 구성 요소를 편집할 수 있는 메뉴 옵션을 선택할 수 있습니다. 또한 텍스트 검색을 수행하고 변형 및 확장 차원에 대한 성능 정보를 표시할 수 있습니다.