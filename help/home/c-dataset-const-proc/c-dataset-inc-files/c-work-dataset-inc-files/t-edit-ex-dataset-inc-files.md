---
description: 기존 데이터 세트를 편집하는 단계에는 파일이 포함됩니다.
solution: Analytics
title: 기존 데이터 세트 편집 포함 파일
topic: Data workbench
uuid: fcce2e46-b4a8-4c53-83bb-32ab410eb89e
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 기존 데이터 세트 편집 포함 파일{#editing-existing-dataset-include-files}

기존 데이터 세트를 편집하는 단계에는 파일이 포함됩니다.

데이터 워크벤치에서 을 사용하여 기존 데이터 세트 포함 파일을 열 [!DNL Profile Manager] 수 있습니다.

데이터 워크벤치 사용자 안내서를 [!DNL Profile Manager]참조하여 열기 및 작업에 *대한 정보를 얻을 수 있습니다*.

1. 데이터 집합 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 열고 을 클릭하여 **[!UICONTROL Dataset]** 디렉터리의 내용을 표시합니다.

   * 파일을 열려면 [!DNL Log Processing Dataset Include] **[!UICONTROL Log Processing]** 을 클릭하여 디렉토리의 컨텐츠를 표시합니다.

   * 파일을 열려면 [!DNL Transformation Dataset Include] **[!UICONTROL Transformation]** 을 클릭하여 디렉토리의 컨텐츠를 표시합니다.

1. 원하는 데이터 세트 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 구성 창이 나타납니다.

   데이터 세트에 포함된 파일을 열 수도 [!DNL Transformation Dependency Maps]있습니다. 자세한 내용은 [!DNL Transformation Dependency Maps]재처리 및 [재변형을 참조하십시오](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

1. 구성 파일의 매개 변수를 적절히 편집합니다. 매개 [변수에 대한 설명은 로그 처리 데이터 세트에 파일](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) 또는 [변형 데이터](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) 세트 포함 파일을참조하십시오.

   데이터 워크벤치 창에서 데이터 세트 포함 파일을 편집할 때 바로 가기 키를 사용하여 잘라내기(Ctrl+x), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a)을 비롯한 기본 편집 기능을 사용할 수 있습니다. 또한 단축키를 사용하여 구성 파일( [!DNL .cfg])의 텍스트를 복사하여 다른 파일에 붙여넣을 수 있습니다.

1. 변경 내용을 저장하려면 창 **[!UICONTROL (modified)]** 맨 위에 있는 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Profile Manager]> [!DNL User] &lt; **[!UICONTROL Save to]** > ***[!UICONTROL profile name]***&#x200B;을 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트에 포함된 파일이 속하는 상속된 프로필입니다. 데이터 집합 프로필의 동기화 후 데이터의 재처리 또는 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

