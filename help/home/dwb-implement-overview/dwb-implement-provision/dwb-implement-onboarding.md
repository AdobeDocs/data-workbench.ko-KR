---
description: 다음 단계에 따라 Adobe Analytics Premium(AAP)의 구성 요소인 DWB(Adobe Data Workbench)에 대한 온보딩 프로세스를 시작합니다.
title: DWB Managed Services에 대한 기본 온보딩 지침
uuid: ad44a4eb-00ea-49c7-8401-58976d8fe39e
translation-type: tm+mt
source-git-commit: ded50c4eeadea80156c17a4cad985d0ceddd5500

---


# DWB Managed Services에 대한 기본 온보딩 지침{#basic-onboarding-instructions-for-dwb-managed-services}

다음 단계에 따라 Adobe Analytics Premium(AAP)의 구성 요소인 DWB(Adobe Data Workbench)에 대한 온보딩 프로세스를 시작합니다.

이러한 온보딩 지침은 컨설팅 서비스 없이 Adobe 관리 서비스를 사용하여 단일 보고서 세트로 데이터 워크벤치를 구현하는 고객을 위한 것입니다. DWB를 구현하는 신규 AAP 고객인 경우 Adobe 온보딩 팀이 첫 번째 연락처가 됩니다. Adobe Analytics 표준이나 이전 버전의 DWB에서 업그레이드하는 경우 Adobe 고객 성공 관리자가 도와드립니다.

## 온보딩 정보:What We Need from You {#section-bdeb9aa26dc14e45a6c90920832becaa}

Adobe는 다음 담당자에게 연락합니다.

* DWB의 기본 사용자를 식별하여 네트워크 디렉토리에서 해당 사용자에 대한 인증서를 생성합니다. 또한 주요 사용자는 Adobe 고객 지원 센터와 상호 작용할 수 있는 포인트 역할을 합니다.
* DWB로 로드할 보고서 세트를 식별합니다.

그러면 Adobe Digital Marketing 팀이 정보를 수집하여 프로파일을 만들고 계정을 설정하며 DWB에 대한 구성 파일을 제공합니다.

**Adobe 온보딩 작업**

* Adobe 고객 지원 센터는 DWB 라이센스 계정을 생성합니다. Adobe 고객 지원 센터는 주 사용자에 대한 DWB 인증서를 생성합니다.
* Adobe 고객 지원 센터는 주 사용자를 지원되는 호출 및 문제 해결을 위해 식별된 &quot;지원되는 사용자&quot;로 정의합니다.
* Adobe 고객 지원 센터는 조직에 다운로드할 소프트웨어 패키지를 DWB 라이선스 및 소프트웨어 포털(SoftDocs/Software 및 Docs 프로필)에 로드합니다.
* Adobe TechOps 팀은 DWB에 대한 프로덕션 및 개발 환경 및 프로필(계약에 따라)을 준비합니다.
* Adobe TechOps 팀은 데이터 피드 및 프로필 관리 스크립트를 구성합니다.
* Adobe TechOps 팀은 DWB 구성 파일(Insight.cfg)을 만들어 조직 관련 온보딩 작업을 담당하는 Adobe 온보딩 팀에 보냅니다.

데이터 피드를 사용자 정의하고 자격 증명, 인증서 및 프로필 구성을 생성한 후 Adobe 고객 지원 센터에서 구성 파일과 자격 증명을 보내 다음 단계를 수행합니다.

## 사용자 정의 설치 파일에 액세스 {#section-26962bf57fef435dbd1c5486d4b6f688}

Adobe 고객 지원 센터에서 이러한 설치 파일을 받아 클라이언트 컴퓨터에 DWB 워크스테이션을 설치합니다.

* 사용자 지정 DWB 구성 파일(Insight.cfg)

   클라이언트 컴퓨터의 이 구성 파일에는 관리되는 DWB 서버에 대한 연결이 포함됩니다.

* DWB 설치 마법사 및 기본 사용자 이름으로 필요한 인증서(.pem 파일)를 다운로드하려면 라이선스 포털에 대한 로그인 자격 증명입니다.

**추가 설치 파일 다운로드**

1. 탐색:license.visualsciences.com에서 라이선스 인증서와 DWB 설치 마법사 실행 파일을 다운로드할 수 있습니다.
1. 조직(계정 이름), 기본 사용자의 이름 및 Adobe 고객 지원에서 받은 암호를 입력한 다음 로그인을 클릭합니다.

   >[!NOTE]
   >
   >이때 브라우저가 디지털 인증서를 제시하라는 메시지를 표시할 수 있습니다. 그런 경우 취소를 클릭하여 대화 상자를 닫습니다.

