---
description: 감사 로그 파일은 Insight Server의 모든 연결 및 연결을 추적하며, Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 있는 <YYYYYYYYMMDD>-access.txt 파일에 각각 기록됩니다.
solution: Insight
title: 감사 로그 모니터링
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 감사 로그 모니터링{#monitoring-audit-logs}

감사 로그 파일은 Insight Server의 모든 접속 및 연결을 추적하며, 각 연결은 Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 `<YYYYMMDD>-access.txt` 있는 파일에 기록됩니다.

**권장 빈도:** 문제 해결에 필요한 일별 또는 일별

연결 문제를 해결할 때 감사 로그가 매우 유용할 수 [!DNL Insight Server]있습니다. 자동화된 관리 툴을 사용하거나 [!DNL access.txt] 파일을 직접 보면서 이러한 로그를 모니터링할 수 있습니다.

**를 통해 access.txt 파일을 보려면[!DNL Server Files Manager]**

1. > [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 활성 상태의 아이콘을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Audit]** 봅니다.
1. 원하는 파일 옆의 *서버 이름* 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 열의 파일 이름 옆에 확인 표시가 [!DNL Temp] 나타납니다.
1. 열에서 새 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 감사 로그가 새 Microsoft Windows 메모장 창에 나타납니다.

   ![단계 정보](assets/cfg_accesscontrol_accessFile.png)

