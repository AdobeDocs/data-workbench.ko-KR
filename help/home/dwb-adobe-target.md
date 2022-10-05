---
description: Adobe Target과 Data Workbench 통합. 데이터 세그먼트를 내보내고 내보내기 파일을 자동으로 채웁니다.
title: Adobe Target과 Data Workbench 통합
exl-id: e7c41e7a-aae6-4b5c-8b14-7ae97b62d70b
source-git-commit: 4ab43bfbad96096fb2cebd77a8be8fa6d49fa7dc
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 1%

---

# Adobe Target과 Data Workbench 통합

{{eol}}

Adobe Target과 Adobe Data Workbench의 통합이 보다 쉬워지면서 데이터 세그먼트를 내보내고 내보내기 파일을 자동으로 채울 수 있습니다.

Adobe Data Workbench은 데이터를 공유하고 보고서를 생성하기 위해 Adobe Target과 폐쇄 루프 통합을 제공합니다. Data Workbench 내에서 전화, 스토어 등과 같은 채널을 통한 오프라인 전환을 포함하여 사용 가능한 모든 데이터를 사용하여 의미 있는 세그먼트에 대한 모집단을 분석할 수 있습니다.

예를 들어 방문자는 웹 사이트에서 신발을 찾지만 전환되지 않습니다. 대신 방문자는 다음 구매에서 20%에 대한 쿠폰을 다운로드한 다음 스토어에서 셔츠를 구입합니다. Data Workbench을 사용하여 해당 데이터를 수집한 다음 해당 프로필 데이터를 다시 Target으로 푸시하여 방문자가 셔츠를 오프라인으로 구입했음을 표시할 수 있습니다. 그런 다음 일반적으로 Target이 해당 방문자에게 신발을 리마케팅하려고 할 수 있는 경우 넥타이 제공 캠페인을 해당 방문자에게 타깃팅할 수 있습니다.

## Adobe Target으로 Data Workbench 설정

1. 에서 헤더를 마우스 오른쪽 단추로 클릭합니다. [!UICONTROL Detail Table] 창을 엽니다.

   ![](assets/insight-to-tnt.png)

1. 선택 **[!UICONTROL New Target Export]** 그리고 아래에 새 내보내기 파일의 이름을 입력합니다. **[!UICONTROL Save As]** 명령을 클릭합니다.

1. 클릭 **[!UICONTROL Save Export File]**.

   템플릿 내보내기 창이 열립니다.

   모든 Adobe Target 정보가 자동으로 채워집니다. 세그먼트 내보내기에 입력한 내용을 기반으로 매개 변수 목록을 만듭니다. 완료되면 Data Workbench은 데이터를 Adobe Target 서버로 전송합니다.

   **참고:** 템플릿 파일은 [!UICONTROL Profile Architect]. 다음 [!UICONTROL Client Name], [!UICONTROL Domain Postfix], [!UICONTROL Mbox Host], 및 [!UICONTROL Mbox Name] 을 입력해야 합니다. 여러 사이트가 있는 경우 여러 템플릿을 작성하고 서버에 저장합니다. 프로필 관리자의 템플릿은 `Context\FileNew\Detail Table\Export\Copy`.

   ![](assets/insight-to-tnt1.png)

1. 을(를) 지정합니다. [!UICONTROL mboxPC] 쿼리 매개 변수.

   Data Workbench 속성의 이름이 [!UICONTROL mboxPC]를 채울 때는 적절한 쿼리 매개 변수를 편집하고 이름을 로 변경해야 합니다. _mboxPC_.

   ![](assets/insight-to-tnt2.png)

   내보내기 파일을 서버에 저장하면 내보내기가 시작됩니다. 완료되면 [!UICONTROL TnTSend.exe] 애플리케이션이 실행되어 Target 계정으로 데이터 전송을 시작합니다.

## Target Data Workbench 구성

Adobe Target에서 다음 작업을 완료하십시오.

Data Workbench이 사용자 프로필을 Adobe Target에 전달하고 있습니다. Target으로 내보내기를 구성하려면 API를 설정 및 활성화하고 를 제공해야 합니다. **[!UICONTROL clientname]** 및 **[!UICONTROL domain postfix]** 내보내기 구성 파일의 매개 변수(`export.cfg`).

라는 새로운 부울 옵션 **[!UICONTROL Oneshot]** 을 세그먼트 내보내기 파일에 추가했습니다. 이 옵션은 새 프로필과 함께 배포되는 템플릿 파일에 포함되어 있습니다. If [!UICONTROL Oneshot] 가 로 설정되어 있습니다. _true_, 그런 다음 `.export` 파일 이름이 `.export.done-TIMESTAMP` 내보내기가 완료되면 세그먼트를 두 번 이상 내보낼 수 없습니다. Adobe Target으로 내보낼 때 중요합니다.

**참고:** Data Workbench에서 Adobe Target로의 호출은 [!UICONTROL mbox] 를 호출하여 전송된 각 프로필에 대해 한 번의 호출이 필요합니다. 따라서 두 솔루션 간에 여러 번의 호출이 필요할 경우 비용이 증가합니다.

구성이 완료되지 않으면 로그에 다음과 같은 오류 메시지가 표시됩니다.

```
TNT-040615-133212-Adobe-Target-Product-Test.log:
TnT Configuration left out these empty fields:
ClientName,MboxHost,MboxName
```

## Data Workbench에 대한 Adobe Target 구성

Adobe Target 내에서 고객이 프로필 데이터를 전송하는 데에는 특별한 구성이 필요하지 않습니다. 사용자에 대한 프로필 정보는 일반적으로 일반으로 전달됩니다 [!UICONTROL mbox] 요청이 수행되면 서버는 추가적인 설정 없이 타깃팅된 캠페인 설정에 프로필 매개 변수를 표준 기능으로 사용할 수 있도록 합니다.

Adobe Target에는 내장 Data Workbench 통합이 있으며, 이 기능은 수퍼 사용자 클라이언트 세부 사항 페이지에서 활성화할 수 있습니다. 옵션을 활성화하면 타깃팅에 사용할 수 있도록 Adobe Target 내의 Data Workbench에서 공유되는 세그먼트를 표시합니다.

## ExportIntegration.exe에서 HTTP 로그 보고 설정

보고 시간 단축 [!UICONTROL HTTP.log] 사용 시 [!UICONTROL ExportIntegration.exe] Adobe Target 통합 파일을 내보내려면 다음을 수행하십시오.

새로운 [!UICONTROL httpLoggingEI.cfg] 구성 파일(위치 `server\Admin\Export\httpLoggingEI.cfg`)에 대한 세부 정보 로깅을 줄일 수 있습니다 [!UICONTROL HTTP.log] 을 사용하여 데이터를 내보낼 때 파일 [!UICONTROL ExportIntegration.exe]. 자세한 요청/응답 로깅을 중지할 수 있습니다.

자세한 정보 로깅이 이미 캡처되었습니다. [!UICONTROL TnTSend.log] 파일.

_True_ 자세한 로깅을 설정하고 _False_ 세부 정보 로깅을 중지합니다. [!UICONTROL HTTP.log] 파일.

False 설정에서는 경고 메시지만 [!UICONTROL HTTP.log] 파일(정보 컨텐츠가 전송되지 않음).
