---
description: 대시보드에는 데이터 워크벤치 데이터에 액세스하고 표시할 수 있는 특정 읽기 전용 권한이 필요합니다. 쓰기 권한은 필요하지 않습니다.
solution: Analytics
title: 액세스 제어 구성
topic: Data workbench
uuid: 600b6799-547d-46da-9027-4f64943e2ccd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 액세스 제어 구성{#configuring-access-control}

대시보드에는 데이터 워크벤치 데이터에 액세스하고 표시할 수 있는 특정 읽기 전용 권한이 필요합니다. 쓰기 권한은 필요하지 않습니다.

액세스 제어 구성에는 FSU에서 [!DNL Access Control.cfg] 파일을 편집하고 데이터 워크벤치 대시보드에 권한을 부여하는 새 그룹을 추가하는 작업이 포함됩니다.

1. 파일을 편집합니다(가급적이면 데이터 워크벤치 워크스테이션 사용). [!DNL AccessControl.cfg]
1. Insight 대시보드 액세스라는 새 *그룹을 만듭니다*.
1. 이 그룹의 구성원 아래에서 이 용도로 제공된 적절한 CN을 추가합니다(예:CN:INSIGHT-USER01). 이 CN은 Adobe 고객 지원 센터에 문의하십시오.
1. 이 그룹의 읽기 전용 액세스 아래에서 다음을 반영하도록 목록을 수정합니다.

* /Profiles/$
* /Profiles/
* /주소
* /상태/
* /사용자 참조/$

1. 대시보드에 대한 쓰기 권한이 필요하지 않으므로 읽기-쓰기 액세스 섹션에서 항목을 제거합니다.
1. 파일에 대한 변경 내용을 서버에 저장하여 권한을 적용할 수 [!DNL AccessControl.cfg] 있습니다.
