---
description: 새 데이터 세트를 만드는 단계는 파일 포함
title: 새 데이터 세트 만들기 포함 파일
uuid: 707bdd84-b12b-4226-b6aa-43c9fc7ec9fe
exl-id: 8a7b343d-b695-41aa-b465-8c5cd68d6ef7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 3%

---

# 새 데이터 세트 만들기 포함 파일{#creating-new-dataset-include-files}

{{eol}}

새 데이터 세트를 만드는 단계는 파일 포함

다음 데이터 집합 구성 작업을 수행하려면 새 데이터 집합 포함 파일을 만들어야 합니다.

* 로그 처리에서 변환으로 전달할 데이터의 새 필드 지정
* 다음 중 하나를 수행하는 변환 정의:

   * 기존 로그 필드를 업데이트합니다.
   * 로그 처리에서 변형으로 전달되거나 확장 차원을 정의하는 데 사용되는 새 필드를 생성합니다.

      사용 가능한 변형 유형에 대한 자세한 내용은 [데이터 변환](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

      >[!NOTE]
      >
      >새 데이터 집합에 포함된 파일에서 변형을 정의하는 경우 입력 및 출력 순서를 염두에 두어야 합니다. 변형 순서에 대한 자세한 내용은 [변환 구성을 위한 규칙](../../../../home/c-dataset-const-proc/c-data-trans/c-con-transf.md#concept-01998eebb7e347c58255fb442f2613b6).

* 확장 차원 만들기. 사용 가능한 차원 유형에 대한 자세한 내용은 [확장 Dimension](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Profile Manager] 을(를) 클릭합니다. **[!UICONTROL Dataset]** 기존 데이터 집합을 보려면 포함 파일이 포함됩니다.

   * 를 보려면 [!DNL Log Processing Dataset Include] 파일, **[!UICONTROL Log Processing]**.

   * 를 보려면 [!DNL Transformation Dataset Include] 파일, **[!UICONTROL Transformation]**.

1. 새 만들기 [!DNL Log Processing] 또는 [!DNL Transformation Dataset Include] 다음 단계 중 하나를 수행하여 파일을 작성합니다.

   * 에서 [!DNL User] 로그 처리 디렉토리의 열에서 **[!UICONTROL Create]** > **[!UICONTROL New Log Processing]**. 이름이 인 파일 [!DNL New Log Processing.cfg] 이 디렉토리에 나타납니다.

   * 에서 [!DNL User] 변환 디렉토리의 열에서 **[!UICONTROL Create]** > **[!UICONTROL New Transformation]**. 이름이 인 파일 [!DNL New Transformation.cfg] 이 디렉토리에 나타납니다.

1. 새 파일의 이름을 변경하려면 [!DNL User] 열을 입력하고 파일 매개 변수에 새 이름을 입력합니다.

   ![단계 정보](assets/vis_ProfileManager_RenameFile.png)

1. 이름이 변경된 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 를 클릭합니다. **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 구성 창이 나타납니다.
1. 구성 파일에서 매개 변수를 적절하게 편집합니다. 자세한 내용은 [로그 처리 데이터 집합에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) 또는 [변형 데이터 집합에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) 를 참조하십시오.
1. 변경 사항을 저장하려면 마우스 오른쪽 단추를 클릭합니다 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;여기서 프로필 이름은 데이터 집합 프로필 또는 데이터 집합에 포함된 파일이 속한 상속된 프로필의 이름입니다. 데이터 집합 프로필을 동기화한 후 데이터의 재처리 또는 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.

생성한 데이터 집합 포함 파일을 편집하려면 다음을 참조하십시오 [기존 데이터 집합 편집 포함 파일](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).
