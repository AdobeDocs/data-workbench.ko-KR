---
description: Log Processing.cfg 파일을 편집할 때 고려할 개념 정보입니다.
title: 로그 처리 구성 파일에 대한 고려 사항
uuid: 2ccedf63-12d9-40e9-912a-aee030191b1e
exl-id: 278a4a10-d382-4d9f-b3f4-bcc4783eb50c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 4%

---

# 로그 처리 구성 파일에 대한 고려 사항{#considerations-for-the-log-processing-configuration-file}

{{eol}}

Log Processing.cfg 파일을 편집할 때 고려할 개념 정보입니다.

* 데이터 세트에 대한 소스가 정의된 후에는 디렉토리 간에 데이터 파일을 이동해서는 안 됩니다. 디렉터리가 받아야 하는 유일한 추가 파일은 Data Workbench 서버에서 센서에서 데이터를 받는 파일입니다.
* 이 파일에서 매개 변수를 변경하려면 모든 데이터를 재처리해야 합니다. 의 Pause 매개 변수 [!DNL Log Processing Mode.cfg] 재처리가 수행되려면 파일을 false로 설정해야 합니다. (이 매개 변수의 기본값은 false이므로 매개 변수를 변경할 필요가 없습니다.) 에 대한 정보 [!DNL Log Processing Mode.cfg] 파일, [추가 구성 파일](../../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* 데이터를 다시 처리하는 경우 Data Workbench의 로그 처리 진행률 매개 변수를 확인할 수 있습니다 [!DNL Processing Legend].

   데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md). 자세한 내용은 [처리 범례](../../../home/c-get-started/c-admin-intrf/c-pro-lgd.md#concept-233e27c9c84c426f8c178a27cc7ff828).

* 다음 [!DNL Log Processing.cfg] 여러 데이터 세트 프로필에서 파일을 공유할 수 있습니다. 에 정의된 변형 [!DNL Log Processing.cfg] 파일은 이 구성 파일을 공유하는 모든 데이터 세트 프로필에 적용됩니다.

   >[!NOTE]
   >
   >Adobe은 하나 이상의 로그 처리에서 로그 처리에 대한 변환을 정의할 것을 권장합니다 [!DNL dataset include] 파일. 자세한 내용은 [로그 처리 데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

* 위에 설명된 매개 변수를 [!DNL Log Processing.cfg] 파일을 열고 메모장에서 편집하여 파일을 엽니다. 사용자가 만들고 저장하는 모든 변경 사항은 Data Workbench에서 파일을 다시 열면 나타납니다. 새 매개 변수를 추가할 때 Space 키(Tab 키 아님)를 사용하여 이전 제목 수준 오른쪽에 있는 두 개의(2) 공백을 들여씁니다.

   데이터 집합 프로필에 대한 데이터 집합 구성 프로세스의 로그 처리 단계 중에 발생하는 모든 오류는 [!DNL Profiles] 노드 [!DNL Detailed Status] data workbench 인터페이스. 에 대한 정보 [!DNL Detailed Status] 인터페이스, 자세한 내용은 *Data Workbench 사용 안내서*.
