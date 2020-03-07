---
description: Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하며, 작업 영역 name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.
solution: Analytics
title: Folder.lock 및 workspace.lock 파일
topic: Data workbench
uuid: d4c69e16-0596-4542-854f-bc614167ae80
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Folder.lock 및 workspace.lock 파일{#folder-lock-and-workspace-lock-files}

Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하며, 작업 영역 name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.

전체 폴더를 잠글 때 작업 영역 폴더 수준 또는 하위 폴더(탭) 수준에서 잠글 수 있습니다. 또한 모든 폴더(작업 영역 폴더 수준)를 잠그거나 잠금 해제한 다음 특정 하위 폴더( [!DNL folder.lock] 파일 사용) 또는 특정 작업 영역( *작업 영역 name*.lock 파일 사용)에 대한 예외를 지정할 수 있습니다.

다음 예에서는 세 가지 요소를 [!DNL Profile Manager] 강조 표시합니다.

* 기본 작업 영역 폴더에 대한 [!DNL folder.lock] 파일
* 작업 공간 [!DNL Monthly Numbers.lock] 파일에 대한 [!DNL Monthly Numbers.vw] 파일

* 작업 영역\사용자 정의 하위 폴더에 대한 [!DNL folder.lock] 파일

![](assets/wsp_Locking_lockFiles.png)

이 예에서는 파일이 잠기도록 설정되어 [!DNL Workspaces folder.lock] 있으며 이 Data Workbench 인스턴스에 있는 모든 작업 영역이 잠깁니다. Workspaces\Custom 하위 폴더 [!DNL folder.lock] 파일이 잠금 해제되어 [!DNL Custom] 탭의 모든 작업 영역이 잠깁니다. 마지막으로, 파일은 잠금으로 설정되어 [!DNL Monthly Numbers.lock] 있으므로 월별 번호 작업 영역이 잠깁니다.

## .lock 파일 만들기 {#section-c4f78b4b43c347368a376904effb41d2}

또는 의 [!DNL new folder.lock] 옵션을 사용하여 [!DNL Create menu] 파일을 만들 수 [!DNL Profile Manager] [!DNL Workspaces Manager]있습니다. 또한 기존 [!DNL folder.lock] 파일을 적절한 폴더에 복사하여 붙여 넣고 파일 이름( *작업 공간 이름*.lock 파일에만 해당)을 변경하고 필요한 경우 파일의 설정을 변경하여 [!DNL .lock] 또는 *작업 영역 이름*.lock 파일을 만들 수 있습니다.

**새 folder.lock 파일을 만들려면**

1. 데이터 워크벤치에서 작업 영역 내에서 마우스 오른쪽 단추를 [!DNL Workspaces Manager] 클릭하여 을 열고 **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]**&#x200B;을 클릭합니다.
1. [!DNL folder.lock] 파일을 만들 폴더를 클릭합니다.
1. 해당 폴더의 [!DNL User] 열에서 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Create]** > **[!UICONTROL folder.lock]**&#x200B;을 클릭합니다. 파일이 [!DNL new folder.lock] 나타납니다. [!DNL New folder.lock] 파일은 기본적으로 [잠금 해제된] 상태로 설정됩니다.
1. (선택 사항) 파일의 설정을 변경해야 하는 경우:

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 파일이 [!DNL folder.lock] 열립니다.

   1. 설정을 [잠금으로]변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 동일한 작업 프로필을 사용하여 작업하는 모든 사용자에 대해 이 설정을 설정하려면 해당 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*&#x200B;을 클릭합니다.

이제 이 폴더의 작업 영역은 새 파일의 설정에 따라 잠기거나 잠금 해제됩니다.

**기존 파일에서 .lock 파일을 만들려면**

1. 또는 에서 [!DNL Profile Manager] 기존 [!DNL Workspaces Manager]파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL .lock] **[!UICONTROL Copy]**&#x200B;을 클릭합니다.
1. 파일을 붙여넣을 폴더의 [!DNL User] 열에서 [!DNL .lock] 셀을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Paste]**.
1. 이 파일을 사용하여 개별 작업 영역을 잠글 경우 [!DNL .lock] 열의 [!DNL User] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL File] 필드에서 해당 이름을 변경하여 잠글 작업 영역의 이름과 일치시킵니다.

   예를 들어 [!DNL Monthly Numbers.vw] 작업 영역을 잠그려면 파일 이름을 &quot; [!DNL Monthly Numbers.lock]&quot;로 지정합니다.이 파일을 사용하여 개별 작업 영역을 잠글 경우 [!DNL .lock] 열의 [!DNL User] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL File] 필드에서 해당 이름을 변경하여 잠글 작업 영역의 이름과 일치시킵니다. 예를 들어 [!DNL Monthly Numbers.vw] 작업 영역을 잠그려면 파일 이름을 &quot; [!DNL Monthly Numbers.lock]&quot;로 지정합니다.

1. 파일의 설정을 변경하려면:

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 파일이 [!DNL .lock] 열립니다.

   1. 설정을 [잠김] 또는 [잠금 해제됨으로 변경합니다].
   1. 파일을 저장하고 닫습니다.

1. 동일한 작업 프로필을 사용하여 작업하는 모든 사용자에 대해 이 설정을 설정하려면 해당 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*&#x200B;을 클릭합니다.

이제 선택한 작업 영역이 새 파일의 설정에 따라 잠기거나 잠금 해제됩니다.
