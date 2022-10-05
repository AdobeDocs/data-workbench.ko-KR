---
description: 이러한 단계는 작업 공간 창 메뉴의 하위 메뉴 및 메뉴 항목을 만드는 경우에만 적용됩니다.
title: 작업 영역 메뉴 및 메뉴 항목 만들기
uuid: 9565fe7a-fa4c-42b6-9aa5-b652a2d62796
exl-id: 26f2b85c-ab23-41a4-bf4b-9e507952fede
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 3%

---

# 작업 영역 메뉴 및 메뉴 항목 만들기{#create-a-workspace-menu-and-menu-item}

{{eol}}

이러한 단계는 작업 공간 창 메뉴의 하위 메뉴 및 메뉴 항목을 만드는 경우에만 적용됩니다.

새 폴더 및 새로 파생된 지표 및 차원을 만들어 지표 및 차원 메뉴를 사용자 지정할 수 있습니다. 자세한 내용은 [파생 지표 만들기 및 편집](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40) 및 [파생 Dimension 만들기 및 편집](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-dvrd-dim.md#concept-ece3c3ea8cdf4fc796680173993bff93).

**새 작업공간 창 메뉴를 생성하려면**

1. 에서 [!DNL Profile Manager]를 클릭하고 **[!UICONTROL Menu]** 디렉토리 을 클릭하여 컨텐츠를 확인합니다.
1. 에서 [!DNL User] 메뉴 디렉토리의 열에서 **[!UICONTROL Create]** > **[!UICONTROL Folder]**. New Folder 라는 폴더가 [!DNL File] 열 [!DNL Menu].

   >[!NOTE]
   >
   >Menu 디렉토리 내에서 하위 디렉토리에 대한 새 폴더를 만들 수도 있습니다.

1. 에서 마우스 오른쪽 단추를 클릭하여 새 폴더의 이름을 변경합니다. [!DNL User] 열을 눌러 새 이름을 Dir 매개 변수에 입력합니다.
1. 원하는 파일을 새 폴더에 추가합니다.
1. (선택 사항)에서 [!DNL User] 새 폴더의 열에서 **[!UICONTROL Create]** > **[!UICONTROL order.txt]**.

   An [!DNL order.txt] 파일이 [!DNL File] 새 폴더에 대한 열과 새 파일에 대한 확인 표시가 [!DNL User] 열.

1. (선택 사항) [!DNL order.txt] 필요에 따라 파일을 사용하십시오. 자세한 내용은 [Order.txt 파일을 사용하여 메뉴 사용자 정의](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL User] 열 및 클릭 **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL working profile name]**>*.

**기존 메뉴에 새 메뉴 항목을 추가하려면**

1. 다음 단계 중 하나를 완료합니다.

   * 메뉴에 추가할 새 항목(시각화, 주석 등)을 만듭니다.

      1. Data Workbench에서 작업 공간을 열고 원하는 항목을 만듭니다.
      1. 항목을 다음 디렉토리에 저장합니다.

         *Data Workbench 설치 디렉토리*\User\*working profile name*\작업

      1. 에서 [!DNL Profile Manager]를 클릭하고 **[!UICONTROL Work]** 디렉토리 을 클릭하여 컨텐츠를 확인합니다.
      1. 에서 [!DNL User] 열에서 원하는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]**.
      1. 에서 [!DNL User] 원하는 폴더에 대한 열에서 **[!UICONTROL Paste]**.

         파일의 사본이 [!DNL File] 새 폴더에 대한 열과 새 파일에 대한 확인 표시가 [!DNL User] 열.
   * 한 메뉴(폴더)에서 다른 메뉴(폴더)로 기존 항목을 복사하여 붙여 넣습니다.

      1. 에서 [!DNL Profile Manager]를 클릭하고 **[!UICONTROL Menu]** 디렉토리 을 클릭하여 컨텐츠를 확인합니다.
      1. 에서 *작업 프로필 이름* 열에서 원하는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**.
      1. 에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Copy]**.
      1. 에서 [!DNL User] 원하는 폴더에 대한 열에서 **[!UICONTROL Paste]**. 파일의 사본이 [!DNL File] 새 폴더에 대한 열과 새 파일에 대한 확인 표시가 [!DNL User] 열.


1. (선택 사항) [!DNL order.txt] 필요에 따라 파일을 사용하십시오. 자세한 내용은 [Order.txt 파일을 사용하여 메뉴 사용자 정의](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
1. (선택 사항) 여러 메뉴에 메뉴 항목이 나타나지 않게 하려면 파일의 체크 표시를 마우스 오른쪽 단추로 클릭하여 해당 파일을 원래 폴더에서 삭제해야 합니다 *작업 프로필 이름* 열 및 클릭 **[!UICONTROL Remove]** > **[!UICONTROL Yes]**.

   에서 파일의 체크 표시에 대해 이 단계를 반복합니다. [!DNL User] 열.
