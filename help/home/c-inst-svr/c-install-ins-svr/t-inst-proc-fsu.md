---
description: Insight Server FSU를 설치하고 관리용으로 구성하는 지침은 Insight Server DPU를 설치 및 구성하는 방법과 매우 유사합니다.
solution: Insight
title: Insight Server FSU의 설치 절차
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Insight Server FSU의 설치 절차{#installation-procedures-for-an-insight-server-fsu}

Insight Server FSU를 설치하고 관리용으로 구성하는 지침은 Insight Server DPU를 설치 및 구성하는 방법과 매우 유사합니다.

Windows *2012 Server의 MS System* Center Endpoint Protection의 경우 이러한 실행 파일을 **제외된 프로세스에 추가해야 합니다.**

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

FSU를 설치하고 구성하려면 [!DNL Insight Server] 다음 작업을 완료해야 합니다.

1. 프로그램 파일을 [!DNL Insight Server] 설치합니다.
1. 디지털 인증서를 [!DNL Insight Server] 설치합니다.
1. 파일의 포트 설정을 [!DNL Communications.cfg] 확인합니다.
1. 에서 관리 액세스를 허용하도록 [!DNL Access Control.cfg] 파일을 [!DNL the Server] 수정합니다 [!DNL the Client].
1. 서버의 네트워크 위치를 정의하려면 [!DNL server.address] 파일을 수정합니다.
1. 설명된 대로 Windows 메모리 사용률 매개 변수를 설정합니다.
1. 설명에 [!DNL Insight Server] 따라 Windows 서비스로 등록하십시오.

   FSU에 대한 데이터 소스, 권한 및 통신을 구성하는 [!DNL Insight Server] 방법은 데이터 세트 구성 *안내서를 참조하십시오*.

