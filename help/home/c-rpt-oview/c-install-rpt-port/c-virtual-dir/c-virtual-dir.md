---
description: 보고서 포털을 구성하려면 해당 응용 프로그램 파일을 가상 디렉터리에 매핑해야 합니다.
title: 보고서 포털 페이지를 가상 디렉터리에 매핑
uuid: 75ca85d5-d526-48f9-b2c4-ca77c903c6af
exl-id: 13e457d4-7039-491a-a65d-f23ad7e9fe77
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 18%

---

# 보고서 포털 페이지를 가상 디렉터리에 매핑{#map-the-report-portal-pages-to-virtual-directories}

보고서 포털을 구성하려면 해당 응용 프로그램 파일을 가상 디렉터리에 매핑해야 합니다.

가상 디렉터리는 브라우저 클라이언트가 IIS 응용 프로그램 서버에서 물리적 리소스를 찾는 데 사용하는 주소를 정의합니다. [!DNL Report Portal]에 액세스하려면 클라이언트는 브라우저에서 포털에 할당한 가상 디렉토리를 가리킵니다.

[!DNL Report Portal]에 할당하는 가상 디렉터리의 이름은 이전 섹션의 3단계에서 VSVirtualPortalName 폴더에 사용한 이름과 일치해야 합니다. 예를 들어 &quot;Portal&quot;을 [!DNL Report Portal]의 이름으로 사용하려면 포털의 파일을 &quot;포털&quot;이라는 가상 디렉토리에 매핑해야 합니다. 다음 예제는 클라이언트가 myWebServer라는 서버의 가상 디렉터리 [!DNL VisualReportPortal]에 할당된 [!DNL Report Portal]에 액세스하는 데 사용하는 URI를 보여줍니다.

[!DNL http://myWebServer/VisualReportPortal]

다음 절차에서는 IIS 5.0, 6.0 및 7.0 이상의 가상 디렉터리에 [!DNL Report Portal]을(를) 매핑하는 방법을 설명합니다.

사용 중인 IIS 버전에 대한 절차 세트를 따르십시오.

* [보고서 포털을 가상 디렉터리에 매핑(IIS 7.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-7.md#concept-9fc9595bb83147238965be4832df0a08)
* [보고서 포털을 가상 디렉터리에 매핑(IIS 5.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-5.md#concept-402cb33c50d640e480098517140ffc74)
* \ [세션 구성 파일 편집](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)
