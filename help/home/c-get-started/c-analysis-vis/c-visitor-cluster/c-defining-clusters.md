---
description: 입력 변수, 클러스터 수 및 대상 모집단(원하는 경우)을 선택하여 데이터 집합에 클러스터를 정의합니다.
title: 클러스터 구축
uuid: f8462445-b7d2-48ae-aed7-2a3abc491cfb
exl-id: 60bc75bf-2f89-455b-8be9-aa20bb837752
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---

# 클러스터 구축{#building-clusters}

{{eol}}

입력 변수, 클러스터 수 및 대상 모집단(원하는 경우)을 선택하여 데이터 집합에 클러스터를 정의합니다.

**클러스터 구축**

1.  **[!UICONTROL Cluster Builder]**.

   클릭 **시각화** > **Predictive Analytics** > **클러스터링** > **클러스터 빌더**.

   ![](assets/cluster-builder-step1.png)

1. 입력 변수를 선택합니다.

   * 에 지표 추가 **[!UICONTROL Input Variables]** 목록에서 을(를) 선택하여 나열합니다. **[!UICONTROL Metric]** 메뉴 아래의 제품에서 사용할 수 있습니다.

      ![](assets/cluster_metric_select.png)

   * 에 차원 요소 추가 **[!UICONTROL Input Variables]** Dimension 테이블에서 드래그하여 나열합니다.

      누르기 **[!UICONTROL Ctrl + Alt]** 선택한 차원 요소를 드래그하여 **[!UICONTROL Input Variables]** 또는 **[!UICONTROL Element]** 상자에 표시되지 않습니다.

      ![](assets/cluster_dim_select.png)
   기본적으로 클러스터링은 전체 데이터 세트에서 수행됩니다. 왼쪽에 모든 입력 변수가 표시됩니다 **[!UICONTROL Preprocessing]** 창
1. 를 사용하십시오 **[!UICONTROL Options]** 원하는 클러스터 수를 선택할 수 있습니다.

   ![](assets/build_cluster_2.png)

1. 데이터 집합에 있는 방문자 하위 집합을 클러스터링하려는 경우 모집단 필터를 정의할 수 있습니다.

   ![](assets/build_cluster_3.png)

   먼저 Workspace에서 선택 사항을 사용하거나 **[!UICONTROL Filter Editor]**. 원하는 하위 집합을 선택하면 **[!UICONTROL Options]** 메뉴 아래의 제품에서 사용할 수 있습니다. 타깃팅된 그룹에 식별 이름을 지정하는 것이 좋습니다.

   다음 **[!UICONTROL Options]** 또한 메뉴에는 최대 가공 패스 수 및 센터 컨버전스의 허용 가능한 임계값을 제어하는 설정이 있습니다.

1. 입력 및 옵션이 구성된 후 **이동** 로컬로 클러스터링을 실행하거나 키를 누릅니다. **[!UICONTROL Submit]** 을 눌러 Predictive Analytics 서버로 작업을 보냅니다. 서버에 제출하면 수렴이 완료되면 결과 차원이 데이터 세트에 저장됩니다.

   로컬에서 실행할 때 입력을 기반으로 지능형 센터를 정의하면 클러스터 빌더가 4개의 캐노피 클러스터링 단계를 이동하는 것을 볼 수 있습니다.

   클러스터 중심이 지정된 융합 임계값 이상의 변경을 중지하면 클러스터 Dimension이 수렴되고 클러스터 빌더에 각 클러스터에 대한 입력이 어떻게 관련되었는지에 대한 추가 정보가 표시됩니다.

1. 클러스터를 사용자 정의합니다.

   통계 색상 막대를 마우스 오른쪽 단추로 클릭하면 관련성 임계값을 사용자 정의할 수 있는 컨텍스트 메뉴가 열리고 차원 요소 배포의 경우 표시되는 테스트를 선택할 수 있습니다.

   ![](assets/build_cluster_7.png)

   지표 입력은 각 클러스터에 대한 t-test를 제공하는 반면 차원 요소 입력은 각 클러스터에 대해 세 가지 배포 테스트(카이 제곱, 엔트로피 U 통계 및 Cramer의 V 통계)를 제공합니다.

   >[!NOTE]
   >
   >융합 중에 입력을 추가하거나 제거하면 사용자가 키를 누를 때까지 프로세스가 일시 중지됩니다 **이동** 다시 한 번

   클러스터를 작성한 후 색상 선택기를 열어 다른 배포 결과에 대한 색상을 할당할 수 있습니다.

   ![](assets/build_cluster_5.png)

1. 클러스터 Dimension이 수렴되면 테이블에 지표를 추가하고 정상적으로 선택할 수 있습니다. 요소 이름(클러스터 1, 클러스터 2 등)을 마우스 오른쪽 단추로 클릭하여 컨텍스트 메뉴를 열어 의미 있는 이름으로 바꿀 수도 있습니다.

   ![](assets/build_cluster_6.png)

1. 이 클러스터 차원을 다른 시각화에서 사용하려면 다음을 수행할 수 있습니다 **[!UICONTROL Save]** 로컬에서 또는 **[!UICONTROL Submit]** 서버에 전달됩니다.

컨버전스를 다시 실행하거나 입력의 관련성을 확인하려는 경우 Cluster Builder가 기존 클러스터 차원을 로드할 수도 있습니다.

>[!TIP]
>
>선택한 경우, **[!UICONTROL Reset]** 은(는) 모든 입력 변수를 완전히 해제하고 새 클러스터를 정의하기 위해 빈 클러스터 빌더 시각화를 제공합니다.
