---
description: Geography 프로필 레이어, 이미지 레이어 유형 및 새 레이어 만들기에 대한 개념 정보
title: 이미지 레이어 이해
uuid: 8f4618bf-d8bd-4d21-a29e-ab2871d781ca
exl-id: ffe084ec-db8b-46f4-8266-0f1b771b3349
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 1%

---

# 이미지 레이어 이해{#understanding-imagery-layers}

Geography 프로필 레이어, 이미지 레이어 유형 및 새 레이어 만들기에 대한 개념 정보

## 이미지 레이어 유형 {#section-ce25364651a04cd1b83f9ac7c231fa41}

Data Workbench [!DNL Geography] 를 사용하면 Data Workbench에서 다음 유형의 이미지 레이어를 볼 수 있습니다.

* **지형 이미지 레이어:**  이 유형의 레이어는 지구의 지형 이미지를 표시하며, 그 위에 지리적 데이터를 표시할 수 있습니다. Data Workbench의 전역 시각화는 지형 이미지 레이어의 예입니다. [지형 이미지 레이어 작업](../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf)을 참조하십시오.

* **요소 점 레이어:**  이 유형의 레이어는 차원의 각 요소에 대해 지구본에 한 점을 표시합니다. [요소 점 레이어 작업](../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs.md#concept-52b3262ab4e042a18956be8809638af9)을 참조하십시오.

* **벡터 레이어:** 이 유형의 레이어는 전구에서 벡터 데이터(라인 아트)를 표시합니다. [벡터 레이어를 사용한 작업](../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-wk-vctr-lyrs.md#concept-a2c9e8155f554cbe96ee3aaf44f2d620)을 참조하십시오.

Data Workbench에서 특정 분석 작업에 표시할 이러한 레이어 중 하나를 선택할 수 있습니다.

## Geography 프로필 레이어 {#section-4d9fb9b357764493a4d97d2b4068bb67}

[!DNL Geography] 프로필은 Profiles\Geography\Maps folder within the data workbench server installation directory에 저장된 기본 이미지 레이어 집합을 제공합니다.

* **블루 마블 2km:** 이 지형 이미지 레이어는 세계 3차원 맵을 만듭니다. 이 맵은 지구 시각화를 작업 공간에 추가할 때 표시됩니다. 이 레이어를 선택하지 않으면 글로브가 표시되지 않지만 다른 레이어는 계속 표시됩니다. [!DNL Blue Marble 2km.layer] 파일은 [!DNL Blue Marble 2km.tsi] 파일을 참조합니다.

   지구 시각화 작업에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.

* **zip 지점:** 이 요소 포인트 레이어를 사용하면 미국 우편 번호를 사용하여 데이터 집합에 있는 위치를 매핑할 수 있습니다. [!DNL Zip Points.txt] 조회 파일(Adobe에서 제공)에는 모든 미국 ZIP 코드 목록과 각 ZIP 코드의 위도와 경도가 포함되어 있습니다. [!DNL Zip Points.layer] 파일은 [!DNL Zip Points.txt] 파일 및 [!DNL Zipcode.dim] 파일을 참조하며 전구에서 위치를 표시하는 데 필요한 구성 매개 변수를 포함합니다. 데이터 세트 내에서 정의한 ZIP 코드 차원( [!DNL Zipcode.dim])의 각 요소는 [!DNL Zip Points.txt] 조회 파일에서 해당 ZIP 코드에 대해 나열된 위도와 경도를 사용하여 전방에 매핑됩니다.

   차원 정의에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

* **경계:** 이 벡터 층은 호수와 섬들과 같은 지구의 자연적 특징들의 경계뿐만 아니라 국가들과 같은 주요 세계 정치적 경계를 제공합니다. [!DNL Boundaries.layer] 파일은 [!DNL mwcoast.vec], [!DNL mwisland.vec], [!DNL mwlake.vec], [!DNL mwnation.vec], [!DNL mwriver.vec], [!DNL mwstate.vec], [!DNL US states.vec] 및 [!DNL world boundaries.vec] 파일 중 하나 이상을 참조합니다.

* **IP 좌표:**  이 요소 점 계층은 동적 점을 사용하여 IP 주소를 사용하여 데이터 집합에 있는 위치를 매핑할 수 있도록 합니다. [!DNL IP Coordinates.layer] 파일은 좌표 차원( [!DNL Coordinates.dim])을 참조하고 방문자 지표를 지표로 지정하여 각 좌표에 대해 지구별점의 크기를 결정합니다.

설치 중인 [!DNL Geography] 프로필 또는 기타 프로필에는 Adobe이 제공하거나 회사에서 만든 추가 이미지 레이어가 포함될 수 있습니다.

## 새 레이어 만들기 {#section-dc5a2f31d5fc46f58b865b9bb89fcfd4}

[!DNL Geography] 프로필에 포함된 적절한 유형의 레이어 파일을 Profiles\*profile name*\Maps 폴더로 복사한 다음 파일 이름을 적절하게 변경하여 새 이미지 레이어를 만들 수 있습니다. 새 레이어는 모두 다음 요구 사항을 충족해야 합니다.

* [!DNL .layer] 파일은 지원되는 레이어 형식 중 하나의 형식을 따라야 합니다.
* 필요한 경우 [!DNL .layer] 파일은 적절한 조회 및 차원 파일을 참조해야 합니다.
* 참조된 조회 파일도 Data Workbench 서버 설치 디렉토리 내에 저장해야 하며 경로가 [!DNL .layer] 파일에 정확하게 지정되어 있어야 합니다.

각 레이어 파일 유형 및 관련 파일의 형식 및 매개 변수에 대한 자세한 내용은 이 장의 해당 레이어 유형에 대한 섹션을 참조하십시오.
