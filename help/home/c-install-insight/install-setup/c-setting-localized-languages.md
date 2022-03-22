---
description: 클라이언트 애플리케이션의 언어를 설정하도록 insight.zbin 파일을 설정합니다.
title: 현지화된 언어 insight.zbin 설정
uuid: 7735e183-7ba3-4e11-bfe2-7f87e4c55fc8
exl-id: bb57887f-f213-48a4-9a10-8da7ea33eda5
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---

# 현지화 언어 설정{#setting-up-localized-languages}

클라이언트 애플리케이션의 언어를 설정하도록 insight.zbin 파일을 설정합니다.

## Data Workbench 서버 구성 요소 업데이트 {#section-5d07a081befc4eaa8fdf7fea904e0d48}

관리자는 먼저 이러한 서버 구성 요소를 업데이트하려면 다음 작업을 완료해야 합니다.

1. **Data Workbench 서버 6.x로 업데이트합니다.** 다음을 업데이트하여 지역화를 위한 Data Workbench 서버를 업데이트해야 합니다 [!DNL base\localization\*.zbin] 파일. 이 [!DNL insight.zbin] 그러면 파일이 클라이언트에 복사됩니다.

   An [!DNL insight.zbin] 파일은 설치 폴더에 포함되어 있습니다 [!DNL insight.exe] 파일. 특정 언어를 제공하지 않는 서버에 연결하는 경우 [!DNL .zbin] 파일 다음에 data workbench가 이 파일을 사용하도록 진행합니다.

   백업 [!DNL insight.zbin] 파일은 모든 언어로 제공할 수 있습니다. 따라서 중국어로 Data Workbench를 사용하고 이 언어를 지원하지 않는 서버에 연결하는 경우 서버가 기본 프로필을 변경하고 사용자를 제거하는 경우에도 Data Workbench 클라이언트가 여전히 중국어로 유지됩니다 [!DNL .zbin] 파일의 [!DNL Base/Localization] 폴더를 입력합니다.

1. **Data Workbench 보고서 서버를 업데이트합니다.** 다음 [!DNL insight.zbin] data workbench 보고서 서버의 루트 폴더는 기본적으로 영어로 제공됩니다. 관리자는 을(를) 선택하고 복사해야 합니다 [!DNL .zbin] 업데이트된 보고서 서버 패키지의 파일을 만든 후 data workbench 보고서 서버의 루트 디렉토리에 배치합니다. 클라이언트와 마찬가지로 보고서 서버에도 선택한 언어에 대한 적절한 인수(예: )가 필요합니다 [!DNL Insight.exe -zh-cn]

   1. 보고서 서버 서비스를 중지합니다.
   1. 를 복사합니다. [!DNL Localization] 새 보고서 서버 패키지의 폴더입니다.
   1. 에서 [!DNL Localization] 폴더, 복사 [!DNL Insight.zbin] 파일을 만든 후 보고서 서버의 루트 디렉토리에 배치합니다. [!DNL Insight.exe] 이(가) 있습니다.

   1. 다음과 같은 필요한 인수를 추가합니다. [!DNL insight.exe -zh-cn]
   1. 보고서 서버를 다시 시작합니다.

## Data Workbench 클라이언트 업데이트 {#section-9653d3fcaf2a4337a97b685857e7aeac}

서버를 업데이트한 후 다음 단계에 따라 각 클라이언트를 업데이트합니다.

1. 이 업데이트 중에 클라이언트가 서버에서 업데이트되지 않도록 하려면 [!DNL Insight.cfg] False에 대한 인수입니다.

   ```
   Update Software = bool: false
   ```

1. 클라이언트를 다시 시작합니다.
1. 소프트웨어 및 문서 프로필(SoftDocs 프로필)로 이동하여 필요한 를 다운로드합니다 **[!UICONTROL insight.zbin]** 클라이언트 패키지의 파일: [!DNL Software\Insight Client\Insight_6.1.zip]

1. 이동 [!DNL insight.zbin] 파일이 있는 폴더에 [!DNL insight.exe] 이(가) 있습니다.

1. 이제 클라이언트 파일이 서버에서 업데이트되도록 하려면 [!DNL Insight.cfg] 파일 인수:

   ```
   Update Software = bool: true
   ```

   I

   >[!NOTE]
   >
   >클라이언트가 서버와 동기화되며 업데이트 중임을 알리는 메시지가 표시됩니다. 다운로드가 완료되면 클라이언트를 다시 시작할지 묻는 메시지가 나타납니다.

1. 클릭 **확인** 클라이언트를 다시 시작하려면

다음 메시지가 나타나면 [!DNL zbin] 파일이 [!DNL Insight.exe].

```
Insight Terminated: The backup dictionary file insight.zbin 
is missing.
```

**현지화된 시작 화면**

Data Workbench는 다음 시작 화면 파일을 찾습니다.

* 영어(기본값): [!DNL Base/Images/<version_product> Splash.png]
* 중국어(시작 시 -zh-cn): [!DNL Base/Images/<version_product> Splash zh-cn.png].

시작 화면이 요청되었지만 누락된 경우 Data Workbench가 기본적으로 영어 시작 화면에 액세스합니다.

<!-- <a id="section_91AE5EF234C14652A7B04082A22629AB"></a> -->
