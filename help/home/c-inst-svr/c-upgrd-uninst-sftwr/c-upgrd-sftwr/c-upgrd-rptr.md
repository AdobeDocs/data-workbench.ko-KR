---
description: Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 지침
solution: Analytics
title: 반복 업그레이드
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---


# 반복 업그레이드{#upgrading-repeater}

Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 지침

다음 방법 중 하나를 사용하여 Platform 4.x 이상 [!DNL Repeater] 에서 업그레이드할 수 있습니다.

* 인사이트와 반복 간 연결 만들기 [!DNL Insight] 에 설명된 [!DNL Repeater] 대로 [와 사이](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)의 연결을 만든 [!DNL Insight] 경우 [!DNL Repeater]로 업그레이드할 수 있습니다. Insight [를 사용하여 반복 업그레이드를 참조하십시오](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -또는-

* 과(와) 간에 연결을 만들 수 없거나 [!DNL Insight] 생성할 수 없는 [!DNL Repeater]경우 업그레이드 파일을 [!DNL Repeater] 컴퓨터에 직접 복사해야 합니다. 파일 [을 복사하여 반복 업그레이드를 참조하십시오](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1).

## Insight를 사용한 반복 업그레이드 {#section-59c24448fd0f45c08abd0245ad746764}

1. 컴퓨터의 경우 [!DNL Insight] 업그레이드 패키지 [!DNL bin] 의 폴더 [!DNL Insight Server] 를 설치된 디렉토리의 [!DNL Temp] 폴더로 [!DNL Insight] 복사합니다.
1. 시작 시간 [!DNL Insight].
1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 업그레이드하려는 아이콘을 마우스 오른쪽 버튼으로 [!DNL Repeater] 클릭하고 을 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]다음을 수행하여 업그레이드 파일을 서버에 업로드합니다.

   1. 폴더를 [!DNL bin] 찾습니다.
   1. Temp 디렉토리에서 [!DNL bin] 폴더에 대한 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>을 선택합니다*.

>[!NOTE]
>
>이 단계가 서버에 있는 동일한 이름의 파일을 덮어쓰도록 하는 메시지가 표시됩니다. 계속하려면 클릭하십시오 **[!UICONTROL Yes]** .

>[!NOTE]
>
>업그레이드를 완료하기 위해 추가 파일을 업로드해야 하는 경우 Adobe에서 [!DNL Repeater] 이에 대한 지침을 제공합니다.

업그레이드 파일을 컴퓨터에 업로드하면 자동으로 [!DNL Repeater] 자동으로 다시 [!DNL Repeater] 시작되고 새 버전이 로드됩니다.

## 파일을 복사하여 반복 업그레이드 {#section-202f2209f6604f19a15d96b517ea1bc1}

1. Adobe에서 제공하는 업그레이드 파일을 엽니다. 이 파일은 업그레이드할 [!DNL .zip] 수 있는 파일입니다 [!DNL Insight Server].
1. 설치한 디렉토리(예: [!DNL Repeater] [!DNL D:\Adobe\Repeater])로 이동합니다.
1. 파일 [!DNL bin] 내의 [!DNL .zip] 폴더를 복사하여 [!DNL Repeater] 설치 디렉토리에 붙여넣어 기존 [!DNL bin] 폴더를 덮어씁니다.

>[!NOTE]
>
>업그레이드를 완료하기 위해 추가 파일을 업로드해야 하는 경우 Adobe에서 [!DNL Insight Server] 이에 대한 지침을 제공합니다.

업그레이드 파일을 컴퓨터에 복사하면 자동으로 [!DNL Repeater] 자동으로 다시 [!DNL Repeater] 시작되고 새 버전이 로드됩니다.
