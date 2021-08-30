---
description: Data Workbench 6.73의 새로운 기능 및 수정 사항.
title: Data Workbench 6.73 릴리스 정보
uuid: bba63a8c-9cb7-4334-b66a-22db92153066
exl-id: 911c0cb7-ad95-4dbb-90ff-8e5c40b19f7f
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 26%

---

# Data Workbench 6.73 릴리스 정보{#data-workbench-release-notes}

Data Workbench 6.73의 새로운 기능 및 수정 사항.

## 수정 사항 {#section-160baf6ea04c45a993777ee4260691ed}

* 사용자가 해상도와 DPI가 높은 일부 하드웨어에 로그인할 수 없는 Workstation 문제를 해결했습니다.
* IMS 로그인을 사용할 때 아카이브 파일 이름에 이메일이 누락되는 서버의 문제를 수정했습니다.
* OpenSSL을 버전 1.1.0h로 업데이트하여 몇 가지 취약성 문제 해결 방법과 새로운 SSL Cipher가 포함되어 있습니다. 
* 아래에 나열된 오픈 소스 라이브러리를 최신 안정적인 버전으로 업데이트했습니다

   * libssh2 1.8.0
   * Apache Xerces 3.2.1
   * Apache Xalan 1.11
   * libpng 1.6.34
   * libarchive 3.3.2
   * zlib 1.2.11
   * pcre 8.42

* Lookup File 행 수가 지원되는 357913908개 행을 초과할 때 오류 로깅이 추가되었습니다.

## 알려진 문제 {#section-f2cb932f6225457a872fb916a78df89a}

* Data Workbench 워크스테이션 버전 6.73은 Data Workbench 서버 버전 6.61 이상에 연결되지 않습니다. 이유는 이전 서버 버전에서 버전 6.73에서 지원되지 않는 약한 형식의 cpher를 사용하기 때문입니다. 이전 버전을 지원하려면

   1. OpenSSL 버전 1.0.1h에서 지원하는 강력한 암호화 목록으로 서버의 기본 SSL 암호 목록을 무시합니다. 재정의하려면 &#39;Components&#39; 및 &#39;Components for Processing Server&#39; 디렉토리에 있는 &#39;Communications.cfg&#39; 파일에 &#39;SSL 암호&#39; 키를 추가합니다. 예: `SSL Ciphers = string: !aNULL:AESGCM`

      >[!NOTE]
      >
      >키가 SSL 포트와 동일한 수준에 있는지 확인합니다. 자세한 내용은 [통신 구성 설정](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/config-settings/c-comm-cfg-stgs.html)을 참조하십시오

   1. 서버 6.61 및 이전 서버에 최신 trust_ca_cert.pem 파일을 배치합니다. 이 설정은 모든 Workstation 6.7x 버전에 적용됩니다.

5.3~5.52에 대해서는 [보관된 릴리스 노트](https://experienceleague.adobe.com/docs/data-workbench/using/release-notes/release-notes.html)를 참조하십시오.
