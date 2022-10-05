---
description: 트래픽 프로필에는 방문자 작업을 식별하는 데 도움이 되는 다음 차원이 포함되어 있습니다.
title: 트래픽 프로필 차원
uuid: 9c0dabfc-67c9-4772-99ac-4c503c06ea78
exl-id: 1e7d2904-aa5d-4848-a398-5d4669953be9
source-git-commit: 4ab43bfbad96096fb2cebd77a8be8fa6d49fa7dc
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 8%

---

# 트래픽 프로필 차원{#traffic-profile-dimensions}

{{eol}}

트래픽 프로필에는 방문자 작업을 식별하는 데 도움이 되는 다음 차원이 포함되어 있습니다.

다음 표의 차원은 변환 데이터 집합에 정의되어 있으며 Traffic\Dataset\Transformation 디렉터리에 있는 파일이 포함됩니다.

| 이름 | 유형 | 레벨 | 설명 |
|---|---|---|---|
| 일 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 날짜입니다. |
| 요일 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 요일. |
| 정확한 페이지 기간(숨김) | 숫자 | 페이지 보기 | 해당 페이지 보기 시간으로부터 다음 페이지 보기의 시간을 뺀 시간(밀리초)입니다. 세션에서 마지막 페이지 보기의 정확한 기간은 항상 0입니다. |
| 시간 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 시간입니다. |
| 시간 (일 기준) | 단순 | 세션 | 세션의 첫 번째 로그 항목의 시간 |
| 월 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 월입니다. |
| 페이지 보기 | 계산 가능 | 세션 | 페이지 보기 조건을 충족하는 로그 항목 또는 &quot;이벤트 데이터 레코드&quot;입니다. |
| 레퍼러 | 단순 | 세션 | 세션의 첫 번째 로그 항목에 대한 레퍼러의 두 번째 수준 도메인(내부 레퍼러 도메인인 경우 없음)입니다. |
| 세션 | 계산 가능 | 방문자 | 방문자가 관련된 연속 활동의 기간입니다. 30분 동안 활동이 없고 외부 레퍼러 도메인 또는 최대 48시간 세션 기간으로 구분됩니다. 이러한 시간 초과와 내부로 간주되는 도메인 세트는 모두 [!DNL Transformation.cfg] 파일. |
| URI | 단순 | 페이지 보기 | 페이지 보기의 URI 줄기입니다. ReplaceURI, PrependURI 및 AppendURI 변환을 사용하여 URI 차원을 재정의할 수 있습니다. |
| 방문자 | 계산 가능 | 해당 사항 없음 | x-trackingid의 고유한 값입니다. 일반적으로 영구 쿠키를 사용하는 경우 고유 브라우저에 해당합니다. x-trackingid는 IP 번호 또는 x.509 공통 이름과 같은 기타 고유한 식별자를 기반으로 할 수 있습니다. |
| 주 | 단순 | 세션 | 세션의 첫 번째 로그 항목의 주입니다. |

