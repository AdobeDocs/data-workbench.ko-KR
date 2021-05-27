---
description: 사용자의 Insight.cfg 파일에 있는 잠금 해제 매개 변수는 사용자가 편집을 위해 잠긴 작업 공간을 일시적으로 잠금 해제할 권한이 있는지 여부를 지정합니다.
title: 잠금 해제 매개 변수 설정
uuid: db094e32-7d82-4f93-a492-a6bed33ae722
exl-id: 5eda919f-4cfe-4692-9dbf-f7cf64fde1de
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---

# 잠금 해제 매개 변수 설정{#set-the-unlock-parameter}

사용자의 Insight.cfg 파일에 있는 잠금 해제 매개 변수는 사용자가 편집을 위해 잠긴 작업 공간을 일시적으로 잠금 해제할 권한이 있는지 여부를 지정합니다.

잠금 해제 매개 변수가 사용자의 [!DNL Insight.cfg] 파일에 이미 있으면 Data Workbench을 사용하여 매개 변수를 편집할 수 있습니다. 사용자의 [!DNL Insight.cfg] 파일에 아직 없는 경우 메모장과 같은 텍스트 편집기를 사용하여 파일에 추가해야 합니다.

**Insight.cfg 파일에서 기존  [!DNL Unlock] 매개 변수를 설정하려면 다음을 수행하십시오**

1. 작업 공간에서 **[!UICONTROL Admin]** > **[!UICONTROL Client Configuration]**&#x200B;을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight.cfg] 파일이 열립니다.
1. 잠금 해제 매개 변수의 경우 true 또는 false를 입력합니다. True를 사용하면 사용자가 잠긴 작업 공간의 잠금을 일시적으로 해제할 수 있지만 False는 잠기지 않습니다.
1. 구성 변경 사항을 저장하려면 창 상단에서 **[!UICONTROL Insight.cfg (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save as Insight.cfg]** 를 클릭합니다.

**Insight.cfg 파일에 잠금 해제 매개 변수를 추가하려면**

1. Data Workbench 설치 디렉터리로 이동하고 메모장과 같은 텍스트 편집기를 사용하여 [!DNL Insight.cfg] 파일을 엽니다.
1. 다음 예와 같이 파일의 끝에 Unlock 매개 변수를 추가합니다.

[!DNL Unlock = bool: false]

1. 값을 true 또는 false로 설정합니다. True를 사용하면 사용자가 잠긴 작업 공간의 잠금을 일시적으로 해제할 수 있지만 False는 잠기지 않습니다.
1. 파일을 저장하고 닫습니다.
