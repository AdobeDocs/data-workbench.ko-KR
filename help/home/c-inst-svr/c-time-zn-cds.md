---
description: Insight Server에서 시간 기반 매개 변수에 대한 형식 지정 지침을 참조하십시오.
solution: Insight
title: 시간대 코드
uuid: dcc8aa15-5846-4f24-8b82-e25ff89871ba
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 시간대 코드{#time-zone-codes}

Insight Server에서 시간 기반 매개 변수에 대한 형식 지정 지침을 참조하십시오.

대부분의 시간 기반 매개 변수는 다음 형식으로 [!DNL Insight Server] 지정됩니다.

*월 DD, YYYY HH:MM:SS 표준 시간대*

예:2013년 8월 13일 22:30:00 EST

시간대는 시스템 독립적인 표준 시간대 형식(조정된 보편적 시간)으로 표현되며 다음과 같은 형식을 사용합니다.

UTC +hmm *틀*

기호(+)는 더하기(+) 또는 빼기(-) 기호 중 하나일 수 있으며 *hmm* 은 시간 및 분 단위의 UTC로부터의 오프셋입니다. 옵션 변수 *규칙은* 일광 절약 시간제 또는 유사한 시계 이동 정책을 구현할 규칙 세트를 지정합니다.

규칙을 *지정하는*&#x200B;경우 *&lt;>[!DNL dstrules]탭으로 구분된 파일이 기본 프로필의 Dataset\TimeZone 디렉터리(특정 데이터 세트와 연결되지 않은 구성 파일의 경우) 또는 데이터 세트 프로필(데이터 세트별 구성 파일의 경우)에 있어야 합니다* [!DNL .dst] . 이 파일은 일광 절약 시간에 대한 표준 시간대 독립적인 규칙 세트를 지정합니다. 여러 해에 대해 다른 규칙 세트를 사용할 수 있습니다. Adobe가 기본 프로파일에 제공한 [!DNL DST.dst] 파일은 2005년 에너지 정책법(2007년 이후)에 의해 제정된 표준 미국 규정과 이전 년 동안 미국 규칙을 지정합니다.

샘플 표준 시간대 항목은 다음과 같습니다.

* 미국 동부 일광 절약 시간:시간대 = 문자열:UTC -0500 DST
* 오프셋이 없고 *규칙이* 없는 UTC 시간(GMT에 해당):시간대 = 문자열:UTC -0000

이 형식을 사용하는 경우 시스템 표준 시간대 [!DNL Insight Server][!DNL Insight]및 [!DNL Report] 컴퓨터의 시스템 표준 시간대는 지정된 표준 시간대와 같을 필요가 없습니다. 또한 [!DNL Insight Server] 컴퓨터의 모든 활성 데이터 집합 프로필에는 동일한 표준 시간대 설정이 필요하지 않습니다.

다음 표에는 시간 기반 매개 변수에서 시간대를 지정하는 데 사용할 수 있는 코드 목록이 포함되어 있습니다.

## 시간대 코드 테이블 {#section-3cab225b864f4e54ac4f5bd83ab4ed36}

>[!NOTE]
>
>일광 절약 시간제 또는 유사한 시계 이동 정책을 구현하는 경우, 적절한 규칙이 포함된 [!DNL .dst] 파일을 *프로필 이름*\Dataset\Timezone directory on the [!DNL Insight Server] 시스템에 저장해야 합니다.

| 코드 | 시간대 | GMT에서 오프셋 |
|---|---|---|
| gmt | 그리니치 평균 | 0 |
| est | 동부 표준 | 5 |
| edit | 동부 일광 | 5 |
| cst | Central Standard | 6 |
| cdt | 중앙 일광 | 6 |
| mst | Mountain Standard | 7 |
| mdt | Mountain Daylight | 7 |
| past | Pacific Standard | 8 |
| pdt | 태평양 일광 | 8 |

