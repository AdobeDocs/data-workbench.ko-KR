---
description: 사용자 정의 인증서 사용 지침
title: 데이터 워크벤치에서 사용자 지정 인증서 사용
uuid: c3a2db27-bdb2-44b3-95dd-65eedd05c957
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# 데이터 워크벤치에서 사용자 지정 인증서 사용{#using-custom-certificates-in-data-workbench}

사용자 정의 인증서 사용 지침

Data Workbench 클라이언트 또는 서버에서 사용하는 인증서는 신뢰할 수 있는 CA(인증 기관)에서 서명해야 합니다. Data Workbench 고객은 Visual Sciences CA에서 서명한 인증서를 받습니다. 이러한 인증서는 Visual Sciences CA에 대한 루트 CA 인증서를 [!DNL trust_ca_cert.pem] 포함하므로 Data Workbench **** 소프트웨어는 Insight 소프트웨어와 함께 제공되며 *서버 및 클라이언트의 인증서* 디렉토리에 보관됩니다. 이러한 인증서는 클라이언트와 서버가 SSL을 사용하여 통신할 때 소프트웨어 라이센스와 인증 모두에 사용됩니다. Visual Sciences CA에서 발행한 인증서만 라이센스에 사용할 수 있지만 다른 인증서는 통신 및 인증에 사용할 수 있습니다. Visual Sciences 이외의 CA에서 발행한 인증서는 *사용자 정의 인증이라고 합니다.*

**중요 정보:** 서버 및 클라이언트의 경우 Data Workbench 소프트웨어는 클라이언트 또는 서버의 인증서 **디렉토리에** 설치된 인증서 파일이나 구성에 명시적으로 식별된 인증서를 사용합니다. 그러나 클라이언트용 Windows 인증서 [저장소를 사용할](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/crypto-api.md#concept-4acb13b7de9340ea8cde8ad84b93358d) 수도 있습니다.

다음 지침은 Data Workbench 클라이언트와 서버 간의 통신에 사용자 정의 인증서를 사용하기 위해 수행되는 절차를 설명합니다. 모든 세부 사항이 까다로운 것은 아니며 그 과정에서 다양한 변형을 적용할 수 있습니다. 그러나 아래 절차는 제대로 수행되도록 테스트되었습니다.

## 사용자 지정 클라이언트 인증서 설정 {#section-2083fd41973e451fa404e7a4ae4da591}

1. 이 사용자 정의 인증서를 사용하여 액세스할 모든 클러스터의 인증서 [!DNL trust_cert_ca.pem]디렉토리에 설치되는 **** 발급 CA의 인증서를 에 추가합니다.

1. 클러스터의 각 서버에 대한 사용자 정의 인증서를 얻습니다.

   1. 인증서는 [!DNL .pem] 인증서로 형식이 지정됩니다.
   1. 인증서는 키를 포함하며 암호화되지 않습니다(즉, 암호/암호 구문 없음).

      인증서에는 다음 줄 중 하나가 있는 키가 들어 있습니다.

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      인증서에서 암호 구문을 제거하는 한 가지 방법: [!DNL .pem]

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. 인증서에 CN, O, OU 등이 있습니다. 에 있는 값. [!DNL Access Control.cfg]
   1. 인증서가 *클라이언트의* *목적 **** 또는 두 가지 *클라이언트* 서버 **및 Safety** Client *와 함께*&#x200B;발급되었습니다.

      인증서에 서버 및/또는 클라이언트의 목적 코드가 있는지 확인하려면 다음 명령을 사용할 수 있습니다.

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      서버 인증서의 경우 두 명령 모두 다음을 수행해야 합니다.

      ```
      custom_communications_cert.pem: OK
      ```

      클라이언트 인증서의 경우 두 번째 명령만 전달해야 [!DNL OK]합니다.

1. 클라이언트의 인증서 **디렉토리에 인증서를** 배치합니다.
1. 이 인증서를 [!DNL Insight.cfg] 사용할 각 클러스터의 *serverInfo 아래에서* 사용자 지정 클라이언트 인증서의 ** 이름을 다음과 같이 지정하십시오.

   ```
   Servers = vector: 1 items 
     0 = serverInfo: 
       SSL Client Certificate = string:
   <my_custom_client_cert.pem>
   ```

## 사용자 정의 서버 인증서 설정 {#setting-up-custom-server-certificates}

이 섹션에서는 Visual Sciences에서 발행한 인증서를 사용하여 실행 중인 클러스터가 있고, 이 구성은 일반적인 방법(예: 마스터의 처리 *서버용 구성* 요소 디렉토리가 모든 DPU의 구성 요소 *디렉토리에 동기화됨* )을따릅니다.

1. 클러스터의 모든 서버 및 이 클러스터와 통신해야 하는 모든 클라이언트에 [!DNL trust_cert_ca.pem] 설치된 발급 CA의 인증서를 추가합니다.
1. 클러스터의 각 서버에 대한 사용자 정의 인증서를 얻습니다.

   1. 사용자 정의 인증서는 [!DNL .pem] 인증서로 형식이 지정됩니다.
   1. 인증서는 키를 포함하며 암호화되지 않습니다(즉, 암호/암호 구문 없음).

      다음과 같은 라인이 있는 경우 인증서에 키가 포함됩니다.

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      인증서에서 암호 구문을 제거하는 한 가지 방법: [!DNL .pem]

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. 인증서는 [!DNL server_cert.pem] 현재 서버에 설치된 CN과 동일합니다.
   1. 인증서가 *서버* 및 *클라이언트*&#x200B;용도로 발급되었습니다.

      인증서에 서버 및/또는 클라이언트의 목적 코드가 있는지 확인하려면 다음 명령을 사용할 수 있습니다.

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      서버 인증서의 경우 두 명령 모두 다음을 수행해야 합니다.

      ```
      custom_communications_cert.pem: OK
      ```

      클라이언트 인증서의 경우 두 번째 명령만 전달해야 [!DNL OK]합니다.

1. 각 서버의 사용자 정의 인증서를 서버의 인증서 **디렉토리에** 로 [!DNL custom_communications_cert.pem]설치합니다.

1. 텍스트 편집기를 사용하여 처리 서버용 구성 요소 **및 구성** 요소 *디렉토리에* 있는 Communications.cfg *파일에 첫 번째 줄(*[!DNL component = CommServer]) 바로 아래에 다음 줄을 추가합니다.

   ```
   Certificate = string: Certificates\\custom_communications_cert.pem
   ```

1. 모든 서버를 다시 시작합니다.

**인증서 실패 경고 정보**

Insight 서버 또는 클라이언트가 인증서 **디렉토리에서** 라이센스 **인증서를 찾는** 경우 [!DNL trust_ca_cert.pem]Insight CA 인증서의 하드 코딩된 복사본에 대해 모든 인증서(제외)의 유효성을 검사하려고 합니다. 이 사본은 디렉토리에 있는 사용자 정의 인증서에 대해 실패합니다. 서버에서 다음 경고를 표시합니다.

```
Certificate failed to verify. Error 20 at 0 depth. Desc: unable to get local issuer certificate. Cert details:
```

이 경고는 안전하게 무시될 수 있습니다.
