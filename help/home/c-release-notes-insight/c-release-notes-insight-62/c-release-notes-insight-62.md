---
description: Data Workbench 6.2 릴리스 노트에는 새로운 기능, 업그레이드 요구 사항, 버그 수정 및 알려진 문제가 포함되어 있습니다.
title: Data Workbench 6.2 릴리스 노트
uuid: 8631c936-d53b-493d-9f58-72f541c3ddce
translation-type: tm+mt
source-git-commit: a276b16565634fea9b693206c8a55b528fada977
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 5%

---


# Data Workbench 6.2 릴리스 노트{#data-workbench-release-notes}

Data Workbench 6.2 릴리스 노트에는 새로운 기능, 업그레이드 요구 사항, 버그 수정 및 알려진 문제가 포함되어 있습니다.

## 새로운 기능 {#section-1225066ea8f44cf68e42e019d0bca816}

Data Workbench 6.2에는 다음과 같은 새로운 기능이 포함되어 있습니다.

| 기능 | 설명 |
|--- |--- |
| 의사 결정 분지도 | 의사 결정 트리는 방문자 특성 및 관계를 평가하는 데 사용되는 예측 분석 시각화입니다. 의사 결정 트리 빌더에서는 지정된 긍정적인 사례와 입력 세트를 기반으로 의사 결정 트리 시각화를 생성합니다. |
| 상관 관계 매트릭스의 이진 필터 업데이트 | 이진 필터가 새로운 기능으로 업데이트되어 이전 버전에 내장된 이진 필터로 모든 상관 관계 매트릭스를 다시 빌드해야 합니다. |
| 밀도 맵 | 밀도 맵은 정사각형 맵 내에서 음영처리된 사각형으로 요소를 표시하는 시각화입니다. |
| 속성 프로필 | 기여도 값(성공적인 전환 또는 판매에 대한 책임을 지는 이벤트)을 신속하게 분석하기 위해 Data Workbench은 아키텍트가 속성 보고서를 설정하고 분석가를 위한 기능을 포함하는 규칙 기반 속성 프로필을 제공합니다. |
| 분석 보고서 | 보고서 템플릿은 Adobe SC 프로필을 사용하는 데이터 워크벤치 사용자를 위해 Adobe Analytics 보고서를 표준화합니다. 이러한 보고서는 마케팅 보고 및 분석(이전 SiteCatalyst)에 사용되는 보고서와 동일합니다. |
| 3D 산포도 | 3D 산포도는 x, y, z 축이 다양한 지표를 나타내는 3차원 격자에 데이터 차원(일 또는 참조 사이트 등)의 요소를 그래프로 표시합니다. |


## Data Workbench 클라이언트 UI 업데이트{#data-workbench-client-ui-updates}

Data Workbench 6.2에는 책갈피 패널에 대한 새로운 사용자 인터페이스 업데이트, 작업 공간 도구 모음의 새로운 아이콘, 화면 내에서 작업 영역을 드래그하는 기능, 새로운 빠른 키 및 파이 차트 시각화에 대한 업데이트 등이 포함되어 있습니다.

## 새로운 책갈피 기능 {#section-e361b605441540ca8213c3fddb5e0718}

이제 중요한 작업 영역을 책갈피로 지정하여 워크플로우에 사용되는 시각화와 보고서 간에 빠르게 이동할 수 있습니다.

**책갈피 작업**

1. 도구 모음의 오른쪽 상단 모서리에 있는 책갈피 아이콘 ![](assets/bookmark_icon.png) 을 클릭하여 작업 영역에 책갈피를 지정합니다.
1. 왼쪽 창 **[!UICONTROL Add]** **[!UICONTROL Bookmarks Panel]** 에서 > 을 클릭하여 책갈피 목록을 엽니다.

   ![](assets/bookmarks_panel.png)

1. 책갈피가 지정된 작업 영역을 열려면 에서 작업 공간 이름을 클릭합니다 **[!UICONTROL Bookmark Panel]**.

   ![](assets/bookmarks_panel_left.png)

   선택한 작업 영역이 열립니다. 다른 책갈피가 지정된 작업 영역을 클릭하면 이전 작업 영역이 닫히고 새로 선택한 작업 영역이 열리면서 작업 흐름을 빠르게 탐색할 수 있습니다.

**책갈피를 삭제하려면**

* 책갈피 패널에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL 제거를 선택합니다<bookmark title>]**선택한 책갈피를 삭제하거나 모든 책갈피&#x200B;**[!UICONTROL Clear All Bookmarks]**를 삭제하도록 선택합니다.

* 또한 작업공간의 축소판 보기에서 작업 영역을 마우스 오른쪽 단추로 클릭하고 선택할 수도 있습니다 **[!UICONTROL Clear Bookmark]**.

