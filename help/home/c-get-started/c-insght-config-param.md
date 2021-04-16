---
description: Insight.cfg 파일의 매개 변수를 설정하여 네트워크 연결 및 Data Workbench 구성 설정을 지정합니다.
title: 구성 매개 변수
uuid: 6e1248c1-3eae-44a3-8b19-f595d79e8d0d
exl-id: c92fc79f-452d-4839-840a-a3ea9e8754c4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 2%

---

# 구성 매개 변수{#configuration-parameters}

Insight.cfg 파일의 매개 변수를 설정하여 네트워크 연결 및 Data Workbench 구성 설정을 지정합니다.

다음 예제는 기본적으로 [!DNL Insight.cfg] 파일에 포함된 매개 변수만 포함합니다.

**새 레이아웃 보기**

![](assets/config_tree_new_layout.png)

**원본 레이아웃 보기**

![](assets/cfg_Workstation_AddServer.png)

새 [!DNL Insight.cfg] 파일에서 사용할 수 있는 매개 변수 중 일부는 사용 중인 [!DNL Insight.cfg] 파일 버전에서 사용할 수 없습니다. 이러한 매개 변수 중 하나가 필요한 경우 [!DNL Add Custom Key] 매개 변수를 마우스 오른쪽 단추로 클릭한 다음 이름과 유형을 지정하여 [!DNL Insight.cfg] 파일에 추가해야 합니다. 텍스트 편집기를 사용하여 [!DNL .cfg] 파일(Data Workbench 설치 디렉토리에 있음)을 열어 매개 변수를 추가할 수도 있습니다.

다음은 매개 변수 항목을 추가하기 위한 모델로 사용할 수 있는 [!DNL Insight.cfg] 파일에 사용할 수 있는 모든 매개 변수의 예입니다.

```
Licensing = serverInfo:
  Proxy Address = string: 
  Proxy Port = int: 8080
  Proxy User Name = string: 
  Proxy Password = string: 
Servers = vector: 1 items
  0 = serverInfo: 
    Address = string: VS02
    Name = string: Insight Server
    Port = int: 443
    Proxy Address = string: 
    Proxy Password = string: 
    Proxy Port = int: 8080
    Proxy User Name = string: 
    SSL Client Certificate = string: Named User.pem
    SSL Server Common Name = string: VS02
    Use Address File = bool: false
    Use SSL = bool: true
Color Set = int: 0
Default to Online = bool: false
Fonts = vector: 0 items
Gamma = float: 1.6
Maximum Sample Size (MB) = double: 0
Network Location = string: 
Unhide All = bool: false
Unlock = bool: false
Update Software = bool: true
User Folder = string: User\\
Toolbar Icons = bool: false
```

다음 표에서는 사용 가능한 [!DNL Insight.cfg] 파일 매개 변수에 대한 설명을 알파벳 순서로 제공합니다.

