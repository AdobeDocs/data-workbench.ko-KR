---
description: 시스템 및 애플리케이션 오류를 가능한 한 빨리 감지하여 주요 문제 또는 정전을 발생하기 전에 처리하려면 이벤트 로그를 정기적으로 모니터링해야 합니다.
title: 오류에 대한 이벤트 모니터링
uuid: 09bb34db-e24d-4bc5-84d2-7fc37df60681
exl-id: 88f48594-5c73-4ae3-8014-b8543e689426
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 6%

---

# 오류에 대한 이벤트 모니터링{#monitoring-events-for-errors}

{{eol}}

시스템 및 애플리케이션 오류를 가능한 한 빨리 감지하여 주요 문제 또는 정전을 발생하기 전에 처리하려면 이벤트 로그를 정기적으로 모니터링해야 합니다.

**권장 빈도:** 5-10분마다

Adobe 서버 소프트웨어 제품을 모니터링하기 위해 자동화된 관리 도구를 설정하여 이벤트 로그에서 소스 &quot;Adobe&quot;의 오류에 대해 모니터링한 다음 개입이 필요할 수 있는 문제에 대해 적절한 직원에게 알립니다.

Windows에서는 응용 프로그램 오류 메시지가 Windows의 응용 프로그램 이벤트 로그로 출력되며 Windows 이벤트 뷰어를 사용하여 액세스할 수 있습니다. Unix에서는 LOG_DAEMON 기능을 사용하여 응용 프로그램 오류 메시지가 Unix syslog로 출력됩니다.

**Windows 이벤트 뷰어를 열려면**

* 클릭 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.
