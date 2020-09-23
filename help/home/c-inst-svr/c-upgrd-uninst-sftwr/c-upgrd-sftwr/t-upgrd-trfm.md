---
description: 변형 폴더를 업그레이드하는 절차.
solution: Analytics
title: 변형 업그레이드
uuid: 26e567bc-7571-4317-b77c-2631a163a4b5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---


# 변형 업그레이드{#upgrading-transform}

변형 폴더를 업그레이드하는 절차.

1. 릴리스 패키지의 [!DNL .zip] 파일을 열고 해당 [!DNL Insight Server] 파일 [!DNL Profiles] [!DNL .zip] 내의 폴더를 엽니다.
1. 설치 디렉토리 [!DNL Transform] 의 [!DNL Profiles] 폴더에 [!DNL Insight Server] 폴더를 복사합니다. 이렇게 하면 기존 [!DNL Transform] 폴더를 덮어씁니다.
1. 프로필을 상속하는 각 프로필에 대해 디렉토리 벡터에 [!DNL Transform] [!DNL profile.cfg] 파일에 &quot;변형&quot; 항목이 있는지 확인합니다.
프로필 동기화 후 데이터 재처리가 시작됩니다.
