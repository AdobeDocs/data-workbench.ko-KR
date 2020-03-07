---
description: 보고서 서버의 일부 기능이 작동하려면 설치하기 전에 하드웨어 또는 소프트웨어를 제공 및 구성해야 합니다.
solution: Analytics
title: 시작하기 전에
topic: Data workbench
uuid: cb464fb6-3109-4eff-9c95-f0cf1f8a8c66
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# 시작하기 전에{#before-you-begin}

보고서 서버의 일부 기능이 작동하려면 설치하기 전에 하드웨어 또는 소프트웨어를 제공 및 구성해야 합니다.

## 기본 보고서 서버 요구 사항 {#section-e891eaee79fe4fa98e658426dc3b2777}

출력되는 보고서는 파일 시스템에 배치된 .PNG 이미지 또는 .XLS 스프레드시트의 형식이거나 이메일로 전송할 수 있습니다. 하드웨어 요구 사항은 [데이터 워크벤치 클라이언트와](https://docs.adobe.com/content/help/en/data-workbench/using/install/c-data-workbench-client-install.html#Data_Workbench_Client_Minimum_System_Requirements)동일합니다.

보고서 서버에 대해 다음 요구 사항이 있습니다.

* 데이터 출력(네트워크 공유 또는 로컬 드라이브)을 위한 파일 시스템에 액세스
* 구성된 SMTP 서버에 대한 액세스.
* 서버에 설치된 Microsoft Excel 2010 64비트 [!DNL Report] 이상 자세한 [내용은 서버측 Office 자동화에 대한](http://support.microsoft.com/kb/257757) 고려 사항을 참조하십시오.

## 추가 요구 사항 {#section-f53d4388656a4dfc90aefe29dfabef89}

* **적절한 그래픽 어댑터를 설치합니다.** 보고서를 제대로 렌더링하려면 Server를 설치하는 컴퓨터에 [!DNL Report] 적절한 그래픽 어댑터가 설치되어 있어야 합니다.

* **Microsoft Excel을 설치하여 보고서를 Excel 파일로 생성합니다.** 보고서를 생성하여 Microsoft Excel 파일( [!DNL .xls] 또는 [!DNL .xlsx])로 배포하려면 보고서 서버를 설치하는 컴퓨터에 해당 버전의 64비트 Microsoft Excel이 설치 및 등록되어 있어야 합니다. Excel이 등록되지 않은 상태에서 보고서 서버가 처음으로 보고서 서버에 액세스를 시도하면 등록 대화 상자가 표시됩니다. 복사본이 등록되었는지 확실하지 않은 경우 Excel을 수동으로 시작하고 등록 대화 상자가 나타나면 등록 프로세스를 완료합니다.

   >[!NOTE]
   >
   >보고서를 Excel 파일로 생성할 때 새 Excel 인스턴스를 엽니다. 이 프로세스에 대한 자세한 내용은 http://support.microsoft.com/kb/257757을 [참조하십시오](http://support.microsoft.com/kb/257757).

* **SMTP 서버에 대한 액세스 권한을 제공하여 보고서를 이메일로 배포합니다.** 보고서를 이메일로 배포하려면 보고서 서버가 SMTP 서버에 연결할 수 있어야 하며 이메일 전달 서비스에 적합한 포트를 열어야 합니다.

