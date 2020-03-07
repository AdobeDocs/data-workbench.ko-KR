---
description: 특정 사용자만 특정 작업 영역을 변경할 수 있도록 데이터 워크벤치를 구성할 수 있습니다.
solution: Analytics
title: 잠긴 작업 영역 구성
topic: Data workbench
uuid: 0bb264f6-20b9-43d9-903e-1b2422af21d5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 잠긴 작업 영역 구성{#configure-a-locked-workspace}

특정 사용자만 특정 작업 영역을 변경할 수 있도록 데이터 워크벤치를 구성할 수 있습니다.

작업 영역이 잠겨 있는 동안 대부분의 시각화를 선택하여 표에서 데이터를 정렬할 수 있지만 다른 경우에는 작업 영역을 변경할 수 없습니다. 이 기능을 사용하면 사용자가 작업 영역을 의도하지 않게 변경할 수 없습니다.

다음 세 가지 요소가 함께 작동하여 작업 영역의 잠금을 제어합니다.

* **folder.lock 또는&#x200B;*workspace name*.lock 파일:** 파일은 특정 폴더의 작업 영역을 잠글 것인지, 작업 영역 [!DNL folder.lock] [!DNL name.lock] 파일은 특정 작업 영역의 잠금 여부를 지정합니다.

* **사용자[!DNL Insight.cfg]파일의 잠금 해제 매개 변수:** 이 매개 변수는 사용자가 잠긴 작업 영역의 잠금을 일시적으로 해제할 수 있는지 여부를 지정합니다.
* **일시적으로 잠금 해제 메뉴 옵션:** 사용자의 잠금 해제 매개 변수가 true로 [!DNL Insight.cfg] 설정된 경우 이 옵션은 잠긴 각 작업 영역의 제목 표시줄 메뉴에 자동으로 표시되므로 사용자가 잠금을 해제할 수 있습니다.

작업 공간 파일에 대한 자세한 [!DNL folder.lock] 내용은 다음 [!DNL name.lock] 섹션을 참조하십시오. 잠금 해제 매개 변수 설정에 대한 자세한 내용은 잠금 해제 [매개 변수 설정을 참조하십시오](../../../../home/c-get-started/c-intf-anlys-ftrs/c-config-locked-wkspc/c-unlck-param.md#concept-b018a85c6217489aa01b17845872df7f). 옵션에 대한 자세한 내용은 [!DNL Temporarily Unlock menu] 작업 [영역 잠금 해제를 참조하십시오](../../../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e).
