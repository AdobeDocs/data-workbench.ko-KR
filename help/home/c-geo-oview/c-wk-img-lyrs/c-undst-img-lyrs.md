---
description: 지리적 위치 프로파일 레이어, 이미지 레이어 유형 및 새 레이어 만들기에 대한 개념 정보입니다.
solution: Analytics
title: 이미지 레이어 이해
topic: Data workbench
uuid: 8f4618bf-d8bd-4d21-a29e-ab2871d781ca
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 이미지 레이어 이해{#understanding-imagery-layers}

지리적 위치 프로파일 레이어, 이미지 레이어 유형 및 새 레이어 만들기에 대한 개념 정보입니다.

## 이미지 레이어 유형 {#section-ce25364651a04cd1b83f9ac7c231fa41}

데이터 워크벤치를 [!DNL Geography] 사용하면 데이터 워크벤치에서 다음 유형의 이미지 레이어를 볼 수 있습니다.

* **지형 이미지 레이어:** 이러한 유형의 레이어는 지구의 지형 이미지를 표시합니다. 이 이미지는 지리적 데이터를 표시할 수 있습니다. 데이터 워크벤치의 지구 시각화는 지형 이미지 레이어의 예입니다. 지형 [이미지 레이어 작업을 참조하십시오](../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf).

* **요소 점 레이어:** 이 유형의 레이어는 치수의 각 요소에 대해 지구상 한 점을 표시합니다. 요소 [점 레이어 작업을 참조하십시오](../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs.md#concept-52b3262ab4e042a18956be8809638af9).

* **벡터 레이어:** 이러한 유형의 레이어는 지구에서의 벡터 데이터(라인 아트)를 표시합니다. 벡터 [레이어 작업을 참조하십시오](../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-wk-vctr-lyrs.md#concept-a2c9e8155f554cbe96ee3aaf44f2d620).

데이터 워크벤치에서는 특정 분석 작업에 표시할 이러한 레이어 중 하나를 선택할 수 있습니다.

## 지리 프로필 레이어 {#section-4d9fb9b357764493a4d97d2b4068bb67}

이 [!DNL Geography] 프로파일은 Profiles\Geography\Maps folder within the data workbench server installation directory폴더에 저장되는 기본 이미지 레이어 세트를 제공합니다.

* **블루 마블 2km:** 이 지형 이미지 레이어는 3D 지도를 만듭니다. 이 맵은 작업 영역에 지구 시각화를 추가할 때 표시됩니다. 이 레이어를 선택하지 않으면 구형은 보이지 않지만 다른 레이어는 계속 표시됩니다. 파일이 파일을 [!DNL Blue Marble 2km.layer] 참조합니다 [!DNL Blue Marble 2km.tsi] .

   지구 시각화 작업에 대한 자세한 내용은 데이터 워크벤치 *사용 안내서를 참조하십시오*.

* **우편 번호:** 이 요소 포인트 레이어를 사용하면 미국 우편 번호를 사용하여 데이터 세트에 있는 위치를 매핑할 수 있습니다. 조회 파일(Adobe에서 제공)에는 모든 미국 ZIP 코드 목록과 각 ZIP 코드의 위도 및 경도 목록이 포함되어 있습니다. [!DNL Zip Points.txt] 이 [!DNL Zip Points.layer] 파일은 [!DNL Zip Points.txt] 파일 및 [!DNL Zipcode.dim] 파일을 참조하며 지구에서의 위치를 표시하는 데 필요한 구성 매개 변수를 포함합니다. 데이터 세트 내에서 정의하는 ZIP 코드 차원( [!DNL Zipcode.dim])의 각 요소는 [!DNL Zip Points.txt] 조회 파일의 해당 ZIP 코드에 대해 나열된 위도 및 경도를 사용하여 지구 전체에 매핑됩니다.

   차원 정의에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오.*

* **경계:** 이 벡터 레이어는 국가 같은 주요 세계 정치적 경계는 물론 호수와 섬들과 같은 지구의 자연 물리적 기능의 경계를 제공합니다. 하나 이상의 [!DNL Boundaries.layer] 파일, [!DNL mwcoast.vec][!DNL mwisland.vec]파일, [!DNL mwlake.vec]파일, [!DNL mwnation.vec]파일, [!DNL mwriver.vec][!DNL mwstate.vec][!DNL US states.vec][!DNL world boundaries.vec] 파일 및 파일 참조

* **IP 좌표:** 이 요소 포인트 레이어는 동적 포인트를 사용하여 IP 주소를 사용하여 데이터 세트에 있는 위치를 매핑할 수 있도록 합니다. 이 [!DNL IP Coordinates.layer] 파일은 좌표 차원( [!DNL Coordinates.dim])을 참조하고 방문자 지표를 지표로 지정하여 각 좌표에 대한 지구별 포인트 크기를 결정합니다.

사용자의 [!DNL Geography] 프로필이나 설치 내의 다른 프로필에는 Adobe에서 제공한 추가 이미지 레이어 또는 회사가 만든 이미지 레이어가 포함될 수 있습니다.

## 새 레이어 만들기 {#section-dc5a2f31d5fc46f58b865b9bb89fcfd4}

프로파일에 포함된 적절한 유형의 레이어 파일을 Profiles\*profile name*\Maps 폴더에 복사한 다음 파일 이름을 변경하고 원하는 대로 편집하여 새로운 이미지 레이어를 만들 수 있습니다. [!DNL Geography] 모든 새 레이어는 다음 요구 사항을 충족해야 합니다.

* 이 [!DNL .layer] 파일은 지원되는 레이어 유형 중 하나의 형식을 따라야 합니다.
* 필요한 경우 [!DNL .layer] 파일은 적절한 조회 및 차원 파일을 참조해야 합니다.
* 참조된 조회 파일도 데이터 워크벤치 서버 설치 디렉토리 내에 저장해야 하며 [!DNL .layer] 파일에 해당 경로를 정확하게 지정해야 합니다.

각 유형의 레이어 파일 및 관련 파일의 형식 및 매개 변수에 대한 자세한 내용은 이 장의 해당 레이어 유형에 대한 섹션을 참조하십시오.
