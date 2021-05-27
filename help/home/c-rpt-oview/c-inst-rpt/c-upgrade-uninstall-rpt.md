---
description: 보고서 서버 소프트웨어 업그레이드 및 제거에 대한 정보입니다.
title: 보고서 서버 업그레이드 및 제거
uuid: 42f0d190-1a88-424d-be4b-90338144d287
exl-id: 86d0d848-4e2a-45cb-a1b3-b8a856332d33
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 2%

---

# 보고서 서버 업그레이드 및 제거{#upgrading-and-uninstalling-report-server}

보고서 서버 소프트웨어 업그레이드 및 제거에 대한 정보입니다.

* [보고서 업그레이드](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-95fea4bddad74616a8aea450dcdb2282)
* [보고서 제거](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-96eb3281c45a45c0a7065deaa6845c25)

## 보고서 서버 {#section-95fea4bddad74616a8aea450dcdb2282} 업그레이드

[!DNL Report Server] 5.4로 업그레이드하는 경우 지침을 사용하여 [!DNL Report Server] 소프트웨어를 업그레이드할 수 있습니다. [!DNL Report Server] 3.6 또는 이전 버전을 사용하는 경우 Adobe에 업그레이드에 대한 지원을 문의하십시오.

[!DNL Report Server] 5.4를 업그레이드하려면 Data Workbench를 사용하여 업그레이드 파일을 [!DNL Report Server] 이 연결된 Data Workbench 서버에 복사합니다. 이렇게 하면 [!DNL Report] 서버 인스턴스가 해당 서버에 연결하고 프로필을 로드할 때 자동으로 업그레이드됩니다.

>[!NOTE]
>
>[!DNL Report Server]을(를) 업그레이드하기 전에 Data Workbench 서버에서 실행 중인 프로필과 Data Workbench 서버 소프트웨어를 제대로 업그레이드했는지 확인하십시오. 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오.

다음 절차를 수행하려면 먼저 [!DNL Report Server]에 대한 업그레이드 파일을 받아야 합니다.

**[!DNL Report Server] 5.4 이상 버전으로 업그레이드하려면**

1. [!DNL E:\Portal] 아래의 모든 파일을 백업하고 이 디렉터리 내의 모든 파일과 폴더를 제거합니다.
1. 새 빌드의 내용을 [!DNL E:\Portal]에 복사합니다.
1. 이전 섹션의 지침에 따라 [!DNL global.asa], [!DNL email.asp] 및 [!DNL TopNavigation.xml]를 수정합니다.

1. 백업에서 [!DNL users.mdb]을(를) 복사합니다.

   >[!NOTE]
   >
   >이전에 .png 출처가 있는 보고서를 생성하지 않은 경우 개별 보고서 폴더로 이동하고 [!DNL reports.xml] 을 수정하여 png의 보고서 형식을 포함해야 합니다. 그렇지 않으면 500 오류가 발생할 수 있습니다. 원래 [!DNL reports.xml]은 다음과 같은 모습입니다.

   ```
      <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <REPORTS>
    <REPORT format="xls">
     <NAME>Dashboard</NAME>
     <PATH>Dashboard.xls</PATH>
     <WEB_PATH>Dashboard.xls</WEB_PATH>
    </REPORT>
   </REPORTS>
   ```

   이를 다음과 같이 수정해야 합니다.

   ```
   <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <REPORTS>
    <REPORT format="xls">
     <NAME>Dashboard</NAME>
     <PATH>Dashboard.xls</PATH>
     <WEB_PATH>Dashboard.xls</WEB_PATH>
    </REPORT>
    <REPORT format="png">
    <NAME>Dashboard</NAME>
     <PATH>Dashboard.png</PATH>
     <WEB_PATH>Dashboard.png</WEB_PATH>
    </REPORT>
   </REPORTS>
   ```

1. [!DNL report.cfg]에 png의 출력 형식을 포함하고 저장합니다. 앞으로는 보고서를 png 형식으로 생성해야 합니다.

**[!DNL Report Server] 4.0으로 업그레이드하려면**

1. Data Workbench 컴퓨터에서 보고서 서버 업그레이드 파일을 Data Workbench가 설치된 디렉토리의 [!DNL Temp\Software] 폴더에 복사합니다.
1. Data Workbench를 시작하고 [!DNL Configuration] 프로필을 로드합니다.
1. **[!UICONTROL Configure Connection to Servers]** 축소판을 클릭합니다.
1. [!DNL Servers Manager]에서 Data Workbench 서버 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.

1. Software 폴더에서 [!DNL Report Server] 폴더를 엽니다.
1. [!DNL ReportServer.exe]에 대한 **[!UICONTROL Temp]** 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.

## 보고서 서버 {#section-96eb3281c45a45c0a7065deaa6845c25} 제거

**제거하려면[!DNL Report Server]**

1. [!DNL Report Windows] 서비스를 등록 취소합니다.

   1. 명령 프롬프트를 열고 Data Workbench 서버를 설치한 폴더의 bin 하위 디렉토리로 이동합니다(InsightServer64.exe). 예: [!DNL D:\Adobe\Report\bin]
   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지하고 등록을 취소합니다.[!DNL visualreport /unregserver]

1. 보고서 서버 설치 디렉터리를 삭제합니다.
