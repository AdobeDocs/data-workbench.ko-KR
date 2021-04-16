---
description: Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 방법 지침
title: 반복 업그레이드
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
exl-id: f81fa79e-f660-48fd-b2ff-419961d49c55
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 반복 업그레이드{#upgrading-repeater}

Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 방법 지침

다음 방법 중 하나를 사용하여 플랫폼 4.x 이상에서 [!DNL Repeater]을(를) 업그레이드할 수 있습니다.

* [인사이트와 반복 사이의 연결 만들기](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)에 설명된 대로 [!DNL Insight]과 [!DNL Repeater] 사이에 연결을 만든 경우 [!DNL Insight]를 사용하여 [!DNL Repeater]를 업그레이드할 수 있습니다. [Insight](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764)를 사용하여 반복 업그레이드를 참조하십시오.

   -또는-

* [!DNL Insight]과 [!DNL Repeater] 사이에 연결할 수 없거나 연결을 만들지 않은 경우 업그레이드 파일을 [!DNL Repeater] 컴퓨터에 직접 복사해야 합니다. [파일을 복사하여 반복 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1)를 참조하십시오.

## Insight {#section-59c24448fd0f45c08abd0245ad746764}을(를) 사용하여 반복 업그레이드

1. [!DNL Insight] 컴퓨터에서 [!DNL Insight Server] 업그레이드 패키지의 [!DNL bin] 폴더를 [!DNL Insight]이(가) 설치된 디렉토리의 [!DNL Temp] 폴더로 복사합니다.
1. 시작 시간 [!DNL Insight].
1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 업그레이드하려는 [!DNL Repeater] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]**&#x200B;을 클릭합니다.
1. [!DNL Server Files Manager]에서 다음을 수행하여 업그레이드 파일을 서버에 업로드합니다.

   1. [!DNL bin] 폴더를 찾습니다.
   1. 임시 디렉토리에서 [!DNL bin] 폴더의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.

>[!NOTE]
>
>이 단계가 서버에 있는 동일한 이름의 파일을 덮어쓰도록 하는 메시지가 표시됩니다. 계속하려면 **[!UICONTROL Yes]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>[!DNL Repeater] 업그레이드를 완료하기 위해 추가 파일을 업로드해야 하는 경우 Adobe에서 이에 대한 지침을 제공합니다.

업그레이드 파일을 [!DNL Repeater] 컴퓨터에 업로드하면 [!DNL Repeater]이 자동으로 다시 시작하고 새 버전을 로드합니다.

## {#section-202f2209f6604f19a15d96b517ea1bc1} 파일을 복사하여 반복 업그레이드

1. Adobe에서 제공하는 업그레이드 파일을 엽니다. 이 파일은 [!DNL Insight Server] 업그레이드를 위한 [!DNL .zip] 파일입니다.
1. [!DNL Repeater](예: [!DNL D:\Adobe\Repeater])을 설치한 디렉토리로 이동합니다.
1. [!DNL .zip] 파일 내에 [!DNL bin] 폴더를 복사하여 [!DNL Repeater] 설치 디렉토리에 붙여 넣어 기존 [!DNL bin] 폴더를 덮어씁니다.

>[!NOTE]
>
>[!DNL Insight Server] 업그레이드를 완료하기 위해 추가 파일을 업로드해야 하는 경우 Adobe에서 이에 대한 지침을 제공합니다.

업그레이드 파일을 [!DNL Repeater] 컴퓨터에 복사하면 [!DNL Repeater]이 자동으로 다시 시작하고 새 버전을 로드합니다.
