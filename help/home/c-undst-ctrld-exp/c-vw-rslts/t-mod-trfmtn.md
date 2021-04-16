---
description: x-실험 필드를 사용할 수 있으므로 데이터 세트에 x-실험 필드를 포함할 확장 차원을 만들어야 합니다. 이렇게 하면 Insight에서 결과를 볼 수 있습니다.
solution: Analytics,Analytics
title: Transformation.cfg 수정
uuid: c17e48db-8fd9-4640-b621-6963bb8223d7
exl-id: a9c89789-8290-4a24-91c1-ca1c5b7b437a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---

# Transformation.cfg 수정{#modifying-transformation-cfg}

x-실험 필드를 사용할 수 있으므로 데이터 세트에 x-실험 필드를 포함할 확장 차원을 만들어야 합니다. 이렇게 하면 Insight에서 결과를 볼 수 있습니다.

이렇게 하려면 [!DNL Transformation.cfg] 파일에 새 차원을 추가해야 합니다.

여러 실험을 실행할 계획인 경우 새 분할 변형을 [!DNL Transformation.cfg] 파일에 추가해야 합니다. 이 분할 변환은 정보를 보다 쉽게 해석할 수 있도록 서로 다른 실험과 그룹 이름을 구분합니다. 나중에 추가 실험을 추가할 필요가 있는 경우 데이터를 다시 재처리하지 않으려면 현재 여러 개의 실험을 실행할 계획이 없는 경우에도 분할 변형을 추가하는 것이 좋습니다.

다음 절차에는 새 분할 변형과 확장 치수 생성을 포함합니다. 분할 변형을 추가하지 않으려면 5-7단계를 건너뛰기만 하면 됩니다.

**Transformation.cfg를 수정하려면**

1. [!DNL Insight]에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 [!DNL Profile Manager] > **[!UICONTROL Profile Manager]**&#x200B;을 클릭하거나 [!DNL Admin] 탭에서 프로필 관리 작업 영역을 열어 **[!UICONTROL Admin]** 파일을 엽니다.
1. [!DNL Profile Manager]에서 **[!UICONTROL Dataset]**&#x200B;을 클릭하여 내용을 표시합니다.
1. [!DNL Transformation.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. [!DNL Transformation.cfg] 창이 나타납니다.
1. 내용을 표시하려면 **[!UICONTROL Transformation]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Transformations]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Split]**&#x200B;를 클릭합니다.
1. 다음 예제와 같이 쉼표 변환에서 새 분할을 완료합니다.

   ![단계 정보](assets/New_split_transformation.png)

   >[!NOTE]
   >
   >이름 필드에 값을 입력할 수 있습니다.

1. **[!UICONTROL Extended Dimensions]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL ManyToMany]**&#x200B;를 클릭합니다.
1. 다음 예와 같이 새 차원을 완료합니다.

   ![단계 정보](assets/New_Dimension_controlled_experiment_groups.png)

   >[!NOTE]
   >
   >* 이름 필드에 값을 입력할 수 있습니다.
   >* 분할 변형을 포함하지 않은 경우 [!DNL Input] 필드에 &quot;x-expertion&quot;을 입력해야 합니다.


1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL Transformation.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > **[!UICONTROL profile name]**&#x200B;를 클릭하여 작업 프로필에 로컬로 변경한 내용을 저장합니다.

   >[!NOTE]
   >
   >데이터 세트가 즉시 다시 변형되기 시작합니다.

   [!DNL Transformation.cfg] 및 확장 차원에 대한 자세한 내용은 *데이터 세트 구성 안내서*&#x200B;를 참조하십시오.
