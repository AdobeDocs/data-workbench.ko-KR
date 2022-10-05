---
description: 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑하는 단계입니다.
title: 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑
uuid: 9d18fb85-f9d7-48b6-a19b-1e7b68a5adca
exl-id: 2fa3439a-1fe5-4a20-83db-d233ae8b5263
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 5%

---

# 보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑{#mapping-report-portal-to-a-virtual-directory-iis-or-higher}

{{eol}}

보고서 포털을 가상 디렉터리(IIS 7.0 이상)에 매핑하는 단계입니다.

현재 대부분의 Managed Service 클라이언트는 Windows Server 2008 운영 체제와 IIS 7.0 이상의 웹 서버를 사용하는 서버를 가지고 있습니다.

## 사전 요구 사항 {#section-7b1cff24fc4f4c8591540b78de686f2f}

* ASP와 [!DNL ASP.Net] 구성 요소가 IIS 7.0 이상용으로 설치되어 있습니다.
* IIS 웹 사용자가 [!DNL Modify] 액세스 권한 [!DNL E:\Portal\data\users.mdb] 파일. 을 마우스 오른쪽 단추로 클릭하여 변경할 수 있습니다 **[!UICONTROL users.mdb]** 파일 및 아래 [!DNL Properties]로 이동합니다. [!DNL Security] 탭. 목록에 IIS 웹 사용자가 표시되지 않거나 목록에 IIS 웹 사용자를 추가할 수 없는 경우에는 [!DNL Users] 그룹 [!DNL Modify] 액세스 권한.

* 를 실행하는 데 사용 중인 사용자 계정을 확인합니다. [!DNL Application Pools] 또한 [!DNL Modify] 액세스 권한 [!DNL E:\Portal\data\users.mdb] 및 [!DNL C:\Windows\Temp\] 폴더를 입력합니다.

## 설치 단계 {#section-2a6476a221fa43dfa91866c0d41f82e5}

1. 머신에서 [!DNL Report Portal] 이(가) 설치되어 있으면 [!DNL IIS Manager]:

   **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services (IIS) Manager]**.

1. 선택 **[!UICONTROL Local Machine]** > **[!UICONTROL Sites]** > **[!UICONTROL Default Web Site]**.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Default Web Site]** 을(를) 선택합니다. **[!UICONTROL Add Virtual Directory]**.

1. 별칭에 대해 Portal을 입력합니다.
1. 물리적 경로에 대해 를 입력합니다. [!DNL E:\Portal\PortalASP].
1. 클릭 **[!UICONTROL OK]**.

   생성한 가상 디렉터리가 [!DNL Default Web Site].

1. 방금 생성한 가상 디렉터리 아래에 다음 가상 디렉터리를 추가합니다.

   | 이 별칭 만들기.. | 이 물리적 리소스의 경우 |
   |---|---|
   | 코어 | [!DNL E:\Portal\PortalFiles\Core] |
   | CSS | [!DNL E:\Portal\PortalFiles\CSS] |
   | 이미지 | [!DNL E:\Portal\PortalFiles\Images] |
   | 출력 | 디렉터리가 있는 실제 위치 [!DNL Report Server] 보고서 세트의 출력을 저장합니다. 출력 폴더는 어느 곳에서든 찾을 수 있으며 아무 이름이나 지정할 수 있습니다. 이 파일에는 각 보고서 세트에 대한 하위 폴더가 포함되어 있습니다. 을(를) 삭제할 수 있습니다 [!DNL E:\Portal\PortalFiles\Output]하지만 이동 [!DNL profiles.xml] 출력 파일의 실제 위치로 이동합니다. |

1. 완료되면 IIS에 4개의 새 가상 디렉터리가 표시되는지 확인하십시오. 디렉토리 구조에 하나의 상위 폴더(포털과 동일한 이름)와 4개의 하위 폴더가 있는지 확인합니다.
1. 클릭 **[!UICONTROL Application Pools]**, 그런 다음 **[!UICONTROL DefaultAppPool]** (포털에서 설정한 것으로 가정)

1. 클릭 **[!UICONTROL Advanced Settings]** 32비트 응용 프로그램 활성화의 경우 True를 선택합니다.
1. 를 가져오려면 [!DNL Portal] 이를 수행하려면 응용 프로그램으로 변환해야 합니다. 가상 디렉터리를 설정한 후 Portal 가상 디렉터리를 마우스 오른쪽 단추로 클릭하고 를 선택합니다 **[!UICONTROL Convert to Application]**.

## 추가 팁과 트릭 {#section-ff84ab3f66c94620a6a11f0e60471d44}

* 을 다운로드할 수 있습니다 [!DNL Portal] 아래의 소프트웨어 문서 **[!UICONTROL Softdocs]** > **[!UICONTROL Report Portal]**. 간단히 을(를) 다운로드할 수 있습니다 [!DNL ReportPortal-Release-1-0-0-7.zip].

* 더 이상 필요하지 않습니다. [!DNL ReportPortalSetup.xml]로 설정되므로 삭제할 수 있습니다.
* 표준화를 위해 이 zip 파일의 내용을 [!DNL E:\Portal].
* SMTP 서버 확인 관리 서비스 클라이언트의 경우 여기에서 볼 수 있습니다.
* 보고서 서버의 IIS에 있는 도메인 이름 항목을 좀 더 친근한 값으로 변경하려면 NetOps에 요청을 넣습니다(예: [!DNL reports.clientname.insight.omniture.com]를 설정하는 것이 좋습니다 [!DNL https://reports.clientname.insight.omniture.com/Portal]. 구성 [!DNL email.asa] 변경 사항이 적용되면 파일을 제출합니다.
