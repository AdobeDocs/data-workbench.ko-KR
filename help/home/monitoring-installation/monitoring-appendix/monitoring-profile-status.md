---
description: Data Workbench 프로필 상태 프로필에서 다음 차원을 사용할 수 있습니다.
title: Data Workbench 프로필 상태 프로필의 차원
uuid: bd84a3e5-d1ea-4768-9dac-62f5dfbad49a
exl-id: 57b3ff16-26db-4292-819b-f6cd8e024c2a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 2%

---

# Data Workbench 프로필 상태 프로필의 차원{#dimensions-in-the-data-workbench-profile-status-profile}

{{eol}}

Data Workbench 프로필 상태 프로필에서 다음 차원을 사용할 수 있습니다.

<table id="table_DD143B4F15FF446DAD24BD2473B485B9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>블록</b> </td> 
   <td colname="col2"> 이 구성에서 유일한 계산 가능이며 모든 차원의 루트로 존재합니다. 블록은 서버로 간주될 수 있습니다. x-trackingid 필드를 사용합니다. 블록 ID는 서버 이름과 호스트 이름의 해시이므로 프로필당 서버당 약 하나의 블록이 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지연 시간(분)</b> </td> 
   <td colname="col2"> cs-uri-query(bi)는 x-as-of-delay-minutes 필드에 배치되고 가장 가까운 분으로 반올림됩니다. 지연 시간 분 은 블록에 대한 지연 시간(분)에서 마지막 행을 가져오는 숫자 차원입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>환경</b> </td> 
   <td colname="col2"> cs-uri-query(c) 값은 환경 ID에 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 이 단순 Dimension은 서버가 실행 중인 환경을 표시합니다(제대로 구성된 경우). <p>insight_monitor_agent.cfg 파일에서 설정할 수 있습니다 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 입력 분당 MegaBytes</b> </td> 
   <td colname="col2"> 이 차원에 cs-uri-query(bj) 값이 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 데이터 세트가 빠른 입력에 있는 경우 이 숫자 Dimension 값은 시스템이 데이터를 입력하는 분당 MB를 표시합니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>분당 빠른 병합 MegaBytes</b> </td> 
   <td colname="col2">이 차원에 cs-uri-query(bk) 값이 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 데이터 세트가 빠른 병합에 있는 경우 이 숫자 Dimension 값은 시스템이 병합되는 분당 MB를 표시합니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>필드 GigaBytes</b> </td> 
   <td colname="col2"> 이 차원에 cs-uri-query(bg) 값이 사용됩니다. 값은 1000으로 나누어지고 가장 가까운 정수로 반올림됩니다. 이 숫자 Dimension의 값은 데이터 집합에서 필드가 사용하는 공간의 크기를 표시합니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>호스트</b> </td> 
   <td colname="col2"> 이 차원에 cs-uri-query(b) 값이 사용됩니다. 단순 차원의 값은 블록의 마지막 행입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 Ping</b> </td> 
   <td colname="col2">x-last-ping은 x-unixtime 나누기 10(숫자 차원 크기 제한을 수용하기 위한). 마지막 Ping은 지정된 블록의 마지막 행이며 모니터링 에이전트가 시스템 상태를 마지막으로 로깅한 시간을 나타냅니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로그 읽기 비율</b> </td> 
   <td colname="col2">이 숫자 차원에 cs-uri-query(be) 값이 사용됩니다. 지정된 블록의 마지막 행입니다. 이 차원은 읽고 있는 로그의 백분율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>처리 모드 ID</b> </td> 
   <td colname="col2"> cs-uri-query(bb) 값은 이 단순 Dimension에 사용됩니다. 지정된 블록의 마지막 행입니다. 처리 모드 ID를 사용하면 시스템의 처리 모드를 확인할 수 있습니다(빠른 입력, 빠른 병합, 실시간). <p>참고: 이 차원은 숨겨진 후 클라이언트측 차원 처리 모드에서 친숙한 값으로 다시 표시됩니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>처리가 중지됨</b> </td> 
   <td colname="col2"> x-processing-stilled 필드는 프로필의 현재 실행 중인지 여부를 나타내는 다양한 조건을 통해 만들어집니다. 단순한 차원입니다. <p>참고: 이 차원은 DPU 간에 공정하게 분배할 입력 로그가 많은 경우에 가장 잘 작동합니다. 예를 들어 하루에 하나의 대용량 파일만 로드되는 경우 Data Workbench는 1시간 이상 "중지"로 표시되고 이로 인해 이 차원에서 긍정 오류가 판독될 수 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>프로필</b> </td> 
   <td colname="col2"> cs-uri-query(ba) 값은 이 단순 Dimension에 사용됩니다. 이 차원은 현재 모니터링 중인 프로필의 이름을 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>소스 후방</b> </td> 
   <td colname="col2"> cs-uri-query(bl)의 마지막 행이 x-source-furnest-behind 필드에 복사됩니다. 단순 Dimension은 지정된 블록에 마지막 행을 사용합니다. 이 차원은 데이터 소스의 마지막 연락처가 발생한 시점을 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>변형 비율</b> </td> 
   <td colname="col2"> cs-uri-query(bf) 값은 이 숫자 차원에 사용됩니다. 지정된 블록의 마지막 행입니다. 이 차원은 전체 데이터 변환의 백분율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>시간 차원</b> </td> 
   <td colname="col2"> 시간, 일, 주, 월, 시간 및 요일은 모두 x-timestamp 필드에서 파생됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>그룹</b> </td> 
   <td colname="col2"> 결과 데이터 집합을 필터링할 다른 방법을 제공하는 그룹화 단어 insight_monitor_agent.cfg 파일에서 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지표</b> </td> 
   <td colname="col2"> 다음은 Data Workbench 프로필 모니터링 프로필에 포함된 지표와 이러한 지표가 파생된 방법을 나열합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지연 시간(분)</b> </td> 
   <td colname="col2"> 이 지표는 각 블록에 대한 지연 시간 분 의 합계이며, 블록 지표로 나눈 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지연 시간(초)</b> </td> 
   <td colname="col2"> 이 지표는 각 블록에 대한 지연 시간(초)의 합계이며, 총 블록 수로 나눈 값입니다. (기준 지연 시간 초 Dimension이 즉시 구성되지 않음) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>블록</b> </td> 
   <td colname="col2"> 각 블록에 대해 1을 합합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 입력 시간(분)</b> </td> 
   <td colname="col2"> 각 블록에 대한 빠른 입력 MegaBytes의 합계는 빠른 입력 MegaBytes per Minute가 0보다 큰 경우 블록 수로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 병합(분) MB</b> </td> 
   <td colname="col2"> 각 블록에 대한 Fast Merge MegaBytes/Minute의 합계는 Fast Merge MegaBytes per Minute가 0보다 큰 경우 블록 수로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>필드 GigaBytes</b> </td> 
   <td colname="col2"> 각 블록에 대한 필드 GB의 합계를 블록 지표로 나눈 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 Ping 페이지</b> </td> 
   <td colname="col2"> 시간 기준 - 마지막 Ping 시간 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 Ping 시간</b> </td> 
   <td colname="col2"> 각 블록에 대한 마지막 Ping의 합계를 블록으로 나눈 다음 10으로 곱합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로그 읽기</b> </td> 
   <td colname="col2"> Log Reading Percentage가 0보다 큰 경우 Log Reading은 각 블록에 대한 로그 읽기 백분율의 합계이며, 이 값은 모두 10으로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>처리가 중지됨</b> </td> 
   <td colname="col2"> 각 블록에 대한 처리 정지된 Dimension의 합계로서, 블록 지표로 나눈 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>변환</b> </td> 
   <td colname="col2"> 각 블록에 대한 변환 백분율의 합은 변환 백분율이 0보다 큰 경우 모두 10으로 나누어집니다. </td> 
  </tr> 
 </tbody> 
</table>
