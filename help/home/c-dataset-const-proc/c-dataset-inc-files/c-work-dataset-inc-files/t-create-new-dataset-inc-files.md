---
description: 새 데이터 세트를 만드는 단계에는 파일이 포함됩니다.
solution: Analytics
title: 새 데이터 세트 만들기 포함 파일
topic: Data workbench
uuid: 707bdd84-b12b-4226-b6aa-43c9fc7ec9fe
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 새 데이터 세트 만들기 포함 파일{#creating-new-dataset-include-files}

새 데이터 세트를 만드는 단계에는 파일이 포함됩니다.

다음 데이터 집합 구성 작업을 수행하려면 새 데이터 집합 포함 파일을 만들어야 합니다.

* 로그 처리에서 변환으로 전달할 데이터의 새 필드 지정
* 다음 중 하나를 수행하는 변형 정의:

   * 기존 로그 필드를 업데이트합니다.
   * 로그 처리에서 변환으로 전달하거나 확장 차원을 정의하는 데 사용되는 새 필드를 만듭니다.

      사용 가능한 변환 유형에 대한 자세한 내용은 데이터 [변형을 참조하십시오](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

      >[!NOTE]
      >
      >새 데이터 세트에 변형을 정의하는 경우 입력 및 출력 순서를 염두에 두어야 합니다. 변형 순서에 대한 자세한 내용은 변형 [구성을 위한 규칙을 참조하십시오](../../../../home/c-dataset-const-proc/c-data-trans/c-con-transf.md#concept-01998eebb7e347c58255fb442f2613b6).

* 확장 차원 만들기. 사용 가능한 차원 유형에 대한 자세한 내용은 확장 [차원을 참조하십시오](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

1. 데이터 세트 프로필에서 작업하는 동안 데이터 세트를 열고 [!DNL Profile Manager] 을 클릭하여 기존 데이터 세트에 포함된 파일을 **[!UICONTROL Dataset]** 봅니다.

   * 파일을 보려면 [!DNL Log Processing Dataset Include] 을 클릭합니다 **[!UICONTROL Log Processing]**.

   * 파일을 보려면 [!DNL Transformation Dataset Include] 을 클릭합니다 **[!UICONTROL Transformation]**.

1. 다음 단계 중 하나를 수행하여 새 [!DNL Log Processing] 또는 [!DNL Transformation Dataset Include] 파일을 만듭니다.

   * 로그 처리 디렉토리의 [!DNL User] 열에서 **[!UICONTROL Create]** > **[!UICONTROL New Log Processing]**&#x200B;를 클릭합니다. 디렉토리에 이름이 지정된 파일이 [!DNL New Log Processing.cfg] 나타납니다.

   * 변환 디렉토리의 [!DNL User] 열에서 **[!UICONTROL Create]** > 를 **[!UICONTROL New Transformation]**&#x200B;클릭합니다. 디렉토리에 이름이 지정된 파일이 [!DNL New Transformation.cfg] 나타납니다.

1. 열에서 해당 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 File 매개 변수에 새 이름을 입력하여 새 파일의 이름을 변경합니다. [!DNL User]

   ![단계 정보](assets/vis_ProfileManager_RenameFile.png)

1. 이름을 바꾼 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;을 클릭합니다. 구성 창이 나타납니다.
1. 구성 파일의 매개 변수를 적절히 편집합니다. 사용 가능한 [매개 변수에 대한 설명을 보려면 로그 처리 데이터](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) 세트에 파일 또는 [변형 데이터 세트 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) 파일을 참조하십시오.
1. 변경 내용을 저장하려면 창 **[!UICONTROL (modified)]** 맨 위에 있는 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Profile Manager]> [!DNL User] &lt; **[!UICONTROL Save to]** > ***[!UICONTROL profile name]***&#x200B;을 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트에 포함된 파일이 속하는 상속된 프로필입니다. 데이터 집합 프로필의 동기화 후 데이터의 재처리 또는 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

데이터 세트에 만든 파일이 포함되어 있는 파일을 편집하려면 기존 데이터 [세트 포함 파일 편집을 참조하십시오](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).
