---
description: 프로필 관리자는 작업 프로필과 관련된 모든 디렉토리를 표시합니다.
solution: Analytics
title: 프로필 관리자 만들기
topic: Data workbench
uuid: e16741e2-740b-4f57-861d-e2f57d30abbc
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 프로필 관리자 만들기{#create-a-profile-manager}

프로필 관리자는 작업 프로필과 관련된 모든 디렉토리를 표시합니다.

전체 디렉토리 구조를 검색하지 [!DNL Profile Manager] 않고도 의 하위 디렉토리에 액세스할 수 있습니다. 예를 들어 작업 공간 창 [!DNL Metrics] 메뉴의 메뉴에서 사용할 수 있는 [!DNL Workspaces] 및 [!DNL Manage] 메뉴 옵션을 사용하여 각각 프로필 관리자 지표 및 작업 영역 폴더를 열 수 있습니다.

자세한 내용은 [!DNL Profile Manager]프로필 [관리자를 참조하십시오](https://docs.adobe.com/content/help/en/data-workbench/using/client/ui-analysis-features/cstm-prof-files-mgrs/c-new-prof-mgrs.html).

기본적으로 다음 관리자에 액세스할 수 있습니다.

* **[!DNL Metrics Manager]:**프로필 관리자의 지표 폴더의 컨텐츠를 표시합니다. 각 프로필 내에 정의된 지표를 열거나 편집하거나 제거하거나 복사할 수 있습니다.
* **[!DNL Reports Manager]:**프로필 관리자의 보고서 폴더의 컨텐츠를 표시합니다. 보고서 작업 영역 또는[!DNL report.cfg]파일을 열거나 편집하거나 제거하거나 복사할 수 있습니다.

* **[!DNL Workspaces Manager]:**프로필 관리자의 작업 영역 폴더의 컨텐츠를 표시합니다. 탭을 구성하기 위한 모든 파일이[!DNL Worktop]여기에 있습니다. 작업[상단 탭 사용자 지정을 참조하십시오](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md).

데이터 워크벤치를 사용하면 에서 하위 디렉토리 하나를 표시하는 추가 프로필 관리자를 만들 수 [!DNL Profile Manager]있습니다. 만드는 각 관리자에는 컨텐츠가 표시되는 디렉토리 및 해당 창의 속성을 지정하는 [!DNL .vw] [!DNL Profile Manager] 파일이 있어야 합니다. 제공된 관리자 중 하나에 대해 해당 [!DNL .vw] 파일을 템플릿으로 사용할 수 있습니다.

**프로필 관리자를 만들려면**

1. 에서 [!DNL Profile Manager]해당 **[!UICONTROL Menu]** 디렉토리를 클릭하여 해당 컨텐츠를 봅니다.
1. Menu 디렉토리에서 **[!UICONTROL Admin]** 디렉토리를 클릭한 다음 **[!UICONTROL Profile]** 디렉토리를 클릭합니다. 기존 관리자용 [!DNL .vw] 파일은 여기에 있습니다.
1. 프로필 이름 *열에서* 파일 중 하나(예: [!DNL .vw] )에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Workspaces.vw]**[!UICONTROL Make Local]**&#x200B;을 클릭합니다.

   파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

1. 열에서 해당 [!DNL .vw] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다.
1. 필드에 새 관리자를 만들 디렉토리를 [!DNL Profile Path] [!DNL Profile Manager] 입력합니다. 디렉토리 이름 뒤에 슬래시(/)를 포함해야 합니다.

   ```
   window = simpleBorderWindow:
   client = scrollWindow: 
   client = fileManager:
     Profile Path = string: directory name/
     size = v3d: (820, 5649, 0)
     scroll_offset = v3d: (0, 0, 0)
     size = v3d: (830, 881, 0)
     pos = v3d: (525, 162, 0)
     size = v3d: (830, 900, 0)
   ```

1. 메모장에서 > **[!UICONTROL File]** 을 **[!UICONTROL Save As]** 클릭하여 편집된 파일을 데이터 워크벤치 설치 폴더\User\* *작업 프로필 이름*\Menu\Admin\Profile Management폴더에*&#x200B;저장합니다.

   해당 파일의 디렉토리를 반영하려면 [!DNL .vw] 파일 이름을 변경해야 [!DNL Profile Manager] 합니다.

1. (선택 사항) 작업 중인 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL .vw] 열에서 해당 [!DNL User] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > &lt; **[!UICONTROL working profile name]**>을 클릭합니다.

