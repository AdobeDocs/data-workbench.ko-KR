---
description: 보고서 포털 내의 액세스 및 권한은 개별 사용자 및 그룹 계정을 사용하여 제어됩니다.
title: Email.asp 파일 편집
uuid: 18251170-0317-4a32-b9e1-4ebf2d7ad123
exl-id: e984f12f-362a-4dee-9af3-6d7a38a178a4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 2%

---

# Email.asp 파일 편집{#edit-the-email-asp-file}

{{eol}}

보고서 포털 내의 액세스 및 권한은 개별 사용자 및 그룹 계정을 사용하여 제어됩니다.

새 계정을 추가하거나 기존 계정을 편집할 때마다 해당 계정에 대해 지정한 이메일 주소로 확인 이메일을 보낼 수 있습니다( 참조) [계정 작업](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d))에서 지정한 이메일 주소로 복사됩니다. [!DNL email.asp] 파일.

>[!NOTE]
>
>계정에 대한 이메일 주소를 지정하고 을(를) 올바르게 구성한 경우에만 알림 이메일이 계정 사용자에게 전송됩니다 [!DNL email.asp] 파일. 계정에 대해 알림 이메일을 보내지 않으려면 계정의 이메일 필드를 비워 둡니다.

이 파일은 `\*PortalName*\PortalASP` 폴더를 입력합니다.

1. IIS가 실행 중인 컴퓨터에서 [!DNL email.asp] 메모장과 같은 텍스트 편집기에 있는 파일입니다.
1. 다음 변수를 설정합니다.

<table id="table_44F52DA266364DF993C40678A28E0F0D">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 이 변수에 대해 를 입력합니다. . . </th>
   <th colname="col2" class="entry"> 이 정보를 제공합니다 . . . </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> smtpserver </td>
   <td colname="col2"> <p>메시지를 보내는 SMTP 서버의 DNS 이름 또는 IP 주소입니다. </p> <p>예: <span class="filepath"> mail.hq.omniture.com</span></p> </td>
  </tr>
  <tr>
   <td colname="col1"> smtpserverport </td>
   <td colname="col2"> SMTP 서버가 연결을 수신하는 포트입니다. 일반적으로 포트 25입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> sendusing </td>
   <td colname="col2"> <p>메시지를 보내는 방법을 나타냅니다. 값은 다음과 같습니다. </p> <p>1 - 로컬로 설치된 SMTP 서비스를 사용하여 메시지를 보냅니다. 스크립트가 실행 중인 컴퓨터에 SMTP 서비스가 설치된 경우 이 값을 사용합니다. </p> <p>2 - 네트워크에서 SMTP 서비스를 사용하여 메시지를 보냅니다. 스크립트가 실행 중인 컴퓨터에 SMTP 서비스가 설치되어 있지 않으면 이 값을 사용합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> smtpconnectiontimeout </td>
   <td colname="col2">해당 시간 <span class="wintitle"> 보고서</span> 연결을 시간 초과하기 전에 SMTP 서버의 응답을 기다려야 합니다. </td>
  </tr>
 </tbody>
</table>

1. 대상 [!DNL NewUserEmail()] 및 [!DNL UpdateUserEmail()] 함수에서 다음 변수를 설정합니다.

   <table id="table_91C5E36B84A94C4097EE5993592BE587">
   <thead>
   <tr>
      <th colname="col1" class="entry"> 이 변수에 대해 를 입력합니다. . . </th>
      <th colname="col2" class="entry"> 이 정보를 제공합니다 . . . </th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td colname="col1"> From </td>
      <td colname="col2">확인 이메일의 보낸 사람 헤더 행에 표시할 텍스트입니다. 이 값은 <span class="wintitle"> CC</span> 값. </td>
   </tr>
   <tr>
      <td colname="col1"> CC </td>
      <td colname="col2"> <p>선택 사항. 새 사용자 계정 및 변경된 사용자 계정에 대한 모든 메시지 사본을 받아야 하는 개인 또는 별칭의 유효한 이메일 주소입니다. 주소는 쉼표(공백 없음)로 구분하여 여러 개의 이메일 주소를 지정할 수 있습니다. </p> <p>예: <span class="filepath"> admin@company.com,joemanager@company.com</span></p> <p> <p>참고: 수신자는 사용자 암호가 포함된 전자 메일의 사본을 받습니다. </p> </p> </td>
   </tr>
   <tr>
      <td colname="col1"> 제목 </td>
      <td colname="col2"> 확인 이메일의 제목 줄에 표시할 텍스트입니다. </td>
   </tr>
   <tr>
      <td colname="col1"> WebPath </td>
      <td colname="col2"> <p>포털의 실제 경로. </p> <p>예: <span class="filepath"> https://portal.omniture.com/Example</span></p> </td>
   </tr>
   <tr>
      <td colname="col1"> 본문 </td>
      <td colname="col2"> <p>자동으로 생성된 이메일에 포함된 텍스트입니다. </p> <p>예를 들어 로그인 정보를 제공하기 위해 전송된 이메일에 포함된 기본 텍스트는 다음과 같습니다.
      <ul id="ul_7FF2E7399AB64D279EC5794AB02C9749">
      <li id="li_7CBCC5CFF9E04776BBC893278785AEE7">웹 포털 로그인 정보는 아래에 제공됩니다. </li>
      <li id="li_5346F0AB3568444B88117C295D8E99C5"><p>사용자 이름: 사용자 이름 </p><p>새 암호: 암호 </p></li>
      <li id="li_B0D1FAE818BA42CF8546796800A1AA08"><p>다음 URL을 사용하여 포털에 액세스할 수 있습니다. </p><p><span class="filepath"> https://WebPath</span></p></li>
      <li id="li_7CD71EBDFA1D418F960040569CD511EB">포털에 로그인하면 <span class="wintitle"> 관리</span> 탭. </li>
      </ul></p> </td>
   </tr>
   </tbody>
   </table>

1. 파일을 저장하고 닫습니다.
