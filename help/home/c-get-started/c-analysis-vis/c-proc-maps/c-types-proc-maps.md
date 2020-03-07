---
description: 다양한 유형의 프로세스 맵에 대한 정보입니다.
solution: Analytics
title: 프로세스 맵 유형
topic: Data workbench
uuid: 19473b77-13c1-4829-b018-d3316e434ba4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 프로세스 맵 유형{#types-of-process-maps}

다양한 유형의 프로세스 맵에 대한 정보입니다.

## 2D 프로세스 맵 {#section-ea7fbdb80b1b44aebcd9e4090b6540bf}

2차원 프로세스 맵은 차원 요소 간의 활동에 대한 2차원 보기를 제공합니다. 2D 프로세스 맵의 노드 크기는 해당 노드와 연관된 지표 값에 비례합니다. 또한 두 노드 사이의 화살표 두께와 강도 모두 해당 노드에 대한 지표 값의 평균에 비례합니다.

2D 프로세스 맵 내에서 다음 작업 중 하나를 수행할 수 있습니다.

* 노드 선택, 이동, 제거 및 레이블 지정
* 선택
* 차원 저장
* 다른 시각화 만들기
* 색상 링크 활성화
* 지표 수량 표시
* 설명선 추가

다음 예제의 2D 프로세스 맵은 동영상의 이름에 해당하는 노드를 보여줍니다. 각 동영상 이름은 동영상 차원의 요소로, 동영상 데이터로 구성된 데이터 세트에 정의됩니다. 동영상 차원은 이 프로세스 맵의 기본 차원입니다.

![](assets/vis_2DProcessMap_MovieNodes.png)

이 예에서 각 노드의 크기와 각 화살표의 두께 및 강도는 동영상이 받은 등급 수 지표와 비례합니다. 따라서 독립기념일과 같은 큰 노드를 갖는 *영화는*&#x200B;이벤트 수평선과 같은 작은 노드를 갖는 영화보다 높은 평가를 *받습니다*. 또한 더 많은 영화 시청자들이 콜드마운틴보다 *독립기념일을* 더 높게 ** 보는 것을 볼 수 있다. 이 화살표는 시청자가 독립기념일을 등급을 매긴 *다음* Cold Mountain 등급을 *매기거나 그 반대로* 평가할 수 없음을 나타냅니다. 시청자가 다른 영화를 그 중간에 봤을지 모르지만, 이 영화는 이 지도에서 보이지 않는다.

## 2D 지표 맵 {#section-a9b846fc71224058918fbc378315effe}

2차원 지표 맵은 특정 지표의 값을 기준으로 노드를 배치하는 2D 프로세스 맵 유형입니다. 대부분의 경우 2D 지표 맵에 사용된 지표는 전환 또는 유지입니다. 전환 및 유지 맵은 고객이 접하는 채널의 프로세스에서 고객 전환율과 유지율에 영향을 미치는 단계를 파악하는 데 도움이 됩니다.

>[!NOTE]
>
>2D 지표 맵에 사용하는 지표는 백분율로 표시되어야 합니다.

전환 지표 맵에서 0%의 전환이 있는 노드는 그래프 왼쪽에 표시되며, 100% 전환이 있는 페이지는 오른쪽에 표시됩니다. 노드 간 활동이 표시되므로 프로세스 중 전환을 증가 또는 감소시키고 포기를 유도하는 단계를 쉽게 확인할 수 있습니다. 프로세스 전환 분석은 프로세스를 비교하거나 동일한 프로세스의 다른 구현을 비교하는 효과적인 방법입니다.

![](assets/vis_2DMetricMap_Conversion.png)

마찬가지로, 보존 맵은 그래프 왼쪽에 0%의 유지율을 가진 요소와 오른쪽에 100%의 유지율을 가진 요소를 보여줍니다. 맵에서 각 노드에 대한 유지율을 볼 수 있으므로 고객이 반환에 영향을 미치는 요소를 결정할 수 있습니다.

![](assets/vis_2DMetricMap_Retention.png)

>[!NOTE]
>
>2D 지표 맵의 노드를 가로로 이동할 수 없습니다. 지표 맵은 지표 값을 기준으로 노드를 왼쪽에서 오른쪽으로 배치하도록 디자인되었습니다.

## 3D 프로세스 맵 {#section-80acb63ea0994af1af7faef3c6264e51}

3차원 프로세스 맵은 차원 요소 간의 활동에 대한 3차원 보기를 제공합니다. 3D 프로세스 맵에서 막대의 높이는 해당 노드와 연관된 지표의 값에 비례합니다. 2D 프로세스 맵과 마찬가지로 두 노드 사이의 커넥터의 두께와 강도 모두 해당 노드에 대한 지표 값의 평균과 비례합니다. 3D 프로세스 맵 내에서 다음 작업 중 하나를 수행할 수 있습니다.

* 노드 선택, 이동, 제거 및 레이블 지정
* 선택
* 차원 저장
* 다른 시각화 만들기
* 색상 링크 활성화

다음 예제의 3D 프로세스 맵은 웹 사이트의 페이지에 해당하는 노드를 보여줍니다. 각 페이지는 페이지 차원의 요소로, 웹 트래픽 데이터로 구성된 데이터 세트에 정의됩니다. 페이지 차원은 이 프로세스 맵의 기본 차원입니다.

![](assets/vis_3DProcessMap_PageNodes.png)

이 예에서 각 막대의 높이와 각 커넥터의 두께 및 강도는 페이지를 본 세션 수 지표인 세션 수에 비례합니다. 따라서 /faq/all/FAQ와 같은 긴 막대가 있는 페이지는 /vs/demo와 같은 짧은 막대가 있는 페이지보다 많은 세션 동안 볼 수 있었습니다. 두 페이지 간의 연결에는 특정 페이지가 지정된 세션 중에 다른 페이지 바로 앞 또는 뒤에 표시되었음을 의미하지 않습니다. 다른 페이지는 동일한 세션 동안 표시되었을 수 있지만 이 페이지에는 표시되지 않습니다.