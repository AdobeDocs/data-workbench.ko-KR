---
description: x-experiment 필드를 사용할 수 있으므로 데이터 세트에 x-experiment 필드를 포함하도록 확장 차원을 만들어야 합니다. 이 필드를 통해 Insight에서 결과를 볼 수 있습니다.
solution: Analytics,Analytics
title: Transformation.cfg 수정
uuid: c17e48db-8fd9-4640-b621-6963bb8223d7
exl-id: a9c89789-8290-4a24-91c1-ca1c5b7b437a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---

# Transformation.cfg 수정{#modifying-transformation-cfg}

x-experiment 필드를 사용할 수 있으므로 데이터 세트에 x-experiment 필드를 포함하도록 확장 차원을 만들어야 합니다. 이 필드를 통해 Insight에서 결과를 볼 수 있습니다.

이렇게 하려면 [!DNL Transformation.cfg] 파일에 새 차원을 추가해야 합니다.

여러 실험을 실행할 계획이라면 [!DNL Transformation.cfg] 파일에 새 분할 변환도 추가해야 합니다. 이 분할 변환은 다른 실험 및 그룹 이름을 분리하므로 정보를 해석하기가 더 쉽습니다. 나중에 추가 실험을 추가해야 하는 경우 데이터를 다시 재처리하지 않도록 하려면 현재 여러 실험을 실행할 계획이 없는 경우에도 분할 변형을 추가하는 것이 좋습니다.

다음 절차에는 새 분할 변환과 확장 차원 모두에 대한 생성이 포함됩니다. 분할 변환을 추가하지 않으려면 5-7단계를 건너뛰십시오.

**Transformation.cfg를 수정하려면**

1. [!DNL Insight]에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]**&#x200B;를 클릭하거나 [!DNL Admin] 탭에서 프로필 관리 작업 공간을 열어 [!DNL Profile Manager] 을 엽니다.
1. [!DNL Profile Manager]에서 **[!UICONTROL Dataset]**&#x200B;을 클릭하여 콘텐츠를 표시합니다.
1. [!DNL Transformation.cfg] 옆의 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다. [!DNL Transformation.cfg] 창이 나타납니다.
1. 내용을 표시하려면 **[!UICONTROL Transformation]** 을 클릭하십시오.
1. **[!UICONTROL Transformations]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Split]** 를 클릭합니다.
1. 다음 예에 표시된 대로 쉼표 변환에서 새 분할을 완료합니다.

   ![단계 정보](assets/New_split_transformation.png)

   >[!NOTE]
   >
   >이름 필드에 값을 입력할 수 있습니다.

1. **[!UICONTROL Extended Dimensions]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL ManyToMany]** 를 클릭합니다.
1. 다음 예와 같이 새 차원을 완료합니다.

   ![단계 정보](assets/New_Dimension_controlled_experiment_groups.png)

   >[!NOTE]
   >
   >* 이름 필드에 값을 입력할 수 있습니다.
   >* 분할 변형을 포함하지 않은 경우 [!DNL Input] 필드에 &quot;x-experiment&quot;를 입력해야 합니다.


1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.
1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL Transformation.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > **[!UICONTROL profile name]**&#x200B;를 클릭하여 로컬에서 변경한 작업 프로필을 저장합니다.

   >[!NOTE]
   >
   >데이터 세트가 즉시 재변환을 시작합니다.

   [!DNL Transformation.cfg] 및 확장 차원에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.
