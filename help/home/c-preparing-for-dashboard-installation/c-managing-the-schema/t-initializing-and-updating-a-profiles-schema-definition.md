---
description: 프로필의 스키마 정의 초기화 및 업데이트
title: 프로필의 스키마 정의 초기화 및 업데이트
uuid: 38e47ded-340e-4f65-b06c-f2e2254f0863
exl-id: e8190909-4416-4d4a-8901-130d01906773
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---

# 프로필의 스키마 정의 초기화 및 업데이트{#initializing-and-updating-a-profile-s-schema-definition}

1. 설정할 프로필의 **[!UICONTROL Schema Builder]** 을 엽니다.
1. Insight 프로필에서 스키마를 검색하는 동안 **[!UICONTROL Loading]** 메시지가 표시됩니다. 스키마를 로드하는 시간은 로드되는 프로필의 복잡성에 따라 다릅니다.
1. 완료되면 왼쪽 창에 **[!UICONTROL Insight Schema]** 및 오른쪽 창에 **[!UICONTROL Dashboard Schema]** 간의 차이점에 대한 요약이 표시됩니다. 이 요약은 **[!UICONTROL Schema Builder]** 창의 왼쪽 아래에 나타납니다.

   >[!NOTE]
   >
   >처음 스키마를 설정할 때 각 지표, 차원 및 필터가 대시보드의 스키마와 다르게 나열됩니다. 대시보드 스키마 개체가 현재 존재하지 않기 때문입니다.

   ![](assets/schema_builder2.png)

1. Insight Schema 보기의 모든 지표, 차원 및 필터를 대시보드 스키마 보기와 동기화하려면 **[!UICONTROL Synchronize with Schema]** 단추를 클릭합니다.
1. 완료되면 차이점을 찾을 수 없다는 메시지가 표시됩니다.

   ![](assets/diff_found.png)

1. 대시보드 스키마에 중복 지표 및 차원 등 오류가 있는 경우 저장하기 전에 수동으로 수정해야 합니다.

   >[!NOTE]
   >
   >대시보드의 최종 사용자에게 표시되지 않으려는 지표, 차원 또는 필터를 **[!UICONTROL Dashboard Schema]**&#x200B;에서 선택적으로 제거할 수 있습니다. 항목이 대시보드 스키마에 없다는 경고가 표시되지만 저장되지 않습니다.

1. 준비가 되면 **[!UICONTROL Save]** 을 클릭하여 변경 사항을 대시보드의 스키마에 저장합니다.
1. 대시보드 시스템은 이 스키마 정의를 사용하여 대시보드 인터페이스의 최종 사용자가 사용할 수 있는 차원, 지표 및 필터를 채웁니다.
