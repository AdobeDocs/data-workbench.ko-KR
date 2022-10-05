---
description: 세부 사항 테이블에서 TargetBulkUpload.exe를 사용하여 Data Workbench 데이터를 Adobe Target으로 내보냅니다.
title: Adobe Target으로 내보내기
uuid: 0eb99e6f-f0b5-495e-a3b6-df30f61378a7
exl-id: 41e885bb-182a-4983-98e8-65eec1da9fe9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 2%

---

# Adobe Target으로 내보내기{#export-to-adobe-target}

{{eol}}

세부 사항 테이블에서 TargetBulkUpload.exe를 사용하여 Data Workbench 데이터를 Adobe Target으로 내보냅니다.

Data Workbench을 사용하면 통합 Adobe Experience Cloud의 일부로서 Adobe Target과 통합하도록 파일을 내보낼 수 있습니다.

다음 **[!DNL TargetBulkUpload]** 파일은에서 찾을 수 있습니다. *서버\스크립트* 폴더(서버 설치 파일)를 포함합니다. 실행 파일에는 다시 시도 로직뿐만 아니라 성능을 최적화하는 추가 로직도 있습니다.

을 수정할 수 있습니다 `TargetBulkUpload.cfg` 다음 위치로 이동 *서버/관리/내보내기* 폴더에 업로드 스크립트를 실행하기 전 예를 들어 지정된 기간 후 업로드를 시간 초과하도록 최대 시간 제한 간격 을 720분(기본값)으로 설정할 수 있습니다.

**작동 방법**

데이터가 성공적으로 Target에 전송되면 업로드의 상태가 계속 모니터링됩니다. 업로드가 성공하면 성공 메시지가 기록됩니다. 업로드가 실패하거나 보류 중인 경우 모니터링이 계속 수행됩니다. 시간 제한 간격은 `TargetBulkUpload.cfg` 파일. 업로드가 Target에서 멈춘 경우 메시지가 기록되며 상태를 계속 모니터링할 수 있습니다.

아래에 트리거된 내보내기에 대한 추적에 두 개의 로그 파일이 생성됩니다 [!DNL /server/Trace/]:

* `targetbulkuploadexportname.log`
* `targetbulkuploadexportname.log.completed`

다음 `targetbulkuploadexportname.log` 파일에는 여러 배치의 모든 레코드, 배치의 대상 에지 서버 및 상태(성공, 실패, 프로필 찾을 수 없음, 상태 알 수 없음 및 중단)에 대한 세부 상태가 있습니다. 일괄 처리가 중단된 경우, 일괄 처리가 더 이상 처리되지 않습니다. 중단된 배치 URL을 사용하여 상태를 추적할 수 있습니다. 다음 예제 데이터를 `targetbulkuploadexportname.log.completed` 파일:

```
1205057 total rows 
568740 successful 
62 failed 
28964 profile not found 
112169 unknown status 
492339 stuck status
```

업로드 성공 또는 실패한 횟수에 관계없이 중단 상태 값은 총 중단 일괄 처리 크기로 증가합니다. 합계 행 값은 고정된 일괄 처리 크기와 동일한 수로 증가합니다.

>[!NOTE]
>
>이전에는 DWB 데이터를 [!DNL ExportIntegration.exe]. 현재 이 실행 파일에는 MMP, CRS 및 S/FTP 내보내기만 사용됩니다. 이제 Adobe Target 통합에서 을 사용합니다 [!DNL TargetBulkUpload.exe] Data Workbench에서 확인하십시오.
