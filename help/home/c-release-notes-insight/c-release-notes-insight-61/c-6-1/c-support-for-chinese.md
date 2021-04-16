---
description: 이제 데이터 워크벤치 클라이언트 응용 프로그램이 중국어 간체를 지원합니다.
title: 중국어 로컬라이제이션 간소화
uuid: ddf4eade-7c5f-4ccf-aa9f-dd8d109a059f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# 중국어 현지화 간소화{#simplified-chinese-localization}

이제 데이터 워크벤치 클라이언트 응용 프로그램이 중국어 간체를 지원합니다.

**중국어 간체를 설치하려면**:

[!DNL Insight.exe] 및 지원 파일을 구성하기 전에 클라이언트 응용 프로그램을 종료해야 합니다.

1. 명령줄 설정을 [!DNL insight.exe] 파일로 전달하는 단축키를 만듭니다.

   ```
   Insight.exe -zh-cn
   ```

1. 단일 및 더블바이트 글꼴 문자를 지원하도록 [!DNL Insight.cfg]을 구성합니다.

   데이터 워크벤치는 현재 영어 및 중국어 간체를 모두 지원합니다. 다음 언어 모두를 지원하는 글꼴을 선택할 수 있습니다.

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial 
   ```

1. 다시 시작 [!DNL Insight.exe].

