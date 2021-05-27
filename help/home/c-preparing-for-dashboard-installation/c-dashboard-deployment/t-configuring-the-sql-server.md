---
description: 대시보드를 작동하려면 먼저 SQL Server에 액세스할 수 있도록 허용해야 합니다.
title: SQL Server 구성
uuid: bdd5f9f5-a69f-4001-9f80-901bd7eae129
exl-id: 16116cc8-f539-4cf0-ab1d-f2bddd39b38c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# SQL Server 구성{#configuring-the-sql-server}

대시보드를 작동하려면 먼저 SQL Server에 액세스할 수 있도록 허용해야 합니다.

1. SQL Management Studio를 관리자로 엽니다.
1. **[!UICONTROL Logins]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL New Login]** 을 선택하여 새 로그인을 추가합니다.
1. 전체 응용 프로그램 풀 ID 이름을 입력합니다.

   기본적으로 응용 프로그램 풀 ID는 응용 프로그램 풀의 이름을 따서 이름이 지정됩니다. `dashboard`을 선택하면 ID의 이름이 `IIS AppPool\dashboard`로 지정됩니다. 1. **[!UICONTROL Server Roles]** 을 선택하고 **[!UICONTROL dbcreator]** 역할을 선택합니다.
1. **[!UICONTROL OK]** 을 클릭하여 새 사용자를 추가합니다.
