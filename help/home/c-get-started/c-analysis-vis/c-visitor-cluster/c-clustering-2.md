---
description: 이제 클러스터 빌더에는 신속 클러스터 생성 프로세스를 위해 센터를 찾는 더 빠른 접근 방식을 사용하는 KMeans++ 알고리즘(이전에 KMeans 알고리즘만 지원됨)이 포함되어 있습니다.
title: 클러스터링 2.0
uuid: 14462bd3-06d1-4622-a2d8-f96aadb357f3
exl-id: 6a779ddc-c8f1-4c55-9c17-1119fe1aa791
source-git-commit: 050468bf6a9ef9c07719ded79c8ab68753d58647
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# 클러스터링 2.0{#clustering}

이제 클러스터 빌더에는 신속 클러스터 생성 프로세스를 위해 센터를 찾는 더 빠른 접근 방식을 사용하는 KMeans++ 알고리즘(이전에 KMeans 알고리즘만 지원됨)이 포함되어 있습니다.

## KMeans 알고리즘 {#section-92383a1be1d6402c95a25c902e90b850}

이제 [클러스터 빌더](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/visitor-cluster/c-visitor-cluster.html?lang=en)에서 **[!UICONTROL Options]** > **[!UICONTROL Algorithm]**&#x200B;를 선택하여 클러스터를 정의할 때 알고리즘을 선택할 수 있습니다.

* **[!UICONTROL KMeans]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 알고리즘에서는 캐노피 클러스터링을 사용하여 클러스터의 중심을 정의합니다.
* **[!UICONTROL KMeans++]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 알고리즘은 대규모 데이터 세트에 대해 실행할 때 클러스터 빌드를 촉진합니다.

<!-- <a id="section_8193A6D60C5540BB985085BE670B4544"></a> -->

KMeans++는 초기 kCenter의 더 나은 초기화를 제공하기 때문에 KMeans 클러스터링 알고리즘의 구현이 개선되었습니다. (원래 KMeans 알고리즘은 초기 센터를 임의로 선택합니다.) KMeans++ 첫 번째 중심을 임의로 선택합니다. 나머지 k-1 센터는 데이터 포인트가 가장 가까운 기존 센터까지의 거리에 따라 하나씩 선택됩니다. 가장 멀리 있는 데이터 포인트는 가까운 데이터 포인트보다 새로운 센터로 선택할 가능성이 더 높습니다. 초기 중심이 선택된 후, 절차는 원래 KMeans 클러스터링과 정확히 동일하게 수행됩니다.

KMeans++용 워크플로우는 클러스터 빌더에서 **옵션** > **알고리즘** > **KMeans++**&#x200B;을 선택해야 한다는 점을 제외하면 KMeans클러스터링을 위한 워크플로우와 정확히 동일합니다.

>[!NOTE]
>
>각 DPU는 자체 데이터 부분에서 고유한 KMeans++ 프로시저를 실행합니다. DPU에 사용 가능한 메모리가 충분하면(PAServer.cfg 파일에서 비율이 구성 가능) 관련 변수의 데이터가 메모리에 생성됩니다. 나머지 k-1 초기 중심 선택 및 변환 반복은 모두 이전 KMeans 클러스터링보다 빠른 메모리에서 발생합니다.
