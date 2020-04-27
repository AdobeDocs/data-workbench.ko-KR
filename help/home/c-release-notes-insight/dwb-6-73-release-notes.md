---
description: Data Workbench 6.73의 새로운 기능 및 수정 내용
title: 데이터 워크벤치 6.73 릴리스 노트
uuid: bba63a8c-9cb7-4334-b66a-22db92153066
translation-type: tm+mt
source-git-commit: 9552a2f9fe4e450b1e212b38a09f77252a009419

---


# Data Workbench 6.73 Release Notes{#data-workbench-release-notes}

Data Workbench 6.73의 새로운 기능 및 수정 내용

## 수정 사항 {#section-160baf6ea04c45a993777ee4260691ed}

* 사용자가 해상도와 DPI가 높은 일부 하드웨어에 로그인할 수 없는 Workstation 문제를 해결했습니다.
* IMS 로그인을 사용할 때 아카이브 파일 이름에 이메일이 누락되었던 서버의 문제를 수정했습니다.
* OpenSSL을 버전 1.1.0h로 업데이트하여 몇 가지 취약성 문제 해결 방법과 새로운 SSL Cipher가 포함되어 있습니다. 
* 아래 나열된 오픈 소스 라이브러리를 최신 안정된 버전으로 업데이트

   * libssh2 1.8.0
   * Apache Xerces 3.2.1
   * Apache Xalan 1.11
   * libpng 1.6.34
   * libarchive 3.3.2
   * zlib 1.2.11
   * pcre 8.42

* Lookup File 행 수가 지원되는 357913908개 행을 초과할 때 오류 로깅이 추가되었습니다.

## Known issue {#section-f2cb932f6225457a872fb916a78df89a}

* 데이터 워크벤치 워크스테이션 버전 6.73은 데이터 워크벤치 서버 버전 6.61 및 이전 버전에 연결되지 않습니다. 이전 서버 버전은 버전 6.73에서 지원되지 않는 약한 형식의 암호를 사용하므로이전 버전에 대한 지원을 활성화하려면

   1. OpenSSL 버전 1.0.1h에서 지원하는 강력한 암호화 목록을 사용하여 서버의 기본 SSL 암호 목록을 무시합니다. 재정의하려면 &#39;Components&#39; 및 &#39;Components for Processing Server&#39; 디렉토리에 있는 &#39;Communications.cfg&#39; 파일에 &#39;SSL 암호&#39; 키를 추가합니다. 예: `SSL Ciphers = string: !aNULL:AESGCM`

      >[!NOTE]
      >
      >키가 SSL 포트와 동일한 수준에 있는지 확인합니다. 자세한 내용은 통신 [구성 설정을 참조하십시오.](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/config-settings/c-comm-cfg-stgs.html)

   1. 최신 trust_ca_cert.pem 파일을 서버 6.61 및 이전 서버에 배치합니다. 이 설정은 모든 Workstation 6.7x 버전에 적용됩니다.

데이터 워크벤치 5.3 - 5.52에 대한 [보관된 릴리스 노트를](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html) 참조하십시오.
