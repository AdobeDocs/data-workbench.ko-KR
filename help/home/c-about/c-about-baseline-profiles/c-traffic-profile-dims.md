---
description: 트래픽 프로필에는 방문자 작업을 식별하는 데 도움이 되는 다음 차원이 포함되어 있습니다.
solution: Analytics
title: 트래픽 프로필 차원
topic: Data workbench
uuid: 9c0dabfc-67c9-4772-99ac-4c503c06ea78
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 트래픽 프로필 차원{#traffic-profile-dimensions}

트래픽 프로필에는 방문자 작업을 식별하는 데 도움이 되는 다음 차원이 포함되어 있습니다.

다음 표의 차원은 변형 데이터 세트에 정의되어 있으며 Traffic\Dataset\Transformation directory폴더에 파일이 있습니다.

|  이름  | 유형 | 레벨 | 설명 |
|---|---|---|---|
| 일 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 날짜입니다. |
| 요일 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 요일. |
| 정확한 페이지 지속 시간(숨김) | 숫자 | 페이지 보기 | 페이지 보기 시간에서 다음 페이지 보기 시간을 빼서 측정된 페이지 보기 시간(밀리초)입니다. 세션에서 마지막 페이지 보기의 정확한 지속 시간은 항상 0입니다. |
| 시간 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 시간입니다. |
| 시간 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 시간. |
| 월 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 월입니다. |
| 페이지 보기 | 계산 가능 | 세션 | 페이지 보기 조건을 만족하는 로그 항목 또는 &quot;이벤트 데이터 레코드&quot;입니다. |
| 레퍼러 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 레퍼러의 두 번째 수준 도메인(내부 레퍼러 도메인인 경우 없음)입니다. |
| 세션 | 계산 가능 | 방문자 | 방문자의 관련 연속 활동 기간. 30분 동안 활동하지 않고 외부 레퍼러 도메인 또는 최대 48시간 세션 지속 시간으로 구분됩니다. 이러한 시간 초과와 내부로 간주되는 도메인 집합을 [!DNL Transformation.cfg] 파일에 구성할 수 있습니다. |
| URI | 단순 | 페이지 보기 | 페이지 보기의 URI 체계입니다. URI 차원은 ReplaceURI, PrependURI 및 AppendURI 변형을 사용하여 재정의할 수 있습니다. |
| 방문자 | 계산 가능 | 해당 없음 | x-trackingid의 고유한 값입니다. 일반적으로 지속적인 쿠키를 사용하는 경우 고유 브라우저에 해당합니다. x-trackingid는 IP 번호나 x.509 일반 이름과 같은 다른 고유 식별자를 기반으로 할 수 있습니다. |
| 주 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 주입니다. |

다음 표의 차원은 트래픽 프로필의 차원 디렉토리에 정의됩니다.

<table id="table_02AC8DAD1B62443A96FABCB75C37F23A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 차원 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col03" class="entry"> 레벨 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 브라우저 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 버전 번호(예: MSIE 6.0)를 포함하여 방문자가 사용하는 사용자 에이전트 유형입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 브라우저 유형 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자가 사용하는 사용자 에이전트 유형(예: MSIE). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 엔진 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03">세션 <p>첫 번째 행 </p></td> 
   <td colname="col3"> 방문자가 명명된 검색 엔진에서 검색했을 때의 방문자 세션의 첫 번째 검색 엔진. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다음 URI </td> 
   <td colname="col2"> 파생(URI 차원을 기반으로 하는 ShiftDim) </td> 
   <td colname="col03"> 페이지 보기 </td> 
   <td colname="col3"> 현재 선택한 URI 다음에 있는 다음 URI의 URI입니다. 이 파생 차원은 주어진 URI 다음에 방문자가 수행하는 작업을 분석하는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onetime과 Repeat </td> 
   <td colname="col2"> 파생(반복 방문자 수 및 일회성 방문자 수 지표를 기반으로 하는 SegmentDim) </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자 유형:1회 또는 반복. 일회성 방문자는 사이트에서 한 세션만 보유했지만 반복 방문자는 두 개 이상의 세션을 보유했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 </td> 
   <td colname="col2"> 파생(URI 차원을 기반으로 이름 바꾸기Dim) </td> 
   <td colname="col03"> 페이지 보기 </td> 
   <td colname="col3"> 세션 중에 방문한 각 페이지의 이름입니다. 처음에는 각 페이지의 이름이 URI와 동일하지만 해석하기 쉽도록 변경할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 레퍼러 </td> 
   <td colname="col2"> 내장된 레퍼러 차원으로 상속됨 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자의 브라우저가 제공한 사이트 세션을 처음 참조한 웹 사이트의 두 번째 수준 도메인 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색어 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03">세션 <p>첫 번째 행 </p></td> 
   <td colname="col3"> 방문자가 지정된 검색 엔진에서 검색했을 때 검색 엔진이 전달한 방문자 세션의 첫 번째 검색 구문입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 조건 </td> 
   <td colname="col2"> 다대다 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자에게 명명된 검색 엔진에서 검색 레퍼러 클릭스루가 있을 때 검색 엔진에서 전달된 각 검색 용어입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 기간 </td> 
   <td colname="col2"> 파생(정확한 페이지 기간 지표를 기반으로 하는 MetricDim) </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 30초 단위로 세션 지속 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 번호 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자가 사이트를 방문한 횟수입니다. 예를 들어 첫 번째 방문자는 세션 번호가 "1"이고 두 번째 방문자는 세션 번호가 "2"인 등을 갖습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 페이지 보기 </td> 
   <td colname="col2"> 파생(페이지 보기 횟수 지표를 기반으로 하는 MetricDim) </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 세션의 페이지 보기 수입니다. 예를 들어 세션 페이지 보기 수 차원에서 "3"을 선택하면 정확히 3개의 페이지 보기가 있는 모든 세션이 선택됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 엔진 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자의 브라우저가 제공한 대로 세션 중에 방문자를 사이트로 안내한 이름이 지정된 검색 엔진인 첫 번째 웹 사이트의 두 번째 수준 도메인 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 차원 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 세션이 시작된 시간, 일, 시간, 시간, 주, 요일, 월, 분기 또는 연도. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 보고 차원 </td> 
   <td colname="col2"> 파생(기본 제공 시간 차원에 따라 LastN 및 차원 이름 변경) </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 일 전, 마지막 달의 일, 마지막 주의 일, 이번 주의 일, 이번 주의 일, 오늘 시간, 어제 시간, 지난 12개월, 지난 24시간, 지난 24시간, 지난 3개월, 지난 4개월, 지난 6개월, 지난 6개월, 7일, 마지막 7일 및 오늘, 지난 8주, 지난 9개월, 지난 달, 지난 주, 지난 주, 이번 주, 지난 14일, 이주와 지난 6개월, 이것과 지난 8주, 오늘, 오늘 보고, 오늘 및 지난 30일, 주 이전 및 어제 데이터 집합에서 항상 데이터의 일부를 표시하는 작업 공간 또는 보고서를 작성하는 편리한 방법을 제공합니다. 각 세션은 세션이 시작된 시기를 기반으로 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URI </td> 
   <td colname="col2"> 내장 차원 URI에서 상속됨 </td> 
   <td colname="col03"> 페이지 보기 </td> 
   <td colname="col3"> 본 각 페이지의 URI입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 페이지 보기 </td> 
   <td colname="col2"> 파생(페이지 보기 횟수 지표를 기반으로 하는 MetricDim) </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자에 대한 날짜까지의 페이지 보기 수입니다. 예를 들어 방문자 페이지 보기 횟수 차원에서 "3"을 선택하면 모든 세션에서 정확히 3개의 페이지 보기가 있는 모든 방문자를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 레퍼러 </td> 
   <td colname="col2"> 내장 차원 레퍼러에서 상속됨 </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자의 브라우저가 제공한 첫 번째 세션(방문자의 브라우저가 제공한 대로)에 대해 방문자를 처음으로 사이트에 소개한 웹 사이트의 두 번째 수준 도메인 이름. </td> 
  </tr> 
 </tbody> 
</table>

