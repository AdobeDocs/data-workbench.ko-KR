---
description: 다음 차원은 데이터 워크벤치 기록 프로파일에서 사용할 수 있습니다.
solution: Analytics
title: 데이터 워크벤치 기록 프로파일의 차원
topic: Data workbench
uuid: 6d93fba4-986b-46a4-9479-aeb54853dff5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 워크벤치 기록 프로파일의 차원{#dimensions-in-the-data-workbench-historic-profile}

다음 차원은 데이터 워크벤치 기록 프로파일에서 사용할 수 있습니다.

## 데이터 워크벤치 기록 프로파일의 차원 {#section-96f1b64f5cb84411b630f97f227d888d}

다음 차원은 데이터 워크벤치 기록 프로파일에서 사용할 수 있습니다.

<table id="table_3EAEA68E73BE431D841F7F2E83EDD6AC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>블록</b> </td> 
   <td colname="col2">이 구성에서 유일한 계산 가능한 것은 모든 차원의 루트입니다. 블록을 서버로 간주할 수 있습니다. x-trackingid 필드를 사용합니다. <p>참고: 블록 ID는 서버 이름과 호스트 이름의 해시이므로 프로파일당 서버당 약 하나의 블록이 있습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ping</b> </td> 
   <td colname="col2"> 블록 계산 가능한 차원입니다. 프로필의 각 데이터 행은 모니터링 에이전트의 Ping입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>경고 중요</b> </td> 
   <td colname="col2"> cs-uri-query(ad) 값에서 작성된 숫자 차원입니다. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>경고 중지</b> </td> 
   <td colname="col2"> cs-uri-query(ac) 값에서 작성된 Numeric Dimension Ping 수준에서 구현되어 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>경고 경고</b> </td> 
   <td colname="col2"> cs-uri-query(ae) 값에서 작성된 숫자 차원. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>모든 프로필 재처리</b> </td> 
   <td colname="col2"> cs-uri-query(aa) 값에서 작성된 숫자 차원. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하고 cs-uriquery(k)가 비어 있지 않은 경우 설정됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>지연 시간(분) 기준</b> </td> 
   <td colname="col2"> cs-uri-query(bi)는 x-as-of-delay-minutes 필드에 삽입되고 가장 가까운 분으로 반올림됩니다. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>능력 행 백분율</b> </td> 
   <td colname="col2"> cs-uri-query(r) 값에서 작성된 숫자 차원. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하고 cs-uriquery(k)가 비어 있지 않은 경우 설정됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>용량 크기 백분율</b> </td> 
   <td colname="col2"> cs-uri-query(n) 값에서 작성된 숫자 차원. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하고 cs-uriquery(k)가 비어 있지 않은 경우 설정됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>구성 요소 확인 성공</b> </td> 
   <td colname="col2"> cs-uri-query(v) 값을 기반으로 구축된 단순 차원. Ping 수준에서 빌드되고 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>구성 요소 오류</b> </td> 
   <td colname="col2"> cs-uri-query(ao)는 "|" 구분 기호로 분할되어 x-components-in-error 필드에 복사됩니다. x-components-in-error 필드에서 작성한 다대다 차원입니다. Ping 수준에 맞게 구축 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>자세한 확인 시간(초)</b> </td> 
   <td colname="col2"> cs-uri-query(l) 값에서 작성된 숫자 차원. Ping 수준에 따라 cs-uri-query(k)가 비어 있지 않음을 알려줍니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>세부 확인 성공</b> </td> 
   <td colname="col2"> cs-uri-query(k) 값을 기반으로 구축된 단순 차원. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dimension GigaBytes</b> </td> 
   <td colname="col2"> cs-uri-query(bc)는 x-dimension-기가바이트 필드에 복사됩니다. x-dimension-기가바이트 필드는 cs-uri-query(a) matching "2"에 대해 조건이 붙은 이 Simple Dimension의 사용자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>디스크 "x" 사용 비율</b> </td> 
   <td colname="col2"> 이러한 숫자 차원은 cs-uri-query(ah, ai, aj, ak, al) 값에서 구성됩니다. Ping 수준에서 빌드되고 cs-uri-query(a)에 대해 조건이 설정됩니다. "1"과 일치하고 cs-uri-query(k)는 비어 있지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>예상 쓸비 감소</b> </td> 
   <td colname="col2"> x-estimated-sweep-dekaseconds 필드는 이 숫자 차원에 사용됩니다. 이 시간은 서버의 예상 청소 시간을 10으로 나눈 값입니다(치수의 크기를 보다 적절하게 만들기 위해 비우기 측정 해상도 감소). <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 입력 분당 메가 바이트 수</b> </td> 
   <td colname="col2"> cs-uri-query(bj) 값은 이 차원에 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 데이터 세트가 빠른 입력인 경우 이 숫자 차원 값은 시스템이 데이터를 입력하는 분당 MB를 표시합니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>분당 MegaBytes 빠른 병합</b> </td> 
   <td colname="col2">cs-uri-query(bk) 값은 이 차원에 사용됩니다. 블록의 마지막 행은 차원의 값으로 사용됩니다. 데이터 세트가 빠른 병합인 경우 이 숫자 차원 값은 시스템이 병합되는 분당 MB를 표시합니다. <p><p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>필드 기가바이트</b> </td> 
   <td colname="col2">cs-uri-query(bg) 값이 이 차원에 사용됩니다. 값은 1000으로 나누며 가장 가까운 정수로 반올림됩니다. 이 숫자 차원 값은 데이터 세트에 있는 필드가 사용하는 공간을 표시합니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>그룹</b> </td> 
   <td colname="col2"> cs-uri-query(x) 값에서 Ping 수준에서 작성된 단순 차원. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>호스트</b> </td> 
   <td colname="col2"> cs-uri-query(b) 값은 이 차원에 사용됩니다. 단순 차원의 값은 블록의 마지막 행입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>마지막 핑</b> </td> 
   <td colname="col2"> x-unixtime 필드가 x-last-ping으로 복사되고 10으로 나누어져 카디널리티를 줄입니다. 숫자 차원은 블록 수준에서 빌드되고 x-last-ping 필드를 사용합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로드 평균</b> </td> 
   <td colname="col2"> 지정된 서버의 cs-uri-query(i) 값에 대해 마지막 행을 사용하는 숫자 차원입니다. cs-uri-query(k)가 비어 있지 않은 경우 조건이 적용됩니다. 이 차원은 모니터되는 시스템의 서버에서 평균 로드를 계산하는 데 사용됩니다. <p><p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>로그 읽기 비율</b> </td> 
   <td colname="col2">cs-uri-query(be) 값은 Ping 수준에서 작성된 이 숫자 차원에 사용됩니다. 이 차원은 읽고 있는 로그의 백분율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 페이지 파일 비율</b> </td> 
   <td colname="col2"> Ping 수준에서 작성된 cs-uri-query(o) 값을 사용하는 Numeric 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a) "1"과 일치하는 경우 조건이 적용됩니다. 이 차원은 페이지 파일 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>총 메모리 물리적 메가 바이트 수</b> </td> 
   <td colname="col2">Ping 수준에서 작성된 cs-uri-query(ag) 값을 사용하는 Numeric 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a) "1"과 일치하는 경우 조건이 적용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 실제 백분율</b> </td> 
   <td colname="col2">Ping 수준에서 작성된 cs-uri-query(ag) 값을 사용하는 Numeric 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a) "1"과 일치하는 경우 조건이 적용됩니다. 이 차원은 각 서버의 실제 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>메모리 쿼리 비율</b> </td> 
   <td colname="col2"> Ping 수준에서 cs-uri-query 값을 사용하는 Numeric 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a) "1"과 일치하는 경우 조건이 적용됩니다. 이 차원은 각 서버의 쿼리 메모리 사용 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>네트워크 연결</b> </td> 
   <td colname="col2"> Ping 수준에서 작성된 cs-uri-query(q) 값을 사용하는 Numeric 차원입니다. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a) "1"과 일치하는 경우 조건이 적용됩니다. 이 값은 해당 서버에 대한 네트워크 연결 수를 표시하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>출력 행</b> </td> 
   <td colname="col2"> cs-uri-query(bh) 값은 100000으로 나누어지고 x-output-rows 필드로 복사되어 차원의 크기를 줄입니다. X-output-rows는 Ping 수준에서 작성된 Numeric Dimension에서 사용되며, cs-uri-query(a)는 "2"와 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ping 유형 ID</b> </td> 
   <td colname="col2"> Ping 수준에서 cs-uri-query(a) 값을 사용하여 만든 단순 차원. 이것은 어떤 종류의 핑이 기록되었는지를 보여줍니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>투표 지연 센티초</b> </td> 
   <td colname="col2">cs-uri-query(m) 값은 10으로 나누어져 크기 크기를 줄인 다음 x-poll-latency-censeconds 필드에 복사됩니다. 이것은 Ping 수준에서 작성된 Numeric 차원이며, cs-uri-query(k)는 비어 있지 않고, cs-uri-query(a)는 "1"과 일치합니다. 이 차원은 투표 지연을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>처리 모드 ID</b> </td> 
   <td colname="col2"> cs-uri-query(bb) 값은 Ping 수준에서 구축된 이 단순 차원에 사용됩니다. cs-uri-query(bb)가 비어 있지 않고, cs-uri-query(a)가 "2" 처리 모드 ID와 일치하므로 시스템에서 어떤 처리 모드(빠른 입력, 빠른 병합, 실시간)가 있는지 확인할 수 있습니다. <p>참고: 이 차원은 숨겨진 다음 클라이언트측 차원 처리 모드에서 친숙한 값으로 다시 노출됩니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>프로필</b> </td> 
   <td colname="col2"> cs-uri-query(ba) 값은 이 단순 차원에 사용되며 Ping 수준에서 빌드됩니다. 이 차원은 현재 모니터링하고 있는 프로필의 이름을 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 확인 초</b> </td> 
   <td colname="col2"> cs-uri-query(h) 값은 이 숫자 차원에 사용됩니다. Ping 수준에 따라 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>빠른 확인 성공</b> </td> 
   <td colname="col2"> Ping 수준에서 작성된 cs-uri-query(g) 값을 기반으로 구축된 단순 차원입니다. 빠른 확인 지표를 계산하는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>실시간 처리 비율</b> </td> 
   <td colname="col2"> Ping 수준에서 작성된 cs-uri-query(t) 값을 사용하는 숫자 차원입니다. cs-uri-query(a)가 "1"과 일치하는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>소스 맨 뒤</b> </td> 
   <td colname="col2"> 핑 수준에서 작성된 cs-uri-query(bl) 값을 기반으로 구축된 단순 차원. 이 차원은 데이터 소스의 마지막 연락처가 발생한 시기를 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>임시 DB 공간 비율</b> </td> 
   <td colname="col2">Ping 수준에서 작성된 cs-uri-query(an) 값을 사용하여 작성된 Numeric Dimension. cs-uri-query(k)가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. 지정된 서버에서 사용된 임시 DB 공간의 비율을 계산하는 데 사용됩니다. <p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>변형 백분율</b> </td> 
   <td colname="col2">cs-uri-query(bf) 값은 이 숫자 차원에 사용됩니다. Ping 수준에 따라 만들어집니다. 이 차원은 전체 데이터 변환의 백분율을 계산하는 데 사용됩니다. <p><p>참고: 이 차원은 지표로 평균을 낼 때만 유용하므로 숨겨집니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>데이터 워크벤치 버전</b> </td> 
   <td colname="col2"> cs-uri-query(ab) 값은 이 단순 차원에 사용됩니다. Ping 수준에서 빌드되고 cs-uri-query(ab)가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치하는지 확인합니다. 각 서버에서 실행 중인 데이터 워크벤치 서버 버전이 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>데이터 워크벤치 버전 주</b> </td> 
   <td colname="col2"> cs-uri-query(ab) 값은 분할되고 주요 릴리스 값이 x-insight-version-major 필드에 복사됩니다. Ping 수준에서 작성된 단순 차원이며 x-insight-version-major가 비어 있지 않고 cs-uri-query(a)가 "1"과 일치하는지 확인했습니다. </td> 
  </tr> 
 </tbody> 
</table>

<!-- <a id="section_76D8A4B07BB947558EBED1123EA203D5"></a> -->

