---
description: 지구에서 그릴 벡터를 정의하는 데이터가 포함된 하나 이상의 벡터(.vec) 파일을 참조하는 벡터 레이어를 만들 수 있습니다.
title: 벡터 파일을 참조하는 벡터 레이어 정의
uuid: fe6639fb-98fb-4246-9cc1-1a928df6ae0a
exl-id: d78fa7ea-e2a9-42b7-9071-5f72409c5b7a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 7%

---

# 벡터 파일을 참조하는 벡터 레이어 정의{#define-vector-layers-referencing-vector-files}

{{eol}}

지구에서 그릴 벡터를 정의하는 데이터가 포함된 하나 이상의 벡터(.vec) 파일을 참조하는 벡터 레이어를 만들 수 있습니다.

하나 이상을 참조하는 벡터 레이어를 정의하려면 [!DNL .vec] 파일, 다음 항목이 있어야 합니다.

* **하나 이상 [!DNL .vec] 파일** 여기에는 전 세계에서 벡터를 그리는 데 사용되는 데이터가 포함됩니다.

   >[!NOTE]
   >
   >를 가져오려면 [!DNL .vec] 벡터 레이어에서 사용할 파일은 Adobe에 문의하십시오.

* **레이어 파일** 지정 [!DNL .vec] 파일. 레이어 파일의 필수 형식에 대한 자세한 내용은 [벡터 레이어 파일 형식](../../../../home/c-get-started/c-im-layers/c-vctr-layers/c-ref-vctr-files.md#section-83a0077cf0c8479b9e7b2939bc761af1).

   >[!NOTE]
   >
   >다음 [!DNL Boundaries.layer] 파일, [!DNL Geography] profile 은 [!DNL mwnation.vec], [!DNL mwstate.vec], [!DNL mwcoast.vec], [!DNL mwlake.vec], 및 [!DNL mwisland.vec] 파일.

## 벡터 레이어 파일 형식 {#section-83a0077cf0c8479b9e7b2939bc761af1}

참조하는 각 벡터 레이어 파일 [!DNL .vec] 파일은 다음 템플릿을 사용하여 포맷해야 합니다.

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
| Vec 파일 | 경로 [!DNL .vec] 벡터 데이터가 포함된 파일입니다. |
| 색상 | (빨간색,녹색,파란색)으로 표시되는 RGB 색상 벡터입니다. 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다. 예를 들어, (1.0, 0.0, 0.0)은 밝은 빨간색이고 (0.5, 0.5, 0.5)은 회색으로 표시됩니다. |
| 알파 | 전경에 표시된 벡터의 투명도를 제어합니다. 범위는 0~1이며 0은 가장 투명합니다. |
| 너비 | 선택 사항. 데이터 너비를 픽셀 단위로 설정합니다. 권장 범위는 1~4입니다. |
| 오류 요소 | 벡터가 얼마나 정확하게 그려지는지를 제어합니다. 큰 값의 경우 벡터가 덜 정확하게 더 빨리 그려집니다. 기본값은 5입니다. |

다음 [!DNL Boundaries.layer] 파일의 형식은 다음과 같습니다.

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
