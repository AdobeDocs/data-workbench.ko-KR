---
description: Report.cfg 매개 변수에 대한 정보입니다.
title: Report.cfg 매개 변수
uuid: 7a20f4f6-99e6-401a-ba3c-c508881c0f0d
exl-id: 31e4de5f-f7e8-4a35-b5c6-6ad8ef79a259
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 2%

---

# Report.cfg 매개 변수{#report-cfg-parameters}

Report.cfg 매개 변수에 대한 정보입니다.

[보고서 세트 구성](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0)에 표시된 샘플 [!DNL Report.cfg]에는 기본적으로 [!DNL Report.cfg] 파일에 포함된 매개 변수만 포함되어 있습니다. 다음 표에서는 사용 가능한 모든 [!DNL Report.cfg] 파일 매개 변수에 대한 설명을 제공합니다.

[!DNL Report.cfg] 파일에 매개 변수를 더 추가해야 하는 경우 텍스트 편집기를 사용하여 추가해야 합니다. 각 매개 변수 항목을 정의하는 방법의 예를 포함하여 이러한 단계를 보려면 [기존 Report.cfg 파일 편집](../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887)을 참조하십시오.

>[!NOTE]
>
>이 테이블의 매개 변수는 알파벳 순서로 나열됩니다. Data Workbench에서 [!DNL Report.cfg] 파일을 열면 벡터는 알파벳 순서로 나열되고 그 뒤에는 개별 매개 변수가 알파벳순으로 나열됩니다.

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
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수는 지표 표시기가 있는 보고서에만 적용됩니다. 경고 보고서를 보내기 전에 워크시트에 표시해야 하는 지표 표시기 수입니다. </p> <p>지표 지표 지표 워크시트에서 하나의 지표만 모니터되는 경우 임계값을 1로 설정합니다. 시트의 지표가 위쪽/아래쪽 화살표 또는 X로 평가될 때 보고서가 생성됩니다. 보고서에서 두 개 이상의 지표가 모니터되고 있는 경우 보고서가 생성되기 전에 위쪽/아래쪽 화살표 또는 X로 평가되어야 하는 지표 지표의 수를 선택할 수 있습니다. 예를 들어 두 개의 지표가 모니터링되는 경우:
     <ul id="ul_A64E8A2306B14371A233D372B956F64D">
      <li id="li_2A3020ED350644A3954C36D3EB0B86D4">임계값이 1로 설정되면 시트의 지표 중 하나가 위쪽/아래쪽 화살표 또는 X로 평가될 경우 보고서가 생성됩니다. </li>
      <li id="li_DA4EF4984880483DA48322D9D57B9240">임계값이 2로 설정된 경우 보고서를 생성하기 전에 두 지표 모두 위쪽/아래쪽 화살표 또는 X로 평가해야 합니다. </li>
     </ul> </p> <p>지표 지표에 대한 자세한 내용은 <i>Data Workbench 사용 안내서</i>를 참조하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 보고서 재생성 허용 </td>
   <td colname="col2"> <p>이러한 보고서를 만들거나 수정할 때 <span class="keyword"> 보고서 서버 </span>가 자동으로 특정 보고서를 생성하거나 재생성하는지 여부를 나타냅니다. 옵션은 true 또는 false입니다. true로 설정하면 보고서 작업 공간을 만들거나 수정하여 <span class="keyword"> 보고서 서버 </span>가 최근 실행을 위해 해당 보고서를 다시 생성합니다. </p> <p> <p>참고:  <span class="filepath"> Report.cfg </span> 파일을 변경하면 <span class="keyword"> 보고서 서버 </span>가 해당 <span class="filepath"> Report.cfg </span> 파일에서 제어하는 모든 보고서를 다시 생성합니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 첨부 파일 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 첨부 파일 수를 비롯하여 전자 메일을 통해 배포되는 보고서와 함께 실행되는 첨부 파일의 이름 및 콘텐츠 유형에 대한 섹션 식별자입니다. </p> <p>새 첨부 파일을 추가하려면
     <ol id="ol_CBDC1E95D34A4D08A862680127438433">
      <li id="li_784C48C540534F4CBB35BBDA6BC5F48E">Data Workbench에서 <span class="filepath"> Report.cfg </span> 파일을 엽니다. </li>
      <li id="li_0709ADDDDF2E469FAB10761B46173136"><span class="uicontrol"> 첨부 파일 </span>을 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 새 하위 </span> 추가 <span class="uicontrol"> 첨부 파일 </span>을 클릭합니다. </li>
     </ol> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 콘텐츠 유형 </td>
   <td colname="col2"> <p>첨부할 파일의 컨텐츠 유형입니다. </p> <p>예: 이미지/jpeg </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 파일 이름 </td>
   <td colname="col2"> <p>첨부할 파일의 위치 및 이름입니다. </p> <p>예: <span class="filepath"> c:\myimage.jpg </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 색상 세트 </td>
   <td colname="col2"> <span class="filepath"> .png </span> 파일에 사용할 색상 구성표를 식별합니다. 0은 검은색 배경입니다. 1은 흰색 바탕입니다. 및 2는 회색 음영 이미지용입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 실행할 명령 </td>
   <td colname="col2"> <i>선택 사항입니다</i>. 보고서 세트가 생성된 후 실행되는 배치 명령 또는 실행 파일입니다. 명령 셸 인터프리터를 실행해야 하는 경우 명령 앞에 cmd /c를 사용합니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 기본 Excel 템플릿 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서를 Excel 파일로 생성할 때 사용할 일반 Excel 템플릿 파일( <span class="filepath"> .xls </span> 또는 <span class="filepath"> .xlsx </span>)의 파일 이름입니다. 이 매개 변수는 <span class="filepath"> c:\templates\mytemplate.xls </span> 과 같은 전체 파일 경로를 지원합니다. </p> <p>특정 보고서에 대해 특별히 템플릿을 정의하지 않는 한 이 파일은 모든 Excel 보고서에 사용됩니다. <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> 템플릿 파일 사용 </a>을 참조하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 차원 이름 </td>
   <td colname="col2"> <i>선택 사항입니다</i>. 보고서를 동적으로 생성할 차원의 이름입니다. 이 매개 변수에 차원 이름을 입력하는 경우 조회 파일 매개 변수 또는 Top N 지표 및 Top N 값 매개 변수에 값을 입력해야 합니다. 이 매개 변수에서 이름이 지정된 차원은 보고서를 만들 데이터 세트에 있어야 합니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 완벽한 경우에만 이메일 </td>
   <td colname="col2"> <i>선택 사항입니다</i>. 사용자가 실행 중에 오류가 발생하지 않는 경우에만 보고서 세트를 전송하도록 지정할 수 있습니다. 옵션은 true 및 false입니다. 기본값은 false입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 종료 날짜 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 세트를 실행할 마지막 날짜 및 시간입니다. 이 시간은 데이터 집합의 현재 시간을 기반으로 합니다. </p> <p>형식: MM/DD/YYYY hh:mm 시간대, 시간 기준 24시간 구문 사용 </p> <p>예: 08/01/2007 12:01 편집 </p> <p>시간대 설정에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>를 참조하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 각 </td>
   <td colname="col2"> 보고서 세트 생성 빈도: 일, 주 또는 월 </td>
  </tr>
  <tr>
   <td colname="col1"> Excel Watchdog 시간 초과(초) </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. <span class="keyword"> 보고서 서버 </span>에서 Excel이 응답하지 않고 프로세스를 종료하기 전에 보고서를 Excel 파일로 생성할 때 <span class="keyword"> 보고서 서버 </span>에서 Microsoft Excel이 응답할 때까지 대기할 시간(초)입니다. 이 매개 변수를 사용하면 응답이 없을 때 <span class="keyword"> 보고서 서버 </span>에서 Excel을 종료하고 Excel이 아닌 보고서를 계속 처리할 수 있습니다. 기본값은 300.0입니다. 이 기능을 사용하지 않도록 설정하려면 이 매개 변수를 0.0으로 설정하십시오. </p> <p>정의하는 값이 보고서를 Excel로 내보낼 수 있도록 충분히 길었는지 확인합니다. 그렇지 않으면 <span class="keyword"> 보고서 서버 </span>가 Excel을 조기에 종료할 수 있으며 보고서가 생성되지 않습니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 필터 공식 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 세트의 모든 작업 공간에 적용되는 필터입니다. </p> <p>자세한 내용은 </a> 필터를 만드는 <a href="https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html#Syntax_for_Filter_Expressions" format="http" scope="external"> 구문을 참조하십시오. </a></p> </td>
  </tr>
  <tr>
   <td colname="col1"> 감마 보정 </td>
   <td colname="col2"> <p><span class="filepath"> .png </span> 파일 출력에 대한 감마 설정입니다. 기본값은 1.6입니다. </p> <p> <p>참고:  Adobe은 이 값을 변경하지 않는 것을 권장합니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 로고 숨기기 </td>
   <td colname="col2"> 보고서를 생성할 때 보고서 서버가 로고를 숨기는지 여부를 나타냅니다. 옵션은 <span class="filepath"> true </span> 또는 <span class="filepath"> false </span>입니다. <span class="filepath"> false </span>로 설정하면 보고서가 보고서 로고와 함께 생성됩니다. 기본값은 <span class="filepath"> false </span>입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 조회 파일 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수를 채우면 보고서 서버는 동적 모드로 실행되고 Dimension 이름 매개 변수에 지정된 차원의 각 요소에 대한 보고서를 생성합니다. 이 파일에는 머리글 행 없이 탭으로 구분된 두 개의 열이 포함되어야 합니다. </p> <p>
     <ul id="ul_378D4104BB5141C4A013EFE881BFFC6A">
      <li id="li_6F2C89A286B24FFE8EE8C82D278D0633">열 1에는 차원 요소 목록이 포함되어 있습니다. </li>
      <li id="li_4BD1CAA77FEC43268B40489BC5E5E6F7">열 2에는 보고서 수신자의 전자 메일 주소가 포함되어 있습니다. 열 1의 지정된 요소에 대한 보고서가 열 2의 동일한 행에 있는 이메일 주소로 전송됩니다. 여러 개의 이메일 주소를 쉼표로(공백 없음) 구분하여 입력할 수 있습니다. 보고서를 이메일로 보내지 않는 경우 이 열은 비어 있을 수 있지만 반드시 있어야 합니다. </li>
     </ul> </p> <p> <p>참고:  이 매개 변수에 값을 입력하는 경우 Dimension 이름 매개 변수에 값을 입력해야 합니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 알림만 </td>
   <td colname="col2"> 이 <span class="wintitle"> 보고서 서버 </span> 설정을 사용하면 보고서가 생성될 때 이메일을 보내도록 Data Workbench를 구성할 수 있습니다. 이 값을 <span class="filepath"> true </span>로 설정하면 보고서가 전송되지 않고, 대신 구독한 사용자에게 보고서가 생성되었음을 알리는 이메일을 보냅니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 메일 보고서 </td>
   <td colname="col2"> <p>이메일을 통해 보고서를 배포하기 위한 섹션 식별자입니다. 이메일을 통해 보고서를 배포하려면 <span class="wintitle"> 메일 보고서 </span> 항목에 대해 다음 매개 변수를 완료하십시오. 보고서 세트의 모든 보고서는 한 개의 메시지로 수신자 매개 변수에 지정된 이메일 주소로 발송됩니다. </p> <p> <p>참고:  보고서 서버가 하나 이상의 보고서를 생성한 경우에만 이메일을 전송합니다. </p> </p> <p>보고서 이메일을 보낼 수 있도록 하려면 이 항목에 대해 다음 매개 변수 이상을 완료해야 합니다.
     <ul id="ul_539D64D61A8B4F1E95D889C6610EE3B8">
      <li id="li_D2EDBEE57BFE4FD4BB66F63AE561F1E2">SMTP 서버 </li>
      <li id="li_4EEFE6CDA3384FE38149CE8DCBEFF847">수신자 </li>
      <li id="li_CF9F0CF7ECFC4D88A7F4F11BAC4938D6">보낸 사람 주소 </li>
      <li id="li_40BFDCDC9640488EBB450CF8579DA250">알림만 </li>
     </ul> </p> <p> <p>참고:  보고서 세트를 다시 생성한 후 이메일로 보고서를 보내려면 <a href="../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887"> 기존 Report.cfg 파일 편집 </a>을 참조하십시오. </p> </p> <p>알림 전용 값은 5.4x 및 5.5x 릴리스에서 사용할 수 있습니다. </p> <p>알림을 받을 대규모 수신자 세트(20명 이상)의 경우 이메일 배포 목록을 사용하는 것이 좋습니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 본문 XSL 템플릿 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. <span class="filepath"> reports.xml </span> 파일에 적용할 XSL 템플릿 파일의 경로입니다. 이 매개 변수를 사용하면 보고서 서버가 첨부 파일이 아닌 배포된 전자 메일 내에 보고서를 보낼 수 있습니다. 결과 텍스트는 이메일 메시지 본문으로 사용됩니다. </p> <p>샘플 파일에 대해서는 <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> 보고서 샘플 파일 </a> 을 참조하십시오. </p> <p>XSLT(Extensible Stylesheet Language)에 대한 자세한 내용은 <a href="https://www.w3.org/Style/XSL/" format="http" scope="external"> The Extensible Stylesheet Language Family </a>를 참조하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 수신자 </td>
   <td colname="col2"> 보고서를 전송할 사람의 이메일 주소입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 보낸 사람 주소 </td>
   <td colname="col2"> 보낸 사람의 이메일 주소입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 발신자 이름 </td>
   <td colname="col2"> 선택 사항입니다. 보낸 사람의 이름입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> SMTP 서버 </td>
   <td colname="col2"> SMTP 서버 컴퓨터의 주소와 인증에 필요한 암호와 사용자 이름입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 제목 </td>
   <td colname="col2"> <i>선택 사항입니다</i>. 보낼 이메일을 설명하는 제목 줄입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 알림만 </td>
   <td colname="col2"> 배경 보고서가 생성될 때 이메일을 보내도록 Data Workbench를 구성할 수 있습니다. 이 값을 True로 설정하면 보고서가 전송되지 않고, 대신 구독한 사용자를 보고서 위치에 연결하는 이메일을 보냅니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 출력 루트 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 생성된 보고서 세트의 출력 위치입니다. 기본값은 보고서 서버 설치 디렉터리 내의 <i>&lt;프로필 이름&gt;</i>\Reports 폴더입니다. </p> <p>보고서를 포털에 출력하도록 <span class="keyword"> 보고서 서버 </span>를 구성하려면 <span class="wintitle"> 출력 루트 </span>를 포털에 사용되는 웹 서버의 문서 루트로 설정하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 쿼리 필터 사전 로드 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수는 <span class="wintitle"> 최상위 Dimension 요소 </span> 보고서 유형에만 적용됩니다. </p> <p>보고서를 생성하기 전에 상위 N 차원 요소를 결정하기 위해 실행해야 하는 쿼리에 적용할 필터의 이름입니다. 기본값은 <span class="wintitle"> Broken_Session_Filter </span>입니다. <span class="wintitle"> 중단된 세션 필터 </span>에 대한 자세한 내용은 <i>Data Workbench 사용 안내서</i>를 참조하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <span class="wintitle"> 보고서 유형 </span> </td>
   <td colname="col2"> <p>출력을 생성할 형식입니다. 다음 옵션 중 하나 또는 모두를 사용하여 보고서 세트를 한 번에 여러 형식으로 출력할 수 있습니다.
     <ul id="ul_FAF024F73F6B4F2C9D6760441E8F0CF9">
      <li id="li_04A3E0C7812B43E7BBFCDA8C3EA21CFC">Excel에서는 워크시트당 하나의 시각화가 있는 Excel 통합 문서를 만듭니다. 일반적인 규칙으로 전자 메일 배포에 Excel 파일을 사용하십시오. <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#concept-0b0fdb938805422d95c5f6fe706f09ee"> 보고서를 Microsoft Excel 파일로 생성 </a>을 참조하십시오. 템플릿 파일 사용에 대한 자세한 내용은 <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> 템플릿 파일 사용 </a>을 참조하십시오. </li>
      <li id="li_CD1BDDEDE85349CE8C736887BB5E4726">png는 휴대용 네트워크 그래픽 파일을 만듭니다. 일반적인 규칙으로, 웹 브라우저(포털)에 표시하려면 <span class="filepath"> .png </span> 파일을 사용하십시오. </li>
      <li id="li_869DA266E6A041A5BD343537743FAC79">축소판 그림에서 작업 공간의 축소판( <span class="filepath"> .jpg </span> 파일)을 만듭니다. 기본 크기는 240x180입니다. 기본 크기를 변경하려면 Thumbnail X 및 Thumbnail Y 매개 변수를 편집합니다. </li>
     </ul> </p> <p>Data Workbench에서 <span class="filepath"> Report.cfg </span>를 편집할 때 새 보고서 유형을 추가하려면 <span class="uicontrol"> 보고서 유형 </span>을 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 새 하위 추가 </span>를 클릭한 다음 원하는 보고서 유형을 선택합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 시작 날짜 </td>
   <td colname="col2"> <p>보고서 세트를 실행할 첫 번째 날짜 및 시간입니다. 이 시간은 데이터 집합의 현재 시간을 기반으로 합니다. </p> <p>형식: MM/DD/YYY hh:mm 표준 시간대(24시간 구문 사용) </p> <p>시간대 설정에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>를 참조하십시오. </p> <p> <p>참고:  프로필의 데이터 타임스탬프가 지정된 날짜 및 시간과 일치하면 보고서가 실행되기 시작합니다. </p> </p> <p>예: </p> <p>시작 날짜가 08/08/2006 12:00 EST이면 보고서는 08/08/2006 12:00 이상의 타임스탬프가 있는 데이터에 대해 실행됩니다.
     <ul id="ul_EEF6F61B55E440DFB3348A9B10DFA5F1">
      <li id="li_133374F1287D4631BCAE7691E3FC93B6">일별 보고서는 hh:mm = 12:00 EST인 데이터에 대해 08/08/2006 및 그 다음 날에 대해 실행됩니다. </li>
      <li id="li_89514719C5F94D789E4A1049D2CD5F93">주별 보고서는 hh:mm = 12:00 EST를 사용하는 데이터에 대해 08/08/2006 및 그 후 7일마다 실행됩니다. </li>
      <li id="li_EB986D04FA664DB89C66B0FC1CE4D36B">월별 보고서는 hh:mm = 12:00 EST를 사용하는 데이터에 대해 08/08/2006 및 그 후 8일 동안 실행됩니다. </li>
     </ul> </p> <p><span class="wintitle"> 보고서 시간 </span> 지표는 "최근 7일", "어제" 및 "3주 전"과 같은 "마지막 N" 보고 차원에 영향을 줍니다. 보고서 서버의 쿼리에 대해 <span class="wintitle"> 보고서 시간 </span> 지표( <span class="filepath"> 보고서 시간.지표 </span>)는 보고서가 실행되는 날짜와 시간을 식별합니다. 처음에는 시작 날짜 매개 변수에 지정된 날짜 및 시간으로, Every 매개 변수에서 지정된 기간별로 증가합니다. Data Workbench의 쿼리에 대해 <span class="wintitle"> 보고서 시간 </span> 지표는 기준 지표( <span class="filepath"> 기준 지표 </span>)의 자정을 기반으로 합니다. 보고서 시간 지표의 정의 차이로 인해, 마지막 N 차원을 사용하는 작업 공간을 쿼리하는 경우, 동일한 작업 공간에 대해 Data Workbench 및 <span class="keyword"> 보고서 서버 </span>에서 다른 결과를 받을 수 있습니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 축소판 X </td>
   <td colname="col2"> <i>선택 사항입니다</i>. 출력으로 생성된 축소판의 X축의 크기(픽셀 단위)를 제어하는 정수입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 축소판 Y </td>
   <td colname="col2"> <i>선택 사항입니다</i>. 출력으로 생성된 축소판의 Y축의 크기(픽셀 단위)를 제어하는 정수입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 상위 N 지표 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. Top N 값 매개 변수에 대한 설명을 참조하십시오. </p> <p> <p>참고:  이 매개 변수에 값을 입력하는 경우 Dimension 이름 매개 변수와 Top N 값 매개 변수에 값을 입력해야 합니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 상위 N 값 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 이 매개 변수가 채워지면 <span class="keyword"> 보고서 서버 </span>는 동적 모드로 실행되고 Dimension 이름 매개 변수에 지정된 차원에 대한 요소의 최상위 번호(이 매개 변수에 지정된)에 대한 보고서를 생성하여 Top N 지표 매개 변수에 지정된 지표로 계산합니다. </p> <p>예: Dimension 이름 매개 변수, 최상위 N 지표 매개 변수의 세션 및 이 매개 변수에 5를 입력하면 생성된 보고서에 세션 수가 가장 많은 5개의 상위 페이지가 표시됩니다. </p> <p> <p>참고:  이 매개 변수에 값을 입력하는 경우 Dimension 이름 매개 변수와 상위 N 지표 매개 변수에 값을 입력해야 합니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 로컬 샘플만 사용 </td>
   <td colname="col2"> <i>선택 사항입니다</i>. <span class="keyword"> 보고서 서버 </span>에서 데이터 집합의 로컬 샘플만 사용하여 보고서를 생성할지 여부를 나타냅니다. 이 매개 변수를 true로 설정하면 Data Workbench 서버에 로드를 배치하지 않고 보고서 세트의 샘플을 보고 데이터를 완전히 처리하는 데 필요한 모든 시간을 들이지 않고 출력이 어떻게 표시되는지 볼 수 있습니다. 테스트 함수로 작동합니다. 옵션은 true 또는 false입니다. 기본값은 false입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 작업 공간 경로 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 주어진 보고서 세트에 대한 작업 공간 모음의 위치입니다. 이 기능은 여러 보고서 세트에 대해 <span class="filepath"> Report.cfg </span> 파일을 사용하여 여러 방법으로 생성 및 배포해야 하는 작업 공간의 단일 복사본을 유지 관리하는 데 유용합니다. 이 경로의 루트 디렉터리는 모든 프로필 폴더일 수 있습니다. 경로 문자열의 시작 부분에 슬래시(\)를 입력하지 마십시오. </p> <p>예: <span class="filepath"> Reports\Common </span> 폴더에 A 및 Set B에 대한 공통 작업 공간을 저장한 다음, 각각 다른 생성 및 배포 설정을 갖는 두 개의 서로 다른 보고서 세트에 대해 <span class="filepath"> Report.cfg </span> 파일을 정의할 수 있습니다. <span class="filepath"> Report.cfg </span> 파일 모두에서 작업 공간 경로 매개 변수를 <i>프로필 이름</i>\Reports\Common으로 설정합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> XSL 출력 파일 </td>
   <td colname="col2"> <i>선택 사항입니다</i>. <span class="wintitle"> XSL 템플릿 </span>이 보고서 인덱스에 적용될 때 생성되는 출력 파일의 경로입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> XSL 템플릿 </td>
   <td colname="col2"> <p><i>선택 사항입니다</i>. 보고서 인덱스에 적용할 XSL 템플릿 파일의 경로입니다. 변환된 <span class="filepath">.xml </span>은 지정된 <span class="wintitle"> XSL 출력 파일 </span>에 기록됩니다. 샘플 파일에 대해서는 <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> 보고서 샘플 파일 </a> 을 참조하십시오. </p> <p> <p>참고:  보고서를 생성할 때 <span class="filepath"> .xsl </span> 템플릿을 사용하지 않으면 모든 보고서가 전자 메일로 첨부 파일로 배포됩니다. </p> </p> </td>
  </tr>
 </tbody>
</table>