1. 다운로드 섹션에서 Adobe Data Workbench(`<PrimaryUser>`.pem) 인스턴스에 대해 발행된 인증서를 찾아 다운로드합니다.
1. 다운로드 섹션에서 표준 클라이언트 설치 프로그램을 찾아 DWB 설치 마법사(InsightSetup-x.xx.exe 파일)를 다운로드합니다.
1. Adobe 고객 지원 센터에서 파일을 수신하고 다운로드한 후 DWB 설치 마법사를 실행하여 클라이언트 컴퓨터에 워크스테이션 소프트웨어를 설치합니다.

>[!NOTE]
DWB 설치 마법사는 DWB 클라이언트 워크스테이션의 설치 과정을 안내하고 필요한 폴더에 배치할 Insight.cfg 및 `<PrimaryUser>`.pem 파일을 찾습니다. Insight.cfg 파일은 설치된 클라이언트 워크스테이션의 Insight.exe 파일에 있습니다. . `<PrimaryUser>`pem 파일은 trust_ca_cert.pem 파일과 함께 Certificates 폴더에 있습니다. DWB가 작동하려면 모든 인증서 및 구성 파일이 있어야 합니다.

자세한 내용은 DWB 설정 [마법사를 참조하십시오](https://docs.adobe.com/content/help/en/data-workbench/using/install/workstation-setup/install-setup.html).

## DWB 서버에 연결 {#section-8e79c4e07c2a4342a5bb8af6ee7be3c9}

관리 대상 서버는 Adobe 고객 지원 센터에서 수신하고 클라이언트 워크스테이션에 상주하는 Insight.cfg 파일에서 식별됩니다. Adobe TechOps는 서버를 설정하고 Adobe 고객 지원 센터는 이러한 관리 서버 및 프로파일에 대한 참조를 Insight.cfg 파일에 추가한 후 사용자에게 보냅니다. (DWB 설치 마법사 설명서의 12단계에서 서버에 대한 연결 구성 방법이 완료됩니다.)

>[!NOTE]
DWB 클라이언트 워크스테이션의 워크스테이션 구성 작업 공간에서는 연결된 서버와 프로필을 볼 수 있습니다.

**Adobe Managed Services**

・ Adobe TechOps는 네트워크, 데이터 센터, 서버 및 스토리지를 비롯한 인프라를 관리합니다. 인프라 모니터링 및 경고에 대한 응답은 24시간 연중무휴 이며, TechOps 작업이 필요합니다. 다른 경고의 경우 TechOps는 Adobe 고객 지원 센터에 통보하여 연락을 드릴 것입니다.

・ Adobe TechOps는 관리 대상 서버에 대한 유지 관리 및 펌웨어 업데이트를 수행합니다. 다운타임의 원인이 되는 유지 관리를 위해, 최소 2주 전에 고객 지원 센터에서 유지 관리 기간 알림을 받게 됩니다. Adobe TechOps를 사용하면 신속하게 즉각적인 요구 사항을 해결할 수 있습니다. 알림은 긴급성에 따라 달라지며 일정을 알려면 해결됩니다.

・ Adobe TechOps는 데이터를 자동으로 관리하기 위해 예약된 작업을 설정합니다. 분석 피드 데이터는 21:00 보고서 세트 시간부터 매일 저녁 처리 및 변환을 위해 DWB로 이동합니다.

・ Adobe TechOps는 데이터 백업, FTP 계정, 데이터 보관 및 필요한 경우 데이터 전송을 비롯한 다른 Adobe Managed Services를 처리합니다.

・ Adobe TechOps는 기본 프로덕션 클러스터를 구성하여 3개월 동안 롤링 데이터를 재설정하고 매월 재처리합니다. 조회 업데이트(지리적 위치, DeviceAtlas, 표준 분류)도 재처리 작업의 일부로 발생합니다. 기본적으로 작업은 매달 첫 번째 금요일에 실행됩니다. 필요한 경우 고객 지원 센터에서 일정을 수정할 수 있습니다.

자세한 내용은 Adobe 고객 [지원 센터에 문의하십시오](https://helpx.adobe.com/support/programs/enterprise-support-terms.html).
