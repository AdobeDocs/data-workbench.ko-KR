---
description: Worktop을 사용하면 각 특정 작업 영역이 저장된 위치, Data Workbench 서버, 로컬 시스템 또는 둘 다에 있는지 손쉽게 파악할 수 있습니다.
title: 파일 버전 관리
uuid: 5e7430f3-1425-41d2-828b-bc8f5786bf3b
exl-id: 82a70d51-a95c-4ddd-8d3c-cd0364940693
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 2%

---

# 파일 버전 관리{#file-versioning}

Worktop을 사용하면 각 특정 작업 영역이 저장된 위치, Data Workbench 서버, 로컬 시스템 또는 둘 다에 있는지 손쉽게 파악할 수 있습니다.

## 파일 버전 식별 {#section-d555c96b016344f19b356c12213dd2a9}

**서버**

서버 작업 공간은 연결된 Data Workbench 서버에 저장되며 이 프로필 및 탭에 액세스할 수 있는 모든 사용자가 사용할 수 있습니다. 서버 작업 영역이 단일 축소판으로 표시됩니다.

![](assets/wsp_thumb_server.png)

서버 작업 공간은 기본적으로 연결된 Data Workbench 서버의 작업 공간 폴더 내의 적절한 하위 폴더에 저장됩니다.

**로컬**

로컬 작업 공간은 서버 작업 공간의 로컬 버전입니다. 로컬 작업공간은 겹치는 두 개의 축소판으로 표시됩니다. 맨 위에 있는 축소판은 처음에 서버 작업 영역에서 최근 변경 사항이 로컬로 수행되었음을 나타내는 광선으로 둘러싸여 있습니다. 이 광선은 시간이 지남에 따라 소멸된다.

![](assets/wsp_thumb_local.png)

로컬 작업 공간은 기본적으로 Data Workbench(또는 Insight) 설치 디렉토리 내의 [!DNL User\working profile name\Workspaces\tab] 이름 폴더에 저장됩니다.

>[!NOTE]
>
>서버 작업 영역의 로컬 버전이 있는 경우 업데이트된 버전의 서버 작업 영역을 다운로드하려면 먼저 서버 버전으로 되돌려야 합니다. 로컬 변경 없이 서버 버전으로 되돌리려면 로컬 작업 영역의 축소판을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Revert to server version]** 를 클릭합니다.

**사용자**

사용자 작업 공간은 생성된 작업 영역이며 로컬 시스템에만 있습니다. 사용자 작업 영역은 연결된 Data Workbench 서버에 소스 작업 영역이 없음을 나타내는 점선 윤곽선이 있는 단일 축소판으로 표시됩니다.

![](assets/wsp_thumb_user.png)

사용자 작업 공간은 기본적으로 Insight 설치 디렉토리 내의 User\*working profile name*\Workspaces\*tab name* 폴더에 저장됩니다.
