---
description: 시간대 코드 및 형식에 대한 정보입니다.
title: 시간대 코드 및 형식
uuid: 5698882a-9682-41d8-88d3-8471578a22cc
exl-id: 2829c4ca-af6f-4ddb-acce-b33c3b552ba7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# 시간대 코드{#time-zone-codes}

{{eol}}

시간대 코드 및 형식에 대한 정보입니다.

Data Workbench 서버의 대부분의 시간 기반 매개 변수는 다음 형식으로 지정됩니다.

* 월 DD , YYYY HH:MM:SS TZone
* 예: 2013년 8월 13일 22일:30:EST 00

시간대는 다음 형식의 시스템 독립 시간대 형식(Coordinated Universal Time)으로 표시됩니다.

* UTC +hhhmm 문자열

기호(+)는 더하기(+) 또는 빼기(-) 기호 중 하나일 수 있으며, hmm은 UTC로부터의 시간 및 분 단위입니다. 선택적 변수 규칙은 일광 절약 시간제 또는 유사한 시계 변환 정책을 구현할 규칙 세트를 지정합니다.

규칙을 지정하는 경우, [!DNL dstrules.dst] 다음 중 하나의 Dataset\TimeZone 디렉터리에 있어야 합니다. [!DNL Base] 프로필(특정 데이터 세트와 연관되지 않은 구성 파일의 경우) 또는 데이터 세트 프로필(데이터 세트에 고유한 구성 파일의 경우) 이 파일은 일광 절약 시간제에 대한 표준 시간대와 독립적인 규칙 집합을 지정합니다. 여러 해 동안 다양한 규칙 세트를 사용할 수 있습니다. 다음 [!DNL DST.dst] Adobe이 제공하는 파일 [!DNL Base] 이 프로필은 2005년 에너지 정책법에 의해 제정된 표준 미국 규칙(2007년 시행)과 이전 년 동안 미국 규정을 지정합니다.

다음은 샘플 시간대 항목입니다.

* 미국 동부 일광 절약 시간: 시간대 = 문자열: UTC -0500 DST
* 오프셋 및 조건이 없는 UTC 시간(GMT에 해당): 시간대 = 문자열: UTC -0000

이 형식을 사용하는 경우 Data Workbench 서버, Data Workbench 및 보고서 컴퓨터의 시스템 시간대가 지정된 시간대와 같을 필요가 없습니다. 또한 Data Workbench 서버 컴퓨터의 모든 활성 데이터 세트 프로필에는 동일한 시간대 설정이 필요하지 않습니다.

다음 표에는 시간 기반 매개 변수에서 시간대를 지정하는 데 사용할 수 있는 코드 목록이 나와 있습니다.

## 시간대 코드 테이블 {#section-b4f965b872c543e2ac52a3c94410d076}

일광 절약 시간제 또는 유사한 클럭 변환 정책을 구현하려면 [!DNL .dst] 프로필 이름에 적절한 규칙이 들어 있는 파일 [!DNL \Dataset\Timezone] data workbench 서버 시스템의 디렉토리입니다.

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
