---
description: CRS(Customer Record Service) 내보내기 기능을 사용하면 Reports & Analytics를 포함하여 다른 Analytics 기능과 통합하도록 Data Workbench 데이터를 Adobe Analytics 핵심 서비스로 내보낼 수 있습니다.
title: Analytics Core Services로 내보내기
uuid: 8fd7e8d8-989a-4ad6-bab5-61bfd37b0201
exl-id: 573085e8-2260-4872-be90-a84ad61145bb
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 2%

---

# Analytics Core Services로 내보내기{#exporting-to-analytics-core-services}

CRS(Customer Record Service) 내보내기 기능을 사용하면 Reports &amp; Analytics를 포함하여 다른 Analytics 기능과 통합하도록 Data Workbench 데이터를 Adobe Analytics 핵심 서비스로 내보낼 수 있습니다.

>[!NOTE]
>
>CRS 내보내기 기능이 작동하려면 방문자의 Analytics ID가 ECID(Experience Cloud ID Service)를 기반으로 해야 합니다. 방문자의 Data Workbench에 ECID를 채울 수 있지만 클라이언트가 유예 기간 중이거나 방문자의 쿠키가 ECID로 대체되지 않은 경우 해당 방문자에 대해 CRS 내보내기가 작동하지 않습니다. 자세한 내용은 [방문자 식별](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-visid.html) 및 [ID 서비스 유예 기간](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/grace-period.html)을 참조하십시오.

**세부 테이블**(작업 공간에서 **[!UICONTROL Tools]** > **[!UICONTROL Detail Table]** 마우스 오른쪽 단추 클릭)에서 속성 값 및 Analytics의 Reports &amp; Analytics와 통합(Adobe 파이프라인 서비스 사용)하는 데 필요한 변수를 설정할 수 있습니다.

1. **테이블 헤더를 마우스 오른쪽 단추로 클릭하고 새 고객 레코드 서비스를 클릭합니다.**

   ![](assets/6_4_CRS.png)

1. **내보내기 파일의 이름을 지정하고 저장합니다.**

   파일 내보내기 편집 창이 열립니다.

1. **** **OpenQuery > CRS 구성**&#x200B;을 참조하십시오.
1. **CRS Attributes > 새로 추가 를 마우스 오른쪽 단추로 클릭합니다.**
1. **** ***CRS 속성*** **매개 변수를 입력합니다**.

   새 항목을 열고 내보내기 파일의 *CRS Attributes* 섹션에 값을 입력하거나 확인합니다.

   ![](assets/6_4_CRS1.png)

   <table id="table_8156A2C66C0E41D381C31F1082CCA479"> 
    <tbody> 
      <tr> 
      <td colname="col1"> <p><b>속성 이름</b> </p> </td> 
      <td colname="col2"><i>Reports &amp; Analytics</i>에 표시되는 <i>고객 속성</i> 변수의 이름입니다. </td> 
      </tr> 
      <tr> 
      <td colname="col1"><b>속성 유형</b> </td> 
      <td colname="col2"> <p>이 매개 변수는 (<i>int</i>, <i>문자열</i>)의 값을 허용합니다. </p> <p>참고: 특성이 Analytics에 구독되지 않은 <b>인 경우:</b> <p> 
      <ul id="ul_B77BF6FDA3FB4F1BBF9380C2FD938270"> 
       <li id="li_3D099456AF6B4103B227D841C81AB936">속성은 Analytics에서 지원하는 유효한 속성 유형으로 작성됩니다. 이 릴리스에는 <i>string</i> 및 <i>int</i>만 사용할 수 있습니다. </li> 
       <li id="li_EA1DBDB2E6BE49278C6CD6A5503EDC8A">잘못된 속성 유형을 입력하면 Analytics 가입 실패를 나타내는 오류가 표시됩니다. </li> 
      </ul> </p> <p>특성이 <b>이미 Analytics에 가입되어 있는 경우:</b> </p> <p> 
      <ul id="ul_16415B639F1C49A5AE9932C128184171"> 
       <li id="li_83C90D44FE5C4D979DEA786660C7F3EC">이미 가입한 속성에 대해 올바른 속성 유형을 입력해야 합니다. </li> 
       <li id="li_02C5024E335C4C59B4F7B0084232CC24">속성에 대해 잘못된 유형을 입력하면 해당 동작은 Analytics의 속성 유형 처리에 따라 달라집니다. </li> 
      </ul> </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><b>필드 이름</b> </p> </td> 
      <td colname="col2">속성 값을 선택한 차원 또는 지표의 이름입니다. <p>참고: <i>CRS 속성</i> 아래의 <i><b>필드 이름</b></i>은 <b><i>출력 필드</i> &gt; <i>필드 이름</i></b>(선택한 속성에 따라 자동으로 채워짐)와 같아야 합니다. <i>필드 이름</i>이 잘못된 경우 내보내기가 실행되지 않습니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. **[!UICONTROL Report Suite]** > **[!UICONTROL Add New]** 을 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL Report Suite ID]** 을 입력합니다.

   새 항목을 열고 내보내기 파일의 *보고서 세트* 섹션에 값을 입력하거나 확인합니다.

   <table id="table_A3279CADB74C441DA2E062E2123CE9D4"> 
    <tbody> 
      <tr> 
      <td colname="col1"><b>보고서 세트</b> </td> 
      <td colname="col2">내보낼 <i>고객 속성</i> 변수를 식별하는 <i>Reports &amp; Analytics</i>에 있는 보고서 세트의 ID입니다. <p> <p>참고: <i>Reports &amp; Analytics</i>를 사용하면 여러 보고서 세트에 추가할 수 있지만, Data Workbench 6.4는 <i>인덱스 0</i>에서 식별된 단일 보고서 세트만 내보냅니다. <p>이 필드에 입력한 보고서 세트 값은 보고서 세트 ID(보고서 세트의 이름이 아님)입니다. </p> </p> </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. ECID Field 매개 변수를 입력합니다.

   **ECID 필드**: Adobe Experience Cloud ID를 나타내는 프로필의 차원 이름입니다. 필수 필드이며 입력한 잘못된 차원 값은 내보내지지 않습니다.

1. (선택 사항) 방문자 ID 필드 매개 변수를 완료합니다.

   **방문자 ID 필드**: 사용자가 데이터에서 방문자에 대한 다른 사용자 지정 ID를 전송하려는 경우 이 단계에서 사용자 지정 방문자 ID를 나타내는 차원의 이름을 입력합니다. 선택적 필드이며 비워 둘 수 있습니다.
