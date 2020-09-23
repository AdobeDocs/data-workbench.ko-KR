---
description: 디지털 인증서에 대한 일반 정보 및 다운로드 및 설치 절차.
solution: Analytics
title: 디지털 인증서 다운로드 및 설치
uuid: ac484e96-21dc-4643-ae74-01ac957e30ee
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 3%

---


# 디지털 인증서 다운로드 및 설치{#downloading-and-installing-the-digital-certificates}

디지털 인증서에 대한 일반 정보 및 다운로드 및 설치 절차.

* [디지털 인증서 이해](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-e48a776ef39042759d1dfb3444996d8b)
* [노드 잠금 인증서](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-b3dc7dcf2aa3439cbe66b0461b42d485)
* [현재 인증서](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-15aabaa8625c46edaa7436e1f3fc29c5)
* [인터넷에 액세스할 수 없는 시스템에서 디지털 인증서 사용](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-809366329a7d4e198f95fe06c1f534fa)
* [디지털 인증서 설치 절차](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-19f31676aad344a98e26e4fca1fad03b)

## 디지털 인증서 이해 {#section-e48a776ef39042759d1dfb3444996d8b}

Adobe은 X.509 디지털 인증서를 사용하여 구현을 구성하는 클라이언트 및 서버 구성 요소를 식별하고 인증합니다.

서버 구성 요소( [!DNL Insight Server] 또는 [!DNL Repeater])를 설치할 때 구성 요소에 대해 Adobe이 발급한 디지털 인증서를 설치해야 합니다. Adobe 응용 프로그램을 다른 컴퓨터로 마이그레이션해야 하는 경우 Adobe에서 새 인증서를 받아야 합니다. 이렇게 하려면 Adobe 고객 지원 센터에 문의하십시오.

이 인증서에 나타나는 일반 이름은 지정된 도메인 이름(예: [!DNL vs001a.mycompany.com])으로 서버를 식별합니다. 서버 클라이언트가 이 서버에 연결되면 서버는 클라이언트가 요청한 서버임을 증명하는 증표로 이 인증서를 표시합니다.

마찬가지로 서버 클라이언트(예: [!DNL Insight] 또는 [!DNL Report])를 설치할 때 설치된 클라이언트 응용 프로그램을 사용하려면 이름이 지정된 개인(예: Jane Smith)을 인증하는 디지털 인증서를 설치해야 합니다. Adobe 응용 프로그램을 다른 컴퓨터 또는 다른 명명된 사용자로 마이그레이션해야 하는 경우 Adobe에서 새 인증서를 받아야 합니다. 이렇게 하려면 Adobe 고객 지원 센터에 문의하십시오.

클라이언트 응용 프로그램은 서버 구성 요소에 액세스할 수 있도록 이 디지털 인증서를 제공합니다. 서버 구성 요소의 관리자는 클라이언트 인증서에 표시되는 일반 이름 또는 조직 단위 값을 기준으로 서버 리소스에 대한 액세스를 제한할 수 있습니다.

Adobe 응용 프로그램과 함께 설치되는 X.509 디지털 인증서에서도 클라이언트 및 서버 구성 요소가 SSL(Secure Sockets Layer)을 통해 정보를 교환할 수 있습니다. SSL은 공개 및 개인 키 암호화 시스템을 사용하여 HTTP를 통해 전송을 보호합니다. Adobe의 SSL 구현은 1024비트 RSA 키를 지원하며 128비트 RC4 암호화 알고리즘을 사용합니다.

보안 이외에도 설치한 디지털 인증서는 설치된 Adobe 소프트웨어를 실행할 수 있는 라이센스 키로도 작동합니다. 디지털 인증서가 제대로 작동하려면 노드가 잠겼고 최신 상태여야 합니다. 그렇지 않으면 응용 프로그램이 시작되지 않습니다.

## 문자열 암호화 {#section-8abe6b2d95704d38a04137d5c4602f0b}

