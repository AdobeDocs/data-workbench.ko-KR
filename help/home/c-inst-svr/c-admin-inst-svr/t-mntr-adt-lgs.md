---
description: 감사 로그 파일은 Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 있는 <YYYYYYMMDD>-access.txt 파일에 기록되는 Insight Server와의 모든 연결 및 연결 해제를 추적합니다.
solution: Analytics
title: 감사 로그 모니터링
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 4%

---


# 감사 로그 모니터링{#monitoring-audit-logs}

감사 로그 파일은 Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 있는 파일에 로그인한 각 `<YYYYMMDD>-access.txt` 파일의 연결을 모두 추적하고 Insight Server의 연결을 해제합니다.

**권장 빈도:** 문제 해결에 필요한 일별 또는 일별

연결 문제를 해결할 때 감사 로그가 매우 유용할 수 있습니다 [!DNL Insight Server]. 자동화된 관리 툴을 사용하거나 [!DNL access.txt] 파일을 직접 보면서 이러한 로그를 모니터링할 수 있습니다.

**를 통해 access.txt 파일을 보려면[!DNL Server Files Manager]**

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 활성 상태의 아이콘을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 을 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Audit]** 를 봅니다.
1. 원하는 파일 옆의 *서버 이름* 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Make Local]**. 열의 파일 이름 옆에 확인 표시가 [!DNL Temp] 나타납니다.
1. 열에서 새 체크 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 클릭합니다 **[!UICONTROL in Notepad]**. 감사 로그는 새 Microsoft Windows 메모장 창에 나타납니다.

   ![단계 정보](assets/cfg_accesscontrol_accessFile.png)

