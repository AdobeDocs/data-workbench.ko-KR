---
description: 보고서 포털에서 사용자를 인증하는 데 필요한 정보가 포함된 데이터베이스에 쓸 수 있도록 하려면 데이터베이스에 대한 적절한 권한을 설정해야 합니다.
title: 데이터베이스에 대한 권한 설정
uuid: 747d1adc-bfc9-4f54-a2b1-ae5e12dd82a2
exl-id: 901cf702-633c-4660-b1bd-4937d0c3293c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 10%

---

# 데이터베이스에 대한 권한 설정{#set-permissions-for-the-database}

보고서 포털에서 사용자를 인증하는 데 필요한 정보가 포함된 데이터베이스에 쓸 수 있도록 하려면 데이터베이스에 대한 적절한 권한을 설정해야 합니다.

1. IIS가 실행 중인 컴퓨터에서 \*PortalName*\data\users.mdb으로 이동합니다.
1. **[!UICONTROL users.mdb]** 파일을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Properties]** 을 선택합니다.
1. [!DNL Security] 탭의 그룹 또는 사용자 이름에서 **[!UICONTROL Users]**&#x200B;을 클릭합니다.
1. [!DNL Permission for User]의 쓰기 행에서 **[!UICONTROL Allow]**&#x200B;을 선택합니다.
1. **[!UICONTROL OK]** 을 클릭하고 [!DNL Properties] 대화 상자를 닫습니다.
