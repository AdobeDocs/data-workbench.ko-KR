---
description: 이스케이프 해제 URI 변환은 이스케이프된 문자열의 모든 문자를 escape합니다.
solution: Analytics
title: UnescapeURI
topic: Data workbench
uuid: 25e87cc7-812d-4d77-be94-16093e8955fe
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# UnescapeURI{#unescapeuri}

이스케이프 해제 URI 변환은 이스케이프된 문자열의 모든 문자를 escape합니다.

>[!NOTE]
>
>이스케이프 처리된 문자는 URI 문자열의 안전하지 않은 문자를 대체합니다. 이 변수들은 퍼센트 기호 뒤에 두 개의 16진수 숫자(예: %20)가 오는 16진수로 구성된 삼각형으로 표시됩니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | 이스케이프할 URI 문자열입니다. |  |
| 출력 | 이스케이프 처리되지 않은 문자열을 저장할 필드의 이름입니다. |  |

다음 변환은 HTTP 헤더 필드의 docname 값을 escape 취소하고 x-docname-unescape 필드에 출력을 저장합니다.

![](assets/cfg_TransformationType_UnescapeURI.png)

docname 값이

* [!DNL mysite.net/lending%20and%20leasing%20forms/document%20library/credit%20application.doc]

그러면 x-docname-unescape 값이

* [!DNL mysite.net/lending and leasing forms/document library/credit application.doc]

