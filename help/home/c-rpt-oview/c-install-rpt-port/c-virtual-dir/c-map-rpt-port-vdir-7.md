---
description: 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑하는 절차.
title: 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑
uuid: 9d18fb85-f9d7-48b6-a19b-1e7b68a5adca
exl-id: 2fa3439a-1fe5-4a20-83db-d233ae8b5263
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 5%

---

# 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑{#mapping-report-portal-to-a-virtual-directory-iis-or-higher}

보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑하는 절차.

현재 대부분의 관리 서비스 클라이언트에는 Windows Server 2008 운영 체제와 IIS 7.0 이상의 웹 서버가 있는 서버가 있습니다.

## 전제 조건 {#section-7b1cff24fc4f4c8591540b78de686f2f}

* ASP 및 [!DNL ASP.Net] 구성 요소가 IIS 7.0 이상용으로 설치되어 있는지 확인합니다.
* IIS 웹 사용자에게 [!DNL E:\Portal\data\users.mdb] 파일에 대한 [!DNL Modify] 액세스 권한이 있는지 확인합니다. **[!UICONTROL users.mdb]** 파일을 마우스 오른쪽 버튼으로 클릭하고 [!DNL Properties] 아래에서 [!DNL Security] 탭으로 이동하여 변경할 수 있습니다. 목록에 IIS 웹 사용자가 없거나 IIS 웹 사용자를 목록에 추가할 수 없는 경우 [!DNL Users] 그룹에 [!DNL Modify] 액세스 권한을 제공하면 됩니다.

* [!DNL Application Pools]을(를) 실행하는 데 사용 중인 사용자 계정이 [!DNL E:\Portal\data\users.mdb] 및  [!DNL C:\Windows\Temp\] 폴더에 대한 [!DNL Modify] 액세스 권한도 있는지 확인합니다.

## 설치 단계 {#section-2a6476a221fa43dfa91866c0d41f82e5}

1. [!DNL Report Portal]이(가) 설치된 컴퓨터에서 [!DNL IIS Manager]:

   **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services (IIS) Manager]**.

1. 선택 **[!UICONTROL Local Machine]** > **[!UICONTROL Sites]** > **[!UICONTROL Default Web Site]**.

1. **[!UICONTROL Default Web Site]**&#x200B;을(를) 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Virtual Directory]**&#x200B;을 선택합니다.

1. 별칭에 대해 포털을 입력합니다.
1. 실제 경로에 대해 [!DNL E:\Portal\PortalASP]을 입력합니다.
1. 클릭 **[!UICONTROL OK]**.

   만든 가상 디렉터리가 [!DNL Default Web Site] 아래에 나타납니다.

1. 방금 만든 가상 디렉터리 아래에 다음 가상 디렉터리를 추가합니다.

   | 이 별칭 만들기... | 이 물리적 리소스의 경우 |
   |---|---|
   | Core | [!DNL E:\Portal\PortalFiles\Core] |
   | CSS | [!DNL E:\Portal\PortalFiles\CSS] |
   | 이미지 | [!DNL E:\Portal\PortalFiles\Images] |
   | 출력 | [!DNL Report Server]이 보고서 세트에 대한 출력을 저장하는 디렉토리의 물리적 위치입니다. 출력 폴더는 어느 위치에서나 찾을 수 있으며 모든 이름으로 지정할 수 있습니다. 각 보고서 세트에 대한 하위 폴더가 포함되어 있습니다. [!DNL E:\Portal\PortalFiles\Output]을(를) 삭제할 수 있지만 [!DNL profiles.xml]을(를) 출력 파일의 실제 위치로 이동합니다. |

1. 완료되면 IIS에 4개의 새 가상 디렉터리가 표시되는지 확인합니다. 디렉토리 구조에 하나의 상위 폴더(포털과 동일한 이름)와 4개의 하위 폴더가 있는지 확인합니다.
1. **[!UICONTROL Application Pools]**&#x200B;을 클릭한 다음 **[!UICONTROL DefaultAppPool]**(포털에서 설정한 것으로 가정함)을 클릭합니다.

1. **[!UICONTROL Advanced Settings]**&#x200B;을 클릭하고 32비트 응용 프로그램 활성화를 위해 True를 선택합니다.
1. [!DNL Portal]이(가) 작동하려면 응용 프로그램으로 변환해야 합니다. 가상 디렉터리를 설정한 후 포털 가상 디렉터리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Convert to Application]**&#x200B;을 선택합니다.

## 추가 팁 및 트릭 {#section-ff84ab3f66c94620a6a11f0e60471d44}

* **[!UICONTROL Softdocs]** > **[!UICONTROL Report Portal]** 아래의 Softdocs에서 [!DNL Portal]을 다운로드할 수 있습니다. [!DNL ReportPortal-Release-1-0-0-7.zip]만 다운로드할 수 있습니다.

* [!DNL ReportPortalSetup.xml]이(가) 더 이상 필요하지 않으므로 삭제할 수 있습니다.
* 표준화를 위해 이 zip 파일의 내용을 [!DNL E:\Portal]에 넣습니다.
* SMTP 서버 관리 서비스 클라이언트를 확인하려면 여기에서 확인할 수 있습니다.
* NetOps에 요청하여 보고서 서버에 대한 IIS의 도메인 이름 항목을 좀 더 친근한 이름으로 변경합니다(예: [!DNL reports.clientname.insight.omniture.com]). 그러면 전체 포털 URL이 [!DNL http://reports.clientname.insight.omniture.com/Portal]이 됩니다. 이 변경 사항이 적용되면 [!DNL email.asa] 파일을 구성합니다.
