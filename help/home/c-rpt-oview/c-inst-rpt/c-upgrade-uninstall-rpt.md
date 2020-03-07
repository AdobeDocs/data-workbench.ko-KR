---
description: 보고서 서버 소프트웨어 업그레이드 및 제거에 대한 정보입니다.
solution: Analytics
title: 보고서 서버 업그레이드 및 제거
topic: Data workbench
uuid: 42f0d190-1a88-424d-be4b-90338144d287
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 서버 업그레이드 및 제거{#upgrading-and-uninstalling-report-server}

보고서 서버 소프트웨어 업그레이드 및 제거에 대한 정보입니다.

* [보고서 업그레이드](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-95fea4bddad74616a8aea450dcdb2282)
* [보고서 제거](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-96eb3281c45a45c0a7065deaa6845c25)

## 보고서 서버 업그레이드 {#section-95fea4bddad74616a8aea450dcdb2282}

5.4 [!DNL Report Server] 로 업그레이드하는 경우 지침에 따라 [!DNL Report Server] 소프트웨어를 업그레이드할 수 있습니다. 3.6 [!DNL Report Server] 이전 버전을 사용하고 있는 경우 Adobe에 업그레이드 지원을 요청하십시오.

5.4 [!DNL Report Server] [!DNL Report Server] 를 업그레이드하려면 데이터 워크벤치를 사용하여 연결된 데이터 워크벤치 서버에 업그레이드 파일을 복사합니다. 이렇게 하면 서버 인스턴스가 해당 서버에 [!DNL Report] 연결하여 프로파일을 로드할 때 자동으로 업그레이드됩니다.

>[!NOTE]
>
>업그레이드하기 [!DNL Report Server]전에 데이터 워크벤치 서버에서 실행 중인 프로필뿐만 아니라 데이터 워크벤치 서버 소프트웨어를 제대로 업그레이드했는지 확인하십시오. 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오.

다음 절차를 수행하려면 먼저 에 대한 업그레이드 파일을 입수해야 합니다 [!DNL Report Server].

**5.4[!DNL Report Server]이상 버전으로 업그레이드하려면**

1. 아래 있는 모든 파일을 백업하고 이 디렉토리 내의 모든 [!DNL E:\Portal] 파일과 폴더를 제거합니다.
1. 새 빌드의 내용을 에 복사합니다 [!DNL E:\Portal].
1. 이전 [!DNL global.asa]섹션의 지침에 따라 [!DNL email.asp][!DNL TopNavigation.xml] 및 를 수정합니다.

1. 백업에서 [!DNL users.mdb] 을 복사합니다.

   >[!NOTE]
   >
   >이전에 .png 출처가 있는 보고서를 생성하지 않은 경우 개별 보고서 폴더로 이동한 다음 PNG의 보고서 형식을 포함하도록 [!DNL reports.xml] 수정해야 합니다. 그렇지 않으면 500 오류가 발생할 수 있습니다. 원본은 다음과 [!DNL reports.xml] 같습니다.

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

   다음을 위해 수정해야 합니다.

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

1. 에 [!DNL report.cfg]png의 출력 형식을 포함시키고 저장합니다. 앞으로는 보고서를 png 형식으로 생성해야 합니다.

**4.0[!DNL Report Server]으로 업그레이드하려면**

1. 데이터 워크벤치 컴퓨터에서 보고서 서버 업그레이드 파일을 데이터 워크벤치가 설치된 디렉토리의 [!DNL Temp\Software] 폴더에 복사합니다.
1. 데이터 워크벤치를 시작하고 [!DNL Configuration] 프로필을 로드합니다.
1. 축소판을 **[!UICONTROL Configure Connection to Servers]** 클릭합니다.
1. 데이터 워크벤치 서버 아이콘을 [!DNL Servers Manager]마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Server Files]**&#x200B;클릭합니다.

1. Software 폴더에서 [!DNL Report Server] 폴더를 엽니다.
1. 에 대한 **[!UICONTROL Temp]** 확인 표시를 마우스 오른쪽 단추로 [!DNL ReportServer.exe] 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*&#x200B;를 선택합니다.

## 보고서 서버 제거 {#section-96eb3281c45a45c0a7065deaa6845c25}

**제거하려면[!DNL Report Server]**

1. 서비스 등록을 [!DNL Report Windows] 취소합니다.

   1. 명령 프롬프트를 열고 데이터 워크벤치 서버를 설치한 폴더의 bin 하위 디렉토리(InsightServer64.exe)로 이동합니다. 예: [!DNL D:\Adobe\Report\bin]
   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지 및 등록을 취소합니다. [!DNL visualreport /unregserver]

1. 보고서 서버 설치 디렉토리를 삭제합니다.

