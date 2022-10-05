---
description: Data Workbench 설치 패키지에 포함된 파일입니다.
title: 설치 패키지에 포함된 파일
uuid: 46cda536-ea71-4840-bd7f-3fe9e0242c33
exl-id: 086fb49c-d492-4670-938b-7ede70a7cd16
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 5%

---

# 설치 패키지에 포함된 파일{#files-included-in-the-installation-package}

{{eol}}

Data Workbench 설치 패키지에 포함된 파일입니다.

다음 디렉토리는 Insight 패키지에 포함되어 있습니다.

## 프로그램 파일 {#section-ddb14bf42cdd4dc7a6b4310a5b4388e4}

워크스테이션 실행 파일(**[!DNL Insight.exe]**) 및 지원 파일은 기본적으로 이 폴더에 설치됩니다.

```
C:\Program Files\Adobe\Adobe Analytics\Data Workbench
```

<table id="table_56BAC85184A04E7680FBB4B36DE73285"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 디렉토리 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.exe </span> </b> </td> 
   <td colname="col2"> Data Workbench 클라이언트 실행 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> insight.ini </span> </b> </td> 
   <td colname="col2"> 언어 및 경로 설정 <span class="filepath"> Appdata </span> 폴더를 입력합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.zbin </span> </b> </td> 
   <td colname="col2"> <p>이제 Data Workbench에서 부동 텍스트 상자를 사용하여 키보드에서 국제 문자를 입력할 수 있는 보조 텍스트 입력 프로세스로서 IME(입력 방법 편집기)를 지원합니다. Data Workbench는 기본적으로 영어로 지원되지만, 가상 중국어 키보드(병음 IME)와 같은 국제 언어를 지원하기 위해 다른 파일을 로드할 수도 있습니다. </p> <p>새 사전 파일 <span class="filepath"> (Insight.zbin) </span>) 는 IME를 지원하기 위해 클라이언트 응용 프로그램에 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> unins000.exe </span></b> </td> 
   <td colname="col2"> 워크스테이션을 제거하고 파일을 삭제하는 실행 파일입니다. </td> 
  </tr> 
 </tbody> 
</table>

## AppData 파일 {#section-afddeedf8d29451f996fa46b2dfe932c}

데이터 파일 (**[!DNL Insight.cfg]**, 프로필, 인증서, 추적 로그 및 사용자 파일)은 기본적으로 다음과 같이 저장됩니다.

```
<filepath>
  C:\Users\<Winuser>\AppData\Adobe\Analytics\DataWorkbench\ 
</filepath>
```

<table id="table_DBA4DBB54C57409C8EC116C686A08560"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 디렉토리 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.cfg </span> </b> </td> 
   <td colname="col2"> Data Workbench 구성 파일입니다. Data Workbench이 작동하는 매개 변수를 정의합니다. 자세한 내용은 <a href="../../../home/c-install-insight/install-setup/c-conn-isvr.md#concept-9f47b2cd7c12492693a2cf810cfc1d9e"> Insight Server에 연결 구성 </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> 기본 </span> </b> </td> 
   <td colname="col2"> <p>Data Workbench에 사용할 프로그램 파일을 포함합니다. </p> <p> <p>참고: 이러한 파일을 제거하거나 변경하면 안 됩니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> 인증서 </span> </b> </td> 
   <td colname="col2"> 인증서 파일 포함, <span class="filepath"> trust_ca_cert.pem </span>, 및 Data Workbench에 대해 이름이 지정된 사용자 디지털 인증서입니다. 자세한 내용은 <a href="../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-4c6a900074d4464fb6ec7862f7e54f10"> 디지털 인증서 다운로드 및 설치 </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> 구성 </span> </b> </td> 
   <td colname="col2"> 워크스테이션 구성에 사용되는 파일을 포함합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Geography </span></b> </td> 
   <td colname="col2"> 지리적 시각화의 그래픽 렌더링용 파일. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Trace </span></b> </td> 
   <td colname="col2"> 워크스테이션에서 생성된 로그 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> 프로필 </span></b> </td> 
   <td colname="col2"> <i>AdobeSC</i>, <i>Predictive Analytics</i> 및 기타 프로필 구성 파일을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> InsightSetup.exe </span></b> </td> 
   <td colname="col2"> 설치 마법사에서 <b> <span class="filepath"> 소프트웨어/인사이트 </span></b> 폴더를 입력합니다. </td> 
  </tr> 
 </tbody> 
</table>
