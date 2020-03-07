---
description: 입력 변수, 클러스터 수 및 타겟 모집단(원하는 경우)을 선택하여 데이터 세트에 클러스터를 정의합니다.
solution: Analytics
title: 클러스터 작성
topic: Data workbench
uuid: f8462445-b7d2-48ae-aed7-2a3abc491cfb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 클러스터 작성{#building-clusters}

입력 변수, 클러스터 수 및 타겟 모집단(원하는 경우)을 선택하여 데이터 세트에 클러스터를 정의합니다.

**클러스터 작성**

1.  **[!UICONTROL Cluster Builder]**.

   예측 **분석** > **클러스터링** > **클러스터** 빌더 **시각화를**&#x200B;클릭합니다.

   ![](assets/cluster-builder-step1.png)

1. 입력 변수를 선택합니다.

   * 도구 모음의 **[!UICONTROL Input Variables]** **[!UICONTROL Metric]** 메뉴에서 선택하여 목록에 지표를 추가합니다.

      ![](assets/cluster_metric_select.png)

   * 차원 테이블에서 차원 요소를 드래그하여 **[!UICONTROL Input Variables]** 목록에 추가합니다.

      선택한 차원 요소를 **[!UICONTROL Ctrl + Alt]** 눌러 **[!UICONTROL Input Variables]** 목록 또는 도구 모음의 **[!UICONTROL Element]** 상자로 드래그합니다.

      ![](assets/cluster_dim_select.png)
   기본적으로 클러스터링은 전체 데이터 세트에 대해 수행됩니다. 왼쪽 **[!UICONTROL Preprocessing]** 창에 모든 입력 변수가 표시됩니다.
1. 메뉴를 사용하여 원하는 클러스터 수를 선택합니다. **[!UICONTROL Options]**

   ![](assets/build_cluster_2.png)

1. 데이터 세트에 방문자의 하위 집합을 클러스터하려면 모집단 필터를 정의할 수 있습니다.

   ![](assets/build_cluster_3.png)

   먼저 작업공간에서 선택한 항목을 사용하거나 를 사용하여 원하는 하위 세트를 정의합니다 **[!UICONTROL Filter Editor]**. 원하는 하위 집합을 선택한 후에는 **[!UICONTROL Options]** 메뉴에서 타겟 모집단 을 설정합니다. 타깃팅된 그룹에 식별 이름을 지정하는 것이 좋습니다.

   또한 **[!UICONTROL Options]** 메뉴에는 최대 패스 수와 중앙 컨버전스에 대해 허용 가능한 임계값을 제어하는 설정이 있습니다.

1. 입력 및 옵션이 구성된 후 **이동** 단추를 클릭하여 클러스터링을 로컬로 실행하거나 을 눌러 **[!UICONTROL Submit]** 예측 분석 서버로 작업을보냅니다. 서버에 제출하면 수렴이 완료되면 결과 차원이 데이터 세트에 저장됩니다.

   로컬로 실행할 때 클러스터 빌더가 입력을 기반으로 지능형 센터를 정의함에 따라 4개의 캐노피 클러스터링 단계를 거치는 것을 볼 수 있습니다.

   클러스터 중심이 지정된 수렴 임계값보다 더 이상 변경되지 않으면 클러스터 차원이 수렴되고 클러스터 빌더가 각 클러스터에 대한 입력과 관련된 추가 정보를 표시합니다.

1. 클러스터를 사용자 정의합니다.

   통계 색상 막대를 마우스 오른쪽 단추로 클릭하면 관련 임계값을 사용자 정의할 수 있는 컨텍스트 메뉴가 열리고, 차원 요소 분배의 경우 표시되는 테스트를 선택할 수 있습니다.

   ![](assets/build_cluster_7.png)

   지표 입력은 각 클러스터에 대해 t-test를 제공하는 반면 차원 요소 입력은 각 클러스터에 대해 세 가지 배포 테스트(Chi 제곱, 엔트로피 U 통계 및 Cramer의 V 통계)를 제공합니다.

   >[!NOTE]
   >
   >수렴하는 동안 입력을 추가하거나 제거하면 다시 이동을 누를 때까지 프로세스가 일시 **중지됩니다** .

   클러스터를 빌드한 후 색상 피커를 열어 다양한 배포 결과에 대한 색상을 할당할 수 있습니다.

   ![](assets/build_cluster_5.png)

1. 클러스터 차원이 수렴되면 표에 지표를 추가하고 정상으로 선택할 수 있습니다. 요소 이름(클러스터 1, 클러스터 2 등)을 마우스 오른쪽 단추로 클릭하여 컨텍스트 메뉴를 열어 보다 의미 있는 이름으로 변경할 수도 있습니다.

   ![](assets/build_cluster_6.png)

1. 다른 시각화에서 이 클러스터 차원을 사용하려면 로컬이나 서버에 **[!UICONTROL Save]** 저장할 수 **[!UICONTROL Submit]** 있습니다.

수렴을 다시 실행하거나 입력의 연관성을 확인하려면 Cluster Builder에서 기존 클러스터 차원을 로드할 수도 있습니다.

>[!TIP]
>
>이 옵션을 선택하면 모든 입력 변수가 완전히 **[!UICONTROL Reset]** 해제되며 새 클러스터를 정의하는 빈 클러스터 빌더 시각화를 제공합니다.

