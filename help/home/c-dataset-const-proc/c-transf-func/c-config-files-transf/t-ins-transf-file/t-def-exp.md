---
description: 이벤트 데이터를 출력하는 사용자는 이를 출력하기 위한 지침을 제공합니다.
title: 내보내기 정의
uuid: 565d4482-6c25-407c-bda7-0d116180902a
exl-id: 5de6266a-e959-414c-9512-5e9f4011881b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 2%

---

# 내보내기 정의{#defining-exporters}

이벤트 데이터를 출력하는 사용자는 이를 출력하기 위한 지침을 제공합니다.

변형 기능은 [!DNL .vsl] 파일, 로그 파일, XML 파일 및 ODBC 데이터를 DataWarehouse 로드 루틴, 감사 기관 또는 기타 타겟에서 사용할 수 있는 [!DNL .vsl] 파일, 텍스트 파일 또는 구분된 텍스트 파일로 내보내는 세 가지 내보내기 유형을 제공합니다.

>[!NOTE]
>
>내보내기가 제대로 작동하려면 로그 소스가 [로그 처리 구성 파일](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md)의 [로그 소스](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea) 섹션에서 설명한 적절한 요구 사항을 충족해야 합니다.

**내보내기 도구를 정의하려면**

1. 데이터 워크벤치에서 [!DNL Transform.cfg]을(를) 엽니다. [Insight Transform.cfg 파일을 편집하려면](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13)을 참조하십시오.
1. **[!UICONTROL Exporters]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add New]**&#x200B;을 클릭합니다.
1. 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL ExportTextFile]**
   * **[!UICONTROL ExportDelimitedTextFile]**
   * **[!UICONTROL ExportVSLFile]**

   >[!NOTE]
   >
   >[!DNL ExportVSLFile] 옵션의 경우 입력 파일의 모든 확장 필드와 cs(*header*) 형식의 모든 사용자 정의 필드가 항상 VSL 출력 파일에 기록됩니다. 기존 확장 필드를 덮어쓰면 필드가 비어 있어도 새 값이 출력 파일에 기록됩니다.

