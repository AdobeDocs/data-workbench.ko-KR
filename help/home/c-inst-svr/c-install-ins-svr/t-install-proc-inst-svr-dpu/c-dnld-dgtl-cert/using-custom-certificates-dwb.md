---
description: 사용자 정의 인증서 사용 지침.
title: Data Workbench에서 사용자 정의 인증서 사용
uuid: c3a2db27-bdb2-44b3-95dd-65eedd05c957
exl-id: f813d599-723f-4b5d-a0b5-f4d71c1b1a22
translation-type: ht
source-git-commit: 233b04c65a45d3f92b8670bc244b907dc198b51d
workflow-type: ht
source-wordcount: '732'
ht-degree: 100%

---

# Data Workbench에서 사용자 정의 인증서 사용{#using-custom-certificates-in-data-workbench}

사용자 정의 인증서 사용 지침.

Data Workbench 클라이언트와 서버 중 하나에서 사용하는 인증서는 신뢰할 수 있는 CA(인증 당국)가 서명해야 합니다. Data Workbench 고객에게 Visual Sciences CA가 서명한 인증서가 발급됩니다. [!DNL trust_ca_cert.pem] (Insight 소프트웨어와 함께 제공되고 서버와 클라이언트의 **Certificates** 디렉터리에 저장됨)에는 Visual Sciences CA의 *루트 CA 인증서* 가 포함되어 있기 때문에 Data Workbench 소프트웨어는 이 인증서를 신뢰할 수 있습니다. 클라이언트와 서버가 SSL을 사용하여 상호 통신하는 경우 이 인증서는 소프트웨어와 인증에 라이선스를 부여하는 데 사용됩니다. 라이선싱에서는 Visual Sciences CA에서 발급한 인증서만을 사용할 수 있지만 통신 및 인증에 있어서는 다른 인증서를 사용할 수 있습니다. Visual Sciences이외의 CA에서 발급한 인증서는 *사용자 정의 인증서*&#x200B;라고 합니다.

