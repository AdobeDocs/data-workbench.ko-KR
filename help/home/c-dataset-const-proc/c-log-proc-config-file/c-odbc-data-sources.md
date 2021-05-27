---
description: 'Data Workbench 서버(InsightServer64.exe)는 ODBC 3.0 호환 드라이버가 있는 모든 SQL 데이터베이스(예: Oracle 또는 Microsoft SQL Server)에서 이벤트 데이터를 읽을 수 있습니다.'
title: ODBC 데이터 소스
uuid: 5b37cd41-2d79-472c-8e6d-00ff894991a9
exl-id: b22b1e27-9b6c-4708-b45c-a9605807689a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 1%

---

# ODBC 데이터 소스{#odbc-data-sources}

Data Workbench 서버(InsightServer64.exe)는 ODBC 3.0 호환 드라이버가 있는 모든 SQL 데이터베이스(예: Oracle 또는 Microsoft SQL Server)에서 이벤트 데이터를 읽을 수 있습니다.

Data Workbench 서버의 ODBC 지원은 센서에서 데이터 로드를 위한 기존 지원 또는 외부 프로세스에서 생성된 로그 파일과 유사합니다. 그러나 몇 가지 추가 고려 사항과 제한 사항이 있습니다.

* Data Workbench 서버의 ODBC 지원은 클러스터링 기능과 호환됩니다. 데이터는 모든 처리 서버 간에 배포되며, 모든 후속 처리(쿼리 처리 포함)는 클러스터링을 통해 완전히 이점이 있습니다.
* ODBC 지원은 타사 ODBC 드라이버에 따라 다릅니다. ODBC 지원이 작동하려면 Adobe 플랫폼 외부의 도구를 사용하여 Data Workbench 서버가 실행되는 시스템에 이러한 드라이버를 구성해야 합니다. Data Workbench 시스템은 추가 구성이 필요하지 않습니다.
* 데이터가 로드되는 테이블 또는 뷰의 ID 열이 증가해야 합니다. 모든 행의 경우 새 행이 데이터베이스에 삽입되므로 이 열의 값(테이블의 실제 열 또는 SQL 열 표현식의 열)이 감소되지 않아야 합니다. 이 제약 조건을 위반하면 데이터가 손실됩니다. 적절한 성능을 위해 이 열 또는 열 식에 인덱스가 필요합니다.

   >[!NOTE]
   >
   >여러 행이 [!DNL Increasing ID] 열에 동일한 값을 가질 수 있습니다. 한 가지 가능성은 완벽한 정밀도 미만의 타임스탬프 열입니다.

* Data Workbench 서버는 긴 데이터(사용 중인 특정 데이터베이스 애플리케이션에 의해 결정된 특정 길이 이상의 데이터)가 있는 열을 로드할 수 없습니다.
* 데이터베이스에서 데이터를 검색하는 속도가 디스크 파일에서 데이터를 읽는 것보다 느립니다. ODBC 소스에서 데이터를 로드하는 데이터 세트는 센서나 기타 디스크 파일에서 데이터를 가져오는 동등한 크기의 데이터 세트보다 처리(특히 재처리 시)시간이 훨씬 오래 걸립니다.

데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.

**ODBC용 Insight Server를 구성하려면[!DNL event data]**

SQL 데이터베이스에서 데이터를 로드하도록 Data Workbench 서버를 구성하려면 먼저 다음 단계를 순서대로 수행해야 합니다.

1. 데이터 집합이 처리되는 Data Workbench 서버 시스템에 ODBC 드라이버를 포함한 적절한 데이터베이스 클라이언트 소프트웨어를 설치합니다.

   >[!NOTE]
   >
   >Data Workbench 서버 클러스터에서 처리를 위해 ODBC 이벤트 데이터를 로드하는 경우 클러스터의 모든 처리 서버에 데이터베이스 클라이언트 소프트웨어를 설치해야 합니다. 클러스터에서 처리 서버를 지정하는 방법에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서*&#x200B;를 참조하십시오.

1. Windows용 ODBC 데이터 소스 관리자를 사용하여 데이터 소스를 구성합니다.

   Data Workbench 서버(InsightServer64.exe)는 Windows 서비스로 실행됩니다. 따라서 Data Source는 일반적으로 Data Workbench 서버에서 사용할 수 있도록 User DSN 대신 System DSN으로 구성되어야 합니다. 데이터베이스 소프트웨어 설명서에서 이 구성 단계에 대한 자세한 정보를 찾을 수 있습니다.

해당 Data Workbench 서버 시스템에 데이터베이스 클라이언트 소프트웨어를 설치한 후 원하는 프로필에 대한 [!DNL Log Processing] 구성 파일에서 적절한 매개 변수를 편집하여 ODBC 데이터 소스를 사용하도록 데이터 집합을 구성할 수 있습니다.

## 매개 변수 {#section-15c0218d93364693a565f2609a12f73e}

ODBC(Open Database Connectivity) 표준을 사용하는 데이터베이스의 데이터에 대해서는 다음 매개 변수를 사용할 수 있습니다.

