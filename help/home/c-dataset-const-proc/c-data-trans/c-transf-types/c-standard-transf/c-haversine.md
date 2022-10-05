---
description: 수학에서, 해버신 공식은 장점과 위도에서 식별된 구에서 두 점 사이의 원거리를 제공하는 방정식입니다.
title: Haversine
uuid: 835fa9dd-db70-4498-a03e-59595bc041fe
exl-id: e700c0a0-1a1a-4c56-bb4f-1deb1b39b059
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 4%

---

# Haversine{#haversine}

{{eol}}

수학에서, 해버신 공식은 장점과 위도에서 식별된 구에서 두 점 사이의 원거리를 제공하는 방정식입니다.

공식 처럼 [!DNL Haversine] 변환에는 두 개의 세트가 필요합니다 [!DNL Latitude] 및 [!DNL Longitude] 설정(이 네 개의 입력을 사용하여 두 위치 사이의 지구 사이의 실제 거리를 계산합니다.)

이 거리는 &quot;In Km&quot; 깃발을 false에서 true로 변경하여 마일리지 또는 킬로미터로 표시될 수 있습니다.

![](assets/cfg_TransformationType_Haversine.png)

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| Latitude 1 필드 | 1점의 위도입니다. |  |
| Latitude 2 필드 | 점 2의 위도입니다. |  |
| 경도 1 필드 | 1점의 경도입니다. |  |
| 경도 2 필드 | 2점의 경도입니다. |  |
| 출력 | 계산되면 [!DNL Output] 필드에는 Dimension에서 요소로 지정된 점 사이의 거리가 포함됩니다. |  |

예를 들어 해당 스토어의 위도 및 경도에 Lat1, Lon1로 코딩하고 고객에 대해 IP 마지막으로 조회를 사용하는 경우 대부분의 고객이 구매하거나 가져오는 스토어까지의 거리를 결정할 수 있습니다.

>[!NOTE]
>
>다른 위치의 거리를 식별하려면 각 개별 위치에는 위도 및 경도 필드가 있어야 합니다.
