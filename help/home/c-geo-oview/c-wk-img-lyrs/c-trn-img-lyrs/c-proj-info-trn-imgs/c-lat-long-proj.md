---
description: Terrain Images.cfg 파일의 위도-경도 투영 형식(LatLonProjection)은 위도와 경도에 대한 네 개의 매개 변수로 정의됩니다.
title: 위도-경도 예측
uuid: 0ac947d6-3cd6-4272-96ae-456d2835e63f
exl-id: 67ebc7a8-3046-4524-b3a0-0b6da2f235fc
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 2%

---

# 위도-경도 예측{#latitude-longitude-projections}

Terrain Images.cfg 파일의 위도-경도 투영 형식(LatLonProjection)은 위도와 경도에 대한 네 개의 매개 변수로 정의됩니다.

투영되지 않은 이미지(투영되지 않은 원시 비트맵 및 일반 이미지, 투영되지 않은 이미지)에 대한 LatLonProjection을 지정하려면 Data Workbench의 [!DNL Terrain Images.cfg] 창 내에 LatLonProjection에 대한 설정을 입력할 수 있습니다. 투영되지 않은 이미지에 대한 [LatLonProjection을 지정하려면](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)를 참조하십시오.

포함된 투영 정보가 있는 이미지의 LatLonProjection을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 &quot;LatLonProjection&quot;으로 설정하고 LatLonProjection에 대한 설정을 추가해야 합니다. 포함된 투영 정보 내의 이미지에 대한 LatLonProjection을 지정하려면 [를 참조하십시오.](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1).

* [투영되지 않은 이미지에 대한 LatLonProjection 지정하기](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)
* [포함된 투영 정보 내의 이미지에 대한 LatLonProjection을 지정하는 방법..](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1)

## 투영되지 않은 이미지에 대한 LatLonProjection을 지정하려면 {#section-26554eefe645481faba68396fa13756a}

1. Data Workbench에서 [!DNL Terrain Images.cfg] 파일을 열고 [지형 이미지 레이어를 정의하려면 ](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf)에 설명된 대로 지형 이미지 레이어 소스를 추가합니다.

1. 다음 매개변수 테이블을 안내서로 사용하여 투영 정보 매개변수를 편집합니다.

   | 매개 변수 | 설명 |
   |---|---|
   | Lat0 | 영상의 위쪽 가장자리의 위도인 도(도)로 90은 북극이고 -90은 남극이다. |
   | Lat1 | 이미지 하단 가장자리의 위도입니다. |
   | Lon0 | 영상의 왼쪽 가장자리 경도로서, 양수가 동이고 음수가 서쪽입니다. |
   | Lon1 | 이미지의 오른쪽 가장자리 경도입니다. |

1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭하여 파일을 저장합니다.

1. 로컬로 수행된 변경 사항을 Data Workbench 서버 컴퓨터에 저장하려면 [!DNL Server Files Manager]에서 [!DNL Temp] 열의 [!DNL Terrain Images.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭합니다.

## 포함된 투영 정보 내에 이미지에 대한 LatLonProjection을 지정하려면 {#section-174f4e00fad84a7ca0c995423dd37ae1}

1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 서버 이름 열의 [!DNL Terrain Images.cfg] 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. [!DNL Terrain Images.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.

1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** 를 클릭합니다. [!DNL Terrain Images.cfg] 파일이 메모장 창에 나타납니다.

1. 다음 샘플 파일 조각을 안내서로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 대로 지정해야 합니다. 매개 변수에 대한 설명은 이전 절차의 LatLonProjection 매개 변수 테이블을 참조하십시오.

   ```
   Projection Info = LatLonProjection: 
     Lat0 = double: 90
     Lat1 = double: -90
     Lon0 = double: -180
     Lon1 = double: 180
   ```
