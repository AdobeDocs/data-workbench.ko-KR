---
description: 사용자의 Insight.cfg 파일에 있는 잠금 해제 매개 변수는 사용자가 편집을 위해 잠긴 작업 공간을 일시적으로 잠금 해제할 권한이 있는지 여부를 지정합니다.
title: 잠금 해제 매개 변수 설정
uuid: db094e32-7d82-4f93-a492-a6bed33ae722
exl-id: 5eda919f-4cfe-4692-9dbf-f7cf64fde1de
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---

# 잠금 해제 매개 변수 설정{#set-the-unlock-parameter}

{{eol}}

사용자의 Insight.cfg 파일에 있는 잠금 해제 매개 변수는 사용자가 편집을 위해 잠긴 작업 공간을 일시적으로 잠금 해제할 권한이 있는지 여부를 지정합니다.

잠금 해제 매개 변수가 사용자의 [!DNL Insight.cfg] 파일에서 Data Workbench을 사용하여 매개 변수를 편집할 수 있습니다. 사용자의 [!DNL Insight.cfg] 파일에서 메모장과 같은 텍스트 편집기를 사용하여 파일에 추가해야 합니다.

**기존 [!DNL Unlock] insight.cfg 파일의 매개 변수**

1. 작업 공간에서 마우스 오른쪽 단추 클릭 **[!UICONTROL Admin]** > **[!UICONTROL Client Configuration]**. 다음 [!DNL Insight.cfg] 파일이 열립니다.
1. 잠금 해제 매개 변수의 경우 true 또는 false를 입력합니다. True를 사용하면 사용자가 잠긴 작업 공간의 잠금을 일시적으로 해제할 수 있지만 False는 잠기지 않습니다.
1. 구성 변경 사항을 저장하려면 마우스 오른쪽 단추를 클릭합니다 **[!UICONTROL Insight.cfg (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save as Insight.cfg]**.

**Insight.cfg 파일에 잠금 해제 매개 변수를 추가하려면**

1. Data Workbench 설치 디렉토리로 이동하고 [!DNL Insight.cfg] 메모장과 같은 텍스트 편집기를 사용하여 파일을 작성합니다.
1. 다음 예와 같이 파일의 끝에 Unlock 매개 변수를 추가합니다.

[!DNL Unlock = bool: false]

1. 값을 true 또는 false로 설정합니다. True를 사용하면 사용자가 잠긴 작업 공간의 잠금을 일시적으로 해제할 수 있지만 False는 잠기지 않습니다.
1. 파일을 저장하고 닫습니다.
