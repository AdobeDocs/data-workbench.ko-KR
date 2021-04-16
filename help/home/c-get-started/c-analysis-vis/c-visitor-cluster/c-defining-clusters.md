---
description: 입력 변수, 클러스터 수 및 타겟 모집단(원하는 경우)을 선택하여 데이터 세트에 클러스터를 정의합니다.
title: 클러스터 구축
uuid: f8462445-b7d2-48ae-aed7-2a3abc491cfb
exl-id: 60bc75bf-2f89-455b-8be9-aa20bb837752
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---

# 클러스터 구축{#building-clusters}

입력 변수, 클러스터 수 및 타겟 모집단(원하는 경우)을 선택하여 데이터 세트에 클러스터를 정의합니다.

**클러스터 구축**

1.  **[!UICONTROL Cluster Builder]**.

   **시각화** > **예측 분석** > **클러스터링** > **클러스터 빌더**&#x200B;를 클릭합니다.

   ![](assets/cluster-builder-step1.png)

1. 입력 변수를 선택합니다.

   * 도구 모음의 **[!UICONTROL Metric]** 메뉴에서 선택하여 **[!UICONTROL Input Variables]** 목록에 지표를 추가합니다.

      ![](assets/cluster_metric_select.png)

   * Dimension 테이블에서 차원 요소를 드래그하여 **[!UICONTROL Input Variables]** 목록에 추가합니다.

      **[!UICONTROL Ctrl + Alt]**&#x200B;을 누르고 선택한 차원 요소를 **[!UICONTROL Input Variables]** 목록 또는 도구 모음의 **[!UICONTROL Element]** 상자로 드래그합니다.

      ![](assets/cluster_dim_select.png)
   기본적으로 클러스터링은 전체 데이터 세트에 대해 수행됩니다. 왼쪽 **[!UICONTROL Preprocessing]** 창에 모든 입력 변수가 표시됩니다.
1. 원하는 수의 클러스터를 선택하려면 **[!UICONTROL Options]** 메뉴를 사용합니다.

   ![](assets/build_cluster_2.png)

1. 데이터 세트에 방문자의 하위 집합을 클러스터링하려면 모집단 필터를 정의할 수 있습니다.

   ![](assets/build_cluster_3.png)

   먼저 작업공간에서 선택한 항목을 사용하거나 **[!UICONTROL Filter Editor]**&#x200B;을 사용하여 원하는 하위 세트를 정의합니다. 원하는 하위 집합을 선택한 후에는 **[!UICONTROL Options]** 메뉴에서 Target 채우기를 설정합니다. 타깃팅된 그룹에 식별 이름을 지정하는 것이 좋습니다.

   또한 **[!UICONTROL Options]** 메뉴에는 최대 패스 수 및 중앙 컨버전스의 허용 가능한 임계값을 제어하는 설정도 있습니다.

1. 입력과 옵션이 구성된 후 **이동** 단추를 클릭하여 클러스터링을 로컬로 실행하거나 **[!UICONTROL Submit]**&#x200B;를 눌러 작업을 예측 분석 서버로 보냅니다. 컨버전스가 완료되면 서버에 제출하면 결과 차원이 데이터 세트에 저장됩니다.

   로컬에서 실행할 때 입력에 따라 지능형 센터를 정의하면 클러스터 빌더가 4개의 캐노피 클러스터링 단계를 통해 이동하는 것을 볼 수 있습니다.

   클러스터 중심이 지정된 컨버전스 임계값보다 더 많은 변경을 중지하면 클러스터 Dimension이 통합하고 클러스터 빌더에서 각 클러스터에 대한 입력과 관련된 추가 정보를 표시합니다.

1. 클러스터를 사용자 정의합니다.

   통계 색상 막대를 마우스 오른쪽 단추로 클릭하면 관련 임계값을 사용자 정의할 수 있는 컨텍스트 메뉴가 열리고 차원 요소 분포의 경우 표시되는 테스트를 선택할 수 있습니다.

   ![](assets/build_cluster_7.png)

   지표 입력은 각 클러스터에 대한 t-test를 제공하는 반면 차원 요소 입력은 각 클러스터에 대한 세 가지 배포 테스트(Chi 제곱, 엔트로피 U 통계 및 Cramer의 V 통계)를 제공합니다.

   >[!NOTE]
   >
   >수렴하는 동안 입력을 추가하거나 제거하면 **Go**&#x200B;을 다시 누를 때까지 프로세스가 일시 중지됩니다.

   클러스터를 빌드한 후 색상 피커를 열어 다양한 배포 결과에 대한 색상을 할당할 수 있습니다.

   ![](assets/build_cluster_5.png)

1. 클러스터 Dimension이 통합되면 표에 지표를 추가하고 정상으로 선택할 수 있습니다. 요소 이름(클러스터 1, 클러스터 2 등)을 마우스 오른쪽 단추로 클릭하여 컨텍스트 메뉴를 열어 보다 의미 있는 이름으로 바꿀 수도 있습니다.

   ![](assets/build_cluster_6.png)

1. 다른 시각화에 이 클러스터 차원을 사용하려면 로컬에서 **[!UICONTROL Save]** 사용하거나 서버에 **[!UICONTROL Submit]** 저장할 수 있습니다.

컨버전스를 다시 실행하거나 입력의 연관성을 확인하려면 Cluster Builder에서 기존 클러스터 차원을 로드할 수도 있습니다.

>[!TIP]
>
>이 옵션을 선택하면 **[!UICONTROL Reset]**&#x200B;은 모든 입력 변수를 완전히 해제하고 새 클러스터를 정의하는 빈 클러스터 빌더 시각화를 제공합니다.
