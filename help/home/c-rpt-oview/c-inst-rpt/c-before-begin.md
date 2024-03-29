---
description: 보고서 서버의 일부 기능이 작동하려면 설치하기 전에 하드웨어 또는 소프트웨어를 제공하고 구성해야 합니다.
title: 시작하기 전에
uuid: cb464fb6-3109-4eff-9c95-f0cf1f8a8c66
exl-id: 5c8bb4c3-fe76-4b4e-960d-113a9927ad59
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# 시작하기 전에{#before-you-begin}

{{eol}}

보고서 서버의 일부 기능이 작동하려면 설치하기 전에 하드웨어 또는 소프트웨어를 제공하고 구성해야 합니다.

## 기본 보고서 서버 요구 사항 {#section-e891eaee79fe4fa98e658426dc3b2777}

출력되는 보고서는 파일 시스템에 배치된 .PNG 이미지 또는 .XLS 스프레드시트의 형식이나 전자 메일로 출력될 수 있습니다. 하드웨어 요구 사항은 [data workbench 클라이언트](https://experienceleague.adobe.com/docs/data-workbench/using/install/c-data-workbench-client-install.html#Data_Workbench_Client_Minimum_System_Requirements).

보고서 서버에 대해 다음 요구 사항이 있습니다.

* 데이터 출력(네트워크 공유 또는 로컬 드라이브)을 위한 파일 시스템에 액세스합니다.
* 구성된 SMTP 서버에 대한 액세스 권한
* Microsoft Excel 2010 64비트 이상 [!DNL Report] 서버. 자세한 내용은 [Office의 서버측 자동화를 위한 고려 사항](https://support.microsoft.com/kb/257757) 추가 정보.

## 추가 요구 사항 {#section-f53d4388656a4dfc90aefe29dfabef89}

* **적절한 그래픽 어댑터를 설치합니다.** 보고서를 올바르게 렌더링하려면 설치한 컴퓨터입니다 [!DNL Report] 서버에 적절한 그래픽 어댑터가 설치되어 있어야 합니다.

* **보고서를 Excel 파일로 생성하려면 Microsoft Excel을 설치합니다.** 보고서를 Microsoft Excel 파일로 생성하고 배포하려면 다음을 수행하십시오( [!DNL .xls] 또는 [!DNL .xlsx]). 보고서 서버를 설치하는 시스템의 경우 해당 버전의 64비트 Microsoft Excel이 설치 및 등록되어 있어야 합니다. Excel이 등록되지 않고 보고서 서버에서 처음으로 Excel에 액세스하려고 하면 Excel에 등록 대화 상자가 표시됩니다. 복사본이 등록되어 있는지 모를 경우 Excel을 수동으로 시작하고 등록 대화 상자가 나타나면 등록 프로세스를 완료합니다.

   >[!NOTE]
   >
   >보고서를 Excel 파일로 생성하면 새 Excel 인스턴스가 열립니다. 이 프로세스에 대한 자세한 내용은 [https://support.microsoft.com/kb/257757](https://support.microsoft.com/kb/257757).

* **전자 메일로 보고서를 배포할 수 있도록 SMTP 서버에 대한 액세스 권한을 제공합니다.** 보고서를 이메일로 배포하려면 보고서 서버가 SMTP 서버에 연결할 수 있어야 하며 이메일 전달 서비스에 대한 적절한 포트를 열어야 합니다.