<table id="table_4465713A08B649E280A3B4840E829518"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>주소 </p> </td> 
   <td colname="col2"> <p>Data Workbench 서버 컴퓨터의 호스트 이름 또는 숫자 IP 주소입니다. </p> <p>예:<span class="filepath"> vsServer.mycompany.com 또는 192.168.1.90</span> </p> <p><span class="wintitle"> 주소</span>가 지정되지 않은 경우, 주소 파일 사용이 false로 설정된 경우 클라이언트<span class="keyword"> 클라이언트는 SSL 서버 일반 이름 매개 변수에 지정된 공통 이름을 사용합니다.</span> </p> <p> <p>참고:Use Address File 매개 변수가 true로 설정된 경우 Address 매개 변수에 입력한 텍스트는 클라이언트</span>에서 첫 번째 프로필을 연 후 제거할 수 있습니다. <span class="keyword"> 그런 다음 네트워크 위치 매개 변수 설정에 따라 클러스터 주소 파일에서 마스터 서버에 연결하는 데 사용되는 주소가 결정됩니다. </span></p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>색상 세트 </p> </td> 
   <td colname="col2"> <p><span class="keyword"> 클라이언트 응용 프로그램</span>의 배경색을 지정합니다. 옵션은 다음과 같습니다. </p> <p>0 = 검정 </p> <p>1 = 흰색 </p> <p>2 = 단색 </p> <p>기본값은 0, 검정입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기본 온라인 수준 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. Data Workbench 인스턴스가 열릴 때마다 스트리밍, 오프라인 또는 온라인으로 기본적으로 작동되도록 할 수 있습니다. 옵션은 스트리밍, 온라인 또는 오프라인 중 하나입니다. Data Workbench의 기본 구성은 오프라인으로 작업합니다. </p> <p> <p>참고:기본적으로 온라인상에서 작업하기로 결정하기 전에 <a href="../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54"> 오프라인 작업 및 온라인 작업</a>에 나와 있는 이점과 결과를 고려해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>글꼴 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 클라이언트</span>이(가) UTF8 기반 유니코드 특수 문자를 렌더링하는 데 사용해야 하는 글꼴을 나열하는 벡터입니다. <span class="keyword"> 목록의 글꼴 수는 제한이 없습니다. </span></p> <p>첫 번째 글꼴은 항상 Lucida Sans Console이어야 합니다. 이 매개 변수가 <span class="filepath"> Insight.cfg</span> 파일에 포함되지 않은 경우 Data Workbench은 Lucida Sans 콘솔만 사용하여 텍스트를 표시합니다. </p> <p> Data Workbench은 렌더링할 수 없는 문자가 나타날 때까지 목록에 있는 첫 번째 글꼴을 사용하여 모든 문자를 렌더링합니다. 목록의 두 번째 글꼴을 사용하여 해당 문자를 렌더링합니다. 해당 글꼴이 문자를 렌더링하지 않는 경우 Data Workbench은 목록의 세 번째 글꼴을 사용하여 해당 문자를 렌더링하는 등 글꼴 목록의 끝에 도달할 때까지 해당 문자를 렌더링합니다. 올바른 글꼴이 벡터에 나열되지 않으면 Data Workbench은 해당 문자의 16진수 값을 표시합니다. </p> <p> <p>참고: Data Workbench이 실행 중인 동안에는 이 매개 변수를 변경하지 마십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>감마 </p> </td> 
   <td colname="col2"> Data Workbench 표시에 대한 감마 설정입니다. 기본값은 1.6입니다. Adobe에서는 이 값을 변경하는 것이 권장되지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>라이선스 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 서버를 통해 Adobe 라이센스 서버에 연결하는 경우에만 라이센스 벡터에서 매개 변수를 수정해야 합니다. </p> <p>프록시 서버를 통해 Adobe 라이센스 서버에 연결할 수 있도록 <span class="keyword"> 클라이언트</span>를 활성화하는 매개 변수의 섹션 식별자입니다. 라이센스 노드를 확장하고 다음 매개 변수를 완료합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 주소 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. Adobe 라이센스 서버에 액세스하는 데 <span class="keyword"> 클라이언트</span>이(가) 사용해야 하는 프록시 서버의 주소입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 포트 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 서버의 포트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 사용자 이름 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 서버의 사용자 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 암호 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 사용자 이름과 연결된 암호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>최대 샘플 크기(MB) </p> </td> 
   <td colname="col2"> <p>단일 컴퓨터에서 실행 중인 클라이언트</span>에서 사용하는 데이터 캐시에 허용되는 최대 크기를 지정합니다.<span class="keyword"> </span></p> <p><span class="filepath"> Server.cfg</span> 파일의 샘플 바이트 매개 변수가 Data Workbench 서버에 연결하는 모든 <span class="keyword"> 클라이언트</span>(기본적으로 250e6바이트)에 대한 데이터 캐시 크기를 지정하는 동안 Maximum Sample Size 매개 변수를 사용하면 특정 컴퓨터의 데이터 캐시 크기를 추가로 제한할 수 있습니다. 이 기능은 저장 공간 또는 컴퓨팅 성능이 제한된 컴퓨터에 클라이언트가 설치된 경우에 유용합니다. </p> <p> <p>참고:이 매개 변수는 클라이언트 프로그램에서 로컬로 쿼리하는 로컬 데이터 샘플의 크기를 제한합니다. 이와 반대로 <span class="filepath"> cache.db</span> 파일에는 클라이언트가 연결하는 각 프로필에 대한 데이터와 요소 이름 및 해당 차원에 대한 데이터가 포함되어 있습니다. 로컬 쿼리를 실행하려면 <span class="filepath"> cache.db</span> 파일의 이러한 요소 이름 및 차원이 필요합니다. 따라서 데이터 세트에서 요소 수를 줄이는 것 외에 크기를 제한할 방법이 없습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2">선택 사항입니다. <span class="keyword"> 클라이언트</span>이 <span class="keyword"> 서버</span>을(를) 식별하는 데 사용하는 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>네트워크 위치 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. <span class="keyword"> 클라이언트</span>에서 Data Workbench 서버 일반 이름을 IP 주소로 확인하는 데 사용하는 네트워크 위치입니다. 사용 가능한 네트워크 위치는 서버의 주소 파일에 정의됩니다. 자세한 내용은 <i>서버 제품 설치 및 관리 안내서</i>를 참조하십시오. </p> <p>네트워크 위치를 지정하지 않으면 <span class="keyword"> client</span> 는 기본 네트워크 위치 "Insight"를 사용하여 공통 이름을 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>포트 </p> </td> 
   <td colname="col2"> <p><span class="keyword"> 클라이언트가 요청을 보내는 포트입니다. </span> 이 포트 번호는 Data Workbench 서버가 요청을 수신하는 포트와 일치해야 합니다. 일반적으로 보안 연결에 443입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 주소 </p> </td> 
   <td colname="col2"> <p>Data Workbench 서버 컴퓨터에 연결하기 위해 프록시 서버가 필요한 경우 이 매개 변수 및 프록시 포트 매개 변수 이상을 완료해야 합니다. 선택적으로 프록시 사용자 이름 및 프록시 사용자 암호 매개 변수를 완료할 수 있습니다. </p> <p>Data Workbench 서버에 액세스하는 데 클라이언트</span>이(가) 사용해야 하는 프록시 서버의 주소입니다.<span class="keyword"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 암호 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 서버의 암호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 포트 </p> </td> 
   <td colname="col2"> <p>프록시 서버의 포트입니다. 기본값은 8080입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프록시 사용자 이름 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 서버의 사용자 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색 </p> </td> 
   <td colname="col2"> <p><span class="filepath"> Insight.cfg</span>(또는 <span class="filepath"> .cfg</span> 파일)에서 키 이름, 키 유형 또는 값으로 검색하여 항목을 빠르게 찾을 수 있으며, 중첩된 정보를 위해 확장된 대용량 파일을 스크롤할 필요가 없습니다. 차원 이름, 서버 이름 등을 찾을 수 있습니다. </p> <p>데이터를 찾으려면 이 필드에 검색 구문을 입력합니다. 일치 결과에 따라 필드 색상이 변경됩니다. 일치 항목이 강조 표시되고 불일치가 흐리게 표시됩니다. 일치하는 항목이 없으면 검색 필드의 배경이 빨간색으로 바뀝니다. Enter 키를 누르면 구성 트리가 일치하는 모든 위치에 확장되고 일치하지 않는 경우 축소됩니다. </p> <p><span class="wintitle"> 검색</span> 필드에서 정규 표현식을 사용할 수도 있습니다. 예를 들어 re:<span class="filepath"> *zip*</span> "zip"이라는 단어를 포함하는 모든 항목의 경우 </p> <p>검색을 지우려면 <span class="uicontrol"> Escape</span>를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 </p> </td> 
   <td colname="col2"> <p><span class="keyword"> 클라이언트</span>에서 <span class="keyword"> 서버</span> 연결에 대한 벡터 제목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL 클라이언트 인증서 </p> </td> 
   <td colname="col2"> <p>둘 이상의 인증서가 없는 한 선택 사항입니다. 이 Data Workbench 사본에 대한 디지털 인증서를 포함하는 파일의 이름입니다. 디지털 인증서 다운로드 및 설치에서 다운로드한 파일입니다. </p> <p>예:<span class="filepath"> Samantha Smith.pem</span> </p> <p>이 매개 변수를 비워 두면 <span class="keyword"> 클라이언트가 존재하는 모든 인증서를 사용합니다.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL 서버 일반 이름 </p> </td> 
   <td colname="col2"> <p>디지털 인증서에 지정된 Data Workbench 서버의 일반 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>도구 모음 아이콘 </p> </td> 
   <td colname="col2"> <p>False는 워크스테이션 사용자 인터페이스의 아이콘을 끄고 도구 모음에 텍스트를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주소 파일 사용 </p> </td> 
   <td colname="col2"> <p>주소 파일의 설정이 주소 매개 변수 설정을 재정의할지 여부를 지정합니다. 옵션은 true 또는 false입니다. true로 설정된 경우 주소 파일의 설정이 있으면 주소 매개 변수 설정을 무시합니다. 기본값은 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL 사용 </p> </td> 
   <td colname="col2">Data Workbench 서버와 클라이언트</span> 사이의 보안 통신에 SSL이 사용되는지 여부를 지정합니다. <span class="keyword"> 옵션은 true 또는 false입니다. 기본값은 true입니다. </span></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모두 숨김 취소 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 다음 기능 중 하나를 사용하여 숨겨진 모든 지표, 차원 및 필터를 일시적으로 숨김 취소할 수 있습니다. 
     <ul id="ul_B40E28D9FDC0418BBFA9B0A37F4F6913"> 
      <li id="li_E51BAC99AAE949E5886F19557366453A">[배타적] <span class="filepath"> order.txt</span> 파일의 설정 </li> 
      <li id="li_E3D8222BC55D4CEB90BCCAE606711306"><span class="filepath"> order.txt</span> 파일의 옵션 숨기기 </li> 
      <li id="li_2ADE4EFC1F964D0A90B40CFB3D2766E8"><span class="filepath"> .metric</span>, <span class="filepath"> .dim</span> 및 <span class="filepath"> .filter</span> 파일에 매개 변수를 표시합니다. </li> 
      <li id="li_BBCD248A8F33440092B52E407E300FCC"><span class="filepath"> Transformation.cfg</span> 파일의 숨겨진 매개 변수입니다. </li> 
     </ul> </p> <p>이러한 메서드에 대한 자세한 내용은 <a href="../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999"> 메뉴 항목 숨기기</a>를 참조하십시오. </p> <p>옵션은 true 또는 false입니다. 기본 설정은 false입니다. 숨겨진 지표, 차원 및 필터를 일시적으로 숨김 취소하려면 이 매개 변수를 true로 변경합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>잠금 해제 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 잠긴 작업 영역의 잠금을 해제할 수 있는지 여부를 지정합니다. 옵션은 true이고, false입니다. True를 사용하면 잠긴 작업 영역의 잠금을 해제할 수 있고 False를 사용하면 잠금을 해제할 수 없습니다. 기본값은 false입니다. 잠긴 작업 영역에 대한 자세한 내용은 <a href="../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e"> 작업 공간 잠금 해제</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>소프트웨어 업데이트 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. Data Workbench 서버에서 이 <span class="keyword">클라이언트 소프트웨어를 업데이트하도록 허용할지 여부를 지정합니다. </span> 옵션은 true 또는 false입니다. 기본값은 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 폴더 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 각 프로파일에 대한 작업 영역, 지표, 차원 또는 구성 파일의 로컬 복사본이 포함된 폴더의 이름과 위치를 지정합니다. 기본 설정은 Data Workbench 설치 디렉토리 내의 사용자 폴더를 지정하는 사용자\\입니다. </p> <p>이 설정을 변경하면 두 사용자가 동일한 컴퓨터를 공유할 때 유용합니다. 두 사용자를 모두 수용하려면 두 사용자가 액세스할 수 있는 공유 폴더를 지정할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
