---
description: Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 방법 지침
solution: Insight
title: 반복 업그레이드
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 반복 업그레이드{#upgrading-repeater}

Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 방법 지침

다음 방법 중 하나를 사용하여 Platform 4.x 이상에서 업그레이드할 [!DNL Repeater] 수 있습니다.

* 인사이트와 반복 간의 연결 만들기에 설명된 [!DNL Insight] 것과 [!DNL Repeater][사이의 연결을 만든 경우](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)를 [!DNL Insight] 사용하여 업그레이드할 수 있습니다 [!DNL Repeater]. Insight [를 사용하여 반복 업그레이드를 참조하십시오](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -또는-

* 과(와) 사이에 연결을 만들 수 없거나 [!DNL Insight] 만들지 않은 [!DNL Repeater]경우 업그레이드 파일을 [!DNL Repeater] 컴퓨터에 직접 복사해야 합니다. 파일을 [복사하여 반복 업그레이드를 참조하십시오](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1).

## Insight를 사용하여 반복 업그레이드 {#section-59c24448fd0f45c08abd0245ad746764}

1. 컴퓨터에서 [!DNL Insight] 업그레이드 패키지에서 설치 디렉토리의 [!DNL bin] 폴더로 폴더를 [!DNL Insight Server] [!DNL Temp] [!DNL Insight] 복사합니다.
1. Start [!DNL Insight].
1. &#x200B;> [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 업그레이드하려는 아이콘을 마우스 오른쪽 단추로 [!DNL Repeater] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]다음을 수행하여 업그레이드 파일을 서버에 업로드합니다.

   1. 폴더를 [!DNL bin] 찾습니다.
   1. 임시 디렉토리에서 [!DNL bin] 폴더의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>*&#x200B;을 선택합니다.

>[!NOTE]
>
>이 단계에서 서버에 있는 동일한 이름의 파일을 덮어쓰도록 하는 메시지가 표시됩니다. 계속하려면 을 **[!UICONTROL Yes]** 클릭합니다.

>[!NOTE]
>
>업그레이드를 완료하기 위해 추가 파일을 업로드해야 하는 경우 Adobe에서 [!DNL Repeater] 이에 대한 지침을 제공합니다.

업그레이드 파일을 [!DNL Repeater] [!DNL Repeater] 컴퓨터에 업로드하면 자동으로 다시 시작되고 새 버전이 로드됩니다.

## 파일을 복사하여 반복 업그레이드 {#section-202f2209f6604f19a15d96b517ea1bc1}

1. Adobe에서 제공하는 업그레이드 파일을 엽니다. 이 파일은 업그레이드할 수 있는 [!DNL .zip] 파일입니다 [!DNL Insight Server].
1. 설치한 디렉토리 [!DNL Repeater] (예: [!DNL D:\Adobe\Repeater])로 이동합니다.
1. 파일 내의 [!DNL bin] 폴더를 [!DNL .zip] 복사하여 [!DNL Repeater] 설치 디렉토리에 붙여넣어 기존 [!DNL bin] 폴더를 덮어씁니다.

>[!NOTE]
>
>업그레이드를 완료하기 위해 추가 파일을 업로드해야 하는 경우 Adobe에서 [!DNL Insight Server] 이에 대한 지침을 제공합니다.

업그레이드 파일을 [!DNL Repeater] [!DNL Repeater] 컴퓨터에 복사하면 자동으로 다시 시작되고 새 버전이 로드됩니다.