<table id="table_606D8A90DA4A43C29F2C6130F8C753F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> ODBC 원본에 대한 식별자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데이터 소스 이름 </td> 
   <td colname="col2"> 데이터 집합이 처리되는 Data Workbench 서버 시스템의 관리자가 제공하는 DSN으로서 데이터가 로드될 데이터베이스를 참조합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데이터베이스 암호 </td> 
   <td colname="col2"> 데이터베이스에 연결할 때 사용할 암호입니다. <span class="wintitle"> 데이터 소스 관리자</span>에서 DSN에 대해 암호가 구성된 경우 암호는 비워 둘 수 있습니다. 여기서 제공된 모든 암호는 <span class="wintitle"> 데이터 소스 관리자</span>에서 DSN에 대해 구성된 암호를 무시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데이터베이스 사용자 ID </td> 
   <td colname="col2"> 데이터베이스에 연결할 때 사용할 사용자 ID입니다. <span class="wintitle"> 데이터 소스 관리자</span>에서 DSN에 대해 사용자 ID가 구성된 경우 이 ID가 비어 있을 수 있습니다. 여기서 제공된 모든 사용자 ID는 <span class="wintitle"> 데이터 소스 관리자</span>에서 DSN에 대해 구성된 사용자 ID를 무시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필드 </td> 
   <td colname="col2"> 데이터베이스의 데이터 열에서 Data Workbench 서버 실행 엔진의 데이터 필드에 대한 매핑을 지정하는 열 개체의 벡터입니다. 각 열에는 <span class="wintitle"> 열 이름</span> 및 <span class="wintitle"> 필드 이름</span> 항목이 있습니다. <span class="wintitle"> 열 </span> 이름은 위에 설명된 테이블 식별자로 식별되는 테이블의 컨텍스트에서  <span class="wintitle"> 유효해야 </span> 하는 SQL 열 표현식입니다. 테이블의 열 수를 기반으로 하는 열 이름 또는 SQL 표현식일 수 있습니다. 특정 데이터 형식의 값을 정밀도를 잃지 않는 방식으로 문자열로 변환하는 데 서식 함수가 필요할 수 있습니다. 모든 데이터는 데이터베이스의 기본 서식 방법을 사용하여 암시적으로 문자열로 변환됩니다. 이 경우 명시적 형식 식을 사용하지 않는 경우 일부 열 데이터 형식(예: 날짜/시간 데이터 형식)에 대해 데이터가 손실될 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID 열 증가 </td> 
   <td colname="col2"> <p>새 행이 추가되면 증가하거나 감소하지 않는 기준을 충족하는 열 이름 또는 SQL 열 식입니다. 즉, 행 B가 행 A보다 늦은 시간에 테이블에 추가되는 경우 행 B의 이 열(또는 열 표현식)의 값은 데이터베이스 고유 정렬 순서에 따라 행 A의 해당 값보다 커야 합니다. </p> <p> 
     <ul id="ul_EBF6AEE4746B41B3B5BB6CC74194DAED"> 
      <li id="li_A5C9BE52B01649DE9726ECEC68B99828"> <span class="wintitle"> ID 열 증가 </span>이름은 기존 열의 이름과 동일할 수 있지만 반드시 그럴 필요는 없습니다. </li> 
      <li id="li_CF69EAB4AFB14F4894F7A5CDCAF06947"> 이 식은 SQL 문자 데이터 형식을 가진 것으로 간주됩니다. 실제 증가하는 ID 열이 다른 데이터 유형의 경우, 이 값은 문자열로 변환하려면 열 표현식이어야 합니다. 이는 일반적으로 비교가 사전적(문자별)이므로 값의 서식을 신중하게 지정하는 것이 중요합니다. </li> 
      <li id="li_58977431962E48039C898CFC47C53323"> 이 식은 SQL ORDER BY 절에 사용되고 SQL WHERE 절에 비교됩니다. 사용되는 정확한 열 표현식을 기반으로 인덱스를 만드는 것이 매우 중요합니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 소스 ID </td> 
   <td colname="col2"> <p>이 매개 변수의 값은 임의의 문자열일 수 있습니다. 값이 지정된 경우 이 매개 변수를 사용하여 로그 항목을 소스 식별 또는 대상 처리를 위해 다른 로그 소스와 구분할 수 있습니다. x-log-source-id 필드는 각 로그 항목에 대한 로그 소스를 식별하는 값으로 채워집니다. 예를 들어 ODBCSsource01이라는 ODBC 소스에서 로그 항목을 식별하려면 ODBCSsource01에서 <span class="filepath"> 를 입력할 수 있습니다.</span> 그리고 이 문자열은 해당 소스의 모든 로그 항목에 대해 x-log-source-id 필드에 전달됩니다. </p> <p> x-log-source-id 필드에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> 이벤트 데이터 레코드 필드</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버에서 실행 </td> 
   <td colname="col2"> ODBC 쿼리를 데이터베이스에서 데이터를 가져오는 처리 서버의 <span class="filepath"> profile.cfg</span> 파일의 인덱스 값입니다. (<span class="filepath"> profile.cfg</span> 파일의 Processing Server 매개 변수는 데이터 집합에 대한 모든 처리 서버를 나열하며 각 서버에는 인덱스 값이 있으며, 첫 번째는 0입니다.) 기본값은 0입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 테이블 식별자 </td> 
   <td colname="col2"> 데이터를 로드할 테이블 또는 뷰의 이름을 지정하는 SQL 식입니다. 일반적인 테이블 식별자는 SCHEMA.TABLE 형식입니다. </td> 
  </tr> 
 </tbody> 
</table>

이 예는 ODBC 데이터 소스가 있는 Data Workbench의 [!DNL Log Processing] 구성 창을 보여줍니다. 이 데이터 소스는 [!DNL Data Source Name] &quot;VSTestO&quot;를 사용하는 데이터베이스의 [!DNL VISUAL.VSL] 테이블에서 데이터를 가져옵니다. 5개의 (5) 열 개체( [!DNL Fields])는 데이터베이스의 데이터 열에서 Data Workbench 서버에 데이터를 매핑합니다.

![](assets/cfg_LogProcessing_LogSources_ODBC.png)
