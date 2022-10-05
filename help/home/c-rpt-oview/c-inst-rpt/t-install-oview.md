---
description: 보고서 서버 소프트웨어를 설치 및 구성하는 절차.
title: 설치 개요
uuid: ffc72aa1-98d8-41dc-b4e5-6f70ff43430e
exl-id: 4ddc0761-a999-49ed-b0e4-12cf34e2688c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# 설치 개요{#installation-overview}

{{eol}}

보고서 서버 소프트웨어를 설치 및 구성하는 절차.

다음 작업을 순서대로 완료해야 합니다.

1. 보고서 서버 프로그램 파일을 설치합니다.
1. 보고서 서버 디지털 인증서를 다운로드하여 설치합니다. 자세한 내용은 [디지털 인증서 다운로드 및 설치](../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/c-install-dig-cert.md#concept-5a61fc67df3643598c7c403962075f76).
1. 보고서 서버와 Data Workbench 서버(InsightServer64.exe) 간의 연결을 구성합니다. 자세한 내용은 [Insight Server에 연결 구성](../../../home/c-rpt-oview/c-inst-rpt/t-config-conn-ins-svr.md#task-a3ca949c43244782b658fb4437fd724c).
1. 언어 파일(.zbin 파일)로 보고서 서버를 업데이트합니다.

   자세한 내용은 [언어 파일(.zbin 파일)로 보고서 서버 업데이트](../../../home/c-rpt-oview/c-inst-rpt/c-zbin-file-update.md#concept-5637a8f52b7643759e423c2068b4126b). 1. Data Workbench 서버 시스템에서 액세스 제어 파일을 업데이트하여 보고서 서버가 Data Workbench 서버에 액세스할 수 있도록 합니다. 자세한 내용은 [Insight Server에 대한 액세스 활성화](../../../home/c-rpt-oview/c-inst-rpt/t-en-acc-ins-svr.md#task-e7b95cf9cb194842ad72fa534c56c3cc).
1. 마스터 Data Workbench 서버 시스템에서 통신 파일을 편집하여 [!DNL Master Server Detailed Status] 인터페이스. 자세한 내용은 [보고서에 대한 서버 상태를 표시하도록 Insight Server 구성](../../../home/c-rpt-oview/c-inst-rpt/t-display-svr-st-rpt.md#task-a14d096f85924d9b93eef950591f93a8).
1. 보고서를 Windows 서비스로 등록합니다. 자세한 내용은 [보고서를 Windows 서비스로 등록](../../../home/c-rpt-oview/c-inst-rpt/t-reg-rpt-win-svc.md#task-a8762d7818ed4cfd87e616db6a68b3a6).
