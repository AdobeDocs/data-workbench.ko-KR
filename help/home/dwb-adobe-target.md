---
description: 데이터 워크벤치를 Adobe Target과 통합합니다. 데이터 세그먼트를 내보내고 내보내기 파일을 자동으로 채웁니다.
solution: Analytics
title: Adobe Target과 데이터 워크벤치 통합
topic: Data workbench
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Adobe Target과 데이터 워크벤치 통합

Adobe Data Workbench와 Adobe Target의 통합이 데이터 워크벤치 기능을 사용하여 데이터 세그먼트를 내보내고 내보내기 파일을 자동으로 채울 수 있게 되었습니다.

Adobe Data Workbench는 데이터 공유 및 보고서 생성을 위해 Adobe Target과 폐쇄 루프 통합을 제공합니다. 데이터 워크벤치 내에서 전화, 스토어 등과 같은 채널을 통한 오프라인 전환을 포함하여 사용 가능한 모든 데이터를 사용하여 의미 있는 세그먼트의 모집단에서 분석할 수 있습니다.

예를 들어 방문자는 웹 사이트에서 구두를 찾지만 전환하지는 않습니다. 대신 방문자는 다음 구입 시 20% 할인 쿠폰을 다운로드한 다음 스토어에서 셔츠를 구입합니다. 데이터 워크벤치를 사용하여 해당 데이터를 수집한 다음 해당 프로필 데이터를 다시 Target으로 푸시하여 방문자가 오프라인으로 셔츠를 구입했음을 표시할 수 있습니다. 그런 다음 일반적으로 Target이 해당 방문자에게 구두를 다시 마케팅하려고 할 때 넥타이를 제공하는 캠페인을 타깃팅할 수 있습니다.

## Adobe Target을 사용하여 데이터 워크벤치 설정

1. 창에서 헤더를 마우스 오른쪽 단추로 [!UICONTROL Detail Table] 클릭합니다.

   ![](assets/insight-to-tnt.png)

1. 메뉴에서 **[!UICONTROL New Target Export]** 새 내보내기 파일의 이름을 선택하고 **[!UICONTROL Save As]** 명령 아래에 입력합니다.

1. 클릭 **[!UICONTROL Save Export File]**.

   템플릿 내보내기 창이 열립니다.

   모든 Adobe Target 정보는 자동으로 채워집니다. 세그먼트 내보내기에 입력한 내용을 기반으로 매개 변수 목록이 만들어집니다. 완료되면 데이터 워크벤치에서는 데이터를 Adobe Target 서버로 보냅니다.

   **참고:** 템플릿 파일은 에서 구성해야 합니다 [!UICONTROL Profile Architect]. 을 [!UICONTROL Client Name]입력하고 [!UICONTROL Domain Postfix], [!UICONTROL Mbox Host]입력해야 [!UICONTROL Mbox Name] 합니다. 여러 사이트가 있는 경우 여러 템플릿을 작성하고 서버에 저장합니다. 프로필 관리자의 템플릿은 에 있습니다 `Context\FileNew\Detail Table\Export\Copy`.

   ![](assets/insight-to-tnt1.png)

1. 쿼리 매개 변수를 [!UICONTROL mboxPC] 지정합니다.

   데이터 워크벤치 속성의 이름이 다른 [!UICONTROL mboxPC]것인 경우 적절한 쿼리 매개 변수를 편집하고 이름을 mboxPC로 _변경해야 합니다_.

   ![](assets/insight-to-tnt2.png)

   내보내기 파일을 서버에 저장하면 내보내기가 시작됩니다. 완료되면 응용 프로그램이 [!UICONTROL TnTSend.exe] 실행되고 Target 계정으로 데이터 전송을 시작합니다.

## Target용 데이터 워크벤치 구성

Adobe Target에서 다음 작업을 완료합니다.

데이터 워크벤치가 사용자 프로필을 Adobe Target으로 전달하고 있습니다. Target으로 내보내도록 구성하려면 API를 설정 및 활성화하고 내보내기 구성 파일에 대한 **[!UICONTROL clientname]** 및 **[!UICONTROL domain postfix]** 매개 변수를 제공해야 합니다(`export.cfg`).

세그먼트 내보내기 파일에 새 부울 옵션인 **[!UICONTROL Oneshot]** 이 추가되었습니다. 이 옵션은 새 프로필과 함께 배포된 템플릿 파일에 포함됩니다. 이 [!UICONTROL Oneshot] 값이 _true로_&#x200B;설정된 경우 내보내기가 완료된 후 파일 이름이 `.export` `.export.done-TIMESTAMP` 변경되므로 세그먼트가 두 번 이상 내보내지지 않습니다. Adobe Target으로 내보낼 때 중요합니다.

**참고:** Data Workbench에서 Adobe Target으로의 호출은 [!UICONTROL mbox] 호출로 계산되며 전송된 각 프로필에 대해 한 번의 호출이 필요합니다. 따라서 두 솔루션 간에 여러 호출이 필요할 경우 비용이 증가합니다.

구성이 완료되지 않으면 로그에 다음과 같은 오류 메시지가 표시됩니다.

```
TNT-040615-133212-Adobe-Target-Product-Test.log:
TnT Configuration left out these empty fields:
ClientName,MboxHost,MboxName
```

## 데이터 워크벤치에 대한 Adobe Target 구성

Adobe Target에서는 고객이 프로필 데이터를 전송하는 데 특별한 구성이 필요하지 않습니다. 사용자에 대한 프로필 정보는 일반적으로 일반 [!UICONTROL mbox] 요청에서 전달되며, 서버는 추가 설정 없이 타깃팅된 캠페인 설정에 대한 프로필 매개 변수를 표준 기능으로 사용할 수 있도록 합니다.

Adobe Target에는 Data Workbench 통합 기능이 내장되어 있으며, 이 통합은 수퍼 사용자 클라이언트 세부 사항 페이지에서 활성화할 수 있습니다. 이 옵션을 활성화하면 타깃팅에 사용할 수 있도록 Adobe Target 내의 데이터 워크벤치에서 공유된 세그먼트가 표시됩니다.

## ExportIntegration.exe에서 HTTP 로그 보고 설정

Adobe Target 통합 파일을 내보낼 [!UICONTROL HTTP.log] 때 긴 보고 기능을 [!UICONTROL ExportIntegration.exe] 줄일 수 있습니다.

새 [!UICONTROL httpLoggingEI.cfg] 구성 파일(위치 `server\Admin\Export\httpLoggingEI.cfg`)을 사용하면 데이터를 내보낼 때 파일에 대한 자세한 로깅을 줄일 수 [!UICONTROL HTTP.log] [!UICONTROL ExportIntegration.exe]있습니다. 자세한 요청/응답 로깅을 중지할 수 있습니다.

자세한 로깅(verbose logging)이 이미 [!UICONTROL TnTSend.log] 파일에 캡처되었습니다.

_True는_ 자세한 로깅을 설정하고 False _는_ 세부 정보 로깅을 [!UICONTROL HTTP.log] 파일에 중지합니다.

False 설정에서 경고 메시지만 [!UICONTROL HTTP.log] 파일로 전송됩니다(정보 컨텐츠는 전송되지 않음).