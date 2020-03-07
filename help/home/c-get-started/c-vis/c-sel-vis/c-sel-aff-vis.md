---
description: 작업 영역 내에서 시각화는 쿼리 결과 집합을 나타냅니다.
solution: Analytics
title: 선택 사항이 다른 시각화에 미치는 영향 이해
topic: Data workbench
uuid: d46f4e8d-df6f-4a7f-a796-eb9f11536ae5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 선택 사항이 다른 시각화에 미치는 영향 이해{#understanding-how-a-selection-affects-other-visualizations}

작업 영역 내에서 시각화는 쿼리 결과 집합을 나타냅니다.

선택 시 데이터 워크벤치는 작업 공간에서 시각화를 생성하는 데 사용하는 쿼리의 결과를 필터링합니다. 특정 필터는 시각화에 따라 달라집니다.

다음 예는 데이터 워크벤치가 세 가지 다른 유형의 시각화에 선택 사항을 적용하는 방법을 보여줍니다. 이러한 예제를 검토하면 선택 사항이 시각화에 미치는 필터링 효과를 이해하는 데 도움이 됩니다. 또한 필터링된 시각화에서 표시되는 결과를 해석하는 방법을 이해하는 데에도 도움이 됩니다.

* [세션 지표로 시각화 필터링](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-7cc06493ecb34cd4a696dbf0f0a7aaef)
* [방문자 지표로 시각화 필터링](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-97d38c7f03e8457189a9c72d69514ed2)
* [방문자별 세션 지표로 시각화 필터링](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-f746182311d648dcb98716b0fe846e25)

## 세션 지표로 시각화 필터링 {#section-7cc06493ecb34cd4a696dbf0f0a7aaef}

이 예에서 왼쪽의 시각화에 [!DNL /direct.asp/?ldPage=hme] 있는 URI는 오른쪽의 시각화에 표시된 세션의 지표를 필터링합니다.

![](assets/client-vis1.png)

* **선택 사항이 쿼리에 미치는 영향:** 데이터 워크벤치는 선택한 URI에 대한 세션을 필터링합니다. 이 예에서는 요소의 값을 생성하는 쿼리가 다음과 같이 필터링됩니다. [!DNL /pops/disclosure_pop.asp]

   ```
   Sessions[ URI="/pops/disclosure_pop.asp" AND URI="/direct.asp
   /?ldPage=hme"] by Page View by Session
   ```

* **시각화 해석:** 필터링된 시각화는 시각화 및 [!DNL /direct.asp/?ldPage=hme]에 나열된 URI를 포함하는 세션 수를 나타냅니다. 이 예에서는 방문자가 [!DNL /pops/disclosure_pop.asp] 페이지와 동일한 세션에서 모두 본 동안 1,113개의 세션이 [!DNL /direct.asp/?ldPage=hme] 있었다는 것을 보여줍니다.

## 방문자 지표로 시각화 필터링 {#section-97d38c7f03e8457189a9c72d69514ed2}

이 예에서 왼쪽의 시각화의 [!DNL /direct.asp/?ldPage=home] URI는 오른쪽의 시각화에서 방문자에 대한 지표를 필터링하는 것입니다.

![](assets/client-vis2.png)

* **선택 사항이 쿼리에 미치는 영향:** 데이터 워크벤치는 선택한 URI에 대한 방문자를 필터링합니다. 이 예에서는 URI에 대한 값을 생성하는 [!DNL /pops/disclosure_pop.asp] 쿼리가 다음과 같이 필터링됩니다.

   ```
   Visitors[ URI="/pops/disclosure_pop.asp" by Page View by Visitor 
     AND URI="/direct.asp/?ldPage=hme" by Page View by Visitor ]
   ```

* **시각화 해석:** 필터링된 시각화는 시각화 및 [!DNL /direct.asp/?ldPage=hme] (동일한 세션 중에 반드시 나열되지는 않더라도) 목록에 있는 URI를 본 방문자를 나타냅니다. 위의 예는 2,041명의 방문자가 [!DNL /pops/disclosure_pop.asp] 및 [!DNL /direct.asp/?ldPage=hme]모두를 본 것을 보여줍니다.

## 방문자별 세션 지표로 시각화 필터링 {#section-f746182311d648dcb98716b0fe846e25}

이 예에서는 [!DNL /direct.asp/?ldPage=hme] 왼쪽의 시각화의 URI가 오른쪽의 시각화에서 세션별 지표를 필터링합니다.

![](assets/client-vis3.png)

* **선택 사항이 쿼리에 미치는 영향:** 데이터 워크벤치는 선택한 URI에 대해 세션별 방문자를 필터링합니다. 예를 들어 URI에 대한 값을 생성하는 [!DNL /pops/disclosure_pop.asp] 쿼리는 다음과 같이 필터링됩니다.

   ```
   Visitors[ ( URI="/pops/disclosure_pop.asp" by Page View 
     AND URI="/direct.asp/?ldPage=hme" by Page View ) by Session ]
   ```

* **시각화 해석:** 필터링된 시각화는 시각화와 동일한 세션 [!DNL /direct.asp/?ldPage=hme] 동안 두 URI를 모두 본 방문자를 나타냅니다. 이 예에서는 1,069명의 방문자가 단일 세션 동안 [!DNL /pops/disclosure_pop.asp] 및 [!DNL /direct.asp/?ldPage=hme] 둘 다를 보았다는 것을 보여줍니다.

