---
description: 기존 데이터 집합을 편집하는 단계는 파일을 포함합니다.
title: 기존 데이터 세트 편집 포함 파일
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
exl-id: f4095871-d004-4e10-af18-bf6c1e47493d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 3%

---

# 기존 데이터 세트 편집 포함 파일{#editing-existing-dataset-include-files}

기존 데이터 집합을 편집하는 단계는 파일을 포함합니다.

Data Workbench에서 [!DNL Profile Manager] 을 사용하여 기존 데이터 집합 포함 파일을 엽니다.

[!DNL Profile Manager] 열기 및 작업에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.

1. 데이터 집합 프로필에서 작업하는 동안 [!DNL Profile Manager] 을 열고 **[!UICONTROL Dataset]** 를 클릭하여 디렉토리의 콘텐츠를 표시합니다.

   * [!DNL Log Processing Dataset Include] 파일을 열려면 **[!UICONTROL Log Processing]** 을 클릭하여 디렉터리 내용을 표시합니다.

   * [!DNL Transformation Dataset Include] 파일을 열려면 **[!UICONTROL Transformation]** 을 클릭하여 디렉터리 내용을 표시합니다.

1. 원하는 데이터 세트 포함 파일 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]** 를 클릭합니다. 구성 창이 나타납니다.

   데이터 집합 포함 파일을 [!DNL Transformation Dependency Maps]에서 열 수도 있습니다. [!DNL Transformation Dependency Maps]에 대한 자세한 내용은 [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.

1. 구성 파일에서 매개 변수를 적절하게 편집합니다. 매개 변수에 대한 설명은 [로그 처리 데이터 집합에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) 또는 [변형 데이터 집합에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace)을 참조하십시오.

   데이터 집합 포함 파일을 Data Workbench 창 내에서 편집할 때 잘라내기(Ctrl+x), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a )을 비롯한 기본적인 편집 기능에 바로 가기 키를 사용할 수 있습니다. 또한 바로 가기를 사용하여 한 구성 파일( [!DNL .cfg])에서 다른 구성 파일로 텍스트를 복사하고 붙여넣을 수 있습니다.

1. 변경 사항을 저장하려면 창 상단에 있는 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.
1. 로컬로 수행된 변경 사항을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]*** 를 클릭합니다. 여기서 프로필 이름은 데이터 집합 프로필의 이름이거나 포함 파일이 속한 데이터 집합에 속한 상속된 프로필입니다. 데이터 집합 프로필을 동기화한 후 데이터의 재처리 또는 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.
