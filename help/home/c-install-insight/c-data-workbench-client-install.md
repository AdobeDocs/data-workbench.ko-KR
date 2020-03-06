---
description: 다음은 데이터 워크벤치에서 워크스테이션(클라이언트)을 설치하기 위한 요구 사항 및 권장 사항입니다.
solution: Analytics
title: 워크스테이션 요구 사항
topic: Data workbench
uuid: 3c4ba2e8-efbc-45fe-8ac1-923d070bc710
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# 워크스테이션 요구 사항{#workstation-requirements}

다음은 데이터 워크벤치에서 워크스테이션(클라이언트)을 설치하기 위한 요구 사항 및 권장 사항입니다.

추가 [데이터 워크벤치](https://docs.adobe.com/help/en/data-workbench/using/server-admin-install/c-msr-server.html) 시스템 요구 사항은 서버 시스템 요구 사항을 참조하십시오.

>[!IMPORTANT]
>
>서버, 보고서 서버 및 클라이언트 구성 요소는 64비트 Windows 운영 체제에서 실행되도록 업그레이드됩니다.

**시작하기 전에**

데이터 워크벤치 워크스테이션(클라이언트)을 설치하기 전에 다음 작업을 완료했는지 확인합니다.

* **Windows** 2012 ***Server에서*** MS System Center Endpoint Protection에 대해 *제외된 프로세스를* 다음 실행 파일에 추가합니다.

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**
   이렇게 하면 이러한 인터페이스 실행 파일에 대한 &quot;허용 목록&quot; 권한이 허용됩니다.

* **Microsoft Excel을 설치하여 분석 데이터를 내보냅니다.** 작업 영역의 데이터를 Microsoft Excel( [!DNL .xls] 또는 [!DNL .xlsx]) 파일로 내보내려면 Data Workbench를 설치한 컴퓨터에 Excel이 설치 및 등록되어 있어야 합니다. Excel이 등록되지 않은 경우 Data Workbench에서 처음으로 Excel에 액세스를 시도하면 등록 대화 상자가 표시됩니다. 복사본이 등록되었는지 확실하지 않은 경우 Excel을 수동으로 시작하고 등록 대화 상자가 나타나면 등록 프로세스를 완료합니다.

   >[!NOTE]
   >
   >Data Workbench 6.4가 릴리스되면서 Excel 2007에 대한 지원이 중단되었습니다. 또한 Data Workbench는 64비트 아키텍처용 Microsoft Windows에서만 실행되므로 64비트 버전의 Microsoft Excel도 설치하는 것이 좋습니다.

* **크기가 조절된 작업 영역을 PDF로 인쇄하기 위해 Adobe[!DNL Acrobat]설치** 크기가 조정된 작업 영역을 Adobe PDF 형식으로 인쇄하려면 Data Workbench를 설치한 컴퓨터에 Adobe가 [!DNL Acrobat] 설치되어 있어야 합니다.

* **인쇄 작업 영역에 대한 프린터 액세스 제공** 데이터 워크벤치에서 작업 영역을 인쇄하려면 데이터 워크벤치를 설치한 컴퓨터에 프린터에 액세스할 수 있어야 합니다. Data Workbench는 작업 영역을 색상 또는 단색 프린터로 인쇄할 수 있으며 포스트스크립트 또는 기타 고급 프린터 기능이 필요하지 않습니다. 최적의 결과를 얻으려면 작업 영역을 색상으로 인쇄하는 것이 좋습니다.
* **보안 조치 구현** Data Workbench 컴퓨터에 대한 회사의 일반적인 엔터프라이즈 보안 정책을 따라야 합니다. 기본 목적을 위해 데이터 워크벤치는 포트 80 및 443을 통해 서버와 데이터를 수집하는 서버에만 연결할 수 있는 기능만 필요로 합니다. Data Workbench 소프트웨어를 유지 관리하고 Data Workbench에 최소 10GB의 저장 공간을 할당하는 한, 데이터 워크벤치 하드웨어를 다른 목적으로 사용할 수 있습니다.
* 시각화를 정확하게 렌더링하려면 워크벤치를 설치한 컴퓨터에 적절한 **그래픽 어댑터가** 설치되어 있어야 합니다(아래 그래픽 어댑터 요구 사항 참조).

**데이터 워크벤치 클라이언트 요구 사항**

**운영 체제**

* Microsoft Windows 7 64비트
* Microsoft Windows 8.1 64비트
* Microsoft Windows 10 64비트

>[!NOTE]
>
>Windows XP는 Data Workbench 6.1 이상 버전에서 지원되지 않습니다.

**해상도**

* 필수:1024 x 768(XGA)
* 권장:1920 x 1200(WUXGA)

**그래픽 어댑터**

* 필수:OpenGL 3.2를 지원하는 OpenGL 하드웨어 가속
* 권장:전용 비디오 어댑터(예: NVIDIA 또는 ATI 어댑터)

**프로세서**

* 필수:1.2GHz 이상의 Intel 또는 AMD
* 권장:ICore 2 Duo-Class

**RAM**

* 필수:2GB
* 권장:4GB

**연결**

* 필수:DPU에 대한 512Kbps 링크
* 권장:2Mbps 이상의 DPU 링크

**파일 시스템**

NTFS

**디스크 스토리지**

최소 10GB 이상의 여유 하드 디스크 드라이브 공간

**인쇄**

인쇄 작업 영역 및 보고서를 위한 프린터 액세스(컬러 또는 회색 크기 프린터)

**기타**

* 전용 마우스
* 눈부심 방지 작업 환경
* 매트가 적용된 모니터

