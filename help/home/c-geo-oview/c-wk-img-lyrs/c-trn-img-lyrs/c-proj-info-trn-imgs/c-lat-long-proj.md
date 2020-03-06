---
description: Terrain Images.cfg 파일의 위도 경도 투영 형식(LatLonProjection)은 위도 및 경도의 네 가지 매개 변수로 정의됩니다.
solution: Analytics
title: 위도-경도 예측
topic: Data workbench
uuid: 0ac947d6-3cd6-4272-96ae-456d2835e63f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 위도-경도 예측{#latitude-longitude-projections}

Terrain Images.cfg 파일의 위도 경도 투영 형식(LatLonProjection)은 위도 및 경도의 네 가지 매개 변수로 정의됩니다.

투영되지 않은 이미지(투영되지 않은 원시 비트맵 및 일반 이미지, 투영되지 않은 이미지)에 대한 LatLonProjection을 지정하려면 데이터 워크벤치의 창 내에서 LatLonProjection에 대한 설정을 입력할 수 [!DNL Terrain Images.cfg] 있습니다. 투영되지 [않은 이미지에](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)대해 LatLonProjection을 지정하려면 을 참조하십시오.

포함된 투영 정보가 있는 이미지에 LatLonProjection을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 &quot;LatLonProjection&quot;으로 설정하고 LatLonProjection에 대한 설정을 추가해야 합니다. 포함된 [투영 정보 내에서 이미지에 대한 LatLonProjection을 지정하려면...을 참조하십시오.](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1).

* [투영되지 않은 이미지에 대한 LatLonProjection 지정하기](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)
* [포함된 투영 정보 내에서 이미지에 대한 LatLonProjection을 지정하려면...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1)

## 투영되지 않은 이미지에 대한 LatLonProjection 지정하기 {#section-26554eefe645481faba68396fa13756a}

1. 데이터 워크벤치에서 [!DNL Terrain Images.cfg] 파일을 열고 지형 이미지 레이어 소스를 추가하려면 [지형 이미지 레이어를](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf)정의합니다.

1. 다음 매개변수 테이블을 가이드로 사용하여 투영 정보 매개변수를 편집합니다.

   | 매개 변수 | 설명 |
   |---|---|
   | Lat0 | 이미지의 맨 위 가장자리 위도는 도 단위로, 90은 북극이고 -90은 남극입니다. |
   | Lat1 | 이미지의 아래쪽 가장자리 위도입니다. |
   | Lon0 | 이미지의 왼쪽 가장자리의 위도(도)로, 양수가 동쪽이고 음수가 서쪽인 경우 |
   | Lon1 | 이미지의 오른쪽 가장자리의 경도입니다. |

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**.

1. 로컬에서 변경한 데이터 워크벤치 서버 시스템을 저장하려면 [!DNL Server Files Manager]열에서 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Terrain Images.cfg] > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL server name]***.

## 포함된 투영 정보 내에서 이미지에 대한 LatLonProjection을 지정하려면 {#section-174f4e00fad84a7ca0c995423dd37ae1}

1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Terrain Images.cfg] 파일은 이 디렉토리 내에 있습니다.

1. 에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Terrain Images.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Terrain Images.cfg].

1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 파일이 메모장 창에 나타납니다 [!DNL Terrain Images.cfg] .

1. 다음 샘플 파일 조각을 가이드로 사용하여 투영 정보 매개변수를 편집합니다. 아래 강조표시된 투영 유형을 지정해야 합니다. 매개 변수에 대한 설명은 이전 절차의 LatLonProjection 매개 변수 표를 참조하십시오.

   ```
   Projection Info = LatLonProjection: 
     Lat0 = double: 90
     Lat1 = double: -90
     Lon0 = double: -180
     Lon1 = double: 180
   ```

