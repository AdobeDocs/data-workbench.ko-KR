---
description: Report.cfg 매개 변수에 대한 정보입니다.
solution: Analytics
title: Report.cfg 매개 변수
topic: Data workbench
uuid: 7a20f4f6-99e6-401a-ba3c-c508881c0f0d
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Report.cfg 매개 변수{#report-cfg-parameters}

Report.cfg 매개 변수에 대한 정보입니다.

보고서 세트 [!DNL Report.cfg] 구성에 [표시된 샘플에는](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) 기본적으로 파일에 포함된 [!DNL Report.cfg] 매개 변수만 포함되어 있습니다. 다음 표에서는 사용 가능한 모든 [!DNL Report.cfg] 파일 매개 변수에 대한 설명을 제공합니다.

파일에 매개 변수를 추가로 추가해야 하는 경우 텍스트 편집기를 사용하여 [!DNL Report.cfg] 추가해야 합니다. 각 매개 변수 항목을 정의하는 방법의 예를 포함하여 이를 위한 단계는 기존 Report.cfg [파일 편집을 참조하십시오](../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887).

>[!NOTE]
>
>이 표의 매개 변수는 알파벳 순으로 나열됩니다. 데이터 워크벤치에서 파일을 열면 벡터가 알파벳 순으로 나열되고 개별 매개 변수가 알파벳 순으로 나열됩니다. [!DNL Report.cfg]

<table id="table_F55E925EA34F43B6832788BB6878BB4A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 경고 임계값 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수는 지표 표시기가 있는 보고서에만 적용됩니다. 경고 보고서가 전송되기 전에 워크시트에 표시해야 하는 지표 수입니다. </p> <p>지표 지표 지표 워크시트에서 하나의 지표만 모니터하는 경우 임계값을 1로 설정합니다. 시트의 지표가 위쪽/아래쪽 화살표 또는 X로 평가되면 보고서가 생성됩니다.보고서에서 두 개 이상의 지표가 모니터되는 경우 보고서를 생성하기 전에 위쪽/아래쪽 화살표 또는 X로 평가해야 하는 지표 지표를 선택할 수 있습니다. 예를 들어 두 개의 지표가 모니터되는 경우: 
     <ul id="ul_A64E8A2306B14371A233D372B956F64D"> 
      <li id="li_2A3020ED350644A3954C36D3EB0B86D4">임계값이 1로 설정된 경우 시트의 지표 중 하나가 위쪽/아래쪽 화살표 또는 X로 평가되면 보고서가 생성됩니다. </li> 
      <li id="li_DA4EF4984880483DA48322D9D57B9240">임계값이 2로 설정된 경우 두 지표 모두 보고서를 생성하기 전에 위쪽/아래쪽 화살표 또는 X로 평가되어야 합니다. </li> 
     </ul> </p> <p>지표 표시기에 대한 자세한 내용은 데이터 워크벤치 <i>사용 안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 보고서 재생성 허용 </td> 
   <td colname="col2"> <p>보고서를 <span class="keyword"> 만들거나 수정할 때 보고서 서버가 특정 보고서를 </span> 자동으로 생성하거나 재생성하는지 여부를 나타냅니다. 옵션은 true 또는 false입니다. true로 설정된 경우 보고서 작업 영역을 만들거나 수정하면 보고서 <span class="keyword"> 서버가 최근 실행을 위해 해당 </span> 보고서를 다시 생성합니다. </p> <p> <p>참고: Report. <span class="filepath"> cfg </span> 파일을 변경하면 <span class="keyword"> 보고서 서버가 해당 Report.cfg </span> 파일에 의해 제어되는 모든 보고서를 <span class="filepath"> 다시 </span> 생성합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 첨부 파일 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 첨부 파일 수를 포함하여 이메일을 통해 배포된 보고서와 함께 나가는 첨부 파일의 이름 및 컨텐츠 유형에 대한 섹션 식별자입니다. </p> <p>새 첨부 파일을 추가하려면: 
     <ol id="ol_CBDC1E95D34A4D08A862680127438433"> 
      <li id="li_784C48C540534F4CBB35BBDA6BC5F48E">데이터 <span class="filepath"> 워크벤치에서 Report.cfg </span> 파일을 엽니다. </li> 
      <li id="li_0709ADDDDF2E469FAB10761B46173136">첨부 파일을 마우스 오른쪽 <span class="uicontrol"> 단추로 </span> 클릭하고 <span class="uicontrol"> 새 하위 </span> 추가 &gt; <span class="uicontrol"> 첨부 파일을 클릭합니다 </span>. </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 컨텐츠 유형 </td> 
   <td colname="col2"> <p>첨부할 파일의 콘텐트 유형입니다. </p> <p>예:이미지/jpeg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 이름 </td> 
   <td colname="col2"> <p>첨부할 파일의 위치 및 이름입니다. </p> <p>예:c:\myimage.jpg <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 색상 세트 </td> 
   <td colname="col2"> .png 파일에 사용할 색상 구성표를 <span class="filepath"> 식별합니다 </span> . 0은 검은색 배경입니다.1은 흰색 배경입니다.2는 회색 음영 이미지용입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 실행할 명령 </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 보고서 세트가 생성된 후 실행되는 배치 명령 또는 실행 파일입니다. 명령 셸 인터프리터의 시작이 필요한 경우 명령 앞에 cmd /c를 입력합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본 Excel 템플릿 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서를 Excel 파일로 생성할 때 사용할 일반 Excel 템플릿 파일( <span class="filepath"> .xls </span> 또는 <span class="filepath"> .xlsx </span>)의 파일 이름입니다. 이 매개 변수는 c:\templates\mytemplate.xls과 같은 전체 파일 경로를 <span class="filepath"> 지원합니다 </span>. </p> <p>특정 보고서에 대해 템플릿이 특별히 정의되어 있지 않으면 이 파일은 모든 Excel 보고서에 사용됩니다. 템플릿 <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> 파일 사용을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 차원 이름 </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 보고서를 동적으로 생성할 차원의 이름입니다. 이 매개 변수에 차원 이름을 입력하는 경우 조회 파일 매개 변수 또는 상위 N 지표 및 상위 N 값 매개 변수에 값을 입력해야 합니다. 이 매개 변수에서 명명된 차원은 보고서를 만들 데이터 세트에 있어야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 완벽한 경우에만 이메일 </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 사용자가 실행 중에 오류가 발생하지 않은 경우에만 보고서 세트를 전송하도록 지정할 수 있습니다. 옵션이 true이고 false입니다. 기본값은 false입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 날짜 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 세트를 실행할 마지막 날짜 및 시간입니다. 이 시간은 데이터 세트의 기준 시간을 기반으로 합니다. </p> <p>형식:YYYY/MM/DD hh:mm 표준 시간대, 24시간 구문 사용 </p> <p>예:08/01/2007 12:01 EDT </p> <p>시간대 설정에 대한 자세한 내용은 데이터 집합 <i>구성 안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 각 </td> 
   <td colname="col2"> 보고서 세트 생성 빈도:일, 주 또는 월. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Excel 감시 시간 초과(초) </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 서버가 Excel 파일로 보고서를 생성할 때 Microsoft <span class="keyword"> Excel </span> 이 응답할 때까지 기다릴 시간(초)을 <span class="keyword"> 지정했다가 보고서 서버에서 Excel이 응답하지 않는다고 </span> 판단하여 프로세스를 종료합니다. 이 매개 변수를 사용하면 보고서 <span class="keyword"> 서버가 응답이 없을 때 Excel </span> 을 종료하고 Excel이 아닌 보고서를 계속 처리할 수 있습니다. 기본값은 300.0입니다.이 기능을 비활성화하려면 이 매개 변수를 0.0으로 설정합니다. </p> <p>정의한 값이 Excel로 내보낼 수 있을 만큼 길어야 합니다. 그렇지 않으면 <span class="keyword"> 보고서 서버가 Excel을 중간에 종료할 </span> 수 있으며 보고서가 생성되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필터 공식 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 세트의 모든 작업 영역에 적용되는 필터입니다. </p> <p>자세한 내용은 필터 만들기 <a href="https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Syntax_for_Filter_Expressions" format="http" scope="external"> 구문을 </a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 감마 교정 </td> 
   <td colname="col2"> <p>.png 파일 출력에 대한 <span class="filepath"> 감마 </span> 설정. 기본값은 1.6입니다. </p> <p> <p>참고: 이 값은 변경하지 않는 것이 좋습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로고 숨기기 </td> 
   <td colname="col2"> 보고서를 생성할 때 보고서 서버가 로고를 숨기는지 여부를 나타냅니다. 옵션은 <span class="filepath"> true </span> 또는 <span class="filepath"> false입니다 </span>. false로 설정된 <span class="filepath"> </span>경우 보고서 로고로 보고서가 생성됩니다. The default is <span class="filepath"> false </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조회 파일 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수가 채워지면 보고서 서버는 동적 모드로 실행되고 차원 이름 매개 변수에 지정된 차원의 각 요소에 대한 보고서를 생성합니다. 이 파일에는 두 개의 탭으로 구분된 열이 있어야 하며 머리글 행이 없어야 합니다. </p> <p> 
     <ul id="ul_378D4104BB5141C4A013EFE881BFFC6A"> 
      <li id="li_6F2C89A286B24FFE8EE8C82D278D0633">열 1에는 차원 요소 목록이 포함되어 있습니다. </li> 
      <li id="li_4BD1CAA77FEC43268B40489BC5E5E6F7">열 2에는 보고서 수신자의 이메일 주소가 포함되어 있습니다. 열 1의 지정된 요소에 대한 보고서가 열 2의 동일한 행에 있는 이메일 주소로 전송됩니다. 쉼표(공백 없음)로 구분하여 여러 이메일 주소를 입력할 수 있습니다. 보고서를 이메일로 보내지 않을 경우 이 열은 비어 있을 수 있지만 반드시 있어야 합니다. </li> 
     </ul> </p> <p> <p>참고: 이 매개 변수에 값을 입력할 경우 차원 이름 매개 변수에 값을 입력해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 알림 전용 </td> 
   <td colname="col2"> 이 <span class="wintitle"> 보고서 서버 </span> 설정을 사용하면 보고서가 생성될 때 이메일을 보내도록 데이터 워크벤치를 구성할 수 있습니다. 이 값을 <span class="filepath"> true로 설정하면 보고서가 </span> 전송되지 않고 구독된 사용자에게 보고서가 생성되었음을 알리는 전자 메일을 보냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 메일 보고서 </td> 
   <td colname="col2"> <p>이메일로 보고서를 배포하는 섹션 식별자입니다. 이메일로 보고서를 배포하려면 메일 보고서 항목에 대해 다음 매개 변수를 <span class="wintitle"> 작성하십시오 </span> . 보고서 세트의 모든 보고서는 수신자 매개 변수에 지정된 이메일 주소로 한 개의 메시지로 이메일로 전송됩니다. </p> <p> <p>참고: 보고서 서버가 하나 이상의 보고서를 생성한 경우에만 이메일을 보냅니다. </p> </p> <p>보고서 이메일을 전송하려면 이 항목에 대해 다음 매개 변수 이상을 완료해야 합니다. 
     <ul id="ul_539D64D61A8B4F1E95D889C6610EE3B8"> 
      <li id="li_D2EDBEE57BFE4FD4BB66F63AE561F1E2">SMTP 서버 </li> 
      <li id="li_4EEFE6CDA3384FE38149CE8DCBEFF847">수신자 </li> 
      <li id="li_CF9F0CF7ECFC4D88A7F4F11BAC4938D6">보낸 사람 주소 </li> 
      <li id="li_40BFDCDC9640488EBB450CF8579DA250">알림 전용 </li> 
     </ul> </p> <p> <p>참고: 보고서 세트를 다시 생성한 후 이메일로 보고서를 전송하려면 기존 Report.cfg <a href="../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887"> 파일 편집을 참조하십시오 </a>. </p> </p> <p>알림 전용 값은 5.4x 및 5.5x 릴리스에서 사용할 수 있습니다. </p> <p>20명 이상의 수신자에게 알림을 받으려면 이메일 배포 목록을 사용하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 본문 XSL 템플릿 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. reports.xml 파일에 적용할 XSL 템플릿 파일의 <span class="filepath"> 경로입니다 </span> . 이 매개 변수를 사용하면 보고서 서버가 배포된 이메일 내에 보고서를 첨부 파일로 보낼 수 있습니다. 결과 텍스트는 이메일 메시지의 본문으로 사용됩니다. </p> <p>샘플 <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> 파일은 보고서 샘플 </a> 파일을 참조하십시오. </p> <p>XSLT(Extensible Stylesheet Language)에 대한 자세한 내용은 The <a href="http://www.w3.org/Style/XSL/" format="http" scope="external"> Extensible Stylesheet Language Family를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 수신자 </td> 
   <td colname="col2"> 보고서를 보낼 사람의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 보낸 사람 주소 </td> 
   <td colname="col2"> 보낸 사람의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 보낸 사람 이름 </td> 
   <td colname="col2"> 선택 사항입니다. 보낸 사람의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP 서버 </td> 
   <td colname="col2"> SMTP 서버 컴퓨터의 주소와 인증에 필요한 암호 및 사용자 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 제목 </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 보낼 이메일을 설명하는 제목 줄입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 알림 전용 </td> 
   <td colname="col2"> 배경 보고서가 생성될 때 이메일을 보내도록 데이터 워크벤치를 구성할 수 있습니다. 이 값을 True로 설정하면 보고서가 전송되지 않고 구독된 사용자를 보고서 위치로 연결하는 이메일을 보냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 루트 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 생성된 보고서 세트의 출력 위치입니다. 기본값은 보고서 서버 설치 디렉토리 <i>&lt;프로필 이름&gt;</i>\Reports 폴더입니다. </p> <p>보고서를 <span class="keyword"> 포털에 </span> 출력하도록 보고서 서버를 구성하려면 출력 루트를 <span class="wintitle"> 포털에 사용되는 웹 서버의 문서 </span> 루트로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 쿼리 필터 미리 로드 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수는 최상위 차원 요소 <span class="wintitle"> 보고서 </span> 유형에만 적용됩니다. </p> <p>보고서를 생성하기 전에 최상위 N 차원 요소를 결정하기 위해 실행해야 하는 쿼리에 적용할 필터의 이름입니다. 기본값은 <span class="wintitle"> Broken_Session_Filter </span>입니다. 끊어진 세션 <span class="wintitle"> 필터에 대한 자세한 </span>내용은 데이터 워크벤치 <i>사용자 안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 보고서 유형 </span> </td> 
   <td colname="col2"> <p>출력을 생성할 형식 다음 옵션 중 하나 또는 모두를 사용하여 한 번에 여러 형식으로 보고서 세트를 출력할 수 있습니다. 
     <ul id="ul_FAF024F73F6B4F2C9D6760441E8F0CF9"> 
      <li id="li_04A3E0C7812B43E7BBFCDA8C3EA21CFC">Excel은 워크시트당 하나의 시각화로 Excel 통합 문서를 만듭니다. 일반적인 규칙으로, 이메일 배포에는 Excel 파일을 사용합니다. Microsoft <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#concept-0b0fdb938805422d95c5f6fe706f09ee"> Excel 파일로 보고서 생성을 </a>참조하십시오. 템플릿 파일 사용에 대한 자세한 내용은 템플릿 <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> 파일 사용을 참조하십시오 </a>. </li> 
      <li id="li_CD1BDDEDE85349CE8C736887BB5E4726">png를 사용하면 휴대용 네트워크 그래픽 파일이 만들어집니다. 일반적인 규칙으로, 웹 브라우저(포털)에 표시할 <span class="filepath"> .png </span> 파일을 사용합니다. </li> 
      <li id="li_869DA266E6A041A5BD343537743FAC79">축소판에서 작업 영역의 축소판( <span class="filepath"> .jpg </span> 파일)을 만듭니다. 기본 크기는 240x180입니다. 기본 크기를 변경하려면 Thumbnail X 및 Thumbnail Y 매개 변수를 편집합니다. </li> 
     </ul> </p> <p>데이터 워크벤치에서 Report. <span class="filepath"> cfg </span> 를 편집할 때 새 보고서 유형을 추가하려면 보고서 유형을 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 새 </span>자식 추가를 클릭한 <span class="uicontrol"> </span>다음 원하는 보고서 유형을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시작 날짜 </td> 
   <td colname="col2"> <p>보고서 세트를 실행할 첫 번째 날짜 및 시간입니다. 이 시간은 데이터 세트의 기준 시간을 기반으로 합니다. </p> <p>형식:MM/DD/YYY hh:mm 표준 시간대(24시간 구문 사용) </p> <p>시간대 설정에 대한 자세한 내용은 데이터 집합 <i>구성 안내서를 참조하십시오</i>. </p> <p> <p>참고: 프로필의 데이터 타임스탬프가 지정된 날짜 및 시간과 일치하면 보고서가 실행되기 시작합니다. </p> </p> <p>예: </p> <p>시작 날짜가 2006/08/08 12:00 EST이면 타임스탬프가 08/08/2006 12:00 EST 이상인 데이터에 대해 보고서가 실행됩니다. 
     <ul id="ul_EEF6F61B55E440DFB3348A9B10DFA5F1"> 
      <li id="li_133374F1287D4631BCAE7691E3FC93B6">일별 보고서는 2006/08/08에 대해 실행되며 그 이후에는 hh:mm = 12:00 EST의 데이터에 대해 매일 실행됩니다. </li> 
      <li id="li_89514719C5F94D789E4A1049D2CD5F93">주별 보고서는 2006년 8월 8일에, 그 후 7일마다 hh:mm = 12:00 EST의 데이터에 대해 실행됩니다. </li> 
      <li id="li_EB986D04FA664DB89C66B0FC1CE4D36B">월별 보고서는 2006년 8월 8일과 그 이후 매월 8일에 대해 hh:mm = 12:00 EST의 데이터에 대해 실행됩니다. </li> 
     </ul> </p> <p>보고서 <span class="wintitle"> 시간 </span> 지표는 "지난 7일", "어제" 및 "3주 전"과 같은 "마지막 N" 보고 차원에 영향을 줍니다. 보고서 서버의 쿼리에 대해 보고서 <span class="wintitle"> 시간 </span> 지표( <span class="filepath"> 보고서 시간.지표 </span>)는 보고서를 실행하는 날짜와 시간을 식별합니다. 이것은 처음에 시작 날짜 매개 변수에 지정된 날짜 및 시간으로, 이후 Every 매개 변수에 의해 지정된 기간별로 증가합니다. 데이터 워크벤치의 쿼리의 경우 보고서 <span class="wintitle"> 시간 </span> 지표는 기준 지표( 기준.지표 <span class="filepath"> </span>)의 자정을 기반으로 합니다. 보고서 시간 지표의 정의 차이로 인해 마지막 N 차원을 사용하는 작업 영역을 쿼리하는 경우 동일한 작업 공간에 대한 데이터 워크벤치와 보고서 <span class="keyword"> 서버에서 다른 결과를 받을 </span> 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 축소판 X </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 출력으로 생성된 축소판의 X축의 크기(픽셀 단위)를 제어하는 정수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 축소판 Y </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 출력으로 생성된 축소판의 Y축 크기(픽셀 단위)를 제어하는 정수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 N 지표 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 상위 N 값 매개 변수에 대한 설명을 참조하십시오. </p> <p> <p>참고: 이 매개 변수에 값을 입력할 경우 차원 이름 매개 변수와 최상위 N 값 매개 변수에 값을 입력해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 N 값 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수가 채워지면 <span class="keyword"> 보고서 서버는 동적 모드로 </span> 실행되고 차원 이름 매개 변수에 지정된 차원의 요소에 대한 최상위 숫자(이 매개 변수에 지정됨)에 대한 보고서를 생성하여 최상위 N 지표 매개 변수에 지정된 지표별로 계산합니다. </p> <p>예:차원 이름 매개 변수, 상위 N 지표 매개 변수의 세션 및 이 매개 변수의 5에 페이지를 입력하면 생성된 보고서에 세션 수가 가장 많은 상위 5개의 상위 페이지가 표시됩니다. </p> <p> <p>참고: 이 매개 변수에 값을 입력할 경우 차원 이름 매개 변수와 최상위 N 지표 매개 변수에 값을 입력해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로컬 샘플만 사용 </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. 보고서 서버가 데이터 <span class="keyword"> 집합의 로컬 샘플만 사용하여 보고서를 </span> 생성할지 여부를 나타냅니다. 이 매개 변수를 true로 설정하면 데이터 워크벤치 서버에 로드를 배치하지 않고 보고서 세트 샘플을 보고 데이터를 완전히 처리하는 데 필요한 시간을 모두 소비하지 않고도 출력이 어떻게 표시되는지 확인할 수 있습니다. 테스트 기능으로 작동합니다. 옵션은 true 또는 false입니다. 기본값은 false입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 영역 경로 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 지정된 보고서 세트에 대한 작업 영역 컬렉션의 위치입니다. 이 기능은 여러 보고서 세트에 대해 Report.cfg 파일을 사용하여 여러 방법으로 생성 및 배포해야 하는 작업 영역의 단일 복사본을 유지 관리하는 데 유용합니다 <span class="filepath"> . </span> 이 경로의 루트 디렉토리는 모든 프로필 폴더가 될 수 있습니다. 경로 문자열의 시작 부분에 슬래시(\)를 입력하지 마십시오. </p> <p>예:Reports\Common 폴더에 Set A 및 Set B에 대한 공통 작업 영역을 <span class="filepath"> 저장한 </span> 다음 <span class="filepath"> 각각 다른 생성 및 배포 설정을 갖는 두 개의 다른 보고서 세트에 대해 Report.cfg </span> 파일을 정의할 수 있습니다. 두 <span class="filepath"> Report.cfg </span> 파일에서 작업 영역 경로 매개 변수를 <i>프로필 이름</i>\Reports\Common으로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> XSL 출력 파일 </td> 
   <td colname="col2"> <i>선택 사항입니다</i>. XSL 템플릿이 보고서 <span class="wintitle"> 인덱스에 </span> 적용될 때 생성되는 출력 파일의 경로입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> XSL 템플릿 </td> 
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 인덱스에 적용할 XSL 템플릿 파일의 경로입니다. 생성된 변환된 <span class="filepath"> .xml </span> 은 지정된 XSL <span class="wintitle"> 출력 파일에 기록됩니다 </span>. 샘플 <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> 파일은 보고서 샘플 </a> 파일을 참조하십시오. </p> <p> <p>참고: 보고서를 생성할 때 <span class="filepath"> .xsl </span> 템플릿을 사용하지 않으면 모든 보고서가 이메일로 첨부 파일로 배포됩니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>