**중요 정보:** 서버와 클라이언트의 경우 Data Workbench 소프트웨어는 클라이언트이나 서버의 **인증서** 디렉터리에 설치된 인증서 파일 또는 해당 구성에 명시된 인증서를 사용합니다. 단, 클라이언트의 [Windows Certificate Store](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/crypto-api.md#concept-4acb13b7de9340ea8cde8ad84b93358d) 를 사용할 수도 있습니다.

Data Workbench 클라이언트와 서버 간 통신하는 경우 아래 지침의 절차에 따라 사용자 정의 인증서를 사용할 수 있습니다. 세부 정보에 대한 요구 사항이 까다롭지 않으며, 프로세스에서 다양한 변형을 사용할 수 있습니다. 단, 아래 절차를 작업에 맞게 테스트했습니다.

## 사용자 정의 클라이언트 인증서 설정 {#section-2083fd41973e451fa404e7a4ae4da591}

1. 클라이언트의 **인증서** 디렉터리에 설치된 [!DNL trust_cert_ca.pem]에 발급 CA 인증서를 추가하고, 이 사용자 정의 인증서를 사용하여 클러스터 내 모든 서버의 인증서에 액세스할 수 있습니다.

1. 다음 조건에 따라 클러스터 내 각 서버의 사용자 정의 인증서를 받습니다.

   1. 인증서의 형식이 [!DNL .pem] 인증서로 지정됩니다.
   1. 인증서에는 인증서 키가 있고 인증서는 암호화되지 않습니다(예: 암호/암호구가 없음).

      인증서에는 다음 문구 중 하나가 포함된 인증서 키가 있습니다.

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      [!DNL .pem] 인증서에서 암호구를 제거하는 방법 중 하나:

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. 인증서에는 CN, O, OU 등이 있습니다. 서버의 [!DNL Access Control.cfg] 파일에서 해당 클라이언트에 필요한 인증서입니다.
   1. *클라이언트* *기능 **** (또는 *서버* **및** *클라이언트* 기능 모두)이 포함된 인증서가 발급되었습니다.

      인증서에 서버 및/또는 클라이언트의 기능 코드가 있는지 확인하기 위해 다음 명령어를 사용할 수 있습니다.

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      서버 인증서의 경우 두 명령어 모두 일시 중단되어야 합니다.

      ```
      custom_communications_cert.pem: OK
      ```

      클라이언트 인증서의 경우 두 번째 명령어만 일시 중단되어야 합니다 [!DNL OK].

1. 클라이언트의 **인증서** 디렉터리에 인증서를 배치합니다.
1. 이 인증서를 사용하려는 각 클러스터의 [!DNL Insight.cfg] *serverInfo* 에 *사용자 정의 인증서* 가 지정되었는지 확인합니다.

   ```
   Servers = vector: 1 items 
     0 = serverInfo: 
       SSL Client Certificate = string:
   <my_custom_client_cert.pem>
   ```

## 사용자 정의 서버 인증서 설정 {#setting-up-custom-server-certificates}

이 섹션은 실행 중인 클러스터가 Visual Sciences에서 발급한 인증서를 사용하고 있다고 가정합니다. 구성은 일반 사례(예: 마스터의 *프로세싱 서버 디렉터리 구성 요소* 가 모든 DPU의 *구성 요소* 디렉터리와 동기화)를 따릅니다.

1. 클러스터 내 모든 서버와 이 클러스터와 통신할 모든 클라이언트에 설치된 [!DNL trust_cert_ca.pem] 에 발급 CA 인증서를 추가합니다.
1. 이러한 요구 사항에 따라 클러스터 내 각 서버의 사용자 정의 인증서를 받습니다.

   1. 사용자 정의 인증서의 형식이 [!DNL .pem] 인증서로 지정됩니다.
   1. 인증서에는 인증서 키가 있고 인증서는 암호화되지 않습니다(예: 암호/암호구가 없음).

      인증서에는 다음 문구가 포함된 경우 인증서 키가 있습니다.

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      [!DNL .pem] 인증서에서 암호구를 제거하는 방법 중 하나:

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. 인증서에는 최근 서버에 설치된 [!DNL server_cert.pem] 와(과) 동일한 CN이 있습니다.
   1. *서버* 및 *클라이언트* 기능이 포함된 인증서가 발급되었습니다.

      인증서에 서버 및/또는 클라이언트의 기능 코드가 있는지 확인하기 위해 다음 명령어를 사용할 수 있습니다.

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      서버 인증서의 경우 두 명령어 모두 일시 중단되어야 합니다.

      ```
      custom_communications_cert.pem: OK
      ```

      클라이언트 인증서의 경우 두 번째 명령어만 일시 중단되어야 합니다 [!DNL OK].

1. [!DNL custom_communications_cert.pem]으로 서버의 **인증서** 디렉터리에 각 서버의 사용자 정의 인증서를 설치합니다.

1. 텍스트 에디터를 사용하여, 첫 번째 문구([!DNL component = CommServer]) 바로 아래에 있는 *구성 요소* 와 *프로세싱 서버 디렉터리 구성 요소* 모두의 **Communications.cfg** 파일에 다음 문구를 추가합니다.

   ```
   Certificate = string: Certificates\\custom_communications_cert.pem
   ```

1. 모든 서버를 다시 시작합니다.

**인증서 오류 경고 정보**

Insight 서버 또는 클라이언트가 **인증서** 디렉터리에서 **라이선스** 인증서가 필요한 경우, 디렉터리의 모든 사용자 지정 인증서에 오류가 발생하면 하드 코딩된 Insight CA 사본에 대해 모든 인증서([!DNL trust_ca_cert.pem] 제외)를 검증해야 합니다. 서버에서 이 경고가 발행됩니다.

```
Certificate failed to verify. Error 20 at 0 depth. Desc: unable to get local issuer certificate. Cert details:
```

이 경고는 간단히 무시할 수 있습니다.
