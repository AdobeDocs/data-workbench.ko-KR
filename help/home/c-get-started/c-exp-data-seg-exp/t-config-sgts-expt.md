---
description: 모든 계산 가능한 차원의 요소 세그먼트를 만든 다음 해당 세그먼트에 대한 데이터를 일괄 또는 지속적으로 실시간으로 탭 구분 파일로 출력할 수 있습니다.
title: 내보낼 세그먼트 구성
uuid: 651be834-ee41-4487-8c5a-30d94580f6a0
exl-id: 4f53e02c-3f00-44b3-9f6d-a2f23903b3fa
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 6%

---

# 내보낼 세그먼트 구성{#configure-segments-for-export}

모든 계산 가능한 차원의 요소 세그먼트를 만든 다음 해당 세그먼트에 대한 데이터를 일괄 또는 지속적으로 실시간으로 탭 구분 파일로 출력할 수 있습니다.

세그먼트를 내보낼 때마다 해당 세그먼트에 포함된 모든 측정기준 요소의 출력 지표 또는 측정기준 데이터가 출력됩니다. 다른 시스템에서 데이터를 쉽게 로드할 수 있도록 출력 데이터의 형식을 제어할 수도 있습니다.

>[!NOTE]
>
>참조용으로 [!DNL report time.metric] 파일을 사용하므로 보고 차원을 내보낼 수 없습니다. 해결 방법으로, 프로필에 하드 코딩된 [!DNL report time.metric]을 배치하는 경우 세그먼트 내보내기에서 이것을 보고 차원에 대한 참조 지점으로 사용할 수 있습니다. 그러나 [!DNL report time.metric]은(는) 프로필의 [기준 시간]을 기반으로 자동으로 업데이트되지 않으므로 보고 차원 참조를 변경하려면 하드 코딩된 [!DNL report time.metric] 파일을 변경해야 합니다.

내보낼 세그먼트를 구성하려면 [!DNL .export] 파일을 열고 편집해야 합니다.

1. [!DNL Profile Manager]에서 [!DNL File] 열의 **[!UICONTROL Export]** 디렉토리를 클릭하여 해당 컨텐츠를 표시합니다.

       내보내기 디렉토리가 없는 경우 다음과 같이 만듭니다.
   
   1. Data Workbench 설치 디렉터리로 이동합니다.
   1. 작업 중인 프로필의 디렉토리를 엽니다.
   1. 프로필 디렉터리 내에 &quot;Export&quot;라는 새 디렉터리를 만듭니다.

1. [!DNL Profile Manager]에서 내보내기 디렉토리의 [!DNL User] 열에 있는 빈 셀을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Create]** > **[!UICONTROL New Segment Export]**&#x200B;을 클릭합니다.

   [!DNL New Segment Export.export] 파일이 내보내기의 [!DNL File] 열에 나타납니다.

1. 파일의 [!DNL User] 열을 마우스 오른쪽 단추로 클릭하고 File 매개 변수에 새 이름을 입력하여 새 파일의 이름을 변경합니다.
1. 파일의 [!DNL User] 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭하여 새 파일을 엽니다.

   [!DNL .export] 파일의 구성 창이 나타납니다.

1. **[!UICONTROL Query]**&#x200B;을 클릭한 다음 다음 다음 표에 설명된 대로 [!DNL .export] 파일의 필드를 수정합니다.

