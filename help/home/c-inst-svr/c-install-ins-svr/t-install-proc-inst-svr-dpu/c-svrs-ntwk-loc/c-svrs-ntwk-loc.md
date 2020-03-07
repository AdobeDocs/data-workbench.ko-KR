---
description: Insight Server의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight 서버를 참조합니다.
solution: Insight
title: 서버의 네트워크 위치 정의
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 서버의 네트워크 위치 정의{#defining-the-server-s-network-location}

Insight Server의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight 서버를 참조합니다.

예를 들어, 서버에 연결하거나 연결할 [!DNL Insight] 때 서버를 공통 이름(예: [!DNL Report] [!DNL Insight Server][!DNL Server.MyCompany.com])으로 식별합니다. 내부적으로 클라이언트는 일반적인 이름을 숫자 IP 주소로 확인한 후 서버에 요청을 보냅니다.

IP 주소에 대한 일반적인 이름을 해결하려면 [!DNL Insight Server’s] 클라이언트가 주소 파일이라는 로컬 조회 파일을 사용합니다. 주소 파일에는 조직에 [!DNL Insight Servers] 설치되어 있는 공통 이름이 나열되며 숫자 IP 주소를 식별합니다. 클라이언트는 에서 프로파일을 열면 자동으로 주소 파일 사본을 수신합니다 [!DNL Insight Server].

클라이언트가 서버에 요청을 [!DNL Insight Server]발행할 때 주소 파일을 통해 서버의 일반 이름을 확인하려고 합니다. 주소 파일이 요청된 서버의 IP 주소를 식별하는 경우 클라이언트는 지정된 주소로 요청을 라우팅합니다. 주소가 정의되지 않은 경우(예: 주소 파일이 서버의 공통 이름을 정의하지 않음) 요청이 실패합니다. 선택적으로, 클라이언트의 주소 파일에 이름이 정의되지 않은 경우 운영 환경의 일반 DNS(Domain Naming Service) 메커니즘을 통해 주소를 확인하도록 클라이언트를 구성할 수 있습니다. 지침은 다음 섹션의 NetworkLocation 매개 변수 [테이블의](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05) Parent 매개 변수를 참조하십시오.
