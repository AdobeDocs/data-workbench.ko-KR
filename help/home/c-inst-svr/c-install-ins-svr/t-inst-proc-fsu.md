---
description: Insight Server FSU를 설치하고 관리용으로 구성하기 위한 지침은 Insight Server DPU를 설치 및 구성하는 방법과 매우 유사합니다.
title: Insight Server FSU의 설치 절차
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
exl-id: 7373af97-0ecf-47a2-bc27-dbfeb7ca3eaa
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 8%

---

# Insight Server FSU의 설치 절차{#installation-procedures-for-an-insight-server-fsu}

Insight Server FSU를 설치하고 관리용으로 구성하기 위한 지침은 Insight Server DPU를 설치 및 구성하는 방법과 매우 유사합니다.

Windows 2012 Server의 *MS System Center Endpoint Protection*&#x200B;의 경우 이러한 실행 파일을 **제외된 프로세스:**&#x200B;에 추가해야 합니다.

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

[!DNL Insight Server] FSU를 설치하고 구성하려면 다음 작업을 완료해야 합니다.

1. [!DNL Insight Server] 프로그램 파일을 설치합니다.
1. [!DNL Insight Server] 디지털 인증서를 설치합니다.
1. [!DNL Communications.cfg] 파일의 포트 설정을 확인합니다.
1. [!DNL Access Control.cfg] 파일을 수정하여 [!DNL the Client]의 [!DNL the Server]에 대한 관리 액세스를 허용합니다.
1. [!DNL server.address] 파일을 수정하여 서버의 네트워크 위치를 정의합니다.
1. 설명된 대로 Windows 메모리 사용 매개 변수를 설정합니다.
1. 설명한 대로 [!DNL Insight Server]을(를) Windows 서비스로 등록합니다.

   [!DNL Insight Server] FSU에 대한 데이터 소스, 권한 및 통신 구성에 대한 지침은 *데이터 세트 구성 안내서*&#x200B;를 참조하십시오.
