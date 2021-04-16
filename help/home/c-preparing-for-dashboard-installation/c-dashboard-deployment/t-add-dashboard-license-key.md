---
description: 대시보드 제품에는 Adobe ClientCare에서 제공하는 라이센스가 필요합니다.
title: 대시보드 라이선스 키 추가
uuid: 51ec87a8-e9cc-4aa1-8d13-a79612a13d17
exl-id: bf532fb0-9287-4c15-aa4c-07f7bd0fdba7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 12%

---

# 대시보드 라이선스 키 추가{#add-dashboard-license-key}

대시보드 제품에는 Adobe ClientCare에서 제공하는 라이센스가 필요합니다.

1. **[!UICONTROL SQL Management Studio]**&#x200B;을(를) 관리자로 엽니다.
1. 대시보드에서 만든 데이터베이스(예: thinclientdb)를 엽니다.
1. **[!UICONTROL Configuration]** 테이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Edit Top 200 Rows]** 을 클릭합니다.
1. **[!UICONTROL licenseKey]** 필드를 찾고 Adobe ClientCare에서 제공하는 키를 **[!UICONTROL Value]** 열에 입력합니다.
1. **[!UICONTROL IIS Manager Console]**&#x200B;에서 **[!UICONTROL Application Pool]**&#x200B;을 다시 시작합니다.
