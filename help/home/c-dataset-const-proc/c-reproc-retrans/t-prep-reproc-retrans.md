---
description: Data Workbench 사용자가 다시 작업하기 위해 재처리 또는 재변환이 원활하게 진행되고 제시간에 완료되도록 하는 절차
title: 재처리 또는 재변형 준비
uuid: 69a5878e-707a-4100-89ba-bae0b8a16c84
exl-id: f3746edf-416e-45c2-896c-48a3c875318c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 4%

---

# 재처리 또는 재변형 준비{#preparing-for-reprocessing-or-retransformation}

{{eol}}

Data Workbench 사용자가 다시 작업하기 위해 재처리 또는 재변환이 원활하게 진행되고 제시간에 완료되도록 하는 절차

1. 데이터 집합 프로필의 [!DNL Processing Mode History] 에서 [!DNL Detailed Status] 인터페이스.

   1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Detailed Status] 인터페이스.
   1. 클릭 **[!UICONTROL Processing Status]** > *&lt;**[!UICONTROL dataset profile name]**>* > **[!UICONTROL Processing Mode History]** 이전 처리 또는 변환의 경과 시간을 보려면

      * 빠른 입력은 로그 처리에 필요한 총 시간입니다.
      * 빠른 병합은 변환에 필요한 총 시간입니다.
      * 두 번(빠른 입력 + 빠른 병합) 합계는 데이터 집합을 처리하는 데 필요한 총 시간입니다.

      아래 예는 로그 처리에 약 43초가 소요되었지만 변환은 2분 미만의 시간이 소요되었음을 나타냅니다.

      ![](assets/vis_DetailedStatus_ProcessingModeHistory.png)

      에 대한 자세한 정보 [!DNL Detailed Status] 인터페이스, 자세한 내용은 *Data Workbench 사용 안내서*.


1. 재처리를 예약하고 계획합니다. Data Workbench 사용자는 로그 처리 단계 동안 데이터에 액세스할 수 없으므로 주말 등 적절한 시간(예: 주말 이상)에 재처리를 수행하도록 예약해야 합니다.
1. 의 필드를 사용하여 재처리 및 재변환의 진행 상황을 모니터링합니다 [!DNL Processing Legend.] 에 대한 자세한 정보 [!DNL Processing Legend]를 참조하고 *Data Workbench 사용 안내서*.
