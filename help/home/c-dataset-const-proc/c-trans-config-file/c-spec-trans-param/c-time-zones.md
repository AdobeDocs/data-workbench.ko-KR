---
description: 'Transformation.cfg 파일의 시간대 매개 변수는 데이터 세트 프로필에서 시간 차원, 시간 전환(예: x-local-timestring 필드 정의) 및 모든 로컬 시간의 형식을 제어합니다.'
title: 시간대
uuid: 7b253c5a-f2b1-410c-9433-f13ed1d7a8b3
exl-id: c8dc49d5-3245-428a-bfb9-42970df73d3e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# 시간대{#time-zones}

{{eol}}

Transformation.cfg 파일의 시간대 매개 변수는 데이터 세트 프로필에서 시간 차원, 시간 전환(예: x-local-timestring 필드 정의) 및 모든 로컬 시간의 형식을 제어합니다.

>[!NOTE]
>
>시간대 매개 변수는 시스템 로컬 시간으로 표시되는 상태 및 이벤트 로그의 타임스탬프와 같은 시스템 수준 기능에 영향을 주지 않습니다.

시간대 매개 변수는 시스템 독립적인 표준 시간대 형식(&quot;Coordinated Universal Time&quot;)을 다음 형식으로 지원합니다.

시간대 = 문자열: UTC +hhhmm 문자열

기호(+)는 더하기(+) 또는 빼기(-) 기호 중 하나일 수 있으며 *흠* 는 UTC와의 오프셋(시간 및 분 단위)입니다. 선택적 변수 *dstrules* 일광 절약 시간제 또는 유사한 시계 변환 정책을 구현할 규칙 세트를 지정합니다.

지정한 경우 *dstrules*, 이름이 인 탭으로 구분된 파일 [!DNL dstrules .dst] 데이터 집합 프로필의 Dataset\TimeZone 하위 디렉터리 내에 있어야 합니다. 이 파일은 일광 절약 시간제에 대한 표준 시간대와 독립적인 규칙 집합을 지정합니다. 여러 해 동안 다양한 규칙 세트를 사용할 수 있습니다. 다음 [!DNL DST.dst] 기본 프로필에서 Adobe이 제공하는 파일은 2005년 에너지 정책법(2007년부터 적용)에 의해 설정된 표준 미국 규칙과 이전 년 동안 미국 규정을 지정합니다.

다음은 샘플 시간대 항목입니다.

* 미국 동부 일광 절약 시간: 시간대 = 문자열: UTC -0500 DST
* 오프셋 및 조건이 없는 UTC 시간 : 시간대 = 문자열: UTC -0000

이 형식을 사용하는 경우 Data Workbench 서버, Data Workbench 및 [!DNL Report] 컴퓨터는 지정된 시간대와 같을 필요가 없습니다. 또한 Data Workbench 서버 컴퓨터의 모든 활성 데이터 세트 프로필에는 동일한 시간대 설정이 필요하지 않습니다.

Adobe은 단일 data workbench 서버 컴퓨터 또는 data workbench 서버 클러스터에서 두 개 이상의 데이터 세트 프로필을 실행하지 않는 것이 좋습니다.

Data Workbench 사용자는 시스템 시간대가 아니라 데이터 집합 프로필의 시간대에 있는 데이터를 보게 됩니다. Adobe은 Data Workbench 서버 컴퓨터의 시스템 시간대가 데이터 세트에 사용되는 시간대와 동일하도록 권장합니다.

>[!NOTE]
>
>에서 시간대 매개 변수를 지정할 수 있습니다 [!DNL Log Processing.cfg] 파일. 로그 처리 중 시간 변환에 사용됩니다. 의 시간대 매개 변수에 대한 자세한 내용은 [!DNL Log Processing.cfg] 파일, [로그 처리 구성 파일](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).
