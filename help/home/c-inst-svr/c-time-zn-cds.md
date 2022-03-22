---
description: Insight Server에서 시간 기반 매개 변수에 대한 지침 형식을 지정합니다.
title: 시간대 코드(Insight Server)
uuid: dcc8aa15-5846-4f24-8b82-e25ff89871ba
exl-id: d8923b01-24fe-4a70-9800-f2eedf567c6a
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 4%

---

# 시간대 코드{#time-zone-codes}

Insight Server에서 시간 기반 매개 변수에 대한 지침 형식을 지정합니다.

의 대부분의 시간 기반 매개 변수 [!DNL Insight Server] 는 다음 형식으로 지정됩니다.

*월 DD, YYYY HH:MM:SS 시간대*

예: 2013년 8월 13일 22일:30:EST 00

시간대는 다음 형식의 시스템 독립 시간대 형식(Coordinated Universal Time)으로 표시됩니다.

UTC +hmm *dstrules*

기호(+)는 더하기(+) 또는 빼기(-) 기호 중 하나일 수 있으며 *흠* 는 UTC와의 오프셋(시간 및 분 단위)입니다. 선택적 변수 *dstrules* 일광 절약 시간제 또는 유사한 시계 변환 정책을 구현할 규칙 세트를 지정합니다.

지정한 경우 *dstrules*, 이름이 인 탭으로 구분된 파일 *&lt; [!DNL dstrules]>* [!DNL .dst] 기본 프로필의 Dataset\TimeZone 디렉터리(특정 데이터 집합과 연결되지 않은 구성 파일의 경우) 또는 데이터 집합 프로필(데이터 집합과 관련된 구성 파일의 경우)에 있어야 합니다. 이 파일은 일광 절약 시간제에 대한 표준 시간대와 독립적인 규칙 집합을 지정합니다. 여러 해 동안 다양한 규칙 세트를 사용할 수 있습니다. 다음 [!DNL DST.dst] 기본 프로필에서 Adobe이 제공하는 파일은 2005년 에너지 정책법(2007년부터 적용)에 의해 설정된 표준 미국 규칙과 이전 년 동안 미국 규정을 지정합니다.

다음은 샘플 시간대 항목입니다.

* 미국 동부 일광 절약 시간: 시간대 = 문자열: UTC -0500 DST
* UTC 시간(오프셋 없음 및 없음) *dstrules* (GMT에 해당): 시간대 = 문자열: UTC -0000

이 형식을 사용하면 [!DNL Insight Server], [!DNL Insight], 및 [!DNL Report] 컴퓨터는 지정된 시간대와 같을 필요가 없습니다. 또한 [!DNL Insight Server] 컴퓨터에 동일한 시간대 설정이 필요하지 않습니다.

다음 표에는 시간 기반 매개 변수에서 시간대를 지정하는 데 사용할 수 있는 코드 목록이 나와 있습니다.

## 시간대 코드 테이블 {#section-3cab225b864f4e54ac4f5bd83ab4ed36}

>[!NOTE]
>
>일광 절약 시간제 또는 유사한 클럭 변환 정책을 구현하려면 [!DNL .dst] 에 적절한 규칙이 들어 있는 파일 *프로필 이름*\Dataset\표준 시간대 디렉토리 [!DNL Insight Server] 시스템.

| 코드 | 시간대 | GMT로부터의 오프셋 |
|---|---|---|
| gmt | 그리니치 평균 | 0 |
| est | 동부 표준 | 5 |
| 편집 | 동부 일광 | 5개 |
| cst | Central Standard | 6 |
| cdt | 중앙 일광 | 6 |
| mst | Mountain Standard | 7 |
| mdt | 일광 | 7 |
| pst | 태평양 표준 | 8 |
| pdt | 태평양 일광 | 8 |
