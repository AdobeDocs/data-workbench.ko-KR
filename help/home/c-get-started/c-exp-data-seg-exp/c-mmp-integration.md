---
description: 데이터 워크벤치를 사용하면 파일을 내보내 프로필 및 대상 내보내기를 통합된 Adobe Experience Cloud의 일부로 통합할 수 있습니다.
title: 마스터 마케팅 프로필 내보내기
uuid: bae0f0c5-a452-4afd-9f2c-5f3ab69a12d2
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# 마스터 마케팅 프로필 내보내기{#master-marketing-profile-export}

Data Workbench를 사용하면 파일을 내보내 프로필 및 대상과 통합하여 통합된 Adobe Experience Cloud의 일부로 사용할 수 있습니다.

<!-- <a id="section_731922BC8628479198A41EF3EA72F2FF"></a> -->

프로필 및 대상은 Adobe Experience [Cloud](https://docs.adobe.com/content/help/en/id-service/using/home.html)ID Service의 핵심 [!DNL Adobe Experience Cloud]서비스입니다. 프로필 및 대상 내보내기를 사용하면 모든 방문자에게 할당되고 Audience Manager에서 사용되는 고유한 ECID(Experience Cloud ID)를 사용하여 Experience Cloud에서 대상을 공유할 [수 있습니다](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html). 애플리케이션( [!DNL ExportIntegration.exe] [!DNL E:\Server\Scripts])은 MMP 및 Adobe Target 내보내기를 모두 생성하는 데 사용됩니다.

**프로필 및 대상을 사용하도록 FSU 서버 구성**

1. FSU 서버에 액세스합니다.
1. MMPExport.cfg 파일을 엽니다. `Server/Admin/Export/MMPExport.cfg`Adobe
1. 필요에 따라 모든 필드에 값을 입력합니다. 예:

   >[!NOTE]
   >
   >MMP/AAM 통합은 데이터 전송을 위해 Amazon의 3 버킷에 의존합니다.
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
   >또한 이 [!DNL MMPExport.cfg]파일을 사용하면 모든 레코드를 가져와서 세트로 분할하고 레코드 청크를 만들 수 있습니다. 그런 다음 레코드 청크를 Amazon S3로 내보냅니다. 레코드 청크를 만들려면 세 개의 필수 매개 변수가 필요합니다. [!DNL numRecordsPerChunk]및 [!DNL numThreads]를 [!DNL maxRetriesOnSendFailure]참조하십시오.

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
   <td colname="col2"> 내보내기가 전송될 AWS S3 버킷입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 개체 디렉토리</i> </td> 
   <td colname="col2"> s3 파일을 저장할 경로입니다. 이 기능은 하위 디렉토리를 지원합니다. <p> <p>중요: 경로에 공백 및 멀티바이트 문자를 사용할 수 없으며 내보내기에서 오류가 발생합니다. (최면 허용됨). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 지역</i> </td> 
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
   <td colname="col2"> 세그먼트와 트레이트를 각각 AAM에 저장하는 데 사용되는 폴더 이름이 됩니다. 고객당 고유해야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>클라이언트 ID</i> </td> 
   <td colname="col2"> MMP를 제공받을 때 고객에게 제공된 고유한 클라이언트 ID입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>클라이언트 암호</i> </td> 
   <td colname="col2"> <p><i></i>MMP에 대한 프로비저닝을 받을 때 고객에게 제공된 고유한 클라이언트 암호입니다. </p> </td> 
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
   <td colname="col2"> <p>레코드 수의 관점에서 청크 크기를 결정합니다. </p> <p>구현은 사용자가 지정한 값을 min = 1000 records&amp;nbsp;(~50KB 청크)&amp;nbsp;및 max = 50000 레코드(~2.5MB 청크)로 클립합니다.&amp;nbsp;사용자가 이 구성 속성을 지정하지 않을 경우 기본값 10000이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>numThreads</i> </td> 
   <td colname="col2"> <p>청크 전송 부품의 병렬 처리 수를 결정합니다. 이 변수는 1에서 24개 스레드 사이의 값을 허용하며, 기본값은 12개의 스레드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>maxRetriesOnSendFailure</i> </td> 
   <td colname="col2"> <p>청크 전송 실패 시 수행할 재시도 횟수를 결정합니다. 기본값은 0으로 재시도를 지정하지 않습니다. </p> <p>대기 간격 2초가 재시도 사이에 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**클라이언트에서 MMP 내보내기 생성**

1. 클라이언트에서 작업 영역을 열고 마우스 오른쪽 단추를 **[!UICONTROL Tools]**> **[!UICONTROL Detail Table]**&#x200B;클릭합니다.
1. 수준 **추가를 참조하십시오**.
1. 헤더를 마우스 오른쪽 단추로 클릭하고 속성 **추가를 선택합니다**.
1. 헤더를 마우스 오른쪽 단추로 클릭하고 새 **마스터 마케팅 프로필 내보내기를 선택합니다**. ![](assets/mmp_mmp_export.png)
1. 쿼리를 **확장합니다**.

   ![](assets/mmp_mmp_query.png)

1. MMP **구성을 확장합니다**.
1. (필수) MMP **세그먼트 이름** 및 MMP **방문자 ID 필드를 입력합니다**. 이러한 매개 변수는 비워 둘 수 없습니다.
1. MMP **세그먼트** 이름은 MMP에 정의된 세그먼트 ID와 일치해야 합니다.
1. MMP **방문자** ID는 방문자 ID에 해당하는 4단계에서 정의된 속성 **열입니다**.
1. 이러한 필드를 입력하면 내보내기의 헤더를 마우스 오른쪽 단추로 클릭하여 내보내기를 저장하고 &quot;사용자\. **내보내기&quot;로** 저장을 선택합니다.
1. 관리 **** > **프로필 관리자를** 열고 내보내기를 프로필에 저장합니다.

   모든 데이터가 올바르게 입력되면 FSU([!DNL Server/Exports])에 내보내기 파일이 생성되며, 에 있는 정보를 사용하여 내보내기도 AWS로 전송됩니다 [!DNL MMPExport.cfg]. 로그인이 [!DNL Server/Trace/]제공됩니다. 예. [!DNL MMP-102014-133651- `<Segment Export Name>` .log]

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
| MMP 세그먼트 ID | 필수 여부. 이것은 Audience Manager에서 먼저 정의하는 식별자입니다. |
| MMP 방문자 ID 필드 | ECID를 매핑합니다. |

