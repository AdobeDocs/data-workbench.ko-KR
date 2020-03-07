---
description: ReplaceURI 변환은 내부 URI 차원의 값을 새 값으로 변경합니다.
solution: Analytics
title: ReplaceURI
topic: Data workbench
uuid: f9fc6d51-6eb6-4ace-8c19-2c0200555363
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ReplaceURI{#replaceuri}

ReplaceURI 변환은 내부 URI 차원의 값을 새 값으로 변경합니다.

를 [!DNL URI Prefix] 지정하면 결과 값은 제공된 입력 값과 연결된 URI 접두사입니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | URI를 대체할 값입니다. |  |
| URI 접두사 | 필드의 값에 추가할 값(문자열)입니다. [!DNL Input] |  |

>[!NOTE]
>
>변형을 적용하기 전에 cs-uri-stem 또는 cs-uri [!DNL ReplaceURI] [!DNL Page View]사본의 상위가 있는 간단한 새 차원을 만들어야 합니다. 도움이 필요한 경우 Adobe에 문의하십시오.

이 예에서는 페이지 ID가 [!DNL ReplaceURI] 웹 사이트의 홈 페이지를 볼 때마다 &quot;page=*pageid*&quot; 쿼리 문자열을 &quot; [!DNL homepage.html]&quot;로 ** 바꾸는 데 사용하는 방법을 보여 줍니다. 최종 결과는 URI를 보다 쉽게 볼 수 있게 됩니다.

![](assets/cfg_TransformationType_ReplaceURI.bmp)

표시된 변환의 경우, 페이지

* [!DNL www.examplesite.com/info.html?page=1550]

를

* [!DNL www.examplesite.com/homepage.html]

