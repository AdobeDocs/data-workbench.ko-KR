---
description: 프리미엄 메뉴에서 최적 속성을 열고 다음 단계에 따라 최적 속성 모델을 작성합니다.
title: 최적 속성 모델 작성
uuid: d1fd0340-1917-41bc-9a08-e78a79d084e7
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# 최적 속성 모델 작성{#build-a-best-fit-attribution-model}

프리미엄 메뉴에서 최적 속성을 열고 다음 단계에 따라 최적 속성 모델을 작성합니다.

최적 속성에 대한 개요를 [참조하십시오](../../../../home/c-get-started/c-attribution-profiles/c-attrib-algorithmic/c-attrib-algorithmic.md#concept-237feb6e9c4d49efaf75399297dcb9d1).

1. 최적 **속성을 엽니다**.

   작업 영역을 열고 **[!UICONTROL Premium]** > **[!UICONTROL Best Fit Attribution]**&#x200B;을 클릭합니다.

   ![](assets/attrib_windows_launch.png)

   >[!NOTE]
   >
   >Best Fit Attribution은 Adobe Analytics Premium 기능으로서, 프로필에서 Premium을 활성화해야 합니다. 인증서를 업데이트하고 Premium 프로필을 profile.cfg 파일에 추가해야 합니다. DWB [Server 업그레이드 참조:DWB 6.3의](https://docs.adobe.com/content/help/en/data-workbench/using/install/upgrade-dwb/c-6-2-to-6-3-upgrade.html) 경우 6.2 ~ 6.3.

1. 지표를 **[!UICONTROL Success]** 설정합니다.

   >[!NOTE]
   >
   >표의 지표를 기여도 시각화의 왼쪽 창으로 끌거나 입력 메뉴에서 선택할 수 **[!UICONTROL Finder]** 있습니다 **** .

   클릭 **[!UICONTROL Inputs]** > **[!UICONTROL Set Success]**. 지표 메뉴가 열립니다. ![](assets/attrib_set_success_metric.png)

   성공적인 전환을 식별하는 지표를 선택합니다.

1. (선택 사항) 매출 **지표를** 설정합니다.

   전환 프로세스 전체에서 매출을 평가하도록 지표를 설정합니다.

1. 터치 **지표를** 설정합니다.

   >[!NOTE]
   >
   >터치 지표 설정은 차원 요소를 시각화로 드래그하여 성공 지표를 자동으로 빌드하려는 경우에만 필요합니다.

   메뉴를 클릭하고 **[!UICONTROL Inputs]** 터치 설정을 ****&#x200B;선택하거나 Finder에서 지표를 드래그합니다. ![](assets/attrib_set_touch.png)

   차원 요소를 입력으로 사용할 때 채널 지표를 추출하는 데 사용됩니다.

1. 성공 **창을** 설정합니다.

   클릭 [!DNL Inputs > Success Window]. 테이블에서 날짜 범위를 선택한 다음 성공 창의 이름을 지정합니다. 을 **[!UICONTROL Workspace Selection]** 클릭하면 선택한 날짜가 성공 지표의 시간 범위로 지정됩니다.

   ![](assets/attrib_set_success_window.png)

   >[!NOTE]
   >
   >성공 창은 워크스테이션 선택이므로 성공 창에 차원을 포함할 수 있습니다.

1. 설정을 **[!UICONTROL Touch Window]**&#x200B;참조하십시오.

   클릭 [!DNL Inputs > Touch Window]. 표에서 날짜 범위를 선택한 다음 터치 창의 이름을 지정합니다. 을 **[!UICONTROL Workspace Selection]** 클릭하면 선택한 날짜가 성공 지표의 시간 범위로 지정됩니다.

   ![](assets/attrib_set_touch_window.png)

   기본적으로 **터치** 창은 **[!UICONTROL Success]** 창과 동일한 시간으로 설정됩니다.

1. (선택 사항) 교육 필터를 설정합니다.

   또한 작업 영역에서 **교육 필터를** 지정하여 방문자 데이터를 필터링할 수도 있습니다.

   >[!NOTE]
   >
   >[성공] 창과 [터치] 창을 둘 다 설정할 때 현재 작업 영역 선택 영역에 교육 필터를 적용하여 데이터를 추가로 제한할 수 있습니다.

   ![](assets/attrib_filter.png)

   >[!NOTE]
   >
   >교육 세트는 항상 성공 창을 만족하는 방문자로부터 그려집니다. 필터 편집기를 사용하여 필터링하면 성공 창에서 보고된 방문자 하위 집합을 만들 수 있습니다.

1. 터치를 나타내는 채널 지표를 지정합니다.

   지표를 시각화로 드래그하거나 [!DNL Inputs] > [!DNL Add Channel] 메뉴에서 선택합니다. 캠페인 또는 채널에 대해 정의된 지표가 없지만 채널을 나타내는 차원이 있는 경우, 시각화는 터치 지표의 사양으로 자동으로 만들 수 있습니다.

   예를 들어, 터치 지표를 로 설정하고, [!DNL Hits], [!DNL dimension] , [!DNL Media Type] 및 [!DNL Email]같은 요소를 포함하는 요소가 있는 [!DNL Press Release][!DNL Print Ad][!DNL Social Media][!DNL Hits where Media Type = Email] 호출된 경우, 시각화에서는 요소를 시각화에 드래그하여 놓을 때 양식의 채널 지표를 생성합니다.

1. Go **를 누릅니다**.

   최적 분석 프로세스가 실행되며 선택한 입력을 기반으로 채널별 기여도가 차트에 표시됩니다.

   >[!NOTE]
   >
   >완료된 **분석에서 모델** 완료를 마우스 오른쪽 단추로 클릭하여 속성 모델에 대한 통계를 봅니다.

   ![](assets/attrib_visualization.png)

완료되면, 그래프는 채널별로 계산된 속성 모델과 매출액 *지표의 배포(설정된 경우* )를 표시합니다. 모델을 내부적으로 저장하거나 다른 시스템으로 내보낼 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Streaming]**, **[!UICONTROL Online]** and **[!UICONTROL Offline]** modes produce different effects when building a attribution model based on the latency of the data 평가 중인 데이터의 지연 시간을 기반으로 하여 속성 모델을 작성할 때. 스트리밍 모드에서 세부 정보 **[!UICONTROL Model Complete]** 메시지가 표시됩니다. 온라인 및 오프라인 모드에서는 세부 사항이 **[!UICONTROL Local Model Complete]** 표시됩니다.

## 옵션 메뉴 {#section-22288867f6c8483a8a38410f4b948346}

옵션 **메뉴에서는** 최적 속성 분석을 설정하고 표시하는 고급 기능을 제공합니다.

<table id="table_8F6F517B7DBF4259814BEC6D07A72EAC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 옵션 메뉴 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><span class="uicontrol"> 교육 필터 설정 </span> </td> 
   <td colname="col2"> 교육 필터는 속성 모델을 작성할 때 모집단 필터링을 위해 성공 창과 함께 사용됩니다. 분석하려는 방문자만 포함하는 데이터 하위 세트가 제공됩니다. <p>참고:또한 숙련된 사용자는 유연한 필터 기능을 활용하여 성공 및 터치 윈도우의 시간대를 뛰어넘어 집중할 수 있습니다. 예를 들어, 시간 범위를 선택하는 것 외에도 참조 도메인 세트를 선택하여 <i>해당</i> 도메인의 사용자에 대한 속성만 검사할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="uicontrol"> 복잡한 필터 설명 표시 </span> </td> 
   <td colname="col2"> 교육 필터, 성공 창 및 터치 창의 필터 코드를 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="uicontrol"> 모델 저장 </span> </td> 
   <td colname="col2"> 향후 사용을 위해 현재 속성 모델을 저장합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="uicontrol"> 모델 로드 </span> </td> 
   <td colname="col2"> 이전에 저장한 속성 모델을 엽니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="uicontrol"> 프레젠테이션 보기 </span> </td> 
   <td colname="col2"> 프레젠테이션의 상단 메뉴 막대를 숨깁니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>[옵션</b> ] &gt; [고급]에는 교육 세트 크기를 설정하고 클래스 불균형 시 적용할 방법을 지정하는 기능이 포함되어 있습니다. </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="uicontrol"> 고급 &gt; 교육 세트 크기 </span> </td> 
   <td colname="col2"> <p>교육 세트 크기를 설정합니다. </p> <p>참고: 기본 교육 크기는 250,000명의 방문자에게 큽니다. </p> 
    <ul id="ul_5F17C60227C34A85A2C476A32F2B5DCD"> 
     <li id="li_A076FC2AD0214ADDBFCFD82AEA5F0880">Tiny = 50,000 </li> 
     <li id="li_17E77E01D5374068BEBC80B3AD4CCD41">작음 = 75,000 </li> 
     <li id="li_7F6B4834742A4BFCBC3DB214425B88C3">보통 = 100,000 </li> 
     <li id="li_0BB7F791603745028CFC661EBC94D8B4">큼 = 250,000 </li> 
     <li id="li_34B60233C84F48F1BCB8040C5195411A">큼 = 500,000 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>고급 &gt; 클래스 균형 </b> </td> 
   <td colname="col2"> <p>데이터 집합 크기를 기반으로 하는 클래스 불균형 문제에 대해 생성할 입력 레코드 수를 식별하고 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

| 재설정 및 제거 옵션 | 설명 |
|---|---|
| **[!UICONTROL Reset Model]** | 메뉴에서 시각화를 **[!UICONTROL Reset]** **[!UICONTROL Reset Model]** 지우는 대신 입력 지표를 유지하려면 선택합니다. |
| **[!UICONTROL Reset All]** | 메뉴에서 시각화 및 입력 지표를 **[!UICONTROL Reset]** **[!UICONTROL Reset All]** 지우려면 선택합니다. |
| **[!UICONTROL Remove]** | 입력을 마우스 오른쪽 단추로 클릭하고 선택한 입력에서 지표를 **[!UICONTROL Remove]** 지우려면 선택합니다. |
| **[!UICONTROL Remove All]** | 채널을 마우스 오른쪽 단추로 클릭하고 *모든* 입력 지표를 **[!UICONTROL Remove All]** 지우려면 선택합니다. |

