---
description: 설치 후 Adobe에서 발행한 디지털 인증서는 보고서 서버를 실행할 수 있는 키 역할을 합니다.
solution: Analytics
title: 디지털 인증서 유효성 확인
topic: Data workbench
uuid: 6c8533df-f459-41eb-84ac-344bad9fecdc
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 디지털 인증서 유효성 확인{#re-validating-the-digital-certificate}

설치 후 Adobe에서 발행한 디지털 인증서는 보고서 서버를 실행할 수 있는 키 역할을 합니다.

**권장 빈도:** 필요에 따라

제대로 작동하려면 디지털 인증서가 최신 상태여야 합니다.

최신 상태로 유지하려면 디지털 인증서의 유효성을 정기적으로 다시 검사해야 합니다(일반적으로 30일마다 확인되지만 Adobe와의 계약에 따라 달라질 수 있습니다). 컴퓨터에 인터넷에 액세스할 수 있는 경우 재인증 프로세스는 완전히 투명합니다. [!DNL Report Server] 자동으로 Adobe 라이센스 서버에 연결하여 필요한 경우 인증서를 다시 확인합니다. 컴퓨터에 인터넷에 액세스할 수 없는 경우 Adobe 사용권 서버에서 유효성이 확인된 새 인증서를 다운로드하여 디지털 인증서 다운로드 및 설치에 설명된 단계에 따라 컴퓨터에 설치해야 [합니다](../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/c-install-dig-cert.md#concept-5a61fc67df3643598c7c403962075f76).