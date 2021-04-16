---
description: 변형 폴더를 업그레이드하는 절차.
title: 변형 업그레이드
uuid: 26e567bc-7571-4317-b77c-2631a163a4b5
exl-id: b5e21862-caf1-42e4-9247-c870d7b3180e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# 변형 업그레이드{#upgrading-transform}

변형 폴더를 업그레이드하는 절차.

1. [!DNL Insight Server] 릴리스 패키지의 [!DNL .zip] 파일을 열고 해당 [!DNL .zip] 파일 내에서 [!DNL Profiles] 폴더를 엽니다.
1. [!DNL Transform] 폴더를 [!DNL Insight Server] 설치 디렉토리의 [!DNL Profiles] 폴더에 복사합니다. 이렇게 하면 기존 [!DNL Transform] 폴더를 덮어씁니다.
1. [!DNL Transform] 프로필을 상속하는 각 프로필에 대해 [!DNL profile.cfg] 파일에 디렉터리 벡터에 &quot;변형&quot; 항목이 있는지 확인합니다.
프로필 동기화 후 데이터 재처리가 시작됩니다.
