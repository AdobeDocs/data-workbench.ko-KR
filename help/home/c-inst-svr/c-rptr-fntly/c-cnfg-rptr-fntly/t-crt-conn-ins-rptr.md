---
description: 네트워크 방화벽이 Insight Machine에서 반복 서버에 대한 액세스를 차단하지 않는 경우 Insight를 사용하여 반복 서버를 관리할 수 있도록 반복 서버와 Insight 간에 연결을 만들 수 있습니다.
title: Insight와 반복 간의 연결 만들기
uuid: dccce83a-8708-4763-a19a-64d905a9f624
exl-id: 81e81db5-0517-41d4-a958-d08cd3975096
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 4%

---

# Insight와 반복 간의 연결 만들기{#creating-a-connection-between-insight-and-repeater}

{{eol}}

네트워크 방화벽이 Insight Machine에서 반복 서버에 대한 액세스를 차단하지 않는 경우 Insight를 사용하여 반복 서버를 관리할 수 있도록 반복 서버와 Insight 간에 연결을 만들 수 있습니다.

**다음 사이에 연결을 만들려면 [!DNL Insight] 그리고 중계기 서버**

1. in [!DNL Insight], [!DNL Admin] 탭에서 **[!UICONTROL Configure Connections to Servers]** 축소판을 사용하여 서버에 연결 구성 작업 공간을 엽니다.
1. 에서 [!DNL Insight.cfg] 창, 마우스 오른쪽 단추 클릭 **[!UICONTROL Servers]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Server]**.
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
   <td colname="col2">(선택 사항) 원하는 이름입니다 <span class="keyword"> 인사이트</span> 를 사용하여 사용자 인터페이스에서 반복 서버를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> <p>반복 서버의 호스트 이름 또는 숫자 IP 주소입니다. </p> <p>예: <span class="filepath"> Repeater.mycompany.com</span> 또는 192.168.1.90 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 클라이언트 인증서 </td> 
   <td colname="col2"> <p>두 개 이상의 인증서가 있는 한 선택 사항입니다. 이 복사본 디지털 인증서가 포함된 파일의 이름입니다. <span class="keyword"> 인사이트</span>. (설치하는 동안 다운로드한 파일입니다 <span class="keyword"> 인사이트</span>) </p> <p>예: <span class="filepath"> 사만다 스미스.pem</span></p> <p>이 매개 변수를 비워 두면 <span class="keyword"> 인사이트</span> 은 존재하는 모든 인증서를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL 서버 </p> <p>일반 이름 </p> </td> 
   <td colname="col2">반복 서버에 할당된 공통 이름입니다. 이 이름은 라이선스 인증서 내에서 반복 서버에 할당된 공통 이름과 일치해야 합니다. 중계기의 인증서 파일(<span class="filepath"> Certificates\server_cert.pem</span>)를 입력하면 메모장과 같은 텍스트 편집기로 파일을 열어 일반 이름을 찾을 수 있습니다. 공통 이름은 인증서의 CN 필드에서 식별됩니다. </td> 
  </tr> 
 </tbody> 
</table>

1. 마우스 오른쪽 단추를 클릭하여 파일을 저장합니다 **[!UICONTROL (modified)]** 창 상단에서 **[!UICONTROL Save]**. [!DNL Insight] 지정한 설정을 사용하여 반복 서버에 연결을 시도합니다. 연결이 설정되어 있으면 녹색 서버 아이콘이 [!DNL Servers Manager] 인터페이스. 연결을 설정할 수 없으면 빨간색 아이콘이 나타납니다.

   에 대한 자세한 정보 [!DNL Servers Manager] 인터페이스, * [!DNL Insight] 사용 안내서*.
