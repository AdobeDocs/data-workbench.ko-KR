---
description: Insight Server를 시작하고 동시에 Microsoft Windows Service로 등록하는 절차입니다.
title: Insight Server를 Windows 서비스로 등록
uuid: 1b3d53ca-d50f-4520-abf5-6d5c40493b88
exl-id: ba74d4c0-5d99-47a4-8b92-c65d0ec514e2
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 3%

---

# Insight Server를 Windows 서비스로 등록{#registering-insight-server-as-a-windows-service}

Insight Server를 시작하고 동시에 Microsoft Windows Service로 등록하는 절차입니다.

>[!NOTE]
>
>처음으로 [!DNL Insight Server]을(를) 시작하면 Adobe 라이센스 서버에 자동으로 연결하여 디지털 인증서를 등록합니다. 등록 프로세스를 성공적으로 완료하려면 다음 단계를 실행할 때 컴퓨터가 인터넷에 연결되어 있어야 합니다.

**Windows 서비스로 시작  [!DNL Insight Server] 및 등록하려면**

1. 명령 프롬프트를 열고 [!DNL Insight Server]을(를) 설치한 폴더의 bin 하위 디렉터리로 이동합니다.

   예: [!DNL C:\Adobe\Server\bin]

1. 명령 프롬프트에서 다음 명령을 실행하여 [!DNL Insight Server]을 시작하고 Microsoft Windows에서 서비스로 실행되도록 동시에 등록합니다.

   ```
   <filepath>
   InsightServer64.exe /regserver 
   </filepath>
   ```

1. [!DNL Insight Server]이(가) 올바르게 실행되고 있는지 확인하려면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**&#x200B;를 클릭합니다. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 다를 수 있습니다.

   1. 서비스 목록에서 **[!DNL Adobe Insight Server]** 항목을 찾아 상태가 시작이고 시작 유형이 자동인지 확인합니다.
   1. 서비스 제어판을 닫습니다.

1. 시작 중에 [!DNL Insight Server]에 오류가 있는지 확인하려면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**&#x200B;를 클릭합니다. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 다를 수 있습니다.

   1. [!DNL Event Viewer] 창의 왼쪽 창에서 **[!UICONTROL Application]** 로그를 선택합니다.
   1. 오른쪽 창에서 [!DNL Source] 열에 &quot;Adobe&quot;이 있는 이벤트를 찾습니다.
   1. &quot;Adobe&quot;에서 오류가 발견되면 오류를 두 번 클릭하여 [!DNL Event Properties] 창을 표시합니다. 이 창은 오류에 대한 자세한 정보를 제공합니다.

1. [!DNL Applications] 로그 검사를 마치면 이벤트 뷰어를 닫습니다.

[!DNL Insight Server] 설치를 완료했습니다. [!DNL Insight Server] 는 지속적으로 실행되도록 설계되었습니다. 컴퓨터를 다시 시작하면 [!DNL Insight Server]이(가) 자동으로 다시 시작됩니다. [!DNL Insight Server]을(를) 수동으로 시작 및 중지해야 하는 경우 Windows의 서비스 제어판을 사용하여 시작할 수 있습니다. 다음 섹션에 설명된 바와 같이, [!DNL Insight Server] 서비스가 정기적으로 자동으로 다시 시작되도록 구성할 수도 있습니다.

## 자동으로 {#section-f9bb91614513435f84ee55c0ec8edb13} 다시 시작하도록 서비스 구성

[!DNL Insight Server] 이 플러그인은 중단 없이 계속 실행되도록 설계되었습니다. 일반적으로 소프트웨어 업그레이드 또는 인증서 변경이나 특정 시스템 오류가 발생하는 경우 등과 같은 비정기적인 작업을 수행할 때만 중지되거나 시작됩니다. 일반적인 시스템 작업 중에는 [!DNL Insight Server] 서비스를 중지하거나 다시 시작할 필요가 없습니다.그러나 이벤트 메시지를 지우는 것과 같이 주기적으로(일별, 주별 또는 월별) 서비스를 다시 시작하도록 구성할 수 있습니다.

**서비스가 자동으로 다시  [!DNL Insight Server] 시작되도록 구성하려면**

1. [!DNL Insight Server]을(를) 설치한 디렉토리의 [!DNL Components] 폴더로 이동합니다.

   예: [!DNL C:\Adobe\Server\Components]

1. 메모장과 같은 텍스트 편집기를 사용하여 [!DNL ScheduledRestart.cfg]이라는 새 파일을 만듭니다.
1. [!DNL ScheduledRestart.cfg] 파일에 다음 텍스트를 입력합니다.

   ```
   component = ScheduledRestart:  
     Start Time = string: Month DD, YYYY HH:MM:SS TZone 
     Restart Every = string: frequency
   ```

   <table id="table_AC05861E141E4928BE844C8611DEC43D"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> 이 값에 대해... </th> 
      <th colname="col2" class="entry"> 분류에 사용할 </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <i>월 DD, YYYY HH:MM:SS TZone</i> </td> 
      <td colname="col2"> <p><span class="keyword"> Insight Server </span>을(를) 처음으로 다시 시작할 시간입니다. </p> <p>예:2013년 8월 13일 22:30:00 </p> <p> <p>참고: 시간대를 지정해야 합니다. 지정되지 않은 경우 표준 시간대가 시스템 시간으로 기본값이 아닙니다. 일광 절약 시간제 또는 유사한 시계 방향 정책을 구현하려면 Base\Dataset\Timezone directory on the <span class="keyword"> Insight Server </span> 컴퓨터에 적절한 규칙이 포함된 <span class="filepath"> .dst </span> 파일을 저장해야 합니다. 지원되는 표준 시간대 약어 목록과 일광 절약 시간 구현에 대한 정보는 <a href="../../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> 시간대 코드 </a>를 참조하십시오. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <i>주파수</i> </td> 
      <td colname="col2"> <p>다음 값 중 하나: 
       <ul id="ul_C29A40CD8FBB4333B5FA1D9E7DAD35EC"> 
       <li id="li_9FE07DD30C524CBB81C8F7968E7C733E">개월 </li> 
       <li id="li_E5E1B97ED8FB43C0BDA496C620D24A4C">주 </li> 
       <li id="li_E6043B382FAE4B5D85CAADDFA60E4902">일 </li> 
       </ul> </p> <p>시작 시간에 지정된 초기 시간 후에 <span class="keyword"> Insight Server </span>을 다시 시작할 빈도를 나타냅니다. </p> <p>예를 들어 <span class="keyword"> Insight Server </span>이 일주일에 한 번 다시 시작되도록 하려면 이 값을 "week"로 설정합니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. [!DNL ScheduledRestart.cfg] 파일을 저장합니다.

   [!DNL ScheduledRestart.cfg] 파일이 [!DNL Insight Server]을(를) 설치한 디렉토리의 [!DNL Components] 폴더에 있는지 확인합니다.
