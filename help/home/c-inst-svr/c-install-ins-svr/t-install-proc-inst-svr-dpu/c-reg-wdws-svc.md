---
description: Insight Server를 시작하고 동시에 Microsoft Windows 서비스로 등록하는 절차입니다.
title: Insight Server를 Windows 서비스로 등록
uuid: 1b3d53ca-d50f-4520-abf5-6d5c40493b88
exl-id: ba74d4c0-5d99-47a4-8b92-c65d0ec514e2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 3%

---

# Insight Server를 Windows 서비스로 등록{#registering-insight-server-as-a-windows-service}

{{eol}}

Insight Server를 시작하고 동시에 Microsoft Windows 서비스로 등록하는 절차입니다.

>[!NOTE]
>
>시작할 때 [!DNL Insight Server] 처음으로 디지털 인증서를 등록하기 위해 Adobe 라이센스 서버에 자동으로 연결됩니다. 등록 프로세스를 성공적으로 완료하려면 다음 단계를 실행할 때 컴퓨터가 인터넷에 연결되어 있어야 합니다.

**시작하려면 [!DNL Insight Server] Windows 서비스로 등록**

1. 명령 프롬프트를 열고 설치한 폴더의 bin 하위 디렉토리로 이동합니다 [!DNL Insight Server].

   예: [!DNL C:\Adobe\Server\bin]

1. 명령 프롬프트에서 다음 명령을 실행하여 시작합니다 [!DNL Insight Server] 또한 Microsoft Windows에서 서비스로 실행하도록 등록하십시오.

   ```
   <filepath>
   InsightServer64.exe /regserver 
   </filepath>
   ```

1. 이를 확인하려면 [!DNL Insight Server] 올바르게 실행되고 있는 경우 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 서비스 목록에서 **[!DNL Adobe Insight Server]** 시작 상태이고 시작 유형이 자동인지 확인합니다.
   1. 서비스 제어판을 닫습니다.

1. 다음을 확인하려면 [!DNL Insight Server] 시작하는 동안 오류가 발생하면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 왼쪽 창에서 [!DNL Event Viewer] 창에서 **[!UICONTROL Application]** 로그.
   1. 오른쪽 창에서 [!DNL Source] 열.
   1. &quot;Adobe&quot;에서 오류가 발견되면 오류를 두 번 클릭하여 [!DNL Event Properties] 창을 엽니다. 이 창에서는 오류에 대한 자세한 정보를 제공합니다.

1. 검사를 마치면 [!DNL Applications] 로그를 사용하여 이벤트 뷰어를 닫습니다.

설치를 완료했습니다. [!DNL Insight Server]. [!DNL Insight Server] 는 지속적으로 실행되도록 설계되었습니다. 시스템을 다시 시작하면 [!DNL Insight Server] 자동으로 다시 시작됩니다. 시작하고 중지해야 하는 경우 [!DNL Insight Server] 수동으로 Windows의 서비스 제어판을 사용하면 됩니다. 다음 섹션에 설명된 대로 선택적으로 구성할 수 있습니다 [!DNL Insight Server] 서비스를 주기적으로 자동으로 다시 시작합니다.

## 서비스를 자동으로 다시 시작하도록 구성 {#section-f9bb91614513435f84ee55c0ec8edb13}

[!DNL Insight Server] 는 중단 없이 계속 실행되도록 설계되었습니다. 일반적으로 소프트웨어 업그레이드 또는 인증서 변경과 같은 빈번한 작업을 수행하거나 특정 시스템 오류가 발생하는 경우에만 중지되거나 시작됩니다. 를 중지하거나 다시 시작할 필요는 없습니다 [!DNL Insight Server] 정상 시스템 작동 중 서비스 하지만 정기적으로(일별, 주별 또는 월별) 다시 시작되도록 서비스를 구성할 수 있습니다. 예를 들어 이벤트 메시지를 지울 수 있습니다.

**를 구성하려면 [!DNL Insight Server] 서비스를 자동으로 다시 시작합니다.**

1. 로 이동합니다 [!DNL Components] 설치한 디렉토리의 폴더 [!DNL Insight Server].

   예: [!DNL C:\Adobe\Server\Components]

1. 메모장과 같은 텍스트 편집기를 사용하여 [!DNL ScheduledRestart.cfg].
1. 에 다음 텍스트를 입력합니다. [!DNL ScheduledRestart.cfg] 파일:

   ```
   component = ScheduledRestart:  
     Start Time = string: Month DD, YYYY HH:MM:SS TZone 
     Restart Every = string: frequency
   ```

   <table id="table_AC05861E141E4928BE844C8611DEC43D"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> 이 값의 경우... </th> 
      <th colname="col2" class="entry"> 분류에 사용할 </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <i>월 DD, YYYY HH:MM:SS TZone</i> </td> 
      <td colname="col2"> <p>원하는 시간 <span class="keyword"> Insight Server </span> 을(를) 처음으로 다시 시작할 예정입니다. </p> <p>예: 2013년 8월 13일 22일:30:EST 00 </p> <p> <p>참고: 표준 시간대를 지정해야 합니다. 지정하지 않은 경우 시간대가 시스템 시간으로 기본값이 아닙니다. 일광 절약 시간제 또는 유사한 클럭 변환 정책을 구현하려면 <span class="filepath"> .dst </span> 파일의 Base\Dataset\Timezone 디렉터리에 적절한 규칙이 들어 있습니다 <span class="keyword"> Insight Server </span> 시스템. 지원되는 표준 시간대 약자 목록 및 일광 절약 시간 구현에 대한 정보는 다음을 참조하십시오 <a href="../../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> 시간대 코드 </a>. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <i>빈도</i> </td> 
      <td colname="col2"> <p>다음 값 중 하나: 
       <ul id="ul_C29A40CD8FBB4333B5FA1D9E7DAD35EC"> 
       <li id="li_9FE07DD30C524CBB81C8F7968E7C733E">월 </li> 
       <li id="li_E5E1B97ED8FB43C0BDA496C620D24A4C">주 </li> 
       <li id="li_E6043B382FAE4B5D85CAADDFA60E4902">일 </li> 
       </ul> </p> <p>원하는 주파수를 나타내려면 <span class="keyword"> Insight Server </span> 시작 시간에 지정된 초기 시간 후에 다시 시작되어야 합니다. </p> <p>예를 들어, <span class="keyword"> Insight Server </span> 일주일에 한 번 다시 시작하려면 이 값을 "주"로 설정합니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. 를 저장합니다 [!DNL ScheduledRestart.cfg] 파일.

   다음 사항을 확인합니다. [!DNL ScheduledRestart.cfg] 파일이 다음 위치에 있습니다. [!DNL Components] 설치한 디렉토리의 폴더 [!DNL Insight Server].
