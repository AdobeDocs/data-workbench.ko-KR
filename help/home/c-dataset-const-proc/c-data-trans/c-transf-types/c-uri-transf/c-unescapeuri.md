---
description: 이스케이프 해제 URI 변환은 이스케이프 처리된 문자열의 모든 문자를 이스케이프 처리합니다.
title: UnescapeURI
uuid: 25e87cc7-812d-4d77-be94-16093e8955fe
exl-id: abf20906-5052-4bbe-9ffb-522b850669a6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 6%

---

# UnescapeURI{#unescapeuri}

이스케이프 해제 URI 변환은 이스케이프 처리된 문자열의 모든 문자를 이스케이프 처리합니다.

>[!NOTE]
>
>이스케이프 처리된 문자는 URI 문자열의 안전하지 않은 문자를 대체합니다. 16진수 뒤에 두 개의 16진수로 구성된 세 개의 숫자(예: %20)로 표시됩니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | 이스케이프되지 않을 URI 문자열입니다. |  |
| 출력 | 이스케이프 처리되지 않은 문자열을 저장할 필드의 이름입니다. |  |

다음 변환은 HTTP 헤더 필드의 docname 값을 이스케이프하고 x-docname-unescape 필드에 출력을 저장합니다.

![](assets/cfg_TransformationType_UnescapeURI.png)

docname 값이

* [!DNL mysite.net/lending%20and%20leasing%20forms/document%20library/credit%20application.doc]

그러면 x-docname-unescape 값이

* [!DNL mysite.net/lending and leasing forms/document library/credit application.doc]
