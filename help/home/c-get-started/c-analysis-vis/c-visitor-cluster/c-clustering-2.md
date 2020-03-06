---
description: 이제 클러스터 빌더에는 신속 클러스터 생성 프로세스를 위한 센터를 찾는 데 보다 빠른 방법을 사용하는 KMeans++ 알고리즘(KMeans 알고리즘만 이전에 지원됨)이 포함되어 있습니다.
title: 클러스터링 2.0
uuid: 14462bd3-06d1-4622-a2d8-f96aadb357f3
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# 클러스터링 2.0{#clustering}

이제 클러스터 빌더에는 신속 클러스터 생성 프로세스를 위한 센터를 찾는 데 보다 빠른 방법을 사용하는 KMeans++ 알고리즘(KMeans 알고리즘만 이전에 지원됨)이 포함되어 있습니다.

## KMeans 알고리즘 {#section-92383a1be1d6402c95a25c902e90b850}

이제 [클러스터 빌더에서](https://docs.adobe.com/help/en/data-workbench/using/client/analysis-visualizations/visitor-cluster/c-visitor-cluster.html)클러스터를 정의할 때 **[!UICONTROL Options]** > 을 선택하여 알고리즘을 선택할 **[!UICONTROL Algorithm]** 수 있습니다.

* **[!UICONTROL KMeans]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 알고리즘은 캐노피 클러스터링을 사용하여 클러스터의 중심을 정의합니다.
* **[!UICONTROL KMeans++]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 알고리즘은 대규모 데이터 세트에 대해 실행할 때 클러스터 빌드를 촉진합니다.

<!-- <a id="section_8193A6D60C5540BB985085BE670B4544"></a> -->

KMeans++는 초기 k 센터를 더 잘 초기화하기 때문에 향상된 KMeans 클러스터링 알고리즘 구현입니다. (원래 KMeans 알고리즘은 초기 센터를 임의로 선택합니다.) KMeans++는 첫 번째 중심을 무작위로 선택합니다. 나머지 초중고 센터는 데이터 포인트가 가장 가까운 기존 센터와의 거리를 기준으로 한 곳을 기준으로 한 곳을 선택합니다. 가장 멀리 있는 데이터 포인트는 가까운 데이터 포인트보다 새로운 센터로 선택할 가능성이 더 높습니다. 초기 중심을 선택한 후 절차는 원래 KMeans 클러스터링과 정확하게 동일하게 수행됩니다.

KMeans++의 워크플로우는 클러스터 빌더에서 옵션 > 알고리즘 **>** KMeans **++** 를 선택해야 한다는 점을 제외하면 KMeans **클러스터링을 위한 워크플로우와 정확하게 동일합니다** .

>[!NOTE]
>
>각 DPU 파섹 DPU에 사용 가능한 메모리가 충분하면(비율이 PAServer.cfg 파일에서 구성 가능) 관련 변수의 데이터가 메모리에 추가됩니다. 나머지 k-1 초기 가운데 선택 및 변환 반복은 모두 메모리에서 발생하며, 이는 이전 KMeans 클러스터링보다 빠릅니다.

