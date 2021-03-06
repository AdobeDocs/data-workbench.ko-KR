---
description: 이미지 레이어에 대한 개념 정보.
title: 이미지 레이어 정보
uuid: a8b00bda-c5b2-4f27-8c15-2d319b3bfa70
exl-id: c6d30747-70d2-4489-ad64-fd131e76a7a2
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 5%

---

# 이미지 레이어 정보{#about-imagery-layers}

이미지 레이어에 대한 개념 정보.

## 이미지 레이어 유형 {#section-891cbf61e8334690bd203a2bb9761b25}

Data Workbench에서 다음 유형의 이미지 레이어를 볼 수 있습니다.

* **[!UICONTROL Terrain image layer]:** 이러한 유형의 레이어는 지구의 지형 이미지를 표시하며, 여기에서 지리적 데이터를 표시할 수 있습니다. 의 지구본 시각화는 지형 이미지 레이어의 예입니다. [지형 이미지 레이어 작업](../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f)을 참조하십시오.

* **[!UICONTROL Element point layer]:** 이 유형의 레이어는 차원의 각 요소에 대해 전경에 한 점을 표시합니다. [요소 점 레이어 작업](../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-layers.md#concept-7c93c54552844a20bd6014ae8446b3fd)을 참조하십시오.

* **[!UICONTROL Vector layer]:** 이 유형의 레이어는 전구에서 벡터 데이터(라인 아트)를 표시합니다. [벡터 레이어를 사용한 작업](../../../home/c-get-started/c-im-layers/c-vctr-layers/c-vctr-layers.md#concept-a9b9cb7fc33b4aa5ae1646fab202dcc9)을 참조하십시오.

* **[!UICONTROL Presentation layer]**&#x200B;프레젠테이션 오버레이를 사용하여 시각화에 대해 주석을 달고 명확하게 합니다. 텍스트 설명선, 화살표, 이미지 및 색상 코딩을 추가하여 데이터를 강조 표시하여 명확히 한 다음 다른 사용자와 공유합니다.

Data Workbench에서 특정 분석 작업에 표시할 이러한 레이어 중 하나를 선택할 수 있습니다.

## Geography 프로필 레이어 {#section-d04ab9f1a8cd4c6580e48ce44ac51898}

[!DNL Geography] 프로필은 Profiles\Geography\Maps folder within the Data Workbench server installation directory에 저장된 기본 이미지 레이어 집합을 제공합니다.

* **[!UICONTROL Blue Marble 2km]** : 이 지형 이미지 레이어는 세계 3D 맵을 만듭니다. 이 그래프는 지구 시각화를 작업 공간에 추가할 때 표시됩니다. 이 레이어를 선택하지 않으면 글로브가 표시되지 않지만 다른 레이어는 계속 표시됩니다. [!DNL Blue Marble 2km.layer] 파일은 [!DNL Blue Marble 2km.tsi] 파일을 참조합니다.

* **[!UICONTROL Zip Points]** : 이 요소 점 레이어를 사용하면 미국 우편 번호를 사용하여 데이터 집합에 있는 위치를 매핑할 수 있습니다. [!DNL Zip Points.txt] 조회 파일(Adobe에서 제공)에는 모든 미국 ZIP 코드 목록과 각 ZIP 코드의 위도와 경도가 포함되어 있습니다. [!DNL Zip Points.layer] 파일은 [!DNL Zip Points.txt] 파일 및 [!DNL Zipcode.dim] 파일을 참조하며 전구에서 위치를 표시하는 데 필요한 구성 매개 변수를 포함합니다. 데이터 세트 내에서 정의한 ZIP 코드 차원( [!DNL Zipcode.dim])의 각 요소는 [!DNL Zip Points.txt] 조회 파일에서 해당 ZIP 코드에 대해 나열된 위도와 경도를 사용하여 전방에 매핑됩니다.

   차원 정의에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

* **[!UICONTROL Boundaries]:** 이 벡터 층은 호수와 섬들과 같은 지구의 자연적 특징들의 경계뿐만 아니라 국가들과 같은 주요 세계 정치적 경계를 제공합니다. [!DNL Boundaries.layer] 파일은 [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec] 및 [!DNL world boundaries.vec] 파일 중 하나 이상을 참조합니다.

* **[!UICONTROL IP Coordinates]** : 이 요소 점 계층은 동적 점을 사용하여 IP 주소를 사용하여 데이터 집합에 있는 위치를 매핑할 수 있도록 합니다. [!DNL IP Coordinates.layer] 파일은 좌표 차원( [!DNL Coordinates.dim])을 참조하고 방문자 지표를 지표로 지정하여 각 좌표에 대해 지구별점의 크기를 결정합니다.

설치 중인 [!UICONTROL NL Geography] 프로필 또는 기타 프로필에는 Adobe이 제공하거나 회사에서 만든 추가 이미지 레이어가 포함될 수 있습니다.

## 새 레이어 {#section-b5313773316c4e0fa748f7376a8e7f0b} 만들기

[!DNL Geography] 프로필에 포함된 적절한 유형의 레이어 파일을 Profiles\*profile name*\Maps 폴더로 복사한 다음 파일 이름을 적절하게 변경하여 새 이미지 레이어를 만들 수 있습니다. 새 레이어는 모두 다음 요구 사항을 충족해야 합니다.

* [!DNL .layer] 파일은 지원되는 레이어 형식 중 하나의 형식을 따라야 합니다.
* 필요한 경우 [!DNL .layer] 파일은 적절한 조회 및 차원 파일을 참조해야 합니다.
* 참조된 조회 파일도 Data Workbench 서버 설치 디렉터리 내에 저장해야 하며 경로가 [!DNL .layer] 파일에 정확하게 지정되어 있어야 합니다.

각 레이어 파일 유형 및 관련 파일의 형식 및 매개 변수에 대한 자세한 내용은 이 장의 해당 레이어 유형에 대한 섹션을 참조하십시오.
