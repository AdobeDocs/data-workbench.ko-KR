---
description: 쿼리 API 설정에 대한 빠른 안내서입니다.
title: 쿼리 API 설정
uuid: 521f06a4-65ee-4206-b769-4c1ce6e5fe7d
exl-id: 8b9dace8-4dad-434c-aec3-2f6ca872a5f6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---

# 쿼리 API 설정{#query-api-setup}

{{eol}}

쿼리 API 설정에 대한 빠른 안내서입니다.

쿼리 API를 설정하려면 아래 단계를 따르십시오.

1. 쿼리 API 인증서 획득

   Adobe Email의 Tech Ops 팀에 이메일 보내기 - `Dataworkbench@adobe.com`.

   쿼리 API에 사용할 CN 이름을 제공하십시오( 다음과 같은 일반 이름을 제공) `<Client>` 쿼리 API).

   >[!NOTE]
   >
   >Tech Ops에서 인증서를 생성하여 URL로 업로드합니다. 티켓을 성공적으로 생성할 때 Tech Ops로부터 알림을 받은 후 Adobe 컨설턴트에게 알리면 티켓을 다시 받게 됩니다.

1. API Stunnel 다운로드 및 추출. 컨설턴트로부터 api-stunnel 파일을 받습니다.

   Perl이 컴퓨터에 설치되어 있는지 확인하십시오.

   추출된 폴더(파일을 복사하는 폴더 경로)에서 Query API 인증서를 *스턴트* 폴더를 입력합니다.

1. Stunnel.conf 구성

   라는 파일이 있어야 합니다. *stunnel.conf* 내부 *스턴넬* 폴더(인증서를 복사한 위치).

   메모장에서 파일을 편집합니다.

   ![](assets/dwb_impl_API1.png)

   다음과 같이 매개 변수를 변경합니다. ![](assets/dwb_impl_API2.png)

   이 파일에서 두 매개 변수를 변경해야 합니다.

   * *인증서* = 인증서의 이름입니다. 이 예에서는 Aadhitiya Ramani QAPI Client.pem입니다.
   * *Connect* = 주 DPU의 서버 이름입니다.

1. 복사 *Query.pm*.

   다음 *Query.pm* 파일은 Insight API 폴더에서 사용할 수 있습니다.

   를 복사합니다. *Query.pm* 파일을 Perl 라이브러리 폴더에 붙여 넣습니다(일반적으로 *C:\Perl64\lib *이지만 컴퓨터에서 Perl이 설치되어 있는지 확인합니다.).

1. 수정 *api-http.pl* 파일

   api-http.pl 파일은 api-stunnel 폴더에서 사용할 수 있습니다.

   수정할 매개 변수는 하나만

   *내 $profile* = 쿼리 API를 구성하는 프로필 이름입니다.

1. 쿼리 API를 설치합니다.

   시스템에서 명령 프롬프트를 &quot;관리자&quot;로 열고 압축을 푼 디렉토리로 이동합니다 *스턴트* 다음과 같이 표시됩니다. ![](assets/dwb_impl_API3.png)

   다음 명령을 실행합니다 *.\stunnel -install*. ![](assets/dwb_impl_API4.png)

   명령을 실행하면 *스턴트* 가 설치되어 있습니다.

   >[!NOTE]
   >
   >명령을 실행하면 *스턴트* 가 설치되어 있습니다.

1. 쿼리 API 스턴채널 구성 테스트

   이 프로세스의 최종 단계는 쿼리 API 구성을 테스트하는 것입니다. api-stunnel 디렉토리를 설치하는 데 사용한 명령 프롬프트에서 다음을 수행합니다. ![](assets/dwb_impl_API5.png)

   다음 명령* perl api-http.pl*을 사용하여 해당 폴더에서 사용할 수 있는 Perl 스크립트를 실행합니다. ![](assets/dwb_impl_API6.png)

   스크립트를 실행한 후 결과는 아래 스크린샷과 같아야 합니다(결과에 있는 날짜 시간 및 값은 Query API를 구성한 프로필의 다른 매개 변수에 따라 달라집니다(6단계). ![](assets/dwb_impl_API7.png)
