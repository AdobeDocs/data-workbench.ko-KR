---
description: 설명선은 시각화에서 특정 차원 요소의 가상 선택을 사용하여 새 시각화를 만들어 특정 차원 요소에 주의를 줍니다.
title: 설명선 구성
uuid: 779764bd-86c3-49cf-aabc-edb39caf0490
exl-id: 509163b2-0bd1-47b4-8612-aac460a501cc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# 설명선 구성{#configure-a-callout}

{{eol}}

설명선은 시각화에서 특정 차원 요소의 가상 선택을 사용하여 새 시각화를 만들어 특정 차원 요소에 주의를 줍니다.

Profiles\*profile name*\Context\Callout 폴더에 저장된 콜아웃 파일을 구성하여 콜아웃을 추가하거나 편집할 수 있습니다 [!DNL Server] 설치 폴더. 워크시트 시각화의 특정 지표에 주의를 기울이는 콜아웃을 지표 콜아웃이라고 합니다. 지표 콜아웃 파일은 Profiles\*profile name*\Context\Metric Callout 폴더에 저장됩니다.

시각화에 설명선 또는 지표 설명선을 추가하는 방법은 다음을 참조하십시오 [작업 공간에 설명선 추가](../../../home/c-get-started/c-vis/c-call-wkspc.md#concept-212b09e763044d938987b4a9c658adc0).

**새 유형의 콜아웃을 생성하려면**

1. 모든 작업 영역에서 새 콜아웃 유형에 표시할 데이터가 포함된 시각화를 만듭니다. 예를 들어 콜아웃을 테이블로 만들려면 원하는 지표 및 차원을 보여주는 테이블 시각화를 만듭니다.
1. 콜아웃 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**.
1. 에서 [!DNL Save] 창 ![](assets/btn_folder_up.png), 두 번 클릭 **[!UICONTROL Context]**&#x200B;를 두 번 클릭한 다음 **[!UICONTROL Callout]**. 에서 [!DNL File Name] 필드에 파일 이름을 입력하고 **[!UICONTROL Save]**. 콜아웃 파일은 User\*working profile name*\Context\Callout 폴더에 저장됩니다.

   >[!NOTE]
   >
   >콜아웃 이름을 지정할 때 시각화 유형 및 표시되는 지표 및 차원을 반영하는 설명적 이름을 선택합니다. 예를 들어 일 차원의 세션 지표를 표시하는 테이블 시각화에서 콜아웃을 만들려면 콜아웃 이름을 &quot;일별 세션&quot; 로 지정할 수 있습니다.

1. (선택 사항) 작업 프로필의 모든 사용자가 이 변경 사항을 사용할 수 있도록 하려면 다음을 수행하십시오.

   1. 에서 [!DNL Profile Manager]를 클릭합니다. **[!UICONTROL Context]**&#x200B;를 클릭한 다음 **[!UICONTROL Callout]**. 이 폴더에는 모든 시각화 파일( [!DNL .vw])을 클릭하여 기존 설명선 유형을 정의합니다.

   1. 에서 새 콜아웃의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

**콜아웃을 지표 콜아웃으로 변경하려면**

1. 에서 [!DNL Profile Manager]를 클릭합니다. **[!UICONTROL Context]**&#x200B;를 클릭한 다음 **[!UICONTROL Callout]**. 이 폴더에는 모든 시각화 파일( [!DNL .vw])을 클릭하여 기존 설명선 유형을 정의합니다.

1. 변경할 콜아웃 유형의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 를 클릭합니다 **[!UICONTROL Make Local]**. 파일을 로컬 컴퓨터에 다운로드한 후에는 [!DNL User] 열.

1. 에서 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL In Notepad]**.

1. 을(를) 찾습니다 [!DNL metric_y = ref:] 콜아웃 파일의 항목을 입력하고 기존 값을 지표로 바꿉니다. 다음 파일 조각의 강조 표시된 텍스트는 이 단어를 삽입한 위치를 보여줍니다.

   ```
   window = simpleBorderWindow: 
     client = graph: 
       bars = bool: true
       dim_x = ref: wdata/model/dim/dimension name
       lines = bool: false
       metrics = vector: 1 items
         0 = gr_metric: 
           metric_y = ref: Metric
           yaxis = axisLegend: 
             max_value = double: maximum y-value
             min_value = double: minimum y-value
             zoom_max = double: maximum y-zoom
             zoom_min = double: minimum y-zoom
   . . . 
   ```

1. 클릭 **[!UICONTROL File]** > **[!UICONTROL Save As]**. 에서 **[!UICONTROL Save As]** 창을 한 번 클릭한 다음 두 번 클릭합니다 **[!UICONTROL Metric Callout]**. 에서 [!DNL File Name] 필드에 파일 이름을 입력하고 **[!UICONTROL Save]**. 지표 콜아웃 파일은 User\*working profile name*\Context\Metric Callout 폴더에 저장됩니다.

1. (선택 사항) 작업 프로필의 모든 사용자가 이 지표 콜아웃을 사용할 수 있도록 하려면 [!DNL Profile Manager]에서 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
