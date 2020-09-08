---
description: 'null'
solution: Analytics
title: 값 프로필 지표
topic: Data workbench
uuid: 68951e33-013a-466b-b0f3-839eaef89cb5
translation-type: tm+mt
source-git-commit: 662bf8fdff196814e5a11c1f5e1ae12d4d57e1db
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 16%

---


# 값 프로필 지표{#value-profile-metrics}

| 지표 | 공식 | 레벨 | 설명 |
|---|---|---|---|
| 전환 | `Sessions[not Session_Value=#0]/Sessions` | 세션 | 비즈니스 값(비즈니스 가치 모델에 의해 정의됨)을 생성한 세션의 백분율입니다. |
| Pct of Value | `Value/total(Value)` | 세션 | 선택한 세션 세트에서 생성된 전체 값의 백분율입니다. |
| 값 | `sum(Session_Value, Session)*0.01` | 세션 | 창출되는 총 비즈니스 가치(달러(비즈니스 가치 모델에 의해 정의됨). |
| 값 이벤트 | `Sessions[not Session_Value=#0]` | 세션 | 비즈니스 값(비즈니스 가치 모델에 의해 정의됨)을 생성한 세션 수입니다. |
| 방문자당 값 이벤트 | `(Value_Events/Visitors) by Visitor` | 방문자 | 비즈니스 값 모델에 의해 정의된 대로 비즈니스 값을 생성한 각 방문자에 대한 평균 세션 수입니다. |
| 방문자당 값 | `(Value/Visitors) by Visitor` | 방문자 | 각 방문자에 의해 생성된 평균 비즈니스 가치(달러) |
