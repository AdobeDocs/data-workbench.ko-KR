---
description: 값 프로필 지표
title: 값 프로필 지표
uuid: 68951e33-013a-466b-b0f3-839eaef89cb5
exl-id: 9e95008c-1162-4f50-89d2-dcf5fcf8746a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 17%

---

# 값 프로필 지표{#value-profile-metrics}

| 지표 | 공식 | 레벨 | 설명 |
|---|---|---|---|
| 전환 | `Sessions[not Session_Value=#0]/Sessions` | 세션 | 비즈니스 가치 모델에 의해 정의된 대로 비즈니스 가치를 생성한 세션의 백분율입니다. |
| 값의 부분 | `Value/total(Value)` | 세션 | 선택한 세션 세트에서 생성된 전체 값의 백분율입니다. |
| 값 | `sum(Session_Value, Session)*0.01` | 세션 | 생성된 총 비즈니스 가치(달러 기준)입니다(비즈니스 가치 모델에 의해 정의됨). |
| 값 이벤트 | `Sessions[not Session_Value=#0]` | 세션 | 비즈니스 가치를 생성한 세션 수(비즈니스 가치 모델에 의해 정의됨). |
| 방문자당 값 이벤트 | `(Value_Events/Visitors) by Visitor` | 방문자 | 비즈니스 가치 모델에 의해 정의된 대로 비즈니스 값을 생성한 각 방문자의 평균 세션 수입니다. |
| 방문자당 값 | `(Value/Visitors) by Visitor` | 방문자 | 각 방문자에 의해 생성된 평균 비즈니스 가치(달러)입니다. |
