---
description: Adobe이 특정 응용 프로그램에 대해 개발한 프로필 및 조회 파일은 데이터 세트에 대한 분석을 활성화하는 지표, 차원 및 작업 영역을 제공하는 내부 프로필입니다.
solution: Analytics
title: 프로필 및 조회 파일 설치
uuid: edc670a6-ebc9-4a20-a66f-81dd4adf7433
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 2%

---


# 프로필 및 조회 파일 설치{#installing-profiles-and-lookup-files}

Adobe이 특정 응용 프로그램에 대해 개발한 프로필 및 조회 파일은 데이터 세트에 대한 분석을 활성화하는 지표, 차원 및 작업 영역을 제공하는 내부 프로필입니다.

Adobe에서 제공하는 기타 모든 내부 프로필과 마찬가지로 이러한 프로필도 변경하지 마십시오. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 이루어져야 합니다.

Adobe은 응용 프로그램에 대한 프로필 및 조회 파일을 [!DNL .zip] 파일로 배포합니다. 각 zip 파일의 이름은 프로파일 및 조회 파일이 포함된 응용 프로그램의 이름입니다. (예: Site v5.2에 대한 프로필 파일을 [!DNL Site52.zip] 포함합니다.) 이 [!DNL .zip] 파일에는 두 개의 폴더( 및 [!DNL Lookups] )가 [!DNL Profiles]있습니다.

>[!NOTE]
>
>응용 프로그램의 프로필 및 조회 파일이 포함된 설치 파일이 아직 없는 경우 시작하기 전에 Adobe FTP 사이트에서 다운로드하십시오.

데이터 집합 프로필을 처리하고 실행하는 컴퓨터에 프로필 및 해당 조회 파일을 [!DNL Insight Server] 설치해야 합니다. 클러스터를 실행 중인 경우 [!DNL Insight Server] 마스터 서버에 파일을 설치해야 합니다. 데이터 집합 프로필에 대한 자세한 내용은 데이터 집합 *구성 안내서를 참조하십시오*.

**Adobe 응용 프로그램의 프로필을 설치하려면**

1. Adobe에서 제공한 [!DNL Profiles] [!DNL .zip] 파일에서 폴더를 엽니다.

1. 파일의 [!DNL Profiles] 폴더 내의 모든 폴더를 [!DNL .zip] 설치 디렉토리 [!DNL Profiles] [!DNL Insight Server] 의 폴더에 복사합니다. 다음 예제와 같이&#x200B; [!DNL ...\Profiles\]*&lt;[!DNL internal profile name]>* 폴더로 [!DNL Insight Server] 끝내려는 것입니다. 실제 프로필 이름은 다를 수 있습니다.

   ![](assets/win_installprofiles.png)

1. 디렉토리&#x200B; [!DNL Profiles\]*의[!DNL dataset profile name]* &lt;> [!DNL Insight Server] 폴더로 이동하여 이 디렉토리에서 [!DNL profile.cfg] 해당 파일을 찾습니다.

   >[!NOTE]
   >
   >프로필을 처음 설치하는 경우 제공된 샘플 프로필을 데이터 세트 프로필로 사용할 수 있습니다. 설치 디렉토리의 [!DNL profile.cfg] 폴더 내에서 샘플 프로필의 파일(이름이 [!DNL profile.cfg.offline]될 수 있음)을 찾을 수 [!DNL Profiles\Sample] [!DNL Insight Server] 있습니다.

1. 메모장과 같은 텍스트 편집기를 사용하여 [!DNL profile.cfg] 파일을 열고 다음을 수행합니다.

   1. 디렉토리 벡터에 내부 프로파일에 대한 항목을 추가합니다. 프로필 이름은 컴퓨터의 [!DNL Profiles] 폴더에 복사한 디렉토리 이름에 [!DNL Insight Server] 해당합니다.

   1. 디렉토리 수를 적절히 업데이트합니다.
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
      >파일 *의 일반 이름에 대해 지정하는* serverCommonName [!DNL profile.cfg] 은 데이터 집합 프로필을 처리하고 실행하는 [!DNL Insight Server] 컴퓨터의 서버 일반 이름에 해당합니다. 데이터 세트 프로필이 클러스터에서 실행되도록 업데이트하는 지침 [!DNL profile.cfg] 은 [!DNL Insight Server] Insight Server 클러스터를 참조하십시오 [](../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-abt-ins-svr-clsters.md).

1. 파일을 저장합니다. 이름이 다르게 지정된 것처럼 파일을 [!DNL profile.cfg] 저장해야 합니다.

**Adobe 응용 프로그램의 조회 파일을 설치하려면**

1. Adobe에서 제공한 [!DNL Lookups] [!DNL .zip] 파일에서 폴더를 엽니다.

1. 파일의 [!DNL Lookups] 폴더 내의 모든 폴더를 [!DNL .zip] 설치 디렉토리 [!DNL Lookups] [!DNL Insight Server] 의 폴더에 복사합니다. 다음 예제와 같이&#x200B; [!DNL ...\Lookups\]*&lt;[!DNL internal profile name]>* 폴더로 [!DNL Insight Server] 끝내려는 것입니다. 실제 프로필 이름은 다를 수 있습니다.

   ![](assets/win_installLookups.png)

