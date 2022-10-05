---
description: Premium 메뉴에서 최적 속성 을 열고 다음 단계에 따라 최적 속성 모델을 구축합니다.
title: 최적 속성 모델 구축
uuid: d1fd0340-1917-41bc-9a08-e78a79d084e7
exl-id: e0a42374-2500-46a3-a72a-708ab2d228db
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 1%

---

# 최적 속성 모델 구축{#build-a-best-fit-attribution-model}

{{eol}}

Premium 메뉴에서 최적 속성 을 열고 다음 단계에 따라 최적 속성 모델을 구축합니다.

개요 참조 [최적 속성](../../../../home/c-get-started/c-attribution-profiles/c-attrib-algorithmic/c-attrib-algorithmic.md#concept-237feb6e9c4d49efaf75399297dcb9d1).

1. 열기 **최적 속성**.

   작업 공간을 열고 를 클릭합니다. **[!UICONTROL Premium]** > **[!UICONTROL Best Fit Attribution]**.

   ![](assets/attrib_windows_launch.png)

   >[!NOTE]
   >
   >Best Fit Attribution은 프로필에서 Premium을 활성화해야 하는 Adobe Analytics Premium 기능입니다. 인증서를 업데이트하고 Premium 프로필을 profile.cfg 파일에 추가해야 합니다. 자세한 내용은 [DWB 서버 업그레이드: 6.2~6.3](/help/home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-2-to-6-3-upgrade.md) DWB 6.3용.

1. 설정 **[!UICONTROL Success]** 지표.

   >[!NOTE]
   >
   >지표를 **[!UICONTROL Finder]** 표(속성 시각화의 왼쪽 창)를 클릭하거나 **입력** 메뉴 아래의 제품에서 사용할 수 있습니다.

   클릭 **[!UICONTROL Inputs]** > **[!UICONTROL Set Success]**. 지표 메뉴가 열립니다. ![](assets/attrib_set_success_metric.png)

   성공적인 전환을 식별하는 지표를 선택합니다.

1. (선택 사항) **매출** 지표.

   전환 프로세스에서 매출을 평가하도록 지표를 설정합니다.

1. 설정 **터치** 지표.

   >[!NOTE]
   >
   >터치 지표 설정은 차원 요소를 시각화로 끌어 성공 지표를 자동으로 작성하려는 경우에만 필요합니다.

   을(를) 클릭합니다. **[!UICONTROL Inputs]** 메뉴 및 선택 **터치 설정**&#x200B;또는 파인더에서 지표를 드래그합니다. ![](assets/attrib_set_touch.png)

   차원 요소를 입력으로 사용할 때 채널 지표를 파생시키는 데 사용됩니다.

1. 설정 **성공** 창을 엽니다.

   클릭 [!DNL Inputs > Success Window]. 테이블에서 날짜 범위를 선택한 다음 성공 창의 이름을 지정합니다. 클릭 **[!UICONTROL Workspace Selection]** 선택한 날짜가 성공 지표에 대한 시간 범위로 지정됩니다.

   ![](assets/attrib_set_success_window.png)

   >[!NOTE]
   >
   >성공 창은 워크스테이션 선택이므로 성공 창에 차원을 포함할 수 있습니다.

1. 설정 **[!UICONTROL Touch Window]**.

   클릭 [!DNL Inputs > Touch Window]. 테이블에서 날짜 범위를 선택한 다음 터치 창의 이름을 지정합니다. 클릭 **[!UICONTROL Workspace Selection]** 선택한 날짜가 성공 지표에 대한 시간 범위로 지정됩니다.

   ![](assets/attrib_set_touch_window.png)

   기본적으로 **터치** 창이 와 동일한 기간으로 설정됩니다. **[!UICONTROL Success]** 창을 엽니다.

1. (선택 사항) 교육 필터를 설정합니다.

   을(를) 지정할 수도 있습니다 **교육 필터** 를 사용하여 방문자 데이터를 필터링합니다.

   >[!NOTE]
   >
   >성공 및 터치 창을 모두 설정할 때 교육 필터를 현재 작업 영역 선택 항목에 적용하여 데이터를 추가로 제한할 수 있습니다.

   ![](assets/attrib_filter.png)

   >[!NOTE]
   >
   >교육 세트는 항상 성공 기간을 충족하는 방문자로부터 그려집니다. 필터 편집기를 사용하여 필터링하면 성공 창에서 보고된 방문자의 하위 집합을 만들 수 있습니다.

1. 터치를 나타내는 채널 지표를 지정합니다.

   지표를 시각화로 드래그하거나 시각화에서 선택합니다 [!DNL Inputs] > [!DNL Add Channel] 메뉴 아래의 제품에서 사용할 수 있습니다. 캠페인이나 채널에 대해 정의된 지표가 아직 없지만 채널을 나타내는 차원이 있는 경우 터치 지표의 사양에 따라 시각화가 자동으로 구성될 수 있습니다.

   예를 들어 터치 지표가 [!DNL Hits], 및 [!DNL dimension] called [!DNL Media Type] 와 같은 항목을 포함하는 요소 사용 [!DNL Email], [!DNL Press Release], [!DNL Print Ad], 및 [!DNL Social Media]로 설정되면 시각화는 양식의 채널 지표를 생성합니다 [!DNL Hits where Media Type = Email] 요소를 시각화에 끌어다 놓습니다.

1. 누르기 **이동**.

   Best Fit Analysis 프로세스가 실행되며 선택한 입력을 기반으로 채널별 기여도가 차트에 표시됩니다.

   >[!NOTE]
   >
   >마우스 오른쪽 단추 클릭 **모델 완료** 완료된 분석에서 속성 모델에 대한 통계를 확인합니다.

   ![](assets/attrib_visualization.png)

완료되면 그래프는 채널별로 계산된 속성 모델 및 의 배포를 표시합니다 *매출* 지표 (설정된 경우). 모델을 내부적으로 저장하거나 다른 시스템으로 내보낼 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Streaming]**, **[!UICONTROL Online]** 및 **[!UICONTROL Offline]** 모드는 평가되는 데이터의 지연 시간을 기반으로 속성 모델을 작성할 때 다른 효과를 생성합니다. 스트리밍 모드에서 세부 사항 **[!UICONTROL Model Complete]** 메시지가 표시됩니다. 온라인 및 오프라인 모드에서 세부 사항 **[!UICONTROL Local Model Complete]** 이 표시됩니다.

