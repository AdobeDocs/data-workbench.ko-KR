---
description: 하위 집합을 생성할 때 레벨을 지정해야 합니다.
title: 수준 선택
uuid: 18c2bee7-a70f-4510-978f-830b56780f47
exl-id: 39d8407c-e2ec-4080-8918-26cafbf988df
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 4%

---

# 수준 선택{#select-a-level}

하위 집합을 생성할 때 레벨을 지정해야 합니다.

레벨은 계산 가능한 차원입니다. 예를 들어, 웹 사이트 데이터를 사용하여 작업하는 경우 요일 차원에서 True 요소를 선택하고 하위 집합을 생성하는 경우, 보려는 레벨을 선택해야 합니다.페이지 보기, 세션 또는 방문자

* **페이지 보기의 요일=&quot;화&quot;:** 페이지 보기 수준은 화요일에 발생한 페이지 보기 수만 표시합니다.

   ![](assets/vis_Subset_byPageView.png)

* **요일=&quot;세션&quot;:** 세션 레벨은 화요일에 발생한 세션만 표시합니다.

   ![](assets/vis_Subset_bySession.png)

* **방문자의 요일=&quot;화&quot;:** 방문자 수준은 화요일에 사이트를 방문한 모든 방문자를 표시하지만 동일한 방문자가 사이트에 방문한 다른 날짜도 보여줍니다.

   ![](assets/vis_Subset_byVisitor.png)
