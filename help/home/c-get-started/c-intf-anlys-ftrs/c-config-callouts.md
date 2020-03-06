---
description: 설명선은 시각화에서 특정 차원 요소의 가상 선택을 사용하여 새 시각화를 만들어 특정 차원 요소에 관심을 집중합니다.
solution: Analytics
title: 설명선 구성
topic: Data workbench
uuid: 779764bd-86c3-49cf-aabc-edb39caf0490
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 설명선 구성{#configure-a-callout}

설명선은 시각화에서 특정 차원 요소의 가상 선택을 사용하여 새 시각화를 만들어 특정 차원 요소에 관심을 집중합니다.

Profiles\*profile name*\Context\Callout folder of the  설치 폴더에 저장된 설명선 파일을 구성하여 설명선을 추가하거나 편집할 수 [!DNL Server] 있습니다. 워크시트 시각화에서 특정 지표에 주의를 기울이는 설명선을 지표 설명선이라고 합니다. 지표 설명선 파일은 프로필\*프로필 이름*\Context\Metric Callout folder에 저장됩니다.

시각화에 설명선 또는 지표 설명선을 추가하는 지침은 작업 공간에 [설명선 추가를 참조하십시오](../../../home/c-get-started/c-vis/c-call-wkspc.md#concept-212b09e763044d938987b4a9c658adc0).

**새 유형의 콜아웃을 생성하려면**

1. 모든 작업 영역에서 새 설명선 유형에 표시할 데이터가 포함된 시각화를 만듭니다. 예를 들어 설명선을 표로 만들려면 원하는 지표와 차원을 보여주는 테이블 시각화를 만듭니다.
1. 설명선 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;클릭합니다.
1. 창에서 [!DNL Save] 을 클릭하고 두 번 ![](assets/btn_folder_up.png)클릭한 다음 두 번 **[!UICONTROL Context]****[!UICONTROL Callout]**&#x200B;클릭합니다. 필드에 [!DNL File Name] 파일 이름을 입력하고 을 클릭합니다 **[!UICONTROL Save]**. 콜아웃 파일은 사용자\*작업 프로필 이름*\Context\Callout folder에 저장됩니다.

   >[!NOTE]
   >
   >콜아웃 이름을 지정할 때 시각화 유형과 표시되는 지표 및 차원을 반영하는 설명형 이름을 선택합니다. 예를 들어 일 차원의 세션 지표를 보여주는 테이블 시각화에서 콜아웃을 만들려면 콜아웃 이름을 &quot;일별 세션 테이블&quot;으로 지정할 수 있습니다.

1. (선택 사항) 이 변경 사항을 작업 중인 프로필의 모든 사용자가 사용할 수 있도록 하려면:

   1. 에서 [!DNL Profile Manager]을 **[!UICONTROL Context]**&#x200B;클릭한 다음 을 클릭합니다 **[!UICONTROL Callout]**. 이 폴더에는 기존 콜아웃 유형을 정의하는 모든 시각화 파일( [!DNL .vw])이 포함되어 있습니다.

   1. 열에서 새 설명선의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL working profile name]**을 클릭합니다*.

**설명선을 지표 설명선으로 변경하려면**

1. 에서 [!DNL Profile Manager]을 **[!UICONTROL Context]**&#x200B;클릭한 다음 을 클릭합니다 **[!UICONTROL Callout]**. 이 폴더에는 기존 콜아웃 유형을 정의하는 모든 시각화 파일( [!DNL .vw])이 포함되어 있습니다.

1. 변경할 콜아웃 유형의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 파일을 로컬 컴퓨터에 다운로드한 후 [!DNL User] 열에 확인 표시가 나타납니다.

1. 열의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Open]** **[!UICONTROL In Notepad]**&#x200B;을 클릭합니다.

1. 설명선 파일에서 [!DNL metric_y = ref:] 항목을 찾고 기존 값을 지표로 바꿉니다. 다음 파일 조각의 강조 표시된 텍스트는 이 단어를 삽입하는 위치를 보여줍니다.

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

1. 클릭 **[!UICONTROL File]** > **[!UICONTROL Save As]**. 창에서 한 번 **[!UICONTROL Save As]** 클릭한 다음 두 번 클릭합니다 **[!UICONTROL Metric Callout]**. 필드에 [!DNL File Name] 파일 이름을 입력하고 을 클릭합니다 **[!UICONTROL Save]**. 지표 설명선 파일은 사용자\*작업 프로필 이름*\Context\Metric Callout folder에 저장됩니다.

1. (선택 사항) 작업 중인 프로필의 모든 사용자가 이 지표 설명선을 사용할 수 있도록 하려면 [!DNL Profile Manager]열에서 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.

