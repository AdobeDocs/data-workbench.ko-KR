---
description: 프로필 관리자에 적용된 Internal.cfg 파일은 프로필, 차원, 보고서, 작업 영역, 지표 및 필터 관리자에 의한 사용자 정의 프로필 변경을 방지합니다.
title: 워크스테이션에서 프로파일 잠금
uuid: 6b65d7c1-dade-4c6e-9d59-09693e62f3f5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 워크스테이션에서 프로파일 잠금{#locking-profiles-in-the-workstation}

프로필 관리자에 적용된 Internal.cfg 파일은 프로필, 차원, 보고서, 작업 영역, 지표 및 필터 관리자에 의한 사용자 정의 프로필 변경을 방지합니다.

프로필 관리자에서 파일을 사용자 정의 프로필에 저장하여 관리자를 사용할 때 프로필 파일을 수정 및 덮어쓰는 것을 방지할 수 있습니다. **[!DNL Internal.cfg]** 이 구성 파일은 관리자가 작업할 때([관리] > [프로필] **메뉴에서 액세스** ) 사용자가 여러 파일을 덮어쓰지 **못하도록** 합니다.

**프로필 관리자에서 프로필 잠금**

1. 작업 영역에서 관리 > 프로필 **관리자를** 마우스 오른쪽 단추로 **클릭합니다**.

1. 프로필 **관리자에서**&#x200B;마우스 오른쪽 단추를 클릭하고 [로컬로 만들기] **[!DNL Context > Internal.cfg]** 를 **클릭합니다**.

1. 사용자 열에서 확인 표시를 마우스 오른쪽 **단추로** 클릭하고 에 저장합니다 `<custom profile>`.

![](assets/dwb_lock_profiles.png)

**참고**:프로필 관리자에서 프로필 파일을 사용자 정의 프로필에 저장할 때는 관리자가 프로필 파일을 변경할 **[!DNL Internal.cfg]** 수 없습니다. 서버에 **** 저장 명령을 사용하여 작업 영역을 워크플로우에서 서버에 저장할 수 있습니다.