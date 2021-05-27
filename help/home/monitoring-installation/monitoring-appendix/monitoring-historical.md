---
description: Data Workbench 내역 프로필에서는 다음 차원을 사용할 수 있습니다.
title: Data Workbench 내역 프로필의 차원
uuid: 6d93fba4-986b-46a4-9479-aeb54853dff5
exl-id: 9df1f317-a985-4132-b32e-f2263e0c23b2
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 1%

---

# Data Workbench 내역 프로필의 차원{#dimensions-in-the-data-workbench-historic-profile}

Data Workbench 내역 프로필에서는 다음 차원을 사용할 수 있습니다.

## Data Workbench 내역 프로필의 차원 {#section-96f1b64f5cb84411b630f97f227d888d}

Data Workbench 내역 프로필에서는 다음 차원을 사용할 수 있습니다.

<table id="table_3EAEA68E73BE431D841F7F2E83EDD6AC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>블록</b> </td> 
   <td colname="col2">이 구성에서 유일한 계산 가능한 것은 모든 차원의 루트입니다. 블록은 서버로 간주될 수 있습니다. x-trackingid 필드를 사용합니다. <p>참고: 블록 ID는 서버 이름과 호스트 이름의 해시이므로 프로필당 서버당 약 하나의 블록이 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ping</b> </td> 
   <td colname="col2"> 블록 가산 테이블에서 작성된 가산 차원입니다. 프로필의 각 데이터 행은 모니터링 에이전트의 ping입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>경고 위험</b> </td> 
   <td colname="col2"> cs-uri-query(ad) 값으로 빌드된 숫자 Dimension. Ping 수준에 빌드되어 cs-uri-query(a)가 "1"과 일치됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>경고 다운</b> </td> 
   <td colname="col2"> cs-uri-query(ac) 값으로 빌드된 숫자 Dimension. Ping 수준에서 빌드되며, cs-uri-query(a)가 "1"과 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>경고 경고</b> </td> 
   <td colname="col2"> cs-uri-query(ae) 값으로 빌드된 숫자 Dimension. Ping 수준에 빌드되어 cs-uri-query(a)가 "1"과 일치됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>모든 프로필 재처리</b> </td> 
   <td colname="col2"> cs-uri-query(aa) 값으로 빌드된 숫자 Dimension. Ping 수준에 구축되어 cs-uri-query(a)가 "1"과 일치하고 cs-uriquery(k)가 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지연 시간(분)</b> </td> 
   <td colname="col2"> cs-uri-query(bi)는 x-as-of-delay-minutes 필드에 배치되고 가장 가까운 분으로 반올림됩니다. Ping 수준에 빌드되어 cs-uri-query(a)가 "1"과 일치됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>능력 행 퍼센트</b> </td> 
   <td colname="col2"> cs-uri-query(r) 값에서 만든 숫자 Dimension. Ping 수준에 구축되어 cs-uri-query(a)가 "1"과 일치하고 cs-uriquery(k)가 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>용량 크기 백분율</b> </td> 
   <td colname="col2"> cs-uri-query(n) 값으로 빌드된 숫자 Dimension. Ping 수준에 구축되어 cs-uri-query(a)가 "1"과 일치하고 cs-uriquery(k)가 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>구성 요소 확인 성공</b> </td> 
   <td colname="col2"> cs-uri-query(v) 값으로 빌드된 간단한 Dimension. Ping 수준에서 빌드되고 cs-uri-query(a)가 "1"과 일치하는지 확인했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>오류가 발생한 구성 요소</b> </td> 
   <td colname="col2"> cs-uri-query(ao)는 "|" 구분 기호로 분할되어 x-components-in-error 필드에 복사됩니다. x-components-in-error 필드에서 빌드된 Dimension 중 다대다. Ping 수준에서 빌드됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>자세한 확인 시간(초)</b> </td> 
   <td colname="col2"> cs-uri-query(l) 값으로 빌드된 숫자 Dimension. Ping 수준에 빌드되어 cs-uri-query(k)가 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>자세한 확인 성공</b> </td> 
   <td colname="col2"> cs-uri-query(k) 값으로 빌드된 단순 Dimension. Ping 수준에 빌드되어 cs-uri-query(a)가 "1"과 일치됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dimension GigaBytes</b> </td> 
   <td colname="col2"> cs-uri-query(bc)가 x-dimension-gb 필드에 복사됩니다. x-dimension-gb 필드는 cs-uri-query(a) "2"와 일치하는 이 Simple Dimension의 사용자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>사용된 디스크 "x" 비율</b> </td> 
   <td colname="col2"> 이러한 숫자 Dimension은 cs-uri-query(ah, ai, aj, ak, al) 값에서 구성됩니다. Ping 수준에서 빌드되고 cs-uri-query(a)에 따라 조건이 "1"과 일치하고 cs-uri-query(k)가 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>예상 청소 발생 시간</b> </td> 
   <td colname="col2"> 이 숫자 Dimension에서 x-estimated-sweep-decasections 필드가 사용됩니다. 이 시간은 서버의 예상 청소 시간을 10으로 나눈 것입니다(차원의 크기를 합리적으로 만들기 위해 청소 측정 해상도가 감소). <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 입력 분당 MegaBytes</b> </td> 
   <td colname="col2"> 이 차원에 cs-uri-query(bj) 값이 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 데이터 세트가 빠른 입력에 있는 경우 이 숫자 Dimension 값은 시스템이 데이터를 입력하는 분당 MB를 표시합니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>분당 빠른 병합 MegaBytes</b> </td> 
   <td colname="col2">이 차원에 cs-uri-query(bk) 값이 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 데이터 세트가 빠른 병합에 있는 경우 이 숫자 Dimension 값은 시스템이 병합되는 분당 MB를 표시합니다. <p><p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>필드 GigaBytes</b> </td> 
   <td colname="col2">이 차원에 cs-uri-query(bg) 값이 사용됩니다. 값은 1000으로 나누어지고 가장 가까운 정수로 반올림됩니다. 이 숫자 Dimension의 값은 데이터 집합에서 필드가 사용하는 공간의 크기를 표시합니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>그룹</b> </td> 
   <td colname="col2"> cs-uri-query(x) 값에서 Ping 수준에서 빌드된 단순 Dimension. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>호스트</b> </td> 
   <td colname="col2"> 이 차원에 cs-uri-query(b) 값이 사용됩니다. 단순 차원의 값은 블록의 마지막 행입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 Ping</b> </td> 
   <td colname="col2"> x-unixtime 필드는 x-last-ping에 복사되고 10으로 나누어져 카디널리티를 줄입니다. 숫자 Dimension은 블록 수준에서 빌드되며 x-last-ping 필드를 사용합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로드 평균</b> </td> 
   <td colname="col2"> 주어진 서버의 cs-uri-query(i) 값에 대해 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 이 차원은 모니터링 중인 시스템의 서버에 대한 평균 로드를 계산하는 데 사용됩니다. <p><p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로그 읽기 비율</b> </td> 
   <td colname="col2">cs-uri-query(be) 값은 Ping 수준에서 빌드된 이 숫자 차원에 사용됩니다. 이 차원은 읽고 있는 로그의 백분율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 페이지 파일 비율</b> </td> 
   <td colname="col2"> Ping 수준에서 빌드된 cs-uri-query(o) 값을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치하는 경우 조건이 적용됩니다. 이 차원은 페이지 파일 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>총 메모리 실제 MegaBytes</b> </td> 
   <td colname="col2">Ping 수준에서 빌드된 cs-uri-query(ag) 값을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1과 일치하는 경우 조건이 적용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 실제 비율</b> </td> 
   <td colname="col2">Ping 수준에서 빌드된 cs-uri-query(ag) 값을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1과 일치하는 경우 조건이 적용됩니다. 이 차원은 각 서버의 실제 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 쿼리 비율</b> </td> 
   <td colname="col2"> Ping 수준에서 cs-uri-query 값을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1과 일치하는 경우 조건이 적용됩니다. 이 차원은 각 서버의 쿼리 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>네트워크 연결</b> </td> 
   <td colname="col2"> Ping 수준에서 빌드된 cs-uri-query(q) 값을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1과 일치하는 경우 조건이 적용됩니다. 지정된 서버에 대한 네트워크 연결 수를 표시하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>출력 행</b> </td> 
   <td colname="col2"> cs-uri-query(bh) 값은 100000으로 분할되어 x-output-rows 필드에 복사되어 치수 크기를 줄입니다. X-output-rows는 Ping 수준에서 빌드된 숫자 Dimension에서 사용되며 cs-uri-query(a)는 "2"와 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ping 유형 ID</b> </td> 
   <td colname="col2"> Ping 수준에서 cs-uri-query(a) 값을 사용하여 빌드된 간단한 Dimension. 이는 어떤 Ping이 기록되었는지 보여줍니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>폴링 지연 시간(분)</b> </td> 
   <td colname="col2">cs-uri-query(m) 값은 10으로 나누어 차원 크기를 줄이고 x-poll-latency-centi 초 필드에 복사됩니다. Ping 수준에서 빌드된 숫자 차원으로서, cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치합니다. 이 차원은 폴링 지연을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>처리 모드 ID</b> </td> 
   <td colname="col2"> cs-uri-query(bb) 값은 Ping 수준에서 빌드된 이 단순 Dimension에 사용됩니다. cs-uri-query(bb)가 비어 있지 않고 cs-uri-query(a)가 "2" 처리 모드 ID와 일치하면 시스템이 어떤 처리 모드인지 볼 수 있습니다(빠른 입력, 빠른 병합, 실시간). <p>참고: 이 차원은 숨겨진 후 클라이언트측 차원 처리 모드에서 친숙한 값으로 다시 표시됩니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>프로필</b> </td> 
   <td colname="col2"> cs-uri-query(ba) 값은 이 단순 Dimension에 사용되며 Ping 수준에서 빌드됩니다. 이 차원은 현재 모니터링 중인 프로필의 이름을 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 확인 초</b> </td> 
   <td colname="col2"> 이 숫자 Dimension에 cs-uri-query(h) 값이 사용됩니다. Ping 수준에 빌드되어 cs-uri-query(a)가 "1"과 일치됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 확인 성공</b> </td> 
   <td colname="col2"> Ping 수준에서 빌드된 cs-uri-query(g) 값으로 빌드된 단순 차원입니다. 이 변수는 빠른 확인 지표를 계산하는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>실시간 처리 비율</b> </td> 
   <td colname="col2"> Ping 수준에서 빌드된 cs-uri-query(t) 값을 사용하는 숫자 Dimension. cs-uri-query(a)가 "1"과 일치하는 조건이 적용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>소스 후방</b> </td> 
   <td colname="col2"> Ping 수준에서 빌드된 cs-uri-query(bl) 값으로 빌드된 간단한 Dimension. 이 차원은 데이터 소스의 마지막 연락처가 발생한 시점을 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>임시 DB 공간 비율</b> </td> 
   <td colname="col2">Ping 수준에서 빌드된 cs-uri-query(an) 값을 사용하여 작성된 숫자 Dimension. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치한다는 조건이 적용됩니다. 특정 서버에서 사용된 Temp DB 공간의 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>변형 비율</b> </td> 
   <td colname="col2">cs-uri-query(bf) 값은 이 숫자 차원에 사용됩니다. Ping 수준에서 빌드됩니다. 이 차원은 전체 데이터 변환의 백분율을 계산하는 데 사용됩니다. <p><p>참고: 이 차원은 지표로 평균한 경우에만 유용하므로 숨겨져 있습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Data Workbench 버전</b> </td> 
   <td colname="col2"> cs-uri-query(ab) 값은 이 단순 Dimension에 사용됩니다. Ping 수준에서 빌드되고 cs-uri-query(ab)가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치하는지 확인했습니다. 각 서버에서 실행 중인 Data Workbench 서버의 버전이 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Data Workbench 버전 주요</b> </td> 
   <td colname="col2"> cs-uri-query(ab) 값은 분할되고 주요 릴리스 값은 x-insight-version-major 필드에 복사됩니다. Ping 수준에서 빌드된 단순 Dimension으로, x-insight-version-major가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치합니다. </td> 
  </tr> 
 </tbody> 
</table>

<!-- <a id="section_76D8A4B07BB947558EBED1123EA203D5"></a> -->
