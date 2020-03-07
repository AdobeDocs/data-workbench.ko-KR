---
description: 데이터 워크벤치 사용자가 다시 작업하기 위해 재처리 또는 재변환이 순조롭게 진행되어 제 시간에 완료되도록 하는 절차
solution: Analytics
title: 재처리 또는 재변형 준비
topic: Data workbench
uuid: 69a5878e-707a-4100-89ba-bae0b8a16c84
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 재처리 또는 재변형 준비{#preparing-for-reprocessing-or-retransformation}

데이터 워크벤치 사용자가 다시 작업하기 위해 재처리 또는 재변환이 순조롭게 진행되어 제 시간에 완료되도록 하는 절차

1. 데이터 집합 프로필의 [!DNL Processing Mode History] [!DNL Detailed Status] 인터페이스를 확인하여 이전 처리 또는 변환 경과 시간을 결정합니다.

   1. 데이터 집합 프로필에서 작업하는 동안 [!DNL Detailed Status] 인터페이스를 엽니다.
   1. > **[!UICONTROL Processing Status]** &lt; ***[!UICONTROL dataset profile name]**>* > **[!UICONTROL Processing Mode History]** 을 클릭하여 이전 처리 또는 변환의 경과 시간을 봅니다.

      * 빠른 입력은 로그 처리에 필요한 총 시간입니다.
      * 빠른 병합은 변환에 필요한 총 시간입니다.
      * 두 번(빠른 입력 + 빠른 병합)의 합계는 데이터 세트를 처리하는 데 필요한 총 시간입니다.
      아래 예는 로그 처리에 약 43초가 소요되었지만 변환에 2분 미만이 소요되었음을 나타냅니다.

      ![](assets/vis_DetailedStatus_ProcessingModeHistory.png)

      인터페이스에 대한 자세한 내용은 [!DNL Detailed Status] 데이터 워크벤치 *사용 안내서를 참조하십시오*.


1. 재처리를 예약하고 계획합니다. 데이터 워크벤치 사용자는 로그 처리 단계 동안 데이터에 액세스할 수 없으므로 주말 등 적절한 시간 동안 재처리를 예약해야 합니다.
1. Data Workbench 사용자 안내서의 필드를 사용하여 재처리 및 [!DNL Processing Legend.] 재변환의 진행 상황을 [!DNL Processing Legend]모니터링합니다 **.
