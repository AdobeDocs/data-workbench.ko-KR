---
description: Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하는 반면 workspace name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.
title: Folder.lock 및 workspace.lock 파일
uuid: d4c69e16-0596-4542-854f-bc614167ae80
exl-id: 980b8692-8aa5-481f-b6bc-33836d8a3a76
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 1%

---

# Folder.lock 및 workspace.lock 파일{#folder-lock-and-workspace-lock-files}

Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하는 반면 workspace name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.

전체 폴더를 잠글 때 작업 공간 폴더 수준 또는 하위 폴더(탭) 수준에서 잠글 수 있습니다. 모든 폴더를 잠그거나 잠금 해제할 수도 있습니다(작업 공간 폴더 수준에서). 그런 다음 특정 하위 폴더([!DNL folder.lock] 파일 사용) 또는 특정 작업 공간(*작업 공간 이름*.lock 파일 사용)에 대한 예외를 지정할 수도 있습니다.

[!DNL Profile Manager] 의 다음 예에서는 세 가지 요소를 강조 표시합니다.

* 기본 작업 공간 폴더의 [!DNL folder.lock] 파일
* [!DNL Monthly Numbers.vw] 작업 공간 파일에 대한 [!DNL Monthly Numbers.lock] 파일

* Workspaces\Custom 하위 폴더의 [!DNL folder.lock] 파일

![](assets/wsp_Locking_lockFiles.png)

이 예제에서 [!DNL Workspaces folder.lock] 파일은 잠금으로 설정되어 이 Data Workbench 인스턴스의 모든 작업 영역을 잠급니다. Workspaces\Custom 하위 폴더 [!DNL folder.lock] 파일이 잠금으로 설정되어 [!DNL Custom] 탭에서 모든 작업 공간을 잠금 해제합니다. 마지막으로 [!DNL Monthly Numbers.lock] 파일이 잠금으로 설정되어 월별 숫자 작업 영역이 잠깁니다.

## .lock 파일 만들기 {#section-c4f78b4b43c347368a376904effb41d2}

[!DNL Profile Manager] 또는 [!DNL Workspaces Manager]에서 [!DNL Create menu] 옵션을 사용하여 [!DNL new folder.lock] 파일을 만들 수 있습니다. 기존 [!DNL .lock] 파일을 적절한 폴더에 복사하여 붙여넣고 파일 이름을 변경하고(*workspace name*.lock 파일만 해당) 필요한 경우 파일의 설정을 변경하여 [!DNL folder.lock] 또는 *작업 공간 이름*.lock 파일을 만들 수도 있습니다.

**새 folder.lock 파일을 만들려면**

1. Data Workbench에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하여 [!DNL Workspaces Manager] 를 열고 **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]** 를 클릭합니다.
1. [!DNL folder.lock] 파일을 만들 폴더를 클릭합니다.
1. 해당 폴더의 [!DNL User] 열에서 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Create]** > **[!UICONTROL folder.lock]** 를 클릭합니다. [!DNL new folder.lock] 파일이 나타납니다. [!DNL New folder.lock] 파일은 기본적 [] 으로 unlockeddedn으로 설정됩니다.
1. (선택 사항) 파일에서 설정을 변경해야 하는 경우:

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. [!DNL folder.lock] 파일이 열립니다.

   1. 설정을 [잠긴]으로 변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 동일한 작업 프로필을 사용하는 모든 사용자에 대해 설정을 지정하려면 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.

이제 이 폴더의 작업 공간은 새 파일의 설정에 따라 잠기거나 잠금 해제됩니다.

**기존 파일에서 .lock 파일을 만들려면**

1. [!DNL Profile Manager] 또는 [!DNL Workspaces Manager]에서 기존 [!DNL .lock] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]** 를 클릭합니다.
1. [!DNL .lock] 파일을 붙여넣을 폴더의 [!DNL User] 열에서 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]** 를 클릭합니다.
1. 이 파일을 사용하여 개별 작업 영역을 잠그면 [!DNL User] 열에서 [!DNL .lock] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL File] 필드에서 해당 이름을 변경하여 잠글 작업 영역의 이름과 일치시킵니다.

   예를 들어 [!DNL Monthly Numbers.vw] 작업 영역을 잠그려면 파일 이름을 &quot;[!DNL Monthly Numbers.lock]&quot;로 지정합니다.이 파일을 사용하여 개별 작업 영역을 잠그면 [!DNL User] 열에서 [!DNL .lock] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL File] 필드에서 해당 이름을 변경하여 잠글 작업 영역의 이름과 일치시킵니다. 예를 들어 [!DNL Monthly Numbers.vw] 작업 영역을 잠그려면 파일 이름을 &quot;[!DNL Monthly Numbers.lock]&quot;로 지정합니다.

1. 파일에서 설정을 변경하려면 다음을 수행하십시오.

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. [!DNL .lock] 파일이 열립니다.

   1. 설정을 [잠긴] 또는 [잠금 해제된]로 변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 동일한 작업 프로필을 사용하는 모든 사용자에 대해 설정을 지정하려면 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.

이제 선택한 작업 공간이 새 파일의 설정에 따라 잠겨 있거나 잠금이 해제됩니다.
