---
description: Insight 프로그램 파일을 설치한 후에는 Adobe에서 제공하는 디지털 인증서를 다운로드하여 설치해야 합니다.
title: 디지털 인증서 다운로드 및 설치
uuid: 93ab2222-a977-4279-9e1e-71038b1d1cfa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 디지털 인증서 다운로드 및 설치{#downloading-and-installing-the-digital-certificate}

Insight 프로그램 파일을 설치한 후에는 Adobe에서 제공하는 디지털 인증서를 다운로드하여 설치해야 합니다.

## 디지털 인증서 다운로드 및 설치 {#topic-fed3b44e472c4e4ca6dd5852af14cdb9}

Insight 프로그램 파일을 설치한 후에는 Adobe에서 제공하는 디지털 인증서를 다운로드하여 설치해야 합니다.

## 디지털 인증서 이해 {#concept-9eed01c8d95440cda6ce29d68e65098c}

Adobe는 X.509 디지털 인증서를 사용하여 구현을 구성하는 클라이언트 및 서버 구성 요소를 식별하고 인증합니다.

<!--
c_undst_dgtl_crtf.xml
-->

Insight를 설치할 때 설치된 클라이언트 애플리케이션을 사용하려면 지정된 개인(예: Jane Smith)을 인증하는 디지털 인증서를 설치해야 합니다.

>[!NOTE]
>
>Insight를 다른 컴퓨터 또는 다른 명명된 사용자로 마이그레이션해야 하는 경우 Adobe에서 새 인증서를 받아야 합니다. 이렇게 하려면 Adobe 고객 지원 센터에 문의하십시오.

Insight는 서버 구성 요소에 액세스할 수 있도록 이 디지털 인증서를 제공합니다. 서버 구성 요소의 관리자는 사용자 인증서에 표시되는 일반 이름 또는 조직 단위 값을 기준으로 서버 리소스에 대한 액세스를 제한할 수 있습니다.

Adobe 응용 프로그램과 함께 설치되는 X.509 디지털 인증서는 클라이언트 및 서버 구성 요소에서 SSL(Secure Sockets Layer)을 통해 정보를 교환할 수도 있습니다. SSL은 공개 및 개인 키 암호화 시스템을 사용하여 HTTP를 통해 전송을 보호합니다. Adobe의 SSL 구현은 1024비트 RSA 키를 지원하며 128비트 RC4 암호화 알고리즘을 사용합니다.

보안 외에도 사용자가 설치하는 디지털 인증서는 Insight를 실행할 수 있는 라이센스 키로도 작동합니다. 디지털 인증서가 제대로 작동하려면 노드가 잠겼고 최신 상태여야 합니다. 그렇지 않으면 응용 프로그램이 시작되지 않습니다.

## 노드 잠금 인증서 {#section-984aa8f2f5a1448cadc4afea978aedc9}

노드 잠금 인증서는 컴퓨터가 설치된 컴퓨터에 등록된 디지털 인증서입니다. 노드 잠금은 특정 노드 식별자(특정 컴퓨터를 고유하게 식별하는 값)와 인증서를 영구적으로 연결합니다. 인증서를 노드 잠금하려면 컴퓨터에서 Adobe 라이센스 서버 또는 라이센스 서버에 액세스할 수 있는 프록시 서버에 대한 인터넷 액세스 권한이 있어야 합니다.

인터넷에 액세스할 수 없는 컴퓨터에 설치하는 경우, 인터넷 액세스 없이 컴퓨터에서 디지털 인증서 사용에 설명된 대로 미리 [잠근 특수 인증서를 받아서 설치해야 합니다](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#section-d3c060131d7f45cda27f68848b704fa1).

인터넷에 액세스할 수 있는 컴퓨터에 설치하는 경우 Insight를 처음 시작하면 디지털 인증서가 자동으로 노드 잠깁니다. 노드를 잠근 후에는 다른 컴퓨터에서 인증서를 사용할 수 없습니다. Insight를 다른 컴퓨터로 마이그레이션해야 하는 경우 Adobe에서 잠금 해제된 새 인증서를 받아야 합니다.

## 현재 인증서 {#section-0816b031df3e415ab3f0205b720c723e}

노드가 잠겨있을 뿐만 아니라 디지털 인증서가 최신 상태여야 합니다. 최신 상태로 유지하려면, 인증서의 유효성을 정기적으로 다시 검사해야 합니다(일반적으로 30일마다 확인되지만 Adobe와의 계약에 따라 달라질 수 있음). 컴퓨터에 인터넷에 액세스할 수 있는 경우 재인증 프로세스는 완전히 투명하게 진행됩니다. Insight는 자동으로 라이센스 서버에 연결하여 필요한 경우 인증서의 유효성을 다시 검사합니다. 컴퓨터에 인터넷에 액세스할 수 없는 경우 다음 섹션에 설명된 대로 업데이트된 인증서를 수동으로 설치해야 합니다.

## 인터넷 액세스 권한이 없는 컴퓨터에서 디지털 인증서 사용 {#section-d3c060131d7f45cda27f68848b704fa1}

인터넷에 액세스할 수 없는 컴퓨터에 설치하는 경우 Insight 설치를 위해 미리 잠긴 인증서를 요청해야 합니다. 사전 잠김 인증서는 Adobe가 컴퓨터의 노드 식별자에 수동으로 잠그는 디지털 인증서입니다.

사전 잠김 인증서를 요청하려면 노드 식별자 및 인증서 번호를 Adobe 고객 지원 센터로 보내야 합니다. 컴퓨터의 노드 식별자를 얻으려면 Adobe 고객 지원 센터에 문의하여 Adobe [!DNL Node Identifier] 유틸리티를 요청하십시오. 또한 Insight가 라이센스 서버에 연결을 시도할 때 문제를 일으키며 연결할 수 없다는 경고에서 노드 식별자를 가져올 수도 있습니다. 사전 잠김 인증서를 받으면 디지털 인증서 설치의 마지막 두 단계에 설명된 대로 [설치합니다](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#task-1dad1e1d86d04100a7bcf87f26303c38).

인증서의 유효성을 다시 검사해야 하는 경우 라이센스 서버에서 유효성이 확인된 새 인증서를 다운로드하여 컴퓨터에 다시 설치해야 합니다(Adobe와의 계약에 다른 규정이 없는 경우).

## 디지털 인증서 설치 {#task-1dad1e1d86d04100a7bcf87f26303c38}

<!--
t_install_dgtl_crtf.xml
-->

**디지털 인증서를 다운로드하여 설치하려면**

1. 웹 브라우저를 열 수 [!DNL http:\\license.visualsciences.com]있습니다.

   >[!NOTE]
   >
   >이때 브라우저가 디지털 인증서를 제시하라는 메시지를 표시할 수 있습니다. 그런 경우 을 클릭하여 대화 상자를 **[!UICONTROL Cancel]** 닫습니다.

1. 로그인 화면에서 Adobe로부터 받은 [!DNL Account Name] 및 [!DNL Password] 을 입력한 다음 을 클릭합니다 **[!UICONTROL login]**.
1. 인사이트 인스턴스에 대해 발급된 인증서(Your Name. *pem*)를 찾아 해당 인증서와 연결된 ![](assets/btn_save_certificatedownload.PNG) 아이콘을 클릭합니다.
1. 인증서를 저장하라는 메시지가 표시되면 을 클릭합니다 **[!UICONTROL Save]**.
1. Insight를 설치한 디렉토리의 [!DNL Certificates] 폴더에 파일을 다운로드합니다.

   이 폴더에는 이름이 지정된 인증서 파일이 [!DNL trust_ca_cert.pem]있습니다. Insight가 작동하려면 두 인증서 파일이 항상 있어야 합니다.

## Windows 인증서 저장소 {#concept-4acb13b7de9340ea8cde8ad84b93358d}

Windows 인증서 저장소를 사용하면 서버와의 SSL 통신을 위해 Windows 인증서 저장소에 클라이언트의 인증서 및 개인 키를 저장할 수 있습니다.

<!--
crypto-api.xml
-->

클라이언트에 대한 Windows 인증서 저장소는 SSL 통신 인증서와 개인 키를 `Insight/Certificates/<CertName>.pem` 파일이 아닌 Windows 인증서 저장소에 저장할 수 있는 새로운 기능입니다. 다른 응용 프로그램에 대해 인증서 저장소를 사용하고 한 곳에서 인증서 관리를 하려는 경우 또는 Windows 인증서 저장소에서 제공하는 추가 Windows 감사 로깅을 즐기는 사용자에게 Windows 인증서 저장소를 사용하는 것이 좋습니다.

>[!NOTE]
>
>라이센스 서버와의 라이센스는 여전히 기존 `<Common Name>.pem` 파일을 사용하여 유지되며 인증서 저장소에서 얻은 인증서는 지정한 서버와의 통신에 대해서만 사용됩니다.

## 전제 조건 {#section-69b18600052145ff8e5299b7123e69c5}

1. 인증서 및 키를 개인 [!DNL certmgr.msc] 스토어로 가져올 수 있는 권한이 있어야 **합니다** . (대부분의 Windows 사용자에 대해 기본적으로 true여야 합니다.)

1. 구성을 수행하는 사용자는 OpenSSL **명령줄 도구의** 복사본이 있어야 합니다.
1. 사용자 정의 SSL 인증서를 사용하도록 서버 및 클라이언트를 이미 구성해야 하며 인증서 디렉토리에 저장하지 않고 Windows 인증서 저장소에 클라이언트 인증서를 저장하는 지침을 **제공합니다** .

## Windows 인증서 저장소 구성 {#section-3629802122e947d4b4f63e8b732cfe27}

클라이언트에 대한 Windows 인증서 저장소는 다음 단계에 따라 활성화됩니다.

**1단계:사용자의 SSL 인증서 및 개인 키를 Windows 인증서 저장소로 가져옵니다.**

데이터 [워크벤치에서 사용자 지정 인증서](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) 사용에서 SSL 인증서와 키를 다음 디렉토리에 넣도록 지시됩니다.

```
< 
<filepath>
  DWB Install folder 
</filepath>>\Certificates\
```

인증서 이름은 Analytics Server 1.pem(trust_ca_cert.pem 파일이 `<Common Name>.pem` 아님)과 같습니다.

인증서 및 개인 키를 가져오기 전에 에서 변환해야 합니다. [!DNL pem] 형식을 [!DNL .pfx] 형식(예: [!DNL pkcs12.pfx] )으로 지정합니다.

1. 명령 프롬프트 또는 터미널을 열고 다음 디렉토리로 이동합니다.

   ```
   <CommonName>.pem c: cd \<filepath>DWB Install folder</filepath>>\Certificates
   ```

1. 다음 인수를 [!DNL openssl] 사용하여 실행합니다(실제 [!DNL .pem] 파일 이름 포함).

   ```
   openssl pkcs12 -in "<Common Name>.pem" -export -out "<Common Name>.pfx"
   ```

   메시지가 표시되면 Enter **를** 눌러 내보내기 암호 입력을 건너뜁니다.

1. 실행 프롬프트, 시작 메뉴 또는 명령줄에서 [!DNL certmgr.msc] 실행합니다.
1. 현재 **사용자의 개인** 인증서 저장소를 엽니다.

   ![](assets/6_5_crypto_api_0.png)

1. 인증서를 마우스 오른쪽 단추로 클릭하고 **모든** 작업 **> 가져오기를** 클릭합니다 ****.

   [현재 사용자] **옵션을** 선택한 다음 [다음]을 **클릭합니다**.

   ![](assets/6_5_crypto_api_4.png)

1. 찾아보기를 **클릭하고** 이전에 만든 `<CommonName>.pfx` 파일을 선택합니다. 파일 확장자 드롭다운 상자를 X.509 인증서에서 개인 정보 교환 **또는 모든** 파일로변경해야 **파일을** 볼 수 있습니다.

   파일을 선택하고 [열기] **를**&#x200B;클릭한 다음 **[다음]을**&#x200B;클릭합니다.

1. 암호를 입력하지 말고 이 키를 내보낼 수 **있는** 것으로 표시 및 모든 확장 속성 **** 포함 옵션만선택되어 있는지 확인합니다.

   ![](assets/6_5_crypto_api_3.png)

   **다음**&#x200B;을 클릭합니다.

1. 다음 **저장소에** 모든 인증서를 배치하고 나열된 인증서 저장소가 개인인지 확인하십시오 ****. (고급 사용자의 경우 이 시점에서 다른 스토어를 선택할 수 있지만 나중에 구성을 변경해야 합니다.)

1. 다음을 **클릭한** 다음 마침을 **클릭합니다**. 가져오기가 성공적이었고 스토어의 인증서 폴더에서 인증서를 볼 수 있다는 대화 상자가 표시됩니다.

   >[!NOTE]
   >
   >발급 대상 및 **발급자** 필드에 **대해** 특별히 주의하십시오. 다음 단계에서 필요한 것입니다.

**2단계:Insight.cfg 파일을 편집합니다.**

Data Workbench에서 Windows 인증서 저장소 기능을 사용하도록 하려면 파일을 편집해야 [!DNL Insight.cfg] 합니다. 이 파일의 각 서버 항목에는 몇 가지 추가 매개 변수가 지정되어 있어야 합니다. 매개 변수를 생략하면 워크스테이션은 기본적으로 기존 인증서 구성을 사용합니다. 매개 변수가 지정되었지만 잘못된 값이 있는 경우 워크스테이션에 오류 상태가 입력되고 오류 정보를 보려면 로그 파일을 참조해야 합니다.

1. Insight **.cfg** 파일을 엽니다(Insight **설치** 디렉토리에있음).

1. 구성할 서버 항목으로 스크롤합니다. 모든 서버에 대해 Windows 인증서 저장소를 사용하려면 [!DNL serverInfo] 개체 벡터의 모든 항목을 수정해야 합니다.
1. 이러한 매개 변수를 [!DNL Insight.cfg] 파일에 추가합니다. 이 작업은 워크스테이션에서 또는 다음 매개변수를 [!DNL serverInfo] 객체에 추가하여 수동으로 수행할 수 있습니다. 탭 문자 대신 공백을 사용해야 하며 이 파일에서 다른 타이포그래피 또는 구문 오류를 발생시키지 마십시오.)

   ```
   SSL Use CryptoAPI = bool: true  
   SSL CryptoAPI Cert Name = string: <Common Name>  
   SSL CryptoAPI Cert Issuer Name = string: Visual Sciences,LLC  
   SSL CryptoAPI Cert Store Name = string: My 
   ```

   부울은 기능을 활성화하거나 비활성화합니다. 인증서 이름은 인증서 **관리자의** 발급자 이름과 일치합니다. 인증서 발급자 이름이 발급자와 **일치하고**&#x200B;저장소 **이름이** 인증서 저장소 이름과 일치해야 합니다.

   >[!NOTE]
   >
   >인증서 관리자(certmgr.msc)의 &quot;개인&quot;이라는 이름은 실제로 My라는 인증서 저장소를 **나타냅니다.** 따라서 SSL 통신 인증서 및 키(.PFX)를 Personal **인증서** 저장소로 가져오는 경우 **SSL CryptoAPI Cert Store 이름** 문자열을 &quot;My&quot;로 설정해야 합니다. 이 매개 변수를 &quot;개인&quot;으로 설정하면 작동하지 않습니다. 이것은 Windows 인증서 저장소의 특성입니다.

   사전 정의된 시스템 스토어의 전체 목록을 여기에서 얻을 수 있습니다.https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136(v=vs.85).aspx [](https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136%28v=vs.85%29.aspx). 시스템에 추가 인증서 저장소가 있을 수 있습니다. &quot;개인&quot;(예: 내) **이 아닌**&#x200B;스토어를 사용하려면 인증서 저장소의 정식 이름을 얻고 [!DNL Insight.cfg] 파일에 제공해야 합니다. (시스템 저장소 이름 &quot;My&quot;는 Windows 설명서에서 &quot;My&quot; 및 &quot;MY&quot;로 일관되지 않습니다. 매개 변수는 대/소문자를 구분하지 않습니다.)

1. 이러한 매개 변수를 추가하고 값이 Windows 인증서 관리자의 목록과 일치하는지 확인한 후 [!DNL Insight.cfg] 파일을 저장합니다.

이제 워크스테이션을 시작하거나 서버의 연결을 끊거나 다시 연결할 수 있습니다. 데이터 워크벤치는 인증서 저장소에서 인증서 및 키를 로드하고 정상적으로 연결해야 합니다.

## 로그 출력 {#section-a7ef8c9e90ef4bbabaa3cd51a2aca3ab}

인증서를 찾을 수 없거나 유효하지 않은 경우 이 오류 메시지가 [!DNL HTTP.log] 파일에 표시됩니다.

```
ERROR Fatal error: the cert could not be found!
```

>[!NOTE]
>
>L4 로깅 프레임워크는 [!DNL L4.cfg] 파일을 설정하여 활성화할 수 있습니다(이 설정을 위한 계정 관리자 참조).

## 데이터 워크벤치에서 사용자 지정 인증서 사용 {#concept-ee6a9b5015f84a0ba64a11428b0a72dd}

사용자 정의 인증서 사용 지침

<!--
using-custom-certificates-DWB.xml
-->

Data Workbench 클라이언트 또는 서버에서 사용하는 인증서는 신뢰할 수 있는 CA(인증 기관)에서 서명해야 합니다. Data Workbench 고객은 Visual Sciences CA에서 서명한 인증서를 받습니다. 이러한 인증서는 Visual Sciences CA에 대한 루트 CA 인증서를 [!DNL trust_ca_cert.pem] 포함하므로 Data Workbench **** 소프트웨어는 Insight 소프트웨어와 함께 제공되며 *서버 및 클라이언트의 인증서* 디렉토리에 보관됩니다. 이러한 인증서는 클라이언트와 서버가 SSL을 사용하여 통신할 때 소프트웨어 라이센스와 인증 모두에 사용됩니다. Visual Sciences CA에서 발행한 인증서만 라이센스에 사용할 수 있지만 다른 인증서는 통신 및 인증에 사용할 수 있습니다. Visual Sciences 이외의 CA에서 발행한 인증서는 *사용자 정의 인증이라고 합니다.*

**중요 정보:** 서버 및 클라이언트의 경우 Data Workbench 소프트웨어는 클라이언트 또는 서버의 인증서 **디렉토리에** 설치된 인증서 파일이나 구성에 명시적으로 식별된 인증서를 사용합니다. 그러나 클라이언트용 Windows 인증서 저장소를 사용할 수도 있습니다.

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
   1. 인증서가 *클라이언트의* *목적 **** 또는 두 가지 *클라이언트* 서버 **및 SafetyClient** 와 함께 **&#x200B;발급되었습니다.

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

1. 텍스트 편집기를 사용하여 처리 서버용 구성 요소 및 **구성** 요소 *디렉토리에* 있는 Communications.cfg *파일에 첫 번째 줄* ( [!DNL component = CommServer]) 바로 아래에 다음 줄을 추가합니다.

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

## 문자열 암호화 {#concept-35da0b53650a4d7e82b240ad27f6d45a}

클라이언트와 서버 간의 통신 시 암호 및 기타 문자열을 암호화합니다.

<!--
string_encryption.xml
-->

데이터 워크벤치 클라이언트(워크스테이션)와 서버 간에 통신할 때 Value 매개 변수(암호 등)를 EncryptedString 유형으로 저장할 수 *있습니다*. 그러면 매개 변수가 숨겨지고 해당 키가 반환된 *상태로* 서버의 Windows 자격 증명 저장소에 문자열이 저장됩니다. 기본적으로 내보내기에 사용되는 자격 증명이 저장되지만 매개 변수를 암호화하는 데 사용할 수 있습니다.

* Server\*EncryptStrings*에 새&#x200B;*폴더가 추가되었습니다*.

   구성 파일을 설정하여 문자열을 암호화합니다.

* Server\Component\*EncryptedStrings.cfg **에 새 구성 파일이 추가되었습니다*.

   ```
   component = EncryptionComponent: 
     Path = Path: EncryptStrings\\*.cfg
   ```

   이 파일은 암호화 구성 *파일을*&#x200B;위해 Server\*EncryptStrings* 폴더를 폴링합니다.

**문자열을**&#x200B;암호화하려면

1. 다음 **필드를** 설정하여 문자열에 대한 EncryptedStrings.cfg 구성 파일을 만듭니다.

   ```
   Names = vector: 1 items 
    0 = NameEncryptValuePair: 
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server 
     Name = string: // Name for identifier  
     Value = string: // Value to be encrypted
   ```

   * *값* - 이 필드에는 암호화해야 하는 일반 텍스트 문자열이 포함되어 있습니다.

      서버 측 암호입니다. 값 *설정은* 서버 컴퓨터에서만 암호화됩니다.

   * *이름* - 이 필드에는 암호화된 문자열을 식별하는 값이 포함되어 있습니다.
   * *EncryptValue* - 이 필드는 입력 구성 파일에 비어 있게 됩니다. 암호화된 값이 이 필드에 반환됩니다.
   암호화에 대해 여러 **필드에** NameEncryptValuePair 값을 추가할 수 있습니다.

   >[!NOTE]
   >
   >빈 값 필드는 모두 제거됩니다.

1. EncryptedStrings. **cfg** 파일을 Server\*EncryptStrings ** 폴더에*&#x200B;저장합니다.

**출력 파일**

출력 파일은 &lt;*filename*>의 입력 파일과 동일한 이름으로 생성됩니다.*암호화된* 확장. 예를 들어 입력 파일의 이름이 *sample.cfg* 인 경우 출력 파일의 이름은 *sample.cfg.encrypted*&#x200B;입니다.