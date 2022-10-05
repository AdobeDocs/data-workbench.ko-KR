---
description: Insight Server, 변환 또는 반복을 제거하는 지침입니다.
title: 소프트웨어 제거
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
exl-id: 3ba5e5e3-c1a2-4ecb-9f88-a3fe923837e7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 4%

---

# 소프트웨어 제거{#uninstalling-your-software}

{{eol}}

Insight Server, 변환 또는 반복을 제거하는 지침입니다.

## Insight Server Adobe 제거 {#section-7d7befe672854df79bb6c28ec02f6670}

1. 등록 취소 [!DNL Insight Server] Windows 서비스.

   1. 명령 프롬프트를 열고 설치한 폴더의 bin 하위 디렉토리로 이동합니다 [!DNL Insight Server].

      예: [!DNL C:\Adobe\Server\bin]

   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지하고 등록을 취소합니다.

      ```
      InsightServer64.exe /unregserver
      ```

1. 삭제 [!DNL Insight Server] 설치 디렉토리.

## 변형 제거 {#section-5e6a604dadb5477ba4dc9f93c9be0897}

1. 다음 단계를 사용하여 를 업데이트합니다 [!DNL profile.cfg] 사용 중인 각 프로필에 대한 파일 [!DNL Transform].

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. 다음 [!DNL profile.cfg] 창이 나타납니다.

   1. 에서 [!DNL profile.cfg] 창, 삭제 [!DNL Transform] 디렉토리 벡터의 프로파일 항목.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. 삭제 [!DNL Transform] 폴더의 [!DNL Profiles] 폴더의 [!DNL Insight Server] 설치 디렉토리.

## 반복 제거 {#section-2f94141d956749d88f549dbea26e5272}

1. 등록 취소 [!DNL Repeater] Windows 서비스.

   1. 명령 프롬프트를 열고 설치한 폴더의 bin 하위 디렉토리로 이동합니다 [!DNL Repeater].

      예: [!DNL D:\Adobe\Repeater\bin]

   1. 명령 프롬프트에서 다음 명령을 실행하여 Microsoft Windows에서 서비스로 중지하고 등록을 취소합니다.

      ```
      InsightServer64.exe /unregserver
      ```

1. 삭제 [!DNL Repeater] 설치 디렉토리.
