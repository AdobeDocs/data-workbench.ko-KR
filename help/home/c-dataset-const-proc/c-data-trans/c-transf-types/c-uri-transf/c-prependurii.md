---
description: AppendURI 변환과 마찬가지로 PrependURI 변환은 URI 차원을 구성하기 위해 Data Workbench 서버가 사용하는 내부 필드에 영향을 줍니다.
title: PrependURI
uuid: 3f2fb1a7-83f7-481e-b892-0937acd379f9
exl-id: c39d9241-ed66-446e-b59d-fdb11942d0e8
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 6%

---

# PrependURI{#prependuri}

AppendURI 변환과 마찬가지로 PrependURI 변환은 URI 차원을 구성하기 위해 Data Workbench 서버가 사용하는 내부 필드에 영향을 줍니다.

[!DNL PrependURI] 변환은 식별된 입력 필드의 값을 현재 URI에 있는 값의 앞면에 추가하여 작동합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | 값이 URI 앞에 추가되는 필드의 이름입니다. |  |

다음 예제에서는 s-dns 필드를 URI로 접두사로 추가하여 클라이언트 장치에서 요청한 도메인을 포함하도록 URI 차원의 표현을 확장합니다.

![](assets/cfg_TransformationType_PrependURI.png)

이 예에서는 s-dns 필드를 URI에 미리 추가합니다

* [!DNL /modelview.asp&id=login]

결과는 다음 URL로 표시됩니다.

* [!DNL www.adobe.com/modelview.asp?id=login]

이제 요청한 도메인을 포함하도록 URI가 확장됩니다.
