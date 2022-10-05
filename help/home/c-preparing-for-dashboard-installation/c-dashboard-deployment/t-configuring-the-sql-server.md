---
description: 대시보드를 작동하려면 먼저 SQL Server에 액세스할 수 있도록 허용해야 합니다.
title: SQL Server 구성
uuid: bdd5f9f5-a69f-4001-9f80-901bd7eae129
exl-id: 16116cc8-f539-4cf0-ab1d-f2bddd39b38c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# SQL Server 구성{#configuring-the-sql-server}

{{eol}}

대시보드를 작동하려면 먼저 SQL Server에 액세스할 수 있도록 허용해야 합니다.

1. SQL Management Studio를 관리자로 엽니다.
1. 마우스 오른쪽 단추를 클릭하여 새 로그인 추가 **[!UICONTROL Logins]** 및 선택 **[!UICONTROL New Login]**.
1. 전체 응용 프로그램 풀 ID 이름을 입력합니다.

   기본적으로 응용 프로그램 풀 ID는 응용 프로그램 풀의 이름을 따서 이름이 지정됩니다. 만약 `dashboard`를 입력하면 id 이름이 로 지정됩니다. `IIS AppPool\dashboard`. 1. 선택 **[!UICONTROL Server Roles]** 그리고 **[!UICONTROL dbcreator]** 역할.
1. 클릭 **[!UICONTROL OK]** 새 사용자를 추가하려면
