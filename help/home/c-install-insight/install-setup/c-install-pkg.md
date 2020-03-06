---
description: 데이터 워크벤치 설치 패키지에 포함된 파일.
title: 설치 패키지에 포함된 파일
uuid: 46cda536-ea71-4840-bd7f-3fe9e0242c33
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 설치 패키지에 포함된 파일{#files-included-in-the-installation-package}

데이터 워크벤치 설치 패키지에 포함된 파일.

다음 디렉토리는 Insight 패키지에 포함됩니다.

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
   <td colname="col1"> <b> Insight.exe <span class="filepath"> </span></b> </td> 
   <td colname="col2"> 데이터 워크벤치 클라이언트 실행 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> insight.ini </span></b> </td> 
   <td colname="col2"> Appdata 폴더의 언어와 경로를 <span class="filepath"> 설정합니다 </span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> Insight.zbin <span class="filepath"></span></b> </td> 
   <td colname="col2"> <p>이제 데이터 워크벤치에서는 부동 텍스트 상자를 사용하여 키보드에서 국제 문자를 입력할 수 있는 보조 텍스트 입력 프로세스로 IME(Input Method Editor)를 지원합니다. 데이터 워크벤치는 기본적으로 영어를 지원하지만 가상 중국어 키보드(병음 IME)와 같은 국제 언어를 지원하기 위해 다른 파일을 로드할 수도 있습니다. </p> <p>클라이언트 응용 프로그램에서 IME를 지원하기 위해 새 사전 파일 <span class="filepath"> (Insight.zbin </span>)이 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> unins00.exe </span></b> </td> 
   <td colname="col2"> 워크스테이션 제거 및 파일 삭제 실행 </td> 
  </tr> 
 </tbody> 
</table>

## AppData 파일 {#section-afddeedf8d29451f996fa46b2dfe932c}

데이터 파일(**[!DNL Insight.cfg]**&#x200B;프로필, 인증서, 추적 로그 및 사용자 파일)은 기본적으로 다음과 같이 저장됩니다.

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
   <td colname="col1"> <b> Insight.cfg <span class="filepath"></span></b> </td> 
   <td colname="col2"> 데이터 워크벤치 구성 파일입니다. 데이터 워크벤치가 작동하는 매개 변수를 정의합니다. Insight <a href="../../../home/c-install-insight/install-setup/c-conn-isvr.md#concept-9f47b2cd7c12492693a2cf810cfc1d9e"> 서버에 연결 구성을 </a>참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> 기본 </span></b> </td> 
   <td colname="col2"> <p>데이터 워크벤치에 대한 프로그램 파일을 포함합니다. </p> <p> <p>참고: 이러한 파일을 제거하거나 변경해서는 안 됩니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> 인증서 <span class="filepath"></span></b> </td> 
   <td colname="col2"> 인증서 파일 <span class="filepath"> trust_ca_cert.pem </span>및 데이터 워크벤치에 대한 지정된 사용자 디지털 인증서가 들어 있습니다. 디지털 <a href="../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-4c6a900074d4464fb6ec7862f7e54f10"> 인증서 다운로드 및 설치를 </a>참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> 구성 </span> </b> </td> 
   <td colname="col2"> 워크스테이션 구성에 사용되는 파일을 포함합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> 지리적 <span class="filepath"> 위치 </span></b> </td> 
   <td colname="col2"> 지리적 시각화를 그래픽으로 렌더링하기 위한 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> 추적 <span class="filepath"></span></b> </td> 
   <td colname="col2"> 워크스테이션에서 생성된 로그 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> 프로필 <span class="filepath"> 프로필 </span></b> </td> 
   <td colname="col2"> <i>AdobeSC</i>, <i>예측 분석</i> 및 기타 프로필 구성 파일 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> InsightSetup.exe <span class="filepath"></span></b> </td> 
   <td colname="col2"> Software/Insight <b> 폴더에 클라이언트 컴퓨터를 추가로 설치하려면 설치 마법사를 <span class="filepath"> </span></b> 사용합니다. </td> 
  </tr> 
 </tbody> 
</table>

