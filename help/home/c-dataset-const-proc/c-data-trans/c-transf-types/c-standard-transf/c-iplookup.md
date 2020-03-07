---
description: IPLookup 변환은 IP 지리 위치 또는 IP 지리 정보 데이터(이러한 데이터의 공급업체가 제공하고 Adobe가 독점 포맷으로 변환)를 가져와서 분석에 사용할 수 있는 지리적 정보로 데이터를 변환합니다.
solution: Analytics
title: IPLookup
topic: Data workbench
uuid: 6fccee39-761f-4854-a7fd-3f8b453e0698
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# IPLookup{#iplookup}

IPLookup 변환은 IP 지리 위치 또는 IP 지리 정보 데이터(이러한 데이터의 공급업체가 제공하고 Adobe가 독점 포맷으로 변환)를 가져와서 분석에 사용할 수 있는 지리적 정보로 데이터를 변환합니다.

새로 추가 > *변형 유형 *메뉴에 두 가지 [!DNL IPLookup] 변형이 나열됩니다.

* [!DNL IPLookup] Quova for [!DNL IP geo-location] data

* [!DNL IPLookup] Digital Envoy for [!DNL IP geo-intelligence] data

변형을 정의할 [!DNL IPLookup] 때 [!DNL IP geo-location] 또는 [!DNL IP geo-intelligence] 데이터에 적합한 변형을 선택합니다.

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
   <td colname="col1">  이름  </td> 
   <td colname="col2"> 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
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
   <td colname="col2"> 조회 파일의 경로 및 파일 이름입니다. 상대 경로는 데이터 워크벤치 서버에 대한 설치 디렉토리와 관련이 있습니다. 이 파일은 일반적으로 데이터 워크벤치 서버 설치 디렉토리 내의 조회 디렉토리에 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP 주소 </td> 
   <td colname="col2"> IP 주소를 읽을 필드입니다. </td> 
   <td colname="col3"> c-ip </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p>출력 문자열의 이름입니다. </p> <p> IPLookup <span class="wintitle"> Quova</span> 및 <span class="wintitle"> IPLookup Digital</span> Envoy 변환에는 다른 출력 매개 변수가 있습니다. IP 조회 데이터에 적절한 변환을 사용해야 합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 조회 파일에서 [!DNL IP geo-location] 데이터가 나열된 출력 필드를 만드는 데 [!DNL Quova.bin]사용됩니다. 출력(AOL, ASN, 지역 코드 등)을 사용하여 방문자 트래픽의 지리적 분석을 위한 차원을 만들 수 있습니다.

![](assets/cfg_TransformationType_IPLookup.png)

