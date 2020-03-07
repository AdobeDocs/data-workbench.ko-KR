---
description: 위도 및 경도 데이터를 얻기 위해 조회 파일을 참조하는 요소 포인트 레이어를 만들 때 조회 파일에서 각 요소 및 관련 위도와 경도를 검색하여 해당 위치의 위치를 얻습니다.
solution: Analytics
title: 조회 파일을 참조하는 요소 포인트 레이어 정의
topic: Data workbench
uuid: 99d08d43-bdbb-42e1-927a-edf320686c79
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 조회 파일을 참조하는 요소 포인트 레이어 정의{#defining-element-point-layers-referencing-lookup-files}

위도 및 경도 데이터를 얻기 위해 조회 파일을 참조하는 요소 포인트 레이어를 만들 때 조회 파일에서 각 요소 및 관련 위도와 경도를 검색하여 해당 위치의 위치를 얻습니다.

조회 파일을 사용하는 대신 위치의 위도와 경도를 치수의 각 요소 이름에 포함하는 기능을 사용할 수 있습니다. [!DNL Dynamic Points] 동적 [포인트를 사용하여 요소 점 레이어 정의를 참조하십시오](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

조회 파일을 참조하는 요소 포인트 레이어를 정의하려면 다음을 만들거나 이미 사용할 수 있어야 합니다.

* **파일 또는 변형 데이터 세트에** 정의된 차원은 [!DNL Transformation.cfg] 파일을 포함합니다. 변형 구성 파일에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.

* **각 데이터 포인트를 플롯하는 데 사용되는 데이터가 들어 있는 조회 파일** . 이 파일에는 각 데이터 포인트에 대해 최소 3개의 데이터 열이 있어야 합니다.키, 경도 및 위도 조회 파일의 필수 형식에 대한 자세한 내용은 요소 포인트 조회 [파일 형식을 참조하십시오](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lkp-file-frmt.md#concept-c059121019ea4dbcb1c17129567f4121).

* **조회 파일의 위치를 지정하고 조회 파일의 키, 경도 및 위도 열 이름뿐만 아니라 관련 차원과 지표를 식별하는 레이어 파일입니다** . 레이어 파일의 필수 형식에 대한 자세한 내용은 요소 점 레이어 [파일 형식을 참조하십시오](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981).

>[!NOTE]
>
>프로파일과 함께 제공되는 [!DNL Zip Points.layer] 파일은 [!DNL Geography] [!DNL Zipcode.dim] [!DNL Sessions.metric] [!DNL Zip Points.txt] 파일, 파일, 조회 파일, 조회 파일, 조회 파일의 키, 경도, 위도 및 이름 열의 이름을 식별하는 요소 포인트 레이어입니다.

