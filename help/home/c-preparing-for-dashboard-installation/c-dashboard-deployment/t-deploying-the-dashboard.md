---
description: IIS에서 대시보드를 배포하는 단계입니다.
title: 대시보드 배포
uuid: e9a5d62e-9d59-448a-9728-8087aec0fdec
exl-id: d59efcc3-7405-407d-840a-b5202f418d51
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 5%

---

# 대시보드 배포{#deploying-the-dashboard}

IIS에서 대시보드를 배포하는 단계입니다.

1. 설치 폴더를 만들어 대시보드를 설치합니다(예: [!DNL c:\inetpub\wwwroot\dashboard]).
1. IIS에서 대시보드의 응용 프로그램 풀을 만듭니다.
1. IIS 관리자 콘솔을 엽니다.
1. **[!UICONTROL Application Pools]** 으로 이동합니다.
1. 오른쪽 **[!UICONTROL Actions]** 메뉴에서 **[!UICONTROL Add Application Pool…]**을 선택합니다.
1. **[!UICONTROL Add Application Pool]** 양식에서 이름에 대시보드를 사용하고 .NET Framework v.4.0.xxxxxx 을 .NET Framework 버전으로 선택합니다.
1. 다른 필드를 기본값으로 두고 **[!UICONTROL OK]** 을 클릭하여 응용 프로그램 풀을 만듭니다.
1. 대시보드 응용 프로그램을 배포합니다.
1. IIS 관리자 콘솔을 엽니다.
1. **[!UICONTROL Default Web Site]**&#x200B;을 확장하면 c:\inetpub\wwwroot\dashboard by default에서 만든 폴더가 표시됩니다.
1. 폴더를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Convert to Application]** 을 선택합니다.
1. 2단계에서 생성된 **[!UICONTROL Application Pool]**를 선택합니다(예: &quot;대시보드&quot;).
1. **[!UICONTROL Sites]** 아래에서 배포할 웹 사이트(예: &quot;기본 웹 사이트&quot;)를 마우스 오른쪽 단추로 클릭합니다.
1. 선택 **[!UICONTROL Deploy]** > **[!UICONTROL Import Application]**.
1. Adobe에서 제공하는 대시보드 배포 파일을 찾아 선택합니다.
1. **[!UICONTROL Next]** 을 두 번 클릭하여 응용 프로그램 정보 입력 화면으로 진행합니다.
1. 이 화면에서 대시보드 배포를 사용자 지정하도록 선택할 수 있습니다.
1. **[!UICONTROL Application Path]**&#x200B;에 대해 이전에 선택한 폴더 이름을 입력합니다.
1. **[!UICONTROL Disable Automatic Database Upgrade]** 아래에 `False` 을 입력합니다. 새 설치이므로 이 값을 입력합니다.
1. 필요한 경우 연결 문자열을 사용자 지정합니다. 예를 들어,

   ```
   Data Source=.;Initial Catalog=thinclientdb;Integrated Security=SSPI;Connect Timeout=30; 
   Application Name=Insight Dashboard;MultipleActiveResultSets=true;
   ```

1. **[!UICONTROL Next]** 을 클릭하면 IIS에서 응용 프로그램 설치를 시작합니다.
1. 설치가 완료되면 설치 로그에 오류가 표시되지 않습니다.
