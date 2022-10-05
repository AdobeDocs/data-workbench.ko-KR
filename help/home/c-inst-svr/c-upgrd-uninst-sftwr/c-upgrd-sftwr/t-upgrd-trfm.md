---
description: 변형 폴더를 업그레이드하는 단계입니다.
title: 변형 업그레이드
uuid: 26e567bc-7571-4317-b77c-2631a163a4b5
exl-id: b5e21862-caf1-42e4-9247-c870d7b3180e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# 변형 업그레이드{#upgrading-transform}

{{eol}}

변형 폴더를 업그레이드하는 단계입니다.

1. 를 엽니다. [!DNL .zip] 파일 [!DNL Insight Server] 릴리스 패키지를 열고 [!DNL Profiles] 해당 내의 폴더 [!DNL .zip] 파일.
1. 를 복사합니다. [!DNL Transform] 폴더 [!DNL Profiles] 폴더의 [!DNL Insight Server] 설치 디렉토리. 이렇게 하면 기존 파일을 덮어씁니다. [!DNL Transform] 폴더를 입력합니다.
1. 를 상속하는 각 프로필에 대해 [!DNL Transform] 프로필에서 [!DNL profile.cfg] 파일의 디렉토리 벡터에 &quot;변환&quot; 항목이 있습니다.
프로필 동기화 후 데이터 재처리가 시작됩니다.
