---
description: IIS에서 대시보드를 배포하는 단계입니다.
title: 대시보드 배포
uuid: e9a5d62e-9d59-448a-9728-8087aec0fdec
exl-id: d59efcc3-7405-407d-840a-b5202f418d51
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 5%

---

# 대시보드 배포{#deploying-the-dashboard}

{{eol}}

IIS에서 대시보드를 배포하는 단계입니다.

1. 대시보드를 설치할 설치 폴더 만들기(예: ) [!DNL c:\inetpub\wwwroot\dashboard].
1. IIS에서 대시보드의 응용 프로그램 풀을 만듭니다.
1. IIS 관리자 콘솔을 엽니다.
1. **[!UICONTROL Application Pools]**&#x200B;로 이동합니다.
1. 선택 **[!UICONTROL Add Application Pool…]**에서 **[!UICONTROL Actions]** 오른쪽 메뉴입니다.
1. 에서 **[!UICONTROL Add Application Pool]** 양식에서 이름에 대한 대시보드를 사용하고 .NET Framework v.4.0.xxxxxx 을 .NET Framework 버전으로 선택합니다.
1. 다른 필드를 기본값으로 두고 를 클릭합니다. **[!UICONTROL OK]** 응용 프로그램 풀을 만들려면
1. 대시보드 응용 프로그램을 배포합니다.
1. IIS 관리자 콘솔을 엽니다.
1. 를 확장합니다. **[!UICONTROL Default Web Site]** c:\inetpub\wwwroot\dashboard by default에서 만든 폴더가 표시됩니다.
1. 폴더를 마우스 오른쪽 단추로 클릭하고 를 선택합니다. **[!UICONTROL Convert to Application]**.
1. **[!UICONTROL Application Pool]**2단계에서 생성됩니다(예: &quot;대시보드&quot;).
1. 아래 **[!UICONTROL Sites]**&#x200B;를 클릭하여 배포할 웹 사이트를 마우스 오른쪽 단추로 클릭합니다(예: &quot;기본 웹 사이트&quot;).
1. 선택 **[!UICONTROL Deploy]** > **[!UICONTROL Import Application]**.
1. Adobe에서 제공하는 대시보드 배포 파일을 찾아 선택합니다.
1. 클릭 **[!UICONTROL Next]** 응용 프로그램 정보 입력 화면으로 두 번 진행합니다.
1. 이 화면에서 대시보드 배포를 사용자 지정하도록 선택할 수 있습니다.
1. 대상 **[!UICONTROL Application Path]**&#x200B;이전에 선택한 폴더 이름을 입력합니다.
1. 아래 **[!UICONTROL Disable Automatic Database Upgrade]**, 입력 `False`새 설치이므로 입니다.
1. 필요한 경우 연결 문자열을 사용자 지정합니다. 예:

   ```
   Data Source=.;Initial Catalog=thinclientdb;Integrated Security=SSPI;Connect Timeout=30; 
   Application Name=Insight Dashboard;MultipleActiveResultSets=true;
   ```

1. 클릭 **[!UICONTROL Next]** 응용 프로그램 설치를 시작합니다.
1. 설치가 완료되면 설치 로그에 오류가 표시되지 않습니다.
