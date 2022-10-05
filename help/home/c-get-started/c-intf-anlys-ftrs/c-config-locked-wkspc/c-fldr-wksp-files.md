---
description: Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하는 반면 workspace name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.
title: Folder.lock 및 workspace.lock 파일
uuid: d4c69e16-0596-4542-854f-bc614167ae80
exl-id: 980b8692-8aa5-481f-b6bc-33836d8a3a76
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 1%

---

# Folder.lock 및 workspace.lock 파일{#folder-lock-and-workspace-lock-files}

{{eol}}

Data Workbench 설치 디렉토리의 Workspaces 폴더 내에서 folder.lock 파일은 특정 폴더의 작업 영역이 잠겨 있는지 여부를 지정하는 반면 workspace name.lock 파일은 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.

전체 폴더를 잠글 때 작업 공간 폴더 수준 또는 하위 폴더(탭) 수준에서 잠글 수 있습니다. 모든 폴더를 잠그거나 잠금 해제할 수도 있습니다(작업 공간 폴더 수준에서). 그런 다음 특정 하위 폴더에 대한 예외를 지정할 수도 있습니다 [!DNL folder.lock] 파일 또는 특정 작업 공간( *작업 공간 이름*.lock 파일).

다음 예제 의 [!DNL Profile Manager] 세 가지 요소를 강조 표시합니다.

* A [!DNL folder.lock] 기본 작업 공간 폴더의 파일
* A [!DNL Monthly Numbers.lock] 파일 [!DNL Monthly Numbers.vw] 작업 공간 파일

* A [!DNL folder.lock] 작업 공간\사용자 지정 하위 폴더의 파일

![](assets/wsp_Locking_lockFiles.png)

이 예에서 [!DNL Workspaces folder.lock] 파일이 잠긴 것으로 설정되어 이 Data Workbench 인스턴스에 있는 모든 작업 영역이 잠깁니다. Workspaces\Custom 하위 폴더 [!DNL folder.lock] 파일이 잠금 해제로 설정되어 파일의 모든 작업 공간을 잠금 해제합니다. [!DNL Custom] 탭. 마지막으로, [!DNL Monthly Numbers.lock] 파일이 잠긴 것으로 설정되어 월별 숫자 작업 영역을 잠급니다.

## .lock 파일 만들기 {#section-c4f78b4b43c347368a376904effb41d2}

을(를) 만들 수 있습니다 [!DNL new folder.lock] 파일을 [!DNL Create menu] 옵션 [!DNL Profile Manager] 또는 [!DNL Workspaces Manager]. 또한 [!DNL folder.lock] 또는 *작업 공간 이름*&#x200B;기존 파일을 복사하여 붙여넣어 .lock 파일 [!DNL .lock] 파일을 해당 폴더로 이동하여 파일의 이름을 변경합니다(용). *작업 공간 이름*.lock 파일만 해당), 필요한 경우 파일에서 설정을 변경합니다.

**새 folder.lock 파일을 만들려면**

1. Data Workbench에서 [!DNL Workspaces Manager] 작업 공간 내에서 마우스 오른쪽 단추 클릭 및 **[!UICONTROL Manage]** > **[!UICONTROL Profile]** > **[!UICONTROL Workspaces Manager]**.
1. 만들 폴더를 클릭합니다 [!DNL folder.lock] 파일.
1. 에서 [!DNL User] 해당 폴더의 열에서 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Create]** > **[!UICONTROL folder.lock]**. A [!DNL new folder.lock] 파일이 나타납니다. [!DNL New folder.lock] 파일이 [unlocked] 기본적으로 제공됩니다.
1. (선택 사항) 파일에서 설정을 변경해야 하는 경우:

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 다음 [!DNL folder.lock] 파일이 열립니다.

   1. 설정을 (으)로 변경합니다. [잠김].
   1. 파일을 저장하고 닫습니다.

1. 동일한 작업 프로필을 사용하여 작업하는 모든 사용자에 대해 이 설정을 설정하려면 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

이제 이 폴더의 작업 공간은 새 파일의 설정에 따라 잠기거나 잠금 해제됩니다.

**기존 파일에서 .lock 파일을 만들려면**

1. 에서 [!DNL Profile Manager] 또는 [!DNL Workspaces Manager]기존 [!DNL .lock] 를 클릭하고 **[!UICONTROL Copy]**.
1. 에서 [!DNL User] 붙여넣을 폴더의 열 [!DNL .lock] 파일에서 셀을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Paste]**.
1. 이 파일을 사용하여 개별 작업 영역을 잠그면 [!DNL .lock] 파일의 [!DNL User] 열 및 이름 변경 [!DNL File] 잠글 작업 영역의 이름과 일치하는 필드입니다.

   예를 들어, [!DNL Monthly Numbers.vw] 작업 영역에서 파일 이름을 &quot; [!DNL Monthly Numbers.lock].&quot;이 파일을 사용하여 개별 작업 영역을 잠그면 [!DNL .lock] 파일의 [!DNL User] 열 및 이름 변경 [!DNL File] 잠글 작업 영역의 이름과 일치하는 필드입니다. 예를 들어, [!DNL Monthly Numbers.vw] 작업 영역에서 파일 이름을 &quot; [!DNL Monthly Numbers.lock].&quot;

1. 파일에서 설정을 변경하려면 다음을 수행하십시오.

   1. 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 다음 [!DNL .lock] 파일이 열립니다.

   1. 설정을 (으)로 변경합니다. [잠김] 또는 [unlocked].
   1. 파일을 저장하고 닫습니다.

1. 동일한 작업 프로필을 사용하여 작업하는 모든 사용자에 대해 이 설정을 설정하려면 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

이제 선택한 작업 공간이 새 파일의 설정에 따라 잠겨 있거나 잠금이 해제됩니다.
