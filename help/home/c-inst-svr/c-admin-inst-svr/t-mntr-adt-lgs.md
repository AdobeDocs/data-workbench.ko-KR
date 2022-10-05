---
description: 감사 로그 파일은 각각 Insight Server에 로그인하여 Insight Server에서 시도된 모든 연결을 추적합니다 <yyyymmdd>Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 있는 -access.txt 파일입니다.
title: 감사 로그 모니터링
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
exl-id: 220330da-e5dc-4ac0-9b70-42b08ccb3577
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 4%

---

# 감사 로그 모니터링{#monitoring-audit-logs}

{{eol}}

감사 로그 파일은 각각 Insight Server에 로그인하여 Insight Server에서 시도된 모든 연결을 추적합니다 `<YYYYMMDD>-access.txt` Insight Server 설치 디렉토리 내의 감사 폴더에 기본적으로 있는 파일입니다.

**권장 빈도:** 문제 해결에 필요한 일별 또는 일

감사 로그는 연결 문제를 해결할 때 유용합니다 [!DNL Insight Server]. 자동화된 관리 도구를 사용하거나 [!DNL access.txt] 파일을 직접 가져올 수 있습니다.

**를 통해 access.txt 파일을 보려면[!DNL Server Files Manager]**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 활성 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 클릭합니다. **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Audit]** 콘텐츠를 보려면 클릭하십시오.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 원하는 파일 옆에 있는 열을 클릭하고 **[!UICONTROL Make Local]**. 에서 파일 이름 옆에 확인 표시가 나타납니다 [!DNL Temp] 열.
1. 에서 새 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 감사 로그가 새 Microsoft Windows 메모장 창에 나타납니다.

   ![단계 정보](assets/cfg_accesscontrol_accessFile.png)
