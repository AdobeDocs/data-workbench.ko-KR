---
description: 하나 이상의 벡터(.vec) 파일을 참조하는 벡터 레이어를 만들 수 있습니다. 이 파일에는 지구에서 그릴 벡터를 정의하는 데이터가 포함되어 있습니다.
solution: Analytics
title: 벡터 파일을 참조하는 벡터 레이어 정의
topic: Data workbench
uuid: fe6639fb-98fb-4246-9cc1-1a928df6ae0a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 벡터 파일을 참조하는 벡터 레이어 정의{#define-vector-layers-referencing-vector-files}

하나 이상의 벡터(.vec) 파일을 참조하는 벡터 레이어를 만들 수 있습니다. 이 파일에는 지구에서 그릴 벡터를 정의하는 데이터가 포함되어 있습니다.

하나 이상의 [!DNL .vec] 파일을 참조하는 벡터 레이어를 정의하려면 다음 항목이 있어야 합니다.

* **지구에서 벡터를 그리는 데 사용된 데이터가 들어 있는 하나 이상의[!DNL .vec]파일** .

   >[!NOTE]
   >
   >벡터 레이어와 함께 사용할 [!DNL .vec] 파일을 얻으려면 Adobe에 문의하십시오.

* **파일의 위치를 지정하는 레이어 파일입니다** . [!DNL .vec] 필요한 레이어 파일 형식에 대한 자세한 내용은 벡터 레이어 [파일 형식을 참조하십시오](../../../../home/c-get-started/c-im-layers/c-vctr-layers/c-ref-vctr-files.md#section-83a0077cf0c8479b9e7b2939bc761af1).

   >[!NOTE]
   >
   >이 [!DNL Boundaries.layer] 파일은 [!DNL Geography] 프로파일과 함께 [!DNL mwnation.vec], [!DNL mwstate.vec], [!DNL mwcoast.vec]및 [!DNL mwlake.vec][!DNL mwisland.vec] 파일을 참조하는 벡터 레이어입니다.

## 벡터 레이어 파일 포맷 {#section-83a0077cf0c8479b9e7b2939bc761af1}

파일을 참조하는 각 벡터 레이어 파일의 형식은 다음 템플릿을 사용하여 지정해야 합니다. [!DNL .vec]

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
| 벡터 파일 | 벡터 데이터를 포함하는 [!DNL .vec] 파일의 경로입니다. |
| 색상 | RGB 색상 벡터로 표현됩니다(빨강,녹색,파랑). 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다.예를 들어 (1.0, 0.0, 0.0)은 밝은 빨강이고 (0.5, 0.5, 0.5)는 회색입니다. |
| 알파 | 세계에 표시되는 벡터의 투명도를 제어합니다. 범위는 0에서 1이며, 0은 가장 투명합니다. |
| 너비 | 선택 사항입니다. 데이터의 너비를 픽셀 단위로 설정합니다. 권장 범위는 1~4입니다. |
| 오류 계수 | 벡터의 정확한 드로잉 정도를 제어합니다. 값이 클수록 벡터가 덜 정확하게 더 빠르게 그려집니다. 기본값은 5입니다. |

파일의 [!DNL Boundaries.layer] 형식은 다음과 같습니다.

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

