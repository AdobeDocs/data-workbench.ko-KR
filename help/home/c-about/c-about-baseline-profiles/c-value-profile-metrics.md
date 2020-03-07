---
description: 'null'
solution: Analytics
title: 값 프로필 지표
topic: Data workbench
uuid: 68951e33-013a-466b-b0f3-839eaef89cb5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 값 프로필 지표{#value-profile-metrics}

| 지표 | 공식 | 레벨 | 설명 |
|---|---|---|---|
| 변환 | [!DNL[Sessionsnot Session_Value=#0]/Sessions] | 세션 | 비즈니스 가치를 생성한 세션의 백분율(비즈니스 값 모델에 의해 정의됨). |
| Pct of Value | [!DNL Value/total(Value)] | 세션 | 선택한 세션 세트에서 생성된 전체 값의 비율입니다. |
| 값 | [!DNL sum(Session_Value, Session)*0.01] | 세션 | 생성된 총 비즈니스 가치(달러)(비즈니스 가치 모델에 의해 정의됨). |
| 값 이벤트 | [!DNL[Sessionsnot Session_Value=#0]] | 세션 | 비즈니스 값을 생성한 세션 수(비즈니스 가치 모델에 의해 정의됨). |
| 방문자당 값 이벤트 | [!DNL (Value_Events/Visitors) by Visitor] | 방문자 | 비즈니스 값을 생성한 각 방문자에 대한 평균 세션 수(비즈니스 가치 모델에 의해 정의됨). |
| 방문자당 값 | [!DNL (Value/Visitors) by Visitor] | 방문자 | 각 방문자에 의해 생성된 평균 비즈니스 가치(달러)입니다. |
