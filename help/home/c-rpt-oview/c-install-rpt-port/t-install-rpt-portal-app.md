---
description: 보고서 포털은 ASP(응용 프로그램 서버 페이지) 집합 및 지원 파일로 구성됩니다.
title: 보고서 포털 애플리케이션 파일 설치
uuid: 483a7401-1bb4-4a71-b8c7-e70ff1b129e7
exl-id: 0eb7805c-d8f6-4cfd-834e-babc1818ebc0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 5%

---

# 보고서 포털 애플리케이션 파일 설치{#install-the-report-portal-application-files}

{{eol}}

보고서 포털은 ASP(응용 프로그램 서버 페이지) 집합 및 지원 파일로 구성됩니다.

를 설치하려면 [!DNL Report Portal]로 지정하는 경우 Adobe에서 받은 배포 파일에서 이러한 파일을 추출하여 Microsoft IIS가 실행 중인 시스템에 설치해야 합니다.

**를 설치하려면 [!DNL Report Portal] 애플리케이션 파일**

1. 아직 다운로드하지 않았다면 의 설치 패키지(.zip 파일)를 다운로드하십시오. [!DNL Report Portal] Adobe FTP 사이트입니다.
1. IIS가 실행 중인 컴퓨터에서 설치 패키지의 파일을 임의의 위치로 추출합니다. 이 단계에서는 VSVirtualPortalName 폴더에 다음 하위 폴더와 파일을 설치합니다.

   | 폴더 또는 파일 | 설명 |
   |---|---|
   | [!DNL \data\users.mdb] | 권한이 부여된 목록 포함 데이터베이스 [!DNL Report Portal] 사용자 참조. |
   | [!DNL \PortalASP\] | 구성하는 ASP 파일이 들어 있는 폴더 [!DNL Report Portal]. |
   | [!DNL \PortalFiles\] | 에서 사용하는 지원 파일이 포함된 5개의 하위 폴더(코어, CSS, HTC, 이미지 및 출력)가 포함된 폴더 [!DNL Report Portal]. |
   | [!DNL ReportPortalSetup.xml] | 연결된 가상 디렉터리를 정의하는 데 사용하는 구성 파일입니다. [!DNL Report Portal] (IIS 6.0에서만 사용) |

   디렉토리는 다음과 같습니다.

   ![](assets/rptPort_scrn_installDir.png)

   >[!NOTE]
   >
   >디렉토리 이름은 예제에 표시된 이름과 다를 수 있습니다.

1. VSVirtualPortalName(또는 다른 이름) 폴더의 이름을 루트 가상 디렉터리로 사용할 폴더로 변경합니다 [!DNL Report Portal] (이하 &quot;라 한다) *PortalName*). 가상 디렉터리에 대한 자세한 내용은 다음 섹션을 참조하십시오.
