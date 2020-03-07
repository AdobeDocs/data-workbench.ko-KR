---
description: 필요한 Microsoft 구성 요소를 설치하는 단계입니다.
solution: Analytics
title: 필수 구성 요소 설치
topic: Data workbench
uuid: e23fba09-4684-4daf-8426-ea91169b3348
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 필수 구성 요소 설치{#installing-required-components}

필요한 Microsoft 구성 요소를 설치하는 단계입니다.

1. Microsoft .NET Framework v4.0을 설치합니다.

   >[!NOTE]
   >
   >IIS 웹 역할을 설치하고 구성한 후에만 설치해야 합니다.

1. 마법사를 따라 설치를 완료하라는 메시지가 표시되는 기본값을 선택합니다.
1. ASP.NET v.4.0 응용 프로그램 풀이 IIS의 **[!UICONTROL Application Pools]** 목록 내에 추가되었는지 확인합니다.
1. Microsoft SQL Server 데이터베이스를 설치합니다.

   관리 도구(SQL Server 2008 R2 SP1 - Express Edition 권장)와 함께 모든 버전의 SQL Server 2008 또는 2008 R2(Express 지원)를 사용하십시오. 1.미리 실행 중인 기존 SQL Server 인스턴스가 없는 일반 설치의 경우 **[!UICONTROL Default Instance]** **[!UICONTROL Instance Configuration]** 화면에서 옵션을 선택하십시오.
1. 나머지 구성 옵션의 경우 마법사를 따라 설치를 완료하라는 메시지가 표시되면 기본값을 선택합니다.
1. Microsoft Web Deploy v2.0을 설치합니다.

   대부분의 설치에서는 **[!UICONTROL Typical]** 설치가 좋습니다. 그러나 원격 배포를 수행하려면 전체 설치를 수행해야 합니다(선택 **[!UICONTROL Complete]**).

   모든 사전 요구 사항이 제대로 설치되면 대시보드와 통신할 수 있도록 데이터 워크벤치 서버를 준비할 수 있습니다.
