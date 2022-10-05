---
description: Adobe이 특정 애플리케이션용으로 개발한 프로필 및 조회 파일은 데이터 집합을 분석할 수 있도록 해주는 지표, 차원 및 작업 공간을 제공하는 내부 프로필입니다.
title: 프로필 및 조회 파일 설치
uuid: edc670a6-ebc9-4a20-a66f-81dd4adf7433
exl-id: bf9a3bca-e849-47b6-b038-0349f8ec334a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 2%

---

# 프로필 및 조회 파일 설치{#installing-profiles-and-lookup-files}

{{eol}}

Adobe이 특정 애플리케이션용으로 개발한 프로필 및 조회 파일은 데이터 집합을 분석할 수 있도록 해주는 지표, 차원 및 작업 공간을 제공하는 내부 프로필입니다.

Adobe이 제공하는 다른 모든 내부 프로필과 마찬가지로 이러한 프로필은 변경하지 않아야 합니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

Adobe은 응용 프로그램에 대한 프로필 및 조회 파일을 [!DNL .zip] 파일. 각 zip 파일의 이름은 해당 파일에 포함된 프로필 및 조회 파일이 있는 애플리케이션의 이름입니다. (예: [!DNL Site52.zip] 에는 사이트 v5.2의 프로필 파일이 포함되어 있습니다.) 다음 [!DNL .zip] 파일에는 두 개의 폴더( [!DNL Lookups] 및 [!DNL Profiles]).

>[!NOTE]
>
>애플리케이션에 대한 프로필 및 조회 파일이 포함된 설치 파일이 아직 없는 경우 시작하기 전에 Adobe FTP 사이트에서 다운로드하십시오.

프로필과 조회 파일을 [!DNL Insight Server] 데이터 세트 프로필을 처리하고 실행하는 시스템입니다. 를 실행하는 경우 [!DNL Insight Server] 클러스터에서는 마스터 서버에 파일을 설치해야 합니다. 데이터 집합 프로필에 대한 자세한 내용은 *데이터 집합 구성 안내서*.

**Adobe 애플리케이션용 프로필을 설치하려면**

1. 를 엽니다. [!DNL Profiles] 폴더의 [!DNL .zip] Adobe이 제공한 파일입니다.

1. 내의 모든 폴더 복사 [!DNL Profiles] 폴더의 [!DNL .zip] 파일 [!DNL Profiles] 폴더의 [!DNL Insight Server] 설치 디렉토리. [!DNL ...로 끝나야 합니다.\Profiles\]*&lt; [!DNL internal profile name]>* 폴더 [!DNL Insight Server] 다음 예와 같이, 실제 프로필 이름이 다를 수 있습니다.

   ![](assets/win_installprofiles.png)

1. 로 이동합니다&#x200B; [!DNL Profiles\]*&lt; [!DNL dataset profile name]>* 설치한 디렉토리의 폴더 [!DNL Insight Server] 그리고 [!DNL profile.cfg] 이 디렉토리에 있는 파일입니다.

   >[!NOTE]
   >
   >처음으로 프로필을 설치하는 경우 제공된 샘플 프로필을 데이터 세트 프로필로 사용할 수 있습니다. 다음 항목이 있습니다. [!DNL profile.cfg] 파일(이름이 [!DNL profile.cfg.offline])를 사용하십시오 [!DNL Profiles\Sample] 폴더의 [!DNL Insight Server] 설치 디렉토리.

1. 를 엽니다. [!DNL profile.cfg] 메모장과 같은 텍스트 편집기를 사용하여 파일을 만들고 다음을 수행합니다.

   1. 디렉토리 벡터에 내부 프로필에 대한 항목을 추가합니다. 프로필 이름은 복사한 디렉토리의 이름에 해당합니다 [!DNL Profiles] 폴더의 [!DNL Insight Server] 시스템.

   1. 디렉토리 수를 적절하게 업데이트합니다.
   1. 아래 강조 표시된 대로 이 파일의 일반 이름 행에 서버의 일반 이름을 추가합니다.

      ```
      Profile = profileInfo: 
      Directories = vector: n+1 items
        0 = string: Base\\
        1 = string: internal profile name 1\\
        2 = string: internal profile name 2\\
      . . .
        n = string: internal profile name n\\
      Processing Servers = vector: 1 items
        0 = ProfileServerInfo: 
          Common Name = string: serverCommonName
          Server = string: 
      ```

      >[!NOTE]
      >
      >다음 *serverCommonName* 일반 이름을에 지정하는경우입니다. [!DNL profile.cfg] 파일은 [!DNL Insight Server] 데이터 집합 프로필을 처리하고 실행하는 시스템입니다. 업데이트에 대한 지침 [!DNL profile.cfg] 데이터 집합 프로필이 [!DNL Insight Server] 클러스터 [Insight Server 클러스터](../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-abt-ins-svr-clsters.md).

1. 파일을 저장합니다. 파일을 다른 이름으로 저장해야 합니다 [!DNL profile.cfg] 이름이 다르게 지정된 경우

**Adobe 응용 프로그램에 대한 조회 파일을 설치하려면**

1. 를 엽니다. [!DNL Lookups] 폴더의 [!DNL .zip] Adobe이 제공한 파일입니다.

1. 내의 모든 폴더 복사 [!DNL Lookups] 폴더의 [!DNL .zip] 파일 [!DNL Lookups] 폴더의 [!DNL Insight Server] 설치 디렉토리. [!DNL ...로 끝나야 합니다.\조회\]*&lt; [!DNL internal profile name]>* 폴더 [!DNL Insight Server] 다음 예와 같이, 실제 프로필 이름이 다를 수 있습니다.

   ![](assets/win_installLookups.png)
