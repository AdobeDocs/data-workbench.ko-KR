---
description: 보고서 포털을 구성하려면 해당 응용 프로그램 파일을 가상 디렉터리에 매핑해야 합니다.
title: 보고서 포털 페이지를 가상 디렉터리에 매핑
uuid: 75ca85d5-d526-48f9-b2c4-ca77c903c6af
exl-id: 13e457d4-7039-491a-a65d-f23ad7e9fe77
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 18%

---

# 보고서 포털 페이지를 가상 디렉터리에 매핑{#map-the-report-portal-pages-to-virtual-directories}

{{eol}}

보고서 포털을 구성하려면 해당 응용 프로그램 파일을 가상 디렉터리에 매핑해야 합니다.

가상 디렉터리는 브라우저 클라이언트가 IIS 응용 프로그램 서버에서 물리적 리소스를 찾는 데 사용하는 주소를 정의합니다. 에 액세스하려면 [!DNL Report Portal]인 경우 클라이언트는 해당 브라우저를 포털에 할당하는 가상 디렉터리에 보냅니다.

지정한 가상 디렉터리의 이름입니다 [!DNL Report Portal] 는 이전 섹션의 3단계에서 VSVirtualPortalName 폴더에 사용한 이름과 일치해야 합니다. 예를 들어 의 이름으로 &quot;Portal&quot;을 사용하려는 경우 [!DNL Report Portal]를 채울 때는 포털의 파일을 &quot;Portal&quot;이라는 가상 디렉터리에 매핑해야 합니다. 다음 예제에서는 클라이언트가 [!DNL Report Portal] 가상 디렉터리에 할당됨 [!DNL VisualReportPortal] myWebServer라는 서버에서 다음을 수행합니다.

[!DNL https://myWebServer/VisualReportPortal]

다음 절차에서는 매핑 방법을 설명합니다 [!DNL Report Portal] 를 클릭합니다.

사용 중인 IIS 버전에 대한 절차 집합을 따르십시오.

* [보고서 포털을 가상 디렉터리에 매핑(IIS 7.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-7.md#concept-9fc9595bb83147238965be4832df0a08)
* [보고서 포털을 가상 디렉터리에 매핑(IIS 5.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-5.md#concept-402cb33c50d640e480098517140ffc74)
* \ [세션 구성 파일 편집](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)