다음 테이블의 차원은 트래픽 프로필의 Dimension 디렉토리에 정의됩니다.

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
   <td colname="col3"> 방문자가 사용하는 사용자 에이전트 유형(예: MSIE)입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 엔진 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03">세션 <p>첫 번째 행 </p></td> 
   <td colname="col3"> 방문자가 명명된 검색 엔진에서 검색했을 때 방문자 세션에서 첫 번째 검색 엔진입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다음 URI </td> 
   <td colname="col2"> 파생(URI 차원을 기반으로 ShiftDim) </td> 
   <td colname="col03"> 페이지 보기 </td> 
   <td colname="col3"> 현재 선택한 URI 뒤에 있는 다음 URI의 URI입니다. 이 파생 차원은 주어진 URI 이후에 방문자가 다음에 수행하는 작업에 대한 분석을 수행하는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 한 시간과 반복 </td> 
   <td colname="col2"> 파생(반복 방문자 및 1회 방문자 지표를 기반으로 하는 SegmentDim) </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자 유형: 한 번 또는 반복. 한 번 방문하는 사람은 사이트에 세션이 한 번만 있는 반면 반복 방문자는 세션이 두 개 이상 있었습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 </td> 
   <td colname="col2"> 파생(URI 차원을 기반으로 이름 바꾸기) </td> 
   <td colname="col03"> 페이지 보기 </td> 
   <td colname="col3"> 세션 중에 방문한 각 페이지의 이름입니다. 처음에는 각 페이지의 이름이 URI와 동일하지만 쉽게 해석할 수 있도록 변경할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 레퍼러 </td> 
   <td colname="col2"> 기본 제공 레퍼러 차원에서 상속됨 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자의 브라우저가 제공한 사이트 세션을 처음 참조한 웹 사이트의 두 번째 수준 도메인 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 구 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03">세션 <p>첫 번째 행 </p></td> 
   <td colname="col3"> 방문자가 명명된 검색 엔진에서 검색했을 때 검색 엔진이 전달한 방문자 세션의 첫 번째 검색 구문입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색어 </td> 
   <td colname="col2"> 다대다 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자에게 명명된 검색 엔진에서 검색 레퍼러 클릭스루가 있을 때 검색 엔진에서 전달한 각 검색어. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 기간 </td> 
   <td colname="col2"> 파생(정확한 페이지 기간 지표를 기반으로 하는 MetricDim) </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 세션 기간은 30초 단위로 증가합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 번호 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 방문자가 사이트를 방문한 횟수입니다. 예를 들어 처음 방문하는 사람의 세션 번호는 "1"이고, 두 번째 방문자의 세션 번호는 "2"입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 페이지 보기 수 </td> 
   <td colname="col2"> 파생(페이지 보기 수 지표를 기반으로 하는 지표 치수) </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 세션의 페이지 보기 수입니다. 예를 들어, 세션 페이지 보기 수 차원에서 "3"을 선택하면 정확히 3개의 페이지 보기가 있는 모든 세션이 선택됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 엔진 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 세션 중에 방문자를 사이트로 안내한 이름이 지정된 검색 엔진인 첫 번째 웹 사이트의 두 번째 수준 도메인 이름입니다(방문자의 브라우저에서 제공). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 차원 </td> 
   <td colname="col2"> 단순 </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> 세션이 시작된 시간, 일, 시간, 일, 주, 일, 월, 분기 또는 년입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 보고 Dimension </td> 
   <td colname="col2"> 파생(기본 시간 차원을 기반으로 차원 이름 변경 및 마지막 n) </td> 
   <td colname="col03"> 세션 </td> 
   <td colname="col3"> Days Ago, Last Month, Days of Last Week, This Week, Days of This Week, Today, Today, Hours, 지난 12개월, 지난 2주, 지난 24시간, 지난 3개월, 지난 4주, 지난 6개월, 지난 7일, 지난 7일, 오늘, 지난 8주, 지난 9개월, 지난 달, 지난 주, 이번 주, 이번 달, 이번 주, 이번 및 최근 14일, 최근 6개월, 이 달 및 최근 8주, 오늘, 오늘, 오늘 및 최근 30일, 주 전 및 어제의 경우 데이터 집합에 항상 데이터 부분을 표시하는 작업 공간 또는 보고서를 작성하는 편리한 방법을 제공합니다. 각각 세션이 시작된 시기를 기준으로 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URI </td> 
   <td colname="col2"> 기본 제공 Dimension URI에서 상속됨 </td> 
   <td colname="col03"> 페이지 보기 </td> 
   <td colname="col3"> 본 각 페이지의 URI입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 페이지 보기 수 </td> 
   <td colname="col2"> 파생(페이지 보기 수 지표를 기반으로 하는 지표 치수) </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자에 대해 현재까지 페이지 보기 수입니다. 예를 들어 방문자 페이지 보기 수 차원에서 "3"을 선택하면 모든 세션에서 정확히 3개의 페이지 보기가 있는 모든 방문자를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 레퍼러 </td> 
   <td colname="col2"> 기본 제공 차원 레퍼러에서 상속됨 </td> 
   <td colname="col03"> 방문자 </td> 
   <td colname="col3"> 방문자가 첫 번째 세션(방문자의 브라우저에서 제공하는 대로)에 대해 방문자를 사이트에 처음 참조한 웹 사이트의 두 번째 수준 도메인 이름입니다. </td> 
  </tr> 
 </tbody> 
</table>
