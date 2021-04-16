---
description: ExpPartialMatch 매개 변수 수정(선택 사항)
title: ExpPartialMatch 매개 변수 수정(선택 사항)
uuid: 15ed33cc-5ec8-45b2-a4eb-d1941962ca9d
exl-id: 8ad45368-85a4-4865-b66b-52c29c28799c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 18%

---

# ExpPartialMatch 매개 변수 수정(선택 사항){#modifying-the-exppartialmatch-parameter-optional}

제어된 실험이 전체 웹 사이트 또는 웹 사이트의 전체 하위 디렉토리를 다른 위치에 다시 매핑하도록 하려면 [!DNL txlogd.conf] 파일의 ExpPartialMatch 매개 변수를 &quot;on&quot;으로 설정할 수 있습니다. 기본값은 &quot;off&quot;입니다.

다음은 ExpPartialMatch 매개 변수의 예입니다.

[!DNL ExpPartialMatch off]

이 매개 변수를 &quot;on&quot;으로 설정하면 실수로 전체 웹 사이트를 다시 매핑할 수 있으므로 주의하십시오.
