---
description: 목표, 가설 및 실험 세부 사항을 정의하고 테스트 컨텐츠를 만든 후에는 센서가 제어된 실험을 배포하도록 구성해야 합니다.
solution: Analytics,Analytics
title: 실험 구성 및 배포
topic: Data workbench
uuid: 460d3ea4-a6c8-4ac4-9a3f-eab71f65b096
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 1%

---


# 실험 구성 및 배포{#configuring-and-deploying-the-experiment}

목표, 가설 및 실험 세부 사항을 정의하고 테스트 컨텐츠를 만든 후에는 센서가 제어된 실험을 배포하도록 구성해야 합니다.

## 실험 구성 파일 구성 {#section-037fe7dea9c94aee9cdc354dafdb7c03}

실험을 구성하려면 Adobe(기본적으로 이름 지정)에서 제공하는 실험 구성 스프레드시트를 완료해야 [!DNL TestExperiment.xls] 합니다. 이 파일 [!DNL Sensor] 은 실험을 수행하도록 구성되며 ExpFile 매개 변수 수정에서 지정한 텍스트 파일 [의 Excel 버전입니다](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

이 파일에는 여러 실험에 대한 정보가 포함될 수 있으며 이 정보는 동일하거나 다른 시간에 실행할 수 있으며 서로 다른 그룹 및 백분율을 사용할 수 있지만 이러한 실험은 어떠한 방법으로든 상관 관계가 없습니다.

사용자는 현재 실행되도록 구성된 파일에 나열된 각 실험에 대해 그룹에 배치됩니다.

>[!NOTE]
>
>각 실험은 다른 모든 실험과는 별개다. 한 실험에 대한 변경 사항은 다른 실험에는 영향을 주지 않으며, 방문자가 여러 실험에 있을 수 있지만 결과는 서로 관련이 없습니다. 여러 실험의 변경 간에 상관 관계가 있다고 생각되는 경우 이러한 변경 사항을 함께 테스트하는 새로운 실험을 만들어야 합니다.

**실험을 구성하려면**

실험 시작 전에 이 파일을 완료해야 하며 실험 실행 중에는 정보를 수정하지 않아야 합니다.

>[!NOTE]
>
>실험이 시작된 후 실험의 정의가 바뀌면 모든 실험은 즉각 무효이다.

1. 웹 또는 응용 프로그램 서버에 대한 관리자 액세스 권한이 있는 경우 웹 클러스터 [!DNL Sensor] 의 모든 [!DNL Sensor] 시스템에서 설치 폴더로 이동하여 [!DNL TestExperiment.xls] 파일에 액세스합니다. 관리자 액세스 권한이 없는 경우 Adobe 계정 관리자에게 문의하여 [!DNL TestExperiment.xls] 파일을 요청하십시오.

1. 파일을 열고(필요한 경우 이 파일의 이름을 변경할 수 있음) 다음 필드를 완료합니다. [!DNL TestExperiment.xls]

<table id="table_FDD6AE631C614F97AD7AE8829E53CCAC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 실험 </td> 
   <td colname="col2"> <p>실험에 사용할 설명형 이름입니다. 각 실험 이름은 고유해야 하며 공백을 포함할 수 없습니다. </p> <p>실험 이름은 Insight에서 실험 결과를 표시할 때 <span class="keyword"> 사용됩니다 </span>. 제어된 실험 차원에 있는 요소 이름의 첫 번째 부분으로 이름이 나타납니다. 요소 이름의 두 번째 절반은 이 파일의 그룹 필드의 그룹 이름입니다. 각 그룹의 이름은 실험 이름 다음에 그룹 이름을 사용하여 다음 형식으로 지정됩니다. </p> <p><i>ExperimentName.Group Name</i> </p> <p>예: <span class="filepath"> New_Homepage.Control </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시작 </td> 
   <td colname="col2"> <p>실험을 시작할 날짜와 시간입니다. 값을 입력하지 않으면 파일이 배포된 직후 실험이 시작됩니다. </p> <p>형식:YYYY/MM/DD H:MM </p> 
    <ul id="ul_FB8B50C688584683AC2226FCBED40AF9"> 
     <li id="li_223EF962CFC64454965444E66284F670">시작 및 중지 시간을 비워 두면 실험이 무기한 실행됩니다. </li> 
     <li id="li_0544C9A98635418CAECD85B67F345772">시작 및 중지 시간을 미리 정의할 수 있습니다.따라서 원하는 경우 다음 해의 모든 실험을 한 번에 구성할 수 있습니다. </li> 
     <li id="li_BDFBB74B1D134E57B37DC5C3457AA1A9">시작 및 중지 시간은 웹 서버의 시스템 시간을 기반으로 합니다. 어떤 이유에서든 그 시계가 바뀌면 여러분의 실험이 예상치 않게 시작하거나 중지될 수 있습니다. </li> 
     <li id="li_3295FE5B2AC64B6CA90CC7F31B808EB9">실험 결과를 구성 파일 항목으로 추가하지만 가까운 시일 내에 실험 결과를 실행하지 않으려면 숫자 기호 "#"을 사용하여 실험 정보에 주석을 달거나 과거에 시작 및 중지 시간을 정의할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 중지 </td> 
   <td colname="col2"> <p>실험을 종료할 날짜와 시간입니다. 정지 날짜 및 시간이 발생하면 <span class="wintitle"> 센서는 테스트 그룹으로 식별된 쿠키 값을 테스트 URI로 보내지 </span> 않고 모든 쿠키를 제어 그룹 URI로 전송합니다. </p> <p>형식:YYYY/MM/DD H:MM </p> <p>시작 필드에 대한 <span class="wintitle"> 메모를 </span> 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 그룹 </td> 
   <td colname="col2"> <p>실험 내의 각 방문자 그룹에 대한 설명형 이름입니다. 그룹 이름에는 공백을 사용할 수 없습니다. </p> <p>그룹 이름은 <span class="keyword"> 인사이트에서 실험 결과를 표시할 때 사용됩니다 </span>. 자세한 내용은 실험 필드 설명을 참조하십시오. </p> <p>비율 필드에 입력한 값을 기반으로 하여 제어 그룹을 암시적 또는 명시적으로 정의할 수 있습니다. </p> <p> <p>참고: 정의된 기간 동안 필요한 방문자 수를 통계적으로 유효화하려면 신뢰 수준을 줄이거나 기간을 늘려야 할 수 있습니다. 예를 들어 시간대가 5일이면 신뢰 수준이 98%이고 필요한 방문자 수가 해당 기간 동안 예상 수를 초과하는 경우 예상 방문자 수가 통계적으로 유효한 실험을 실행하는 데 필요한 수를 초과할 때까지 기간을 늘리거나 신뢰 수준을 줄여야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비율 </td> 
   <td colname="col2"> <p>정의된 각 그룹에 포함할 웹 사이트 방문자의 백분율입니다. 이러한 값은 백분율 또는 십진수 값으로 표현될 수 있습니다. 또한 두 값 모두 1보다 크거나 작아야 합니다. </p> <p>예: </p> <p>33.3% 및 66.7% </p> <p>.99 및 .01 </p> <p>모든 그룹에 대한 합계가 100보다 작으면 정의되지 않은 초과는 제어 그룹으로 기본 설정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 원래 URL </td> 
   <td colname="col2"> <p>제거할 컨텐츠의 URI에 $가 추가됩니다. 이 값은 대/소문자를 구분합니다. </p> <p>형식:index.asp$ </p> <p>원본 URI는 URI 끝에 달러 기호($)를 사용하여 지정할 수 있으므로 파일 이름의 정확한 일치를 필요로 합니다. 예를 들어 /product/product_view.asp$ 표현식 <span class="filepath"> 은 해당 페이지에만 </span> 일치하지만 <span class="filepath"> /product </span> 은 <span class="filepath"> /product </span> 디렉토리의 모든 페이지와 일치하며 해당 하위 트리 전체를 다시 매핑하는 데 사용할 수 있습니다. ExpPartialMatch 매개 변수가 "on"으로 설정되어 있지 않으면 파일 이름 끝에 $ 문자를 지정하지 않는 원본 URL 항목은 실험에서 무시됩니다. 이 매개 변수에 대한 자세한 내용은 ExpPartialMatch 매개 변수 <a href="../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expplmth-prm.md#concept-9c817c4c49b74287b0f70d6a1a37655e"> 수정(선택 사항)을 참조하십시오 </a>. </p> <p>제어 실험 기능은 URI 줄기에 추가된 모든 쿼리 문자열을 무시합니다. 예를 들어, </p> <p> <span class="filepath"> /product/product_view.asp?productid=53982 </span> 는 올바른 URI가 아니지만 /product/product_view.asp 페이지 <span class="filepath"> 는 유효한 URI </span> 입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다시 매핑된 URL </td> 
   <td colname="col2"> <p>대체 컨텐츠의 URI입니다. </p> <p>형식:index2.asp </p> <p>원본 URL 필드에 대한 메모를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음은 완료된 [!DNL TextExperiment.xls] 스프레드시트의 예입니다.

![](assets/TestExperimentSpreadsheet.png)

>[!NOTE]
>
>스프레드시트의 열 위치를 수정하지 마십시오.

이 예는 &quot;New_Homepage&quot; 실험이 2006년 6월 1일에 시작되고, 2006년 6월 30일에 종료되며, 방문자의 50%가 포함된 제어 그룹과 방문자의 50%가 포함된 테스트 그룹을 포함하고 있으며, 각 URI에 대해 서로 다른 컨텐츠를 보고 있습니다.

>[!NOTE]
>
>위의 샘플 파일에는 명시적 제어 그룹이 정의되어 있지만 제어 그룹을 명시적으로 정의할 필요는 없습니다. 그러면 자동으로 제어 그룹이 생성됩니다. 실험 내의 모든 그룹에 대한 비율의 합이 100% 미만인 경우 명시적 그룹 중 하나에 해당되지 않는 사용자에게 암시적 제어 그룹이 할당됩니다.

1. 특정 실험에 대한 추가 정보를 제공하는 주석을 삽입하려면 숫자 기호(#)로 셀을 시작하고 설명을 따릅니다. 주석은 파일의 아무 곳에나 삽입할 수 있습니다.
1. 실험 구성 스프레드시트에서 변수를 완료한 후 변경 내용을 저장한 다음 구성 파일의 ExpFile 매개 변수에서 지정한 이름을 사용하여 탭으로 구분된 텍스트 형식( [!DNL *.txt])으로 파일을 [!DNL Sensor] 저장합니다. See [Modifying the ExpFile Parameter](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

   다음은 실험 구성 텍스트 파일의 예입니다.

   ![](assets/testexperiment.png)

   >[!NOTE]
   >
   >이 파일에 필요한 탭이므로 직접 실험 구성 텍스트 파일을 편집하지 마십시오. 파일을 변경해야 하는 경우 실험 구성 Excel 파일을 변경하고 탭으로 구분된 텍스트 파일로 파일을 다시 저장합니다.

시작 및 중지 시간을 정의한 경우 실험 구성 파일에서 실험을 삭제할 이유가 없습니다. 실험 구성 파일에 모든 실험을 나열하는 것은 실제로 각 실험을 정의했다는 기록을 유지하는 좋은 방법입니다.

## 구성 파일 배포 및 컨텐츠 테스트 {#section-34ff29649f584b93bc6129b75084b37c}

실험 구성 파일을 실행하고 실험과 관련된 페이지를 제공하는 웹 클러스터 [!DNL Sensor] 의 각 컴퓨터에 배포해야 합니다. 수동 절차나 기존 컨텐츠 관리 시스템을 사용하여 수행할 수 있습니다.

**테스트 컨텐츠를 배포하려면**

* 실험과 관련된 페이지를 제공하는 웹 서버 [!DNL Sensor] 를 실행하는 각 응용 프로그램 또는 웹 서버에서 기존 게시 프로세스를 사용하여 테스트 컨텐츠를 적절한 위치에 배포합니다.

   예를 들어, 테스트 그룹 페이지를 웹 사이트()의 테스트 폴더 [!DNL index2.asp] 에 게시하려면 해당 파일 [!DNL mysite.com]을 게시합니다 [!DNL www.mysite.com/test].

   >[!NOTE]
   >
   >웹 사이트의 페이지에서 직접 테스트 파일에 연결하지 마십시오. 이렇게 하면 테스트 결과와 인덱스 점수가 무효화됩니다.

**실험 배포**

* 실험과 관련된 페이지를 제공하는 페이지를 실행하는 각 응용 프로그램 또는 웹 서버 [!DNL Sensor] 에서 실험 구성 텍스트 파일을 구성 파일의 ExpFile 매개 변수에 지정한 디렉토리에 [!DNL Sensor] 넣습니다. See [Modifying the ExpFile Parameter](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

[!DNL Sensor] 파일에서 정의한 백분율을 기반으로 각 그룹의 웹 사이트 방문자를 임의로 선택하고 테스트 또는 제어 그룹 컨텐트를 적절히 제공합니다.
