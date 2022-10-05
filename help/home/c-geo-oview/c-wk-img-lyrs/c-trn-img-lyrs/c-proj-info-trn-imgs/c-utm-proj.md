---
description: UTM(Universal Transverse Mercator) 프로젝션은 8개의 매개 변수로 정의됩니다.
title: 범용 교차 지표 예측
uuid: 55421412-5c68-4a4f-88d6-650d5999a77c
exl-id: 7d7610c3-14e7-474e-b792-ad413c86a2ef
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---

# 범용 교차 지표 예측{#universal-transverse-mercator-projections}

{{eol}}

UTM(Universal Transverse Mercator) 프로젝션은 8개의 매개 변수로 정의됩니다.

지형 이미지 레이어에 대해 범용 교차 지표 투영을 지정할 때 지형 이미지 파일은 이미지의 맨 위 방향으로 false(투영됨) 북쪽으로 정렬하고 이미지의 오른쪽 방향으로 false로 정렬해야 합니다.

지형 이미지 소스에 대한 UTM 투영을 지정하려면 [!DNL Terrain Images.cfg] 메모장과 같은 텍스트 편집기의 파일에서 프로젝션 정보 매개 변수를 &quot;TransverseMercatorProjection&quot;으로 설정하고 UTM 프로젝션에 대한 설정을 추가합니다.

**범용 교차 지표 투영 지정하기**

1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL Terrain Images.cfg]를 클릭한 다음 **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Terrain Images.cfg].

1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 다음 [!DNL Terrain Images.cfg]파일이 메모장 창에 나타납니다.

1. 다음 샘플 파일 조각 및 매개변수 테이블을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 대로 지정해야 합니다.

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
| 타원 역 평탄화, 타원 반조축 | 투영에 사용되는 줄임표의 매개 변수입니다. 반축축은 미터 단위로 지정됩니다. |
| 거짓 이스팅 | 투영법 중앙 경락의 잘못된 동쪽을 미터 단위로. UTM의 경우 항상 50만 개입니다. |
| 잘못된 노링 | 적도의 잘못된 북구, 즉 수 미터 단위. UTM의 경우, 이것은 북반구 지역은 0이고, 남반구 지역은 1만입니다. |
| 북서쪽 모서리 좌표, 남동 코너 좌표 | 이미지의 왼쪽 상단 및 오른쪽 하단 모서리의 좌표(투영된 미터)입니다. |
| 경락 | 그리니치의 동쪽에 지정된 투영 중앙 경도의 경도입니다. 음수는 서쪽으로 도 지정을 위해 사용될 수 있습니다. |
| 배율 계수 | 투영 실린더의 반경과 타원의 반조축에 대한 비율입니다. UTM(범용 교차 지표) 예측의 경우 항상 0.9996입니다. |
