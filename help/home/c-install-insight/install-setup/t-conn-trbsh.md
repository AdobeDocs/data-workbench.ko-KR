---
description: Insight가 지정된 설정을 사용하여 Insight 서버에 연결할 수 없는 경우 서버 관리자에 빨간색 노드가 나타납니다.
title: 연결 문제 해결
uuid: 17190cee-da5c-449f-aca5-8e9e35e0a5fd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 연결 문제 해결{#connection-troubleshooting}

Insight가 지정된 설정을 사용하여 Insight 서버에 연결할 수 없는 경우 서버 관리자에 빨간색 노드가 나타납니다.

예를 들어, 연결을 잘못 구성하거나 [!DNL Insight Server’s] 상태를 볼 수 있는 권한이 없는 경우 이러한 문제가 발생할 수 있습니다.

**Insight에서 연결을 설정할 수 없는 이유를 확인하려면**

1. 빨간색 서버 노드를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Detailed Status]**&#x200B;클릭합니다.
1. 인터페이스에서 번호가 매겨진 항목을 클릭하고 [!DNL Detailed Status] **[!UICONTROL Network Connections]** 확장합니다. 이 [!DNL Status] 매개 변수는 Insight가 연결을 설정할 수 없는 이유에 대한 정보를 제공합니다.

   * 500년대 상태 코드는 구성 오류를 나타냅니다.
   * 상태 코드 403은 일반적으로 서버의 상태를 볼 수 있는 권한이 없음을 나타냅니다.

추가 상태 정보는 [!DNL insight.log] 파일에서 볼 수 있습니다. 이 로그 파일은 Insight를 설치한 디렉토리의 [!DNL Trace] 폴더에 있습니다. 파일을 보려면 메모장과 같은 텍스트 편집기에서 파일을 엽니다.

파일의 정보를 이해하는 데 도움이 필요한 경우 먼저 시스템 관리자에게 문의하십시오. [!DNL insight.log] 추가 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오.
