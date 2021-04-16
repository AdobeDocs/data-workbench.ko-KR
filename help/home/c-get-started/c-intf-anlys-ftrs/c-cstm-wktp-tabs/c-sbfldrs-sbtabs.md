---
description: 기본적으로 새로 만든 탭은 연결된 디렉토리 내의 하위 폴더를 하위 탭이 아닌 계층적 드롭다운 하위 디렉터리로 표시합니다.
title: 하위 폴더를 하위 탭으로 표시
uuid: b4d7c6dd-d5ad-4b93-ba67-65a69e11eefc
exl-id: 6a05852b-3efc-4e71-9782-d4cc3a687a26
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 3%

---

# 하위 폴더를 하위 탭으로 표시{#display-subfolders-as-subtabs}

기본적으로 새로 만든 탭은 연결된 디렉토리 내의 하위 폴더를 하위 탭이 아닌 계층적 드롭다운 하위 디렉터리로 표시합니다.

다음 예제와 같이 Data Workbench 설치 디렉토리 내에 *작업 프로필 이름*\Workspaces\*tab name 폴더*에 [!DNL empty folder.useTabs] 파일을 배치하여 하위 폴더를 하위 탭으로 표시할 수 있습니다.

다음 예제는 드롭다운 하위 디렉토리가 있는 [!DNL Custom] 탭을 보여줍니다.

![](assets/client-sub.png)

[!DNL empty folder.useTabs] 파일을 Workspaces\Custom 폴더에 배치하는 경우 다음 예와 같이 Custom 폴더 내의 모든 하위 폴더가 [!DNL Worktop]에 하위 탭으로 표시됩니다.

![](assets/client-sub2.png)

**하위 폴더를[!DNL Worktop]**

>[!NOTE]
>
>하위 폴더의 내용이 계층, 드롭다운 하위 디렉토리 대신 하위 탭으로 표시되도록 하려면 각 디렉토리 수준에는 [!DNL Tab Name.useTabs] 파일이 있어야 합니다.

1. [!DNL Profile Manager]에서 **[!UICONTROL Workspaces]**&#x200B;을 클릭하여 콘텐트를 봅니다.
1. *작업 프로필 이름* 열에서 [!DNL folder.useTabs] 파일 중 하나에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]**&#x200B;을 클릭합니다.
1. 작업 영역\*탭 이름* 폴더의 [!DNL User] 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]**&#x200B;을 클릭합니다. 이제 해당 탭 내의 하위 폴더가 하위 탭으로 표시됩니다.
1. (선택 사항) 이 변경 사항을 작업 프로필의 모든 사용자가 사용할 수 있도록 하려면 [!DNL User] 열에서 [!DNL new folder.useTabs] 파일의 흰색 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > **[!UICONTROL working profile name]**>을 클릭합니다.
