---
description: 기본적으로 잠금 해제된 작업 영역을 닫으면 작업 공간에 수행된 변경 사항이 저장됩니다.
solution: Analytics
title: 작업 영역 저장
topic: Data workbench
uuid: 166f9ef8-c2c4-4dfc-8d7d-453650bee6b8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 작업 영역 저장{#save-a-workspace}

기본적으로 잠금 해제된 작업 영역을 닫으면 작업 공간에 수행된 변경 사항이 저장됩니다.

작업 영역이 서버 작업 영역인 경우 업데이트된 작업 영역을 Data Workbench 서버에 특별히 저장하지 않는 한 변경 사항이 로컬에만 저장됩니다. 잠긴 작업 영역에 대한 자세한 내용은 작업 영역 [잠금을 참조하십시오](../../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e).

## 로컬에 작업 영역 저장 {#section-3f331c880f1a490c96844103c2432d61}

기본 저장 위치는 Data Workbench **설치 디렉토리** 내의 User\profile name\Workspaces\tab name 폴더입니다. 예를 들어 무비 프로필을 사용하여 작업 중이며 [!UICONTROL Custom] 탭에서 작업 영역을 로컬에 저장하는 경우 작업 영역은 데이터 워크벤치 설치 **디렉토리의 User\Movies\Workspaces\Custom** 폴더에 저장됩니다.

**작업 영역에 변경 사항을 저장하려면**

* 작업 영역에서 을 클릭한 **[!UICONTROL File]**&#x200B;다음 을 **[!UICONTROL Save]**&#x200B;클릭합니다.

**기존 작업 영역을 새 작업 영역으로 저장하려면**

1. 원하는 [!DNL Worktop] 탭에서 표시할 작업 영역의 축소판을 클릭합니다.
1. 작업 영역에서 을 클릭한 **[!UICONTROL File]**&#x200B;다음 을 클릭합니다 **[!UICONTROL Save Copy As]**.
1. 대화 [!DNL Save Workspace As] 상자에서 복사한 작업 영역을 저장할 이름과 위치를 지정하고 을 클릭합니다 **[!UICONTROL Save]**.

## 작업 영역을 데이터 워크벤치 서버에 저장 {#section-65a23da852ee4186880e002f7c87ea81}

>[!NOTE]
>
>적절한 권한이 있는 사용자만 작업 영역을 데이터 워크벤치 서버에 저장할 수 있습니다. 자세한 내용은 시스템 관리자에게 문의하십시오.

작업 영역을 연결된 Data Workbench 서버에 저장하는 것은 작업 영역을 다른 사용자가 사용할 수 있게 하기 때문에 작업 공간을 게시하는 라고도 합니다. 기본적으로 작업 영역은 데이터 워크벤치 서버의 *작업 프로필 이름*\Workspaces\*tab name* 폴더에 저장됩니다. 예를 들어 동영상 프로필을 사용하여 작업 영역을 [!DNL Custom] 탭에서 연결된 데이터 워크벤치 서버에 저장하면 작업 영역이 Movies\Workspaces\Custom folder of the Data Workbench server폴더에 저장됩니다.

**작업 영역을 데이터 워크벤치 서버에 저장하려면**

* 원하는 [!DNL Worktop] 탭에서 데이터 워크벤치 서버에 저장할 작업 영역의 축소판을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save to server]**.

![](assets/mnu_workspaceManager_SaveToServerwksp.png)
