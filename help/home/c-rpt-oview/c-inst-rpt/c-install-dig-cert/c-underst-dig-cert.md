---
description: Adobe은 X.509 디지털 인증서를 사용하여 구현을 구성하는 클라이언트 및 서버 구성 요소를 식별하고 인증합니다.
title: 디지털 인증서 이해
uuid: a2d84e9a-16aa-4973-85da-303614a4ad7f
exl-id: 967e9d5b-7972-497e-8902-8db0eb304f27
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 54%

---

# 디지털 인증서 이해{#understanding-digital-certificates}

Adobe은 X.509 디지털 인증서를 사용하여 구현을 구성하는 클라이언트 및 서버 구성 요소를 식별하고 인증합니다.

[!DNL Report Server]을 설치할 때 설치된 클라이언트 응용 프로그램을 사용하려면 이름이 지정된 개인(예: Jane Smith)을 인증하는 디지털 인증서를 설치해야 합니다.

>[!NOTE]
>
>[!DNL Report Server]을 다른 컴퓨터 또는 다른 명명된 사용자로 마이그레이션해야 하는 경우 Adobe에서 새 인증서를 받아야 합니다. 이 작업을 수행하려면 Adobe 고객 지원 센터에 문의하십시오.

[!DNL Report Server] 서버 구성 요소에 액세스할 수 있도록 이 디지털 인증서를 제공합니다. 서버 구성 요소의 관리자는 클라이언트 인증서에 표시되는 일반 이름 또는 조직 단위 값을 기준으로 서버 리소스에 대한 액세스를 제한할 수 있습니다.

Adobe 애플리케이션과 함께 설치되는 X.509 디지털 인증서에서도 클라이언트 및 서버 구성 요소가 SSL(Secure Sockets Layer)을 통해 정보를 교환할 수 있습니다. SSL은 공개 및 개인 키 암호화 시스템을 사용하여 HTTP를 통해 전송을 보호합니다. Adobe의 SSL 구현은 1024비트 RSA 키를 지원하며 128비트 RC4 암호화 알고리즘을 사용합니다.

보안 이외에도 설치한 디지털 인증서는 설치된 [!DNL Report Server]을 실행할 수 있는 라이센스 키로도 작동합니다. 디지털 인증서가 제대로 작동하려면 노드가 잠기고 최신 상태여야 합니다. 그렇지 않으면 응용 프로그램이 시작되지 않습니다.

## 노드 잠금 인증서 {#section-3338f1558e7844888dced8f395888744}

노드 잠금 인증서는 컴퓨터가 설치된 컴퓨터에 등록된 디지털 인증서입니다. 노드 잠금은 특정 노드 식별자(특정 컴퓨터를 고유하게 식별하는 값)와 인증서를 영구적으로 연결합니다. 인증서를 노드에 잠그려면 Adobe 라이선스 서버 또는 라이선스 서버에 대한 액세스 권한이 있는 프록시 서버에 대한 인터넷 액세스 권한이 있어야 합니다.

인터넷에 액세스할 수 없는 시스템에 설치하는 경우, 이 페이지에서 [인터넷에 액세스할 수 없는 시스템에서 디지털 인증서 사용](../../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/c-underst-dig-cert.md#section-18cce05e2204407bb2b6b75deab9197d)에 설명된 대로 미리 잠금 특수 인증서를 가져와 설치해야 합니다.

인터넷에 액세스할 수 있는 시스템에 설치하는 경우, [!DNL Report Server]을 처음 시작할 때 디지털 인증서가 자동으로 노드 잠깁니다. 노드를 잠근 후에는 다른 컴퓨터에서 인증서를 사용할 수 없습니다. [!DNL Report Server]을 다른 컴퓨터로 마이그레이션해야 하는 경우 Adobe에서 잠금이 해제된 새 인증서를 받아야 합니다.

## 현재 인증서 {#section-b4053ab714514dfb97ea7f61bbb8da1e}

노드가 잠겼을 뿐만 아니라 디지털 인증서가 최신 상태여야 합니다. 최신 상태를 유지하려면, 인증서의 유효성을 정기적으로 재검사해야 합니다(일반적으로 30일마다 확인되지만, Adobe와의 계약에 따라 달라질 수 있음). 컴퓨터에 인터넷에 액세스할 수 있는 경우 재인증 프로세스는 완전히 투명합니다. [!DNL Report Server] 라이센스 서버에 자동으로 연결하고 필요한 경우 인증서의 유효성을 다시 확인합니다. 컴퓨터에 인터넷에 액세스할 수 없는 경우 다음 섹션에 설명된 대로 업데이트된 인증서를 수동으로 설치해야 합니다.

## 인터넷에 액세스할 수 없는 시스템에서 디지털 인증서 사용 {#section-18cce05e2204407bb2b6b75deab9197d}

인터넷에 액세스할 수 없는 시스템에 설치하는 경우, 미리 잠금 인증서를 요청하여 설치를 완료해야 합니다 [!DNL Report Server]. 미리 잠금 인증서는 Adobe이 컴퓨터의 노드 식별자에 수동으로 잠그는 디지털 인증서입니다.

미리 잠금 인증서를 요청하려면 노드 식별자 및 인증서 번호를 Adobe 고객 지원 센터로 보내야 합니다. 시스템의 노드 식별자를 얻으려면 Adobe 고객 지원 센터에 문의하여 Adobe [!DNL Node Identifier] 유틸리티를 요청하십시오. 또한 [!DNL Report Server]이 라이센스 서버에 연결하려고 할 때 문제가 발생하여 연결할 수 없다는 경고에서 노드 식별자를 확인할 수도 있습니다. 미리 잠금 인증서를 받으면 [디지털 인증서 설치 절차](../../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/t-dig-cert-install-proc.md#task-5c4bb352ff534b40adc46dd053874e5d)의 마지막 두 단계에 설명된 대로 설치합니다.

인증서의 유효성을 다시 검사해야 하는 경우 라이센스 서버에서 유효성이 확인된 새 인증서를 다운로드하여 시스템에 다시 설치해야 합니다(Adobe 상태와의 계약이 따로 있지 않음).
