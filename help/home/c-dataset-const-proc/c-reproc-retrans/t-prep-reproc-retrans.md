---
description: 데이터 워크벤치 사용자가 다시 작업하기 위해 재처리 또는 재변환이 원활하고 제시간에 완료되도록 하는 절차
title: 재처리 또는 재변형 준비
uuid: 69a5878e-707a-4100-89ba-bae0b8a16c84
exl-id: f3746edf-416e-45c2-896c-48a3c875318c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 4%

---

# 재처리 또는 재변형 준비{#preparing-for-reprocessing-or-retransformation}

데이터 워크벤치 사용자가 다시 작업하기 위해 재처리 또는 재변환이 원활하고 제시간에 완료되도록 하는 절차

1. [!DNL Detailed Status] 인터페이스에서 데이터 집합 프로필의 [!DNL Processing Mode History]을 확인하여 이전 처리 또는 변환의 경과 시간을 결정합니다.

   1. 데이터 집합 프로필에서 작업하는 동안 [!DNL Detailed Status] 인터페이스를 엽니다.
   1. 이전 처리 또는 변환의 경과 시간을 보려면 **[!UICONTROL Processing Status]** > *&lt;**[!UICONTROL dataset profile name]*** > **[!UICONTROL Processing Mode History]**&#x200B;를 클릭합니다.

      * 빠른 입력은 로그 처리에 필요한 총 시간입니다.
      * 신속한 병합은 변환에 필요한 총 시간입니다.
      * 두 번(빠른 입력 + 빠른 병합)의 합계는 데이터 집합을 처리하는 데 필요한 총 시간입니다.

      아래 예제는 로그 처리에 걸리는 시간이 약 43초이고 변환에는 2분 미만임을 나타냅니다.

      ![](assets/vis_DetailedStatus_ProcessingModeHistory.png)

      [!DNL Detailed Status] 인터페이스에 대한 자세한 내용은 *Data Workbench 사용자 안내서*&#x200B;를 참조하십시오.


1. 재처리를 예약하고 계획합니다. 데이터 워크벤치 사용자는 로그 처리 단계 중 데이터에 액세스할 수 없으므로, 주말에 대한 것과 같이 적절한 시간 동안 재처리를 예약해야 합니다.
1. [!DNL Processing Legend.]의 필드를 사용하여 재처리 및 재변환의 진행 상황을 모니터링합니다. [!DNL Processing Legend]에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.
