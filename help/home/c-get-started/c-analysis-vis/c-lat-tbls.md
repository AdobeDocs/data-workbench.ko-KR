---
description: 지연 테이블 시각화 는 지연 차원을 포함하는 테이블이며, 이 차원은 특정 이벤트가 발생한 이후 경과된 시간을 측정하는 파생 차원의 유형입니다.
title: 지연 테이블
uuid: 8081540c-f96c-424e-802d-05d1be5a728d
exl-id: 22f6d52f-e1c2-430a-9e69-3440be0ecdea
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 1%

---

# 지연 테이블{#latency-tables}

{{eol}}

지연 테이블 시각화 는 지연 차원을 포함하는 테이블이며, 이 차원은 특정 이벤트가 발생한 이후 경과된 시간을 측정하는 파생 차원의 유형입니다.

하나 이상의 시각화 내에서 선택하고 이벤트 컨텍스트 설정 메뉴 옵션을 사용하여 해당 선택 사항을 이벤트로 설정하여 이벤트를 정의합니다. 지연 테이블은 시간 상관 관계를 찾는 캠페인 또는 특정 고객 주문과 관련된 활동을 추적하는 데 특히 유용합니다.

in [!DNL Site], 지연 테이블은 이벤트 이전 또는 7일 이후에 발생한 방문자 세션에 대한 정보를 제공하지만 지연 테이블을 구성하여 가산 및 시간 차원에 대한 정보를 제공할 수 있습니다. 자세한 내용은 [지연 테이블 구성](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/c-config-ltcy-tbls.md#concept-7175c3defec64556994f0dfcccb7d15c).

선택한 특정 이벤트의 일부인 세션 등의 상위 차원 요소에는 지연 시간이 0입니다. 다른 모든 요소에는 이벤트와의 거리(해당 시간 차원)를 반영하는 지연이 할당됩니다.

다음 예는 지연 테이블을 사용할 수 있는 방법을 보여줍니다.

**캠페인과 관련된 값 이벤트 식별**

고객이 특정 광고 캠페인에 응답하기 전후에 7일 동안 고객의 활동을 추적한다고 가정해 보겠습니다. 특정 광고 캠페인에 대한 지연을 보려면 관심 캠페인을 지연 테이블의 이벤트로 설정합니다.

아래 작업 공간에서 지연은 Campaign 11566(이 캠페인에 대한 응답으로 세션)의 선택을 기반으로 합니다.

![](assets/vis_Latency.png)

지연이 &quot;+0일&quot;이면 Campaign 11566에 대한 응답으로 세션과 같은 날 발생한 동일한 고객에 대한 다른 모든 세션을 식별합니다.

지연 시간 &quot;-2일&quot;은 고객이 캠페인에 응답하기 2일 전에 발생한 동일한 고객에 대한 세션을 식별합니다.

지연 시간 &quot;+7일&quot;은 캠페인에 응답한 후 7일 후 발생한 동일한 고객에 대한 세션을 식별합니다.

다음 섹션에 나열된 절차 외에도 정렬 요소, 마스크 요소, 시리즈 범례 추가, 데이터 내보내기 등과 같이 테이블에서 수행할 수 있는 동일한 작업을 모두 수행할 수 있습니다. 자세한 내용은 [표](../../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f).

## 지연 테이블 만들기 {#section-31a03031d9854ef7acc2462d4f37678d}

지연 테이블을 만들려면 먼저 선택을 하고 해당 선택을 지연을 추적할 이벤트로 설정합니다.

1. 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고, 지연 테이블을 구성하는 데 사용되는 가산 차원을 기반으로 해야 하는 원하는 시각화를 엽니다.

   예, 에서 [!DNL Site] 시각화는 세션을 기반으로 해야 합니다.

1. 빈 지연 테이블을 엽니다.
1. 작업 공간에서 선택
1. 지연 테이블 내에서 마우스 오른쪽 단추를 클릭하고 를 클릭합니다. **[!UICONTROL Set Event]**.

![](assets/vis_Latency_SetEvent.png)

>[!NOTE]
>
>선택한 이벤트는 선택 사항을 지연 차원으로 저장하지 않는 한 지속되지 않습니다. 단계에 대해서는 [지연 Dimension 재사용](../../../home/c-get-started/c-analysis-vis/c-lat-tbls.md#section-29c6483bf9ba476fb1c24ad1df253f46).

## 지연 테이블 재사용 {#section-05f741169d204213b6537dce553e4f73}

동일한 지연 테이블을 다시 사용하려는 경우 지연 테이블을 로컬로 저장하거나 적절한 권한이 있는 경우 특정 프로필의 모든 사용자가 액세스할 수 있도록 서버에 저장할 수 있습니다.

**다른 작업공간에서 사용할 지연 테이블을 저장하려면**

1. 시각화의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 를 클릭합니다. **[!UICONTROL Save]**. 다음 [!DNL Save] 창이 나타납니다. 기본 저장 위치는 User\*profile name*\Work 폴더입니다.
1. 에서 [!DNL File name] 필드에서 시각화를 설명하는 이름을 입력하고 **[!UICONTROL Save]**.

**저장된 지연 테이블을 검색하려면**

1. 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL File]**. 다음 [!DNL Open Visualization] 창이 나타납니다.
1. 저장한 지연 테이블로 이동합니다.
1. 지연 테이블 시각화 파일( [!DNL *.vw]) 를 클릭하고 를 클릭합니다. **[!UICONTROL Open]**.

## 지연 차원 재사용 {#section-29c6483bf9ba476fb1c24ad1df253f46}

동일한 지연 차원을 다시 사용하려면 로컬로 지연 차원을 저장하거나 적절한 권한이 있는 경우 특정 프로필의 모든 사용자가 액세스할 수 있도록 서버에 저장할 수 있습니다.

사용자가 만드는 모든 지연 차원은 프로필의 Dimension 디렉토리에 저장되며 [!DNL Change Dimension] Data Workbench 내의 드롭다운 목록.

**다른 작업 공간에서 사용할 지연 차원을 저장하려면**

1. 마우스 오른쪽 단추를 클릭합니다. [!DNL Latency] 열 레이블 또는 해당 요소 중 하나를 클릭합니다. **[!UICONTROL Save Dimension]**. 다음 [!DNL Save Dimension As] 창이 나타납니다.
1. Dimension 디렉토리 내에서 적절한 하위 디렉토리를 선택하거나 생성합니다.
1. 에서 [!DNL File name] 필드에서 차원의 수사적 이름을 입력합니다(예: [!DNL Latency for Campaign 11565.dim]) 를 클릭하고 를 클릭합니다. **[!UICONTROL Save]**.

**저장된 지연 차원을 검색하려면**

1. 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL File]**. 다음 [!DNL Open Visualization] 창이 나타납니다.
1. User\*profile name*\Dimension 폴더에 저장한 지연 시각화로 이동합니다.
1. 지연 차원 파일( [!DNL *.dim]) 를 클릭하고 를 클릭합니다. **[!UICONTROL Open]**.

## Microsoft Excel로 내보내기 {#section-3dffa5c3aab14cdaa40c78b81b08fe53}

창 내보내기에 대한 자세한 내용은 [창 데이터 내보내기](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349).

## TSV 파일로 내보내기 {#section-fd921f351c994ed0a94f63d3bd5b5a87}

창 내보내기에 대한 자세한 내용은 [창 데이터 내보내기](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349).
