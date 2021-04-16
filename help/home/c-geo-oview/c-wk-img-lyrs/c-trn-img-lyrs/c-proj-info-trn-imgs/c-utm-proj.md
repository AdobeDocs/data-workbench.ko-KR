---
description: UTM(Universal Transverse Mercator) 투영은 8개의 매개 변수로 정의됩니다.
title: 범용 교차 지표 예측
uuid: 55421412-5c68-4a4f-88d6-650d5999a77c
exl-id: 7d7610c3-14e7-474e-b792-ad413c86a2ef
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---

# 범용 교차 지표 예측{#universal-transverse-mercator-projections}

UTM(Universal Transverse Mercator) 투영은 8개의 매개 변수로 정의됩니다.

지형 이미지 레이어에 대해 Universal Transverse Mercator 투영을 지정할 때 지형 이미지 파일은 이미지 위쪽을 향해 false(투영된) 북쪽으로 정렬하고 이미지 오른쪽에 거짓 동쪽을 기준으로 정렬해야 합니다.

모든 지형 이미지 소스에 대한 UTM 투영을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 [투영 정보] 매개 변수를 &quot;TransverseMercatorProjection&quot;으로 설정하고 UTM 투영에 대한 설정을 추가해야 합니다.

**범용 가로 병합 투영 지정하기**

1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 콘텐트를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

1. [!DNL Terrain Images.cfg]에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. [!DNL Terrain Images.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.

1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. [!DNL Terrain Images.cfg]파일이 메모장 창에 나타납니다.

1. 다음 샘플 파일 조각 및 매개변수 테이블을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 것으로 지정해야 합니다.

   ```
   Projection Info = TransverseMercatorProjection:
     Ellipsoid Inverse Flattening = double: 294.9786982139006
     Ellipsoid Semimajor Axis = double: 6378206.4000000004
     False Easting = double: 500000
     False Northing = double: 0
     Northwest Corner Coordinates = v3d: (550339, 5.42059e+006, 0)
     Prime Meridian = double: -123
     Scale Factor = double: 0.9996
     Southeast Corner Coordinates = v3d: (555099, 5.41356e+006, 0)
   ```

| 매개 변수 | 설명 |
|---|---|
| 타원 반전 병합, 타원 반축 | 투영에 사용되는 타원 매개 변수입니다. 반축 은 미터 단위로 지정됩니다. |
| False Easting | 투영 중경에서 오직하는 길이 미터 단위. UTM의 경우 항상 500,000입니다. |
| False Northing | 적도의 잘못된 북쪽, 즉 미터로. UTM의 경우 북반구 지역은 0이고 남반구 지역은 10,000입니다. |
| 북서쪽 모퉁이 좌표, 남동쪽 모퉁이 좌표 | 이미지의 왼쪽 위 및 오른쪽 아래 모서리의 좌표(투영된 미터)입니다. |
| Primerid | 그리니치의 동쪽에 지정된 투영 중앙 경도의 경도입니다. 음수가 서쪽을 지정하는 데 사용될 수 있습니다. |
| 비율 인수 | 투영 원통의 반지름을 타원형의 반지축에 대한 비율입니다. UTM(Universal Transverse Mercator) 예상치에 대해서는 항상 0.9996입니다. |
