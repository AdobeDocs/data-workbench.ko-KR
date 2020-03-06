---
description: AppendURI 변환과 마찬가지로 PrependURI 변환은 데이터 워크벤치 서버에서 URI 차원을 구성하기 위해 사용하는 내부 필드에 영향을 줍니다.
solution: Analytics
title: PrependURI
topic: Data workbench
uuid: 3f2fb1a7-83f7-481e-b892-0937acd379f9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# PrependURI{#prependuri}

AppendURI 변환과 마찬가지로 PrependURI 변환은 데이터 워크벤치 서버에서 URI 차원을 구성하기 위해 사용하는 내부 필드에 영향을 줍니다.

변환은 [!DNL PrependURI] 식별된 입력 필드의 값을 현재 URI에 있는 값의 앞면에 추가하여 작동합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | 값이 URI에 추가되는 필드의 이름입니다. |  |

다음 예제에서는 s-dns 필드를 URI에 추가하면 클라이언트 장치에서 요청한 도메인을 포함하도록 URI 차원 표현을 확장합니다.

![](assets/cfg_TransformationType_PrependURI.png)

이 예에서는 s-dns 필드를 URI에 미리 대기시킵니다.

* [!DNL /modelview.asp&id=login]

결과:

* [!DNL www.adobe.com/modelview.asp?id=login]

이제 요청된 도메인을 포함하도록 URI가 확장되었습니다.
