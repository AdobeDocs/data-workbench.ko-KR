---
description: Insight Server, 변환 또는 반복을 제거하는 지침입니다.
title: 소프트웨어 제거
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
exl-id: 3ba5e5e3-c1a2-4ecb-9f88-a3fe923837e7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 4%

---

# 소프트웨어 제거{#uninstalling-your-software}

Insight Server, 변환 또는 반복을 제거하는 지침입니다.

## Insight Server Adobe {#section-7d7befe672854df79bb6c28ec02f6670} 제거

1. [!DNL Insight Server] Windows 서비스를 등록 취소합니다.

   1. 명령 프롬프트를 열고 [!DNL Insight Server]을 설치한 폴더의 bin 하위 디렉토리로 이동합니다.

      예: [!DNL C:\Adobe\Server\bin]

   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지하고 등록을 취소합니다.

      ```
      InsightServer64.exe /unregserver
      ```

1. [!DNL Insight Server] 설치 디렉터리를 삭제합니다.

## Transform {#section-5e6a604dadb5477ba4dc9f93c9be0897} 제거

1. 다음 단계를 사용하여 [!DNL Transform] 을 사용 중인 각 프로필에 대해 [!DNL profile.cfg] 파일을 업데이트합니다.

   1.  [!DNL Profile Manager].
   1. [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다. [!DNL profile.cfg] 창이 나타납니다.

   1. [!DNL profile.cfg] 창의 디렉토리 벡터에서 [!DNL Transform] 프로필 항목을 삭제합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL profile.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;를 클릭합니다.

1. [!DNL Insight Server] 설치 디렉토리의 [!DNL Profiles] 폴더에서 [!DNL Transform] 폴더를 삭제합니다.

## 반복 제거 중 {#section-2f94141d956749d88f549dbea26e5272}

1. [!DNL Repeater] Windows 서비스를 등록 취소합니다.

   1. 명령 프롬프트를 열고 [!DNL Repeater]을 설치한 폴더의 bin 하위 디렉토리로 이동합니다.

      예: [!DNL D:\Adobe\Repeater\bin]

   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지하고 등록을 취소합니다.

      ```
      InsightServer64.exe /unregserver
      ```

1. [!DNL Repeater] 설치 디렉터리를 삭제합니다.
