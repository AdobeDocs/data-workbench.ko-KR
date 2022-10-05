---
description: Insight가 지정된 설정을 사용하여 Insight Server에 연결할 수 없는 경우 서버 관리자에 빨간색 노드가 나타납니다.
title: 연결 문제 해결
uuid: 17190cee-da5c-449f-aca5-8e9e35e0a5fd
exl-id: 7938d4d6-e1ab-46d9-9ccb-cf79677c5688
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---

# 연결 문제 해결{#connection-troubleshooting}

{{eol}}

Insight가 지정된 설정을 사용하여 Insight Server에 연결할 수 없는 경우 서버 관리자에 빨간색 노드가 나타납니다.

예를 들어 연결을 잘못 구성하거나 을 볼 권한이 없는 경우 이러한 문제가 발생할 수 있습니다 [!DNL Insight Server’s] 상태.

**Insight가 연결을 설정할 수 없는 이유를 확인하려면**

1. 빨간색 서버 노드를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Detailed Status]**.
1. 에서 [!DNL Detailed Status] 인터페이스, **[!UICONTROL Network Connections]** 번호가 매겨진 항목을 확장합니다. 다음 [!DNL Status] 매개 변수는 Insight가 연결을 설정할 수 없는 이유에 대한 정보를 제공합니다.

   * 500의 상태 코드는 구성 오류를 나타냅니다.
   * 상태 코드 403은 일반적으로 서버의 상태를 볼 수 있는 권한이 없음을 나타냅니다.

에서 추가 상태 정보를 볼 수 있습니다. [!DNL insight.log] 파일. 이 로그 파일은 [!DNL Trace] 폴더가 비어 있습니다. 파일을 보려면 메모장과 같은 텍스트 편집기에서 파일을 엽니다.

의 정보를 이해하는 데 도움이 필요한 경우 [!DNL insight.log] 파일, 먼저 시스템 관리자에게 문의하십시오. 추가 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오.
