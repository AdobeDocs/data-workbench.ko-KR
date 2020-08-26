---
description: 이미지 레이어에 대한 개념 정보
solution: Analytics
title: 이미지 레이어 정보
topic: Data workbench
uuid: a8b00bda-c5b2-4f27-8c15-2d319b3bfa70
translation-type: tm+mt
source-git-commit: f4b37f50b115a1e1d2c9d000897a8fa47b03b233
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 5%

---


# 이미지 레이어 정보{#about-imagery-layers}

이미지 레이어에 대한 개념 정보

## 이미지 레이어 유형 {#section-891cbf61e8334690bd203a2bb9761b25}

Data Workbench에서 다음과 같은 유형의 이미지 레이어를 볼 수 있습니다.

* **[!UICONTROL Terrain image layer]:** 이러한 유형의 레이어는 지구의 지형을 보여주며, 그 위에 지리적 데이터를 표시할 수 있다. 지구별 시각화는 지형 이미지 레이어의 예입니다. See [Working with Terrain Image Layers](../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f).

* **[!UICONTROL Element point layer]:** 이러한 유형의 레이어는 차원의 각 요소에 대해 지구 상의 한 점을 표시합니다. See [Working with Element Point Layers](../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-layers.md#concept-7c93c54552844a20bd6014ae8446b3fd).

* **[!UICONTROL Vector layer]:** 이러한 유형의 레이어는 벡터의 데이터(라인 아트)를 전세계에 표시합니다. See [Working with Vector Layers](../../../home/c-get-started/c-im-layers/c-vctr-layers/c-vctr-layers.md#concept-a9b9cb7fc33b4aa5ae1646fab202dcc9).

* **[!UICONTROL Presentation layer]**&#x200B;프레젠테이션 오버레이를 사용하여 시각화에 대해 주석을 달고 명확하게 합니다. 텍스트 설명선, 화살표, 이미지 및 색상 코딩을 추가하여 데이터를 강조 표시하여 명확히 한 다음 다른 사용자와 공유합니다.

Data Workbench에서 특정 분석 작업에 표시할 이러한 레이어 중 하나를 선택할 수 있습니다.

## 지리 프로필 레이어 {#section-d04ab9f1a8cd4c6580e48ce44ac51898}

이 [!DNL Geography] 프로필은 Profiles\Geography\Maps folder within the Data Workbench server installation directory폴더에 저장되는 기본 이미지 레이어 세트를 제공합니다.

* **[!UICONTROL Blue Marble 2km]:** 이 지형 이미지 레이어는 세계 3D 지도를 만듭니다. 이 지도는 지구 시각화를 작업 공간에 추가할 때 표시됩니다. 이 레이어를 선택하지 않으면 지구본이 보이지 않지만 다른 레이어는 계속 표시됩니다. 파일이 [!DNL Blue Marble 2km.layer] 파일을 참조합니다 [!DNL Blue Marble 2km.tsi] .

* **[!UICONTROL Zip Points]:** 이 요소 포인트 레이어를 사용하면 미국 우편 번호를 사용하여 데이터 세트에 있는 위치를 매핑할 수 있습니다. 조회 파일(Adobe에서 제공)에는 모든 미국 ZIP 코드 목록과 각 ZIP 코드의 위도 및 경도 목록이 포함되어 있습니다. [!DNL Zip Points.txt] 이 [!DNL Zip Points.layer] 파일은 [!DNL Zip Points.txt] 파일과 [!DNL Zipcode.dim] 파일을 참조하며 지구 상의 위치를 표시하는 데 필요한 구성 매개 변수를 포함합니다. 데이터 세트 내에서 정의하는 ZIP 코드 차원( [!DNL Zipcode.dim])의 각 요소는 [!DNL Zip Points.txt] 조회 파일의 해당 ZIP 코드에 대해 나열된 위도 및 경도를 사용하여 지구 위에 매핑됩니다.

   차원 정의에 대한 자세한 내용은 데이터 세트 *구성 안내서를 참조하십시오*.

* **[!UICONTROL Boundaries]:** 이 벡터 레이어는 국가 등의 주요 세계 정치적 경계는 물론 호수와 섬들과 같은 지구의 자연 물리적 기능의 경계를 제공합니다. 하나 이상의 [!DNL Boundaries.layer] 파일 [!DNL mwcoast.vec], [!DNL mwisland.vec][!DNL mwlake.vec], Facebook,파일 [!DNL mwnation.vec]및 [!DNL mwriver.vec][!DNL mwstate.vec][!DNL US states.vec][!DNL world boundaries.vec] 를 참조합니다.

* **[!UICONTROL IP Coordinates]:** 이 요소 포인트 레이어는 동적 점을 사용하여 IP 주소를 사용하여 데이터 세트에 있는 위치를 매핑할 수 있도록 합니다. 이 [!DNL IP Coordinates.layer] 파일은 좌표 차원( [!DNL Coordinates.dim])을 참조하고 방문자 지표를 지표로 지정하여 각 좌표에 대한 지구별 포인트 크기를 결정합니다.

설치 내의 [!UICONTROL NL Geography] 프로필 또는 기타 프로필에는 Adobe이 제공하거나 회사가 만든 추가 이미지 레이어가 포함될 수 있습니다.

## Create a new layer {#section-b5313773316c4e0fa748f7376a8e7f0b}

프로필에 포함된 적절한 유형의 레이어 파일을 Profiles\*profile name*\Maps 폴더에 복사한 다음 파일의 이름을 변경하고 원하는 파일을 편집하여 새로운 이미지 레이어를 만들 수 있습니다. [!DNL Geography] 모든 새 레이어는 다음 요구 사항을 충족해야 합니다.

* 이 [!DNL .layer] 파일은 지원되는 레이어 유형 중 하나의 형식을 따라야 합니다.
* 필요한 경우 해당 조회 및 치수 파일을 [!DNL .layer] 참조해야 합니다.
* 또한 참조된 조회 파일은 Data Workbench 서버 설치 디렉터리 내에 저장되어야 하며 파일의 경로를 정확하게 지정해야 [!DNL .layer] 합니다.

각 유형의 레이어 파일 및 관련 파일의 포맷 및 매개 변수에 대한 자세한 내용은 해당 레이어 유형에 대한 이 장의 섹션을 참조하십시오.
