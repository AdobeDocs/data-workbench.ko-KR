---
description: Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.
title: 변환 구성 파일에 대한 고려 사항
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
exl-id: 7164ccb5-269c-4968-a3b4-1ff046a57f92
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 5%

---

# 변환 구성 파일에 대한 고려 사항{#considerations-for-the-transformation-configuration-file}

Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.

* 이 파일에서 매개 변수를 변경하려면 데이터를 다시 변환해야 합니다.
* 데이터를 다시 처리하는 경우 데이터 워크벤치의 [!DNL Processing Legend]에서 [!DNL Transformation Progress] 매개 변수를 확인할 수 있습니다.

   데이터 재처리 또는 [!DNL Processing Legend,]에 대한 자세한 내용은 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.

* [!DNL CrossRows],  [!DNL ODBCLookup],  [!DNL Sessionize]및  [!DNL AppendURI] 변형은  [!DNL Transformation Dataset Configuration] 파일에서 정의할 때만 작동합니다. 이러한 변형에 대한 자세한 내용은 [데이터 변형](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md)을 참조하십시오.

   >[!NOTE]
   >
   >Adobe에서는 하나 이상의 [!DNL Transformation Dataset Include] 파일에서 데이터 세트 구성의 변형 단계에 대한 변형을 정의하는 것이 좋습니다. 자세한 내용은 [변형 데이터 세트에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace)을 참조하십시오.

* 메모장에서 파일을 열고 편집하여 위에 설명한 매개 변수를 [!DNL Transformation.cfg] 파일에 추가할 수 있습니다. 데이터 워크벤치에서 파일을 다시 열 때 적용한 변경 내용이 모두 나타납니다. 새 매개 변수를 추가할 때 Tab 키가 아닌 Space 키를 사용하여 이전 머리글 수준 오른쪽에 2개의 공백을 들여씁니다.

   데이터 집합 프로필에 대한 데이터 집합 구성 프로세스의 변형 단계에서 발생하는 모든 오류는 데이터 워크벤치의 [!DNL Detailed Status] 인터페이스의 [!DNL Profiles] 노드에 표시됩니다. [!DNL Detailed Status] 인터페이스에 대한 자세한 내용은 *Data Workbench 사용자 안내서*&#x200B;를 참조하십시오.
