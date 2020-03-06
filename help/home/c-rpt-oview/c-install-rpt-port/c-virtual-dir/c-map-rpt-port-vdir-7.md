---
description: 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑하는 단계입니다.
solution: Analytics
title: 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑
topic: Data workbench
uuid: 9d18fb85-f9d7-48b6-a19b-1e7b68a5adca
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑{#mapping-report-portal-to-a-virtual-directory-iis-or-higher}

보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑하는 단계입니다.

현재 대부분의 Managed Service 클라이언트는 Windows Server 2008 운영 체제와 IIS 7.0 이상의 웹 서버를 가지고 있습니다.

## 전제 조건 {#section-7b1cff24fc4f4c8591540b78de686f2f}

* ASP 및 [!DNL ASP.Net] 구성 요소가 IIS 7.0 이상용으로 설치되어 있는지 확인합니다.
* IIS 웹 사용자가 파일에 [!DNL Modify] 액세스할 수 있는지 확인합니다 [!DNL E:\Portal\data\users.mdb] . 파일을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL users.mdb]** 탭으로 이동하면 해당 [!DNL Properties]파일을 변경할 수 [!DNL Security] 있습니다. 목록에 IIS 웹 사용자가 표시되지 않거나 목록에 IIS 웹 사용자를 추가할 수 없는 경우 [!DNL Users] 그룹에 [!DNL Modify] 액세스 권한을 부여하면 됩니다.

* 사용자 계정을 사용하여 실행하는 경우에도 [!DNL Application Pools] 및 [!DNL C:\Windows\Temp\] 폴더에 [!DNL Modify] [!DNL E:\Portal\data\users.mdb] 액세스할 수 있는지 확인하십시오.

## 설치 단계 {#section-2a6476a221fa43dfa91866c0d41f82e5}

1. 설치된 컴퓨터에서 [!DNL Report Portal] 다음을 시작합니다 [!DNL IIS Manager]:

   **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services (IIS) Manager]**.

1. 선택 **[!UICONTROL Local Machine]** > **[!UICONTROL Sites]** > **[!UICONTROL Default Web Site]**.

1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Default Web Site]** 선택합니다 **[!UICONTROL Add Virtual Directory]**.

1. 별칭의 경우 포털을 입력합니다.
1. 실제 경로에 대해 를 입력합니다 [!DNL E:\Portal\PortalASP].
1. 클릭 **[!UICONTROL OK]**.

   만든 가상 디렉토리가 [!DNL Default Web Site]표시됩니다.

1. 방금 만든 가상 디렉터리 아래에 다음 가상 디렉터리를 추가합니다.

   | 이 별칭 만들기... | 이 물리적 리소스의 경우 |
   |---|---|
   | 코어 | [!DNL E:\Portal\PortalFiles\Core] |
   | CSS | [!DNL E:\Portal\PortalFiles\CSS] |
   | 이미지 | [!DNL E:\Portal\PortalFiles\Images] |
   | 출력 | 보고서 세트에 대한 출력을 [!DNL Report Server] 저장하는 디렉토리의 실제 위치입니다. 출력 폴더는 어느 위치에서나 찾을 수 있으며 어떤 이름이든 지정할 수 있습니다. 각 보고서 세트에 대한 하위 폴더가 포함되어 있습니다. 를 삭제할 수 [!DNL E:\Portal\PortalFiles\Output]있지만 출력 파일의 물리적 [!DNL profiles.xml] 위치로 이동합니다. |

1. 완료되면 IIS에 4개의 새 가상 디렉터리가 표시되는지 확인합니다. 디렉터리 구조에 포털과 동일한 이름의 상위 폴더 1개와 하위 폴더 4개가 있는지 확인합니다.
1. 을 **[!UICONTROL Application Pools]**&#x200B;클릭한 다음 **[!UICONTROL DefaultAppPool]** (포털에서 설정한 것)

1. 을 클릭하고 32비트 응용 프로그램 활성화를 **[!UICONTROL Advanced Settings]** 선택합니다.
1. 애플리케이션을 [!DNL Portal] 실행하려면 애플리케이션을 애플리케이션으로 전환해야 합니다. 가상 디렉터리를 설정한 후 포털 가상 디렉터리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Convert to Application]**&#x200B;선택합니다.

## 추가 팁 및 기법 {#section-ff84ab3f66c94620a6a11f0e60471d44}

* > 아래에 [!DNL Portal] 있는 Softdocs에서 **[!UICONTROL Softdocs]** 을 다운로드할 수 **[!UICONTROL Report Portal]**&#x200B;있습니다. 간단히 다운로드할 수 [!DNL ReportPortal-Release-1-0-0-7.zip]있습니다.

* 더 이상 [!DNL ReportPortalSetup.xml]필요하지 않으므로 삭제할 수 있습니다.
* 표준화를 위해 이 zip 파일의 내용을 에 넣습니다 [!DNL E:\Portal].
* SMTP 서버를 확인하려면 관리 서비스 클라이언트를 찾아 보십시오.
* NetOps에 요청하여 보고서 서버의 도메인 이름 항목을 좀 더 친숙한 IIS로 변경해 [!DNL reports.clientname.insight.omniture.com]보십시오. 예를 들어, 전체 포털 URL이 [!DNL http://reports.clientname.insight.omniture.com/Portal]있습니다. 이 변경 사항이 적용되면 [!DNL email.asa] 파일을 구성합니다.

