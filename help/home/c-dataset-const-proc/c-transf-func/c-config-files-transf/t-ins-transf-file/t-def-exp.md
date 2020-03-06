---
description: 내보내기는 이벤트 데이터를 출력하는 방법에 대한 지침을 제공합니다.
solution: Analytics
title: 수출자 정의
topic: Data workbench
uuid: 565d4482-6c25-407c-bda7-0d116180902a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 수출자 정의{#defining-exporters}

내보내기는 이벤트 데이터를 출력하는 방법에 대한 지침을 제공합니다.

변환 기능은 파일, 로그 파일, XML 파일 및 ODBC 데이터를 파일, 텍스트 파일 또는 DataWarehouse 로드 루틴, 감사 기관 또는 기타 대상에 사용할 수 있는 구분된 텍스트 파일로 내보내는 세 가지 내보내기 형식을 제공합니다. [!DNL .vsl] [!DNL .vsl]

>[!NOTE]
>
>내보내기가 제대로 작동하려면 로그 소스가 로그 처리 구성 파일의 [로그 소스](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea) 섹션에서 설명한 적절한 요구 사항을 [충족해야 합니다](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

**내보내기를 정의하려면**

1. 데이터 [!DNL Transform.cfg] 워크벤치에서 엽니다. Insight [Transform.cfg 파일을](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13)편집하려면 을 참조하십시오.
1. 마우스 오른쪽 버튼을 클릭한 **[!UICONTROL Exporters]**&#x200B;다음 을 클릭합니다 **[!UICONTROL Add New]**.
1. 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL ExportTextFile]**
   * **[!UICONTROL ExportDelimitedTextFile]**
   * **[!UICONTROL ExportVSLFile]**
   >[!NOTE]
   >
   >이 [!DNL ExportVSLFile] 옵션의 경우 입력 파일의 모든 확장 필드와 cs(*header*) 양식의 모든 사용자 정의 필드는 항상 VSL 출력 파일에 기록됩니다. 기존 확장 필드를 덮어쓰면 필드가 비어 있어도 새 값이 출력 파일에 기록됩니다.

1. 다음 표를 참조하여 구성 파일에서 내보내기 매개 변수를 편집합니다.

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
      <td colname="col2"> <p>ExportTextFile <span class="wintitle"> 에만</span> 해당합니다. 필드 이름으로 구성된 각 출력 줄의 형식은 이스케이프됩니다(%fieldname%<i></i>%). 원하는 기타 모든 고정 텍스트입니다. 형식에는 선 구분 문자(일반적으로 [CR] [LF]가 포함되어야 합니다. </p> <p> 다음과 같이 문자를 escape하여 형식 문자열에 리터럴 백분율 기호(%)를 포함할 수 있습니다.%% </p> <p> 데이터 형식 매개 변수의 항목 예는 <span class="filepath"> %x-timestring% %x-trackingid%[CR][LF]</span>입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 필드 </td> 
      <td colname="col2">Export구분된 <span class="wintitle"> TextFile에만</span> 해당합니다. 출력할 필드의 이름입니다. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 구분 기호 </td> 
      <td colname="col2"> <p>선택 사항입니다. Export구분된 <span class="wintitle"> TextFile에만</span> 해당합니다. 출력 파일의 필드를 구분하는 데 사용되는 문자입니다. </p> <p> 소프트웨어는 데이터 값에 포함된 구분 기호를 escape할 수 없습니다. 따라서 쉼표를 구분 기호로 사용하는 것은 권장되지 않습니다. </p> <p> Ctrl 키를 누른 채로 구분 기호 매개 변수 내에서 마우스 오른쪽 단추를 클릭하면 삽입 <span class="wintitle"> 메뉴가</span> 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자 목록이 포함되어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 선 구분 기호 </td> 
      <td colname="col2">선택 사항입니다. Export구분된 <span class="wintitle"> TextFile에만</span> 해당합니다. 출력 파일에서 라인을 구분하는 데 사용되는 문자입니다. 기본값은 [CR] [LF]입니다. </td> 
      </tr> 
      <tr> 
      <td colname="col1">  이름  </td> 
      <td colname="col2"> <p>선택 사항입니다. 내보내기의 식별자입니다. 이 이름은 세부 상태 <span class="wintitle"> 인터페이스에 표시됩니다</span> . </p> <p> 자세한 상태 <span class="wintitle"> 인터페이스에 대한</span> 자세한 내용은 데이터 워크벤치 <i>사용자 안내서를 참조하십시오</i>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 설명 </td> 
      <td colname="col2"> 선택 사항입니다. 내보내기 도구에 대한 참고 사항. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 출력 경로 </td> 
      <td colname="col2"> <p>출력 파일을 저장할 경로입니다. 경로는 데이터 워크벤치 서버 설치 폴더에 상대적입니다. </p> <p> <p>참고:출력 데이터를 저장하는 데이터 워크벤치 서버는 profile.cfg <span class="filepath"> 파일에서 서버 #0을</span> 처리하고 있습니다. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 파일 순환 기간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 출력 파일로 데이터를 내보내는 빈도. 각 출력 파일에는 순환 기간이라는 특정 기간과 관련된 데이터가 들어 있습니다. 모든 시간 계산은 GMT입니다.파일에 기록된 데이터에 현지 시간으로 변환된 필드가 포함되어 있더라도 어느 날은 자정 GMT에 시작하여 다음 날 자정 GMT에 종료됩니다. </p> <p> 사용 가능한 값은 다음과 같습니다. </p> 
      <ul id="ul_64F56D093E2E4D07ACB7D7921F4E6FA1"> 
       <li id="li_E4985C7F56E443049AFF57B0270032D6"> 연도. 각 파일에는 1년의 데이터가 포함됩니다. </li> 
       <li id="li_42E59BB7A5704C85A6079ED9715C44BC"> 개월. 각 파일에는 한 달력의 데이터가 들어 있습니다. 월 번호는 1(1월)부터 12(12월)까지입니다. </li> 
       <li id="li_91831283616C48DA8C8086776D181751"> 주 각 파일에는 1주 동안의 데이터가 들어 있습니다. 일주일은 월요일부터 시작한다. 연도의 첫 7일 중 하나에서 시작하는 주는 1주이고, 이전(부분) 주가 있는 경우 0주입니다. </li> 
       <li id="li_BDB7B4D779434B98935261B8B5C0AABB"> 하루 각 파일에는 하루 동안의 데이터가 포함됩니다. </li> 
       <li id="li_018F4133E03C42F29073FED1DB082ED5"> 시간. 각 파일에는 1시간 동안의 데이터가 들어 있습니다. </li> 
       <li id="li_EE8CF71BA12149F49D4B7F7108262CD0"> NONE. 회전이 수행되지 않습니다. 모든 데이터는 동일한 파일(또는 다른 매개 변수 설정에 의해 결정된 파일 집합)에 기록됩니다. 이 표에서 <span class="wintitle"> 파일 이름 형식</span> 매개 변수를 참조하십시오. </li> 
      </ul> <p>기본 파일 순환 기간은 DAY입니다. </p> 
      <ul id="ul_0F3BC98275634F759E5022FF2C19715E"> 
       <li id="li_24DC4D144DA94ED0B7B50E8BB39DB8E3"> 오프라인 모드에서 작업하는 경우에만 파일 회전을 NONE으로 <span class="wintitle"> 설정합니다</span>. 오프라인 모드 <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13"> 매개 변수</a> 설명을 참조하십시오. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 파일 이름 형식 </td> 
      <td colname="col2"> <p>선택 사항입니다. 출력 파일 이름의 형식입니다. </p> <p> 각 로그 항목은 회전 기간의 시작 시간에서 파생된 파일에 저장할 수 있으며, 필요에 따라 포함하는 행의 필드 값에서 가져올 수 있습니다. 파일 이름에 사용할 필드는 필드 이름 이스케이프하므로 포함됩니다(%<i>fieldname</i>%). </p> <p>회전 기간과 관련된 파일 이름 구성 요소는 다음 이스케이프 시퀀스를 사용하여 형식 문자열에 포함됩니다. 
      <ul id="ul_3C5C8C5DC9104070ABCFDD85F49BE596"> 
       <li id="li_B100AE13FEA84AB6A1138CF58440E29E"> %yyyy%(4자리 연도) </li> 
       <li id="li_0583970798494A1795B03866DC717FB9"> %yy%(두 자리 연도) </li> 
       <li id="li_10AA96200F294364A5CE9DC3F22C789A"> %mm%(두 자리 월, 01 - 12) </li> 
       <li id="li_E112E367F62147C49751D6894E47607C"> %ww%(2자리 주, 01 - 52) </li> 
       <li id="li_C4B30E38C05942BB8CAA92F3C9B98A3C"> %dd%(2자리 날짜, 01 - 31) </li> 
       <li id="li_0318CA8C4DC441B48C16B29A615F3293"> %HH%(두 자리 시간, 00 - 23) </li> 
      </ul> </p> <p> 기본 파일 이름 형식은 <span class="filepath"> %yyyy%%mm%%dd%-%x-mask%.txt입니다.</span> </p> 
      <ul id="ul_07AE3624E7D74632AD5E5F164048196F"> 
       <li id="li_BA5C2BFBA73D4AAD8D729B30FF812759"> 이스케이프 시퀀스는 대/소문자를 구분합니다. </li> 
       <li id="li_32CB9C98190D4B17B4DA84732CFB9E2F"> [파일 회전 기간]을 [없음]으로 설정하면 이스케이프 시퀀스의 각 값으로 빈 문자열이 대체됩니다(있는 경우). </li> 
       <li id="li_C64731961ED6402FB92210A42854BA72"> 파일 이름 형식으로 인해 <span class="wintitle"> 각 순환</span> 기간에 대한 고유한 파일 이름이 만들어지지 않는 경우 오류가 생성됩니다(이 표의 파일 순환 기간 매개 변수 참조). 예를 들어 DAY 순환 기간을 사용할 때 데이터 손실을 방지하기 위해 %dd%, %mm%, %yy% 또는 %yyyy% 이스케이프 시퀀스가 패턴에 있어야 합니다. </li> 
       <li id="li_15CDA2ABE450418FA8D9C4BC581C4ADD"> 패턴 내에서 필드 이름 이스케이프 시퀀스를 사용하고 주어진 필드에 서로 다른 값이 많이 있는 경우 회전 기간마다 많은 출력 파일이 작성됩니다. 이 시나리오로 인해 성능이 저하될 수 있으므로 이 기능을 신중하게 사용해야 합니다. </li> 
       <li id="li_D0F75E4FFAFF47C4AA8A8D14A6E1C18A"> 모든 시간 계산은 GMT로 합니다. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 롤오버 시 실행 </td> 
      <td colname="col2"> <p>선택 사항입니다. 각 파일이 완료되면 외부(Windows) 명령을 실행할 수 있습니다. 명령줄은 다음 이스케이프 시퀀스를 이 매개 변수로 대체하여 최종 파일 이름에서 파생됩니다. </p> 
      <ul id="ul_5E16832BDBEA4757A2C02DE4B019A122"> 
       <li id="li_6A74D069353E4FE781657BF492675220"> %dir%. 후행 백슬래시를 포함하여 최종 파일 이름의 디렉토리 부분. </li> 
       <li id="li_2CF7232553C348089B1395BBB0BBD6AE"> %file%. 최종 파일의 파일 이름(디렉토리 및 확장명 제외). </li> 
       <li id="li_901BAB90E5EA434F9EE37A60477F4591"> %ext%. 확장(행간 "." 포함) 의 최종 파일 이름을 지정합니다. </li> 
       <li id="li_AD7269A67A0041438A6951FD1898D458"> %경로%. 파일의 전체 경로 이름입니다. %dir%%file%%ext%에 해당합니다. </li> 
      </ul> <p> 기본적으로 이 매개 변수는 비어 있습니다(명령이 실행되지 않음). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 메모리 제한 </td> 
      <td colname="col2"> <p>선택 사항입니다. 내보내기 프로그램의 출력을 버퍼링하는 데 사용되는 메모리 크기(바이트)입니다. 기본값은 10,000,000바이트입니다. </p> <p> <p>참고: 동시에 열려 있는 출력 파일이 많은 경우 이 값을 늘릴 수 있지만 시스템의 다른 구성 요소에서 사용할 수 있는 메모리 양을 줄일 수 있습니다. 그러나 이 값을 줄이면 내보내기 프로세스가 느려질 수 있습니다. 도움이 필요하면 Adobe에 문의하십시오. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> 파일 열기 제한 </td> 
      <td colname="col2"> <p>선택 사항입니다. 내보내기에서 출력하기 위해 동시에 열 수 있는 최대 파일 수입니다. 이 수를 초과하면 이벤트 로그에 오류가 기록되고 데이터 워크벤치 서버 실행이 중지됩니다. 기본값은 1000입니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. 내보내기를 정의하고 다른 매개 변수를 변경한 후 [!DNL Transform.cfg] 파일을 로컬에 저장하고 데이터 워크벤치 서버 시스템의 해당 프로필에 저장합니다.