>[!IMPORTANT]
>
>* 25개의 책갈피를 저장할 수 있습니다.
>* 책갈피를 추가한 다음 작업 영역의 위치를 이동하는 경우 책갈피는 유효하지 않게 되며 책갈피 패널에서 삭제하고 재설정해야 합니다.

>



## 작업 공간의 새 아이콘 {#section-c108bbd1661249e79c146727ff3d2470}

이제 Data Workbench 6.2가 작업 공간의 텍스트를 아이콘으로 대체합니다. 마우스로 계속 가리키면 아이콘을 식별하는 도구 설명 메시지(예: **[!UICONTROL File]**, **[!UICONTROL Add]**&#x200B;및 **[!UICONTROL Export]**&#x200B;포함)가 표시됩니다.

![](assets/new_icons.png)

다음 링크를 비롯한 설명서 및 기타 기술 자료에 액세스하기 위해 새 **[!UICONTROL Help]** 아이콘이 추가됩니다.

<table id="table_64BBC67B1BB44B1197FF7E5E7B067696"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 설명서 링크 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 마케팅 Reports &amp; Analytics </td> 
   <td colname="col2">Adobe 마케팅 보고 및 분석 <span class="uicontrol"></span> 도움말 페이지로 엽니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Idea Exchange </td> 
   <td colname="col2">Idea Exchange 로그인 <span class="uicontrol"> 으로 엽니다</span>. 이 온라인 포털에서는 사용자가 데이터 워크벤치에 업데이트 변경 사항 및 개선 아이디어를 제공할 수 있습니다. 이러한 고객 중심의 아이디어는 모든 사용자가 투표에 참여할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 도움말 </td> 
   <td colname="col2">Data Workbench 설명서를 <span class="uicontrol"> 엽니다</span>. <p>&lt;F1&gt; <span class="uicontrol"> 을 눌러</span> 작업 공간 내에서 도움말을 열 수도 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 정보 </td> 
   <td colname="col2">데이터 워크벤치의 <span class="uicontrol"> 클라이언트 버전을</span> 확인하려면 엽니다. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>를 눌러 작업 공간 `<F1>` 에서 설명서를 열 수도 있습니다.

## 작업 공간 보기 드래그 {#section-9129c340c21d45a3864c923884cd4382}

작업 영역이 볼 수 있는 화면보다 큰 경우 보기를 이동하여 작업 공간 내의 모든 요소를 볼 수 있습니다. 시각화 및 표 외부의 배경을 클릭하고 화면을 드래그하여 작업 공간 내에서 볼 수 있는 영역을 이동할 수 있습니다. 작업 공간 프레임 내에서 보기를 드래그하면 커서가 손 아이콘으로 바뀝니다.

![](assets/drag_workspace.png)

## 작업 공간 보기 변경을 위한 빠른 키 {#section-d8322f72423f437aa2e34f2188b1341c}

새로운 빠른 키를 사용하면 창 및 전체 페이지 보기 간에 작업 영역의 크기를 조정하고 조정할 수 있습니다.

<table id="table_A01C514C99F043338D183A6839E03DEA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 명령 </th> 
   <th colname="col2" class="entry"> 빠른 키 </th> 
   <th colname="col3" class="entry"> 결합된 메뉴 명령 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><b>전체 화면 보기</b>. 작업 공간이 화면을 채우고 새 크기를 조정합니다. </td> 
   <td colname="col2"><b>Ctrl +</b> <p>Ctrl +(키패드) </p> <p><i> 또는 </i> </p> <p>Ctrl Shift +(키보드) </p> </td> 
   <td colname="col3"> 
    <ul id="ul_C7C731B894D946D9916F50806F015857"> 
     <li id="li_452B4C119B1A40038A408CFFC53653A9">파일 &gt; 페이지 크기 &gt; 화면 채우기 <p><i>follby</i> </p> </li> 
     <li id="li_DE9B8B31B9F24A6AA68A1D0DB886B501">파일 &gt; 작업 공간 조정 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>창 보기</b>. 작업 공간은 표준 창 보기에 표시되고 새 크기에 맞게 조정됩니다. </td> 
   <td colname="col2"><b>Ctrl+빼기</b> <p>Ctrl - </p> </td> 
   <td colname="col3"> 
    <ul id="ul_3474B9EFD69343C09BC84E485D896C28"> 
     <li id="li_820BAED76FF24A5785E6D89C5C692DD5">파일 &gt; 페이지 크기 &gt; 표준 <p><i>follby</i> </p> </li> 
     <li id="li_337789F282CE4C2C990C67B115782454">파일 &gt; 작업 공간 조정 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 버그 수정 {#section-8704a9ac358246cd81233dd0982d534f}

* 쿼리 검색어에 대한 검색 엔진 변경 사항을 처리하도록 시각적 사이트 조회 파일을 업데이트했습니다.
* 가져오기에 성공했더라도 클라이언트 워크스테이션에서 작업 공간을 가져올 때 부정확한 오류 메시지 &quot;작업 공간을 가져오지 못했습니다.&quot;가 수정되었습니다.
* &quot;412 구성 충돌&quot; 메시지를 표시하는 워크스테이션 연결 오류가 이제 시스템 작업을 식별하는 사용자에게 친숙한 메시지로 대체되었습니다.
* 이제 &quot;post&quot; 명령을 보고서 서버에서 실행할 수 있습니다.
* 중국어 간체에 대한 클라이언트 사용자 인터페이스의 사용자 인터페이스 오류를 수정했습니다.
* Adobe Analytics은 Adobe Experience Cloud과 통합된 프로필 및 대상을 활용할 수 있는 데이터 피드를 업데이트했습니다. 모든 Data Workbench 사용자는 2014년 4월 21일까지 이러한 전환을 위한 환경을 준비해야 했습니다.

   프로파일과 대상은 Adobe Analytics에서 고객을 전체적으로 파악하기 위해 도입되었습니다. 이 새로운 서비스는 Adobe Experience Cloud 내에서 사용할 수 있으며 Analytics 내에서 이러한 기능에 대한 기반 설정을 시작하기 위해 분석 도구 간에 더 많은 가치를 창출할 수 있습니다. 새 Experience Cloud 방문자 식별자는 새 데이터 피드 및 전역 방문자 식별자에 맞게 다른 개선 사항 및 개선 사항과 함께 데이터 피드에 추가됩니다.
* 작업 영역을 가져올 때 가져오기가 성공적임에도 불구하고 오류 메시지가 표시됩니다.

## 업그레이드 요구 사항 {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* 속성 프로필은 Analytics(SC/Insight) 데이터 피드를 사용하도록 Adobe SC 프로필을 구현한 사용자에 대해 구성됩니다. 기본적으로 마케팅 및 전환 이벤트는 규칙 기반 모델에서 평가되는 기본 상호 작용으로 사용됩니다.
* Data Workbench 6.2로 업그레이드하는 Adobe SC 프로파일 사용자의 경우 기본 구성을 사용하지 않는 경우 파일의 [!DNL x-bot_id] 값이 [!DNL SC Fields.cfg] 디코딩되고 있는지, 필드 [!DNL x-bot_id] 가 [!DNL Decoding Instructions.cfg] 및 [!DNL Exclude Hit.cfg] 파일에 올바르게 나열되는지 확인하십시오. 이 문제는 기본 구성에서 구성 파일을 수정한 경우에만 발생합니다.

* Adobe SC 프로필의 **[!UICONTROL Dataset]** > **[!UICONTROL Log Processing]** **[!DNL SC Fields.cfg]** > 파일에서 사용되지 않은 필드를 삭제한 경우 속성 프로필에 사용되는 업데이트된 필드 값을 포함하도록 업데이트해야 합니다.

## 알려진 문제 {#section-dbb307639835493a83409f5f461932b8}

* 3D 산포도 시각화에 설명선이 포함되는 경우 확대/축소는 시각화의 테두리 외부에 플롯을 표시할 수 있습니다.

   해결 방법:먼저 3D 분포도를 확대/축소한 다음 시각화에 콜아웃을 추가합니다.
* 지표 패널의 지표를 지표 열 외부에 있는 지표 범례로 드래그하면 작업 영역에서 지표 범례가 삭제됩니다.

   해결 방법:지표를 지표 범례로 드래그하려는 사용자는 첫 번째 열(지표 열)에 드롭해야 합니다.
* 사이드바와 두 옵션을 사용한 인쇄 작업 영역에는 인쇄된 페이지에 대한 저작권 정보가 포함되지 않습니다.
* 작업 영역 이름을 바꾸면 원격 데스크톱 세션에서 워크스테이션 사용이 중단됩니다.
* (중국어 간체 버전에서) 실제 보고서 출력이 보고서 서버에서 유효하지만 이메일 제목 줄 및 첨부 파일 이름은 알아볼 수 없습니다.
* (중국어 간체 버전) 워크시트 시각화에서 단어 감싸기를 사용할 때 현지화된 단어가 올바로 래핑되지 않아 문자열에 정크 문자가 추가됩니다.
* (중국어 간체 버전) 설치 디렉토리의 이름이 영어가 아닌 문자로 지정되어 있으면 Insight.exe를 시작할 수 없습니다.

   해결 방법:실행 파일의 폴더 경로에 있는 영어로만 기본 이름을 유지하거나 이름을 변경합니다.

