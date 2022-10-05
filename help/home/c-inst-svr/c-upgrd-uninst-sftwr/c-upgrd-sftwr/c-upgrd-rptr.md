---
description: Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 지침
title: 반복 업그레이드
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
exl-id: f81fa79e-f660-48fd-b2ff-419961d49c55
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 반복 업그레이드{#upgrading-repeater}

{{eol}}

Insight를 사용하여 반복을 업그레이드하거나 파일을 복사하여 업그레이드하는 지침

다음 방법 중 하나를 사용하여 업그레이드할 수 있습니다 [!DNL Repeater] 플랫폼 4.x 이상:

* 다음 사이에 연결을 만든 경우 [!DNL Insight] 및 [!DNL Repeater] 에 설명된 대로 [Insight와 반복 간의 연결 만들기](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118), 다음 사용 가능 [!DNL Insight] 업그레이드하려면 [!DNL Repeater]. 자세한 내용은 [Insight를 사용하여 반복 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -또는-

* 연결할 수 없거나 만들 수 없는 경우 [!DNL Insight] 및 [!DNL Repeater]로 업그레이드 파일을 직접 [!DNL Repeater] 시스템. 자세한 내용은 [파일을 복사하여 반복 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1).

## Insight를 사용하여 반복 업그레이드 {#section-59c24448fd0f45c08abd0245ad746764}

1. 설정 [!DNL Insight] 컴퓨터, 복사 [!DNL bin] 폴더의 [!DNL Insight Server] 패키지를 [!DNL Temp] 디렉토리의 폴더 [!DNL Insight] 가 설치되어 있습니다.
1. 시작 [!DNL Insight].
1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Repeater] 업그레이드하려는 경우 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 눌러 업그레이드 파일을 서버에 업로드합니다.

   1. 을(를) 찾습니다 [!DNL bin] 폴더를 입력합니다.
   1. 에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL bin] Temp 디렉토리의 폴더를 선택하고 **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>이 단계에서 서버에 있는 것과 동일한 이름의 파일을 덮어쓰도록 하는 메시지가 표시됩니다. 클릭 **[!UICONTROL Yes]** 계속하십시오.

>[!NOTE]
>
>완료하기 위해 추가 파일을 업로드해야 하는 경우 [!DNL Repeater] 업그레이드하면 Adobe에서 이에 대한 지침을 제공합니다.

업그레이드 파일을 [!DNL Repeater] 머신, [!DNL Repeater] 자동으로 자신을 다시 시작하고 새 버전을 로드합니다.

## 파일을 복사하여 반복 업그레이드 {#section-202f2209f6604f19a15d96b517ea1bc1}

1. Adobe에서 제공한 업그레이드 파일을 엽니다. 이 파일은 [!DNL .zip] 업그레이드 파일 [!DNL Insight Server].
1. 설치한 디렉토리로 이동합니다 [!DNL Repeater] (예: [!DNL D:\Adobe\Repeater]).
1. 를 복사합니다. [!DNL bin] 폴더 내 [!DNL .zip] 파일에 붙여 넣습니다. [!DNL Repeater] 기존 을 덮어쓸 설치 디렉토리 [!DNL bin] 폴더를 입력합니다.

>[!NOTE]
>
>완료하기 위해 추가 파일을 업로드해야 하는 경우 [!DNL Insight Server] 업그레이드하면 Adobe에서 이에 대한 지침을 제공합니다.

업그레이드 파일을 [!DNL Repeater] 머신, [!DNL Repeater] 자동으로 자신을 다시 시작하고 새 버전을 로드합니다.
