---
description: 지구별로 그릴 벡터를 정의하는 데이터가 포함된 하나 이상의 벡터(.vec) 파일을 참조하는 벡터 레이어를 만들 수 있습니다.
title: 벡터 파일을 참조하는 벡터 레이어 정의
uuid: 162d4ecc-d305-42e3-a5d4-0c1609a40f29
exl-id: c6da3cd9-f42a-4e9c-ae48-9f4ffdc42f7b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 7%

---

# 벡터 파일을 참조하는 벡터 레이어 정의{#defining-vector-layers-referencing-vector-files}

지구별로 그릴 벡터를 정의하는 데이터가 포함된 하나 이상의 벡터(.vec) 파일을 참조하는 벡터 레이어를 만들 수 있습니다.

하나 이상의 [!DNL .vec]개 파일을 참조하는 벡터 레이어를 정의하려면 다음 항목이 있어야 합니다.

* 지구에서 벡터를 그리는 데 사용된 데이터가 포함된 하나 이상의 [!DNL .vec]개 파일

   >[!NOTE]
   >
   >벡터 레이어에 사용할 [!DNL .vec] 파일을 얻으려면 Adobe에 문의하십시오.

* [!DNL .vec] 파일의 위치를 지정하는 레이어 파일입니다. 레이어 파일의 필수 형식에 대한 자세한 내용은 [벡터 레이어 파일 형식](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-def-vctr-files.md#section-530d03f41ede4a339aebbb680e15240a)을 참조하십시오.

   >[!NOTE]
   >
   >[!DNL Geography] 프로필과 함께 제공되는 [!DNL Boundaries.layer] 파일은 [!DNL mwnation.vec], [!DNL mwstate.vec], [!DNL mwcoast.vec], [!DNL mwlake.vec] 및 [!DNL mwisland.vec] 파일을 참조하는 벡터 레이어입니다.

## 벡터 레이어 파일 형식 {#section-530d03f41ede4a339aebbb680e15240a}

[!DNL .vec]파일을 참조하는 각 벡터 레이어 파일은 다음 템플릿을 사용하여 서식을 지정해야 합니다.

```
Layer = VectorLayer:
  Vec Files = vector: n items
    0 = string: Maps\\.vec file 1
    1 = string: Maps\\.vec file 2
    . . .
    n-1 = string: Maps\\.vec file n
  Color = v3d: color vector
  Alpha = double: alpha
  Width = double: width
  Error Factor = double: error factor
```

| 매개 변수 | 설명 |
|---|---|
| Vec 파일 | 벡터 데이터를 포함하는 [!DNL .vec] 파일의 경로입니다. |
| 색상 | RGB 색상 벡터로서 (빨강,녹색,파랑)으로 표현됩니다. 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다. 예를 들어 (1.0, 0.0, 0.0)은 밝은 빨간색이고 (0.5, 0.5, 0.5)는 회색입니다. |
| 알파 | 지구 위에 표시되는 벡터의 투명도를 제어합니다. 범위는 0~1이며, 0은 가장 투명합니다. |
| 너비 | 선택 사항입니다. 데이터의 너비를 픽셀 단위로 설정합니다. 권장 범위는 1~4입니다. |
| 오류 계수 | 벡터가 얼마나 정확하게 그려지는지를 제어합니다. 값이 클수록 벡터가 덜 정확하게 더 빠르게 그려집니다. 기본값은 5입니다. |

[!DNL Boundaries.layer] 파일의 형식은 다음과 같습니다.

```
 Boundaries.layer file is formatted as follows:
Layer = VectorLayer:
  Vec Files = vector: 5 items
    0 = string: Maps\\mwnation.vec
    1 = string: Maps\\mwstate.vec
    2 = string: Maps\\mwcoast.vec
    3 = string: Maps\\mwlake.vec
    4 = string: Maps\\mwisland.vec
  Color = v3d: (.5,.5,1)
  Alpha = double: .5
  Error Factor = double: 4
```
