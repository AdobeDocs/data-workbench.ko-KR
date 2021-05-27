---
description: 단기, 임시 분석 요구 사항에도 대시보드를 만드는 것이 좋습니다.
title: 대시보드 만들기
uuid: 5b9e9db2-d7ac-4c97-8df0-74a9e5a0c496
exl-id: bd51d4c0-bcf2-4ba6-8b32-de06c74f359f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# 대시보드 만들기{#creating-a-dashboard}

단기, 임시 분석 요구 사항에도 대시보드를 만드는 것이 좋습니다.

>[!NOTE]
>
>읽기 전용 사용자는 대시보드를 만들 수 없습니다. 이 섹션은 일반 사용자 및 관리자만 적용됩니다.

사용자는 다음과 같은 몇 가지 이유로 대시보드를 만들도록 결정할 수 있습니다.

* 대시보드를 재사용하거나 공유할 필요 없이 즉시 분석할 수 있도록 처음부터 새로운 대시보드를 시작할 수 있습니다.
* 저장하고 다시 사용하되 공유하지는 않으려는 개인 분석을 수행할 목적으로 새 대시보드를 만들 수 있습니다.
* 사용자 및 나머지 대시보드 사용자 모집단에서 액세스할 수 있도록 새 대시보드를 만들고, 저장하고, 공유할 수 있습니다. 어떤 경우든 각 시나리오는 동일한 지점에서 시작됩니다.빈 대시보드 캔버스.

>[!NOTE]
>
>대시보드를 작성하기 전에 쿼리 비율을 10% 또는 25%와 같이 낮은 수준으로 줄이는 것이 좋습니다. 이렇게 하면 전체 쿼리를 수행하는 것보다 Data Workbench에서 데이터 샘플을 훨씬 빨리 가져올 수 있습니다. 이렇게 샘플링된 결과는 훨씬 더 빠르게 반환되므로 대시보드 및 분석을 프레이밍하는 동안 이상적인 응답성을 제공합니다. 쿼리를 완료하기 위해 실행할 준비가 되면 쿼리-to 매개 변수를 100%로 업데이트할 수 있습니다. 쿼리 완료를 조정하려면 [Query-to 매개 변수](../../../home/c-adobe-data-workbench-dashboard/c-dashboards/c-query-to-parameter.md#concept-33db106e28bc4108bca9e8d0a440d323)를 참조하십시오.

새 대시보드를 만들려면 대시보드 메뉴에서 **[!UICONTROL New]** 을 선택합니다.

![](assets/new_dashboard.png)

분석 요구 사항에 따라 시각화를 추가하고 구성할 수 있는 빈 대시보드 캔버스가 표시됩니다. 작업할 때 저장할 때까지 서버에서 업데이트되지 않습니다.

다음으로 표시할 데이터 종류와 표시할 방법을 결정합니다. 일반적으로 테이블 시각화로 시작하여 원시 데이터를 확인한 다음 해당 차트에 맞게 다른 차트를 작성하는 데 도움이 됩니다. 시각화를 추가 및 구성하는 방법에 대한 자세한 내용은 [시각화 만들기](../../../home/c-adobe-data-workbench-dashboard/c-visualizations/t-creating-visualizations.md#task-c6f1d20fa2484aeeb9a8487625054ecf)를 참조하십시오. 대시보드를 작성하기 위해 시각화를 추가 및 구성한 후에는 다음 항목이 표시됩니다.

![](assets/after_configure.png)

이 시점에서는 분석을 수행하고 대시보드를 버리거나, 대시보드를 재사용 및/또는 공유하기 위해 서버에 저장하도록 선택할 수 있습니다. 분석을 수행하기 위해 대시보드와 상호 작용하는 방법에 대한 자세한 내용은 대시보드](../../../home/c-adobe-data-workbench-dashboard/c-making-selections-within-the-dashboard/c-making-selections-within-the-dashboard.md#concept-0989862de0044cc4bbfd7f4441275fc4) 내에서 선택 [섹션을 참조하십시오.
