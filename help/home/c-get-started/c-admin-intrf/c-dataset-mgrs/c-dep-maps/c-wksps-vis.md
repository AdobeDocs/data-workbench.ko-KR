---
description: 작업 영역 및 시각화에 대한 개념 정보입니다.
solution: Analytics
title: 작업 영역 및 시각화
topic: Data workbench
uuid: dc7fab6c-d8b4-4ed7-bad6-b3df14b9ebbf
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 작업 영역 및 시각화{#workspaces-and-visualizations}

작업 영역 및 시각화에 대한 개념 정보입니다.

다음 그림은 노드에서 프로파일에 정의된 작업 영역, 보고서, 메뉴 옵션 및 지구 레이어를 나타내는 종속성 맵을 보여줍니다. 이 옵션은 [!DNL Query Model] 표시 옵션이 활성화된 경우에만 작동합니다.

>[!NOTE]
>
>표시 옵션을 선택할 때 [!DNL Query Model] 표시 옵션이 활성화되지 않으면 오류 메시지가 [!DNL Workspaces and Visualizations] 나타납니다.

![](assets/vis_DependencyMap_QueryModelandWorkspaces.png)

* 회색 노드는 작업 공간 또는 보고서를 나타냅니다.
* 노란색-녹색 노드는 메뉴 옵션을 나타냅니다.
* 빨간색 노드는 끊기거나 순환 종속성이 있거나 다른 오류가 있는 작업 영역, 보고서, 메뉴 옵션 또는 지구 레이어를 나타냅니다.

>[!NOTE]
>
>종속성 맵은 클릭 종속성을 수용하도록 설계되었으므로 순환 종속성에 관련된 노드가 맵에 제대로 표시되지 않을 수 있습니다. 텍스트 상자에 &quot;순환 종속성&quot;을 입력하여 순환 종속성을 검색할 수 [!DNL Search] 있습니다. 기능에 대한 자세한 [!DNL Search] 내용은 맵 내 [검색을 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/t-srch-map.md#task-a1e7065a538d46c78a7d28676d880dfb).

맵의 다른 노드에 대한 설명은 쿼리 모델 [구성 요소를 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-qry-mod-comp.md#concept-32c6dadd32f74179b026c7e96d47710f).
