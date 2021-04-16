---
description: 데이터 워크벤치 데이터에 액세스하고 표시할 수 있으려면 대시보드에 특정 읽기 전용 권한이 필요합니다. 쓰기 권한은 필요하지 않습니다.
title: 액세스 제어 구성
uuid: 600b6799-547d-46da-9027-4f64943e2ccd
exl-id: a9ff61bb-c519-4205-8fa8-bfd1986fcd60
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 6%

---

# 액세스 제어 구성{#configuring-access-control}

데이터 워크벤치 데이터에 액세스하고 표시할 수 있으려면 대시보드에 특정 읽기 전용 권한이 필요합니다. 쓰기 권한은 필요하지 않습니다.

액세스 제어 구성에는 FSU에서 [!DNL Access Control.cfg] 파일을 편집하고 데이터 워크벤치 대시보드에 권한을 부여하는 새 그룹을 추가하는 작업이 포함됩니다.

1. [!DNL AccessControl.cfg] 파일을 편집합니다(데이터 워크벤치 워크스테이션 사용 권장).
1. *Insight 대시보드 액세스*&#x200B;라는 새 그룹을 만듭니다.
1. 이 그룹의 구성원 아래에서 이 용도로 제공된 적절한 CN을 추가합니다(예:CN:INSIGHT-USER01). 이 CN은 Adobe 고객 지원 센터에 문의하십시오.
1. 이 그룹의 읽기 전용 액세스 아래에서 다음을 반영하도록 목록을 수정합니다.

* /프로필/$
* /프로필/
* /주소
* /상태/
* /사용자 참조/$

1. 대시보드에 대한 쓰기 권한이 필요하지 않으므로 읽기-쓰기 액세스 섹션에서 항목을 제거합니다.
1. 사용 권한을 적용하려면 [!DNL AccessControl.cfg] 파일의 변경 내용을 서버에 저장합니다.
