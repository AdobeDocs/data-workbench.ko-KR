---
description: Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.
solution: Analytics
title: 변환 구성 파일에 대한 고려 사항
topic: Data workbench
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 변환 구성 파일에 대한 고려 사항{#considerations-for-the-transformation-configuration-file}

Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.

* 이 파일에서 매개 변수를 변경하려면 데이터를 다시 변환해야 합니다.
* 데이터를 재처리하는 경우 데이터 워크벤치의 [!DNL Transformation Progress] 매개 변수를 확인할 수 [!DNL Processing Legend]있습니다.

   데이터 재처리 또는 재처리 및 재변형을 [!DNL Processing Legend,] 참조하십시오 [](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL CrossRows], [!DNL ODBCLookup][!DNL Sessionize]및 [!DNL AppendURI] 변형은 [!DNL Transformation Dataset Configuration] 파일에 정의된 경우에만 작동합니다. 이러한 변형에 대한 자세한 내용은 데이터 [변형을 참조하십시오](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

   >[!NOTE]
   >
   >하나 이상의 [!DNL Transformation Dataset Include] 파일에서 데이터 세트 구성의 변형 단계를 정의하는 것이 좋습니다. 자세한 내용은 변형 데이터 [세트 포함 파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace).

* 메모장에서 파일을 열고 편집하여 위에 설명된 매개 변수를 [!DNL Transformation.cfg] 파일에 추가할 수 있습니다. 데이터 워크벤치에서 파일을 다시 열면 변경 사항이 모두 나타납니다. 새 매개 변수를 추가할 때 Tab 키가 아닌 Space 키를 사용하여 이전 제목 수준 오른쪽에 두 개의 공백을 들여씁니다.

   데이터 집합 프로필에 대한 데이터 집합 구성 프로세스의 변형 단계에서 발생하는 오류는 데이터 워크벤치의 인터페이스 [!DNL Profiles] 노드에 표시됩니다 [!DNL Detailed Status] . 인터페이스에 대한 자세한 내용은 [!DNL Detailed Status] 데이터 워크벤치 *사용 안내서를 참조하십시오*.

