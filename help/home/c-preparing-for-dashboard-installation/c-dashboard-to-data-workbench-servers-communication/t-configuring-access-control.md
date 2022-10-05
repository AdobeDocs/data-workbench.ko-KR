---
description: 대시보드에는 Data Workbench 데이터에 액세스하고 표시할 수 있도록 특정 읽기 전용 권한이 필요합니다. 쓰기 권한은 필요하지 않습니다.
title: 대시보드 액세스 제어 구성
uuid: 600b6799-547d-46da-9027-4f64943e2ccd
exl-id: a9ff61bb-c519-4205-8fa8-bfd1986fcd60
source-git-commit: 90b9fff995cb37a62024f454f009e9e0d7b927cd
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---

# 대시보드 액세스 제어 구성{#configuring-dashboard-access-control}

{{eol}}

대시보드에는 Data Workbench 데이터에 액세스하고 표시할 수 있도록 특정 읽기 전용 권한이 필요합니다. 쓰기 권한은 필요하지 않습니다.

액세스 제어 구성에는 편집 작업이 포함됩니다 [!DNL Access Control.cfg] 파일을 업로드하고 Data Workbench 대시보드에 권한을 부여하는 새 그룹을 추가합니다.

1. 편집 [!DNL AccessControl.cfg] 파일(바람직하게는 data workbench workstation 사용).
1. 이름이 인 새 그룹 만들기 *Insight Dashboard 액세스*.
1. 이 그룹의 멤버 아래에서 이 용도로 제공된 적절한 CN을 추가합니다(예: CN:INSIGHT-USER01). 이 CN에 대해서는 Adobe 고객 지원 센터에 문의하십시오.
1. 이 그룹의 읽기 전용 액세스 권한 아래에서 다음을 반영하도록 목록을 수정합니다.

* /프로필/$
* /프로필/
* /Addresses
* /상태/
* /사용자 참조/$

1. 대시보드에 대한 쓰기 권한이 없으므로 읽기-쓰기 액세스 섹션에서 항목을 제거합니다.
1. 변경 내용을 [!DNL AccessControl.cfg] 파일을 서버에 저장하여 권한을 적용할 수 있습니다.
