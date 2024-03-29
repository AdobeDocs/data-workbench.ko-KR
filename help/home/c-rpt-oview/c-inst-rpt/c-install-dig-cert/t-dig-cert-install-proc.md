---
description: 디지털 인증서를 다운로드하여 설치하는 단계입니다.
title: 디지털 인증서 설치 절차
uuid: 14749a68-96cb-4cf4-819e-07df065e4016
exl-id: a8ae8d23-8db8-44d9-8c45-e552da81c384
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 33%

---

# 디지털 인증서 설치 절차{#digital-certificate-installation-procedures}

{{eol}}

디지털 인증서를 다운로드하여 설치하는 단계입니다.

1. 웹 브라우저를 열고 [https://aap.adobe.com](https://aap.adobe.com)으로 이동합니다.

   >[!NOTE]
   >
   >이때 브라우저에서 디지털 인증서를 입력하라는 메시지가 표시될 수 있습니다. 이 경우 **[!UICONTROL Cancel]** 을 클릭하여 대화 상자를 닫습니다.

1. 로그인 화면에서 Adobe에서 받은 계정 이름 및 암호를 입력한 다음 을 클릭합니다 **[!UICONTROL login]**.
1. 인스턴스에 대해 발급된 인증서를 찾습니다. [!DNL Report] 서버 (*사용자 이름*.pem)을 클릭하고 ![](assets/btn_save_certificatedownload.PNG) 해당 인증서와 연결된 아이콘입니다.
1. 인증서를 저장하라는 메시지가 표시되면 **[!UICONTROL Save]**&#x200B;을 클릭합니다 .
1. 설치한 디렉토리의 Certificates 폴더에 파일을 다운로드합니다 [!DNL Report Server].

   이 폴더에는 이름이 [!DNL trust_ca_cert.pem]인 인증서 파일이 이미 있습니다. 두 인증서 파일은 항상 있어야 합니다 [!DNL Report] Server to function.
