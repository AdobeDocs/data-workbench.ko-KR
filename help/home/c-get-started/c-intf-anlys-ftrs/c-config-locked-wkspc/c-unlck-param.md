---
description: 사용자의 Insight.cfg 파일에 있는 잠금 해제 매개 변수는 사용자가 편집을 위해 잠근 작업 영역의 잠금을 일시적으로 해제할 수 있는 권한이 있는지 여부를 지정합니다.
solution: Analytics
title: 잠금 해제 매개 변수 설정
topic: Data workbench
uuid: db094e32-7d82-4f93-a492-a6bed33ae722
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 잠금 해제 매개 변수 설정{#set-the-unlock-parameter}

사용자의 Insight.cfg 파일에 있는 잠금 해제 매개 변수는 사용자가 편집을 위해 잠근 작업 영역의 잠금을 일시적으로 해제할 수 있는 권한이 있는지 여부를 지정합니다.

잠금 해제 매개 변수가 사용자의 [!DNL Insight.cfg] 파일에 이미 있는 경우 데이터 워크벤치를 사용하여 매개 변수를 편집할 수 있습니다. 사용자의 파일에 아직 없는 경우 메모장과 같은 텍스트 편집기를 사용하여 파일에 추가해야 합니다. [!DNL Insight.cfg]

**Insight.cfg 파일에서 기존[!DNL Unlock]매개 변수를 설정하려면**

1. 작업 영역에서 마우스 오른쪽 단추를 클릭하여 **[!UICONTROL Admin]** > **[!UICONTROL Client Configuration]**&#x200B;을 클릭합니다. 파일이 [!DNL Insight.cfg] 열립니다.
1. 잠금 해제 매개 변수에 true 또는 false를 입력합니다. True를 사용하면 잠긴 작업 영역을 일시적으로 잠금 해제할 수 있지만 False는 잠금 해제된 작업 영역을 사용할 수 없습니다.
1. 구성 변경 사항을 저장하려면 창 **[!UICONTROL Insight.cfg (modified)]** 맨 위에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save as Insight.cfg]**.

**Insight.cfg 파일에 잠금 해제 매개 변수를 추가하려면**

1. 데이터 워크벤치 설치 디렉토리로 이동한 다음 메모장과 같은 텍스트 편집기를 사용하여 [!DNL Insight.cfg] 파일을 엽니다.
1. 다음 예와 같이 파일 끝에 잠금 해제 매개 변수를 추가합니다.

[!DNL Unlock = bool: false]

1. 값을 true 또는 false로 설정합니다. True를 사용하면 잠긴 작업 영역을 일시적으로 잠금 해제할 수 있지만 False는 잠금 해제된 작업 영역을 사용할 수 없습니다.
1. 파일을 저장하고 닫습니다.

