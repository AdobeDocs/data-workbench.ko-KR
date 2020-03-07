---
description: 조건 추가, 제거 또는 복사에 대한 정보입니다.
solution: Analytics
title: 조건을 사용한 작업
topic: Data workbench
uuid: b6f52b40-26aa-429b-9ff5-3f3b9c9d57a9
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 조건을 사용한 작업{#working-with-conditions}

조건 추가, 제거 또는 복사에 대한 정보입니다.

* [데이터 세트 구성 파일에 조건 추가](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-3e2a34db047b462585502f69722f6511)
* [데이터 세트 구성 파일에서 조건 제거](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-677270f93f1648c3a268ca2aea7d4540)
* [조건 복사하기](../../../home/c-dataset-const-proc/c-conditions/c-work-cond.md#section-00617bcf2c274f428686b2ec7f2d1db8)

## 데이터 세트 구성 파일에 조건 추가 {#section-3e2a34db047b462585502f69722f6511}

1. 데이터 집합 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 사용하여 편집할 데이터 집합 구성 파일을 엽니다.

   * 파일을 열려면 로그 처리 [!DNL Log Processing.cfg] 구성 파일 편집을 참조하십시오 [](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5).

   * 파일을 열려면 변환 구성 [!DNL Transformation.cfg] 파일 편집을 참조하십시오 [](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc).

   * 파일을 열려면 데이터 세트 포함 [!DNL Dataset Include] 파일을 참조하십시오 [](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. 데이터 집합 구성 파일에서 정의할 로그 항목 조건 또는 조건 매개 변수를 찾습니다.
1. 매개 변수를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]**&#x200B;클릭합니다. 다음 조건 유형 중 하나를 선택합니다.

   * [!DNL Not Empty]
   * [!DNL String Match]
   * [!DNL Regular Expression]
   * [!DNL Range]
   * [!DNL And]
   * [!DNL Or]
   * [!DNL Neither]
   * [!DNL Compare]

1. 원하는 대로 조건의 매개 변수를 편집합니다. 각 조건의 매개 변수에 대한 설명은 이 부칙의 해당 섹션을 참조하십시오.
1. 변경 내용을 저장하려면 창 **[!UICONTROL (modified)]** 맨 위에 있는 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

1. 로컬에서 변경한 내용을 적용하려면 열에서 파일에 대한 확인 표시를 [!DNL Profile Manager,] 마우스 오른쪽 단추로 클릭한 다음 [!DNL User] > &lt;* **[!UICONTROL Save to]** **[!UICONTROL profile name]***>을 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 파일이 속한 상속된 프로필입니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

## 데이터 세트 구성 파일에서 조건 제거 {#section-677270f93f1648c3a268ca2aea7d4540}

1. 제거할 조건에 해당하는 조건 이름 또는 번호를 마우스 오른쪽 단추로 클릭합니다.
1. &lt; **[!UICONTROL Remove]** * **[!UICONTROL #number]***>을 클릭합니다. 여기서 number는 제거할 조건에 해당하는 번호입니다.

## 조건 복사하기 {#section-00617bcf2c274f428686b2ec7f2d1db8}

조건을 한 위치에서 동일한 파일의 다른 위치로 복사하거나 하나의 데이터 세트 구성 파일에서 다른 위치로 복사할 수 있습니다.

1. 복사하려는 조건에 해당하는 번호나 조건 이름을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]**&#x200B;클릭합니다.
1. 복사된 조건을 배치할 조건 이름 또는 번호를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]**&#x200B;클릭합니다.

