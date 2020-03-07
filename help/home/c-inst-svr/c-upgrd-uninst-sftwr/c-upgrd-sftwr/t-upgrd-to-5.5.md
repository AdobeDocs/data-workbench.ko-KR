---
description: Data Workbench 6.1용 서버 구성 요소를 5.4 설치에서 업그레이드합니다.
solution: Insight
title: DWB Server 업그레이드 5.4 - 5.5
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# DWB Server 업그레이드:5.4 - 5.5{#dwb-server-upgrade-to}

Data Workbench 6.1용 서버 구성 요소를 5.4 설치에서 업그레이드합니다.

따라서 5.4에서 [!DNL Insight] 5.5로 [!DNL Insight] 업그레이드하는 것은 비교적 간단합니다.

아래 단계를 사용하여 [!DNL Insight] 5.3에서 5.5로 [!DNL Insight] 직접 업그레이드할 수도 있습니다. Insight 5.4에서 5.5 [로 업그레이드 섹션과 Insight 5.4에서 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) 로 [업그레이드 섹션에 나열된 모든 업그레이드 작업을 수행해야](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) 합니다.

1. 클러스터를 제외한 클러스터의 모든 서버에서 서비스를 [!DNL Insight Server] [!DNL Insight Master Server]중지합니다.

   1. 새 [!DNL ReportServer.exe] 파일과 [!DNL Insight.exe] 파일을 Software\Insight 폴더에 복사합니다.

   1. 클라이언트가 업데이트된 후 [!DNL Insight] 및 [!DNL InsightServer.exe] [!DNL InsightServer64.exe] 파일을 \Bin 폴더에 복사합니다.

   1. 시작할 [!DNL Insight Master Server] [!DNL Connections] 때까지 기다렸다가 시각화를 통해 실행 중인 버전을 확인합니다.

1. 클러스터의 [!DNL Master Server] [!DNL Insight] 클라이언트:

   1. 기존 프로필의 로컬 복사본을 만들고 이름을 변경합니다(예: BaseBackup). [!DNL Base]
   1. 새 [!DNL Base] 프로필을 프로필 폴더에 복사합니다.
   1. 변형 폴더에 대해 이 두 단계를 반복합니다.

1. 서버 패키지의 Scripts 폴더를 서버 설치 디렉토리로 [!DNL Master Server] 복사합니다.
1. 파일을 [!DNL Terrain Images.cfg.off] 의 구성 요소 폴더에 복사합니다 [!DNL Master Server].
   **클라이언트 소프트웨어를[!DNL Insight]5.4에서 5.5로 업그레이드하려면**

파일에서 소프트웨어 업데이트 설정이 TRUE로 설정되어 있는지 확인합니다. [!DNL Insight.cfg]
