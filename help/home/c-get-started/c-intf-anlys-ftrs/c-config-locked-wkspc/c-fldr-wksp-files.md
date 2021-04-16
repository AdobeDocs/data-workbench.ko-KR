---
description: Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하는 반면, 작업 공간 name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.
title: Folder.lock 및 workspace.lock 파일
uuid: d4c69e16-0596-4542-854f-bc614167ae80
exl-id: 980b8692-8aa5-481f-b6bc-33836d8a3a76
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 1%

---

# Folder.lock 및 workspace.lock 파일{#folder-lock-and-workspace-lock-files}

Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하는 반면, 작업 공간 name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.

전체 폴더를 잠그면 [작업 영역] 폴더 수준 또는 하위 폴더(탭) 수준에서 잠글 수 있습니다. 모든 폴더(작업 영역 폴더 수준에서)를 잠그거나 잠금 해제할 수도 있고, 특정 하위 폴더([!DNL folder.lock] 파일 사용) 또는 특정 작업 영역(*작업 영역 이름*.lock 파일 사용)에 대한 예외를 지정할 수도 있습니다.

다음 [!DNL Profile Manager] 예제에서는 3개의 요소를 강조 표시합니다.

* 기본 작업 영역 폴더에 대한 [!DNL folder.lock] 파일
* [!DNL Monthly Numbers.vw] 작업 영역 파일에 대한 [!DNL Monthly Numbers.lock] 파일

* 작업 영역\사용자 정의 하위 폴더에 대한 [!DNL folder.lock] 파일

![](assets/wsp_Locking_lockFiles.png)

이 예에서 [!DNL Workspaces folder.lock] 파일은 잠금으로 설정되어 이 Data Workbench 인스턴스에 있는 모든 작업 영역이 잠깁니다. Workspaces\Custom 하위 폴더 [!DNL folder.lock] 파일이 잠금 해제되어 [!DNL Custom] 탭에서 모든 작업 영역을 잠금 해제합니다. 마지막으로 [!DNL Monthly Numbers.lock] 파일은 잠금으로 설정되어 월별 숫자 작업 영역이 잠깁니다.

## .lock 파일 만들기 {#section-c4f78b4b43c347368a376904effb41d2}

[!DNL Profile Manager] 또는 [!DNL Workspaces Manager]에서 [!DNL Create menu] 옵션을 사용하여 [!DNL new folder.lock] 파일을 만들 수 있습니다. 기존 [!DNL .lock] 파일을 적절한 폴더로 복사하여 붙여 넣고 파일 이름을 변경하고 필요한 경우 *작업 공간 이름*.lock 파일의 설정을 변경하여 [!DNL folder.lock] 또는 *작업 공간 이름*.lock 파일을 만들 수도 있습니다.

**새 folder.lock 파일을 만들려면**

1. Data Workbench에서 작업 영역 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]**&#x200B;를 클릭하여 [!DNL Workspaces Manager]을 엽니다.
1. [!DNL folder.lock] 파일을 만들 폴더를 클릭합니다.
1. 해당 폴더의 [!DNL User] 열에서 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Create]** > **[!UICONTROL folder.lock]**&#x200B;를 클릭합니다. [!DNL new folder.lock] 파일이 나타납니다. [!DNL New folder.lock] 파일은 기본적으로  [] unlockeded로 설정됩니다.
1. (선택 사항) 파일의 설정을 변경해야 하는 경우:

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. [!DNL folder.lock] 파일이 열립니다.

   1. 설정을 [잠근]으로 변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 이 설정을 동일한 작업 프로필을 사용하는 모든 사용자에 대한 설정으로 만들려면 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;을 클릭합니다.

이제 새 파일의 설정에 따라 이 폴더의 작업 영역이 잠기거나 잠금 해제됩니다.

**기존 파일에서 .lock 파일을 만들려면**

1. [!DNL Profile Manager] 또는 [!DNL Workspaces Manager]에서 기존 [!DNL .lock] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]**&#x200B;을 클릭합니다.
1. [!DNL .lock] 파일을 붙여 넣을 폴더의 [!DNL User] 열에서 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]**&#x200B;를 클릭합니다.
1. 이 파일을 사용하여 개별 작업 영역을 잠그는 경우 [!DNL User] 열의 [!DNL .lock] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL File] 필드에서 해당 이름을 변경하여 잠그려는 작업 영역의 이름과 일치시킵니다.

   예를 들어 [!DNL Monthly Numbers.vw] 작업 영역을 잠그려면 &quot;[!DNL Monthly Numbers.lock]&quot; 파일의 이름을 지정합니다.이 파일을 사용하여 개별 작업 영역을 잠그는 경우 [!DNL User] 열의 [!DNL .lock] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL File] 필드에서 해당 이름을 변경하여 잠그려는 작업 영역의 이름과 일치시킵니다. 예를 들어 [!DNL Monthly Numbers.vw] 작업 영역을 잠그려면 &quot;[!DNL Monthly Numbers.lock]&quot; 파일의 이름을 지정합니다.

1. 파일의 설정을 변경하려면:

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. [!DNL .lock] 파일이 열립니다.

   1. 설정을 [잠김] 또는 [잠금 해제됨]으로 변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 이 설정을 동일한 작업 프로필을 사용하는 모든 사용자에 대한 설정으로 만들려면 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;을 클릭합니다.

이제 새 파일의 설정에 따라 선택한 작업 영역이 잠기거나 잠금 해제됩니다.
