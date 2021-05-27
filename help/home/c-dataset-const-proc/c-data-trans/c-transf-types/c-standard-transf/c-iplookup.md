---
description: IP 조회 변환은 IP 지리적 위치 또는 IP 지리 인텔리전스 데이터(이러한 데이터의 공급업체에서 제공하며 Adobe에 의해 독점 형식으로 변환됨)를 가져와 데이터를 분석에 사용할 수 있는 지리 정보로 변환합니다.
title: IP 조회
uuid: 6fccee39-761f-4854-a7fd-3f8b453e0698
exl-id: 3e9dba44-8d31-49af-8ce0-fecaf92edeb7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 4%

---

# IP 조회{#iplookup}

IP 조회 변환은 IP 지리적 위치 또는 IP 지리 인텔리전스 데이터(이러한 데이터의 공급업체에서 제공하며 Adobe에 의해 독점 형식으로 변환됨)를 가져와 데이터를 분석에 사용할 수 있는 지리 정보로 변환합니다.

두 개의 [!DNL IPLookup] 변형이 새로 추가 > *변형 유형 *메뉴에 나열됩니다.

* [!DNL IPLookup] 데이터의  [!DNL IP geo-location] 견적

* [!DNL IPLookup] Digital Envoy for  [!DNL IP geo-intelligence] data

[!DNL IPLookup] 변형을 정의할 때 [!DNL IP geo-location] 또는 [!DNL IP geo-intelligence] 데이터에 적절한 변형을 선택합니다.

<table id="table_C438A30AB5E64160A5C486D6887B1D7E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 변환에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 </td> 
   <td colname="col2"> 조회 파일의 경로 및 파일 이름입니다. 상대 경로는 Data Workbench 서버의 설치 디렉토리에 대한 것입니다. 이 파일은 일반적으로 Data Workbench 서버 설치 디렉토리 내의 조회 디렉토리에 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP 주소 </td> 
   <td colname="col2"> IP 주소를 읽을 필드입니다. </td> 
   <td colname="col3"> c-ip </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p>출력 문자열의 이름입니다. </p> <p> <span class="wintitle"> IPLookup</span> Quova 및 <span class="wintitle"> IPLookup</span> Digital Envoy 변환에는 다른 출력 매개 변수가 있습니다. IP 조회 데이터에 적절한 변형을 사용해야 합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예제에서 [!DNL IP geo-location] 데이터(조회 파일 [!DNL Quova.bin])는 나열된 출력 필드를 만드는 데 사용됩니다. 출력(AOL, ASN, 지역 코드 등)을 사용하여 방문자 트래픽의 지리 분석을 위한 차원을 만들 수 있습니다.

![](assets/cfg_TransformationType_IPLookup.png)
