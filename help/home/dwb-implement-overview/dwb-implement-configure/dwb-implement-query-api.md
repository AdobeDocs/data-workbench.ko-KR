---
description: 쿼리 API 설정에 대한 빠른 가이드입니다.
title: 쿼리 API 설정
uuid: 521f06a4-65ee-4206-b769-4c1ce6e5fe7d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 쿼리 API 설정{#query-api-setup}

쿼리 API 설정에 대한 빠른 가이드입니다.

쿼리 API를 설정하려면 아래 단계를 따르십시오.

1. 쿼리 API 인증서 획득

   Adobe 이메일 IT Ops 팀으로 이메일을 보내십시오 `Dataworkbench@adobe.com`.

   쿼리 API에 사용할 CN 이름을 제공하십시오( 쿼리 API와 같은 일반 이름 제공 `<Client>` ).

   >[!NOTE]
   >
   >Tech Ops가 인증서를 생성하여 URL로 업로드합니다. 티켓의 성공적인 생성에 대한 TechOps로부터 통보를 받은 후에 Adobe 컨설턴트에게 연락하여 티켓을 돌려 줄 수 있도록 하십시오.

1. API Stunnel 다운로드 및 압축 풀기 컨설턴트가 API-stunnel 파일을 수신합니다.

   Perl이 컴퓨터에 설치되어 있는지 확인하십시오.

   압축을 푼 폴더(파일을 복사하는 폴더 경로)에서 Query API 인증서를 *stunnel* 폴더 내에 복사합니다.

1. Stunnel.conf 구성

   인증서를 복사했던 Stunnel *폴더* 내에 stunnel.conf라는 파일이 ** 있어야 합니다.

   메모장에서 파일을 편집합니다.

   ![](assets/dwb_impl_API1.png)

   다음과 같이 매개 변수를 변경합니다. ![](assets/dwb_impl_API2.png)

   이 파일에서 두 개의 매개 변수를 변경해야 합니다.

   * *인증서* = 인증서의 이름입니다. 이 예에서는 Aadhithiya Ramani QAPI Client.pem입니다.
   * *Connect* = 주 DPU의 서버 이름입니다.

1. Query. *pm*&#x200B;복사

   Query *.pm* 파일은 Insight API 폴더에서 사용할 수 있습니다.

   Query. *pm* 파일을 복사하여 Perl Library 폴더에 붙여 넣습니다(일반적으로 Perl은 *C:\Perl64\lib *이지만 컴퓨터에서 Perl이 설치되어 있는지 확인하십시오.).

1. API- *http.pl* 파일 수정

   api-http.pl 파일은 api-stunnel 폴더에서 사용할 수 있습니다.

   수정할 매개 변수는 하나만

   *내 $profile* = 쿼리 API를 구성하는 프로필 이름입니다.

1. 쿼리 API를 설치합니다.

   시스템에서 명령 프롬프트를 &quot;Administrator&quot;로 열고 아래와 같이 *stunnel* 압축을 푼 디렉토리로 이동합니다. ![](assets/dwb_impl_API3.png)

   Run the following command *.\stunnel -install*. ![](assets/dwb_impl_API4.png)

   명령을 실행하면 *stunnel* 설치 창이 나타납니다.

   >[!NOTE]
   >
   >명령을 실행하면 *stunnel* 설치 창이 나타납니다.

1. 쿼리 API 스턴넬 구성 테스트

   이 프로세스의 최종 단계는 쿼리 API 구성을 테스트하는 것입니다. api-stunnel 디렉토리를 설치하는 데 사용한 명령 프롬프트에서. ![](assets/dwb_impl_API5.png)

   다음 명령을 사용하여 해당 폴더에서 사용할 수 있는 Perl 스크립트를 실행합니다* perl api-http.pl*. ![](assets/dwb_impl_API6.png)

   스크립트를 실행한 후에는 아래 스크린샷과 결과가 같아야 합니다(6단계에서 쿼리 API를 구성한 프로필의 시간 및 기타 매개 변수에 따라 결과의 날짜 및 값이 달라집니다.). ![](assets/dwb_impl_API7.png)

