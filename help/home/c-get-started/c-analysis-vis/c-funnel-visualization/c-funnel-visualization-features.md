---
description: 단계 시각화에는 여러 차원, 원시 방문자 수, 각 단계에서 방문자 비율, 별도의 범위를 갖는 단계를 만드는 기능이 포함되어 있습니다.
title: 단계 기능
uuid: 7d2f5ff9-95d3-41f5-931c-689f140714c2
exl-id: e78dcefe-6f92-45de-9990-0beac09ad82f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 단계 기능{#funnel-features}

단계 시각화에는 여러 차원, 원시 방문자 수, 각 단계에서 방문자 비율, 별도의 범위를 갖는 단계를 만드는 기능이 포함되어 있습니다.

단계 시각화의 기본 기능은 다음과 같습니다.

![](assets/funnel_visualization_capture.png)

<table id="table_49A08740CEE74D64B6F9C37CD91F1AE5"> 
 <tbody> 
  <tr> 
   <td colname="col01"> <img id="image_0C1701833FE049708CE38ADEB5EC7EEF" src="assets/funnel_visualization_capture_1.png" /> </td> 
   <td colname="col1"> 첫 번째 요소 </td> 
   <td colname="col2"> 프로세스의 첫 번째 단계. </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img id="image_EF8AF94D833B4A249959B76F8FAF2318" src="assets/funnel_visualization_capture_2.png" /> </td> 
   <td colname="col1"> 세 번째 요소 </td> 
   <td colname="col2">프로세스의 세 번째 단계. <p><p>참고: 선택한 요소는 동일한 차원에서 가져올 필요가 없습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img id="image_F3C5130B52234FAC9DEB50279F94FF90" src="assets/funnel_visualization_capture_3.png" /> </td> 
   <td colname="col1"> 폴스루 비율 </td> 
   <td colname="col2"> 3개의 범위에 표시된 정의된 경로를 수료한 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img id="image_3F030396CEB14528980F5B965113BD36" src="assets/funnel_visualization_capture_4.png" /> </td> 
   <td colname="col1"> 폴아웃 브라우저 </td> 
   <td colname="col2">폴아웃 화살표. 마우스 오른쪽 단추를 클릭하고 <span class="uicontrol"> 경로 브라우저 추가</span>를 선택하여 다른 경로 방문자가 사용한 경로를 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img id="image_0DA7567BDBDF4BEF9CA840D2F88A414E" src="assets/funnel_visualization_capture_5.png" /> </td> 
   <td colname="col1"> 폴아웃 비율 </td> 
   <td colname="col2">경로를 완료하지 않은 사용자에 대한 폴아웃 3가지 범위를 설명하는 백분율입니다. <p>백분율은 다음 3개의 범위로 표시됩니다. </p><p><img id="image_B85C46DDF12C41D5BF213D5F9DC04967" placement="break" src="assets/funnel_path_browser_5.png" /></p><p><img id="image_BC37007D7B4B425C8F87905CE68F0114" src="assets/funnel_path_browser_6.png" /> 이 단계 이전 단계에서 이 단계까지의 폴아웃 비율입니다. </p><p><img id="image_B10866B083424360AFF1B19E836A94CF" src="assets/funnel_path_browser_7.png" /> 단계의 첫 번째 단계에서 폴아웃 비율입니다. </p><p><img id="image_19B9AE916B584E18A82F5D5E10674414" src="assets/funnel_path_browser_8.png" /> 총 방문자 수를 기반으로 하는 폴아웃 비율입니다. </p></td> 
  </tr> 
 </tbody> 
</table>

## 단계 {#section-96a6732558dd4740b73541844f06d3ef}

단계의 디스크는 탐색 단계를 나타내고, 추상체는 한 단계부터 다음 단계까지 폴스루를 나타내고, 화살표는 폴아웃을 나타냅니다. 원뿔을 클릭하면 해당 시점에 들어온 사용자를 선택하고 현재 작업 영역 필터에 포함합니다. 화살표를 클릭하면 폴아웃된 방문자가 선택됩니다.

>[!NOTE]
>
>단계 시각화에는 적용할 수 있는 8단계로 제한됩니다.

## 추가 단계 기능 및 기능 {#section-22a3582db8114ca8bce77f50bbbf296a}

* **단계의 클립 및 레벨을 조정합니다**. 시각화 메뉴에서 단계 옵션을 선택합니다. 단계를 만든 후 제목을 마우스 오른쪽 버튼으로 클릭하여 시스템의 계산 가능한 지표에 클립 및 레벨을 조정할 수 있습니다.

   ![](assets/funnel_path_browser_9.png)

* **요소를 더 드래그합니다**. `<Ctrl>` + `<Alt>` 키를 사용하여 Dimension 테이블의 요소를 깔때기로 드래그하여 놓아 과정에 더 많은 요소를 추가합니다. 여러 항목을 선택(`<Ctrl>` + 클릭 사용)한 다음 `<Ctrl>` + `<Alt>` 키를 사용하여 단계 시각화로 드래그하여 Dimension 테이블에서 동시에 여러 단계를 드래그할 수 있습니다.
* **단계 삭제**:시각화의 단계를 마우스 오른쪽 단추로 클릭하고 예를 클릭하여 요소를  **삭제합니다**.

   ![](assets/funnel_path_browser_4.png)

* **깔때기로 드래그한 단계를 다시 정렬합니다**. 단계를 클릭하여 선택하고 다른 위치로 드래그하여 단계를 재정렬하기만 하면 됩니다.
* **경로 브라우저를 엽니다**. [경로 브라우저 추가](../../../../home/c-get-started/c-analysis-vis/c-funnel-visualization/c-path-browser-funnel.md#concept-b0cedf7a28ae422696ded1258c9a4119) 기능을 통해 고객이 프로세스 중에 도달하거나 이탈하는 경우에 대한 자세한 정보를 볼 수 있습니다.

* **추가 단계**. 각 단계 시각화에 최대 8단계를 추가할 수 있습니다.
* **지표를 변경합니다**. 각 단계에서 방문 횟수 또는 일부 다른 지표를 카운트하도록 지표를 변경할 수 있습니다. 사용 가능한 옵션은 데이터 세트에 따라 다릅니다.
* **표 형식으로 표시합니다**. 제목을 마우스 오른쪽 단추로 클릭하여 단계 시각화 메뉴를 표시하고 **[!UICONTROL Show Tabular View]**&#x200B;을 클릭합니다. 테이블 형식 보기에서 **[!UICONTROL Show Graph View]**&#x200B;을 선택하여 단계의 그래픽 표현으로 돌아갈 수 있습니다. 표 형식 보기를 열려면 제목을 마우스 오른쪽 단추로 클릭하고 메뉴에서 표 형식 보기 표시를 선택합니다.

* **시퀀스** 비교 두 개의 유사한 시퀀스를 비교할 수 있는 효율적인 방법은 두 개의 시각화를 나란히 표시하는 것입니다. 복제 기능을 사용하여 표 형식 보기와 그래프 보기를 나란히 표시할 수도 있습니다. 열려면 제목을 마우스 오른쪽 단추로 클릭하고 메뉴에서 복제를 선택합니다.
