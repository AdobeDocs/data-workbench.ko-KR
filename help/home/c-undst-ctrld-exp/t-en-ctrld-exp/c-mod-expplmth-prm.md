---
description: 'null'
solution: Insight,Analytics
title: ExpPartialMatch 매개 변수 수정(선택 사항)
topic: Data workbench
uuid: 15ed33cc-5ec8-45b2-a4eb-d1941962ca9d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ExpPartialMatch 매개 변수 수정(선택 사항){#modifying-the-exppartialmatch-parameter-optional}

제어된 실험이 전체 웹 사이트 또는 웹 사이트의 전체 하위 디렉토리를 다른 위치로 다시 매핑하도록 하려면 [!DNL txlogd.conf] 파일의 ExpPartialMatch 매개 변수를 &quot;on&quot;으로 설정할 수 있습니다. 기본값은 &quot;off&quot;입니다.

다음은 ExpPartialMatch 매개 변수의 예입니다.

[!DNL ExpPartialMatch off]

이 매개 변수를 &quot;설정&quot;으로 설정하면 실수로 전체 웹 사이트를 다시 매핑할 수 있으므로 주의하십시오.