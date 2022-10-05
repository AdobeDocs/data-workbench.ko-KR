---
description: Windows 인증서 저장소를 사용하면 서버와의 SSL 통신을 위해 Windows 인증서 저장소에 클라이언트의 인증서 및 개인 키를 저장할 수 있습니다.
title: Windows 인증서 저장소
uuid: a8021295-375a-460b-8686-acf3bc43cd17
exl-id: 8613a941-6213-4bfa-9c35-dccc2acb6c17
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 100%

---

# Windows 인증서 저장소{#windows-certificate-store}

{{eol}}

Windows 인증서 저장소를 사용하면 서버와의 SSL 통신을 위해 Windows 인증서 저장소에 클라이언트의 인증서 및 개인 키를 저장할 수 있습니다.

클라이언트용 Windows 인증서 저장소는 SSL 통신 인증서와 개인 키를 `Insight/Certificates/<CertName>.pem` 파일이 아닌 Windows 인증서 저장소에 저장할 수 있는 새로운 기능입니다. 다른 애플리케이션에 대해 인증서 저장소를 사용하고 한 곳에서 인증서 관리를 하려는 경우 또는 Windows 인증서 저장소에서 제공하는 추가 Windows 감사 로깅을 사용하는 사용자의 경우 Windows 인증서 저장소를 사용하는 것이 좋습니다.

>[!NOTE]
>
>라이선스 서버의 라이선스는 여전히 기존 `<Common Name>.pem` 파일을 사용하여 유지되며 인증서 저장소에서 가져온 인증서는 지정한 서버와의 통신에 대해서만 사용됩니다.

## 사전 요구 사항 {#section-69b18600052145ff8e5299b7123e69c5}

1. [!DNL certmgr.msc] 파일에 액세스하여 인증서 및 키를 **Personal** 저장소로 가져올 수 있어야 합니다. (대부분의 Windows 사용자의 경우 기본적으로 true로 설정되어야 함).

1. 구성을 수행하는 사용자에게는 **OpenSSL** 명령줄 도구의 사본이 있어야 합니다.
1. [사용자 정의 인증서 사용](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd)에서의 설명과 같이 사용자 정의 SSL 인증서를 사용하도록 서버 및 클라이언트가 구성되어 있어야 합니다. 이 지침은 **Certificates** 디렉터리에 클라이언트 인증서를 저장하지 않고 Windows 인증서 저장소에 클라이언트 인증서를 저장하는 지침을 제공합니다.

## Windows 인증서 저장소 구성 {#section-3629802122e947d4b4f63e8b732cfe27}

클라이언트용 Windows 인증서 저장소는 다음 단계에 따라 활성화됩니다.

**1단계: 사용자의 SSL 인증서 및 개인 키를 Windows 인증서 저장소로 가져옵니다.**

[사용자 정의 인증서 사용](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) 에서는 SSL 인증서와 키를 다음 디렉터리에 추가하라는 메시지가 표시됩니다.

```
< 
<filepath>
  DWB Install folder 
</filepath>>\Certificates\
```

인증서의 이름은 `<Common Name>.pem` (예: [!DNL Analytics Server 1.pem] [!DNL trust_ca_cert.pem] 파일 아님)입니다.

인증서 및 개인 키를 가져오기 전에 [!DNL pem] 형식에서 [!DNL .pfx] 형식(예: [!DNL pkcs12.pfx] ) 으로 변환해야 합니다.

1. 명령 프롬프트 또는 터미널을 열고 다음 디렉터리로 이동합니다.

   ```
   <CommonName>.pem c: cd \<DWB Install folder \Certificates
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
