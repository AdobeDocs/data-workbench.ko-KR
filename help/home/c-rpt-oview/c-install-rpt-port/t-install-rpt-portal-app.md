---
description: 보고서 포털은 ASP(응용 프로그램 서버 페이지) 및 지원 파일 세트로 구성됩니다.
solution: Analytics
title: 보고서 포털 애플리케이션 파일 설치
topic: Data workbench
uuid: 483a7401-1bb4-4a71-b8c7-e70ff1b129e7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 포털 애플리케이션 파일 설치{#install-the-report-portal-application-files}

보고서 포털은 ASP(응용 프로그램 서버 페이지) 및 지원 파일 세트로 구성됩니다.

Adobe [!DNL Report Portal]에서 받은 배포 파일에서 이러한 파일을 추출하여 Microsoft IIS가 실행 중인 컴퓨터에 설치해야 합니다.

**응용 프로그램 파일을[!DNL Report Portal]설치하려면**

1. 아직 설치하지 않은 경우 Adobe FTP 사이트에서 해당 설치 패키지(.zip 파일) [!DNL Report Portal] 를 다운로드합니다.
1. IIS가 실행 중인 컴퓨터에서 설치 패키지의 파일을 모든 위치로 추출합니다. 이 단계에서는 VSVirtualPortalName 폴더에 다음 하위 폴더와 파일을 설치합니다.

   | 폴더 또는 파일 | 설명 |
   |---|---|
   | [!DNL \data\users.mdb] | 권한이 있는 [!DNL Report Portal] 사용자 목록이 포함된 데이터베이스. |
   | [!DNL \PortalASP\] | 구성하는 ASP 파일이 들어 있는 [!DNL Report Portal]폴더입니다. |
   | [!DNL \PortalFiles\] | 에서 사용하는 지원 파일이 포함된 5개의 하위 폴더(코어, CSS, HTC, 이미지 및 출력)가 들어 있는 [!DNL Report Portal]폴더. |
   | [!DNL ReportPortalSetup.xml] | IIS 6.0에서만 [!DNL Report Portal] 사용되는 가상 디렉터리를 정의하는 데 사용하는 구성 파일입니다. |

   디렉토리는 다음과 같습니다.

   ![](assets/rptPort_scrn_installDir.png)

   >[!NOTE]
   >
   >디렉토리 이름은 예제에 표시된 이름과 다를 수 있습니다.

1. VSVirtualPortalName(또는 기타 이름) 폴더의 이름을 루트 가상 디렉토리( [!DNL Report Portal] 이하 PortalName이라고 *함)로 변경합니다*. 가상 디렉토리에 대한 자세한 내용은 다음 섹션을 참조하십시오.