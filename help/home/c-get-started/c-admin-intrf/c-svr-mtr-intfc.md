---
description: 서버 모니터 인터페이스는 Data Workbench 서버 컴퓨터의 클라이언트인 Data Workbench 서버 컴퓨터 및 보고서 컴퓨터의 성능 매개 변수를 문제 해결하거나 간단히 추적하는 데 유용합니다.
title: 서버 모니터 인터페이스
uuid: 609dd8ea-31a9-44c1-ab75-ca783ec85650
exl-id: fb8baae9-ac1e-4355-ba38-fef6621e22bb
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 2%

---

# 서버 모니터 인터페이스{#server-monitor-interface}

서버 모니터 인터페이스는 Data Workbench 서버 컴퓨터의 클라이언트인 Data Workbench 서버 컴퓨터 및 보고서 컴퓨터의 성능 매개 변수를 문제 해결하거나 간단히 추적하는 데 유용합니다.

서버 모니터 인터페이스에서는 컴퓨터 이름의 왼쪽에 녹색 점 또는 빨간색 점이 표시됩니다. 녹색 점은 컴퓨터가 문제 없이 작동하고 있음을 나타냅니다. 빨간색 점은 컴퓨터에서 하나 이상의 오류가 발생했음을 나타냅니다.

서버 모니터 인터페이스 하단에는 사용 가능한 각 프로필의 처리 상태와 컴퓨터에 대한 성능 세부 정보가 표시됩니다.

[!DNL Data Workbench servers]에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서*&#x200B;를 참조하십시오. [!DNL Report]에 대한 자세한 내용은 *Data Workbench 보고서 안내서*&#x200B;를 참조하십시오.

**서버 모니터 인터페이스를 열려면**

* 서버 관리자에서 Data Workbench 서버의 노드 또는 [!DNL Report] 컴퓨터를 마우스 오른쪽 단추로 클릭합니다. t

한 서버에 대한 세부 정보를 보려면 **[!UICONTROL Server Monitor]** 을 클릭하고, 관련 서버 클러스터에 대한 세부 정보를 보려면 **[!UICONTROL Related Servers]** > **[!UICONTROL Server Monitor List]** 를 클릭하십시오.

![](assets/vis_ServerMonitor.png)

[!DNL Server Monitor]인터페이스는 10초마다 자동으로 업데이트됩니다.

다음 표에는 [!DNL Server Monitor] 인터페이스를 사용하여 완료할 수 있는 작업이 나열되어 있습니다.

<table id="table_A65426669ADE44B5A6BAD9D4E99A5CAC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>프로필의 로그 처리 상태를 확인하려면 </p> </td> 
   <td colname="col2"> <p>프로필 <i>프로필</i> 이름 벡터를 봅니다. 위의 예에서는 Profile ExampleProfile 벡터를 보고 한 서버에서 ExampleProfile 프로필 프로세스가 완료되고 로그 처리가 100% 완료되었음을 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컴퓨터가 요청에 응답하는 데 걸리는 시간을 확인하려면 </p> </td> 
   <td colname="col2"> <p>폴링 지연 필드를 봅니다. 이 값이 1000ms 이상인 경우 Adobe 지원 서비스에 문의하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>변환 또는 쿼리를 완료하는 데 걸리는 시간에 대한 추정치를 보려면 </p> </td> 
   <td colname="col2"> <p>변환하거나 쿼리하는 동안에만 표시되는 청소 시간(hh:mm:ss) 필드를 봅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컴퓨터에 대한 현재 네트워크 연결 수를 확인하려면 </p> </td> 
   <td colname="col2"> <p>컴퓨터의 <span class="wintitle"> 서버 모니터</span> 정보의 마지막 줄을 봅니다. 위의 예에서는 현재 한 컴퓨터에서 2개의 네트워크 연결이 오고 있는 것을 볼 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
