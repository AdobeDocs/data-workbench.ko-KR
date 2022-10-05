---
description: Insight Server FSU를 설치하고 관리를 위해 구성하는 지침은 Insight Server DPU를 설치 및 구성하는 방법과 매우 유사합니다.
title: Insight Server FSU의 설치 절차
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
exl-id: 7373af97-0ecf-47a2-bc27-dbfeb7ca3eaa
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 8%

---

# Insight Server FSU의 설치 절차{#installation-procedures-for-an-insight-server-fsu}

{{eol}}

Insight Server FSU를 설치하고 관리를 위해 구성하는 지침은 Insight Server DPU를 설치 및 구성하는 방법과 매우 유사합니다.

대상 *MS System Center Endpoint Protection* Windows 2012 Server에서는 이러한 실행 파일을 **제외된 프로세스:**

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

를 설치하고 구성하려면 [!DNL Insight Server] FSU, 다음 작업을 완료해야 합니다.

1. 설치 [!DNL Insight Server] 프로그램 파일.
1. 설치 [!DNL Insight Server] 디지털 인증서.
1. 에서 포트 설정을 확인합니다. [!DNL Communications.cfg] 파일.
1. 수정 [!DNL Access Control.cfg] 파일에 대한 관리자 액세스 허용 [!DNL the Server] 변환 전: [!DNL the Client].
1. 수정 [!DNL server.address] 파일을 사용하여 서버의 네트워크 위치를 정의합니다.
1. 설명된 대로 Windows 메모리 사용률 매개 변수를 설정합니다.
1. 등록 [!DNL Insight Server] 에 설명되어 있습니다.

   에 대한 데이터 소스, 권한 및 통신을 구성하는 방법에 대한 지침 [!DNL Insight Server] FSU에서 *데이터 집합 구성 안내서*.
