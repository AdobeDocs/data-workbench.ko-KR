---
description: 이제 FTP 및 SFTP 프로토콜을 사용하여 CSV, TSV, 세그먼트 내보내기 및 헤더로 세그먼트 내보내기 를 사용하여 클라이언트(워크스테이션)에서 서버로 세그먼트 파일을 내보낼 수 있습니다.
title: S/FTP 배달을 사용하여 세그먼트 내보내기
uuid: 4d654368-cbf7-4e7f-8ab9-82f4e0261ac6
exl-id: 0f1dc0a1-f376-47fb-887c-612a654ed0f0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---

# S/FTP 배달을 사용하여 세그먼트 내보내기{#export-a-segment-using-s-ftp-delivery}

{{eol}}

이제 FTP 및 SFTP 프로토콜을 사용하여 CSV, TSV, 세그먼트 내보내기 및 헤더로 세그먼트 내보내기 를 사용하여 클라이언트(워크스테이션)에서 서버로 세그먼트 파일을 내보낼 수 있습니다.

**S/FTP 내보내기 구성 파일 설정**

내보내기 구성을 설정하기 위해, FTP 또는 SFTP 연결을 설정하기 위해 두 개의 새로운 내보내기 구성 파일이 추가되어, Server 세부 사항을 *FTPServerInfo.cfg* 파일 및 자격 증명이 *FTPUserCredentials* 폴더(명령 인수에 지정된 서버 이름에 해당)

* 설정 **FTPServerInfo.cfg** 파일.

   FTP 서버 정보를 입력하고 워크스테이션에서 허용되는 연결 다시 시도를 설정합니다. 다음 위치에서 워크스테이션 또는 서버에서 편집&#x200B; [!DNL Server\Addresses\Export\] **[!DNL FTPServerInfo.cfg]**파일.

   ```
   FTP Servers = vector: 1 items 
     0 = ftpServerInfo:  
       Address = string:  
       Name = string:  
       Port = int: 21 
   Connect Retries = vector: 1 items 
     0 = connectServerRetries:  
       Retries = int: 0 
       Server Name = string:
   ```

* 설정 **FTPUserCredentials.cfg** 파일.

   을 사용하여 서버에 연결할 사용자 자격 증명을 입력합니다. [!DNL Server\Admin\Export\] **[!DNL FTPUserCredentials.cfg]**파일. 이 파일에는 서버에 연결하는 데 필요한 사용자 자격 증명이 포함되어 있으며 워크스테이션(클라이언트)이 아니라 서버에서만 편집할 수 있습니다.

   ```
   FTP User Credentials = vector: 1 items 
     0 = ftpUserCredInfo: 
       User Name = string:  
       User Password = EncryptedString:  
       Server Name = string:  
       Public Key Path = string:  
       Private Key Path = string:  
       Passphrase = EncryptedString:
   ```

   >[!NOTE]
   >
   >인증을 위해 생성하는 SSH 키는 SSH Keygen 명령을 사용할 때 생성되는 SSH 키와 같은 형식이어야 합니다.
   >
   >keygen을 사용하여 SSH 키를 생성하는 예:
   >
   >
   ```
   >ssh-keygen -t rsa -b 4096 -C "<label>"
   >```

   에는 6개의 매개 변수가 있습니다 **FTPUserCredentials.cfg** 다양한 FTP 또는 SFTP 전송에 필요한 파일입니다.

   1. *사용자 이름*
   1. *사용자 암호*
   1. *서버 이름*
   1. *공개 키 경로*
   1. *개인 키 경로*
   1. *암호*

   <table id="table_4EB416DC770D4D1AA4FAD9676C0D680C"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> 프로토콜 </th> 
      <th colname="col2" class="entry"> 매개 변수 </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>FTP </p> </td> 
      <td colname="col2"> <p>매개 변수 1, 2, 3을 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>암호 인증을 사용한 SFTP </p> </td> 
      <td colname="col2"> <p>전송에서 암호 인증을 사용할 때 매개 변수 1, 2, 3을 설정합니다( 명령 인수에서 -p). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>키 인증을 사용한 SFTP </p> </td> 
      <td colname="col2"> <p>전송에서 키 인증을 사용할 때 매개 변수 1, 2, 3, 4, 5, 6을 설정합니다( 명령 인수에서는 -k ). </p> </td> 
      </tr> 
    </tbody> 
    </table>

