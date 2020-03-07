---
description: CRS(고객 레코드 서비스) 내보내기 기능을 사용하면 Data Workbench 데이터를 Adobe Analytics 핵심 서비스로 내보내 보고 및 분석을 비롯한 다른 Analytics 기능과 통합할 수 있습니다.
title: Analytics 코어 서비스로 내보내기
uuid: 8fd7e8d8-989a-4ad6-bab5-61bfd37b0201
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Analytics 코어 서비스로 내보내기{#exporting-to-analytics-core-services}

CRS(고객 레코드 서비스) 내보내기 기능을 사용하면 Data Workbench 데이터를 Adobe Analytics 핵심 서비스로 내보내 보고 및 분석을 비롯한 다른 Analytics 기능과 통합할 수 있습니다.

>[!NOTE]
>
>CRS 내보내기 기능이 작동하려면 방문자의 Analytics ID가 Experience Cloud ID 서비스(ECID)를 기반으로 해야 합니다. 방문자에 대해 데이터 워크벤치에서 ECID를 채울 수 있지만 클라이언트가 유예 기간에 있거나 방문자의 쿠키가 ECID로 대체되지 않은 경우 CRS 내보내기는 해당 방문자에 대해 작동하지 않습니다. 자세한 내용은 방문자 식별 및 [ID](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-visid.html) 서비스 [유예 기간을 참조하십시오](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/grace-period.html).

세부 사항 **테이블** (작업 공간에서 마우스 오른쪽 단추 클릭 **[!UICONTROL Tools]** > **[!UICONTROL Detail Table]** )에서 속성 값과 Analytics의 보고 및 분석과 통합하는 데 필요한 변수를 설정할 수 있습니다(Adobe Pipeline Services 사용).

1. **테이블 헤더를 마우스 오른쪽 단추로 클릭하고 새 고객 레코드 서비스를 클릭합니다.**

   ![](assets/6_4_CRS.png)

1. **내보내기 파일의 이름을 지정하고 저장합니다.**

   내보내기 파일 편집 창이 열립니다.

1. **쿼리** > **CRS 구성을 엽니다**.
1. **CRS 속성 > 새로 추가를 마우스 오른쪽 단추로 클릭합니다.**
1. **CRS** 속성 ****** 매개 변수를 입력합니다 ****.

   새 항목을 열고 내보내기 파일의 CRS 속성 *섹션에서 값을* 입력하거나 확인합니다.

   ![](assets/6_4_CRS1.png)

   <table id="table_8156A2C66C0E41D381C31F1082CCA479"> 
    <tbody> 
      <tr> 
      <td colname="col1"> <p><b>속성 이름</b> </p> </td> 
      <td colname="col2">보고 및 분석에 <i>표시되는</i> 고객 속성 <i>변수의 이름</i>. </td> 
      </tr> 
      <tr> 
      <td colname="col1"><b>속성 유형</b> </td> 
      <td colname="col2"> <p>이 매개 변수는 (<i>int</i>, <i>string</i>)의 값을 수락합니다. </p> <p>참고:속성이 Analytics에서 구독되지 <b>않은</b> 경우: <p> 
      <ul id="ul_B77BF6FDA3FB4F1BBF9380C2FD938270"> 
       <li id="li_3D099456AF6B4103B227D841C81AB936">Analytics에서 지원하는 유효한 속성 유형을 사용하여 속성이 만들어집니다(이 릴리스의 경우 <i>문자열</i> 및 <i>int</i>만제한). </li> 
       <li id="li_EA1DBDB2E6BE49278C6CD6A5503EDC8A">잘못된 속성 유형을 입력하면 Analytics 가입 실패 오류가 표시됩니다. </li> 
      </ul> </p> <p>속성이 Analytics에서 <b>이미</b> 구독된 경우: </p> <p> 
      <ul id="ul_16415B639F1C49A5AE9932C128184171"> 
       <li id="li_83C90D44FE5C4D979DEA786660C7F3EC">이미 가입한 속성에 대한 올바른 속성 유형을 입력해야 합니다. </li> 
       <li id="li_02C5024E335C4C59B4F7B0084232CC24">속성에 대해 잘못된 유형을 입력하면 해당 동작이 Analytics의 속성 유형 처리에 따라 달라집니다. </li> 
      </ul> </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><b>필드 이름</b> </p> </td> 
      <td colname="col2">속성 값이 선택된 차원 또는 지표의 이름입니다. <p>참고:CRS <i><b>속성</b></i> 아래의 <i>필드</i> 이름은 <b><i>선택한 속성을 기반으로 자동으로 채워지는 출력 필드</i> &gt; 필드 이름 <i>(</i></b> 선택한 속성에 따라 자동으로 채워짐)과 같아야 합니다. 필드 <i>이름이</i> 잘못된 경우 내보내기가 실행되지 않습니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. 마우스 오른쪽 단추를 **[!UICONTROL Report Suite]** > **[!UICONTROL Add New]**&#x200B;클릭합니다.
1. Enter the **[!UICONTROL Report Suite ID]**.

   새 항목을 열고 내보내기 파일의 보고서 세트 *섹션에서 값을* 입력하거나 확인합니다.

   <table id="table_A3279CADB74C441DA2E062E2123CE9D4"> 
    <tbody> 
      <tr> 
      <td colname="col1"><b>보고서 세트</b> </td> 
      <td colname="col2">내보낼 고객 속성 변수를 식별하는 보고 <i>및</i> 분석의 보고서 <i>세트의</i> ID입니다. <p> <p>참고:보고 <i>및 분석을</i> 사용하여 여러 보고서 세트에 추가할 수 있지만, 데이터 워크벤치 6.4는 <i>인덱스 0에</i>식별된 단일 보고서 세트만 내보냅니다. <p>이 필드에 입력한 보고서 세트 값은 보고서 세트 ID이며 보고서 세트의 이름이 아닙니다. </p> </p> </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. ECID 필드 매개 변수를 입력합니다.

   **ECID 필드**:Adobe Experience Cloud ID를 나타내는 프로필의 차원 이름입니다. 이것은 필수 필드이며 입력한 잘못된 차원 값은 내보내지지 않습니다.

1. (선택 사항) 방문자 ID 필드 매개 변수를 완료합니다.

   **방문자 ID 필드**:사용자가 데이터에서 방문자에 대한 다른 사용자 지정 ID를 전송하려는 경우 이 위치에서 사용자 지정 방문자 ID를 나타내는 차원 이름을 입력합니다. 선택 필드이며 비워 둘 수 있습니다.
