---
description: 쿼리 모델 구성 요소에 대한 개념 정보입니다.
solution: Analytics
title: 쿼리 모델 구성 요소
topic: Data workbench
uuid: 708fab0b-dc10-4306-b410-49268069ac3b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 쿼리 모델 구성 요소{#query-model-components}

쿼리 모델 구성 요소에 대한 개념 정보입니다.

다음 그림은 노드 종속성 맵이 표시되어 있습니다. 종속성 맵은 프로필 내에서 차원, 지표 및 필터 폴더에 정의된 필터 및 이와 관련된 데이터 세트에 정의된 확장 차원을 나타냅니다.

![](assets/vis_DependencyMap_QueryModel.png)

* 노란색-녹색 노드는 필터를 나타냅니다.
* 자주색 노드는 지표를 나타냅니다.
* 파란색-녹색 노드는 파생된 차원을 나타냅니다.
* 녹색 노드는 확장된 차원(데이터 세트에 정의됨)을 나타냅니다.
* 빨간색 노드는 끊기거나 순환 종속성이 있거나 다른 오류가 있는 지표, 파생 차원 또는 필터를 나타냅니다.

>[!NOTE]
>
>종속성 맵은 클릭 종속성을 수용하도록 설계되었으므로 순환 종속성에 관련된 노드가 맵에 제대로 표시되지 않을 수 있습니다. 텍스트 상자에 &quot;순환 종속성&quot;을 입력하여 순환 종속성을 검색할 수 [!DNL Search] 있습니다. 기능에 대한 자세한 [!DNL Search] 내용은 맵 내 [검색을 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/t-srch-map.md#task-a1e7065a538d46c78a7d28676d880dfb).

