---
description: Insight Server, Transform 또는 Repeater 제거 지침
solution: Insight
title: 소프트웨어 제거
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 소프트웨어 제거{#uninstalling-your-software}

Insight Server, Transform 또는 Repeater 제거 지침

## Insight Server Adobe 제거 {#section-7d7befe672854df79bb6c28ec02f6670}

1. Windows 서비스의 등록을 [!DNL Insight Server] 취소합니다.

   1. 명령 프롬프트를 열고 설치한 폴더의 bin 하위 디렉토리로 이동합니다 [!DNL Insight Server].

      예: [!DNL C:\Adobe\Server\bin]

   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지 및 등록을 취소합니다.

      ```
      InsightServer64.exe /unregserver
      ```

1. 설치 디렉토리를 [!DNL Insight Server] 삭제합니다.

## 변형 제거 {#section-5e6a604dadb5477ba4dc9f93c9be0897}

1. 다음 단계에 따라 사용 중인 각 프로필에 대한 [!DNL profile.cfg] 파일을 업데이트합니다 [!DNL Transform].

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL profile.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. 창이 [!DNL profile.cfg] 나타납니다.

   1. 창의 디렉토리 벡터에서 [!DNL profile.cfg] [!DNL Transform] 프로필 항목을 삭제합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL profile.cfg] > [!DNL User] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL profile name]***.

1. [!DNL Transform] 설치 디렉토리의 [!DNL Profiles] [!DNL Insight Server] 폴더에서 폴더를 삭제합니다.

## 반복 제거 {#section-2f94141d956749d88f549dbea26e5272}

1. Windows 서비스의 등록을 [!DNL Repeater] 취소합니다.

   1. 명령 프롬프트를 열고 설치한 폴더의 bin 하위 디렉토리로 이동합니다 [!DNL Repeater].

      예: [!DNL D:\Adobe\Repeater\bin]

   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지 및 등록을 취소합니다.

      ```
      InsightServer64.exe /unregserver
      ```

1. 설치 디렉토리를 [!DNL Repeater] 삭제합니다.

