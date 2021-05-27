---
description: Insight Server에서 시간 기반 매개 변수에 대한 지침 형식을 지정합니다.
title: 시간대 코드
uuid: dcc8aa15-5846-4f24-8b82-e25ff89871ba
exl-id: d8923b01-24fe-4a70-9800-f2eedf567c6a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 5%

---

# 시간대 코드{#time-zone-codes}

Insight Server에서 시간 기반 매개 변수에 대한 지침 형식을 지정합니다.

[!DNL Insight Server]에 있는 대부분의 시간 기반 매개 변수는 다음 형식으로 지정됩니다.

*월 DD, YYYY HH:MM:SS 시간대*

예:2013년 8월 13일 22:30:00

시간대는 다음 형식의 시스템 독립 시간대 형식(Coordinated Universal Time)으로 표시됩니다.

UTC +hhmm *dstrules*

기호(+)는 더하기(+) 또는 빼기(-) 기호 중 하나일 수 있으며 *hmm*&#x200B;은 시간 및 분 단위의 UTC로부터의 오프셋입니다. 옵션 변수 *규칙*&#x200B;은 일광 절약 시간제 또는 유사한 클럭 변환 정책을 구현할 규칙 세트를 지정합니다.

*dstrules*&#x200B;를 지정하는 경우, *&lt; [!DNL dstrules]* [!DNL .dst]라는 탭 구분 파일이 기본 프로필의 Dataset\TimeZone 디렉토리(특정 데이터 세트와 연결되지 않은 구성 파일의 경우) 또는 데이터 집합 프로필(데이터 집합별 구성 파일의 경우)에 있어야 합니다. 이 파일은 일광 절약 시간제에 대한 표준 시간대와 독립적인 규칙 집합을 지정합니다. 여러 해 동안 다양한 규칙 세트를 사용할 수 있습니다. Base Profile에서 Adobe이 제공하는 [!DNL DST.dst] 파일은 2005년 에너지 정책법에 의해 설정된 표준 미국 규칙(2007년부터 적용) 및 이전 연도의 미국 규칙을 지정합니다.

다음은 샘플 시간대 항목입니다.

* 미국 동부 일광 절약 시간:시간대 = 문자열:UTC -0500 DST
* 오프셋 없이 *dstrules*(GMT에 해당)가 없는 UTC 시간:시간대 = 문자열:UTC -0000

이 형식을 사용하면 [!DNL Insight Server], [!DNL Insight] 및 [!DNL Report] 컴퓨터의 시스템 시간대가 지정된 시간대와 동일하지 않아도 됩니다. 또한 [!DNL Insight Server] 컴퓨터의 모든 활성 데이터 집합 프로필에는 동일한 시간대 설정이 있어야 합니다.

다음 표에는 시간 기반 매개 변수에서 시간대를 지정하는 데 사용할 수 있는 코드 목록이 나와 있습니다.

## 시간대 코드 테이블 {#section-3cab225b864f4e54ac4f5bd83ab4ed36}

>[!NOTE]
>
>일광 절약 시간제 또는 유사한 클럭 변환 정책을 구현하는 경우 *프로필 이름*\Dataset\Timezone directory on the [!DNL Insight Server] 컴퓨터에 적절한 규칙이 들어 있는 [!DNL .dst] 파일을 저장해야 합니다.

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
