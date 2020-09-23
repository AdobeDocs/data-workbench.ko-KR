---
description: Insight Server, Repeater 또는 Transform에 대한 관리 경고를 구성하는 지침입니다.
solution: Analytics
title: 관리 경고 구성 설정
uuid: c2be2d1e-d81d-4d9f-ac94-4b642dad90b9
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 4%

---


# 관리 경고 구성 설정{#administrative-alerts-configuration-settings}

Insight Server, Repeater 또는 Transform에 대한 관리 경고를 구성하는 지침입니다.

다음 파일에서 매개 변수를 완료합니다.

[!DNL Product Name installation directory\Components\Administrative Alerts.cfg]

<table id="table_5A2298906D5F4215B8FAC42CACBC0002"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 카테고리 </td> 
   <td colname="col2"> 카테고리 이름입니다. 기본값 카테고리가 필요합니다. 이 표의 오류 범주를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 범주 </td> 
   <td colname="col2"> 오류 분류 파일과 함께 오류를 분류할 수 있습니다. 각 오류 범주에는 자체 수신자 세트와 자체 스로틀 지연이 있을 수 있습니다. 예를 들어 스로틀 지연 0으로 위기 범주를 만들면 모든 중요한 오류가 [수신자] 목록에 지정된 수신자에게 즉시 이메일로 전송될 수 있습니다. 오류 분류 파일의 하위 문자열과 일치하지 않는 오류는 기본 카테고리에 할당됩니다. 새 카테고리를 추가하려면 숫자를 마우스 오른쪽 단추로 클릭하고 새로 추가 <span class="uicontrol"> &gt; </span> 오류 범주 <span class="uicontrol"> </span>를 클릭합니다. 마우스 오른쪽 단추 클릭 동작을 사용하여 복사 또는 제거할 수도 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 분류 파일 </td> 
   <td colname="col2"> <p>각 경고를 분류하는 데 사용할 파일의 이름입니다. 메모장을 사용하여 이 파일을 만듭니다. 이 파일에는 각 줄에 3개의 열이 있고 탭으로 구분되어 있어야 합니다. 첫 번째 열은 오류와 일치하는 문자열입니다. ^기호는 시작과 일치하고 $는 문자열의 끝과 일치합니다.다른 모든 문자는 문자 그대로 일치합니다. 두 번째 열은 오류 카테고리에 있는 일치하는 오류 카테고리입니다. 세 번째 메시지는 전송되는 이메일의 실제 오류 메시지 앞에 오는 대체 메시지입니다. 파일을 지정하지 않으면 모든 오류가 기본값으로 분류됩니다. </p> <p>이 파일의 예를 보려면 조회 디렉토리에서 <span class="filepath"> Error Categories.txt </span> 파일을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> From </td> 
   <td colname="col2"> <p>이메일 메시지의 "보낸 사람" 매개 변수에 표시되는 주소입니다. </p> <p>예: <span class="filepath"> server_errors@mycompany.com </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최소 디스크 공간(MB) </td> 
   <td colname="col2"> 서버에서 사용하는 모든 디렉토리의 사용 가능한 디스크 스토리지가 이 값 아래로 떨어지면 서버가 이메일 경고를 생성합니다. 기본값은 1000입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 경고 시간 초과(분) </td> 
   <td colname="col2"> <p>서버가 이 시간 창 내에 구성되고 이전에 연결된 <span class="wintitle"> 센서에서 데이터를 받지 못하면 이메일 알림 </span> 을 생성합니다. 기본값은 15입니다. </p> <p> <p>참고: <span class="wintitle"> 센서 </span> 경고 시간 제한은 센서에 대한 기존 연결이 <span class="wintitle"> 끊어진 경우에만 </span> 작동합니다. 서버 서비스가 중지되고 다시 시작되고 센서가 <span class="wintitle"> 연결되지 </span> 않으면 서버가 이메일 경고를 생성하지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 주소 </td> 
   <td colname="col2"> <p>발신 전자 메일에 대한 SMTP 서버의 주소입니다. </p> <p>예: <span class="filepath"> mail.mycompany.com </span></p> <p>설명된 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 암호 </td> 
   <td colname="col2"> <p>SMTP 서버에 로그인하기 위한 비밀번호입니다. 이 매개 변수는 메일을 보내는 데 로그인이 필요하지 않은 경우 선택 사항입니다. </p> <p>설명된 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 사용자 </td> 
   <td colname="col2"> <p>SMTP 서버에 로그인하기 위한 사용자 ID/이름입니다. 이 매개 변수는 메일을 보내는 데 로그인이 필요하지 않은 경우 선택 사항입니다. </p> <p>설명된 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 스로틀 지연(초) </td> 
   <td colname="col2"> 이메일을 보낼 때 해당 범주의 두 오류 사이에 경과해야 하는 최소 시간(초)입니다. 값 0은 이메일을 즉시 전송합니다. </td> 
  </tr> 
 </tbody> 
</table>

