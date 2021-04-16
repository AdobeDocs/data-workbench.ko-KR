---
description: 이러한 단계는 [작업 영역 창] 메뉴의 하위 메뉴와 메뉴 항목을 만드는 경우에만 적용됩니다.
title: 작업 영역 메뉴 및 메뉴 항목 만들기
uuid: 9565fe7a-fa4c-42b6-9aa5-b652a2d62796
exl-id: 26f2b85c-ab23-41a4-bf4b-9e507952fede
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 3%

---

# 작업 영역 메뉴 및 메뉴 항목 만들기{#create-a-workspace-menu-and-menu-item}

이러한 단계는 [작업 영역 창] 메뉴의 하위 메뉴와 메뉴 항목을 만드는 경우에만 적용됩니다.

새 폴더 및 새로운 파생된 지표 및 차원을 만들어 지표 및 차원 메뉴를 사용자 지정할 수 있습니다. 자세한 내용은 [파생된 지표 만들기 및 편집](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40) 및 [파생된 Dimension 만들기 및 편집](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-dvrd-dim.md#concept-ece3c3ea8cdf4fc796680173993bff93)을 참조하십시오.

**새 작업 영역 창 메뉴를 만들려면**

1. [!DNL Profile Manager]에서 **[!UICONTROL Menu]** 디렉터리를 클릭하여 콘텐트를 봅니다.
1. 메뉴 디렉토리의 [!DNL User] 열에서 **[!UICONTROL Create]** > **[!UICONTROL Folder]**&#x200B;를 클릭합니다. [!DNL Menu]의 [!DNL File] 열에 새 폴더라는 폴더가 나타납니다.

   >[!NOTE]
   >
   >Menu 디렉토리 내의 모든 하위 디렉토리에 대한 새 폴더를 만들 수도 있습니다.

1. 폴더의 [!DNL User] 열을 마우스 오른쪽 버튼으로 클릭하고 Dir 매개 변수에 새 이름을 입력하여 새 폴더의 이름을 변경합니다.
1. 원하는 파일을 새 폴더에 추가합니다.
1. (선택 사항) 새 폴더의 [!DNL User] 열에서 **[!UICONTROL Create]** > **[!UICONTROL order.txt]**&#x200B;를 클릭합니다.

   [!DNL order.txt] 파일이 새 폴더의 [!DNL File] 열에 나타나고 새 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

1. (선택 사항) 필요에 따라 [!DNL order.txt] 파일을 편집합니다. [Order.txt 파일을 사용하여 메뉴 사용자 지정](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999)을 참조하십시오.
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL User] 열의 폴더에 대한 흰색 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.

**기존 메뉴에 새 메뉴 항목을 추가하려면**

1. 다음 단계 중 하나를 완료합니다.

   * 메뉴에 추가할 새 항목(시각화, 주석 등)을 만듭니다.

      1. Data Workbench에서 작업 영역을 열고 원하는 항목을 만듭니다.
      1. 항목을 다음 디렉토리에 저장합니다.

         *데이터 워크벤치 설치 디렉토리*\User\*작업 프로필 이름*\작업

      1. [!DNL Profile Manager]에서 **[!UICONTROL Work]** 디렉터리를 클릭하여 콘텐트를 봅니다.
      1. [!DNL User] 열에서 원하는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]**&#x200B;을 클릭합니다.
      1. 원하는 폴더의 [!DNL User] 열에서 **[!UICONTROL Paste]**&#x200B;을 클릭합니다.

         파일의 복사본이 새 폴더의 [!DNL File] 열에 나타나고 새 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
   * 한 메뉴(폴더)에서 다른 메뉴로 기존 항목을 복사하여 붙여 넣습니다.

      1. [!DNL Profile Manager]에서 **[!UICONTROL Menu]** 디렉터리를 클릭하여 콘텐트를 봅니다.
      1. *작업 프로필 이름* 열에서 원하는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;를 클릭합니다.
      1. [!DNL User] 열에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]** 을 클릭합니다.
      1. 원하는 폴더의 [!DNL User] 열에서 **[!UICONTROL Paste]**&#x200B;을 클릭합니다. 파일의 복사본이 새 폴더의 [!DNL File] 열에 나타나고 새 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.


1. (선택 사항) 필요에 따라 [!DNL order.txt] 파일을 편집합니다. [Order.txt 파일을 사용하여 메뉴 사용자 지정](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999)을 참조하십시오.
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL User] 열의 각 파일에 대한 흰색 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.
1. (선택 사항) 메뉴 항목이 여러 메뉴에 나타나지 않도록 하려면 *작업 프로필 이름* 열에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Remove]** > **[!UICONTROL Yes]**&#x200B;을 클릭하여 해당 파일을 원래 폴더에서 삭제해야 합니다.

   [!DNL User] 열에 있는 파일의 체크 표시에 대해 이 단계를 반복합니다.
