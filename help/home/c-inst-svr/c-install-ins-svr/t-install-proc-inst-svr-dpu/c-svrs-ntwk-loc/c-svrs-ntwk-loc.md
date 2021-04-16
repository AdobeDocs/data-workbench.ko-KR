---
description: Insight Server의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight 서버를 참조합니다.
title: 서버의 네트워크 위치 정의
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
exl-id: def360b8-f146-45ca-ae61-fd213adef68b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 4%

---

# 서버의 네트워크 위치 정의{#defining-the-server-s-network-location}

Insight Server의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight 서버를 참조합니다.

예를 들어 [!DNL Insight] 또는 [!DNL Report]을 [!DNL Insight Server]에 연결하는 경우, 공통 이름(예: [!DNL Server.MyCompany.com])으로 서버를 식별합니다. 내부적으로 클라이언트는 서버에 요청을 보내기 전에 일반적인 이름을 숫자 IP 주소로 해결합니다.

IP 주소로 일반 이름을 확인하려면 [!DNL Insight Server’s] 클라이언트는 주소 파일이라는 로컬 조회 파일을 사용합니다. 주소 파일은 조직에 설치된 [!DNL Insight Servers]의 공통 이름을 나열하고 해당 숫자 IP 주소를 식별합니다. 클라이언트는 [!DNL Insight Server]에서 프로파일을 열면 자동으로 주소 파일 사본을 수신합니다.

클라이언트가 [!DNL Insight Server]에 대한 요청을 실행하면 주소 파일을 통해 서버의 일반 이름을 확인하려고 시도합니다. 주소 파일이 요청된 서버의 IP 주소를 식별하면 클라이언트는 지정된 주소로 요청을 라우팅합니다. 주소가 정의되지 않은 경우(예: 주소 파일이 서버의 공통 이름을 정의하지 않음) 요청이 실패합니다. 필요에 따라 클라이언트의 주소 파일에 이름이 정의되지 않은 경우 운영 환경의 일반 DNS(Domain Naming Service) 메커니즘을 통해 주소를 확인하도록 클라이언트를 구성할 수 있습니다. 지침은 다음 섹션의 [NetworkLocation 매개 변수 표](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05)에 있는 상위 매개 변수를 참조하십시오.
