---
description: 감사 로그 파일은 Insight Server 설치 디렉토리의 Audit 폴더에 기본적으로 각각 있는 <YYYYYYMMDD>-access.txt 파일에 기록되어 있는 Insight Server와의 모든 연결 및 연결 해제를 추적합니다.
title: 감사 로그 모니터링
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
exl-id: 220330da-e5dc-4ac0-9b70-42b08ccb3577
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 4%

---

# 감사 로그 모니터링{#monitoring-audit-logs}

감사 로그 파일은 Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 있는 `<YYYYMMDD>-access.txt` 파일에 로그인한 Insight Server의 모든 시도한 연결을 추적하고 연결을 해제합니다.

**권장 빈도:** 일별 또는 문제 해결에 필요한 경우

감사 로그는 [!DNL Insight Server]에 연결하는 문제를 해결할 때 매우 유용합니다. 자동 관리 도구를 사용하거나 [!DNL access.txt] 파일을 직접 보면서 이러한 로그를 모니터링할 수 있습니다.

**를 통해 access.txt 파일을 보려면[!DNL Server Files Manager]**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 활성 [!DNL Insight Server]의 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]**&#x200B;을 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Audit]**&#x200B;을 클릭하여 콘텐트를 봅니다.
1. 원하는 파일 옆에 있는 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;를 클릭합니다. [!DNL Temp] 열의 파일 이름 옆에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 새 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. 감사 로그는 새 Microsoft Windows 메모장 창에 나타납니다.

   ![단계 정보](assets/cfg_accesscontrol_accessFile.png)
