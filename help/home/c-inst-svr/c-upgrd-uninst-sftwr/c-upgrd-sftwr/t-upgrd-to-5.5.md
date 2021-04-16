---
description: 5.4 설치에서 Data Workbench 6.1용 서버 구성 요소를 업그레이드합니다.
title: DWB Server 업그레이드 5.4 - 5.5
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
exl-id: dd8c2a89-6a40-4ebf-a964-eb4851ab94a5
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# DWB 서버 업그레이드: 5.4에서 5.5로{#dwb-server-upgrade-to}

5.4 설치에서 Data Workbench 6.1용 서버 구성 요소를 업그레이드합니다.

따라서 [!DNL Insight] 5.4에서 [!DNL Insight] 5.5로 업그레이드하는 것은 비교적 간단합니다.

아래 단계를 사용하여 [!DNL Insight] 5.3에서 [!DNL Insight] 5.5로 직접 업그레이드할 수도 있습니다. [Insight 5.4에서 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) 섹션으로 업그레이드 및 [Insight 5.4에서 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) 섹션으로 업그레이드 섹션에 나열된 모든 업그레이드 작업을 수행해야 합니다.

1. [!DNL Insight Master Server]을(를) 제외한 클러스터의 모든 서버에서 [!DNL Insight Server] 서비스를 중지합니다.

   1. 새 [!DNL ReportServer.exe] 및 [!DNL Insight.exe] 파일을 Software\Insight 폴더에 복사합니다.

   1. [!DNL Insight] 클라이언트가 업데이트된 후 [!DNL InsightServer.exe] 및 [!DNL InsightServer64.exe] 파일을 \Bin 폴더에 복사합니다.

   1. [!DNL Insight Master Server]이(가) 시작될 때까지 기다렸다가 [!DNL Connections] 시각화를 통해 실행 중인 버전을 확인합니다.

1. [!DNL Insight] 클라이언트의 클러스터 [!DNL Master Server]에서:

   1. 기존 [!DNL Base] 프로필의 로컬 복사본을 만들고 이름을 변경합니다(예: BaseBackup).
   1. 새 [!DNL Base] 프로필을 Profiles 폴더에 복사합니다.
   1. 변형 폴더에 대해 이 2단계를 반복합니다.

1. 서버 패키지의 Scripts 폴더를 [!DNL Master Server] 서버 설치 디렉토리로 복사합니다.
1. [!DNL Terrain Images.cfg.off] 파일을 [!DNL Master Server]의 Components 폴더에 복사합니다.
   **클라이언트 소프트웨어를  [!DNL Insight] 5.4에서 5.5로 업그레이드하려면**

[!DNL Insight.cfg] 파일에서 소프트웨어 업데이트 설정이 TRUE로 설정되어 있는지 확인합니다.
