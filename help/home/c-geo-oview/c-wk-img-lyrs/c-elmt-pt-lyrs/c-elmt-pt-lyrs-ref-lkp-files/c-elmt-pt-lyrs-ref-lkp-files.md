---
description: 조회 파일을 참조하여 위도 및 경도 데이터를 얻는 요소 점 레이어를 만들면 조회 파일에서 각 요소 및 연관된 위도와 경도를 검색하여 점의 위치를 얻습니다.
title: 조회 파일을 참조하는 요소 점 레이어 정의
uuid: 99d08d43-bdbb-42e1-927a-edf320686c79
exl-id: b6928821-c825-43e2-8c7b-2ce0f49aa67e
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 4%

---

# 조회 파일을 참조하는 요소 점 레이어 정의{#defining-element-point-layers-referencing-lookup-files}

조회 파일을 참조하여 위도 및 경도 데이터를 얻는 요소 점 레이어를 만들면 조회 파일에서 각 요소 및 연관된 위도와 경도를 검색하여 점의 위치를 얻습니다.

조회 파일을 사용하는 대신 [!DNL Dynamic Points] 기능을 사용하여 차원의 각 요소 이름에 위치의 위도와 경도를 포함할 수 있습니다. [동적 점을 사용하여 요소 점 레이어 정의](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3)를 참조하십시오.

조회 파일을 참조하는 요소 점 레이어를 정의하려면 다음을 생성하거나 이미 사용 가능해야 합니다.

* **파일** 또는 변형 데이터 세트에  [!DNL Transformation.cfg] 정의된 차원은 파일을 포함합니다. 변형 구성 파일에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

* **각** 데이터 포인트를 플롯하는 데 사용되는 데이터가 포함된 조회 필터입니다. 이 파일은 각 데이터 포인트에 대해 최소 3개의 데이터 열을 포함해야 합니다.키, 경도 및 위도입니다. 조회 파일의 필수 형식에 대한 자세한 내용은 [요소 점 조회 파일 형식](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lkp-file-frmt.md#concept-c059121019ea4dbcb1c17129567f4121)을 참조하십시오.

* **조회 파일** 의 위치를 지정하고 조회 파일의 키, 경도 및 위도 열 이름과 관련 차원 및 지표를 식별하는 레이어 파일입니다. 레이어 파일의 필수 형식에 대한 자세한 내용은 [요소 점 레이어 파일 형식](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981)을 참조하십시오.

>[!NOTE]
>
>[!DNL Geography] 프로필과 함께 제공되는 [!DNL Zip Points.layer] 파일은 [!DNL Zipcode.dim] 파일, [!DNL Sessions.metric] 파일, [!DNL Zip Points.txt] 조회 파일 및 조회 파일의 키, 경도, 위도 및 이름 열의 이름을 식별하는 요소 포인트 레이어입니다.
