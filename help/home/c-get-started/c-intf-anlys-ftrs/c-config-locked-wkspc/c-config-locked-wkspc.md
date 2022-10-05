---
description: 특정 사용자만 특정 작업 공간을 변경할 수 있도록 Data Workbench을 구성할 수 있습니다.
title: 잠긴 작업 영역 구성
uuid: 0bb264f6-20b9-43d9-903e-1b2422af21d5
exl-id: e31a786e-064e-4f2c-9bf4-7ceafde814c0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---

# 잠긴 작업 영역 구성{#configure-a-locked-workspace}

{{eol}}

특정 사용자만 특정 작업 공간을 변경할 수 있도록 Data Workbench을 구성할 수 있습니다.

작업 공간이 잠겨 있는 동안 대부분의 시각화에서 항목을 선택하고 테이블의 데이터를 정렬할 수 있지만 그렇지 않으면 작업 공간을 변경할 수 없습니다. 이 기능은 사용자가 작업 공간을 실수로 변경하지 못하도록 합니다.

다음 세 가지 요소가 함께 작동하여 작업 공간의 잠금을 제어합니다.

* **folder.lock 또는 *작업 공간 이름*.lock 파일:** A [!DNL folder.lock] 파일은 작업 공간에서 특정 폴더의 작업 영역을 잠기는지 여부를 지정합니다 [!DNL name.lock] 파일 특정 작업 영역이 잠겨 있는지 여부를 지정합니다.

* **사용자의 [!DNL Insight.cfg] 파일:** 이 매개 변수는 사용자가 잠긴 작업 공간의 잠금을 일시적으로 해제할 수 있는지 여부를 지정합니다.
* **임시 잠금 해제 메뉴 옵션:** 사용자의 [!DNL Insight.cfg] 가 true로 설정되어 있으면 사용자가 잠금을 해제할 수 있도록 잠근 각 작업 공간의 제목 표시줄 메뉴에 이 옵션이 자동으로 표시됩니다.

에 대한 자세한 정보 [!DNL folder.lock] 및 작업 공간 [!DNL name.lock] 파일에서 다음 섹션을 참조하십시오. 잠금 해제 매개 변수 설정에 대한 자세한 내용은 [잠금 해제 매개 변수 설정](../../../../home/c-get-started/c-intf-anlys-ftrs/c-config-locked-wkspc/c-unlck-param.md#concept-b018a85c6217489aa01b17845872df7f). 에 대한 정보 [!DNL Temporarily Unlock menu] 옵션을 참조하십시오. [작업 공간 잠금 해제](../../../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e).
