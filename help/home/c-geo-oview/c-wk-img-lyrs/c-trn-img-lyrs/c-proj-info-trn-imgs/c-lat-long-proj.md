---
description: Terrain Images.cfg 파일의 위도-경도 투영 형식(LatLonProjection)은 위도와 경도에 대한 네 개의 매개 변수로 정의됩니다.
title: 위도-경도 예측
uuid: 0ac947d6-3cd6-4272-96ae-456d2835e63f
exl-id: 67ebc7a8-3046-4524-b3a0-0b6da2f235fc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 2%

---

# 위도-경도 예측{#latitude-longitude-projections}

{{eol}}

Terrain Images.cfg 파일의 위도-경도 투영 형식(LatLonProjection)은 위도와 경도에 대한 네 개의 매개 변수로 정의됩니다.

투영되지 않은 이미지(투영되지 않은 원시 비트맵 및 일반 이미지, 투영되지 않은 이미지)에 대한 LatLonProjection을 지정하려면 [!DNL Terrain Images.cfg] data workbench의 창. 자세한 내용은 [투영되지 않은 이미지에 대한 LatLonProjection을 지정하려면](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a).

포함된 투영 정보가 있는 이미지에 대한 LatLonProjection을 지정하려면 [!DNL Terrain Images.cfg] 메모장과 같은 텍스트 편집기의 파일에서 투영 정보 매개 변수를 &quot;LatLonProjection&quot;으로 설정하고 LatLonProjection에 대한 설정을 추가합니다. 자세한 내용은 [포함된 투영 정보 내의 이미지에 대한 LatLonProjection을 지정하려면...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1).

* [투영되지 않은 이미지에 대한 LatLonProjection 지정하기](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)
* [포함된 투영 정보 내의 이미지에 대한 LatLonProjection을 지정하는 방법..](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1)

## 투영되지 않은 이미지에 대한 LatLonProjection 지정하기 {#section-26554eefe645481faba68396fa13756a}

1. 를 엽니다. [!DNL Terrain Images.cfg] data workbench에서 파일을 추가하고 다음과 같이 지형 이미지 레이어 소스를 추가합니다. [지형 이미지 레이어를 정의하려면](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf).

1. 다음 매개변수 테이블을 안내서로 사용하여 투영 정보 매개변수를 편집합니다.

   | 매개 변수 | 설명 |
   |---|---|
   | Lat0 | 영상의 위쪽 가장자리의 위도인 도(도)로 90은 북극이고 -90은 남극이다. |
   | Lat1 | 이미지 하단 가장자리의 위도입니다. |
   | Lon0 | 영상의 왼쪽 가장자리 경도로서, 양수가 동이고 음수가 서쪽입니다. |
   | Lon1 | 이미지의 오른쪽 가장자리 경도입니다. |

1. 마우스 오른쪽 단추를 클릭하여 파일을 저장합니다 **[!UICONTROL (modified)]** 창 상단에서 **[!UICONTROL Save]**.

1. 로컬에서 변경한 Data Workbench 서버 시스템을 저장하려면 [!DNL Server Files Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Terrain Images.cfg] 에서 [!DNL Temp] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## 포함된 투영 정보 내의 이미지에 대한 LatLonProjection 지정하기 {#section-174f4e00fad84a7ca0c995423dd37ae1}

1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 서버 이름 열의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Terrain Images.cfg]를 클릭한 다음 **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Terrain Images.cfg].

1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 다음 [!DNL Terrain Images.cfg] 파일이 메모장 창에 나타납니다.

1. 다음 샘플 파일 조각을 안내서로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 대로 지정해야 합니다. 매개 변수에 대한 설명은 이전 절차의 LatLonProjection 매개 변수 테이블을 참조하십시오.

   ```
   Projection Info = LatLonProjection: 
     Lat0 = double: 90
     Lat1 = double: -90
     Lon0 = double: -180
     Lon1 = double: 180
   ```
