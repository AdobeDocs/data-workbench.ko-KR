---
description: 이제 Data Workbench에서는 국제 언어를 위한 보조 텍스트 입력 프로세스로서 IME(입력 방법 편집기)를 지원합니다.
title: 입력 방법 편집기 설치
uuid: 2a4dc6de-9dd7-4280-b410-fb88a135fe45
exl-id: 3fcc58f5-29a9-427e-831a-44d527614b56
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 4%

---

# 입력 방법 편집기 설치{#installing-the-input-method-editor}

{{eol}}

이제 Data Workbench에서는 국제 언어를 위한 보조 텍스트 입력 프로세스로서 IME(입력 방법 편집기)를 지원합니다.

IME를 사용하면 지역 언어에 맞는 다양한 방법을 사용하여 국제 문자를 입력할 수 있습니다. Data Workbench에서는 텍스트 필드에 원하는 IME를 열고 사용할 수 있는 입력 대화 상자를 제공합니다.

>[!NOTE]
>
>Data Workbench 6.1 릴리스의 경우 가상 중국어 간체 키보드만 지원됩니다. IME를 통해 다른 언어를 입력하면 예기치 않은 동작이 발생할 수 있습니다.

## IME 사용 {#section-5f008d75a7b24119ab6aebc55454f927}

부동 IME 텍스트 입력 기능을 사용하려면

1. 클릭 **[!UICONTROL Alt + Space]** 텍스트 입력 영역에 대해 지정합니다.
1. 시스템의 IME를 사용하여 값을 입력합니다.
1. 을(를) 선택하여 입력 대화 상자를 닫습니다. **[!UICONTROL Enter]** 키 또는 **[!UICONTROL OK]** 버튼을 클릭합니다.

   대화 상자가 사라지고 문자가 선택한 필드에 나타납니다.

**Insight.cfg 파일 업데이트**

IME를 사용하려면 [!DNL Insight.cfg] 이 설정을 사용하는 파일:

```
Localized IME = bool: true
```

이 설정이 구성 파일에 없으면 **[!UICONTROL Alt + Space]** 는 IME 기능을 사용하지 않습니다.

**다른 언어로 인사이트 시작:** 시작 화면과 같이 지역화된 자산을 더 잘 지원하고 향후에 여러 언어를 지원하기 위해 Data Workbench에서 로드할 언어를 식별하는 명령줄 인수가 필요합니다. 기본 언어는 영어입니다.

중국어 Data Workbench를 시작하려면 다음을 수행해야 합니다 [!DNL Insight.exe] &quot;-zh-cn&quot; 인수 사용:

```
Insight.exe -zh-cn
```

이러한 명령줄 인수는 대/소문자를 구분하지 않습니다.
