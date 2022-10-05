---
description: 조회 파일을 참조하여 위도 및 경도 데이터를 얻는 요소 점 레이어를 만들면 조회 파일에서 각 요소 및 연관된 위도와 경도를 검색하여 점의 위치를 얻습니다.
title: 조회 파일을 참조하는 요소 점 레이어 정의
uuid: 99d08d43-bdbb-42e1-927a-edf320686c79
exl-id: b6928821-c825-43e2-8c7b-2ce0f49aa67e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 4%

---

# 조회 파일을 참조하는 요소 점 레이어 정의{#defining-element-point-layers-referencing-lookup-files}

{{eol}}

조회 파일을 참조하여 위도 및 경도 데이터를 얻는 요소 점 레이어를 만들면 조회 파일에서 각 요소 및 연관된 위도와 경도를 검색하여 점의 위치를 얻습니다.

조회 파일을 사용하는 대신 [!DNL Dynamic Points] 차원의 각 요소 이름에 위치의 위도와 경도를 포함하는 기능입니다. 자세한 내용은 [동적 점을 사용하여 요소 점 레이어 정의](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

조회 파일을 참조하는 요소 점 레이어를 정의하려면 다음을 생성하거나 이미 사용 가능해야 합니다.

* **차원** 에 정의됨 [!DNL Transformation.cfg] 파일 또는 변형 데이터 세트에 파일이 포함됩니다. 변환 구성 파일에 대한 자세한 내용은 *데이터 집합 구성 안내서*.

* **조회 파일** 각 데이터 포인트를 플롯하는 데 사용되는 데이터를 포함합니다. 이 파일은 각 데이터 포인트에 대해 최소 3개의 데이터 열을 포함해야 합니다. 키, 경도 및 위도입니다. 조회 파일의 필수 형식에 대한 자세한 내용은 [요소 점 조회 파일 형식](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lkp-file-frmt.md#concept-c059121019ea4dbcb1c17129567f4121).

* **레이어 파일** 조회 파일의 위치를 지정하고 조회 파일의 키, 경도 및 위도 열 이름뿐만 아니라 관련 차원과 지표를 식별합니다. 레이어 파일의 필수 형식에 대한 자세한 내용은 [요소 점 레이어 파일 형식](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981).

>[!NOTE]
>
>다음 [!DNL Zip Points.layer] 파일, [!DNL Geography] 프로파일, 은 [!DNL Zipcode.dim] 파일, [!DNL Sessions.metric] 파일, [!DNL Zip Points.txt] 조회 파일과 조회 파일에 있는 키, 경도, 위도 및 이름 열의 이름.
