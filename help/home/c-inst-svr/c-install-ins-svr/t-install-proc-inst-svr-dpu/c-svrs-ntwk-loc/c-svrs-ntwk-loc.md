---
description: Insight Server의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight Server를 나타냅니다.
title: 서버의 네트워크 위치 정의
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
exl-id: def360b8-f146-45ca-ae61-fd213adef68b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 4%

---

# 서버의 네트워크 위치 정의{#defining-the-server-s-network-location}

{{eol}}

Insight Server의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight Server를 나타냅니다.

예를 들어 연결할 때 [!DNL Insight] 또는 [!DNL Report] 변환 후 [!DNL Insight Server]를 입력하면 서버가 일반 이름(예: [!DNL Server.MyCompany.com]). 내부적으로 클라이언트가 서버에서 요청을 보내기 전에 공통 이름을 숫자 IP 주소로 확인합니다.

공통 이름을 IP 주소로 확인하려면, [!DNL Insight Server’s] 클라이언트는 주소 파일이라는 로컬 조회 파일을 사용합니다. 주소 파일에는 [!DNL Insight Servers] 가 조직에 설치되어 있고 해당 숫자 IP 주소를 식별합니다. 클라이언트에서 프로파일을 열 때 자동으로 주소 파일의 사본을 수신함 [!DNL Insight Server].

클라이언트가 [!DNL Insight Server]로 설정되면 주소 파일을 통해 서버의 일반 이름을 확인합니다. 주소 파일이 요청된 서버의 IP 주소를 식별하면 클라이언트가 요청을 지정된 주소로 라우팅합니다. 주소가 정의되지 않은 경우(예: 주소 파일에서 서버의 일반 이름을 정의하지 않음) 요청이 실패합니다. 선택적으로 클라이언트의 주소 파일에 이름이 정의되지 않은 경우 운영 환경의 일반 DNS(Domain Naming Service) 메커니즘을 통해 주소를 확인하도록 클라이언트를 구성할 수 있습니다. 자세한 내용은 [NetworkLocation 매개 변수 테이블](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05) 을 참조하십시오.
