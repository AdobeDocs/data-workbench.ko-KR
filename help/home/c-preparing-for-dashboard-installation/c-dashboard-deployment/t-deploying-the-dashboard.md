---
description: IIS에서 대시보드를 배포하는 절차.
solution: Analytics
title: 대시보드 배포
topic: Data workbench
uuid: e9a5d62e-9d59-448a-9728-8087aec0fdec
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 대시보드 배포{#deploying-the-dashboard}

IIS에서 대시보드를 배포하는 절차.

1. 설치 폴더를 만들어 대시보드(예: [!DNL c:\inetpub\wwwroot\dashboard]) 설치
1. IIS에서 대시보드의 응용 프로그램 풀을 만듭니다.
1. IIS Manager 콘솔을 엽니다.
1. **[!UICONTROL Application Pools]** 으로 이동합니다.
1. 오른쪽 메뉴에서 **[!UICONTROL Add Application Pool…]** **[!UICONTROL Actions]** 을 선택합니다.
1. 양식에서 이름에 대한 대시보드를 사용하고 .NET Framework v.4.0.xxxxxx를 .NET Framework 버전으로 선택합니다. **[!UICONTROL Add Application Pool]**
1. 다른 필드를 기본값으로 두고 을 클릭하여 애플리케이션 풀을 **[!UICONTROL OK]** 만듭니다.
1. 대시보드 애플리케이션을 배포합니다.
1. IIS Manager 콘솔을 엽니다.
1. 를 **[!UICONTROL Default Web Site]**&#x200B;확장하면 c:\inetpub\wwwroot\dashboard by default에서 만든 폴더가 표시됩니다.
1. 폴더를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Convert to Application]**&#x200B;선택합니다.
1. 2단계에서 만든 **[!UICONTROL Application Pool]**을 선택합니다(예: &quot;대시보드&quot;).
1. 아래에서 배포할 웹 사이트(예: &quot;기본 웹 사이트&quot;)를 마우스 오른쪽 단추로 **[!UICONTROL Sites]**&#x200B;클릭합니다.
1. 선택 **[!UICONTROL Deploy]** > **[!UICONTROL Import Application]**.
1. Adobe에서 제공하는 대시보드 배포 파일로 이동하여 선택합니다.
1. 애플리케이션 정보 입력 화면으로 이동하려면 **[!UICONTROL Next]** 두 번 클릭합니다.
1. 이 화면에서 대시보드 배포를 사용자 지정할 수 있습니다.
1. 에 **[!UICONTROL Application Path]**&#x200B;대해 이전에 선택한 폴더 이름을 입력합니다.
1. 새 **[!UICONTROL Disable Automatic Database Upgrade]**`False`&#x200B;설치이므로 을 입력합니다.
1. 필요한 경우 연결 문자열을 사용자 정의합니다. 예:

   ```
   Data Source=.;Initial Catalog=thinclientdb;Integrated Security=SSPI;Connect Timeout=30; 
   Application Name=Insight Dashboard;MultipleActiveResultSets=true;
   ```

1. 을 **[!UICONTROL Next]** 클릭하면 IIS에서 응용 프로그램 설치를 시작합니다.
1. 설치가 완료되면 설치 로그에 오류가 표시되지 않습니다.
