---
description: Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.
title: 변환 구성 파일에 대한 고려 사항
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
exl-id: 7164ccb5-269c-4968-a3b4-1ff046a57f92
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 5%

---

# 변환 구성 파일에 대한 고려 사항{#considerations-for-the-transformation-configuration-file}

{{eol}}

Transformation.cfg 파일을 편집할 때 고려해야 할 중요한 정보입니다.

* 이 파일의 매개 변수를 변경하려면 데이터를 다시 변환해야 합니다.
* 데이터를 다시 처리하는 경우 [!DNL Transformation Progress] data workbench의 매개 변수 [!DNL Processing Legend].

   데이터 또는 [!DNL Processing Legend,] 참조 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL CrossRows], [!DNL ODBCLookup], [!DNL Sessionize], 및 [!DNL AppendURI] 변형은 [!DNL Transformation Dataset Configuration] 파일. 이러한 변형에 대한 자세한 내용은 [데이터 변환](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

   >[!NOTE]
   >
   >Adobe은 하나 이상의 데이터 집합 구성의 변형 단계에 대한 변형을 정의할 것을 권장합니다 [!DNL Transformation Dataset Include] 파일. 자세한 내용은 [변형 데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace).

* 위에 설명된 매개 변수를 [!DNL Transformation.cfg] 파일을 열고 메모장에서 편집하여 파일을 엽니다. 사용자가 만들고 저장하는 모든 변경 사항은 Data Workbench에서 파일을 다시 열면 나타납니다. 새 매개 변수를 추가할 때 Space 키(Tab 키 아님)를 사용하여 이전 제목 수준 오른쪽에 있는 두 개의(2) 공백을 들여씁니다.

   데이터 집합 프로필에 대한 데이터 집합 구성 프로세스의 변형 단계 중에 발생하는 모든 오류는 [!DNL Profiles] 노드 [!DNL Detailed Status] data workbench 인터페이스. 에 대한 정보 [!DNL Detailed Status] 인터페이스, 자세한 내용은 *Data Workbench 사용 안내서*.
