---
description: 대시보드를 작동하려면 먼저 대시보드가 SQL Server에 액세스하도록 허용해야 합니다.
solution: Analytics
title: SQL Server 구성
topic: Data workbench
uuid: bdd5f9f5-a69f-4001-9f80-901bd7eae129
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# SQL Server 구성{#configuring-the-sql-server}

대시보드를 작동하려면 먼저 대시보드가 SQL Server에 액세스하도록 허용해야 합니다.

1. SQL Management Studio를 관리자로 엽니다.
1. 마우스 오른쪽 단추를 클릭하고 선택하여 새 로그인을 **[!UICONTROL Logins]** 추가합니다 **[!UICONTROL New Login]**.
1. 전체 응용 프로그램 풀 ID 이름을 입력합니다.

   기본적으로 응용 프로그램 풀 ID는 응용 프로그램 풀 이름을 따릅니다. 선택한 `dashboard`경우 ID가 이름이 지정됩니다 `IIS AppPool\dashboard`. 1.역할을 **[!UICONTROL Server Roles]** 선택하고 **[!UICONTROL dbcreator]** 확인합니다.
1. Click **[!UICONTROL OK]** to add the new user.
