---
description: 막대 그래프, 표 및 계층 보기의 요소를 빈 맵으로 드래그하여 놓아 2D 및 3D 프로세스 맵을 만들 수 있습니다.
solution: Analytics
title: 프로세스 맵 만들기
topic: Data workbench
uuid: dbcde637-0411-4296-99ca-5510e0285e4b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 프로세스 맵 만들기{#create-a-process-map}

막대 그래프, 표 및 계층 보기의 요소를 빈 맵으로 드래그하여 놓아 2D 및 3D 프로세스 맵을 만들 수 있습니다.

추가할 수 있는 요소는 프로세스 맵의 기본 차원의 요소여야 합니다. 맵이 동일한 기본 차원을 사용하는 한 프로세스 맵에서 다른 프로세스 맵으로 노드를 드래그하여 놓을 수도 있습니다. 또한 전체 맵을 확대/축소하거나 이동하여 특정 노드에 초점을 맞추거나 다른 시각화 유형으로 변경할 수 있습니다. 시각화 [확대/축소를 참조하십시오](../../../../home/c-get-started/c-vis/c-zoom-vis.md#concept-7e33670bb5344f78a316f1a84cc20530).

**표 또는 막대 그래프를 사용하여 프로세스 맵에 요소를 추가하려면**

* 프로세스 맵과 동일한 기본 차원이 있는 표 또는 막대 그래프에서 Ctrl+Alt를 누른 상태에서 개별 요소를 클릭하고 프로세스 맵으로 드래그합니다. 마우스 커서에 &quot;아니요&quot;라는 단어가 프로세스 맵에 도달할 때까지 표시됩니다.

   >[!NOTE]
   >
   >추가할 수 있는 요소는 프로세스 맵의 기본 차원의 요소여야 합니다.

   ![](assets/vis_2DProcessMap_addPages.png)

**계층 보기를 사용하여 프로세스 맵에 요소를 추가하려면**

>[!NOTE]
>
>분석 중인 계층의 최상위 수준에서 노드를 추가하는 것이 좋습니다.

1. 프로세스 맵과 동일한 기본 차원이 있는 테이블 또는 막대 그래프에서 요소 또는 기본 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Hierarchy View]**&#x200B;클릭합니다.
1. 요소를 클릭하고 프로세스 맵으로 드래그하는 동안 Ctrl+Alt를 누릅니다. 마우스가 맵에 도달할 때까지 마우스 커서에 &quot;아니요&quot;라는 단어가 표시됩니다.

   >[!NOTE]
   >
   >추가할 수 있는 요소는 프로세스 맵의 기본 차원의 요소여야 합니다.

   단일 요소를 프로세스 맵으로 드래그하면 해당 요소에 대해서만 맵 노드가 만들어지지만, 여러 요소(그룹)나 여러 요소가 들어 있는 폴더를 선택하면 계층에서 드래그하면 해당 그룹이나 폴더에 대한 단일 노드가 만들어집니다. 예를 들어 웹 사이트 데이터를 사용하여 작업하는 경우 이름이 지정된 폴더를 [!DNL site.com/cgi-bin] 맵으로 드래그하면 해당 폴더의 하위 폴더인 모든 페이지 및 디렉토리를 나타내는 [!DNL site.com/cgi-bin/*]노드가 만들어집니다.

페이지 계층 보기에 대한 자세한 내용은 계층 보기 [적용을 참조하십시오](../../../../home/c-get-started/c-analysis-vis/c-tables/c-hier-vews.md#concept-b461183424a841eb94f8143a0eaf9bff).

**다른 프로세스 맵에서 프로세스 맵에 노드를 추가하려면**

>[!NOTE]
>
>프로세스 맵에는 동일한 기본 차원이 있어야 합니다.

* 다음 방법을 사용하여 첫 번째 프로세스맵에서 두 번째 프로세스 맵으로 노드를 복사합니다.

   * 개별 노드를 복사하려면 각 노드를 클릭하여 두 번째 프로세스 맵으로 드래그합니다.
   * 여러 노드를 복사하려면 Ctrl 키를 누른 채 드래그하여 복사할 노드 주위에 상자를 만든 다음 강조 표시된 노드를 클릭하여 두 번째 프로세스 맵으로 드래그합니다. 강조 표시된 모든 노드가 두 번째 프로세스 맵에 복사됩니다.
