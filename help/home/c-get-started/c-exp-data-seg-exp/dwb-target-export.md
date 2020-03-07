---
description: 세부 사항 테이블에서 TargetBulkUpload.exe를 사용하여 데이터 워크벤치 데이터를 Adobe Target으로 내보냅니다.
title: Adobe Target으로 내보내기
uuid: 0eb99e6f-f0b5-495e-a3b6-df30f61378a7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Adobe Target으로 내보내기{#export-to-adobe-target}

세부 사항 테이블에서 TargetBulkUpload.exe를 사용하여 데이터 워크벤치 데이터를 Adobe Target으로 내보냅니다.

Data Workbench를 사용하면 파일을 내보내 Adobe Target과 통합하여 통합된 Adobe Experience Cloud의 일부로 사용할 수 있습니다.

이 **[!DNL TargetBulkUpload]** 파일은 서버 설치 *파일의 Server\Scripts* 폴더에 있습니다. 실행 파일에는 재시도 로직뿐만 아니라 성능을 최적화하는 추가 로직이 있습니다.

업로드 스크립트를 실행하기 전에 `TargetBulkUpload.cfg` 파일을 수정하여 *Server/Admin/Export* 폴더로 이동할 수 있습니다. 예를 들어 최대 시간 초과 간격을 720분(기본값)으로 설정하여 지정된 기간 후 업로드를 시간 초과하도록 할 수 있습니다.

**작동 방법**

데이터가 Target으로 성공적으로 전송되면 업로드 상태가 계속 모니터링됩니다. 업로드가 성공하면 성공 메시지가 기록됩니다. 업로드가 실패하거나 보류 중인 경우 모니터링이 계속됩니다. 파일에서 시간 초과 간격을 구성할 수 `TargetBulkUpload.cfg` 있습니다. 업로드가 Target에 고정되면 메시지가 기록되고 상태를 계속 모니터링할 수 있습니다.

트리거된 내보내기의 추적에 생성된 로그 파일은 [!DNL /server/Trace/]다음과 같습니다.

* `targetbulkuploadexportname.log`
* `targetbulkuploadexportname.log.completed`

이 `targetbulkuploadexportname.log` 파일은 여러 배치의 모든 레코드, 배치하려는 Edge Server 및 상태(성공, 실패, 프로필을 찾을 수 없음, 상태 알 수 없음 및 중지)에 대한 세부 상태를 갖습니다. 일괄 처리가 중단되는 경우 일괄 처리가 더 이상 처리되지 않습니다. 중단된 일괄 처리 URL을 사용하여 상태를 추적할 수 있습니다. 다음 예제 데이터를 `targetbulkuploadexportname.log.completed` 파일에서 참조하십시오.

```
1205057 total rows 
568740 successful 
62 failed 
28964 profile not found 
112169 unknown status 
492339 stuck status
```

연결이 끊어진 상태 값은 성공적으로 또는 실패한 업로드의 수에 관계없이 총 보류 배치 크기로 증가합니다. 총 행 값도 고정 일괄 크기의 동일한 수로 증가합니다.

>[!NOTE]
>
>이전에는 DWB 데이터를 를 사용하여 [!DNL ExportIntegration.exe]내보냈습니다. 현재 이 실행 파일에는 MMP, CRS 및 S/FTP 내보내기만 사용됩니다. 이제 Adobe Target 통합은 데이터 [!DNL TargetBulkUpload.exe] 워크벤치에서 을 사용합니다.

