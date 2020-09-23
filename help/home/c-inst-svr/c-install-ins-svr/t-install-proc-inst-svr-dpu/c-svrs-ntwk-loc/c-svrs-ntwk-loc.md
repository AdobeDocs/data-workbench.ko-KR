---
description: Insight 서버의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight 서버를 참조합니다.
solution: Analytics
title: 서버의 네트워크 위치 정의
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 4%

---


# 서버의 네트워크 위치 정의{#defining-the-server-s-network-location}

Insight 서버의 클라이언트(보고서 및 인사이트)는 공통 이름을 사용하여 Insight 서버를 참조합니다.

예를 들어, 연결 [!DNL Insight] 을 하거나 [!DNL Report] 에 연결할 [!DNL Insight Server]때 일반 이름(예: [!DNL Server.MyCompany.com])으로 서버를 식별합니다. 내부적으로 클라이언트는 서버에 요청을 보내기 전에 공통 이름을 숫자 IP 주소로 확인합니다.

IP 주소로 일반 이름을 확인하려면 [!DNL Insight Server’s] 클라이언트가 주소 파일이라는 로컬 조회 파일을 사용합니다. 주소 파일은 조직에 설치되어 있는 일반적인 이름 [!DNL Insight Servers] 을 나열하고 숫자 IP 주소를 식별합니다. 클라이언트는 주소 파일의 복사본을 자동으로 수신합니다. 이때 주소 파일의 프로필이 에서 열립니다 [!DNL Insight Server].

클라이언트가 클라이언트에 대한 요청을 [!DNL Insight Server]실행하면 주소 파일을 통해 서버의 일반 이름을 확인하려고 시도합니다. 주소 파일이 요청한 서버의 IP 주소를 식별하는 경우 클라이언트는 요청을 지정된 주소로 라우팅합니다. 주소가 정의되지 않은 경우(예: 주소 파일이 서버의 공통 이름을 정의하지 않음) 요청이 실패합니다. 필요에 따라 클라이언트의 주소 파일에 이름이 정의되지 않은 경우 운영 환경의 일반 DNS(Domain Naming Service) 메커니즘을 통해 주소를 확인하도록 클라이언트를 구성할 수 있습니다. 자세한 내용은 다음 섹션의 NetworkLocation 매개 변수 표 [에](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05) 있는 Parent 매개 변수를 참조하십시오.
