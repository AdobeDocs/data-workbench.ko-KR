---
description: 워크시트를 사용하여 지표가 정의된 임계값에 도달했음을 나타낼 수 있습니다.
solution: Analytics
title: 지표 표시기 만들기
topic: Data workbench
uuid: da304004-ef45-4c89-8c91-dd5158172dd6
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 지표 표시기 만들기{#create-a-metric-indicator}

워크시트를 사용하여 지표가 정의된 임계값에 도달했음을 나타낼 수 있습니다.

또한 지표가 지정된 기간 내에 정의된 임계값에 도달할 때 보고서를 자동으로 생성하고 배포하는 [!DNL Report] 데 사용할 수 있습니다.

자세한 [!DNL Report]내용은 데이터 워크벤치 *보고서 안내서를 참조하십시오*.

* [위쪽 또는 아래쪽 표시기](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-40d7a2c3df0d40d4a7bb1a7e856abcba)
* [확인 표시기](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-98c5298a74f34dcbaaf151549fcc7090)

**워크시트를 사용하여 지표 표시기를 만들려면**

1. 워크시트의 셀 내용을 정의합니다.

   1. 열 A에서 원하는 지표의 이름을 입력합니다(예: [!DNL Visitors]).
   1. 열 B에서 원하는 지표의 값을 입력합니다(예: [!DNL =Visitors]).
   1. 열 C에서 지표의 낮은 임계값을 입력합니다.
   1. 열 D에서 지표의 높은 임계값을 입력합니다.
   1. 열 E에서 적절한 공식을 입력합니다. 예를 들어 위쪽 또는 [아래쪽 표시기](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-40d7a2c3df0d40d4a7bb1a7e856abcba) 또는 확인 [표시기를 참조하십시오](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-98c5298a74f34dcbaaf151549fcc7090).
   1. 공식 셀(열 E)에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Format]** > **[!UICONTROL Indicator]**&#x200B;을 클릭한 다음 다음 다음 중 하나를 클릭합니다.

      * **[!UICONTROL None]**:표시기 대신 정확한 계산을 나열합니다.
      * **[!UICONTROL Check]**:확인 표시 또는 X를 사용하여 공식에 따라 값이 설정한 임계값 위 또는 아래에 있음을 나타냅니다. 확인 [표시기를 참조하십시오](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-98c5298a74f34dcbaaf151549fcc7090).
      * **[!UICONTROL Up or Down]**:위쪽 또는 아래쪽 화살표를 사용하여 값이 낮은 임계값(아래쪽 화살표), 높은 임계값(위쪽 화살표) 위 또는 낮은 임계값과 높은 임계값 사이(비어 있음)를 나타냅니다. 위쪽 [또는 아래쪽 표시기를 참조하십시오](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-40d7a2c3df0d40d4a7bb1a7e856abcba).

1. 지표를 만들 다른 지표에 대해 1단계를 반복합니다.

결과 워크시트는 다음 예와 같습니다.

![](assets/vis_Worksheet_Alerts.png)

## 위쪽 또는 아래쪽 표시기 {#section-40d7a2c3df0d40d4a7bb1a7e856abcba}

또는 에 대해 [!DNL Up] 다음 공식을 [!DNL Down indicator]사용합니다.

[!DNL (metric value - low threshold)/(high threshold - low threshold)*2 - 1]

예: [!DNL =(b2-c2)/(d2-c2)*2-1]

이 공식을 [!DNL Up] 또는 [!DNL Down indicator]:

* 지표 값이 낮은 임계값과 높은 임계값 사이에 있으면 공식은 -1과 1 사이의 수로 평가됩니다(전용). 워크시트에 위쪽 또는 아래쪽 화살표가 표시되지 않습니다.
* 지표 값이 낮은 임계값보다 작거나 같은 경우 공식은 -1보다 작거나 같은 값으로 평가됩니다. 지표 표시기가 아래쪽 화살표로 변경됩니다.
* 지표 값이 높은 임계값보다 크거나 같은 경우 공식은 1보다 크거나 같은 숫자로 평가됩니다. 지표 표시기가 위쪽 화살표로 변경됩니다.

다음 워크시트는 예제 공식이 [!DNL =(b2-c2)/(d2-c2)*2-1] 표시되는 내용을 보여 줍니다.

![](assets/vis_Worksheet_Alerts_UpDown.png)

## 확인 표시기 {#section-98c5298a74f34dcbaaf151549fcc7090}

에 [!DNL Check indicator]대해, 지표 값이 지정한 임계값보다 높거나 낮을 때 알림을 받을 것인지 여부를 나타내는 공식을 사용합니다. 예:

* 값이 설정한 임계값 미만일 때 알림을 받으려면 다음 형식을 사용할 수 있습니다.

   * [!DNL threshold - metric]

      예: [!DNL =(c2-b2)]

* 값이 설정된 임계값을 초과할 때 알림을 받으려면 다음 공식을 사용할 수 있습니다.

   * [!DNL metric - threshold]

      예: [!DNL =(b3-c3)]

확인 표시가 표시되면 양수로 평가된 공식이 표시됩니다. X가 표시되면 공식을 음수로 계산했습니다.

다음 두 가지 결과를 사용할 때 각 지표에 대해 가능한 결과가 [!DNL Check indicator]있습니다.

* 공식이 지표 값을 임계값보다 높게 유지하는 것이 바람직함을 나타내는 경우 지표 값이 임계값보다 크거나 같을 때 확인 표시가 표시되고 값이 임계값보다 작으면 X가 표시됩니다.
* 공식이 지표 값을 임계값 아래로 유지하는 것이 바람직하다고 나타내는 경우 지표 값이 임계값보다 작거나 같으면 확인 표시가 표시되고 값이 임계값보다 크면 X가 표시됩니다.

다음 워크시트는 예제 수식과 [!DNL =(c2-b2)] 표시할 [!DNL =(b3-c3)] 내용을 보여 줍니다.

![](assets/vis_Worksheet_Alerts_Check.png)

