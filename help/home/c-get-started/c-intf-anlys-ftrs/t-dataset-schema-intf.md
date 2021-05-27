---
description: 기본 시각화를 변경하는 절차.
title: 데이터 세트 스키마 인터페이스 구성
uuid: 953909e8-3382-43cf-98c0-d4785c6d1dda
exl-id: 0227663f-4789-4780-b753-d0deb35f6144
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 데이터 세트 스키마 인터페이스 구성{#configure-the-dataset-schema-interface}

기본 시각화를 변경하는 절차.

Profiles\*profile name*\Context\Dimension Legend folder of the Data Workbench server installation folder에 파일을 추가하여 [!DNL Dataset Schema Interface]에서 차원 이름을 클릭할 때 표시되는 시각화 유형을 제어할 수 있습니다. 이 폴더의 [!DNL Default.1d] 파일은 모든 차원에 대한 기본 시각화 유형을 제어합니다. *차원 이름*.1d 파일(예: [!DNL Hour.1d])을 이 폴더에 추가하면 해당 특정 차원에 대한 기본 시각화를 제어할 수 있습니다.

[!DNL Dataset Schema Interfaces]에 대한 자세한 내용은 [데이터 집합 스키마 인터페이스](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175)를 참조하십시오.

**기본 시각화를 변경하려면**

1. 작업 공간에서 새로운 기본 시각화에 표시할 데이터가 포함된 시각화를 만듭니다.

   예를 들어 차원을 막대 그래프에 표시하려면 원하는 지표 및 차원을 보여주는 막대 그래프 시각화를 만듭니다.

1. 콜아웃 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 을 클릭합니다.
1. [!DNL Save] 창에서 ![](assets/btn_folder_up.png) 을 클릭하고 **[!UICONTROL Context]** 를 두 번 클릭한 다음 **[!UICONTROL Dimension Legend]** 를 두 번 클릭합니다.
1. [!DNL File Name] 필드에 차원 이름을 입력합니다.

   [!DNL .1d] 파일의 이름은 차원의 이름과 정확히 일치해야 합니다. (예: [!DNL Hour.1d])

1. 파일 확장자를 &quot;1d&quot;로 변경하고 **[!UICONTROL Save]** 을 클릭합니다.

   파일이 User\*working profile name*\Context\Dimension Legend folder에 저장됩니다.

   다음에 [!DNL Dataset Schema Interface]에서 해당 차원을 클릭하면 지정한 시각화가 표시됩니다.

1. (선택 사항) 작업 프로필의 모든 사용자가 이 변경 사항을 사용할 수 있도록 하려면 다음을 수행하십시오.

   1. [!DNL Profile Manager]에서 **[!UICONTROL Context]**&#x200B;을 클릭한 다음 **[!UICONTROL Dimension Legend]**&#x200B;를 클릭합니다.

   1. [!DNL User] 열에서 새 콜아웃의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]*** 를 클릭합니다.
