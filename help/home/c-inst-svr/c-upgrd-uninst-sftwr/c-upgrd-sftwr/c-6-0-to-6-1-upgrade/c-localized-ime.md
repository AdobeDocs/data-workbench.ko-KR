---
description: 이제 데이터 워크벤치에서는 국제 언어에 대한 보조 텍스트 입력 프로세스로 IME(Input Method Editor)를 지원합니다.
solution: Analytics
title: 입력 방법 편집기 설치
topic: Data workbench
uuid: 2a4dc6de-9dd7-4280-b410-fb88a135fe45
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 입력 방법 편집기 설치{#installing-the-input-method-editor}

이제 데이터 워크벤치에서는 국제 언어에 대한 보조 텍스트 입력 프로세스로 IME(Input Method Editor)를 지원합니다.

IME 파섹 데이터 워크벤치에서는 텍스트 필드를 열고 원하는 IME를 사용할 수 있는 입력 대화 상자를 제공합니다.

>[!NOTE]
>
>데이터 워크벤치 6.1 릴리스의 경우 가상 중국어 간체 키보드만 지원됩니다. IME 파섹

## IME 사용 {#section-5f008d75a7b24119ab6aebc55454f927}

부동 IME 텍스트 입력 기능을 사용하려면:

1. 텍스트 입력 영역을 **[!UICONTROL Alt + Space]** 클릭합니다.
1. 시스템의 IME를 사용하여 값을 입력합니다.
1. 키를 선택하거나 **[!UICONTROL Enter]** **[!UICONTROL OK]** 단추를 클릭하여 입력 대화 상자를 닫습니다.

   대화 상자가 사라지고 선택한 필드에 문자가 나타납니다.

**Insight.cfg 파일 업데이트**

IME를 사용하려면 다음 설정으로 [!DNL Insight.cfg] 파일을 업데이트해야 합니다.

```
Localized IME = bool: true
```

이 설정이 구성 파일에 없으면 키를 누르면 IME 기능이 작동하지 **[!UICONTROL Alt + Space]** 않습니다.

**다른 언어로 인사이트 시작:** 시작 화면과 같은 현지화된 에셋을 보다 효과적으로 지원하고 나중에 여러 언어를 지원하기 위해 데이터 워크벤치는 로드할 언어를 식별하는 명령줄 인수를 필요로 합니다. 기본 언어는 영어입니다.

중국어 간체로 데이터 워크벤치를 시작하려면 &quot;-zh-cn&quot; 인수로 [!DNL Insight.exe] 호출해야 합니다.

```
Insight.exe -zh-cn
```

이러한 명령줄 인수는 대/소문자를 구분하지 않습니다.
