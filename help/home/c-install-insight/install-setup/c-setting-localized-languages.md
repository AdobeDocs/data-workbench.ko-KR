---
description: 클라이언트 응용 프로그램의 언어를 설정하도록 insight.zbin 파일을 설정합니다.
title: 현지화 언어 설정
uuid: 7735e183-7ba3-4e11-bfe2-7f87e4c55fc8
exl-id: bb57887f-f213-48a4-9a10-8da7ea33eda5
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 1%

---

# 현지화 언어 설정{#setting-up-localized-languages}

클라이언트 응용 프로그램의 언어를 설정하도록 insight.zbin 파일을 설정합니다.

## 데이터 워크벤치 서버 구성 요소 {#section-5d07a081befc4eaa8fdf7fea904e0d48} 업데이트

관리자는 이러한 서버 구성 요소를 업데이트하려면 먼저 다음 작업을 완료해야 합니다.

1. **데이터 워크벤치 서버 6.x로 업데이트합니다.** 파일을 업데이트하여 로컬라이제이션용 데이터 워크벤치 서버를  [!DNL base\localization\*.zbin] 업데이트해야 합니다. 이 [!DNL insight.zbin] 파일은 클라이언트에 복사됩니다.

   [!DNL insight.zbin] 파일은 [!DNL insight.exe] 파일과 함께 설치 폴더에 포함됩니다. 언어별 [!DNL .zbin] 파일을 제공하지 않는 서버에 연결하는 경우 데이터 워크벤치는 이 파일을 계속 사용합니다.

   백업 [!DNL insight.zbin] 파일은 모든 언어로 제공할 수 있습니다. 그 결과, 중국어 데이터 워크벤치를 사용하고 이 언어를 지원하지 않는 서버에 연결하면 서버가 기본 프로필을 변경하고 [!DNL Base/Localization] 폴더에서 [!DNL .zbin] 파일을 제거하더라도 데이터 워크벤치 클라이언트는 여전히 중국어 상태가 됩니다.

1. **데이터 워크벤치 보고서 서버를 업데이트합니다.** 데이터 워크벤치 보고서 서버 [!DNL insight.zbin] 의 루트 폴더는 기본적으로 영어로 제공됩니다. 관리자는 업데이트된 보고서 서버 패키지에서 [!DNL .zbin] 파일을 선택하고 복사하여 데이터 워크벤치 보고서 서버의 루트 디렉토리에 저장해야 합니다. 클라이언트와 마찬가지로 보고서 서버에도 선택한 언어에 대한 적절한 인수(예: [!DNL Insight.exe -zh-cn])가 필요합니다.

   1. 보고서 서버 서비스를 중지합니다.
   1. 새 보고서 서버 패키지에서 [!DNL Localization] 폴더를 복사합니다.
   1. [!DNL Localization] 폴더에서 [!DNL Insight.zbin] 파일을 복사하여 [!DNL Insight.exe]이(가) 있는 보고서 서버의 루트 디렉토리에 넣습니다.

   1. [!DNL insight.exe -zh-cn] 같은 필요한 인수를 추가합니다.
   1. 보고서 서버를 다시 시작합니다.

## 데이터 워크벤치 클라이언트 {#section-9653d3fcaf2a4337a97b685857e7aeac} 업데이트

서버를 업데이트한 후 다음 단계에 따라 각 클라이언트를 업데이트합니다.

1. 이 업데이트 중에 클라이언트가 서버에서 업데이트되지 않도록 하려면 [!DNL Insight.cfg] 인수를 False로 설정하십시오.

   ```
   Update Software = bool: false
   ```

1. 클라이언트를 다시 시작합니다.
1. 소프트웨어 및 문서 프로파일(SoftDocs 프로파일)로 이동하여 클라이언트 패키지에서 필요한 **[!UICONTROL insight.zbin]** 파일을 다운로드합니다.[!DNL Software\Insight Client\Insight_6.1.zip]

1. [!DNL insight.zbin] 파일을 [!DNL insight.exe]이(가) 있는 폴더로 이동합니다.

1. 클라이언트 파일이 이제 서버에서 업데이트되도록 하려면 [!DNL Insight.cfg] 파일 인수를 True로 변경합니다.

   ```
   Update Software = bool: true
   ```

   I

   >[!NOTE]
   >
   >클라이언트가 서버와 동기화되고 업데이트되고 있다는 메시지가 표시됩니다. 다운로드가 완료되면 클라이언트를 다시 시작할지 묻는 메시지가 나타납니다.

1. **확인**&#x200B;을 클릭하여 클라이언트를 다시 시작합니다.

다음 메시지가 표시되면 [!DNL zbin] 파일이 [!DNL Insight.exe]과(와) 동일한 위치에 배치되지 않은 것입니다.

```
Insight Terminated: The backup dictionary file insight.zbin 
is missing.
```

**현지화된 시작 화면**

데이터 워크벤치는 다음 시작 화면 파일을 찾습니다.

* 영어(기본값):[!DNL Base/Images/<version_product> Splash.png]
* 중국어(-zh-cn으로 시작하는 경우):[!DNL Base/Images/<version_product> Splash zh-cn.png].

시작 화면이 요청되었지만 누락된 경우 데이터 워크벤치는 기본적으로 영어 시작 화면에 액세스합니다.

<!-- <a id="section_91AE5EF234C14652A7B04082A22629AB"></a> -->
