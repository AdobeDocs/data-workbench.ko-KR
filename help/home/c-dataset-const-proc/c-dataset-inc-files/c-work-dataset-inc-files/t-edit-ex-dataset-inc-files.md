---
description: 기존 데이터 세트를 편집하는 단계에는 파일이 포함됩니다.
title: 기존 데이터 세트 편집 포함 파일
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
exl-id: f4095871-d004-4e10-af18-bf6c1e47493d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 3%

---

# 기존 데이터 세트 편집 포함 파일{#editing-existing-dataset-include-files}

기존 데이터 세트를 편집하는 단계에는 파일이 포함됩니다.

데이터 워크벤치에서 [!DNL Profile Manager]을(를) 사용하여 기존 데이터 세트 포함 파일을 엽니다.

[!DNL Profile Manager]을(를) 열고 사용하는 방법에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.

1. 데이터 집합 프로필에서 작업하는 동안 [!DNL Profile Manager]을 열고 **[!UICONTROL Dataset]**&#x200B;을 클릭하여 디렉터리의 내용을 표시합니다.

   * [!DNL Log Processing Dataset Include] 파일을 열려면 **[!UICONTROL Log Processing]**&#x200B;을 클릭하여 디렉토리의 내용을 표시합니다.

   * [!DNL Transformation Dataset Include] 파일을 열려면 **[!UICONTROL Transformation]**&#x200B;을 클릭하여 디렉토리의 내용을 표시합니다.

1. 원하는 데이터 세트 포함 파일 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 구성 창이 나타납니다.

   데이터 세트에 [!DNL Transformation Dependency Maps]의 포함 파일을 열 수도 있습니다. [!DNL Transformation Dependency Maps]에 대한 자세한 내용은 [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.

1. 구성 파일의 매개 변수를 적절히 편집합니다. 매개 변수에 대한 설명은 [로그 처리 데이터 세트에 파일](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) 또는 [변형 데이터 세트에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace)을 참조하십시오.

   데이터 워크벤치 창에서 데이터 세트에 파일이 포함되어 있는 파일을 편집할 때 단축키(잘라내기(Ctrl+x), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그), 모든 선택(Ctrl+a)을 사용할 수 있습니다. 또한 단축키를 사용하여 한 구성 파일( [!DNL .cfg])의 텍스트를 복사하여 다른 구성 파일에 붙여넣을 수 있습니다.

1. 변경 내용을 저장하려면 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열의 파일 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;를 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트 포함 파일이 속한 상속된 프로필입니다. 데이터 세트 프로파일을 동기화한 후 데이터의 재처리 또는 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰여지기 때문에 수정된 구성 파일을 Adobe에서 제공하는 내부 프로파일에 저장하지 마십시오.
