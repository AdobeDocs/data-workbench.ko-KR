---
description: 하위 집합을 만들 때는 수준을 지정해야 합니다.
solution: Analytics
title: 수준 선택
topic: Data workbench
uuid: 18c2bee7-a70f-4510-978f-830b56780f47
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 수준 선택{#select-a-level}

하위 집합을 만들 때는 수준을 지정해야 합니다.

레벨은 계산 가능한 차원입니다. 예를 들어, 웹 사이트 데이터를 사용하여 작업하는 경우 요일 차원에서 True 요소를 선택하고 하위 집합을 만드는 경우 보려는 수준을 선택해야 합니다.페이지 보기, 세션 또는 방문자.

* **요일=&quot;화&quot;(페이지 보기 기준):** 페이지 보기 수준에는 화요일에 발생한 페이지 보기만 표시됩니다.

   ![](assets/vis_Subset_byPageView.png)

* **요일=&quot;화&quot;(세션별):** 세션 수준에는 화요일에 발생한 세션만 표시됩니다.

   ![](assets/vis_Subset_bySession.png)

* **요일=&quot;화&quot; - 방문자:** 방문자 수준은 화요일에 사이트를 방문한 모든 방문자를 보여주지만, 동일한 방문자가 사이트에 온 다른 날들도 보여줍니다.

   ![](assets/vis_Subset_byVisitor.png)