<table id="table_C2EC8FCD3FA04DE78D2CADFA3F7FD8E3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수의 경우.. </th> 
   <th colname="col2" class="entry"> 이 정보 제공... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 명령 </td> 
   <td colname="col2"> <p>선택 사항입니다. 출력 파일을 만든 후 실행할 프로그램입니다. 이 필드는 셸 명령이 아닌 실행 파일(<span class="filepath"> .exe </span> 파일)을 참조해야 합니다. </p> <p>참고: 명령 매개 변수에 공백이 있으면 세그먼트 내보내기가 실패합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필터 </td> 
   <td colname="col2"> <p>선택 사항입니다. 이름이 지정된 필터 또는 필터 식입니다. 필터 편집기를 사용하여 명명된 필터를 만든 다음 여기에 해당 필터의 이름을 입력하거나 필터 표현식 자체를 입력할 수 있습니다. </p> <p>필터 편집기에 대한 자세한 내용은 <a href="../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3"> 필터 편집기 </a>를 참조하십시오. 필터 표현식 구문에 대한 자세한 내용은 <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-fltr-exp.md#concept-72f2563f809747a2a3cff7ec72462a15"> 필터 표현식 </a>의 구문을 참조하십시오. </p> <p>필터와 일치하는 레벨 요소를 내보낼 수 있지만 다른 모든 요소는 내보낼 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 레벨 </td> 
   <td colname="col2"> <p>요소를 내보낼 수 있는 계산 가능한 차원입니다. </p> <p>예:방문자 수준은 각 방문자에 대해 하나의 데이터 행을 내보냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 파일 </td> 
   <td colname="col2"> <p>내보낸 데이터의 경로 및 파일 이름입니다. 프로파일이 Data Workbench 서버 클러스터에서 실행 중인 경우 각 Data Workbench 서버는 데이터의 일부를 포함하는 출력 파일을 기록합니다. </p> <p>Data Workbench 서버 설치 디렉토리에는 출력 파일을 저장할 수 있는 내보내기 디렉토리가 포함되어 있습니다. 예를 들어 <span class="filepath"> Exports\Visitor Segment.txt </span>를 입력할 수 있습니다. 여기서 <span class="filepath"> Visitor Segment.txt </span>는 내보낸 데이터를 포함하는 파일의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 형식 </td> 
   <td colname="col2"> 각 레벨 요소에 대해 내보낼 지표 또는 차원 데이터입니다. 출력은 탭으로 구분된 파일인 경우 필드를 탭 문자로 구분해야 하며 형식은 적절한 새 줄 문자로 끝나야 합니다. 자세한 내용은 <a href="../../../home/c-get-started/c-exp-data-seg-exp/c-abt-otpt-frmt.md#concept-ac7e24d1374a4b418365db7cc98c361e"> 출력 형식 </a> 정보를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 예약 종료 시간 </td> 
   <td colname="col2"> <p>선택 사항입니다. 시간대를 포함하여 일정의 종료 날짜 및 시간입니다. </p> <p>형식:YYYY-MM-DD hh:mm 표준 시간대 </p> <p>예:2013-08-01 12:01 편집 </p> <p>현재 예약된 수출이 중지됩니다.그러나 출력 파일의 정의가 변경될 때마다 출력 파일이 다시 생성됩니다. 이 필드는 스케줄 간격 정의 없이 의미가 없습니다. 시간대 설정에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다음 간격으로 예약 </td> 
   <td colname="col2"> 선택 사항입니다. 출력 파일을 다시 생성할 빈도. 지원되는 값은 시간, 일, 주 및 월입니다. 출력 파일의 정의가 변경될 때마다 출력 파일이 다시 생성됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 예약 시작 시간 </td> 
   <td colname="col2"> <p>선택 사항입니다. 시간대를 포함하여 일정의 시작 날짜 및 시간입니다. </p> <p>형식:YYYY-MM-DD hh:mm 표준 시간대 </p> <p>예:2013-08-01 12:01 편집 </p> <p>현재 예약된 내보내기는 시작되며 일정은 이 시간에 상대적입니다. 이 필드는 <span class="wintitle"> 모든 </span>을(를) 정의하지 않고 의미가 없습니다. 시간대 설정에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 제한(초) </td> 
   <td colname="col2"> 선택 사항입니다. 세그먼트 내보내기가 생성되는 동안 허용되는 최대 시간. 지정한 간격을 초과하면 내보내기가 다시 시작됩니다. 이 값을 0(영)으로 설정하면 제한이 제거됩니다. 기본값은 600초입니다. </td> 
  </tr> 
 </tbody> 
</table>

1. 창 위쪽에 있는 **[!UICONTROL (New)]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. 이 파일을 작업 프로필의 모든 사용자가 사용할 수 있게 하려면 [!DNL User] 열에서 작성된 [!DNL .export] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL .export] 파일을 Data Workbench 서버에 저장하면 예약 시작 시간이 미래 날짜 및 시간으로 설정되어 있어도 내보내기가 즉시 한 번 실행됩니다.

   다음은 샘플 [!DNL .export] 파일입니다.

   ![](assets/vis_Segment_Export_File.png)

   >[!NOTE]
   >
   >샘플에 표시된 [!DNL Visitor Segment.export] 파일은 방문자 세그먼트 필터를 참조합니다. 이 필터의 정의를 수정하면 내보내기 정의가 변경됩니다.
