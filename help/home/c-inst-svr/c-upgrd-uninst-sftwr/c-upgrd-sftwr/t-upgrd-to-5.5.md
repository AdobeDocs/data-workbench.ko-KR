---
description: 5.4 설치에서 Data Workbench 6.1용 서버 구성 요소를 업그레이드하는 중입니다.
title: DWB 서버 업그레이드 5.4에서 5.5로
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
exl-id: dd8c2a89-6a40-4ebf-a964-eb4851ab94a5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# DWB 서버 업그레이드: 5.4에서 5.5로{#dwb-server-upgrade-to}

{{eol}}

5.4 설치에서 Data Workbench 6.1용 서버 구성 요소를 업그레이드하는 중입니다.

따라서 [!DNL Insight] 5.4에서 [!DNL Insight] 5.5는 비교적 간단합니다.

또한 [!DNL Insight] 5.3에서 [!DNL Insight] 5.5 를 사용하려면 아래 단계를 따르십시오. 에 나열된 모든 업그레이드 작업을 수행해야 합니다. [Insight 5.4에서 5.5로 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) 섹션 및 [Insight 5.4에서 5.5로 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) 섹션을 참조하십시오.

1. 를 중지합니다. [!DNL Insight Server] 클러스터의 모든 서버에서 서비스를 제외하고 [!DNL Insight Master Server].

   1. 새 복사본 [!DNL ReportServer.exe] 및 [!DNL Insight.exe] Software\Insight 폴더에 파일을 저장합니다.

   1. 다음 이후 [!DNL Insight] 클라이언트가 업데이트되어 복사 [!DNL InsightServer.exe] 및 [!DNL InsightServer64.exe] 파일을 \Bin 폴더에 넣습니다.

   1. 대기 [!DNL Insight Master Server] 시작하려면 다음을 통해 실행 중인 버전을 확인합니다. [!DNL Connections] 시각화.

1. 클러스터의 [!DNL Master Server] 에서 [!DNL Insight] 클라이언트:

   1. 기존 파일의 로컬 복사본 만들기 [!DNL Base] 프로파일을 생성하고 이름을 변경합니다(예: BaseBackup).
   1. 새 복사본 [!DNL Base] 프로파일을 프로파일 폴더에 추가합니다.
   1. 변형 폴더에 대해 이 두 단계를 반복합니다.

1. 서버 패키지의 Scripts 폴더를 [!DNL Master Server] 를 Server 설치 디렉토리에 추가합니다.
1. 를 복사합니다. [!DNL Terrain Images.cfg.off] 파일을 [!DNL Master Server].
   **클라이언트 소프트웨어를 [!DNL Insight] 5.4~5.5**

에서 [!DNL Insight.cfg] 파일에서 소프트웨어 업데이트 설정이 TRUE로 설정되어 있는지 확인하십시오.
