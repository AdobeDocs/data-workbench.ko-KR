---
description: Data Workbench을 사용하면 통합 Adobe Experience Cloud의 일부로 프로필 및 대상 내보내기와 통합하도록 파일을 내보낼 수 있습니다.
title: 기본 마케팅 프로필 내보내기
uuid: bae0f0c5-a452-4afd-9f2c-5f3ab69a12d2
exl-id: 9fc89815-d31d-41a7-a0c0-de1e84b24baa
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 3%

---

# 기본 마케팅 프로필 내보내기{#master-marketing-profile-export}

Data Workbench을 사용하면 파일을 내보내 프로필 및 대상자와 통합된 Adobe Experience Cloud의 일부로 통합할 수 있습니다.

<!-- <a id="section_731922BC8628479198A41EF3EA72F2FF"></a> -->

프로필 및 대상은 [!DNL Adobe Experience Cloud]의 핵심 서비스인 [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko-KR)의 일부입니다. 프로필 및 대상 내보내기를 사용하면 모든 방문자에게 할당된 다음 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=ko-KR)에서 사용하는 고유한 Experience Cloud ID(ECID)를 사용하여 Experience Cloud 간에 대상을 공유할 수 있습니다. [!DNL ExportIntegration.exe] 애플리케이션( [!DNL E:\Server\Scripts])은 MMP와 Adobe Target 내보내기를 모두 생성하는 데 사용됩니다.

**프로필 및 대상자를 사용하도록 FSU 서버 구성**

1. FSU 서버에 액세스합니다.
1. MMPExport.cfg 파일을 엽니다. `Server/Admin/Export/MMPExport.cfg`
1. 필요에 따라 모든 필드에 값을 입력합니다. 예를 들어,

   >[!NOTE]
   >
   >MMP/AAM 통합은 데이터 전송을 위해 Amazon의 3 버킷을 사용합니다.
   >
   >
   >MMP(s3) 전송에 필요한 s3 정보는 Audience Manager 팀에서 얻을 수 있습니다.

   ```
   Sample MMPExport.cfg
   MMP Export Configuration = MMPExportConfiguration: 
   s3 Bucket = string: aws_bucket_for_mmp 
   s3 Object Directory = string: test/files/ 
   s3 Region = string: us-east-1 
   s3 Access Key = string: ZZKI62OO5YBA 
   s3 Secret Key = string: ioqwa3OpNE5 
   data Provider Name = string: 895 
   client ID = string: mcprofile2-test 
   client Secret = string: saea1287617212987q 
   username = string: mmptest 
   password = string: pass 
   numRecordsPerChunk = int:  
   numThreads = int:  
   maxRetriesOnSendFailure = unsigned int:
   ```

   >[!NOTE]
   >
   >또한 [!DNL MMPExport.cfg]파일을 사용하면 모든 레코드를 세트에서 분리하고 레코드 청크를 만들 수 있습니다. 그런 다음 레코드 청크를 Amazon S3로 내보냅니다. 레코드 청크를 만들려면 세 가지 필수 매개 변수가 필요합니다. [!DNL numRecordsPerChunk], [!DNL numThreads] 및 [!DNL maxRetriesOnSendFailure]

**매개 변수 정의**

