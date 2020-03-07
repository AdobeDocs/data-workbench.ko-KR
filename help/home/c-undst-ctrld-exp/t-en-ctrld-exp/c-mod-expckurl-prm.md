---
description: ExpCookieURL 매개 변수를 사용하여 제어 실험이 제대로 작동하는지 테스트할 수 있습니다.
solution: Insight,Analytics
title: ExpCookieURL 매개 변수 수정(선택 사항)
topic: Data workbench
uuid: 0c160c26-f9de-4e41-a05d-bf7bb32395bb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ExpCookieURL 매개 변수 수정(선택 사항){#modifying-the-expcookieurl-paramter-optional}

ExpCookieURL 매개 변수를 사용하여 제어 실험이 제대로 작동하는지 테스트할 수 있습니다.

이 매개 변수는 요청 시 지정된 실험 및 그룹으로 이동한 다음 웹 사이트의 루트로 리디렉션하는 가상 페이지의 URL을 정의합니다. 이 지점부터 실험의 끝까지 사용자는 지정된 실험 및 그룹의 일부입니다.

이 매개 변수의 기본 페이지는 [!DNL setcookie.htm]으로 설정되지만 유효한 가상 URL을 사용할 수 있습니다.

>[!NOTE]
>
>가상 URL이어야 하며 실제 페이지 또는 기존 컨텐츠가 아니어야 합니다. 지정한 이름의 지정된 경로에 웹 서버에 파일이 없어야 합니다.

다음은 ExpCookieURL 매개 변수의 예입니다.

[!DNL ExpCookieURL /setcookie.htm]
