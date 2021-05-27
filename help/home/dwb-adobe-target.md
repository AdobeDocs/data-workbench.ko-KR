---
description: Adobe Target과 Data Workbench 통합. 데이터 세그먼트를 내보내고 내보내기 파일을 자동으로 채웁니다.
title: Adobe Target과 Data Workbench 통합
exl-id: e7c41e7a-aae6-4b5c-8b14-7ae97b62d70b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 1%

---

# Adobe Target과 Data Workbench 통합

Adobe Target과 Adobe Data Workbench의 통합이 보다 쉬워지면서 데이터 세그먼트를 내보내고 내보내기 파일을 자동으로 채울 수 있습니다.

Adobe Data Workbench은 데이터를 공유하고 보고서를 생성하기 위해 Adobe Target과 폐쇄 루프 통합을 제공합니다. Data Workbench 내에서 전화, 스토어 등과 같은 채널을 통한 오프라인 전환을 포함하여 사용 가능한 모든 데이터를 사용하여 의미 있는 세그먼트에 대한 모집단을 분석할 수 있습니다.

예를 들어 방문자는 웹 사이트에서 신발을 찾지만 전환되지 않습니다. 대신 방문자는 다음 구매에서 20%에 대한 쿠폰을 다운로드한 다음 스토어에서 셔츠를 구입합니다. Data Workbench을 사용하여 해당 데이터를 수집한 다음 해당 프로필 데이터를 다시 Target으로 푸시하여 방문자가 셔츠를 오프라인으로 구입했음을 표시할 수 있습니다. 그런 다음 일반적으로 Target이 해당 방문자에게 신발을 리마케팅하려고 할 수 있는 경우 넥타이 제공 캠페인을 해당 방문자에게 타깃팅할 수 있습니다.

## Adobe Target으로 Data Workbench 설정

1. [!UICONTROL Detail Table] 창에서 헤더를 마우스 오른쪽 단추로 클릭합니다.

   ![](assets/insight-to-tnt.png)

1. **[!UICONTROL New Target Export]** 을 선택하고 메뉴의 **[!UICONTROL Save As]** 명령 아래에 새 내보내기 파일의 이름을 입력합니다.

1. 클릭 **[!UICONTROL Save Export File]**.

   템플릿 내보내기 창이 열립니다.

   모든 Adobe Target 정보가 자동으로 채워집니다. 세그먼트 내보내기에 입력한 내용을 기반으로 매개 변수 목록을 만듭니다. 완료되면 Data Workbench은 데이터를 Adobe Target 서버로 전송합니다.

   **참고:** 템플릿 파일은 로 구성해야  [!UICONTROL Profile Architect]합니다. [!UICONTROL Client Name], [!UICONTROL Domain Postfix], [!UICONTROL Mbox Host] 및 [!UICONTROL Mbox Name]을 입력해야 합니다. 여러 사이트가 있는 경우 여러 템플릿을 작성하고 서버에 저장합니다. 프로필 관리자의 템플릿은 `Context\FileNew\Detail Table\Export\Copy`에 있습니다.

   ![](assets/insight-to-tnt1.png)

1. [!UICONTROL mboxPC] 쿼리 매개 변수를 지정합니다.

   Data Workbench 속성의 이름이 [!UICONTROL mboxPC] 이외의 것인 경우 적절한 쿼리 매개 변수를 편집하고 이름을 _mboxPC_&#x200B;로 변경해야 합니다.

   ![](assets/insight-to-tnt2.png)

   내보내기 파일을 서버에 저장하면 내보내기가 시작됩니다. 완료되면 [!UICONTROL TnTSend.exe] 애플리케이션이 실행되고 Target 계정으로 데이터 전송을 시작합니다.

## Target Data Workbench 구성

Adobe Target에서 다음 작업을 완료하십시오.

Data Workbench이 사용자 프로필을 Adobe Target에 전달하고 있습니다. Target으로 내보내기를 구성하려면 API를 설정 및 활성화하고 내보내기 구성 파일(`export.cfg`)에 대해 **[!UICONTROL clientname]** 및 **[!UICONTROL domain postfix]** 매개 변수를 제공해야 합니다.

세그먼트 내보내기 파일에 **[!UICONTROL Oneshot]** 이라는 새로운 부울 옵션이 추가되었습니다. 이 옵션은 새 프로필과 함께 배포되는 템플릿 파일에 포함되어 있습니다. [!UICONTROL Oneshot]이 _true_&#x200B;로 설정된 경우 내보내기가 완료된 후 `.export` 파일의 이름이 `.export.done-TIMESTAMP`로 변경되므로 세그먼트가 두 번 이상 내보내지지 않습니다. Adobe Target으로 내보낼 때 중요합니다.

**참고:** Data Workbench에서 Adobe Target에 대한 호출은  [!UICONTROL mbox] 호출로 계산되며, 전송된 각 프로필에 대해 한 번의 호출이 필요합니다. 따라서 두 솔루션 간에 여러 번의 호출이 필요할 경우 비용이 증가합니다.

구성이 완료되지 않으면 로그에 다음과 같은 오류 메시지가 표시됩니다.

```
TNT-040615-133212-Adobe-Target-Product-Test.log:
TnT Configuration left out these empty fields:
ClientName,MboxHost,MboxName
```

## Data Workbench에 대한 Adobe Target 구성

Adobe Target 내에서 고객이 프로필 데이터를 전송하는 데에는 특별한 구성이 필요하지 않습니다. 사용자에 대한 프로필 정보는 일반적으로 일반 [!UICONTROL mbox] 요청에서 전달되며, 서버는 프로필 매개 변수를 추가 설정 없이 타깃팅된 캠페인 설정에 표준 기능으로 사용할 수 있도록 합니다.

Adobe Target에는 내장 Data Workbench 통합이 있으며, 이 기능은 수퍼 사용자 클라이언트 세부 사항 페이지에서 활성화할 수 있습니다. 옵션을 활성화하면 타깃팅에 사용할 수 있도록 Adobe Target 내의 Data Workbench에서 공유되는 세그먼트를 표시합니다.

## ExportIntegration.exe에서 HTTP 로그 보고 설정

[!UICONTROL ExportIntegration.exe]을 사용하여 Adobe Target 통합 파일을 내보낼 때 [!UICONTROL HTTP.log]으로 긴 보고를 줄입니다.

새 [!UICONTROL httpLoggingEI.cfg] 구성 파일(`server\Admin\Export\httpLoggingEI.cfg`에 있음)을 사용하면 [!UICONTROL ExportIntegration.exe]을 사용하여 데이터를 내보낼 때 [!UICONTROL HTTP.log] 파일에 대한 세부 정보 로깅을 줄일 수 있습니다. 자세한 요청/응답 로깅을 중지할 수 있습니다.

자세한 정보 로깅이 이미 [!UICONTROL TnTSend.log] 파일에 캡처되었습니다.

__ Trueset 세부 정보 로깅을 설정하고  __ False는 파일에 대한 세부 정보 로깅을  [!UICONTROL HTTP.log] 중지합니다.

False 설정에서는 경고 메시지만 [!UICONTROL HTTP.log] 파일에 전송됩니다(정보 컨텐츠는 전송되지 않음).
