---
description: 기존 데이터 집합을 편집하는 단계는 파일을 포함합니다.
title: 기존 데이터 세트 편집 포함 파일
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
exl-id: f4095871-d004-4e10-af18-bf6c1e47493d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 3%

---

# 기존 데이터 세트 편집 포함 파일{#editing-existing-dataset-include-files}

{{eol}}

기존 데이터 집합을 편집하는 단계는 파일을 포함합니다.

기존 데이터 집합 포함 파일은 [!DNL Profile Manager] data workbench에서 확인하십시오.

열기 및 작업에 대한 자세한 내용은 [!DNL Profile Manager]를 참조하고 *Data Workbench 사용 안내서*.

1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Profile Manager] 을(를) 클릭합니다. **[!UICONTROL Dataset]** 디렉토리 내용을 표시합니다.

   * 를 열려면 [!DNL Log Processing Dataset Include] 파일, **[!UICONTROL Log Processing]** 디렉토리 내용을 표시합니다.

   * 를 열려면 [!DNL Transformation Dataset Include] 파일, **[!UICONTROL Transformation]** 디렉토리 내용을 표시합니다.

1. 원하는 데이터 세트 포함 파일 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 를 클릭합니다 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 구성 창이 나타납니다.

   데이터 집합에 포함된 파일을 [!DNL Transformation Dependency Maps]. 에 대한 자세한 정보 [!DNL Transformation Dependency Maps]를 참조하십시오. [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

1. 구성 파일에서 매개 변수를 적절하게 편집합니다. 자세한 내용은 [로그 처리 데이터 집합에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) 또는 [변형 데이터 집합에 파일 포함](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) 를 참조하십시오.

   데이터 집합 포함 파일을 Data Workbench 창 내에서 편집할 때 잘라내기(Ctrl+x), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a )을 비롯한 기본적인 편집 기능에 바로 가기 키를 사용할 수 있습니다. 또한 바로 가기를 사용하여 한 구성 파일( [!DNL .cfg])를 다른 이름으로 바꿉니다.

1. 변경 사항을 저장하려면 마우스 오른쪽 단추를 클릭합니다 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;여기서 프로필 이름은 데이터 집합 프로필 또는 데이터 집합에 포함된 파일이 속한 상속된 프로필의 이름입니다. 데이터 집합 프로필을 동기화한 후 데이터의 재처리 또는 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.
