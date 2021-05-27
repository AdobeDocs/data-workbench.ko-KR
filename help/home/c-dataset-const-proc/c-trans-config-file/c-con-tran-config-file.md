---
description: Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.
title: 변환 구성 파일에 대한 고려 사항
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
exl-id: 7164ccb5-269c-4968-a3b4-1ff046a57f92
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 5%

---

# 변환 구성 파일에 대한 고려 사항{#considerations-for-the-transformation-configuration-file}

Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.

* 이 파일의 매개 변수를 변경하려면 데이터를 다시 변환해야 합니다.
* 데이터를 다시 처리하는 경우 Data Workbench의 [!DNL Processing Legend]에서 [!DNL Transformation Progress] 매개 변수를 확인할 수 있습니다.

   데이터 또는 [!DNL Processing Legend,] 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.

* [!DNL CrossRows],  [!DNL ODBCLookup],  [!DNL Sessionize]및  [!DNL AppendURI] 변형은 파일에 정의된 경우에만  [!DNL Transformation Dataset Configuration] 작동합니다. 이러한 변형에 대한 자세한 내용은 [데이터 변환](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md)을 참조하십시오.

   >[!NOTE]
   >
   >Adobe은 하나 이상의 [!DNL Transformation Dataset Include] 파일에서 데이터 집합 구성의 변환 단계에 대한 변환을 정의할 것을 권장합니다. 자세한 내용은 [변형 데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace)을 참조하십시오.

* 메모장에서 파일을 열고 편집하여 위에 설명된 매개 변수를 [!DNL Transformation.cfg] 파일에 추가할 수 있습니다. 사용자가 만들고 저장하는 모든 변경 사항은 Data Workbench에서 파일을 다시 열면 나타납니다. 새 매개 변수를 추가할 때 Space 키(Tab 키 아님)를 사용하여 이전 제목 수준 오른쪽에 있는 두 개의(2) 공백을 들여씁니다.

   데이터 집합 프로필에 대한 데이터 집합 구성 프로세스의 변형 단계 동안 발생하는 모든 오류는 Data Workbench에서 [!DNL Detailed Status] 인터페이스의 [!DNL Profiles] 노드에 표시됩니다. [!DNL Detailed Status] 인터페이스에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.
