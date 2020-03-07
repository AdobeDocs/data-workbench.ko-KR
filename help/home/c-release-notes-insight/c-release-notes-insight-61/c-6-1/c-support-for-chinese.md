---
description: 이제 데이터 워크벤치 클라이언트 응용 프로그램이 중국어 간체를 지원합니다.
solution: Analytics
title: 중국어 로컬라이제이션 간소화
topic: Data workbench
uuid: ddf4eade-7c5f-4ccf-aa9f-dd8d109a059f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 중국어 로컬라이제이션 간소화{#simplified-chinese-localization}

이제 데이터 워크벤치 클라이언트 응용 프로그램이 중국어 간체를 지원합니다.

**중국어 간체를 설치하려면**:

파일을 구성하고 [!DNL Insight.exe] 지원하기 전에 클라이언트 애플리케이션을 종료해야 합니다.

1. 명령줄 설정에서 [!DNL insight.exe] 파일에 전달하는 단축키를 만듭니다.

   ```
   Insight.exe -zh-cn
   ```

1. 단일 및 2바이트 글꼴 문자를 지원하도록 [!DNL Insight.cfg] 구성합니다.

   데이터 워크벤치에서는 현재 영어 및 중국어 간체를 모두 지원합니다. 다음 두 언어를 모두 지원하는 글꼴을 선택할 수 있습니다.

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial 
   ```

1. 다시 시작 [!DNL Insight.exe].