1. 다음 표를 안내서로 사용하여 구성 파일에서 내보내기 매개 변수를 편집합니다.

   <table id="table_35C380DB6E4F42448C149D5EC185213C"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> 매개 변수 </th> 
      <th colname="col2" class="entry"> 설명 </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> 데이터 형식 </td> 
      <td colname="col2"> <p><span class="wintitle"> ExportTextFile</span>에만 해당됩니다. 필드 이름으로 구성된 각 출력 라인의 형식은 이스케이프됩니다(%<i>fieldname</i>%). 그리고 원하는 기타 고정 텍스트로 표현됩니다. 형식에는 일반적으로 [CR] [LF]인 줄 구분 기호가 포함되어야 합니다. </p> <p> 다음과 같이 문자를 escape하여 형식 문자열에 리터럴 백분율 기호(%)를 포함할 수 있습니다.%% </p> <p> 데이터 형식 매개 변수의 항목의 예는 <span class="filepath"> %x-timestring% %x-trackingid%[CR][LF]</span>입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 필드 </td> 
      <td colname="col2"><span class="wintitle"> Export구분된 텍스트 파일</span>에만 해당됩니다. 출력할 필드의 이름입니다. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 구분 기호 </td> 
      <td colname="col2"> <p>선택 사항입니다. <span class="wintitle"> Export구분된 텍스트 파일</span>에만 해당됩니다. 출력 파일의 필드를 구분하는 데 사용되는 문자입니다. </p> <p> 소프트웨어는 데이터 값에 포함된 구분 기호를 escape할 수 없습니다. 따라서 Adobe에서는 쉼표를 구분 기호로 사용하는 것이 권장되지 않습니다. </p> <p> Ctrl 키를 누른 채 구분 기호 매개 변수 내에서 마우스 오른쪽 단추를 클릭하면 <span class="wintitle"> 삽입</span> 메뉴가 나타납니다. 이 메뉴에는 자주 구분 기호로 사용되는 특수 문자 목록이 포함되어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 줄 구분 기호 </td> 
      <td colname="col2">선택 사항입니다. <span class="wintitle"> Export구분된 텍스트 파일</span>에만 해당됩니다. 출력 파일에서 행을 구분하는 데 사용되는 문자입니다. 기본값은 [CR] [LF]입니다. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 이름 </td> 
      <td colname="col2"> <p>선택 사항입니다. 내보내기 프로그램의 식별자입니다. 이 이름은 <span class="wintitle"> 세부 상태</span> 인터페이스에 표시됩니다. </p> <p> <span class="wintitle"> 세부 상태</span> 인터페이스에 대한 자세한 내용은 <i>Data Workbench 사용자 안내서</i>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 댓글 </td> 
      <td colname="col2"> 선택 사항입니다. 내보내기 도구에 대한 참고 사항. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 출력 경로 </td> 
      <td colname="col2"> <p>출력 파일을 저장할 경로입니다. 경로는 데이터 워크벤치 서버 설치 폴더에 상대적입니다. </p> <p> <p>참고:출력 데이터를 저장하는 데이터 워크벤치 서버는 <span class="filepath"> profile.cfg</span> 파일의 #0 처리 서버있습니다. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 파일 순환 기간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 데이터를 출력 파일로 내보내는 빈도. 각 출력 파일에는 순환 기간이라는 특정 기간과 관련된 데이터가 포함됩니다. 모든 시간 계산은 GMT입니다.파일에 기록된 데이터에 현지 시간으로 변환된 필드가 포함되어 있더라도 어느 날은 자정 GMT에 시작하여 그 다음 날 자정 GMT에 종료됩니다. </p> <p> 사용 가능한 값은 다음과 같습니다. </p> 
      <ul id="ul_64F56D093E2E4D07ACB7D7921F4E6FA1"> 
       <li id="li_E4985C7F56E443049AFF57B0270032D6"> 연도. 각 파일에는 1년의 데이터가 포함됩니다. </li> 
       <li id="li_42E59BB7A5704C85A6079ED9715C44BC"> 개월. 각 파일에는 한 달력의 데이터가 들어 있습니다. 달은 1(1월)부터 12(12월)까지 번호가 매겨집니다. </li> 
       <li id="li_91831283616C48DA8C8086776D181751"> 주. 각 파일에는 1주일 동안의 데이터가 들어 있습니다. 일주일은 월요일부터 시작한다. 연도의 첫 7일 중 하나에서 시작하는 주는 1주이고, 이전(일부) 주가 있는 경우 0주입니다. </li> 
       <li id="li_BDB7B4D779434B98935261B8B5C0AABB"> 오늘. 각 파일에는 1일 동안의 데이터가 들어 있습니다. </li> 
       <li id="li_018F4133E03C42F29073FED1DB082ED5"> 시간. 각 파일에는 1시간 동안의 데이터가 들어 있습니다. </li> 
       <li id="li_EE8CF71BA12149F49D4B7F7108262CD0"> NONE. 회전이 수행되지 않습니다. 모든 데이터는 동일한 파일(또는 다른 매개 변수 설정에 의해 결정된 파일 세트)에 기록됩니다. 이 표에서 <span class="wintitle"> 파일 이름 형식</span> 매개 변수를 참조하십시오. </li> 
      </ul> <p>기본 파일 순환 기간은 DAY입니다. </p> 
      <ul id="ul_0F3BC98275634F759E5022FF2C19715E"> 
       <li id="li_24DC4D144DA94ED0B7B50E8BB39DB8E3"> <span class="wintitle"> 오프라인 모드</span>에서 작업하는 경우에만 파일 회전을 NONE으로 설정합니다. <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13"> 오프라인 모드</a> 매개 변수 설명을 참조하십시오. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 파일 이름 형식 </td> 
      <td colname="col2"> <p>선택 사항입니다. 출력 파일 이름의 형식입니다. </p> <p> 각 로그 항목은 순환 기간의 시작 시간부터 이름이 파생되는 파일에 저장할 수 있으며, 필요에 따라 해당 항목이 포함된 행의 필드 값에서 가져올 수 있습니다. 파일 이름에 사용할 필드는 필드 이름 이스케이프로서 포함됩니다(%<i>fieldname</i>%). </p> <p>순환 기간과 관련된 파일 이름 구성 요소는 다음 이스케이프 시퀀스를 사용하여 형식 문자열에 포함됩니다. 
      <ul id="ul_3C5C8C5DC9104070ABCFDD85F49BE596"> 
       <li id="li_B100AE13FEA84AB6A1138CF58440E29E"> %yyyy%(4자리 연도) </li> 
       <li id="li_0583970798494A1795B03866DC717FB9"> %yy%(2자리 연도) </li> 
       <li id="li_10AA96200F294364A5CE9DC3F22C789A"> %mm%(2자리 월, 01 - 12) </li> 
       <li id="li_E112E367F62147C49751D6894E47607C"> %ww%(2자리 주, 01 - 52) </li> 
       <li id="li_C4B30E38C05942BB8CAA92F3C9B98A3C"> %dd%(2자리 일, 01 - 31) </li> 
       <li id="li_0318CA8C4DC441B48C16B29A615F3293"> %HH%(2자리 시간, 00 - 23) </li> 
      </ul> </p> <p> 기본 파일 이름 형식은 <span class="filepath"> %yyy%%mm%dd%-%x-mask%.txt</span>입니다. </p> 
      <ul id="ul_07AE3624E7D74632AD5E5F164048196F"> 
       <li id="li_BA5C2BFBA73D4AAD8D729B30FF812759"> 이스케이프 시퀀스는 대/소문자를 구분합니다. </li> 
       <li id="li_32CB9C98190D4B17B4DA84732CFB9E2F"> [파일 회전 기간]을 [없음]으로 설정하면 이스케이프 시퀀스의 각 값으로 빈 문자열이 대체됩니다(있는 경우). </li> 
       <li id="li_C64731961ED6402FB92210A42854BA72"> <span class="wintitle"> 파일 이름 형식</span>이 각 순환 기간에 대한 고유한 파일 이름을 만들지 않으면 오류가 생성됩니다(이 표의 파일 순환 기간 매개 변수 참조). 예를 들어 DAY 순환 기간을 사용할 때 데이터 손실을 방지하기 위해 %dd%, %mm%, %y% 또는 %yyyyy% 이스케이프 시퀀스가 패턴에 있어야 합니다. </li> 
       <li id="li_15CDA2ABE450418FA8D9C4BC581C4ADD"> 패턴 내에서 필드 이름 이스케이프 시퀀스를 사용하고 주어진 필드에 서로 다른 많은 값이 있는 경우 각 회전 기간에 대해 많은 출력 파일이 작성됩니다. 이 시나리오는 성능이 저하될 수 있으므로 이 기능을 주의해서 사용해야 합니다. </li> 
       <li id="li_D0F75E4FFAFF47C4AA8A8D14A6E1C18A"> 모든 시간 계산은 GMT입니다. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 롤오버 시 실행 </td> 
      <td colname="col2"> <p>선택 사항입니다. 각 파일이 완료되면 외부(Windows) 명령을 실행할 수 있습니다. 명령줄은 다음 이스케이프 시퀀스를 이 매개 변수로 대체하여 최종 파일 이름에서 파생됩니다. </p> 
      <ul id="ul_5E16832BDBEA4757A2C02DE4B019A122"> 
       <li id="li_6A74D069353E4FE781657BF492675220"> %dir%. 후행 백슬래시를 포함하여 최종 파일 이름의 디렉토리 부분. </li> 
       <li id="li_2CF7232553C348089B1395BBB0BBD6AE"> %file%입니다. 최종 파일의 파일 이름(디렉토리 및 확장명 제외). </li> 
       <li id="li_901BAB90E5EA434F9EE37A60477F4591"> %ext%. 확장(행간 "." 포함) 를 최종 파일 이름으로 변경합니다. </li> 
       <li id="li_AD7269A67A0041438A6951FD1898D458"> %경로%. 파일의 전체 경로 이름(%dir%%file%%ext%에 해당합니다. </li> 
      </ul> <p> 기본적으로 이 매개 변수는 비어 있습니다(명령이 실행되지 않음). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 메모리 제한 </td> 
      <td colname="col2"> <p>선택 사항입니다. 내보내기 프로그램의 출력을 버퍼링하는 데 사용되는 메모리 양(바이트)입니다. 기본값은 10,000,000바이트입니다. </p> <p> <p>참고: 동시에 열려 있는 많은 출력 파일이 있는 경우 이 값을 늘리겠지만 시스템의 다른 구성 요소에서 사용할 수 있는 메모리 양을 줄일 수 있습니다. 그러나 이 값을 줄이면 내보내기 프로세스가 느려질 수 있습니다. 도움이 필요하면 Adobe에 문의하십시오. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 열린 파일 제한 </td> 
      <td colname="col2"> <p>선택 사항입니다. 내보내기에서 출력하기 위해 동시에 열 수 있는 최대 파일 수입니다. 이 수가 초과되면 이벤트 로그에 오류가 기록되고 데이터 워크벤치 서버 실행이 중지됩니다. 기본값은 1000입니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. [!DNL Transform.cfg] 파일에서 내보내기를 정의하고 다른 매개 변수를 변경한 후 파일을 로컬로 저장하고 데이터 워크벤치 서버 컴퓨터의 해당 프로필에 저장합니다.
