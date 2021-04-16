---
description: 필요한 Microsoft 구성 요소를 설치하는 단계입니다.
title: 필수 구성 요소 설치
uuid: e23fba09-4684-4daf-8426-ea91169b3348
exl-id: d39cb14e-7cce-4088-8301-8ff566c0bde4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 3%

---

# 필수 구성 요소 설치{#installing-required-components}

필요한 Microsoft 구성 요소를 설치하는 단계입니다.

1. Microsoft .NET Framework v4.0을 설치합니다.

   >[!NOTE]
   >
   >IIS 웹 역할을 설치하고 구성한 후에만 설치해야 합니다.

1. 마법사를 따라 설치를 완료하라는 메시지가 표시되면 기본값을 선택합니다.
1. ASP.NET v.4.0 응용 프로그램 풀이 IIS의 **[!UICONTROL Application Pools]** 목록 내에 추가되었는지 확인합니다.
1. Microsoft SQL Server 데이터베이스를 설치합니다.

   관리 도구(Adobe 권장: SQL Server 2008 R2 SP1 - Express Edition)를 사용하여 모든 버전의 SQL Server 2008 또는 2008 R2(Express Edition)를 사용할 수 있습니다. 1. 미리 실행 중인 기존 SQL Server 인스턴스가 없는 일반 설치의 경우 **[!UICONTROL Instance Configuration]** 화면에서 **[!UICONTROL Default Instance]** 옵션을 선택하십시오.
1. 나머지 구성 옵션에 대해 마법사를 따라 설치를 완료하라는 메시지가 표시되면 기본값을 선택합니다.
1. Microsoft Web Deploy v2.0을 설치합니다.

   대부분의 설치에서 **[!UICONTROL Typical]** 설치가 좋습니다. 그러나 원격 배포를 수행하려면 전체 설치를 수행해야 합니다(**[!UICONTROL Complete]** 선택).

   모든 사전 요구 사항이 제대로 설치되면 데이터 워크벤치 서버를 준비하여 대시보드와 통신합니다.