**FTP 및 SFTP 내보내기 명령 설정**

1. 내보내기 테이블을 엽니다.

   워크스테이션에서 *세부 사항 테이블* 및 내보내기 유형(CSV , TSV, 세그먼트 내보내기 또는 헤더로 세그먼트 내보내기) 중 하나를 선택합니다. 또는 [!DNL .export] 명령 프롬프트에서 파일 및 편집( [내보낼 세그먼트 구성](../../../home/c-get-started/c-exp-data-seg-exp/t-config-sgts-expt.md#task-8857f221fa66463990ec9b60db6db372)).

1. 에서 *명령* 필드에서 내보내기 실행 파일을 가리키도록 설정합니다.

   ```
   ExportIntegration.exe
   ```

1. 설정 *명령 인수* 프로토콜 및 인증에 필요한 아래와 같은 필드입니다.

   **FTP**

   ```
   <Command Arguments> set to  
   <ftp "%file%" ServerName ServerDestinationPath>
   ```

   ![](assets/FTP_Command_arguments.png)

   **SFTP** (인증에 암호를 사용하는 경우)

   ```
   <Command Arguments> set to  
   <sftp "%file%" ServerName ServerDestinationPath -p>
   ```

   **SFTP** (인증에 키를 사용하는 경우)

   ```
   <Command Arguments> set to  
   <sftp "%file%" ServerName ServerDestinationPath -k>
   ```

   ![](assets/SFTP_command_arguments.png)

모든 명령 인수는 필수 항목이며 표시된 대로 입력해야 합니다.

## 개인/공개 키를 사용한 S/FTP 내보내기 {#section-0534424d79a54a47b82594cfa7b3c17f}

개인 및 공개 키를 사용하여 FTP 및 SFTP 내보내기를 구현하려면 다음 폴더에 구성 파일을 넣습니다.

* 장소 **FTPServerInfo.cfg** 에서 [!DNL Server/Addresses/Export/] 폴더를 입력합니다.
* 장소 **FTPUserCredentials.cfg** 에서 [!DNL Server/Admin/Export/] 폴더를 입력합니다.

에는 6개의 매개 변수가 포함되어 있습니다 **FTPServerInfo.cfg** 파일:

1. *사용자 이름*
1. *사용자 암호*
1. *서버 이름*
1. *공개 키 경로*
1. *개인 키 경로 —* 확장 없이 구성 파일에 개인 키 경로를 배치합니다. 예를 들면 다음과 같습니다.

[!DNL Private Key Path = string: E:\\Server\\campaign\\campaignprivatekey]

1. *암호*

FTP는 매개 변수 1, 2 및 3을 사용합니다.

SFTP는 전송에서 암호 인증을 사용할 때 매개 변수 1, 2 및 3을 사용합니다.

SFTP는 키 인증을 사용하여 전송이 완료되면 6개의 매개 변수를 모두 사용합니다. 예를 들어 인증에 키를 사용하는 경우:

[!DNL 'Command Arguments' = sftp "%file%" ServerName ServerDestinationPath -k]

구성 파일이 올바른 위치에 있어야 합니다.

>[!NOTE]
>
>공개 키는 **.pem** 파일을 폴더 위치에 넣을 수 없습니다. Cygwin과 같은 애플리케이션에서 SSH 키 생성 기능을 사용하여 키를 만들 수 있습니다. (Putty는 지원되지 않는 .ppk 형식으로 키를 생성합니다.)
