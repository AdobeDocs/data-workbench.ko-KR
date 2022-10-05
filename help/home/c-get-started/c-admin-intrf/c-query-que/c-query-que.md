---
description: 일반적으로 Data Workbench 서버는 들어오는 사용자 쿼리를 수신함에 따라 응답하고, 사용자가 더 이상 요청하지 않을 때까지 결과 및 실시간 업데이트를 계속 제공합니다.
title: 쿼리 큐
uuid: 4d64bc89-b664-4532-9f17-be11812d36d4
exl-id: 5d9b20bf-9396-4016-beed-cee8f533f3ea
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 쿼리 큐{#query-queue}

{{eol}}

일반적으로 Data Workbench 서버는 들어오는 사용자 쿼리를 수신함에 따라 응답하고, 사용자가 더 이상 요청하지 않을 때까지 결과 및 실시간 업데이트를 계속 제공합니다.

종종, 특히 Data Workbench 사용자가 많은 시스템에서 활성 쿼리 수는 서버에서 사용할 수 있는 것보다 더 많은 시스템 리소스를 필요로 합니다. [!DNL Query Queue] 답변을 제공하는 데 필요한 리소스를 사용할 수 있을 때까지 서버가 일부 쿼리를 일시적으로 보류할 수 있습니다. 다음 [!DNL Query Queue] 또한 다양한 매개 변수를 기반으로 쿼리를 우선 순위를 지정하는 기능을 제공하여 리소스 경합 시 우선 순위가 높은 쿼리가 먼저 응답되도록 합니다.

단일 클라이언트 또는 보고서 서버의 쿼리는 묶음에 배치되고 단위로 예약됩니다. 쿼리로 사용되는 특정 시스템 리소스의 양을 제한하도록 리소스 모니터를 구성할 수 있습니다. 모니터링되는 리소스가 다른 쿼리 번들의 예약을 허용하는 경우 우선순위가 가장 높은 번들이 예약됩니다. 리소스 제한 사항으로 인해 쿼리가 아직 예약되지 않은 사용자는 오류를 받지 않지만 쿼리가 큐에 올라간다는 알림을 받고 사용자가 로컬 샘플에서 계속 작업할 수 있습니다.

기본 구성에는 [!DNL Query Queue]하지만 비활성화되어 있습니다. 관리자는 [!DNL Query Queue]를 구성하는 경우 리소스 모니터를 구성하여 쿼리에 사용되는 다양한 리소스의 양을 확인하고 여러 사용자에 대해 복잡한 우선 순위 지정 정책을 구성합니다.

**에 대한 Server.cfg 파일을 구성하려면[!DNL Query Queuing]**

1. 열기 [!DNL Server.cfg] 를 클릭합니다. **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]** > **[!UICONTROL Dataset]**.
1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Server.cfg]** 로컬에서 편집할 수 있습니다.
1. 확장 [!DNL Query Queue].

   ![](assets/queryqueue1.png)

1. 다음 매개 변수를 구성합니다.

   * **사용자 그룹:** 정책, 사용자 및 큐 우선 순위를 구성할 수 있습니다. 자세한 내용은 [쿼리 큐 사용자 그룹](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-user-grps.md#concept-5555f51402ed49419c067d61738474c1) 참조하십시오.

   * **활성:** (벡터) [!DNL Query Queue]. 유효한 값은 true 또는 false입니다. 기본 설정은 false입니다.

   * **기본 사용자 그룹:** (문자열) 사용자가 사용자 그룹에 나열되지 않은 경우 사용자가 추가되는 사용자 그룹의 이름을 입력합니다.
   * **리소스 모니터:** (벡터) 마우스 오른쪽 단추를 클릭하여 리소스 모니터를 추가합니다. 다음을 지정할 수 있습니다 [!DNL Query Queue] 메모리 또는 쿼리 수를 모니터링합니다. 마우스 오른쪽 단추 클릭 **[!UICONTROL Resource Monitor]** 메모리 예산 모니터 또는 질의 수 모니터를 선택하려면 다음을 수행합니다. 자세한 내용은 [쿼리 큐 리소스 모니터](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-res-mon.md#concept-0840967b228c4d5ba3b59b4b2759f325) 추가 정보.

   * **터치 할 수 없는 우선 순위:** (Int) 우선 순위가 이 값보다 크거나 같은 번들이 우선순위가 높은 번치를 예약하기 위해 선점되지 않도록 지정합니다. 와 함께 사용됩니다. [!DNL Memory Budget Monitor] 에 설명되어 있습니다. [사용자 그룹 매개변수 테이블](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-user-grps.md#concept-5555f51402ed49419c067d61738474c1).
