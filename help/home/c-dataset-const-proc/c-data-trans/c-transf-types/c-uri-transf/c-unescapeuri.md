---
description: 이스케이프 해제 URI 변환은 이스케이프된 문자열에 있는 모든 문자를 이스케이프합니다.
title: UnescapeURI
uuid: 25e87cc7-812d-4d77-be94-16093e8955fe
exl-id: abf20906-5052-4bbe-9ffb-522b850669a6
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 6%

---

# UnescapeURI{#unescapeuri}

이스케이프 해제 URI 변환은 이스케이프된 문자열에 있는 모든 문자를 이스케이프합니다.

>[!NOTE]
>
>이스케이프된 문자는 URI 문자열의 안전하지 않은 문자를 대체합니다. 16진수(예: %20)와 16진수 숫자 2로 구성된 삼각형으로 표시됩니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명형 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항입니다. 변형에 대한 참고 사항 |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | 이스케이프할 URI 문자열입니다. |  |
| 출력 | 이스케이프 처리되지 않은 문자열을 저장할 필드의 이름입니다. |  |

다음 변환은 HTTP 헤더 필드의 docname 값을 escape 취소하고 x-docname-unescaped 필드에 출력을 저장합니다.

![](assets/cfg_TransformationType_UnescapeURI.png)

docname 값이

* [!DNL mysite.net/lending%20and%20leasing%20forms/document%20library/credit%20application.doc]

x-docname-unescape의 값은

* [!DNL mysite.net/lending and leasing forms/document library/credit application.doc]
