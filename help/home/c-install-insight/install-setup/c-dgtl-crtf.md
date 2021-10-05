---
description: Insight 프로그램 파일을 설치한 후에는 Adobe에서 제공한 디지털 인증서를 다운로드하여 설치해야 합니다.
title: 디지털 인증서 다운로드 및 설치
uuid: 93ab2222-a977-4279-9e1e-71038b1d1cfa
exl-id: 0dff95ae-880b-45d5-96df-4eb6bea58891
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '2743'
ht-degree: 74%

---

# 디지털 인증서 다운로드 및 설치{#downloading-and-installing-the-digital-certificate}

Insight 프로그램 파일을 설치한 후에는 Adobe에서 제공한 디지털 인증서를 다운로드하여 설치해야 합니다.

## 디지털 인증서 다운로드 및 설치 {#topic-fed3b44e472c4e4ca6dd5852af14cdb9}

Insight 프로그램 파일을 설치한 후에는 Adobe에서 제공한 디지털 인증서를 다운로드하여 설치해야 합니다.

## 디지털 인증서 이해 {#concept-9eed01c8d95440cda6ce29d68e65098c}

Adobe은 X.509 디지털 인증서를 사용하여 구현을 구성하는 클라이언트 및 서버 구성 요소를 식별하고 인증합니다.

<!--
c_undst_dgtl_crtf.xml
-->

Insight를 설치할 때 설치된 클라이언트 응용 프로그램을 사용하려면 이름이 지정된 개인(예: Jane Smith)을 인증하는 디지털 인증서를 설치해야 합니다.

>[!NOTE]
>
>Insight를 다른 컴퓨터 또는 다른 명명된 사용자로 마이그레이션해야 하는 경우 Adobe에서 새 인증서를 받아야 합니다. 이 작업을 수행하려면 Adobe 고객 지원 센터에 문의하십시오.

인사이트는 서버 구성 요소에 액세스할 수 있도록 이 디지털 인증서를 제공합니다. 서버 구성 요소의 관리자는 사용자 인증서에 표시되는 일반 이름 또는 조직 단위 값을 기준으로 서버 리소스에 대한 액세스를 제한할 수 있습니다.

Adobe 애플리케이션과 함께 설치되는 X.509 디지털 인증서에서도 클라이언트 및 서버 구성 요소가 SSL(Secure Sockets Layer)을 통해 정보를 교환할 수 있습니다. SSL은 공개 및 개인 키 암호화 시스템을 사용하여 HTTP를 통해 전송을 보호합니다. Adobe의 SSL 구현은 1024비트 RSA 키를 지원하며 128비트 RC4 암호화 알고리즘을 사용합니다.

보안 이외에도 설치한 디지털 인증서는 Insight를 실행할 수 있는 라이센스 키로도 작동합니다. 디지털 인증서가 제대로 작동하려면 노드가 잠기고 최신 상태여야 합니다. 그렇지 않으면 응용 프로그램이 시작되지 않습니다.

## 노드 잠금 인증서 {#section-984aa8f2f5a1448cadc4afea978aedc9}

노드 잠금 인증서는 컴퓨터가 설치된 컴퓨터에 등록된 디지털 인증서입니다. 노드 잠금은 특정 노드 식별자(특정 컴퓨터를 고유하게 식별하는 값)와 인증서를 영구적으로 연결합니다. 인증서를 노드에 잠그려면 Adobe 라이센스 서버 또는 라이센스 서버에 대한 액세스 권한이 있는 프록시 서버에 대한 인터넷 액세스 권한이 있어야 합니다.

