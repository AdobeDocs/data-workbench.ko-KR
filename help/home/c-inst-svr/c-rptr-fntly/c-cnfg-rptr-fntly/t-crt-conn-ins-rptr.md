---
description: 네트워크 방화벽이 Insight 컴퓨터의 반복 서버에 대한 액세스를 막지 못하는 경우, Insight를 사용하여 반복 서버를 관리할 수 있도록 반복 서버와 Insight 간에 연결을 만들 수 있습니다.
solution: Analytics
title: Insight와 반복 간의 연결 만들기
uuid: dccce83a-8708-4763-a19a-64d905a9f624
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 4%

---


# Insight와 반복 간의 연결 만들기{#creating-a-connection-between-insight-and-repeater}

네트워크 방화벽이 Insight 컴퓨터의 반복 서버에 대한 액세스를 막지 못하는 경우, Insight를 사용하여 반복 서버를 관리할 수 있도록 반복 서버와 Insight 간에 연결을 만들 수 있습니다.

**반복 서버 간 연결[!DNL Insight]을 만들려면**

1. 탭 [!DNL Insight]에서 [!DNL Admin] **[!UICONTROL Configure Connections to Servers]** 축소판을 클릭하여 서버에 대한 연결 구성 작업 영역을 엽니다.
1. 창에서 [!DNL Insight.cfg] 마우스 오른쪽 단추를 클릭하고 > **[!UICONTROL Servers]** 를 **[!UICONTROL Add new]** 클릭합니다 **[!UICONTROL Server]**.
1. 새 서버의 경우 다음 매개 변수를 완료하십시오.

<table id="table_DD79587255134B5A888A0F57CF10E5B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수의 경우.. </th> 
   <th colname="col2" class="entry"> 분류에 사용할... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2">(선택 사항) 이 <span class="keyword"> Insight</span> 가 사용자 인터페이스에서 반복 서버를 나타내는 데 사용할 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> <p>반복 서버의 호스트 이름 또는 숫자 IP 주소입니다. </p> <p>예: <span class="filepath"> Repeater.mycompany.com</span> 또는 192.168.1.90 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 클라이언트 인증서 </td> 
   <td colname="col2"> <p>둘 이상의 인증서가 없는 한 선택 사항입니다. 이 Insight 사본의 디지털 인증서가 포함된 파일의 <span class="keyword"> 이름입니다</span>. (Insight를 설치하는 동안 다운로드한 <span class="keyword"> 파일입니다</span>.) </p> <p>예: <span class="filepath"> 사만다 스미스</span></p> <p>이 매개 변수를 비워 두면 <span class="keyword"> Insight는</span> 존재하는 모든 인증서를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL 서버 </p> <p>일반 이름 </p> </td> 
   <td colname="col2">반복 서버에 할당된 일반 이름입니다. 이 이름은 라이센스 인증서 내의 반복 서버에 할당된 일반 이름과 일치해야 합니다. 중계기의 인증서 파일(인증서\server_cert.pem<span class="filepath"></span>)에 액세스할 수 있는 경우 메모장과 같은 텍스트 편집기로 파일을 열어 일반 이름을 찾을 수 있습니다. 인증서의 CN 필드에서 일반 이름이 식별됩니다. </td> 
  </tr> 
 </tbody> 
</table>

1. 창 맨 위에서 마우스 오른쪽 단추 **[!UICONTROL (modified)]** 를 클릭하고 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**. [!DNL Insight] 지정한 설정을 사용하여 반복 서버에 연결을 시도합니다. 연결이 설정된 경우 인터페이스에 녹색 서버 아이콘이 [!DNL Servers Manager] 나타납니다. 연결을 설정할 수 없으면 빨간색 아이콘이 표시됩니다.

   For more information about the [!DNL Servers Manager] interface, see the * [!DNL Insight] User Guide*.

