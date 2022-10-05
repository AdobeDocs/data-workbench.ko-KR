---
description: Data Workbench 서버 상태 프로필에서 다음 차원을 사용할 수 있습니다.
title: Data Workbench 서버 상태 프로필의 차원
uuid: 4cfe882a-2797-4af9-bd6d-75bc31ee909c
exl-id: 002f6b95-f151-41d9-ae28-9c01c1f621ee
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1366'
ht-degree: 1%

---

# Data Workbench 서버 상태 프로필의 차원{#dimensions-in-the-data-workbench-server-status-profile}

{{eol}}

Data Workbench 서버 상태 프로필에서 다음 차원을 사용할 수 있습니다.

<table id="table_10DFAD7A0C5946B0A2458F6C08D04FC5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>서버</b> </td> 
   <td colname="col2"> x-trackingid 필드에서 빌드된 이 계산 가능한 차원은 현재 Data Workbench를 실행하는 서버를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>에이전트 버전</b> </td> 
   <td colname="col2"> cs-uri-query(af) 값은 이 단순 Dimension에 사용됩니다. 서버의 마지막 비공백 값입니다. 실행 중인 모니터링 에이전트 버전에 대한 빌드 날짜 및 시간을 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>모든 프로필 재처리</b> </td> 
   <td colname="col2"> cs-uri-query(aa) 필드는 이 숫자 Dimension에 사용되며, 해당 서버에 대한 마지막 행의 값이며, cs-uri-query(k)에 있는 조건부 값은 비어 있지 않습니다. 이 차원은 프로필이 재처리되는지 여부를 나타내는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>능력 행 퍼센트</b> </td> 
   <td colname="col2"> cs-uri-query(r) 필드는 이 숫자 Dimension에 사용되며, 해당 서버에 대한 마지막 행의 값이며, cs-uri-query(k)에 있는 조건부 값은 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>용량 크기 백분율</b> </td> 
   <td colname="col2"> cs-uri-query(n) 필드는 이 숫자 Dimension에 사용되며, 해당 서버에 대한 마지막 행의 값이며, cs-uri-query(k)에 대한 조건부 값은 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>일반 이름</b> </td> 
   <td colname="col2"> sc-ur-query(am) 필드는 이 단순 Dimension에 사용되며, 이 값은 주어진 서버에 대한 마지막 비어 있지 않은 값의 값입니다. 모니터링 중인 서버의 일반 이름이 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>구성 요소 확인 성공</b> </td> 
   <td colname="col2"> cs-uri-query(v) 필드는 이 단순 Dimension에 사용되며, 이 값은 지정된 서버의 마지막 행 값입니다. 이 차원은 서버의 구성 요소가 제대로 작동하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>오류가 발생한 구성 요소</b> </td> 
   <td colname="col2"> 교차 행 변환은 cs-uri-query(ao)의 마지막 행 값을 가져와 x-components-in-error 필드에 복사합니다. 이 다대다 차원은 모니터링 중인 서버에 오류가 있는 모든 구성 요소를 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>환경</b> </td> 
   <td colname="col2">cs-uri-query(c) 값은 환경 ID에 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 이 단순 Dimension은 서버가 실행 중인 환경을 표시합니다(제대로 구성된 경우). <p><p>참고: 이 차원은 insight_monitor_agent.cfg에서 설정됩니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>예상 청소 발생 시간</b> </td> 
   <td colname="col2"> 이 숫자 Dimension에서 x-estimated-sweep-decasections 필드가 사용됩니다. 이 시간은 서버의 예상 청소 시간을 10으로 나눈 것입니다(차원의 크기를 합리적으로 만들기 위해 청소 측정 해상도가 감소). <p><p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>호스트</b> </td> 
   <td colname="col2"> 이 차원에 cs-uri-query(b) 값이 사용됩니다. 단순 차원의 값은 블록의 마지막 행입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 Ping</b> </td> 
   <td colname="col2"> x-last-ping은 x-unixtime 나누기 10(숫자 차원 크기 제한을 수용하기 위한). 마지막 Ping은 지정된 블록의 마지막 행이며 모니터링 에이전트가 시스템 상태를 마지막으로 로깅한 시간을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로드 평균</b> </td> 
   <td colname="col2"> 주어진 서버의 cs-uri-query(i) 값에 대해 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 이 차원은 모니터링 중인 시스템의 서버에 대한 평균 로드를 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 페이지 파일 비율</b> </td> 
   <td colname="col2"> 주어진 서버의 cs-uri-query(o) 값에 대해 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 이 차원은 페이지 파일 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>총 메모리 실제 MegaBytes</b> </td> 
   <td colname="col2"> 주어진 서버의 cs-uri-query(ag) 값에 대해 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 실제 비율</b> </td> 
   <td colname="col2"> 주어진 서버의 cs-uri-query(ag) 값에 대해 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 이 차원은 각 서버의 실제 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 쿼리 비율</b> </td> 
   <td colname="col2"> 지정된 서버의 cs-uri-query 값에 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 이 차원은 각 서버의 쿼리 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>네트워크 연결</b> </td> 
   <td colname="col2"> 주어진 서버의 cs-uri-query(q) 값에 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 지정된 서버에 대한 네트워크 연결 수를 표시하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>폴링 지연 시간(분)</b> </td> 
   <td colname="col2"> 이 차원은 폴링 지연을 계산하는 데 사용됩니다. cs-uri-query(m) 값은 10으로 나누어 차원 크기를 줄이고 x-poll-latency-centi 초 필드에 복사됩니다. 특정 서버에 대한 마지막 행을 가져오는 숫자 차원입니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 확인 성공</b> </td> 
   <td colname="col2"> 주어진 서버에 대한 마지막 행의 cs-uri-query(g) 값으로 작성된 단순 차원입니다. 이 변수는 빠른 확인 지표를 계산하는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>임시 DB 공간 비율</b> </td> 
   <td colname="col2"> cs-uri-query(an) 값의 마지막 행이 x-temp-db-space-percentage 필드에 복사됩니다. 특정 서버에서 사용된 Temp DB 공간의 비율을 계산하는 데 사용되는 숫자 Dimension입니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>인사이트 버전</b> </td> 
   <td colname="col2"> cs-uri-query(ab) 값은 이 단순 Dimension에 사용됩니다. 서버의 마지막 비공백 값입니다. 각 서버에서 실행 중인 Data Workbench 서버의 버전이 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>그룹</b> </td> 
   <td colname="col2"> 결과 데이터 집합을 필터링할 다른 방법을 제공하는 그룹화 단어 <p>참고: 이 차원은 insight_monitor_agent.cfg에서 설정됩니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지표</b> </td> 
   <td colname="col2"> 다음은 Data Workbench 프로필 모니터링 프로필에 포함된 지표와 이러한 지표가 파생된 방법을 나열합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>전체 용량</b> </td> 
   <td colname="col2"> 용량 크기 지표에 2를 더한 + 능력 행 지표를 3으로 나눈 것입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>용량 행</b> </td> 
   <td colname="col2"> 서버 지표로 나눈 각 서버의 용량 행 비율 합입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>용량 크기</b> </td> 
   <td colname="col2"> 각 서버에 대한 용량 크기 백분율의 합계를 서버 지표로 나눈 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>구성 요소 확인</b> </td> 
   <td colname="col2"> 구성 요소 확인 성공 이 1인 서버의 수입니다. 서버 수는 서비스가 DPU 또는 FSU인 서버로 나누며 모두 100을 곱합니다(백분율로 만들기). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>디스크 "x"</b> </td> 
   <td colname="col2"> 디스크 지표는 각 서버에 대해 사용된 디스크 백분율에 대한 합계를 서버 지표로 나누어 계산됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>예상 청소 시간(분)</b> </td> 
   <td colname="col2"> 이 값은 각 서버에 대한 예상 청소 예상 소요 시간 합계이며, 예상 청소 범위가 0보다 크고 모두 6으로 나누어진 서버 지표로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 Ping 시간</b> </td> 
   <td colname="col2"> 각 블록에 대한 마지막 Ping의 합계를 블록으로 나눈 다음 10으로 곱합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로드</b> </td> 
   <td colname="col2"> 이 값은 각 서버에 대한 로드 평균의 합계이며, 서버 지표로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 페이지 파일</b> </td> 
   <td colname="col2"> 이것은 각 서버에 대한 메모리 페이지 파일 백분율의 합계이며, 서버 지표로 나눈 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 물리적</b> </td> 
   <td colname="col2"> 이것은 각 서버에 대한 메모리 실제 백분율의 합계이며, 서버 지표로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 쿼리</b> </td> 
   <td colname="col2"> 이것은 각 서버에 대한 메모리 쿼리 백분율의 합계이며, 서버 지표로 나누어집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>네트워크 연결</b> </td> 
   <td colname="col2"> 각 서버에 대한 네트워크 연결 합계를 서버 지표로 나눈 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>폴링 지연 시간 밀리초</b> </td> 
   <td colname="col2"> 이 값은 각 서버에 대한 폴링 지연 시간 센티미터(초)의 합이며, 서버 지표를 구분하며, 모두 10을 곱합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 확인</b> </td> 
   <td colname="col2"> 빠른 확인 성공 이 1인 서버의 수를 서버 지표로 나눈 수로, 모두 100을 곱합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>서버</b> </td> 
   <td colname="col2"> 이것은 각 서버에 대해 하나씩 또는 모니터링되는 총 서버 수의 합계입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>임시 DB</b> </td> 
   <td colname="col2"> 각 서버에 대한 임시 DB 공간 백분율의 합계이며, 서버 지표로 나누어집니다. </td> 
  </tr> 
 </tbody> 
</table>
