---
description: 데이터 세트 구성 요소에 대한 개념 정보입니다.
solution: Analytics
title: 데이터 세트 구성 요소
topic: Data workbench
uuid: a5dde039-3b79-4543-9953-995eefc73b5f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 세트 구성 요소{#dataset-components}

데이터 세트 구성 요소에 대한 개념 정보입니다.

다음 그림은 노드가 데이터 세트의 로그 소스, 필드, 변형 및 확장 크기를 나타내는 종속성 맵을 보여줍니다.

![](assets/vis_DependencyMap.png)

* 노란색-녹색 노드는 데이터 세트에 정의된 하나 이상의 로그 소스 또는 필터(예: 로그 항목 조건)를 나타냅니다.

   * 로그 소스의 노드는 항상 맵의 왼쪽에서 가장 멀리 표시됩니다. 데이터 세트에 단일 로그 소스가 있으면 맵에 로그 소스가 표시됩니다. *로그 소스 이름*. 데이터 세트에 여러 개의 로그 소스가 있는 경우 맵에는 로그 소스 *수가* 표시됩니다. 로그 소스 수는 로그 소스 수입니다. 예를 들어 데이터 세트에 3개의 로그 소스가 있는 경우 맵에 3개의 로그 소스가 표시됩니다.

   * 맵에는 각 [!DNL log processing dataset include] 파일에 대해 하나의 로그 항목 조건 노드가 표시되지만 변환에는 하나의 로그 항목 조건 노드만 표시됩니다( [!DNL Transformation.cfg] 파일에 정의된 경우). 로그 항목 조건이 비어 있으면 맵에 표시되지 않습니다.

* 회색 노드는 [!DNL Log Processing.cfg] 또는 [!DNL Log Processing include] 파일의 필드 매개 변수에 나열된 필드를 나타냅니다.

* 파란색 노드는 변환을 나타냅니다.
* 녹색 노드는 확장 차원을 나타냅니다.

>[!NOTE]
>
>프로필의 데이터 세트 폴더에 파일이 포함되어 [!DNL Insight Transform.cfg]있으면 종속성 맵은 Transform에 사용하기 위해 정의된 로그 소스, 변형 및 내보내기 기능을 표시합니다. 변형에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.

표시 포함 옵션을 활성화하면 맵은 하나의 데이터 세트 구성 파일에 정의된 모든 변환에 대해 단일 파란색 노드를 표시하고 하나의 데이터 세트 구성 파일에 정의된 모든 확장 차원에 대해 하나의 녹색 노드를 표시합니다. [!DNL File Blocks] 이 표시 옵션에 대한 자세한 내용은 파일 블록 [작업을 참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wkg-file-blocks.md#concept-3652bbabfbd34449a5f842d8aa598efc).
