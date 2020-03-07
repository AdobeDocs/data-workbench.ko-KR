---
description: 액세스 제어 구성 파일인 Access Control.cfg는 Insight Server가 들어오는 연결 인증서의 특성(OU, CN 등)을 기반으로 파일에 권한을 부여하는 액세스 제어 그룹을 정의합니다.
solution: Insight
title: 액세스 제어 구성
uuid: e0206b43-3c8c-48ec-b663-814f5b663b96
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 액세스 제어 구성{#configuring-access-control}

액세스 제어 구성 파일인 Access Control.cfg는 Insight Server가 들어오는 연결 인증서의 특성(OU, CN 등)을 기반으로 파일에 권한을 부여하는 액세스 제어 그룹을 정의합니다.

**권장 빈도:** 필요에 따라

[!DNL Insight Server] 에 대한 연결의 보안을 관리하기 위해 구성 가능한 액세스 제어 그룹을 [!DNL Insight Server]제공합니다. 액세스 제어 그룹은 다음을 통해 관리 기능을 수행할 수 있는 사용자를 식별합니다 [!DNL Insight].

새 사용자나 새 컴퓨터에 대한 액세스 권한을 제공해야 하는 경우(예: [!DNL Insight Server] 클러스터에 시스템을 추가하는 경우) 액세스 제어 구성 파일을 편집하면 됩니다.