인터넷에 액세스할 수 없는 컴퓨터에 설치하는 경우 [인터넷에 액세스할 수 없는 컴퓨터에서 디지털 인증서 사용](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#section-d3c060131d7f45cda27f68848b704fa1)에 설명된 대로 미리 잠금 특수 인증서를 가져와 설치해야 합니다.

인터넷에 액세스할 수 있는 컴퓨터에 설치하는 경우 Insight를 처음 시작할 때 디지털 인증서가 자동으로 노드 잠깁니다. 노드를 잠근 후에는 다른 컴퓨터에서 인증서를 사용할 수 없습니다. Insight를 다른 컴퓨터로 마이그레이션해야 하는 경우 Adobe에서 잠금이 해제된 새 인증서를 받아야 합니다.

## 현재 인증서 {#section-0816b031df3e415ab3f0205b720c723e}

노드가 잠겼을 뿐만 아니라 디지털 인증서가 최신 상태여야 합니다. 최신 상태를 유지하려면, 인증서의 유효성을 정기적으로 재검사해야 합니다(일반적으로 30일마다 확인되지만, Adobe와의 계약에 따라 달라질 수 있음). 컴퓨터에 인터넷에 액세스할 수 있는 경우 재인증 프로세스는 완전히 투명합니다. Insight는 라이센스 서버에 자동으로 연결되고 필요한 경우 인증서의 유효성을 다시 확인합니다. 컴퓨터에 인터넷에 액세스할 수 없는 경우 다음 섹션에 설명된 대로 업데이트된 인증서를 수동으로 설치해야 합니다.

## 인터넷에 액세스할 수 없는 컴퓨터에서 디지털 인증서 사용 {#section-d3c060131d7f45cda27f68848b704fa1}

인터넷에 액세스할 수 없는 컴퓨터에 설치하는 경우, 미리 잠금 인증서를 요청하여 Insight 설치를 완료해야 합니다. 미리 잠금 인증서는 Adobe이 컴퓨터의 노드 식별자에 수동으로 잠그는 디지털 인증서입니다.

미리 잠금 인증서를 요청하려면 노드 식별자 및 인증서 번호를 Customer Care Adobe으로 보내야 합니다. 컴퓨터의 노드 식별자를 얻으려면 Adobe 고객 지원 센터에 문의하여 Adobe [!DNL Node Identifier] 유틸리티를 요청하십시오. 또한 Insight가 라이센스 서버에 연결하려고 할 때 문제가 발생하여 연결할 수 없다는 경고에서 노드 식별자를 가져올 수도 있습니다. 미리 잠금 인증서를 받으면 [디지털 인증서 설치](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#task-1dad1e1d86d04100a7bcf87f26303c38)의 마지막 두 단계에 설명된 대로 설치합니다.

인증서의 유효성을 다시 검사해야 하는 경우 라이센스 서버에서 유효성이 확인된 새 인증서를 다운로드하여 컴퓨터에 다시 설치해야 합니다(Adobe 상태와의 계약이 따로 없는 경우).

## 디지털 인증서 설치 {#task-1dad1e1d86d04100a7bcf87f26303c38}

<!--
t_install_dgtl_crtf.xml
-->

**디지털 인증서를 다운로드하여 설치하려면 다음을 수행하십시오.**

1. 웹 브라우저를 열고 [!DNL https:\\license.visualsciences.com](으)로 이동합니다.

   >[!NOTE]
   >
   >이때 브라우저에서 디지털 인증서를 입력하라는 메시지가 표시될 수 있습니다. 이 경우 **[!UICONTROL Cancel]** 을 클릭하여 대화 상자를 닫습니다.

1. 로그인 화면에서 Adobe에서 받은 [!DNL Account Name] 및 [!DNL Password] 을 입력한 다음 **[!UICONTROL login]**&#x200B;을 클릭합니다 .
1. Insight 인스턴스에 대해 발급된 인증서( *이름*.pem)를 찾고 해당 인증서와 연결된 ![](assets/btn_save_certificatedownload.PNG) 아이콘을 클릭합니다.
1. 인증서를 저장하라는 메시지가 표시되면 **[!UICONTROL Save]**&#x200B;을 클릭합니다 .
1. Insight를 설치한 디렉토리의 [!DNL Certificates] 폴더에 파일을 다운로드합니다.

   이 폴더에는 [!DNL trust_ca_cert.pem] 인증서 파일이 포함되어 있습니다. Insight가 작동하려면 두 인증서 파일이 항상 있어야 합니다.

## Windows 인증서 저장소 {#concept-4acb13b7de9340ea8cde8ad84b93358d}

Windows 인증서 저장소를 사용하면 서버와의 SSL 통신을 위해 Windows 인증서 저장소에 클라이언트의 인증서 및 개인 키를 저장할 수 있습니다.

<!--
crypto-api.xml
-->

클라이언트용 Windows 인증서 저장소는 SSL 통신 인증서와 개인 키를 `Insight/Certificates/<CertName>.pem` 파일이 아닌 Windows 인증서 저장소에 저장할 수 있는 새로운 기능입니다. 다른 애플리케이션에 대해 인증서 저장소를 사용하고 한 곳에서 인증서 관리를 하려는 경우 또는 Windows 인증서 저장소에서 제공하는 추가 Windows 감사 로깅을 사용하는 사용자의 경우 Windows 인증서 저장소를 사용하는 것이 좋습니다.

>[!NOTE]
>
>라이선스 서버의 라이선스는 여전히 기존 `<Common Name>.pem` 파일을 사용하여 유지되며 인증서 저장소에서 가져온 인증서는 지정한 서버와의 통신에 대해서만 사용됩니다.

## 전제 조건 {#section-69b18600052145ff8e5299b7123e69c5}

1. [!DNL certmgr.msc] 파일에 액세스하여 인증서 및 키를 **Personal** 저장소로 가져올 수 있어야 합니다. (대부분의 Windows 사용자의 경우 기본적으로 true로 설정되어야 함).

1. 구성을 수행하는 사용자에게는 **OpenSSL** 명령줄 도구의 사본이 있어야 합니다.
1. 사용자 지정 SSL 인증서를 사용하도록 서버 및 클라이언트가 구성되어 있어야 합니다. 이 지침은 **Certificates** 디렉터리에 클라이언트 인증서를 저장하지 않고 Windows 인증서 저장소에 클라이언트 인증서를 저장하는 지침을 제공합니다.

## Windows 인증서 저장소 구성 {#section-3629802122e947d4b4f63e8b732cfe27}

클라이언트용 Windows 인증서 저장소는 다음 단계에 따라 활성화됩니다.

**1단계: 사용자의 SSL 인증서 및 개인 키를 Windows 인증서 저장소로 가져옵니다.**

[Data Workbench](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd)에서 사용자 정의 인증서를 사용하면 SSL 인증서와 키를 다음 디렉토리에 추가하라는 메시지가 표시됩니다.

```
<
<filepath>
  DWB Install folder
</filepath>>\Certificates\
```

인증서의 이름은 Analytics Server 1.pem(trust_ca_cert.pem 파일 아님)과 같은 `<Common Name>.pem`입니다.

인증서 및 개인 키를 가져오기 전에 [!DNL pem] 형식에서 [!DNL .pfx] 형식(예: [!DNL pkcs12.pfx] ) 으로 변환해야 합니다.

1. 명령 프롬프트 또는 터미널을 열고 다음 디렉터리로 이동합니다.

   ```
   <CommonName>.pem c: cd \<filepath>DWB Install folder</filepath>>\Certificates
   ```

1. 다음 인수(실제 [!DNL openssl] 파일 이름 포함)로 [!DNL .pem] 을 실행합니다.

   ```
   openssl pkcs12 -in "<Common Name>.pem" -export -out "<Common Name>.pfx"
   ```

   메시지가 표시되면 **Enter** 를 눌러 암호 내보내기를 건너뜁니다.

1. 실행 프롬프트, 시작 메뉴 또는 명령줄에서 [!DNL certmgr.msc] 를 실행합니다.
1. 현재 사용자의 **Personal** 인증서 저장소를 엽니다.

   ![](assets/6_5_crypto_api_0.png)

1. **Certificates** 를 마우스 오른쪽 버튼으로 클릭하고 **모든 작업** > **가져오기**&#x200B;를 클릭합니다.

   **현재 사용자** 옵션이 선택되어 있는지 확인하고 **다음**&#x200B;을 클릭합니다.

   ![](assets/6_5_crypto_api_4.png)

1. **찾아보기** 를 클릭하고 이전에 만든 `<CommonName>.pfx` 파일을 선택합니다. X.509 인증서에서 파일 확장자 드롭다운 상자를 **개인 정보 교환** 또는 **모든 파일** 로 변경해야 이를 확인할 수 있습니다.

   파일을 선택하고 **열기**&#x200B;를 클릭한 후 **다음**&#x200B;을 클릭합니다.

1. 암호를 입력하지 말고 **이 키를 내보낼 수 있도록 표시** 및 **모든 확장 속성 포함** 옵션만 선택되었는지 확인합니다.

   ![](assets/6_5_crypto_api_3.png)

   **다음**&#x200B;을 클릭합니다.

1. **모든 인증서를 다음 저장소에 저장** 을 선택하고 나열된 인증서 저장소가 **Personal**&#x200B;인지 확인하십시오. (고급 사용자의 경우 이 시점에서 다른 저장소를 선택할 수 있지만 나중에 구성을 변경해야 합니다.)

1. **다음** 을 클릭한 다음 **마침**&#x200B;을 클릭합니다. 가져오기에 성공했으며 저장소의 인증서 폴더에 인증서가 저장되었다는 대화 상자가 표시됩니다.

   >[!NOTE]
   >
   >**발급 대상** 및 **발급 대상 필드** 에 특별히 주의하십시오. 다음 단계에서 이러한 항목이 필요합니다.

**2단계: Insight.cfg 파일을 편집합니다.**

Data Workbench에서 Windows 인증서 저장소 기능을 사용하도록 하려면 [!DNL Insight.cfg] 파일을 편집해야 합니다. 이 파일의 각 서버 항목에는 몇 가지 추가 매개 변수가 지정되어 있어야 합니다. 매개 변수를 생략하면 워크스테이션은 기본적으로 기존 인증서 구성을 사용합니다. 매개 변수가 지정되었지만 값이 잘못된 경우 워크스테이션에서 오류 상태를 입력하고 오류 정보를 보려면 로그 파일을 참조해야 합니다.

1. **Insight.cfg** 파일(**Insight** 설치 디렉터리)을 엽니다.

1. 구성할 서버 항목으로 스크롤합니다. 모든 서버에 대해 Windows 인증서 저장소를 사용하려면 [!DNL serverInfo] 객체 벡터의 모든 항목을 수정해야 합니다.
1. 이러한 매개 변수를 [!DNL Insight.cfg] 파일에 추가합니다. 이 작업은 워크스테이션에서 수행하거나 [!DNL serverInfo] 객체에 다음 매개 변수를 추가하여 수동으로 수행할 수 있습니다. (tab 문자 대신 공백을 사용해야 하며 이 파일에서 기타 오타 또는 구문 오류가 발생하지 않아야 합니다.)

   ```
   SSL Use CryptoAPI = bool: true
   SSL CryptoAPI Cert Name = string: <Common Name>
   SSL CryptoAPI Cert Issuer Name = string: Visual Sciences,LLC
   SSL CryptoAPI Cert Store Name = string: My
   ```

   부울을 사용하여 기능을 활성화하거나 비활성화할 수 있습니다. 인증서 이름은 인증서 관리자의 **발급 대상** 과 일치해야 합니다. 인증서 발급자 이름은 **발급자**&#x200B;와 일치하고 **저장소 이름** 은 인증서 저장소 이름과 일치해야 합니다.

   >[!NOTE]
   >
   >인증서 관리자(certmgr.msc)의 &quot;개인&quot;이라는 이름은 실제로 **My라는 인증서 저장소를 참조합니다.** 따라서 SSL 통신 인증서 및 키(.PFX)를 **Personal** 인증서 저장소로 가져오는 경우 **SSL CryptoAPI 인증서 저장소 이름** 문자열을 &quot;My&quot;로 설정해야 합니다. 이 매개 변수를 &quot;개인&quot;으로 설정하면 작동하지 않습니다. 이는 Windows 인증서 저장소의 특성입니다.

   사전 정의된 시스템 저장소의 전체 목록은 [https://msdn.microsoft.com/ko-kr/library/windows/desktop/aa388136(v=vs.85).aspx](https://msdn.microsoft.com/ko-kr/library/windows/desktop/aa388136%28v=vs.85%29.aspx)에서 확인할 수 있습니다. 시스템에 추가 인증서 저장소가 있을 수 있습니다. &quot;개인&quot; 이외의 저장소(예: **My**)를 사용하려면 인증서 저장소의 정식 이름을 가져와 [!DNL Insight.cfg] 파일에 입력해야 합니다. (시스템 저장소 이름 &quot;My&quot;는 Windows 설명서에서 일관되지 않게 &quot;My&quot; 및 &quot;MY&quot;로 사용됩니다. 매개 변수는 대/소문자를 구분하지 않습니다.)

1. 이러한 매개 변수를 추가하고 값이 Windows 인증서 관리자의 목록과 일치하는지 확인한 후 [!DNL Insight.cfg] 파일을 저장합니다.

이제 워크스테이션을 시작(또는 서버에 연결 해제/다시 연결)할 수 있습니다. Data Workbench가 인증서 저장소에서 인증서 및 키를 로드하고 정상적으로 연결해야 합니다.

## 로그 출력 {#section-a7ef8c9e90ef4bbabaa3cd51a2aca3ab}

인증서가 없거나 유효하지 않은 경우 이 오류 메시지가 [!DNL HTTP.log] 파일에 표시됩니다.

```
ERROR Fatal error: the cert could not be found!
```

>[!NOTE]
>
>L4 로깅 프레임워크는 [!DNL L4.cfg] 파일을 설정하여 활성화할 수 있습니다(이 설정과 관련한 내용은 계정 관리자 참조).

## Data Workbench에서 사용자 정의 인증서 사용 {#concept-ee6a9b5015f84a0ba64a11428b0a72dd}

사용자 정의 인증서 사용 지침.

<!--
using-custom-certificates-DWB.xml
-->

Data Workbench 클라이언트와 서버 중 하나에서 사용하는 인증서는 신뢰할 수 있는 CA(인증 당국)가 서명해야 합니다. Data Workbench 고객에게 Visual Sciences CA가 서명한 인증서가 발급됩니다. [!DNL trust_ca_cert.pem] (Insight 소프트웨어와 함께 제공되고 서버와 클라이언트의 **Certificates** 디렉터리에 저장됨)에는 Visual Sciences CA의 *루트 CA 인증서* 가 포함되어 있기 때문에 Data Workbench 소프트웨어는 이 인증서를 신뢰할 수 있습니다. 클라이언트와 서버가 SSL을 사용하여 상호 통신하는 경우 이 인증서는 소프트웨어와 인증에 라이선스를 부여하는 데 사용됩니다. 라이선싱에서는 Visual Sciences CA에서 발급한 인증서만을 사용할 수 있지만 통신 및 인증에 있어서는 다른 인증서를 사용할 수 있습니다. Visual Sciences이외의 CA에서 발급한 인증서는 *사용자 정의 인증서*&#x200B;라고 합니다.

**중요 정보:** 서버와 클라이언트의 경우 Data Workbench 소프트웨어는 클라이언트이나 서버의 **인증서** 디렉터리에 설치된 인증서 파일 또는 해당 구성에 명시된 인증서를 사용합니다. 단, 클라이언트의 Windows Certificate Store 를 사용할 수도 있습니다.

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

1. 텍스트 에디터를 사용하여, 첫 번째 문구(**) 바로 아래에 있는**&#x200B;구성 요소&#x200B;*와*&#x200B;프로세싱 서버 디렉터리 구성 요소&#x200B;*모두의* Communications.cfg[!DNL component = CommServer] 파일에 다음 문구를 추가합니다.

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

## 문자열 암호화 {#concept-35da0b53650a4d7e82b240ad27f6d45a}

클라이언트와 서버 간 통신하는 경우 암호와 기타 문자열을 암호화합니다.

<!--
string_encryption.xml
-->

Data Workbench 클라이언트(워크스테이션)와 서버 간 통신하는 경우 *EncryptedString* 유형이 포함된 값 매개 변수(암호 등)를 저장할 수 있습니다. 해당 키가 반환되면 매개 변수를 숨기고 서버측 *Windows Credential Store* 에 문자열을 저장합니다. 내보내기에 사용되는 자격 증명이 일차적으로 저장되지만 매개 변수를 암호화하는 데 사용될 수 있습니다.

* Server\**EncryptStrings**에 새 폴더가 추가되었습니다.

   여기에서 구성 파일을 설정하여 문자열을 암호화합니다.

* Server\Component\**EncryptedStrings.cfg**에 새 구성 파일이 추가되었습니다.

   ```
   component = EncryptionComponent:
     Path = Path: EncryptStrings\\*.cfg
   ```

   이 파일은 암호화 구성 파일의 *Server*\*EncryptStrings* 폴더를 폴링합니다.

**문자열을 암호화하려면**

1. 이들 필드가 설정되면 문자열의 **EncryptedStrings.cfg** 구성 파일을 생성합니다.

   ```
   Names = vector: 1 items
    0 = NameEncryptValuePair:
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server
     Name = string: // Name for identifier
     Value = string: // Value to be encrypted
   ```

   * *Value* - 이 필드에는 암호화될 일반 텍스트 문자열이 포함됩니다.

      서버측 암호화전용입니다. *Value* 설정은 서버 컴퓨터에서만 암호화됩니다.

   * *Name* - 이 필드에는 암호화된 문자열을 식별하는 값이 포함됩니다.
   * *EncryptValue* - 이 필드는 입력 설정 파일에 비워 둡니다. 암호화된 값이 이 필드에서 반환됩니다.

   다른 암호화 필드의 여러 **NameEncryptValuePair** 값을 추가할 수 있습니다.

   >[!NOTE]
   >
   >비어 있는 값 필드가 모두 제거됩니다.

1. *Server\*EncryptStrings** 폴더에 **EncryptedStrings.cfg** 파일을 저장합니다.

**출력 파일**

출력 파일이 &lt;*filename*>이 포함된 입력 파일과 동일한 이름으로 생성됩니다.*암호화된* 확장 프로그램. 예를 들어 입력 파일이 *sample.cfg* 로 지정되면 출력 파일이 *sample.cfg.encrypted*&#x200B;로 지정됩니다.
