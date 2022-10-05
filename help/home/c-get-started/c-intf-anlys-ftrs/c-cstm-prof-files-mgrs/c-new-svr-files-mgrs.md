---
description: 서버 파일 관리자는 구성 및 조회 파일을 포함하여 Data Workbench 서버 설치 디렉토리에 있는 모든 디렉토리를 표시합니다.
title: 서버 파일 관리자 만들기
uuid: 9fb2163d-3756-40d2-9817-4a89bd8a38c9
exl-id: 9e0c8144-0f52-4e46-85d8-c2dcd60ddcb8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 3%

---

# 서버 파일 관리자 만들기{#create-a-server-files-manager}

{{eol}}

서버 파일 관리자는 구성 및 조회 파일을 포함하여 Data Workbench 서버 설치 디렉토리에 있는 모든 디렉토리를 표시합니다.

일부 또는 [!DNL Server Files Manager] 전체 디렉토리 구조를 탐색하거나 특정 요구 사항을 해결하기 위해 몇 개의 하위 디렉토리만 표시할 필요가 없습니다. 예를 들어, 별도의 [!DNL Server Files Manager] 에는 액세스 제어 및 사용자 하위 디렉토리만 표시되어 사용자와 사용자 액세스를 관리할 수 있습니다.

만드는 각 관리자에는 [!DNL .vw] 파일. 를 사용할 수 있습니다 [!DNL Server Files.vw] 파일로 내보낼 때 시간별 세부기간이 작동하지 않는 문제를 해결했습니다.

에 대한 자세한 정보 [!DNL Server Files Manager]를 참조하십시오. [서버 파일 관리자](../../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4).

**서버 파일 관리자를 만들려면**

1. 에서 [!DNL Profile Manager]를 클릭하고 **[!UICONTROL Menu]** 디렉토리, **[!UICONTROL Admin]** 디렉토리. 다음 [!DNL Server Files.vw] 파일이 여기에 있습니다.
1. 에서 *프로필 이름* 열에서 [!DNL Server Files.vw] 를 클릭하고 **[!UICONTROL Make Local]**. 파일에 대한 확인 표시가 [!DNL User] 열.
1. 에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Server Files.vw] 파일의 [!DNL User] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 다음 [!DNL Server Files.vw] 파일이 열립니다.
1. 디렉토리를 제거하려면 [!DNL Server Files Manager] 을(를) 클릭합니다. **[!UICONTROL Server Directories]** > **[!UICONTROL Remove]** > *&lt;**[!UICONTROL directory name]**>*.
1. 디렉토리를 추가하려면 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Server Directories]** > **[!UICONTROL Add]** > **[!UICONTROL Directory]**.

   URI 필드에 디렉토리 URI를 입력하고 **[!UICONTROL OK]**.

   >[!NOTE]
   >
   >URI 필드에서 여러 디렉토리를 지정할 수 있습니다. 예를 들어 [!DNL Profiles\Marketing\]를 입력하면 서버 파일 관리자에 Marketing 하위 디렉터리가 들어 있지만, Profiles 디렉터리 내에 다른 하위 디렉터리는 없습니다.

1. 위쪽 테두리를 마우스 오른쪽 단추로 클릭합니다. [!DNL Server Files Manager] 을(를) 클릭합니다. **[!UICONTROL Save]**.
1. 새 관리자를 만들려면 [!DNL File Name] 필드를 클릭한 다음 **[!UICONTROL Save]**. 기존 관리자를 덮어쓰려면 **[!UICONTROL Save]**.
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL .vw] 파일의 [!DNL User] 열.

   그런 후 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
