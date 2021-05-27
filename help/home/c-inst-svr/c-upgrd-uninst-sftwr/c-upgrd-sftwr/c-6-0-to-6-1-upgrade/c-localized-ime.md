---
description: 이제 Data Workbench에서는 국제 언어를 위한 보조 텍스트 입력 프로세스로서 IME(입력 방법 편집기)를 지원합니다.
title: 입력 방법 편집기 설치
uuid: 2a4dc6de-9dd7-4280-b410-fb88a135fe45
exl-id: 3fcc58f5-29a9-427e-831a-44d527614b56,0bdc7d95-b49a-4ca5-9fde-9c1ce2cd14ec,e4e1c016-0544-434a-b82e-fdd2a4af316c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 4%

---

# 입력 방법 편집기 설치{#installing-the-input-method-editor}

이제 Data Workbench에서는 국제 언어를 위한 보조 텍스트 입력 프로세스로서 IME(입력 방법 편집기)를 지원합니다.

IME를 사용하면 지역 언어에 맞는 다양한 방법을 사용하여 국제 문자를 입력할 수 있습니다. Data Workbench에서는 텍스트 필드에 원하는 IME를 열고 사용할 수 있는 입력 대화 상자를 제공합니다.

>[!NOTE]
>
>Data Workbench 6.1 릴리스의 경우 가상 중국어 간체 키보드만 지원됩니다. IME를 통해 다른 언어를 입력하면 예기치 않은 동작이 발생할 수 있습니다.

## IME {#section-5f008d75a7b24119ab6aebc55454f927} 사용

부동 IME 텍스트 입력 기능을 사용하려면

1. 텍스트 입력 영역에 대해 **[!UICONTROL Alt + Space]** 를 클릭합니다.
1. 시스템의 IME를 사용하여 값을 입력합니다.
1. **[!UICONTROL Enter]** 키를 선택하거나 **[!UICONTROL OK]** 버튼을 클릭하여 입력 대화 상자를 닫습니다.

   대화 상자가 사라지고 문자가 선택한 필드에 나타납니다.

**Insight.cfg 파일 업데이트**

IME를 사용하려면 [!DNL Insight.cfg] 파일을 다음 설정으로 업데이트해야 합니다.

```
Localized IME = bool: true
```

이 설정이 구성 파일에 없으면 **[!UICONTROL Alt + Space]** 키를 누르면 IME 기능이 작동하지 않습니다.

**Insight를 다른 언어로 시작:**  시작 화면과 같이 현지화된 자산을 더 잘 지원하고 나중에 여러 언어를 지원하기 위해 Data Workbench에서 로드할 언어를 식별하는 명령줄 인수가 필요합니다. 기본 언어는 영어입니다.

중국어 Data Workbench를 시작하려면 &quot;-zh-cn&quot; 인수를 사용하여 [!DNL Insight.exe]을 호출해야 합니다.

```
Insight.exe -zh-cn
```

이러한 명령줄 인수는 대/소문자를 구분하지 않습니다.