## 옵션 메뉴 {#section-22288867f6c8483a8a38410f4b948346}

다음 **옵션** 이 메뉴는 최적 속성 분석을 설정 및 표시하기 위한 고급 기능을 제공합니다.

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
   <td colname="col2"> 교육 필터는 속성 모델을 작성할 때 모집단을 필터링하는 성공 창과 함께 사용됩니다. 이렇게 하면 분석하려는 방문자만 포함하는 데이터 하위 세트가 제공됩니다. <p>참고: 숙련된 사용자는 또한 필터의 유연성을 활용하여 성공 및 터치 윈도우의 시간대를 넘어 집중할 수도 있습니다. 예를 들어 시간 범위를 선택할 수 있을 뿐만 아니라, <i>참조 도메인</i> 를 입력하여 해당 도메인의 사용자에 대한 속성을 검사합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> 복잡한 필터 설명 표시 </span> </td>
   <td colname="col2"> 교육 필터, 성공 창 및 터치 창의 필터 코드를 표시합니다. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> 모델 저장 </span> </td>
   <td colname="col2"> 나중에 사용할 수 있도록 현재 속성 모델을 저장합니다. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> 모델 로드 </span> </td>
   <td colname="col2"> 이전에 저장한 속성 모델을 엽니다. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> 프레젠테이션 보기 </span> </td>
   <td colname="col2"> 프레젠테이션의 위쪽 메뉴 모음을 숨깁니다. </td>
  </tr>
  <tr>
   <td colname="col1"> <p><b>옵션 &gt; 고급</b> 교육 세트 크기를 설정하고 클래스 불균형 시 취할 접근 방식을 지정하는 기능이 포함됩니다. </p> </td>
   <td colname="col2"> </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> 고급 &gt; 교육 세트 크기 </span> </td>
   <td colname="col2"> <p>교육 집합 크기를 설정합니다. </p> <p>참고: 기본 교육 크기는 250,000명의 방문자에 대해 큽니다. </p>
    <ul id="ul_5F17C60227C34A85A2C476A32F2B5DCD">
     <li id="li_A076FC2AD0214ADDBFCFD82AEA5F0880">작은 = 50,000 </li>
     <li id="li_17E77E01D5374068BEBC80B3AD4CCD41">작게 = 75,000 </li>
     <li id="li_7F6B4834742A4BFCBC3DB214425B88C3">일반 = 100,000 </li>
     <li id="li_0BB7F791603745028CFC661EBC94D8B4">큰 = 250,00 </li>
     <li id="li_34B60233C84F48F1BCB8040C5195411A">거대 = 500,000 </li>
    </ul> </td>
  </tr>
  <tr>
   <td colname="col1"><b>고급 &gt; 분류 잔액 </b> </td>
   <td colname="col2"> <p>데이터 세트 크기를 기반으로 하여 클래스 불균형 문제에 대해 생성할 입력 레코드 수를 식별하고 정의합니다. </p> </td>
  </tr>
 </tbody>
</table>

| 재설정 및 제거 옵션 | 설명 |
|---|---|
| **[!UICONTROL Reset Model]** | 에서 **[!UICONTROL Reset]** 메뉴, 선택 **[!UICONTROL Reset Model]** 시각화를 지우지만 입력 지표를 유지합니다. |
| **[!UICONTROL Reset All]** | 에서 **[!UICONTROL Reset]** 메뉴, 선택 **[!UICONTROL Reset All]** 시각화 및 입력 지표를 지우려면 |
| **[!UICONTROL Remove]** | 입력을 마우스 오른쪽 단추로 클릭하고 를 선택합니다. **[!UICONTROL Remove]** 선택한 입력에서 지표를 지우려면 |
| **[!UICONTROL Remove All]** | 마우스 오른쪽 단추 클릭 *채널* 을(를) 선택합니다. **[!UICONTROL Remove All]** 모든 입력 지표를 지우려면 |
