---
description: 데이터 집합 구성 요소에 대한 개념적 정보입니다.
title: 데이터 세트 구성 요소
uuid: a5dde039-3b79-4543-9953-995eefc73b5f
exl-id: 6be625c5-1a2e-4b0d-9c34-5f3baec4ba81
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---

# 데이터 세트 구성 요소{#dataset-components}

{{eol}}

데이터 집합 구성 요소에 대한 개념적 정보입니다.

다음 그림은 노드가 데이터 집합의 로그 소스, 필드, 변형 및 확장 차원을 나타내는 종속성 맵을 보여줍니다.

![](assets/vis_DependencyMap.png)

* 노란색 녹색 노드는 데이터 집합에 정의된 하나 이상의 로그 소스 또는 필터(예: 로그 항목 조건)를 나타냅니다.

   * 로그 소스의 노드는 항상 맵에서 왼쪽으로 가장 멀리 표시됩니다. 데이터 세트에 단일 로그 소스가 있는 경우 맵에 로그 소스가 표시됩니다. *로그 소스 이름*. 데이터 세트에 여러 로그 소스가 있는 경우 맵이 표시됩니다 *number* 로그 소스. 여기서 number 는 로그 소스의 수입니다. 예를 들어 데이터 세트에 3개의 로그 소스가 있는 경우 맵에 3개의 로그 소스가 표시됩니다.

   * 맵에는 각 항목에 대해 하나의 로그 항목 조건 노드가 표시됩니다 [!DNL log processing dataset include] 파일에 변환용 로그 항목 조건 노드가 하나만 있어야 합니다(에 정의된 경우). [!DNL Transformation.cfg] 파일)에 액세스할 수 없습니다. 로그 항목 조건이 비어 있으면 맵에 표시되지 않습니다.

* 회색 노드는 [!DNL Log Processing.cfg] 또는 [!DNL Log Processing include] 파일.

* 파란색 노드는 변형을 나타냅니다.
* 녹색 노드는 확장된 차원을 나타냅니다.

>[!NOTE]
>
>프로필의 데이터 세트 폴더에 파일이 포함되어 있는 경우 [!DNL Insight Transform.cfg]에 대한 종속성 맵은 변환에 사용하기 위해 정의된 로그 소스, 변환 및 내보내기를 표시합니다. 변형에 대한 자세한 내용은 *데이터 집합 구성 안내서*.

포함을 활성화할 때 [!DNL File Blocks] 표시 옵션을 선택하면 맵에는 하나의 데이터 세트 구성 파일에 정의된 모든 변환에 대한 단일 파란색 노드와 하나의 데이터 세트 구성 파일에 정의된 모든 확장 차원에 대한 단일 녹색 노드가 표시됩니다. 이 표시 옵션에 대한 자세한 내용은 [파일 블록 작업](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wkg-file-blocks.md#concept-3652bbabfbd34449a5f842d8aa598efc).
