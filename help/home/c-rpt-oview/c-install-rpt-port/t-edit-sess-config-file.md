---
description: 보고서 포털은 global.asa라는 구성 파일의 정보를 사용하여 사용자 세션을 초기화합니다.
title: 세션 구성 파일 편집
uuid: c1bcd4d2-9bf5-425a-bda2-7f805983cdc6
exl-id: 98cf2e11-afb8-4530-aaa4-ea3c913effc1
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 6%

---

# 세션 구성 파일 편집{#edit-the-session-configuration-file}

보고서 포털은 global.asa라는 구성 파일의 정보를 사용하여 사용자 세션을 초기화합니다.

[!DNL Report Portal]을(를) 설치할 때 지정한 대로 이 파일을 편집해야 합니다. [!DNL global.asa] 파일은 \*PortalName*\PortalASP\ folder폴더에 있습니다.

>[!NOTE]
>
>이 구성 파일의 다른 매개 변수는 변경하지 마십시오.

1. IIS가 실행 중인 컴퓨터에서 메모장과 같은 텍스트 편집기에서 [!DNL global.asa] 파일을 엽니다.
1. 선택 사항입니다. 사용자가 인증 없이 [!DNL Report Portal]에 액세스할 수 있도록 하려면 Session(&quot;In&quot;) 매개 변수 값을 true로 변경합니다. 기본값은 false로, [!DNL Report Portal]에 액세스하려는 모든 사용자를 인증합니다.
1. [!DNL Report Portal]이(가) C 드라이브가 아닌 드라이브에 설치되어 있는 경우 Session(&quot;Drive&quot;) 매개 변수의 값을 올바른 드라이브 위치로 변경하십시오.
1. Session(&quot;DBPath&quot;) 매개 변수에 대해 [!DNL Report Portal] 사용자를 인증하는 데 필요한 정보가 포함된 데이터베이스의 경로를 반영하도록 값을 변경합니다. 드라이브 문자를 포함하지 말고 후행 슬래시를 포함해야 합니다.

   예: [!DNL /Inetpub/wwwroot/Portal/data/]

1. 파일을 저장합니다.
1. [!DNL Report Portal] 파일이 올바르게 설치되었고 지정된 가상 디렉토리를 통해 연결할 수 있는지 확인하려면 브라우저에서 다음 페이지를 엽니다.

   http://*YourServerAddress*/*YourPortalName*

   예: [!DNL http://localhost/VisualReportPortal]

   [!DNL Report Portal] ASP가 올바르게 설치된 경우 포털 로그인 페이지가 표시됩니다. 이 페이지가 표시되지 않으면 IIS에서 ASP가 활성화되어 있는지 확인하고 가상 디렉터리 매핑을 두 번 확인하십시오.
