---
description: 데이터 워크벤치의 파인더 패널을 사용하여 지표, 차원 및 필터를 선택합니다. 이러한 패널은 검색 지원, 정렬 옵션 및 드래그 앤 드롭 기능을 제공합니다.
solution: Analytics
title: 파인더
topic: Data workbench
uuid: 7a4144f5-133f-48ed-9613-1e42b1313120
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# 파인더{#finders}

데이터 워크벤치의 파인더 패널을 사용하여 지표, 차원 및 필터를 선택합니다. 이러한 패널은 검색 지원, 정렬 옵션 및 드래그 앤 드롭 기능을 제공합니다.

파인더 패널은 왼쪽 사이드바 또는 작업 영역 내에서 열 수 있습니다.

![](assets/query_entity_panel_main.png)

<table id="table_3E43DBA0646842898F14F31374F9E39C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 차원 파인더 </th> 
   <th colname="col2" class="entry"> 지표 파인더 </th> 
   <th colname="col3" class="entry"> 필터 파인더 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>쿼리 모델의 모든 차원 목록입니다. </p><img placement="break" id="image_D7D317D84C0843BE8D324E5B9F7AF20D" src="assets/query_entity_dim_panel.png" /> </td> 
   <td colname="col2"> <p>쿼리 모델의 모든 지표 목록입니다. </p><img placement="break" id="image_04553B2F2C6A48FE897B4EFF002BED59" src="assets/query_entity_metric_panel.png" /> </td> 
   <td colname="col3"> <p>조직에 대해 만든 모든 필터 목록입니다. </p><img placement="break" id="image_920E72D795644634A82D1955CB64B355" src="assets/query_entity_filters_panel.png" /> </td> 
  </tr> 
 </tbody> 
</table>

**파인더를 열려면**

* 작업 영역을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Tools]** > **[!UICONTROL Finder]**&#x200B;을 선택합니다.

   지표, 차원 및 필터에 대한 탭이 있는 파인더 창이 작업 영역에서 열립니다.

* 왼쪽 세로 막대에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add]** > **[!UICONTROL Finder]**&#x200B;을 선택합니다.

   왼쪽 패널에서 파인더 창이 열립니다.

Finder **에는** 다음 기능이 포함되어 있습니다.

