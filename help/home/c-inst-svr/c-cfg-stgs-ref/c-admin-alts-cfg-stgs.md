---
description: Insight Server, 반복 또는 변형에 대한 관리 경고를 구성하는 지침입니다.
title: 관리 경고 구성 설정
uuid: c2be2d1e-d81d-4d9f-ac94-4b642dad90b9
exl-id: c75e442e-33e6-4fc8-8368-29482f09e1cc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 4%

---

# 관리 경고 구성 설정{#administrative-alerts-configuration-settings}

{{eol}}

Insight Server, 반복 또는 변형에 대한 관리 경고를 구성하는 지침입니다.

다음 파일에서 매개 변수를 작성합니다.

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
   <td colname="col2"> 카테고리의 이름입니다. 기본값 카테고리가 필요합니다. 이 표에서 오류 카테고리를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 카테고리 </td> 
   <td colname="col2"> 오류를 오류 분류 파일과 함께 분류할 수 있습니다. 각 오류 카테고리에는 자체 수신자 세트와 자체 스로틀 지연이 있을 수 있습니다. 예를 들어, 스로틀 지연 0을 사용하여 [위험] 범주를 만들 수 있으므로 모든 중요한 오류가 [수신자] 목록에 지정된 수신자에게 즉시 이메일로 전송됩니다. 오류 분류 파일의 하위 문자열과 일치하지 않는 오류는 기본 카테고리에 지정됩니다. 새 카테고리를 추가하려면 숫자를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 새로 추가 </span> &gt; <span class="uicontrol"> 오류 카테고리 </span>. 마우스 오른쪽 단추 클릭 작업을 사용하여 복사 또는 제거할 수도 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 분류 파일 </td> 
   <td colname="col2"> <p>각 경고를 분류하는 데 사용할 파일의 이름입니다. 메모장을 사용하여 이 파일을 만듭니다. 이 파일에는 각 행에 탭으로 구분된 세 개의 열이 있어야 합니다. 첫 번째 열은 오류에서 일치하는 문자열입니다. ^기호는 문자열의 시작과 일치하고 $는 문자열 끝에 일치합니다. 다른 모든 문자는 문자 그대로 일치합니다. 두 번째 열은 오류 카테고리에 있는 일치하는 오류의 카테고리입니다. 세 번째는 전송되는 이메일의 실제 오류 메시지 앞에 오는 대체 메시지입니다. 파일을 지정하지 않으면 모든 오류가 기본값으로 분류됩니다. </p> <p>이 파일의 예제를 보려면 <span class="filepath"> 오류 카테고리.txt </span> 조회 디렉토리에 있는 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> From </td> 
   <td colname="col2"> <p>이메일 메시지의 "보낸 사람" 매개 변수에 표시되는 주소입니다. </p> <p>예: <span class="filepath"> server_errors@mycompany.com </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최소 디스크 공간(MB) </td> 
   <td colname="col2"> 서버에서 사용하는 모든 디렉토리에 있는 사용 가능한 디스크 저장소가 이 값 이하로 떨어지면 서버가 e-메일 경고를 생성합니다. 기본값은 1000입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 경고 시간 초과(분) </td> 
   <td colname="col2"> <p>서버가 구성 및 이전에 연결된 상태에서 데이터를 받지 못하면 이메일 경고를 생성합니다 <span class="wintitle"> Sensor </span> 이 시간 창 내에서 사용할 수 있습니다. 기본값은 15입니다. </p> <p> <p>참고:  <span class="wintitle"> Sensor </span> 경고 시간 제한은 <span class="wintitle"> Sensor </span> 이 삭제됩니다. 서버의 서비스가 중지되고 다시 시작되고 <span class="wintitle"> 센서 </span> 연결하지 않으면 서버에서 전자 메일 경고를 생성하지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 주소 </td> 
   <td colname="col2"> <p>보내는 전자 메일에 대한 SMTP 서버의 주소입니다. </p> <p>예: <span class="filepath"> mail.mycompany.com </span></p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 암호 </td> 
   <td colname="col2"> <p>SMTP 서버에 로그인하기 위한 암호입니다. 이 매개 변수는 메일을 보내는 데 로그인이 필요하지 않으면 선택 사항입니다. </p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 사용자 </td> 
   <td colname="col2"> <p>SMTP 서버에 로그인하기 위한 사용자 ID/이름입니다. 이 매개 변수는 메일을 보내는 데 로그인이 필요하지 않으면 선택 사항입니다. </p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 스로틀 지연(초) </td> 
   <td colname="col2"> 이메일을 전송하기 위해 해당 카테고리의 두 오류 사이에 경과해야 하는 최소 시간(초)입니다. 값이 0이면 즉시 이메일을 전송합니다. </td> 
  </tr> 
 </tbody> 
</table>
