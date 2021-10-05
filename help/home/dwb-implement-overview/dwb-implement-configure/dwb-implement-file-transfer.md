---
description: DWB의 다양한 파일 전송 방법에 대한 빠른 안내서입니다.
title: 파일 전송 거버넌스
uuid: a3e19f8a-1cc4-437c-9661-408f675109c0
exl-id: a0ecd8e1-6d6f-4811-9869-092837dc9e55
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# 파일 전송 거버넌스{#file-transfer-governance}

DWB의 다양한 파일 전송 방법에 대한 빠른 안내서입니다.

파일 전송 거버넌스는 내부 디렉토리에서 다른 서버나 내부 파일 이동으로 파일을 전송하는 표준 프로세스입니다.

## 다양한 파일 전송 방법 {#section-972bb39ba1954c6ebd35f6d042593efe}

1. AWS (Amazon Web Services)

   1. 아직 설치되어 있지 않은 경우 서버에 AWS 명령줄 인터페이스를 설치하려면 티켓을 올립니다( [https://docs.aws.amazon.com/cli/latest/userguide/installing.html](https://docs.aws.amazon.com/cli/latest/userguide/installing.html) 참조).
   1. 어떻게 확인해? 명령 프롬프트를 사용하여 AWS을 구성하려고 합니다( [https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html) 참조).

1. FTP 서버에서 NAS 디렉토리로 파일을 전송합니다.

   1. ftp 서버에서 NAS 디렉터리로 FTP 오프라인 피드입니다. 아래 세부 사항은 FTP에 필요합니다.

      ftp_username

      ftp_password

      ftp_port

      ftp_address

      ftp_directory

      delete_ftp_files

      ftp_file_extension

      local_directory

      (FTP 세부 사항은 프로젝트 체크리스트에서 확인할 수 있습니다. 파일 전송에 외부 ftp 사용자 사용)

   1. 아래에 첨부된 ftp_winscp_get.pl 스크립트를 사용하고 요구 사항에 따라 예약합니다.

      ftp_winscp_get.pl

      이 스크립트는 E:\scripts\Scripository\Library\Perl에 배치해야 합니다.

      >[!NOTE]
      >
      >저장소 폴더를 사용할 수 없는 경우 폴더를 다운로드하려면 [주별 재처리](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-reprocess-scripting.md#concept-60529e12d6d94386a02c1c6fdedf0295) 를 참조하십시오.

   1. ftp_address의 파일 가용성을 기준으로 스크립트를 예약합니다.
   1. 파일의 이름 지정 규칙은 YYYMMDD-&lt;offline_feed_name>-00이어야 합니다.*

1. 파일을 NAS 디렉토리에서 FTP 서버로 전송합니다.

   1. ftp_winscp_put.pl 스크립트를 사용하고 요구 사항에 따라 예약하십시오.

      이 스크립트는 E:\scripts\Scripository\Library\Perl에 배치해야 합니다.

      스크립트를 실행하려면 아래 세부 사항이 필요합니다.

      ftp_username

      ftp_password

      ftp_port

      ftp_address

      ftp_directory

      delete_ftp_files

      ftp_file_extension

      local_directory

      ```
      #######################################################################################################################
      # PLUGIN NAME HERE
      my $pluginname = "FTP WinSCP";
      # 20140421 Script tp put files on the FTP
      #######################################################################################################################
      # INCLUDE SCRIPOSITORY CORE
      use FindBin;                 # locate this script
      BEGIN {push @INC, $FindBin::Bin}
      require 'core.pl';
      
         # check for the required parameters
       GetOptions('local_directory:s'     => \$local_directory,
                     'source_file_pattern:s' => \$source_file_pattern,
                     'ftp_file_extension:s' => \$ftp_file_extension,
                     'ftp_address=s'  => \$ftp_address,
                     'ftp_username=s'  => \$ftp_username,
                     'ftp_password:s'  => \$ftp_password,
                     'ftp_port:s'   => \$ftp_port,
                     'ftp_directory:s'     => \$ftp_directory,
           'log_directory:s'  => \$log_directory,
                     'error_directory:s'  => \$error_directory,
                     'mail_from:s'  => \$mail_from,
                     'mail_to:s'   => \$mail_to,
                     'host:s'   => \$host,
                     'trigger_directory:s' => \$trigger_directory,
                     'trigger_file_extension:s' => \$trigger_file_extension,
                     'delete_ftp_files:s'  => \$delete_ftp_files,);
      
       # FOR LEFT OVER PARAMS, WE CAN CHECK GLOBAL PARAMS
       check_parameters(@argv);
      
       my $ftp_winscp_script = "winscpscript.txt";
       if (index($trigger_file_extension, '.') != -1) {
        my @trigger_file_extension1=split(/\./,$trigger_file_extension,2);
        $trigger_file_extension =  $trigger_file_extension1[1];
       }
       if (index($ftp_file_extension, '.') != -1) {
        my @ftp_file_extension1=split(/\./,$ftp_file_extension,2);
        $ftp_file_extension =  $ftp_file_extension1[1];
       }
       if ($trigger_file_extension ne "_empty_" && $trigger_directory ne "_empty_") {
         print $trigger_file_extension;
        my $ftp_winscp_trigger_script = "winscpscript_trigger.txt";
        create_winscp_script($ftp_winscp_trigger_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$trigger_directory,$ftp_directory,$delete_ftp_files,"*",$trigger_file_extension);
        sleep(10);
        system("\"E:\\Scripts\\Scripository\\Library\\WinSCP\\WinSCP.exe\" /console /script=$ftp_winscp_trigger_script /log=$logfile");
        $files = getFiles($trigger_directory,$trigger_file_extension,$days_ago,$months_ago);
        my $ftp_file_pattern="";
        my $numberoffiles = @$files;
        my $i=0;
        foreach my $trigger_file(@$files) {
         $i++;
         my $file_string=substr($trigger_file,length($trigger_directory), length($trigger_file)-length($trigger_directory));
         my @file_string1=split(/\./, $file_string, 2);
         if ($i == $numberoffiles) {
          $ftp_file_pattern.=$file_string1[0].".".$ftp_file_extension;
         }
         else {
          $ftp_file_pattern.=$file_string1[0].".".$ftp_file_extension.", ";
         }
      
        }
      
        #unlink($ftp_winscp_trigger_script);
        print $local_directory;
        print $trigger_directory;
        create_winscp_script($ftp_winscp_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$local_directory,$ftp_directory,$delete_ftp_files,$ftp_file_pattern, "");
        runLogger("$pluginname: Sleeping for 10 sec to give enough time for the temp script to be available");
        sleep(10);
        runLogger("$pluginname: FTP started");
        system("\"E:\\Scripts\\Scripository\\Library\\WinSCP\\WinSCP.exe\" /console /script=$ftp_winscp_script /log=$logfile");
        runLogger("$pluginname: FTP ended");
      
       }
       else {
        if ($source_file_pattern eq "_empty_") {
         $source_file_pattern="*";
        }
        else {
         if (index($source_file_pattern, '.') != -1) {
          my @source_file=split(/\./,$source_file_pattern,2);
          $source_file_pattern =  $source_file[0];
         }
        }
        $ftp_file_extension=".".$ftp_file_extension;
      print $local_directory;
        create_winscp_script($ftp_winscp_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$local_directory,$ftp_directory,$delete_ftp_files,$source_file_pattern,$ftp_file_extension);
        runLogger("$pluginname: Sleeping for 10 sec to give enough time for the temp script to be available");
        sleep(10);
        runLogger("$pluginname: FTP started");
        system("\"E:\\Scripts\\Scripository\\Library\\WinSCP\\WinSCP.exe\" /console /script=$ftp_winscp_script /log=$logfile");
        runLogger("$pluginname: FTP ended");
       }
       unlink($ftp_winscp_script);
      
      sub create_winscp_script() {
       my ($ftp_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$local_directory,$ftp_directory,$delete_ftp_files,$file_pattern, $file_extension) = @_;
       open (FTP, "> $ftp_script") or die "Can't open log: $!";
       print FTP "\# Automatically answer all prompts negatively not to stall\n";
       print FTP "option batch on\n\n";
       print FTP "\# Disable overwrite confirmations that conflict with the previous\n";
       print FTP "option confirm off\n\n";
       print FTP "\# Connect using a password\n";
       if ($ftp_port eq "22") {
        print FTP "open sftp://$ftp_username:$ftp_password\@$ftp_address\n\n";
       }
       else {
        print FTP "open ftp://$ftp_username:$ftp_password\@$ftp_address\n\n";
       }
       print FTP "\# Change local directory\n";
       print FTP "lcd \"$local_directory\"\n\n";
       print FTP "\# Change remote directory\n";
       if ($ftp_directory eq "_empty_") {
       }
       else {
        print FTP "cd \"$ftp_directory\"\n\n";
       }
       print FTP "\# Force binary mode transfer\n";
       print FTP "option transfer binary\n\n";
       print FTP "\# Download the file to specified directory\n";
       my @get_files=split(/,/,$file_pattern);
       foreach my $file (@get_files){
        if ($delete_ftp_files eq "Y" || $delete_ftp_files eq "Yes") {
         print FTP "put -nopreservetime -nopermissions -delete $file$file_extension\n";
      
        }
        else {
         print FTP "put -nopreservetime -nopermissions $file$file_extension\n";
      
        }
      
       }
      
       print FTP "\n\n";
       print FTP "\# Disconnect\n";
       print FTP "close\n\n";
       print FTP "\# Exit WinSCP\n";
       print FTP "exit\n\n";
       close(FTP);
       runLogger("$pluginname: creating temporary winscp file");
      
      }
      ```

   1. ftp_address의 파일 가용성을 기준으로 스크립트를 예약합니다.
   1. 파일의 이름 지정 규칙은 YYYMMDD-&lt;offline_feed_name>-00이어야 합니다.*

1. 하나의 NAS 디렉토리에서 다른 NAS 디렉토리로 파일을 전송합니다.

   1. 다른 NAS 디렉토리에 직접 연결하는 파일을 복사하여 붙여넣습니다. 아래 프로세스를 따르십시오.)

      서버에 로그인 -> 실행 -> \\server_name\E$ [새 폴더가 열리고 파일을 직접 복사하거나 이동합니다]

   1. &quot;copy_files.pl&quot; 스크립트를 사용하여 한 서버에서 다른 서버로 파일을 복사하거나 &quot;move_files.pl&quot;을 사용하여 한 서버에서 다른 서버로 파일을 이동합니다. (이러한 파일은 E:\scripts\Scripository에서 사용할 수 있습니다.)
