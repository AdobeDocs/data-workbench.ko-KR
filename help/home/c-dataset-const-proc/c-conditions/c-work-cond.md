---
description: 조건 추가, 제거 또는 복사에 대한 정보입니다.
title: 조건 사용
uuid: b6f52b40-26aa-429b-9ff5-3f3b9c9d57a9
exl-id: 0792b308-aa0b-4741-be0c-4f7cc28f3e09
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---

# 조건 사용{#working-with-conditions}

조건 추가, 제거 또는 복사에 대한 정보입니다.

* [데이터 세트 구성 파일에 조건을 추가하려면](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-3e2a34db047b462585502f69722f6511)
* [데이터 세트 구성 파일에서 조건을 제거하려면](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-677270f93f1648c3a268ca2aea7d4540)
* [조건을 복사하려면](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-00617bcf2c274f428686b2ec7f2d1db8)

## 데이터 집합 구성 파일 {#section-3e2a34db047b462585502f69722f6511}에 조건을 추가하려면

1. 데이터 집합 프로필에서 작업하는 동안 [!DNL Profile Manager]을 사용하여 편집할 데이터 집합 구성 파일을 엽니다.

   * [!DNL Log Processing.cfg] 파일을 열려면 [로그 처리 구성 파일 편집](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5)을 참조하십시오.

   * [!DNL Transformation.cfg] 파일을 열려면 [변형 구성 파일 편집](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc)을 참조하십시오.

   * [!DNL Dataset Include] 파일을 열려면 [데이터 세트에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오.

1. 데이터 집합 구성 파일에서 정의할 로그 항목 조건 또는 조건 매개 변수를 찾습니다.
1. 매개 변수를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]**&#x200B;을 클릭합니다. 다음 조건 유형 중 하나를 선택합니다.

   * [!DNL Not Empty]
   * [!DNL String Match]
   * [!DNL Regular Expression]
   * [!DNL Range]
   * [!DNL And]
   * [!DNL Or]
   * [!DNL Neither]
   * [!DNL Compare]

1. 원하는 대로 조건의 매개 변수를 편집합니다. 각 조건의 매개 변수에 대한 설명은 이 부록의 적절한 섹션을 참조하십시오.
1. 변경 내용을 저장하려면 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager,] 열에서 해당 파일의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > &lt;* **[!UICONTROL profile name]***>을 클릭합니다. 여기서 프로필 이름은 파일이 속한 데이터 세트 프로필 또는 상속된 프로필의 이름입니다.[!DNL User]

   >[!NOTE]
   >
   >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰여지기 때문에 수정된 구성 파일을 Adobe에서 제공하는 내부 프로파일에 저장하지 마십시오.

## 데이터 집합 구성 파일 {#section-677270f93f1648c3a268ca2aea7d4540}에서 조건을 제거하려면

1. 제거할 조건에 해당하는 조건 이름 또는 번호를 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>을 클릭합니다. 여기서 숫자는 제거할 조건에 해당하는 숫자입니다.

## 조건 {#section-00617bcf2c274f428686b2ec7f2d1db8}을 복사하려면

조건을 한 위치에서 동일한 파일의 다른 위치로 복사하거나 하나의 데이터 세트 구성 파일에서 다른 위치로 복사할 수 있습니다.

1. 복사할 조건에 해당하는 조건 이름 또는 번호를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]** 을 클릭합니다.
1. 복사된 조건을 배치할 아래 조건의 이름 또는 번호를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]**&#x200B;을 클릭합니다.
