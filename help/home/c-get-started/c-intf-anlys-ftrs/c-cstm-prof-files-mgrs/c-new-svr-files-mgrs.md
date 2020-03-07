---
description: 서버 파일 관리자는 구성 및 조회 파일을 포함하여 데이터 워크벤치 서버 설치 디렉토리에 있는 모든 디렉토리를 표시합니다.
solution: Analytics
title: 서버 파일 관리자 만들기
topic: Data workbench
uuid: 9fb2163d-3756-40d2-9817-4a89bd8a38c9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 서버 파일 관리자 만들기{#create-a-server-files-manager}

서버 파일 관리자는 구성 및 조회 파일을 포함하여 데이터 워크벤치 서버 설치 디렉토리에 있는 모든 디렉토리를 표시합니다.

전체 디렉토리 구조를 탐색하지 [!DNL Server Files Manager] 않고 특정 요구 사항을 해결하기 위해 몇 개의 하위 디렉토리만 표시하지 않고도 특정 부분에 액세스할 수 있습니다. 예를 들어 액세스 제어 및 사용자 하위 디렉토리만 [!DNL Server Files Manager] 표시하는 별도의 디렉토리를 만들어 사용자와 해당 액세스를 관리할 수 있습니다.

만드는 각 관리자에는 [!DNL .vw] 파일이 있어야 합니다. 이 [!DNL Server Files.vw] 파일을 템플릿으로 사용할 수 있습니다.

자세한 내용은 [!DNL Server Files Manager]서버 파일 [관리자를 참조하십시오](../../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4).

**서버 파일 관리자를 만들려면**

1. 에서 [!DNL Profile Manager]디렉토리를 **[!UICONTROL Menu]** 클릭한 다음 **[!UICONTROL Admin]** 디렉토리를 클릭합니다. 이 [!DNL Server Files.vw] 파일은 여기에 있습니다.
1. 프로필 이름 *열에서* 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Server Files.vw] **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 열에서 해당 [!DNL Server Files.vw] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Open]** **[!UICONTROL from the workbench]**&#x200B;을 클릭합니다. 파일이 [!DNL Server Files.vw] 열립니다.
1. 디렉토리를 제거하려면 위쪽 테두리를 마우스 오른쪽 버튼으로 클릭하고 [!DNL Server Files Manager] > **[!UICONTROL Server Directories]** > **[!UICONTROL Remove]** &lt; *>**[!UICONTROL directory name]***&#x200B;를 클릭합니다.
1. 디렉토리를 추가하려면 의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 [!DNL Server Files Manager]> **[!UICONTROL Server Directories]** > **[!UICONTROL Add]** **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

   URI 필드에 디렉토리 URI를 입력하고 을 **[!UICONTROL OK]**&#x200B;클릭합니다.

   >[!NOTE]
   >
   >URI 필드에서 여러 디렉토리를 지정할 수 있습니다. 예를 들어 [!DNL Profiles\Marketing\]을 입력하면 서버 파일 관리자에 Marketing 하위 디렉토리가 포함되지만 Profiles 디렉터리 내에 다른 하위 디렉터리가 없습니다.

1. 위쪽 테두리의 맨 위를 마우스 오른쪽 단추로 [!DNL Server Files Manager] 클릭하고 **[!UICONTROL Save]**&#x200B;클릭합니다.
1. 새 관리자를 만들려면 [!DNL File Name] 필드에서 파일 이름을 변경한 다음 을 클릭합니다 **[!UICONTROL Save]**. 기존 관리자를 덮어쓰려면 을 **[!UICONTROL Save]**&#x200B;클릭합니다.
1. (선택 사항) 작업 중인 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 열에서 해당 [!DNL .vw] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다 [!DNL User] .

   그런 후 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