<table id="table_072047E919204577AE85789BAE0F4EE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Finder 기능 </th> 
   <th colname="col2" class="entry"> 세부 사항 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><b>드래그 앤 드롭</b> </td> 
   <td colname="col2"> <p> 패널에서 차원 또는 지표를 작업 영역의 시각화로 드래그하여 놓아 차원을 변경하거나 새 지표를 추가할 수 있습니다. </p> 
    <ol id="ol_612DC76EC04C4FCE938B20B388C43CE8"> 
     <li id="li_7F73B781141E4B8CAE9800F580F62E44">&lt;Ctrl&gt; <span class="uicontrol"></span> 및 <span class="uicontrol"> &lt;Alt&gt;</span> 키를 누른 채 Finder 패널에서 차원이나 지표를 선택합니다. </li> 
     <li id="li_631D57976F71415AA61F33EBBFDD128A">창에서 새 차원을 드래그하여 시각화에 놓아 차원을 변경하거나 추가합니다. </li> 
     <li id="li_5329FB82225F46EBBE3A996A641058DE">지표를 추가하려면 창에서 새 지표를 끌어 선택한 시각화의 지표 헤더에 놓습니다. </li> 
    </ol> <p>이 작업은 테이블, 방문자 클러스터, 상관 관계 매트릭스, 산포도, 2D 막대 그래프(축에 따라 다름)를 비롯한 모든 관련 시각화에 작동합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>검색</b> </td> 
   <td colname="col2">파인더 <span class="uicontrol"> 패널의</span> 검색 상자를 사용하면 차원, 지표 및 필터의 이름을 필터링할 수 있습니다. 
    <ul id="ul_0F6F377E9906472E99008EBE7483F689"> 
     <li id="li_75857895EDB045C8B2960393854B257D"> <p>패턴 일치(단순 전역 검색). 검색 필드에 필요한 차원, 지표 또는 필터 엔티티의 이름을 입력하기 시작하면 이름에 포함된 일치하는 문자열만 필터링되어 파인더 창에 표시됩니다. </p> <p>예를 들어 다음을 입력합니다. </p> <code><b>Search:</b>click</code> <p>차원 파인더에서 다음 결과를 얻을 수 있습니다. </p> <p><img placement="break" id="image_7CBAAABA92BB47658B7F9F5C0263CF20" src="assets/finders_glob_search.png" /> </p> <p>표준 패턴 일치를 사용하면 . 등의 와일드카드 문자를 사용할 수 있습니다. (dot), "?" , and "*" (star). </p> </li> 
     <li id="li_044F9EC1399B44CD81E1852F85137704"> <p>정규 표현식을 참조하십시오. 추가적인 검색 기능에는 더 복잡한 정규 표현식도 지원됩니다. 검색어(공백 없음) 앞에 접두사 "re:"를 추가하여 정규식으로 해석합니다. </p> <p>예를 들어 다음을 입력합니다. </p> <code><b>Search:</b>re.*ip</code> <p>차원 파인더에서 다음 결과를 얻을 수 있습니다. </p> <p><img placement="break" id="image_F47DB90B36504997AA1C509855B89A47" src="assets/finders_regex_search.png" /> </p> </li> 
    </ul> <p>자세한 검색 정보는 <a href="https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-reg-exp.html" format="http" scope="external"> 정규 표현식을</a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>차원 유형</b> </td> 
   <td colname="col2">차원 탭에서 탭 제목을 마우스 오른쪽 단추로 클릭하여 차원 유형별로 정렬할 수 있습니다. <p><img id="image_FB44D0F4D36B4AD7A6165E0432211AB6" placement="break" src="assets/query_entity_search_types.png" /> 
     <ul id="ul_D36B8474730F4859BC7AA015CC1B8EF0"> 
      <li id="li_4AE1D5699D0E45AF880A134F886B8B19">속성 - 방문자, 제품, 지리적 위치, 시간, 비디오 및 기타 속성의 특성을 기반으로 구축된 차원입니다. </li> 
      <li id="li_0B2A08F8CBE94356AC506F95DC268C47">클러스터(Clusters) - 클러스터 빌더 내에서 작성된 차원입니다. </li> 
      <li id="li_4BC3396A680B49A4B6BDAAD066826864">점수 - 성향 점수 내에 작성된 차원입니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>레이블</b> </td> 
   <td colname="col2">각 탭에서 마우스 오른쪽 단추를 클릭하고 레이블을 선택하여 <span class="uicontrol"> 찾기</span> 창의 이름을 변경할 수 있습니다. <p><img placement="break" id="image_F61C57F6548646069242DFB2490C67B9" src="assets/label_change.png" /> </p> <p>기본 차원, 지표 및 필터 레이블은 조직의 규칙을 충족하는 탭 이름으로 변경할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>항목 추가</b> </td> 
   <td colname="col2">각 탭에서 마우스 오른쪽 단추를 클릭하고 항목 추가를 선택하여 <span class="uicontrol"> 테이블을</span> 열고 차원, 지표 및 필터를 수동으로 추가할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>파인더 막대</b> </td> 
   <td colname="col2">왼쪽 세로 막대의 파인더 <span class="uicontrol"> 막대를 마우스</span> 오른쪽 버튼으로 클릭하여 추가 기능을 위한 메뉴를 엽니다. <p><img placement="break" id="image_4DA4930294B84308A1E627C828C35663" src="assets/finders_menu.png" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>닫기</b> </td> 
   <td colname="col2">파인더 막대를 마우스 오른쪽 단추로 <span class="uicontrol"> 클릭하고</span> 닫기를 <span class="uicontrol"> 선택하여</span> 파인더 창을 닫습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>저장</b> </td> 
   <td colname="col2">헤더 막대를 마우스 오른쪽 단추로 클릭하고 저장 옵션을 선택하여 목록을 로컬에 <span class="uicontrol"> 저장합니다</span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>내보내기</b> </td> 
   <td colname="col2">파인더 패널을 마우스 오른쪽 단추로 클릭하고 메뉴에서 내보내기를 선택하여 선택한 차원, 지표 또는 필터 목록을 파인더 패널에서 내보낼 <span class="uicontrol"> 수</span> 있습니다. <p> 이름을 추가하고 Microsoft Excel로 내보냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>복사</b> </td> 
   <td colname="col2"> 차원, 지표 또는 필터 목록을 복사합니다. [어두운 배경], [밝은 배경] 또는 [단색]에서 파일이나 그래픽으로 복사할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>최소화</b> </td> 
   <td colname="col2"> 파인더 창을 최소화합니다. 파인더 막대만 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>테두리 없음</b> </td> 
   <td colname="col2"> 작업 영역에서 파인더 테두리 선이 없는 창을 표시합니다(왼쪽 사이드바는 아님). </td> 
  </tr> 
 </tbody> 
</table>

