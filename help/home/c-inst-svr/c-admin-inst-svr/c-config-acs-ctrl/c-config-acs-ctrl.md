---
description: 액세스 제어 구성 파일인 Access Control.cfg는 Insight 서버가 들어오는 연결 인증서의 특성(OU, CN 등)을 기반으로 파일에 권한을 부여하는 액세스 제어 그룹을 정의합니다.
title: 액세스 제어 구성
uuid: e0206b43-3c8c-48ec-b663-814f5b663b96
exl-id: 2836c907-fc74-4d35-badc-b8f06cd6989f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# 액세스 제어 구성{#configuring-access-control}

액세스 제어 구성 파일인 Access Control.cfg는 Insight 서버가 들어오는 연결 인증서의 특성(OU, CN 등)을 기반으로 파일에 권한을 부여하는 액세스 제어 그룹을 정의합니다.

**권장 빈도:** 필요에 따라

[!DNL Insight Server] 에 대한 연결의 보안을 관리하기 위해 구성 가능한 액세스 제어 그룹을 제공합니다 [!DNL Insight Server]. 액세스 제어 그룹은 [!DNL Insight]을(를) 통해 관리 기능을 수행할 수 있는 사용자를 식별합니다.

새 사용자나 새 컴퓨터에 대한 액세스 권한을 제공해야 하는 경우(예: [!DNL Insight Server] 클러스터에 컴퓨터를 추가하는 경우) 액세스 제어 구성 파일을 편집하기만 하면 됩니다.
