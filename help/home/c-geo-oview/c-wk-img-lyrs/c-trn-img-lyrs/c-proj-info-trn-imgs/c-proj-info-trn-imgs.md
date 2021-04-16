---
description: 데이터 워크벤치 지리적 위치에서는 모든 지형 이미지 레이어 소스에 대한 위도 경도 예상 및 UTM(Universal Transverse Mercator) 예상치를 모두 지원합니다.
title: 지형 이미지에 대한 투영 정보 지정
uuid: 4a476192-e749-4187-b64e-9794f39b0019
exl-id: 400b9b59-f700-4b16-8549-fe93140cad1a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---

# 지형 이미지에 대한 투영 정보 지정{#specifying-projection-information-for-terrain-images}

데이터 워크벤치 지리적 위치에서는 모든 지형 이미지 레이어 소스에 대한 위도 경도 예상 및 UTM(Universal Transverse Mercator) 예상치를 모두 지원합니다.

투영 정보는 투영되지 않은 원시 비트맵과 투영되지 않은 일반 이미지에 필요합니다. 투영 매개 변수가 이미지 자체에 포함된 지리 데이터(geometric data)에서 자동으로 결정되므로 일반적으로 필요하지 않지만 포함된 투영 정보가 있는 이미지에 대한 투영 정보를 지정할 수 있습니다. 다음 섹션에서는 [!DNL Terrain Images.cfg] 파일에서 이러한 투영 형식을 지정하는 방법에 대한 세부 정보를 제공합니다.
