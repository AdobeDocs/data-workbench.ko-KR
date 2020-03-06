---
description: Log Processing.cfg 파일을 편집할 때 고려할 개념 정보입니다.
solution: Analytics
title: 로그 처리 구성 파일에 대한 고려 사항
topic: Data workbench
uuid: 2ccedf63-12d9-40e9-912a-aee030191b1e
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 로그 처리 구성 파일에 대한 고려 사항{#considerations-for-the-log-processing-configuration-file}

Log Processing.cfg 파일을 편집할 때 고려할 개념 정보입니다.

* 데이터 세트에 대한 소스가 정의된 후에는 데이터 파일을 디렉터리 간에 이동할 수 없습니다. 디렉토리가 받아야 하는 추가 파일만 센서로부터 데이터를 받는 데이터 워크벤치 서버에서 새로 만들어집니다.
* 이 파일의 매개 변수를 변경하려면 모든 데이터를 다시 처리해야 합니다. 재처리가 수행되려면 [!DNL Log Processing Mode.cfg] 파일의 Pause 매개 변수를 false로 설정해야 합니다. 이 매개 변수의 기본값은 false이므로 매개 변수를 변경할 필요가 없습니다. 파일에 대한 자세한 내용은 추가 [!DNL Log Processing Mode.cfg] 구성 [파일을 참조하십시오](../../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* 데이터를 재처리하는 경우 데이터 워크벤치의 로그 처리 진행률 매개 변수를 확인할 수 [!DNL Processing Legend]있습니다.

   데이터 재처리에 대한 자세한 내용은 재처리 및 [재변형을 참조하십시오](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md). 처리 [범례를 참조하십시오](../../../home/c-get-started/c-admin-intrf/c-pro-lgd.md#concept-233e27c9c84c426f8c178a27cc7ff828).

* 여러 데이터 집합 프로필에서 파일을 공유할 수 [!DNL Log Processing.cfg] 있습니다. 파일에 정의된 [!DNL Log Processing.cfg] 변형이 이 구성 파일을 공유하는 모든 데이터 집합 프로필에 적용됩니다.

   >[!NOTE]
   >
   >하나 이상의 로그 처리 [!DNL dataset include] 파일에서 로그 처리에 대한 변형을 정의하는 것이 좋습니다. 자세한 내용은 로그 처리 데이터 [세트 포함 파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

* 메모장에서 파일을 열고 편집하여 위에 설명된 매개 변수를 [!DNL Log Processing.cfg] 파일에 추가할 수 있습니다. 데이터 워크벤치에서 파일을 다시 열면 변경 사항이 모두 나타납니다. 새 매개 변수를 추가할 때 Tab 키가 아닌 Space 키를 사용하여 이전 제목 수준 오른쪽에 두 개의 공백을 들여씁니다.

   데이터 집합 프로필에 대한 데이터 집합 구성 프로세스의 로그 처리 단계에서 발생하는 모든 오류는 데이터 워크벤치의 인터페이스 [!DNL Profiles] 노드에 표시됩니다 [!DNL Detailed Status] . 인터페이스에 대한 자세한 내용은 [!DNL Detailed Status] 데이터 워크벤치 *사용 안내서를 참조하십시오*.
