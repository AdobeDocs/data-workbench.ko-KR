---
description: 액세스 제어 구성 파일인 Access Control.cfg는 Insight Server가 들어오는 연결 인증서의 특성(OU, CN 등)을 기반으로 파일에 권한을 부여하는 액세스 제어 그룹을 정의합니다.
title: 액세스 제어 구성
uuid: e0206b43-3c8c-48ec-b663-814f5b663b96
exl-id: 2836c907-fc74-4d35-badc-b8f06cd6989f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# 액세스 제어 구성{#configuring-access-control}

{{eol}}

액세스 제어 구성 파일인 Access Control.cfg는 Insight Server가 들어오는 연결 인증서의 특성(OU, CN 등)을 기반으로 파일에 권한을 부여하는 액세스 제어 그룹을 정의합니다.

**권장 빈도:** 필요한 경우

[!DNL Insight Server] 은 구성 가능한 액세스 제어 그룹을 제공하여 연결 보안을 관리합니다 [!DNL Insight Server]. 액세스 제어 그룹은 [!DNL Insight].

새 사용자 또는 새 컴퓨터에 대한 액세스 권한을 제공해야 하는 경우(예: 컴퓨터에 시스템 추가 시) [!DNL Insight Server] 클러스터에서는 액세스 제어 구성 파일을 편집하기만 하면 됩니다.
