---
description: 프로필 관리자는 작업 프로필과 연관된 모든 디렉토리를 표시합니다.
title: 프로필 관리자 만들기
uuid: e16741e2-740b-4f57-861d-e2f57d30abbc
exl-id: 43b95473-ab3e-4a80-9b91-7c221e74b096
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 2%

---

# 프로필 관리자 만들기{#create-a-profile-manager}

{{eol}}

프로필 관리자는 작업 프로필과 연관된 모든 디렉토리를 표시합니다.

의 하위 디렉토리에 액세스할 수 있습니다 [!DNL Profile Manager] 전체 디렉토리 구조를 탐색하지 않아도 됩니다. 예: [!DNL Metrics] 및 [!DNL Workspaces] 메뉴 옵션에서 사용할 수 있습니다. [!DNL Manage] workspace 창 메뉴의 메뉴를 사용하여 각각 프로필 관리자 지표 및 작업 공간 폴더를 열 수 있습니다.

에 대한 자세한 정보 [!DNL Profile Manager]를 참조하십시오. [프로필 관리자](https://experienceleague.adobe.com/docs/data-workbench/using/client/ui-analysis-features/cstm-prof-files-mgrs/c-new-prof-mgrs.html).

기본적으로 다음 관리자에 액세스할 수 있습니다.

* **[!DNL Metrics Manager]:** 프로필 관리자의 지표 폴더의 컨텐츠를 표시합니다. 각 프로필 내에 정의된 지표를 열기, 편집, 제거 또는 복사할 수 있습니다.
* **[!DNL Reports Manager]:** 프로필 관리자 보고서 폴더의 컨텐츠를 표시합니다. 보고서 작업 공간을 열거나, 편집하거나, 제거하거나, 복사할 수 있습니다. [!DNL report.cfg] 파일.

* **[!DNL Workspaces Manager]:** 프로필 관리자의 작업 공간 폴더의 컨텐츠를 표시합니다. 구성을 위한 모든 파일 [!DNL Worktop]탭은 여기에 있습니다. 자세한 내용은 [worktop 탭 사용자 정의](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md).

Data Workbench을 사용하면 하위 디렉터리에서 하위 디렉터리를 표시하는 추가 프로필 관리자를 만들 수 있습니다 [!DNL Profile Manager]. 만드는 각 관리자에는 [!DNL .vw] 를 지정하는 파일 [!DNL Profile Manager] 내용이 표시되는 디렉토리와 해당 창의 등록 정보를 포함합니다. 를 사용할 수 있습니다 [!DNL .vw] 제공된 관리자를 템플릿으로 사용합니다.

**프로필 관리자를 만들려면**

1. 에서 [!DNL Profile Manager]를 클릭하고 **[!UICONTROL Menu]** 디렉토리 을 클릭하여 컨텐츠를 확인합니다.
1. 메뉴 디렉토리 내에서 **[!UICONTROL Admin]** 디렉토리 및 **[!UICONTROL Profile]** 디렉토리. 다음 [!DNL .vw] 기존 관리자의 파일은 여기에 있습니다.
1. 에서 *프로필 이름* 열에서 다음 중 하나에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL .vw] 파일(예: [!DNL Workspaces.vw])를 클릭한 다음 **[!UICONTROL Make Local]**.

   파일에 대한 확인 표시가 [!DNL User] 열.

1. 에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL .vw] 파일의 [!DNL User] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. 에서 [!DNL Profile Path] 필드에 을 입력합니다 [!DNL Profile Manager] 새 관리자를 만들 디렉토리입니다. 디렉토리 이름 뒤에 슬래시(/)를 포함해야 합니다.

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

1. 메모장에서 **[!UICONTROL File]** > **[!UICONTROL Save As]** 편집한 파일을 *Data Workbench 설치 폴더*\User\*working profile name*\Menu\Admin\Profile Management

   이름을 변경해야 합니다 [!DNL .vw] 파일을 사용하여 [!DNL Profile Manager] 해당 위치에 표시됩니다.

1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL .vw] 파일의 [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > &lt; **[!UICONTROL working profile name]**>.
