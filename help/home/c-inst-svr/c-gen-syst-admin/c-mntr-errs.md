---
description: 시스템 및 애플리케이션 오류를 가능한 한 빨리 감지하여 주요 문제 또는 중단을 일으키기 전에 이를 해결하려면 정기적으로 이벤트 로그를 모니터링해야 합니다.
solution: Insight
title: 오류에 대한 이벤트 모니터링
uuid: 09bb34db-e24d-4bc5-84d2-7fc37df60681
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 오류에 대한 이벤트 모니터링{#monitoring-events-for-errors}

시스템 및 애플리케이션 오류를 가능한 한 빨리 감지하여 주요 문제 또는 중단을 일으키기 전에 이를 해결하려면 정기적으로 이벤트 로그를 모니터링해야 합니다.

**권장 빈도:** 5-10분마다

Adobe 서버 소프트웨어 제품을 모니터링하기 위해 자동화된 관리 툴을 사용하여 이벤트 로그에서 소스 &quot;Adobe&quot;의 오류를 모니터링한 다음 적절한 직원에게 개입이 필요할 수 있는 문제를 알릴 수 있습니다.

Windows에서는 응용 프로그램 오류 메시지가 Windows의 응용 프로그램 이벤트 로그로 출력되어 Windows 이벤트 뷰어를 사용하여 액세스할 수 있습니다. Unix에서는 LOG_DAEMON 기능을 사용하여 애플리케이션 오류 메시지가 Unix 시스템 로그로 출력됩니다.

**Windows 이벤트 뷰어를 열려면**

* 클릭 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

