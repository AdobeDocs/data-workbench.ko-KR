---
description: 기본 시각화를 변경하는 단계입니다.
solution: Analytics
title: 데이터 집합 스키마 인터페이스 구성
topic: Data workbench
uuid: 953909e8-3382-43cf-98c0-d4785c6d1dda
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# 데이터 집합 스키마 인터페이스 구성{#configure-the-dataset-schema-interface}

기본 시각화를 변경하는 단계입니다.

Profiles\*profile name*\Context\Dimension Legend folder of the Data Workbench server installation folder에 파일을 추가하여 Creative Cloud에서 차원 이름을 클릭할 때 표시되는 시각화 유형을 제어할 [!DNL Dataset Schema Interface] 수 있습니다. 이 폴더의 [!DNL Default.1d] 파일은 모든 차원에 대한 기본 시각화 유형을 제어합니다. 이 폴더에 *차원 이름*.1d 파일(예: [!DNL Hour.1d])을 추가하면 해당 특정 차원에 대한 기본 시각화를 제어할 수 있습니다.

자세한 [!DNL Dataset Schema Interfaces]내용은 데이터 집합 [스키마 인터페이스를 참조하십시오](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175).

**기본 시각화를 변경하려면**

1. 모든 작업 영역에서 새 기본 시각화에 표시할 데이터가 포함된 시각화를 만듭니다.

   예를 들어 차원을 막대 그래프로 표시하려면 원하는 지표와 차원을 보여주는 막대 그래프 시각화를 만듭니다.

1. 설명선 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;클릭합니다.
1. 창에서 [!DNL Save] 을 클릭하고 두 번 ![](assets/btn_folder_up.png)클릭한 다음 두 번 **[!UICONTROL Context]****[!UICONTROL Dimension Legend]**&#x200B;클릭합니다.
1. 필드에 [!DNL File Name] 차원 이름을 입력합니다.

   The name of the [!DNL .1d] file must match the name of the dimension exactly. (예: [!DNL Hour.1d])

1. 파일 확장명을 &quot;1d&quot;로 변경하고 을 **[!UICONTROL Save]**&#x200B;클릭합니다.

   파일이 User\*working profile name*\Context\Dimension Legend folder에 저장됩니다.

   다음에 In a에서 해당 차원을 클릭하면 지정한 [!DNL Dataset Schema Interface]시각화가 표시됩니다.

1. (선택 사항) 이 변경 사항을 작업 중인 프로필의 모든 사용자가 사용할 수 있도록 하려면:

   1. 에서 [!DNL Profile Manager]을 **[!UICONTROL Context]**&#x200B;클릭한 다음 을 클릭합니다 **[!UICONTROL Dimension Legend]**.

   1. 열에서 새 설명선의 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL working profile name]**을 클릭합니다*.

