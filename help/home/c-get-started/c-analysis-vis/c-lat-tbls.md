---
description: 지연 테이블 시각화는 지연 차원이 포함된 테이블이며, 지연 차원은 특정 이벤트가 발생한 이후 경과된 시간을 측정하는 파생 차원의 유형입니다.
title: 지연 테이블
uuid: 8081540c-f96c-424e-802d-05d1be5a728d
exl-id: 22f6d52f-e1c2-430a-9e69-3440be0ecdea
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 1%

---

# 지연 테이블{#latency-tables}

지연 테이블 시각화는 지연 차원이 포함된 테이블이며, 지연 차원은 특정 이벤트가 발생한 이후 경과된 시간을 측정하는 파생 차원의 유형입니다.

하나 이상의 시각화 내에서 선택하고 [이벤트 컨텍스트 설정] 메뉴 옵션을 사용하여 이러한 선택 사항을 이벤트로 설정하여 이벤트를 정의합니다. 지연 테이블은 캠페인과 관련된 활동 또는 시간 상관 관계를 찾는 특정 고객 주문을 추적하는 데 특히 유용합니다.

[!DNL Site]에서 지연 표는 이벤트 전후로 7일 정도 발생한 방문자 세션에 대한 정보를 제공하지만, 다른 계산 가능한 차원과 시간 차원에 대한 정보를 제공하도록 지연 테이블을 구성할 수 있습니다. [지연 테이블 구성](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/c-config-ltcy-tbls.md#concept-7175c3defec64556994f0dfcccb7d15c)을 참조하십시오.

선택한 특정 이벤트에 속하는 세션과 같은 상위 차원의 요소에는 0의 지연이 있습니다. 다른 모든 요소는 이벤트에서 거리(적절한 시간 차원)를 반영하는 대기 시간이 지정됩니다.

다음 예제에서는 지연 테이블을 사용할 수 있는 방법을 보여 줍니다.

**캠페인과 관련된 값 이벤트 식별**

특정 광고 캠페인에 반응하기 전과 후 7일 동안 고객의 활동을 추적하려는 경우 특정 광고 캠페인에 대한 지연을 보려면 관심 캠페인을 지연 테이블에 대한 이벤트로 설정합니다.

아래 작업 영역의 지연은 캠페인 11566(이 캠페인에 대한 응답의 세션)의 선택을 기반으로 합니다.

![](assets/vis_Latency.png)

&quot;+0일&quot;의 지연은 Campaign 11566에 대한 응답으로 세션뿐만 아니라 같은 날에 발생한 동일한 고객에 대한 다른 모든 세션을 식별합니다.

&quot;-2일&quot;의 지연은 고객이 캠페인에 응답하기 2일 전에 발생한 동일한 고객에 대한 세션을 식별합니다.

&quot;+7일&quot;의 지연은 캠페인에 반응한 후 7일이 지난 동일한 고객에 대한 세션을 식별합니다.

다음 섹션에 나열된 절차 외에도 정렬 요소, 마스크 요소, 시리즈 범례 추가, 데이터 내보내기 등과 같이 테이블에서 수행할 수 있는 모든 동일한 작업을 수행할 수 있습니다. 자세한 내용은 [표](../../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f)를 참조하십시오.

## 지연 테이블 {#section-31a03031d9854ef7acc2462d4f37678d} 만들기

대기 시간 테이블을 만들려면 먼저 선택 항목을 선택한 다음 지연을 추적하려는 이벤트로 설정합니다.

1. 작업 공간 내에서 마우스 오른쪽 버튼을 클릭하고 원하는 시각화를 엽니다. 이 시각화는 지연 테이블을 구성하는 데 사용되는 계산 가능한 차원을 기반으로 합니다.

   예를 들어 [!DNL Site]에서 시각화는 세션을 기반으로 해야 합니다.

1. 빈 지연 테이블을 엽니다.
1. 작업 영역에서 선택 영역을 만듭니다.
1. 지연 테이블 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Set Event]**&#x200B;을 클릭합니다.

![](assets/vis_Latency_SetEvent.png)

>[!NOTE]
>
>선택한 이벤트는 선택 사항을 지연 차원으로 저장하지 않으면 지속되지 않습니다. 단계에 대해서는 [지연 Dimension 다시 사용](../../../home/c-get-started/c-analysis-vis/c-lat-tbls.md#section-29c6483bf9ba476fb1c24ad1df253f46)을 참조하십시오.

## 지연 테이블 {#section-05f741169d204213b6537dce553e4f73} 다시 사용

동일한 지연 테이블을 다시 사용하려는 경우 지연 테이블을 로컬에 저장하거나 적절한 권한이 있는 경우 특정 프로필의 모든 사용자가 액세스할 수 있도록 서버에 저장할 수 있습니다.

**다른 작업 영역에서 사용할 지연 테이블을 저장하려면**

1. 시각화의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다. [!DNL Save] 창이 나타납니다. 기본 저장 위치는 사용자\*프로필 이름*\작업 폴더입니다.
1. [!DNL File name] 필드에 시각화에 사용할 설명형 이름을 입력하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

**저장된 지연 테이블을 검색하려면**

1. 작업 공간 내에서 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL File]**&#x200B;를 클릭합니다. [!DNL Open Visualization] 창이 나타납니다.
1. 저장한 지연 테이블로 이동합니다.
1. 지연 테이블 시각화 파일( [!DNL *.vw])을 선택하고 **[!UICONTROL Open]**&#x200B;을 클릭합니다.

## 지연 차원 {#section-29c6483bf9ba476fb1c24ad1df253f46} 다시 사용

동일한 지연 차원을 다시 사용하려면 지연 차원을 로컬에 저장하거나 적절한 권한이 있는 경우 특정 프로필의 모든 사용자가 액세스할 수 있도록 서버에 저장할 수 있습니다.

만드는 모든 지연 차원은 프로필의 Dimension 디렉토리에 저장되고 Data Workbench 내의 [!DNL Change Dimension] 드롭다운 목록에서 사용할 수 있습니다.

**다른 작업 영역에서 사용할 지연 차원을 저장하려면**

1. [!DNL Latency] 열 레이블 또는 해당 요소 중 하나를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save Dimension]** 을 클릭합니다. [!DNL Save Dimension As] 창이 나타납니다.
1. Dimension 디렉토리 내에서 적절한 하위 디렉토리를 선택하거나 만듭니다.
1. [!DNL File name] 필드에 차원의 설명형 이름(예: [!DNL Latency for Campaign 11565.dim])을 입력하고 **[!UICONTROL Save]**&#x200B;를 클릭합니다.

**저장된 지연 차원을 검색하려면**

1. 작업 공간 내에서 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL File]**&#x200B;를 클릭합니다. [!DNL Open Visualization] 창이 나타납니다.
1. User\*profile name*\Dimension 폴더에 저장한 지연 시각화로 이동합니다.
1. 지연 차원 파일( [!DNL *.dim])을 선택하고 **[!UICONTROL Open]**&#x200B;을 클릭합니다.

## Microsoft Excel로 내보내기 {#section-3dffa5c3aab14cdaa40c78b81b08fe53}

창 내보내기에 대한 자세한 내용은 [창 데이터 내보내기](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349)를 참조하십시오.

## TSV 파일로 내보내기 {#section-fd921f351c994ed0a94f63d3bd5b5a87}

창 내보내기에 대한 자세한 내용은 [창 데이터 내보내기](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349)를 참조하십시오.