<table id="table_DDEFBC45895A4663973F9C2EB9052FEF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 정의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>s3 버킷</i> </td> 
   <td colname="col2"> 내보내기가 전송되는 AWS S3 버킷입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 개체 디렉토리</i> </td> 
   <td colname="col2"> s3 파일을 저장하는 경로입니다. 이 옵션은 하위 디렉토리를 지원합니다. <p> <p>중요 사항:  경로에 공백 및 멀티바이트 문자를 사용할 수 없으며 내보내기에 오류가 발생합니다. (하이픈이 허용됩니다.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 영역</i> </td> 
   <td colname="col2"> 내보내기가 전송되는 AWS s3 지역. 예. us-east-1 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 액세스 키</i> </td> 
   <td colname="col2"> AWS s3 액세스 키 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 비밀 키</i> </td> 
   <td colname="col2"> AWS s3 비밀 키 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>데이터 공급자 이름</i> </td> 
   <td colname="col2"> 이 이름은 각각 AAM에 세그먼트와 트레이트를 저장하는 데 사용되는 폴더 이름입니다. 고객별로 고유해야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>클라이언트 ID</i> </td> 
   <td colname="col2"> MMP에 대해 프로비저닝될 때 고객에게 제공되는 고유한 클라이언트 ID입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>클라이언트 암호</i> </td> 
   <td colname="col2"> <p><i></i>고객이 MMP에 대해 프로비저닝될 때 고객에게 제공되는 고유한 클라이언트 암호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>username</i> </td> 
   <td colname="col2"> MMP 사용자 이름 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>password</i> </td> 
   <td colname="col2"> MMP 암호 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>numRecordsPerChunk</i> </td> 
   <td colname="col2"> <p>레코드 수로 청크 크기를 결정합니다. </p> <p>구현은 사용자가 지정한 값을 min = 1000 records&amp;nbsp;(~50KB 청크)&amp;로 클립하고 최대 = 50000 레코드(~2.5MB 청크)로 클립합니다.&amp;nbsp;사용자가 이 구성 속성을 지정하지 않는 경우 기본값은 10000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>numThreads</i> </td> 
   <td colname="col2"> <p>청크 전송 부분의 병렬 처리 수를 결정합니다. 스레드 1개에서 24개 사이의 값을 수락하며 기본값은 12개의 스레드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>maxRetriesOnSendFailure</i> </td> 
   <td colname="col2"> <p>청크 전송 실패 시 수행할 다시 시도 횟수를 결정합니다. 기본값은 0으로 다시 시도 횟수를 지정하지 않습니다. </p> <p>절전 모드 간격은 다시 시도 간에 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**클라이언트에서 MMP 내보내기 생성**

1. 클라이언트에서 작업 공간을 열고 **[!UICONTROL Tools]** **[!UICONTROL Detail Table]** 를 마우스 오른쪽 단추로 클릭합니다.
1. **수준**&#x200B;을 추가합니다.
1. 헤더를 마우스 오른쪽 단추로 클릭하고 **속성 추가**&#x200B;를 선택합니다.
1. 헤더를 마우스 오른쪽 단추로 클릭하고 **새 기본 마케팅 프로필 내보내기**&#x200B;를 선택합니다. ![](assets/mmp_mmp_export.png)
1. **쿼리**&#x200B;를 확장합니다.

   ![](assets/mmp_mmp_query.png)

1. **MMP 구성**&#x200B;을 확장합니다.
1. (필수) **MMP 세그먼트 이름** 및 **MMP 방문자 ID 필드**&#x200B;를 입력합니다. 이러한 매개 변수는 비워 둘 수 없습니다.
1. **MMP 세그먼트 이름**&#x200B;은 MMP에 정의된 세그먼트 ID와 일치해야 합니다.
1. **MMP 방문자 ID**&#x200B;는 **방문자 ID**&#x200B;에 해당하는 4단계에서 정의한 속성 열입니다.
1. 이러한 필드를 입력하면 내보내기에 대한 헤더를 마우스 오른쪽 단추로 클릭하고 **Save**&#x200B;을 &quot;User\.export&quot;로 선택할 수 있습니다.
1. **Admin** > **프로필 관리자**&#x200B;를 열고 내보내기를 프로필에 저장합니다.

   모든 데이터가 올바르게 입력되면 FSU([!DNL Server/Exports])에서 내보내기 파일이 생성되며, [!DNL MMPExport.cfg] 의 정보를 사용하여 내보내기도 AWS로 전송됩니다. 이 로그의 로그는 [!DNL Server/Trace/]에 제공됩니다. 예, [!DNL MMP-102014-133651- `<Segment Export Name>`.log]

```
Query = SegmentExportQuery: 
Command = string: ExportIntegration.exe 
Command Arguments = string: \"%file%.cfg\" \"%file%\" 
Filter = string: 
Level = string: Page View 
MMP Configuration = MMPConfiguration: 
MMP Segment Name = string: 12345 
MMP Visitor ID Field = string: Tracking ID 
Oneshot = bool: true 
Output Fields = vector: 3 items 
0 = ColumnDefinition: 
Column Name = string: 
Field Name = string: Tracking ID 
1 = ColumnDefinition: 
Column Name = string: 
Field Name = string: PID 
2 = ColumnDefinition: 
Column Name = string: 
Field Name = string: SID 
Output File = string: MMPTest.txt 
Output Format = string: %1%\t%2%\t%3%\r\n 
Schedule End Time = string: 
Schedule Every = string: 
Schedule Start Time = string: 
Time Limit (sec) = double: 1800 
```

| 구성 세부 사항 | 설명 |
|---|---|
| MMP 세그먼트 ID | 필수 여부. Audience Manager에서 먼저 정의하는 식별자입니다. |
| MMP 방문자 ID 필드 | ECID를 매핑합니다. |
