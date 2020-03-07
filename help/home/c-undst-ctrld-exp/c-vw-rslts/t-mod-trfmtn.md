---
description: x-experiment 필드를 사용할 수 있으므로 데이터 세트에 x-experiment 필드를 포함할 확장 차원을 만들어야 합니다. 이렇게 하면 Insight에서 결과를 볼 수 있습니다.
solution: Insight,Analytics
title: Transformation.cfg 수정
topic: Data workbench
uuid: c17e48db-8fd9-4640-b621-6963bb8223d7
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Transformation.cfg 수정{#modifying-transformation-cfg}

x-experiment 필드를 사용할 수 있으므로 데이터 세트에 x-experiment 필드를 포함할 확장 차원을 만들어야 합니다. 이렇게 하면 Insight에서 결과를 볼 수 있습니다.

이렇게 하려면 [!DNL Transformation.cfg] 파일에 새 차원을 추가해야 합니다.

여러 실험을 실행하려면 [!DNL Transformation.cfg] 파일에 새로운 분할 변형을 추가해야 합니다. 이 분할 변환은 정보를 보다 쉽게 해석할 수 있도록 서로 다른 실험 및 그룹 이름을 구분합니다. 나중에 추가적인 실험을 추가해야 하는 경우 데이터를 다시 재처리하지 않으려면 현재 여러 실험을 실행할 계획이 없는 경우에도 분할 변형을 추가하는 것이 좋습니다.

다음 절차에는 새 분할 변환과 확장 치수 둘 다의 생성이 포함됩니다. 분할 변형을 추가하지 않으려면 5-7단계를 건너뛰기만 하면 됩니다.

**Transformation.cfg를 수정하려면**

1. 에서 작업 공간 내에서 마우스 오른쪽 단추를 [!DNL Insight]클릭하고 [!DNL Profile Manager] > **[!UICONTROL Admin]** 를 클릭하거나 **[!UICONTROL Profile Manager]**[!DNL Admin] 탭에서 프로필 관리 작업 영역을 열어 해당 작업을 엽니다.
1. 에서 [!DNL Profile Manager]아이콘을 클릭하여 **[!UICONTROL Dataset]** 내용을 표시합니다.
1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL Transformation.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. 창이 [!DNL Transformation.cfg] 나타납니다.
1. 아이콘을 **[!UICONTROL Transformation]** 클릭하여 컨텐츠를 표시합니다.
1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Transformations]** > **[!UICONTROL Add new]** **[!UICONTROL Split]**&#x200B;를 클릭합니다.
1. 다음 예와 같이 쉼표 변환 시 새 분할을 완료합니다.

   ![단계 정보](assets/New_split_transformation.png)

   >[!NOTE]
   >
   >이름 필드에 값을 입력할 수 있습니다.

1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Extended Dimensions]** > **[!UICONTROL Add new]** **[!UICONTROL ManyToMany]**&#x200B;를 클릭합니다.
1. 다음 예와 같이 새 차원을 완료합니다.

   ![단계 정보](assets/New_Dimension_controlled_experiment_groups.png)

   >[!NOTE]
   >
   >* 이름 필드에 값을 입력할 수 있습니다.
   >* 분할 변형을 포함하지 않은 경우 [!DNL Input] 필드에 &quot;x-experiment&quot;를 입력해야 합니다.


1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Transformation.cfg] >을 클릭하여 [!DNL User] **[!UICONTROL Save to]** **[!UICONTROL profile name]** 로컬에서 만든 작업 프로필에 변경 내용을 저장합니다.

   >[!NOTE]
   >
   >데이터 세트가 즉시 다시 변환되기 시작합니다.

   확장 [!DNL Transformation.cfg] 및 데이터 세트에 대한 자세한 내용은 데이터 세트 *구성 안내서를 참조하십시오*.
