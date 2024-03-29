---
description: 쿼리 모델 구성 요소에 대한 개념적 정보입니다.
title: 쿼리 모델 구성 요소
uuid: 708fab0b-dc10-4306-b410-49268069ac3b
exl-id: 1f5d0a3a-6647-4762-ab20-9d80e467d48f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# 쿼리 모델 구성 요소{#query-model-components}

{{eol}}

쿼리 모델 구성 요소에 대한 개념적 정보입니다.

다음 그림은 Dimension의 지표, 파생 차원 및 프로필 내의, 지표 및 필터 폴더에 정의된 필터와 이러한 지표와 관련된 데이터 세트에 정의된 확장 차원을 나타내는 종속성 맵을 보여줍니다.

![](assets/vis_DependencyMap_QueryModel.png)

* 노란색-녹색 노드는 필터를 나타냅니다.
* 자주색 노드는 지표를 나타냅니다.
* 파란색 녹색 노드는 파생된 차원을 나타냅니다.
* 녹색 노드는 확장된 차원(데이터 세트에 정의됨)을 나타냅니다.
* 빨간색 노드는 끊어지거나 순환 종속성 또는 기타 오류가 있는 지표, 파생 차원 또는 필터를 나타냅니다.

>[!NOTE]
>
>종속성 맵은 순환 종속성을 수용하도록 설계되었으므로 순환 종속성에 관련된 노드가 맵에 제대로 표시되지 않을 수 있습니다. 에 &quot;순환 종속성&quot;을 입력하여 순환 종속성을 검색할 수 있습니다 [!DNL Search] 텍스트 상자 에 대한 자세한 정보 [!DNL Search] 기능 [맵에서 검색](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/t-srch-map.md#task-a1e7065a538d46c78a7d28676d880dfb).
