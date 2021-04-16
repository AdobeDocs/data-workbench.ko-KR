---
description: 서버 파일 관리자는 구성 및 조회 파일을 포함하여 Data Workbench 서버 설치 디렉토리에 있는 모든 디렉토리를 표시합니다.
title: 서버 파일 관리자 만들기
uuid: 9fb2163d-3756-40d2-9817-4a89bd8a38c9
exl-id: 9e0c8144-0f52-4e46-85d8-c2dcd60ddcb8
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 3%

---

# 서버 파일 관리자 만들기{#create-a-server-files-manager}

서버 파일 관리자는 구성 및 조회 파일을 포함하여 Data Workbench 서버 설치 디렉토리에 있는 모든 디렉토리를 표시합니다.

특정 요구 사항을 해결하기 위해 전체 디렉토리 구조를 탐색하거나 일부 하위 디렉토리만 표시하지 않고도 [!DNL Server Files Manager]의 일부에 액세스할 수 있습니다. 예를 들어 액세스 제어 및 사용자 하위 디렉토리만 표시하는 별도의 [!DNL Server Files Manager]을 만들어 사용자와 액세스 권한을 관리할 수 있습니다.

만드는 각 관리자에는 [!DNL .vw] 파일이 있어야 합니다. [!DNL Server Files.vw] 파일을 템플릿으로 사용할 수 있습니다.

[!DNL Server Files Manager]에 대한 자세한 내용은 [서버 파일 관리자](../../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4)를 참조하십시오.

**서버 파일 관리자를 만들려면**

1. [!DNL Profile Manager]에서 **[!UICONTROL Menu]** 디렉토리를 클릭한 다음 **[!UICONTROL Admin]** 디렉토리를 클릭합니다. [!DNL Server Files.vw] 파일이 여기에 있습니다.
1. *프로필 이름* 열에서 [!DNL Server Files.vw] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 파일의 확인 표시가 [!DNL User] 열에 나타납니다.
1. [!DNL User] 열에서 [!DNL Server Files.vw] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. [!DNL Server Files.vw] 파일이 열립니다.
1. 디렉토리를 제거하려면 [!DNL Server Files Manager]의 위쪽 테두리를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Server Directories]** > **[!UICONTROL Remove]** > *&lt;**[!UICONTROL directory name]***&#x200B;를 클릭합니다.
1. 디렉토리를 추가하려면 [!DNL Server Files Manager]의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Directories]** > **[!UICONTROL Add]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

   URI 필드에 디렉토리 URI를 입력하고 **[!UICONTROL OK]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >URI 필드에 여러 디렉토리를 지정할 수 있습니다. 예를 들어  [!DNL Profiles\Marketing\]을 입력하면 서버 파일 관리자에 Marketing 하위 디렉터리가 포함되지만 Profiles 디렉터리 내의 다른 하위 디렉터리가 없습니다.

1. [!DNL Server Files Manager]의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. 새 관리자를 만들려면 [!DNL File Name] 필드에서 파일 이름을 변경한 다음 **[!UICONTROL Save]**&#x200B;을 클릭합니다. 기존 관리자를 덮어쓰려면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL User] 열에서 [!DNL .vw] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.

   그런 후 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
