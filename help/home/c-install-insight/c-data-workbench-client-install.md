---
description: 다음은 Data Workbench에 워크스테이션(클라이언트)을 설치하기 위한 요구 사항 및 권장 사항입니다.
title: 워크스테이션 요구 사항
uuid: 3c4ba2e8-efbc-45fe-8ac1-923d070bc710
exl-id: 35e259e3-3d6d-45c8-a923-2f8de117489d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 2%

---

# 워크스테이션 요구 사항{#workstation-requirements}

{{eol}}

다음은 Data Workbench에 워크스테이션(클라이언트)을 설치하기 위한 요구 사항 및 권장 사항입니다.

자세한 내용은 [서버 시스템 요구 사항](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/c-msr-server.html?lang=en) 추가 Data Workbench 시스템 요구 사항

>[!IMPORTANT]
>
>서버, 보고서 서버 및 클라이언트 구성 요소가 64비트 Windows 운영 체제에서 실행되도록 업그레이드됩니다.

**시작하기 전에**

Data Workbench 워크스테이션(클라이언트)을 설치하기 전에 다음 작업을 완료했는지 확인하십시오.

* **추가** ***제외된 프로세스*** 대상 *Windows 2012 서버의 MS System Center Endpoint Protection* 다음 실행 파일의 경우:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**

   이렇게 하면 허용 목록에 추가하다 이러한 인터페이스 실행 파일에 대한 권한이 활성화됩니다.

* **분석 데이터를 내보내려면 Microsoft Excel을 설치하십시오.** 작업 공간에서 데이터를 Microsoft Excel로 내보내려면 [!DNL .xls] 또는 [!DNL .xlsx]) 파일에서 Excel을 설치하고 등록해야 합니다. Excel이 등록되지 않은 상태에서 Data Workbench이 처음으로 Excel에 액세스하려고 하면 Excel에 등록 대화 상자가 표시됩니다. 복사본이 등록되어 있는지 모를 경우 Excel을 수동으로 시작하고 등록 대화 상자가 나타나면 등록 프로세스를 완료합니다.

   >[!NOTE]
   >
   >Data Workbench 6.4가 릴리스되면서 Excel 2007에 대한 지원이 중단되었습니다. 또한 Data Workbench은 64비트 아키텍처용 Microsoft Windows에서만 실행되므로 64비트 버전의 Microsoft Excel도 설치하는 것이 좋습니다.

* **Adobe 설치 [!DNL Acrobat] 크기가 조정된 작업 공간을 PDF으로 인쇄하기 위해** 크기가 조정된 작업 공간을 Adobe PDF 형식으로 인쇄하려면 Data Workbench을 설치한 컴퓨터에 Adobe이 있어야 합니다 [!DNL Acrobat] 설치되었습니다.

* **인쇄 작업 공간을 위한 프린터에 대한 액세스 제공** Data Workbench에서 작업 영역을 인쇄하려면 Data Workbench을 설치한 컴퓨터에 프린터에 액세스할 수 있어야 합니다. Data Workbench은 작업 공간을 컬러 또는 모노크롬 프린터로 인쇄할 수 있으며 포스트스크립트 또는 기타 고급 프린터 기능은 필요하지 않습니다. 최적의 결과를 얻으려면 Adobe에서 작업 공간을 색상으로 인쇄하는 것이 좋습니다.
* **보안 조치를 구현합니다.** Data Workbench 컴퓨터에 대한 회사의 일반적인 엔터프라이즈 보안 정책을 따라야 합니다. Data Workbench은 서버(포트 80 및 443을 통해)와 데이터를 수집하는 서버에만 연결하는 기능만 필요로 합니다. Data Workbench 소프트웨어를 유지 관리하고 Data Workbench에 최소 10GB의 저장 공간을 할당하는 한 다른 용도로 Data Workbench 하드웨어를 사용할 수 있습니다.
* 시각화를 정확하게 렌더링하려면 워크벤치를 설치하는 컴퓨터에 적절한 기능이 있어야 합니다 **그래픽 어댑터** 설치됨(아래의 그래픽 어댑터 요구 사항 참조).

**Data Workbench 클라이언트 요구 사항**

**운영 체제**

* Microsoft Windows 7 64비트
* Microsoft Windows 8.1 64비트
* Microsoft Windows 10 64비트

>[!NOTE]
>
>Windows XP는 Data Workbench 6.1 이상 버전에서 지원되지 않습니다.

**해상도**

* 필수 여부: 1024 x 768(XGA)
* 권장 사항: 1920 x 1200(WUXGA)

**그래픽 어댑터**

* 필수 여부: OpenGL 3.2를 지원하는 OpenGL 하드웨어 가속
* 권장 사항: 전용 비디오 어댑터(예: NVIDIA 또는 ATI 어댑터)

**프로세서**

* 필수 여부: 1.2GHz 이상 Intel 또는 AMD
* 권장 사항: ICore 2 듀오 클래스

**RAM**

* 필수 여부: 2GB
* 권장 사항: 4GB

**연결**

* 필수 여부: DPU에 대한 512Kbps 링크
* 권장 사항: DPU에 대한 2Mbps 이상 링크

**파일 시스템**

NTFS

**디스크 스토리지**

최소 10GB 이상의 사용 가능한 하드 디스크 드라이브 공간

**인쇄**

작업 공간 및 보고서를 인쇄하기 위한 프린터 액세스(컬러 또는 회색 크기 프린터)

**기타**

* 전용 마우스
* 눈부심 방지 작업 환경
* 무광택 모니터
