---
description: 특정 노드와 연관된 데이터를 포함하거나 제외하는 필터를 만들기 위해 프로세스 맵 내에서 선택할 수 있습니다.
title: 프로세스 맵에서 선택
uuid: 7fd00090-c9ab-4bb6-8584-7de7b6f4b68c
exl-id: 8ede395f-906a-49e0-8ff8-b43a326275e5
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 3%

---

# 프로세스 맵에서 선택{#make-a-selection-from-a-process-map}

특정 노드와 연관된 데이터를 포함하거나 제외하는 필터를 만들기 위해 프로세스 맵 내에서 선택할 수 있습니다.

프로세스 맵 내에서 선택을 하는 것은 맵의 그룹 차원과 관련되어, 맵의 노드 등 기본 차원의 요소를 그룹화하여 노드 사이의 연결을 형성하는 방법을 결정합니다.

>[!NOTE]
>
>프로세스 맵에 대한 기본 그룹 차원을 변경할 수 있습니다. [프로세스 맵 구성](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-proc-maps.md#task-4a95730b18a14bc790a77c013832b2d6)을 참조하십시오.

프로세스 맵 내의 노드를 기반으로 선택할 경우 해당 노드가 포함된 그룹 차원의 모든 요소를 선택합니다. 그룹 차원의 역할을 더 잘 이해하려면 다음 예를 고려하십시오.

* 영화는 시청자를 대상으로 분류할 수 있다. 각 뷰어는 사용자 차원의 요소이므로 사용자 차원은 프로세스 맵의 그룹 차원이 됩니다. 특정 동영상의 노드를 선택할 때 해당 동영상을 재생했거나 평가하지 않은 사용자의 데이터를 표시하는 필터를 만듭니다.
* 웹 사이트 페이지를 본 세션별로 그룹화할 수 있습니다. 각 세션은 세션 차원의 요소이므로 세션 차원은 프로세스 맵의 그룹 차원이 됩니다. 특정 페이지에 대한 노드를 선택할 때 해당 페이지를 보았거나 보지 않은 세션에 대한 데이터를 표시하는 필터를 만듭니다.

**선택 영역을 만들려면**

1. 프로세스 맵에서 노드를 마우스 오른쪽 단추로 클릭합니다.
1. 노드를 기준으로 선택하려면 다음 옵션 중 하나를 클릭합니다.

   * **[!UICONTROL Select]***  **[!UICONTROL group dimension name +s]***  **[!UICONTROL through node name]**:노드를 통과하지 않은 모든 세션을 필터링하여 노드를 통과하는 그룹 차원의 모든 요소를 포함하도록 데이터를 필터링합니다.

   * **[!UICONTROL Select]***  **[!UICONTROL group dimension name +s]***  **[!UICONTROL NOT through node name]**:노드를 통과하는 모든 세션을 필터링하여 노드를 통과하지 않은 그룹 차원의 모든 요소를 포함하도록 데이터를 필터링합니다.

![](assets/vis_2DProcessMap_Selections_Movie.png)

![](assets/vis_2DProcessMap_Selections_Page.png)

3D 프로세스 맵에서 선택 영역을 만들면 선택 항목이 만들어진 노드가 원으로 표시됩니다. 각 막대에 벤치마크가 나타나므로 선택 항목을 사용하거나 사용하지 않고 지표 값을 비교할 수 있습니다. [벤치마크 이해](../../../../home/c-get-started/c-vis/c-ustd-benchmks.md#concept-c7b0f4102e92458096f8c4765cbe2914)를 참조하십시오.

![](assets/vis_3DProcessMap_Selection.png)