암호 [를](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/string-encryption.md#concept-35da0b53650a4d7e82b240ad27f6d45a) 암호화하려면 문자열 암호화를 참조하십시오.

## 노드 잠금 인증서 {#section-b3dc7dcf2aa3439cbe66b0461b42d485}

노드 잠금 인증서는 컴퓨터가 설치된 컴퓨터에 등록된 디지털 인증서입니다. 노드 잠금은 특정 노드 식별자(특정 컴퓨터를 고유하게 식별하는 값)와 인증서를 영구적으로 연결합니다. 인증서를 노드에 잠그려면 Adobe 라이센스 서버 또는 라이센스 서버에 대한 액세스 권한이 있는 프록시 서버에 대한 인터넷 액세스 권한이 있어야 합니다.

인터넷에 액세스할 수 없는 시스템에 설치하는 경우, 인터넷 액세스 [없는 시스템에서 디지털 인증서](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-809366329a7d4e198f95fe06c1f534fa)사용에 설명된 대로 미리 잠긴 특수 인증서를 가져와 설치해야 합니다.

인터넷에 액세스할 수 있는 시스템에 설치하는 경우 Adobe 제품을 처음 시작할 때 디지털 인증서가 자동으로 노드 잠깁니다. 노드를 잠근 후에는 다른 컴퓨터에서 인증서를 사용할 수 없습니다. Adobe 제품을 다른 컴퓨터로 마이그레이션해야 하는 경우 Adobe에서 잠금 해제된 새 인증서를 받아야 합니다.

## 현재 인증서 {#section-15aabaa8625c46edaa7436e1f3fc29c5}

노드가 잠겼을 뿐만 아니라 디지털 인증서가 최신 상태여야 합니다. 최신 상태를 유지하려면, 인증서의 유효성을 정기적으로 재검사해야 합니다(일반적으로 30일마다 확인되지만, Adobe와의 계약에 따라 달라질 수 있음). 컴퓨터에 인터넷에 액세스할 수 있는 경우 재인증 프로세스는 완전히 투명합니다. Adobe 제품은 라이센스 서버에 자동으로 연결되고 필요한 경우 인증서의 유효성을 다시 확인합니다. 컴퓨터에 인터넷에 액세스할 수 없는 경우 다음 섹션에 설명된 대로 업데이트된 인증서를 수동으로 설치해야 합니다.

## 인터넷에 액세스할 수 없는 시스템에서 디지털 인증서 사용 {#section-809366329a7d4e198f95fe06c1f534fa}

인터넷에 액세스할 수 없는 시스템에 설치하는 경우, 사전 잠김 인증서를 요청하여 설치를 완료해야 합니다 [!DNL Insight Server]. 사전 잠근 인증서는 Adobe이 컴퓨터의 노드 식별자에 수동으로 잠그는 디지털 인증서입니다.

사전 잠긴 인증서를 요청하려면 노드 식별자 및 인증서 번호를 Adobe 고객 지원 센터로 보내야 합니다. 시스템의 노드 식별자를 얻으려면 Adobe 고객 지원 센터에 문의하여 Adobe 노드 식별자 유틸리티를 요청하십시오. 또한 Adobe 소프트웨어가 라이센스 서버에 연결하려고 할 때 문제가 발생하여 연결할 수 없다는 경고에서 노드 식별자를 받을 수도 있습니다.

사전 잠김 인증서를 받으면 [디지털 인증서 설치 절차의 마지막 두 단계에 설명된 대로 설치합니다](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-19f31676aad344a98e26e4fca1fad03b). 인증서의 유효성을 다시 검사해야 하는 경우 사용권 서버에서 유효성이 확인된 새 인증서를 다운로드하여 시스템에 다시 설치해야 합니다.

## 디지털 인증서 설치 절차 {#section-19f31676aad344a98e26e4fca1fad03b}

**디지털 인증서를 다운로드하여 설치하려면**

1. https://aap.adobe.com으로 웹 브라우저를 [엽니다](https://aap.adobe.com).

   >[!NOTE]
   >
   >이때 브라우저가 디지털 인증서를 제시하라는 메시지를 표시할 수 있습니다. 이 경우 을 클릭하여 대화 상자 **[!UICONTROL Cancel]** 를 닫습니다.

1. 로그인 화면에서 Adobe에서 받은 **[!UICONTROL Account Name]** 및 **[!UICONTROL Password]** 을 입력한 다음 을 클릭합니다 **[!UICONTROL login]**.

1. 사용자에 대해 발급된 인증서를 찾은 [!DNL Insight Server]다음 해당 인증서와 관련된 아이콘을 클릭합니다.

   >[!NOTE]
   >
   >이 인증서에 할당된 공통 이름을 메모하십시오. 이 이름은 이후 단계에서 사용합니다.

1. 인증서를 저장하라는 메시지가 표시되면 을 클릭합니다 **[!UICONTROL Save]**. 파일 이름은 인증서와 연관된 공통 이름과 일치한다는 점을 참고하십시오.
1. 파일을 설치한 디렉토리의 [!DNL Certificates] 폴더에 다운로드합니다 [!DNL Insight Server]. 이 폴더에는 이름이 지정된 인증서 파일이 이미 있습니다 [!DNL trust_ca_cert.pem]. 이 인증서 파일은 항상 있어야 합니다.

1. 다운로드한 인증서 파일의 이름 변경:

[!DNL server_cert.pem]

