---
description: 작업 공간 내에서 시각화는 쿼리 결과 집합을 나타냅니다.
title: 선택 사항이 다른 시각화에 미치는 영향 이해
uuid: d46f4e8d-df6f-4a7f-a796-eb9f11536ae5
exl-id: 7756646b-9309-41aa-a098-8988f6c065c8
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 3%

---

# 선택 사항이 다른 시각화에 미치는 영향 이해{#understanding-how-a-selection-affects-other-visualizations}

작업 공간 내에서 시각화는 쿼리 결과 집합을 나타냅니다.

선택 영역을 선택하면 Data Workbench은 작업 공간에서 시각화를 생성하는 데 사용하는 질의 결과를 필터링합니다. 특정 필터는 시각화에 따라 달라집니다.

다음 예는 Data Workbench이 3가지 시각화 유형에 선택 사항을 적용하는 방법을 보여줍니다. 이러한 예제를 검토하면 선택 사항이 시각화에 미치는 필터링 효과를 이해하는 데 도움이 됩니다. 또한 필터링된 시각화에서 표시되는 결과를 해석하는 방법을 이해하는 데에도 도움이 됩니다.

* [세션 지표로 시각화 필터링](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-7cc06493ecb34cd4a696dbf0f0a7aaef)
* [방문자 지표로 시각화 필터링](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-97d38c7f03e8457189a9c72d69514ed2)
* [세션별 방문자 수 지표로 시각화 필터링](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-f746182311d648dcb98716b0fe846e25)

## 세션 지표 {#section-7cc06493ecb34cd4a696dbf0f0a7aaef}으로 시각화 필터링

이 예에서 왼쪽의 시각화에 있는 [!DNL /direct.asp/?ldPage=hme] URI는 오른쪽의 시각화에 표시된 세션의 지표를 필터링합니다.

![](assets/client-vis1.png)

* **쿼리에 대한 선택 효과:Data Workbench은 선택한 URI에 대한 세션을** 필터링합니다. 이 예에서 [!DNL /pops/disclosure_pop.asp] 요소에 대한 값을 생성하는 쿼리는 다음과 같이 필터링됩니다.

   ```
   Sessions[ URI="/pops/disclosure_pop.asp" AND URI="/direct.asp
   /?ldPage=hme"] by Page View by Session
   ```

* **시각화 해석:** 필터링된 시각화는 시각화 및 시각화에 나열되는 URI를 포함하는 세션 수를 나타냅니다 [!DNL /direct.asp/?ldPage=hme]. 이 예는 방문자가 동일한 세션에서 [!DNL /pops/disclosure_pop.asp] 페이지와 [!DNL /direct.asp/?ldPage=hme] 페이지를 모두 본 동안 1,113개의 세션이 있음을 보여줍니다.

## 방문자 지표가 {#section-97d38c7f03e8457189a9c72d69514ed2}인 시각화 필터링

이 예에서 왼쪽의 시각화에 있는 [!DNL /direct.asp/?ldPage=home] URI는 오른쪽의 시각화에서 방문자에 대한 지표를 필터링하는 것입니다.

![](assets/client-vis2.png)

* **쿼리에 대한 선택 효과:Data Workbench은 선택한 URI의** 방문자를 필터링합니다. 이 예에서 [!DNL /pops/disclosure_pop.asp] URI에 대한 값을 생성하는 쿼리는 다음과 같이 필터링됩니다.

   ```
   Visitors[ URI="/pops/disclosure_pop.asp" by Page View by Visitor 
     AND URI="/direct.asp/?ldPage=hme" by Page View by Visitor ]
   ```

* **시각화 해석: 필터링된 시각화** 는 시각화에 나열된 URI를 본 방문자 및  [!DNL /direct.asp/?ldPage=hme] (동일한 세션 중에는 반드시 발생하지 않음)를 나타냅니다. 위의 예는 2,041명의 방문자가 [!DNL /pops/disclosure_pop.asp]과 [!DNL /direct.asp/?ldPage=hme]을(를) 모두 보았음을 보여줍니다.

## 방문자별 세션 지표로 시각화 필터링 {#section-f746182311d648dcb98716b0fe846e25}

이 예에서 왼쪽의 시각화에 있는 [!DNL /direct.asp/?ldPage=hme] URI는 오른쪽의 시각화에서 세션별 방문자 지표를 필터링하는 것입니다.

![](assets/client-vis3.png)

* **쿼리에 대한 선택 효과:Data Workbench은 선택한 URI에 대한** 세션별 방문자를 필터링합니다. 예를 들어 [!DNL /pops/disclosure_pop.asp] URI에 대한 값을 생성하는 쿼리는 다음과 같이 필터링됩니다.

   ```
   Visitors[ ( URI="/pops/disclosure_pop.asp" by Page View 
     AND URI="/direct.asp/?ldPage=hme" by Page View ) by Session ]
   ```

* **시각화 해석: 필터링된 시각화** 는 시각화에 나열되고 동일한 세션  [!DNL /direct.asp/?ldPage=hme] 중에 두 URI를 모두 본 방문자를 나타냅니다. 이 예는 1,069명의 방문자가 단일 세션 중에 [!DNL /pops/disclosure_pop.asp]과 [!DNL /direct.asp/?ldPage=hme]을 모두 보았음을 보여줍니다.
