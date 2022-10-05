---
description: 프로필의 스키마 정의 초기화 및 업데이트
title: 프로필의 스키마 정의 초기화 및 업데이트
uuid: 38e47ded-340e-4f65-b06c-f2e2254f0863
exl-id: e8190909-4416-4d4a-8901-130d01906773
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---

# 프로필의 스키마 정의 초기화 및 업데이트{#initializing-and-updating-a-profile-s-schema-definition}

{{eol}}

1. 를 엽니다. **[!UICONTROL Schema Builder]** 을 사용하도록 설정할 수 있습니다.
1. A **[!UICONTROL Loading]** insight 프로필에서 스키마를 검색하는 동안 메시지가 표시됩니다. 스키마를 로드하는 시간은 로드되는 프로필의 복잡성에 따라 다릅니다.
1. 완료되면, **[!UICONTROL Insight Schema]** 왼쪽 창에서 **[!UICONTROL Dashboard Schema]** 오른쪽 창에 있습니다. 이 요약은 **[!UICONTROL Schema Builder]** 창을 엽니다.

   >[!NOTE]
   >
   >처음 스키마를 설정할 때 각 지표, 차원 및 필터가 대시보드의 스키마와 다르게 나열됩니다. 대시보드 스키마 개체가 현재 존재하지 않기 때문입니다.

   ![](assets/schema_builder2.png)

1. 을(를) 클릭합니다. **[!UICONTROL Synchronize with Schema]** 인사이트 스키마 보기에서 모든 지표, 차원 및 필터를 대시보드 스키마 보기와 동기화하기 위한 단추.
1. 완료되면 차이점을 찾을 수 없다는 메시지가 표시됩니다.

   ![](assets/diff_found.png)

1. 대시보드 스키마에 중복 지표 및 차원 등 오류가 있는 경우 저장하기 전에 수동으로 수정해야 합니다.

   >[!NOTE]
   >
   >지표나 차원 또는 필터를 **[!UICONTROL Dashboard Schema]** 대시보드 최종 사용자에게 표시되지 않도록 합니다. 항목이 대시보드 스키마에 없다는 경고가 표시되지만 저장되지 않습니다.

1. 준비가 되면 을(를) 클릭합니다. **[!UICONTROL Save]** 대시보드 스키마에 대한 변경 내용을 저장하려면 을 클릭합니다.
1. 대시보드 시스템은 이 스키마 정의를 사용하여 대시보드 인터페이스의 최종 사용자가 사용할 수 있는 차원, 지표 및 필터를 채웁니다.
